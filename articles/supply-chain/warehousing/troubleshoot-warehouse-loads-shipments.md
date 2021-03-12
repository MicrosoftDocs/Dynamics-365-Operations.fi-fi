---
title: Kuormituksen luomisen ja lähetysten vianmääritys
description: Tässä aiheessa käsitellään yleisiä ongelmia, joita voi esiintyä, kun kuormituksen luontia ja lähetyksiä käytetään Microsoft Dynamics 365 Supply Chain Managementissa.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: f49a91afe9281f912d6d3579ac8e52cb1d8e5b5d
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4994026"
---
# <a name="troubleshoot-load-building-and-shipments"></a><span data-ttu-id="e5db9-103">Kuormituksen luomisen ja lähetysten vianmääritys</span><span class="sxs-lookup"><span data-stu-id="e5db9-103">Troubleshoot load building and shipments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e5db9-104">Tässä aiheessa käsitellään yleisiä ongelmia, joita voi esiintyä, kun kuormituksen luontia ja lähetyksiä käytetään Microsoft Dynamics 365 Supply Chain Managementissa.</span><span class="sxs-lookup"><span data-stu-id="e5db9-104">This topic describes how to fix common issues that you might encounter while you work with load building and shipments in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-you-cant-create-a-load-line-for-this-order-line-because-it-contains-inventory-dimensions-that-are-invalid"></a><span data-ttu-id="e5db9-105">Seuraava virhesanoma avautuu: Et voi luoda tälle tilausriville kuormariviä, koska se sisältää virheellisiä varastodimensioita...</span><span class="sxs-lookup"><span data-stu-id="e5db9-105">I receive the following error message: "You can't create a load line for this order line because it contains inventory dimensions that are invalid..."</span></span>

### <a name="issue-description"></a><span data-ttu-id="e5db9-106">Ongelman kuvaus</span><span class="sxs-lookup"><span data-stu-id="e5db9-106">Issue description</span></span>

<span data-ttu-id="e5db9-107">Seuraava virhesanoma avautuu, kun yrität vapauttaa myyntitilauksen palautuksen varastoon:</span><span class="sxs-lookup"><span data-stu-id="e5db9-107">You receive the following error message when you try to release a return sales order to the warehouse:</span></span>

> <span data-ttu-id="e5db9-108">Et voi luoda tälle tilausriville kuormariviä, koska se sisältää virheellisiä varastodimensioita.</span><span class="sxs-lookup"><span data-stu-id="e5db9-108">You can't create a load line for this order line because it contains inventory dimensions that are invalid.</span></span> <span data-ttu-id="e5db9-109">Et voi viitata varastodimensioihin, jotka sijaitsevat varaushierarkiassa sijaintidimension alla.</span><span class="sxs-lookup"><span data-stu-id="e5db9-109">You can't reference inventory dimensions that are located below the location dimension in the reservation hierarchy.</span></span> <span data-ttu-id="e5db9-110">Poista virheelliset dimensiot tilausriviltä.</span><span class="sxs-lookup"><span data-stu-id="e5db9-110">Remove the invalid dimensions from the order line.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="e5db9-111">Ongelman ratkaisu</span><span class="sxs-lookup"><span data-stu-id="e5db9-111">Issue resolution</span></span>

<span data-ttu-id="e5db9-112">Tuote ei valitettavasti tue myynnin palautusprosessin kuorman käsittelyä.</span><span class="sxs-lookup"><span data-stu-id="e5db9-112">Unfortunately, the product doesn't support load processing for a sales return process.</span></span> <span data-ttu-id="e5db9-113">Niinpä myyntitilauksen palautusta ei voi vapauttaa varastoon.</span><span class="sxs-lookup"><span data-stu-id="e5db9-113">Therefore, you can't release the return sales order to the warehouse.</span></span>

