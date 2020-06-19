---
title: Linkkipolkumoduuli
description: Tässä ohjeaiheessa on tietoja linkkipolkumoduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.
author: anupamar-ms
manager: annbe
ms.date: 06/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 1c6d846686e3214e976a55271694382d7c5973ed
ms.sourcegitcommit: 2683aacb426bfb3b541637edf1f8ec2d6cb5a745
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/01/2020
ms.locfileid: "3417389"
---
# <a name="breadcrumb-module"></a><span data-ttu-id="6dfc5-103">Linkkipolkumoduuli</span><span class="sxs-lookup"><span data-stu-id="6dfc5-103">Breadcrumb module</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="6dfc5-104">Tässä ohjeaiheessa on tietoja linkkipolkumoduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.</span><span class="sxs-lookup"><span data-stu-id="6dfc5-104">This topic covers breadcrumb modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="6dfc5-105">Yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="6dfc5-105">Overview</span></span>

<span data-ttu-id="6dfc5-106">Linkkipolkua käytetään sivuston sivujen toissijaiseen navigointiin.</span><span class="sxs-lookup"><span data-stu-id="6dfc5-106">Breadcrumb modules are used to provide secondary navigation on site pages.</span></span> <span data-ttu-id="6dfc5-107">Ne näkyvät yleensä sivun yläosassa otsikon alapuolella.</span><span class="sxs-lookup"><span data-stu-id="6dfc5-107">They are typically shown at the top of a page, below the header.</span></span> <span data-ttu-id="6dfc5-108">Vaikka linkkipolkumoduulit voidaan lisätä mille tahansa sivulle, niitä käytetään useimmiten tuotetietosivuilla (PDP:t), jotka näyttävät tuoteluokkahierarkian ja tarjoavat nopean tavan liikkua sivustossa.</span><span class="sxs-lookup"><span data-stu-id="6dfc5-108">Although breadcrumb modules can be added to any page, they are most often used on product details pages (PDPs), to show the product category hierarchy and provide a quick way to move around a site.</span></span> <span data-ttu-id="6dfc5-109">Linkkipolkua käyttämällä voidaan myös näyttää takaisin tuloksiin -linkki, kun käyttäjät avaavat PDP:n haku- tai luettelosivulta.</span><span class="sxs-lookup"><span data-stu-id="6dfc5-109">A breadcrumb module can also be used to show a "Back to results" link when users open a PDP from a search or list page.</span></span> <span data-ttu-id="6dfc5-110">Tällä tavoin käyttäjät voivat palata nopeasti suodatettuun luettelosivuun ja jatkaa ostosten tekemistä.</span><span class="sxs-lookup"><span data-stu-id="6dfc5-110">In this way, users can quickly return to their filtered list page to continue shopping.</span></span>

<span data-ttu-id="6dfc5-111">Sivuilla, joilla on tuoteluokkakonteksti, kuten PDP:t ja luokkasivut, linkkipolkumoduulit näyttävät luokkahierarkian.</span><span class="sxs-lookup"><span data-stu-id="6dfc5-111">On pages that have product category context, such as PDPs and category pages, breadcrumb modules show the category hierarchy.</span></span> <span data-ttu-id="6dfc5-112">Sivuilla, joilla ei ole luokkakontekstia, linkkipolkumoduulit näyttävät **&lt;sivuston juuri&gt; / &lt;nykyinen sivu&gt;** oletusarvon mukaan.</span><span class="sxs-lookup"><span data-stu-id="6dfc5-112">On pages that don't have category context, breadcrumb modules show **&lt;Site root&gt; / &lt;Current page&gt;** by default.</span></span> <span data-ttu-id="6dfc5-113">Linkkipolkumoduulit voidaan määrittää myös manuaalisesti muun tyyppisillä sivuston sivuilla, jotka näyttävät linkit sivuston tietyille sivuille.</span><span class="sxs-lookup"><span data-stu-id="6dfc5-113">Breadcrumb modules can also be manually configured on other types of site pages to show links to specific pages on the site.</span></span>

<span data-ttu-id="6dfc5-114">Seuraavassa kuvassa on esimerkki linkkipolkumoduulista, jossa näkyy PDP:n luokkahierarkia.</span><span class="sxs-lookup"><span data-stu-id="6dfc5-114">The following image shows an example of a breadcrumb module that shows the category hierarchy on a PDP.</span></span>

