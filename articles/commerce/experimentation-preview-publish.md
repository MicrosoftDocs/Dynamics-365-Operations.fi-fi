---
title: Kokeen esikatselu ja julkaisu
description: Tässä ohjeaiheessa käsitellään kokeen esikatselua ja julkaisua Dynamics 365 Commercessa.
author: sushma-rao
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 91e2e4840a2d53f195d881279050b6415d48b070
ms.sourcegitcommit: b6ab46f6e5ce60e2c3d70a348827eaf60c84cae2
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/01/2020
ms.locfileid: "3930189"
---
# <a name="preview-and-publish-an-experiment"></a><span data-ttu-id="f9e64-103">Kokeen esikatselu ja julkaisu</span><span class="sxs-lookup"><span data-stu-id="f9e64-103">Preview and publish an experiment</span></span>

<span data-ttu-id="f9e64-104">Tässä ohjeaiheessa käsitellään kokeen esikatselua ja julkaisua Dynamics 365 Commercessa sen jälkeen, kun [koe on yhdistetty ja variaatiot muokattu](experimentation-connect-edit.md).</span><span class="sxs-lookup"><span data-stu-id="f9e64-104">This topic describes how to preview and publish your experiment in Dynamics 365 Commerce after you've [connected your experiment and edited your variations](experimentation-connect-edit.md).</span></span> <span data-ttu-id="f9e64-105">Seuraavassa kaaviossa on kaikki vaiheet, jotka sisältyvät kokeen määrittämiseen ja suorittamiseen sähköisessä kaupankäyntisivustossa Dynamics 365 Commercessa.</span><span class="sxs-lookup"><span data-stu-id="f9e64-105">The following diagram shows all of the steps involved in setting up and running an experiment on an e-Commerce website in Dynamics 365 Commerce.</span></span> <span data-ttu-id="f9e64-106">Muut vaiheet käsitellään erillisissä ohjeaiheissa.</span><span class="sxs-lookup"><span data-stu-id="f9e64-106">Additional steps are covered in separate topics.</span></span>

