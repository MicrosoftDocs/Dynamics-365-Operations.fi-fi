---
title: Moduulien käyttäminen
description: Tässä ohjeaiheessa kuvataan, miten ja milloin moduuleja käytetään Microsoft Dynamics 365 Commerce -sovelluksessa.
author: phinneyridge
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: eddee09fa81c18bc464b7768921981e6b5159a3e
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5210896"
---
# <a name="work-with-modules"></a><span data-ttu-id="4d6e1-103">Moduulien käyttäminen</span><span class="sxs-lookup"><span data-stu-id="4d6e1-103">Work with modules</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="4d6e1-104">Tässä ohjeaiheessa kuvataan, miten ja milloin moduuleja käytetään Microsoft Dynamics 365 Commerce -sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="4d6e1-104">This topic describes how and when to use modules in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="4d6e1-105">Yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="4d6e1-105">Overview</span></span>

<span data-ttu-id="4d6e1-106">Moduulit ovat loogisia rakenneosia, jotka muodostavat sivurakenteen. Niillä on eri tarkoitukset ja käyttöalueet.</span><span class="sxs-lookup"><span data-stu-id="4d6e1-106">Modules are logical building blocks that make up your page structure, and they have various purposes and scopes.</span></span> <span data-ttu-id="4d6e1-107">Jotkin moduulit ovat korkean tason säilöjä, joiden ainoa tarkoitus on säilyttää ja järjestää muita moduuleja (alimoduuleja).</span><span class="sxs-lookup"><span data-stu-id="4d6e1-107">Some modules are high-level containers, and their only purpose is to hold and organize other modules (child modules).</span></span> <span data-ttu-id="4d6e1-108">Muilla moduuleilla, kuten yksinkertaisella kuvansijoittelumoduulilla, on tarkkaan määritetty tarkoitus.</span><span class="sxs-lookup"><span data-stu-id="4d6e1-108">Other modules, such as a simple image placement module, have a very specific purpose.</span></span> <span data-ttu-id="4d6e1-109">Muut moduulit, kuten karusellimoduuli, ovat näiden kahden luokan välissä.</span><span class="sxs-lookup"><span data-stu-id="4d6e1-109">Other modules, such as a carousel module, fall somewhere between those two categories.</span></span>

<span data-ttu-id="4d6e1-110">Dynamics 365 Commerce -sivusto sisältää oletusarvoisesti moduulikirjaston. Sen avulla voit arkistoida useimmat sähköisen kaupankäynnin perusskenaariot.</span><span class="sxs-lookup"><span data-stu-id="4d6e1-110">By default, your Dynamics 365 Commerce site includes a module library that lets you achieve most basic e-Commerce scenarios.</span></span> <span data-ttu-id="4d6e1-111">Voit muodostaa kattavan sähköisen kaupankäynnin sivuston pelkästään näiden moduulien avulla.</span><span class="sxs-lookup"><span data-stu-id="4d6e1-111">You should be able to construct an end-to-end e-Commerce site just by using these modules.</span></span> <span data-ttu-id="4d6e1-112">Saatat kuitenkin haluta mukauttaa näitä moduuleja tai luoda uusia mukautettuja moduuleja erityistarpeita varten.</span><span class="sxs-lookup"><span data-stu-id="4d6e1-112">However, you might also want to customize these modules or build new, custom modules for specific needs.</span></span> <span data-ttu-id="4d6e1-113">Voit käyttää mukautettujen moduulien luomisessa moduulin suunnittelun SDK:ta. Sen avulla voit luoda mukautetun moduulikirjaston.</span><span class="sxs-lookup"><span data-stu-id="4d6e1-113">If you want to build custom modules, a module design software development kit (SDK) is available to help you create a custom module library.</span></span>

## <a name="container-modules-and-slots"></a><span data-ttu-id="4d6e1-114">Konttimoduulit ja -paikat</span><span class="sxs-lookup"><span data-stu-id="4d6e1-114">Container modules and slots</span></span>

