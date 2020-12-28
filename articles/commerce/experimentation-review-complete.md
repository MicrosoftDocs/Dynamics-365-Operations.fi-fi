---
title: Variaation määrittäminen ja kokeen päättäminen
description: Tässä ohjeaiheessa käsitellään onnistuneen variaation korottamista ja kokeen päättämistä Dynamics 365 Commercessa.
author: sushma-rao
manager: AnnBe
ms.date: 10/21/2020
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
ms.openlocfilehash: c7da601323663d4c1ea76f7cad7bdab8e7632d1c
ms.sourcegitcommit: cd83f2bc0e52e13071ad306e07e4c255fc65cb03
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/22/2020
ms.locfileid: "4412114"
---
# <a name="promote-a-variation-and-complete-an-experiment"></a><span data-ttu-id="6aac1-103">Variaation määrittäminen ja kokeen päättäminen</span><span class="sxs-lookup"><span data-stu-id="6aac1-103">Promote a variation and complete an experiment</span></span>

<span data-ttu-id="6aac1-104">Tässä ohjeaiheessa käsitellään kokeessa parhaan tuloksen tuottaneen variaation korottamista ja kokeen päättämistä.</span><span class="sxs-lookup"><span data-stu-id="6aac1-104">This topic describes how to promote the variation that produced the best results in your experiment, and how to complete the experiment.</span></span> <span data-ttu-id="6aac1-105">Seuraavassa kaaviossa on kaikki vaiheet, jotka sisältyvät kokeen määrittämiseen ja suorittamiseen sähköisessä kaupankäyntisivustossa Dynamics 365 Commercessa.</span><span class="sxs-lookup"><span data-stu-id="6aac1-105">The following diagram shows all of the steps involved in setting up and running an experiment on an e-Commerce website in Dynamics 365 Commerce.</span></span> <span data-ttu-id="6aac1-106">Muut vaiheet käsitellään erillisissä ohjeaiheissa.</span><span class="sxs-lookup"><span data-stu-id="6aac1-106">Additional steps are covered in separate topics.</span></span>

