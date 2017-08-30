--- 
title: "Edeltäjän lisääminen tuotantovirran tehtävään"
description: "Kaikkien tehtävien on oltava järjestyksessä tuotantovirran versiossa."
author: cvocph
manager: AnnBe
ms.date: 10/26/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: c1afd6a5c2eb5235a42fc9aeea0c8aed6d33e0c9
ms.contentlocale: fi-fi
ms.lasthandoff: 07/28/2017

---
# <a name="add-a-predecessor-to-a-production-flow-activity"></a>Edeltäjän lisääminen tuotantovirran tehtävään

[!include[task guide banner](../../includes/task-guide-banner.md)]

Kaikkien tehtävien on oltava järjestyksessä tuotantovirran versiossa. Tehtävällä voi olla yksi tai useampi edeltäjä tai seuraaja. 

Tässä menettelyssä kuvataan, miten liität tehtävään edeltäjän. 

Tämän tehtävän suorittamiseen tarvitset tuotantovirran, jossa on luonnosversio, jolla on vähintään kaksi yhdistettävää aktiviteetteihin. 

Lisätietoja on mietinnössä Lean-valmistuksen tuotantovirrat ja tehtävät.


## <a name="find-the-production-flow-and-version"></a>Etsi tuotantovirta ja versio
1. Valitse Tuotannonhallinta > Asetukset > Lean-tuotantovirta > Tuotantovirrat.
2. Etsi haluamasi tietue luettelosta ja valitse se.
3. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
4. Etsi haluamasi tietue luettelosta ja valitse se.
5. Valitse Tehtävät.

## <a name="select-an-activity-and-add-a-predecessor"></a>Valitse tehtävä ja lisää edeltäjä
1. Etsi haluamasi tietue luettelosta ja valitse se.
2. Valitse Lisää edeltäjä.
3. Syötä tai valitse arvo Tehtävä-kenttään.
4. Lisää Syklin kestojen suhde -kenttään numero.
    * Tehtäväsuhteen oletusarvoinen syklin keston suhde on 1. Oletuksena on, että molemmat tehtävät suoritetaan samassa tahdissa eli niiden tahtiaika on sama. Jos edeltäjä suoritetaan suuremmalla nopeudella (alempi tahtiaika), suhteen pitäisi olla pienempi kuin 1; jos edeltäjä suoritetaan hitaammalla nopeudella (korkeampi tahtiaika) syklin kestosuhde on suurempi kuin 1.  
5. Valitse OK.

