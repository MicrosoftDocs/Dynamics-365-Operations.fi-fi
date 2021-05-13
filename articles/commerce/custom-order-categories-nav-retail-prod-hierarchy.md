---
title: Kaupankäynnin entiteettien lajittelujärjestyksen muuttaminen
description: Tässä ohjeaiheessa selitetään käsitteitä, jotka liittyvät useiden kaupankäyntiin liittyvien entiteettien näyttöjärjestyksen valvontaan Dynamics 365 Commercessa.
author: josaw1
ms.date: 08/05/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: Category, Retail product hierarchy, Navigation hierarchy
audience: Application User, Merchandising manager, Catalog manager
ms.reviewer: josaw
ms.custom: 268444
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 31798508e4cc71e31a30dc91acebfdde8226b16c
ms.sourcegitcommit: 9eadc7ca08e2db3fd208f5fc835551abe9d06dc8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/22/2021
ms.locfileid: "5937059"
---
# <a name="change-the-sort-order-for-merchandising-entities"></a><span data-ttu-id="01782-103">Kaupankäynnin entiteettien lajittelujärjestyksen muuttaminen</span><span class="sxs-lookup"><span data-stu-id="01782-103">Change the sort order for merchandising entities</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="01782-104">Vähittäiskauppiaat pitävät tuotteen etsintätyökalua ensisijaisena työkaluna asiakkaan vuorovaikutuksessa kaikkien kanavien kautta.</span><span class="sxs-lookup"><span data-stu-id="01782-104">Retailers consider product discovery a primary tool for customer interaction across all channels.</span></span> <span data-ttu-id="01782-105">Eri toiminnot voivat auttaa asiakkaita löytämään tuotteita helposti.</span><span class="sxs-lookup"><span data-stu-id="01782-105">Various functionality can help customers easily discover products.</span></span> <span data-ttu-id="01782-106">He voivat esimerkiksi selata luokkia, hakua ja suodatusta.</span><span class="sxs-lookup"><span data-stu-id="01782-106">For example, they can browse categories, search, and filter.</span></span>

<span data-ttu-id="01782-107">Tässä ohjeaiheessa selitetään käsitteitä, jotka liittyvät useiden kaupankäyntiin liittyvien entiteettien näyttöjärjestyksen valvontaan.</span><span class="sxs-lookup"><span data-stu-id="01782-107">This topic explains the concepts that are related to controlling the display order for various merchandising-related entities.</span></span> <span data-ttu-id="01782-108">Siinä selitetään myös lajittelujärjestyksen muuttaminen.</span><span class="sxs-lookup"><span data-stu-id="01782-108">It also explains how to change the sort order.</span></span>

## <a name="overview"></a><span data-ttu-id="01782-109">Yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="01782-109">Overview</span></span>

<span data-ttu-id="01782-110">Useiden kaupankäyntiin liittyvien entiteettien lajittelun tukea on parannettu.</span><span class="sxs-lookup"><span data-stu-id="01782-110">The support for sorting various merchandising-related entities has been enhanced.</span></span> <span data-ttu-id="01782-111">Tämä tuki on nyt paremmin linjassa nykyisten asiakasskenaarioiden kanssa, jotka ovat aiemmin edellyttäneet käyttöönottokumppaneiden laajennuksia.</span><span class="sxs-lookup"><span data-stu-id="01782-111">This support is now better aligned with existing customer scenarios that previously required extensions from implementation partners.</span></span>

<span data-ttu-id="01782-112">Retailin versiota 10.0.5 vanhemmissa versioissa siirtymishierarkian luokkien lajittelujärjestys oli aakkosjärjestyksessä.</span><span class="sxs-lookup"><span data-stu-id="01782-112">In versions of Retail that are earlier than version 10.0.5, the sort order for categories in the navigation hierarchy was alphabetical.</span></span> <span data-ttu-id="01782-113">Uuden mukautetun lajittelujärjestystoiminnon avulla myyntipäälliköt voivat määrittää eri myyntikohteisiin liittyvien entiteettien lajittelujärjestyksen kaikissa peruskäyttäjäohjelmissa.</span><span class="sxs-lookup"><span data-stu-id="01782-113">The new custom sort order functionality lets merchandising managers configure the sort order for various merchandising-related entities across all end-user clients.</span></span> <span data-ttu-id="01782-114">Näitä asiakasohjelmia ovat esimerkiksi pääkonttori (HQ) ja puhelinkeskus.</span><span class="sxs-lookup"><span data-stu-id="01782-114">These clients include headquarters (HQ) and call centers.</span></span>

