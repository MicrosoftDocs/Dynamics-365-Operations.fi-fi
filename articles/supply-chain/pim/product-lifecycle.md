---
title: Tuotteen elinkaaren tila
description: Tuotteen elinkaaren tila kirjaa julkaistun tuotteen tai tuotevariantin elinkaaren tilan.
author: cvocph
manager: AnnBe
ms.date: 12/08/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResProductLifecycleState, EcoResReleasedProductLifecycleStateChanges
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: cvocph
ms.dyn365.ops.version: 7.3
ms.search.validFrom: 2017-12-31
ms.translationtype: HT
ms.sourcegitcommit: ceea24519d641c676521771cee274feb64ca7783
ms.openlocfilehash: 8337f1dfb938f9fa69924e77a25a68ee56dbd2ac
ms.contentlocale: fi-fi
ms.lasthandoff: 01/19/2018

---

# <a name="product-lifecycle-state"></a><span data-ttu-id="6ebba-103">Tuotteen elinkaaren tila</span><span class="sxs-lookup"><span data-stu-id="6ebba-103">Product lifecycle state</span></span> 

[!include[banner](../includes/banner.md)]


<span data-ttu-id="6ebba-104">Tuotteen elinkaaren tila kirjaa julkaistun tuotteen tai tuotevariantin elinkaaren tilan.</span><span class="sxs-lookup"><span data-stu-id="6ebba-104">A product lifecycle state documents the lifecycle state of a released product or product variant.</span></span> <span data-ttu-id="6ebba-105">Tuotteen elinkaaren tilat määrittää käyttäjä, yleensä tuotepäällikkö tai tuotteen päätietojen hallinta.</span><span class="sxs-lookup"><span data-stu-id="6ebba-105">Product lifecycle states are defined by the user, typically a product manager or a product master data manager.</span></span> <span data-ttu-id="6ebba-106">Tietty elinkaaren tila voi vaikuttaa tiettyihin liiketoimintaprosesseihin, kuten pääsuunnitteluun.</span><span class="sxs-lookup"><span data-stu-id="6ebba-106">Specific business processes, such as master planning, can be affected by a specific lifecycle state.</span></span>   
 
<span data-ttu-id="6ebba-107">Vapautettu tuote tai tuotevariantti voidaan liittää tuotteen elinkaaren tilaan, joka kirjaa, mikä on tietyn tuotteen tai variantin tämän hetkinen elinkaaren tila.</span><span class="sxs-lookup"><span data-stu-id="6ebba-107">A released product or product variant can be associated with a product lifecycle state that documents in which lifecycle state a specific product or variant is currently in.</span></span> <span data-ttu-id="6ebba-108">Voit määrittää haluamasi määrän tuotteen elinkaaren tiloja määrittämällä tilalle nimen ja kuvauksen.</span><span class="sxs-lookup"><span data-stu-id="6ebba-108">You can define any number of product lifecycle states by assigning a state name and description.</span></span> <span data-ttu-id="6ebba-109">Voit valita yhden elinkaarin tilan uusien vapautettujen tuotteiden oletustilaksi.</span><span class="sxs-lookup"><span data-stu-id="6ebba-109">You can select one lifecycle state as the default state for new released products.</span></span> <span data-ttu-id="6ebba-110">Vapautetut tuotevariantit perivät luonnin yhteydessä tuotteen elinkaaren tilan vapautetulta päätuotteelta.</span><span class="sxs-lookup"><span data-stu-id="6ebba-110">Released product variants inherit their product lifecycle state from their released product master on creation.</span></span> <span data-ttu-id="6ebba-111">Kun muutat vapautetun päätuotteen elinkaaren tilaa, voit halutessasi päivittää kaikki sellaisen aiemmin luodut variantit, joilla on sama alkuperäinen tila.</span><span class="sxs-lookup"><span data-stu-id="6ebba-111">When changing the lifecycle state on a released product master, you can choose to update all existing variants that have the same original state.</span></span>  

