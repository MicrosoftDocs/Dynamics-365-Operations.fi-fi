---
title: Asiakastilausten yleiskatsaus
description: "Tässä ohjeaiheessa on tietoja asiakkaiden tilauksista Retail Modern POS (MPOS) -laitteissa. Asiakastilauksia kutsutaan myös erikoistilauksiksi. Aihe sisältää keskustelun liittyvistä parametreista ja tapahtumatyönkuluista."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
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
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: ce6774ede836eb29e6ef2cd8d4baa9efb931020c
ms.contentlocale: fi-fi
ms.lasthandoff: 11/03/2017

---

# <a name="customer-orders-overview"></a><span data-ttu-id="368a6-105">Asiakastilausten yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="368a6-105">Customer orders overview</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="368a6-106">Tässä ohjeaiheessa on tietoja asiakkaiden tilauksista Retail Modern POS (MPOS) -laitteissa.</span><span class="sxs-lookup"><span data-stu-id="368a6-106">This topic provides information about customer orders in Retail Modern POS (MPOS).</span></span> <span data-ttu-id="368a6-107">Asiakastilauksia kutsutaan myös erikoistilauksiksi.</span><span class="sxs-lookup"><span data-stu-id="368a6-107">Customer orders are also known as special orders.</span></span> <span data-ttu-id="368a6-108">Aihe sisältää keskustelun liittyvistä parametreista ja tapahtumatyönkuluista.</span><span class="sxs-lookup"><span data-stu-id="368a6-108">The topic includes a discussion of related parameters and transaction flows.</span></span>

<span data-ttu-id="368a6-109">Monikanavaisessa vähittäismyyntimaailmassa monet vähittäiskauppiaat tarjoavat asiakastilausten eli erikoistilausten mahdollisuuden täyttääkseen erilaisia eri tuote- ja palveluvaatimuksia.</span><span class="sxs-lookup"><span data-stu-id="368a6-109">In an omni-channel retail world, many retailers provide the option of customer orders, or special orders, to meet various product and fulfillment requirements.</span></span> <span data-ttu-id="368a6-110">Seuraavassa on joitakin tyypillisiä skenaarioita:</span><span class="sxs-lookup"><span data-stu-id="368a6-110">Here are some typical scenarios:</span></span>

-   <span data-ttu-id="368a6-111">Asiakas haluaa, että tuotteet toimitetaan tiettynä päivänä tiettyyn osoitteeseen.</span><span class="sxs-lookup"><span data-stu-id="368a6-111">A customer wants products to be delivered to a specific address on a specific date.</span></span>
-   <span data-ttu-id="368a6-112">Asiakas haluaa noutaa tuotteet myymälästä tai sijainnista, joka on eri kuin myymälä tai sijainti, josta asiakas osti nämä tuotteet.</span><span class="sxs-lookup"><span data-stu-id="368a6-112">A customer wants to pick up products from a store or location that differs from the store or location where the customer purchased those products.</span></span>
-   <span data-ttu-id="368a6-113">Asiakas haluaa jonkun toisen noutavan ostamansa tuotteet.</span><span class="sxs-lookup"><span data-stu-id="368a6-113">A customer wants someone else to pick up products that the customer purchased.</span></span>

<span data-ttu-id="368a6-114">Vähittäiskauppiaat käyttävät asiakastilauksia myös pienentääkseen menetettyä myyntiä, jota varaston tyhjeneminen voi muuten aiheuttaa, koska kauppatavara voidaan toimittaa tai kerätä eri aikaan tai eri paikasta.</span><span class="sxs-lookup"><span data-stu-id="368a6-114">Retailers also use customer orders to minimize lost sales that stock outages might otherwise cause, because the merchandise can be delivered or picked up at a different time or place.</span></span>

