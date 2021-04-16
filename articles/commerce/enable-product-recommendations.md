---
title: Ota tuotesuositukset käyttöön
description: Tässä ohjeaiheessa kerrotaa, miten tekoälyn koneoppimiseen perustuvia tuotesuosituksia voidaan tehdä Microsoft Dynamics 365 Commerce -asiakkaiden käyttöä varten.
author: bebeale
ms.date: 08/18/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 59d6b298896c92cbc0f6bbae17096ee1f027b922
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799152"
---
# <a name="enable-product-recommendations"></a><span data-ttu-id="ac9da-103">Ota tuotesuositukset käyttöön</span><span class="sxs-lookup"><span data-stu-id="ac9da-103">Enable product recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="ac9da-104">Tässä ohjeaiheessa kerrotaa, miten tekoälyn koneoppimiseen perustuvia tuotesuosituksia voidaan tehdä Microsoft Dynamics 365 Commerce -asiakkaiden käyttöä varten.</span><span class="sxs-lookup"><span data-stu-id="ac9da-104">This topic explains how to make product recommendations that are based on artificial intelligence-machine learning (AI-ML) available for Microsoft Dynamics 365 Commerce customers.</span></span> <span data-ttu-id="ac9da-105">Lisätietoja tuotesuositusten luetteloista on kohdassa [Tuotesuositusten yleiskatsaus](product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="ac9da-105">For more information about product recommendation lists, see [Product recommendations overview](product-recommendations.md).</span></span>

## <a name="recommendations-pre-check"></a><span data-ttu-id="ac9da-106">Suositusten esitarkistus</span><span class="sxs-lookup"><span data-stu-id="ac9da-106">Recommendations pre-check</span></span>

<span data-ttu-id="ac9da-107">Ota huomioon ennen käyttöönottoa, että tuotesuosituksia tuetaan vain Commerce-asiakkaille, jotka ovat siirtäneet tallennustilansa Azure Data Lake Storagea käyttäen.</span><span class="sxs-lookup"><span data-stu-id="ac9da-107">Before enabling, note that product recommendations are only supported for Commerce customers who have migrated their storage to using Azure Data Lake Storage.</span></span> 

<span data-ttu-id="ac9da-108">Seuraavat kokoonpanot on otettava käyttöön taustajärjestelmässä ennen suositusten käyttöönottoa:</span><span class="sxs-lookup"><span data-stu-id="ac9da-108">The following configurations must be enabled in the back office before enabling recommendations:</span></span>

1. <span data-ttu-id="ac9da-109">Varmista, että Azure Data Lake Storage on ostettu ja todennettu onnistuneesti ympäristössä.</span><span class="sxs-lookup"><span data-stu-id="ac9da-109">Ensure that Azure Data Lake Storage has been purchased and successfully verified in the environment.</span></span> <span data-ttu-id="ac9da-110">Katso lisätietoja kohdasta [Varmista, että Azure Data Lake Storage on ostettu ja todennettu onnistuneesti ympäristössä](enable-ADLS-environment.md).</span><span class="sxs-lookup"><span data-stu-id="ac9da-110">For more information, see [Ensure that Azure Data Lake Storage has been purchased and successfully verified in the environment](enable-ADLS-environment.md).</span></span>
2. <span data-ttu-id="ac9da-111">Varmista, että yksikkösäilön päivitys on automatisoitu.</span><span class="sxs-lookup"><span data-stu-id="ac9da-111">Ensure that the entity store refresh has been automated.</span></span> <span data-ttu-id="ac9da-112">Lisätietoja on kohdassa [Varmista, että yksikkösäilön päivitys on automatisoitu](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md).</span><span class="sxs-lookup"><span data-stu-id="ac9da-112">For more information, see [Ensure that the Entity store refresh has been automated](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md).</span></span>
3. <span data-ttu-id="ac9da-113">Vahvista, että Azure AD -käyttäjätietojen määritys sisältää suositusten merkinnän.</span><span class="sxs-lookup"><span data-stu-id="ac9da-113">Confirm that Azure AD Identity configuration contains an entry for Recommendations.</span></span> <span data-ttu-id="ac9da-114">Lisätietoja tästä toiminnosta alla.</span><span class="sxs-lookup"><span data-stu-id="ac9da-114">More information on how to do this action is below.</span></span>

