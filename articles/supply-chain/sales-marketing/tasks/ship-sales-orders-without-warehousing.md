--- 
title: "Lähetä myyntitilaukset ilman varastointia"
description: "Tässä opastuksessa käsitellään, miten myyntitilaus päivitetään, kun tuotteet on lähetetty asiakkaalle."
author: omulvad
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SalesTableListPage, SalesTable, SalesEditLines,  SrsReportViewerForm, SalesTableLineQuantity, CustPackingSlipJournal
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: ae70e09dbc4da90b7d1802d076384eae2d00da0e
ms.contentlocale: fi-fi
ms.lasthandoff: 09/14/2018

---
# <a name="ship-sales-orders-without-warehousing"></a><span data-ttu-id="958ef-103">Lähetä myyntitilaukset ilman varastointia</span><span class="sxs-lookup"><span data-stu-id="958ef-103">Ship sales orders without warehousing</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="958ef-104">Tässä opastuksessa käsitellään, miten myyntitilaus päivitetään, kun tuotteet on lähetetty asiakkaalle.</span><span class="sxs-lookup"><span data-stu-id="958ef-104">This guide demonstrates how to update a sales order when products are shipped to the customer.</span></span> <span data-ttu-id="958ef-105">Opastus koskee toteutustyönkulkua, jota ei ole määritetty varastonhallintaa varten (ei perus- eikä lisätason varastointiin), joten se ei edellytä tuotteen keräilyn rekisteröintiä ennen lähetystä.</span><span class="sxs-lookup"><span data-stu-id="958ef-105">The guide is applicable to the fulfillment flow that is not set up for warehouse management (neither basic or advanced warehousing), and therefore does not require product picking to be registered before shipment.</span></span> <span data-ttu-id="958ef-106">Voit suorittaa tämän menettelyn USMF-demoyrityksen tiedoilla tai käyttää omia tietoja.</span><span class="sxs-lookup"><span data-stu-id="958ef-106">You can run this procedure on your own data or in demo data company USMF.</span></span> <span data-ttu-id="958ef-107">Molemmissa tapauksissa ennen tehtävän aloittamista varastoidulle tuotteelle on luotava myyntitilaus, jonka määrä on suurempi kuin 1.</span><span class="sxs-lookup"><span data-stu-id="958ef-107">In both cases, before you start this task, create a sales order for an inventoried product with a quantity of greater than 1.</span></span> <span data-ttu-id="958ef-108">Kirjausvirheen välttämiseksi sinun on tarkistettava, että tuotteen varastossa oleva määrä tilaukseen valitussa toimipaikassa ja varastossa riittää kattamaan tilausmäärän.</span><span class="sxs-lookup"><span data-stu-id="958ef-108">To avoid a posting error, you need to check that the product's on-hand quantity in the site and warehouse that you’ve selected on the order covers the order quantity.</span></span>


