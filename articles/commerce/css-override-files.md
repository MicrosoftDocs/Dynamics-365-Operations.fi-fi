---
title: Työskentely CSS-korvaustiedostojen kanssa
description: Tässä ohjeaiheessa kerrotaan, miksi, milloin ja miten CSS-tyylisivuja (CSS) käytetään ohittamaan tiedostot Microsoft Dynamics 365 Commercessa.
author: phinneyridge
manager: annbe
ms.date: 05/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-12-12
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 41fb0be51f7af25faba1b860319aea84ae7a8b56
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5207796"
---
# <a name="work-with-css-override-files"></a><span data-ttu-id="57f6f-103">Työskentely CSS-korvaustiedostojen kanssa</span><span class="sxs-lookup"><span data-stu-id="57f6f-103">Work with CSS override files</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="57f6f-104">Tässä ohjeaiheessa kerrotaan, miksi, milloin ja miten CSS-tyylisivuja (CSS) käytetään ohittamaan tiedostot Microsoft Dynamics 365 Commercessa.</span><span class="sxs-lookup"><span data-stu-id="57f6f-104">This topic describes why, when, and how to use Cascading Style Sheets (CSS) override files in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="57f6f-105">Yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="57f6f-105">Overview</span></span>

<span data-ttu-id="57f6f-106">Pysyviä sivustotyylejä tulisi yleensä käsitellä sivuston teemalla.</span><span class="sxs-lookup"><span data-stu-id="57f6f-106">Permanent site styles should usually be handled through a site's theme.</span></span> <span data-ttu-id="57f6f-107">Teemat sisältävät perus-CSS- ja tyyliasetuksia mille tahansa sivustosi sivulla oleville moduuleille.</span><span class="sxs-lookup"><span data-stu-id="57f6f-107">Themes provide the foundational CSS and style settings for the modules on any page of your site.</span></span> <span data-ttu-id="57f6f-108">Teemat luodaan käyttämällä Dynamics 365 Commerce online Software Development Kit (SDK) -pakettia, ja ne otetaan käyttöön sivustoillesi Microsoft Dynamics Lifecycle Servicesin (LCS) kautta.</span><span class="sxs-lookup"><span data-stu-id="57f6f-108">Themes are created by using the Dynamics 365 Commerce online software development kit (SDK), and they are deployed to your websites through Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="57f6f-109">SDK-ohjesivuston kehittäjien teeman virheenkorjausominaisuudet ja moduuliliittymän määritykset luovat mukautettavia ja yhtenäisiä sivustonsuunnittelupaketteja.</span><span class="sxs-lookup"><span data-stu-id="57f6f-109">Theme debugging capabilities and module interface configurations in the SDK help site developers create customizable and cohesive site design packages.</span></span> <span data-ttu-id="57f6f-110">Kun nämä suunnittelupaketit otetaan käyttöön sivustossa, sivuston tekijät voivat keskittyä sisällön luomiseen, muokkaamiseen ja julkaisemiseen sivuston kehittämisen sijasta.</span><span class="sxs-lookup"><span data-stu-id="57f6f-110">When these design packages are deployed to a site, site authors can focus on creating, editing, and publishing content instead of site development.</span></span>

<span data-ttu-id="57f6f-111">Teeman tavanomaisen elinkaaren vuoksi riippuvuus kehittäjistä tekee tyylimuutoksia SDK:n ja LCS-käyttöönottoputken kautta voi joissakin tilanteissa olla esteenä.</span><span class="sxs-lookup"><span data-stu-id="57f6f-111">Given the usual lifecycle of a theme, the dependency on developers to make style changes through the SDK and LCS deployment pipeline can be prohibitive in some scenarios.</span></span> <span data-ttu-id="57f6f-112">Sivuston prototyypit tai hotfix-korjaukset voivat tuntua hankalilta, jos SDK:ta ei ole määritetty tai jos sinulla ei ole aikaa odottaa LCS-käyttöönottoa.</span><span class="sxs-lookup"><span data-stu-id="57f6f-112">Site prototypes or hotfixes can seem cumbersome if the SDK isn't configured, or if you don't have time to wait for an LCS deployment.</span></span>

