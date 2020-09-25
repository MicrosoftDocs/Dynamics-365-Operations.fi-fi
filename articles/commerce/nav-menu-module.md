---
title: Siirtymisvalikkomoduuli
description: Tässä ohjeaiheessa on tietoja siirtymisvalikkomoduuleista ja niiden lisäämisestä sivuston sivuille Microsoft Dynamics 365 Commercessa.
author: anupamar-ms
manager: annbe
ms.date: 08/31/2020
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
ms.openlocfilehash: 9f66bbe7bf436ab6360dda7d92d6d51e47eedf16
ms.sourcegitcommit: 420b9e538f706178f8e1f2786e02f4f400bf2336
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/02/2020
ms.locfileid: "3761385"
---
# <a name="navigation-menu-module"></a><span data-ttu-id="4f787-103">Siirtymisvalikkomoduuli</span><span class="sxs-lookup"><span data-stu-id="4f787-103">Navigation menu module</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="4f787-104">Tässä ohjeaiheessa on tietoja siirtymisvalikkomoduuleista ja niiden lisäämisestä sivuston sivuille Microsoft Dynamics 365 Commercessa.</span><span class="sxs-lookup"><span data-stu-id="4f787-104">This topic covers navigation menu modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="4f787-105">Yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="4f787-105">Overview</span></span>

<span data-ttu-id="4f787-106">Siirrymisvalikkomoduulien ensisijainen tarkoitus on antaa sivuston käyttäjille mahdollisuus selata tuotteita ja sivuston sivuja kanavan siirtymishierarkian mukaan. Hierarkia määritetään Dynamics 365 Commerce Headquarters -sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="4f787-106">The primary purpose of navigation menu modules is to allow site users to browse products and site pages according to the channel navigation hierarchy defined in Dynamics 365 Commerce headquarters.</span></span> <span data-ttu-id="4f787-107">Siirtymisvalikkomoduulissa määritetyt nimikkeet näkyvät sivuston otsikon navigointitoiminnossa.</span><span class="sxs-lookup"><span data-stu-id="4f787-107">Items configured in a navigation menu module appear as site header navigation.</span></span> <span data-ttu-id="4f787-108">Siirtymisvalikkomoduulit tukevat myös staattisia valikon vaihtoehtoja, joka sisältävät linkit muille sivuille sähköisen kaupankäynnin sivustossa.</span><span class="sxs-lookup"><span data-stu-id="4f787-108">Navigation menu modules also support static menu items that link to other pages on an e-Commerce site.</span></span>

<span data-ttu-id="4f787-109">Navigointivalikkomoduuli voidaan lisätä sivun ylätunnistemoduuliin.</span><span class="sxs-lookup"><span data-stu-id="4f787-109">The navigation menu module can be added to the header module of a page.</span></span> <span data-ttu-id="4f787-110">Fabrikam-teeman siirtymisvalikossa on näkyvissä kaksi tasoa oletusarvoisesti.</span><span class="sxs-lookup"><span data-stu-id="4f787-110">In the Fabrikam theme, the navigation menu shows two levels by default.</span></span> <span data-ttu-id="4f787-111">Starter (aloitus) -teeman siirtymisvalikossa on näkyvissä kolme tasoa oletusarvoisesti.</span><span class="sxs-lookup"><span data-stu-id="4f787-111">In the Starter theme, the navigation menu shows three levels by default.</span></span> <span data-ttu-id="4f787-112">Jos haluat vaihtaa tasojen määrän, teemalle on määritettävä näkymän laajennus.</span><span class="sxs-lookup"><span data-stu-id="4f787-112">To change to the number of levels, a view extension is required on the theme.</span></span>

<span data-ttu-id="4f787-113">Seuraavassa kuvassa on esimerkki Fabrikam-sivuston siirtymisvalikosta, jossa on kaksi luokkahierarkian tasoa ja joitakin staattisia valikon vaihtoehtoja.</span><span class="sxs-lookup"><span data-stu-id="4f787-113">The following illustration shows an example of a navigation menu for the Fabrikam site with two levels of category hierarchy and some static menu items.</span></span>
<span data-ttu-id="4f787-114">![Esimerkki siirtymisvalikkomoduulista](./media/ecommerce-header.png)</span><span class="sxs-lookup"><span data-stu-id="4f787-114">![Example of a navigation meu module](./media/ecommerce-header.png)</span></span>

## <a name="navigation-menu-module-properties"></a><span data-ttu-id="4f787-115">Siirtymisvalikkomoduulin ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="4f787-115">Navigation menu module properties</span></span>