## <a name="create-a-new-product-lifecycle-state"></a><span data-ttu-id="6ebba-112">Uuden tuotteen elinkaaren tilan luominen</span><span class="sxs-lookup"><span data-stu-id="6ebba-112">Create a new product lifecycle state</span></span> 
 
- <span data-ttu-id="6ebba-113">Toista tai lue tehtäväopas **Uuden tuotteen elinkaaren tilan luominen**, kun haluat luoda uuden tuotteen elinkaaren tilan.</span><span class="sxs-lookup"><span data-stu-id="6ebba-113">To create a new product lifecycle state, play or read the task guide **Create a new product lifecycle state**.</span></span> 

-  <span data-ttu-id="6ebba-114">Toista tai lue tehtäväopas **Tuotteen elinkaaren oletustilan luominen**, kun haluat luoda tuotteen elinkaaren oletustilan.</span><span class="sxs-lookup"><span data-stu-id="6ebba-114">To create a default product lifecycle state, play or read the task guide **Create a default product lifecycle state**.</span></span>   

## <a name="associate-product-lifecycle-states-to-released-products"></a><span data-ttu-id="6ebba-115">Tuotteen elinkaaren tilojen liittäminen vapautettuihin tuotteisiin</span><span class="sxs-lookup"><span data-stu-id="6ebba-115">Associate product lifecycle states to released products</span></span>  

<span data-ttu-id="6ebba-116">Tuotteen elinkaaren tilan voi liittää eri tavoin vapautettuihin tuotteisiin tai tuotevariantteihin.</span><span class="sxs-lookup"><span data-stu-id="6ebba-116">There are multiple ways to associate a product lifecycle state to released products or product variants.</span></span>

-  <span data-ttu-id="6ebba-117">Kun uusi vapautettu tuote luodaan, oletusarvoinen **tuotteen elinkaaren tila** määritetään automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="6ebba-117">On creation of a new released product, the default **Product lifecycle state** is automatically assigned.</span></span> 
-  <span data-ttu-id="6ebba-118">Kun tuote vapautetaan yritykseen, oletusarvoinen **tuotteen elinkaaren tila** määritetään automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="6ebba-118">On release of a product to a legal entity, the default **Product lifecycle state** is automatically assigned.</span></span> 
-  <span data-ttu-id="6ebba-119">Kun tuotevariantti vapautetaan yritykseen, yrityksessä vapautettuun päätuotteeseen liitetty **tuotteen elinkaaren tila** määritetään automaattisesti uuteen varianttiin.</span><span class="sxs-lookup"><span data-stu-id="6ebba-119">On release of a product variant to a legal entity, the **Product lifecycle state** associated to the released product master in this legal entity is automatically assigned to the new variant.</span></span> 

<span data-ttu-id="6ebba-120">Voit päivittää tuotteen elinkaaren tilan manuaalisesti käyttämällä</span><span class="sxs-lookup"><span data-stu-id="6ebba-120">You can manually update the product lifecycle state by using:</span></span> 

-    <span data-ttu-id="6ebba-121">**Vapautetut tuotteet** -luettelosivua tai **tietonäkymää**</span><span class="sxs-lookup"><span data-stu-id="6ebba-121">The **Released products** list page or **Details view**.</span></span> 
-  <span data-ttu-id="6ebba-122">**Vapautetut tuotevariantit** -luettelosivua tai **tietonäkymää**.</span><span class="sxs-lookup"><span data-stu-id="6ebba-122">The **Released product variants** list page or **Details view**.</span></span> 
-  <span data-ttu-id="6ebba-123">Voit etsiä vanhentuneita tuotteita tai tuotevariantteja kysynnän ja liitetyn elinkaaren tilan mukaan.</span><span class="sxs-lookup"><span data-stu-id="6ebba-123">Find the obsolete products or product variants based on demand and associate a lifecycle state.</span></span>  

<span data-ttu-id="6ebba-124">Saat lisätietoja tuotteen elinkaaren tilojen liittämisestä toistamalla tai lukemalla seuraavat tehtäväoppaat.</span><span class="sxs-lookup"><span data-stu-id="6ebba-124">For detailed information about how to associate product lifecycle states, play or read the following two task guides.</span></span>

