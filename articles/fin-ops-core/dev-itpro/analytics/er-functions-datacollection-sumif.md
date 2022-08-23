---
title: SUMIF ER-funktio
description: Tässä artikkelissa on tietoja siitä, miten sähköisen raportoinnin (ER) SUMIF-funktiota käytetään.
author: kfend
ms.date: 04/27/2020
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
ms.openlocfilehash: 66f8f60714f403c9e4ce5c798f08d9566a3e334d
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9285332"
---
# <a name="sumif-er-function"></a>SUMIF ER-funktio

[!include [banner](../includes/banner.md)]

`SUMIF`-funktio palauttaa *Todellisen* arvon, joka on niiden arvojen summa, jotka palautettiin muotoiluelementtien sitomisella ja, jotka kerättiin, kun muotoelementtejä käytettiin lähtevän asiakirjan luomiseen muotoajon aikana ja joka täyttää määritetyn ehdon. Ehto muodostuu avainalueesta ja avainarvosta.

## <a name="syntax"></a>Syntaksi

```vb
SUMIF (key name for summing, condition range, condition value)
```

## <a name="arguments"></a>Argumentit

`key name for summing`: *Merkkijono*

Arvo, joka palautetaan lausekkeella, joka on määritetty sähköisen raportoinnin (ER) muoto-osan **kerätyn tietoavaimen nimi** -ominaisarvoon, jolle sidonnan arvoa on käytettävä summaustarkoituksiin.

**Kerättyjen tietoavainten nimi** -ominaisuus voidaan määrittää joko **sarja**-komponentille tai ER-muodon **XML-elementti**-komponentille, joka sijaitsee **yhteinen\\tiedosto**-komponentissa, jossa **Kerää tuotostiedot** -asetus on käytössä.

## <a name="return-values"></a>Palautusarvot

*Reaaliluku*

Tuloksena oleva numeroarvo.

## <a name="usage-notes"></a>Käyttöhuomautukset

Tämä funktio palauttaa **0** (nolla)-arvon, kun **Kerää tuotos tiedot** -vaihtoehto on poistettu käytöstä nykyisessä **Yleinen\\Tiedosto**-komponentissa.

`condition range`-argumentessa yleismerkkiä **"\*"** voidaan käyttää kuvaamaan mitä tahansa useita merkkejä.

`condition value`-argumentessa yleismerkkiä **"\*"** voidaan käyttää kuvaamaan mitä tahansa useita merkkejä.

## <a name="example"></a>Esimerkki

Lisätietoja tämän toiminnon käytöstä on tehtäväoppaassa [ER Käytä tulostusmuotoa laskennassa ja summauksessa](tasks/er-format-counting-summing-1.md), joka on osa **IT-palvelujen ja -ratkaisujen komponenttien hankkiminen ja kehittäminen** -liiketoimintaprosessia.

Lisätietoja ja esimerkkejä tämän toiminnon käyttämisestä on kohdassa [Sekvenssielementtien suorituksen lykkääminen ER-muodoissa](er-defer-sequence-element.md#Example) sekä [XML-elementtien suorituksen siirtäminen ER-muodoissa](er-defer-xml-element.md#Example).

## <a name="additional-resources"></a>Lisäresurssit

[Tietojen keruutoiminnot](er-functions-category-data-collection.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
