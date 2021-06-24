---
title: 'Opas: Perusennusteen luominen'
description: Tuotannon suunnittelija voi luoda perusennusteen aikasarjan ennustemallien avulla tai kopioimalla aiemman kysynnän.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ReqIntercompanyPlanningGroupSetup, ReqIntercompanyPlanningGroupAllocKeys, ReqDemPlanForecastParameters, ReqDemPlanCreateForecastDialog, SysQueryForm, ReqDemPlanForecastViewer
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 95a20b30827c9096dd8d8f67d149305cf594ff05
ms.sourcegitcommit: 15aacd0e109b05c7281407b5bba4e6cd99116c28
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/10/2021
ms.locfileid: "6223959"
---
# <a name="guide-create-a-baseline-forecast"></a><span data-ttu-id="475c7-103">Opas: Perusennusteen luominen</span><span class="sxs-lookup"><span data-stu-id="475c7-103">Guide: Create a baseline forecast</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="475c7-104">Tuotannon suunnittelija voi luoda perusennusteen aikasarjan ennustemallien avulla tai kopioimalla aiemman kysynnän.</span><span class="sxs-lookup"><span data-stu-id="475c7-104">A production planner can create a baseline forecast either by using time series forecast models or by copying the historical demand.</span></span> <span data-ttu-id="475c7-105">Tässä menettelyssä kerrotaan, miten perusennuste luodaan kaikille tuotteille yhden nimikkeen kohdistustunnuksen avulla niin, että aiempi kysyntä kopioidaan.</span><span class="sxs-lookup"><span data-stu-id="475c7-105">This procedure shows how to copy the historical demand to create a baseline forecast for all products using one item allocation key.</span></span>

## <a name="set-up-an-item-allocation-key"></a><span data-ttu-id="475c7-106">Nimikkeenkohdistustunnuksen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="475c7-106">Set up an item allocation key</span></span>

1. <span data-ttu-id="475c7-107">Siirry kohtaan **Pääsuunnittelu > Asetukset > Konsernin sisäiset suunnitteluryhmät**.</span><span class="sxs-lookup"><span data-stu-id="475c7-107">Go to **Master planning > Setup > Intercompany planning groups**.</span></span>
2. <span data-ttu-id="475c7-108">Käytä pikasuodatinta tietueiden etsimiseen.</span><span class="sxs-lookup"><span data-stu-id="475c7-108">Use the Quick Filter to find records.</span></span> <span data-ttu-id="475c7-109">Voit esimerkiksi suodattaa *Nimi*-kenttää arvolla *10*.</span><span class="sxs-lookup"><span data-stu-id="475c7-109">For example, filter on the *Name* field with a value of *10*.</span></span>
    * <span data-ttu-id="475c7-110">Kysynnän ennuste suoritetaan kaikille yrityksille.</span><span class="sxs-lookup"><span data-stu-id="475c7-110">Demand forecasting runs across legal entities.</span></span> <span data-ttu-id="475c7-111">Tämän vuoksi on määritettävä kaikki yritykset, joille haluat luoda ennusteet yhdessä konsernin sisäisen suunnitteluryhmässä.</span><span class="sxs-lookup"><span data-stu-id="475c7-111">That's why you need to set up all the companies for which you want to generate forecasts in one intercompany planning group.</span></span>  
3. <span data-ttu-id="475c7-112">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="475c7-112">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="475c7-113">Valitse **Nimikkeen kohdistustunnukset**.</span><span class="sxs-lookup"><span data-stu-id="475c7-113">Select **Item allocation keys**.</span></span>
    * <span data-ttu-id="475c7-114">Valitse kaikki nimikkeen kohdistustunnukset, joille haluat luoda ennusteet.</span><span class="sxs-lookup"><span data-stu-id="475c7-114">Select all the item allocation keys for which you want to create forecasts.</span></span>  
5. <span data-ttu-id="475c7-115">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="475c7-115">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="475c7-116">Valitse nimikkeen kohdistustunnus D_Aloc.</span><span class="sxs-lookup"><span data-stu-id="475c7-116">Select D_Aloc item allocation key.</span></span>  
6. <span data-ttu-id="475c7-117">Valitse **>**.</span><span class="sxs-lookup"><span data-stu-id="475c7-117">Select **>**.</span></span>
7. <span data-ttu-id="475c7-118">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="475c7-118">Close the page.</span></span>
8. <span data-ttu-id="475c7-119">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="475c7-119">Close the page.</span></span>

## <a name="set-up-the-demand-forecasting-parameters"></a><span data-ttu-id="475c7-120">Kysynnän ennusteen parametrien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="475c7-120">Set up the demand forecasting parameters</span></span>

