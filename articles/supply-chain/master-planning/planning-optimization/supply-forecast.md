---
title: Pääsuunnittelu ja tarjontaennusteet
description: Tässä artikkelissa kerrotaan, miten tarjontaennusteet otetaan huomioon pääsuunnittelun aikana.
author: t-benebo
ms.date: 09/21/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2022-09-21
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: dc83d10851958ec67166cb7e40cfd84dceae6651
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/18/2022
ms.locfileid: "9690077"
---
# <a name="master-planning-with-supply-forecasts"></a>Pääsuunnittelu ja tarjontaennusteet

[!include [banner](../../includes/banner.md)]

Tarjontaennusteiden avulla voit määrittää tarjonnan, jota odotat tarvittavan tietyn tulevan kauden aikana. Yleensä arvion perustana käytetään edellisen vuoden myyntihistoriaa, jonka jälkeen ennustetta käytetään budjetoinnissa. Voit myös määrittää pääsuunnitelmat käyttämään ennusteita suunnittelun aikana.

## <a name="set-up-a-master-plan-to-consider-supply-forecasts"></a>Pääsuunnittelun määrittäminen käyttämään tarjontaennusteita

Voit määrittää, käyttääkö pääsuunnitelma ennusteita suorituksen aikana. Seuraavien ohjeiden avulla voit määrittää kunkin suunnitelman ennustevaihtoehdot.

1. Siirry kohtaan **Pääsuunnittelu \> Määritykset \> Suunnitelmat \> Pääsuunnitelmat**.
1. Valitse aiemmin luotu pääsuunnitelma luetteloruudusta tai luo uusi valitsemalla toimintoruudusta **Uusi**.
1. Valitse **Yleiset**-pikavälilehdellä seuraavat lisäkentät:

    - **Ennustemalli** – Valitse malli, joka sisältää pääsuunnitelmassa käytettävän tarjonta- ja/tai kysyntäennusteen.
    - **Sisällytä tarjontaennuste** – Määritä vaihtoehdoksi *Kyllä*, jos pääsuunnitelman tulee ottaa huomioon tarjontaennuste.
    - **Sisällytä kysyntäennuste** – Määritä vaihtoehdoksi *Kyllä*, jos pääsuunnitelman tulee ottaa huomioon kysyntäennuste. Vaikka tämä asetus ei riipu **Sisällytä tarjontaennuste** -asetuksesta , jotkin sivun muut asetukset käyttävät sekä tarjonta- että kysyntäennusteita. Lisätietoja suunnittelusta, jossa otetaan huomioon kysyntäennusteet, on kohdassa [Pääsuunnittelu ja kysyntäennusteet](demand-forecast.md).
    - **Ennustevaatimusten vähentämiseen käytetty menetelmä** – Valitse menetelmä, jolla ennustevaatimuksia vähennetään pääsuunnittelun aikana seuraavasti:

        - *Ei mitään*: Ennustetarpeita ei vähennetä pääsuunnittelun aikana.
        - *Prosentti - vähennysavain* – Ennustetarpeita vähennetään vähennysavaimen määrittämien prosenttien ja ajanjaksojen mukaan.
        - *Tapahtumat - vähennysavain* – Ennustetarpeita vähennetään vähennysavaimen määrittämien ajanjaksojen aikaisten tapahtumien mukaan.
        - *Tapahtumat – dynaaminen kausi* – Ennustetarpeita vähennetään dynaamisen kauden aikana tapahtuvien tilaustapahtumien mukaan. Dynaaminen kausi kattaa nykyiset ennustepäivämäärät ja päättyy seuraavan ennusteen alkaessa. *Tapahtumat – dynaaminen kausi* -menetelmä ei käytä eikä vaadi vähennysavainta. Kun käytät sitä, seuraavat ehdot ovat käytössä:

            - Jos ennuste vähenee kokonaan, nykyisen ennusteen ennustetarpeiksi tulee nolla.
            - Jos tulevaa ennustetta ei ole, vähennetään edellisen syötetyn ennusteen ennustetarpeita.
            - Ennusteen vähennyslaskentaan sisällytetään aikarajat.
            - Ennusteen vähennyslaskentaan sisällytetään positiiviset päivät.
            - Jos toteutuneet tilaustapahtumat ylittävät ennustetarpeet, jäljelle jääviä tapahtumia ei siirretä seuraavalle ennustekaudelle.

        > [!NOTE]
        > **Ennustevaatimusten vähentämiseen käytetty menetelmä** -asetusta käytetään myös kysyntäennusteissa, jos olet ottanut ne käyttöön pääsuunnitelmassa. Asetus vaikuttaa niihin samalla tavalla. Lisätietoja on kohdassa [Pääsuunnittelu ja kysyntäennusteet](demand-forecast.md).

