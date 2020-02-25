---
title: Modernin myyntipisteen (MPOS) asiakastilaukset
description: Tässä ohjeaiheessa on tietoja asiakkaiden tilauksista Modern POS (MPOS) -laitteissa. Asiakastilauksia kutsutaan myös erikoistilauksiksi. Aihe sisältää keskustelun liittyvistä parametreista ja tapahtumatyönkuluista.
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailFunctionalityProfile
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 260594
ms.assetid: 6fc835ef-d62e-4f23-9d49-50299be642ca
ms.search.region: global
ms.search.industry: Retail
ms.author: anpurush
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: b8ea8339c2ad25ceed2415eb5ccf5e2048c612fa
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/01/2020
ms.locfileid: "3022349"
---
# <a name="customer-orders-in-modern-pos-mpos"></a><span data-ttu-id="2e529-105">Modernin myyntipisteen (MPOS) asiakastilaukset</span><span class="sxs-lookup"><span data-stu-id="2e529-105">Customer orders in Modern POS (MPOS)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="2e529-106">Tässä ohjeaiheessa on tietoja asiakkaiden tilauksista Modern POS (MPOS) -laitteissa.</span><span class="sxs-lookup"><span data-stu-id="2e529-106">This topic provides information about customer orders in Modern POS (MPOS).</span></span> <span data-ttu-id="2e529-107">Asiakastilauksia kutsutaan myös erikoistilauksiksi.</span><span class="sxs-lookup"><span data-stu-id="2e529-107">Customer orders are also known as special orders.</span></span> <span data-ttu-id="2e529-108">Aihe sisältää keskustelun liittyvistä parametreista ja tapahtumatyönkuluista.</span><span class="sxs-lookup"><span data-stu-id="2e529-108">The topic includes a discussion of related parameters and transaction flows.</span></span>

<span data-ttu-id="2e529-109">Monikanavaisessa kaupan maailmassa monet vähittäiskauppiaat tarjoavat asiakastilausten eli erikoistilausten mahdollisuuden täyttääkseen erilaisia eri tuote- ja palveluvaatimuksia.</span><span class="sxs-lookup"><span data-stu-id="2e529-109">In an omni-channel commerce world, many retailers provide the option of customer orders, or special orders, to meet various product and fulfillment requirements.</span></span> <span data-ttu-id="2e529-110">Seuraavassa on joitakin tyypillisiä skenaarioita:</span><span class="sxs-lookup"><span data-stu-id="2e529-110">Here are some typical scenarios:</span></span>

- <span data-ttu-id="2e529-111">Asiakas haluaa, että tuotteet toimitetaan tiettynä päivänä tiettyyn osoitteeseen.</span><span class="sxs-lookup"><span data-stu-id="2e529-111">A customer wants products to be delivered to a specific address on a specific date.</span></span>
- <span data-ttu-id="2e529-112">Asiakas haluaa noutaa tuotteet myymälästä tai sijainnista, joka on eri kuin myymälä tai sijainti, josta asiakas osti nämä tuotteet.</span><span class="sxs-lookup"><span data-stu-id="2e529-112">A customer wants to pick up products from a store or location that differs from the store or location where the customer purchased those products.</span></span>
- <span data-ttu-id="2e529-113">Asiakas haluaa jonkun toisen noutavan ostamansa tuotteet.</span><span class="sxs-lookup"><span data-stu-id="2e529-113">A customer wants someone else to pick up products that the customer purchased.</span></span>

<span data-ttu-id="2e529-114">Vähittäiskauppiaat käyttävät asiakastilauksia myös pienentääkseen menetettyä myyntiä, jota varaston tyhjeneminen voi muuten aiheuttaa, koska kauppatavara voidaan toimittaa tai kerätä eri aikaan tai eri paikasta.</span><span class="sxs-lookup"><span data-stu-id="2e529-114">Retailers also use customer orders to minimize lost sales that stock outages might otherwise cause, because the merchandise can be delivered or picked up at a different time or place.</span></span>

