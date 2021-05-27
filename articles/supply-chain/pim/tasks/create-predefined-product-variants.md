---
title: Luo ennalta määritetyt tuotevariantit
description: Tässä menettelyssä selvitetään tuotevariantien luonti päätuotteelle käyttämällä tuotedimensioiden yhdistelmiä.
author: t-benebo
ms.date: 04/22/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResProductListPage, EcoResProductCreate, EcoResProductDetails, EcoResProductMasterDimension, EcoResProductVariants, EcoResProductVariantSuggestions, EcoResProductVariantsPendingReleaseFormPart, EcoResProductVariantSuggestionsEnhanced
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 6f78441445baecba279f96eb3935d9ebbb4ff03f
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021905"
---
# <a name="predefined-product-variants"></a><span data-ttu-id="fd6fb-103">Ennalta määritellyt tuotevariantit</span><span class="sxs-lookup"><span data-stu-id="fd6fb-103">Predefined product variants</span></span>

[!include [banner](../../includes/banner.md)]

## <a name="example-scenario-create-predefined-product-variants"></a><span data-ttu-id="fd6fb-104">Esimerkkiskenaario: Luo ennalta määriteltyjä tuotevariantteja</span><span class="sxs-lookup"><span data-stu-id="fd6fb-104">Example scenario: Create predefined product variants</span></span>

<span data-ttu-id="fd6fb-105">Tässä esimerkkiskenaariossa näytetään tuotevariantien luonti päätuotteelle käyttämällä tuotedimensioiden yhdistelmiä.</span><span class="sxs-lookup"><span data-stu-id="fd6fb-105">This example scenario shows how to create product variants for a product master using a combinations of product dimensions.</span></span>

### <a name="make-demo-data-available"></a><span data-ttu-id="fd6fb-106">Demotietojen ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="fd6fb-106">Make demo data available</span></span>

<span data-ttu-id="fd6fb-107">Tämän skenaarion noudattaminen tässä ehdotettuja arvoja käyttämällä edellyttää, että demotiedot on asennettu ja että *USMF*-yritys on valittu.</span><span class="sxs-lookup"><span data-stu-id="fd6fb-107">To follow this scenario using the values suggested here, you must have demo data installed, and you must select the *USMF* legal entity.</span></span>

### <a name="step-1-create-a-product-master"></a><span data-ttu-id="fd6fb-108">Vaihe 1: Luo päätuote</span><span class="sxs-lookup"><span data-stu-id="fd6fb-108">Step 1: Create a product master</span></span>

<span data-ttu-id="fd6fb-109">Päätuotteen luominen:</span><span class="sxs-lookup"><span data-stu-id="fd6fb-109">To create a product master:</span></span>

1. <span data-ttu-id="fd6fb-110">Siirry kohtaan **Tuotetietojen hallinta > Tuotteet > Päätuotteet**.</span><span class="sxs-lookup"><span data-stu-id="fd6fb-110">Go to **Product information management > Products > Product masters**.</span></span>
1. <span data-ttu-id="fd6fb-111">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="fd6fb-111">Select **New**.</span></span>
1. <span data-ttu-id="fd6fb-112">Jos **Tuotenumero**-kentässä ei vielä ole numeroa näkyvissä, kirjoita arvo.</span><span class="sxs-lookup"><span data-stu-id="fd6fb-112">If the **Product number** field doesn't already show a number, then enter a value.</span></span> <span data-ttu-id="fd6fb-113">Tämä vaaditaan vain, jos kentälle ei ole määritetty numerosarjaa.</span><span class="sxs-lookup"><span data-stu-id="fd6fb-113">This is only required if no number sequence has been set for this field.</span></span>
1. <span data-ttu-id="fd6fb-114">Syötä **Tuotenimi** -kenttään nimi.</span><span class="sxs-lookup"><span data-stu-id="fd6fb-114">Enter a name in the **Product name** field.</span></span>
1. <span data-ttu-id="fd6fb-115">Valitse **Tuotedimensioryhmä**-kentästä tuotedimensioryhmä *SizeCol* (koko ja väri).</span><span class="sxs-lookup"><span data-stu-id="fd6fb-115">In the **Product dimension group** field, select the product dimension group *SizeCol* (Size and Color).</span></span>
1. <span data-ttu-id="fd6fb-116">Luo ja avaa uusi päätuote valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="fd6fb-116">Select **OK** to create and open the new product master.</span></span>

