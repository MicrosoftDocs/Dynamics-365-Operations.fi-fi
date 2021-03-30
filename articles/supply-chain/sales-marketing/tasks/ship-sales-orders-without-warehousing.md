---
title: Myyntitilausten lähettäminen ilman varastointia
description: Tässä aiheessa kerrotaan, miten myyntitilaus päivitetään, kun tuotteet on lähetetty asiakkaalle.
author: omulvad
manager: tfehr
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesTable, SalesEditLines,  SrsReportViewerForm, SalesTableLineQuantity, CustPackingSlipJournal
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9a2079ae02c01d30eb648e9cc95ee9cf6599048b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5205878"
---
# <a name="ship-sales-orders-without-warehousing"></a><span data-ttu-id="38142-103">Myyntitilausten lähettäminen ilman varastointia</span><span class="sxs-lookup"><span data-stu-id="38142-103">Ship sales orders without warehousing</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="38142-104">Tässä aiheessa kerrotaan, miten myyntitilaus päivitetään, kun tuotteet on lähetetty asiakkaalle.</span><span class="sxs-lookup"><span data-stu-id="38142-104">This topic explains how to update a sales order when products are shipped to the customer.</span></span> <span data-ttu-id="38142-105">Opastus koskee toteutustyönkulkua, jota ei ole määritetty varastonhallintaa varten (ei perus- eikä lisätason varastointiin), joten se ei edellytä tuotteen keräilyn rekisteröintiä ennen lähetystä.</span><span class="sxs-lookup"><span data-stu-id="38142-105">The guide is applicable to the fulfillment flow that is not set up for warehouse management (neither basic or advanced warehousing), and therefore does not require product picking to be registered before shipment.</span></span> <span data-ttu-id="38142-106">Voit suorittaa tämän menettelyn USMF-demoyrityksen tiedoilla tai käyttää omia tietoja.</span><span class="sxs-lookup"><span data-stu-id="38142-106">You can run this procedure on your own data or in demo data company USMF.</span></span> <span data-ttu-id="38142-107">Molemmissa tapauksissa ennen tehtävän aloittamista varastoidulle tuotteelle on luotava myyntitilaus, jonka määrä on suurempi kuin 1.</span><span class="sxs-lookup"><span data-stu-id="38142-107">In both cases, before you start this task, create a sales order for an inventoried product with a quantity of greater than 1.</span></span> <span data-ttu-id="38142-108">Kirjausvirheen välttämiseksi sinun on tarkistettava, että tuotteen varastossa oleva määrä tilaukseen valitussa toimipaikassa ja varastossa riittää kattamaan tilausmäärän.</span><span class="sxs-lookup"><span data-stu-id="38142-108">To avoid a posting error, you need to check that the product's on-hand quantity in the site and warehouse that you've selected on the order covers the order quantity.</span></span>

