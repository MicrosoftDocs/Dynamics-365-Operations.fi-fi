---
title: Tuotannon käyttöliittymän suunnitteleminen
description: Tässä aiheessa käsitellään kunkin määrityksen käyttöliittymän sisällön suunnittelua.
author: johanhoffmann
manager: tfehr
ms.date: 12/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: Release 10.0.16
ms.openlocfilehash: 81c5c83128bb81523dee6ede549eece7b0d80e30
ms.sourcegitcommit: d9d1ddce6a334ade8b32b5ea3ac4c1e1a8f72715
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/02/2020
ms.locfileid: "4664269"
---
# <a name="design-the-production-floor-execution-interface"></a><span data-ttu-id="de91a-103">Tuotannon käyttöliittymän suunnitteleminen</span><span class="sxs-lookup"><span data-stu-id="de91a-103">Design the production floor execution interface</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="de91a-104">Kunkin tuotannon käyttöliittymän käyttämän määrityksen käyttöliittymän sisältö voidaan suunnitella.</span><span class="sxs-lookup"><span data-stu-id="de91a-104">You can design the content of the user interface for each configuration used by the production floor execution interface.</span></span> <span data-ttu-id="de91a-105">Esimerkiksi tietyn työsolun työntekijöiden on ehkä voitava avata työohjeet tuotannossa, kun toisessa työsolussa näitä ohjeita ei tarvita.</span><span class="sxs-lookup"><span data-stu-id="de91a-105">For example, workers in one work cell might need to be able to open job instructions on the production floor, while in another work cell, instructions are not needed.</span></span> <span data-ttu-id="de91a-106">Siinä tapauksessa on luotava kaksi määritystä, joista toisessa on painike asiakirjaliitteiden avaamiseen ja toisessa kyseistä painiketta ei ole.</span><span class="sxs-lookup"><span data-stu-id="de91a-106">In that case, two configurations should be created, one with a button for opening document attachments and one without this button.</span></span>

## <a name="design-a-tab"></a><span data-ttu-id="de91a-107">Välilehden suunnitteleminen</span><span class="sxs-lookup"><span data-stu-id="de91a-107">Design a tab</span></span>

<span data-ttu-id="de91a-108">**Määritä tuotantoliittymä** -sivulla voi luoda ja määrittää välilehtiä valitsemalla toimintoruudussa **Suunnittele välilehtiä**.</span><span class="sxs-lookup"><span data-stu-id="de91a-108">On the **Configure production floor execution** page, you can create and configure tabs by selecting **Design tabs** on the Action Pane.</span></span>

<span data-ttu-id="de91a-109">Kukin välilehti on jaettu neljään osaan, kuten seuraavassa kuvassa.</span><span class="sxs-lookup"><span data-stu-id="de91a-109">Each tab is divided into four sections, as shown in the following illustration.</span></span>

<span data-ttu-id="de91a-110">![Välilehden asettelu](media/pfe-tab-layout.png "Välilehden asettelu")</span><span class="sxs-lookup"><span data-stu-id="de91a-110">![Tab layout](media/pfe-tab-layout.png "Tab layout")</span></span>

<span data-ttu-id="de91a-111">Kuvassa näkyy seuraavat elementit:</span><span class="sxs-lookup"><span data-stu-id="de91a-111">The following elements are shown in the illustration:</span></span>

1. <span data-ttu-id="de91a-112">Ensisijainen työkalurivi</span><span class="sxs-lookup"><span data-stu-id="de91a-112">Primary toolbar</span></span>
1. <span data-ttu-id="de91a-113">Toissijainen työkalurivi</span><span class="sxs-lookup"><span data-stu-id="de91a-113">Secondary toolbar</span></span>
1. <span data-ttu-id="de91a-114">Päänäkymä</span><span class="sxs-lookup"><span data-stu-id="de91a-114">Main view</span></span>
1. <span data-ttu-id="de91a-115">Tarkka näkymä</span><span class="sxs-lookup"><span data-stu-id="de91a-115">Detailed view</span></span>

<span data-ttu-id="de91a-116">Uusi välilehti luodaan ja määritetään seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="de91a-116">To create and configure a new tab, follow these steps:</span></span>

1. <span data-ttu-id="de91a-117">Valitse **Tuotannonhallinta &gt; Määritys &gt; Tuotannonohjaus**.</span><span class="sxs-lookup"><span data-stu-id="de91a-117">Go to **Production control &gt; Setup &gt; Manufacturing execution**.</span></span>

