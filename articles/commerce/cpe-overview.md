---
title: Dynamics 365 Commerce -arviointiympäristön yleiskatsaus
description: Tässä ohjeaiheessa on yleiskatsaus Microsoft Dynamics 365 Commerce -arviointiympäristöstä.
author: v-chgri
manager: annbe
ms.date: 07/16/2020
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
ms.openlocfilehash: 25c0574e8d4502bcb846fba0ddf913d81eded87b
ms.sourcegitcommit: 5175e3fae432016246244cf70fe05465f43de88c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/17/2020
ms.locfileid: "3599751"
---
# <a name="dynamics-365-commerce-evaluation-environment-overview"></a><span data-ttu-id="aa584-103">Dynamics 365 Commerce -arviointiympäristön yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="aa584-103">Dynamics 365 Commerce evaluation environment overview</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="aa584-104">Tässä ohjeaiheessa on yleiskatsaus Microsoft Dynamics 365 Commerce -arviointiympäristöstä.</span><span class="sxs-lookup"><span data-stu-id="aa584-104">This topic gives an overview of the Microsoft Dynamics 365 Commerce evaluation environment.</span></span>

> [!NOTE]
> <span data-ttu-id="aa584-105">Commercen arviointiympäristöt eivät ole yleisesti saatavana, ja ne myönnetään kumppaneille ja asiakkaille pyyntökohtaisesti.</span><span class="sxs-lookup"><span data-stu-id="aa584-105">Commerce evaluation environments aren't generally available, and are granted to partners and customers on a per-request basis.</span></span> <span data-ttu-id="aa584-106">Pyydä lisätietoja Microsoft-kumppanilta.</span><span class="sxs-lookup"><span data-stu-id="aa584-106">For more information, reach out to your Microsoft partner contact.</span></span>

## <a name="overview"></a><span data-ttu-id="aa584-107">Yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="aa584-107">Overview</span></span>

<span data-ttu-id="aa584-108">Commercen arviointiympäristö on kokonaisvaltainen valinnainen Dynamics 365 Commercen ympäristö, jonka avulla kumppanit ja potentiaaliset asiakkaat voivat kokeilla Commerce-tuotetta.</span><span class="sxs-lookup"><span data-stu-id="aa584-108">The Commerce evaluation environment is an optional end-to-end environment of Dynamics 365 Commerce that lets partners and potential customers try out the Commerce product.</span></span>

<span data-ttu-id="aa584-109">Arviointiympäristöt on määritetty osittain valmiiksi, mikä vähentää valmistelun jälkeisten vaiheiden tarvetta.</span><span class="sxs-lookup"><span data-stu-id="aa584-109">Evaluation environments are partially preconfigured to reduce the required post-provisioning steps.</span></span>

<span data-ttu-id="aa584-110">Lukuun ottamatta joitakin pieniä rajoituksia, jotka eivät vaikuta ominaisuuksiin tai toimintoihin, Commercen arviointiympäristö on täydellinen Commerce-kokemus, jonka avulla asiakkaat ja toteutuskumppanit voivat arvioida tuotetta, antaa palautetta sekä tehdä sopivuus- ja aukkoanalyysiin.</span><span class="sxs-lookup"><span data-stu-id="aa584-110">Aside from some minor limitations that don't affect features or functionality, the Commerce evaluation environment provides the complete Commerce experience, and can be used by customers and implementation partners to evaluate the product, provide feedback, and do fit/gap analysis.</span></span>

## <a name="limitations-of-the-commerce-evaluation-environment"></a><span data-ttu-id="aa584-111">Commercen arviointiympäristön rajoitukset</span><span class="sxs-lookup"><span data-stu-id="aa584-111">Limitations of the Commerce evaluation environment</span></span>

<span data-ttu-id="aa584-112">Vaikka Commercen arviointiympäristö sisältää täydet Commercen ominaisuudet ja toiminnot, siinä on joitakin vähäisiä rajoituksia:</span><span class="sxs-lookup"><span data-stu-id="aa584-112">Although the Commerce evaluation environment provides the full set of Commerce features and functionality, there are some minor limitations:</span></span>