<span data-ttu-id="57f6f-113">Näissä tilanteissa tiedostojen CSS-korvaaminen voi auttaa.</span><span class="sxs-lookup"><span data-stu-id="57f6f-113">In these scenarios, CSS override files can help.</span></span> <span data-ttu-id="57f6f-114">Todennetut käyttäjät voivat ladata CSS-tiedoston Commercen julkaisutyökalujen avulla, esikatsella sitä ja aktivoida sen ja ohittaa sivuston teeman.</span><span class="sxs-lookup"><span data-stu-id="57f6f-114">In the Commerce authoring tools, authenticated users can upload a CSS file, preview it, and then activate it to override a site's theme.</span></span> <span data-ttu-id="57f6f-115">SDK- tai LCS-käyttöönoton yleiskustannuksia ei tarvita.</span><span class="sxs-lookup"><span data-stu-id="57f6f-115">The overhead of SDK or LCS deployment isn't required.</span></span> <span data-ttu-id="57f6f-116">CSS-ohitustiedostossa määritetyt ohitukset voivat olla yhtä pieniä kuin yksittäisen tekstityylin muutos tai laaja-alainen koko tuotemerkin tarkistaminen.</span><span class="sxs-lookup"><span data-stu-id="57f6f-116">The overrides that are specified in a CSS override file can be as small as a change to a single text style or as wide-ranging as a complete brand overhaul.</span></span>

<span data-ttu-id="57f6f-117">Ennen kuin käytät CSS:n ohitustiedostoja, huomaa seuraavat rajoitukset:</span><span class="sxs-lookup"><span data-stu-id="57f6f-117">Before you use CSS override files, be aware of the following limitations:</span></span>

- <span data-ttu-id="57f6f-118">Vain yksi CSS-ohitustiedosto voi olla aktiivisena sivustossa kerrallaan.</span><span class="sxs-lookup"><span data-stu-id="57f6f-118">Only one CSS override file can be active on a site at a time.</span></span> <span data-ttu-id="57f6f-119">Siksi kaikkien aktiivisten ohitusten on oltava yhdessä ohitustiedostossa.</span><span class="sxs-lookup"><span data-stu-id="57f6f-119">Therefore, all active overrides must be present in a single override file.</span></span>
- <span data-ttu-id="57f6f-120">Vaikka voit esikatsella ohituksia Commerce julkaisutyökaluissa, siinä ei ole erityisiä virheenkorjausominaisuuksia, jotka auttavat tunnistamaan mahdolliset virheet, joita ohittaa.</span><span class="sxs-lookup"><span data-stu-id="57f6f-120">Although you can preview the overrides in the Commerce authoring tools, there are no dedicated debugging features to help identify any bugs that the overrides introduce.</span></span> <span data-ttu-id="57f6f-121">Toisin sanoen, kun käytät CSS:n ohitustiedostoja, sinulla ei ole samaa työkalujoukkoa, jonka SDK tarjoaa moduulin ja sisällönluonnin validointiin.</span><span class="sxs-lookup"><span data-stu-id="57f6f-121">In other words, when you use CSS override files, you don't have the same toolset that the SDK provides for module and authoring validation.</span></span>

<span data-ttu-id="57f6f-122">CSS-ohitustiedostot ovat kuitenkin nopea tapa suunnitella mallin prototyyppi tai toteuttaa hotfix-korjaus, ennen kuin täydellinen teemapäivitys on kehitetty ja otettu käyttöön.</span><span class="sxs-lookup"><span data-stu-id="57f6f-122">Nevertheless, CSS override files provide a quick way to prototype a design or implement a hotfix before a full theme update is developed and deployed.</span></span>

## <a name="create-a-css-override-file"></a><span data-ttu-id="57f6f-123">Luo CSS-ohitustiedosto</span><span class="sxs-lookup"><span data-stu-id="57f6f-123">Create a CSS override file</span></span>

