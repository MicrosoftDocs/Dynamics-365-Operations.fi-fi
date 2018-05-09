---
title: "Joukkotyöhönottoprojektit"
description: "Henkilöstöhallinnon asiantuntija voi luoda useita toimia ja palkata useita työntekijöitä näihin toimiin joukkotyöhönottoprojektien avulla."
author: rschloma
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: HRMMassHireProject
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations
ms.custom: 7481
ms.assetid: 5f5eb271-76eb-4305-bd1c-5d171dafccc9
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 17789f8f74826136aa5765cadd96a4929729323f
ms.contentlocale: fi-fi
ms.lasthandoff: 05/08/2018

---

# <a name="mass-hire-projects"></a><span data-ttu-id="a7316-103">Joukkotyöhönottoprojektit</span><span class="sxs-lookup"><span data-stu-id="a7316-103">Mass hire projects</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a7316-104">Henkilöstöhallinnon asiantuntija voi luoda useita toimia ja palkata useita työntekijöitä näihin toimiin joukkotyöhönottoprojektien avulla.</span><span class="sxs-lookup"><span data-stu-id="a7316-104">Mass hire projects allow human resources specialists to create multiple positions and efficiently hire workers into those positions.</span></span>

<a name="overview"></a><span data-ttu-id="a7316-105">Yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="a7316-105">Overview</span></span>
--------

<span data-ttu-id="a7316-106">Jos otat työhön samalla kertaa useita työntekijöitä esimerkiksi sesonkitarpeen vuoksi, kannattaa luoda joukkotyöhönottoprojekti.</span><span class="sxs-lookup"><span data-stu-id="a7316-106">Use mass hire projects when you hire multiple workers at one time, such as when you hire to meet a seasonal demand.</span></span> <span data-ttu-id="a7316-107">Joukkotyöhönottoprojektin luominen on kannattavaa, koska voit luoda toimitietueet, työntekijätietueet ja työntekijämääritykset toimille samanaikaisesti.</span><span class="sxs-lookup"><span data-stu-id="a7316-107">Creating a mass hire project is useful because you can create position records, worker records, and worker assignments for positions at the same time.</span></span> <span data-ttu-id="a7316-108">Kun luot toimia joukkotyöhönottoprojektiin, voit määrittää seuraavat tiedot:</span><span class="sxs-lookup"><span data-stu-id="a7316-108">When you create positions for a mass hire project, you can specify the following information:</span></span>
-   <span data-ttu-id="a7316-109">Luotavien toimien määrä</span><span class="sxs-lookup"><span data-stu-id="a7316-109">The number of positions to create</span></span>
-   <span data-ttu-id="a7316-110">Työntekijätyyppi, joita palkkaat toimiin</span><span class="sxs-lookup"><span data-stu-id="a7316-110">The worker type of the people that you will hire for the positions</span></span>
-   <span data-ttu-id="a7316-111">Osasto ja työ, jotka liittyvät toimiin</span><span class="sxs-lookup"><span data-stu-id="a7316-111">The department and the job that are associated with the positions</span></span>
-   <span data-ttu-id="a7316-112">Toimen kokoaikaisuutta vastaava arvo</span><span class="sxs-lookup"><span data-stu-id="a7316-112">The full-time equivalent value of the position</span></span>

