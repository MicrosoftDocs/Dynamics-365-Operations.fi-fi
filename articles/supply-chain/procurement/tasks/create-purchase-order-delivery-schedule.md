--- 
title: Luo ostotilaus, jolla on toimitusaikataulu
description: "Tässä osoitetaan, miten ostotilaukselle luodaan toimitusaikataulu."
author: FrankDahl
manager: AnnBe
ms.date: 08/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 91a548d8fb6c46920fcb5660ac94c732fe27249a
ms.contentlocale: fi-fi
ms.lasthandoff: 05/08/2018

---
# <a name="create-a-purchase-order-with-a-delivery-schedule"></a><span data-ttu-id="f5798-103">Luo ostotilaus, jolla on toimitusaikataulu</span><span class="sxs-lookup"><span data-stu-id="f5798-103">Create a purchase order with a delivery schedule</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f5798-104">Tässä osoitetaan, miten ostotilaukselle luodaan toimitusaikataulu.</span><span class="sxs-lookup"><span data-stu-id="f5798-104">This procedure demonstrates how to create a delivery schedule for a purchase order.</span></span> <span data-ttu-id="f5798-105">Toimitusaikataulua käytetään, kun tilauksen tai kirjauskansion määrä pyydetään toimittamaan useissa lähetyksissä.</span><span class="sxs-lookup"><span data-stu-id="f5798-105">A delivery schedule is used when a quantity on an order or a journal is requested to be delivered in multiple shipments.</span></span> <span data-ttu-id="f5798-106">Tämän oppaan esimerkissä käytetään esittely-yritys USMF:n tietoja.</span><span class="sxs-lookup"><span data-stu-id="f5798-106">The example shown in this guide can be used in the USMF demo data company.</span></span> <span data-ttu-id="f5798-107">Tämä on yleensä ostoedustajan tehtävä.</span><span class="sxs-lookup"><span data-stu-id="f5798-107">This procedure would typically be done by a purchasing agent.</span></span>


## <a name="create-a-delivery-schedule"></a><span data-ttu-id="f5798-108">Toimitusaikataulun luominen</span><span class="sxs-lookup"><span data-stu-id="f5798-108">Create a delivery schedule</span></span>
1. <span data-ttu-id="f5798-109">Valitse Hankinta > Ostotilaukset > Kaikki ostotilaukset.</span><span class="sxs-lookup"><span data-stu-id="f5798-109">Go to Procurement and sourcing > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="f5798-110">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="f5798-110">Click New.</span></span>
3. <span data-ttu-id="f5798-111">Kirjoita Toimittajan tili -kenttään arvoksi US-101.</span><span class="sxs-lookup"><span data-stu-id="f5798-111">In the Vendor account field, enter US-101.</span></span>
4. <span data-ttu-id="f5798-112">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="f5798-112">Click OK.</span></span>
5. <span data-ttu-id="f5798-113">Kirjoita Nimiketunnus-kenttään arvo M0001.</span><span class="sxs-lookup"><span data-stu-id="f5798-113">In the Item number field, enter M0001.</span></span>
6. <span data-ttu-id="f5798-114">Kirjoita 10 Määrä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="f5798-114">In the Quantity field, enter 10.</span></span>
7. <span data-ttu-id="f5798-115">Valitse Ostotilausrivi.</span><span class="sxs-lookup"><span data-stu-id="f5798-115">Click Purchase order line.</span></span>
8. <span data-ttu-id="f5798-116">Valitse Toimitusaikataulu.</span><span class="sxs-lookup"><span data-stu-id="f5798-116">Click Delivery schedule.</span></span>
    * <span data-ttu-id="f5798-117">Toimitusaikataulu-sivulla voi määrittää toimittajalta saatavan tilausrivin kokonaismäärän lähetysten määrän.</span><span class="sxs-lookup"><span data-stu-id="f5798-117">The Delivery schedule page allows you to specify the number of shipments in which the total quantity of the order line will be delivered from the vendor.</span></span>  
    * <span data-ttu-id="f5798-118">Oletusarvon mukaan järjestelmä kopioi ensimmäiselle toimituksen aikatauluriville kokonaismäärän ja muita alkuperäisen ostorivin toimitustietoja.</span><span class="sxs-lookup"><span data-stu-id="f5798-118">By default, the system copies the total quantity and other delivery details of the original purchase line into the first delivery schedule line.</span></span> <span data-ttu-id="f5798-119">Tässä esimerkissä luodaan aikataulu kahdelle lähetykselle siten, että toisen lähetyksen päivämäärä poikkeaa viikolla ensimmäisestä lähetyspäivästä.</span><span class="sxs-lookup"><span data-stu-id="f5798-119">In this example, we’ll create a schedule for two shipments, with the second shipment’s date offset by a week from the first shipment.</span></span>  
