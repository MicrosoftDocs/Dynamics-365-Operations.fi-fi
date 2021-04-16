---
title: Valinnaisten toimintojen määrittäminen Dynamics 365 Commerce -arviointiympäristöä varten
description: Tässä ohjeaiheessa kerrotaan, miten valinnaiset toiminnot määritetään Microsoft Dynamics 365 Commercen arviointiympäristössä.
author: psimolin
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 6bc968c2659380bb8c92292ee19e3a7ec8a20a2b
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795904"
---
# <a name="configure-optional-features-for-a-dynamics-365-commerce-evaluation-environment"></a><span data-ttu-id="11a66-103">Dynamics 365 Commerce -arviointiympäristön valinnaisten ominaisuuksien määritykset</span><span class="sxs-lookup"><span data-stu-id="11a66-103">Configure optional features for a Dynamics 365 Commerce evaluation environment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="11a66-104">Tässä ohjeaiheessa kerrotaan, miten valinnaiset toiminnot määritetään Microsoft Dynamics 365 Commercen arviointiympäristössä.</span><span class="sxs-lookup"><span data-stu-id="11a66-104">This topic explains how to configure optional features for a Microsoft Dynamics 365 Commerce evaluation environment.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="11a66-105">Edellytykset</span><span class="sxs-lookup"><span data-stu-id="11a66-105">Prerequisites</span></span>

<span data-ttu-id="11a66-106">Jos haluat arvioida tapahtuman sähköpostiominaisuuksia, seuraavat edellytykset on täytettävä:</span><span class="sxs-lookup"><span data-stu-id="11a66-106">If you want to evaluate the transactional email features, the following prerequisites must be met:</span></span>

- <span data-ttu-id="11a66-107">Käytettävissä on sähköpostipalvelin (Simple Mail Transfer Protocol \[SMTP\]-palvelin), jota voi käyttää sen Microsoft Azure -tilauksen kanssa, jossa arviointiympäristö valmisteltiin.</span><span class="sxs-lookup"><span data-stu-id="11a66-107">You have an available email server (Simple Mail Transfer Protocol \[SMTP\] server) that can be used from the Microsoft Azure subscription where you provisioned the evaluation environment.</span></span>
- <span data-ttu-id="11a66-108">Sinulla on käytettävissä palvelimen täydellinen nimi (FQDN)/IP-osoite, SMTP-portin numero ja todennustiedot.</span><span class="sxs-lookup"><span data-stu-id="11a66-108">You have the server's fully qualified domain name (FQDN)/IP address, SMTP port number, and authentication details available.</span></span>

## <a name="configure-the-image-back-end"></a><span data-ttu-id="11a66-109">Kuvan taustan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="11a66-109">Configure the image back end</span></span>

### <a name="find-your-media-base-url"></a><span data-ttu-id="11a66-110">Median URL-perusosoitteen löytäminen</span><span class="sxs-lookup"><span data-stu-id="11a66-110">Find your media base URL</span></span>

