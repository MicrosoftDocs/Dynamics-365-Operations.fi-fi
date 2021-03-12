---
title: Manuaalisten oikaisujen tekeminen perusennusteeseen
description: Tässä ohjeaiheessa kerrotaan, miten voit tehdä manuaalisia oikaisuja perusennusteeseen ja tarkastella ennusteen tietoja.
author: roxanadiaconu
manager: tfehr
ms.date: 01/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqDemPlanForecastViewer
audience: Application User
ms.reviewer: kamaybac
ms.custom: 72704
ms.assetid: e7c5d44e-07bc-40b1-a4b3-8ba46483ef9e
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: afdcbb98c96b2a685f64a16886b9a064ed13c2c0
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4967027"
---
# <a name="make-manual-adjustments-to-the-baseline-forecast"></a><span data-ttu-id="f157b-103">Manuaalisten oikaisujen tekeminen perusennusteeseen</span><span class="sxs-lookup"><span data-stu-id="f157b-103">Make manual adjustments to the baseline forecast</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f157b-104">Tässä ohjeaiheessa kerrotaan, miten voit tehdä manuaalisia oikaisuja perusennusteeseen ja tarkastella ennusteen tietoja.</span><span class="sxs-lookup"><span data-stu-id="f157b-104">This topic explains how you can make manual adjustments to a baseline forecast and view details of the forecast.</span></span> 

<span data-ttu-id="f157b-105">Ennen kuin teet manuaalisia oikaisuja, on tärkeää, että ymmärrät muutamia eri sivujen konsepteja.</span><span class="sxs-lookup"><span data-stu-id="f157b-105">Before you make manual adjustments, it's important that you understand a few concepts on various pages.</span></span>

## <a name="grid-on-the-adjusted-demand-forecast-page"></a><span data-ttu-id="f157b-106">Ruudukko Oikaistu kysynnän ennuste -sivulla</span><span class="sxs-lookup"><span data-stu-id="f157b-106">Grid on the Adjusted demand forecast page</span></span>
<span data-ttu-id="f157b-107">**Oikaistu kysynnän ennuste** -sivu sisältää ruudukon, jossa on seuraava rakenne:</span><span class="sxs-lookup"><span data-stu-id="f157b-107">The **Adjusted demand forecast** page includes a grid that has the following structure:</span></span>

-   <span data-ttu-id="f157b-108">Ensimmäisessä sarakkeessa näytetään nimike, nimikkeen kohdistustunnukset, yritykset ja niin edelleen, joille ennuste on luotu.</span><span class="sxs-lookup"><span data-stu-id="f157b-108">The first column shows the items, item allocation keys, companies, and so on, that the forecast has been generated for.</span></span> <span data-ttu-id="f157b-109">Sivun alaotsikko antaa kuvauksen nykyisistä ennustedimensioista, jotka näkyvät ruudukossa.</span><span class="sxs-lookup"><span data-stu-id="f157b-109">The subtitle of the page provides a description of the current forecast dimensions that are shown in the grid.</span></span> <span data-ttu-id="f157b-110">Jos esimerkiksi sivun alaotsikko on **Yritys/Toimipaikka/Nimikkeen kohdistustunnus**, ja yksi ruudukon riviotsikoista on **USMF / 1 / D\_Alloc**, kyseinen rivi näyttää ennusteen USMF-yrityksen toimipaikalle 1, ja **D\_Alloc** nimikkeen kohdistustunnuksen.</span><span class="sxs-lookup"><span data-stu-id="f157b-110">For example, if the subtitle of the page is **Company / Site / Item allocation key**, and one of the row headers in the grid is **USMF / 1 / D\_Alloc**, that row shows the forecast for the USMF company, site 1, and the **D\_Alloc** item allocation key.</span></span>
-   <span data-ttu-id="f157b-111">Seuraavissa sarakkeissa näytetään ennustejaksot, joille ennuste on luotu.</span><span class="sxs-lookup"><span data-stu-id="f157b-111">Subsequent columns represent the forecast buckets that the forecast has been generated for.</span></span> <span data-ttu-id="f157b-112">Kussakin sarakkeen otsikossa on sarakkeen näyttämä ennustejakson ensimmäinen päivä.</span><span class="sxs-lookup"><span data-stu-id="f157b-112">Each column header is the first date of the forecast bucket that the column shows.</span></span>
-   <span data-ttu-id="f157b-113">Solujen arvot edustavat yhden nimikkeen, nimikkeen kohdistustunnuksen jne. ennustetta tälle nimenomaiselle ennustejaksolle.</span><span class="sxs-lookup"><span data-stu-id="f157b-113">The values in the cells represent the forecast for one item, item allocation key, and so on, for that specific forecast bucket.</span></span>

