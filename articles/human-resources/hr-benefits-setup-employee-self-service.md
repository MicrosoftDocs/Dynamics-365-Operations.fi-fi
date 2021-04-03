---
title: Työntekijän itsepalvelun määrittäminen
description: Microsoft Dynamics 365 Human Resources -ohjelmassa voit määrittää ylimmän tason siirtymisruudut työntekijän itsepalvelussa.
author: andreabichsel
manager: tfehr
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c4fe8f7afd4b77636ce77e58a2e75196fddae132
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/17/2021
ms.locfileid: "5466107"
---
# <a name="configure-employee-self-service"></a><span data-ttu-id="a069a-103">Työntekijän itsepalvelun määrittäminen</span><span class="sxs-lookup"><span data-stu-id="a069a-103">Configure employee self service</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="a069a-104">Microsoft Dynamics 365 Human Resources -ohjelmassa voit määrittää ylimmän tason siirtymisruudut työntekijän itsepalvelussa.</span><span class="sxs-lookup"><span data-stu-id="a069a-104">In Microsoft Dynamics 365 Human Resources, you can configure tiles for top-level navigation in Employee self service.</span></span> <span data-ttu-id="a069a-105">Etuussuunnitelmaruudut ohjaavat käyttäjät etuussuunnitelmiin, joihin he ovat oikeutettuja.</span><span class="sxs-lookup"><span data-stu-id="a069a-105">Benefit plan tiles direct users to benefit plans that they're eligible for.</span></span>

## <a name="set-up-a-benefit-plans-tile"></a><span data-ttu-id="a069a-106">Etuussuunnitelmien ruudun määrittäminen</span><span class="sxs-lookup"><span data-stu-id="a069a-106">Set up a benefit plans tile</span></span>

1. <span data-ttu-id="a069a-107">Valitse **Etujen hallinta** -työtilassa **Asetukset**-kohdasta **Työntekijän itsepalvelun parametrit**.</span><span class="sxs-lookup"><span data-stu-id="a069a-107">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="a069a-108">Valitse **Etuussuunnitelmien ruudun asetukset** -välilehti ja valitse sitten **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="a069a-108">Select the **Benefit plans tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="a069a-109">Määritä seuraavien kenttien arvot.</span><span class="sxs-lookup"><span data-stu-id="a069a-109">Specify values for the following fields:</span></span>

   | <span data-ttu-id="a069a-110">Kenttä</span><span class="sxs-lookup"><span data-stu-id="a069a-110">Field</span></span> | <span data-ttu-id="a069a-111">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="a069a-111">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="a069a-112">**Ruudun tunnus**</span><span class="sxs-lookup"><span data-stu-id="a069a-112">**Tile ID**</span></span> | <span data-ttu-id="a069a-113">Ruudun yksilöivä tunniste.</span><span class="sxs-lookup"><span data-stu-id="a069a-113">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="a069a-114">**Ruudun selitteen teksti**</span><span class="sxs-lookup"><span data-stu-id="a069a-114">**Tile label text**</span></span> | <span data-ttu-id="a069a-115">Teksti, joka tulee näkyviin itsepalvelun ruudussa.</span><span class="sxs-lookup"><span data-stu-id="a069a-115">The text that will appear for the tile on Self-service.</span></span> |
   | <span data-ttu-id="a069a-116">**Kuvaus**</span><span class="sxs-lookup"><span data-stu-id="a069a-116">**Description**</span></span> | <span data-ttu-id="a069a-117">Ruudun kuvaus.</span><span class="sxs-lookup"><span data-stu-id="a069a-117">A description of the tile.</span></span> |
   | <span data-ttu-id="a069a-118">**Internet-osoite**</span><span class="sxs-lookup"><span data-stu-id="a069a-118">**Internet address**</span></span> | <span data-ttu-id="a069a-119">Kirjoita työntekijän itsepalvelusivun URL-osoite.</span><span class="sxs-lookup"><span data-stu-id="a069a-119">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="a069a-120">**Ruudun koko**</span><span class="sxs-lookup"><span data-stu-id="a069a-120">**Tile size**</span></span> | <span data-ttu-id="a069a-121">Ruudun koko: pieni, keskikokoinen tai suuri.</span><span class="sxs-lookup"><span data-stu-id="a069a-121">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="a069a-122">**Kohde**</span><span class="sxs-lookup"><span data-stu-id="a069a-122">**Target**</span></span> | <span data-ttu-id="a069a-123">Määrittää, avataanko sivu uudessa ikkunassa vai nykyisessä ikkunassa.</span><span class="sxs-lookup"><span data-stu-id="a069a-123">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="a069a-124">**Ruudun taustakuva**</span><span class="sxs-lookup"><span data-stu-id="a069a-124">**Tile background image**</span></span> | <span data-ttu-id="a069a-125">Ruudussa käytettävän kuvan URL-osoite (valinnainen).</span><span class="sxs-lookup"><span data-stu-id="a069a-125">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="a069a-126">**Alku**</span><span class="sxs-lookup"><span data-stu-id="a069a-126">**Start**</span></span> | <span data-ttu-id="a069a-127">Aloituspäivämäärä ja -kellonaika, jolloin laatta on käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="a069a-127">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="a069a-128">**End-näppäin**</span><span class="sxs-lookup"><span data-stu-id="a069a-128">**End**</span></span> | <span data-ttu-id="a069a-129">Lopetuspäivämäärä ja -kellonaika, jolloin laatta on käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="a069a-129">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="a069a-130">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="a069a-130">Select **Save**.</span></span>

