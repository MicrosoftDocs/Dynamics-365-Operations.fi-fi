---
title: Luokitukset ja arvostelut – yleiskatsaus
description: Tämä ohjeaihe sisältää Microsoft Dynamics 365 Commercen luokitukset ja arvostelut.
author: gvrmohanreddy
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: ed31982dad8af4509d8dd0615ae53e3d3806640f
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4979775"
---
# <a name="ratings-and-reviews-overview"></a><span data-ttu-id="4d7fa-103">Luokitukset ja arvostelut – yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="4d7fa-103">Ratings and reviews overview</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="4d7fa-104">Tämä ohjeaihe sisältää Microsoft Dynamics 365 Commercen luokitukset ja arvostelut.</span><span class="sxs-lookup"><span data-stu-id="4d7fa-104">This topic covers ratings and reviews in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="4d7fa-105">Yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="4d7fa-105">Overview</span></span>

<span data-ttu-id="4d7fa-106">Luokitukset ja arvostelut ovat tärkeä osa sähköisen kaupankäynnin asiakkaille, jotka haluavat tietää muiden asiakkaiden mielipiteen tuotteesta.</span><span class="sxs-lookup"><span data-stu-id="4d7fa-106">Ratings and reviews are crucial for e-Commerce customers who want to know how other customers perceive a product.</span></span> <span data-ttu-id="4d7fa-107">Ne voivat myös auttaa kuluttajia tekemään ostopäätöksiä.</span><span class="sxs-lookup"><span data-stu-id="4d7fa-107">They can also help consumers make purchase decisions.</span></span> <span data-ttu-id="4d7fa-108">Dynamics 365 Commerce -sovelluksessa luokitusten ja arvostelujen ratkaisun avulla jälleenmyyjät keräävät tuotearvosteluja ja -luokituksia asiakkailta.</span><span class="sxs-lookup"><span data-stu-id="4d7fa-108">In Dynamics 365 Commerce, the ratings and reviews solution lets retailers capture product reviews and ratings from customers.</span></span> <span data-ttu-id="4d7fa-109">Jälleenmyyjät voivat tämän jälkeen näyttää keskimääräiset arvostelujen ja luokitusten tiedot sähköisen kaupankäynnin sivustossa.</span><span class="sxs-lookup"><span data-stu-id="4d7fa-109">Retailers can then show average ratings and review information across their e-Commerce website.</span></span>

<span data-ttu-id="4d7fa-110">Keskimääräiset luokitustiedot näytetään myyntipiste- ja puhelinkeskuskanavissa.</span><span class="sxs-lookup"><span data-stu-id="4d7fa-110">Average rating information is shown in point of sale (POS) and call center channels.</span></span> <span data-ttu-id="4d7fa-111">Tämän vuoksi myyntikumppanit voivat käyttää niitä auttaessaan käyttäjiä tekemään päätöksiä.</span><span class="sxs-lookup"><span data-stu-id="4d7fa-111">Therefore, sales associates can use it to help users make decisions.</span></span> <span data-ttu-id="4d7fa-112">Luokitukset ja arvostelut voivat toimia myös palautemekanismina, jota jälleenmyyjät voivat käyttää parantaakseen tuotteen laatua ja kasvattaessaan samalla myyntiä.</span><span class="sxs-lookup"><span data-stu-id="4d7fa-112">Ratings and reviews can also serve as a feedback mechanism that retailers can use to improve the quality of a product and therefore increase sales.</span></span>

<span data-ttu-id="4d7fa-113">Luokitukset ja arvostelut -toiminto Dynamics 365 Commerce -sovelluksessa on monikanavaratkaisu. Se on saatavana ympäristön osana.</span><span class="sxs-lookup"><span data-stu-id="4d7fa-113">Ratings and reviews functionality in Dynamics 365 Commerce is an omnichannel solution and is natively available as part of the platform.</span></span> <span data-ttu-id="4d7fa-114">Luokitukset ja arvostelut -ratkaisu on luotu Microsoft Azuren avulla. Tämä mahdollistaa korkean skaalautuvuuden ja luotettavuuden.</span><span class="sxs-lookup"><span data-stu-id="4d7fa-114">The ratings and reviews solution is built on top of Microsoft Azure, which provides high scalability and reliability.</span></span>

