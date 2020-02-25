---
title: Määritä työntekijän itsepalvelu
description: ''
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e44a35071b8d0987e6c949fb11312204317b44a1
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008893"
---
# <a name="configure-employee-self-service"></a><span data-ttu-id="fb0d3-102">Määritä työntekijän itsepalvelu</span><span class="sxs-lookup"><span data-stu-id="fb0d3-102">Configure employee self service</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="fb0d3-103">Microsoft Dynamics 365 Human Resources -ohjelmassa voit määrittää ylimmän tason siirtymisruudut työntekijän itsepalvelussa.</span><span class="sxs-lookup"><span data-stu-id="fb0d3-103">In Microsoft Dynamics 365 Human Resources, you can configure tiles for top-level navigation in Employee self service.</span></span> <span data-ttu-id="fb0d3-104">Etuussuunnitelmaruudut ohjaavat käyttäjät etuussuunnitelmiin, joihin he voivat ilmoittautua.</span><span class="sxs-lookup"><span data-stu-id="fb0d3-104">Benefit plan tiles direct users to benefit plans that they are eligible to enroll in.</span></span>

## <a name="set-up-a-role-center-tile"></a><span data-ttu-id="fb0d3-105">Roolikeskus-ruudun määrittäminen</span><span class="sxs-lookup"><span data-stu-id="fb0d3-105">Set up a role center tile</span></span>

1. <span data-ttu-id="fb0d3-106">Valitse **Etujen hallinta** -työtilassa **Asetukset**-kohdasta **Työntekijän itsepalvelun parametrit**.</span><span class="sxs-lookup"><span data-stu-id="fb0d3-106">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="fb0d3-107">Valitse **Roolikeskus-ruudun asetukset** -välilehti ja valitse sitten **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="fb0d3-107">Select the **Role center tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="fb0d3-108">Määritä seuraavien kenttien arvot.</span><span class="sxs-lookup"><span data-stu-id="fb0d3-108">Specify values for the following fields:</span></span>

   | <span data-ttu-id="fb0d3-109">Kenttä</span><span class="sxs-lookup"><span data-stu-id="fb0d3-109">Field</span></span> | <span data-ttu-id="fb0d3-110">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="fb0d3-110">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="fb0d3-111">Ruudun tunnus</span><span class="sxs-lookup"><span data-stu-id="fb0d3-111">Tile ID</span></span> | <span data-ttu-id="fb0d3-112">Ruudun yksilöivä tunniste.</span><span class="sxs-lookup"><span data-stu-id="fb0d3-112">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="fb0d3-113">Ruudun selitteen teksti</span><span class="sxs-lookup"><span data-stu-id="fb0d3-113">Tile label text</span></span> | <span data-ttu-id="fb0d3-114">Teksti, joka tulee näkyviin itsepalvelun ruudussa.</span><span class="sxs-lookup"><span data-stu-id="fb0d3-114">The text that will appear for the tile on Self-service.</span></span> |
   | <span data-ttu-id="fb0d3-115">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="fb0d3-115">Description</span></span> | <span data-ttu-id="fb0d3-116">Ruudun kuvaus.</span><span class="sxs-lookup"><span data-stu-id="fb0d3-116">A description of the tile.</span></span> |
   | <span data-ttu-id="fb0d3-117">Internet-osoite</span><span class="sxs-lookup"><span data-stu-id="fb0d3-117">Internet address</span></span> | <span data-ttu-id="fb0d3-118">Kirjoita työntekijän itsepalvelusivun URL-osoite.</span><span class="sxs-lookup"><span data-stu-id="fb0d3-118">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="fb0d3-119">Ruudun koko</span><span class="sxs-lookup"><span data-stu-id="fb0d3-119">Tile size</span></span> | <span data-ttu-id="fb0d3-120">Ruudun koko: pieni, keskikokoinen tai suuri.</span><span class="sxs-lookup"><span data-stu-id="fb0d3-120">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="fb0d3-121">Kohde</span><span class="sxs-lookup"><span data-stu-id="fb0d3-121">Target</span></span> | <span data-ttu-id="fb0d3-122">Määrittää, avataanko sivu uudessa ikkunassa vai nykyisessä ikkunassa.</span><span class="sxs-lookup"><span data-stu-id="fb0d3-122">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="fb0d3-123">Ruudun taustakuva</span><span class="sxs-lookup"><span data-stu-id="fb0d3-123">Tile background image</span></span> | <span data-ttu-id="fb0d3-124">Ruudussa käytettävän kuvan URL-osoite (valinnainen).</span><span class="sxs-lookup"><span data-stu-id="fb0d3-124">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="fb0d3-125">Alku</span><span class="sxs-lookup"><span data-stu-id="fb0d3-125">Start</span></span> | <span data-ttu-id="fb0d3-126">Aloituspäivämäärä ja -kellonaika, jolloin laatta on käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="fb0d3-126">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="fb0d3-127">End-näppäin</span><span class="sxs-lookup"><span data-stu-id="fb0d3-127">End</span></span> | <span data-ttu-id="fb0d3-128">Lopetuspäivämäärä ja -kellonaika, jolloin laatta on käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="fb0d3-128">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="fb0d3-129">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="fb0d3-129">Select **Save**.</span></span>

