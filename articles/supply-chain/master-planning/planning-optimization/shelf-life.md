---
title: Pääsuunnittelu tuotteille, joiden säilyvyysaika on rajallinen
description: Tässä artikkelissa kerrotaan, miten määritetään pilaantumisalttiiden tuotteiden säilyvyysajan huomioon ottavat suunnitteluominaisuudet ja miten niitä käytetään.
author: t-benebo
ms.date: 08/10/2022
ms.topic: article
ms.search.form: ReqPlanSched, CustTable, EcoResProductDetailsExtended, InventModelGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-08-10
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: 95c905cbcc3c057dbccf2b7d6e894b1e99ddfba5
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/23/2022
ms.locfileid: "9337148"
---
# <a name="master-planning-for-products-with-limited-shelf-life"></a>Pääsuunnittelu tuotteille, joiden säilyvyysaika on rajallinen

[!include [banner](../../includes/banner.md)]

Säilyvyysaika on aika, jonka tuote voi olla varastossa ennen kuin siitä tulee käyttö- ja myyntikelvoton. Rajallisen säilyvyysajan omaavissa tuotteissa käytetään todennäköisesti FEFO (first out) -varastointistrategiaa. Se priorisoi nimikkeiden kulutuksen ja myynnin nimikkeiden säilyvyysajan perusteella. Tämä varastointistrategia koskee ruokatarvikkeita, lääkkeitä ja muita lyhyen varastointiajan omaavia tuotteita. FEFO-menetelmässä varaston nimikkeet säilytetään samalla tavalla kuin supermarketin hyllyllä: pitkän säilyvyysajan omaavat tuotteet sijoitetaan hyllyssä taakse, jotta lyhyen säilyvyysajan omaavat tuotteet voidaan toimittaa ensin.

## <a name="using-shelf-life-in-master-planning"></a>Säilyvyysajan käyttäminen pääsuunnittelussa

Tässä osassa kerrotaan, miten pääsuunnittelu ehdottaa toimitusta nimikkeille, joilla on tietty säilyvyysaika.

Kun pääsuunnitelma suoritetaan, se luo ehdotetut suunnitellut tilaukset (tarjonta), jotka täyttävät kysynnän ja minimoivat viiveet. Jos suunnitelmaan kuuluu rajallisen säilyvyysajan omaavia nimikkeitä, suunnitelman laskelmat ovat monimutkaisia, koska suunnitelman on sekä minimoitava viiveet että käytettävä olemassa oleva tarjonta ennen sen vanhenemista. Suunnitelmassa on yritettävä käyttää lähinnä vanhenemispäivämäärää olevaa tarjontaa myöhemmin vanhenevan tarjonnan sijaan. Tämän vuoksi pääsuunnittelu pyrkii saavuttamaan seuraavat tavoitteet alla olevassa järjestyksessä:

1. viiveiden määrän minimoiminen
1. FEFO-tarjonnan määrän maksimoiminen
1. varaston täydennyksen minimoiminen.

Joissakin tapauksissa kahden ensimmäisen tavoitteen välillä voi olla ristiriita. Tällöin on valittava toimituksen viivästyminen tai myöhemmin vanhenevan tarjonnan käyttäminen aiemmin vanhenevan tarjonnan sijaan. Järjestelmä priorisoi viiveiden minimointia pian vanhentuvan tarjonnan käyttämisen sijaan, kun tämä ristiriita on ratkaistava pääsuunnittelun aikana. Yleensä tällainen ristiriita esiintyy viiveiden ja kauden mukaan määritetyn kattavuuden yhteydessä. Tämän vuoksi on suositeltavaa käyttää kattavuuskautta, joka on nimikkeen säilyvyysaikaa lyhyempi. Tällaista ristiriitaa ei yleensä esiinny muun tyyppisissä kattavuuksissa (kuten tarpeen mukaisessa kattavuudessa).

## <a name="set-up-shelf-life"></a>Säilyvyysajan määrittäminen

### <a name="configure-each-master-plan-to-consider-shelf-life"></a>Kunkin pääsuunnitelman määrittäminen säilyvyysajan ottamiseksi huomioon

Oletusarvoisesti pääsuunnitelmissa ei oteta huomioon säilyvyysaikaa. Seuraavien ohjeiden avulla voit ottaa käyttöön säilyvyysajan laskelmat jokaiselle laskelman vaativalle pääsuunnitelmalle.