## <a name="set-up-a-flex-credit-plan-tile"></a><span data-ttu-id="a069a-131">Joustoluottosuunnitelman ruudun määrittäminen</span><span class="sxs-lookup"><span data-stu-id="a069a-131">Set up a flex credit plan tile</span></span>

1. <span data-ttu-id="a069a-132">Valitse **Etujen hallinta** -työtilassa **Asetukset**-kohdasta **Työntekijän itsepalvelun parametrit**.</span><span class="sxs-lookup"><span data-stu-id="a069a-132">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="a069a-133">Valitse **Joustoluottosuunnitelman ruudun asetukset** -välilehti ja valitse sitten **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="a069a-133">Select the **Flex credit plan tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="a069a-134">Määritä seuraavien kenttien arvot.</span><span class="sxs-lookup"><span data-stu-id="a069a-134">Specify values for the following fields:</span></span>

   | <span data-ttu-id="a069a-135">Kenttä</span><span class="sxs-lookup"><span data-stu-id="a069a-135">Field</span></span> | <span data-ttu-id="a069a-136">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="a069a-136">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="a069a-137">**Ruudun tunnus**</span><span class="sxs-lookup"><span data-stu-id="a069a-137">**Tile ID**</span></span> | <span data-ttu-id="a069a-138">Ruudun yksilöivä tunniste.</span><span class="sxs-lookup"><span data-stu-id="a069a-138">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="a069a-139">**Ruudun selitteen teksti**</span><span class="sxs-lookup"><span data-stu-id="a069a-139">**Tile label text**</span></span> | <span data-ttu-id="a069a-140">Teksti, joka tulee näkyviin itsepalvelun ruudussa.</span><span class="sxs-lookup"><span data-stu-id="a069a-140">The text that will appear for the tile on Self service.</span></span> |
   | <span data-ttu-id="a069a-141">**Kuvaus**</span><span class="sxs-lookup"><span data-stu-id="a069a-141">**Description**</span></span> | <span data-ttu-id="a069a-142">Ruudun kuvaus.</span><span class="sxs-lookup"><span data-stu-id="a069a-142">A description of the tile.</span></span> |
   | <span data-ttu-id="a069a-143">**Internet-osoite**</span><span class="sxs-lookup"><span data-stu-id="a069a-143">**Internet address**</span></span> | <span data-ttu-id="a069a-144">Kirjoita työntekijän itsepalvelusivun URL-osoite.</span><span class="sxs-lookup"><span data-stu-id="a069a-144">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="a069a-145">**Ruudun koko**</span><span class="sxs-lookup"><span data-stu-id="a069a-145">**Tile size**</span></span> | <span data-ttu-id="a069a-146">Ruudun koko: pieni, keskikokoinen tai suuri.</span><span class="sxs-lookup"><span data-stu-id="a069a-146">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="a069a-147">**Kohde**</span><span class="sxs-lookup"><span data-stu-id="a069a-147">**Target**</span></span> | <span data-ttu-id="a069a-148">Määrittää, avataanko sivu uudessa ikkunassa vai nykyisessä ikkunassa.</span><span class="sxs-lookup"><span data-stu-id="a069a-148">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="a069a-149">**Ruudun taustakuva**</span><span class="sxs-lookup"><span data-stu-id="a069a-149">**Tile background image**</span></span> | <span data-ttu-id="a069a-150">Ruudussa käytettävän kuvan URL-osoite (valinnainen).</span><span class="sxs-lookup"><span data-stu-id="a069a-150">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="a069a-151">**Alku**</span><span class="sxs-lookup"><span data-stu-id="a069a-151">**Start**</span></span> | <span data-ttu-id="a069a-152">Aloituspäivämäärä ja -kellonaika, jolloin laatta on käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="a069a-152">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="a069a-153">**End-näppäin**</span><span class="sxs-lookup"><span data-stu-id="a069a-153">**End**</span></span> | <span data-ttu-id="a069a-154">Lopetuspäivämäärä ja -kellonaika, jolloin laatta on käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="a069a-154">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="a069a-155">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="a069a-155">Select **Save**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]