-  <span data-ttu-id="6ebba-125">Toista tai lue **Tuotteen elinkaaren tilan määrittäminen vapautettuun päätuotteeseen** -tehtäväopas, jos haluat liittää tuotteen elinkaaren tilan vapautettuun päätuotteeseen.</span><span class="sxs-lookup"><span data-stu-id="6ebba-125">To associate a product lifecycle state to a released product master, play or read the task guide **Assign a product lifecycle state to a released product master**.</span></span> 

-  <span data-ttu-id="6ebba-126">Toista tai lue **Tuotteen elinkaaren tilan määrittäminen vapautettuun tuotteeseen** -tehtäväopas, jos haluat liittää tuotteen elinkaaren tilan vapautettuun tuotteeseen.</span><span class="sxs-lookup"><span data-stu-id="6ebba-126">To associate a product lifecycle state to a release product, play or read the task guide **Assign a product lifecycle state to a released product**.</span></span> 

## <a name="impact-on-master-planning"></a><span data-ttu-id="6ebba-127">Vaikutus pääsuunnitteluun</span><span class="sxs-lookup"><span data-stu-id="6ebba-127">Impact on master planning</span></span> 

<span data-ttu-id="6ebba-128">Tuotteen elinkaaren tilalla on vain yksi valvontamerkki: **On käytettävissä suunnitteluun**.</span><span class="sxs-lookup"><span data-stu-id="6ebba-128">The product lifecycle state has only one control flag: **Is active for planning**.</span></span> <span data-ttu-id="6ebba-129">Sen oletusasetus on **Kyllä** kaikissa luoduissa tuotteen elinkaaren tiloissa, mutta asetukseksi voidaan vaihtaa **Ei**.</span><span class="sxs-lookup"><span data-stu-id="6ebba-129">By default, this is set to **Yes** for all created product lifecycle states, but it can be changed to **No**.</span></span> <span data-ttu-id="6ebba-130">Kun **Ei** on valittu, liitetyt vapautetut tuotteet tai tuotevariantit</span><span class="sxs-lookup"><span data-stu-id="6ebba-130">When set to **No**, the associated released products or released product variants are:</span></span> 

-  <span data-ttu-id="6ebba-131">jätetään pääsuunnittelun ulkopuolelle</span><span class="sxs-lookup"><span data-stu-id="6ebba-131">Excluded from master planning.</span></span> 
-  <span data-ttu-id="6ebba-132">jätetään tuoterakennetason laskennan ulkopuolelle.</span><span class="sxs-lookup"><span data-stu-id="6ebba-132">Excluded from BOM-level calculation.</span></span> 

<span data-ttu-id="6ebba-133">Saat lisätietoja tavoista, joilla tuotteen elinkaaren tilan avulla voidaan jättää tuotteita pääsuunnittelun ja tuoterakennetason laskennan ulkopuolelle, toistamalla tai lukemalla tehtäväoppaan **Tuotteen elinkaaren tason luonti jättämään tuotteita pääsuunnittelun ulkopuolelle**.</span><span class="sxs-lookup"><span data-stu-id="6ebba-133">For detailed information about how to use product lifecycle state to exclude products from master planning and BOM-level calculation, play or read the task guide **Create a product lifecycle state to exclude products from Master planning**.</span></span>

> [!NOTE]
> <span data-ttu-id="6ebba-134">Suorituskyvyn kannalta on suositeltavaa liittää kaikki vanhentuneet vapautetut tuotteet tai tuotevariantit sellaiseen tuotteen elinkaaren tilaan, jossa käyttö pääsuunnittelussa on poistettu käytöstä. Tämä kannattaa erityisesti käsiteltäessä tuotemääritysvariantteja, joita ei voi käyttää uudelleen.</span><span class="sxs-lookup"><span data-stu-id="6ebba-134">For performance reasons, it is highly recommended to associate all obsolete released products or product variants, especially when working with non-reusable product configuration variants, with a product lifecycle state that is deactivated for master planning.</span></span>  
 