## <a name="set-reduction-options-for-coverage-groups"></a>Kattavuusryhmien vähennysasetusten määrittäminen

Jos haluat määrittää asetukset, jotka määrittävät, miten kattavuusryhmä vähentää ennustevaatimuksia tapahtumaperusteisia vähennyksiä käyttäjissä pääsuunnitelmissa, noudata alla olevia ohjeita.

1. Valitse **Pääsuunnittelu \> Määritys \> Suunnitelmat \> Kattavuusryhmät**.
1. Valitse luetteloruudussa olemassa oleva kattavuusryhmä tai luo uusi valitsemalla toimintoruudussa **Uusi**.
1. Määritä **Muut**-pikavälilehden **Ennusteen vähennysperuste** -kentässä, miten tarjontaennustevaatimukset on vähennettävä kattavuusryhmän nimikkeissä pääsuunnitelmalle, jossa **Ennustevaatimusten vähentämiseen käytetty menetelmä** -kentän arvoksi on määritetty *Tapahtumat – vähennysavain* tai *Tapahtumat – dynaaminen kausi*. Valitse jokin seuraavista:

    - *Kaikki tapahtumat* – kaikki tapahtumat vähentävät ennustetta.
    - *Tilaukset* – vain myyntitilaukset, joilla on sama tyyppi, vähentävät ennustetta.

    Esimerkiksi nimikkeen oletustilausasetukset ilmaisevat, että tilaus on tuotettava. Tarjontaennusteen rivin tarjontaennusteen rivin määrä on 50. Olemassa olevan ostotilauksen määrä on 20. Jos **Ennusteen vähennysperuste** -kentän arvoksi on määritetty *Tilaukset*, luodaan suunniteltu tuotantotilaus, jonka määrä on 50. Jos sen arvoksi määritetään *Kaikki tapahtumat*, suunnitellun tuotantotilauksen määrää vähennetään arvoon 30.

    Tämä asetus koskee myös kysyntäennusteen vähennystä. Lisätietoja on kohdassa [Pääsuunnittelu ja kysyntäennusteet](demand-forecast.md).

## <a name="enter-a-supply-forecast-for-a-product"></a>Tarjontaennusteen antaminen tuotteelle

Jos haluat antaa tuotteelle tarjontaennusteen, noudata alla olevia ohjeita.

1. Mene **Tuotetietojen hallinta \> Tuotteet \> Vapautetut tuotteet**.
1. Valitse tuote, jolle haluat antaa ennusteen.
1. Valitse toimintoruudun **Suunnitelma**-välilehdessä **Tarjontaennuste**.
1. Valitse toimintoruudun **Tarjontaennuste**-sivulla **Uusi**, jos haluat lisätä ruudukkoon ennusteen.
1. Anna tiedot uudelle riville vaaditulla tavalla ennusteen määrittämiseksi.

## <a name="plan-for-an-item-with-supply-forecast-lines"></a>Suunnitelma nimikkeelle, jolla on tarjontaennusterivejä

Kun suoritat pääsuunnitelman, joka sisältää tarjontanimikkeen sisältävän nimikkeen, järjestelmä luo ostotilauksen annetuille tarjontariveille. Nimikkeen tilauksen oletusasetuksia noudatetaan. Jos nämä tilauksen oletusasetukset määrittävät **tilauksen oletustyypin** arvon *ostotilaukselle*, eikä toimittajatiliä ole määritetty tarjontaennusterivillä, järjestelmä käyttää nimikkeessä oletustoimittajaa.

