---
title: Linkkipolkumoduuli
description: Tässä ohjeaiheessa on tietoja navigointipolkumoduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.
author: anupamar-ms
ms.date: 10/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: e7b7cff280d8c6bcb09f2f59d96ec415b9cc1167
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5796195"
---
# <a name="breadcrumb-module"></a><span data-ttu-id="e8524-103">Navigointipolkumoduuli</span><span class="sxs-lookup"><span data-stu-id="e8524-103">Breadcrumb module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e8524-104">Tässä ohjeaiheessa on tietoja navigointipolkumoduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.</span><span class="sxs-lookup"><span data-stu-id="e8524-104">This topic covers breadcrumb modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="e8524-105">Linkkipolkua käytetään sivuston sivujen toissijaiseen navigointiin.</span><span class="sxs-lookup"><span data-stu-id="e8524-105">Breadcrumb modules are used to provide secondary navigation on site pages.</span></span> <span data-ttu-id="e8524-106">Ne näkyvät yleensä sivun yläosassa otsikon alapuolella.</span><span class="sxs-lookup"><span data-stu-id="e8524-106">They are typically shown at the top of a page, below the header.</span></span> <span data-ttu-id="e8524-107">Vaikka linkkipolkumoduulit voidaan lisätä mille tahansa sivulle, niitä käytetään useimmiten tuotetietosivuilla (PDP:t), jotka näyttävät tuoteluokkahierarkian ja tarjoavat nopean tavan liikkua sivustossa.</span><span class="sxs-lookup"><span data-stu-id="e8524-107">Although breadcrumb modules can be added to any page, they are most often used on product details pages (PDPs), to show the product category hierarchy and provide a quick way to move around a site.</span></span> <span data-ttu-id="e8524-108">Linkkipolkua käyttämällä voidaan myös näyttää takaisin tuloksiin -linkki, kun käyttäjät avaavat PDP:n haku- tai luettelosivulta.</span><span class="sxs-lookup"><span data-stu-id="e8524-108">A breadcrumb module can also be used to show a "Back to results" link when users open a PDP from a search or list page.</span></span> <span data-ttu-id="e8524-109">Tällä tavoin käyttäjät voivat palata nopeasti suodatettuun luettelosivuun ja jatkaa ostosten tekemistä.</span><span class="sxs-lookup"><span data-stu-id="e8524-109">In this way, users can quickly return to their filtered list page to continue shopping.</span></span>

<span data-ttu-id="e8524-110">Sivuilla, joilla on tuoteluokkakonteksti, kuten PDP:t ja luokkasivut, linkkipolkumoduulit näyttävät luokkahierarkian.</span><span class="sxs-lookup"><span data-stu-id="e8524-110">On pages that have product category context, such as PDPs and category pages, breadcrumb modules show the category hierarchy.</span></span> <span data-ttu-id="e8524-111">Sivuilla, joilla ei ole luokkakontekstia, linkkipolkumoduulit näyttävät **&lt;sivuston juuri&gt; / &lt;nykyinen sivu&gt;** oletusarvon mukaan.</span><span class="sxs-lookup"><span data-stu-id="e8524-111">On pages that don't have category context, breadcrumb modules show **&lt;Site root&gt; / &lt;Current page&gt;** by default.</span></span> <span data-ttu-id="e8524-112">Linkkipolkumoduulit voidaan määrittää myös manuaalisesti muun tyyppisillä sivuston sivuilla, jotka näyttävät linkit sivuston tietyille sivuille.</span><span class="sxs-lookup"><span data-stu-id="e8524-112">Breadcrumb modules can also be manually configured on other types of site pages to show links to specific pages on the site.</span></span>

> [!NOTE]
> <span data-ttu-id="e8524-113">Linkkipolkumoduuli on käytettävissä Dynamics 365 Commercen versiossa 10.0.12.</span><span class="sxs-lookup"><span data-stu-id="e8524-113">The breadcrumb module is available in the Dynamics 365 Commerce 10.0.12 release.</span></span>

<span data-ttu-id="e8524-114">Seuraavassa kuvassa on esimerkki linkkipolkumoduulista, jossa näkyy PDP:n luokkahierarkia.</span><span class="sxs-lookup"><span data-stu-id="e8524-114">The following image shows an example of a breadcrumb module that shows the category hierarchy on a PDP.</span></span>

![Esimerkki linkkipolkumoduulista](./media/ecommerce-breadcrumb.PNG)

