---
title: Ota tuotesuositukset käyttöön
description: Tässä ohjeaiheessa kerrotaa, miten tekoälyn koneoppimiseen perustuvia tuotesuosituksia voidaan tehdä Microsoft Dynamics 365 Commerce -asiakkaiden käyttöä varten.
author: bebeale
manager: AnnBe
ms.date: 04/13/2020
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
ms.openlocfilehash: d38d7b0e98d84e23d7a51c5d8ee65df4a3b9e4a7
ms.sourcegitcommit: dbff1c6bb371a443a0cd2a310f5a48d5c21b08ca
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/13/2020
ms.locfileid: "3259791"
---
# <a name="enable-product-recommendations"></a><span data-ttu-id="e179f-103">Ota tuotesuositukset käyttöön</span><span class="sxs-lookup"><span data-stu-id="e179f-103">Enable product recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e179f-104">Tässä ohjeaiheessa kerrotaa, miten tekoälyn koneoppimiseen perustuvia tuotesuosituksia voidaan tehdä Microsoft Dynamics 365 Commerce -asiakkaiden käyttöä varten.</span><span class="sxs-lookup"><span data-stu-id="e179f-104">This topic explains how to make product recommendations that are based on artificial intelligence-machine learning (AI-ML) available for Microsoft Dynamics 365 Commerce customers.</span></span> <span data-ttu-id="e179f-105">Lisätietoja tuotesuositusten luetteloista on kohdassa [Tuotesuositusten yleiskatsaus](product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="e179f-105">For more information about product recommendation lists, see [Product recommendations overview](product-recommendations.md).</span></span>

## <a name="recommendations-pre-check"></a><span data-ttu-id="e179f-106">Suositusten esitarkistus</span><span class="sxs-lookup"><span data-stu-id="e179f-106">Recommendations pre-check</span></span>

<span data-ttu-id="e179f-107">Ota huomioon ennen käyttöönottoa, että tuotesuosituksia tuetaan vain Commerce-asiakkaille, jotka ovat siirtäneet tallennustilansa Azure Data Lake Storagea (ADLS:ää) käyttäen.</span><span class="sxs-lookup"><span data-stu-id="e179f-107">Before enabling, note that product recommendations are only supported for Commerce customers who have migrated their storage to using Azure Data Lake Storage (ADLS).</span></span> 

<span data-ttu-id="e179f-108">Seuraavat kokoonpanot on otettava käyttöön taustajärjestelmässä ennen suositusten käyttöönottoa:</span><span class="sxs-lookup"><span data-stu-id="e179f-108">The following configurations must be enabled in the back office before enabling recommendations:</span></span>

1. <span data-ttu-id="e179f-109">Varmista, että ADLS on ostettu ja todennettu onnistuneesti ympäristössä.</span><span class="sxs-lookup"><span data-stu-id="e179f-109">Ensure that ADLS has been purchased and successfully verified in the environment.</span></span> <span data-ttu-id="e179f-110">Katso lisätietoja kohdasta [Varmista, että ADLS on ostettu ja todennettu onnistuneesti ympäristössä](enable-ADLS-environment.md).</span><span class="sxs-lookup"><span data-stu-id="e179f-110">For more information, see [Ensure that ADLS has been purchased and successfully verified in the environment](enable-ADLS-environment.md).</span></span>
2. <span data-ttu-id="e179f-111">Varmista, että yksikkösäilön päivitys on automatisoitu.</span><span class="sxs-lookup"><span data-stu-id="e179f-111">Ensure that the entity store refresh has been automated.</span></span> <span data-ttu-id="e179f-112">Lisätietoja on kohdassa [Varmista, että yksikkösäilön päivitys on automatisoitu](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md).</span><span class="sxs-lookup"><span data-stu-id="e179f-112">For more information, see [Ensure that the Entity store refresh has been automated](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md).</span></span>
3. <span data-ttu-id="e179f-113">Vahvista, että Azure AD -käyttäjätietojen määritys sisältää suositusten merkinnän.</span><span class="sxs-lookup"><span data-stu-id="e179f-113">Confirm that Azure AD Identity configuration contains an entry for Recommendations.</span></span> <span data-ttu-id="e179f-114">Lisätietoja tästä toiminnosta alla.</span><span class="sxs-lookup"><span data-stu-id="e179f-114">More information on how to do this action is below.</span></span>