## <a name="set-up-customer-orders"></a><span data-ttu-id="368a6-115">Määritä asiakastilaukset</span><span class="sxs-lookup"><span data-stu-id="368a6-115">Set up customer orders</span></span>
<span data-ttu-id="368a6-116">Seuraavassa on joitakin parametreja, jotka voidaan asettaa **Vähittäismyynnin parametrit** -sivulla määrittääksesi, miten asiakkaiden tilaukset suoritetaan:</span><span class="sxs-lookup"><span data-stu-id="368a6-116">Here are some of the parameters that can be set on the **Retail parameters** page to define how customer orders are fulfilled:</span></span>

-   <span data-ttu-id="368a6-117">**Oletuskäsirahaprosentti** – määritä summa, joka asiakkaan on maksettava talletuksena ennen tilauksen vahvistamista.</span><span class="sxs-lookup"><span data-stu-id="368a6-117">**Default deposit percentage** – Specify the amount that the customer must pay as a deposit before an order can be confirmed.</span></span> <span data-ttu-id="368a6-118">Oletuskäsirahaprosentti lasketaan prosenttiosuutena tilauksen arvosta.</span><span class="sxs-lookup"><span data-stu-id="368a6-118">The default deposit amount is calculated as a percentage of the order value.</span></span> <span data-ttu-id="368a6-119">Oikeuksista riippuen myymälän johtaja saattaa pysytä ohittamaan summan käyttämällä asetusta **Talletuksen ohitus**.</span><span class="sxs-lookup"><span data-stu-id="368a6-119">Depending on privileges, a store associate might be able to override the amount by using **Deposit override**.</span></span>
-   <span data-ttu-id="368a6-120">**Peruutusmaksuprosentti** – Jos asiakkaan tilauksen peruuttamisesta perittään maksu, määritä kyseisen maksun määrä.</span><span class="sxs-lookup"><span data-stu-id="368a6-120">**Cancellation charge percentage** – If a charge will be applied when a customer order is canceled, specify the amount of that charge.</span></span>
-   <span data-ttu-id="368a6-121">**Peruutusmaksun koodi** – Jos asiakkaan tilauksen peruuttamisesta perittään maksu, kyseinen maksu näkyy myyntitilauksessa maksukoodina.</span><span class="sxs-lookup"><span data-stu-id="368a6-121">**Cancellation charge code** – If a charge will be applied when a customer order is canceled, that charge will be reflected under a charge code on the sales order.</span></span> <span data-ttu-id="368a6-122">Tämän parametrin avulla voit määrittää peruutusmaksun koodin.</span><span class="sxs-lookup"><span data-stu-id="368a6-122">Use this parameter to define the cancellation charge code.</span></span>
-   <span data-ttu-id="368a6-123">**Toimitusmaksun koodi** – Vähittäiskauppiaat voivat veloittaa ylimääräisen lisämaksun tavaran lähettämisestä asiakkaalle.</span><span class="sxs-lookup"><span data-stu-id="368a6-123">**Shipping charge code** – Retailers can charge an extra fee for shipping merchandise to a customer.</span></span> <span data-ttu-id="368a6-124">Tämän toimitusmaksu näkyy maksukoodina myyntitilauksessa.</span><span class="sxs-lookup"><span data-stu-id="368a6-124">The amount of that shipping charge will be reflected under a charge code on the sales order.</span></span> <span data-ttu-id="368a6-125">Tämän parametrin avulla voit yhdistää toimitusmaksun koodia toimitusmaksuihin asiakastilauksessa.</span><span class="sxs-lookup"><span data-stu-id="368a6-125">Use this parameter to map the shipping charge code to shipping charges on the customer order.</span></span>
-   <span data-ttu-id="368a6-126">**Palauta toimitusmaksut** – Määritä, ovatko asiakastilaukseen liittyvät toimitusmaksut palautettavia.</span><span class="sxs-lookup"><span data-stu-id="368a6-126">**Refund shipping charges** – Specify whether shipping charges that are associated with a customer order are refundable.</span></span>
-   <span data-ttu-id="368a6-127">**Enimmäissumma ilman hyväksyntää** – Jos kuljetusmaksut ovat palautettavia, määritä palautustilausten toimitusmaksujen palautusten enimmäismäärä.</span><span class="sxs-lookup"><span data-stu-id="368a6-127">**Maximum amount without approval** – If shipping charges are refundable, specify the maximum amount of shipping charge refunds across return orders.</span></span> <span data-ttu-id="368a6-128">Jos tämä määrä ylittyy, toiminnon jatkaminen edellyttää esimiehen hyväksyntää.</span><span class="sxs-lookup"><span data-stu-id="368a6-128">If this amount is exceeded, manager override is required in order to continue with the refund.</span></span> <span data-ttu-id="368a6-129">Sopeutuakseen seuraaviin skenaarioihin, toimitusmaksujen palautus voi ylittää alunperin maksetun summan:</span><span class="sxs-lookup"><span data-stu-id="368a6-129">To accommodate the following scenarios, a refund of shipping charges can exceed the amount that was originally paid:</span></span>
    -   <span data-ttu-id="368a6-130">Kulut otetaan käyttöön myyntitilauksen otsikon tasolla ja kun tuotelinjan jokin määrä palautetaan, suurinta tuotteille ja määrälle sallittua toimitusmaksun palautusta ei voi määrittää tavalla, joka toimii kaikille vähittäismyynnin asiakkaille.</span><span class="sxs-lookup"><span data-stu-id="368a6-130">Charges are applied at the level of the sales order header, and when some quantity of a product line is returned, the maximum refund of shipping charges that is allowed for the products and the quantity can't be determined in way that works for all retail customers.</span></span>
    -   <span data-ttu-id="368a6-131">Kuljetusmaksut syntyvät toimituksen kaikissa esiintymissä.</span><span class="sxs-lookup"><span data-stu-id="368a6-131">Shipping charges are incurred for every instance of shipping.</span></span> <span data-ttu-id="368a6-132">Jos asiakas palauttaa tuotteet useita kertoja ja jälleenmyyjän käytäntö määrittää, että vähittäismyyjä vasta toimituskustannuksista, palautettavat kuljetusmaksut ovat enemmän kuin todelliset kuljetusmaksut.</span><span class="sxs-lookup"><span data-stu-id="368a6-132">If a customer returns products multiple times, and the retailer’s policy specifies that the retailer will bear the cost of return shipping charges, the return shipping charges will be more than the actual shipping charges.</span></span>

