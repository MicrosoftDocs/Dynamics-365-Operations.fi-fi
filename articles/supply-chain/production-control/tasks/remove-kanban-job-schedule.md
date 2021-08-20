---
title: Poista kanban-työ aikataulusta
description: Tässä menettelyssä keskitytään prosessin suunnitellun kanban-työn poistamiseen aikataulusta palauttamalla työn tilaksi Ei suunniteltu.
author: ChristianRytt
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanJobSchedulingListPage, SysLookupMultiSelectGrid, KanbanJobStatusUpdate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: eeedfad5f294f73097fc1b6a973d63125df72209227fc06470663665961af2d4
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6756916"
---
# <a name="remove-a-kanban-job-from-the-schedule"></a>Poista kanban-työ aikataulusta

[!include [banner](../../includes/banner.md)]

Tässä menettelyssä keskitytään prosessin suunnitellun kanban-työn poistamiseen aikataulusta palauttamalla työn tilaksi Ei suunniteltu. Tämän menettelyn luomisessa käytetty esittely-yritys on USMF. Tämä menettely on tarkoitettu työn ohjauksen esimiehelle tai tuotannon suunnittelijalle.


## <a name="find-a-planned-kanban-job"></a>Suunnitellun kanban-työn etsiminen
1. Siirry kohtaan Tuotannonhallinta > Kanban > Kanban-työn aikataulutus.
2. Avaa haku valitsemalla Työsolu-kentässä avattavan valikon painike.
3. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
    * Valitse työsolu 1250.  
4. Klikkaa Valitse.
5. Valitse Näytä työn tila -kentässä Ajoitettu.

## <a name="remove-the-planned-kanban-job-from-the-schedule"></a>Suunnitellun kanban-työn poistaminen aikataulusta
1. Etsi haluamasi tietue luettelosta ja valitse se.
    * Valitse työ, jonka tila on Suunniteltu. Voit valita esimerkiksi työn, jonka päivämäärä on 19.12.2012.  
2. Valitse toimintoruudussa Suunnitelma.
3. Valitse Palauta työn tila.
4. Valitse OK.
    * Tällöin työn nykyinen tila muuttuu Suunniteltu-tilasta Ei suunniteltu -tilaan, ja työ poistetaan prosessitaululta.   



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]