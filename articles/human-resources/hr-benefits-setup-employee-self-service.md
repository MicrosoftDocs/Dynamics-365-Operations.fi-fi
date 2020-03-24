---
title: Työntekijän itsepalvelun määrittäminen
description: Microsoft Dynamics 365 Human Resources -ohjelmassa voit määrittää ylimmän tason siirtymisruudut työntekijän itsepalvelussa.
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
ms.openlocfilehash: 17918fc7b894929c92c54b59b7440ab8aef980bd
ms.sourcegitcommit: f38302b9430f2ab3efe91d0a7beff946bc610e8f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/28/2020
ms.locfileid: "3092657"
---
# <a name="configure-employee-self-service"></a><span data-ttu-id="f916e-103">Työntekijän itsepalvelun määrittäminen</span><span class="sxs-lookup"><span data-stu-id="f916e-103">Configure employee self service</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="f916e-104">Microsoft Dynamics 365 Human Resources -ohjelmassa voit määrittää ylimmän tason siirtymisruudut työntekijän itsepalvelussa.</span><span class="sxs-lookup"><span data-stu-id="f916e-104">In Microsoft Dynamics 365 Human Resources, you can configure tiles for top-level navigation in Employee self service.</span></span> <span data-ttu-id="f916e-105">Etuussuunnitelmaruudut ohjaavat käyttäjät etuussuunnitelmiin, joihin he voivat ilmoittautua.</span><span class="sxs-lookup"><span data-stu-id="f916e-105">Benefit plan tiles direct users to benefit plans that they are eligible to enroll in.</span></span>

## <a name="set-up-a-role-center-tile"></a><span data-ttu-id="f916e-106">Roolikeskus-ruudun määrittäminen</span><span class="sxs-lookup"><span data-stu-id="f916e-106">Set up a role center tile</span></span>

1. <span data-ttu-id="f916e-107">Valitse **Etujen hallinta** -työtilassa **Asetukset**-kohdasta **Työntekijän itsepalvelun parametrit**.</span><span class="sxs-lookup"><span data-stu-id="f916e-107">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="f916e-108">Valitse **Roolikeskus-ruudun asetukset** -välilehti ja valitse sitten **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="f916e-108">Select the **Role center tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="f916e-109">Määritä seuraavien kenttien arvot.</span><span class="sxs-lookup"><span data-stu-id="f916e-109">Specify values for the following fields:</span></span>

   | <span data-ttu-id="f916e-110">Kenttä</span><span class="sxs-lookup"><span data-stu-id="f916e-110">Field</span></span> | <span data-ttu-id="f916e-111">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="f916e-111">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="f916e-112">Ruudun tunnus</span><span class="sxs-lookup"><span data-stu-id="f916e-112">Tile ID</span></span> | <span data-ttu-id="f916e-113">Ruudun yksilöivä tunniste.</span><span class="sxs-lookup"><span data-stu-id="f916e-113">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="f916e-114">Ruudun selitteen teksti</span><span class="sxs-lookup"><span data-stu-id="f916e-114">Tile label text</span></span> | <span data-ttu-id="f916e-115">Teksti, joka tulee näkyviin itsepalvelun ruudussa.</span><span class="sxs-lookup"><span data-stu-id="f916e-115">The text that will appear for the tile on Self-service.</span></span> |
   | <span data-ttu-id="f916e-116">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="f916e-116">Description</span></span> | <span data-ttu-id="f916e-117">Ruudun kuvaus.</span><span class="sxs-lookup"><span data-stu-id="f916e-117">A description of the tile.</span></span> |
   | <span data-ttu-id="f916e-118">Internet-osoite</span><span class="sxs-lookup"><span data-stu-id="f916e-118">Internet address</span></span> | <span data-ttu-id="f916e-119">Kirjoita työntekijän itsepalvelusivun URL-osoite.</span><span class="sxs-lookup"><span data-stu-id="f916e-119">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="f916e-120">Ruudun koko</span><span class="sxs-lookup"><span data-stu-id="f916e-120">Tile size</span></span> | <span data-ttu-id="f916e-121">Ruudun koko: pieni, keskikokoinen tai suuri.</span><span class="sxs-lookup"><span data-stu-id="f916e-121">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="f916e-122">Kohde</span><span class="sxs-lookup"><span data-stu-id="f916e-122">Target</span></span> | <span data-ttu-id="f916e-123">Määrittää, avataanko sivu uudessa ikkunassa vai nykyisessä ikkunassa.</span><span class="sxs-lookup"><span data-stu-id="f916e-123">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="f916e-124">Ruudun taustakuva</span><span class="sxs-lookup"><span data-stu-id="f916e-124">Tile background image</span></span> | <span data-ttu-id="f916e-125">Ruudussa käytettävän kuvan URL-osoite (valinnainen).</span><span class="sxs-lookup"><span data-stu-id="f916e-125">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="f916e-126">Alku</span><span class="sxs-lookup"><span data-stu-id="f916e-126">Start</span></span> | <span data-ttu-id="f916e-127">Aloituspäivämäärä ja -kellonaika, jolloin laatta on käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="f916e-127">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="f916e-128">End-näppäin</span><span class="sxs-lookup"><span data-stu-id="f916e-128">End</span></span> | <span data-ttu-id="f916e-129">Lopetuspäivämäärä ja -kellonaika, jolloin laatta on käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="f916e-129">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="f916e-130">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="f916e-130">Select **Save**.</span></span>

