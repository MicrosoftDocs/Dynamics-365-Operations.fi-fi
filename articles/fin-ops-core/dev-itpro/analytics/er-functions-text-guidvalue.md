---
title: GUIDVALUE ER -funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) GUIDVALUE-funktiota käytetään.
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: eb6f301cf7a39208aa23337401a9684fb5b3a73d
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685951"
---
# <a name="guidvalue-er-function"></a>GUIDVALUE ER -funktio

[!include [banner](../includes/banner.md)]

`GUIDVALUE`-funktio muuntaa *Merkkijono*-tyypin määritetyn syötteen *GUID*-tyypin tietokohteeksi.

## <a name="syntax"></a>Syntaksi

```vb
GUIDVALUE (input)
```

## <a name="arguments"></a>Argumentit

`input`: *Merkkijono*

*Merkkijono*-tietotyypin tietolähteen kelvollinen polku.

## <a name="return-values"></a>Palautusarvot

*GUID*

Tulokseksi saatu maailmanlaajuisesti yksilöivä tunniste (GUID) -arvo.

## <a name="usage-notes"></a>Käyttöhuomautukset

Voit tehdä muunnon vastakkaiseen suuntaan käyttämällä [TEXT](er-functions-text-text.md)-funktiota. (*GUID*-tietotyypin määritetty syöte siis muunnetaan *String*-tietotyypin tietokohteeksi.)

## <a name="example"></a>Esimerkki

Määritä seuraavat tietolähteet omassa mallimäärityksessäsi:

- *Lasketun kenttätyypin* **myID**-tietolähde, joka sisältää lausekkeen `GUIDVALUE ("AF5CCDAC-F728-4609-8C8B- A4B30B0C0AA0")`
- **Users**-tietolähde, joka on *Taulukkotietueet*-tyypiä, joka viittaa UserInfo-tauluun

Tämän jälkeen voit käyttää lauseketta, kuten `FILTER (Users, Users.objectId = myID)`, joka suodattaa UserInfo-taulukon *GUID*-tietotyypin **objectID**-kentän mukaan.

## <a name="additional-resources"></a>Lisäresurssit

[Tekstitoiminnot](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]