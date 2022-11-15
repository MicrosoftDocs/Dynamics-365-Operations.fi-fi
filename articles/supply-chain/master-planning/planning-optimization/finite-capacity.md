---
title: Rajallisen kapasiteetin suunnittelu ja ajoitus
description: Rajallisen kapasiteetin suunnittelun ja ajoituksen avulla saat lisätietoja siitä, miten paljon työtä voidaan tehdä tiettynä ajanjaksona, kun eri resurssien rajoitukset otetaan huomioon.
author: t-benebo
ms.date: 09/19/2022
ms.topic: article
ms.search.form: ReqParameters, ReqPlanSched, WrkCtrTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2022-09-19
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: 5f02ec58c88cfd0d663a97de4e3e4dff1cdd5e90
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740083"
---
# <a name="finite-capacity-planning-and-scheduling"></a>Rajallisen kapasiteetin suunnittelu ja ajoitus

[!include [banner](../../includes/banner.md)]
[!INCLUDE [preview-banner](../../includes/preview-banner.md)]
<!--KFM: Preview until 10.0.31 GA -->

Rajallinen kapasiteetti -ominaisuuden avulla saat lisätietoja siitä, miten paljon työtä voidaan tehdä tiettynä ajanjaksona, kun eri resurssien rajoitukset otetaan huomioon. Rajallisen kapasiteetin ajoituksen tarkoitus on varmistaa, että työ etenee tasaiseen tahtiin ja tehokkaasti koko tehtaassa.

Rajallisen kapasiteetin suunnittelu ja ajoitus luo tuotantoprosesseille realistisemman aikataulun kuin ääretön latausmenetelmä. Jos resursseilla ei ole tarpeeksi kapasiteettia, toimituspäivämäärää siirretään kauemmaksi tulevaisuuteen ja työ ajoitetaan tehtäväksi sitten, kun kapasiteettia on riittävästi.

> [!NOTE]
> Rajallisen kapasiteetin suunnittelu ja ajoitus toimii lähes samalla tavalla riippumatta siitä, käytätkö suunnittelun optimointia vai vanhentunutta pääsuunnittelumoduulia. Suunnittelun optimointi ei kuitenkaan käytä **pullonkaula-aikarajan** parametria. Kun käytät suunnittelu optimointia, pullonkaularesurssit ajoitetaan aina käyttämällä samaa aikarajaa kuin muissa kuin pullonkaularesursseissa (rajallisen kapasiteetin aikarajan osoittamalla tavalla).

## <a name="set-up-finite-capacity-functionality"></a>Rajallisen kapasiteetin toimintojen määrittäminen

Jos haluat käyttää rajallisen kapasiteetin toimintoja, ota käyttöön kapasiteetin suunnittelu yleisellä tasolla ja rajallisen kapasiteetin suunnittelu sekä pääsuunnitelmalle, jossa sitä käytetään, sekä muille resursseille, jota se koskee. Suunniteltujen tuotantotilausten ajoituksessa otetaan huomioon jo varattu kapasiteetti suunnitelmissa ja resursseissa, joissa rajallinen kapasiteetti on käytössä. Suunnitellut tuotantotilaukset ajoitetaan taaksepäin tarvepäivästä lukien. Jos kapasiteetti ei riitä optimoitua ajoitusta varten, järjestelmä yrittää pyytää komponenttinimikkeitä aiempana päivämääränä. Jos kapasiteettia voidaan muuttaa tarpeiden muuttuessa (esimerkiksi silloin, kun työ on vuorotyötä), rajallisen kapasiteetin toimintoa ei pidä valita, koska lasketut käsittelyajat eivät ole oikeita. Ajoitus ottaa huomioon jo varatun kapasiteetin vain resursseissa, joissa rajallinen kapasiteetti on otettu käyttöön. Kun rajallinen kapasiteetti otetaan käyttöön resurssille, voit muokata rajallisen kapasiteetin aikarajaa.

### <a name="activate-master-planning-parameters"></a>Pääsuunnittelun parametrien aktivoiminen

Voit käyttää rajallisen kapasiteetin toimintoa, jos kapasiteetin suunnittelu on otettu käyttöön **Pääsuunnittelun parametrit** -sivulla.

1. Valitse **Pääsuunnittelu \> Määritys \> Pääsuunnittelun parametrit**.
1. Määritä **Suunnitellut tilaukset** -välilehden **Kapasiteetin suunnittelu** -osan **Tuotanto**-vaihtoehdon arvoksi *Kyllä*.

### <a name="activate-a-master-plan"></a>Pääsuunnitelman aktivoiminen

Rajallisen kapasiteetin suunnittelu ja ajoitus on otettava käyttöön jokaisessa pääsuunnitelmassa, jossa sitä käytetään.

