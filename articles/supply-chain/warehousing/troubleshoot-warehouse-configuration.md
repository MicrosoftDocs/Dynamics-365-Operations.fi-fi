---
title: Varaston määrityksen vianmääritys
description: Tässä aiheessa käsitellään yleisiä ongelmia, joita voi esiintyä Microsoft Dynamics 365 Supply Chain Managementia määritettäessä.
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
ms.openlocfilehash: 09b5770190fea9591f422b61ce6deedb2b9fa790
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4994000"
---
# <a name="troubleshoot-warehouse-configuration"></a><span data-ttu-id="18831-103">Varaston määrityksen vianmääritys</span><span class="sxs-lookup"><span data-stu-id="18831-103">Troubleshoot warehouse configuration</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="18831-104">Tässä aiheessa käsitellään yleisiä ongelmia, joita voi esiintyä Microsoft Dynamics 365 Supply Chain Managementia määritettäessä.</span><span class="sxs-lookup"><span data-stu-id="18831-104">This topic describes how to fix common issues that you might encounter while you configure Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-the-license-plate-or-location-is-not-valid"></a><span data-ttu-id="18831-105">Seuraava virhesanoma avautuu: Rekisterikilpi tai sijainti ei kelpaa.</span><span class="sxs-lookup"><span data-stu-id="18831-105">I receive the following error message: "The license plate or location is not valid."</span></span>

### <a name="issue-description"></a><span data-ttu-id="18831-106">Ongelman kuvaus</span><span class="sxs-lookup"><span data-stu-id="18831-106">Issue description</span></span>

<span data-ttu-id="18831-107">Tämä virhesanoma avautuu,, kun rekisterikilven tunnus tai sijainti skannataan.</span><span class="sxs-lookup"><span data-stu-id="18831-107">You receive this error message when you scan a license plate ID or location.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="18831-108">Ongelman ratkaisu</span><span class="sxs-lookup"><span data-stu-id="18831-108">Issue resolution</span></span>

<span data-ttu-id="18831-109">Varmista, että mikään muu ei ole varannut rekisterikilven tunnusta.</span><span class="sxs-lookup"><span data-stu-id="18831-109">Make sure that the license plate ID isn't reserved by something else.</span></span> <span data-ttu-id="18831-110">Tämä ongelma esiintyi aiemmin, kun käyttäjän varastosovelluksessa skannaama arvo oli sekä kelvollinen sijainti että kelvollinen rekisterikilven tunnus.</span><span class="sxs-lookup"><span data-stu-id="18831-110">This issue used to occur when the value that a user scanned in the warehouse app was both a valid location and a valid license plate ID.</span></span> <span data-ttu-id="18831-111">Tämä ongelma kuitenkin korjattiin versiossa 10.0.11.</span><span class="sxs-lookup"><span data-stu-id="18831-111">However, this issue was resolved in version 10.0.11.</span></span>

## <a name="i-receive-the-following-error-message-license-plate-must-be-specified-for-this-location"></a><span data-ttu-id="18831-112">Seuraava virhesanoma avautuu: Tälle sijainnille on määritettävä rekisterikilpi.</span><span class="sxs-lookup"><span data-stu-id="18831-112">I receive the following error message: "License plate must be specified for this location."</span></span>

### <a name="issue-description"></a><span data-ttu-id="18831-113">Ongelman kuvaus</span><span class="sxs-lookup"><span data-stu-id="18831-113">Issue description</span></span>

<span data-ttu-id="18831-114">Tämä virhesanoma avautuu, jos siirtotilaus luodaan käyttämällä varastoa, jossa on otettu käyttöön edistyksellinen varastonhallinta, ja kun lähetystä yritetään vahvistaa työn valmistumisen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="18831-114">You receive this error message if you create a transfer order by using a warehouse that is enabled for advanced warehouse management (WMS), and then, after the work is completed, you try to confirm the shipment.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="18831-115">Ongelman ratkaisu</span><span class="sxs-lookup"><span data-stu-id="18831-115">Issue resolution</span></span>

