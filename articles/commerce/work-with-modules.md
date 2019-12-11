---
title: Moduulien käyttäminen
description: Tässä ohjeaiheessa kuvataan, miten ja milloin moduuleja käytetään Microsoft Dynamics 365 Commerce -sovelluksessa.
author: v-chgri
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: phinneyridge
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 06a26e5dfd35bf229e67ed27213210d0da726bdf
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/01/2019
ms.locfileid: "2698070"
---
# <a name="work-with-modules"></a><span data-ttu-id="21a55-103">Moduulien käyttäminen</span><span class="sxs-lookup"><span data-stu-id="21a55-103">Work with modules</span></span>

<span data-ttu-id="21a55-104">Tässä ohjeaiheessa kuvataan, miten ja milloin moduuleja käytetään Microsoft Dynamics 365 Commerce -sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="21a55-104">This topic describes how and when to use modules in Microsoft Dynamics 365 Commerce.</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

## <a name="overview"></a><span data-ttu-id="21a55-105">Yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="21a55-105">Overview</span></span>

<span data-ttu-id="21a55-106">Moduulit ovat loogisia rakenneosia, jotka muodostavat sivurakenteen. Niillä on eri tarkoitukset ja käyttöalueet.</span><span class="sxs-lookup"><span data-stu-id="21a55-106">Modules are logical building blocks that make up your page structure, and they have various purposes and scopes.</span></span> <span data-ttu-id="21a55-107">Jotkin moduulit ovat korkean tason säilöjä, joiden ainoa tarkoitus on säilyttää ja järjestää muita moduuleja (alimoduuleja).</span><span class="sxs-lookup"><span data-stu-id="21a55-107">Some modules are high-level containers, and their only purpose is to hold and organize other modules (child modules).</span></span> <span data-ttu-id="21a55-108">Muilla moduuleilla, kuten yksinkertaisella kuvansijoittelumoduulilla, on tarkkaan määritetty tarkoitus.</span><span class="sxs-lookup"><span data-stu-id="21a55-108">Other modules, such as a simple image placement module, have a very specific purpose.</span></span> <span data-ttu-id="21a55-109">Muut moduulit, kuten karusellimoduuli, ovat näiden kahden luokan välissä.</span><span class="sxs-lookup"><span data-stu-id="21a55-109">Other modules, such as a carousel module, fall somewhere between those two categories.</span></span>

<span data-ttu-id="21a55-110">Dynamics 365 Commerce -sivusto sisältää oletusarvoisesti aloituspakkausmoduulikirjaston. Sen avulla voit arkistoida useimmat sähköisen kaupankäynnin perusskenaariot.</span><span class="sxs-lookup"><span data-stu-id="21a55-110">By default, your Dynamics 365 Commerce site includes a starter kit module library that lets you achieve most basic e-Commerce scenarios.</span></span> <span data-ttu-id="21a55-111">Voit muodostaa kattavan sähköisen kaupankäynnin sivuston pelkästään näiden moduulien avulla.</span><span class="sxs-lookup"><span data-stu-id="21a55-111">You should be able to construct an end-to-end e-Commerce site just by using these modules.</span></span> <span data-ttu-id="21a55-112">Saatat kuitenkin haluta mukauttaa näitä moduuleja tai luoda uusia mukautettuja moduuleja erityistarpeita varten.</span><span class="sxs-lookup"><span data-stu-id="21a55-112">However, you might also want to customize these modules or build new, custom modules for specific needs.</span></span> <span data-ttu-id="21a55-113">Voit käyttää mukautettujen moduulien luomisessa moduulin suunnittelun SDK:ta. Sen avulla voit luoda mukautetun moduulikirjaston.</span><span class="sxs-lookup"><span data-stu-id="21a55-113">If you want to build custom modules, a module design software development kit (SDK) is available to help you create a custom module library.</span></span>

## <a name="container-modules-and-slots"></a><span data-ttu-id="21a55-114">Konttimoduulit ja -paikat</span><span class="sxs-lookup"><span data-stu-id="21a55-114">Container modules and slots</span></span>

