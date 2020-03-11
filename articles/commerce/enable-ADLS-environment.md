---
title: ADLS:n käyttöönotto Dynamics 365 Commerce -ympäristössä
description: Tässä ohjeaiheessa selitetään, miten voit ottaa Azure Data Lake Storagen (ADLS:n) käyttöön Dynamics 365 Commerce -ympäristöä varten. Tämä on edellytys tuotesuositusten käyttöönotolle.
author: bebeale
manager: AnnBe
ms.date: 02/03/2020
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
ms.openlocfilehash: 068eb522bd44e02dd31d3337a051691a956637fc
ms.sourcegitcommit: b5ecde955a69f577de46e7db10e89caaedeb2b49
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/04/2020
ms.locfileid: "3025242"
---
# <a name="enable-adls-in-a-dynamics-365-commerce-environment"></a><span data-ttu-id="d8249-103">ADLS:n käyttöönotto Dynamics 365 Commerce -ympäristössä</span><span class="sxs-lookup"><span data-stu-id="d8249-103">Enable ADLS in a Dynamics 365 Commerce environment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="d8249-104">Tässä ohjeaiheessa selitetään, miten voit ottaa Azure Data Lake Storagen (ADLS:n) käyttöön Dynamics 365 Commerce -ympäristöä varten. Tämä on edellytys tuotesuositusten käyttöönotolle.</span><span class="sxs-lookup"><span data-stu-id="d8249-104">This topic explains how to enable and test Azure Data Lake Storage (ADLS) for a Dynamics 365 Commerce environment, which is a prerequisite for enabling product recommendations.</span></span>

## <a name="overview"></a><span data-ttu-id="d8249-105">Yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="d8249-105">Overview</span></span>

<span data-ttu-id="d8249-106">Dynamics 365 Commerce -ratkaisussa kaikkia tuote- ja tapahtumatietoja seurataan ympäristön yksikkösäilöön.</span><span class="sxs-lookup"><span data-stu-id="d8249-106">In the Dynamics 365 Commerce solution, all product and transaction information is tracked in the environment's Entity store.</span></span> <span data-ttu-id="d8249-107">Näiden tietojen muiden Dynamics 365:n palvelujen, kuten tietojen analytiikan, yritystietojen ja mukautettujen suositusten, käyttöön asettamista varten ympäristö on yhdistettävä asiakkaan omistamaan toisen sukupolven Azure Data Lake Storage (ADLS) -ratkaisuun.</span><span class="sxs-lookup"><span data-stu-id="d8249-107">To make this data accessible to other Dynamics 365 services, such as data analytics, business intelligence, and personalized recommendations, it is necessary to connect the environment to a customer-owned Azure Data Lake Storage Gen 2 (ADLS) solution.</span></span>

<span data-ttu-id="d8249-108">Koska ADLS on määritetty ympäristössä, kaikki tarvittavat tiedot peilataan yksikkösäilöstä samalla, kun ne ovat edelleen suojattuja ja asiakkaan valvonnassa.</span><span class="sxs-lookup"><span data-stu-id="d8249-108">As ADLS is configured in an environment, all necessary data is mirrored from the Entity store while still being protected and under customer's control.</span></span>

<span data-ttu-id="d8249-109">Jos myös tuotesuositukset tai mukautetut suositukset ovat käytössä ympäristössä, tuotesuositusten pinolle myönnetään käyttöoikeus ADLS:n varattuun kansioon asiakastietojen noutamista ja niihin perustuvien suositusten laskemista varten.</span><span class="sxs-lookup"><span data-stu-id="d8249-109">If product recommendations or personalized recommendations are also enabled in the environment, then the product recommendations stack will be granted access to the dedicated folder in ADLS to retrieve the customer’s data and compute recommendations based on it.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="d8249-110">Edellytykset</span><span class="sxs-lookup"><span data-stu-id="d8249-110">Prerequisites</span></span>

<span data-ttu-id="d8249-111">Asiakkailla on oltava ADLS määritettynä omistamassaan Azure-tilauksessa.</span><span class="sxs-lookup"><span data-stu-id="d8249-111">Customers need to have ADLS configured in an Azure subscription that they own.</span></span> <span data-ttu-id="d8249-112">Tässä ohjeaiheessa ei käsitellä Azure-tilauksen hankkimista eikä ADLS-yhteensopivan säilötilin määrittämistä.</span><span class="sxs-lookup"><span data-stu-id="d8249-112">This topic does not cover the purchase of an Azure subscription or the setup of an ADLS-enabled storage account.</span></span>