<span data-ttu-id="6aac1-107">[ ![Kokeilun käyttäjän siirtymä – arviointi ja päättäminen](./media/experimentation_review_complete.svg) ](./media/experimentation_review_complete.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="6aac1-107">[ ![Experimentation user journey - Review & Complete](./media/experimentation_review_complete.svg) ](./media/experimentation_review_complete.svg#lightbox)</span></span>

<span data-ttu-id="6aac1-108">Kun [koe on suoritettu](experimentation-run-monitor.md) ja on kerätty riittävästi tietoa sen määrittämiseen, mitä variaatiota halutaan käyttää live-sivustossa, variaatio korotetaan ja koe lopetetaan.</span><span class="sxs-lookup"><span data-stu-id="6aac1-108">After you've [run your experiment](experimentation-run-monitor.md) and collected sufficient data to determine which variation you want to use on your live site, you'll promote the variation and end the experiment.</span></span>

## <a name="promote-a-variation"></a><span data-ttu-id="6aac1-109">Variaation korottaminen</span><span class="sxs-lookup"><span data-stu-id="6aac1-109">Promote a variation</span></span>
<span data-ttu-id="6aac1-110">Kolmannen osapuolen palvelussa suoritettuun kokeeseen liittyvien tietojen ja analyysien avulla voi päättää, millä variaatiolla saatiin parhaat tulokset.</span><span class="sxs-lookup"><span data-stu-id="6aac1-110">Use the data and analytics related to the experiment in the third-party service to decide which variation produced the best results.</span></span> <span data-ttu-id="6aac1-111">Sen voi sitten korottaa korvaamalla live-sivuston nykyisen sisällön voittajavariaatiolla siten, että se on kaikkien käyttäjien käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="6aac1-111">You can then promote it by replacing the current content on the live site with the winning variation so that it's available to all users of your website.</span></span>

<span data-ttu-id="6aac1-112">Voittajavariaatio korotetaan seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="6aac1-112">To promote the winning variation, follow these steps.</span></span> 

1. <span data-ttu-id="6aac1-113">Valitse Commercen sivustonmuodostimen vasemmassa siirtymisruudussa ensin **Kokeet** ja sitten koe.</span><span class="sxs-lookup"><span data-stu-id="6aac1-113">In Commerce site builder, select **Experiments** in the left navigation pane, and then select the experiment.</span></span>
1. <span data-ttu-id="6aac1-114">Valitse komentopalkissa **Päätä koe**.</span><span class="sxs-lookup"><span data-stu-id="6aac1-114">On the command bar, select **Complete experiment**.</span></span>
1. <span data-ttu-id="6aac1-115">Valitse **Päätä koe** -valintaikkunassa **Arvioi kokeen tiedot**.</span><span class="sxs-lookup"><span data-stu-id="6aac1-115">In the **Complete the experiment** dialog box, select **Review the experiment data**.</span></span> <span data-ttu-id="6aac1-116">Voit arvioida avautuvassa kolmannen osapuolen palvelussa mittareita ja määrittää, mikä variaatio suoriutui parhaiten.</span><span class="sxs-lookup"><span data-stu-id="6aac1-116">The third-party service opens where you can validate the metrics and determine which variation performed the best.</span></span>
1. <span data-ttu-id="6aac1-117">Valitse **Päätä koe** -valintaikkunassa voittajavariaatio ja valitse sitten **Seuraava**.</span><span class="sxs-lookup"><span data-stu-id="6aac1-117">In the **Complete the experiment** dialog box, select the winning variation, and then select **Next**.</span></span>
1. <span data-ttu-id="6aac1-118">Avaa kolmannen osapuolen palvelu ja pysäytä kokeilu.</span><span class="sxs-lookup"><span data-stu-id="6aac1-118">Open the third-party service and stop the experiment.</span></span>
1. <span data-ttu-id="6aac1-119">Valitse sivustonmuodostimessa **Päätä**. jolloin alkuperäinen live-sivusto korvataan ja voittajavariaatio julkaistaan. Sen jälkeen kyseinen variaatio on kaikkien sivuston käyttäjien käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="6aac1-119">In site builder, select **Complete** to overwrite the original live page and publish the winning variation so that it's available to all users of your website.</span></span> 

> [!NOTE]
> <span data-ttu-id="6aac1-120">Jos valitset nykyisen live-sivun säilyttämisen etkä julkaise variaatiota, valitse **Julkaise alkuperäinen sivu uudelleen**.</span><span class="sxs-lookup"><span data-stu-id="6aac1-120">If you choose to keep the current live page and not publish a variation, select **Republish the original page**.</span></span>

## <a name="delete-your-experiment"></a><span data-ttu-id="6aac1-121">Kokeen poistaminen</span><span class="sxs-lookup"><span data-stu-id="6aac1-121">Delete your experiment</span></span>
<span data-ttu-id="6aac1-122">Vaikka Commercessa päättynyttä koetta ei ole pakko poistaa, sen voi poistaa, mikä säästää tilaa ja siistii työntilaa.</span><span class="sxs-lookup"><span data-stu-id="6aac1-122">While it's not required that you delete a completed experiment in Commerce, you may choose to delete it to save space or clean up your workspace.</span></span> 

<span data-ttu-id="6aac1-123">Kokeen voi poistaa Commercen sivustonmuodostimessa seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="6aac1-123">To delete an experiment in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="6aac1-124">Valitse Commercen vasemmassa siirtymisruudussa ensin **Kokeet** ja sitten koe.</span><span class="sxs-lookup"><span data-stu-id="6aac1-124">Select **Experiments** in the left navigation pane, and then select the experiment.</span></span> 
    > [!NOTE]
    > <span data-ttu-id="6aac1-125">Jos koe on edelleen aktiivinen, lopeta koe kolmannen osapuolen palvelussa ennen jatkamista.</span><span class="sxs-lookup"><span data-stu-id="6aac1-125">If the experiment is still active, stop the experiment in the third-party service before proceeding.</span></span>
1. <span data-ttu-id="6aac1-126">Poista variaatiosisältö live-sivustosta valitsemalla komentopalkissa **Peruuta julkaisu**.</span><span class="sxs-lookup"><span data-stu-id="6aac1-126">On the command bar, select **Unpublish**  to remove the variation content from the live site.</span></span>
1. <span data-ttu-id="6aac1-127">Poista koe valitsemalla **Poista**.</span><span class="sxs-lookup"><span data-stu-id="6aac1-127">Select **Delete** to delete the experiment.</span></span>

## <a name="previous-step"></a><span data-ttu-id="6aac1-128">Edellinen vaihe</span><span class="sxs-lookup"><span data-stu-id="6aac1-128">Previous step</span></span>
[<span data-ttu-id="6aac1-129">Kokeilun suoritus ja seuranta</span><span class="sxs-lookup"><span data-stu-id="6aac1-129">Run and monitor an experiment</span></span>](experimentation-run-monitor.md)