1. Siirry kohtaan **Pääsuunnittelu \> Määritykset \> Suunnitelmat \> Pääsuunnitelmat**.
1. Valitse olemassa oleva suunnitelma luetteloruudussa tai luo uusi suunnitelma.
1. Määritä **Yleinen**-pikavälilehdessä **Käytä säilyvyysajan päivämääriä** -asetukseksi *Kyllä*.

### <a name="configure-tracking-dimension-groups-to-track-the-batch-dimension"></a>Seurantadimensioryhmien määrittäminen erädimension seuraamista varten

Nimikkeen säilyvyysaikaa voidaan seurata vain, jos nimikettä seurataan erädimensiossa. Toisin sanoen erän viite ja vaaditut päivämäärät on kirjattava vastaanoton tai valmistuksen yhteydessä sekä nimikkeen jokaisen varastotapahtuman kautta. Voit hallita tätä vaihtoehtoa määrittämällä pakollisen seurannan suorittamiseksi yhden seurantadimensioryhmän tai useita seurantadimensioryhmiä. Liitä sitten näille ryhmille tarvittavat nimikkeet.

Seuraavan menettelyn avulla voit määrittää seurantadimensioryhmän erädimension seurantaa varten.

1. Valitse **Tuotetietojen hallinta \> Määritys \> Dimensio- ja varianttiryhmät \> Seurantadimensioryhmät**.
1. Noudata seuraavia ohjeita:

    - Valitse toimintoruudussa **Uusi** luodaksesi uuden seurantadimensioryhmän. Syötä nimi ja kuvaus ja valitse toimintoruudussa **Tallenna**.
    - Valitse luetteloruudussa olemassa oleva seurantadimensioryhmä, jolle erädimensio määritetään.

1. Valitse **Seurantadimensio**-pikavälilehden **Eränumero**-rivillä **Aktiivinen**- ja **Varastotilanne**-sarakkeiden valintaruudut.

### <a name="set-up-shelf-life-for-a-product"></a>Tuotteen säilyvyysajan määrittäminen

Seuraavien ohjeiden avulla voit määrittää tuotteen säilyvyysajan.

1. Mene **Tuotetietojen hallinta \> Tuotteet \> Vapautetut tuotteet**.
1. Luo tai avaa tuote, jonka haluat määrittää.
1. Voit ottaa säilyvyysajan määritykset käyttöön määrittämällä **Yleiset**-pikavälilehdessä **Seurantadimensioryhmä**-kenttään seurantadimensioryhmän, joka on määritetty seuraamaan erädimensiota. Tämän kentän voi määrittää vain tuotteen ensimmäisellä luontikerralla. Olemassa olevien tuotteiden arvoa ei voi muuttaa.
1. Määritä **Varastonhallinta**-pikavälilehdellä seuraavat kentät:

    - **Suositeltava varastointiaika päivinä** – Määritä aika (päivinä), jonka aikana on tarkistettava, että tämän tuotteen erä kelpaa kulutettavaksi tai jälleenmyyntiin. Tämän kentän arvo lisätään erän *valmistuspäivämäärään* *suositeltavan varastointiajan* määrittämiseksi. Voit määrittää järjestelmän luomaan laatutilauksia, kun erä lähestyy suositeltavan varastointiajan päivämäärää.
    - **Varastointiaika päivinä** – Määritä päivien lukumäärä ennen kuin tämän tuotteen erä vanhenee. Tämä arvo lisätään *valmistuspäivämäärään*, jotta voidaan määrittää *vanhentumispäivä*. Erää pidetään käyttökelvottomana tämän päivän jälkeen.
    - **Parasta ennen -aika päivinä** – Määritä aika (päivinä), jonka jälkeen tämän tuotteen erä määritetään yhä myyntikelpoiseksi, mutta jotkin sen alkuperäisistä ominaisuuksista eivät enää ole voimassa. Tämä arvo lisätään *valmistuspäivämäärään*, jotta voidaan määrittää *parasta ennen -päivä*. Voit suorittaa raportteja määrittääksesi varaston, joka on ohittanut parasta ennen -päivän. 

### <a name="set-a-sellable-days-rule-for-each-customer"></a>Myyntipäivien säännön määrittäminen kullekin asiakkaalle

