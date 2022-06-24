---
title: Luettelo ER-funktioista päivämäärä- ja aikaluokassa
description: Tässä artikkelissa on tietoja sähköisen raportoinnin (ER) tukemista päivämäärä- ja aikafunktioista.
author: NickSelin
ms.date: 09/09/2021
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
ms.openlocfilehash: e6e15d143bad016883f03ecf0125ce9429215a71
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8880236"
---
# <a name="list-of-er-functions-in-the-date-and-time-category"></a>Luettelo ER-funktioista päivämäärä- ja aikaluokassa

[!include [banner](../includes/banner.md)]

Sähköisen raportoinnin (ER) päivämäärä- ja aikafunktioiden avulla voidaan poimia tietoja päivämäärä- ja aika-arvoista sekä suorittaa niitä koskevia toimintoja. Tässä artikkelissa on yhteenveto näistä funktioista.

## <a name="list-of-supported-functions"></a>Luettelo tuetuista toiminnoista

| Toiminto | Kuvaus |
|----------|-------------|
| [AddDays](er-functions-datetime-adddays.md) | Tämä funktio palauttaa *[DateTime](er-formula-supported-data-types-primitive.md#datetime)*-arvon, joka on määritetty päivien määrä ennen määritettyä alkamispäivää tai sen jälkeen. |
| [ChangeTimeZone](er-functions-datetime-changetimezone.md) | Tämä funktio palauttaa *DateTime*-arvon , joka muunnetaan tietystä päivämäärä/aika-arvosta yhdellä aikavyöhykkeellä päivämäärä- ja aika-arvoksi toisella aikavyöhykkeellä. |
| [DateFormat](er-functions-datetime-dateformat.md) | Tämä funktio palauttaa *[Merkkijono](er-formula-supported-data-types-primitive.md#string)*-arvon, joka esittää tietyn päivämääräarvon tekstinä määritetyssä muodossa ja valinnaisesti määritetyssä kulttuurissa. |
| [DateTimeFormat](er-functions-datetime-datetimeformat.md) | Tämä funktio palauttaa *Merkkijonoarvon*, joka esittää tietyn päivämäärä-/aika-arvon tekstinä määritetyssä muodossa ja valinnaisesti määritetyssä kulttuurissa. |
| [DateTimeValue](er-functions-datetime-datetimevalue.md) | Tämä funktio palauttaa *DateTime-arvon*, joka muunnetaan tietystä tekstiarvosta tekstinä määritetyssä muodossa ja valinnaisesti määritetyssä kulttuurissa päivämäärä-/aika-arvoksi. |
| [DateToDateTime](er-functions-datetime-datetodatetime.md) | Tämä funktio palauttaa *DateTime-arvon* , joka muunnetaan tietyn päivämäärän arvosta päivämäärä- ja aika-arvoksi koordinoidussa yleisajassa (Greenwichin aika \[GMT\]). |
| [DateValue](er-functions-datetime-datevalue.md) | Tämä funktio palauttaa *[Date](er-formula-supported-data-types-primitive.md#date)*-arvon, joka muunnetaan annetusta tekstiarvosta määrätyssä muodossa ja valinnaisesti määritellyssä kulttuurissa päivämääräarvoksi. |
| [DayOfYear](er-functions-datetime-dayofyear.md) | Tämä toiminto palauttaa tammikuun 1. päivän ja määritetyn päivämäärän välisten päivien määrää kuvaavan arvon *[kokonaislukuna](er-formula-supported-data-types-primitive.md#integer)*. |
| [Päivää](er-functions-datetime-days.md) | Tämä toiminto palauttaa ensimmäisen määritetyn päivämäärän ja toisen määritetyn päivämäärän välisten päivien määrää kuvaavan arvon *kokonaislukuna*. |
| [Now](er-functions-datetime-now.md) | Tämä funktio palauttaa *DateTime*-arvon, joka edustaa nykyistä sovelluspalvelimen päivämäärää ja aikaa. |
| [NullDate](er-functions-datetime-nulldate.md) | Tämä funktio palauttaa *päivämäärän* arvon, joka vastaa **Null** -arvoa (1. tammikuuta 1900). |
| [NullDateTime](er-functions-datetime-nulldatetime.md) | Tämä funktio palauttaa *DateTime*-arvon, joka edustaa **Null**-arvoista päivämäärä- ja aika-arvoa (1. tammikuuta 1900) koordinoituun yleisaikaan. |
| [SessionNow](er-functions-datetime-sessionnow.md) | Tämä funktio palauttaa *DateTime*-arvon, joka edustaa nykyistä sovellusistunnon päivämäärää ja aikaa. |
| [SessionToday](er-functions-datetime-sessiontoday.md) | Tämä funktio palauttaa *Date*-arvon, joka edustaa nykyistä sovellusistunnon päivämäärää. |
| [Tänään](er-functions-datetime-today.md) | Tämä funktio palauttaa *Date*-arvon, joka edustaa nykyistä sovelluspalvelimen päivämäärää. |
| [WeekNum](er-functions-datetime-weeknum.md) | Tämä funktio palauttaa *Kokonaisluku*-arvon, joka edustaa tiettyä viikkoa vuodessa. |

## <a name="additional-resources"></a>Lisäresurssit

[Sähköisen raportoinnin yleiskatsaus](general-electronic-reporting.md)

[Sähköisen raportoinnin kaavojen suunnittelutoiminto](general-electronic-reporting-formula-designer.md)

[Sähköisen raportoinnin kaavakieli](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
