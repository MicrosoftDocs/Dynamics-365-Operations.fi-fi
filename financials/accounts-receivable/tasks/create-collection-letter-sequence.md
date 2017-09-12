--- 
title: "Maksukehotusjärjestyksen määrittäminen"
description: "Tämän tehtävän ohjauksen avulla luodaan maksukehotussarja."
author: mikefalkner
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 6331c3680169b305c4bfbfada4ba106b619be092
ms.contentlocale: fi-fi
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-collection-letter-sequence"></a><span data-ttu-id="4f085-103">Maksukehotusjärjestyksen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="4f085-103">Create a collection letter sequence</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4f085-104">Tämän tehtävän ohjauksen avulla luodaan maksukehotussarja.</span><span class="sxs-lookup"><span data-stu-id="4f085-104">Use this task guide to create a collection letter sequence.</span></span> <span data-ttu-id="4f085-105">Tässä tehtävässä käytetään esittely-yritystä USMF.</span><span class="sxs-lookup"><span data-stu-id="4f085-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="4f085-106">Siirry kohtaan Luotonvalvonta > Asetukset > Määritä maksukehotusjärjestys.</span><span class="sxs-lookup"><span data-stu-id="4f085-106">Go to Credit and collections > Setup > Set up collection letter sequence.</span></span>
2. <span data-ttu-id="4f085-107">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="4f085-107">Click New.</span></span>
3. <span data-ttu-id="4f085-108">Syötä Maksukehotussarja-kenttään sarjaa kuvaavan järjestyksen tunnus.</span><span class="sxs-lookup"><span data-stu-id="4f085-108">In the Collection letter sequence field, enter a sequence ID that will represent the sequence.</span></span> <span data-ttu-id="4f085-109">Sitä käytetään kirjausprofiilin määrittämisessä.</span><span class="sxs-lookup"><span data-stu-id="4f085-109">It will be used when you set up a posting profile.</span></span>
4. <span data-ttu-id="4f085-110">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="4f085-110">In the Description field, type a value.</span></span>
    * <span data-ttu-id="4f085-111">Maksuehdot ovat valinnaisia.</span><span class="sxs-lookup"><span data-stu-id="4f085-111">The terms of payment is optional.</span></span> <span data-ttu-id="4f085-112">Jos syötät tähän arvon, maksukehotuksen perintälaskussa käytetään näitä maksuehtoja asiakkaan tietoihin tallennettujen maksuehtojen sijaan.</span><span class="sxs-lookup"><span data-stu-id="4f085-112">If you enter a value here, the collection letter fee invoice will use these terms of payment instead of the terms of payment stored with the customer.</span></span>  
5. <span data-ttu-id="4f085-113">Valitse Maksukehotuskoodi-kenttään ensimmäisenä lähetettävän maksukehotuksen koodi.</span><span class="sxs-lookup"><span data-stu-id="4f085-113">In the collection letter code field, select the code for the first collection letter that you want to send.</span></span>
    * <span data-ttu-id="4f085-114">Ensimmäinen maksukehotus luodaan laskun eräpäivän, tämän rivin Päivät-kenttään syöttämäsi lisäajan ja muiden tälle riville syöttämiesi tietojen perusteella.</span><span class="sxs-lookup"><span data-stu-id="4f085-114">The first collection letter is created according to the due date on the invoice, the value that you enter for the grace period in the Days field on this line, and other information that you enter on this line.</span></span>  
6. <span data-ttu-id="4f085-115">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="4f085-115">In the Description field, type a value.</span></span>
    * <span data-ttu-id="4f085-116">Lisämaksun valuutan oletusarvo on asiakkaan valuutta.</span><span class="sxs-lookup"><span data-stu-id="4f085-116">The currency for the fee defaults to the customer currency.</span></span> <span data-ttu-id="4f085-117">Tämä valuuttakoodi voi olla eri kuin laskun valuutta.</span><span class="sxs-lookup"><span data-stu-id="4f085-117">This currency code can be different than the invoice currency.</span></span>  
