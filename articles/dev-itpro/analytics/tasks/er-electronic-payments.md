---
title: ER Luo sähköisiä maksuasiakirjoja muotokokoonpanon avulla
description: Seuraavissa vaiheissa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän roolin omaava käyttäjä voi käyttää uutta sähköisen raportoinnin (ER) muotokonfiguraatiota maksukäsittelyn sähköisten asiakirjojen luomiseen.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendPaymMode, LedgerJournalTable, LedgerJournalTransVendPaym, BankAccountTableLookUp
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cf2ae8fb451eba1054bb94edbce009dcfa8c872c
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/15/2019
ms.locfileid: "1551365"
---
# <a name="er-generate-electronic-documents-for-payments-using-a-format-configuration"></a><span data-ttu-id="8d917-103">ER Luo sähköisiä maksuasiakirjoja muotokokoonpanon avulla</span><span class="sxs-lookup"><span data-stu-id="8d917-103">ER Generate electronic documents for payments using a format configuration</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8d917-104">Seuraavissa vaiheissa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän roolin omaava käyttäjä voi käyttää uutta sähköisen raportoinnin (ER) muotokonfiguraatiota maksukäsittelyn sähköisten asiakirjojen luomiseen.</span><span class="sxs-lookup"><span data-stu-id="8d917-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can use a new Electronic reporting (ER) format configuration to generate electronic documents for processing payments.</span></span> <span data-ttu-id="8d917-105">Nämä vaiheet voidaan suorittaa GBSI-esimerkkiyrityksessä.</span><span class="sxs-lookup"><span data-stu-id="8d917-105">These steps can be performed in the GBSI sample company.</span></span>

<span data-ttu-id="8d917-106">Konfiguraation luominen, joka sisältää maksuasiakirjan muodon -menettelyn vaiheet on suoritettava ennen näiden vaiheiden suorittamista.</span><span class="sxs-lookup"><span data-stu-id="8d917-106">To complete these steps, you must first complete the steps in the “Create a configuration with format of payment document” procedure.</span></span>


## <a name="change-the-configuration-of-the-electronic-payment-method"></a><span data-ttu-id="8d917-107">Vaihda sähköisen maksutavan konfiguraatio</span><span class="sxs-lookup"><span data-stu-id="8d917-107">Change the configuration of the electronic payment method</span></span>
1. <span data-ttu-id="8d917-108">Siirry kohtaan Ostoreskontra > Maksun asetukset > Maksutavat.</span><span class="sxs-lookup"><span data-stu-id="8d917-108">Go to Accounts payable > Payment setup > Methods of payment.</span></span>
2. <span data-ttu-id="8d917-109">Laajenna tiedostomuodon valinta tarvittaessa.</span><span class="sxs-lookup"><span data-stu-id="8d917-109">Toggle the File format section to expand it, if needed.</span></span>
3. <span data-ttu-id="8d917-110">Käytä pikasuodatinta tietueiden etsimiseen.</span><span class="sxs-lookup"><span data-stu-id="8d917-110">Use the Quick Filter to find records.</span></span> <span data-ttu-id="8d917-111">Voit esimerkiksi suodattaa Maksutapa-kenttää arvolla Sähköinen.</span><span class="sxs-lookup"><span data-stu-id="8d917-111">For example, filter on the Method of payment field with a value of 'Electronic'.</span></span>
4. <span data-ttu-id="8d917-112">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="8d917-112">Click Edit.</span></span>
5. <span data-ttu-id="8d917-113">Aseta Yleinen sähköinen raportointi -kentän arvoksi Kyllä.</span><span class="sxs-lookup"><span data-stu-id="8d917-113">Set the General electronic reporting field to Yes.</span></span>
    * <span data-ttu-id="8d917-114">Valitse Kyllä käyttääksesi yleistä sähköisen raportoinnin mallia maksutiedostojen luonnissa.</span><span class="sxs-lookup"><span data-stu-id="8d917-114">Select Yes to use the General electronic reporting pattern for payment files generation.</span></span>  
6. <span data-ttu-id="8d917-115">Avaa haku valitsemalla Nimi-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="8d917-115">In the Name field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="8d917-116">Valitse BACS-muotokonfiguraatio (Iso-Britannia, kuvitteellinen).</span><span class="sxs-lookup"><span data-stu-id="8d917-116">Select BACS (UK fictitious) format configuration.</span></span>
8. <span data-ttu-id="8d917-117">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="8d917-117">Click Save.</span></span>
9. <span data-ttu-id="8d917-118">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="8d917-118">Close the page.</span></span>

