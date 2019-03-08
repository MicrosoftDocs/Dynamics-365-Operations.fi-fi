---
title: Kanban-määräehdotusten laskeminen
description: Tässä menettelyssä keskitytään tietyn kanbanin koon ja määrien optimointiin tietylle kanban-säännölle kanban-määrän laskelman avulla.
author: ChristianRytt
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 540dd32c5da5859ef5e69f55d6806eada90bc840
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "348983"
---
# <a name="calculate-kanban-quantity-suggestions"></a><span data-ttu-id="f8018-103">Kanban-määräehdotusten laskeminen</span><span class="sxs-lookup"><span data-stu-id="f8018-103">Calculate kanban quantity suggestions</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f8018-104">Tässä menettelyssä keskitytään tietyn kanbanin koon ja määrien optimointiin tietylle kanban-säännölle kanban-määrän laskelman avulla.</span><span class="sxs-lookup"><span data-stu-id="f8018-104">This procedure focuses on optimizing the kanban size and quantities for a specific kanban rule by using the kanban quantity calculation.</span></span> <span data-ttu-id="f8018-105">Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="f8018-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="f8018-106">Tämä menettely on tarkoitettu arvovirtaa hallitsevalle työntekijälle.</span><span class="sxs-lookup"><span data-stu-id="f8018-106">This procedure is intended for the value stream manager.</span></span> <span data-ttu-id="f8018-107">Edellytys on Lisää uusi kanban-määrän laskentakäytäntö kanban-sääntöön -menettelyn suorittaminen.</span><span class="sxs-lookup"><span data-stu-id="f8018-107">It is a prerequisite that you have completed the procedure Add a new kanban quantity calculation policy to a kanban rule.</span></span>


## <a name="create-a-kanban-quantity-calculation"></a><span data-ttu-id="f8018-108">Kanban-määrän laskelman luominen</span><span class="sxs-lookup"><span data-stu-id="f8018-108">Create a kanban quantity calculation</span></span>
1. <span data-ttu-id="f8018-109">Siirry kohtaan Tuotannonhallinta > Kausittaiset tehtävät > Kanban-määrän laskeminen > Laske Kanban-määrä.</span><span class="sxs-lookup"><span data-stu-id="f8018-109">Go to Production control > Periodic tasks > Kanban quantity calculation > Calculate kanban quantity.</span></span>
2. <span data-ttu-id="f8018-110">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="f8018-110">Click New.</span></span>
3. <span data-ttu-id="f8018-111">Syötä Nimi-kenttään Kaiutin2016.</span><span class="sxs-lookup"><span data-stu-id="f8018-111">In the Name field, type 'Speaker2016'.</span></span>
4. <span data-ttu-id="f8018-112">Avaa haku valitsemalla Nimi-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="f8018-112">In the Name field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="f8018-113">Valitse Lisää uusi kanban-määrän laskentakäytäntö kanban-sääntöön -menettelyssä luotu käytäntö.</span><span class="sxs-lookup"><span data-stu-id="f8018-113">Select the policy that you have created in the procedure Add a new kanban quantity calculation policy to a kanban rule.</span></span> <span data-ttu-id="f8018-114">Valitse esimerkiksi arvo Kaiutin2016.</span><span class="sxs-lookup"><span data-stu-id="f8018-114">For example, Speaker2016.</span></span>  
5. <span data-ttu-id="f8018-115">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="f8018-115">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="f8018-116">Määritä Säännön voimassaolon alkupäivämäärä -kenttään päivämääräksi ja kellonajaksi 17.12.2012 8.00,00.</span><span class="sxs-lookup"><span data-stu-id="f8018-116">In the Rule active as of date field, set the date and time to '2012-12-17T08:00:00'.</span></span>
    * <span data-ttu-id="f8018-117">Tämä Päivämäärä toimii kanban-määrän laskentaan sisällytettävien kiinteiden kanban-sääntöjen määrittämisen perustana.</span><span class="sxs-lookup"><span data-stu-id="f8018-117">This date serves as the basis for determining which fixed kanban rules are included in the kanban quantity calculation.</span></span>  
7. <span data-ttu-id="f8018-118">Määritä Täytetyn kysynnän kauden aloituspäivämäärä -kenttään päivämääräksi ja kellonajaksi 17.11.2012 9.00,00</span><span class="sxs-lookup"><span data-stu-id="f8018-118">In the Fulfilled demand period start date field, set the date and time to '2012-11-17T09:00:00'.</span></span>
    * <span data-ttu-id="f8018-119">Päivämäärä, josta alkaen aiemman kysynnän tapahtumat sisällytetään kanban-määrän laskentaan.</span><span class="sxs-lookup"><span data-stu-id="f8018-119">The date from when past demand transactions are included to calculate the kanban quantity.</span></span>  
