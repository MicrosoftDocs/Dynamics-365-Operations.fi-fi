---
title: Brasilian sähköisen laskutuksen lisäosan käytön aloittaminen
description: Tässä aiheessa on tietoja, joiden avulla voit aloittaa Brasilian sähköisen laskutuksen lisäosan käytön Microsoft Dynamics 365 Financessa ja Dynamics 365 Supply Chain Managementissa.
author: gionoder
manager: AnnBe
ms.date: 09/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 6472672f5d618cc6d100298dd35939afa4c0066d
ms.sourcegitcommit: 025561f6a21fe8705493daa290f3f6bfb9f1b962
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/23/2020
ms.locfileid: "3835950"
---
# <a name="get-started-with-the-electronic-invoicing-add-on-for-brazil"></a><span data-ttu-id="26f58-103">Brasilian sähköisen laskutuksen lisäosan käytön aloittaminen</span><span class="sxs-lookup"><span data-stu-id="26f58-103">Get started with the Electronic invoicing add-on for Brazil</span></span> 

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

> [!IMPORTANT]
> <span data-ttu-id="26f58-104">Brasilian sähköisen laskutuksen lisäosa ei tällä hetkellä tue kaikkia toimintoja, jotka ovat käytettävissä veroasiakirjan integroinnissa Microsoft Dynamics 365 Financeen ja Dynamics 365 Supply Chain Managementiin.</span><span class="sxs-lookup"><span data-stu-id="26f58-104">The Electronic invoicing add-on for Brazil doesn't currently support all the functions that are available in the fiscal document integration that is built into Microsoft Dynamics 365 Finance and Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="26f58-105">Tässä aiheessa on tietoja, joiden avulla voit aloittaa Brasilian sähköisen laskutuksen lisäosan käytön.</span><span class="sxs-lookup"><span data-stu-id="26f58-105">This topic provides information that will help you get started with the Electronic invoicing add-on for Brazil.</span></span> <span data-ttu-id="26f58-106">Se opastaa Regulatory Configuration Servicesin (RCS), Financen ja Supply Chain Managementin maakohtaisissa määritysvaiheissa.</span><span class="sxs-lookup"><span data-stu-id="26f58-106">It guides you through the configuration steps that are country-dependent in Regulatory Configuration Services (RCS) and in Finance and Supply Chain Management.</span></span> <span data-ttu-id="26f58-107">Se opastaa myös NF-e-veroasiakirjan (sähköinen veroasiakirjamalli 55) lähettämisessä palvelun kautta ja selittää, miten käsittelyn tulokset ja veroasiakirjojen tila arvioidaan.</span><span class="sxs-lookup"><span data-stu-id="26f58-107">It also guides you through the process of submitting an NF-e fiscal document (Electronic fiscal document model 55) through the service, and it explains how review the processing results and the status of the fiscal documents.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="26f58-108">Edellytykset</span><span class="sxs-lookup"><span data-stu-id="26f58-108">Prerequisites</span></span>

<span data-ttu-id="26f58-109">Ennen kuin suoritat tämän aiheen vaiheet, sinun on suoritettava aiheen [Sähköisen laskutuksen lisäosan käytön aloittaminen](e-invoicing-get-started.md) vaiheet.</span><span class="sxs-lookup"><span data-stu-id="26f58-109">Before you complete the steps in this topic, you must complete the steps in [Get started with the Electronic invoicing add-on](e-invoicing-get-started.md).</span></span>

## <a name="rcs-setup"></a><span data-ttu-id="26f58-110">RCS-asetukset</span><span class="sxs-lookup"><span data-stu-id="26f58-110">RCS setup</span></span>

<span data-ttu-id="26f58-111">RCS:n määrityksen aikana suoritat seuraavat tehtävät:</span><span class="sxs-lookup"><span data-stu-id="26f58-111">During the RCS setup, you will complete these tasks:</span></span>

1. <span data-ttu-id="26f58-112">NF-e-veroasiakirjojen sähköisen laskutuksen toiminnon tuonti.</span><span class="sxs-lookup"><span data-stu-id="26f58-112">Import the e-Invoicing feature for NF-e fiscal documents.</span></span>
2. <span data-ttu-id="26f58-113">Niiden tiedostomuotojen tarkistaminen, joita edellytetään NF-e-veroasiakirjojen hyväksyttäväksi lähettämisessä.</span><span class="sxs-lookup"><span data-stu-id="26f58-113">Review the file formats that are required to submit NF-e fiscal documents for authorization.</span></span>
3. <span data-ttu-id="26f58-114">Niiden tiedostomuotojen tarkistaminen, joita edellytetään hyväksytyn NF-e-veroasiakirjan peruuttamiseen.</span><span class="sxs-lookup"><span data-stu-id="26f58-114">Review the file formats that are required to request the cancellation of an approved NF-e.</span></span>
4. <span data-ttu-id="26f58-115">Sen tapahtuman määrittäminen, joka vaaditaan NF-e-veroasiakirjojen hyväksyttäväksi lähettämisessä.</span><span class="sxs-lookup"><span data-stu-id="26f58-115">Configure the event that is required to submit NF-e fiscal documents for authorization.</span></span>
5. <span data-ttu-id="26f58-116">Sen tapahtuman määrittäminen, jota edellytetään hyväksytyn NF-e-veroasiakirjan peruuttamiseen.</span><span class="sxs-lookup"><span data-stu-id="26f58-116">Configure the event that is required to request the cancellation of an approved NF-e.</span></span>
6. <span data-ttu-id="26f58-117">Sähköisen laskutuksen toiminnon määrittäminen sähköisen laskutuksen lisäosaympäristölle.</span><span class="sxs-lookup"><span data-stu-id="26f58-117">Assign the e-Invoicing feature to an Electronic invoicing add-on environment.</span></span>
7. <span data-ttu-id="26f58-118">Sähköisen laskutuksen toiminnon julkaiseminen.</span><span class="sxs-lookup"><span data-stu-id="26f58-118">Publish the e-Invoicing feature.</span></span>

> [!NOTE]
> <span data-ttu-id="26f58-119">Sähköisen laskutuksen toiminto on sen resurssin yleinen nimi, joka määritetään ja julkaistaan käytettäväksi sähköisen laskutuksen lisäosan palvelimella.</span><span class="sxs-lookup"><span data-stu-id="26f58-119">"The e-Invoicing feature" is the generic name for the resource that is configured and published to consume the Electronic invoicing add-on server.</span></span> <span data-ttu-id="26f58-120">Sähköisen laskutuksen toiminnon määrityksessä yhdistyvät muun muassa sähköisen raportoinnin (ER) määrityksen muodot määritettävien vienti- ja tuontitiedostojen luomista varten sekä toimintojen ja toimintokulkujen käyttäminen määritettävien pyyntöjen lähettämisen sääntöjen luomiseen, vastausten tuomiseen sekä vastausten sisältöjen jäsentämiseen.</span><span class="sxs-lookup"><span data-stu-id="26f58-120">The setup of the e-Invoicing feature combines, among other things, the use of Electronic reporting (ER) configuration formats to create configurable export and import files, and the use of actions and actions flows to enable the creation of configurable rules to send requests, import responses, and parse the response contents.</span></span>

## <a name="import-the-e-invoicing-feature"></a><span data-ttu-id="26f58-121">Sähköisen laskutuksen toiminnon tuominen</span><span class="sxs-lookup"><span data-stu-id="26f58-121">Import the e-Invoicing feature</span></span>

1. <span data-ttu-id="26f58-122">Kirjaudu RCS-tilille</span><span class="sxs-lookup"><span data-stu-id="26f58-122">Sign in to your RCS account</span></span>
2. <span data-ttu-id="26f58-123">Valitse **Globalisointitoiminnot**-työtila ja **Toiminnot**-kohdan **Sähköinen laskutus** -ruutu.</span><span class="sxs-lookup"><span data-stu-id="26f58-123">In the **Globalization features** workspace, in the **Features** section, select the **e-Invoicing** tile.</span></span>
3. <span data-ttu-id="26f58-124">Valitse **Sähköisen laskutuksen toiminnot** -sivulla **Tuo** tuodaksesi NF-e-veroasiakirjan sähköisen laskutuksen toiminnon yleisestä säilöstä.</span><span class="sxs-lookup"><span data-stu-id="26f58-124">On the **e-Invoicing Features** page, select **Import** to import a NF-e fiscal document e-Invoicing feature from the Global repository.</span></span>

    ![Tuontipainike](media/e-Invoicing-services-get-started-BRA-Select-Import-e-Invoicing-feature.png)

