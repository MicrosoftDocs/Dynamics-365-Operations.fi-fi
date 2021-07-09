---
title: Varastoennusteet
description: Tässä aiheessa kuvataan tarjonta- ja kysyntäennustetoimintoa, jota voidaan käyttää varastoennusteiden luomiseen Microsoft Dynamics 365 Supply Chain Managementissa.
author: crytt
ms.date: 06/08/2021
ms.topic: article
ms.search.form: EcoResProductDetailsExtended, ForecastSales, ForecastPurch, ForecastInvent
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-06-08
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7901bcfc239885aa53863729e573d1f37ba67f81
ms.sourcegitcommit: f21659f1c23bc2cd65bbe7fb7210910d5a8e1cb9
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/24/2021
ms.locfileid: "6306412"
---
# <a name="inventory-forecasts"></a>Varastoennusteet

[!include [banner](../includes/banner.md)]

Tässä aiheessa kuvataan, miten varastoennusteita voidaan tarkastella ja luoda. Voit luoda ja tarkastella nimikkeiden, nimikeryhmien, nimikkeiden kohdistustunnusten, asiakastilien, asiakasryhmien, toimittajatilien ja toimittajaryhmien tarjonta- ja kysyntäennusteita.

Voit valita kullekin ennusteriville käytetyn ennustemallin. Sen jälkeen voit määrittää nimikkeen tai nimikeryhmän sekä määrän tai tapahtumasumman. Voit määrittää myös aikavälit ennustemäärän kohdistusta varten.

Tarjonta- ja kysyntäennusterivit tuottavat varastoennusteen samalle nimikkeen ja mallin yhdistelmälle. Tämä varastoennuste edustaa samalle nimikkeelle syötetyn tarjonnan ja kysynnän välistä saldoa. Arvoa ei voi muokata. Varastoennusteen avulla varastonhallintatiimi voi tarkistaa nimikkeen käytettävissä olevan varaston odotetut muutokset ennustetulta tulevalta jaksolta.

Kun kysyntä ja/tai tarjonta on syötetty, voidaan ennustesuunnittelutoiminnolla laskea materiaalien ja kapasiteetin bruttotarve sekä luoda suunnitellut tilaukset.

## <a name="view-and-manually-enter-forecast-lines"></a><a name="manual-entry"></a>Ennusterivien tarkasteleminen ja syöttäminen manuaalisesti

Tämän menetelmän avulla voit luoda manuaalisesti ennusterivejä tuotteille.

Ennusterivejä voi luoda myös muilla tavoin:

- [Tilastollisen perusennusteen luominen](generate-statistical-baseline-forecast.md).
- [Kysynnän ennusteiden historiatietojen tuonti](import-historical-data.md).
- [Ennusteen luominen Microsoft Azure automaattianalyysipalveluiden avulla](demand-forecasting-setup.md).
- [Tuo kysyntä- tai tarjontaennusterivejä käyttämällä tietohallintakehystä (ForecastDemandForecastEntryStaging- ja ForecastSupplyForecastEntryStaging-tietoentiteetit)](../../dev-itpro/data-entities/data-entities-data-packages.md).

Vaiheen 1 taulukossa näkyvät eri tavat käyttää käytettyjä sivuja.

1. Sen mukaan, minkä tyyppistä entiteettiä varten haluat luoda ennusteen, ja luotavan ennustetyypin mukaan, avaa tarjonta-, kysyntä- tai varastoennustesivu seuraavassa taulukossa kuvatulla tavalla.

    | Entiteetti | Ohjeet |
    |---|---|
    | Vapautetut tuotteet | <ol><li>Mene **Tuotetietojen hallinta \> Tuotteet \> Vapautetut tuotteet**.</li><li>Valitse tuote, jolle ennuste luodaan.</li><li>Valitse toimintoruudun **Suunnitelma**-välilehden **Ennuste**-ryhmässä **Kysyntäennuste**, **Tarjontaennuste** tai **Varastoennuste** sen mukaan, minkä tyyppistä ennustetta haluat käyttää.</li></ol> |
    | Vapautetut tuotevariantit | <ol><li>Mene kohtaan **Tuotetietojen hallinta \> Tuotteet \> Vapautetut tuotevariantit**.</li><li>Valitse variantti, jolle ennuste luodaan.</li><li>Valitse toimintoruudun **Suunnitelma**-välilehden **Ennuste**-ryhmässä **Kysyntäennuste**, **Tarjontaennuste** tai **Varastoennuste** sen mukaan, minkä tyyppistä ennustetta haluat käyttää.</li></ol> |
    | Nimikeryhmät | <ol><li>Valitse **Varastonhallinta \> Asetukset \> Varasto \> Nimikeryhmät**.</li><li>Valitse nimikeryhmä, jolle ennuste luodaan.</li><li>Valitse toimintoruudussa **Ennusteet \> Kysyntä**, **Ennusteet \> Tarjonta** tai **Ennusteet \> Varastoennuste** sen mukaan, minkä tyyppistä ennustetta haluat käyttää.</li></ol> |
    | Nimikkeenkohdistustunnukset | <ol><li>Mene **Varastonhallinta \> Asetukset \> Ennuste**.</li><li>Valitse nimikkeen kohdistustunnus, jolle ennuste luodaan.</li><li>Valitse toimintoruudussa **Kysyntäennuste**.</li></ol> |
    | Asiakkaat | <ol><li>Siirry kohtaan **Pääsuunnittelu \> Ennuste \> Manuaalinen ennusteen syöttö \> Asiakkaat**.</li><li>Valitse asiakas, jolle ennuste luodaan.</li><li>Valitse toimintoruudussa **Määritä kysyntäennuste**.</li></ol> |
    | Asiakasryhmät | <ol><li>Siirry kohtaan **Pääsuunnittelu \> Ennuste \> Manuaalinen ennusteen syöttö \> Asiakasryhmät**.</li><li>Valitse asiakas, jolle ennuste luodaan.</li><li>Valitse toimintoruudussa **Määritä kysyntäennuste**.</li></ol> |
    | Toimittajat | <ol><li>Siirry kohtaan **Pääsuunnittelu \> Ennuste \> Manuaalinen ennusteen syöttö \> Toimittajat**.</li><li>Valitse toimittaja, jolle ennuste luodaan.</li><li>Valitse toimintoruudussa kohta **Syötä** ja avaa **Tarjontaennuste**-sivu.</li></ol> |
    | Toimittajaryhmät | <ol><li>Siirry kohtaan **Pääsuunnittelu \> Ennuste \> Manuaalinen ennusteen syöttö \> Toimittajaryhmät**.</li><li>Valitse toimittaja, jolle ennuste luodaan.</li><li>Valitse toimintoruudussa kohta **Syötä** ja avaa **Tarjontaennuste**-sivu.</li></ol> | 
    | Kaikki rivit | <ul><li>Siirry kohtaan **Pääsuunnittelu \> Ennusteet \> Kysyntäennusterivit** tai **Pääsuunnittelu \> Ennusteet \> Tarjontaennusterivit** sen mukaan, minkä tyyppistä ennustetta haluat käyttää..</li></ul> |

    Näyttöön tulee **Tarjontaennuste**- tai **Kysyntäennuste**-sivu valintasi mukaan. Siinä näkyvät ennen sivun avaamista valitun tietueen ennusterivit.

