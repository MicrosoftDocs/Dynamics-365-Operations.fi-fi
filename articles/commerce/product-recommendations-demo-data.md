---
title: Suositusten luominen esittelytietojen avulla
description: Tämä aihe antaa ohjeita monikanavan tuotesuositusten käyttämiseen tason 1 yhden ruudun ympäristöissä käyttämällä valmiiksi täytettyjä ja mukautettavia esittelytietoja.
author: bebeale
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: RetailStoreTable, RetailTillLayout
audience: Application User
ms.reviewer: josaw
ms.custom: 260624
ms.assetid: a4f9d315-9951-451c-8ee6-37f9b3b15ef0
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 7ccb0b6c5aace0fc76c6886299fba7369abed860
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4972360"
---
# <a name="create-recommendations-with-demo-data"></a><span data-ttu-id="39afa-103">Suositusten luominen esittelytietojen avulla</span><span class="sxs-lookup"><span data-stu-id="39afa-103">Create recommendations with demo data</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="39afa-104">Tämä aihe antaa ohjeita monikanavan tuotesuositusten käyttämiseen tason 1 yhden ruudun ympäristöissä käyttämällä valmiiksi täytettyjä ja mukautettavia esittelytietoja.</span><span class="sxs-lookup"><span data-stu-id="39afa-104">This topic provides guidance on how to leverage omni-channel product recommendations in Tier-1 single box environments using pre-populated, customizable demo data.</span></span>

