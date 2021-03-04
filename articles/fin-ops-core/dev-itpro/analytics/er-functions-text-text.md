---
title: TEXT ER -funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) TEXT-funktiota käytetään.
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d489da24d0589549153913bbc6db699e3c217e72
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/05/2020
ms.locfileid: "4682892"
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