## <a name="set-up-a-benefit-plans-tile"></a><span data-ttu-id="fb0d3-130">Etuussuunnitelmien ruudun määrittäminen</span><span class="sxs-lookup"><span data-stu-id="fb0d3-130">Set up a benefit plans tile</span></span>

1. <span data-ttu-id="fb0d3-131">Valitse **Etujen hallinta** -työtilassa **Asetukset**-kohdasta **Työntekijän itsepalvelun parametrit**.</span><span class="sxs-lookup"><span data-stu-id="fb0d3-131">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="fb0d3-132">Valitse **Etuussuunnitelmien ruudun asetukset** -välilehti ja valitse sitten **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="fb0d3-132">Select the **Benefit plans tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="fb0d3-133">Määritä seuraavien kenttien arvot.</span><span class="sxs-lookup"><span data-stu-id="fb0d3-133">Specify values for the following fields:</span></span>

   | <span data-ttu-id="fb0d3-134">Kenttä</span><span class="sxs-lookup"><span data-stu-id="fb0d3-134">Field</span></span> | <span data-ttu-id="fb0d3-135">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="fb0d3-135">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="fb0d3-136">Ruudun tunnus</span><span class="sxs-lookup"><span data-stu-id="fb0d3-136">Tile ID</span></span> | <span data-ttu-id="fb0d3-137">Ruudun yksilöivä tunniste.</span><span class="sxs-lookup"><span data-stu-id="fb0d3-137">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="fb0d3-138">Ruudun selitteen teksti</span><span class="sxs-lookup"><span data-stu-id="fb0d3-138">Tile label text</span></span> | <span data-ttu-id="fb0d3-139">Teksti, joka tulee näkyviin itsepalvelun ruudussa.</span><span class="sxs-lookup"><span data-stu-id="fb0d3-139">The text that will appear for the tile on Self-service.</span></span> |
   | <span data-ttu-id="fb0d3-140">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="fb0d3-140">Description</span></span> | <span data-ttu-id="fb0d3-141">Ruudun kuvaus.</span><span class="sxs-lookup"><span data-stu-id="fb0d3-141">A description of the tile.</span></span> |
   | <span data-ttu-id="fb0d3-142">Internet-osoite</span><span class="sxs-lookup"><span data-stu-id="fb0d3-142">Internet address</span></span> | <span data-ttu-id="fb0d3-143">Kirjoita työntekijän itsepalvelusivun URL-osoite.</span><span class="sxs-lookup"><span data-stu-id="fb0d3-143">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="fb0d3-144">Ruudun koko</span><span class="sxs-lookup"><span data-stu-id="fb0d3-144">Tile size</span></span> | <span data-ttu-id="fb0d3-145">Ruudun koko: pieni, keskikokoinen tai suuri.</span><span class="sxs-lookup"><span data-stu-id="fb0d3-145">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="fb0d3-146">Kohde</span><span class="sxs-lookup"><span data-stu-id="fb0d3-146">Target</span></span> | <span data-ttu-id="fb0d3-147">Määrittää, avataanko sivu uudessa ikkunassa vai nykyisessä ikkunassa.</span><span class="sxs-lookup"><span data-stu-id="fb0d3-147">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="fb0d3-148">Ruudun taustakuva</span><span class="sxs-lookup"><span data-stu-id="fb0d3-148">Tile background image</span></span> | <span data-ttu-id="fb0d3-149">Ruudussa käytettävän kuvan URL-osoite (valinnainen).</span><span class="sxs-lookup"><span data-stu-id="fb0d3-149">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="fb0d3-150">Alku</span><span class="sxs-lookup"><span data-stu-id="fb0d3-150">Start</span></span> | <span data-ttu-id="fb0d3-151">Aloituspäivämäärä ja -kellonaika, jolloin laatta on käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="fb0d3-151">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="fb0d3-152">End-näppäin</span><span class="sxs-lookup"><span data-stu-id="fb0d3-152">End</span></span> | <span data-ttu-id="fb0d3-153">Lopetuspäivämäärä ja -kellonaika, jolloin laatta on käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="fb0d3-153">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="fb0d3-154">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="fb0d3-154">Select **Save**.</span></span>

