--- 
title: Alusta varaston varastotasoja
description: "Tässä menettelyssä selitetään, miten käytettävissä oleva varasto päivitetään manuaalisesti varastosiirron kirjauskansion avulla."
author: perlynne
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventJournalMovement, InventJournalCreate, InventItemIdLookupSimple, InventLocationIdLookup, WMSLocationIdLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 4bfa40c19e34631edb68b8cff42e7f72eb9ce2ad
ms.contentlocale: fi-fi
ms.lasthandoff: 09/14/2018

---
# <a name="initialize-stock-levels-in-the-warehouse"></a><span data-ttu-id="5997a-103">Alusta varaston varastotasoja</span><span class="sxs-lookup"><span data-stu-id="5997a-103">Initialize stock levels in the warehouse</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5997a-104">Tässä menettelyssä selitetään, miten käytettävissä oleva varasto päivitetään manuaalisesti varastosiirron kirjauskansion avulla.</span><span class="sxs-lookup"><span data-stu-id="5997a-104">This procedure shows you how to get the on-hand inventory updated manually using an Inventory movement journal.</span></span> <span data-ttu-id="5997a-105">(Käytettävissä oleva varasto voidaan päivittää myös tuomatta tietoyksiköiden tapahtumat.) Voit suorittaa tämän opastuksen USMF-yrityksen demotiedoissa, jolloin kaikki edellytykset, kuten kirjauskansion nimi, nimikeasetukset, kirjausprofiilit ja tilit ovat käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="5997a-105">(It’s also possible to update on-hand inventory by importing transactions in data entities.) You can run this guide in demo data company USMF where all the prerequisites like journal name, item setup, posting profiles, and accounts are available.</span></span> <span data-ttu-id="5997a-106">Opastuksessa ehdotetaan käytettäville nimikkeelle ja dimensioille tiettyjä arvoja.</span><span class="sxs-lookup"><span data-stu-id="5997a-106">The guide suggests specific values for the item and dimensions that are used.</span></span> <span data-ttu-id="5997a-107">Jos valitset toisen nimikkeen, eri dimensioiden arvot on ehkä annettava.</span><span class="sxs-lookup"><span data-stu-id="5997a-107">If you choose a different item, you may need to enter values for different dimensions.</span></span>

1. <span data-ttu-id="5997a-108">Valitse Inventoinnin- ja varastonhallinta > Kirjauskansioviennit > Nimikkeet > Siirto.</span><span class="sxs-lookup"><span data-stu-id="5997a-108">Go to Inventory management > Journal entries > Items > Movement.</span></span>
2. <span data-ttu-id="5997a-109">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="5997a-109">Click New.</span></span>
3. <span data-ttu-id="5997a-110">Avaa haku valitsemalla Nimi-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="5997a-110">In the Name field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="5997a-111">Valitse IMov.</span><span class="sxs-lookup"><span data-stu-id="5997a-111">Select IMov.</span></span>
    * <span data-ttu-id="5997a-112">On hyvän käytännön mukaista käyttää erilaisia kirjauskansion nimimalleja eri liiketoimintatarkoituksiin.</span><span class="sxs-lookup"><span data-stu-id="5997a-112">It’s a good practise to use different journal name templates for the different business purposes.</span></span>  
5. <span data-ttu-id="5997a-113">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="5997a-113">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="5997a-114">Määritä Vastatili-kenttään arvo 140200.</span><span class="sxs-lookup"><span data-stu-id="5997a-114">In the Offset account field, specify the values '140200'.</span></span>
    * <span data-ttu-id="5997a-115">Tämä vastatili on kirjauskansiorivien oletustili.</span><span class="sxs-lookup"><span data-stu-id="5997a-115">This is the offset account that will be the default account on the journal lines.</span></span> <span data-ttu-id="5997a-116">Oletuksen voi korvat määrittämällä rivikohtaisesti eri vastatilit.</span><span class="sxs-lookup"><span data-stu-id="5997a-116">It’s possible to override the default to assign different offset accounts per line.</span></span>  
7. <span data-ttu-id="5997a-117">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="5997a-117">Click OK.</span></span>
8. <span data-ttu-id="5997a-118">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="5997a-118">Click New.</span></span>
9. <span data-ttu-id="5997a-119">Avaa haku valitsemalla Nimiketunnus-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="5997a-119">In the Item number field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="5997a-120">Valitse nimike A0001.</span><span class="sxs-lookup"><span data-stu-id="5997a-120">Select item A0001.</span></span>
11. <span data-ttu-id="5997a-121">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="5997a-121">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="5997a-122">Valitse Varastodimensiot-välilehti.</span><span class="sxs-lookup"><span data-stu-id="5997a-122">Click the Inventory dimensions tab.</span></span>
13. <span data-ttu-id="5997a-123">Avaa haku napsauttamalla Toimipaikka-kentässä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="5997a-123">In the Site field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="5997a-124">Valitse toimipaikka 1.</span><span class="sxs-lookup"><span data-stu-id="5997a-124">Select site 1.</span></span>
15. <span data-ttu-id="5997a-125">Avaa haku valitsemalla Varasto-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="5997a-125">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
16. <span data-ttu-id="5997a-126">Valitse varasto 13.</span><span class="sxs-lookup"><span data-stu-id="5997a-126">Select warehouse 13.</span></span>
17. <span data-ttu-id="5997a-127">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="5997a-127">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="5997a-128">Avaa haku valitsemalla Sijainnit-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="5997a-128">In the Location field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="5997a-129">Valitse sijainti 13.</span><span class="sxs-lookup"><span data-stu-id="5997a-129">Select location 13.</span></span>
20. <span data-ttu-id="5997a-130">Kirjoita numero Määrä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="5997a-130">In the Quantity field, enter a number.</span></span>
21. <span data-ttu-id="5997a-131">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="5997a-131">Click Save.</span></span>
22. <span data-ttu-id="5997a-132">Valitse Kirjaa.</span><span class="sxs-lookup"><span data-stu-id="5997a-132">Click Post.</span></span>
23. <span data-ttu-id="5997a-133">Valitse Siirrä kaikki kirjausvirheet uuteen kirjauskansioon -valintaruutu tai poista sen valinta.</span><span class="sxs-lookup"><span data-stu-id="5997a-133">Check or uncheck the Transfer all posting errors to a new journal check box.</span></span>
    * <span data-ttu-id="5997a-134">Jos tämä vaihtoehto otetaan käyttöön, kaikki rivit, joiden kirjaus epäonnistui, kopioidaan uuteen kirjauskansioon.</span><span class="sxs-lookup"><span data-stu-id="5997a-134">If you enable this option, any lines that fail to post will be copied to a new journal.</span></span> <span data-ttu-id="5997a-135">Voit korjata ongelmat tämän lokin tietojen perusteella ja kirjata rivit uudelleen.</span><span class="sxs-lookup"><span data-stu-id="5997a-135">You can use the information in the log to correct the issues and then re-post the lines.</span></span>  
24. <span data-ttu-id="5997a-136">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="5997a-136">Click OK.</span></span>
25. <span data-ttu-id="5997a-137">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="5997a-137">Close the page.</span></span>
26. <span data-ttu-id="5997a-138">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="5997a-138">Close the page.</span></span>


