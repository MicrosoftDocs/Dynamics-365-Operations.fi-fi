---
title: Kokeen yhdistäminen ja variaatioiden muokkaaminen
description: Tässä ohjeaiheessa käsitellään kolmannen osapuolen palvelussa olevan kokeen yhdistämistä Dynamics 365 Commerceen ja kokeen variaatioiden muokkaamista.
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
ms.openlocfilehash: 030640ba8907ae52c198ac96ad2c243b533d8c53
ms.sourcegitcommit: cd83f2bc0e52e13071ad306e07e4c255fc65cb03
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/22/2020
ms.locfileid: "4412111"
---
# <a name="connect-an-experiment-and-edit-variations"></a><span data-ttu-id="721ed-103">Kokeen yhdistäminen ja variaatioiden muokkaaminen</span><span class="sxs-lookup"><span data-stu-id="721ed-103">Connect an experiment and edit variations</span></span>

<span data-ttu-id="721ed-104">Tässä ohjeaiheessa käsitellään kokeen yhdistämistä Commercessa ja muutosten tekemistä variaatioihin siten, että ne vastaavat hypoteesia.</span><span class="sxs-lookup"><span data-stu-id="721ed-104">This topic describes how to connect your experiment in Commerce and make changes to your variations so that they align with your hypothesis.</span></span> 

<span data-ttu-id="721ed-105">Seuraavassa kaaviossa on kaikki vaiheet, jotka sisältyvät kokeen määrittämiseen ja suorittamiseen sähköisessä kaupankäyntisivustossa Dynamics 365 Commercessa.</span><span class="sxs-lookup"><span data-stu-id="721ed-105">The following diagram shows all of the steps involved in setting up and running an experiment on an e-Commerce website in Dynamics 365 Commerce.</span></span> <span data-ttu-id="721ed-106">Muut vaiheet käsitellään erillisissä ohjeaiheissa.</span><span class="sxs-lookup"><span data-stu-id="721ed-106">Additional steps are covered in separate topics.</span></span>

