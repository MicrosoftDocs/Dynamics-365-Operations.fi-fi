---
title: Ennusteen vähennysavaimet
description: Tämä aihe sisältää esimerkkejä, jotka kuvaavat vähennysavaimen määrittämistä. Artikkelissa kuvataan erilaisia vähennysavaimen asetuksia ja kunkin asetuksen tuloksia. Vähennysavaimen avulla voit määrittää, kuinka ennustevaatimuksia voidaan vähentää.
author: roxanadiaconu
manager: AnnBe
ms.date: 02/28/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqPlanSched
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19251
ms.assetid: aa9e0dfb-6052-4a2e-9378-89507c02fdf2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b915570145a48db7a182b9fce34e1544e3600107
ms.sourcegitcommit: a95ccf4cee8757c5fb2442a2aaeb45b1e33b6492
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/14/2019
ms.locfileid: "993041"
---
# <a name="method-used-to-reduce-forecast-requirements"></a>Ennustevaatimusten vähentämiseen käytetty menetelmä

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa on tietoja eri menetelmistä, joiden avulla ennustetarpeita voidaan vähentää. Se sisältää esimerkkejä kunkin menetelmän tuloksista. Se myös käsittelee, miten luoda, määrittää ja käyttää ennusteen vähennysavainta. Jotkin menetelmät käyttävät ennusteen vähennysavaimia vähentämään ennustevaatimuksia.

## <a name="methods-that-are-used-to-reduce-forecast-requirements"></a>Ennustevaatimusten vähentämiseen käytetyt menetelmät

Kun lisäät ennusteen pääsuunnitelman, voit valita kuinka ennusteen tarpeita vähennetään, kun todellinen kysyntä sisällytetään.

Voit sisällyttää ennusteen pääsuunnitelmaan ja valita menetelmän, jolla voit pienentää ennustetarpeita siirtymällä kohtaan **Pääsuunnittelu \> Määritys \> Suunnitelmat \> Pääsuunnitelmat**. Valitse **Ennustemalli** -kentästä ennustemalli. Valitse **Ennustevaatimusten vähentämiseen käytetty menetelmä** -kentästä menetelmä. Käytettävissä ovat seuraavat asetukset:

- Ei mitään
- Prosentti - vähennysavain
- Tapahtumat - vähennysavain
- Tapahtumat - dynaaminen kausi

Seuraavissa osissa on lisätietoja kustakin vaihtoehdosta.

### <a name="none"></a>Ei mitään

Jos valitset **Ei mikään**, ennusteen tarpeita ei vähennetä pääajoituksen aikana. Tässä tapauksessa pääsuunnittelu luo suunnitellut tilaukset toimittaakseen ennustetun kysynnän (ennusteen tarpeet). Nämä suunnitellut tilaukset ylläpitävät ehdotettua määrää muuntyyppisestä kysynnästä riippumatta. Jos esimerkiksi tehdään myyntitilaukset, pääsuunnittelu luo uusia suunniteltuja lisätilauksia toimittamaan myyntitilaukset. Ennustetarpeiden määrää ei vähennetä.

### <a name="percent--reduction-key"></a>Prosentti - vähennysavain

Jos **Prosentti - vähennysavain**: ennusteen tarpeita vähennetään vähennysavaimen määrittämien prosenttien ja kausien mukaan. Tässä tapauksessa pääsuunnittelu luo suunnitellut tilaukset, joissa määrä lasketaan seuraavasti: ennustettu määrä × vähennysavain kullakin kaudella. Jos on muuntyyppistä kysyntää, pääsuunnittelu luo myös suunnitellut tilaukset, jotka toimittavat tämän kysynnän.

#### <a name="example-percent--reduction-key"></a>Esimerkki: Prosentti - vähennysavain

Tämä esimerkki osoittaa, miten vähennysavain pienentää kysynnän ennustetarpeita vähennysavaimen määrittämien prosenttien ja kausien mukaisesti.

Tässä esimerkissä lisäät seuraavan kysyntäennusteen pääsuunnitelmaan.

