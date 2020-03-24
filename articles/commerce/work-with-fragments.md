---
title: Katkelmien käyttäminen
description: Tässä ohjeaiheessa kuvataan, miksi, milloin ja miten osia käytetään Microsoft Dynamics 365 Commerce -sovelluksessa.
author: v-chgri
manager: annbe
ms.date: 01/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: retail
ms.author: phinneyridge
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: f29046ded47ed9c49a2cc841aa7c1f6492b49aec
ms.sourcegitcommit: 1d5a4f70a931e78b06811add97c1962e8d93689b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/13/2020
ms.locfileid: "3124356"
---
# <a name="work-with-fragments"></a><span data-ttu-id="00f24-103">Katkelmien käyttäminen</span><span class="sxs-lookup"><span data-stu-id="00f24-103">Work with fragments</span></span> 


[!include [banner](includes/banner.md)]

<span data-ttu-id="00f24-104">Tässä ohjeaiheessa kuvataan, miksi, milloin ja miten osia käytetään Microsoft Dynamics 365 Commerce -sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="00f24-104">This topic describes why, when, and how to use fragments in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="00f24-105">Yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="00f24-105">Overview</span></span>

<span data-ttu-id="00f24-106">Osat mahdollistavat koko sivustossa uudelleenkäytettävien moduulin määritysten keskitetyn muokkauskokemuksen.</span><span class="sxs-lookup"><span data-stu-id="00f24-106">Fragments allow for a centralized authoring experience for module configurations that must be reused throughout your site.</span></span> <span data-ttu-id="00f24-107">Esimerkiksi ylä- ja alatunnisteet sekä ilmoituspalkit määritetään usein osiksi, koska ne jaetaan useille sivuille.</span><span class="sxs-lookup"><span data-stu-id="00f24-107">For example, headers, footers, and banners are often configured as fragments, because they are shared across many pages.</span></span> <span data-ttu-id="00f24-108">Voit ajatella osia pienoisverkkosivuina, jotka voidaan lisätä sivuston muihin sivuihin.</span><span class="sxs-lookup"><span data-stu-id="00f24-108">You can think of fragments as miniature webpages that can be inserted into other pages on your site.</span></span> <span data-ttu-id="00f24-109">Osilla on oma elinkaarensa.</span><span class="sxs-lookup"><span data-stu-id="00f24-109">Fragments have their own lifecycle.</span></span> <span data-ttu-id="00f24-110">Toisin sanoen ne luodaan, päivitetään, niihin viitataan ja ne poistetaan yksittäisinä entiteetteinä muokkaustyökaluissa.</span><span class="sxs-lookup"><span data-stu-id="00f24-110">In other words, they are created, referenced, updated, and deleted as independent entities in the authoring tools.</span></span>

<span data-ttu-id="00f24-111">Kun osat on määritetty, niitä voidaan käyttää aina, kun moduuleja voi käyttää sivuston rakenteessa.</span><span class="sxs-lookup"><span data-stu-id="00f24-111">After fragments are configured, they can be used wherever modules can be used in your site structure.</span></span> <span data-ttu-id="00f24-112">Osiin voi viitata sivuilla, asetteluissa, malleissa ja muissa osissa.</span><span class="sxs-lookup"><span data-stu-id="00f24-112">Fragments can be referenced on pages, in layouts, in templates, and in other fragments.</span></span>

> [!NOTE]
> <span data-ttu-id="00f24-113">Osat voivat olla sisäkkäisiä jopa seitsemän tason syvyyteen muissa osissa.</span><span class="sxs-lookup"><span data-stu-id="00f24-113">Fragments can be nested up to seven levels deep inside other fragments.</span></span>

<span data-ttu-id="00f24-114">Jos haluat edistää esimerkiksi kausiluonteista tapahtumaa useilla sivuston sivuilla, voit käyttää osia.</span><span class="sxs-lookup"><span data-stu-id="00f24-114">For example, if you want to promote a seasonal event cross many pages on our site, you can use a fragment.</span></span> <span data-ttu-id="00f24-115">Uuden osan luontiprosessin ensimmäinen vaihe on valita sen moduulin tyyppi, jolla haluat aloittaa.</span><span class="sxs-lookup"><span data-stu-id="00f24-115">The first step in the process of creating a new fragment is to select the type of module that you want to start from.</span></span> <span data-ttu-id="00f24-116">Tässä esimerkissä voit muodostaa osan hero-moduulista.</span><span class="sxs-lookup"><span data-stu-id="00f24-116">For this example, you can build the fragment from a hero module.</span></span>

