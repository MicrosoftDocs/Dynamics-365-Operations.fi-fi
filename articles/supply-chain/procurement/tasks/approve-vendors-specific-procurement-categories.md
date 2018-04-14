--- 
title: "Hyväksy toimittajia tiettyihin hankintaluokkiin"
description: "Ostoehdotusta luotaessa saattaa olla tarpeen valita hyväksytty tai ensisijainen toimittaja sen mukaan, miten ostokäytännöt on määritetty."
author: mkirknel
manager: AnnBe
ms.date: 08/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 3ee04497653b21600cd42fa9c90e7876e613acee
ms.contentlocale: fi-fi
ms.lasthandoff: 04/13/2018

---
# <a name="approve-vendors-for-specific-procurement-categories"></a><span data-ttu-id="aa4df-103">Hyväksy toimittajia tiettyihin hankintaluokkiin</span><span class="sxs-lookup"><span data-stu-id="aa4df-103">Approve vendors for specific procurement categories</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="aa4df-104">Ostoehdotusta luotaessa saattaa olla tarpeen valita hyväksytty tai ensisijainen toimittaja sen mukaan, miten ostokäytännöt on määritetty.</span><span class="sxs-lookup"><span data-stu-id="aa4df-104">When a purchase requisition is created, there may be a requirement to select an approved or preferred vendor, depending on how the purchasing policies are set up.</span></span> <span data-ttu-id="aa4df-105">Seuraavassa menettelyssä kuvataan, miten toimittaja määritetään hyväksytyksi tai ensisijaiseksi tietylle hankintaluokalle.</span><span class="sxs-lookup"><span data-stu-id="aa4df-105">This procedure shows you how to specify that a vendor is approved or preferred for a specific procurement category.</span></span> <span data-ttu-id="aa4df-106">Yleensä hankinta-asiantuntijat suorittavat tämän tehtävän.</span><span class="sxs-lookup"><span data-stu-id="aa4df-106">This task would usually be carried out by a procurement professional.</span></span> <span data-ttu-id="aa4df-107">Voit käyttää tätä menettelyä esittely-yrityksessä USMF.</span><span class="sxs-lookup"><span data-stu-id="aa4df-107">You can use this procedure in demo data company USMF.</span></span>

1. <span data-ttu-id="aa4df-108">Valitse Hankinta > Toimittajat > Kaikki toimittajat.</span><span class="sxs-lookup"><span data-stu-id="aa4df-108">Go to Procurement and sourcing > Vendors > All vendors.</span></span>
2. <span data-ttu-id="aa4df-109">Valitse toimittaja, jonka haluat määrittää hyväksytyksi tai ensisijaiseksi tietylle luokalle.</span><span class="sxs-lookup"><span data-stu-id="aa4df-109">Select the vendor that you want to set as an approved or preferred vendor for a category.</span></span>
3. <span data-ttu-id="aa4df-110">Valitse toimintoruudussa Yleiset.</span><span class="sxs-lookup"><span data-stu-id="aa4df-110">On the Action Pane, click General.</span></span>
4. <span data-ttu-id="aa4df-111">Valitse Luokat.</span><span class="sxs-lookup"><span data-stu-id="aa4df-111">Click Categories.</span></span>
5. <span data-ttu-id="aa4df-112">Valitse Lisää luokka.</span><span class="sxs-lookup"><span data-stu-id="aa4df-112">Click Add category.</span></span>
6. <span data-ttu-id="aa4df-113">Valitse Luokka-kenttään TOIMISTON JA TYÖPÖYDÄN LISÄVARUSTEET (TOIMISTON JA TYÖPÖYDÄN LISÄVARUSTEET).</span><span class="sxs-lookup"><span data-stu-id="aa4df-113">In the Category field, select OFFICE AND DESK ACCESSORIES (OFFICE AND DESK ACCESSORIES).</span></span>
7. <span data-ttu-id="aa4df-114">Valitse Toimittajaluokan tila -kenttään "Ensisijainen".</span><span class="sxs-lookup"><span data-stu-id="aa4df-114">In the Vendor category status field, select 'Preferred'.</span></span>
    * <span data-ttu-id="aa4df-115">Luokalle on mahdollista määrittää useampi kuin yksi ensisijainen toimittaja.</span><span class="sxs-lookup"><span data-stu-id="aa4df-115">It’s possible to specify more than one preferred vendor for a category.</span></span>  
8. <span data-ttu-id="aa4df-116">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="aa4df-116">Click Save.</span></span>
9. <span data-ttu-id="aa4df-117">Valitse Hankinta > Hankintaluokat.</span><span class="sxs-lookup"><span data-stu-id="aa4df-117">Go to Procurement and sourcing > Procurement categories.</span></span>
10. <span data-ttu-id="aa4df-118">Valitse puusta "CORP PROCUREMENT CATEGORIES\OFFICE AND DESK ACCESSORIES".</span><span class="sxs-lookup"><span data-stu-id="aa4df-118">In the tree, select 'CORP PROCUREMENT CATEGORIES\OFFICE AND DESK ACCESSORIES'.</span></span>
11. <span data-ttu-id="aa4df-119">Laajenna Toimittajat-osa.</span><span class="sxs-lookup"><span data-stu-id="aa4df-119">Expand the Vendors section.</span></span>
    * <span data-ttu-id="aa4df-120">Tarkista, että valitsemasi toimittaja näkyy ensisijaisten toimittajien luettelossa Toimiston ja työpöydän lisävarusteet -luokassa.</span><span class="sxs-lookup"><span data-stu-id="aa4df-120">Check if the vendor that you selected  appears as a preferred vendor for the Office and desk accessories category.</span></span> <span data-ttu-id="aa4df-121">Jos käytät tätä menettelyä tehtäväoppaana, saatat joutua napsauttamaan lukituksen avauspainiketta voidaksesi selata alas toimittajaluetteloon.</span><span class="sxs-lookup"><span data-stu-id="aa4df-121">If you’re running this procedure as a task guide, you may have to click the Unlock button to be able to scroll down to the list of vendors.</span></span>  <span data-ttu-id="aa4df-122">On myös mahdollista lisätä ensisijaisia ja hyväksyttyjä toimittajia tällä sivulla.</span><span class="sxs-lookup"><span data-stu-id="aa4df-122">It’s also possible to add preferred and approved vendors on this page.</span></span>  
12. <span data-ttu-id="aa4df-123">Laajenna puussa "OFFICE AND DESK ACCESSORIES".</span><span class="sxs-lookup"><span data-stu-id="aa4df-123">In the tree, expand 'OFFICE AND DESK ACCESSORIES'.</span></span>
13. <span data-ttu-id="aa4df-124">Valitse puussa "Sakset".</span><span class="sxs-lookup"><span data-stu-id="aa4df-124">In the tree, select 'Scissors'.</span></span>
14. <span data-ttu-id="aa4df-125">Valitse Ei Peri toimittajat ylemmän tason luokalta -kenttään.</span><span class="sxs-lookup"><span data-stu-id="aa4df-125">Select No in the Inherit vendors from parent category: field.</span></span>
15. <span data-ttu-id="aa4df-126">Valitse Kyllä Peri toimittajat ylemmän tason luokalta -kenttään.</span><span class="sxs-lookup"><span data-stu-id="aa4df-126">Select Yes in the Inherit vendors from parent category: field.</span></span>


