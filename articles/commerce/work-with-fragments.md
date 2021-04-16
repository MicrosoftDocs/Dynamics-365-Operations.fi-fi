---
title: Katkelmien käyttäminen
description: Tässä ohjeaiheessa kuvataan, miksi, milloin ja miten osia käytetään Microsoft Dynamics 365 Commerce -sovelluksessa.
author: phinneyridge
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 1fa55ab83562983273768895db61032ec7199fa6
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5793942"
---
# <a name="work-with-fragments"></a><span data-ttu-id="e0abf-103">Katkelmien käyttäminen</span><span class="sxs-lookup"><span data-stu-id="e0abf-103">Work with fragments</span></span> 

[!include [banner](includes/banner.md)]

<span data-ttu-id="e0abf-104">Tässä ohjeaiheessa kuvataan, miksi, milloin ja miten osia käytetään Microsoft Dynamics 365 Commerce -sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="e0abf-104">This topic describes why, when, and how to use fragments in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="e0abf-105">Osat mahdollistavat koko sivustossa uudelleenkäytettävien moduulin määritysten keskitetyn muokkauskokemuksen.</span><span class="sxs-lookup"><span data-stu-id="e0abf-105">Fragments allow for a centralized authoring experience for module configurations that must be reused throughout your site.</span></span> <span data-ttu-id="e0abf-106">Esimerkiksi ylä- ja alatunnisteet sekä ilmoituspalkit määritetään usein osiksi, koska ne jaetaan useille sivuille.</span><span class="sxs-lookup"><span data-stu-id="e0abf-106">For example, headers, footers, and banners are often configured as fragments, because they are shared across many pages.</span></span> <span data-ttu-id="e0abf-107">Voit ajatella osia pienoisverkkosivuina, jotka voidaan lisätä sivuston muihin sivuihin.</span><span class="sxs-lookup"><span data-stu-id="e0abf-107">You can think of fragments as miniature webpages that can be inserted into other pages on your site.</span></span> <span data-ttu-id="e0abf-108">Osilla on oma elinkaarensa.</span><span class="sxs-lookup"><span data-stu-id="e0abf-108">Fragments have their own lifecycle.</span></span> <span data-ttu-id="e0abf-109">Toisin sanoen ne luodaan, päivitetään, niihin viitataan ja ne poistetaan yksittäisinä entiteetteinä muokkaustyökaluissa.</span><span class="sxs-lookup"><span data-stu-id="e0abf-109">In other words, they are created, referenced, updated, and deleted as independent entities in the authoring tools.</span></span>

<span data-ttu-id="e0abf-110">Kun osat on määritetty, niitä voidaan käyttää aina, kun moduuleja voi käyttää sivuston rakenteessa.</span><span class="sxs-lookup"><span data-stu-id="e0abf-110">After fragments are configured, they can be used wherever modules can be used in your site structure.</span></span> <span data-ttu-id="e0abf-111">Osiin voi viitata sivuilla, asetteluissa, malleissa ja muissa osissa.</span><span class="sxs-lookup"><span data-stu-id="e0abf-111">Fragments can be referenced on pages, in layouts, in templates, and in other fragments.</span></span>

> [!NOTE]
> <span data-ttu-id="e0abf-112">Osat voivat olla sisäkkäisiä jopa seitsemän tason syvyyteen muissa osissa.</span><span class="sxs-lookup"><span data-stu-id="e0abf-112">Fragments can be nested up to seven levels deep inside other fragments.</span></span>

<span data-ttu-id="e0abf-113">Jos haluat edistää esimerkiksi kausiluonteista tapahtumaa useilla sivuston sivuilla, voit käyttää osia.</span><span class="sxs-lookup"><span data-stu-id="e0abf-113">For example, if you want to promote a seasonal event cross many pages on our site, you can use a fragment.</span></span> <span data-ttu-id="e0abf-114">Uuden osan luontiprosessin ensimmäinen vaihe on valita sen moduulin tyyppi, jolla haluat aloittaa.</span><span class="sxs-lookup"><span data-stu-id="e0abf-114">The first step in the process of creating a new fragment is to select the type of module that you want to start from.</span></span> <span data-ttu-id="e0abf-115">Tässä esimerkissä voit muodostaa osan hero-moduulista.</span><span class="sxs-lookup"><span data-stu-id="e0abf-115">For this example, you can build the fragment from a hero module.</span></span>

> [!NOTE]
> <span data-ttu-id="e0abf-116">Osia voi muodostaa mistä tahansa moduulityypistä.</span><span class="sxs-lookup"><span data-stu-id="e0abf-116">Fragments can be built from any module type.</span></span>