<span data-ttu-id="21a55-115">Kuten aiemmin mainittiin, jotkin moduulit on suunniteltu alimoduulien säilytystä varten.</span><span class="sxs-lookup"><span data-stu-id="21a55-115">As was mentioned earlier, some modules are designed to hold child modules.</span></span> <span data-ttu-id="21a55-116">Näitä moduuleja kutsutaan *säilöiksi*. Ne mahdollistavat sisäkkäisten moduulien hierarkian muodostamisen.</span><span class="sxs-lookup"><span data-stu-id="21a55-116">These modules are known as *containers*, and they allow for hierarchies of nested modules.</span></span> <span data-ttu-id="21a55-117">Konttimoduuleissa on *paikkoja*.</span><span class="sxs-lookup"><span data-stu-id="21a55-117">Container modules include *slots*.</span></span> <span data-ttu-id="21a55-118">Paikkojen avulla käsitellään säilön alimoduulien asettelua ja tarkoitusta.</span><span class="sxs-lookup"><span data-stu-id="21a55-118">Slots are used to handle the layout and purpose of child modules in the container.</span></span> <span data-ttu-id="21a55-119">Seuraavassa on esimerkki perussivun säilömoduulista (ylimmän tason moduulista millä tahansa sivulla), joka määrittää useita tärkeitä paikkoja:</span><span class="sxs-lookup"><span data-stu-id="21a55-119">An example is a basic page container module (a top-level module for any page) that defines several important slots:</span></span>

- <span data-ttu-id="21a55-120">Ylätunnistepaikka</span><span class="sxs-lookup"><span data-stu-id="21a55-120">A header slot</span></span>
- <span data-ttu-id="21a55-121">Tekstiosapaikka</span><span class="sxs-lookup"><span data-stu-id="21a55-121">A body slot</span></span>
- <span data-ttu-id="21a55-122">Alatunnistepaikka</span><span class="sxs-lookup"><span data-stu-id="21a55-122">A footer slot</span></span>

<span data-ttu-id="21a55-123">Moduulin kehittäjä määrittää nämä paikat. Hän määrittää myös, mitkä alimoduulit ja miten monta alimoduulia voidaan laittaa suoraan paikan sisään.</span><span class="sxs-lookup"><span data-stu-id="21a55-123">The module's developer defines these slots, and determines which child modules and how many child modules can be put directly inside it.</span></span> <span data-ttu-id="21a55-124">Esimerkiksi ylätunnistepaikka voi tukea vain yhtä **ylätunnistemoduuli**-tyyppiä, kun taas tekstiosapaikka voi tukea rajoittamatonta määrää moduulityyppejä (ei kutienkaan muita sivun säilömoduuleja).</span><span class="sxs-lookup"><span data-stu-id="21a55-124">For example, the header slot might support only one module of the **Header Module** type, whereas the body slot might support an unlimited number of modules of any type (except other page container modules).</span></span>

<span data-ttu-id="21a55-125">Sivun tekijöiden ei tarvitse tietää etukäteen muokkaustyökaluissa, mitkä moduulit voi asettaa kuhunkin paikkaan.</span><span class="sxs-lookup"><span data-stu-id="21a55-125">In the authoring tools, page authors don't have to know in advance which modules can and can't be put in each slot.</span></span> <span data-ttu-id="21a55-126">Kun sivun tekijät valitsevat paikan ja yrittävät sitten valita siihen lisättävän moduulin, he näkevät suodatetun näkymän moduulityypeistä, joita kyseinen paikka tukee.</span><span class="sxs-lookup"><span data-stu-id="21a55-126">When page authors select a slot and then try to select a module to add to it, they see a filtered view of module types that are supported for that slot.</span></span>

## <a name="content-modules"></a><span data-ttu-id="21a55-127">Sisältömoduulit</span><span class="sxs-lookup"><span data-stu-id="21a55-127">Content modules</span></span>

<span data-ttu-id="21a55-128">Sisältömoduulit sisältävät sisältö- ja mediaelementtejä, kuten tekstiä (esimerkiksi otsikoita, kappaleita ja linkkejä) tai resurssiviitteitä (esimerkiksi kuvia, videota ja PDF-tiedostoja).</span><span class="sxs-lookup"><span data-stu-id="21a55-128">Content modules contain content and media elements, such as text (for example, headlines, paragraphs, and links) or asset references (for example, images, video, and PDFs).</span></span> <span data-ttu-id="21a55-129">Esimerkkejä yleisistä sisältömoduulityypeistä ovat **Hero**, **Ominaisuus** ja **Ilmoituspalkki**.</span><span class="sxs-lookup"><span data-stu-id="21a55-129">Examples of typical content module types are **Hero**, **Feature**, and **Banner**.</span></span> <span data-ttu-id="21a55-130">Nämä kolme moduulityyppiä voivat sisältää tekstiä tai mediaa. Ne eivät tarvitse alimoduuleja voidakseen näyttää sivulla asioita.</span><span class="sxs-lookup"><span data-stu-id="21a55-130">Modules of these three types can contain text or media, and they don't require any child modules to make something visible on a page.</span></span>