## <a name="post-packing-slip-for-an-order"></a><span data-ttu-id="38142-109">Kirjaa tilauksen pakkausluettelo</span><span class="sxs-lookup"><span data-stu-id="38142-109">Post packing slip for an order</span></span>
1. <span data-ttu-id="38142-110">Valitse **Siirtymisruutu > Moduulit > Myynti ja markkinointi > Myyntitilaukset > Kaikki myyntitilaukset**.</span><span class="sxs-lookup"><span data-stu-id="38142-110">In the navigation pane, go to **Modules > Sales and marketing > Sales orders > All sales orders**.</span></span>
2. <span data-ttu-id="38142-111">Etsi ja valitse luettelossa tehtävää varten luotu tilaus.</span><span class="sxs-lookup"><span data-stu-id="38142-111">In the list, find and select the order you have created for this task.</span></span>
3. <span data-ttu-id="38142-112">Valitse toimintoruudussa **Kerää ja pakkaa**.</span><span class="sxs-lookup"><span data-stu-id="38142-112">On the Action Pane, select **Pick and pack**.</span></span>
4. <span data-ttu-id="38142-113">Valitse **Kirjaa pakkausluettelo**.</span><span class="sxs-lookup"><span data-stu-id="38142-113">Select **Post packing slip**.</span></span>
5. <span data-ttu-id="38142-114">Laajenna tai tiivistä **Parametrit**-osa.</span><span class="sxs-lookup"><span data-stu-id="38142-114">Expand or collapse the **Parameters** section.</span></span>
6. <span data-ttu-id="38142-115">Valitse **Määrä**-kentässä **Kaikki**.</span><span class="sxs-lookup"><span data-stu-id="38142-115">In the **Quantity** field, select **All**.</span></span>
    - <span data-ttu-id="38142-116">Vaihtoehtoja ovat lisäksi **Toimita nyt** ja **Keräilty**.</span><span class="sxs-lookup"><span data-stu-id="38142-116">Other options include **Deliver now** and **Picked**.</span></span> <span data-ttu-id="38142-117">Jos tilausrivi toimitetaan osittain ja tilausrivin **Toimita nyt** -kentässä on määrä, valitaan **Toimita nyt**.</span><span class="sxs-lookup"><span data-stu-id="38142-117">If the order line is to be shipped partially and the **Deliver now** field on the order line contains a quantity, you would select **Deliver now**.</span></span> <span data-ttu-id="38142-118">Jos organisaation toteuttamistyönkulku sisältää keräilyn erillisenä, keräysluettelon hallitsemana ja rekisteröimänä prosessina, valitaan **Keräilty**.</span><span class="sxs-lookup"><span data-stu-id="38142-118">If your organization's fulfillment flow includes picking as a separate process that is managed by and registered with a picking list, you would select **Picked**.</span></span>  
    - <span data-ttu-id="38142-119">Tarkista, että **Kirjaus**-asetukseksi on valittu **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="38142-119">Check that the **Posting** option is set to **Yes**.</span></span>  
