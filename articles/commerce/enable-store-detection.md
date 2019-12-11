---
title: Sijaintiin perustuvan myymälän tunnistuksen käyttöönotto
description: Tässä ohjeaiheessa kerrotaan, miten sijaintiin perustuva myymälän tunnistaminen otetaan käyttöön Dynamics 365 Commerce -sivustossa.
author: brianshook
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: a542d6987280451910b4ff3bcfb3a109a0e028c6
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697609"
---
# <a name="enable-location-based-store-detection"></a><span data-ttu-id="0f456-103">Sijaintiin perustuvan myymälän tunnistuksen käyttöönotto</span><span class="sxs-lookup"><span data-stu-id="0f456-103">Enable location-based store detection</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="0f456-104">Tässä ohjeaiheessa kerrotaan, miten sijaintiin perustuva myymälän tunnistaminen otetaan käyttöön Dynamics 365 Commerce -sivustossa.</span><span class="sxs-lookup"><span data-stu-id="0f456-104">This topic describes how to turn on location-based store detection for your Dynamics 365 Commerce site.</span></span>

## <a name="overview"></a><span data-ttu-id="0f456-105">Yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="0f456-105">Overview</span></span>

<span data-ttu-id="0f456-106">Sijaintiin perustuva myymälän tunnistaminen Commerce-sovelluksessa mahdollistaa soveltuvan sivustosisällön tarjoamisen asiakkaille näiden sijainnin perusteella.</span><span class="sxs-lookup"><span data-stu-id="0f456-106">Location-based store detection in Commerce lets you provide relevant site content to customers, based on their location.</span></span> <span data-ttu-id="0f456-107">Kun sijaintiin perustuva myymälän tunnistaminen on käytössä, Commercen hahmonnuspalvelu käyttää maan/alueen tietoja asiakkaan verkkoselaimen IP-osoitteen avulla ja ohjaa asiakkaan parhaaseen mahdolliseen käytettävissä olevaan maantieteellisen paikan sivustomääritykseen.</span><span class="sxs-lookup"><span data-stu-id="0f456-107">When location-based store detection is turned on, the Commerce rendering service uses the country/region information from the IP address of the customer's web browser to direct the customer to the best geographical site configuration that is available.</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="0f456-108">Tietosuojatiedot</span><span class="sxs-lookup"><span data-stu-id="0f456-108">Privacy notice</span></span>

<span data-ttu-id="0f456-109">Jos otat sijaintiin perustuvan myymälän tunnistustoiminnon käyttöön, asiakkaan selaimen tiedot lähetetään Microsoftin paikannuspalveluun.</span><span class="sxs-lookup"><span data-stu-id="0f456-109">If you turn on the location-based store detection feature, information from the customer's browser is sent to a Microsoft location service.</span></span> <span data-ttu-id="0f456-110">Näiden tietojen avulla tarjotaan asiakkaalle sisältöä, joka sopii asiakkaan sijaintiin.</span><span class="sxs-lookup"><span data-stu-id="0f456-110">This information is then used to provide the customer content that is relevant to his or her location.</span></span> <span data-ttu-id="0f456-111">Sekä asiakkaan selaimesta lähetettävät tiedot että sijaintiin perustuvat tiedot, jotka palautetaan asiakkaalle, ovat tietoturva- ja evästekäytäntöjen alaisia.</span><span class="sxs-lookup"><span data-stu-id="0f456-111">Both the information that is sent from the customer's browser and the location-based information that is returned to the customer are subject to privacy and cookie compliance policies.</span></span>

## <a name="turn-on-location-based-store-detection"></a><span data-ttu-id="0f456-112">Sijaintiin perustuvan myymälän tunnistuksen ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="0f456-112">Turn on location-based store detection</span></span>

<span data-ttu-id="0f456-113">Voit ottaa sijaintiin perustuvan myymälän tunnistamisen käyttöön Commercessa seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="0f456-113">To turn on location-based store detection in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="0f456-114">Siirry muokkaustyökaluissa sivustoon.</span><span class="sxs-lookup"><span data-stu-id="0f456-114">In the authoring tool, go to your site.</span></span>
1. <span data-ttu-id="0f456-115">Valitse vasemmanpuoleisessa siirtymisruudussa **Sivuston hallinta**.</span><span class="sxs-lookup"><span data-stu-id="0f456-115">In the navigation pane on the left, select **Site Management**.</span></span>
1. <span data-ttu-id="0f456-116">Valitse **Sivuston asetukset**.</span><span class="sxs-lookup"><span data-stu-id="0f456-116">Select **Site Settings**.</span></span>
1. <span data-ttu-id="0f456-117">Määritä **Ota sijaintiin perustuva myymälän tunnistus käyttöön** -asetukseksi **Päällä**.</span><span class="sxs-lookup"><span data-stu-id="0f456-117">Set the **Enable location based store detection** option to **On**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0f456-118">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="0f456-118">Additional resources</span></span>

[<span data-ttu-id="0f456-119">Verkkokaupan yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="0f456-119">Online store overview</span></span>](online-store-overview.md)

[<span data-ttu-id="0f456-120">Sähköisen kaupankäynnin sivuston luominen</span><span class="sxs-lookup"><span data-stu-id="0f456-120">Create an e-Commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="0f456-121">Uuden sähköisen kaupankäynnin sivuston käyttöönotto</span><span class="sxs-lookup"><span data-stu-id="0f456-121">Deploy a new e-Commerce site</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="0f456-122">Liitä verkkosivusto kanavaan</span><span class="sxs-lookup"><span data-stu-id="0f456-122">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="0f456-123">Toimialueen nimen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="0f456-123">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="0f456-124">Sisältöverkon (CDN) tuen lisääminen</span><span class="sxs-lookup"><span data-stu-id="0f456-124">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="0f456-125">Mukautettujen sivujen määrittäminen käyttäjän kirjautumisia varten</span><span class="sxs-lookup"><span data-stu-id="0f456-125">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)
