---
title: Projektiresurssin ajoituksen suorituskyky
description: Tässä ohjeaiheessa on tietoja suurten projektimäärien resurssien ajoituksen suorituskyvyn parantamisesta.
author: Yowelle
manager: AnnBe
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 10.0.14
ms.search.validFrom: 2020-09-01
ms.openlocfilehash: 988fc83230f08a6534caa7c37784757d73c1cc12
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760539"
---
# <a name="project-resource-scheduling-performance"></a><span data-ttu-id="2e1e5-103">Projektiresurssin ajoituksen suorituskyky</span><span class="sxs-lookup"><span data-stu-id="2e1e5-103">Project resource scheduling performance</span></span>

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]


<span data-ttu-id="2e1e5-104">Resurssien ajoitukseen liittyviä suorituskykyongelmia voi esiintyä, jos projekteja on tuhansia.</span><span class="sxs-lookup"><span data-stu-id="2e1e5-104">Performance issues related to resource scheduling can occur when the number of projects reaches into the thousands.</span></span> <span data-ttu-id="2e1e5-105">Resurssien ajoituksen suorituskyvyn parantamiseksi on käytettävissä ominaisuus, jonka avulla käyttäjät voivat vähentää resurssin käytettävyyslomakkeen käynnistykseen kuluvaa aikaa.</span><span class="sxs-lookup"><span data-stu-id="2e1e5-105">To improve resource scheduling performance, a feature is available that allows users to reduce the time that it takes to launch the resource availability form.</span></span> <span data-ttu-id="2e1e5-106">Tämä poistaa erityisesti resurssin kapasiteetin koonnin synkronointiprosessia ja nopeuttaa resurssin hakua käyttämällä **ResProjectResource**-taulua.</span><span class="sxs-lookup"><span data-stu-id="2e1e5-106">Specifically, this removes the resource capacity roll-up synchronization process and uses the **ResProjectResource** table to speed up the resource lookup.</span></span> <span data-ttu-id="2e1e5-107">Huomaa, että **ResRollup**-taulua ei enää käytetä.</span><span class="sxs-lookup"><span data-stu-id="2e1e5-107">Note that the **ResRollup** table will no longer be used.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2e1e5-108">Jos resurssin kapasiteetin koonnin synkronointiprosessissa tai **ResProjectResource**-taulussa on riipppuvuus, älä käytä tätä ominaisuutta.</span><span class="sxs-lookup"><span data-stu-id="2e1e5-108">If there is a dependency on either the resource capacity roll-up synchronization process or the **ResProjectResource** table, do not use this feature.</span></span>

## <a name="enable-resource-scheduling-performance-enhancement"></a><span data-ttu-id="2e1e5-109">Resurssin ajoituksen suorituskyvyn parantamisen ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="2e1e5-109">Enable resource scheduling performance enhancement</span></span>
<span data-ttu-id="2e1e5-110">Voit ottaa resurssien aikataulutuksen suorituskyvyn parantamisen käyttöön seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="2e1e5-110">To enable resource scheduling performance enhancement, complete the following steps.</span></span>

1. <span data-ttu-id="2e1e5-111">Siirry kohtaan **Ominaisuuksien hallinta** > **Kaikki** ja etsi ominaisuusluettelosta **Resurssin ajoituksen suorituskyvyn parantamisen ottaminen käyttöön** -ominaisuus.</span><span class="sxs-lookup"><span data-stu-id="2e1e5-111">Go to **Feature management** > **All**, and in the feature list, locate **Enable project resource scheduling performance enhancement feature**.</span></span>
2. <span data-ttu-id="2e1e5-112">Valitse **Ota käyttöön nyt**.</span><span class="sxs-lookup"><span data-stu-id="2e1e5-112">Select **Enable now**.</span></span>

> [!NOTE]
> <span data-ttu-id="2e1e5-113">Jos et löydä ominaisuutta luettelosta, päivitä luettelo valitsemalla **Tarkista päivitykset**.</span><span class="sxs-lookup"><span data-stu-id="2e1e5-113">If you can't find the feature in the list, select **Check for updates** to refresh the list.</span></span>

