---
title: Puhelukeskuksen myyntitoiminnot
description: Tässä ohjeaiheessa on Dynamics 365 Commercein puhelinkeskuksen myyntitoimintojen yleiskatsaus.
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
ms.openlocfilehash: 816bfc8b93f52fe91192874bcc1c8e605e41b582
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/01/2020
ms.locfileid: "3022357"
---
# <a name="call-center-sales-functionality"></a><span data-ttu-id="0dac7-103">Puhelupalvelukeskuksen myyntitoiminnot</span><span class="sxs-lookup"><span data-stu-id="0dac7-103">Call center sales functionality</span></span>

[!include [banner](includes/banner.md)]


<span data-ttu-id="0dac7-104">Dynamics 365 Commercessa puhelinpalvelukeskus on vähittäismyynnin kanava, joka voidaan määrittää sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="0dac7-104">In Dynamics 365 Commerce, a call center is a type of channel that can be defined in the application.</span></span> <span data-ttu-id="0dac7-105">Määrittämällä tietyn kanavan kaikille puhelinkeskusyksiköillesi järjestelmä voi liittää tietyt oletustiedot ja tilauksen käsittelyn oletusarvot myyntitilauksiin, jotka puhelinkeskuskanavan käyttäjä on luonut.</span><span class="sxs-lookup"><span data-stu-id="0dac7-105">Defining a specific channel for your call center entities allows the system to tie specific data defaults and order processing defaults to sales orders created by a user of the call center channel.</span></span>

<span data-ttu-id="0dac7-106">Puhelinkeskuksen ominaisuuksia ovat tarkennettu hinta ja alennukset, luettelot, lahjakortit, kanta-asiakasohjelmat ja kupongit.</span><span class="sxs-lookup"><span data-stu-id="0dac7-106">Call center features include advanced price and promotions, catalogs, gift cards, loyalty programs, and coupons.</span></span> <span data-ttu-id="0dac7-107">Puhelinkeskuksen tilauksia toimittaa myös myyntipistesovellus (POS) ristikanavatilauksen tukemiseksi.</span><span class="sxs-lookup"><span data-stu-id="0dac7-107">Call center orders are also leveraged by the point of sale (POS) application to support cross-channel order fulfillment scenarios.</span></span>

<span data-ttu-id="0dac7-108">On tärkeää muistaa, että vaikka puhelinkeskusmoduulia voidaan käyttää muilla aloilla kaupankäynnin ulkopuolella, nykyisen version puhelinkeskussovellusta ei ole vielä optimoitu käytettäväksi yritysten välisissä (B2B) tilauksen käsittelytilanteissa tai tilanteissa, joissa tilauksessa on paljon myyntirivejä.</span><span class="sxs-lookup"><span data-stu-id="0dac7-108">It's important to note that while the call center module can be utilized by other industries outside of Commerce, the current release of the call center application hasn't been optimized for use in business-to-business (B2B) order processing scenarios, or scenarios where orders have a large amount of sales lines.</span></span> <span data-ttu-id="0dac7-109">On suositeltavaa, että käyttäjät, jotka haluavat käyttää puhelinkeskuksen ominaisuuksia tilausten käsittelyyn tavallisten kuluttajatapahtumien ulkopuolella, varaavat riittävästi aikaa puhelinkeskuksen toimintojen testaamiseen ja vahvistamiseen, jotta ne toimivat halutulla tavalla.</span><span class="sxs-lookup"><span data-stu-id="0dac7-109">It's recommended that users who want to utilize the call center features for order processing outside of typical direct-to-consumer transaction processing, take adequate time to test and validate that enabling call center functionality will meet functional and performance needs.</span></span>

<span data-ttu-id="0dac7-110">Tilauksen luonnin tukemisen lisäksi puhelinkeskusmoduuli tarjoaa myös helppokäyttöisen asiakaspalvelusovelluksen, joka helpottaa asiakastilien paikantamista ja asiakkaan tilaustietojen ja määritteiden tarkastamista.</span><span class="sxs-lookup"><span data-stu-id="0dac7-110">In addition to supporting order creation, the call center module also provides a user-friendly customer service application that makes it easier for users to locate customer accounts and review all of the related customer order data and attributes.</span></span> <span data-ttu-id="0dac7-111">Asiakaspalvelunäyttö on suunniteltu siten, että käyttäjä pääsee nopeasti tarvittaviin tietoihin, joiden avulla voidaan vastata asiakkaan useimpiin tilausta koskeviin kysymyksiin.</span><span class="sxs-lookup"><span data-stu-id="0dac7-111">The customer service screen is designed to enable a user to quickly access order related data that will allow them to answer the most common order-related questions received from customers.</span></span>