4. <span data-ttu-id="26f58-126">Valitse NF-e-veroasiakirjan toiminto ja sitten **Tuo**.</span><span class="sxs-lookup"><span data-stu-id="26f58-126">Select the NF-e fiscal document feature, and then select **Import**.</span></span>

    ![NF-e-toiminnon tuominen](media/e-Invoicing-services-get-started-BRA-Select-Import-NF-e-feature.png)

### <a name="create-a-new-version-of-the-nf-e-fiscal-document-feature"></a><span data-ttu-id="26f58-128">Uuden versoin luominen NF-e-veroasiakirjan toiminnosta</span><span class="sxs-lookup"><span data-stu-id="26f58-128">Create a new version of the NF-e fiscal document feature</span></span>

- <span data-ttu-id="26f58-129">Valitse **Sähköisen laskutuksen toiminnot** -sivun **Versiot**-välilehdellä **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="26f58-129">On the **e-Invoicing Features** page, on the **Versions** tab, select **New**.</span></span>

![Uuden sähköisen laskutuksen toiminnon version lisääminen](media/e-Invoicing-services-get-started-BRA-Select-New-e-Invoicing-feature-version.png)

### <a name="update-the-configuration-version"></a><span data-ttu-id="26f58-131">Määritysversion päivittäminen</span><span class="sxs-lookup"><span data-stu-id="26f58-131">Update the configuration version</span></span>

1. <span data-ttu-id="26f58-132">Voit hallita määritysversioita (ER-tiedostomuodon määrityksiä) valitsemalla **Sähköisen laskutuksen toiminnot** -sivun **Määritykset**-välilehdessä **Lisää** tai **Poista**.</span><span class="sxs-lookup"><span data-stu-id="26f58-132">On the **e-Invoicing Features** page, on the **Configurations** tab, select **Add** or **Delete** to manage the configuration versions (ER file format configurations).</span></span>

    ![Sähköisen laskutuksen toimintojen määritysten hallinta](media/e-Invoicing-services-get-started-BRA-Manage-e-Invoicing-feature-configurations.png)

    - <span data-ttu-id="26f58-134">Kun luot uuden version NF-e-veroasiakirjan toiminnosta, kaikki määritysversiot (ER-tiedostomuodot) periytyvät uusimmasta versiosta.</span><span class="sxs-lookup"><span data-stu-id="26f58-134">When you create a new version of the NF-e fiscal document feature, all configuration version (ER file formats) are inherited from the latest version.</span></span>
    - <span data-ttu-id="26f58-135">NF-e-veroasiakirjan lähettäminen hyväksyttäväksi edellyttää seuraavia määritysversioita:</span><span class="sxs-lookup"><span data-stu-id="26f58-135">To submit the NF-e fiscal document for authorization, the following configuration versions are required:</span></span>

        - <span data-ttu-id="26f58-136">NFe-lähetyksen vientimuoto</span><span class="sxs-lookup"><span data-stu-id="26f58-136">NFe submit export format</span></span>
        - <span data-ttu-id="26f58-137">NFe-vastaussanoman tuonti</span><span class="sxs-lookup"><span data-stu-id="26f58-137">NFe response message import</span></span>
        - <span data-ttu-id="26f58-138">NFe-virhelokin tuonti</span><span class="sxs-lookup"><span data-stu-id="26f58-138">NFe error log import</span></span>

    - <span data-ttu-id="26f58-139">NF-e-peruutuksen lähettäminen edellyttää seuraavaa määritysversiota:</span><span class="sxs-lookup"><span data-stu-id="26f58-139">To submit the NF-e cancellation, the following configuration version is required:</span></span>

        - <span data-ttu-id="26f58-140">NFe-peruutuksen vientimuoto</span><span class="sxs-lookup"><span data-stu-id="26f58-140">NFe cancel export format</span></span>

2. <span data-ttu-id="26f58-141">Valitse luettelosta määritysversio ja valitse sitten **Muokkaa** tai **Näytä** avataksesi **Muodon suunnittelija** -sivun, jolla voit muokata tai tarkastella määritystä.</span><span class="sxs-lookup"><span data-stu-id="26f58-141">In the list, select a configuration version, and then select **Edit** or **View** to open the **Format designer** page, where you can edit or view the configuration.</span></span>

    ![Muodon suunnittelija -sivun avaaminen](media/e-Invoicing-services-get-started-BRA-Configuration-ER-fomat-designer.png)

3. <span data-ttu-id="26f58-143">Käytä **Muodon suunnittelija** -sivua muokataksesi tai tarkastellaksesi ER-muodon tiedostomäärityksiä.</span><span class="sxs-lookup"><span data-stu-id="26f58-143">Use the **Format designer** page to edit or view the ER format file configurations.</span></span> <span data-ttu-id="26f58-144">Lisätietoja on kohdassa [Sähköisten asiakirjojen määritysten luominen](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/electronic-reporting-configuration)</span><span class="sxs-lookup"><span data-stu-id="26f58-144">For more information, see [Create electronic document configurations](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/electronic-reporting-configuration).</span></span>

    ![Muodon suunnittelutoiminto -sivu](media/e-Invoicing-services-get-started-BRA-ER-Format-designer.png)

### <a name="manage-the-e-invoicing-feature-setups"></a><span data-ttu-id="26f58-146">Sähköisen laskutuksen toiminnon määritysten hallinta</span><span class="sxs-lookup"><span data-stu-id="26f58-146">Manage the e-Invoicing feature setups</span></span>

- <span data-ttu-id="26f58-147">Voit hallita sähköisen laskutuksen toiminnon määrityksiä (eli NF-e-tapahtumia) valitsemalla **Sähköisen laskutuksen toiminnot** -sivun **Määritykset**-välilehdessä **Lisää** tai **Poista**.</span><span class="sxs-lookup"><span data-stu-id="26f58-147">On the **e-Invoicing Features** page, on the **Setups** tab, select **Add** or **Delete** to manage the e-Invoicing feature setups (that is, NF-e events).</span></span>

![Sähköisen laskutuksen toiminnon määritysten hallinta](media/e-Invoicing-services-get-started-BRA-Manage-e-Invoicing-feature-setup.png)

<span data-ttu-id="26f58-149">Kun luot uuden version NF-e-veroasiakirjan toiminnosta, joka on johdettu toisesta sähköisen laskutuksen toiminnosta, kaikki toiminnon määritykset (NF-e-tapahtumat) periytyvät uusimmasta versiosta.</span><span class="sxs-lookup"><span data-stu-id="26f58-149">When you create a new version of the NF-e fiscal document feature that is derived from another e-Invoicing feature, all feature setups (NF-e events) are inherited from the latest version.</span></span>

<span data-ttu-id="26f58-150">NF-e-veroasiakirjojen hyväksyttäväksi lähettäminen edellyttää **Lähetä**-toimintamääritystä.</span><span class="sxs-lookup"><span data-stu-id="26f58-150">To submit NF-e fiscal documents for authorization, the **Submit** feature setup is required.</span></span>

<span data-ttu-id="26f58-151">NF-e-peruutuksen lähettäminen edellyttää **Peruutus**-toimintomääritystä</span><span class="sxs-lookup"><span data-stu-id="26f58-151">To submit NF-e cancellation, the **Cancellation** feature setup is required.</span></span>

#### <a name="configure-the-submit-feature-setup"></a><span data-ttu-id="26f58-152">Lähetä-toimintomäärityksen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="26f58-152">Configure the Submit feature setup</span></span>

