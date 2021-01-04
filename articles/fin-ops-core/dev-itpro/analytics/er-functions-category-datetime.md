---
title: Luettelo ER-funktioista päivämäärä- ja aikaluokassa
description: Tässä ohjeaiheessa on tietoja sähköisen raportoinnin (ER) tukemista päivämäärä- ja aikafunktioista.
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
ms.openlocfilehash: 2745298ae1f6787c3de5a4aaf6a2a6350f5f3e85
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686216"
---
# <a name="list-of-er-functions-in-the-date-and-time-category"></a>Luettelo ER-funktioista päivämäärä- ja aikaluokassa

[!include [banner](../includes/banner.md)]

Sähköisen raportoinnin (ER) päivämäärä- ja aikafunktioiden avulla voidaan poimia tietoja päivämäärä- ja aika-arvoista sekä suorittaa niitä koskevia toimintoja. Tässä aiheessa on yhteenveto näistä funktioista.

## <a name="list-of-supported-functions"></a>Luettelo tuetuista toiminnoista

| Toiminto | Kuvaus |
|----------|-------------|
| [AddDays](er-functions-datetime-adddays.md) | Tämä funktio palauttaa *DateTime*-arvon, joka on määritetty päivien määrä ennen määritettyä alkamispäivää tai sen jälkeen. |
| [DateFormat](er-functions-datetime-dateformat.md) | Tämä funktio palauttaa *Merkkijonoarvon*, joka esittää tietyn päivämääräarvon tekstinä määritetyssä muodossa ja valinnaisesti määritetyssä kulttuurissa. |
| [DateTimeFormat](er-functions-datetime-datetimeformat.md) | Tämä funktio palauttaa *Merkkijonoarvon*, joka esittää tietyn päivämäärä-/aika-arvon tekstinä määritetyssä muodossa ja valinnaisesti määritetyssä kulttuurissa. |
| [DateTimeValue](er-functions-datetime-datetimevalue.md) | Tämä funktio palauttaa *DateTime-arvon*, joka muunnetaan tietystä tekstiarvosta tekstinä määritetyssä muodossa ja valinnaisesti määritetyssä kulttuurissa päivämäärä-/aika-arvoksi. |
| [DateToDateTime](er-functions-datetime-datetodatetime.md) | Tämä funktio palauttaa *DateTime-arvon* , joka muunnetaan tietyn päivämäärän arvosta päivämäärä- ja aika-arvoksi koordinoidussa yleisajassa (Greenwichin aika \[GMT\]). |
| [DateValue](er-functions-datetime-datevalue.md) | Tämä funktio palauttaa *Date-arvon*, joka muunnetaan annetusta tekstiarvosta määrätyssä muodossa ja valinnaisesti määritellyssä kulttuurissa päivämääräarvoksi. |
| [DayOfYear](er-functions-datetime-dayofyear.md) | Tämä toiminto palauttaa tammikuun 1. päivän ja määritetyn päivämäärän välisten päivien määrää kuvaavan arvon *kokonaislukuna*. |
| [Päivää](er-functions-datetime-days.md) | Tämä toiminto palauttaa ensimmäisen määritetyn päivämäärän ja toisen määritetyn päivämäärän välisten päivien määrää kuvaavan arvon *kokonaislukuna*. |
| [Now](er-functions-datetime-now.md) | Tämä funktio palauttaa *DateTime*-arvon, joka edustaa nykyistä sovelluspalvelimen päivämäärää ja aikaa. |
| [NullDate](er-functions-datetime-nulldate.md) | Tämä funktio palauttaa *päivämäärän* arvon, joka vastaa **Null** -arvoa (1. tammikuuta 1900). |
| [NullDateTime](er-functions-datetime-nulldatetime.md) | Tämä funktio palauttaa *DateTime*-arvon, joka edustaa **Null**-arvoista päivämäärä- ja aika-arvoa (1. tammikuuta 1900) koordinoituun yleisaikaan. |
| [SessionNow](er-functions-datetime-sessionnow.md) | Tämä funktio palauttaa *DateTime*-arvon, joka edustaa nykyistä sovellusistunnon päivämäärää ja aikaa. |
| [SessionToday](er-functions-datetime-sessiontoday.md) | Tämä funktio palauttaa *Date*-arvon, joka edustaa nykyistä sovellusistunnon päivämäärää. |
| [Tänään](er-functions-datetime-today.md) | Tämä funktio palauttaa *Date*-arvon, joka edustaa nykyistä sovelluspalvelimen päivämäärää. |

## <a name="additional-resources"></a>Lisäresurssit

[Sähköisen raportoinnin yleiskatsaus](general-electronic-reporting.md)

[Sähköisen raportoinnin kaavojen suunnittelutoiminto](general-electronic-reporting-formula-designer.md)

[Sähköisen raportoinnin kaavakieli](er-formula-language.md)