<span data-ttu-id="18831-116">Lähtövaraston kuljetusvaraston **Oletusvastaanottosijainti** -kenttä on tyhjä.</span><span class="sxs-lookup"><span data-stu-id="18831-116">The **Default receipt location** field is blank for a transit warehouse of the "from" warehouse.</span></span> <span data-ttu-id="18831-117">Korjaa ongelma määrittämällä oletusvastaanottosijainti kuljetusvarastossa.</span><span class="sxs-lookup"><span data-stu-id="18831-117">To fix this issue, specify a default receipt location in the transit warehouse.</span></span> <span data-ttu-id="18831-118">Varmista, että tämä sijainti on rekisterikilpiohjattu.</span><span class="sxs-lookup"><span data-stu-id="18831-118">Make sure that this location is license plate–controlled.</span></span>

## <a name="i-receive-the-following-error-message-you-cant-create-a-work-template-line-for-inventory-status-change-because-the-work-type-is-not-valid-select-a-different-work-type"></a><span data-ttu-id="18831-119">Seuraava virhesanoma avautuu: Et voida luoda työmalliriviä kohteelle Varaston tilanmuutos, koska työtyyppi ei ole kelvollinen.</span><span class="sxs-lookup"><span data-stu-id="18831-119">I receive the following error message: "You can't create a work template line for Inventory status change because the work type is not valid.</span></span> <span data-ttu-id="18831-120">Valitse toinen työtyyppi.</span><span class="sxs-lookup"><span data-stu-id="18831-120">Select a different work type."</span></span>

### <a name="issue-description"></a><span data-ttu-id="18831-121">Ongelman kuvaus</span><span class="sxs-lookup"><span data-stu-id="18831-121">Issue description</span></span>

<span data-ttu-id="18831-122">Työmallissa ei voi valita *Varaston tilanmuutos* **Työmallin tiedot** -osan **Työtyyppi**-sarakkeessa.</span><span class="sxs-lookup"><span data-stu-id="18831-122">For a work template, you can't select *Inventory status change* in the **Work type** column of the **Work template details** section.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="18831-123">Ongelman ratkaisu</span><span class="sxs-lookup"><span data-stu-id="18831-123">Issue resolution</span></span>

<span data-ttu-id="18831-124">Tämä on suunniteltu ominaisuus.</span><span class="sxs-lookup"><span data-stu-id="18831-124">This behavior is by design.</span></span> <span data-ttu-id="18831-125">Vain järjestelmäprosessit käyttävät *Varaston tilanmuutos* -työtyyppiä.</span><span class="sxs-lookup"><span data-stu-id="18831-125">The *Inventory status change* work type is used only by system processes.</span></span> <span data-ttu-id="18831-126">Sitä ei voi määrittää.</span><span class="sxs-lookup"><span data-stu-id="18831-126">It can't be configured.</span></span> <span data-ttu-id="18831-127">Koska työtyyppiluettelo on korjattu luettelointina, lisäkohteita ei voi suodattaa pois avattavasta **Työtyyppi**-valikosta.</span><span class="sxs-lookup"><span data-stu-id="18831-127">Because the list of work types is fixed as an enumeration, the extra entries can't be filtered out of the **Work type** drop-down menu.</span></span>

## <a name="i-receive-the-following-error-message-the-quantity-is-not-valid-for-unit-1"></a><span data-ttu-id="18831-128">Seuraava virhesanoma avautuu: Yksikön 1% määrä ei kelpaa.</span><span class="sxs-lookup"><span data-stu-id="18831-128">I receive the following error message: "The Quantity is not valid for unit 1%."</span></span>

### <a name="issue-description"></a><span data-ttu-id="18831-129">Ongelman kuvaus</span><span class="sxs-lookup"><span data-stu-id="18831-129">Issue description</span></span>

<span data-ttu-id="18831-130">*Kpl*-yksikön määrä ei kelpaa, jos keräilytyössä on useita rekisterikilpiä yhdessä sijainnissa.</span><span class="sxs-lookup"><span data-stu-id="18831-130">The quantity isn't valid for the *ea* unit when there is picking work that has multiple license plates in one location.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="18831-131">Ongelman ratkaisu</span><span class="sxs-lookup"><span data-stu-id="18831-131">Issue resolution</span></span>