## <a name="transaction-flow-for-customer-orders"></a><span data-ttu-id="368a6-133">Asiakastilausten tapahtumien työnkulku</span><span class="sxs-lookup"><span data-stu-id="368a6-133">Transaction flow for customer orders</span></span>
### <a name="create-a-customer-order-in-retail-modern-pos"></a><span data-ttu-id="368a6-134">Luo asiakastilaus Retail Modern POS -sovelluksessa</span><span class="sxs-lookup"><span data-stu-id="368a6-134">Create a customer order in Retail Modern POS</span></span>

1.  <span data-ttu-id="368a6-135">Lisää asiakas tapahtumaan.</span><span class="sxs-lookup"><span data-stu-id="368a6-135">Add a customer to the transaction.</span></span>
2.  <span data-ttu-id="368a6-136">Lisää tuotteet ostoskoriin.</span><span class="sxs-lookup"><span data-stu-id="368a6-136">Add products to the cart.</span></span>
3.  <span data-ttu-id="368a6-137">Valitse **Luo asiakastilaus** ja valitse sitten tilauksen tyyppi.</span><span class="sxs-lookup"><span data-stu-id="368a6-137">Click **Create customer order**, and then select the order type.</span></span> <span data-ttu-id="368a6-138">Tilauksen tyyppi voi olla joko **Asiakastilaus** tai **Tarjous**.</span><span class="sxs-lookup"><span data-stu-id="368a6-138">The order type can be either **Customer order** or **Quote**.</span></span>
4.  <span data-ttu-id="368a6-139">Valitse **Lähetä valitut** tai **Lähetä kaikki** toimittaaksesi tuotteet asiakastilin osoitteeseen. Määritä pyydetty lähetyspäivä ja kuljetusmaksut.</span><span class="sxs-lookup"><span data-stu-id="368a6-139">Click **Ship selected** or **Ship all** to ship the products to an address on the customer account, specify the requested shipping date, and specify shipping charges.</span></span>
5.  <span data-ttu-id="368a6-140">Valitse **Kerää valitut** tai **Kerää kaikki** valitaksesi tuotteet, jotka kerätään nykyisestä myymälästä tai eri myymälästä tiettynä päivänä.</span><span class="sxs-lookup"><span data-stu-id="368a6-140">Click **Pick up selected** or **Pick-up all** to select products that will be picked up from the current store or a different store on a specific date.</span></span>
6.  <span data-ttu-id="368a6-141">Veloita talletussumma, jos seitä vaaditaan.</span><span class="sxs-lookup"><span data-stu-id="368a6-141">Collect the deposit amount, if a deposit is required.</span></span>

