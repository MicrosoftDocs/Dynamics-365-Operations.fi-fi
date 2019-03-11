---
title: Siirrä aikataulutetut kanban-työt
description: Tässä menettelyssä keskitytään prosessin suunniteltujen kanban-töiden siirtämiseen toiseen kauteen.
author: ChristianRytt
manager: AnnBe
ms.date: 11/07/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanJobSchedulingListPage
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f791c9048ef6efe1585c991f998099cd1fc12df7
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "310849"
---
# <a name="move-scheduled-kanban-jobs"></a>Siirrä aikataulutetut kanban-työt

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tässä menettelyssä keskitytään prosessin suunniteltujen kanban-töiden siirtämiseen toiseen kauteen. Tämän menettelyn luomisessa käytetty esittely-yritys on USMF. Tämä menettely on tarkoitettu työnohjauksen esimiehelle tai tuotannon suunnittelijalle, jotka käsittelevät kanbaneita.

## <a name="select-scheduled-kanban-jobs"></a>Valitse aikataulutetut kanban-työt. 

1. Valitse **Tuotannonhallinta > Kanban > Kanban-työn aikataulutus**. 

2. Avaa haku valitsemalla **Työsolu**-kentässä avattavan valikon painike. 

3. Merkitse valittu rivi luettelossa. 
   - Valitse työsolu 1250. 
4. Klikkaa **Valitse**. 

5. Valitse **Näytä työn tila** -kentässä **Ajoitettu**. Tämä suodattaa työluettelon niin, että vain aikataulutetut kanban-työt näkyvät. 

## <a name="move-kanban-jobs-to-a-different-period"></a>Siirrä kanban-työt toiseen jaksoon. 

1. Etsi haluamasi tietue luettelosta ja valitse se. Valitse työ, jonka työn tila on **Suunniteltu**. Voit valita, **Suunniteltu kausi** -kentässä esimerkiksi työn, joka on aikataulutettu suoritettavaksi 20.12.2012. Siirrä sitten työ edelliseen kauteen. 

2. Valitse **Edellinen jakso**. 

3. Siirrä työ työluettelon loppuun valitsemalla **Loppu**, koska sitä pidetään edellisen kauden viimeisenä työnä. 

4. Etsi haluamasi tietue luettelosta ja valitse se. Valitse työ, jonka työn tila on **Suunniteltu**. Voit valita **Suunniteltu kausi** -kentässä esimerkiksi työn, joka on aikataulutettu suoritettavaksi 18.12.2012. Siirrä sitten työ seuraavaan kauteen. 

5. Valitse **Seuraava jakso**. 

6. Siirrä työ työluettelon alkuun valitsemalla **Alku**, koska sitä pidetään edellisen kauden ensimmäisenä työnä. 

## <a name="move-a-job-within-a-period"></a>Siirrä työtä kauden sisällä. 

1. Etsi haluamasi tietue luettelosta ja valitse se. Valitse työ, jonka työn tila on Suunniteltu. Voit valita **Suunniteltu kausi** -kentässä esimerkiksi toisen työn, joka on aikataulutettu suoritettavaksi 19.12.2012. Siirrä sitten työtä kauden sisällä. 

2. Valitse **Eteenpäin**. Huomaa, että työtä siirrettiin yksi rivi alaspäin luettelossa. 

3. Valitse **Taaksepäin**. Huomaa, että työtä siirrettiin yksi rivi ylöspäin luettelossa.