<span data-ttu-id="4d6e1-115">Kuten aiemmin mainittiin, jotkin moduulit on suunniteltu alimoduulien säilytystä varten.</span><span class="sxs-lookup"><span data-stu-id="4d6e1-115">As was mentioned earlier, some modules are designed to hold child modules.</span></span> <span data-ttu-id="4d6e1-116">Näitä moduuleja kutsutaan *säilöiksi*. Ne mahdollistavat sisäkkäisten moduulien hierarkian muodostamisen.</span><span class="sxs-lookup"><span data-stu-id="4d6e1-116">These modules are known as *containers*, and they allow for hierarchies of nested modules.</span></span> <span data-ttu-id="4d6e1-117">Konttimoduuleissa on *paikkoja*.</span><span class="sxs-lookup"><span data-stu-id="4d6e1-117">Container modules include *slots*.</span></span> <span data-ttu-id="4d6e1-118">Paikkojen avulla käsitellään säilön alimoduulien asettelua ja tarkoitusta.</span><span class="sxs-lookup"><span data-stu-id="4d6e1-118">Slots are used to handle the layout and purpose of child modules in the container.</span></span> <span data-ttu-id="4d6e1-119">Seuraavassa on esimerkki perussivun säilömoduulista (ylimmän tason moduulista millä tahansa sivulla), joka määrittää useita tärkeitä paikkoja:</span><span class="sxs-lookup"><span data-stu-id="4d6e1-119">An example is a basic page container module (a top-level module for any page) that defines several important slots:</span></span>

- <span data-ttu-id="4d6e1-120">Ylätunnistepaikka</span><span class="sxs-lookup"><span data-stu-id="4d6e1-120">A header slot</span></span>
- <span data-ttu-id="4d6e1-121">Aliylätunnistepaikka</span><span class="sxs-lookup"><span data-stu-id="4d6e1-121">A sub-header slot</span></span>
- <span data-ttu-id="4d6e1-122">Pääpaikka</span><span class="sxs-lookup"><span data-stu-id="4d6e1-122">A main slot</span></span>
- <span data-ttu-id="4d6e1-123">Alatunnistepaikka</span><span class="sxs-lookup"><span data-stu-id="4d6e1-123">A footer slot</span></span>
- <span data-ttu-id="4d6e1-124">Alialatunnistepaikka</span><span class="sxs-lookup"><span data-stu-id="4d6e1-124">A sub-footer slot</span></span>

<span data-ttu-id="4d6e1-125">Moduulin kehittäjä määrittää nämä paikat. Hän määrittää myös, mitkä alimoduulit ja miten monta alimoduulia voidaan laittaa suoraan paikan sisään.</span><span class="sxs-lookup"><span data-stu-id="4d6e1-125">The module's developer defines these slots, and determines which child modules and how many child modules can be put directly inside it.</span></span> <span data-ttu-id="4d6e1-126">Esimerkiksi ylätunnistepaikka voi tukea vain yhtä **ylätunnistemoduuli**-tyyppiä, kun taas tekstiosapaikka voi tukea rajoittamatonta määrää moduulityyppejä (ei kutienkaan muita sivun säilömoduuleja).</span><span class="sxs-lookup"><span data-stu-id="4d6e1-126">For example, the header slot might support only one module of the **Header Module** type, whereas the body slot might support an unlimited number of modules of any type (except other page container modules).</span></span>

<span data-ttu-id="4d6e1-127">Sivun tekijöiden ei tarvitse tietää etukäteen muokkaustyökaluissa, mitkä moduulit voi asettaa kuhunkin paikkaan.</span><span class="sxs-lookup"><span data-stu-id="4d6e1-127">In the authoring tools, page authors don't have to know in advance which modules can and can't be put in each slot.</span></span> <span data-ttu-id="4d6e1-128">Kun sivun tekijät valitsevat paikan ja yrittävät sitten valita siihen lisättävän moduulin, he näkevät suodatetun näkymän moduulityypeistä, joita kyseinen paikka tukee.</span><span class="sxs-lookup"><span data-stu-id="4d6e1-128">When page authors select a slot and then try to select a module to add to it, they see a filtered view of module types that are supported for that slot.</span></span>