1. Siirry kohtaan **Pääsuunnittelu \> Määritykset \> Suunnitelmat \> Pääsuunnitelmat**.
1. Valitse luetteloruudusta pääsuunnitelma, jonka haluat määrittää käyttämään rajallisen kapasiteetin suunnittelua ja ajoitusta.
1. Määritä **Yleiset**-pikavälilehden **Suunnitellut tuotantotilaukset** -osassa **Rajallinen kapasiteetti** -vaihtoehdon arvoksi *Kyllä*.
1. Toista vaiheet 2 ja 3 jokaiselle pääsuunnitelmalle, jonka haluat määrittää.

### <a name="activate-resources"></a>Resurssien aktivoiminen

Rajallisen kapasiteetin suunnittelu ja ajoitus on otettava käyttöön jokaisessa resurssissa, jossa sitä käytetään.

1. Valitse **Tuotannonhallinta \> Asetukset \> Resurssit \> Resurssit**.
1. Valitse luetteloruudusta resurssi, jonka haluat määrittää käyttämään rajallisen kapasiteetin suunnittelua ja ajoitusta.
1. Määritä **Työvaihe**-pikavälilehden **Kapasiteetti-painike**-osan **Rajallinen kapasiteetti** -vaihtoehdon arvoksi *Kyllä*.
1. Toista vaiheet 2 ja 3 jokaiselle lisäresurssille, jonka haluat määrittää.

## <a name="examples"></a>Esimerkkejä

Tämä osa sisältää seuraavat esimerkit, joissa kerrotaan, miten äärettömän ja rajallisen kapasiteetin suunnittelu ja ajoitus toimii:

- Esimerkki 1 – Äärettömän kapasiteetin suunnittelu
- Esimerkki 2 – Rajallisen kapasiteetin suunnittelu yhden päivän aikarajan avulla
- Esimerkki 3 – Rajallisen kapasiteetin suunnittelu kahden päivän aikarajan avulla

### <a name="preconditions"></a>Ennakkoehdot

Kaikissa kolmessa esimerkissä otetaan huomioon tässä osassa kerrotut ennakkoehdot.

Tuotteella *Tuote1* on reitti, joka sisältää alla mainitut työvaiheet.

| Työvaiheen numero | Työvaiheen nimi | Resurssi        | Ajoaika | Käsittelymäärä | Seuraava |
|---------------|----------------|-----------------|----------|--------------|------|
| 10            | Hitsaus        | Hitsauslinja    | 1        | 2            | 20   |
| 20            | Kokoaminen     | Kokoonpanolinja | 1        | 4            |      |

Yrityksen työntekijät työskentelevät yhdessä kahdeksan tunnin pituisessa vuorossa (8.00–16.00).

Järjestelmässä on ajoitettu tuotantotilaus, joka sisältää *24 pakettia* *tuotetta1*. Toimituspäivä on *tänään + 3 päivää*.

Suunnittelun tuloksena järjestelmä lataa resurssit seuraavasti:

- **Hitsauslinja:** Tämä resurssi latausajankohta on *tänään klo 8.00* – *tänään + 1 klo 12.00*.
- **Kokoonpanolinja:** Tämä resurssi latausajankohta on *tänään + 1 klo 12.00* – *tänään + 2 klo 10.00*.

Seuraavassa kuvassa näkyy tuloksena oleva Gantt-kaavio (valitsemalla sen voit katsella sitä isossa näkymässä).

[![Gantt-kaavio, jossa näkyvät ennakkoehdot.](media/finite-examples-conditions-small.png "Gantt-kaavio, jossa näkyvät ennakkoehdot")](media/finite-examples-conditions.png)

### <a name="example-1--infinite-capacity-planning"></a>Esimerkki 1 – Äärettömän kapasiteetin suunnittelu

Tässä esimerkissä näytetään suunnittelutulokset, kun käytössä on ääretön kapasiteetin suunnittelu rajallisen kapasiteetin suunnittelun sijaan.

Pääsuunnitelmalla on seuraava asiaankuuluva asetus, joka poistaa käytöstä rajallisen kapasiteetin suunnittelun suunnitelmasta:

- **Rajallinen kapasiteetti:** *Ei*

**Rajallinen kapasiteetti** -vaihtoehdon arvoksi määritetään *Ei* myös molemmissa soveltuvissa resursseissa, jotta niiden rajallisen kapasiteetin suunnittelu poistetaan käytöstä seuraavasti:

- Hitsauslinja
- Kokoonpanolinja

Voit nyt lisätä uuden myyntitilauksen, joka sisältää *8 pakettia* *tuotetta1*, ja suorittaa suunnittelun. Tuloksena järjestelmä lataa hitsauslinjan ajalta *tänään klo 8.00* – *tänään klo 12.00*. Kun hitsausrivin työvaiheet on tehty valmiiksi, järjestelmä lataa kokoonpanorivin ajalta *tänään klo 12.00* – *tänään klo 14.00*.

Seuraavassa kuvassa näkyy tuloksena oleva Gantt-kaavio (valitsemalla sen voit katsella sitä isossa näkymässä).

