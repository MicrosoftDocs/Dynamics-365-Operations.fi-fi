---
title: Pilvipohjaisen haun yleiskatsaus
description: Tässä ohjeaiheessa on yleiskatsaus pilvipohjaisesta hausta Microsoft Dynamics 365 Commerce -sovelluksessa.
author: ashishmsft
manager: annbe
ms.date: 06/29/2020
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
ms.openlocfilehash: 00a3de2515cea341f7529b8cb6cb2caae5e33d22
ms.sourcegitcommit: ce397c2759f642c595e30fef58a770b50360b2bd
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/01/2020
ms.locfileid: "3527440"
---
# <a name="cloud-powered-search-overview"></a><span data-ttu-id="91a04-103">Pilvipohjaisen haun yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="91a04-103">Cloud-powered search overview</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="91a04-104">Tässä ohjeaiheessa on yleiskatsaus pilvipohjaisesta hausta Microsoft Dynamics 365 Commerce -sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="91a04-104">This topic gives an overview of cloud-powered search in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="91a04-105">Yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="91a04-105">Overview</span></span>

<span data-ttu-id="91a04-106">Tuotteiden löydettävyyden avulla varmistetaan, että asiakkaat löytävät tuotteita nopeasti ja helposti selaamalla luokkia sekä tekemällä hakuja ja suodattamalla luokkia.</span><span class="sxs-lookup"><span data-stu-id="91a04-106">Product discoverability helps guarantee that customers can quickly and easily find products by browsing categories, searching, and filtering.</span></span> <span data-ttu-id="91a04-107">Vähittäiskauppiaat pitävät tuotteen etsintätyökalua ensisijaisena työkaluna asiakkaan vuorovaikutuksessa kaikkien kanavien kautta.</span><span class="sxs-lookup"><span data-stu-id="91a04-107">Retailers consider product discovery a primary tool for customer interaction across all channels.</span></span>

<span data-ttu-id="91a04-108">Asiakkaat ovat tottuneet lähes välittömiin vastausaikoihin verkon hakukoneissa, kehittyneissä sähköisen kaupankäynnin sivustoissa, yhteisöpalvelusovelluksissa, automaattisissa ehdotuksissa hakuehdotusten syöttämisen yhteydessä, kohdistetussa siirtymisessä ja korostuksissa.</span><span class="sxs-lookup"><span data-stu-id="91a04-108">Customers are accustomed to the nearly instantaneous response times of web search engines, sophisticated e-Commerce websites, social apps, automatic suggestions that appear as they type search terms, faceted navigation, and highlighting.</span></span> <span data-ttu-id="91a04-109">Jos asiakkaat eivät löydä hakemaansa tuotetta riittävän nopeasti yhdestä sähköisen kaupankäynnin myymälästä, he siirtyvät nopeasti toiseen sähköisen kaupankäynnin myymälään.</span><span class="sxs-lookup"><span data-stu-id="91a04-109">If customers can't find the product that they are looking for quickly enough in one e-Commerce store, they won't hesitate to go to a different e-Commerce store.</span></span>

<span data-ttu-id="91a04-110">Pilvipohjaisen tuotteen etsintätoiminto Dynamics 365 Commerce -sovelluksessa auttaa jälleenmyyjiä lisäämään asiakkaiden pysymistä ja eri kanavien muuntomääriä sekä sähköisen kaupankäynnin kanavissa että myyntipistekanavissa.</span><span class="sxs-lookup"><span data-stu-id="91a04-110">The cloud-powered product discoverability in Dynamics 365 Commerce helps retailers continue to increase consumer retention and conversion rates across all channels, both e-Commerce channels and point of sale (POS) channels.</span></span>

<span data-ttu-id="91a04-111">Dynamics 365 Commercen hakukokemus on parantanut ominaisuuksia, joiden avulla jälleenmyyjät saavuttavat aiempaa paremman tuotteiden löydettävyyden.</span><span class="sxs-lookup"><span data-stu-id="91a04-111">The Dynamics 365 Commerce search experience has improved capabilities to help retailers achieve better product discoverability.</span></span> <span data-ttu-id="91a04-112">Samalla nämä ominaisuudet tarjoavat skaalautuvuutta ja suorituskykyä, jota sähköisen kaupankäynnin liikenne vaatii.</span><span class="sxs-lookup"><span data-stu-id="91a04-112">At the same time, these capabilities deliver the scalability and performance that are required for e-Commerce traffic.</span></span>