## <a name="forecast-aggregation-and-de-aggregation"></a><span data-ttu-id="f157b-114">Ennusteen koostaminen ja koosteen purkaminen</span><span class="sxs-lookup"><span data-stu-id="f157b-114">Forecast aggregation and de-aggregation</span></span>
<span data-ttu-id="f157b-115">Sivun alaotsikko näyttää ennusteen koostamisen tason.</span><span class="sxs-lookup"><span data-stu-id="f157b-115">The subtitle of the page shows the level of forecast aggregation.</span></span> 

<span data-ttu-id="f157b-116">Jos esimerkiksi sivun alaotsikko on **Yritys/Toimipaikka/Kohdistustunnus/Nimikkeen numero/Väri/Koko/Konfiguraatio/Tyyli**, ennusteen koostetta ei ole ja ennuste näytetään nimikkeen ja sen dimensioiden tasolla.</span><span class="sxs-lookup"><span data-stu-id="f157b-116">For example, if the subtitle of the page is **Company / Site / Allocation key / Item number / Color / Size / Configuration / Style**, there is no forecast aggregation, and the forecast is shown at the level of the item and its dimensions.</span></span> <span data-ttu-id="f157b-117">Voit muuttaa koostetta **Muuta ennustedimensioita** -sivulla, jonka voit avata sovellusvalikosta.</span><span class="sxs-lookup"><span data-stu-id="f157b-117">To change the aggregation, use the **Change forecast dimensions** page, which you can open from the application menu.</span></span> 

<span data-ttu-id="f157b-118">Muokkaa ennustetta napsauttamalla mitä tahansa käytettävissä olevaa solua ja kirjoita oikaistu ennusteen arvo.</span><span class="sxs-lookup"><span data-stu-id="f157b-118">To modify the forecast, click in any of the cells that are available, and type the adjusted forecast value.</span></span> <span data-ttu-id="f157b-119">Muokattu solu muuttuu heti lihavoiduksi osoittamaan, että sen näyttämä ennuste ei ole kysynnän ennusteen palvelun luoma ennuste, vaan sitä on muokattu manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="f157b-119">The edited cell immediately becomes bold to indicate that the forecast that it shows isn't the forecast that the demand forecasting service created, but has been manually adjusted.</span></span> 

<span data-ttu-id="f157b-120">Jos muutat koosteen niin, että sivu näyttää enemmän koostettuja tietoja, voit näet **Kysynnän ennusteen rivit** -sivulla yksittäiset ennusteen rivit, joista koostettu ennuste on muodostunut.</span><span class="sxs-lookup"><span data-stu-id="f157b-120">If you change the aggregation to make the page show more aggregated data, you can use the **Demand forecast lines** page to see the individual forecast lines that make up the aggregated forecast.</span></span> 

<span data-ttu-id="f157b-121">Olet esimerkiksi luonut ennusteen nimiketasolla mutta tiedät, että tämän nimikkeen kysyntä tulee kasvamaan kaikissa toimipaikoissa kampanjasta tai vastaavasta tapahtumasta johtuen.</span><span class="sxs-lookup"><span data-stu-id="f157b-121">For example, you've generated the forecast at the item level, but you know that the demand for this item will increase across all sites because of a promotion or another similar event.</span></span> <span data-ttu-id="f157b-122">Tässä tapauksessa voit määrittää koosteen arvoksi **Yritys/Nimikkeen kohdistustunnus/Nimike** **Muuta ennustedimensioita** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="f157b-122">In this case, you can set the aggregation to **Company / Item allocation key / Item** on the **Change forecast dimensions** page.</span></span> <span data-ttu-id="f157b-123">Voit oikaista nimikkeen yleisen ennusteen kaikissa toimipaikoissa **Oikaistu kysynnän ennuste** -ruudukossa.</span><span class="sxs-lookup"><span data-stu-id="f157b-123">You can adjust the global forecast for the item across all sites in the **Adjusted demand forecast** grid.</span></span> <span data-ttu-id="f157b-124">Näet muutoksesi vaikutuksen kaikissa toimipaikoissa, kun avaat **Kysynnän ennusteen rivit** -sivun.</span><span class="sxs-lookup"><span data-stu-id="f157b-124">To see the effect of your change across all sites, open the **Demand forecast lines** page.</span></span> <span data-ttu-id="f157b-125">Tällä sivulla näet yhden rivin nimikkeelle kussakin toimipisteessä, oikaistun ennusteen määrän sekä alkuperäisen ennusteen määrän.</span><span class="sxs-lookup"><span data-stu-id="f157b-125">On this page, you will see one line for the item for each site, the adjusted forecast quantity, and the original forecast quantity.</span></span> 

