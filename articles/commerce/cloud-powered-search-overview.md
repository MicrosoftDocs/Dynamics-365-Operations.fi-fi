---
title: Pilvipohjaisen haun yleiskatsaus
description: Tässä ohjeaiheessa on yleiskatsaus pilvipohjaisesta hausta Microsoft Dynamics 365 Commerce -sovelluksessa.
author: v-chgri
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
ms.author: asharchw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: de0981d3200c2b1d62cab7600d2382bd11dd4b20
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002240"
---
# <a name="cloud-powered-search-overview"></a><span data-ttu-id="ef1cb-103">Pilvipohjaisen haun yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="ef1cb-103">Cloud-powered search overview</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="ef1cb-104">Tässä ohjeaiheessa on yleiskatsaus pilvipohjaisesta hausta Microsoft Dynamics 365 Commerce -sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="ef1cb-104">This topic gives an overview of cloud-powered search in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="ef1cb-105">Yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="ef1cb-105">Overview</span></span>

<span data-ttu-id="ef1cb-106">Tuotteiden löydettävyyden avulla varmistetaan, että asiakkaat löytävät tuotteita nopeasti ja helposti selaamalla luokkia sekä tekemällä hakuja ja suodattamalla luokkia.</span><span class="sxs-lookup"><span data-stu-id="ef1cb-106">Product discoverability helps guarantee that customers can quickly and easily find products by browsing categories, searching, and filtering.</span></span> <span data-ttu-id="ef1cb-107">Vähittäiskauppiaat pitävät tuotteen etsintätyökalua ensisijaisena työkaluna asiakkaan vuorovaikutuksessa kaikkien vähittäismyyntikanavien kautta.</span><span class="sxs-lookup"><span data-stu-id="ef1cb-107">Retailers consider product discovery a primary tool for customer interaction across all retail channels.</span></span>

<span data-ttu-id="ef1cb-108">Asiakkaat ovat tottuneet lähes välittömiin vastausaikoihin verkon hakukoneissa, kehittyneissä sähköisen kaupankäynnin sivustoissa, yhteisöpalvelusovelluksissa, automaattisissa ehdotuksissa hakuehdotusten syöttämisen yhteydessä, kohdistetussa siirtymisessä ja korostuksissa.</span><span class="sxs-lookup"><span data-stu-id="ef1cb-108">Customers are accustomed to the nearly instantaneous response times of web search engines, sophisticated e-Commerce websites, social apps, automatic suggestions that appear as they type search terms, faceted navigation, and highlighting.</span></span> <span data-ttu-id="ef1cb-109">Jos asiakkaat eivät löydä hakemaansa tuotetta riittävän nopeasti yhdestä sähköisen kaupankäynnin myymälästä, he siirtyvät nopeasti toiseen sähköisen kaupankäynnin myymälään.</span><span class="sxs-lookup"><span data-stu-id="ef1cb-109">If customers can't find the product that they are looking for quickly enough in one e-Commerce store, they won't hesitate to go to a different e-Commerce store.</span></span>

<span data-ttu-id="ef1cb-110">Pilvipohjaisen tuotteen etsintätoiminto Dynamics 365 Commerce -sovelluksessa auttaa jälleenmyyjiä lisäämään asiakkaiden pysymistä ja eri kanavien muuntomääriä sekä sähköisen kaupankäynnin kanavissa että myyntipistekanavissa.</span><span class="sxs-lookup"><span data-stu-id="ef1cb-110">The cloud-powered product discoverability in Dynamics 365 Commerce helps retailers continue to increase consumer retention and conversion rates across all channels, both e-Commerce channels and point of sale (POS) channels.</span></span>

<span data-ttu-id="ef1cb-111">Dynamics 365 Commercen hakukokemus on parantanut ominaisuuksia, joiden avulla jälleenmyyjät saavuttavat aiempaa paremman tuotteiden löydettävyyden.</span><span class="sxs-lookup"><span data-stu-id="ef1cb-111">The Dynamics 365 Commerce search experience has improved capabilities to help retailers achieve better product discoverability.</span></span> <span data-ttu-id="ef1cb-112">Samalla nämä ominaisuudet tarjoavat skaalautuvuutta ja suorituskykyä, jota sähköisen kaupankäynnin liikenne vaatii.</span><span class="sxs-lookup"><span data-stu-id="ef1cb-112">At the same time, these capabilities deliver the scalability and performance that are required for e-Commerce traffic.</span></span>

## <a name="browse-and-search"></a><span data-ttu-id="ef1cb-113">Selaaminen ja hakeminen</span><span class="sxs-lookup"><span data-stu-id="ef1cb-113">Browse and search</span></span>

<span data-ttu-id="ef1cb-114">Hakurelevanssi ja suorituskyky ovat tärkeitä tekijöitä monikanavakokemuksessa, koska tuotteen löydettävyys riippuu suureksi osaksi tiedonhaun ja sisällön navigoinnin hakutoiminnoista.</span><span class="sxs-lookup"><span data-stu-id="ef1cb-114">Search relevance and performance are key factors in the omnichannel experience, because product discovery relies primarily on search functionality for information retrieval and content navigation.</span></span> <span data-ttu-id="ef1cb-115">Tehokas selaus- ja hakukokemus auttaa muunnon lisäämisessä.</span><span class="sxs-lookup"><span data-stu-id="ef1cb-115">An effective and efficient browse and search experience helps increase conversion.</span></span>

<span data-ttu-id="ef1cb-116">Seuraavassa kuvassa on esimerkki tyypillisestä selaus- ja hakutoiminnosta.</span><span class="sxs-lookup"><span data-stu-id="ef1cb-116">The following illustration shows an example of typical browse and search functionality.</span></span>

