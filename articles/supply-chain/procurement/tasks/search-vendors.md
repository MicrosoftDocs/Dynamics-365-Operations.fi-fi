---
title: Toimittajien etsiminen
description: Opettele hakemaan toimittajia tiettyjen ehtojen perusteella.
author: RichardLuan
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendSearchCriterion, VendSearchAddCategory, VendSearchAddReviewCriterionGroup, VendSearchResults, VendSearchAddReviewCriterion
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7caa146532d2bce06b009c45da635327766a88d1
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/16/2021
ms.locfileid: "5020701"
---
# <a name="search-for-vendors"></a><span data-ttu-id="1f3b6-103">Toimittajien etsiminen</span><span class="sxs-lookup"><span data-stu-id="1f3b6-103">Search for vendors</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1f3b6-104">Opettele hakemaan toimittajia tiettyjen ehtojen perusteella.</span><span class="sxs-lookup"><span data-stu-id="1f3b6-104">Learn how to search for vendors based on specific criteria.</span></span> <span data-ttu-id="1f3b6-105">Tässä esimerkissä näytetään, miten voit hakea tiettyyn hankintaluokkaan hyväksyttyjä toimittajia ja miten saat heidän ensisijaisen osoitteen tietyssä maassa.</span><span class="sxs-lookup"><span data-stu-id="1f3b6-105">This example shows you how to search for vendors that are approved for a particular procurement category and have their primary address in a specific country.</span></span> <span data-ttu-id="1f3b6-106">Voit suorittaa tämän menettelyn USMF-demoyrityksen tiedoilla tai käyttää omia tietoja.</span><span class="sxs-lookup"><span data-stu-id="1f3b6-106">You can run this procedure in demo data company USMF, or on your own data.</span></span> <span data-ttu-id="1f3b6-107">Yleensä hankinta-asiantuntijat suorittavat tämän tehtävän.</span><span class="sxs-lookup"><span data-stu-id="1f3b6-107">This task would usually be carried out by a procurement professional.</span></span>

1. <span data-ttu-id="1f3b6-108">Valitse Hankinta > Toimittajat > Toimittajahaku.</span><span class="sxs-lookup"><span data-stu-id="1f3b6-108">Go to Procurement and sourcing > Vendors > Vendor search.</span></span>
2. <span data-ttu-id="1f3b6-109">Avaa Hankintaluokan valinta -sivu napsauttamalla plus-kuvaketta.</span><span class="sxs-lookup"><span data-stu-id="1f3b6-109">Click on the Plus icon to open the Procurement category selection page.</span></span>  
3. <span data-ttu-id="1f3b6-110">Valitse puusta CORP PROCUREMENT CATEGORIES\OFFICE MACHINES.</span><span class="sxs-lookup"><span data-stu-id="1f3b6-110">In the tree, select 'CORP PROCUREMENT CATEGORIES\OFFICE MACHINES'.</span></span>
    * <span data-ttu-id="1f3b6-111">Jos käytät menettelyä tehtävän ohjauksena, sinun on ehkä napsautettava Poista lukitus -painiketta, ennen kuin voit valita oikean solmun.</span><span class="sxs-lookup"><span data-stu-id="1f3b6-111">If you're running this procedure as a task guide, you may have to click the Unlock button before you can select the correct node.</span></span> <span data-ttu-id="1f3b6-112">Jos käytössä on USMF. valitse jokin käytössäsi olevista luokista.</span><span class="sxs-lookup"><span data-stu-id="1f3b6-112">If you're not using USMF, select one of the categories that you have.</span></span>  
4. <span data-ttu-id="1f3b6-113">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="1f3b6-113">Click Add.</span></span>
    * <span data-ttu-id="1f3b6-114">Useiden luokkien valitseminen on mahdollista.</span><span class="sxs-lookup"><span data-stu-id="1f3b6-114">It's possible to select more than one category here.</span></span> <span data-ttu-id="1f3b6-115">Haku etsii siinä tapauksessa kaikki toimittajat, jotka on hyväksytty vähintään yhteen luokkaan.</span><span class="sxs-lookup"><span data-stu-id="1f3b6-115">If you do so, the search will find all the vendors that are approved for at least one of the categories.</span></span>  
5. <span data-ttu-id="1f3b6-116">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="1f3b6-116">Click OK.</span></span>
6. <span data-ttu-id="1f3b6-117">Kirjoita arvo Maa/alue-kenttään.</span><span class="sxs-lookup"><span data-stu-id="1f3b6-117">In the Country/region field, type a value.</span></span>
7. <span data-ttu-id="1f3b6-118">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="1f3b6-118">Click OK.</span></span>