8. <span data-ttu-id="f8018-120">Määritä Täytetyn kysynnän kauden päättymispäivämäärä -kenttään päivämääräksi ja kellonajaksi 17.12.2012 07.59,59.</span><span class="sxs-lookup"><span data-stu-id="f8018-120">In the Fulfilled demand period end date field, set the date and time to '2012-12-17T07:59:59'.</span></span>
    * <span data-ttu-id="f8018-121">Päivämäärä, johon asti aiemman kysynnän tapahtumat sisällytetään kanban-määrän laskentaan.</span><span class="sxs-lookup"><span data-stu-id="f8018-121">The date until when past demand transactions are included to calculate the kanban quantity.</span></span>  
9. <span data-ttu-id="f8018-122">Määritä Kysynnän kauden aloituspäivämäärä -kenttään päivämääräksi ja kellonajaksi 17.12.2012 8.00,00.</span><span class="sxs-lookup"><span data-stu-id="f8018-122">In the Demand period start date field, set the date and time to '2012-12-17T08:00:00'.</span></span>
    * <span data-ttu-id="f8018-123">Päivämäärä, josta alkaen kuluvan kysynnän tapahtumat sisällytetään kanban-määrän laskentaan.</span><span class="sxs-lookup"><span data-stu-id="f8018-123">The date from when current demand transactions are included to calculate the kanban quantity.</span></span>  
10. <span data-ttu-id="f8018-124">Määritä Kysynnän kauden lopetuspäivämäärä -kenttään päivämääräksi ja kellonajaksi 16.1.2012 07.59,59.</span><span class="sxs-lookup"><span data-stu-id="f8018-124">In the Demand period end date field, set the date and time to '2013-01-16T07:59:59'.</span></span>
    * <span data-ttu-id="f8018-125">Päivämäärä, johon asti kuluvan kysynnän tapahtumat sisällytetään kanban-määrän laskentaan.</span><span class="sxs-lookup"><span data-stu-id="f8018-125">The date until when current demand transactions are included to calculate the kanban quantity.</span></span>  

## <a name="generate-kanban-quantity-proposal"></a><span data-ttu-id="f8018-126">Kanban-määräehdotuksen luominen</span><span class="sxs-lookup"><span data-stu-id="f8018-126">Generate kanban quantity proposal</span></span>
1. <span data-ttu-id="f8018-127">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="f8018-127">Click Save.</span></span>
2. <span data-ttu-id="f8018-128">Valitse Luo.</span><span class="sxs-lookup"><span data-stu-id="f8018-128">Click Generate.</span></span>
    * <span data-ttu-id="f8018-129">Tämä luo kanban-säännölle 000020 kanban-määräehdotusrivin.</span><span class="sxs-lookup"><span data-stu-id="f8018-129">This generates a kanban quantity proposal line for the kanban rule 000020.</span></span>  

## <a name="run-kanban-quantity-calculation"></a><span data-ttu-id="f8018-130">Kanban-määrän laskelman suorittaminen</span><span class="sxs-lookup"><span data-stu-id="f8018-130">Run kanban quantity calculation</span></span>
1. <span data-ttu-id="f8018-131">Valitse Laske.</span><span class="sxs-lookup"><span data-stu-id="f8018-131">Click Calculate.</span></span>
    * <span data-ttu-id="f8018-132">Tässä lasketaan kanban-määräehdotus.</span><span class="sxs-lookup"><span data-stu-id="f8018-132">This calculates the kanban quantity proposal.</span></span>  
2. <span data-ttu-id="f8018-133">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="f8018-133">Click OK.</span></span>
3. <span data-ttu-id="f8018-134">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="f8018-134">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="f8018-135">Huomaa, että ehdotettu kanban-määrä on 2.</span><span class="sxs-lookup"><span data-stu-id="f8018-135">Notice the suggested kanban quantity is 2.</span></span>  

## <a name="change-product-quantity-and-calculate-again"></a><span data-ttu-id="f8018-136">Tuotemäärän muuttaminen ja laskeminen uudelleen</span><span class="sxs-lookup"><span data-stu-id="f8018-136">Change product quantity and calculate again</span></span>
1. <span data-ttu-id="f8018-137">Määritä tuotemääräksi 5.</span><span class="sxs-lookup"><span data-stu-id="f8018-137">Set Product quantity to '5'.</span></span>
2. <span data-ttu-id="f8018-138">Valitse Laske.</span><span class="sxs-lookup"><span data-stu-id="f8018-138">Click Calculate.</span></span>
3. <span data-ttu-id="f8018-139">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="f8018-139">Click OK.</span></span>
    * <span data-ttu-id="f8018-140">Huomaa, että jos kanban-määrä on 5, ehdotus muutetaan kanban-määräksi 4.</span><span class="sxs-lookup"><span data-stu-id="f8018-140">Notice that with a kanban quantity of 5, the suggestion is changed to a kanban quantity of 4.</span></span>  
    * <span data-ttu-id="f8018-141">Tämä johtuu siitä, että kun tuotemäärä on alempi, kysynnän täyttämiseksi tarvitaan enemmän kanbaneita.</span><span class="sxs-lookup"><span data-stu-id="f8018-141">This is caused by the fact that with a lower product quantity, we need more kanbans to fulfill the demand.</span></span>  