<span data-ttu-id="f157b-126">Kun ennustetun määrän oikaisu tehdään koostetasolla, järjestelmä käyttää painotettua kohdistusta jakaakseen muutoksen riveille, joista kooste muodostuu.</span><span class="sxs-lookup"><span data-stu-id="f157b-126">When the adjustment of the forecasted quantity is made at an aggregated level, the system uses weighted allocation to distribute the change among the lines that create the aggregation.</span></span> 

<span data-ttu-id="f157b-127">Voit myös tehdä manuaalisia oikaisuja **Kysynnän ennusteen rivit** -sivulla muokkaamalla joko **Kokonaismäärä**-arvoa tai **Määrä**-soluja koosteen purkuruudukossa.</span><span class="sxs-lookup"><span data-stu-id="f157b-127">You can also make manual adjustments on the **Demand forecast lines** page, by modifying either the **Total quantity** value or the **Quantity** cells in the de-aggregation grid.</span></span>

## <a name="viewing-details-of-the-forecast"></a><span data-ttu-id="f157b-128">Ennusteen tietojen tarkasteleminen</span><span class="sxs-lookup"><span data-stu-id="f157b-128">Viewing details of the forecast</span></span>
<span data-ttu-id="f157b-129">Voit avata **Kysynnän ennusteen tiedot** -sivun nähdäksesi ennustetta koskevia lisätietoja.</span><span class="sxs-lookup"><span data-stu-id="f157b-129">You can open the **Demand forecast details** page to view more information about the forecast.</span></span> 

<span data-ttu-id="f157b-130">**Kysynnän ennusteen tiedot** -sivulla näet seuraavat tiedot graafisessa ja taulukkomuodossa.</span><span class="sxs-lookup"><span data-stu-id="f157b-130">The **Demand forecast details** page shows the following information in graphical and tabular formats:</span></span>

-   <span data-ttu-id="f157b-131">Historiallinen kysyntä, johon ennusteet perustuvat.</span><span class="sxs-lookup"><span data-stu-id="f157b-131">The historical demand that the forecast predictions are based on.</span></span>
-   <span data-ttu-id="f157b-132">Nykyinen ennuste, jota pääsuunnittelu käyttää.</span><span class="sxs-lookup"><span data-stu-id="f157b-132">The current forecast that is used by Master planning.</span></span>
-   <span data-ttu-id="f157b-133">Uudet kysynnän ennusteen arvot ja niiden manuaalisten oikaisujen määrät.</span><span class="sxs-lookup"><span data-stu-id="f157b-133">The new demand forecast values and the amounts they have been manually adjusted by.</span></span>
-   <span data-ttu-id="f157b-134">Ennustettujen arvojen luottamusväli.</span><span class="sxs-lookup"><span data-stu-id="f157b-134">The confidence interval for the forecasted values.</span></span>
-   <span data-ttu-id="f157b-135">Ennustemalli, jota käytettiin ennusteen luontiin.</span><span class="sxs-lookup"><span data-stu-id="f157b-135">The forecast model that was used to generate the forecast.</span></span> <span data-ttu-id="f157b-136">Jos tarkastelet koostetietoja, näet luettelon kaikista menetelmistä, joita on käytetty kaikissa aikasarjojen koosteissa.</span><span class="sxs-lookup"><span data-stu-id="f157b-136">If you're viewing aggregated data, you will see the list of all the methods that were used for all the aggregated time series.</span></span>
-   <span data-ttu-id="f157b-137">Sisäisen mallin tarkkuus (MAPE).</span><span class="sxs-lookup"><span data-stu-id="f157b-137">The internal model accuracy (MAPE).</span></span> <span data-ttu-id="f157b-138">Lisätietoa ennusteen tarkkuudesta on kohdassa [Ennusteen tarkkuuden valvonta](monitor-forecast-accuracy.md).</span><span class="sxs-lookup"><span data-stu-id="f157b-138">For more information about forecast accuracy, see [Monitor forecast accuracy](monitor-forecast-accuracy.md).</span></span>

