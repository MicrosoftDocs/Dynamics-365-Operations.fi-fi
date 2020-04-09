---
title: Konsernin sisäisen projektilaskutuksen määrittäminen
description: Tässä ohjeessa kerrotaan, miten projektin laskutus määritetään kahden organisaation yrityksen välillä.
author: KimANelson
manager: AnnBe
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, InterCompanyTradingRelationSetupVendor, SysDataAreaSelectLookup, ProjParameters, ProjPosting, ProjTransferPrice
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 31dbae2d37aefe1841fe85cb6caf185c78596e55
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/18/2020
ms.locfileid: "3144276"
---
# <a name="configure-intercompany-project-invoicing"></a><span data-ttu-id="196b4-103">Konsernin sisäisen projektilaskutuksen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="196b4-103">Configure intercompany project invoicing</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="196b4-104">Tässä ohjeessa kerrotaan, miten projektin laskutus määritetään kahden organisaation yrityksen välillä.</span><span class="sxs-lookup"><span data-stu-id="196b4-104">This topic shows how to set up project invoicing between two companies in your organization.</span></span> <span data-ttu-id="196b4-105">Tässä tehtävässä käytetään USSI-tietojoukkoa.</span><span class="sxs-lookup"><span data-stu-id="196b4-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="196b4-106">Siirry siirtymisruudussa kohtaan **Moduulit > Ostoreskontra > Toimittajat > Kaikki toimittajat**.</span><span class="sxs-lookup"><span data-stu-id="196b4-106">In the navigation pane, go to **Modules > Accounts payable > Vendors > All vendors**.</span></span>
2. <span data-ttu-id="196b4-107">Etsi haluamasi tietue **Kaikki toimittajat** -luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="196b4-107">In the **All vendors** list, find and select the desired record.</span></span>
3. <span data-ttu-id="196b4-108">Valitse toimintoruudussa **Yleiset**.</span><span class="sxs-lookup"><span data-stu-id="196b4-108">On the Action Pane, select **General**.</span></span>
4. <span data-ttu-id="196b4-109">Valitse **Konsernin sisäinen**.</span><span class="sxs-lookup"><span data-stu-id="196b4-109">Select **Intercompany**.</span></span>
5. <span data-ttu-id="196b4-110">Ota konsernin sisäinen kauppa käyttöön valitsemalla **Aktiivinen**-asetukseksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="196b4-110">Set **Active** to **Yes** to enable intercompany trading.</span></span>
6. <span data-ttu-id="196b4-111">Anna tai valitse arvo **Asiakasyritys**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="196b4-111">In the **Customer company** field, enter or select a value.</span></span>
7. <span data-ttu-id="196b4-112">Anna tai valitse arvo **Oma tili** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="196b4-112">In the **My account** field, enter or select a value.</span></span>
8. <span data-ttu-id="196b4-113">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="196b4-113">Select **Save**.</span></span>
9. <span data-ttu-id="196b4-114">Palaa kotisivulle sulkemalla sivut.</span><span class="sxs-lookup"><span data-stu-id="196b4-114">Close the pages to return to the home page.</span></span>
10. <span data-ttu-id="196b4-115">Valitse siirtymisruudussa **Moduulit > Projektinhallinta ja kirjanpito > Asetukset > Projektinhallinnan ja kirjanpidon parametrit**.</span><span class="sxs-lookup"><span data-stu-id="196b4-115">In the navigation pane, go to **Modules > Project management and accounting > Setup > Project management and accounting parameters**.</span></span>
11. <span data-ttu-id="196b4-116">Valitse **Konsernin sisäinen**-välilehti.</span><span class="sxs-lookup"><span data-stu-id="196b4-116">Select the **Intercompany** tab.</span></span>
12. <span data-ttu-id="196b4-117">Ota konsernin sisäinen resurssien ajoitus ja aikaraportit käyttöön siirtämällä liukusäädin **Kyllä**-kohtaan.</span><span class="sxs-lookup"><span data-stu-id="196b4-117">Move the slider to **Yes** to enable intercompany resource scheduling and timesheets.</span></span>
13. <span data-ttu-id="196b4-118">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="196b4-118">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="196b4-119">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="196b4-119">Select **New**.</span></span>
15. <span data-ttu-id="196b4-120">Anna tai valitse arvo **Lainaava yritys** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="196b4-120">In the **Borrowing legal entity** field, enter or select a value.</span></span>
16. <span data-ttu-id="196b4-121">Valitse **Jaksota tuotot** -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="196b4-121">Select the **Accrue revenue** check box.</span></span>
17. <span data-ttu-id="196b4-122">Anna tai valitse arvo **Oletusaikaraporttiluokka**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="196b4-122">In the **Default timesheet category** field, enter or select a value.</span></span>
18. <span data-ttu-id="196b4-123">Anna tai valitse arvo **Oletuskululuokka**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="196b4-123">In the **Default expense category** field, enter or select a value.</span></span>
19. <span data-ttu-id="196b4-124">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="196b4-124">Select **Save**.</span></span>
20. <span data-ttu-id="196b4-125">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="196b4-125">Close the page.</span></span>
21. <span data-ttu-id="196b4-126">Siirry siirtymisruudussa kohtaan **Moduulit > Projektinhallinta ja kirjanpito > Asetukset > Kirjaus > Kirjanpidon asetukset.**</span><span class="sxs-lookup"><span data-stu-id="196b4-126">In the navigation pane, go to **Modules > Project management and accounting > Setup > Posting > Ledger posting setup**.</span></span>
22. <span data-ttu-id="196b4-127">Valitse **Kirjanpitotilityypit**-kentässä vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="196b4-127">In the **Ledger account types** field, select an option.</span></span>
23. <span data-ttu-id="196b4-128">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="196b4-128">Select **New**.</span></span>
24. <span data-ttu-id="196b4-129">Määritä uuden rivin **Päätili**-kenttään haluamasi arvot.</span><span class="sxs-lookup"><span data-stu-id="196b4-129">In the **Main account** field of the new row, specify the desired values.</span></span>
25. <span data-ttu-id="196b4-130">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="196b4-130">Select **Save**.</span></span>
26. <span data-ttu-id="196b4-131">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="196b4-131">Close the page.</span></span>
27. <span data-ttu-id="196b4-132">Siirry siirtymisruudussa kohtaan **Moduulit > Projektinhallinta ja kirjanpito > Asetukset > Hinnat > Siirtohinta.**</span><span class="sxs-lookup"><span data-stu-id="196b4-132">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Transfer price**.</span></span>
28. <span data-ttu-id="196b4-133">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="196b4-133">Select **New**.</span></span>
29. <span data-ttu-id="196b4-134">Syötä päivämäärä **Voimaantulopäivä**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="196b4-134">In the **Effective date** field, enter a date.</span></span>
30. <span data-ttu-id="196b4-135">Anna tai valitse arvo **Lainaava yritys** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="196b4-135">In the **Borrowing legal entity** field, enter or select a value.</span></span>
31. <span data-ttu-id="196b4-136">Valitse **Siirtohintamalli**-kentässä vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="196b4-136">In the **Transfer price model** field, select an option.</span></span>
32. <span data-ttu-id="196b4-137">Anna **Hinnoittelu**-kentässä luku.</span><span class="sxs-lookup"><span data-stu-id="196b4-137">In the **Pricing** field, enter a number.</span></span>
33. <span data-ttu-id="196b4-138">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="196b4-138">Select **Save**.</span></span>

