---
title: Puhelukeskuksen myyntitoiminnot
description: Tässä ohjeaiheessa on Dynamics 365 Retailin puhelinkeskuksen myyntitoimintojen yleiskatsaus.
author: josaw1
manager: AnnBe
ms.date: 04/03/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailMCRChannelDetailPage, MCROrderParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16361
ms.assetid: c8ed2ba4-8d06-4d99-9728-2a83e6d95ca9
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 2e44770af4a30f539e56d38b21c897cacd2707e7
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/18/2019
ms.locfileid: "2812336"
---
# <a name="call-center-sales-functionality"></a><span data-ttu-id="b431c-103">Puhelupalvelukeskuksen myyntitoiminnot</span><span class="sxs-lookup"><span data-stu-id="b431c-103">Call center sales functionality</span></span>

[!include [banner](includes/banner.md)]


<span data-ttu-id="b431c-104">Dynamics 365 Retailissa puhelinpalvelukeskus on vähittäismyynnin kanava, joka voidaan määrittää sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="b431c-104">In Dynamics 365 Retail, a call center is a type of Retail channel that can be defined in the application.</span></span> <span data-ttu-id="b431c-105">Määrittämällä tietyn kanavan kaikille puhelinkeskusyksiköillesi järjestelmä voi liittää tietyt oletustiedot ja tilauksen käsittelyn oletusarvot myyntitilauksiin, jotka puhelinkeskuskanavan käyttäjä on luonut.</span><span class="sxs-lookup"><span data-stu-id="b431c-105">Defining a specific channel for your call center entities allows the system to tie specific data defaults and order processing defaults to sales orders created by a user of the call center channel.</span></span>

<span data-ttu-id="b431c-106">Puhelinkeskuksen ominaisuuksia ovat tarkennettu vähittäismyyntihinta ja alennukset, luettelot, lahjakortit, kanta-asiakasohjelmat ja kupongit.</span><span class="sxs-lookup"><span data-stu-id="b431c-106">Call center features include advanced retail price and promotions, catalogs, gift cards, loyalty programs, and coupons.</span></span> <span data-ttu-id="b431c-107">Puhelinkeskuksen tilauksia toimittaa myös myyntipistesovellus (POS) ristikanavatilauksen tukemiseksi.</span><span class="sxs-lookup"><span data-stu-id="b431c-107">Call center orders are also leveraged by the point of sale (POS) application to support cross-channel order fulfillment scenarios.</span></span>

<span data-ttu-id="b431c-108">On tärkeää muistaa, että vaikka puhelinkeskusmoduulia voidaan käyttää muilla aloilla vähittäismyynnin ulkopuolella, Retailin nykyisen version puhelinkeskussovellusta ei ole vielä optimoitu käytettäväksi yritysten välisissä (B2B) tilauksen käsittelytilanteissa tai tilanteissa, joissa tilauksessa on paljon myyntirivejä.</span><span class="sxs-lookup"><span data-stu-id="b431c-108">It's important to note that while the call center module can be utilized by other industries outside of Retail, the current release of the Retail call center application hasn't been optimized for use in business-to-business (B2B) order processing scenarios, or scenarios where orders have a large amount of sales lines.</span></span> <span data-ttu-id="b431c-109">On suositeltavaa, että käyttäjät, jotka haluavat käyttää puhelinkeskuksen ominaisuuksia tilausten käsittelyyn tavallisten kuluttajatapahtumien ulkopuolella, varaavat riittävästi aikaa puhelinkeskuksen toimintojen testaamiseen ja vahvistamiseen, jotta ne toimivat halutulla tavalla.</span><span class="sxs-lookup"><span data-stu-id="b431c-109">It's recommended that users who want to utilize the call center features for order processing outside of typical direct-to-consumer transaction processing, take adequate time to test and validate that enabling call center functionality will meet functional and performance needs.</span></span>