## <a name="set-up-customer-orders"></a><span data-ttu-id="2e529-115">Määritä asiakastilaukset</span><span class="sxs-lookup"><span data-stu-id="2e529-115">Set up customer orders</span></span>

<span data-ttu-id="2e529-116">Seuraavassa on joitakin parametreja, jotka voidaan asettaa **Commercen parametrit** -sivulla määrittääksesi, miten asiakkaiden tilaukset suoritetaan:</span><span class="sxs-lookup"><span data-stu-id="2e529-116">Here are some of the parameters that can be set on the **Commerce parameters** page to define how customer orders are fulfilled:</span></span>

- <span data-ttu-id="2e529-117">**Oletuskäsirahaprosentti** – määritä summa, joka asiakkaan on maksettava talletuksena ennen tilauksen vahvistamista.</span><span class="sxs-lookup"><span data-stu-id="2e529-117">**Default deposit percentage** – Specify the amount that the customer must pay as a deposit before an order can be confirmed.</span></span> <span data-ttu-id="2e529-118">Oletuskäsirahaprosentti lasketaan prosenttiosuutena tilauksen arvosta.</span><span class="sxs-lookup"><span data-stu-id="2e529-118">The default deposit amount is calculated as a percentage of the order value.</span></span> <span data-ttu-id="2e529-119">Oikeuksista riippuen myymälän johtaja saattaa pysytä ohittamaan summan käyttämällä asetusta **Talletuksen ohitus**.</span><span class="sxs-lookup"><span data-stu-id="2e529-119">Depending on privileges, a store associate might be able to override the amount by using **Deposit override**.</span></span>
- <span data-ttu-id="2e529-120">**Peruutusmaksuprosentti** – Jos asiakkaan tilauksen peruuttamisesta perittään maksu, määritä kyseisen maksun määrä.</span><span class="sxs-lookup"><span data-stu-id="2e529-120">**Cancellation charge percentage** – If a charge will be applied when a customer order is canceled, specify the amount of that charge.</span></span>
- <span data-ttu-id="2e529-121">**Peruutusmaksun koodi** – Jos asiakkaan tilauksen peruuttamisesta perittään maksu, kyseinen maksu näkyy myyntitilauksessa maksukoodina.</span><span class="sxs-lookup"><span data-stu-id="2e529-121">**Cancellation charge code** – If a charge will be applied when a customer order is canceled, that charge will be reflected under a charge code on the sales order.</span></span> <span data-ttu-id="2e529-122">Tämän parametrin avulla voit määrittää peruutusmaksun koodin.</span><span class="sxs-lookup"><span data-stu-id="2e529-122">Use this parameter to define the cancellation charge code.</span></span>
- <span data-ttu-id="2e529-123">**Toimitusmaksun koodi** – Vähittäiskauppiaat voivat veloittaa ylimääräisen lisämaksun tavaran lähettämisestä asiakkaalle.</span><span class="sxs-lookup"><span data-stu-id="2e529-123">**Shipping charge code** – Retailers can charge an extra fee for shipping merchandise to a customer.</span></span> <span data-ttu-id="2e529-124">Tämän toimitusmaksu näkyy maksukoodina myyntitilauksessa.</span><span class="sxs-lookup"><span data-stu-id="2e529-124">The amount of that shipping charge will be reflected under a charge code on the sales order.</span></span> <span data-ttu-id="2e529-125">Tämän parametrin avulla voit yhdistää toimitusmaksun koodia toimitusmaksuihin asiakastilauksessa.</span><span class="sxs-lookup"><span data-stu-id="2e529-125">Use this parameter to map the shipping charge code to shipping charges on the customer order.</span></span>
- <span data-ttu-id="2e529-126">**Palauta toimitusmaksut** – Määritä, ovatko asiakastilaukseen liittyvät toimitusmaksut palautettavia.</span><span class="sxs-lookup"><span data-stu-id="2e529-126">**Refund shipping charges** – Specify whether shipping charges that are associated with a customer order are refundable.</span></span>
- <span data-ttu-id="2e529-127">**Enimmäissumma ilman hyväksyntää** – Jos kuljetusmaksut ovat palautettavia, määritä palautustilausten toimitusmaksujen palautusten enimmäismäärä.</span><span class="sxs-lookup"><span data-stu-id="2e529-127">**Maximum amount without approval** – If shipping charges are refundable, specify the maximum amount of shipping charge refunds across return orders.</span></span> <span data-ttu-id="2e529-128">Jos tämä määrä ylittyy, toiminnon jatkaminen edellyttää esimiehen hyväksyntää.</span><span class="sxs-lookup"><span data-stu-id="2e529-128">If this amount is exceeded, manager override is required in order to continue with the refund.</span></span> <span data-ttu-id="2e529-129">Sopeutuakseen seuraaviin skenaarioihin, toimitusmaksujen palautus voi ylittää alunperin maksetun summan:</span><span class="sxs-lookup"><span data-stu-id="2e529-129">To accommodate the following scenarios, a refund of shipping charges can exceed the amount that was originally paid:</span></span>

    - <span data-ttu-id="2e529-130">Kulut otetaan käyttöön myyntitilauksen otsikon tasolla ja kun tuotelinjan jokin määrä palautetaan, suurinta tuotteille ja määrälle sallittua toimitusmaksun palautusta ei voi määrittää tavalla, joka toimii kaikille asiakkaille.</span><span class="sxs-lookup"><span data-stu-id="2e529-130">Charges are applied at the level of the sales order header, and when some quantity of a product line is returned, the maximum refund of shipping charges that is allowed for the products and the quantity can't be determined in way that works for all customers.</span></span>
    - <span data-ttu-id="2e529-131">Kuljetusmaksut syntyvät toimituksen kaikissa esiintymissä.</span><span class="sxs-lookup"><span data-stu-id="2e529-131">Shipping charges are incurred for every instance of shipping.</span></span> <span data-ttu-id="2e529-132">Jos asiakas palauttaa tuotteet useita kertoja ja jälleenmyyjän käytäntö määrittää, että vähittäismyyjä vasta toimituskustannuksista, palautettavat kuljetusmaksut ovat enemmän kuin todelliset kuljetusmaksut.</span><span class="sxs-lookup"><span data-stu-id="2e529-132">If a customer returns products multiple times, and the retailer's policy specifies that the retailer will bear the cost of return shipping charges, the return shipping charges will be more than the actual shipping charges.</span></span>

