---
title: Tuotemääritys – yleiskatsaus
description: Tarve määrittää tuotteita vastaamaan erityisvaatimuksiin on muuttumassa säännöksi poikkeuksen sijaan sekä yritys- että kuluttajasuhteissa.
author: cvocph
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PCProductConfigurationModelDetails, ConfigPartOf
audience: Application User
ms.reviewer: kamaybac
ms.custom: 75083
ms.assetid: f08072b8-cb0b-43aa-9509-f5ec32caecd9
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4ba1fcdffec27e848afaf4b821df85240139f41f
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5812808"
---
# <a name="product-configuration-overview"></a>Tuotemääritys – yleiskatsaus

[!include [banner](../includes/banner.md)]

Tarve määrittää tuotteita vastaamaan erityisvaatimuksiin on muuttumassa säännöksi poikkeuksen sijaan sekä yritys- että kuluttajasuhteissa.

Määritä-tilaukseen-skenaariota tukevalla valmistajalla on mahdollisuus huolehtia paremmin asiakkaan tarpeista. Valmistaja voi lisäksi pienentää varastoon sitoutunutta pääomaansa varastoimalla puolivalmiita tuotteita yleisten osien muodossa valmiiden tuotteiden sijaan.  

Onnistunut siirtyminen valmistus-varastoon-tilanteesta määritä-tilaukseen-tilanteeseen vaatii huolellista tuoterakenteiden analyysiä, tuoteperheiden tunnistamista ja komponenttien määrittämistä. Prosessissa olevien osien ja tuotteiden lukumäärän vähentämiseksi on erittäin tärkeää, että ymmärrät tuotteiden liittymät ja että suunnittelet uudelleen käytettävissä olevia tuotteita.  

On olemassa useita tuotekonfiguraation mallinnusperiaatteita, kuten sääntöihin perustuva, dimensioihin perustuva, ja poissulkeva mallinnus. Tutkimukset osoittavat, että poissulkeva menetelmä voi vähentää mallien koodirivien lukumäärää noin 50 prosentilla verrattuna muihin mallinnusperiaatteisiin. Tällä menetelmällä voidaan siis pienentää omistuksen kokonaiskustannusta (TCO). Kun siirryt sääntöpohjaisesta, X++-koodiin perustuvasta mallista poissulkevaan malliin, et enää tarvitse suunnittelijan lisenssiä tuotemallien ylläpitoon.

## <a name="product-configuration"></a>Tuotekonfiguraatio
Teollistumisprosessi on johtanut merkittäviin saavutuksiin korkealaatuisten ja ominaisuuksiltaan runsaiden tuotteiden valmistamisessa kohtuulliseen hintaan. Mittakaavaedut ovat tehneet useimmille teollistuneissa maissa asuville ihmisille mahdolliseksi ostaa autoja, televisioita, kodinkoneita ja muita tuotteita, joita useimmat meistä pitävät arjessamme välttämättöminä.  

Koska monista tuotteista on tullut hyödykkeitä, on syntynyt tarve erilaistaa niitä. Valmistajien välitön vastaus tähän haasteeseen on ollut luoda variantteja kustakin tuotteesta niin, että asiakkailla on enemmän vaihtoehtoja. Tämä strategia on johtanut ennusteiden laatimisen vaikeutumiseen, kasvaneisiin varastointikustannuksiin sekä myymättömien, vanhentuneiden tuotteiden kasvaneeseen määrään.  

Omaksumalla määritä-tilaukseen-filosofian valmistajilla on mahdollisuus vastata asiakaskysyntään yksilöidyillä tuotteilla ja samalla vähentää tai eliminoida vanhentuneiden varastonimikkeiden määrän. Siirryttäessä valmistus-varastoon-filosofiasta määritä-tilaukseen-filosofiaan, yksi välittömästi esiin nouseva haaste on tarve tasapainottaa lyhyet läpimenoajat alhaisten varastotasojen kanssa.  

Avain menestykseen on analysoida huolellisesti tuotevalikoima ja etsiä malleja sekä tuoteominaisuuksissa että prosesseissa. Tavoite on tunnistaa yleiset osat, jotka voidaan valmistaa samoilla laitteilla ja käyttää kaikissa varianteissa.  

