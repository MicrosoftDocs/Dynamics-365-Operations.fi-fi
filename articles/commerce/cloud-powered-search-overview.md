---
title: Pilvipohjaisen haun yleiskatsaus
description: Tässä ohjeaiheessa on yleiskatsaus pilvipohjaisesta hausta Microsoft Dynamics 365 Commerce -sovelluksessa.
author: ashishmsft
ms.date: 06/29/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: b5182df9d45a3b5d2572a5b6b391c924ef23bf9a
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5800418"
---
# <a name="cloud-powered-search-overview"></a><span data-ttu-id="609f0-103">Pilvipohjaisen haun yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="609f0-103">Cloud-powered search overview</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="609f0-104">Tässä ohjeaiheessa on yleiskatsaus pilvipohjaisesta hausta Microsoft Dynamics 365 Commerce -sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="609f0-104">This topic gives an overview of cloud-powered search in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="609f0-105">Tuotteiden löydettävyyden avulla varmistetaan, että asiakkaat löytävät tuotteita nopeasti ja helposti selaamalla luokkia sekä tekemällä hakuja ja suodattamalla luokkia.</span><span class="sxs-lookup"><span data-stu-id="609f0-105">Product discoverability helps guarantee that customers can quickly and easily find products by browsing categories, searching, and filtering.</span></span> <span data-ttu-id="609f0-106">Vähittäiskauppiaat pitävät tuotteen etsintätyökalua ensisijaisena työkaluna asiakkaan vuorovaikutuksessa kaikkien kanavien kautta.</span><span class="sxs-lookup"><span data-stu-id="609f0-106">Retailers consider product discovery a primary tool for customer interaction across all channels.</span></span>

<span data-ttu-id="609f0-107">Asiakkaat ovat tottuneet lähes välittömiin vastausaikoihin verkon hakukoneissa, kehittyneissä sähköisen kaupankäynnin sivustoissa, yhteisöpalvelusovelluksissa, automaattisissa ehdotuksissa hakuehdotusten syöttämisen yhteydessä, kohdistetussa siirtymisessä ja korostuksissa.</span><span class="sxs-lookup"><span data-stu-id="609f0-107">Customers are accustomed to the nearly instantaneous response times of web search engines, sophisticated e-Commerce websites, social apps, automatic suggestions that appear as they type search terms, faceted navigation, and highlighting.</span></span> <span data-ttu-id="609f0-108">Jos asiakkaat eivät löydä hakemaansa tuotetta riittävän nopeasti yhdestä sähköisen kaupankäynnin myymälästä, he siirtyvät nopeasti toiseen sähköisen kaupankäynnin myymälään.</span><span class="sxs-lookup"><span data-stu-id="609f0-108">If customers can't find the product that they are looking for quickly enough in one e-Commerce store, they won't hesitate to go to a different e-Commerce store.</span></span>

<span data-ttu-id="609f0-109">Pilvipohjaisen tuotteen etsintätoiminto Dynamics 365 Commerce -sovelluksessa auttaa jälleenmyyjiä lisäämään asiakkaiden pysymistä ja eri kanavien muuntomääriä sekä sähköisen kaupankäynnin kanavissa että myyntipistekanavissa.</span><span class="sxs-lookup"><span data-stu-id="609f0-109">The cloud-powered product discoverability in Dynamics 365 Commerce helps retailers continue to increase consumer retention and conversion rates across all channels, both e-Commerce channels and point of sale (POS) channels.</span></span>

<span data-ttu-id="609f0-110">Dynamics 365 Commercen hakukokemus on parantanut ominaisuuksia, joiden avulla jälleenmyyjät saavuttavat aiempaa paremman tuotteiden löydettävyyden.</span><span class="sxs-lookup"><span data-stu-id="609f0-110">The Dynamics 365 Commerce search experience has improved capabilities to help retailers achieve better product discoverability.</span></span> <span data-ttu-id="609f0-111">Samalla nämä ominaisuudet tarjoavat skaalautuvuutta ja suorituskykyä, jota sähköisen kaupankäynnin liikenne vaatii.</span><span class="sxs-lookup"><span data-stu-id="609f0-111">At the same time, these capabilities deliver the scalability and performance that are required for e-Commerce traffic.</span></span>

