---
title: Määritä koulutuskursseja
description: Henkilöstöhallinnon järjestelmänvalvojat ja esimiehet voivat ylläpitää tietoja työntekijöille tarjottavista kursseista kurssitoiminnoilla.
author: andreabichsel
manager: AnnBe
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: HcmCourseType, HcmCourseTypeGroup, HRMCourseTable
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.custom: 7532
ms.assetid: a6950c29-8b3e-45b2-9084-ddfb1317ffaa
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.openlocfilehash: c68601b150e5c0963bfba0fa1c6c866abdd092cb
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/06/2019
ms.locfileid: "2898870"
---
# <a name="set-up-training-courses"></a><span data-ttu-id="ef91f-103">Määritä koulutuskursseja</span><span class="sxs-lookup"><span data-stu-id="ef91f-103">Set up training courses</span></span>

<span data-ttu-id="ef91f-104">Henkilöstöhallinnon järjestelmänvalvojat ja esimiehet voivat ylläpitää tietoja työntekijöille tarjottavista kursseista kurssitoiminnoilla.</span><span class="sxs-lookup"><span data-stu-id="ef91f-104">Human resources administrators and managers can use the courses features to maintain information about the training that's offered to workers.</span></span>

 <a name="set-up-prerequisites"></a><span data-ttu-id="ef91f-105"> Määritä edellytykset</span><span class="sxs-lookup"><span data-stu-id="ef91f-105">Set up prerequisites</span></span>
---------------------

<span data-ttu-id="ef91f-106">Seuraavat tiedot ovat pakollisia, ja ne on määritettävä ennen kurssien luontia.</span><span class="sxs-lookup"><span data-stu-id="ef91f-106">The following information is required and must be set up before you create courses.</span></span>
-   <span data-ttu-id="ef91f-107">**Kurssityypit**</span><span class="sxs-lookup"><span data-stu-id="ef91f-107">**Course types**</span></span>

<span data-ttu-id="ef91f-108">Seuraavat tiedot ovat valinnaisia, jotka voit halutessasi määrittää kursseille.</span><span class="sxs-lookup"><span data-stu-id="ef91f-108">The following information is optional information that you can specify for courses.</span></span> <span data-ttu-id="ef91f-109">Jos tiedät, että kirjoitat kursseille nämä tiedot, sinun on määritettävä nämä tiedot, ennen kuin voit luoda kurssin tietueita.</span><span class="sxs-lookup"><span data-stu-id="ef91f-109">If you know that you will be entering this information for courses, you should set up this information before you create course records.</span></span>
-   <span data-ttu-id="ef91f-110">**Luokkahuoneryhmät**</span><span class="sxs-lookup"><span data-stu-id="ef91f-110">**Classroom groups**</span></span>
-   <span data-ttu-id="ef91f-111">**Kurssiryhmät**</span><span class="sxs-lookup"><span data-stu-id="ef91f-111">**Course groups**</span></span>
-   <span data-ttu-id="ef91f-112">**Kurssipaikat**</span><span class="sxs-lookup"><span data-stu-id="ef91f-112">**Course locations**</span></span>
-   <span data-ttu-id="ef91f-113">**Luokkahuoneet**</span><span class="sxs-lookup"><span data-stu-id="ef91f-113">**Classrooms**</span></span>
-   <span data-ttu-id="ef91f-114">**Opettajat**</span><span class="sxs-lookup"><span data-stu-id="ef91f-114">**Instructors**</span></span>

## <a name="course-types"></a><span data-ttu-id="ef91f-115">Kurssityypit</span><span class="sxs-lookup"><span data-stu-id="ef91f-115">Course types</span></span>
<span data-ttu-id="ef91f-116">Voit käyttää kurssityyppejä kurssien luokittelemiseen kurssin rakenteen tai sisällön perusteella.</span><span class="sxs-lookup"><span data-stu-id="ef91f-116">You can use course types to categorize courses according to the structure or content of the course.</span></span> <span data-ttu-id="ef91f-117">Voit luoda kurssityyppejä **Kurssityypit**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="ef91f-117">You can create course types on the **Course types** page.</span></span> <span data-ttu-id="ef91f-118">Sinun on valittava kurssityyppi, kun luot kurssitietueen.</span><span class="sxs-lookup"><span data-stu-id="ef91f-118">You must select a course type when you create a course record.</span></span>

