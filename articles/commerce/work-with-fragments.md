---
title: Katkelmien käyttäminen
description: Tässä ohjeaiheessa kuvataan, miksi, milloin ja miten osia käytetään Microsoft Dynamics 365 Commerce -sovelluksessa.
author: phinneyridge
manager: annbe
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 3df2d99ef10f909cedef16167fb8d5a0024683b3
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5210944"
---
# <a name="work-with-fragments"></a><span data-ttu-id="45bab-103">Katkelmien käyttäminen</span><span class="sxs-lookup"><span data-stu-id="45bab-103">Work with fragments</span></span> 

[!include [banner](includes/banner.md)]

<span data-ttu-id="45bab-104">Tässä ohjeaiheessa kuvataan, miksi, milloin ja miten osia käytetään Microsoft Dynamics 365 Commerce -sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="45bab-104">This topic describes why, when, and how to use fragments in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="45bab-105">Yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="45bab-105">Overview</span></span>

<span data-ttu-id="45bab-106">Osat mahdollistavat koko sivustossa uudelleenkäytettävien moduulin määritysten keskitetyn muokkauskokemuksen.</span><span class="sxs-lookup"><span data-stu-id="45bab-106">Fragments allow for a centralized authoring experience for module configurations that must be reused throughout your site.</span></span> <span data-ttu-id="45bab-107">Esimerkiksi ylä- ja alatunnisteet sekä ilmoituspalkit määritetään usein osiksi, koska ne jaetaan useille sivuille.</span><span class="sxs-lookup"><span data-stu-id="45bab-107">For example, headers, footers, and banners are often configured as fragments, because they are shared across many pages.</span></span> <span data-ttu-id="45bab-108">Voit ajatella osia pienoisverkkosivuina, jotka voidaan lisätä sivuston muihin sivuihin.</span><span class="sxs-lookup"><span data-stu-id="45bab-108">You can think of fragments as miniature webpages that can be inserted into other pages on your site.</span></span> <span data-ttu-id="45bab-109">Osilla on oma elinkaarensa.</span><span class="sxs-lookup"><span data-stu-id="45bab-109">Fragments have their own lifecycle.</span></span> <span data-ttu-id="45bab-110">Toisin sanoen ne luodaan, päivitetään, niihin viitataan ja ne poistetaan yksittäisinä entiteetteinä muokkaustyökaluissa.</span><span class="sxs-lookup"><span data-stu-id="45bab-110">In other words, they are created, referenced, updated, and deleted as independent entities in the authoring tools.</span></span>

<span data-ttu-id="45bab-111">Kun osat on määritetty, niitä voidaan käyttää aina, kun moduuleja voi käyttää sivuston rakenteessa.</span><span class="sxs-lookup"><span data-stu-id="45bab-111">After fragments are configured, they can be used wherever modules can be used in your site structure.</span></span> <span data-ttu-id="45bab-112">Osiin voi viitata sivuilla, asetteluissa, malleissa ja muissa osissa.</span><span class="sxs-lookup"><span data-stu-id="45bab-112">Fragments can be referenced on pages, in layouts, in templates, and in other fragments.</span></span>

> [!NOTE]
> <span data-ttu-id="45bab-113">Osat voivat olla sisäkkäisiä jopa seitsemän tason syvyyteen muissa osissa.</span><span class="sxs-lookup"><span data-stu-id="45bab-113">Fragments can be nested up to seven levels deep inside other fragments.</span></span>

<span data-ttu-id="45bab-114">Jos haluat edistää esimerkiksi kausiluonteista tapahtumaa useilla sivuston sivuilla, voit käyttää osia.</span><span class="sxs-lookup"><span data-stu-id="45bab-114">For example, if you want to promote a seasonal event cross many pages on our site, you can use a fragment.</span></span> <span data-ttu-id="45bab-115">Uuden osan luontiprosessin ensimmäinen vaihe on valita sen moduulin tyyppi, jolla haluat aloittaa.</span><span class="sxs-lookup"><span data-stu-id="45bab-115">The first step in the process of creating a new fragment is to select the type of module that you want to start from.</span></span> <span data-ttu-id="45bab-116">Tässä esimerkissä voit muodostaa osan hero-moduulista.</span><span class="sxs-lookup"><span data-stu-id="45bab-116">For this example, you can build the fragment from a hero module.</span></span>

> [!NOTE]
> <span data-ttu-id="45bab-117">Osia voi muodostaa mistä tahansa moduulityypistä.</span><span class="sxs-lookup"><span data-stu-id="45bab-117">Fragments can be built from any module type.</span></span>