### <a name="step-2-add-product-dimensions"></a><span data-ttu-id="fd6fb-117">Vaihe 2: Lisää tuotedimensiot</span><span class="sxs-lookup"><span data-stu-id="fd6fb-117">Step 2: Add product dimensions</span></span>

<span data-ttu-id="fd6fb-118">Tässä esimerkissä havainnollistetaan, kuinka tuotedimensiot voi antaa käsin.</span><span class="sxs-lookup"><span data-stu-id="fd6fb-118">This example shows how to manually enter product dimensions.</span></span> <span data-ttu-id="fd6fb-119">Voit myös valita koko-, väri- tai tyyliryhmän, joka sisältää haluamasi tuotedimension arvot.</span><span class="sxs-lookup"><span data-stu-id="fd6fb-119">You can also choose to select a size, color, or style group that includes the product dimension values you want to use.</span></span>

<span data-ttu-id="fd6fb-120">Tuotedimensioiden lisääminen:</span><span class="sxs-lookup"><span data-stu-id="fd6fb-120">To add product dimensions:</span></span>

1. <span data-ttu-id="fd6fb-121">Kun uusi päätuote on vielä avoinna, valitse **Tuotedimensiot** toimintoruudusta.</span><span class="sxs-lookup"><span data-stu-id="fd6fb-121">With your new product master still open, select **Product dimensions** on the Action Pane.</span></span>
1. <span data-ttu-id="fd6fb-122">Avaa **Koko**-välilehti ja lisää ruudukkoon rivi valitsemalla työkaluriviltä **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="fd6fb-122">Open the **Size** tab and select **New** on the toolbar to add a row to the grid.</span></span> <span data-ttu-id="fd6fb-123">Tee uudelle riville seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="fd6fb-123">Make the following settings for the new row:</span></span>
    - <span data-ttu-id="fd6fb-124">**Koko:** Valitse koon arvo.</span><span class="sxs-lookup"><span data-stu-id="fd6fb-124">**Size:** Select a size value.</span></span>
    - <span data-ttu-id="fd6fb-125">**Nimi:** Syötä koolle nimi.</span><span class="sxs-lookup"><span data-stu-id="fd6fb-125">**Name:** Enter a name for the size.</span></span>
1. <span data-ttu-id="fd6fb-126">Valitse työkaluriviltä **Uusi** ja lisää toinen koko ruudukkoon, jossa on uusi **Koko** ja **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="fd6fb-126">Select **New** on the toolbar and add a second size to the grid with a new **Size** and **Name**.</span></span>
1. <span data-ttu-id="fd6fb-127">Avaa **Värit**-välilehti ja lisää ruudukkoon rivi valitsemalla työkaluriviltä **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="fd6fb-127">Open the **Colors** tab and select **New** on the toolbar to add a row to the grid.</span></span> <span data-ttu-id="fd6fb-128">Tee uudelle riville seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="fd6fb-128">Make the following settings for the new row:</span></span>
    - <span data-ttu-id="fd6fb-129">**Väri:** Valitse väriarvo.</span><span class="sxs-lookup"><span data-stu-id="fd6fb-129">**Color:** Select a color value.</span></span>
    - <span data-ttu-id="fd6fb-130">**Nimi:** Syötä värille nimi.</span><span class="sxs-lookup"><span data-stu-id="fd6fb-130">**Name:** Enter a name for the color.</span></span>
1. <span data-ttu-id="fd6fb-131">Valitse työkaluriviltä **Uusi** ja lisää toinen väri ruudukkoon, jossa on uusi **Väri** ja **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="fd6fb-131">Select **New** on the toolbar and add a second color to the grid with a new **Color** and **Name**.</span></span>
1. <span data-ttu-id="fd6fb-132">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="fd6fb-132">Select **Save**.</span></span>
1. <span data-ttu-id="fd6fb-133">Voit palata uuteen päätuotteeseen sulkemalla sivun.</span><span class="sxs-lookup"><span data-stu-id="fd6fb-133">Close the page to return to your new product master.</span></span>