> [!NOTE]
> <span data-ttu-id="11a66-111">Ennen kuin voit suorittaa nämä toimet, sinun on suoritettava [sivuston määrittäminen Commercessa](cpe-post-provisioning.md#set-up-your-site-in-commerce).</span><span class="sxs-lookup"><span data-stu-id="11a66-111">Before you can complete this procedure, you must complete the steps in [Set up your site in Commerce](cpe-post-provisioning.md#set-up-your-site-in-commerce).</span></span>

1. <span data-ttu-id="11a66-112">Kirjaudu Commercen sivustonmuodostimeen käyttämällä URL-osoitetta, johon olet tehnyt huomautuksen verkkokaupan valmistelusta valmistelun aikana (katso [verkkokaupan alustaminen](provisioning-guide.md#initialize-e-commerce)).</span><span class="sxs-lookup"><span data-stu-id="11a66-112">Sign in to the Commerce site builder by using the URL you made a note of when you initialized e-Commerce during provisioning (see [Initialize e-Commerce](provisioning-guide.md#initialize-e-commerce)).</span></span>
1. <span data-ttu-id="11a66-113">Avaa **Fabrikam**-sivusto.</span><span class="sxs-lookup"><span data-stu-id="11a66-113">Open the **Fabrikam** site.</span></span>
1. <span data-ttu-id="11a66-114">Valitse vasemmalla olevasta valikosta **Mediakirjasto**.</span><span class="sxs-lookup"><span data-stu-id="11a66-114">On the menu on the left, select **Media Library**.</span></span>
1. <span data-ttu-id="11a66-115">Valitse jokin yksittäinen kuvaresurssi.</span><span class="sxs-lookup"><span data-stu-id="11a66-115">Select any single image asset.</span></span>
1. <span data-ttu-id="11a66-116">Etsi oikealta puolelta ominaisuuksien tarkistamisen **Julkinen URL** -ominaisuus.</span><span class="sxs-lookup"><span data-stu-id="11a66-116">In the property inspector on the right, find the **Public URL** property.</span></span> <span data-ttu-id="11a66-117">Arvo on URL-osoite.</span><span class="sxs-lookup"><span data-stu-id="11a66-117">The value is a URL.</span></span> <span data-ttu-id="11a66-118">Tässä on esimerkki:</span><span class="sxs-lookup"><span data-stu-id="11a66-118">Here is an example:</span></span>

    <span data-ttu-id="11a66-119">`https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/MA1nQC`.</span><span class="sxs-lookup"><span data-stu-id="11a66-119">`https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/MA1nQC`.</span></span>

1. <span data-ttu-id="11a66-120">Korvaa URL-osoitteen viimeinen tunniste (**MA1nQC** edellisessä esimerkissä) seuraavalla merkkijonolla **search?fileName=**.</span><span class="sxs-lookup"><span data-stu-id="11a66-120">Replace the last identifier in the URL (**MA1nQC** in the preceding example) with the string **search?fileName=**.</span></span> <span data-ttu-id="11a66-121">Tässä on esimerkki siitä, miltä URL-osoite näyttää tämän muutoksen jälkeen:</span><span class="sxs-lookup"><span data-stu-id="11a66-121">Here is what the example URL looks like after this change is made:</span></span>

    `https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/search?fileName=`

    <span data-ttu-id="11a66-122">Tämä URL-osoite on median perus-URL-osoite.</span><span class="sxs-lookup"><span data-stu-id="11a66-122">This URL is your media base URL.</span></span> <span data-ttu-id="11a66-123">Merkitse se muistiin.</span><span class="sxs-lookup"><span data-stu-id="11a66-123">Make a note of it.</span></span>

### <a name="update-the-media-base-url"></a><span data-ttu-id="11a66-124">Median URL-perusosoitteen päivittäminen</span><span class="sxs-lookup"><span data-stu-id="11a66-124">Update the media base URL</span></span>

1. <span data-ttu-id="11a66-125">Kirjaudu sisään Commercen pääkonttoriversioon.</span><span class="sxs-lookup"><span data-stu-id="11a66-125">Sign in to Commerce headquarters.</span></span>
1. <span data-ttu-id="11a66-126">Siirry vasemmalla olevan valikon avulla kohtaan **Moduulit \> Vähittäismyynti ja kauppa \> Kanavan asetukset \> Kanavaprofiilit**.</span><span class="sxs-lookup"><span data-stu-id="11a66-126">Use the menu on the left to go to **Modules \> Retail and commerce \> Channel setup \> Channel profiles**.</span></span>
1. <span data-ttu-id="11a66-127">Valitse **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="11a66-127">Select **Edit**.</span></span>
1. <span data-ttu-id="11a66-128">Mene **Profiilin ominaisuudet** -kohdan alle, korvaa **Mediapalvelimen URL-perusosoite** -ominaisuus aiemmin luodulla Median URL-perusosoite -arvolla.</span><span class="sxs-lookup"><span data-stu-id="11a66-128">Under **Profile properties**, replace the value for the **Media Server Base URL** property with the media base URL that you created earlier.</span></span>
1. <span data-ttu-id="11a66-129">Valitse kanava, jonka nimi on **scXXXXXXXXX**.</span><span class="sxs-lookup"><span data-stu-id="11a66-129">Select the channel that is named **scXXXXXXXXX**.</span></span>
1. <span data-ttu-id="11a66-130">Valitse **Profiilin ominaisuudet** -kohdassa **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="11a66-130">Under **Profile properties**, select **Add**.</span></span>
1. <span data-ttu-id="11a66-131">Valitse lisättyjen ominaisuuksien kohdalla **Mediapalvelimen perus-URL-osoite** ominaisuusavaimeksi.</span><span class="sxs-lookup"><span data-stu-id="11a66-131">For the property that was added, select **Media Server Base URL** as the property key.</span></span> <span data-ttu-id="11a66-132">Kirjoita ominaisuuden arvoksi aiemmin luomasi median perus-URL-osoitteen URL-osoite.</span><span class="sxs-lookup"><span data-stu-id="11a66-132">As the property value, enter the media base URL that you created earlier.</span></span>
1. <span data-ttu-id="11a66-133">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="11a66-133">Select **Save**.</span></span>

## <a name="configure-and-test-the-email-server"></a><span data-ttu-id="11a66-134">Sähköpostipalvelimen määrittäminen ja testaaminen</span><span class="sxs-lookup"><span data-stu-id="11a66-134">Configure and test the email server</span></span>

> [!NOTE]
> <span data-ttu-id="11a66-135">Tähän syötettävän SMTP-palvelimen tai sähköpostipalvelun on oltava käytettävissä ympäristössä käytettävän Azure-tilauksen avulla.</span><span class="sxs-lookup"><span data-stu-id="11a66-135">The SMTP server or email service that you enter here must be accessible from the Azure subscription that you're using for the environment.</span></span>

1. <span data-ttu-id="11a66-136">Kirjaudu sisään Commercen pääkonttoriversioon.</span><span class="sxs-lookup"><span data-stu-id="11a66-136">Sign in to Commerce headquarters.</span></span>
1. <span data-ttu-id="11a66-137">Valitse vasemman valikon avulla **Moduulit \> Retail ja Commerce \> Pääkonttorin asetukset \> Parametrit \> Sähköpostiparametrit**.</span><span class="sxs-lookup"><span data-stu-id="11a66-137">Use the menu on the left to go to **Modules \> Retail and Commerce \> Headquarters setup \> Parameters \> Email parameters**.</span></span>
1. <span data-ttu-id="11a66-138">Kirjoita **SMTP-asetukset**-välilehden **Lähtevän postin palvelin** -kenttään SMTP-palvelimen tai sähköpostipalvelun FQDN-tai IP-osoite.</span><span class="sxs-lookup"><span data-stu-id="11a66-138">On the **SMTP settings** tab, in the **Outgoing mail server** field, enter the FQDN or IP address of your SMTP server or email service.</span></span>
1. <span data-ttu-id="11a66-139">Kirjoita **SMTP-porttinumero**-kenttään porttinumero.</span><span class="sxs-lookup"><span data-stu-id="11a66-139">In the **SMTP port number** field, enter the port number.</span></span> <span data-ttu-id="11a66-140">(Jos et käytä Secure Sockets Layer \[SSL\]-suojausta, oletusportin numero on **25**.)</span><span class="sxs-lookup"><span data-stu-id="11a66-140">(If you aren't using Secure Sockets Layer \[SSL\], the default port number is **25**.)</span></span>
1. <span data-ttu-id="11a66-141">Jos todennus on pakollinen, kirjoita arvot **Käyttäjänimi**- ja **Salasana**-kenttiin.</span><span class="sxs-lookup"><span data-stu-id="11a66-141">If authentication is required, enter values in the **User name** and **Password** fields.</span></span>
1. <span data-ttu-id="11a66-142">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="11a66-142">Select **Save**.</span></span>
1. <span data-ttu-id="11a66-143">Valitse **Päivitä**.</span><span class="sxs-lookup"><span data-stu-id="11a66-143">Select **Refresh**.</span></span>
1. <span data-ttu-id="11a66-144">Valitse **Testaa sähköposti** -välilehdellä **Sähköpostipalvelu**-kentässä **SMTP**.</span><span class="sxs-lookup"><span data-stu-id="11a66-144">On the **Test email** tab, in the **Email provider** field, select **SMTP**.</span></span>
1. <span data-ttu-id="11a66-145">Kirjoita **Lähetä**-kenttään sähköpostiosoite, johon testisähköpostiviesti tulee toimittaa.</span><span class="sxs-lookup"><span data-stu-id="11a66-145">In the **Send to** field, enter the email address that the test email should be delivered to.</span></span>
1. <span data-ttu-id="11a66-146">Valitse **Lähetä testisähköpostiviesti**.</span><span class="sxs-lookup"><span data-stu-id="11a66-146">Select **Send test email**.</span></span>

## <a name="configure-email-templates"></a><span data-ttu-id="11a66-147">Sähköpostimallien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="11a66-147">Configure email templates</span></span>

<span data-ttu-id="11a66-148">Jokaista tapahtumaa kohti, josta haluat lähettää sähköposteja, on päivitettävä sähköpostimalli, jossa on sallittu lähettäjän sähköpostiosoite.</span><span class="sxs-lookup"><span data-stu-id="11a66-148">For each transactional event that you want to send emails for, you must update the email template with a valid sender email address.</span></span>

1. <span data-ttu-id="11a66-149">Kirjaudu sisään Commercen pääkonttoriversioon.</span><span class="sxs-lookup"><span data-stu-id="11a66-149">Sign in to Commerce headquarters.</span></span>
1. <span data-ttu-id="11a66-150">Valitse vasemman valikon avulla **Moduulit \> Retail ja Commerce \> Pääkonttorin asetukset \> Parametrit \> Organisaation sähköpostimallit**.</span><span class="sxs-lookup"><span data-stu-id="11a66-150">Use the menu on the left to go to **Modules \> Retail and Commerce \> Headquarters setup \> Parameters \> Organization email templates**.</span></span>
1. <span data-ttu-id="11a66-151">Valitse **Näytä luettelo**.</span><span class="sxs-lookup"><span data-stu-id="11a66-151">Select **Show list**.</span></span>
1. <span data-ttu-id="11a66-152">Luo kukin luettelossa oleva malli seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="11a66-152">For each template in the list, follow these steps:</span></span>

    1. <span data-ttu-id="11a66-153">Kirjoita **Lähettäjän sähköpostiosoite** -kenttään lähettäjän sähköpostiosoite.</span><span class="sxs-lookup"><span data-stu-id="11a66-153">In the **Sender email** field, enter the sender email address.</span></span>
    1. <span data-ttu-id="11a66-154">Valinnainen: Kirjoita **Lähettäjän nimi** -kenttään nimi, jota käytetään lähettäjän nimenä.</span><span class="sxs-lookup"><span data-stu-id="11a66-154">Optional: In the **Sender name** field, enter the name that should be used as the sender name.</span></span>

1. <span data-ttu-id="11a66-155">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="11a66-155">Select **Save**.</span></span>

## <a name="customize-email-templates"></a><span data-ttu-id="11a66-156">Mukauta sähköpostimalleja</span><span class="sxs-lookup"><span data-stu-id="11a66-156">Customize email templates</span></span>

<span data-ttu-id="11a66-157">Haluat ehkä mukauttaa sähköpostimalleja niin, että ne käyttävät eri kuvia.</span><span class="sxs-lookup"><span data-stu-id="11a66-157">You might want to customize the email templates so that they use different images.</span></span> <span data-ttu-id="11a66-158">Tai haluat ehkä päivittää mallien linkit niin, että ne menevät arviointiympäristöön.</span><span class="sxs-lookup"><span data-stu-id="11a66-158">Or you might want to update the links in the templates so that they go to your evaluation environment.</span></span> <span data-ttu-id="11a66-159">Tässä menettelyssä kerrotaan, miten oletusmallit ladataan ja mukautetaan ja miten järjestelmän mallit päivitetään.</span><span class="sxs-lookup"><span data-stu-id="11a66-159">This procedure explains how to download the default templates, customize them, and update the templates in the system.</span></span>

1. <span data-ttu-id="11a66-160">Lataa selaimessa [Microsoft Dynamics 365 Commerce -arviointisovelluksen oletussähköpostimallien zip-tiedosto](https://download.microsoft.com/download/d/7/b/d7b6c4d4-fe09-4922-9551-46bbb29d202d/Commerce.Preview.Default.Email.Templates.zip) paikalliseen tietokoneeseen.</span><span class="sxs-lookup"><span data-stu-id="11a66-160">In a web browser, download the [Microsoft Dynamics 365 Commerce Evaluation default email templates zip file](https://download.microsoft.com/download/d/7/b/d7b6c4d4-fe09-4922-9551-46bbb29d202d/Commerce.Preview.Default.Email.Templates.zip) to your local computer.</span></span> <span data-ttu-id="11a66-161">Tämä tiedosto sisältää seuraavat HTML-asiakirjat:</span><span class="sxs-lookup"><span data-stu-id="11a66-161">This file contains the following HTML documents:</span></span>

    - <span data-ttu-id="11a66-162">Tilauksen vahvistuksen malli</span><span class="sxs-lookup"><span data-stu-id="11a66-162">Order confirmation template</span></span>
    - <span data-ttu-id="11a66-163">Lahjakorttimallin lähettäminen</span><span class="sxs-lookup"><span data-stu-id="11a66-163">Issue gift card template</span></span>
    - <span data-ttu-id="11a66-164">Uusi tilausmalli</span><span class="sxs-lookup"><span data-stu-id="11a66-164">New order template</span></span>
    - <span data-ttu-id="11a66-165">Pakkaustilauksen malli</span><span class="sxs-lookup"><span data-stu-id="11a66-165">Pack order template</span></span>
    - <span data-ttu-id="11a66-166">Keräystilauksen malli</span><span class="sxs-lookup"><span data-stu-id="11a66-166">Pick order template</span></span>

1. <span data-ttu-id="11a66-167">Mukauta malleja teksti- tai HTML-editorin avulla.</span><span class="sxs-lookup"><span data-stu-id="11a66-167">Customize the templates by using a text or HTML editor.</span></span> <span data-ttu-id="11a66-168">Katso [tuettujen tunnusten](#supported-tokens-in-the-email-template) luettelo myöhemmin tässä ohjeaiheessa.</span><span class="sxs-lookup"><span data-stu-id="11a66-168">See the list of [supported tokens](#supported-tokens-in-the-email-template) later in this topic.</span></span>
1. <span data-ttu-id="11a66-169">Kirjaudu sisään Commerce-sovellukseen.</span><span class="sxs-lookup"><span data-stu-id="11a66-169">Sign in to Commerce.</span></span>
1. <span data-ttu-id="11a66-170">Siirry vasemmalla olevan valikon avulla kohtaan **Moduulit \> Organisaation hallinta \> Asetukset \> Organisaation sähköpostimallit**.</span><span class="sxs-lookup"><span data-stu-id="11a66-170">Use the menu on the left to go to **Modules \> Organization administration \> Setup \> Organization email templates**.</span></span>
1. <span data-ttu-id="11a66-171">Laajenna vasemmanpuoleista luetteloa, niin näet kaikki mallit.</span><span class="sxs-lookup"><span data-stu-id="11a66-171">Expand the list on the left to see all the templates.</span></span>
1. <span data-ttu-id="11a66-172">Noudata seuraavia vaiheita jokaiselle mukautettavan mallin kohdalle:</span><span class="sxs-lookup"><span data-stu-id="11a66-172">For each template that you want to customize, follow these steps:</span></span>

    1. <span data-ttu-id="11a66-173">Valitse luettelossa oleva malli.</span><span class="sxs-lookup"><span data-stu-id="11a66-173">Select the template in the list.</span></span>
    1. <span data-ttu-id="11a66-174">Valitse **Sähköpostiviestin sisältö** -kohdassa soveltuva kieliversio luettelosta.</span><span class="sxs-lookup"><span data-stu-id="11a66-174">Under **Email message content**, select the appropriate language version in the list.</span></span> <span data-ttu-id="11a66-175">(Oletuskieli on **fi-fi**.)</span><span class="sxs-lookup"><span data-stu-id="11a66-175">(The default language is **en-us**.)</span></span>
    1. <span data-ttu-id="11a66-176">Valitse **Sähköpostiviestin sisältö** -kohdassa **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="11a66-176">Under **Email message content**, select **Edit**.</span></span> <span data-ttu-id="11a66-177">**Lataa sähköpostimalli** -ruutu tulee näkyviin.</span><span class="sxs-lookup"><span data-stu-id="11a66-177">The **Upload email template** pane appears.</span></span>
    1. <span data-ttu-id="11a66-178">Valitse **Selaa** ja Etsi HTML-tiedosto, jolla on mukautettu sisältö.</span><span class="sxs-lookup"><span data-stu-id="11a66-178">Select **Browse**, and find the HTML file that has the customized content.</span></span>
    1. <span data-ttu-id="11a66-179">Valitse **Lataa palvelimeen**.</span><span class="sxs-lookup"><span data-stu-id="11a66-179">Select **Upload**.</span></span> <span data-ttu-id="11a66-180">Malli ladataan järjestelmään ja näkyviin tulee esikatselu.</span><span class="sxs-lookup"><span data-stu-id="11a66-180">The template is uploaded into the system, and a preview is shown.</span></span>
    1. <span data-ttu-id="11a66-181">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="11a66-181">Select **OK**.</span></span>
    1. <span data-ttu-id="11a66-182">Valinnainen: Mukauta mallin **Aihe**-ominaisuutta.</span><span class="sxs-lookup"><span data-stu-id="11a66-182">Optional: Customize the **Subject** property of the template.</span></span>
    1. <span data-ttu-id="11a66-183">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="11a66-183">Select **Save**.</span></span>

### <a name="supported-tokens-in-the-email-template"></a><span data-ttu-id="11a66-184">Sähköpostimallin tuetut tunnukset</span><span class="sxs-lookup"><span data-stu-id="11a66-184">Supported tokens in the email template</span></span>

<span data-ttu-id="11a66-185">Kun sähköposti lähetetään, nämä tunnukset korvataan todellisilla arvoilla, jotka koskevat asiakasta ja asiakkaan tilausta.</span><span class="sxs-lookup"><span data-stu-id="11a66-185">When the email is rendered, these tokens are replaced with actual values that apply to the customer and the customer's order.</span></span>

#### <a name="sales-order"></a><span data-ttu-id="11a66-186">Myyntitilaus</span><span class="sxs-lookup"><span data-stu-id="11a66-186">Sales order</span></span>

<span data-ttu-id="11a66-187">Seuraavat tunnukset koskevat yleistä myyntitilausta.</span><span class="sxs-lookup"><span data-stu-id="11a66-187">The following tokens apply to the overall sales order.</span></span>

| <span data-ttu-id="11a66-188">Tunnuksen nimi</span><span class="sxs-lookup"><span data-stu-id="11a66-188">Name of the token</span></span> | <span data-ttu-id="11a66-189">Tunnus</span><span class="sxs-lookup"><span data-stu-id="11a66-189">Token</span></span> |
|-------------------|-------|
| <span data-ttu-id="11a66-190">Tilauksen numero</span><span class="sxs-lookup"><span data-stu-id="11a66-190">Order number</span></span>      | <span data-ttu-id="11a66-191">%salesid%</span><span class="sxs-lookup"><span data-stu-id="11a66-191">%salesid%</span></span> |
| <span data-ttu-id="11a66-192">Asiakkaan nimi</span><span class="sxs-lookup"><span data-stu-id="11a66-192">Customer's name</span></span>   | <span data-ttu-id="11a66-193">%customername%</span><span class="sxs-lookup"><span data-stu-id="11a66-193">%customername%</span></span> |
| <span data-ttu-id="11a66-194">Toimitusosoite</span><span class="sxs-lookup"><span data-stu-id="11a66-194">Delivery address</span></span>  | <span data-ttu-id="11a66-195">%deliveryaddress%</span><span class="sxs-lookup"><span data-stu-id="11a66-195">%deliveryaddress%</span></span> |
| <span data-ttu-id="11a66-196">Laskutusosoite</span><span class="sxs-lookup"><span data-stu-id="11a66-196">Billing address</span></span>   | <span data-ttu-id="11a66-197">%customeraddress%</span><span class="sxs-lookup"><span data-stu-id="11a66-197">%customeraddress%</span></span> |
| <span data-ttu-id="11a66-198">Tilauspäivämäärä</span><span class="sxs-lookup"><span data-stu-id="11a66-198">Order date</span></span>        | <span data-ttu-id="11a66-199">%shipdate%</span><span class="sxs-lookup"><span data-stu-id="11a66-199">%shipdate%</span></span> |
| <span data-ttu-id="11a66-200">Toimitustapa</span><span class="sxs-lookup"><span data-stu-id="11a66-200">Delivery mode</span></span>     | <span data-ttu-id="11a66-201">%modeofdelivery%</span><span class="sxs-lookup"><span data-stu-id="11a66-201">%modeofdelivery%</span></span> |
| <span data-ttu-id="11a66-202">Alennus</span><span class="sxs-lookup"><span data-stu-id="11a66-202">Discount</span></span>          | <span data-ttu-id="11a66-203">%discount%</span><span class="sxs-lookup"><span data-stu-id="11a66-203">%discount%</span></span> |
| <span data-ttu-id="11a66-204">Arvonlisävero</span><span class="sxs-lookup"><span data-stu-id="11a66-204">Sales tax</span></span>         | <span data-ttu-id="11a66-205">%tax%</span><span class="sxs-lookup"><span data-stu-id="11a66-205">%tax%</span></span> |
| <span data-ttu-id="11a66-206">Tilauksen kokonaissumma</span><span class="sxs-lookup"><span data-stu-id="11a66-206">Order total</span></span>       | <span data-ttu-id="11a66-207">%total%</span><span class="sxs-lookup"><span data-stu-id="11a66-207">%total%</span></span> |

#### <a name="sales-line"></a><span data-ttu-id="11a66-208">Myyntirivi</span><span class="sxs-lookup"><span data-stu-id="11a66-208">Sales line</span></span>

<span data-ttu-id="11a66-209">Seuraavat tunnukset korvataan arvoilla jokaisessa tuotteessa tilauksessa.</span><span class="sxs-lookup"><span data-stu-id="11a66-209">The following tokens are replaced with values for each product in the order.</span></span>

> [!NOTE]
> <span data-ttu-id="11a66-210">Sijoita **Tuoteluettelo - aloitus** -tunnus jokaiselle tuotteelle toistetun HTML-lohkon alkuun ja sijoita **Tuoteluettelo - lopetus** -tunnus lohkon loppuun.</span><span class="sxs-lookup"><span data-stu-id="11a66-210">Put the **Product list - start** token at the beginning of the HTML block that is repeated for every product, and put the **Product list - end** token at the end of the block.</span></span>

| <span data-ttu-id="11a66-211">Tunnuksen nimi</span><span class="sxs-lookup"><span data-stu-id="11a66-211">Name of the token</span></span>      | <span data-ttu-id="11a66-212">Tunnus</span><span class="sxs-lookup"><span data-stu-id="11a66-212">Token</span></span> |
|------------------------|-------|
| <span data-ttu-id="11a66-213">Tuoteluettelo - alku</span><span class="sxs-lookup"><span data-stu-id="11a66-213">Product list - start</span></span>   | \<!--%tablebegin.salesline% --\> |
| <span data-ttu-id="11a66-214">Tuoteluettelo - loppu</span><span class="sxs-lookup"><span data-stu-id="11a66-214">Product list - end</span></span>     | \<!--%tableend.salesline%--\> |
| <span data-ttu-id="11a66-215">Tuotteen nimi</span><span class="sxs-lookup"><span data-stu-id="11a66-215">Product name</span></span>           | <span data-ttu-id="11a66-216">%lineproductname%</span><span class="sxs-lookup"><span data-stu-id="11a66-216">%lineproductname%</span></span> |
| <span data-ttu-id="11a66-217">kuvaus</span><span class="sxs-lookup"><span data-stu-id="11a66-217">Description</span></span>            | <span data-ttu-id="11a66-218">%lineproductdescription%</span><span class="sxs-lookup"><span data-stu-id="11a66-218">%lineproductdescription%</span></span> |
| <span data-ttu-id="11a66-219">Määrä</span><span class="sxs-lookup"><span data-stu-id="11a66-219">Quantity</span></span>               | <span data-ttu-id="11a66-220">%linequantity%</span><span class="sxs-lookup"><span data-stu-id="11a66-220">%linequantity%</span></span> |
| <span data-ttu-id="11a66-221">Rivin yksikköhinta</span><span class="sxs-lookup"><span data-stu-id="11a66-221">Line unit price</span></span>        | <span data-ttu-id="11a66-222">%lineprice% (tarkista)</span><span class="sxs-lookup"><span data-stu-id="11a66-222">%lineprice% (verify)</span></span> |
| <span data-ttu-id="11a66-223">rivinimikkeen kokonaissumma</span><span class="sxs-lookup"><span data-stu-id="11a66-223">line item total</span></span>        | <span data-ttu-id="11a66-224">%linenetamount%</span><span class="sxs-lookup"><span data-stu-id="11a66-224">%linenetamount%</span></span> |
| <span data-ttu-id="11a66-225">rivin alennus</span><span class="sxs-lookup"><span data-stu-id="11a66-225">line discount</span></span>          | <span data-ttu-id="11a66-226">%linediscount%</span><span class="sxs-lookup"><span data-stu-id="11a66-226">%linediscount%</span></span> |
| <span data-ttu-id="11a66-227">Lähetyspäivä</span><span class="sxs-lookup"><span data-stu-id="11a66-227">Ship date</span></span>              | <span data-ttu-id="11a66-228">%lineshipdate%</span><span class="sxs-lookup"><span data-stu-id="11a66-228">%lineshipdate%</span></span> |
| <span data-ttu-id="11a66-229">Hankintamenetelmä</span><span class="sxs-lookup"><span data-stu-id="11a66-229">Procurement method</span></span>     | <span data-ttu-id="11a66-230">%linedeliverymode%</span><span class="sxs-lookup"><span data-stu-id="11a66-230">%linedeliverymode%</span></span> |
| <span data-ttu-id="11a66-231">toimitusosoite</span><span class="sxs-lookup"><span data-stu-id="11a66-231">delivery address</span></span>       | <span data-ttu-id="11a66-232">%linedeliveryaddress%</span><span class="sxs-lookup"><span data-stu-id="11a66-232">%linedeliveryaddress%</span></span> |
| <span data-ttu-id="11a66-233">Rivin myyntiyksikkö</span><span class="sxs-lookup"><span data-stu-id="11a66-233">Sales unit of the line</span></span> | <span data-ttu-id="11a66-234">%lineunit%</span><span class="sxs-lookup"><span data-stu-id="11a66-234">%lineunit%</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="11a66-235">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="11a66-235">Additional resources</span></span>

[<span data-ttu-id="11a66-236">Dynamics 365 Commerce -arviointiympäristön yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="11a66-236">Dynamics 365 Commerce evaluation environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="11a66-237">Dynamics 365 Commerce -arviointiympäristön valmisteleminen</span><span class="sxs-lookup"><span data-stu-id="11a66-237">Provision a Dynamics 365 Commerce evaluation environment</span></span>](provisioning-guide.md)

[<span data-ttu-id="11a66-238">Dynamics 365 Commerce -arviointiympäristön määritykset</span><span class="sxs-lookup"><span data-stu-id="11a66-238">Configure a Dynamics 365 Commerce evaluation environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="11a66-239">BOPIS:n määritykset Dynamics 365 Commerce -arviointiympäristössä</span><span class="sxs-lookup"><span data-stu-id="11a66-239">Configure BOPIS in a Dynamics 365 Commerce evaluation environment</span></span>](cpe-bopis.md)

[<span data-ttu-id="11a66-240">Dynamics 365 Commerce -arviointiympäristön usein kysytyt kysymykset</span><span class="sxs-lookup"><span data-stu-id="11a66-240">Dynamics 365 Commerce evaluation environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="11a66-241">Microsoft Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="11a66-241">Microsoft Lifecycle Services (LCS)</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="11a66-242">Retail Cloud Scale Unit (RCSU)</span><span class="sxs-lookup"><span data-stu-id="11a66-242">Retail Cloud Scale Unit (RCSU)</span></span>](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="11a66-243">Microsoft Azure -portaali</span><span class="sxs-lookup"><span data-stu-id="11a66-243">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="11a66-244">Dynamics 365 Commerce -sivusto</span><span class="sxs-lookup"><span data-stu-id="11a66-244">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)


[!INCLUDE[footer-include](../includes/footer-banner.md)]