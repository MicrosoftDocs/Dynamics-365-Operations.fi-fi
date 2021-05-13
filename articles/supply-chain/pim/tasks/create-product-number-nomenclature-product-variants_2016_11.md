---
title: Luo tuotenumeroiden nimikkeistö määritetyille tuotevarianteille
description: Tässä aiheessa kuvataan, miten tuotenumeroiden nimikkeistö määritetään konfiguroiduille tuotevarianteille ja miten se voidaan liittää konfiguroitavaan päätuotteeseen.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, EcoResNomenclature, EcoResProductListPage, EcoResProductDetails, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7ea30dc107213b1a2c6b2a109188066a6ea82159
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921008"
---
# <a name="create-a-product-number-nomenclature-for-configured-product-variants"></a><span data-ttu-id="85a58-103">Luo tuotenumeroiden nimikkeistö määritetyille tuotevarianteille</span><span class="sxs-lookup"><span data-stu-id="85a58-103">Create a product number nomenclature for configured product variants</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="85a58-104">Tässä aiheessa kuvataan, miten tuotenumeroiden nimikkeistö määritetään konfiguroiduille tuotevarianteille ja miten se voidaan liittää konfiguroitavaan päätuotteeseen.</span><span class="sxs-lookup"><span data-stu-id="85a58-104">This procedure shows you how to set up a product number nomenclature for configured product variants, and how it can be attached to a configurable product master.</span></span> <span data-ttu-id="85a58-105">Tässä ohjeaiheessa kerrotaan myös, miten tuotteen kokoonpanomallin osan konfiguraationimikkeistö rakennetaan.</span><span class="sxs-lookup"><span data-stu-id="85a58-105">This procedure also demonstrates how you can build a configuration nomenclature for a product configuration model component.</span></span> <span data-ttu-id="85a58-106">Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="85a58-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="85a58-107">Uusi tuotenumeroiden nimikkeistö on määritetty päätuotteelle D0004.</span><span class="sxs-lookup"><span data-stu-id="85a58-107">The new product number nomenclature is assigned to the D0004 product master.</span></span> <span data-ttu-id="85a58-108">Tuotesuunnittelija tekee yleensä tämän tehtävän.</span><span class="sxs-lookup"><span data-stu-id="85a58-108">This task would typically be done by a product designer.</span></span>

## <a name="create-a-product-number-nomenclature"></a><span data-ttu-id="85a58-109">Tuotenumeroiden nimikkeistön luominen</span><span class="sxs-lookup"><span data-stu-id="85a58-109">Create a product number nomenclature</span></span>

1. <span data-ttu-id="85a58-110">Valitse **Tuotetietojen hallinta \> Asetukset \> Tuotenimikkeistö**.</span><span class="sxs-lookup"><span data-stu-id="85a58-110">Go to **Product information management \> Setup \> Product nomenclature**.</span></span>
1. <span data-ttu-id="85a58-111">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="85a58-111">Select **New**.</span></span>
1. <span data-ttu-id="85a58-112">Kirjoita arvo **Nimi**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="85a58-112">In the **Name** field, type a value.</span></span>
1. <span data-ttu-id="85a58-113">Kirjoita **Kuvaus**-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="85a58-113">In the **Description** field, type a value.</span></span>
1. <span data-ttu-id="85a58-114">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="85a58-114">Select **Add**.</span></span>
1. <span data-ttu-id="85a58-115">Valitse **Päätuotteen numero**.</span><span class="sxs-lookup"><span data-stu-id="85a58-115">Select **Product master number**.</span></span>
1. <span data-ttu-id="85a58-116">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="85a58-116">Select **Add**.</span></span>
1. <span data-ttu-id="85a58-117">Valitse **Tekstivakio**.</span><span class="sxs-lookup"><span data-stu-id="85a58-117">Select **Text constant**.</span></span>
1. <span data-ttu-id="85a58-118">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="85a58-118">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="85a58-119">Kirjoita arvo **Teksti**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="85a58-119">In the **Text** field, type a value.</span></span>
1. <span data-ttu-id="85a58-120">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="85a58-120">Select **Add**.</span></span>
1. <span data-ttu-id="85a58-121">Valitse **Määritys**.</span><span class="sxs-lookup"><span data-stu-id="85a58-121">Select **Configuration**.</span></span>
1. <span data-ttu-id="85a58-122">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="85a58-122">Close the page.</span></span>