<span data-ttu-id="e5db9-114">Myyntitilaustapahtumissa ei voi viitata varastodimensioihin, jotka sijaitsevat varaushierarkiassa **Sijainti**-dimension alla.</span><span class="sxs-lookup"><span data-stu-id="e5db9-114">On sales order transactions, you can't reference inventory dimensions that are located below the **Location** dimension in the reservation hierarchy.</span></span> <span data-ttu-id="e5db9-115">Ongelman ratkaisu on virheellisten dimensioiden poistaminen tilausriviltä.</span><span class="sxs-lookup"><span data-stu-id="e5db9-115">The resolution is to remove the invalid dimensions from the order line.</span></span>

## <a name="i-receive-the-following-error-message-one-of-the-lines-is-already-on-a-load-unable-to-release-to-warehouse"></a><span data-ttu-id="e5db9-116">Seuraava virhesanoma avautuu: Yksi riveistä on jo kuormassa.</span><span class="sxs-lookup"><span data-stu-id="e5db9-116">I receive the following error message: "One of the lines is already on a load.</span></span> <span data-ttu-id="e5db9-117">Vapautus varastoon ei onnistu.</span><span class="sxs-lookup"><span data-stu-id="e5db9-117">Unable to release to warehouse."</span></span>

### <a name="issue-description"></a><span data-ttu-id="e5db9-118">Ongelman kuvaus</span><span class="sxs-lookup"><span data-stu-id="e5db9-118">Issue description</span></span>

<span data-ttu-id="e5db9-119">Jos kuormat luodaan manuaalisesti tai jos prosessi määritetään siten, että kuormat on jo luotu ennen myyntitilausrivin kirjaamista, oletuksena on, että seuraava vapautus tehdään manuaalisesti ja että käytössä on kuorman reititys ja hinnoittelu.</span><span class="sxs-lookup"><span data-stu-id="e5db9-119">If you manually create loads, or if you set up the process so that loads are already created before sales order line entry occurs, the assumption is that the subsequent release will be done manually, and that the route and rating from the load will be used.</span></span>

<span data-ttu-id="e5db9-120">Mahdollinen on myös skenaario, jossa varastoon yritetään tehdä automaattinen vapautus mutta aaltoprosessi ei luo työtä.</span><span class="sxs-lookup"><span data-stu-id="e5db9-120">In another possible scenario, you're trying to do an automatic release to the warehouse, but the wave process failed to create work.</span></span> <span data-ttu-id="e5db9-121">Tämän vuoksi luodaan kuitenkin avoin lähetys tai kuorma.</span><span class="sxs-lookup"><span data-stu-id="e5db9-121">Therefore, an open shipment or load is still created.</span></span> <span data-ttu-id="e5db9-122">Tämä avoin lähetys tai kuorma estää seuraavat yritykset vapauttaa tilaus automaattisesti siihen asti, että avoin lähetys tai kuorma poistetaan tai aalto käsitellään uudelleen manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="e5db9-122">This open shipment or load then blocks subsequent attempts to automatically release the order until you either delete the open shipment or load, or manually reprocess the wave.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="e5db9-123">Ongelman ratkaisu</span><span class="sxs-lookup"><span data-stu-id="e5db9-123">Issue resolution</span></span>

<span data-ttu-id="e5db9-124">Vapautus voidaan tehdä myyntitilaussivulta tai automaattinen vapautus myyntitilauksen vapautussivulta vain siinä tapauksessa, että yhtään kuormaa ei ole ennen vapautusta varastoon.</span><span class="sxs-lookup"><span data-stu-id="e5db9-124">You can release from the sales order page, or automatic release can be done from the release sales order page, only if no load exists before the release to the warehouse.</span></span> <span data-ttu-id="e5db9-125">Kuorma luodaan automaattisesti aallon käsittelyn jälkeen.</span><span class="sxs-lookup"><span data-stu-id="e5db9-125">The load will automatically be created after the wave is processed.</span></span>