## <a name="browse-and-search"></a><span data-ttu-id="91a04-113">Selaaminen ja hakeminen</span><span class="sxs-lookup"><span data-stu-id="91a04-113">Browse and search</span></span>

<span data-ttu-id="91a04-114">Hakurelevanssi ja suorituskyky ovat tärkeitä tekijöitä monikanavakokemuksessa, koska tuotteen löydettävyys riippuu suureksi osaksi tiedonhaun ja sisällön navigoinnin hakutoiminnoista.</span><span class="sxs-lookup"><span data-stu-id="91a04-114">Search relevance and performance are key factors in the omnichannel experience, because product discovery relies primarily on search functionality for information retrieval and content navigation.</span></span> <span data-ttu-id="91a04-115">Tehokas selaus- ja hakukokemus auttaa muunnon lisäämisessä.</span><span class="sxs-lookup"><span data-stu-id="91a04-115">An effective and efficient browse and search experience helps increase conversion.</span></span>

<span data-ttu-id="91a04-116">Seuraavassa kuvassa on esimerkki tyypillisestä selaus- ja hakutoiminnosta.</span><span class="sxs-lookup"><span data-stu-id="91a04-116">The following illustration shows an example of typical browse and search functionality.</span></span>

![Aloitussivun haku](./media/SearchLanding.png)

## <a name="faceted-navigation-and-choice-summary"></a><span data-ttu-id="91a04-118">Kohdistetun siirtymisen ja valinnan yhteenveto</span><span class="sxs-lookup"><span data-stu-id="91a04-118">Faceted navigation and choice summary</span></span> 

<span data-ttu-id="91a04-119">Kohdistettu siirtyminen auttaa asiakkaita selaamaan sisältöä helpommin, koska he voivat suodattaa termeihin linkitettyjä tarkenteita termijoukossa.</span><span class="sxs-lookup"><span data-stu-id="91a04-119">Faceted navigation helps customers more easily browse for content by letting them filter on refiners that are linked to terms in a term set.</span></span> <span data-ttu-id="91a04-120">Kun asiakas on valinnut ja ottanut tarkenteet käyttöön, näkyviin tulee valintojen yhteenveto.</span><span class="sxs-lookup"><span data-stu-id="91a04-120">After a customer has selected and applied refiners, a summary of the choices is shown.</span></span> 

<span data-ttu-id="91a04-121">Kohdistetun siirtymisen avulla voi määrittää erilaisia tarkenteita eri termijoukon termeille ilman, että niille on luotava erillisiä sivuja.</span><span class="sxs-lookup"><span data-stu-id="91a04-121">By using faceted navigation, you can configure different refiners for different terms in a term set, without having to create additional pages.</span></span> 

<span data-ttu-id="91a04-122">Seuraavassa kuvassa on esimerkki kohdistetun siirtymisen käytöstä haussa.</span><span class="sxs-lookup"><span data-stu-id="91a04-122">The following illustration shows an example where faceted navigation is used in a search.</span></span>

![Valinnan yhteenveto](./media/ChoiceSummary.png)

## <a name="immersive-autosuggest"></a><span data-ttu-id="91a04-124">Mukaansatempaava automaattinen ehdotustoiminto</span><span class="sxs-lookup"><span data-stu-id="91a04-124">Immersive autosuggest</span></span>

<span data-ttu-id="91a04-125">Nykyinen automaattisen ehdotuksen toiminto näyttää avainsanat, jotka käynnistävät vastaavan avainsanan haun.</span><span class="sxs-lookup"><span data-stu-id="91a04-125">Current autosuggest functionality just shows keywords that trigger a search for the matching keyword.</span></span> <span data-ttu-id="91a04-126">Dynamics 365 Commercen uusien parannusten avulla asiakkaat voivat usein löytää linkkejä tuotteisiin ennen kuin he ovat kirjoittaneet hakusanoja.</span><span class="sxs-lookup"><span data-stu-id="91a04-126">Because of new enhancements in Dynamics 365 Commerce, customers can often discover links to products before they have finished typing.</span></span>

