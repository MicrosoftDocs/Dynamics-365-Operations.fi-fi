---
title: Luo päätili
description: Tässä tehtäväopastuksessa käsitellään päätilin lisäämistä aiemmin luotuun tilikarttaan.
author: aprilolson
manager: AnnBe
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MainAccount, CompanyInfoList
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a116164a31337013d34f963b549c394aade2de1c
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/18/2020
ms.locfileid: "3139989"
---
# <a name="create-a-main-account"></a><span data-ttu-id="acf61-103">Luo päätili</span><span class="sxs-lookup"><span data-stu-id="acf61-103">Create a main account</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="acf61-104">Tässä tehtäväopastuksessa käsitellään päätilin lisäämistä aiemmin luotuun tilikarttaan.</span><span class="sxs-lookup"><span data-stu-id="acf61-104">This task guide steps through adding a main account to an existing chart of accounts.</span></span> <span data-ttu-id="acf61-105">Tässä tallenteessa käytetään esittely-yritystä USMF.</span><span class="sxs-lookup"><span data-stu-id="acf61-105">This recording uses the USMF demo company.</span></span>  

1. <span data-ttu-id="acf61-106">Valitse **Siirtymisruutu > Moduulit > Kirjanpito > Tilikartta > Tilit > Päätilit**.</span><span class="sxs-lookup"><span data-stu-id="acf61-106">Go to **Navigation pane > Modules > General ledger > Chart of accounts > Accounts > Main accounts**.</span></span>
2. <span data-ttu-id="acf61-107">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="acf61-107">Click **New**.</span></span>
3. <span data-ttu-id="acf61-108">Kirjoita **Päätili**-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="acf61-108">In the **Main account** field, type a value.</span></span>
4. <span data-ttu-id="acf61-109">Kirjoita arvo **Nimi**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="acf61-109">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="acf61-110">Valitse **Päätilin tyyppi** -kentässä tyyppi, joka vastaa parhaiten tilien saldoa ja sijaintia raporteissa.</span><span class="sxs-lookup"><span data-stu-id="acf61-110">In the **Main account type** field, select the type that best represents the accounts balance and location on financial statements.</span></span>
6. <span data-ttu-id="acf61-111">Valitse luettelossa tililuokka, johon päätili kuuluu.</span><span class="sxs-lookup"><span data-stu-id="acf61-111">In the list, select the account category the main account belongs to.</span></span> <span data-ttu-id="acf61-112">Tililuokkaa käytetään oletusraporteissa ja Power BI -koontinäytön sisällössä.</span><span class="sxs-lookup"><span data-stu-id="acf61-112">Account category is used for default financial reports and Power BI dashboard content.</span></span>  
7. <span data-ttu-id="acf61-113">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="acf61-113">In the list, click the link in the selected row.</span></span> <span data-ttu-id="acf61-114">Muuta oletussaatavien tai -maksettavien saldo.</span><span class="sxs-lookup"><span data-stu-id="acf61-114">Change the default debit or credit balance.</span></span>  
8. <span data-ttu-id="acf61-115">Valitse **Oletusvaluutta**-kentässä arvo valuuttaluettelosta.</span><span class="sxs-lookup"><span data-stu-id="acf61-115">In the **Default currency** field, select a value from the list of currencies.</span></span>
9. <span data-ttu-id="acf61-116">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="acf61-116">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="acf61-117">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="acf61-117">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="acf61-118">Ota käyttöön **Yrityksen ohitukset** -osan laajennus.</span><span class="sxs-lookup"><span data-stu-id="acf61-118">Toggle the expansion of the **Legal entity overrides** section.</span></span>
12. <span data-ttu-id="acf61-119">Valitse yritys valitsemalla **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="acf61-119">Click **Add** to select a legal entity.</span></span>
13. <span data-ttu-id="acf61-120">Valitse luettelossa Yritys.</span><span class="sxs-lookup"><span data-stu-id="acf61-120">In the list, select the Legal entity.</span></span>
14. <span data-ttu-id="acf61-121">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="acf61-121">Click **Add**.</span></span>
15. <span data-ttu-id="acf61-122">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="acf61-122">In the list, mark the selected row.</span></span>
16. <span data-ttu-id="acf61-123">Valitse **Keskeytetty**-valintaruutu tai poista sen valinta.</span><span class="sxs-lookup"><span data-stu-id="acf61-123">Check or uncheck the **Suspended** checkbox.</span></span>
17. <span data-ttu-id="acf61-124">Laajenna **Taloushallinnon raportointi** -osa.</span><span class="sxs-lookup"><span data-stu-id="acf61-124">Expand the **Financial reporting** section.</span></span>
18. <span data-ttu-id="acf61-125">Avaa haku valitsemalla **Vaihtokurssin tyyppi** -kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="acf61-125">In the **Exchange rate type** field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="acf61-126">Valitse luettelossa tilin **Vaihtokurssin tyyppi**.</span><span class="sxs-lookup"><span data-stu-id="acf61-126">In the list, select the **Exchange rate type for the account**.</span></span>
20. <span data-ttu-id="acf61-127">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="acf61-127">In the list, click the link in the selected row.</span></span>
21. <span data-ttu-id="acf61-128">Valitse **Valuutan muuntotyyppi** -kentässä menetelmä, jolla tilin vaihtokurssit lasketaan.</span><span class="sxs-lookup"><span data-stu-id="acf61-128">In the **Currency translation type** field, select the method for calculating exchange rates for the account.</span></span>
22. <span data-ttu-id="acf61-129">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="acf61-129">Close the page.</span></span>

