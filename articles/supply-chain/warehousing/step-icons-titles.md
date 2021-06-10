---
title: Warehouse Management -mobiilisovelluksen vaihekuvakkeiden ja otsikoiden määrittäminen
description: Tässä aiheessa kuvataan, miten määritetään Warehouse Managementin mobiilisovelluksen uusien tai mukautettujen tehtävävirtojen vaihekuvakkeet ja otsikot.
author: MarkusFogelberg
ms.date: 05/17/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2021-05-17
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 9523492d766669e6c38579fba7b5ddd6b3d282fc
ms.sourcegitcommit: c53de2c09b9296b41653e739178edf29f79e0679
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/17/2021
ms.locfileid: "6049361"
---
# <a name="assign-step-icons-and-titles-for-the-warehouse-management-mobile-app"></a><span data-ttu-id="d0194-103">Warehouse Management -mobiilisovelluksen vaihekuvakkeiden ja otsikoiden määrittäminen</span><span class="sxs-lookup"><span data-stu-id="d0194-103">Assign step icons and titles for the Warehouse Management mobile app</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d0194-104">Tässä aiheessa kuvataan, miten määritetään Warehouse Managementin mobiilisovelluksen uusien tai mukautettujen tehtävävirtojen vaihekuvakkeet ja vaiheiden otsikot.</span><span class="sxs-lookup"><span data-stu-id="d0194-104">This topic describes how to assign step icons and step titles for new or customized task flows for the Warehouse Management mobile app.</span></span>

<span data-ttu-id="d0194-105">Seuraavissa kuvissa näytetään, miten vaihekuvakkeet ja otsikot näkyvät Warehouse Management -mobiilisovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="d0194-105">The following illustrations shows how step icons and titles appear in the Warehouse Management mobile app.</span></span>

<span data-ttu-id="d0194-106">![Esimerkki vaihekuvakkeesta ja vaiheen otsikosta Warehouse Management -mobiilisovelluksessa](media/step-icon-example.png "Esimerkki vaihekuvakkeesta ja vaiheen otsikosta Warehouse Management -mobiilisovelluksessa")</span><span class="sxs-lookup"><span data-stu-id="d0194-106">![Example of a step icon and a step title in the Warehouse Management mobile app](media/step-icon-example.png "Example of a step icon and a step title in the Warehouse Management mobile app")</span></span>

## <a name="turn-on-this-feature-in-your-system"></a><span data-ttu-id="d0194-107">Tämän toiminnon ottaminen käyttöön järjestelmässä</span><span class="sxs-lookup"><span data-stu-id="d0194-107">Turn on this feature in your system</span></span>

<span data-ttu-id="d0194-108">Ennen kuin käytät tätä toimintoa, sen on oltava päällä järjestelmässäsi.</span><span class="sxs-lookup"><span data-stu-id="d0194-108">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="d0194-109">Järjestelmänvalvojat voivat tarkistaa toiminnon tilan ja ottaa sen käyttöön [ominaisuuksien hallinnan](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) asetusten avulla.</span><span class="sxs-lookup"><span data-stu-id="d0194-109">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="d0194-110">**Ominaisuuksien hallinta** -työtilassa ominaisuus on luetteloitu seuraavalla tavalla:</span><span class="sxs-lookup"><span data-stu-id="d0194-110">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="d0194-111">**Moduuli:** *Varastonhallinta*</span><span class="sxs-lookup"><span data-stu-id="d0194-111">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="d0194-112">**Toiminnon nimi:** *Uuden varastointisovelluksen käyttäjäasetukset, kuvakkeet ja vaiheiden otsikot*</span><span class="sxs-lookup"><span data-stu-id="d0194-112">**Feature name:** *User settings, icons, and step titles for the new warehouse app*</span></span>

## <a name="standard-step-ids-classes-and-icons"></a><span data-ttu-id="d0194-113">Vakiovaihetunnukset, -luokat ja -kuvakkeet</span><span class="sxs-lookup"><span data-stu-id="d0194-113">Standard step IDs, classes, and icons</span></span>

<span data-ttu-id="d0194-114">Jokainen tehtävätyönkulun vaihe on määritetty vaiheen tunnuksen perusteella, ja kullakin vaiheen tunnuksella on vastaava vaiheluokka.</span><span class="sxs-lookup"><span data-stu-id="d0194-114">Each step in a task flow is identified by a step ID, and each step ID has a corresponding step class.</span></span> <span data-ttu-id="d0194-115">Vaihekuvake ja otsikko määritetään jokaisessa vaiheen luokassa.</span><span class="sxs-lookup"><span data-stu-id="d0194-115">The step icon and title are specified in each step class.</span></span>

### <a name="step-ids-and-step-classes"></a><a name="step-ids-classes"></a><span data-ttu-id="d0194-116">Vaihetunnukset ja vaiheluokat</span><span class="sxs-lookup"><span data-stu-id="d0194-116">Step IDs and step classes</span></span>

<span data-ttu-id="d0194-117">Seuraavassa taulukossa luetellaan kaikki käytettävissä olevat vaihetunnukset, ja vaiheluokka on sitä vastaava.</span><span class="sxs-lookup"><span data-stu-id="d0194-117">The following table lists every step ID that is currently available, and its corresponding step class.</span></span> <span data-ttu-id="d0194-118">Ensisijaisen syöttökentän ohjausobjektin nimeä käytetään vaiheen tunnuksena.</span><span class="sxs-lookup"><span data-stu-id="d0194-118">The control name of the primary input field is used as the step ID.</span></span>