## <a name="i-receive-the-following-error-message-the-delivery-note-correction-cant-be-processed-the-delivery-note-only-contains-items-that-are-subject-to-warehouse-management-processes-as-these-are-not-supported-by-delivery-note-correction"></a><span data-ttu-id="e5db9-126">Seuraava virhesanoma avautuu: Toimitusilmoituksen korjausta ei voitu käsitellä.</span><span class="sxs-lookup"><span data-stu-id="e5db9-126">I receive the following error message: "The delivery note correction can't be processed.</span></span> <span data-ttu-id="e5db9-127">Toimitusilmoitus sisältää vain nimikkeet, jotka liittyvät varastonhallintaprosesseihin, koska toimitusilmoituksen korjaus ei tue niitä.</span><span class="sxs-lookup"><span data-stu-id="e5db9-127">The delivery note only contains items that are subject to warehouse management processes, as these are not supported by Delivery Note correction."</span></span>

### <a name="issue-description"></a><span data-ttu-id="e5db9-128">Ongelman kuvaus</span><span class="sxs-lookup"><span data-stu-id="e5db9-128">Issue description</span></span>

<span data-ttu-id="e5db9-129">Kirjattua toimitusilmoitusta ei voi peruuttaa, koska **Peruuta**-painike ei ole käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="e5db9-129">After you post a delivery note, you can't cancel it, because the **Cancel** button is unavailable.</span></span> <span data-ttu-id="e5db9-130">Toimitusilmoitusta ei voi myöskään korjata.</span><span class="sxs-lookup"><span data-stu-id="e5db9-130">You also can't correct the delivery note.</span></span> <span data-ttu-id="e5db9-131">Jos yrität sitä, kyseinen virhesanoma avautuu.</span><span class="sxs-lookup"><span data-stu-id="e5db9-131">If you try, you receive this error message.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="e5db9-132">Ongelman ratkaisu</span><span class="sxs-lookup"><span data-stu-id="e5db9-132">Issue resolution</span></span>

<span data-ttu-id="e5db9-133">Varastonhallintajärjestelmää käyttävien nimikkeiden kirjattujen pakkausluetteloiden korjaaminen edellyttää, että kirjaaminen tehdään kuormasta eikä suoraan tilauksesta.</span><span class="sxs-lookup"><span data-stu-id="e5db9-133">To correct posted packing slips for items that are enabled for advanced warehouse management (WMS), you must do the posting from the load, not directly from the order.</span></span>

## <a name="how-can-i-create-work-from-outbound-loads-instead-of-waves"></a><span data-ttu-id="e5db9-134">Miten työ luodaan lähtevistä kuormista ei aalloista?</span><span class="sxs-lookup"><span data-stu-id="e5db9-134">How can I create work from outbound loads instead of waves?</span></span>

### <a name="issue-description"></a><span data-ttu-id="e5db9-135">Ongelman kuvaus</span><span class="sxs-lookup"><span data-stu-id="e5db9-135">Issue description</span></span>

<span data-ttu-id="e5db9-136">Ongelman voi toisintaa esimerkiksi seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="e5db9-136">Here is one way to reproduce this issue.</span></span>

1. <span data-ttu-id="e5db9-137">Luo lähtevä kuorma käyttämällä myyntitilausta tai siirtotilausta.</span><span class="sxs-lookup"><span data-stu-id="e5db9-137">Create an outbound load by using a sales order or transfer order.</span></span>
2. <span data-ttu-id="e5db9-138">Vapauta kuorma varastoon.</span><span class="sxs-lookup"><span data-stu-id="e5db9-138">Release the load to the warehouse.</span></span>
3. <span data-ttu-id="e5db9-139">Huomaa, että keräilytyötä ei ole vielä luotu.</span><span class="sxs-lookup"><span data-stu-id="e5db9-139">Notice that no picking work has yet been generated.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="e5db9-140">Ongelman ratkaisu</span><span class="sxs-lookup"><span data-stu-id="e5db9-140">Issue resolution</span></span>