1. <span data-ttu-id="26f58-153">Valitse **Sähköisen laskutuksen toiminnot** -sivun **Määritykset**-välilehden **Toiminnon määritys** -sarakkeessa **Lähetä**.</span><span class="sxs-lookup"><span data-stu-id="26f58-153">On the **e-Invoicing Features** page, on the **Setups** tab, in the **Feature setup** column, select **Submit**.</span></span>
2. <span data-ttu-id="26f58-154">Valitse **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="26f58-154">Select **Edit**.</span></span>

    ![Sähköisen laskutuksen toiminnon muokkaaminen](media/e-Invoicing-services-get-started-BRA-Edit-e-Invoicing-feature-setup.png)

3. <span data-ttu-id="26f58-156">Voit hallita toimiluetteloa valitsemalla **Toimintoversion määritys** -sivulla **Toimet**-välilehti.</span><span class="sxs-lookup"><span data-stu-id="26f58-156">On the **Feature version setup** page, select the **Actions** tab to manage the list of actions.</span></span>

    ![Toimet-välilehti](media/e-Invoicing-services-get-started-BRA-Select-Actions.png)

4. <span data-ttu-id="26f58-158">Niiden toimien tarkistaminen, joita edellytetään NF-e-veroasiakirjojen hyväksyttäväksi lähettämisessä.</span><span class="sxs-lookup"><span data-stu-id="26f58-158">Review the actions that are required to submit an NF-e for authorization.</span></span>

    | <span data-ttu-id="26f58-159">Toimenpiteen tunnus</span><span class="sxs-lookup"><span data-stu-id="26f58-159">Action ID</span></span> | <span data-ttu-id="26f58-160">Toiminnon nimi</span><span class="sxs-lookup"><span data-stu-id="26f58-160">Action name</span></span>                  | <span data-ttu-id="26f58-161">Toiminnon kuvaus</span><span class="sxs-lookup"><span data-stu-id="26f58-161">Action description</span></span>                                                |
    |-----------|------------------------------|-------------------------------------------------------------------|
    | <span data-ttu-id="26f58-162">1</span><span class="sxs-lookup"><span data-stu-id="26f58-162">1</span></span>         | <span data-ttu-id="26f58-163">Muunna asiakirja</span><span class="sxs-lookup"><span data-stu-id="26f58-163">Transform document</span></span>           | <span data-ttu-id="26f58-164">Luo NF-e-XML-tiedosto lähetystä varten.</span><span class="sxs-lookup"><span data-stu-id="26f58-164">Create the NF-e XML file for submission.</span></span>                          |
    | <span data-ttu-id="26f58-165">2</span><span class="sxs-lookup"><span data-stu-id="26f58-165">2</span></span>         | <span data-ttu-id="26f58-166">Allekirjoita tiedosto</span><span class="sxs-lookup"><span data-stu-id="26f58-166">Sign document</span></span>                | <span data-ttu-id="26f58-167">Käytä XML-tiedostossa digitaalista varmennetta.</span><span class="sxs-lookup"><span data-stu-id="26f58-167">Apply the digital certificate to the XML file.</span></span>                    |
    | <span data-ttu-id="26f58-168">3</span><span class="sxs-lookup"><span data-stu-id="26f58-168">3</span></span>         | <span data-ttu-id="26f58-169">Brasilian SEFAZ-palvelun kutsuminen</span><span class="sxs-lookup"><span data-stu-id="26f58-169">Call Brazilian SEFAZ service</span></span> | <span data-ttu-id="26f58-170">Lähetä allekirjoitettu XML-tiedosto verkkopalveluihin hyväksymistä varten.</span><span class="sxs-lookup"><span data-stu-id="26f58-170">Submit the signed XML file to the web services for authorization.</span></span> |
    | <span data-ttu-id="26f58-171">4</span><span class="sxs-lookup"><span data-stu-id="26f58-171">4</span></span>         | <span data-ttu-id="26f58-172">Käsittele vastaus</span><span class="sxs-lookup"><span data-stu-id="26f58-172">Process response</span></span>             | <span data-ttu-id="26f58-173">Vastaanota verkkopalvelun vastaus.</span><span class="sxs-lookup"><span data-stu-id="26f58-173">Get the web service response.</span></span>                                     |
    | <span data-ttu-id="26f58-174">5</span><span class="sxs-lookup"><span data-stu-id="26f58-174">5</span></span>         | <span data-ttu-id="26f58-175">Muunna asiakirja</span><span class="sxs-lookup"><span data-stu-id="26f58-175">Transform document</span></span>           | <span data-ttu-id="26f58-176">Jäsennä vastauksena saatavan tiedoston sisältö.</span><span class="sxs-lookup"><span data-stu-id="26f58-176">Parse the content of the file that is received as a response.</span></span>     |
    | <span data-ttu-id="26f58-177">6</span><span class="sxs-lookup"><span data-stu-id="26f58-177">6</span></span>         | <span data-ttu-id="26f58-178">Muunna asiakirja</span><span class="sxs-lookup"><span data-stu-id="26f58-178">Transform document</span></span>           | <span data-ttu-id="26f58-179">Luo XML-tiedosto lähetyksen tilan kyselemistä varten.</span><span class="sxs-lookup"><span data-stu-id="26f58-179">Create the XML file to inquire about status of the submission.</span></span>    |
    | <span data-ttu-id="26f58-180">7</span><span class="sxs-lookup"><span data-stu-id="26f58-180">7</span></span>         | <span data-ttu-id="26f58-181">Brasilian SEFAZ-palvelun kutsuminen</span><span class="sxs-lookup"><span data-stu-id="26f58-181">Call Brazilian SEFAZ service</span></span> | <span data-ttu-id="26f58-182">Lähetä XML-tiedosto, joka pyytää lähetystilaa.</span><span class="sxs-lookup"><span data-stu-id="26f58-182">Submit the XML file that requests the submission status.</span></span>          |
    | <span data-ttu-id="26f58-183">8</span><span class="sxs-lookup"><span data-stu-id="26f58-183">8</span></span>         | <span data-ttu-id="26f58-184">Käsittele vastaus</span><span class="sxs-lookup"><span data-stu-id="26f58-184">Process response</span></span>             | <span data-ttu-id="26f58-185">Vastaanota verkkopalvelun vastaus.</span><span class="sxs-lookup"><span data-stu-id="26f58-185">Get the web service response.</span></span>                                     |

#### <a name="set-up-the-url-for-sefaz-web-services"></a><span data-ttu-id="26f58-186">Määritä SEFAZ-verkkopalvelujen URL-osoite</span><span class="sxs-lookup"><span data-stu-id="26f58-186">Set up the URL for SEFAZ web services</span></span> 

1. <span data-ttu-id="26f58-187">Valitse **Toimet**-pikavälilehden **Toimet**-välilehden **Toiminnon versiomääritys** -sivulla **Kutsu Brasilian SEFAZ-palvelua** (toimitunnus **3**).</span><span class="sxs-lookup"><span data-stu-id="26f58-187">On the **Feature version setup** page, on the **Actions** tab, on the **Actions** FastTab, select **Call Brazilian SEFAZ service** (action ID **3**).</span></span>
2. <span data-ttu-id="26f58-188">Syötä **Parametrit**-pikavälilehden **URL-osoiteparametri**-kenttään NF-e-lähetyksen SEFAZ-verkkopalvelun URL-osoite.</span><span class="sxs-lookup"><span data-stu-id="26f58-188">On the **Parameters** FastTab, in the **URL address parameter** field, enter the URL of the SEFAZ web service for NF-e submission.</span></span>
3. <span data-ttu-id="26f58-189">Valitse **Toimet**-pikavälilehdessä **Kutsu Brasilian SEFAZ-palvelua** (toimitunnus **7**).</span><span class="sxs-lookup"><span data-stu-id="26f58-189">On the **Actions** FastTab, select **Call Brazilian SEFAZ service** (action ID **7**).</span></span>
4. <span data-ttu-id="26f58-190">Syötä **Parametrit**-pikavälilehden **URL-osoiteparametri**-kenttään NF-e-lähetyksen SEFAZ-verkkopalvelun URL-osoite.</span><span class="sxs-lookup"><span data-stu-id="26f58-190">On the **Parameters** FastTab, in the **URL address parameter** field, enter the URL of the SEFAZ web service for NF-e submission.</span></span>

#### <a name="configure-the-cancellation-feature-setup"></a><span data-ttu-id="26f58-191">Peruutus-toimintomäärityksen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="26f58-191">Configure the Cancellation feature setup</span></span>