## <a name="configure-the-display-order-for-categories-in-the-product-hierarchy"></a><span data-ttu-id="01782-115">Tuotehierarkian luokkien näyttöjärjestyksen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="01782-115">Configure the display order for categories in the product hierarchy</span></span>

<span data-ttu-id="01782-116">Ennen kuin voit tehdä nämä toimet, demotiedot on asennettava ympäristöösi.</span><span class="sxs-lookup"><span data-stu-id="01782-116">Before you can complete this procedure, demo data must be installed in your environment.</span></span>

1. <span data-ttu-id="01782-117">Valitse **Retail ja Commerce \> Luokka- ja tuotehallinta \> Commerce-tuotehierarkia**.</span><span class="sxs-lookup"><span data-stu-id="01782-117">Go to **Retail and Commerce \> Products and categories \> Commerce product hierarchy**.</span></span>
2. <span data-ttu-id="01782-118">Valitse **Muokkaa luokkahierarkiaa**.</span><span class="sxs-lookup"><span data-stu-id="01782-118">Click **Edit category hierarchy**.</span></span>
3. <span data-ttu-id="01782-119">Valitse **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="01782-119">Click **Edit**.</span></span>
4. <span data-ttu-id="01782-120">Laajenna puussa **ALL \> Action Sports**.</span><span class="sxs-lookup"><span data-stu-id="01782-120">In the tree, expand **ALL \> Action Sports**.</span></span>
5. <span data-ttu-id="01782-121">Laajenna puussa **ALL \> Team Sports**.</span><span class="sxs-lookup"><span data-stu-id="01782-121">In the tree, expand **ALL \> Team Sports**.</span></span>
6. <span data-ttu-id="01782-122">Syötä **Näyttöjärjestys**-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="01782-122">In the **Display order** field, enter a number.</span></span> <span data-ttu-id="01782-123">(Luku voi olla negatiivinen.)</span><span class="sxs-lookup"><span data-stu-id="01782-123">(The number can be negative.)</span></span>
7. <span data-ttu-id="01782-124">Toista vaiheet 4-6 kaikille muille luokille, joiden järjestystä haluat muuttaa.</span><span class="sxs-lookup"><span data-stu-id="01782-124">Repeat steps 4 through 6 for any additional categories that you want to change the order of.</span></span>

<span data-ttu-id="01782-125">Kanavan siirtymishierarkian näyttöjärjestys näkyy kaupankäynnin tuotehierarkian ja vapautettujen tuotteiden luokan pääkonttorissa.</span><span class="sxs-lookup"><span data-stu-id="01782-125">The display order for the channel navigation hierarchy will be reflected in HQ for the commerce product hierarchy and released products by category.</span></span>

![Tuotehierarkian mukautettu lajittelu negatiivisin arvoin](./media/RetailProductHierarchyCustomSortedWithNegativeValues.png)

![Vapautetut tuotteet luokittain tuotehierarkian mukaan mukautetusti lajiteltuna](./media/ReleasedProductsByCategoryCustomSortedBasedOnRetailProductHierarchy.png)

## <a name="configure-the-display-order-for-categories-in-the-channel-navigation-hierarchy"></a><span data-ttu-id="01782-128">Kanavan siirtymishierarkian luokkien näyttöjärjestyksen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="01782-128">Configure the display order for categories in the channel navigation hierarchy</span></span>

<span data-ttu-id="01782-129">Ennen kuin voit tehdä nämä toimet, demotiedot on asennettava ympäristöösi.</span><span class="sxs-lookup"><span data-stu-id="01782-129">Before you can complete this procedure, demo data must be installed in your environment.</span></span>

