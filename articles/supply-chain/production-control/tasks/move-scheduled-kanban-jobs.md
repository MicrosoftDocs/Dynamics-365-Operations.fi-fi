--- 
title: "Siirrä aikataulutetut kanban-työt"
description: "Tässä menettelyssä keskitytään prosessin suunniteltujen kanban-töiden siirtämiseen toiseen kauteen."
author: ChristianRytt
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 2a12a6859a3a436706822873bc6fdd781e0ef032
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---
# <a name="move-scheduled-kanban-jobs"></a>Siirrä aikataulutetut kanban-työt

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Tässä menettelyssä keskitytään prosessin suunniteltujen kanban-töiden siirtämiseen toiseen kauteen. Tämän menettelyn luomisessa käytetty esittely-yritys on USMF. Tämä menettely on tarkoitettu työnohjauksen esimiehelle tai tuotannon suunnittelijalle, jotka käsittelevät kanbaneita.


## <a name="select-scheduled-kanban-jobs"></a>Aikataulutettujen kanban-töiden valitseminen
1. Gå til Produktionsstyring > Kanban > Tidsplanlægning af kanban-job.
2. !MtCMR!IAvaa haku valitsemalla Työsolu-kentässä avattavan valikon painike. áçêìõý !
3. Markér den valgte række på listen.
    * Valitse työsolu 1250.  
4. Klik på Select.
5. Vælg 'Planlagt' i feltet Display job status.
    * Tämä suodattaa työluettelon niin, että vain aikataulutetut kanban-työt näkyvät.  

## <a name="move-kanban-jobs-to-a-different-period"></a>Kanban-töiden siirtäminen toiseen kauteen
1. Find og vælg den ønskede post på listen.
    * Valitse työ, jonka työn tila on Suunniteltu. Voit valita esimerkiksi työn, joka on aikataulutettu suoritettavaksi 20.12.2012 Suunniteltu kausi -kentässä. Siirrä sitten työ edelliseen kauteen.  
2. Klik på Previous period.
3. Klik på End.
    * Nyt työ siirretään työluettelon loppuun, koska sitä pidetään edellisen kauden viimeisenä työnä.  
4. Find og vælg den ønskede post på listen.
    * Valitse työ, jonka työn tila on Suunniteltu. Voit valita Suunniteltu kausi -kentässä esimerkiksi työn, joka on aikataulutettu suoritettavaksi 18.12.2012. Siirrä sitten työ seuraavaan kauteen.  
5. Klik på Next period.
6. Klik på Start.
    * Nyt työ siirretään työluettelon alkuun, koska sitä pidetään edellisen kauden ensimmäisenä työnä.  

## <a name="task-move-a-job-within-a-period"></a>Tehtävä: Työn siirtäminen kauden sisällä
1. Find og vælg den ønskede post på listen.
    * Valitse työ, jonka työn tila on Suunniteltu. Voit valita esimerkiksi toisen työn, joka on aikataulutettu suoritettavaksi 19.12.2012 Suunniteltu kausi -kentässä. Siirrä sitten työtä kauden sisällä.  
2. Klik på Forward.
    * Huomaa, että työtä siirrettiin yksi rivi alaspäin luettelossa.  
3. Klik på Backward.
    * Huomaa, että työtä siirrettiin yksi rivi ylöspäin luettelossa.  