<span data-ttu-id="45bab-118">Tämän jälkeen voit määrittää hero-osaan määritetyn kampanjasisällön.</span><span class="sxs-lookup"><span data-stu-id="45bab-118">You can then configure the hero fragment with your specific promotional content.</span></span> <span data-ttu-id="45bab-119">Voit myös lokalisoida sen tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="45bab-119">You can also localize it as you require.</span></span> <span data-ttu-id="45bab-120">Uutta erillistä hero-osaa voi tämän jälkeen kuluttaa esimääritettynä moduulina koko sivustossa.</span><span class="sxs-lookup"><span data-stu-id="45bab-120">The new stand-alone hero fragment can then be consumed as a preconfigured module throughout your site.</span></span> <span data-ttu-id="45bab-121">Voit helposti lisätä sen malleihin, tiettyihin sivuihin tai muihin osiin, joissa voi olla hero-moduuleita.</span><span class="sxs-lookup"><span data-stu-id="45bab-121">You can easily add it to templates, to specific pages, or to other fragments that can contain hero modules.</span></span>

<span data-ttu-id="45bab-122">Kaikki paikat, joihin osa lisätään, ovat viittauksia luotuun, keskitettyyn hero-osaan.</span><span class="sxs-lookup"><span data-stu-id="45bab-122">All the places where the fragment is added are references to the central hero fragment that you created.</span></span> <span data-ttu-id="45bab-123">Jos julkaiset osan muutokset, ne vaikuttavat heti kaikissa sivuston paikoissa, joissa osaan viitataan.</span><span class="sxs-lookup"><span data-stu-id="45bab-123">If you publish changes to the fragment, those changes are immediately reflected in all the places where the fragment is referenced across the site.</span></span> <span data-ttu-id="45bab-124">Tämän vuoksi osat ovat tehokas tapa käyttää uudelleen moduulin määrityksiä sivustossa ja hallita niitä keskitetysti.</span><span class="sxs-lookup"><span data-stu-id="45bab-124">Therefore, fragments provide a powerful and efficient way to reuse and centrally manage module configurations on a site.</span></span> <span data-ttu-id="45bab-125">Tämä tehostettu käyttö ketteröittää toimintoja ja auttaa vähentämään sivuston hallintaan liittyviä kustannuksia.</span><span class="sxs-lookup"><span data-stu-id="45bab-125">By effectively using them, you can significantly increase agility and help reduce the cost that is associated with managing site content.</span></span>

<span data-ttu-id="45bab-126">Seuraavassa kuvassa näkyy, kuinka osia voi käyttää jaettujen moduulin määritysten keskitetyssä muokkauksessa sähköisen kaupankäynnin sivustossa.</span><span class="sxs-lookup"><span data-stu-id="45bab-126">The following illustration shows how fragments can be used to centralize authoring of shared module configurations across an e-Commerce site.</span></span>

![Kuvassa näkyy, kuinka osia voi käyttää jaettujen moduulin määritysten keskitetyssä muokkauksessa sähköisen kaupankäynnin sivustossa](./media/fragment-figure1.png)

## <a name="create-a-fragment"></a><span data-ttu-id="45bab-128">Osan luominen</span><span class="sxs-lookup"><span data-stu-id="45bab-128">Create a fragment</span></span>

<span data-ttu-id="45bab-129">Voit luoda uuden osan tai tallentaa olemassa olevan osan määrityksen osana.</span><span class="sxs-lookup"><span data-stu-id="45bab-129">You can either create a new fragment or save an existing module configuration as a fragment.</span></span>

### <a name="save-an-existing-module-configuration-as-a-fragment"></a><span data-ttu-id="45bab-130">Aiemmin luodun moduulin määrityksen tallentaminen osana</span><span class="sxs-lookup"><span data-stu-id="45bab-130">Save an existing module configuration as a fragment</span></span>