*Myyntipäivät*-toiminto varmistaa, että pian vanhenevan erän tuotteita ei lähetetä asiakkaille. Lisäksi se varmistaa, että kun tuotteet lähetetään asiakkaalle, tuotteella on yhä jäljellä riittävästi myyntipäiviä toimituksen jälkeen.

Myyntipäivätoimintoa voi käyttää, jos määritettynä on myyntipäivien määrä, joka koskee kaikkien asiakkaiden jokaista tuotetta (tai tuoteryhmää). Tämä prosessi on suoritettava manuaalisesti, koska sillä ei ole tietoyksikköä.

Seuraavien ohjeiden avulla voit määrittää myyntipäivät kaikkien asiakkaiden jokaiselle tuotteelle.

1. Valitse **Myynti ja markkinointi \> Asiakkaat \> Kaikki asiakkaat**.
1. Etsi ja valitse asiakas, jonka haluat määrittää.
1. Valitse toimintoruudun **Myynti**-välilehden **Määritys**-ryhmässä **Myynti \> Myyntipäivät**.
1. Ruudukko luetteloi **Asiakkaan myyntipäivät** -sivulla olemassa olevien myyntipäivien säännön jokaiselle tuotteelle tai tuoteryhmälle. Toimintoruudun painikkeiden avulla voit lisätä ruudukkoon rivejä tai muokata niitä tarvittaessa. Käytössä on **suodatin**, jonka avulla voit etsiä olemassa olevia rivejä.
1. Määritä kullekin riville seuraavat kentät:

    - **Nimikekoodi** – Valitse jokin seuraavista arvoista määrittääksesi käsiteltävän nimikkeiden käyttöalueen:

        - *Taulu* – Rivi koskee tiettyä nimikettä.
        - *Ryhmä* – Rivi koskee tiettyä nimikeryhmää.
        - *Kaikki* – Rivi koskee kaikkia nimikkeitä.

    - **Nimikesuhde** – Jos määrität **Nimikekoodi**-kentän arvoksi *Taulukko*, valitse tietty nimike. Jos määrität **Nimikekoodi**-kentän asetukseksi *Ryhmä*, valitse nimikeryhmä. Jos määrität **Nimikekoodi**-kentän arvoksi *Kaikki*, tämä kenttä ei ole käytettävissä.
    - **Myyntipäivät** – Syötä niiden päivien vähimmäismäärä, joiden aikana asiakkaan on myytävä vastaavat tuotteet ennen erän vanhenemista. Myyntipäivät perustuvat myyntitilauksen vastaavien tuotteiden pyydettyyn vastaanottopäivään (tai vahvistettuun vastaanottopäivään, jos se on määritetty).
    - *(Muut tuotedimensiot)* – Jos haluat rajoittaa rivin laajuutta, määritä tarvittaessa muita dimension arvoja (kuten **koko** ja **väri**). Voit määrittää, mitkä dimensiot näkyvät ruudukossa, valitsemalla toimintoruudussa **Näytä dimensiot**.

### <a name="set-up-all-relevant-products-so-that-they-are-fefo-date-controlled"></a>Määritä kaikki tarvittavat tuotteet niin, että ne ovat FEFO-päivämääräohjattuja

Myyntipäivät-toiminto toimii, jos kukin asiaankuuluva nimike kuulu nimikemalliryhmään, jossa **Päivämäärän mukaan ohjattu FEFO** -valintaruutu on valittuna.

Seuraavien ohjeiden avulla voit määrittää nimikemalliryhmän niin, että se tukee myyntipäivätoimintoa.

1. Siirry kohtaan **Varastonhallinta \> Asetukset \> Varasto \> Nimikemalliryhmät**.
1. Valitse olemassa oleva ryhmä luetteloruudusta tai luo uusi ryhmä valitsemalla toimintoruudussa **Uusi**.
1. Valitse **Varastokäytännöt**-pikavälilehdessä **Päivämäärän mukaan ohjattu FEFO** -valintaruutu.
1. Määritä ryhmän muut kentät tarpeen mukaan.

Seuraavien ohjeiden avulla voit tarkastella tuotteen nimikemalliryhmää tai määrittää sen.

