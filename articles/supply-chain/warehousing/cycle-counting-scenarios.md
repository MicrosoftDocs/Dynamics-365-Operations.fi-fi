---
title: Inventoinnin esimerkkiskenaariot
description: Tämä artikkeli sisältää kokoelman skenaarioita, jotka tutustuvat Microsoft Dynamics 365 Supply Chain Managementin inventointiominaisuuksiin.
author: GalynaFedorova
ms.date: 06/08/2021
ms.topic: article
ms.search.form: WHSCycleCountPlan, WHSCycleCountPlanListPage, WHSCycleCountThreshold, WHSWorkTableListPage, SalesShipmentDeviation, WHSRFMenuItemCycleCount, WHSWorkLineCycleCount
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2021-06-08
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 4f6f3f2db6efcc4d4d6ae3d278751a230fca9a64
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/29/2022
ms.locfileid: "9068593"
---
# <a name="cycle-counting-example-scenarios"></a>Inventoinnin esimerkkiskenaariot

[!include [banner](../includes/banner.md)]

Tämä artikkeli sisältää kokoelman skenaarioita, jotka tutustuvat Microsoft Dynamics 365 Supply Chain Managementin inventointiominaisuuksiin. Tässä kuvataan ensin aiemmin luodun Supply Chain Management -ympäristön vaatimukset. Sen jälkeen selitetään, miten inventointi konfiguroidaan ja miten kaikki inventoinnin vaiheet kuvataan. Kun olet lukenut ohjeen, sinulle on tuttu inventointi, myös ohjattu inventointi, sokkoinventointi, pisteinventointi, inventointirajat ja inventointisuunnitelmat.

## <a name="prerequisites"></a>Edellytykset

### <a name="make-demo-data-available"></a>Demotietojen ottaminen käyttöön

Tämän artikkelin kussakin skenaariossa viitataan arvoihin ja tietueisiin, jotka sisältyvät Supply Chain Management -sovelluksen vakiodemotietoihin. Jos haluat käyttää skenaarioiden työstämisessä näitä annettuja arvoja, varmista, että demotiedot on asennettu työskentely-ympäristöön ja että yritykseksi on valittu **USMF** ennen aloittamista.

### <a name="turn-on-support-for-the-warehouse-management-mobile-app"></a>Warehouse Management ‑mobiilisovelluksen tuen käyttöönotto

Warehouse Management -mobiilisovelluksen käyttöä varten järjestelmässäsi on oltava käytössä *Uuden varastosovelluksen käyttäjäasetukset, kuvakkeet ja vaiheotsikot* -toiminto. Supply Chain Managementin versiosta 10.0.25 alkaen tämä toiminto on pakollinen, eikä sitä voi poistaa käytöstä. Jos käytät vanhempaa versiota kuin 10.0.25, järjestelmänvalvojat voivat ottaa tämän toiminnon käyttöön tai pois käytöstä hakemalla *Uuden varastosovelluksen käyttäjäasetukset, kuvakkeet ja vaiheotsikot* -toimintoa [Toimintojen hallinta](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) -työtilassa.

### <a name="prepare-demo-data-for-the-scenarios"></a><a name= "prepare-demo-data"></a>Skenaarioiden esittelytietojen valmisteleminen

Noudattamalla näitä ohjeita voit vahvistaa, että kaikki skenaarioihin vaadittavat demotiedot ovat käytettävissä järjestelmässäsi USMF-yrityksessä. Luo kaikki puuttuvat tietueet tai arvot.

1. Valitse **Varastonhallinta \> Asetukset \> Työntekijä**.
1. Valitse luetteloruudusta **Julia Funderburk**
1. Valitse **Käyttäjät**-pikavälilehdestä rivi, jolla on seuraavat arvot. Jos näillä arvoilla ei ole olemassa olevaa riviä, luo se.

    - **Käyttäjätunnus:** *61*
    - **Käyttäjänimi:** *WH61*
    - **Oletusvarasto:** *61*
    - **Valikon nimi:** *Pää*