## <a name="transaction-flow-for-customer-orders"></a><span data-ttu-id="2e529-133">Asiakastilausten tapahtumien työnkulku</span><span class="sxs-lookup"><span data-stu-id="2e529-133">Transaction flow for customer orders</span></span>

### <a name="create-a-customer-order-in-modern-pos"></a><span data-ttu-id="2e529-134">Asiakastilauksen luonti Modern POS:ssa</span><span class="sxs-lookup"><span data-stu-id="2e529-134">Create a customer order in Modern POS</span></span>

1. <span data-ttu-id="2e529-135">Lisää asiakas tapahtumaan.</span><span class="sxs-lookup"><span data-stu-id="2e529-135">Add a customer to the transaction.</span></span>
2. <span data-ttu-id="2e529-136">Lisää tuotteet ostoskoriin.</span><span class="sxs-lookup"><span data-stu-id="2e529-136">Add products to the cart.</span></span>
3. <span data-ttu-id="2e529-137">Valitse **Luo asiakastilaus** ja valitse sitten tilauksen tyyppi.</span><span class="sxs-lookup"><span data-stu-id="2e529-137">Click **Create customer order**, and then select the order type.</span></span> <span data-ttu-id="2e529-138">Tilauksen tyyppi voi olla joko **Asiakastilaus** tai **Tarjous**.</span><span class="sxs-lookup"><span data-stu-id="2e529-138">The order type can be either **Customer order** or **Quote**.</span></span>
4. <span data-ttu-id="2e529-139">Valitse **Lähetä valitut** tai **Lähetä kaikki** toimittaaksesi tuotteet asiakastilin osoitteeseen. Määritä pyydetty lähetyspäivä ja kuljetusmaksut.</span><span class="sxs-lookup"><span data-stu-id="2e529-139">Click **Ship selected** or **Ship all** to ship the products to an address on the customer account, specify the requested shipping date, and specify shipping charges.</span></span>
5. <span data-ttu-id="2e529-140">Valitse **Kerää valitut** tai **Kerää kaikki** valitaksesi tuotteet, jotka kerätään nykyisestä myymälästä tai eri myymälästä tiettynä päivänä.</span><span class="sxs-lookup"><span data-stu-id="2e529-140">Click **Pick up selected** or **Pick-up all** to select products that will be picked up from the current store or a different store on a specific date.</span></span>
6. <span data-ttu-id="2e529-141">Veloita talletussumma, jos seitä vaaditaan.</span><span class="sxs-lookup"><span data-stu-id="2e529-141">Collect the deposit amount, if a deposit is required.</span></span>