9. <span data-ttu-id="f5798-120">Muuta Määrä-kentän arvoksi 4.</span><span class="sxs-lookup"><span data-stu-id="f5798-120">In the Quantity field, change the quantity to 4.</span></span>
10. <span data-ttu-id="f5798-121">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="f5798-121">Click New.</span></span>
11. <span data-ttu-id="f5798-122">Syötä jäljellä olevaksi määräksi 6 Määrä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="f5798-122">In the Quantity field, enter 6 as the remaining quantity.</span></span>
    * <span data-ttu-id="f5798-123">Valitse toimituspäivä-kenttään päivämäärä, joka on viikon ensimmäisen toimitusrivin päivämäärän jälkeen.</span><span class="sxs-lookup"><span data-stu-id="f5798-123">In the delivery date field, select a date that’s one week after the date on the first delivery line.</span></span>  
    * <span data-ttu-id="f5798-124">Voit seurata toimitusaikatauluriveille kohdistettua kokonaismäärää Summa- ja Jäljellä-kentän avulla.</span><span class="sxs-lookup"><span data-stu-id="f5798-124">You can keep track of the total quantity that’s allocated to the delivery schedule lines by looking at the Total and Remaining fields.</span></span> <span data-ttu-id="f5798-125">Kun jäljellä oleva summa on nolla, alkuperäisen rivin kokonaismäärä on kohdistettu aikatauluun.</span><span class="sxs-lookup"><span data-stu-id="f5798-125">When the remaining quantity is zero, the full quantity from the original line has been allocated to the schedule.</span></span>  
12. <span data-ttu-id="f5798-126">Laajenna Kulujen muunto -osa.</span><span class="sxs-lookup"><span data-stu-id="f5798-126">Expand the Charges conversion section.</span></span>
    * <span data-ttu-id="f5798-127">Vaihtoehtojen avulla voit määrittää, kuinka kulut jaetaan toimitusaikataulun rivien kesken.</span><span class="sxs-lookup"><span data-stu-id="f5798-127">The options here allow you to control how you want charges to be distributed across the delivery schedule lines.</span></span> <span data-ttu-id="f5798-128">Jos valitset Kopioi bruttosummat, jokaiselle riville kopioidaan alkuperäisen tilausrivin kulusumma.</span><span class="sxs-lookup"><span data-stu-id="f5798-128">If you select Copy gross amounts, the charge amount on the original order line is copied to each delivery line.</span></span> <span data-ttu-id="f5798-129">Kohdista toimitusriveille -vaihtoehto jakaa alkuperäisen rivin kulut kunkin toimitusrivin määrän mukaan.</span><span class="sxs-lookup"><span data-stu-id="f5798-129">The Allocate to delivery lines option divides the original line charge according to the quantity on each delivery line.</span></span>  
13. <span data-ttu-id="f5798-130">Tiivistä Kulujen muunto -osa.</span><span class="sxs-lookup"><span data-stu-id="f5798-130">Collapse the Charges conversion section.</span></span>
14. <span data-ttu-id="f5798-131">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="f5798-131">Click OK.</span></span>
    * <span data-ttu-id="f5798-132">Toimitusaikataulu on nyt otettu käyttöön tilauksessa.</span><span class="sxs-lookup"><span data-stu-id="f5798-132">The delivery schedule has now been applied to the order.</span></span>  
    * <span data-ttu-id="f5798-133">Alkuperäinen tilausrivi, jota sanotaan kaupalliseksi riviksi, on muunnettu tilausriviksi, jolla on useita toimituksia.</span><span class="sxs-lookup"><span data-stu-id="f5798-133">The original order line, now referred to as a Commercial line, has been converted to an Order line with multiple deliveries.</span></span> <span data-ttu-id="f5798-134">Se on merkitty erillisellä kuvakkeella ja toimii toimitusrivien otsikkona.</span><span class="sxs-lookup"><span data-stu-id="f5798-134">It is marked with a distinct icon and acts as a header for the delivery lines.</span></span>  
