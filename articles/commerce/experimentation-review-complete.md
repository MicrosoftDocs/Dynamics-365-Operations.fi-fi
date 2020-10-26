---
title: Variaation määrittäminen ja kokeen päättäminen
description: Tässä ohjeaiheessa käsitellään onnistuneen variaation korottamista ja kokeen päättämistä Dynamics 365 Commercessa.
author: sushma-rao
manager: AnnBe
ms.date: 09/15/2020
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
ms.openlocfilehash: 2e011f10e908d6a2efe2e928fc5e0abc7659cb8b
ms.sourcegitcommit: b6ab46f6e5ce60e2c3d70a348827eaf60c84cae2
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/01/2020
ms.locfileid: "3930184"
---
# <a name="promote-a-variation-and-complete-an-experiment"></a><span data-ttu-id="f0998-103">Variaation määrittäminen ja kokeen päättäminen</span><span class="sxs-lookup"><span data-stu-id="f0998-103">Promote a variation and complete an experiment</span></span>

<span data-ttu-id="f0998-104">Tässä ohjeaiheessa käsitellään kokeessa parhaan tuloksen tuottaneen variaation korottamista ja kokeen päättämistä.</span><span class="sxs-lookup"><span data-stu-id="f0998-104">This topic describes how to promote the variation that produced the best results in your experiment, and how to complete the experiment.</span></span> <span data-ttu-id="f0998-105">Seuraavassa kaaviossa on kaikki vaiheet, jotka sisältyvät kokeen määrittämiseen ja suorittamiseen sähköisessä kaupankäyntisivustossa Dynamics 365 Commercessa.</span><span class="sxs-lookup"><span data-stu-id="f0998-105">The following diagram shows all of the steps involved in setting up and running an experiment on an e-Commerce website in Dynamics 365 Commerce.</span></span> <span data-ttu-id="f0998-106">Muut vaiheet käsitellään erillisissä ohjeaiheissa.</span><span class="sxs-lookup"><span data-stu-id="f0998-106">Additional steps are covered in separate topics.</span></span>

