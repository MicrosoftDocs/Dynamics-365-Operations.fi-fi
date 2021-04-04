---
title: Azure Data Lake Storagen käyttöönotto Dynamics 365 Commerce -ympäristössä
description: Tässä ohjeaiheessa selitetään, miten voit ottaa Azure Data Lake Storagen käyttöön Dynamics 365 Commerce -ympäristöä varten. Tämä on edellytys tuotesuositusten käyttöönotolle.
author: bebeale
manager: AnnBe
ms.date: 04/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 5887ae7983fd817a929a185327671b301808b354
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/19/2021
ms.locfileid: "5478233"
---
# <a name="enable-azure-data-lake-storage-in-a-dynamics-365-commerce-environment"></a><span data-ttu-id="8a30d-103">Azure Data Lake Storagen käyttöönotto Dynamics 365 Commerce -ympäristössä</span><span class="sxs-lookup"><span data-stu-id="8a30d-103">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="8a30d-104">Tässä ohjeaiheessa selitetään, miten voit ottaa Azure Data Lake Storagen käyttöön Dynamics 365 Commerce -ympäristöä varten. Tämä on edellytys tuotesuositusten käyttöönotolle.</span><span class="sxs-lookup"><span data-stu-id="8a30d-104">This topic explains how to enable and test Azure Data Lake Storage for a Dynamics 365 Commerce environment, which is a prerequisite for enabling product recommendations.</span></span>

<span data-ttu-id="8a30d-105">Dynamics 365 Commerce -ratkaisussa kaikkia tuote- ja tapahtumatietoja seurataan ympäristön yksikkösäilöön.</span><span class="sxs-lookup"><span data-stu-id="8a30d-105">In the Dynamics 365 Commerce solution, all product and transaction information is tracked in the environment's Entity store.</span></span> <span data-ttu-id="8a30d-106">Näiden tietojen muiden Dynamics 365:n palvelujen, kuten tietojen analytiikan, yritystietojen ja mukautettujen suositusten, käyttöön asettamista varten ympäristö on yhdistettävä asiakkaan omistamaan toisen sukupolven Azure Data Lake Storage Gen 2 -ratkaisuun.</span><span class="sxs-lookup"><span data-stu-id="8a30d-106">To make this data accessible to other Dynamics 365 services, such as data analytics, business intelligence, and personalized recommendations, it is necessary to connect the environment to a customer-owned Azure Data Lake Storage Gen 2 solution.</span></span>

<span data-ttu-id="8a30d-107">Koska Azure Data Lake Storage on määritetty ympäristössä, kaikki tarvittavat tiedot peilataan yksikkösäilöstä samalla, kun ne ovat edelleen suojattuja ja asiakkaan valvonnassa.</span><span class="sxs-lookup"><span data-stu-id="8a30d-107">As Azure Data Lake Storage is configured in an environment, all necessary data is mirrored from the Entity store while still being protected and under customer's control.</span></span>

<span data-ttu-id="8a30d-108">Jos myös tuotesuositukset tai mukautetut suositukset ovat käytössä ympäristössä, tuotesuositusten pinolle myönnetään käyttöoikeus Azure Data Lake Storagen varattuun kansioon asiakastietojen noutamista ja niihin perustuvien suositusten laskemista varten.</span><span class="sxs-lookup"><span data-stu-id="8a30d-108">If product recommendations or personalized recommendations are also enabled in the environment, then the product recommendations stack will be granted access to the dedicated folder in Azure Data Lake Storage to retrieve the customer’s data and compute recommendations based on it.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="8a30d-109">Edellytykset</span><span class="sxs-lookup"><span data-stu-id="8a30d-109">Prerequisites</span></span>

<span data-ttu-id="8a30d-110">Asiakkailla on oltava Azure Data Lake Storage määritettynä omistamassaan Azure-tilauksessa.</span><span class="sxs-lookup"><span data-stu-id="8a30d-110">Customers need to have Azure Data Lake Storage configured in an Azure subscription that they own.</span></span> <span data-ttu-id="8a30d-111">Tässä ohjeaiheessa ei käsitellä Azure-tilauksen hankkimista eikä Azure Data Lake Storage -yhteensopivan säilötilin määrittämistä.</span><span class="sxs-lookup"><span data-stu-id="8a30d-111">This topic does not cover the purchase of an Azure subscription or the setup of an Azure Data Lake Storage-enabled storage account.</span></span>

