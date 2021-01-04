---
title: Meksikon sähköisen laskutuksen lisäosan käytön aloittaminen
description: Tässä aiheessa on tietoja, joiden avulla voit aloittaa Meksikon sähköisen laskutuksen lisäosan käytön Microsoft Dynamics 365 Financessa ja Dynamics 365 Supply Chain Managementissa.
author: gionoder
manager: AnnBe
ms.date: 09/22/2020
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
ms.openlocfilehash: 6d15a79a359b3c708b2b33893d700377a57c3eb7
ms.sourcegitcommit: cfd84321fba38e02e270d361df369a536a48efa3
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/11/2020
ms.locfileid: "4512231"
---
# <a name="get-started-with-the-electronic-invoicing-add-on-for-mexico"></a><span data-ttu-id="4ac8b-103">Meksikon sähköisen laskutuksen lisäosan käytön aloittaminen</span><span class="sxs-lookup"><span data-stu-id="4ac8b-103">Get started with the Electronic invoicing add-on for Mexico</span></span>

[!include [banner](../includes/banner.md)]

> [!IMPORTANT]
> <span data-ttu-id="4ac8b-104">Meksikon sähköisen laskutuksen lisäosa ei välttämättä tällä hetkellä tue kaikkia toimintoja, jotka ovat käytettävissä Comprobante Fiscal Digital por Internet (CFDI) -asiakirjassa tai siihen liittyvässä integroinnissa Microsoft Dynamics 365 Financeen tai Dynamics 365 Supply Chain Managementiin.</span><span class="sxs-lookup"><span data-stu-id="4ac8b-104">The Electronic invoicing add-on for Mexico might not currently support all the functions that are available in the Comprobante Fiscal Digital por Internet (CFDI) document, and in the related integration that is built into Microsoft Dynamics 365 Finance or Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="4ac8b-105">Tässä aiheessa on tietoja, joiden avulla voit aloittaa Meksikon sähköisen laskutuksen lisäosan käytön.</span><span class="sxs-lookup"><span data-stu-id="4ac8b-105">This topic provides information that will help you get started with the Electronic invoicing add-on for Mexico.</span></span> <span data-ttu-id="4ac8b-106">Se opastaa Regulatory Configuration Servicesin (RCS) ja Financen maakohtaisissa määritysvaiheissa.</span><span class="sxs-lookup"><span data-stu-id="4ac8b-106">It guides you through the configuration steps that are country-dependent in Regulatory Configuration Services (RCS) and Finance.</span></span> <span data-ttu-id="4ac8b-107">Saat myös ohjeita siihen, mitä sinun on tehtävä Financessa lähettääksesi CFDI-laskuja palvelulla, ja sinulle selitetään, miten käsittelyn tulokset ja CFDI-laskujen tila arvioidaan.</span><span class="sxs-lookup"><span data-stu-id="4ac8b-107">It also guides you through the steps that you must follow in Finance to submit CFDI invoices through the service, and it explains how to review the processing results and the status of CFDI invoices.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="4ac8b-108">Edellytykset</span><span class="sxs-lookup"><span data-stu-id="4ac8b-108">Prerequisites</span></span>

<span data-ttu-id="4ac8b-109">Ennen kuin suoritat tämän aiheen vaiheet, sinun on suoritettava aiheen [Sähköisen laskutuksen lisäosan käytön aloittaminen](e-invoicing-get-started.md) vaiheet.</span><span class="sxs-lookup"><span data-stu-id="4ac8b-109">Before you complete the steps in this topic, you must complete the steps in [Get started with the Electronic invoicing add-on](e-invoicing-get-started.md).</span></span>

## <a name="rcs-setup"></a><span data-ttu-id="4ac8b-110">RCS-asetukset</span><span class="sxs-lookup"><span data-stu-id="4ac8b-110">RCS setup</span></span>

<span data-ttu-id="4ac8b-111">RCS:n määrityksen aikana suoritat seuraavat tehtävät:</span><span class="sxs-lookup"><span data-stu-id="4ac8b-111">During the RCS setup, you will complete these tasks:</span></span>

1. <span data-ttu-id="4ac8b-112">Tuo sähköisen laskutuksen toiminto CFDI-laskujen käsittelyyn.</span><span class="sxs-lookup"><span data-stu-id="4ac8b-112">Import the e-Invoicing feature for processing CFDI invoices.</span></span>
2. <span data-ttu-id="4ac8b-113">Tarkista muotomääritykset, jotka vaaditaan CFID-laskuja koskevien vastausten luomiseen, lähettämiseen ja vastaanottamiseen sekä peruutuksia koskevien vastausten lähettämiseen ja vastaanottamiseen.</span><span class="sxs-lookup"><span data-stu-id="4ac8b-113">Review the format configurations that are required to generate, submit, and receive responses about CFDI invoices, and to submit and receive responses about cancellation.</span></span>
3. <span data-ttu-id="4ac8b-114">Määritä tapahtumat, jotka tukevat CFDI-laskun lähetysskenaarioita.</span><span class="sxs-lookup"><span data-stu-id="4ac8b-114">Configure the events that support the CFDI invoice submission scenarios.</span></span>
4. <span data-ttu-id="4ac8b-115">Julkaise CFDI-laskujen sähköisen laskutuksen toiminto.</span><span class="sxs-lookup"><span data-stu-id="4ac8b-115">Publish the e-Invoicing feature for CFDI invoices.</span></span>

> [!NOTE]
> <span data-ttu-id="4ac8b-116">Sähköisen laskutuksen toiminto on sen resurssin yleinen nimi, joka määritetään ja julkaistaan käytettäväksi sähköisen laskutuksen lisäosan palvelimella.</span><span class="sxs-lookup"><span data-stu-id="4ac8b-116">"The e-Invoicing feature" is the generic name for the resource that is configured and published to consume the Electronic invoicing add-on server.</span></span> <span data-ttu-id="4ac8b-117">Tässä tapauksessa CFDI-laskut (MX) ovat määritettävä sähköisen laskutuksen toiminto.</span><span class="sxs-lookup"><span data-stu-id="4ac8b-117">In this case, CFDI invoices (MX) are the e-Invoicing feature that you will set up.</span></span>

## <a name="import-the-e-invoicing-feature"></a><span data-ttu-id="4ac8b-118">Sähköisen laskutuksen toiminnon tuominen</span><span class="sxs-lookup"><span data-stu-id="4ac8b-118">Import the e-Invoicing feature</span></span>

1. <span data-ttu-id="4ac8b-119">Kirjaudu RCS-tilille.</span><span class="sxs-lookup"><span data-stu-id="4ac8b-119">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="4ac8b-120">Valitse **Globalisointitoiminnot**-työtila ja **Toiminnot**-kohdan **Sähköinen laskutus** -ruutu.</span><span class="sxs-lookup"><span data-stu-id="4ac8b-120">In the **Globalization features** workspace, in the **Features** section, select the **e-Invoicing** tile.</span></span>
3. <span data-ttu-id="4ac8b-121">Valitse **Sähköisen laskutuksen toiminnot** -sivulla **Tuo** tuodaksesi **CFDI-laskut (MX)** -toiminnon yleisestä säilöstä.</span><span class="sxs-lookup"><span data-stu-id="4ac8b-121">On the **e-Invoicing Features** page, select **Import** to import the **CFDI invoices (MX)** feature from the Global repository.</span></span>

    > [!NOTE]
    > <span data-ttu-id="4ac8b-122">Jos toiminto ei näy luettelossa, valitse **Synkronoi** ja toista sitten vaihe 3.</span><span class="sxs-lookup"><span data-stu-id="4ac8b-122">If you don't see the feature in the list, select **Synchronize**, and then repeat step 3.</span></span>

![CFDI-laskujen (MX) tuominen](media/e-Invoicing-services-get-started-MEX-Select-Import-CFDI-feature.png)

