---
title: Hyväksy toimittajia tietyille tuotteille
description: Tässä menettelyssä kuvataan, miten voit hyväksyä toimittajia tietyille tuotteille.
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, PdsApprovedVendorList, VendTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8f2cd1badb0b924150ab51ef2efc049e6666562a
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/15/2019
ms.locfileid: "1559206"
---
# <a name="approve-vendors-for-specific-products"></a><span data-ttu-id="f2d98-103">Hyväksy toimittajia tietyille tuotteille</span><span class="sxs-lookup"><span data-stu-id="f2d98-103">Approve vendors for specific products</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f2d98-104">Tässä menettelyssä kuvataan, miten voit hyväksyä toimittajia tietyille tuotteille.</span><span class="sxs-lookup"><span data-stu-id="f2d98-104">This procedure shows you how to approve vendors for specific products.</span></span> <span data-ttu-id="f2d98-105">Tämän avulla voit määrittää, mitä toimittajia voidaan käyttää, kun tuote lisätään ostotilaukseen.</span><span class="sxs-lookup"><span data-stu-id="f2d98-105">This allows you to control which vendors can be used when the product is added to a purchase order.</span></span> <span data-ttu-id="f2d98-106">Voit käyttää tätä menettelyä emotietojen yrityksen USMF kanssa tai käyttää omia tietojasi.</span><span class="sxs-lookup"><span data-stu-id="f2d98-106">You can use this procedure in demo data company USMF, or on your own data.</span></span> <span data-ttu-id="f2d98-107">Yleensä ostopäällikkö tekee tämän tehtävän.</span><span class="sxs-lookup"><span data-stu-id="f2d98-107">This task would typically be carried out by a Purchasing manager.</span></span>

1. <span data-ttu-id="f2d98-108">Mene Tuotetietojen hallinta > Tuotteet > Vapautetut tuotteet.</span><span class="sxs-lookup"><span data-stu-id="f2d98-108">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="f2d98-109">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="f2d98-109">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="f2d98-110">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="f2d98-110">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="f2d98-111">Laajenna Ostot-osa.</span><span class="sxs-lookup"><span data-stu-id="f2d98-111">Expand the Purchase section.</span></span>
    * <span data-ttu-id="f2d98-112">Jos toimittajan kentässä näytetään ensisijainen toimittaja, sinun on lisättävä tämä toimittaja hyväksyttyjen toimittajien luettelon noudattamalla seuraavia vaiheita.</span><span class="sxs-lookup"><span data-stu-id="f2d98-112">If there is a primary vendor shown in the Vendor field, then you need to add this vendor as an approved vendor in the following steps.</span></span> <span data-ttu-id="f2d98-113">Ota muistiin toimittajanumero, jos sellainen näytetään.</span><span class="sxs-lookup"><span data-stu-id="f2d98-113">Make a note of the vendor number, if one is shown.</span></span>  
5. <span data-ttu-id="f2d98-114">Valitse toimintoruudussa Osta.</span><span class="sxs-lookup"><span data-stu-id="f2d98-114">On the Action Pane, click Purchase.</span></span>
6. <span data-ttu-id="f2d98-115">Valitse Asetukset.</span><span class="sxs-lookup"><span data-stu-id="f2d98-115">Click Setup.</span></span>
7. <span data-ttu-id="f2d98-116">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="f2d98-116">Click Add.</span></span>
8. <span data-ttu-id="f2d98-117">Syötä tai valitse Toimittaja-kentän arvo.</span><span class="sxs-lookup"><span data-stu-id="f2d98-117">In the Vendor field, enter or select a value.</span></span>
    * <span data-ttu-id="f2d98-118">Valitse hyväksytty toimittaja.</span><span class="sxs-lookup"><span data-stu-id="f2d98-118">Select the approved vendor.</span></span> <span data-ttu-id="f2d98-119">Vähintään yhden rivin tulee olla ensisijainen toimittaja, jos sellainen on tuotetietueessa.</span><span class="sxs-lookup"><span data-stu-id="f2d98-119">At least one of the lines has to be the primary vendor if there was one in the product record.</span></span> <span data-ttu-id="f2d98-120">Jos olet pannut muistiin toimittajanumeron aiemmin, valitse se tässä.</span><span class="sxs-lookup"><span data-stu-id="f2d98-120">If you made a note of the vendor number earlier, select it here.</span></span>  
9. <span data-ttu-id="f2d98-121">Syötä päivämäärä Päättyminen-kenttään.</span><span class="sxs-lookup"><span data-stu-id="f2d98-121">In the Expiration field, enter a date.</span></span>
    * <span data-ttu-id="f2d98-122">Valitse päivämäärä, joka on muutaman kuukauden päässä.</span><span class="sxs-lookup"><span data-stu-id="f2d98-122">Choose a date a that is a few months ahead.</span></span>  
10. <span data-ttu-id="f2d98-123">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="f2d98-123">Click Add.</span></span>
11. <span data-ttu-id="f2d98-124">Syötä tai valitse Toimittaja-kentän arvo.</span><span class="sxs-lookup"><span data-stu-id="f2d98-124">In the Vendor field, enter or select a value.</span></span>
12. <span data-ttu-id="f2d98-125">Syötä päivämäärä Päättyminen-kenttään.</span><span class="sxs-lookup"><span data-stu-id="f2d98-125">In the Expiration field, enter a date.</span></span>
    * <span data-ttu-id="f2d98-126">Valitse päivämäärä, joka ei ole sama, kuin edellinen erääntymispäivämäärä.</span><span class="sxs-lookup"><span data-stu-id="f2d98-126">Choose a date that is different than the previous expiration date.</span></span>  