Uusi Tuotemääritys-ominaisuusjoukko sisältää käyttöliittymän (UI), joka tarjoaa visuaalisen yleiskatsauksen tuotemääritysmallin rakenteesta sekä määrittelevän rajoitussyntaksin, jota ei tarvitse kääntää. Siksi yritykset, jotka haluavat tukea määrityskäytäntöä, pääsevät helpommin aloittamaan. Kuten seuraavissa kohdissa kerrotaan, tuotteen suunnittelija ei enää tarvitse kehittäjän tukea tuotemääritysmallin rakentamiseen, testaukseen, tai sen myyntiorganisaatiolle julkaisemiseen.

## <a name="building-a-product-configuration-model"></a>Tuotemääritysmallin rakentaminen
Käyttäjällä on valittavanaan useita lähestymistapoja tuotemääritysmallin rakentamiseen. Yksi vaihtoehto on seurata määritettyä järjestystä luomalla ensin viitetiedot kuten päätuotteet, erilliset tuotteet ja toiminnalliset resurssit, ja sisällyttää ne sitten komponentteina, tuoterakenteen (BOM) riveinä, reititystoimintoina ja muina tuotemääritysmallin elementteinä. Vaihtoehtoisesti voit valita iteroivamman tavan luomalla ensin mallin ja lisäämällä sitten viitetiedot tarpeen mukaan.

### <a name="components"></a>Komponentit

Tuotemääritysmalli koostuu yhdestä tai useammasta toisiinsa alikomponenttisuhteiden kautta sidotusta komponentista. Komponentit määritetään yksi kerrallaan, ja niitä voidaan sitten käyttää useita kertoja yhdessä tai useammassa tuotemääritysmallissa. Komponentit ovat tuotemääritysmallin tärkeimmät rakennusosat, ja melkein kaikki mallia koskevat tiedot liittyvät niihin.

### <a name="attributes"></a>Määritteet

Kullakin komponentilla on yksi tai useampia määritteitä, joiden mukaan sen ominaisuudet tunnistetaan. Käyttäjät valitsevat nämä määritteet määritysprosessin aikana. Määritteet ohjaavat sekä komponenttien välisiä että komponenttien sisäisiä suhteita niiden rajoitteisiin tai laskelmiin sisällyttämisen kautta. Tuoterakenteen riveillä käyttöön otettujen ehtojen kautta määritteitä voidaan käyttää määrittämään fyysiset osat, joista konfiguroitu tuote tulee koostumaan. Määrite voi lisäksi ohjata tuoterakenteen rivin ominaisuutta yhdistämismekanismin kautta. Samanlainen toiminne on olemassa reititykselle koskien sekä sisällyttämistä että ominaisuuksien määrittämistä.

>[!NOTE]
> Vältä määritetyyppejä luotaessa suurinumeroisia määritetyypin toimialueen arvoja. Se voi nimittäin hidastaa tuotekonfigurointia. 

### <a name="expression-constraints"></a>Lausekerajoitukset

Poissulkevan tuotemääritysmallin käyttö viittaa siihen, että on olemassa rajoituksia, kun käyttäjä valitsee arvoja eri määritteille. Näitä rajoitteita voidaan toteuttaa lausekerajoituksina käyttämällä Optimization Modeling Language (OML) -kieltä. Vaihtoehtoisesti rajoitteet voidaan toteuttaa taulurajoituksen muodossa.

### <a name="table-constraints"></a>Taulurajoitukset

Taulukon rajoitukset voivat olla joko käyttäjän tai järjestelmän määrittämiä.  

Käyttäjän määrittämän taulurajoituksen rakentaa käyttäjä. Käyttäjä valitsee määritetyyppien yhdistelmän kuvaamaan taulukon sarakkeita ja syöttää sitten arvot valittujen määritetyyppien toimialueilta muodostamaan taulurajoituksen rivit.  

Järjestelmän määrittämä taulurajoitus määritetään valitsemalla viitteenä käytettävä taulu ja valitsemalla sitten tästä taulusta kentät, jotka muodostavat rajoituksen sarakkeet. Taulurajoituksen rivit ovat Supply Chain Management -taulukossa määrityshetkellä olevat rivit.  

Taulurajoitus sisällytetään tuotemääritysmalliin viittaamalla taulurajoituksen määritykseen ja yhdistämällä mallin asiaankuuluvat määritteet taulurajoituksen sarakkeisiin.

### <a name="calculations"></a>Laskelmat