1. Valitse toimintoruudussa **Uusi** lisätäksesi ennusterivin ruudukkoon sivun yläosassa.
1. Valitse uuden rivin **Malli**-kentästä käytettävä ennustemalli. Syötä sitten muut tarvittavat tiedot, kuten nimike, nimikeryhmä, asiakas- tai toimittajatili tai -ryhmä, nimikemäärä tai tapahtuman kokonaissumma. Tässä ohjeaiheessa jäljempänä on tietoja **Tarjontaennuste**- ja **Kysyntäennuste**-sivuilla käytettävissä olevista kentistä.
1. Jos haluat jakaa ennusteen kaudelle, valitse **Yhteenveto**-välilehdestä **Kohdista ennuste** työkaluriviltä.
1. Tarkista **Kohdistus**-ruudukossa aikajakso ja aikavälit ennustemäärien jakelua varten.

## <a name="supply-forecast-lines"></a>Tarjontaennusterivit

Tarjontaennusteen avulla voit luoda suunnitelman ostettaville nimikkeille. Se kertoo hankintatyöntekijöille, mitä heidän odotetaan tilaavan.

Voit määrittää tarjontaennusteen nimikkeen, nimikeryhmän, nimikkeen varaustunnuksen, toimittajan ja toimittajaryhmän mukaan. Tietoja kaikista tavoista, joilla eri yksiköiden ja tietueiden **Tarjontaennuste**-sivu voidaan avata, on tämän ohjeaiheen aiemmassa kohdassa [Ennusterivien tarkasteleminen ja manuaalinen syöttäminen](#manual-entry).

**Tarjontaennuste**-sivun yläosassa on tarjontaennusterivien ruudukko sekä välilehtijoukko, jonka avulla voit tarkastella ja määrittää lisätietoja valitusta ennusterivistä. Sivun alaosassa on **Kohdistus**-ruudukko.

Seuraavissa aliosioissa kuvaillaan kaikki kussakin välilehdessä käytettävissä olevat kentät sekä kaikki sivun toimintoruudussa ja **Yhteenveto**-välilehden työkalurivissä käytettävissä olevat komennot.

### <a name="action-pane-commands-on-the-supply-forecast-page"></a>Toimintoruudun komennot Tarjontaennuste-sivulla

Seuraavassa taulukossa kuvataan komennot, jotka ovat käytettävissä **Tarjontaennuste** -sivun toimintoruudussa.

| Komento | kuvaus |
|---|---|
| Tallenna | Tallenna nykyiset asetukset. |
| Muokkaa | Määritä sivun asetukset muokattaviksi. |
| Luo uusi | Lisää ennusterivi ylempään ruudukkoon. |
| Delete-näppäin | Poista valittu ennusterivi ylemmästä ruudukosta. |
| Ennustetut saldot | Tarkastele ennustesaldoja, jotka on laskettu valitun rivin mallin tunnukselle nykyiselle tilivuodelle. Saldot jaetaan kauden (kuukauden) mukaan. |
| Kassavirtaennusteet | Tarkastele kirjanpitoon kohdistettuja ennustetapahtumia. Lisätietoja on kohdassa [Kassavirtaennusteet](../../finance/cash-bank-management/cash-flow-forecasting.md). |
| Varasto \> Näytä dimensiot | Valitse varastodimensiot, jotka näytetään **Yhteenveto**-välilehden ruudukossa. |

### <a name="toolbar-commands-on-the-overview-tab-of-the-supply-forecast-page"></a>Tarjontaennuste-sivun Yhteenveto-välilehden työkalurivin komennot

Seuraavassa taulukossa kuvataan komennot, jotka ovat käytettävissä **Tarjontaennuste** -sivun **Yhteenveto**-välilehden työkalurivissä.

| Komento | kuvaus |
|---|---|
| Kohdista ennuste | Jos käytät kohdistusmenetelmää, luo yksittäiset ajoitusrivit ennustetapahtumalle. Rivin määrä jaetaan sitten päivämäärän (valittujen aikavälien mukaan), määrän ja summan mukaan koko aikajaksolle. |
| Joukkopäivitys | Avaa **Muokkaa ennustetapahtumia** -sivu. (Lisätietoja on jäljempänä tässä ohjeessa kohdassa [Ennustetapahtumien joukkopäivitys](#bulk-update).) |
| Varastoennuste | Avaa valitulle nimike-/malliyhdistelmälle suodatettu **Varastoennuste**-sivu. (Lisätietoja on jäljempänä tässä ohjeessa kohdassa [Varastoennusteet](#inventory-forecast).) |
| Luo nimiketarve | Avaa valintaikkuna, jossa voit luoda nimiketarpeet sekä projektiin liittyvien ennustetapahtumien myyntitilaus- tai nimikekirjauskansion rivit. Vaikka tämä komento on käytettävissä sekä tarjontaennusteriveillä että kysyntäennusteriveillä, sitä ei voi käyttää **Tarjontaennuste**-sivulla. |

### <a name="the-overview-tab-on-the-supply-forecast-page"></a>Tarjontaennuste-sivun Yhteenveto-välilehti

Seuraavassa taulukossa kuvataan **Tarjontaennuste**-sivun **Yhteenveto**-välilehden kentät.

| Kenttä | kuvaus |
|---|---|
| **Malli** | Ennustemalli, johon tapahtuma liittyy. |
| **Päivämäärä** | Tapahtuman aloituspäivämäärä. |
| **Toimittajanro** | Tapahtumaan liittyvä toimittajatili. |
| **Toimittajaryhmä** | Tapahtumaan liittyvä toimittajaryhmä. |
| **Nimiketunnus** | Nimikkeen tunniste. |
| **Nimikeryhmä** | Nimikeryhmä, johon tapahtuma liittyy. |
| **Nimikkeenkohdistustunnus** | Ennusteeseen liittyvä nimikkeenkohdistustunnus. |
| **Todellinen paino** | Ennustemäärä määritettynä todellisen painon yksikkönä. |
| **Todellisen painon yksikkö** | Todellisen painon yksikkö, jossa nimike ostetaan. Arvo noudetaan automaattisesti nimikkeen asetuksista. |
| **Määrä** | Ennustemäärä määritettynä ostoyksikkönä. |
| **Yksikkö** | Yksikkö, jossa nimike ostetaan. Arvo noudetaan automaattisesti nimikkeen asetuksista. Voit kuitenkin muokata sitä, jos yksikkömuunnokset on määritetty. |
| **summa** | Ennustetapahtuman ennusteeseen tuoma bruttosumma, josta on vähennetty alennukset. |
| **Valuutta** | Ennustetapahtumassa käytetty valuutta. Oletusvaluutta lisätään automaattisesti, mutta voit valita toisen valuutan. |
| (Muut dimensiot) | Ruudukon sarakkeina voidaan näyttää lisädimensioita. Valitse toimintoruudusta **Näytä dimensiot** valitaksesi näytettävät lisädimensiot. |

### <a name="the-general-tab-on-the-supply-forecast-page"></a>Tarjontaennuste-sivun Yleiset-välilehti

**Yleiset**-välilehdessä on lisätietoja **Yhteenveto**-välilehdessä valittuna olevasta rivistä. Osa näistä tiedoista toistuu **Yhteenveto**-välilehdestä. Seuraavassa taulukossa kuvataan kentät, jotka ovat näkyvät vain **Yleiset**-välilehdessä.

| Kenttä | kuvaus |
|---|---|
| Raportoi | Valitse tämän vaihtoehdon arvoksi *Kyllä*, jos haluat sisällyttää tapahtuman raportointiin. |
| Huomautukset | Kirjoita tarvittaessa ennustetapahtumaa koskevat huomautukset. |
| Käytössä | Valitsemalla tämän valintaruudun voit sisällyttää tapahtuman budjettiraportointiin. |
| Sisällytä kassavirtaennusteisiin | Valitse tämä valintaruutu, jos haluat kohdistaa ennustetapahtuman kirjanpitoon. Tämän valintaruudun asetusta ei voi muokata raportointitapahtumia varten. |
| Arvonlisäveroryhmä | Veroryhmä, jota käytetään ennustetapahtuman veron määrityksessä. |
| Nimikkeen arvonlisäveroryhmä | Nimikkeen veroryhmä, jota käytetään ennustetapahtuman veron määrityksessä. |
| Tapa | <p>Valitse ennustetapahtuman kohdistusmenetelmä:</p><ul><li>**Ei mitään** – Kohdistusta ei tehdä.</li><li>**Kausi** – Ennusta sama määrä jokaiselle kaudelle. Jos valitset tämän arvon, määritä määrä **Per**-kentässä ja aikayksikkö **Yksikkö**-kentässä.</li><li>**Avain** – Kohdista ennuste **Kausiavain**-kentässä määritettävän kauden kohdistustunnuksen perusteella. Voit käyttää tätä menetelmää, kun haluat ottaa huomioon kausittaisen vaihtelun.</li></ol>|
| Per | <p>Kirjoita aikavälien määränä aika, kuinka pitkälle ennuste ulottuu tulevaisuudessa. Tämä kenttä on käytettävissä vain, jos valitset **Menetelmä**-kentässä *Kausi*.</p><p>Jos esimerkiksi valitset **Menetelmä**-kentästä *Kausi*-vaihtoehdon, syötä **Per**-kenttään arvoksi *1* ja valitse **Yksikkö**-kentästä *Kuukaudet*-vaihtoehto, Määritä **Loppu**-kentässä päättymispäivämäärä vuoden päähän. Tässä tapauksessa luodaan kullekin tulevan vuoden kuukaudelle yksi ennusterivi, joka perustuu otsikkorivillä määritettyyn nimikkeeseen ja määrään.</p> |
| Yksikkö | Valitse aikavälin yksikkö: *Päivät*, *Kuukaudet* tai *Vuodet*. Kohdistus vastaa **Per**-kenttään määritettyjen päivien, kuukausien tai vuosien määrää.|
| Kausiavain | Määritä kaudenkohdistustunnus. |
| Loppu | Määritä päättymispäivämäärä **Per**- ja **Yksikkö**-kenttiä käytettäessä. |

### <a name="the-item-tab-on-the-supply-forecast-page"></a>Tarjontaennuste-sivun Nimike-välilehti

**Nimike**-välilehdessä näkyy nimikkeen lisätietoja **Yhteenveto**-välilehdessä valittuna olevalle riville.

**Nimike**-välilehden yläosassa ruudukko toistaa nimikkeen tiedot, jotka näkyvät myös **Yhteenveto**-välilehdessä. Lisäksi se sisältää **Yksikköhinta**-kentän, joka ilmaisee **Yksikkö**-kentässä määritettyjen yksiköiden ostohinnan. Yksikköhinta noudetaan automaattisesti nimikkeen asetuksista, mutta sitä voi muokata.

Ruudukon alla olevat kentät antavat lisätietoja nimikkeestä. Osa näistä tiedoista toistuu **Yhteenveto**-välilehdestä. Seuraavassa taulukossa kuvataan kentät, jotka näkyvät vain **Nimike**-välilehdessä.

| Kenttä | kuvaus |
|---|---|
| Hintayksikkö | Yksikkömäärä, jota ostohinta koskee. Arvo noudetaan automaattisesti  Nimikkeet-taulukosta, mutta sitä voi muokata. |
| Ostojen kulut | Ostohinnan kiinteät kulut. Kulut ovat riippumattomia määrästä. |
| Alennusprosentti | Alennus prosenttiosuutena. |
| Alennuksen suuruus | Alennus summana myyntiyksikköä kohden. |
| Bruttosumma | Summa, kun alennuksia ei käytetä. |
| Määrä | Tapahtuman määrä nimikkeen varastoyksikköinä. |
| Alituoterakenne | Määritetyn alituoterakenteen numero. |
| Alireititys | Määritetyn alireitityksen reititysnumero. |

### <a name="the-financial-dimensions-tab-on-the-supply-forecast-page"></a>Tarjontaennuste-sivun Taloushallinnon dimensiot -välilehti

**Taloushallinnon dimensiot** -välilehdessä näkyvät kaikki **Yhteenveto**-välilehdessä valittuna olevan rivin taloushallinnon dimension arvot.

### <a name="the-inventory-dimensions-tab-on-the-supply-forecast-page"></a>Tarjontaennuste-sivun Varastodimensiot-välilehti

**Varastodimensiot** -välilehdessä näkyvät kaikki **Yhteenveto**-välilehdessä valittuna olevan rivin varastodimension arvot.

### <a name="the-allocation-grid-on-the-supply-forecast-page"></a>Tarjontaennuste-sivun Kohdistus-ruudukko

Jos käytät nimikkeenkohdistustunnusta tai olet syöttänyt nimike-ennusteen yhdelle tai useammalle tulevalle kaudelle, voit kohdistaa ennusteen valitsemalla **Yhteenveto**-välilehden työkaluriviltä **Kohdista ennuste**. Määrä jaetaan **Kohdistus**-ruudukon rivien osoittamalla tavalla.

## <a name="demand-forecast-lines"></a>Kysynnän ennusteen rivit

Kysyntäennusteen avulla voit määrittää tai luoda asiakkaalle kysyntää. Se auttaa myynti- ja markkinointityöntekijöitä tiedottamaan pääsuunnittelun työntekijöille odotetusta kysynnästä tulevan ennustekauden aikana.

Voit määrittää kysyntäennusteen nimikkeen, nimikeryhmän, nimikkeen varaustunnuksen, asiakkaan ja asiakasryhmän mukaan. Tietoja kaikista tavoista, joilla eri yksiköiden ja tietueiden **Kysyntäennuste**-sivu voidaan avata, on tämän ohjeaiheen aiemmassa kohdassa [Ennusterivien tarkasteleminen ja manuaalinen syöttäminen](#manual-entry).

**Kysyntäennuste**-sivun yläosassa on kysyntäennusterivien ruudukko sekä välilehtijoukko, jonka avulla voit tarkastella ja määrittää lisätietoja valitusta ennusterivistä. Sivun alaosassa on **Kohdistus**-ruudukko.

Seuraavissa aliosioissa kuvaillaan kaikki kussakin välilehdessä käytettävissä olevat kentät sekä kaikki sivun toimintoruudussa ja **Yhteenveto**-välilehden työkalurivissä käytettävissä olevat komennot.

### <a name="action-pane-commands-on-the-demand-forecast-page"></a>Toimintoruudun komennot Kysyntäennuste-sivulla

Seuraavassa taulukossa kuvataan komennot, jotka ovat käytettävissä **Kysyntäennuste** -sivun toimintoruudussa.

| Komento | kuvaus |
|---|---|
| Tallenna | Tallenna nykyiset asetukset. |
| Muokkaa | Määritä sivun asetukset muokattaviksi. |
| Luo uusi | Lisää ennusterivi ylempään ruudukkoon. |
| Delete-näppäin | Poista valittu ennusterivi ylemmästä ruudukosta. |
| Ennustetut saldot | Tarkastele ennustesaldoja, jotka on laskettu valitun rivin mallin tunnukselle nykyiselle tilivuodelle. Saldot jaetaan kauden (kuukauden) mukaan. |
| Kassavirtaennuste | Tarkastele ennustetapahtumia, jotka on kohdistettava kirjanpitoon. Lisätietoja on kohdassa [Kassavirtaennusteet](../../finance/cash-bank-management/cash-flow-forecasting.md). |
| Näytä dimensiot | Valitse tuote-, varasto - ja seurantadimensiot, jotka näytetään **Yhteenveto**-välilehden ruudukossa. |
| Kirjanpidon esikatselu | Tarkastele valitun tapahtuman kirjanpitokirjauksia. |
| Siirrä tarjousrivit | Siirtää tarjousrivit valittuun projektiin. |

### <a name="toolbar-commands-on-the-overview-tab-of-the-demand-forecast-page"></a>Kysyntäennuste-sivun Yhteenveto-välilehden työkalurivin komennot

Seuraavassa taulukossa kuvataan komennot, jotka ovat käytettävissä **Kysyntäennuste** -sivun **Yhteenveto**-välilehden työkalurivissä.

| Komento | kuvaus |
|---|---|
| Kohdista ennuste | Jos käytät kohdistusmenetelmää, luo yksittäiset ajoitusrivit ennustetapahtumalle. Rivin määrä jaetaan sitten päivämäärän (valittujen aikavälien mukaan), määrän ja summan mukaan koko aikajaksolle. |
| Joukkopäivitys | Avaa **Muokkaa ennustetapahtumia** -sivu. (Lisätietoja on jäljempänä tässä ohjeessa kohdassa [Ennustetapahtumien joukkopäivitys](#bulk-update).) |
| Varastoennuste | Avaa valitulle nimike-/malliyhdistelmälle suodatettu **Varastoennuste**-sivu. (Lisätietoja on jäljempänä tässä ohjeessa kohdassa [Varastoennusteet](#inventory-forecast).) |
| Luo nimiketarve | Avaa valintaikkuna, jossa voit luoda nimiketarpeet sekä projektiin liittyvien ennustetapahtumien myyntitilaus- tai nimikekirjauskansion rivit. |

### <a name="the-overview-tab-on-the-demand-forecast-page"></a>Kysyntäennuste-sivun Yhteenveto-välilehti

Seuraavassa taulukossa kuvataan **Kysyntäennuste**-sivun **Yhteenveto**-välilehden kentät.

| Kenttä | kuvaus |
|---|---|
| **Tehtävän nimi** | Sen erätehtävän nimi, jolla ennusterivi luotiin. |
| **Malli** | Ennustemalli, johon tapahtuma liittyy. |
| **Päivämäärä** | Tapahtuman aloituspäivämäärä. |
| **Asiakastili** | Tapahtumaan liittyvä asiakastili. |
| **Asiakasryhmä** | Tapahtumaan liittyvä asiakasryhmä. |
| **Nimiketunnus** | Nimikkeen tunniste. |
| **Tuotteen nimi** | Nimikkeen kuvaus. |
| **Nimikkeenkohdistustunnus** | Varaston ennustekohdistuksessa käytettävä nimikkeenkohdistustunnus. |
| **Myyntimäärä** | Tapahtuman määrä määritettynä myyntiyksikkönä. |
| **Yksikkö** | Yksikkö, jona nimike myydään. |
| **summa** | Ennustetapahtuman ennusteeseen tuoma bruttosumma, josta on vähennetty alennukset. |
| **Myyntihinta** | **Hintayksikkö**-kentässä määritettyjen yksiköiden myyntihinta. Arvo noudetaan nimikkeen asetuksista, mutta sitä voi muokata. |
| **Myyntivaluutta** | Ennustetapahtumassa käytetty valuutta. Oletusvaluutta lisätään automaattisesti, mutta voit valita toisen valuutan. |
| **Todellinen paino** | Ennustemäärä määritettynä todellisen painon yksikkönä. |
| **Todellisen painon yksikkö** | Todellisen painon yksikkö, jossa nimike myydään. Arvo noudetaan automaattisesti nimikkeen asetuksista. |
| (Muut dimensiot) | Ruudukon sarakkeina voidaan näyttää tuotteen, varaston ja seurannan lisädimensioita. Valitse toimintoruudusta **Näytä dimensiot** valitaksesi näytettävät lisädimensiot. |

### <a name="the-general-tab-on-the-demand-forecast-page"></a>Kysyntäennuste-sivun Yleiset-välilehti

**Yleiset**-välilehdessä on lisätietoja **Yhteenveto**-välilehdessä valittuna olevasta rivistä. Osa näistä tiedoista toistuu **Yhteenveto**-välilehdestä. Seuraavassa taulukossa kuvataan kentät, jotka ovat näkyvät vain **Yleiset**-välilehdessä.

| Kenttä | kuvaus |
|---|---|
| Kysynnän ennusteen järjestysnumero | Kysyntäennusterivin yksilöivä numero. Numero luodaan käyttämällä kysyntäennusteille **pPääsuunnittelun parametrit** -sivulla valittua numerosarjaa. |
| Nimikeryhmä | Nimikeryhmä, johon tapahtuma liittyy. |
| Raportoi | Valitse tämän vaihtoehdon arvoksi *Kyllä*, jos haluat sisällyttää tapahtuman raportointiin. |
| Huomautukset | Kirjoita tarvittaessa ennustetapahtumaa koskevat huomautukset. |
| Käytössä | Valitsemalla tämän valintaruudun voit sisällyttää tapahtuman budjettiraportointiin. Tämän valintaruudun asetusta ei voi muokata raportointitapahtumia varten. |
| Sisällytä kassavirtaennusteisiin | Valitse tämä valintaruutu, jos haluat kohdistaa ennustetapahtuman kirjanpitoon. Tämän valintaruudun asetusta ei voi muokata raportointitapahtumia varten. Lisätietoja on kohdassa [Kassavirtaennusteet](../../finance/cash-bank-management/cash-flow-forecasting.md). |
| Arvonlisäveroryhmä | Veroryhmä, jota käytetään ennustetapahtuman veron määrityksessä. |
| Nimikkeen arvonlisäveroryhmä | Nimikkeen veroryhmä, jota käytetään ennustetapahtuman veron määrityksessä. |
| Tapa | <p>Valitse ennustetapahtuman kohdistusmenetelmä:</p><ul><li>**Ei mitään** – Kohdistusta ei tehdä.</li><li>**Kausi** – Ennusta sama määrä jokaiselle kaudelle. Jos valitset tämän arvon, määritä määrä **Per**-kentässä ja aikayksikkö **Yksikkö**-kentässä.</li><li>**Avain** – Kohdista ennuste **Kausiavain**-kentässä määritettävän kauden kohdistustunnuksen perusteella. Voit käyttää tätä menetelmää, kun haluat ottaa huomioon kausittaisen vaihtelun.</li><ul>|
| Per | <p>Kirjoita aikavälien määränä aika, kuinka pitkälle ennuste ulottuu tulevaisuudessa. Tämä kenttä on käytettävissä vain, jos valitset **Menetelmä**-kentässä *Kausi*.</p><p>Jos esimerkiksi valitset **Menetelmä**-kentästä *Kausi*-vaihtoehdon, syötä **Per**-kenttään arvoksi *1* ja valitse **Yksikkö**-kentästä *Kuukaudet*-vaihtoehto, Määritä **Loppu**-kentässä päättymispäivämäärä vuoden päähän. Tässä tapauksessa luodaan kullekin tulevan vuoden kuukaudelle yksi ennusterivi, joka perustuu otsikkorivillä määritettyyn nimikkeeseen ja määrään. |
| Yksikkö | Valitse aikavälin yksikkö: *Päivät*, *Kuukaudet* tai *Vuodet*. Kohdistus vastaa **Per**-kenttään määritettyjen päivien, kuukausien tai vuosien määrää.|
| Kausiavain | Määritä ennusteen kohdistuksessa käytettävä kauden kohdistustunnus. Lisätietoja kohdassa [Budjettisuunnittelun tietojen kohdistus](../../finance/budgeting/budget-planning-data-allocation.md). |
| Loppu | Määritä päättymispäivämäärä **Per**- ja **Yksikkö**-kenttiä käytettäessä. |

### <a name="the-item-tab-on-the-demand-forecast-page"></a>Kysyntäennuste-sivun Nimike-välilehti

**Nimike**-välilehdessä on nimikkeen lisätietoja **Yhteenveto**-välilehdessä valittuna olevasta rivistä. Osa näistä tiedoista toistuu **Yhteenveto**-välilehdestä. Seuraavassa taulukossa kuvataan kentät, jotka ovat näkyvät vain **Nimike**-välilehdessä.

| Kenttä | kuvaus |
|---|---|
| Hintayksikkö | Myyntiyksiköiden määrä, jota myyntihinta koskee. Arvo noudetaan automaattisesti  Nimikkeet-taulukosta, mutta sitä voi muokata. |
| Myynnin kulut | Myyntihinnan kiinteät kulut. Kulut ovat riippumattomia määrästä. |
| Kustannushinta | Valitun ennustetapahtuman kustannukset varastoyksiköittäin. Arvo noudetaan automaattisesti nimiketaulukosta, mutta niitä voi muokata. |
| Alennusprosentti | Alennus prosenttiosuutena. |
| Alennuksen suuruus | Alennus summana myyntiyksikköä kohden. |
| Bruttosumma | Summa, kun alennuksia ei käytetä. |
| Varastomäärä | Tapahtuman määrä nimikkeen varastoyksikköinä. |
| Käytä erityistä tuoterakennetta | Määritetyn tuoterakenteen numero. |
| Käytä erityistä reittiä | Määritetyn alireitityksen reititysnumero. |

### <a name="the-project-tab-on-the-demand-forecast-page"></a>Kysyntäennuste-sivun Projekti-välilehti

**Projekti**-välilehdessä on projektin lisätietoja **Yhteenveto**-välilehdessä valittuna olevasta rivistä. Osa näistä tiedoista toistuu **Yhteenveto**-, **Yleiset**- ja **Nimike**-välilehdistä. Seuraavassa taulukossa kuvataan kentät, jotka ovat näkyvät vain **Projekti**-välilehdessä.

| Kenttä | kuvaus |
|---|---|
| Projektipäiväys | Kysyntäennusteen tapahtuman päivämäärä. |
| Projektitunnus | Sen projektin tunnus, johon nykyinen tapahtuma viittaa. |
| Rahoituslähde | Kysyntäennusteeseen liittyvä rahoituslähde. |
| Tehtävän numero | Kysyntäennusteen tapahtumaan liittyvä aktiviteetti. |
| Luokka | Nykyisen tapahtuman kustannusluokka. |
| Rivin ominaisuus | Tila, johon tapahtuma liittyy. |
| Tapahtumatunnus | Kysyntäennusteen tapahtuman järjestelmätunnus. |
| Kustannusten summa | Kysyntäennusteen tapahtuman summa. |
| Yksikköhinta | Yksikkökohtainen hinta. |
| Muokannut | Valittua tapahtumaa viimeksi muokanneen työntekijän tunnus. |
| Laskun päivämäärä | Kirjoita odotettu laskupäivä. |
| Eliminointipäivä | Tarkastele tai muokkaa eliminointipäivää. Kun ennuste luodaan, eliminointipäiväksi määritetään projektin päättymispäivämäärä. Jos projektilla ei ole päättymispäivämäärää, käytetään projektin päivämäärää. Tämä kenttä koskee kiinteähintaisia projekteja ja investointiprojekteja. |
| Kustannuksen maksupäivä | Kirjoita oston odotettu maksupäivämäärä. |
| Myynnin maksupäivä | Kirjoita myynnin odotettu maksupäivämäärä. |

### <a name="the-financial-dimensions-tab-on-the-demand-forecast-page"></a>Kysyntäennuste-sivun Taloushallinnon dimensiot -välilehti

**Taloushallinnon dimensiot** -välilehdessä näkyvät kaikki **Yhteenveto**-välilehdessä valittuna olevan rivin taloushallinnon dimension arvot.

### <a name="the-inventory-dimensions-tab-on-the-demand-forecast-page"></a>Varastoennuste-sivun Taloushallinnon dimensiot -välilehti

**Varastodimensiot** -välilehdessä näkyvät kaikki **Yhteenveto**-välilehdessä valittuna olevan rivin varastodimension arvot.

### <a name="the-allocation-grid-on-the-demand-forecast-page"></a>Kysyntäennuste-sivun Kohdistus-ruudukko

Jos käytät nimikkeenkohdistustunnusta tai olet syöttänyt nimike-ennusteen yhdelle tai useammalle tulevalle kaudelle, voit kohdistaa ennusteen valitsemalla **Yhteenveto**-välilehden työkaluriviltä **Kohdista ennuste**. Määrä jaetaan **Kohdistus**-ruudukon rivien osoittamalla tavalla.

## <a name="inventory-forecast"></a><a name="inventory-forecast"></a>Varastoennuste

Tarjonta- ja kysyntäennusterivien sivuilla on **Varastoennuste**-painike, joka avaa samalla nimike-/malliyhdistelmällä suodatetun näkymän **Varastoennuste**-sivusta. Varastoennuste edustaa samalle nimikkeelle syötetyn tarjonnan ja kysynnän välistä saldoa. Arvoa ei voi muokata. Varastoennusteen avulla varastonhallintatiimi voi tarkistaa nimikkeen käytettävissä olevan varaston odotetut muutokset ennustetulta tulevalta jaksolta.

### <a name="the-action-pane-on-the-inventory-forecast-page"></a>Toimintoruutu Varastoennuste-sivulla

Seuraavassa taulukossa kuvataan komennot, jotka ovat käytettävissä **Varastoennuste** -sivun toimintoruudussa.

| Toimenpide | kuvaus |
|---|---|
| Tarjontaennuste | Avaa samalle nimike-/malli-/päivämääräyhdistelmälle suodatettu **Tarjontaennuste**-sivu. |
| Kysynnän ennuste | Avaa samalle nimike-/malli-/päivämääräyhdistelmälle suodatettu **Kysyntäennuste**-sivu. |
| Varasto \> Näytä dimensiot | Valitse tuote-, varasto - ja seurantadimensiot, jotka näytetään **Yhteenveto**-ruudukossa. |

### <a name="the-grid-on-the-inventory-forecast-page"></a>Ruudukko Varastoennuste-sivulla

Seuraavassa taulukossa kuvataan **Varastoennuste** -sivun ruudukon kentät.

| Kenttä | kuvaus |
|---|---|
| **Malli** | Ennustemalli, johon tapahtuma liittyy. |
| **Nimiketunnus** | Nimikkeen tunniste. |
| **Budjettipäivämäärä** | Ennustetapahtuman päivämäärä. |
| **Ennustetyyppi** | Tapahtuman lähde (*Kysyntäennuste* tai *Tarjontaennuste*). |
| **Todellinen paino** | Ennustemäärä todellisen painon yksikkönä. |
| **Määrä** | Ennusteen määrä varastoyksikköinä. |
| **Todellinen paino, kertynyt** | Kertynyt ennustemäärä todellisen painon yksikköinä, kun samalle nimikkeelle on kertynyt useita ennusterivejä. |
| **Alituoterakenne** | Määritetyn alituoterakenteen numero. |
| **Alireititys** | Määritetyn alireitityksen reititysnumero. |
| (Muut dimensiot) | Ruudukon sarakkeina voidaan näyttää lisädimensioita. Valitse toimintoruudusta **Varasto \> Näytä dimensiot** valitaksesi näytettävät lisädimensiot. |

## <a name="bulk-update-forecast-transactions"></a><a name="bulk-update"></a>Ennustetapahtumien joukkopäivitys

Näiden ohjeiden avulla voit käsitellä aiemmin luotuja ennustetapahtumarivejä. Voit kopioida, muokata ja poistaa ennustetapahtumarivejä.

1. Valitse tarjonta- tai kysyntäennusterivien sivulla **Joukkopäivitys**.
1. Valitse valintaikkunassa **Suodata**.
1. Valitse **Alue**-välilehdellä ehdot, jotka määrittävät kopioitavat, muokattavat tai poistettavat lähde-ennustetiedot. Tällaisia tietoja voivat olla ennustemalli, nimiketunnus ja asiakastili.
1. Vahvista valinta valitsemalla **OK**.

    Kun tiedot on valittu, voit **Muokkaa ennustetapahtumia** -valintaikkunan avulla määrittää, miten tietoja kopioidaan, muokataan tai poistetaan.

    > [!NOTE]
    > Suodatusvaihe on edellytyksenä **Joukkomuokkaus**-toimintojen käyttämiselle. Jos ohitat sen, ohjelma valitsee ja päivittää **kaikki** ennusterivit. Tämän vuoksi saatat vahingossa aiheuttaa tapahtumien kaksoiskappaleita tai poistoja.

1. Valitse **Hallinta**-osassa, haluatko kopioida, päivittää vai poistaa valittuja ennustetapahtumia.
1. **Kentän muutokset** -osassa voit muuttaa ennusteen parametreja. Valitse parametrin valintaruutu ja valitse käytettävissä olevista vaihtoehdoista haluamasi. Valitse esimerkiksi **Malli**-valintaruutu ja valitse sitten ennustemallin numero. Olemassa olevat ennusterivit kopioidaan valittuun ennustemalliin.
1. Voit siirtää ennusteen alku- ja loppupäiviä eteenpäin tai taaksepäin käyttämällä **Kauden muutos** -osaa. Valitse valintaruutu ja määritä ajanjakso ennusteen päivämäärien muuttamista varten käyttämällä määrä- ja kausikenttiä. Voit siirtää aloituspäivää taaksepäin (jolloin se tehdään aiemmin) syöttämällä negatiivinen arvo.

    Jos esimerkiksi haluat viivyttää ennustetapahtuman alkamispäivää kuudella kuukaudella, valitse valintaruutu, kirjoita määräksi *6* ja valitse kaudeksi *Kuukaudet*.

1. **Korjaa kenttä** -osan avulla voit päivittää todelliset ennusteen tiedot. Valitse **Kenttä**-kentästä muutettavat ehdot. Kirjoita **Kerroin**-kenttään kerroin, jota sovelletaan valittuun ehtoon, tai määritä yhteenlaskun tai vähennyslaskun vakio. Voit esimerkiksi valita ehdoksi *Määrä* ja antaa kertoimeksi *1,5*, jos nimikemäärä kerrotaan 1,5:llä. Voit myös kirjoittaa vakioluvun, esimerkiksi *-25*, jolloin nimikemäärästä vähennetään 25 yksikköä.
1. **Taloushallinnon dimensiot** -osassa voit päivittää ennusterivien taloushallinnon dimensiot. Valitse muutettavat taloushallinnon dimensiot ja anna sitten valittuihin dimensioihin sovellettava arvo.
1. Ota muutokset käyttöön valitsemalla **OK**.

## <a name="use-forecasts-with-master-planning"></a>Käytä ennusteita pääsuunnittelussa

Kun olet syöttänyt kysyntäennusteen ja/tai tarjontaennusteen, voit sisällyttää ennusteet pääsuunnittelun aikana odotetun kysynnän ja/tai tarjonnan huomioon ottamiseksi pääsuunnitteluajossa. Kun ennusteet sisältyvät pääsuunnitteluun, järjestelmä laskee materiaalien ja kapasiteetin bruttotarpeet ja luo suunnitellut tilaukset.

### <a name="set-up-a-master-plan-to-include-an-inventory-forecast"></a>Pääsuunnittelun määrittäminen sisältämään varaston ennuste

Pääsuunnitelma asennetaan sisältämään varaston ennuste seuraavasti.

1. Siirry kohtaan **Pääsuunnittelu \> Määritykset \> Suunnitelmat \> Pääsuunnitelmat**.
1. Valitse aiemmin luotu suunnitelma tai luo uusi suunnitelma.
1. Valitse **Yleiset**-pikavälilehdellä seuraavat lisäkentät:

    - **Ennustemalli** – Valitse käytettävä ennustemalli. Tämä malli otetaan huomioon, kun nykyiselle pääsuunnitelmalle luodaan toimitusehdotuksia.
    - **Sisällytä tarjonnan ennuste** – Määritä vaihtoehdoksi *Kyllä*, jos haluat sisällyttää tarjonnan ennusteen nykyiseen pääsuunnitelmaan. Jos määrität vaihtoehdoksi *Ei*, tarjonnan ennusteen tapahtumia ei sisällytetä pääsuunnitelmaan.
    - **Sisällytä kysynnän ennuste** – Määritä vaihtoehdoksi *Kyllä*, jos haluat sisällyttää kysynnän ennusteen nykyiseen pääsuunnitelmaan. Jos määrität vaihtoehdoksi *Ei*, kysynnän ennusteen tapahtumia ei sisällytetä pääsuunnitelmaan.
    - **Ennustevaatimusten vähentämiseen käytetty menetelmä** – Valitse menetelmä, jolla ennustevaatimuksia vähennetään. Lisätietoja on [Ennusteiden vähennysavaimet](planning-optimization/demand-forecast.md#reduction-keys).

1. Voit määrittää **Aikarajat päivinä** -pikavälilehdessä seuraavat kentät määrittämään ennusteen sisältävän kauden seuraavien aikana:

    - **Ennustesuunnitelma** – Määritä asetukseksi *Kyllä*, jolloin yksittäisistä kattavuusryhmistä peräisin oleva ennustesuunnitelman aikaraja ohitetaan. Määritä asetukseksi *Ei*, jolloin käytetään nykyisen pääsuunnitelman yksittäisen kattavuusryhmien arvoja.
    - **Ennusteen ajanjakso** – jos **Ennustesuunnitelman** -asetuksena on *Kyllä*, määritä kuinka monta päivää (kuluvasta päivämäärästä) kysynnän ennustetta käytetään.

    > [!IMPORTANT]
    > **Ennustesuunnitelma**-valintaa ei vielä tueta suunnittelun optimoinnissa.

### <a name="run-a-master-plan-that-includes-an-inventory-forecast"></a>Suorita pääsuunnittelu, joka sisältää varaston ennusteen

Pääsuunnitelma suoritetaan sisältämään varaston ennuste seuraavasti.

1. Mene kohtaan **Pääsuunnittelu \> Työtila \> Pääsuunnittelu**.
1. Lisää tai valitse **Pääsuunnittelu**-kentässä pääsuunnitelma, joka määritetään edellisessä menetelmässä.
1. Valitse **Pääsuunnittelu**-ruudussa **Suorita**.
1. Määritä **Pääsuunnittelu**-valintaikkunassa **Seuraa käsittelyaikaa** -asetuksen arvoksi *Kyllä*.
1. Syötä **Säikeiden määrä** -kenttään numero.
1. Valitse **Sisällytettävät tietueet** -pikavälilehdessä **Suodatus**.
1. Näyttöön tulee vakiokyselyeditorin valintaikkuna. Valitse **Alue**-välilehdellä rivi, jonka **Kenttä**-kentän arvona on *Nimiketunnus*.
1. Valitse **Kriteeri**-kentästä suunnitelmaan sisällytettävä nimiketunnus.
1. Valitse **OK**.

Voit tarkastella laskettuja tarpeita avaamalla **Bruttotarve**-sivun. Valitse esimerkiksi toimintoruudun **Vapautetut tuotteet** -sivun **Suunnitelma**-välilehden **Tarve**-ryhmästä **Bruttotarve**.

Voit tarkastella luotuja suunniteltuja tilauksia kohdassa **Pääsuunnittelu \> Yhteiset \> Suunnitellut tilaukset** ja valita soveltuvan ennustesuunnitelman.

## <a name="additional-resources"></a>Lisäresurssit

- [Kysynnän ennustepalveluiden yleiskatsaus](introduction-demand-forecasting.md)
- [Kysynnän ennusteiden asetukset](demand-forecasting-setup.md)
- [Tilastollisen perusennusteen luominen](generate-statistical-baseline-forecast.md)
- [Manuaalisten oikaisujen tekeminen perusennusteeseen](manual-adjustments-baseline-forecast.md)
- [Pääsuunnittelu ja kysynnän ennusteet](planning-optimization/demand-forecast.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
