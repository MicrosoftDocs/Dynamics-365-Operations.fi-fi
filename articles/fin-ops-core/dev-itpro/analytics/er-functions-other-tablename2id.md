---
title: TABLENAME2ID ER -funktio
description: Tässä artikkelissa on tietoja siitä, miten sähköisen raportoinnin (ER) TABLENAME2ID-funktiota käytetään.
author: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: fe7ed336f2264e15e0a8a7305e1bcebb75b2cd07
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9268053"
---
# <a name="tablename2id-er-function"></a>TABLENAME2ID ER -funktio

[!include [banner](../includes/banner.md)]

`TABLENAME2ID`-funktio palauttaa määritetyn taulukon nimen numeerisen esityksen taulukon tunnukselle *kokonaisluku*-arvona.

## <a name="syntax"></a>Syntaksi

```vb
TABLENAME2ID (text)
```

## <a name="arguments"></a>Argumentit

`text`: *Merkkijono*

Tekstiarvo, joka edustaa kelvollista taulukon nimeä.

## <a name="return-values"></a>Palautusarvot

*Kokonaisluku*

Tuloksena oleva numeroarvo.

## <a name="usage-notes"></a>Käyttöhuomautukset

Tämän funktion suorittaminen voi aiheuttaa erilaisia tuloksia eri Microsoft Dynamics 365 Finance -esiintymissä, vaikka käytössä olisi sama yrityksen nimi.

## <a name="example"></a>Esimerkki

`TABLENAME2ID ("Intrastat")` palauttaa **1510**.

## <a name="additional-resources"></a>Lisäresurssit

[Muut (liiketoiminnan toimialuekohtaiset) toiminnot](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
