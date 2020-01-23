---
title: NUMBERFORMAT ER-funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) NUMBERFORMAT-funktiota käytetään.
author: NickSelin
manager: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: 392135abaf7db05d5ac591ab56312a0e0f6ae5ff
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916795"
---
# <a name="NUMBERFORMAT">NUMBERFORMAT ER-funktio</a>

[!include [banner](../includes/banner.md)]

`NUMBERFORMAT`-funktio palauttaa *Merkkijonoarvon*, joka edustaa määritetyn numeron määritetyssä muodossa ja valinnaisesti määritetyssä [kulttuurissa](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes). Lisätietoja tuetuista muodoista on kohdassa [vakio](https://msdn.microsoft.com/library/dwhawy9k(v=vs.110).aspx) ja [mukautettu](https://msdn.microsoft.com/library/0c899ak8(v=vs.110).aspx).

## <a name="syntax-1"></a>Syntaksi 1

```
NUMBERFORMAT (number, format)
```

## <a name="syntax-2"></a>Syntaksi 2

```
NUMBERFORMAT (number, format, culture)
```

## <a name="arguments"></a>Argumentit

`number`: *Kokonaisluku* tai *Todellinen*

Numeerinen arvo, joka määrittää muotoiltava lukumäärän.

`format` : *Merkkijono*

*Merkkijono*-arvo, joka esittelee alkuperäisen muodon.

`culture`: *Merkkijono*

*Merkkijono*-arvo, joka edustaa muotoilussa käytettävää kulttuuria.

## <a name="return-values"></a>Palautusarvot

*merkkijono*

Tulokseksi saatava tekstiarvo.

## <a name="usage-notes"></a>Käyttöhuomautukset

Jos kulttuuria ei ole määritetty kutsuttujen funktioiden argumentiksi, sen konteksti, jossa tämä funktio suoritetaan, määrittää lukujen muotoilussa käytettävän kulttuurin.

## <a name="example-1"></a>Esimerkki 1

Jos maa-asetukset ovat **EN-US**, `NUMBERFORMAT (0.45, "p")` palauttaa arvon **45.00 %** ja `NUMBERFORMAT (10.45, "#")` palauttaa arvon **10**.

## <a name="example-2"></a>Esimerkki 2

`NUMBERFORMAT (10/3, "F2", "de")`-funktio palauttaa arvon **3,33**, kun `NUMBERFORMAT (10/3, "F2", "en-us")` palauttaa arvon **3.33**.

## <a name="additional-resources"></a>Lisäresurssit

[Tekstitoiminnot](er-functions-category-text.md)