<span data-ttu-id="4ac8b-124">Kun tuot **CFDI-laskut (MX)** -toiminnon yleisestä säilöstä, kaikki toiminnon asetukset, kuten määritykset ja toimet, tuodaan myös.</span><span class="sxs-lookup"><span data-stu-id="4ac8b-124">When you import the **CFDI invoices (MX)** feature from the Global repository, all the feature settings, including configurations and actions, are also imported.</span></span>

### <a name="create-a-new-version-of-the-cfdi-invoices-mx-feature"></a><span data-ttu-id="4ac8b-125">Uuden versoin luominen CFDI-laskujen (MX) toiminnosta</span><span class="sxs-lookup"><span data-stu-id="4ac8b-125">Create a new version of the CFDI invoices (MX) feature</span></span>

<span data-ttu-id="4ac8b-126">Voit luoda uuden version, jos esimerkiksi URL-osoitteita on päivitettävä.</span><span class="sxs-lookup"><span data-stu-id="4ac8b-126">You can create a new version if, for example, URLs must be updated.</span></span> <span data-ttu-id="4ac8b-127">Lisätietoja: [Sähköinen CFDI-laskutus](tasks/mx-00010-e-invoicing-cfdi.md).</span><span class="sxs-lookup"><span data-stu-id="4ac8b-127">For more information, see [E-invoicing CFDI](tasks/mx-00010-e-invoicing-cfdi.md).</span></span>

- <span data-ttu-id="4ac8b-128">Valitse **Sähköisen laskutuksen toiminnot** -sivun **Versiot**-välilehdellä **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="4ac8b-128">On the **e-Invoicing Features** page, on the **Versions** tab, select **New**.</span></span>

![Uuden sähköisen laskutuksen toiminnon version lisääminen](media/e-Invoicing-services-get-started-MEX-Select-New-e-Invoicing-feature.png)

### <a name="update-the-configuration-version"></a><span data-ttu-id="4ac8b-130">Määritysversion päivittäminen</span><span class="sxs-lookup"><span data-stu-id="4ac8b-130">Update the configuration version</span></span>

1. <span data-ttu-id="4ac8b-131">Voit hallita määritysversioita (ER-tiedostomuodon määrityksiä) valitsemalla **Sähköisen laskutuksen toiminnot** -sivun **Määritykset**-välilehdessä **Lisää** tai **Poista**.</span><span class="sxs-lookup"><span data-stu-id="4ac8b-131">On the **e-Invoicing Features** page, on the **Configurations** tab, select **Add** or **Delete** to manage the configuration versions (ER file format configurations).</span></span>

    ![Sähköisen laskutuksen toimintojen määritysten hallinta](media/e-Invoicing-services-get-started-MEX-Manage-e-Invoicing-feature-Configurations.png)

    <span data-ttu-id="4ac8b-133">Kun luot uuden version, kaikki määritykset periytyvät edellisestä julkaistusta versiosta.</span><span class="sxs-lookup"><span data-stu-id="4ac8b-133">When you create a new version, all configurations are inherited from the last published version.</span></span> <span data-ttu-id="4ac8b-134">CFDI-laskujen käsittelyä varten tarvitaan seuraavat määritykset:</span><span class="sxs-lookup"><span data-stu-id="4ac8b-134">To process CFDI invoices, the following configurations are required:</span></span>

    - <span data-ttu-id="4ac8b-135">CFDI-lasku (BusinessDocumentService)</span><span class="sxs-lookup"><span data-stu-id="4ac8b-135">CFDI invoice (BusinessDocumentService)</span></span>
    - <span data-ttu-id="4ac8b-136">CFDI-vastaussanoman tuonti</span><span class="sxs-lookup"><span data-stu-id="4ac8b-136">CFDI response message import</span></span>
    - <span data-ttu-id="4ac8b-137">CFDI-virhelokin tuonti</span><span class="sxs-lookup"><span data-stu-id="4ac8b-137">CFDI error log import</span></span>
    - <span data-ttu-id="4ac8b-138">CFDI-peruutuspyyntö (MX) (BusinessDocumentService)</span><span class="sxs-lookup"><span data-stu-id="4ac8b-138">CFDI cancelation request (MX) (BusinessDocumentService)</span></span>
    - <span data-ttu-id="4ac8b-139">CFDI-lasku (BusinessDocumentService)</span><span class="sxs-lookup"><span data-stu-id="4ac8b-139">CFDI invoice (BusinessDocumentService)</span></span>

2. <span data-ttu-id="4ac8b-140">Valitse luettelosta määritysversio ja valitse sitten **Muokkaa** tai **Näytä** avataksesi **Muodon suunnittelija** -sivun, jolla voit muokata tai tarkastella määritystä.</span><span class="sxs-lookup"><span data-stu-id="4ac8b-140">In the list, select a configuration version, and then select **Edit** or **View** to open the **Format designer** page, where you can edit or view the configuration.</span></span>

    ![Muodon suunnittelija -sivun avaaminen](media/e-Invoicing-services-get-started-MEX-Configuration-ER-format-designer.png)

3. <span data-ttu-id="4ac8b-142">Käytä **Muodon suunnittelija** -sivua muokataksesi ja tarkastellaksesi ER-muodon tiedostomäärityksiä.</span><span class="sxs-lookup"><span data-stu-id="4ac8b-142">Use the **Format designer** page to edit and view the ER format file configurations.</span></span> <span data-ttu-id="4ac8b-143">Lisätietoja on kohdassa [Sähköisten asiakirjojen määritysten luominen](../../dev-itpro/analytics/electronic-reporting-configuration.md)</span><span class="sxs-lookup"><span data-stu-id="4ac8b-143">For more information, see [Create electronic document configurations](../../dev-itpro/analytics/electronic-reporting-configuration.md).</span></span>

    ![Muodon suunnittelutoiminto -sivu](media/e-Invoicing-services-get-started-MEX-ER-format-designer.png)

## <a name="manage-the-e-invoicing-feature-setups"></a><span data-ttu-id="4ac8b-145">Sähköisen laskutuksen toiminnon määritysten hallinta</span><span class="sxs-lookup"><span data-stu-id="4ac8b-145">Manage the e-Invoicing feature setups</span></span>

- <span data-ttu-id="4ac8b-146">Voit hallita sähköisen laskutuksen toiminnon määrityksiä valitsemalla **Sähköisen laskutuksen toiminnot** -sivun **Määritykset**-välilehdessä **Lisää**, **Poista** tai **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="4ac8b-146">On the **e-Invoicing Features** page, on the **Setups** tab, select **Add**, **Delete**, or **Edit** to manage the e-Invoicing feature setups.</span></span>

![Sähköisen laskutuksen toiminnon määritysten hallinta](media/e-Invoicing-services-get-started-MEX-Manage-e-Invoicing-feature-Setup.png)

<span data-ttu-id="4ac8b-148">Jos haluat lähettää CFDI-laskuja hyväksyttäväksi (luoda XML-tiedoston, lähettää XML-tiedoston ja käsitellä vastauksen), tarvitaan **Myyntilasku**-toimintomääritys.</span><span class="sxs-lookup"><span data-stu-id="4ac8b-148">To submit CFDI invoices for authorization (generate the XML file, submit the XML file, and process the response), the **Sales invoice** feature setup is required.</span></span>

<span data-ttu-id="4ac8b-149">CFDI-laskun peruutuksen lähettämiseen vaaditaan toimintomääritykset **Peruutus** ja **Peruuta**.</span><span class="sxs-lookup"><span data-stu-id="4ac8b-149">To submit CFDI invoice cancellation, the **Cancellation** and **Cancel** feature setups are required.</span></span>

### <a name="configure-the-sales-invoice-feature-setup"></a><span data-ttu-id="4ac8b-150">Myyntilaskutoiminnon asetusten määrittäminen</span><span class="sxs-lookup"><span data-stu-id="4ac8b-150">Configure the Sales invoice feature setup</span></span>

