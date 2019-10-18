---
title: Omni-Channel-tuotesuositusten demotiedot
description: Tämän asiakirjan tarkoituksena on antaa ohjeita Omni-Channel-tuotesuositusten käyttämiseen tason 1 yhden ruudun ympäristöissä käyttämällä valmiiksi täytettyjä ja mukautettavia demotietoja.
author: bebeale
manager: AnnBe
ms.date: 10/1/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
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
ms.search.validFrom: 2019-07-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 81af4c1bb7828c9b346a3ef514d8657e853dcefb
ms.sourcegitcommit: c526cfd1f823df1ff33ded95e599a72f0a15cc5a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/27/2019
ms.locfileid: "2225863"
---
# <a name="omni-channel-product-recommendations-demo-data"></a><span data-ttu-id="b6db6-103">Omni-Channel-tuotesuositusten demotiedot</span><span class="sxs-lookup"><span data-stu-id="b6db6-103">Omni-channel product recommendations demo data</span></span>

<span data-ttu-id="b6db6-104">Tämän asiakirjan tarkoituksena on antaa ohjeita Omni-Channel-tuotesuositusten käyttämiseen tason 1 yhden ruudun ympäristöissä käyttämällä valmiiksi täytettyjä ja mukautettavia demotietoja.</span><span class="sxs-lookup"><span data-stu-id="b6db6-104">This document aims to provide guidance on how to leverage omni-channel product recommendations in Tier-1 single box environments using pre-populated, customizable demo data.</span></span>

<span data-ttu-id="b6db6-105">Omni-Channel-tuotesuositukset tarjoavat joukon manuaalisesti koottuja tai ohjelmallisesti luotuja tuoteluetteloita järjestyksessä.</span><span class="sxs-lookup"><span data-stu-id="b6db6-105">Omni-channel product recommendations provide a set of editorially curated or programmatically generated ordered list of products.</span></span> <span data-ttu-id="b6db6-106">Näitä luetteloita voidaan käyttää useissa skenaarioissa liiketoimintatarpeiden mukaan.</span><span class="sxs-lookup"><span data-stu-id="b6db6-106">These lists can be used in several scenarios, depending on the business need.</span></span> <span data-ttu-id="b6db6-107">Lisätietoja tuotesuositusten luetteloista on kohdassa [Tuotesuositusten yleiskatsaus](product-recommendaitons-overview.md).</span><span class="sxs-lookup"><span data-stu-id="b6db6-107">For more information about product recommendation lists, see [Product recommendations overview.](product-recommendaitons-overview.md)</span></span>

<span data-ttu-id="b6db6-108">Tason 2 ja sitä korkeampien Dynamics-ympäristöjen tuotesuositukset lasketaan automaattisesti asiakastietojen perusteella.</span><span class="sxs-lookup"><span data-stu-id="b6db6-108">For Tier-2 and higher Dynamics Environments product recommendations are automatically computed based on customer data.</span></span>
<span data-ttu-id="b6db6-109">Tuotesuositusten demotietojen käyttäminen ei poista käytöstä mitään ympäristöön lisättyä tuotesuositusten ratkaisua tai mitään sen käyttöön liittyviä kustannuksia.</span><span class="sxs-lookup"><span data-stu-id="b6db6-109">Using product recommendations demo data does not disable any product recommendations solution already provisioned in the environment and any costs associated with its usage.</span></span>

<span data-ttu-id="b6db6-110">Tason 1 ympäristöjen tuotesuositukset perustuvat vain CSV-tiedoston sisältämiin staattisiin demotietoihin.</span><span class="sxs-lookup"><span data-stu-id="b6db6-110">For Tier-1 environments product recommendations are based only off the static demo data stored in a csv file.</span></span>

## <a name="enabling-product-recommendations-demo-data-in-an-environment"></a><span data-ttu-id="b6db6-111">Tuotesuositusten demotietojen ottaminen käyttöön ympäristössä</span><span class="sxs-lookup"><span data-stu-id="b6db6-111">Enabling product recommendations demo data in an environment</span></span>