<span data-ttu-id="0dac7-112">Tällä sivulla on linkit asianmukaisiin dokumentteihin, jotka liittyvät puhelinkeskusominaisuuksien määritykseen ja käyttöön.</span><span class="sxs-lookup"><span data-stu-id="0dac7-112">This page provides links to relevant documentation related to the setup, configuration, and functional use of the call center features.</span></span>


## <a name="configure-the-call-center"></a><span data-ttu-id="0dac7-113">Määritä puhelinkeskus</span><span class="sxs-lookup"><span data-stu-id="0dac7-113">Configure the call center</span></span>

[<span data-ttu-id="0dac7-114">Puhelinkeskuskanavien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="0dac7-114">Set up call center channels</span></span>](set-up-order-processing-options.md)

## <a name="configure-order-processing"></a><span data-ttu-id="0dac7-115">Määritä tilauksen käsittely</span><span class="sxs-lookup"><span data-stu-id="0dac7-115">Configure order processing</span></span>

[<span data-ttu-id="0dac7-116">Puhelinkeskuksen petosilmoitusten määrittäminen ja niiden käyttäminen</span><span class="sxs-lookup"><span data-stu-id="0dac7-116">Set up and work with call center fraud alerts</span></span>](set-up-fraud-alerts.md)

[<span data-ttu-id="0dac7-117">Puhelinkeskustilausten pidon määrittäminen ja käyttäminen</span><span class="sxs-lookup"><span data-stu-id="0dac7-117">Configure and work with call center order holds</span></span>](work-with-order-holds.md)

## <a name="configure-payment-processing"></a><span data-ttu-id="0dac7-118">Määritä maksun käsittely</span><span class="sxs-lookup"><span data-stu-id="0dac7-118">Configure payment processing</span></span>

[<span data-ttu-id="0dac7-119">Puhelinkeskusten maksutavat</span><span class="sxs-lookup"><span data-stu-id="0dac7-119">Payment methods in call centers</span></span>](work-with-payments.md)

## <a name="configure-delivery-modes"></a><span data-ttu-id="0dac7-120">Määritä toimitustavat</span><span class="sxs-lookup"><span data-stu-id="0dac7-120">Configure delivery modes</span></span>

[<span data-ttu-id="0dac7-121">Määritä puhelinkeskuksen toimitustavat ja kulut</span><span class="sxs-lookup"><span data-stu-id="0dac7-121">Configure call center delivery modes and charges</span></span>](configure-call-center-delivery.md)

## <a name="configure-direct-marketing"></a><span data-ttu-id="0dac7-122">Määritä suoramarkkinointi</span><span class="sxs-lookup"><span data-stu-id="0dac7-122">Configure direct marketing</span></span>

[<span data-ttu-id="0dac7-123">Puhelinpalvelukeskuksen luettelot</span><span class="sxs-lookup"><span data-stu-id="0dac7-123">Call center catalogs</span></span>](call-center-catalogs.md)

[<span data-ttu-id="0dac7-124">RFM-analyysin (äskettäisyys, toistuvuus ja rahallinen arvo) määrittäminen</span><span class="sxs-lookup"><span data-stu-id="0dac7-124">Set up Recency, Frequency, and Monetary (RFM) analysis</span></span>](set-up-rfm-analysis.md)

## <a name="configure-continuity-programs"></a><span data-ttu-id="0dac7-125">Määritä jatkuvuusohjelmat</span><span class="sxs-lookup"><span data-stu-id="0dac7-125">Configure continuity programs</span></span>

[<span data-ttu-id="0dac7-126">Jatkuvuusohjelmien määrittäminen puhelinkeskuksille</span><span class="sxs-lookup"><span data-stu-id="0dac7-126">Set up continuity programs for call centers</span></span>](set-up-continuity-program.md)