## <a name="test-the-format-of-generated-payment-files"></a><span data-ttu-id="8d917-119">Testaa luotujen maksutiedostojen muoto</span><span class="sxs-lookup"><span data-stu-id="8d917-119">Test the format of generated payment files</span></span>
1. <span data-ttu-id="8d917-120">Siirry kohtaan Ostoreskontra > Maksut > Maksukirjauskansio.</span><span class="sxs-lookup"><span data-stu-id="8d917-120">Go to Accounts payable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="8d917-121">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="8d917-121">Click New.</span></span>
3. <span data-ttu-id="8d917-122">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="8d917-122">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="8d917-123">Avaa haku valitsemalla Nimi-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="8d917-123">In the Name field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="8d917-124">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="8d917-124">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="8d917-125">Valitse VendPay.</span><span class="sxs-lookup"><span data-stu-id="8d917-125">Select VendPay.</span></span>  
6. <span data-ttu-id="8d917-126">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="8d917-126">Click Save.</span></span>
7. <span data-ttu-id="8d917-127">Valitse Rivit.</span><span class="sxs-lookup"><span data-stu-id="8d917-127">Click Lines.</span></span>
8. <span data-ttu-id="8d917-128">Kirjoita Yritys-kenttän arvoksi "DEMF".</span><span class="sxs-lookup"><span data-stu-id="8d917-128">In the Company field, type 'DEMF'.</span></span>
    * <span data-ttu-id="8d917-129">DEMF</span><span class="sxs-lookup"><span data-stu-id="8d917-129">DEMF</span></span>  
9. <span data-ttu-id="8d917-130">Määritä Tili-kentässä arvoksi DE-01001.</span><span class="sxs-lookup"><span data-stu-id="8d917-130">In the Account field, specify the values 'DE-01001'.</span></span>
    * <span data-ttu-id="8d917-131">DE - 01001</span><span class="sxs-lookup"><span data-stu-id="8d917-131">DE-01001</span></span>  
10. <span data-ttu-id="8d917-132">Kirjoita Kuvaus-kentän arvoksi Maksu.</span><span class="sxs-lookup"><span data-stu-id="8d917-132">In the Description field, type 'Payment'.</span></span>
    * <span data-ttu-id="8d917-133">Maksu</span><span class="sxs-lookup"><span data-stu-id="8d917-133">Payment</span></span>  
11. <span data-ttu-id="8d917-134">Syötä Debet-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="8d917-134">In the Debit field, enter a number.</span></span>
    * <span data-ttu-id="8d917-135">1 000</span><span class="sxs-lookup"><span data-stu-id="8d917-135">1000</span></span>  
12. <span data-ttu-id="8d917-136">Valitse Maksu-välilehti.</span><span class="sxs-lookup"><span data-stu-id="8d917-136">Click the Payment tab.</span></span>
13. <span data-ttu-id="8d917-137">Avaa haku valitsemalla Maksutapa-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="8d917-137">In the Method of payment field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="8d917-138">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="8d917-138">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="8d917-139">Valitse arvoksi Sähköinen.</span><span class="sxs-lookup"><span data-stu-id="8d917-139">Select the Electronic value.</span></span>  
15. <span data-ttu-id="8d917-140">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="8d917-140">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="8d917-141">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="8d917-141">Click Save.</span></span>
17. <span data-ttu-id="8d917-142">Valitse Muodosta maksut.</span><span class="sxs-lookup"><span data-stu-id="8d917-142">Click Generate payments.</span></span>
18. <span data-ttu-id="8d917-143">Avaa haku valitsemalla Maksutapa-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="8d917-143">In the Method of payment field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="8d917-144">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="8d917-144">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="8d917-145">Valitse arvoksi Sähköinen.</span><span class="sxs-lookup"><span data-stu-id="8d917-145">Select the Electronic value.</span></span>  
20. <span data-ttu-id="8d917-146">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="8d917-146">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="8d917-147">Valitse arvoksi Sähköinen.</span><span class="sxs-lookup"><span data-stu-id="8d917-147">Select the Electronic value.</span></span>  
21. <span data-ttu-id="8d917-148">Kirjoita arvo Tiedostonimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="8d917-148">In the File name field, type a value.</span></span>
    * <span data-ttu-id="8d917-149">Kirjoita esimerkiksi Maksut.</span><span class="sxs-lookup"><span data-stu-id="8d917-149">For example, type 'payments'.</span></span>  
22. <span data-ttu-id="8d917-150">Avaa haku valitsemalla Pankkitili-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="8d917-150">In the Bank account field, click the drop-down button to open the lookup.</span></span>
23. <span data-ttu-id="8d917-151">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="8d917-151">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="8d917-152">Valitse arvoksi GBSI OPER.</span><span class="sxs-lookup"><span data-stu-id="8d917-152">Select the value GBSI OPER.</span></span>  
24. <span data-ttu-id="8d917-153">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="8d917-153">Click OK.</span></span>
25. <span data-ttu-id="8d917-154">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="8d917-154">Click OK.</span></span>
    * <span data-ttu-id="8d917-155">Analysoi luotu, XML-muotoinen maksutiedosto.</span><span class="sxs-lookup"><span data-stu-id="8d917-155">Analyze the created payment file in XML format.</span></span> <span data-ttu-id="8d917-156">Vertaa tiedostoa suunniteltuun asiakirjan asetteluun ja määriteltyihin maksutapahtuman määritteisiin.</span><span class="sxs-lookup"><span data-stu-id="8d917-156">Compare it with the designed document layout and defined payment transaction attributes.</span></span>  