## <a name="check-whether-a-planned-order-is-a-supply-forecast-order"></a>Tarkistetaan, onko suunniteltu tilaus tarjontaennustetilaus

Alla olevien ohjeiden avulla saat tietää, onko suunniteltu tilaus luotu tarjontaennusteen tuloksena.

1. Valitse **Pääsuunnittelu \> Pääsuunnittelu \> Suunnitellut tilaukset**.
1. Avaa suunniteltu ostotilaus, jonka haluat tarkastaa.
1. Katso **Yleinen**-pikavälilehden **Tila**-kentän arvo. Jos tilaus on luotu kattamaan tarjontaennuste, kentän arvon tulisi olla *Kyllä*.

## <a name="examples-of-master-planning-with-supply-forecasts"></a>Pääsuunnittelun ja tarjontaennusteiden esimerkit

Tässä osassa on useita esimerkkejä, jotka näyttävät, miten tarjontaennusteet vaikuttavat pääsuunnitteluun.

### <a name="example-1-supply-forecast-for-an-item"></a>Esimerkki 1: Nimikkeen tarjontaennuste

Nimikkeen tilauksen oletustyyppi on *ostotilaus* ja oletustoimittaja on *US-002*. Sillä on seuraava tarjontaennusterivi.

| Malli    | Päivämäärä     | Toimittajanro | Toimittajaryhmä | Määrä | Yksikkö | Sivusto | Varasto |
|----------|----------|----------------|--------------|----------|------|------|-----------|
| CurrentF | 10.10.22 |                |              | 35       | kpl   | 1    | 11        |

Kun pääsuunnittelu suoritetaan, luodaan ostotilaus *35 kpl* toimittajalta *US-002*.

### <a name="example-2-several-supply-forecast-lines-with-and-without-a-vendor"></a>Esimerkki 2: Useita tarjontaennusterivejä toimittajan kanssa ja ilman toimittajaa

Nimikkeen tilauksen oletustyyppi on *ostotilaus* ja oletustoimittaja on *US-002*. Sillä on seuraavat tarjontaennusterivit.

| Malli    | Päivämäärä     | Toimittajanro | Toimittajaryhmä | Määrä | Yksikkö | Sivusto | Varasto |
|----------|----------|----------------|--------------|----------|------|------|-----------|
| CurrentF | 10.10.22 |                |              | 35       | kpl   | 1    | 11        |
| CurrentF | 10.10.22 | US-101         |              | 25       | kpl   | 1    | 11        |

Tässä tapauksessa järjestelmä käsittelee yleisenä ennusteena riviä, joka ei määritä toimittajaa. Oletuksena on, että rivi, jolla määritetään toimittaja, on vähennettävä yleisestä ennusteesta. Näin ollen pääsuunnittelu luo nimikkeelle seuraavat suunnitellut ostotilaukset:

- Suunniteltu ostotilaus määrälle *25 kpl* toimittajalta *US-101* (Toimittaja ja määrä määritetään ennusterivillä.)
- Luotiin ostotilaus määrälle *10 kpl* toimittajalta *US-002* (Koska toisella ennusterivillä ei määritetty toimittajaa, käytettiin oletustoimittajaa. Tämän ennusterivin määrää vähennetään toimittajakohtaisen ennusterivin määrällä.)

### <a name="example-3-plans-that-use-the-transactions---dynamic-period-reduction-method-in-a-single-forecast-period"></a>Esimerkki 3: Suunnitelmat, joissa käytetään Tapahtumat – dynaaminen kausi -vähennysmenetelmää yksittäisellä ennustekaudella

Jos pääsuunnitelmassa on käytössä *Tapahtumat – dynaaminen kausi* ennusteen vähennysmenetelmänä, pääsuunnittelu vähentää ennustemäärät, jos olemassa on tapahtumia, jotka vastaavat tarjonnan ominaisuuksia.

Tässä esimerkissä nimikkeen tilauksen oletustyyppi on *Ostotilaus*. Sillä on seuraava tarjontaennusterivi.