<span data-ttu-id="57f6f-124">Voit luoda CSS-ohitustiedoston käyttämällä mitä tahansa integroitua kehitysympäristöä (IDE), tekstieditoria tai lähdekoodieditoria.</span><span class="sxs-lookup"><span data-stu-id="57f6f-124">To create a CSS override file, you can use any integrated development environment (IDE), text editor, or source code editor.</span></span> <span data-ttu-id="57f6f-125">Tyypillinen lähestymistapa on käyttää tavallisia verkkovirheenkorjaajia selaimessasi tunnistamaan tyylin valitsimet, ominaisuudet ja arvot nykyisessä sivustossa.</span><span class="sxs-lookup"><span data-stu-id="57f6f-125">A typical approach is to use standard web debuggers in your browser to identify style selectors, properties, and values on your existing site.</span></span> <span data-ttu-id="57f6f-126">Useimpien selainten avulla voit muuttaa arvoja ja esikatsella niitä virheenkorjaajassa.</span><span class="sxs-lookup"><span data-stu-id="57f6f-126">Most browsers let you change values and preview them in the debugger.</span></span> <span data-ttu-id="57f6f-127">Kun olet määrittänyt muutokset, jotka haluat tehdä, voit tallentaa ne omaan CSS-tiedostoosi.</span><span class="sxs-lookup"><span data-stu-id="57f6f-127">After you've identified the changes that you want to make, you can save them to your own CSS file.</span></span>

## <a name="upload-a-css-override-file"></a><span data-ttu-id="57f6f-128">Lataa CSS-ohitustiedosto</span><span class="sxs-lookup"><span data-stu-id="57f6f-128">Upload a CSS override file</span></span>

<span data-ttu-id="57f6f-129">Jos haluat ladata CSS-tiedoston sivustoon Commerce-sivustossa, toimi seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="57f6f-129">To upload a CSS file to your site in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="57f6f-130">Siirry muokkaustyökaluissa sivustoon.</span><span class="sxs-lookup"><span data-stu-id="57f6f-130">In the authoring tools, go to your site.</span></span>
1. <span data-ttu-id="57f6f-131">Valitse vasemmanpuoleisessa siirtymisruudussa **Rakenne**.</span><span class="sxs-lookup"><span data-stu-id="57f6f-131">In the navigation pane on the left, select **Design**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="57f6f-132">Voit joutua laajentamaan siirtymisruudun **asetukset**, ennen kuin voit valita **Rakenne** käyttämäsi Commercen julkaisutyökalujen mukaan.</span><span class="sxs-lookup"><span data-stu-id="57f6f-132">Depending on the version of the Commerce authoring tools that you're using, you might have to expand **Settings** in the navigation pane before you can select **Design**.</span></span>

1. <span data-ttu-id="57f6f-133">Valitse päärakenneruudun yläosassa **CSS-ohitus**-välilehti, jos se ei ole jo valittuna.</span><span class="sxs-lookup"><span data-stu-id="57f6f-133">At the top of the main design pane, select the **CSS override** tab, if it isn't already selected.</span></span>
1. <span data-ttu-id="57f6f-134">Valitse **Käytettävissä olevat CSS-ohitukset** -kohdasta **Lataa CSS-tiedosto**.</span><span class="sxs-lookup"><span data-stu-id="57f6f-134">Under **Available CSS overrides**, select **Upload CSS file**.</span></span> <span data-ttu-id="57f6f-135">Näyttöön tulee Resurssienhallinta-ikkuna.</span><span class="sxs-lookup"><span data-stu-id="57f6f-135">A File Explorer window appears.</span></span>
1. <span data-ttu-id="57f6f-136">Selaa Resurssienhallintaa ja valitse CSS-tiedosto ja valitse sitten **Avaa**.</span><span class="sxs-lookup"><span data-stu-id="57f6f-136">In File Explorer, browse to and select a CSS file, and then select **Open**.</span></span> <span data-ttu-id="57f6f-137">Ladattu CSS-tiedosto näkyy nyt **Käytettävissä olevat CSS-ohitukset** -kohdassa.</span><span class="sxs-lookup"><span data-stu-id="57f6f-137">The uploaded CSS file now appears under **Available CSS overrides**.</span></span>

## <a name="preview-a-css-override-file"></a><span data-ttu-id="57f6f-138">CSS-ohitustiedoston esikatseleminen</span><span class="sxs-lookup"><span data-stu-id="57f6f-138">Preview a CSS override file</span></span>

<span data-ttu-id="57f6f-139">Voit esikatsella CSS-ohitustiedostoa, ennen kuin teet sen aktiiviseksi sivustoosi, toimimalla seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="57f6f-139">To preview a CSS override file before you make it active on your live site, follow these steps.</span></span>