<span data-ttu-id="4d7fa-115">Seuraavassa kuvassa näkyy, miten luokitukset ja arvostelut -ratkaisu toimii Dynamics 365 Commerce -sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="4d7fa-115">The following illustration shows how the ratings and reviews solution works in Dynamics 365 Commerce.</span></span>

![Luokitukset ja arvostelut Dynamics 365 for Commerce -sovelluksessa](media/Dynamics-365-Commerce-Ratings-and-Reviews-Overview.jpg)

<span data-ttu-id="4d7fa-117">Luokitukset ja arvostelut -ratkaisu Dynamics 365 Commerce -sovelluksessa käyttää Azure Cognitive Services -ratkaisua. Sen avulla tarjotaan sopimattomien sanojen valvontaa 40 kielellä.</span><span class="sxs-lookup"><span data-stu-id="4d7fa-117">The ratings and reviews solution in Dynamics 365 Commerce uses Azure Cognitive Services to offer automatic moderation of profane words in 40 languages.</span></span> <span data-ttu-id="4d7fa-118">Koska valvonnassa ei tarvita ihmisiä, valvontakustannukset pienenevät.</span><span class="sxs-lookup"><span data-stu-id="4d7fa-118">Because human approval isn't required, moderation costs are reduced.</span></span> <span data-ttu-id="4d7fa-119">Järjestelmä tarjoaa myös valvontatyökaluja, joiden avulla voidaan vastata asiakkaiden kyselyihin, palautteeseen ja poistopyyntöihin sekä käyttäjien tietopyyntöihin.</span><span class="sxs-lookup"><span data-stu-id="4d7fa-119">The system also offers moderator tools that can be used to respond to customer concerns, feedback, and take-down requests, and to address data requests from users.</span></span>

<span data-ttu-id="4d7fa-120">Luokitukset ja arvostelut -ratkaisu sisältää pienoissovelluksia, jotka näyttävät arvostelujen yhteenvedot tuoteluetteloissa, hakutuloksissa, tuotetietosivulla ja muissa paikoissa.</span><span class="sxs-lookup"><span data-stu-id="4d7fa-120">The ratings and reviews solution provides widgets that show rating summaries in product lists, in search results, on product details page, and in other places.</span></span> <span data-ttu-id="4d7fa-121">Pienoissovellukset näyttävät täydelliset luokitusluettelot ja ne sisältävät myös lajittelu- ja suodatusasetukset.</span><span class="sxs-lookup"><span data-stu-id="4d7fa-121">The widgets show complete review lists, and they also provide sorting and filtering options.</span></span>

<span data-ttu-id="4d7fa-122">Luokitukset ja arvostelut -ratkaisu sisältää myös Business Intelligence (BI) -mallin, joka sisältää mittarijoukon. Sen avulla saadaan tietoja luokituksista ja arvosteluista.</span><span class="sxs-lookup"><span data-stu-id="4d7fa-122">The ratings and reviews solution also provides a business intelligence (BI) template that includes a set of metrics to provide insights into ratings and reviews.</span></span> <span data-ttu-id="4d7fa-123">Luokitusten ja arvostelujen tiedot voidaan viedä tarkempaa analysointia varten.</span><span class="sxs-lookup"><span data-stu-id="4d7fa-123">Ratings and reviews data can be exported for further analysis.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4d7fa-124">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="4d7fa-124">Additional resources</span></span>

[<span data-ttu-id="4d7fa-125">Osallistu käyttääksesi luokituksia ja arvosteluja</span><span class="sxs-lookup"><span data-stu-id="4d7fa-125">Opt in to use ratings and reviews</span></span>](opt-in-ratings-reviews.md)

[<span data-ttu-id="4d7fa-126">Hallitse luokituksia ja arvosteluja</span><span class="sxs-lookup"><span data-stu-id="4d7fa-126">Manage ratings and reviews</span></span>](manage-reviews.md)

[<span data-ttu-id="4d7fa-127">Määritä luokitukset ja arvostelut</span><span class="sxs-lookup"><span data-stu-id="4d7fa-127">Configure ratings and reviews</span></span>](configure-ratings-reviews.md)

[<span data-ttu-id="4d7fa-128">Tuoteluokitusten synkronoiminen Dynamics 365 Commerceissa</span><span class="sxs-lookup"><span data-stu-id="4d7fa-128">Sync product ratings in Dynamics 365 Commerce</span></span>](sync-product-ratings.md)
