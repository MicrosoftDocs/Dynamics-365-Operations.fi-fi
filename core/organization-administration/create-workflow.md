---
title: "Luo työnkulku"
description: "Tässä ohjeaiheessa kerrotaan, miten voit luoda työnkulun."
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, UnifiedOperations
ms.custom: 195583
ms.assetid: 836ddd01-cc34-45c3-a4b0-20647357dbc6
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 2
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 4d57e47fe7f38a43ecfdfbdd701d7e6a7d7800d6
ms.contentlocale: fi-fi
ms.lasthandoff: 07/18/2017

---

# <a name="create-a-workflow"></a><span data-ttu-id="61dcd-103">Luo työnkulku</span><span class="sxs-lookup"><span data-stu-id="61dcd-103">Create a workflow</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="61dcd-104">Tässä ohjeaiheessa kerrotaan, miten voit luoda työnkulun.</span><span class="sxs-lookup"><span data-stu-id="61dcd-104">This topics explains how to create a workflow.</span></span>

<a name="open-the-workflow-editor"></a><span data-ttu-id="61dcd-105">Avaa työnkulkueditori</span><span class="sxs-lookup"><span data-stu-id="61dcd-105">Open the workflow editor</span></span>
------------------------

<span data-ttu-id="61dcd-106">Käyttämäsi Microsoft Dynamics 365 for Finance and Operationsin moduuli määrittää, mitä työnkulun tyyppejä voi luoda.</span><span class="sxs-lookup"><span data-stu-id="61dcd-106">The Microsoft Dynamics 365 for Finance and Operations module that you're working in determines the types of workflow that you can create.</span></span> <span data-ttu-id="61dcd-107">Valitse näiden ohjeiden avulla työnkulkutyyppi työnkulkueditorin luomiseksi ja avaamiseksi.</span><span class="sxs-lookup"><span data-stu-id="61dcd-107">Follow these steps to select the type of workflow to create and open the workflow editor.</span></span>

1.  <span data-ttu-id="61dcd-108">Avaa moduuli, jolle haluat luoda uuden työnkulun.</span><span class="sxs-lookup"><span data-stu-id="61dcd-108">Open the module that you want to create a new workflow for.</span></span> <span data-ttu-id="61dcd-109">Esimerkiksi luoda työnkulun ostoehdotukselle valitsemalla **hankinta**.</span><span class="sxs-lookup"><span data-stu-id="61dcd-109">For example, to create a workflow for purchase requisitions, click **Procurement and sourcing**.</span></span>
2.  <span data-ttu-id="61dcd-110">Valitse **Asetukset** &gt; **\[moduulin nimi\] työnkulut**.</span><span class="sxs-lookup"><span data-stu-id="61dcd-110">Click **Setup** &gt; **\[Module name\] workflows**.</span></span>
3.  <span data-ttu-id="61dcd-111">Luettelosivun, joka näkyy toimintoruudussa valitse **uusi**.</span><span class="sxs-lookup"><span data-stu-id="61dcd-111">On the list page that appears, on the Action Pane, click **New**.</span></span>
4.  <span data-ttu-id="61dcd-112">Valitse **luoda työnkulun** -sivu, ja valitse sitten työnkulun tyyppi ja valitse **luoda työnkulun**.</span><span class="sxs-lookup"><span data-stu-id="61dcd-112">On the **Create workflow** page, select the type of workflow to create, and then click **Create workflow**.</span></span> <span data-ttu-id="61dcd-113">Työnkulkueditori tulee näyttöön</span><span class="sxs-lookup"><span data-stu-id="61dcd-113">The workflow editor appears.</span></span> <span data-ttu-id="61dcd-114">Seuraavan menetelmän avulla voit rakentaa työnkulun.</span><span class="sxs-lookup"><span data-stu-id="61dcd-114">You can now use the following procedures to design the workflow.</span></span>

## <a name="drag-workflow-elements-onto-the-canvas"></a><span data-ttu-id="61dcd-115">Vedä työnkulun elementit alustalle.</span><span class="sxs-lookup"><span data-stu-id="61dcd-115">Drag workflow elements onto the canvas</span></span>
<span data-ttu-id="61dcd-116">**Työnkulun elementit** -alue sisältää osia, jotka voidaan lisätä työnkulkuun.</span><span class="sxs-lookup"><span data-stu-id="61dcd-116">The **Workflow elements** area of the workflow editor contains the elements that you can add to your workflow.</span></span> <span data-ttu-id="61dcd-117">Lisää työnkulun elementit, vedä ne alustalle.</span><span class="sxs-lookup"><span data-stu-id="61dcd-117">To add elements to the workflow, drag them onto the canvas.</span></span>

