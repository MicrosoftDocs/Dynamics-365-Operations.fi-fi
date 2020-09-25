---
title: Projektiresurssien määrittäminen
description: Tässä aiheessa on tietoja projektin resurssien määrittämisestä ja pyytämisestä.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c882e23794e3937f85b3e73774b36deaf28ac3ed
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760538"
---
# <a name="set-up-project-resources"></a><span data-ttu-id="7f539-103">Projektiresurssien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="7f539-103">Set up project resources</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7f539-104">Sinun täytyy määrittää kalenteri ja liittää se työntekijään.</span><span class="sxs-lookup"><span data-stu-id="7f539-104">You must set up a calendar and associate it with an employee or a worker.</span></span> <span data-ttu-id="7f539-105">Kalenterin avulla aikataulutetaan projekti ja siihen varattujen resurssien työaika.</span><span class="sxs-lookup"><span data-stu-id="7f539-105">The calendar is used to schedule the project and the working time of the resources that are reserved for the project.</span></span> <span data-ttu-id="7f539-106">Kalenteria määrittäessään projektipäälliköt voivat suorittaa resurssien tasaamisen resurssien optimoinnin yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="7f539-106">During calendar setup, project managers can do resource leveling as part of resource optimization.</span></span> <span data-ttu-id="7f539-107">Kalenterin aikataulun perusteella resursseille voidaan asettaa rajoituksia.</span><span class="sxs-lookup"><span data-stu-id="7f539-107">Based on the calendar schedule, restrictions can be put on resources.</span></span> <span data-ttu-id="7f539-108">Voit määrittää kalenterin **Kalenterit**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="7f539-108">You can set up a calendar on the **Calendars** page.</span></span>

<span data-ttu-id="7f539-109">Työntekijän projektin resurssiksi määrittäessäsi voit valita sen yrityksen työntekijät, jolle resursseja määritetään.</span><span class="sxs-lookup"><span data-stu-id="7f539-109">When you set up a worker as a project resource, you can select from workers who work in the company that you're setting up resources for.</span></span> <span data-ttu-id="7f539-110">Voit vaihtoehtoisesti valita työntekijät muista organisaation yrityksistä.</span><span class="sxs-lookup"><span data-stu-id="7f539-110">Alternatively, you can select workers from other companies in your organization.</span></span> <span data-ttu-id="7f539-111">Nämä työntekijät ovat konsernin sisäisiä resursseja.</span><span class="sxs-lookup"><span data-stu-id="7f539-111">These workers are known as intercompany resources.</span></span>

<span data-ttu-id="7f539-112">Seuraavissa ohjeissa selitetään, miten työntekijä määritetään yrityksen projektiin resurssiksi ja miten konsernin sisäinen projektin resurssi määritetään.</span><span class="sxs-lookup"><span data-stu-id="7f539-112">The following procedures explain how to set up a worker as a project resource in your company and how to set up an intercompany project resource.</span></span>

## <a name="set-up-a-worker-as-a-project-resource"></a><span data-ttu-id="7f539-113">Työntekijän määrittäminen projektiresurssiksi</span><span class="sxs-lookup"><span data-stu-id="7f539-113">Set up a worker as a project resource</span></span>

1. <span data-ttu-id="7f539-114">Valitse **Työntekijät**-sivun **Työntekijät**-luettelosta työntekijä, jonka haluat lisätä projektiin resurssiksi, ja avaa haluamasi työntekijätietue.</span><span class="sxs-lookup"><span data-stu-id="7f539-114">On the **Workers** page, in the **Workers** list, select the worker that you're adding as a project resource, and open the worker record.</span></span>
2. <span data-ttu-id="7f539-115">Valitse toimintoruudussa **Projekti** &gt; **Asetukset** &gt; **Projektiasetukset**.</span><span class="sxs-lookup"><span data-stu-id="7f539-115">On the Action Pane, select **Project** &gt; **Setup** &gt; **Project setup**.</span></span>
3. <span data-ttu-id="7f539-116">Valitse kalenteri ja sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="7f539-116">Select a calendar, and then close the page.</span></span>

