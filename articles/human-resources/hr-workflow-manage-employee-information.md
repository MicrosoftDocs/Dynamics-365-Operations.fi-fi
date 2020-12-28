---
title: Työntekijätietojen hallinta työnkulkujen avulla
description: Tässä artikkelissa kerrotaan, henkilöstöhallinnon työnkulkuja käytetään työntekijätietojen hallintaan. Voit esimerkiksi liittää työnkulun toimeen ja määrittää hyväksynnän työnkulun, joka käynnistyy, kun työntekijät muuttavat tietuettaan.
author: andreabichsel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Human Resources
ms.custom: 269074
ms.assetid: 426c6127-42ee-4163-8dd0-b2867f95581d
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 250b214372a12f99d2ababc97c5edf4456cadcad
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4418375"
---
# <a name="use-workflows-to-manage-employee-information"></a><span data-ttu-id="eb099-104">Työntekijätietojen hallinta työnkulkujen avulla</span><span class="sxs-lookup"><span data-stu-id="eb099-104">Use workflows to manage employee information</span></span>

<span data-ttu-id="eb099-105">Tässä artikkelissa kerrotaan, henkilöstöhallinnon työnkulkuja käytetään työntekijätietojen hallintaan.</span><span class="sxs-lookup"><span data-stu-id="eb099-105">This article explains how you can use the workflow capability for Human resources to manage employee information.</span></span> <span data-ttu-id="eb099-106">Voit esimerkiksi liittää työnkulun toimeen ja määrittää hyväksynnän työnkulun, joka käynnistyy, kun työntekijät muuttavat tietuettaan.</span><span class="sxs-lookup"><span data-stu-id="eb099-106">For example, you can associate a workflow with a position and configure an approval workflow that is started when employees change their record.</span></span>

<span data-ttu-id="eb099-107">Henkilöstöhallinnon työnkulut sisältävät useita työnkulkuja henkilöstönhallinnon tehtävien hallintaan.</span><span class="sxs-lookup"><span data-stu-id="eb099-107">The workflow capability for Human resources provides numerous workflows for managing human resources activities.</span></span> <span data-ttu-id="eb099-108">Käytettävissä on myös useita vaihtoehtoja tiettyjen työkulkujen muokkaamiseen ja niiden liittämiseen raportointihierarkiaan.</span><span class="sxs-lookup"><span data-stu-id="eb099-108">Additionally, numerous options are available so that you can modify specific workflows and associate them with a reporting hierarchy.</span></span> <span data-ttu-id="eb099-109">Työnkulut auttavat muutosten tekemisessä useisiin, vakiomuotoisiin työntekijätietoihin.</span><span class="sxs-lookup"><span data-stu-id="eb099-109">Workflows are available to help manage changes to several standard types of employee information.</span></span> <span data-ttu-id="eb099-110">Voit liittää työnkulun toimeen.</span><span class="sxs-lookup"><span data-stu-id="eb099-110">You can associate a workflow with a position.</span></span> <span data-ttu-id="eb099-111">Jos työntekijä muuttaa nyt työntekijätietuettaan, käynnistyy työnkulku, joka edellyttää hyväksynnän ennen, kuin uudet tiedot voidaan tallentaa.</span><span class="sxs-lookup"><span data-stu-id="eb099-111">Then, if employees change their employee record, a workflow is started that requires approval before the new information is saved.</span></span> <span data-ttu-id="eb099-112">Seuraaville tietotyypeille on määritetty työnkulut etukäteen, jotta työntekijätietojen tarkkuuden säilyttäminen ja muutosten hallinta olisi mahdollisimman tehokasta:</span><span class="sxs-lookup"><span data-stu-id="eb099-112">Workflows are predefined for the following types of information to help you efficiently manage changes and keep your employees’ data accurate:</span></span>

-   <span data-ttu-id="eb099-113">Tunnusnumerot</span><span class="sxs-lookup"><span data-stu-id="eb099-113">Identification numbers</span></span>
-   <span data-ttu-id="eb099-114">Kurssit</span><span class="sxs-lookup"><span data-stu-id="eb099-114">Courses</span></span>
-   <span data-ttu-id="eb099-115">Koulutus</span><span class="sxs-lookup"><span data-stu-id="eb099-115">Education</span></span>
-   <span data-ttu-id="eb099-116">Kuva</span><span class="sxs-lookup"><span data-stu-id="eb099-116">Image</span></span>
-   <span data-ttu-id="eb099-117">Lainatut nimikkeet</span><span class="sxs-lookup"><span data-stu-id="eb099-117">Loaned items</span></span>
-   <span data-ttu-id="eb099-118">Ammattikokemus</span><span class="sxs-lookup"><span data-stu-id="eb099-118">Professional experience</span></span>
-   <span data-ttu-id="eb099-119">Projektikokemus</span><span class="sxs-lookup"><span data-stu-id="eb099-119">Project experience</span></span>
-   <span data-ttu-id="eb099-120">Osaamisalueet</span><span class="sxs-lookup"><span data-stu-id="eb099-120">Skills</span></span>
-   <span data-ttu-id="eb099-121">Luottamustoimet</span><span class="sxs-lookup"><span data-stu-id="eb099-121">Positions of trust</span></span>
-   <span data-ttu-id="eb099-122">Henkilöstöhallinnon toimet</span><span class="sxs-lookup"><span data-stu-id="eb099-122">Human resources actions</span></span>
-   <span data-ttu-id="eb099-123">Kurssin rekisteröinti</span><span class="sxs-lookup"><span data-stu-id="eb099-123">Course registration</span></span>