3. <span data-ttu-id="2e1e5-114">Päivitä selain ja siirry kohtaan **Projektinhallinta ja kirjanpito** > **Kausittainen** > **Projektiresurssit** > **Synkronoi resurssikalenterien kapasiteetti kaikissa yrityksissä**.</span><span class="sxs-lookup"><span data-stu-id="2e1e5-114">Refresh your browser, and then go to **Project management and accounting** > **Periodic** > **Project resources** > **Synchronize resource calendars capacity across all companies**.</span></span>
4. <span data-ttu-id="2e1e5-115">Määritä **Poista olemassa olevat kapasiteettitietueet** -kohdan arvoksi **Kyllä**, jos haluat poistaa aiemmat tiedot.</span><span class="sxs-lookup"><span data-stu-id="2e1e5-115">Set **Remove existing capacity records** to **Yes** to remove previous data.</span></span> <span data-ttu-id="2e1e5-116">Jos haluat luoda lisää tietoja, määritä arvoksi **Ei**.</span><span class="sxs-lookup"><span data-stu-id="2e1e5-116">If you want generate incremental data, set it to **No**.</span></span>
5. <span data-ttu-id="2e1e5-117">Valitse **Kausikoodi**-kentässä kausi, jolle tietoja luodaan.</span><span class="sxs-lookup"><span data-stu-id="2e1e5-117">In the **Period code** field, select the period in which data should be generated.</span></span> <span data-ttu-id="2e1e5-118">Jos valitset kausikoodin, aloitus- ja päättymispäivämäärää ei tarvitse määrittää.</span><span class="sxs-lookup"><span data-stu-id="2e1e5-118">If you select a period code, a start and end date do not need to be defined.</span></span>
6. <span data-ttu-id="2e1e5-119">Jos jätät **Kausikoodi**-kentän tyhjäksi, valitse tietyt aloitus- ja päättymispäivämäärät tietojen luontia varten.</span><span class="sxs-lookup"><span data-stu-id="2e1e5-119">If you leave the **Period code** field blank, select specific start and end dates to generate data.</span></span>
7. <span data-ttu-id="2e1e5-120">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="2e1e5-120">Select **OK**.</span></span>

 > [!NOTE]
 > <span data-ttu-id="2e1e5-121">Tämä jakaa yleiset tiedot **ResCalendarCapacity**-tauluun ympäristön kaikissa yrityksissä. Tällöin erätyö on suoritettava vain yhdessä yrityksessä.</span><span class="sxs-lookup"><span data-stu-id="2e1e5-121">This will distribute general data to the **ResCalendarCapacity** table across all companies in your environment, so the batch job only needs to be run in one legal entity.</span></span> <span data-ttu-id="2e1e5-122">Tämän erätyön tietoja tarvitaan laskettaessa resurssikapasiteetti liittyvän kalenterin avulla.</span><span class="sxs-lookup"><span data-stu-id="2e1e5-122">The data in this batch job is needed to calculate resource capacity through the associated calendar.</span></span>

8. <span data-ttu-id="2e1e5-123">Siirry kohtaan **Projektinhallinta ja kirjanpito** > **Kausittainen** > **Projektiresurssit** > **Täytä projektiresurssit kaikissa yrityksissä** ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="2e1e5-123">Go to **Project management and accounting** > **Periodic** > **Project resources** > **Populate project resources across all companies** and then select **OK**.</span></span> <span data-ttu-id="2e1e5-124">Tämä on tietojen päivityskomentosarja yleisiä tietoja varten **ResProjectResource**-, **ResCalendarDateTimeRange**- ja **ResEffectiveDateTimeRange**-tauluissa.</span><span class="sxs-lookup"><span data-stu-id="2e1e5-124">This is the data upgrade script for general data in the **ResProjectResource**, **ResCalendarDateTimeRange**, and **ResEffectiveDateTimeRange** tables.</span></span> <span data-ttu-id="2e1e5-125">**PSAPRojSchedRole.RootActivity**-kentän arvot päivitetään myös.</span><span class="sxs-lookup"><span data-stu-id="2e1e5-125">Values for the **PSAPRojSchedRole.RootActivity** field are also updated.</span></span> <span data-ttu-id="2e1e5-126">Jos tätä ei suoriteta, näyttöön tulee varoitus, kun yrität suorittaa resurssien ajoituksen toimintoja.</span><span class="sxs-lookup"><span data-stu-id="2e1e5-126">If this is not run, you will receive a warning when you try to execute resource scheduling operations.</span></span>
 