## <a name="update-kanban-rule"></a><span data-ttu-id="f8018-142">Kanban-säännön päivittäminen</span><span class="sxs-lookup"><span data-stu-id="f8018-142">Update kanban rule</span></span>
1. <span data-ttu-id="f8018-143">Syötä päivämäärä ja kellonaika Säännön voimaantulopäivämäärä -kenttään.</span><span class="sxs-lookup"><span data-stu-id="f8018-143">In the Rule effective date field, enter a date and time.</span></span>
    * <span data-ttu-id="f8018-144">Määritä Säännön voimassaolon alkupäivämäärä -kohdan arvoksi tuleva päivämäärä.</span><span class="sxs-lookup"><span data-stu-id="f8018-144">Set the 'Rule active as of date' to a date in the future.</span></span> <span data-ttu-id="f8018-145">Syötä arvoksi esimerkiksi kuluvan päivä + yksi vuosi.</span><span class="sxs-lookup"><span data-stu-id="f8018-145">For example, today + one year.</span></span>  
2. <span data-ttu-id="f8018-146">Valitse Päivitä.</span><span class="sxs-lookup"><span data-stu-id="f8018-146">Click Update.</span></span>
3. <span data-ttu-id="f8018-147">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="f8018-147">Click OK.</span></span>
4. <span data-ttu-id="f8018-148">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="f8018-148">Close the page.</span></span>

## <a name="validate-change-on-kanban-rule"></a><span data-ttu-id="f8018-149">Kanban-säännön muutoksen vahvistaminen</span><span class="sxs-lookup"><span data-stu-id="f8018-149">Validate change on kanban rule</span></span>
1. <span data-ttu-id="f8018-150">Siirry kohtaan Tuotetietojen hallinta > Lean-valmistus > Kanban-säännöt.</span><span class="sxs-lookup"><span data-stu-id="f8018-150">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
2. <span data-ttu-id="f8018-151">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="f8018-151">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="f8018-152">Valitse edellisessä alitehtävässä luotu kanban-sääntö.</span><span class="sxs-lookup"><span data-stu-id="f8018-152">Select the kanban rule that was created in the previous sub-task.</span></span> <span data-ttu-id="f8018-153">Tämän tulee olla numeroiden mukaan lajitellun luettelon ensimmäinen kanban-sääntö.</span><span class="sxs-lookup"><span data-stu-id="f8018-153">This should be the first kanban rule in the list sorted by number.</span></span>  
3. <span data-ttu-id="f8018-154">Ota käyttöön Tiedot-osan laajennus.</span><span class="sxs-lookup"><span data-stu-id="f8018-154">Toggle the expansion of the Details section.</span></span>
    * <span data-ttu-id="f8018-155">Ota huomioon voimaantulopäivä. Sääntö ei ole aktiivinen ennen tätä päivää.</span><span class="sxs-lookup"><span data-stu-id="f8018-155">Notice the effective date, which means that this rule is not activated until this date.</span></span>  
4. <span data-ttu-id="f8018-156">Ota käyttöön Määrät-osan laajennus.</span><span class="sxs-lookup"><span data-stu-id="f8018-156">Toggle the expansion of the Quantities section.</span></span>
    * <span data-ttu-id="f8018-157">Huomaa, että tämä on kanban-määrän laskelmassa syöttämäsi oletusmäärä.</span><span class="sxs-lookup"><span data-stu-id="f8018-157">Notice this is the default quantity that you entered on the kanban quantity calculation.</span></span>  
    * <span data-ttu-id="f8018-158">Huomaa, että tämä on kanban-määrän laskelman kiinteä kanban-määrä 4.</span><span class="sxs-lookup"><span data-stu-id="f8018-158">Notice this is the fixed kanban quantity of 4 from the kanban quantity calculation.</span></span>  
5. <span data-ttu-id="f8018-159">Valitse ListPanel-välilehti.</span><span class="sxs-lookup"><span data-stu-id="f8018-159">Click the ListPanel tab.</span></span>

