---
title: Työntekijän itsepalvelun määrittäminen
description: Microsoft Dynamics 365 Human Resources -ohjelmassa voit määrittää ylimmän tason siirtymisruudut työntekijän itsepalvelussa.
author: andreabichsel
manager: AnnBe
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
ms.openlocfilehash: d1534e37e83e22dd9860de54165c062935db3798
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4418378"
---
# <a name="configure-employee-self-service"></a><span data-ttu-id="74a48-103">Työntekijän itsepalvelun määrittäminen</span><span class="sxs-lookup"><span data-stu-id="74a48-103">Configure employee self service</span></span>

<span data-ttu-id="74a48-104">Microsoft Dynamics 365 Human Resources -ohjelmassa voit määrittää ylimmän tason siirtymisruudut työntekijän itsepalvelussa.</span><span class="sxs-lookup"><span data-stu-id="74a48-104">In Microsoft Dynamics 365 Human Resources, you can configure tiles for top-level navigation in Employee self service.</span></span> <span data-ttu-id="74a48-105">Etuussuunnitelmaruudut ohjaavat käyttäjät etuussuunnitelmiin, joihin he ovat oikeutettuja.</span><span class="sxs-lookup"><span data-stu-id="74a48-105">Benefit plan tiles direct users to benefit plans that they're eligible for.</span></span>

## <a name="set-up-a-benefit-plans-tile"></a><span data-ttu-id="74a48-106">Etuussuunnitelmien ruudun määrittäminen</span><span class="sxs-lookup"><span data-stu-id="74a48-106">Set up a benefit plans tile</span></span>

1. <span data-ttu-id="74a48-107">Valitse **Etujen hallinta** -työtilassa **Asetukset**-kohdasta **Työntekijän itsepalvelun parametrit**.</span><span class="sxs-lookup"><span data-stu-id="74a48-107">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="74a48-108">Valitse **Etuussuunnitelmien ruudun asetukset** -välilehti ja valitse sitten **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="74a48-108">Select the **Benefit plans tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="74a48-109">Määritä seuraavien kenttien arvot.</span><span class="sxs-lookup"><span data-stu-id="74a48-109">Specify values for the following fields:</span></span>

   | <span data-ttu-id="74a48-110">Kenttä</span><span class="sxs-lookup"><span data-stu-id="74a48-110">Field</span></span> | <span data-ttu-id="74a48-111">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="74a48-111">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="74a48-112">**Ruudun tunnus**</span><span class="sxs-lookup"><span data-stu-id="74a48-112">**Tile ID**</span></span> | <span data-ttu-id="74a48-113">Ruudun yksilöivä tunniste.</span><span class="sxs-lookup"><span data-stu-id="74a48-113">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="74a48-114">**Ruudun selitteen teksti**</span><span class="sxs-lookup"><span data-stu-id="74a48-114">**Tile label text**</span></span> | <span data-ttu-id="74a48-115">Teksti, joka tulee näkyviin itsepalvelun ruudussa.</span><span class="sxs-lookup"><span data-stu-id="74a48-115">The text that will appear for the tile on Self-service.</span></span> |
   | <span data-ttu-id="74a48-116">**Kuvaus**</span><span class="sxs-lookup"><span data-stu-id="74a48-116">**Description**</span></span> | <span data-ttu-id="74a48-117">Ruudun kuvaus.</span><span class="sxs-lookup"><span data-stu-id="74a48-117">A description of the tile.</span></span> |
   | <span data-ttu-id="74a48-118">**Internet-osoite**</span><span class="sxs-lookup"><span data-stu-id="74a48-118">**Internet address**</span></span> | <span data-ttu-id="74a48-119">Kirjoita työntekijän itsepalvelusivun URL-osoite.</span><span class="sxs-lookup"><span data-stu-id="74a48-119">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="74a48-120">**Ruudun koko**</span><span class="sxs-lookup"><span data-stu-id="74a48-120">**Tile size**</span></span> | <span data-ttu-id="74a48-121">Ruudun koko: pieni, keskikokoinen tai suuri.</span><span class="sxs-lookup"><span data-stu-id="74a48-121">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="74a48-122">**Kohde**</span><span class="sxs-lookup"><span data-stu-id="74a48-122">**Target**</span></span> | <span data-ttu-id="74a48-123">Määrittää, avataanko sivu uudessa ikkunassa vai nykyisessä ikkunassa.</span><span class="sxs-lookup"><span data-stu-id="74a48-123">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="74a48-124">**Ruudun taustakuva**</span><span class="sxs-lookup"><span data-stu-id="74a48-124">**Tile background image**</span></span> | <span data-ttu-id="74a48-125">Ruudussa käytettävän kuvan URL-osoite (valinnainen).</span><span class="sxs-lookup"><span data-stu-id="74a48-125">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="74a48-126">**Alku**</span><span class="sxs-lookup"><span data-stu-id="74a48-126">**Start**</span></span> | <span data-ttu-id="74a48-127">Aloituspäivämäärä ja -kellonaika, jolloin laatta on käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="74a48-127">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="74a48-128">**End-näppäin**</span><span class="sxs-lookup"><span data-stu-id="74a48-128">**End**</span></span> | <span data-ttu-id="74a48-129">Lopetuspäivämäärä ja -kellonaika, jolloin laatta on käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="74a48-129">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="74a48-130">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="74a48-130">Select **Save**.</span></span>