Laskelmat edustavat mekanismia, jolla suoritetaan laskutoimenpiteitä määritysmallissa. Laskelma voi esimerkiksi määrittää tietyn raaka-aineen pituuden tai kiillotustoiminnon käsittelyajan. Laskelmat ovat käskymuotoisia ja niillä asetetaan kohdemääritteen arvo sen jälkeen, kun kaikki laskentalausekkeeseen sisältyvät määritearvot ovat tulleet saataville.

### <a name="subcomponents"></a>Alikomponentit

Alikomponentit kuvaavat tuotemääritysrakenteen solmuja. Jokaiselle alikomponentin suhteelle on määritettävä viite päätuotteeseen, jolla on poissulkevalle konfiguraatiolle asetettu variantin määritysmenetelmä.

### <a name="user-requirements"></a>Käyttäjän vaatimukset

Käyttäjän vaatimuksella on kaikki alikomponentin rakenneosat. Ainoana erona on, että käyttäjän vaatimusta ei ole sidottu päätuotteeseen. Tämän eron käytännön vaikutus on, että kaikki tuoterakenteen rivit tai reititykset, jotka on määritetty käyttäjän vaatimuksen kontekstissa, tiivistetään pääkomponentin tuoterakenteen tai reitityksen rakenteeseen. Tämä toiminta muistuttaa haamutuoterakenteen toimintaa.

### <a name="bom-lines"></a>Tuoterakenteen rivit

Tuoterakenteen rivit on sisällytetty kunkin komponentin valmistuksen tuoterakenteen tunnistamiseen. Tuoterakennerivin on viitattava nimikkeeseen ja kaikki nimikkeen ominaisuudet voidaan asettaa kiinteäksi arvoksi tai yhdistää määritteeseen.

### <a name="route-operations"></a>Reitityksen työvaihe

Reititys on sisällytetty valmistusreitin tunnistamista varten. Reitityksen on viitattava määritettyyn toimintoon, ja kaikki toiminnon ominaisuudet voidaan asettaa kiinteäksi arvoksi. Kaikki ominaisuudet lukuun ottamatta resurssivaatimuksia voidaan yhdistää määritteeseen arvon sijaan.

## <a name="validating-and-testing-a-product-configuration-model"></a>Tuotemääritysmallin tarkistaminen ja testaaminen
Tuotemääritysmallin tarkistaminen voidaan suorittaa useilla mallin tasoilla ja se voi siten kattaa erilaisia alueita. Alhaisin taso on yksittäistä lausekerajoitusta koskeva. Tässä tapauksessa tarkistuksen suorittaa yleensä tuotteen suunnittelija varmistaakseen, että lausekkeen syntaksi on oikea.  

Tuoterakennerivin tai reitityksen ehto voidaan myös tarkistaa erikseen.  

Tarkistus voidaan lisäksi suorittaa käyttäjän määrittämälle taulurajoituksen määritykselle. Tässä tapauksessa käyttäjä voi tarkistaa, että jokaiselle kentälle syötetyt arvot ovat vastaavien määritetyyppien toimialueen sisällä.  

Viimeisenä, tarkistus voidaan suorittaa koko tuotemääritysmallille tarkistamaan, että koko syntaksi on oikein ja että kaikkia nimeämis- ja mallinnuskäytäntöjä on noudatettu.

### <a name="testing"></a>Testaus

Mallin testaus on samanlaista kuin todellinen konfigurointi-istunnon suoritus. Käyttäjä voi käydä läpi kokoonpanosivut ja varmistaa, että mallin rakenne tukee määritysprosessia. Käyttäjä voi tarkistaa, että määritearvot ovat oikeat ja että määritteiden kuvaukset ohjaavat käyttäjää valitsemaan oikeat arvot. Lopuksi, kun testausistunto on valmistunut, järjestelmä yrittää luoda tuoterakenteen ja reitityksen, joka vastaa valittuja määritysarvoja ja näyttää virhesanoman, jos jostain menee vikaan.

### <a name="the-configuration-page"></a>Konfiguraatio-sivu

Voit liikkua komponenttien välillä valitsemalla **Seuraava**, tai napsauttamalla komponenttia tuotemääritysmallin puussa huomion kohdistamiseksi siihen.

## <a name="finalizing-a-model-for-configuration"></a>Mallin viimeistely konfiguraatiota varten
Kun tuotemääritysmalli on valmis käytettäväksi määritä-tilaukseen-skenaariossa, on luotava versio. On kuitenkin olemassa useita vaihtoehtoja, joilla mallinnuskokemusta voidaan parantaa.

