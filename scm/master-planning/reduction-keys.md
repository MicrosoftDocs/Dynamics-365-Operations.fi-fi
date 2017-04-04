---
title: "Vähennysavaimet"
description: "Tämä artikkeli sisältää esimerkkejä, jotka kuvaavat vähennysavaimen määrittämistä. Artikkelissa kuvataan erilaisia vähennysavaimen asetuksia ja kunkin asetuksen tuloksia. Vähennysavaimen avulla voit määrittää, kuinka ennustevaatimuksia voidaan vähentää."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ReqPlanSched
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 19251
ms.assetid: aa9e0dfb-6052-4a2e-9378-89507c02fdf2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: ff7525f4360e755e68ac3d7ecae281770481ef89
ms.lasthandoff: 03/31/2017


---

# <a name="reduction-keys"></a>Vähennysavaimet

Tämä artikkeli sisältää esimerkkejä, jotka kuvaavat vähennysavaimen määrittämistä. Artikkelissa kuvataan erilaisia vähennysavaimen asetuksia ja kunkin asetuksen tuloksia. Vähennysavaimen avulla voit määrittää, kuinka ennustevaatimuksia voidaan vähentää.

<a name="example-1-percent---reduction-key-forecast-reduction-principle"></a>Esimerkki 1: Ennusteen vähennysperiaatteena Prosentti – vähennysavain
---------------------------------------------------------------

Tämä esimerkki osoittaa, miten vähennysavain pienentää kysynnän ennustetarpeita vähennysavaimen määrittämien prosenttien ja kausien mukaisesti.

1.  Määritä **Vähennysavaimet**-sivulla seuraavat rivit.
    | Vaihto | Yksikkö  | Prosentti |
    |--------|-------|---------|
    | 1      | Kuukausi | 100     |
    | 2      | Kuukausi | 75      |
    | 3      | Kuukausi | 50      |
    | 4      | Kuukausi | 25      |

2.  Linkitä vähennysavain nimikkeen kattavuusryhmään.
3.  Valitse **Pääsuunnitelmat**-sivulla **Vähennysperiaate** -kentästä **Prosentti - vähennysavain**.
4.  Luo kysynnän ennuste 1 000 kappaleesta kuukaudessa.

Jos suoritat ennusteajoituksen 1. tammikuuta, kysynnän ennustetarpeita kulutetaan **Vähennysavaimet**-sivulla määritettyjen prosenttien mukaisesti. Pääsuunnitelmaan siirretään seuraavat tarvemäärät.

| Kuukausi                | Kappaletarve |
|----------------------|---------------------------|
| Tammikuu              | 0                         |
| Helmikuu             | 250                       |
| Maaliskuu                | 500                       |
| Huhtikuu                | 750                       |
| Touko–joulukuu | 1 000                     |

## <a name="example-2-transactions--reduction-key-forecast-reduction-principle"></a>Esimerkki 2: Tapahtumat-vähennysavain Vähennysperiaate ennuste
Tämä esimerkki osoittaa, miten vähennysavaimen määrittelemillä jaksoilla toteutuvat tilaukset pienentävät kysynnän ennustetarpeita.

-   Valitse **Pääsuunnitelmat**-sivulla **Vähennysperiaate** -kentästä **Tapahtuma - vähennysavain**.

1. tammikuuta mennessä on tehty seuraavat myyntitilaukset.

| Kuukausi    | Tilattu kappalemäärä |
|----------|--------------------------|
| Tammikuu  | 956                      |
| Helmikuu | 1 176                    |
| Maaliskuu    | 451                      |
| Huhtikuu    | 119                      |

Jos käytät samaa 1 000 kappaleen kysyntäennustetta kuukaudessa, pääsuunnitelmaan siirretään seuraavat tarvemäärät.

| Kuukausi                | Kappaletarve |
|----------------------|---------------------------|
| Tammikuu              | 44                        |
| Helmikuu             | 0                         |
| Maaliskuu                | 549                       |
| Huhtikuu                | 881                       |
| Touko–joulukuu | 1 000                     |

## <a name="example-3-transactions--dynamic-period-forecast-reduction-principle"></a>Esimerkki 3: Tapahtumat-dynaaminen kausi Vähennysperiaate ennuste
Useimmiten järjestelmät on määritetty siten, että tapahtumat vähentävät kysynnän ennustetta määritetyillä ennustekausilla: viikkoina, kuukausina ja niin edelleen. Nämä kaudet vähennysavaimeen. Kahden kysynnän ennusterivin välinen aika voi kuitenkin myös *vihjata* tiettyyn kauteen.

1.  Luo kysynnän ennuste seuraaville päivämäärille ja määrille.
    | Päivämäärä       | Kysynnän ennuste |
    |------------|-----------------|
    | 1. tammikuuta  | 1 000           |
    | 5. tammikuuta  | 500             |
    | 12. tammikuuta | 1 000           |

    Tässä ennusteessa ennustepäivämäärien välillä ei ole selvää jaksoa. Ensimmäisen ja toisen päivämäärän välissä on neljä päivää ja toisen sekä kolmannen päivämäärän välissä seitsemän päivää. Nämä eri aikavälit ovat dynaamisia kausia.
2.  Luo myyntitilausrivit seuraavasti.
    | Päivämäärä                             | Myyntitilauksen määrä |
    |----------------------------------|----------------------|
    | 15. joulukuuta edellisenä vuonna | 500                  |
    | 3. tammikuuta                        | 100                  |
    | 10. tammikuuta                       | 200                  |

Ennustetta vähennetään seuraavasti:

-   Ensimmäinen myyntitilaus ei ole millään kaudella, joten se ei vähennä mitään ennustetta.
-   Toinen myyntitilaus on 1.–5. tammikuuta, joten se vähentää tammikuun 1. päivän ennustetta 100:lla.
-   Kolmas myyntitilaus on 5.–12. tammikuuta, joten se vähentää tammikuun 5. päivän 200:lla.

Ennusteen täyttämiseksi luodaan seuraava suunniteltu tilaus.

| Kysynnän ennusteen päivämäärä | Vähennetty määrä |
|----------------------|------------------|
| 1. tammikuuta            | 900              |
| 5. tammikuuta            | 300              |
| 12. tammikuuta           | 1 000            |

Seuraavassa on yhteenveto **Tapahtumat - dynaaminen kausi** -vähennyksestä:

-   Ennustetarvetta vähentävät dynaamisella kaudella tapahtuvat toteutuneet tilaustapahtumat Dynaaminen kausi kattaa nykyiset ennustepäivämäärät ja päättyy seuraavan ennusteen alkuun.
-   Tämä menetelmä ei käytä tai edellytä vähennysavainta.
-   Kun tätä vaihtoehtoa käytetään, tapahtuu seuraavaa:
    -   Jos ennuste vähenee kokonaan, nykyisen ennusteen ennustetarpeiksi tulee nolla.
    -   Jos tulevaa ennustetta ei ole, vähennetään edellisen syötetyn ennusteen ennustetarpeita.
    -   Ennusteen vähennyslaskentaan sisällytetään aikarajat.
    -   Ennusteen vähennyslaskentaan sisällytetään positiiviset päivät.
    -   Jos toteutuneet tilaustapahtumat ylittävät ennustetarpeet, jäljelle jääviä tapahtumia ei siirretä seuraavalle ennustekaudelle.


<a name="see-also"></a>Lisätietoja
--------

[Master plans](master-plans.md)


