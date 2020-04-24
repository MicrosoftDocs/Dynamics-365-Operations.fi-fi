---
title: Palautuksen kustannushinta ja erätunnus
description: Saatat haluta, että palautettujen tuotteiden kustannus vastaa tuotteiden kustannusta sinä hetkenä, kun myit tuotteet asiakkaalle. Voit tehdä tämän käyttämällä **Palauta erätunnus** -kenttää.
author: ShylaThompson
manager: tfehr
ms.date: 04/30/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReturnTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b3d038b90595511b25863865045c5ce8ad45b1e0
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/02/2020
ms.locfileid: "3216324"
---
# <a name="return-cost-price-and-return-lot-id"></a><span data-ttu-id="24471-104">Palautuksen kustannushinta ja erätunnus</span><span class="sxs-lookup"><span data-stu-id="24471-104">Return cost price and return lot ID</span></span>        

[!include [banner](../includes/banner.md)]



<span data-ttu-id="24471-105">Varastoon palautettavien tuotteiden kustannus lasketaan käyttämällä tuotteiden nykyistä kustannusta.</span><span class="sxs-lookup"><span data-stu-id="24471-105">The cost of products that are returned to inventory is calculated by using the current cost of the products.</span></span> <span data-ttu-id="24471-106">Saatat kuitenkin haluta, että palautettujen tuotteiden kustannus vastaa tuotteiden kustannusta sinä hetkenä, kun myit tuotteet asiakkaalle.</span><span class="sxs-lookup"><span data-stu-id="24471-106">However, you might want the cost of the returned products to equal the cost of the products at the time when you sold the products to the customer.</span></span> <span data-ttu-id="24471-107">Voit tehdä tämän käyttämällä **Palauta erätunnus** -kenttää, joka on **Rivin tiedot** -pikavälilehdellä **Myyntitilaus** -lomakkeessa.</span><span class="sxs-lookup"><span data-stu-id="24471-107">You can do this by using the **Return lot ID** field on the **Line details** FastTab in the **Sales order** form.</span></span>

<span data-ttu-id="24471-108">Tässä on yksi esimerkkitilanne.</span><span class="sxs-lookup"><span data-stu-id="24471-108">For example, consider the following scenario.</span></span> <span data-ttu-id="24471-109">Teet asiakkaalle laskun.</span><span class="sxs-lookup"><span data-stu-id="24471-109">You invoice a customer.</span></span> <span data-ttu-id="24471-110">Asiakas palauttaa toimitetut tuotteet sinulle.</span><span class="sxs-lookup"><span data-stu-id="24471-110">Then, the customer returns the delivered products to you.</span></span> <span data-ttu-id="24471-111">Palautat tuotteen varastoon.</span><span class="sxs-lookup"><span data-stu-id="24471-111">You return the products to stock.</span></span> <span data-ttu-id="24471-112">Tässä tapauksessa kyseisten tuotteiden kustannus lasketaan käyttämällä tuotteiden nykyistä kustannusta, kun hyvität palautetut tuotteet asiakkaalle.</span><span class="sxs-lookup"><span data-stu-id="24471-112">In this case, when you credit the customer for the returned products, the cost of those products is calculated by using the current cost of the products.</span></span> <span data-ttu-id="24471-113">Jos käytät **Palauta erätunnus** -kenttää, palautettujen tuotteiden kustannus lasketaan asiakkaan alkuperäisessä laskussa olevan kustannuksen mukaan.</span><span class="sxs-lookup"><span data-stu-id="24471-113">However, if you use the **Return lot ID** field, the cost of the returned products is calculated by using the cost on the invoice of the original sale to the customer.</span></span>

<span data-ttu-id="24471-114">Jos haluat käyttää muuta kuin nykyistä kustannusta asiakkaan palautuksille, käytä jotakin seuraavista tavoista.</span><span class="sxs-lookup"><span data-stu-id="24471-114">To use a cost other than the current cost for returns from a customer, use one of the following methods.</span></span>

## <a name="method-1-manually-enter-the-return-cost-price"></a><span data-ttu-id="24471-115">Menetelmä 1: Syötä palautuksen kustannushinta käsin</span><span class="sxs-lookup"><span data-stu-id="24471-115">Method 1: Manually enter the return cost price</span></span>