### <a name="user-interface"></a>Käyttöliittymä

Konfiguraatiokäyttöliittymää voidaan muokata lisäämällä määriteryhmiä yhteen tai useampaan alikomponenttiin. Tällainen ryhmittely voi korostaa tiettyjen määritteiden välisiä suhteita ja auttaa konfiguraation käyttäjää tunnistamaan tuotteen alueen, joka on kyseisellä hetkellä tarkasteltavana.

### <a name="templates"></a>Mallit

On mahdollista luoda yksi tai useampi määritysmalli nopeuttamaan määritysprosessia. Vaihtoehtoisesti voidaan luoda malleja, jotka edistävät tiettyjä määritteiden yhdistelmiä esimerkiksi silloin, kun myyntikampanja keskittyy määrättyjen tuoteominaisuuksien joukkoon.

### <a name="translations"></a>Käännökset

Jos tuotetta tullaan myymään eri maissa/alueilla, on mahdollista luoda käännökset kaikelle tekstille, joka näkyy konfiguraation käyttöliittymässä. Tämä teksti sisältää nimi- ja kuvauskenttien lisäksi myös määritetekstien arvot.

### <a name="versions"></a>Versiot

Viimeinen ja tärkein vaihe viimeistelyprosessissa on luoda tuotemääritysmallin versio. Tämä versio kuvaa päätuotteen, joka voidaan valita konfiguraatiolle tilaus- tai tarjousrivillä, ja tuotemääritysmallin välillä. Versio on hyväksyttävä ja aktivoitava ennen kuin sitä voidaan käyttää määritysistunnossa.

## <a name="extending-a-product-configuration-model-through-the-api"></a>Tuotemääritysmallin laajentaminen ohjelmointirajapinnan kautta
On luotu oma ohjelmointirajapinta (API), jotta kumppanit ja muut, joilla on kehittäjälisenssi, voivat laajentaa tuotemääritysmallin ominaisuuksia. Pääasiallinen tavoite on ollut luoda mekanismi, jolla kumppanit ja asiakkaat, jotka käyttävät nykyistä Product Builderiä, siirtävät Product Builderin malleihin sisältyvän koodin ohjelmointirajapintaan. Näin he voivat siirtää mallinsa Product Builderistä tuotemääritykseen. Uudet kumppanit ja asiakkaat voivat myös hyötyä ohjelmointirajapinnan käytöstä uusien tuotemääritysmallien laajentamisessa.

### <a name="pcadaptor-class"></a>PCAdaptor-luokka

Ohjelmointirajapinta on toteutettu käyttämällä **PCAdaptor**-luokkien joukkoa, joka näyttää tuotemääritysmallien tietorakenteen. **PCAdaptor**-luokan esiintymä on luotava jokaiselle laajennettavalle mallille. Konfigurointi-istunnon jälkeen järjestelmä etsii tämän luokan esiintymiä ja suorittaa sen, jos se löytyy.  

Seuraavassa vuokaaviossa kuvataan tätä prosessia.  

[![Vuokaavio](./media/product_configuration_2.png)](./media/product_configuration_2.png)  

Tuotteen kokoonpanon API-vuokaavio

## <a name="product-configuration"></a>Tuotekonfiguraatio
Tuotemäärityksiä voidaan suorittaa seuraavissa sijainneissa:

-   Myyntitilausrivi
-   Myyntitarjousrivi
-   Ostotilausrivi
-   Tuotantotilausrivi
-   Nimiketarverivi (projekti)

Konfiguraation tarkoitus on luoda erilinen tuotevariantti, joka vastaa asiakkaan vaatimuksia. Kullekin uudelle konfiguraatiolle luodaan yksilöivä konfiguraatiotunnus. Tämä tunnus mahdollistaa seurannan koko varastoinnin ajan.

### <a name="multiple-sites-and-intercompany"></a>Useita toimipaikkoja ja yrityksen sisäinen

Jos konfiguraatio tullaan tekemään toimipaikassa tai jopa yrityksessä, joka eroaa toimipaikasta tai yrityksestä, jossa tuotanto tulee tapahtumaan, tuoterakenne ja reititys luodaan toimittajan toimipaikkaa varten toimittavassa yrityksessä ja laitetaan sinne. Tuotevariantti julkaistaan kaikissa toimitusketjuun osallistuvissa yrityksissä.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]