> [!NOTE]
> <span data-ttu-id="00f24-117">Osia voi muodostaa mistä tahansa moduulityypistä.</span><span class="sxs-lookup"><span data-stu-id="00f24-117">Fragments can be built from any module type.</span></span>

<span data-ttu-id="00f24-118">Tämän jälkeen voit määrittää hero-osaan määritetyn kampanjasisällön.</span><span class="sxs-lookup"><span data-stu-id="00f24-118">You can then configure the hero fragment with your specific promotional content.</span></span> <span data-ttu-id="00f24-119">Voit myös lokalisoida sen tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="00f24-119">You can also localize it as you require.</span></span> <span data-ttu-id="00f24-120">Uutta erillistä hero-osaa voi tämän jälkeen kuluttaa esimääritettynä moduulina koko sivustossa.</span><span class="sxs-lookup"><span data-stu-id="00f24-120">The new stand-alone hero fragment can then be consumed as a preconfigured module throughout your site.</span></span> <span data-ttu-id="00f24-121">Voit helposti lisätä sen malleihin, tiettyihin sivuihin tai muihin osiin, joissa voi olla hero-moduuleita.</span><span class="sxs-lookup"><span data-stu-id="00f24-121">You can easily add it to templates, to specific pages, or to other fragments that can contain hero modules.</span></span>

<span data-ttu-id="00f24-122">Kaikki paikat, joihin osa lisätään, ovat viittauksia luotuun, keskitettyyn hero-osaan.</span><span class="sxs-lookup"><span data-stu-id="00f24-122">All the places where the fragment is added are references to the central hero fragment that you created.</span></span> <span data-ttu-id="00f24-123">Jos julkaiset osan muutokset, ne vaikuttavat heti kaikissa sivuston paikoissa, joissa osaan viitataan.</span><span class="sxs-lookup"><span data-stu-id="00f24-123">If you publish changes to the fragment, those changes are immediately reflected in all the places where the fragment is referenced across the site.</span></span> <span data-ttu-id="00f24-124">Tämän vuoksi osat ovat tehokas tapa käyttää uudelleen moduulin määrityksiä sivustossa ja hallita niitä keskitetysti.</span><span class="sxs-lookup"><span data-stu-id="00f24-124">Therefore, fragments provide a powerful and efficient way to reuse and centrally manage module configurations on a site.</span></span> <span data-ttu-id="00f24-125">Tämä tehostettu käyttö ketteröittää toimintoja ja auttaa vähentämään sivuston hallintaan liittyviä kustannuksia.</span><span class="sxs-lookup"><span data-stu-id="00f24-125">By effectively using them, you can significantly increase agility and help reduce the cost that is associated with managing site content.</span></span>

<span data-ttu-id="00f24-126">Seuraavassa kuvassa näkyy, kuinka osia voi käyttää jaettujen moduulin määritysten keskitetyssä muokkauksessa sähköisen kaupankäynnin sivustossa.</span><span class="sxs-lookup"><span data-stu-id="00f24-126">The following illustration shows how fragments can be used to centralize authoring of shared module configurations across an e-Commerce site.</span></span>

![Kuvassa näkyy, kuinka osia voi käyttää jaettujen moduulin määritysten keskitetyssä muokkauksessa sähköisen kaupankäynnin sivustossa](./media/fragment-figure1.png)

## <a name="create-a-fragment"></a><span data-ttu-id="00f24-128">Osan luominen</span><span class="sxs-lookup"><span data-stu-id="00f24-128">Create a fragment</span></span>

<span data-ttu-id="00f24-129">Voit luoda uuden osan tai tallentaa olemassa olevan osan määrityksen osana.</span><span class="sxs-lookup"><span data-stu-id="00f24-129">You can either create a new fragment or save an existing module configuration as a fragment.</span></span>

### <a name="save-an-existing-module-configuration-as-a-fragment"></a><span data-ttu-id="00f24-130">Aiemmin luodun moduulin määrityksen tallentaminen osana</span><span class="sxs-lookup"><span data-stu-id="00f24-130">Save an existing module configuration as a fragment</span></span>

<span data-ttu-id="00f24-131">Voit muuntaa aiemmin määritetyn moduulin uudelleenkäytettäväksi osaksi seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="00f24-131">To convert a previously configured module to a reusable fragment, follow these steps.</span></span>