## <a name="example"></a><span data-ttu-id="a7316-113">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="a7316-113">Example</span></span>
<span data-ttu-id="a7316-114">Kesällä palkataan yleensä 15-20 osa-aikaista opiskelijaa yrityksen kesäharjoittelupaikkoihin.</span><span class="sxs-lookup"><span data-stu-id="a7316-114">In the summer, you usually hire 15-20 part-time college students to fill available internships in your company.</span></span> <span data-ttu-id="a7316-115">Tänä vuonna haluat palkata viisi kirjanpitäjää, viisi tilauskäsittelijää ja viisi kassanhoitajaa.</span><span class="sxs-lookup"><span data-stu-id="a7316-115">This year, you want to hire five accountants, five order processors, and five cashiers.</span></span> <span data-ttu-id="a7316-116">Sen sijaan, että loisit jokaisen toimi- ja työntekijätietueen erikseen, voit luoda yhden joukkotyöhönottoprojektin nimellä "SummerInterns".</span><span class="sxs-lookup"><span data-stu-id="a7316-116">Instead of creating each position record and worker record separately, you create one mass hire project called “SummerInterns”.</span></span> <span data-ttu-id="a7316-117">Projektin aloitus- ja päättymispäivämäärät vastaavat joukkotyöhönottoprojektille luomiesi toimien aloitus- ja päättymispäivämääriä.</span><span class="sxs-lookup"><span data-stu-id="a7316-117">The project start and end dates correlate with the start and end dates of the position durations for the positions you create for the mass hire project.</span></span> 

<span data-ttu-id="a7316-118">Valitse **Joukkotyöhönottoprojektit** -sivulla "SummerInterns"-projekti ja napsauta sitten **Avaa projekti**.</span><span class="sxs-lookup"><span data-stu-id="a7316-118">In the **Mass hire projects** page, select the “SummerInterns” project and then click **Open project**.</span></span> <span data-ttu-id="a7316-119">Valitse avoimet joukkotyöhönottoprojektissa **Luo toimia** ja kirjoita kirjanpitäjätoimen tiedot.</span><span class="sxs-lookup"><span data-stu-id="a7316-119">In the open mass hire project, click **Create positions** and enter information about the accountant position.</span></span> <span data-ttu-id="a7316-120">Voit määrittää, että viisi kirjanpitäjän toimea on luotava samoilla tiedoilla, ja napsauttaa sitten OK.</span><span class="sxs-lookup"><span data-stu-id="a7316-120">You can indicate that five accountant positions should be created using the same information for each one, and then click OK.</span></span> <span data-ttu-id="a7316-121">Toista nämä vaiheet tilauskäsittelijän ja kassanhoitajan toimille.</span><span class="sxs-lookup"><span data-stu-id="a7316-121">Repeat this process for the order processor and cashier positions.</span></span> 

<span data-ttu-id="a7316-122">Valittuasi kesäharjoittelijoiksi palkattavat opiskelijat, voit syöttää opiskelijoiden tiedot niiden toimien **Toimen tiedot** kohtaan, johon olet kunkin opiskelijan valinnut.</span><span class="sxs-lookup"><span data-stu-id="a7316-122">After selecting students to hire for the internship positions, you'll enter each student’s information in the **Position details** for the position that you're hiring them for.</span></span> <span data-ttu-id="a7316-123">Kun olet syöttänyt kaikkien toimien tiedot, valitse toimi Joukkotyöhönottoprojektit-sivulta ja napsauta sitten **Ota palvelukseen**.</span><span class="sxs-lookup"><span data-stu-id="a7316-123">When you have entered all of the position details, select the position in the Mass hire projects page, and then click **Hire**.</span></span> <span data-ttu-id="a7316-124">Jokaiselle toimelle luodaan toimitietue ja jokaiselle työhön ottamallesi henkilölle luodaan työntekijätietue, joka liitetään asiaankuuluvaan toimeen.</span><span class="sxs-lookup"><span data-stu-id="a7316-124">A position record will be created for each position and a worker record will be created and assigned to the correct position for each person who you hire.</span></span>