## <a name="content-modules"></a><span data-ttu-id="4d6e1-129">Sisältömoduulit</span><span class="sxs-lookup"><span data-stu-id="4d6e1-129">Content modules</span></span>

<span data-ttu-id="4d6e1-130">Sisältömoduulit sisältävät sisältö- ja mediaelementtejä, kuten tekstiä (esimerkiksi otsikoita, kappaleita ja linkkejä) tai resurssiviitteitä (esimerkiksi kuvia, videota ja PDF-tiedostoja).</span><span class="sxs-lookup"><span data-stu-id="4d6e1-130">Content modules contain content and media elements, such as text (for example, headlines, paragraphs, and links) or asset references (for example, images, video, and PDFs).</span></span> <span data-ttu-id="4d6e1-131">Tyypillisiä sisältömoduulin tyyppejä ovat sisältölohko-, tekstilohko- ja kampanjabannerimoduulit.</span><span class="sxs-lookup"><span data-stu-id="4d6e1-131">Typical content module types include content block, text block, and promo banner modules.</span></span> <span data-ttu-id="4d6e1-132">Nämä kolme moduulityyppiä voivat sisältää tekstiä tai mediaa. Ne eivät tarvitse alimoduuleja voidakseen näyttää sivulla asioita.</span><span class="sxs-lookup"><span data-stu-id="4d6e1-132">Modules of these three types can contain text or media, and they don't require any child modules to make something visible on a page.</span></span>

<span data-ttu-id="4d6e1-133">Suurin osa yleisistä päivittäisistä sivun- ja sisällöntuottamisaktiviteeteista liittyy sisältömoduuleihin. Tämä pääasiassa sen vuoksi, että nämä moduulit määrittävät pääsäilömoduuleissa hahmonnetun todellisen sisällön.</span><span class="sxs-lookup"><span data-stu-id="4d6e1-133">The majority of typical, day-to-day page and content authoring activities involve content modules, primarily because these modules define the actual content that is rendered in their parent container modules.</span></span> <span data-ttu-id="4d6e1-134">Käytettävissä on useita sisältömoduuleja. Nämä moduulit ovat yleensä viimeisiä sisäkkäisten moduulien sivuhierarkiaan lisättäviä osia.</span><span class="sxs-lookup"><span data-stu-id="4d6e1-134">Many content modules are available, and these modules are typically the last pieces that you will add to a page's hierarchy of nested modules.</span></span>

<span data-ttu-id="4d6e1-135">Seuraavassa kuvassa näkyy, kuinka moduulit ovat sisäkkäin pääsäilömoduulin paikoissa.</span><span class="sxs-lookup"><span data-stu-id="4d6e1-135">The following illustration shows how modules are nested inside parent container module slots.</span></span>

![Sisäkkäiset moduulit](../commerce/media/basic-module-nesting.png)

## <a name="add-or-remove-modules"></a><span data-ttu-id="4d6e1-137">Moduulien lisääminen tai poistaminen</span><span class="sxs-lookup"><span data-stu-id="4d6e1-137">Add or remove modules</span></span>

<span data-ttu-id="4d6e1-138">Seuraavissa ohjeissa kuvataan, miten moduuleja lisätään ja poistetaan.</span><span class="sxs-lookup"><span data-stu-id="4d6e1-138">The following procedures describe how to add and remove modules.</span></span>

### <a name="add-a-module"></a><span data-ttu-id="4d6e1-139">Moduulin lisääminen</span><span class="sxs-lookup"><span data-stu-id="4d6e1-139">Add a module</span></span>

<span data-ttu-id="4d6e1-140">Voit lisätä sivun moduulin paikkaan tai säilöön seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="4d6e1-140">To add a module to a slot or container on a page, follow these steps.</span></span>

