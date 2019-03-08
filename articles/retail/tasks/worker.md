---
title: Työntekijän konfiguroiminen
description: Tässä menettelyssä kerrotaan, miten määrität vähittäismyynnin työntekijästä myyntiedustajan, joka on oikeutettu myyntipisteen myyntiprovisioihin.
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
ms.openlocfilehash: 797640b487884fc487582addea274007e4ba7a7d
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "362530"
---
# <a name="configure-a-worker"></a><span data-ttu-id="8907e-103">Työntekijän konfiguroiminen</span><span class="sxs-lookup"><span data-stu-id="8907e-103">Configure a worker</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="8907e-104">Tässä menettelyssä kerrotaan, miten määrität vähittäismyynnin työntekijästä myyntiedustajan, joka on oikeutettu myyntipisteen myyntiprovisioihin.</span><span class="sxs-lookup"><span data-stu-id="8907e-104">This procedure demonstrates how to configure a retail worker as a sales representative who is eligible for commission on sales in POS.</span></span> <span data-ttu-id="8907e-105">Menettely käyttää esittelytietojen USRT-yritystä.</span><span class="sxs-lookup"><span data-stu-id="8907e-105">This procedure uses the USRT demo data company.</span></span>


## <a name="create-a-commission-sales-group-for-the-worker"></a><span data-ttu-id="8907e-106">Luo työntekijälle myyntiprovisioryhmä</span><span class="sxs-lookup"><span data-stu-id="8907e-106">Create a commission sales group for the worker</span></span>
1. <span data-ttu-id="8907e-107">Valitse Myynti ja markkinointi > Provisiot > Myyntiryhmät.</span><span class="sxs-lookup"><span data-stu-id="8907e-107">Go to Sales and marketing > Commissions > Sales groups.</span></span>
    * <span data-ttu-id="8907e-108">Työntekijöitä voi liittää yhteen tai useampaan myyntiryhmään.</span><span class="sxs-lookup"><span data-stu-id="8907e-108">Workers can be assigned to one or more sales groups.</span></span> <span data-ttu-id="8907e-109">Myyntipisteessä voit valita minkä tahansa myyntiryhmän, joka sisältää työntekijöitä liikkeen osoitekirjasta.</span><span class="sxs-lookup"><span data-stu-id="8907e-109">In POS, you can choose any sales group that contains workers from the store's address book.</span></span>  
2. <span data-ttu-id="8907e-110">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="8907e-110">Click New.</span></span>
3. <span data-ttu-id="8907e-111">Kirjoita Ryhmä-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="8907e-111">In the Group field, type a value.</span></span>
4. <span data-ttu-id="8907e-112">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="8907e-112">In the Name field, type a value.</span></span>
5. <span data-ttu-id="8907e-113">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="8907e-113">Click Save.</span></span>
6. <span data-ttu-id="8907e-114">Valitse toimintoruudussa Yleiset.</span><span class="sxs-lookup"><span data-stu-id="8907e-114">On the Action Pane, click General.</span></span>
7. <span data-ttu-id="8907e-115">Valitse Myyjä.</span><span class="sxs-lookup"><span data-stu-id="8907e-115">Click Sales rep.</span></span>
    * <span data-ttu-id="8907e-116">Myyntiryhmä voi sisältää useamman kuin yhden työntekijän.</span><span class="sxs-lookup"><span data-stu-id="8907e-116">A sales group can contain more than one worker.</span></span> <span data-ttu-id="8907e-117">Provisiot voi jakaa työntekijöille sen mukaan, miten provisio-osuus on määritetty.</span><span class="sxs-lookup"><span data-stu-id="8907e-117">Commissions can be split between workers based on how you define the commission share.</span></span>  
8. <span data-ttu-id="8907e-118">Syötä tai valitse arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="8907e-118">In the Name field, enter or select a value.</span></span>
9. <span data-ttu-id="8907e-119">Kirjoita Provisio-osuus -kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="8907e-119">In the Commission share field, enter a number.</span></span>
10. <span data-ttu-id="8907e-120">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="8907e-120">Click Save.</span></span>
11. <span data-ttu-id="8907e-121">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="8907e-121">Close the page.</span></span>
12. <span data-ttu-id="8907e-122">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="8907e-122">Close the page.</span></span>

## <a name="assign-the-workers-default-sales-group"></a><span data-ttu-id="8907e-123">Määritä työntekijät oletusmyyntiryhmään</span><span class="sxs-lookup"><span data-stu-id="8907e-123">Assign the workers default sales group</span></span>
1. <span data-ttu-id="8907e-124">Siirry kohtaan Vähittäismyynti ja kauppa > Työntekijät > Työntekijät.</span><span class="sxs-lookup"><span data-stu-id="8907e-124">Go to Retail and commerce > Employees > Workers.</span></span>
2. <span data-ttu-id="8907e-125">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="8907e-125">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="8907e-126">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="8907e-126">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="8907e-127">Valitse Vähittäismyynti-välilehti.</span><span class="sxs-lookup"><span data-stu-id="8907e-127">Click the Retail tab.</span></span>
    * <span data-ttu-id="8907e-128">Työntekijä voidaan määrittää myynnin oletusryhmään.</span><span class="sxs-lookup"><span data-stu-id="8907e-128">A worker can be assigned to a default sales group.</span></span> <span data-ttu-id="8907e-129">Myynnin oletusryhmä automaattisesti lisätään automaattisesti myyntipisteen myyntiriveille, jos asetus on käytössä myymälän toimintoprofiilissa.</span><span class="sxs-lookup"><span data-stu-id="8907e-129">The default sales group will be automatically added to sales lines in POS if the option is enabled in the functionality profile for the store.</span></span>  
5. <span data-ttu-id="8907e-130">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="8907e-130">Click Edit.</span></span>
6. <span data-ttu-id="8907e-131">Syötä tai valitse arvo Oletusryhmä-kentässä.</span><span class="sxs-lookup"><span data-stu-id="8907e-131">In the Default group field, enter or select a value.</span></span>
7. <span data-ttu-id="8907e-132">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="8907e-132">Click Save.</span></span>