1. <span data-ttu-id="4ac8b-151">Valitse **Sähköisen laskutuksen toiminnot** -sivun **Määritykset**-välilehden **Toiminnon määritys** -sarakkeessa **Myyntilasku**.</span><span class="sxs-lookup"><span data-stu-id="4ac8b-151">On the **e-Invoicing Features** page, on the **Setups** tab, in the **Feature setup** column, select **Sales invoice**.</span></span>
2. <span data-ttu-id="4ac8b-152">Määritä toimet, soveltuvuussäännöt ja muuttujat valitsemalla **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="4ac8b-152">Select **Edit** to configure the actions, applicability rules, and variables.</span></span>

    ![Sähköisen laskutuksen toiminnon määritysten muokkaaminen](media/e-Invoicing-services-get-started-MEX-Edit-e-Invoicing-feature-setup.png)

3. <span data-ttu-id="4ac8b-154">Voit hallita toimiluetteloa valitsemalla **Toimintoversion määritys** -sivulla **Toimet**-välilehti.</span><span class="sxs-lookup"><span data-stu-id="4ac8b-154">On the **Feature version setup** page, select the **Actions** tab to manage the list of actions.</span></span> <span data-ttu-id="4ac8b-155">Toimet määrittävät luettelon toiminnoista, jotka on suoritettava peräkkäisessä järjestyksessä, jotta toiminto suoritetaan kokonaisuudessaan.</span><span class="sxs-lookup"><span data-stu-id="4ac8b-155">Actions define a list of operations that must be run in sequential order to accomplish full execution of the event.</span></span>

    ![Toimet-välilehti](media/e-Invoicing-services-get-started-MEX-Select-Actions.png)

    | <span data-ttu-id="4ac8b-157">Toimenpiteen tunnus</span><span class="sxs-lookup"><span data-stu-id="4ac8b-157">Action ID</span></span> | <span data-ttu-id="4ac8b-158">Toimenpide</span><span class="sxs-lookup"><span data-stu-id="4ac8b-158">Action</span></span>                   | <span data-ttu-id="4ac8b-159">Toiminnon nimi</span><span class="sxs-lookup"><span data-stu-id="4ac8b-159">Action name</span></span>                                  | <span data-ttu-id="4ac8b-160">Toiminnon kuvaus</span><span class="sxs-lookup"><span data-stu-id="4ac8b-160">Action description</span></span>                                          |
    |-----------|--------------------------|----------------------------------------------|-------------------------------------------------------------|
    | <span data-ttu-id="4ac8b-161">1</span><span class="sxs-lookup"><span data-stu-id="4ac8b-161">1</span></span>         | <span data-ttu-id="4ac8b-162">Muunna asiakirja</span><span class="sxs-lookup"><span data-stu-id="4ac8b-162">Transform document</span></span>       | <span data-ttu-id="4ac8b-163">Luo sähköinen CFDI-lasku ilman digitaalista allekirjoitusta</span><span class="sxs-lookup"><span data-stu-id="4ac8b-163">Generate CFDI E-Invoice without digital sign</span></span> | <span data-ttu-id="4ac8b-164">Luo sähköinen CFDI-lasku.</span><span class="sxs-lookup"><span data-stu-id="4ac8b-164">Generate the CFDI e-invoice.</span></span>                                |
    | <span data-ttu-id="4ac8b-165">2</span><span class="sxs-lookup"><span data-stu-id="4ac8b-165">2</span></span>         | <span data-ttu-id="4ac8b-166">Allekirjoita tiedosto</span><span class="sxs-lookup"><span data-stu-id="4ac8b-166">Sign document</span></span>            | <span data-ttu-id="4ac8b-167">Digitaalinen allekirjoitus</span><span class="sxs-lookup"><span data-stu-id="4ac8b-167">Digital sign</span></span>                                 | <span data-ttu-id="4ac8b-168">Allekirjoita sähköinen lasku lähetystä varten digitaalisesti.</span><span class="sxs-lookup"><span data-stu-id="4ac8b-168">Digitally sign the e-invoice for submission.</span></span>                |
    | <span data-ttu-id="4ac8b-169">3</span><span class="sxs-lookup"><span data-stu-id="4ac8b-169">3</span></span>         | <span data-ttu-id="4ac8b-170">Kutsu Meksikon PAC-palvelua</span><span class="sxs-lookup"><span data-stu-id="4ac8b-170">Call Mexican PAC service</span></span> | <span data-ttu-id="4ac8b-171">Lähetä sähköinen CFDI-lasku</span><span class="sxs-lookup"><span data-stu-id="4ac8b-171">Submit CFDI E-Invoice</span></span>                        | <span data-ttu-id="4ac8b-172">Windows Communication Foundation (WCF) -asiakas lähettää sähköisen CFDI-laskun.</span><span class="sxs-lookup"><span data-stu-id="4ac8b-172">The Windows Communication Foundation (WCF) client submits the CFDI e-invoice.</span></span> |
    | <span data-ttu-id="4ac8b-173">4</span><span class="sxs-lookup"><span data-stu-id="4ac8b-173">4</span></span>         | <span data-ttu-id="4ac8b-174">Käsittele vastaus</span><span class="sxs-lookup"><span data-stu-id="4ac8b-174">Process response</span></span>         | <span data-ttu-id="4ac8b-175">Verkkopalvelun vastauksen analysoiminen</span><span class="sxs-lookup"><span data-stu-id="4ac8b-175">Analyze web service response</span></span>                 | <span data-ttu-id="4ac8b-176">Analysoi verkkopalvelun vastaus ja palauta virheloki.</span><span class="sxs-lookup"><span data-stu-id="4ac8b-176">Analyze the web service response, and return the error log.</span></span> |

### <a name="set-up-the-url-for-mexican-pac-web-services"></a><span data-ttu-id="4ac8b-177">Määritä Meksikon PAC-verkkopalvelujen URL-osoite</span><span class="sxs-lookup"><span data-stu-id="4ac8b-177">Set up the URL for Mexican PAC web services</span></span> 

1. <span data-ttu-id="4ac8b-178">Valitse **Toimet**-pikavälilehden **Toimet**-välilehden **Toiminnon versiomääritys**-sivulla **Kutsu Meksikon PAC-palvelua**.</span><span class="sxs-lookup"><span data-stu-id="4ac8b-178">On the **Feature version setup** page, on the **Actions** tab, on the **Actions** FastTab, select **Call Mexican PAC service**.</span></span>
2. <span data-ttu-id="4ac8b-179">Syötä **Parametrit**-pikavälilehden **URL-osoitteet**-kenttään CFDI-laskun lähetyksen verkkopalvelun URL-osoite.</span><span class="sxs-lookup"><span data-stu-id="4ac8b-179">On the **Parameters** FastTab, in the **URL address** field, enter the URL of the web service for CFDI invoice submission.</span></span>

> [!NOTE]
> <span data-ttu-id="4ac8b-180">Käytä samoja vaiheita toimintovaiheiden **Peruuta** ja **Peruutuspyyntö** **Kutsu Meksikon PAC-palvelua**-toiminnon URL-osoitteen päivittämiseen.</span><span class="sxs-lookup"><span data-stu-id="4ac8b-180">Use the same steps to update the URL for **Call Mexican PAC service** action for the **Cancel** and **Cancelation request** feature setups.</span></span>

## <a name="assign-the-draft-version-to-an-e-invoicing-environment"></a><span data-ttu-id="4ac8b-181">Luonnosversion määrittäminen sähköisen laskutuksen ympäristölle</span><span class="sxs-lookup"><span data-stu-id="4ac8b-181">Assign the Draft version to an e-Invoicing environment</span></span>