<span data-ttu-id="e179f-115">Varmista myös, että RetailSale-mittarit on otettu käyttöön.</span><span class="sxs-lookup"><span data-stu-id="e179f-115">Additionally, ensure that RetailSale measurements have been enabled.</span></span> <span data-ttu-id="e179f-116">Lisätietoja tästä määritysprosessista on kohdassa [Mittayksiköiden käsitteleminen](https://docs.microsoft.com/dynamics365/ai/customer-insights/pm-measures).</span><span class="sxs-lookup"><span data-stu-id="e179f-116">To learn more about this set up process, see [Work with measures](https://docs.microsoft.com/dynamics365/ai/customer-insights/pm-measures).</span></span>

## <a name="azure-ad-identity-configuration"></a><span data-ttu-id="e179f-117">Azure AD -tunnisteen konfiguraatio</span><span class="sxs-lookup"><span data-stu-id="e179f-117">Azure AD Identity configuration</span></span>

<span data-ttu-id="e179f-118">Tämä vaihe on pakollinen kaikille asiakkaille, jotka käyttävät infrastruktuuria palvelun (IaaS) määrityksenä.</span><span class="sxs-lookup"><span data-stu-id="e179f-118">This step is required for all customers running an infra-structure as a service (IaaS) configuration.</span></span> <span data-ttu-id="e179f-119">Jos asiakas käyttää Service fabric (SF) -palvelua, tämän vaiheen tulisi olla automaattinen ja suosittelemme, että asetus määritetään odotetulla tavalla.</span><span class="sxs-lookup"><span data-stu-id="e179f-119">For customers running on service fabric (SF), this step should be automatic and we recommend verifying the setting is configured as expected.</span></span>

### <a name="setup"></a><span data-ttu-id="e179f-120">Määritys</span><span class="sxs-lookup"><span data-stu-id="e179f-120">Setup</span></span>

1. <span data-ttu-id="e179f-121">Etsi taustaohjelmistosta **Azure Active Directory -sovellukset** -sivu.</span><span class="sxs-lookup"><span data-stu-id="e179f-121">From the back office, search for the **Azure Active Directory applications** page.</span></span>
2. <span data-ttu-id="e179f-122">Tarkista, onko "RecommendationSystemApplication-1"-merkintää olemassa.</span><span class="sxs-lookup"><span data-stu-id="e179f-122">Verify if an entry exists for "RecommendationSystemApplication-1".</span></span>

<span data-ttu-id="e179f-123">Jos tapahtumaa ei ole olemassa, lisää uusi tietue, jossa on seuraavat tiedot:</span><span class="sxs-lookup"><span data-stu-id="e179f-123">If the entry does not exist, add a new entry with the following information:</span></span>

- <span data-ttu-id="e179f-124">**Asiakastunnus** - d37b07e8-dd1c-4514-835d-8b918e6f9727</span><span class="sxs-lookup"><span data-stu-id="e179f-124">**Client Id** - d37b07e8-dd1c-4514-835d-8b918e6f9727</span></span>
- <span data-ttu-id="e179f-125">**Nimi** - RecommendationSystemApplication-1</span><span class="sxs-lookup"><span data-stu-id="e179f-125">**Name** - RecommendationSystemApplication-1</span></span>
- <span data-ttu-id="e179f-126">**Käyttäjätunnus** - RetailServiceAccount</span><span class="sxs-lookup"><span data-stu-id="e179f-126">**User Id** - RetailServiceAccount</span></span>

<span data-ttu-id="e179f-127">Tallenna ja sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="e179f-127">Save and close the page.</span></span> 

## <a name="turn-on-recommendations"></a><span data-ttu-id="e179f-128">Suositusten ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="e179f-128">Turn on recommendations</span></span>

<span data-ttu-id="e179f-129">Voit ottaa tuotesuositukset käyttöön noudattamalla seuraavia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="e179f-129">To turn on product recommendations, follow these steps.</span></span>

1. <span data-ttu-id="e179f-130">Siirry kohtaan **Retail ja Commerce &gt; Tuotesuositukset &gt; Suositusparametrit**.</span><span class="sxs-lookup"><span data-stu-id="e179f-130">Go to **Retail and Commerce &gt; Product recommendations &gt; Recommendation parameters**.</span></span>
1. <span data-ttu-id="e179f-131">Valitse jaettujen parametrien luettelossa **Suositusluettelot**.</span><span class="sxs-lookup"><span data-stu-id="e179f-131">In the list of shared parameters, select **Recommendation Lists**.</span></span>
1. <span data-ttu-id="e179f-132">Määritä **Ota suositukset käyttöön** -asetukseksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="e179f-132">Set the **Enable recommendations** option to **Yes**.</span></span>

![Suositusten ottaminen käyttöön](./media/enablepersonalization.png)

> [!NOTE]
> <span data-ttu-id="e179f-134">Tämä menettely käynnistää tuotesuositusluetteloiden luontiprosessin.</span><span class="sxs-lookup"><span data-stu-id="e179f-134">This procedure starts the process of generating product recommendation lists.</span></span> <span data-ttu-id="e179f-135">Luetteloiden luominen, niiden saaminen käyttöön ja näkyminen myyntipisteessä tai Dynamics 365 Commerce -sovelluksessa voi kestää useita tunteja.</span><span class="sxs-lookup"><span data-stu-id="e179f-135">It may take several hours before the lists are available and can be viewed at the point of sale (POS) or in Dynamics 365 Commerce.</span></span>

## <a name="configure-recommendation-list-parameters"></a><span data-ttu-id="e179f-136">Suositusluettelon parametrien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="e179f-136">Configure recommendation list parameters</span></span>

<span data-ttu-id="e179f-137">Oletusarvoisesti tekoälyyn perustuva tuotesuositusluettelo sisältää ehdotetut arvot.</span><span class="sxs-lookup"><span data-stu-id="e179f-137">By default, the AI-ML-based product recommendation list provides suggested values.</span></span> <span data-ttu-id="e179f-138">Voit muuttaa ehdotettuja oletusarvoja haluamallasi tavalla.</span><span class="sxs-lookup"><span data-stu-id="e179f-138">You can change the default suggested values to suit the flow of your business.</span></span> <span data-ttu-id="e179f-139">Lisätietoja oletusparametrien muuttamisesta on kohdassa [Tekoälyn koneoppimiseen perustuvan tuotesuositusluettelon hallinta](modify-product-recommendation-results.md).</span><span class="sxs-lookup"><span data-stu-id="e179f-139">To learn more about how to change the default parameters, go to [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>

## <a name="show-recommendations-on-pos-devices"></a><span data-ttu-id="e179f-140">Suositusten näyttäminen myyntipistelaitteissa</span><span class="sxs-lookup"><span data-stu-id="e179f-140">Show recommendations on POS devices</span></span>

<span data-ttu-id="e179f-141">Kun suositukset on otettu käyttöön Commercen taustatoiminnossa, suosituspaneeli on lisättävä ohjausobjektin myyntipistenäyttöön asettelutyökalun avulla.</span><span class="sxs-lookup"><span data-stu-id="e179f-141">After enabling recommendations in Commerce back office, the recommendations panel must be added to the control POS screen using the layout tool.</span></span> <span data-ttu-id="e179f-142">Lisä tietoja tästä prosessista on kohdassa [Suositusten ohjausobjektin lisääminen myyntipisteen laitteen tapahtumaruudulle](add-recommendations-control-pos-screen.md).</span><span class="sxs-lookup"><span data-stu-id="e179f-142">To learn about this process, see [Add a recommendations control to the transaction screen on POS devices](add-recommendations-control-pos-screen.md).</span></span> 

## <a name="enable-personalized-recommendations"></a><span data-ttu-id="e179f-143">Kohdennettujen suositusten ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="e179f-143">Enable personalized recommendations</span></span>

<span data-ttu-id="e179f-144">Dynamics 365 Commerce -ohjelmassa jälleenmyyjät voivat tehdä mukautettuja tuotesuosituksia (eli personointeja).</span><span class="sxs-lookup"><span data-stu-id="e179f-144">In Dynamics 365 Commerce, retailers can make personalized product recommendations (also known as personalization) available.</span></span> <span data-ttu-id="e179f-145">Näin henkilökohtaiset suositukset voidaan sisällyttää asiakaskokemukseen verkossa ja myyntipisteessä.</span><span class="sxs-lookup"><span data-stu-id="e179f-145">In this way, personalized recommendations can be incorporated into the online customer experience and at the point of sale.</span></span> <span data-ttu-id="e179f-146">Kun mukautustoiminto on käytössä, järjestelmä voi liittää käyttäjän osto- ja tuotetiedot ja luoda yksilöllisiä tuotesuosituksia.</span><span class="sxs-lookup"><span data-stu-id="e179f-146">When the personalization functionality is turned on, the system can associate a user's purchase and product information to generate individualized product recommendations.</span></span>

<span data-ttu-id="e179f-147">Lisätietoja mukautetuista suosituksista on kohdassa [Mukautettujen suositusten ottaminen käyttöön](personalized-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="e179f-147">To learn more about personalized recommendations, see [Enable personalized recommendations](personalized-recommendations.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e179f-148">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="e179f-148">Additional resources</span></span>

[<span data-ttu-id="e179f-149">Tuotesuositusten yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="e179f-149">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="e179f-150">ADLS:n käyttöönotto Dynamics 365 Commerce -ympäristössä</span><span class="sxs-lookup"><span data-stu-id="e179f-150">Enable ADLS in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="e179f-151">Kohdennettujen suositusten ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="e179f-151">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="e179f-152">Kohdennetuista tuotesuosituksista kieltäytyminen</span><span class="sxs-lookup"><span data-stu-id="e179f-152">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="e179f-153">Tuotesuositusten lisääminen myyntipisteessä</span><span class="sxs-lookup"><span data-stu-id="e179f-153">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="e179f-154">Suositusten lisääminen tapahtumanäyttöön</span><span class="sxs-lookup"><span data-stu-id="e179f-154">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="e179f-155">AI-ML-suositusten tulosten muokkaaminen</span><span class="sxs-lookup"><span data-stu-id="e179f-155">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="e179f-156">Kuratoitujen suositusten manuaalinen luominen</span><span class="sxs-lookup"><span data-stu-id="e179f-156">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="e179f-157">Suositusten luominen esittelytietojen avulla</span><span class="sxs-lookup"><span data-stu-id="e179f-157">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="e179f-158">Tuotesuositukset – usein kysytyt kysymykset</span><span class="sxs-lookup"><span data-stu-id="e179f-158">Product recommendations FAQ</span></span>](faq-recommendations.md)