7. <span data-ttu-id="4f085-118">Lisää järjestyksessä seuraavana lähetettävä maksukehotus valitsemalla Lisää.</span><span class="sxs-lookup"><span data-stu-id="4f085-118">Click Add to add the next collection letter that will be sent in the sequence</span></span>
    * <span data-ttu-id="4f085-119">Usein ensimmäinen maksukehotus toimii vain varoituksena.</span><span class="sxs-lookup"><span data-stu-id="4f085-119">In many cases, the first collection letter is just a warning.</span></span> <span data-ttu-id="4f085-120">Voit lisätä lisämaksuja tarvittaessa.</span><span class="sxs-lookup"><span data-stu-id="4f085-120">You can add fees if needed.</span></span>  
8. <span data-ttu-id="4f085-121">Valitse Maksukehotuskoodi-kentässä järjestyksessä seuraavana lähetettävä maksukehotus.</span><span class="sxs-lookup"><span data-stu-id="4f085-121">In the collection letter code field, select the next collection letter that will be sent in the sequence.</span></span>
9. <span data-ttu-id="4f085-122">Kirjoita Kuvaus-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="4f085-122">In the Description field, type a value.</span></span>
10. <span data-ttu-id="4f085-123">Valitse Päätili-kentässä lisämaksuissa käytettävä tuottotili.</span><span class="sxs-lookup"><span data-stu-id="4f085-123">In the main account field, select the revenue account that will be used for fees.</span></span>
11. <span data-ttu-id="4f085-124">Syötä lisämaksu, joka veloitetaan tämän maksukehotuksen kirjaamisen yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="4f085-124">Enter the fee that will be charged when this collection letter is posted.</span></span>
12. <span data-ttu-id="4f085-125">Avaa haku valitsemalla Nimikkeen arvonlisäveroryhmä -kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="4f085-125">In the Item sales tax group field, click the drop down button to open the lookup.</span></span>
    * <span data-ttu-id="4f085-126">Valitse nimikkeen arvonlisäveroryhmä, jos lisämaksulle on laskettava arvonlisävero.</span><span class="sxs-lookup"><span data-stu-id="4f085-126">Select an item sales tax group if sales taxes must be calculated on the fee.</span></span>  
13. <span data-ttu-id="4f085-127">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="4f085-127">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="4f085-128">Syötä maksukehotuksen lähettämiseksi vaadittava erääntynyt vähimmäissaldo.</span><span class="sxs-lookup"><span data-stu-id="4f085-128">Enter the minimum overdue balance required before a collection letter is sent.</span></span>
15. <span data-ttu-id="4f085-129">Syötä sallittujen eräpäivän jälkeisten maksupäivien määrä.</span><span class="sxs-lookup"><span data-stu-id="4f085-129">Enter the number of grace days that you will allow.</span></span>
    * <span data-ttu-id="4f085-130">Tämä on niiden eräpäivän jälkeisten päivien lukumäärä, joille maksukehotus voidaan luoda.</span><span class="sxs-lookup"><span data-stu-id="4f085-130">This is the number of days after the due date that a collection letter can be generated.</span></span> <span data-ttu-id="4f085-131">Laskennassa käytettävä eräpäivä riippuu maksukehotuksen sijainnista maksukehotussarjassa: ⦁ Maksukehotuksen 1 lisäaika määritetään suhteessa laskun eräpäivään.</span><span class="sxs-lookup"><span data-stu-id="4f085-131">The due date that is used for the calculation depends on the position of the collection letter in the collection letter sequence:   ⦁    The grace period for collection letter 1 is relative to the due date on the invoice.</span></span>  <span data-ttu-id="4f085-132">⦁ Maksukehotuksen 2 ja sen jälkeisten maksukehotusten lisäaika määritetään suhteessa edellisen maksukehotuksen kirjaus- tai tulostuspäivämäärään. Tämä riippuu Myyntireskontran parametrit -sivun Päivitä maksukehotuskoodi -kentässä tehdystä valinnasta.</span><span class="sxs-lookup"><span data-stu-id="4f085-132">⦁ The grace period for collection letters 2 and higher is relative to the date that the previous collection letter is posted or printed, depending on the selection in the Update collection letter code field in the Accounts receivable parameters page.</span></span>  
