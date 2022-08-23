---
title: Tilausten nopea tekeminen B2B-verkkosivustolla
description: Tässä artikkelissa kuvataan Microsoft Dynamics 365 Commercen ominaisuudet, joiden avulla yritysten välisten (B2B) sivustojen käyttäjät voivat tehdä joukkotilauksia ja toistuvia tilauksia nopeasti.
author: ShalabhjainMSFT
ms.date: 02/16/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: shajain
ms.search.validFrom: 2022-01-31
ms.dyn365.ops.version: 10.0.23
ms.search.industry: retail
ms.search.form: RetailOperations
ms.openlocfilehash: a153be1da43b63e8d29d6ece3dcbf47d5bbec487
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9275117"
---
# <a name="place-b2b-website-orders-quickly"></a>Tilausten nopea tekeminen B2B-verkkosivustolla

[!include [banner](../../includes/banner.md)]

Tässä artikkelissa kuvataan Microsoft Dynamics 365 Commercen ominaisuudet, joiden avulla yritysten välisten (B2B) sivustojen käyttäjät voivat tehdä joukkotilauksia ja toistuvia tilauksia nopeasti.

Dynamics 365 Commercen B2B-verkkokauppasivustot sallivat käyttäjien suorittaa vakiotoimintoja, kuten uusien tuotteiden löytämistä etsimällä ja selailemalla, tuotetietojen tarkastelemista, nimikkeiden koriin laittamista ja uloskuittausta. Yritysten ja kuluttajien välisten (B2C) sivustojen asiakkaat kuitenkin yleensä tilaavat pieniä nimikemääriä vain kerran, kun taas B2B-asiakkaat yleensä tilaavat suuria nimikemääriä toistuvasti. Koska nämä asiakkaat tietävät yleensä tarkalleen, mitä nimikkeitä he haluavat ostaa, he ohittavat usein tuotteenetsinnän ja siirtyvät suoraan tilaamiseen. Vastatakseen asiakkaidensa tarpeisiin Commercen B2B-verkkokaupoissa on useita ominaisuuksia, jotka mahdollistavat nopeat tilaukset.

## <a name="bulk-order-by-item-number"></a>Joukkotilaus nimikenumeron perusteella

Commercen B2B-verkkokauppasivustoilla käyttäjät voivat lisätä nimikkeitä koriin syöttämällä tuotteiden nimikenumeroita yhdessä halutun määrän kanssa.

Seuraavassa kuvassa on esimerkki nopeasta tilauksen syöttämisestä tuotteen nimikenumeron perusteella.

![Nopea tilauksen syöttäminen tuotteen nimikenumeron perusteella.](../media/QuickAddByItem.png)

## <a name="bulk-order-by-variant"></a>Joukkotilaus variantin mukaan

Commercen B2B-verkkokauppasivustoilla käyttäjät voivat lisätä nopeasti saman tuotteen eri variantteja yksittäisessä näkymässä, jossa näkyy varaston saatavuus koon, värin ja tyylin mukaan. Lisäksi sivuston käyttäjät voivat helposti syöttää saman määrän kaikille varastossa oleville tuotteille valitsemalla **Syötä kaikki määrät**.

Seuraavassa kuvassa on esimerkki nopeasta tilauksen syötöstä, jossa käytetään kaikkien määrien syötön toimintoa.

![Nopea tilauksen syöttö, jossa käytetään kaikkien määrien syötön toimintoa.](../media/MatrixView.png)

## <a name="use-order-templates-for-quick-order-entry"></a>Tilausmallien käyttö nopeaan tilauksen syöttöön

B2B-verkkosivustojen ostajat tilaavat usein tiettyjä nimikkeitä yhdessä. Jos esimerkiksi tekee tilauksia rakennustyömaata varten, saattaa tilata paitoja, takkeja, housuja, kenkiä ja lakkeja yhdessä. Jos tekee tilauksia sairaaloille, joissa lääkäreillä, sairaanhoitajilla ja puhtaanapitohenkilöstöllä on erilaiset työvaatteet, voi olla käytännöllistä ryhmitellä kukin työvaatekokonaisuus yhteen helpompaa tilausta varten. Tällaisia skenaarioita varten Commercen B2B-sivustot mahdollistavat tilausmallien luomisen. Sivuston käyttäjät voivat luoda kuinka monta mukautettua mallia tahansa ja tilata sitten kaikki mallien nimikkeet tai osan niistä tarpeen mukaan.

Seuraavassa kuvassa on esimerkki tilausmallista.

![Esimerkki tilausmallista.](../media/OrderTemplateHeader.png)

Seuraavassa kuvassa on esimerkki tilausmallin tietonäkymästä.

![Esimerkki tilausmallin tietonäkymästä.](../media/OrderTemplateLines.png)

## <a name="reorder-from-order-history"></a>Uudelleentilaus tilaushistoriasta

Commercen B2B-verkkokauppasivustoilla käyttäjät voivat tilata nimikkeitä nopeasti uudelleen tilaushistoriastaan. Sivuston käyttäjät voivat joko ostaa valikoituja nimekkeitä tilaushistoriastaan tai lisätä kaikki aiemmin ostetut esineet koriin.

Seuraavassa kuvassa on esimerkki käyttäjän tilaushistoriasta ja asetukset nimikkeiden uudelleentilaamiseen siitä.

![Uudelleentilaus tilaushistoriasta.](../media/Reorder.png)

Tässä artikkelissa on kuvattu vain joitakin tapoja, joilla Commercen B2B-sivustot auttavat käyttäjiä löytämään, tilaamaan ja tilaamaan uudelleen haluamiaan tuotteita. Joukkotilausten taltioinnin yksinkertaistamiseksi edelleen on kehitteillä lisää ominaisuuksia.