<span data-ttu-id="b6db6-112">Asiakkaiden on otettava käyttöön **Dynamics 365 Commerce -esikatselun demo-laajennus** kyseisessä ympäristössä, mikä ottaa tuotesuositusten demotiedot automaattisesti käyttöön.</span><span class="sxs-lookup"><span data-stu-id="b6db6-112">Customers need to deploy the **Dynamics 365 Commerce Preview Demo Extension** to the respective environment, which automatically enables product recommendations demo data.</span></span>

## <a name="default-demo-data"></a><span data-ttu-id="b6db6-113">Oletusarvoiset demotiedot</span><span class="sxs-lookup"><span data-stu-id="b6db6-113">Default demo data</span></span>
<span data-ttu-id="b6db6-114">Jokaisessa Onebox-tyyppisessä ympäristössä on valmiita tuotesuositusten demotietoja. Ne on tallennettu pilkuilla erotettuun **reco_demo_data.csv**-tiedostoon, joka sijaitsee samassa kansiossa kuin tämä asiakirja Retail Serverissä.</span><span class="sxs-lookup"><span data-stu-id="b6db6-114">Each Onebox type environment comes with a preloaded set of product recommendations demo data stored in the coma separated **‘reco_demo_data.csv’** file, located in the same folder as this document on Retail Server.</span></span>

<span data-ttu-id="b6db6-115">Nämä tiedot on järjestetty seuraaviin sarakkeisiin.</span><span class="sxs-lookup"><span data-stu-id="b6db6-115">This data is structured along the following columns</span></span>

| <span data-ttu-id="b6db6-116">Sarakkeen nimi</span><span class="sxs-lookup"><span data-stu-id="b6db6-116">Column name</span></span>         | <span data-ttu-id="b6db6-117">Pakollinen</span><span class="sxs-lookup"><span data-stu-id="b6db6-117">Mandatory</span></span>          | <span data-ttu-id="b6db6-118">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="b6db6-118">Description</span></span>                                                                                                                                 | <span data-ttu-id="b6db6-119">Mahdolliset arvot</span><span class="sxs-lookup"><span data-stu-id="b6db6-119">Possible Values</span></span>                                                              |
|---------------------|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="b6db6-120">RecoList</span><span class="sxs-lookup"><span data-stu-id="b6db6-120">RecoList</span></span>            | :heavy_check_mark: | <span data-ttu-id="b6db6-122">Tuotesuosituksen tietty luettelotyyppi, jonka demotietojen piste luo.</span><span class="sxs-lookup"><span data-stu-id="b6db6-122">The specific product   recommendation list type that the demo data point is to generate.</span></span>                                                    | <ul><li><span data-ttu-id="b6db6-123">RecoBestSelling</span><span class="sxs-lookup"><span data-stu-id="b6db6-123">RecoBestSelling</span></span></li><li><span data-ttu-id="b6db6-124">RecoNew</span><span class="sxs-lookup"><span data-stu-id="b6db6-124">RecoNew</span></span></li><li><span data-ttu-id="b6db6-125">RecoTrending</span><span class="sxs-lookup"><span data-stu-id="b6db6-125">RecoTrending</span></span></li><li><span data-ttu-id="b6db6-126">RecoCart</span><span class="sxs-lookup"><span data-stu-id="b6db6-126">RecoCart</span></span></li><li><span data-ttu-id="b6db6-127">RecoPeopleAlsoBuy</span><span class="sxs-lookup"><span data-stu-id="b6db6-127">RecoPeopleAlsoBuy</span></span></li></ul> |
| <span data-ttu-id="b6db6-128">OperatingUnitNumber</span><span class="sxs-lookup"><span data-stu-id="b6db6-128">OperatingUnitNumber</span></span> | :heavy_check_mark: | <span data-ttu-id="b6db6-130">Tietty toimintayksikön numero, jossa tuotesuositusten odotetaan näkyvän.</span><span class="sxs-lookup"><span data-stu-id="b6db6-130">The specific   operating unit number where product recommendations are expected to be   surfaced in.</span></span>                                        |                                                                              |
| <span data-ttu-id="b6db6-131">Luokka</span><span class="sxs-lookup"><span data-stu-id="b6db6-131">Category</span></span>            |                    |    <span data-ttu-id="b6db6-132">Luokka, jolle määritetty luettelo tulisi palauttaa.</span><span class="sxs-lookup"><span data-stu-id="b6db6-132">The category the   specific list should be returned for.</span></span> <span data-ttu-id="b6db6-133">Jos luokkaa ei ole määritetty, luettelo koskee vain siirtymishierarkian ylätasoa.</span><span class="sxs-lookup"><span data-stu-id="b6db6-133">If no category is specified, list is   for top of navigation hierarchy only.</span></span>    |                                                                              |
| <span data-ttu-id="b6db6-134">SeedItemId</span><span class="sxs-lookup"><span data-stu-id="b6db6-134">SeedItemId</span></span>          |                    |    <span data-ttu-id="b6db6-135">Jos luettelo edellyttää alkuarvoa (RecoPeopleAlsoBuy ja RecoCart), tuote, jolle näiden luetteloiden tulisi näyttää lisätuotteita.</span><span class="sxs-lookup"><span data-stu-id="b6db6-135">For lists that   require seed (RecoPeopleAlsoBuy and RecoCart) the product those lists should   show additional products for.</span></span>            |                                                                              |
| <span data-ttu-id="b6db6-136">ItemIds</span><span class="sxs-lookup"><span data-stu-id="b6db6-136">ItemIds</span></span>             | :heavy_check_mark: | <span data-ttu-id="b6db6-138">Yksi tai useampi tuloksena palautettava tuote, erotettu toisistaan **‘;’**-merkillä.</span><span class="sxs-lookup"><span data-stu-id="b6db6-138">One or more products   to be returned as the result, separated by **‘;’**.</span></span>                                                                  |                                                                              |


