---
title: Luettelo ER-funktioista tyypinmuutosluokassa
description: Tässä ohjeaiheessa on tietoja sähköisen raportoinnin (ER) tukemista muunnosfunktioista.
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: eb2d4ab3434a563e907f6540809888cd3f671c1a
ms.sourcegitcommit: fcc4596eeadac5dfe9a3242afa49b9b1c0c96575
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/15/2020
ms.locfileid: "4740805"
---
# <a name="list-of-er-functions-in-the-type-conversion-category"></a>Luettelo ER-funktioista tyypinmuutosluokassa

[!include [banner](../includes/banner.md)]

Sähköisen raportoinnin (ER) tyyppimuuntofunktioita voidaan käyttää arvojen muuntamiseen tyyppien välillä. Tässä aiheessa on yhteenveto näistä funktioista.

## <a name="type-conversion-functions"></a>Tyypin muuntamisen toiminnot

| Toiminto | Kuvaus |
|----------|-------------|
| [Int64Value](er-functions-conversion-int64value.md)   | Tämä funktio palauttaa *Int64*-arvon, joka edustaa määritettyä merkkijonoa. |
| [IntValue](er-functions-conversion-intvalue.md)       | Tämä funktio palauttaa *Int*-arvon, joka edustaa määritettyä merkkijonoa. |
| [NumberValue](er-functions-conversion-numbervalue.md) | Tämä funktio palauttaa *todellisen* arvon, joka muunnetaan määritetystä *merkki* arvosta. Muuntamisen aikana otetaan huomioon määritetyt desimaali- ja numeroryhmittelyerottimet. |
| [Arvo](er-functions-conversion-value.md)             | Tämä funktio palauttaa *todellisen* arvon, joka muunnetaan määritetystä *merkki* arvosta. |

## <a name="type-conversion-functions-in-the-container-category"></a>Säilöluokan tyyppimuuntofunktiot

Seuraavassa taulukossa kuvataan [säilöluokan](er-functions-category-container.md) tyyppimuuntofunktiot.

| Toiminto | kuvaus |
|----------|-------------|
| [Base64StringToContainer](er-functions-container-base64stringtocontainer.md) | Tämä funktio muuntaa *Merkkijono*-tyypin määritetyn syötteen *Säilö*-tyypin tietokohteeksi. |

## <a name="type-conversion-functions-in-the-date-and-time-category"></a>Syötä muuntofunktiot päivämäärä- ja aikaluokassa

Seuraavassa taulukossa kuvataan tyyppimuuntofunktiot [päivämäärä- ja aikaluokassa](er-functions-category-datetime.md).

| Toiminto | Kuvaus |
|----------|-------------|
| [DateTimeValue](er-functions-datetime-datetimevalue.md)   | Tämä funktio palauttaa *DateTime*-arvon, joka muunnetaan tietystä *Merkki*-arvosta tekstinä määritetyssä muodossa ja valinnaisesti määritetyssä kulttuurissa päivämäärä-/aika-arvoksi. |
| [DateToDateTime](er-functions-datetime-datetodatetime.md) | Tämä funktio palauttaa *DateTime*-arvon , joka muunnetaan tietyn *päivämäärän* arvosta päivämäärä- ja aika-arvoksi koordinoidussa yleisajassa (Greenwichin aika \[GMT\]). |
| [DateValue](er-functions-datetime-datevalue.md)           | Tämä funktio palauttaa *Date*-arvon, joka muunnetaan tietystä *Merkki*-arvosta tekstinä määritetyssä muodossa ja valinnaisesti määritetyssä kulttuurissa päivämäärä-/aika-arvoksi. |

## <a name="type-conversion-functions-in-the-list-category"></a>Kirjoita muuntamisfunktiot luetteloluokkaan

Seuraavassa taulukossa kuvataan tyyppimuuntofunktiot [luettelokategoriassa](er-functions-category-list.md).

| Toiminto | Kuvaus |
|----------|-------------|
| [Luettelo](er-functions-list-list.md)                 | Tämä funktio palauttaa *Tietueluettelon* arvon uutena luettelona, joka luodaan *säilö (tietue)* -tyypin määritetyistä argumenteista. |
| [ListOfFields](er-functions-list-listoffields.md) | Tämä funktio palauttaa *Tietueluettelon* arvon, joka luodaan *luettelointi*- tai *säilö (tietue)* -tyypin tietyn argumentin rakenteen perusteella. |
| [Jako](er-functions-list-split.md)               | Tämä funktio jakaa määritetyn *merkkijono*-arvon alimerkkijonoiksi ja palauttaa tuloksen uudeksi *Tietueluettelon* arvoksi. |
| [StringJoin](er-functions-list-stringjoin.md)     | Tämä funktio palauttaa määritetystä luettelosta *merkkijonon*, joka koostuu määritetyn kentän ketjutetuista arvoista tietystä *Tietueluettelon* arvosta. Arvot voidaan erottaa määritetyllä erottimella. |

## <a name="type-conversion-functions-in-the-text-category"></a>Kirjoita muuntamisfunktiot tekstiluokkaan

Seuraavassa taulukossa kuvataan tyyppimuuntofunktiot [tekstikategoriassa](er-functions-category-text.md).

| Toiminto | Kuvaus |
|----------|-------------|
| [Char](er-functions-text-char.md)                 | Tämä funktio palauttaa *Merkkijono*-arvon, joka edustaa yksittäistä merkkiä, johon viitataan määritetyllä Unicode-numerolla. |
| [GuidValue](er-functions-text-guidvalue.md)       | Tämä funktio muuntaa *Merkkijono*-tyypin määritetyn syötteen *GUID*-tyypin tietokohteeksi. |
| [NumberFormat](er-functions-text-numberformat.md) | Tämä funktio palauttaa *Merkkijonoarvon*, joka edustaa määritetyn numeron määritetyssä muodossa ja valinnaisesti määritetyssä kulttuurissa. |
| [QrCode](er-functions-text-qrcode.md)             | Tämä funktio palauttaa *Säilön* arvon, joka esittää määritetyn merkkijonon nopean vastauskoodin (QR Code) binaarimuodossa. |
| [Teksti](er-functions-text-text.md)                 | Tämä funktio palauttaa määritetyn *merkkijono*-arvon, joka edustaa määritettyä numeroa sen jälkeen, kun se on muunnettu tekstimerkkijonoksi. Se puolestaan muotoillaan nykyisen sovellusesiintymän palvelimen aluekohtaisten asetusten perusteella. |

## <a name="additional-resources"></a>Lisäresurssit

[Sähköisen raportoinnin yleiskatsaus](general-electronic-reporting.md)

[Sähköisen raportoinnin kaavojen suunnittelutoiminto](general-electronic-reporting-formula-designer.md)

[Sähköisen raportoinnin kaavakieli](er-formula-language.md)