![Esimerkki linkkipolkumoduulista](./media/ecommerce-breadcrumb.PNG)

## <a name="breadcrumb-module-settings"></a><span data-ttu-id="6dfc5-116">Linkkipolkumoduulin asetukset</span><span class="sxs-lookup"><span data-stu-id="6dfc5-116">Breadcrumb module settings</span></span>

<span data-ttu-id="6dfc5-117">Linkkipolkumoduuli käyttää **linkkipolun näyttötyyppiä PDP**-asetuksessa, joka määritetään kohdassa **Sivuston asetukset \> Laajennukset** sivustomuodostustyökalussa.</span><span class="sxs-lookup"><span data-stu-id="6dfc5-117">The breadcrumb module relies on the **Breadcrumb display type on PDP** setting, which is defined at **Site Settings \> Extensions** in site builder.</span></span> <span data-ttu-id="6dfc5-118">Tällä asetuksella on kolme mahdollista arvoa:</span><span class="sxs-lookup"><span data-stu-id="6dfc5-118">This setting has three possible values:</span></span>

- <span data-ttu-id="6dfc5-119">**Näytä luokkahierarkia** – Kun tämä arvo on valittuna, linkkipolkumoduulissa näkyy PDP:n tarkasteltavissa olevan tuotteen koko luokkahierarkia.</span><span class="sxs-lookup"><span data-stu-id="6dfc5-119">**Show category hierarchy** – When this value is selected, the breadcrumb module will show the full category hierarchy of the product that is viewed on the PDP.</span></span>
- <span data-ttu-id="6dfc5-120">**Näytä takaisin tuloksiin** – Kun tämä arvo on valittu, linkkipolkumoduulissa näkyy PDP:n takaisin tuloksiin -linkki, jos käyttäjä avaa PDP:n moduulista, joka sallii takaisin tuloksiin -linkin.</span><span class="sxs-lookup"><span data-stu-id="6dfc5-120">**Show back to results** – When this value is selected, the breadcrumb module will show a "Back to results" link on a PDP if the user opened the PDP from a module that allows for a "Back to results" link.</span></span> <span data-ttu-id="6dfc5-121">Tämä toiminto on käytettävissä, kun käyttäjät siirtyvät luokka-, haku-, luettelo- ja suositusluettelot -sivuista.</span><span class="sxs-lookup"><span data-stu-id="6dfc5-121">This functionality is available when users navigate from category, search, list, and recommendation lists pages.</span></span> <span data-ttu-id="6dfc5-122">Tämän toiminnon tukemiseksi tuotekokoelma- ja hakutulosmoduuleissa on ominaisuus, jonka nimi on **Salli takaisin PDP:n tuloksiin**.</span><span class="sxs-lookup"><span data-stu-id="6dfc5-122">To support this functionality, product collection and search results modules have a property that is named **Allow back to results on PDP**.</span></span> <span data-ttu-id="6dfc5-123">Tämän ominaisuuden avulla voit joustavasti määrittää, mitkä moduulit tukevat takaisin tuloksiin -linkkitoimintoa PDP:n yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="6dfc5-123">This property gives you the flexibility to define which modules should support the "Back to results" link functionality on the PDP.</span></span> <span data-ttu-id="6dfc5-124">Jos esimerkiksi **Näytä takaisin tuloksiin** -asetus on valittuna **linkkipolkunäyttötyyppi PDP:ssä** -linkkipolkumoduulille, ja **Salli takaisin tulokset PDP:ssä** valitaan hakusivun hakutulokset-moduulille, näkyviin tulee takaisin tuloksiin -linkki, kun käyttäjät siirtyvät hakusivulta PDP:n kautta.</span><span class="sxs-lookup"><span data-stu-id="6dfc5-124">For example, when **Show back to results** is selected for the **Breadcrumb display type on PDP** setting of the breadcrumb module, and **Allow back to results on PDP** is selected for the search page search results module, a "Back to results" link will be shown when users navigate from the search page to a PDP.</span></span>
- <span data-ttu-id="6dfc5-125">**Näytä luokkahierarkia ja takaisin tuloksiin** – Tämä arvo on kahden edellisen yhdistelmä.</span><span class="sxs-lookup"><span data-stu-id="6dfc5-125">**Show category hierarchy and back to results** – This value is a combination of the previous two.</span></span> <span data-ttu-id="6dfc5-126">Kun tämä arvo on valittu, linkkipolkumoduuli näyttää sekä koko luokkahierarkian että Takaisin tuloksiin -linkin (jos se on määritetty) PDP:n yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="6dfc5-126">When this value is selected, the breadcrumb module will show both the full category hierarchy and a "Back to results" link (if it's configured) on a PDP.</span></span>

## <a name="breadcrumb-module-properties"></a><span data-ttu-id="6dfc5-127">Navigointipolkumoduulin ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="6dfc5-127">Breadcrumb module properties</span></span>

| <span data-ttu-id="6dfc5-128">Ominaisuuden nimi</span><span class="sxs-lookup"><span data-stu-id="6dfc5-128">Property name</span></span> | <span data-ttu-id="6dfc5-129">Arvot</span><span class="sxs-lookup"><span data-stu-id="6dfc5-129">Values</span></span> | <span data-ttu-id="6dfc5-130">kuvaus</span><span class="sxs-lookup"><span data-stu-id="6dfc5-130">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="6dfc5-131">Juuri</span><span class="sxs-lookup"><span data-stu-id="6dfc5-131">Root</span></span> | <span data-ttu-id="6dfc5-132">Teksti tai linkki</span><span class="sxs-lookup"><span data-stu-id="6dfc5-132">Text or link</span></span>| <span data-ttu-id="6dfc5-133">Tämä valinnainen ominaisuus määrittää linkkitekstin ja linkin kohteen polkua varten.</span><span class="sxs-lookup"><span data-stu-id="6dfc5-133">This optional property specifies link text and a link target for the breadcrumb site root.</span></span> <span data-ttu-id="6dfc5-134">Jos tätä ominaisuutta ei ole määritetty, pääkansiota ei määritetä.</span><span class="sxs-lookup"><span data-stu-id="6dfc5-134">If this property isn't configured, no root will be defined.</span></span> |
| <span data-ttu-id="6dfc5-135">Linkkipolkulinkki</span><span class="sxs-lookup"><span data-stu-id="6dfc5-135">Breadcrumb link</span></span> | <span data-ttu-id="6dfc5-136">Linkitä</span><span class="sxs-lookup"><span data-stu-id="6dfc5-136">Link</span></span> | <span data-ttu-id="6dfc5-137">Tämä valinnainen ominaisuus määrittää manuaalisesti määritetyn polun linkit, jos linkit ovat pakollisia.</span><span class="sxs-lookup"><span data-stu-id="6dfc5-137">This optional property specifies links for a manually configured breadcrumb, if these links are required.</span></span> <span data-ttu-id="6dfc5-138">Linkit näkyvät siinä järjestyksessä, jossa ne ovat luettelossa.</span><span class="sxs-lookup"><span data-stu-id="6dfc5-138">Links appear in the order that they are listed in.</span></span> |

## <a name="add-a-breadcrumb-module-to-a-new-page"></a><span data-ttu-id="6dfc5-139">Linkkipolkumoduulin lisääminen uudelle sivulle</span><span class="sxs-lookup"><span data-stu-id="6dfc5-139">Add a breadcrumb module to a new page</span></span>

<span data-ttu-id="6dfc5-140">Voit lisätä linkkipolkumoduulin PDP:hen ja määrittää pakolliset ominaisuudet seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="6dfc5-140">To add a breadcrumb module to a PDP and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="6dfc5-141">Siirry kohtaan **Sivuston asetukset /> Laajennukset** ja valitse sitten **Linkkipolun näyttötyyppi PDP**-asetuksessa **Näytä luokkahierarkia**.</span><span class="sxs-lookup"><span data-stu-id="6dfc5-141">Go to **Site Settings /> Extensions**, and then, for the **Breadcrumb display type on PDP** setting, select **Show category hierarchy**.</span></span>
1. <span data-ttu-id="6dfc5-142">Siirry kohtaan **Mallit** ja valitse PDP-malli.</span><span class="sxs-lookup"><span data-stu-id="6dfc5-142">Go to **Templates**, and select the PDP template.</span></span>
1. <span data-ttu-id="6dfc5-143">Valitse **Kontti**-paikka, joka sisältää ostoruutumoduulin. Valitse kolmen pisteen painike (**...**) ja valitse sitten **Lisää moduuli**.</span><span class="sxs-lookup"><span data-stu-id="6dfc5-143">In the **Container** slot that contains the buy box module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="6dfc5-144">Valitse **Lisää moduuli** -valintaikkunassa **Linkkipolku**-moduuli ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="6dfc5-144">In the **Add Module** dialog box, select the **Breadcrumb** module, and then select **OK**.</span></span>
1. <span data-ttu-id="6dfc5-145">Valitse **Tallenna**, valitse **Viimeistele muokkaus** tarkistaaksesi mallin, ja julkaise se valitsemalla **Julkaise**.</span><span class="sxs-lookup"><span data-stu-id="6dfc5-145">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="6dfc5-146">Siirry kohtaan **Sivut** ja avaa PDP, joka käyttää PDP-mallia.</span><span class="sxs-lookup"><span data-stu-id="6dfc5-146">Go to **Pages**, and open a PDP that uses the PDP template.</span></span> <span data-ttu-id="6dfc5-147">Jos PDP:tä ei vielä ole olemassa, luo sellainen.</span><span class="sxs-lookup"><span data-stu-id="6dfc5-147">If a PDP doesn't yet exist, create one.</span></span>
1. <span data-ttu-id="6dfc5-148">Valitse **Kontti**-paikka, joka sisältää ostoruutumoduulin. Valitse kolmen pisteen painike (**...**) ja valitse sitten **Lisää moduuli**.</span><span class="sxs-lookup"><span data-stu-id="6dfc5-148">In the **Container** slot that contains the buy box module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="6dfc5-149">Valitse **Lisää moduuli** -valintaikkunassa **Linkkipolku**-moduuli ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="6dfc5-149">In the **Add Module** dialog box, select the **Breadcrumb** module, and then select **OK**.</span></span>
1. <span data-ttu-id="6dfc5-150">Valitse **Linkkipolku**-paikan ominaisuudet-ruudun **Pääkansio**-kohdasta **Linkitä teksti**.</span><span class="sxs-lookup"><span data-stu-id="6dfc5-150">In the properties pane of the **Breadcrumb** slot, under **Root**, select **Link text**.</span></span>
1. <span data-ttu-id="6dfc5-151">Kirjoita **Linkin teksti** -valintaikkunaan **Koti** ja valitse sitten **Linkin kohde** -kohdasta **Lisää linkki**.</span><span class="sxs-lookup"><span data-stu-id="6dfc5-151">In the **Link text** dialog box, enter **Home**, and then, under **Link target**, select **Add a link**.</span></span>
1. <span data-ttu-id="6dfc5-152">Valitse **Lisää linkki** -valintaikkunassa linkkipolkupääkansion linkki ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="6dfc5-152">In the **Add a link** dialog box, select a link for the breadcrumb root, and then select **OK**.</span></span>
1. <span data-ttu-id="6dfc5-153">Valitse **Tallenna**ja esikatsele sitten sivua valitsemalla **Esikatselu**.</span><span class="sxs-lookup"><span data-stu-id="6dfc5-153">Select **Save**, and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="6dfc5-154">Valitse **Lopeta muokkaus** tallentaaksesi mallin ja valitse sitten **Julkaise** julkaistaksesi sen.</span><span class="sxs-lookup"><span data-stu-id="6dfc5-154">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6dfc5-155">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="6dfc5-155">Additional resources</span></span>

[<span data-ttu-id="6dfc5-156">Aloituspakkauksen yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="6dfc5-156">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="6dfc5-157">Luokan oletussaapumis- ja oletushakutulossivun yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="6dfc5-157">Overview of default category landing page and search results page</span></span>](category-search-page-overview.md)

[<span data-ttu-id="6dfc5-158">Tuotekokoelmamoduulit</span><span class="sxs-lookup"><span data-stu-id="6dfc5-158">Product collection modules</span></span>](product-collection-module-overview.md)

[<span data-ttu-id="6dfc5-159">Ostoruutumoduuli</span><span class="sxs-lookup"><span data-stu-id="6dfc5-159">Buy box module</span></span>](add-buy-box.md)