## <a name="set-up-a-flex-credit-plan-tile"></a><span data-ttu-id="fb0d3-155">Joustoluottosuunnitelman ruudun määrittäminen</span><span class="sxs-lookup"><span data-stu-id="fb0d3-155">Set up a flex credit plan tile</span></span>

1. <span data-ttu-id="fb0d3-156">Valitse **Etujen hallinta** -työtilassa **Asetukset**-kohdasta **Työntekijän itsepalvelun parametrit**.</span><span class="sxs-lookup"><span data-stu-id="fb0d3-156">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="fb0d3-157">Valitse **Joustoluottosuunnitelman ruudun asetukset** -välilehti ja valitse sitten **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="fb0d3-157">Select the **Flex credit plan tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="fb0d3-158">Määritä seuraavien kenttien arvot.</span><span class="sxs-lookup"><span data-stu-id="fb0d3-158">Specify values for the following fields:</span></span>

   | <span data-ttu-id="fb0d3-159">Kenttä</span><span class="sxs-lookup"><span data-stu-id="fb0d3-159">Field</span></span> | <span data-ttu-id="fb0d3-160">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="fb0d3-160">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="fb0d3-161">Ruudun tunnus</span><span class="sxs-lookup"><span data-stu-id="fb0d3-161">Tile ID</span></span> | <span data-ttu-id="fb0d3-162">Ruudun yksilöivä tunniste.</span><span class="sxs-lookup"><span data-stu-id="fb0d3-162">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="fb0d3-163">Ruudun selitteen teksti</span><span class="sxs-lookup"><span data-stu-id="fb0d3-163">Tile label text</span></span> | <span data-ttu-id="fb0d3-164">Teksti, joka tulee näkyviin itsepalvelun ruudussa.</span><span class="sxs-lookup"><span data-stu-id="fb0d3-164">The text that will appear for the tile on Self-service.</span></span> |
   | <span data-ttu-id="fb0d3-165">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="fb0d3-165">Description</span></span> | <span data-ttu-id="fb0d3-166">Ruudun kuvaus.</span><span class="sxs-lookup"><span data-stu-id="fb0d3-166">A description of the tile.</span></span> |
   | <span data-ttu-id="fb0d3-167">Internet-osoite</span><span class="sxs-lookup"><span data-stu-id="fb0d3-167">Internet address</span></span> | <span data-ttu-id="fb0d3-168">Kirjoita työntekijän itsepalvelusivun URL-osoite.</span><span class="sxs-lookup"><span data-stu-id="fb0d3-168">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="fb0d3-169">Ruudun koko</span><span class="sxs-lookup"><span data-stu-id="fb0d3-169">Tile size</span></span> | <span data-ttu-id="fb0d3-170">Ruudun koko: pieni, keskikokoinen tai suuri.</span><span class="sxs-lookup"><span data-stu-id="fb0d3-170">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="fb0d3-171">Kohde</span><span class="sxs-lookup"><span data-stu-id="fb0d3-171">Target</span></span> | <span data-ttu-id="fb0d3-172">Määrittää, avataanko sivu uudessa ikkunassa vai nykyisessä ikkunassa.</span><span class="sxs-lookup"><span data-stu-id="fb0d3-172">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="fb0d3-173">Ruudun taustakuva</span><span class="sxs-lookup"><span data-stu-id="fb0d3-173">Tile background image</span></span> | <span data-ttu-id="fb0d3-174">Ruudussa käytettävän kuvan URL-osoite (valinnainen).</span><span class="sxs-lookup"><span data-stu-id="fb0d3-174">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="fb0d3-175">Alku</span><span class="sxs-lookup"><span data-stu-id="fb0d3-175">Start</span></span> | <span data-ttu-id="fb0d3-176">Aloituspäivämäärä ja -kellonaika, jolloin laatta on käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="fb0d3-176">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="fb0d3-177">End-näppäin</span><span class="sxs-lookup"><span data-stu-id="fb0d3-177">End</span></span> | <span data-ttu-id="fb0d3-178">Lopetuspäivämäärä ja -kellonaika, jolloin laatta on käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="fb0d3-178">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="fb0d3-179">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="fb0d3-179">Select **Save**.</span></span>
