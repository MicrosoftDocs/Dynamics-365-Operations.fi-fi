---
title: Nimikehintojen vertailun varastoraportti
description: Lisätietoja nimikehintojen vertailun varastoraportin luomisesta ja tuloksen selaamisesta ja/tai viemisestä.
author: AndersGirke
manager: tfehr
ms.date: 01/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostAdminWorkspace, CostAnalysisWorkspace, InventItemPriceCompareStorage, InventItemPriceCompareStorageDetailsChart, InventItemPriceCompareStorageDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2020-03-01
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 73e43a685f390fd718028de6add0370dfcd6cf3b
ms.sourcegitcommit: cd339f48066b1d0fc740b513cb72ea19015acd16
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/02/2020
ms.locfileid: "3759637"
---
# <a name="compare-item-prices-storage-report"></a><span data-ttu-id="41268-103">Nimikehintojen vertailun varastoraportti</span><span class="sxs-lookup"><span data-stu-id="41268-103">Compare item prices storage report</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="41268-104">Tässä ohjeaiheessa kerrotaan, miten **nimikehintojen vertailun varasto** -raportti suoritetaan ja miten tulos määritetään käytettäväksi digitaalisesti interaktiivisena sivuna Dynamics 365 Supply Chain Management -sovelluksessa tai vietynä asiakirjana jossakin useista muodoista.</span><span class="sxs-lookup"><span data-stu-id="41268-104">This topic explains how to run a **Compare item prices storage** report and make the output available digitally, either as an interactive page in Dynamics 365 Supply Chain Management, or as an exported document in any of several formats.</span></span>

<span data-ttu-id="41268-105">Kun tarkastelet raporttia selaimessa, sarakkeita ja yhdistettyjä saldoja muutetaan dynaamisesti määritetyn asettelun perusteella.</span><span class="sxs-lookup"><span data-stu-id="41268-105">When you view the report in your browser, columns and aggregate balances are dynamically adjusted, depending on your configured layout.</span></span> <span data-ttu-id="41268-106">Voit esimerkiksi lajitella tulokset, suodattaa ne ja porautua tietoihin.</span><span class="sxs-lookup"><span data-stu-id="41268-106">You can sort the results, filter them, drill down into the data, and more.</span></span>

<span data-ttu-id="41268-107">Raportin tulokset tallennetaan **Vertaa nimikehintoja** -tietoentiteettiin. Sen avulla voit suodattaa ja viedä tulokset esimerkiksi CSV- tai Microsoft Excel -muodossa.</span><span class="sxs-lookup"><span data-stu-id="41268-107">Report results are stored in the **Compare item prices** data entity, which lets you filter and export the results to a format such as CSV or Microsoft Excel.</span></span>

<span data-ttu-id="41268-108">**Nimikehintojen vertailun varasto** -raportti on hyödyllinen silloin, kun tuloksissa on useita rivejä.</span><span class="sxs-lookup"><span data-stu-id="41268-108">The **Compare item prices storage** report is helpful in cases where the output contains many lines.</span></span> <span data-ttu-id="41268-109">Tuloksissa voi olla useita rivejä esimerkiksi silloin, jos yli 40 000 nimikettä sisältää odottavan nimikehinnan kustannuslaskennan versiossa.</span><span class="sxs-lookup"><span data-stu-id="41268-109">For example, the output will contain many lines if you have more than 40,000 items holding a pending item price in the costing version.</span></span>

## <a name="enable-compare-item-prices-storage"></a><span data-ttu-id="41268-110">Nimikehintojen vertailun varaston käyttöönotto</span><span class="sxs-lookup"><span data-stu-id="41268-110">Enable compare item prices storage</span></span>

<span data-ttu-id="41268-111">Ennen kuin käytät tätä toimintoa, sinun on otettava se käyttöön järjestelmässä.</span><span class="sxs-lookup"><span data-stu-id="41268-111">Before you can use this feature, you must enable it on your system.</span></span> <span data-ttu-id="41268-112">Järjestelmänvalvojat voivat käyttää [toimintojen hallinnan](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) asetuksia ja tarkistaa toiminnon tilan sekä ottaa sen käyttöön tarvittaessa.</span><span class="sxs-lookup"><span data-stu-id="41268-112">Administrators can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the feature status and enable it if needed.</span></span> <span data-ttu-id="41268-113">Toiminto näkyy seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="41268-113">Here, the feature is listed as:</span></span>