<span data-ttu-id="e0abf-117">Tämän jälkeen voit määrittää hero-osaan määritetyn kampanjasisällön.</span><span class="sxs-lookup"><span data-stu-id="e0abf-117">You can then configure the hero fragment with your specific promotional content.</span></span> <span data-ttu-id="e0abf-118">Voit myös lokalisoida sen tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="e0abf-118">You can also localize it as you require.</span></span> <span data-ttu-id="e0abf-119">Uutta erillistä hero-osaa voi tämän jälkeen kuluttaa esimääritettynä moduulina koko sivustossa.</span><span class="sxs-lookup"><span data-stu-id="e0abf-119">The new stand-alone hero fragment can then be consumed as a preconfigured module throughout your site.</span></span> <span data-ttu-id="e0abf-120">Voit helposti lisätä sen malleihin, tiettyihin sivuihin tai muihin osiin, joissa voi olla hero-moduuleita.</span><span class="sxs-lookup"><span data-stu-id="e0abf-120">You can easily add it to templates, to specific pages, or to other fragments that can contain hero modules.</span></span>

<span data-ttu-id="e0abf-121">Kaikki paikat, joihin osa lisätään, ovat viittauksia luotuun, keskitettyyn hero-osaan.</span><span class="sxs-lookup"><span data-stu-id="e0abf-121">All the places where the fragment is added are references to the central hero fragment that you created.</span></span> <span data-ttu-id="e0abf-122">Jos julkaiset osan muutokset, ne vaikuttavat heti kaikissa sivuston paikoissa, joissa osaan viitataan.</span><span class="sxs-lookup"><span data-stu-id="e0abf-122">If you publish changes to the fragment, those changes are immediately reflected in all the places where the fragment is referenced across the site.</span></span> <span data-ttu-id="e0abf-123">Tämän vuoksi osat ovat tehokas tapa käyttää uudelleen moduulin määrityksiä sivustossa ja hallita niitä keskitetysti.</span><span class="sxs-lookup"><span data-stu-id="e0abf-123">Therefore, fragments provide a powerful and efficient way to reuse and centrally manage module configurations on a site.</span></span> <span data-ttu-id="e0abf-124">Tämä tehostettu käyttö ketteröittää toimintoja ja auttaa vähentämään sivuston hallintaan liittyviä kustannuksia.</span><span class="sxs-lookup"><span data-stu-id="e0abf-124">By effectively using them, you can significantly increase agility and help reduce the cost that is associated with managing site content.</span></span>

<span data-ttu-id="e0abf-125">Seuraavassa kuvassa näkyy, kuinka osia voi käyttää jaettujen moduulin määritysten keskitetyssä muokkauksessa sähköisen kaupankäynnin sivustossa.</span><span class="sxs-lookup"><span data-stu-id="e0abf-125">The following illustration shows how fragments can be used to centralize authoring of shared module configurations across an e-Commerce site.</span></span>

![Kuvassa näkyy, kuinka osia voi käyttää jaettujen moduulin määritysten keskitetyssä muokkauksessa sähköisen kaupankäynnin sivustossa](./media/fragment-figure1.png)

## <a name="create-a-fragment"></a><span data-ttu-id="e0abf-127">Osan luominen</span><span class="sxs-lookup"><span data-stu-id="e0abf-127">Create a fragment</span></span>

<span data-ttu-id="e0abf-128">Voit luoda uuden osan tai tallentaa olemassa olevan osan määrityksen osana.</span><span class="sxs-lookup"><span data-stu-id="e0abf-128">You can either create a new fragment or save an existing module configuration as a fragment.</span></span>

### <a name="save-an-existing-module-configuration-as-a-fragment"></a><span data-ttu-id="e0abf-129">Aiemmin luodun moduulin määrityksen tallentaminen osana</span><span class="sxs-lookup"><span data-stu-id="e0abf-129">Save an existing module configuration as a fragment</span></span>

