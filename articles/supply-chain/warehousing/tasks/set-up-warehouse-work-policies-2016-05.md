---
title: Määritä varastotyön käytännöt (Sovellus, Toukokuu 2016)
description: Varastointiprosessit eivät aina sisällä varastotyötä.
author: johanhoffmann
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkPolicy, WMSLocationIdLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 34b4255c85bb53f7e238b60559890571070953a6
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/15/2019
ms.locfileid: "1569076"
---
# <a name="set-up-warehouse-work-policies-application-may-2016"></a><span data-ttu-id="18951-103">Määritä varastotyön käytännöt (Sovellus, Toukokuu 2016)</span><span class="sxs-lookup"><span data-stu-id="18951-103">Set up warehouse work policies (Application, May 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="18951-104">Varastointiprosessit eivät aina sisällä varastotyötä.</span><span class="sxs-lookup"><span data-stu-id="18951-104">Warehouse processes don’t always include warehouse work.</span></span> <span data-ttu-id="18951-105">Voit määrittää työn käytännön, joka estää raaka-aineen keräilytyön ja valmiiden tuotteiden poispanotöiden luonnin tietyille tuotejoukoille tietyissä sijainneissa.</span><span class="sxs-lookup"><span data-stu-id="18951-105">By defining a work policy, you can prevent the creation of work for raw material picking and put-away of finished goods for a set of products at specific locations.</span></span> <span data-ttu-id="18951-106">Tämän tallenteen luomisessa käytetty demotietojen yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="18951-106">The USMF demo data company was used to create this recording.</span></span> <span data-ttu-id="18951-107">Tämä tehtäväopas vaatii Dynamics AX -sovelluksen version 7.0.1 tai sitä uudemman.</span><span class="sxs-lookup"><span data-stu-id="18951-107">This task guide requires Dynamics AX application 7.0.1 or later.</span></span>

1. <span data-ttu-id="18951-108">Valitse Varastonhallinta > Asetukset > Työ > Työkäytännöt.</span><span class="sxs-lookup"><span data-stu-id="18951-108">Go to Warehouse management > Setup > Work > Work policies.</span></span>
2. <span data-ttu-id="18951-109">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="18951-109">Click New.</span></span>
3. <span data-ttu-id="18951-110">Kirjoita Työkäytännön nimi -kenttään Ei poispanotyötä.</span><span class="sxs-lookup"><span data-stu-id="18951-110">In the Work policy name field, type 'No put-away work'.</span></span>
4. <span data-ttu-id="18951-111">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="18951-111">Click Save.</span></span>
5. <span data-ttu-id="18951-112">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="18951-112">Click Add.</span></span>
6. <span data-ttu-id="18951-113">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="18951-113">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="18951-114">Valitse Työtilauksen tyyppi -kentässä Valmiiden tuotteiden poispano.</span><span class="sxs-lookup"><span data-stu-id="18951-114">In the Work order type field, select 'Finished goods put away'.</span></span>
8. <span data-ttu-id="18951-115">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="18951-115">Click Add.</span></span>
9. <span data-ttu-id="18951-116">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="18951-116">In the list, mark the selected row.</span></span>
10. <span data-ttu-id="18951-117">Valitse Työtilauksen tyyppi -kenttään Rinnakkaistuotteen ja sivutuotteen poispano.</span><span class="sxs-lookup"><span data-stu-id="18951-117">In the Work order type field, select 'Co-product and by-product put away'.</span></span>
11. <span data-ttu-id="18951-118">Laajenna Varastosijainnit-osa.</span><span class="sxs-lookup"><span data-stu-id="18951-118">Expand the Inventory locations section.</span></span>
12. <span data-ttu-id="18951-119">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="18951-119">Click Add.</span></span>
13. <span data-ttu-id="18951-120">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="18951-120">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="18951-121">Kirjoita varasto-luetteloon arvo 51.</span><span class="sxs-lookup"><span data-stu-id="18951-121">In the Warehouse list, enter '51'.</span></span>
15. <span data-ttu-id="18951-122">Syötä tai valitse Sijainti-kentän arvoksi 001.</span><span class="sxs-lookup"><span data-stu-id="18951-122">In the Location field, enter or select '001'.</span></span>
16. <span data-ttu-id="18951-123">Laajenna Tuotteet-osa.</span><span class="sxs-lookup"><span data-stu-id="18951-123">Expand the Products section.</span></span>
17. <span data-ttu-id="18951-124">Valitse Tuotteen valinta -kentän arvoksi Valittu.</span><span class="sxs-lookup"><span data-stu-id="18951-124">In the Product selection field, select 'Selected'.</span></span>
18. <span data-ttu-id="18951-125">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="18951-125">Click Add.</span></span>
19. <span data-ttu-id="18951-126">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="18951-126">In the list, mark the selected row.</span></span>
20. <span data-ttu-id="18951-127">Syötä tai valitse Nimiketunnus-kentän arvoksi L0101.</span><span class="sxs-lookup"><span data-stu-id="18951-127">In the Item number field, enter or select 'L0101'.</span></span>
21. <span data-ttu-id="18951-128">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="18951-128">Click Save.</span></span>