- <span data-ttu-id="aa584-113">Vaikka Commercen arviointiympäristössä itsessään ei ole maantieteellisiä rajoituksia, ympäristön osia, kuten Retail Cloud Scale Unit (RCSU) ja sähköisen kaupankäynnin sovelluksia voidaan valmistella vain Yhdysvalloissa.</span><span class="sxs-lookup"><span data-stu-id="aa584-113">Although the Commerce evaluation environment itself has no geographical limitations, components of the environment, such as the Retail Cloud Scale Unit (RCSU) and e-Commerce applications, should be provisioned only in the United States.</span></span>
- <span data-ttu-id="aa584-114">Commercen arviointiympäristön käyttö on rajoitettu 30 päivään siitä päivästä, jolloin sähköinen kaupankäynti on valmisteltu.</span><span class="sxs-lookup"><span data-stu-id="aa584-114">Use of the Commerce evaluation environment is limited to 30 days from the date when e-Commerce is provisioned.</span></span>
- <span data-ttu-id="aa584-115">Commercen arviointiympäristön käyttöönotto ja alustus onnistuu vain ympäristössä, jossa käytetään demotopologiaa ja jossa kaikki ympäristön osat otetaan käyttöön yhdessä pilvessä käytettävässä virtuaalikoneessa (VM).</span><span class="sxs-lookup"><span data-stu-id="aa584-115">The Commerce evaluation environment can be successfully deployed and initialized only in an environment that uses the demo topology, where all components of an environment are deployed on a single cloud-hosted virtual machine (VM).</span></span> <span data-ttu-id="aa584-116">Topologian pääasiallinen rajoitus on samanaikaisten käyttäjien määrä, jota ympäristö voi tukea.</span><span class="sxs-lookup"><span data-stu-id="aa584-116">The main limitation of this topology is the number of concurrent users that the environment can support.</span></span>

## <a name="get-started"></a><span data-ttu-id="aa584-117">Aloittaminen</span><span class="sxs-lookup"><span data-stu-id="aa584-117">Get started</span></span>

<span data-ttu-id="aa584-118">Lisätietoja Commercen arviointiympäristön valmistelusta on kohdassa [Commercen arviointiympäristön valmisteleminen](provisioning-guide.md).</span><span class="sxs-lookup"><span data-stu-id="aa584-118">To provision the Commerce evaluation environment, see [Provision a Commerce evaluation environment](provisioning-guide.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="aa584-119">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="aa584-119">Additional resources</span></span>

[<span data-ttu-id="aa584-120">Dynamics 365 Commerce -arviointiympäristön valmisteleminen</span><span class="sxs-lookup"><span data-stu-id="aa584-120">Provision a Dynamics 365 Commerce evaluation environment</span></span>](provisioning-guide.md)

[<span data-ttu-id="aa584-121">Dynamics 365 Commerce -arviointiympäristön määritykset</span><span class="sxs-lookup"><span data-stu-id="aa584-121">Configure a Dynamics 365 Commerce evaluation environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="aa584-122">BOPIS:n määritykset Dynamics 365 Commerce -arviointiympäristössä</span><span class="sxs-lookup"><span data-stu-id="aa584-122">Configure BOPIS in a Dynamics 365 Commerce evaluation environment</span></span>](cpe-bopis.md)

[<span data-ttu-id="aa584-123">Dynamics 365 Commerce -arviointiympäristön valinnaisten ominaisuuksien määritykset</span><span class="sxs-lookup"><span data-stu-id="aa584-123">Configure optional features for a Dynamics 365 Commerce evaluation environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="aa584-124">Dynamics 365 Commerce -arviointiympäristön usein kysytyt kysymykset</span><span class="sxs-lookup"><span data-stu-id="aa584-124">Dynamics 365 Commerce evaluation environment FAQ</span></span>](cpe-faq.md)