7. <span data-ttu-id="38142-120">Valitse **Tulosta pakkausluettelo** -asetukseksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="38142-120">Set the **Print packing slip** option to **Yes**.</span></span> <span data-ttu-id="38142-121">Tälle kirjaukselle luotavat pakkausluettelot ovat **Yhteenveto**-välilehdessä.</span><span class="sxs-lookup"><span data-stu-id="38142-121">The **Overview** tab contains a list of packing slips to be generated in this posting.</span></span> <span data-ttu-id="38142-122">Jos toimitat yksittäisen tilauksen, pakkausluetteloita on yleensä yksi.</span><span class="sxs-lookup"><span data-stu-id="38142-122">If you are shipping an individual order, there will typically be one packing slip.</span></span> <span data-ttu-id="38142-123">Jos kyseiseen tilauksen rivit kuitenkin toimitetaan eri toimipaikoista, kirjaus jaetaan automaattisesti niin, että asiakirjoja on tarvittava määrä.</span><span class="sxs-lookup"><span data-stu-id="38142-123">However, if that order's lines are to be shipped from different sites, posting will automatically be split into the appropriate number of documents.</span></span> <span data-ttu-id="38142-124">Tämä on pakollinen ehto, jota ei voi muuttaa.</span><span class="sxs-lookup"><span data-stu-id="38142-124">This is a mandatory condition that cannot be changed.</span></span> <span data-ttu-id="38142-125">Kirjaus jaetaan vastaavasti useisiin asiakirjoihin myös silloin, jos tilauksen rivit lähetetään eri toimitusosoitteisiin ja lähetyskäytäntö määrittää jaon pakolliseksi.</span><span class="sxs-lookup"><span data-stu-id="38142-125">Similarly, the posting will also be split into multiple documents if the order's lines are to be shipped to different delivery addresses, and the shipping policy is set up to require a split.</span></span>  
8. <span data-ttu-id="38142-126">Valitse **Rivit**-välilehdessä lähetettävän tilausrivin rivi.</span><span class="sxs-lookup"><span data-stu-id="38142-126">On the **Lines** tab, select the row for the order line to be shipped.</span></span>
9. <span data-ttu-id="38142-127">Lisää **Päivitä**-kenttään luku, joka on pienempi kuin alkuperäinen määrä.</span><span class="sxs-lookup"><span data-stu-id="38142-127">In the **Update** field, enter a number lower than the original quantity.</span></span>
10. <span data-ttu-id="38142-128">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="38142-128">Select **OK**.</span></span>
11. <span data-ttu-id="38142-129">Valitse **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="38142-129">Select **Yes**.</span></span>
12. <span data-ttu-id="38142-130">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="38142-130">Close the page.</span></span>
13. <span data-ttu-id="38142-131">Valitse toimintoruudussa **Asetukset**.</span><span class="sxs-lookup"><span data-stu-id="38142-131">On the Action Pane, select **Options**.</span></span>
14. <span data-ttu-id="38142-132">Valitse **Vaihda näyttö**.</span><span class="sxs-lookup"><span data-stu-id="38142-132">Select **Change view**.</span></span>
15. <span data-ttu-id="38142-133">Valitse **Otsikkonäkymä**.</span><span class="sxs-lookup"><span data-stu-id="38142-133">Select **Header view**.</span></span>
    - <span data-ttu-id="38142-134">Jos kaikki tilauksen rivit on lähetetty kokonaisuudessa, tilauksen tila muuttuu avoimesta toimitetuksi.</span><span class="sxs-lookup"><span data-stu-id="38142-134">If all of the lines on the order have been fully shipped, the order status changes from Open to Delivered.</span></span>  
    - <span data-ttu-id="38142-135">Tässä esimerkissä tilausrivi on toimitettu osittain.</span><span class="sxs-lookup"><span data-stu-id="38142-135">In this example, the order line has been shipped partially.</span></span> <span data-ttu-id="38142-136">Tämän vuoksi vielä tilaus on edelleen avoinna.</span><span class="sxs-lookup"><span data-stu-id="38142-136">This is why the the order status remains Open.</span></span>     
    - <span data-ttu-id="38142-137">**Asiakirjan tila** -kentän asetuksena on Pakkausluettelo, koska vähintään yksi tilausriveistä on lähetetty.</span><span class="sxs-lookup"><span data-stu-id="38142-137">The **Document status** field is set to Packing slip because at least one of the order lines have been shipped.</span></span>  
16. <span data-ttu-id="38142-138">Valitse toimintoruudussa **Yleiset**.</span><span class="sxs-lookup"><span data-stu-id="38142-138">On the Action Pane, select **General**.</span></span>
17. <span data-ttu-id="38142-139">Valitse **Rivin määrä**.</span><span class="sxs-lookup"><span data-stu-id="38142-139">Select **Line quantity**.</span></span>
18. <span data-ttu-id="38142-140">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="38142-140">Close the page.</span></span>
19. <span data-ttu-id="38142-141">Valitse toimintoruudussa **Kerää ja pakkaa**.</span><span class="sxs-lookup"><span data-stu-id="38142-141">On the Action Pane, select **Pick and pack**.</span></span>
20. <span data-ttu-id="38142-142">Valitse **Pakkausluettelo**.</span><span class="sxs-lookup"><span data-stu-id="38142-142">Select **Packing slip**.</span></span> <span data-ttu-id="38142-143">Kaikki tilausta varten luodut pakkausluetteloasiakirjat ovat **Pakkausluettelo-kirjauskansio**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="38142-143">The **Packing slip journal** page contains all the packing slip documents that were generated for your order.</span></span> <span data-ttu-id="38142-144">Voit tarvittaessa tarkastella kunkin asiakirjan tietoja ja tulostaa ne.</span><span class="sxs-lookup"><span data-stu-id="38142-144">You can review details of each document and print them, if you wish.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]