1. <span data-ttu-id="4d6e1-141">Valitse vasemmalla olevasta jäsennysruudusta tai suoraan pääalustalla säilö tai paikka, johon alimoduuli voidaan lisätä.</span><span class="sxs-lookup"><span data-stu-id="4d6e1-141">In the outline pane on the left or directly in the main canvas, select a container or slot to which a child module can be added.</span></span>

    > [!NOTE]
    > <span data-ttu-id="4d6e1-142">Moduulin suunnittelija määrittää moduulityyppien luettelon, joka voidaan lisätä tiettyyn moduulipaikkaan.</span><span class="sxs-lookup"><span data-stu-id="4d6e1-142">The module designer defines the list of modules types that can be added to a specific module slot.</span></span> <span data-ttu-id="4d6e1-143">Mallien tekijät voivat tämän jälkeen tarkentaa sallittuja moduulivaihtoehtoja. Tämän avulla varmistetaan yhdenmukainen hakukoneoptimointi ja luotitehokkuus kaikilla sivuilla, jotka on luotu tietyn mallin avulla.</span><span class="sxs-lookup"><span data-stu-id="4d6e1-143">Template authors can then refine the allowed module options to help guarantee consistent search engine optimization (SEO) and authoring efficiency for all the pages that are built from a specific template.</span></span> <span data-ttu-id="4d6e1-144">Kun moduulia lisätään paikkaan, **Lisää moduuli** -valintaikkuna suodatetaan automaattisesti siten, että siinä näkyvät vain ne moduulit, joita valittu säilö tai paikka tukee.</span><span class="sxs-lookup"><span data-stu-id="4d6e1-144">When adding a module to a slot, the **Add Module** dialog box is automatically filtered so that it shows only modules that are supported in the selected container or slot.</span></span> <span data-ttu-id="4d6e1-145">Tämä sallittujen moduulien luettelo määräytyy sivun mallin tai säilömoduulin määrityksen mukaan.</span><span class="sxs-lookup"><span data-stu-id="4d6e1-145">This list of allowed modules is determined by the page's template or the container's module definition.</span></span>

1. <span data-ttu-id="4d6e1-146">Jos käytössä on jäsennysruutu, valitse kolme pistettä (**...**) moduulin nimen vierestä ja valitse sitten **Lisää moduuli**.</span><span class="sxs-lookup"><span data-stu-id="4d6e1-146">If using the outline pane, select the ellipsis (**...**) next to the module name, and then select **Add Module**.</span></span> <span data-ttu-id="4d6e1-147">Jos käytät ohjausobjekteja suoraan alustassa, valitse plusmerkki (**+**) tyhjässä paikassa tai parhaillaan valittuna olevan moduulin vieressä. Valitse sitten **Lisää moduuli**.</span><span class="sxs-lookup"><span data-stu-id="4d6e1-147">If using the controls directly within the canvas, select the plus symbol (**+**) in an empty slot or adjacent to the currently selected module, and then select **Add Module**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="4d6e1-148">Jos säilö tai paikka ei tue uusia alimoduuleja, **Lisää moduuli** -vaihtoehto ei ole käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="4d6e1-148">If a container or slot doesn't support new child modules, the **Add Module** option is unavailable.</span></span>

1. <span data-ttu-id="4d6e1-149">Valitse **Lisää moduuli** -valintaikkunassa sivulle lisättävä moduuli.</span><span class="sxs-lookup"><span data-stu-id="4d6e1-149">In the **Add Module** dialog box, select a module to add to your page.</span></span>

    > [!TIP]
    > <span data-ttu-id="4d6e1-150">Aloittelijan kannattaa käyttää **Sisältölohko**-moduulityyppiä.</span><span class="sxs-lookup"><span data-stu-id="4d6e1-150">**Content block** is a good module type for beginners to work with.</span></span>

1. <span data-ttu-id="4d6e1-151">Valitse **OK**, jos haluat lisätä valitun moduulin sivun valittuun säilöön tai paikkaan.</span><span class="sxs-lookup"><span data-stu-id="4d6e1-151">Select **OK** to add the selected module to the selected container or slot on your page.</span></span>

### <a name="remove-a-module"></a><span data-ttu-id="4d6e1-152">Moduulin poistaminen</span><span class="sxs-lookup"><span data-stu-id="4d6e1-152">Remove a module</span></span>

<span data-ttu-id="4d6e1-153">Voit poistaa sivun moduulin paikasta tai säilöstä seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="4d6e1-153">To remove a module from a slot or container on a page, follow these steps.</span></span>

