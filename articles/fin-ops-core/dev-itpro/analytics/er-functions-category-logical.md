---
title: Luettelo ER-funktioista loogisessa luokassa
description: Tässä artikkelissa on tietoja sähköisen raportoinnin (ER) tukemista loogisista funktioista.
author: kfend
ms.date: 02/11/2021
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
ms.openlocfilehash: 1d011968d9cfa4125e7283ca36c3558e3e79b93a
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9291291"
---
# <a name="list-of-er-functions-in-the-logical-category"></a>Luettelo ER-funktioista loogisessa luokassa

[!include [banner](../includes/banner.md)]

Sähköisten raportointitoimintojen loogisia funktioita voidaan käyttää loogisten arvojen tekemiseen, jotta voit suorittaa useamman kuin yhden vertailun yksittäisessä lausekkeessa tai testata useita ehtoja. Tässä artikkelissa on yhteenveto näistä funktioista.

## <a name="list-of-supported-functions"></a>Luettelo tuetuista toiminnoista

| Toiminto | Kuvaus |
|----------|-------------|
| [Ja](er-functions-logical-and.md)                       | Tämä funktio palauttaa *totuusarvon* **TOSI**, jos kaikki määritetyt ehdot toteutuvat. Muussa tapauksessa se palauttaa *totuusarvon* **EPÄTOSI**. |
| [Laatikko](er-functions-logical-case.md)                     | Tämä funktio arvioi määritetyn lausekkeen arvon määritettyjen vaihtoehtoisten asetusten mukaan ja palauttaa ensimmäisen vaihtoehdon tuloksen, joka on yhtä suuri kuin määritetyn lausekkeen arvo. Muussa tapauksessa se palauttaa valinnaisen oletustuloksen, jos oletustulos määritetään kutsutussa funktiossa viimeisenä argumenttina, jota ei edellä vaihtoehto. Palautettava arvo voi olla minkä tahansa tuettujen tietotyyppien arvo. |
| [Sisältää](er-functions-logical-contains.md)             | Tämä funktio määrittää, sisältääkö määritetty syöte määritetyn tekstin. Se palauttaa *totuus*-arvon **TOSI**, jos määritetty syöte sisältää määritetyn tekstin. Muussa tapauksessa se palauttaa *totuusarvon* **EPÄTOSI**. |
| [EndsWith](er-functions-logical-endswith.md)             | Tämä funktio määrittää, loppuuko määritetty syöte määritettyyn tekstiin. Se palauttaa *totuus*-arvon **TOSI**, jos määritetty syöte loppuu määritetyllä tekstillä. Muussa tapauksessa se palauttaa *totuusarvon* **EPÄTOSI**. |
| [Jos](er-functions-logical-if.md)                         | Tämä funktio palauttaa ensimmäisen määritetyn arvon, jos määritetyt ehdot täyttyvät. Muussa tapauksessa se palauttaa toisen määritetyn arvon. Palautettava arvo voi olla minkä tahansa tuettujen tietotyyppien arvo. |
| [Ei](er-functions-logical-not.md)                       | Tämä funktio palauttaa määritetyn ehdon käänteisen loogisen arvon *totuusarvoksi*. |
| [Or](er-functions-logical-or.md)                         | Tämä funktio palauttaa *totuusarvon* **EPÄTOSI**, jos mikään määritetty ehto ei toteudu. Jos joku määritetty ehto toteutuu, tämä funktio palauttaa *totuusarvon* **TOSI**. |
| [StartsWith](er-functions-logical-startswith.md)         | Tämä funktio määrittää, alkaako määritetty syöte määritetyllä tekstillä. Se palauttaa *totuus*-arvon **TOSI**, jos määritetty syöte alkaa määritetyllä tekstillä. Muussa tapauksessa se palauttaa *totuusarvon* **EPÄTOSI**. |
| [ValueIn](er-functions-logical-valuein.md)               | Tämä funktio määrittää, vastaako määritetty syöte määritetyn luettelokohteen tiettyä arvoa. Se palauttaa *totuusarvon* arvon **TOSI**, jos määritetty syöte vastaa määritetyn lausekkeen suorittamisen tulosta vähintään yhdelle määritetyn luettelon tietueelle. Muussa tapauksessa se palauttaa *totuusarvon* **EPÄTOSI**. |
| [ValueInLarge](er-functions-logical-valueinlarge.md)     | Tämä funktio määrittää, vastaako määritetty *Int64*- tai *Kokonaisluku*-tyyppi määritetyn luettelokohteen tiettyä arvoa. Se palauttaa *totuusarvon* arvon **TOSI**, jos määritetty syöte vastaa määritetyn lausekkeen suorittamisen tulosta vähintään yhdelle määritetyn luettelon tietueelle. Muussa tapauksessa se palauttaa *totuusarvon* **EPÄTOSI**. |


## <a name="additional-resources"></a>Lisäresurssit

[Sähköisen raportoinnin yleiskatsaus](general-electronic-reporting.md)

[Sähköisen raportoinnin kaavojen suunnittelutoiminto](general-electronic-reporting-formula-designer.md)

[Sähköisen raportoinnin kaavakieli](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