<span data-ttu-id="e5db9-141">Jos työ on luotava heti, kun kuorma vapautetaan, aaltomalli on määritettävä vastaavasti.</span><span class="sxs-lookup"><span data-stu-id="e5db9-141">If work must be generated immediately when the load is released, you must configure the wave template accordingly.</span></span> <span data-ttu-id="e5db9-142">Määritä aaltomallin seuraavissa asetuksissa *Kyllä*:</span><span class="sxs-lookup"><span data-stu-id="e5db9-142">On the wave template, set the following options to *Yes*:</span></span>

- <span data-ttu-id="e5db9-143">Automatisoi aallon luonti</span><span class="sxs-lookup"><span data-stu-id="e5db9-143">Automate wave creation</span></span>
- <span data-ttu-id="e5db9-144">Käsittele aalto, kun se vapautetaan varastoon</span><span class="sxs-lookup"><span data-stu-id="e5db9-144">Process wave at release to warehouse</span></span>
- <span data-ttu-id="e5db9-145">Automatisoi aallon vapautus</span><span class="sxs-lookup"><span data-stu-id="e5db9-145">Automate wave release</span></span>

## <a name="i-cant-re-release-a-partially-shipped-load"></a><span data-ttu-id="e5db9-146">Osittain lähetettyä kuormaa ei voi vapauttaa uudelleen</span><span class="sxs-lookup"><span data-stu-id="e5db9-146">I can't re-release a partially shipped load.</span></span>

### <a name="issue-description"></a><span data-ttu-id="e5db9-147">Ongelman kuvaus</span><span class="sxs-lookup"><span data-stu-id="e5db9-147">Issue description</span></span>

<span data-ttu-id="e5db9-148">Osittain lähetettyä kuormaa ei voi vapauttaa varastoon.</span><span class="sxs-lookup"><span data-stu-id="e5db9-148">You can't release a partially shipped load to the warehouse.</span></span> <span data-ttu-id="e5db9-149">Kun vapautus varastoon tehdään, Toiminto valmis -sanoma avautuu mutta mitään ei tapahdu eikä jäljellä olevalle määrälle luoda työtä.</span><span class="sxs-lookup"><span data-stu-id="e5db9-149">When you do the release to the warehouse, an "Operation complete" message appears, but nothing happens, and no work is created for the remaining quantity.</span></span> <span data-ttu-id="e5db9-150">Tämä ongelma esiintyy käytettäessä kuljetuskuormatoimintoa ja varaus on keskeneräinen.</span><span class="sxs-lookup"><span data-stu-id="e5db9-150">This issue occurs when you use transport load functionality and there is an incomplete reservation.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="e5db9-151">Ongelman ratkaisu</span><span class="sxs-lookup"><span data-stu-id="e5db9-151">Issue resolution</span></span>

<span data-ttu-id="e5db9-152">[KB 470069](https://fix.lcs.dynamics.com/Issue/Details?kb=4574490&bugId=470069&dbType=3&qc=84ce1e09d7032d8b8ef86f5a0c68b86badf3dfaf29686c5ebbe97c53c0957b5f) (Osittain lähetetyt kuormat voidaan uudelleenaallottaa ja -käsitellä) on korjattu [versiossa 10.0.15](../get-started/whats-new-scm-10-0-15.md).</span><span class="sxs-lookup"><span data-stu-id="e5db9-152">[KB issue 470069](https://fix.lcs.dynamics.com/Issue/Details?kb=4574490&bugId=470069&dbType=3&qc=84ce1e09d7032d8b8ef86f5a0c68b86badf3dfaf29686c5ebbe97c53c0957b5f) ("Partially shipped loads can be re-waved and re-processed") is fixed in [release 10.0.15](../get-started/whats-new-scm-10-0-15.md).</span></span>
