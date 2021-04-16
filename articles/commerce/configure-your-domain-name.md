---
title: Toimialueen nimen määrittäminen
description: Tässä ohjeaiheessa kerrotaan, miten Microsoft Dynamics 365:n sähköisen kaupankäynnin sivuston toimialueen nimi määritetään.
author: psimolin
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 3d41168da44100a09c58b8c05367ab45bbd62a30
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5796048"
---
# <a name="configure-your-domain-name"></a><span data-ttu-id="ce0d0-103">Toimialueen nimen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="ce0d0-103">Configure your domain name</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="ce0d0-104">Tässä ohjeaiheessa kerrotaan, miten Microsoft Dynamics 365:n sähköisen kaupankäynnin sivuston toimialueen nimi määritetään.</span><span class="sxs-lookup"><span data-stu-id="ce0d0-104">This topic explains how to configure a domain name for a Microsoft Dynamics 365 e-commerce site.</span></span> 

## <a name="add-domains-during-e-commerce-initialization"></a><span data-ttu-id="ce0d0-105">Toimialueiden lisääminen sähköisen kaupankäynnin alustamisen aikana</span><span class="sxs-lookup"><span data-stu-id="ce0d0-105">Add domains during e-commerce initialization</span></span>

<span data-ttu-id="ce0d0-106">Jos haluat liittää toimialueet sähköisen kaupankäynnin Dynamics 365 Commerce -ympäristöön, alusta sähköinen kaupankäynti kohdassa [Uuden sähköisen kaupankäynnin vuokraajan käyttöönotto](deploy-ecommerce-site.md) kuvatulla tavalla.</span><span class="sxs-lookup"><span data-stu-id="ce0d0-106">To associate domains with your Dynamics 365 Commerce e-commerce environment, initialize e-commerce as described in [Deploy a new e-commerce tenant](deploy-ecommerce-site.md).</span></span> <span data-ttu-id="ce0d0-107">Alustuksen aikana sinua pyydetään antamaan tietoja, joita käytetään sähköisen kaupankäynnin ympäristössä.</span><span class="sxs-lookup"><span data-stu-id="ce0d0-107">During initialization, you're asked to provide information that will be used to provision your e-commerce environment.</span></span> <span data-ttu-id="ce0d0-108">Lisää **Tuetut isäntänimet** -kenttään toimialueet, joita aiot käyttää tämän ympäristön kanssa.</span><span class="sxs-lookup"><span data-stu-id="ce0d0-108">In the **Supported host names** field, add all the domains that you plan to use with this environment.</span></span> <span data-ttu-id="ce0d0-109">Jos toimialueita on useita, erota ne puolipisteellä.</span><span class="sxs-lookup"><span data-stu-id="ce0d0-109">Multiple domains should be separated with semi-colon.</span></span> <span data-ttu-id="ce0d0-110">Näin toimialueet määritetään kaikissa vaadituissa sähköisen kaupankäynnin osissa. Ne ovat valmiita käytettäviksi, kun siirrät liikenteen omasta CDN-verkosta tai verkkopalvelimelta sähköisen kaupankäynnin edustalle.</span><span class="sxs-lookup"><span data-stu-id="ce0d0-110">In this way, the domains are configured in all the required Commerce components, and they are ready to be used when you switch traffic from your content delivery network (CDN) or web server and point it to the e-commerce front ends.</span></span>

## <a name="add-domains-after-e-commerce-initialization"></a><span data-ttu-id="ce0d0-111">Toimialueiden lisääminen sähköisen kaupankäynnin alustamisen jälkeen</span><span class="sxs-lookup"><span data-stu-id="ce0d0-111">Add domains after e-commerce initialization</span></span>

<span data-ttu-id="ce0d0-112">Jos haluat liittää sähköisen kaupankäynnin ympäristöön uusia toimialueita sähköisen kaupankäynnin alustamisen jälkeen, sinun on lähetettävä palvelupyyntö.</span><span class="sxs-lookup"><span data-stu-id="ce0d0-112">To associate new domains with your e-commerce environment after e-commerce initialization, you must submit a service request.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ce0d0-113">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="ce0d0-113">Additional resources</span></span>

[<span data-ttu-id="ce0d0-114">Uuden sähköisen kaupankäynnin vuokraajan käyttöönotto</span><span class="sxs-lookup"><span data-stu-id="ce0d0-114">Deploy a new e-commerce tenant</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="ce0d0-115">Sähköisen kaupankäynnin sivuston luominen</span><span class="sxs-lookup"><span data-stu-id="ce0d0-115">Create an e-commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="ce0d0-116">Dynamics 365 Commerce -sivuston liittäminen online-kanavaan</span><span class="sxs-lookup"><span data-stu-id="ce0d0-116">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="ce0d0-117">Robots.txt-tiedostojen hallinta</span><span class="sxs-lookup"><span data-stu-id="ce0d0-117">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="ce0d0-118">URL-uudelleenohjausten joukkolataus palveluun</span><span class="sxs-lookup"><span data-stu-id="ce0d0-118">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="ce0d0-119">B2C-vuokraajan määrittäminen Commercessa</span><span class="sxs-lookup"><span data-stu-id="ce0d0-119">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="ce0d0-120">Mukautettujen sivujen määrittäminen käyttäjän kirjautumisia varten</span><span class="sxs-lookup"><span data-stu-id="ce0d0-120">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="ce0d0-121">Useiden B2C-vuokraajien määrittäminen Commerce-ympäristössä</span><span class="sxs-lookup"><span data-stu-id="ce0d0-121">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="ce0d0-122">Sisältöverkon (CDN) tuen lisääminen</span><span class="sxs-lookup"><span data-stu-id="ce0d0-122">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="ce0d0-123">Sijaintiin perustuvan myymälän tunnistuksen käyttöönotto</span><span class="sxs-lookup"><span data-stu-id="ce0d0-123">Enable location-based store detection</span></span>](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]