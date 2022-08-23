---
title: Luettelo ER-funktioista tietojenkeräysluokassa
description: Tässä artikkelissa on tietoja sähköisen raportoinnin (ER) tukemista tietojenkeräysfunktioista.
author: kfend
ms.date: 12/04/2019
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: e01bed49646ffe344004f9eb51e9013e1b4c5430
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9286146"
---
# <a name="list-of-er-functions-in-the-data-collection-category"></a>Luettelo ER-funktioista tietojenkeräysluokassa

[!include [banner](../includes/banner.md)]

Sähköisen raportoinnin (ER) tiedonkeruufunktioita käytetään suorittamaan laskenta ja summaus ER-muodossa, joka suoritetaan perustuen tietoihin, jotka on jo luotu **teksti**- tai **XML**-muodossa. Tätä lähestymistapaa käytetään parantamaan suoritettavan ER-muodon suorituskykyä, syöttämään arvojen juoksevat summat luotaviin asiakirjoihin ja muihin tarkoituksiin. Tässä artikkelissa on yhteenveto näistä funktioista.

## <a name="list-of-supported-functions"></a>Luettelo tuetuista toiminnoista

| Toiminto | Kuvaus |
|----------|-------------|
| [CollectedList](er-functions-datacollection-collectedlist.md) | Tämä funktio palauttaa *Tietueluettelon* arvon, joka sisältää luettelon arvoista, jotka on palautettu **kerättyjen tietojen avainarvo** -ominaisuuden muotoelementeistä ja kerätty, kun muotoelementtejä käytettiin lähtevän asiakirjan luomiseen muotoajon aikana ja jotka täyttävät määritetyt ehdot. Jokainen ehto muodostuu avainalueesta ja avainarvosta. |
| [CountIF](er-functions-datacollection-countif.md) | Tämä funktio palauttaa *Kokonaislukuarvon*, joka vastaa niiden muotoelementtien määrää, jotka kerättiin, kun muotoelementtejä käytettiin lähtevän asiakirjan luomiseen muotoajon aikana ja joka täyttää määritetyn ehdon. Ehto muodostuu avainalueesta ja avainarvosta. |
| [CountIFs](er-functions-datacollection-countifs.md) | Tämä funktio palauttaa *Kokonaislukuarvon*, joka vastaa niiden muotoelementtien määrää, jotka kerättiin, kun muotoelementtejä käytettiin lähtevän asiakirjan luomiseen muotoajon aikana ja joka täyttää määritetyt ehdot. Jokainen ehto muodostuu avainalueesta ja avainarvosta. |
| [FormatElementName](er-functions-datacollection-formatelementname.md) | Tämä funktio palauttaa *Merkkijonoarvon*, joka edustaa nykyisen ER-muodon elementin nimeä. |
| [SumIF](er-functions-datacollection-sumif.md) | Tämä funktio palauttaa *Todellisen* arvon, joka on niiden arvojen summa, jotka palautettiin muotoiluelementtien sitomisella ja, jotka kerättiin, kun muotoelementtejä käytettiin lähtevän asiakirjan luomiseen muotoajon aikana ja joka täyttää määritetyn ehdon. Ehto muodostuu avainalueesta ja avainarvosta. |
| [SumIFs](er-functions-datacollection-sumifs.md) | Tämä funktio palauttaa *Todellisen* arvon, joka on niiden arvojen summa, jotka palautettiin muotoiluelementtien sitomisella ja, jotka kerättiin, kun muotoelementtejä käytettiin lähtevän asiakirjan luomiseen muotoajon aikana ja joka täyttää määritetyt ehdot. Jokainen ehto muodostuu avainalueesta ja avainarvosta. |

## <a name="additional-resources"></a>Lisäresurssit

[Sähköisen raportoinnin yleiskatsaus](general-electronic-reporting.md)

[Sähköisen raportoinnin kaavojen suunnittelutoiminto](general-electronic-reporting-formula-designer.md)

[Sähköisen raportoinnin kaavakieli](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