<span data-ttu-id="ac9da-115">Varmista myös, että RetailSale-mittarit on otettu käyttöön.</span><span class="sxs-lookup"><span data-stu-id="ac9da-115">Additionally, ensure that RetailSale measurements have been enabled.</span></span> <span data-ttu-id="ac9da-116">Lisätietoja tästä määritysprosessista on kohdassa [Mittayksiköiden käsitteleminen](https://docs.microsoft.com/dynamics365/ai/customer-insights/pm-measures).</span><span class="sxs-lookup"><span data-stu-id="ac9da-116">To learn more about this set up process, see [Work with measures](https://docs.microsoft.com/dynamics365/ai/customer-insights/pm-measures).</span></span>

## <a name="azure-ad-identity-configuration"></a><span data-ttu-id="ac9da-117">Azure AD -tunnisteen konfiguraatio</span><span class="sxs-lookup"><span data-stu-id="ac9da-117">Azure AD Identity configuration</span></span>

<span data-ttu-id="ac9da-118">Tämä vaihe on pakollinen kaikille asiakkaille, jotka käyttävät infrastruktuuria palvelun (IaaS) määrityksenä.</span><span class="sxs-lookup"><span data-stu-id="ac9da-118">This step is required for all customers running an infra-structure as a service (IaaS) configuration.</span></span> <span data-ttu-id="ac9da-119">Jos asiakas käyttää Service fabric (SF) -palvelua, tämän vaiheen tulisi olla automaattinen ja suosittelemme, että asetus määritetään odotetulla tavalla.</span><span class="sxs-lookup"><span data-stu-id="ac9da-119">For customers running on service fabric (SF), this step should be automatic and we recommend verifying the setting is configured as expected.</span></span>

### <a name="setup"></a><span data-ttu-id="ac9da-120">Määritys</span><span class="sxs-lookup"><span data-stu-id="ac9da-120">Setup</span></span>

1. <span data-ttu-id="ac9da-121">Etsi taustaohjelmistosta **Azure Active Directory -sovellukset** -sivu.</span><span class="sxs-lookup"><span data-stu-id="ac9da-121">From the back office, search for the **Azure Active Directory applications** page.</span></span>
2. <span data-ttu-id="ac9da-122">Tarkista, onko "RecommendationSystemApplication-1"-merkintää olemassa.</span><span class="sxs-lookup"><span data-stu-id="ac9da-122">Verify if an entry exists for "RecommendationSystemApplication-1".</span></span>

<span data-ttu-id="ac9da-123">Jos tapahtumaa ei ole olemassa, lisää uusi tietue, jossa on seuraavat tiedot:</span><span class="sxs-lookup"><span data-stu-id="ac9da-123">If the entry does not exist, add a new entry with the following information:</span></span>

- <span data-ttu-id="ac9da-124">**Asiakastunnus** - d37b07e8-dd1c-4514-835d-8b918e6f9727</span><span class="sxs-lookup"><span data-stu-id="ac9da-124">**Client Id** - d37b07e8-dd1c-4514-835d-8b918e6f9727</span></span>
- <span data-ttu-id="ac9da-125">**Nimi** - RecommendationSystemApplication-1</span><span class="sxs-lookup"><span data-stu-id="ac9da-125">**Name** - RecommendationSystemApplication-1</span></span>
- <span data-ttu-id="ac9da-126">**Käyttäjätunnus** - RetailServiceAccount</span><span class="sxs-lookup"><span data-stu-id="ac9da-126">**User Id** - RetailServiceAccount</span></span>

<span data-ttu-id="ac9da-127">Tallenna ja sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="ac9da-127">Save and close the page.</span></span> 

## <a name="turn-on-recommendations"></a><span data-ttu-id="ac9da-128">Suositusten ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="ac9da-128">Turn on recommendations</span></span>

<span data-ttu-id="ac9da-129">Voit ottaa tuotesuositukset käyttöön noudattamalla seuraavia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="ac9da-129">To turn on product recommendations, follow these steps.</span></span>

1. <span data-ttu-id="ac9da-130">Hae **Ominaisuuksien hallinta** Commercen pääkonttoriversiossa.</span><span class="sxs-lookup"><span data-stu-id="ac9da-130">In Commerce headquarters, search for **Feature Management**.</span></span>
1. <span data-ttu-id="ac9da-131">Avaa käytettävissä olevien ominaisuuksien luettelo valitsemalla **Kaikki**.</span><span class="sxs-lookup"><span data-stu-id="ac9da-131">Select **All** to see a list of available features.</span></span> 
1. <span data-ttu-id="ac9da-132">Kirjoita hakuruutuun **Suositukset**.</span><span class="sxs-lookup"><span data-stu-id="ac9da-132">In the search box, enter **Recommendations**.</span></span>
1. <span data-ttu-id="ac9da-133">Valitse **Tuotesuositukset** -ominaisuus.</span><span class="sxs-lookup"><span data-stu-id="ac9da-133">Select the **Product recommendations** feature.</span></span>
1. <span data-ttu-id="ac9da-134">Valitse **Tuotesuositukset** -ominaisuusruudussa **Ota käyttöön nyt**.</span><span class="sxs-lookup"><span data-stu-id="ac9da-134">In the **Product recommendations** properties pane, select **Enable now**.</span></span>

![Suositusten ottaminen käyttöön](./media/FeatureManagement_Recommendations.PNG)

> [!NOTE]
> <span data-ttu-id="ac9da-136">Tämä menettely käynnistää tuotesuositusluetteloiden luontiprosessin.</span><span class="sxs-lookup"><span data-stu-id="ac9da-136">This procedure starts the process of generating product recommendation lists.</span></span> <span data-ttu-id="ac9da-137">Luetteloiden luominen, niiden saaminen käyttöön ja näkyminen myyntipisteessä tai Dynamics 365 Commerce -sovelluksessa voi kestää useita tunteja.</span><span class="sxs-lookup"><span data-stu-id="ac9da-137">It may take several hours before the lists are available and can be viewed at the point of sale (POS) or in Dynamics 365 Commerce.</span></span>

## <a name="configure-recommendation-list-parameters"></a><span data-ttu-id="ac9da-138">Suositusluettelon parametrien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="ac9da-138">Configure recommendation list parameters</span></span>

<span data-ttu-id="ac9da-139">Oletusarvoisesti tekoälyyn perustuva tuotesuositusluettelo sisältää ehdotetut arvot.</span><span class="sxs-lookup"><span data-stu-id="ac9da-139">By default, the AI-ML-based product recommendation list provides suggested values.</span></span> <span data-ttu-id="ac9da-140">Voit muuttaa ehdotettuja oletusarvoja haluamallasi tavalla.</span><span class="sxs-lookup"><span data-stu-id="ac9da-140">You can change the default suggested values to suit the flow of your business.</span></span> <span data-ttu-id="ac9da-141">Lisätietoja oletusparametrien muuttamisesta on kohdassa [Tekoälyn koneoppimiseen perustuvan tuotesuositusluettelon hallinta](modify-product-recommendation-results.md).</span><span class="sxs-lookup"><span data-stu-id="ac9da-141">To learn more about how to change the default parameters, go to [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>

## <a name="show-recommendations-on-pos-devices"></a><span data-ttu-id="ac9da-142">Suositusten näyttäminen myyntipistelaitteissa</span><span class="sxs-lookup"><span data-stu-id="ac9da-142">Show recommendations on POS devices</span></span>

<span data-ttu-id="ac9da-143">Kun suositukset on otettu käyttöön Commercen taustatoiminnossa, suosituspaneeli on lisättävä ohjausobjektin myyntipistenäyttöön asettelutyökalun avulla.</span><span class="sxs-lookup"><span data-stu-id="ac9da-143">After enabling recommendations in Commerce back office, the recommendations panel must be added to the control POS screen using the layout tool.</span></span> <span data-ttu-id="ac9da-144">Lisä tietoja tästä prosessista on kohdassa [Suositusten ohjausobjektin lisääminen myyntipisteen laitteen tapahtumaruudulle](add-recommendations-control-pos-screen.md).</span><span class="sxs-lookup"><span data-stu-id="ac9da-144">To learn about this process, see [Add a recommendations control to the transaction screen on POS devices](add-recommendations-control-pos-screen.md).</span></span> 

## <a name="enable-personalized-recommendations"></a><span data-ttu-id="ac9da-145">Kohdennettujen suositusten ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="ac9da-145">Enable personalized recommendations</span></span>

<span data-ttu-id="ac9da-146">Dynamics 365 Commerce -ohjelmassa jälleenmyyjät voivat tehdä mukautettuja tuotesuosituksia (eli personointeja).</span><span class="sxs-lookup"><span data-stu-id="ac9da-146">In Dynamics 365 Commerce, retailers can make personalized product recommendations (also known as personalization) available.</span></span> <span data-ttu-id="ac9da-147">Näin henkilökohtaiset suositukset voidaan sisällyttää asiakaskokemukseen verkossa ja myyntipisteessä.</span><span class="sxs-lookup"><span data-stu-id="ac9da-147">In this way, personalized recommendations can be incorporated into the online customer experience and at the point of sale.</span></span> <span data-ttu-id="ac9da-148">Kun mukautustoiminto on käytössä, järjestelmä voi liittää käyttäjän osto- ja tuotetiedot ja luoda yksilöllisiä tuotesuosituksia.</span><span class="sxs-lookup"><span data-stu-id="ac9da-148">When the personalization functionality is turned on, the system can associate a user's purchase and product information to generate individualized product recommendations.</span></span>

<span data-ttu-id="ac9da-149">Lisätietoja mukautetuista suosituksista on kohdassa [Mukautettujen suositusten ottaminen käyttöön](personalized-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="ac9da-149">To learn more about personalized recommendations, see [Enable personalized recommendations](personalized-recommendations.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ac9da-150">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="ac9da-150">Additional resources</span></span>

[<span data-ttu-id="ac9da-151">Tuotesuositusten yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="ac9da-151">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="ac9da-152">Azure Data Lake Storagen käyttöönotto Dynamics 365 Commerce -ympäristössä</span><span class="sxs-lookup"><span data-stu-id="ac9da-152">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="ac9da-153">Kohdennettujen suositusten ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="ac9da-153">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="ac9da-154">"Osta samankaltaisia tyylejä" -suositusten käyttöönotto</span><span class="sxs-lookup"><span data-stu-id="ac9da-154">Enable "shop similar looks" recommendations</span></span>](shop-similar-looks.md)

[<span data-ttu-id="ac9da-155">Kohdennetuista tuotesuosituksista kieltäytyminen</span><span class="sxs-lookup"><span data-stu-id="ac9da-155">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="ac9da-156">Tuotesuositusten lisääminen myyntipisteessä</span><span class="sxs-lookup"><span data-stu-id="ac9da-156">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="ac9da-157">Suositusten lisääminen tapahtumanäyttöön</span><span class="sxs-lookup"><span data-stu-id="ac9da-157">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="ac9da-158">AI-ML-suositusten tulosten muokkaaminen</span><span class="sxs-lookup"><span data-stu-id="ac9da-158">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="ac9da-159">Kuratoitujen suositusten manuaalinen luominen</span><span class="sxs-lookup"><span data-stu-id="ac9da-159">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="ac9da-160">Suositusten luominen esittelytietojen avulla</span><span class="sxs-lookup"><span data-stu-id="ac9da-160">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="ac9da-161">Tuotesuositukset – usein kysytyt kysymykset</span><span class="sxs-lookup"><span data-stu-id="ac9da-161">Product recommendations FAQ</span></span>](faq-recommendations.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]