| Kuukausi    | Kysynnän ennuste |
|----------|-----------------|
| Tammikuu  | 1 000           |
| Helmikuu | 1 000           |
| Maaliskuu    | 1 000           |
| Huhtikuu    | 1 000           |

Määritä **Vähennysavaimet**-sivulla seuraavat rivit.

| Muutos | Yksikkö  | Prosenttia |
|--------|-------|---------|
| 1      | Kuukausi | 100     |
| 2      | Kuukausi | 75      |
| 3      | Kuukausi | 50      |
| 4      | Kuukausi | 25      |

Määritä vähennysavain nimikkeen kattavuusryhmään. Sitten **Pääsuunnitelmat** -sivun **Ennustevaatimusten vähentämiseen käytetty menetelmä** -kentässä valitse **Prosentti - vähennysavain**.

Tällöin jos suoritat ennusteajoituksen 1. tammikuuta, kysynnän ennustetarpeita kulutetaan **Vähennysavaimet**-sivulla määritettyjen prosenttien mukaisesti. Pääsuunnitelmaan siirretään seuraavat tarvemäärät.

| Kuukausi                | Suunniteltu tilausmäärä | Laskelma    |
|----------------------|------------------------|----------------|
| Tammikuu              | 0                      | = 0 % × 1 000   |
| Helmikuu             | 250                    | = 25 % × 1 000  |
| Maaliskuu                | 500                    | = 50 % × 1 000  |
| Huhtikuu                | 750                    | = 75 % × 1 000  |
| Touko–joulukuu | 1 000                  | = 100 % × 1 000 |

### <a name="transactions--reduction-key"></a>Tapahtumat - vähennysavain

Jos valitset **Tapahtumat - vähennysavain**: ennusteen tarpeita vähennetään vähennysavaimen määrittämien kausien aikaisten tapahtumien mukaan.

#### <a name="example-transactions--reduction-key"></a>Esimerkki: Tapahtumat - vähennysavain

Tämä esimerkki osoittaa, miten vähennysavaimen määrittelemillä jaksoilla toteutuvat tilaukset pienentävät kysynnän ennustetarpeita.

Tässä esimerkissä valitset **Pääsuunnitelmat** -sivun **Ennustevaatimusten vähentämiseen käytetty menetelmä** -kentässä **Tapahtumat - vähennysavain**.

1. tammikuuta mennessä on tehty seuraavat myyntitilaukset.

| Kuukausi    | Tilattu kappalemäärä |
|----------|--------------------------|
| Tammikuu  | 956                      |
| Helmikuu | 1 176                    |
| Maaliskuu    | 451                      |
| Huhtikuu    | 119                      |

Jos käytät edellisen esimerkin kanssa samaa 1 000 kappaleen kysyntäennustetta kuukaudessa, pääsuunnitelmaan siirretään seuraavat tarvemäärät.

| Kuukausi                | Kappaletarve |
|----------------------|---------------------------|
| Tammikuu              | 44                        |
| Helmikuu             | 0                         |
| Maaliskuu                | 549                       |
| Huhtikuu                | 881                       |
| Touko–joulukuu | 1 000                     |

### <a name="transactions--dynamic-period"></a>Tapahtumat - dynaaminen kausi

Jos valitset **Tapahtumat - dynaaminen kausi**, ennusteen tarpeita vähennetään dynaamisen kauden aikana tapahtuvien todellisten tilaustapahtumien mukaan. Dynaaminen kausi kattaa nykyiset ennustepäivämäärät ja päättyy seuraavan ennusteen alkuun. Tässä tapauksessa pääsuunnittelu luo suunnitellut tilaukset toimittaakseen ennustetun kysynnän (ennusteen tarpeet). Kun todelliset tilaustapahtumat tallennetaan, ennusteen tarpeita kuitenkin vähennetään. Todelliset tapahtumat kuluttavat osan ennustetuista vaatimuksista.

Kun tätä vaihtoehtoa käytetään, tapahtuu seuraavaa:

- Vähennysavaimia ei vaadita tai käytetä. 
- Jos ennuste vähenee kokonaan, nykyisen ennusteen ennustetarpeiksi tulee nolla.
- Jos tulevaa ennustetta ei ole, vähennetään edellisen syötetyn ennusteen ennustetarpeita.
- Ennusteen vähennyslaskentaan sisällytetään aikarajat.
- Ennusteen vähennyslaskentaan sisällytetään positiiviset päivät.
- Jos toteutuneet tilaustapahtumat ylittävät ennustetarpeet, jäljelle jääviä tapahtumia ei siirretä seuraavalle ennustekaudelle.

#### <a name="example-1-transactions--dynamic-period"></a>Esimerkki 1: Tapahtumat - dynaaminen kausi

Tässä on yksinkertainen esimerkki, jossa näkyy, kuinka **Tapahtumat - dynaaminen kausi** -menetelmä toimii.

Tässä esimerkissä lisäät seuraavan kysyntäennusteen pääsuunnitelmaan.

| Päivämäärä       | Kysynnän ennuste |
|------------|-----------------|
| 1. tammikuuta  | 1 000           |
| Helmikuun 1. | 500             |

Luot myös seuraavat myyntitilaukset.

| Päivämäärä        | Myyntitilauksen määrä |
|-------------|----------------------|
| 15. tammikuuta  | 500                  |
| Helmikuun 15. | 100                  |

Tässä tapauksessa luodaan seuraavat suunnitellut tilaukset.

| Kysynnän ennusteen päivämäärä | Määrä | Selitys                           |
|--------------------- |----------|---------------------------------------|
| 1. tammikuuta            | 800      | Ennusteen tarpeet (= 1 000-200) |
| 15. tammikuuta           | 200      | Myyntitilausten tarpeet             |
| Helmikuun 1.           | 600      | Ennusteen tarpeet (= 1 000-400) |
| Helmikuun 15.          | 400      | Myyntitilausten tarpeet             |

#### <a name="example-2-transactions--dynamic-period"></a>Esimerkki 2: Tapahtumat - dynaaminen kausi

Useimmiten järjestelmät on määritetty siten, että tapahtumat vähentävät kysynnän ennustetta määritetyillä ennustekausilla: viikkoina, kuukausina ja niin edelleen. Nämä kaudet vähennysavaimeen. Kahden kysynnän ennusterivin välinen aika voi kuitenkin myös *vihjata* tiettyyn kauteen.

Tässä esimerkissä luot kysynnän ennusteen seuraaville päivämäärille ja määrille.

| Päivämäärä       | Kysynnän ennuste |
|------------|-----------------|
| 1. tammikuuta  | 1 000           |
| 5. tammikuuta  | 500             |
| 12. tammikuuta | 1 000           |

Huomaa, että tässä ennusteessa ei ole selkeää kautta ennusteen päivämäärien välillä. Ensimmäisen ja toisen päivämäärän välillä on neljän päivän jakson, ja toisen ja kolmannen päivämäärän välillä on seitsemän päivän jakso. Nämä aikavälit ovat dynaamisia kausia.

Luot myös seuraavat myyntitilausrivit.

| Päivämäärä                             | Myyntitilauksen määrä |
|----------------------------------|----------------------|
| 15. joulukuuta edellisenä vuonna | 500                  |
| 3. tammikuuta                        | 100                  |
| 10. tammikuuta                       | 200                  |

Tässä tapauksessa ennustetta vähennetään seuraavasti:

- Koska ensimmäinen myyntitilaus ei ole millään kaudella, se ei vähennä mitään ennustetta.
- Koska toinen myyntitilaus on välillä 1.–5. tammikuuta, se vähentää tammikuun 1. päivän ennustetta 100:lla.
- Koska kolmas myyntitilaus on välillä 5.–12. tammikuuta, se vähentää tammikuun 5. päivän ennustetta 200:lla.

Siksi luodaan seuraavat suunnitellut tilaukset.

| Kysynnän ennusteen päivämäärä             | Määrä | Selitys                                                         |
|----------------------------------|----------|---------------------------------------------------------------------|
| 15. joulukuuta edellisenä vuonna | 500      | Myyntitilauksen tarpeet                                            |
| 1. tammikuuta                        | 900      | Ennustetarpeiden kausi 1.1.–5.1 (= 1 000 – 100) |
| 3. tammikuuta                        | 100      | Myyntitilauksen tarpeet                                            |
| 5. tammikuuta                        | 300      | Ennustetarpeiden kausi 5.1.–10.1 (= 500 – 200)  |
| 12. tammikuuta                       | 1 000    | Ennustetarpeiden kausi 12.1.–loppu                      |

