---
title: Pääsuunnittelu ja kysynnän ennusteet
description: Tässä aiheessa käsitellään kysynnän ennusteiden sisällyttämistä pääsuunnitteluun suunnittelun optimoinnin avulla
author: ChristianRytt
ms.date: 12/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqPlanSched, ReqGroup, ReqReduceKey, ForecastModel
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-12-02
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: cbac68b79b2a10f05e0e442d4f0aa716e5a04634
ms.sourcegitcommit: ac23a0a1f0cc16409aab629fba97dac281cdfafb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/29/2021
ms.locfileid: "7867244"
---
# <a name="master-planning-with-demand-forecasts"></a>Pääsuunnittelu ja kysynnän ennusteet

[!include [banner](../../includes/banner.md)]

Kysynnän ennusteita voi käyttää yhdessä suunnittelun optimoinnin kanssa kattamaan odotetun kysynnän pääsuunnittelussa. Kysynnän ennuste voidaan luoda manuaalisesti, se voidaan tuoda tai se voidaan luoda käyttämällä Microsoft Dynamics 365 Supply Chain Managementin kysynnän ennustetta. Lisätietoja kysynnän ennusteesta on kohdassa [Kysynnän ennusten yleiskatsaus](../introduction-demand-forecasting.md).

> [!NOTE]
> Suunnittelun optimointi ei tue erillistä ennustesuunnittelua. Niinpä **Pääsuunnittelun parametrit** -sivun **Nykyinen ennustesuunnitelma** -asetuksella ei ole merkitystä suunnittelun optimointia käytettäessä.

## <a name="set-up-a-master-plan-to-include-a-demand-forecast"></a>Pääsuunnittelun määrittäminen sisältämään kysynnän ennuste

Pääsuunnitelma määritetään sisältämään kysynnän ennuste seuraavasti:

