---
title: DAYS ER -funktio
description: Tässä artikkelissa on tietoja siitä, miten sähköisen raportoinnin (ER) DAYS-funktiota käytetään.
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
ms.openlocfilehash: a0c50e36bbf0c2bd999a17631e3e00d2feb162fd
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9268722"
---
# <a name="days-er-function"></a>DAYS ER -funktio

[!include [banner](../includes/banner.md)]

`DAYS`-funktio palauttaa ensimmäisen määritetyn päivämäärän ja toisen määritetyn päivämäärän välisten päivien määrää kuvaavan arvon *kokonaislukuna*.

## <a name="syntax"></a>Syntaksi

```vb
DAYS (date 1, date 2) as Integer
```

## <a name="arguments"></a>Argumentit

`date 1`: *Päivämäärä*

Päivämääräarvo, joka ilmaisee päivien määrän laskennassa käytettävää aloituspäivämäärää.

`date 2`: *Päivämäärä*

Päivämääräarvo, joka ilmaisee päivien määrän laskennassa käytettävää lopetuspäivämäärää.

## <a name="return-values"></a>Palautusarvot

*Kokonaisluku*

Tuloksena oleva numeroarvo.

## <a name="usage-notes"></a>Käyttöhuomautukset

`DAYS`-funktio palauttaa positiivisen arvon, kun ensimmäinen päivämäärä on myöhemmin kuin toinen päivämäärä, se palauttaa arvon **0** (nolla), kun ensimmäinen päivämäärä on sama kuin toinen päivämäärä ja palauttaa negatiivisen arvon, kun ensimmäinen päivämäärä on aikaisempi kuin toinen päivämäärä.

## <a name="example"></a>Esimerkki

`DAYS (TODAY (), DATEVALUE( DATETIMEFORMAT( ADDDAYS ( NOW(), 1), "yyyyMMdd"), "yyyyMMdd"))` returns **-1**.

## <a name="additional-resources"></a>Lisäresurssit

[Päivämäärä- ja aikatoiminnot](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