## <a name="breadcrumb-module-settings"></a><span data-ttu-id="e8524-116">Linkkipolkumoduulin asetukset</span><span class="sxs-lookup"><span data-stu-id="e8524-116">Breadcrumb module settings</span></span>

<span data-ttu-id="e8524-117">Linkkipolkumoduuli käyttää **linkkipolun näyttötyyppiä PDP**-asetuksessa, joka määritetään kohdassa **Sivuston asetukset \> Laajennukset** sivustomuodostustyökalussa.</span><span class="sxs-lookup"><span data-stu-id="e8524-117">The breadcrumb module relies on the **Breadcrumb display type on PDP** setting, which is defined at **Site Settings \> Extensions** in site builder.</span></span> <span data-ttu-id="e8524-118">Tällä asetuksella on kolme mahdollista arvoa:</span><span class="sxs-lookup"><span data-stu-id="e8524-118">This setting has three possible values:</span></span>

- <span data-ttu-id="e8524-119">**Näytä luokkahierarkia** – Kun tämä arvo on valittuna, linkkipolkumoduulissa näkyy PDP:n tarkasteltavissa olevan tuotteen koko luokkahierarkia.</span><span class="sxs-lookup"><span data-stu-id="e8524-119">**Show category hierarchy** – When this value is selected, the breadcrumb module will show the full category hierarchy of the product that is viewed on the PDP.</span></span>
- <span data-ttu-id="e8524-120">**Näytä takaisin tuloksiin** – Kun tämä arvo on valittu, linkkipolkumoduulissa näkyy PDP:n takaisin tuloksiin -linkki, jos käyttäjä avaa PDP:n moduulista, joka sallii takaisin tuloksiin -linkin.</span><span class="sxs-lookup"><span data-stu-id="e8524-120">**Show back to results** – When this value is selected, the breadcrumb module will show a "Back to results" link on a PDP if the user opened the PDP from a module that allows for a "Back to results" link.</span></span> <span data-ttu-id="e8524-121">Tämä toiminto on käytettävissä, kun käyttäjät siirtyvät luokka-, haku-, luettelo- ja suositusluettelot -sivuista.</span><span class="sxs-lookup"><span data-stu-id="e8524-121">This functionality is available when users navigate from category, search, list, and recommendation lists pages.</span></span> <span data-ttu-id="e8524-122">Tämän toiminnon tukemiseksi tuotekokoelma- ja hakutulosmoduuleissa on ominaisuus, jonka nimi on **Salli takaisin PDP:n tuloksiin**.</span><span class="sxs-lookup"><span data-stu-id="e8524-122">To support this functionality, product collection and search results modules have a property that is named **Allow back to results on PDP**.</span></span> <span data-ttu-id="e8524-123">Tämän ominaisuuden avulla voit joustavasti määrittää, mitkä moduulit tukevat takaisin tuloksiin -linkkitoimintoa PDP:n yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="e8524-123">This property gives you the flexibility to define which modules should support the "Back to results" link functionality on the PDP.</span></span> <span data-ttu-id="e8524-124">Jos esimerkiksi **Näytä takaisin tuloksiin** -asetus on valittuna **linkkipolkunäyttötyyppi PDP:ssä** -linkkipolkumoduulille, ja **Salli takaisin tulokset PDP:ssä** valitaan hakusivun hakutulokset-moduulille, näkyviin tulee takaisin tuloksiin -linkki, kun käyttäjät siirtyvät hakusivulta PDP:n kautta.</span><span class="sxs-lookup"><span data-stu-id="e8524-124">For example, when **Show back to results** is selected for the **Breadcrumb display type on PDP** setting of the breadcrumb module, and **Allow back to results on PDP** is selected for the search page search results module, a "Back to results" link will be shown when users navigate from the search page to a PDP.</span></span>
- <span data-ttu-id="e8524-125">**Näytä luokkahierarkia ja takaisin tuloksiin** – Tämä arvo on kahden edellisen yhdistelmä.</span><span class="sxs-lookup"><span data-stu-id="e8524-125">**Show category hierarchy and back to results** – This value is a combination of the previous two.</span></span> <span data-ttu-id="e8524-126">Kun tämä arvo on valittu, linkkipolkumoduuli näyttää sekä koko luokkahierarkian että Takaisin tuloksiin -linkin (jos se on määritetty) PDP:n yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="e8524-126">When this value is selected, the breadcrumb module will show both the full category hierarchy and a "Back to results" link (if it's configured) on a PDP.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e8524-127">Nämä asetukset ovat käytettävissä Dynamics 365 Commercen versiossa 10.0.12.</span><span class="sxs-lookup"><span data-stu-id="e8524-127">These settings are available in the Dynamics 365 Commerce 10.0.12 release.</span></span> <span data-ttu-id="e8524-128">Jos päivität vanhemmasta Dynamics 365 Commerce -versiosta, sinun on päivitettävä appsettings.json-tiedosto manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="e8524-128">If you are updating from an older version of Dynamics 365 Commerce, you must manually update the appsettings.json file.</span></span> <span data-ttu-id="e8524-129">Ohjeet appsettings.json-tiedoston päivittämiseen: [SDK:n ja moduuliskirjaston päivitykset](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span><span class="sxs-lookup"><span data-stu-id="e8524-129">For instructions on updating the appsettings.json file, see [SDK and module library updates](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span></span>

## <a name="breadcrumb-module-properties"></a><span data-ttu-id="e8524-130">Navigointipolkumoduulin ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="e8524-130">Breadcrumb module properties</span></span>

| <span data-ttu-id="e8524-131">Ominaisuuden nimi</span><span class="sxs-lookup"><span data-stu-id="e8524-131">Property name</span></span> | <span data-ttu-id="e8524-132">Arvot</span><span class="sxs-lookup"><span data-stu-id="e8524-132">Values</span></span> | <span data-ttu-id="e8524-133">kuvaus</span><span class="sxs-lookup"><span data-stu-id="e8524-133">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="e8524-134">Juuri</span><span class="sxs-lookup"><span data-stu-id="e8524-134">Root</span></span> | <span data-ttu-id="e8524-135">Teksti tai linkki</span><span class="sxs-lookup"><span data-stu-id="e8524-135">Text or link</span></span>| <span data-ttu-id="e8524-136">Tämä valinnainen ominaisuus määrittää linkkitekstin ja linkin kohteen polkua varten.</span><span class="sxs-lookup"><span data-stu-id="e8524-136">This optional property specifies link text and a link target for the breadcrumb site root.</span></span> <span data-ttu-id="e8524-137">Jos tätä ominaisuutta ei ole määritetty, pääkansiota ei määritetä.</span><span class="sxs-lookup"><span data-stu-id="e8524-137">If this property isn't configured, no root will be defined.</span></span> |
| <span data-ttu-id="e8524-138">Linkkipolkulinkki</span><span class="sxs-lookup"><span data-stu-id="e8524-138">Breadcrumb link</span></span> | <span data-ttu-id="e8524-139">Linkitä</span><span class="sxs-lookup"><span data-stu-id="e8524-139">Link</span></span> | <span data-ttu-id="e8524-140">Tämä valinnainen ominaisuus määrittää manuaalisesti määritetyn polun linkit, jos linkit ovat pakollisia.</span><span class="sxs-lookup"><span data-stu-id="e8524-140">This optional property specifies links for a manually configured breadcrumb, if these links are required.</span></span> <span data-ttu-id="e8524-141">Linkit näkyvät siinä järjestyksessä, jossa ne ovat luettelossa.</span><span class="sxs-lookup"><span data-stu-id="e8524-141">Links appear in the order that they are listed in.</span></span> |

## <a name="add-a-breadcrumb-module-to-a-new-page"></a><span data-ttu-id="e8524-142">Linkkipolkumoduulin lisääminen uudelle sivulle</span><span class="sxs-lookup"><span data-stu-id="e8524-142">Add a breadcrumb module to a new page</span></span>

<span data-ttu-id="e8524-143">Voit lisätä linkkipolkumoduulin PDP:hen ja määrittää pakolliset ominaisuudet seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="e8524-143">To add a breadcrumb module to a PDP and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="e8524-144">Siirry kohtaan **Sivuston asetukset \> Laajennukset** ja valitse sitten **Linkkipolun näyttötyyppi PDP** -asetuksessa **Näytä luokkahierarkia**.</span><span class="sxs-lookup"><span data-stu-id="e8524-144">Go to **Site Settings \> Extensions**, and then, for the **Breadcrumb display type on PDP** setting, select **Show category hierarchy**.</span></span>
1. <span data-ttu-id="e8524-145">Siirry kohtaan **Mallit** ja valitse PDP-malli.</span><span class="sxs-lookup"><span data-stu-id="e8524-145">Go to **Templates**, and select the PDP template.</span></span>
1. <span data-ttu-id="e8524-146">Valitse **Kontti**-paikka, joka sisältää ostoruutumoduulin. Valitse kolmen pisteen painike (**...**) ja valitse sitten **Lisää moduuli**.</span><span class="sxs-lookup"><span data-stu-id="e8524-146">In the **Container** slot that contains the buy box module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="e8524-147">Valitse **Lisää moduuli** -valintaikkunassa **Linkkipolku**-moduuli ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="e8524-147">In the **Add Module** dialog box, select the **Breadcrumb** module, and then select **OK**.</span></span>
1. <span data-ttu-id="e8524-148">Valitse **Tallenna**, valitse **Viimeistele muokkaus** tarkistaaksesi mallin, ja julkaise se valitsemalla **Julkaise**.</span><span class="sxs-lookup"><span data-stu-id="e8524-148">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="e8524-149">Siirry kohtaan **Sivut** ja avaa PDP, joka käyttää PDP-mallia.</span><span class="sxs-lookup"><span data-stu-id="e8524-149">Go to **Pages**, and open a PDP that uses the PDP template.</span></span> <span data-ttu-id="e8524-150">Jos PDP:tä ei vielä ole olemassa, luo sellainen.</span><span class="sxs-lookup"><span data-stu-id="e8524-150">If a PDP doesn't yet exist, create one.</span></span>
1. <span data-ttu-id="e8524-151">Valitse **Kontti**-paikka, joka sisältää ostoruutumoduulin. Valitse kolmen pisteen painike (**...**) ja valitse sitten **Lisää moduuli**.</span><span class="sxs-lookup"><span data-stu-id="e8524-151">In the **Container** slot that contains the buy box module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="e8524-152">Valitse **Lisää moduuli** -valintaikkunassa **Linkkipolku**-moduuli ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="e8524-152">In the **Add Module** dialog box, select the **Breadcrumb** module, and then select **OK**.</span></span>
1. <span data-ttu-id="e8524-153">Valitse **Linkkipolku**-paikan ominaisuudet-ruudun **Pääkansio**-kohdasta **Linkitä teksti**.</span><span class="sxs-lookup"><span data-stu-id="e8524-153">In the properties pane of the **Breadcrumb** slot, under **Root**, select **Link text**.</span></span>
1. <span data-ttu-id="e8524-154">Kirjoita **Linkin teksti** -valintaikkunaan **Koti** ja valitse sitten **Linkin kohde** -kohdasta **Lisää linkki**.</span><span class="sxs-lookup"><span data-stu-id="e8524-154">In the **Link text** dialog box, enter **Home**, and then, under **Link target**, select **Add a link**.</span></span>
1. <span data-ttu-id="e8524-155">Valitse **Lisää linkki** -valintaikkunassa linkkipolkupääkansion linkki ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="e8524-155">In the **Add a link** dialog box, select a link for the breadcrumb root, and then select **OK**.</span></span>
1. <span data-ttu-id="e8524-156">Valitse **Tallenna** ja esikatsele sitten sivua valitsemalla **Esikatselu**.</span><span class="sxs-lookup"><span data-stu-id="e8524-156">Select **Save**, and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="e8524-157">Valitse **Lopeta muokkaus** tallentaaksesi mallin ja valitse sitten **Julkaise** julkaistaksesi sen.</span><span class="sxs-lookup"><span data-stu-id="e8524-157">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e8524-158">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="e8524-158">Additional resources</span></span>

[<span data-ttu-id="e8524-159">Moduulikirjaston yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="e8524-159">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="e8524-160">Siirtymisvalikkomoduulit</span><span class="sxs-lookup"><span data-stu-id="e8524-160">Navigation menu module</span></span>](nav-menu-module.md)

[<span data-ttu-id="e8524-161">Toimipaikan valitsinmoduuli</span><span class="sxs-lookup"><span data-stu-id="e8524-161">Site selector module</span></span>](site-selector.md)

[<span data-ttu-id="e8524-162">Luokan oletussaapumis- ja oletushakutulossivun yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="e8524-162">Overview of default category landing page and search results page</span></span>](category-search-page-overview.md)

[<span data-ttu-id="e8524-163">Tuotekokoelmamoduulit</span><span class="sxs-lookup"><span data-stu-id="e8524-163">Product collection modules</span></span>](product-collection-module-overview.md)

[<span data-ttu-id="e8524-164">Ostoruutumoduuli</span><span class="sxs-lookup"><span data-stu-id="e8524-164">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="e8524-165">SDK:n ja moduulikirjaston päivitykset</span><span class="sxs-lookup"><span data-stu-id="e8524-165">SDK and module library updates</span></span>](e-commerce-extensibility/sdk-updates.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]