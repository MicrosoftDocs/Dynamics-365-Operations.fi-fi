--- 
title: "Varmuusvaraston kirjauskansion käyttäminen minimikattavuuden päivittämiseen"
description: "Seuraavassa menettelyssä kuvataan, miten voit laskea vähimmäiskattavuuden ehdotukset historiatapahtumiin perustuen ja päivittää nimikekattavuuden ehdotusten mukaiseksi."
author: ChristianRytt
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqItemJournalName, ReqItemJournalSafetyStock, EcoResProductInformationDialog, EcoResProductDetailsExtended, ReqItemTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: 5199d5270a6ec709f76ddb05fda3d98d3df02384
ms.contentlocale: fi-fi
ms.lasthandoff: 09/11/2018

---
# <a name="use-the-safety-stock-journal-to-update-minimum-coverage"></a><span data-ttu-id="562c9-103">Varmuusvaraston kirjauskansion käyttäminen minimikattavuuden päivittämiseen</span><span class="sxs-lookup"><span data-stu-id="562c9-103">Use the safety stock journal to update minimum coverage</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="562c9-104">Seuraavassa menettelyssä kuvataan, miten voit laskea vähimmäiskattavuuden ehdotukset historiatapahtumiin perustuen ja päivittää nimikekattavuuden ehdotusten mukaiseksi.</span><span class="sxs-lookup"><span data-stu-id="562c9-104">This procedure shows how to calculate minimum coverage proposals based on historical transactions and then update the item coverage with the proposals.</span></span> <span data-ttu-id="562c9-105">Tämä tehdään varmuusvaraston kirjauskansion avulla.</span><span class="sxs-lookup"><span data-stu-id="562c9-105">This is done using the safety stock journal.</span></span> <span data-ttu-id="562c9-106">Tämän tehtävän luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="562c9-106">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="562c9-107">Tämä tehtävä on tarkoitettu tuotannon suunnittelijalle minimikattavuuden ylläpitoa varten.</span><span class="sxs-lookup"><span data-stu-id="562c9-107">This task is intended for the production planner, to help maintain minimum coverage.</span></span>


## <a name="create-a-new-safety-stock-journal-name"></a><span data-ttu-id="562c9-108">Uuden varmuusvaraston kirjauskansion nimen luominen</span><span class="sxs-lookup"><span data-stu-id="562c9-108">Create a new safety stock journal name</span></span>
1. <span data-ttu-id="562c9-109">Siirry kohtaan Varmuusvarastokirjauskansion nimet.</span><span class="sxs-lookup"><span data-stu-id="562c9-109">Go to Safety stock journal names.</span></span>
2. <span data-ttu-id="562c9-110">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="562c9-110">Click New.</span></span>
3. <span data-ttu-id="562c9-111">Kirjoita "Materiaali" nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="562c9-111">In the Name field, type 'Material'.</span></span>
4. <span data-ttu-id="562c9-112">Kirjoita Kuvaus-kentän arvoksi Materiaali.</span><span class="sxs-lookup"><span data-stu-id="562c9-112">In the Description field, type 'Material'.</span></span>
5. <span data-ttu-id="562c9-113">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="562c9-113">Close the page.</span></span>

## <a name="create-a-safety-stock-journal"></a><span data-ttu-id="562c9-114">Luo varmuusvaraston kirjauskansio</span><span class="sxs-lookup"><span data-stu-id="562c9-114">Create a safety stock journal</span></span>
1. <span data-ttu-id="562c9-115">Siirry kohtaan Varmuusvaraston laskenta.</span><span class="sxs-lookup"><span data-stu-id="562c9-115">Go to Safety stock calculation.</span></span>
2. <span data-ttu-id="562c9-116">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="562c9-116">Click New.</span></span>
3. <span data-ttu-id="562c9-117">Syötä tai valitse arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="562c9-117">In the Name field, enter or select a value.</span></span>
    * <span data-ttu-id="562c9-118">Valitse luomasi varmuusvaraston kirjauskansion nimi, esimerkiksi Materiaali.</span><span class="sxs-lookup"><span data-stu-id="562c9-118">Select the safety stock journal name that you created, for example, Material.</span></span>  