1. <span data-ttu-id="de91a-118">Avaa **Suunnittele välilehtiä** -sivu valitsemalla toimintoruudussa **Suunnittele välilehtiä**.</span><span class="sxs-lookup"><span data-stu-id="de91a-118">Select **Design tabs** on the Action Pane to open the **Design tabs** page.</span></span>

    <span data-ttu-id="de91a-119">![Suunnittele välilehtiä -sivu](media/pfe-design-tabs.png "Suunnittele välilehtiä -sivu")</span><span class="sxs-lookup"><span data-stu-id="de91a-119">![The Design tabs page](media/pfe-design-tabs.png "The Design tabs page")</span></span>

1. <span data-ttu-id="de91a-120">Valitse toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="de91a-120">Select **New** on the Action Pane.</span></span>

1. <span data-ttu-id="de91a-121">Määritä seuraavat asetukset sivun otsikossa:</span><span class="sxs-lookup"><span data-stu-id="de91a-121">Make the following settings in the header of the page:</span></span>

    - <span data-ttu-id="de91a-122">**Välilehden nimi** – määritä välilehden nimi.</span><span class="sxs-lookup"><span data-stu-id="de91a-122">**Tab name** - Specify a name for the tab.</span></span>
    - <span data-ttu-id="de91a-123">**Päänäkymä** – valitse jompikumpi esimääritetyistä työluetteloista (*Aktiiviset työt* tai *Kaikki työt*).</span><span class="sxs-lookup"><span data-stu-id="de91a-123">**Main view** - Select between the two pre-defined job lists (*Active jobs* or *All jobs*).</span></span>
    - <span data-ttu-id="de91a-124">**Tietonäkymä** – Valitse joko tyhjä arvo tai **Työn tiedot**.</span><span class="sxs-lookup"><span data-stu-id="de91a-124">**Details view** - Select between a blank value or **Job details**.</span></span> <span data-ttu-id="de91a-125">Jos valitset tyhjän arvon, välilehdessä ei ole tietonäkymää. Jos valitse **Työn tiedot**, tietonäkymässä on tarkka kuvaus päänäkymän työluettelossa valitusta työstä.</span><span class="sxs-lookup"><span data-stu-id="de91a-125">If you select the blank value, there will be no detailed view in the tab. If you select **Job details**, the detailed view will contain a detailed description of the job selected in the job list in the main view.</span></span>

1. <span data-ttu-id="de91a-126">Valitse **Ensisijainen työkalurivi** -osassa ensisijaisessa työkalurivissä käytettävissä olevat painikkeet.</span><span class="sxs-lookup"><span data-stu-id="de91a-126">In the **Primary toolbar** section, choose which buttons should be available in the primary toolbar.</span></span> <span data-ttu-id="de91a-127">**Käytettävissä olevat toiminnot** -sarakkeessa on luettelo lisättävistä painikkeista.</span><span class="sxs-lookup"><span data-stu-id="de91a-127">The **Available actions** column shows a list of all the buttons that can be added.</span></span> <span data-ttu-id="de91a-128">**Valitut toiminnot** -sarakkeessa on luettelo kaikista painikkeista, jotka sisältyvät nykyiseen määritykseen.</span><span class="sxs-lookup"><span data-stu-id="de91a-128">The **Selected actions** columns shows a list of all the buttons that are included in the current configuration.</span></span> <span data-ttu-id="de91a-129">Siirrä nimikkeitä tarvittaessa sarakkeesta toiseen sarakkeiden välissä olevilla painikkeilla.</span><span class="sxs-lookup"><span data-stu-id="de91a-129">Use the buttons between the columns to move selected items between the columns as needed.</span></span> <span data-ttu-id="de91a-130">Määritä järjestys, jossa painikkeet näytetään käyttöliittymässä, **Valitut toiminnot** -sarakkeen vieressä olevilla ylä- ja alanuolipainikkeilla.</span><span class="sxs-lookup"><span data-stu-id="de91a-130">Use the up and down buttons next to the **Selected actions** column to control the order in which the buttons are presented in the user interface.</span></span>

