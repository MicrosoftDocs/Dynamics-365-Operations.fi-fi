---
title: Prosessioppaan kehys
description: Tässä aiheessa on tietoja prosessiopaskehyksestä kehittäjille, jotka laajentavat varaston mobiiliprosesseja X++:ssa.
author: Mirzaab
ms.date: 11/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mirzaab
ms.search.validFrom: 2018-4-30
ms.dyn365.ops.version: 8
ms.openlocfilehash: 6882c979ad9b37eb4f95a04259b6ac0f0a0edcdc
ms.sourcegitcommit: fd6270dc7f49f93a8155d2b827153b13edb7be8a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/09/2021
ms.locfileid: "7902043"
---
# <a name="process-guide-framework"></a>Prosessioppaan kehys

[!include [banner](../includes/banner.md)]

Tässä aiheessa on tietoja prosessiopaskehyksestä kehittäjille, jotka laajentavat varaston mobiiliprosesseja X++:ssa. Varaston mobiiliprosessit ovat laajennettavissa, koska prosessit jaetaan pieniin vaiheisiin. Kunkin vaiheen liiketoimintalogiikka ja käyttöliittymän kehittäminen on jaettu yksittäisiin luokkiin, mikä mahdollistaa laajennettavuuden.

## <a name="overview-of-the-existing-design"></a>Olemassa olevan rakenteen yleiskatsaus

Varaston mobiilit suoritustyönkulut tulevat näkyviin yksittäisen asiakaspalvelun päätepisteen kautta. Pyyntö saapuu mobiilisovelluksesta XML-merkkijonona, joka sisältää mobiilisovelluksessa esitettävän käyttöliittymän metatiedot sekä käyttäjän syöttämät arvot.

Kun pyyntö vastaanotetaan, ensimmäinen vaihe on tämän XML-tiedoston sarjoituksen purkaminen. **WHSMobileAppServiceXMLTranslator**-luokka muuntaa XML-tiedoston kontiksi, joka sisältää sekä valvontatiedot että istuntotiedot.

Tämän jälkeen kontissa olevien tietojen avulla voidaan johtaa, mitä varastoprosessia käyttäjä suorittaa tai on aloittamassa (edustettuna **WHSWorkExecuteMode**-numeroinnilla), ja siten luoda **WHSWorkExecuteDisplay**-arvon johdetun luokan esiintymä. **displayform()**-menetelmä käynnistetään, mikä johtaa seuraavaan:

-   Käyttäjän tiedot käsitellään (määritetään luokkaan **WHSRFControlData**, mutta joissakin prosesseissa käytetään erityistä logiikkaa ohittamalla **processControl()**-menetelmä).

-   Liiketoimintalogiikka suoritetaan.

-   Siirrytään seuraavaan vaiheeseen.

-   Muodostetaan kontti, joka edustaa uutta käyttöliittymää (yleensä **build…()**-menetelmällä).

Kontti palautetaan kääntäjälle, joka sitten sarjoittaa XML:n ja lähettää sen vastauksena takaisin mobiililaitteeseen.

Seuraavassa sekvenssikaaviossa näkyy suoritustyönkulun yleiskuva. Huomaa, että kaavio on kaavamainen yleiskuvaus, eikä todellisen koodin täydellinen kuvaus.

![Prosessin kaavamainen yleiskuvaus.](media/schematic-overview.png) 

### <a name="reason-for-the-redesign"></a>Uudelleensuunnittelun syy

Edellä esitetty rakenne tarjoaa erittäin yksinkertaisen kehyksen mobiilityönkuluissa käytettyjen prosessien kehittämiseen. Kuten edellä kuitenkin havaittiin, **displayform()**-menetelmille siirtyy monia vastuita. Se delegoi ne muille menetelmille ja luokille, mutta koska konkreettisia luokkavastuita ei ole, tämä tapahtuu epäjohdonmukaisesti eri luokkien välillä. Lisäksi, koska tuettujen skenaarioiden määrä kasvaa luontaisesti, osa näistä luokista voi muuttua melko monimutkaiseksi. Mielenkiintoisempaa tästä tekee vielä, että osa luokista/menetelmistä ohitetaan ja että niitä käytetään uudelleen useissa muodoissa. Tuloksena on erittäin pitkiä menetelmiä, joiden syklomaattinen monimutkaisuus on suurta. Tämä on aiemmin aiheuttanut ylläpito-ongelmia. Näiden menetelmien virheiden korjaaminen on ollut riski- ja regressioaltista.
Esimerkiksi **processWorkLine()**-menetelmään luokassa **WhsWorkExecuteDisplay** viitataan useista prosesseista (oikeastaan mistä tahansa, missä työt suoritetaan).

Yksi vaihtoehto näiden laajennettavuuden takaamiseksi olisi jakaa **displayForm**-menetelmät pienempiin menetelmiin ja ottaa käyttöön laajennettavuuspisteet. Skenaariomatriisin vuoksi kumppaneille olisi kuitenkin haasteellista kirjoittaa laajennuksia ja tarkistaa niitä regressioiden varalta. Lisäksi koodi kasvaisi ennustamattomasti ajan mittaan edellä mainitun jäsennetyn vastuunjaon puuttumisen vuoksi, mikä aiheuttaisi haasteita laadukkaiden laajennusten kehittämisessä.

Tuloksena uudelleensuunnittelu on kestävä vaihtoehto, kun tavoitteena on saavuttaa selkeästi määritettyjä luokkia, joilla on itsenäiset vastuualueet. Luokalla pitäisi olla oltava yksi vastuualue, yksi muutoksen syy ja yksi syytä laajentamiselle.

## <a name="design-overview"></a>Suunnittelun yleiskuvaus

Uudelleensuunnittelussa kehyksessä ydinstrategiassa on kaksi pääperiaatetta: suoritustyönkuun jakaminen yksittäisiin osiin, joilla on hyvin määritetyt vastuualueet, ja hyvin määritettyjen laajennuspisteiden sisällyttäminen kuhunkin komponenttiin.

Uuden kehyksen nimi on ProcessGuide. Tämä johtuu siitä, että näiden luokkien tehtävänä on ohjata käyttäjää liiketoimintaprosessin läpi (toisin kuin raskas asiakas, joka on lomakepohjainen kokemus, jossa käyttäjällä on enemmän joustavuutta vuorovaikutuksessa tietojen kanssa ja siinä, missä järjestyksessä tehtäviä suoritetaan).