<span data-ttu-id="b431c-110">Tilauksen luonnin tukemisen lisäksi puhelinkeskusmoduuli tarjoaa myös helppokäyttöisen asiakaspalvelusovelluksen, joka helpottaa asiakastilien paikantamista ja asiakkaan tilaustietojen ja määritteiden tarkastamista.</span><span class="sxs-lookup"><span data-stu-id="b431c-110">In addition to supporting order creation, the call center module also provides a user-friendly customer service application that makes it easier for users to locate customer accounts and review all of the related customer order data and attributes.</span></span> <span data-ttu-id="b431c-111">Asiakaspalvelunäyttö on suunniteltu siten, että käyttäjä pääsee nopeasti tarvittaviin tietoihin, joiden avulla voidaan vastata asiakkaan useimpiin tilausta koskeviin kysymyksiin.</span><span class="sxs-lookup"><span data-stu-id="b431c-111">The customer service screen is designed to enable a user to quickly access order related data that will allow them to answer the most common order-related questions received from customers.</span></span>

<span data-ttu-id="b431c-112">Tällä sivulla on linkit asianmukaisiin dokumentteihin, jotka liittyvät Retailin puhelinkeskusominaisuuksien määritykseen ja käyttöön.</span><span class="sxs-lookup"><span data-stu-id="b431c-112">This page provides links to relevant documentation related to the setup, configuration, and functional use of the call center features in Retail.</span></span>


## <a name="configure-the-call-center"></a><span data-ttu-id="b431c-113">Määritä puhelinkeskus</span><span class="sxs-lookup"><span data-stu-id="b431c-113">Configure the call center</span></span>

[<span data-ttu-id="b431c-114">Puhelinkeskuskanavien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="b431c-114">Set up call center channels</span></span>](set-up-order-processing-options.md)

## <a name="configure-order-processing"></a><span data-ttu-id="b431c-115">Määritä tilauksen käsittely</span><span class="sxs-lookup"><span data-stu-id="b431c-115">Configure order processing</span></span>

[<span data-ttu-id="b431c-116">Puhelinkeskuksen petosilmoitusten määrittäminen ja niiden käyttäminen</span><span class="sxs-lookup"><span data-stu-id="b431c-116">Set up and work with call center fraud alerts</span></span>](set-up-fraud-alerts.md)

[<span data-ttu-id="b431c-117">Puhelinkeskustilausten pidon määrittäminen ja käyttäminen</span><span class="sxs-lookup"><span data-stu-id="b431c-117">Configure and work with call center order holds</span></span>](work-with-order-holds.md)

## <a name="configure-payment-processing"></a><span data-ttu-id="b431c-118">Määritä maksun käsittely</span><span class="sxs-lookup"><span data-stu-id="b431c-118">Configure payment processing</span></span>

[<span data-ttu-id="b431c-119">Puhelinkeskusten maksutavat</span><span class="sxs-lookup"><span data-stu-id="b431c-119">Payment methods in call centers</span></span>](work-with-payments.md)

## <a name="configure-delivery-modes"></a><span data-ttu-id="b431c-120">Määritä toimitustavat</span><span class="sxs-lookup"><span data-stu-id="b431c-120">Configure delivery modes</span></span>

[<span data-ttu-id="b431c-121">Määritä puhelinkeskuksen toimitustavat ja kulut</span><span class="sxs-lookup"><span data-stu-id="b431c-121">Configure call center delivery modes and charges</span></span>](configure-call-center-delivery.md)

## <a name="configure-direct-marketing"></a><span data-ttu-id="b431c-122">Määritä suoramarkkinointi</span><span class="sxs-lookup"><span data-stu-id="b431c-122">Configure direct marketing</span></span>

[<span data-ttu-id="b431c-123">Puhelinpalvelukeskuksen luettelot</span><span class="sxs-lookup"><span data-stu-id="b431c-123">Call center catalogs</span></span>](call-center-catalogs.md)

[<span data-ttu-id="b431c-124">RFM-analyysin (äskettäisyys, toistuvuus ja rahallinen arvo) määrittäminen</span><span class="sxs-lookup"><span data-stu-id="b431c-124">Set up Recency, Frequency, and Monetary (RFM) analysis</span></span>](set-up-rfm-analysis.md)

## <a name="configure-continuity-programs"></a><span data-ttu-id="b431c-125">Määritä jatkuvuusohjelmat</span><span class="sxs-lookup"><span data-stu-id="b431c-125">Configure continuity programs</span></span>

[<span data-ttu-id="b431c-126">Jatkuvuusohjelmien määrittäminen puhelinkeskuksille</span><span class="sxs-lookup"><span data-stu-id="b431c-126">Set up continuity programs for call centers</span></span>](set-up-continuity-program.md)
