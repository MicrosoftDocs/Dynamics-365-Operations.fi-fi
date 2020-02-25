---
title: Dynamics 365 Commercen esikatseluympäristön yleiskuvaus
description: Tässä ohjeaiheessa on yleiskatsaus Microsoft Dynamics 365 Commerce -esikatseluympäristössä.
author: v-chgri
manager: annbe
ms.date: 12/10/2019
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
ms.author: v-chgri
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 1ff96aeb5963df9ddee56783a089dad129bbb71c
ms.sourcegitcommit: 4ed1d8ad8a0206a4172dbb41cc43f7d95073059c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/04/2020
ms.locfileid: "3024680"
---
# <a name="dynamics-365-commerce-preview-environment-overview"></a><span data-ttu-id="9908b-103">Dynamics 365 Commercen esikatseluympäristön yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="9908b-103">Dynamics 365 Commerce preview environment overview</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="9908b-104">Tässä ohjeaiheessa on yleiskatsaus Microsoft Dynamics 365 Commerce -esikatseluympäristössä.</span><span class="sxs-lookup"><span data-stu-id="9908b-104">This topic gives an overview of the Microsoft Dynamics 365 Commerce preview environment.</span></span>

## <a name="overview"></a><span data-ttu-id="9908b-105">Yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="9908b-105">Overview</span></span>

<span data-ttu-id="9908b-106">Commercen esikatseluympäristö on valinnainen Dynamics 365 Commercen päästä päähän -esikatseluympäristö, jonka avulla potentiaaliset asiakkaat voivat kokeilla Commerce-tuotetta ennen sen yleistä julkaisua yleisölle.</span><span class="sxs-lookup"><span data-stu-id="9908b-106">The Commerce preview environment is an optional end-to-end preview environment of Dynamics 365 Commerce that lets potential customers try out the Commerce product before its general release to the public.</span></span>

<span data-ttu-id="9908b-107">Lukuun ottamatta joitakin pieniä rajoituksia, jotka eivät vaikuta ominaisuuksiin tai toimintoihin, Commerce-esikatseluympäristö tarjoaa täydellisen kaupankäynnin kokemuksen, ja asiakkaat ja toteutuskumppanit voivat käyttää sitä tuotteen arviointiin, palautteen tarjoamiseen ja sopivuus- ja aukkoanalyysiin.</span><span class="sxs-lookup"><span data-stu-id="9908b-107">Aside from some minor limitations that don't affect features or functionality, the Commerce preview environment provides the complete Commerce experience, and can be used by customers and implementation partners to evaluate the product, provide feedback, and do fit/gap analysis.</span></span>

## <a name="limitations-of-the-commerce-preview-environment"></a><span data-ttu-id="9908b-108">Commerce-esikatseluympäristön rajoitukset</span><span class="sxs-lookup"><span data-stu-id="9908b-108">Limitations of the Commerce preview environment</span></span>

<span data-ttu-id="9908b-109">Vaikka Commercen esiversioympäristö tarjoaa täydet Commercen ominaisuudet ja toiminnot, siinä on joitakin pieniä rajoituksia:</span><span class="sxs-lookup"><span data-stu-id="9908b-109">Although the Commerce preview environment provides the full set of Commerce features and functionality, there are some minor limitations:</span></span>

- <span data-ttu-id="9908b-110">Vaikka Commercen esiversioympäristössä itsessään ei ole maantieteellisiä rajoituksia, ympäristön osia, kuten Retail Cloud Scale Unit (RCSU) ja sähköisen kaupankäynnin sovelluksia voidaan valmistella vain Yhdysvalloissa.</span><span class="sxs-lookup"><span data-stu-id="9908b-110">Although the Commerce preview environment itself has no geographical limitations, components of the environment, such as the Retail Cloud Scale Unit (RCSU) and e-Commerce applications, can be provisioned only in the United States.</span></span>
- <span data-ttu-id="9908b-111">Commercen esikatseluympäristön käyttö on rajoitettu 30 päivään siitä päivästä, jolloin sähköinen kaupankäynti on valmisteltu.</span><span class="sxs-lookup"><span data-stu-id="9908b-111">Use of the Commerce preview environment is limited to 30 days from the date when e-Commerce is provisioned.</span></span>
- <span data-ttu-id="9908b-112">Commerce esikatseluympäristön voi onnistuneesti ottaa käyttöön ja alustaa vain ympäristössä, joka käyttää demotopologiaa, jossa kaikki ympäristön osat otetaan käyttöön yhdessä näennäiskoneessa (VM).</span><span class="sxs-lookup"><span data-stu-id="9908b-112">The Commerce preview environment can be successfully deployed and initialized only in an environment that uses the demo topology, where all components of an environment are deployed in a single virtual machine (VM).</span></span> <span data-ttu-id="9908b-113">Tämän OneBox VM -topologian pääasiallinen rajoitus on samanaikaisten käyttäjien määrä, jota esikatseluympäristö voi tukea.</span><span class="sxs-lookup"><span data-stu-id="9908b-113">The main limitation of this OneBox VM topology is the number of concurrent users that the preview environment can support.</span></span>
- <span data-ttu-id="9908b-114">Commercen esikatseluympäristöä voi arvioida vain, kunnes Commerce-tuote on yleisesti saatavilla (GA).</span><span class="sxs-lookup"><span data-stu-id="9908b-114">The Commerce preview environment can be evaluated only until the general availability (GA) of the Commerce product.</span></span> <span data-ttu-id="9908b-115">Uudet esittely-ympäristöt ovat käytettävissä GA:n jälkeen.</span><span class="sxs-lookup"><span data-stu-id="9908b-115">New demo environments will be available after GA.</span></span>

## <a name="get-started"></a><span data-ttu-id="9908b-116">Aloittaminen</span><span class="sxs-lookup"><span data-stu-id="9908b-116">Get started</span></span>

<span data-ttu-id="9908b-117">Katso Commercen esikatseluympäristön tarjoaminen kohdasta [Commercen esikatseluympäristön tarjoaminen](provisioning-guide.md).</span><span class="sxs-lookup"><span data-stu-id="9908b-117">To provision the Commerce preview environment, see [Provision a Commerce preview environment](provisioning-guide.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9908b-118">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="9908b-118">Additional resources</span></span>

[<span data-ttu-id="9908b-119">Dynamics 365 Commercen esiversioympäristön valmistelu</span><span class="sxs-lookup"><span data-stu-id="9908b-119">Provision a Dynamics 365 Commerce preview environment</span></span>](provisioning-guide.md)

[<span data-ttu-id="9908b-120">Dynamics 365 Commercen esikatseluympäristön määrittäminen</span><span class="sxs-lookup"><span data-stu-id="9908b-120">Configure a Dynamics 365 Commerce preview environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="9908b-121">Valinnaisten ominaisuuksien määrittäminen Dynamics 365 Commercen esikatseluympäristöä varten</span><span class="sxs-lookup"><span data-stu-id="9908b-121">Configure optional features for a Dynamics 365 Commerce preview environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="9908b-122">Dynamics 365 Commerce -esikatseluympäristön usein kysytyt kysymykset</span><span class="sxs-lookup"><span data-stu-id="9908b-122">Dynamics 365 Commerce preview environment FAQ</span></span>](cpe-faq.md)