> [!NOTE]
> Yksi huomionarvoinen yksityiskohta on WHS-etuliitteen tahallinen pois jättäminen. Vaikka mobiiliprosessit on alun perin otettu käyttöön varastointia varten, ne ovat sen jälkeen rikkoneet rajoja ja toimivat nyt tukena erilaisille tuotannon ja varastonhallinnan prosesseille. Tämän seurauksena viittaus varastoon on jätetty pois kehyksen nimestä.

Komponenttien tunnistamisen ensimmäinen vaihe on tarkastella tuotannon aloitusprosessia (**WhsWorkExecuteDisplayProdStart**-luokka). Tässä on kaavio prosessista.

![Kaavamaisen prosessin kuva.](media/production-start-process-schematic.png)

Toiminnonkulussa tarvitaan seuraavat komponentit:

-   Ohjain, joka yhdistää koko liiketoimintaprosessin.
-   Prosessin vaiheen suorittamisesta vastaava vaihe.
-   Tietojen käsittelijä, joka käsittelee vaiheen tiedot.
-   Sivunmuodostin, joka vastaa vaiheen käyttöliittymän luomisesta.
-   Vaihesiirrosta vastaava siirtymisagentti.
-   Liiketoimintaprosessin suorittamisesta vastaava luokka.

Jos aloitat yllä olevan prosessityönkulun kaavion vaiheen 1 ja aloitat edellisen vaiheen tietojen käsittelyn ja luot lopulta käyttöliittymän, tietojen käsittelyä jatketaan seuraavassa vaiheessa. Tässä luodaan vahva yhteys peräkkäisten vaiheiden jälkeen, mistä tuloksena uusi korkean tason kaavio näyttäisi seuraavanlaiselta:

![Korkean tason kaavamaisen prosessin kuva.](media/high-level-schematic.png)

Seuraavassa ovat uudelleensuunnitellun prosessin pääkomponentit:

-   **ProcessGuideController** – Tämä luokka orkestroi liiketoimintaprosessin yleisen suorittamisen. Se määrittää vaiheen ja siirtymisagentin esiintymän luovat tehtaat, jotka sitten muodostavat prosessin suorittamisen sekä prosessin peruuttamisen tai siitä poistumisen puhdistuslogiikan.

-   **ProcessGuideStep** – Tämä luokka edustaa yhtä yksittäistä vaihetta liiketoimintaprosessissa. Tämä luokka sisältää niiden tehtaiden määritelmän, jotka luovat esiintymiä sivunmuodostimesta, toiminnosta ja tietojenkäsittelijöistä, ja se on vastuussa niiden käynnistämisestä oikeassa järjestyksessä.

-   **ProcessGuideNavigationAgent** – Tämä luokka on vastuussa vaiheiden välillä siirtymisestä. Kun vaihe on valmis, siirtymisagentti vastaa seuraavan vaiheen määrittämisestä ja välittää kaikki parametrit, jotka edellisen vaiheen voi olla tarpeen viestiä seuraavalle.

-   **ProcessGuidePageBuilder** – Tämä luokka vastaa käyttöliittymän esiintymän luomisesta.

-   **ProcessGuideAction** – Tämä luokka edustaa toimintoa, joka näkyy käyttäjälle painikkeena.

-   **ProcessGuideDataProcessor** – Tämä luokka vastaa käyttäjän kenttään syöttämien tietojen käsittelystä.

## <a name="execution-flow"></a>Suoritustyönkulku

Suoritustyönkulun aloituspiste pysyy muuttumattomana. Pyyntö saapuu siis samojen päätepisteiden kautta, ja sitä seuraa XML-tiedoston sarjoituksen purkaminen konttiin. Tämä kontti välitetään sitten kohteeseen **getNextFormState()**.

Tärkeitä huomioon otettavia luokkia on kolme:

-  **ProcessGuideSessionState** – Tämä sisältää istunnon tilatiedot – tilan, hyväksynnän, ohjaimen, suoritettavan vaiheen jne.

-  **ProcessGuidePage** – Tämä sisältää vahvasti kirjoitetun esityksen käyttöliittymän metatiedoista.

-  **ProcessGuideRequest** – Tämä sisältää edellä mainitut kaksi jäseninä ja on vahvasti kirjoitettu esitys mobiililaitteella saadusta pyynnöstä.

Nämä luokat luodaan käyttämällä konttitietoja (sekä tilatietoja että käyttäjän syöttämiä valvontatietoja). Tämä tarjoaa tyyppiturvallisen tavan käyttää ja muuttaa arvoja. Verrattuna kontin toistuvaan käyttöön prosessin aikana tämä on edullista sekä luettavuuden että suorituskyvyn osalta.

Istunnon tilatietoja käytetään oikean **ProcessGuideController**-luokan esiintymän luomiseen. Kun sen esiintymä on luotu, käynnistetään **createResponse()**-menetelmä **ProcessGuideController**-luokassa. Tämä menetelmä on prosessiopaslogiikan aloituspiste. Se palauttaa vastauksen (edustettuna **ProcessGuideResponse**-luokassa) suorittamisen jälkeen. Vastaus muunnetaan sitten takaisin konttiin ja luovutetaan takaisin vanhalle logiikalle, joka sitten sarjallistaa sen XML-muotoon ja lähettää vastauksen takaisin mobiililaitteelle.

Seuraavaksi ohjaimen on löydettävä seuraava suoritettava vaihe. Jos kyseessä on uuden prosessin alku, ohjain kutsuu kohteen **initialStep()** saadakseen prosessin ensimmäisen vaiheen. Tämän jälkeen se kutsuu **execute()**-menetelmän **ProcessGuideStep**-vaiheessa. Tämä menetelmä luo sitten **ProcessGuidePageBuilder**-luokan esiintymän ja kutsuu kohdetta **buildPage()**, joka palauttaa **ProcessGuidePage**-objektin, joka on käyttäjälle esitettävän käyttöliittymän virtuaalinen esitys. Tämän jälkeen vaihe lähettää tuloksen takaisin ohjaimelle, joka sitten tallentaa kulloisenkin istunnon tilan ja palauttaa tuloksen takaisin kohteeseen **getNextFormState()** **ProcessGuideResponse**-luokan muodossa. Sen jälkeen vastaus muunnetaan takaisin konttiin, sarjoitetaan XML-muotoon ja lähetetään takaisin mobiililaitteelle.

