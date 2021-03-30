---
title: Prosessin kanban-työn valmisteleminen kun materiaalit ovat käytettävissä työsolulle
description: Tässä tehtävässä keskitytään prosessin kanban-työn valmistelemiseen silloin, kun kaikki työsolun materiaalit ovat käytettävissä.
author: johanhoffmann
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanBoardWorkCell
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bde7a52e092723f9c6a686cb79080656c8de964c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5204589"
---
# <a name="prepare-a-process-kanban-job-when-materials-are-available-for-the-work-cell"></a><span data-ttu-id="cfd75-103">Prosessin kanban-työn valmisteleminen kun materiaalit ovat käytettävissä työsolulle</span><span class="sxs-lookup"><span data-stu-id="cfd75-103">Prepare a process kanban job when materials are available for the work cell</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="cfd75-104">Tässä tehtävässä keskitytään prosessin kanban-työn valmistelemiseen silloin, kun kaikki työsolun materiaalit ovat käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="cfd75-104">This task focuses on preparing a process kanban job when all materials are available for the work cell.</span></span> <span data-ttu-id="cfd75-105">Tämän tehtävän luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="cfd75-105">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="cfd75-106">Tämä tehtävä on tarkoitettu koneenkäyttäjille.</span><span class="sxs-lookup"><span data-stu-id="cfd75-106">This task is intended for the machine operator.</span></span>

1. <span data-ttu-id="cfd75-107">Siirry Prosessitöiden kanban-taulu -kohtaan.</span><span class="sxs-lookup"><span data-stu-id="cfd75-107">Go to Kanban board for process jobs.</span></span>
2. <span data-ttu-id="cfd75-108">Avaa haku valitsemalla Työsolu-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="cfd75-108">In the Work cell field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="cfd75-109">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="cfd75-109">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="cfd75-110">Valitse työsolu 1250 ja valitse sitten OK.</span><span class="sxs-lookup"><span data-stu-id="cfd75-110">Select work cell 1250 and click OK.</span></span>  
4. <span data-ttu-id="cfd75-111">Valitse luettelosta rivi 4.</span><span class="sxs-lookup"><span data-stu-id="cfd75-111">In the list, select row 4.</span></span>
    * <span data-ttu-id="cfd75-112">Tyhjässä esittely-yrityksessä rivillä 4 oleva kanban 000329 on ensimmäinen työ, jota ei ole vielä suoritettu.</span><span class="sxs-lookup"><span data-stu-id="cfd75-112">In the clean demo company, Kanban 000329 in row 4 is the first job that is not completed yet.</span></span>  
5. <span data-ttu-id="cfd75-113">Ota käyttöön Keräysluettelo-osan laajennus.</span><span class="sxs-lookup"><span data-stu-id="cfd75-113">Toggle the expansion of the Picking list section.</span></span>
    * <span data-ttu-id="cfd75-114">Varmista, että kaikkien keräysluettelon nimikkeiden toimituksen tila on käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="cfd75-114">Verify that the supply status is available for all items in the picking list.</span></span>  
    * <span data-ttu-id="cfd75-115">Jos valittuna on useita töitä, keräysluettelossa näkyy kaikkien valittujen töiden vaatimien nimikkeiden kokonaismäärä.</span><span class="sxs-lookup"><span data-stu-id="cfd75-115">If multiple jobs are selected, the picking list will show the sum of all items needed for the selected jobs.</span></span>  
6. <span data-ttu-id="cfd75-116">Valitse Valmistele.</span><span class="sxs-lookup"><span data-stu-id="cfd75-116">Click Prepare.</span></span>
    * <span data-ttu-id="cfd75-117">Prosessin valmistelu on nyt valmis.</span><span class="sxs-lookup"><span data-stu-id="cfd75-117">The preparation process is now completed.</span></span> <span data-ttu-id="cfd75-118">Keräysluettelon rivien valintaruutujen valinta osoittaa, niiden toimituksen tila on Kerätty.</span><span class="sxs-lookup"><span data-stu-id="cfd75-118">The selected check box for all rows in the picking list indicates that the supply status is picked.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]