| Malli    | Päivämäärä     | Toimittajanro | Toimittajaryhmä | Määrä | Yksikkö | Sivusto | Varasto |
|----------|----------|----------------|--------------|----------|------|------|-----------|
| CurrentF | 10.10.22 | US-101         |              | 25       | kpl   | 1    | 11        |

Koska olemassa on vain yksi tarjontaennusterivi, olemassa on vain yksi ennustekausi.

Suoritettaessa pääsuunnitelmaa, joka on määritetty käyttämään *Tapahtumat – dynaaminen kausi* -vähennysmenetelmää, saattaa tapahtua jokin seuraavista vaihtoehdoista:

- Jos toimittajalla *US-101* ja määrällä *10 kpl* on ostotilaus ja **Tarjontaennuste**-kentän arvoksi on määritetty *Kyllä*, pääsuunnittelussa luodaan uusi suunniteltu ostotilaus jäljellä olevalle määrälle, joka on *10 kpl*. Ennusteriviä vähennetään, koska toimittaja vastaa aiemmin luotua ostotilausta.
- Jos toimittajalla *US-102*, sijainnilla *1*, varastolla *11* ja määrällä *10 kpl* on ostotilaus ja **Tarjontaennuste**-kentän arvoksi on määritetty *Kyllä*, pääsuunnittelu luo uuden suunnitellun ostotilauksen täydelle määrälle, joka on *25 kpl*. Ennusteriviä ei voi vähentää, koska sillä on eri toimittaja kuin olemassa olevalla ostotilauksella.

> [!NOTE]
> Tämä tilanne voi tapahtua suunnitelluille ostotilauksille, koska niille on liitetty toimittaja. Siirto- ja tuotantotilausten tarjontaennustesummat kuitenkin vähennetään aina olemassa olevien tilausten mukaan, koska toimittajaa ei määritetä näille tilauksille.

### <a name="example-4-plans-that-use-the-transactions---dynamic-period-reduction-method-over-several-forecast-periods"></a>Esimerkki 4: Suunnitelmat, joissa käytetään Tapahtumat – dynaaminen kausi -vähennysmenetelmää useilla ennustekausilla

Nimikkeen tilauksen oletustyyppi on *Ostotilaus*. Sillä on seuraavat tarjontaennusterivit.

| Malli    | Päivämäärä     | Toimittajanro | Toimittajaryhmä | Määrä | Yksikkö | Sivusto | Varasto |
|----------|----------|----------------|--------------|----------|------|------|-----------|
| CurrentF | 10.10.22 | US-101         |              | 25       | kpl   | 1    | 11        |
| CurrentF | 15.10.22 | US-101         |              | 25       | kpl   | 1    | 11        |

Tässä esimerkissä on kaksi ennusteriviä, joilla on eri päivämäärät. Päivämäärät siis muodostavat ennustekausien rajat. Ensimmäinen kausi on lokakuun 10. päivästä lokakuun 14. päivään (10.10.–14.10.2022). Toinen kausi on lokakuun 15. päivästä (15.10.22) eteenpäin.

Toimittajan *US-101* ostotilaus, jonka määrä on *10 kpl* ja päivämäärä *12.10.22* (12. lokakuuta 2022). Suoritettaessa pääsuunnitelmaa, joka on määritetty käyttämään *Tapahtumat – dynaaminen kausi* -vähennysmenetelmää, luodaan seuraavat tilaukset:

- Suunniteltu tilaus, jonka määrä on *15 kpl* ja päivämäärä *10.10.22* (Määrää vähennetään sen olemassa olevan ostotilauksen mukaan, jonka päivämäärä on samalla ennustekaudella.)
- Suunniteltu tilaus, jonka määrä on *25 kpl* ja päivämäärä *15.10.22* (Määrä on ennusteen koko määrä.)

### <a name="example-5-plans-that-use-no-reduction"></a>Esimerkki 5: Suunnitelmat, joissa ei käytetä vähennystä