1. <span data-ttu-id="00f24-132">Avaa sivu tai malli, joka sisältää osaksi muunnettavan moduulin.</span><span class="sxs-lookup"><span data-stu-id="00f24-132">Open a page or template that contains the module that you want to convert to a fragment.</span></span>
1. <span data-ttu-id="00f24-133">Valitse vasemmalla olevasta jäsennysruudusta painike, jossa on kolme pistettä (**...**) moduulin nimen vieressä.</span><span class="sxs-lookup"><span data-stu-id="00f24-133">In the outline pane on the left, select the ellipsis button (**...**) next to the name of the module.</span></span> 
1. <span data-ttu-id="00f24-134">Valitse **Jaa fragmenttina**.</span><span class="sxs-lookup"><span data-stu-id="00f24-134">Select **Share as Fragment**.</span></span> 
1. <span data-ttu-id="00f24-135">Näyttöön tulee valintaikkuna.</span><span class="sxs-lookup"><span data-stu-id="00f24-135">A dialog box appears.</span></span> <span data-ttu-id="00f24-136">Anna osan nimi ja metatiedot.</span><span class="sxs-lookup"><span data-stu-id="00f24-136">Enter a name and metadata for the fragment.</span></span>
1. <span data-ttu-id="00f24-137">Valitse **OK**, jos haluat tallentaa moduulin määrityksen osana, joka voidaan lisätä muille sivuille.</span><span class="sxs-lookup"><span data-stu-id="00f24-137">Select **OK** to save the module configuration as a fragment that can be added to other pages.</span></span>

<span data-ttu-id="00f24-138">Seuraavassa kuvassa näkyy, miten moduulin konfiguraatio tallennetaan fragmenttina.</span><span class="sxs-lookup"><span data-stu-id="00f24-138">The following image shows how to save a module configuration as a fragment.</span></span>

![Näyttökaappaus moduulin kokoonpanon tallentamisesta fragmenttina](./media/save-as-fragment.png)

### <a name="create-a-new-fragment"></a><span data-ttu-id="00f24-140">Uuden osan luominen</span><span class="sxs-lookup"><span data-stu-id="00f24-140">Create a new fragment</span></span>

<span data-ttu-id="00f24-141">Voit luoda uuden osan seuraavien vaiheiden avulla.</span><span class="sxs-lookup"><span data-stu-id="00f24-141">To create a new fragment, follow these steps.</span></span>

1. <span data-ttu-id="00f24-142">Valitse vasemmanpuoleisessa siirtymisruudussa **Osat**.</span><span class="sxs-lookup"><span data-stu-id="00f24-142">In the navigation pane on the left, select **Fragments**.</span></span>
1. <span data-ttu-id="00f24-143">Valitse **Uuden sivun osa**.</span><span class="sxs-lookup"><span data-stu-id="00f24-143">Select **New Page Fragment**.</span></span> <span data-ttu-id="00f24-144">Näyttöön tulee valintaikkuna, jossa näkyvät kaikki käytettävissä olevat moduulityypit.</span><span class="sxs-lookup"><span data-stu-id="00f24-144">A dialog box appears that shows all the available module types.</span></span> <span data-ttu-id="00f24-145">Osat voi luoda mistä tahansa moduulityypistä, kuten aiemmin jo mainittiin.</span><span class="sxs-lookup"><span data-stu-id="00f24-145">As was mentioned earlier, fragments can be created from any module type.</span></span>
1. <span data-ttu-id="00f24-146">Valitse fragmentin moduulityyppi.</span><span class="sxs-lookup"><span data-stu-id="00f24-146">Select a module type for your fragment.</span></span>

<span data-ttu-id="00f24-147">Seuraavassa kuvassa näkyy, mistä uusi katkelma luodaan.</span><span class="sxs-lookup"><span data-stu-id="00f24-147">The following image shows where to create a new fragment.</span></span>

![Näyttökaappaus, jossa tulee luoda uusi fragmentti](./media/fragment-nav-menu.png)

> [!TIP]
> <span data-ttu-id="00f24-149">Kun valitset yleisen säilömoduulin tyypin, osan päivittäminen ja määrittäminen sujuu joustavasti myöhemmin.</span><span class="sxs-lookup"><span data-stu-id="00f24-149">By selecting a generic container module type, you get the most flexibility when you need to update and configure your fragment later.</span></span>

## <a name="add-remove-or-edit-fragments-on-a-page"></a><span data-ttu-id="00f24-150">Osien lisääminen sivulle tai niiden poistaminen tai muokkaaminen</span><span class="sxs-lookup"><span data-stu-id="00f24-150">Add, remove, or edit fragments on a page</span></span>

