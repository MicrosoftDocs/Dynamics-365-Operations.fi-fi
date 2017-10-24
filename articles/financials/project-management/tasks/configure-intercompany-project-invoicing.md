--- 
title: "Konsernin sisäisen projektilaskutuksen määrittäminen"
description: "Tämä menettely osoittaa, miten projektin laskutus määritetään kahden organisaation yrityksen välillä."
author: KimANelson
manager: AnnBe
ms.date: 02/13/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 4de7257ed5e9c9c08ec6cc423c29739a541926d5
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---
# <a name="configure-intercompany-project-invoicing"></a><span data-ttu-id="2c71b-103">Konsernin sisäisen projektilaskutuksen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="2c71b-103">Configure intercompany project invoicing</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2c71b-104">Tämä menettely osoittaa, miten projektin laskutus määritetään kahden organisaation yrityksen välillä.</span><span class="sxs-lookup"><span data-stu-id="2c71b-104">This procedure shows how to set up project invoicing between two companies in your organization.</span></span> <span data-ttu-id="2c71b-105">Tässä tehtävässä käytetään USSI-tietojoukkoa.</span><span class="sxs-lookup"><span data-stu-id="2c71b-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="2c71b-106">Siirry kohtaan Ostoreskontra > Toimittajat > Kaikki toimittajat.</span><span class="sxs-lookup"><span data-stu-id="2c71b-106">Go to Accounts payable > Vendors > All vendors.</span></span>
2. <span data-ttu-id="2c71b-107">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="2c71b-107">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="2c71b-108">Valitse toimintoruudussa Yleiset.</span><span class="sxs-lookup"><span data-stu-id="2c71b-108">On the Action Pane, click General.</span></span>
4. <span data-ttu-id="2c71b-109">Valitse Konsernin sisäinen.</span><span class="sxs-lookup"><span data-stu-id="2c71b-109">Click Intercompany.</span></span>
5. <span data-ttu-id="2c71b-110">Ota konsernin sisäinen kauppa käyttöön valitsemalla Aktiivinen-asetukseksi Kyllä.</span><span class="sxs-lookup"><span data-stu-id="2c71b-110">Set Active to Yes to enable intercompany trading.</span></span>
6. <span data-ttu-id="2c71b-111">Anna tai valitse arvo Asiakasyritys-kentässä.</span><span class="sxs-lookup"><span data-stu-id="2c71b-111">In the Customer company field, enter or select a value.</span></span>
7. <span data-ttu-id="2c71b-112">Anna tai valitse arvo Oma tili -kentässä.</span><span class="sxs-lookup"><span data-stu-id="2c71b-112">In the My account field, enter or select a value.</span></span>
8. <span data-ttu-id="2c71b-113">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="2c71b-113">Click Save.</span></span>
9. <span data-ttu-id="2c71b-114">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="2c71b-114">Close the page.</span></span>
10. <span data-ttu-id="2c71b-115">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="2c71b-115">Close the page.</span></span>
11. <span data-ttu-id="2c71b-116">Valitse Projektinhallinta ja kirjanpito > Asetukset > Projektinhallinnan ja kirjanpidon parametrit.</span><span class="sxs-lookup"><span data-stu-id="2c71b-116">Go to Project management and accounting > Setup > Project management and accounting parameters.</span></span>
12. <span data-ttu-id="2c71b-117">Valitse Konsernin sisäinen -välilehti.</span><span class="sxs-lookup"><span data-stu-id="2c71b-117">Click the Intercompany tab.</span></span>
13. <span data-ttu-id="2c71b-118">Ota konsernin sisäinen resurssien ajoitus ja aikaraportit käyttöön siirtämällä liukusäädin Kyllä-kohtaan.</span><span class="sxs-lookup"><span data-stu-id="2c71b-118">Move the slider to Yes to enable intercompany resource scheduling and timesheets.</span></span>
14. <span data-ttu-id="2c71b-119">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="2c71b-119">In the list, mark the selected row.</span></span>
15. <span data-ttu-id="2c71b-120">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="2c71b-120">Click New.</span></span>
16. <span data-ttu-id="2c71b-121">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="2c71b-121">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="2c71b-122">Anna tai valitse arvo Lainaava yritys -kentässä.</span><span class="sxs-lookup"><span data-stu-id="2c71b-122">In the Borrowing legal entity field, enter or select a value.</span></span>
18. <span data-ttu-id="2c71b-123">Valitse Jaksota tuotot -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="2c71b-123">Select the Accrue revenue check box.</span></span>
19. <span data-ttu-id="2c71b-124">Anna tai valitse arvo Oletusaikaraporttiluokka-kentässä.</span><span class="sxs-lookup"><span data-stu-id="2c71b-124">In the Default timesheet category field, enter or select a value.</span></span>
20. <span data-ttu-id="2c71b-125">Anna tai valitse arvo Oletuskululuokka-kentässä.</span><span class="sxs-lookup"><span data-stu-id="2c71b-125">In the Default expense category field, enter or select a value.</span></span>
21. <span data-ttu-id="2c71b-126">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="2c71b-126">Click Save.</span></span>
22. <span data-ttu-id="2c71b-127">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="2c71b-127">Close the page.</span></span>
23. <span data-ttu-id="2c71b-128">Valitse Projektinhallinta ja kirjanpito > Asetukset > Kirjaus > Kirjanpidon asetukset.</span><span class="sxs-lookup"><span data-stu-id="2c71b-128">Go to Project management and accounting > Setup > Posting > Ledger posting setup.</span></span>
24. <span data-ttu-id="2c71b-129">Valitse Kirjanpitotilityypit-kentässä vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="2c71b-129">In the Ledger account types field, select an option.</span></span>
25. <span data-ttu-id="2c71b-130">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="2c71b-130">Click New.</span></span>
26. <span data-ttu-id="2c71b-131">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="2c71b-131">In the list, mark the selected row.</span></span>
27. <span data-ttu-id="2c71b-132">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="2c71b-132">In the list, mark the selected row.</span></span>
28. <span data-ttu-id="2c71b-133">Määritä Päätili-kenttään haluamasi arvot.</span><span class="sxs-lookup"><span data-stu-id="2c71b-133">In the Main account field, specify the desired values.</span></span>
29. <span data-ttu-id="2c71b-134">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="2c71b-134">Click Save.</span></span>
30. <span data-ttu-id="2c71b-135">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="2c71b-135">Close the page.</span></span>
31. <span data-ttu-id="2c71b-136">Valitse Projektinhallinta ja kirjanpito > Asetukset > Hinnat > Siirtohinta.</span><span class="sxs-lookup"><span data-stu-id="2c71b-136">Go to Project management and accounting > Setup > Prices > Transfer price.</span></span>
32. <span data-ttu-id="2c71b-137">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="2c71b-137">Click New.</span></span>
33. <span data-ttu-id="2c71b-138">Syötä päivämäärä Voimaantulopäivä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="2c71b-138">In the Effective date field, enter a date.</span></span>
34. <span data-ttu-id="2c71b-139">Anna tai valitse arvo Lainaava yritys -kentässä.</span><span class="sxs-lookup"><span data-stu-id="2c71b-139">In the Borrowing legal entity field, enter or select a value.</span></span>
35. <span data-ttu-id="2c71b-140">Valitse Siirtohintamalli-kentässä vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="2c71b-140">In the Transfer price model field, select an option.</span></span>
36. <span data-ttu-id="2c71b-141">Anna Hinnoittelu-kentässä luku.</span><span class="sxs-lookup"><span data-stu-id="2c71b-141">In the Pricing field, enter a number.</span></span>
37. <span data-ttu-id="2c71b-142">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="2c71b-142">Click Save.</span></span>


