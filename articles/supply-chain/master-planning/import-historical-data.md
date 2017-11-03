---
title: "Kysynnän ennusteiden historiallisten tietojen tuominen"
description: "Jos haluat hakea tarkat kysynnän ennusteet, pyydä historialliset kysyntätiedot nimikettä tai nimikkeen kohdistustunnusta kohti. Tässä aiheessa kerrotaan, miten tietojen entiteettejä käytetään historiallisten kysyntätietojen tuomisessa mistä tahansa järjestelmästä niin, että kysynnän ennusteen tietoja on pidemmältä ajalta."
author: roxanadiaconu
manager: AnnBe
ms.date: 05/10/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.assetid: 59c0d269-9db0-48e7-b8c7-9a388781a9ca
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 02daa312d74311432c0c468e3e691637dcf94157
ms.contentlocale: fi-fi
ms.lasthandoff: 11/03/2017

---

# <a name="import-historical-data-for-demand-forecasts"></a><span data-ttu-id="2f79c-104">Kysynnän ennusteiden historiallisten tietojen tuominen</span><span class="sxs-lookup"><span data-stu-id="2f79c-104">Import historical data for demand forecasts</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="2f79c-105">Ennusteiden tarkkuuden varmistamiseksi historiallisia kysyntätietoja tulee olla niin paljon kuin niitä saadaan nimikettä tai nimikkeen kohdistustunnusta kohti.</span><span class="sxs-lookup"><span data-stu-id="2f79c-105">To help guarantee the accuracy of demand forecasts, you must have as much historical demand data as you can get per item or item allocation key.</span></span> <span data-ttu-id="2f79c-106">Jos historiallisia kysyntätietoja ei ole vielä tuotu, tuo ne Microsoft Dynamics 365 for Finance and Operationsin tietoyksikön **Historiallinen ulkoinen kysyntä** (ReqDemPlanHistoricalExternalDemandEntity) avulla.</span><span class="sxs-lookup"><span data-stu-id="2f79c-106">If the historical demand data isn't already imported, use the **Historical external demand** (ReqDemPlanHistoricalExternalDemandEntity) data entity in Microsoft Dynamics 365 for Finance and Operations to import it.</span></span>

<span data-ttu-id="2f79c-107">**Tietojen hallinta** -työtila sisältää yksikön kaikkien kenttien yleiskatsauksen.</span><span class="sxs-lookup"><span data-stu-id="2f79c-107">In the **Data management** workspace, you can see an overview of all the fields in the entity.</span></span>

1. <span data-ttu-id="2f79c-108">Avaa **Tietojen hallinta** -työtila.</span><span class="sxs-lookup"><span data-stu-id="2f79c-108">Open the **Data management** workspace.</span></span>
2. <span data-ttu-id="2f79c-109">Valitse **Tietoyksiköt**-ruutu.</span><span class="sxs-lookup"><span data-stu-id="2f79c-109">Click the **Data entities** tile.</span></span>
3. <span data-ttu-id="2f79c-110">Suorita haku **Historiallinen ulkoinen kysyntä** -kohdan yksikköluettelosta.</span><span class="sxs-lookup"><span data-stu-id="2f79c-110">Search the entity list for **Historical external demand**.</span></span>
4. <span data-ttu-id="2f79c-111">Valitse **Kohdekentät**.</span><span class="sxs-lookup"><span data-stu-id="2f79c-111">Click **Target fields**.</span></span> <span data-ttu-id="2f79c-112">Seuraavat yksikkökentät ovat pakollisia: sivusto (**DeliveringSiteId**), päivämäärä (**DemandDate**), määrä (**DemandQuantity**) ja joko nimikenumero (**ItemNumber**) tai nimikkeen kohdistustunnus (**ProductAllocationKeyId**).</span><span class="sxs-lookup"><span data-stu-id="2f79c-112">The following entity fields are mandatory: site (**DeliveringSiteId**), date (**DemandDate**), quantity (**DemandQuantity**), and either item number (**ItemNumber**) or item allocation key (**ProductAllocationKeyId**).</span></span>

<span data-ttu-id="2f79c-113">Voit käyttää tietoyksikköä, kun käytössä on historialliset kysyntätiedot sisältävä Microsoft Excel -tiedosto tai CSV-tiedosto (pilkulla erotettujen arvojen tiedosto).</span><span class="sxs-lookup"><span data-stu-id="2f79c-113">To use the data entity, you must have a Microsoft Excel file or comma-separated values (CSV) file that contains the historical demand data.</span></span> <span data-ttu-id="2f79c-114">Seuraavassa esimerkissä näytetään, miten tiedot tuodaan CSV-tiedostosta.</span><span class="sxs-lookup"><span data-stu-id="2f79c-114">The following example shows how to import the data from a CSV file.</span></span>