1. <span data-ttu-id="4d6e1-154">Valitse vasemmanpuoleisessa jäsennysruudussa poistettavan moduulin nimen vieressä oleva kolmen pisteen painike (**...**) ja valitse sitten roskakorisymboli.</span><span class="sxs-lookup"><span data-stu-id="4d6e1-154">In the outline pane on the left, select the ellipsis (**...**) next to the name of the module to be removed, and then select the trash can symbol.</span></span> <span data-ttu-id="4d6e1-155">Vaihtoehtoisesti voit valita pääalustalle valitun moduulin työkalurivin roskakorisymbolin.</span><span class="sxs-lookup"><span data-stu-id="4d6e1-155">Alternately, in the main canvas you can select the trash can symbol on a selected module's toolbar.</span></span>
1. <span data-ttu-id="4d6e1-156">Kun sinua pyydetään vahvistamaan moduulin poistaminen, valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="4d6e1-156">When prompted to confirm that you want to remove the module, select **OK**.</span></span>

## <a name="move-a-module-to-a-new-position"></a><span data-ttu-id="4d6e1-157">Moduulin siirtäminen uuteen kohtaan</span><span class="sxs-lookup"><span data-stu-id="4d6e1-157">Move a module to a new position</span></span>

<span data-ttu-id="4d6e1-158">Voit siirtää moduulin uuteen kohtaan sivulla jollakin seuraavista tavoista.</span><span class="sxs-lookup"><span data-stu-id="4d6e1-158">To move a module to a new position within your page, use any of the following methods.</span></span>

### <a name="move-a-module-using-the-outline-pane"></a><span data-ttu-id="4d6e1-159">Moduulin siirtäminen jäsennysruudun avulla</span><span class="sxs-lookup"><span data-stu-id="4d6e1-159">Move a module using the outline pane</span></span>

<span data-ttu-id="4d6e1-160">Voit siirtää moduulin jäsennysruudun avulla noudattamalla seuraavia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="4d6e1-160">To move a module using the outline pane, follow these steps.</span></span>

1. <span data-ttu-id="4d6e1-161">Valitse ja pidä painettuna siirrettävää moduulia jäsennysruudussa. Vedä sitten moduuli uuteen kohtaan jäsennyksessä.</span><span class="sxs-lookup"><span data-stu-id="4d6e1-161">Select and hold the module you want to move in the outline pane, then drag the module to a new position in the outline.</span></span> <span data-ttu-id="4d6e1-162">Jäsennyksen ja alustan sininen viiva ilmaisee, mihin moduuli voidaan sijoittaa.</span><span class="sxs-lookup"><span data-stu-id="4d6e1-162">The blue line in the outline and on the canvas indicates where the module can be placed.</span></span>
1. <span data-ttu-id="4d6e1-163">Vapauta moduuli ja pudota se uuteen kohtaan.</span><span class="sxs-lookup"><span data-stu-id="4d6e1-163">Release the module to drop it into the new position.</span></span>

### <a name="move-a-module-directly-within-the-canvas"></a><span data-ttu-id="4d6e1-164">Moduulin siirtäminen suoraan alustaan</span><span class="sxs-lookup"><span data-stu-id="4d6e1-164">Move a module directly within the canvas</span></span>

<span data-ttu-id="4d6e1-165">Voit siirtää moduulin suoraan alustassa noudattamalla seuraavia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="4d6e1-165">To move a module directly within the canvas, follow these steps.</span></span>

