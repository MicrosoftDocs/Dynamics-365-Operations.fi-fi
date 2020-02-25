---
title: Poista kohdennetut suositukset
description: Tässä ohjeaiheessa kerrotaan, miten voit antaa asiakkaiden kieltäytyä vastaanottamasta mukautettuja Microsoft Dynamics 365 Commerce -suosituksia.
author: bebeale
manager: AnnBe
ms.date: 01/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 8e7b800218f68167901d86d61ae483680a04cfab
ms.sourcegitcommit: b5ecde955a69f577de46e7db10e89caaedeb2b49
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/04/2020
ms.locfileid: "3025243"
---
# <a name="opt-out-of-personalized-recommendations"></a><span data-ttu-id="6798b-103">Poista kohdennetut suositukset</span><span class="sxs-lookup"><span data-stu-id="6798b-103">Opt out of personalized recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="6798b-104">Tässä ohjeaiheessa kerrotaan, miten voit antaa asiakkaiden kieltäytyä vastaanottamasta mukautettuja Microsoft Dynamics 365 Commerce -suosituksia.</span><span class="sxs-lookup"><span data-stu-id="6798b-104">This topic explains how you can let customers opt out of receiving personalized recommendations in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="6798b-105">Yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="6798b-105">Overview</span></span>

<span data-ttu-id="6798b-106">Tilin luonnin yhteydessä uudet asiakkaat määritetään automaattisesti vastaanottamaan mukautettuja suosituksia.</span><span class="sxs-lookup"><span data-stu-id="6798b-106">During account creation, new customers are automatically set up to receive personalized recommendations.</span></span> <span data-ttu-id="6798b-107">Dynamics 365 Commerce tarjoaa kuitenkin useita tapoja, joilla jälleenmyyjät voivat antaa käyttäjien kieltäytyä vastaanottamasta näitä suosituksia ja rajoittaa henkilökohtaisten tietojen käsittelyä.</span><span class="sxs-lookup"><span data-stu-id="6798b-107">However, Dynamics 365 Commerce provides various ways for retailers to let users opt out of receiving these recommendations and restrict the processing of their personal data.</span></span> <span data-ttu-id="6798b-108">Todennetut käyttäjät, jotka eivät halua saada mukautettuja suosituksia, eivät heti näe mukautettuja luetteloita.</span><span class="sxs-lookup"><span data-stu-id="6798b-108">Authenticated users who opt out of receiving personalized recommendations will immediately stop seeing personalized lists.</span></span> <span data-ttu-id="6798b-109">Lisäksi kaikki personointia varten kerätyt henkilökohtaiset tiedot poistetaan mukautetuista suositusmalleista.</span><span class="sxs-lookup"><span data-stu-id="6798b-109">Additionally, all personal data that is collected for personalization will be removed from personalized recommendations models.</span></span>