<span data-ttu-id="24471-116">Oletusarvon mukaan lisätessäsi nimikkeitä palautustilaukseen nimikkeet palautetaan varastoon nykyisellä kustannushinnalla.</span><span class="sxs-lookup"><span data-stu-id="24471-116">By default, when you add items to a return order, the items are returned to inventory at the current cost price.</span></span> <span data-ttu-id="24471-117">Voit määrittää muun palautuksen kustannushinnan seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="24471-117">To specify a different return cost price, follow these steps.</span></span>

1.  <span data-ttu-id="24471-118">Valitse **Myynti ja markkinointi** \> **Yleinen** \> **Palautustilaukset** \> **Kaikki palautustilaukset**.</span><span class="sxs-lookup"><span data-stu-id="24471-118">Click **Sales and marketing** \> **Common** \> **Return orders** \> **All return orders**.</span></span>

2.  <span data-ttu-id="24471-119">Valitse **toimintoruudussa** **Uusi** -ryhmästä **Palautustilaus**.</span><span class="sxs-lookup"><span data-stu-id="24471-119">On the **Action Pane**, in the **New** group, click **Return order**.</span></span>

3.  <span data-ttu-id="24471-120">Valitse **Luo palautustilaus** -lomakkeessa asiakastili ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="24471-120">In the **Create return order** form, select a customer account, and then click **OK**.</span></span>

4.  <span data-ttu-id="24471-121">Valitse **Palautustilaus - palautusnumero: %1, %2** -lomakkeessa nimike, ja kirjoita negatiivinen määrä **Määrä**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="24471-121">In the **Return order - RMA number: %1, %2** form, select an item, and then enter a negative quantity in the **Quantity** field.</span></span>

5.  <span data-ttu-id="24471-122">Valitse **Rivin erittely** -pikavälilehti.</span><span class="sxs-lookup"><span data-stu-id="24471-122">Click the **Line details** FastTab.</span></span>

6.  <span data-ttu-id="24471-123">Syötä **Yleinen**-välilehdessä arvo **Palautuksen kustannushinta** -kenttään.</span><span class="sxs-lookup"><span data-stu-id="24471-123">On the **General** tab, enter a value in the **Return cost price** field.</span></span> <span data-ttu-id="24471-124">Tätä arvoa käytetään, kun tavaroita palautetaan varastoon.</span><span class="sxs-lookup"><span data-stu-id="24471-124">This value is used when the goods are returned to inventory.</span></span> <span data-ttu-id="24471-125">Jos et syötä arvoa, nykyistä kustannushintaa käytetään, kun tavaroita palautetaan varastoon.</span><span class="sxs-lookup"><span data-stu-id="24471-125">If you do not enter a value, the current cost price is used when the goods are returned to inventory.</span></span>

## <a name="method-2-automatically-generate-the-cost-price-based-on-the-customer-invoice-line"></a><span data-ttu-id="24471-126">Menetelmä 2: Luo kustannushinta automaattisesti myyntilaskun rivin perusteella</span><span class="sxs-lookup"><span data-stu-id="24471-126">Method 2: Automatically generate the cost price based on the customer invoice line</span></span>

<span data-ttu-id="24471-127">Tämä on ensisijainen menetelmä palautusrivien luomiseen.</span><span class="sxs-lookup"><span data-stu-id="24471-127">This is the preferred method to use to create return lines.</span></span> <span data-ttu-id="24471-128">Käyttääksesi tuotteiden kustannusta, joka oli voimassa kun tuotteet myytiin asiakkaalle, luo palautustilaus ja määritä myyntirivi palautukseen.</span><span class="sxs-lookup"><span data-stu-id="24471-128">To use the cost of the products at the time when you sold the products to the customer, create a return order and specify a sales line to return.</span></span>

1.  <span data-ttu-id="24471-129">Valitse **Myynti ja markkinointi** \> **Yleinen** \> **Palautustilaukset** \> **Kaikki palautustilaukset**.</span><span class="sxs-lookup"><span data-stu-id="24471-129">Click **Sales and marketing** \> **Common** \> **Return orders** \> **All return orders**.</span></span>

2.  <span data-ttu-id="24471-130">Valitse **toimintoruudussa** **Uusi** -ryhmästä **Palautustilaus**.</span><span class="sxs-lookup"><span data-stu-id="24471-130">On the **Action Pane**, in the **New** group, click **Return order**.</span></span>

