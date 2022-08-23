---
title: SPLITLIST ER-funktio
description: Tässä artikkelissa on tietoja siitä, miten sähköisen raportoinnin (ER) SPLITLIST-funktiota käytetään.
author: kfend
ms.date: 03/15/2021
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
ms.openlocfilehash: 38ac7e6c6bdf53705d1374c173422f7347253a5f
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9292523"
---
# <a name="splitlist-er-function"></a>SPLITLIST ER-funktio

[!include [banner](../includes/banner.md)]

`SPLITLIST`-funktio jakaa määritetyn luettelon aliluetteloiksi (tai eriksi), joissa on tietty määrä tietueita. Sitten se palauttaa tuloksen uutena *Tietueluettelon* arvona, joka koostuu eristä.

## <a name="syntax-1"></a>Syntaksi 1

```vb
SPLITLIST (list, number)
```

## <a name="syntax-2"></a>Syntaksi 2

```vb
SPLITLIST (list, number, on-demand reading flag)
```

## <a name="arguments"></a>Argumentit

`list`: *Tietueluettelo*

*Tietueluettelo*-tietotyypin tietolähteen kelvollinen polku.

`number`: *Kokonaisluku*

Tietueiden enimmäismäärä erää kohti.

`on-demand reading flag`: *Totuusarvo*

*Totuusarvo* joka määrittää, luodaanko aliluetteloiden elementtejä tarpeen mukaan.

## <a name="return-values"></a>Palautusarvot

*Tietueluettelo*

Tuloksena oleva tietueluettelo.

## <a name="usage-notes"></a>Käyttöhuomautukset

Palautettu eräluettelo, joka sisältää seuraavat elementit:

 - **Arvo:** *Luettelo*

    Nykyiseen erään kuuluvien tietueiden luettelo.

- **BatchNumber:** *Kokonaisluku*

    Palautetun luettelon nykyisen erän numero.

Kun tarvittaessa lukemisen merkinnän arvoksi määritetään **Tosi**, järjestelmä luo pyydettäessä aliluetteloita, jotka mahdollistavat muistin kulutuksen vähentämisen, mutta jotka voivat aiheuttaa suorituskyvyn heikentymisen, jos elementtejä ei käytetä peräkkäin.

## <a name="example"></a>Esimerkki

Seuraavassa kuvassa **Rivit**-tietolähde luodaan tietueluettelo, jossa on kolme tietuetta. Tämä luettelo on jaettu eriin, joista kussakin on enintään kaksi tietuetta.

<a href="./media/picture-splitlist-datasource.jpg"><img src="./media/picture-splitlist-datasource.jpg" alt="Data source that is divided into batches" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a>

Seuraavassa kuvassa on suunnitellun muodon asettelu. Tässä muodon asettelussa sidonnat **Rivit**-tietolähde luodaan muodostamaan tulos XML-muodossa. Tämä tulos esittää kunkin erän erilliset solmut ja sen tietueet.

<a href="./media/picture-splitlist-format.jpg"><img src="./media/picture-splitlist-format.jpg" alt="Format layout that has bindings to a data source" class="alignnone wp-image-290691 size-full" width="374" height="161" /></a>

Seuraavassa kuvassa on tulos, kun suunniteltu muoto suoritetaan.

<a href="./media/picture-splitlist-result.jpg"><img src="./media/picture-splitlist-result.jpg" alt="Result of running the format" class="alignnone wp-image-290701 size-full" width="358" height="191" /></a>

## <a name="additional-resources"></a>Lisäresurssit

[Luettelotoiminnot](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
