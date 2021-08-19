---
title: SPLITLISTBYLIMIT ER-funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) SPLITLISTBYLIMIT-funktiota käytetään.
author: NickSelin
ms.date: 12/12/2019
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
ms.openlocfilehash: 52351c131480119ce9fb98a75307ebf6026cb12b9977e8b4236d3a24ef6a140e
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6744431"
---
# <a name="splitlistbylimit-er-function"></a>SPLITLISTBYLIMIT ER-funktio

[!include [banner](../includes/banner.md)]

`SPLITLISTBYLIMIT`-funktio jakaa määritetyn luettelon uuteen aliluetteloon (erät). Kunkin erän tietueiden määrä lasketaan dynaamisesti. Sitten funktio palauttaa tuloksen uutena *Tietueluettelon* arvona, joka koostuu eristä.

## <a name="syntax"></a>Syntaksi

```vb
SPLITLISTBYLIMIT (list, limit value, limit source)
```

## <a name="arguments"></a>Argumentit

`list`: *Tietueluettelo*

*Tietueluettelo*-tietotyypin tietolähteen kelvollinen polku.

`limit value`: *Kokonaisluku* tai *Todellinen*

Enimmäisarvo, jonka avulla alkuperäinen luettelo jaetaan eriin.

`limit source`: *Kenttä*

*Kokonaisluku*- tai *Todellinen*-tyypin kentän kelvollinen polku on määritetyssä luettelossa. Tämän kentän arvo määrittää vaiheen, jonka kokonaissumma on kasvanut.

## <a name="return-values"></a>Palautusarvot

*Tietueluettelo*

Tuloksena oleva tietueluettelo.

## <a name="usage-notes"></a>Käyttöhuomautukset

Palautettu eräluettelo, joka sisältää seuraavat elementit:

- **Arvo**: *Luettelo*

    Nykyiseen erään kuuluvien tietueiden luettelo.

- **BatchNumber**: *Kokonaisluku*

    Palautetun luettelon nykyisen erän numero.

Rajaa ei käytetä tietyn alkuperäisen luettelon yhteen nimikkeeseen, jos lähderaja ylittää määritetyn rajan.

## <a name="example"></a>Esimerkki

Seuraavassa kuvassa on sähköisen raportoinnin (ER) muodon.

<a href="./media/ger-splitlistbylimit-format.png"><img src="./media/ger-splitlistbylimit-format.png" alt="Format" class="alignnone size-full wp-image-1204063" width="396" height="195" /></a>

Seuraavissa kuvissa näkyvät muodossa käytetyt tietolähteet.

<a href="./media/ger-splitlistbylimit-datasources.png"><img src="./media/ger-splitlistbylimit-datasources.png" alt="Data sources" class="alignnone size-full wp-image-1204073" width="320" height="208" /></a>

Seuraavassa kuvassa on tulos, kun muoto suoritetaan. Tässä tapauksessa tuloksena muoto, joka on kauppatavaroiden jäsentämätön luettelo.

<a href="./media/ger-splitlistbylimit-output.png"><img src="./media/ger-splitlistbylimit-output.png" alt="Output" class="alignnone size-full wp-image-1204083" width="462" height="204" /></a>

Seuraavissa kuvissa sama muoto on säädetty ilmaisemaan kauppatavarat erinä, jos yhdessä erässä on oltava kauppatavaroita, joiden kokonaispaino ei saa olla suurempi kuin 9.

<a href="./media/ger-splitlistbylimit-format-1.png"><img src="./media/ger-splitlistbylimit-format-1.png" alt="Adjusted format" class="alignnone size-full wp-image-1204103" width="466" height="438" /></a>

<a href="./media/ger-splitlistbylimit-datasources-1.png"><img src="./media/ger-splitlistbylimit-datasources-1.png" alt="Data sources for the adjusted format" class="alignnone size-full wp-image-1204093" width="645" height="507" /></a>

Seuraavassa kuvassa on tulos, kun säädetty muoto suoritetaan.

<a href="./media/ger-splitlistbylimit-output-1.png"><img src="./media/ger-splitlistbylimit-output-1.png" alt="Output of the adjusted format" class="alignnone size-full wp-image-1204113" width="676" height="611" /></a>

> [!NOTE] 
> Rajaa ei sovellettu alkuperäisen luettelon viimeiseen nimikkeeseen, koska arvo (**11**) ylittää lähteen (**painon**) määritetyn raja-arvon (**9**). Ohita alaluettelot raportin luomisen aikana käyttämällä joko `WHERE`-funktiota tai vastaavan muodon elementin **Käytössä**-lauseketta tarvittaessa.

## <a name="additional-resources"></a>Lisäresurssit

[Luettelotoiminnot](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]