## <a name="post-packing-slip-for-an-order"></a><span data-ttu-id="958ef-109">Kirjaa tilauksen pakkausluettelo</span><span class="sxs-lookup"><span data-stu-id="958ef-109">Post packing slip for an order</span></span>
1. <span data-ttu-id="958ef-110">Siirry kohtaan Myynti ja markkinointi > Myyntitilaukset > Kaikki myyntitilaukset.</span><span class="sxs-lookup"><span data-stu-id="958ef-110">Go to Sales and marketing > Sales orders > All sales orders.</span></span>
2. <span data-ttu-id="958ef-111">Etsi ja valitse luettelossa tehtävää varten luotu tilaus.</span><span class="sxs-lookup"><span data-stu-id="958ef-111">In the list, find and select the order you have created for this task.</span></span>
3. <span data-ttu-id="958ef-112">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="958ef-112">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="958ef-113">Valitse toimintoruudussa Kerää ja pakkaa.</span><span class="sxs-lookup"><span data-stu-id="958ef-113">On the Action Pane, click Pick and pack.</span></span>
5. <span data-ttu-id="958ef-114">Valitse Kirjaa pakkausluettelo.</span><span class="sxs-lookup"><span data-stu-id="958ef-114">Click Post packing slip.</span></span>
6. <span data-ttu-id="958ef-115">Laajenna tai tiivistä Parametrit-osa.</span><span class="sxs-lookup"><span data-stu-id="958ef-115">Expand or collapse the Parameters section.</span></span>
7. <span data-ttu-id="958ef-116">Valitse Määrä-kentässä Kaikki.</span><span class="sxs-lookup"><span data-stu-id="958ef-116">In the Quantity field, select 'All'.</span></span>
    * <span data-ttu-id="958ef-117">Vaihtoehtoja ovat lisäksi Toimita nyt ja Keräilty.</span><span class="sxs-lookup"><span data-stu-id="958ef-117">Other options include Deliver now and Picked.</span></span> <span data-ttu-id="958ef-118">Jos tilausrivi toimitetaan osittain ja tilausrivin Toimita nyt -kentässä on määrä, valitaan Toimita nyt.</span><span class="sxs-lookup"><span data-stu-id="958ef-118">If the order line is to be shipped partially and the Deliver now field on the order line contains a quantity, you would select Deliver now.</span></span> <span data-ttu-id="958ef-119">Jos organisaation toteuttamistyönkulku sisältää keräilyn erillisenä, keräysluettelon hallitsemana ja rekisteröimänä prosessina, valitaan Keräilty.</span><span class="sxs-lookup"><span data-stu-id="958ef-119">If your organization's fulfillment flow includes picking as a separate process that is managed by and registered with a picking list, you would select Picked.</span></span>  
    * <span data-ttu-id="958ef-120">Tarkista, että Kirjaus-asetukseksi on valittu Kyllä.</span><span class="sxs-lookup"><span data-stu-id="958ef-120">Check that the Posting option is set to Yes.</span></span>  
8. <span data-ttu-id="958ef-121">Valitse Tulosta pakkausluettelo -asetukseksi Kyllä.</span><span class="sxs-lookup"><span data-stu-id="958ef-121">Set the Print packing slip option to Yes.</span></span>
    * <span data-ttu-id="958ef-122">Tälle kirjaukselle luotavat pakkausluettelot ovat Yhteenveto-välilehdessä.</span><span class="sxs-lookup"><span data-stu-id="958ef-122">The Overview tab contains a list of packing slips to be generated in this posting.</span></span> <span data-ttu-id="958ef-123">Jos toimitat yksittäisen tilauksen, pakkausluetteloita on yleensä yksi.</span><span class="sxs-lookup"><span data-stu-id="958ef-123">If you are shipping an individual order, there will typically be one packing slip.</span></span> <span data-ttu-id="958ef-124">Jos kyseiseen tilauksen rivit kuitenkin toimitetaan eri toimipaikoista, kirjaus jaetaan automaattisesti niin, että asiakirjoja on tarvittava määrä.</span><span class="sxs-lookup"><span data-stu-id="958ef-124">However, if that order's lines are to be shipped from different sites, posting will automatically be split into the appropriate number of documents.</span></span> <span data-ttu-id="958ef-125">Tämä on pakollinen ehto, jota ei voi muuttaa.</span><span class="sxs-lookup"><span data-stu-id="958ef-125">This is a mandatory condition that cannot be changed.</span></span> <span data-ttu-id="958ef-126">Kirjaus jaetaan vastaavasti useisiin asiakirjoihin myös silloin, jos tilauksen rivit lähetetään eri toimitusosoitteisiin ja lähetyskäytäntö määrittää jaon pakolliseksi.</span><span class="sxs-lookup"><span data-stu-id="958ef-126">Similarly, the posting will also be split into multiple documents if the order’s lines are to be shipped to different delivery addresses, and the shipping policy is set up to require a split.</span></span>  