1. <span data-ttu-id="26f58-192">Valitse **Sähköisen laskutuksen toiminnot** -sivun **Määritykset**-välilehden **Toiminnon määritys** -sarakkeessa **Peruuta**.</span><span class="sxs-lookup"><span data-stu-id="26f58-192">On the **e-Invoicing Features** page, on the **Setups** tab, in the **Feature setup** column, select **Cancellation**.</span></span>
2. <span data-ttu-id="26f58-193">Valitse **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="26f58-193">Select **Edit**.</span></span>
3. <span data-ttu-id="26f58-194">Voit hallita toimiluetteloa valitsemalla **Toimintoversion määritys** -sivulla **Toimet**-välilehti.</span><span class="sxs-lookup"><span data-stu-id="26f58-194">On the **Feature version setup** page, select the **Actions** tab to manage the list of actions.</span></span>
4. <span data-ttu-id="26f58-195">Niiden toimien tarkistaminen, joita edellytetään hyväksytyn NF-e-veroasiakirjan peruuttamiseen.</span><span class="sxs-lookup"><span data-stu-id="26f58-195">Review the actions that are required to request the cancellation of an approved NF-e.</span></span>

    | <span data-ttu-id="26f58-196">Toimenpiteen tunnus</span><span class="sxs-lookup"><span data-stu-id="26f58-196">Action ID</span></span> | <span data-ttu-id="26f58-197">Toiminnon nimi</span><span class="sxs-lookup"><span data-stu-id="26f58-197">Action name</span></span>                  | <span data-ttu-id="26f58-198">Toiminnon kuvaus</span><span class="sxs-lookup"><span data-stu-id="26f58-198">Action description</span></span>                                               |
    |-----------|------------------------------|------------------------------------------------------------------|
    | <span data-ttu-id="26f58-199">1</span><span class="sxs-lookup"><span data-stu-id="26f58-199">1</span></span>         | <span data-ttu-id="26f58-200">Muunna asiakirja</span><span class="sxs-lookup"><span data-stu-id="26f58-200">Transform document</span></span>           | <span data-ttu-id="26f58-201">Luo NF-e-XML-peruutustiedosto lähetystä varten.</span><span class="sxs-lookup"><span data-stu-id="26f58-201">Create the NF-e cancellation XML file for submission.</span></span>            |
    | <span data-ttu-id="26f58-202">2</span><span class="sxs-lookup"><span data-stu-id="26f58-202">2</span></span>         | <span data-ttu-id="26f58-203">Allekirjoita tiedosto</span><span class="sxs-lookup"><span data-stu-id="26f58-203">Sign document</span></span>                | <span data-ttu-id="26f58-204">Käytä XML-tiedostossa digitaalista varmennetta.</span><span class="sxs-lookup"><span data-stu-id="26f58-204">Apply the digital certificate to the XML file.</span></span>                   |
    | <span data-ttu-id="26f58-205">3</span><span class="sxs-lookup"><span data-stu-id="26f58-205">3</span></span>         | <span data-ttu-id="26f58-206">Brasilian SEFAZ-palvelun kutsuminen</span><span class="sxs-lookup"><span data-stu-id="26f58-206">Call Brazilian SEFAZ service</span></span> | <span data-ttu-id="26f58-207">Lähetä allekirjoitettu XML-tiedosto verkkopalveluihin peruuttamista varten.</span><span class="sxs-lookup"><span data-stu-id="26f58-207">Submit the signed XML file to the web services for cancellation.</span></span> |
    | <span data-ttu-id="26f58-208">4</span><span class="sxs-lookup"><span data-stu-id="26f58-208">4</span></span>         | <span data-ttu-id="26f58-209">Käsittele vastaus</span><span class="sxs-lookup"><span data-stu-id="26f58-209">Process response</span></span>             | <span data-ttu-id="26f58-210">Vastaanota verkkopalvelun vastaus.</span><span class="sxs-lookup"><span data-stu-id="26f58-210">Get the web service response.</span></span>                                    |

#### <a name="set-up-the-url-for-sefaz-web-services"></a><span data-ttu-id="26f58-211">Määritä SEFAZ-verkkopalvelujen URL-osoite</span><span class="sxs-lookup"><span data-stu-id="26f58-211">Set up the URL for SEFAZ web services</span></span>

1. <span data-ttu-id="26f58-212">Valitse **Toimet**-pikavälilehden **Toimet**-välilehden **Toiminnon versiomääritys** -sivulla **Kutsu Brasilian SEFAZ-palvelua** (toimitunnus **3**).</span><span class="sxs-lookup"><span data-stu-id="26f58-212">On the **Feature version setup** page, on the **Actions** tab, on the **Actions** FastTab, select **Call Brazilian SEFAZ service** (action ID **3**).</span></span>
2. <span data-ttu-id="26f58-213">Syötä **Parametrit**-pikavälilehden **URL-osoiteparametri**-kenttään SEFAZ-verkkopalvelun URL-osoite hyväksytyn NF-e-veroasiakirjan peruuttamista varten.</span><span class="sxs-lookup"><span data-stu-id="26f58-213">On the **Parameters** FastTab, in the **URL address parameter** field, enter the URL of the SEFAZ web service for cancellation of an approved NF-e.</span></span>

### <a name="make-an-e-invoicing-environment-available-and-assign-a-draft-version"></a><span data-ttu-id="26f58-214">Sähköisen laskutuksen ympäristön käyttöön ottaminen ja luonnosversion määrittäminen</span><span class="sxs-lookup"><span data-stu-id="26f58-214">Make an e-Invoicing environment available and assign a Draft version</span></span>

1. <span data-ttu-id="26f58-215">Valitse **Sähköisen laskutuksen toiminnot** -sivun **Ympäristöt**-välilehdellä **Ota käyttöön**.</span><span class="sxs-lookup"><span data-stu-id="26f58-215">On the **e-Invoicing Features** page, on the **Environments** tab, select **Enable**.</span></span>
2. <span data-ttu-id="26f58-216">Valitse ympäristö **Ympäristöt**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="26f58-216">In the **Environment** field, select the environment.</span></span>
3. <span data-ttu-id="26f58-217">Valitse **Voimaantulo**-kentässä päivämäärä, jona uusi ympäristö on tarkoitus ottaa käyttöön.</span><span class="sxs-lookup"><span data-stu-id="26f58-217">In the **Effective from** field, select the date when the environment should become effective.</span></span>
4. <span data-ttu-id="26f58-218">Valitse **Ota käyttöön**.</span><span class="sxs-lookup"><span data-stu-id="26f58-218">Select **Enable**.</span></span>

![Sähköisen laskutuksen ympäristön käyttöönotto](media/e-Invoicing-services-get-started-BRA-Enable-e-Invoicing-environment.png)

### <a name="change-the-status-to-completed"></a><span data-ttu-id="26f58-220">Version tilan muuttaminen valmiiksi</span><span class="sxs-lookup"><span data-stu-id="26f58-220">Change the status to Completed</span></span>

1. <span data-ttu-id="26f58-221">Valitse **Sähköisen laskutuksen toiminnot** -sivun **Versiot**-välilehdessä se sähköisen laskutuksen toiminto, jonka tilana on **Luonnos**.</span><span class="sxs-lookup"><span data-stu-id="26f58-221">On the **e-Invoicing Features** page, on the **Versions** tab, select the version of the e-Invoicing feature that has a status of **Draft**.</span></span>
2. <span data-ttu-id="26f58-222">Valitse **Muutoksen tila \> Viimeistele**.</span><span class="sxs-lookup"><span data-stu-id="26f58-222">Select **Change status \> Complete**.</span></span>

### <a name="change-the-status-to-publish"></a><span data-ttu-id="26f58-223">Version tilan muuttaminen muotoon Julkaise</span><span class="sxs-lookup"><span data-stu-id="26f58-223">Change the status to Publish</span></span>