## <a name="example"></a><span data-ttu-id="2f79c-115">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="2f79c-115">Example</span></span>

<span data-ttu-id="2f79c-116">Voit käyttää esimerkkinä seuraavaa tiedostoa.</span><span class="sxs-lookup"><span data-stu-id="2f79c-116">You can use the following file as an example.</span></span> <span data-ttu-id="2f79c-117">Lataa [HistoricalDemandData](https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/how-to-articles/365OperationsDemandForecast).</span><span class="sxs-lookup"><span data-stu-id="2f79c-117">Download the [HistoricalDemandData](https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/how-to-articles/365OperationsDemandForecast).</span></span> <span data-ttu-id="2f79c-118">Tämä tiedosto sisältää nimikkeen D0001 historialliset kysyntätiedot.</span><span class="sxs-lookup"><span data-stu-id="2f79c-118">This file contains the historical demand data for item D0001.</span></span> <span data-ttu-id="2f79c-119">Se sisältää vain seuraavat pakolliset kentät: sivusto, määrä ja kysynnän päivämäärä.</span><span class="sxs-lookup"><span data-stu-id="2f79c-119">It contains only the following mandatory fields: site, quantity, and the demand date.</span></span>

1. <span data-ttu-id="2f79c-120">Valitse yritys, johon historialliset kysyntätiedot tuodaan.</span><span class="sxs-lookup"><span data-stu-id="2f79c-120">Select the company to import the historical demand data into.</span></span>
2. <span data-ttu-id="2f79c-121">Avaa **Tietojen hallinta** -työtila.</span><span class="sxs-lookup"><span data-stu-id="2f79c-121">Open the **Data management** workspace.</span></span>
3. <span data-ttu-id="2f79c-122">Valitse **Tuo**-ruutu.</span><span class="sxs-lookup"><span data-stu-id="2f79c-122">Click the **Import** tile.</span></span>
4. <span data-ttu-id="2f79c-123">Syötä tuontiprojektin nimi, kuten **Nimikkeen D0001 historiallisen kysynnän tuominen**.</span><span class="sxs-lookup"><span data-stu-id="2f79c-123">Enter a name for the import project, such as **Import historical demand for item D0001**.</span></span>
5. <span data-ttu-id="2f79c-124">Valitse **Lähdetietojen muoto** -kenttään tuotavan tiedoston muoto.</span><span class="sxs-lookup"><span data-stu-id="2f79c-124">In the **Source data format** field, select the file format of the file that you're importing.</span></span> <span data-ttu-id="2f79c-125">Voit tuoda tämän esimerkin HistoricalDemandData-tiedoston valitsemalla **CSV**.</span><span class="sxs-lookup"><span data-stu-id="2f79c-125">To import the HistoricalDemandData file for this example, select **CSV**.</span></span>
6. <span data-ttu-id="2f79c-126">Valitse **Yksikön nimi** -kenttään **Historiallinen ulkoinen kysyntä**.</span><span class="sxs-lookup"><span data-stu-id="2f79c-126">In the **Entity name** field, select **Historical external demand**.</span></span>
7. <span data-ttu-id="2f79c-127">Tallenna tiedosto tietokoneeseen ja lataa se.</span><span class="sxs-lookup"><span data-stu-id="2f79c-127">Save the file to your computer, and then upload it.</span></span>
8. <span data-ttu-id="2f79c-128">Valitse **Tuo**.</span><span class="sxs-lookup"><span data-stu-id="2f79c-128">Click **Import**.</span></span>
9. <span data-ttu-id="2f79c-129">**Suorituksen yhteenveto** -sivu avautuu automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="2f79c-129">The **Execution summary** page is opened automatically.</span></span> <span data-ttu-id="2f79c-130">Tarkista sivun tuodut tiedot.</span><span class="sxs-lookup"><span data-stu-id="2f79c-130">Verify the imported data on the page.</span></span>

<span data-ttu-id="2f79c-131">Kun historialliset kysyntätiedot on tuotu, voit luoda kysynnän ennusteen.</span><span class="sxs-lookup"><span data-stu-id="2f79c-131">After you've imported the historical demand data, you can generate a demand forecast.</span></span>

## <a name="see-also"></a><span data-ttu-id="2f79c-132">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="2f79c-132">See also</span></span>

[<span data-ttu-id="2f79c-133">Tilastollisen perusennusteen luominen</span><span class="sxs-lookup"><span data-stu-id="2f79c-133">Generate a statistical baseline forecast</span></span>](generate-statistical-baseline-forecast.md)

