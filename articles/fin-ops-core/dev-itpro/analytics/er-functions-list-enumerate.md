---
title: ENUMERATE ER-funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) ENUMERATE-funktiota käytetään.
author: NickSelin
ms.date: 12/12/2019
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
ms.openlocfilehash: b05448b57d3b08af61144dacdfa2a4e1ba30d009
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746648"
---
# <a name="enumerate-er-function"></a>ENUMERATE ER-funktio

[!include [banner](../includes/banner.md)]

`ENUMERATE`-funktio palauttaa uuden *Tietueluettelon* arvon, joka koostuu määritetyn luettelon valintalistan tietueista.

## <a name="syntax"></a>Syntaksi

```vb
ENUMERATE (list)
```

## <a name="arguments"></a>Argumentit

`list`: *Tietueluettelo*

*Tietueluettelo*-tietotyypin tietolähteen kelvollinen polku.

## <a name="return-values"></a>Palautusarvot

*Tietueluettelo*

Tuloksena oleva tietueluettelo.

## <a name="usage-notes"></a>Käyttöhuomautukset

Palautettujen luetteloidut tietueet -luettelo paljastaa seuraavat lisäelementit:

- Kenttien tietue (**Arvo**-komponentti)
- Nykyisen tietueen indeksi (**numero**-komponentti)

## <a name="example"></a>Esimerkki

Seuraavassa kuvassa **Numeroitu**-tietolähde luodaan toimittajan tietueiden numeroituna luettelona **Toimittajat**-tietolähteestä, joka viittaa VendTable-tauluun.

<a href="./media/picture-enumerate-datasource.jpg"><img src="./media/picture-enumerate-datasource.jpg" alt="Enumerated data source" class="alignnone wp-image-290711 size-full" width="387" height="136" /></a>

Seuraavassa kuvassa on sähköisen raportoinnin (ER) muodon. Tässä muodossa tiedon sidonnat luodaan muodostamaan tulos XML-muodossa. Tämä tulos esittää yksittäiset toimittajat luetteloituina solmuina.

<a href="./media/picture-enumerate-format.jpg"><img src="./media/picture-enumerate-format.jpg" alt="Format that has data bindings" class="alignnone wp-image-290721 size-full" width="414" height="138" /></a>

Seuraavassa kuvassa on tulos, kun suunniteltu muoto suoritetaan.

<a href="./media/picture-enumerate-result.jpg"><img src="./media/picture-enumerate-result.jpg" alt="Result of running the format" class="alignnone wp-image-290731 size-full" width="567" height="176" /></a>

## <a name="additional-resources"></a>Lisäresurssit

[Luettelotoiminnot](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]