1. Määritä **Työ**-pikavälilehdessä käyttäjälle *61* seuraavat arvot, jos niitä ei ole vielä määritetty:

    - **On inventoinnin valvoja:** *Ei*
    - **Prosenttiosuuden enimmäisraja:** *0*
    - **Määrän enimmäisraja:** *0*
    - **Arvon enimmäisraja:** *0*

1. Valitse **Varastonhallinta \> Asetukset \> Työ \> Työpoolit**.
1. Työpooleja käytetään varastotyön erotteluun työn tyypin (tässä tapauksessa inventointityön) perusteella. Varmista, että tietue on olemassa, jolla on seuraavat asetukset:

    - **Työpoolin tunnus:** *CycleCount*
    - **Kuvaus:** *Inventointi*

1. Siirry kohtaan **Varastonhallinta \> Asetukset \> Mobiililaite \> Mobiililaitteen valikkovaihtoehdot**.
1. Valitse luetteloruudusta tietue, jonka nimi on *Inventointi*. Jos tällä nimellä ei ole aiemmin luotua tietuetta, luo se. Vahvista tai määritä tietueelle seuraavat arvot:

    - **Valikkokohteen nimi:** *Inventointi*
    - **Otsikko:** *Ohjattu inventointi*
    - **Tila:** *Työ*
    - **Käytä aiemmin luotua työtä:** *Kyllä*
    - **Ohjaus:** *Järjestelmän ohjaama* (Tämä arvo ilmaisee, että Supply Chain Management määrittää työntekijälle inventoinnin työtunnuksen.)
    - **Näytä varaston tila:** *Kyllä*

1. Valitse toimintoruudussa **Inventointi**.
1. Vahvista tai määritä seuraavat arvot **Kannettavan laitteen inventointi** -valintaikkunassa:

    - **Näytä nimiketunnus:** *Kyllä*
    - **Näytä rekisterikilpi:** *Kyllä*
    - **Yritysten määrä:** *1*

1. Sulje valintaikkuna valitsemalla **OK**.
1. Valitse luetteloruudusta tietue, jonka nimi on *Sokkoinventointi*. Jos tällä nimellä ei ole aiemmin luotua tietuetta, luo se. Vahvista tai määritä tietueelle seuraavat arvot:

    - **Valikkokohteen nimi:** *Sokkoinventointi*
    - **Otsikko:** *Sokkoinventointi*
    - **Tila:** *Työ*
    - **Käytä aiemmin luotua työtä:** *Kyllä*
    - **Ohjaaja:** *Inventoinnin ryhmittely* – (Tämä arvo ilmaisee, että työntekijä voi ryhmitellä inventointitöiden tunnukset, jotka liittyvät tiettyyn sijaintiin, vyöhykkeeseen tai työpooliin.)

1. Valitse toimintoruudussa **Inventointi**.
1. Vahvista tai määritä seuraavat arvot **Kannettavan laitteen inventointi** -valintaikkunassa:

    - **Näytä nimiketunnus:** *Ei*
    - **Näytä rekisterikilpi:** *Ei*
    - **Yritysten määrä:** *0*

1. Sulje valintaikkuna valitsemalla **OK**.
1. Valitse luetteloruudusta tietue, jonka nimi on *Pisteinventointi*. Jos tällä nimellä ei ole aiemmin luotua tietuetta, luo se. Vahvista tai määritä tietueelle seuraavat arvot:

    - **Valikkokohteen nimi:** *Pisteinventointi*
    - **Otsikko:** *Pisteinventointi*
    - **Tila:** *Työ*
    - **Käytä aiemmin luotua työtä:** *Ei*
    - **Työn luontiprosessi:** *Pisteinventointi* – (Tämä arvo ilmaisee, että työntekijä voi laskea varastosijainnin nimikkeet milloin tahansa inventointityötä luomatta. Työntekijä suorittaa pistoinvestoinnin sijainnissa syöttämällä sijainnin tunnuksen.)

