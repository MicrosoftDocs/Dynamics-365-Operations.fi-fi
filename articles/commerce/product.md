---
title: Myyntipisteen tuotesuositukset
description: Tässä ohjeaiheessa kuvataan myyntipisteen (POS) tuotesuositusten käyttöä.
author: bebeale
manager: AnnBe
ms.date: 10/01/19
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
ms.openlocfilehash: bfb13904b774558907b29e74158b1e0a193e17cd
ms.sourcegitcommit: 12b9d6f2dd24e52e46487748c848864909af6967
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/14/2020
ms.locfileid: "3057438"
---
# <a name="product-recommendations-on-pos"></a><span data-ttu-id="8e617-103">Tuotesuositukset myyntipisteessä</span><span class="sxs-lookup"><span data-stu-id="8e617-103">Product recommendations on POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="8e617-104">Tuotesuositukset ovat uudistava yrityssovellus, joka ulottuu kaikkiin kaupan tiloihin monipuolisten, sitouttavien ja räätälöityjen tuotteiden löytämisen kokemusten luomiseksi.</span><span class="sxs-lookup"><span data-stu-id="8e617-104">At its core, product recommendations are a transformative business application that span across all commerce spaces to create rich, engaging, and tailored product discovery experiences.</span></span> <span data-ttu-id="8e617-105">Jos haluat ottaa tämän toiminnon käyttöön myyntipisteessä, noudata ohjeita [Suositusten lisääminen POS-laitteisiin.](add-recommendations-control-pos-screen.md)</span><span class="sxs-lookup"><span data-stu-id="8e617-105">To implement this feature on POS, follow the steps on [how to add recommendations to your POS devices.](add-recommendations-control-pos-screen.md)</span></span> 

