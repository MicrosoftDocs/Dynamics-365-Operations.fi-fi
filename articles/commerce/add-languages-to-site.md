---
title: Kielten lisääminen sivustoon
description: Tässä ohjeaiheessa kerrotaan, kuinka lisäkielten tuki lisätään Microsoft Dynamics 365 Commerce -sivustoon.
author: bicyclingfool
manager: annbe
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: fa3029387d5f1ca605fc9559c4272c8dfebcddaf
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4411910"
---
# <a name="add-languages-to-your-site"></a><span data-ttu-id="5fcb1-103">Kielten lisääminen sivustoon</span><span class="sxs-lookup"><span data-stu-id="5fcb1-103">Add languages to your site</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="5fcb1-104">Tässä ohjeaiheessa kerrotaan, kuinka lisäkielten tuki lisätään Microsoft Dynamics 365 Commerce -sivustoon.</span><span class="sxs-lookup"><span data-stu-id="5fcb1-104">This topic explains how to add support for additional languages to a Microsoft Dynamics 365 Commerce site.</span></span>

## <a name="overview"></a><span data-ttu-id="5fcb1-105">Yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="5fcb1-105">Overview</span></span>

<span data-ttu-id="5fcb1-106">Voit lokalisoida sivuston millä tahansa kielellä, jota Commerce tukee.</span><span class="sxs-lookup"><span data-stu-id="5fcb1-106">You can localize your website into any language that Commerce supports.</span></span> <span data-ttu-id="5fcb1-107">(Tuettujen kielten luettelo tulee näkyviin myöhemmin tässä ohjeaiheessa.) Jos haluat lisätä kielen sivustoon, kieli on ensin lisättävä sivustoon sidottuun verkkokauppaan.</span><span class="sxs-lookup"><span data-stu-id="5fcb1-107">(The list of supported languages appears later in this topic.) To add a language on your website, you must first add it to an online store that is bound to your site.</span></span>

## <a name="add-a-language-to-an-online-store"></a><span data-ttu-id="5fcb1-108">Kielen lisääminen verkkokauppaan</span><span class="sxs-lookup"><span data-stu-id="5fcb1-108">Add a language to an online store</span></span>

<span data-ttu-id="5fcb1-109">Voit lisätä kielen verkkokauppaan seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="5fcb1-109">To add a language to an online store, follow these steps.</span></span>

1. <span data-ttu-id="5fcb1-110">Avaa sivuston Dynamics 365 Commerce -ympäristö.</span><span class="sxs-lookup"><span data-stu-id="5fcb1-110">Open the Dynamics 365 Commerce environment for your site.</span></span>
1. <span data-ttu-id="5fcb1-111">Siirry kohtaan **Retail ja Commerce \> Kanavat \> Verkkokaupat**. Näkyviin tulee ympäristöäsi varten määritettyjen verkkokauppojen luettelo.</span><span class="sxs-lookup"><span data-stu-id="5fcb1-111">Go to **Retail and Commerce \> Channels \> Online stores** to access the list of online stores that are configured for your environment.</span></span> <span data-ttu-id="5fcb1-112">Vaihtoehtoisesti voit kirjoittaa hakutermiksi **verkkokaupat**.</span><span class="sxs-lookup"><span data-stu-id="5fcb1-112">Alternatively, enter **online stores** as a search term.</span></span>
1. <span data-ttu-id="5fcb1-113">Valitse verkkokauppa, johon kieli lisätään.</span><span class="sxs-lookup"><span data-stu-id="5fcb1-113">Select the online store to add a language for.</span></span>
1. <span data-ttu-id="5fcb1-114">Valitse **Kielet**-pikavälilehdessä **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="5fcb1-114">On the **Languages** FastTab, select **Add**.</span></span>
1. <span data-ttu-id="5fcb1-115">Valitse lisättävä kieli **Kieli**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="5fcb1-115">In the **Language** field, select the language to add.</span></span>

<span data-ttu-id="5fcb1-116">Lisäämäsi kieli on nyt käytettävissä. Voit määrittää sivuston käyttämään sitä sivuston luontiympäristössä.</span><span class="sxs-lookup"><span data-stu-id="5fcb1-116">The language that you added will now be available so that you can configure your site to use it in the site authoring environment.</span></span>

### <a name="languages-that-are-supported-by-dynamics-365-commerce"></a><span data-ttu-id="5fcb1-117">Kielet, joita Dynamics 365 Commerce tukee</span><span class="sxs-lookup"><span data-stu-id="5fcb1-117">Languages that are supported by Dynamics 365 Commerce</span></span>

