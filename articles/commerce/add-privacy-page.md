---
title: Lisää tietosuojakäytäntösivu
description: Tässä ohjeaiheessa kerrotaan, miten tietosuojakäytäntösivu lisätään sivustollesi Microsoft Dynamics 365 Commerce -sovelluksessa.
author: v-chgri
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 12cd0358279684ce1d3050348c37209ba3d29140
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797524"
---
# <a name="add-a-privacy-policy-page"></a><span data-ttu-id="9987d-103">Lisää tietosuojakäytäntösivu</span><span class="sxs-lookup"><span data-stu-id="9987d-103">Add a privacy policy page</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="9987d-104">Tässä ohjeaiheessa kerrotaan, miten tietosuojakäytäntösivu lisätään sivustollesi Microsoft Dynamics 365 Commerce -sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="9987d-104">This topic describes how to add a privacy policy page to your site in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="9987d-105">Tietosuojan noudattaminen sisältää organisatorisia toimenpiteitä, jotka ilmoittavat sivuston käyttäjille, miten heidän tietojaan kerätään ja käsitellään.</span><span class="sxs-lookup"><span data-stu-id="9987d-105">Privacy compliance includes organizational measures that inform site users about how their data is collected and handled.</span></span> <span data-ttu-id="9987d-106">Käyttäjät voivat sitten päättää, miten he haluavat henkilötietojaan käsiteltävän, ja ryhtyä asianmukaisiin toimiin.</span><span class="sxs-lookup"><span data-stu-id="9987d-106">Users can then decide how they want their personal data to be handled and can take appropriate action.</span></span>

## <a name="review-the-microsoft-privacy-statement-in-dynamics-365-commerce"></a><span data-ttu-id="9987d-107">Tarkastele Microsoftin tietosuojatietoja Dynamics 365 Commercessa</span><span class="sxs-lookup"><span data-stu-id="9987d-107">Review the Microsoft privacy statement in Dynamics 365 Commerce</span></span>

<span data-ttu-id="9987d-108">Jos haluat tarkastella Microsoftin tietosuojalausuntoa, kun olet kirjautuneena Dynamics 365 Commercen sisällönluontityökaluihin, valitse oikeasta yläkulmasta **Ohje**-painike (**?**) ja valitse sitten **Tietosuoja ja evästeet**.</span><span class="sxs-lookup"><span data-stu-id="9987d-108">To review the Microsoft privacy statement while you're signed in to the Dynamics 365 Commerce authoring tools, select the **Help** button (**?**) in the upper-right corner, and then select **Privacy and cookies**.</span></span> <span data-ttu-id="9987d-109">Avataan uusi välilehti, jolla on linkki [Microsoftin tietosuojalausuntoon](https://privacy.microsoft.com/privacystatement).</span><span class="sxs-lookup"><span data-stu-id="9987d-109">A new tab is opened that has a link to the [Microsoft privacy statement](https://privacy.microsoft.com/privacystatement).</span></span>

## <a name="build-a-privacy-policy-page-for-your-site"></a><span data-ttu-id="9987d-110">Luo sivustoosi tietosuojakäytäntösivu</span><span class="sxs-lookup"><span data-stu-id="9987d-110">Build a privacy policy page for your site</span></span>

<span data-ttu-id="9987d-111">Dynamics 365 Commercesta löydät useita tapoja antaa sivustosi käyttäjille pääsy tietosuojakäytäntöihin.</span><span class="sxs-lookup"><span data-stu-id="9987d-111">In Dynamics 365 Commerce, there are several ways to give users of your site access to your privacy policy.</span></span> <span data-ttu-id="9987d-112">Tässä osassa kerrotaan, miten voit luoda tietosuojakäytäntösivun ja viitata sitten sivuun alatunnisteosan avulla.</span><span class="sxs-lookup"><span data-stu-id="9987d-112">This section shows how to build a privacy policy page and then reference the page by using a footer fragment.</span></span>

<span data-ttu-id="9987d-113">Seuraavassa on esimerkki siitä, miten voit luoda yleisen tietosuojakäytäntösivun Commerce-sivustolle.</span><span class="sxs-lookup"><span data-stu-id="9987d-113">The guidance that follows is an example that shows how to build a generic privacy policy page for a Commerce site.</span></span> <span data-ttu-id="9987d-114">Olet vastuussa siitä, että suunnittelet ja toteutat tietosuojakäytäntösivuratkaisun, joka vastaa parhaiten yrityksesi lakisääteisiä vaatimuksia.</span><span class="sxs-lookup"><span data-stu-id="9987d-114">You're responsible for designing and implementing a privacy policy page solution that best meets your company's legal requirements.</span></span>