1. Siirry kohtaan **Pääsuunnittelu \> Määritykset \> Suunnitelmat \> Pääsuunnitelmat**.
1. Valitse aiemmin luotu suunnitelma tai luo uusi suunnitelma.
1. Valitse **Yleiset**-pikavälilehdellä seuraavat lisäkentät:

    - **Ennustemalli** – Valitse käytettävä ennustemalli. Tämä malli otetaan huomioon, kun nykyiselle pääsuunnitelmalle luodaan toimitusehdotuksia.
    - **Sisällytä kysynnän ennuste** – Määritä vaihtoehdoksi *Kyllä*, jos haluat sisällyttää kysynnän ennusteen nykyiseen pääsuunnitelmaan. Jos määrität vaihtoehdoksi *Ei*, kysynnän ennusteen tapahtumia ei sisällytetä pääsuunnitelmaan.
    - **Ennustevaatimusten vähentämiseen käytetty menetelmä** – Valitse menetelmä, jolla ennustevaatimuksia vähennetään. Lisätietoja on jäljempänä tämän aiheen kohdassa [Ennusteen vähennysavaimet](#reduction-keys).

1. Voit määrittää **Aikarajat päivinä** -pikavälilehdessä seuraavat kentät määrittämään kysynnän ennusteen sisältävän kauden seuraavien aikana:

    - **Ennustesuunnitelma** – Määritä asetukseksi *Kyllä*, jolloin yksittäisistä kattavuusryhmistä peräisin oleva ennustesuunnitelman aikaraja ohitetaan. Määritä asetukseksi *Ei*, jolloin käytetään nykyisen pääsuunnitelman yksittäisen kattavuusryhmien arvoja.
    - **Ennusteen ajanjakso** – jos **Ennustesuunnitelman** -asetuksena on *Kyllä*, määritä kuinka monta päivää (kuluvasta päivämäärästä) kysynnän ennustetta käytetään.

    > [!IMPORTANT]
    > **Ennustesuunnitelma**-asetusta ei vielä tueta suunnittelun optimoinnissa.

## <a name="set-up-a-coverage-group-to-include-a-demand-forecast"></a>Kattavuusryhmän määrittäminen sisältämään kysynnän ennuste

Kattavuusryhmä määritetään sisältämään kysynnän ennuste seuraavasti:

1. Valitse **Pääsuunnittelu \> Määritys \> Suunnitelmat \> Kattavuusryhmät**.
1. Valitse aiemmin luotu kattavuusryhmä tai luo uusi ryhmä.
1. Määritä **Muu**-pikavälilehdessä seuraavat kentät:

    - **Ennustesuunnitelman aikaraja** – Määritä kuinka monta päivää (kuluvasta päivämäärästä) kysynnän ennustetta käytetään. Tämä arvo voidaan ohittaa käyttämällä edellisessä osassa kuvattua pääsuunnitelman **Ennustesuunnitelma**-asetusta.
    - **Vähennysavain** – Valitse käytettävä vähennysavain. Lisätietoja on jäljempänä tämän aiheen kohdissa [Ennusteen vähennysavaimen luominen ja määrittäminen](#create-reduction-key) ja [Vähennysavaimen käyttäminen](#use-reduction-key).
    - **Vähennä ennustetta seuraavasti** – Jos pääsuunnitelman **Ennustevaatimusten vähentämiseen käytetty menetelmä** -kentän asetuksena on *Tapahtumat – vähennysavain* tai *Tapahtumat – dynaaminen kausi*, määritä, mitkä tapahtumat vähentävät ennustetta. Valitse jokin seuraavista:

        - **Kaikki tapahtumat** – kaikki tapahtumat vähentävät ennustetta.
        - **Tilaukset** – vain myyntitilaukset vähentävät ennustetta.

        > [!NOTE]
        > Jos valitset *Kaikki tapahtumat*, tapahtumia, joissa on sekä kysyntää ja tarjontaa samoissa varastodimensioissa, pidetään neutraaleina ja ne ohitetaan ennusten vähennyksen aikana. Jos esimerkiksi suunnitteludimensioksi on määritetty vain toimipaikka eikä varasto, toimipaikan 1, varaston 11 ja toimipaikan 1, varaston 13 välinen siirtotilaus ohitetaan, eikä se vähennän jäljellä olevaa kysynnän ennustetta.

    - **Sisällytä konsernin sisäiset tilaukset** – Määritä asetukseksi *Kyllä* jos konsernin sisäiset tilaukset sisällytetään ennustetta vähennettäessä. Määritä asetukseksi muutoin *Ei*.
    - **Sisällytä asiakasennuste kysynnän ennusteeseen** – Määritä, sisällytetäänkö asiakasennuste yleiseen ennusteeseen. Tämä asetus määrittää, miten todellinen kysyntä vähentää ennustettua kysyntää. Voit varmistaa sen avulla, että pääsuunnittelu kattaa tiettyjen asiakkaiden ostamien nimikkeiden tarjonnan.

        - Kun asetukseksi määritetään *Kyllä*, asiakasennuste sisällytetään yleiseen kysyntään. Siinä tapauksessa todellinen asiakaskysyntää vähentää sekä asiakaskysyntää että yleistä kysyntää. Pääsuunnittelu luo suunniteltuja tilauksia, jotka kattavat vain yleisen ennusteen määrän.
        - Määritä asetukseksi *Ei*, jos asiakasennustetta ei sisällytetä yleiseen kysyntään. Siinä tapauksessa todellinen asiakaskysyntä vähentää vain asiakaskysyntää. Pääsuunnittelu luo suunniteltuja tilauksia, jotka kattavat yleisen ennusteen määrän ja kunkin asiakkaan määrän ennusteen.

## <a name="forecast-reduction-keys"></a><a name="reduction-keys"></a>Ennusteen vähennysavaimet

Tässä osassa on tietoja eri menetelmistä, joiden avulla ennustetarpeita voidaan vähentää. Se sisältää esimerkkejä kunkin menetelmän tuloksista. Se myös käsittelee, miten luoda, määrittää ja käyttää ennusteen vähennysavainta. Jotkin menetelmät käyttävät ennusteen vähennysavaimia vähentämään ennustevaatimuksia.

### <a name="methods-that-are-used-to-reduce-forecast-requirements"></a>Ennustevaatimusten vähentämiseen käytetyt menetelmät

Kun lisäät ennusteen pääsuunnitelman, voit valita kuinka ennusteen tarpeita vähennetään, kun todellinen kysyntä sisällytetään. Huomaa, että pääsuunnittelu sulkee pois aiempien ennusteiden tarpeet, mikä tarkoittaa kaikkia ennustetarpeita ennen kuluvan päivän päivämäärää.

Voit sisällyttää ennusteen pääsuunnitelmaan ja valita menetelmän, jolla voit pienentää ennustetarpeita siirtymällä kohtaan **Pääsuunnittelu \> Määritys \> Suunnitelmat \> Pääsuunnitelmat**. Valitse **Ennustemalli** -kentästä ennustemalli. Valitse **Ennustevaatimusten vähentämiseen käytetty menetelmä** -kentästä menetelmä. Käytettävissä ovat seuraavat asetukset:

- Ei mitään
- Prosentti - vähennysavain
- Tapahtumat - vähennysavain
- Tapahtumat - dynaaminen kausi

Seuraavissa osissa on lisätietoja kustakin vaihtoehdosta.

#### <a name="none"></a>Ei mitään

Jos valitset **Ei mikään**, ennusteen tarpeita ei vähennetä pääajoituksen aikana. Tässä tapauksessa pääsuunnittelu luo suunnitellut tilaukset toimittaakseen ennustetun kysynnän (ennusteen tarpeet). Nämä suunnitellut tilaukset ylläpitävät ehdotettua määrää muuntyyppisestä kysynnästä riippumatta. Jos esimerkiksi tehdään myyntitilaukset, pääsuunnittelu luo uusia suunniteltuja lisätilauksia toimittamaan myyntitilaukset. Ennustetarpeiden määrää ei vähennetä.

#### <a name="percent--reduction-key"></a>Prosentti - vähennysavain

Jos **Prosentti - vähennysavain**: ennusteen tarpeita vähennetään vähennysavaimen määrittämien prosenttien ja kausien mukaan. Tässä tapauksessa pääsuunnittelu luo suunnitellut tilaukset, joissa määrä lasketaan seuraavasti: ennustettu määrä × vähennysavain kullakin kaudella. Jos on muuntyyppistä kysyntää, pääsuunnittelu luo myös suunnitellut tilaukset, jotka toimittavat tämän kysynnän.

##### <a name="example-percent--reduction-key"></a>Esimerkki: Prosentti - vähennysavain

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

#### <a name="transactions--reduction-key"></a>Tapahtumat - vähennysavain

Jos määrität **Ennustevaatimusten vähentämiseen käytetty menetelmä** -kentän arvoksi *Tapahtumat – vähennysavain*, ennustevaatimuksista vähennetään kelvollisilla kysyntätapahtumilla, jotka esiintyvät vähennysavaimen määrittäminä ajanjaksoina.

Kelvollinen kysyntä määritetään **Kattavuusryhmät**-sivun **Ennusteen vähennysperuste** -kentän avulla. Jos **Ennusteen vähennysperuste** -kentän arvoksi määritetään *Tilaukset*, vain tilaustapahtumat katsotaan kelvolliseksi kysynnäksi. Jos sen arvoksi määritetään *Kaikki tapahtumat*, kaikki muut kuin konsernin sisäiset varastonsiirrot katsotaan kelvolliseksi kysynnäksi. Jos myös konsernin sisäiset myynnit katsotaan kelvolliseksi kysynnäksi, **Sisällytä konsernin sisäiset tilaukset** -asetuksen arvoksi *Kyllä*.

Ennusteen vähennys alkaa vähennysavaimen jakson ensimmäisestä (aikaisimmasta) kysynnän ennustetietueesta. Jos kelvollisten varastotapahtumien määrä ylittää kysynnän ennusterivien määrän samalla vähennysavainjaksolla, varastotapahtumien määrän saldo vähennetään edellisen jakson kysynnän ennustemäärästä (jos käyttämätöntä ennustetta on jäljellä).

Jos edelliseltä vähennysavaimen jaksolta ei ole jäljellä käyttämätöntä ennustetta, varastotapahtumien määrän saldo vähennetään seuraavan kuukauden ennustemäärästä (jos käyttämätöntä ennustetta on).

Vähennysavainrivien **Prosenttiosuus**-kentän arvoa ei käytetä, kun **Ennustevaatimusten vähentämiseen käytetty menetelmä** -kentän asetuksena on *Tapahtumat – vähennysavain*. Vain päivämääriä käytetään vähennysavainjakson määrittämiseen.

> [!NOTE]
> Kulloisenakin päivämääränä tai sitä ennen kirjattuja ennusteita ei oteta huomioon eikä käytetä suunniteltujen tilausten luomiseen. Jos esimerkiksi kuukauden kysynnän ennuste on luotu 1. tammikuuta ja suoritat pääsuunnittelun, johon kuuluu kysynnän ennuste 2. tammikuuta, laskennassa ei oteta huomioon kysyntäennusteriviä, jonka päivämääränä on 1. tammikuuta.

##### <a name="example-transactions--reduction-key"></a>Esimerkki: Tapahtumat - vähennysavain

Tämä esimerkki osoittaa, miten vähennysavaimen määrittelemillä jaksoilla toteutuvat tilaukset pienentävät kysynnän ennustetarpeita.

[![Toteutuneet tilaukset ja ennuste ennen pääsuunnittelun suorittamista.](media/forecast-reduction-keys-1-small.png)](media/forecast-reduction-keys-1.png)

Tässä esimerkissä valitset *Pääsuunnitelmat* -sivun **Ennustevaatimusten vähentämiseen käytetty menetelmä** -kentässä **Tapahtumat - vähennysavain**.

Seuraavat kysyntäennusterivit ovat olemassa 1. huhtikuuta.

| Päivämäärä     | Ennustettu kappalemäärä |
|----------|-----------------------------|
| Huhtikuun 5.  | 100                         |
| Huhtikuun 12. | 100                         |
| Huhtikuun 19. | 100                         |
| Huhtikuun 26. | 100                         |
| Toukokuun 3.    | 100                         |
| Toukokuun 10.   | 100                         |
| Toukokuun 17.   | 100                         |

Seuraavat myyntitilausrivit ovat olemassa huhtikuun osalta.

| Päivämäärä     | Tarvittava kappalemäärä |
|----------|----------------------------|
| Huhtikuun 27. | 240                        |

[![Suunniteltu huhtikuun tilausten perusteella muodostettu tarjonta.](media/forecast-reduction-keys-2-small.png)](media/forecast-reduction-keys-2.png)

Seuraavat tarvemäärät siirretään pääsuunnitelmaan, kun pääsuunnittelu suoritetaan 1. huhtikuuta. Kuten näkyy, huhtikuun ennustetapahtumia vähennettiin kysyntämäärällä 240 sarjassa, joka alkaa ensimmäisestä näistä tapahtumista.

| Päivämäärä     | Kappaletarve |
|----------|---------------------------|
| Huhtikuun 5.  | 0                         |
| Huhtikuun 12. | 0                         |
| Huhtikuun 19. | 60                        |
| Huhtikuun 26. | 100                       |
| Huhtikuun 27. | 240                       |
| Toukokuun 3.    | 100                       |
| Toukokuun 10.   | 100                       |
| Toukokuun 17.   | 100                       |

Oletetaan nyt, että toukokuulle on tuotu uusia tilauksia.

Seuraavat myyntitilausrivit ovat olemassa toukokuun osalta.

| Päivämäärä   | Tarvittava kappalemäärä |
|--------|----------------------------|
| Toukokuun 4.  | 80                         |
| Toukokuun 11. | 130                        |

[![Suunniteltu huhtikuun ja toukokuun tilausten perusteella muodostettu tarjonta.](media/forecast-reduction-keys-3-small.png)](media/forecast-reduction-keys-3.png)

Seuraavat tarvemäärät siirretään pääsuunnitelmaan, kun pääsuunnittelu suoritetaan 1. huhtikuuta. Kuten näkyy, huhtikuun ennustetapahtumia vähennettiin kysyntämäärällä 240 sarjassa, joka alkaa ensimmäisestä näistä tapahtumista. Toukokuun ennustetapahtumien määrää kuitenkin vähennettiin yhteensä 210:llä alkaen toukokuun ensimmäisestä kysyntäennustetapahtumasta. Jaksokohtainen kokonaissumma kuitenkin säilytetään (400 huhtikuussa ja 300 toukokuussa).

| Päivämäärä     | Kappaletarve |
|----------|---------------------------|
| Huhtikuun 5.  | 0                         |
| Huhtikuun 12. | 0                         |
| Huhtikuun 19. | 60                        |
| Huhtikuun 26. | 100                       |
| Huhtikuun 27. | 240                       |
| Toukokuun 3.    | 0                         |
| Toukokuun 4.    | 80                        |
| Toukokuun 10.   | 0                         |
| Toukokuun 11.   | 130                       |
| Toukokuun 17.   | 90                        |

#### <a name="transactions--dynamic-period"></a>Tapahtumat - dynaaminen kausi

Jos valitset **Tapahtumat - dynaaminen kausi**, ennusteen tarpeita vähennetään dynaamisen kauden aikana tapahtuvien todellisten tilaustapahtumien mukaan. Dynaaminen kausi kattaa nykyiset ennustepäivämäärät ja päättyy seuraavan ennusteen alkuun. Tässä tapauksessa pääsuunnittelu luo suunnitellut tilaukset toimittaakseen ennustetun kysynnän (ennusteen tarpeet). Kun todelliset tilaustapahtumat tallennetaan, ennusteen tarpeita kuitenkin vähennetään. Todelliset tapahtumat kuluttavat osan ennustetuista vaatimuksista.

Kun tätä vaihtoehtoa käytetään, tapahtuu seuraavaa:

- Vähennysavaimia ei vaadita tai käytetä. 
- Jos ennuste vähenee kokonaan, nykyisen ennusteen ennustetarpeiksi tulee nolla.
- Jos tulevaa ennustetta ei ole, vähennetään edellisen syötetyn ennusteen ennustetarpeita.
- Ennusteen vähennyslaskentaan sisällytetään aikarajat.
- Ennusteen vähennyslaskentaan sisällytetään positiiviset päivät.
- Jos toteutuneet tilaustapahtumat ylittävät ennustetarpeet, jäljelle jääviä tapahtumia ei siirretä seuraavalle ennustekaudelle.

##### <a name="example-1-transactions--dynamic-period"></a>Esimerkki 1: Tapahtumat - dynaaminen kausi

Tässä on yksinkertainen esimerkki, jossa näkyy, kuinka **Tapahtumat - dynaaminen kausi** -menetelmä toimii.

Tässä esimerkissä lisäät seuraavan kysyntäennusteen pääsuunnitelmaan.

| Päivämäärä       | Kysynnän ennuste |
|------------|-----------------|
| 1. tammikuuta  | 1 000           |
| Helmikuun 1. | 1 000             |

Luot myös seuraavat myyntitilaukset.

| Päivämäärä        | Myyntitilauksen määrä |
|-------------|----------------------|
| 15. tammikuuta  | 200                  |
| Helmikuun 15. | 400                  |

Tässä tapauksessa luodaan seuraavat suunnitellut tilaukset.

| Kysynnän ennusteen päivämäärä | Määrä | Selitys                           |
|--------------------- |----------|---------------------------------------|
| 1. tammikuuta            | 800      | Ennusteen tarpeet (= 1 000-200) |
| 15. tammikuuta           | 200      | Myyntitilausten tarpeet             |
| Helmikuun 1.           | 600      | Ennusteen tarpeet (= 1 000-400) |
| Helmikuun 15.          | 400      | Myyntitilausten tarpeet             |

##### <a name="example-2-transactions--dynamic-period"></a>Esimerkki 2: Tapahtumat - dynaaminen kausi

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

### <a name="create-and-set-up-a-forecast-reduction-key"></a><a name="create-reduction-key"></a>Luo ja määritä ennusteen vähennysavain

Ennusteen vähennysavainta käytetään **Tapahtumat - vähennysavain**- ja **Prosentti - vähennysavain** -menetelmissä ennusteen tarpeiden vähentämiseen. Näiden ohjeiden avulla voit luoda ja määrittää vähennysavaimen.

1. Siirry kohtaan **Pääsuunnittelu \> Määritys \> Kattavuus \> Vähennysavaimet**.
2. Luo vähennysavain valitsemalla **Uusi**.
3. Syötä **Vähennysavain**-kenttään ennusteen vähennysavaimen yksilöivä tunnus. Syötä **Nimi**-kenttään nimi. 
4. Määritä kaudet sekä kunkin kauden vähennysavaimen prosentti:

    - **Voimaantulopäivä**-kenttä ilmaisee päivämäärän, jolloin kauden luonti alkaa. Kun **Käytä voimassaolopäivää** -kentän arvo on **Kyllä**, jaksot alkavat voimassaolopäivänä. Kun arvo on **Ei**, kaudet alkavat päivämääränä, kun pääsuunnittelu suoritetaan.
    - Määritä kaudet, joiden aikana ennusteen vähennys tulisi tapahtua.
    - Määritä tietylle kaudellle prosentit, joiden mukaan ennusteen tarpeita tulisi vähentää. Voit pienentää tarpeita määrittämällä positiivisia arvoja ja lisätä tarpeita määrittämällä negatiivisia arvoja.

### <a name="use-a-reduction-key"></a><a name="use-reduction-key"></a>Vähennysavaimen käyttö

Ennusteen vähennysavain on määritettävä nimikkeen kattavuusryhmään. Määritä vähennysavain nimikkeen kattavuusryhmään seuraavasti.

1. Siirry kohtaan **Pääsuunnittelu \> Määritys \> Kattavuus \> Kattavuusryhmät**.
2. Valitse **Muut**-pikavälilehden **Vähennysavain**-kentässä kattavuusryhmään määritettävä vähennysavain. Vähennysavaimen sitten kohdistetaan kaikkiin nimikkeisiin, jotka kuuluvat kyseiseen kattavuusryhmään.
3. Voit käyttää vähennysavainta laskemaan ennusteen vähennykset pääajoituksen aikana määrittämällä tämän asetuksen pääsuunnitelman tai ennustesuunnitelman asetuksissa. Valitse jokin seuraavista sijainneista:

    - **Pääsuunnittelu \> Määritys \> Suunnitelmat \> Ennustesuunnitelmat**
    - **Pääsuunnittelu \> Määritys \> Suunnitelmat \> Pääsuunnitelmat**

4. Kun olet **Ennustesuunnitelmat** tai **Pääsuunnitelmat**-sivulla, valitse edelleen **Yleiset**-pikavälilehden **Ennustevaatimusten vähentämiseen käytetty menetelmä** -kentässä **Prosentti - vähennysavain** tai **Tapahtumat - vähennysavain**.

### <a name="reduce-a-forecast-by-transactions"></a>Vähennä ennustetta tapahtumien mukaan

Kun valitset **Tapahtumat - vähennysavain** tai **Tapahtumat - dynaaminen kausi** ennustetarpeita vähennystapana, voit määrittää, mitkä tapahtumat vähentävät ennustetta. Valitse **Kattavuusryhmät** -sivun **Muut**-pikavälilehden **Vähennä ennustetta seuraavasti** -kentässä **Kaikki tapahtumat**, jossa kaikkien tapahtumien tulisi vähentää ennustetta, tai **Tilaukset**, jos vain myyntitilausten tulisi vähentää ennustetta.

## <a name="forecast-models-and-submodels"></a>Ennustemallit ja osamallit

Tässä osiossa kuvataan, kuinka voit luoda ennustemalleja ja yhdistää useita ennustemalleja yhdistetään määrittämällä osamalleja.

*Ennustemalli* nimeää ja yksilöi tietyn ennusteen. Kun olet luonut ennustemallin, voit lisätä siihen ennusterivejä. Jos haluat lisätä ennusterivejä useille nimikkeille, käytä **Kysynnän ennusteen rivit** -sivua. Jos haluat lisätä ennusterivejä tietylle valitulle nimikkeelle, käytä **Vapautetut tuotteet** -sivua.

Ennustemalli voi sisältää ennusteita muista ennustemalleista. Voit tehdä näin lisäämällä muita ennustemalleja pääennustemallin *osamalleiksi*. Sinun täytyy luoda malli ennen kuin voit lisätä sen pääennustemallin osamalliksi.

Tuloksena oleva rakenne tarjoaa sinulle tehokkaan tavan hallita ennusteita, koska sen avulla voit yhdistää (koostaa) useiden yksittäisten ennusteiden syötteet toisiinsa. Näin ollen ennusteiden yhdistäminen simulaatioita varten on helppoa suunnittelun näkökulmasta. Voit esimerkiksi luoda simulaation, joka perustuu tavallisen ennusteen ja kevätkampanjan ennusteen yhdistelmään.

### <a name="submodel-levels"></a>Osamallien tasot

Pääennustemalliin lisättävien osamallien määrää ei ole rajoitettu. Rakenne voi kuitenkin olla vain yhden tason syvä. Toisin sanoen ennustemallilla, joka on toisen ennustemallin osamalli, ei voi olla omia osamalleja. Kun lisäät ennustemalliin osamalleja, järjestelmä tarkastaa, onko ennustemalli jo toisen ennustemallin osamalli.

Jos pääsuunnittelu kohtaa osamallin, jolla on omia osamalleja, näkyviin tulee virhesanoma.

#### <a name="submodel-levels-example"></a>Esimerkki osamallien tasoista

Ennustemallilla A on osamallina ennustemalli B. Näin ollen ennustemallilla B ei voi olla omia osamallejaan. Jos yrität lisätä osamallia ennustemalliin B, näet tämän virhesanoman: "Ennustemalli B on mallin A osamalli”.

### <a name="aggregating-forecasts-across-forecast-models"></a>Ennusteiden koostaminen yhteen eri ennustemalleista

Samana päivänä tapahtuvat ennusterivit yhdistetään niiden ennustemallista ja sen osamalleista.

#### <a name="aggregation-example"></a>Esimerkki koostamisesta

Ennustemallilla A on osamalleina ennustemallit B ja C.

- Ennustemalli A sisältää kysynnän ennusteen 2 kappaleelle (kpl) 15. kesäkuuta.
- Ennustemalli B sisältää kysynnän ennusteen 3 kappaleelle 15. kesäkuuta.
- Ennustemalli C sisältää kysynnän ennusteen 4 kappaleelle 15. kesäkuuta.

Tuloksena syntyvä kysynnän ennuste on yksi 9 kpl (2+3+4) kysyntä 15. kesäkuuta.

> [!NOTE]
> Jokainen osamalli käyttää omia parametrejään, ei pääennustemallin parametrejä.

### <a name="create-a-forecast-model"></a>Ennustemallin luominen

Voit luoda ennustemallin noudattamalla seuraavia ohjeita.

1. Avaa **Pääsuunnittelu \> Määritys \> Kysynnän ennuste \> Ennustemallit**.
1. Valitse toimintoruudussa **Uusi**.
1. Määritä uudelle ennustemallille seuraavat kentät:

    - **Malli** – Syötä mallille yksilöivä tunnus.
    - **Nimi** – Anna mallille kuvaava nimi.
    - **Pysäytetty** – Tavallisesti sinun tulisi valita täksi vaihtoehdoksi *Ei*. Valitse *Kyllä* vain, jos haluat estää kaikkien malliin kohdistettujen ennusterivien muokaamisen.

    > [!NOTE]
    > **Sisällytä kassavirtaennusteisiin** -kenttä ja **Projekti**-pikavälilehden kentät eivät liity pääsuunnitteluun. Sinun ei tarvitse siis huomioida niitä tässä asiayhteydessä. Sinun täytyy ottaa ne huomioon vain, kun käytät **Projektinhallinta ja kirjanpito** -moduulin ennusteita.

### <a name="assign-submodels-to-a-forecast-model"></a>Osamallien kohdistaminen ennustemalliin

Kohdista ennustemalliin osamalleja noudattamalla seuraavia ohjeita.

1. Valitse **Varastonhallinta \> Määritys \> Ennuste \> Ennustemallit**.
1. Valitse luetteloruudusta ennustemalli, jolle haluat määrittää osamallin.
1. Valitse **Osamalli**-pikavälilehdestä **Lisää** lisätäksesi ruudukkoon uuden rivin.
1. Määritä uudella rivillä seuraavat kentät:

    - **Osamalli** – Valitse ennustemalli, joka lisätään osamalliksi. Tämän ennustemallin täytyy olla jo olemassa, eikä sillä saa olla omia osamalleja.
    - **Nimi** – Anna osamallille kuvaava nimi. Tämä nimi voi esimerkiksi osoittaa osamallin suhteen pääennustemalliin.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