1. <span data-ttu-id="4ac8b-182">Valitse **Sähköisen laskutuksen toiminnot** -sivun **Ympäristöt**-välilehdellä **Ota käyttöön**.</span><span class="sxs-lookup"><span data-stu-id="4ac8b-182">On the **e-Invoicing Features** page, on the **Environments** tab, select **Enable**.</span></span>
2. <span data-ttu-id="4ac8b-183">Valitse ympäristö **Ympäristöt**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="4ac8b-183">In the **Environment** field, select the environment.</span></span>
3. <span data-ttu-id="4ac8b-184">Valitse **Voimaantulo**-kentässä päivämäärä, jona uusi ympäristö on tarkoitus ottaa käyttöön.</span><span class="sxs-lookup"><span data-stu-id="4ac8b-184">In the **Effective from** field, select the date when the environment should become effective.</span></span>
3. <span data-ttu-id="4ac8b-185">Valitse **Ota käyttöön**.</span><span class="sxs-lookup"><span data-stu-id="4ac8b-185">Select **Enable**.</span></span>

![Sähköisen laskutuksen ympäristön käyttöönotto](media/e-Invoicing-services-get-started-MEX-Enable-e-Invoicing-Environment.png)

## <a name="change-the-version-status-to-completed"></a><span data-ttu-id="4ac8b-187">Version tilan muuttaminen valmiiksi</span><span class="sxs-lookup"><span data-stu-id="4ac8b-187">Change the version status to Completed</span></span>

1. <span data-ttu-id="4ac8b-188">Valitse **Sähköisen laskutuksen toiminnot** -sivun **Versiot**-välilehdessä se sähköisen laskutuksen toiminto, jonka tilana on **Luonnos**.</span><span class="sxs-lookup"><span data-stu-id="4ac8b-188">On the **e-Invoicing Features** page, on the **Versions** tab, select the version of the e-Invoicing feature that has a status of **Draft**.</span></span>
2. <span data-ttu-id="4ac8b-189">Valitse **Muutoksen tila \> Viimeistele**.</span><span class="sxs-lookup"><span data-stu-id="4ac8b-189">Select **Change status \> Complete**.</span></span>

## <a name="change-the-version-status-to-published"></a><span data-ttu-id="4ac8b-190">Version tilan muuttaminen julkaistuksi</span><span class="sxs-lookup"><span data-stu-id="4ac8b-190">Change the version status to Published</span></span>

- <span data-ttu-id="4ac8b-191">Valitse **Sähköisen laskutuksen toiminnot**-sivun **Versiot**-välilehdellä **Muuta tilaa \> Julkaise**.</span><span class="sxs-lookup"><span data-stu-id="4ac8b-191">On the **e-Invoicing Features** page, on the **Versions** tab, select **Change status \> Publish**.</span></span>

## <a name="publish-the-e-invoicing-feature"></a><span data-ttu-id="4ac8b-192">Sähköisen laskutuksen toiminnon julkaiseminen</span><span class="sxs-lookup"><span data-stu-id="4ac8b-192">Publish the e-Invoicing feature</span></span>

1. <span data-ttu-id="4ac8b-193">Valitse **Sähköisen laskutuksen toiminnot** -sivulla **Versiot**-välilehti hallitaksesi **CFDI-laskut (MX)** -toiminnon tilaa.</span><span class="sxs-lookup"><span data-stu-id="4ac8b-193">On the **e-Invoicing Features** page, select the **Versions** tab to manage the status of the **CFDI invoices (MX)** feature.</span></span>
2. <span data-ttu-id="4ac8b-194">Muuta toiminnon tilaa valitsemalla **Muuta tilaa**.</span><span class="sxs-lookup"><span data-stu-id="4ac8b-194">Select **Change status** to change the status of the feature.</span></span>

![Sähköisen laskutuksen toiminnon tilan muuttaminen](media/e-Invoicing-services-get-started-MEX-Change-status-of-e-Invoicing-feature.png)

## <a name="set-up-electronic-invoicing-add-on-integration-in-finance"></a><span data-ttu-id="4ac8b-196">Sähköisen laskutuksen lisäosan integroinnin määritys Financessa</span><span class="sxs-lookup"><span data-stu-id="4ac8b-196">Set up Electronic invoicing add-on integration in Finance</span></span>

<span data-ttu-id="4ac8b-197">Sähköisen laskutuksen lisäosa määritetään Financessa suorittamalla seuraavat tehtävät:</span><span class="sxs-lookup"><span data-stu-id="4ac8b-197">To set up the Electronic invoicing add-on in Finance, you will complete these tasks:</span></span>

1. <span data-ttu-id="4ac8b-198">Tuo ER-tietomalli, ER-tietomallin yhdistämismääritys ja CFDI-laskuja varten vaadittavat muodot.</span><span class="sxs-lookup"><span data-stu-id="4ac8b-198">Import the ER data model, the ER data model mapping, and the formats that are required for CFDI invoices.</span></span>
2. <span data-ttu-id="4ac8b-199">Määritä CFDI-laskujen päivityksen vastaustyypit.</span><span class="sxs-lookup"><span data-stu-id="4ac8b-199">Configure response types for updating the CFDI invoices.</span></span> <span data-ttu-id="4ac8b-200">Näitä vastaustyyppejä käytetään vastaukseen hyväksytyn varmenteentarjoajan (PAC) palvelimelta.</span><span class="sxs-lookup"><span data-stu-id="4ac8b-200">These response types are used for the response from the authorized certification provider (PAC) server.</span></span>

### <a name="import-the-er-data-model-er-data-model-mapping-and-context-configurations-for-cfdi-invoices"></a><span data-ttu-id="4ac8b-201">Tuo ER-tietomalli, ER-tietomallin yhdistämismääritys ja CFDI-laskujen kontekstimääritykset</span><span class="sxs-lookup"><span data-stu-id="4ac8b-201">Import the ER data model, ER data model mapping, and context configurations for CFDI invoices</span></span>

1. <span data-ttu-id="4ac8b-202">Kirjaudu Financeen.</span><span class="sxs-lookup"><span data-stu-id="4ac8b-202">Sign in to Finance.</span></span>
2. <span data-ttu-id="4ac8b-203">Valitse **Sähköisen raportointi** -työtilan **Määrityslähteet** -osassa **Microsoft**-ruutu.</span><span class="sxs-lookup"><span data-stu-id="4ac8b-203">In the **Electronic reporting** workspace, in the **Configuration providers** section, select the **Microsoft** title.</span></span> <span data-ttu-id="4ac8b-204">Varmista, että tämän määrityspalvelun arvoksi on määritetty **Aktiivinen**.</span><span class="sxs-lookup"><span data-stu-id="4ac8b-204">Make sure that this configuration provider is set to **Active**.</span></span> <span data-ttu-id="4ac8b-205">Tietoja palvelun arvon **Aktiivinen**-muotoon määrittämisestä: [Luo määrityspalveluja ja merkitse ne aktiiviseksi](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11).</span><span class="sxs-lookup"><span data-stu-id="4ac8b-205">For information about how to set a provider to **Active**, see [Create configuration providers and mark them as active](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11).</span></span>
3. <span data-ttu-id="4ac8b-206">Valitse **Säilöt**.</span><span class="sxs-lookup"><span data-stu-id="4ac8b-206">Select **Repositories**.</span></span>
4. <span data-ttu-id="4ac8b-207">Valitse **Yleinen resurssi \> Avaa**.</span><span class="sxs-lookup"><span data-stu-id="4ac8b-207">Select **Global resource \> Open**.</span></span>
5. <span data-ttu-id="4ac8b-208">Tuo **Laskumalli**, **Laskumallin yhdistämismääritys**, **CFDI-laskun muoto (MX)**, **CFDI-laskun peruutuspyynnön muoto (MX)** sekä **CFDI-laskun peruutusmuoto (MX)**.</span><span class="sxs-lookup"><span data-stu-id="4ac8b-208">Import **Invoice model**, **Invoice model mapping**, **CFDI invoice format (MX)**, **CFDI invoice cancelation request format (MX)**, and **CFDI invoice cancel format (MX)**.</span></span>