1. <span data-ttu-id="26f58-224">Valitse **Sähköisen laskutuksen toiminnot** -sivun **Versiot**-välilehdessä se sähköisen laskutuksen toiminto, jonka tilana on **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="26f58-224">On the **e-Invoicing Features** page, on the **Versions** tab, select the version of the e-Invoicing feature that has a status of **Completed**.</span></span>
2. <span data-ttu-id="26f58-225">Valitse **Muuta tilaa \> Julkaise**.</span><span class="sxs-lookup"><span data-stu-id="26f58-225">Select **Change status \> Publish**.</span></span>

![Sähköisen laskutuksen toiminnon julkaiseminen](media/e-Invoicing-services-get-started-BRA-Publish-e-Invoicing-feature.png)

## <a name="set-up-electronic-invoicing-add-on-integration-in-finance-or-supply-chain-management"></a><span data-ttu-id="26f58-227">Sähköisen laskutuksen lisäosan integroinnin määrittäminen Financessa tai Supply Chain Managementissa</span><span class="sxs-lookup"><span data-stu-id="26f58-227">Set up Electronic invoicing add-on integration in Finance or Supply Chain Management</span></span>

<span data-ttu-id="26f58-228">Määrityksen aikana suoritat seuraavat tehtävät:</span><span class="sxs-lookup"><span data-stu-id="26f58-228">During setup, you will complete these tasks:</span></span>

1. <span data-ttu-id="26f58-229">NF-e Federal -toiminnon käyttöönotto Brasilian osalta.</span><span class="sxs-lookup"><span data-stu-id="26f58-229">Turn on the NF-e Federal feature for Brazil.</span></span>
2. <span data-ttu-id="26f58-230">Tuo tietty ER-tietomalli, ER-tietomallin yhdistämismääritys ja NF-e-veroasiakirjoja varten vaadittavat muodot.</span><span class="sxs-lookup"><span data-stu-id="26f58-230">Import the specific ER data model, the data model mapping, and the formats that are required for NF-e fiscal documents.</span></span>
3. <span data-ttu-id="26f58-231">ER-määrityksen tuonti ja niiden vastaustyyppien määrittäminen, jotka tarvitaan veroasiakirjan tilan päivittämiseen, kun lähetysprosessi palautetaan.</span><span class="sxs-lookup"><span data-stu-id="26f58-231">Import the ER configuration, and set up the response types that are required to update the status of the fiscal document after the submission process is returned.</span></span>

### <a name="turn-on-the-nf-e-federal-feature-for-brazil"></a><span data-ttu-id="26f58-232">NF-e Federal -toiminnon käyttöönotto Brasilian osalta</span><span class="sxs-lookup"><span data-stu-id="26f58-232">Turn on the NF-e Federal feature for Brazil</span></span>

1. <span data-ttu-id="26f58-233">Siirry kohtaan **Organisaation hallinta \> Määritys \> Sähköisten asiakirjojen parametrit**.</span><span class="sxs-lookup"><span data-stu-id="26f58-233">Go to **Organization administration \> Setup \> Electronic document parameters**.</span></span>
2. <span data-ttu-id="26f58-234">Valitse **Toiminnot**-välilehdellä **Ota käyttöön** -valintaruutu toimintoviitteen **BR00053** rivillä.</span><span class="sxs-lookup"><span data-stu-id="26f58-234">On the **Features** tab, select the **Enable** check box in the row for feature reference **BR00053**.</span></span>

### <a name="import-the-er-data-model-mapping-required-for-nf-e-fiscal-documents"></a><span data-ttu-id="26f58-235">NF-e-veroasiakirjojen edellyttämän ER-tietomallin yhdistämismäärityksen tuonti</span><span class="sxs-lookup"><span data-stu-id="26f58-235">Import the ER data model mapping required for NF-e fiscal documents</span></span>

1. <span data-ttu-id="26f58-236">Kirjaudu Financeen.</span><span class="sxs-lookup"><span data-stu-id="26f58-236">Sign in to Finance.</span></span>
2. <span data-ttu-id="26f58-237">Valitse **Sähköisen raportointi** -työtilan **Määrityslähteet** -osassa **Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="26f58-237">In the **Electronic reporting** workspace, in the **Configuration providers** section, select the **Microsoft** tile.</span></span> <span data-ttu-id="26f58-238">Varmista, että tämän määrityspalvelun arvoksi on määritetty **Aktiivinen**.</span><span class="sxs-lookup"><span data-stu-id="26f58-238">Make sure that this configuration provider is set to **Active**.</span></span> <span data-ttu-id="26f58-239">Tietoja palvelun arvon **Aktiivinen**-muotoon määrittämisestä: [Luo määrityspalveluja ja merkitse ne aktiiviseksi](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11).</span><span class="sxs-lookup"><span data-stu-id="26f58-239">For information about how to set a provider to **Active**, see [Create configuration providers and mark them as active](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11).</span></span>
3. <span data-ttu-id="26f58-240">Valitse **Säilöt**.</span><span class="sxs-lookup"><span data-stu-id="26f58-240">Select **Repositories**.</span></span>
4. <span data-ttu-id="26f58-241">Valitse **Yleinen resurssi \> Avaa**.</span><span class="sxs-lookup"><span data-stu-id="26f58-241">Select **Global resource \> Open**.</span></span>
5. <span data-ttu-id="26f58-242">Tuo **Veroasiakirjojen yhdistämismääritys** -määritykset.</span><span class="sxs-lookup"><span data-stu-id="26f58-242">Import **Fiscal documents mapping** configurations.</span></span>

### <a name="import-er-configurations-and-set-up-the-response-types-for-fiscal-documents"></a><span data-ttu-id="26f58-243">ER-määritysten tuominen ja veroasiakirjojen vastaustyyppien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="26f58-243">Import ER configurations and set up the response types for fiscal documents</span></span>

1. <span data-ttu-id="26f58-244">Valitse **Sähköisen raportointi** -työtilan **Määrityslähteet** -osassa **Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="26f58-244">In the **Electronic reporting** workspace, in the **Configuration providers** section, select the **Microsoft** tile.</span></span>
2. <span data-ttu-id="26f58-245">Valitse **Säilöt**.</span><span class="sxs-lookup"><span data-stu-id="26f58-245">Select **Repositories**.</span></span>
3. <span data-ttu-id="26f58-246">Valitse **Yleinen resurssi \> Avaa**.</span><span class="sxs-lookup"><span data-stu-id="26f58-246">Select **Global resource \> Open**.</span></span>
4. <span data-ttu-id="26f58-247">Tuo **NF-e-virhelokin tuonti (BR)**, **NF-e-vastausten tietotuonnin muoto (BR)** ja **NF-e-vastaussanoman tuonti (BR)**.</span><span class="sxs-lookup"><span data-stu-id="26f58-247">Import **NF-e error log import (BR)**, **NF-e response data import format (BR)**, and **NF-e response message import (BR)**.</span></span>
5. <span data-ttu-id="26f58-248">Siirry kohtaan **Organisaation hallinta \> Määritys \> Sähköisten asiakirjojen parametrit**.</span><span class="sxs-lookup"><span data-stu-id="26f58-248">Go to **Organization administration \> Setup \> Electronic document parameters**.</span></span>
6. <span data-ttu-id="26f58-249">Valitse **Sähköinen asiakirja** -välilehdellä **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="26f58-249">On the **Electronic document** tab, select **Add**.</span></span>
6. <span data-ttu-id="26f58-250">Syötä **Taulukon nimi** -kenttään **Veroasiakirjan otsikko**.</span><span class="sxs-lookup"><span data-stu-id="26f58-250">In the **Table name** field, enter **Fiscal document header**.</span></span>
7. <span data-ttu-id="26f58-251">Valitse **Asiakirjan konteksti** -kentässä **Asiakaslaskun kontekstimalli – veroasiakirjan konteksti**.</span><span class="sxs-lookup"><span data-stu-id="26f58-251">In the **Document context** field, select **Customer invoice context model – Fiscal document context**.</span></span>
8. <span data-ttu-id="26f58-252">Valitse **Vastaustyypit**.</span><span class="sxs-lookup"><span data-stu-id="26f58-252">Select **Response types**.</span></span>
9. <span data-ttu-id="26f58-253">Valitse **Uusi** ja sitten **Vastaustyyppi** -kentässä **Vastaus**.</span><span class="sxs-lookup"><span data-stu-id="26f58-253">Select **New**, and then, in the **Response type** field, select **Response**.</span></span>
10. <span data-ttu-id="26f58-254">Valitse **Lähetystila**-kentässä **Odottaa**.</span><span class="sxs-lookup"><span data-stu-id="26f58-254">In the **Submission status** field, select **Pending**.</span></span>
11. <span data-ttu-id="26f58-255">Valitse **Mallin yhdistämismääritys** -kentässä **Vastaussanoman tuontimuoto – mallin yhdistämismääritys vastaussanomasta**.</span><span class="sxs-lookup"><span data-stu-id="26f58-255">In the **Model mapping** field, select **Response message import format – Model mapping from response message**.</span></span>
12. <span data-ttu-id="26f58-256">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="26f58-256">Select **Save**.</span></span>
13. <span data-ttu-id="26f58-257">Valitse **Uusi** ja syötä sitten **Vastaustyyppi**-kenttään **ResponseData**.</span><span class="sxs-lookup"><span data-stu-id="26f58-257">Select **New**, and then, in the **Response type** field, enter **ResponseData**.</span></span>
14. <span data-ttu-id="26f58-258">Valitse **Lähetystila**-kentässä **Odottaa**.</span><span class="sxs-lookup"><span data-stu-id="26f58-258">In the **Submission status** field, select **Pending**.</span></span>
15. <span data-ttu-id="26f58-259">Valitse **Mallin yhdistämismääritys** -kentässä **NFe-vastaustietojen tuontimuoto – vastaustietojen tuonti**</span><span class="sxs-lookup"><span data-stu-id="26f58-259">In the **Model mapping** field, select **NFe response data import format – Response data import**.</span></span>
16. <span data-ttu-id="26f58-260">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="26f58-260">Select **Save**.</span></span>

