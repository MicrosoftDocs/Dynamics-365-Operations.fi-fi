---
title: Siirrä aikataulutetut kanban-työt
description: Tässä menettelyssä keskitytään prosessin suunniteltujen kanban-töiden siirtämiseen toiseen kauteen.
author: ChristianRytt
manager: tfehr
ms.date: 11/07/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanJobSchedulingListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bb95bab2173cb45300560f59c394cd2d558fe69f
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/02/2020
ms.locfileid: "3206976"
---
# <a name="move-scheduled-kanban-jobs"></a>Siirrä aikataulutetut kanban-työt

[!include [banner](../../includes/banner.md)]

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
