---
title: Ota tuotesuositukset käyttöön
description: Tässä ohjeaiheessa kerrotaa, miten tekoälyn koneoppimiseen perustuvia tuotesuosituksia voidaan tehdä Microsoft Dynamics 365 Commerce -asiakkaiden käyttöä varten.
author: bebeale
manager: AnnBe
ms.date: 03/12/2020
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
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 879fccb063ca0b74e0f022a9edf6a15f7d1311ae
ms.sourcegitcommit: 1e7e7c4bc197b0a42e4d53d2a54600a2fb125b69
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/13/2020
ms.locfileid: "3127879"
---
# <a name="enable-product-recommendations"></a><span data-ttu-id="e9070-103">Ota tuotesuositukset käyttöön</span><span class="sxs-lookup"><span data-stu-id="e9070-103">Enable product recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e9070-104">Tässä ohjeaiheessa kerrotaa, miten tekoälyn koneoppimiseen perustuvia tuotesuosituksia voidaan tehdä Microsoft Dynamics 365 Commerce -asiakkaiden käyttöä varten.</span><span class="sxs-lookup"><span data-stu-id="e9070-104">This topic explains how to make product recommendations that are based on artificial intelligence-machine learning (AI-ML) available for Microsoft Dynamics 365 Commerce customers.</span></span> <span data-ttu-id="e9070-105">Lisätietoja tuotesuositusten luetteloista on kohdassa [Tuotesuositusten yleiskatsaus](product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="e9070-105">For more information about product recommendation lists, see [Product recommendations overview](product-recommendations.md).</span></span>

## <a name="recommendations-pre-check"></a><span data-ttu-id="e9070-106">Suositusten esitarkistus</span><span class="sxs-lookup"><span data-stu-id="e9070-106">Recommendations pre-check</span></span>

<span data-ttu-id="e9070-107">Ota huomioon ennen käyttöönottoa, että tuotesuosituksia tuetaan vain Commerce-asiakkaille, jotka ovat siirtäneet tallennustilansa Azure Data Lake Storagea (ADLS:ää) käyttäen.</span><span class="sxs-lookup"><span data-stu-id="e9070-107">Before enabling, please note that product recommendations are only supported for Commerce customers who have migrated their storage to using Azure Data Lake Storage (ADLS).</span></span> 

<span data-ttu-id="e9070-108">Katso ADLS:n käyttöönoton vaiheet kohdasta [ADLS:n käyttöönotto Dynamics 365 -ympäristössä](enable-ADLS-environment.md).</span><span class="sxs-lookup"><span data-stu-id="e9070-108">For steps on enabling ADLS, see [How to enable ADLS in a Dynamics 365 environment](enable-ADLS-environment.md).</span></span>