1. <span data-ttu-id="4d6e1-166">Valitse alustassa siirrettävä moduuli.</span><span class="sxs-lookup"><span data-stu-id="4d6e1-166">Select the module you want to move in the canvas.</span></span> 
1. <span data-ttu-id="4d6e1-167">Valitse joko ylös- tai alaspäin osoittava nuolisymboli moduulin työkalurivillä. Vedä nuolta uuteen kohtaan sivulla.</span><span class="sxs-lookup"><span data-stu-id="4d6e1-167">Select either an upward or downward pointing arrow symbol in the module's toolbar, and then drag the arrow to a new position on the page.</span></span> <span data-ttu-id="4d6e1-168">Jäsennyksen ja kaavan sininen viiva ilmaisee, mihin moduuli voidaan sijoittaa.</span><span class="sxs-lookup"><span data-stu-id="4d6e1-168">The blue line in the canvas and outline indicates where the module can be placed.</span></span> <span data-ttu-id="4d6e1-169">Jos moduulia ei voi siirtää ylös tai alas, nuolisymboli näkyy harmaana.</span><span class="sxs-lookup"><span data-stu-id="4d6e1-169">If a module cannot be moved up or down, that arrow symbol will be grayed out.</span></span> 
1. <span data-ttu-id="4d6e1-170">Vapauta moduuli ja pudota se uuteen kohtaan.</span><span class="sxs-lookup"><span data-stu-id="4d6e1-170">Release the module to drop it into the new position.</span></span>

### <a name="move-a-module-using-the-ellipsis-menu"></a><span data-ttu-id="4d6e1-171">Moduulin siirtäminen kolmen pisteen valikon avulla</span><span class="sxs-lookup"><span data-stu-id="4d6e1-171">Move a module using the ellipsis menu</span></span>

<span data-ttu-id="4d6e1-172">Voit siirtää moduulin kolmen pisteen valikon avulla noudattamalla seuraavia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="4d6e1-172">To move a module using the ellipsis menu, follow these steps.</span></span>

1. <span data-ttu-id="4d6e1-173">Valitse moduuli jäsennyksestä tai alustasta.</span><span class="sxs-lookup"><span data-stu-id="4d6e1-173">Select a module in either the outline or the canvas.</span></span>
1. <span data-ttu-id="4d6e1-174">Valitse kolme pistettä (**...**) moduulin nimen vierestä jäsennysruudusta tai moduulin työkaluriviltä.</span><span class="sxs-lookup"><span data-stu-id="4d6e1-174">Select the ellipsis (**...**) next to the module's name in the outline pane, or in the module's toolbar in the canvas.</span></span>
1. <span data-ttu-id="4d6e1-175">Jos moduulia voi siirtää ylös ja alas säilössä tai paikassa, näkyvissä ovat **Siirrä ylös**- tai **Siirrä alas** -vaihtoehdot.</span><span class="sxs-lookup"><span data-stu-id="4d6e1-175">If the module can be moved up or down within the container or slot, you will see options for **Move up** or **Move down**.</span></span> <span data-ttu-id="4d6e1-176">Valitse haluttu siirtovaihtoehto, kun haluat siirtää moduulia ylös tai alas suhteessa sen sisaruksiin.</span><span class="sxs-lookup"><span data-stu-id="4d6e1-176">Select the desired move option to move the module up or down relative to its siblings.</span></span>

## <a name="configure-modules"></a><span data-ttu-id="4d6e1-177">Moduulien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="4d6e1-177">Configure modules</span></span>

<span data-ttu-id="4d6e1-178">Seuraavissa ohjeissa kuvataan, miten sisältö ja säilömoduulit määritetään.</span><span class="sxs-lookup"><span data-stu-id="4d6e1-178">The following procedures describe how to configure content and container modules.</span></span>

### <a name="configure-a-content-module"></a><span data-ttu-id="4d6e1-179">Sisältömoduulin määrittäminen</span><span class="sxs-lookup"><span data-stu-id="4d6e1-179">Configure a content module</span></span>

<span data-ttu-id="4d6e1-180">Voit määrittää sivun sisältömoduulin seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="4d6e1-180">To configure a content module on a page, follow these steps.</span></span>