9. <span data-ttu-id="958ef-127">Valitse Rivit-välilehdessä lähetettävän tilausrivin rivi.</span><span class="sxs-lookup"><span data-stu-id="958ef-127">On the Lines tab, select the row for the order line to be shipped.</span></span>
10. <span data-ttu-id="958ef-128">Lisää Päivitä-kenttään luku, joka on pienempi kuin alkuperäinen määrä.</span><span class="sxs-lookup"><span data-stu-id="958ef-128">In the Update field, enter a number lower than the original quantity.</span></span>
11. <span data-ttu-id="958ef-129">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="958ef-129">Click OK.</span></span>
12. <span data-ttu-id="958ef-130">Valitse Kyllä.</span><span class="sxs-lookup"><span data-stu-id="958ef-130">Click Yes.</span></span>
13. <span data-ttu-id="958ef-131">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="958ef-131">Close the page.</span></span>
14. <span data-ttu-id="958ef-132">Valitse toimintoruudussa Asetukset.</span><span class="sxs-lookup"><span data-stu-id="958ef-132">On the Action Pane, click Options.</span></span>
15. <span data-ttu-id="958ef-133">Valitse Vaihda näkymä.</span><span class="sxs-lookup"><span data-stu-id="958ef-133">Click Change view.</span></span>
16. <span data-ttu-id="958ef-134">Valitse Otsikkonäkymä.</span><span class="sxs-lookup"><span data-stu-id="958ef-134">Click Header view.</span></span>
    * <span data-ttu-id="958ef-135">Jos kaikki tilauksen rivit on lähetetty kokonaisuudessa, tilauksen tila muuttuu avoimesta toimitetuksi.</span><span class="sxs-lookup"><span data-stu-id="958ef-135">If all of the lines on the order have been fully shipped, the order status changes from Open to Delivered.</span></span>  
    * <span data-ttu-id="958ef-136">Tässä esimerkissä tilausrivi on toimitettu osittain.</span><span class="sxs-lookup"><span data-stu-id="958ef-136">In this example, the order line has been shipped partially.</span></span> <span data-ttu-id="958ef-137">Tämän vuoksi vielä tilaus on edelleen avoinna.</span><span class="sxs-lookup"><span data-stu-id="958ef-137">This is why the the order status remains Open.</span></span>     
    * <span data-ttu-id="958ef-138">Asiakirjan tila -kentän asetuksena on Pakkausluettelo, koska vähintään yksi tilausriveistä on lähetetty.</span><span class="sxs-lookup"><span data-stu-id="958ef-138">The Document status field is set to Packing slip because at least one of the order lines have been shipped.</span></span>  
17. <span data-ttu-id="958ef-139">Valitse toimintoruudussa Yleiset.</span><span class="sxs-lookup"><span data-stu-id="958ef-139">On the Action Pane, click General.</span></span>
18. <span data-ttu-id="958ef-140">Valitse Rivin määrä.</span><span class="sxs-lookup"><span data-stu-id="958ef-140">Click Line quantity.</span></span>
19. <span data-ttu-id="958ef-141">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="958ef-141">Close the page.</span></span>
20. <span data-ttu-id="958ef-142">Valitse toimintoruudussa Kerää ja pakkaa.</span><span class="sxs-lookup"><span data-stu-id="958ef-142">On the Action Pane, click Pick and pack.</span></span>
21. <span data-ttu-id="958ef-143">Valitse Pakkausluettelo.</span><span class="sxs-lookup"><span data-stu-id="958ef-143">Click Packing slip.</span></span>
    * <span data-ttu-id="958ef-144">Kaikki tilausta varten luodut pakkausluetteloasiakirjat ovat Pakkausluettelo-kirjauskansio-sivulla.</span><span class="sxs-lookup"><span data-stu-id="958ef-144">The Packing slip journal page contains all the packing slip documents that were generated for your order.</span></span> <span data-ttu-id="958ef-145">Voit tarvittaessa tarkastella kunkin asiakirjan tietoja ja tulostaa ne.</span><span class="sxs-lookup"><span data-stu-id="958ef-145">You can review details of each document and print them, if you wish.</span></span>  