16. <span data-ttu-id="4f085-133">Lisää sarjan viimeinen maksukehotus valitsemalla Lisää.</span><span class="sxs-lookup"><span data-stu-id="4f085-133">Click Add to add the last collection letter in the sequence.</span></span>
    * <span data-ttu-id="4f085-134">Voit lisätä maksukehotussarjaan enintään viisi maksukehotuskoodia.</span><span class="sxs-lookup"><span data-stu-id="4f085-134">You can add up to five collection letter codes for a collection letter sequence.</span></span>  
17. <span data-ttu-id="4f085-135">Valitse Maksukehotuskoodi-kentässä järjestyksessä seuraavana lähetettävä maksukehotus.</span><span class="sxs-lookup"><span data-stu-id="4f085-135">In the collection letter code field, select the next collection letter that will be sent in the sequence.</span></span>
18. <span data-ttu-id="4f085-136">Kirjoita Kuvaus-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="4f085-136">In the Description field, type a value.</span></span>
19. <span data-ttu-id="4f085-137">Määritä Päätili-kenttään haluamasi arvot.</span><span class="sxs-lookup"><span data-stu-id="4f085-137">In the Main account field, specify the desired values.</span></span>
20. <span data-ttu-id="4f085-138">Syötä Lisämaksu valuuttana -kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="4f085-138">In the Fee in currency field, enter a number.</span></span>
21. <span data-ttu-id="4f085-139">Avaa haku valitsemalla Nimikkeen arvonlisäveroryhmä -kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="4f085-139">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
22. <span data-ttu-id="4f085-140">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="4f085-140">In the list, click the link in the selected row.</span></span>
23. <span data-ttu-id="4f085-141">Syötä Erääntynyt vähimmäissaldo -kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="4f085-141">In the Minimum overdue balance field, enter a number.</span></span>
24. <span data-ttu-id="4f085-142">Syötä Päivät-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="4f085-142">In the Days field, enter a number.</span></span>
25. <span data-ttu-id="4f085-143">Lopeta asiakkaan lisätoimitukset ja laskutus valitsemalla tämä valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="4f085-143">Select this check box to stop the customer from additional deliveries and invoicing.</span></span>
    * <span data-ttu-id="4f085-144">Voit poistaa tilin eston valitsemalla Asiakkaat-sivun Pidossa oleva laskutus ja toimitus -kenttään arvon Ei.</span><span class="sxs-lookup"><span data-stu-id="4f085-144">To unblock the account, select No in the Invoicing and delivery on hold field in the Customers page.</span></span>  
26. <span data-ttu-id="4f085-145">Laajenna Huomautukset-pikavälilehti.</span><span class="sxs-lookup"><span data-stu-id="4f085-145">Expand the Note fasttab.</span></span>
27. <span data-ttu-id="4f085-146">Kirjoita valitun maksukehotuskoodin maksukehotuksessa näkyvä teksti.</span><span class="sxs-lookup"><span data-stu-id="4f085-146">Enter the text to appear on the collection letter for the selected collection letter code.</span></span>
    * <span data-ttu-id="4f085-147">Huomautusruudun yläpuolella olevan Käännökset-valikon avulla voit kääntää tämän tekstin useille eri kielille.</span><span class="sxs-lookup"><span data-stu-id="4f085-147">You can translate this text in to multiple languages using the Translations menu above the note box.</span></span>  