<span data-ttu-id="eb099-124">Työnkulkuun voi sisältyä arviointiprosessi, kun työntekijöitä palkataan, siirretään tai irtisanotaan.</span><span class="sxs-lookup"><span data-stu-id="eb099-124">When employees are hired, transferred, or terminated, the workflow can include a review process.</span></span> <span data-ttu-id="eb099-125">Tällä tavalla asiakirjan voi tarkistaa tai toiminnon ehdot määrittää osaksi työnkulkua.</span><span class="sxs-lookup"><span data-stu-id="eb099-125">In this way, a document can be revised or the terms of an action can be defined as part of the workflow.</span></span> <span data-ttu-id="eb099-126">Kun tarkistus on valmis, asiakirja tai toiminto on valmis ja työnkulku siirtyy lopulliseen hyväksyntävaiheeseen.</span><span class="sxs-lookup"><span data-stu-id="eb099-126">When the review process is completed, the document or action is completed, and the workflow moves to a final approval step.</span></span>

## <a name="associate-a-workflow-with-a-position-hierarchy"></a><span data-ttu-id="eb099-127">Työnkulun liittäminen toimihierarkiaan</span><span class="sxs-lookup"><span data-stu-id="eb099-127">Associate a workflow with a position hierarchy</span></span>
<span data-ttu-id="eb099-128">Voit liittää työnkulun mihin tahansa määrittämääsi hierarkiaan.</span><span class="sxs-lookup"><span data-stu-id="eb099-128">You can associate a workflow with any hierarchy that you configure.</span></span> <span data-ttu-id="eb099-129">Jos toimeen liittyy esimerkiksi raportointihierarkian matriisi, voit määrittää työnkulun, joka reitittää kulut tietystä projektista projektin johtajalle toimeen liittyvän työntekijän esimiehen sijasta.</span><span class="sxs-lookup"><span data-stu-id="eb099-129">For example, if a position is associated with a matrix reporting hierarchy, you might configure a workflow that routes expenses for a specific project to the project lead instead of the manager of the employee who is associated with that position.</span></span> <span data-ttu-id="eb099-130">Luo uusi työnkulku tai muokkaa aiemmin luotua työnkulkua napsauttamalla **Henkilöstöhallinnan työnkulku** -sivulla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="eb099-130">To create a new workflow or modify an existing workflow, on the **Human resources workflow** page, click **New**.</span></span> <span data-ttu-id="eb099-131">Käynnistä työnkulun suunnittelija valitsemalla luettelosta työnkulku.</span><span class="sxs-lookup"><span data-stu-id="eb099-131">Select a workflow in the list to start the Workflow designer.</span></span> <span data-ttu-id="eb099-132">Voit käyttää suunnittelusovellusta uuden työnkulun luontiin tai muuttaa aiemmin luodun työnkulun vaiheita.</span><span class="sxs-lookup"><span data-stu-id="eb099-132">You can use the designer to create a new workflow or change the steps in an existing workflow.</span></span> <span data-ttu-id="eb099-133">Kun muutat aiemmin luotua työnkulkua, muutokset tallennetaan uuteen versioon.</span><span class="sxs-lookup"><span data-stu-id="eb099-133">When you change an existing workflow, your changes are saved as a new version.</span></span> <span data-ttu-id="eb099-134">Tämän ansiosta voit tarvittaessa palata aiempaan versioon.</span><span class="sxs-lookup"><span data-stu-id="eb099-134">Therefore, you can always go back to a previous version if you have to.</span></span>

## <a name="configure-a-human-resources-workflow"></a><span data-ttu-id="eb099-135">Henkilöstöhallinnon toimien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="eb099-135">Configure a Human resources workflow</span></span>
<span data-ttu-id="eb099-136">Seuraa näitä vaiheita määrittääksesi perustyönkulun, joka käynnistetään, kun työntekijät haluavat muuttaa henkilötietojaan.</span><span class="sxs-lookup"><span data-stu-id="eb099-136">To configure a basic workflow that is started when employees request changes to their personal identification, follow these steps.</span></span>