<span data-ttu-id="00f24-151">Seuraavissa ohjeissa kuvataan, miten osia lisätään, poistetaan ja muokataan.</span><span class="sxs-lookup"><span data-stu-id="00f24-151">The following procedures describe how to add, remove, and edit fragments.</span></span>

### <a name="add-a-fragment"></a><span data-ttu-id="00f24-152">Osan lisääminen</span><span class="sxs-lookup"><span data-stu-id="00f24-152">Add a fragment</span></span>

<span data-ttu-id="00f24-153">Voit lisätä osan sivulle seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="00f24-153">To add a fragment to a page, follow these steps.</span></span>

1. <span data-ttu-id="00f24-154">Valitse vasemmalla olevasta jäsennysruudusta säilö tai paikka, johon alimoduulit voidaan lisätä.</span><span class="sxs-lookup"><span data-stu-id="00f24-154">In the outline pane on the left, select a container or slot that child modules can be added to.</span></span>
1. <span data-ttu-id="00f24-155">Valitse säilön tai paikan vieressä oleva kolmen pisteen painike ja valitse sitten **Lisää osa**.</span><span class="sxs-lookup"><span data-stu-id="00f24-155">Select the ellipsis button next to the name of the container or slot, and then select **Add Fragment**.</span></span> <span data-ttu-id="00f24-156">Näyttöön tulee valintaikkuna.</span><span class="sxs-lookup"><span data-stu-id="00f24-156">A dialog box appears.</span></span>

    ![Näyttökaappaus siitä, miten olemassa oleva fragmentti lisätään paikkaan tai säilöön](./media/add-fragment.png)
 
    > [!NOTE]
    > <span data-ttu-id="00f24-158">Jos säilö tai paikka ei tue uusia alimoduuleja, **Lisää osa** -vaihtoehto ei ole käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="00f24-158">If the container or slot doesn't support new child modules, the **Add Fragment** option is unavailable.</span></span>
    
1. <span data-ttu-id="00f24-159">Hae valintaikkunassa lisättävä osa ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="00f24-159">In the dialog box, search for and select a fragment to add.</span></span> <span data-ttu-id="00f24-160">Jos käytettävissä olevia osia ei ole näkyvissä, sinun on ehkä ensin luotava osa moduulityypistä, jota valittu säilö tai paikka tukee.</span><span class="sxs-lookup"><span data-stu-id="00f24-160">If no available fragments are listed, you might first have to create a fragment from a module type that the selected container or slot supports.</span></span>
1. <span data-ttu-id="00f24-161">Valitse haluamasi fragmentti lisätäksesi sen sivullasi olevaan säilöön tai paikkaan.</span><span class="sxs-lookup"><span data-stu-id="00f24-161">Select your desired fragment to add it to the container or slot on your page.</span></span>

    ![Näyttökaappaus fragmenttivalitsimen modaalisesta ikkunasta](./media/fragment-picker.png)

> [!NOTE]
> <span data-ttu-id="00f24-163">Moduulit, jotka sallitaan säilössä tai paikassa, määräytyvät sivun mallin tai moduulien omien määritysten mukaan.</span><span class="sxs-lookup"><span data-stu-id="00f24-163">The modules that are allowed in a container or slot are defined by the page's template or the modules' own definitions.</span></span>

### <a name="remove-a-fragment"></a><span data-ttu-id="00f24-164">Osan poistaminen</span><span class="sxs-lookup"><span data-stu-id="00f24-164">Remove a fragment</span></span>

<span data-ttu-id="00f24-165">Voit poistaa sivun osan paikasta tai säilöstä seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="00f24-165">To remove a fragment from a slot or container on a page, follow these steps.</span></span>

