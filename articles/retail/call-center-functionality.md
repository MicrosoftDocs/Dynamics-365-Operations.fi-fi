---
title: Puhelukeskuksen toiminnot
description: "Tässä ohjeaiheessa on Microsoft Dynamics 365 for Retailin puhelinkeskuksen myyntitoimintojen yleiskatsaus."
author: josaw1
manager: AnnBe
ms.date: 04/03/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
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
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: e85b65e116b32adca09e46252d7d3bbe5101e1cf
ms.contentlocale: fi-fi
ms.lasthandoff: 05/08/2018

---

# <a name="call-center"></a><span data-ttu-id="a2ec9-103">Puhelinkeskus</span><span class="sxs-lookup"><span data-stu-id="a2ec9-103">Call center</span></span> 

[!include [banner](includes/banner.md)]

<span data-ttu-id="a2ec9-104">Dynamics 365 for Retailissa puhelinpalvelukeskus on vähittäismyynnin kanava, joka voidaan määrittää sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="a2ec9-104">In Dynamics 365 for Retail, a call center is a type of Retail channel that can be defined in the application.</span></span> <span data-ttu-id="a2ec9-105">Määrittämällä tietyn kanavan kaikille puhelinkeskusyksiköillesi järjestelmä voi liittää tietyt oletustiedot ja tilauksen käsittelyn oletusarvot myyntitilauksiin, jotka puhelinkeskuskanavan käyttäjä on luonut.</span><span class="sxs-lookup"><span data-stu-id="a2ec9-105">Defining a specific channel for your call center entities allows the system to tie specific data defaults and order processing defaults to sales orders created by a user of the call center channel.</span></span>

<span data-ttu-id="a2ec9-106">Puhelinkeskuksen ominaisuuksia ovat tarkennettu vähittäismyyntihinta ja alennukset, luettelot, lahjakortit, kanta-asiakasohjelmat ja kupongit.</span><span class="sxs-lookup"><span data-stu-id="a2ec9-106">Call center features include advanced retail price and promotions, catalogs, gift cards, loyalty programs, and coupons.</span></span> <span data-ttu-id="a2ec9-107">Puhelinkeskuksen tilauksia toimittaa myös myyntipistesovellus (POS) ristikanavatilauksen tukemiseksi.</span><span class="sxs-lookup"><span data-stu-id="a2ec9-107">Call center orders are also leveraged by the point of sale (POS) application to support cross-channel order fulfillment scenarios.</span></span>

<span data-ttu-id="a2ec9-108">On tärkeää muistaa, että vaikka puhelinkeskusmoduulia voidaan käyttää muilla aloilla vähittäismyynnin ulkopuolella, Dynamics 365 for Retailin nykyisen version puhelinkeskussovellusta ei ole vielä optimoitu käytettäväksi yritysten välisissä (B2B) tilauksen käsittelytilanteissa tai tilanteissa, joissa tilauksessa on paljon myyntirivejä.</span><span class="sxs-lookup"><span data-stu-id="a2ec9-108">It's important to note that while the call center module can be utilized by other industries outside of Retail, the current release of the Dynamics 365 for Retail call center application hasn't been optimized for use in business-to-business (B2B) order processing scenarios, or scenarios where orders have a large amount of sales lines.</span></span> <span data-ttu-id="a2ec9-109">On suositeltavaa, että käyttäjät, jotka haluavat käyttää puhelinkeskuksen ominaisuuksia tilausten käsittelyyn tavallisten kuluttajatapahtumien ulkopuolella, varaavat riittävästi aikaa puhelinkeskuksen toimintojen testaamiseen ja vahvistamiseen, jotta ne toimivat halutulla tavalla.</span><span class="sxs-lookup"><span data-stu-id="a2ec9-109">It's recommended that users who want to utilize the call center features for order processing outside of typical direct-to-consumer transaction processing, take adequate time to test and validate that enabling call center functionality will meet functional and performance needs.</span></span>