## <a name="create-and-set-up-a-forecast-reduction-key"></a>Luo ja määritä ennusteen vähennysavain

Ennusteen vähennysavainta käytetään **Tapahtumat - vähennysavain**- ja **Prosentti - vähennysavain** -menetelmissä ennusteen tarpeiden vähentämiseen. Näiden ohjeiden avulla voit luoda ja määrittää vähennysavaimen.

1. Siirry kohtaan **Pääsuunnittelu \> Määritys \> Kattavuus \> Vähennysavaimet**.
2. Valitse **Uusi** tai paina **Ctrl + N** luodaksesi vähennysavaimen.
3. Syötä **Vähennysavain**-kenttään ennusteen vähennysavaimen yksilöivä tunnus. Syötä **Nimi**-kenttään nimi. 
4. Määritä kaudet sekä kunkin kauden vähennysavaimen prosentti:

    - **Voimaantulopäivä**-kenttä ilmaisee päivämäärän, jolloin kauden luonti alkaa. Kun **Käytä voimassaolopäivää** -kentän arvo on **Kyllä**, jaksot alkavat voimassaolopäivänä. Kun arvo on **Ei**, kaudet alkavat päivämääränä, kun pääsuunnittelu suoritetaan.
    - Määritä kaudet, joiden aikana ennusteen vähennys tulisi tapahtua.
    - Määritä tietylle kaudellle prosentit, joiden mukaan ennusteen tarpeita tulisi vähentää. Voit pienentää tarpeita määrittämällä positiivisia arvoja ja lisätä tarpeita määrittämällä negatiivisia arvoja.

## <a name="use-a-reduction-key"></a>Vähennysavaimen käyttö

Ennusteen vähennysavain on määritettävä nimikkeen kattavuusryhmään. Määritä vähennysavain nimikkeen kattavuusryhmään seuraavasti.

1. Siirry kohtaan **Pääsuunnittelu \> Määritys \> Kattavuus \> Kattavuusryhmät**.
2. Valitse **Muut**-pikavälilehden **Vähennysavain**-kentässä kattavuusryhmään määritettävä vähennysavain. Vähennysavaimen sitten kohdistetaan kaikkiin nimikkeisiin, jotka kuuluvat kyseiseen kattavuusryhmään.
3. Voit käyttää vähennysavainta laskemaan ennusteen vähennykset pääajoituksen aikana määrittämällä tämän asetuksen pääsuunnitelman tai ennustesuunnitelman asetuksissa. Valitse jokin seuraavista sijainneista:

    - Pääsuunnittelu \> Määritys \> Suunnitelmat \> Ennustesuunnitelmat
    - Pääsuunnittelu \> Asetukset \> Suunnitelmat \> Pääsuunnitelmat

4. Kun olet **Ennustesuunnitelmat** tai **Pääsuunnitelmat**-sivulla, valitse edelleen **Yleiset**-pikavälilehden **Ennustevaatimusten vähentämiseen käytetty menetelmä** -kentässä **Prosentti - vähennysavain**tai **Tapahtumat - vähennysavain**.

## <a name="reduce-a-forecast-by-transactions"></a>Vähennä ennustetta tapahtumien mukaan

Kun valitset **Tapahtumat - vähennysavain** tai **Tapahtumat - dynaaminen kausi** ennustetarpeita vähennystapana, voit määrittää, mitkä tapahtumat vähentävät ennustetta. Valitse **Vapautetut tuotteet** -sivun **Muut**-pikavälilehden **Vähennä ennustetta seuraavasti** -kentässä **Kaikki tapahtumat**, josa kaikkien tapahtumien tulisi vähentää ennustetta, tai **Tilaukset**, jos vain myyyntitilausten tulisi vähentää ennustetta.

## <a name="additional-resources"></a>Lisäresurssit

[Pääsuunnitelmat](master-plans.md)