<span data-ttu-id="f9e64-107">[ ![Kokeilun käyttäjän siirtymä – esikatselu ja julkaisu](./media/experimentation_preview_publish.svg) ](./media/experimentation_preview_publish.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="f9e64-107">[ ![Experimentation user journey - Preview & Publish](./media/experimentation_preview_publish.svg) ](./media/experimentation_preview_publish.svg#lightbox)</span></span>

## <a name="preview-your-experiment-variations"></a><span data-ttu-id="f9e64-108">Kokeen variaatioiden esikatselu</span><span class="sxs-lookup"><span data-stu-id="f9e64-108">Preview your experiment variations</span></span>
<span data-ttu-id="f9e64-109">Voit esikatsella variaatioita ja jatkaa niiden muokkausta, kunnes olet tyytyväinen niiden ulkoasuun.</span><span class="sxs-lookup"><span data-stu-id="f9e64-109">You can preview your variations and continue editing them until they look the way you want them to.</span></span>

1. <span data-ttu-id="f9e64-110">Valitse sivustonmuodostimessa komentopalkin alapuolella olevassa variaatioiden avattavassa valikossa esikatseltava sisältö.</span><span class="sxs-lookup"><span data-stu-id="f9e64-110">In site builder, use the variations drop-down menu below the command bar to select the content you want to preview.</span></span> 
1. <span data-ttu-id="f9e64-111">Valitse yläpalkissa **Esikatselu**.</span><span class="sxs-lookup"><span data-stu-id="f9e64-111">Select **Preview** in the top bar.</span></span> <span data-ttu-id="f9e64-112">Esikatselussa nähdään, miltä sisältö näyttää julkaistuna.</span><span class="sxs-lookup"><span data-stu-id="f9e64-112">A preview of what the content will look like when it's published is displayed.</span></span>
1. <span data-ttu-id="f9e64-113">Jos haluat esikatsella toisen variaation, valitse se avattavasta variaatioluettelosta ja valitse sitten **Esikatselu** uudelleen.</span><span class="sxs-lookup"><span data-stu-id="f9e64-113">To preview a different variation, select it from the variation drop-down and select **Preview** again.</span></span>

## <a name="publish-your-experiment"></a><span data-ttu-id="f9e64-114">Kokeen julkaiseminen</span><span class="sxs-lookup"><span data-stu-id="f9e64-114">Publish your experiment</span></span>
<span data-ttu-id="f9e64-115">Jos et käytä julkaisuryhmää aikatauluttamiseen, kun koe siirtyy live-tilaan ja haluat julkaista heti, valitse komentopalkissa **Julkaisu**.</span><span class="sxs-lookup"><span data-stu-id="f9e64-115">If you aren't using a publish group to schedule when your experiment goes live and you want to publish immediately, select **Publish** in the command bar.</span></span> <span data-ttu-id="f9e64-116">Kaikki kokeeseen kuuluvat variaatiot julkaistaan.</span><span class="sxs-lookup"><span data-stu-id="f9e64-116">All variations that belong to the experiment will be published.</span></span>
    
> [!IMPORTANT]
> <span data-ttu-id="f9e64-117">Jos sivulla on julkaisematon URL-osoite, URL-osoite on ensin julkaistava tai se ei näy sivuston käyttäjille.</span><span class="sxs-lookup"><span data-stu-id="f9e64-117">If the page has an unpublished URL, you must first publish the URL or it won't be visible to your website users.</span></span> <span data-ttu-id="f9e64-118">Lisätietoja kohdassa [Sivun tallentaminen, esikatseleminen ja julkaiseminen](save-preview-publish-page.md).</span><span class="sxs-lookup"><span data-stu-id="f9e64-118">For details, see [Save, preview, and publish a page](save-preview-publish-page.md).</span></span>
    
### <a name="use-publish-groups-to-schedule-when-your-experiment-goes-live"></a><span data-ttu-id="f9e64-119">Kokeen live-tilaan siirtämisen aikatauluttaminen julkaisuryhmien avulla</span><span class="sxs-lookup"><span data-stu-id="f9e64-119">Use publish groups to schedule when your experiment goes live</span></span>
<span data-ttu-id="f9e64-120">Sivustonmuodostimessa luodut variaatiot voidaan aikatauluttaa julkaistaviksi käyttämällä julkaisuryhmää.</span><span class="sxs-lookup"><span data-stu-id="f9e64-120">Variations created in site builder can be scheduled for publishing by using a publish group.</span></span> <span data-ttu-id="f9e64-121">Julkaisuryhmässä voi yhdistää sivun tai osan kokeeseen siirtymällä **Kokeet**-välilehteen tai **Sivut**- ja **Osat**-välilehteen. Lisätietoja on kohdassa [Kokeen yhdistäminen ja variaatioiden muokkaaminen](experimentation-connect-edit.md).</span><span class="sxs-lookup"><span data-stu-id="f9e64-121">Within a publish group, you can connect a page or fragment to your experiment by going to the **Experiments** tab or the **Pages** or **Fragments** tab. For more information, see [Connect an experiment and edit variations](experimentation-connect-edit.md) topic.</span></span> <span data-ttu-id="f9e64-122">Lisätietoja julkaisuryhmistä on kohdassa [Julkaisuryhmien kanssa työskenteleminen](publish-groups.md).</span><span class="sxs-lookup"><span data-stu-id="f9e64-122">For information about publish groups, see [Work with publish groups](publish-groups.md).</span></span>

<span data-ttu-id="f9e64-123">Kun julkaisuryhmiä käytetään kokeissa, tietyt tärkeät seikat on otettava huomioon.</span><span class="sxs-lookup"><span data-stu-id="f9e64-123">When using publish groups with experiments, there are some important considerations to be aware of.</span></span>
- <span data-ttu-id="f9e64-124">Kun sivu tai osa, jossa koe on käynnissä, lisätään julkaisuryhmään, koe poistetaan julkaisuryhmän sivulta tai osasta.</span><span class="sxs-lookup"><span data-stu-id="f9e64-124">When you add a page or fragment that has an experiment running on it to a publish group, the experiment will be removed from the page or fragment in the publish group.</span></span>
- <span data-ttu-id="f9e64-125">Live-sivuston sivuihin yhdistetyt kokeet eivät ole käytettävissä julkaisuryhmien sivulla ja päin vastoin.</span><span class="sxs-lookup"><span data-stu-id="f9e64-125">Experiments that are connected to pages in a live site aren't available to pages within publish groups and vice-versa.</span></span> <span data-ttu-id="f9e64-126">Vastaavasti sivut, joissa on live-sivustossa käytössä olevia kokeita, eivät ole muiden kokeiden käytettävissä julkaisuryhmissä ja päin vastoin.</span><span class="sxs-lookup"><span data-stu-id="f9e64-126">Similarly, pages that have experiments running on them in a live site aren't available to other experiments in publish groups and vice versa.</span></span>
- <span data-ttu-id="f9e64-127">Kun julkaiset tai aikataulutat julkaisuryhmän, koko julkaisuryhmän sisältö julkaistaan riippumatta siitä, onko julkaisuryhmään liitetty koe vai ei.</span><span class="sxs-lookup"><span data-stu-id="f9e64-127">When you publish or schedule a publish group, all content in the publish group is published, regardless of whether there's an experiment associated with the publish group.</span></span>
- <span data-ttu-id="f9e64-128">Koska julkaisuryhmä jää pysyväksi, kun se on julkaistu live-sivustoon, myös julkaisuryhmässä olevat kokeet jäävät pysyviksi.</span><span class="sxs-lookup"><span data-stu-id="f9e64-128">Because a publish group continues to persist after it's been published to a live site, experiments in the publish group will also persist.</span></span> <span data-ttu-id="f9e64-129">Tämän vuoksi muita kokeita voi liittää samalla sivulla tai samassa ryhmässä.</span><span class="sxs-lookup"><span data-stu-id="f9e64-129">Therefore, you won't be able to associate other experiments with the same page or fragment.</span></span> <span data-ttu-id="f9e64-130">Tämä rajoitus voidaan välttää poistamalla kaikki julkaisuryhmät, joissa on pysyviä kokeita.</span><span class="sxs-lookup"><span data-stu-id="f9e64-130">To avoid this limitation, delete any publish groups with persisting experiments.</span></span> <span data-ttu-id="f9e64-131">Jos vastaavasti poista kokeen live-sivustossa, joka on myös julkaisuryhmässä, poista se ensin julkaisuryhmästä.</span><span class="sxs-lookup"><span data-stu-id="f9e64-131">Similarly, if you want to delete an experiment in a live site that also exists in a publish group, delete it from the publish group first.</span></span>

## <a name="previous-step"></a><span data-ttu-id="f9e64-132">Edellinen vaihe</span><span class="sxs-lookup"><span data-stu-id="f9e64-132">Previous step</span></span>
[<span data-ttu-id="f9e64-133">Kokeilun yhdistäminen ja muokkaaminen</span><span class="sxs-lookup"><span data-stu-id="f9e64-133">Connect and edit an experiment</span></span>](experimentation-connect-edit.md)

## <a name="next-step"></a><span data-ttu-id="f9e64-134">Seuraava vaihe</span><span class="sxs-lookup"><span data-stu-id="f9e64-134">Next step</span></span>
[<span data-ttu-id="f9e64-135">Kokeen suorittaminen ja seuranta</span><span class="sxs-lookup"><span data-stu-id="f9e64-135">Run and monitor an experiment</span></span>](experimentation-run-monitor.md)