## <a name="set-up-a-benefit-plans-tile"></a><span data-ttu-id="f916e-131">Etuussuunnitelmien ruudun määrittäminen</span><span class="sxs-lookup"><span data-stu-id="f916e-131">Set up a benefit plans tile</span></span>

1. <span data-ttu-id="f916e-132">Valitse **Etujen hallinta** -työtilassa **Asetukset**-kohdasta **Työntekijän itsepalvelun parametrit**.</span><span class="sxs-lookup"><span data-stu-id="f916e-132">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="f916e-133">Valitse **Etuussuunnitelmien ruudun asetukset** -välilehti ja valitse sitten **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="f916e-133">Select the **Benefit plans tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="f916e-134">Määritä seuraavien kenttien arvot.</span><span class="sxs-lookup"><span data-stu-id="f916e-134">Specify values for the following fields:</span></span>

   | <span data-ttu-id="f916e-135">Kenttä</span><span class="sxs-lookup"><span data-stu-id="f916e-135">Field</span></span> | <span data-ttu-id="f916e-136">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="f916e-136">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="f916e-137">Ruudun tunnus</span><span class="sxs-lookup"><span data-stu-id="f916e-137">Tile ID</span></span> | <span data-ttu-id="f916e-138">Ruudun yksilöivä tunniste.</span><span class="sxs-lookup"><span data-stu-id="f916e-138">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="f916e-139">Ruudun selitteen teksti</span><span class="sxs-lookup"><span data-stu-id="f916e-139">Tile label text</span></span> | <span data-ttu-id="f916e-140">Teksti, joka tulee näkyviin itsepalvelun ruudussa.</span><span class="sxs-lookup"><span data-stu-id="f916e-140">The text that will appear for the tile on Self-service.</span></span> |
   | <span data-ttu-id="f916e-141">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="f916e-141">Description</span></span> | <span data-ttu-id="f916e-142">Ruudun kuvaus.</span><span class="sxs-lookup"><span data-stu-id="f916e-142">A description of the tile.</span></span> |
   | <span data-ttu-id="f916e-143">Internet-osoite</span><span class="sxs-lookup"><span data-stu-id="f916e-143">Internet address</span></span> | <span data-ttu-id="f916e-144">Kirjoita työntekijän itsepalvelusivun URL-osoite.</span><span class="sxs-lookup"><span data-stu-id="f916e-144">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="f916e-145">Ruudun koko</span><span class="sxs-lookup"><span data-stu-id="f916e-145">Tile size</span></span> | <span data-ttu-id="f916e-146">Ruudun koko: pieni, keskikokoinen tai suuri.</span><span class="sxs-lookup"><span data-stu-id="f916e-146">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="f916e-147">Kohde</span><span class="sxs-lookup"><span data-stu-id="f916e-147">Target</span></span> | <span data-ttu-id="f916e-148">Määrittää, avataanko sivu uudessa ikkunassa vai nykyisessä ikkunassa.</span><span class="sxs-lookup"><span data-stu-id="f916e-148">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="f916e-149">Ruudun taustakuva</span><span class="sxs-lookup"><span data-stu-id="f916e-149">Tile background image</span></span> | <span data-ttu-id="f916e-150">Ruudussa käytettävän kuvan URL-osoite (valinnainen).</span><span class="sxs-lookup"><span data-stu-id="f916e-150">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="f916e-151">Alku</span><span class="sxs-lookup"><span data-stu-id="f916e-151">Start</span></span> | <span data-ttu-id="f916e-152">Aloituspäivämäärä ja -kellonaika, jolloin laatta on käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="f916e-152">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="f916e-153">End-näppäin</span><span class="sxs-lookup"><span data-stu-id="f916e-153">End</span></span> | <span data-ttu-id="f916e-154">Lopetuspäivämäärä ja -kellonaika, jolloin laatta on käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="f916e-154">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="f916e-155">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="f916e-155">Select **Save**.</span></span>

