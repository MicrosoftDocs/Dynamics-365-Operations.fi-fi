---
title: Toimittajien etsiminen
description: Opettele hakemaan toimittajia tiettyjen ehtojen perusteella.
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendSearchCriterion, VendSearchAddCategory
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 86fced38d0ac73e67d04a59c5f39f4ec9b192daa
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "311470"
---
# <a name="search-for-vendors"></a><span data-ttu-id="38619-103">Toimittajien etsiminen</span><span class="sxs-lookup"><span data-stu-id="38619-103">Search for vendors</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="38619-104">Opettele hakemaan toimittajia tiettyjen ehtojen perusteella.</span><span class="sxs-lookup"><span data-stu-id="38619-104">Learn how to search for vendors based on specific criteria.</span></span> <span data-ttu-id="38619-105">Tässä esimerkissä näytetään, miten voit hakea tiettyyn hankintaluokkaan hyväksyttyjä toimittajia ja miten saat heidän ensisijaisen osoitteen tietyssä maassa.</span><span class="sxs-lookup"><span data-stu-id="38619-105">This example shows you how to search for vendors that are approved for a particular procurement category and have their primary address in a specific country.</span></span> <span data-ttu-id="38619-106">Voit suorittaa tämän menettelyn USMF-demoyrityksen tiedoilla tai käyttää omia tietoja.</span><span class="sxs-lookup"><span data-stu-id="38619-106">You can run this procedure in demo data company USMF, or on your own data.</span></span> <span data-ttu-id="38619-107">Yleensä hankinta-asiantuntijat suorittavat tämän tehtävän.</span><span class="sxs-lookup"><span data-stu-id="38619-107">This task would usually be carried out by a procurement professional.</span></span>

1. <span data-ttu-id="38619-108">Valitse Hankinta > Toimittajat > Toimittajahaku.</span><span class="sxs-lookup"><span data-stu-id="38619-108">Go to Procurement and sourcing > Vendors > Vendor search.</span></span>
2. <span data-ttu-id="38619-109">Avaa Hankintaluokan valinta -sivu napsauttamalla plus-kuvaketta.</span><span class="sxs-lookup"><span data-stu-id="38619-109">Click on the Plus icon to open the Procurement category selection page.</span></span>  
3. <span data-ttu-id="38619-110">Valitse puusta CORP PROCUREMENT CATEGORIES\OFFICE MACHINES.</span><span class="sxs-lookup"><span data-stu-id="38619-110">In the tree, select 'CORP PROCUREMENT CATEGORIES\OFFICE MACHINES'.</span></span>
    * <span data-ttu-id="38619-111">Jos käytät menettelyä tehtävän ohjauksena, sinun on ehkä napsautettava Poista lukitus -painiketta, ennen kuin voit valita oikean solmun.</span><span class="sxs-lookup"><span data-stu-id="38619-111">If you're running this procedure as a task guide, you may have to click the Unlock button before you can select the correct node.</span></span> <span data-ttu-id="38619-112">Jos käytössä on USMF. valitse jokin käytössäsi olevista luokista.</span><span class="sxs-lookup"><span data-stu-id="38619-112">If you're not using USMF, select one of the categories that you have.</span></span>  
4. <span data-ttu-id="38619-113">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="38619-113">Click Add.</span></span>
    * <span data-ttu-id="38619-114">Useiden luokkien valitseminen on mahdollista.</span><span class="sxs-lookup"><span data-stu-id="38619-114">It’s possible to select more than one category here.</span></span> <span data-ttu-id="38619-115">Haku etsii siinä tapauksessa kaikki toimittajat, jotka on hyväksytty vähintään yhteen luokkaan.</span><span class="sxs-lookup"><span data-stu-id="38619-115">If you do so, the search will find all the vendors that are approved for at least one of the categories.</span></span>  
5. <span data-ttu-id="38619-116">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="38619-116">Click OK.</span></span>
6. <span data-ttu-id="38619-117">Kirjoita arvo Maa/alue-kenttään.</span><span class="sxs-lookup"><span data-stu-id="38619-117">In the Country/region field, type a value.</span></span>
7. <span data-ttu-id="38619-118">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="38619-118">Click OK.</span></span>

