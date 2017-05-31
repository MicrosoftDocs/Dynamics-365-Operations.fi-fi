---
title: Laske materiaalin kulutus
description: "Tässä artikkelissa on tietoja eri asetuksista, jotka liittyvät materiaalikulutuksen laskemiseen."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BOMDesignerEditBOM, BOMTable, ProdBOM
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 53401
ms.assetid: 9cff88e4-0425-4707-9178-3c2cb10df7c2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 1bd3168e80719c86e9a0541200fdb1608410c8f5
ms.contentlocale: fi-fi
ms.lasthandoff: 05/25/2017


---

# <a name="calculate-material-consumption"></a>Laske materiaalin kulutus

[!include[banner](../includes/banner.md)]


Tässä artikkelissa on tietoja eri asetuksista, jotka liittyvät materiaalikulutuksen laskemiseen. 

Käytettävissä ovat seuraavat materiaalikulutuksen laskemiseen liittyvät vaihtoehdot, jotka ovat saatavilla **Tuoterakenne**-sivun **Rivin tiedot** -pikavälilehden **Asetukset**- ja **Vaihekulutus**-välilehdillä.

## <a name="variable-and-constant-consumption"></a>Muuttuva ja kiinteä kulutus
**Kulutus on** -kentässä voit valita, onko kulutus laskettava vakiomääränä vai vaihtelevana määränä. Valitse **Vakio**, jos tuotannolle tarvitaan kiinteä määrä tai volyymi tuotetusta määrästä riippumatta. Valitse **Muuttuva**, joka on oletusarvo, jos tarvittava valmiiden tuotteiden määrä on suhteellinen tuotettavien tavaroiden valmiiseen määrään nähden.

## <a name="calculating-consumption-from-a-formula"></a>Kulutuksen laskeminen kaavalla
Voit määrittää **Kaava**-kenttään useita kaavoja materiaalikulutuksen laskentaan. Jos käytät oletusarvoa, joka on **Vakio**, kulutusta ei lasketa kaavalla. Seuraavia kaavoja voi käyttää **Korkeus**-, **Leveys**-, **Syvyys**-, **Tiheys**- ja **Vakio**-kenttien kanssa:

-   Korkeus \* Vakio
-   Korkeus \* Leveys \* Vakio
-   Korkeus \* Leveys \* Syvyys \* Vakio
-   (Korkeus \* Leveys \* Syvyys / Tiheys) \* Vakio

## <a name="rounding-up-and-multiples"></a>Pyöristäminen ja kerrannaiset
**Pyöristys**- ja **Kerrannaiset**-kenttien avulla voit pyöristää materiaalikulutuksen arvon. Voit esimerkiksi pyöristää sen materiaalin käsittely-yksikön arvon mukaan, jossa raaka-aineet poimitaan tuotantoon. **Pyöristys**-kentässä voit käyttää seuraavia asetuksia: **Määrä**, **Mittaus**, ja **Kulutus**.

### <a name="quantity"></a>Määrä

Jos valitset pyöristysmekanismiksi **Määrän**, määrän on oltava määritetyn määrän kerrannainen. Jos esimerkiksi tarvitaan kokonaislukuja, valitse **Kerrannaiset**-kenttään **1**. Luvut pyöristetään sitten määrään, joka on 1:llä jaollinen.

### <a name="measurement"></a>Mittaus

Tavallisesti voit valita **Mittauksen** pyöristysmekanismiksi, kun raaka-aineet saapuvat tietyissä mitoissa. Lopputuotteeseen vaaditaan esimerkiksi 2 metrin metalliputkea, ja metalliputki varastoidaan 4,5 metrin mittaisena. Tässä tapauksessa **Mittausta** voi käyttää pyöristysmekanismina laskemaan, kuinka monta metalliputkea tarvitaan tietyn määrän lopputuotteita valmistamiseen. Tässä esimerkissä **Kaavan** -kentän arvo on **Korkeus \* Vakio**. **Korkeus** -kentän arvo on **2** ilmaisemaan putken pituuden, joka vaaditaan valmiissa tuotteessa. **Kerrannainen**-kentän arvoksi tulee **4,5** osoittamaan, että putkea voi keräillä 4,5 metrin mittaisena. Laskenta näyttää tältä:

1.  Kerrannaisten summa, joka tarvitaan 10:een lopputuotteeseen: 10 ÷ 2 = 5 osaa
2.  Kokonaiskulutus: 4,5 x 5 = 22,5 metriä metalliputkea

Oletamme, 0,5 metriä putkea menee hävikkiin jokaista viittä kulutettua putken osaa kohden.

### <a name="consumption"></a>Kulutus

Tavallisesti valitset **Kulutuksen** pyöristysmekanismiksi, kun raaka-aine on keräiltävä kokonaisina määrinä tietystä tuotteen materiaalin käsittely-yksiköstä. Esimerkiksi 2 litraa maalia käytetään yhden lopputuotekappaleen tuottamiseen, ja maali on keräiltävä 25 litran purkeissa. Tässä tapauksessa **Kulutus**-pyöristysmekanismia voi käyttää pyöristämään kulutus kokonaisiin 25 litran maalipurkkeihin. Tässä ovat laskutoimitukset maalin määrälle, joka tarvitaan 180 lopputuotekappaleen tuottamiseen:

1.  Vaadittu maalin määrä ilman hävikkiä: 180 x 2 = 360 litraa
2.  Maalipurkkien määrä: 360 ÷ 25 = 14,4, joka pyöristetään 15:een
3.  Vaadittu maalin määrä, hävikki mukaan lukien: 15 x 25 = 375 litraa

## <a name="step-consumption"></a>Vaihekulutus
Vaihekulutusta käytetään määrävälien vakiokulutuksen laskennassa. Jos valitset **Vaihekulutus**-asetuksen **Kaava**-kentän arvoksi **Asetukset**-välilehdessä, voit lisätä tietoja vaiheista **Vaihekulutus**-välilehdellä. Kiinteä kulutettu määrä on mahdollista asettaa väleittäin tuotetun määrän mukaan. Vaihdekulutuksen voi esimerkiksi asettaa seuraavan taulukon mukaiseksi.

| Sarjasta | Määrä |
|-------------|----------|
| 0,00        | 10,0000  |
| 100,00      | 20,0000  |
| 200,00      | 40,0000  |

Tuoterakenteen määrä on 1 ja tuotannon määrä 110. Kulutuksen laskentakaava on Sarjasta (Määrä) = Kulutus. Koska tuotannon määrä on 110, se kuuluu "100-sarjaan". Määrä on siis 20.