| <span data-ttu-id="4f787-116">Ominaisuuden nimi</span><span class="sxs-lookup"><span data-stu-id="4f787-116">Property name</span></span>             | <span data-ttu-id="4f787-117">Arvo</span><span class="sxs-lookup"><span data-stu-id="4f787-117">Value</span></span>                 | <span data-ttu-id="4f787-118">kuvaus</span><span class="sxs-lookup"><span data-stu-id="4f787-118">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="4f787-119">Lähde</span><span class="sxs-lookup"><span data-stu-id="4f787-119">Source</span></span>                  | <span data-ttu-id="4f787-120">**Vähittäismyynti**, **Manuaalinen luominen**, **Vähittäismyynti ja manuaalinen luominen**</span><span class="sxs-lookup"><span data-stu-id="4f787-120">**Retail**, **Manual authoring**, **Retail and manual authoring**</span></span> | <span data-ttu-id="4f787-121">**Vähittäismyynti**-arvon ansiosta Commerce Headquarters -sovelluksen kanavan siirtymishierarkia voidaan näyttää siirtymisvalikossa.</span><span class="sxs-lookup"><span data-stu-id="4f787-121">The **Retail** value allows the channel navigation hierarchy from Commerce headquarters to be displayed on the navigation menu.</span></span> <span data-ttu-id="4f787-122">**Manuaalisen luominen** -arvo sallii staattisten valikon vaihtoehtojen kuratoinnin.</span><span class="sxs-lookup"><span data-stu-id="4f787-122">The **Manual authoring** value allows static menu items to be curated.</span></span> <span data-ttu-id="4f787-123">**Vähittäismyynti ja manuaalinen luominen** -arvo sallii näiden yhdistämisen.</span><span class="sxs-lookup"><span data-stu-id="4f787-123">The **Retail and manual authoring** value allows a mix of both.</span></span> |
| <span data-ttu-id="4f787-124">Näytä luokan kuvat</span><span class="sxs-lookup"><span data-stu-id="4f787-124">Show category images</span></span> | <span data-ttu-id="4f787-125">**Tosi** vai **Epätosi**</span><span class="sxs-lookup"><span data-stu-id="4f787-125">**True** or **False**</span></span>    | <span data-ttu-id="4f787-126">Kun tämä ominaisuus on käytössä, tämä ominaisuus näyttää siirtymisvalikon luokan kuvat Commerce Headquarters -sovelluksessa määritetyllä tavalla.</span><span class="sxs-lookup"><span data-stu-id="4f787-126">When enabled, this property displays category images on the navigation menu as defined in Commerce headquarters for each category.</span></span> <span data-ttu-id="4f787-127">Lisätty Commercen versioon 10.0.14.</span><span class="sxs-lookup"><span data-stu-id="4f787-127">Added in Commerce release 10.0.14.</span></span> |
| <span data-ttu-id="4f787-128">Staattinen valikon vaihtoehto</span><span class="sxs-lookup"><span data-stu-id="4f787-128">Static menu item</span></span>| <span data-ttu-id="4f787-129">Arvomatriisi</span><span class="sxs-lookup"><span data-stu-id="4f787-129">Array of values</span></span>| <span data-ttu-id="4f787-130">Staattisia valikon vaihtoehtoha, jotka liittävät valikon vaihtoehdon nimen ja linkin staattisen sivuston sivuun.</span><span class="sxs-lookup"><span data-stu-id="4f787-130">Static menu items that associate a menu item name with a link to a static site page.</span></span> <span data-ttu-id="4f787-131">Voit luoda valikon vaihtoehtoja muiden valikon vaihtoehtojen alle.</span><span class="sxs-lookup"><span data-stu-id="4f787-131">You can create menu items below other menu items.</span></span> <span data-ttu-id="4f787-132">Oletusarvoisesti staattinen valikko näkyy juuri tasolla. Se liitetään kanavan siirtymishierarkiaan, jos se on olemassa.</span><span class="sxs-lookup"><span data-stu-id="4f787-132">By default, static menus appear at the root level and will be appended to the channel navigation hierarchy if it exists.</span></span> |

<span data-ttu-id="4f787-133">Seuraavassa kuvassa näkyy esimerkki Fabrikam-sivuston siirtymisvalikossa näkyvästä luokan kuvasta.</span><span class="sxs-lookup"><span data-stu-id="4f787-133">The following illustration shows an example of a category image displayed on the navigation menu for the Fabrikam site.</span></span>
<span data-ttu-id="4f787-134">![Esimerkki siirtymisvalikkomoduulista ja luokan kuvista](./media/ecommerce-categoryimages.PNG)</span><span class="sxs-lookup"><span data-stu-id="4f787-134">![Example of a navigation meu module with category images](./media/ecommerce-categoryimages.PNG)</span></span>

## <a name="add-a-navigation-menu-module-to-a-header-module"></a><span data-ttu-id="4f787-135">Siirtymisvalikkomoduulin lisääminen ylätunnistemoduuliin</span><span class="sxs-lookup"><span data-stu-id="4f787-135">Add a navigation menu module to a header module</span></span>

<span data-ttu-id="4f787-136">Lisätietoja siirtymisvalikkomoduulin lisäämisestä ylätunnistemoduuliin on kohdassa [Ylätunnistemoduuli](author-header-module.md).</span><span class="sxs-lookup"><span data-stu-id="4f787-136">For details about how to add a navigation menu module to a header module, see [Header module](author-header-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4f787-137">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="4f787-137">Additional resources</span></span>

[<span data-ttu-id="4f787-138">Aloituspakkauksen yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="4f787-138">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="4f787-139">Ostoruutumoduuli</span><span class="sxs-lookup"><span data-stu-id="4f787-139">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="4f787-140">Evästeen yhteensopivuus</span><span class="sxs-lookup"><span data-stu-id="4f787-140">Cookie compliance</span></span>](cookie-compliance.md)

[<span data-ttu-id="4f787-141">Ylätunnistemoduuli</span><span class="sxs-lookup"><span data-stu-id="4f787-141">Header module</span></span>](author-header-module.md)