<span data-ttu-id="a2ec9-110">Tilauksen luonnin tukemisen lisäksi puhelinkeskusmoduuli tarjoaa myös helppokäyttöisen asiakaspalvelusovelluksen, joka helpottaa asiakastilien paikantamista ja asiakkaan tilaustietojen ja määritteiden tarkastamista.</span><span class="sxs-lookup"><span data-stu-id="a2ec9-110">In addition to supporting order creation, the call center module also provides a user-friendly customer service application that makes it easier for users to locate customer accounts and review all of the related customer order data and attributes.</span></span> <span data-ttu-id="a2ec9-111">Asiakaspalvelunäyttö on suunniteltu siten, että käyttäjä pääsee nopeasti tarvittaviin tietoihin, joiden avulla voidaan vastata asiakkaan useimpiin tilausta koskeviin kysymyksiin.</span><span class="sxs-lookup"><span data-stu-id="a2ec9-111">The customer service screen is designed to enable a user to quickly access order related data that will allow them to answer the most common order-related questions received from customers.</span></span>

<span data-ttu-id="a2ec9-112">Tällä sivulla on linkit asianmukaisiin dokumentteihin, jotka liittyvät Dynamics 365 for Retailin puhelinkeskusominaisuuksien määritykseen ja käyttöön.</span><span class="sxs-lookup"><span data-stu-id="a2ec9-112">This page provides links to relevant documentation related to the setup, configuration, and functional use of the call center features in Dynamics 365 for Retail.</span></span>

## <a name="configure-the-call-center"></a><span data-ttu-id="a2ec9-113">Määritä puhelinkeskus</span><span class="sxs-lookup"><span data-stu-id="a2ec9-113">Configure the call center</span></span>
[<span data-ttu-id="a2ec9-114">Tilaustenkäsittelyasetusten määrittäminen</span><span class="sxs-lookup"><span data-stu-id="a2ec9-114">Set up order processing options</span></span>](set-up-order-processing-options.md)

## <a name="configure-order-processing"></a><span data-ttu-id="a2ec9-115">Määritä tilauksen käsittely</span><span class="sxs-lookup"><span data-stu-id="a2ec9-115">Configure order processing</span></span>
<span data-ttu-id="a2ec9-116">[Määritä petoshälytykset](set-up-fraud-alerts.md)
[Manuaaliset tilausten pidot](work-with-order-holds.md)</span><span class="sxs-lookup"><span data-stu-id="a2ec9-116">[Set up fraud alerts](set-up-fraud-alerts.md)
[Manual Order Holds](work-with-order-holds.md)</span></span>

## <a name="configure-payment-processing"></a><span data-ttu-id="a2ec9-117">Määritä maksun käsittely</span><span class="sxs-lookup"><span data-stu-id="a2ec9-117">Configure payment processing</span></span>
[<span data-ttu-id="a2ec9-118">Puhelinkeskuksen maksutavat</span><span class="sxs-lookup"><span data-stu-id="a2ec9-118">Payment methods in a call center</span></span>](work-with-payments.md)

## <a name="configure-direct-marketing"></a><span data-ttu-id="a2ec9-119">Määritä suoramarkkinointi</span><span class="sxs-lookup"><span data-stu-id="a2ec9-119">Configure direct marketing</span></span>
[<span data-ttu-id="a2ec9-120">Puhelinkeskuksen luettelot</span><span class="sxs-lookup"><span data-stu-id="a2ec9-120">Call center catalogs</span></span>](call-center-catalogs.md)

[<span data-ttu-id="a2ec9-121">RFM-analyysin määrittäminen</span><span class="sxs-lookup"><span data-stu-id="a2ec9-121">Set up RFM analysis</span></span>](set-up-rfm-analysis.md)

## <a name="configure-continuity-programs"></a><span data-ttu-id="a2ec9-122">Määritä jatkuvuusohjelmat</span><span class="sxs-lookup"><span data-stu-id="a2ec9-122">Configure continuity programs</span></span>
[<span data-ttu-id="a2ec9-123">Puhelinkeskuksen jatkuvuusohjelman määrittäminen</span><span class="sxs-lookup"><span data-stu-id="a2ec9-123">Set up a continuity program for a call center</span></span>](set-up-continuity-program.md)