<span data-ttu-id="e0abf-130">Voit muuntaa aiemmin määritetyn moduulin uudelleenkäytettäväksi osaksi seuraavasti Commercen sivustonmuodostimessa.</span><span class="sxs-lookup"><span data-stu-id="e0abf-130">To convert a previously configured module to a reusable fragment in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="e0abf-131">Avaa sivu tai malli, joka sisältää osaksi muunnettavan moduulin.</span><span class="sxs-lookup"><span data-stu-id="e0abf-131">Open a page or template that contains the module that you want to convert to a fragment.</span></span>
1. <span data-ttu-id="e0abf-132">Valitse vasemmalla jäsennysruudussa aiemmin määritetty moduuli tai valitse se suoraan visuaalisessa sivunmuodostimessa.</span><span class="sxs-lookup"><span data-stu-id="e0abf-132">In the outline pane on the left or directly in visual page builder, select the previously configured module.</span></span>
1. <span data-ttu-id="e0abf-133">Valitse kolme pistettä (**...**) moduulin nimen vieressä joko jäsennysruudusta tai valitun moduulin työkaluriviltä visuaalisessa sivunmuodostimessa.</span><span class="sxs-lookup"><span data-stu-id="e0abf-133">Select the ellipsis (**...**) next to the name of the module in either the outline pane or the selected module's toolbar in visual page builder.</span></span> 
1. <span data-ttu-id="e0abf-134">Valitse **Jaa osana**.</span><span class="sxs-lookup"><span data-stu-id="e0abf-134">Select **Share as fragment**.</span></span> 
1. <span data-ttu-id="e0abf-135">Anna **Tallenna osana** -valintaikkunassa osan nimi.</span><span class="sxs-lookup"><span data-stu-id="e0abf-135">In the **Save as fragment** dialog box, enter a name for the fragment.</span></span>
1. <span data-ttu-id="e0abf-136">Valitse **OK**, jos haluat tallentaa moduulin määrityksen osana, joka voidaan lisätä muille sivuille.</span><span class="sxs-lookup"><span data-stu-id="e0abf-136">Select **OK** to save the module configuration as a fragment that can be added to other pages.</span></span>
<!-- The following image shows how to save a module configuration as a fragment.-->
<!--![A screen capture of how to save a module configuration as a fragment](./media/save-as-fragment.png)-->

### <a name="create-a-new-fragment"></a><span data-ttu-id="e0abf-137">Luo uusi osa</span><span class="sxs-lookup"><span data-stu-id="e0abf-137">Create a new fragment</span></span>

<span data-ttu-id="e0abf-138">Uusi osa luodaan Commercen sivustonmuodostimessa seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="e0abf-138">To create a new fragment in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="e0abf-139">Valitse vasemmanpuoleisessa siirtymisruudussa **Osat**.</span><span class="sxs-lookup"><span data-stu-id="e0abf-139">In the navigation pane on the left, select **Fragments**.</span></span>
1. <span data-ttu-id="e0abf-140">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="e0abf-140">Select **New**.</span></span> <span data-ttu-id="e0abf-141">Avautuvassa **Uusi osa** -valintaikkunassa näkyy kaikki käytettävissä olevat moduulityypit.</span><span class="sxs-lookup"><span data-stu-id="e0abf-141">A **New fragment** dialog box appears that shows all the available module types.</span></span> <span data-ttu-id="e0abf-142">Osat voi luoda mistä tahansa moduulityypistä, kuten aiemmin jo mainittiin.</span><span class="sxs-lookup"><span data-stu-id="e0abf-142">As was mentioned earlier, fragments can be created from any module type.</span></span>
1. <span data-ttu-id="e0abf-143">Valitse fragmentin moduulityyppi.</span><span class="sxs-lookup"><span data-stu-id="e0abf-143">Select a module type for your fragment.</span></span>

<!-- The following image shows where to create a new fragment.-->
<!-- ![A screen capture of where to create a new fragment](./media/fragment-nav-menu.png)-->
> [!TIP]
> <span data-ttu-id="e0abf-144">Kun valitset yleisen säilömoduulin tyypin, osan päivittäminen ja määrittäminen sujuu joustavasti myöhemmin.</span><span class="sxs-lookup"><span data-stu-id="e0abf-144">By selecting a generic container module type, you get the most flexibility when you need to update and configure your fragment later.</span></span>

## <a name="add-remove-or-edit-fragments-on-a-page"></a><span data-ttu-id="e0abf-145">Osien lisääminen sivulle tai niiden poistaminen tai muokkaaminen</span><span class="sxs-lookup"><span data-stu-id="e0abf-145">Add, remove, or edit fragments on a page</span></span>

<span data-ttu-id="e0abf-146">Seuraavissa ohjeissa kuvataan, miten osia lisätään, poistetaan ja muokataan.</span><span class="sxs-lookup"><span data-stu-id="e0abf-146">The following procedures describe how to add, remove, and edit fragments.</span></span>

### <a name="add-a-fragment"></a><span data-ttu-id="e0abf-147">Osan lisääminen</span><span class="sxs-lookup"><span data-stu-id="e0abf-147">Add a fragment</span></span>

