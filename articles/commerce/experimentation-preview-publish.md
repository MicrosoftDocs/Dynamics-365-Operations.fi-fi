---
title: Kokeen esikatselu ja julkaisu
description: Tässä ohjeaiheessa käsitellään kokeen esikatselua ja julkaisua Dynamics 365 Commercessa.
author: sushma-rao
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 52ca23e5aaeb7058853fed2241d5804180fa7f8d
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5798960"
---
# <a name="preview-and-publish-an-experiment"></a><span data-ttu-id="fa256-103">Kokeen esikatselu ja julkaisu</span><span class="sxs-lookup"><span data-stu-id="fa256-103">Preview and publish an experiment</span></span>

<span data-ttu-id="fa256-104">Tässä ohjeaiheessa käsitellään kokeen esikatselua ja julkaisua Dynamics 365 Commercessa sen jälkeen, kun [koe on yhdistetty ja variaatiot muokattu](experimentation-connect-edit.md).</span><span class="sxs-lookup"><span data-stu-id="fa256-104">This topic describes how to preview and publish your experiment in Dynamics 365 Commerce after you've [connected your experiment and edited your variations](experimentation-connect-edit.md).</span></span> <span data-ttu-id="fa256-105">Seuraavassa kaaviossa on kaikki vaiheet, jotka sisältyvät kokeen määrittämiseen ja suorittamiseen sähköisessä kaupankäyntisivustossa Dynamics 365 Commercessa.</span><span class="sxs-lookup"><span data-stu-id="fa256-105">The following diagram shows all of the steps involved in setting up and running an experiment on an e-Commerce website in Dynamics 365 Commerce.</span></span> <span data-ttu-id="fa256-106">Muut vaiheet käsitellään erillisissä ohjeaiheissa.</span><span class="sxs-lookup"><span data-stu-id="fa256-106">Additional steps are covered in separate topics.</span></span>

