---
title: Määritä luokitukset ja arvostelut
description: Tässä ohjeaiheessa kerrotaan, miten sähköisen kaupankäynnin sivusto määritetään niin, että se näyttää asiakasluokituksia ja -arvostelut Microsoft Dynamics 365 Commerce -sovelluksessa.
author: gvrmohanreddy
manager: annbe
ms.date: 02/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: edd2082b5d2cafcb955f8e3c7762bcba523ac479
ms.sourcegitcommit: 0dace221e8874021dd212271567666f717d39793
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/19/2020
ms.locfileid: "3071563"
---
# <a name="configure-ratings-and-reviews"></a><span data-ttu-id="8ad8b-103">Määritä luokitukset ja arvostelut</span><span class="sxs-lookup"><span data-stu-id="8ad8b-103">Configure ratings and reviews</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="8ad8b-104">Tässä ohjeaiheessa kerrotaan, miten sähköisen kaupankäynnin sivusto määritetään niin, että se näyttää asiakasluokituksia ja -arvostelut Microsoft Dynamics 365 Commerce -sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="8ad8b-104">This topic describes how to configure your e-Commerce site to show customer ratings and reviews in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="8ad8b-105">Yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="8ad8b-105">Overview</span></span>

<span data-ttu-id="8ad8b-106">Sähköisen kaupankäynnin sivustojen luokitukset ja arvostelut auttavat asiakkaita saamaan tietoja tuotteista ennen ostopäätöksen tekemistä. NIiden avulla saadaan selville, mitä muut asiakkaat ajattelevat kyseisistä tuotteista.</span><span class="sxs-lookup"><span data-stu-id="8ad8b-106">Ratings and reviews on e-Commerce websites help customers learn about products before they make a purchase decision by showing them what other customers think about those products.</span></span> <span data-ttu-id="8ad8b-107">Sähköisen kaupankäynnin sivustoissa luokitukset ja arvostelut ovat myös keino, jolla kerätään asiakaspalautetta tuotteista.</span><span class="sxs-lookup"><span data-stu-id="8ad8b-107">For e-Commerce websites, ratings and reviews are also a mechanism for collecting customer feedback about products.</span></span> 

## <a name="configure-a-site-to-show-ratings-and-reviews"></a><span data-ttu-id="8ad8b-108">Sivuston määrittäminen niin, että se näyttää luokitukset ja arvostelut</span><span class="sxs-lookup"><span data-stu-id="8ad8b-108">Configure a site to show ratings and reviews</span></span>

<span data-ttu-id="8ad8b-109">Luokitusten ja arvostelujen määrityksen arvot, kuten vuokraajan tunnus, arvostelun tekstin pituus ja luokituksen otsikon pituus, määritetään sivustotasolla.</span><span class="sxs-lookup"><span data-stu-id="8ad8b-109">Configuration values for ratings and reviews, such as the tenant ID, review text length, and review title length, are configured at the site level.</span></span> 

<span data-ttu-id="8ad8b-110">Voit määrittää sivuston näyttämään luokitukset ja arvostelut seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="8ad8b-110">To configure a site to show ratings and reviews, follow these steps.</span></span> 

1. <span data-ttu-id="8ad8b-111">Siirry kohtaan **Aloitus \> Sivustot**.</span><span class="sxs-lookup"><span data-stu-id="8ad8b-111">Go to **Home \> Sites**.</span></span>
1. <span data-ttu-id="8ad8b-112">Valitse sivuston nimi.</span><span class="sxs-lookup"><span data-stu-id="8ad8b-112">Select the name of your site.</span></span> 
1. <span data-ttu-id="8ad8b-113">Siirry kohtaan **Sivuston asetukset \> Laajennukset**.</span><span class="sxs-lookup"><span data-stu-id="8ad8b-113">Go to **Site settings \> Extensions**.</span></span> 
1. <span data-ttu-id="8ad8b-114">Syötä **Arvostelun tekstin enimmäispituus** -kenttään arvostelun tekstin merkkien enimmäismäärä (esimerkiksi **1 000**).</span><span class="sxs-lookup"><span data-stu-id="8ad8b-114">In the **Review text max length** field, enter the maximum number of characters that review text can have (for example, **1000**).</span></span> 
1. <span data-ttu-id="8ad8b-115">Syötä **Arvostelun otsikon enimmäispituus** -kenttään arvostelun otsikoiden merkkien enimmäismäärä (esimerkiksi **55**).</span><span class="sxs-lookup"><span data-stu-id="8ad8b-115">In the **Review title max length** field, enter the maximum number of characters that review titles can have (for example, **55**).</span></span> 
1. <span data-ttu-id="8ad8b-116">Valitse **Tallenna ja julkaise**.</span><span class="sxs-lookup"><span data-stu-id="8ad8b-116">Select **Save and Publish**.</span></span> 