## <a name="electronic-invoice-processing"></a><span data-ttu-id="26f58-261">Sähköisen laskun käsittely</span><span class="sxs-lookup"><span data-stu-id="26f58-261">Electronic invoice processing</span></span>

<span data-ttu-id="26f58-262">Financessa käsittelyn aikana suoritat seuraavat tehtävät:</span><span class="sxs-lookup"><span data-stu-id="26f58-262">During processing in Finance, you will complete these tasks:</span></span>

1. <span data-ttu-id="26f58-263">Veroasiakirjan lähettäminen sähköisen laskutuksen lisäosalla.</span><span class="sxs-lookup"><span data-stu-id="26f58-263">Submit a fiscal document through the Electronic invoicing add-on.</span></span>
2. <span data-ttu-id="26f58-264">Lähetyksen suorituslokien tarkasteleminen ja käsittelytulosten arvioiminen.</span><span class="sxs-lookup"><span data-stu-id="26f58-264">View the submission execution logs and review the results of processing.</span></span>
3. <span data-ttu-id="26f58-265">Veroasiakirjan peruutuksen lähettäminen sähköisen laskutuksen lisäosalla.</span><span class="sxs-lookup"><span data-stu-id="26f58-265">Submit the cancellation of a fiscal document through the Electronic invoicing add-on.</span></span>

### <a name="submit-nf-e-fiscal-documents-for-sefaz-authorization"></a><span data-ttu-id="26f58-266">NF-e-veroasiakirjojen lähettäminen SEFAZ:n hyväksyttäväksi</span><span class="sxs-lookup"><span data-stu-id="26f58-266">Submit NF-e fiscal documents for SEFAZ authorization</span></span> 

<span data-ttu-id="26f58-267">Kun olet ottanut käyttöön **Määritettävä sähköisen laskutuksen lisäosan integrointi** vanhaa prosessia NF-e-veroasiakirjojen hyväksyttäväksi lähettämiseen (**Vie/tuo NF-e-prosessi)** ei voi enää käyttää.</span><span class="sxs-lookup"><span data-stu-id="26f58-267">After you turn on the **Configurable Electronic invoicing add-on integration** feature, the old process for submitting NF-e fiscal documents for authorization (**Export/Import NF-e process**) can no longer be used.</span></span> <span data-ttu-id="26f58-268">Se korvataan uudella prosessilla, jonka nimi on **Lähetä sähköiset asiakirjat**.</span><span class="sxs-lookup"><span data-stu-id="26f58-268">It's replaced by a new process that is named **Submit electronic documents**.</span></span>

> [!NOTE]
> <span data-ttu-id="26f58-269">Varmista ennen jatkamista, että sinulla on vähintään yksi asiakkaan veroasiakirjamalli 55, jotka asiakkaan talousosasto on luonut.</span><span class="sxs-lookup"><span data-stu-id="26f58-269">Before you continue, make sure that you have one or more customer fiscal documents model 55 that were issued by the customer's fiscal establishment.</span></span> <span data-ttu-id="26f58-270">Näiden veroasiakirjojen suunnan on oltava **Lähtevä** ja tilan **Luotu**.</span><span class="sxs-lookup"><span data-stu-id="26f58-270">The direction for these fiscal documents must be set to **Outgoing**, and the status must be **Created**.</span></span> <span data-ttu-id="26f58-271">Lisätietoja [Asiakkaan veroasiakirjan luominen (Brasilia)](https://docs.microsoft.com/dynamics365/finance/localizations/tasks/br-00038-issuing-customer-fiscal-document).</span><span class="sxs-lookup"><span data-stu-id="26f58-271">For more information, see [Issue customer fiscal document (Brazil)](https://docs.microsoft.com/dynamics365/finance/localizations/tasks/br-00038-issuing-customer-fiscal-document).</span></span>

1. <span data-ttu-id="26f58-272">Siirry kohtaan **Organisaation hallinta \> Säännölliset \> Sähköiset asiakirjat \> Lähetä sähköisiä asiakirjoja**.</span><span class="sxs-lookup"><span data-stu-id="26f58-272">Go to **Organization administration \> Periodic \> Electronic documents \> Submit electronic documents**.</span></span>
2. <span data-ttu-id="26f58-273">Kun mikä tahansa asiakirja lähetetään ensimmäistä kertaa, määritä **Lähetä asiakirjat uudelleen** -asetukseksi aina **Ei**.</span><span class="sxs-lookup"><span data-stu-id="26f58-273">For the first submission of any document, always set the **Resubmit documents** option to **No**.</span></span> <span data-ttu-id="26f58-274">Jos sinun on lähetettävä asiakirja uudelleen palvelun kautta, määritä asetukseksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="26f58-274">If you must resubmit a document through the service, set this option to **Yes**.</span></span>
3. <span data-ttu-id="26f58-275">Valitse **Sisällytettävät tietueet** -pikavälilehdessä **Suodata** avataksesi **Kysely**-valintaruudun, jossa voit muodostaa kyselyn lähetettävien asiakirjojen valitsemista varten.</span><span class="sxs-lookup"><span data-stu-id="26f58-275">On the **Records to include** FastTab, select **Filter** to open the **Inquiry** dialog box, where you can build a query to select documents for submission.</span></span>
4. <span data-ttu-id="26f58-276">Valitse **Alue**-välilehdessä **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="26f58-276">On the **Range** tab, select **Add**.</span></span>
5. <span data-ttu-id="26f58-277">Valitse **Taulukko** -kentässä **Veroasiakirjan otsikko**.</span><span class="sxs-lookup"><span data-stu-id="26f58-277">In the **Table** field, select **Fiscal document header**.</span></span>
6. <span data-ttu-id="26f58-278">Valitse **Johdettu taulukko** -kentässä **Veroasiakirjan otsikko**.</span><span class="sxs-lookup"><span data-stu-id="26f58-278">In the **Derived table** field, select **Fiscal document header**.</span></span>
6. <span data-ttu-id="26f58-279">Valitse **Kenttä** -kentässä **Numero**.</span><span class="sxs-lookup"><span data-stu-id="26f58-279">In the **Field** field, select **Number**.</span></span>
7. <span data-ttu-id="26f58-280">Syötä **Perusteet**-kenttään lähetettävän veroasiakirjan numero.</span><span class="sxs-lookup"><span data-stu-id="26f58-280">In the **Criteria** field, enter the number of the fiscal document that should be submitted.</span></span>
8. <span data-ttu-id="26f58-281">Valitse **OK**, jotta voit sulkea **Kysely**-valintaikkunan.</span><span class="sxs-lookup"><span data-stu-id="26f58-281">Select **OK** to close the **Inquiry** dialog box.</span></span>
8. <span data-ttu-id="26f58-282">Lähetä valitut asiakirjat valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="26f58-282">Select **OK** to submit the selected documents.</span></span>