<span data-ttu-id="d8249-113">Lisätietoja ADLS:stä on kohdassa [ADLS:n virallinen dokumentaatio](https://azure.microsoft.com/pricing/details/storage/data-lake).</span><span class="sxs-lookup"><span data-stu-id="d8249-113">For more information about ADLS, see [ADLS official documentation](https://azure.microsoft.com/pricing/details/storage/data-lake).</span></span>
  
## <a name="configuration-steps"></a><span data-ttu-id="d8249-114">Määritysvaiheet</span><span class="sxs-lookup"><span data-stu-id="d8249-114">Configuration steps</span></span>

<span data-ttu-id="d8249-115">Tässä osassa käsitellään ADLS:n ympäristössä käyttöön ottamisen edellyttämät määritysvaiheet.</span><span class="sxs-lookup"><span data-stu-id="d8249-115">This section covers the configuration steps necessary for enabling ADLS in an environment.</span></span>

### <a name="enable-adls-in-the-environment"></a><span data-ttu-id="d8249-116">ADLS:n käyttöönotto ympäristössä</span><span class="sxs-lookup"><span data-stu-id="d8249-116">Enable ADLS in the environment</span></span>

1. <span data-ttu-id="d8249-117">Kirjaudu ympäristön taustajärjestelmäportaaliin.</span><span class="sxs-lookup"><span data-stu-id="d8249-117">Log in to the environment's back office portal.</span></span>
1. <span data-ttu-id="d8249-118">Etsi **Järjestelmäparametrit** ja siirry **Tietoyhteydet**-välilehteen.</span><span class="sxs-lookup"><span data-stu-id="d8249-118">Search for **System Parameters** and navigate to the **Data connections** tab.</span></span> 
1. <span data-ttu-id="d8249-119">Määritä **Ota Data Lake -integrointi käyttöön** -parametrin arvoksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="d8249-119">Set **Enable Data Lake integration** to **Yes**.</span></span>
1. <span data-ttu-id="d8249-120">Määritä **Data Laken vähittäinen päivitys** -parametrin arvoksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="d8249-120">Set **Trickle update Data Lake** to **Yes**.</span></span>
1. <span data-ttu-id="d8249-121">Syötä sitten seuraavat vaaditut tiedot:</span><span class="sxs-lookup"><span data-stu-id="d8249-121">Next, enter the following required information:</span></span>
    1. <span data-ttu-id="d8249-122">**Sovellustunnus** // **Sovelluksen salauskoodi** // **DNS-nimi** – Tarvitaan siihen KeyVault-säilöön yhdistämistä varten, johon ADLS-salauskoodi on tallennettu.</span><span class="sxs-lookup"><span data-stu-id="d8249-122">**Application ID** // **Application Secret** // **DNS Name** - Needed to connect to KeyVault where the ADLS secret is stored.</span></span>
    1. <span data-ttu-id="d8249-123">**Salainen nimi** – KeyVaultiin tallennettu ja ADLS-todennukseen käytetty salainen nimi.</span><span class="sxs-lookup"><span data-stu-id="d8249-123">**Secret name** - The secret name stored in KeyVault and used to authenticate with ADLS.</span></span>
1. <span data-ttu-id="d8249-124">Tallenna muutoksesi sivun vasemmassa yläkulmassa.</span><span class="sxs-lookup"><span data-stu-id="d8249-124">Save your changes in the top left corner of the page.</span></span>

<span data-ttu-id="d8249-125">Seuraavassa kuvassa näkyy esimerkki ADLS-määrityksessä.</span><span class="sxs-lookup"><span data-stu-id="d8249-125">The following image shows an example ADLS configuration.</span></span>

![Esimerkki ADLS-määrityksestä](./media/exampleADLSConfig1.png)

### <a name="test-the-adls-connection"></a><span data-ttu-id="d8249-127">ADLS-yhteyden testaaminen</span><span class="sxs-lookup"><span data-stu-id="d8249-127">Test the ADLS connection</span></span>

1. <span data-ttu-id="d8249-128">Testaa yhteys KeyVaultiin **Testaa Azure Vault** -linkin avulla.</span><span class="sxs-lookup"><span data-stu-id="d8249-128">Test the connection to KeyVault using the **Test Azure Key Vault** link.</span></span>
1. <span data-ttu-id="d8249-129">Testaa yhteys ADLS:ään käyttämällä **Testaa Azure-tallennustila** -linkin avulla.</span><span class="sxs-lookup"><span data-stu-id="d8249-129">Test the connection to ADLS using the **Test Azure Storage** link.</span></span>

> [!NOTE]
> <span data-ttu-id="d8249-130">Jos testit epäonnistuvat, tarkista uudelleen, että kaikki edellä lisätyt KeyVault-tiedot ovat oikein. Kokeile sen jälkeen uudelleen.</span><span class="sxs-lookup"><span data-stu-id="d8249-130">If the tests fail, double-check that all of the KeyVault information added above is correct, then try again.</span></span>

<span data-ttu-id="d8249-131">Kun kaikki yhteystestit ovat onnistuneet, sinun on otettava yksikkötallennustilan automaattinen päivitys käyttöön.</span><span class="sxs-lookup"><span data-stu-id="d8249-131">Once the connection tests are successful, you must enable automatic refresh for Entity store.</span></span>

<span data-ttu-id="d8249-132">Ota yksikkötallennustilan päivitys käyttöön seuraavia vaiheita noudattamalla.</span><span class="sxs-lookup"><span data-stu-id="d8249-132">To enable automatic refresh for Entity store, follow these steps.</span></span>

1. <span data-ttu-id="d8249-133">Etsi kohdetta **Entiteettitallennustila**.</span><span class="sxs-lookup"><span data-stu-id="d8249-133">Search for **Entity Store**.</span></span>
1. <span data-ttu-id="d8249-134">Siirry vasemmalla olevassa luettelossa **RetailSales**-kirjaukseen ja valitse **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="d8249-134">In the list on the left, navigate to the **RetailSales** entry, and select **Edit**.</span></span>
1. <span data-ttu-id="d8249-135">Varmista, että **Automaattinen päivitys käytössä** -kohdan arvoksi on määritetty **Kyllä**, valitse **Päivitys** ja sitten **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="d8249-135">Ensure that **Automatic Refresh Enabled** is set to **Yes**, select **Refresh**, and then select **Save**.</span></span>

<span data-ttu-id="d8249-136">Seuraavassa kuvassa näkyy esimerkki yksikkösäilöstä, jossa automaattinen päivitys on käytössä.</span><span class="sxs-lookup"><span data-stu-id="d8249-136">The following image shows an example of Entity store with automatic refresh enabled.</span></span>

![Esimerkki yksikkötallennustilasta, jossa automaattinen päivitys on käytössä](./media/exampleADLSConfig2.png)

<span data-ttu-id="d8249-138">ADLS on nyt määritetty ympäristölle.</span><span class="sxs-lookup"><span data-stu-id="d8249-138">ADLS is now configured for the environment.</span></span> 

<span data-ttu-id="d8249-139">Jos et ole vielä suorittanut niitä, suorita ympäristön [tuotesuositusten ja mukautusten käyttöönoton](enable-product-recommendations.md) vaiheet.</span><span class="sxs-lookup"><span data-stu-id="d8249-139">If not completed already, follow the steps for [enabling product recommendations and personalization](enable-product-recommendations.md) for the environment.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d8249-140">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="d8249-140">Additional resources</span></span>

[<span data-ttu-id="d8249-141">Tuotesuositusten yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="d8249-141">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="d8249-142">Ota tuotesuositukset käyttöön</span><span class="sxs-lookup"><span data-stu-id="d8249-142">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="d8249-143">Tuotesuositusluetteloiden lisääminen sivuille</span><span class="sxs-lookup"><span data-stu-id="d8249-143">Add product recommendation lists to pages</span></span>](add-reco-list-to-page.md)

[<span data-ttu-id="d8249-144">Suositusten ohjausobjektin lisääminen myyntipisteen laitteen tapahtumaruudulle</span><span class="sxs-lookup"><span data-stu-id="d8249-144">Add a recommendations control to the transaction screen on POS devices</span></span>](../retail/add-recommendations-control-pos-screen.md?toc=/dynamics365/commerce/toc.json)