<span data-ttu-id="45bab-131">Voit muuntaa aiemmin määritetyn moduulin uudelleenkäytettäväksi osaksi seuraavasti Commercen sivustonmuodostimessa.</span><span class="sxs-lookup"><span data-stu-id="45bab-131">To convert a previously configured module to a reusable fragment in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="45bab-132">Avaa sivu tai malli, joka sisältää osaksi muunnettavan moduulin.</span><span class="sxs-lookup"><span data-stu-id="45bab-132">Open a page or template that contains the module that you want to convert to a fragment.</span></span>
1. <span data-ttu-id="45bab-133">Valitse vasemmalla jäsennysruudussa aiemmin määritetty moduuli tai valitse se suoraan visuaalisessa sivunmuodostimessa.</span><span class="sxs-lookup"><span data-stu-id="45bab-133">In the outline pane on the left or directly in visual page builder, select the previously configured module.</span></span>
1. <span data-ttu-id="45bab-134">Valitse kolme pistettä (**...**) moduulin nimen vieressä joko jäsennysruudusta tai valitun moduulin työkaluriviltä visuaalisessa sivunmuodostimessa.</span><span class="sxs-lookup"><span data-stu-id="45bab-134">Select the ellipsis (**...**) next to the name of the module in either the outline pane or the selected module's toolbar in visual page builder.</span></span> 
1. <span data-ttu-id="45bab-135">Valitse **Jaa osana**.</span><span class="sxs-lookup"><span data-stu-id="45bab-135">Select **Share as fragment**.</span></span> 
1. <span data-ttu-id="45bab-136">Anna **Tallenna osana** -valintaikkunassa osan nimi.</span><span class="sxs-lookup"><span data-stu-id="45bab-136">In the **Save as fragment** dialog box, enter a name for the fragment.</span></span>
1. <span data-ttu-id="45bab-137">Valitse **OK**, jos haluat tallentaa moduulin määrityksen osana, joka voidaan lisätä muille sivuille.</span><span class="sxs-lookup"><span data-stu-id="45bab-137">Select **OK** to save the module configuration as a fragment that can be added to other pages.</span></span>
<!-- The following image shows how to save a module configuration as a fragment.-->
<!--![A screen capture of how to save a module configuration as a fragment](./media/save-as-fragment.png)-->

### <a name="create-a-new-fragment"></a><span data-ttu-id="45bab-138">Luo uusi osa</span><span class="sxs-lookup"><span data-stu-id="45bab-138">Create a new fragment</span></span>

<span data-ttu-id="45bab-139">Uusi osa luodaan Commercen sivustonmuodostimessa seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="45bab-139">To create a new fragment in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="45bab-140">Valitse vasemmanpuoleisessa siirtymisruudussa **Osat**.</span><span class="sxs-lookup"><span data-stu-id="45bab-140">In the navigation pane on the left, select **Fragments**.</span></span>
1. <span data-ttu-id="45bab-141">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="45bab-141">Select **New**.</span></span> <span data-ttu-id="45bab-142">Avautuvassa **Uusi osa** -valintaikkunassa näkyy kaikki käytettävissä olevat moduulityypit.</span><span class="sxs-lookup"><span data-stu-id="45bab-142">A **New fragment** dialog box appears that shows all the available module types.</span></span> <span data-ttu-id="45bab-143">Osat voi luoda mistä tahansa moduulityypistä, kuten aiemmin jo mainittiin.</span><span class="sxs-lookup"><span data-stu-id="45bab-143">As was mentioned earlier, fragments can be created from any module type.</span></span>
1. <span data-ttu-id="45bab-144">Valitse fragmentin moduulityyppi.</span><span class="sxs-lookup"><span data-stu-id="45bab-144">Select a module type for your fragment.</span></span>

<!-- The following image shows where to create a new fragment.-->
<!-- ![A screen capture of where to create a new fragment](./media/fragment-nav-menu.png)-->
> [!TIP]
> <span data-ttu-id="45bab-145">Kun valitset yleisen säilömoduulin tyypin, osan päivittäminen ja määrittäminen sujuu joustavasti myöhemmin.</span><span class="sxs-lookup"><span data-stu-id="45bab-145">By selecting a generic container module type, you get the most flexibility when you need to update and configure your fragment later.</span></span>

## <a name="add-remove-or-edit-fragments-on-a-page"></a><span data-ttu-id="45bab-146">Osien lisääminen sivulle tai niiden poistaminen tai muokkaaminen</span><span class="sxs-lookup"><span data-stu-id="45bab-146">Add, remove, or edit fragments on a page</span></span>

<span data-ttu-id="45bab-147">Seuraavissa ohjeissa kuvataan, miten osia lisätään, poistetaan ja muokataan.</span><span class="sxs-lookup"><span data-stu-id="45bab-147">The following procedures describe how to add, remove, and edit fragments.</span></span>

### <a name="add-a-fragment"></a><span data-ttu-id="45bab-148">Osan lisääminen</span><span class="sxs-lookup"><span data-stu-id="45bab-148">Add a fragment</span></span>