> [!NOTE]
> <span data-ttu-id="26f58-283">Kun yrität lähettää asiakirjan palvelun kautta ensimmäisen kerran, järjestelmä pyytää vahvistamaan yhteyden sähköisen laskutuksen lisäosaan.</span><span class="sxs-lookup"><span data-stu-id="26f58-283">During your first attempt to submit a document through the service, you will be prompted to confirm the connection with the Electronic invoicing add-on.</span></span> <span data-ttu-id="26f58-284">Valitse **Yhdistä sähköisten asiakirjojen lähetyspalveluun napsauttamalla tätä**.</span><span class="sxs-lookup"><span data-stu-id="26f58-284">Select **Click here to connect to Electronic Document Submission Service**.</span></span>

### <a name="view-all-submission-logs"></a><span data-ttu-id="26f58-285">Kaikkien lähetyslokien tarkastelu</span><span class="sxs-lookup"><span data-stu-id="26f58-285">View all submission logs</span></span>

<span data-ttu-id="26f58-286">Kun olet ottanut **Määritettävä sähköisen laskutuksen lisäosan integrointi** -toiminnon käyttöön, käytettävissä on uusi sivu, jolla voi seurata asiakirjan lähetysprosessia.</span><span class="sxs-lookup"><span data-stu-id="26f58-286">After you turn on the **Configurable Electronic invoicing add-on integration** feature, a new page is available that lets you follow up on the document submission process.</span></span> <span data-ttu-id="26f58-287">Voit käyttää tätä sivua kaikkien lähetettyjen asiakirjojen lähetyslokien tarkasteluun.</span><span class="sxs-lookup"><span data-stu-id="26f58-287">You can use this page to view the submission logs for all submitted documents.</span></span>

1. <span data-ttu-id="26f58-288">Siirry kohtaan **Organisaation hallinta \> Säännölliset \> Sähköiset asiakirjat \> Sähköisen asiakirjan lähetysloki**.</span><span class="sxs-lookup"><span data-stu-id="26f58-288">Go to **Organization administration \> Periodic \> Electronic documents \> Electronic document submission log**.</span></span>
2. <span data-ttu-id="26f58-289">Valitse **Asiakirjatyyppi**-kentässä **Veroasiakirjan otsikko** suodattaaksesi vain veroasiakirjoja.</span><span class="sxs-lookup"><span data-stu-id="26f58-289">In the **Document type** field, select **Fiscal document header** to filter for fiscal documents only.</span></span>
3. <span data-ttu-id="26f58-290">Valitse toimintoruudussa **Kyselyt \> Lähetystiedot** tarkastellaksesi lähetyksen toteutuslokien tietoja.</span><span class="sxs-lookup"><span data-stu-id="26f58-290">On the Action Pane, select **Inquiries \> Submission details** to view the details of the submission execution logs.</span></span>

![Lähetyslokitietojen tarkastelu](media/e-Invoicing-services-get-started-BRA-View-Submission-log-details.png)

> [!NOTE] 
> <span data-ttu-id="26f58-292">Muiden kuin NF-e-veroasiakirjojen osalta **Virhekoodi**-sarakkeessa näkyy SEFAZ-verkkopalvelujen palauttama palautuskoodi.</span><span class="sxs-lookup"><span data-stu-id="26f58-292">For NF-e fiscal documents, the **Error code** column shows the return code that was returned by SEFAZ web services.</span></span>

### <a name="view-submission-logs-through-the-fiscal-document-page"></a><span data-ttu-id="26f58-293">Lähetyslokien tarkasteleminen veroasiakirjan sivun kautta</span><span class="sxs-lookup"><span data-stu-id="26f58-293">View submission logs through the fiscal document page</span></span>

<span data-ttu-id="26f58-294">Kun otat **Määritettävä sähköisen laskutuksen lisäosan integrointi** -toiminnon käyttöön, voit myös tarkastella lähetyslokeja veroasiakirjojen sivun kautta.</span><span class="sxs-lookup"><span data-stu-id="26f58-294">After you turn on the **Configurable Electronic invoicing add-on integration** feature, you can also view the submission logs through the fiscal document page.</span></span>

1. <span data-ttu-id="26f58-295">Siirry kohtaan **Kirjanpito \> Kyselyt ja raportit \> Veroasiakirjat \> Kaikki veroasiakirjat**.</span><span class="sxs-lookup"><span data-stu-id="26f58-295">Go to **General ledger \> Inquiries and reports \> Fiscal documents \> All fiscal documents**.</span></span>
2. <span data-ttu-id="26f58-296">Valitse veroasiakirja, joka on lähetetty sähköisen laskutuksen lisäosan kautta.</span><span class="sxs-lookup"><span data-stu-id="26f58-296">Select a fiscal document that was previously submitted through the Electronic invoicing add-on.</span></span>
3. <span data-ttu-id="26f58-297">Valitse toimintoruudun **NF-e federal**-välilehdessä **Sähköisen asiakirjan loki**.</span><span class="sxs-lookup"><span data-stu-id="26f58-297">On the Action Pane, on the **NF-e federal** tab, select **Electronic document log**.</span></span>

![Lähetyslokien tarkasteleminen veroasiakirjan sivun kautta](media/e-Invoicing-services-get-started-BRA-View-Submission-log-from-Fiscal-document-viewer.png)

### <a name="submit-approved-nf-e-fiscal-documents-for-sefaz-cancellation"></a><span data-ttu-id="26f58-299">Hyväksyttyjen NF-e-veroasiakirjojen lähettäminen SEFAZ:n peruutettavaksi</span><span class="sxs-lookup"><span data-stu-id="26f58-299">Submit approved NF-e fiscal documents for SEFAZ cancellation</span></span>

<span data-ttu-id="26f58-300">Kun olet ottanut **Määritettävä sähköisen laskutuksen lisäosan integrointi** -toiminnon käyttöön, vanhaa NF-e-veroasiakirjojen peruutusprosessia ei voi enää käyttää.</span><span class="sxs-lookup"><span data-stu-id="26f58-300">After you turn on the **Configurable Electronic invoicing add-on integration** feature, the old process for canceling NF-e fiscal documents can no longer be used.</span></span> <span data-ttu-id="26f58-301">Se korvataan uudella peruutusprosessilla, joka on upotettu **Sähköisen asiakirjan lähetysloki** -sivulle.</span><span class="sxs-lookup"><span data-stu-id="26f58-301">It's replaced by a new cancellation process that is embedded on the **Electronic document submission log** page.</span></span>

> [!NOTE]
> <span data-ttu-id="26f58-302">Varmista, että olet suorittanut asiakkaan veroasiakirjan peruuttamisen hyväksytyn NF-e-veroasiakirjan osalta.</span><span class="sxs-lookup"><span data-stu-id="26f58-302">Make sure that you've run the cancellation of the customer fiscal document for an approved NF-e fiscal document.</span></span> <span data-ttu-id="26f58-303">Lisätietoja: [Asiakkaan veroasiakirjan peruuttaminen (Brasilia)](https://docs.microsoft.com/dynamics365/finance/localizations/latam-bra-cancel-customer-fiscal-documents).</span><span class="sxs-lookup"><span data-stu-id="26f58-303">For more information see, [Cancel customer fiscal document (Brazil)](https://docs.microsoft.com/dynamics365/finance/localizations/latam-bra-cancel-customer-fiscal-documents).</span></span>

1. <span data-ttu-id="26f58-304">Siirry kohtaan **Organisaation hallinta \> Säännölliset \> Sähköiset asiakirjat \> Sähköisen asiakirjan lähetysloki**.</span><span class="sxs-lookup"><span data-stu-id="26f58-304">Go to **Organization administration \> Periodic \> Electronic documents \> Electronic document submission log**.</span></span>
2. <span data-ttu-id="26f58-305">Valitse veroasiakirja ja valitse sitten **Funktiot \> Lähetä liittyvät lähetykset**.</span><span class="sxs-lookup"><span data-stu-id="26f58-305">Select the fiscal document, and then select **Functions \> Send related submissions**.</span></span>
3. <span data-ttu-id="26f58-306">Kirjoita liittyvän lähetyksen kuvaus ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="26f58-306">Enter a description for the related submission, and then select **OK**.</span></span>