1.  <span data-ttu-id="eb099-137">Valitse **Henkilöstöhallinnon työkulut** -sivulla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="eb099-137">On the **Human resources workflows** page, click **New**.</span></span>
2.  <span data-ttu-id="eb099-138">Valitse käytettävien työnkulkujen luettelosta **Tunnusnumerot**.</span><span class="sxs-lookup"><span data-stu-id="eb099-138">In the list of available workflows, select **Identification numbers**.</span></span>
3.  <span data-ttu-id="eb099-139">Käynnistä työnkulun suunnittelusovellus valitsemalla **Suorita** ja kirjoita käyttäjänimesi ja salasanasi pyydettäessä.</span><span class="sxs-lookup"><span data-stu-id="eb099-139">Click **Run** to start the Workflow designer, and then enter your user name and password when you're prompted.</span></span>
4.  <span data-ttu-id="eb099-140">Vedä **Hyväksy tunnusnumero** -elementti työnkulun elementtien luettelosta suunnittelusovelluksen alustalle.</span><span class="sxs-lookup"><span data-stu-id="eb099-140">Drag the **Approve identification number** element from the list of workflow elements to the designer canvas.</span></span>
5.  <span data-ttu-id="eb099-141">Yhdistä hyväksyntäelementti **Alku**- ja **Loppu**-elementteihin.</span><span class="sxs-lookup"><span data-stu-id="eb099-141">Connect the approval element to **Start** and **Finish**.</span></span>
6.  <span data-ttu-id="eb099-142">Kaksoisnapsauta **Hyväksy elementti** -kohtaa sitten valitse **Ominaisuudet**.</span><span class="sxs-lookup"><span data-stu-id="eb099-142">Double-click **Approve element**, and then right-click, and select **Properties**.</span></span>
7.  <span data-ttu-id="eb099-143">Voit lisätä työkohteen ohjeita seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="eb099-143">Follow these steps to add work item instructions:</span></span>
    1.  <span data-ttu-id="eb099-144">Valitse **Tehtävä** ja sitten **Hierarkia** tehtävätyyppi-kohdasta.</span><span class="sxs-lookup"><span data-stu-id="eb099-144">Select **Assignment**, and then select **Hierarchy** under the assignment type.</span></span>
    2.  <span data-ttu-id="eb099-145">Valitse **Hierarkia**-vaihtoehdoista **Määritettävä hierarkia**.</span><span class="sxs-lookup"><span data-stu-id="eb099-145">Under the **Hierarchy** selection, select **Configurable hierarchy**.</span></span>
    3.  <span data-ttu-id="eb099-146">Lisää pysäytysehto ja sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="eb099-146">Add a stop condition, and close the page.</span></span>

8.  <span data-ttu-id="eb099-147">Täytä lisäohjeet (muita varoituksia ei tule olla).</span><span class="sxs-lookup"><span data-stu-id="eb099-147">Complete any additional instructions (no additional warnings should exist).</span></span>
9.  <span data-ttu-id="eb099-148">Valitse **Tallenna ja sulje**.</span><span class="sxs-lookup"><span data-stu-id="eb099-148">Click **Save and close**.</span></span> <span data-ttu-id="eb099-149">Aktivoi uusi työnkulku valitsemalla **Aktivoi** aukeavasta valintaikkunasta.</span><span class="sxs-lookup"><span data-stu-id="eb099-149">Activate the new workflow when the dialog box opens, and select **Make active**.</span></span>
10. <span data-ttu-id="eb099-150">Siirry kohtaan **Henkilöstöhallinto** &gt; **Toimet** &gt; **Positiohierarkiatyypit**.</span><span class="sxs-lookup"><span data-stu-id="eb099-150">Go to **Human Resources** &gt; **Positions** &gt; **Position hierarchy types**.</span></span>
11. <span data-ttu-id="eb099-151">Valitse **Matriisi**.</span><span class="sxs-lookup"><span data-stu-id="eb099-151">Select **Matrix**.</span></span>
12. <span data-ttu-id="eb099-152">Lisää **työntekijän tunnusnumero** -työnkulku luetteloon.</span><span class="sxs-lookup"><span data-stu-id="eb099-152">Add the **Worker identification number** workflow to the list.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="eb099-153">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="eb099-153">Additional resources</span></span>

[<span data-ttu-id="eb099-154">Osoitemuutosten tarkasteleminen ja hallinta</span><span class="sxs-lookup"><span data-stu-id="eb099-154">View and manage address changes</span></span>](hr-personnel-view-address-changes.md) 