<span data-ttu-id="45bab-149">Osa lisätään sivulle Commercen sivustonmuodostimessa seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="45bab-149">To add a fragment to a page in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="45bab-150">Valitse vasemmassa jäsennysruudussa tai suoraan visuaalisessa sivunmuodostimessa säilö tai paikka, johon alimoduulit voidaan lisätä.</span><span class="sxs-lookup"><span data-stu-id="45bab-150">In the outline pane on the left or directly in visual page builder, select a container or slot to which child modules can be added.</span></span>
1. <span data-ttu-id="45bab-151">Valitse kolme pistettä (**...**) säilön tai paikan nimen vieressä.</span><span class="sxs-lookup"><span data-stu-id="45bab-151">Select the ellipsis (**...**) next to the name of the container or slot.</span></span>  <span data-ttu-id="45bab-152">Vaihtoehtoisesti voit valita plusmerkin (**+**), jos visuaalinen sivunmuodostin on käytössä.</span><span class="sxs-lookup"><span data-stu-id="45bab-152">Alternately, if using visual page builder, select the plus symbol (**+**).</span></span>  
1. <span data-ttu-id="45bab-153">Valitse **Lisää osa**.</span><span class="sxs-lookup"><span data-stu-id="45bab-153">Select **Add fragment**.</span></span>
    <!-- ![A screen capture of how to add an existing fragment to a slot or container](./media/add-fragment.png)-->
 
    > [!NOTE]
    > <span data-ttu-id="45bab-154">Jos säilö tai paikka ei tue uusia alimoduuleja, **Lisää osa** -vaihtoehto ei ole käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="45bab-154">If the container or slot doesn't support new child modules, the **Add fragment** option is unavailable.</span></span>
    
1. <span data-ttu-id="45bab-155">Hae **Lisää osa** -valintaikkunassa lisättävä osa ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="45bab-155">In the **Select fragment** dialog box, search for and select a fragment to add.</span></span> <span data-ttu-id="45bab-156">Jos käytettävissä olevia osia ei ole näkyvissä, sinun on ehkä ensin luotava osa moduulityypistä, jota valittu säilö tai paikka tukee.</span><span class="sxs-lookup"><span data-stu-id="45bab-156">If no available fragments are listed, you might first have to create a fragment from a module type that the selected container or slot supports.</span></span>
1. <span data-ttu-id="45bab-157">Valitse haluamasi fragmentti lisätäksesi sen sivullasi olevaan säilöön tai paikkaan.</span><span class="sxs-lookup"><span data-stu-id="45bab-157">Select your desired fragment to add it to the container or slot on your page.</span></span>
<!--    ![A screen capture of the fragment picker modal window](./media/fragment-picker.png)-->

> [!NOTE]
> <span data-ttu-id="45bab-158">Moduulit, jotka sallitaan säilössä tai paikassa, määräytyvät sivun mallin tai moduulien omien määritysten mukaan.</span><span class="sxs-lookup"><span data-stu-id="45bab-158">The modules that are allowed in a container or slot are defined by the page's template or the modules' own definitions.</span></span>

### <a name="remove-a-fragment"></a><span data-ttu-id="45bab-159">Osan poistaminen</span><span class="sxs-lookup"><span data-stu-id="45bab-159">Remove a fragment</span></span>

<span data-ttu-id="45bab-160">Osa poistetaan Commercen sivustonmuodostimessa sivulla olevasta paikasta tai säilöstä seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="45bab-160">To remove a fragment from a slot or container on a page in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="45bab-161">Valitse vasemmanpuoleisessa jäsennysruudussa poistettavan osan nimen vieressä oleva kolmen pisteen painike (**...**) ja valitse sitten roskakorisymboli.</span><span class="sxs-lookup"><span data-stu-id="45bab-161">In the outline pane on the left, select the ellipsis (**...**) next to the name of the fragment to be removed, and then select the trash can symbol.</span></span>  <span data-ttu-id="45bab-162">Vaihtoehtoisesti voit valita osan visuaalisessa sivunmuodostimessa ja valita roskakorisymbolin osan työkalurivillä.</span><span class="sxs-lookup"><span data-stu-id="45bab-162">Alternately, you can select the fragment in visual page builder and select the trash can symbol in the fragment's toolbar.</span></span>
1. <span data-ttu-id="45bab-163">Kun sinua pyydetään vahvistamaan osan poistaminen, valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="45bab-163">When you're prompted to confirm that you want to remove the fragment, select **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="45bab-164">Kun poistat osan sivulta, poistat vain viittauksen kyseiseltä sivulta.</span><span class="sxs-lookup"><span data-stu-id="45bab-164">When you remove a fragment from a page, you just remove the reference to it from that page.</span></span> <span data-ttu-id="45bab-165">**Et** poista osaa sivustosta.</span><span class="sxs-lookup"><span data-stu-id="45bab-165">You do **not** delete the fragment from your site.</span></span> <span data-ttu-id="45bab-166">Jos haluat poistaa osia sivustosta, käytä osan tarkistusohjelman käyttöliittymää.</span><span class="sxs-lookup"><span data-stu-id="45bab-166">To delete fragments from your site, you must use the fragment inspector user interface (UI).</span></span> <span data-ttu-id="45bab-167">Voit poistaa osia sivustosta vain, jos niihin ei tällä hetkellä viitata sivuissa, malleissa tai muissa osissa.</span><span class="sxs-lookup"><span data-stu-id="45bab-167">You can delete fragments from a site only if they aren't currently referenced by any pages, templates, or other fragments.</span></span>

