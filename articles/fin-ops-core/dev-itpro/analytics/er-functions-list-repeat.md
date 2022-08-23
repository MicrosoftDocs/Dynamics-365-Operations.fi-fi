---
title: REPEAT ER-funktio
description: Tässä artikkelissa on tietoja siitä, miten sähköisen raportoinnin (ER) REPEAT-funktiota käytetään.
author: NickSelin
ms.date: 08/01/2022
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2022-06-01
ms.dyn365.ops.version: AX 10.0.29
ms.openlocfilehash: c56139a3c63b03f907b1dcbf4365990d2a13c35a
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/02/2022
ms.locfileid: "9220688"
---
# <a name="repeat-er-function"></a>REPEAT ER-funktio

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

Tämä `REPEAT`-funktio muodostaa tietueen, jonka sisältämän kentän arvo vastaa määritettyä syötettä. Sen jälkeen se palauttaa tietueen uuden *tietueluettelon*, joka toistetaan määritetyn määrän kertoja.

## <a name="syntax"></a>Syntaksi

```vb
REPEAT (item, number)
```

## <a name="arguments"></a>Argumentit

`item`: Mikä tahansa tuettu [primitiivinen](er-formula-supported-data-types-primitive.md) tai [yhdistelmä](er-formula-supported-data-types-composite.md)tietotyyppi

Toistettava arvo.

`number`: *Kokonaisluku*

Toistojen määrä.

## <a name="return-values"></a>Palautusarvot

*Tietueluettelo*

Tuloksena oleva tietueluettelo.

## <a name="usage-notes"></a>Käyttöhuomautukset

Palautettu toistettujen tietueiden luettelo paljastaa seuraavat kentät:

- Määritetty arvo (`Item`-kenttä)
- Nykyisen tietueen indeksi (`Number`-kenttä)

> [!NOTE]
> Koska tällä funktiolla käytetään yksiperusteista numerointia, `Number`-kentässä on arvo **1** tuloksena olevan luettelon ensimmäisessä tietueessa.

Tämän toiminnon avulla voit kertoa aiemmin luodut tiedot niin, että voit tehdä [sähköisen raportoinnin (ER)](general-electronic-reporting.md) ratkaisujen suorituskyvyn ja volyymitestauksen käyttämällä [Regression Suite Automation Tool (RSAT)](../perf-test/rsat/rsat-overview.md) -työkalua.

## <a name="example"></a>Esimerkki

Haluat luoda XML-muodossa asiakirjan, joka sisältää yhtä monta `Party` XML -elementtiä kuin valintaikkunan tietojen syöttökentässä on määritetty suorituksen aikana, ennen kuin ER-muodon suorittaminen alkaa.

ER-[muoto](er-overview-components.md#format-component) näkyy seuraavassa kuvassa. Tässä muodossa yksi `Party` XML -elementti lisätään, jotta yhden osapuolen ominaisuudet voidaan paljastaa.

<a href="./media/er-repeat-function-1.png"><img src="./media/er-repeat-function-1.png" alt="Format structure on the Format tab of the Format designer page." class="alignnone size-full" width="929" height="548" /></a>

Seuraavassa kuvassa näkyvät seuraavat konfiguroidut tietolähteet:

- Tietolähde `Party`, joka edustaa yksittäistä osapuolta. `Party.Value`-kenttää käytetään yhden tekstiarvon näyttämiseksi.
- [Tietolähde](er-user-input-parameter-data-sources.md) `NumberOfRepeats`, jota käytetään tietojen syöttökentän suorituksen aikana valintaikkunassa. Näin voit määrittää muodostettuun tiedostoon syötettävän osapuolten määrän.
- Tietolähde `Party2`, joka toistaa `Party`-tietueen `NumberOfRepeats`-tietolähteessä määritetyn määrän.

<a href="./media/er-repeat-function-2.png"><img src="./media/er-repeat-function-2.png" alt="Configured data sources on the Mapping tab of the Format designer page." class="alignnone size-full" width="1044" height="411" /></a>

Seuraavassa kuvassa esitetään xml-muotoisia tuotoksia varten luodun muokattavan ER-muodon tietojen sidonnat. Tämä tulos esittää yksittäiset osapuolet luetteloituina solmuina.

<a href="./media/er-repeat-function-3.png"><img src="./media/er-repeat-function-3.png" alt="Configured data bindings on the Mapping tab of the Format designer page." class="alignnone size-full" width="1051" height="417" /></a>

Seuraavassa kuvassa näytetään tulos, kun suunniteltu muoto suoritetaan ja tietolähteen `NumberOfRepeats` arvoksi on määritetty **5**.

<a href="./media/er-repeat-function-4.png"><img src="./media/er-repeat-function-4.png" alt="Result of running the format on a new web browser tab." class="alignnone wp-image-290711 size-full" width="400" height="380" /></a>

## <a name="additional-resources"></a>Lisäresurssit

[Luettelotoiminnot](er-functions-category-list.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