Seuraava sekvenssikaavio selittää tämän toiminnonkulun. Huomaa, että tämä on yleisin toiminnonkulku yksinkertaistettuna suunnittelun selittämiseksi.

![Yksinkertaistettu toiminnonkulku.](media/control-flow.png)

Kun käyttäjä toteuttaa toimenpiteen mobiililaitteella napsauttamalla painiketta (tai skannaamalla arvon, mikä yleensä käynnistää oletustoiminnon), pyyntö saapuu **createResponse()**-menetelmään **ProcessGuideController**-luokkaan samaa reittiä. Tällä kertaa kuitenkin ohjain tietää istunnon tilasta, missä vaiheessa käyttäjä on. Vastaavasti se luo asianmukaisen **ProcessGuideStep**-luokan esiintymän ja käynnistää suoritusmenetelmän. **ProcessGuideStep** vuorostaan lukee käyttäjän käynnistämän toiminnon nimen ja luo sitten asianmukaisen **ProcessGuideAction**-luokan esiintymän ja kutsuu sitten kohdetta **execute()**.

**ProcessGuideAction**-luokka vastaa kulloisenkin toiminnon suorittamisesta, vaikka tähän on kaksi merkittävää poikkeusta.

Ensimmäinen on **ProcessGuideOKAction**-luokka. Tämä toiminto tarkoittaa, että käyttäjä haluaa suorittaa vahvistuksen ja siirtyä prosessissa eteenpäin. Sen mukaisesti tämä menetelmä itse asiassa suorittaa vastakutsun ProcessGuideStep-luokkaa, mikä tarkoittaa, että vaihe käynnistää kohteen **processData()** kohteessa **ProcessGuideDataProcessor**. Tämä käsittelee käyttäjän syöttämät tiedot, päivittää vaiheen tilan ja lähettää tuloksen takaisin ohjaimelle. Käsittelijän tuloksesta riippuen, vaihe käynnistää sivunmuodostimen muodostamaan asianmukaisen käyttöliittymän tai määrittää vaiheen tilan valmiiksi. Tämä näkyy alla olevan sekvenssikaavion yläosassa.

Toinen poikkeus on peruutustoiminto, jota sovelletaan luokissa **ProcessGuideCancelResetProcessAction** ja **ProcessGuideCancelExitProcessAction**. Nämä toimenpiteet edustavat tarkoitusta peruuttaa prosessi ja joko palata prosessin alkuun tai poistua prosessista kokonaan. **OK**-toiminnon lailla myös nämä toiminnot suorittavat vastakutsun vaiheeseen, mikä ilmaisee tarkoituksen kohteelle **ProcessGuideController**. Ohjain suorittaa sitten vaihemuuttujien tarpeellisen puhdistuksen ja joko siirtää valvonnan sitten prosessin ensimmäisen tai lopettaa koko prosessin.

Kun vaihe on suoritettu ja jos vaiheen tilaksi on määritetty **Valmis**, ohjain luo **ProcessGuideNavigationAgent**-esiintymän, joka palauttaa seuraavan vaiheen nimen. Tämän jälkeen ohjain luo esiintymän tästä vaiheesta ja käynnistää **execute()**-menetelmän, jolloin sykli jatkuu. Yleensä uusi vaihe käynnistää vastaavan **ProcessGuidePageBuilder**-muodostimen muodostamaan käyttöliittymän seuraavalle näytölle, joka esitetään käyttäjälle ja joka lähetetään sitten takaisin. Tämä työnkulku näkyy alla olevan sekvenssikaavion alaosassa.

![sekvenssikaavio.](media/sequence-diagram.png)

## <a name="building-a-new-process-using-the-processguide-framework"></a>Uuden prosessin luominen ProcessGuide-kehyksen avulla

Paras tapa selittää toiminnonkulku on käyttää sovelluksessa olevaa esimerkkiä eli tuotannon aloitusprosessia.

## <a name="overview-of-the-production-start-process"></a>Tuotannon aloitusprosessin yleiskatsaus

Aloitetaanpa tutustumalla prosessin työnkulkuun. Ensimmäisessä vaiheessa käyttäjältä pyydetään tuotantotilauksen tunnusta.

![Tuotantotunnuksen kysely.](media/production-id-prompt.png)

Kun käyttäjä syöttää tuotantotilauksen tunnuksen, tilausnumero tarkistetaan. Osa suoritettavista tarkistuksista perustuvat siihen, onko tilaus siinä varastossa, johon käyttäjä on kirjautuneena, sekä tilauksen tilaan. Jos tarkistus epäonnistuu, käyttäjä saa virhesanoman. Jos tarkistus onnistuu, käyttäjälle näytetään tuotantotilauksen ja nimikkeen tiedot.

Käyttäjä voi joko palata prosessin alkuun peruuttamalla tai vahvistaa valitsemalla **OK**. Jälkimmäisessä tapauksessa tuotantotilauksen tilaksi tulee **Käynnistetty**, vastaavat kirjauskansiot kirjataan, valvonta siirtyy takaisin ensimmäiseen vaiheeseen ja käyttäjälle näytetään Työ suoritettu -sanoma.


## <a name="creating-the-controller"></a>Ohjaimen luominen

Liiketoimintaprosessin ensimmäinen vaihe on ohjainluokan luominen. Se alkaa **ProcessGuideController**-abstraktiluokasta, joka toteuttaa ohjaimen oletustoimintatavat. Uusi luokan nimi on **ProdProcessGuideProductionStartController**, ja se on varustettu kohteen **StartProdOrder** arvolla **WHSWorkExecuteMode**. Tässä käytetään samaa **SysExtension**-perusteista esiintymän luontia, jota käytettiin **WHSWorkExecuteDisplay**-luokissa. Se auttaa ohjainesiintymän luonnissa, kun käyttäjä suorittaa tämän tilan valikkonimikkeen.

```xpp
[WHSWorkExecuteMode(WHSWorkExecuteMode::StartProdOrder)]
public class ProdProcessGuideProductionStartController extends ProcessGuideController
```

> [!NOTE]
> Luokan nimeämiskaava on **\<FunctionalArea\>ProcessGuide\<Businessprocessname\>Ohjain**. Tätä kaavaa käytetään ohjainluokkiin ja muihin luokkiin laajentamisessa.


## <a name="building-the-first-step"></a>Ensimmäisen vaiheen rakentaminen

Seuraavaksi määritetään ensimmäinen vaihe luomalla **ProdProcessGuidePromptProductionIdStep**-luokka, joka jatkuu kohteesta **ProcessGuideStep**.