### <a name="edit-an-existing-customer-order"></a><span data-ttu-id="2e529-142">Olemassa olevan asiakkaan tilauksen muokkaaminen</span><span class="sxs-lookup"><span data-stu-id="2e529-142">Edit an existing customer order</span></span>

1. <span data-ttu-id="2e529-143">Valitse kotisivulla **Etsi tilaus**.</span><span class="sxs-lookup"><span data-stu-id="2e529-143">On the home page, click **Find an order**.</span></span>
2. <span data-ttu-id="2e529-144">Etsi ja valitse muokattava tilaus.</span><span class="sxs-lookup"><span data-stu-id="2e529-144">Find and select the order to edit.</span></span> <span data-ttu-id="2e529-145">Valitse sivun alareunassa **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="2e529-145">At the bottom of the page, click the **Edit**.</span></span>

### <a name="pick-up-an-order"></a><span data-ttu-id="2e529-146">Kerää tilaus</span><span class="sxs-lookup"><span data-stu-id="2e529-146">Pick up an order</span></span>

1. <span data-ttu-id="2e529-147">Valitse kotisivulla **Etsi tilaus**.</span><span class="sxs-lookup"><span data-stu-id="2e529-147">On the home page, click **Find an order**.</span></span>
2. <span data-ttu-id="2e529-148">Valitse kerättävä tilaus.</span><span class="sxs-lookup"><span data-stu-id="2e529-148">Select the order to pick up.</span></span> <span data-ttu-id="2e529-149">Valitse sivun alareunassa **Keräys ja pakkaus**.</span><span class="sxs-lookup"><span data-stu-id="2e529-149">At the bottom of the page, click **Picking and packing**.</span></span>
3. <span data-ttu-id="2e529-150">Valitse **Kerää**.</span><span class="sxs-lookup"><span data-stu-id="2e529-150">Click **Pick up**.</span></span>

### <a name="cancel-an-order"></a><span data-ttu-id="2e529-151">Tilauksen peruuttaminen</span><span class="sxs-lookup"><span data-stu-id="2e529-151">Cancel an order</span></span>

1. <span data-ttu-id="2e529-152">Valitse kotisivulla **Etsi tilaus**.</span><span class="sxs-lookup"><span data-stu-id="2e529-152">On the home page, click **Find an order**.</span></span>
2. <span data-ttu-id="2e529-153">Valitse peruutettava tilaus.</span><span class="sxs-lookup"><span data-stu-id="2e529-153">Select the order to cancel.</span></span> <span data-ttu-id="2e529-154">Valitse sivun alareunassa **Peruuta**.</span><span class="sxs-lookup"><span data-stu-id="2e529-154">At the bottom of the page, click **Cancel**.</span></span>

### <a name="create-a-return-order"></a><span data-ttu-id="2e529-155">Palautustilauksen luominen</span><span class="sxs-lookup"><span data-stu-id="2e529-155">Create a return order</span></span>