### <a name="view-cancellation-submission-logs"></a><span data-ttu-id="26f58-307">Peruutusten lähetyslokien tarkastelu</span><span class="sxs-lookup"><span data-stu-id="26f58-307">View cancellation submission logs</span></span>

1. <span data-ttu-id="26f58-308">Siirry kohtaan **Organisaation hallinta \> Säännölliset \> Sähköiset asiakirjat \> Sähköisen asiakirjan lähetysloki**.</span><span class="sxs-lookup"><span data-stu-id="26f58-308">Go to **Organization administration \> Periodic \> Electronic documents \> Electronic document submission log**.</span></span>
2. <span data-ttu-id="26f58-309">Valitse **Asiakirjatyyppi**-kentässä **Veroasiakirjan otsikko** suodattaaksesi vain veroasiakirjoja.</span><span class="sxs-lookup"><span data-stu-id="26f58-309">In the **Document type** field, select **Fiscal document header** to filter for fiscal documents only.</span></span>
3. <span data-ttu-id="26f58-310">Valitse veroasiakirja ja valitse sitten toimintoruudussa **Tiedustelut \> Liittyvä lähetys**.</span><span class="sxs-lookup"><span data-stu-id="26f58-310">Select the fiscal document, and then, on the Action Pane, select **Inquiries \> Related submission**.</span></span>

    <span data-ttu-id="26f58-311">Liittyvät lähetykset ovat lähetyksiä, jotka liittyvät aiemmin luotuun päälähetykseen.</span><span class="sxs-lookup"><span data-stu-id="26f58-311">Related submissions are submissions that are related to a main submission that was made first.</span></span> <span data-ttu-id="26f58-312">Esimerkiksi tietyn NF-e-veroasiakirjan hyväksyvä lähetys on päälähetys.</span><span class="sxs-lookup"><span data-stu-id="26f58-312">For example, the submission that authorizes a specific NF-e is the main submission.</span></span> <span data-ttu-id="26f58-313">Lähetys, jossa pyydetään saman NF-e-veroasiakirjan peruuttamista SEFAZ:ssa on liittyvä lähetys.</span><span class="sxs-lookup"><span data-stu-id="26f58-313">The submission that requests the cancellation of the same NF-e in SEFAZ is a related submission.</span></span> <span data-ttu-id="26f58-314">Se on olemassa vain siksi, että sillä pyydetään toisella lähetyksellä suoritetun tehtävän peruuttamista.</span><span class="sxs-lookup"><span data-stu-id="26f58-314">It exists only because it's requesting the cancellation of the job that was done through another submission.</span></span>

    <span data-ttu-id="26f58-315">**Liittyvät lähetykset** -sivulla näkyvät kaikki liittyvät lähetykset ja niiden lähetystila tietyn veroasiakirjan osalta.</span><span class="sxs-lookup"><span data-stu-id="26f58-315">The **Related submissions** page shows all related submissions, and their submission status, for a given fiscal document.</span></span> <span data-ttu-id="26f58-316">Seuraavassa kuvassa ensimmäinen rivi edustaa lähetystä, joka pyysi veroasiakirjan hyväksymistä.</span><span class="sxs-lookup"><span data-stu-id="26f58-316">In the following illustration, the first line represents the submission that requested approval of the fiscal document.</span></span> <span data-ttu-id="26f58-317">Toinen rivi vastaa edustaa lähetystä, joka peruutti veroasiakirjan.</span><span class="sxs-lookup"><span data-stu-id="26f58-317">The second line represents the submission that canceled that fiscal document.</span></span>

    ![Peruutusten lähetyslokien tarkastelu](media/e-Invoicing-services-get-started-BRA-View-Cancellation-Submission-log.png)

4. <span data-ttu-id="26f58-319">Valitse toimintoruudussa **Kyselyt \> Lähetystiedot** tarkastellaksesi lähetyksen toteutuslokien tietoja.</span><span class="sxs-lookup"><span data-stu-id="26f58-319">On the Action Pane, select **Inquiries \> Submission details** to view the details of the submission execution logs.</span></span>

    ![Peruutusten lähetyslokitietojen tarkastelu](media/e-Invoicing-services-get-started-BRA-View-Cancellation-Submission-log-details.png)

## <a name="privacy-notice"></a><span data-ttu-id="26f58-321">Tietosuojatiedot</span><span class="sxs-lookup"><span data-stu-id="26f58-321">Privacy notice</span></span>
<span data-ttu-id="26f58-322">BR-00053 (NF-e Federal) -toiminnon käyttöönotto saattaa edellyttää rajoitettujen tietojen, joihin kuuluu organisaation verorekisteritunnus, lähettämistä.</span><span class="sxs-lookup"><span data-stu-id="26f58-322">Enabling the BR-00053 (NF-e Federal) feature may require sending limited data, which includes the organization tax registration ID.</span></span> <span data-ttu-id="26f58-323">Ne välitetään kolmannen osapuolen virastoille, jotka veroviranomaiset ovat hyväksyneet sähköisten laskujen kyseiselle veroviranomaiselle lähettämistä varten siinä esimääritetyssä muodossa, jota integrointi valtion verkkopalveluun edellyttää.</span><span class="sxs-lookup"><span data-stu-id="26f58-323">This will be transmitted to third-party agencies authorized by the tax authority for purposes of sending electronic invoices to this tax authority in the predefined format required for integration with the government’s web service.</span></span> <span data-ttu-id="26f58-324">Järjestelmänvalvoja voi ottaa toiminnon BR-00053 (NF-e Federal) -toiminnon käyttöön ja poistaa sen käytöstä siirtymällä kohtaan **Organisaation hallinta \> Määritykset \> Sähköisten asiakirjojen parametrit**.</span><span class="sxs-lookup"><span data-stu-id="26f58-324">An administrator can enable and disable the BR-00053 (NF-e Federal) feature by navigating to **Organization administration \> Setup \> Electronic document parameters**.</span></span> <span data-ttu-id="26f58-325">Valitse **Toiminnot**-välilehti, valitse toiminnon BR-00053 sisältävä rivi ja tee sitten haluamasi valinta.</span><span class="sxs-lookup"><span data-stu-id="26f58-325">Select the **Features** tab, select the row containing the BR-00053 feature, and then make the appropriate selection.</span></span> <span data-ttu-id="26f58-326">Näistä ulkoisista järjestelmistä tähän Dynamics 365 -verkkopalveluun tuotuihin tietoihin sovelletaan [tietosuojalausuntoamme](https://go.microsoft.com/fwlink/?LinkId=512132).</span><span class="sxs-lookup"><span data-stu-id="26f58-326">Data imported from these external systems into this Dynamics 365 online service are subject to our [privacy statement](https://go.microsoft.com/fwlink/?LinkId=512132).</span></span> <span data-ttu-id="26f58-327">Katso lisätietoja maakohtaisten toimintodokumentaatioiden tietosuojaosista.</span><span class="sxs-lookup"><span data-stu-id="26f58-327">Please consult the Privacy notice sections in country-specific feature documentation for more information.</span></span>


## <a name="additional-resources"></a><span data-ttu-id="26f58-328">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="26f58-328">Additional resources</span></span>

- [<span data-ttu-id="26f58-329">Sähköisen laskutuksen yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="26f58-329">Electronic invoicing add-on overview</span></span>](e-invoicing-service-overview.md)
- [<span data-ttu-id="26f58-330">Sähköisen laskutuksen lisäosan käytön aloittaminen</span><span class="sxs-lookup"><span data-stu-id="26f58-330">Get started with the Electronic invoicing add-on</span></span>](e-invoicing-get-started.md)
- [<span data-ttu-id="26f58-331">Sähköisen laskutuksen lisäosan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="26f58-331">Set up the Electronic invoicing add-on</span></span>](e-invoicing-setup.md)