Luokan esiintymän luomisen tehtävä osoitetaan vaihetehtaalle, jonka käynnistää **ProcessGuideController**-perusluokka. Tehtaan oletustoteutus luo vaiheen esiintymän nimen perustella. Siten **ProdProcessGuidePromptProductionIdStep**-vaiheen esiintymän luominen ohjaimen ensimmäisenä vaiheena edellyttää kahta asiaa:

-   **ProdProcessGuidePromptProductionIdStep**-luokka on varustettava **ProcessGuideStepName**-määritteellä.

    ```xpp
    [ProcessGuideStepName(classStr(ProdProcessGuidePromptProductionIdStep))] public class ProdProcessGuidePromptProductionIdStep extends ProcessGuideStep
    ```

-   Ohjainluokassa vaiheen nimi on palautettava toteuttamalla **initialStepName()**-abstraktimenetelmä.

    ```xpp
    protected final ProcessGuideStepName initialStepName()
    {
        return classStr(ProdProcessGuidePromptProductionIdStep);
    }
    ````   
    
> [!NOTE]
> **ProcessGuideStepName**-määritteen arvon ei tarvitse olla täsmälleen sama edellä esitetyn luokan nimen kanssa. Saman nimen käyttäminen kuitenkin mahdollistaa yhdenmukaisuuden ja typpiturvallisuuden ristiviittauksien osalta, kun luokkaa käytetään. Tätä nimeämiskäytäntöä suositellaan.
>
> Vaiheen esiintymän **ProcessGuideStepName**-perusteinen luonti toteutetaan **ProcessGuideStepDefaultFactory**-luokassa. Siinä harvinaisessa tapauksessa, että vaiheen esiintymän luomiselle halutaan eri strategia, on tehtävä seuraavaa:
> -   On luotava uusi tehdasluokka, joka periytyy kohteesta **ProcessGuidStepAbstractFactory**.
> -   Vaihtoehtoisesti voidaan luoda uusi parametriluokka, joka panee täytäntöön **ProcessGuideIStepCreationParameters**-liittymän, joka sisältää tehtaan tarvitsemat parametrit.
> -   Ohjainluokassa on ohitettava menetelmät **stepFactory()** ja **stepCreationParameters()**, jotta palautteena saadaan edellä mainittu tehdas ja parametrit.

Seuraavana vaiheena on **ProdProcessGuidePromptProductionIdStep**-luokan toimintojen täytäntöönpano. Tässä on toteutettava käyttöliittymän rakentamisen, käyttäjän syöttämien tietojen käsittelyn ja vaiheen valmistumisen määrittämisen logiikka.

### <a name="building-the-user-interface-for-the-first-step"></a>Ensimmäisen vaiheen käyttöliittymän rakentaminen

Käyttöliittymä rakennetaan käyttäen **ProcessGuidePageBuilder**-abstraktiluokasta periytyvää luokkaa. Tässä vaiheessa luokka nimetään sen toimintaa vastaavasti: **ProdProcessGuidePromptProductionIdPageBuilder**.

Luokan esiintymänluontimekanismi vastaa sitä, miten vaiheen esiintymä luotiin ohjaimesta. 

-   **ProdProcessGuidePromptProductionIdPageBuilder**-luokka varustetaan **ProcessGuidePageBuilderName**-määritteellä.

    ```xpp
    [ProcessGuidePageBuilderName(classStr(ProdProcessGuidePromptProductionIdPageBuilder))] public class ProdProcessGuidePromptProductionIdPageBuilder extends ProcessGuidePageBuilder
    ```

-   Tämän nimi palautetaan toteuttamalla **ProdProcessGuidePromptProductionIdStep**-luokassa abstraktimenetelmä **pageBuilderName()**.

    ```xpp
    protected final ProcessGuidePageBuilderName pageBuilderName()
    {
        return classStr(ProdProcessGuidePromptProductionIdPageBuilder);
    }
    ```    

> [!TIP]
> Samoin kuin vaihetehtaassa myös sivunmuodostintehtaassa käytetään abstraktia tehdaskaaviota. Siten siinä harvinaisessa tapauksessa, että sivunmuodostumisen esiintymän luomiselle halutaan eri strategia, voi tehdä seuraavaa:
> - Vuot luoda uuden tehdasluokan, joka periytyy kohteesta **ProcessGuidePageBuilderAbstractFactory**.
> - Vaihtoehtoisesti voit luoda uuden parametriluokan, joka panee täytäntöön **ProcessGuideIPageBuilderCreationParameters**-liittymän, joka sisältää tehtaan tarvitsemat parametrit.
> - Vaiheluokassa ohitetaan menetelmät **pageBuilderFactory()** ja **pageBuilderCreationParameters()**, jotta palautteena saadaan edellä mainittu tehdas ja parametrit.

Käyttöliittymän toteuttamiseen tarvitaan sivu, jossa on yksi tekstiruutu tuotantotilaustunnuksen syöttämistä varten, **OK**-painike ja **Peruuta**-painike. **Peruuta**-painikkeella on voitava poistua prosessista.

Tämän toteuttamiseksi on ohitettava kaksi **ProdProcessGuidePromptProductionIdPageBuilder**-luokan menetelmää:

-   Lisää tekstiruutu **addDataControls()**-menetelmällä.

    ```xpp
    protected final void addDataControls(ProcessGuidePage _page)
    {
        _page.addTextBox(ProcessGuideDataTypeNames::ProdId, "@SYS4398", extendedTypeNum(ProdId));
    }
    ```   

-   Lisää **OK**- ja **Peruuta**-painikkeet **addActionControls()**-menetelmällä.

    ```xpp
    protected final void addActionControls(ProcessGuidePage _page)
    {
        #ProcessGuideActionNames
        _page.addButton(step.createAction(#ActionOK), true);
        _page.addButton(step.createAction(#ActionCancelExitProcess));
    }
    ``` 

Tällä lisätään tietojen ohjausobjektit sekä painikkeet. Jos kuitenkin haluat rakentaa näytön, jossa on sekaisin tiedon ohjausobjekteja ja painikkeita, voit saada joustavuutta ohittamalla **addControls()**-menetelmän.

Kannattaa myös harkita, miten sivu rakennetaan uudelleen, jos esiintyy epäonnistuneita tarkistuksia – esimerkiksi, jos käyttäjä syöttää virheellisen tuotantotilaustunnuksen. **ProcessGuidePageBuilder**-perusluokka toteuttaa oletustoimintatavan, joka rakentaa käyttöliittymän uudelleen, tyhjentää skannatun arvon ja lisää virheohjauksen virhesanomineen. Koska tämä on oletustoimintatapa, jota kannattaa käyttää, virheiden käsittelyä varten ei tarvitse lisätä koodia.

> [!TIP]
> Jos haluat toteuttaa mukautettua käyttöliittymätoimintaa virhetilanteissa, voit ohittaa yhden tai useamman menetelmistä **rebuildFromRequestPage()**, **isErrorState()** ja **reuseRequestPageOnError()**.

### <a name="processing-the-user-entered-data-in-the-first-step"></a>Käyttäjän syöttämien tietojen käsittely ensimmäisessä vaiheessa

Tietojen käsittely tapahtuu **ProcessGuideDataProcessorDefault**-luokassa, joka vuorostaan käynnistää vanhan **WhsRfControlData**-luokan. Tähän oletustoimintatapaan ei tarvitse tehdä muutoksia, ja kohteessa **WhsRfControlData** on jo logiikka **ProdId**-kentän tarkistamista varten. Tämän käsittelyä varten ei siis tarvitse kirjoittaa logiikkaa. Jos tarkistuslogiikkaa on laajennettava, harkitse **WhsControl**-perusteisen laajennusmekanismin käyttöä.

### <a name="determine-if-the-first-step-is-complete"></a>Ensimmäisen vaiheen valmiuden määrittäminen

Kun tarkistus on läpäisty, on aika merkitä vaihe valmiiksi. Tämä tehdään perusluokassa, mutta sinun on pantava täytäntöön vaiheen valmiuden määrittämisen ehto. Seuraava ohitettu menetelmä tekee sen.

```xpp
protected final boolean isComplete()
{
    WhsrfPassthrough pass = controller.parmSessionState().parmPass();
    ProdId prodId = pass.lookup(ProcessGuideDataTypeNames::ProdId);
        return (prodId != '');
}
```   

### <a name="step-two-view-order-details-and-confirm"></a>Vaihe kaksi: Tilaustietojen tarkastelu ja vahvistus

Prosessin toisessa vaiheessa käyttäjälle näytetään näyttö, jossa on tilauksia koskevia tietoja. Käyttäjä voi vahvistaa tuotantotilauksen aloittamisen **OK**-painikkeella tai palata prosessin alkuun valitsemalla **Peruuta**. Anna tässä esimerkissä vaiheelle nimeksi **ProdProcessGuideConfirmProductionOrderStep** ja sivunmuodostimen luokan nimeksi **ProdProcessGuideConfirmProductionOrderPageBuilder**.

ProdProcessGuideConfirmProductionOrderStep-luokka näyttää seuraavalta.

```xpp
[ProcessGuideStepName(classStr(ProdProcessGuideConfirmProductionOrderStep))]
public class ProdProcessGuideConfirmProductionOrderStep extends ProcessGuideStep
{
    protected final ProcessGuidePageBuilderName pageBuilderName()
    {
        return classStr(ProdProcessGuideConfirmProductionOrderPageBuilder);
     }
}
```     

Koska käyttäjä ei syötä tässä arvoja, **isComplete()**-menetelmää ei tarvitse ohittaa. Vaihe on valmis, kun käyttäjä valitsee **OK**.

Sivunmuodostinluokka ohittaa **addDataControls()**-menetelmän lisätäkseen kolme otsikkoa. Ensimmäisessä otsikossa näkyy tuotantotilauksen tunnus, toinen sisältää nimiketietoja (kuten nimikkeen tunnuksen, mitat tai kuvauksen) ja kolmas sisältää määrän ja mittayksikön.

Tämän jälkeen **addActionControls()** ohitetaan kahden painikkeen lisäämiseksi eli **OK**-painikkeen ja **Peruuta**-painikkeen, jolla prosessi perutaan ja palataan prosessin alkuun.

```xpp
/// <summary>
/// The <c>ProdProcessGuideConfirmProductionOrderPageBuilder</c> builds a page that allows the user to see details of a production order
/// and then confirm.
/// </summary>
[ProcessGuidePageBuilderName(classStr(ProdProcessGuideConfirmProductionOrderPageBuilder))]
public class ProdProcessGuideConfirmProductionOrderPageBuilder extends ProcessGuidePageBuilder
{
    protected void addDataControls(ProcessGuidePage _page)
    {
        WhsrfPassthrough pass = controller.parmSessionState().parmPass();
        ProdTable prodTable = ProdTable::find(pass.lookup(ProcessGuideDataTypeNames::ProdId));
        UnitOfMeasureSymbol inventUOM = InventTableModule::find(prodTable.ItemId, ModuleInventPurchSales::Invent).UnitId;
        
        _page.addLabel(ProcessGuideDataTypeNames::ProdIdLabelName, strFmt("@WAX1684", prodTable.ProdId), extendedTypeNum(ProdId));
        _page.addLabel(ProcessGuideDataTypeNames::ItemInfo, this.generateItemInfoForProdId(pass.lookup(ProcessGuideDataTypeNames::ProdId)), extendedTypeNum(WHSRFUndefinedDataType));
        _page.addLabel(ProcessGuideDataTypeNames::QtyLabelName, strFmt("@WAX1685", WHSWorkExecuteDisplay::num2StrDisplay(ProdUpdStartUp::proposalStartUpQty(prodTable.ProdId)), inventUOM), extendedTypeNum(WHSRFQuantityAndUOM));

        if (PdsGlobal::pdsIsCWItem(prodTable.ItemId))
        {
            _page.addLabel(ProcessGuideDataTypeNames::InventQtyLabelName, strFmt("@WAX1685", WHSWorkExecuteDisplay::num2StrDisplay(ProdUpdStartUp::pdsCWProposalStartupQty(prodTable.ProdId)), PdsCatchWeightItem::pdsCWUnitId(prodTable.ItemId)), extendedTypeNum(WHSRFQuantityAndUOM));
        }
    }

    protected void addActionControls(ProcessGuidePage _page)
    {
        #ProcessGuideActionNames
        _page.addButton(step.createAction(#ActionOK), true);
        _page.addButton(step.createAction(#ActionCancelResetProcess));
    }
```

> [!NOTE]
> Saman X++-menetelmien lähdekoodin löytää tästä aiheesta käyttämällä sovellusten hallintaa. Suodata luokan nimen perusteella, napsauta luokan nimeä hiiren kakkospainikkeella ja valitse **Näytä koodi**.

### <a name="step-3-start-the-production-order"></a>Vaihe 3: Tuotantotilauksen käynnistys

Kolmannessa vaiheessa suoritetaan tuotantotilauksen käynnistämisen liiketoimintalogiikka. Tämä vaihe eroaa edellisistä vaiheista jonkin verran, sillä tässä vaiheessa ei ole käyttöliittymää. Tämä vaihe suoritetaan hiljaisesti, kun käyttäjä valitsee edellisessä vaiheessa **OK**.

**ProcessGuideStepWithoutPrompt**-abstraktiluokka toteuttaa tällaisten vaiheiden oletustoimintatavan. Siten tämän vaiheen pitäisi laajentaa **ProcessGuideStepWithoutPrompt**-luokkaa ja ohittaa **doExecute()**-menetelmä.

Seuraavassa koodiesimerkissä näytetään luokka ja **doExecute()**-menetelmän täytäntöönpano. Tämä menetelmä yksinkertaisesti noutaa tilaustunnuksen ja käyttäjätunnuksen istunnon tilasta ja käynnistää menetelmän tämän tuotantotilauksen käynnistämiseksi.

```xpp
/// <summary>
/// The <c>ProdProcessGuideStartProductionOrderStep</c> represents a step that starts a production order.
/// </summary>
[ProcessGuideStepName(classStr(ProdProcessGuideStartProductionOrderStep))]
public class ProdProcessGuideStartProductionOrderStep extends ProcessGuideStepWithoutPrompt
{
    protected final void doExecute()
    {
        WhsrfPassthrough pass = controller.parmSessionState().parmPass();
        WHSUserId userId = pass.lookup(ProcessGuideDataTypeNames::UserId);
        ProdTable prodTable = ProdTable::find(pass.lookup(ProcessGuideDataTypeNames::ProdId));
        WhsWorkExecute workExecute = WhsWorkExecute::construct();
        workExecute.prodStartUp(prodTable.ProdId, ProdUpdStartUp::proposalStartUpQty(prodTable.ProdId), userId);

        this.addProcessCompletionMessage();

        super();
    }

}
```

Poikkeuksien kohdalla kehyksen poikkeuksienhallintalogiikka varmistaa, että prosessi palautetaan edelliseen vaiheeseen.

> [!NOTE]
> Käynnistämistä varten **addProcessCompletionMessage** lisää siirtymisparametreihin Työ valmis -sanoman. Tämä sanoma näkyy seuraavassa vaiheessa (olettaen, että siinä on käyttöliittymä). Perusluokat käsittelevät tämän logiikan, eikä prosessiluokkiin tarvitse lisätä tiettyä koodia tämän toimintatavan saavuttamiseksi.


### <a name="building-the-navigation-through-the-steps"></a>Vaiheiden läpi siirtymisen rakentaminen

**ProcessGuideController**-perusluokka luo **ProcessGuideNavigationAgentDefault**-luokan esiintymän, joka perustuu esimääritettyyn siirtymisreittiin, joka on yksinkertainen lähde- ja kohdevaiheiden kartta. Tämä toteutus riittää tuotannonaloitusskenaariossa, koska ehdollista haarautumista ei ole. Siten siirtymisreitin määrittämistä varten on vain ohitettava **initializeNavigationRoute()**-menetelmä.

```xpp
    protected ProcessGuideNavigationRoute initializeNavigationRoute()
    {
        ProcessGuideNavigationRoute navigationRoute = new ProcessGuideNavigationRoute();
        navigationRoute.addFollowingStep(classStr(ProdProcessGuidePromptProductionIdStep), classStr(ProdProcessGuideConfirmProductionOrderStep));
        navigationRoute.addFollowingStep(classStr(ProdProcessGuideConfirmProductionOrderStep), classStr(ProdProcessGuideStartProductionOrderStep));
        navigationRoute.addFollowingStep(classStr(ProdProcessGuideStartProductionOrderStep), classStr(ProdProcessGuidePromptProductionIdStep));

        return navigationRoute;
    }
```

Joissakin prosesseissa esiintyy ehdollista haarautumista (käyttäjätoiminnan tai muiden ehtojen perusteella). Tällaisten prosessien on tehtävä seuraavaa:

-   Toteuttaa tiettyjä siirtymisagentteja, jotka periytyvät luokasta **ProcessGuideNavigationAgent**.

-   Toteuttaa tietty siirtymisagenttitehdas, joka periytyy **ProcessGuideNavigationAgentAbstractFactory**-luokasta. Se sisältää logiikan, jolla luodaan esiintymä oikeasta siirtymisagentista, kulloisenkin vaiheen, istunnon tilan, käyttäjän toimen tai muun logiikan perusteella.

-   Vaihtoehtoisesti voit ohittaa **navigationAgentCreationParameters()**-ohjainluokassa soveltuvien parametrien välittämistä varten.

-   Ohittaa **navigationAgentFactory()** ohjaimessa yllä luodun siirtymisagenttitehtaan esiintymän luomista varten.

### <a name="action-classes"></a>Toimintoluokat

Toimintoluokat edustavat käyttäjätoimia, joten tässä esimerkissä käytetään **OK**-toimintoa sen esittämiseen, miten toimintoja luodaan.

```xpp
[ProcessGuideActionName(#ActionOK)]
public class ProcessGuideOKAction extends ProcessGuideAction
{
    public final str label()
    {
        return "@SYS5473";
     }
     protected final void doExecute()
     {
        step.executeOKAction();
      }
}
```    

Luokan on toteutettava kaksi abstraktimenetelmää:

-   **label()**, joka palauttaa tähän toimintoon liitetyssä painikeohjausobjektissa näytettävän otsikon.

-   **doExecute()**, joka suorittaa toiminnon. Kuten edellä mainittiin, **OK**-painike yksinkertaisesti suorittaa vastakutsun vaiheeseen. Muissa toiminnoissa voi kuitenkin olla tässä monimutkaisempaa logiikkaa.

Toimintojen esiintymät luodaan käyttäen **SysExtension**-kehystä **ProcessGuideActionName**-määritteen perusteella. Kuten sivunmuodostinten esiintymien luomisessa, vaiheluokka toteuttaa oletusarvoisen toimintotehtaan, ja tämä on mahdollista ohittaa. Sivunmuodostin lisää tällaisen painikeohjausobjektin.

```xpp
_page.addButton(step.createAction(#ActionOK), true);
```

Tässä yhteydessä se pyytää vaihetta luomaan toimintoluokan välitetylle nimelle ja liittää kyseisen toiminnon painikkeeseen.

### <a name="summary"></a>Yhteenveto

Seuraavassa vedetään yhteen kaikki tässä aiheessa selitetty kattavassa yhteenvedossa prosessia varten tarvittavasta koodista:

1.  **ProdProcessGuideProductionStartController**

    1.  Anna ensimmäisen vaiheen nimi ohittamalla **initialStepName()**.
    2.  Luo siirtymiskartta ohittamalla **initializeNavigationRoute()**.

        ```xpp
        /// <summary>
        /// The <c>ProdProcessGuideProductionStartController</c> class is the controller class for the production order start process guide.
        /// </summary>
        [WHSWorkExecuteMode(WHSWorkExecuteMode::StartProdOrder)]
        public class ProdProcessGuideProductionStartController extends ProcessGuideController
        {
            protected ProcessGuideStepName initialStepName()
            {
                return classStr(ProdProcessGuidePromptProductionIdStep);
            }

            protected ProcessGuideNavigationRoute initializeNavigationRoute()
            {
                ProcessGuideNavigationRoute navigationRoute = new ProcessGuideNavigationRoute();
                navigationRoute.addFollowingStep(classStr(ProdProcessGuidePromptProductionIdStep), classStr(ProdProcessGuideConfirmProductionOrderStep));
                navigationRoute.addFollowingStep(classStr(ProdProcessGuideConfirmProductionOrderStep), classStr(ProdProcessGuideStartProductionOrderStep));
                navigationRoute.addFollowingStep(classStr(ProdProcessGuideStartProductionOrderStep), classStr(ProdProcessGuidePromptProductionIdStep));

                return navigationRoute;
            }

        }
        ```

2.  **ProdProcessGuidePromptProductionIdStep**

    1.  Määritä vaiheen valmiiksi katsominen ohittamalla **isComplete()**.
    2.  Määritä käytettävä sivunmuodostin ohittamalla **pageBuilderName()**.

        ```xpp
        /// <summary>
        /// The <c>ProdProcessGuidePromptProductionIdStep</c> represents a step that 
        /// that prompts the user for a production order id.
        /// </summary>
        [ProcessGuideStepName(classStr(ProdProcessGuidePromptProductionIdStep))]
        public class ProdProcessGuidePromptProductionIdStep extends ProcessGuideStep
        {
            protected boolean isComplete()
            {
                WhsrfPassthrough pass = controller.parmSessionState().parmPass();
                ProdId prodId = pass.lookup(ProcessGuideDataTypeNames::ProdId);

                return (prodId != '');
            }

            protected ProcessGuidePageBuilderName pageBuilderName()
            {
                return classStr(ProdProcessGuidePromptProductionIdPageBuilder);
            }

        }
        ```

3.  **ProdProcessGuidePromptProductionIdPageBuilder**

    1.  Lisää **Tuotetunnus**-tekstiruutu ohittamalla **addDataControls()**.
    2.  Lisää **OK**- ja **Peruuta**-painikkeet ohittamalla **addActionControls()**.
        
        ```xpp
        /// <summary>
        /// The <c>ProdProcessGuidePromptProductionIdPageBuilder</c> class builds a page 
        /// that prompts the user for a production order id.
        /// </summary>
        [ProcessGuidePageBuilderName(classStr(ProdProcessGuidePromptProductionIdPageBuilder))]
        public class ProdProcessGuidePromptProductionIdPageBuilder extends ProcessGuidePageBuilder
        {
            protected void addDataControls(ProcessGuidePage _page)
            {
                _page.addTextBox(ProcessGuideDataTypeNames::ProdId, "@SYS4398", extendedTypeNum(ProdId));
            }

            protected void addActionControls(ProcessGuidePage _page)
            {
                #ProcessGuideActionNames
                _page.addButton(step.createAction(#ActionOK), true);
                _page.addButton(step.createAction(#ActionCancelExitProcess));
            }

        }
        ```

4.  **ProdProcessGuideConfirmProductionOrderStep**

    1.  Määritä käytettävä sivunmuodostin ohittamalla **pageBuilderName()**.
        
        ```xpp
        /// <summary>
        /// The <c>ProdProcessGuideConfirmProductionOrderStep</c> class represents the step for viewing production order
        /// details and confirming the same.
        /// </summary>
        [ProcessGuideStepName(classStr(ProdProcessGuideConfirmProductionOrderStep))]
        public class ProdProcessGuideConfirmProductionOrderStep extends ProcessGuideStep
        {    
            protected ProcessGuidePageBuilderName pageBuilderName()
            {
                return classStr(ProdProcessGuideConfirmProductionOrderPageBuilder);
            }

        }
        ```

3.  **ProdProcessGuideConfirmProductionOrderPageBuilder**

    1.  Lisää tilaus-, nimike- ja määrätietojen otsikot ohittamalla **addDataControls()**.

    2.  Lisää **OK**- ja **Peruuta**-painikkeet ohittamalla **addActionControls()**.
        
        ```xpp
        /// <summary>
        /// The <c>ProdProcessGuideConfirmProductionOrderPageBuilder</c> builds a page that allows the user to see details of a production order
        /// and then confirm.
        /// </summary>
        [ProcessGuidePageBuilderName(classStr(ProdProcessGuideConfirmProductionOrderPageBuilder))]
        public class ProdProcessGuideConfirmProductionOrderPageBuilder extends ProcessGuidePageBuilder
        {
            protected void addDataControls(ProcessGuidePage _page)
            {
                WhsrfPassthrough pass = controller.parmSessionState().parmPass();
                ProdTable prodTable = ProdTable::find(pass.lookup(ProcessGuideDataTypeNames::ProdId));
                UnitOfMeasureSymbol inventUOM = InventTableModule::find(prodTable.ItemId, ModuleInventPurchSales::Invent).UnitId;

                _page.addLabel(ProcessGuideDataTypeNames::ProdIdLabelName, strFmt("@WAX1684", prodTable.ProdId), extendedTypeNum(ProdId));
                _page.addLabel(ProcessGuideDataTypeNames::ItemInfo, this.generateItemInfoForProdId(pass.lookup(ProcessGuideDataTypeNames::ProdId)), extendedTypeNum(WHSRFUndefinedDataType));
                _page.addLabel(ProcessGuideDataTypeNames::QtyLabelName, strFmt("@WAX1685", WHSWorkExecuteDisplay::num2StrDisplay(ProdUpdStartUp::proposalStartUpQty(prodTable.ProdId)), inventUOM), extendedTypeNum(WHSRFQuantityAndUOM));

                if (PdsGlobal::pdsIsCWItem(prodTable.ItemId))
                {
                    _page.addLabel(ProcessGuideDataTypeNames::InventQtyLabelName, strFmt("@WAX1685", WHSWorkExecuteDisplay::num2StrDisplay(ProdUpdStartUp::pdsCWProposalStartupQty(prodTable.ProdId)), PdsCatchWeightItem::pdsCWUnitId(prodTable.ItemId)), extendedTypeNum(WHSRFQuantityAndUOM));
                }
            }

            protected void addActionControls(ProcessGuidePage _page)
            {
                #ProcessGuideActionNames
                _page.addButton(step.createAction(#ActionOK), true);
                _page.addButton(step.createAction(#ActionCancelResetProcess));
            }

        ```

        > [!NOTE]
        > **generateItemInfoForProdId()**-menetelmä, jota käytetään nimikkeen tieto-otsikkojen luomiseen on jätetty pois tästä aiheesta. Tässä menetelmässä lähetetään kyselyjä joillekin taulukoille nimikkeen tunnuksen, kuvauksen ja mittojen noutamista varten. Paremman kuvan **generateItemInfoForProdId()**-menetelmästä saat tarkastelemalla lähdekoodia.

4.  **ProdProcessGuideStartProductionOrderStep**

    1.  Suorita tuotannonkäynnistysprosessi ja lisää prosessin valmistumisen sanoma ohittamalla **doExecute()**.

        ```xpp
        /// <summary>
        /// The <c>ProdProcessGuideStartProductionOrderStep</c> represents a step that starts a production order.
        /// </summary>
        [ProcessGuideStepName(classStr(ProdProcessGuideStartProductionOrderStep))]
        public class ProdProcessGuideStartProductionOrderStep extends ProcessGuideStepWithoutPrompt
        {
            protected final void doExecute()
            {
                WhsrfPassthrough pass = controller.parmSessionState().parmPass();
                WHSUserId userId = pass.lookup(ProcessGuideDataTypeNames::UserId);
                ProdTable prodTable = ProdTable::find(pass.lookup(ProcessGuideDataTypeNames::ProdId));
                WhsWorkExecute workExecute = WhsWorkExecute::construct();
                workExecute.prodStartUp(prodTable.ProdId, ProdUpdStartUp::proposalStartUpQty(prodTable.ProdId), userId);

                this.addProcessCompletionMessage();

                super();
            }

        }
        ```

> [!NOTE]
> Huomaa, että kehykseen on siirretty monia yleisiä kaavoja (käyttöliittymän palautus virheen jälkeen, prosessin valmistumissanomien määritys, **OK**- ja **Peruuta**-toiminnot). Tällä tavoin sovelluksen kehittäjä säästyy vakiokoodin kirjottamiselta, siihen kun liittyy virhealttiutta ja epäjohdonmukaisen toiminnan vaara eri prosessien välillä. Kun skenaarion kuitenkin on poikettava yleiseltä polulta, sovelluksen kehittäjällä on mahdollisuus ohittaa soveltuvia menetelmiä. Silloin kyseessä on kuitenkin tarkoituksellinen poikkeama, joka on sekä eksplisiittinen että jäljitettävissä.


### <a name="extending-a-business-process"></a>Liiketoimintaprosessin laajentaminen

Tähän mennessä tässä aiheessa on esitetty, miten rakennetaan uusi prosessi **ProcessGuide**-kehystä käyttäen. Tässä viimeisessä osassa on esimerkkejä siitä, miten tätä liiketoimintaprosessia voi laajentaa.

### <a name="add-a-step-in-a-flow-using-processguidenavigationagentdefault"></a>Vaiheen lisääminen työnkulkuun (ProcessGuideNavigationAgentDefault)

Laajennuksen kohde:

-   Prosessin **ProcessGuideController**-luokan aliluokka.

Laajentaminen:

-   Laajenna **initializeNavigationRoute()**-menetelmää ohjainluokassa ja käynnistä **addFollowingStep()** **ProcessGuideNavigationRoute**-luokassa.

### <a name="add-a-step-in-a-flow-using-custom-navigation-agent"></a>Vaiheen lisääminen työnkulkuun (mukautetulla siirtymisagentilla)

Laajennuksen kohde:

-   Agentin **ProdProcessGuideNavigationAgentFactory/ProdProcessGuideNavigationAgent** aliagentti.

Laajentaminen:

-   Luo uusi **ProcessGuideNavigationAgent**-luokan aliluokka, joka palauttaa halutun vaihenimen.

-   Luo uusi **ProcessGuideNavigationAgentFactory**-luokasta johtuva luokka, joka palauttaa yllä luodun siirtymisagentin ehdollisesti.

-   Laajenna **navigationAgentFactory()**-menetelmää ohjainluokassa yllä luodun siirtymisagenttitehtaan palauttamista varten.

### <a name="add-a-new-control-in-the-ui-of-an-existing-step"></a>Uuden olemassa olevan vaiheen käyttöliittymän ohjausobjektin lisääminen 

Laajennuksen kohde:

-   Vaiheen **ProdProcessGuidePageBuilder**-sivunmuodostimen alisivunmuodostin.

Laajentaminen:

-   Laajenna **addDataControls()**-menetelmää ja lisää lisäohjausobjekti.

### <a name="complete-overhaul-of-the-user-interface-in-an-existing-step"></a>Olemassa olevan vaiheen käyttöliittymän täysi uusiminen

Laajennuksen kohde:

-   **ProdProcessGuideStep**-vaiheen alivaihe.

Laajentaminen:

-   Luo uusi **ProdProcessGuidePageBuilder**-luokan aliluokka ja toteuta haluttu käyttöliittymä.

-   Laajenna **pageBuildeName()**-menetelmä vaiheluokassa palauttaaksesi edellä luodun luokan **ProcessGuidePageBuilderNameAttribute**-määritteen.

### <a name="alter-logic-when-a-step-is-considered-complete"></a>Logiikan muuttaminen, kun vaihe on katsottu valmiiksi

Laajennuksen kohde:

-   **ProdProcessGuideStep**-vaiheen alivaihe.

Laajentaminen:

-   Laajenna **isComplete()**-menetelmää lisälogiikan rakentamista varten.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]