15. <span data-ttu-id="f5798-135">Valitse toinen tilausrivi, joka on ensimmäinen kahdesta toimitusrivistä.</span><span class="sxs-lookup"><span data-stu-id="f5798-135">Select the second order line, which is the first of the two delivery lines.</span></span>
    * <span data-ttu-id="f5798-136">Kaksi uutta riviä, joita sanotaan toimitusriveiksi, muodostavat toimitusaikataulun.</span><span class="sxs-lookup"><span data-stu-id="f5798-136">The two new lines, referred to as Delivery lines, make up one delivery schedule.</span></span> <span data-ttu-id="f5798-137">Tilaus käsitellään alkuperäisen rivin sijaan näiden rivien avulla.</span><span class="sxs-lookup"><span data-stu-id="f5798-137">The order will be processed against these lines and not the original line.</span></span> <span data-ttu-id="f5798-138">Jos tulostettuna on asiakirjoja, kuten myyntivahvistuksia, tuotteen vastaanottokirjauksia tai laskuja, vain toimitusrivit näytetään.</span><span class="sxs-lookup"><span data-stu-id="f5798-138">If documents such as confirmations, product receipt journals, or invoices are printed, only the delivery lines are shown.</span></span>  

## <a name="change-the-delivery-schedule"></a><span data-ttu-id="f5798-139">Muuta toimitusaikataulu</span><span class="sxs-lookup"><span data-stu-id="f5798-139">Change the delivery schedule</span></span>
    * <span data-ttu-id="f5798-140">Toimitusrivien määrää voi muuttaa.</span><span class="sxs-lookup"><span data-stu-id="f5798-140">You can change the quantity on delivery lines.</span></span> <span data-ttu-id="f5798-141">Jos muutat sitä, kaupallinen rivi päivitetään automaattisesi toimitusrivien kokonaismäärän mukaiseksi.</span><span class="sxs-lookup"><span data-stu-id="f5798-141">If you do this, the commercial line is automatically updated to the total quantity in the delivery lines.</span></span>  
1. <span data-ttu-id="f5798-142">Muuta ensimmäisen toimitusrivin Määrä-kentän arvoksi 4:n sijaan 5.</span><span class="sxs-lookup"><span data-stu-id="f5798-142">In the Quantity field of the first delivery line, change the quantity from 4 to 5.</span></span>
2. <span data-ttu-id="f5798-143">Valitse ensimmäinen tilausrivi (kaupallinen rivi).</span><span class="sxs-lookup"><span data-stu-id="f5798-143">Select the first order line (the commercial line).</span></span>
    * <span data-ttu-id="f5798-144">Kaupallisen rivin määräksi on muutettu 11.</span><span class="sxs-lookup"><span data-stu-id="f5798-144">The quantity on the commercial line has been changed to 11.</span></span>  

## <a name="process-product-receipt-using-delivery-schedules"></a><span data-ttu-id="f5798-145">Käsittele tuotteiden vastaanotto toimitusaikataulujen avulla</span><span class="sxs-lookup"><span data-stu-id="f5798-145">Process product receipt using delivery schedules</span></span>
    * <span data-ttu-id="f5798-146">Ostotilaus on vahvistettava ennen tuotteen vastaanoton käsittelyä.</span><span class="sxs-lookup"><span data-stu-id="f5798-146">The purchase order must be confirmed before product receipt can be processed.</span></span> <span data-ttu-id="f5798-147">Tässä esimerkissä vastaanotto kirjataan yleensä suoraan ostotilaukseen.</span><span class="sxs-lookup"><span data-stu-id="f5798-147">In this example, receipt is recorded directly on the purchase order.</span></span> <span data-ttu-id="f5798-148">Vastaanotto on myös voitu kirjata, kun tuotteet ovat saapuneet varastoon.</span><span class="sxs-lookup"><span data-stu-id="f5798-148">Receipt could also have been recorded when the goods arrived in the warehouse.</span></span>  