![Aloitussivun haku](./media/SearchLanding.png)

## <a name="faceted-navigation-and-choice-summary"></a><span data-ttu-id="ef1cb-118">Kohdistetun siirtymisen ja valinnan yhteenveto</span><span class="sxs-lookup"><span data-stu-id="ef1cb-118">Faceted navigation and choice summary</span></span> 

<span data-ttu-id="ef1cb-119">Kohdistettu siirtyminen auttaa asiakkaita selaamaan sisältöä helpommin, koska he voivat suodattaa termeihin linkitettyjä tarkenteita termijoukossa.</span><span class="sxs-lookup"><span data-stu-id="ef1cb-119">Faceted navigation helps customers more easily browse for content by letting them filter on refiners that are linked to terms in a term set.</span></span> <span data-ttu-id="ef1cb-120">Kun asiakas on valinnut ja ottanut tarkenteet käyttöön, näkyviin tulee valintojen yhteenveto.</span><span class="sxs-lookup"><span data-stu-id="ef1cb-120">After a customer has selected and applied refiners, a summary of the choices is shown.</span></span> 

<span data-ttu-id="ef1cb-121">Kohdistetun siirtymisen avulla voi määrittää erilaisia tarkenteita eri termijoukon termeille ilman, että niille on luotava erillisiä sivuja.</span><span class="sxs-lookup"><span data-stu-id="ef1cb-121">By using faceted navigation, you can configure different refiners for different terms in a term set, without having to create additional pages.</span></span> 

<span data-ttu-id="ef1cb-122">Seuraavassa kuvassa on esimerkki kohdistetun siirtymisen käytöstä haussa.</span><span class="sxs-lookup"><span data-stu-id="ef1cb-122">The following illustration shows an example where faceted navigation is used in a search.</span></span>

![Valinnan yhteenveto](./media/ChoiceSummary.png)

## <a name="immersive-autosuggest"></a><span data-ttu-id="ef1cb-124">Mukaansatempaava automaattinen ehdotustoiminto</span><span class="sxs-lookup"><span data-stu-id="ef1cb-124">Immersive autosuggest</span></span>

<span data-ttu-id="ef1cb-125">Nykyinen automaattisen ehdotuksen toiminto näyttää avainsanat, jotka käynnistävät vastaavan avainsanan haun.</span><span class="sxs-lookup"><span data-stu-id="ef1cb-125">Current autosuggest functionality just shows keywords that trigger a search for the matching keyword.</span></span> <span data-ttu-id="ef1cb-126">Dynamics 365 Commercen uusien parannusten avulla asiakkaat voivat usein löytää linkkejä tuotteisiin ennen kuin he ovat kirjoittaneet hakusanoja.</span><span class="sxs-lookup"><span data-stu-id="ef1cb-126">Because of new enhancements in Dynamics 365 Commerce, customers can often discover links to products before they have finished typing.</span></span>

<span data-ttu-id="ef1cb-127">Dynamics 365 Commerce tukee myös eri luokkiin kuuluvien avainsanavastaavuuksien toimintoja.</span><span class="sxs-lookup"><span data-stu-id="ef1cb-127">Dynamics 365 Commerce also supports functionality for keyword matches in various categories.</span></span> <span data-ttu-id="ef1cb-128">Tämän toiminnon avulla asiakkaan näkevät vastaavien avainsanojen määrän eri luokissa. He voivat myös käynnistää avainsanahaun muissa luokissa.</span><span class="sxs-lookup"><span data-stu-id="ef1cb-128">This functionality lets customers see the number of matching keywords across categories and trigger a search for a keyword in other categories.</span></span>

<span data-ttu-id="ef1cb-129">Seuraavassa kuvassa näkyy esimerkki, jossa käytetään mukaansatempaavaa automaattista ehdotustoimintoa.</span><span class="sxs-lookup"><span data-stu-id="ef1cb-129">The following illustration shows an example where immersive autosuggest is being used.</span></span>

![Mukaansatempaava automaattinen ehdotustoiminto](./media/ImmersiveAutoSuggestUX.png)

## <a name="sort"></a><span data-ttu-id="ef1cb-131">Lajittele</span><span class="sxs-lookup"><span data-stu-id="ef1cb-131">Sort</span></span>

<span data-ttu-id="ef1cb-132">Dynamics 365 Commercen parannellun lajittelun avulla asiakkaat voivat lajitella, hakea ja selata hakutuloksia ja tarkentaa niitä erilaisten ehtojen, kuten hinnan, tuotenimen ja tuotenumeron avulla.</span><span class="sxs-lookup"><span data-stu-id="ef1cb-132">Enhanced sorting in Dynamics 365 Commerce lets customers sort, search, and browse search results, and refine them by criteria such as price, product name, and product number.</span></span> <span data-ttu-id="ef1cb-133">Asiakkaat voivat myös lajitella tulokset sen mukaan, onko tuote uusi, kuuluuko se myydyimpien joukkoon vai onko se lisätty äskettäin.</span><span class="sxs-lookup"><span data-stu-id="ef1cb-133">Customers can also sort results based on whether a product is new, top-selling, or recently added.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ef1cb-134">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="ef1cb-134">Additional resources</span></span>

[<span data-ttu-id="ef1cb-135">Luokan oletussaapumis- ja oletushakutulossivu</span><span class="sxs-lookup"><span data-stu-id="ef1cb-135">Default category landing page and search results page</span></span>](category-search-page-overview.md)

[<span data-ttu-id="ef1cb-136">SEO-metatietojen hallinta</span><span class="sxs-lookup"><span data-stu-id="ef1cb-136">Manage SEO metadata</span></span>](manage-seo-metadata.md)
