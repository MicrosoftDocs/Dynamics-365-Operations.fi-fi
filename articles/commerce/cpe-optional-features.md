---
title: Valinnaisten ominaisuuksien määrittäminen Dynamics 365 Commercen esikatseluympäristöä varten
description: Tässä ohjeaiheessa kerrotaan, kuinka voit määrittää valinnaisia ominaisuuksia Microsoft Dynamics 365 Commercen esikatseluympäristössä.
author: psimolin
manager: annbe
ms.date: 12/10/2019
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
ms.author: psimolin
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 43b23b9ef881b2ab2f3d005d4ba761848a7fa4ed
ms.sourcegitcommit: 4ed1d8ad8a0206a4172dbb41cc43f7d95073059c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/04/2020
ms.locfileid: "3024726"
---
# <a name="configure-optional-features-for-a-dynamics-365-commerce-preview-environment"></a><span data-ttu-id="46ccd-103">Valinnaisten ominaisuuksien määrittäminen Dynamics 365 Commercen esikatseluympäristöä varten</span><span class="sxs-lookup"><span data-stu-id="46ccd-103">Configure optional features for a Dynamics 365 Commerce preview environment</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="46ccd-104">Tässä ohjeaiheessa kerrotaan, kuinka voit määrittää valinnaisia ominaisuuksia Microsoft Dynamics 365 Commercen esikatseluympäristössä.</span><span class="sxs-lookup"><span data-stu-id="46ccd-104">This topic explains how to configure optional features for a Microsoft Dynamics 365 Commerce preview environment.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="46ccd-105">Edellytykset</span><span class="sxs-lookup"><span data-stu-id="46ccd-105">Prerequisites</span></span>

<span data-ttu-id="46ccd-106">Jos haluat arvioida tapahtuman sähköpostiominaisuuksia, seuraavat edellytykset on täytettävä:</span><span class="sxs-lookup"><span data-stu-id="46ccd-106">If you want to evaluate the transactional email features, the following prerequisites must be met:</span></span>

- <span data-ttu-id="46ccd-107">Käytettävissä on sähköpostipalvelin (Simple Mail Transfer Protocol \[SMTP\]-palvelin), jota voi käyttää sen Microsoft Azure -tilauksen kanssa, jossa esiversioympäristö valmisteltiin.</span><span class="sxs-lookup"><span data-stu-id="46ccd-107">You have an available email server (Simple Mail Transfer Protocol \[SMTP\] server) that can be used from the Microsoft Azure subscription where you provisioned the preview environment.</span></span>
- <span data-ttu-id="46ccd-108">Sinulla on käytettävissä palvelimen täydellinen nimi (FQDN)/IP-osoite, SMTP-portin numero ja todennustiedot.</span><span class="sxs-lookup"><span data-stu-id="46ccd-108">You have the server's fully qualified domain name (FQDN)/IP address, SMTP port number, and authentication details available.</span></span>

<span data-ttu-id="46ccd-109">Jos haluat arvioida digitaalisten resurssien hallintaominaisuuksia käyttämällä uusia monikanavakuvia, sinulla on oltava käytettävissä sisällönhallintajärjestelmän (CMS) vuokraajan nimi.</span><span class="sxs-lookup"><span data-stu-id="46ccd-109">If you want to evaluate Digital Asset Management features by ingesting new omni-channel images, you must have the name of your content management system (CMS) tenant available.</span></span> <span data-ttu-id="46ccd-110">Tämän nimen löytämistä koskevat ohjeet annetaan myöhemmin tässä ohjeaiheessa.</span><span class="sxs-lookup"><span data-stu-id="46ccd-110">Instructions for finding this name are provided later in this topic.</span></span> <span data-ttu-id="46ccd-111">>>> (Q: missä ohjeet ovat?)</span><span class="sxs-lookup"><span data-stu-id="46ccd-111">>>>(Q: where are the instructions?)</span></span>

## <a name="configure-the-image-back-end"></a><span data-ttu-id="46ccd-112">Kuvan taustan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="46ccd-112">Configure the image back end</span></span>

### <a name="find-your-media-base-url"></a><span data-ttu-id="46ccd-113">Median URL-perusosoitteen löytäminen</span><span class="sxs-lookup"><span data-stu-id="46ccd-113">Find your media base URL</span></span>