### <a name="step-3-generate-product-variants"></a><span data-ttu-id="fd6fb-134">Vaihe 3: Luo tuotevariantit</span><span class="sxs-lookup"><span data-stu-id="fd6fb-134">Step 3: Generate product variants</span></span>

> [!NOTE]
> <span data-ttu-id="fd6fb-135">Tässä osassa kuvataan, miten tuotevariantteja luodaan, kun *Muuttujaehdotukset-sivun parannukset* -toiminto ei ole käytössä.</span><span class="sxs-lookup"><span data-stu-id="fd6fb-135">This section describes how to generate product variants when the *Variant suggestions page improvements* feature isn't enabled.</span></span> <span data-ttu-id="fd6fb-136">Seuraavassa osassa on tietoja siitä, miten tuotevariantteja luodaan, kun tämä ominaisuus on käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="fd6fb-136">See the next section for details about how to generate product variants when that feature is available.</span></span>

<span data-ttu-id="fd6fb-137">Tuotevarianttien luonti:</span><span class="sxs-lookup"><span data-stu-id="fd6fb-137">To generate product variants:</span></span>

1. <span data-ttu-id="fd6fb-138">Kun uusi päätuote on vielä avoinna, valitse **Tuotevariantit** toimintoruudusta.</span><span class="sxs-lookup"><span data-stu-id="fd6fb-138">With your new product master still open, select **Product variants** on the Action Pane.</span></span>
1. <span data-ttu-id="fd6fb-139">Valitse toimintoruudussa **Muuttujaehdotukset**.</span><span class="sxs-lookup"><span data-stu-id="fd6fb-139">Select **Variant suggestions** on the Action Pane.</span></span>
1. <span data-ttu-id="fd6fb-140">Järjestelmä luo luettelon, joka sisältää kaikki mahdolliset tuotteeseen määritetyt koko- ja väriyhdistelmät.</span><span class="sxs-lookup"><span data-stu-id="fd6fb-140">The system generates a list with all possible combinations of the sizes and colors you defined for the product.</span></span> <span data-ttu-id="fd6fb-141">Valitse työkalurivillä **Valitse kaikki**.</span><span class="sxs-lookup"><span data-stu-id="fd6fb-141">Select **Select all** on the toolbar.</span></span>
    - <span data-ttu-id="fd6fb-142">Tässä esimerkissä valitse kaikki mahdolliset muuttujat.</span><span class="sxs-lookup"><span data-stu-id="fd6fb-142">In this example, select all of the possible variants.</span></span> <span data-ttu-id="fd6fb-143">Jos haluat käyttää vain mahdollisen tuotedimensioyhdistelmän alijoukkoa, valitse vain tarvittavat valintaruudut.</span><span class="sxs-lookup"><span data-stu-id="fd6fb-143">If you only want to use a subset of the possible product dimension combinations, select only the required check boxes as needed.</span></span>  
1. <span data-ttu-id="fd6fb-144">Valitse **Luo**.</span><span class="sxs-lookup"><span data-stu-id="fd6fb-144">Select **Create**.</span></span>
1. <span data-ttu-id="fd6fb-145">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="fd6fb-145">Select **Save**.</span></span>

## <a name="improved-variant-suggestions"></a><span data-ttu-id="fd6fb-146">Parannetut muuttujaehdotukset</span><span class="sxs-lookup"><span data-stu-id="fd6fb-146">Improved variant suggestions</span></span>

[!INCLUDE [preview-banner-section](../../../includes/preview-banner-section.md)]