<span data-ttu-id="f0998-107">[ ![Kokeilun käyttäjän siirtymä – arviointi ja päättäminen](./media/experimentation_review_complete.svg) ](./media/experimentation_review_complete.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="f0998-107">[ ![Experimentation user journey - Review & Complete](./media/experimentation_review_complete.svg) ](./media/experimentation_review_complete.svg#lightbox)</span></span>

<span data-ttu-id="f0998-108">Kun [koe on suoritettu](experimentation-run-monitor.md) ja on kerätty riittävästi tietoa sen määrittämiseen, mitä variaatiota halutaan käyttää live-sivustossa, variaatio korotetaan ja koe lopetetaan.</span><span class="sxs-lookup"><span data-stu-id="f0998-108">After you've [run your experiment](experimentation-run-monitor.md) and collected sufficient data to determine which variation you want to use on your live site, you'll promote the variation and end the experiment.</span></span>

## <a name="promote-a-variation"></a><span data-ttu-id="f0998-109">Variaation korottaminen</span><span class="sxs-lookup"><span data-stu-id="f0998-109">Promote a variation</span></span>
<span data-ttu-id="f0998-110">Kolmannen osapuolen palvelussa suoritettuun kokeeseen liittyvien tietojen ja analyysien avulla voi päättää, millä variaatiolla saatiin parhaat tulokset.</span><span class="sxs-lookup"><span data-stu-id="f0998-110">Use the data and analytics related to the experiment in the third-party service to decide which variation produced the best results.</span></span> <span data-ttu-id="f0998-111">Live-sivuston nykyisen sisällön voi korvata voittajavariaatiolla siten, että se on kaikkien käyttäjien käytettävissä, toimimalla seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="f0998-111">To replace the current content on the live site with the winning variation so that it's available to all users of your website, do the following.</span></span> 

1. <span data-ttu-id="f0998-112">Siirry sivustonmuodostimessa **Kokeet**-välilehteen ja valitse koe.</span><span class="sxs-lookup"><span data-stu-id="f0998-112">Go to the **Experiments** tab in site builder and select the experiment.</span></span>
1. <span data-ttu-id="f0998-113">Valitse yläpalkissa **Päätä koe**.</span><span class="sxs-lookup"><span data-stu-id="f0998-113">Select **Complete experiment** on the top bar.</span></span>
1. <span data-ttu-id="f0998-114">Valitse **Päätä koe** -valintaikkunassa **Arvioi kokeen tiedot**.</span><span class="sxs-lookup"><span data-stu-id="f0998-114">In the **Complete the experiment** dialog menu, select **Review the experiment data**.</span></span> <span data-ttu-id="f0998-115">Voit arvioida avautuvassa kolmannen osapuolen palvelussa mittareita ja määrittää, mikä variaatio suoriutui parhaiten.</span><span class="sxs-lookup"><span data-stu-id="f0998-115">The third-party service opens where you can validate the metrics and determine which variation performed the best.</span></span>
1. <span data-ttu-id="f0998-116">Valitse sivustonmuodostimen **Päätä koe** -valintaikkunassa voittajavariaatio ja valitse sitten **Seuraava**.</span><span class="sxs-lookup"><span data-stu-id="f0998-116">In the **Complete the experiment** dialog menu in site builder, select the winning variation and then select **Next**.</span></span>
1. <span data-ttu-id="f0998-117">Avaa kolmannen osapuolen palvelu ja pysäytä kokeilu.</span><span class="sxs-lookup"><span data-stu-id="f0998-117">Open the third-party service and stop the experiment.</span></span>
1. <span data-ttu-id="f0998-118">Valitse sivustonmuodostimessa **Päätä**. jolloin alkuperäinen live-sivusto korvataan ja voittajavariaatio julkaistaan. Sen jälkeen kyseinen variaatio on kaikkien sivuston käyttäjien käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="f0998-118">In site builder, select **Complete** to overwrite the original live page and publish the winning variation so that it's available to all users of your website.</span></span> 

> [!NOTE]
> <span data-ttu-id="f0998-119">Jos valitset nykyisen live-sivun säilyttämisen etkä julkaise variaatiota, valitse **Julkaise alkuperäinen sivu uudelleen**.</span><span class="sxs-lookup"><span data-stu-id="f0998-119">If you choose to keep the current live page and not publish a variation, select **Republish the original page**.</span></span>

## <a name="delete-your-experiment"></a><span data-ttu-id="f0998-120">Kokeen poistaminen</span><span class="sxs-lookup"><span data-stu-id="f0998-120">Delete your experiment</span></span>
<span data-ttu-id="f0998-121">Vaikka Commercessa päättynyttä koetta ei ole pakko poistaa, sen voi poistaa, mikä säästää tilaa ja siistii työntilaa.</span><span class="sxs-lookup"><span data-stu-id="f0998-121">While it's not required that you delete a completed experiment in Commerce, you may choose to delete it to save space or clean up your workspace.</span></span> <span data-ttu-id="f0998-122">Poista koe seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="f0998-122">To delete an experiment, do the following.</span></span>

1. <span data-ttu-id="f0998-123">Siirry sivustonmuodostimessa **Kokeet**-välilehteen ja valitse koe.</span><span class="sxs-lookup"><span data-stu-id="f0998-123">Go to the **Experiments** tab in site builder and select the experiment.</span></span> 
    > [!NOTE]
    > <span data-ttu-id="f0998-124">Jos koe on edelleen aktiivinen, lopeta koe kolmannen osapuolen palvelussa ennen jatkamista.</span><span class="sxs-lookup"><span data-stu-id="f0998-124">If the experiment is still active, stop the experiment in the third-party service before proceeding.</span></span>
1. <span data-ttu-id="f0998-125">Poista variaatiosisältö live-sivustosta valitsemalla komentopalkissa **Peruuta julkaisu**.</span><span class="sxs-lookup"><span data-stu-id="f0998-125">Select **Unpublish** in the command bar to remove the variation content from the live site.</span></span>
1. <span data-ttu-id="f0998-126">Poista koe valitsemalla komentopalkissa **Poista**.</span><span class="sxs-lookup"><span data-stu-id="f0998-126">Select **Delete** in the command bar to delete the experiment.</span></span>

## <a name="previous-step"></a><span data-ttu-id="f0998-127">Edellinen vaihe</span><span class="sxs-lookup"><span data-stu-id="f0998-127">Previous step</span></span>
[<span data-ttu-id="f0998-128">Kokeen suorittaminen ja seuranta</span><span class="sxs-lookup"><span data-stu-id="f0998-128">Run and monitor an experiment</span></span>](experimentation-run-monitor.md)