## <a name="customize-demo-data"></a><span data-ttu-id="b6db6-139">Mukauta demotietoja</span><span class="sxs-lookup"><span data-stu-id="b6db6-139">Customize demo data</span></span>
<span data-ttu-id="b6db6-140">Asiakkaat voivat muokata oletusarvoisia demotietoja HQ:ssa määritettyjen tuote- ja luokkatietojen avulla.</span><span class="sxs-lookup"><span data-stu-id="b6db6-140">Customers can edit the default demo data with any product and category information that is configured in HQ.</span></span> <span data-ttu-id="b6db6-141">Kun CSV on päivitetty, asiakkaille palautetut tuotesuositukset päivitetään heti muutosten mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="b6db6-141">Once the CSV is updated, the Product Recommendations returned to customers will immediately reflect the changes.</span></span>

<span data-ttu-id="b6db6-142">Laajennus sisältää datatiedoston nimeltään RecoMockDataset.csv. Sen avulla asiakas voi hallita tietojoukkoa, jota käytetään suositusten esimerkkitulosten luomiseen.</span><span class="sxs-lookup"><span data-stu-id="b6db6-142">The extension contains a datafile called RecoMockDataset.csv which allows the customer to control the dataset used to power the mock recommendations results.</span></span> <span data-ttu-id="b6db6-143">Tiedoston nimeä voidaan hallita laajennuksen kokoonpanon kautta käyttämällä **ext.Recommendations.DemoFilePath**-asetusta.</span><span class="sxs-lookup"><span data-stu-id="b6db6-143">The file name can be controlled through extension configuration using the **ext.Recommendations.DemoFilePath** setting.</span></span> <span data-ttu-id="b6db6-144">Näin asiakkaalla voi olla käytettävissä useita tietojoukkoja, joita voidaan vaihtaa helposti kokoonpanon kautta.</span><span class="sxs-lookup"><span data-stu-id="b6db6-144">This enables the customers to have multiple datasets available that can be switched between easily through configuration.</span></span>

```
  <settings>
    <add name="ext.Recommendations.DemoFilePath" value="RecoMockDataset.csv" />
  </settings>
```

## <a name="additional-resources"></a><span data-ttu-id="b6db6-145">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="b6db6-145">Additional resources</span></span>

[<span data-ttu-id="b6db6-146">Tuotesuositusten yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="b6db6-146">Product recommendations overview</span></span>](product-recommendations-overview.md)

[<span data-ttu-id="b6db6-147">Työympäristön suunnittelu</span><span class="sxs-lookup"><span data-stu-id="b6db6-147">Environment planning</span></span>](environment-planning.md)