<span data-ttu-id="21a55-131">Suurin osa yleisistä päivittäisistä sivun- ja sisällöntuottamisaktiviteeteista liittyy sisältömoduuleihin. Tämä pääasiassa sen vuoksi, että nämä moduulit määrittävät pääsäilömoduuleissa hahmonnetun todellisen sisällön.</span><span class="sxs-lookup"><span data-stu-id="21a55-131">The majority of typical, day-to-day page and content authoring activities involve content modules, primarily because these modules define the actual content that is rendered in their parent container modules.</span></span> <span data-ttu-id="21a55-132">Käytettävissä on useita sisältömoduuleja. Nämä moduulit ovat yleensä viimeisiä sisäkkäisten moduulien sivuhierarkiaan lisättäviä osia.</span><span class="sxs-lookup"><span data-stu-id="21a55-132">Many content modules are available, and these modules are typically the last pieces that you will add to a page's hierarchy of nested modules.</span></span>

<span data-ttu-id="21a55-133">Seuraavassa kuvassa näkyy, kuinka moduulit ovat sisäkkäin pääsäilömoduulin paikoissa.</span><span class="sxs-lookup"><span data-stu-id="21a55-133">The following illustration shows how modules are nested inside parent container module slots.</span></span>

![Sisäkkäiset moduulit](../commerce/media/basic-module-nesting.png)

## <a name="add-or-remove-modules"></a><span data-ttu-id="21a55-135">Moduulien lisääminen tai poistaminen</span><span class="sxs-lookup"><span data-stu-id="21a55-135">Add or remove modules</span></span>

<span data-ttu-id="21a55-136">Seuraavissa ohjeissa kuvataan, miten moduuleja lisätään ja poistetaan.</span><span class="sxs-lookup"><span data-stu-id="21a55-136">The following procedures describe how to add and remove modules.</span></span>

### <a name="add-a-module"></a><span data-ttu-id="21a55-137">Moduulin lisääminen</span><span class="sxs-lookup"><span data-stu-id="21a55-137">Add a module</span></span>

<span data-ttu-id="21a55-138">Voit lisätä sivun moduulin paikkaan tai säilöön seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="21a55-138">To add a module to a slot or container on a page, follow these steps.</span></span>

1. <span data-ttu-id="21a55-139">Valitse vasemmalla olevasta jäsennysruudusta säilö tai paikka, johon alimoduuli voidaan lisätä.</span><span class="sxs-lookup"><span data-stu-id="21a55-139">In the outline pane on the left, select a container or slot that a child module can be added to.</span></span>

    > [!NOTE]
    > <span data-ttu-id="21a55-140">Moduulin suunnittelija määrittää moduulityyppien luettelon, joka voidaan lisätä tiettyyn moduulipaikkaan.</span><span class="sxs-lookup"><span data-stu-id="21a55-140">The module designer defines the list of modules types that can be added to a specific module slot.</span></span> <span data-ttu-id="21a55-141">Mallien tekijät voivat tämän jälkeen tarkentaa sallittuja moduulivaihtoehtoja. Tämän avulla varmistetaan yhdenmukainen hakukoneoptimointi ja luotitehokkuus kaikilla sivuilla, jotka on luotu tietyn mallin avulla.</span><span class="sxs-lookup"><span data-stu-id="21a55-141">Template authors can then refine the allowed module options to help guarantee consistent search engine optimization (SEO) and authoring efficiency for all the pages pages that are built from a specific template.</span></span>

1. <span data-ttu-id="21a55-142">Valitse moduulin kolmen pisteen painike (**...**) ja valitse sitten **Lisää moduuli**.</span><span class="sxs-lookup"><span data-stu-id="21a55-142">Select the ellipsis button (**...**) for the module, and then select **Add Module**.</span></span> <span data-ttu-id="21a55-143">**Lisää moduuli** -valintaikkuna tulee näkyviin.</span><span class="sxs-lookup"><span data-stu-id="21a55-143">The **Add Module** dialog box appears.</span></span> <span data-ttu-id="21a55-144">Tämä valintaikkuna suodatetaan automaattisesti siten, että siinä näkyvät vain ne moduulit, joita valittu säilö tai paikka tukee.</span><span class="sxs-lookup"><span data-stu-id="21a55-144">This dialog box is automatically filtered so that it shows only modules that are supported in the selected container or slot.</span></span> <span data-ttu-id="21a55-145">Moduuliluettelo määräytyy sivun mallin tai säilömoduulin määrityksen mukaan.</span><span class="sxs-lookup"><span data-stu-id="21a55-145">The list of modules is determined by the page's template or the container module definition.</span></span>

    > [!NOTE]
    > <span data-ttu-id="21a55-146">Jos säilö tai paikka ei tue uusia alimoduuleja, **Lisää moduuli** -vaihtoehto ei ole käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="21a55-146">If a container or slot doesn't support new child modules, the **Add Module** option is unavailable.</span></span>

