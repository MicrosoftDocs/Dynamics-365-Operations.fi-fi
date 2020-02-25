---
title: Lisää tietosuojakäytäntösivu
description: Tässä ohjeaiheessa kerrotaan, miten tietosuojakäytäntösivu lisätään sivustollesi Microsoft Dynamics 365 Commerce -sovelluksessa.
author: v-chgri
manager: annbe
ms.date: 01/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: ee9a68f46c91299065732e5f65479906f9e06079
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/01/2020
ms.locfileid: "3001320"
---
# <a name="add-a-privacy-policy-page"></a><span data-ttu-id="896f3-103">Lisää tietosuojakäytäntösivu</span><span class="sxs-lookup"><span data-stu-id="896f3-103">Add a privacy policy page</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="896f3-104">Tässä ohjeaiheessa kerrotaan, miten tietosuojakäytäntösivu lisätään sivustollesi Microsoft Dynamics 365 Commerce -sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="896f3-104">This topic describes how to add a privacy policy page to your site in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="896f3-105">Yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="896f3-105">Overview</span></span>

<span data-ttu-id="896f3-106">Tietosuojan noudattaminen sisältää organisatorisia toimenpiteitä, jotka ilmoittavat sivuston käyttäjille, miten heidän tietojaan kerätään ja käsitellään.</span><span class="sxs-lookup"><span data-stu-id="896f3-106">Privacy compliance includes organizational measures that inform site users about how their data is collected and handled.</span></span> <span data-ttu-id="896f3-107">Käyttäjät voivat sitten päättää, miten he haluavat henkilötietojaan käsiteltävän, ja ryhtyä asianmukaisiin toimiin.</span><span class="sxs-lookup"><span data-stu-id="896f3-107">Users can then decide how they want their personal data to be handled and can take appropriate action.</span></span>

## <a name="review-the-microsoft-privacy-statement-in-dynamics-365-commerce"></a><span data-ttu-id="896f3-108">Tarkastele Microsoftin tietosuojatietoja Dynamics 365 Commercessa</span><span class="sxs-lookup"><span data-stu-id="896f3-108">Review the Microsoft privacy statement in Dynamics 365 Commerce</span></span>

<span data-ttu-id="896f3-109">Jos haluat tarkastella Microsoftin tietosuojalausuntoa, kun olet kirjautuneena Dynamics 365 Commercen sisällönluontityökaluihin, valitse oikeasta yläkulmasta **Ohje**-painike (**?**) ja valitse sitten **Tietosuoja ja evästeet**.</span><span class="sxs-lookup"><span data-stu-id="896f3-109">To review the Microsoft privacy statement while you're signed in to the Dynamics 365 Commerce authoring tools, select the **Help** button (**?**) in the upper-right corner, and then select **Privacy and cookies**.</span></span> <span data-ttu-id="896f3-110">Avataan uusi välilehti, jolla on linkki [Microsoftin tietosuojalausuntoon](https://privacy.microsoft.com/privacystatement).</span><span class="sxs-lookup"><span data-stu-id="896f3-110">A new tab is opened that has a link to the [Microsoft privacy statement](https://privacy.microsoft.com/privacystatement).</span></span>

## <a name="build-a-privacy-policy-page-for-your-site"></a><span data-ttu-id="896f3-111">Luo sivustoosi tietosuojakäytäntösivu</span><span class="sxs-lookup"><span data-stu-id="896f3-111">Build a privacy policy page for your site</span></span>

<span data-ttu-id="896f3-112">Dynamics 365 Commercesta löydät useita tapoja antaa sivustosi käyttäjille pääsy tietosuojakäytäntöihin.</span><span class="sxs-lookup"><span data-stu-id="896f3-112">In Dynamics 365 Commerce, there are several ways to give users of your site access to your privacy policy.</span></span> <span data-ttu-id="896f3-113">Tässä osassa kerrotaan, miten voit luoda tietosuojakäytäntösivun ja viitata sitten sivuun alatunnisteosan avulla.</span><span class="sxs-lookup"><span data-stu-id="896f3-113">This section shows how to build a privacy policy page and then reference the page by using a footer fragment.</span></span>