## <a name="set-up-a-flex-credit-plan-tile"></a><span data-ttu-id="f916e-156">Joustoluottosuunnitelman ruudun määrittäminen</span><span class="sxs-lookup"><span data-stu-id="f916e-156">Set up a flex credit plan tile</span></span>

1. <span data-ttu-id="f916e-157">Valitse **Etujen hallinta** -työtilassa **Asetukset**-kohdasta **Työntekijän itsepalvelun parametrit**.</span><span class="sxs-lookup"><span data-stu-id="f916e-157">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="f916e-158">Valitse **Joustoluottosuunnitelman ruudun asetukset** -välilehti ja valitse sitten **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="f916e-158">Select the **Flex credit plan tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="f916e-159">Määritä seuraavien kenttien arvot.</span><span class="sxs-lookup"><span data-stu-id="f916e-159">Specify values for the following fields:</span></span>

   | <span data-ttu-id="f916e-160">Kenttä</span><span class="sxs-lookup"><span data-stu-id="f916e-160">Field</span></span> | <span data-ttu-id="f916e-161">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="f916e-161">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="f916e-162">Ruudun tunnus</span><span class="sxs-lookup"><span data-stu-id="f916e-162">Tile ID</span></span> | <span data-ttu-id="f916e-163">Ruudun yksilöivä tunniste.</span><span class="sxs-lookup"><span data-stu-id="f916e-163">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="f916e-164">Ruudun selitteen teksti</span><span class="sxs-lookup"><span data-stu-id="f916e-164">Tile label text</span></span> | <span data-ttu-id="f916e-165">Teksti, joka tulee näkyviin itsepalvelun ruudussa.</span><span class="sxs-lookup"><span data-stu-id="f916e-165">The text that will appear for the tile on Self-service.</span></span> |
   | <span data-ttu-id="f916e-166">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="f916e-166">Description</span></span> | <span data-ttu-id="f916e-167">Ruudun kuvaus.</span><span class="sxs-lookup"><span data-stu-id="f916e-167">A description of the tile.</span></span> |
   | <span data-ttu-id="f916e-168">Internet-osoite</span><span class="sxs-lookup"><span data-stu-id="f916e-168">Internet address</span></span> | <span data-ttu-id="f916e-169">Kirjoita työntekijän itsepalvelusivun URL-osoite.</span><span class="sxs-lookup"><span data-stu-id="f916e-169">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="f916e-170">Ruudun koko</span><span class="sxs-lookup"><span data-stu-id="f916e-170">Tile size</span></span> | <span data-ttu-id="f916e-171">Ruudun koko: pieni, keskikokoinen tai suuri.</span><span class="sxs-lookup"><span data-stu-id="f916e-171">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="f916e-172">Kohde</span><span class="sxs-lookup"><span data-stu-id="f916e-172">Target</span></span> | <span data-ttu-id="f916e-173">Määrittää, avataanko sivu uudessa ikkunassa vai nykyisessä ikkunassa.</span><span class="sxs-lookup"><span data-stu-id="f916e-173">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="f916e-174">Ruudun taustakuva</span><span class="sxs-lookup"><span data-stu-id="f916e-174">Tile background image</span></span> | <span data-ttu-id="f916e-175">Ruudussa käytettävän kuvan URL-osoite (valinnainen).</span><span class="sxs-lookup"><span data-stu-id="f916e-175">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="f916e-176">Alku</span><span class="sxs-lookup"><span data-stu-id="f916e-176">Start</span></span> | <span data-ttu-id="f916e-177">Aloituspäivämäärä ja -kellonaika, jolloin laatta on käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="f916e-177">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="f916e-178">End-näppäin</span><span class="sxs-lookup"><span data-stu-id="f916e-178">End</span></span> | <span data-ttu-id="f916e-179">Lopetuspäivämäärä ja -kellonaika, jolloin laatta on käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="f916e-179">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="f916e-180">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="f916e-180">Select **Save**.</span></span>