<span data-ttu-id="e9070-109">Varmista myös, että RetailSale-mittarit on otettu käyttöön.</span><span class="sxs-lookup"><span data-stu-id="e9070-109">Additionally, ensure that RetailSale measurements have been enabled.</span></span> <span data-ttu-id="e9070-110">Lisätietoja tästä määritysprosessista on [täällä.](https://docs.microsoft.com/dynamics365/ai/customer-insights/pm-measures)</span><span class="sxs-lookup"><span data-stu-id="e9070-110">To learn more about this set up process, go [here.](https://docs.microsoft.com/dynamics365/ai/customer-insights/pm-measures)</span></span>


## <a name="turn-on-recommendations"></a><span data-ttu-id="e9070-111">Suositusten ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="e9070-111">Turn on recommendations</span></span>

<span data-ttu-id="e9070-112">Voit ottaa tuotesuositukset käyttöön noudattamalla seuraavia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="e9070-112">To turn on product recommendations, follow these steps.</span></span>

1. <span data-ttu-id="e9070-113">Siirry kohtaan **Retail ja Commerce &gt; Tuotesuositukset &gt; Suositusparametrit**.</span><span class="sxs-lookup"><span data-stu-id="e9070-113">Go to **Retail and Commerce &gt; Product recommendations &gt; Recommendation parameters**.</span></span>
1. <span data-ttu-id="e9070-114">Valitse jaettujen parametrien luettelossa **Suositusluettelot**.</span><span class="sxs-lookup"><span data-stu-id="e9070-114">In the list of shared parameters, select **Recommendation Lists**.</span></span>
1. <span data-ttu-id="e9070-115">Määritä **Ota suositukset käyttöön** -asetukseksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="e9070-115">Set the **Enable recommendations** option to **Yes**.</span></span>

![ota tuotesuositukset käyttöön](./media/enableproductrecommendations.png)

> [!NOTE]
> <span data-ttu-id="e9070-117">Tämä menettely käynnistää tuotesuositusluetteloiden luontiprosessin.</span><span class="sxs-lookup"><span data-stu-id="e9070-117">This procedure starts the process of generating product recommendation lists.</span></span> <span data-ttu-id="e9070-118">Luetteloiden luominen, niiden saaminen käyttöön ja näkyminen myyntipisteessä tai Dynamics 365 Commerce -sovelluksessa voi kestää useita tunteja.</span><span class="sxs-lookup"><span data-stu-id="e9070-118">Up to several hours might be required before the lists are available and can be seen at the point of sale (POS) or in Dynamics 365 Commerce.</span></span>

## <a name="configure-recommendation-list-parameters"></a><span data-ttu-id="e9070-119">Suositusluettelon parametrien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="e9070-119">Configure recommendation list parameters</span></span>

<span data-ttu-id="e9070-120">Oletusarvoisesti tekoälyyn perustuva tuotesuositusluettelo sisältää ehdotetut arvot.</span><span class="sxs-lookup"><span data-stu-id="e9070-120">By default, the AI-ML-based product recommendation list provides suggested values.</span></span> <span data-ttu-id="e9070-121">Voit muuttaa ehdotettuja oletusarvoja haluamallasi tavalla.</span><span class="sxs-lookup"><span data-stu-id="e9070-121">You can change the default suggested values to suit the flow of your business.</span></span> <span data-ttu-id="e9070-122">Lisätietoja oletusparametrien muuttamisesta on kohdassa [Tekoälyn koneoppimiseen perustuvan tuotesuositusluettelon hallinta](modify-product-recommendation-results.md).</span><span class="sxs-lookup"><span data-stu-id="e9070-122">To learn more about how to change the default parameters, go to [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>

## <a name="show-recommendations-on-pos-devices"></a><span data-ttu-id="e9070-123">Suositusten näyttäminen myyntipistelaitteissa</span><span class="sxs-lookup"><span data-stu-id="e9070-123">Show recommendations on POS devices</span></span>

<span data-ttu-id="e9070-124">Kun suositukset on otettu käyttöön Commercen taustatoiminnossa, suosituspaneeli on lisättävä ohjausobjektin myyntipistenäyttöön asettelutyökalun avulla.</span><span class="sxs-lookup"><span data-stu-id="e9070-124">After enabling recommendations in Commerce back office, the recommendations panel must be added to the control POS screen using the layout tool.</span></span> <span data-ttu-id="e9070-125">Lisä tietoja tästä prosessista on kohdassa [Suositusten ohjausobjektin lisääminen myyntipisteen laitteen tapahtumaruudulle](add-recommendations-control-pos-screen.md).</span><span class="sxs-lookup"><span data-stu-id="e9070-125">To learn about this process, see [Add a recommendations control to the transaction screen on POS devices](add-recommendations-control-pos-screen.md).</span></span> 

## <a name="enable-personalized-recommendations"></a><span data-ttu-id="e9070-126">Ota käyttöön kohdennetut tuotesuositukset</span><span class="sxs-lookup"><span data-stu-id="e9070-126">Enable personalized recommendations</span></span>

<span data-ttu-id="e9070-127">Lisätietoja mukautettujen suositusten vastaanottamisesta on kohdassa [Mukautettujen suositusten ottaminen käyttöön](personalized-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="e9070-127">To learn more about how to receive personalized recommendations, see [Enable personalized recommendations](personalized-recommendations.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e9070-128">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="e9070-128">Additional resources</span></span>

[<span data-ttu-id="e9070-129">Tuotesuositusten yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="e9070-129">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="e9070-130">ADLS:n käyttöönotto Dynamics 365 Commerce -ympäristössä</span><span class="sxs-lookup"><span data-stu-id="e9070-130">Enable ADLS in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="e9070-131">Ota kohdennetut suositukset käyttöön</span><span class="sxs-lookup"><span data-stu-id="e9070-131">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="e9070-132">Kohdennetuista tuotesuosituksista kieltäytyminen</span><span class="sxs-lookup"><span data-stu-id="e9070-132">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="e9070-133">Suositusluettelojen lisääminen sähköisen kaupankäynnin sivustoon</span><span class="sxs-lookup"><span data-stu-id="e9070-133">Add recommendation lists to an e-Commerce site</span></span>](add-reco-list-to-page.md)

[<span data-ttu-id="e9070-134">Tuotesuositusten lisääminen myyntipisteessä</span><span class="sxs-lookup"><span data-stu-id="e9070-134">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="e9070-135">Suositusten lisääminen tapahtumanäyttöön</span><span class="sxs-lookup"><span data-stu-id="e9070-135">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="e9070-136">AI-ML-suositusten tulosten muokkaaminen</span><span class="sxs-lookup"><span data-stu-id="e9070-136">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="e9070-137">Kuratoitujen suositusten manuaalinen luominen</span><span class="sxs-lookup"><span data-stu-id="e9070-137">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="e9070-138">Suositusten luominen esittelytietojen avulla</span><span class="sxs-lookup"><span data-stu-id="e9070-138">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="e9070-139">Tuotesuositukset – usein kysytyt kysymykset</span><span class="sxs-lookup"><span data-stu-id="e9070-139">Product recommendations FAQ</span></span>](faq-recommendations.md)