## <a name="connect-the-elements"></a><span data-ttu-id="61dcd-118">Yhdistä elementit</span><span class="sxs-lookup"><span data-stu-id="61dcd-118">Connect the elements</span></span>
<span data-ttu-id="61dcd-119">Voit yhdistää yhden työnkulkuelementin toiseen pitämällä osoitinta elementin päällä, kunnes yhteyspisteet avautuvat näkyville.</span><span class="sxs-lookup"><span data-stu-id="61dcd-119">To connect one workflow element to another, hold the pointer over an element until connection points appear.</span></span> <span data-ttu-id="61dcd-120">Napsauta yhteyspistettä ja vedä se toiseen elementtiin.</span><span class="sxs-lookup"><span data-stu-id="61dcd-120">Click a connection point, and drag it to another element.</span></span> <span data-ttu-id="61dcd-121">Varmista, että liität kaikki osat.</span><span class="sxs-lookup"><span data-stu-id="61dcd-121">Be sure to connect all the elements.</span></span>

## <a name="configure-the-properties-of-the-workflow"></a><span data-ttu-id="61dcd-122">Työnkulun ominaisuuksien konfiguroiminen</span><span class="sxs-lookup"><span data-stu-id="61dcd-122">Configure the properties of the workflow</span></span>
<span data-ttu-id="61dcd-123">Seuraavien ohjeiden avulla voit määrittää työnkulkuprosessin ominaisuudet.</span><span class="sxs-lookup"><span data-stu-id="61dcd-123">Follow these steps to configure the properties of the workflow.</span></span>

1.  <span data-ttu-id="61dcd-124">Valitse alusta varmistaaksesi, että työnkulun elementtiä ei ole valittuna.</span><span class="sxs-lookup"><span data-stu-id="61dcd-124">Click the canvas to make sure that no workflow element is selected.</span></span>
2.  <span data-ttu-id="61dcd-125">Napsauta **Ominaisuudet** avataksesi **Ominaisuudet**-lomakkeen työnkululle.</span><span class="sxs-lookup"><span data-stu-id="61dcd-125">Click **Properties** to open the **Properties** page for the workflow.</span></span>
3.  <span data-ttu-id="61dcd-126">Noudata ohjeiden ohjeaiheessa [Työnkulun ominaisuuksien konfiguroiminen](configure-workflow-properties.md).</span><span class="sxs-lookup"><span data-stu-id="61dcd-126">Follow the procedures in the [Configure the properties of a workflow](configure-workflow-properties.md) topic.</span></span>

## <a name="configure-the-elements-of-the-workflow"></a><span data-ttu-id="61dcd-127">Työnkulun elementtien konfiguroiminen</span><span class="sxs-lookup"><span data-stu-id="61dcd-127">Configure the elements of the workflow</span></span>
<span data-ttu-id="61dcd-128">Määritä jokainen elementti, jonka vedit alustaan.</span><span class="sxs-lookup"><span data-stu-id="61dcd-128">Configure each element that you dragged onto the canvas.</span></span> <span data-ttu-id="61dcd-129">Lisätietoja kunkin työnkulkuelementin muokkaamisesta on seuraavissa ohjeaiheissa.</span><span class="sxs-lookup"><span data-stu-id="61dcd-129">For information about how to configure each workflow element, see the following topics:</span></span>

-   [<span data-ttu-id="61dcd-130">Manuaalisen tehtävän konfiguroiminen</span><span class="sxs-lookup"><span data-stu-id="61dcd-130">Configure a manual task</span></span>](configure-manual-task-workflow.md)
-   [<span data-ttu-id="61dcd-131">Automaattisen tehtävän määrittäminen</span><span class="sxs-lookup"><span data-stu-id="61dcd-131">Configure an automated task</span></span>](configure-automated-task-workflow.md)
-   [<span data-ttu-id="61dcd-132">Hyväksyntäprosessin konfiguroiminen</span><span class="sxs-lookup"><span data-stu-id="61dcd-132">Configure an approval process</span></span>](configure-approval-process-workflow.md)
-   [<span data-ttu-id="61dcd-133">Hyväksyntävaiheen konfiguroiminen</span><span class="sxs-lookup"><span data-stu-id="61dcd-133">Configure an approval step</span></span>](configure-approval-step-workflow.md)
-   [<span data-ttu-id="61dcd-134">Manuaalisen päätöksen konfiguroiminen</span><span class="sxs-lookup"><span data-stu-id="61dcd-134">Configure a manual decision</span></span>](configure-manual-decision-workflow.md)
-   [<span data-ttu-id="61dcd-135">Ehdollisen päätöksen konfiguroiminen</span><span class="sxs-lookup"><span data-stu-id="61dcd-135">Configure a conditional decision</span></span>](configure-conditional-decision-workflow.md)
-   [<span data-ttu-id="61dcd-136">Määritä rinnakkainen tehtävä</span><span class="sxs-lookup"><span data-stu-id="61dcd-136">Configure a parallel activity</span></span>](configure-parallel-activity-workflow.md)
-   [<span data-ttu-id="61dcd-137">Määritä rinnakkaishaara</span><span class="sxs-lookup"><span data-stu-id="61dcd-137">Configure a parallel branch</span></span>](configure-parallel-branch-workflow.md)
-   [<span data-ttu-id="61dcd-138">Määritä rivinimikkeen työnkulku</span><span class="sxs-lookup"><span data-stu-id="61dcd-138">Configure a line-item workflow</span></span>](configure-line-item-workflow.md)