<span data-ttu-id="7f539-117">Voit myös määrittää resurssille oletusprojektit eräänlaisena esimäärityksenä.</span><span class="sxs-lookup"><span data-stu-id="7f539-117">You can also specify default projects for a resource as a type of pre-assignment.</span></span> <span data-ttu-id="7f539-118">Esimäärityksiä voidaan käyttää, kun resurssi- tai projektipäällikkö tietää jo etukäteen, missä projekteissa resurssi työskentelee.</span><span class="sxs-lookup"><span data-stu-id="7f539-118">Pre-assignments can be used when the resource manager or project manager knows which projects the resource will be working on in advance.</span></span> <span data-ttu-id="7f539-119">Esimääritykset voivat perustua myös projektin sponsorin tai asiakkaan pyyntöön.</span><span class="sxs-lookup"><span data-stu-id="7f539-119">Pre-assignments can also be based on the request of a project sponsor or customer.</span></span> <span data-ttu-id="7f539-120">Jos haluat esimäärittää projektin, valitse **Määritä projektit** -sivulta **Projektit**-välilehdestä **Jäljellä olevat projektit** -luettelosta haluamasi projekti.</span><span class="sxs-lookup"><span data-stu-id="7f539-120">To pre-assign a project, on the **Assign projects** page, on the **Projects** tab, in the **Remaining projects** list, select the appropriate project.</span></span>

## <a name="set-up-an-intercompany-resource"></a><span data-ttu-id="7f539-121">Konsernin sisäisen resurssin määrittäminen</span><span class="sxs-lookup"><span data-stu-id="7f539-121">Set up an intercompany resource</span></span>

<span data-ttu-id="7f539-122">Kun määrität työntekijää konsernin sisäiseksi resurssiksi, määritä tiedot yrityksestä, joka antaa resurssin lainaksi ja yrityksestä, joka ottaa resurssin lainaksi.</span><span class="sxs-lookup"><span data-stu-id="7f539-122">When you set up a worker as an intercompany resource, you must complete the setup in both the lending company and the borrowing company.</span></span>

### <a name="in-the-lending-company"></a><span data-ttu-id="7f539-123">Yritys, joka antaa resurssin lainaksi</span><span class="sxs-lookup"><span data-stu-id="7f539-123">In the lending company</span></span>

1. <span data-ttu-id="7f539-124">Varmista Financessa, että resurssin lainaava yritys on valittu. Tee sitten toimenpiteet, jotka on mainittu edellä olevassa kohdassa "Työntekijän määrittäminen projektiresurssiksi".</span><span class="sxs-lookup"><span data-stu-id="7f539-124">In Finance, verify that the lending company is selected, and then complete the procedure in the previous section, "Set up a worker as a project resource."</span></span>
2. <span data-ttu-id="7f539-125">Valitse **Konsernin sisäinen kirjanpito** -sivulla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="7f539-125">On the **Intercompany accounting** page, select **New**.</span></span>
3. <span data-ttu-id="7f539-126">**Yrityksen tunnus** -kenttään yritys, jolta resurssi lainataan.</span><span class="sxs-lookup"><span data-stu-id="7f539-126">In the **Legal entity ID** field, select the lending company.</span></span> <span data-ttu-id="7f539-127">Anna tarvittavat tiedot muihin kenttiin ja valitse sitten **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="7f539-127">Fill in the remaining fields as appropriate, and then select **Save**.</span></span>
4. <span data-ttu-id="7f539-128">Valitse **Siirtohinta** -sivulla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="7f539-128">On the **Transfer price** page, select **New**.</span></span>
5. <span data-ttu-id="7f539-129">**Lainaava yritys** -kenttään asianmukainen yritys.</span><span class="sxs-lookup"><span data-stu-id="7f539-129">In the **Borrowing legal entity** field, select the appropriate company.</span></span>
6. <span data-ttu-id="7f539-130">Jos haluat lainata lainaavalle yritykselle vain resurssin, jonka loit tämän osan alussa, valitse **Resurssi**-kentässä luomasi resurssin nimi.</span><span class="sxs-lookup"><span data-stu-id="7f539-130">To lend the borrowing company only the resource that you created at the beginning of this section, in the **Resource** field, select the name of the resource that you created.</span></span> <span data-ttu-id="7f539-131">Jos haluat, että kaikki lainan antavan yrityksen resurssit ovat lainaavan yrityksen käytettävissä, jätä **Resurssi**-kenttä tyhjäksi.</span><span class="sxs-lookup"><span data-stu-id="7f539-131">To make all resources in the lending company available to the borrowing company, leave the **Resource** field blank.</span></span>
7. <span data-ttu-id="7f539-132">Määritä **Projektinhallinnan ja kirjanpidon parametrit** -sivun **Konsernin sisäinen** -välilehden **Ota käyttöön konsernin sisäinen resurssien ajoitus ja aikaraportit** -asetuksen arvoksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="7f539-132">On the **Project management and accounting parameters** page, on the **Intercompany** tab, set the **Enable intercompany resource scheduling and timesheets** option to **Yes**.</span></span>