## <a name="browse-and-search"></a><span data-ttu-id="609f0-112">Selaaminen ja hakeminen</span><span class="sxs-lookup"><span data-stu-id="609f0-112">Browse and search</span></span>

<span data-ttu-id="609f0-113">Hakurelevanssi ja suorituskyky ovat tärkeitä tekijöitä monikanavakokemuksessa, koska tuotteen löydettävyys riippuu suureksi osaksi tiedonhaun ja sisällön navigoinnin hakutoiminnoista.</span><span class="sxs-lookup"><span data-stu-id="609f0-113">Search relevance and performance are key factors in the omnichannel experience, because product discovery relies primarily on search functionality for information retrieval and content navigation.</span></span> <span data-ttu-id="609f0-114">Tehokas selaus- ja hakukokemus auttaa muunnon lisäämisessä.</span><span class="sxs-lookup"><span data-stu-id="609f0-114">An effective and efficient browse and search experience helps increase conversion.</span></span>

<span data-ttu-id="609f0-115">Seuraavassa kuvassa on esimerkki tyypillisestä selaus- ja hakutoiminnosta.</span><span class="sxs-lookup"><span data-stu-id="609f0-115">The following illustration shows an example of typical browse and search functionality.</span></span>

![Aloitussivun haku](./media/SearchLanding.png)

## <a name="faceted-navigation-and-choice-summary"></a><span data-ttu-id="609f0-117">Kohdistetun siirtymisen ja valinnan yhteenveto</span><span class="sxs-lookup"><span data-stu-id="609f0-117">Faceted navigation and choice summary</span></span> 

<span data-ttu-id="609f0-118">Kohdistettu siirtyminen auttaa asiakkaita selaamaan sisältöä helpommin, koska he voivat suodattaa termeihin linkitettyjä tarkenteita termijoukossa.</span><span class="sxs-lookup"><span data-stu-id="609f0-118">Faceted navigation helps customers more easily browse for content by letting them filter on refiners that are linked to terms in a term set.</span></span> <span data-ttu-id="609f0-119">Kun asiakas on valinnut ja ottanut tarkenteet käyttöön, näkyviin tulee valintojen yhteenveto.</span><span class="sxs-lookup"><span data-stu-id="609f0-119">After a customer has selected and applied refiners, a summary of the choices is shown.</span></span> 

<span data-ttu-id="609f0-120">Kohdistetun siirtymisen avulla voi määrittää erilaisia tarkenteita eri termijoukon termeille ilman, että niille on luotava erillisiä sivuja.</span><span class="sxs-lookup"><span data-stu-id="609f0-120">By using faceted navigation, you can configure different refiners for different terms in a term set, without having to create additional pages.</span></span> 

<span data-ttu-id="609f0-121">Seuraavassa kuvassa on esimerkki kohdistetun siirtymisen käytöstä haussa.</span><span class="sxs-lookup"><span data-stu-id="609f0-121">The following illustration shows an example where faceted navigation is used in a search.</span></span>

![Valinnan yhteenveto](./media/ChoiceSummary.png)

## <a name="immersive-autosuggest"></a><span data-ttu-id="609f0-123">Mukaansatempaava automaattinen ehdotustoiminto</span><span class="sxs-lookup"><span data-stu-id="609f0-123">Immersive autosuggest</span></span>

<span data-ttu-id="609f0-124">Nykyinen automaattisen ehdotuksen toiminto näyttää avainsanat, jotka käynnistävät vastaavan avainsanan haun.</span><span class="sxs-lookup"><span data-stu-id="609f0-124">Current autosuggest functionality just shows keywords that trigger a search for the matching keyword.</span></span> <span data-ttu-id="609f0-125">Dynamics 365 Commercen uusien parannusten avulla asiakkaat voivat usein löytää linkkejä tuotteisiin ennen kuin he ovat kirjoittaneet hakusanoja.</span><span class="sxs-lookup"><span data-stu-id="609f0-125">Because of new enhancements in Dynamics 365 Commerce, customers can often discover links to products before they have finished typing.</span></span>

