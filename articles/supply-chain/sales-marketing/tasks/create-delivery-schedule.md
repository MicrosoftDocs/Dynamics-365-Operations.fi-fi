---
title: Toimitusaikataulun luominen
description: Tässä osoitetaan, miten myyntitilaukselle luodaan toimitusaikataulu.
author: omulvad
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, SalesDeliverySchedule, SalesEditLines,  SrsReportViewerForm
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d99dfae5e045262d34daf3529a6a3f4716b4afe3
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/15/2019
ms.locfileid: "1563864"
---
# <a name="create-delivery-schedule"></a><span data-ttu-id="25dbd-103">Toimitusaikataulun luominen</span><span class="sxs-lookup"><span data-stu-id="25dbd-103">Create delivery schedule</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="25dbd-104">Tässä osoitetaan, miten myyntitilaukselle luodaan toimitusaikataulu.</span><span class="sxs-lookup"><span data-stu-id="25dbd-104">This procedure demonstrates how to create a delivery schedule for a sales order.</span></span> <span data-ttu-id="25dbd-105">Toimitusaikataulua käytetään, kun tilauksen määrä tai tarjous pyydetään toimittamaan useissa lähetyksissä.</span><span class="sxs-lookup"><span data-stu-id="25dbd-105">A delivery schedule is used when a quantity on an order or a quotation is requested to be delivered in multiple shipments.</span></span> <span data-ttu-id="25dbd-106">Voit suorittaa tämän menettelyn esittely-yrityksen USMF kanssa tai käyttää omia tietojasi.</span><span class="sxs-lookup"><span data-stu-id="25dbd-106">You can run this procedure in demo data company USMF or on your own data.</span></span>


## <a name="create-delivery-schedule"></a><span data-ttu-id="25dbd-107">Toimitusaikataulun luominen</span><span class="sxs-lookup"><span data-stu-id="25dbd-107">Create delivery schedule</span></span>
1. <span data-ttu-id="25dbd-108">Siirry Kaikki myyntitilaukset -kohtaan.</span><span class="sxs-lookup"><span data-stu-id="25dbd-108">Go to All sales orders.</span></span>
2. <span data-ttu-id="25dbd-109">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="25dbd-109">Click New.</span></span>
3. <span data-ttu-id="25dbd-110">Syötä tai valitse arvo Asiakastili-kentässä.</span><span class="sxs-lookup"><span data-stu-id="25dbd-110">In the Customer account field, enter or select a value.</span></span>
4. <span data-ttu-id="25dbd-111">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="25dbd-111">Click OK.</span></span>
5. <span data-ttu-id="25dbd-112">Syötä tai valitse arvo Nimiketunnus-kentässä.</span><span class="sxs-lookup"><span data-stu-id="25dbd-112">In the Item number field, enter or select a value.</span></span>
6. <span data-ttu-id="25dbd-113">Syötä Määrä-kenttään lukua 1 suurempi arvo.</span><span class="sxs-lookup"><span data-stu-id="25dbd-113">In the Quantity field, enter a number that is bigger than 1.</span></span>
7. <span data-ttu-id="25dbd-114">Valitse myyntitilausrivi.</span><span class="sxs-lookup"><span data-stu-id="25dbd-114">Click Sales order line.</span></span>
8. <span data-ttu-id="25dbd-115">Valitse Toimitusaikataulu.</span><span class="sxs-lookup"><span data-stu-id="25dbd-115">Click Delivery schedule.</span></span>
    * <span data-ttu-id="25dbd-116">Toimitusaikataulu-sivulla voi määrittää asiakkaalle toimitettavan tilausrivin kokonaismäärän lähetysten määrän.</span><span class="sxs-lookup"><span data-stu-id="25dbd-116">The Delivery schedule page is the place where you can specify the number of shipments in which the total quantity of the order line will be delivered to the customer.</span></span>    
    * <span data-ttu-id="25dbd-117">Oletusarvoisesti järjestelmä kopioi alkuperäisen myyntirivin kokonaismäärän ja muut toimitustiedot ensimmäiselle toimitusaikatauluriville.</span><span class="sxs-lookup"><span data-stu-id="25dbd-117">By default, the system copies the total quantity and other delivery details of the original sales line into the first delivery schedule line.</span></span> <span data-ttu-id="25dbd-118">Tässä esimerkissä luodaan kaksi lähetystä sisältävä aikataulu. Toisen lähetyksen päivämäärä on viikon kuluttua ensimmäisen lähetyksen päivämäärästä.</span><span class="sxs-lookup"><span data-stu-id="25dbd-118">In this example, we’ll create a schedule for two shipments, with the second shipment's date offset by a week from the first one.</span></span>  
