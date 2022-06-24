---
title: LISTDISTINCT ER -toiminto
description: Tässä artikkelissa on tietoja siitä, miten sähköisen raportoinnin (ER) LISTDISTINCT-funktiota käytetään.
author: NickSelin
ms.date: 7/30/2020
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-08-01
ms.dyn365.ops.version: AX 10.0.14
ms.openlocfilehash: d2f8e3a9d077493df3c3b7628608d31834f43f8a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8876802"
---
# <a name="listdistinct-er-function"></a>LISTDISTINCT ER -toiminto

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

`LISTDISTINCT`-funktio laskee määritetyn lausekkeen valitun luettelon jokaisen tietueen valitsimena. Se palauttaa uuden *tietueluettelon* arvon, joka sisältää yhden tietueen kutakin yksilöllistä valitsinarvoa kohden.

## <a name="syntax"></a>Syntaksi

```
LISTDISTINCT (list, selector)
```

## <a name="arguments"></a>Argumentit

`list`: *Tietueluettelo*

*Tietueluettelo*-tietotyypin tietolähteen kelvollinen polku.

`selector`: *Primitiiviset tietotyypit*

Kelvollinen lauseke, jonka avulla lasketaan valitun luettelon jokaisen tietueen valitsinarvo.

Tämä parametri tukee seuraavia tietotyyppejä:

- Boolen arvo
- Päivämäärä
- Päivämäärä ja aika
- Guid
- Kokonaisluku
- Int64
- Reaaliluku
- Merkkijono

## <a name="return-values"></a>Palautusarvot

*Tietueluettelo*

Tuloksena oleva tietueluettelo.

## <a name="usage-notes"></a>Käyttöhuomautukset

Luotavan luettelon rakenne vastaa määritetyn luettelon rakennetta.

Sama valitsimen arvo voidaan laskea useille tietueille määritetyssä luettelossa. Tässä tapauksessa luodun luettelon vastaavan tietueen kenttäarvot vastaavat määritetyn luettelon ensimmäisen tietueen arvoja, joille valitsinarvo lasketaan.

Tämän toiminnon suorittaminen tapahtuu muistissa olevan *tietueluettelo*-tyypin [sähköisen raportoinnin (ER)](general-electronic-reporting.md) tietolähteen avulla.

**GROUPBY**-tietolähdettä voidaan käyttää myös sellaisten luettelotietojen luomiseen, joille on määritetty erilliset arvot sisältävä valitsin. Suorituskyvyn ja muistin kulutuksen näkökulmasta on kuitenkin parempi käyttää `LISTDISTINCT`-funktiota kuin **GROUPBY**-tietolähdettä, koska toiminnon suorittaminen tapahtuu muistissa.

## <a name="example"></a>Esimerkki

Seuraavassa esimerkissä näkyy, miten voit saada luettelon yksilöivistä asiakastilinumeroista, joille on myönnetty vähintään yksi myyntilasku tai projektilasku tiettynä kautena.

1. Kirjoita sen tyypin **SalesInvoice**-tietolähde `Record list`-tyyppistä, joka viittaa **CustInvoiceJour**-sovellustauluun ja suodattaa tiettyjen kausien myyntilaskut.

    Tämän tietolähteen `InvoiceAccount`-kenttä palauttaa laskutetun asiakkaan tilinumeron.

2. Kirjoita sen tyypin **ProjectInvoice**-tietolähde `Record list`-tyyppistä, joka viittaa **ProjInvoiceJour**-sovellustauluun ja suodattaa tiettyjen kausien projektilaskut.

    Tämän tietolähteen `InvoiceAccount`-kenttä palauttaa laskutetun asiakkaan tilinumeron.

3. Määritä `Calculated field`-tyypin **AllInvoices**-tietolähde, joka sisältää lausekkeen `LISTJOIN(SalesInvoice, ProjectInvoice)`.

    Tämä tietolähde palauttaa liitettyjen myyntilaskujen ja projektilaskujen luettelon.

4. Määritä `Record list`-tyypin **InvoicedCustomer**-tietolähde, joka sisältää lausekkeen `LISTDISTINCT(AllInvoices, AllInvoices.InvoiceAccount)`.

    Tämä tietolähde palauttaa uuden luettelon, joka sisältää yhden tietueen jokaiselle määritetyn kauden aikana laskutetulle asiakkaalle. Tämän luettelon `InvoiceAccount`-kenttä sisältää asiakkaan tilinumeron.

## <a name="additional-resources"></a>Lisäresurssit

[Luettelotoiminnot](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]