1. <span data-ttu-id="2e529-156">Valitse kotisivulla **Etsi tilaus**.</span><span class="sxs-lookup"><span data-stu-id="2e529-156">On the home page, click **Find an order**.</span></span>
2. <span data-ttu-id="2e529-157">Valitse palautettava tilaus, valitse tilauksen lasku ja sitten tuotelinja, johon kauppatavara palautetaan.</span><span class="sxs-lookup"><span data-stu-id="2e529-157">Select the order to return, select the invoice for the order, and then select the product line for the merchandise to return.</span></span>
3. <span data-ttu-id="2e529-158">Valitse sivun alareunassa **Palautustilaus**.</span><span class="sxs-lookup"><span data-stu-id="2e529-158">At the bottom of the page, click the **Return order**.</span></span>

## <a name="asynchronous-transaction-flow-for-customer-orders"></a><span data-ttu-id="2e529-159">Asiakastilausten tapahtumien asynkroninen työnkulku</span><span class="sxs-lookup"><span data-stu-id="2e529-159">Asynchronous transaction flow for customer orders</span></span>

<span data-ttu-id="2e529-160">Asiakastilauksia voi luoda myyntipisteen (POS) asiakasohjelmassa joko synkronoidussa tai asynkronisessa tilassa.</span><span class="sxs-lookup"><span data-stu-id="2e529-160">Customer orders can be created from the point of sale (POS) client in either synchronous mode or asynchronous mode.</span></span>

### <a name="enable-customer-orders-to-be-created-in-asynchronous-mode"></a><span data-ttu-id="2e529-161">Ota käyttöön asiakastilausten luonti asynkronisessa tilassa</span><span class="sxs-lookup"><span data-stu-id="2e529-161">Enable customer orders to be created in asynchronous mode</span></span>

1. <span data-ttu-id="2e529-162">Valitse **Retail ja Commerce** &gt; **Kanavan asetukset** &gt; **POS-asetukset** &gt; **POS-profiili** &gt; **Toimintoprofiilit**.</span><span class="sxs-lookup"><span data-stu-id="2e529-162">Click **Retail and Commerce** &gt; **Channel setup** &gt; **POS setup** &gt; **POS profile** &gt; **Functionality profiles**.</span></span>
2. <span data-ttu-id="2e529-163">**Yleiset**-pikavälilehdessä määritä **Luo asiakastilaus asynkronisessa tilassa** -asetuksen arvoksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="2e529-163">On the **General** FastTab, set the **Create customer order in async mode** option to **Yes**.</span></span>

<span data-ttu-id="2e529-164">Kun **Luo asiakastilaus asynkronisessa tilassa** -asetuksen arvo on **Kyllä**, asiakastilaukset luodaan aina asynkronisessa tilassa, vaikka Retail Transaction Service (RTS) -palvelu on käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="2e529-164">When the **Create customer order in async mode** option is set to **Yes**, customer orders are always created in asynchronous mode, even if Retail Transaction Service (RTS) is available.</span></span> <span data-ttu-id="2e529-165">Jos määrität tämän asetuksen arvoksi **Ei**, asiakkaan tilaukset luodaan aina synkronoidussa tilassa RTS:n avulla.</span><span class="sxs-lookup"><span data-stu-id="2e529-165">If you set this option to **No**, customer orders are always created in synchronous mode by using RTS.</span></span> <span data-ttu-id="2e529-166">Kun asiakastilaukset on luotu asynkronisessa tilassa, ne ovat vedetään ja lisätään Commerceen Pull (P) -töitä käyttämällä.</span><span class="sxs-lookup"><span data-stu-id="2e529-166">When customer orders are created in asynchronous mode, they are pulled and inserted into Commerce by Pull (P) jobs.</span></span> <span data-ttu-id="2e529-167">Vastaavat myyntitilaukset luodaan, kun **Synkronoi tilaukset** suoritetaan joko manuaalisesti tai eräprosessina.</span><span class="sxs-lookup"><span data-stu-id="2e529-167">The corresponding sales orders are created when **Synchronize orders** is run either manually or through a batch process.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2e529-168">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="2e529-168">Additional resources</span></span>

[<span data-ttu-id="2e529-169">Asiakkaiden yhdistelmätilaukset</span><span class="sxs-lookup"><span data-stu-id="2e529-169">Hybrid customer orders</span></span>](hybrid-customer-orders.md)