1. <span data-ttu-id="4d6e1-181">Laajenna puuta vasemmalla olevassa jäsennysruudussa ja valitse mikä tahansa sisältömoduuli (esimerkiksi **Sisältölohko**).</span><span class="sxs-lookup"><span data-stu-id="4d6e1-181">In the outline pane on the left, expand the tree and select any content module (for example, **Content block**).</span></span> <span data-ttu-id="4d6e1-182">Vaihtoehtoisesti voit valita moduulin pääalustassa.</span><span class="sxs-lookup"><span data-stu-id="4d6e1-182">Alternately, you can select the module in the main canvas.</span></span>
1. <span data-ttu-id="4d6e1-183">Anna haluttujen moduulin ohjausobjektien ominaisuudet oikealla olevaan moduulin ominaisuuksien ruutuun.</span><span class="sxs-lookup"><span data-stu-id="4d6e1-183">In the module properties pane on the right, enter properties for any desired module controls.</span></span>
1. <span data-ttu-id="4d6e1-184">Valitse **Tallenna** komentopalkissa.</span><span class="sxs-lookup"><span data-stu-id="4d6e1-184">On the command bar, select **Save**.</span></span> <span data-ttu-id="4d6e1-185">Tämä päivittää myös esikatselualustan.</span><span class="sxs-lookup"><span data-stu-id="4d6e1-185">This will also refresh the preview canvas.</span></span>

### <a name="edit-module-text-properties"></a><span data-ttu-id="4d6e1-186">Moduulin tekstiominaisuuksien muokkaaminen</span><span class="sxs-lookup"><span data-stu-id="4d6e1-186">Edit module text properties</span></span>

<span data-ttu-id="4d6e1-187">Moduulin tekstiominaisuuksia, jotka eivät ole vain luku -tilassa, voi muokata suoraan alustassa.</span><span class="sxs-lookup"><span data-stu-id="4d6e1-187">Module text properties that are not read-only can be edited directly in the canvas.</span></span>

<span data-ttu-id="4d6e1-188">Voit muokata moduulin tekstiominaisuuksia noudattamalla seuraavia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="4d6e1-188">To edit module text properties, follow these steps.</span></span>

1. <span data-ttu-id="4d6e1-189">Valitse alustan tekstin ohjausobjekti ja sijoita kohdistin kohtaan, jossa haluat muokata tekstiä.</span><span class="sxs-lookup"><span data-stu-id="4d6e1-189">Select the text control in the canvas, then place your cursor where you wish to edit text.</span></span>
1. <span data-ttu-id="4d6e1-190">Anna tekstisisältö.</span><span class="sxs-lookup"><span data-stu-id="4d6e1-190">Enter your text content.</span></span>
1. <span data-ttu-id="4d6e1-191">Jatka muiden sisältöjen muokkaamista valitsemalla kohta tekstisisällön ulkopuolelta.</span><span class="sxs-lookup"><span data-stu-id="4d6e1-191">Select anywhere outside the text content to continue editing other content.</span></span>

### <a name="inline-image-selection"></a><span data-ttu-id="4d6e1-192">Sisäisen kuvan valitseminen</span><span class="sxs-lookup"><span data-stu-id="4d6e1-192">Inline image selection</span></span>

<span data-ttu-id="4d6e1-193">Moduulin kuvia, jotka eivät ole vain luku -tilassa, voi muuttaa suoraan alustassa.</span><span class="sxs-lookup"><span data-stu-id="4d6e1-193">Module images that are not read-only can be changed directly from the canvas.</span></span>

<span data-ttu-id="4d6e1-194">Voit valita sisältömoduulin uuden kuvan seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="4d6e1-194">To choose a new image for a content module, follow these steps.</span></span>

1. <span data-ttu-id="4d6e1-195">Kaksoisnapsauta kuvaa alustassa.</span><span class="sxs-lookup"><span data-stu-id="4d6e1-195">In the canvas, double-click the image.</span></span> <span data-ttu-id="4d6e1-196">Näkyviin tulee mediavalitsimen ikkuna.</span><span class="sxs-lookup"><span data-stu-id="4d6e1-196">This will bring up the media picker window.</span></span>
1. <span data-ttu-id="4d6e1-197">Etsi ja valitse uusi kuva, jota haluat käyttää, ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="4d6e1-197">Find and select a new image you want to use, and then select **OK**.</span></span> <span data-ttu-id="4d6e1-198">Uusi kuva hahmonnetaan nyt alustassa.</span><span class="sxs-lookup"><span data-stu-id="4d6e1-198">The new image is now rendered in the canvas.</span></span>

