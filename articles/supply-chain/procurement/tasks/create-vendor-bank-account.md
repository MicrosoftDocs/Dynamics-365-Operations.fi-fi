---
title: Luo toimittajan pankkitili
description: Tässä menettelyssä näytetään, miten luodaan toimittajalle pankkitili.
author: RichardLuan
manager: tfehr
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, VendBankAccounts, LogisticsPostalAddressSingle
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 425cce178c96097c8aa0a28345d4a9094b7970d9
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5262186"
---
# <a name="create-a-vendor-bank-account"></a><span data-ttu-id="46775-103">Luo toimittajan pankkitili</span><span class="sxs-lookup"><span data-stu-id="46775-103">Create a vendor bank account</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="46775-104">Tässä menettelyssä näytetään, miten luodaan toimittajalle pankkitili.</span><span class="sxs-lookup"><span data-stu-id="46775-104">This procedure shows you how to create a bank account for a vendor.</span></span> <span data-ttu-id="46775-105">Voit käyttää tätä menettelyä esittely-yrityksessä USMF.</span><span class="sxs-lookup"><span data-stu-id="46775-105">You can use this procedure in demo data company USMF.</span></span>

1. <span data-ttu-id="46775-106">Siirry kohtaan **siirtymisruutu > Moduulit > Hankinta > Toimittajat > Kaikki toimittajat**.</span><span class="sxs-lookup"><span data-stu-id="46775-106">Go to **Navigation pane > Modules > Procurement and sourcing > Vendors > All vendors**.</span></span>
2. <span data-ttu-id="46775-107">Valitse toimittaja, jolle haluat luoda pankkitilin ja napsauta sitten **Toimittajan tilitunnus** -kentän linkkiä.</span><span class="sxs-lookup"><span data-stu-id="46775-107">Select the vendor that you want to create a bank account for, and then click the link on the **Vendor account ID** field.</span></span>
3. <span data-ttu-id="46775-108">Valitse **toimintoruudussa** **Toimittaja**.</span><span class="sxs-lookup"><span data-stu-id="46775-108">On the **Action Pane**, click **Vendor**.</span></span>
4. <span data-ttu-id="46775-109">Valitse **Pankkitilit**.</span><span class="sxs-lookup"><span data-stu-id="46775-109">Click **Bank accounts**.</span></span>
5. <span data-ttu-id="46775-110">Napsauta **Toimintoruudussa** **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="46775-110">On the **Action Pane**, click **New**.</span></span>
6. <span data-ttu-id="46775-111">Kirjoita arvo **Pankkitili**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="46775-111">In the **Bank account** field, type a value.</span></span> <span data-ttu-id="46775-112">Tätä tunnusta käytetään toimittajatietueen pankkitilin yksilöimiseen.</span><span class="sxs-lookup"><span data-stu-id="46775-112">This ID will be used to identify the bank account on the vendor record.</span></span>  
7. <span data-ttu-id="46775-113">Kirjoita arvo **Nimi**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="46775-113">In the **Name** field, type a value.</span></span>
8. <span data-ttu-id="46775-114">Syötä tai valitse arvo **Pankkiryhmät**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="46775-114">In the **Bank groups** field, enter or select a value.</span></span>
9. <span data-ttu-id="46775-115">Valitse **Pankkikoodin tyyppi** -kenttään vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="46775-115">In the **Routing number type** field, select an option.</span></span> <span data-ttu-id="46775-116">Tämä on kansainvälisten tilisiirtojen pankkikoodityyppi.</span><span class="sxs-lookup"><span data-stu-id="46775-116">This is the type of routing number that's used for international payments.</span></span>  
10. <span data-ttu-id="46775-117">Kirjoita arvo **Pankkitilin numero** -kenttään.</span><span class="sxs-lookup"><span data-stu-id="46775-117">In the **Bank account number** field, type a value.</span></span>
11. <span data-ttu-id="46775-118">Syötä arvo **SWIFT-koodi**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="46775-118">In the **SWIFT code** field, type a value.</span></span>
12. <span data-ttu-id="46775-119">Syötä arvon **IBAN**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="46775-119">In the **IBAN** field, type a value.</span></span>
    - <span data-ttu-id="46775-120">IBAN-tilinumeron on oltava oikeassa muodossa.</span><span class="sxs-lookup"><span data-stu-id="46775-120">The IBAN number must be in the correct format.</span></span> <span data-ttu-id="46775-121">Voit esimerkiksi käyttää tilinumeroa DE89370400440532013000.</span><span class="sxs-lookup"><span data-stu-id="46775-121">For example, you could use DE89370400440532013000.</span></span>  
    - <span data-ttu-id="46775-122">Pankkitilin tila on Aktiivinen, jos aktivointipäivämäärä on ohitettu, mutta vanhentumispäivää ei ole ohitettu.</span><span class="sxs-lookup"><span data-stu-id="46775-122">The status of the bank account is Active if the Active date has been reached, and the Expiration date has not been exceeded.</span></span> <span data-ttu-id="46775-123">Se on aktiivinen myös, jos aktivointi- ja vanhentumispäiväkentät ovat tyhjiä.</span><span class="sxs-lookup"><span data-stu-id="46775-123">It's also active if both the Active date and Expiration date fields are blank.</span></span> <span data-ttu-id="46775-124">Jos sekä aktivointi- että vanhentumispäiväkentän päivämäärät ovat tulevia, sähköiset maksut eivät ole käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="46775-124">If the dates in both the Active date and Expiration date fields are in the future electronic payments are not available.</span></span> <span data-ttu-id="46775-125">Muut maksutyypit ovat käytettävissä, ja pankkitili on aktiivinen.</span><span class="sxs-lookup"><span data-stu-id="46775-125">Other payment types are available and the bank account is active.</span></span>  