## <a name="assign-the-product-number-nomenclature-to-a-product-master"></a><span data-ttu-id="85a58-123">Tuotenumeroiden nimikkeistön määrittäminen päätuotteelle</span><span class="sxs-lookup"><span data-stu-id="85a58-123">Assign the product number nomenclature to a product master</span></span>

1. <span data-ttu-id="85a58-124">Valitse **Tuotetietojen hallinta \> Tuotteet \> Päätuotteet**.</span><span class="sxs-lookup"><span data-stu-id="85a58-124">Go to **Product information management \> Products \> Product masters**.</span></span>
1. <span data-ttu-id="85a58-125">Käytä pikasuodatinta tietueiden etsimiseen.</span><span class="sxs-lookup"><span data-stu-id="85a58-125">Use the Quick Filter to find records.</span></span> <span data-ttu-id="85a58-126">Voit esimerkiksi suodattaa **Tuotenumero**-kenttää arvolla D.</span><span class="sxs-lookup"><span data-stu-id="85a58-126">For example, filter on the **Product number** field with a value of 'D'.</span></span>
1. <span data-ttu-id="85a58-127">Valitse luettelossa valitulla rivillä oleva linkki.</span><span class="sxs-lookup"><span data-stu-id="85a58-127">In the list, select the link in the selected row.</span></span>
1. <span data-ttu-id="85a58-128">Valitse **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="85a58-128">Select **Edit**.</span></span>
1. <span data-ttu-id="85a58-129">Valitse **Käytä nimikkeistöä** -kentässä *Kyllä*.</span><span class="sxs-lookup"><span data-stu-id="85a58-129">Select *Yes* in the **Use nomenclature** field.</span></span>
1. <span data-ttu-id="85a58-130">Syötä tai valitse arvo **Tuotevariantin numeron nimikkeistö** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="85a58-130">In the **Product variant number nomenclature** field, enter or select a value.</span></span>
1. <span data-ttu-id="85a58-131">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="85a58-131">Close the page.</span></span>
1. <span data-ttu-id="85a58-132">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="85a58-132">Close the page.</span></span>

## <a name="create-nomenclature-for-a-product-configuration-model-component"></a><span data-ttu-id="85a58-133">Nimikkeistön luominen tuotemääritysmallin osalle</span><span class="sxs-lookup"><span data-stu-id="85a58-133">Create nomenclature for a product configuration model component</span></span>