## <a name="course-setup-type"></a><span data-ttu-id="ef91f-119">Kurssin asetustyyppi</span><span class="sxs-lookup"><span data-stu-id="ef91f-119">Course setup type</span></span>
<span data-ttu-id="ef91f-120">Seuraavassa taulukossa luetellaan kurssien kolme asetustyyppiä.</span><span class="sxs-lookup"><span data-stu-id="ef91f-120">The following table lists the three setup types for courses.</span></span> <span data-ttu-id="ef91f-121">Kurssin rakenteen määrittävät asetustyypit.</span><span class="sxs-lookup"><span data-stu-id="ef91f-121">Setup types determine the structure of the course.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="ef91f-122">Asetustyyppi</span><span class="sxs-lookup"><span data-stu-id="ef91f-122">Setup type</span></span></th>
<th><span data-ttu-id="ef91f-123">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="ef91f-123">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ef91f-124"><strong>Vakio</strong></span><span class="sxs-lookup"><span data-stu-id="ef91f-124"><strong>Standard</strong></span></span></td>
<td><span data-ttu-id="ef91f-125">Valitse tämä tyyppi kursseille, joille ei ole määritetty päivittäistä työjärjestystä.</span><span class="sxs-lookup"><span data-stu-id="ef91f-125">Select this type for courses that will not have a daily agenda.</span></span> <span data-ttu-id="ef91f-126">Tämä on oletusarvoinen asetustyyppi, kun luot uuden kurssin.</span><span class="sxs-lookup"><span data-stu-id="ef91f-126">This is the default setup type when you create a new course.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ef91f-127"><strong>Työjärjestys</strong></span><span class="sxs-lookup"><span data-stu-id="ef91f-127"><strong>Agenda</strong></span></span></td>
<td><span data-ttu-id="ef91f-128">Valitsemalla tämän tyypin voit suunnitella useita päiviä kestävän kurssin eri päivien sisällön.</span><span class="sxs-lookup"><span data-stu-id="ef91f-128">Select this type to plan the details of each day of a course that takes place over multiple days.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ef91f-129"><strong>Työjärjestys ja istunto</strong></span><span class="sxs-lookup"><span data-stu-id="ef91f-129"><strong>Agenda + session</strong></span></span></td>
<td><span data-ttu-id="ef91f-130">Valitse tämä laji monimutkaisemmille kursseille.</span><span class="sxs-lookup"><span data-stu-id="ef91f-130">Select this type for the more complex courses.</span></span> <span data-ttu-id="ef91f-131">Voit esimerkiksi jakaa kurssin ohjelman kappaleisiin ja istuntoihin.</span><span class="sxs-lookup"><span data-stu-id="ef91f-131">For example, you can divide the agenda for the course into tracks and sessions.</span></span>
<ul>
<li><span data-ttu-id="ef91f-132"><strong>Etenemissuunnitelma</strong> – etenemissuunnitelmat ovat kurssin erityisiä aihealueita.</span><span class="sxs-lookup"><span data-stu-id="ef91f-132"><strong>Track</strong> – Tracks are specific subject areas for a course.</span></span></li>
<li><span data-ttu-id="ef91f-133"><strong>Istunnot</strong> – istunnot jaetaan etenemissuunnitelmiin ja auttamat tunnistamaan prosesseja tai tekniikkoja, joilla on merkitystä etenemissuunnitelman kannalta.</span><span class="sxs-lookup"><span data-stu-id="ef91f-133"><strong>Sessions</strong> – Sessions divide up tracks and help identify specific processes or techniques that are relevant to the track.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="course-tasks"></a><span data-ttu-id="ef91f-134">Kurssin tehtävät</span><span class="sxs-lookup"><span data-stu-id="ef91f-134">Course tasks</span></span>
<span data-ttu-id="ef91f-135">Voit suorittaa jokaiselle kurssille seuraavat tehtävät:</span><span class="sxs-lookup"><span data-stu-id="ef91f-135">For each course, you can complete the following tasks.</span></span>
- <span data-ttu-id="ef91f-136">Osallistujien rekisteröinti</span><span class="sxs-lookup"><span data-stu-id="ef91f-136">Register participants</span></span>
- <span data-ttu-id="ef91f-137">Rekisteröinnin määräajan määritys</span><span class="sxs-lookup"><span data-stu-id="ef91f-137">Specify a registration deadline</span></span>
- <span data-ttu-id="ef91f-138">Osallistujien vähimmäis- ja enimmäismäärien määritys</span><span class="sxs-lookup"><span data-stu-id="ef91f-138">Define the minimum and maximum number of participants</span></span>
- <span data-ttu-id="ef91f-139">Kurssipaikan ja luokkahuoneen määritys</span><span class="sxs-lookup"><span data-stu-id="ef91f-139">Assign a course location and classroom</span></span>
- <span data-ttu-id="ef91f-140">Hotellien suosittelu kurssin osallistujille</span><span class="sxs-lookup"><span data-stu-id="ef91f-140">Recommend hotels to course participants</span></span>
- <span data-ttu-id="ef91f-141">kurssikuvauksen luonti, jota voidaan mainostaa työntekijöiden itsepalvelussa</span><span class="sxs-lookup"><span data-stu-id="ef91f-141">Create a course description, which you can then advertise on Employee self service</span></span>

  ><span data-ttu-id="ef91f-142">**Huomautus** Voit poistaa kurssin vain, jos kukaan ei ole rekisteröitynyt siihen.</span><span class="sxs-lookup"><span data-stu-id="ef91f-142">**Note** You can delete a course only if no one has registered for it.</span></span> 

