---
title: Luo uusi kauppasopimus
description: Tämä menetelmä selittää, miten luodaan kauppasopimus, johon rekisteröidään tuotteen tietyn asiakkaan kanssa sovittu uusi hinta.
author: omulvad
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TradeNonStockedConversion, TradeNonStockedConversionChangeWizard, TradeNonStockedConversionCheckWorksheet, TradeNonStockedConversionWizard, TradeNonStockedRegister
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 592b3d0265a3be92a5a823c6aabdd40b4e3f0a27
ms.sourcegitcommit: 890a0b3eb3c1f48d786b0789e5bb8641e0b8455e
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/20/2021
ms.locfileid: "5919938"
---
# <a name="create-a-new-trade-agreement"></a><span data-ttu-id="e3019-103">Luo uusi kauppasopimus</span><span class="sxs-lookup"><span data-stu-id="e3019-103">Create a new trade agreement</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e3019-104">Tämä menetelmä selittää, miten luodaan kauppasopimus, johon rekisteröidään tuotteen tietyn asiakkaan kanssa sovittu uusi hinta.</span><span class="sxs-lookup"><span data-stu-id="e3019-104">This procedure shows you how to create a trade agreement where you register a new product sales price that you've agreed with a specific customer.</span></span> <span data-ttu-id="e3019-105">Voit suorittaa tämän menettelyn esittely-yrityksen USMF kanssa tai käyttää omia tietojasi.</span><span class="sxs-lookup"><span data-stu-id="e3019-105">You can run this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="e3019-106">Jos käytät omia tietojasi, varmista ennen tämän ohjeen käyttöä, että kauppasopimuksen kirjauskansion nimi on kohteeseen, jossa Oletussuhde-arvoksi on valittu Hinta (myynti).</span><span class="sxs-lookup"><span data-stu-id="e3019-106">If you're using your own data, before you start this guide you need to make sure that a Trade agreement journal name exists where the Default relation is set to "Price (sales)".</span></span>

## <a name="create-and-post-a-new-trade-agreement-journal"></a><span data-ttu-id="e3019-107">Luo ja kirjaa uusi kauppasopimuksen kirjauskansi</span><span class="sxs-lookup"><span data-stu-id="e3019-107">Create and post a new trade agreement journal</span></span>

1. <span data-ttu-id="e3019-108">Valitse **Siirtymisruutu > Moduulit >Myynti ja markkinointi > Hinnat ja alennukset > Kauppasopimuksen kirjauskansiot**.</span><span class="sxs-lookup"><span data-stu-id="e3019-108">Go to **Navigation pane > Modules > Sales and marketing > Prices and discounts > Trade agreement journals**.</span></span>
2. <span data-ttu-id="e3019-109">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="e3019-109">Click **New**.</span></span>
3. <span data-ttu-id="e3019-110">Avaa haku valitsemalla **Nimi**-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="e3019-110">In the **Name** field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="e3019-111">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="e3019-111">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="e3019-112">Valitse **toimintoruudussa** **Rivit**.</span><span class="sxs-lookup"><span data-stu-id="e3019-112">On **Action Pane**, click **Lines**.</span></span>
6. <span data-ttu-id="e3019-113">Valitse **Tilikoodi**-kentässä Taulu.</span><span class="sxs-lookup"><span data-stu-id="e3019-113">In the **Account code** field, select 'Table'.</span></span>
    
    <span data-ttu-id="e3019-114">Tässä esimerkissä päivitetään tietyn asiakkaan hinta, joten sinun on valittava Taulu.</span><span class="sxs-lookup"><span data-stu-id="e3019-114">In this example, you're updating the price for a specific customer, which means you need to choose Table.</span></span> <span data-ttu-id="e3019-115">Jos päivittäisit tuotteen luettelohinnan, valitsisit Kaikki, jotta uusi hinta koskisi kaikkia asiakkaita.</span><span class="sxs-lookup"><span data-stu-id="e3019-115">If you were updating the product's list price, you would select 'All', so that the new price is valid for all customers.</span></span> <span data-ttu-id="e3019-116">Jos eri asiakassegmenteillä olisi eri hinta, valitsisit Ryhmä.</span><span class="sxs-lookup"><span data-stu-id="e3019-116">If you were differentiating prices among different customer segments, then you would select Group.</span></span> <span data-ttu-id="e3019-117">Ryhmä-vaihtoehdon käyttö edellyttää asiakkaan hintaryhmien määrittämistä.</span><span class="sxs-lookup"><span data-stu-id="e3019-117">To select Group, you must have set up Customer price groups.</span></span>  

