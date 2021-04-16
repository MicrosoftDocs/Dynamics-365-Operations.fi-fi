---
title: Kielten lisääminen sivustoon
description: Tässä ohjeaiheessa kerrotaan, kuinka lisäkielten tuki lisätään Microsoft Dynamics 365 Commerce -sivustoon.
author: bicyclingfool
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: d74b24cc6363aa0a59f4f6c3365a8b37bbbe292b
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797620"
---
# <a name="add-languages-to-your-site"></a><span data-ttu-id="3e4c8-103">Kielten lisääminen sivustoon</span><span class="sxs-lookup"><span data-stu-id="3e4c8-103">Add languages to your site</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="3e4c8-104">Tässä ohjeaiheessa kerrotaan, kuinka lisäkielten tuki lisätään Microsoft Dynamics 365 Commerce -sivustoon.</span><span class="sxs-lookup"><span data-stu-id="3e4c8-104">This topic explains how to add support for additional languages to a Microsoft Dynamics 365 Commerce site.</span></span>

<span data-ttu-id="3e4c8-105">Voit lokalisoida sivuston millä tahansa kielellä, jota Commerce tukee.</span><span class="sxs-lookup"><span data-stu-id="3e4c8-105">You can localize your website into any language that Commerce supports.</span></span> <span data-ttu-id="3e4c8-106">(Tuettujen kielten luettelo tulee näkyviin myöhemmin tässä ohjeaiheessa.) Jos haluat lisätä kielen sivustoon, kieli on ensin lisättävä sivustoon sidottuun verkkokauppaan.</span><span class="sxs-lookup"><span data-stu-id="3e4c8-106">(The list of supported languages appears later in this topic.) To add a language on your website, you must first add it to an online store that is bound to your site.</span></span>

## <a name="add-a-language-to-an-online-store"></a><span data-ttu-id="3e4c8-107">Kielen lisääminen verkkokauppaan</span><span class="sxs-lookup"><span data-stu-id="3e4c8-107">Add a language to an online store</span></span>

<span data-ttu-id="3e4c8-108">Voit lisätä kielen verkkokauppaan seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="3e4c8-108">To add a language to an online store, follow these steps.</span></span>

1. <span data-ttu-id="3e4c8-109">Avaa sivuston Dynamics 365 Commerce -ympäristö.</span><span class="sxs-lookup"><span data-stu-id="3e4c8-109">Open the Dynamics 365 Commerce environment for your site.</span></span>
1. <span data-ttu-id="3e4c8-110">Siirry kohtaan **Retail ja Commerce \> Kanavat \> Verkkokaupat**. Näkyviin tulee ympäristöäsi varten määritettyjen verkkokauppojen luettelo.</span><span class="sxs-lookup"><span data-stu-id="3e4c8-110">Go to **Retail and Commerce \> Channels \> Online stores** to access the list of online stores that are configured for your environment.</span></span> <span data-ttu-id="3e4c8-111">Vaihtoehtoisesti voit kirjoittaa hakutermiksi **verkkokaupat**.</span><span class="sxs-lookup"><span data-stu-id="3e4c8-111">Alternatively, enter **online stores** as a search term.</span></span>
1. <span data-ttu-id="3e4c8-112">Valitse verkkokauppa, johon kieli lisätään.</span><span class="sxs-lookup"><span data-stu-id="3e4c8-112">Select the online store to add a language for.</span></span>
1. <span data-ttu-id="3e4c8-113">Valitse **Kielet**-pikavälilehdessä **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="3e4c8-113">On the **Languages** FastTab, select **Add**.</span></span>
1. <span data-ttu-id="3e4c8-114">Valitse lisättävä kieli **Kieli**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="3e4c8-114">In the **Language** field, select the language to add.</span></span>

<span data-ttu-id="3e4c8-115">Lisäämäsi kieli on nyt käytettävissä. Voit määrittää sivuston käyttämään sitä sivuston luontiympäristössä.</span><span class="sxs-lookup"><span data-stu-id="3e4c8-115">The language that you added will now be available so that you can configure your site to use it in the site authoring environment.</span></span>

### <a name="languages-that-are-supported-by-dynamics-365-commerce"></a><span data-ttu-id="3e4c8-116">Kielet, joita Dynamics 365 Commerce tukee</span><span class="sxs-lookup"><span data-stu-id="3e4c8-116">Languages that are supported by Dynamics 365 Commerce</span></span>

