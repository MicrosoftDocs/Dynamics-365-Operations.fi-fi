---
title: Luo uusi kauppasopimus
description: Tämä menetelmä selittää, miten luodaan kauppasopimus, johon rekisteröidään tuotteen tietyn asiakkaan kanssa sovittu uusi hinta.
author: omulvad
manager: AnnBe
ms.date: 11/16/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e132cd20437b7929e81fcaa123d70bb57fb320c8
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/15/2019
ms.locfileid: "1549264"
---
# <a name="create-a-new-trade-agreement"></a><span data-ttu-id="d56dc-103">Luo uusi kauppasopimus</span><span class="sxs-lookup"><span data-stu-id="d56dc-103">Create a new trade agreement</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d56dc-104">Tämä menetelmä selittää, miten luodaan kauppasopimus, johon rekisteröidään tuotteen tietyn asiakkaan kanssa sovittu uusi hinta.</span><span class="sxs-lookup"><span data-stu-id="d56dc-104">This procedure shows you how to create a trade agreement where you register a new product sales price that you've agreed with a specific customer.</span></span> <span data-ttu-id="d56dc-105">Voit suorittaa tämän menettelyn esittely-yrityksen USMF kanssa tai käyttää omia tietojasi.</span><span class="sxs-lookup"><span data-stu-id="d56dc-105">You can run this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="d56dc-106">Jos käytät omia tietojasi, varmista ennen tämän ohjeen käyttöä, että kauppasopimuksen kirjauskansion nimi on kohteeseen, jossa Oletussuhde-arvoksi on valittu Hinta (myynti).</span><span class="sxs-lookup"><span data-stu-id="d56dc-106">If you’re using your own data, before you start this guide you need to make sure that a Trade agreement journal name exists where the Default relation is set to “Price (sales)”.</span></span>


## <a name="create-and-post-a-new-trade-agreement-journal"></a><span data-ttu-id="d56dc-107">Luo ja kirjaa uusi kauppasopimuksen kirjauskansi</span><span class="sxs-lookup"><span data-stu-id="d56dc-107">Create and post a new trade agreement journal</span></span>
1. <span data-ttu-id="d56dc-108">Valitse Myynti ja markkinointi > Hinnat ja alennukset > Kauppasopimuksen kirjauskansiot.</span><span class="sxs-lookup"><span data-stu-id="d56dc-108">Go to Sales and marketing > Prices and discounts > Trade agreement journals.</span></span>
2. <span data-ttu-id="d56dc-109">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="d56dc-109">Click New.</span></span>
3. <span data-ttu-id="d56dc-110">Avaa haku valitsemalla Nimi-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="d56dc-110">In the Name field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="d56dc-111">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="d56dc-111">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="d56dc-112">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="d56dc-112">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="d56dc-113">Valitse Rivit.</span><span class="sxs-lookup"><span data-stu-id="d56dc-113">Click Lines.</span></span>
7. <span data-ttu-id="d56dc-114">Valitse Tilikoodi-kentässä Taulu.</span><span class="sxs-lookup"><span data-stu-id="d56dc-114">In the Account code field, select 'Table'.</span></span>
    * <span data-ttu-id="d56dc-115">Tässä esimerkissä päivitetään tietyn asiakkaan hinta, joten sinun on valittava Taulu.</span><span class="sxs-lookup"><span data-stu-id="d56dc-115">In this example, you're updating the price for a specific customer, which means you need to choose Table.</span></span> <span data-ttu-id="d56dc-116">Jos päivittäisit tuotteen luettelohinnan, valitsisit Kaikki, jotta uusi hinta koskisi kaikkia asiakkaita.</span><span class="sxs-lookup"><span data-stu-id="d56dc-116">If you were updating the product's list price, you would select All, so that the new price is valid for all customers.</span></span> <span data-ttu-id="d56dc-117">Jos eri asiakassegmenteillä olisi eri hinta, valitsisit Ryhmä.</span><span class="sxs-lookup"><span data-stu-id="d56dc-117">If you were differentiating prices among different customer segments, then you would select Group.</span></span> <span data-ttu-id="d56dc-118">Ryhmä-vaihtoehdon käyttö edellyttää asiakkaan hintaryhmien määrittämistä.</span><span class="sxs-lookup"><span data-stu-id="d56dc-118">To select Group, you must have set up Customer price groups.</span></span>  
8. <span data-ttu-id="d56dc-119">Avaa haku napsauttamalla Tilin valinta -kentässä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="d56dc-119">In the Account selection field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="d56dc-120">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="d56dc-120">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="d56dc-121">Valitse Nimikekoodi-kentässä Taulu.</span><span class="sxs-lookup"><span data-stu-id="d56dc-121">In the Item code field, select 'Table'.</span></span>
    * <span data-ttu-id="d56dc-122">Kun annat kauppasopimuksen tyypiksi Hinta (myynti), Nimikekoodi-kentässä valitaan vain Taulu.</span><span class="sxs-lookup"><span data-stu-id="d56dc-122">When you are entering a trade agreement of type 'Price (sales)', you must only select 'Table' in the Item code field.</span></span> <span data-ttu-id="d56dc-123">Tämä johtuu siitä, että hinta on absoluuttinen arvo eikä kaikilla tuotteilla tai tuoteryhmillä voi olla sama hinta.</span><span class="sxs-lookup"><span data-stu-id="d56dc-123">This is because a price is an absolute value and cannot be same for all products or a group of products.</span></span>  
