---
title: SUMIFS ER-funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) SUMIFS-funktiota käytetään.
author: NickSelin
manager: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: 6820be1976e722f7b108b3e9303c8ed4d822ae9b
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917600"
---
# <a name="SUMIFS">SUMIFS ER-funktio</a>

[!include [banner](../includes/banner.md)]

`SUMIFS`-funktio palauttaa *Todellisen* arvon, joka on niiden arvojen summa, jotka palautettiin muotoiluelementtien sitomisella ja, jotka kerättiin, kun muotoelementtejä käytettiin lähtevän asiakirjan luomiseen muotoajon aikana ja joka täyttää määritetyt ehdot. Jokainen ehto muodostuu avainalueesta ja avainarvosta.

## <a name="syntax"></a>Syntaksi

```
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