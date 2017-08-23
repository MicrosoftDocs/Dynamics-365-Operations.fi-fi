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
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 5f101a097643fa027a667b9d6577fbe5d24ecd27
ms.contentlocale: fi-fi
ms.lasthandoff: 07/27/2017

---
# <a name="move-scheduled-kanban-jobs"></a>Siirrä aikataulutetut kanban-työt

[!include[task guide banner](../../includes/task-guide-banner.md)]

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