1. <span data-ttu-id="85a58-134">Valitse **Tuotetietojen hallinta \> Tuotteet \> Tuotekonfiguraation mallit**.</span><span class="sxs-lookup"><span data-stu-id="85a58-134">Go to **Product information management \> Products \> Product configuration models**.</span></span>
1. <span data-ttu-id="85a58-135">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="85a58-135">In the list, find and select the desired record.</span></span>
1. <span data-ttu-id="85a58-136">Valitse luettelossa valitulla rivillä oleva linkki.</span><span class="sxs-lookup"><span data-stu-id="85a58-136">In the list, select the link in the selected row.</span></span>
1. <span data-ttu-id="85a58-137">Valitse **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="85a58-137">Select **Edit**.</span></span>
1. <span data-ttu-id="85a58-138">Valitse **Käytä konfiguraationimikkeistöä** -kentässä *Kyllä*.</span><span class="sxs-lookup"><span data-stu-id="85a58-138">Select *Yes* in the **Use configuration nomenclature** field.</span></span>
1. <span data-ttu-id="85a58-139">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="85a58-139">Select **Add**.</span></span>
1. <span data-ttu-id="85a58-140">Valitse **Määritteen arvo**.</span><span class="sxs-lookup"><span data-stu-id="85a58-140">Select **Attribute value**.</span></span>
1. <span data-ttu-id="85a58-141">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="85a58-141">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="85a58-142">Syötä tai valitse arvo kentässä **Määrite**.</span><span class="sxs-lookup"><span data-stu-id="85a58-142">In the **Attribute** field, enter or select a value.</span></span>
1. <span data-ttu-id="85a58-143">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="85a58-143">Select **Add**.</span></span>
1. <span data-ttu-id="85a58-144">Valitse **Tekstivakio**.</span><span class="sxs-lookup"><span data-stu-id="85a58-144">Select **Text constant**.</span></span>
1. <span data-ttu-id="85a58-145">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="85a58-145">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="85a58-146">Kirjoita arvo **Teksti**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="85a58-146">In the **Text** field, type a value.</span></span>
1. <span data-ttu-id="85a58-147">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="85a58-147">Select **Add**.</span></span>
1. <span data-ttu-id="85a58-148">Valitse **Määritteen arvo**.</span><span class="sxs-lookup"><span data-stu-id="85a58-148">Select **Attribute value**.</span></span>
1. <span data-ttu-id="85a58-149">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="85a58-149">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="85a58-150">Syötä tai valitse arvo kentässä **Määrite**.</span><span class="sxs-lookup"><span data-stu-id="85a58-150">In the **Attribute** field, enter or select a value.</span></span>
1. <span data-ttu-id="85a58-151">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="85a58-151">Select **Add**.</span></span>
1. <span data-ttu-id="85a58-152">Valitse **Tekstivakio**.</span><span class="sxs-lookup"><span data-stu-id="85a58-152">Select **Text constant**.</span></span>
1. <span data-ttu-id="85a58-153">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="85a58-153">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="85a58-154">Kirjoita arvo **Teksti**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="85a58-154">In the **Text** field, type a value.</span></span>
1. <span data-ttu-id="85a58-155">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="85a58-155">Select **Add**.</span></span>
1. <span data-ttu-id="85a58-156">Valitse **Määritteen arvo**.</span><span class="sxs-lookup"><span data-stu-id="85a58-156">Select **Attribute value**.</span></span>
1. <span data-ttu-id="85a58-157">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="85a58-157">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="85a58-158">Syötä tai valitse arvo kentässä **Määrite**.</span><span class="sxs-lookup"><span data-stu-id="85a58-158">In the **Attribute** field, enter or select a value.</span></span>
1. <span data-ttu-id="85a58-159">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="85a58-159">Select **Add**.</span></span>
1. <span data-ttu-id="85a58-160">Valitse **Tekstivakio**.</span><span class="sxs-lookup"><span data-stu-id="85a58-160">Select **Text constant**.</span></span>
1. <span data-ttu-id="85a58-161">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="85a58-161">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="85a58-162">Kirjoita arvo **Teksti**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="85a58-162">In the **Text** field, type a value.</span></span>
1. <span data-ttu-id="85a58-163">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="85a58-163">Select **Add**.</span></span>
1. <span data-ttu-id="85a58-164">Valitse **Määritteen arvo**.</span><span class="sxs-lookup"><span data-stu-id="85a58-164">Select **Attribute value**.</span></span>
1. <span data-ttu-id="85a58-165">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="85a58-165">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="85a58-166">Syötä tai valitse arvo kentässä **Määrite**.</span><span class="sxs-lookup"><span data-stu-id="85a58-166">In the **Attribute** field, enter or select a value.</span></span>
1. <span data-ttu-id="85a58-167">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="85a58-167">Select **Add**.</span></span>
1. <span data-ttu-id="85a58-168">Valitse **Tekstivakio**.</span><span class="sxs-lookup"><span data-stu-id="85a58-168">Select **Text constant**.</span></span>
1. <span data-ttu-id="85a58-169">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="85a58-169">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="85a58-170">Kirjoita arvo **Teksti**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="85a58-170">In the **Text** field, type a value.</span></span>
1. <span data-ttu-id="85a58-171">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="85a58-171">Select **Add**.</span></span>
1. <span data-ttu-id="85a58-172">Valitse **Numerosarjan arvo**.</span><span class="sxs-lookup"><span data-stu-id="85a58-172">Select **Number sequence value**.</span></span>
1. <span data-ttu-id="85a58-173">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="85a58-173">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="85a58-174">Anna tai valitse **Numerosarja**-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="85a58-174">In the **Number sequence** field, enter or select a value.</span></span>
1. <span data-ttu-id="85a58-175">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="85a58-175">Close the page.</span></span>
1. <span data-ttu-id="85a58-176">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="85a58-176">Close the page.</span></span>
1. <span data-ttu-id="85a58-177">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="85a58-177">Close the page.</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]