<span data-ttu-id="e0abf-148">Osa lisätään sivulle Commercen sivustonmuodostimessa seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="e0abf-148">To add a fragment to a page in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="e0abf-149">Valitse vasemmassa jäsennysruudussa tai suoraan visuaalisessa sivunmuodostimessa säilö tai paikka, johon alimoduulit voidaan lisätä.</span><span class="sxs-lookup"><span data-stu-id="e0abf-149">In the outline pane on the left or directly in visual page builder, select a container or slot to which child modules can be added.</span></span>
1. <span data-ttu-id="e0abf-150">Valitse kolme pistettä (**...**) säilön tai paikan nimen vieressä.</span><span class="sxs-lookup"><span data-stu-id="e0abf-150">Select the ellipsis (**...**) next to the name of the container or slot.</span></span>  <span data-ttu-id="e0abf-151">Vaihtoehtoisesti voit valita plusmerkin (**+**), jos visuaalinen sivunmuodostin on käytössä.</span><span class="sxs-lookup"><span data-stu-id="e0abf-151">Alternately, if using visual page builder, select the plus symbol (**+**).</span></span>  
1. <span data-ttu-id="e0abf-152">Valitse **Lisää osa**.</span><span class="sxs-lookup"><span data-stu-id="e0abf-152">Select **Add fragment**.</span></span>
    <!-- ![A screen capture of how to add an existing fragment to a slot or container](./media/add-fragment.png)-->
 
    > [!NOTE]
    > <span data-ttu-id="e0abf-153">Jos säilö tai paikka ei tue uusia alimoduuleja, **Lisää osa** -vaihtoehto ei ole käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="e0abf-153">If the container or slot doesn't support new child modules, the **Add fragment** option is unavailable.</span></span>
    
1. <span data-ttu-id="e0abf-154">Hae **Lisää osa** -valintaikkunassa lisättävä osa ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="e0abf-154">In the **Select fragment** dialog box, search for and select a fragment to add.</span></span> <span data-ttu-id="e0abf-155">Jos käytettävissä olevia osia ei ole näkyvissä, sinun on ehkä ensin luotava osa moduulityypistä, jota valittu säilö tai paikka tukee.</span><span class="sxs-lookup"><span data-stu-id="e0abf-155">If no available fragments are listed, you might first have to create a fragment from a module type that the selected container or slot supports.</span></span>
1. <span data-ttu-id="e0abf-156">Valitse haluamasi fragmentti lisätäksesi sen sivullasi olevaan säilöön tai paikkaan.</span><span class="sxs-lookup"><span data-stu-id="e0abf-156">Select your desired fragment to add it to the container or slot on your page.</span></span>
<!--    ![A screen capture of the fragment picker modal window](./media/fragment-picker.png)-->

> [!NOTE]
> <span data-ttu-id="e0abf-157">Moduulit, jotka sallitaan säilössä tai paikassa, määräytyvät sivun mallin tai moduulien omien määritysten mukaan.</span><span class="sxs-lookup"><span data-stu-id="e0abf-157">The modules that are allowed in a container or slot are defined by the page's template or the modules' own definitions.</span></span>

### <a name="remove-a-fragment"></a><span data-ttu-id="e0abf-158">Osan poistaminen</span><span class="sxs-lookup"><span data-stu-id="e0abf-158">Remove a fragment</span></span>

<span data-ttu-id="e0abf-159">Osa poistetaan Commercen sivustonmuodostimessa sivulla olevasta paikasta tai säilöstä seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="e0abf-159">To remove a fragment from a slot or container on a page in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="e0abf-160">Valitse vasemmanpuoleisessa jäsennysruudussa poistettavan osan nimen vieressä oleva kolmen pisteen painike (**...**) ja valitse sitten roskakorisymboli.</span><span class="sxs-lookup"><span data-stu-id="e0abf-160">In the outline pane on the left, select the ellipsis (**...**) next to the name of the fragment to be removed, and then select the trash can symbol.</span></span>  <span data-ttu-id="e0abf-161">Vaihtoehtoisesti voit valita osan visuaalisessa sivunmuodostimessa ja valita roskakorisymbolin osan työkalurivillä.</span><span class="sxs-lookup"><span data-stu-id="e0abf-161">Alternately, you can select the fragment in visual page builder and select the trash can symbol in the fragment's toolbar.</span></span>
1. <span data-ttu-id="e0abf-162">Kun sinua pyydetään vahvistamaan osan poistaminen, valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="e0abf-162">When you're prompted to confirm that you want to remove the fragment, select **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="e0abf-163">Kun poistat osan sivulta, poistat vain viittauksen kyseiseltä sivulta.</span><span class="sxs-lookup"><span data-stu-id="e0abf-163">When you remove a fragment from a page, you just remove the reference to it from that page.</span></span> <span data-ttu-id="e0abf-164">**Et** poista osaa sivustosta.</span><span class="sxs-lookup"><span data-stu-id="e0abf-164">You do **not** delete the fragment from your site.</span></span> <span data-ttu-id="e0abf-165">Jos haluat poistaa osia sivustosta, käytä osan tarkistusohjelman käyttöliittymää.</span><span class="sxs-lookup"><span data-stu-id="e0abf-165">To delete fragments from your site, you must use the fragment inspector user interface (UI).</span></span> <span data-ttu-id="e0abf-166">Voit poistaa osia sivustosta vain, jos niihin ei tällä hetkellä viitata sivuissa, malleissa tai muissa osissa.</span><span class="sxs-lookup"><span data-stu-id="e0abf-166">You can delete fragments from a site only if they aren't currently referenced by any pages, templates, or other fragments.</span></span>