1. <span data-ttu-id="475c7-121">Siirry kohtaan **Pääsuunnittelu > Asetukset > Kysynnän ennuste > Kysynnän ennusteen parametrit**.</span><span class="sxs-lookup"><span data-stu-id="475c7-121">Go to **Master planning > Setup > Demand forecasting > Demand forecasting parameters**.</span></span>
2. <span data-ttu-id="475c7-122">Laajenna **Ennustealgoritmin parametrit** -osa.</span><span class="sxs-lookup"><span data-stu-id="475c7-122">Expand the **Forecast algorithm parameters** section.</span></span>
3. <span data-ttu-id="475c7-123">Valitse **Kysynnän luontistrategia** -kentässä **Kopioi historiallisen kysynnän päälle**.</span><span class="sxs-lookup"><span data-stu-id="475c7-123">In the **Forecast generation strategy** field, select **Copy over historical demand**.</span></span>
4. <span data-ttu-id="475c7-124">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="475c7-124">Select **Save**.</span></span>

## <a name="create-a-baseline-forecast"></a><span data-ttu-id="475c7-125">Perusennusteen luominen</span><span class="sxs-lookup"><span data-stu-id="475c7-125">Create a baseline forecast</span></span>

1. <span data-ttu-id="475c7-126">Siirry **kohtaan Pääsuunnittelu > Ennuste > Kysynnän ennuste > Luo tilastollinen perusennuste**.</span><span class="sxs-lookup"><span data-stu-id="475c7-126">Go to **Master planning > Forecasting > Demand forecasting > Generate statistical baseline forecast**.</span></span>
2. <span data-ttu-id="475c7-127">Syötä päivämäärä **Päivämäärästä**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="475c7-127">In the **From date** field, enter a date.</span></span>
    * <span data-ttu-id="475c7-128">Jos olemassa on myyntitilauksia, jotka alkavat 1.1.2015, syötä tämä päivämäärä.</span><span class="sxs-lookup"><span data-stu-id="475c7-128">If you have sales orders starting from January 1, 2015, enter this date.</span></span> <span data-ttu-id="475c7-129">Jos päivämäärä ei ole oikea, syötä ensimmäisen myyntitilauksen päivämäärä.</span><span class="sxs-lookup"><span data-stu-id="475c7-129">If you don't, enter the earliest date of your sales orders.</span></span>  
3. <span data-ttu-id="475c7-130">Kirjoita päivämäärä **Päivämäärään**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="475c7-130">In the **To date** field, enter a date.</span></span>
    * <span data-ttu-id="475c7-131">Syötä myyntitilausten viimeinen päivämäärä, esimerkiksi *2015-03-31*.</span><span class="sxs-lookup"><span data-stu-id="475c7-131">Enter the last date of your sales orders, for example *2015-03-31*.</span></span>  
4. <span data-ttu-id="475c7-132">Syötä päivämäärä **Päivämäärästä**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="475c7-132">In the **From date** field, enter a date.</span></span>
    * <span data-ttu-id="475c7-133">Syötä *2015-04-01*.</span><span class="sxs-lookup"><span data-stu-id="475c7-133">Enter *2015-04-01*.</span></span> <span data-ttu-id="475c7-134">Tämä päivämäärä lasketaan automaattisesti seuraavan ennustejakson alkupäivänä.</span><span class="sxs-lookup"><span data-stu-id="475c7-134">This date will be automatically calculated as the start date of the next forecasting bucket.</span></span>  
5. <span data-ttu-id="475c7-135">Laajenna **Sisällytettävät tietueet** -osa.</span><span class="sxs-lookup"><span data-stu-id="475c7-135">Expand the **Records to include** section.</span></span>
6. <span data-ttu-id="475c7-136">Valitse **Suodata**.</span><span class="sxs-lookup"><span data-stu-id="475c7-136">Select **Filter**.</span></span>
7. <span data-ttu-id="475c7-137">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="475c7-137">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="475c7-138">Merkitse rivi, jossa **Kenttä** = *Konsernin sisäinen suunnitteluryhmä*.</span><span class="sxs-lookup"><span data-stu-id="475c7-138">Mark the row where **Field** = *Intercompany planning group*.</span></span>  
8. <span data-ttu-id="475c7-139">Kirjoita arvo **Ehdot**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="475c7-139">In the **Criteria** field, type a value.</span></span>
    * <span data-ttu-id="475c7-140">Syötä konsernin sisäinen suunnitteluryhmä (esimerkiksi *10*), jota käytettiin ensimmäisessä tehtävässä.</span><span class="sxs-lookup"><span data-stu-id="475c7-140">Type the intercompany planning group (for example, *10*) that you used in the first task.</span></span>  