<span data-ttu-id="609f0-126">Dynamics 365 Commerce tukee myös eri luokkiin kuuluvien avainsanavastaavuuksien toimintoja.</span><span class="sxs-lookup"><span data-stu-id="609f0-126">Dynamics 365 Commerce also supports functionality for keyword matches in various categories.</span></span> <span data-ttu-id="609f0-127">Tämän toiminnon avulla asiakkaan näkevät vastaavien avainsanojen määrän eri luokissa. He voivat myös käynnistää avainsanahaun muissa luokissa.</span><span class="sxs-lookup"><span data-stu-id="609f0-127">This functionality lets customers see the number of matching keywords across categories and trigger a search for a keyword in other categories.</span></span>

<span data-ttu-id="609f0-128">Seuraavassa kuvassa näkyy esimerkki, jossa käytetään mukaansatempaavaa automaattista ehdotustoimintoa.</span><span class="sxs-lookup"><span data-stu-id="609f0-128">The following illustration shows an example where immersive autosuggest is being used.</span></span>

![Mukaansatempaava automaattinen ehdotustoiminto](./media/ImmersiveAutoSuggestUX.png)

## <a name="sort"></a><span data-ttu-id="609f0-130">Lajittele</span><span class="sxs-lookup"><span data-stu-id="609f0-130">Sort</span></span>

<span data-ttu-id="609f0-131">Dynamics 365 Commercen parannellun lajittelun avulla asiakkaat voivat lajitella, hakea ja selata hakutuloksia ja tarkentaa niitä erilaisten ehtojen, kuten hinnan, tuotenimen ja tuotenumeron avulla.</span><span class="sxs-lookup"><span data-stu-id="609f0-131">Enhanced sorting in Dynamics 365 Commerce lets customers sort, search, and browse search results, and refine them by criteria such as price, product name, and product number.</span></span> <span data-ttu-id="609f0-132">Asiakkaat voivat myös lajitella tulokset sen mukaan, onko tuote uusi, kuuluuko se myydyimpien joukkoon vai onko se lisätty äskettäin.</span><span class="sxs-lookup"><span data-stu-id="609f0-132">Customers can also sort results based on whether a product is new, top-selling, or recently added.</span></span>

>[!NOTE]
><span data-ttu-id="609f0-133">Nämä pilvipohjaiset hakutoiminnot ovat saatavilla versiosta 10.0.8 alkaen.</span><span class="sxs-lookup"><span data-stu-id="609f0-133">These cloud-powered search capabilities are available starting in version 10.0.8.</span></span> <span data-ttu-id="609f0-134">Varmista, että valikossa **Kaupan parametrit > Määrityksen parametrit** on merkintä ProductSearch.UseAzureSearch set to 'true'.</span><span class="sxs-lookup"><span data-stu-id="609f0-134">Ensure that under **Commerce Parameters > Configuration Parameters** there is an entry for "ProductSearch.UseAzureSearch set to 'true'".</span></span> 
<span data-ttu-id="609f0-135">![Määrityksen parametrit pilvipohjaiselle haulle](./media/CloudPoweredSearchConfigurationParameters.png)</span><span class="sxs-lookup"><span data-stu-id="609f0-135">![Configuration parameters for cloud-powered search](./media/CloudPoweredSearchConfigurationParameters.png)</span></span>

## <a name="additional-resources"></a><span data-ttu-id="609f0-136">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="609f0-136">Additional resources</span></span>

[<span data-ttu-id="609f0-137">Luokan oletussaapumissivun ja oletushakutulossivun yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="609f0-137">Default category landing page and search results page overview</span></span>](category-search-page-overview.md)

[<span data-ttu-id="609f0-138">SEO-metatietojen hallinta</span><span class="sxs-lookup"><span data-stu-id="609f0-138">Manage SEO metadata</span></span>](manage-seo-metadata.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