### <a name="configure-a-container-module"></a><span data-ttu-id="4d6e1-199">Konttimoduulin määrittäminen</span><span class="sxs-lookup"><span data-stu-id="4d6e1-199">Configure a container module</span></span>

<span data-ttu-id="4d6e1-200">Voit määrittää sivun säilömoduulin seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="4d6e1-200">To configure a container module on a page, follow these steps.</span></span>

1. <span data-ttu-id="4d6e1-201">Valitse sivulla oleva säilömoduuli (esimerkiksi karuselli- tai nestesäilömoduuli).</span><span class="sxs-lookup"><span data-stu-id="4d6e1-201">Select a container module on your page (for example, a carousel or fluid container module).</span></span>
1. <span data-ttu-id="4d6e1-202">Laajenna oikeanpuoleisessa ominaisuusruudussa sisäkkäiset ohjausobjektit valitsemalla ylätunnisteet ja määrittämällä vaaditut ohjausobjektin arvot.</span><span class="sxs-lookup"><span data-stu-id="4d6e1-202">In the properties pane on the right, expand the nested controls by selecting the headers, and set any required control values.</span></span>
1. <span data-ttu-id="4d6e1-203">Valitse vasemmanpuoleisessa jäsennysruudussa säilön tai jonkin sen sisällä olevan paikan nimen vieressä oleva kolmen pisteen painike ja valitse sitten **Lisää moduuliin**.</span><span class="sxs-lookup"><span data-stu-id="4d6e1-203">In the outline pane on the left, select the ellipsis button next to the name of either the container or any slots inside the container, and then select **Add Module**.</span></span> <span data-ttu-id="4d6e1-204">Lisää sitten alimoduulit valittuun säilöön.</span><span class="sxs-lookup"><span data-stu-id="4d6e1-204">Then, add child modules to the selected container.</span></span> <span data-ttu-id="4d6e1-205">Lisätietoja on tämän ohjeaiheen edellä olevassa osassa [Moduulin kanssa työskenteleminen](#add-a-module).</span><span class="sxs-lookup"><span data-stu-id="4d6e1-205">For more information, see the [Work with modules](#add-a-module) section earlier in this topic.</span></span>
1. <span data-ttu-id="4d6e1-206">Jos pääsäilössä on useita alimoduuleja sisaruksina, voit muuttaa niiden näyttöjärjestystä pääsäilössä.</span><span class="sxs-lookup"><span data-stu-id="4d6e1-206">If multiple child modules exist as siblings in a parent container, you can change their display order in the parent container.</span></span> <span data-ttu-id="4d6e1-207">Valitse moduulin kolmen pisteen painike ja käytä sitten ylä- ja alanuolipainikkeita.</span><span class="sxs-lookup"><span data-stu-id="4d6e1-207">Select the ellipsis button for a module, and then use the up arrow and down arrow buttons.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4d6e1-208">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="4d6e1-208">Additional resources</span></span>

[<span data-ttu-id="4d6e1-209">Mallit ja asettelut – yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="4d6e1-209">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="4d6e1-210">Mallien käyttö</span><span class="sxs-lookup"><span data-stu-id="4d6e1-210">Work with templates</span></span>](work-with-templates.md)

[<span data-ttu-id="4d6e1-211">Esimääritettyjen asettelujen käyttö</span><span class="sxs-lookup"><span data-stu-id="4d6e1-211">Work with preset layouts</span></span>](work-with-layouts.md)

[<span data-ttu-id="4d6e1-212">Katkelmien käyttäminen</span><span class="sxs-lookup"><span data-stu-id="4d6e1-212">Work with fragments</span></span>](work-with-fragments.md)

[<span data-ttu-id="4d6e1-213">Konttimoduulin lisääminen sivulle</span><span class="sxs-lookup"><span data-stu-id="4d6e1-213">Add a container module to a page</span></span>](add-container-module.md)

[<span data-ttu-id="4d6e1-214">Julkaisuryhmien kanssa työskenteleminen</span><span class="sxs-lookup"><span data-stu-id="4d6e1-214">Work with publish groups</span></span>](publish-groups.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]