13. <span data-ttu-id="f2d98-127">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="f2d98-127">Close the page.</span></span>
14. <span data-ttu-id="f2d98-128">Napsauta Hyväksytyt toimittajat -kohtaa.</span><span class="sxs-lookup"><span data-stu-id="f2d98-128">Click Approved vendors.</span></span>
15. <span data-ttu-id="f2d98-129">Syötä päivämäärä Päättyminen-kenttään.</span><span class="sxs-lookup"><span data-stu-id="f2d98-129">In the Expiration field, enter a date.</span></span>
    * <span data-ttu-id="f2d98-130">Tämä päivämäärä toimii suodattimena, jonka avulla voit tarkastella hyväksyttyjä toimittajia tiettyyn päivämäärään saakka.</span><span class="sxs-lookup"><span data-stu-id="f2d98-130">This date acts as a filter so you can see who the approved vendors are, up to a certain date.</span></span>  
16. <span data-ttu-id="f2d98-131">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="f2d98-131">Close the page.</span></span>
17. <span data-ttu-id="f2d98-132">Napsauta Voimassaoloaika-kohtaa.</span><span class="sxs-lookup"><span data-stu-id="f2d98-132">Click Effective period.</span></span>
18. <span data-ttu-id="f2d98-133">Anna päivämäärä Näytä vanhentuneet toimittajat -kenttään.</span><span class="sxs-lookup"><span data-stu-id="f2d98-133">In the Show vendors expired by field, enter a date.</span></span>
    * <span data-ttu-id="f2d98-134">Tämän sivun avulla voit tunnistaa toimittajat, joiden hyväksymistilaa päättyy tietyn päivämäärän jälkeen.</span><span class="sxs-lookup"><span data-stu-id="f2d98-134">You can use this page to identify vendors where the approval status will expire after a certain date.</span></span>  
19. <span data-ttu-id="f2d98-135">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="f2d98-135">Close the page.</span></span>
20. <span data-ttu-id="f2d98-136">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="f2d98-136">Click Edit.</span></span>
21. <span data-ttu-id="f2d98-137">Valitse vaihtoehto Hyväksytyn toimittajan tarkistusmenetelmä ‑kentästä.</span><span class="sxs-lookup"><span data-stu-id="f2d98-137">In the Approved vendor check method field, select an option.</span></span>
    * <span data-ttu-id="f2d98-138">Tässä kentässä voit valita käytännön sille, mitä tapahtuu, jos tuote lisätään ostotilauksen riville, jonka toimittaja ei ole hyväksytty toimittaja.</span><span class="sxs-lookup"><span data-stu-id="f2d98-138">This field allows you to select the policy for what should happen if the product is added to a purchase order line where the vendor is not an approved vendor.</span></span>  
22. <span data-ttu-id="f2d98-139">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="f2d98-139">Click Save.</span></span>
23. <span data-ttu-id="f2d98-140">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="f2d98-140">Close the page.</span></span>
24. <span data-ttu-id="f2d98-141">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="f2d98-141">Close the page.</span></span>
25. <span data-ttu-id="f2d98-142">Valitse Hankinta > Toimittajat > Toimittaja-nimike-suhteet > Hyväksyttyjen toimittajien luettelo nimikkeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="f2d98-142">Go to Procurement and sourcing > Vendors > Vendor/item relations > Approved vendor list by item.</span></span>
    * <span data-ttu-id="f2d98-143">Tällä sivulla on yhteenveto kaikista tuotteista ja hyväksytyistä toimittajista.</span><span class="sxs-lookup"><span data-stu-id="f2d98-143">This page gives you an overview of all products and the approved vendors.</span></span>  
26. <span data-ttu-id="f2d98-144">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="f2d98-144">Close the page.</span></span>
27. <span data-ttu-id="f2d98-145">Valitse Hankinta > Toimittajat > Kaikki toimittajat.</span><span class="sxs-lookup"><span data-stu-id="f2d98-145">Go to Procurement and sourcing > Vendors > All vendors.</span></span>
    * <span data-ttu-id="f2d98-146">Voit myös aloittaa toimittajasta ja siirtyä kyseiselle toimittajan tilille hyväksyttyjen tuotteiden luetteloon.</span><span class="sxs-lookup"><span data-stu-id="f2d98-146">You can also start from a vendor and then go to the list of approved products for that vendor account.</span></span>  
28. <span data-ttu-id="f2d98-147">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="f2d98-147">In the list, find and select the desired record.</span></span>
29. <span data-ttu-id="f2d98-148">Valitse toimintoruudussa Hankinta.</span><span class="sxs-lookup"><span data-stu-id="f2d98-148">On the Action Pane, click Procurement.</span></span>
30. <span data-ttu-id="f2d98-149">Napsauta Hyväksyttyjen toimittajien luettelo toimittajien mukaan -kohtaa.</span><span class="sxs-lookup"><span data-stu-id="f2d98-149">Click Approved vendor list by vendor.</span></span>
31. <span data-ttu-id="f2d98-150">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="f2d98-150">Close the page.</span></span>
32. <span data-ttu-id="f2d98-151">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="f2d98-151">Close the page.</span></span>

