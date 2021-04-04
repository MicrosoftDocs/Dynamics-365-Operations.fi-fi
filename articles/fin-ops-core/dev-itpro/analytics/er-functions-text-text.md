---
title: TEXT ER -funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) TEXT-funktiota käytetään.
author: NickSelin
manager: kfend
ms.date: 12/10/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5da7375020be827f432ba97740da37abe48962fc
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/09/2021
ms.locfileid: "5560058"
---
# <a name="text-er-function"></a>TEXT ER -funktio

[!include [banner](../includes/banner.md)]

`TEXT`-funktio palauttaa määritetyn numeron *merkkijono*-arvona, sen jälkeen, kun se on muunnettu tekstimerkkijonoksi. Se puolestaan muotoillaan nykyisen sovellusesiintymän palvelimen aluekohtaisten asetusten perusteella.

## <a name="syntax"></a>Syntaksi

```vb
TEXT (number)
```

## <a name="arguments"></a>Argumentit

`number`: *Kokonaisluku* tai *Todellinen*

Numero, jota ei pidä muuntaa tekstimerkkijonoksi.

## <a name="return-values"></a>Palautusarvot

*merkkijono*

Tulokseksi saatava tekstiarvo.

## <a name="usage-notes"></a>Käyttöhuomautukset

*Todellinen*-tyyppisten arvojen merkkijonon muunnos on rajoitettu kahteen desimaaliin.

## <a name="example"></a>Esimerkki

Jos Microsoft Dynamics 365 Finance -esiintymän palvelimen aluekohtaisiksi asetuksiksi on määritetty **FI-FI**, `TEXT (NOW ())` palauttaa nykyisen sovellusistunnon päivämäärän 17.12.2015 tekstimerkkijonona **17.12.2015 07.59.23**. `TEXT (1/3)` palauttaa **"0.33"**.

## <a name="additional-resources"></a>Lisäresurssit

[Tekstitoiminnot](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]