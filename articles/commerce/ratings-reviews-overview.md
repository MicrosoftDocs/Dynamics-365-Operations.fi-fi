---
title: Luokitukset ja arvostelut – yleiskatsaus
description: Tämä ohjeaihe sisältää Microsoft Dynamics 365 Commercen luokitukset ja arvostelut.
author: gvrmohanreddy
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 0788091755fb784621e972a0573f7004952e8e11
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5792096"
---
# <a name="ratings-and-reviews-overview"></a><span data-ttu-id="a579f-103">Luokitukset ja arvostelut – yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="a579f-103">Ratings and reviews overview</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="a579f-104">Tämä ohjeaihe sisältää Microsoft Dynamics 365 Commercen luokitukset ja arvostelut.</span><span class="sxs-lookup"><span data-stu-id="a579f-104">This topic covers ratings and reviews in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="a579f-105">Yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="a579f-105">Overview</span></span>

<span data-ttu-id="a579f-106">Luokitukset ja arvostelut ovat tärkeä osa sähköisen kaupankäynnin asiakkaille, jotka haluavat tietää muiden asiakkaiden mielipiteen tuotteesta.</span><span class="sxs-lookup"><span data-stu-id="a579f-106">Ratings and reviews are crucial for e-Commerce customers who want to know how other customers perceive a product.</span></span> <span data-ttu-id="a579f-107">Ne voivat myös auttaa kuluttajia tekemään ostopäätöksiä.</span><span class="sxs-lookup"><span data-stu-id="a579f-107">They can also help consumers make purchase decisions.</span></span> <span data-ttu-id="a579f-108">Dynamics 365 Commerce -sovelluksessa luokitusten ja arvostelujen ratkaisun avulla jälleenmyyjät keräävät tuotearvosteluja ja -luokituksia asiakkailta.</span><span class="sxs-lookup"><span data-stu-id="a579f-108">In Dynamics 365 Commerce, the ratings and reviews solution lets retailers capture product reviews and ratings from customers.</span></span> <span data-ttu-id="a579f-109">Jälleenmyyjät voivat tämän jälkeen näyttää keskimääräiset arvostelujen ja luokitusten tiedot sähköisen kaupankäynnin sivustossa.</span><span class="sxs-lookup"><span data-stu-id="a579f-109">Retailers can then show average ratings and review information across their e-Commerce website.</span></span>

<span data-ttu-id="a579f-110">Keskimääräiset luokitustiedot näytetään myyntipiste- ja puhelinkeskuskanavissa.</span><span class="sxs-lookup"><span data-stu-id="a579f-110">Average rating information is shown in point of sale (POS) and call center channels.</span></span> <span data-ttu-id="a579f-111">Tämän vuoksi myyntikumppanit voivat käyttää niitä auttaessaan käyttäjiä tekemään päätöksiä.</span><span class="sxs-lookup"><span data-stu-id="a579f-111">Therefore, sales associates can use it to help users make decisions.</span></span> <span data-ttu-id="a579f-112">Luokitukset ja arvostelut voivat toimia myös palautemekanismina, jota jälleenmyyjät voivat käyttää parantaakseen tuotteen laatua ja kasvattaessaan samalla myyntiä.</span><span class="sxs-lookup"><span data-stu-id="a579f-112">Ratings and reviews can also serve as a feedback mechanism that retailers can use to improve the quality of a product and therefore increase sales.</span></span>

<span data-ttu-id="a579f-113">Luokitukset ja arvostelut -toiminto Dynamics 365 Commerce -sovelluksessa on monikanavaratkaisu. Se on saatavana ympäristön osana.</span><span class="sxs-lookup"><span data-stu-id="a579f-113">Ratings and reviews functionality in Dynamics 365 Commerce is an omnichannel solution and is natively available as part of the platform.</span></span> <span data-ttu-id="a579f-114">Luokitukset ja arvostelut -ratkaisu on luotu Microsoft Azuren avulla. Tämä mahdollistaa korkean skaalautuvuuden ja luotettavuuden.</span><span class="sxs-lookup"><span data-stu-id="a579f-114">The ratings and reviews solution is built on top of Microsoft Azure, which provides high scalability and reliability.</span></span>