<span data-ttu-id="8ad8b-117">Seuraava kuva osoittaa, miltä tämä määritys näyttää Dynamics 365 Commerce -sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="8ad8b-117">The following illustration shows what this configuration looks like in Dynamics 365 Commerce.</span></span>

![Sivuston määrittäminen niin, että se näyttää luokitukset ja arvostelut](media/rnr-eCommerce-site-appsettings.png)

## <a name="link-a-product-rating-to-the-reviews-section-of-a-pdp"></a><span data-ttu-id="8ad8b-119">Tuoteluokituksen linkittäminen PDP:n Arvostelut-osaan</span><span class="sxs-lookup"><span data-stu-id="8ad8b-119">Link a product rating to the Reviews section of a PDP</span></span>

<span data-ttu-id="8ad8b-120">Tuoteluokitus näkyy PDP:n yläosassa olevan tuotteen otsikon alla.</span><span class="sxs-lookup"><span data-stu-id="8ad8b-120">A product rating is shown below the product title at the top of PDP.</span></span> <span data-ttu-id="8ad8b-121">Tuoteluokitus voidaan määrittää niin, että se on linkitetty saman PDP:n **Arvostelut**-osaan.</span><span class="sxs-lookup"><span data-stu-id="8ad8b-121">The product rating can be configured so that it's linked to the **Reviews** section of the same PDP.</span></span> 

<span data-ttu-id="8ad8b-122">Voit linkittää tuoteluokituksen PDP:n osan **Arvostelut**-osaan seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="8ad8b-122">To link a product rating to the **Reviews** section of the PDP, follow these steps.</span></span>

1. <span data-ttu-id="8ad8b-123">Avaa PDP-malli.</span><span class="sxs-lookup"><span data-stu-id="8ad8b-123">Open the PDP template.</span></span> 
1. <span data-ttu-id="8ad8b-124">Siirry kohtaan **Ostoruudun säilömoduulin asetukset**.</span><span class="sxs-lookup"><span data-stu-id="8ad8b-124">Go to **Buy box container module settings**.</span></span>
1. <span data-ttu-id="8ad8b-125">Valitse **Ostoruutu**-kohdassa **Tuoteluokitukset** ja valitse sitten **Linkitä napsautus täydellisten arviointien moduuliin** -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="8ad8b-125">Under **Buy box**, select **Product ratings**, and then select the **Link the click to full reviews module** check box.</span></span>

<span data-ttu-id="8ad8b-126">Seuraava kuva osoittaa, miltä tämä määritys näyttää Dynamics 365 Commerce -sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="8ad8b-126">The following illustration shows what this configuration looks like in Dynamics 365 Commerce.</span></span>

![Tuoteluokituksen linkittäminen PDP:n Arvostelut-osaan](media/rnr-eCommerce-buy-box-rating-summary.png)

## <a name="configure-the-link-for-the-privacy-and-policy-page"></a><span data-ttu-id="8ad8b-128">Tietosuoja- ja käytäntösivun linkin määrittäminen</span><span class="sxs-lookup"><span data-stu-id="8ad8b-128">Configure the link for the privacy and policy page</span></span>

<span data-ttu-id="8ad8b-129">Voit määrittää tietosuoja- ja käytäntösivun linkin seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="8ad8b-129">To configure the link for the privacy and policy page, follow these steps.</span></span>