### <a name="in-the-borrowing-company"></a><span data-ttu-id="7f539-133">Yritys, joka lainaa resurssin</span><span class="sxs-lookup"><span data-stu-id="7f539-133">In the borrowing company</span></span>

- <span data-ttu-id="7f539-134">Syötä **Resurssiluettelo**-sivun hakusuodattimeen sille yritykselle luomasi resurssin nimi, jolta resurssi lainataan. Varmista, että nimi löytyy sen yrityksen resurssiluettelosta, jolle resurssi lainataan.</span><span class="sxs-lookup"><span data-stu-id="7f539-134">On the **Resources list** page, in the search filter, enter the name of the resource that you created for the lending company, to verify that the name is included in the resource list for the borrowing company.</span></span>

## <a name="request-project-resources"></a><span data-ttu-id="7f539-135">Projektiresurssien pyytäminen</span><span class="sxs-lookup"><span data-stu-id="7f539-135">Request project resources</span></span>
<span data-ttu-id="7f539-136">Projektiresurssin ajoitustoiminto tukee vain resurssipäälliköitä, jotka jakavat henkilöllisiä resursseja sitoumuksiin tai projekteihin.</span><span class="sxs-lookup"><span data-stu-id="7f539-136">The functionality for project resource scheduling only lets resource managers distribute staffed resources on engagements or projects.</span></span> <span data-ttu-id="7f539-137">Tämä toiminto otetaan käyttöön suorittamalla seuraavat tehtävät valmiiksi tai varmistamalla, että ne on suoritettu:</span><span class="sxs-lookup"><span data-stu-id="7f539-137">To enable this functionality, complete the following tasks, or verify that they have been completed:</span></span>

- <span data-ttu-id="7f539-138">Määritä numerosarjat.</span><span class="sxs-lookup"><span data-stu-id="7f539-138">Set up number sequences.</span></span>
- <span data-ttu-id="7f539-139">Määritä projektinhallinnan ja kirjanpidon työnkulut.</span><span class="sxs-lookup"><span data-stu-id="7f539-139">Set up project management and accounting workflows.</span></span>
- <span data-ttu-id="7f539-140">Ota resurssipyynnön työnkulut käyttöön.</span><span class="sxs-lookup"><span data-stu-id="7f539-140">Enable resource request workflows.</span></span>

<span data-ttu-id="7f539-141">Kun edeltävät tehtävät on suoritettu, voit suorittaa seuraavat tehtävät tarvittaessa:</span><span class="sxs-lookup"><span data-stu-id="7f539-141">After the preceding tasks have been completed, you can complete the following tasks as you require:</span></span>

- <span data-ttu-id="7f539-142">Luo resurssipyyntö alustavasti varatusta henkilöllisestä resurssista.</span><span class="sxs-lookup"><span data-stu-id="7f539-142">Create a resource request from a soft-booked staffed resource.</span></span>
- <span data-ttu-id="7f539-143">Seuraa resurssipyyntöjä.</span><span class="sxs-lookup"><span data-stu-id="7f539-143">Monitor resource requests.</span></span>
- <span data-ttu-id="7f539-144">Täytä resurssipyynnöt.</span><span class="sxs-lookup"><span data-stu-id="7f539-144">Fulfill resource requests.</span></span>
- <span data-ttu-id="7f539-145">Pyydä henkilöllistä resurssia työrakenteesta.</span><span class="sxs-lookup"><span data-stu-id="7f539-145">Request a staffed resource from a WBS.</span></span>
- <span data-ttu-id="7f539-146">Varaa projektin resurssit ilman henkilöllisen resurssin pyyntöä.</span><span class="sxs-lookup"><span data-stu-id="7f539-146">Book resources to a project without having a request for a staffed resource.</span></span>