- <span data-ttu-id="41268-114">**Moduuli** - kustannustenhallinta</span><span class="sxs-lookup"><span data-stu-id="41268-114">**Module** - Cost management</span></span>
- <span data-ttu-id="41268-115">**Toiminnon nimi** - nimikehintojen vertailun varasto</span><span class="sxs-lookup"><span data-stu-id="41268-115">**Feature name** - Compare item price storage</span></span>

## <a name="generate-a-compare-item-prices-storage-report"></a><span data-ttu-id="41268-116">Nimikehintojen vertailun varastoraportin luominen</span><span class="sxs-lookup"><span data-stu-id="41268-116">Generate a Compare item prices storage report</span></span>

<span data-ttu-id="41268-117">Seuraavien vaiheiden avulla voit luoda ja tallentaa **Nimikehintojen vertailun varasto** -raportin:</span><span class="sxs-lookup"><span data-stu-id="41268-117">Follow these steps to generate and store a **Compare item prices storage** report:</span></span>

1. <span data-ttu-id="41268-118">Siirry kohtaan **Kustannustenhallinta > Kyselyt ja raportit > Ennalta määritetyt kustannusraportit > Nimikehintojen vertailun varasto**.</span><span class="sxs-lookup"><span data-stu-id="41268-118">Go to **Cost management > Inquiries and reports > Predetermined cost reports > Compare item prices storage**.</span></span>

1. <span data-ttu-id="41268-119">Valitse **Uusi**, jos haluat avata **Vertaa nimikehintoja** -ruudun.</span><span class="sxs-lookup"><span data-stu-id="41268-119">Select **New** to open the **Compare item prices** pane.</span></span> <span data-ttu-id="41268-120">Määritä seuraavat vaihtoehdot, jos haluat määrittää, mitä hintoja raportissa vertaillaan:</span><span class="sxs-lookup"><span data-stu-id="41268-120">Set the following options to define which prices to compare in your report:</span></span>

    - <span data-ttu-id="41268-121">Anna **Parametrit**-pikavälilehdessä raportille yksilöivä **nimi** ja määritä **Odottavat hinnat, joita vertaillaan**- ja **Vertailussa käytettävät hinnat** -osien avulla vertailtavat hinnat ja päivämäärät.</span><span class="sxs-lookup"><span data-stu-id="41268-121">On the **Parameters** FastTab, give the report a unique **Name** and use the fields in the **Pending prices to compare** and **Prices used for comparison** sections to define which prices and dates to compare.</span></span>
    - <span data-ttu-id="41268-122">Määritä **Sisällytettävät tietueet** -pikavälilehdessä suodattimet ja rajoitteet, joiden avulla määritetään raporttiin sisällytettävät tiedot.</span><span class="sxs-lookup"><span data-stu-id="41268-122">On the **Records to include** FastTab, set up filters and constraints to define which data to include in the report.</span></span>
    - <span data-ttu-id="41268-123">Määritä **Suorita taustalla** -pikavälilehdessä miten, milloin ja miten usein raportti luodaan.</span><span class="sxs-lookup"><span data-stu-id="41268-123">On the **Run in the background** FastTab, set up how, when, and the frequency at which you want to generate the report.</span></span>
    > [!NOTE]
    > <span data-ttu-id="41268-124">Tämä raportti suoritetaan aina osana erätyötä.</span><span class="sxs-lookup"><span data-stu-id="41268-124">This report is always executed as part of a batch job.</span></span>

1. <span data-ttu-id="41268-125">Ota asetukset käyttöön valitsemalla **OK** ja sulje ruutu.</span><span class="sxs-lookup"><span data-stu-id="41268-125">Select **OK** to apply your settings and close the pane.</span></span>

1. <span data-ttu-id="41268-126">Kun erätyö on tehty, se näkyy **Nimikehintojen vertailun varasto** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="41268-126">After the batch job is completed, it will be listed on the **Compare item prices storage** page.</span></span> <span data-ttu-id="41268-127">Sinun on ehkä päivitettävä sivu, jotta näet raportin.</span><span class="sxs-lookup"><span data-stu-id="41268-127">You may need to refresh the page to see the report.</span></span>

## <a name="explore-the-compare-item-prices-storage-report"></a><span data-ttu-id="41268-128">Nimikehintojen vertailun varastoraporttiin tutustuminen</span><span class="sxs-lookup"><span data-stu-id="41268-128">Explore the Compare item prices storage report</span></span>

<span data-ttu-id="41268-129">Kun olet luonut raportin, voit tarkastella sitä ja tutustua sen tietoihin milloin tahansa seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="41268-129">After you've generated a report, you can view and explore it at any time as follows:</span></span>