### <a name="turn-on-the-feature-for-processing-cfdi-invoices"></a><span data-ttu-id="4ac8b-209">CFDI-laskujen käsittelytoiminnon käyttöönotto</span><span class="sxs-lookup"><span data-stu-id="4ac8b-209">Turn on the feature for processing CFDI invoices</span></span>

1. <span data-ttu-id="4ac8b-210">Siirry kohtaan **Organisaation hallinta \> Määritys \> Sähköisten asiakirjojen parametrit**.</span><span class="sxs-lookup"><span data-stu-id="4ac8b-210">Go to **Organization administration \> Setup \> Electronic document parameters**.</span></span>
2. <span data-ttu-id="4ac8b-211">Valitse **Toiminnot**-välilehdellä **Ota käyttöön** -valintaruutu toimintoviitteiden **MX-00010** ja **MX-00016** riveillä.</span><span class="sxs-lookup"><span data-stu-id="4ac8b-211">On the **Features** tab, select the **Enable** check box in the rows for feature references **MX-00010** and **MX-00016**.</span></span>

![CFDI-laskujen käsittelytoimintojen käyttöönotto](media/e-Invoicing-services-get-started-MEX-Enable-CFDI-feature.png)

### <a name="import-er-configurations-and-set-up-the-response-types-for-updating-cfdi-invoices"></a><span data-ttu-id="4ac8b-213">ER-määritysten tuominen ja CFDI-laskujen päivittämisen vastaustyyppien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="4ac8b-213">Import ER configurations and set up the response types for updating CFDI invoices</span></span>

#### <a name="import-er-configurations"></a><span data-ttu-id="4ac8b-214">ER-konfiguraatioiden tuominen</span><span class="sxs-lookup"><span data-stu-id="4ac8b-214">Import ER configurations</span></span>

1. <span data-ttu-id="4ac8b-215">Valitse **Sähköisen raportointi** -työtilan **Määrityslähteet** -osassa **Microsoft**-ruutu.</span><span class="sxs-lookup"><span data-stu-id="4ac8b-215">In the **Electronic reporting** workspace, in the **Configuration providers** section, select the **Microsoft** title.</span></span>
3. <span data-ttu-id="4ac8b-216">Valitse **Säilöt**.</span><span class="sxs-lookup"><span data-stu-id="4ac8b-216">Select **Repositories**.</span></span>
4. <span data-ttu-id="4ac8b-217">Valitse **Yleinen resurssi \> Avaa**.</span><span class="sxs-lookup"><span data-stu-id="4ac8b-217">Select **Global resource \> Open**.</span></span>
5. <span data-ttu-id="4ac8b-218">Tuo **Vastaussanomamalli**, **CFDI-virhelokin tuonti (MX)** ja **CFDI-vastaussanoman tuonti (MX)**.</span><span class="sxs-lookup"><span data-stu-id="4ac8b-218">Import **Response message model**, **CFDI error log import (MX)**, and **CFDI response message import (MX)**.</span></span>

#### <a name="set-up-the-response-types"></a><span data-ttu-id="4ac8b-219">Vastaustyyppien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="4ac8b-219">Set up the response types</span></span>

1. <span data-ttu-id="4ac8b-220">Siirry kohtaan **Organisaation hallinta \> Määritys \> Sähköisten asiakirjojen parametrit**.</span><span class="sxs-lookup"><span data-stu-id="4ac8b-220">Go to **Organization administration \> Setup \> Electronic document parameters**.</span></span>
2. <span data-ttu-id="4ac8b-221">Valitse **Sähköinen asiakirja** -välilehdellä **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="4ac8b-221">On the **Electronic document** tab, select **Add**.</span></span>
3. <span data-ttu-id="4ac8b-222">Siirry asiakkaan laskukirjauskansioon ja valitse projektin lasku sitten **Taulukon nimi** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="4ac8b-222">Enter the customer invoice journal, and then, in the **Table name** field, select the project invoice.</span></span>
4. <span data-ttu-id="4ac8b-223">Määritä kullekin taulukolle liittyvä asiakirjakonteksti:</span><span class="sxs-lookup"><span data-stu-id="4ac8b-223">For each table, define a related document context:</span></span>

    - <span data-ttu-id="4ac8b-224">Syötä kohtaan **Asiakkaan laskukirjauskansio** **Asiakkaan laskukonteksti**.</span><span class="sxs-lookup"><span data-stu-id="4ac8b-224">For **Customer invoice journal**, enter **Customer invoice context**.</span></span>
    - <span data-ttu-id="4ac8b-225">Syötä kohtaan **Projektilasku** **Projektilaskun konteksti**.</span><span class="sxs-lookup"><span data-stu-id="4ac8b-225">For **Project invoice**, enter **Project invoice context**.</span></span>

4. <span data-ttu-id="4ac8b-226">Valitsemalla **Vastaustyypit** määrittää vastaustyypit, jotka voidaan palauttaa sähköisen laskutuksen lisäosasta ja lisätä asiakkaan laskukirjauskansioon tai projektilaskuun.</span><span class="sxs-lookup"><span data-stu-id="4ac8b-226">Select **Response types** to configure the response types that can be returned from the Electronic invoicing add-on and included in a customer invoice journal or project invoice.</span></span>
5. <span data-ttu-id="4ac8b-227">Valitse **Uusi** ja sitten **Vastaustyyppi** -kentässä **Vastaus**.</span><span class="sxs-lookup"><span data-stu-id="4ac8b-227">Select **New**, and then, in the **Response type** field, select **Response**.</span></span>
6. <span data-ttu-id="4ac8b-228">Valitse **Lähetystila**-kentässä **Odottaa**.</span><span class="sxs-lookup"><span data-stu-id="4ac8b-228">In the **Submission status** field, select **Pending**.</span></span>
7. <span data-ttu-id="4ac8b-229">Valitse **Mallin yhdistämismääritys** -kentässä **Vastaussanoman tuontimuoto – mallin yhdistämismääritys vastaussanomasta**.</span><span class="sxs-lookup"><span data-stu-id="4ac8b-229">In the **Model mapping** field, select **Response message import format – Model mapping from response message**.</span></span>
8. <span data-ttu-id="4ac8b-230">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="4ac8b-230">Select **Save**.</span></span>
9. <span data-ttu-id="4ac8b-231">Valitse **Uusi** ja sitten **Vastaustyyppi** -kentässä **ResponseData**.</span><span class="sxs-lookup"><span data-stu-id="4ac8b-231">Select **New**, and then, in the **Response type** field, select **ResponseData**.</span></span>
10. <span data-ttu-id="4ac8b-232">Valitse **Lähetystila**-kentässä **Odottaa**.</span><span class="sxs-lookup"><span data-stu-id="4ac8b-232">In the **Submission status** field, select **Pending**.</span></span>
11. <span data-ttu-id="4ac8b-233">Valitse **Mallin yhdistämismääritys** -kentässä **CFDI-vastaustietojen tuontimuoto (tiedot) – vastaustietojen tuonti**</span><span class="sxs-lookup"><span data-stu-id="4ac8b-233">In the **Model mapping** field, select **CFDI response data import format (details) – Response data import**.</span></span>
12. <span data-ttu-id="4ac8b-234">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="4ac8b-234">Select **Save**.</span></span>

## <a name="process-electronic-invoices-in-finance"></a><span data-ttu-id="4ac8b-235">Sähköisten laskujen käsittely Financessa</span><span class="sxs-lookup"><span data-stu-id="4ac8b-235">Process electronic invoices in Finance</span></span> 

<span data-ttu-id="4ac8b-236">Kun käsittelet CFDI-laskuja Financessa sähköisen laskutuksen lisäosan kautta, voit suorittaa seuraavia tehtäviä:</span><span class="sxs-lookup"><span data-stu-id="4ac8b-236">During the processing of CFDI invoices in Finance through the Electronic invoicing add-on, you can perform the following tasks:</span></span>