<span data-ttu-id="d0194-119">Katso esimerkki `WHSMobileAppStepInfoBuilder.stepId()` -menetelmän toteutuksesta, joka osoittaa, kuinka näitä vaihetunnuksia ja luokkia käytetään on kohdassa [Esimerkki: Vaihekuvakkeiden ja otsikoiden määrittäminen muokatulle työnkululle](#example) jäljempänä tässä ohjeaiheessa.</span><span class="sxs-lookup"><span data-stu-id="d0194-119">For an example that shows how these step IDs and classes are used, see the implementation of the `WHSMobileAppStepInfoBuilder.stepId()` method in the [Example: Assign step icons and titles for a custom flow](#example) section later in this topic.</span></span>

| <span data-ttu-id="d0194-120">Vaihetunnus</span><span class="sxs-lookup"><span data-stu-id="d0194-120">Step ID</span></span> | <span data-ttu-id="d0194-121">Vaiheluokka</span><span class="sxs-lookup"><span data-stu-id="d0194-121">Step Class</span></span> |
|-|-|
| <span data-ttu-id="d0194-122">BatchDisposition</span><span class="sxs-lookup"><span data-stu-id="d0194-122">BatchDisposition</span></span> | <span data-ttu-id="d0194-123">WHSMobileAppStepBatchDisposition</span><span class="sxs-lookup"><span data-stu-id="d0194-123">WHSMobileAppStepBatchDisposition</span></span> |
| <span data-ttu-id="d0194-124">Rahdinkuljettaja</span><span class="sxs-lookup"><span data-stu-id="d0194-124">Carrier</span></span> | <span data-ttu-id="d0194-125">WHSMobileAppStepCarrier</span><span class="sxs-lookup"><span data-stu-id="d0194-125">WHSMobileAppStepCarrier</span></span> |
| <span data-ttu-id="d0194-126">CatchWeight</span><span class="sxs-lookup"><span data-stu-id="d0194-126">CatchWeight</span></span> | <span data-ttu-id="d0194-127">WHSMobileAppStepCatchWeight</span><span class="sxs-lookup"><span data-stu-id="d0194-127">WHSMobileAppStepCatchWeight</span></span> |
| <span data-ttu-id="d0194-128">CatchWeightQtyOutboundWeight</span><span class="sxs-lookup"><span data-stu-id="d0194-128">CatchWeightQtyOutboundWeight</span></span> | <span data-ttu-id="d0194-129">WHSMobileAppStepCatchWeight</span><span class="sxs-lookup"><span data-stu-id="d0194-129">WHSMobileAppStepCatchWeight</span></span> |
| <span data-ttu-id="d0194-130">CatchWeightTag</span><span class="sxs-lookup"><span data-stu-id="d0194-130">CatchWeightTag</span></span> | <span data-ttu-id="d0194-131">WHSMobileAppStepCatchWeightTag</span><span class="sxs-lookup"><span data-stu-id="d0194-131">WHSMobileAppStepCatchWeightTag</span></span> |
| <span data-ttu-id="d0194-132">CatchWeightTagWeight</span><span class="sxs-lookup"><span data-stu-id="d0194-132">CatchWeightTagWeight</span></span> | <span data-ttu-id="d0194-133">WHSMobileAppStepCatchWeightTagWeight</span><span class="sxs-lookup"><span data-stu-id="d0194-133">WHSMobileAppStepCatchWeightTagWeight</span></span> |
| <span data-ttu-id="d0194-134">ChangeWarehouseSuccess</span><span class="sxs-lookup"><span data-stu-id="d0194-134">ChangeWarehouseSuccess</span></span> | <span data-ttu-id="d0194-135">WHSMobileAppStepChangeWarehouseSuccess</span><span class="sxs-lookup"><span data-stu-id="d0194-135">WHSMobileAppStepChangeWarehouseSuccess</span></span> |
| <span data-ttu-id="d0194-136">CheckDigit</span><span class="sxs-lookup"><span data-stu-id="d0194-136">CheckDigit</span></span> | <span data-ttu-id="d0194-137">WHSMobileAppStepCheckDigit</span><span class="sxs-lookup"><span data-stu-id="d0194-137">WHSMobileAppStepCheckDigit</span></span> |
| <span data-ttu-id="d0194-138">ClusterId</span><span class="sxs-lookup"><span data-stu-id="d0194-138">ClusterId</span></span> | <span data-ttu-id="d0194-139">WHSMobileAppStepClusterId</span><span class="sxs-lookup"><span data-stu-id="d0194-139">WHSMobileAppStepClusterId</span></span> |
| <span data-ttu-id="d0194-140">ClusterPickQtyVerification</span><span class="sxs-lookup"><span data-stu-id="d0194-140">ClusterPickQtyVerification</span></span> | <span data-ttu-id="d0194-141">WHSMobileAppStepQtyVerification</span><span class="sxs-lookup"><span data-stu-id="d0194-141">WHSMobileAppStepQtyVerification</span></span> |
| <span data-ttu-id="d0194-142">ClusterPosition</span><span class="sxs-lookup"><span data-stu-id="d0194-142">ClusterPosition</span></span> | <span data-ttu-id="d0194-143">WHSMobileAppStepClusterPosition</span><span class="sxs-lookup"><span data-stu-id="d0194-143">WHSMobileAppStepClusterPosition</span></span> |
| <span data-ttu-id="d0194-144">ConfigId</span><span class="sxs-lookup"><span data-stu-id="d0194-144">ConfigId</span></span> | <span data-ttu-id="d0194-145">WHSMobileAppStepConfigId</span><span class="sxs-lookup"><span data-stu-id="d0194-145">WHSMobileAppStepConfigId</span></span> |
| <span data-ttu-id="d0194-146">Vahvistus</span><span class="sxs-lookup"><span data-stu-id="d0194-146">Confirmation</span></span> | <span data-ttu-id="d0194-147">WHSMobileAppStepConfirmation</span><span class="sxs-lookup"><span data-stu-id="d0194-147">WHSMobileAppStepConfirmation</span></span> |
| <span data-ttu-id="d0194-148">ConsolidateFromLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="d0194-148">ConsolidateFromLicensePlateId</span></span> | <span data-ttu-id="d0194-149">WHSMobileAppStepConsolidateFromLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="d0194-149">WHSMobileAppStepConsolidateFromLicensePlateId</span></span> |
| <span data-ttu-id="d0194-150">ConsolidateLPConfirmation</span><span class="sxs-lookup"><span data-stu-id="d0194-150">ConsolidateLPConfirmation</span></span> | <span data-ttu-id="d0194-151">WHSMobileAppStepConsolidateLPConfirmation</span><span class="sxs-lookup"><span data-stu-id="d0194-151">WHSMobileAppStepConsolidateLPConfirmation</span></span> |
| <span data-ttu-id="d0194-152">ConsolidateToLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="d0194-152">ConsolidateToLicensePlateId</span></span> | <span data-ttu-id="d0194-153">WHSMobileAppStepConsolidateToLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="d0194-153">WHSMobileAppStepConsolidateToLicensePlateId</span></span> |
| <span data-ttu-id="d0194-154">ContainerType</span><span class="sxs-lookup"><span data-stu-id="d0194-154">ContainerType</span></span> | <span data-ttu-id="d0194-155">WHSMobileAppStepContainerType</span><span class="sxs-lookup"><span data-stu-id="d0194-155">WHSMobileAppStepContainerType</span></span> |
| <span data-ttu-id="d0194-156">CountingReasonCode</span><span class="sxs-lookup"><span data-stu-id="d0194-156">CountingReasonCode</span></span> | <span data-ttu-id="d0194-157">WHSMobileAppStepCountingReasonCode</span><span class="sxs-lookup"><span data-stu-id="d0194-157">WHSMobileAppStepCountingReasonCode</span></span> |
| <span data-ttu-id="d0194-158">CycleCountingAddLPOrFinish</span><span class="sxs-lookup"><span data-stu-id="d0194-158">CycleCountingAddLPOrFinish</span></span> | <span data-ttu-id="d0194-159">WHSMobileAppStepCycleCountingAddLPOrFinish</span><span class="sxs-lookup"><span data-stu-id="d0194-159">WHSMobileAppStepCycleCountingAddLPOrFinish</span></span> |
| <span data-ttu-id="d0194-160">CycleCountQty1</span><span class="sxs-lookup"><span data-stu-id="d0194-160">CycleCountQty1</span></span> | <span data-ttu-id="d0194-161">WHSMobileAppStepCycleCountQty</span><span class="sxs-lookup"><span data-stu-id="d0194-161">WHSMobileAppStepCycleCountQty</span></span> |
| <span data-ttu-id="d0194-162">CycleCountQty2</span><span class="sxs-lookup"><span data-stu-id="d0194-162">CycleCountQty2</span></span> | <span data-ttu-id="d0194-163">WHSMobileAppStepCycleCountQty</span><span class="sxs-lookup"><span data-stu-id="d0194-163">WHSMobileAppStepCycleCountQty</span></span> |
| <span data-ttu-id="d0194-164">CycleCountQty3</span><span class="sxs-lookup"><span data-stu-id="d0194-164">CycleCountQty3</span></span> | <span data-ttu-id="d0194-165">WHSMobileAppStepCycleCountQty</span><span class="sxs-lookup"><span data-stu-id="d0194-165">WHSMobileAppStepCycleCountQty</span></span> |
| <span data-ttu-id="d0194-166">CycleCountQty4</span><span class="sxs-lookup"><span data-stu-id="d0194-166">CycleCountQty4</span></span> | <span data-ttu-id="d0194-167">WHSMobileAppStepCycleCountQty</span><span class="sxs-lookup"><span data-stu-id="d0194-167">WHSMobileAppStepCycleCountQty</span></span> |
| <span data-ttu-id="d0194-168">Käsittely</span><span class="sxs-lookup"><span data-stu-id="d0194-168">Disposition</span></span> | <span data-ttu-id="d0194-169">WHSMobileAppStepDisposition</span><span class="sxs-lookup"><span data-stu-id="d0194-169">WHSMobileAppStepDisposition</span></span> |
| <span data-ttu-id="d0194-170">DriverCheckInConfirmation</span><span class="sxs-lookup"><span data-stu-id="d0194-170">DriverCheckInConfirmation</span></span> | <span data-ttu-id="d0194-171">WHSMobileAppStepDriverCheckInConfirmation</span><span class="sxs-lookup"><span data-stu-id="d0194-171">WHSMobileAppStepDriverCheckInConfirmation</span></span> |
| <span data-ttu-id="d0194-172">DriverCheckInId</span><span class="sxs-lookup"><span data-stu-id="d0194-172">DriverCheckInId</span></span> | <span data-ttu-id="d0194-173">WHSMobileAppStepDriverCheckInId</span><span class="sxs-lookup"><span data-stu-id="d0194-173">WHSMobileAppStepDriverCheckInId</span></span> |
| <span data-ttu-id="d0194-174">DriverCheckOutConfirmation</span><span class="sxs-lookup"><span data-stu-id="d0194-174">DriverCheckOutConfirmation</span></span> | <span data-ttu-id="d0194-175">WHSMobileAppStepDriverCheckOutConfirmation</span><span class="sxs-lookup"><span data-stu-id="d0194-175">WHSMobileAppStepDriverCheckOutConfirmation</span></span> |
| <span data-ttu-id="d0194-176">DriverCheckOutId</span><span class="sxs-lookup"><span data-stu-id="d0194-176">DriverCheckOutId</span></span> | <span data-ttu-id="d0194-177">WHSMobileAppStepDriverCheckOutId</span><span class="sxs-lookup"><span data-stu-id="d0194-177">WHSMobileAppStepDriverCheckOutId</span></span> |
| <span data-ttu-id="d0194-178">ExpDate</span><span class="sxs-lookup"><span data-stu-id="d0194-178">ExpDate</span></span> | <span data-ttu-id="d0194-179">WHSMobileAppStepExpDate</span><span class="sxs-lookup"><span data-stu-id="d0194-179">WHSMobileAppStepExpDate</span></span> |
| <span data-ttu-id="d0194-180">FromBatchDisposition</span><span class="sxs-lookup"><span data-stu-id="d0194-180">FromBatchDisposition</span></span> | <span data-ttu-id="d0194-181">WHSMobileAppStepFromBatchDisposition</span><span class="sxs-lookup"><span data-stu-id="d0194-181">WHSMobileAppStepFromBatchDisposition</span></span> |
| <span data-ttu-id="d0194-182">FromInventoryStatus</span><span class="sxs-lookup"><span data-stu-id="d0194-182">FromInventoryStatus</span></span> | <span data-ttu-id="d0194-183">WHSMobileAppStepInventoryStatusFrom</span><span class="sxs-lookup"><span data-stu-id="d0194-183">WHSMobileAppStepInventoryStatusFrom</span></span> |
| <span data-ttu-id="d0194-184">FullQty</span><span class="sxs-lookup"><span data-stu-id="d0194-184">FullQty</span></span> | <span data-ttu-id="d0194-185">WHSMobileAppStepFullQty</span><span class="sxs-lookup"><span data-stu-id="d0194-185">WHSMobileAppStepFullQty</span></span> |
| <span data-ttu-id="d0194-186">InboundPut</span><span class="sxs-lookup"><span data-stu-id="d0194-186">InboundPut</span></span> | <span data-ttu-id="d0194-187">WHSMobileAppStepInboundPut</span><span class="sxs-lookup"><span data-stu-id="d0194-187">WHSMobileAppStepInboundPut</span></span> |
| <span data-ttu-id="d0194-188">InventBatchId</span><span class="sxs-lookup"><span data-stu-id="d0194-188">InventBatchId</span></span> | <span data-ttu-id="d0194-189">WHSMobileAppStepBatch</span><span class="sxs-lookup"><span data-stu-id="d0194-189">WHSMobileAppStepBatch</span></span> |
| <span data-ttu-id="d0194-190">InventColorId</span><span class="sxs-lookup"><span data-stu-id="d0194-190">InventColorId</span></span> | <span data-ttu-id="d0194-191">WHSMobileAppStepInventColorId</span><span class="sxs-lookup"><span data-stu-id="d0194-191">WHSMobileAppStepInventColorId</span></span> |
| <span data-ttu-id="d0194-192">InventLocation</span><span class="sxs-lookup"><span data-stu-id="d0194-192">InventLocation</span></span> | <span data-ttu-id="d0194-193">WHSMobileAppStepInventLocation</span><span class="sxs-lookup"><span data-stu-id="d0194-193">WHSMobileAppStepInventLocation</span></span> |
| <span data-ttu-id="d0194-194">InventLocationId</span><span class="sxs-lookup"><span data-stu-id="d0194-194">InventLocationId</span></span> | <span data-ttu-id="d0194-195">WHSMobileAppStepWarehouse</span><span class="sxs-lookup"><span data-stu-id="d0194-195">WHSMobileAppStepWarehouse</span></span> |
| <span data-ttu-id="d0194-196">InventSerialId</span><span class="sxs-lookup"><span data-stu-id="d0194-196">InventSerialId</span></span> | <span data-ttu-id="d0194-197">WHSMobileAppStepInventSerialId</span><span class="sxs-lookup"><span data-stu-id="d0194-197">WHSMobileAppStepInventSerialId</span></span> |
| <span data-ttu-id="d0194-198">InventSizeId</span><span class="sxs-lookup"><span data-stu-id="d0194-198">InventSizeId</span></span> | <span data-ttu-id="d0194-199">WHSMobileAppStepInventSizeId</span><span class="sxs-lookup"><span data-stu-id="d0194-199">WHSMobileAppStepInventSizeId</span></span> |
| <span data-ttu-id="d0194-200">InventStatusId</span><span class="sxs-lookup"><span data-stu-id="d0194-200">InventStatusId</span></span> | <span data-ttu-id="d0194-201">WHSMobileAppStepInventStatus</span><span class="sxs-lookup"><span data-stu-id="d0194-201">WHSMobileAppStepInventStatus</span></span> |
| <span data-ttu-id="d0194-202">InventStyleId</span><span class="sxs-lookup"><span data-stu-id="d0194-202">InventStyleId</span></span> | <span data-ttu-id="d0194-203">WHSMobileAppStepInventStyleId</span><span class="sxs-lookup"><span data-stu-id="d0194-203">WHSMobileAppStepInventStyleId</span></span> |
| <span data-ttu-id="d0194-204">InventVersionId</span><span class="sxs-lookup"><span data-stu-id="d0194-204">InventVersionId</span></span> | <span data-ttu-id="d0194-205">WHSMobileAppStepInventVersionId</span><span class="sxs-lookup"><span data-stu-id="d0194-205">WHSMobileAppStepInventVersionId</span></span> |
| <span data-ttu-id="d0194-206">ItemId</span><span class="sxs-lookup"><span data-stu-id="d0194-206">ItemId</span></span> | <span data-ttu-id="d0194-207">WHSMobileAppStepItem</span><span class="sxs-lookup"><span data-stu-id="d0194-207">WHSMobileAppStepItem</span></span> |
| <span data-ttu-id="d0194-208">ITMContainerID</span><span class="sxs-lookup"><span data-stu-id="d0194-208">ITMContainerID</span></span> | <span data-ttu-id="d0194-209">ITMMobileAppStepContainerId</span><span class="sxs-lookup"><span data-stu-id="d0194-209">ITMMobileAppStepContainerId</span></span> |
| <span data-ttu-id="d0194-210">ITMShipmentID</span><span class="sxs-lookup"><span data-stu-id="d0194-210">ITMShipmentID</span></span> | <span data-ttu-id="d0194-211">ITMMobileAppStepShipmentId</span><span class="sxs-lookup"><span data-stu-id="d0194-211">ITMMobileAppStepShipmentId</span></span> |
| <span data-ttu-id="d0194-212">KanbanCardId</span><span class="sxs-lookup"><span data-stu-id="d0194-212">KanbanCardId</span></span> | <span data-ttu-id="d0194-213">WHSMobileAppStepKanbanCard</span><span class="sxs-lookup"><span data-stu-id="d0194-213">WHSMobileAppStepKanbanCard</span></span> |
| <span data-ttu-id="d0194-214">KanbanCardToEmpty</span><span class="sxs-lookup"><span data-stu-id="d0194-214">KanbanCardToEmpty</span></span> | <span data-ttu-id="d0194-215">WHSMobileAppStepKanbanCardToEmpty</span><span class="sxs-lookup"><span data-stu-id="d0194-215">WHSMobileAppStepKanbanCardToEmpty</span></span> |
| <span data-ttu-id="d0194-216">KanbanOrCardId</span><span class="sxs-lookup"><span data-stu-id="d0194-216">KanbanOrCardId</span></span> | <span data-ttu-id="d0194-217">WHSMobileAppStepKanbanCard</span><span class="sxs-lookup"><span data-stu-id="d0194-217">WHSMobileAppStepKanbanCard</span></span> |
| <span data-ttu-id="d0194-218">LicensePlateId</span><span class="sxs-lookup"><span data-stu-id="d0194-218">LicensePlateId</span></span> | <span data-ttu-id="d0194-219">WHSMobileAppStepLicensePlate</span><span class="sxs-lookup"><span data-stu-id="d0194-219">WHSMobileAppStepLicensePlate</span></span> |
| <span data-ttu-id="d0194-220">LoadId</span><span class="sxs-lookup"><span data-stu-id="d0194-220">LoadId</span></span> | <span data-ttu-id="d0194-221">WHSMobileAppStepLoadId</span><span class="sxs-lookup"><span data-stu-id="d0194-221">WHSMobileAppStepLoadId</span></span> |
| <span data-ttu-id="d0194-222">LocationLicensePlatePosition</span><span class="sxs-lookup"><span data-stu-id="d0194-222">LocationLicensePlatePosition</span></span> | <span data-ttu-id="d0194-223">WHSMobileAppStepLocationLicensePlatePosition</span><span class="sxs-lookup"><span data-stu-id="d0194-223">WHSMobileAppStepLocationLicensePlatePosition</span></span> |
| <span data-ttu-id="d0194-224">LocOrLP</span><span class="sxs-lookup"><span data-stu-id="d0194-224">LocOrLP</span></span> | <span data-ttu-id="d0194-225">WHSMobileAppStepLocOrLP</span><span class="sxs-lookup"><span data-stu-id="d0194-225">WHSMobileAppStepLocOrLP</span></span> |
| <span data-ttu-id="d0194-226">LocOrLP_From</span><span class="sxs-lookup"><span data-stu-id="d0194-226">LocOrLP_From</span></span> | <span data-ttu-id="d0194-227">WHSMobileAppStepLocOrLPFrom</span><span class="sxs-lookup"><span data-stu-id="d0194-227">WHSMobileAppStepLocOrLPFrom</span></span> |
| <span data-ttu-id="d0194-228">LocOrLP_To</span><span class="sxs-lookup"><span data-stu-id="d0194-228">LocOrLP_To</span></span> | <span data-ttu-id="d0194-229">WHSMobileAppStepLocOrLPTo</span><span class="sxs-lookup"><span data-stu-id="d0194-229">WHSMobileAppStepLocOrLPTo</span></span> |
| <span data-ttu-id="d0194-230">LocOrLPCheck</span><span class="sxs-lookup"><span data-stu-id="d0194-230">LocOrLPCheck</span></span> | <span data-ttu-id="d0194-231">WHSMobileAppStepLocOrLPCheck</span><span class="sxs-lookup"><span data-stu-id="d0194-231">WHSMobileAppStepLocOrLPCheck</span></span> |
| <span data-ttu-id="d0194-232">LocVerification</span><span class="sxs-lookup"><span data-stu-id="d0194-232">LocVerification</span></span> | <span data-ttu-id="d0194-233">WHSMobileAppStepLocVerification</span><span class="sxs-lookup"><span data-stu-id="d0194-233">WHSMobileAppStepLocVerification</span></span> |
| <span data-ttu-id="d0194-234">LPAdjustIn</span><span class="sxs-lookup"><span data-stu-id="d0194-234">LPAdjustIn</span></span> | <span data-ttu-id="d0194-235">WHSMobileAppStepLPAdjustIn</span><span class="sxs-lookup"><span data-stu-id="d0194-235">WHSMobileAppStepLPAdjustIn</span></span> |
| <span data-ttu-id="d0194-236">LPBreakChildLP</span><span class="sxs-lookup"><span data-stu-id="d0194-236">LPBreakChildLP</span></span> | <span data-ttu-id="d0194-237">WHSMobileAppStepLPBreakChildLP</span><span class="sxs-lookup"><span data-stu-id="d0194-237">WHSMobileAppStepLPBreakChildLP</span></span> |
| <span data-ttu-id="d0194-238">LPBreakParentLP</span><span class="sxs-lookup"><span data-stu-id="d0194-238">LPBreakParentLP</span></span> | <span data-ttu-id="d0194-239">WHSMobileAppStepLPBreakParentLP</span><span class="sxs-lookup"><span data-stu-id="d0194-239">WHSMobileAppStepLPBreakParentLP</span></span> |
| <span data-ttu-id="d0194-240">LPBuildChildLP</span><span class="sxs-lookup"><span data-stu-id="d0194-240">LPBuildChildLP</span></span> | <span data-ttu-id="d0194-241">WHSMobileAppStepLPBuildChildLP</span><span class="sxs-lookup"><span data-stu-id="d0194-241">WHSMobileAppStepLPBuildChildLP</span></span> |
| <span data-ttu-id="d0194-242">LPBuildParentLP</span><span class="sxs-lookup"><span data-stu-id="d0194-242">LPBuildParentLP</span></span> | <span data-ttu-id="d0194-243">WHSMobileAppStepLPBuildParentLP</span><span class="sxs-lookup"><span data-stu-id="d0194-243">WHSMobileAppStepLPBuildParentLP</span></span> |
| <span data-ttu-id="d0194-244">LPVerification</span><span class="sxs-lookup"><span data-stu-id="d0194-244">LPVerification</span></span> | <span data-ttu-id="d0194-245">WHSMobileAppStepLPVerification</span><span class="sxs-lookup"><span data-stu-id="d0194-245">WHSMobileAppStepLPVerification</span></span> |
| <span data-ttu-id="d0194-246">MergeContainerId</span><span class="sxs-lookup"><span data-stu-id="d0194-246">MergeContainerId</span></span> | <span data-ttu-id="d0194-247">WHSMobileAppStepMergeContainerId</span><span class="sxs-lookup"><span data-stu-id="d0194-247">WHSMobileAppStepMergeContainerId</span></span> |
| <span data-ttu-id="d0194-248">MixedLPLineNum</span><span class="sxs-lookup"><span data-stu-id="d0194-248">MixedLPLineNum</span></span> | <span data-ttu-id="d0194-249">WHSMobileAppStepMixedLPLineNum</span><span class="sxs-lookup"><span data-stu-id="d0194-249">WHSMobileAppStepMixedLPLineNum</span></span> |
| <span data-ttu-id="d0194-250">MobileDeviceQueueMessageCollectionIdentifierId</span><span class="sxs-lookup"><span data-stu-id="d0194-250">MobileDeviceQueueMessageCollectionIdentifierId</span></span> | <span data-ttu-id="d0194-251">WHSMobileAppStepSelectOrder</span><span class="sxs-lookup"><span data-stu-id="d0194-251">WHSMobileAppStepSelectOrder</span></span> |
| <span data-ttu-id="d0194-252">MovementConfirmCancel</span><span class="sxs-lookup"><span data-stu-id="d0194-252">MovementConfirmCancel</span></span> | <span data-ttu-id="d0194-253">WHSMobileAppStepMovementConfirmCancel</span><span class="sxs-lookup"><span data-stu-id="d0194-253">WHSMobileAppStepMovementConfirmCancel</span></span> |
| <span data-ttu-id="d0194-254">NewCaptureWeight</span><span class="sxs-lookup"><span data-stu-id="d0194-254">NewCaptureWeight</span></span> | <span data-ttu-id="d0194-255">WHSMobileAppStepCatchWeight</span><span class="sxs-lookup"><span data-stu-id="d0194-255">WHSMobileAppStepCatchWeight</span></span> |
| <span data-ttu-id="d0194-256">NewQty</span><span class="sxs-lookup"><span data-stu-id="d0194-256">NewQty</span></span> | <span data-ttu-id="d0194-257">WHSMobileAppStepNewQty</span><span class="sxs-lookup"><span data-stu-id="d0194-257">WHSMobileAppStepNewQty</span></span> |
| <span data-ttu-id="d0194-258">OutboundCatchWeightTag</span><span class="sxs-lookup"><span data-stu-id="d0194-258">OutboundCatchWeightTag</span></span> | <span data-ttu-id="d0194-259">WHSMobileAppStepCatchWeightTag</span><span class="sxs-lookup"><span data-stu-id="d0194-259">WHSMobileAppStepCatchWeightTag</span></span> |
| <span data-ttu-id="d0194-260">OutboundPut</span><span class="sxs-lookup"><span data-stu-id="d0194-260">OutboundPut</span></span> | <span data-ttu-id="d0194-261">WHSMobileAppStepOutboundPut</span><span class="sxs-lookup"><span data-stu-id="d0194-261">WHSMobileAppStepOutboundPut</span></span> |
| <span data-ttu-id="d0194-262">OutboundWeight</span><span class="sxs-lookup"><span data-stu-id="d0194-262">OutboundWeight</span></span> | <span data-ttu-id="d0194-263">WHSMobileAppStepCatchWeight</span><span class="sxs-lookup"><span data-stu-id="d0194-263">WHSMobileAppStepCatchWeight</span></span> |
| <span data-ttu-id="d0194-264">OverridePutNewLocation</span><span class="sxs-lookup"><span data-stu-id="d0194-264">OverridePutNewLocation</span></span> | <span data-ttu-id="d0194-265">WHSMobileAppStepOverridePutNewLocation</span><span class="sxs-lookup"><span data-stu-id="d0194-265">WHSMobileAppStepOverridePutNewLocation</span></span> |
| <span data-ttu-id="d0194-266">PieceByPieceConfirmation</span><span class="sxs-lookup"><span data-stu-id="d0194-266">PieceByPieceConfirmation</span></span> | <span data-ttu-id="d0194-267">WHSMobileAppStepQtyVerification</span><span class="sxs-lookup"><span data-stu-id="d0194-267">WHSMobileAppStepQtyVerification</span></span> |
| <span data-ttu-id="d0194-268">POLineNum</span><span class="sxs-lookup"><span data-stu-id="d0194-268">POLineNum</span></span> | <span data-ttu-id="d0194-269">WHSMobileAppStepPOLineNum</span><span class="sxs-lookup"><span data-stu-id="d0194-269">WHSMobileAppStepPOLineNum</span></span> |
| <span data-ttu-id="d0194-270">Tilausnumero</span><span class="sxs-lookup"><span data-stu-id="d0194-270">PONum</span></span> | <span data-ttu-id="d0194-271">WHSMobileAppStepPONum</span><span class="sxs-lookup"><span data-stu-id="d0194-271">WHSMobileAppStepPONum</span></span> |
| <span data-ttu-id="d0194-272">PositionFull</span><span class="sxs-lookup"><span data-stu-id="d0194-272">PositionFull</span></span> | <span data-ttu-id="d0194-273">WHSMobileAppStepPositionFull</span><span class="sxs-lookup"><span data-stu-id="d0194-273">WHSMobileAppStepPositionFull</span></span> |
| <span data-ttu-id="d0194-274">PositionFullQty</span><span class="sxs-lookup"><span data-stu-id="d0194-274">PositionFullQty</span></span> | <span data-ttu-id="d0194-275">WHSMobileAppStepPositionFullQty</span><span class="sxs-lookup"><span data-stu-id="d0194-275">WHSMobileAppStepPositionFullQty</span></span> |
| <span data-ttu-id="d0194-276">Vaikuttavuus</span><span class="sxs-lookup"><span data-stu-id="d0194-276">Potency</span></span> | <span data-ttu-id="d0194-277">WHSMobileAppStepPotency</span><span class="sxs-lookup"><span data-stu-id="d0194-277">WHSMobileAppStepPotency</span></span> |
| <span data-ttu-id="d0194-278">PrinterName</span><span class="sxs-lookup"><span data-stu-id="d0194-278">PrinterName</span></span> | <span data-ttu-id="d0194-279">WHSMobileAppStepPrinterName</span><span class="sxs-lookup"><span data-stu-id="d0194-279">WHSMobileAppStepPrinterName</span></span> |
| <span data-ttu-id="d0194-280">ProdId</span><span class="sxs-lookup"><span data-stu-id="d0194-280">ProdId</span></span> | <span data-ttu-id="d0194-281">WHSMobileAppStepProdId</span><span class="sxs-lookup"><span data-stu-id="d0194-281">WHSMobileAppStepProdId</span></span> |
| <span data-ttu-id="d0194-282">ProdLastPalletConfirmation</span><span class="sxs-lookup"><span data-stu-id="d0194-282">ProdLastPalletConfirmation</span></span> | <span data-ttu-id="d0194-283">WHSMobileAppStepProdLastPalletConfirmation</span><span class="sxs-lookup"><span data-stu-id="d0194-283">WHSMobileAppStepProdLastPalletConfirmation</span></span> |
| <span data-ttu-id="d0194-284">ProductConfirmation</span><span class="sxs-lookup"><span data-stu-id="d0194-284">ProductConfirmation</span></span> | <span data-ttu-id="d0194-285">WHSMobileAppStepProductConfirmation</span><span class="sxs-lookup"><span data-stu-id="d0194-285">WHSMobileAppStepProductConfirmation</span></span> |
| <span data-ttu-id="d0194-286">ProductionScrapConfirmation</span><span class="sxs-lookup"><span data-stu-id="d0194-286">ProductionScrapConfirmation</span></span> | <span data-ttu-id="d0194-287">WHSMobileAppStepProductionScrapConfirmation</span><span class="sxs-lookup"><span data-stu-id="d0194-287">WHSMobileAppStepProductionScrapConfirmation</span></span> |
| <span data-ttu-id="d0194-288">Määritä</span><span class="sxs-lookup"><span data-stu-id="d0194-288">Put</span></span> | <span data-ttu-id="d0194-289">WHSMobileAppStepPut</span><span class="sxs-lookup"><span data-stu-id="d0194-289">WHSMobileAppStepPut</span></span> |
| <span data-ttu-id="d0194-290">PutawayClusterId</span><span class="sxs-lookup"><span data-stu-id="d0194-290">PutawayClusterId</span></span> | <span data-ttu-id="d0194-291">WHSMobileAppStepPutawayClusterId</span><span class="sxs-lookup"><span data-stu-id="d0194-291">WHSMobileAppStepPutawayClusterId</span></span> |
| <span data-ttu-id="d0194-292">Määrä</span><span class="sxs-lookup"><span data-stu-id="d0194-292">Qty</span></span> | <span data-ttu-id="d0194-293">WHSMobileAppStepQty</span><span class="sxs-lookup"><span data-stu-id="d0194-293">WHSMobileAppStepQty</span></span> |
| <span data-ttu-id="d0194-294">QtyAdjust</span><span class="sxs-lookup"><span data-stu-id="d0194-294">QtyAdjust</span></span> | <span data-ttu-id="d0194-295">WHSMobileAppStepQtyAdjust</span><span class="sxs-lookup"><span data-stu-id="d0194-295">WHSMobileAppStepQtyAdjust</span></span> |
| <span data-ttu-id="d0194-296">QtyShort</span><span class="sxs-lookup"><span data-stu-id="d0194-296">QtyShort</span></span> | <span data-ttu-id="d0194-297">WHSMobileAppStepQtyShort</span><span class="sxs-lookup"><span data-stu-id="d0194-297">WHSMobileAppStepQtyShort</span></span> |
| <span data-ttu-id="d0194-298">QtyToConsume</span><span class="sxs-lookup"><span data-stu-id="d0194-298">QtyToConsume</span></span> | <span data-ttu-id="d0194-299">WHSMobileAppStepQtyToConsume</span><span class="sxs-lookup"><span data-stu-id="d0194-299">WHSMobileAppStepQtyToConsume</span></span> |
| <span data-ttu-id="d0194-300">QtyToPick</span><span class="sxs-lookup"><span data-stu-id="d0194-300">QtyToPick</span></span> | <span data-ttu-id="d0194-301">WHSMobileAppStepQtyToPick</span><span class="sxs-lookup"><span data-stu-id="d0194-301">WHSMobileAppStepQtyToPick</span></span> |
| <span data-ttu-id="d0194-302">QtyToPut</span><span class="sxs-lookup"><span data-stu-id="d0194-302">QtyToPut</span></span> | <span data-ttu-id="d0194-303">WHSMobileAppStepQtyToPut</span><span class="sxs-lookup"><span data-stu-id="d0194-303">WHSMobileAppStepQtyToPut</span></span> |
| <span data-ttu-id="d0194-304">QtyToScrap</span><span class="sxs-lookup"><span data-stu-id="d0194-304">QtyToScrap</span></span> | <span data-ttu-id="d0194-305">WHSMobileAppStepQtyToScrap</span><span class="sxs-lookup"><span data-stu-id="d0194-305">WHSMobileAppStepQtyToScrap</span></span> |
| <span data-ttu-id="d0194-306">QtyVerification</span><span class="sxs-lookup"><span data-stu-id="d0194-306">QtyVerification</span></span> | <span data-ttu-id="d0194-307">WHSMobileAppStepQtyVerification</span><span class="sxs-lookup"><span data-stu-id="d0194-307">WHSMobileAppStepQtyVerification</span></span> |
| <span data-ttu-id="d0194-308">QtyWithScanningLimit</span><span class="sxs-lookup"><span data-stu-id="d0194-308">QtyWithScanningLimit</span></span> | <span data-ttu-id="d0194-309">WHSMobileAppStepQtyAdjust</span><span class="sxs-lookup"><span data-stu-id="d0194-309">WHSMobileAppStepQtyAdjust</span></span> |
| <span data-ttu-id="d0194-310">ReasonString</span><span class="sxs-lookup"><span data-stu-id="d0194-310">ReasonString</span></span> | <span data-ttu-id="d0194-311">WHSMobileAppStepReasonString</span><span class="sxs-lookup"><span data-stu-id="d0194-311">WHSMobileAppStepReasonString</span></span> |
| <span data-ttu-id="d0194-312">RecvLocationId</span><span class="sxs-lookup"><span data-stu-id="d0194-312">RecvLocationId</span></span> | <span data-ttu-id="d0194-313">WHSMobileAppStepRecvLocationId</span><span class="sxs-lookup"><span data-stu-id="d0194-313">WHSMobileAppStepRecvLocationId</span></span> |
| <span data-ttu-id="d0194-314">RemoveContainerId</span><span class="sxs-lookup"><span data-stu-id="d0194-314">RemoveContainerId</span></span> | <span data-ttu-id="d0194-315">WHSMobileAppStepRemoveContainerId</span><span class="sxs-lookup"><span data-stu-id="d0194-315">WHSMobileAppStepRemoveContainerId</span></span> |
| <span data-ttu-id="d0194-316">ReprintLabelConfirmation</span><span class="sxs-lookup"><span data-stu-id="d0194-316">ReprintLabelConfirmation</span></span> | <span data-ttu-id="d0194-317">WHSMobileAppStepReprintLabelConfirmation</span><span class="sxs-lookup"><span data-stu-id="d0194-317">WHSMobileAppStepReprintLabelConfirmation</span></span> |
| <span data-ttu-id="d0194-318">RMANum</span><span class="sxs-lookup"><span data-stu-id="d0194-318">RMANum</span></span> | <span data-ttu-id="d0194-319">WHSMobileAppStepRMANum</span><span class="sxs-lookup"><span data-stu-id="d0194-319">WHSMobileAppStepRMANum</span></span> |
| <span data-ttu-id="d0194-320">ShortPickReason</span><span class="sxs-lookup"><span data-stu-id="d0194-320">ShortPickReason</span></span> | <span data-ttu-id="d0194-321">WHSMobileAppStepShortPickReason</span><span class="sxs-lookup"><span data-stu-id="d0194-321">WHSMobileAppStepShortPickReason</span></span> |
| <span data-ttu-id="d0194-322">SortConOrLP</span><span class="sxs-lookup"><span data-stu-id="d0194-322">SortConOrLP</span></span> | <span data-ttu-id="d0194-323">WHSMobileAppStepSortConOrLP</span><span class="sxs-lookup"><span data-stu-id="d0194-323">WHSMobileAppStepSortConOrLP</span></span> |
| <span data-ttu-id="d0194-324">SortLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="d0194-324">SortLicensePlateId</span></span> | <span data-ttu-id="d0194-325">WHSMobileAppStepSortLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="d0194-325">WHSMobileAppStepSortLicensePlateId</span></span> |
| <span data-ttu-id="d0194-326">SortPositionId</span><span class="sxs-lookup"><span data-stu-id="d0194-326">SortPositionId</span></span> | <span data-ttu-id="d0194-327">WHSMobileAppStepSortPositionId</span><span class="sxs-lookup"><span data-stu-id="d0194-327">WHSMobileAppStepSortPositionId</span></span> |
| <span data-ttu-id="d0194-328">SortVerification</span><span class="sxs-lookup"><span data-stu-id="d0194-328">SortVerification</span></span> | <span data-ttu-id="d0194-329">WHSMobileAppStepSortVerification</span><span class="sxs-lookup"><span data-stu-id="d0194-329">WHSMobileAppStepSortVerification</span></span> |
| <span data-ttu-id="d0194-330">StartLocationId</span><span class="sxs-lookup"><span data-stu-id="d0194-330">StartLocationId</span></span> | <span data-ttu-id="d0194-331">WHSMobileAppStepStartLocationId</span><span class="sxs-lookup"><span data-stu-id="d0194-331">WHSMobileAppStepStartLocationId</span></span> |
| <span data-ttu-id="d0194-332">StartProdOrderConfirmation</span><span class="sxs-lookup"><span data-stu-id="d0194-332">StartProdOrderConfirmation</span></span> | <span data-ttu-id="d0194-333">WHSMobileAppStepStartProdOrderConfirmation</span><span class="sxs-lookup"><span data-stu-id="d0194-333">WHSMobileAppStepStartProdOrderConfirmation</span></span> |
| <span data-ttu-id="d0194-334">TargetLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="d0194-334">TargetLicensePlateId</span></span> | <span data-ttu-id="d0194-335">WHSMobileAppStepTargetLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="d0194-335">WHSMobileAppStepTargetLicensePlateId</span></span> |
| <span data-ttu-id="d0194-336">TOLineNum</span><span class="sxs-lookup"><span data-stu-id="d0194-336">TOLineNum</span></span> | <span data-ttu-id="d0194-337">WHSMobileAppStepTOLineNum</span><span class="sxs-lookup"><span data-stu-id="d0194-337">WHSMobileAppStepTOLineNum</span></span> |
| <span data-ttu-id="d0194-338">ToLocation</span><span class="sxs-lookup"><span data-stu-id="d0194-338">ToLocation</span></span> | <span data-ttu-id="d0194-339">WHSMobileAppStepToLocation</span><span class="sxs-lookup"><span data-stu-id="d0194-339">WHSMobileAppStepToLocation</span></span> |
| <span data-ttu-id="d0194-340">TONum</span><span class="sxs-lookup"><span data-stu-id="d0194-340">TONum</span></span> | <span data-ttu-id="d0194-341">WHSMobileAppStepTONum</span><span class="sxs-lookup"><span data-stu-id="d0194-341">WHSMobileAppStepTONum</span></span> |
| <span data-ttu-id="d0194-342">ToWarehouse</span><span class="sxs-lookup"><span data-stu-id="d0194-342">ToWarehouse</span></span> | <span data-ttu-id="d0194-343">WHSMobileAppStepWarehouseTo</span><span class="sxs-lookup"><span data-stu-id="d0194-343">WHSMobileAppStepWarehouseTo</span></span> |
| <span data-ttu-id="d0194-344">TransportLoadId</span><span class="sxs-lookup"><span data-stu-id="d0194-344">TransportLoadId</span></span> | <span data-ttu-id="d0194-345">WHSMobileAppStepTransportLoadId</span><span class="sxs-lookup"><span data-stu-id="d0194-345">WHSMobileAppStepTransportLoadId</span></span> |
| <span data-ttu-id="d0194-346">WaveLabelId</span><span class="sxs-lookup"><span data-stu-id="d0194-346">WaveLabelId</span></span> | <span data-ttu-id="d0194-347">WHSMobileAppStepWaveLabelId</span><span class="sxs-lookup"><span data-stu-id="d0194-347">WHSMobileAppStepWaveLabelId</span></span> |
| <span data-ttu-id="d0194-348">WaveLblQty</span><span class="sxs-lookup"><span data-stu-id="d0194-348">WaveLblQty</span></span> | <span data-ttu-id="d0194-349">WHSMobileAppStepWaveLblQty</span><span class="sxs-lookup"><span data-stu-id="d0194-349">WHSMobileAppStepWaveLblQty</span></span> |
| <span data-ttu-id="d0194-350">Paino</span><span class="sxs-lookup"><span data-stu-id="d0194-350">Weight</span></span> | <span data-ttu-id="d0194-351">WHSMobileAppStepWeight</span><span class="sxs-lookup"><span data-stu-id="d0194-351">WHSMobileAppStepWeight</span></span> |
| <span data-ttu-id="d0194-352">WeightToConsume</span><span class="sxs-lookup"><span data-stu-id="d0194-352">WeightToConsume</span></span> | <span data-ttu-id="d0194-353">WHSMobileAppStepWeightToConsume</span><span class="sxs-lookup"><span data-stu-id="d0194-353">WHSMobileAppStepWeightToConsume</span></span> |
| <span data-ttu-id="d0194-354">WHSAdjustmentType</span><span class="sxs-lookup"><span data-stu-id="d0194-354">WHSAdjustmentType</span></span> | <span data-ttu-id="d0194-355">WHSMobileAppStepWHSAdjustmentType</span><span class="sxs-lookup"><span data-stu-id="d0194-355">WHSMobileAppStepWHSAdjustmentType</span></span> |
| <span data-ttu-id="d0194-356">WHSReceivingException</span><span class="sxs-lookup"><span data-stu-id="d0194-356">WHSReceivingException</span></span> | <span data-ttu-id="d0194-357">WHSMobileAppStepWHSReceivingException</span><span class="sxs-lookup"><span data-stu-id="d0194-357">WHSMobileAppStepWHSReceivingException</span></span> |
| <span data-ttu-id="d0194-358">WHSWorkException</span><span class="sxs-lookup"><span data-stu-id="d0194-358">WHSWorkException</span></span> | <span data-ttu-id="d0194-359">WHSMobileAppStepWHSWorkException</span><span class="sxs-lookup"><span data-stu-id="d0194-359">WHSMobileAppStepWHSWorkException</span></span> |
| <span data-ttu-id="d0194-360">WHSWorkLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="d0194-360">WHSWorkLicensePlateId</span></span> | <span data-ttu-id="d0194-361">WHSMobileAppStepWorkLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="d0194-361">WHSMobileAppStepWorkLicensePlateId</span></span> |
| <span data-ttu-id="d0194-362">WMSLocationId</span><span class="sxs-lookup"><span data-stu-id="d0194-362">WMSLocationId</span></span> | <span data-ttu-id="d0194-363">WHSMobileAppStepLocation</span><span class="sxs-lookup"><span data-stu-id="d0194-363">WHSMobileAppStepLocation</span></span> |
| <span data-ttu-id="d0194-364">WorkId</span><span class="sxs-lookup"><span data-stu-id="d0194-364">WorkId</span></span> | <span data-ttu-id="d0194-365">WHSMobileAppStepWorkId</span><span class="sxs-lookup"><span data-stu-id="d0194-365">WHSMobileAppStepWorkId</span></span> |
| <span data-ttu-id="d0194-366">WorkIdToCancel</span><span class="sxs-lookup"><span data-stu-id="d0194-366">WorkIdToCancel</span></span> | <span data-ttu-id="d0194-367">WHSMobileAppStepWorkIdToCancel</span><span class="sxs-lookup"><span data-stu-id="d0194-367">WHSMobileAppStepWorkIdToCancel</span></span> |
| <span data-ttu-id="d0194-368">WorkLPIdPutawayCluster</span><span class="sxs-lookup"><span data-stu-id="d0194-368">WorkLPIdPutawayCluster</span></span> | <span data-ttu-id="d0194-369">WHSMobileAppStepWorkLPIdPutawayCluster</span><span class="sxs-lookup"><span data-stu-id="d0194-369">WHSMobileAppStepWorkLPIdPutawayCluster</span></span> |
| <span data-ttu-id="d0194-370">WorkPoolId</span><span class="sxs-lookup"><span data-stu-id="d0194-370">WorkPoolId</span></span> | <span data-ttu-id="d0194-371">WHSMobileAppStepWorkPoolId</span><span class="sxs-lookup"><span data-stu-id="d0194-371">WHSMobileAppStepWorkPoolId</span></span> |
| <span data-ttu-id="d0194-372">ZoneId</span><span class="sxs-lookup"><span data-stu-id="d0194-372">ZoneId</span></span> | <span data-ttu-id="d0194-373">WHSMobileAppStepZoneId</span><span class="sxs-lookup"><span data-stu-id="d0194-373">WHSMobileAppStepZoneId</span></span> |

### <a name="available-step-icons"></a><a name="step-icons"></a><span data-ttu-id="d0194-374">Käytettävissä olevat vaiheen kuvakkeet</span><span class="sxs-lookup"><span data-stu-id="d0194-374">Available step icons</span></span>

<span data-ttu-id="d0194-375">Järjestelmä sisältää kokoelman vakiovaihekuvakkeita, joita voit käyttää myös mukautetuissa vaiheissasi.</span><span class="sxs-lookup"><span data-stu-id="d0194-375">The system includes a collection of standard step icons that you can also use for your custom steps.</span></span> <span data-ttu-id="d0194-376">Et voi ladata mukautettuja vaihekuvakkeita palvelimeen.</span><span class="sxs-lookup"><span data-stu-id="d0194-376">You can't currently upload custom step icons.</span></span> <span data-ttu-id="d0194-377">Siksi sinun on aina valittava jokin vakiovaihekuvakkeista.</span><span class="sxs-lookup"><span data-stu-id="d0194-377">Therefore, you must always select one of the standard step icons.</span></span>

<span data-ttu-id="d0194-378">Seuraavassa taulukossa näkyvät kaikki käytettävissä olevat vakiovaihekuvakkeet ja niiden nimet.</span><span class="sxs-lookup"><span data-stu-id="d0194-378">The following table shows every standard step icon that is currently available, and its name.</span></span>

<table>
<tbody>
<tr>
<td><img src="media/step-icons-about.png" alt="About step icon" title="Tietoja vaihekuvakkeesta"><br><span data-ttu-id="d0194-380">Tietoja</span><span class="sxs-lookup"><span data-stu-id="d0194-380">About</span></span></td>
<td><img src="media/step-icons-add-lp.png" alt="Add license plate or item step icon" title="Käyttöoikeussopimuksen tai nimikevaihekuvakkeen lisääminen"><br><span data-ttu-id="d0194-382">AddLpOrItem</span><span class="sxs-lookup"><span data-stu-id="d0194-382">AddLpOrItem</span></span></td>
<td><img src="media/step-icons-batch-disposition.png" alt="Batch disposition step icon" title="Erän käsittelyvaihe -kuvake"><br><span data-ttu-id="d0194-384">BatchDisposition</span><span class="sxs-lookup"><span data-stu-id="d0194-384">BatchDisposition</span></span></td>
<td><img src="media/step-icons-carrier.png" alt="Carrier step icon" title="Rahdinkuljettajan vaiheen kuvake"><br><span data-ttu-id="d0194-386">Rahdinkuljettaja</span><span class="sxs-lookup"><span data-stu-id="d0194-386">Carrier</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-cw-tag.png" alt="Catch weight tag step icon" title="Todellisen painon tunnisteen vaiheen kuvake"><br><span data-ttu-id="d0194-388">CatchWeightTag</span><span class="sxs-lookup"><span data-stu-id="d0194-388">CatchWeightTag</span></span></td>
<td><img src="media/step-icons-cw-tag-weight.png" alt="Catch weight tag weight step icon" title="Todellisen painon tunnisteen painovaiheen kuvake"><br><span data-ttu-id="d0194-390">CatchWeightTagWeight</span><span class="sxs-lookup"><span data-stu-id="d0194-390">CatchWeightTagWeight</span></span></td>
<td><img src="media/step-icons-check-digit.png" alt="Check digit step icon" title="Tarkistusnumerovaihe-kuvake"><br><span data-ttu-id="d0194-392">CheckDigit</span><span class="sxs-lookup"><span data-stu-id="d0194-392">CheckDigit</span></span></td>
<td><img src="media/step-icons-check-in-out.png" alt="Check in or out ID step icon" title="Sisään- tai uloskäyntitunnuksen vaiheen kuvake"><br><span data-ttu-id="d0194-394">CheckInOutId</span><span class="sxs-lookup"><span data-stu-id="d0194-394">CheckInOutId</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-child-lp.png" alt="Child license plate step icon" title="Alikäyttöoikeusvaihekuvake"><br><span data-ttu-id="d0194-396">ChildLP</span><span class="sxs-lookup"><span data-stu-id="d0194-396">ChildLP</span></span></td>
<td><img src="media/step-icons-cluster-id.png" alt="Cluster ID step icon" title="Klusterin tunnus -vaiheen kuvake"><br><span data-ttu-id="d0194-398">ClusterId</span><span class="sxs-lookup"><span data-stu-id="d0194-398">ClusterId</span></span></td>
<td><img src="media/step-icons-cluster-position.png" alt="Cluster position step icon" title="Klusterin sijainti -vaiheen kuvake"><br><span data-ttu-id="d0194-400">ClusterPosition</span><span class="sxs-lookup"><span data-stu-id="d0194-400">ClusterPosition</span></span></td>
<td><img src="media/step-icons-config-id.png" alt="Config ID step icon" title="Määritteen tunnus -vaiheen kuvake"><br><span data-ttu-id="d0194-402">ConfigId</span><span class="sxs-lookup"><span data-stu-id="d0194-402">ConfigId</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-configured-field.png" alt="Configured field step icon" title="Määritetty kentän vaiheen kuvake"><br><span data-ttu-id="d0194-404">ConfiguredField</span><span class="sxs-lookup"><span data-stu-id="d0194-404">ConfiguredField</span></span></td>
<td><img src="media/step-icons-con-lp.png" alt="Con or LP step icon" title="Con- tai LP-vaihekuvake"><br><span data-ttu-id="d0194-406">ConOrLP</span><span class="sxs-lookup"><span data-stu-id="d0194-406">ConOrLP</span></span></td>
<td><img src="media/step-icons-consolidate-from-LP.png" alt="Consolidate from license plate ID step icon" title="Konsolidoi lisenssikäyttöoikeuksien tunnuksen vaiheen kuvake"><br><span data-ttu-id="d0194-408">ConsolidateFromLicensePlateID</span><span class="sxs-lookup"><span data-stu-id="d0194-408">ConsolidateFromLicensePlateID</span></span></td>
<td><img src="media/step-icons-consolidate-to-LP.png" alt="Consolidate to license plate ID step icon" title="Konsolidoi lisenssikäyttöoikeustunnuksen vaihekuvakkeeseen"><br><span data-ttu-id="d0194-410">ConsolidateToLicensePlateID</span><span class="sxs-lookup"><span data-stu-id="d0194-410">ConsolidateToLicensePlateID</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-container-type.png" alt="Container type step icon" title="Konttityypin vaiheen kuvake"><br><span data-ttu-id="d0194-412">ContainerType</span><span class="sxs-lookup"><span data-stu-id="d0194-412">ContainerType</span></span></td>
<td><img src="media/step-icons-counting.png" alt="Counting step icon" title="Inventointivaihe-kuvake"><br><span data-ttu-id="d0194-414">Inventointi</span><span class="sxs-lookup"><span data-stu-id="d0194-414">Counting</span></span></td>
<td><img src="media/step-icons-counting-reason.png" alt="Counting reason code step icon" title="Inventoinnin syykoodin vaiheen kuvake"><br><span data-ttu-id="d0194-416">CountingReasonCode</span><span class="sxs-lookup"><span data-stu-id="d0194-416">CountingReasonCode</span></span></td>
<td><img src="media/step-icons-country-origin.png" alt="Country of origin code step icon" title="Alkuperämaakoodin vaiheen kuvake"><br><span data-ttu-id="d0194-418">CountryOfOrigin</span><span class="sxs-lookup"><span data-stu-id="d0194-418">CountryOfOrigin</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-disposition.png" alt="Disposition step icon" title="Käsittelyvaihe-kuvake"><br><span data-ttu-id="d0194-420">Käsittely</span><span class="sxs-lookup"><span data-stu-id="d0194-420">Disposition</span></span></td>
<td><img src="media/step-icons-done.png" alt="Done step icon" title="Valmis vaihe -kuvake"><br><span data-ttu-id="d0194-422">Valmis</span><span class="sxs-lookup"><span data-stu-id="d0194-422">Done</span></span></td>
<td><img src="media/step-icons-driver-check-in-confirmation.png" alt="Driver check in confirmation step icon" title="Ohjaimen vahvistusvaihe -kuvake"><br><span data-ttu-id="d0194-424">DriverCheckInConfirmation</span><span class="sxs-lookup"><span data-stu-id="d0194-424">DriverCheckInConfirmation</span></span></td>
<td><img src="media/step-icons-driver-check-in-id.png" alt="Driver check in ID step icon" title="Kuljettajan sisäänkäyntitunnuksen vaiheen kuvake"><br><span data-ttu-id="d0194-426">DriverCheckInId</span><span class="sxs-lookup"><span data-stu-id="d0194-426">DriverCheckInId</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-driver-check-out-id.png" alt="Driver check out ID step icon" title="Kuljettajan uloskäyntitunnuksen vaiheen kuvake"><br><span data-ttu-id="d0194-428">DriverCheckOutId</span><span class="sxs-lookup"><span data-stu-id="d0194-428">DriverCheckOutId</span></span></td>
<td><img src="media/step-icons-exp-date.png" alt="Expiration date step icon" title="Vanhenemispäivän vaiheen kuvake"><br><span data-ttu-id="d0194-430">ExpDate</span><span class="sxs-lookup"><span data-stu-id="d0194-430">ExpDate</span></span></td>
<td><img src="media/step-icons-field.png" alt="Field step icon" title="Kentän vaiheen kuvake"><br><span data-ttu-id="d0194-432">Kenttä</span><span class="sxs-lookup"><span data-stu-id="d0194-432">Field</span></span></td>
<td><img src="media/step-icons-from-batch.png" alt="From batch disposition step icon" title="Erästä käsittelyvaiheen kuvake"><br><span data-ttu-id="d0194-434">FromBatchDisposition</span><span class="sxs-lookup"><span data-stu-id="d0194-434">FromBatchDisposition</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-from-inventory-status.png" alt="From inventory status step icon" title="Varastosta tilan vaiheen kuvake"><br><span data-ttu-id="d0194-436">FromInventoryStatus</span><span class="sxs-lookup"><span data-stu-id="d0194-436">FromInventoryStatus</span></span></td>
<td><img src="media/step-icons-id-attribute.png" alt="ID attribute step icon" title="Määritystunnus -vaiheen kuvake"><br><span data-ttu-id="d0194-438">IdAttribute</span><span class="sxs-lookup"><span data-stu-id="d0194-438">IdAttribute</span></span></td>
<td><img src="media/step-icons-invent-batch-id.png" alt="Inventory batch ID step icon" title="Varastoerän tunnuksen vaiheen kuvake"><br><span data-ttu-id="d0194-440">InventBatchID</span><span class="sxs-lookup"><span data-stu-id="d0194-440">InventBatchID</span></span></td>
<td><img src="media/step-icons-invent-color-id.png" alt="Inventory color ID step icon" title="Varastovärin tunnuksen vaiheen kuvake"><br><span data-ttu-id="d0194-442">InventColorID</span><span class="sxs-lookup"><span data-stu-id="d0194-442">InventColorID</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-invent-location.png" alt="Inventory location step icon" title="Varastosijainnin tunnuksen vaiheen kuvake"><br><span data-ttu-id="d0194-444">InventLocation</span><span class="sxs-lookup"><span data-stu-id="d0194-444">InventLocation</span></span></td>
<td><img src="media/step-icons-invent-serial-id.png" alt="Inventory serial ID step icon" title="Varastosarjan tunnuksen vaiheen kuvake"><br><span data-ttu-id="d0194-446">InventSerialID</span><span class="sxs-lookup"><span data-stu-id="d0194-446">InventSerialID</span></span></td>
<td><img src="media/step-icons-invent-size-id.png" alt="Inventory size ID step icon" title="Varastokoon tunnuksen vaiheen kuvake"><br><span data-ttu-id="d0194-448">InventSizeID</span><span class="sxs-lookup"><span data-stu-id="d0194-448">InventSizeID</span></span></td>
<td><img src="media/step-icons-invent-status-id.png" alt="Inventory status ID step icon" title="Varastotilan tunnuksen vaiheen kuvake"><br><span data-ttu-id="d0194-450">InventStatusID</span><span class="sxs-lookup"><span data-stu-id="d0194-450">InventStatusID</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-invent-style-id.png" alt="Inventory style ID step icon" title="Varastotyylin tunnuksen vaiheen kuvake"><br><span data-ttu-id="d0194-452">InventStyleID</span><span class="sxs-lookup"><span data-stu-id="d0194-452">InventStyleID</span></span></td>
<td><img src="media/step-icons-invent-version-id.png" alt="Inventory version ID step icon" title="Varastoversion tunnuksen vaiheen kuvake"><br><span data-ttu-id="d0194-454">InventVersionID</span><span class="sxs-lookup"><span data-stu-id="d0194-454">InventVersionID</span></span></td>
<td><img src="media/step-icons-item-id.png" alt="Item ID step icon" title="Nimikkeen tunnus -vaiheen kuvake"><br><span data-ttu-id="d0194-456">ItemID</span><span class="sxs-lookup"><span data-stu-id="d0194-456">ItemID</span></span></td>
<td><img src="media/step-icons-itm-contianer-id.png" alt="ITM container ID step icon" title="ITM-konttitunnuksen vaiheen kuvake"><br><span data-ttu-id="d0194-458">ITMContainerID</span><span class="sxs-lookup"><span data-stu-id="d0194-458">ITMContainerID</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-itm-shipment-id.png" alt="ITM shipment ID step icon" title="ITM-lähetystunnuksen vaiheen kuvake"><br><span data-ttu-id="d0194-460">ITMShipmentID</span><span class="sxs-lookup"><span data-stu-id="d0194-460">ITMShipmentID</span></span></td>
<td><img src="media/step-icons-kanban-card-id.png" alt="Kanban card ID step icon" title="Kanban-kortin tunnus -vaiheen kuvake"><br><span data-ttu-id="d0194-462">KanbanCardID</span><span class="sxs-lookup"><span data-stu-id="d0194-462">KanbanCardID</span></span></td>
<td><img src="media/step-icons-kanban-or-card-id.png" alt="Kanban or card ID step icon" title="Kanban- tai kortin tunnus -vaiheen kuvake"><br><span data-ttu-id="d0194-464">KanbanOrCardID</span><span class="sxs-lookup"><span data-stu-id="d0194-464">KanbanOrCardID</span></span></td>
<td><img src="media/step-icons-license-plate-id.png" alt="License plate ID step icon" title="Käyttöoikeustunnuksen vaiheen kuvake"><br><span data-ttu-id="d0194-466">LicensePlateID</span><span class="sxs-lookup"><span data-stu-id="d0194-466">LicensePlateID</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-load-id.png" alt="Load ID step icon" title="Lataa tunnus -vaiheen kuvake"><br><span data-ttu-id="d0194-468">LoadId</span><span class="sxs-lookup"><span data-stu-id="d0194-468">LoadId</span></span></td>
<td><img src="media/step-icons-location-lp-pos.png" alt="Location license plate position step icon" title="Toimipaikan rekisterikilpien paikan vaiheen kuvake"><br><span data-ttu-id="d0194-470">LocationLicensePlatePosition</span><span class="sxs-lookup"><span data-stu-id="d0194-470">LocationLicensePlatePosition</span></span></td>
<td><img src="media/step-icons-location-or-lp.png" alt="Location or license plate step icon" title="Sijainti- tai käyttöoikeussopimuksen vaiheen kuvakkeen lisääminen"><br><span data-ttu-id="d0194-472">LocOrLP</span><span class="sxs-lookup"><span data-stu-id="d0194-472">LocOrLP</span></span></td>
<td><img src="media/step-icons-location-or-lp-check.png" alt="Location or license plate check step icon" title="Sijainti- tai käyttöoikeussopimuksen tarkistusvaiheen kuvake"><br><span data-ttu-id="d0194-474">LocOrLPCheck</span><span class="sxs-lookup"><span data-stu-id="d0194-474">LocOrLPCheck</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-location-or-lp-from.png" alt="Location or license plate from step icon" title="Sijainti- tai käyttöoikeussopimuksen lomakevaiheesta kuvake"><br><span data-ttu-id="d0194-476">LocOrLPFrom</span><span class="sxs-lookup"><span data-stu-id="d0194-476">LocOrLPFrom</span></span></td>
<td><img src="media/step-icons-location-or-lp-to.png" alt="Location or license plate to step icon" title="Sijainti- tai käyttöoikeussopimuksen vaiheeseen kuvakkeen lisääminen"><br><span data-ttu-id="d0194-478">LocOrLPTo</span><span class="sxs-lookup"><span data-stu-id="d0194-478">LocOrLPTo</span></span></td>
<td><img src="media/step-icons-long-process-complete.png" alt="Long process completed step icon" title="Pitkä prosessi valmis -vaiheen kuvake"><br><span data-ttu-id="d0194-480">LongProcessCompleted</span><span class="sxs-lookup"><span data-stu-id="d0194-480">LongProcessCompleted</span></span></td>
<td><img src="media/step-icons-lp-break-parent.png" alt="LP break parent LP step icon" title="LP-tauon pää-LP-vaiheen kuvake"><br><span data-ttu-id="d0194-482">LPBreakParentLP</span><span class="sxs-lookup"><span data-stu-id="d0194-482">LPBreakParentLP</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-merge-container.png" alt="Merge container ID step icon" title="Yhdistä konttitunnuksen vaiheen kuvake"><br><span data-ttu-id="d0194-484">MergeContainerId</span><span class="sxs-lookup"><span data-stu-id="d0194-484">MergeContainerId</span></span></td>
<td><img src="media/step-icons-mixed-lp-line.png" alt="Mixed license plate line number step icon" title="Sekalaisen käyttöoikeusnumerorivin vaiheen kuvake"><br><span data-ttu-id="d0194-486">MixedLPLineNum</span><span class="sxs-lookup"><span data-stu-id="d0194-486">MixedLPLineNum</span></span></td>
<td><img src="media/step-icons-outbound-weight.png" alt="Outbound weight step icon" title="Lähtevän painon vaiheen kuvake"><br><span data-ttu-id="d0194-488">OutboundWeight</span><span class="sxs-lookup"><span data-stu-id="d0194-488">OutboundWeight</span></span></td>
<td><img src="media/step-icons-owner.png" alt="Owner step icon" title="Omistajavaihe-kuvake"><br><span data-ttu-id="d0194-490">Omistaja</span><span class="sxs-lookup"><span data-stu-id="d0194-490">Owner</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-parent-lp.png" alt="Parent license plate step icon" title="Pääkäyttöoikeusvaihekuvake"><br><span data-ttu-id="d0194-492">ParentLP</span><span class="sxs-lookup"><span data-stu-id="d0194-492">ParentLP</span></span></td>
<td><img src="media/step-icons-please-confirm.png" alt="Please confirm step icon" title="Vahvista vaiheen kuvake"><br><span data-ttu-id="d0194-494">PleaseConfirm</span><span class="sxs-lookup"><span data-stu-id="d0194-494">PleaseConfirm</span></span></td>
<td><img src="media/step-icons-po-line-num.png" alt="Purchase order line number step icon" title="Ostotilausrivin numeron vaiheen kuvake"><br><span data-ttu-id="d0194-496">POLineNum</span><span class="sxs-lookup"><span data-stu-id="d0194-496">POLineNum</span></span></td>
<td><img src="media/step-icons-po-num.png" alt="Purchase order number step icon" title="Ostotilauksen numeron vaiheen kuvake"><br><span data-ttu-id="d0194-498">Tilausnumero</span><span class="sxs-lookup"><span data-stu-id="d0194-498">PONum</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-position-full.png" alt="Position full step icon" title="Sijainti täynnä -vaiheen kuvake"><br><span data-ttu-id="d0194-500">PositionFull</span><span class="sxs-lookup"><span data-stu-id="d0194-500">PositionFull</span></span></td>
<td><img src="media/step-icons-potency.png" alt="Potency step icon" title="Vaikuttavuusvaihe-kuvake"><br><span data-ttu-id="d0194-502">Vaikuttavuus</span><span class="sxs-lookup"><span data-stu-id="d0194-502">Potency</span></span></td>
<td><img src="media/step-icons-printer-name.png" alt="Printer name step icon" title="Tulostimen nimen vaiheen kuvake"><br><span data-ttu-id="d0194-504">PrinterName</span><span class="sxs-lookup"><span data-stu-id="d0194-504">PrinterName</span></span></td>
<td><img src="media/step-icons-prod-id.png" alt="Prod ID step icon" title="Tuotteen tunnus -vaiheen kuvake"><br><span data-ttu-id="d0194-506">ProdId</span><span class="sxs-lookup"><span data-stu-id="d0194-506">ProdId</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-product-confirm.png" alt="Product confirmation step icon" title="Tuotevahvistusvaihe-kuvake"><br><span data-ttu-id="d0194-508">ProductConfirmation</span><span class="sxs-lookup"><span data-stu-id="d0194-508">ProductConfirmation</span></span></td>
<td><img src="media/step-icons-put.png" alt="Put step icon" title="Pitovaiheen kuvake"><br><span data-ttu-id="d0194-510">Määritä</span><span class="sxs-lookup"><span data-stu-id="d0194-510">Put</span></span></td>
<td><img src="media/step-icons-putaway-cluster-id.png" alt="Putaway cluster ID step icon" title="Pois laitettavan klusterin tunnus -vaiheen kuvake"><br><span data-ttu-id="d0194-512">PutawayClusterId</span><span class="sxs-lookup"><span data-stu-id="d0194-512">PutawayClusterId</span></span></td>
<td><img src="media/step-icons-qty.png" alt="Quantity step icon" title="Määrävaihekuvake"><br><span data-ttu-id="d0194-514">Määrä</span><span class="sxs-lookup"><span data-stu-id="d0194-514">Qty</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-qty-adjust-in.png" alt="Quantity adjust in step icon" title="Määrän oikaisemisvaiheen kuvake"><br><span data-ttu-id="d0194-516">QtyAdjustIn</span><span class="sxs-lookup"><span data-stu-id="d0194-516">QtyAdjustIn</span></span></td>
<td><img src="media/step-icons-qty-short.png" alt="Quantity short step icon" title="Määrä vähissä -vaiheen kuvake"><br><span data-ttu-id="d0194-518">QtyShort</span><span class="sxs-lookup"><span data-stu-id="d0194-518">QtyShort</span></span></td>
<td><img src="media/step-icons-qty-to-consume.png" alt="Quantity to consume step icon" title="Kulutettavan määrän vaiheen kuvake"><br><span data-ttu-id="d0194-520">QtyToConsume</span><span class="sxs-lookup"><span data-stu-id="d0194-520">QtyToConsume</span></span></td>
<td><img src="media/step-icons-qty-to-put.png" alt="Quantity to put step icon" title="Pidettävän määrän vaiheen kuvake"><br><span data-ttu-id="d0194-522">QtyToPut</span><span class="sxs-lookup"><span data-stu-id="d0194-522">QtyToPut</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-qty-to-scrap.png" alt="Quantity to scrap step icon" title="Hävikkimäärän vaiheen kuvake"><br><span data-ttu-id="d0194-524">QtyToScrap</span><span class="sxs-lookup"><span data-stu-id="d0194-524">QtyToScrap</span></span></td>
<td><img src="media/step-icons-qty-confirmation.png" alt="Quantity confirmation step icon" title="Määrän vahvistuksen vaihe -kuvake"><br><span data-ttu-id="d0194-526">QuantityConfirmation</span><span class="sxs-lookup"><span data-stu-id="d0194-526">QuantityConfirmation</span></span></td>
<td><img src="media/step-icons-raf-end-job.png" alt="Report as finished end job step icon" title="Ilmoita valmiiksi -työn vaiheen kuvake"><br><span data-ttu-id="d0194-528">RAFEndJob</span><span class="sxs-lookup"><span data-stu-id="d0194-528">RAFEndJob</span></span></td>
<td><img src="media/step-icons-recv-loc-id.png" alt="Receive location ID step icon" title="Vastaanottosijainnin tunnus -vaiheen kuvake"><br><span data-ttu-id="d0194-530">RecvLocationID</span><span class="sxs-lookup"><span data-stu-id="d0194-530">RecvLocationID</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-remove-container-id.png" alt="Remove container ID step icon" title="Poista konttitunnuksen vaiheen kuvake"><br><span data-ttu-id="d0194-532">RemoveContainerID</span><span class="sxs-lookup"><span data-stu-id="d0194-532">RemoveContainerID</span></span></td>
<td><img src="media/step-icons-rma-no.png" alt="RMA number step icon" title="RMA-numeron vaiheen kuvake"><br><span data-ttu-id="d0194-534">RMANum</span><span class="sxs-lookup"><span data-stu-id="d0194-534">RMANum</span></span></td>
<td><img src="media/step-icons-select-order.png" alt="Select order step icon" title="Valitse tilaus -vaiheen kuvake"><br><span data-ttu-id="d0194-536">SelectOrder</span><span class="sxs-lookup"><span data-stu-id="d0194-536">SelectOrder</span></span></td>
<td><img src="media/step-icons-short-pick-reason.png" alt="Short pick reason step icon" title="Lyhyen poiminnan syyvaihe -kuvake"><br><span data-ttu-id="d0194-538">ShortPickReason</span><span class="sxs-lookup"><span data-stu-id="d0194-538">ShortPickReason</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-sort-position-id.png" alt="Sort position ID step icon" title="Sijaintitunnuksen vaiheen lajittelukuvake"><br><span data-ttu-id="d0194-540">SortPositionId</span><span class="sxs-lookup"><span data-stu-id="d0194-540">SortPositionId</span></span></td>
<td><img src="media/step-icons-target-lp-id.png" alt="Target license plate ID step icon" title="Kohdekäyttöoikeustunnuksen vaiheen kuvake"><br><span data-ttu-id="d0194-542">TargetLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="d0194-542">TargetLicensePlateId</span></span></td>
<td><img src="media/step-icons-to-line-no.png" alt="To line number step icon" title="Rivinumeroon -vaiheen kuvake"><br><span data-ttu-id="d0194-544">ToLineNum</span><span class="sxs-lookup"><span data-stu-id="d0194-544">ToLineNum</span></span></td>
<td><img src="media/step-icons-to-location.png" alt="To location step icon" title="Sijaintiin -vaiheen kuvake"><br><span data-ttu-id="d0194-546">ToLocation</span><span class="sxs-lookup"><span data-stu-id="d0194-546">ToLocation</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-to-number.png" alt="To number step icon" title="Numeroon -vaiheen kuvake"><br><span data-ttu-id="d0194-548">ToNum</span><span class="sxs-lookup"><span data-stu-id="d0194-548">ToNum</span></span></td>
<td><img src="media/step-icons-to-warehouse.png" alt="To warehouse step icon" title="Varastoon -vaiheen kuvake"><br><span data-ttu-id="d0194-550">ToWarehouse</span><span class="sxs-lookup"><span data-stu-id="d0194-550">ToWarehouse</span></span></td>
<td><img src="media/step-icons-tranport-load-id.png" alt="Transport load ID step icon" title="Välitä kuormatunnus -vaiheen kuvake"><br><span data-ttu-id="d0194-552">TransportLoadId</span><span class="sxs-lookup"><span data-stu-id="d0194-552">TransportLoadId</span></span></td>
<td><img src="media/step-icons-vendor-batch-id.png" alt="Vendor batch ID step icon" title="Toimittajaerän tunnuksen vaiheen kuvake"><br><span data-ttu-id="d0194-554">VendBatchId</span><span class="sxs-lookup"><span data-stu-id="d0194-554">VendBatchId</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-wave-label-id.png" alt="Wave label ID step icon" title="Aallon nimiketunnuksen vaiheen kuvake"><br><span data-ttu-id="d0194-556">WaveLabelId</span><span class="sxs-lookup"><span data-stu-id="d0194-556">WaveLabelId</span></span></td>
<td><img src="media/step-icons-wave-label-qty.png" alt="Wave label quantity step icon" title="Aallon nimikemäärän vaiheen kuvake"><br><span data-ttu-id="d0194-558">WaveLblQty</span><span class="sxs-lookup"><span data-stu-id="d0194-558">WaveLblQty</span></span></td>
<td><img src="media/step-icons-weight.png" alt="Weight step icon" title="Painon vaiheen kuvake"><br><span data-ttu-id="d0194-560">Paino</span><span class="sxs-lookup"><span data-stu-id="d0194-560">Weight</span></span></td>
<td><img src="media/step-icons-weight-to-consume.png" alt="Weight to consume step icon" title="Kulutettavan painon vaiheen kuvake"><br><span data-ttu-id="d0194-562">WeightToConsume</span><span class="sxs-lookup"><span data-stu-id="d0194-562">WeightToConsume</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-whs-adjustment-type.png" alt="WHS adjustment type step icon" title="WHS-oikaisutyypin vaiheen kuvake"><br><span data-ttu-id="d0194-564">WHSAdjustmentType</span><span class="sxs-lookup"><span data-stu-id="d0194-564">WHSAdjustmentType</span></span></td>
<td><img src="media/step-icons-whs-receiving-exception.png" alt="WHS receiving exception step icon" title="WHS-vastaanottopoikkeusvaiheen kuvake"><br><span data-ttu-id="d0194-566">WHSReceivingException</span><span class="sxs-lookup"><span data-stu-id="d0194-566">WHSReceivingException</span></span></td>
<td><img src="media/step-icons-wms-location-id.png" alt="WMS location ID step icon" title="WMS-sijainnin tunnus -vaiheen kuvake"><br><span data-ttu-id="d0194-568">WMSLocationID</span><span class="sxs-lookup"><span data-stu-id="d0194-568">WMSLocationID</span></span></td>
<td><img src="media/step-icons-work-id.png" alt="Work ID step icon" title="Työn tunnus -vaiheen kuvake"><br><span data-ttu-id="d0194-570">WorkId</span><span class="sxs-lookup"><span data-stu-id="d0194-570">WorkId</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-work-id-to-cancel.png" alt="Work ID to cancel step icon" title="Työtunnus, kun haluat peruuttaa vaiheen kuvakkeen"><br><span data-ttu-id="d0194-572">WorkIdToCancel</span><span class="sxs-lookup"><span data-stu-id="d0194-572">WorkIdToCancel</span></span></td>
<td><img src="media/step-icons-work-lp-id.png" alt="Work license plate ID step icon" title="Työn käyttöoikeustunnuksen vaiheen kuvake"><br><span data-ttu-id="d0194-574">WorkLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="d0194-574">WorkLicensePlateId</span></span></td>
<td><img src="media/step-icons-work-lp-putaway-cluster.png" alt="Work license plate ID putaway cluster step icon" title="Työn käyttöoikeustunnuksen säilytettävän klusterin vaiheen kuvake"><br><span data-ttu-id="d0194-576">WorkLPIDPutawayCluster</span><span class="sxs-lookup"><span data-stu-id="d0194-576">WorkLPIDPutawayCluster</span></span></td>
<td><img src="media/step-icons-work-pool-id.png" alt="Work pool ID step icon" title="Työpoolin tunnus -vaiheen kuvake"><br><span data-ttu-id="d0194-578">WorkPoolID</span><span class="sxs-lookup"><span data-stu-id="d0194-578">WorkPoolID</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-zone-pool-id.png" alt="Zone ID step icon" title="Vyöhyketunnus -vaiheen kuvake"><br><span data-ttu-id="d0194-580">ZoneID</span><span class="sxs-lookup"><span data-stu-id="d0194-580">ZoneID</span></span></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

## <a name="example-assign-step-icons-and-titles-for-a-custom-flow"></a><a name="example"></a><span data-ttu-id="d0194-581">Esimerkki: Mukautetun työnkulun vaihekuvakkeiden ja otsikoiden liittäminen</span><span class="sxs-lookup"><span data-stu-id="d0194-581">Example: Assign step icons and titles for a custom flow</span></span>

<span data-ttu-id="d0194-582">Tässä esimerkissä kerrotaan, miten mukautetun tehtävän työnkulun vaihekuvakkeet ja otsikot määritetään.</span><span class="sxs-lookup"><span data-stu-id="d0194-582">This example explains how to set up step icons and titles for a custom task flow.</span></span> <span data-ttu-id="d0194-583">Skenaario perustuu esimerkkiin mukautetusta tehtävätyönkulusta, joka esitellään ja johon voi tutustua tarkemmin seuraavassa kirjauksen esimerkissä: [Warehouse Mobile App -sovelluksen mukauttaminen](https://cloudblogs.microsoft.com/dynamics365/it/2017/07/06/customizing-the-warehousing-mobile-app).</span><span class="sxs-lookup"><span data-stu-id="d0194-583">The scenario is built on an example of a custom task flow that is presented and explored in more detail in the following blog post: [Customizing the Warehousing Mobile App](https://cloudblogs.microsoft.com/dynamics365/it/2017/07/06/customizing-the-warehousing-mobile-app).</span></span> <span data-ttu-id="d0194-584">Tehtävätyönkulku toimii seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="d0194-584">The task flow works in the following way:</span></span>

1. <span data-ttu-id="d0194-585">Sovellus näyttää sivun, joka kehottaa työntekijää antamaan säilötunnuksen (esimerkiksi skannaamalla viivakoodi).</span><span class="sxs-lookup"><span data-stu-id="d0194-585">The app shows a page that prompts the worker to provide a container ID (for example, by scanning a bar code).</span></span>
1. <span data-ttu-id="d0194-586">Jos säilön tunnus on kelvollinen, sovellus avaa uuden sivun, joka kysyy työntekijältä painoa.</span><span class="sxs-lookup"><span data-stu-id="d0194-586">If the container ID is valid, the app opens a new page that prompts the worker for the weight.</span></span> <span data-ttu-id="d0194-587">(Jos säilön tunnus ei kelpaa, työntekijä palautetaan ensimmäiselle sivulle.)</span><span class="sxs-lookup"><span data-stu-id="d0194-587">(If the container ID isn't valid, the worker is returned to the first page.)</span></span>
1. <span data-ttu-id="d0194-588">Kun työntekijä määrittää kelvollisen painon, järjestelmä tallentaa painon ja palauttaa työntekijän ensimmäiselle sivulle.</span><span class="sxs-lookup"><span data-stu-id="d0194-588">When the worker enters a valid weight, the system stores the weight and returns the worker to the first page.</span></span>

<span data-ttu-id="d0194-589">Seuraavassa kuvassa näkyy tämä tehtävätyönkulku.</span><span class="sxs-lookup"><span data-stu-id="d0194-589">The following illustration shows this task flow.</span></span>

<span data-ttu-id="d0194-590">![Tehtävän työnkulkukaavio](media/step-icons-example-task-flow.png "Tehtävän työnkulkukaavio")</span><span class="sxs-lookup"><span data-stu-id="d0194-590">![Task flow diagram](media/step-icons-example-task-flow.png "Task flow diagram")</span></span>

### <a name="create-a-step-class-for-the-container-input-page"></a><span data-ttu-id="d0194-591">Vaiheluokan luominen säilön syöttösivulle</span><span class="sxs-lookup"><span data-stu-id="d0194-591">Create a step class for the container input page</span></span>

<span data-ttu-id="d0194-592">Säilön syöttösivun avulla työntekijä voi skannata tai määrittää säilön tunnuksen.</span><span class="sxs-lookup"><span data-stu-id="d0194-592">The container input page lets the worker scan or enter a container ID.</span></span>

<span data-ttu-id="d0194-593">![Säilön syöttösivu](media/step-icons-example-container-input.png "Säilön syöttösivu")</span><span class="sxs-lookup"><span data-stu-id="d0194-593">![Container input page](media/step-icons-example-container-input.png "Container input page")</span></span>

<span data-ttu-id="d0194-594">Säilön syöttö -sivulla syöttökentän ohjausobjektinimi on `ContainerId`.</span><span class="sxs-lookup"><span data-stu-id="d0194-594">On the container input page, the control name of the input field is `ContainerId`.</span></span> <span data-ttu-id="d0194-595">Koska tätä ohjausobjektin nimeä ei ole [vaihetunnusten luettelossa](#step-ids-classes), siihen perustuvaa vaihetta ei etsitä.</span><span class="sxs-lookup"><span data-stu-id="d0194-595">Because this control name isn't in the [list of step IDs](#step-ids-classes), you won't find an existing step that is based on it.</span></span> <span data-ttu-id="d0194-596">Siksi sinun on luotava vaiheluokka, joka edustaa vaihetta.</span><span class="sxs-lookup"><span data-stu-id="d0194-596">Therefore, you must create a step class that represents the step.</span></span> <span data-ttu-id="d0194-597">Esimerkki:</span><span class="sxs-lookup"><span data-stu-id="d0194-597">Here is an example.</span></span>

```xpp
[WHSMobileAppStepId('ContainerId')]
final internal class WHSMobileAppStepContainerId extends WHSMobileAppStep
{
    private const WHSMobileAppStepIcon PopulationIcon = 'InventBatchID';
    private const WHSMobileAppStepTitle InputNotFilledTitle = "@WAX:WHSMobileAppStepContainerID_InputNotFilled"; //Scan a container
    protected void initValues()
    {
        defaultStepIcon = PopulationIcon;
        defaultStepTitle = InputNotFilledTitle;
    }
}
```

<span data-ttu-id="d0194-598">Vaiheen kuvakkeen tunnus tallennetaan `defaultStepIcon`-luokan jäseneksi ja vaiheen otsikko tallennetaan `defaultStepTitle`-luokan jäseneksi.</span><span class="sxs-lookup"><span data-stu-id="d0194-598">The identifier of the step icon is stored in the `defaultStepIcon` class member, and the step title is stored in the `defaultStepTitle` class member.</span></span>

<span data-ttu-id="d0194-599">Jos haluat määrittää vaihekuvakkeen, aseta `defaultStepIcon` jollekin kuvaketunnukselle, joita on lueteltu aiemmin tässä ohjeaiheessa olevassa [Käytettävissä olevan vaiheen kuvakkeet](#step-icons) -osassa.</span><span class="sxs-lookup"><span data-stu-id="d0194-599">To assign a step icon, set `defaultStepIcon` to one of the icon IDs that are listed in the [Available step icons](#step-icons) section earlier in this topic.</span></span>

### <a name="use-a-standard-or-custom-step-icon-and-title-for-the-weight-input"></a><span data-ttu-id="d0194-600">Painosyötön vakiokuvakkeen tai mukautetun vaiheen kuvakkeen ja otsikon käyttö</span><span class="sxs-lookup"><span data-stu-id="d0194-600">Use a standard or custom step icon and title for the weight input</span></span>

<span data-ttu-id="d0194-601">Painon syöttö -sivulla työntekijä voi määrittää painon.</span><span class="sxs-lookup"><span data-stu-id="d0194-601">The weight input page lets the worker enter a weight.</span></span>

<span data-ttu-id="d0194-602">![Painon syöttösivu](media/step-icons-example-weight-input.png "Painon syöttösivu")</span><span class="sxs-lookup"><span data-stu-id="d0194-602">![Weight input page](media/step-icons-example-weight-input.png "Weight input page")</span></span>

<span data-ttu-id="d0194-603">Painon syöttösivulla syöttökentän ohjausobjektinimi on `Weight`, joka on [vaihetunnusten luettelossa](#step-ids-classes).</span><span class="sxs-lookup"><span data-stu-id="d0194-603">On the weight input page, the control name of the input field is `Weight`, which is in the [list of step IDs](#step-ids-classes).</span></span> <span data-ttu-id="d0194-604">Jos voit hyväksyä `WHSMobileAppStepWeight`-luokassa määritetyn vaihekuvakkeen ja otsikon, sinun ei tarvitse muuttaa mitään tätä vaihetta varten.</span><span class="sxs-lookup"><span data-stu-id="d0194-604">Therefore, if the step icon and title that are defined in the `WHSMobileAppStepWeight` class are acceptable to you, you don't have to change anything for this step.</span></span>

<span data-ttu-id="d0194-605">Jos kuitenkin haluat käyttää tässä vaiheessa toista kuvaketta tai otsikkoa, voit ohittaa joko builder-luokan `stepId()`-menetelmän tai `stepInfo()`-menetelmän.</span><span class="sxs-lookup"><span data-stu-id="d0194-605">However, if you prefer to use a different icon or title for this step, you can override either the `stepId()` method or the `stepInfo()` method in the builder class.</span></span> <span data-ttu-id="d0194-606">Jokaisella tehtävätyönkululla on oma vaiheen tiedon muodostin.</span><span class="sxs-lookup"><span data-stu-id="d0194-606">Each task flow has its own step info builder.</span></span>

#### <a name="override-the-stepid-method"></a><span data-ttu-id="d0194-607">StepId()-menetelmän ohittaminen</span><span class="sxs-lookup"><span data-stu-id="d0194-607">Override the stepId() method</span></span>

<span data-ttu-id="d0194-608">Seuraavassa esimerkissä näkyy yksi tapa, jolla voit muokata muodostinluokkaa ohitamalla `stepId()`-menetelmän.</span><span class="sxs-lookup"><span data-stu-id="d0194-608">The following example shows one way that you can modify a builder class by overriding the `stepId()` method.</span></span>

```xpp
[WHSWorkExecuteMode(WHSWorkExecuteMode:: WeighContainer)]
public class WHSMobileAppStepInfoBuilderWeighContainer extends WHSMobileAppStepInfoBuilder
{
    protected WHSMobileAppStepId stepId()
    {
        WHSMobileAppStepId stepIdLocal = super();
        if (stepIdLocal == 'Weight')
        {
            return 'NewWeight';
        }
        return stepIdLocal;
    }
}
```

<span data-ttu-id="d0194-609">Sen jälkeen luot vaiheluokan `NewWeight`-vaiheelle.</span><span class="sxs-lookup"><span data-stu-id="d0194-609">You then create a step class for the `NewWeight` step.</span></span> <span data-ttu-id="d0194-610">Koodin pitäisi muistuttaa aiemmin tässä ohjeaiheessa näkyvää `ContainerId`-esimerkkiä.</span><span class="sxs-lookup"><span data-stu-id="d0194-610">The code should resemble the code for the `ContainerId` example that was shown earlier in this topic.</span></span>

#### <a name="override-the-stepinfo-method"></a><span data-ttu-id="d0194-611">StepInfo()-menetelmän ohittaminen</span><span class="sxs-lookup"><span data-stu-id="d0194-611">Override the stepInfo() method</span></span>

<span data-ttu-id="d0194-612">Seuraavassa esimerkissä näkyy yksi tapa, jolla voit muokata muodostinluokkaa ohitamalla `stepInfo()`-menetelmän.</span><span class="sxs-lookup"><span data-stu-id="d0194-612">The following example shows one way that you can modify a builder class by overriding the `stepInfo()` method.</span></span>

```xpp
[WHSWorkExecuteMode(WHSWorkExecuteMode:: WeighContainer)]
public class WHSMobileAppStepInfoBuilderWeighContainer extends WHSMobileAppStepInfoBuilder
{
    protected WHSMobileAppStepInfo stepInfo()
    {
        if (stepId != 'Weight')
        {
            return super();
        }
        WHSMobileAppStepInfo stepInfo = WHSMobileAppStepInfo::construct();
        stepInfo.parmStepIcon('NewIcon');
        stepInfo.parmStepTitle('NewTitle');
        return stepInfo;
    }
}
```

<span data-ttu-id="d0194-613">Sen jälkeen voit luoda `WHSMobileAppStepInfo`-objektin ja määrittää kuvakkeen ja/tai otsikon suoraan.</span><span class="sxs-lookup"><span data-stu-id="d0194-613">You then construct a `WHSMobileAppStepInfo` object, and set the icon and/or title directly.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d0194-614">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="d0194-614">Additional resources</span></span>

- [<span data-ttu-id="d0194-615">Varastonhallinnan mobiilisovelluksen asentaminen ja yhteyden muodostaminen</span><span class="sxs-lookup"><span data-stu-id="d0194-615">Install and connect the Warehouse Management mobile app</span></span>](install-configure-warehouse-management-app.md)
- [<span data-ttu-id="d0194-616">Mobiililaitteen käyttäjäasetukset</span><span class="sxs-lookup"><span data-stu-id="d0194-616">Mobile device user settings</span></span>](mobile-device-user-settings.md)
