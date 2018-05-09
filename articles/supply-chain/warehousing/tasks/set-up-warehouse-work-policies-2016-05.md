--- 
title: "Määritä varaston työkäytännöt"
description: "Varastointiprosessit eivät aina sisällä varastotyötä."
author: johanhoffmann
manager: AnnBe
ms.date: 06/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: af2e01ccf570bbc647784351752ecb5c7c7d7595
ms.contentlocale: fi-fi
ms.lasthandoff: 05/08/2018

---
# <a name="set-up-warehouse-work-policies"></a><span data-ttu-id="25602-103">Määritä varaston työkäytännöt</span><span class="sxs-lookup"><span data-stu-id="25602-103">Set up warehouse work policies</span></span> 

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="25602-104">Varastointiprosessit eivät aina sisällä varastotyötä.</span><span class="sxs-lookup"><span data-stu-id="25602-104">Warehouse processes don’t always include warehouse work.</span></span> <span data-ttu-id="25602-105">Voit määrittää työn käytännön, joka estää raaka-aineen keräilytyön ja valmiiden tuotteiden poispanotöiden luonnin tietyille tuotejoukoille tietyissä sijainneissa.</span><span class="sxs-lookup"><span data-stu-id="25602-105">By defining a work policy, you can prevent the creation of work for raw material picking and put-away of finished goods for a set of products at specific locations.</span></span> <span data-ttu-id="25602-106">Tämän tallenteen luomisessa käytetty demotietojen yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="25602-106">The USMF demo data company was used to create this recording.</span></span> <span data-ttu-id="25602-107">Tämä tehtäväopas vaatii Dynamics AX -sovelluksen version 7.0.1 tai sitä uudemman.</span><span class="sxs-lookup"><span data-stu-id="25602-107">This task guide requires Dynamics AX application 7.0.1 or later.</span></span>

1. <span data-ttu-id="25602-108">Valitse Varastonhallinta > Asetukset > Työ > Työkäytännöt.</span><span class="sxs-lookup"><span data-stu-id="25602-108">Go to Warehouse management > Setup > Work > Work policies.</span></span>
2. <span data-ttu-id="25602-109">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="25602-109">Click New.</span></span>
3. <span data-ttu-id="25602-110">Kirjoita Työkäytännön nimi -kenttään Ei poispanotyötä.</span><span class="sxs-lookup"><span data-stu-id="25602-110">In the Work policy name field, type 'No put-away work'.</span></span>
4. <span data-ttu-id="25602-111">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="25602-111">Click Save.</span></span>
5. <span data-ttu-id="25602-112">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="25602-112">Click Add.</span></span>
6. <span data-ttu-id="25602-113">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="25602-113">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="25602-114">Valitse Työtilauksen tyyppi -kentässä Valmiiden tuotteiden poispano.</span><span class="sxs-lookup"><span data-stu-id="25602-114">In the Work order type field, select 'Finished goods put away'.</span></span>
8. <span data-ttu-id="25602-115">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="25602-115">Click Add.</span></span>
9. <span data-ttu-id="25602-116">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="25602-116">In the list, mark the selected row.</span></span>
10. <span data-ttu-id="25602-117">Valitse Työtilauksen tyyppi -kenttään Rinnakkaistuotteen ja sivutuotteen poispano.</span><span class="sxs-lookup"><span data-stu-id="25602-117">In the Work order type field, select 'Co-product and by-product put away'.</span></span>
11. <span data-ttu-id="25602-118">Laajenna Varastosijainnit-osa.</span><span class="sxs-lookup"><span data-stu-id="25602-118">Expand the Inventory locations section.</span></span>
12. <span data-ttu-id="25602-119">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="25602-119">Click Add.</span></span>
13. <span data-ttu-id="25602-120">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="25602-120">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="25602-121">Kirjoita varasto-luetteloon arvo 51.</span><span class="sxs-lookup"><span data-stu-id="25602-121">In the Warehouse list, enter '51'.</span></span>
15. <span data-ttu-id="25602-122">Syötä tai valitse Sijainti-kentän arvoksi 001.</span><span class="sxs-lookup"><span data-stu-id="25602-122">In the Location field, enter or select '001'.</span></span>
16. <span data-ttu-id="25602-123">Laajenna Tuotteet-osa.</span><span class="sxs-lookup"><span data-stu-id="25602-123">Expand the Products section.</span></span>
17. <span data-ttu-id="25602-124">Valitse Tuotteen valinta -kentän arvoksi Valittu.</span><span class="sxs-lookup"><span data-stu-id="25602-124">In the Product selection field, select 'Selected'.</span></span>
18. <span data-ttu-id="25602-125">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="25602-125">Click Add.</span></span>
19. <span data-ttu-id="25602-126">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="25602-126">In the list, mark the selected row.</span></span>
20. <span data-ttu-id="25602-127">Syötä tai valitse Nimiketunnus-kentän arvoksi L0101.</span><span class="sxs-lookup"><span data-stu-id="25602-127">In the Item number field, enter or select 'L0101'.</span></span>
21. <span data-ttu-id="25602-128">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="25602-128">Click Save.</span></span>