## <a name="resolve-any-errors-or-warnings"></a><span data-ttu-id="61dcd-139">Korjaa mahdolliset virheet ja varoitukset</span><span class="sxs-lookup"><span data-stu-id="61dcd-139">Resolve any errors or warnings</span></span>
<span data-ttu-id="61dcd-140">Työnkulkueditorin alaosassa oleva **Virheet ja varoitukset** -ruutu näyttää työnkululle luodut sanomat.</span><span class="sxs-lookup"><span data-stu-id="61dcd-140">The **Errors and warnings** pane at the bottom of the workflow editor shows messages that have been generated for the workflow.</span></span> <span data-ttu-id="61dcd-141">Jos haluat paikallistaa elementin, jossa on tapahtunut virhe tai varoitus, kaksoisnapsauta virhe- tai varoitussanomaa.</span><span class="sxs-lookup"><span data-stu-id="61dcd-141">To find the element where an error or warning occurred, double-click the error or warning message.</span></span> <span data-ttu-id="61dcd-142">Kaikki virheet ja varoitukset on ratkaistava, ennen kuin työnkulun voi aktivoida.</span><span class="sxs-lookup"><span data-stu-id="61dcd-142">You must resolve all errors and warnings before you can make the workflow active.</span></span>

## <a name="save-and-activate-the-workflow"></a><span data-ttu-id="61dcd-143">Työnkulun tallennus ja aktivoiminen</span><span class="sxs-lookup"><span data-stu-id="61dcd-143">Save and activate the workflow</span></span>
<span data-ttu-id="61dcd-144">Kun olet valmis tallentamaan ja aktivoimaan työnkulun, noudata seuraavia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="61dcd-144">When you're ready to save and activate the workflow, follow these steps.</span></span>

1.  <span data-ttu-id="61dcd-145">Valitse **Tallenna ja sulje** sulkeaksesi työnkulkueditori ja avaa **Tallenna työnkulku** -sivu.</span><span class="sxs-lookup"><span data-stu-id="61dcd-145">Click **Save and close** to close the workflow editor and open the **Save workflow** page.</span></span>
2.  <span data-ttu-id="61dcd-146">Kirjoita kommentit työnkulkuun tekemistäsi muutoksista ja napsauta **OK**.</span><span class="sxs-lookup"><span data-stu-id="61dcd-146">Enter comments about the changes that you've made to the workflow, and then click **OK**.</span></span>
3.  <span data-ttu-id="61dcd-147">Jos kaikki virheet ja varoitukset on ratkaistu, **työnkulun aktivoiminen** -sivu tulee näkyviin.</span><span class="sxs-lookup"><span data-stu-id="61dcd-147">If all errors and warnings have been resolved, the **Activate workflow** page appears.</span></span> <span data-ttu-id="61dcd-148">Valitse jompikumpi seuraavista vaihtoehdoista:</span><span class="sxs-lookup"><span data-stu-id="61dcd-148">Select one of the following options:</span></span>
    -   <span data-ttu-id="61dcd-149">Voit aktivoida tämän työnkulun version valitsemalla **Ota uusi versio käyttöön**.</span><span class="sxs-lookup"><span data-stu-id="61dcd-149">To activate this version of the workflow, click **Activate the new version**.</span></span> <span data-ttu-id="61dcd-150">Kun työnkulku on aktiivinen, käyttäjät voivat lähettää siihen asiakirjoja käsittelyä varten.</span><span class="sxs-lookup"><span data-stu-id="61dcd-150">When a workflow is active, users can submit documents to it for processing.</span></span>
    -   <span data-ttu-id="61dcd-151">Jos et halua aktivoida versiota napsauta **Älä ota uutta versiota käyttöön**.</span><span class="sxs-lookup"><span data-stu-id="61dcd-151">If you don't want to activate this version, click **Do not activate the new version**.</span></span> <span data-ttu-id="61dcd-152">Voit ottaa työnkulun käyttöön myöhemmin.</span><span class="sxs-lookup"><span data-stu-id="61dcd-152">You can activate the workflow later.</span></span>