1. <span data-ttu-id="21a55-147">Hae valintaikkunassa sivulle lisättävä moduuli ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="21a55-147">In the dialog box, search for and select a module to add to your page.</span></span>

    > [!TIP]
    > <span data-ttu-id="21a55-148">Aloittelijan kannattaa käsitellä ensin **Ominaisuus**- ja **Hero**-moduulityyppejä.</span><span class="sxs-lookup"><span data-stu-id="21a55-148">**Feature** and **Hero** are good module types for beginners to work with.</span></span>

1. <span data-ttu-id="21a55-149">Valitse **OK**, jos haluat lisätä valitun moduulin sivun valittuun säilöön tai paikkaan.</span><span class="sxs-lookup"><span data-stu-id="21a55-149">Select **OK** to add the selected module to the selected container or slot on your page.</span></span>

### <a name="remove-a-module"></a><span data-ttu-id="21a55-150">Moduulin poistaminen</span><span class="sxs-lookup"><span data-stu-id="21a55-150">Remove a module</span></span>

<span data-ttu-id="21a55-151">Voit poistaa sivun moduulin paikasta tai säilöstä seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="21a55-151">To remove a module from a slot or container on a page, follow these steps.</span></span>

1. <span data-ttu-id="21a55-152">Valitse vasemmanpuoleisessa jäsennysruudussa poistettavan moduulin nimen vieressä oleva kolmen pisteen painike ja valitse sitten roskakoripainike.</span><span class="sxs-lookup"><span data-stu-id="21a55-152">In the outline pane on the left, select the ellipsis button next to the name of the module to remove, and then select the trash can button.</span></span>
1. <span data-ttu-id="21a55-153">Kun sinua pyydetään vahvistamaan moduulin poistaminen, valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="21a55-153">When you're prompted to confirm that you want to remove the module, select **OK**.</span></span>

## <a name="configure-modules"></a><span data-ttu-id="21a55-154">Moduulien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="21a55-154">Configure modules</span></span>

<span data-ttu-id="21a55-155">Seuraavissa ohjeissa kuvataan, miten sisältö ja säilömoduulit määritetään.</span><span class="sxs-lookup"><span data-stu-id="21a55-155">The following procedures describe how to configure content and container modules.</span></span>

### <a name="configure-a-content-module"></a><span data-ttu-id="21a55-156">Sisältömoduulin määrittäminen</span><span class="sxs-lookup"><span data-stu-id="21a55-156">Configure a content module</span></span>

<span data-ttu-id="21a55-157">Voit määrittää sivun sisältömoduulin seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="21a55-157">To configure a content module on a page, follow these steps.</span></span>

1. <span data-ttu-id="21a55-158">Valitse vasemmanpuoleisessa jäsennysruudussa sisältömoduulin tyyppi (esimerkiksi **Ominaisuus**, **Hero** tai **Ilmoituspalkki**).</span><span class="sxs-lookup"><span data-stu-id="21a55-158">In the outline pane on the left, select a content module type (for example, **Feature**, **Hero**, or **Banner**).</span></span>
1. <span data-ttu-id="21a55-159">Laajenna oikeanpuoleisessa ominaisuusruudussa sisäkkäiset ohjausobjektit valitsemalla ylätunnisteet ja määrittämällä vaaditut ohjausobjektin arvot.</span><span class="sxs-lookup"><span data-stu-id="21a55-159">In the properties pane on the right, expand the nested controls by selecting the headers, and set any required control values.</span></span>
1. <span data-ttu-id="21a55-160">Jos ominaisuusruudussa on **Tietojen määritys** -osa, valitse ja laajenna se.</span><span class="sxs-lookup"><span data-stu-id="21a55-160">If the properties pane has a **Data Configuration** section, select it to expand it.</span></span> <span data-ttu-id="21a55-161">Muussa tapauksessa siirry vaiheeseen 5.</span><span class="sxs-lookup"><span data-stu-id="21a55-161">Otherwise, go to step 5.</span></span>
1. <span data-ttu-id="21a55-162">Jos näkyvissä on **Lisää tietolähde** -painike, valitse se ja valitse sitten lisättävät sisältönimikkeet.</span><span class="sxs-lookup"><span data-stu-id="21a55-162">If there is a **Add Data Source** button, select it, and then select the content items to add.</span></span>
1. <span data-ttu-id="21a55-163">Anna kaikkien pakollisten tai haluttujen moduulin ohjausobjektien asetukset.</span><span class="sxs-lookup"><span data-stu-id="21a55-163">Enter settings for any required or desired module controls.</span></span>
1. <span data-ttu-id="21a55-164">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="21a55-164">Select **Save**.</span></span>