1. Mene **Tuotetietojen hallinta \> Tuotteet \> Vapautetut tuotteet**.
1. Avaa tuote, jota haluat tarkastella tai muokata.
1. Määritä **Yleiset**-pikavälilehdessä **Nimikemalliryhmä**-kentän arvoksi ryhmä, jossa **Päivämäärän mukaan ohjattu FEFO** -valintaruutu on valittuna.

## <a name="example-1-simple-fefo-10-day-period-zero-days-of-lead-time"></a>Esimerkki 1: Yksinkertainen FEFO, 10 päivän jakso, läpimenoaika nolla päivää

Tässä esimerkissä on perusesimerkki säilyvyysajasta, jossa tarjontatilausten ja kysynnän välinen tarvekohdistus tehdään järjestelmän seuraavien tavoitteiden täyttämiseksi:

- viiveiden määrän minimoiminen
- FEFO-tarjonnan määrän maksimoiminen
- varaston täydennyksen minimoiminen.

Järjestelmällä on seuraavat nimikkeen ja pääsuunnitelman asetukset:

- **Kattavuuskoodi (täydennysstrategia):** Kausi 
- **Kattavuuskausi:** 10 päivää (sama kuin säilyvyysaika)
- **Säilyvyysaika:** 10 päivää
- **Myyntipäivät:** 0 päivää
- **Läpimenoaika:** 0 päivää
- **Negatiiviset päivät:** 0 päivää
- **Suunnitellun tilauksen tyyppi (nimikkeen tilauksen oletusmääritykset):** Ostotilaus

Järjestelmässä on nimikkeelle seuraavat myyntitilaukset:

- **MT1:** Määrä = 2, pyydetty toimituspäivä = tänään + 1 päivä
- **MT2:** Määrä = 1, pyydetty toimituspäivä = tänään + 4 päivää
- **MT3:** Määrä = 1, pyydetty toimituspäivä = tänään + 5 päivää

Kaikki nämä myyntitilaukset luovat nimikkeelle kysyntää.

Nimikkeelle on olemassa seuraava tarjonta:

- **Käytettävissä oleva varasto:** Määrä = 1, vanhentumispäivä = tänään + 5 päivää
- **Ostotilaus 1 (OT1):** Vastaanottopäivä = tänään + 2 päivää, määrä = 1, vanhentumispäivä = tänään + 4 päivää

Järjestelmä luo tarjontaluettelon, joka voi kattaa tämän kysynnän, ja lajittelee luettelon vanhentumispäivän mukaan (käyttämällä FEFO-menetelmää).

Pääsuunnittelu luo tarjonnan ja kysynnän välille vaaditun tarvekohdistuksen. Se luo myös vaaditun kysynnän tarjontaluettelon perusteella (käyttämällä FEFO-menetelmä) ja ottaa huomioon saatavuuspäivän.

- MT1 voidaan täyttää käyttämällä varastosaldoa. OT1:tä ei voida käyttää, koska OT1:n saatavuuspäivä on yhtä päivää myöhempi kuin MT1:n vaatima päivä. MT1 luo näin kysyntää yhdelle tavarayksikölle.
- MT2 voidaan kattaa OT1:n avulla, koska OT1 saapuu pyydettynä aikana ja vanhenemispäivä on yhä voimassa. Tämän vuoksi OT1 kattaa täysin MT2:n vaatimuksen.
- MT3:a ei kateta, koska resurssit eivät ole saatavissa. MT3 luo näin ollen kysyntää yhdelle tavarayksikölle.

Järjestelmän on luotava seuraava suunniteltu ostotilaus, jotta kaikki jäljellä olevat tarpeet tulevat katetuiksi:

- **SOT1:** Vastaanottopäivä = tänään, määrä = 2, vanhenemispäivä = tänään + 10 päivää

Seuraavassa taulukossa on tulosten yhteenveto.

| Kysyntä | Tarvekohdistus |
|---|---|
| **MT1:** Toimituspäivä = tänään + 1 päivä, määrä = 2 | <p>**Käytettävissä:** Määrä = 1, vanhentumispäivä = tänään + 5 päivää</p><p>**SOT1:** Vastaanottopäivä = tänään, määrä = 1, vanhenemispäivä = tänään + 10 päivää</p> |
| **MT2:** Toimituspäivä = tänään + 4 päivää, määrä = 1 | **OT1:** Vastaanottopäivä = tänään + 2 päivää, 1 määrä, vanhenemispäivä = tänään + 4 päivää |
| **OT3:** Toimituspäivä = tänään + 5 päivää, määrä = 1 | **SOT1:** Vastaanottopäivä = tänään, määrä = 2, vanhenemispäivä = tänään + 10 päivää |

