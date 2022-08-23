---
title: FORMATELEMENTNAME ER -funktio
description: Tässä artikkelissa on tietoja siitä, miten sähköisen raportoinnin (ER) FORMATELEMENTNAME-funktiota käytetään.
author: kfend
ms.date: 12/05/2019
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: 1c8c319075f8f39bec963df2c88d2d8d3beace43
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9275422"
---
# <a name="formatelementname-er-function"></a>FORMATELEMENTNAME ER -funktio

[!include [banner](../includes/banner.md)]

`FORMATELEMENTNAME`-funktio palauttaa *Merkkijonoarvon*, joka edustaa nykyisen sähköisen raportoinnin (ER) muodon elementin nimeä.

## <a name="syntax"></a>Syntaksi

```vb
FORMATELEMENTNAME ()
```

## <a name="return-values"></a>Palautusarvot

*merkkijono*

Tulokseksi saatava tekstiarvo.

## <a name="usage-notes"></a>Käyttöhuomautukset

Tätä funktiota voidaan kutsua ER-lausekkeissa, jotka määritettiin **Kerättyjen tietojen avaimen nimi** ja **Kerättyjen tietojen avainten arvo** -ominaisuuksiksi ER-muotokomponentin **Teksti**-ryhmästä, joka sijaitsee **Yleinen\\Tiedosto**-komponentissa, jossa **Kerää tuotostiedot** -asetus on käytössä.

## <a name="example"></a>Esimerkki

Lisätietoja tämän toiminnon käytöstä on tehtäväoppaassa [ER Käytä tulostusmuotoa laskennassa ja summauksessa](tasks/er-format-counting-summing-1.md), joka on osa **IT-palvelujen ja -ratkaisujen komponenttien hankkiminen ja kehittäminen** -liiketoimintaprosessia.

## <a name="additional-resources"></a>Lisäresurssit

[Tietojen keruutoiminnot](er-functions-category-data-collection.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