<span data-ttu-id="8e617-106">Lisätietoja tuotesuositusominaisuuksista on kohdassa [Tuotesuositusten yleiskatsaus](../commerce/product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="8e617-106">For more information about product recommendations features, read the [product recommendations overview.](../commerce/product-recommendations.md)</span></span> 

## <a name="scenarios"></a><span data-ttu-id="8e617-107">Skenaariot</span><span class="sxs-lookup"><span data-stu-id="8e617-107">Scenarios</span></span>

<span data-ttu-id="8e617-108">Tuotteen suosituksia on käytössä seuraavissa myyntipisteskenaarioissa.</span><span class="sxs-lookup"><span data-stu-id="8e617-108">Product recommendations are enabled for the following POS scenarios.</span></span> <span data-ttu-id="8e617-109">Ne ovat saatavissa Cloud POS - ja Modern POS (MPOS) -myyntipisteissä.</span><span class="sxs-lookup"><span data-stu-id="8e617-109">They are available in Cloud POS or Modern POS (MPOS).</span></span>

1. <span data-ttu-id="8e617-110">**Tuotteen tiedot** -sivulla:</span><span class="sxs-lookup"><span data-stu-id="8e617-110">On the **Product details** page:</span></span>

    - <span data-ttu-id="8e617-111">Jos myyjä käy **Tuotteen tiedot** -sivulla tarkastellessaan aiempia tapahtumia eri kanavissa, suosituspalvelu ehdottaa muita nimikkeitä, jotka todennäköisesti voi ostaa yhdessä.</span><span class="sxs-lookup"><span data-stu-id="8e617-111">If a store associate visits a **Product details** page when looking at previous transactions across different channels, the recommendations service suggests additional items that are likely to be purchased together.</span></span>

    <span data-ttu-id="8e617-112">[![Tuotetiedot-sivun suositukset](./media/proddetails.png)](./media/proddetails.png)</span><span class="sxs-lookup"><span data-stu-id="8e617-112">[![Recommendations on the Product details page](./media/proddetails.png)](./media/proddetails.png)</span></span>

2. <span data-ttu-id="8e617-113">**Tapahtuma**-sivulla:</span><span class="sxs-lookup"><span data-stu-id="8e617-113">On the **Transaction** page:</span></span>

    - <span data-ttu-id="8e617-114">Suositusmoduuli ehdottaa nimikkeitä, jotka perustuvat niiden korissa olevien nimikkeiden luetteloon, jotka ostetaan usein yhdessä.</span><span class="sxs-lookup"><span data-stu-id="8e617-114">The recommendation engine suggests items based on the entire list of items in the basket that are frequently bought together.</span></span>

    > [!NOTE]
    > <span data-ttu-id="8e617-115">Jotta suositukset voitaisiin näyttää **Tapahtuma**-sivulla, vähittäismyyjän pitää päivittää näytön asettelu Dynamics 365 Commerceissa.</span><span class="sxs-lookup"><span data-stu-id="8e617-115">To display recommendations on the **Transaction** page, the retailer needs to update the screen layout in Dynamics 365 Commerce.</span></span> <span data-ttu-id="8e617-116">**Suositukset**-ohjausobjekti on pudotettava **Tapahtuma**-sivulle.</span><span class="sxs-lookup"><span data-stu-id="8e617-116">The **Recommendations** control must be dropped onto the **Transaction** page.</span></span>

    <span data-ttu-id="8e617-117">[![Tapahtumasivun suositukset](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)</span><span class="sxs-lookup"><span data-stu-id="8e617-117">[![Recommendations on the Transaction page](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)</span></span>

## <a name="configure-commerce-to-enable-pos-recommendations"></a><span data-ttu-id="8e617-118">Commercen määrittäminen ottamaan käyttöön myyntipisteen suositukset</span><span class="sxs-lookup"><span data-stu-id="8e617-118">Configure Commerce to enable POS recommendations</span></span>

<span data-ttu-id="8e617-119">Voit määrittää tuotesuositukset noudattamalla seuraavia ohjeita:</span><span class="sxs-lookup"><span data-stu-id="8e617-119">To set up product recommendations, follow these steps:</span></span>

1. <span data-ttu-id="8e617-120">Varmista, että palvelu on päivitetty **10.0.6-versioon.**</span><span class="sxs-lookup"><span data-stu-id="8e617-120">Ensure your service has been updated to the **10.0.6 build.**</span></span>
2. <span data-ttu-id="8e617-121">Noudata ohjeita: [tuotesuositusten käyttöönotto](../commerce/enable-product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="8e617-121">Follow the instructions on how to [enable product recommendations](../commerce/enable-product-recommendations.md) for your business.</span></span>
3. <span data-ttu-id="8e617-122">Valinnainen: Jos haluat näyttää suositukset Tapahtuma-näytössä, siirry kohtaan **Näytön asettelu**, valitse näyttöasettelu, käynnistä **Näytön asettelun suunnittelutoiminto** ja pudota **Suositukset**-ohjausobjekti haluamaasi paikkaan.</span><span class="sxs-lookup"><span data-stu-id="8e617-122">Optional: To display recommendations on the transaction screen, go to **Screen Layout**, choose your screen layout, launch the **Screen layout designer**, and then drop the **recommendations** control where needed.</span></span>
4. <span data-ttu-id="8e617-123">Siirry kohtaan **Commercen parametrit**, valitse **Automaattianalyysipalvelut** ja valitse **Kyllä** kohdassa **Ota käyttöön myyntipisteen suositukset**.</span><span class="sxs-lookup"><span data-stu-id="8e617-123">Go to **Commerce parameters**, select **Machine-learning**, select **Yes** under **Enable POS recommendations**.</span></span>
5. <span data-ttu-id="8e617-124">Saat suositukset näkyviin myyntipisteessä suorittamalla yleisen konfiguraatiotyön **1110**.</span><span class="sxs-lookup"><span data-stu-id="8e617-124">To see recommendations on POS, run global configuration job **1110**.</span></span> <span data-ttu-id="8e617-125">Saat myyntipisteen näytön asetteluun tehdyt muutokset näkyviin suorittamalla kanavan konfigurointityön **1070**.</span><span class="sxs-lookup"><span data-stu-id="8e617-125">To reflect changes made to POS screen layout designer, run channel configuration job **1070**.</span></span>

## <a name="troubleshoot-issues-where-you-have-product-recommendations-already-enabled"></a><span data-ttu-id="8e617-126">Jo käyttöönotettuihin tuotesuosituksiin liittyvien ongelmien vianmääritys</span><span class="sxs-lookup"><span data-stu-id="8e617-126">Troubleshoot issues where you have Product recommendations already enabled</span></span>

- <span data-ttu-id="8e617-127">Valitse **Commercen parametrit** \> **Suositusluettelot** \> **Poista tuotesuositukset käytöstä** ja suorita **Yleinen konfiguraatiotyö \[9999\]**.</span><span class="sxs-lookup"><span data-stu-id="8e617-127">Navigate to **Commerce Parameters** \> **Recommendation lists** \> **Disable product recommendations** and run **Global configuration job \[9999\]**.</span></span> 
- <span data-ttu-id="8e617-128">Jos lisäsit **suositusten ohjausobjektin** tapahtumanäyttöön **näytön asettelun suunnittelutoiminnolla**, poista myös se.</span><span class="sxs-lookup"><span data-stu-id="8e617-128">If you added the **Recommendations control** to your transaction screen using the **Screen layout designer**, please remove that as well.</span></span>
- <span data-ttu-id="8e617-129">Jos sinulla on lisäkysymyksiä, lisätietoja kohdassa [Tuotesuositusten usein kysytyt kysymykset](../commerce/faq-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="8e617-129">If you have additional questions, check out the [Product recommendations FAQ](../commerce/faq-recommendations.md) for more information.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8e617-130">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="8e617-130">Additional resources</span></span>

[<span data-ttu-id="8e617-131">Suositusten ohjausobjektin lisääminen myyntipisteen laitteen tapahtumaruudulle</span><span class="sxs-lookup"><span data-stu-id="8e617-131">Add a recommendations control to the transaction screen on POS devices</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="8e617-132">Tuotesuositusten yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="8e617-132">Product recommendations overview</span></span>](../commerce/product-recommendations.md)

[<span data-ttu-id="8e617-133">Ota tuotesuositukset käyttöön</span><span class="sxs-lookup"><span data-stu-id="8e617-133">Enable product recommendations</span></span>](../commerce/enable-product-recommendations.md) 
