---
title: Päivitä kanbanin tila
description: Kun kanban tyhjennetään vahingossa tai vastaanotettu kanban on tyhjennettävä, kanbanin tila tulee päivittää.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Kanban, KanbanResetEmpty
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 48dd5c3a878efb7413f461e76fde086030015b60
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/18/2020
ms.locfileid: "3146672"
---
# <a name="update-kanban-status"></a>Päivitä kanbanin tila

[!include [banner](../../includes/banner.md)]

Kun kanban tyhjennetään vahingossa tai vastaanotettu kanban on tyhjennettävä, kanbanin tila tulee päivittää. Tämän menettelyn luomisessa käytetty esittely-yritys on USMF. Tämä menettely on tarkoitettu tuotannon työnjohtajalle.


## <a name="find-the-kanban"></a>Paikanna kanban.
1. Valitse Tuotannonhallinta > Kanban > Kanbanit.
2. Avaa materiaalin käsittely-yksikön tilasarakkeen suodatin.
3. Valitse Tyhjennä.
    * Tämä palauttaa suodattimet.  
4. Käytä pikasuodatinta tietueiden etsimiseen. Voit esimerkiksi suodattaa Kortin numero -kenttää arvolla 000149.

## <a name="change-emptied-status-to-received-status"></a>Vaihda tila tyhjennetystä vastaanotetuksi.
1. Napsauta Palauta tyhjä materiaalin käsittely-yksikkö -kohtaa.
2. Valitse OK.
    * Huomaa, että materiaalin käsittely-yksikön tila on Vastaanotettu.  

## <a name="change-received-status-to-emptied-status"></a>Vaihda tila vastaanotetusta tyhjennetyksi.
1. Napsauta Tyhjennä kanban -kohtaa.
2. Merkitse valittu rivi luettelossa.
    * Huomaa, että materiaalin käsittely-yksikön tila on Tyhjennetty.  

