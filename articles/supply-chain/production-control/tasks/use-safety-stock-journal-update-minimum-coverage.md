---
title: Varmuusvaraston kirjauskansion käyttäminen minimikattavuuden päivittämiseen
description: Seuraavassa menettelyssä kuvataan, miten voit laskea vähimmäiskattavuuden ehdotukset historiatapahtumiin perustuen ja päivittää nimikekattavuuden ehdotusten mukaiseksi.
author: ChristianRytt
manager: AnnBe
ms.date: 08/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqItemJournalName, ReqItemJournalSafetyStock, EcoResProductInformationDialog, EcoResProductDetailsExtended, ReqItemTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 478dd85abebf76dd264e93bcbe3f218a0ff0a5a8
ms.sourcegitcommit: cbcf344b3b552acca56c3e27606eac7f2f124afe
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/22/2019
ms.locfileid: "1916803"
---
# <a name="use-the-safety-stock-journal-to-update-minimum-coverage"></a><span data-ttu-id="35a37-103">Varmuusvaraston kirjauskansion käyttäminen minimikattavuuden päivittämiseen</span><span class="sxs-lookup"><span data-stu-id="35a37-103">Use the safety stock journal to update minimum coverage</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="35a37-104">Seuraavassa menettelyssä kuvataan, miten voit laskea vähimmäiskattavuuden ehdotukset historiatapahtumiin perustuen ja päivittää nimikekattavuuden ehdotusten mukaiseksi.</span><span class="sxs-lookup"><span data-stu-id="35a37-104">This procedure shows how to calculate minimum coverage proposals based on historical transactions and then update the item coverage with the proposals.</span></span> <span data-ttu-id="35a37-105">Tämä tehdään varmuusvaraston kirjauskansion avulla.</span><span class="sxs-lookup"><span data-stu-id="35a37-105">This is done using the safety stock journal.</span></span> <span data-ttu-id="35a37-106">Tämän tehtävän luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="35a37-106">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="35a37-107">Tämä tehtävä on tarkoitettu tuotannon suunnittelijalle minimikattavuuden ylläpitoa varten.</span><span class="sxs-lookup"><span data-stu-id="35a37-107">This task is intended for the production planner, to help maintain minimum coverage.</span></span>


## <a name="create-a-new-safety-stock-journal-name"></a><span data-ttu-id="35a37-108">Uuden varmuusvaraston kirjauskansion nimen luominen</span><span class="sxs-lookup"><span data-stu-id="35a37-108">Create a new safety stock journal name</span></span>
1. <span data-ttu-id="35a37-109">Siirry kohtaan **Siirtymisruutu** > **Pääsuunnitelu > Asetukset > Varmuusvarastokirjauskansion nimet**.</span><span class="sxs-lookup"><span data-stu-id="35a37-109">In the **Navigation pane**, go to **Master planning > Setup > Safety stock journal names**.</span></span>
2. <span data-ttu-id="35a37-110">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="35a37-110">Click **New**.</span></span>
3. <span data-ttu-id="35a37-111">Kirjoita "Materiaali" **Nimi**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="35a37-111">In the **Name** field, type 'Material'.</span></span>
4. <span data-ttu-id="35a37-112">Kirjoita **Kuvaus**-kentän arvoksi Materiaali.</span><span class="sxs-lookup"><span data-stu-id="35a37-112">In the **Description** field, type 'Material'.</span></span>
5. <span data-ttu-id="35a37-113">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="35a37-113">Close the page.</span></span>