<span data-ttu-id="896f3-114">Seuraavassa on esimerkki siitä, miten voit luoda yleisen tietosuojakäytäntösivun Commerce-sivustolle.</span><span class="sxs-lookup"><span data-stu-id="896f3-114">The guidance that follows is an example that shows how to build a generic privacy policy page for a Commerce site.</span></span> <span data-ttu-id="896f3-115">Olet vastuussa siitä, että suunnittelet ja toteutat tietosuojakäytäntösivuratkaisun, joka vastaa parhaiten yrityksesi lakisääteisiä vaatimuksia.</span><span class="sxs-lookup"><span data-stu-id="896f3-115">You're responsible for designing and implementing a privacy policy page solution that best meets your company's legal requirements.</span></span>

<span data-ttu-id="896f3-116">Kun haluat aloittaa, siirry sisällönluontityökaluihin sivustossa, johon haluat luoda tietosuojakäytäntösivun.</span><span class="sxs-lookup"><span data-stu-id="896f3-116">To start, in the authoring tools, go to the site that you want to build a privacy policy page for.</span></span>

### <a name="create-a-template"></a><span data-ttu-id="896f3-117">Luo malli</span><span class="sxs-lookup"><span data-stu-id="896f3-117">Create a template</span></span>

> [!NOTE]
> <span data-ttu-id="896f3-118">Jos tietosuojakäytäntösivulla käytettävä malli on jo luotu, siirry eteenpäin [Muodosta tietosuojakäytäntösivu](#build-a-privacy-policy-page) -osioon.</span><span class="sxs-lookup"><span data-stu-id="896f3-118">If a template that can be used for the privacy policy page has already been created, skip ahead to the [Build a privacy policy page](#build-a-privacy-policy-page) section.</span></span>

<span data-ttu-id="896f3-119">Voit luoda mallin seuraavien vaiheiden avulla.</span><span class="sxs-lookup"><span data-stu-id="896f3-119">To create a template, follow these steps.</span></span>

1. <span data-ttu-id="896f3-120">Siirry kohtaan **Mallit \> Uusi malli**.</span><span class="sxs-lookup"><span data-stu-id="896f3-120">Go to **Templates \> New Template**.</span></span>
1. <span data-ttu-id="896f3-121">Kirjoita mallin nimi ja valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="896f3-121">Enter the template name, and then select **OK**.</span></span>
1. <span data-ttu-id="896f3-122">Lisää tarvittavat moduulit malliin vaadittavien sivupaikkojen kohdalle.</span><span class="sxs-lookup"><span data-stu-id="896f3-122">In the template, add any required modules to the required page slots.</span></span> <span data-ttu-id="896f3-123">Jos haluat ohjeita, vie hiiri punaisen huutomerkin päälle.</span><span class="sxs-lookup"><span data-stu-id="896f3-123">For guidance, hover over the red exclamation marks.</span></span>

    <span data-ttu-id="896f3-124">Esimerkiksi **HTML-head-paikka** saattaa vaatia **ulkoisen oletuskomentosarjamoduulin**.</span><span class="sxs-lookup"><span data-stu-id="896f3-124">For example, the **HTML Head** slot might require a **Default External Script** module.</span></span>

1. <span data-ttu-id="896f3-125">Lisää **Tekstipaikkaan** **Oletussivumoduuli**.</span><span class="sxs-lookup"><span data-stu-id="896f3-125">In the **Body** slot, add a **Default Page** module.</span></span>
1. <span data-ttu-id="896f3-126">Lisää **Sisällöntäyteinen lohkomoduuli** **Oletussivun** **Pääpaikkaan**.</span><span class="sxs-lookup"><span data-stu-id="896f3-126">In the **Default Page** module, in the **Main** slot, add a **Content Rich Block** module.</span></span>
1. <span data-ttu-id="896f3-127">Lisää **Sisällöntäyteiseen lohkomoduuliin** **Sisällöntäyteinen lohkonimikemoduuli**.</span><span class="sxs-lookup"><span data-stu-id="896f3-127">In the **Content Rich Block** module, add a **Content rich block item** module.</span></span>
1. <span data-ttu-id="896f3-128">Kirjaa malli sisään ja julkaise se.</span><span class="sxs-lookup"><span data-stu-id="896f3-128">Check the template in, and publish it.</span></span>

### <a name="build-a-privacy-policy-page"></a><span data-ttu-id="896f3-129">Luo tietosuojakäytäntösivu</span><span class="sxs-lookup"><span data-stu-id="896f3-129">Build a privacy policy page</span></span>

<span data-ttu-id="896f3-130">Voit luoda tietosuojakäytäntösivun noudattamalla seuraavia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="896f3-130">To build a privacy policy page, follow these steps.</span></span>

1. <span data-ttu-id="896f3-131">Siirry kohtaan **Sivut \> Uusi sivu**.</span><span class="sxs-lookup"><span data-stu-id="896f3-131">Go to **Pages \> New Page**.</span></span>
1. <span data-ttu-id="896f3-132">Valitse tietosuojakäytäntösivun malli.</span><span class="sxs-lookup"><span data-stu-id="896f3-132">Select the template for the privacy policy page.</span></span>
1. <span data-ttu-id="896f3-133">Kirjoita sivun nimi ja URL-osoite ja valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="896f3-133">Enter a page name and URL, and then select **OK**.</span></span> 
1. <span data-ttu-id="896f3-134">Lisää **Sisällöntäyteinen lohkomoduuli** sivun **Pääpaikkaan**.</span><span class="sxs-lookup"><span data-stu-id="896f3-134">In the **Main** slot of the page, add a **Content Rich Block** module.</span></span>
1. <span data-ttu-id="896f3-135">Lisää **Sisällöntäyteiseen lohkomoduuliin** **Sisällöntäyteinen lohkonimikemoduuli**.</span><span class="sxs-lookup"><span data-stu-id="896f3-135">In the **Content Rich Block** module, add a **Content rich block item** module.</span></span>
1. <span data-ttu-id="896f3-136">Valitse **Sisällön Rich Block** -moduulin Ominaisuudet-ruudusta **Lisää tietolähde** ja valitse sitten **Rich Text -sisältö**.</span><span class="sxs-lookup"><span data-stu-id="896f3-136">In the properties pane for the **Content Rich Block** module, select **Add Data Source**, and then select **Rich Text Content**.</span></span>
1. <span data-ttu-id="896f3-137">Kirjoita RTF-editorissa tietosuojakäytäntösivun sisältö.</span><span class="sxs-lookup"><span data-stu-id="896f3-137">In the rich text editor, enter the content for the privacy policy page.</span></span> <span data-ttu-id="896f3-138">Laajenna Rich Text -editori tarvittaessa koko näytön tilaan.</span><span class="sxs-lookup"><span data-stu-id="896f3-138">Expand the rich text editor to full-screen mode as you require.</span></span>
1. <span data-ttu-id="896f3-139">Kun olet lopettanut sisällön kirjoittamisen, esikatsele sivua verkkoselaimessa valitsemalla **Esikatselu**.</span><span class="sxs-lookup"><span data-stu-id="896f3-139">When you've finished entering content, select **Preview** to preview the page in the web browser.</span></span>
1. <span data-ttu-id="896f3-140">Täydennä kaikki sivun ja moduulin ominaisuuksien jäljellä olevat lisäykset.</span><span class="sxs-lookup"><span data-stu-id="896f3-140">Complete any remaining additions to the page and module properties.</span></span>
1. <span data-ttu-id="896f3-141">Kirjaa tietosuojakäytäntösivu sisään ja julkaise se.</span><span class="sxs-lookup"><span data-stu-id="896f3-141">Check the privacy policy page in, and publish it.</span></span>

<span data-ttu-id="896f3-142">Voit julkaista tietosuojakäytäntösivun URL-osoitteen seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="896f3-142">To publish the URL for the privacy policy page, follow these steps.</span></span>

1. <span data-ttu-id="896f3-143">Siirry **URL-osoitteisiin** ja valitse tietosuojakäytäntösivun URL-osoite.</span><span class="sxs-lookup"><span data-stu-id="896f3-143">Go to **URLs**, and select the URL for the privacy policy page.</span></span>
1. <span data-ttu-id="896f3-144">Julkaise valitut URL-osoitteet.</span><span class="sxs-lookup"><span data-stu-id="896f3-144">Publish the selected URL.</span></span>

### <a name="create-a-link-to-the-privacy-policy-page-in-a-footer"></a><span data-ttu-id="896f3-145">Luo linkki tietosuojakäytäntösivun alatunnisteeseen</span><span class="sxs-lookup"><span data-stu-id="896f3-145">Create a link to the privacy policy page in a footer</span></span>

<span data-ttu-id="896f3-146">Voit lisätä linkin tietosuojakäytäntösivun osaan.</span><span class="sxs-lookup"><span data-stu-id="896f3-146">You can add a link to the privacy policy page to a fragment.</span></span> <span data-ttu-id="896f3-147">Tällä tavoin voit jakaa linkin ja päivittää sen useille sivustosivuille viittaamalla osaan.</span><span class="sxs-lookup"><span data-stu-id="896f3-147">In this way, you can share the link and update it across multiple site pages by referencing the fragment.</span></span> <span data-ttu-id="896f3-148">Tässä esimerkissä kerrotaan, kuinka voit lisätä linkin tietosuojakäytäntösivulle alatunnisteen osaan.</span><span class="sxs-lookup"><span data-stu-id="896f3-148">This example shows how to add a link to the privacy policy page to a footer fragment.</span></span>

<span data-ttu-id="896f3-149">Voit lisätä linkin alatunnisteosaan seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="896f3-149">To add a link to a footer fragment, follow these steps.</span></span>

1. <span data-ttu-id="896f3-150">Siirry kohtaan **Sivun osat \> Uusi sivun osa**.</span><span class="sxs-lookup"><span data-stu-id="896f3-150">Go to **Page Fragments \> New Page Fragment**.</span></span>
1. <span data-ttu-id="896f3-151">Valitse **Alatunniste**-moduuli ja kirjoita sitten nimi **Sivun osan nimi** -kenttään.</span><span class="sxs-lookup"><span data-stu-id="896f3-151">Select the **Footer** module, and then enter a name in the **Page Fragment Name** field.</span></span>
1. <span data-ttu-id="896f3-152">Lisää **Alatunnisteluokka**-paikkaan **Alatunnisteen nimike** -moduuli.</span><span class="sxs-lookup"><span data-stu-id="896f3-152">In the **Footer category** slot, add a **Footer item** module.</span></span>
1. <span data-ttu-id="896f3-153">Valitse oikeanpuoleisessa ominaisuusruudussa **Linkitä teksti**.</span><span class="sxs-lookup"><span data-stu-id="896f3-153">In the properties pane on the right, select **Link text**.</span></span>
1. <span data-ttu-id="896f3-154">Kirjoita **Linkitä teksti** -valintaikkunassa tietosuojakäytäntösivun linkkiteksti ja linkkikohde ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="896f3-154">In the **Link text** dialog box, enter the link text and link target of the privacy policy page, and then click **OK**.</span></span>

    <span data-ttu-id="896f3-155">Jos haluat saada tietosuojakäytäntösivun URL-osoitteen, siirry kohtaan **Sivut**, siirry tietosuojakäytäntösivulle ja kopioi URL-osoite Ominaisuudet-ruudusta.</span><span class="sxs-lookup"><span data-stu-id="896f3-155">To get the URL of the privacy policy page, go to **Pages**, go to the privacy policy page, and copy the URL from the properties pane.</span></span>

1. <span data-ttu-id="896f3-156">Tallenna osa, kirjaa se sisään ja julkaise se.</span><span class="sxs-lookup"><span data-stu-id="896f3-156">Save the fragment, check it in, and publish it.</span></span>
1. <span data-ttu-id="896f3-157">Esikatsele osa ja testaa linkki tietosuojakäytäntösivulle.</span><span class="sxs-lookup"><span data-stu-id="896f3-157">Preview the fragment, and test the link to the privacy policy page.</span></span>

<span data-ttu-id="896f3-158">Osaan voidaan nyt viitata muiden sivuston sivujen mallissa.</span><span class="sxs-lookup"><span data-stu-id="896f3-158">The fragment can now be referenced in the template for other site pages.</span></span> <span data-ttu-id="896f3-159">Kun tähän osaan viitataan mallin **Alatunniste**-moduulissa, linkkiviittaus näkyy kaikilla sivuilla, jotka on rakennettu kyseisen mallin avulla.</span><span class="sxs-lookup"><span data-stu-id="896f3-159">When this fragment is referenced in the **Footer** module of a template, the link reference will appear on any pages that are built by using that template.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="896f3-160">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="896f3-160">Additional resources</span></span>

[<span data-ttu-id="896f3-161">Yhteensopivuuden yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="896f3-161">Compliance overview</span></span>](compliance-overview.md)

[<span data-ttu-id="896f3-162">Helppokäyttöisyyden toiminnot ja ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="896f3-162">Accessibility features and capabilities</span></span>](accessibility.md)

[<span data-ttu-id="896f3-163">Evästeen yhteensopivuus</span><span class="sxs-lookup"><span data-stu-id="896f3-163">Cookie compliance</span></span>](cookie-compliance.md)