## <a name="mass-hire-project-statuses"></a><span data-ttu-id="a7316-125">Joukkotyöhönottoprojektin tilat</span><span class="sxs-lookup"><span data-stu-id="a7316-125">Mass hire project statuses</span></span>
<span data-ttu-id="a7316-126">Joukkotyöhönottoprojektin tila voi olla jokin seuraavista.</span><span class="sxs-lookup"><span data-stu-id="a7316-126">A mass hire project can have the following statuses.</span></span>
-   <span data-ttu-id="a7316-127">Luotu</span><span class="sxs-lookup"><span data-stu-id="a7316-127">Created</span></span>
-   <span data-ttu-id="a7316-128">Avoin</span><span class="sxs-lookup"><span data-stu-id="a7316-128">Open</span></span>
-   <span data-ttu-id="a7316-129">Suljettu</span><span class="sxs-lookup"><span data-stu-id="a7316-129">Closed</span></span>

<span data-ttu-id="a7316-130">Napsauta **Joukkotyöhönottoprojekti**-sivulla **Avaa projekti** tai **Sulje projekti** muuttaaksesi joukkotyöhönottoprojektin tilaa.</span><span class="sxs-lookup"><span data-stu-id="a7316-130">On the **Mass hire project** page, click **Open project** or **Close project** to change the status of a mass hire project.</span></span> <span data-ttu-id="a7316-131">Seuraavassa taulukossa on kuvattu, mitä voit tehdä projektille sen tilan mukaan.</span><span class="sxs-lookup"><span data-stu-id="a7316-131">The following table describes what you can do with a project according to its status.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="a7316-132">Tila</span><span class="sxs-lookup"><span data-stu-id="a7316-132">Status</span></span></th>
<th><span data-ttu-id="a7316-133">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="a7316-133">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a7316-134">Luotu</span><span class="sxs-lookup"><span data-stu-id="a7316-134">Created</span></span></td>
<td><span data-ttu-id="a7316-135">Voit luoda ja muokata tietoja, mutta et luoda toimia projektille.</span><span class="sxs-lookup"><span data-stu-id="a7316-135">You can create and modify information, but cannot create positions for the project.</span></span> <span data-ttu-id="a7316-136">Tämä on uusien projektien oletustila.</span><span class="sxs-lookup"><span data-stu-id="a7316-136">This is the default status for new projects.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a7316-137">Avoin</span><span class="sxs-lookup"><span data-stu-id="a7316-137">Open</span></span></td>
<td><span data-ttu-id="a7316-138">Voit muokata projektin tietoja, luoda toimia joukkotyöhönottoprojektin ja palkata henkilöitä toimiin.</span><span class="sxs-lookup"><span data-stu-id="a7316-138">You can modify the project details, create positions for the mass hire project, and hire people for the positions.</span></span> <span data-ttu-id="a7316-139">Tämä on aktiivisten projektien tila.</span><span class="sxs-lookup"><span data-stu-id="a7316-139">This is the status for active projects.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a7316-140">Suljettu</span><span class="sxs-lookup"><span data-stu-id="a7316-140">Closed</span></span></td>
<td><span data-ttu-id="a7316-141">Et voi lisätä toimia projektiin.</span><span class="sxs-lookup"><span data-stu-id="a7316-141">You cannot add positions to the project.</span></span> <span data-ttu-id="a7316-142">Lisätäksesi toimia joukkotyöhönottoprojektiin, avaa projekti uudelleen.</span><span class="sxs-lookup"><span data-stu-id="a7316-142">To add positions to the mass hire project, open the project again.</span></span> <span data-ttu-id="a7316-143">Tämä on valmiiden projektien tila.</span><span class="sxs-lookup"><span data-stu-id="a7316-143">This is the status for completed projects.</span></span>
<div class="alert">
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="a7316-144"><strong>Huomautus </strong></span><span class="sxs-lookup"><span data-stu-id="a7316-144"><strong>Note</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a7316-145">Ennen joukkotyöhönottoprojektin sulkemista kaikkien projektin toimien tilan on oltava joko Luotu tai Suljettu.</span><span class="sxs-lookup"><span data-stu-id="a7316-145">Before you can close a mass hire project, all positions in the project must have a status of either Created or Closed.</span></span></td>
</tr>
</tbody>
</table>
</div></td>
</tr>
</tbody>
</table>








