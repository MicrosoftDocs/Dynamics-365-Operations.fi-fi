---
title: Dynamics 365 Commerce -sivuston liittäminen online-kanavaan
description: Tässä ohjeaiheessa kerrotaan, kuinka Microsoft Dynamics 365 Commerce -sivusto sidotaan yhteen tai useaan verkkomyymälään.
author: bicyclingfool
manager: AnnBe
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ROBOTS: ''
audience: Application user
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.author: stuharg
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: fc93441bd09deccdb8c7ecf955c0ec5177c0b31e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4980020"
---
# <a name="associate-a-dynamics-365-commerce-site-with-an-online-channel"></a><span data-ttu-id="658d5-103">Dynamics 365 Commerce -sivuston liittäminen online-kanavaan</span><span class="sxs-lookup"><span data-stu-id="658d5-103">Associate a Dynamics 365 Commerce site with an online channel</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="658d5-104">Tässä ohjeaiheessa kerrotaan, kuinka Microsoft Dynamics 365 Commerce -sivusto sidotaan yhteen tai useaan verkkomyymälään.</span><span class="sxs-lookup"><span data-stu-id="658d5-104">This topic explains how to bind your Microsoft Dynamics 365 Commerce site to one or more online stores.</span></span> 

<span data-ttu-id="658d5-105">Kun olet valmistellut sähköisen kaupankäynnin Dynamics 365 Commerce -ympäristön Microsoft Dynamics Lifecycle Services (LCS) -portaalin avulla, olet valmis muodostamaan ensimmäisen sähköisen kaupankäynnin sivuston.</span><span class="sxs-lookup"><span data-stu-id="658d5-105">After you've provisioned your Dynamics 365 Commerce e-commerce environment by using the Microsoft Dynamics Lifecycle Services (LCS) portal, you're ready to establish your first e-commerce website.</span></span> <span data-ttu-id="658d5-106">Liitä sivusto ensimmäisen sivuston luonnin osana verkkomyymälään, joka luotiin aiemmin.</span><span class="sxs-lookup"><span data-stu-id="658d5-106">As part of the initial site creation, you associate the site with an online store that was previously created.</span></span> <span data-ttu-id="658d5-107">Tämä vaihe sitoo sivuston verkkokanavaan ja antaa sivuston näyttää siirtymishierarkian, tuotteet, luokat, hinnat, toimitusvaihtoehdot ja kaiken muun verkkomyymälässä määritetyn tiedon.</span><span class="sxs-lookup"><span data-stu-id="658d5-107">This step binds the site to an online channel and lets the site show the navigation hierarchy, products, categories, prices, shipping options, and everything else that you defined in the online store.</span></span>

<span data-ttu-id="658d5-108">Jos haluat luoda uuden sivuston ja liittää siihen verkkomyymälän, valitse LCS:ssä sivuston muokkausympäristön linkki.</span><span class="sxs-lookup"><span data-stu-id="658d5-108">To establish a new site and associate an online store with it, in LCS, select the link for the site authoring environment.</span></span> <span data-ttu-id="658d5-109">Valitse sitten sivuston muokkausympäristön aloitussivulla **Uusi sivusto**.</span><span class="sxs-lookup"><span data-stu-id="658d5-109">Then, on the page for the site authoring environment, select **New site**.</span></span> <span data-ttu-id="658d5-110">Anna **Uusi sivusto** -valintaikkunassa joitakin perustietoja sivustosta.</span><span class="sxs-lookup"><span data-stu-id="658d5-110">In the **New site** dialog box, you must provide some basic information about your site.</span></span> <span data-ttu-id="658d5-111">Lisätietoja annettavista tiedoista on kohdassa [Uuden sähköisen kaupankäynnin sivuston luominen](create-ecommerce-site.md).</span><span class="sxs-lookup"><span data-stu-id="658d5-111">For a complete explanation of the information that you must provide, see [Create a new e-commerce site](create-ecommerce-site.md).</span></span>

<span data-ttu-id="658d5-112">Kun sivusto on luotu, voit varmistaa, että se on liitetty verkkomyymälään, valitsemalla **Tuotteet**-välilehden. Näkyvissä on tuotevalikoima, joka on määritetty verkkomyymälälle.</span><span class="sxs-lookup"><span data-stu-id="658d5-112">After your site is created, you can verify that it's associated with your online store by selecting the **Products** tab. You should see the assortment of products that has been allocated to the online store.</span></span> <span data-ttu-id="658d5-113">Voit käyttää avattavaa kenttää sivun vasemmassa yläosassa, jos haluat käyttää tuotteita luokan mukaan.</span><span class="sxs-lookup"><span data-stu-id="658d5-113">You can also use the drop-down field in the upper left of the page to access the products by category.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="658d5-114">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="658d5-114">Additional resources</span></span>

[<span data-ttu-id="658d5-115">Toimialueen nimen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="658d5-115">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="658d5-116">Uuden sähköisen kaupankäynnin vuokraajan käyttöönotto</span><span class="sxs-lookup"><span data-stu-id="658d5-116">Deploy a new e-commerce tenant</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="658d5-117">Sähköisen kaupankäynnin sivuston luominen</span><span class="sxs-lookup"><span data-stu-id="658d5-117">Create an e-commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="658d5-118">Robots.txt-tiedostojen hallinta</span><span class="sxs-lookup"><span data-stu-id="658d5-118">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="658d5-119">URL-uudelleenohjausten joukkolataus palveluun</span><span class="sxs-lookup"><span data-stu-id="658d5-119">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="658d5-120">B2C-vuokraajan määrittäminen Commercessa</span><span class="sxs-lookup"><span data-stu-id="658d5-120">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="658d5-121">Mukautettujen sivujen määrittäminen käyttäjän kirjautumisia varten</span><span class="sxs-lookup"><span data-stu-id="658d5-121">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="658d5-122">Useiden B2C-vuokraajien määrittäminen Commerce-ympäristössä</span><span class="sxs-lookup"><span data-stu-id="658d5-122">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="658d5-123">Sisältöverkon (CDN) tuen lisääminen</span><span class="sxs-lookup"><span data-stu-id="658d5-123">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="658d5-124">Sijaintiin perustuvan myymälän tunnistuksen käyttöönotto</span><span class="sxs-lookup"><span data-stu-id="658d5-124">Enable location-based store detection</span></span>](enable-store-detection.md)