<span data-ttu-id="a579f-115">Seuraavassa kuvassa näkyy, miten luokitukset ja arvostelut -ratkaisu toimii Dynamics 365 Commerce -sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="a579f-115">The following illustration shows how the ratings and reviews solution works in Dynamics 365 Commerce.</span></span>

![Luokitukset ja arvostelut Dynamics 365 for Commerce -sovelluksessa](media/Dynamics-365-Commerce-Ratings-and-Reviews-Overview.jpg)

<span data-ttu-id="a579f-117">Luokitukset ja arvostelut -ratkaisu Dynamics 365 Commerce -sovelluksessa käyttää Azure Cognitive Services -ratkaisua. Sen avulla tarjotaan sopimattomien sanojen valvontaa 40 kielellä.</span><span class="sxs-lookup"><span data-stu-id="a579f-117">The ratings and reviews solution in Dynamics 365 Commerce uses Azure Cognitive Services to offer automatic moderation of profane words in 40 languages.</span></span> <span data-ttu-id="a579f-118">Koska valvonnassa ei tarvita ihmisiä, valvontakustannukset pienenevät.</span><span class="sxs-lookup"><span data-stu-id="a579f-118">Because human approval isn't required, moderation costs are reduced.</span></span> <span data-ttu-id="a579f-119">Järjestelmä tarjoaa myös valvontatyökaluja, joiden avulla voidaan vastata asiakkaiden kyselyihin, palautteeseen ja poistopyyntöihin sekä käyttäjien tietopyyntöihin.</span><span class="sxs-lookup"><span data-stu-id="a579f-119">The system also offers moderator tools that can be used to respond to customer concerns, feedback, and take-down requests, and to address data requests from users.</span></span>

<span data-ttu-id="a579f-120">Luokitukset ja arvostelut -ratkaisu sisältää pienoissovelluksia, jotka näyttävät arvostelujen yhteenvedot tuoteluetteloissa, hakutuloksissa, tuotetietosivulla ja muissa paikoissa.</span><span class="sxs-lookup"><span data-stu-id="a579f-120">The ratings and reviews solution provides widgets that show rating summaries in product lists, in search results, on product details page, and in other places.</span></span> <span data-ttu-id="a579f-121">Pienoissovellukset näyttävät täydelliset luokitusluettelot ja ne sisältävät myös lajittelu- ja suodatusasetukset.</span><span class="sxs-lookup"><span data-stu-id="a579f-121">The widgets show complete review lists, and they also provide sorting and filtering options.</span></span>

<span data-ttu-id="a579f-122">Luokitukset ja arvostelut -ratkaisu sisältää myös Business Intelligence (BI) -mallin, joka sisältää mittarijoukon. Sen avulla saadaan tietoja luokituksista ja arvosteluista.</span><span class="sxs-lookup"><span data-stu-id="a579f-122">The ratings and reviews solution also provides a business intelligence (BI) template that includes a set of metrics to provide insights into ratings and reviews.</span></span> <span data-ttu-id="a579f-123">Luokitusten ja arvostelujen tiedot voidaan viedä tarkempaa analysointia varten.</span><span class="sxs-lookup"><span data-stu-id="a579f-123">Ratings and reviews data can be exported for further analysis.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a579f-124">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="a579f-124">Additional resources</span></span>

[<span data-ttu-id="a579f-125">Osallistu käyttääksesi luokituksia ja arvosteluja</span><span class="sxs-lookup"><span data-stu-id="a579f-125">Opt in to use ratings and reviews</span></span>](opt-in-ratings-reviews.md)

[<span data-ttu-id="a579f-126">Hallitse luokituksia ja arvosteluja</span><span class="sxs-lookup"><span data-stu-id="a579f-126">Manage ratings and reviews</span></span>](manage-reviews.md)

[<span data-ttu-id="a579f-127">Määritä luokitukset ja arvostelut</span><span class="sxs-lookup"><span data-stu-id="a579f-127">Configure ratings and reviews</span></span>](configure-ratings-reviews.md)

[<span data-ttu-id="a579f-128">Tuoteluokitusten synkronoiminen Dynamics 365 Commercessa</span><span class="sxs-lookup"><span data-stu-id="a579f-128">Sync product ratings in Dynamics 365 Commerce</span></span>](sync-product-ratings.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]