1. <span data-ttu-id="de91a-131">Valitse **Toissijainen** **työkalurivi** -osassa toissijaisessa työkalurivissä käytettävissä olevat painikkeet.</span><span class="sxs-lookup"><span data-stu-id="de91a-131">In the **Secondary** **toolbar** section, choose which buttons should be available in the secondary toolbar.</span></span> <span data-ttu-id="de91a-132">**Käytettävissä olevat toiminnot** -sarakkeessa on luettelo lisättävistä painikkeista.</span><span class="sxs-lookup"><span data-stu-id="de91a-132">The **Available actions** column shows a list of all the buttons that can be added.</span></span> <span data-ttu-id="de91a-133">**Valitut toiminnot** -sarakkeessa on luettelo kaikista painikkeista, jotka sisältyvät nykyiseen määritykseen.</span><span class="sxs-lookup"><span data-stu-id="de91a-133">The **Selected actions** columns shows a list of all the buttons that are included in the current configuration.</span></span> <span data-ttu-id="de91a-134">Siirrä nimikkeitä tarvittaessa sarakkeesta toiseen sarakkeiden välissä olevilla painikkeilla.</span><span class="sxs-lookup"><span data-stu-id="de91a-134">Use the buttons between the columns to move selected items between the columns as needed.</span></span> <span data-ttu-id="de91a-135">Määritä järjestys, jossa painikkeet näytetään käyttöliittymässä, **Valitut toiminnot** -sarakkeen vieressä olevilla ylä- ja alanuolipainikkeilla.</span><span class="sxs-lookup"><span data-stu-id="de91a-135">Use the up and down buttons next to the **Selected actions** column to control the order in which the buttons are presented in the user interface.</span></span>

## <a name="associate-a-tab-with-a-configuration"></a><span data-ttu-id="de91a-136">Välilehden liittäminen määritykseen</span><span class="sxs-lookup"><span data-stu-id="de91a-136">Associate a tab with a configuration</span></span>

<span data-ttu-id="de91a-137">Kun kaikki tarvittavat välilehdet on suunniteltu, voit liittää ne määritykseen.</span><span class="sxs-lookup"><span data-stu-id="de91a-137">After you designed all the tabs you need, you can associate them with a configuration.</span></span>

1. <span data-ttu-id="de91a-138">Valitse **Tuotannonhallinta &gt; Määritys &gt; Määritä tuotantoliittymä**.</span><span class="sxs-lookup"><span data-stu-id="de91a-138">Go to **Production control &gt; Setup &gt; Configure production floor execution**.</span></span>

    <span data-ttu-id="de91a-139">![Määritä tuotannon suoritus](media/pfe-config-prod-floor-execution.png "Määritä tuotannon suoritus")</span><span class="sxs-lookup"><span data-stu-id="de91a-139">![Configure production floor execution](media/pfe-config-prod-floor-execution.png "Configure production floor execution")</span></span>

1. <span data-ttu-id="de91a-140">Valitse **Välilehtivalinta**-pikavälilehdessä **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="de91a-140">On the **Tab selection** FastTab, select **Add**.</span></span>

1. <span data-ttu-id="de91a-141">Uusi rivi lisätään ruudukkoon.</span><span class="sxs-lookup"><span data-stu-id="de91a-141">A new row is added to the grid.</span></span> <span data-ttu-id="de91a-142">Valitse uudelle riville määritykseen lisättävän välilehden nimi.</span><span class="sxs-lookup"><span data-stu-id="de91a-142">For this new row, select the name of a tab that you want to add to the configuration.</span></span>

1. <span data-ttu-id="de91a-143">Jatka lisäämällä välilehtiä tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="de91a-143">Continue to add additional tabs as needed.</span></span>

1. <span data-ttu-id="de91a-144">Järjestele välilehtiä tarpeen mukaan työkalurivin **Siirrä ylös**- ja **Siirrä alas** -painikkeilla.</span><span class="sxs-lookup"><span data-stu-id="de91a-144">Use the **Move up** and **Move down** buttons on the toolbar to arrange the tabs as needed.</span></span> <span data-ttu-id="de91a-145">Välilehdet näytetään vasemmalta oikealle edellä olevassa näyttökuvassa olevassa järjestyksessä (ylhäällä oleva välilehti näytetään vasemmalla).</span><span class="sxs-lookup"><span data-stu-id="de91a-145">The tabs will be displayed from left to right in the order shown in the above screenshot (the tab at the top is shown on the left).</span></span>
