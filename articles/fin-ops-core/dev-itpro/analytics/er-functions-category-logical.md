---
title: Luettelo ER-funktioista loogisessa luokassa
description: Tässä ohjeaiheessa on tietoja sähköisen raportoinnin (ER) tukemista loogisista funktioista.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 408b3c5ec37b24e0ccf6e368012a936701eedf0f
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916634"
---
# <a name="list-of-er-functions-in-the-logical-category"></a>Luettelo ER-funktioista loogisessa luokassa

[!include [banner](../includes/banner.md)]

Sähköisten raportointitoimintojen loogisia funktioita voidaan käyttää loogisten arvojen tekemiseen, jotta voit suorittaa useamman kuin yhden vertailun yksittäisessä lausekkeessa tai testata useita ehtoja. Tässä aiheessa on yhteenveto näistä funktioista.

## <a name="list-of-supported-functions"></a>Luettelo tuetuista toiminnoista

| Toiminto | Kuvaus |
|----------|-------------|
| [Ja](er-functions-logical-and.md)                       | Tämä funktio palauttaa *totuusarvon* **TOSI**, jos kaikki määritetyt ehdot toteutuvat. Muussa tapauksessa se palauttaa *totuusarvon* **EPÄTOSI**. |
| [Laatikko](er-functions-logical-case.md)                     | Tämä funktio arvioi määritetyn lausekkeen arvon määritettyjen vaihtoehtoisten asetusten mukaan ja palauttaa ensimmäisen vaihtoehdon tuloksen, joka on yhtä suuri kuin määritetyn lausekkeen arvo. Muussa tapauksessa se palauttaa valinnaisen oletustuloksen, jos oletustulos määritetään kutsutussa funktiossa viimeisenä argumenttina, jota ei edellä vaihtoehto. Palautettava arvo voi olla minkä tahansa tuettujen tietotyyppien arvo. |
| [Jos](er-functions-logical-if.md)                         | Tämä funktio palauttaa ensimmäisen määritetyn arvon, jos määritetyt ehdot täyttyvät. Muussa tapauksessa se palauttaa toisen määritetyn arvon. Palautettava arvo voi olla minkä tahansa tuettujen tietotyyppien arvo. |
| [Ei](er-functions-logical-not.md)                       | Tämä funktio palauttaa määritetyn ehdon käänteisen loogisen arvon *totuusarvoksi*. |
| [Or](er-functions-logical-or.md)                         | Tämä funktio palauttaa *totuusarvon* **EPÄTOSI**, jos mikään määritetty ehto ei toteudu. Jos joku määritetty ehto toteutuu, tämä funktio palauttaa *totuusarvon* **TOSI**. |
| [ValueIn](er-functions-logical-valuein.md)               | Tämä funktio määrittää, vastaako määritetty syöte määritetyn luettelokohteen tiettyä arvoa. Se palauttaa *totuusarvon* arvon **TOSI**, jos määritetty syöte vastaa määritetyn lausekkeen suorittamisen tulosta vähintään yhdelle määritetyn luettelon tietueelle. Muussa tapauksessa se palauttaa *totuusarvon* **EPÄTOSI**. |

## <a name="additional-resources"></a>Lisäresurssit

[Sähköisen raportoinnin yleiskatsaus](general-electronic-reporting.md)

[Sähköisen raportoinnin kaavojen suunnittelutoiminto](general-electronic-reporting-formula-designer.md)

[Sähköisen raportoinnin kaavakieli](er-formula-language.md)