## <a name="default-migration-import-and-export"></a><span data-ttu-id="6ebba-135">Oletusarvoinen siirto, tuonti ja vienti</span><span class="sxs-lookup"><span data-stu-id="6ebba-135">Default migration, import, and export</span></span> 

<span data-ttu-id="6ebba-136">Tietoyksiköt eivät tue tuotteen elinkaaren tiloja eikä elinkaaren tilaa voi määrittää muuttuvaksi tilaksi vapautettujen tuotetietoyksiköiden avulla.</span><span class="sxs-lookup"><span data-stu-id="6ebba-136">The product lifecycle states are not supported by data entities, and the lifecycle state cannot be set to a variable state through the released product data entities.</span></span>

-  <span data-ttu-id="6ebba-137">Kaikkien tuotteiden ja tuotevarianttien elinkaaren tila on tyhjä aiemmista versioista siirrettäessä.</span><span class="sxs-lookup"><span data-stu-id="6ebba-137">On migration from previous releases, the lifecycle state of all products and product variants will be blank.</span></span>  
-  <span data-ttu-id="6ebba-138">Kun vapautettuja tuotteita tuodaan tietoyksikön avulla, elinkaaren oletustila otetaan käyttöön luonnin yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="6ebba-138">When importing released products through a data entity, the default lifecycle state will be applied on creation.</span></span>  
-  <span data-ttu-id="6ebba-139">Kun vapautettuja tuotevariantteja tuodaan tietoyksikön avulla, vapautetun päätuotteen elinkaaren tila tuodaan.</span><span class="sxs-lookup"><span data-stu-id="6ebba-139">When importing released product variants through a data entity, the product lifecycle state of the released product master will be imported.</span></span>   
 
## <a name="find-obsolete-products-and-products-variants"></a><span data-ttu-id="6ebba-140">Vanhentuneiden tuotteiden ja tuotevarianttien etsiminen</span><span class="sxs-lookup"><span data-stu-id="6ebba-140">Find obsolete products and products variants</span></span> 
 
<span data-ttu-id="6ebba-141">Voit etsiä vanhentuneita vapautettuja tuotteita ja tuotevariantteja suorittamalla simulointianalyysin ja päivittää sitten niiden tuotteen elinkaaren tilan.</span><span class="sxs-lookup"><span data-stu-id="6ebba-141">You can run a simulation analysis to find the obsolete released products or product variants and then update their product lifecycle status.</span></span> <span data-ttu-id="6ebba-142">Toista ja lue **Vanhentuneiden tuotevarianttien etsiminen ja tuotteen elinkaaren tilan määrittäminen** -tehtäväopas, jos haluat etsiä vanhentuneita tuotteita.</span><span class="sxs-lookup"><span data-stu-id="6ebba-142">To find obsolete products, play and read the task guide **Find obsolete product variants and assign a product lifecycle state**.</span></span> <span data-ttu-id="6ebba-143">Tässä tehtäväoppaassa kerrotaan, miten vanhentuneita julkaistuja tuotteita tai tuotevariantteja etsitään ja miten tuotteen elinkaaren tila liitetään vanhentuneisiin tuotteisiin.</span><span class="sxs-lookup"><span data-stu-id="6ebba-143">This task guide shows how to find obsolete released products or product variants and how to associate a product lifecycle state to the obsolete products.</span></span> <span data-ttu-id="6ebba-144">Siinä kerrotaan myös miten simulointituloksia tarkastellaan ja miten useita tuotteita ja tuotevariantteja liitetään uuteen tuotteen elinkaaren tilaan, kun päivitys suoritetaan ilman simulointia.</span><span class="sxs-lookup"><span data-stu-id="6ebba-144">It also shows hot to view the simulation results and assess how many products and product variants will be associated with a new product lifecycle state when running the update without simulation.</span></span>  
 