<span data-ttu-id="f157b-139">**Huomautuksia:**</span><span class="sxs-lookup"><span data-stu-id="f157b-139">**Notes:**</span></span>

-   <span data-ttu-id="f157b-140">Jos otat **Ennustemallin valinnan käyttöön kysynnän ennusteen tiedoissa** ominaisuuksien hallinnasta, voit valita ennustemallit, jotka sisällytetään historialliseen ennusteeseen **Kysynnän ennusteen tiedot** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="f157b-140">If you enable **Forecast model selection on Demand forecast details** from Feature management, you will be able to select the forecast models to be include, for the historical forecast, on the **Demand forecast details** page.</span></span>
-   <span data-ttu-id="f157b-141">Sivun **Ennuste** -kohdassa näkyvä luottamusväli kuvaa luottamusvälin ylärajan ja luottamusvälin alarajan erotusta.</span><span class="sxs-lookup"><span data-stu-id="f157b-141">The confidence interval that appears in the **Forecast** section of the page represents the difference between the confidence interval upper limit and the confidence interval lower limit.</span></span> <span data-ttu-id="f157b-142">Jos haluat nähdä ylärajan ja alarajan arvot, pidä kohdistinta **Historiallinen kysyntä ja ennuste graafisesti** -osiossa olevan kaavion yläpuolella.</span><span class="sxs-lookup"><span data-stu-id="f157b-142">To see the values for the upper and lower limits, hover over the chart in the **Historical demand and forecast graphically** section.</span></span>
-   <span data-ttu-id="f157b-143">Jos käytät kysynnän ennustamisen Microsoft Azuren automaattianalyysiä, voit määrittää luotettavuustasoprosentin, joka luodulla ennusteella tulee olla.</span><span class="sxs-lookup"><span data-stu-id="f157b-143">If you use the Demand forecasting Microsoft Azure Machine Learning, you can specify the confidence level percentage that the forecast that is generated should have.</span></span> <span data-ttu-id="f157b-144">Luottamusväli koostuu arvoalueesta, joka toimii hyvinä ennusteina kysynnän ennusteelle.</span><span class="sxs-lookup"><span data-stu-id="f157b-144">A confidence interval consists of a range of values that act as good estimates for the demand forecast.</span></span> <span data-ttu-id="f157b-145">95 prosentin luotettavuustasoprosentti osoittaa, että on 5 %:n riski, että kysynnän ennuste on luottamusvälin ulkopuolella.</span><span class="sxs-lookup"><span data-stu-id="f157b-145">A 95-percent confidence level percentage indicates that there is a 5-percent risk that the demand forecast falls outside the confidence interval range.</span></span>

<span data-ttu-id="f157b-146">Voit myös tehdä manuaalisia oikaisuja ennusteeseen **Kysynnän ennusteen tiedot** -sivulla muokkaamalla **Ennuste**-rivin arvoja **Ennuste**-osiossa.</span><span class="sxs-lookup"><span data-stu-id="f157b-146">You can also make manual adjustments to the forecast on the **Demand forecast details** page, by modifying the values in the **Forecast** row in the **Forecast** section.</span></span>

<a name="additional-resources"></a><span data-ttu-id="f157b-147">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="f157b-147">Additional resources</span></span>
--------

[<span data-ttu-id="f157b-148">Ennusteen tarkkuuden seuranta</span><span class="sxs-lookup"><span data-stu-id="f157b-148">Monitor forecast accuracy</span></span>](monitor-forecast-accuracy.md)

[<span data-ttu-id="f157b-149">Tilastollisen perusennusteen luominen</span><span class="sxs-lookup"><span data-stu-id="f157b-149">Generate a statistical baseline forecast</span></span>](generate-statistical-baseline-forecast.md)



