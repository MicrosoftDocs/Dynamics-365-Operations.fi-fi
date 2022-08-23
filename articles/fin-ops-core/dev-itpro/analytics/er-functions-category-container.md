---
title: Luettelo säilöluokan ER-funktioista
description: Tässä artikkelissa on tietoja sähköisen raportoinnin (ER) tukemista säilöfunktioista.
author: kfend
ms.date: 12/14/2020
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: 10.0.17
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: f07c3645f824fc2fe8ca156c8cf06840e993a9a5
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9282648"
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