Seuraava kuva näyttää tämän esimerkin aikajanan.

![Esimerkki 1: Yksinkertainen FEFO, 10 päivän jakso, läpimenoaika nolla päivää.](media/fefo-example-1.png "Esimerkki 1: Yksinkertainen FEFO, 10 päivän jakso, läpimenoaika nolla päivää")

## <a name="example-2-simple-fefo-requirement-three-days-of-lead-time"></a>Esimerkki 2: Yksinkertainen FEFO, tarve, läpimenoaika kolme päivää

Tässä esimerkissä kerrotaan, miten järjestelmän yritys minimoida viiveitä voi joskus aiheuttaa ylitilaamista.

Järjestelmällä on seuraavat nimikkeen ja pääsuunnitelman asetukset:

- **Kattavuuskoodi (täydennysstrategia):** Tarve
- **Säilyvyysaika:** 10 päivää
- **Myyntipäivät:** 0 päivää
- **Läpimenoaika:** Muodostettu seuraavien toimittajien kauppasopimusten perusteella:

    - **Kauppasopimus 1:** Jos määrä = 1, läpimenoaika = 4
    - **Kauppasopimus 2:** Jos määrä = 2, läpimenoaika = 3

- **Negatiiviset päivät:** 0 päivää
- **Suunnitellun tilauksen tyyppi (nimikkeen tilauksen oletusmääritykset):** Ostotilaus

Seuraava myyntitilaus on olemassa järjestelmässä:

- **MT1:** Määrä = 2, pyydetty toimituspäivä = tänään + 3 päivää

Tämä kysyntä katetaan olemassa olevalla tarjonnalla ja vahvistetulla ostotilauksella seuraavasti:

- **Käytettävissä oleva varasto:** Saatavissa = tänään, määrä = 1, vanhentumispäivä = tänään + 2 päivää
- **OT1:** Vastaanottopäivä = tänään + 3 päivää, määrä = 1, vanhenemispäivä = tänään + 4 päivää

Käytettävissä oleva varasto ei voi täyttää MT1:tä, koska varaston vanhenemispäivä on aiempi kuin lähetyspäivä. OT1 voi kattaa MT1:n tarpeen vain, jos määrä on 1. MT1 luo näin kysyntää yhdelle tavarayksikölle. Järjestelmä kattaa tämän tarpeen luomalla suunnitellun ostotilauksen (SOT1).

Järjestelmässä on kaksi kauppasopimuksia (yksi, jossa määrä = 1, läpimenoaika = 4 päivää ja yksi, jossa määrä = 2, läpimenoaika = 3 päivää). Järjestelmä yrittää näin minimoida viiveitä luomalla suunnitellun ostotilauksen (SOT1), joka vastaa toista kauppasopimusta. Tuloksena on ylitoimitus (määrä = 2, vanhenemispäivä = tänään + 10 päivää).

Seuraavassa taulukossa on tulosten yhteenveto.

| Kysyntä | Tarvekohdistus |
|---|---|
| **MT1:** Toimituspäivä = tänään + 3 päivää, määrä = 2 | <p>**OT1:** Vastaanottopäivä = tänään + 3 päivää, määrä = 1, vanhenemispäivä = tänään + 4 päivää</p><p>**SOT1:** Vastaanottopäivä = tänään + 3 päivää, määrä = 1, vanhenemispäivä = tänään + 10 päivää</p> |

Seuraava kuva näyttää tämän esimerkin aikajanan.

![Esimerkki 2: Yksinkertainen FEFO, tarve, läpimenoaika kolme päivää.](media/fefo-example-2.png "Esimerkki 2: Yksinkertainen FEFO, tarve, läpimenoaika kolme päivää")

## <a name="example-3-simple-fefo-requirement-three-days-of-lead-time-five-sellable-days"></a>Esimerkki 3: Yksinkertainen FEFO, tarve, läpimenoaika kolme päivää, viisi myyntipäivää