1. <span data-ttu-id="41268-130">Siirry kohtaan **Kustannustenhallinta > Kyselyt ja raportit > Ennalta määritetyt kustannusraportit > Nimikehintojen vertailun varasto**.</span><span class="sxs-lookup"><span data-stu-id="41268-130">Go to **Cost management > Inquiries and reports > Predetermined cost reports > Compare item prices storage**.</span></span>

1. <span data-ttu-id="41268-131">Valitse luettelosta raportti.</span><span class="sxs-lookup"><span data-stu-id="41268-131">Select a report from the list.</span></span>

1. <span data-ttu-id="41268-132">Tee jompikumpi seuraavista toimista:</span><span class="sxs-lookup"><span data-stu-id="41268-132">Do one of the following:</span></span>

    - <span data-ttu-id="41268-133">Voit hakea raportin tulosten yleiskatsauksen valitsemalla **Yleiskatsaus**-kohdan.</span><span class="sxs-lookup"><span data-stu-id="41268-133">Select **Overview** to get an overview of your report results.</span></span>
    - <span data-ttu-id="41268-134">Valitsemalla **Näytä tiedot** saat tarkemman näkymän raportista</span><span class="sxs-lookup"><span data-stu-id="41268-134">Select **View details** to get a more detailed view of your report</span></span>

1. <span data-ttu-id="41268-135">Kun valittu näkymä avautuu, voit tehdä seuraavat toiminnot:</span><span class="sxs-lookup"><span data-stu-id="41268-135">After the selected view opens, you can do the following:</span></span>

    - <span data-ttu-id="41268-136">Valitse lähes mikä tahansa sarakeotsikko, kun haluat lajitella tai suodattaa taulun kyseisen sarakkeen arvojen mukaan. Näin voi tehdä lähes missä tahansa vakiolomakkeessa Supply Chain Management -sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="41268-136">Select almost any column heading to sort or filter the table by values in that column, just as with most standard forms in Supply Chain Management.</span></span> <span data-ttu-id="41268-137">Ota huomioon, että et voi lajitella tai suodattaa **Nettohinnan muutos-%** -sarakkeen mukaan, koska se on laskettu kenttä.</span><span class="sxs-lookup"><span data-stu-id="41268-137">Note, you can't sort or filter the **Net change price %** column because it's a calculated field.</span></span>
    - <span data-ttu-id="41268-138">Valitse **Dimension näyttö**, jos haluat avata ruudun ja valita lomakkeeseen sisällytettävän dimensiosarakkeen.</span><span class="sxs-lookup"><span data-stu-id="41268-138">Select **Dimension display** to open a pane where you can choose which dimension column to include on the form.</span></span> <span data-ttu-id="41268-139">Määritä **Tallenna asetukset** -kohdan arvoksi **Kyllä**, jos haluat tallentaa asetukset niin, että ne ovat käytettävissä raportin seuraavalla avauskerralla.</span><span class="sxs-lookup"><span data-stu-id="41268-139">Set **Save setup** to **Yes** if you'd like to save these settings so they will be preserved the next time you open the report.</span></span> <span data-ttu-id="41268-140">Ota asetukset käyttöön valitsemalla **OK** ja sulje.</span><span class="sxs-lookup"><span data-stu-id="41268-140">Select **OK** to apply your settings and close.</span></span>
    - <span data-ttu-id="41268-141">Valitse mikä tahansa lomakkeen rivi ja valitse sitten **Näytä tiedot**, jos haluat katsella valitun nimikkeen lisätietoja.</span><span class="sxs-lookup"><span data-stu-id="41268-141">Select any row in the form and then select **View details** to see more information about the selected item.</span></span> <span data-ttu-id="41268-142">Voit porautua tietoihin tästä.</span><span class="sxs-lookup"><span data-stu-id="41268-142">You'll be able to drill down into the data from here.</span></span>
    - <span data-ttu-id="41268-143">Valitse mikä tahansa lomakkeen rivi ja valitse sitten **Näytä vertailukaavio**, jos haluat nähdä vuorovaikutteisen graafisen esityksen tuloksista, jotka liittyvät valitsemaasi nimikkeeseen.</span><span class="sxs-lookup"><span data-stu-id="41268-143">Select any row in the form and then select **View comparison chart** to see an interactive graphical representation of your results as they relate to your selected item.</span></span> <span data-ttu-id="41268-144">Voit tutustua näihin tuloksiin valitsemalla kaavion ja kaavion selitteen erilaisia graafisia elementtejä.</span><span class="sxs-lookup"><span data-stu-id="41268-144">You can explore these results by selecting various graphical elements in the chart and chart legend.</span></span>
    - <span data-ttu-id="41268-145">Valitse mikä tahansa lomakkeen rivi ja valitse sitten **Näytä laskelman tiedot**, jos haluat katsella valittuun nimikkeeseen liittyviä laskelmia.</span><span class="sxs-lookup"><span data-stu-id="41268-145">Select any row in the form and then select **View calculation details** to see more information about calculations related to the selected item.</span></span> <span data-ttu-id="41268-146">Voit porautua tietoihin tästä.</span><span class="sxs-lookup"><span data-stu-id="41268-146">You'll be able to drill down into the data from here.</span></span>