<span data-ttu-id="6ebba-145">Kun analyysi suoritetaan simulointitilassa, vanhentuneiksi tunnistetut tuotteet ja tuotevariantit näkyvät erillisessä lomakkeessa, jossa niitä on helppo tarkastella.</span><span class="sxs-lookup"><span data-stu-id="6ebba-145">By running the analysis in a simulation mode, the products and product variants identified as obsolete are displayed in a specific form, where they can easily be reviewed.</span></span> <span data-ttu-id="6ebba-146">Analyysi hakee tapahtumia ja tiettyjä päätietoja, joilla voi tunnistaa tuotteet, joilla ei ole ollut kysyntää muutettavan ajanjakson aikana ja joilla ei ole kysyntänä ilmeneviä päätietoja.</span><span class="sxs-lookup"><span data-stu-id="6ebba-146">The analysis searches for transactions and specific master data to identify products that have no demand within a variable period and no master data that can result in demand.</span></span> <span data-ttu-id="6ebba-147">Analyysin ulkopuolelle voidaan jättää uudet vapautetut tuotteet muutettavan ajanjakson ajalta.</span><span class="sxs-lookup"><span data-stu-id="6ebba-147">New released products within a variable period can be excluded from the analysis.</span></span> <span data-ttu-id="6ebba-148">Kun analyysisimuloinnin tulos on odotettu, käyttäjä voi suorittaa analyysin ja määrittää kaikille analyysin vanhentuneiksi tunnistamille tuotteille uuden tuotteen elinkaaren tilan.</span><span class="sxs-lookup"><span data-stu-id="6ebba-148">When the analysis simulation returns the expected result, the user can run the analysis and set a new product lifecycle state to all products identified as obsolete by the analysis.</span></span>  
 
> [!NOTE]
> <span data-ttu-id="6ebba-149">Huomaa, että analyysi ja päivitykset on tehtävä samassa yrityksessä.</span><span class="sxs-lookup"><span data-stu-id="6ebba-149">Note that all analysis and updates must be done within the same legal entity.</span></span>  
 
## <a name="criteria-to-select-and-update-released-products-or-product-variants"></a><span data-ttu-id="6ebba-150">Vapautettujen tuotteiden ja tuotevarianttien valinta- ja päivitysehdot</span><span class="sxs-lookup"><span data-stu-id="6ebba-150">Criteria to select and update released products or product variants</span></span> 
 
<span data-ttu-id="6ebba-151">Valitse ja päivitä vapautetut tuotteet ja tuotevariantit seuraavien ehtojen mukaisesti:</span><span class="sxs-lookup"><span data-stu-id="6ebba-151">Use the following criteria to select and update the released products and product variants:</span></span> 

