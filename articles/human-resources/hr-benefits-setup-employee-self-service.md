---
title: Työntekijän itsepalvelun määrittäminen
description: Microsoft Dynamics 365 Human Resources -ohjelmassa voit määrittää ylimmän tason siirtymisruudut työntekijän itsepalvelussa.
author: andreabichsel
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 1f0d39b30b7c8d0a5729ebe3b1ed9e0d569a6660
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/18/2021
ms.locfileid: "6052982"
---
# <a name="configure-employee-self-service"></a><span data-ttu-id="b91b8-103">Työntekijän itsepalvelun määrittäminen</span><span class="sxs-lookup"><span data-stu-id="b91b8-103">Configure employee self service</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="b91b8-104">Microsoft Dynamics 365 Human Resources -ohjelmassa voit määrittää ylimmän tason siirtymisruudut työntekijän itsepalvelussa.</span><span class="sxs-lookup"><span data-stu-id="b91b8-104">In Microsoft Dynamics 365 Human Resources, you can configure tiles for top-level navigation in Employee self service.</span></span> <span data-ttu-id="b91b8-105">Etuussuunnitelmaruudut ohjaavat käyttäjät etuussuunnitelmiin, joihin he ovat oikeutettuja.</span><span class="sxs-lookup"><span data-stu-id="b91b8-105">Benefit plan tiles direct users to benefit plans that they're eligible for.</span></span>

## <a name="set-up-a-benefit-plans-tile"></a><span data-ttu-id="b91b8-106">Etuussuunnitelmien ruudun määrittäminen</span><span class="sxs-lookup"><span data-stu-id="b91b8-106">Set up a benefit plans tile</span></span>

1. <span data-ttu-id="b91b8-107">Valitse **Etujen hallinta** -työtilassa **Asetukset**-kohdasta **Työntekijän itsepalvelun parametrit**.</span><span class="sxs-lookup"><span data-stu-id="b91b8-107">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="b91b8-108">Valitse **Etuussuunnitelmien ruudun asetukset** -välilehti ja valitse sitten **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="b91b8-108">Select the **Benefit plans tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="b91b8-109">Määritä seuraavien kenttien arvot.</span><span class="sxs-lookup"><span data-stu-id="b91b8-109">Specify values for the following fields:</span></span>

   | <span data-ttu-id="b91b8-110">Kenttä</span><span class="sxs-lookup"><span data-stu-id="b91b8-110">Field</span></span> | <span data-ttu-id="b91b8-111">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="b91b8-111">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="b91b8-112">**Ruudun tunnus**</span><span class="sxs-lookup"><span data-stu-id="b91b8-112">**Tile ID**</span></span> | <span data-ttu-id="b91b8-113">Ruudun yksilöivä tunniste.</span><span class="sxs-lookup"><span data-stu-id="b91b8-113">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="b91b8-114">**Ruudun selitteen teksti**</span><span class="sxs-lookup"><span data-stu-id="b91b8-114">**Tile label text**</span></span> | <span data-ttu-id="b91b8-115">Teksti, joka tulee näkyviin itsepalvelun ruudussa.</span><span class="sxs-lookup"><span data-stu-id="b91b8-115">The text that will appear for the tile on Self-service.</span></span> |
   | <span data-ttu-id="b91b8-116">**Kuvaus**</span><span class="sxs-lookup"><span data-stu-id="b91b8-116">**Description**</span></span> | <span data-ttu-id="b91b8-117">Ruudun kuvaus.</span><span class="sxs-lookup"><span data-stu-id="b91b8-117">A description of the tile.</span></span> |
   | <span data-ttu-id="b91b8-118">**Internet-osoite**</span><span class="sxs-lookup"><span data-stu-id="b91b8-118">**Internet address**</span></span> | <span data-ttu-id="b91b8-119">Kirjoita työntekijän itsepalvelusivun URL-osoite.</span><span class="sxs-lookup"><span data-stu-id="b91b8-119">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="b91b8-120">**Ruudun koko**</span><span class="sxs-lookup"><span data-stu-id="b91b8-120">**Tile size**</span></span> | <span data-ttu-id="b91b8-121">Ruudun koko: pieni, keskikokoinen tai suuri.</span><span class="sxs-lookup"><span data-stu-id="b91b8-121">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="b91b8-122">**Kohde**</span><span class="sxs-lookup"><span data-stu-id="b91b8-122">**Target**</span></span> | <span data-ttu-id="b91b8-123">Määrittää, avataanko sivu uudessa ikkunassa vai nykyisessä ikkunassa.</span><span class="sxs-lookup"><span data-stu-id="b91b8-123">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="b91b8-124">**Ruudun taustakuva**</span><span class="sxs-lookup"><span data-stu-id="b91b8-124">**Tile background image**</span></span> | <span data-ttu-id="b91b8-125">Ruudussa käytettävän kuvan URL-osoite (valinnainen).</span><span class="sxs-lookup"><span data-stu-id="b91b8-125">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="b91b8-126">**Alku**</span><span class="sxs-lookup"><span data-stu-id="b91b8-126">**Start**</span></span> | <span data-ttu-id="b91b8-127">Aloituspäivämäärä ja -kellonaika, jolloin laatta on käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="b91b8-127">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="b91b8-128">**End-näppäin**</span><span class="sxs-lookup"><span data-stu-id="b91b8-128">**End**</span></span> | <span data-ttu-id="b91b8-129">Lopetuspäivämäärä ja -kellonaika, jolloin laatta on käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="b91b8-129">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="b91b8-130">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="b91b8-130">Select **Save**.</span></span>