Kun suoritat suunnitelman, jossa ennustevähennysmenetelmä on *Ei mitään*, pääsuunnittelu luo aina suunnitellun tarjonnan kaikille tarjontaennusteriveille. Kun tämä suunniteltu tarjonta on hyväksytty, se vähentää tulevia suunniteltuja tilauksia. Ostotilaukset eivät kuitenkaan vähennä tarjontaennusterivejä.

Tässä esimerkissä nimikkeen tilauksen oletustyyppi on *Ostotilaus*. Sillä on seuraava tarjontaennusterivi.

| Malli    | Päivämäärä     | Toimittajanro | Toimittajaryhmä | Määrä | Yksikkö | Sivusto | Varasto |
|----------|----------|----------------|--------------|----------|------|------|-----------|
| CurrentF | 10.10.22 | US-101         |              | 25       | kpl   | 1    | 11        |

Järjestelmässä on toimittajan *US-101* ostotilaus sijainnilla *1*, varastolla *11*, määrällä *25 kpl* ja päivämäärällä *10.10.22*. 

Kun suoritetaan pääsuunnitelma, jonka vähennysmenetelmän arvoksi on määritetty *Ei mitään*, luodaan ostotilaus toimittajalle *US-101*, sijainnille *1*, varastolle *11*, määrälle *25 kpl* ja päivämäärälle *10.10.22*. Toisin sanoen olemassa olevaa ostotilausta ei vähennetä, koska ennusteen vähennysmenetelmä on *Ei mitään*.

Voit nyt muokata suunniteltua ostotilausta, joka luotiin edellisen suunnittelun suorituksen jälkeen ja jonka määräksi muutettiin *15 kpl*. Hyväksy ostotilaus tämän jälkeen. Kun pääsuunnitelma suoritetaan seuraavan kerran, luodaan ostotilaus toimittajalle *US-101*, sijainnille *1*, varastolle *11*, määrälle *10 kpl* ja päivämäärälle *10.10.22*. Nyt määrää vähennetään niin, että se vastaa aiemman edellisen suunnittelun suorituksen olemassa olevan, hyväksytyn tilauksen määrää.

## <a name="differences-between-planning-optimization-and-the-built-in-planning-engine"></a>Suunnittelun optimoinnin ja sisäisen pääsuunnittelumoduulin erot

Tarjontaennusteet toimivat hieman eri tavalla riippuen käyttämästäsi suunnittelumoduulista (sisäinen pääsuunnittelu vai suunnittelun optimointi). Tässä osassa esitellään erot.

### <a name="vendor-groups"></a>Toimittajaryhmät

Kun lisäät ennusterivin, voit määrittää toimittajan ja toimittajaryhmän. Luodut suunnitellut tilaukset ryhmitellään sisäisessä suunnittelumoduulissa toimittajan ja toimittajaryhmän arvojen yhdistelmän mukaan. Suunnittelun optimoinnissa suunnitellut tilaukset ryhmitellään toimittajan mukaan.

Alla olevassa taulukossa on esimerkkejä nimikkeen tarjontaennusteriveistä.

| Malli    | Päivämäärä     | Toimittajanro | Toimittajaryhmä | Määrä | Yksikkö | Sivusto | Varasto |
|----------|----------|----------------|--------------|----------|------|------|-----------|
| CurrentF | 10.10.22 |                | VendorGroupA | 5        | kpl   | 1    | 11        |
| CurrentF | 10.10.22 |                | VendorGroupA | 6        | kpl   | 1    | 11        |
| CurrentF | 10.10.22 |                |              | 7        | kpl   | 1    | 11        |

Toimittaja *VendorA* on toimittajaryhmän *VendorGroupA* oletustoimittaja. Se on myös nimikkeen oletustoimittaja.

Sisäinen suunnittelumoduuli luo seuraavat tilaukset:

- Toimittajan *VendorA*, toimittajaryhmän *VendorGroupA* ja määrän *11* suunniteltu ostotilaus
- Toimittajan *VendorA* ja määrän *7* suunniteltu ostotilaus

Suunnittelun optimointi luo vain yhden tilauksen:

- Toimittajan *VendorA*, toimittajaryhmän *VendorGroupA* ja määrän *18* suunniteltu ostotilaus