- <span data-ttu-id="4ac8b-237">CFDI-laskujen lähettäminen.</span><span class="sxs-lookup"><span data-stu-id="4ac8b-237">Submit CFDI invoices.</span></span>
- <span data-ttu-id="4ac8b-238">Lähetyksen suorituslokien tarkastelu.</span><span class="sxs-lookup"><span data-stu-id="4ac8b-238">View the submission execution logs.</span></span>
- <span data-ttu-id="4ac8b-239">CFDI-laskun peruutuksen lähettäminen.</span><span class="sxs-lookup"><span data-stu-id="4ac8b-239">Submit the cancellation of a CFDI invoice.</span></span>

### <a name="submit-cfdi-invoices"></a><span data-ttu-id="4ac8b-240">CFDI-laskujen lähettäminen</span><span class="sxs-lookup"><span data-stu-id="4ac8b-240">Submit CFDI invoices</span></span>

<span data-ttu-id="4ac8b-241">Kun olet ottanut käyttöön **Määritettävä sähköisen laskutuksen lisäosan integrointi** -toiminnon **Vie/tuo sähköinen lasku** -prosessia (**Myyntireskontra \> Laskut \> Sähköiset laskut**) CFDI-laskujen lähettämiseen ei voida enää käyttää.</span><span class="sxs-lookup"><span data-stu-id="4ac8b-241">After you turn on the **Configurable Electronic invoicing add-on integration** feature, the **Export/Import electronic invoice** process (**Accounts receivable \> Invoices \> E-invoices**) for submitting CFDI invoices can no longer be used.</span></span> <span data-ttu-id="4ac8b-242">Se korvataan uudella prosessilla, jonka nimi on **Lähetä sähköiset asiakirjat**.</span><span class="sxs-lookup"><span data-stu-id="4ac8b-242">It's replaced by a new process that is named **Submit electronic documents**.</span></span>