1. <span data-ttu-id="01782-130">Siirry kohtaan **Retail ja Commerce \> Tuotteet ja luokat \> Kanavan siirtymisluokat**.</span><span class="sxs-lookup"><span data-stu-id="01782-130">Go to **Retail and Commerce \> Products and categories \> Channel navigation categories**.</span></span>
2. <span data-ttu-id="01782-131">Valitse luettelosta **Fashion**-siirtymishierarkia.</span><span class="sxs-lookup"><span data-stu-id="01782-131">In the list, select the **Fashion navigation** hierarchy.</span></span>
3. <span data-ttu-id="01782-132">Valitse **Muokkaa luokkahierarkiaa**.</span><span class="sxs-lookup"><span data-stu-id="01782-132">Click **Edit category hierarchy**.</span></span>
4. <span data-ttu-id="01782-133">Valitse **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="01782-133">Click **Edit**.</span></span>
5. <span data-ttu-id="01782-134">Valitse puussa **Fashion \> Womenswear \> Womens Shoes**.</span><span class="sxs-lookup"><span data-stu-id="01782-134">In the tree, select **Fashion \> Womenswear \> Womens Shoes**.</span></span>
6. <span data-ttu-id="01782-135">Syötä **Näyttöjärjestys**-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="01782-135">In the **Display order** field, enter a number.</span></span>
7. <span data-ttu-id="01782-136">Valitse puussa **Fashion \> Womenswear \> Tops**.</span><span class="sxs-lookup"><span data-stu-id="01782-136">In the tree, select **Fashion \> Womenswear \> Tops**.</span></span>

    <span data-ttu-id="01782-137">Voit myös määrittää alaluokkien lajittelujärjestyksen.</span><span class="sxs-lookup"><span data-stu-id="01782-137">Likewise, you can define the sort order for the sub-categories.</span></span>

8. <span data-ttu-id="01782-138">Valitse puussa **Fashion \> Menswear \> Casual Shirts**.</span><span class="sxs-lookup"><span data-stu-id="01782-138">In the tree, select **Fashion \> Menswear \> Casual Shirts**.</span></span>
9. <span data-ttu-id="01782-139">Syötä **Näyttöjärjestys**-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="01782-139">In the **Display order** field, enter a number.</span></span>
10. <span data-ttu-id="01782-140">Valitse puussa **Fashion \> Menswear \> Coats & Jackets**.</span><span class="sxs-lookup"><span data-stu-id="01782-140">In the tree, select **Fashion \> Menswear \> Coats & Jackets**.</span></span>
11. <span data-ttu-id="01782-141">Syötä **Näyttöjärjestys**-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="01782-141">In the **Display order** field, enter a number.</span></span>
12. <span data-ttu-id="01782-142">Toista kaikille muille luokille, joiden järjestystä haluat muuttaa.</span><span class="sxs-lookup"><span data-stu-id="01782-142">Repeat for any additional categories that you want to change the order of.</span></span>

<span data-ttu-id="01782-143">Kanavan siirtymishierarkian näyttöjärjestys näkyy pääkonttorissa, tuoteluettelossa ja kanavissa.</span><span class="sxs-lookup"><span data-stu-id="01782-143">The display order for the channel navigation hierarchy is reflected in HQ, catalog, and channels.</span></span>

![Kanavan siirtymishierarkia mukautetusti lajiteltuna](./media/ChannelNavCustomSorted.png)

![Luettelon siirtymishierarkia mukautetusti lajiteltuna kanavan siirtymishierarkian mukaan](./media/CatalogNavHierarchyCustomSortedBasedOnChannelNav.png)

![Myyntipisteet, jossa on mukautettuja lajiteltuja luokkia](./media/POSChannelCategoriesCustomSorted.png)

> [!NOTE]
> <span data-ttu-id="01782-147">Mukautettu lajittelujärjestys on oletusarvoisesti poissa käytöstä.</span><span class="sxs-lookup"><span data-stu-id="01782-147">By default the custom sort order feature is turned off.</span></span> <span data-ttu-id="01782-148">Lisätietoja tämän toiminnon ja muiden toimintojen ottamisesta käyttöön on kohdassa [Ominaisuuksien hallinta](/dynamics365/unified-operations/fin-and-ops/get-started/feature-management/feature-management-overview).</span><span class="sxs-lookup"><span data-stu-id="01782-148">To learn how to turn on this feature and other features, see [Feature management](/dynamics365/unified-operations/fin-and-ops/get-started/feature-management/feature-management-overview).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]