11. <span data-ttu-id="d56dc-124">Avaa haku napsauttamalla Nimikesuhde-kentässä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="d56dc-124">In the Item relation field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="d56dc-125">Valitse luettelossa sopimukseen sisällytettävä tuote.</span><span class="sxs-lookup"><span data-stu-id="d56dc-125">In the list, select the product you want to include in the agreement.</span></span>
    * <span data-ttu-id="d56dc-126">Kirjaa muistiin valitsemasi tuotteet.</span><span class="sxs-lookup"><span data-stu-id="d56dc-126">Make a note of which product you've selected.</span></span>  
13. <span data-ttu-id="d56dc-127">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="d56dc-127">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="d56dc-128">Anna Mistä-kenttään vähimmäismäärä.</span><span class="sxs-lookup"><span data-stu-id="d56dc-128">In the From field, enter a minimum quantity.</span></span>
    * <span data-ttu-id="d56dc-129">Jos asiakkaalla on tietty määrä, joka on tilattava ennen uuden hinnan käyttöönottoa, määrä on ilmoitettava tässä.</span><span class="sxs-lookup"><span data-stu-id="d56dc-129">If the customer has to order a minimum quantity  before they can qualify for the new price, then you need to specify that quantity here.</span></span>  
    * <span data-ttu-id="d56dc-130">Määritä Mihin-kenttään arvo, jota suurempana sopimuksen hinta ei kelpaa.</span><span class="sxs-lookup"><span data-stu-id="d56dc-130">Enter a value in the To field to specify the maximum quantity above which the agreement's price will not be valid.</span></span> <span data-ttu-id="d56dc-131">Jos hinnat ja alennukset perustuvat useisiin hintarajoihin, määritä kunkin hintahaarukan vähimmäis- ja enimmäismäärä Mistä- ja Mihin-kenttiin.</span><span class="sxs-lookup"><span data-stu-id="d56dc-131">If you offer prices and discounts based on multiple quantity breaks, then specify each quantity bracket as a pair of minimum and maximum quantity in the 'From' and 'To' fields respectively.</span></span>  
15. <span data-ttu-id="d56dc-132">Anna Summa valuuttana -kenttään hinta.</span><span class="sxs-lookup"><span data-stu-id="d56dc-132">In the Amount in currency field, enter a price.</span></span>
16. <span data-ttu-id="d56dc-133">Anna Päivämäärästä-kenttää päivämäärä, jolloin sopimus astuu voimaan.</span><span class="sxs-lookup"><span data-stu-id="d56dc-133">In the From date field, enter a date from which this agreement will be valid.</span></span>
17. <span data-ttu-id="d56dc-134">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="d56dc-134">Click Save.</span></span>
18. <span data-ttu-id="d56dc-135">Valitse Vahvista.</span><span class="sxs-lookup"><span data-stu-id="d56dc-135">Click Validate.</span></span>
19. <span data-ttu-id="d56dc-136">Valitse Tarkista valitut rivit.</span><span class="sxs-lookup"><span data-stu-id="d56dc-136">Click Validate selected lines.</span></span>
20. <span data-ttu-id="d56dc-137">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="d56dc-137">Click OK.</span></span>
21. <span data-ttu-id="d56dc-138">Valitse Kirjaa.</span><span class="sxs-lookup"><span data-stu-id="d56dc-138">Click Post.</span></span>
22. <span data-ttu-id="d56dc-139">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="d56dc-139">Click OK.</span></span>

## <a name="view-trade-agreements-for-a-product"></a><span data-ttu-id="d56dc-140">Näytä tuotteen kauppasopimukset</span><span class="sxs-lookup"><span data-stu-id="d56dc-140">View trade agreements for a product</span></span>
1. <span data-ttu-id="d56dc-141">Mene Tuotetietojen hallinta > Tuotteet > Vapautetut tuotteet.</span><span class="sxs-lookup"><span data-stu-id="d56dc-141">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="d56dc-142">Etsi ja valitse luettelosta tuote, jonka hinnan päivitit.</span><span class="sxs-lookup"><span data-stu-id="d56dc-142">In the list, find and select the product whose price you have just updated.</span></span>
3. <span data-ttu-id="d56dc-143">Valitse toimintoruudussa Myynti.</span><span class="sxs-lookup"><span data-stu-id="d56dc-143">On the Action Pane, click Sell.</span></span>
4. <span data-ttu-id="d56dc-144">Valitse Näytä kauppasopimukset.</span><span class="sxs-lookup"><span data-stu-id="d56dc-144">Click View trade agreements.</span></span>
    * <span data-ttu-id="d56dc-145">Tarkastele juuri luodun hinnan kauppasopimuksen tietoja.</span><span class="sxs-lookup"><span data-stu-id="d56dc-145">Review the details of the price trade agreement you have just created.</span></span>    
5. <span data-ttu-id="d56dc-146">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="d56dc-146">Close the page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d56dc-147">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="d56dc-147">Additional resources</span></span>
### <a name="community-blogs"></a><span data-ttu-id="d56dc-148">Yhteisöblogit</span><span class="sxs-lookup"><span data-stu-id="d56dc-148">Community blogs</span></span>
- [<span data-ttu-id="d56dc-149">Dynamics 365 for Finance and Operationsin myyntihinnat</span><span class="sxs-lookup"><span data-stu-id="d56dc-149">Sales prices in Dynamics 365 for Finance and Operations</span></span>](https://financefunction.tech/2018/11/14/sales-prices-in-dynamics-365-for-finance-and-operations/#sales_price_in_trade_agreements)
