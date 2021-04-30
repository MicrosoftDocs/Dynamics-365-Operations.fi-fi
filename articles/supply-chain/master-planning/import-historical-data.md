---
title: Kysynnän ennusteiden historiallisten tietojen tuominen
description: Jos haluat hakea tarkat kysynnän ennusteet, pyydä historialliset kysyntätiedot nimikettä tai nimikkeen kohdistustunnusta kohti. Tässä aiheessa kerrotaan, miten tietojen entiteettejä käytetään historiallisten kysyntätietojen tuomisessa mistä tahansa järjestelmästä niin, että kysynnän ennusteen tietoja on pidemmältä ajalta.
author: roxanadiaconu
ms.date: 05/10/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqDemPlanCreateForecastDialog
audience: Application User
ms.reviewer: kamaybac
ms.assetid: 59c0d269-9db0-48e7-b8c7-9a388781a9ca
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: de380113fe951f75c15f9e5526ad2f1f5cc84334
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/16/2021
ms.locfileid: "5908877"
---
# <a name="import-historical-data-for-demand-forecasts"></a><span data-ttu-id="e6654-104">Kysynnän ennusteiden historiallisten tietojen tuominen</span><span class="sxs-lookup"><span data-stu-id="e6654-104">Import historical data for demand forecasts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e6654-105">Ennusteiden tarkkuuden varmistamiseksi historiallisia kysyntätietoja tulee olla niin paljon kuin niitä saadaan nimikettä tai nimikkeen kohdistustunnusta kohti.</span><span class="sxs-lookup"><span data-stu-id="e6654-105">To help guarantee the accuracy of demand forecasts, you must have as much historical demand data as you can get per item or item allocation key.</span></span> <span data-ttu-id="e6654-106">Jos historiallisia kysyntätietoja ei ole vielä tuotu, tuo ne Dynamics 365 Supply Chain Managementin **Historiallinen ulkoinen kysyntä** (ReqDemPlanHistoricalExternalDemandEntity) -tietoyksikön avulla.</span><span class="sxs-lookup"><span data-stu-id="e6654-106">If the historical demand data isn't already imported, use the **Historical external demand** (ReqDemPlanHistoricalExternalDemandEntity) data entity in Dynamics 365 Supply Chain Management to import it.</span></span>

<span data-ttu-id="e6654-107">**Tietojen hallinta** -työtila sisältää yksikön kaikkien kenttien yleiskatsauksen.</span><span class="sxs-lookup"><span data-stu-id="e6654-107">In the **Data management** workspace, you can see an overview of all the fields in the entity.</span></span>

1. <span data-ttu-id="e6654-108">Avaa **Tietojen hallinta** -työtila.</span><span class="sxs-lookup"><span data-stu-id="e6654-108">Open the **Data management** workspace.</span></span>
2. <span data-ttu-id="e6654-109">Valitse **Tietoyksiköt**-ruutu.</span><span class="sxs-lookup"><span data-stu-id="e6654-109">Select the **Data entities** tile.</span></span>
3. <span data-ttu-id="e6654-110">Suorita haku **Historiallinen ulkoinen kysyntä** -kohdan yksikköluettelosta.</span><span class="sxs-lookup"><span data-stu-id="e6654-110">Search the entity list for **Historical external demand**.</span></span>
4. <span data-ttu-id="e6654-111">Valitse **Kohdekentät**.</span><span class="sxs-lookup"><span data-stu-id="e6654-111">Select **Target fields**.</span></span> <span data-ttu-id="e6654-112">Seuraavat yksikkökentät ovat pakollisia: sivusto (**DeliveringSiteId**), päivämäärä (**DemandDate**), määrä (**DemandQuantity**) ja joko nimikenumero (**ItemNumber**) tai nimikkeen kohdistustunnus (**ProductAllocationKeyId**).</span><span class="sxs-lookup"><span data-stu-id="e6654-112">The following entity fields are mandatory: site (**DeliveringSiteId**), date (**DemandDate**), quantity (**DemandQuantity**), and either item number (**ItemNumber**) or item allocation key (**ProductAllocationKeyId**).</span></span>

<span data-ttu-id="e6654-113">Voit käyttää tietoyksikköä, kun käytössä on historialliset kysyntätiedot sisältävä Microsoft Excel -tiedosto tai CSV-tiedosto (pilkulla erotettujen arvojen tiedosto).</span><span class="sxs-lookup"><span data-stu-id="e6654-113">To use the data entity, you must have a Microsoft Excel file or comma-separated values (CSV) file that contains the historical demand data.</span></span> <span data-ttu-id="e6654-114">Seuraavassa esimerkissä näytetään, miten tiedot tuodaan CSV-tiedostosta.</span><span class="sxs-lookup"><span data-stu-id="e6654-114">The following example shows how to import the data from a CSV file.</span></span>