Tässä esimerkissä kerrotaan, miten säilyvyysaika toimii, kun nimikkeelle lisätään myyntipäiviä.

Järjestelmällä on seuraavat nimikkeen ja pääsuunnitelman asetukset:

- **Kattavuuskoodi (täydennysstrategia):** Tarve
- **Säilyvyysaika:** 10 päivää
- **Myyntipäivät:** 5 päivää
- **Läpimenoaika:** 5 päivää
- **Negatiiviset päivät:** 0 päivää
- **Suunnitellun tilauksen tyyppi (nimikkeen tilauksen oletusmääritykset):** Ostotilaus

Seuraavat myyntitilaukset ovat olemassa järjestelmässä:

- **MT1:** Määrä = 2, pyydetty toimituspäivä = tänään + 2 päivää
- **MT2:** Määrä = 1, pyydetty toimituspäivä = tänään + 3 päivää
- **MT3:** Määrä = 1, pyydetty toimituspäivä = tänään + 5 päivää

Tämä kysyntä voidaan kattaa olemassa olevalla tarjonnalla ja vahvistetulla ostotilauksella seuraavasti:

- **Käytettävissä oleva varasto:** Saatavissa = tänään, määrä = 1, vanhentumispäivä = tänään + 6 päivää
- **OT1:** Vastaanottopäivä = tänään + 2 päivää, määrä = 3, vanhenemispäivä = tänään + 10 päivää

Järjestelmä luo tarvekohdistuksen ehdokkaiden luettelon, joka perustuu toimitusluetteloon (FEFO) ja saatavuuspäiviin. Käytettävissä oleva varasto ei voi siis täyttää MT1:tä, koska varasto vanhenee ennen asiakkaan vaatimien myyntipäivien päättymistä (pyydetty vastaanottopäivä + 5 päivää). OT1 voi kattaa MT1:n tarpeen kahdella yksiköllä ja MT2:n tarpeen yhdellä yksiköllä. Näin vain MT3:lla on kattamatonta yhden tavarayksikön kysyntää. Järjestelmä kattaa tämän tarpeen luomalla seuraavan suunnitellun ostotilauksen:

- **SOT1:** Vastaanottopäivä = tänään + 5 päivää, määrä = 1, vanhenemispäivä = tänään + 10 päivää

Seuraavassa taulukossa on tulosten yhteenveto.

| Kysyntä | Tarvekohdistus |
|---|---|
| **MT1:** Toimituspäivä = tänään + 2 päivää, määrä = 2 | **OT1:** Vastaanottopäivä = tänään + 2 päivää, määrä = 2, vanhenemispäivä = tänään + 10 päivää |
| **MT2:** Toimituspäivä = tänään + 3 päivää, määrä = 1 | **OT1:** Vastaanottopäivä = tänään + 2 päivää, määrä = 1, vanhenemispäivä = tänään + 10 päivää |
| **OT3:** Toimituspäivä = tänään + 5 päivää, määrä = 1 | **SOT1:** Vastaanottopäivä = tänään + 5 päivää, määrä = 1, vanhenemispäivä = tänään + 10 päivää |

Seuraava kuva näyttää tämän esimerkin aikajanan.

![Esimerkki 3: Yksinkertainen FEFO, tarve, läpimenoaika kolme päivää, viisi myyntipäivää.](media/fefo-example-3.png "Esimerkki 3: Yksinkertainen FEFO, tarve, läpimenoaika kolme päivää, viisi myyntipäivää")

## <a name="example-4-simple-fefo-period-lead-time-depends-on-the-quantity"></a>Esimerkki 4: Yksinkertainen FEFO, kausi, läpimenoaika riippuu määrästä

Tässä esimerkissä kerrotaan, miten järjestelmän yritys minimoida viiveitä voi joskus aiheuttaa ylitilaamista.

Järjestelmällä on seuraavat nimikkeen ja pääsuunnitelman asetukset:

- **Kattavuuskoodi (täydennysstrategia):** Kausi
- **Kattavuuskausi:** 10 päivää (sama kuin säilyvyysaika)
- **Säilyvyysaika:** 10 päivää
- **Myyntipäivät:** 0 päivää
- **Läpimenoaika:** Muodostettu seuraavien toimittajien kauppasopimusten perusteella:

    - **Kauppasopimus 1:** Jos määrä = 1, läpimenoaika = 5
    - **Kauppasopimus 2:** Jos määrä = 2, läpimenoaika = 0

