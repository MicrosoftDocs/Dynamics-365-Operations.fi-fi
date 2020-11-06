---
title: Siirtymisvalikkomoduuli
description: Tässä ohjeaiheessa on tietoja siirtymisvalikkomoduuleista ja niiden lisäämisestä sivuston sivuille Microsoft Dynamics 365 Commercessa.
author: anupamar-ms
manager: annbe
ms.date: 10/01/2020
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
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: b0e8168ca9ec9ca68011650a73cc09983deca645
ms.sourcegitcommit: 765056b5dc1d0a8c27e56ff2cbd310ad3349ff09
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/20/2020
ms.locfileid: "4055734"
---
# <a name="navigation-menu-module"></a><span data-ttu-id="86123-103">Siirtymisvalikkomoduuli</span><span class="sxs-lookup"><span data-stu-id="86123-103">Navigation menu module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="86123-104">Tässä ohjeaiheessa on tietoja siirtymisvalikkomoduuleista ja niiden lisäämisestä sivuston sivuille Microsoft Dynamics 365 Commercessa.</span><span class="sxs-lookup"><span data-stu-id="86123-104">This topic covers navigation menu modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="86123-105">Yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="86123-105">Overview</span></span>

<span data-ttu-id="86123-106">Siirrymisvalikkomoduulien ensisijainen tarkoitus on antaa sivuston käyttäjille mahdollisuus selata tuotteita ja sivuston sivuja kanavan siirtymishierarkian mukaan. Hierarkia määritetään Dynamics 365 Commerce Headquarters -sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="86123-106">The primary purpose of navigation menu modules is to allow site users to browse products and site pages according to the channel navigation hierarchy defined in Dynamics 365 Commerce headquarters.</span></span> <span data-ttu-id="86123-107">Siirtymisvalikkomoduulissa määritetyt nimikkeet näkyvät sivuston otsikon navigointitoiminnossa.</span><span class="sxs-lookup"><span data-stu-id="86123-107">Items configured in a navigation menu module appear as site header navigation.</span></span> <span data-ttu-id="86123-108">Siirtymisvalikkomoduulit tukevat myös staattisia valikon vaihtoehtoja, joka sisältävät linkit muille sivuille sähköisen kaupankäynnin sivustossa.</span><span class="sxs-lookup"><span data-stu-id="86123-108">Navigation menu modules also support static menu items that link to other pages on an e-Commerce site.</span></span>

<span data-ttu-id="86123-109">Navigointivalikkomoduuli voidaan lisätä sivun ylätunnistemoduuliin.</span><span class="sxs-lookup"><span data-stu-id="86123-109">The navigation menu module can be added to the header module of a page.</span></span> <span data-ttu-id="86123-110">Fabrikam-teeman siirtymisvalikossa on näkyvissä kaksi tasoa oletusarvoisesti.</span><span class="sxs-lookup"><span data-stu-id="86123-110">In the Fabrikam theme, the navigation menu shows two levels by default.</span></span> <span data-ttu-id="86123-111">Starter (aloitus) -teeman siirtymisvalikossa on näkyvissä kolme tasoa oletusarvoisesti.</span><span class="sxs-lookup"><span data-stu-id="86123-111">In the Starter theme, the navigation menu shows three levels by default.</span></span> <span data-ttu-id="86123-112">Jos haluat vaihtaa tasojen määrän, teemalle on määritettävä näkymän laajennus.</span><span class="sxs-lookup"><span data-stu-id="86123-112">To change to the number of levels, a view extension is required on the theme.</span></span>

<span data-ttu-id="86123-113">Seuraavassa kuvassa on esimerkki Fabrikam-sivuston siirtymisvalikosta, jossa on kaksi luokkahierarkian tasoa ja joitakin staattisia valikon vaihtoehtoja.</span><span class="sxs-lookup"><span data-stu-id="86123-113">The following illustration shows an example of a navigation menu for the Fabrikam site with two levels of category hierarchy and some static menu items.</span></span>
<span data-ttu-id="86123-114">![Esimerkki siirtymisvalikkomoduulista](./media/ecommerce-header.png)</span><span class="sxs-lookup"><span data-stu-id="86123-114">![Example of a navigation meu module](./media/ecommerce-header.png)</span></span>

## <a name="navigation-menu-module-properties"></a><span data-ttu-id="86123-115">Siirtymisvalikkomoduulin ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="86123-115">Navigation menu module properties</span></span>

