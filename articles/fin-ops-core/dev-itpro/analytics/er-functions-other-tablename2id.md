---
title: TABLENAME2ID ER -funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) TABLENAME2ID-funktiota käytetään.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: d9f9e38f46df8a93b5cb16b8d0d5e5afbff8558a
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743996"
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
