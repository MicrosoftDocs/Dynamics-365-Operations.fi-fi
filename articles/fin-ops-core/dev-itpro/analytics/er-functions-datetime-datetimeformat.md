---
title: DATETIMEFORMAT ER-funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) DATETIMEFORMAT-funktiota käytetään.
author: NickSelin
ms.date: 01/04/2021
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
ms.openlocfilehash: 859753c04e3b3d3b61d9a61edaf396637ed5a003
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746984"
---
# <a name="datetimeformat-er-function"></a>DATETIMEFORMAT ER-funktio

[!include [banner](../includes/banner.md)]

`DATETIMEFORMAT`-funktio palauttaa *Merkkijono*-arvon, joka esittää tietyn päivämäärä-/aika-arvon tekstinä määritetyssä muodossa ja valinnaisesti määritetyssä [kulttuurissa](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes). Lisätietoja tuetuista muodoista on kohdassa [vakio](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) ja [mukautettu](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).

## <a name="syntax-1"></a>Syntaksi 1

```vb
DATETIMEFORMAT (datetime, format)
```

## <a name="syntax-2"></a>Syntaksi 2

```vb
DATETIMEFORMAT (datetime, format, culture)
```

## <a name="arguments"></a>Argumentit

`datetime`: *DateTime*

Päivämäärä-/aika-arvo, joka vastaa muokattavaa päivämäärää ja aikaa.

`format`: *Merkkijono*

Tulostusmerkkijonon muoto

> [!NOTE]
> Muodon merkkijono ottaa kirjainkoon huomioon, kun käytössä joko vakiomuoto tai mukautettu muoto. Esimerkiksi [vakiomuotoinen](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) d-määrite palauttaa päivämäärän käyttämällä lyhyt päivämäärämalli, kun taas vakiomuotoinen D-määrite palauttaa pitkää päivämäärämallia käyttävän päivämäärän. Lisäksi [mukautetun](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx) muodon M-määrite palauttaa kuukaudet 1–12, kun taas mukautetun muodon m-määrite palauttaa minuutit 0–59.

`culture`: *Merkkijono*

Muotoilussa käytettävä kulttuuri.

## <a name="return-values"></a>Palautusarvot

*Merkkijono*

Tuloksena oleva merkkijonoarvo.

## <a name="usage-notes"></a>Käyttöhuomautukset

Jos kulttuuria ei ole määritetty kutsutun funktion argumentiksi, kutsuvan kontekstin määrittämä arvo `culture` määritetään. Jos `DATETIMEFORMAT`-funktiota kutsutaan esimerkiksi käyttämällä syntaksia 1 sähköisen raportoinnin (ER) muodossa **TIEDOSTO**-elementille, joka on määritetty käyttämään Saksan kulttuuria, muuntaminen tehdään Saksan kulttuurin avulla. `culture`-arvon oletusarvo on **FI-FI**.

Kun `DATETIMEFORMAT`-funktio muuntaa tietyn päivämäärä- ja aika-arvon, se harkitsee sen sovelluksen käyttäjän aikavyöhykeasetusta, joka suorittaa ER-muotoa ja jota funktiota kutsutaan järjestelmän kontekstissa.

## <a name="example-1"></a>Esimerkki 1

`DATETIMEFORMAT (NOW(), "dd-MM-yyyy")` palauttaa nykyisen sovelluspalvelimen päivämäärä-/aika-arvon 24. joulukuuta 2015 muodossa **24-12-2015** määritetyn mukautetun muodon mukaisesti.

## <a name="example-2"></a>Esimerkki 2

`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` palauttaa nykyisen sovellusistunnon päivämäärä-/aika-arvon, 24. joulukuuta 2015, merkkijonona **"24.12.2015"**, joka perustuu valittuun Saksan kulttuuriin ja määritettyyn muotoon.

## <a name="example-3"></a>Esimerkki 3

`DATETIMEFORMAT (DATETIMEVALUE( "2019-11-12T09:00:00.0000000-07:00", "O"), "O")` palauttaa merkkijonon arvon **2019-11-12T 08:00:00.0000000-08:00**, kun funktiota kutsutaan prosessin aikana, jonka käynnistäneen sovelluskäyttäjän aikavyöhykkeen arvo on **(GMT-08:00) Tyynenmeren normaaliaika (USA ja Kanada)** **Kieli- ja alue-asetukset** -osassa.

## <a name="additional-resources"></a>Lisäresurssit

[Päivämäärä- ja aikatoiminnot](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]