## <a name="course-statuses"></a><span data-ttu-id="ef91f-143">Kurssin tilat</span><span class="sxs-lookup"><span data-stu-id="ef91f-143">Course statuses</span></span>
<span data-ttu-id="ef91f-144">Seuraavassa taulukossa luetellaan mahdolliset kurssin tilat sekä toiminnot, jotka voidaan suorittaa, kun kurssilla on tietty tila.</span><span class="sxs-lookup"><span data-stu-id="ef91f-144">The following table lists the possible course statuses and the actions that you can complete when the course has a specific status.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="ef91f-145">Tila</span><span class="sxs-lookup"><span data-stu-id="ef91f-145">Status</span></span></th>
<th><span data-ttu-id="ef91f-146">Toimet</span><span class="sxs-lookup"><span data-stu-id="ef91f-146">Actions</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ef91f-147"><strong>Luotu</strong></span><span class="sxs-lookup"><span data-stu-id="ef91f-147"><strong>Created</strong></span></span></td>
<td><ul>
<li><span data-ttu-id="ef91f-148">Kirjoita ja muuta kurssin tietoja.</span><span class="sxs-lookup"><span data-stu-id="ef91f-148">Enter and modify course information.</span></span></li>
<li><span data-ttu-id="ef91f-149">Muuta kurssin tilaksi <strong>Avoin</strong>, jotta työntekijät voivat rekisteröityä kurssille.</span><span class="sxs-lookup"><span data-stu-id="ef91f-149">Change the course status to <strong>Open</strong> so that workers can register for the course.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ef91f-150"><strong>Avaa</strong></span><span class="sxs-lookup"><span data-stu-id="ef91f-150"><strong>Open</strong></span></span></td>
<td><ul>
<li><span data-ttu-id="ef91f-151">Rekisteröi kurssin osallistujat.</span><span class="sxs-lookup"><span data-stu-id="ef91f-151">Register participants for the course.</span></span></li>
<li><span data-ttu-id="ef91f-152">Poista kurssin osallistujia.</span><span class="sxs-lookup"><span data-stu-id="ef91f-152">Remove participants from the course.</span></span></li>
<li><span data-ttu-id="ef91f-153">Vahvista kurssin osallistujat</span><span class="sxs-lookup"><span data-stu-id="ef91f-153">Confirm participants for the course.</span></span></li>
<li><span data-ttu-id="ef91f-154">Muuta kurssin tilaksi <strong>Suljettu</strong> tai <strong>Peruutettu</strong>.</span><span class="sxs-lookup"><span data-stu-id="ef91f-154">Change the course status to <strong>Closed</strong> or <strong>Canceled</strong>.</span></span></li>
<li><span data-ttu-id="ef91f-155">Suunnittele kyselylomakkeita osallistujille, joiden tila on <strong>Vahvistettu</strong>.</span><span class="sxs-lookup"><span data-stu-id="ef91f-155">Plan questionnaires for participants whose status is <strong>Confirmed</strong>.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ef91f-156"><strong>Suljettu</strong></span><span class="sxs-lookup"><span data-stu-id="ef91f-156"><strong>Closed</strong></span></span></td>
<td><span data-ttu-id="ef91f-157">Voit avata kurssin uudelleen.</span><span class="sxs-lookup"><span data-stu-id="ef91f-157">You can reopen the course.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ef91f-158"><strong>Peruutettu</strong></span><span class="sxs-lookup"><span data-stu-id="ef91f-158"><strong>Canceled</strong></span></span></td>
<td><span data-ttu-id="ef91f-159">Voit avata kurssin uudelleen.</span><span class="sxs-lookup"><span data-stu-id="ef91f-159">You can reopen the course.</span></span></td>
</tr>
</tbody>
</table>

