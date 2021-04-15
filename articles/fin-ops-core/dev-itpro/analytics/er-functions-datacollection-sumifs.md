---
title: SUMIFS ER-funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) SUMIFS-funktiota käytetään.
author: NickSelin
ms.date: 12/04/2019
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
ms.openlocfilehash: a3adfe62d9fd7bdc23784cf7311f65a4d2e88960
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5747080"
---
# <a name="sumifs-er-function"></a>SUMIFS ER-funktio

[!include [banner](../includes/banner.md)]

`SUMIFS`-funktio palauttaa *Todellisen* arvon, joka on niiden arvojen summa, jotka palautettiin muotoiluelementtien sitomisella ja, jotka kerättiin, kun muotoelementtejä käytettiin lähtevän asiakirjan luomiseen muotoajon aikana ja joka täyttää määritetyt ehdot. Jokainen ehto muodostuu avainalueesta ja avainarvosta.

## <a name="syntax"></a>Syntaksi

```vb
SUMIFS (key name for summing, condition 1 range, condition 1 value[, condition 2 range, condition 2 value, …, condition N range, condition N value])
```

## <a name="arguments"></a>Argumentit

`key name for summing`: *Merkkijono*

Arvo, joka palautetaan lausekkeella, joka on määritetty sähköisen raportoinnin (ER) muoto-osan **kerätyn tietoavaimen nimi** -ominaisarvoon, jolle sidonnan arvoa on käytettävä summaustarkoituksiin.

**Kerättyjen tietoavainten nimi** -ominaisuus voidaan määrittää joko **Numeeriselle** komponentille tai ER-muodon **Merkkijono**-komponentille, joka sijaitsee **yhteinen\\tiedosto**-komponentissa, jossa **Kerää tuotostiedot** -asetus on käytössä.

`condition 1 range`: *Merkkijono*

Arvo, joka palautetaan lausekkeella, joka on määritetty ER-muotokomponentin **Kerätyn tietoavaimen nimi** -ominaisarvoon. Tämä argumentti on pakollinen.

**Kerättyjen tietoavainten nimi** -ominaisuus voidaan määrittää joko **sarja**-komponentille tai ER-muodon **XML-elementti**-komponentille, joka sijaitsee **yhteinen\\tiedosto**-komponentissa, jossa **Kerää tuotostiedot** -asetus on käytössä.

`condition 1 value`: *Merkkijono*

Arvo, joka palautetaan lausekkeella, joka on määritetty ER-muotokomponentin **Kerätyn tietoavaimen arvo** -ominaisarvoon. Tämä argumentti on pakollinen.

**Kerättyjen tietoavainten nimi** -ominaisuus voidaan määrittää joko **sarja**-komponentille tai ER-muodon **XML-elementti**-komponentille, joka sijaitsee **yhteinen\\tiedosto**-komponentissa, jossa **Kerää tuotostiedot** -asetus on käytössä.

`condition N range`: *Merkkijono*

Arvo, joka palautetaan lausekkeella, joka on määritetty ER-muotokomponentin **Kerätyn tietoavaimen nimi** -ominaisarvoon. Nämä lisäargumentit ovat valinnaisia.

**Kerättyjen tietoavainten nimi** -ominaisuus voidaan määrittää joko **sarja**-komponentille tai ER-muodon **XML-elementti**-komponentille, joka sijaitsee **yhteinen\\tiedosto**-komponentissa, jossa **Kerää tuotostiedot** -asetus on käytössä.

`condition N value`: *Merkkijono*

Arvo, joka palautetaan lausekkeella, joka on määritetty ER-muotokomponentin **Kerätyn tietoavaimen arvo** -ominaisarvoon. Nämä lisäargumentit ovat valinnaisia.

**Kerättyjen tietoavainten nimi** -ominaisuus voidaan määrittää joko **sarja**-komponentille tai ER-muodon **XML-elementti**-komponentille, joka sijaitsee **yhteinen\\tiedosto**-komponentissa, jossa **Kerää tuotostiedot** -asetus on käytössä.

## <a name="return-values"></a>Palautusarvot

*Reaaliluku*

Tuloksena oleva numeroarvo.

## <a name="usage-notes"></a>Käyttöhuomautukset

Tämä funktio palauttaa **0** (nolla)-arvon, kun **Kerää tuotos tiedot** -vaihtoehto on poistettu käytöstä nykyisessä **Yleinen\\Tiedosto**-komponentissa.

`condition range`-argumenteissa yleismerkkiä **"\*"** voidaan käyttää kuvaamaan mitä tahansa useita merkkejä.

`condition value`-argumenteissa yleismerkkiä **"\*"** voidaan käyttää kuvaamaan mitä tahansa useita merkkejä.

## <a name="example"></a>Esimerkki

Lisätietoja tämän toiminnon käytöstä on tehtäväoppaassa [ER Käytä tulostusmuotoa laskennassa ja summauksessa](tasks/er-format-counting-summing-1.md), joka on osa **IT-palvelujen ja -ratkaisujen komponenttien hankkiminen ja kehittäminen** -liiketoimintaprosessia.

## <a name="additional-resources"></a>Lisäresurssit

[Tietojen keruutoiminnot](er-functions-category-data-collection.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]