-    <span data-ttu-id="6ebba-152">Tuotteen tai tuotevariantin tuotteen elinkaaren tila ei saa olla sama kuin uusi toivottu tila.</span><span class="sxs-lookup"><span data-stu-id="6ebba-152">The product lifecycle state of the product or product variant must be different from the new desired state.</span></span> 
-  <span data-ttu-id="6ebba-153">Tuote tai tuotevariantti luotiin muutamia päiviä aiemmin; päivien määrä perustuu valintaikkunassa annettuun arvoon.</span><span class="sxs-lookup"><span data-stu-id="6ebba-153">The product or product variant was created some days ago based on the number of days that you enter in the selection dialog box.</span></span> 
-  <span data-ttu-id="6ebba-154">Tuotteella tai tuotevariantilla ei ole avoimia tuotantotilauksia (= tila < päättynyt).</span><span class="sxs-lookup"><span data-stu-id="6ebba-154">There are no open production orders (= status < ended) for the product or product variant.</span></span> 
-  <span data-ttu-id="6ebba-155">Tuotteella tai tuotevariantilla ei ole avoimia varastotapahtumia (= tila varasto-otto ReservPhysical–QuotationIssue tai tila vastaanotto Registrered–QuotationReceipt).</span><span class="sxs-lookup"><span data-stu-id="6ebba-155">There are no open inventory transactions (= status issue ReservPhysical to QuotationIssue or status receipt Registrered to QuotationReceipt) for the product or product variant.</span></span> 
-  <span data-ttu-id="6ebba-156">Tuotteella tai tuotevariantilla ei ole varastotapahtumia tiettyjen päivien aikana.</span><span class="sxs-lookup"><span data-stu-id="6ebba-156">There are no inventory transactions within the last number of days for the product or product variant.</span></span> 
-  <span data-ttu-id="6ebba-157">Tuotteella tai tuotevariantilla ei ole tulevaa kysyntää tai tarjontaennustetta.</span><span class="sxs-lookup"><span data-stu-id="6ebba-157">There is no future demand or supply forecast for the product or product variant.</span></span>  
-  <span data-ttu-id="6ebba-158">Tuotteelle tai tuotevariantille ei ole määritetty minimivarastotasoa nimikkeen kattavuudessa.</span><span class="sxs-lookup"><span data-stu-id="6ebba-158">No minimum stock level has been set in item coverage for the product or product variant.</span></span> 
-  <span data-ttu-id="6ebba-159">Tuotteella tai tuotevariantilla ei ole aktiivista kiinteämääräistä kanban-sääntöä.</span><span class="sxs-lookup"><span data-stu-id="6ebba-159">No active fixed quantity kanban rule for the product or product variant.</span></span>  
-  <span data-ttu-id="6ebba-160">Tuotteella tai tuotevariantilla ei ole huoltotilausriviä.</span><span class="sxs-lookup"><span data-stu-id="6ebba-160">No service order line for the product or product variant.</span></span> 
-  <span data-ttu-id="6ebba-161">Tuotteella tai tuotevariantilla ei ole aktiivisia tai tulevia myynti- tai ostosopimusrivejä.</span><span class="sxs-lookup"><span data-stu-id="6ebba-161">No active or future sales or purchase agreement lines for the product or product variant.</span></span> 
-  <span data-ttu-id="6ebba-162">Tuotetta tai tuotevarianttia ei käytetä sellaisessa tuoterakenteessa, joka on liitetty ei-vanhentuneeseen hyväksyttyyn suunnittelussa käytettävissä olevaan tuotteen tai variantin tuoterakenneversioon.</span><span class="sxs-lookup"><span data-stu-id="6ebba-162">The product or product variant is not used in a BOM that is associated with a non-expired approved BOM version for a product or variant that is active for planning.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6ebba-163">Liittyvät aiheet</span><span class="sxs-lookup"><span data-stu-id="6ebba-163">Related topics</span></span>

-  <span data-ttu-id="6ebba-164">Uuden tuotteen elinkaaren tilan luominen</span><span class="sxs-lookup"><span data-stu-id="6ebba-164">Create a new product lifecycle state</span></span>
-  <span data-ttu-id="6ebba-165">Uuden tuotteen elinkaaren oletustilan luominen</span><span class="sxs-lookup"><span data-stu-id="6ebba-165">Create a default new product lifecycle state</span></span>
-  <span data-ttu-id="6ebba-166">Tuotteen elinkaaren tilan liittäminen vapautettuun päätuotteeseen</span><span class="sxs-lookup"><span data-stu-id="6ebba-166">Assign a product lifecycle state to a released product master</span></span>
-  <span data-ttu-id="6ebba-167">Tuotteen elinkaaren tilan liittäminen vapautettuun tuotteeseen</span><span class="sxs-lookup"><span data-stu-id="6ebba-167">Assign a product lifecycle state to a released product</span></span>
-  <span data-ttu-id="6ebba-168">Vanhentuneiden tuotevarianttien etsiminen ja tuotteen elinkaaren tilan liittäminen</span><span class="sxs-lookup"><span data-stu-id="6ebba-168">Find obsolete product variants and assign a product lifecycle state</span></span>
-  <span data-ttu-id="6ebba-169">Tuotteen elinkaaren tason luonti jättämään tuotteita pääsuunnittelun ulkopuolelle</span><span class="sxs-lookup"><span data-stu-id="6ebba-169">Create a product lifecycle state to exclude products from Master planning</span></span>

