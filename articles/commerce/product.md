---
title: Tuotesuositusten lisääminen myyntipisteessä
description: Tässä ohjeaiheessa kuvataan myyntipisteen (POS) tuotesuositusten käyttöä.
author: bebeale
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 259664
ms.assetid: 5dd8db08-cd96-4f7e-9e65-b05ca815d580
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 7afe9225b8fc966ca154a5eb7421e8d4cc7c3023
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4412081"
---
# <a name="add-product-recommendations-on-pos"></a><span data-ttu-id="5c5c1-103">Tuotesuositusten lisääminen myyntipisteessä</span><span class="sxs-lookup"><span data-stu-id="5c5c1-103">Add product recommendations on POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="5c5c1-104">Tuotesuositukset ovat uudistava yrityssovellus, joka ulottuu kaikkiin kaupan tiloihin monipuolisten, sitouttavien ja räätälöityjen tuotteiden löytämisen kokemusten luomiseksi.</span><span class="sxs-lookup"><span data-stu-id="5c5c1-104">At its core, product recommendations are a transformative business application that span across all commerce spaces to create rich, engaging, and tailored product discovery experiences.</span></span> <span data-ttu-id="5c5c1-105">Jos haluat ottaa tämän toiminnon käyttöön myyntipisteessä, noudata ohjeita [Suositusten lisääminen POS-laitteisiin.](add-recommendations-control-pos-screen.md)</span><span class="sxs-lookup"><span data-stu-id="5c5c1-105">To implement this feature on POS, follow the steps on [how to add recommendations to your POS devices.](add-recommendations-control-pos-screen.md)</span></span> 