## <a name="create-a-safety-stock-journal"></a><span data-ttu-id="35a37-114">Luo varmuusvaraston kirjauskansio</span><span class="sxs-lookup"><span data-stu-id="35a37-114">Create a safety stock journal</span></span>
1. <span data-ttu-id="35a37-115">Siirry **siirtymisruudussa** kohtaan **Pääsuunnittelu > Pääsunnittelu > Suorita > Varmuusvaraston laskenta**.</span><span class="sxs-lookup"><span data-stu-id="35a37-115">In the **Navigation pane**, go to **Master planning > Master planning > Run > Safety stock calculation**.</span></span>
2. <span data-ttu-id="35a37-116">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="35a37-116">Click **New**.</span></span>
3. <span data-ttu-id="35a37-117">Anna tai valitse arvo **Nimi**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="35a37-117">In the **Name** field, enter or select a value.</span></span> <span data-ttu-id="35a37-118">Valitse luomasi varmuusvaraston kirjauskansion nimi, esimerkiksi Materiaali.</span><span class="sxs-lookup"><span data-stu-id="35a37-118">Select the safety stock journal name that you created, for example, Material.</span></span>  
4. <span data-ttu-id="35a37-119">Valitse **Luo rivit**.</span><span class="sxs-lookup"><span data-stu-id="35a37-119">Click **Create lines**.</span></span>
5. <span data-ttu-id="35a37-120">Syötä päivämäärä **Päivämäärästä**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="35a37-120">In the **From date** field, enter a date.</span></span>  
6. <span data-ttu-id="35a37-121">Kirjoita päivämäärä **Päivämäärään**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="35a37-121">In the **To date** field, enter a date.</span></span>
7. <span data-ttu-id="35a37-122">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="35a37-122">Click **OK**.</span></span> <span data-ttu-id="35a37-123">Tämä luo rivit dimensioille, joilla on varastotapahtumia.</span><span class="sxs-lookup"><span data-stu-id="35a37-123">This will create lines for the dimensions that have inventory transactions.</span></span>  

## <a name="calculate-proposal"></a><span data-ttu-id="35a37-124">Laske ehdotus</span><span class="sxs-lookup"><span data-stu-id="35a37-124">Calculate proposal</span></span>
1. <span data-ttu-id="35a37-125">Napsauta kohtaa **Laske ehdotus**.</span><span class="sxs-lookup"><span data-stu-id="35a37-125">Click **Calculate proposal**.</span></span>
2. <span data-ttu-id="35a37-126">Valitse **Käytä keskimääräistä varasto-ottoa läpimenoaikana** -vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="35a37-126">Select the **Use average issue during lead time** option.</span></span>
3. <span data-ttu-id="35a37-127">Aseta **kerroinarvoksi** 10.</span><span class="sxs-lookup"><span data-stu-id="35a37-127">Set **Multiplication factor** to '10'.</span></span> <span data-ttu-id="35a37-128">Kerroinarvoa käytetään ehdotuksen oikaisemiseen.</span><span class="sxs-lookup"><span data-stu-id="35a37-128">The Multiply factor is used to adjust the proposal.</span></span> <span data-ttu-id="35a37-129">Koska esittelytiedoissa on vain muutamia tapahtumia, kerroin on määritettävä, jos haluat realistisen ehdotuksen.</span><span class="sxs-lookup"><span data-stu-id="35a37-129">Because demo data only has a few transactions, you will need to set the factor to get a realistic proposal.</span></span>  
4. <span data-ttu-id="35a37-130">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="35a37-130">Click **OK**.</span></span> <span data-ttu-id="35a37-131">Etsi M0002 ja M0003 alaspäin selaamalla.</span><span class="sxs-lookup"><span data-stu-id="35a37-131">Scroll down to find M0002 and M0003.</span></span> <span data-ttu-id="35a37-132">Näytä **Laskettu vähimmäismäärä** -sarake.</span><span class="sxs-lookup"><span data-stu-id="35a37-132">View the **Calculated minimum** quantity column.</span></span>   