9. <span data-ttu-id="25dbd-119">Syötä Määrä-kenttään luku, joka on osa kokonaismäärää.</span><span class="sxs-lookup"><span data-stu-id="25dbd-119">In the Quantity field, enter a number that is part of the total quantity.</span></span>
10. <span data-ttu-id="25dbd-120">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="25dbd-120">Click New.</span></span>
11. <span data-ttu-id="25dbd-121">Syötä jäljellä oleva määrä Määrä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="25dbd-121">In the Quantity field, enter the remaining quantity.</span></span>
12. <span data-ttu-id="25dbd-122">Syötä Pyydetty lähetyspäivämäärä -kenttään päivämäärä, joka on viikon kuluttua ensimmäisen toimitusrivin päivämäärästä.</span><span class="sxs-lookup"><span data-stu-id="25dbd-122">In the Requested ship date field, enter a date a date that is one week ahead from the date of the first delivery line.</span></span>
    * <span data-ttu-id="25dbd-123">Kulujen muunto -pikavälilehden kaksi vaihtoehtoa ohjaavat sitä, miten kulut jaetaan toimitusaikatauluriveille sen jälkeen, kun ne on liitetty alkuperäiseen tilausriviin.</span><span class="sxs-lookup"><span data-stu-id="25dbd-123">The two options on the Charges conversion FastTab control how you want the charges to be distributed across the delivery schedule lines, once they’ve been assigned to the original order line.</span></span> <span data-ttu-id="25dbd-124">Jos valitset Kopioi bruttosummat, jokaiselle riville kopioidaan sama kulusumma.</span><span class="sxs-lookup"><span data-stu-id="25dbd-124">If you select Copy gross amounts, the same charge amount is copied to each line.</span></span> <span data-ttu-id="25dbd-125">Kohdista toimitusriveille -vaihtoehto jakaa kulun tasaisesti kaikille toimitusriveille.</span><span class="sxs-lookup"><span data-stu-id="25dbd-125">The Allocate to delivery lines option divides the charge equally across the delivery lines.</span></span>  
    * <span data-ttu-id="25dbd-126">Vain kiinteät kulut voidaan jakaa. Muuttuvat kulut kopioidaan yhä riveille.</span><span class="sxs-lookup"><span data-stu-id="25dbd-126">Only fixed charges can be divided, whereas variable charges will still be copied to the lines.</span></span>  
13. <span data-ttu-id="25dbd-127">Siirrä kohdistin pois toiselta toimitusriviltä, jolloin sivu päivittyy.</span><span class="sxs-lookup"><span data-stu-id="25dbd-127">Move the cursor away from the second delivery line to update the page.</span></span>
    * <span data-ttu-id="25dbd-128">Voit seurata toimitusaikatauluriveille kohdistettua kokonaismäärää Summa- ja Jäljellä-kentän avulla.</span><span class="sxs-lookup"><span data-stu-id="25dbd-128">You can keep track of the total quantity that’s allocated to the delivery schedule lines by looking at the Total and Remaining fields.</span></span> <span data-ttu-id="25dbd-129">Kun jäljellä oleva summa on nolla, alkuperäisen rivin kokonaismäärä on kohdistettu aikatauluun.</span><span class="sxs-lookup"><span data-stu-id="25dbd-129">When the remaining quantity is zero, the full quantity from the original line has been allocated to the schedule.</span></span>   