[![Gantt-kaavio, jossa on äärettömän kapasiteetin suunnittelun esimerkki.](media/finite-examples-example1-small.png "Gantt-kaavio, jossa on äärettömän kapasiteetin suunnittelun esimerkki")](media/finite-examples-example1.png)

### <a name="example-2--finite-capacity-planning-with-a-time-fence-of-one-day"></a>Esimerkki 2 – Rajallisen kapasiteetin suunnittelu yhden päivän aikarajan avulla

Tässä esimerkissä näytetään suunnittelutulokset, kun käytössä on rajallisen kapasiteetin suunnittelu ja aikarajana yksi päivä.

Pääsuunnitelmalla on seuraavat asiaankuuluvat asetukset, jotka ottavat käyttöön rajallisen kapasiteetin suunnittelun ja määrittävät aikarajan suunnitelmalle:

- **Rajallinen kapasiteetti:** *Kyllä*
- **Rajallisen kapasiteetin aikaraja:** *1*

**Rajallinen kapasiteetti** -vaihtoehdon arvoksi määritetään *Kyllä* myös molemmissa soveltuvissa resursseissa, jotta niiden rajallisen kapasiteetin suunnittelu otetaan käyttöön seuraavasti:

- Hitsauslinja
- Kokoonpanolinja

Voit nyt lisätä uuden myyntitilauksen, joka sisältää *8 pakettia* *tuotetta1*, ja suorittaa suunnittelun. Tuloksena järjestelmä lataa hitsauslinjan ajalta *tänään + 1 klo 8.00* – *tänään + 1 klo 12.00*. Kun hitsausrivin työvaiheet on tehty valmiiksi, järjestelmä lataa kokoonpanorivin ajalta *tänään + 1 klo 12.00* – *tänään + 1 klo 14.00*. Järjestelmä ottaa huomioon rajallisen kapasiteetin vain yhden päivän ajan.

Seuraavassa kuvassa näkyy tuloksena oleva Gantt-kaavio (valitsemalla sen voit katsella sitä isossa näkymässä).

[![Gantt-kaavio, jossa on rajallisen kapasiteetin suunnittelu yhden päivän aikarajan avulla.](media/finite-examples-example2-small.png "Gantt-kaavio, jossa on rajallisen kapasiteetin suunnittelu yhden päivän aikarajan avulla")](media/finite-examples-example2.png)

### <a name="example-3--finite-capacity-planning-with-a-time-fence-of-two-days"></a>Esimerkki 3 – Rajallisen kapasiteetin suunnittelu kahden päivän aikarajan avulla

Tässä esimerkissä näytetään suunnittelutulokset, kun käytössä on rajallisen kapasiteetin suunnittelu ja aikarajana kaksi päivää.

Pääsuunnitelmalla on seuraavat asiaankuuluvat asetukset, jotka ottavat käyttöön rajallisen kapasiteetin suunnittelun ja määrittävät aikarajan suunnitelmalle:

- **Rajallinen kapasiteetti:** *Kyllä*
- **Rajallisen kapasiteetin aikaraja:** *2*

**Rajallinen kapasiteetti** -vaihtoehdon arvoksi määritetään *Kyllä* myös molemmissa soveltuvissa resursseissa, jotta niiden rajallisen kapasiteetin suunnittelu otetaan käyttöön seuraavasti:

- Hitsauslinja
- Kokoonpanolinja

Voit nyt lisätä uuden myyntitilauksen, joka sisältää *8 pakettia* *tuotetta1*, ja suorittaa suunnittelun. Tuloksena järjestelmä lataa hitsauslinjan ajalta *tänään + 1 klo 12.00* – *tänään + 1 klo 16.00*. Kun hitsausrivin työvaiheet on tehty valmiiksi, järjestelmä lataa kokoonpanorivin ajalta *tänään + 2 klo 8.00* – *tänään + 2 klo 10.00*. Järjestelmä ottaa huomioon rajallisen kapasiteetin vain kahden päivän ajan.

Seuraavassa kuvassa näkyy tuloksena oleva Gantt-kaavio (valitsemalla sen voit katsella sitä isossa näkymässä).

[![Gantt-kaavio, jossa on rajallisen kapasiteetin suunnittelu kahden päivän aikarajan avulla.](media/finite-examples-example3-small.png "Gantt-kaavio, jossa on rajallisen kapasiteetin suunnittelu kahden päivän aikarajan avulla")](media/finite-examples-example3.png)

> [!IMPORTANT]
> Määritä aina rajallisen kapasiteetin aikaraja vaadittavalla tavalla, jotta liiketoiminnan tarpeet täytetään. Tämän artikkelin esimerkit on tarkoitettu vain toimintojen kuvaamiseen. Todellisuudessa yhden päivän aikaraja on todennäköisesti liian lyhyt useimmille valmistajille, jotka käyttävät rajallisen kapasiteetin suunnittelua.