1. <span data-ttu-id="57f6f-140">Valitse vasemmalla olevasta siirtymisruudusta **Rakenne** ja etsi sitten **CSS-ohitus**-välilehdellä **Käytettävissä olevat CSS-ohitukset** -kohdasta CSS-tiedosto, jota haluat esikatsella.</span><span class="sxs-lookup"><span data-stu-id="57f6f-140">In the navigation pane on the left, select **Design**, and then, on the **CSS override** tab, under **Available CSS overrides**, find the CSS file that you want to preview.</span></span>
1. <span data-ttu-id="57f6f-141">Valitse CSS-tiedoston nimen vierestä **Esikatsele sivusto**.</span><span class="sxs-lookup"><span data-stu-id="57f6f-141">Next to the CSS file name, select **Preview site**.</span></span>
1. <span data-ttu-id="57f6f-142">Valitse **Valitse URL-osoite** -valintaikkunasta sen sivuston URL-osoite, jonka ohituksen haluat nähdä, ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="57f6f-142">In the **Select a URL** dialog box, select the URL of the site that you want to see the override applied to, and then select **OK**.</span></span>
1. <span data-ttu-id="57f6f-143">Jos valitulle URL-osoitteella on useita variantteja, valitse haluamasi variantti näkyviin tulevasta **Esikatseluvariaatiot**-valintaikkunasta.</span><span class="sxs-lookup"><span data-stu-id="57f6f-143">If there are multiple variants for the selected URL, select the desired variant in the **Preview variations** dialog box that appears.</span></span>

<span data-ttu-id="57f6f-144">Uusi selainvälilehti tai -ikkuna avautuu, jossa voit tarkistaa tyyliisi ohitukset sivustoosi nähden.</span><span class="sxs-lookup"><span data-stu-id="57f6f-144">A new browser tab or window is opened, where you can validate your style overrides against your site.</span></span> <span data-ttu-id="57f6f-145">Voit sitten jakaa URL-osoitteen muiden todennettujen Commerce-käyttäjien kanssa tarkistusta ja palautetta varten.</span><span class="sxs-lookup"><span data-stu-id="57f6f-145">You can then share the URL with other authenticated Commerce users for review and feedback.</span></span>

## <a name="activate-a-css-override-file-on-your-live-site"></a><span data-ttu-id="57f6f-146">Aktivoi CSS-ohitustiedosto live-sivustossasi</span><span class="sxs-lookup"><span data-stu-id="57f6f-146">Activate a CSS override file on your live site</span></span>

<span data-ttu-id="57f6f-147">Kun olet esikatselut ja hyväksynyt CSS-ohitustiedoston, voit aktivoida sen live-sivustossa.</span><span class="sxs-lookup"><span data-stu-id="57f6f-147">After you've previewed and approved the CSS override file, you can activate it on your live site.</span></span>

> [!NOTE]
> <span data-ttu-id="57f6f-148">Vain yksi CSS-ohitustiedosto voi olla aktiivisena kerrallaan sivustossasi.</span><span class="sxs-lookup"><span data-stu-id="57f6f-148">Only one CSS override file can be active on your site at a time.</span></span> <span data-ttu-id="57f6f-149">Jos aktivoit uuden ohitustiedoston, aiempi ohitustiedosto poistetaan käytöstä.</span><span class="sxs-lookup"><span data-stu-id="57f6f-149">If you activate a new override file, the previous override file is inactivated.</span></span> <span data-ttu-id="57f6f-150">Varmista siksi, että kaikki pakolliset ohitukset ovat yksittäisessä CSS-ohitustiedostossa.</span><span class="sxs-lookup"><span data-stu-id="57f6f-150">Therefore, make sure that all required overrides are present in a single CSS override file.</span></span>

<span data-ttu-id="57f6f-151">Voit aktivoida CSS-ohitusasiakirjan seuraavien vaiheiden avulla.</span><span class="sxs-lookup"><span data-stu-id="57f6f-151">To activate a CSS override file, follow these steps.</span></span>

