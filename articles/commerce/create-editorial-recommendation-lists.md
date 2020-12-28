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
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 9826785700dcc1a35e6199b7aeff4e06b6d9da39
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4411973"
---
# <a name="manually-create-curated-recommendations"></a><span data-ttu-id="f718d-103">Kuratoitujen suositusten manuaalinen luominen</span><span class="sxs-lookup"><span data-stu-id="f718d-103">Manually create curated recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="f718d-104">Tässä ohje aiheessa kerrotaan, miten jälleenmyyjät voivat luoda ja hallita tuotesuositusluetteloita Microsoft Dynamics 365 Commerce -sovelluksen asiakkaita varten.</span><span class="sxs-lookup"><span data-stu-id="f718d-104">This topic explains how merchandizers can manually create and manage product recommendations lists for Microsoft Dynamics 365 Commerce customers.</span></span>

<span data-ttu-id="f718d-105">Kuratoidut luettelot ovat yksittäisen sellaisen sisällön kokoelmia, jonka ihmiset ovat luoneet ja jota he kuratoivat.</span><span class="sxs-lookup"><span data-stu-id="f718d-105">Curated lists are collections of individual content, created and curated by people.</span></span>  

## <a name="create-a-new-list"></a><span data-ttu-id="f718d-106">Uuden luettelon luominen</span><span class="sxs-lookup"><span data-stu-id="f718d-106">Create a new list</span></span>

<span data-ttu-id="f718d-107">Voit luoda uuden kuratoidun tuotesuositusluettelon seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="f718d-107">To create a curated product recommendation list, follow these steps.</span></span>

1. <span data-ttu-id="f718d-108">Siirry kohtaan **Retail ja Commerce &gt; Tuotesuositukset &gt; Suositusluettelot**.</span><span class="sxs-lookup"><span data-stu-id="f718d-108">Go to **Retail and Commerce &gt; Product recommendations &gt; Recommendation lists**.</span></span>
1. <span data-ttu-id="f718d-109">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="f718d-109">Select **New**.</span></span>
1. <span data-ttu-id="f718d-110">Anna **Luettelon tunnus** -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="f718d-110">In the **List Id** field, enter a value.</span></span>
1. <span data-ttu-id="f718d-111">Anna **Luettelon nimi** -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="f718d-111">In the **List name** field, enter a value.</span></span>
    - <span data-ttu-id="f718d-112">**Luettelon nimi** on sen luettelon otsikko, joka näkyy kuratoitujen luetteloiden osassa **Tuotekokoelma**-moduulissa.</span><span class="sxs-lookup"><span data-stu-id="f718d-112">The **List name** is the title of the list that will appear in the curated lists section of the **Product collection** module.</span></span>
1. <span data-ttu-id="f718d-113">Voit lisätä tuotteita luetteloon valitsemalla **Lisää tuotteita**.</span><span class="sxs-lookup"><span data-stu-id="f718d-113">To add products to the list, select **Add products**.</span></span>
1. <span data-ttu-id="f718d-114">Jos haluat muuttaa tuotteiden järjestystä luettelossa, kirjoita arvo **Näyttöjärjestys**-sarakkeeseen.</span><span class="sxs-lookup"><span data-stu-id="f718d-114">To change the order of the products in the list, enter a value in the **Display order** column.</span></span>
    - <span data-ttu-id="f718d-115">Jos kahdella tuotteilla on sama näyttöjärjestyksen arvo, näiden kahden tuloksen lopullinen järjestys voi poiketa taustasovelluksen järjestyksestä.</span><span class="sxs-lookup"><span data-stu-id="f718d-115">If two products have the same display order value, then the final order of those two results may differ from the back office.</span></span>
1. <span data-ttu-id="f718d-116">Tallenna luettelo valitsemalla **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="f718d-116">Select **Save** to save the list.</span></span>

## <a name="example-list"></a><span data-ttu-id="f718d-117">Esimerkkiluettelo</span><span class="sxs-lookup"><span data-stu-id="f718d-117">Example List</span></span>

![Esimerkki kuratoidusta luettelosta taustatoiminnossa](./media/examplecuratedrecolist.png)

## <a name="additional-resources"></a><span data-ttu-id="f718d-119">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="f718d-119">Additional resources</span></span>

[<span data-ttu-id="f718d-120">Tuotesuositusten yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="f718d-120">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="f718d-121">Azure Data Lake Storagen käyttöönotto Dynamics 365 Commerce -ympäristössä</span><span class="sxs-lookup"><span data-stu-id="f718d-121">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="f718d-122">Tuotesuositusten ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="f718d-122">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="f718d-123">Kohdennettujen suositusten ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="f718d-123">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="f718d-124">Kohdennetuista tuotesuosituksista kieltäytyminen</span><span class="sxs-lookup"><span data-stu-id="f718d-124">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="f718d-125">"Osta samankaltaisia tyylejä" -suositusten käyttöönotto</span><span class="sxs-lookup"><span data-stu-id="f718d-125">Enable "shop similar looks" recommendations</span></span>](shop-similar-looks.md)

[<span data-ttu-id="f718d-126">Tuotesuositusten lisääminen myyntipisteessä</span><span class="sxs-lookup"><span data-stu-id="f718d-126">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="f718d-127">Suositusten lisääminen tapahtumanäyttöön</span><span class="sxs-lookup"><span data-stu-id="f718d-127">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="f718d-128">AI-ML-suositusten tulosten muokkaaminen</span><span class="sxs-lookup"><span data-stu-id="f718d-128">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="f718d-129">Suositusten luominen esittelytietojen avulla</span><span class="sxs-lookup"><span data-stu-id="f718d-129">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="f718d-130">Tuotesuositukset – usein kysytyt kysymykset</span><span class="sxs-lookup"><span data-stu-id="f718d-130">Product recommendations FAQ</span></span>](faq-recommendations.md)