## <a name="export-the-compare-item-prices-storage-report"></a><span data-ttu-id="41268-147">Nimikehintojen vertailun varastoraportin vieminen</span><span class="sxs-lookup"><span data-stu-id="41268-147">Export the Compare item prices storage report</span></span>

<span data-ttu-id="41268-148">Kaikki luodut raportit tallennetaan **Vertaa nimikehintoja** -tietoentiteettiin.</span><span class="sxs-lookup"><span data-stu-id="41268-148">Each report that you generate is stored in the **Compare item prices** data entity.</span></span> <span data-ttu-id="41268-149">Voit käyttää Supply Chain Management -sovelluksen vakiotiedonhallintatoimintoja, jos haluat viedä tämän entiteetin tiedot mihin tahansa tuettuun tietomuotoon, kuten CSV- tai Microsoft Excel -muotoon.</span><span class="sxs-lookup"><span data-stu-id="41268-149">You can use the standard data management features of Supply Chain Management to export data from this entity to any supported data format, including CSV or Microsoft Excel.</span></span>

<span data-ttu-id="41268-150">Seuraavassa on esimerkki siitä, miten **Nimikehintojen vertailun varasto** -raporttia viedään:</span><span class="sxs-lookup"><span data-stu-id="41268-150">The following is an example of how to export a **Compare item prices storage** report:</span></span>

1. <span data-ttu-id="41268-151">Siirry kohtaan **Järjestelmänhallinta > Työtilat > Tietojen hallinta**.</span><span class="sxs-lookup"><span data-stu-id="41268-151">Go to **System administration > Workspaces > Data management**.</span></span>

1. <span data-ttu-id="41268-152">Valitse **Vie**-painike **Tietojen hallinta** -osassa.</span><span class="sxs-lookup"><span data-stu-id="41268-152">Select the **Export** button in the **Data management** section.</span></span>

1. <span data-ttu-id="41268-153">Näkyviin tulee **Vienti**-sivu, jonka avulla vientityö määritetään.</span><span class="sxs-lookup"><span data-stu-id="41268-153">The **Export** page opens, which you'll use to set up your export job.</span></span> <span data-ttu-id="41268-154">Aloita antamalla työlle **Ryhmän nimi**.</span><span class="sxs-lookup"><span data-stu-id="41268-154">Start by giving your job a **Group name**.</span></span>

1. <span data-ttu-id="41268-155">Valitse **Valitut entiteetit** -osassa **Lisää entiteetti** ja avaa valintaikkuna, jossa määritetään seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="41268-155">In the **Selected entities** section, select **Add entity** to open a dialog box where you can set the following options:</span></span>

    - <span data-ttu-id="41268-156">**Yksikön nimi** - Valitse **Vertaa nimikehintoja**.</span><span class="sxs-lookup"><span data-stu-id="41268-156">**Entity name** - Select **Compare item prices**.</span></span>
    - <span data-ttu-id="41268-157">**Kohdetietojen muoto** - Valitse muoto, johon haluat viedä.</span><span class="sxs-lookup"><span data-stu-id="41268-157">**Target data format** - Choose the format that you want to export to.</span></span>

1. <span data-ttu-id="41268-158">Valitse **Lisää**, jos haluat lisätä uuden rivin. Valitse sitten **Sulje**, jolloin valintaikkuna suljetaan.</span><span class="sxs-lookup"><span data-stu-id="41268-158">Select **Add** to add the new row and then select **Close** to close the dialog box.</span></span>