<span data-ttu-id="9987d-115">Kun haluat aloittaa, siirry sisällönluontityökaluihin sivustossa, johon haluat luoda tietosuojakäytäntösivun.</span><span class="sxs-lookup"><span data-stu-id="9987d-115">To start, in the authoring tools, go to the site that you want to build a privacy policy page for.</span></span>

### <a name="create-a-template"></a><span data-ttu-id="9987d-116">Luo malli</span><span class="sxs-lookup"><span data-stu-id="9987d-116">Create a template</span></span>

> [!NOTE]
> <span data-ttu-id="9987d-117">Jos tietosuojakäytäntösivulla käytettävä malli on jo luotu, siirry eteenpäin [Muodosta tietosuojakäytäntösivu](#build-a-privacy-policy-page) -osioon.</span><span class="sxs-lookup"><span data-stu-id="9987d-117">If a template that can be used for the privacy policy page has already been created, skip ahead to the [Build a privacy policy page](#build-a-privacy-policy-page) section.</span></span>

<span data-ttu-id="9987d-118">Voit luoda mallin seuraavien vaiheiden avulla.</span><span class="sxs-lookup"><span data-stu-id="9987d-118">To create a template, follow these steps.</span></span>

1. <span data-ttu-id="9987d-119">Siirry kohtaan **Mallit** ja luo sivumalli valitsemalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="9987d-119">Go to **Templates**, and then select **New** to create a page template.</span></span>
1. <span data-ttu-id="9987d-120">Kirjoita **Uusi malli** -valintaikkunan **Mallin nimi** -kohtaan **Mainosnauhan malli** ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="9987d-120">In the **New Template** dialog box, under **Template Name**, enter **Promo banner template**, and then select **OK**.</span></span>
1. <span data-ttu-id="9987d-121">Lisää tarvittavat moduulit malliin vaadittavien sivupaikkojen kohdalle.</span><span class="sxs-lookup"><span data-stu-id="9987d-121">In the template, add any required modules to the required page slots.</span></span> <span data-ttu-id="9987d-122">Jos haluat ohjeita, vie hiiri punaisen huutomerkin päälle.</span><span class="sxs-lookup"><span data-stu-id="9987d-122">For guidance, hover over the red exclamation marks.</span></span> <span data-ttu-id="9987d-123">(Esimerkiksi **HTML-head-paikka** saattaa vaatia **ulkoisen oletuskomentosarjamoduulin**.)</span><span class="sxs-lookup"><span data-stu-id="9987d-123">(For example, the **HTML Head** slot might require a **Default External Script** module.)</span></span>
1. <span data-ttu-id="9987d-124">Lisää **Tekstipaikkaan** **Oletussivumoduuli**.</span><span class="sxs-lookup"><span data-stu-id="9987d-124">In the **Body** slot, add a **Default Page** module.</span></span>
1. <span data-ttu-id="9987d-125">Lisää **Sisällöntäyteinen lohkomoduuli** **Oletussivun** **Pääpaikkaan**.</span><span class="sxs-lookup"><span data-stu-id="9987d-125">In the **Default Page** module, in the **Main** slot, add a **Content Rich Block** module.</span></span>
1. <span data-ttu-id="9987d-126">Lisää **Sisällöntäyteiseen lohkomoduuliin** **Sisällöntäyteinen lohkonimikemoduuli**.</span><span class="sxs-lookup"><span data-stu-id="9987d-126">In the **Content Rich Block** module, add a **Content rich block item** module.</span></span>
1. <span data-ttu-id="9987d-127">Valitse **Tallenna**, valitse **Viimeistele muokkaus** tarkistaaksesi mallin, ja julkaise se valitsemalla **Julkaise**.</span><span class="sxs-lookup"><span data-stu-id="9987d-127">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>

### <a name="build-a-privacy-policy-page"></a><span data-ttu-id="9987d-128">Luo tietosuojakäytäntösivu</span><span class="sxs-lookup"><span data-stu-id="9987d-128">Build a privacy policy page</span></span>

<span data-ttu-id="9987d-129">Voit luoda tietosuojakäytäntösivun noudattamalla seuraavia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="9987d-129">To build a privacy policy page, follow these steps.</span></span>

1. <span data-ttu-id="9987d-130">Siirry kohtaan **Sivut** ja sitten **Uusi** luodaksesi uuden sivun.</span><span class="sxs-lookup"><span data-stu-id="9987d-130">Go to **Pages**, and then select **New** to create a page.</span></span>
1. <span data-ttu-id="9987d-131">Valitse **Valitse malli** -valintaikkunan tietosuojakäytäntösivun malli.</span><span class="sxs-lookup"><span data-stu-id="9987d-131">In the **Choose a template** dialog box, select the template for the privacy policy page.</span></span>
1. <span data-ttu-id="9987d-132">Kirjoita sivun nimi ja URL-osoite ja valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="9987d-132">Enter a page name and page URL, and then select **OK**.</span></span> 
1. <span data-ttu-id="9987d-133">Lisää **Sisällöntäyteinen lohkomoduuli** sivun **Pääpaikkaan**.</span><span class="sxs-lookup"><span data-stu-id="9987d-133">In the **Main** slot of the page, add a **Content Rich Block** module.</span></span>
1. <span data-ttu-id="9987d-134">Lisää **Sisällöntäyteiseen lohkomoduuliin** **Sisällöntäyteinen lohkonimikemoduuli**.</span><span class="sxs-lookup"><span data-stu-id="9987d-134">In the **Content Rich Block** module, add a **Content rich block item** module.</span></span>
1. <span data-ttu-id="9987d-135">Valitse **Sisällön Rich Block** -moduulin Ominaisuudet-ruudusta **Lisää tietolähde** ja valitse sitten **Rich Text -sisältö**.</span><span class="sxs-lookup"><span data-stu-id="9987d-135">In the properties pane for the **Content Rich Block** module, select **Add Data Source**, and then select **Rich Text Content**.</span></span>
1. <span data-ttu-id="9987d-136">Kirjoita RTF-editorissa tietosuojakäytäntösivun sisältö.</span><span class="sxs-lookup"><span data-stu-id="9987d-136">In the rich text editor, enter the content for the privacy policy page.</span></span> <span data-ttu-id="9987d-137">Laajenna Rich Text -editori tarvittaessa koko näytön tilaan.</span><span class="sxs-lookup"><span data-stu-id="9987d-137">Expand the rich text editor to full-screen mode as you require.</span></span>
1. <span data-ttu-id="9987d-138">Kun olet lopettanut sisällön kirjoittamisen, esikatsele sivua verkkoselaimessa valitsemalla **Esikatselu**.</span><span class="sxs-lookup"><span data-stu-id="9987d-138">When you've finished entering content, select **Preview** to preview the page in the web browser.</span></span>
1. <span data-ttu-id="9987d-139">Täydennä kaikki sivun ja moduulin ominaisuuksien jäljellä olevat lisäykset.</span><span class="sxs-lookup"><span data-stu-id="9987d-139">Complete any remaining additions to the page and module properties.</span></span>
1. <span data-ttu-id="9987d-140">Valitse **Tallenna**, valitse **Viimeistele muokkaus** tarkistaaksesi sivun, ja julkaise se valitsemalla **Julkaise**.</span><span class="sxs-lookup"><span data-stu-id="9987d-140">Select **Save**, select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="9987d-141">Voit julkaista tietosuojakäytäntösivun URL-osoitteen seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="9987d-141">To publish the URL for the privacy policy page, follow these steps.</span></span>

1. <span data-ttu-id="9987d-142">Siirry **URL-osoitteisiin** ja valitse tietosuojakäytäntösivun URL-osoite.</span><span class="sxs-lookup"><span data-stu-id="9987d-142">Go to **URLs**, and select the URL for the privacy policy page.</span></span>
1. <span data-ttu-id="9987d-143">Julkaise valittu URL-osoite valitsemalla **Julkaise**.</span><span class="sxs-lookup"><span data-stu-id="9987d-143">Select **Publish** to publish the selected URL.</span></span>

### <a name="create-a-link-to-the-privacy-policy-page-in-a-footer"></a><span data-ttu-id="9987d-144">Luo linkki tietosuojakäytäntösivun alatunnisteeseen</span><span class="sxs-lookup"><span data-stu-id="9987d-144">Create a link to the privacy policy page in a footer</span></span>

<span data-ttu-id="9987d-145">Voit lisätä linkin tietosuojakäytäntösivun osaan.</span><span class="sxs-lookup"><span data-stu-id="9987d-145">You can add a link to the privacy policy page to a fragment.</span></span> <span data-ttu-id="9987d-146">Tällä tavoin voit jakaa linkin ja päivittää sen useille sivustosivuille viittaamalla osaan.</span><span class="sxs-lookup"><span data-stu-id="9987d-146">In this way, you can share the link and update it across multiple site pages by referencing the fragment.</span></span> <span data-ttu-id="9987d-147">Tässä esimerkissä kerrotaan, kuinka voit lisätä linkin tietosuojakäytäntösivulle alatunnisteen osaan.</span><span class="sxs-lookup"><span data-stu-id="9987d-147">This example shows how to add a link to the privacy policy page to a footer fragment.</span></span>

<span data-ttu-id="9987d-148">Voit lisätä linkin alatunnisteosaan seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="9987d-148">To add a link to a footer fragment, follow these steps.</span></span>

1. <span data-ttu-id="9987d-149">Siirry kohtaan **Osat** ja **Uusi** luodaksesi sivun osan.</span><span class="sxs-lookup"><span data-stu-id="9987d-149">Go to **Fragments**, and then select **New** to create a page fragment.</span></span>
1. <span data-ttu-id="9987d-150">Valitse **Uusi osa** -valintaikkunassa **Alatunniste**-moduuli.</span><span class="sxs-lookup"><span data-stu-id="9987d-150">In the **New fragment** dialog box, select the **Footer** module.</span></span>
1. <span data-ttu-id="9987d-151">Kirjoita **Osan nimi** -kohtaan osan nimi ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="9987d-151">Under **Fragment name**, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="9987d-152">Lisää **Alatunnisteluokka**-paikkaan **Alatunnisteen nimike** -moduuli.</span><span class="sxs-lookup"><span data-stu-id="9987d-152">In the **Footer category** slot, add a **Footer item** module.</span></span>
1. <span data-ttu-id="9987d-153">Valitse oikeanpuoleisessa ominaisuusruudussa **Linkitä teksti**.</span><span class="sxs-lookup"><span data-stu-id="9987d-153">In the properties pane on the right, select **Link text**.</span></span>
1. <span data-ttu-id="9987d-154">Kirjoita **Linkitä teksti** -valintaikkunassa tietosuojakäytäntösivun linkkiteksti ja linkkikohde ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="9987d-154">In the **Link text** dialog box, enter the link text and link target of the privacy policy page, and then click **OK**.</span></span>
1. <span data-ttu-id="9987d-155">Jos haluat saada tietosuojakäytäntösivun URL-osoitteen, siirry kohtaan **Sivut**, siirry tietosuojakäytäntösivulle ja kopioi URL-osoite Ominaisuudet-ruudusta.</span><span class="sxs-lookup"><span data-stu-id="9987d-155">To get the URL of the privacy policy page, go to **Pages**, go to the privacy policy page, and copy the URL from the properties pane.</span></span>
1. <span data-ttu-id="9987d-156">Valitse **Tallenna**, valitse **Viimeistele muokkaus** tarkistaaksesi osan, ja julkaise se valitsemalla **Julkaise**.</span><span class="sxs-lookup"><span data-stu-id="9987d-156">Select **Save**, select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="9987d-157">Esikatsele osa ja testaa linkki tietosuojakäytäntösivulle.</span><span class="sxs-lookup"><span data-stu-id="9987d-157">Preview the fragment, and test the link to the privacy policy page.</span></span>

<span data-ttu-id="9987d-158">Osaan voidaan nyt viitata muiden sivuston sivujen mallissa.</span><span class="sxs-lookup"><span data-stu-id="9987d-158">The fragment can now be referenced in the template for other site pages.</span></span> <span data-ttu-id="9987d-159">Kun tähän osaan viitataan mallin **Alatunniste**-moduulissa, linkkiviittaus näkyy kaikilla sivuilla, jotka on rakennettu kyseisen mallin avulla.</span><span class="sxs-lookup"><span data-stu-id="9987d-159">When this fragment is referenced in the **Footer** module of a template, the link reference will appear on any pages that are built by using that template.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9987d-160">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="9987d-160">Additional resources</span></span>

[<span data-ttu-id="9987d-161">Yhteensopivuuden yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="9987d-161">Compliance overview</span></span>](compliance-overview.md)

[<span data-ttu-id="9987d-162">Helppokäyttöisyyden toiminnot ja ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="9987d-162">Accessibility features and capabilities</span></span>](accessibility.md)

[<span data-ttu-id="9987d-163">Evästeen yhteensopivuus</span><span class="sxs-lookup"><span data-stu-id="9987d-163">Cookie compliance</span></span>](cookie-compliance.md)

[<span data-ttu-id="9987d-164">Seurattuihin sisällönmuutoksiin liittyvien käyttäjätunnusten korvaaminen</span><span class="sxs-lookup"><span data-stu-id="9987d-164">Replace user IDs associated with tracked content changes</span></span>](replace-IDs-tracked-changes.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
