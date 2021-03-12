---
title: Sijaintiin perustuvan myymälän tunnistuksen käyttöönotto
description: Tässä ohjeaiheessa kerrotaan, miten sijaintiin perustuva myymälän tunnistaminen otetaan käyttöön Dynamics 365 Commerce -sivustossa.
author: brianshook
manager: annbe
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 3f7e9a3acde508f405ce85f125db552c3ae3656b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "5000719"
---
# <a name="enable-location-based-store-detection"></a><span data-ttu-id="4a28d-103">Sijaintiin perustuvan myymälän tunnistuksen käyttöönotto</span><span class="sxs-lookup"><span data-stu-id="4a28d-103">Enable location-based store detection</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="4a28d-104">Tässä ohjeaiheessa kerrotaan, miten sijaintiin perustuva myymälän tunnistaminen otetaan käyttöön Dynamics 365 Commerce -sivustossa.</span><span class="sxs-lookup"><span data-stu-id="4a28d-104">This topic describes how to turn on location-based store detection for your Dynamics 365 Commerce site.</span></span>

## <a name="overview"></a><span data-ttu-id="4a28d-105">Yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="4a28d-105">Overview</span></span>

<span data-ttu-id="4a28d-106">Sijaintiin perustuva myymälän tunnistaminen Commerce-sovelluksessa mahdollistaa soveltuvan sivustosisällön tarjoamisen asiakkaille näiden sijainnin perusteella.</span><span class="sxs-lookup"><span data-stu-id="4a28d-106">Location-based store detection in Commerce lets you provide relevant site content to customers, based on their location.</span></span> <span data-ttu-id="4a28d-107">Kun sijaintiin perustuva myymälän tunnistaminen on käytössä, Commercen hahmonnuspalvelu käyttää maan/alueen tietoja asiakkaan verkkoselaimen IP-osoitteen avulla ja ohjaa asiakkaan parhaaseen mahdolliseen käytettävissä olevaan maantieteellisen paikan sivustomääritykseen.</span><span class="sxs-lookup"><span data-stu-id="4a28d-107">When location-based store detection is turned on, the Commerce rendering service uses the country/region information from the IP address of the customer's web browser to direct the customer to the best geographical site configuration that is available.</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="4a28d-108">Tietosuojatiedot</span><span class="sxs-lookup"><span data-stu-id="4a28d-108">Privacy notice</span></span>

<span data-ttu-id="4a28d-109">Jos otat sijaintiin perustuvan myymälän tunnistustoiminnon käyttöön, asiakkaan selaimen tiedot lähetetään Microsoftin paikannuspalveluun.</span><span class="sxs-lookup"><span data-stu-id="4a28d-109">If you turn on the location-based store detection feature, information from the customer's browser is sent to a Microsoft location service.</span></span> <span data-ttu-id="4a28d-110">Näiden tietojen avulla tarjotaan asiakkaalle sisältöä, joka sopii asiakkaan sijaintiin.</span><span class="sxs-lookup"><span data-stu-id="4a28d-110">This information is then used to provide the customer content that is relevant to his or her location.</span></span> <span data-ttu-id="4a28d-111">Sekä asiakkaan selaimesta lähetettävät tiedot että sijaintiin perustuvat tiedot, jotka palautetaan asiakkaalle, ovat tietoturva- ja evästekäytäntöjen alaisia.</span><span class="sxs-lookup"><span data-stu-id="4a28d-111">Both the information that is sent from the customer's browser and the location-based information that is returned to the customer are subject to privacy and cookie compliance policies.</span></span>

## <a name="turn-on-location-based-store-detection"></a><span data-ttu-id="4a28d-112">Sijaintiin perustuvan myymälän tunnistuksen ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="4a28d-112">Turn on location-based store detection</span></span>

<span data-ttu-id="4a28d-113">Voit ottaa sijaintiin perustuvan myymälän tunnistamisen käyttöön Commercessa seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="4a28d-113">To turn on location-based store detection in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="4a28d-114">Siirry muokkaustyökaluissa sivustoon.</span><span class="sxs-lookup"><span data-stu-id="4a28d-114">In the authoring tool, go to your site.</span></span>
1. <span data-ttu-id="4a28d-115">Valitse vasemmanpuoleisessa siirtymisruudussa **Sivuston hallinta**.</span><span class="sxs-lookup"><span data-stu-id="4a28d-115">In the navigation pane on the left, select **Site Management**.</span></span>
1. <span data-ttu-id="4a28d-116">Valitse **Sivuston asetukset**.</span><span class="sxs-lookup"><span data-stu-id="4a28d-116">Select **Site Settings**.</span></span>
1. <span data-ttu-id="4a28d-117">Määritä **Ota sijaintiin perustuva myymälän tunnistus käyttöön** -asetukseksi **Päällä**.</span><span class="sxs-lookup"><span data-stu-id="4a28d-117">Set the **Enable location based store detection** option to **On**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4a28d-118">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="4a28d-118">Additional resources</span></span>

[<span data-ttu-id="4a28d-119">Toimialueen nimen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="4a28d-119">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="4a28d-120">Uuden sähköisen kaupankäynnin vuokraajan käyttöönotto</span><span class="sxs-lookup"><span data-stu-id="4a28d-120">Deploy a new e-commerce tenant</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="4a28d-121">Sähköisen kaupankäynnin sivuston luominen</span><span class="sxs-lookup"><span data-stu-id="4a28d-121">Create an e-commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="4a28d-122">Dynamics 365 Commerce -sivuston liittäminen online-kanavaan</span><span class="sxs-lookup"><span data-stu-id="4a28d-122">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="4a28d-123">Robots.txt-tiedostojen hallinta</span><span class="sxs-lookup"><span data-stu-id="4a28d-123">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="4a28d-124">URL-uudelleenohjausten joukkolataus palveluun</span><span class="sxs-lookup"><span data-stu-id="4a28d-124">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="4a28d-125">B2C-vuokraajan määrittäminen Commercessa</span><span class="sxs-lookup"><span data-stu-id="4a28d-125">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="4a28d-126">Mukautettujen sivujen määrittäminen käyttäjän kirjautumisia varten</span><span class="sxs-lookup"><span data-stu-id="4a28d-126">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="4a28d-127">Useiden B2C-vuokraajien määrittäminen Commerce-ympäristössä</span><span class="sxs-lookup"><span data-stu-id="4a28d-127">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="4a28d-128">Sisältöverkon (CDN) tuen lisääminen</span><span class="sxs-lookup"><span data-stu-id="4a28d-128">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)