7. <span data-ttu-id="e3019-118">Avaa haku napsauttamalla **Tilin valinta** -kentässä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="e3019-118">In the **Account selection** field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="e3019-119">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="e3019-119">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="e3019-120">Valitse **Nimikekoodi**-kentässä Taulu.</span><span class="sxs-lookup"><span data-stu-id="e3019-120">In the **Item code** field, select 'Table'.</span></span>
    
    <span data-ttu-id="e3019-121">Kun annat kauppasopimuksen tyypiksi Hinta (myynti), **Nimikekoodi**-kentässä valitaan vain Taulu.</span><span class="sxs-lookup"><span data-stu-id="e3019-121">When you are entering a trade agreement of type 'Price (sales)', you must only select 'Table' in the **Item code** field.</span></span> <span data-ttu-id="e3019-122">Tämä johtuu siitä, että hinta on absoluuttinen arvo eikä kaikilla tuotteilla tai tuoteryhmillä voi olla sama hinta.</span><span class="sxs-lookup"><span data-stu-id="e3019-122">This is because a price is an absolute value and cannot be same for all products or a group of products.</span></span>
    
10. <span data-ttu-id="e3019-123">Avaa haku napsauttamalla **Nimikkeen suhde**-kentässä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="e3019-123">In the **Item relation** field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="e3019-124">Valitse luettelossa sopimukseen sisällytettävä tuote.</span><span class="sxs-lookup"><span data-stu-id="e3019-124">In the list, select the product you want to include in the agreement.</span></span> <span data-ttu-id="e3019-125">Kirjaa muistiin valitsemasi tuotteet.</span><span class="sxs-lookup"><span data-stu-id="e3019-125">Make a note of which product you've selected.</span></span>  
12. <span data-ttu-id="e3019-126">Anna **Mistä**-kenttään vähimmäismäärä.</span><span class="sxs-lookup"><span data-stu-id="e3019-126">In the **From** field, enter a minimum quantity.</span></span>
    - <span data-ttu-id="e3019-127">Jos asiakkaalla on tietty määrä, joka on tilattava ennen uuden hinnan käyttöönottoa, määrä on ilmoitettava tässä.</span><span class="sxs-lookup"><span data-stu-id="e3019-127">If the customer has to order a minimum quantity before they can qualify for the new price, then you need to specify that quantity here.</span></span>  
    - <span data-ttu-id="e3019-128">Määritä **Mihin**-kenttään arvo, jota suurempana sopimuksen hinta ei kelpaa.</span><span class="sxs-lookup"><span data-stu-id="e3019-128">Enter a value in the **To** field to specify the maximum quantity above which the agreement's price will not be valid.</span></span> <span data-ttu-id="e3019-129">Jos hinnat ja alennukset perustuvat useisiin hintarajoihin, määritä kunkin hintahaarukan vähimmäis- ja enimmäismäärä **Mistä**- ja **Mihin**-kenttiin.</span><span class="sxs-lookup"><span data-stu-id="e3019-129">If you offer prices and discounts based on multiple quantity breaks, then specify each quantity bracket as a pair of minimum and maximum quantity in the **From** and **To** fields respectively.</span></span>