### <a name="edit-an-existing-customer-order"></a><span data-ttu-id="368a6-142">Olemassa olevan asiakkaan tilauksen muokkaaminen</span><span class="sxs-lookup"><span data-stu-id="368a6-142">Edit an existing customer order</span></span>

1.  <span data-ttu-id="368a6-143">Valitse kotisivulla **Etsi tilaus**.</span><span class="sxs-lookup"><span data-stu-id="368a6-143">On the home page, click **Find an order**.</span></span>
2.  <span data-ttu-id="368a6-144">Etsi ja valitse muokattava tilaus.</span><span class="sxs-lookup"><span data-stu-id="368a6-144">Find and select the order to edit.</span></span> <span data-ttu-id="368a6-145">Valitse sivun alareunassa **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="368a6-145">At the bottom of the page, click the **Edit**.</span></span>

### <a name="pick-up-an-order"></a><span data-ttu-id="368a6-146">Kerää tilaus</span><span class="sxs-lookup"><span data-stu-id="368a6-146">Pick up an order</span></span>

1.  <span data-ttu-id="368a6-147">Valitse kotisivulla **Etsi tilaus**.</span><span class="sxs-lookup"><span data-stu-id="368a6-147">On the home page, click **Find an order**.</span></span>
2.  <span data-ttu-id="368a6-148">Valitse kerättävä tilaus.</span><span class="sxs-lookup"><span data-stu-id="368a6-148">Select the order to pick up.</span></span> <span data-ttu-id="368a6-149">Valitse sivun alareunassa **Keräys ja pakkaus**.</span><span class="sxs-lookup"><span data-stu-id="368a6-149">At the bottom of the page, click **Picking and packing**.</span></span>
3.  <span data-ttu-id="368a6-150">Valitse **Kerää**.</span><span class="sxs-lookup"><span data-stu-id="368a6-150">Click **Pick up**.</span></span>

### <a name="cancel-an-order"></a><span data-ttu-id="368a6-151">Tilauksen peruuttaminen</span><span class="sxs-lookup"><span data-stu-id="368a6-151">Cancel an order</span></span>

1.  <span data-ttu-id="368a6-152">Valitse kotisivulla **Etsi tilaus**.</span><span class="sxs-lookup"><span data-stu-id="368a6-152">On the home page, click **Find an order**.</span></span>
2.  <span data-ttu-id="368a6-153">Valitse peruutettava tilaus.</span><span class="sxs-lookup"><span data-stu-id="368a6-153">Select the order to cancel.</span></span> <span data-ttu-id="368a6-154">Valitse sivun alareunassa **Peruuta**.</span><span class="sxs-lookup"><span data-stu-id="368a6-154">At the bottom of the page, click **Cancel**.</span></span>

#### <a name="create-a-return-order"></a><span data-ttu-id="368a6-155">Palautustilauksen luominen</span><span class="sxs-lookup"><span data-stu-id="368a6-155">Create a return order</span></span>