## <a name="course-participants"></a><span data-ttu-id="ef91f-160">Kurssin osallistujat</span><span class="sxs-lookup"><span data-stu-id="ef91f-160">Course participants</span></span>
<span data-ttu-id="ef91f-161">Kurssin osallistujat ovat työntekijöitä, jotka osallistuvat koulutuskurssille tai tapahtumaan.</span><span class="sxs-lookup"><span data-stu-id="ef91f-161">Course participants are workers who participate in a training course or event.</span></span> <span data-ttu-id="ef91f-162">Voit rekisteröidä osallistujia vain avoimille kursseille.</span><span class="sxs-lookup"><span data-stu-id="ef91f-162">You can only register participants for open courses.</span></span> <span data-ttu-id="ef91f-163">Kurssille rekisteröitävien osallistujien vähimmäis- ja enimmäismäärä on määritetty **Kurssit**-sivun **Yleinen**-pikavälilehdessä.</span><span class="sxs-lookup"><span data-stu-id="ef91f-163">The minimum and maximum number of participants that you can register for a course is defined on the **General** FastTab on the **Courses** page.</span></span>

<a name="workflow"></a><span data-ttu-id="ef91f-164">Työnkulku</span><span class="sxs-lookup"><span data-stu-id="ef91f-164">Workflow</span></span>
--------

<span data-ttu-id="ef91f-165">Työntekijät, jotka ilmoittautuvat kurssille **työntekijän itsepalvelun** sivulla, voivat saada ilmoittautumisen reititettyä hyväksynnän työnkulun kautta.</span><span class="sxs-lookup"><span data-stu-id="ef91f-165">Employees who register for a course through the **Employee self service** page can have their registration routed through workflow for approval.</span></span> <span data-ttu-id="ef91f-166">Voit määrittää työnkulun kurssille **Kurssit**-sivun **Yleiset** -pikavälilehdessä.</span><span class="sxs-lookup"><span data-stu-id="ef91f-166">You can assign a workflow to a course on the **General** FastTab on the **Courses** page.</span></span>