## <a name="set-up-a-flex-credit-plan-tile"></a><span data-ttu-id="b91b8-131">Joustoluottosuunnitelman ruudun määrittäminen</span><span class="sxs-lookup"><span data-stu-id="b91b8-131">Set up a flex credit plan tile</span></span>

1. <span data-ttu-id="b91b8-132">Valitse **Etujen hallinta** -työtilassa **Asetukset**-kohdasta **Työntekijän itsepalvelun parametrit**.</span><span class="sxs-lookup"><span data-stu-id="b91b8-132">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="b91b8-133">Valitse **Joustoluottosuunnitelman ruudun asetukset** -välilehti ja valitse sitten **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="b91b8-133">Select the **Flex credit plan tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="b91b8-134">Määritä seuraavien kenttien arvot.</span><span class="sxs-lookup"><span data-stu-id="b91b8-134">Specify values for the following fields:</span></span>

   | <span data-ttu-id="b91b8-135">Kenttä</span><span class="sxs-lookup"><span data-stu-id="b91b8-135">Field</span></span> | <span data-ttu-id="b91b8-136">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="b91b8-136">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="b91b8-137">**Ruudun tunnus**</span><span class="sxs-lookup"><span data-stu-id="b91b8-137">**Tile ID**</span></span> | <span data-ttu-id="b91b8-138">Ruudun yksilöivä tunniste.</span><span class="sxs-lookup"><span data-stu-id="b91b8-138">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="b91b8-139">**Ruudun selitteen teksti**</span><span class="sxs-lookup"><span data-stu-id="b91b8-139">**Tile label text**</span></span> | <span data-ttu-id="b91b8-140">Teksti, joka tulee näkyviin itsepalvelun ruudussa.</span><span class="sxs-lookup"><span data-stu-id="b91b8-140">The text that will appear for the tile on Self service.</span></span> |
   | <span data-ttu-id="b91b8-141">**Kuvaus**</span><span class="sxs-lookup"><span data-stu-id="b91b8-141">**Description**</span></span> | <span data-ttu-id="b91b8-142">Ruudun kuvaus.</span><span class="sxs-lookup"><span data-stu-id="b91b8-142">A description of the tile.</span></span> |
   | <span data-ttu-id="b91b8-143">**Internet-osoite**</span><span class="sxs-lookup"><span data-stu-id="b91b8-143">**Internet address**</span></span> | <span data-ttu-id="b91b8-144">Kirjoita työntekijän itsepalvelusivun URL-osoite.</span><span class="sxs-lookup"><span data-stu-id="b91b8-144">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="b91b8-145">**Ruudun koko**</span><span class="sxs-lookup"><span data-stu-id="b91b8-145">**Tile size**</span></span> | <span data-ttu-id="b91b8-146">Ruudun koko: pieni, keskikokoinen tai suuri.</span><span class="sxs-lookup"><span data-stu-id="b91b8-146">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="b91b8-147">**Kohde**</span><span class="sxs-lookup"><span data-stu-id="b91b8-147">**Target**</span></span> | <span data-ttu-id="b91b8-148">Määrittää, avataanko sivu uudessa ikkunassa vai nykyisessä ikkunassa.</span><span class="sxs-lookup"><span data-stu-id="b91b8-148">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="b91b8-149">**Ruudun taustakuva**</span><span class="sxs-lookup"><span data-stu-id="b91b8-149">**Tile background image**</span></span> | <span data-ttu-id="b91b8-150">Ruudussa käytettävän kuvan URL-osoite (valinnainen).</span><span class="sxs-lookup"><span data-stu-id="b91b8-150">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="b91b8-151">**Alku**</span><span class="sxs-lookup"><span data-stu-id="b91b8-151">**Start**</span></span> | <span data-ttu-id="b91b8-152">Aloituspäivämäärä ja -kellonaika, jolloin laatta on käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="b91b8-152">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="b91b8-153">**End-näppäin**</span><span class="sxs-lookup"><span data-stu-id="b91b8-153">**End**</span></span> | <span data-ttu-id="b91b8-154">Lopetuspäivämäärä ja -kellonaika, jolloin laatta on käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="b91b8-154">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="b91b8-155">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="b91b8-155">Select **Save**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]