---
title: Ota tuotesuositukset käyttöön
description: Tässä ohjeaiheessa kerrotaa, miten tekoälyn koneoppimiseen perustuvia tuotesuosituksia voidaan tehdä Microsoft Dynamics 365 Commerce -asiakkaiden käyttöä varten.
author: bebeale
manager: AnnBe
ms.date: 10/1/2019
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
ms.openlocfilehash: ecda571a356c6968196d09cc19923105cf4544ab
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770136"
---
# <a name="enable-product-recommendations"></a><span data-ttu-id="b5a34-103">Ota tuotesuositukset käyttöön</span><span class="sxs-lookup"><span data-stu-id="b5a34-103">Enable product recommendations</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="b5a34-104">Tässä ohjeaiheessa kerrotaa, miten tekoälyn koneoppimiseen perustuvia tuotesuosituksia voidaan tehdä Microsoft Dynamics 365 Commerce -asiakkaiden käyttöä varten.</span><span class="sxs-lookup"><span data-stu-id="b5a34-104">This topic explains how to make product recommendations that are based on artificial intelligence-machine learning (AI-ML) available for Microsoft Dynamics 365 Commerce customers.</span></span> <span data-ttu-id="b5a34-105">Lisätietoja tuotesuositusten luetteloista on kohdassa [Tuotesuositusten yleiskatsaus](product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="b5a34-105">For more information about product recommendation lists, see [Product recommendations overview](product-recommendations.md).</span></span>

## <a name="recommendations-pre-check"></a><span data-ttu-id="b5a34-106">Suositusten esitarkistus</span><span class="sxs-lookup"><span data-stu-id="b5a34-106">Recommendations pre-check</span></span>
<span data-ttu-id="b5a34-107">Ota huomioon ennen käyttöönottoa, että tuotesuosituksia tuetaan vain F&O-asiakkaille, joilla on käytössä versio 10.0.6 ja jotka ovat siirtäneet tallennustilan käyttämään BDL-ratkaisua.</span><span class="sxs-lookup"><span data-stu-id="b5a34-107">Before enabling, please note that product recommendations are only supported for F&O customers supporting build 10.0.6 and have migrated their storage to using BDL.</span></span> 

<span data-ttu-id="b5a34-108">Varmista myös, että RetailSale-mittarit on otettu käyttöön.</span><span class="sxs-lookup"><span data-stu-id="b5a34-108">Additionally, ensure that RetailSale measurements have been enabled.</span></span> <span data-ttu-id="b5a34-109">Lisätietoja tästä määritysprosessista on [täällä.](https://docs.microsoft.com/en-us/dynamics365/ai/customer-insights/pm-measures)</span><span class="sxs-lookup"><span data-stu-id="b5a34-109">To Learn more about this set up process, go [here.](https://docs.microsoft.com/en-us/dynamics365/ai/customer-insights/pm-measures)</span></span>


## <a name="turn-on-recommendations"></a><span data-ttu-id="b5a34-110">Suositusten ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="b5a34-110">Turn on recommendations</span></span>

<span data-ttu-id="b5a34-111">Voit ottaa tuotesuositukset käyttöön noudattamalla seuraavia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="b5a34-111">To turn on product recommendations, follow these steps.</span></span>

1. <span data-ttu-id="b5a34-112">Siirry kohtaan **Retail** &gt; **Tuotesuositukset** &gt; **Suositusparametrit**.</span><span class="sxs-lookup"><span data-stu-id="b5a34-112">Go to **Retail** &gt; **Product recommendations** &gt; **Recommendation parameters**.</span></span>
1. <span data-ttu-id="b5a34-113">Valitse vähittäismyynnin jaettujen parametrien luettelossa **Suositusluettelot**.</span><span class="sxs-lookup"><span data-stu-id="b5a34-113">In the list of retail shared parameters, select **Recommendation Lists**.</span></span>
1. <span data-ttu-id="b5a34-114">Määritä **Ota suositukset käyttöön** -asetukseksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="b5a34-114">Set the **Enable recommendations** option to **Yes**.</span></span>

![ota tuotesuositukset käyttöön](./media/enableproductrecommendations.png)

> [!NOTE]
> <span data-ttu-id="b5a34-116">Tämä menettely käynnistää tuotesuositusluetteloiden luontiprosessin.</span><span class="sxs-lookup"><span data-stu-id="b5a34-116">This procedure starts the process of generating product recommendation lists.</span></span> <span data-ttu-id="b5a34-117">Luetteloiden luominen, niiden saaminen käyttöön ja näkyminen myyntipisteessä tai Dynamics 365 for Commerce -sovelluksessa voi kestää useita tunteja.</span><span class="sxs-lookup"><span data-stu-id="b5a34-117">Up to several hours might be required before the lists are available and can be seen at the point of sale (POS) or in Dynamics 365 for Commerce.</span></span>

## <a name="configure-recommendation-list-parameters"></a><span data-ttu-id="b5a34-118">Suositusluettelon parametrien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="b5a34-118">Configure recommendation list parameters</span></span>
<span data-ttu-id="b5a34-119">Oletusarvoisesti tekoälyyn perustuva tuotesuositusluettelo sisältää ehdotetut arvot.</span><span class="sxs-lookup"><span data-stu-id="b5a34-119">By default, the AI-ML-based product recommendation list provides suggested values.</span></span> <span data-ttu-id="b5a34-120">Voit muuttaa ehdotettuja oletusarvoja haluamallasi tavalla.</span><span class="sxs-lookup"><span data-stu-id="b5a34-120">You can change the default suggested values to suit the flow of your business.</span></span> <span data-ttu-id="b5a34-121">Lisätietoja oletusparametrien muuttamisesta on kohdassa [Tekoälyn koneoppimiseen perustuvan tuotesuositusluettelon hallinta](modify-product-recommendation-results.md).</span><span class="sxs-lookup"><span data-stu-id="b5a34-121">To learn more about how to change the default parameters, go to [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>

## <a name="show-recommendations-on-pos-devices"></a><span data-ttu-id="b5a34-122">Suositusten näyttäminen myyntipistelaitteissa</span><span class="sxs-lookup"><span data-stu-id="b5a34-122">Show recommendations on POS devices</span></span>
<span data-ttu-id="b5a34-123">Kun suositukset on otettu käyttöön taustatoiminnossa, suosituspaneeli on lisättävä ohjausobjektin myyntipistenäyttöön asettelutyökalun avulla.</span><span class="sxs-lookup"><span data-stu-id="b5a34-123">After enabling recommendations in the back office, the recommendations pannel must be added to the control POS screen via the layout tool.</span></span> <span data-ttu-id="b5a34-124">Lisätietoja tästä prosessista on [täällä.](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/add-recommendations-control-pos-screen)</span><span class="sxs-lookup"><span data-stu-id="b5a34-124">To learn about this process, go [here.](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/add-recommendations-control-pos-screen)</span></span>


## <a name="additional-resources"></a><span data-ttu-id="b5a34-125">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="b5a34-125">Additional resources</span></span>

[<span data-ttu-id="b5a34-126">Tuotesuositusten yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="b5a34-126">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="b5a34-127">Tuotesuositusluetteloiden lisääminen sivuille</span><span class="sxs-lookup"><span data-stu-id="b5a34-127">Add product recommendation lists to pages</span></span>](add-reco-list-to-page.md)

[<span data-ttu-id="b5a34-128">Suositusten paneelin lisääminen myyntipistelaitteisiin</span><span class="sxs-lookup"><span data-stu-id="b5a34-128">Add recommendations panel to POS devices</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/add-recommendations-control-pos-screen)