<span data-ttu-id="8a30d-112">Lisätietoja Azure Data Lake Storagesta on kohdassa [Azure Data Lake Storage Gen2:n virallinen dokumentaatio](https://azure.microsoft.com/pricing/details/storage/data-lake).</span><span class="sxs-lookup"><span data-stu-id="8a30d-112">For more information about Azure Data Lake Storage, see [Azure Data Lake Storage Gen2 official documentation](https://azure.microsoft.com/pricing/details/storage/data-lake).</span></span>
  
## <a name="configuration-steps"></a><span data-ttu-id="8a30d-113">Määritysvaiheet</span><span class="sxs-lookup"><span data-stu-id="8a30d-113">Configuration steps</span></span>

<span data-ttu-id="8a30d-114">Tämä osa sisältää määritysvaiheet, jotka ovat tarpeen, jotta Azure Data Lake Storage voidaan ottaa käyttöön ympäristössä, joka liittyy tuotesuosituksiin.</span><span class="sxs-lookup"><span data-stu-id="8a30d-114">This section covers the configuration steps necessary for enabling Azure Data Lake Storage in an environment as it relates to product recommendations.</span></span>
<span data-ttu-id="8a30d-115">Lisätietoja Azure Data Lake Storage -lisäosan käyttöön tarvittavista vaiheista on ohjeaiheessa [Määritä yksikkösäilö käytettäväksi Data Lakessa](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md).</span><span class="sxs-lookup"><span data-stu-id="8a30d-115">For a more in-depth overview of the steps required to enable Azure Data Lake Storage, see [Make entity store available as a Data Lake](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md).</span></span>

### <a name="enable-azure-data-lake-storage-in-the-environment"></a><span data-ttu-id="8a30d-116">Azure Data Lake Storagen käyttöönotto ympäristössä</span><span class="sxs-lookup"><span data-stu-id="8a30d-116">Enable Azure Data Lake Storage in the environment</span></span>

1. <span data-ttu-id="8a30d-117">Kirjaudu ympäristön taustajärjestelmäportaaliin.</span><span class="sxs-lookup"><span data-stu-id="8a30d-117">Log in to the environment's back office portal.</span></span>
1. <span data-ttu-id="8a30d-118">Etsi **Järjestelmäparametrit** ja siirry **Tietoyhteydet**-välilehteen.</span><span class="sxs-lookup"><span data-stu-id="8a30d-118">Search for **System Parameters** and navigate to the **Data connections** tab.</span></span> 
1. <span data-ttu-id="8a30d-119">Määritä **Ota Data Lake -integrointi käyttöön** -parametrin arvoksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="8a30d-119">Set **Enable Data Lake integration** to **Yes**.</span></span>
1. <span data-ttu-id="8a30d-120">Määritä **Data Laken vähittäinen päivitys** -parametrin arvoksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="8a30d-120">Set **Trickle update Data Lake** to **Yes**.</span></span>
1. <span data-ttu-id="8a30d-121">Syötä sitten seuraavat vaaditut tiedot:</span><span class="sxs-lookup"><span data-stu-id="8a30d-121">Next, enter the following required information:</span></span>
    1. <span data-ttu-id="8a30d-122">**Sovellustunnus** // **Sovelluksen salauskoodi** // **DNS-nimi** – Tarvitaan siihen KeyVault-säilöön yhdistämistä varten, johon Azure Data Lake Storage -salauskoodi on tallennettu.</span><span class="sxs-lookup"><span data-stu-id="8a30d-122">**Application ID** // **Application Secret** // **DNS Name** - Needed to connect to KeyVault where the Azure Data Lake Storage secret is stored.</span></span>
    1. <span data-ttu-id="8a30d-123">**Salainen nimi** – KeyVaultiin tallennettu ja Azure Data Lake Storage -todennukseen käytetty salainen nimi.</span><span class="sxs-lookup"><span data-stu-id="8a30d-123">**Secret name** - The secret name stored in KeyVault and used to authenticate with Azure Data Lake Storage.</span></span>
1. <span data-ttu-id="8a30d-124">Tallenna muutoksesi sivun vasemmassa yläkulmassa.</span><span class="sxs-lookup"><span data-stu-id="8a30d-124">Save your changes in the top left corner of the page.</span></span>

<span data-ttu-id="8a30d-125">Seuraavassa kuvassa näkyy esimerkki Azure Data Lake Storage -määrityksessä.</span><span class="sxs-lookup"><span data-stu-id="8a30d-125">The following image shows an example Azure Data Lake Storage configuration.</span></span>

![Esimerkki Azure Data Lake Storage -määrityksestä](./media/exampleADLSConfig1.png)

### <a name="test-the-azure-data-lake-storage-connection"></a><span data-ttu-id="8a30d-127">Azure Data Lake Storage -yhteyden testaaminen</span><span class="sxs-lookup"><span data-stu-id="8a30d-127">Test the Azure Data Lake Storage connection</span></span>

1. <span data-ttu-id="8a30d-128">Testaa yhteys KeyVaultiin **Testaa Azure Vault** -linkin avulla.</span><span class="sxs-lookup"><span data-stu-id="8a30d-128">Test the connection to KeyVault using the **Test Azure Key Vault** link.</span></span>
1. <span data-ttu-id="8a30d-129">Testaa yhteys Azure Data Lake Storageen käyttämällä **Testaa Azure-tallennustila** -linkin avulla.</span><span class="sxs-lookup"><span data-stu-id="8a30d-129">Test the connection to Azure Data Lake Storage using the **Test Azure Storage** link.</span></span>

> [!NOTE]
> <span data-ttu-id="8a30d-130">Jos testit epäonnistuvat, tarkista uudelleen, että kaikki edellä lisätyt KeyVault-tiedot ovat oikein. Kokeile sen jälkeen uudelleen.</span><span class="sxs-lookup"><span data-stu-id="8a30d-130">If the tests fail, double-check that all of the KeyVault information added above is correct, then try again.</span></span>

<span data-ttu-id="8a30d-131">Kun kaikki yhteystestit ovat onnistuneet, sinun on otettava yksikkötallennustilan automaattinen päivitys käyttöön.</span><span class="sxs-lookup"><span data-stu-id="8a30d-131">Once the connection tests are successful, you must enable automatic refresh for Entity store.</span></span>

<span data-ttu-id="8a30d-132">Ota yksikkötallennustilan päivitys käyttöön seuraavia vaiheita noudattamalla.</span><span class="sxs-lookup"><span data-stu-id="8a30d-132">To enable automatic refresh for Entity store, follow these steps.</span></span>

1. <span data-ttu-id="8a30d-133">Etsi kohdetta **Entiteettitallennustila**.</span><span class="sxs-lookup"><span data-stu-id="8a30d-133">Search for **Entity Store**.</span></span>
1. <span data-ttu-id="8a30d-134">Siirry vasemmalla olevassa luettelossa **RetailSales**-kirjaukseen ja valitse **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="8a30d-134">In the list on the left, navigate to the **RetailSales** entry, and select **Edit**.</span></span>
1. <span data-ttu-id="8a30d-135">Varmista, että **Automaattinen päivitys käytössä** -kohdan arvoksi on määritetty **Kyllä**, valitse **Päivitys** ja sitten **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="8a30d-135">Ensure that **Automatic Refresh Enabled** is set to **Yes**, select **Refresh**, and then select **Save**.</span></span>

<span data-ttu-id="8a30d-136">Seuraavassa kuvassa näkyy esimerkki yksikkösäilöstä, jossa automaattinen päivitys on käytössä.</span><span class="sxs-lookup"><span data-stu-id="8a30d-136">The following image shows an example of Entity store with automatic refresh enabled.</span></span>

![Esimerkki yksikkötallennustilasta, jossa automaattinen päivitys on käytössä](./media/exampleADLSConfig2.png)

<span data-ttu-id="8a30d-138">Azure Data Lake Storage on nyt määritetty ympäristölle.</span><span class="sxs-lookup"><span data-stu-id="8a30d-138">Azure Data Lake Storage is now configured for the environment.</span></span> 

<span data-ttu-id="8a30d-139">Jos et ole vielä suorittanut niitä, suorita ympäristön [tuotesuositusten ja mukautusten käyttöönoton](enable-product-recommendations.md) vaiheet.</span><span class="sxs-lookup"><span data-stu-id="8a30d-139">If not completed already, follow the steps for [enabling product recommendations and personalization](enable-product-recommendations.md) for the environment.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8a30d-140">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="8a30d-140">Additional resources</span></span>

[<span data-ttu-id="8a30d-141">Yksikkösäilön määrittäminen saataville Data Lake -säilönä</span><span class="sxs-lookup"><span data-stu-id="8a30d-141">Make entity store available as a data lake</span></span>](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md)

[<span data-ttu-id="8a30d-142">Tuotesuositusten yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="8a30d-142">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="8a30d-143">Tuotesuositusten ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="8a30d-143">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="8a30d-144">Kohdennettujen suositusten ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="8a30d-144">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="8a30d-145">Kohdennetuista tuotesuosituksista kieltäytyminen</span><span class="sxs-lookup"><span data-stu-id="8a30d-145">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="8a30d-146">"Osta samankaltaisia tyylejä" -suositusten käyttöönotto</span><span class="sxs-lookup"><span data-stu-id="8a30d-146">Enable "shop similar looks" recommendations</span></span>](shop-similar-looks.md)

[<span data-ttu-id="8a30d-147">Tuotesuositusten lisääminen myyntipisteessä</span><span class="sxs-lookup"><span data-stu-id="8a30d-147">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="8a30d-148">Suositusten lisääminen tapahtumanäyttöön</span><span class="sxs-lookup"><span data-stu-id="8a30d-148">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="8a30d-149">AI-ML-suositusten tulosten muokkaaminen</span><span class="sxs-lookup"><span data-stu-id="8a30d-149">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="8a30d-150">Kuratoitujen suositusten manuaalinen luominen</span><span class="sxs-lookup"><span data-stu-id="8a30d-150">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="8a30d-151">Suositusten luominen esittelytietojen avulla</span><span class="sxs-lookup"><span data-stu-id="8a30d-151">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="8a30d-152">Tuotesuositukset – usein kysytyt kysymykset</span><span class="sxs-lookup"><span data-stu-id="8a30d-152">Product recommendations FAQ</span></span>](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