4. <span data-ttu-id="562c9-119">Valitse Luo rivit.</span><span class="sxs-lookup"><span data-stu-id="562c9-119">Click Create lines.</span></span>
5. <span data-ttu-id="562c9-120">Syötä päivämäärä Päivämäärästä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="562c9-120">In the From date field, enter a date.</span></span>
    * <span data-ttu-id="562c9-121">Aseta päiväksi "2015-01-02".</span><span class="sxs-lookup"><span data-stu-id="562c9-121">Set the date to '2015-01-02'.</span></span>  
6. <span data-ttu-id="562c9-122">Kirjoita päivämäärä Päivämäärään-kenttään.</span><span class="sxs-lookup"><span data-stu-id="562c9-122">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="562c9-123">Aseta päiväksi "2015-12-30".</span><span class="sxs-lookup"><span data-stu-id="562c9-123">Set the date to '2015-12-30'.</span></span>  
7. <span data-ttu-id="562c9-124">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="562c9-124">Click OK.</span></span>
    * <span data-ttu-id="562c9-125">Tämä luo rivit dimensioille, joilla on varastotapahtumia.</span><span class="sxs-lookup"><span data-stu-id="562c9-125">This will create lines for the dimensions that have inventory transactions.</span></span>  

## <a name="calculate-proposal"></a><span data-ttu-id="562c9-126">Laske ehdotus</span><span class="sxs-lookup"><span data-stu-id="562c9-126">Calculate proposal</span></span>
1. <span data-ttu-id="562c9-127">Napsauta kohtaa Laske ehdotus.</span><span class="sxs-lookup"><span data-stu-id="562c9-127">Click Calculate proposal.</span></span>
2. <span data-ttu-id="562c9-128">Valitse Käytä keskimääräistä varasto-ottoa läpimenoaikana -vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="562c9-128">Select the Use average issue during lead time option.</span></span>
3. <span data-ttu-id="562c9-129">Aseta kerroinarvoksi 10.</span><span class="sxs-lookup"><span data-stu-id="562c9-129">Set Multiplication factor to '10'.</span></span>
    * <span data-ttu-id="562c9-130">Kerroinarvoa käytetään ehdotuksen oikaisemiseen.</span><span class="sxs-lookup"><span data-stu-id="562c9-130">The Multiply factor is used to adjust the proposal.</span></span> <span data-ttu-id="562c9-131">Koska esittelytiedoissa on vain muutamia tapahtumia, kerroin on määritettävä, jos haluat realistisen ehdotuksen.</span><span class="sxs-lookup"><span data-stu-id="562c9-131">Because demo data only has a few transactions, you will need to set the factor to get a realistic proposal.</span></span>  
4. <span data-ttu-id="562c9-132">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="562c9-132">Click OK.</span></span>
    * <span data-ttu-id="562c9-133">Etsi M0002 ja M0003 alaspäin selaamalla.</span><span class="sxs-lookup"><span data-stu-id="562c9-133">Scroll down to find M0002 and M0003.</span></span> <span data-ttu-id="562c9-134">Näytä Laskettu vähimmäismäärä -sarake.</span><span class="sxs-lookup"><span data-stu-id="562c9-134">View the Calculated minimum quantity column.</span></span>   