### <a name="edit-a-fragment"></a><span data-ttu-id="45bab-168">Osan muokkaaminen</span><span class="sxs-lookup"><span data-stu-id="45bab-168">Edit a fragment</span></span>

<span data-ttu-id="45bab-169">Jos haluat muokata osia, sinun on käytettävä osan muokkausohjelman käyttöliittymää.</span><span class="sxs-lookup"><span data-stu-id="45bab-169">To edit fragments, you must use the fragment editor UI.</span></span> <span data-ttu-id="45bab-170">Tämä on suunniteltu rajoitus.</span><span class="sxs-lookup"><span data-stu-id="45bab-170">This restriction is by design.</span></span> <span data-ttu-id="45bab-171">Sen avulla voidaan varmistaa, että tekijät eivät sekoita tietyn sivun moduulien muokkausprosessia sellaisten osien muokkausprosessiin, joita voidaan jakaa useille sivuille.</span><span class="sxs-lookup"><span data-stu-id="45bab-171">It helps guarantee that authors don't confuse the process of editing the modules for a specific page with the process of editing fragments that might be shared across many pages.</span></span>

<span data-ttu-id="45bab-172">Osaa muokataan Commercen sivustonmuodostimessa seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="45bab-172">To edit a fragment in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="45bab-173">Valitse vasemmanpuoleisessa siirtymisruudussa **Osat**.</span><span class="sxs-lookup"><span data-stu-id="45bab-173">In the navigation pane on the left, select **Fragments**.</span></span>
1. <span data-ttu-id="45bab-174">Valitse **Osat**-kohdassa muokattava osa.</span><span class="sxs-lookup"><span data-stu-id="45bab-174">Under **Fragments**, select the fragment to edit.</span></span>
1. <span data-ttu-id="45bab-175">Muokkaa osan moduulin ominaisuuksia ja rakennetta tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="45bab-175">Edit the fragment's module properties and structure as you require.</span></span> <span data-ttu-id="45bab-176">Prosessi muistuttaa moduulien muokkausprosessia, jossa moduuleja muokataan sivueditorinäkymässä.</span><span class="sxs-lookup"><span data-stu-id="45bab-176">The process resembles the process for editing modules are edited in the page editor view.</span></span>

<span data-ttu-id="45bab-177">Voit muokata osaa myös valitsemalla sen sivulla, mallissa tai pääosassa ja valitsemalla sitten **Muokkaa osaa** -kohdan oikeanpuoleisessa ominaisuusruudussa.</span><span class="sxs-lookup"><span data-stu-id="45bab-177">You can also edit a fragment by selecting it on a page, in a template, or in a parent fragment, and then selecting **Edit Fragment** in the properties pane on the right.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="45bab-178">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="45bab-178">Additional resources</span></span>

[<span data-ttu-id="45bab-179">Mallit ja asettelut – yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="45bab-179">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="45bab-180">Mallien käyttö</span><span class="sxs-lookup"><span data-stu-id="45bab-180">Work with templates</span></span>](work-with-templates.md)

[<span data-ttu-id="45bab-181">Esimääritettyjen asettelujen käyttö</span><span class="sxs-lookup"><span data-stu-id="45bab-181">Work with preset layouts</span></span>](work-with-layouts.md)

[<span data-ttu-id="45bab-182">Julkaisuryhmien kanssa työskenteleminen</span><span class="sxs-lookup"><span data-stu-id="45bab-182">Work with publish groups</span></span>](publish-groups.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]