13. <span data-ttu-id="e3019-130">Anna **Summa valuuttana** -kenttään hinta.</span><span class="sxs-lookup"><span data-stu-id="e3019-130">In the **Amount in currency field**, enter a price.</span></span>
14. <span data-ttu-id="e3019-131">Anna **Tiedot**-osan **Päivämäärästä**-kenttään päivämäärä, jolloin sopimus astuu voimaan.</span><span class="sxs-lookup"><span data-stu-id="e3019-131">Under the **Details** section, in the **From date** field, enter a date from which this agreement will be valid.</span></span>
15. <span data-ttu-id="e3019-132">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="e3019-132">Click **Save**.</span></span>
16. <span data-ttu-id="e3019-133">Valitse **Vahvista**.</span><span class="sxs-lookup"><span data-stu-id="e3019-133">Click **Validate**.</span></span>
17. <span data-ttu-id="e3019-134">Valitse **Tarkista valitut rivit**.</span><span class="sxs-lookup"><span data-stu-id="e3019-134">Click **Validate selected lines**.</span></span>
18. <span data-ttu-id="e3019-135">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="e3019-135">Click **OK**.</span></span>
19. <span data-ttu-id="e3019-136">Valitse **Kirjaa**.</span><span class="sxs-lookup"><span data-stu-id="e3019-136">Click **Post**.</span></span>
20. <span data-ttu-id="e3019-137">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="e3019-137">Click **OK**.</span></span>

## <a name="view-trade-agreements-for-a-product"></a><span data-ttu-id="e3019-138">Näytä tuotteen kauppasopimukset</span><span class="sxs-lookup"><span data-stu-id="e3019-138">View trade agreements for a product</span></span>

1. <span data-ttu-id="e3019-139">Valitse **Siirtymisruutu > Moduulit > Tuotetietojen hallinta > Tuotteet > Vapautetut tuotteet**.</span><span class="sxs-lookup"><span data-stu-id="e3019-139">Go to **Navigation pane > Modules > Product information management > Products > Released products**.</span></span>
2. <span data-ttu-id="e3019-140">Etsi ja valitse luettelosta tuote, jonka hinnan päivitit.</span><span class="sxs-lookup"><span data-stu-id="e3019-140">In the list, find and select the product whose price you have just updated.</span></span>
3. <span data-ttu-id="e3019-141">Valitse **toimintoruudussa** **Myynti**.</span><span class="sxs-lookup"><span data-stu-id="e3019-141">On the **Action Pane**, click **Sell**.</span></span>
4. <span data-ttu-id="e3019-142">Valitse **Näytä kauppasopimukset**.</span><span class="sxs-lookup"><span data-stu-id="e3019-142">Click **View trade agreements**.</span></span>
    
    <span data-ttu-id="e3019-143">Tarkastele juuri luodun hinnan kauppasopimuksen tietoja.</span><span class="sxs-lookup"><span data-stu-id="e3019-143">Review the details of the price trade agreement you have just created.</span></span>

5. <span data-ttu-id="e3019-144">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="e3019-144">Close the page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e3019-145">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="e3019-145">Additional resources</span></span>

### <a name="whitepaper"></a><span data-ttu-id="e3019-146">Tekninen raportti</span><span class="sxs-lookup"><span data-stu-id="e3019-146">Whitepaper</span></span>

<span data-ttu-id="e3019-147">Lisätietoja saa lataamalla seuraava tekninen raportti (joka on kirjoitettu tukemaan AX2012-versiota, mutta koskee myös Dynamics 365 Supply Chain Managementia)</span><span class="sxs-lookup"><span data-stu-id="e3019-147">For more information, download the following white paper (written to support AX2012, but still applies for Dynamics 365 Supply Chain Management)</span></span>

- [<span data-ttu-id="e3019-148">Kauppasopimukset</span><span class="sxs-lookup"><span data-stu-id="e3019-148">Trade agreements</span></span>](https://download.microsoft.com/download/0/2/9/02972c8b-0159-4936-a3ef-1e64252b2d2f/TradeAgreementsInAX.pdf)

### <a name="community-blogs"></a><span data-ttu-id="e3019-149">Yhteisöblogit</span><span class="sxs-lookup"><span data-stu-id="e3019-149">Community blogs</span></span>

- [<span data-ttu-id="e3019-150">Dynamics 365 for Finance and Operationsin myyntihinnat</span><span class="sxs-lookup"><span data-stu-id="e3019-150">Sales prices in Dynamics 365 for Finance and Operations</span></span>](https://financefunction.tech/2018/11/14/sales-prices-in-dynamics-365-for-finance-and-operations/#sales_price_in_trade_agreements)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]