<span data-ttu-id="6798b-110">Lisätietoja mukautetuista tuotesuosituksista on kohdassa [Mukautettujen suositusten ottaminen käyttöön](personalized-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="6798b-110">For more information about personalized product recommendations, see [Enable personalized recommendations](personalized-recommendations.md).</span></span>

## <a name="ways-for-retailers-to-implement-an-opt-out-experience"></a><span data-ttu-id="6798b-111">Tapoja, joilla jälleenmyyjät voivat toteuttaa opt-out-kokemuksen</span><span class="sxs-lookup"><span data-stu-id="6798b-111">Ways for retailers to implement an opt-out experience</span></span>

<span data-ttu-id="6798b-112">Jälleenmyyjillä on kolme tapaa toteuttaa opt-out-kokemus.</span><span class="sxs-lookup"><span data-stu-id="6798b-112">Retailers have three ways to implement an opt-out experience.</span></span>

### <a name="opting-out-on-behalf-of-users"></a><span data-ttu-id="6798b-113">Käytöstä poistaminen käyttäjien puolesta</span><span class="sxs-lookup"><span data-stu-id="6798b-113">Opting out on behalf of users</span></span>

<span data-ttu-id="6798b-114">Commerce Back Office -tilien hallinnassa jälleenmyyjät voivat jättäytyä pois käyttäjien puolesta.</span><span class="sxs-lookup"><span data-stu-id="6798b-114">In Account management in Commerce back office, retailers can opt out on behalf of users.</span></span>

1. <span data-ttu-id="6798b-115">Hae Back Office -kotisivulta **kaikki asiakkaat**.</span><span class="sxs-lookup"><span data-stu-id="6798b-115">From the back-office home page, search for **all customers**.</span></span>
1. <span data-ttu-id="6798b-116">Hae ja valitse asiakas ja valitse sitten **Retail**-pikavälilehti.</span><span class="sxs-lookup"><span data-stu-id="6798b-116">Search for and select a customer, and then select the **Retail** FastTab.</span></span>

    ![Retail-pikavälilehti](./media/Disablepersonalizationpart1.png)

1. <span data-ttu-id="6798b-118">Valitse **Yksityisyys**-kohdassa **Poista mukautus käytöstä** -asetukseksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="6798b-118">Under **Privacy**, set the **Disable personalization** option to **Yes**.</span></span>

    ![Tietosuoja-asetukset](./media/Disablepersonalizationpart2.png)

1. <span data-ttu-id="6798b-120">Valitse **Tallenna** ja sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="6798b-120">Select **Save**, and close the page.</span></span>

### <a name="module-based-opt-out-experience"></a><span data-ttu-id="6798b-121">Moduulipohjainen opt-out-kokemus</span><span class="sxs-lookup"><span data-stu-id="6798b-121">Module-based opt-out experience</span></span>

<span data-ttu-id="6798b-122">Vähittäiskauppiaat voivat antaa todennettujen käyttäjien jättäytyä pois yksilöllisten suositusten mukaan itse.</span><span class="sxs-lookup"><span data-stu-id="6798b-122">Retailers can let authenticated users opt out of personalized recommendations by themselves.</span></span> <span data-ttu-id="6798b-123">Voit antaa tämän opt-out-käyttökokemuksen lisäämällä käyttäjän opt-out-moduulin asiakastilin profiilisivuille.</span><span class="sxs-lookup"><span data-stu-id="6798b-123">To provide this opt-out experience, add the user opt-out module to customer account profile pages.</span></span>

### <a name="custom-extensions"></a><span data-ttu-id="6798b-124">Mukautetut laajennukset</span><span class="sxs-lookup"><span data-stu-id="6798b-124">Custom extensions</span></span>

<span data-ttu-id="6798b-125">Jälleenmyyjät voivat luoda omia laajennuksia, joilla hallitaan käyttäjien käyttöoikeustietoja.</span><span class="sxs-lookup"><span data-stu-id="6798b-125">Retailers can create their own extensions to manage the opt-out experience for users.</span></span> <span data-ttu-id="6798b-126">Lisätietoja on kohdassa [Soita Retail-palvelimen ohjelmointirajapinnalle](e-commerce-extensibility/call-retail-server-apis.md) ja [Online-kanavan laajennettavuus](e-commerce-extensibility/overview.md).</span><span class="sxs-lookup"><span data-stu-id="6798b-126">For more information, see [Call Retail Server APIs](e-commerce-extensibility/call-retail-server-apis.md) and [Online channel extensibility](e-commerce-extensibility/overview.md).</span></span>

## <a name="obtain-a-digital-copy-of-personalized-recommendations-data-on-behalf-of-an-authenticated-user"></a><span data-ttu-id="6798b-127">Digitaalisen kopion hankkiminen yksilöllisten suositusten tiedoista todennetun käyttäjän puolesta</span><span class="sxs-lookup"><span data-stu-id="6798b-127">Obtain a digital copy of personalized recommendations data on behalf of an authenticated user</span></span>

<span data-ttu-id="6798b-128">Asiakkaat voivat halutessaan hankkia digitaalisen kopion henkilötiedoistaan ja nähdä myös viedyn näkymän niiden suositusten tuloksista.</span><span class="sxs-lookup"><span data-stu-id="6798b-128">Customers might want to obtain a digital copy of their personal data and also see an exported view of their recommendations results.</span></span> <span data-ttu-id="6798b-129">Jos asiakas pyytää näitä tietoja, vähittäismyyjän on luotava mukautettu laajennus, joka kutsuu Retail Server -sovellusohjelmointiliittymää (API), ja kyselyt, jotka koskevat **poimintoja sinulle** -luettelon kaikkia tuloksia asiakkaan asiakastunnuksen perusteella.</span><span class="sxs-lookup"><span data-stu-id="6798b-129">If a customer requests this information, the retailer must create a customized extension that calls the Retail Server application programming interface (API) and queries for the full results from the **Picks for you** list, based on the customer's customer ID.</span></span> <span data-ttu-id="6798b-130">Tämän jälkeen tulokset voidaan viedä CSV-muodossa ja jakaa asiakkaan kanssa.</span><span class="sxs-lookup"><span data-stu-id="6798b-130">The results can then be exported in comma-separated values (CSV) format and shared with the customer.</span></span>

<span data-ttu-id="6798b-131">Seuraavassa esimerkissä näkyy, miten jälleenmyyjä voi suorittaa tämän tehtävän.</span><span class="sxs-lookup"><span data-stu-id="6798b-131">The following example shows how a retailer can accomplish this task.</span></span>

1. <span data-ttu-id="6798b-132">Vähittäiskauppias luo mukautetun laajennuksen henkilökohtaisten suositusten tietojen vastaanottamista varten käyttäjän puolesta.</span><span class="sxs-lookup"><span data-stu-id="6798b-132">The retailer creates a custom extension to pull personal recommendations data on behalf of the user.</span></span> <span data-ttu-id="6798b-133">Lisätietoja moduulien luomisesta, aiemmin luotujen moduulien kloonaamiseksi, Retail Serverin API-liittymien käyttämisestä ja tietojen kutsumisesta on ohjeaiheessa [Online-kanavan laajennettavuus](e-commerce-extensibility/overview.md).</span><span class="sxs-lookup"><span data-stu-id="6798b-133">For information about how to create modules, clone existing modules, call Retail Server APIs, and call data actions, see [Online channel extensibility](e-commerce-extensibility/overview.md).</span></span>
2. <span data-ttu-id="6798b-134">Mukautettu laajennus soittaa **hanki-suositukset**-ydintietotoimenpiteeseen ja välittää tarvittavat tiedot luettelon vaatimusten mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="6798b-134">The custom extension makes a call to the **get-recommendations** core data action and passes the required information to it, based on the requirements of the list.</span></span> <span data-ttu-id="6798b-135">Kun kyseessä on **poiminnat sinulle** -luettelo, tunnisteen on läpäistävä oikea luettelonimi ja asiakastunnus tietotoiminnossa.</span><span class="sxs-lookup"><span data-stu-id="6798b-135">In the case of the **Picks for you** list, the extension must pass the correct list name and customer ID to the data action.</span></span>

    <span data-ttu-id="6798b-136">Yksi tapa luoda mukautettu tunniste on kloonata aiemmin luotu tuotekokoelmamoduuli, jota käytetään suositustulosten palauttamiseen.</span><span class="sxs-lookup"><span data-stu-id="6798b-136">One way to create the custom extension is to clone the existing product collection module that is used to return recommendations results.</span></span> <span data-ttu-id="6798b-137">Kloonaamalla tämän olemassa olevan moduulin jälleenmyyjä voi muokata olemassa olevaa koodia ja lisätä uuden painikkeen, joka vie suositustulokset CSV-tiedostoon.</span><span class="sxs-lookup"><span data-stu-id="6798b-137">By cloning this existing module, a retailer can modify the existing code and add a new button that exports the recommendations results to a CSV file.</span></span> <span data-ttu-id="6798b-138">Lisätietoja on kohdassa [Starttipakettimoduulin](e-commerce-extensibility/clone-starter-module.md) ja [tuotekokoelmamoduulien](product-collection-module-overview.md) kloonaaminen.</span><span class="sxs-lookup"><span data-stu-id="6798b-138">For more information, see [Clone a starter kit module](e-commerce-extensibility/clone-starter-module.md) and [Product collection modules](product-collection-module-overview.md).</span></span>

    <span data-ttu-id="6798b-139">Lisä tietoja Retail Serverin API-kirjaston täydestä näkymästä on kohdassa [Retail Server-asiakas- ja kuluttajasovellusliittymät](dev-itpro/retail-server-customer-consumer-api.md).</span><span class="sxs-lookup"><span data-stu-id="6798b-139">For a full view of the Retail Server API library, see [Retail Server Customer and Consumer APIs](dev-itpro/retail-server-customer-consumer-api.md).</span></span>

3. <span data-ttu-id="6798b-140">Kun mukautettu laajennus on tehty, jälleenmyyjä voi viedä CSV-tiedoston kaikista suositusten tuloksista todennetun käyttäjän yksilöllisen asiakastunnuksen perusteella.</span><span class="sxs-lookup"><span data-stu-id="6798b-140">After the custom extension is created, the retailer can export a CSV file of all recommendations results, based on the unique customer ID of the authenticated user.</span></span>
4. <span data-ttu-id="6798b-141">Jälleenmyyjä voi jakaa viedyn CSV-tiedoston, joka sisältää täyden mukautetun luettelon suositelluista tuotteista todennetun käyttäjän kanssa.</span><span class="sxs-lookup"><span data-stu-id="6798b-141">The retailer can share the exported CSV file that contains the full personalized list of recommended products with the authenticated user.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6798b-142">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="6798b-142">Additional resources</span></span>

[<span data-ttu-id="6798b-143">Tuotesuositusten yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="6798b-143">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="6798b-144">Ota tuotesuositukset käyttöön</span><span class="sxs-lookup"><span data-stu-id="6798b-144">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="6798b-145">Ota käyttöön kohdennetut tuotesuositukset</span><span class="sxs-lookup"><span data-stu-id="6798b-145">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="6798b-146">Tuotesuositusluetteloiden lisääminen sivuille</span><span class="sxs-lookup"><span data-stu-id="6798b-146">Add product recommendation lists to pages</span></span>](add-reco-list-to-page.md)

[<span data-ttu-id="6798b-147">Suositusten paneelin lisääminen myyntipistelaitteisiin</span><span class="sxs-lookup"><span data-stu-id="6798b-147">Add recommendations panel to POS devices</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="6798b-148">Tuotekokoelmamoduulin yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="6798b-148">Product collection module overview</span></span>](product-collection-module-overview.md)
