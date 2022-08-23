---
title: QRCODE ER -funktio
description: Tässä artikkelissa on tietoja siitä, miten sähköisen raportoinnin (ER) QRCODE-funktiota käytetään.
author: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: 9de62eefb82942ccc72e81bd9bf36eed07c99dba
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9287185"
---
# <a name="qrcode-er-function"></a>QRCODE ER -funktio

[!include [banner](../includes/banner.md)]

`QRCODE`-funktio palauttaa *Säilön* arvon, joka esittää määritetyn merkkijonon nopean vastauskoodin (QR Code) binaarimuodossa.

## <a name="syntax"></a>Syntaksi

```vb
QRCODE (text)
```

## <a name="arguments"></a>Argumentit

`text`: *Merkkijono*

*Merkkijono*-arvo, joka esittelee alkuperäisen tekstin.

## <a name="return-values"></a>Palautusarvot

*Säiliö*

Tuloksena oleva binaarinen virta.

## <a name="example"></a>Esimerkki

Voit määrittää sähköisen raportoinnin (ER) muodon, joka luo lähtevän asiakirjan Microsoft Office -muodossa (Excel-työkirjat tai Word-asiakirjat) käyttämällä esimääritettyä mallia. Tämä malli saattaa sisältää **kuva**-objektin (Excel-työkirjan) tai **kuvasisällön ohjausobjektin** (Word-asiakirjan) QR-koodikuvan paikkamerkkinä. Sinun on lisättävä konfiguroituun ER-muotoon **Solu**-elementti, jota käytetään tämän paikkamerkin täyttämiseen. Jos haluat määrittää, mitä tietoja QR-koodiin tallennetaan, sinun on määritettävä sidonta tälle **solu**-elementille. Voit esimerkiksi määrittää tällaisen sidonnan siten, että se sisältää seuraavan lausekkeen:

```vb
QRCODE (model.ListOfShelfLabels.LabelText)`
```

Kun suoritat määritetyn ER-muodon, **LabelText** -kentän **model.ListOfShelfLabels** -tietolähdettä käytetään QR-koodikuvan luomiseen. Tämä kuva korvaa asiakirjamallissa olevan QR-koodikuvan paikkamerkin käyttämällä lähtevän asiakirjan luomiseen. Kun tämä luodun asiakirjan kuva skannataan, se palauttaa tekstin, joka otettiin mallin **LabelText**-kentästä **ListOfShelfLabels** -tietolähteestä. Katso lisätietoja kohdasta [Kuvien ja muotojen upottaminen luomiisi asiakirjoihin ER:n avulla](electronic-reporting-embed-images-shapes.md)

## <a name="additional-resources"></a>Lisäresurssit

[Tekstitoiminnot](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
