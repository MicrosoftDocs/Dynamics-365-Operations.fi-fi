---
title: Työntekijän konfiguroiminen
description: Tässä menettelyssä kerrotaan, miten määrität työntekijästä myyntiedustajan, joka on oikeutettu myyntipisteen myyntiprovisioihin.
author: jblucher
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CommissionSalesGroup, CommissionSalesMember, DirPartyLookup, HcmWorker
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: aee84f2dc39d2225985992fac0f9c20985ed9804
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/01/2020
ms.locfileid: "3022364"
---
# <a name="configure-a-worker"></a><span data-ttu-id="1eb89-103">Työntekijän konfiguroiminen</span><span class="sxs-lookup"><span data-stu-id="1eb89-103">Configure a worker</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="1eb89-104">Tässä menettelyssä kerrotaan, miten määrität työntekijästä myyntiedustajan, joka on oikeutettu myyntipisteen myyntiprovisioihin.</span><span class="sxs-lookup"><span data-stu-id="1eb89-104">This procedure demonstrates how to configure a worker as a sales representative who is eligible for commission on sales in POS.</span></span> <span data-ttu-id="1eb89-105">Menettely käyttää esittelytietojen USRT-yritystä.</span><span class="sxs-lookup"><span data-stu-id="1eb89-105">This procedure uses the USRT demo data company.</span></span>


## <a name="create-a-commission-sales-group-for-the-worker"></a><span data-ttu-id="1eb89-106">Luo työntekijälle myyntiprovisioryhmä</span><span class="sxs-lookup"><span data-stu-id="1eb89-106">Create a commission sales group for the worker</span></span>
1. <span data-ttu-id="1eb89-107">Valitse Myynti ja markkinointi > Provisiot > Myyntiryhmät.</span><span class="sxs-lookup"><span data-stu-id="1eb89-107">Go to Sales and marketing > Commissions > Sales groups.</span></span>
    * <span data-ttu-id="1eb89-108">Työntekijöitä voi liittää yhteen tai useampaan myyntiryhmään.</span><span class="sxs-lookup"><span data-stu-id="1eb89-108">Workers can be assigned to one or more sales groups.</span></span> <span data-ttu-id="1eb89-109">Myyntipisteessä voit valita minkä tahansa myyntiryhmän, joka sisältää työntekijöitä liikkeen osoitekirjasta.</span><span class="sxs-lookup"><span data-stu-id="1eb89-109">In POS, you can choose any sales group that contains workers from the store's address book.</span></span>  
2. <span data-ttu-id="1eb89-110">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="1eb89-110">Click New.</span></span>
3. <span data-ttu-id="1eb89-111">Kirjoita Ryhmä-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="1eb89-111">In the Group field, type a value.</span></span>
4. <span data-ttu-id="1eb89-112">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="1eb89-112">In the Name field, type a value.</span></span>
5. <span data-ttu-id="1eb89-113">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="1eb89-113">Click Save.</span></span>
6. <span data-ttu-id="1eb89-114">Valitse toimintoruudussa Yleiset.</span><span class="sxs-lookup"><span data-stu-id="1eb89-114">On the Action Pane, click General.</span></span>
7. <span data-ttu-id="1eb89-115">Valitse Myyjä.</span><span class="sxs-lookup"><span data-stu-id="1eb89-115">Click Sales rep.</span></span>
    * <span data-ttu-id="1eb89-116">Myyntiryhmä voi sisältää useamman kuin yhden työntekijän.</span><span class="sxs-lookup"><span data-stu-id="1eb89-116">A sales group can contain more than one worker.</span></span> <span data-ttu-id="1eb89-117">Provisiot voi jakaa työntekijöille sen mukaan, miten provisio-osuus on määritetty.</span><span class="sxs-lookup"><span data-stu-id="1eb89-117">Commissions can be split between workers based on how you define the commission share.</span></span>  
8. <span data-ttu-id="1eb89-118">Syötä tai valitse arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="1eb89-118">In the Name field, enter or select a value.</span></span>
9. <span data-ttu-id="1eb89-119">Kirjoita Provisio-osuus -kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="1eb89-119">In the Commission share field, enter a number.</span></span>
10. <span data-ttu-id="1eb89-120">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="1eb89-120">Click Save.</span></span>
11. <span data-ttu-id="1eb89-121">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="1eb89-121">Close the page.</span></span>
12. <span data-ttu-id="1eb89-122">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="1eb89-122">Close the page.</span></span>

## <a name="assign-the-workers-default-sales-group"></a><span data-ttu-id="1eb89-123">Määritä työntekijät oletusmyyntiryhmään</span><span class="sxs-lookup"><span data-stu-id="1eb89-123">Assign the workers default sales group</span></span>
1. <span data-ttu-id="1eb89-124">Siirry kohtaan Retail ja Commerce > Työntekijät > Työntekijät.</span><span class="sxs-lookup"><span data-stu-id="1eb89-124">Go to Retail and Commerce > Employees > Workers.</span></span>
2. <span data-ttu-id="1eb89-125">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="1eb89-125">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="1eb89-126">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="1eb89-126">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="1eb89-127">Valitse Comemrce-välilehti.</span><span class="sxs-lookup"><span data-stu-id="1eb89-127">Click the Commerce tab.</span></span>
    * <span data-ttu-id="1eb89-128">Työntekijä voidaan määrittää myynnin oletusryhmään.</span><span class="sxs-lookup"><span data-stu-id="1eb89-128">A worker can be assigned to a default sales group.</span></span> <span data-ttu-id="1eb89-129">Myynnin oletusryhmä automaattisesti lisätään automaattisesti myyntipisteen myyntiriveille, jos asetus on käytössä myymälän toimintoprofiilissa.</span><span class="sxs-lookup"><span data-stu-id="1eb89-129">The default sales group will be automatically added to sales lines in POS if the option is enabled in the functionality profile for the store.</span></span>  
5. <span data-ttu-id="1eb89-130">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="1eb89-130">Click Edit.</span></span>
6. <span data-ttu-id="1eb89-131">Syötä tai valitse arvo Oletusryhmä-kentässä.</span><span class="sxs-lookup"><span data-stu-id="1eb89-131">In the Default group field, enter or select a value.</span></span>
7. <span data-ttu-id="1eb89-132">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="1eb89-132">Click Save.</span></span>

