---
title: Organisaatiokoulutuksen Power BI -sisältö
description: Tässä ohjeaiheessa käsitellään Finance and Operationsin organisaation koulutuksen Power BI -sisältöä.
author: jcart1106
manager: AnnBe
ms.date: 12/19/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Operations
ms.custom: 263874
ms.assetid: 45dbba14-aba6-4571-be0d-5d1aba3515d9
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 5c9025baccf34195c753fc50ad38cd3016c65b53
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/27/2019
ms.locfileid: "2182965"
---
# <a name="organizational-training-power-bi-content"></a><span data-ttu-id="cf1a1-103">Organisaatiokoulutuksen Power BI -sisältö</span><span class="sxs-lookup"><span data-stu-id="cf1a1-103">Organizational training Power BI content</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cf1a1-104">Tässä ohjeaiheessa käsitellään Finance and Operationsin organisaation koulutuksen Power BI -sisältöä.</span><span class="sxs-lookup"><span data-stu-id="cf1a1-104">This topic describes the Finance and Operations - Organizational training Power BI content.</span></span>

## <a name="reports-that-are-included-in-the-content-pack"></a><span data-ttu-id="cf1a1-105">Raportit, jotka sisältyvät sisältöpakettiin</span><span class="sxs-lookup"><span data-stu-id="cf1a1-105">Reports that are included in the content pack</span></span>
<span data-ttu-id="cf1a1-106">Kun olet liittänyt sisältöpaketin tietoihin, organisaatiosi tiedot näkyvät raporteissa.</span><span class="sxs-lookup"><span data-stu-id="cf1a1-106">After you've connected the content pack to your data, the reports show your organization's data.</span></span> <span data-ttu-id="cf1a1-107">Jos et ole käyttänyt Microsoft Power BI:tä aiemmin, lisätietoja on kohdassa [Power BI:n ohjattu oppiminen](https://powerbi.microsoft.com/guided-learning/?WT.mc_id=PBIService_GetData).</span><span class="sxs-lookup"><span data-stu-id="cf1a1-107">If you've never used Microsoft Power BI before, you can learn more about it on the [Guided Learning page for Power BI](https://powerbi.microsoft.com/guided-learning/?WT.mc_id=PBIService_GetData).</span></span> <span data-ttu-id="cf1a1-108">Raporteissa, jotka sisältyvät sisältöpakettiin, on sekä kaavioita että taulukoita, jotka sisältävät lisätietoja.</span><span class="sxs-lookup"><span data-stu-id="cf1a1-108">The reports that are included in the content pack have both charts and tables that contain additional information.</span></span> <span data-ttu-id="cf1a1-109">Seuraavassa taulukossa kuvataan raportit.</span><span class="sxs-lookup"><span data-stu-id="cf1a1-109">The following table describes the reports.</span></span>

| <span data-ttu-id="cf1a1-110">Raportti</span><span class="sxs-lookup"><span data-stu-id="cf1a1-110">Report</span></span>          | <span data-ttu-id="cf1a1-111">Sisältö</span><span class="sxs-lookup"><span data-stu-id="cf1a1-111">Contents</span></span>                                                                    |
|-----------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="cf1a1-112">Kurssien analysointi</span><span class="sxs-lookup"><span data-stu-id="cf1a1-112">Course Analysis</span></span> | <span data-ttu-id="cf1a1-113">Ilmoittautuminen sijainnin mukaan, kurssin osallistujat tilan mukaan sekä ilmoittautumisluettelo</span><span class="sxs-lookup"><span data-stu-id="cf1a1-113">Registration by location, course attendees by status, and registration list</span></span> |
| <span data-ttu-id="cf1a1-114">Kurssityypit</span><span class="sxs-lookup"><span data-stu-id="cf1a1-114">Course Types</span></span>    | <span data-ttu-id="cf1a1-115">Kurssityypit osaamisalueittain</span><span class="sxs-lookup"><span data-stu-id="cf1a1-115">Course types by skill</span></span>                                                       |

<span data-ttu-id="cf1a1-116">Kaikkien raporttien kaavioita ja ruutuja voi suodattaa sekä kiinnittää koontinäyttöön.</span><span class="sxs-lookup"><span data-stu-id="cf1a1-116">You can filter the charts and tiles on these reports, and pin the charts and tiles to the dashboard.</span></span> <span data-ttu-id="cf1a1-117">Lisätietoja suodattamisesta ja kiinnittämisestä Power BI:ssä on kohdassa [Koontinäytön luominen ja määrittäminen](https://powerbi.microsoft.com/guided-learning/powerbi-learning-4-2-create-configure-dashboards).</span><span class="sxs-lookup"><span data-stu-id="cf1a1-117">For more information about how to filter and pin in Power BI, see [Create and Configure A Dashboard](https://powerbi.microsoft.com/guided-learning/powerbi-learning-4-2-create-configure-dashboards).</span></span>

## <a name="understanding-the-data-model-and-entities"></a><span data-ttu-id="cf1a1-118">Tietomallin ja yksiköiden tiedot</span><span class="sxs-lookup"><span data-stu-id="cf1a1-118">Understanding the data model and entities</span></span>
<span data-ttu-id="cf1a1-119">Sovelluksen tietoja käytetään organisaation koulutuksen sisältöpaketin raporttien täyttämiseen.</span><span class="sxs-lookup"><span data-stu-id="cf1a1-119">Application data is used to populate the reports in the Organizational training content pack.</span></span> <span data-ttu-id="cf1a1-120">Seuraavassa taulukossa on esitetty yksiköt, joihin sisältöpaketti on perustunut.</span><span class="sxs-lookup"><span data-stu-id="cf1a1-120">The following table shows the entities that the content pack was based on.</span></span>

| <span data-ttu-id="cf1a1-121">Kokonaisuus</span><span class="sxs-lookup"><span data-stu-id="cf1a1-121">Entity</span></span>                    | <span data-ttu-id="cf1a1-122">Sisältö</span><span class="sxs-lookup"><span data-stu-id="cf1a1-122">Contents</span></span>                                                         | <span data-ttu-id="cf1a1-123">Suhteet muihin yksiköihin</span><span class="sxs-lookup"><span data-stu-id="cf1a1-123">Relationships with other entities</span></span> |
|---------------------------|------------------------------------------------------------------|-----------------------------------|
| <span data-ttu-id="cf1a1-124">Training\_CalendarOffset</span><span class="sxs-lookup"><span data-stu-id="cf1a1-124">Training\_CalendarOffset</span></span>  | <span data-ttu-id="cf1a1-125">Kalenterin siirtymät raporttien osittamiseen</span><span class="sxs-lookup"><span data-stu-id="cf1a1-125">Calendar offsets to slice reports</span></span>                                | <span data-ttu-id="cf1a1-126">Training\_CourseAgenda, Training\_CourseAttendees</span><span class="sxs-lookup"><span data-stu-id="cf1a1-126">Training\_CourseAgenda, Training\_CourseAttendees</span></span> |
| <span data-ttu-id="cf1a1-127">Training\_Company</span><span class="sxs-lookup"><span data-stu-id="cf1a1-127">Training\_Company</span></span>         | <span data-ttu-id="cf1a1-128">Yritykset, joiden mukaan raportit suodatetaan</span><span class="sxs-lookup"><span data-stu-id="cf1a1-128">Companies to filter reports by</span></span>                                   | <span data-ttu-id="cf1a1-129">Training\_CourseAgenda, Training\_CourseAttendees</span><span class="sxs-lookup"><span data-stu-id="cf1a1-129">Training\_CourseAgenda, Training\_CourseAttendees</span></span> |
| <span data-ttu-id="cf1a1-130">Training\_Course</span><span class="sxs-lookup"><span data-stu-id="cf1a1-130">Training\_Course</span></span>          | <span data-ttu-id="cf1a1-131">Kurssi, kuvaus, opettajan nimi, sijainti, huone ja tila</span><span class="sxs-lookup"><span data-stu-id="cf1a1-131">Course, description, instructor name, location, room, and status</span></span> | <span data-ttu-id="cf1a1-132">Training\_CourseAgenda, Training\_CourseAttendees, Training\_CourseSkill</span><span class="sxs-lookup"><span data-stu-id="cf1a1-132">Training\_CourseAgenda, Training\_CourseAttendees, Training\_CourseSkill</span></span> |
| <span data-ttu-id="cf1a1-133">Training\_CourseAgenda</span><span class="sxs-lookup"><span data-stu-id="cf1a1-133">Training\_CourseAgenda</span></span>    | <span data-ttu-id="cf1a1-134">Esityslista, kurssi sekä aloitus- ja lopetusajat</span><span class="sxs-lookup"><span data-stu-id="cf1a1-134">Agenda, course, and start and end times</span></span>                          | <span data-ttu-id="cf1a1-135">Training\_Company, Training\_CalendarOffset, Training\_Date, Training\_Course</span><span class="sxs-lookup"><span data-stu-id="cf1a1-135">Training\_Company, Training\_CalendarOffset, Training\_Date, Training\_Course</span></span> |
| <span data-ttu-id="cf1a1-136">Training\_CourseAttendees</span><span class="sxs-lookup"><span data-stu-id="cf1a1-136">Training\_CourseAttendees</span></span> | <span data-ttu-id="cf1a1-137">Nimi, tila, työ ja rekisteröinnin päivämäärä</span><span class="sxs-lookup"><span data-stu-id="cf1a1-137">Name, status, job, and registration date</span></span>                         | <span data-ttu-id="cf1a1-138">Training\_Company, Training\_CalendarOffset, Training\_Date, Training\_Demographics, Training\_Employment, Training\_Course, Training\_WorkerName, Training\_WorkerTitle, Training\_Job, Training\_Position</span><span class="sxs-lookup"><span data-stu-id="cf1a1-138">Training\_Company, Training\_CalendarOffset, Training\_Date, Training\_Demographics, Training\_Employment, Training\_Course, Training\_WorkerName, Training\_WorkerTitle, Training\_Job, Training\_Position</span></span> |
| <span data-ttu-id="cf1a1-139">Training\_CourseSkill</span><span class="sxs-lookup"><span data-stu-id="cf1a1-139">Training\_CourseSkill</span></span>     | <span data-ttu-id="cf1a1-140">Taito, osaamisalueen tyyppi ja taso</span><span class="sxs-lookup"><span data-stu-id="cf1a1-140">Skill, skill type, and level</span></span>                                     | <span data-ttu-id="cf1a1-141">Training\_Course</span><span class="sxs-lookup"><span data-stu-id="cf1a1-141">Training\_Course</span></span> |
| <span data-ttu-id="cf1a1-142">Training\_Date</span><span class="sxs-lookup"><span data-stu-id="cf1a1-142">Training\_Date</span></span>            | <span data-ttu-id="cf1a1-143">Päiviä, viikkoja, kuukausia ja vuosia</span><span class="sxs-lookup"><span data-stu-id="cf1a1-143">Days, weeks, months, and years</span></span>                                   | <span data-ttu-id="cf1a1-144">Training\_CourseAgenda, Training\_CourseAttendees</span><span class="sxs-lookup"><span data-stu-id="cf1a1-144">Training\_CourseAgenda, Training\_CourseAttendees</span></span> |
| <span data-ttu-id="cf1a1-145">Training\_Demographics</span><span class="sxs-lookup"><span data-stu-id="cf1a1-145">Training\_Demographics</span></span>    | <span data-ttu-id="cf1a1-146">Syntymäaika, sukupuoli, etninen alkuperä ja siviilisääty</span><span class="sxs-lookup"><span data-stu-id="cf1a1-146">Date of birth, gender, ethnic origin, and marital status</span></span>         | <span data-ttu-id="cf1a1-147">Training\_CourseAgenda, Training\_CourseAttendees</span><span class="sxs-lookup"><span data-stu-id="cf1a1-147">Training\_CourseAgenda, Training\_CourseAttendees</span></span> |
| <span data-ttu-id="cf1a1-148">Training\_Employment</span><span class="sxs-lookup"><span data-stu-id="cf1a1-148">Training\_Employment</span></span>      | <span data-ttu-id="cf1a1-149">Alkamispäivämäärä, päättymispäivämäärä ja siirtymispäivämäärä</span><span class="sxs-lookup"><span data-stu-id="cf1a1-149">Start date, end date, and transition date</span></span>                        | <span data-ttu-id="cf1a1-150">Training\_CourseAgenda, Training\_CourseAttendees</span><span class="sxs-lookup"><span data-stu-id="cf1a1-150">Training\_CourseAgenda, Training\_CourseAttendees</span></span> |
| <span data-ttu-id="cf1a1-151">Training\_Job</span><span class="sxs-lookup"><span data-stu-id="cf1a1-151">Training\_Job</span></span>             | <span data-ttu-id="cf1a1-152">Tehtävä, tyyppi ja nimike</span><span class="sxs-lookup"><span data-stu-id="cf1a1-152">Function, type, and title</span></span>                                        | <span data-ttu-id="cf1a1-153">Training\_CourseAgenda, Training\_CourseAttendees</span><span class="sxs-lookup"><span data-stu-id="cf1a1-153">Training\_CourseAgenda, Training\_CourseAttendees</span></span> |
| <span data-ttu-id="cf1a1-154">Training\_Position</span><span class="sxs-lookup"><span data-stu-id="cf1a1-154">Training\_Position</span></span>        | <span data-ttu-id="cf1a1-155">Toimi, nimike ja kokopäiväistä vastaavat (FTE)</span><span class="sxs-lookup"><span data-stu-id="cf1a1-155">Position, title, and full-time equivalent (FTE)</span></span>                  | <span data-ttu-id="cf1a1-156">Training\_CourseAgenda, Training\_CourseAttendees</span><span class="sxs-lookup"><span data-stu-id="cf1a1-156">Training\_CourseAgenda, Training\_CourseAttendees</span></span> |
| <span data-ttu-id="cf1a1-157">Training\_WorkerName</span><span class="sxs-lookup"><span data-stu-id="cf1a1-157">Training\_WorkerName</span></span>      | <span data-ttu-id="cf1a1-158">Etunimi , sukunimi ja koko nimi</span><span class="sxs-lookup"><span data-stu-id="cf1a1-158">First name, last name, and full name</span></span>                             | <span data-ttu-id="cf1a1-159">Training\_CourseAttendees</span><span class="sxs-lookup"><span data-stu-id="cf1a1-159">Training\_CourseAttendees</span></span> |
| <span data-ttu-id="cf1a1-160">Training\_WorkerTitle</span><span class="sxs-lookup"><span data-stu-id="cf1a1-160">Training\_WorkerTitle</span></span>     | <span data-ttu-id="cf1a1-161">Nimike ja virkaikä</span><span class="sxs-lookup"><span data-stu-id="cf1a1-161">Title and seniority date</span></span>                                         | <span data-ttu-id="cf1a1-162">Training\_CourseAttendees</span><span class="sxs-lookup"><span data-stu-id="cf1a1-162">Training\_CourseAttendees</span></span> |