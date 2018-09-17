--- 
title: "Luo ennalta määritetyt tuotevariantit"
description: "Tässä menettelyssä selvitetään tuotevariantien luonti päätuotteelle käyttämällä tuotedimensioiden yhdistelmiä."
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResProductListPage, EcoResProductCreate, EcoResProductDetails, EcoResProductMasterDimension, EcoResProductVariants, EcoResProductVariantSuggestions
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: c49d25004b19084276404cf887188e89200afa32
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---
# <a name="create-predefined-product-variants"></a>Luo ennalta määritetyt tuotevariantit

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tässä menettelyssä selvitetään tuotevariantien luonti päätuotteelle käyttämällä tuotedimensioiden yhdistelmiä. Tämän menettelyn luomiseen on käytetty USMF-demoyritystä.


## <a name="create-a-product-master"></a>Luo päätuote
1. Siirry kohtaan Tuotetietojen hallinta > Tuotteet > Päätuotteet.
2. Valitse Uusi.
3. Kirjoita arvo Tuotenumero-kenttään.
    * Tuotetunnuksen antaminen manuaalisesti on pakollista vain, jos tuotetunnuskenttään ei ole määritetty numerosarjaa. Toisin sanoen, tämän vaiheen voi ohittaa, jos kentälle on määritetty numerosarja.  
4. Kirjoita arvo Tuotteen nimi -kenttään.
5. Syötä tai valitse arvo Tuotedimension ryhmä -kentässä.
    * Valitse tuotedimensioryhmäksi SizeCol (koko ja väri).  
6. Valitse OK.

## <a name="add-product-dimensions"></a>Lisää tuotedimensiot
1. Valitse Tuotedimensiot.
    * Tässä esimerkissä havainnollistetaan, kuinka tuotedimensiot voi antaa käsin. Voit myös valita koko-, väri- tai tyyliryhmän, joka sisältää haluamasi tuotedimension arvot.  
2. Valitse Uusi.
3. Merkitse valittu rivi luettelossa.
4. Syötä tai valitse arvo Koko-kenttään.
5. Kirjoita arvo Nimi-kenttään.
6. Valitse Uusi.
7. Merkitse valittu rivi luettelossa.
8. Syötä tai valitse arvo Koko-kenttään.
9. Kirjoita arvo Nimi-kenttään.
10. Valitse Värit-välilehti.
11. Valitse Uusi.
12. Merkitse valittu rivi luettelossa.
13. Syötä tai valitse Väri-kentän arvo.
14. Kirjoita arvo Nimi-kenttään.
15. Valitse Uusi.
16. Merkitse valittu rivi luettelossa.
17. Syötä tai valitse Väri-kentän arvo.
18. Kirjoita arvo Nimi-kenttään.
19. Valitse Tallenna.
20. Sulje sivu.

## <a name="generate-product-variants"></a>Luo tuotevariantit
1. Valitse Tuotevariantin koot.
2. Valitse Muuttujaehdotukset.
3. Valitse Valitse kaikki.
    * Tässä esimerkissä kaikki mahdolliset muuttujat on valittu. Jos ainoastaan saatavilla olevien tuotedimensioyhdistelmien alijoukkoa käytetään varianttien luomiseen, voit valita yksittäisiä merkintöjä.  
4. Valitse Luo.
    * Voit luoda kuvaukset kaikille varianteille tuotedimensioarvojen yhdistelmien perusteella. Kuvaukset ovat valinnaisia.  
5. Valitse Tallenna.