<span data-ttu-id="39afa-105">Monikanavan tuotesuositukset tarjoavat joukon manuaalisesti koottuja tai ohjelmallisesti luotuja tuoteluetteloita.</span><span class="sxs-lookup"><span data-stu-id="39afa-105">Omni-channel product recommendations provide a set of editorially curated or programmatically generated list of products.</span></span> <span data-ttu-id="39afa-106">Näitä luetteloita voidaan käyttää useissa skenaarioissa liiketoimintatarpeiden mukaan.</span><span class="sxs-lookup"><span data-stu-id="39afa-106">These lists can be used in several scenarios, depending on the business need.</span></span> <span data-ttu-id="39afa-107">Lisätietoja tuotesuositusten luetteloista on kohdassa [Tuotesuositusten yleiskatsaus](product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="39afa-107">For more information about product recommendation lists, see [Product recommendations overview](product-recommendations.md).</span></span>

<span data-ttu-id="39afa-108">Tason 2 ja sitä korkeampien Dynamics 365 -ympäristöjen tuotesuositukset lasketaan automaattisesti asiakastietojen perusteella.</span><span class="sxs-lookup"><span data-stu-id="39afa-108">For Tier-2 and higher Dynamics 365 environments, product recommendations are automatically computed based on customer data.</span></span> <span data-ttu-id="39afa-109">Tuotesuositusten demotietojen käyttäminen ei poista käytöstä mitään ympäristöön lisättyä tuotesuositusten ratkaisua tai mitään sen käyttöön liittyviä kustannuksia.</span><span class="sxs-lookup"><span data-stu-id="39afa-109">Using product recommendations demo data does not disable any product recommendations solution already provisioned in the environment and any costs associated with its usage.</span></span>

<span data-ttu-id="39afa-110">Tason 1 ympäristöjen tuotesuositukset perustuvat vain .csv-tiedoston sisältämiin staattisiin esittelytietoihin.</span><span class="sxs-lookup"><span data-stu-id="39afa-110">For Tier-1 environments, product recommendations are based only off the static demo data stored in a .csv file.</span></span>

## <a name="enabling-product-recommendations-demo-data-in-an-environment"></a><span data-ttu-id="39afa-111">Tuotesuositusten demotietojen ottaminen käyttöön ympäristössä</span><span class="sxs-lookup"><span data-stu-id="39afa-111">Enabling product recommendations demo data in an environment</span></span>
<span data-ttu-id="39afa-112">Jos haluat ottaa käyttöön tuotesuositusten esittelypäivämäärän, sinun on otettava käyttöön Dynamics 365 Commerce -esikatselun esittelylaajennus kyseisessä ympäristössä.</span><span class="sxs-lookup"><span data-stu-id="39afa-112">To enable product recommendations demo date, you need to deploy the Dynamics 365 Commerce Preview Demo Extension to the respective environment.</span></span> <span data-ttu-id="39afa-113">Kun näin tehdään, tuotesuositusten esittelytiedot otetaan automaattisesti käyttöön.</span><span class="sxs-lookup"><span data-stu-id="39afa-113">Doing so automatically enables product recommendations demo data.</span></span>

## <a name="default-demo-data"></a><span data-ttu-id="39afa-114">Oletusarvoiset demotiedot</span><span class="sxs-lookup"><span data-stu-id="39afa-114">Default demo data</span></span>
<span data-ttu-id="39afa-115">Jokaisessa Onebox-tyyppisessä ympäristössä on valmiita tuotesuositusten demotietoja. Ne on tallennettu pilkuilla erotettuun reco_demo_data.csv-tiedostoon, joka sijaitsee samassa kansiossa kuin tämä asiakirja Commerce Scale Unitissa.</span><span class="sxs-lookup"><span data-stu-id="39afa-115">Each OneBox type environment comes with a preloaded set of product recommendations demo data stored in the coma separated 'reco_demo_data.csv' file, located on the Commerce Scale Unit.</span></span>

<span data-ttu-id="39afa-116">Tiedot on järjestetty seuraaviin sarakkeisiin.</span><span class="sxs-lookup"><span data-stu-id="39afa-116">The data is structured along the following columns.</span></span>

| <span data-ttu-id="39afa-117">Sarakkeen nimi</span><span class="sxs-lookup"><span data-stu-id="39afa-117">Column name</span></span>         | <span data-ttu-id="39afa-118">Pakollinen</span><span class="sxs-lookup"><span data-stu-id="39afa-118">Mandatory</span></span>          | <span data-ttu-id="39afa-119">kuvaus</span><span class="sxs-lookup"><span data-stu-id="39afa-119">Description</span></span>                                                                                                                                 | <span data-ttu-id="39afa-120">Mahdolliset arvot</span><span class="sxs-lookup"><span data-stu-id="39afa-120">Possible values</span></span>                                                              |
|---------------------|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="39afa-121">RecoList</span><span class="sxs-lookup"><span data-stu-id="39afa-121">RecoList</span></span>            | :heavy_check_mark: | <span data-ttu-id="39afa-123">Tuotesuosituksen tietty luettelotyyppi, jonka esittelytietojen piste luo.</span><span class="sxs-lookup"><span data-stu-id="39afa-123">The specific product recommendation list type that the demo data point is to generate.</span></span>                                                    | <ul><li><span data-ttu-id="39afa-124">RecoBestSelling</span><span class="sxs-lookup"><span data-stu-id="39afa-124">RecoBestSelling</span></span></li><li><span data-ttu-id="39afa-125">RecoNew</span><span class="sxs-lookup"><span data-stu-id="39afa-125">RecoNew</span></span></li><li><span data-ttu-id="39afa-126">RecoTrending</span><span class="sxs-lookup"><span data-stu-id="39afa-126">RecoTrending</span></span></li><li><span data-ttu-id="39afa-127">RecoCart</span><span class="sxs-lookup"><span data-stu-id="39afa-127">RecoCart</span></span></li><li><span data-ttu-id="39afa-128">RecoPeopleAlsoBuy</span><span class="sxs-lookup"><span data-stu-id="39afa-128">RecoPeopleAlsoBuy</span></span></li></ul> |
| <span data-ttu-id="39afa-129">OperatingUnitNumber</span><span class="sxs-lookup"><span data-stu-id="39afa-129">OperatingUnitNumber</span></span> | :heavy_check_mark: | <span data-ttu-id="39afa-131">Tietty toimintayksikön numero, jossa tuotesuositusten odotetaan näkyvän.</span><span class="sxs-lookup"><span data-stu-id="39afa-131">The specific operating unit number where product recommendations are expected to be   surfaced.</span></span>                                        |                                                                              |
| <span data-ttu-id="39afa-132">Luokka</span><span class="sxs-lookup"><span data-stu-id="39afa-132">Category</span></span>            |                    |    <span data-ttu-id="39afa-133">Luokka, jolle määritetty luettelo tulisi palauttaa.</span><span class="sxs-lookup"><span data-stu-id="39afa-133">The category the specific list should be returned for.</span></span> <span data-ttu-id="39afa-134">Jos luokkaa ei ole määritetty, luettelo koskee vain siirtymishierarkian ylätasoa.</span><span class="sxs-lookup"><span data-stu-id="39afa-134">If no category is specified, the list is for top of navigation hierarchy only.</span></span>    |                                                                              |
| <span data-ttu-id="39afa-135">SeedItemId</span><span class="sxs-lookup"><span data-stu-id="39afa-135">SeedItemId</span></span>          |                    |    <span data-ttu-id="39afa-136">Jos luettelo edellyttää alkuarvoa (RecoPeopleAlsoBuy ja RecoCart), tuote, jolle näiden luetteloiden tulisi näyttää lisätuotteita.</span><span class="sxs-lookup"><span data-stu-id="39afa-136">For lists that require seed (RecoPeopleAlsoBuy and RecoCart), the product those lists should show additional products for.</span></span>            |                                                                              |
| <span data-ttu-id="39afa-137">Asiakastunnus</span><span class="sxs-lookup"><span data-stu-id="39afa-137">CustomerId</span></span>          |                    |    <span data-ttu-id="39afa-138">Luettelo, joka edellyttää asiakastunnusta (RecoPicks).</span><span class="sxs-lookup"><span data-stu-id="39afa-138">For lists that require a customer identifier (RecoPicks).</span></span>  <span data-ttu-id="39afa-139">Oletusarvo 0 koskee kaikkia asiakkaita.</span><span class="sxs-lookup"><span data-stu-id="39afa-139">The default value '0' applies to all customers.</span></span>          |                                                                              |
| <span data-ttu-id="39afa-140">ItemIds</span><span class="sxs-lookup"><span data-stu-id="39afa-140">ItemIds</span></span>             | :heavy_check_mark: | <span data-ttu-id="39afa-142">Yksi tai useampi tuloksena palautettava tuote, erotettu toisistaan ‘;’-merkillä.</span><span class="sxs-lookup"><span data-stu-id="39afa-142">One or more products to be returned as the result, separated by ';'.</span></span>                                                                  |                                                                              |

## <a name="customize-demo-data"></a><span data-ttu-id="39afa-143">Mukauta demotietoja</span><span class="sxs-lookup"><span data-stu-id="39afa-143">Customize demo data</span></span>
<span data-ttu-id="39afa-144">Voit muokata oletusarvoisia esittelytietoja HQ:ssa määritettyjen tuote- ja luokkatietojen avulla.</span><span class="sxs-lookup"><span data-stu-id="39afa-144">You can edit the default demo data with any product and category information configured in HQ.</span></span> <span data-ttu-id="39afa-145">Sen jälkeen, kun .csv on päivitetty, asiakkaille palautetut tuotesuositukset päivitetään heti muutosten mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="39afa-145">After you update the .csv, the product recommendations that are returned to customers will immediately reflect the changes.</span></span>

<span data-ttu-id="39afa-146">Laajennus sisältää datatiedoston nimeltään RecoMockDataset.csv. Sen avulla asiakas voi hallita tietojoukkoa, jota käytetään suositusten esimerkkitulosten luomiseen.</span><span class="sxs-lookup"><span data-stu-id="39afa-146">The extension contains a datafile called 'RecoMockDataset.csv', which allows you to control the dataset used to power the mock recommendations results.</span></span> <span data-ttu-id="39afa-147">Tiedoston nimeä voidaan hallita laajennuksen kokoonpanon kautta käyttämällä **ext.Recommendations.DemoFilePath**-asetusta.</span><span class="sxs-lookup"><span data-stu-id="39afa-147">The file name can be controlled through extension configuration using the **ext.Recommendations.DemoFilePath** setting.</span></span> <span data-ttu-id="39afa-148">Näin käytettävissä voi olla useita tietojoukkoja, joita voidaan vaihtaa helposti kokoonpanon kautta.</span><span class="sxs-lookup"><span data-stu-id="39afa-148">This enables you to have multiple datasets available that can be switched between easily through configuration.</span></span>


```xml
<settings>
    <add name="ext.Recommendations.DemoFilePath" value="RecoMockDataset.csv" />
</settings>
```

## <a name="additional-resources"></a><span data-ttu-id="39afa-149">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="39afa-149">Additional resources</span></span>

[<span data-ttu-id="39afa-150">Tuotesuositusten yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="39afa-150">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="39afa-151">Azure Data Lake Storagen käyttöönotto Dynamics 365 Commerce -ympäristössä</span><span class="sxs-lookup"><span data-stu-id="39afa-151">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="39afa-152">Tuotesuositusten ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="39afa-152">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="39afa-153">Kohdennettujen suositusten ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="39afa-153">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="39afa-154">Kohdennetuista tuotesuosituksista kieltäytyminen</span><span class="sxs-lookup"><span data-stu-id="39afa-154">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="39afa-155">"Osta samankaltaisia tyylejä" -suositusten käyttöönotto</span><span class="sxs-lookup"><span data-stu-id="39afa-155">Enable "shop similar looks" recommendations</span></span>](shop-similar-looks.md)

[<span data-ttu-id="39afa-156">Tuotesuositusten lisääminen myyntipisteessä</span><span class="sxs-lookup"><span data-stu-id="39afa-156">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="39afa-157">Suositusten lisääminen tapahtumanäyttöön</span><span class="sxs-lookup"><span data-stu-id="39afa-157">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="39afa-158">AI-ML-suositusten tulosten muokkaaminen</span><span class="sxs-lookup"><span data-stu-id="39afa-158">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="39afa-159">Kuratoitujen suositusten manuaalinen luominen</span><span class="sxs-lookup"><span data-stu-id="39afa-159">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="39afa-160">Tuotesuositukset – usein kysytyt kysymykset</span><span class="sxs-lookup"><span data-stu-id="39afa-160">Product recommendations FAQ</span></span>](faq-recommendations.md)