## <a name="turn-off-resource-scheduling-performance-enhancement"></a><span data-ttu-id="2e1e5-127">Resurssin ajoituksen suorituskyvyn parantamisen poistaminen käytöstä</span><span class="sxs-lookup"><span data-stu-id="2e1e5-127">Turn off resource scheduling performance enhancement</span></span>

1. <span data-ttu-id="2e1e5-128">Siirry kohtaan **Ominaisuuksien hallinta** > **Kaikki** ja hae ominaisuusluettelosta **Resurssin ajoituksen suorituskyvyn parantamisen ottaminen käyttöön** -ominaisuus.</span><span class="sxs-lookup"><span data-stu-id="2e1e5-128">Go to **Feature management** > **All**  and search for **Enable project resource scheduling performance enhancement feature**.</span></span>
2. <span data-ttu-id="2e1e5-129">Valitse ominaisuus ja valitse sitten **Poista käytöstä** -painike.</span><span class="sxs-lookup"><span data-stu-id="2e1e5-129">Select the feature, and then select the **Disable** button.</span></span>
3. <span data-ttu-id="2e1e5-130">Päivitä selain.</span><span class="sxs-lookup"><span data-stu-id="2e1e5-130">Refresh your browser.</span></span>
4. <span data-ttu-id="2e1e5-131">Siirry kohtaan **Projektinhallinta ja kirjanpito** > **Kausittainen** > **Kapasiteetin synkronointi** > **Synkronoi resurssin kapasiteetin koonnit**.</span><span class="sxs-lookup"><span data-stu-id="2e1e5-131">Go to **Project management and accounting** > **Periodic** > **Capacity synchronization** > **Synchronize resource capacity roll-ups**.</span></span>
5. <span data-ttu-id="2e1e5-132">Määritä **Kapasiteetin koonnin synkronointi** -sivulla **Poista olemassa olevat kapasiteettitietueet** -kohdan arvoksi **Kyllä**, jos haluat poistaa aiemmat tiedot.</span><span class="sxs-lookup"><span data-stu-id="2e1e5-132">On the **Capacity roll-up synchronization** page, set **Remove existing capacity records** to **Yes** to remove previous data.</span></span> <span data-ttu-id="2e1e5-133">Jos haluat luoda lisää tietoja, määritä arvoksi **Ei**.</span><span class="sxs-lookup"><span data-stu-id="2e1e5-133">If you want to generate incremental data, set it to **No**.</span></span>
6. <span data-ttu-id="2e1e5-134">Valitse **Kausikoodi**-kentässä kausi, jolle tietoja luodaan.</span><span class="sxs-lookup"><span data-stu-id="2e1e5-134">In the **Period code** field, select the period in which data should be generated.</span></span> <span data-ttu-id="2e1e5-135">Jos valitset kausikoodin, aloitus- ja päättymispäivämäärää ei tarvitse määrittää.</span><span class="sxs-lookup"><span data-stu-id="2e1e5-135">If you select a period code, a start and end date do not need to be defined.</span></span>
7. <span data-ttu-id="2e1e5-136">Jos jätät **Kausikoodi**-kentän tyhjäksi, valitse tietyt aloitus- ja päättymispäivämäärät tietojen luontia varten.</span><span class="sxs-lookup"><span data-stu-id="2e1e5-136">If you leave the **Period code** field blank, select specific start and end dates to generate data.</span></span>
8. <span data-ttu-id="2e1e5-137">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="2e1e5-137">Select **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="2e1e5-138">Tämä jakaa yleiset tiedot **ResRollup**-tauluun ympäristön kaikissa yrityksissä. Tällöin erätyö on suoritettava vain yhdessä yrityksessä.</span><span class="sxs-lookup"><span data-stu-id="2e1e5-138">This will distribute general data to the **ResRollup** table across all companies in your environment, so the batch job only needs to be run in one legal entity.</span></span> <span data-ttu-id="2e1e5-139">Tätä erätyötä tarvitaan kaikissa **Resurssin saatavuus** -näkymissä.</span><span class="sxs-lookup"><span data-stu-id="2e1e5-139">This batch job is needed for all **Resource Availability** views.</span></span> <span data-ttu-id="2e1e5-140">Jos tätä eräajoa ei suoriteta, **ResRollup**-tiedot luodaan prosessien aikana. Tämä voi kestää kauan.</span><span class="sxs-lookup"><span data-stu-id="2e1e5-140">If this batch job is not run, the **ResRollup** data will be generated on the fly, which can take time.</span></span>