> [!NOTE]
> <span data-ttu-id="46ccd-114">Ennen kuin voit suorittaa nämä toimet, sinun on suoritettava [sivuston määrittäminen Commercessa](cpe-post-provisioning.md#set-up-your-site-in-commerce).</span><span class="sxs-lookup"><span data-stu-id="46ccd-114">Before you can complete this procedure, you must complete the steps in [Set up your site in Commerce](cpe-post-provisioning.md#set-up-your-site-in-commerce).</span></span>

1. <span data-ttu-id="46ccd-115">Kirjaudu Commercen sivustonhallintatyökaluun käyttämällä URL-osoitetta, johon olet tehnyt huomautuksen verkkokaupan valmistelusta valmistelun aikana (katso [verkkokaupan alustaminen](provisioning-guide.md#initialize-e-commerce)).</span><span class="sxs-lookup"><span data-stu-id="46ccd-115">Sign in to the Commerce site management tool by using the URL you made a note of when you initialized e-Commerce during provisioning (see [Initialize e-Commerce](provisioning-guide.md#initialize-e-commerce)).</span></span>
1. <span data-ttu-id="46ccd-116">Avaa **Fabrikam**-sivusto.</span><span class="sxs-lookup"><span data-stu-id="46ccd-116">Open the **Fabrikam** site.</span></span>
1. <span data-ttu-id="46ccd-117">Valitse vasemmalla olevasta valikosta **Resurssit**.</span><span class="sxs-lookup"><span data-stu-id="46ccd-117">On the menu on the left, select **Assets**.</span></span>
1. <span data-ttu-id="46ccd-118">Valitse jokin yksittäinen kuvaresurssi.</span><span class="sxs-lookup"><span data-stu-id="46ccd-118">Select any single image asset.</span></span>
1. <span data-ttu-id="46ccd-119">Etsi oikealta puolelta ominaisuuksien tarkistamisen **Julkinen URL** -ominaisuus.</span><span class="sxs-lookup"><span data-stu-id="46ccd-119">In the property inspector on the right, find the **Public URL** property.</span></span> <span data-ttu-id="46ccd-120">Arvo on URL-osoite.</span><span class="sxs-lookup"><span data-stu-id="46ccd-120">The value is a URL.</span></span> <span data-ttu-id="46ccd-121">Tässä on esimerkki:</span><span class="sxs-lookup"><span data-stu-id="46ccd-121">Here is an example:</span></span>

    <span data-ttu-id="46ccd-122">`https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/MA1nQC`.</span><span class="sxs-lookup"><span data-stu-id="46ccd-122">`https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/MA1nQC`.</span></span>

1. <span data-ttu-id="46ccd-123">Korvaa URL-osoitteen viimeinen tunniste (**MA1nQC** edellisessä esimerkissä) seuraavalla merkkijonolla **search?fileName=**.</span><span class="sxs-lookup"><span data-stu-id="46ccd-123">Replace the last identifier in the URL (**MA1nQC** in the preceding example) with the string **search?fileName=**.</span></span> <span data-ttu-id="46ccd-124">Tässä on esimerkki siitä, miltä URL-osoite näyttää tämän muutoksen jälkeen:</span><span class="sxs-lookup"><span data-stu-id="46ccd-124">Here is what the example URL looks like after this change is made:</span></span>

    `https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/search?fileName=`

    <span data-ttu-id="46ccd-125">Tämä URL-osoite on median perus-URL-osoite.</span><span class="sxs-lookup"><span data-stu-id="46ccd-125">This URL is your media base URL.</span></span> <span data-ttu-id="46ccd-126">Merkitse se muistiin.</span><span class="sxs-lookup"><span data-stu-id="46ccd-126">Make a note of it.</span></span>

### <a name="update-the-media-base-url"></a><span data-ttu-id="46ccd-127">Median URL-perusosoitteen päivittäminen</span><span class="sxs-lookup"><span data-stu-id="46ccd-127">Update the media base URL</span></span>

1. <span data-ttu-id="46ccd-128">Kirjaudu sisään Dynamics 365 Retail -järjestelmään.</span><span class="sxs-lookup"><span data-stu-id="46ccd-128">Sign in to Dynamics 365 Retail.</span></span>
1. <span data-ttu-id="46ccd-129">Siirry vasemmalla olevan valikon avulla kohtaan **Moduulit \> Vähittäismyynti \> Kanavan asetukset \> Kanavaprofiilit**.</span><span class="sxs-lookup"><span data-stu-id="46ccd-129">Use the menu on the left to go to **Modules \> Retail \> Channel setup \> Channel profiles**.</span></span>
1. <span data-ttu-id="46ccd-130">Valitse **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="46ccd-130">Select **Edit**.</span></span>
1. <span data-ttu-id="46ccd-131">Mene **Profiilin ominaisuudet** -kohdan alle, korvaa **Mediapalvelimen URL-perusosoite** -ominaisuus aiemmin luodulla Median URL-perusosoite -arvolla.</span><span class="sxs-lookup"><span data-stu-id="46ccd-131">Under **Profile properties**, replace the value for the **Media Server Base URL** property with the media base URL that you created earlier.</span></span>
1. <span data-ttu-id="46ccd-132">Valitse toinen kanava vasemmalla olevasta luettelosta **Oletuskanava**-kohdassa.</span><span class="sxs-lookup"><span data-stu-id="46ccd-132">In the list on the left, under the **Default** channel, select the other channel.</span></span>
1. <span data-ttu-id="46ccd-133">Valitse **Profiilin ominaisuudet** -kohdassa **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="46ccd-133">Under **Profile properties**, select **Add**.</span></span>
1. <span data-ttu-id="46ccd-134">Valitse lisättyjen ominaisuuksien kohdalla **Mediapalvelimen perus-URL-osoite** ominaisuusavaimeksi.</span><span class="sxs-lookup"><span data-stu-id="46ccd-134">For the property that was added, select **Media Server Base URL** as the property key.</span></span> <span data-ttu-id="46ccd-135">Kirjoita ominaisuuden arvoksi aiemmin luomasi median perus-URL-osoitteen URL-osoite.</span><span class="sxs-lookup"><span data-stu-id="46ccd-135">As the property value, enter the media base URL that you created earlier.</span></span>
1. <span data-ttu-id="46ccd-136">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="46ccd-136">Select **Save**.</span></span>

## <a name="configure-the-email-server"></a><span data-ttu-id="46ccd-137">Sähköpostipalvelimen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="46ccd-137">Configure the email server</span></span>

> [!NOTE]
> <span data-ttu-id="46ccd-138">Tähän syötettävän SMTP-palvelimen tai sähköpostipalvelun on oltava käytettävissä ympäristössä käytettävän Azure-tilauksen avulla.</span><span class="sxs-lookup"><span data-stu-id="46ccd-138">The SMTP server or email service that you enter here must be accessible from the Azure subscription that you're using for the environment.</span></span>

1. <span data-ttu-id="46ccd-139">Kirjaudu sisään Retailiin.</span><span class="sxs-lookup"><span data-stu-id="46ccd-139">Sign in to Retail.</span></span>
1. <span data-ttu-id="46ccd-140">Siirry vasemmalla olevan valikon avulla kohtaan **Moduulit \> Hallinta \> Asetukset \> Sähköposti \> Sähköpostiparametrit**.</span><span class="sxs-lookup"><span data-stu-id="46ccd-140">Use the menu on the left to go to **Modules \> System administration \> Setup \> Email \> Email parameters**.</span></span>
1. <span data-ttu-id="46ccd-141">Kirjoita **SMTP-asetukset**-välilehden **Lähtevän postin palvelin** -kenttään SMTP-palvelimen tai sähköpostipalvelun FQDN-tai IP-osoite.</span><span class="sxs-lookup"><span data-stu-id="46ccd-141">On the **SMTP settings** tab, in the **Outgoing mail server** field, enter the FQDN or IP address of your SMTP server or email service.</span></span>
1. <span data-ttu-id="46ccd-142">Kirjoita **SMTP-porttinumero**-kenttään porttinumero.</span><span class="sxs-lookup"><span data-stu-id="46ccd-142">In the **SMTP port number** field, enter the port number.</span></span> <span data-ttu-id="46ccd-143">(Jos et käytä Secure Sockets Layer \[SSL\]-suojausta, oletusportin numero on **25**.)</span><span class="sxs-lookup"><span data-stu-id="46ccd-143">(If you aren't using Secure Sockets Layer \[SSL\], the default port number is **25**.)</span></span>
1. <span data-ttu-id="46ccd-144">Jos todennus on pakollinen, kirjoita arvot **Käyttäjänimi**- ja **Salasana**-kenttiin.</span><span class="sxs-lookup"><span data-stu-id="46ccd-144">If authentication is required, enter values in the **User name** and **Password** fields.</span></span>
1. <span data-ttu-id="46ccd-145">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="46ccd-145">Select **Save**.</span></span>
1. <span data-ttu-id="46ccd-146">Valitse **Päivitä**.</span><span class="sxs-lookup"><span data-stu-id="46ccd-146">Select **Refresh**.</span></span>
1. <span data-ttu-id="46ccd-147">Valitse **Testaa sähköposti** -välilehdellä**Sähköpostipalvelu**-kentässä **SMTP**.</span><span class="sxs-lookup"><span data-stu-id="46ccd-147">On the **Test email** tab, in the **Email provider** field, select **SMTP**.</span></span>
1. <span data-ttu-id="46ccd-148">Kirjoita **Lähetä**-kenttään sähköpostiosoite, johon testisähköpostiviesti tulee toimittaa.</span><span class="sxs-lookup"><span data-stu-id="46ccd-148">In the **Send to** field, enter the email address that the test email should be delivered to.</span></span>
1. <span data-ttu-id="46ccd-149">Valitse **Lähetä testisähköpostiviesti**.</span><span class="sxs-lookup"><span data-stu-id="46ccd-149">Select **Send test email**.</span></span>

## <a name="configure-email-templates"></a><span data-ttu-id="46ccd-150">Sähköpostimallien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="46ccd-150">Configure email templates</span></span>

<span data-ttu-id="46ccd-151">Jokaista tapahtumaa kohti, josta haluat lähettää sähköposteja, on päivitettävä sähköpostimalli, jossa on sallittu lähettäjän sähköpostiosoite.</span><span class="sxs-lookup"><span data-stu-id="46ccd-151">For each transactional event that you want to send emails for, you must update the email template with a valid sender email address.</span></span>

1. <span data-ttu-id="46ccd-152">Kirjaudu sisään Retailiin.</span><span class="sxs-lookup"><span data-stu-id="46ccd-152">Sign in to Retail.</span></span>
1. <span data-ttu-id="46ccd-153">Siirry vasemmalla olevan valikon avulla kohtaan **Moduulit \> Organisaation hallinta \> Asetukset \> Organisaation sähköpostimallit**.</span><span class="sxs-lookup"><span data-stu-id="46ccd-153">Use the menu on the left to go to **Modules \> Organization administration \> Setup \> Organization email templates**.</span></span>
1. <span data-ttu-id="46ccd-154">Valitse **Näytä luettelo**.</span><span class="sxs-lookup"><span data-stu-id="46ccd-154">Select **Show list**.</span></span>
1. <span data-ttu-id="46ccd-155">Luo kukin luettelossa oleva malli seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="46ccd-155">For each template in the list, follow these steps:</span></span>

    1. <span data-ttu-id="46ccd-156">Kirjoita **Lähettäjän sähköpostiosoite** -kenttään lähettäjän sähköpostiosoite.</span><span class="sxs-lookup"><span data-stu-id="46ccd-156">In the **Sender email** field, enter the sender email address.</span></span>
    1. <span data-ttu-id="46ccd-157">Valinnainen: Kirjoita **Lähettäjän nimi** -kenttään nimi, jota käytetään lähettäjän nimenä.</span><span class="sxs-lookup"><span data-stu-id="46ccd-157">Optional: In the **Sender name** field, enter the name that should be used as the sender name.</span></span>

1. <span data-ttu-id="46ccd-158">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="46ccd-158">Select **Save**.</span></span>

## <a name="customize-email-templates"></a><span data-ttu-id="46ccd-159">Mukauta sähköpostimalleja</span><span class="sxs-lookup"><span data-stu-id="46ccd-159">Customize email templates</span></span>

<span data-ttu-id="46ccd-160">Haluat ehkä mukauttaa sähköpostimalleja niin, että ne käyttävät eri kuvia.</span><span class="sxs-lookup"><span data-stu-id="46ccd-160">You might want to customize the email templates so that they use different images.</span></span> <span data-ttu-id="46ccd-161">Tai haluat ehkä päivittää mallien linkit niin, että ne menevät esikatseluympäristöön.</span><span class="sxs-lookup"><span data-stu-id="46ccd-161">Or you might want to update the links in the templates so that they go to your preview environment.</span></span> <span data-ttu-id="46ccd-162">Tässä menettelyssä kerrotaan, miten oletusmallit ladataan ja mukautetaan ja miten järjestelmän mallit päivitetään.</span><span class="sxs-lookup"><span data-stu-id="46ccd-162">This procedure explains how to download the default templates, customize them, and update the templates in the system.</span></span>

1. <span data-ttu-id="46ccd-163">Lataa selaimessa [Microsoft Dynamics 365 Commerce -esikatselusovelluksen oletussähköpostimallien zip-tiedosto](https://download.microsoft.com/download/d/7/b/d7b6c4d4-fe09-4922-9551-46bbb29d202d/Commerce.Preview.Default.Email.Templates.zip) paikallista tietokonetta varten.</span><span class="sxs-lookup"><span data-stu-id="46ccd-163">In a web browser, download the [Microsoft Dynamics 365 Commerce Preview default email templates zip file](https://download.microsoft.com/download/d/7/b/d7b6c4d4-fe09-4922-9551-46bbb29d202d/Commerce.Preview.Default.Email.Templates.zip) to your local computer.</span></span> <span data-ttu-id="46ccd-164">Tämä tiedosto sisältää seuraavat HTML-asiakirjat:</span><span class="sxs-lookup"><span data-stu-id="46ccd-164">This file contains the following HTML documents:</span></span>

    - <span data-ttu-id="46ccd-165">Tilauksen vahvistuksen malli</span><span class="sxs-lookup"><span data-stu-id="46ccd-165">Order confirmation template</span></span>
    - <span data-ttu-id="46ccd-166">Lahjakorttimallin lähettäminen</span><span class="sxs-lookup"><span data-stu-id="46ccd-166">Issue gift card template</span></span>
    - <span data-ttu-id="46ccd-167">Uusi tilausmalli</span><span class="sxs-lookup"><span data-stu-id="46ccd-167">New order template</span></span>
    - <span data-ttu-id="46ccd-168">Pakkaustilauksen malli</span><span class="sxs-lookup"><span data-stu-id="46ccd-168">Pack order template</span></span>
    - <span data-ttu-id="46ccd-169">Keräystilauksen malli</span><span class="sxs-lookup"><span data-stu-id="46ccd-169">Pick order template</span></span>

1. <span data-ttu-id="46ccd-170">Mukauta malleja teksti- tai HTML-editorin avulla.</span><span class="sxs-lookup"><span data-stu-id="46ccd-170">Customize the templates by using a text or HTML editor.</span></span> <span data-ttu-id="46ccd-171">Katso [tuettujen tunnusten](#supported-tokens-in-the-email-template) luettelo myöhemmin tässä ohjeaiheessa.</span><span class="sxs-lookup"><span data-stu-id="46ccd-171">See the list of [supported tokens](#supported-tokens-in-the-email-template) later in this topic.</span></span>
1. <span data-ttu-id="46ccd-172">Kirjaudu sisään Retailiin.</span><span class="sxs-lookup"><span data-stu-id="46ccd-172">Sign in to Retail.</span></span>
1. <span data-ttu-id="46ccd-173">Siirry vasemmalla olevan valikon avulla kohtaan **Moduulit \> Organisaation hallinta \> Asetukset \> Organisaation sähköpostimallit**.</span><span class="sxs-lookup"><span data-stu-id="46ccd-173">Use the menu on the left to go to **Modules \> Organization administration \> Setup \> Organization email templates**.</span></span>
1. <span data-ttu-id="46ccd-174">Laajenna vasemmanpuoleista luetteloa, niin näet kaikki mallit.</span><span class="sxs-lookup"><span data-stu-id="46ccd-174">Expand the list on the left to see all the templates.</span></span>
1. <span data-ttu-id="46ccd-175">Noudata seuraavia vaiheita jokaiselle mukautettavan mallin kohdalle:</span><span class="sxs-lookup"><span data-stu-id="46ccd-175">For each template that you want to customize, follow these steps:</span></span>

    1. <span data-ttu-id="46ccd-176">Valitse luettelossa oleva malli.</span><span class="sxs-lookup"><span data-stu-id="46ccd-176">Select the template in the list.</span></span>
    1. <span data-ttu-id="46ccd-177">Valitse **Sähköpostiviestin sisältö** -kohdassa soveltuva kieliversio luettelosta.</span><span class="sxs-lookup"><span data-stu-id="46ccd-177">Under **Email message content**, select the appropriate language version in the list.</span></span> <span data-ttu-id="46ccd-178">(Oletuskieli on **fi-fi**.)</span><span class="sxs-lookup"><span data-stu-id="46ccd-178">(The default language is **en-us**.)</span></span>
    1. <span data-ttu-id="46ccd-179">Valitse **Sähköpostiviestin sisältö** -kohdassa **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="46ccd-179">Under **Email message content**, select **Edit**.</span></span> <span data-ttu-id="46ccd-180">**Lataa sähköpostimalli** -ruutu tulee näkyviin.</span><span class="sxs-lookup"><span data-stu-id="46ccd-180">The **Upload email template** pane appears.</span></span>
    1. <span data-ttu-id="46ccd-181">Valitse **Selaa** ja Etsi HTML-tiedosto, jolla on mukautettu sisältö.</span><span class="sxs-lookup"><span data-stu-id="46ccd-181">Select **Browse**, and find the HTML file that has the customized content.</span></span>
    1. <span data-ttu-id="46ccd-182">Valitse **Lataa palvelimeen**.</span><span class="sxs-lookup"><span data-stu-id="46ccd-182">Select **Upload**.</span></span> <span data-ttu-id="46ccd-183">Malli ladataan järjestelmään ja näkyviin tulee esikatselu.</span><span class="sxs-lookup"><span data-stu-id="46ccd-183">The template is uploaded into the system, and a preview is shown.</span></span>
    1. <span data-ttu-id="46ccd-184">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="46ccd-184">Select **OK**.</span></span>
    1. <span data-ttu-id="46ccd-185">Valinnainen: Mukauta mallin **Aihe**-ominaisuutta.</span><span class="sxs-lookup"><span data-stu-id="46ccd-185">Optional: Customize the **Subject** property of the template.</span></span>
    1. <span data-ttu-id="46ccd-186">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="46ccd-186">Select **Save**.</span></span>

### <a name="supported-tokens-in-the-email-template"></a><span data-ttu-id="46ccd-187">Sähköpostimallin tuetut tunnukset</span><span class="sxs-lookup"><span data-stu-id="46ccd-187">Supported tokens in the email template</span></span>

<span data-ttu-id="46ccd-188">Kun sähköposti lähetetään, nämä tunnukset korvataan todellisilla arvoilla, jotka koskevat asiakasta ja asiakkaan tilausta.</span><span class="sxs-lookup"><span data-stu-id="46ccd-188">When the email is rendered, these tokens are replaced with actual values that apply to the customer and the customer's order.</span></span>

#### <a name="sales-order"></a><span data-ttu-id="46ccd-189">Myyntitilaus</span><span class="sxs-lookup"><span data-stu-id="46ccd-189">Sales order</span></span>

<span data-ttu-id="46ccd-190">Seuraavat tunnukset koskevat yleistä myyntitilausta.</span><span class="sxs-lookup"><span data-stu-id="46ccd-190">The following tokens apply to the overall sales order.</span></span>

| <span data-ttu-id="46ccd-191">Tunnuksen nimi</span><span class="sxs-lookup"><span data-stu-id="46ccd-191">Name of the token</span></span> | <span data-ttu-id="46ccd-192">Tunnus</span><span class="sxs-lookup"><span data-stu-id="46ccd-192">Token</span></span> |
|-------------------|-------|
| <span data-ttu-id="46ccd-193">Tilausnumero</span><span class="sxs-lookup"><span data-stu-id="46ccd-193">Order number</span></span>      | <span data-ttu-id="46ccd-194">%salesid%</span><span class="sxs-lookup"><span data-stu-id="46ccd-194">%salesid%</span></span> |
| <span data-ttu-id="46ccd-195">Asiakkaan nimi</span><span class="sxs-lookup"><span data-stu-id="46ccd-195">Customer's name</span></span>   | <span data-ttu-id="46ccd-196">%customername%</span><span class="sxs-lookup"><span data-stu-id="46ccd-196">%customername%</span></span> |
| <span data-ttu-id="46ccd-197">Toimitusosoite</span><span class="sxs-lookup"><span data-stu-id="46ccd-197">Delivery address</span></span>  | <span data-ttu-id="46ccd-198">%deliveryaddress%</span><span class="sxs-lookup"><span data-stu-id="46ccd-198">%deliveryaddress%</span></span> |
| <span data-ttu-id="46ccd-199">Laskutusosoite</span><span class="sxs-lookup"><span data-stu-id="46ccd-199">Billing address</span></span>   | <span data-ttu-id="46ccd-200">%customeraddress%</span><span class="sxs-lookup"><span data-stu-id="46ccd-200">%customeraddress%</span></span> |
| <span data-ttu-id="46ccd-201">Tilauspäivämäärä</span><span class="sxs-lookup"><span data-stu-id="46ccd-201">Order date</span></span>        | <span data-ttu-id="46ccd-202">%shipdate%</span><span class="sxs-lookup"><span data-stu-id="46ccd-202">%shipdate%</span></span> |
| <span data-ttu-id="46ccd-203">Toimitustapa</span><span class="sxs-lookup"><span data-stu-id="46ccd-203">Delivery mode</span></span>     | <span data-ttu-id="46ccd-204">%modeofdelivery%</span><span class="sxs-lookup"><span data-stu-id="46ccd-204">%modeofdelivery%</span></span> |
| <span data-ttu-id="46ccd-205">Alennus</span><span class="sxs-lookup"><span data-stu-id="46ccd-205">Discount</span></span>          | <span data-ttu-id="46ccd-206">%discount%</span><span class="sxs-lookup"><span data-stu-id="46ccd-206">%discount%</span></span> |
| <span data-ttu-id="46ccd-207">Arvonlisävero</span><span class="sxs-lookup"><span data-stu-id="46ccd-207">Sales tax</span></span>         | <span data-ttu-id="46ccd-208">%tax%</span><span class="sxs-lookup"><span data-stu-id="46ccd-208">%tax%</span></span> |
| <span data-ttu-id="46ccd-209">Tilauksen kokonaissumma</span><span class="sxs-lookup"><span data-stu-id="46ccd-209">Order total</span></span>       | <span data-ttu-id="46ccd-210">%total%</span><span class="sxs-lookup"><span data-stu-id="46ccd-210">%total%</span></span> |

#### <a name="sales-line"></a><span data-ttu-id="46ccd-211">Myyntirivi</span><span class="sxs-lookup"><span data-stu-id="46ccd-211">Sales line</span></span>

<span data-ttu-id="46ccd-212">Seuraavat tunnukset korvataan arvoilla jokaisessa tuotteessa tilauksessa.</span><span class="sxs-lookup"><span data-stu-id="46ccd-212">The following tokens are replaced with values for each product in the order.</span></span>

> [!NOTE]
> <span data-ttu-id="46ccd-213">Sijoita **Tuoteluettelo - aloitus** -tunnus jokaiselle tuotteelle toistetun HTML-lohkon alkuun ja sijoita **Tuoteluettelo - lopetus** -tunnus lohkon loppuun.</span><span class="sxs-lookup"><span data-stu-id="46ccd-213">Put the **Product list - start** token at the beginning of the HTML block that is repeated for every product, and put the **Product list - end** token at the end of the block.</span></span>

| <span data-ttu-id="46ccd-214">Tunnuksen nimi</span><span class="sxs-lookup"><span data-stu-id="46ccd-214">Name of the token</span></span>      | <span data-ttu-id="46ccd-215">Tunnus</span><span class="sxs-lookup"><span data-stu-id="46ccd-215">Token</span></span> |
|------------------------|-------|
| <span data-ttu-id="46ccd-216">Tuoteluettelo - alku</span><span class="sxs-lookup"><span data-stu-id="46ccd-216">Product list - start</span></span>   | <span data-ttu-id="46ccd-217">\<!--%tablebegin.salesline% --\></span><span class="sxs-lookup"><span data-stu-id="46ccd-217">\<!--%tablebegin.salesline% --\></span></span> |
| <span data-ttu-id="46ccd-218">Tuoteluettelo - loppu</span><span class="sxs-lookup"><span data-stu-id="46ccd-218">Product list - end</span></span>     | <span data-ttu-id="46ccd-219">\<!--%tableend.salesline%--\></span><span class="sxs-lookup"><span data-stu-id="46ccd-219">\<!--%tableend.salesline%--\></span></span> |
| <span data-ttu-id="46ccd-220">Tuotteen nimi</span><span class="sxs-lookup"><span data-stu-id="46ccd-220">Product name</span></span>           | <span data-ttu-id="46ccd-221">%lineproductname%</span><span class="sxs-lookup"><span data-stu-id="46ccd-221">%lineproductname%</span></span> |
| <span data-ttu-id="46ccd-222">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="46ccd-222">Description</span></span>            | <span data-ttu-id="46ccd-223">%lineproductdescription%</span><span class="sxs-lookup"><span data-stu-id="46ccd-223">%lineproductdescription%</span></span> |
| <span data-ttu-id="46ccd-224">Määrä</span><span class="sxs-lookup"><span data-stu-id="46ccd-224">Quantity</span></span>               | <span data-ttu-id="46ccd-225">%linequantity%</span><span class="sxs-lookup"><span data-stu-id="46ccd-225">%linequantity%</span></span> |
| <span data-ttu-id="46ccd-226">Rivin yksikköhinta</span><span class="sxs-lookup"><span data-stu-id="46ccd-226">Line unit price</span></span>        | <span data-ttu-id="46ccd-227">%lineprice% (verify)</span><span class="sxs-lookup"><span data-stu-id="46ccd-227">%lineprice% (verify)</span></span> |
| <span data-ttu-id="46ccd-228">rivinimikkeen kokonaissumma</span><span class="sxs-lookup"><span data-stu-id="46ccd-228">line item total</span></span>        | <span data-ttu-id="46ccd-229">%linenetamount%</span><span class="sxs-lookup"><span data-stu-id="46ccd-229">%linenetamount%</span></span> |
| <span data-ttu-id="46ccd-230">rivin alennus</span><span class="sxs-lookup"><span data-stu-id="46ccd-230">line discount</span></span>          | <span data-ttu-id="46ccd-231">%linediscount%</span><span class="sxs-lookup"><span data-stu-id="46ccd-231">%linediscount%</span></span> |
| <span data-ttu-id="46ccd-232">Lähetyspäivä</span><span class="sxs-lookup"><span data-stu-id="46ccd-232">Ship date</span></span>              | <span data-ttu-id="46ccd-233">%lineshipdate%</span><span class="sxs-lookup"><span data-stu-id="46ccd-233">%lineshipdate%</span></span> |
| <span data-ttu-id="46ccd-234">Hankintamenetelmä</span><span class="sxs-lookup"><span data-stu-id="46ccd-234">Procurement method</span></span>     | <span data-ttu-id="46ccd-235">%linedeliverymode%</span><span class="sxs-lookup"><span data-stu-id="46ccd-235">%linedeliverymode%</span></span> |
| <span data-ttu-id="46ccd-236">toimitusosoite</span><span class="sxs-lookup"><span data-stu-id="46ccd-236">delivery address</span></span>       | <span data-ttu-id="46ccd-237">%linedeliveryaddress%</span><span class="sxs-lookup"><span data-stu-id="46ccd-237">%linedeliveryaddress%</span></span> |
| <span data-ttu-id="46ccd-238">Rivin myyntiyksikkö</span><span class="sxs-lookup"><span data-stu-id="46ccd-238">Sales unit of the line</span></span> | <span data-ttu-id="46ccd-239">%lineunit%</span><span class="sxs-lookup"><span data-stu-id="46ccd-239">%lineunit%</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="46ccd-240">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="46ccd-240">Additional resources</span></span>

[<span data-ttu-id="46ccd-241">Dynamics 365 Commercen esikatseluympäristön yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="46ccd-241">Dynamics 365 Commerce preview environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="46ccd-242">Dynamics 365 Commercen esiversioympäristön valmistelu</span><span class="sxs-lookup"><span data-stu-id="46ccd-242">Provision a Dynamics 365 Commerce preview environment</span></span>](provisioning-guide.md)

[<span data-ttu-id="46ccd-243">Dynamics 365 Commercen esikatseluympäristön määrittäminen</span><span class="sxs-lookup"><span data-stu-id="46ccd-243">Configure a Dynamics 365 Commerce preview environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="46ccd-244">Dynamics 365 Commerce -esikatseluympäristön usein kysytyt kysymykset</span><span class="sxs-lookup"><span data-stu-id="46ccd-244">Dynamics 365 Commerce preview environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="46ccd-245">Microsoft Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="46ccd-245">Microsoft Lifecycle Services (LCS)</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="46ccd-246">Retail Cloud Scale Unit (RCSU)</span><span class="sxs-lookup"><span data-stu-id="46ccd-246">Retail Cloud Scale Unit (RCSU)</span></span>](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="46ccd-247">Microsoft Azure -portaali</span><span class="sxs-lookup"><span data-stu-id="46ccd-247">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="46ccd-248">Dynamics 365 Commerce -sivusto</span><span class="sxs-lookup"><span data-stu-id="46ccd-248">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)