## <a name="update-minimum-quantity"></a><span data-ttu-id="35a37-133">Päivitä vähimmäismäärä</span><span class="sxs-lookup"><span data-stu-id="35a37-133">Update minimum quantity</span></span>
1. <span data-ttu-id="35a37-134">Syötä numero **Uusi vähimmäismäärä** -kenttään.</span><span class="sxs-lookup"><span data-stu-id="35a37-134">In the **New minimum quantity** field, enter a number.</span></span> <span data-ttu-id="35a37-135">Päivitä uusi vähimmäismäärä vastaavaan lasketun vähimmäismäärän arvoa.</span><span class="sxs-lookup"><span data-stu-id="35a37-135">Update the New minimum quantity to match the value in the Calculated minimum quantity.</span></span> <span data-ttu-id="35a37-136">Jos laskettu vähimmäismäärä on nolla, voit syöttää haluamasi tulevan arvon.</span><span class="sxs-lookup"><span data-stu-id="35a37-136">If the Calculated minimum is zero,  you can enter the desired future value.</span></span> <span data-ttu-id="35a37-137">Voit esimerkiksi syöttää lasketun vähimmäismäärän tähän kenttään M0002 sisältävälle varastolle 12.</span><span class="sxs-lookup"><span data-stu-id="35a37-137">For example, you can enter the Calculated minimum quantity in this field for M0002 that has warehouse 12.</span></span>  
2. <span data-ttu-id="35a37-138">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="35a37-138">In the list, find and select the desired record.</span></span> <span data-ttu-id="35a37-139">Voit valita esimerkiksi M0002 sisältävän varaston 12.</span><span class="sxs-lookup"><span data-stu-id="35a37-139">For example, you can select M0002 that has warehouse 12.</span></span>  
3. <span data-ttu-id="35a37-140">Syötä numero **Uusi vähimmäismäärä** -kenttään.</span><span class="sxs-lookup"><span data-stu-id="35a37-140">In the **New minimum quantity** field, enter a number.</span></span> <span data-ttu-id="35a37-141">Päivitä uusi vähimmäismäärä vastaavaan lasketun vähimmäismäärän arvoa.</span><span class="sxs-lookup"><span data-stu-id="35a37-141">Update the New minimum quantity to match the value in the Calculated minimum quantity.</span></span> <span data-ttu-id="35a37-142">Jos laskettu vähimmäismäärä on nolla, voit syöttää haluamasi tulevan arvon.</span><span class="sxs-lookup"><span data-stu-id="35a37-142">If the Calculated minimum is zero you can enter the desired future value.</span></span>  

## <a name="post-the-new-minimum-quantity-and-validate-the-result"></a><span data-ttu-id="35a37-143">Kirjaa uusi vähimmäismäärä ja vahvista tulos</span><span class="sxs-lookup"><span data-stu-id="35a37-143">Post the new minimum quantity and validate the result</span></span>
1. <span data-ttu-id="35a37-144">Valitse **Kirjaa**.</span><span class="sxs-lookup"><span data-stu-id="35a37-144">Click **Post**.</span></span>
2. <span data-ttu-id="35a37-145">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="35a37-145">Click **OK**.</span></span>
3. <span data-ttu-id="35a37-146">Käytä **Nimiketunnus**-kentän linkkiä napsauttamalla.</span><span class="sxs-lookup"><span data-stu-id="35a37-146">Click to follow the link in the **Item number** field.</span></span>
4. <span data-ttu-id="35a37-147">Käytä **Nimiketunnus**-kentän linkkiä napsauttamalla.</span><span class="sxs-lookup"><span data-stu-id="35a37-147">Click to follow the link in the **Item number** field.</span></span>
5. <span data-ttu-id="35a37-148">Valitse **toimintoruudussa** Suunnitelma.</span><span class="sxs-lookup"><span data-stu-id="35a37-148">On the **Action Pane**, click Plan.</span></span>
6. <span data-ttu-id="35a37-149">Valitse **Nimikekattavuus**.</span><span class="sxs-lookup"><span data-stu-id="35a37-149">Click **Item coverage**.</span></span> <span data-ttu-id="35a37-150">Huomaa, että **vähimmäismääräksi** on päivitetty uusi vähimmäismäärä varmuusvaraston kirjauskansiosta.</span><span class="sxs-lookup"><span data-stu-id="35a37-150">Notice that the **Minimum quantity** has been updated with the new minimum quantity from the safety stock journal.</span></span>  