9. <span data-ttu-id="475c7-141">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="475c7-141">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="475c7-142">Valitse rivi, jossa **Kenttä** = *Nimikkeen kohdistustunnus*.</span><span class="sxs-lookup"><span data-stu-id="475c7-142">Select the row where **Field** = *Item allocation key*.</span></span>  
10. <span data-ttu-id="475c7-143">Kirjoita arvo **Ehdot**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="475c7-143">In the **Criteria** field, type a value.</span></span>
11. <span data-ttu-id="475c7-144">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="475c7-144">Select **OK**.</span></span>
12. <span data-ttu-id="475c7-145">Laajenna **Lisäparametrit**-osa.</span><span class="sxs-lookup"><span data-stu-id="475c7-145">Expand the **Advanced parameters** section.</span></span>
13. <span data-ttu-id="475c7-146">Valitse **Ennustejakso**-kentässä *Kuukausi*.</span><span class="sxs-lookup"><span data-stu-id="475c7-146">In the **Forecast bucket** field, select *Month*.</span></span>
14. <span data-ttu-id="475c7-147">Syötä **Ennustehorisontti**-kenttään *3*.</span><span class="sxs-lookup"><span data-stu-id="475c7-147">In the **Forecast horizon** field, enter *3*.</span></span>
15. <span data-ttu-id="475c7-148">Syötä **Lukitusaikaraja**-kenttään *1*.</span><span class="sxs-lookup"><span data-stu-id="475c7-148">In the **Freeze time fence** field, enter *1*.</span></span>
16. <span data-ttu-id="475c7-149">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="475c7-149">Select **OK**.</span></span>

## <a name="visualize-the-demand-forecast"></a><span data-ttu-id="475c7-150">Kysynnän ennusteen havainnollistaminen</span><span class="sxs-lookup"><span data-stu-id="475c7-150">Visualize the demand forecast</span></span>

1. <span data-ttu-id="475c7-151">Siirry kohtaan **Pääsuunnittelu > Ennuste > Kysynnän ennuste > Oikaistu kysynnän ennuste**.</span><span class="sxs-lookup"><span data-stu-id="475c7-151">Go to **Master planning > Forecasting > Demand forecasting > Adjusted demand forecast**.</span></span>
2. <span data-ttu-id="475c7-152">Valitse koostenäkymätaulussa rivin 1 ja sarakkeen 2 solu.</span><span class="sxs-lookup"><span data-stu-id="475c7-152">In the aggregated view table, select the cell in row 1, column 2.</span></span> <span data-ttu-id="475c7-153">Tämä on toinen kuukausi, jolle ennuste on luotu.</span><span class="sxs-lookup"><span data-stu-id="475c7-153">This is the second month for which you have created forecast.</span></span>
3. <span data-ttu-id="475c7-154">Määritä **QtyCell**-kohdan arvoksi *400*.</span><span class="sxs-lookup"><span data-stu-id="475c7-154">Set **QtyCell** to *400*.</span></span>
    * <span data-ttu-id="475c7-155">Syötä soluun numero, joka on eri kuin ennustettu numero. Voit syöttää arvoksi esimerkiksi 400.</span><span class="sxs-lookup"><span data-stu-id="475c7-155">In the cell, enter a different number than the one that was forecasted, for example, 400.</span></span>  
4. <span data-ttu-id="475c7-156">Olet tehnyt ennusteeseen manuaalisen oikaisun.</span><span class="sxs-lookup"><span data-stu-id="475c7-156">You have made a manual adjustment to the forecast.</span></span> <span data-ttu-id="475c7-157">Huomaa seuraavassa vaiheessa oleva graafinen tunnus.</span><span class="sxs-lookup"><span data-stu-id="475c7-157">Notice the graphical indication in the next step.</span></span>
5. <span data-ttu-id="475c7-158">Valitse **Ennusteen rivitiedot**.</span><span class="sxs-lookup"><span data-stu-id="475c7-158">Select **Forecast line details**.</span></span>
    * <span data-ttu-id="475c7-159">Tällä sivulla näkyvät tarkkuusarvot, aiempi kysyntä ja ennuste.</span><span class="sxs-lookup"><span data-stu-id="475c7-159">In this page, you can see the accuracy values, historical demand, and forecast.</span></span> <span data-ttu-id="475c7-160">Voit muuttaa myös ennustetta.</span><span class="sxs-lookup"><span data-stu-id="475c7-160">You can make changes to the forecast as well.</span></span>  

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]