- <span data-ttu-id="5fcb1-118">af</span><span class="sxs-lookup"><span data-stu-id="5fcb1-118">af</span></span>
- <span data-ttu-id="5fcb1-119">ar</span><span class="sxs-lookup"><span data-stu-id="5fcb1-119">ar</span></span>
- <span data-ttu-id="5fcb1-120">ar-ae</span><span class="sxs-lookup"><span data-stu-id="5fcb1-120">ar-ae</span></span>
- <span data-ttu-id="5fcb1-121">ar-bh</span><span class="sxs-lookup"><span data-stu-id="5fcb1-121">ar-bh</span></span>
- <span data-ttu-id="5fcb1-122">ar-dz</span><span class="sxs-lookup"><span data-stu-id="5fcb1-122">ar-dz</span></span>
- <span data-ttu-id="5fcb1-123">ar-eg</span><span class="sxs-lookup"><span data-stu-id="5fcb1-123">ar-eg</span></span>
- <span data-ttu-id="5fcb1-124">ar-iq</span><span class="sxs-lookup"><span data-stu-id="5fcb1-124">ar-iq</span></span>
- <span data-ttu-id="5fcb1-125">ar-jo</span><span class="sxs-lookup"><span data-stu-id="5fcb1-125">ar-jo</span></span>
- <span data-ttu-id="5fcb1-126">ar-kw</span><span class="sxs-lookup"><span data-stu-id="5fcb1-126">ar-kw</span></span>
- <span data-ttu-id="5fcb1-127">ar-lb</span><span class="sxs-lookup"><span data-stu-id="5fcb1-127">ar-lb</span></span>
- <span data-ttu-id="5fcb1-128">ar-ly</span><span class="sxs-lookup"><span data-stu-id="5fcb1-128">ar-ly</span></span>
- <span data-ttu-id="5fcb1-129">ar-ma</span><span class="sxs-lookup"><span data-stu-id="5fcb1-129">ar-ma</span></span>
- <span data-ttu-id="5fcb1-130">ar-om</span><span class="sxs-lookup"><span data-stu-id="5fcb1-130">ar-om</span></span>
- <span data-ttu-id="5fcb1-131">ar-qa</span><span class="sxs-lookup"><span data-stu-id="5fcb1-131">ar-qa</span></span>
- <span data-ttu-id="5fcb1-132">ar-sa</span><span class="sxs-lookup"><span data-stu-id="5fcb1-132">ar-sa</span></span>
- <span data-ttu-id="5fcb1-133">ar-sy</span><span class="sxs-lookup"><span data-stu-id="5fcb1-133">ar-sy</span></span>
- <span data-ttu-id="5fcb1-134">ar-tn</span><span class="sxs-lookup"><span data-stu-id="5fcb1-134">ar-tn</span></span>
- <span data-ttu-id="5fcb1-135">ar-ye</span><span class="sxs-lookup"><span data-stu-id="5fcb1-135">ar-ye</span></span>
- <span data-ttu-id="5fcb1-136">be</span><span class="sxs-lookup"><span data-stu-id="5fcb1-136">be</span></span>
- <span data-ttu-id="5fcb1-137">bg</span><span class="sxs-lookup"><span data-stu-id="5fcb1-137">bg</span></span>
- <span data-ttu-id="5fcb1-138">ca</span><span class="sxs-lookup"><span data-stu-id="5fcb1-138">ca</span></span>
- <span data-ttu-id="5fcb1-139">cs</span><span class="sxs-lookup"><span data-stu-id="5fcb1-139">cs</span></span>
- <span data-ttu-id="5fcb1-140">da</span><span class="sxs-lookup"><span data-stu-id="5fcb1-140">da</span></span>
- <span data-ttu-id="5fcb1-141">de</span><span class="sxs-lookup"><span data-stu-id="5fcb1-141">de</span></span>
- <span data-ttu-id="5fcb1-142">de-at</span><span class="sxs-lookup"><span data-stu-id="5fcb1-142">de-at</span></span>
- <span data-ttu-id="5fcb1-143">de-ch</span><span class="sxs-lookup"><span data-stu-id="5fcb1-143">de-ch</span></span>
- <span data-ttu-id="5fcb1-144">de-li</span><span class="sxs-lookup"><span data-stu-id="5fcb1-144">de-li</span></span>
- <span data-ttu-id="5fcb1-145">de-lu</span><span class="sxs-lookup"><span data-stu-id="5fcb1-145">de-lu</span></span>
- <span data-ttu-id="5fcb1-146">el</span><span class="sxs-lookup"><span data-stu-id="5fcb1-146">el</span></span>
- <span data-ttu-id="5fcb1-147">en-029</span><span class="sxs-lookup"><span data-stu-id="5fcb1-147">en-029</span></span>
- <span data-ttu-id="5fcb1-148">en-au</span><span class="sxs-lookup"><span data-stu-id="5fcb1-148">en-au</span></span>
- <span data-ttu-id="5fcb1-149">en-bz</span><span class="sxs-lookup"><span data-stu-id="5fcb1-149">en-bz</span></span>
- <span data-ttu-id="5fcb1-150">en-ca</span><span class="sxs-lookup"><span data-stu-id="5fcb1-150">en-ca</span></span>
- <span data-ttu-id="5fcb1-151">en-gb</span><span class="sxs-lookup"><span data-stu-id="5fcb1-151">en-gb</span></span>
- <span data-ttu-id="5fcb1-152">en-ie</span><span class="sxs-lookup"><span data-stu-id="5fcb1-152">en-ie</span></span>
- <span data-ttu-id="5fcb1-153">en-in</span><span class="sxs-lookup"><span data-stu-id="5fcb1-153">en-in</span></span>
- <span data-ttu-id="5fcb1-154">en-jm</span><span class="sxs-lookup"><span data-stu-id="5fcb1-154">en-jm</span></span>
- <span data-ttu-id="5fcb1-155">en-my</span><span class="sxs-lookup"><span data-stu-id="5fcb1-155">en-my</span></span>
- <span data-ttu-id="5fcb1-156">en-nz</span><span class="sxs-lookup"><span data-stu-id="5fcb1-156">en-nz</span></span>
- <span data-ttu-id="5fcb1-157">en-sg</span><span class="sxs-lookup"><span data-stu-id="5fcb1-157">en-sg</span></span>
- <span data-ttu-id="5fcb1-158">en-tt</span><span class="sxs-lookup"><span data-stu-id="5fcb1-158">en-tt</span></span>
- <span data-ttu-id="5fcb1-159">fi-fi</span><span class="sxs-lookup"><span data-stu-id="5fcb1-159">en-us</span></span>
- <span data-ttu-id="5fcb1-160">en-za</span><span class="sxs-lookup"><span data-stu-id="5fcb1-160">en-za</span></span>
- <span data-ttu-id="5fcb1-161">es</span><span class="sxs-lookup"><span data-stu-id="5fcb1-161">es</span></span>
- <span data-ttu-id="5fcb1-162">es-ar</span><span class="sxs-lookup"><span data-stu-id="5fcb1-162">es-ar</span></span>
- <span data-ttu-id="5fcb1-163">es-bo</span><span class="sxs-lookup"><span data-stu-id="5fcb1-163">es-bo</span></span>
- <span data-ttu-id="5fcb1-164">es-cl</span><span class="sxs-lookup"><span data-stu-id="5fcb1-164">es-cl</span></span>
- <span data-ttu-id="5fcb1-165">es-co</span><span class="sxs-lookup"><span data-stu-id="5fcb1-165">es-co</span></span>
- <span data-ttu-id="5fcb1-166">es-cr</span><span class="sxs-lookup"><span data-stu-id="5fcb1-166">es-cr</span></span>
- <span data-ttu-id="5fcb1-167">es-do</span><span class="sxs-lookup"><span data-stu-id="5fcb1-167">es-do</span></span>
- <span data-ttu-id="5fcb1-168">es-ec</span><span class="sxs-lookup"><span data-stu-id="5fcb1-168">es-ec</span></span>
- <span data-ttu-id="5fcb1-169">es-gt</span><span class="sxs-lookup"><span data-stu-id="5fcb1-169">es-gt</span></span>
- <span data-ttu-id="5fcb1-170">es-hn</span><span class="sxs-lookup"><span data-stu-id="5fcb1-170">es-hn</span></span>
- <span data-ttu-id="5fcb1-171">es-mx</span><span class="sxs-lookup"><span data-stu-id="5fcb1-171">es-mx</span></span>
- <span data-ttu-id="5fcb1-172">es-ni</span><span class="sxs-lookup"><span data-stu-id="5fcb1-172">es-ni</span></span>
- <span data-ttu-id="5fcb1-173">es-pa</span><span class="sxs-lookup"><span data-stu-id="5fcb1-173">es-pa</span></span>
- <span data-ttu-id="5fcb1-174">es-pe</span><span class="sxs-lookup"><span data-stu-id="5fcb1-174">es-pe</span></span>
- <span data-ttu-id="5fcb1-175">es-pr</span><span class="sxs-lookup"><span data-stu-id="5fcb1-175">es-pr</span></span>
- <span data-ttu-id="5fcb1-176">es-py</span><span class="sxs-lookup"><span data-stu-id="5fcb1-176">es-py</span></span>
- <span data-ttu-id="5fcb1-177">es-sv</span><span class="sxs-lookup"><span data-stu-id="5fcb1-177">es-sv</span></span>
- <span data-ttu-id="5fcb1-178">es-tr</span><span class="sxs-lookup"><span data-stu-id="5fcb1-178">es-tr</span></span>
- <span data-ttu-id="5fcb1-179">es-uy</span><span class="sxs-lookup"><span data-stu-id="5fcb1-179">es-uy</span></span>
- <span data-ttu-id="5fcb1-180">es-ve</span><span class="sxs-lookup"><span data-stu-id="5fcb1-180">es-ve</span></span>
- <span data-ttu-id="5fcb1-181">et</span><span class="sxs-lookup"><span data-stu-id="5fcb1-181">et</span></span>
- <span data-ttu-id="5fcb1-182">eu</span><span class="sxs-lookup"><span data-stu-id="5fcb1-182">eu</span></span>
- <span data-ttu-id="5fcb1-183">fa</span><span class="sxs-lookup"><span data-stu-id="5fcb1-183">fa</span></span>
- <span data-ttu-id="5fcb1-184">fi</span><span class="sxs-lookup"><span data-stu-id="5fcb1-184">fi</span></span>
- <span data-ttu-id="5fcb1-185">fo</span><span class="sxs-lookup"><span data-stu-id="5fcb1-185">fo</span></span>
- <span data-ttu-id="5fcb1-186">fr</span><span class="sxs-lookup"><span data-stu-id="5fcb1-186">fr</span></span>
- <span data-ttu-id="5fcb1-187">fr-be</span><span class="sxs-lookup"><span data-stu-id="5fcb1-187">fr-be</span></span>
- <span data-ttu-id="5fcb1-188">fr-ca</span><span class="sxs-lookup"><span data-stu-id="5fcb1-188">fr-ca</span></span>
- <span data-ttu-id="5fcb1-189">fr-ch</span><span class="sxs-lookup"><span data-stu-id="5fcb1-189">fr-ch</span></span>
- <span data-ttu-id="5fcb1-190">fr-lu</span><span class="sxs-lookup"><span data-stu-id="5fcb1-190">fr-lu</span></span>
- <span data-ttu-id="5fcb1-191">hi</span><span class="sxs-lookup"><span data-stu-id="5fcb1-191">hi</span></span>
- <span data-ttu-id="5fcb1-192">h</span><span class="sxs-lookup"><span data-stu-id="5fcb1-192">hr</span></span>
- <span data-ttu-id="5fcb1-193">hu</span><span class="sxs-lookup"><span data-stu-id="5fcb1-193">hu</span></span>
- <span data-ttu-id="5fcb1-194">on</span><span class="sxs-lookup"><span data-stu-id="5fcb1-194">is</span></span>
- <span data-ttu-id="5fcb1-195">it</span><span class="sxs-lookup"><span data-stu-id="5fcb1-195">it</span></span>
- <span data-ttu-id="5fcb1-196">it-ch</span><span class="sxs-lookup"><span data-stu-id="5fcb1-196">it-ch</span></span>
- <span data-ttu-id="5fcb1-197">ja</span><span class="sxs-lookup"><span data-stu-id="5fcb1-197">ja</span></span>
- <span data-ttu-id="5fcb1-198">lt</span><span class="sxs-lookup"><span data-stu-id="5fcb1-198">lt</span></span>
- <span data-ttu-id="5fcb1-199">lv</span><span class="sxs-lookup"><span data-stu-id="5fcb1-199">lv</span></span>
- <span data-ttu-id="5fcb1-200">mk</span><span class="sxs-lookup"><span data-stu-id="5fcb1-200">mk</span></span>
- <span data-ttu-id="5fcb1-201">ms</span><span class="sxs-lookup"><span data-stu-id="5fcb1-201">ms</span></span>
- <span data-ttu-id="5fcb1-202">mt</span><span class="sxs-lookup"><span data-stu-id="5fcb1-202">mt</span></span>
- <span data-ttu-id="5fcb1-203">nb-no</span><span class="sxs-lookup"><span data-stu-id="5fcb1-203">nb-no</span></span>
- <span data-ttu-id="5fcb1-204">nl</span><span class="sxs-lookup"><span data-stu-id="5fcb1-204">nl</span></span>
- <span data-ttu-id="5fcb1-205">nl-be</span><span class="sxs-lookup"><span data-stu-id="5fcb1-205">nl-be</span></span>
- <span data-ttu-id="5fcb1-206">nn-no</span><span class="sxs-lookup"><span data-stu-id="5fcb1-206">nn-no</span></span>
- <span data-ttu-id="5fcb1-207">pl</span><span class="sxs-lookup"><span data-stu-id="5fcb1-207">pl</span></span>
- <span data-ttu-id="5fcb1-208">pt-br</span><span class="sxs-lookup"><span data-stu-id="5fcb1-208">pt-br</span></span>
- <span data-ttu-id="5fcb1-209">ro</span><span class="sxs-lookup"><span data-stu-id="5fcb1-209">ro</span></span>
- <span data-ttu-id="5fcb1-210">ru</span><span class="sxs-lookup"><span data-stu-id="5fcb1-210">ru</span></span>
- <span data-ttu-id="5fcb1-211">ru-ru</span><span class="sxs-lookup"><span data-stu-id="5fcb1-211">ru-ru</span></span>
- <span data-ttu-id="5fcb1-212">sk</span><span class="sxs-lookup"><span data-stu-id="5fcb1-212">sk</span></span>
- <span data-ttu-id="5fcb1-213">sl</span><span class="sxs-lookup"><span data-stu-id="5fcb1-213">sl</span></span>
- <span data-ttu-id="5fcb1-214">sq</span><span class="sxs-lookup"><span data-stu-id="5fcb1-214">sq</span></span>
- <span data-ttu-id="5fcb1-215">sr</span><span class="sxs-lookup"><span data-stu-id="5fcb1-215">sr</span></span>
- <span data-ttu-id="5fcb1-216">sr-la</span><span class="sxs-lookup"><span data-stu-id="5fcb1-216">sr-la</span></span>
- <span data-ttu-id="5fcb1-217">sv</span><span class="sxs-lookup"><span data-stu-id="5fcb1-217">sv</span></span>
- <span data-ttu-id="5fcb1-218">sv-fi</span><span class="sxs-lookup"><span data-stu-id="5fcb1-218">sv-fi</span></span>
- <span data-ttu-id="5fcb1-219">th</span><span class="sxs-lookup"><span data-stu-id="5fcb1-219">th</span></span>
- <span data-ttu-id="5fcb1-220">tn</span><span class="sxs-lookup"><span data-stu-id="5fcb1-220">tn</span></span>
- <span data-ttu-id="5fcb1-221">tr</span><span class="sxs-lookup"><span data-stu-id="5fcb1-221">tr</span></span>
- <span data-ttu-id="5fcb1-222">uk</span><span class="sxs-lookup"><span data-stu-id="5fcb1-222">uk</span></span>
- <span data-ttu-id="5fcb1-223">ur</span><span class="sxs-lookup"><span data-stu-id="5fcb1-223">ur</span></span>
- <span data-ttu-id="5fcb1-224">xh</span><span class="sxs-lookup"><span data-stu-id="5fcb1-224">xh</span></span>
- <span data-ttu-id="5fcb1-225">zh-hans</span><span class="sxs-lookup"><span data-stu-id="5fcb1-225">zh-hans</span></span>
- <span data-ttu-id="5fcb1-226">zh-hk</span><span class="sxs-lookup"><span data-stu-id="5fcb1-226">zh-hk</span></span>
- <span data-ttu-id="5fcb1-227">zh-sg</span><span class="sxs-lookup"><span data-stu-id="5fcb1-227">zh-sg</span></span>
- <span data-ttu-id="5fcb1-228">zu</span><span class="sxs-lookup"><span data-stu-id="5fcb1-228">zu</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5fcb1-229">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="5fcb1-229">Additional resources</span></span>

[<span data-ttu-id="5fcb1-230">Logon lisääminen</span><span class="sxs-lookup"><span data-stu-id="5fcb1-230">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="5fcb1-231">Sivuston teeman valitseminen</span><span class="sxs-lookup"><span data-stu-id="5fcb1-231">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="5fcb1-232">CSS-ohitustiedostojen parissa työskentely</span><span class="sxs-lookup"><span data-stu-id="5fcb1-232">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="5fcb1-233">Favicon-kuvakkeen lisääminen</span><span class="sxs-lookup"><span data-stu-id="5fcb1-233">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="5fcb1-234">Tervetuloviestin lisääminen</span><span class="sxs-lookup"><span data-stu-id="5fcb1-234">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="5fcb1-235">Copyright-ilmoituksen lisääminen</span><span class="sxs-lookup"><span data-stu-id="5fcb1-235">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="5fcb1-236">Komentosarjakoodin lisääminen sivuston sivuihin telemetrian tukemiseksi</span><span class="sxs-lookup"><span data-stu-id="5fcb1-236">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)