- **Negatiiviset päivät:** 0 päivää
- **Suunnitellun tilauksen tyyppi (nimikkeen tilauksen oletusmääritykset):** Ostotilaus

Seuraavat myyntitilaukset ovat olemassa järjestelmässä:

- **MT1:** Määrä = 1, pyydetty toimituspäivä = tänään
- **MT2:** Määrä = 1, pyydetty toimituspäivä = tänään + 6 päivää

Olemassa oleva tarjonta voi kattaa tämän kysynnän osittain seuraavissa vahvistetuissa ostotilauksissa:

- **OT1:** Vastaanottopäivä = tänään + 1 päivä, määrä = 1, vanhenemispäivä = tänään + 2 päivää
- **OT2:** Vastaanottopäivä = tänään + 3 päivää, määrä = 1, vanhenemispäivä = tänään + 7 päivää

Järjestelmässä on kaksi kauppasopimuksia (yksi, jossa määrä = 1, läpimenoaika = 5 päivää ja yksi, jossa määrä = 2, läpimenoaika = 0 päivää). Järjestelmä yrittää näin minimoida viiveen luomalla seuraavan suunnitellun ostotilauksen, joka vastaa toista kauppasopimusta:

- **SOT1:** Vastaanottopäivä = tänään, määrä = 2, vanhenemispäivä = tänään + 10 päivää

MT1 katetaan yhdellä SOT1:n yksiköllä. MT1 katetaan OT2:n avulla, koska OT2 vanhenee aiemmin kuin SOT1.

Seuraavassa taulukossa on tulosten yhteenveto.

| Kysyntä | Tarvekohdistus |
|---|---|
| **MT1:** Toimituspäivä = tänään, määrä = 1 | **SOT1:** Vastaanottopäivä = tänään, määrä = 1, vanhenemispäivä = tänään + 10 päivää |
| **MT2:** Toimituspäivä = tänään + 6 päivää, määrä = 1 | **OT2:** Vastaanottopäivä = tänään + 3 päivää, määrä = 1, vanhenemispäivä = tänään + 7 päivää |

> [!NOTE]
> OT1:tä ei käytetä, koska se saapuu liian myöhään MT1:lle ja vanhenee ennen kuin MT2 toimitetaan. SOT1:lla on yhden yksikön suuruinen ylitilaus, eikä läpimenoaika voi olla 0 (nolla) kauppasopimus 2:lle.

Seuraava kuva näyttää tämän esimerkin aikajanan.

![Esimerkki 4: Yksinkertainen FEFO, kausi, läpimenoaika riippuu määrästä.](media/fefo-example-4.png "Esimerkki 4: Yksinkertainen FEFO, kausi, läpimenoaika riippuu määrästä")

## <a name="example-5-simple-fefo-requirement-10-negative-days"></a>Esimerkki 5: Yksinkertainen FEFO, tarve, 10 negatiivista päivää

<!-- KFM: This is more of a negative days example than a shelf life example. We should point out more explicitly how shelf life affects this situation (or maybe otherwise remove this example). -->

Tässä esimerkissä kerrotaan, miten säilyvyysaika toimii, kun nimikkeelle lisätään suuri määrä negatiivisia päiviä. Negatiiviset päivät osoittaa niiden päivien määrän, jonka olet valmis odottamaan ennen sellaisen nimikkeen täydennyksen tilaamista, jolla on negatiivinen varasto. Järjestelmä luo tarjonnan vasta sitten, kun negatiivisten päivien määrä ylitetään.

Järjestelmällä on seuraavat nimikkeen ja pääsuunnitelman asetukset:

- **Kattavuuskoodi (täydennysstrategia):** Tarve
- **Läpimenoaika:** 0 päivää
- **Negatiiviset päivät:** 10 päivää
- **Suunnitellun tilauksen tyyppi (nimikkeen tilauksen oletusmääritykset):** Ostotilaus

Seuraava myyntitilaus on olemassa järjestelmässä:

- **MT1:** Määrä = 1, pyydetty toimituspäivä = tänään

Olemassa oleva tarjonta voi kattaa tämän kysynnän seuraavassa vahvistetussa ostotilauksessa:

