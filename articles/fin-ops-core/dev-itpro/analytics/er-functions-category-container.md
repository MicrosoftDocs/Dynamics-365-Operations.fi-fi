---
title: Luettelo säilöluokan ER-funktioista
description: Tässä artikkelissa on tietoja sähköisen raportoinnin (ER) tukemista säilöfunktioista.
author: NickSelin
ms.date: 12/14/2020
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 5c86b0ae6cbf4ac6515491b55390d42c371eae4b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8883814"
---
# <a name="list-of-er-functions-in-the-container-category"></a>Luettelo säilöluokan ER-funktioista

[!include [banner](../includes/banner.md)]

[Sähköisen raportoinnin (ER)](general-electronic-reporting.md) [säilöfunktioiden](er-formula-language.md#Functions) avulla voidaan suorittaa *Säilö*-tietotyypin tietolähteitä sisältäviä toimintoja. Näitä toimintoja esiintyy, kun käsiteltävät tiedot ilmaisevat BLOB-muotoisten binaaritietojen kokoelman. Tässä artikkelissa on yhteenveto näistä funktioista.

## <a name="list-of-supported-functions"></a>Luettelo tuetuista toiminnoista

| Toiminto | kuvaus |
|----------|-------------|
| [Base64StringToContainer](er-functions-container-base64stringtocontainer.md) | Tämä funktio palauttaa *Säilö*-arvon. Tämä arvo koostuu binaarisisällöstä, jonka koodaus on purettu määritetystä ASCII-merkkijonosta. Tämä merkkijono puolestaan ilmaiseen binaarista tekstiin koodattavien rakenteiden Base64-ryhmän. |

## <a name="additional-resources"></a>Lisäresurssit

[Sähköisen raportoinnin yleiskatsaus](general-electronic-reporting.md)

[Sähköisen raportoinnin kaavojen suunnittelutoiminto](general-electronic-reporting-formula-designer.md)

[Sähköisen raportoinnin kaavakieli](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