1. <span data-ttu-id="41268-159">Tavallisesti viedään yksi raportti kerralla.</span><span class="sxs-lookup"><span data-stu-id="41268-159">Usually you'll export one report at a time.</span></span> <span data-ttu-id="41268-160">Voit tehdä tämän määrittämällä **suodattimen** **Kysely**-ruudussa lisätylle riville.</span><span class="sxs-lookup"><span data-stu-id="41268-160">To do this, set up a **Filter** for the row you just added to the **Inquiry** pane.</span></span> <span data-ttu-id="41268-161">Näin voit määrittää, mitkä raportit **Vertaa nimikehintoja** -entiteetistä sisällytetään raporttiin.</span><span class="sxs-lookup"><span data-stu-id="41268-161">This will let you define which reports from the **Compare item prices** entity that you want to include in your export.</span></span> <span data-ttu-id="41268-162">Vie yksi raporttiin määrittämällä seuraavat suodatusvalinnat:</span><span class="sxs-lookup"><span data-stu-id="41268-162">Set the following filter options to export a single report:</span></span>

    - <span data-ttu-id="41268-163">Valitse **Väli**-välilehdessä **Lisää**, jos haluat lisätä uuden rivin.</span><span class="sxs-lookup"><span data-stu-id="41268-163">On the **Range** tab, select **Add** to add a new row.</span></span>
    - <span data-ttu-id="41268-164">Määritä **Taulu**-kohdan arvoksi **Vertaa nimikehintoja**.</span><span class="sxs-lookup"><span data-stu-id="41268-164">Set **Table** to **Compare item prices**.</span></span>
    - <span data-ttu-id="41268-165">Määritä **Johdettu taulu** -kohdan arvoksi **Vertaa nimikehintoja**.</span><span class="sxs-lookup"><span data-stu-id="41268-165">Set **Derived table** to **Compare item prices**.</span></span>
    - <span data-ttu-id="41268-166">Määritä **Kenttä** sille kentälle, jonka mukaan haluat suodattaa.</span><span class="sxs-lookup"><span data-stu-id="41268-166">Set **Field** to the field that you want to filter by.</span></span> <span data-ttu-id="41268-167">Yleensä käytetään **suorituksen nimeä** tai **suorituksen aikaa**.</span><span class="sxs-lookup"><span data-stu-id="41268-167">Usually you'll use **Execution name** or **Execution time**.</span></span>
    - <span data-ttu-id="41268-168">Määritä **Ehdot** arvolle valitusta kentästä, jota haluat etsiä (joko raportin nimi tai sen luontiaika).</span><span class="sxs-lookup"><span data-stu-id="41268-168">Set **Criteria** to the value from your selected field that you want to look for (either the name of the report or the time the report was generated).</span></span>
    - <span data-ttu-id="41268-169">Lisää tarvittaessa rivejä **Väli**-taulukkoon, kunnes olet yksilöinyt etsittävän raportin.</span><span class="sxs-lookup"><span data-stu-id="41268-169">If necessary, add more rows to the **Range** table until you have uniquely identified the report that you're looking for.</span></span>

1. <span data-ttu-id="41268-170">Tallenna asetukset valitsemalla **OK** ja sulje.</span><span class="sxs-lookup"><span data-stu-id="41268-170">Select **OK** to save your settings and close.</span></span>

1. <span data-ttu-id="41268-171">Tallenna vientiasetukset valitsemalla **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="41268-171">Select **Save** to save your export setup.</span></span>

1. <span data-ttu-id="41268-172">Avaa **Vientiasetukset**-välilehti ja luo vientitiedosto valitsemalla **Vie nyt**.</span><span class="sxs-lookup"><span data-stu-id="41268-172">Open the **Export options** tab and select **Export now** to generate the export file.</span></span>

1. <span data-ttu-id="41268-173">Näkyviin tulee **Suorituksen yhteenveto** -sivu, jolla näkyy vientityön tila ja vietyjen entiteettien luettelo.</span><span class="sxs-lookup"><span data-stu-id="41268-173">The **Execution summary** page opens, where you can see the status of your export job and a list of entities that were exported.</span></span> <span data-ttu-id="41268-174">Valitse **Vertaa nimikehintoja** -entiteetti, joka on **Entiteetin käsittelyn tila** -alueella. Lataa tästä entiteetistä viedyt tiedot valitsemalla **Lataa tiedosto**.</span><span class="sxs-lookup"><span data-stu-id="41268-174">Select the **Compare item prices** entity listed in the **Entity processing status** area and then select **Download file** to download the data exported from that entity.</span></span>

<span data-ttu-id="41268-175">Lisätietoja tietojen hallinnan käyttämisestä tietojen viemisessä on kohdassa [Tietojen tuonti- ja vientitöiden yleiskatsaus](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md).</span><span class="sxs-lookup"><span data-stu-id="41268-175">For more information about how to use data management to export data, see [Data import and export jobs overview](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md).</span></span>