3.  <span data-ttu-id="24471-131">Valitse **Luo palautustilaus** -lomakkeessa asiakastili ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="24471-131">In the **Create return order** form, select a customer account, and then click **OK**.</span></span>

4.  <span data-ttu-id="24471-132">Valitse **Palautustilaus - palautusnumero: %1, %2** -lomakkeen **toimintoruudussa** **Etsi myyntitilaus**.</span><span class="sxs-lookup"><span data-stu-id="24471-132">In the **Return order - RMA number: %1, %2** form, on the **Action Pane**, click **Find sales order**.</span></span>

5.  <span data-ttu-id="24471-133">Valitse **Etsi myyntitilaus** -lomakkeessa palautettava laskurivi ja napsauta sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="24471-133">In the **Find sales order** form, select the invoice line to return, and then click **OK**.</span></span>
    
    <span data-ttu-id="24471-134">**Rivin erittely** -pikavälilehden **Yleinen**-välilehdessä oleva **Palauta erätunnus** -kenttä näyttää alkuperäisen myyntirivin arvon.</span><span class="sxs-lookup"><span data-stu-id="24471-134">On the **Line details** FastTab, on the **General** tab, the **Return lot ID** field displays the value from the original sales line.</span></span> <span data-ttu-id="24471-135">Lisäksi **Palautuksen kustannushinta** -kentässä näkyy alkuperäisen myyntirivin kustannusarvo.</span><span class="sxs-lookup"><span data-stu-id="24471-135">Additionally, the **Return cost price** field displays the cost value from the original sales line.</span></span>

## <a name="cost-calculation-example"></a><span data-ttu-id="24471-136">Kustannuksen esimerkkilaskelma</span><span class="sxs-lookup"><span data-stu-id="24471-136">Cost calculation example</span></span>

<span data-ttu-id="24471-137">Kun käytät **Palauta erätunnus** -kenttää palautustilausrivillä palautuksen kustannushinnan määrittämiseksi, palautustilausrivin kustannusta käytetään.</span><span class="sxs-lookup"><span data-stu-id="24471-137">When you use the **Return lot ID** field on a return order line to specify the return cost price, the cost on the return order line is used.</span></span> <span data-ttu-id="24471-138">Jos suoritat varaston sulkemis- tai uudelleenlaskentatoiminnon, kustannus oikaistaan alkuperäisellä myyntirivillä.</span><span class="sxs-lookup"><span data-stu-id="24471-138">If you run the inventory close or recalculation functionality, the cost is adjusted on the original sales line.</span></span> <span data-ttu-id="24471-139">Palautustilausrivin kustannus oikaistaan automaattisesti samaan kappalekohtaiseen kustannukseen.</span><span class="sxs-lookup"><span data-stu-id="24471-139">The cost on the return order line is automatically adjusted to reflect the same cost per piece.</span></span>

1.  <span data-ttu-id="24471-140">Luo ja vapauta tuote, jonka nimi on Testi.</span><span class="sxs-lookup"><span data-stu-id="24471-140">Create and release a product that is named Test.</span></span> <span data-ttu-id="24471-141">Määritä **Vapautetun tuotteen tiedot** -lomakkeessa seuraavat tiedot:</span><span class="sxs-lookup"><span data-stu-id="24471-141">In the **Released product details** form, specify the following information:</span></span>
    
    1.  <span data-ttu-id="24471-142">Valitse **Kustannusten hallinta** -pikavälilehden **Nimikeryhmä**-kentässä **Osat**-ryhmä.</span><span class="sxs-lookup"><span data-stu-id="24471-142">On the **Manage costs** FastTab, in the **Item group** field, select the **Parts** group.</span></span>
    
    2.  <span data-ttu-id="24471-143">Valitse **Yleinen**-pikavälilehden **Nimikemalliryhmä**-kentässä **DEF**.</span><span class="sxs-lookup"><span data-stu-id="24471-143">On the **General** FastTab, in the **Item model group** field, select **DEF**.</span></span>
    
    3.  <span data-ttu-id="24471-144">Kirjoita **Osto**-pikavälilehden **Hinta**-kenttään 10.00 nimikkeen hintayksiköksi.</span><span class="sxs-lookup"><span data-stu-id="24471-144">On the **Purchase** FastTab, in the **Price** field, type 10.00 as the cost price of the item.</span></span>
    
    4.  <span data-ttu-id="24471-145">Valitse **toimintoruudussa** **Dimensioryhmät**.</span><span class="sxs-lookup"><span data-stu-id="24471-145">On the **Action Pane**, click **Dimension groups**.</span></span> <span data-ttu-id="24471-146">Valitse **Varastodimensioryhmä**-kentässä **Vain toimipaikka ja varasto**.</span><span class="sxs-lookup"><span data-stu-id="24471-146">In the **Storage dimension group** field, select **Site and Warehouse only**.</span></span> <span data-ttu-id="24471-147">Valitse **Seurantadimensioryhmä**-kentässä **Ei aktiivisia seurantadimensioita**.</span><span class="sxs-lookup"><span data-stu-id="24471-147">In the **Tracking dimension group** field, select **No active tracking dimensions**.</span></span>