1.  <span data-ttu-id="368a6-156">Valitse kotisivulla **Etsi tilaus**.</span><span class="sxs-lookup"><span data-stu-id="368a6-156">On the home page, click **Find an order**.</span></span>
2.  <span data-ttu-id="368a6-157">Valitse palautettava tilaus, valitse tilauksen lasku ja sitten tuotelinja, johon kauppatavara palautetaan.</span><span class="sxs-lookup"><span data-stu-id="368a6-157">Select the order to return, select the invoice for the order, and then select the product line for the merchandise to return.</span></span>
3.  <span data-ttu-id="368a6-158">Valitse sivun alareunassa **Palautustilaus**.</span><span class="sxs-lookup"><span data-stu-id="368a6-158">At the bottom of the page, click the **Return order**.</span></span>

## <a name="asynchronous-transaction-flow-for-customer-orders"></a><span data-ttu-id="368a6-159">Asiakastilausten tapahtumien asynkroninen työnkulku</span><span class="sxs-lookup"><span data-stu-id="368a6-159">Asynchronous transaction flow for customer orders</span></span>
<span data-ttu-id="368a6-160">Asiakastilauksia voi luoda myyntipisteen (POS) asiakasohjelmassa joko synkronoidussa tai asynkronisessa tilassa.</span><span class="sxs-lookup"><span data-stu-id="368a6-160">Customer orders can be created from the point of sale (POS) client in either synchronous mode or asynchronous mode.</span></span>

### <a name="enable-customer-orders-to-be-created-in-asynchronous-mode"></a><span data-ttu-id="368a6-161">Ota käyttöön asiakastilausten luonti asynkronisessa tilassa</span><span class="sxs-lookup"><span data-stu-id="368a6-161">Enable customer orders to be created in asynchronous mode</span></span>

1.  <span data-ttu-id="368a6-162">Valitse **Vähittäismyynti** &gt; **Kanavan asetukset** &gt; **POS-asetukset** &gt; **POS-profiilit** &gt; **Toimintoprofiilit**.</span><span class="sxs-lookup"><span data-stu-id="368a6-162">Click **Retail** &gt; **Channel setup** &gt; **POS setup** &gt; **POS profile** &gt; **Functionality profiles**.</span></span>
2.  <span data-ttu-id="368a6-163">**Yleiset**-pikavälilehdessä määritä **Luo asiakastilaus asynkronisessa tilassa** -asetuksen arvoksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="368a6-163">On the **General** FastTab, set the **Create customer order in async mode** option to **Yes**.</span></span>

<span data-ttu-id="368a6-164">Kun **Luo asiakastilaus asynkronisessa tilassa** -asetuksen arvo on **Kyllä**, asiakastilaukset luodaan aina asynkronisessa tilassa, vaikka Retail Transaction Service (RTS) -palvelu on käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="368a6-164">When the **Create customer order in async mode** option is set to **Yes**, customer orders are always created in asynchronous mode, even if Retail Transaction Service (RTS) is available.</span></span> <span data-ttu-id="368a6-165">Jos määrität tämän asetuksen arvoksi **Ei**, asiakkaan tilaukset luodaan aina synkronoidussa tilassa RTS:n avulla.</span><span class="sxs-lookup"><span data-stu-id="368a6-165">If you set this option to **No**, customer orders are always created in synchronous mode by using RTS.</span></span> <span data-ttu-id="368a6-166">Kun asiakastilaukset on luotu asynkronisessa tilassa, ne ovat vedetään ja lisätään Retailiin Pull (P) -töitä käyttämällä.</span><span class="sxs-lookup"><span data-stu-id="368a6-166">When customer orders are created in asynchronous mode, they are pulled and inserted into Retail by Pull (P) jobs.</span></span> <span data-ttu-id="368a6-167">Retailissa luodaan vastaavat myyntitilaukset, kun **Synkronoi tilaukset** suoritetaan joko manuaalisesti tai eräprosessina.</span><span class="sxs-lookup"><span data-stu-id="368a6-167">The corresponding sales orders are created in Retail when **Synchronize orders** is run either manually or through a batch process.</span></span>

<a name="see-also"></a><span data-ttu-id="368a6-168">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="368a6-168">See also</span></span>
--------

[<span data-ttu-id="368a6-169">Hybridit asiakastilaukset</span><span class="sxs-lookup"><span data-stu-id="368a6-169">Hybrid customer orders</span></span>](hybrid-customer-orders.md)