13. <span data-ttu-id="46775-126">Laajenna osa **Asetukset**.</span><span class="sxs-lookup"><span data-stu-id="46775-126">Expand the **Setup** section.</span></span>
14. <span data-ttu-id="46775-127">Syötä arvo **Tekstikoodi**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="46775-127">In the **Text code** field, type a value.</span></span> <span data-ttu-id="46775-128">Tämä kenttä määrittää koodin, joka näytetään vastaanottajan tiliotteella.</span><span class="sxs-lookup"><span data-stu-id="46775-128">This field specifies a code that will appear on the bank statement of the recipient.</span></span>  
15. <span data-ttu-id="46775-129">Kirjoita arvo **Sanoma pankille** -kenttään.</span><span class="sxs-lookup"><span data-stu-id="46775-129">In the **Message to bank** field, type a value.</span></span>
16. <span data-ttu-id="46775-130">Kirjoita arvo **Vaihtokurssin viite** -kenttään.</span><span class="sxs-lookup"><span data-stu-id="46775-130">In the **Exchange reference** field, type a value.</span></span> <span data-ttu-id="46775-131">Tämä on muuttuvan tai kiinteän vaihtokurssin viitenumero.</span><span class="sxs-lookup"><span data-stu-id="46775-131">This is the reference number for any forward-term or fixed-term rate of exchange.</span></span>
17. <span data-ttu-id="46775-132">Anna tai valitse **Valuutta**-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="46775-132">In the **Currency** field, enter or select a value.</span></span> <span data-ttu-id="46775-133">Jos esilaskujen luonti on käytössä, tässä osassa on katsaus niiden tilaan (odottava tai hyväksytty).</span><span class="sxs-lookup"><span data-stu-id="46775-133">When prenotes are issued, this section provides an overview of their status (pending or approved).</span></span>  
18. <span data-ttu-id="46775-134">Laajenna **Osoite**-osa.</span><span class="sxs-lookup"><span data-stu-id="46775-134">Expand the **Address** section.</span></span>
19. <span data-ttu-id="46775-135">Laajenna **Esilaskut**-osa.</span><span class="sxs-lookup"><span data-stu-id="46775-135">Expand the **Prenotes** section.</span></span>
20. <span data-ttu-id="46775-136">Laajenna **Yhteystiedot**-osa.</span><span class="sxs-lookup"><span data-stu-id="46775-136">Expand the **Contact information** section.</span></span>
21. <span data-ttu-id="46775-137">Kirjoita arvo **Puhelin**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="46775-137">In the **Telephone** field, type a value.</span></span>
22. <span data-ttu-id="46775-138">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="46775-138">Close the page.</span></span>
23. <span data-ttu-id="46775-139">Valitse **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="46775-139">Click **Edit**.</span></span>
24. <span data-ttu-id="46775-140">Laajenna **Maksu**-osa.</span><span class="sxs-lookup"><span data-stu-id="46775-140">Expand the **Payment** section.</span></span>
25. <span data-ttu-id="46775-141">Valitse juuri luomasi tili **Pankkitili**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="46775-141">In the **Bank account** field, select the account that you've just created.</span></span>
26. <span data-ttu-id="46775-142">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="46775-142">Click **Save**.</span></span> <span data-ttu-id="46775-143">Osoite voi periytyä pankkiryhmästä, jos sellainen on määritelty, tai sen voi lisätä tässä.</span><span class="sxs-lookup"><span data-stu-id="46775-143">The address may be inherited from the bank group, if one is specified, or you can add it here.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]