2.  <span data-ttu-id="24471-148">Luo ostotilaus 10 kappaleelle Testi-nimikettä kappalehinnalla 6,00, ja kirjaa sitten lasku ostotilaukselle.</span><span class="sxs-lookup"><span data-stu-id="24471-148">Create a purchase order for 10 pieces of the Test item at 6.00 per piece, and then post an invoice for the purchase order.</span></span>
    
    <span data-ttu-id="24471-149">Luo toinen ostotilaus 10 kappaleelle Testi-nimikettä kappalehinnalla 8,00, ja kirjaa sitten lasku ostotilaukselle.</span><span class="sxs-lookup"><span data-stu-id="24471-149">Create a second purchase order for 10 pieces of the Test item at 8.00 per piece, and then post an invoice for the purchase order.</span></span>

3.  <span data-ttu-id="24471-150">Kirjaa laskun myyntitilaukselle myydäksesi viisi kappaletta Testi-nimikettä.</span><span class="sxs-lookup"><span data-stu-id="24471-150">Post an invoice for a sales order to sell five pieces of the Test item.</span></span>
    
    <span data-ttu-id="24471-151">Tässä tapauksessa myyntitilausrivin kustannus on 35,00 (5 kappaletta \*keskimääräinen kustannus per kappale 7,00).</span><span class="sxs-lookup"><span data-stu-id="24471-151">In this case, the sales order line is costed at 35.00 (5 pieces \* 7.00 average cost per piece).</span></span>

4.  <span data-ttu-id="24471-152">Luo palautustilaus asiakkaalle.</span><span class="sxs-lookup"><span data-stu-id="24471-152">Create a return order for the customer.</span></span> <span data-ttu-id="24471-153">Valitse **Etsi myyntitilaus** -lomakkeessa laskurivi ja napsauta sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="24471-153">In the **Find sales order** form, select the invoice line, and then click **OK**.</span></span>

5.  <span data-ttu-id="24471-154">Tarkista **Palautustilaus - palautusnumero: %1, %2** -lomakkeessa, että palautustilaus luodaan Testi-nimikkeen palautusta varten.</span><span class="sxs-lookup"><span data-stu-id="24471-154">In the **Return order - RMA number: %1, %2** form, verify that a return order is generated to return the Test item.</span></span> <span data-ttu-id="24471-155">Palautustilauksen määräksi määritetään -5,00.</span><span class="sxs-lookup"><span data-stu-id="24471-155">The quantity of the return order is set to -5.00.</span></span>
    
    <span data-ttu-id="24471-156">**Palauta erätunnus** -kentässä näkyy erätunnus.</span><span class="sxs-lookup"><span data-stu-id="24471-156">The **Return lot ID** field displays a lot ID.</span></span> <span data-ttu-id="24471-157">Tämä erätunnus haetaan asiakkaalle alkunperin myydyn nimikkeen myyntitilauksesta.</span><span class="sxs-lookup"><span data-stu-id="24471-157">This lot ID is taken from the original sales order of the item that was sold to the customer.</span></span> <span data-ttu-id="24471-158">**Palautuksen kustannushinta** -kentässä näkyy alkuperäisen myyntirivin kustannushinta.</span><span class="sxs-lookup"><span data-stu-id="24471-158">The **Return cost price** field displays the cost price from the original sales line.</span></span>