14. <span data-ttu-id="25dbd-130">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="25dbd-130">Click OK.</span></span>
    * <span data-ttu-id="25dbd-131">Toimitusaikataulu on nyt kopioitu tilausriveille.</span><span class="sxs-lookup"><span data-stu-id="25dbd-131">The delivery schedule has now been copied to the order lines.</span></span>   
    * <span data-ttu-id="25dbd-132">Alkuperäinen tilausrivi, jota sanotaan kaupalliseksi riviksi, on muunnettu tilausriviksi, jolla on useita toimituksia.</span><span class="sxs-lookup"><span data-stu-id="25dbd-132">The original order line, referred to as a Commercial line, has been converted to an Order line with multiple deliveries.</span></span> <span data-ttu-id="25dbd-133">Se merkitään erillisellä kuvakkeella ja toimii toimitusrivien otsikkona.</span><span class="sxs-lookup"><span data-stu-id="25dbd-133">It is marked with a distinct icon and acts as a header for the delivery lines.</span></span>  
    * <span data-ttu-id="25dbd-134">Kaksi uutta riviä, joita sanotaan toimitusriveiksi, muodostavat toimitusaikataulun.</span><span class="sxs-lookup"><span data-stu-id="25dbd-134">The two new lines, referred to as delivery lines, make up one delivery schedule.</span></span> <span data-ttu-id="25dbd-135">Tilaus käsitellään alkuperäisen rivin sijaan näiden rivien avulla.</span><span class="sxs-lookup"><span data-stu-id="25dbd-135">The order will be processed against these lines and not the original line.</span></span> <span data-ttu-id="25dbd-136">Jos tulostettuna on asiakirjoja, kuten vahvistus-, keräys- tai pakkausluettelot, vain toimitusrivit näytetään.</span><span class="sxs-lookup"><span data-stu-id="25dbd-136">If documents such as confirmation slips, picking lists, packing slips, or invoices are printed, only the delivery lines are shown.</span></span>   
    * <span data-ttu-id="25dbd-137">Toimitusriveillä on eri toimituspäiviä, määriä, toimitustapoja ja varastodimensioita, kuten toimipaikka ja varasto.</span><span class="sxs-lookup"><span data-stu-id="25dbd-137">The delivery lines can have different delivery dates, quantities, modes of delivery, and storage dimensions, such as site and warehouse.</span></span> <span data-ttu-id="25dbd-138">Tuotedimensioiden on kuitenkin aina vastattava kaupallisen rivin arvoja. Niitä ei voi muuttaa.</span><span class="sxs-lookup"><span data-stu-id="25dbd-138">However, the product dimensions must always match the ones on the commercial line and can't be changed.</span></span>  
15. <span data-ttu-id="25dbd-139">Syötä Määrä-kenttään nykyistä lukua suurempi arvo.</span><span class="sxs-lookup"><span data-stu-id="25dbd-139">In the Quantity field, enter a number that's bigger than the current one.</span></span>
16. <span data-ttu-id="25dbd-140">Valitse kaupallinen rivi, kun haluat nähdä tilanteen määrän uudelleenlaskemisen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="25dbd-140">Select the commercial line to see the effect of the quantity recalculation.</span></span>
17. <span data-ttu-id="25dbd-141">Valitse toimintoruudussa Kerää ja pakkaa.</span><span class="sxs-lookup"><span data-stu-id="25dbd-141">On the Action Pane, click Pick and pack.</span></span>
18. <span data-ttu-id="25dbd-142">Valitse Kirjaa pakkausluettelo.</span><span class="sxs-lookup"><span data-stu-id="25dbd-142">Click Post packing slip.</span></span>
19. <span data-ttu-id="25dbd-143">Laajenna Parametrit-osa.</span><span class="sxs-lookup"><span data-stu-id="25dbd-143">Expand the Parameters section.</span></span>
20. <span data-ttu-id="25dbd-144">Valitse Määrä-kentässä Kaikki.</span><span class="sxs-lookup"><span data-stu-id="25dbd-144">In the Quantity field, select 'All'.</span></span>
    * <span data-ttu-id="25dbd-145">Huomaa, että pakkausluettelo luodaan kahdelle toimitusaikatauluriville, ei alkuperäiselle tilausriville.</span><span class="sxs-lookup"><span data-stu-id="25dbd-145">Note that the packing slip will be created for the two delivery schedule lines and not the original order line.</span></span>  
21. <span data-ttu-id="25dbd-146">Valitse Tulosta pakkausluettelo -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="25dbd-146">Select Yes in the Print packing slip field.</span></span>
22. <span data-ttu-id="25dbd-147">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="25dbd-147">Click OK.</span></span>
23. <span data-ttu-id="25dbd-148">Valitse Kyllä.</span><span class="sxs-lookup"><span data-stu-id="25dbd-148">Click Yes.</span></span>
24. <span data-ttu-id="25dbd-149">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="25dbd-149">Close the page.</span></span>