| <span data-ttu-id="86123-116">Ominaisuuden nimi</span><span class="sxs-lookup"><span data-stu-id="86123-116">Property name</span></span>             | <span data-ttu-id="86123-117">Arvo</span><span class="sxs-lookup"><span data-stu-id="86123-117">Value</span></span>                 | <span data-ttu-id="86123-118">kuvaus</span><span class="sxs-lookup"><span data-stu-id="86123-118">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="86123-119">Lähde</span><span class="sxs-lookup"><span data-stu-id="86123-119">Source</span></span>                  | <span data-ttu-id="86123-120">**Vähittäismyynti** , **Manuaalinen luominen** , **Vähittäismyynti ja manuaalinen luominen**</span><span class="sxs-lookup"><span data-stu-id="86123-120">**Retail** , **Manual authoring** , **Retail and manual authoring**</span></span> | <span data-ttu-id="86123-121">**Vähittäismyynti** -arvon ansiosta Commerce Headquarters -sovelluksen kanavan siirtymishierarkia voidaan näyttää siirtymisvalikossa.</span><span class="sxs-lookup"><span data-stu-id="86123-121">The **Retail** value allows the channel navigation hierarchy from Commerce headquarters to be displayed on the navigation menu.</span></span> <span data-ttu-id="86123-122">**Manuaalisen luominen** -arvo sallii staattisten valikon vaihtoehtojen kuratoinnin.</span><span class="sxs-lookup"><span data-stu-id="86123-122">The **Manual authoring** value allows static menu items to be curated.</span></span> <span data-ttu-id="86123-123">**Vähittäismyynti ja manuaalinen luominen** -arvo sallii näiden yhdistämisen.</span><span class="sxs-lookup"><span data-stu-id="86123-123">The **Retail and manual authoring** value allows a mix of both.</span></span> |
| <span data-ttu-id="86123-124">Näytä luokan kuvat</span><span class="sxs-lookup"><span data-stu-id="86123-124">Show category images</span></span> | <span data-ttu-id="86123-125">**Tosi** vai **Epätosi**</span><span class="sxs-lookup"><span data-stu-id="86123-125">**True** or **False**</span></span>    | <span data-ttu-id="86123-126">Kun tämä ominaisuus on käytössä, tämä ominaisuus näyttää siirtymisvalikon luokan kuvat Commerce Headquarters -sovelluksessa määritetyllä tavalla.</span><span class="sxs-lookup"><span data-stu-id="86123-126">When enabled, this property displays category images on the navigation menu as defined in Commerce headquarters for each category.</span></span> <span data-ttu-id="86123-127">Lisätty Commercen versioon 10.0.14.</span><span class="sxs-lookup"><span data-stu-id="86123-127">Added in Commerce release 10.0.14.</span></span> |
| <span data-ttu-id="86123-128">Ota monitasoinen siirtymisvalikko käyttöön</span><span class="sxs-lookup"><span data-stu-id="86123-128">Enable multi-level navigation menu</span></span> | <span data-ttu-id="86123-129">**Tosi** vai **Epätosi**</span><span class="sxs-lookup"><span data-stu-id="86123-129">**True** or **False**</span></span> | <span data-ttu-id="86123-130">Jos tämä ominaisuus on otettu käyttöön, siirtymisvalikossa näkyy monta siirtymishierarkian tasoa.</span><span class="sxs-lookup"><span data-stu-id="86123-130">When this property is enabled, the navigation menu can show multiple levels of the navigation hierarchy.</span></span> <span data-ttu-id="86123-131">Tämä ominaisuus on saatavana Dynamics 365 Commercen versiossa 10.0.15.</span><span class="sxs-lookup"><span data-stu-id="86123-131">This feature is available in the Dynamics 365 Commerce 10.0.15 release.</span></span> |
| <span data-ttu-id="86123-132">Tasojen määrä</span><span class="sxs-lookup"><span data-stu-id="86123-132">Number of levels</span></span> | <span data-ttu-id="86123-133">kokonaisluku</span><span class="sxs-lookup"><span data-stu-id="86123-133">integer</span></span> | <span data-ttu-id="86123-134">Tämä ominaisuus määrittää, kuinka monta tasoa voidaan näyttää, jos **Ota monitasoinen siirtymisvalikko käyttöön** -ominaisuuden arvoksi on määritetty **Tosi**.</span><span class="sxs-lookup"><span data-stu-id="86123-134">This property defines the numbers of levels that should be shown if the **Enable multilevel navigation menu** property is set to **True**.</span></span> |
| <span data-ttu-id="86123-135">Staattinen valikon vaihtoehto</span><span class="sxs-lookup"><span data-stu-id="86123-135">Static menu item</span></span>| <span data-ttu-id="86123-136">Arvomatriisi</span><span class="sxs-lookup"><span data-stu-id="86123-136">Array of values</span></span>| <span data-ttu-id="86123-137">Staattisia valikon vaihtoehtoha, jotka liittävät valikon vaihtoehdon nimen ja linkin staattisen sivuston sivuun.</span><span class="sxs-lookup"><span data-stu-id="86123-137">Static menu items that associate a menu item name with a link to a static site page.</span></span> <span data-ttu-id="86123-138">Voit luoda valikon vaihtoehtoja muiden valikon vaihtoehtojen alle.</span><span class="sxs-lookup"><span data-stu-id="86123-138">You can create menu items below other menu items.</span></span> <span data-ttu-id="86123-139">Oletusarvoisesti staattinen valikko näkyy juuri tasolla. Se liitetään kanavan siirtymishierarkiaan, jos se on olemassa.</span><span class="sxs-lookup"><span data-stu-id="86123-139">By default, static menus appear at the root level and will be appended to the channel navigation hierarchy if it exists.</span></span> |
| <span data-ttu-id="86123-140">Näytä päävalikko</span><span class="sxs-lookup"><span data-stu-id="86123-140">Show root menu</span></span> | <span data-ttu-id="86123-141">**Tosi** vai **Epätosi**</span><span class="sxs-lookup"><span data-stu-id="86123-141">**True** or **False**</span></span> | <span data-ttu-id="86123-142">Jos tämä ominaisuus on otettu käyttöön, siirtymisvalikko voidaan määrittää mukautetussa juuressa (kuten **Osta nyt** ).</span><span class="sxs-lookup"><span data-stu-id="86123-142">When this property is enabled, the navigation menu can be defined under a custom root (for example, **Shop now** ).</span></span> <span data-ttu-id="86123-143">Tämä ominaisuus on saatavana Dynamics 365 Commercen versiossa 10.0.15.</span><span class="sxs-lookup"><span data-stu-id="86123-143">This feature is available in the Dynamics 365 Commerce 10.0.15 release.</span></span> |
| <span data-ttu-id="86123-144">Päävalikko</span><span class="sxs-lookup"><span data-stu-id="86123-144">Root menu</span></span> | <span data-ttu-id="86123-145">merkkijono</span><span class="sxs-lookup"><span data-stu-id="86123-145">string</span></span> | <span data-ttu-id="86123-146">Tällä ominaisuudella voi määrittää mukautetun juuren teksti, jos **Näytä päävalikko** -ominaisuudeksi on määritetty **Tosi**.</span><span class="sxs-lookup"><span data-stu-id="86123-146">This property can be used to define text for a custom root if the **Show root menu** property is set to **True**.</span></span> |