1. <span data-ttu-id="00f24-166">Valitse vasemmanpuoleisessa jäsennysruudussa poistettavan osan nimen vieressä oleva kolmen pisteen painike ja valitse sitten roskakoripainike.</span><span class="sxs-lookup"><span data-stu-id="00f24-166">In the outline pane on the left, select the ellipsis button next to the name of the fragment to remove, and then select the trash can button.</span></span>
1. <span data-ttu-id="00f24-167">Kun sinua pyydetään vahvistamaan osan poistaminen, valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="00f24-167">When you're prompted to confirm that you want to remove the fragment, select **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="00f24-168">Kun poistat osan sivulta, poistat vain viittauksen kyseiseltä sivulta.</span><span class="sxs-lookup"><span data-stu-id="00f24-168">When you remove a fragment from a page, you just remove the reference to it from that page.</span></span> <span data-ttu-id="00f24-169">**Et** poista osaa sivustosta.</span><span class="sxs-lookup"><span data-stu-id="00f24-169">You do **not** delete the fragment from your site.</span></span> <span data-ttu-id="00f24-170">Jos haluat poistaa osia sivustosta, käytä osan tarkistusohjelman käyttöliittymää.</span><span class="sxs-lookup"><span data-stu-id="00f24-170">To delete fragments from your site, you must use the fragment inspector user interface (UI).</span></span> <span data-ttu-id="00f24-171">Voit poistaa osia sivustosta vain, jos niihin ei tällä hetkellä viitata sivuissa, malleissa tai muissa osissa.</span><span class="sxs-lookup"><span data-stu-id="00f24-171">You can delete fragments from a site only if they aren't currently referenced by any pages, templates, or other fragments.</span></span>

### <a name="edit-a-fragment"></a><span data-ttu-id="00f24-172">Osan muokkaaminen</span><span class="sxs-lookup"><span data-stu-id="00f24-172">Edit a fragment</span></span>

<span data-ttu-id="00f24-173">Jos haluat muokata osia, sinun on käytettävä osan muokkausohjelman käyttöliittymää.</span><span class="sxs-lookup"><span data-stu-id="00f24-173">To edit fragments, you must use the fragment editor UI.</span></span> <span data-ttu-id="00f24-174">Tämä on suunniteltu rajoitus.</span><span class="sxs-lookup"><span data-stu-id="00f24-174">This restriction is by design.</span></span> <span data-ttu-id="00f24-175">Sen avulla voidaan varmistaa, että tekijät eivät sekoita tietyn sivun moduulien muokkausprosessia sellaisten osien muokkausprosessiin, joita voidaan jakaa useille sivuille.</span><span class="sxs-lookup"><span data-stu-id="00f24-175">It helps guarantee that authors don't confuse the process of editing the modules for a specific page with the process of editing fragments that might be shared across many pages.</span></span>

<span data-ttu-id="00f24-176">Voit muokata osaa seuraavien vaiheiden avulla.</span><span class="sxs-lookup"><span data-stu-id="00f24-176">To edit a fragment, follow these steps.</span></span>

1. <span data-ttu-id="00f24-177">Valitse vasemmanpuoleisessa siirtymisruudussa **Osat**.</span><span class="sxs-lookup"><span data-stu-id="00f24-177">In the navigation pane on the left, select **Fragments**.</span></span>
1. <span data-ttu-id="00f24-178">Valitse **Osat**-kohdassa muokattava osa.</span><span class="sxs-lookup"><span data-stu-id="00f24-178">Under **Fragments**, select the fragment to edit.</span></span>
1. <span data-ttu-id="00f24-179">Muokkaa osan moduulin ominaisuuksia ja rakennetta tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="00f24-179">Edit the fragment's module properties and structure as you require.</span></span> <span data-ttu-id="00f24-180">Prosessi muistuttaa moduulien muokkausprosessia, jossa moduuleja muokataan sivueditorinäkymässä.</span><span class="sxs-lookup"><span data-stu-id="00f24-180">The process resembles the process for editing modules are edited in the page editor view.</span></span>

<span data-ttu-id="00f24-181">Voit muokata osaa myös valitsemalla sen sivulla, mallissa tai pääosassa ja valitsemalla sitten **Muokkaa osaa** -kohdan oikeanpuoleisessa ominaisuusruudussa.</span><span class="sxs-lookup"><span data-stu-id="00f24-181">You can also edit a fragment by selecting it on a page, in a template, or in a parent fragment, and then selecting **Edit Fragment** in the properties pane on the right.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="00f24-182">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="00f24-182">Additional resources</span></span>

[<span data-ttu-id="00f24-183">Mallit ja asettelut – yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="00f24-183">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="00f24-184">Mallien käyttö</span><span class="sxs-lookup"><span data-stu-id="00f24-184">Work with templates</span></span>](work-with-templates.md)

[<span data-ttu-id="00f24-185">Esimääritettyjen asettelujen käyttö</span><span class="sxs-lookup"><span data-stu-id="00f24-185">Work with preset layouts</span></span>](work-with-layouts.md)

[<span data-ttu-id="00f24-186">Julkaisuryhmien kanssa työskenteleminen</span><span class="sxs-lookup"><span data-stu-id="00f24-186">Work with publish groups</span></span>](publish-groups.md)