<span data-ttu-id="721ed-107">[ ![Kokeilun käyttäjän siirtymä – yhdistäminen ja muokkaaminen](./media/experimentation_connect_edit.svg) ](./media/experimentation_connect_edit.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="721ed-107">[ ![Experimentation user journey - Connect & Edit](./media/experimentation_connect_edit.svg) ](./media/experimentation_connect_edit.svg#lightbox)</span></span>

<span data-ttu-id="721ed-108">Sen jälkeen kun [koe on määritetty](experimentation-setup.md) kolmannen osapuolen palvelussa, koe yhdistetään Dynamics 365 Commercessa, jossa muokataan kokeen variaatioita.</span><span class="sxs-lookup"><span data-stu-id="721ed-108">After you've [set up your experiment](experimentation-setup.md) in a third-party service, you'll connect the experiment in Dynamics 365 Commerce and edit the experiment variations.</span></span>

## <a name="planning-considerations"></a><span data-ttu-id="721ed-109">Suunnittelussa huomioon otettavaa</span><span class="sxs-lookup"><span data-stu-id="721ed-109">Planning considerations</span></span>

<span data-ttu-id="721ed-110">Ennen kuin koe yhdistetään Commercessa, sinun tehtävä päätöksiä, jotka vaikuttavat Commercen tapaan hallita sisältöä.</span><span class="sxs-lookup"><span data-stu-id="721ed-110">Before you connect your experiment in Commerce, you'll need to make some decisions that impact the way Commerce manages your content.</span></span>

### <a name="determine-the-scope-of-your-experiment"></a><span data-ttu-id="721ed-111">Kokeen laajuuden määrittäminen</span><span class="sxs-lookup"><span data-stu-id="721ed-111">Determine the scope of your experiment</span></span>
<span data-ttu-id="721ed-112">Koetta yhdistettäessä sinua pyydetään määrittämään kokeen laajuus.</span><span class="sxs-lookup"><span data-stu-id="721ed-112">When you connect an experiment, you are prompted to define the scope of the experiment.</span></span> <span data-ttu-id="721ed-113">Kokeen laajuudeksi määritetään **osittainen** tai **kokonaan**.</span><span class="sxs-lookup"><span data-stu-id="721ed-113">Experiments are defined as **partial** scope or **entire** scope.</span></span>
- <span data-ttu-id="721ed-114">Valitse **osittainen**, jos haluat suorittaa kokeen tietyssä sivun osassa.</span><span class="sxs-lookup"><span data-stu-id="721ed-114">Choose **partial** if you want to conduct an experiment on a specific portion of a page.</span></span> <span data-ttu-id="721ed-115">Jos valitset tämän vaihtoehdon, sinun on määritettävä, mikä moduuleista sisältyy kokeeseen.</span><span class="sxs-lookup"><span data-stu-id="721ed-115">If you select this option, you must identify which modules are included in the experiment.</span></span> <span data-ttu-id="721ed-116">Oletussivun osiin tai osiin, jotka eivät liity kokeen, tehdyt muutokset synkronoidaan automaattisesti variaatioiden välillä.</span><span class="sxs-lookup"><span data-stu-id="721ed-116">Changes that are made to parts of the default page or fragment that aren't related to the experiment are automatically synchronized across variations.</span></span>
- <span data-ttu-id="721ed-117">Valitse **kokonaan**, jos haluat suorittaa kokeen koko sivulla tai osassa.</span><span class="sxs-lookup"><span data-stu-id="721ed-117">Choose **entire** if you want to conduct an experiment on an entire page or fragment.</span></span> <span data-ttu-id="721ed-118">Oletussivusta tai osasta luodaan erilliset kopiot.</span><span class="sxs-lookup"><span data-stu-id="721ed-118">Separate copies of the default page or fragment are created.</span></span> <span data-ttu-id="721ed-119">Kokeeseen sisältyviä moduuleja ei tarvitse valita, sillä koko muokkausalaa voidaan muuttaa.</span><span class="sxs-lookup"><span data-stu-id="721ed-119">You won't have to select which modules are included in the experiment because the whole editing surface is available to change.</span></span> <span data-ttu-id="721ed-120">Voit tarpeen mukaan lisätä, poistaa tai järjestää moduuleja uudelleen.</span><span class="sxs-lookup"><span data-stu-id="721ed-120">You can add, delete, or re-order modules as needed.</span></span> <span data-ttu-id="721ed-121">Jos muutokset kuitenkin tehdään oletussivulle tai osalle, johon koe on liitetty, kyseiset muutokset on synkronoitava manuaalisesti eri variaatioihin.</span><span class="sxs-lookup"><span data-stu-id="721ed-121">However, if any changes are made to the default page or fragment that the experiment is associated with, those changes have to be manually synchronized across all variations.</span></span>

<!-- not to editors, we're adding an image here to illustrate the difference. it will help.) -->

> [!NOTE]
> <span data-ttu-id="721ed-122">Jos liität kokeen asettelua käyttävään sivuun, kokeen mahdollinen laajuus on **kokonaan**.</span><span class="sxs-lookup"><span data-stu-id="721ed-122">If you associate your experiment with a page that uses a layout, you can only scope the experiment as **entire**.</span></span>

### <a name="decide-if-you-want-to-schedule-when-your-experiment-is-published"></a><span data-ttu-id="721ed-123">Kokeen julkaisun mahdollisesta aikatauluttamisesta päättäminen</span><span class="sxs-lookup"><span data-stu-id="721ed-123">Decide if you want to schedule when your experiment is published</span></span>
<span data-ttu-id="721ed-124">Jos haluat aikatauluttaa kokeen julkaisun live-sivustoon, varmista, että kokeeseen liitettävä sisältö on saatavana julkaisuryhmässä *ennen* kokeen yhdistämistä.</span><span class="sxs-lookup"><span data-stu-id="721ed-124">If you want to schedule when your experiment is published to your live site, make sure the content you want to associate with the experiment is available in a publish group *before* you connect the experiment.</span></span> 

<span data-ttu-id="721ed-125">Lisätietoja julkaisuryhmistä on kohdassa [Julkaisuryhmien kanssa työskenteleminen](publish-groups.md).</span><span class="sxs-lookup"><span data-stu-id="721ed-125">For more information about publish groups, refer to [Work with publish groups](publish-groups.md).</span></span>


## <a name="connect-your-experiment"></a><span data-ttu-id="721ed-126">Kokeen yhdistäminen</span><span class="sxs-lookup"><span data-stu-id="721ed-126">Connect your experiment</span></span>
<span data-ttu-id="721ed-127">Yhdistä koe käynnistämällä ohjattu **Yhdistä koe** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="721ed-127">To connect your experiment, you'll launch the **Connect experiment** wizard.</span></span> <span data-ttu-id="721ed-128">Ohjattu toiminto opastaa kokeen yhdistämisvaiheissa.</span><span class="sxs-lookup"><span data-stu-id="721ed-128">The wizard walks you through the steps required to connect your experiment.</span></span> <span data-ttu-id="721ed-129">Kun ohjattu toiminto on suoritettu, koe on yhdistetty sekä variaatiot luotu ja valmiita muokattaviksi.</span><span class="sxs-lookup"><span data-stu-id="721ed-129">When you complete the wizard, your experiment is connected and variations are created and ready to be edited.</span></span>

<span data-ttu-id="721ed-130">Kokeen yhdistäminen Commercen sivustonmuodostimeen aloitetaan seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="721ed-130">To get started connecting your experiment in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="721ed-131">Käynnistä ohjattu **Yhdistä koe** -toiminto valitsemalla vasemmassa siirtymisruudussa **Kokeet** ja valitsemalla sitten **Yhdistä**.</span><span class="sxs-lookup"><span data-stu-id="721ed-131">To launch the **Connect experiment** wizard, select **Experiments** in the left navigation pane, and then select **Connect**.</span></span> <span data-ttu-id="721ed-132">Vaihtoehtoisesti voit käyttää ohjattua toimintoa sivu- tai osaeditorista muokkaamalla sitä tai valitsemalla komentopalkissa **Yhdistä koe**.</span><span class="sxs-lookup"><span data-stu-id="721ed-132">Alternatively, you can access the wizard from a page or fragment editor by editing it and selecting **Connect experiment** on the command bar.</span></span>

    > [!NOTE]
    > <span data-ttu-id="721ed-133">Sivu voidaan yhdistää kerrallaan vain yhteen kokeeseen.</span><span class="sxs-lookup"><span data-stu-id="721ed-133">A page can only be connected to one experiment at a time.</span></span> <span data-ttu-id="721ed-134">Voit yhdistää sivun toiseen kokeeseen poistamalla ensin kokeen sivulta, johon se on nyt yhdistetty.</span><span class="sxs-lookup"><span data-stu-id="721ed-134">To connect a page to a different experiment, first delete the experiment that the page is currently connected to.</span></span>

1. <span data-ttu-id="721ed-135">Valitse sivu tai osa, jossa haluat suorittaa kokeilun.</span><span class="sxs-lookup"><span data-stu-id="721ed-135">Choose the page or fragment you want to run your experiment on.</span></span>
1. <span data-ttu-id="721ed-136">Määritä kokeilun laajuudeksi **osittainen** tai **kokonaan** sen mukaan, mitä valittiin edellä olevassa kohdassa [Kokeen laajuuden määrittäminen](#determine-the-scope-of-your-experiment).</span><span class="sxs-lookup"><span data-stu-id="721ed-136">Set the experimentation scope to **partial** or **entire**, based on the choice you made in the [Determine the scope of your experiment](#determine-the-scope-of-your-experiment) section above.</span></span>
    > [!NOTE]
    > <span data-ttu-id="721ed-137">**Koe sivuilla tai osissa** -ominaisuusmerkintä on oltava käytössä jos haluat tehdä kokeen koko sivulla tai koko osassa.</span><span class="sxs-lookup"><span data-stu-id="721ed-137">The **Experiment on pages or fragments** feature flag must be enabled if you want to experiment on a full page or fragment.</span></span> <span data-ttu-id="721ed-138">Lisätietoja on kohdassa [Kokeilu Dynamics 365 Commercessa](experimentation-overview.md).</span><span class="sxs-lookup"><span data-stu-id="721ed-138">Refer to the [Experimentation in Dynamics 365 Commerce](experimentation-overview.md) topic for more information.</span></span>
    
1. <span data-ttu-id="721ed-139">Valitse ohjatun toiminnon viimeisessä vaiheessa **Luo variaatiot ja lopeta ohjattu toiminto**.</span><span class="sxs-lookup"><span data-stu-id="721ed-139">In the final step of the wizard, select **Generate variations and exit wizard**.</span></span> <span data-ttu-id="721ed-140">Variaatiot luodaan kokeelle.</span><span class="sxs-lookup"><span data-stu-id="721ed-140">Variations are created for the experiment.</span></span> 

## <a name="edit-your-variations"></a><span data-ttu-id="721ed-141">Variaatioiden muokkaaminen</span><span class="sxs-lookup"><span data-stu-id="721ed-141">Edit your variations</span></span>
<span data-ttu-id="721ed-142">Variaatiot luodaan, kun lopetat ohjatun toiminnon.</span><span class="sxs-lookup"><span data-stu-id="721ed-142">When you exit the wizard, variations are created for you.</span></span> 

<span data-ttu-id="721ed-143">Seuraavaksi muokataan variaatiot vastaamaan valintoja, jotka on vahvistettava kokeen hypoteesi.</span><span class="sxs-lookup"><span data-stu-id="721ed-143">Next, you'll edit the variations so they reflect the choices that you need to verify in the experiment hypothesis.</span></span> <span data-ttu-id="721ed-144">Valitse jokin seuraavista menetelmistä, joka vastaa edellä käsitellyssä kohdassa [Kokeen laajuuden määrittäminen](#determine-the-scope-of-your-experiment) kokeeseen valittua laajuutta.</span><span class="sxs-lookup"><span data-stu-id="721ed-144">Choose one of following procedures that corresponds to the scope you chose for your experiment in the [Determine the scope of your experiment](#determine-the-scope-of-your-experiment) section above.</span></span>

### <a name="edit-variations-for-experiments-with-partial-scope"></a><span data-ttu-id="721ed-145">Osittaisen laajuuden kokeiden variaatioiden muokkaaminen</span><span class="sxs-lookup"><span data-stu-id="721ed-145">Edit variations for experiments with partial scope</span></span>
<span data-ttu-id="721ed-146">Toimi seuraavasti, jos määritit kokeen laajuudeksi **osittainen** ohjatussa **Yhdistä koe** -toiminnossa.</span><span class="sxs-lookup"><span data-stu-id="721ed-146">Follow these steps if you defined the scope of your experiment as **partial** in the **Connect experiment** wizard.</span></span>

1. <span data-ttu-id="721ed-147">Muokkaa editorinäkymässä komentopalkin alapuolella olevan variaatioiden avattavan valikon avulla kutakin variaatiota alkuperäisen hypoteesin perusteella.</span><span class="sxs-lookup"><span data-stu-id="721ed-147">In editor view, use the variations drop-down menu below the command bar to edit each variation based on your original hypothesis.</span></span> <span data-ttu-id="721ed-148">Yhtä variaatioista kannattaa ehkä olla muuttamatta, jolloin se toimii vertailu- tai perusvariaationa.</span><span class="sxs-lookup"><span data-stu-id="721ed-148">You may also want to establish a control or base variation by leaving one of the variations unchanged.</span></span>
1. <span data-ttu-id="721ed-149">Valitse moduuli, jossa koe tehdään, valitsemalla kolme pistettä (....). Valitse lopuksi **Lisää kokeeseen**.</span><span class="sxs-lookup"><span data-stu-id="721ed-149">Select the module to be experimented on, select the ellipsis (...), and then select **Add to experiment**.</span></span>

### <a name="edit-variations-for-experiments-with-entire-scope"></a><span data-ttu-id="721ed-150">Koko laajuuden kokeiden variaatioiden muokkaaminen</span><span class="sxs-lookup"><span data-stu-id="721ed-150">Edit variations for experiments with entire scope</span></span>
<span data-ttu-id="721ed-151">Jos kokeen laajuudeksi määritettiin **kokonaan** ohjatussa **Yhdistä koe** -toiminnossa, editorinäkymän komentopalkin alapuolella olevan variaatioiden avattavan valikon avulla voi muokata kutakin variaatiota alkuperäisen hypoteesin perusteella.</span><span class="sxs-lookup"><span data-stu-id="721ed-151">If you defined the scope of your experiment as **entire** in the **Connect experiment** wizard, while in editor view, use the variations drop-down menu below the command bar to edit each variation based on your original hypothesis.</span></span> 

> [!NOTE]
> <span data-ttu-id="721ed-152">Kummassakin tapauksessa yksi variaatioista kannattaa ehkä jättää muuttamatta, jolloin se toimii vertailu- tai perusvariaationa.</span><span class="sxs-lookup"><span data-stu-id="721ed-152">In either case, you may also want to establish a control or base variation by leaving one of the variations unchanged.</span></span>

## <a name="previous-step"></a><span data-ttu-id="721ed-153">Edellinen vaihe</span><span class="sxs-lookup"><span data-stu-id="721ed-153">Previous step</span></span>
[<span data-ttu-id="721ed-154">Kokeen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="721ed-154">Set up an experiment</span></span>](experimentation-setup.md) 


## <a name="next-step"></a><span data-ttu-id="721ed-155">Seuraava vaihe</span><span class="sxs-lookup"><span data-stu-id="721ed-155">Next step</span></span>
[<span data-ttu-id="721ed-156">Kokeen esikatseleminen ja julkaiseminen</span><span class="sxs-lookup"><span data-stu-id="721ed-156">Preview and publish an experiment</span></span>](experimentation-preview-publish.md)
