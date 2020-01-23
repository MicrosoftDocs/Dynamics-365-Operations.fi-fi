---
title: Sähköisen kaupankäynnin sivuston liittäminen verkkokanavaan
description: Tässä ohjeaiheessa kerrotaan, kuinka Microsoft Dynamics 365 Commerce -sivusto sidotaan yhteen tai useaan verkkomyymälään.
author: stuharg
manager: AnnBe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ROBOTS: ''
audience: Application user
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.author: bicyclingfool
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 62d3c168967bd680b3ded56e627730324f2a5ec6
ms.sourcegitcommit: ef3a1d7527311d00b69a1072ae5eb021ce68034c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/09/2020
ms.locfileid: "2945579"
---
# <a name="associate-an-e-commerce-site-with-an-online-channel"></a><span data-ttu-id="61832-103">Sähköisen kaupankäynnin sivuston liittäminen verkkokanavaan</span><span class="sxs-lookup"><span data-stu-id="61832-103">Associate an e-Commerce site with an online channel</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="61832-104">Tässä ohjeaiheessa kerrotaan, kuinka Microsoft Dynamics 365 Commerce -sivusto sidotaan yhteen tai useaan verkkomyymälään.</span><span class="sxs-lookup"><span data-stu-id="61832-104">This topic explains how to bind your Microsoft Dynamics 365 Commerce site to one or more online stores.</span></span> 

<span data-ttu-id="61832-105">Kun olet valmistellut sähköisen kaupankäynnin Microsoft Dynamics Lifecycle Services (LCS) -portaalin avulla, olet valmis muodostamaan ensimmäisen sähköisen kaupankäynnin sivuston.</span><span class="sxs-lookup"><span data-stu-id="61832-105">After you've provisioned e-Commerce by using the Microsoft Dynamics Lifecycle Services (LCS) portal, you're ready to establish your first e-Commerce website.</span></span> <span data-ttu-id="61832-106">Liitä sivusto ensimmäisen sivuston luonnin osana verkkomyymälään, joka luotiin aiemmin.</span><span class="sxs-lookup"><span data-stu-id="61832-106">As part of the initial site creation, you associate the site with an online store that was previously created.</span></span> <span data-ttu-id="61832-107">Tämä vaihe sitoo sivuston verkkokanavaan ja antaa sivuston näyttää siirtymishierarkian, tuotteet, luokat, hinnat, toimitusvaihtoehdot ja kaiken muun verkkomyymälässä määritetyn tiedon.</span><span class="sxs-lookup"><span data-stu-id="61832-107">This step binds the site to an online channel and lets the site show the navigation hierarchy, products, categories, prices, shipping options, and everything else that you defined in the online store.</span></span>

<span data-ttu-id="61832-108">Jos haluat luoda uuden sivuston ja liittää siihen verkkomyymälän, valitse LCS:ssä sivuston muokkausympäristön linkki.</span><span class="sxs-lookup"><span data-stu-id="61832-108">To establish a new site and associate an online store with it, in LCS, select the link for the site authoring environment.</span></span> <span data-ttu-id="61832-109">Valitse sitten sivuston muokkausympäristön aloitussivulla **Uusi sivusto**.</span><span class="sxs-lookup"><span data-stu-id="61832-109">Then, on the page for the site authoring environment, select **New site**.</span></span> <span data-ttu-id="61832-110">Anna **Uusi sivusto** -valintaikkunassa joitakin perustietoja sivustosta.</span><span class="sxs-lookup"><span data-stu-id="61832-110">In the **New site** dialog box, you must provide some basic information about your site.</span></span> <span data-ttu-id="61832-111">Lisätietoja annettavista tiedoista on kohdassa [Uuden sähköisen kaupankäynnin sivuston luominen](create-ecommerce-site.md).</span><span class="sxs-lookup"><span data-stu-id="61832-111">For a complete explanation of the information that you must provide, see [Create a new e-Commerce site](create-ecommerce-site.md).</span></span>

<span data-ttu-id="61832-112">Kun sivusto on luotu, voit varmistaa, että se on liitetty verkkomyymälään, valitsemalla **Tuotteet**-välilehden. Näkyvissä on tuotevalikoima, joka on määritetty verkkomyymälälle.</span><span class="sxs-lookup"><span data-stu-id="61832-112">After your site is created, you can verify that it's associated with your online store by selecting the **Products** tab. You should see the assortment of products that has been allocated to the online store.</span></span> <span data-ttu-id="61832-113">Voit käyttää avattavaa kenttää sivun vasemmassa yläosassa, jos haluat käyttää tuotteita luokan mukaan.</span><span class="sxs-lookup"><span data-stu-id="61832-113">You can also use the drop-down field in the upper left of the page to access the products by category.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="61832-114">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="61832-114">Additional resources</span></span>

[<span data-ttu-id="61832-115">Toimialueen nimen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="61832-115">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="61832-116">Uuden sähköisen kaupankäynnin sivuston käyttöönotto</span><span class="sxs-lookup"><span data-stu-id="61832-116">Deploy a new e-Commerce site</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="61832-117">Sähköisen kaupankäynnin sivuston luominen</span><span class="sxs-lookup"><span data-stu-id="61832-117">Create an e-Commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="61832-118">Robots.txt-tiedostojen hallinta</span><span class="sxs-lookup"><span data-stu-id="61832-118">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="61832-119">Mukautettujen sivujen määrittäminen käyttäjän kirjautumisia varten</span><span class="sxs-lookup"><span data-stu-id="61832-119">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="61832-120">Sisältöverkon (CDN) tuen lisääminen</span><span class="sxs-lookup"><span data-stu-id="61832-120">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="61832-121">Sijaintiin perustuvan myymälän tunnistuksen käyttöönotto</span><span class="sxs-lookup"><span data-stu-id="61832-121">Enable location-based store detection</span></span>](enable-store-detection.md)