1. Siirry kohtaan **Varastonhallinta \> Asetukset \> Mobiililaite \> Mobiililaitteen valikko**.
1. Valitse luetteloruudusta tietue, jonka nimi on *Varasto*. Jos tällä nimellä ei ole aiemmin luotua tietuetta, luo se. Vahvista, että **Valikkorakenne**-sarakkeessa näkyvät seuraavat inventointivalikon vaihtoehdot:

    - Inventointi
    - Sokkoinventointi
    - Pisteinventointi

1. Siirry kohtaan **Varastonhallinta \> Asetukset \> Varastonhallinnan parametrit**.
1. Määritä **Inventointi**-välilehdessä seuraavat arvot:

    - **Inventoinnin oletusoikaisutyyppi:** *Inventointi* (Tämä kenttä määrittää kirjauskansion tyypin, joka kirjataan inventoinnin yhteydessä.)
    - **Inventoinnin oletustyöluokan tunnus:** *CCount* (Tämä kenttä määrittää työluokan, jota käytetään inventointiin.)
    - **Inventoinnin töiden oletusjärjestys:** *50* (Tässä kentässä määritetään prioriteetti, joka inventointityöllä on suhteessa muihin varaston työlajeihin. Kun syötät luvun, joka on alhaisempi kuin muiden työtyyppien luku, inventointityön prioriteetti nousee.)

1. Valitse **Varastonhallinta \> Määritys \> Varasto \> Oikaisutyypit**.
1. **Oikaisutyypit**-sivulla voit luoda koodeja erilaisia mahdollisia oikaisuja varten. Vahvista, että tietue on olemassa, jolla on seuraavat asetukset:

    - **Varaston oikaisutyyppi:** *Inventointi*
    - **Kuvaus:** *Inventointi*
    - **Nimi:** *ICnt*

1. Valitse **Varastonhallinta \> Asetukset \> Varaston asetukset \> Varastot**.
1. Valitse luetteloruudusta varasto *61*. Jos tällä nimellä ei ole aiemmin luotua tietuetta, luo se.
1. Määritä **Varasto**-pikavälilehdessä seuraavat arvot:

    - **Käytä varastonhallintaprosessia:** *Kyllä* (Tämä arvo mahdollistaa fyysisen varaston varastonhallintaprosessit (WMS).)
    - **Salli rekisterikilven siirrot inventoinnin aikana:** *Kyllä* (Tämän arvon avulla työntekijät voivat siirtää rekisterikilpiä inventoinnin aikana.)

## <a name="scenario-1-guided-cycle-counting"></a>Skenaario 1: Ohjattu inventointi

Ennen kuin ohjattu inventointi voi tapahtua, sinun on luotava joitakin töitä. Tämä työ ohjaa määritetyn henkilön varaston läpi sijainnista sijaintiin ja suorittaa työssä määritetyt inventointiin liittyvät laskut.

### <a name="create-cycle-counting-work-for-scenario-1"></a>Inventointityön luominen skenaariolle 1

Luo varastossa *61* nimikkeen sijainnille *01A02R2S2B* (BULK-06) inventointityö näiden ohjeiden mukaisesti.

1. Valitse **Varastonhallinta \> Inventointi \> Inventointityöt sijainnin mukaan**
1. Määritä **Luo inventointityö sijainnin mukaan** -valintaikkunassa **Työpoolin tunnus** -kentän arvoksi *CycleCount*.
1. Valitse **Sisällytettävät tietueet** -pikavälilehdessä **Suodatus**.
1. Toimi kyselyeditorin valintaikkunassa **Alue**-välilehdessä seuraavasti:

    - Määritä **Ehto**-kentän arvoksi *61* sen rivin osalta, jolla **Kenttä**-kentän arvoksi on määritetty *Varasto*.
    - Määritä **Ehto**-kentän arvoksi *01A02R2S2B* sen rivin osalta, jolla **Kenttä**-kentän arvoksi on määritetty *Sijainti*.