<span data-ttu-id="91a04-127">Dynamics 365 Commerce tukee myös eri luokkiin kuuluvien avainsanavastaavuuksien toimintoja.</span><span class="sxs-lookup"><span data-stu-id="91a04-127">Dynamics 365 Commerce also supports functionality for keyword matches in various categories.</span></span> <span data-ttu-id="91a04-128">Tämän toiminnon avulla asiakkaan näkevät vastaavien avainsanojen määrän eri luokissa. He voivat myös käynnistää avainsanahaun muissa luokissa.</span><span class="sxs-lookup"><span data-stu-id="91a04-128">This functionality lets customers see the number of matching keywords across categories and trigger a search for a keyword in other categories.</span></span>

<span data-ttu-id="91a04-129">Seuraavassa kuvassa näkyy esimerkki, jossa käytetään mukaansatempaavaa automaattista ehdotustoimintoa.</span><span class="sxs-lookup"><span data-stu-id="91a04-129">The following illustration shows an example where immersive autosuggest is being used.</span></span>

![Mukaansatempaava automaattinen ehdotustoiminto](./media/ImmersiveAutoSuggestUX.png)

## <a name="sort"></a><span data-ttu-id="91a04-131">Lajittele</span><span class="sxs-lookup"><span data-stu-id="91a04-131">Sort</span></span>

<span data-ttu-id="91a04-132">Dynamics 365 Commercen parannellun lajittelun avulla asiakkaat voivat lajitella, hakea ja selata hakutuloksia ja tarkentaa niitä erilaisten ehtojen, kuten hinnan, tuotenimen ja tuotenumeron avulla.</span><span class="sxs-lookup"><span data-stu-id="91a04-132">Enhanced sorting in Dynamics 365 Commerce lets customers sort, search, and browse search results, and refine them by criteria such as price, product name, and product number.</span></span> <span data-ttu-id="91a04-133">Asiakkaat voivat myös lajitella tulokset sen mukaan, onko tuote uusi, kuuluuko se myydyimpien joukkoon vai onko se lisätty äskettäin.</span><span class="sxs-lookup"><span data-stu-id="91a04-133">Customers can also sort results based on whether a product is new, top-selling, or recently added.</span></span>

>[!NOTE]
><span data-ttu-id="91a04-134">Nämä pilvipohjaiset hakutoiminnot ovat saatavilla versiosta 10.0.8 alkaen.</span><span class="sxs-lookup"><span data-stu-id="91a04-134">These cloud-powered search capabilities are available starting in version 10.0.8.</span></span> <span data-ttu-id="91a04-135">Varmista, että valikossa **Kaupan parametrit > Määrityksen parametrit** on merkintä ProductSearch.UseAzureSearch set to 'true'.</span><span class="sxs-lookup"><span data-stu-id="91a04-135">Ensure that under **Commerce Parameters > Configuration Parameters** there is an entry for "ProductSearch.UseAzureSearch set to 'true'".</span></span> 
<span data-ttu-id="91a04-136">![Määrityksen parametrit pilvipohjaiselle haulle](./media/CloudPoweredSearchConfigurationParameters.png)</span><span class="sxs-lookup"><span data-stu-id="91a04-136">![Configuration parameters for cloud-powered search](./media/CloudPoweredSearchConfigurationParameters.png)</span></span>

## <a name="additional-resources"></a><span data-ttu-id="91a04-137">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="91a04-137">Additional resources</span></span>

[<span data-ttu-id="91a04-138">Luokan oletussaapumissivun ja oletushakutulossivun yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="91a04-138">Default category landing page and search results page overview</span></span>](category-search-page-overview.md)

[<span data-ttu-id="91a04-139">SEO-metatietojen hallinta</span><span class="sxs-lookup"><span data-stu-id="91a04-139">Manage SEO metadata</span></span>](manage-seo-metadata.md)