1. <span data-ttu-id="8ad8b-130">Siirry kohtaan **Aloitus \> Sivustot**.</span><span class="sxs-lookup"><span data-stu-id="8ad8b-130">Go to **Home \> Sites**.</span></span>
1. <span data-ttu-id="8ad8b-131">Valitse sivuston nimi.</span><span class="sxs-lookup"><span data-stu-id="8ad8b-131">Select the name of your site.</span></span> 
1. <span data-ttu-id="8ad8b-132">Siirry kohtaan **Sivuston asetukset \> Laajennukset**.</span><span class="sxs-lookup"><span data-stu-id="8ad8b-132">Go to **Site settings \> Extensions**.</span></span>
1. <span data-ttu-id="8ad8b-133">Valitse **Reitit**-välilehdessä **RNR - tietosuoja ja käytäntö** -kohdassa **Lisää linkki**.</span><span class="sxs-lookup"><span data-stu-id="8ad8b-133">On the **Routes** tab, under **RNR Privacy and Policy**, select **Add a link**.</span></span> <span data-ttu-id="8ad8b-134">Jos linkki on jo syötetty ja haluat korvata sen, valitse linkki.</span><span class="sxs-lookup"><span data-stu-id="8ad8b-134">If a link is already entered, and you want to replace it, select the link.</span></span> 
1. <span data-ttu-id="8ad8b-135">Valitse **Lisää linkki** -valintaikkunassa tietosuoja-ja käytäntösivun linkki ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="8ad8b-135">In the **Add a link** dialog box, select the link for the privacy and policy page, and then select **OK**.</span></span> 
1. <span data-ttu-id="8ad8b-136">Valitse **Tallenna ja julkaise**.</span><span class="sxs-lookup"><span data-stu-id="8ad8b-136">Select **Save and Publish**.</span></span> 

<span data-ttu-id="8ad8b-137">Seuraava kuva osoittaa, miltä tämä määritys näyttää Dynamics 365 Commerce -sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="8ad8b-137">The following illustration shows what this configuration looks like in Dynamics 365 Commerce.</span></span>

![Tietosuoja- ja käytäntösivun linkin määrittäminen](media/rnr-eCommerce-rnr-privacy-policy-link.png)

## <a name="configure-ratings-and-reviews-modules-on-product-details-pages"></a><span data-ttu-id="8ad8b-139">Luokitus- ja arvostelumoduulien määrittäminen tuotetietojen sivuilla</span><span class="sxs-lookup"><span data-stu-id="8ad8b-139">Configure ratings and reviews modules on product details pages</span></span>

<span data-ttu-id="8ad8b-140">Lisätietoja luokitus- ja arvostelumoduulien määrittämisestä tuotetietojen sivuilla on kohdassa [Luokitus- ja arvostelumoduulit](ratings-reviews-modules.md).</span><span class="sxs-lookup"><span data-stu-id="8ad8b-140">For information on configuring ratings and reviews modules on product details pages, see [Ratings and reviews modules](ratings-reviews-modules.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8ad8b-141">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="8ad8b-141">Additional resources</span></span>

[<span data-ttu-id="8ad8b-142">Luokitukset ja arvostelut – yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="8ad8b-142">Ratings and reviews overview</span></span>](ratings-reviews-overview.md)

[<span data-ttu-id="8ad8b-143">Luokitusten ja arvostelujen käytön hyväksyminen</span><span class="sxs-lookup"><span data-stu-id="8ad8b-143">Opt in to use ratings and reviews</span></span>](opt-in-ratings-reviews.md)

[<span data-ttu-id="8ad8b-144">Hallitse luokituksia ja arvosteluja</span><span class="sxs-lookup"><span data-stu-id="8ad8b-144">Manage ratings and reviews</span></span>](manage-reviews.md)

[<span data-ttu-id="8ad8b-145">Luokitus- ja arvostelumoduulien määrittäminen tuotetietojen sivuilla</span><span class="sxs-lookup"><span data-stu-id="8ad8b-145">Configure ratings and reviews modules on product details pages</span></span>](ratings-reviews-modules.md)

[<span data-ttu-id="8ad8b-146">Tuoteluokitusten synkronoiminen Dynamics 365 Retailissa</span><span class="sxs-lookup"><span data-stu-id="8ad8b-146">Sync product ratings in Dynamics 365 Retail</span></span>](sync-product-ratings.md)