6.  <span data-ttu-id="24471-159">Rekisteröi palautettujen nimikkeiden vastaanotto.</span><span class="sxs-lookup"><span data-stu-id="24471-159">Register the receipt of the returned items.</span></span>

7.  <span data-ttu-id="24471-160">Kirjaa pakkausluettelo palautetuille nimikkeille.</span><span class="sxs-lookup"><span data-stu-id="24471-160">Post a packing slip for the returned items.</span></span>

8.  <span data-ttu-id="24471-161">Kirjaa palautustilauksen lasku.</span><span class="sxs-lookup"><span data-stu-id="24471-161">Post an invoice for the return order.</span></span> <span data-ttu-id="24471-162">Valitse **Kaikki myyntitilaukset** -luettelosivulla myyntitilaus, jonka tilaustyyppi on **Palautustilaus**.</span><span class="sxs-lookup"><span data-stu-id="24471-162">On the **All sales orders** list page, select a sales order for which **Returned order** is the order type.</span></span>

9.  <span data-ttu-id="24471-163">Avaa **Varastotapahtumat**-lomake.</span><span class="sxs-lookup"><span data-stu-id="24471-163">Open the **Inventory transactions** form.</span></span> <span data-ttu-id="24471-164">Varmista, että palautuksen kappalekohtainen kustannus on 7,00 käyttämällä **Palautuksen kustannushinta** -arvoa, jolloin **Kustannussumma**-kentän summa on 35,00.</span><span class="sxs-lookup"><span data-stu-id="24471-164">Verify that the return is costed at 7.00 per piece by using the value in the **Return cost price** field, for a total of 35.00 in the **Cost amount** field.</span></span> <span data-ttu-id="24471-165">Voit avata **Varastotapahtumat**-lomakkeen **Palautustilaus - palautusnumero: %1, %2** -lomakkeesta.</span><span class="sxs-lookup"><span data-stu-id="24471-165">You can open the **Inventory transactions** form from the **Return order - RMA number: %1, %2** form.</span></span> <span data-ttu-id="24471-166">Valitse **Rivit**-ruudukossa **Varasto** \> **Tapahtumat**.</span><span class="sxs-lookup"><span data-stu-id="24471-166">In the **Lines** grid, click **Inventory** \> **Transactions**.</span></span>

10. <span data-ttu-id="24471-167">Käyt Varastonhallinta-moduulin **Päätös ja oikaisu** -lomaketta **Sulje**-menettelyn suorittamiseksi.</span><span class="sxs-lookup"><span data-stu-id="24471-167">In Inventory and warehouse management, use the **Closing and adjustment** form to run the **3. Close** procedure.</span></span>
    
    <span data-ttu-id="24471-168">Tämä toiminto oikaisee alkuperäisen myyntirivin kustannuksen -35,00 (5 kappaletta \* 7,00) muotoon -30,00 (5 kappaletta \* 6,00).</span><span class="sxs-lookup"><span data-stu-id="24471-168">This action adjusts the cost on the original sales line that was costed at -35.00 (5 pieces \* 7.00) to -30.00 (5 pieces \* 6.00).</span></span> <span data-ttu-id="24471-169">Tämä johtuu siitä, varastomalliryhmä käyttää First in, First out (FIFO) -mallia ja kappalehinta 6,00 on FIFO-kustannus ensimmäisestä ostotilauksesta.</span><span class="sxs-lookup"><span data-stu-id="24471-169">This is because the inventory model group uses First in, First out (FIFO), and 6.00 per piece is the FIFO cost from the first purchase order.</span></span> <span data-ttu-id="24471-170">Lisäksi toiminto oikaisee palautuksen myyntirivin kustannuksen vastaamaan alkuperäisen myyntitilausrivin kappalehintaa.</span><span class="sxs-lookup"><span data-stu-id="24471-170">Additionally, the action adjusts the cost on the return sales line to match the cost per piece on the original sales line.</span></span> <span data-ttu-id="24471-171">Palautusrivin kustannus oikaistaan siten 35,00 > 30,00.</span><span class="sxs-lookup"><span data-stu-id="24471-171">Therefore, the cost of the return line is adjusted from 35.00 to 30.00.</span></span>