1. Sulje kyselyeditorin valintaikkuna valitsemalla **OK**.
1. Sulje **Luo inventointityö sijainnin mukaan** -valintaikkuna valitsemalla **OK**.

    Kun työn luontiprosessi on valmis, toimintokeskuksessa näkyy sanoma.

1. Valitse **Varastonhallinta \> Työ \> Työn tiedot**.
1. Etsi juuri luotu työ määrittämällä suodatin **Työpoolin tunnus** -sarakkeeseen, jotta voit etsiä tietueita, joissa on *CycleCount*-arvo.

### <a name="do-cycle-counting-work-for-scenario-1"></a>Inventointityön tekeminen skenaariolle 1

Kun inventointityö on luotu, voit suorittaa sen laskemalla varastosijainnin nimikkeet ja kirjaamalla tulokset Supply Chain Managementiin mobiililaitteella. Noudata näitä ohjeita, kun haluat tehdä inventoinnin Warehouse Management -mobiilisovelluksessa.

1. Kirjaudu sisään Warehouse Management -mobiilisovellukseen aiemmin tässä artikkelissa kohdassa [Skenaarioiden esittelytietojen valmistelu](#prepare-demo-data) määritettynä työkäyttäjänä. Tässä artikkelissa esimerkissä nimenä on *Julia Funderburk*, ja on määritetty varasto *61*. (USMF-demotietojen avulla voit kirjautua sisään tänä työkäyttäjänä antamalla tunnukseksi *61* ja salasanaksi *1*.)
1. Valitse päävalikossa **Varasto**.
1. Valitse **Varasto**-valikosta **Ohjattu inventointi**.
1. Valitse **Määrä**-kenttä, anna arvoksi *9* numeronäppäimistöllä ja valitse sitten **OK** (valintamerkkipainike).
1. Järjestelmä odotti, että syötät tälle nimikkeelle, sijainnille ja rekisterikilvelle 10 kappaletta. Siksi sinua pyydetään laskemaan uudelleen. Valitse **Määrä**-kenttä, anna arvoksi jälleen *9* numeronäppäimistöllä ja valitse sitten **OK** (valintamerkkipainike). Toinen yritys hyväksyy inventointisi.

    > [!NOTE]
    > Kun järjestelmä on havainnut odotetun varastomäärän ja syötetyn määrän välisen eron, se pyysi laskemaan toisen kerran, koska mobiililaitteen **Ohjattu inventointi**-valikkokohteen **Yritysten määrä** -arvoksi on asetettu *1*. Sinut ohjattiin tiettyyn nimiketunnukseen ja rekisterinumeroon, koska sekä **Näytä nimiketunnus** -vaihtoehto että **Näytä rekisterikilpi** -vaihtoehdoksi on määritetty *Kyllä* mobiililaitteen valikkokohteeksi.

1. Valitse **OK** (valintamerkkipainike).

### <a name="review-the-cycle-counting-differences-for-scenario-1"></a>Tarkista skenaarion 1 inventointierot

Tarkista inventointierot noudattamalla näitä ohjeita.

1. Palaa Supply Chain Managementiin.
1. Valitse **Varastonhallinta \> Työ \> Työn tiedot**.
1. Etsi ja valitse inventointityö, jota olet tarkastellut aiemmin. (Voit esimerkiksi asettaa suodattimen **Työpoolin tunnus** -sarakkeeseen löytääksesi *CycleCount*-arvolla toimivat tietueet.) Huomaa, että tämän työn **Työn tila** -kentän arvoksi on nyt määritetty *Odottaa tarkistusta*.

    > [!NOTE]
    > Inventoinnin aikana käytetyn työkäyttäjätilin **Inventoinnin valvoja** -asetuksena on *Ei* ja **Enimmäisprosenttiraja**-, **Enimmäismääräraja**- ja **Enimmäisarvoraja**-kenttien arvoksi määritetään *0* (nolla). Siksi kaikki inventointierot, jotka käyttäjä ilmoittaa, on hyväksyttävä manuaalisesti ja liittyvän työn **Työn tila** -arvoksi määritetään *Odottaa tarkistusta*. Jos laskettu arvo olisi poikkeamarajojen sisällä (määritetty **Työkäyttäjät**-sivun **Enimmäisprosenttiraja**- tai **Enimmäismääräraja**-kentässä) tai jos käyttäjän **Inventoinnin valvoja** -asetuksena on *Kyllä*, työ olisi suljettu automaattisesti.

1. Valitse toimintoruudun **Työ**-välilehdessä **Inventointi**.
1. Valitse toimintoruudussa **Hyväksy määrä**.

    Ero kirjataan vakioinventointikirjauskansion avulla, ja uusi työtilaus luodaan.

1. Etsi hyväksytylle erolle luotu työ valitsemalla **Inventointitapahtumat** -sivun toimintoruudusta **Johdettu työ**.

## <a name="scenario-2-blind-cycle-counting"></a>Skenaario 2: Sokkoinventointi

Tämä skenaario edellyttää, että skenaario 1 on jo valmis järjestelmässäsi.

### <a name="create-cycle-counting-work-for-scenario-2"></a>Inventointityön luominen skenaariolle 2

Ennen kuin sokkoinventointi voi tapahtua, sinun on luotava joitakin töitä. Luo varastossa *61* nimikkeen sijainnille *01A02R2S2B* (BULK-06) inventointityö näiden ohjeiden mukaisesti.

1. Valitse **Varastonhallinta \> Inventointi \> Inventointityöt nimikkeen mukaan**
1. Määritä **Luo inventointityö nimikkeen mukaan** -valintaikkunassa **Työpoolin tunnus** -kentän arvoksi *CycleCount*.
1. Valitse **Sisällytettävät tietueet** -pikavälilehdessä **Suodatus**.
1. Lisää sitten kyselyeditorin valintaikkunan **Alue**-välilehdessä kolme riviä, joissa on seuraavat asetukset:

    - Rivi 1:

        - **Taulukko:** *Nimikkeet*
        - **Kenttä:** *Nimiketunnus*
        - **Kriteerit:** *L0101*

    - Rivi 2:

        - **Taulukko:** *Varastodimensiot*
        - **Kenttä:** *Varasto*
        - **Ehdot:** *61*

    - Rivi 3:

        - **Taulukko:** *Varastodimensiot*
        - **Kenttä:** *Sijainti*
        - **Kriteerit:** *01A02R2S2B*

1. Sulje kyselyeditorin valintaikkuna valitsemalla **OK**.
1. Sulje **Luo inventointityö nimikkeen mukaan** -valintaikkuna valitsemalla **OK**.

    Kun työn luonti on valmis, näyttöön tulee tietosanoma.

### <a name="do-cycle-counting-work-for-scenario-2"></a>Inventointityön tekeminen skenaariolle 2

Noudata näitä ohjeita, kun haluat tehdä inventointityön luomisen jälkeen työn Warehouse Management -mobiilisovelluksessa.

1. Kirjaudu sisään Warehouse Management -mobiilisovellukseen aiemmin tässä artikkelissa kohdassa [Skenaarioiden esittelytietojen valmistelu](#prepare-demo-data) määritettynä työkäyttäjänä. Tässä artikkelissa esimerkissä nimenä on *Julia Funderburk*, ja on määritetty varasto *61*. (USMF-demotietojen avulla voit kirjautua sisään tänä työkäyttäjänä antamalla tunnukseksi *61* ja salasanaksi *1*.)
1. Valitse päävalikossa **Varasto**.
1. Valitse **Varasto**-valikosta **Sokkoinventointi**.
1. Valitse **Vyöhyketunnus** -kenttä, kirjoita *BULK06* ja valitse sitten **OK** (valintamerkkipainike).
1. Valitse **Nimike** -kenttä, kirjoita *L0101* ja valitse sitten **OK** (valintamerkkipainike).
1. Valitse **Rekisterikilpi** -kenttä, kirjoita *LP\_BULK\_06\_01* ja valitse sitten **OK** (valintamerkkipainike).
1. Valitse **Määrä** -kenttä, kirjoita *10* ja valitse sitten **OK** (valintamerkkipainike).

    > [!NOTE]
    > Vaikka järjestelmä on havainnut odotetun varastomäärän ja skannatun määrän välisen eron, se ei pyytänyt laskemaan toista kertaa, koska mobiililaitteen **Sokkoinventointi**-valikkokohteen **Yritysten määrä** -arvoksi on asetettu *0* (nolla). Sinua pyydettiin skannaamaan nimiketunnus ja rekisterikilpi, koska sekä **Näytä nimiketunnus** -vaihtoehto että **Näytä rekisterikilpi** -vaihtoehdoksi on määritetty *Ei* mobiililaitteen valikkokohteeksi.

1. Valitse **OK** (valintamerkkipainike).

### <a name="review-the-cycle-counting-differences-for-scenario-2"></a>Tarkista skenaarion 2 inventointierot

Tarkista inventointierot noudattamalla näitä ohjeita.

1. Palaa Supply Chain Managementiin.
1. Valitse **Varastonhallinta \> Yhteiset \> Työ \> Tarkistusta odottava inventointityö**.
1. Valitse toimintoruudun **Työ**-välilehdessä **Inventointi**.
1. Valitse toimintoruudussa **Hylkää määrä**.

    Koska inventointiero hylättiin, työ suljetaan.

## <a name="scenario-3-spot-cycle-counting"></a>Skenaario 3: Pisteinventointi

Käytettävissä olevan varaston tietue ilmaisee, että nimikkeellä *L0101* on käytettävissä oleva varastomäärä sijainnissa *01A02R2S2B*. Varastotyöntekijä on paikassa *01A02R2S1B*. Vaikka tämän sijainnin pitäisi olla tyhjä, se on täynnä. Siksi varastotyöntekijä tekee heti tämän sijainnin pisteinventoinnin.

### <a name="do-cycle-counting-work-for-scenario-3"></a>Inventointityön tekeminen skenaariolle 3

Noudata näitä ohjeita, kun haluat tehdä inventoinnin Warehouse Management -mobiilisovelluksessa.

1. Kirjaudu sisään Warehouse Management -mobiilisovellukseen aiemmin tässä artikkelissa kohdassa [Skenaarioiden esittelytietojen valmistelu](#prepare-demo-data) määritettynä työkäyttäjänä. Tässä artikkelissa esimerkissä nimenä on *Julia Funderburk*, ja on määritetty varasto *61*. (USMF-demotietojen avulla voit kirjautua sisään tänä työkäyttäjänä antamalla tunnukseksi *61* ja salasanaksi *1*.)
1. Valitse päävalikossa **Varasto**.
1. Valitse **Varasto**-valikosta **Pisteinventointi**.
1. Valitse **Sijainti**-kenttä, kirjoita *01A02R2S1B* ja valitse sitten **OK** (valintamerkkipainike).

    Järjestelmä havaitsee, että sijainti on tyhjä Supply Chain Managementissa.

1. Valitse **Lisää LP tai nimike**.
1. Valitse **Nimike** -kenttä, kirjoita *L0101* ja valitse sitten **OK** (valintamerkkipainike).
1. Valitse **Rekisterikilpi** -kenttä, kirjoita *LP\_BULK\_06\_01* ja valitse sitten **OK** (valintamerkkipainike).
1. Valitse **Määrä** -kenttä, kirjoita *9* ja valitse sitten **OK** (valintamerkkipainike).

    Koska järjestelmä havaitsee, että määritetty rekisterikilpi on jo saatavilla toisessa Supply Chain Managementin sijainnissa, tämä rekisterikilpi siirretään nykyiseen sijaintiin. Siksi järjestelmä pyytää vahvistamaan siirron.

1. Valitse **OK** (valintamerkkipainike).

### <a name="review-the-cycle-counting-differences-for-scenario-3"></a>Tarkista skenaarion 3 inventointierot

Tarkista laskennan tulokset noudattamalla näitä ohjeita.

1. Palaa Supply Chain Managementiin.
1. Valitse **Varastonhallinta \> Yhteiset \> Työn tiedot**.
1. Valitse ruudukon yläosassa **Näytä suljetut** -valintaruutu.
1. Määritä **Työtilaustyyppi**-sarakkeen suodattimeksi *Varastosiirto*.

    Järjestelmä on tunnistanut tämän laskennan automaattisesti varastosiirroksi. Tämä siirto on sallittu, koska **Salli rekisterikilven siirrot inventoinnin aikana** -asetukseksi on määritetty **Varastot**-sivulla *Kyllä* varastolle *61*.

## <a name="scenario-4-define-cycle-count-thresholds"></a>Skenaario 4: Inventointikynnysten määrittäminen

Yksi tapa luoda inventointityö on raja-arvojen käyttö. Inventointikynnys osoittaa varastonimikkeiden määrä- tai suhderajan. Inventointityö luodaan automaattisesti, kun raja-arvo on saavutettu.

Esimerkiksi sijainnissa, jonka inventoinnin raja-arvo on 40, on 60 nimikettä. Myyntitilaustapahtuman aikana poimitaan 25 nimikettä kyseisestä sijainnista ja sijoitetaan väliaikaiseen paikkaan. Uusi nimikkeiden määrä 35 on pienempi kuin raja-arvo, joten inventointityö luodaan sijainnille automaattisesti.

Voit määrittää inventoinnin raja-arvot seuraavasti.

1. Valitse **Varastonhallinta \> Asetukset \> Inventointi \> Inventointirajat**.
1. Luo raja valitsemalla toimintoruudussa **Uusi** ja määritä sille seuraavat arvot:

    - **Inventointirajan tunnus:** *L0101*
    - **Kuvaus:** *Raja L0101*
    - **Rajan määrä:** *2*
    - **Yksikkö:** *ea*
    - **Prosenttiosuuteen perustuva kapasiteettiraja:** *0,00*
    - **Inventointirajan tyyppi:** *Määrä*
    - **Käsittele inventointi heti:** *Kyllä*
    - **Inventointien välissä olevat päivät:** *1*
    - **Työpoolin tunnus:** *CycleCount*

1. Valitse toimintoruudussa **Valitse nimikkeitä**.
1. Etsi kyselyeditorin valintaikkunan **Alue**-välilehdessä rivi, jonka **Kenttä**-kentän asetuksena on *Nimiketunnus*. Määritä kyseisen rivin **Ehdot**-kentän arvoksi *L0101*.
1. Sulje kyselyeditorin valintaikkuna valitsemalla **OK**.

    Nimikkeen *L0101* inventointiraja on nyt määritetty.

Inventointi luodaan nyt nimikkeelle *L0101* missä tahansa kohdassa, jos käytettävissä oleva määrä on alle 2 ja jos sijainnin edellisen inventoinnin päivämäärä ei ole kuluva päivä.

## <a name="scenario-5-define-cycle-count-plans"></a>Skenaario 5: Inventointisuunnitelmien määrittäminen

Inventointisuunnitelmien avulla voit automatisoida inventointiin liittyvät inventointityöt. Voit määrittää kullekin inventointisuunnitelmalle tietyt nimike- ja sijaintikyselyt. Kun erätyö suoritetaan, se luo inventointityön kaikille sijainnille, jotka vastaavat nimike- ja sijaintiehtoja (suunnitelmaa varten määritettyyn inventointien enimmäismäärään asti). Kun inventointityö luodaan, sen rivi sisältää tiedot siitä, mikä sijainti pitää inventoida. Sijaintiin liittyvä käytettävissä oleva varasto ei ole estetty. Siksi se on käytettävissä varaukseen ja lähtevien käsittelyyn, vaikka avoin inventointityö on olemassa.

Voit määrittää inventointisuunnitelman seuraavasti.

1. Valitse **Varastonhallinta \> Asetukset \> Inventointi \> Inventointisuunnitelmat**.
1. Lisää rivi ruudukkoon valitsemalla toimintoruudussa **Uusi** ja määritä sitten sille seuraavat arvot:

    - **Inventointisuunnitelman tunnus:** *BULK06*
    - **Kuvaus:** *Laskenta sijainnille BULK06*
    - **Työpoolin tunnus:** *CycleCount*
    - **Inventointien enimmäismäärä:** *10*
    - **Inventointien välissä olevat päivät:** *10*
    - **Tyhjät sijainnit:** *Jätä tyhjät pois*
    - **Työmalli:** Jätä tämä kenttä tyhjäksi.

1. Valitse toimintoruudussa **Valitse sijainnit**.
1. Näyttöön tulee vakiokyselyeditorin valintaikkuna. Valitse **Alue**-välilehdessä rivi, ja määritä sille seuraavat arvot:

    - **Taulu:** *Sijainnit*
    - **Kenttä:** *Alueen tunnus*
    - **Kriteerit:** *BULK06*

1. Sulje kyselyeditorin valintaikkuna valitsemalla **OK**.
1. Valitse toimintoruudussa **Käsittele inventointisuunnitelma**.
1. Määritä **Inventointisuunnitelmat**-valintaruudussa **Suorita taustalla** -pikavälilehdessä **Eräkäsittely**-asetuksen arvoksi *Kyllä*
1. Valitse **Toistuminen**.
1. Määritä **Määritä toistuminen** -valintaikkunassa erätyö niin, että se alkaa heti ja suoritetaan kerran minuutissa, jolloin päättymispäivää ei ole.
1. Valitse **OK**, jotta voit sulkea **Määritä toistuminen** -valintaikkunan.
1. Valitse **OK**, jotta voit sulkea **Inventointisuunnitelmat** -valintaikkunan.

    Sanoma kertoo, että työ on lisätty eräjonoon.

1. Valitse **Varastonhallinta \> Yhteiset \> Inventoinnin ajoitus**. Suunnitelma alkaa heti, ja se luo inventointityötä. Koska inventointityötä ei ole tehty valmiiksi, **Tila**-kentän arvoksi tulee *Käynnissä*. Yhden minuutin kuluttua **Inventointeja yhteensä** -sarakkeen arvoksi muuttuu *1*.

    > [!NOTE]
    > Inventointityötä ei luoda, jos päivien määrä edellisestä inventoinnista on pienempi kuin inventointisuunnitelman **Inventointien välissä olevat päivät** -arvo. Jos esimerkiksi jos **Inventointien välissä olevat päivät** -kentän arvoksi määritetään *5*, inventointityö luodaan viiden päivän välein. Jos inventointityö kuitenkin käsitellään kolmantena päivänä, seuraava inventointityö luodaan viiden päivän jälkeen edellisen inventoinnin käsittelystä, 8. päiväksi.

1. Valitsemalla toimintoruudussa **Työ** voit tarkastella luotua inventointityötä.