> [!NOTE]
> <span data-ttu-id="4ac8b-243">Ennen kuin käytät uutta **Lähetä sähköisiä asiakirjoja** -prosessia, varmista, että Meksikon sähköisten laskujen edellyttämät määritykset on tehty.</span><span class="sxs-lookup"><span data-stu-id="4ac8b-243">Before you use the new **Submit electronic documents** process, verify that the setup that is required for Mexican e-invoices was completed.</span></span> <span data-ttu-id="4ac8b-244">Lisätietoja [CFDI-asettelun versio 3.3](https://docs.microsoft.com/dynamics365/finance/localizations/latam-mex-cfdi-3-3).</span><span class="sxs-lookup"><span data-stu-id="4ac8b-244">For more information, see [CFDI layout version 3.3](https://docs.microsoft.com/dynamics365/finance/localizations/latam-mex-cfdi-3-3).</span></span>

1. <span data-ttu-id="4ac8b-245">Siirry kohtaan **Organisaation hallinta \> Säännölliset \> Sähköiset asiakirjat \> Lähetä sähköisiä asiakirjoja**.</span><span class="sxs-lookup"><span data-stu-id="4ac8b-245">Go to **Organization administration \> Periodic \> Electronic documents \> Submit electronic documents**.</span></span>
2. <span data-ttu-id="4ac8b-246">Kun mikä tahansa asiakirja lähetetään ensimmäistä kertaa, määritä **Lähetä asiakirjat uudelleen** -asetukseksi aina **Ei**.</span><span class="sxs-lookup"><span data-stu-id="4ac8b-246">For the first submission of any document, always set the **Resubmit documents** option to **No**.</span></span> <span data-ttu-id="4ac8b-247">Jos sinun on lähetettävä asiakirja uudelleen palvelun kautta, määritä asetukseksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="4ac8b-247">If you must resubmit a document through the service, set this option to **Yes**.</span></span>
3. <span data-ttu-id="4ac8b-248">Valitse **Sisällytettävät tietueet** -pikavälilehdessä **Suodata** avataksesi **Kysely**-valintaruudun, jossa voit muodostaa kyselyn lähetettävien asiakirjojen valitsemista varten.</span><span class="sxs-lookup"><span data-stu-id="4ac8b-248">On the **Records to include** FastTab, select **Filter** to open the **Inquiry** dialog box, where you can build a query to select documents for submission.</span></span>

![CFDI-asiakirjan lähettäminen](media/e-Invoicing-services-get-started-MEX-Submit-CFDI-document.png)

> [!NOTE]
> <span data-ttu-id="4ac8b-250">Kun yrität lähettää asiakirjan palvelun kautta ensimmäisen kerran, järjestelmä pyytää vahvistamaan yhteyden sähköisen laskutuksen lisäosaan.</span><span class="sxs-lookup"><span data-stu-id="4ac8b-250">During your first attempt to submit a document through the service, you will be prompted to confirm the connection with the Electronic invoicing add-on.</span></span> <span data-ttu-id="4ac8b-251">Valitse **Yhdistä sähköisten asiakirjojen lähetyspalveluun napsauttamalla tätä**.</span><span class="sxs-lookup"><span data-stu-id="4ac8b-251">Select **Click here to connect to Electronic Document Submission Service**.</span></span>

### <a name="view-submission-logs"></a><span data-ttu-id="4ac8b-252">Lähetyslokien tarkasteleminen</span><span class="sxs-lookup"><span data-stu-id="4ac8b-252">View submission logs</span></span>

<span data-ttu-id="4ac8b-253">Voit tarkastella kaikkien lähetettyjen asiakirjojen tai vain yhden lähetetyn asiakirjan lähetyslokeja.</span><span class="sxs-lookup"><span data-stu-id="4ac8b-253">You can view the submission logs for all submitted documents or for just one submitted document.</span></span>

#### <a name="view-all-submission-logs"></a><span data-ttu-id="4ac8b-254">Kaikkien lähetyslokien tarkastelu</span><span class="sxs-lookup"><span data-stu-id="4ac8b-254">View all submission logs</span></span>

<span data-ttu-id="4ac8b-255">Kun olet ottanut **Määritettävä sähköisen laskutuksen lisäosan integrointi** -toiminnon käyttöön, käytettävissä on uusi sivu, jolla voi seurata asiakirjan lähetysprosessia.</span><span class="sxs-lookup"><span data-stu-id="4ac8b-255">After you turn on the **Configurable Electronic invoicing add-on integration** feature, a new page is available that lets you follow up on the document submission process.</span></span> <span data-ttu-id="4ac8b-256">Voit käyttää tätä sivua kaikkien lähetettyjen asiakirjojen lähetyslokien tarkasteluun.</span><span class="sxs-lookup"><span data-stu-id="4ac8b-256">You can use this page to view the submission logs for all submitted documents.</span></span>

1. <span data-ttu-id="4ac8b-257">Siirry kohtaan **Organisaation hallinta \> Säännölliset \> Sähköiset asiakirjat \> Sähköisen asiakirjan lähetysloki**.</span><span class="sxs-lookup"><span data-stu-id="4ac8b-257">Go to **Organization administration \> Periodic \> Electronic documents \> Electronic document submission log**.</span></span>
2. <span data-ttu-id="4ac8b-258">Valitse **Asiakirjatyyppi**-kentässä **Asiakkaan laskukirjauskansio** suodattaaksesi vaadittavat sähköiset asiakirjat.</span><span class="sxs-lookup"><span data-stu-id="4ac8b-258">In the **Document type** field, select **Customer invoice journal** to filter for the required electronic documents.</span></span>

    ![Asiakirjatyypin valinta lähetyslokien tarkastelua varten](media/e-Invoicing-services-get-started-MEX-Select-document-type-for-viewing-submission-log.png)

3. <span data-ttu-id="4ac8b-260">Valitse toimintoruudussa **Kyselyt \> Lähetystiedot** tarkastellaksesi lähetyksen toteutuslokien tietoja.</span><span class="sxs-lookup"><span data-stu-id="4ac8b-260">On the Action Pane, select **Inquiries \> Submission details** to view the details of the submission execution logs.</span></span>

    ![Lähetyslokitietojen tarkastelu](media/e-Invoicing-services-get-started-MEX-View-submission-log-details.png)

<span data-ttu-id="4ac8b-262">Lähetyslokien tiedot jakautuvat kolmeen pikavälilehteen:</span><span class="sxs-lookup"><span data-stu-id="4ac8b-262">The information in the submission logs is divided among three FastTabs:</span></span>

- <span data-ttu-id="4ac8b-263">**Käsittelytoimet** – Tässä pikavälilehdessä näkyy RCS:ssä määritetyssä toimintoversiossa määritettyjen toimien suoritusloki.</span><span class="sxs-lookup"><span data-stu-id="4ac8b-263">**Processing actions** – This FastTab shows the execution log for the actions that are configured in the feature version that was set up in RCS.</span></span> <span data-ttu-id="4ac8b-264">**Tila**-sarakkeessa näkyy, suoritettiinko toimi onnistuneesti.</span><span class="sxs-lookup"><span data-stu-id="4ac8b-264">The **Status** column shows whether the action was successfully run.</span></span>
- <span data-ttu-id="4ac8b-265">**Toimitiedostot** – Tässä pikavälilehdessä näkyvät välitiedostot, jotka luotiin toimien suorittamisen aikana.</span><span class="sxs-lookup"><span data-stu-id="4ac8b-265">**Action files** – This FastTab shows the intermediate files that were generated during execution of the actions.</span></span> <span data-ttu-id="4ac8b-266">Voit ladata tiedoston ja tarkastella sitä valitsemalla **Näytä**.</span><span class="sxs-lookup"><span data-stu-id="4ac8b-266">You can select **View** to download and view the file.</span></span>
- <span data-ttu-id="4ac8b-267">**Käsittelytoimen loki** – Tässä pikavälilehdessä näkyvät sähköisen laskutuksen lisäosan ja kohteena olevan verkkopalvelun välisen tiedonsiirron tulokset.</span><span class="sxs-lookup"><span data-stu-id="4ac8b-267">**Processing action log** – This FastTab shows the results of the communication between the Electronic invoicing add-on and the target web service.</span></span> <span data-ttu-id="4ac8b-268">Siinä näkyy myös, mitä verkkopalvelun käsittely palautti.</span><span class="sxs-lookup"><span data-stu-id="4ac8b-268">It also shows what was returned by the processing from the web service.</span></span> <span data-ttu-id="4ac8b-269">**Virhekoodi**-sarakkeessa näkyy palautuskoodi, jonka hyväksynnän verkkopalvelu palautti.</span><span class="sxs-lookup"><span data-stu-id="4ac8b-269">The **Error code** column shows the return code that was returned by the authorization web service.</span></span>

<span data-ttu-id="4ac8b-270">Kun lähetetty CFDI-lasku on hyväksytty, sen tilaksi päivitetään **Hyväksytty**.</span><span class="sxs-lookup"><span data-stu-id="4ac8b-270">When the submitted CFDI invoice is authorized, its status is updated to **Approved**.</span></span>

#### <a name="view-submission-logs-from-cfdi-invoices"></a><span data-ttu-id="4ac8b-271">CFDI-laskujen lähetyslokien tarkastelu</span><span class="sxs-lookup"><span data-stu-id="4ac8b-271">View submission logs from CFDI invoices</span></span>

<span data-ttu-id="4ac8b-272">Kun otat **Määritettävä sähköisen laskutuksen lisäosan integrointi** -toiminnon käyttöön, voit myös tarkastella CFDI-laskujen lähetyslokeja.</span><span class="sxs-lookup"><span data-stu-id="4ac8b-272">After you turn on the **ConfigurableElectronic invoicing add-on integration** feature, you can also view the submission logs from CFDI invoices.</span></span>

1. <span data-ttu-id="4ac8b-273">Siirry kohtaan **Myyntireskontra \> Kyselyt ja raportit \> CFDI (sähköiset laskut)**.</span><span class="sxs-lookup"><span data-stu-id="4ac8b-273">Go to **Accounts receivable \> Inquiries and reports \> CFDI (electronic invoices)**.</span></span>
2. <span data-ttu-id="4ac8b-274">Valitse CFDI-lasku, joka on lähetetty sen jälkeen, kun **Määritettävä sähköisen laskutuksen lisäosan integrointi** on otettu käyttöön.</span><span class="sxs-lookup"><span data-stu-id="4ac8b-274">Select a CFDI invoice that was submitted after the **Configurable Electronic invoicing add-on integration** feature was turned on.</span></span>
3. <span data-ttu-id="4ac8b-275">Valitse toimintoruudun **Historia**-välilehdessä **Sähköisen asiakirjan loki**.</span><span class="sxs-lookup"><span data-stu-id="4ac8b-275">On the Action Pane, on the **History** tab, select **Electronic document log**.</span></span>

![CFDI-laskujen lähetyslokien tarkastelu](media/e-Invoicing-services-get-started-MEX-View-submission-log-from-CFDI-invoice.png)

> [!NOTE]
> <span data-ttu-id="4ac8b-277">**Historia**-painike on käytettävissä sellaisten CFDI-laskujen osalta, jotka on lähetetty, ennen kuin **Määritettävä sähköisen laskutuksen lisäosan integrointi** -toiminto otettiin käyttöön.</span><span class="sxs-lookup"><span data-stu-id="4ac8b-277">For CFDI invoices that were submitted before the **Configurable Electronic invoicing add-on integration** feature was turned on, the **History** button is available.</span></span> <span data-ttu-id="4ac8b-278">**Historia**-painike ei ole käytettävissä sellaisten CFDI-laskujen osalta, jotka on lähetetty sen jälkeen, kun **Määritettävä sähköisen laskutuksen lisäosan integrointi** -toiminto otettiin käyttöön.</span><span class="sxs-lookup"><span data-stu-id="4ac8b-278">The **History** button isn't available for CFDI invoices that were submitted after the **Configurable Electronic invoicing add-on integration** feature was turned on.</span></span>

### <a name="submit-cancellation-of-cfdi-invoices"></a><span data-ttu-id="4ac8b-279">CFDI-laskujen peruutuksen lähettäminen</span><span class="sxs-lookup"><span data-stu-id="4ac8b-279">Submit cancellation of CFDI invoices</span></span>

<span data-ttu-id="4ac8b-280">Kun olet ottanut **Määritettävä sähköisen laskutuksen lisäosan integrointi** -toiminnon käyttöön, vanhaa CFDI-laskujen peruutusprosessia ei voi enää käyttää.</span><span class="sxs-lookup"><span data-stu-id="4ac8b-280">After you turn on the **Configurable Electronic invoicing add-on integration** feature, the old process for canceling CFDI invoices can no longer be used.</span></span> <span data-ttu-id="4ac8b-281">Se korvataan uudella peruutusprosessilla, joka on upotettu **Sähköisen asiakirjan lähetysloki** -sivulle.</span><span class="sxs-lookup"><span data-stu-id="4ac8b-281">It's replaced by a new cancellation process that is embedded on the **Electronic document submission log** page.</span></span>

1. <span data-ttu-id="4ac8b-282">Siirry kohtaan **Myyntireskontra \> Kyselyt ja raportit \> CFDI (sähköiset laskut)**.</span><span class="sxs-lookup"><span data-stu-id="4ac8b-282">Go to **Accounts receivable \> Inquiries and reports \> CFDI (electronic invoices)**.</span></span>
2. <span data-ttu-id="4ac8b-283">Jos CFDI-laskun tila on **Hyväksytty**, valitse **Funktiot \> Peruuta CFDI**.</span><span class="sxs-lookup"><span data-stu-id="4ac8b-283">If the CFDI invoice has a status of **Approved**, select **Functions \> Cancel CFDI**.</span></span>
3. <span data-ttu-id="4ac8b-284">Siirry kohtaan **Organisaation hallinta \> Säännölliset \> Sähköiset asiakirjat \> Sähköisen asiakirjan lähetysloki**.</span><span class="sxs-lookup"><span data-stu-id="4ac8b-284">Go to **Organization administration \> Periodic \> Electronic documents \> Electronic document submission log**.</span></span>
4. <span data-ttu-id="4ac8b-285">Valitse CFDI-lasku ja valitse sitten **Funktiot \> Lähetä liittyvät lähetykset**.</span><span class="sxs-lookup"><span data-stu-id="4ac8b-285">Select the CFDI invoice, and then select **Functions \> Send related submissions**.</span></span>
5. <span data-ttu-id="4ac8b-286">Kirjoita liittyvän lähetyksen kuvaus ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="4ac8b-286">Enter a description for the related submission, and then select **OK**.</span></span>

#### <a name="view-cancellation-submission-logs"></a><span data-ttu-id="4ac8b-287">Peruutusten lähetyslokien tarkastelu</span><span class="sxs-lookup"><span data-stu-id="4ac8b-287">View cancellation submission logs</span></span>

1. <span data-ttu-id="4ac8b-288">Siirry kohtaan **Organisaation hallinta \> Säännölliset \> Sähköiset asiakirjat \> Sähköisen asiakirjan lähetysloki**.</span><span class="sxs-lookup"><span data-stu-id="4ac8b-288">Go to **Organization administration \> Periodic \> Electronic documents \> Electronic document submission log**.</span></span>
2. <span data-ttu-id="4ac8b-289">Valitse **Asiakirjatyyppi**-kentässä **Asiakkaan laskukirjauskansio** suodattaaksesi vain asiakkaan laskukirjauskansion asiakirjoja.</span><span class="sxs-lookup"><span data-stu-id="4ac8b-289">In the **Document type** field, select **Customer invoice journal** to filter for customer invoice journal documents only.</span></span>
3. <span data-ttu-id="4ac8b-290">Valitse CFDI-lasku ja valitse sitten toimintoruudussa **Kyselyt \> Liittyvä lähetys**.</span><span class="sxs-lookup"><span data-stu-id="4ac8b-290">Select the CFDI invoice, and then, on the Action Pane, select **Inquiries \> Related submission**.</span></span>

    <span data-ttu-id="4ac8b-291">**Liittyvät lähetykset** -sivulla näkyvät kaikki liittyvät lähetykset ja niiden lähetystila tietyn CFDI-laskun osalta.</span><span class="sxs-lookup"><span data-stu-id="4ac8b-291">The **Related submissions** page shows all related submissions, and their submission status, for a given CFDI invoice.</span></span> <span data-ttu-id="4ac8b-292">Seuraavassa kuvassa ensimmäinen rivi edustaa lähetystä, joka pyysi CFDI-laskun hyväksymistä.</span><span class="sxs-lookup"><span data-stu-id="4ac8b-292">In the following illustration, the first line represents the submission that requested approval of the CFDI invoice.</span></span> <span data-ttu-id="4ac8b-293">Toinen rivi vastaa edustaa lähetystä, joka peruutti CFDI-laskun.</span><span class="sxs-lookup"><span data-stu-id="4ac8b-293">The second line represents the submission that canceled that CFDI invoice.</span></span>

    ![Peruutusten lähetyslokien tarkastelu](media/e-Invoicing-services-get-started-MEX-View-cancellation-submission-log.png)

4. <span data-ttu-id="4ac8b-295">Valitse toimintoruudussa **Kyselyt \> Lähetystiedot** tarkastellaksesi lähetyksen toteutuslokien tietoja.</span><span class="sxs-lookup"><span data-stu-id="4ac8b-295">On the Action Pane, select **Inquiries \> Submission details** to view the details of the submission execution logs.</span></span>

    ![Peruutusten lähetyslokitietojen tarkastelu](media/e-Invoicing-services-get-started-MEX-View-cancellation-submission-log-details.png)

## <a name="privacy-notice"></a><span data-ttu-id="4ac8b-297">Tietosuojatiedot</span><span class="sxs-lookup"><span data-stu-id="4ac8b-297">Privacy notice</span></span>
<span data-ttu-id="4ac8b-298">Toimintojen MX-00010 ja MX-00016 (CFDI-lasku ja CFDI-peruutus) käyttöönotto saattaa edellyttää rajoitettujen tietojen, organisaation verorekisteritunnus mukaan luettuna, lähettämistä.</span><span class="sxs-lookup"><span data-stu-id="4ac8b-298">Enabling the MX-00010 and MX-00016 (CFDI Invoice and CFDI Cancellation) features may require sending limited data, which includes the organization tax registration ID.</span></span> <span data-ttu-id="4ac8b-299">Ne välitetään kolmannen osapuolen virastoille, jotka veroviranomaiset ovat hyväksyneet sähköisten laskujen kyseiselle veroviranomaiselle lähettämistä varten siinä esimääritetyssä muodossa, jota integrointi valtion verkkopalveluun edellyttää.</span><span class="sxs-lookup"><span data-stu-id="4ac8b-299">This will be transmitted to third-party agencies authorized by the tax authority for purposes of sending electronic invoices to this tax authority in the predefined format required for integration with the government’s web service.</span></span> <span data-ttu-id="4ac8b-300">Järjestelmänvalvoja voi ottaa toiminnot MX-00010 ja MX-00016 (CFDI-lasku ja CFDI-peruutus) käyttöön ja poistaa ne käytöstä siirtymällä kohtaan **Organisaation hallinta \> Määritykset \> Sähköisten asiakirjojen parametrit**.</span><span class="sxs-lookup"><span data-stu-id="4ac8b-300">An administrator can enable and disable the MX-00010 and MX-00016 (CFDI Invoice and CFDI Cancellation) features by navigating to **Organization administration \> Setup \> Electronic document parameters**.</span></span> <span data-ttu-id="4ac8b-301">Valitse **Toiminnot**-välilehti, valitse toiminnot MX-00010 ja MX-00016 sisältävät rivit ja tee sitten haluamasi valinta.</span><span class="sxs-lookup"><span data-stu-id="4ac8b-301">Select the **Features** tab, select the rows containing the MX-00010 and MX-00016 features, and then make the appropriate selection.</span></span> <span data-ttu-id="4ac8b-302">Näistä ulkoisista järjestelmistä tähän Dynamics 365 -verkkopalveluun tuotuihin tietoihin sovelletaan [tietosuojalausuntoamme](https://go.microsoft.com/fwlink/?LinkId=512132).</span><span class="sxs-lookup"><span data-stu-id="4ac8b-302">Data imported from these external systems into this Dynamics 365 online service are subject to our [privacy statement](https://go.microsoft.com/fwlink/?LinkId=512132).</span></span> <span data-ttu-id="4ac8b-303">Katso lisätietoja maakohtaisten toimintodokumentaatioiden tietosuojaosista.</span><span class="sxs-lookup"><span data-stu-id="4ac8b-303">Consult the Privacy notice sections in country-specific feature documentation for more information.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4ac8b-304">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="4ac8b-304">Additional resources</span></span>

- [<span data-ttu-id="4ac8b-305">Sähköisen laskutuksen yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="4ac8b-305">Electronic invoicing add-on overview</span></span>](e-invoicing-service-overview.md)
- [<span data-ttu-id="4ac8b-306">Sähköisen laskutuksen lisäosan käytön aloittaminen</span><span class="sxs-lookup"><span data-stu-id="4ac8b-306">Get started with the Electronic invoicing add-on</span></span>](e-invoicing-get-started.md)
- [<span data-ttu-id="4ac8b-307">Sähköisen laskutuksen lisäosan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="4ac8b-307">Set up the Electronic invoicing add-on</span></span>](e-invoicing-setup.md)