1. <span data-ttu-id="f5798-149">Valitse toimintoruudussa Osta.</span><span class="sxs-lookup"><span data-stu-id="f5798-149">On the Action Pane, click Purchase.</span></span>
2. <span data-ttu-id="f5798-150">Valitse Vahvista.</span><span class="sxs-lookup"><span data-stu-id="f5798-150">Click Confirm.</span></span>
3. <span data-ttu-id="f5798-151">Valitse toimintoruudussa Vastaanota.</span><span class="sxs-lookup"><span data-stu-id="f5798-151">On the Action Pane, click Receive.</span></span>
4. <span data-ttu-id="f5798-152">Valitse Tuotteen vastaanotto.</span><span class="sxs-lookup"><span data-stu-id="f5798-152">Click Product receipt.</span></span>
5. <span data-ttu-id="f5798-153">Kirjoita mikä tahansa arvo Tuotteen vastaanotto -kenttään.</span><span class="sxs-lookup"><span data-stu-id="f5798-153">In the Product receipt field, type any value.</span></span>
    * <span data-ttu-id="f5798-154">Tätä kenttää käytetään syöttämään viite, jota käytetään tositteena tuotteen vastaanoton kirjauskansiossa.</span><span class="sxs-lookup"><span data-stu-id="f5798-154">This field is used to enter a reference that will be used as voucher for the product receipt journal.</span></span>  
    * <span data-ttu-id="f5798-155">Valitse Määrä-kentässä "Tilattu määrä".</span><span class="sxs-lookup"><span data-stu-id="f5798-155">In the Quantity field, select ‘Ordered quantity’.</span></span> <span data-ttu-id="f5798-156">Tämä vaihtoehto tarkoittaa, että vastaanotto käsitellään sen määrän mukaiseksi, jolla tilausrivit on luotu.</span><span class="sxs-lookup"><span data-stu-id="f5798-156">This option means that receipt will process for the quantity that the order lines were created with.</span></span>  
    * <span data-ttu-id="f5798-157">Varmista, että Tulosta tuotteen vastaanotto -kentän arvo on Ei.</span><span class="sxs-lookup"><span data-stu-id="f5798-157">Make sure that the Print product receipt field is set to No.</span></span> <span data-ttu-id="f5798-158">Tässä esimerkissä ei tarvita tulostamista.</span><span class="sxs-lookup"><span data-stu-id="f5798-158">Printing isn’t needed in this example.</span></span>  
6. <span data-ttu-id="f5798-159">Laajenna Rivit-osa.</span><span class="sxs-lookup"><span data-stu-id="f5798-159">Expand the Lines section.</span></span>
    * <span data-ttu-id="f5798-160">Huomaa, miten tuotteen vastaanotto luodaan toimitusriveille alkuperäisen tilausrivin sijaan.</span><span class="sxs-lookup"><span data-stu-id="f5798-160">Notice how the product receipt is created for the two delivery lines and not the original order line.</span></span> <span data-ttu-id="f5798-161">Jos vastaanotto olisi kirjattu varastossa, se olisi myös kirjattu toimitusaikataulun riveille.</span><span class="sxs-lookup"><span data-stu-id="f5798-161">If receipt had been recorded in the warehouse, it would also have been recorded on the delivery schedule lines.</span></span>  
7. <span data-ttu-id="f5798-162">Tiivistä Rivit-osa.</span><span class="sxs-lookup"><span data-stu-id="f5798-162">Collapse the Lines section.</span></span>
8. <span data-ttu-id="f5798-163">Kirjaa vastaanotto valitsemalla OK.</span><span class="sxs-lookup"><span data-stu-id="f5798-163">Click OK to post the receipt.</span></span>


