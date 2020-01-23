---
title: ALLITEMSQUERY ER-funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) ALLITEMSQUERY-funktiota käytetään.
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
ms.openlocfilehash: 647019a103006c8b74bc26885c51f5372dcf0c42
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917508"
---
# <a name="ALLITEMSQUERY">ALLITEMSQUERY ER-funktio</a>

[!include [banner](../includes/banner.md)]

`ALLITEMSQUERY`-funktio suoritetaan liitettynä SQL-kyselynä. Se palauttaa uuden litistetyn *Tietueluettelo*-arvon, joka sisältää luettelon kaikista kohteista, jotka vastaavat määritettyä polkua.

## <a name="syntax"></a>Syntaksi

```
ALLITEMSQUERY (path)
```

## <a name="arguments"></a>Argumentit

`path`: *Tietueluettelo*

*Tietueluettelo*-tietotyypin tietolähteen kelvollinen polku. Sen on sisällettävä vähintään yksi suhde.

## <a name="return-values"></a>Palautusarvot

*Tietueluettelo*

Tuloksena oleva tietueluettelo.

## <a name="usage-notes"></a>Käyttöhuomautukset

Määritetty polku on määritettävä sallituksi tietolähteen poluksi *Tietueluettelo*-tietotyypin tietolähteen elementtiin. Sen on myös sisällettävä vähintään yksi suhde. Tietoelementit, kuten polun *merkkijono* ja *päivämäärä*, käynnistävät virheen sähköisen raportoinnin (ER) lausekkeenmuodostimessa suunnitteluaikana.

Kun tätä toimintoa käytetään *tietueluettelon* tietolähteisiin, jotka viittaavat sovellusobjektiin, jota voidaan kutsua suoraan SQL:n (esimerkiksi taulukon, entiteetin tai kyselyn) avulla, se suoritetaan liitetyssä SQL-kyselynä. Muussa tapauksessa se toimii muistissa [ALLITEMS](er-functions-list-allitems.md)-funktiolla.

## <a name="example"></a>Esimerkki

Määritä seuraavat tietolähteet omassa mallimäärityksessäsi:

- **CustInv**-tietolähde, joka on *Taulukkotietueet*-tyypiä, joka viittaa CustInvoiceTable-tauluun
- *Lasketun kenttätyypin* **FilteredInv**-tietolähde, joka sisältää lausekkeen `FILTER (CustInv, CustInv.InvoiceAccount = "US-001")`
- *Lasketun kenttätyypin* **JourLines**, joka sisältää lausekkeen `ALLITEMSQUERY ( FilteredInv.'<Relations'.CustInvoiceJour.'<Relations'.CustInvoiceTrans)`

Kun suoritat mallimäärityksen kutsumaan **JourLines**-tietolähdettä, seuraava SQL-lauseke suoritetaan:

```
SELECT ... FROM CUSTINVOICETABLE T1 CROSS JOIN CUSTINVOICEJOUR T2 CROSS JOIN
CUSTINVOICETRANS T3 WHERE...
```

## <a name="additional-resources"></a>Lisäresurssit

[Luettelotoiminnot](er-functions-category-list.md)