### <a name="edit-a-fragment"></a><span data-ttu-id="e0abf-167">Osan muokkaaminen</span><span class="sxs-lookup"><span data-stu-id="e0abf-167">Edit a fragment</span></span>

<span data-ttu-id="e0abf-168">Jos haluat muokata osia, sinun on käytettävä osan muokkausohjelman käyttöliittymää.</span><span class="sxs-lookup"><span data-stu-id="e0abf-168">To edit fragments, you must use the fragment editor UI.</span></span> <span data-ttu-id="e0abf-169">Tämä on suunniteltu rajoitus.</span><span class="sxs-lookup"><span data-stu-id="e0abf-169">This restriction is by design.</span></span> <span data-ttu-id="e0abf-170">Sen avulla voidaan varmistaa, että tekijät eivät sekoita tietyn sivun moduulien muokkausprosessia sellaisten osien muokkausprosessiin, joita voidaan jakaa useille sivuille.</span><span class="sxs-lookup"><span data-stu-id="e0abf-170">It helps guarantee that authors don't confuse the process of editing the modules for a specific page with the process of editing fragments that might be shared across many pages.</span></span>

<span data-ttu-id="e0abf-171">Osaa muokataan Commercen sivustonmuodostimessa seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="e0abf-171">To edit a fragment in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="e0abf-172">Valitse vasemmanpuoleisessa siirtymisruudussa **Osat**.</span><span class="sxs-lookup"><span data-stu-id="e0abf-172">In the navigation pane on the left, select **Fragments**.</span></span>
1. <span data-ttu-id="e0abf-173">Valitse **Osat**-kohdassa muokattava osa.</span><span class="sxs-lookup"><span data-stu-id="e0abf-173">Under **Fragments**, select the fragment to edit.</span></span>
1. <span data-ttu-id="e0abf-174">Muokkaa osan moduulin ominaisuuksia ja rakennetta tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="e0abf-174">Edit the fragment's module properties and structure as you require.</span></span> <span data-ttu-id="e0abf-175">Prosessi muistuttaa moduulien muokkausprosessia, jossa moduuleja muokataan sivueditorinäkymässä.</span><span class="sxs-lookup"><span data-stu-id="e0abf-175">The process resembles the process for editing modules are edited in the page editor view.</span></span>

<span data-ttu-id="e0abf-176">Voit muokata osaa myös valitsemalla sen sivulla, mallissa tai pääosassa ja valitsemalla sitten **Muokkaa osaa** -kohdan oikeanpuoleisessa ominaisuusruudussa.</span><span class="sxs-lookup"><span data-stu-id="e0abf-176">You can also edit a fragment by selecting it on a page, in a template, or in a parent fragment, and then selecting **Edit Fragment** in the properties pane on the right.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e0abf-177">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="e0abf-177">Additional resources</span></span>

[<span data-ttu-id="e0abf-178">Mallit ja asettelut – yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="e0abf-178">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="e0abf-179">Mallien käyttö</span><span class="sxs-lookup"><span data-stu-id="e0abf-179">Work with templates</span></span>](work-with-templates.md)

[<span data-ttu-id="e0abf-180">Esimääritettyjen asettelujen käyttö</span><span class="sxs-lookup"><span data-stu-id="e0abf-180">Work with preset layouts</span></span>](work-with-layouts.md)

[<span data-ttu-id="e0abf-181">Julkaisuryhmien kanssa työskenteleminen</span><span class="sxs-lookup"><span data-stu-id="e0abf-181">Work with publish groups</span></span>](publish-groups.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
