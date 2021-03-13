---
title: Pikanäkymämoduuli
description: Tässä ohjeaiheessa on tietoja pikanäkymämoduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.
author: anupamar-ms
manager: annbe
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2020-01-08
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 7e8244a06c515029b559b2061d9a25c7355e9e14
ms.sourcegitcommit: 872600103d2a444d78963867e5e0cdc62e68c3ec
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/01/2021
ms.locfileid: "5097049"
---
# <a name="quick-view-module"></a>Pikanäkymämoduuli

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Tässä ohjeaiheessa on tietoja pikanäkymämoduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.

Pikanäkymämoduulin avulla käyttäjät voivat tarkastella nopeasti tuotetietoja, kun he selaavat tuotteita luettelosivulla, ja lisätä tuotteen tai tuotteita luettelosivulta ostoskoriin, tarvitsematta siirtyä tuotetietosivulle (PDP). Pikanäkymämoduuli sisältää yhteenvedon tuotetietoista, joita käyttäjät tarvitsevat Lisää ostoskoriin -päätöksen tekemistä varten. Lisäksi siinä on linkki tuotetietosivulle, jotta käyttäjät voivat tarkastella lisätuotetietoja ja ostovaihtoehtoja.

[Tuotekokoelma](product-collection-module-overview.md)- ja [Hakutulokset](search-result-module.md)-moduulit tukevat pikanäkymämoduulia.

> [!IMPORTANT]
> Pikanäkymämoduuli on käytettävissä Commerce 10.0.17 -versiosta eteenpäin.

Seuraavassa kuvassa on esimerkki pikanäkymämoduulista tuoteluettelosivulla.

![Esimerkki pikanäkymämoduulista tuoteluettelosivulla](./media/ecommerce-quickview.PNG)

## <a name="module-properties"></a>Moduulin ominaisuudet

Pikanäkymämoduuli tukee joitakin samoja toimintoja kuin ostoruutumoduuli. Siksi pikanäkymämoduulin ominaisuudet muistuttavat ostoruutumoduulin ominaisuuksia.

| Ominaisuus | Arvot | kuvaus |
|----------------|--------|-------------|
| Otsikon tunniste | **H1**, **H2**, **H3**, **H4**, **H5** tai **H6** | Tämä ominaisuus määrittää tuoteotsikon otsikon tunnisteen. Jos pikanäkymämoduuli on sivun yläosassa, helppokäyttöisyysstandardit täyttyvät, kun tämän ominaisuuden arvona on **H1**. |
| Salli mukautettu hinta | **Tosi** vai **Epätosi** | Jos ominaisuuden arvoksi määritetään **Tosi**, käyttäjä voi määrittää mukautetun hinnan. |
| Vähimmäishinta | Kokonaisluku | Tämä ominaisuus on käytettävissä vain, jos **Salli mukautettu hinta** -ominaisuuden arvoksi on määritetty **Tosi**. Se määrittää vähimmäishinnan, jonka käyttäjä voi syöttää (esimerkiksi 1 $). |
| Enimmäishinta | Kokonaisluku | Tämä ominaisuus on käytettävissä vain, jos **Salli mukautettu hinta** -ominaisuuden arvoksi on määritetty **Tosi**. Se määrittää enimmäishinnan, jonka käyttäjä voi syöttää (esimerkiksi 1 000 $). |

## <a name="commerce-site-builder-settings"></a>Commercen sivustonmuodostimen asetukset

Kuten ostoruutumoduuli, pikanäkymämoduuli noudattaa asetuksia kohdassa **Sivuston asetukset \> Laajennukset \> Lisää tuote ostoskoriin**. **Siirry ostoskorisivulle** -asetus kuitenkin ohitetaan, koska se on ristiriidassa pikanäkymämoduulin tarkoituksen kanssa. Näin käyttäjät voivat selata useita tuotteita luettelosivulla ja lisätä niitä kärryynsä siirtymättä pois luettelosivulta.

## <a name="add-a-quick-view-module-to-a-product-collection-module"></a>Pikanäkymämoduulin lisääminen kokoelmamoduuliin

Pikanäkymämoduuli voidaan lisätä Tuotekokoelma- ja Hakutulokset-moduuleihin.

Voit lisätä pikanäkymämoduulin tuotekokoelmamoduuliin Commercen sivustonmuodostimessa seuraavasti.

1. Siirry kohtaan **Sivut** ja valitse Fabrikam-sivuston aloitussivu.
1. Siirry mihin tahansa kotisivun **Tuotekokoelma**-moduuliin, valitse kolmepistettä (**...**) ja valitse sitten **Lisää moduuli**.
1. Valitse **Lisää moduuli** -valintaikkunassa **Pikanäkymä**-moduuli ja valitse sitten **OK**.
1. Valitse **Pikanäkymä**-moduulin ominaisuusruudusta **Otsikko**. Määritä **Otsikko**-valintaikkunassa **Otsikkotaso**-kentän arvoksi **H2** ja valitse sitten **OK**.
1. Valitse **Tallenna**, valitse **Viimeistele muokkaus** tarkistaaksesi sivun, ja julkaise se valitsemalla **Julkaise**.

## <a name="additional-resources"></a>Lisäresurssit

[Moduulikirjaston yleiskatsaus](starter-kit-overview.md)

[Ostoruutumoduuli](add-buy-box.md)

[Tuotekokoelmamoduuli](product-collection-module-overview.md)

[Hakutulosmoduuli](search-result-module.md)