<span data-ttu-id="fa256-107">[ ![Kokeilun käyttäjän siirtymä – esikatselu ja julkaisu](./media/experimentation_preview_publish.svg) ](./media/experimentation_preview_publish.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="fa256-107">[ ![Experimentation user journey - Preview & Publish](./media/experimentation_preview_publish.svg) ](./media/experimentation_preview_publish.svg#lightbox)</span></span>

## <a name="preview-your-experiment-variations"></a><span data-ttu-id="fa256-108">Kokeen variaatioiden esikatselu</span><span class="sxs-lookup"><span data-stu-id="fa256-108">Preview your experiment variations</span></span>
<span data-ttu-id="fa256-109">Voit esikatsella variaatioita ja jatkaa niiden muokkausta, kunnes olet tyytyväinen niiden ulkoasuun.</span><span class="sxs-lookup"><span data-stu-id="fa256-109">You can preview your variations and continue editing them until they look the way you want them to.</span></span>

<span data-ttu-id="fa256-110">Koevariaatioita voi esikatsella Commercen sivustonmuodostimessa seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="fa256-110">To preview your experiment variations in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="fa256-111">Valitse komentopalkin alapuolella olevassa avattavassa variaatiovalikossa esikatseltava sisältö.</span><span class="sxs-lookup"><span data-stu-id="fa256-111">From the variations drop-down menu below the command bar, select the content you want to preview.</span></span> 
1. <span data-ttu-id="fa256-112">Valitse komentopalkissa **Esikatsele**.</span><span class="sxs-lookup"><span data-stu-id="fa256-112">On the command bar, select **Preview**.</span></span> <span data-ttu-id="fa256-113">Esikatselussa nähdään, miltä sisältö näyttää julkaistuna.</span><span class="sxs-lookup"><span data-stu-id="fa256-113">A preview of what the content will look like when it's published is displayed.</span></span>
1. <span data-ttu-id="fa256-114">Jos haluat esikatsella toisen variaation, valitse se avattavasta variaatiovalikosta ja valitse sitten **Esikatselu** uudelleen.</span><span class="sxs-lookup"><span data-stu-id="fa256-114">To preview a different variation, select it from the variation drop-down menu and select **Preview** again.</span></span>

## <a name="publish-your-experiment"></a><span data-ttu-id="fa256-115">Kokeen julkaiseminen</span><span class="sxs-lookup"><span data-stu-id="fa256-115">Publish your experiment</span></span>
<span data-ttu-id="fa256-116">Jos et käytä julkaisuryhmää aikatauluttamiseen, kun koe siirtyy live-tilaan ja haluat julkaista heti, valitse komentopalkissa **Julkaisu**.</span><span class="sxs-lookup"><span data-stu-id="fa256-116">If you aren't using a publish group to schedule when your experiment goes live and you want to publish immediately, select **Publish** in the command bar.</span></span> <span data-ttu-id="fa256-117">Kaikki kokeeseen kuuluvat variaatiot julkaistaan.</span><span class="sxs-lookup"><span data-stu-id="fa256-117">All variations that belong to the experiment will be published.</span></span>
    
> [!IMPORTANT]
> <span data-ttu-id="fa256-118">Jos sivulla on julkaisematon URL-osoite, URL-osoite on ensin julkaistava tai se ei näy sivuston käyttäjille.</span><span class="sxs-lookup"><span data-stu-id="fa256-118">If the page has an unpublished URL, you must first publish the URL or it won't be visible to your website users.</span></span> <span data-ttu-id="fa256-119">Lisätietoja kohdassa [Sivun tallentaminen, esikatseleminen ja julkaiseminen](save-preview-publish-page.md).</span><span class="sxs-lookup"><span data-stu-id="fa256-119">For details, see [Save, preview, and publish a page](save-preview-publish-page.md).</span></span>
    
### <a name="use-publish-groups-to-schedule-when-your-experiment-goes-live"></a><span data-ttu-id="fa256-120">Kokeen live-tilaan siirtämisen aikatauluttaminen julkaisuryhmien avulla</span><span class="sxs-lookup"><span data-stu-id="fa256-120">Use publish groups to schedule when your experiment goes live</span></span>
<span data-ttu-id="fa256-121">Sivustonmuodostimessa luodut variaatiot voidaan aikatauluttaa julkaistaviksi käyttämällä julkaisuryhmää.</span><span class="sxs-lookup"><span data-stu-id="fa256-121">Variations created in site builder can be scheduled for publishing by using a publish group.</span></span> <span data-ttu-id="fa256-122">Sivun tai osan voi yhdistää julkaisuryhmässä kokeeseen valitsemalla vasemmassa siirtymisruudussa **Kokeet**.</span><span class="sxs-lookup"><span data-stu-id="fa256-122">Within a publish group, you can connect a page or fragment to your experiment by selecting **Experiments** in the left navigation pane.</span></span> <span data-ttu-id="fa256-123">Se on mahdollista myös valitsemalla **Sivut** tai **Osat** ja noudattamalla ohjeita kohdassa [Kokeen yhdistäminen ja variaatioiden muokkaaminen](experimentation-connect-edit.md).</span><span class="sxs-lookup"><span data-stu-id="fa256-123">You can also do this by selecting **Pages** or **Fragments** and following the instructions in [Connect an experiment and edit variations](experimentation-connect-edit.md).</span></span> <span data-ttu-id="fa256-124">Lisätietoja julkaisuryhmistä on kohdassa [Julkaisuryhmien kanssa työskenteleminen](publish-groups.md).</span><span class="sxs-lookup"><span data-stu-id="fa256-124">For information about publish groups, see [Work with publish groups](publish-groups.md).</span></span>

<span data-ttu-id="fa256-125">Kun julkaisuryhmiä käytetään kokeissa, tietyt tärkeät seikat on otettava huomioon.</span><span class="sxs-lookup"><span data-stu-id="fa256-125">When using publish groups with experiments, there are some important considerations to be aware of.</span></span>
- <span data-ttu-id="fa256-126">Kun sivu tai osa, jossa koe on käynnissä, lisätään julkaisuryhmään, koe poistetaan julkaisuryhmän sivulta tai osasta.</span><span class="sxs-lookup"><span data-stu-id="fa256-126">When you add a page or fragment that has an experiment running on it to a publish group, the experiment will be removed from the page or fragment in the publish group.</span></span>
- <span data-ttu-id="fa256-127">Live-sivuston sivuihin yhdistetyt kokeet eivät ole käytettävissä julkaisuryhmien sivulla ja päin vastoin.</span><span class="sxs-lookup"><span data-stu-id="fa256-127">Experiments that are connected to pages in a live site aren't available to pages within publish groups and vice-versa.</span></span> <span data-ttu-id="fa256-128">Vastaavasti sivut, joissa on live-sivustossa käytössä olevia kokeita, eivät ole muiden kokeiden käytettävissä julkaisuryhmissä ja päin vastoin.</span><span class="sxs-lookup"><span data-stu-id="fa256-128">Similarly, pages that have experiments running on them in a live site aren't available to other experiments in publish groups and vice versa.</span></span>
- <span data-ttu-id="fa256-129">Kun julkaiset tai aikataulutat julkaisuryhmän, koko julkaisuryhmän sisältö julkaistaan riippumatta siitä, onko julkaisuryhmään liitetty koe vai ei.</span><span class="sxs-lookup"><span data-stu-id="fa256-129">When you publish or schedule a publish group, all content in the publish group is published, regardless of whether there's an experiment associated with the publish group.</span></span>
- <span data-ttu-id="fa256-130">Koska julkaisuryhmä jää pysyväksi, kun se on julkaistu live-sivustoon, myös julkaisuryhmässä olevat kokeet jäävät pysyviksi.</span><span class="sxs-lookup"><span data-stu-id="fa256-130">Because a publish group continues to persist after it's been published to a live site, experiments in the publish group will also persist.</span></span> <span data-ttu-id="fa256-131">Tämän vuoksi muita kokeita voi liittää samalla sivulla tai samassa ryhmässä.</span><span class="sxs-lookup"><span data-stu-id="fa256-131">Therefore, you won't be able to associate other experiments with the same page or fragment.</span></span> <span data-ttu-id="fa256-132">Tämä rajoitus voidaan välttää poistamalla kaikki julkaisuryhmät, joissa on pysyviä kokeita.</span><span class="sxs-lookup"><span data-stu-id="fa256-132">To avoid this limitation, delete any publish groups with persisting experiments.</span></span> <span data-ttu-id="fa256-133">Jos vastaavasti poista kokeen live-sivustossa, joka on myös julkaisuryhmässä, poista se ensin julkaisuryhmästä.</span><span class="sxs-lookup"><span data-stu-id="fa256-133">Similarly, if you want to delete an experiment in a live site that also exists in a publish group, delete it from the publish group first.</span></span>

## <a name="previous-step"></a><span data-ttu-id="fa256-134">Edellinen vaihe</span><span class="sxs-lookup"><span data-stu-id="fa256-134">Previous step</span></span>
[<span data-ttu-id="fa256-135">Kokeilun yhdistäminen ja muokkaaminen</span><span class="sxs-lookup"><span data-stu-id="fa256-135">Connect and edit an experiment</span></span>](experimentation-connect-edit.md)

## <a name="next-step"></a><span data-ttu-id="fa256-136">Seuraava vaihe</span><span class="sxs-lookup"><span data-stu-id="fa256-136">Next step</span></span>
[<span data-ttu-id="fa256-137">Kokeen suorittaminen ja seuranta</span><span class="sxs-lookup"><span data-stu-id="fa256-137">Run and monitor an experiment</span></span>](experimentation-run-monitor.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]