## <a name="update-minimum-quantity"></a><span data-ttu-id="562c9-135">Päivitä vähimmäismäärä</span><span class="sxs-lookup"><span data-stu-id="562c9-135">Update minimum quantity</span></span>
1. <span data-ttu-id="562c9-136">Syötä numero Uusi vähimmäismäärä -kenttään.</span><span class="sxs-lookup"><span data-stu-id="562c9-136">In the New minimum quantity field, enter a number.</span></span>
    * <span data-ttu-id="562c9-137">Päivitä uusi vähimmäismäärä vastaavaan lasketun vähimmäismäärän arvoa.</span><span class="sxs-lookup"><span data-stu-id="562c9-137">Update the New minimum quantity to match the value in the Calculated minimum quantity.</span></span> <span data-ttu-id="562c9-138">Jos laskettu vähimmäismäärä on nolla, voit syöttää haluamasi tulevan arvon.</span><span class="sxs-lookup"><span data-stu-id="562c9-138">If the Calculated minimum is zero,  you can enter the desired future value.</span></span> <span data-ttu-id="562c9-139">Voit esimerkiksi syöttää lasketun vähimmäismäärän tähän kenttään M0002 sisältävälle varastolle 12.</span><span class="sxs-lookup"><span data-stu-id="562c9-139">For example, you can enter the Calculated minimum quantity in this field for M0002 that has warehouse 12.</span></span>  
2. <span data-ttu-id="562c9-140">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="562c9-140">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="562c9-141">Voit valita esimerkiksi M0002 sisältävän varaston 12.</span><span class="sxs-lookup"><span data-stu-id="562c9-141">For example, you can select M0002 that has warehouse 12.</span></span>  
3. <span data-ttu-id="562c9-142">Syötä numero Uusi vähimmäismäärä -kenttään.</span><span class="sxs-lookup"><span data-stu-id="562c9-142">In the New minimum quantity field, enter a number.</span></span>
    * <span data-ttu-id="562c9-143">Päivitä uusi vähimmäismäärä vastaavaan lasketun vähimmäismäärän arvoa.</span><span class="sxs-lookup"><span data-stu-id="562c9-143">Update the New minimum quantity to match the value in the Calculated minimum quantity.</span></span> <span data-ttu-id="562c9-144">Jos laskettu vähimmäismäärä on nolla, voit syöttää haluamasi tulevan arvon.</span><span class="sxs-lookup"><span data-stu-id="562c9-144">If the Calculated minimum is zero you can enter the desired future value.</span></span>  

## <a name="post-the-new-minimum-quantity-and-validate-the-result"></a><span data-ttu-id="562c9-145">Kirjaa uusi vähimmäismäärä ja vahvista tulos</span><span class="sxs-lookup"><span data-stu-id="562c9-145">Post the new minimum quantity and validate the result</span></span>
1. <span data-ttu-id="562c9-146">Valitse Kirjaa.</span><span class="sxs-lookup"><span data-stu-id="562c9-146">Click Post.</span></span>
2. <span data-ttu-id="562c9-147">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="562c9-147">Click OK.</span></span>
3. <span data-ttu-id="562c9-148">Käytä Nimiketunnus-kentän linkkiä napsauttamalla.</span><span class="sxs-lookup"><span data-stu-id="562c9-148">Click to follow the link in the Item number field.</span></span>
4. <span data-ttu-id="562c9-149">Käytä Nimiketunnus-kentän linkkiä napsauttamalla.</span><span class="sxs-lookup"><span data-stu-id="562c9-149">Click to follow the link in the Item number field.</span></span>
5. <span data-ttu-id="562c9-150">Valitse toimintoruudussa Suunnitelma.</span><span class="sxs-lookup"><span data-stu-id="562c9-150">On the Action Pane, click Plan.</span></span>
6. <span data-ttu-id="562c9-151">Valitse Nimikekattavuus.</span><span class="sxs-lookup"><span data-stu-id="562c9-151">Click Item coverage.</span></span>
    * <span data-ttu-id="562c9-152">Huomaa, että vähimmäismääräksi on päivitetty uusi vähimmäismäärä varmuusvaraston kirjauskansiosta.</span><span class="sxs-lookup"><span data-stu-id="562c9-152">Notice that the Minimum quantity has been updated with the new minimum quantity from the safety stock journal.</span></span>  