### <a name="configure-a-container-module"></a><span data-ttu-id="21a55-165">Konttimoduulin määrittäminen</span><span class="sxs-lookup"><span data-stu-id="21a55-165">Configure a container module</span></span>

<span data-ttu-id="21a55-166">Voit määrittää sivun säilömoduulin seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="21a55-166">To configure a container module on a page, follow these steps.</span></span>

1. <span data-ttu-id="21a55-167">Valitse sivulla oleva säilömoduuli (esimerkiksi karuselli- tai nestesäilömoduuli).</span><span class="sxs-lookup"><span data-stu-id="21a55-167">Select a container module on your page (for example, a carousel or fluid container module).</span></span>
1. <span data-ttu-id="21a55-168">Laajenna oikeanpuoleisessa ominaisuusruudussa sisäkkäiset ohjausobjektit valitsemalla ylätunnisteet ja määrittämällä vaaditut ohjausobjektin arvot.</span><span class="sxs-lookup"><span data-stu-id="21a55-168">In the properties pane on the right, expand the nested controls by selecting the headers, and set any required control values.</span></span>
1. <span data-ttu-id="21a55-169">Valitse vasemmanpuoleisessa jäsennysruudussa säilön tai jonkin sen sisällä olevan paikan nimen vieressä oleva kolmen pisteen painike ja valitse sitten **Lisää moduuliin**.</span><span class="sxs-lookup"><span data-stu-id="21a55-169">In the outline pane on the left, select the ellipsis button next to the name of either the container or any slots inside the container, and then select **Add Module**.</span></span> <span data-ttu-id="21a55-170">Lisää sitten alimoduulit valittuun säilöön.</span><span class="sxs-lookup"><span data-stu-id="21a55-170">Then add child modules to the selected container.</span></span> <span data-ttu-id="21a55-171">Lisätietoja on tämän ohjeaiheen edellä olevassa kohdassa [Moduulin lisääminen](#add-a-module).</span><span class="sxs-lookup"><span data-stu-id="21a55-171">For more information, see the [Add a module](#add-a-module) procedure earlier in this topic.</span></span>
1. <span data-ttu-id="21a55-172">Jos pääsäilössä on useita alimoduuleja sisaruksina, voit muuttaa niiden näyttöjärjestystä pääsäilössä.</span><span class="sxs-lookup"><span data-stu-id="21a55-172">If multiple child modules exist as siblings in a parent container, you can change their display order in the parent container.</span></span> <span data-ttu-id="21a55-173">Valitse moduulin kolmen pisteen painike ja käytä sitten ylä- ja alanuolipainikkeita.</span><span class="sxs-lookup"><span data-stu-id="21a55-173">Select the ellipsis button for a module, and then use the up arrow and down arrow buttons.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="21a55-174">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="21a55-174">Additional resources</span></span>

[<span data-ttu-id="21a55-175">Mallit ja asettelut – yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="21a55-175">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="21a55-176">Mallien käyttö</span><span class="sxs-lookup"><span data-stu-id="21a55-176">Work with templates</span></span>](work-with-templates.md)

[<span data-ttu-id="21a55-177">Esimääritettyjen asettelujen käyttö</span><span class="sxs-lookup"><span data-stu-id="21a55-177">Work with preset layouts</span></span>](work-with-layouts.md)

[<span data-ttu-id="21a55-178">Katkelmien käyttäminen</span><span class="sxs-lookup"><span data-stu-id="21a55-178">Work with fragments</span></span>](work-with-fragments.md)

[<span data-ttu-id="21a55-179">Konttimoduulin lisääminen sivulle</span><span class="sxs-lookup"><span data-stu-id="21a55-179">Add a container module to a page</span></span>](add-container-module.md)

[<span data-ttu-id="21a55-180">Sisällönsijoittelumoduulien lisääminen sivulla</span><span class="sxs-lookup"><span data-stu-id="21a55-180">Add content placement modules to a page</span></span>](add-content-placement-modules.md)

