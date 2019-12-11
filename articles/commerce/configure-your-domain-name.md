---
title: Toimialueen nimen määrittäminen
description: Tässä ohjeaiheessa kerrotaan, miten Microsoft Dynamics 365:n sähköisen kaupankäynnin sivuston toimialueen nimi määritetään.
author: psimolin
manager: AnnBe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 7a988f533757cc3f8555fcf4fb724a22a5b014f8
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770455"
---
# <a name="configure-your-domain-name"></a><span data-ttu-id="91216-103">Toimialueen nimen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="91216-103">Configure your domain name</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="91216-104">Tässä ohjeaiheessa kerrotaan, miten Microsoft Dynamics 365:n sähköisen kaupankäynnin sivuston toimialueen nimi määritetään.</span><span class="sxs-lookup"><span data-stu-id="91216-104">This topic explains how to configure a domain name for a Microsoft Dynamics 365 e-commerce site.</span></span> 

## <a name="add-domains-during-e-commerce-initialization"></a><span data-ttu-id="91216-105">Toimialueiden lisääminen sähköisen kaupankäynnin alustamisen aikana</span><span class="sxs-lookup"><span data-stu-id="91216-105">Add domains during e-Commerce initialization</span></span>

<span data-ttu-id="91216-106">Jos haluat liittää toimialueet sähköisen kaupankäynnin ympäristöön, alusta sähköinen kaupankäynti kohdassa [Uuden sähköisen kaupankäynnin sivuston käyttöönotto](deploy-ecommerce-site.md) kuvatulla tavalla.</span><span class="sxs-lookup"><span data-stu-id="91216-106">To associate domains with your e-commerce environment, initialize e-Commerce as described in [Deploy a new e-Commerce site](deploy-ecommerce-site.md).</span></span> <span data-ttu-id="91216-107">Alustuksen aikana sinua pyydetään antamaan tietoja, joita käytetään sähköisen kaupankäynnin ympäristössä.</span><span class="sxs-lookup"><span data-stu-id="91216-107">During initialization, you're asked to provide information that will be used to provision your e-Commerce environment.</span></span> <span data-ttu-id="91216-108">Lisää **Tuetut isäntänimet** -kenttään toimialueet, joita aiot käyttää tämän ympäristön kanssa.</span><span class="sxs-lookup"><span data-stu-id="91216-108">In the **Supported host names** field, add all the domains that you plan to use with this environment.</span></span> <span data-ttu-id="91216-109">Jos toimialueita on useita, erota ne puolipisteellä.</span><span class="sxs-lookup"><span data-stu-id="91216-109">Multiple domains should be separated with semi-colon.</span></span> <span data-ttu-id="91216-110">Näin toimialueet määritetään kaikissa vaadituissa sähköisen kaupankäynnin osissa. Ne ovat valmiita käytettäviksi, kun siirrät liikenteen omasta CDN-verkosta tai verkkopalvelimelta sähköisen kaupankäynnin edustalle.</span><span class="sxs-lookup"><span data-stu-id="91216-110">In this way, the domains are configured in all the required e-Commerce components, and they are ready to be used when you switch traffic from your content delivery network (CDN) or web server and point it to the e-Commerce front ends.</span></span>

## <a name="add-domains-after-e-commerce-initialization"></a><span data-ttu-id="91216-111">Toimialueiden lisääminen sähköisen kaupankäynnin alustamisen jälkeen</span><span class="sxs-lookup"><span data-stu-id="91216-111">Add domains after e-Commerce initialization</span></span>

<span data-ttu-id="91216-112">Jos haluat liittää sähköisen kaupankäynnin ympäristöön uusia toimialueita sähköisen kaupankäynnin alustamisen jälkeen, sinun on lähetettävä palvelupyyntö.</span><span class="sxs-lookup"><span data-stu-id="91216-112">To associate new domains with your e-Commerce environment after e-Commerce initialization, you must submit a service request.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="91216-113">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="91216-113">Additional resources</span></span>

[<span data-ttu-id="91216-114">Verkkokaupan yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="91216-114">Online store overview</span></span>](online-store-overview.md)

[<span data-ttu-id="91216-115">Sähköisen kaupankäynnin sivuston luominen</span><span class="sxs-lookup"><span data-stu-id="91216-115">Create an e-Commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="91216-116">Uuden sähköisen kaupankäynnin sivuston käyttöönotto</span><span class="sxs-lookup"><span data-stu-id="91216-116">Deploy a new e-Commerce site</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="91216-117">Liitä verkkosivusto kanavaan</span><span class="sxs-lookup"><span data-stu-id="91216-117">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="91216-118">Sisältöverkon (CDN) tuen lisääminen</span><span class="sxs-lookup"><span data-stu-id="91216-118">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="91216-119">Sijaintiin perustuvan myymälän tunnistuksen käyttöönotto</span><span class="sxs-lookup"><span data-stu-id="91216-119">Enable location-based store detection</span></span>](enable-store-detection.md)

[<span data-ttu-id="91216-120">Mukautettujen sivujen määrittäminen käyttäjän kirjautumisia varten</span><span class="sxs-lookup"><span data-stu-id="91216-120">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)
