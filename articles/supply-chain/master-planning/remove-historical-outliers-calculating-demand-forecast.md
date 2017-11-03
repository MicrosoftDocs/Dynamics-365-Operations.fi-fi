---
title: Poista poikkeavat tiedot aiemmista tapahtumatiedoista laskettaessa ennustetarvetta
description: "Tässä artikkelissa käsitellään, miten poikkeavat arvot suljetaan pois kysynnän ennusteen laskemiseen käytettävistä historiatiedoista. Voit parantaa ennusteen tarkkuuta jättämällä poikkeavat arvot pois."
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqDemPlanForecastParameters, ReqDemPlanOutlierQuerySetup
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 72621
ms.assetid: 88a964af-14eb-4c5c-945b-388e5908362c
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 714a892ff4c168ee3ba1cefd25ae18345af5631b
ms.contentlocale: fi-fi
ms.lasthandoff: 11/03/2017

---

# <a name="remove-outliers-from-historical-transaction-data-when-calculating-a-demand-forecast"></a><span data-ttu-id="07934-104">Poista poikkeavat tiedot aiemmista tapahtumatiedoista laskettaessa ennustetarvetta</span><span class="sxs-lookup"><span data-stu-id="07934-104">Remove outliers from historical transaction data when calculating a demand forecast</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="07934-105">Tässä artikkelissa käsitellään, miten poikkeavat arvot suljetaan pois kysynnän ennusteen laskemiseen käytettävistä historiatiedoista.</span><span class="sxs-lookup"><span data-stu-id="07934-105">This article describes how to exclude outliers from the historical data that is used to calculate a demand forecast.</span></span> <span data-ttu-id="07934-106">Voit parantaa ennusteen tarkkuuta jättämällä poikkeavat arvot pois.</span><span class="sxs-lookup"><span data-stu-id="07934-106">By excluding outliers, you can improve forecast accuracy.</span></span>

<span data-ttu-id="07934-107">Voit parantaa ennusteen tarkkuuta jättämällä poikkeavat arvot pois.</span><span class="sxs-lookup"><span data-stu-id="07934-107">You can exclude outliers to improve forecast accuracy.</span></span> <span data-ttu-id="07934-108">Tämä tehtävä on valinnainen.</span><span class="sxs-lookup"><span data-stu-id="07934-108">This is an optional task.</span></span> <span data-ttu-id="07934-109">Prosessin yhteenveto:</span><span class="sxs-lookup"><span data-stu-id="07934-109">Here is an overview of the process:</span></span>

1.  <span data-ttu-id="07934-110">Voit avata **Poikkeavan arvon poistaminen** -sivun valitsemalla **Pääsuunnittelu** &gt; **Asetukset** &gt; **Kysynnän ennuste** &gt; **Poikkeavan arvon poistaminen**. Voit valita poistettavat tapahtumat tällä sivulla tekemällä kyselyjä.</span><span class="sxs-lookup"><span data-stu-id="07934-110">Click **Master planning** &gt; **Setup** &gt; **Demand forecasting** &gt; **Outlier removal** to open the **Outlier removal** page, where you can use a query to select the transactions to exclude.</span></span>
2.  <span data-ttu-id="07934-111">Valitse yritys, jota kysely koskee, ja sitten anna nimi ja kuvaus.</span><span class="sxs-lookup"><span data-stu-id="07934-111">Select the company that the query applies to, and then enter a name and description.</span></span> <span data-ttu-id="07934-112">**Kyselyn päivämäärä** -kenttään valitaan automaattisesti nykyinen päivämäärä.</span><span class="sxs-lookup"><span data-stu-id="07934-112">The **Query date** field is automatically set to the current date.</span></span>
3.  <span data-ttu-id="07934-113">Valitsemalla **Aktiivinen**-valintaruudun voit jättää historiallisista tiedoista pois kyselyyn sisältyvät tapahtumat.</span><span class="sxs-lookup"><span data-stu-id="07934-113">Select the **Active** check box to exclude the transactions that the query finds from the historical data.</span></span> <span data-ttu-id="07934-114">Tämä asetus tulee voimaan, kun luot perusennusteen.</span><span class="sxs-lookup"><span data-stu-id="07934-114">This setting will take effect when you create a baseline forecast.</span></span>
4.  <span data-ttu-id="07934-115">Voit lisätä, poistaa ja valita **Poikkeavan arvon kysely** -sivulla ehtoja, jotka määrittävät mitkä tapahtumat jätetään pois perusennusteen laskennasta.</span><span class="sxs-lookup"><span data-stu-id="07934-115">On the **Outlier removal query** page, you can add, remove, and select the criteria that define which transactions will be excluded when the baseline forecast is calculated.</span></span> <span data-ttu-id="07934-116">Valitse esimerkiksi tietty nimike tai tilaus, jonka haluat sulkea pois.</span><span class="sxs-lookup"><span data-stu-id="07934-116">For example, select a specific item or order transaction to exclude.</span></span>
5.  <span data-ttu-id="07934-117">Valitse **Näytä tapahtumat**.</span><span class="sxs-lookup"><span data-stu-id="07934-117">Click **Display transactions**.</span></span> <span data-ttu-id="07934-118">**Poikkeavan arvon tapahtumat** -sivulla on luettelo tapahtumista, jotka vastaavat kyselyssä määritettyä ehtoa ja jotka suljetaan pois historiatiedoista, kun kysynnän ennuste lasketaan.</span><span class="sxs-lookup"><span data-stu-id="07934-118">The **Outlier transactions** page lists the transactions that meet the criteria that you defined in the query, and that will be excluded from the historical data when the demand forecast is calculated.</span></span>

<span data-ttu-id="07934-119">**Huomautus:** Voit luoda myös kyselyn, joka perustuu aiemmin luotuun kyselyyn.</span><span class="sxs-lookup"><span data-stu-id="07934-119">**Note:** You can also create a query that is based on an existing query.</span></span> <span data-ttu-id="07934-120">Valitse kysely, jonka haluat kopioida, ja valitse sitten **Monista**.</span><span class="sxs-lookup"><span data-stu-id="07934-120">Select the query to copy, and then click **Duplicate**.</span></span> <span data-ttu-id="07934-121">**Kyselyn päivämäärä** -kenttä ilmaisee version.</span><span class="sxs-lookup"><span data-stu-id="07934-121">The **Query date** field identifies the version.</span></span> <span data-ttu-id="07934-122">Voit käyttää kyselyä sellaisenaan tai muokata ehtoja valitsemalla **Muokkaa kyselyä**.</span><span class="sxs-lookup"><span data-stu-id="07934-122">You can use the query as it is, or you can click **Edit query** to modify the criteria.</span></span> <span data-ttu-id="07934-123">Voit halutessasi muokata uuden kyselyn nimeä ja kuvausta.</span><span class="sxs-lookup"><span data-stu-id="07934-123">You can optionally modify the name and description of the new query.</span></span>

<a name="see-also"></a><span data-ttu-id="07934-124">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="07934-124">See also</span></span>
--------

[<span data-ttu-id="07934-125">Kysynnän ennusteen esittely</span><span class="sxs-lookup"><span data-stu-id="07934-125">Introduction to demand forecasting</span></span>](introduction-demand-forecasting.md)

[<span data-ttu-id="07934-126">Ennusteen tarkkuuden valvonta</span><span class="sxs-lookup"><span data-stu-id="07934-126">Monitoring forecast accuracy</span></span>](monitor-forecast-accuracy.md)