## <a name="set-up-a-flex-credit-plan-tile"></a><span data-ttu-id="74a48-131">Joustoluottosuunnitelman ruudun määrittäminen</span><span class="sxs-lookup"><span data-stu-id="74a48-131">Set up a flex credit plan tile</span></span>

1. <span data-ttu-id="74a48-132">Valitse **Etujen hallinta** -työtilassa **Asetukset**-kohdasta **Työntekijän itsepalvelun parametrit**.</span><span class="sxs-lookup"><span data-stu-id="74a48-132">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="74a48-133">Valitse **Joustoluottosuunnitelman ruudun asetukset** -välilehti ja valitse sitten **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="74a48-133">Select the **Flex credit plan tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="74a48-134">Määritä seuraavien kenttien arvot.</span><span class="sxs-lookup"><span data-stu-id="74a48-134">Specify values for the following fields:</span></span>

   | <span data-ttu-id="74a48-135">Kenttä</span><span class="sxs-lookup"><span data-stu-id="74a48-135">Field</span></span> | <span data-ttu-id="74a48-136">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="74a48-136">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="74a48-137">**Ruudun tunnus**</span><span class="sxs-lookup"><span data-stu-id="74a48-137">**Tile ID**</span></span> | <span data-ttu-id="74a48-138">Ruudun yksilöivä tunniste.</span><span class="sxs-lookup"><span data-stu-id="74a48-138">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="74a48-139">**Ruudun selitteen teksti**</span><span class="sxs-lookup"><span data-stu-id="74a48-139">**Tile label text**</span></span> | <span data-ttu-id="74a48-140">Teksti, joka tulee näkyviin itsepalvelun ruudussa.</span><span class="sxs-lookup"><span data-stu-id="74a48-140">The text that will appear for the tile on Self service.</span></span> |
   | <span data-ttu-id="74a48-141">**Kuvaus**</span><span class="sxs-lookup"><span data-stu-id="74a48-141">**Description**</span></span> | <span data-ttu-id="74a48-142">Ruudun kuvaus.</span><span class="sxs-lookup"><span data-stu-id="74a48-142">A description of the tile.</span></span> |
   | <span data-ttu-id="74a48-143">**Internet-osoite**</span><span class="sxs-lookup"><span data-stu-id="74a48-143">**Internet address**</span></span> | <span data-ttu-id="74a48-144">Kirjoita työntekijän itsepalvelusivun URL-osoite.</span><span class="sxs-lookup"><span data-stu-id="74a48-144">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="74a48-145">**Ruudun koko**</span><span class="sxs-lookup"><span data-stu-id="74a48-145">**Tile size**</span></span> | <span data-ttu-id="74a48-146">Ruudun koko: pieni, keskikokoinen tai suuri.</span><span class="sxs-lookup"><span data-stu-id="74a48-146">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="74a48-147">**Kohde**</span><span class="sxs-lookup"><span data-stu-id="74a48-147">**Target**</span></span> | <span data-ttu-id="74a48-148">Määrittää, avataanko sivu uudessa ikkunassa vai nykyisessä ikkunassa.</span><span class="sxs-lookup"><span data-stu-id="74a48-148">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="74a48-149">**Ruudun taustakuva**</span><span class="sxs-lookup"><span data-stu-id="74a48-149">**Tile background image**</span></span> | <span data-ttu-id="74a48-150">Ruudussa käytettävän kuvan URL-osoite (valinnainen).</span><span class="sxs-lookup"><span data-stu-id="74a48-150">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="74a48-151">**Alku**</span><span class="sxs-lookup"><span data-stu-id="74a48-151">**Start**</span></span> | <span data-ttu-id="74a48-152">Aloituspäivämäärä ja -kellonaika, jolloin laatta on käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="74a48-152">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="74a48-153">**End-näppäin**</span><span class="sxs-lookup"><span data-stu-id="74a48-153">**End**</span></span> | <span data-ttu-id="74a48-154">Lopetuspäivämäärä ja -kellonaika, jolloin laatta on käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="74a48-154">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="74a48-155">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="74a48-155">Select **Save**.</span></span>