- **OT1:** Vastaanottopäivä = tänään + 3 päivää, määrä = 1, vanhenemispäivä = tänään + 5 päivää

Koska järjestelmä on määritetty sallimaan 10 negatiivista päivää, se kattaa MT1:n kysynnän OT1:n avulla, vaikka tuloksena on kolmen päivän viive, koska OT1 luo negatiivisen varaston OT1:n saapumiseen asti. Suunniteltua ostotilausta ei luoda, vaikka läpimenoaika on 0 (nolla) ja suunnitellun ostotilauksen luominen vähentäisi viiveitä.

Seuraavassa taulukossa on tulosten yhteenveto.

| Kysyntä | Tarvekohdistus |
|---|---|
| **MT1:** Toimituspäivä = tänään, määrä = 1 | **OT1:** Vastaanottopäivä = tänään + 3 päivää, määrä = 1, vanhenemispäivä = tänään + 5 päivää |

Seuraava kuva näyttää tämän esimerkin aikajanan.

![Esimerkki 5: Yksinkertainen FEFO, tarve, 10 negatiivista päivää.](media/fefo-example-5.png "Esimerkki 5: Yksinkertainen FEFO, tarve, 10 negatiivista päivää")

## <a name="example-6-simple-fefo-requirement-five-negative-days"></a>Esimerkki 6: Yksinkertainen FEFO, tarve, viisi negatiivista päivää

Tässä esimerkissä kerrotaan, miten säilyvyysaika toimii, kun nimikkeelle lisättyjen negatiivisten päivien määrä on pienempi kuin sen säilyvyysaika.

Järjestelmällä on seuraavat nimikkeen ja pääsuunnitelman asetukset:

- **Kattavuuskoodi (täydennysstrategia):** Tarve
- **Myyntipäivät:** 0 päivää
- **Läpimenoaika:** 0 päivää
- **Negatiiviset päivät:** 5 päivää
- **Suunnitellun tilauksen tyyppi (nimikkeen tilauksen oletusmääritykset):** Ostotilaus

Seuraava myyntitilaus on olemassa järjestelmässä:

- **MT1:** Määrä = 2, pyydetty toimituspäivä = tänään

Olemassa oleva tarjonta voi kattaa tämän kysynnän seuraavassa vahvistetuissa ostotilauksissa:

- **PO1:** Vastaanottopäivä = tänään, määrä = 1, vanhenemispäivä = tänään + 1 päivä
- **OT2:** Vastaanottopäivä = tänään + 2 päivää, määrä = 1, vanhenemispäivä = tänään + 3 päivää

Järjestelmän on kuitenkin noudatettava rajoitusta, jonka mukaan lähetetyt nimikkeet eivät voi vanhentua lähetyksen aikana. MT1:llä ei siis voi olla käytössä sekä OT1 että OT2, koska OT1 vanhenee ennen kuin OT2 saapuu. Järjestelmä luo seuraavan suunnitellun ostotilauksen, jotta MT1:n kysynnän kattaminen voidaan tehdä loppuun:

- **SOT1:** Vastaanottopäivä = tänään, määrä = 1, vanhenemispäivä = tänään + 10 päivää

Järjestelmä voi hyödyntää viittä negatiivista päivää ja kattaa MT1:n OT2:n ja SOT1:n avulla. Tämä menetelmä aiheuttaa kuitenkin toimituksen viivästymisen siihen asti, kunnes OT2 saapuu, ja OT1 vanhenee sillä välin. Tämän vuoksi järjestelmä kattaa OT1:n SOT1:n ja OT1:n avulla.

Seuraavassa taulukossa on tulosten yhteenveto.

| Kysyntä | Tarvekohdistus |
|---|---|
| **MT1:** Toimituspäivä = tänään, määrä = 2 | <p>**PO1:** Vastaanottopäivä = tänään, määrä = 1, vanhenemispäivä = tänään + 1 päivä</p><p>**SOT1:** Vastaanottopäivä = tänään, määrä = 1, vanhenemispäivä = tänään + 10 päivää</p> |

Seuraava kuva näyttää tämän esimerkin aikajanan.

![Esimerkki 6: Yksinkertainen FEFO, tarve, viisi negatiivista päivää.](media/fefo-example-6.png "Esimerkki 6: Yksinkertainen FEFO, tarve, viisi negatiivista päivää")