<span data-ttu-id="18831-132">Varmista, että vapautetun tuotteen tai tuotevariantin **Yksikön sarjaryhmän tunnus**- ja **Yksikkömuunnokset**-kentät on määritetty oikein.</span><span class="sxs-lookup"><span data-stu-id="18831-132">Verify that the **Unit sequence group ID** and **Unit conversions** fields on the released product or product variant are set correctly.</span></span>

<span data-ttu-id="18831-133">Huomaa, että virhesanomaa on parannettu versiossa 10.0.15 (katso [KB 4581627](https://fix.lcs.dynamics.com/Issue/Details/?bugId=486531)).</span><span class="sxs-lookup"><span data-stu-id="18831-133">Note that the error message has been improved in version 10.0.15 (see [KB 4581627](https://fix.lcs.dynamics.com/Issue/Details/?bugId=486531)).</span></span> <span data-ttu-id="18831-134">Uusi virhesanoma: Määrä ei kelpaa.</span><span class="sxs-lookup"><span data-stu-id="18831-134">The new error message is, "The quantity is not valid.</span></span> <span data-ttu-id="18831-135">Odotettiin %1 %2.</span><span class="sxs-lookup"><span data-stu-id="18831-135">Expected %1 %2."</span></span>

## <a name="in-location-directives-for-sales-order-put-work-the-multiple-sku-option-doesnt-evaluate-multiple-location-directive-actions"></a><span data-ttu-id="18831-136">Myyntilauksen hyllytystyön sijaintidirektiivien usean varastointiyksikön vaihtoehto ei arvioi usean sijaintidirektiivin toimintoja</span><span class="sxs-lookup"><span data-stu-id="18831-136">In location directives for sales order put work, the multiple SKU option doesn't evaluate multiple location directive actions.</span></span>

### <a name="issue-description"></a><span data-ttu-id="18831-137">Ongelman kuvaus</span><span class="sxs-lookup"><span data-stu-id="18831-137">Issue description</span></span>

<span data-ttu-id="18831-138">*Myyntitilaus*-työtilaustyötyypin ja *Asetus*-työtyypin sijaintidirektiivit eivät arvioi usean sijaintidirektiivin toimintoja, kun **Useita varastointiyksiköitä** -vaihtoehto on valittu.</span><span class="sxs-lookup"><span data-stu-id="18831-138">Location directives of the *Sales orders* work order type and the *Put* work type don't evaluate multiple location directive actions when the **Multiple SKU** option is selected.</span></span> <span data-ttu-id="18831-139">Vain ensimmäinen sijaintidirektiivin toiminto arvioidaan.</span><span class="sxs-lookup"><span data-stu-id="18831-139">Only the first location directive action is evaluated.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="18831-140">Ongelman ratkaisu</span><span class="sxs-lookup"><span data-stu-id="18831-140">Issue resolution</span></span>

<span data-ttu-id="18831-141">Versioon 10.0.15 on lisätty uusi toiminto, *Arvioi kaikki usean varastointiyksikön sijaintidirektiivien toiminnot* (katso [KB 4579866](https://fix.lcs.dynamics.com/Issue/Details?kb=4579866&bugId=475946&dbType=3&qc=1bc41a56de7a3ee419fa76397a6bf282fce5be9b93e427c08a6d916d1dfa3091)).</span><span class="sxs-lookup"><span data-stu-id="18831-141">A new feature, *Evaluate all actions for Multi SKU location directives*, has been added in version 10.0.15 (see [KB 4579866](https://fix.lcs.dynamics.com/Issue/Details?kb=4579866&bugId=475946&dbType=3&qc=1bc41a56de7a3ee419fa76397a6bf282fce5be9b93e427c08a6d916d1dfa3091)).</span></span> <span data-ttu-id="18831-142">Tämä toiminto arvioi kaikki usean varastointiyksikön sijaintidirektiivien toiminnot.</span><span class="sxs-lookup"><span data-stu-id="18831-142">This feature evaluates all actions for multi-SKU location directives.</span></span> <span data-ttu-id="18831-143">Jos tarvitse tätä toimintoa, ota se käyttöön [ominaisuuksien hallinnassa](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span><span class="sxs-lookup"><span data-stu-id="18831-143">If you require this feature, use [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) to turn it on.</span></span>

## <a name="i-cant-use-the-warehouse-app-to-do-partial-picking"></a><span data-ttu-id="18831-144">Varastosovellusta ei voi käyttää osittaiseen keräilyyn</span><span class="sxs-lookup"><span data-stu-id="18831-144">I can't use the warehouse app to do partial picking.</span></span>

### <a name="issue-description"></a><span data-ttu-id="18831-145">Ongelman kuvaus</span><span class="sxs-lookup"><span data-stu-id="18831-145">Issue description</span></span>

<span data-ttu-id="18831-146">Nimikkeiden ohittaminen ja osittainen keräily ei ole mahdollista myynti- ja siirtotilauksissa.</span><span class="sxs-lookup"><span data-stu-id="18831-146">For sales and transfer orders, you can't skip items and do partial picking.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="18831-147">Ongelman ratkaisu</span><span class="sxs-lookup"><span data-stu-id="18831-147">Issue resolution</span></span>

<span data-ttu-id="18831-148">Määritä **Mobiililaitteen valikkovaihtoehdot** -sivulla jokaisen myynti- tai siirtotilausten käsittelyä varten määritetyn valikkovaihtoehdon **Salli työn jakaminen** -asetukseksi *Kyllä* **Yleiset**-välilehdellä.</span><span class="sxs-lookup"><span data-stu-id="18831-148">On the **Mobile device menu items** page, for each menu item that is set up to process sales orders or transfer orders, set the **Allow splitting of work** option on the **General** FastTab to *Yes*.</span></span>

## <a name="how-can-i-do-an-inventory-status-change-for-partial-quantity-work"></a><span data-ttu-id="18831-149">Miten osittain määrän työn varaston tila muutetaan?</span><span class="sxs-lookup"><span data-stu-id="18831-149">How can I do an inventory status change for partial quantity work?</span></span>

### <a name="issue-description"></a><span data-ttu-id="18831-150">Ongelman kuvaus</span><span class="sxs-lookup"><span data-stu-id="18831-150">Issue description</span></span>

<span data-ttu-id="18831-151">Haluat tehdä erän osittaisen määrän varaston tilan muutoksen.</span><span class="sxs-lookup"><span data-stu-id="18831-151">You want to do an inventory status change for a partial quantity of a batch.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="18831-152">Ongelman ratkaisu</span><span class="sxs-lookup"><span data-stu-id="18831-152">Issue resolution</span></span>

<span data-ttu-id="18831-153">Varastosovellukseen voidaan luoda valikkovaihtoehto, jolla työntekijät voivat tehdä tämän muutoksen.</span><span class="sxs-lookup"><span data-stu-id="18831-153">To enable workers to make this change, you can create a menu item for the warehouse app.</span></span> <span data-ttu-id="18831-154">Luo (tai muokkaa) **Mobiililaitteen valikkovaihtoehdot** -sivulla valikkovaihtoehto, jossa on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="18831-154">On the **Mobile device menu items** page, create (or edit) a menu item that has the following settings:</span></span>

- <span data-ttu-id="18831-155">**Tila:** *Työ*</span><span class="sxs-lookup"><span data-stu-id="18831-155">**Mode:** *Work*</span></span>
- <span data-ttu-id="18831-156">**Käytä aiemmin luotua työtä:** *Ei*</span><span class="sxs-lookup"><span data-stu-id="18831-156">**Use existing work:** *No*</span></span>
- <span data-ttu-id="18831-157">**Työn luontiprosessi:** *Siirto*</span><span class="sxs-lookup"><span data-stu-id="18831-157">**Work creation process:** *Movement*</span></span>
- <span data-ttu-id="18831-158">**Näytä varaston tila:** *Kyllä*</span><span class="sxs-lookup"><span data-stu-id="18831-158">**Display inventory status:** *Yes*</span></span>

<span data-ttu-id="18831-159">Sivulla voi määrittää tarvittaessa myös muita kenttiä.</span><span class="sxs-lookup"><span data-stu-id="18831-159">You can set other fields on the page as you require.</span></span>