- <span data-ttu-id="3e4c8-117">af</span><span class="sxs-lookup"><span data-stu-id="3e4c8-117">af</span></span>
- <span data-ttu-id="3e4c8-118">ar</span><span class="sxs-lookup"><span data-stu-id="3e4c8-118">ar</span></span>
- <span data-ttu-id="3e4c8-119">ar-ae</span><span class="sxs-lookup"><span data-stu-id="3e4c8-119">ar-ae</span></span>
- <span data-ttu-id="3e4c8-120">ar-bh</span><span class="sxs-lookup"><span data-stu-id="3e4c8-120">ar-bh</span></span>
- <span data-ttu-id="3e4c8-121">ar-dz</span><span class="sxs-lookup"><span data-stu-id="3e4c8-121">ar-dz</span></span>
- <span data-ttu-id="3e4c8-122">ar-eg</span><span class="sxs-lookup"><span data-stu-id="3e4c8-122">ar-eg</span></span>
- <span data-ttu-id="3e4c8-123">ar-iq</span><span class="sxs-lookup"><span data-stu-id="3e4c8-123">ar-iq</span></span>
- <span data-ttu-id="3e4c8-124">ar-jo</span><span class="sxs-lookup"><span data-stu-id="3e4c8-124">ar-jo</span></span>
- <span data-ttu-id="3e4c8-125">ar-kw</span><span class="sxs-lookup"><span data-stu-id="3e4c8-125">ar-kw</span></span>
- <span data-ttu-id="3e4c8-126">ar-lb</span><span class="sxs-lookup"><span data-stu-id="3e4c8-126">ar-lb</span></span>
- <span data-ttu-id="3e4c8-127">ar-ly</span><span class="sxs-lookup"><span data-stu-id="3e4c8-127">ar-ly</span></span>
- <span data-ttu-id="3e4c8-128">ar-ma</span><span class="sxs-lookup"><span data-stu-id="3e4c8-128">ar-ma</span></span>
- <span data-ttu-id="3e4c8-129">ar-om</span><span class="sxs-lookup"><span data-stu-id="3e4c8-129">ar-om</span></span>
- <span data-ttu-id="3e4c8-130">ar-qa</span><span class="sxs-lookup"><span data-stu-id="3e4c8-130">ar-qa</span></span>
- <span data-ttu-id="3e4c8-131">ar-sa</span><span class="sxs-lookup"><span data-stu-id="3e4c8-131">ar-sa</span></span>
- <span data-ttu-id="3e4c8-132">ar-sy</span><span class="sxs-lookup"><span data-stu-id="3e4c8-132">ar-sy</span></span>
- <span data-ttu-id="3e4c8-133">ar-tn</span><span class="sxs-lookup"><span data-stu-id="3e4c8-133">ar-tn</span></span>
- <span data-ttu-id="3e4c8-134">ar-ye</span><span class="sxs-lookup"><span data-stu-id="3e4c8-134">ar-ye</span></span>
- <span data-ttu-id="3e4c8-135">be</span><span class="sxs-lookup"><span data-stu-id="3e4c8-135">be</span></span>
- <span data-ttu-id="3e4c8-136">bg</span><span class="sxs-lookup"><span data-stu-id="3e4c8-136">bg</span></span>
- <span data-ttu-id="3e4c8-137">ca</span><span class="sxs-lookup"><span data-stu-id="3e4c8-137">ca</span></span>
- <span data-ttu-id="3e4c8-138">cs</span><span class="sxs-lookup"><span data-stu-id="3e4c8-138">cs</span></span>
- <span data-ttu-id="3e4c8-139">da</span><span class="sxs-lookup"><span data-stu-id="3e4c8-139">da</span></span>
- <span data-ttu-id="3e4c8-140">de</span><span class="sxs-lookup"><span data-stu-id="3e4c8-140">de</span></span>
- <span data-ttu-id="3e4c8-141">de-at</span><span class="sxs-lookup"><span data-stu-id="3e4c8-141">de-at</span></span>
- <span data-ttu-id="3e4c8-142">de-ch</span><span class="sxs-lookup"><span data-stu-id="3e4c8-142">de-ch</span></span>
- <span data-ttu-id="3e4c8-143">de-li</span><span class="sxs-lookup"><span data-stu-id="3e4c8-143">de-li</span></span>
- <span data-ttu-id="3e4c8-144">de-lu</span><span class="sxs-lookup"><span data-stu-id="3e4c8-144">de-lu</span></span>
- <span data-ttu-id="3e4c8-145">el</span><span class="sxs-lookup"><span data-stu-id="3e4c8-145">el</span></span>
- <span data-ttu-id="3e4c8-146">en-029</span><span class="sxs-lookup"><span data-stu-id="3e4c8-146">en-029</span></span>
- <span data-ttu-id="3e4c8-147">en-au</span><span class="sxs-lookup"><span data-stu-id="3e4c8-147">en-au</span></span>
- <span data-ttu-id="3e4c8-148">en-bz</span><span class="sxs-lookup"><span data-stu-id="3e4c8-148">en-bz</span></span>
- <span data-ttu-id="3e4c8-149">en-ca</span><span class="sxs-lookup"><span data-stu-id="3e4c8-149">en-ca</span></span>
- <span data-ttu-id="3e4c8-150">en-gb</span><span class="sxs-lookup"><span data-stu-id="3e4c8-150">en-gb</span></span>
- <span data-ttu-id="3e4c8-151">en-ie</span><span class="sxs-lookup"><span data-stu-id="3e4c8-151">en-ie</span></span>
- <span data-ttu-id="3e4c8-152">en-in</span><span class="sxs-lookup"><span data-stu-id="3e4c8-152">en-in</span></span>
- <span data-ttu-id="3e4c8-153">en-jm</span><span class="sxs-lookup"><span data-stu-id="3e4c8-153">en-jm</span></span>
- <span data-ttu-id="3e4c8-154">en-my</span><span class="sxs-lookup"><span data-stu-id="3e4c8-154">en-my</span></span>
- <span data-ttu-id="3e4c8-155">en-nz</span><span class="sxs-lookup"><span data-stu-id="3e4c8-155">en-nz</span></span>
- <span data-ttu-id="3e4c8-156">en-sg</span><span class="sxs-lookup"><span data-stu-id="3e4c8-156">en-sg</span></span>
- <span data-ttu-id="3e4c8-157">en-tt</span><span class="sxs-lookup"><span data-stu-id="3e4c8-157">en-tt</span></span>
- <span data-ttu-id="3e4c8-158">fi-fi</span><span class="sxs-lookup"><span data-stu-id="3e4c8-158">en-us</span></span>
- <span data-ttu-id="3e4c8-159">en-za</span><span class="sxs-lookup"><span data-stu-id="3e4c8-159">en-za</span></span>
- <span data-ttu-id="3e4c8-160">es</span><span class="sxs-lookup"><span data-stu-id="3e4c8-160">es</span></span>
- <span data-ttu-id="3e4c8-161">es-ar</span><span class="sxs-lookup"><span data-stu-id="3e4c8-161">es-ar</span></span>
- <span data-ttu-id="3e4c8-162">es-bo</span><span class="sxs-lookup"><span data-stu-id="3e4c8-162">es-bo</span></span>
- <span data-ttu-id="3e4c8-163">es-cl</span><span class="sxs-lookup"><span data-stu-id="3e4c8-163">es-cl</span></span>
- <span data-ttu-id="3e4c8-164">es-co</span><span class="sxs-lookup"><span data-stu-id="3e4c8-164">es-co</span></span>
- <span data-ttu-id="3e4c8-165">es-cr</span><span class="sxs-lookup"><span data-stu-id="3e4c8-165">es-cr</span></span>
- <span data-ttu-id="3e4c8-166">es-do</span><span class="sxs-lookup"><span data-stu-id="3e4c8-166">es-do</span></span>
- <span data-ttu-id="3e4c8-167">es-ec</span><span class="sxs-lookup"><span data-stu-id="3e4c8-167">es-ec</span></span>
- <span data-ttu-id="3e4c8-168">es-gt</span><span class="sxs-lookup"><span data-stu-id="3e4c8-168">es-gt</span></span>
- <span data-ttu-id="3e4c8-169">es-hn</span><span class="sxs-lookup"><span data-stu-id="3e4c8-169">es-hn</span></span>
- <span data-ttu-id="3e4c8-170">es-mx</span><span class="sxs-lookup"><span data-stu-id="3e4c8-170">es-mx</span></span>
- <span data-ttu-id="3e4c8-171">es-ni</span><span class="sxs-lookup"><span data-stu-id="3e4c8-171">es-ni</span></span>
- <span data-ttu-id="3e4c8-172">es-pa</span><span class="sxs-lookup"><span data-stu-id="3e4c8-172">es-pa</span></span>
- <span data-ttu-id="3e4c8-173">es-pe</span><span class="sxs-lookup"><span data-stu-id="3e4c8-173">es-pe</span></span>
- <span data-ttu-id="3e4c8-174">es-pr</span><span class="sxs-lookup"><span data-stu-id="3e4c8-174">es-pr</span></span>
- <span data-ttu-id="3e4c8-175">es-py</span><span class="sxs-lookup"><span data-stu-id="3e4c8-175">es-py</span></span>
- <span data-ttu-id="3e4c8-176">es-sv</span><span class="sxs-lookup"><span data-stu-id="3e4c8-176">es-sv</span></span>
- <span data-ttu-id="3e4c8-177">es-tr</span><span class="sxs-lookup"><span data-stu-id="3e4c8-177">es-tr</span></span>
- <span data-ttu-id="3e4c8-178">es-uy</span><span class="sxs-lookup"><span data-stu-id="3e4c8-178">es-uy</span></span>
- <span data-ttu-id="3e4c8-179">es-ve</span><span class="sxs-lookup"><span data-stu-id="3e4c8-179">es-ve</span></span>
- <span data-ttu-id="3e4c8-180">et</span><span class="sxs-lookup"><span data-stu-id="3e4c8-180">et</span></span>
- <span data-ttu-id="3e4c8-181">eu</span><span class="sxs-lookup"><span data-stu-id="3e4c8-181">eu</span></span>
- <span data-ttu-id="3e4c8-182">fa</span><span class="sxs-lookup"><span data-stu-id="3e4c8-182">fa</span></span>
- <span data-ttu-id="3e4c8-183">fi</span><span class="sxs-lookup"><span data-stu-id="3e4c8-183">fi</span></span>
- <span data-ttu-id="3e4c8-184">fo</span><span class="sxs-lookup"><span data-stu-id="3e4c8-184">fo</span></span>
- <span data-ttu-id="3e4c8-185">fr</span><span class="sxs-lookup"><span data-stu-id="3e4c8-185">fr</span></span>
- <span data-ttu-id="3e4c8-186">fr-be</span><span class="sxs-lookup"><span data-stu-id="3e4c8-186">fr-be</span></span>
- <span data-ttu-id="3e4c8-187">fr-ca</span><span class="sxs-lookup"><span data-stu-id="3e4c8-187">fr-ca</span></span>
- <span data-ttu-id="3e4c8-188">fr-ch</span><span class="sxs-lookup"><span data-stu-id="3e4c8-188">fr-ch</span></span>
- <span data-ttu-id="3e4c8-189">fr-lu</span><span class="sxs-lookup"><span data-stu-id="3e4c8-189">fr-lu</span></span>
- <span data-ttu-id="3e4c8-190">hi</span><span class="sxs-lookup"><span data-stu-id="3e4c8-190">hi</span></span>
- <span data-ttu-id="3e4c8-191">h</span><span class="sxs-lookup"><span data-stu-id="3e4c8-191">hr</span></span>
- <span data-ttu-id="3e4c8-192">hu</span><span class="sxs-lookup"><span data-stu-id="3e4c8-192">hu</span></span>
- <span data-ttu-id="3e4c8-193">on</span><span class="sxs-lookup"><span data-stu-id="3e4c8-193">is</span></span>
- <span data-ttu-id="3e4c8-194">it</span><span class="sxs-lookup"><span data-stu-id="3e4c8-194">it</span></span>
- <span data-ttu-id="3e4c8-195">it-ch</span><span class="sxs-lookup"><span data-stu-id="3e4c8-195">it-ch</span></span>
- <span data-ttu-id="3e4c8-196">ja</span><span class="sxs-lookup"><span data-stu-id="3e4c8-196">ja</span></span>
- <span data-ttu-id="3e4c8-197">lt</span><span class="sxs-lookup"><span data-stu-id="3e4c8-197">lt</span></span>
- <span data-ttu-id="3e4c8-198">lv</span><span class="sxs-lookup"><span data-stu-id="3e4c8-198">lv</span></span>
- <span data-ttu-id="3e4c8-199">mk</span><span class="sxs-lookup"><span data-stu-id="3e4c8-199">mk</span></span>
- <span data-ttu-id="3e4c8-200">ms</span><span class="sxs-lookup"><span data-stu-id="3e4c8-200">ms</span></span>
- <span data-ttu-id="3e4c8-201">mt</span><span class="sxs-lookup"><span data-stu-id="3e4c8-201">mt</span></span>
- <span data-ttu-id="3e4c8-202">nb-no</span><span class="sxs-lookup"><span data-stu-id="3e4c8-202">nb-no</span></span>
- <span data-ttu-id="3e4c8-203">nl</span><span class="sxs-lookup"><span data-stu-id="3e4c8-203">nl</span></span>
- <span data-ttu-id="3e4c8-204">nl-be</span><span class="sxs-lookup"><span data-stu-id="3e4c8-204">nl-be</span></span>
- <span data-ttu-id="3e4c8-205">nn-no</span><span class="sxs-lookup"><span data-stu-id="3e4c8-205">nn-no</span></span>
- <span data-ttu-id="3e4c8-206">pl</span><span class="sxs-lookup"><span data-stu-id="3e4c8-206">pl</span></span>
- <span data-ttu-id="3e4c8-207">pt-br</span><span class="sxs-lookup"><span data-stu-id="3e4c8-207">pt-br</span></span>
- <span data-ttu-id="3e4c8-208">ro</span><span class="sxs-lookup"><span data-stu-id="3e4c8-208">ro</span></span>
- <span data-ttu-id="3e4c8-209">ru</span><span class="sxs-lookup"><span data-stu-id="3e4c8-209">ru</span></span>
- <span data-ttu-id="3e4c8-210">ru-ru</span><span class="sxs-lookup"><span data-stu-id="3e4c8-210">ru-ru</span></span>
- <span data-ttu-id="3e4c8-211">sk</span><span class="sxs-lookup"><span data-stu-id="3e4c8-211">sk</span></span>
- <span data-ttu-id="3e4c8-212">sl</span><span class="sxs-lookup"><span data-stu-id="3e4c8-212">sl</span></span>
- <span data-ttu-id="3e4c8-213">sq</span><span class="sxs-lookup"><span data-stu-id="3e4c8-213">sq</span></span>
- <span data-ttu-id="3e4c8-214">sr</span><span class="sxs-lookup"><span data-stu-id="3e4c8-214">sr</span></span>
- <span data-ttu-id="3e4c8-215">sr-la</span><span class="sxs-lookup"><span data-stu-id="3e4c8-215">sr-la</span></span>
- <span data-ttu-id="3e4c8-216">sv</span><span class="sxs-lookup"><span data-stu-id="3e4c8-216">sv</span></span>
- <span data-ttu-id="3e4c8-217">sv-fi</span><span class="sxs-lookup"><span data-stu-id="3e4c8-217">sv-fi</span></span>
- <span data-ttu-id="3e4c8-218">th</span><span class="sxs-lookup"><span data-stu-id="3e4c8-218">th</span></span>
- <span data-ttu-id="3e4c8-219">tn</span><span class="sxs-lookup"><span data-stu-id="3e4c8-219">tn</span></span>
- <span data-ttu-id="3e4c8-220">tr</span><span class="sxs-lookup"><span data-stu-id="3e4c8-220">tr</span></span>
- <span data-ttu-id="3e4c8-221">uk</span><span class="sxs-lookup"><span data-stu-id="3e4c8-221">uk</span></span>
- <span data-ttu-id="3e4c8-222">ur</span><span class="sxs-lookup"><span data-stu-id="3e4c8-222">ur</span></span>
- <span data-ttu-id="3e4c8-223">xh</span><span class="sxs-lookup"><span data-stu-id="3e4c8-223">xh</span></span>
- <span data-ttu-id="3e4c8-224">zh-hans</span><span class="sxs-lookup"><span data-stu-id="3e4c8-224">zh-hans</span></span>
- <span data-ttu-id="3e4c8-225">zh-hk</span><span class="sxs-lookup"><span data-stu-id="3e4c8-225">zh-hk</span></span>
- <span data-ttu-id="3e4c8-226">zh-sg</span><span class="sxs-lookup"><span data-stu-id="3e4c8-226">zh-sg</span></span>
- <span data-ttu-id="3e4c8-227">zu</span><span class="sxs-lookup"><span data-stu-id="3e4c8-227">zu</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3e4c8-228">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="3e4c8-228">Additional resources</span></span>

[<span data-ttu-id="3e4c8-229">Logon lisääminen</span><span class="sxs-lookup"><span data-stu-id="3e4c8-229">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="3e4c8-230">Sivuston teeman valitseminen</span><span class="sxs-lookup"><span data-stu-id="3e4c8-230">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="3e4c8-231">CSS-ohitustiedostojen parissa työskentely</span><span class="sxs-lookup"><span data-stu-id="3e4c8-231">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="3e4c8-232">Favicon-kuvakkeen lisääminen</span><span class="sxs-lookup"><span data-stu-id="3e4c8-232">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="3e4c8-233">Tervetuloviestin lisääminen</span><span class="sxs-lookup"><span data-stu-id="3e4c8-233">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="3e4c8-234">Copyright-ilmoituksen lisääminen</span><span class="sxs-lookup"><span data-stu-id="3e4c8-234">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="3e4c8-235">Komentosarjakoodin lisääminen sivuston sivuihin telemetrian tukemiseksi</span><span class="sxs-lookup"><span data-stu-id="3e4c8-235">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
