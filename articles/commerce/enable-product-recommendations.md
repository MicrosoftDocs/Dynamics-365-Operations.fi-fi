---
title: Ota tuotesuositukset käyttöön
description: Tässä ohjeaiheessa kerrotaa, miten tekoälyn koneoppimiseen perustuvia tuotesuosituksia voidaan tehdä Microsoft Dynamics 365 Commerce -asiakkaiden käyttöä varten.
author: bebeale
manager: AnnBe
ms.date: 08/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: b201e5481cfaf5bb6cd64a89cdb6b5a91f31447f
ms.sourcegitcommit: d3b970c3b93d8be12886b1c5a6bf91f0b33726dd
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/19/2020
ms.locfileid: "3700839"
---
# <a name="enable-product-recommendations"></a><span data-ttu-id="4198f-103">Ota tuotesuositukset käyttöön</span><span class="sxs-lookup"><span data-stu-id="4198f-103">Enable product recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="4198f-104">Tässä ohjeaiheessa kerrotaa, miten tekoälyn koneoppimiseen perustuvia tuotesuosituksia voidaan tehdä Microsoft Dynamics 365 Commerce -asiakkaiden käyttöä varten.</span><span class="sxs-lookup"><span data-stu-id="4198f-104">This topic explains how to make product recommendations that are based on artificial intelligence-machine learning (AI-ML) available for Microsoft Dynamics 365 Commerce customers.</span></span> <span data-ttu-id="4198f-105">Lisätietoja tuotesuositusten luetteloista on kohdassa [Tuotesuositusten yleiskatsaus](product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="4198f-105">For more information about product recommendation lists, see [Product recommendations overview](product-recommendations.md).</span></span>

## <a name="recommendations-pre-check"></a><span data-ttu-id="4198f-106">Suositusten esitarkistus</span><span class="sxs-lookup"><span data-stu-id="4198f-106">Recommendations pre-check</span></span>

<span data-ttu-id="4198f-107">Ota huomioon ennen käyttöönottoa, että tuotesuosituksia tuetaan vain Commerce-asiakkaille, jotka ovat siirtäneet tallennustilansa Azure Data Lake Storagea käyttäen.</span><span class="sxs-lookup"><span data-stu-id="4198f-107">Before enabling, note that product recommendations are only supported for Commerce customers who have migrated their storage to using Azure Data Lake Storage.</span></span> 

<span data-ttu-id="4198f-108">Seuraavat kokoonpanot on otettava käyttöön taustajärjestelmässä ennen suositusten käyttöönottoa:</span><span class="sxs-lookup"><span data-stu-id="4198f-108">The following configurations must be enabled in the back office before enabling recommendations:</span></span>

1. <span data-ttu-id="4198f-109">Varmista, että Azure Data Lake Storage on ostettu ja todennettu onnistuneesti ympäristössä.</span><span class="sxs-lookup"><span data-stu-id="4198f-109">Ensure that Azure Data Lake Storage has been purchased and successfully verified in the environment.</span></span> <span data-ttu-id="4198f-110">Katso lisätietoja kohdasta [Varmista, että Azure Data Lake Storage on ostettu ja todennettu onnistuneesti ympäristössä](enable-ADLS-environment.md).</span><span class="sxs-lookup"><span data-stu-id="4198f-110">For more information, see [Ensure that Azure Data Lake Storage has been purchased and successfully verified in the environment](enable-ADLS-environment.md).</span></span>
2. <span data-ttu-id="4198f-111">Varmista, että yksikkösäilön päivitys on automatisoitu.</span><span class="sxs-lookup"><span data-stu-id="4198f-111">Ensure that the entity store refresh has been automated.</span></span> <span data-ttu-id="4198f-112">Lisätietoja on kohdassa [Varmista, että yksikkösäilön päivitys on automatisoitu](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md).</span><span class="sxs-lookup"><span data-stu-id="4198f-112">For more information, see [Ensure that the Entity store refresh has been automated](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md).</span></span>
3. <span data-ttu-id="4198f-113">Vahvista, että Azure AD -käyttäjätietojen määritys sisältää suositusten merkinnän.</span><span class="sxs-lookup"><span data-stu-id="4198f-113">Confirm that Azure AD Identity configuration contains an entry for Recommendations.</span></span> <span data-ttu-id="4198f-114">Lisätietoja tästä toiminnosta alla.</span><span class="sxs-lookup"><span data-stu-id="4198f-114">More information on how to do this action is below.</span></span>

