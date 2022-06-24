---
title: GETLABELTEXT ER-toiminto
description: Tässä artikkelissa on tietoja siitä, miten sähköisen raportoinnin (ER) GETLABELTEXT-funktiota käytetään.
author: NickSelin
ms.date: 03/18/2022
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2022-01-01
ms.dyn365.ops.version: AX 10.0.25
ms.openlocfilehash: cb3af10d4725e87190f901aa99378e10bdf05bee
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8877064"
---
# <a name="getlabeltext-er-function"></a>GETLABELTEXT ER-toiminto

[!include [banner](../includes/banner.md)]

`GETLABELTEXT`-toiminto etsii tiettyä otsikkoa ja palauttaa *[merkkijono](er-formula-supported-data-types-primitive.md#string)* arvon, joka edustaa määritetyn otsikon käännöstä määritetyllä kielellä.

## <a name="syntax"></a>Syntaksi

```vb
GETLABELTEXT (label id, language)
```

## <a name="arguments"></a>Argumentit

### <a name="label-id"></a>Etikettitunnus

`label id`: *Merkkijono* tai *Otsikon tunnus*

Yhden seuraavista otsikkotyypeistä voimassa oleva tunnus:

- [Sähköisen raportoinnin (ER)](general-electronic-reporting.md) otsikko
- Microsoft Dynamics 365 Financen otsikko

#### <a name="usage-notes"></a>Käyttöhuomautukset

Argumentti voidaan määrittää vain vakiona, kun käytössä on jokin seuraavista tuetuista kaavoista:

- ER-otsikoille:

    - `@"GER_LABEL:<LABEL ID>"`
    - `"GER_LABEL:<LABEL ID>"`

- Finance-otsikoille:

    - `@"<LABEL ID>"`
    - `"<LABEL ID>"`

> [!NOTE]
> Suunnittelun aikana **[Kaavan suunnittelija](er-advanced-formula-editor.md)** -sivulla näkyy oikeellisuustarkistusvirheilmoitus, jos otsikkoa ei löydy annettua otsikkotunnusta käyttäen.

### <a name="language"></a>Kieli

`language`: *Merkkijono*

Kielikoodia edustava merkkijono.

#### <a name="usage-notes"></a>Käyttöhuomautukset

Tämä argumentti voidaan määrittää tekstivakiona tai *merkkijono* arvon palauttavaksi tietolähteen kentän poluksi.

> [!NOTE]
> Suunnittelun aikana näytetään oikeellisuustarkistusvirheilmoitus, jos annettua `language`-argumenttia käyttämällä ei löydy kielikoodia, kun se on määritetty tekstivakioksi.
>
> Ajon aikana `EN-US`-järjestelmäkielen käännös palautetaan määritetylle otsikolle, jos määritettyä `language`-argumenttia käyttämällä ei löydy kielikoodia.

## <a name="return-values"></a>Palautusarvot

*Merkkijono*

Tulokseksi saatava tekstiarvo.

## <a name="example-1-system-label"></a><a name=example-1></a>Esimerkki 1: Järjestelmäotsikko

Lausekkeet `GETLABELTEXT (@"SYS70894", "en-us")`ja `GETLABELTEXT ("SYS70894", "en-us")` palauttavat sovelluksen otsikon `@SYS70894` "Nothing to print" englanninkielisen käännöksen.

## <a name="example-2-er-label"></a><a name=example-2></a>Esimerkki 2: ER-otsikko

Aloitat muokkaamaan ER [-määritystä](general-electronic-reporting.md#Configuration), joka on [johdettu](er-quick-start2-customize-report.md#DeriveProvidedFormat) **ISO20022 Credit transfer (DE)** -määrityksestä, syötät uuden *[Laskettu kenttä](er-calculated-field-ds-performance.md)* -tyypin tietolähteen ja määrität tietolähteelle lausekkeen `GETLABELTEXT(@"GER_LABEL:VendorName", "de")`. Tässä tapauksessa tietolähde palauttaa ajon aikana saksan käännöksen "Kreditorenname" ER-otsikolle `@GER_LABEL:VendorName`, joka määritettiin alun perin **ISO20022 Credit transfer (DE)** ER-peruskonfiguraatiossa.

## <a name="additional-resources"></a>Lisäresurssit

[Tekstitoiminnot](er-functions-category-text.md)

[Monikielisten raporttien suunnitteleminen sähköisessä raportoinnissa](er-design-multilingual-reports.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