<span data-ttu-id="5c5c1-106">Lisätietoja tuotesuositusominaisuuksista on kohdassa [Tuotesuositusten yleiskatsaus](../commerce/product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="5c5c1-106">For more information about product recommendations features, read the [product recommendations overview.](../commerce/product-recommendations.md)</span></span> 

## <a name="scenarios"></a><span data-ttu-id="5c5c1-107">Skenaariot</span><span class="sxs-lookup"><span data-stu-id="5c5c1-107">Scenarios</span></span>

<span data-ttu-id="5c5c1-108">Tuotteen suosituksia on käytössä seuraavissa myyntipisteskenaarioissa.</span><span class="sxs-lookup"><span data-stu-id="5c5c1-108">Product recommendations are enabled for the following POS scenarios.</span></span> <span data-ttu-id="5c5c1-109">Ne ovat saatavissa Cloud POS - ja Modern POS (MPOS) -myyntipisteissä.</span><span class="sxs-lookup"><span data-stu-id="5c5c1-109">They are available in Cloud POS or Modern POS (MPOS).</span></span>

1. <span data-ttu-id="5c5c1-110">**Tuotteen tiedot** -sivulla:</span><span class="sxs-lookup"><span data-stu-id="5c5c1-110">On the **Product details** page:</span></span>

    - <span data-ttu-id="5c5c1-111">Jos myyjä käy **Tuotteen tiedot** -sivulla tarkastellessaan aiempia tapahtumia eri kanavissa, suosituspalvelu ehdottaa muita nimikkeitä, jotka todennäköisesti voi ostaa yhdessä.</span><span class="sxs-lookup"><span data-stu-id="5c5c1-111">If a store associate visits a **Product details** page when looking at previous transactions across different channels, the recommendations service suggests additional items that are likely to be purchased together.</span></span>

    <span data-ttu-id="5c5c1-112">[![Tuotetiedot-sivun suositukset](./media/proddetails.png)](./media/proddetails.png)</span><span class="sxs-lookup"><span data-stu-id="5c5c1-112">[![Recommendations on the Product details page](./media/proddetails.png)](./media/proddetails.png)</span></span>

2. <span data-ttu-id="5c5c1-113">**Tapahtuma**-sivulla:</span><span class="sxs-lookup"><span data-stu-id="5c5c1-113">On the **Transaction** page:</span></span>

    - <span data-ttu-id="5c5c1-114">Suositusmoduuli ehdottaa nimikkeitä, jotka perustuvat niiden korissa olevien nimikkeiden luetteloon, jotka ostetaan usein yhdessä.</span><span class="sxs-lookup"><span data-stu-id="5c5c1-114">The recommendation engine suggests items based on the entire list of items in the basket that are frequently bought together.</span></span>

    > [!NOTE]
    > <span data-ttu-id="5c5c1-115">Jotta suositukset voitaisiin näyttää **Tapahtuma**-sivulla, vähittäismyyjän pitää päivittää näytön asettelu Dynamics 365 Commerceissa.</span><span class="sxs-lookup"><span data-stu-id="5c5c1-115">To display recommendations on the **Transaction** page, the retailer needs to update the screen layout in Dynamics 365 Commerce.</span></span> <span data-ttu-id="5c5c1-116">**Suositukset**-ohjausobjekti on pudotettava **Tapahtuma**-sivulle.</span><span class="sxs-lookup"><span data-stu-id="5c5c1-116">The **Recommendations** control must be dropped onto the **Transaction** page.</span></span>

    <span data-ttu-id="5c5c1-117">[![Tapahtumasivun suositukset](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)</span><span class="sxs-lookup"><span data-stu-id="5c5c1-117">[![Recommendations on the Transaction page](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)</span></span>

## <a name="configure-commerce-to-enable-pos-recommendations"></a><span data-ttu-id="5c5c1-118">Commercen määrittäminen ottamaan käyttöön myyntipisteen suositukset</span><span class="sxs-lookup"><span data-stu-id="5c5c1-118">Configure Commerce to enable POS recommendations</span></span>

<span data-ttu-id="5c5c1-119">Voit määrittää tuotesuositukset noudattamalla seuraavia ohjeita:</span><span class="sxs-lookup"><span data-stu-id="5c5c1-119">To set up product recommendations, follow these steps:</span></span>

1. <span data-ttu-id="5c5c1-120">Varmista, että palvelu on päivitetty **10.0.6-versioon.**</span><span class="sxs-lookup"><span data-stu-id="5c5c1-120">Ensure your service has been updated to the **10.0.6 build.**</span></span>
2. <span data-ttu-id="5c5c1-121">Noudata ohjeita: [tuotesuositusten käyttöönotto](../commerce/enable-product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="5c5c1-121">Follow the instructions on how to [enable product recommendations](../commerce/enable-product-recommendations.md) for your business.</span></span>
3. <span data-ttu-id="5c5c1-122">Valinnainen: Jos haluat näyttää suositukset Tapahtuma-näytössä, siirry kohtaan **Näytön asettelu**, valitse näyttöasettelu, käynnistä **Näytön asettelun suunnittelutoiminto** ja pudota **Suositukset**-ohjausobjekti haluamaasi paikkaan.</span><span class="sxs-lookup"><span data-stu-id="5c5c1-122">Optional: To display recommendations on the transaction screen, go to **Screen Layout**, choose your screen layout, launch the **Screen layout designer**, and then drop the **recommendations** control where needed.</span></span>
4. <span data-ttu-id="5c5c1-123">Siirry kohtaan **Commercen parametrit**, valitse **Automaattianalyysipalvelut** ja valitse **Kyllä** kohdassa **Ota käyttöön myyntipisteen suositukset**.</span><span class="sxs-lookup"><span data-stu-id="5c5c1-123">Go to **Commerce parameters**, select **Machine-learning**, select **Yes** under **Enable POS recommendations**.</span></span>
5. <span data-ttu-id="5c5c1-124">Saat suositukset näkyviin myyntipisteessä suorittamalla yleisen konfiguraatiotyön **1110**.</span><span class="sxs-lookup"><span data-stu-id="5c5c1-124">To see recommendations on POS, run global configuration job **1110**.</span></span> <span data-ttu-id="5c5c1-125">Saat myyntipisteen näytön asetteluun tehdyt muutokset näkyviin suorittamalla kanavan konfigurointityön **1070**.</span><span class="sxs-lookup"><span data-stu-id="5c5c1-125">To reflect changes made to POS screen layout designer, run channel configuration job **1070**.</span></span>

## <a name="troubleshoot-issues-where-you-have-product-recommendations-already-enabled"></a><span data-ttu-id="5c5c1-126">Jo käyttöönotettuihin tuotesuosituksiin liittyvien ongelmien vianmääritys</span><span class="sxs-lookup"><span data-stu-id="5c5c1-126">Troubleshoot issues where you have Product recommendations already enabled</span></span>

- <span data-ttu-id="5c5c1-127">Valitse **Commercen parametrit** \> **Suositusluettelot** \> **Poista tuotesuositukset käytöstä** ja suorita **Yleinen konfiguraatiotyö \[9999\]**.</span><span class="sxs-lookup"><span data-stu-id="5c5c1-127">Navigate to **Commerce Parameters** \> **Recommendation lists** \> **Disable product recommendations** and run **Global configuration job \[9999\]**.</span></span> 
- <span data-ttu-id="5c5c1-128">Jos lisäsit **suositusten ohjausobjektin** tapahtumanäyttöön **näytön asettelun suunnittelutoiminnolla**, poista myös se.</span><span class="sxs-lookup"><span data-stu-id="5c5c1-128">If you added the **Recommendations control** to your transaction screen using the **Screen layout designer**, please remove that as well.</span></span>
- <span data-ttu-id="5c5c1-129">Jos sinulla on lisäkysymyksiä, lisätietoja kohdassa [Tuotesuositusten usein kysytyt kysymykset](../commerce/faq-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="5c5c1-129">If you have additional questions, check out the [Product recommendations FAQ](../commerce/faq-recommendations.md) for more information.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5c5c1-130">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="5c5c1-130">Additional resources</span></span>

[<span data-ttu-id="5c5c1-131">Tuotesuositusten yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="5c5c1-131">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="5c5c1-132">Azure Data Lake Storagen käyttöönotto Dynamics 365 Commerce -ympäristössä</span><span class="sxs-lookup"><span data-stu-id="5c5c1-132">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="5c5c1-133">Tuotesuositusten ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="5c5c1-133">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="5c5c1-134">Kohdennettujen suositusten ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="5c5c1-134">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="5c5c1-135">Kohdennetuista tuotesuosituksista kieltäytyminen</span><span class="sxs-lookup"><span data-stu-id="5c5c1-135">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="5c5c1-136">"Osta samankaltaisia tyylejä" -suositusten käyttöönotto</span><span class="sxs-lookup"><span data-stu-id="5c5c1-136">Enable "shop similar looks" recommendations</span></span>](shop-similar-looks.md)

[<span data-ttu-id="5c5c1-137">Suositusten lisääminen tapahtumanäyttöön</span><span class="sxs-lookup"><span data-stu-id="5c5c1-137">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="5c5c1-138">AI-ML-suositusten tulosten muokkaaminen</span><span class="sxs-lookup"><span data-stu-id="5c5c1-138">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="5c5c1-139">Kuratoitujen suositusten manuaalinen luominen</span><span class="sxs-lookup"><span data-stu-id="5c5c1-139">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="5c5c1-140">Suositusten luominen esittelytietojen avulla</span><span class="sxs-lookup"><span data-stu-id="5c5c1-140">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="5c5c1-141">Tuotesuositukset – usein kysytyt kysymykset</span><span class="sxs-lookup"><span data-stu-id="5c5c1-141">Product recommendations FAQ</span></span>](faq-recommendations.md)
