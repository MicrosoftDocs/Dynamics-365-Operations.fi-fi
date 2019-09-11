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
ms.openlocfilehash: c89b17c09a4f145b5a4ca9cdd127b4e635447d4b
ms.sourcegitcommit: a368682f9cf3897347d155f1a2d4b33e555cc2c4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/08/2019
ms.locfileid: "1867316"
---
# <a name="configure-intercompany-project-invoicing"></a><span data-ttu-id="8d982-103">Konsernin sisäisen projektilaskutuksen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="8d982-103">Configure intercompany project invoicing</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8d982-104">Tässä ohjeessa kerrotaan, miten projektin laskutus määritetään kahden organisaation yrityksen välillä.</span><span class="sxs-lookup"><span data-stu-id="8d982-104">This topic shows how to set up project invoicing between two companies in your organization.</span></span> <span data-ttu-id="8d982-105">Tässä tehtävässä käytetään USSI-tietojoukkoa.</span><span class="sxs-lookup"><span data-stu-id="8d982-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="8d982-106">Siirry siirtymisruudussa kohtaan **Moduulit > Ostoreskontra > Toimittajat > Kaikki toimittajat**.</span><span class="sxs-lookup"><span data-stu-id="8d982-106">In the navigation pane, go to **Modules > Accounts payable > Vendors > All vendors**.</span></span>
2. <span data-ttu-id="8d982-107">Etsi haluamasi tietue **Kaikki toimittajat** -luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="8d982-107">In the **All vendors** list, find and select the desired record.</span></span>
3. <span data-ttu-id="8d982-108">Valitse toimintoruudussa **Yleiset**.</span><span class="sxs-lookup"><span data-stu-id="8d982-108">On the Action Pane, select **General**.</span></span>
4. <span data-ttu-id="8d982-109">Valitse **Konsernin sisäinen**.</span><span class="sxs-lookup"><span data-stu-id="8d982-109">Select **Intercompany**.</span></span>
5. <span data-ttu-id="8d982-110">Ota konsernin sisäinen kauppa käyttöön valitsemalla **Aktiivinen**-asetukseksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="8d982-110">Set **Active** to **Yes** to enable intercompany trading.</span></span>
6. <span data-ttu-id="8d982-111">Anna tai valitse arvo **Asiakasyritys**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="8d982-111">In the **Customer company** field, enter or select a value.</span></span>
7. <span data-ttu-id="8d982-112">Anna tai valitse arvo **Oma tili** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="8d982-112">In the **My account** field, enter or select a value.</span></span>
8. <span data-ttu-id="8d982-113">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="8d982-113">Select **Save**.</span></span>
9. <span data-ttu-id="8d982-114">Palaa kotisivulle sulkemalla sivut.</span><span class="sxs-lookup"><span data-stu-id="8d982-114">Close the pages to return to the home page.</span></span>
10. <span data-ttu-id="8d982-115">Valitse siirtymisruudussa **Moduulit > Projektinhallinta ja kirjanpito > Asetukset > Projektinhallinnan ja kirjanpidon parametrit**.</span><span class="sxs-lookup"><span data-stu-id="8d982-115">In the navigation pane, go to **Modules > Project management and accounting > Setup > Project management and accounting parameters**.</span></span>
11. <span data-ttu-id="8d982-116">Valitse **Konsernin sisäinen**-välilehti.</span><span class="sxs-lookup"><span data-stu-id="8d982-116">Select the **Intercompany** tab.</span></span>
12. <span data-ttu-id="8d982-117">Ota konsernin sisäinen resurssien ajoitus ja aikaraportit käyttöön siirtämällä liukusäädin **Kyllä**-kohtaan.</span><span class="sxs-lookup"><span data-stu-id="8d982-117">Move the slider to **Yes** to enable intercompany resource scheduling and timesheets.</span></span>
13. <span data-ttu-id="8d982-118">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="8d982-118">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="8d982-119">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="8d982-119">Select **New**.</span></span>
15. <span data-ttu-id="8d982-120">Anna tai valitse arvo **Lainaava yritys** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="8d982-120">In the **Borrowing legal entity** field, enter or select a value.</span></span>
16. <span data-ttu-id="8d982-121">Valitse **Jaksota tuotot** -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="8d982-121">Select the **Accrue revenue** check box.</span></span>
17. <span data-ttu-id="8d982-122">Anna tai valitse arvo **Oletusaikaraporttiluokka**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="8d982-122">In the **Default timesheet category** field, enter or select a value.</span></span>
18. <span data-ttu-id="8d982-123">Anna tai valitse arvo **Oletuskululuokka**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="8d982-123">In the **Default expense category** field, enter or select a value.</span></span>
19. <span data-ttu-id="8d982-124">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="8d982-124">Select **Save**.</span></span>
20. <span data-ttu-id="8d982-125">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="8d982-125">Close the page.</span></span>
21. <span data-ttu-id="8d982-126">Siirry siirtymisruudussa kohtaan **Moduulit > Projektinhallinta ja kirjanpito > Asetukset > Kirjaus > Kirjanpidon asetukset.**</span><span class="sxs-lookup"><span data-stu-id="8d982-126">In the navigation pane, go to **Modules > Project management and accounting > Setup > Posting > Ledger posting setup**.</span></span>
22. <span data-ttu-id="8d982-127">Valitse **Kirjanpitotilityypit**-kentässä vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="8d982-127">In the **Ledger account types** field, select an option.</span></span>
23. <span data-ttu-id="8d982-128">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="8d982-128">Select **New**.</span></span>
24. <span data-ttu-id="8d982-129">Määritä uuden rivin **Päätili**-kenttään haluamasi arvot.</span><span class="sxs-lookup"><span data-stu-id="8d982-129">In the **Main account** field of the new row, specify the desired values.</span></span>
25. <span data-ttu-id="8d982-130">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="8d982-130">Select **Save**.</span></span>
26. <span data-ttu-id="8d982-131">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="8d982-131">Close the page.</span></span>
27. <span data-ttu-id="8d982-132">Siirry siirtymisruudussa kohtaan **Moduulit > Projektinhallinta ja kirjanpito > Asetukset > Hinnat > Siirtohinta.**</span><span class="sxs-lookup"><span data-stu-id="8d982-132">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Transfer price**.</span></span>
28. <span data-ttu-id="8d982-133">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="8d982-133">Select **New**.</span></span>
29. <span data-ttu-id="8d982-134">Syötä päivämäärä **Voimaantulopäivä**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="8d982-134">In the **Effective date** field, enter a date.</span></span>
30. <span data-ttu-id="8d982-135">Anna tai valitse arvo **Lainaava yritys** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="8d982-135">In the **Borrowing legal entity** field, enter or select a value.</span></span>
31. <span data-ttu-id="8d982-136">Valitse **Siirtohintamalli**-kentässä vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="8d982-136">In the **Transfer price model** field, select an option.</span></span>
32. <span data-ttu-id="8d982-137">Anna **Hinnoittelu**-kentässä luku.</span><span class="sxs-lookup"><span data-stu-id="8d982-137">In the **Pricing** field, enter a number.</span></span>
33. <span data-ttu-id="8d982-138">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="8d982-138">Select **Save**.</span></span>