<span data-ttu-id="e6654-115">Lisätietoja tietojen tuonnista sekä tietojen tyhjentämisestä tuonnin jälkeen on kohdassa [Tietojen tuonti- ja vientityöt – yleiskatsaus](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md) ja siihen liittyvissä aiheissa.</span><span class="sxs-lookup"><span data-stu-id="e6654-115">For more information about how to import data, including how to clean up data after an import, see [Data import and export jobs overview](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md) and its related topics.</span></span>

## <a name="example"></a><span data-ttu-id="e6654-116">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="e6654-116">Example</span></span>

<span data-ttu-id="e6654-117">Voit käyttää esimerkkinä seuraavaa tiedostoa.</span><span class="sxs-lookup"><span data-stu-id="e6654-117">You can use the following file as an example.</span></span> <span data-ttu-id="e6654-118">Lataa [HistoricalDemandData](/dynamics/s-e/).</span><span class="sxs-lookup"><span data-stu-id="e6654-118">Download the [HistoricalDemandData](/dynamics/s-e/).</span></span> <span data-ttu-id="e6654-119">Tämä tiedosto sisältää nimikkeen D0001 historialliset kysyntätiedot.</span><span class="sxs-lookup"><span data-stu-id="e6654-119">This file contains the historical demand data for item D0001.</span></span> <span data-ttu-id="e6654-120">Se sisältää vain seuraavat pakolliset kentät: sivusto, määrä ja kysynnän päivämäärä.</span><span class="sxs-lookup"><span data-stu-id="e6654-120">It contains only the following mandatory fields: site, quantity, and the demand date.</span></span>

1. <span data-ttu-id="e6654-121">Valitse yritys, johon historialliset kysyntätiedot tuodaan.</span><span class="sxs-lookup"><span data-stu-id="e6654-121">Select the company to import the historical demand data into.</span></span>
2. <span data-ttu-id="e6654-122">Avaa **Tietojen hallinta** -työtila.</span><span class="sxs-lookup"><span data-stu-id="e6654-122">Open the **Data management** workspace.</span></span>
3. <span data-ttu-id="e6654-123">Valitse **Tuonti**-ruutu.</span><span class="sxs-lookup"><span data-stu-id="e6654-123">Select the **Import** tile.</span></span>
4. <span data-ttu-id="e6654-124">Syötä tuontiprojektin nimi, kuten **Nimikkeen D0001 historiallisen kysynnän tuominen**.</span><span class="sxs-lookup"><span data-stu-id="e6654-124">Enter a name for the import project, such as **Import historical demand for item D0001**.</span></span>
5. <span data-ttu-id="e6654-125">Valitse **Lähdetietojen muoto** -kenttään tuotavan tiedoston muoto.</span><span class="sxs-lookup"><span data-stu-id="e6654-125">In the **Source data format** field, select the file format of the file that you're importing.</span></span> <span data-ttu-id="e6654-126">Voit tuoda tämän esimerkin HistoricalDemandData-tiedoston valitsemalla **CSV**.</span><span class="sxs-lookup"><span data-stu-id="e6654-126">To import the HistoricalDemandData file for this example, select **CSV**.</span></span>
6. <span data-ttu-id="e6654-127">Valitse **Yksikön nimi** -kenttään **Historiallinen ulkoinen kysyntä**.</span><span class="sxs-lookup"><span data-stu-id="e6654-127">In the **Entity name** field, select **Historical external demand**.</span></span>
7. <span data-ttu-id="e6654-128">Tallenna tiedosto tietokoneeseen ja lataa se.</span><span class="sxs-lookup"><span data-stu-id="e6654-128">Save the file to your computer, and then upload it.</span></span>
8. <span data-ttu-id="e6654-129">Valitse **Tuo**.</span><span class="sxs-lookup"><span data-stu-id="e6654-129">Select **Import**.</span></span>
9. <span data-ttu-id="e6654-130">**Suorituksen yhteenveto** -sivu avautuu automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="e6654-130">The **Execution summary** page is opened automatically.</span></span> <span data-ttu-id="e6654-131">Tarkista sivun tuodut tiedot.</span><span class="sxs-lookup"><span data-stu-id="e6654-131">Verify the imported data on the page.</span></span>

<span data-ttu-id="e6654-132">Kun historialliset kysyntätiedot on tuotu, voit luoda kysynnän ennusteen.</span><span class="sxs-lookup"><span data-stu-id="e6654-132">After you've imported the historical demand data, you can generate a demand forecast.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e6654-133">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="e6654-133">Additional resources</span></span>

[<span data-ttu-id="e6654-134">Tilastollisen perusennusteen luominen</span><span class="sxs-lookup"><span data-stu-id="e6654-134">Generate a statistical baseline forecast</span></span>](generate-statistical-baseline-forecast.md)  
[<span data-ttu-id="e6654-135">Tietojen tuonti- ja vientityöt – yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="e6654-135">Data import and export jobs overview</span></span>](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]