<span data-ttu-id="86123-147">Seuraavassa kuvassa näkyy esimerkki Fabrikam-sivuston siirtymisvalikossa näkyvästä luokan kuvasta.</span><span class="sxs-lookup"><span data-stu-id="86123-147">The following illustration shows an example of a category image displayed on the navigation menu for the Fabrikam site.</span></span>
<span data-ttu-id="86123-148">![Esimerkki siirtymisvalikkomoduulista ja luokan kuvista](./media/ecommerce-categoryimages.PNG)</span><span class="sxs-lookup"><span data-stu-id="86123-148">![Example of a navigation meu module with category images](./media/ecommerce-categoryimages.PNG)</span></span>

## <a name="add-a-navigation-menu-module-to-a-header-module"></a><span data-ttu-id="86123-149">Siirtymisvalikkomoduulin lisääminen ylätunnistemoduuliin</span><span class="sxs-lookup"><span data-stu-id="86123-149">Add a navigation menu module to a header module</span></span>

<span data-ttu-id="86123-150">Lisätietoja siirtymisvalikkomoduulin lisäämisestä ylätunnistemoduuliin on kohdassa [Ylätunnistemoduuli](author-header-module.md).</span><span class="sxs-lookup"><span data-stu-id="86123-150">For details about how to add a navigation menu module to a header module, see [Header module](author-header-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="86123-151">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="86123-151">Additional resources</span></span>

[<span data-ttu-id="86123-152">Moduulikirjaston yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="86123-152">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="86123-153">Navigointipolkumoduuli</span><span class="sxs-lookup"><span data-stu-id="86123-153">Breadcrumb module</span></span>](add-breadcrumb.md)

[<span data-ttu-id="86123-154">Toimipaikan valitsinmoduuli</span><span class="sxs-lookup"><span data-stu-id="86123-154">Site selector module</span></span>](site-selector.md)

[<span data-ttu-id="86123-155">Ostoruutumoduuli</span><span class="sxs-lookup"><span data-stu-id="86123-155">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="86123-156">Evästeen yhteensopivuus</span><span class="sxs-lookup"><span data-stu-id="86123-156">Cookie compliance</span></span>](cookie-compliance.md)

[<span data-ttu-id="86123-157">Ylätunnistemoduuli</span><span class="sxs-lookup"><span data-stu-id="86123-157">Header module</span></span>](author-header-module.md)
