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
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: v-chgri
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: cc6bffba6ee402c6b48d6a3c8f8356eb32b5423b
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/19/2021
ms.locfileid: "5478017"
---
# <a name="dynamics-365-commerce-evaluation-environment-overview"></a><span data-ttu-id="1b358-103">Dynamics 365 Commerce -arviointiympäristön yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="1b358-103">Dynamics 365 Commerce evaluation environment overview</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="1b358-104">Tässä ohjeaiheessa on yleiskatsaus Microsoft Dynamics 365 Commerce -arviointiympäristöstä.</span><span class="sxs-lookup"><span data-stu-id="1b358-104">This topic gives an overview of the Microsoft Dynamics 365 Commerce evaluation environment.</span></span>

> [!NOTE]
> <span data-ttu-id="1b358-105">Commercen arviointiympäristöt eivät ole yleisesti saatavana, ja ne myönnetään kumppaneille ja asiakkaille pyyntökohtaisesti.</span><span class="sxs-lookup"><span data-stu-id="1b358-105">Commerce evaluation environments aren't generally available, and are granted to partners and customers on a per-request basis.</span></span> <span data-ttu-id="1b358-106">Pyydä lisätietoja Microsoft-kumppanilta.</span><span class="sxs-lookup"><span data-stu-id="1b358-106">For more information, reach out to your Microsoft partner contact.</span></span>

<span data-ttu-id="1b358-107">Commercen arviointiympäristö on kokonaisvaltainen valinnainen Dynamics 365 Commercen ympäristö, jonka avulla kumppanit ja potentiaaliset asiakkaat voivat kokeilla Commerce-tuotetta.</span><span class="sxs-lookup"><span data-stu-id="1b358-107">The Commerce evaluation environment is an optional end-to-end environment of Dynamics 365 Commerce that lets partners and potential customers try out the Commerce product.</span></span>

<span data-ttu-id="1b358-108">Arviointiympäristöt on määritetty osittain valmiiksi, mikä vähentää valmistelun jälkeisten vaiheiden tarvetta.</span><span class="sxs-lookup"><span data-stu-id="1b358-108">Evaluation environments are partially preconfigured to reduce the required post-provisioning steps.</span></span>

<span data-ttu-id="1b358-109">Lukuun ottamatta joitakin pieniä rajoituksia, jotka eivät vaikuta ominaisuuksiin tai toimintoihin, Commercen arviointiympäristö on täydellinen Commerce-kokemus, jonka avulla asiakkaat ja toteutuskumppanit voivat arvioida tuotetta, antaa palautetta sekä tehdä sopivuus- ja aukkoanalyysiin.</span><span class="sxs-lookup"><span data-stu-id="1b358-109">Aside from some minor limitations that don't affect features or functionality, the Commerce evaluation environment provides the complete Commerce experience, and can be used by customers and implementation partners to evaluate the product, provide feedback, and do fit/gap analysis.</span></span>

## <a name="limitations-of-the-commerce-evaluation-environment"></a><span data-ttu-id="1b358-110">Commercen arviointiympäristön rajoitukset</span><span class="sxs-lookup"><span data-stu-id="1b358-110">Limitations of the Commerce evaluation environment</span></span>

<span data-ttu-id="1b358-111">Vaikka Commercen arviointiympäristö sisältää täydet Commercen ominaisuudet ja toiminnot, siinä on joitakin vähäisiä rajoituksia:</span><span class="sxs-lookup"><span data-stu-id="1b358-111">Although the Commerce evaluation environment provides the full set of Commerce features and functionality, there are some minor limitations:</span></span>

- <span data-ttu-id="1b358-112">Vaikka Commercen arviointiympäristössä itsessään ei ole maantieteellisiä rajoituksia, ympäristön osia, kuten Retail Cloud Scale Unit (RCSU) ja sähköisen kaupankäynnin sovelluksia voidaan valmistella vain Yhdysvalloissa.</span><span class="sxs-lookup"><span data-stu-id="1b358-112">Although the Commerce evaluation environment itself has no geographical limitations, components of the environment, such as the Retail Cloud Scale Unit (RCSU) and e-Commerce applications, should be provisioned only in the United States.</span></span>
- <span data-ttu-id="1b358-113">Commercen arviointiympäristön käyttö on rajoitettu 30 päivään siitä päivästä, jolloin sähköinen kaupankäynti on valmisteltu.</span><span class="sxs-lookup"><span data-stu-id="1b358-113">Use of the Commerce evaluation environment is limited to 30 days from the date when e-Commerce is provisioned.</span></span>
- <span data-ttu-id="1b358-114">Commercen arviointiympäristön käyttöönotto ja alustus onnistuu vain ympäristössä, jossa käytetään demotopologiaa ja jossa kaikki ympäristön osat otetaan käyttöön yhdessä pilvessä käytettävässä virtuaalikoneessa (VM).</span><span class="sxs-lookup"><span data-stu-id="1b358-114">The Commerce evaluation environment can be successfully deployed and initialized only in an environment that uses the demo topology, where all components of an environment are deployed on a single cloud-hosted virtual machine (VM).</span></span> <span data-ttu-id="1b358-115">Topologian pääasiallinen rajoitus on samanaikaisten käyttäjien määrä, jota ympäristö voi tukea.</span><span class="sxs-lookup"><span data-stu-id="1b358-115">The main limitation of this topology is the number of concurrent users that the environment can support.</span></span>

## <a name="get-started"></a><span data-ttu-id="1b358-116">Aloittaminen</span><span class="sxs-lookup"><span data-stu-id="1b358-116">Get started</span></span>

<span data-ttu-id="1b358-117">Lisätietoja Commercen arviointiympäristön valmistelusta on kohdassa [Commercen arviointiympäristön valmisteleminen](provisioning-guide.md).</span><span class="sxs-lookup"><span data-stu-id="1b358-117">To provision the Commerce evaluation environment, see [Provision a Commerce evaluation environment](provisioning-guide.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1b358-118">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="1b358-118">Additional resources</span></span>

[<span data-ttu-id="1b358-119">Dynamics 365 Commerce -arviointiympäristön valmisteleminen</span><span class="sxs-lookup"><span data-stu-id="1b358-119">Provision a Dynamics 365 Commerce evaluation environment</span></span>](provisioning-guide.md)

[<span data-ttu-id="1b358-120">Dynamics 365 Commerce -arviointiympäristön määritykset</span><span class="sxs-lookup"><span data-stu-id="1b358-120">Configure a Dynamics 365 Commerce evaluation environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="1b358-121">BOPIS:n määritykset Dynamics 365 Commerce -arviointiympäristössä</span><span class="sxs-lookup"><span data-stu-id="1b358-121">Configure BOPIS in a Dynamics 365 Commerce evaluation environment</span></span>](cpe-bopis.md)

[<span data-ttu-id="1b358-122">Dynamics 365 Commerce -arviointiympäristön valinnaisten ominaisuuksien määritykset</span><span class="sxs-lookup"><span data-stu-id="1b358-122">Configure optional features for a Dynamics 365 Commerce evaluation environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="1b358-123">Dynamics 365 Commerce -arviointiympäristön usein kysytyt kysymykset</span><span class="sxs-lookup"><span data-stu-id="1b358-123">Dynamics 365 Commerce evaluation environment FAQ</span></span>](cpe-faq.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
