---
title: Kuratoitujen suositusten manuaalinen luominen
description: Tässä ohje aiheessa kerrotaan, miten jälleenmyyjät voivat luoda ja hallita tuoteluetteloita Microsoft Dynamics 365 Commerce -sovelluksen asiakkaita varten.
author: bebeale
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 7dd9de055a020d7171aa2dea45714933b0987d49
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5207973"
---
# <a name="manually-create-curated-recommendations"></a><span data-ttu-id="4c9cb-103">Kuratoitujen suositusten manuaalinen luominen</span><span class="sxs-lookup"><span data-stu-id="4c9cb-103">Manually create curated recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="4c9cb-104">Tässä ohje aiheessa kerrotaan, miten jälleenmyyjät voivat luoda ja hallita tuotesuosituksia Microsoft Dynamics 365 Commerce -sovelluksen asiakkaita varten.</span><span class="sxs-lookup"><span data-stu-id="4c9cb-104">This topic explains how merchandizers can manually create and manage product recommendations lists for Microsoft Dynamics 365 Commerce customers.</span></span>

<span data-ttu-id="4c9cb-105">Kuratoidut luettelot ovat yksittäisen sellaisen sisällön kokoelmia, jonka ihmiset ovat luoneet ja jota he kuratoivat.</span><span class="sxs-lookup"><span data-stu-id="4c9cb-105">Curated lists are collections of individual content, created and curated by people.</span></span>  

## <a name="create-a-new-list"></a><span data-ttu-id="4c9cb-106">Uuden luettelon luominen</span><span class="sxs-lookup"><span data-stu-id="4c9cb-106">Create a new list</span></span>

<span data-ttu-id="4c9cb-107">Voit luoda uuden kuratoidun tuotesuositusluettelon seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="4c9cb-107">To create a curated product recommendation list, follow these steps.</span></span>

1. <span data-ttu-id="4c9cb-108">Siirry kohtaan **Retail ja Commerce &gt; Tuotesuositukset &gt; Suositusluettelot**.</span><span class="sxs-lookup"><span data-stu-id="4c9cb-108">Go to **Retail and Commerce &gt; Product recommendations &gt; Recommendation lists**.</span></span>
1. <span data-ttu-id="4c9cb-109">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="4c9cb-109">Select **New**.</span></span>
1. <span data-ttu-id="4c9cb-110">Anna **Luettelon tunnus** -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="4c9cb-110">In the **List Id** field, enter a value.</span></span>
1. <span data-ttu-id="4c9cb-111">Anna **Luettelon nimi** -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="4c9cb-111">In the **List name** field, enter a value.</span></span>
    - <span data-ttu-id="4c9cb-112">**Luettelon nimi** on sen luettelon otsikko, joka näkyy kuratoitujen luetteloiden osassa **Tuotekokoelma**-moduulissa.</span><span class="sxs-lookup"><span data-stu-id="4c9cb-112">The **List name** is the title of the list that will appear in the curated lists section of the **Product collection** module.</span></span>
1. <span data-ttu-id="4c9cb-113">Voit lisätä tuotteita luetteloon valitsemalla **Lisää tuotteita**.</span><span class="sxs-lookup"><span data-stu-id="4c9cb-113">To add products to the list, select **Add products**.</span></span>
1. <span data-ttu-id="4c9cb-114">Jos haluat muuttaa tuotteiden järjestystä luettelossa, kirjoita arvo **Näyttöjärjestys**-sarakkeeseen.</span><span class="sxs-lookup"><span data-stu-id="4c9cb-114">To change the order of the products in the list, enter a value in the **Display order** column.</span></span>
    - <span data-ttu-id="4c9cb-115">Jos kahdella tuotteilla on sama näyttöjärjestyksen arvo, näiden kahden tuloksen lopullinen järjestys voi poiketa taustasovelluksen järjestyksestä.</span><span class="sxs-lookup"><span data-stu-id="4c9cb-115">If two products have the same display order value, then the final order of those two results may differ from the back office.</span></span>
1. <span data-ttu-id="4c9cb-116">Tallenna luettelo valitsemalla **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="4c9cb-116">Select **Save** to save the list.</span></span>

## <a name="example-list"></a><span data-ttu-id="4c9cb-117">Esimerkkiluettelo</span><span class="sxs-lookup"><span data-stu-id="4c9cb-117">Example List</span></span>

![Esimerkki kuratoidusta luettelosta taustatoiminnossa](./media/examplecuratedrecolist.png)

## <a name="additional-resources"></a><span data-ttu-id="4c9cb-119">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="4c9cb-119">Additional resources</span></span>

[<span data-ttu-id="4c9cb-120">Tuotesuositusten yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="4c9cb-120">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="4c9cb-121">Azure Data Lake Storagen käyttöönotto Dynamics 365 Commerce -ympäristössä</span><span class="sxs-lookup"><span data-stu-id="4c9cb-121">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="4c9cb-122">Tuotesuositusten ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="4c9cb-122">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="4c9cb-123">Kohdennettujen suositusten ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="4c9cb-123">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="4c9cb-124">Kohdennetuista tuotesuosituksista kieltäytyminen</span><span class="sxs-lookup"><span data-stu-id="4c9cb-124">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="4c9cb-125">"Osta samankaltaisia tyylejä" -suositusten käyttöönotto</span><span class="sxs-lookup"><span data-stu-id="4c9cb-125">Enable "shop similar looks" recommendations</span></span>](shop-similar-looks.md)

[<span data-ttu-id="4c9cb-126">Tuotesuositusten lisääminen myyntipisteessä</span><span class="sxs-lookup"><span data-stu-id="4c9cb-126">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="4c9cb-127">Suositusten lisääminen tapahtumanäyttöön</span><span class="sxs-lookup"><span data-stu-id="4c9cb-127">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="4c9cb-128">AI-ML-suositusten tulosten muokkaaminen</span><span class="sxs-lookup"><span data-stu-id="4c9cb-128">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="4c9cb-129">Suositusten luominen esittelytietojen avulla</span><span class="sxs-lookup"><span data-stu-id="4c9cb-129">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="4c9cb-130">Tuotesuositukset – usein kysytyt kysymykset</span><span class="sxs-lookup"><span data-stu-id="4c9cb-130">Product recommendations FAQ</span></span>](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]