### <a name="reduction-of-general-forecasts-by-more-specific-forecasts"></a>Yleisten ennusteiden vähennys näitä tarkempien ennusteiden mukaan

Sisäisessä pääsuunnittelumoduulissa tulos ei ole ennustettavissa, jos joillakin ennusteilla on toimittaja mutta joillakin ei.

Suunnittelun optimoinnissa yleisiä ennusteita vähennetään aina näitä tarkemmilla ennusteilla alla olevien esimerkkien mukaisesti.

Alla olevassa taulukossa on esimerkkejä nimikkeen tarjontaennusteriveistä.

| Päivämäärä       | Määrä | Toimittaja   | Toimittajaryhmä  |
|------------|----------|----------|---------------|
| 11.2.2022 | 5.00     | Vendor-A | VendorGroup-A |
| 11.2.2022 | 6,00     | Vendor-A | VendorGroup-A |
| 11.2.2022 | 15.00    |          |               |

Yleistä ennustetta (15,00 kappaletta) vähennetään tätä tarkemmilla ennusteilla (5,00 + 6,00 = 11,00 kappaletta). Jäljellä oleva määrä määritetään oletustoimittajalle. Suunnitellut tilaukset ovat seuraavassa taulukossa.

| Päivämäärä       | Määrä | Toimittaja   | Toimittajaryhmä  |
|------------|----------|----------|---------------|
| 11.2.2022 | 11.00    | Vendor-A | VendorGroup-A |
| 11.2.2022 | 4.00     | Vendor-A | VendorGroup-A |

### <a name="respect-for-default-order-settings-when-planned-orders-are-generated"></a>Tilauksen oletusasetusten noudattaminen suunniteltujen tilausten luomisessa

Kullakin nimikkeellä voi olla tilauksen oletusasetukset, kuten ostotilauksen vähimmäismäärä. Sisäinen suunnittelumoduuli ohittaa nämä asetukset ja muuntaa näin ennusteet suunnitelluiksi tilauksiksi, joilla on sama määrä. Suunnittelun optimointi noudattaa näitä asetuksia, kun suunnitellut tilaukset luodaan tarjontaennusteista. 

### <a name="aggregation-of-planned-orders-as-a-result-of-reduction-by-approved-orders"></a>Suunniteltujen tilausten koostaminen hyväksyttyjen tilausten mukaan tehtävän vähentämisen tuloksena

Sisäinen pääsuunnittelumoduuli olettaa, vain yksi tilaus vähentää olemassa olevaa tarjontaennustetta. Jos siis useat tilaukset vastaavat tarjontaennusteriviä, vain ensimmäinen tilaus vähentää sitä. Suunnittelun optimoinnissa kaikki tarjontaennusteriviä vastaavat tilaukset vähentävät sitä.

### <a name="reduction-of-forecasts-by-matching-vendors-only"></a>Ennusteiden vähennys vain vastaavien toimittajien mukaan

Kun sisäinen pääsuunnittelumoduuli vähentää ennustetta aiemmin luotujen vapautettujen ostotilausten mukaan, se ei varmista, että ostotilausten toimittaja vastaa ennusteen toimittajaa. Suunnittelun optimointi vähentää ennusteita vain niiden ostotilausten mukaan, joilla on vastaava arvo toimittajakentässä.

Siirto- ja tuotantotilauksissa toimittajakenttä ohitetaan aina, koska sillä ei ole merkitystä näissä tilaustyypeissä.

### <a name="reduction-of-forecasts-by-transfer-orders"></a>Ennusteiden vähennys siirtotilausten mukaan

Jos nimikkeen tilauksen oletustyyppi on *Siirto*, ennusteita voidaan vähentää vain olemassa olevien suunniteltujen siirtotilausten mukaan. Tuotanto- ja ostotilauksissa kuitenkin vain vapautetut tilaukset vähentävät tarjontaennustetta.

Sisäinen suunnittelumoduuli vähentää kaikkia siirtotilauksen tiloja, kun taas suunnittelun optimointi vähentää ennusteita vain niiden siirtotilausten mukaan, joiden tila on *Vapautettu*.