<span data-ttu-id="4198f-115">Varmista myös, että RetailSale-mittarit on otettu käyttöön.</span><span class="sxs-lookup"><span data-stu-id="4198f-115">Additionally, ensure that RetailSale measurements have been enabled.</span></span> <span data-ttu-id="4198f-116">Lisätietoja tästä määritysprosessista on kohdassa [Mittayksiköiden käsitteleminen](https://docs.microsoft.com/dynamics365/ai/customer-insights/pm-measures).</span><span class="sxs-lookup"><span data-stu-id="4198f-116">To learn more about this set up process, see [Work with measures](https://docs.microsoft.com/dynamics365/ai/customer-insights/pm-measures).</span></span>

## <a name="azure-ad-identity-configuration"></a><span data-ttu-id="4198f-117">Azure AD -tunnisteen konfiguraatio</span><span class="sxs-lookup"><span data-stu-id="4198f-117">Azure AD Identity configuration</span></span>

<span data-ttu-id="4198f-118">Tämä vaihe on pakollinen kaikille asiakkaille, jotka käyttävät infrastruktuuria palvelun (IaaS) määrityksenä.</span><span class="sxs-lookup"><span data-stu-id="4198f-118">This step is required for all customers running an infra-structure as a service (IaaS) configuration.</span></span> <span data-ttu-id="4198f-119">Jos asiakas käyttää Service fabric (SF) -palvelua, tämän vaiheen tulisi olla automaattinen ja suosittelemme, että asetus määritetään odotetulla tavalla.</span><span class="sxs-lookup"><span data-stu-id="4198f-119">For customers running on service fabric (SF), this step should be automatic and we recommend verifying the setting is configured as expected.</span></span>

### <a name="setup"></a><span data-ttu-id="4198f-120">Määritys</span><span class="sxs-lookup"><span data-stu-id="4198f-120">Setup</span></span>

1. <span data-ttu-id="4198f-121">Etsi taustaohjelmistosta **Azure Active Directory -sovellukset** -sivu.</span><span class="sxs-lookup"><span data-stu-id="4198f-121">From the back office, search for the **Azure Active Directory applications** page.</span></span>
2. <span data-ttu-id="4198f-122">Tarkista, onko "RecommendationSystemApplication-1"-merkintää olemassa.</span><span class="sxs-lookup"><span data-stu-id="4198f-122">Verify if an entry exists for "RecommendationSystemApplication-1".</span></span>

<span data-ttu-id="4198f-123">Jos tapahtumaa ei ole olemassa, lisää uusi tietue, jossa on seuraavat tiedot:</span><span class="sxs-lookup"><span data-stu-id="4198f-123">If the entry does not exist, add a new entry with the following information:</span></span>

- <span data-ttu-id="4198f-124">**Asiakastunnus** - d37b07e8-dd1c-4514-835d-8b918e6f9727</span><span class="sxs-lookup"><span data-stu-id="4198f-124">**Client Id** - d37b07e8-dd1c-4514-835d-8b918e6f9727</span></span>
- <span data-ttu-id="4198f-125">**Nimi** - RecommendationSystemApplication-1</span><span class="sxs-lookup"><span data-stu-id="4198f-125">**Name** - RecommendationSystemApplication-1</span></span>
- <span data-ttu-id="4198f-126">**Käyttäjätunnus** - RetailServiceAccount</span><span class="sxs-lookup"><span data-stu-id="4198f-126">**User Id** - RetailServiceAccount</span></span>

<span data-ttu-id="4198f-127">Tallenna ja sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="4198f-127">Save and close the page.</span></span> 

## <a name="turn-on-recommendations"></a><span data-ttu-id="4198f-128">Suositusten ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="4198f-128">Turn on recommendations</span></span>

<span data-ttu-id="4198f-129">Voit ottaa tuotesuositukset käyttöön noudattamalla seuraavia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="4198f-129">To turn on product recommendations, follow these steps.</span></span>

1. <span data-ttu-id="4198f-130">Hae **Ominaisuuksien hallinta** Commercen pääkonttoriversiossa.</span><span class="sxs-lookup"><span data-stu-id="4198f-130">In Commerce headquarters, search for **Feature Management**.</span></span>
1. <span data-ttu-id="4198f-131">Avaa käytettävissä olevien ominaisuuksien luettelo valitsemalla **Kaikki**.</span><span class="sxs-lookup"><span data-stu-id="4198f-131">Select **All** to see a list of available features.</span></span> 
1. <span data-ttu-id="4198f-132">Kirjoita hakuruutuun **Suositukset**.</span><span class="sxs-lookup"><span data-stu-id="4198f-132">In the search box, enter **Recommendations**.</span></span>
1. <span data-ttu-id="4198f-133">Valitse **Tuotesuositukset** -ominaisuus.</span><span class="sxs-lookup"><span data-stu-id="4198f-133">Select the **Product recommendations** feature.</span></span>
1. <span data-ttu-id="4198f-134">Valitse **Tuotesuositukset** -ominaisuusruudussa **Ota käyttöön nyt**.</span><span class="sxs-lookup"><span data-stu-id="4198f-134">In the **Product recommendations** properties pane, select **Enable now**.</span></span>

![Suositusten ottaminen käyttöön](./media/FeatureManagement_Recommendations.PNG)

> [!NOTE]
> <span data-ttu-id="4198f-136">Tämä menettely käynnistää tuotesuositusluetteloiden luontiprosessin.</span><span class="sxs-lookup"><span data-stu-id="4198f-136">This procedure starts the process of generating product recommendation lists.</span></span> <span data-ttu-id="4198f-137">Luetteloiden luominen, niiden saaminen käyttöön ja näkyminen myyntipisteessä tai Dynamics 365 Commerce -sovelluksessa voi kestää useita tunteja.</span><span class="sxs-lookup"><span data-stu-id="4198f-137">It may take several hours before the lists are available and can be viewed at the point of sale (POS) or in Dynamics 365 Commerce.</span></span>

## <a name="configure-recommendation-list-parameters"></a><span data-ttu-id="4198f-138">Suositusluettelon parametrien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="4198f-138">Configure recommendation list parameters</span></span>

<span data-ttu-id="4198f-139">Oletusarvoisesti tekoälyyn perustuva tuotesuositusluettelo sisältää ehdotetut arvot.</span><span class="sxs-lookup"><span data-stu-id="4198f-139">By default, the AI-ML-based product recommendation list provides suggested values.</span></span> <span data-ttu-id="4198f-140">Voit muuttaa ehdotettuja oletusarvoja haluamallasi tavalla.</span><span class="sxs-lookup"><span data-stu-id="4198f-140">You can change the default suggested values to suit the flow of your business.</span></span> <span data-ttu-id="4198f-141">Lisätietoja oletusparametrien muuttamisesta on kohdassa [Tekoälyn koneoppimiseen perustuvan tuotesuositusluettelon hallinta](modify-product-recommendation-results.md).</span><span class="sxs-lookup"><span data-stu-id="4198f-141">To learn more about how to change the default parameters, go to [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>

## <a name="show-recommendations-on-pos-devices"></a><span data-ttu-id="4198f-142">Suositusten näyttäminen myyntipistelaitteissa</span><span class="sxs-lookup"><span data-stu-id="4198f-142">Show recommendations on POS devices</span></span>

<span data-ttu-id="4198f-143">Kun suositukset on otettu käyttöön Commercen taustatoiminnossa, suosituspaneeli on lisättävä ohjausobjektin myyntipistenäyttöön asettelutyökalun avulla.</span><span class="sxs-lookup"><span data-stu-id="4198f-143">After enabling recommendations in Commerce back office, the recommendations panel must be added to the control POS screen using the layout tool.</span></span> <span data-ttu-id="4198f-144">Lisä tietoja tästä prosessista on kohdassa [Suositusten ohjausobjektin lisääminen myyntipisteen laitteen tapahtumaruudulle](add-recommendations-control-pos-screen.md).</span><span class="sxs-lookup"><span data-stu-id="4198f-144">To learn about this process, see [Add a recommendations control to the transaction screen on POS devices](add-recommendations-control-pos-screen.md).</span></span> 

## <a name="enable-personalized-recommendations"></a><span data-ttu-id="4198f-145">Kohdennettujen suositusten ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="4198f-145">Enable personalized recommendations</span></span>

<span data-ttu-id="4198f-146">Dynamics 365 Commerce -ohjelmassa jälleenmyyjät voivat tehdä mukautettuja tuotesuosituksia (eli personointeja).</span><span class="sxs-lookup"><span data-stu-id="4198f-146">In Dynamics 365 Commerce, retailers can make personalized product recommendations (also known as personalization) available.</span></span> <span data-ttu-id="4198f-147">Näin henkilökohtaiset suositukset voidaan sisällyttää asiakaskokemukseen verkossa ja myyntipisteessä.</span><span class="sxs-lookup"><span data-stu-id="4198f-147">In this way, personalized recommendations can be incorporated into the online customer experience and at the point of sale.</span></span> <span data-ttu-id="4198f-148">Kun mukautustoiminto on käytössä, järjestelmä voi liittää käyttäjän osto- ja tuotetiedot ja luoda yksilöllisiä tuotesuosituksia.</span><span class="sxs-lookup"><span data-stu-id="4198f-148">When the personalization functionality is turned on, the system can associate a user's purchase and product information to generate individualized product recommendations.</span></span>

<span data-ttu-id="4198f-149">Lisätietoja mukautetuista suosituksista on kohdassa [Mukautettujen suositusten ottaminen käyttöön](personalized-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="4198f-149">To learn more about personalized recommendations, see [Enable personalized recommendations](personalized-recommendations.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4198f-150">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="4198f-150">Additional resources</span></span>

[<span data-ttu-id="4198f-151">Tuotesuositusten yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="4198f-151">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="4198f-152">Azure Data Lake Storagen käyttöönotto Dynamics 365 Commerce -ympäristössä</span><span class="sxs-lookup"><span data-stu-id="4198f-152">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="4198f-153">Kohdennettujen suositusten ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="4198f-153">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="4198f-154">"Osta samankaltaisia tyylejä" -suositusten käyttöönotto</span><span class="sxs-lookup"><span data-stu-id="4198f-154">Enable "shop similar looks" recommendations</span></span>](shop-similar-looks.md)

[<span data-ttu-id="4198f-155">Kohdennetuista tuotesuosituksista kieltäytyminen</span><span class="sxs-lookup"><span data-stu-id="4198f-155">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="4198f-156">Tuotesuositusten lisääminen myyntipisteessä</span><span class="sxs-lookup"><span data-stu-id="4198f-156">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="4198f-157">Suositusten lisääminen tapahtumanäyttöön</span><span class="sxs-lookup"><span data-stu-id="4198f-157">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="4198f-158">AI-ML-suositusten tulosten muokkaaminen</span><span class="sxs-lookup"><span data-stu-id="4198f-158">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="4198f-159">Kuratoitujen suositusten manuaalinen luominen</span><span class="sxs-lookup"><span data-stu-id="4198f-159">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="4198f-160">Suositusten luominen esittelytietojen avulla</span><span class="sxs-lookup"><span data-stu-id="4198f-160">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="4198f-161">Tuotesuositukset – usein kysytyt kysymykset</span><span class="sxs-lookup"><span data-stu-id="4198f-161">Product recommendations FAQ</span></span>](faq-recommendations.md)