1. <span data-ttu-id="57f6f-152">Valitse vasemmalla olevasta siirtymisruudusta **Rakenne** ja etsi sitten **CSS-ohitus**-välilehdellä **Käytettävissä olevat CSS-ohitukset** -kohdasta CSS-tiedosto, jonka haluat aktivoida.</span><span class="sxs-lookup"><span data-stu-id="57f6f-152">In the navigation pane on the left, select **Design**, and then, on the **CSS override** tab, under **Available CSS overrides**, find the CSS file that you want to activate.</span></span>
1. <span data-ttu-id="57f6f-153">Valitse CSS-tiedoston nimi -kohdasta **Aktivoi**.</span><span class="sxs-lookup"><span data-stu-id="57f6f-153">Under the CSS file name, select **Activate**.</span></span> <span data-ttu-id="57f6f-154">Ohitustiedosto aktivoituu välittömästi live-sivustossa.</span><span class="sxs-lookup"><span data-stu-id="57f6f-154">The override file immediately becomes active on your live site.</span></span>

## <a name="deactivate-a-css-override-file-on-your-live-site"></a><span data-ttu-id="57f6f-155">Poista CSS-ohitustiedosto käytöstä live-sivustossasi</span><span class="sxs-lookup"><span data-stu-id="57f6f-155">Deactivate a CSS override file on your live site</span></span>

<span data-ttu-id="57f6f-156">Voit poistaa CSS-ohitustiedoston käytöstä sivustossa seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="57f6f-156">To deactivate a CSS override file on your site, follow these steps.</span></span>

1. <span data-ttu-id="57f6f-157">Valitse vasemmalla olevasta siirtymisruudusta **Rakenne** ja etsi sitten **CSS-ohitus**-välilehdellä **Käytettävissä olevat CSS-ohitukset** -kohdasta CSS-tiedosto, jonka haluat poistaa käytöstä.</span><span class="sxs-lookup"><span data-stu-id="57f6f-157">In the navigation pane on the left, select **Design**, and then, on the **CSS override** tab, under **Available CSS overrides**, find the CSS file that you want to deactivate.</span></span>
1. <span data-ttu-id="57f6f-158">Valitse CSS-tiedoston nimi -kohdasta **Poista aktivointi**.</span><span class="sxs-lookup"><span data-stu-id="57f6f-158">Under the CSS file name, select **Deactivate**.</span></span> <span data-ttu-id="57f6f-159">Ohitustiedosto muuttuu passiiviseksi välittömästi live-sivustossa.</span><span class="sxs-lookup"><span data-stu-id="57f6f-159">The override file immediately becomes inactive on your live site.</span></span>

> [!TIP]
> <span data-ttu-id="57f6f-160">Jos haluat käyttää lisäasetuksia CSS-ohitustiedostot-vaihtoehdolle, valitse kolme pistettä (**...**) CSS-tiedostonimen vieressä.</span><span class="sxs-lookup"><span data-stu-id="57f6f-160">To access additional options for CSS override files, select the ellipsis (**...**) next to the CSS file name.</span></span> <span data-ttu-id="57f6f-161">**Lataa**-, **Nimeä uudelleen**, ja **Korvaa**-vaihtoehdoista on hyötyä aiemmin luodun CSS-ohitustiedoston nopeille muutoksille.</span><span class="sxs-lookup"><span data-stu-id="57f6f-161">The **Download**, **Rename**, and **Replace** options are useful for quick changes to an existing CSS override file.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="57f6f-162">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="57f6f-162">Additional resources</span></span>

[<span data-ttu-id="57f6f-163">Logon lisääminen</span><span class="sxs-lookup"><span data-stu-id="57f6f-163">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="57f6f-164">Sivuston teeman valitseminen</span><span class="sxs-lookup"><span data-stu-id="57f6f-164">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="57f6f-165">Tyylien esimääritysten käyttäminen</span><span class="sxs-lookup"><span data-stu-id="57f6f-165">Work with style presets</span></span>](style-presets.md)

[<span data-ttu-id="57f6f-166">Favicon-kuvakkeen lisääminen</span><span class="sxs-lookup"><span data-stu-id="57f6f-166">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="57f6f-167">Tervetuloviestin lisääminen</span><span class="sxs-lookup"><span data-stu-id="57f6f-167">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="57f6f-168">Copyright-ilmoituksen lisääminen</span><span class="sxs-lookup"><span data-stu-id="57f6f-168">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="57f6f-169">Kielten lisääminen sivustoon</span><span class="sxs-lookup"><span data-stu-id="57f6f-169">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="57f6f-170">Komentosarjakoodin lisääminen sivuston sivuihin telemetrian tukemiseksi</span><span class="sxs-lookup"><span data-stu-id="57f6f-170">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]