<span data-ttu-id="fd6fb-147">*Muuttujaehdotukset-sivun parannukset* -ominaisuus parantaa **Muuttujaehdotukset**-sivua niiden yritysten suorituskykyyn ja käytettävyyteen liittyvien ongelmien käsittelemiseksi, joilla on suuri määrä tuotedimensioyhdistelmiä.</span><span class="sxs-lookup"><span data-stu-id="fd6fb-147">The *Variant suggestions page improvements* feature improves the **Variant suggestions** page to address performance and usability issues for companies that have a high number of product dimension combinations.</span></span> <span data-ttu-id="fd6fb-148">Paranneltu prosessi, jossa valitaan tuotedimensioarvot, joiden perusteella muuttujaehdotuksia luodaan, nopeuttaa ja helpottaa asianmukaisten tuotevarianttien tunnistamista ja vapauttamista.</span><span class="sxs-lookup"><span data-stu-id="fd6fb-148">The enhanced process for selecting the product dimension values for which to generate variant suggestions makes it faster and easier to identify and release the relevant set of product variants.</span></span>

<span data-ttu-id="fd6fb-149">Tämä ominaisuus lisää seuraavat parannukset:</span><span class="sxs-lookup"><span data-stu-id="fd6fb-149">The following improvements are added by this feature:</span></span>

- <span data-ttu-id="fd6fb-150">**Varianttiehdotusten lykätty luominen::** **Varianttiehdotukset**-sivun ensimmäisellä avauskerralla ei enää näytetä ehdotuksia.</span><span class="sxs-lookup"><span data-stu-id="fd6fb-150">**Deferred generation of variant suggestions:** The **Variant suggestions** page no longer shows suggestions when you first open it.</span></span> <span data-ttu-id="fd6fb-151">Sen sijaan sinun on nimenomaisesti valittava haluamasi arvot ja luotava yhdistelmät valitsemalla **Ehdota**-painike.</span><span class="sxs-lookup"><span data-stu-id="fd6fb-151">Instead, you must explicitly choose which values you will need and then select the **Suggest** button to generate the combinations.</span></span> <span data-ttu-id="fd6fb-152">Näin prosessi on näkyvämpi ja vuorovaikutteisempi.</span><span class="sxs-lookup"><span data-stu-id="fd6fb-152">This makes the process more visible and interactive.</span></span>
- <span data-ttu-id="fd6fb-153">**Dimension arvojen valitseminen:** Kun dimension arvoja on useita, käyttäjä haluaa yleensä luoda varianttiehdotuksia, jotka sisältävät vain joitakin arvoja (kuten uuden väri- tai tyylijoukon esittely).</span><span class="sxs-lookup"><span data-stu-id="fd6fb-153">**Selection of dimensions values:** When you have many dimension values, you are typically interested in generating variant suggestions that include just a few of them (such as when introducing a new set of colors or styles).</span></span> <span data-ttu-id="fd6fb-154">Tämän parannetun suunnittelun avulla käyttäjä voi valita ne dimension arvot, joille tuotevarianttiehdotukset halutaan luoda.</span><span class="sxs-lookup"><span data-stu-id="fd6fb-154">With the improved design, you can select the dimension values for which you want to generate product variant suggestions.</span></span> <span data-ttu-id="fd6fb-155">Tämä kasvattaa suuresti ehdotettujen varianttien relevanssia ja parantaa sekä järjestelmän suorituskykyä että käyttäjän tuottavuutta.</span><span class="sxs-lookup"><span data-stu-id="fd6fb-155">This greatly increases the relevance of the suggested variants and improves both system performance and user productivity.</span></span>

### <a name="turn-on-the-variant-suggestions-page-improvements-feature"></a><span data-ttu-id="fd6fb-156">Muuttujaehdotus-sivun parannustoiminnon ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="fd6fb-156">Turn on the Variant suggestions page improvements feature</span></span>

