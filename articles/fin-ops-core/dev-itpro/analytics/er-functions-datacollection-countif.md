---
title: COUNTIF ER-funktio
description: Tässä artikkelissa on tietoja siitä, miten sähköisen raportoinnin (ER) COUNTIF-funktiota käytetään.
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
ms.openlocfilehash: 61ac05d30845eae7c107c8a1edc66e4ff547c8a9
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9274166"
---
# <a name="countif-er-function"></a>COUNTIF ER-funktio

[!include [banner](../includes/banner.md)]

`COUNTIF`-funktio palauttaa *Kokonaislukuarvon*, joka vastaa niiden muotoelementtien määrää, jotka kerättiin, kun muotoelementtejä käytettiin lähtevän asiakirjan luomiseen muotoajon aikana ja joka täyttää määritetyn ehdon. Ehto muodostuu avainalueesta ja avainarvosta.

## <a name="syntax"></a>Syntaksi

```vb
COUNTIF (condition range, condition value)
```

## <a name="arguments"></a>Argumentit

`condition range`: *Merkkijono*

Arvo, joka palautetaan lausekkeella, joka on määritetty sähköisen raportoinnin (ER) muotokomponentin **kerätyn tietoavaimen nimi** -ominaisarvoon.

`condition value`: *Merkkijono*

Arvo, joka palautetaan lausekkeella, joka on määritetty ER-muotokomponentin **Kerätyn tietoavaimen arvo** -ominaisarvoon.

## <a name="return-values"></a>Palautusarvot

*Kokonaisluku*

Tuloksena oleva numeroarvo.

## <a name="usage-notes"></a>Käyttöhuomautukset

**Kerättyjen tietoavainten nimen** ja **Kerättyjen tietoavainten arvon** ominaisuudet voidaan määrittää joko **sarja**-komponentille tai ER-muodon **XML-elementti**-komponentille, joka sijaitsee **yhteisessä\\tiedosto**-komponentissa, jossa **Kerää tuotostiedot** -asetus on käytössä.

Tämä funktio palauttaa **0** (nolla)-arvon, kun **Kerää tuotos tiedot** -vaihtoehto on poistettu käytöstä nykyisessä **Yleinen\\Tiedosto**-komponentissa.

`condition range`-argumentessa yleismerkkiä **"\*"** voidaan käyttää kuvaamaan mitä tahansa useita merkkejä.

`condition value`-argumentessa yleismerkkiä **"\*"** voidaan käyttää kuvaamaan mitä tahansa useita merkkejä.

## <a name="example"></a>Esimerkki

Lisätietoja tämän toiminnon käytöstä on tehtäväoppaassa [ER Käytä tulostusmuotoa laskennassa ja summauksessa](tasks/er-format-counting-summing-1.md), joka on osa **IT-palvelujen ja -ratkaisujen komponenttien hankkiminen ja kehittäminen** -liiketoimintaprosessia.

## <a name="additional-resources"></a>Lisäresurssit

[Tietojen keruutoiminnot](er-functions-category-data-collection.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