<span data-ttu-id="fd6fb-157">Ennen kuin voit käyttää *Muuttujaehdotukset-sivun parannukset* -toimintoa, sen pitää olla otettu käyttöön järjestelmässäsi.</span><span class="sxs-lookup"><span data-stu-id="fd6fb-157">Before you can use *Variant suggestions page improvements* feature, it must be turned on in your system.</span></span> <span data-ttu-id="fd6fb-158">Järjestelmänvalvojat voivat käyttää [toimintojen hallinnan](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) asetuksia ja tarkistaa toiminnon tilan sekä laittaa sen päälle tarvittaessa.</span><span class="sxs-lookup"><span data-stu-id="fd6fb-158">Admins can use the [feature management](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="fd6fb-159">**Ominaisuuksien hallinta** -työtilassa ominaisuus on luetteloitu seuraavalla tavalla:</span><span class="sxs-lookup"><span data-stu-id="fd6fb-159">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="fd6fb-160">**Moduuli:** *Tuotetietojen hallinta*</span><span class="sxs-lookup"><span data-stu-id="fd6fb-160">**Module:** *Product information management*</span></span>
- <span data-ttu-id="fd6fb-161">**Ominaisuuden nimi:** *Muuttujaehdotukset-sivun parannukset*</span><span class="sxs-lookup"><span data-stu-id="fd6fb-161">**Feature name:** *Variant suggestions page improvements*</span></span>

### <a name="work-with-the-improved-variant-suggestions"></a><span data-ttu-id="fd6fb-162">Paranneltujen muuttujaehdotusten käyttäminen</span><span class="sxs-lookup"><span data-stu-id="fd6fb-162">Work with the improved variant suggestions</span></span>

<span data-ttu-id="fd6fb-163">Tuotevarianttiehdotusten luominen, kun *Muuttujaehdotukset-sivun parannukset* -toiminto on käytössä:</span><span class="sxs-lookup"><span data-stu-id="fd6fb-163">To generate product variant suggestions when the *Variant suggestions page improvements* feature is enabled:</span></span>

1. <span data-ttu-id="fd6fb-164">Avaa tai luo päätuote ja lisää tarvittavat tuotedimensiot siihen edellisessä osassa kuvatulla tavalla.</span><span class="sxs-lookup"><span data-stu-id="fd6fb-164">Open or create a product master and add the required product dimensions to it, as described in the previous section.</span></span>
1. <span data-ttu-id="fd6fb-165">Kun päätuote on avoinna, valitse **Tuotevariantit** toimintoruudusta.</span><span class="sxs-lookup"><span data-stu-id="fd6fb-165">With the product master open, select **Product variants** on the Action Pane.</span></span>
1. <span data-ttu-id="fd6fb-166">Valitse toimintoruudussa **Muuttujaehdotukset**.</span><span class="sxs-lookup"><span data-stu-id="fd6fb-166">Select **Variant suggestions** on the Action Pane.</span></span>
1. <span data-ttu-id="fd6fb-167">Valitse kullekin dimensiolle arvot, joita haluat käyttää.</span><span class="sxs-lookup"><span data-stu-id="fd6fb-167">Select the values that you want to use for each of the dimensions.</span></span>
1. <span data-ttu-id="fd6fb-168">Valitse yläreunan työkaluriviltä **Ehdota**.</span><span class="sxs-lookup"><span data-stu-id="fd6fb-168">On the top toolbar, select **Suggest**.</span></span>
1. <span data-ttu-id="fd6fb-169">Järjestelmä luo luettelon, joka sisältää kaikki mahdolliset valitut koko- ja väriyhdistelmät.</span><span class="sxs-lookup"><span data-stu-id="fd6fb-169">The system generates a list with all possible combinations of the sizes and colors you selected.</span></span> <span data-ttu-id="fd6fb-170">Valitse **Ehdotetut muuttujat** -pikavälilehdessä kunkin käytettävän tuotedimensioyhdistelmän valintaruutu tai valitse **Valitse kaikki** työkalurivillä valitaksesi ne kaikki.</span><span class="sxs-lookup"><span data-stu-id="fd6fb-170">On the **Suggested variants** FastTab, select the check box for each product dimension combination that you want to use, or select **Select all** on the toolbar to select all of them.</span></span>  
1. <span data-ttu-id="fd6fb-171">Valitse **Luo** lisätäksesi muuttujat nykyiseen päätuotteeseen.</span><span class="sxs-lookup"><span data-stu-id="fd6fb-171">Select **Create** to add the variants to the current product master.</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
