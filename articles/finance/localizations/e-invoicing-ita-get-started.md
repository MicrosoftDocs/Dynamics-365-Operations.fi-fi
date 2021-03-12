---
title: Italian sähköisen laskutuksen lisäosan käytön aloittaminen
description: Tässä aiheessa on tietoja, joiden avulla voit aloittaa Italian sähköisen laskutuksen lisäosan käytön Microsoft Dynamics 365 Financessa ja Dynamics 365 Supply Chain Managementissa.
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
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 08d41244d3ec785127db8f69e37dd522a463c388
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4988537"
---
# <a name="get-started-with-the-electronic-invoicing-add-on-for-italy"></a><span data-ttu-id="4916b-103">Italian sähköisen laskutuksen lisäosan käytön aloittaminen</span><span class="sxs-lookup"><span data-stu-id="4916b-103">Get started with the Electronic invoicing add-on for Italy</span></span>

[!include [banner](../includes/banner.md)]


> [!IMPORTANT]
> <span data-ttu-id="4916b-104">Italian sähköisen laskutuksen lisäosa ei tällä hetkellä välttämättä tue kaikkia funktioita, jotka ovat käytettävissä Microsoft Dynamics 365 Financen ja Dynamics 365 Supply Chain Managementin laskuissa.</span><span class="sxs-lookup"><span data-stu-id="4916b-104">The Electronic invoicing add-on for Italy might not currently support all the functions that are available for electronic invoices in Microsoft Dynamics 365 Finance and Dynamics 365 Supply Chain Management.</span></span> 

<span data-ttu-id="4916b-105">Tässä aiheessa on tietoja, joiden avulla voit aloittaa Italian sähköisen laskutuksen lisäosan käytön.</span><span class="sxs-lookup"><span data-stu-id="4916b-105">This topic provides information that will help you get started with the Electronic invoicing add-on for Italy.</span></span> <span data-ttu-id="4916b-106">Se opastaa Regulatory Configuration Servicesin (RCS) ja Financen maakohtaisissa määritysvaiheissa.</span><span class="sxs-lookup"><span data-stu-id="4916b-106">It guides you through the configuration steps that are country-dependent in Regulatory Configuration Services (RCS) and Finance.</span></span> <span data-ttu-id="4916b-107">Se opastaa myös, miten voidaan lähettää sähköisiä laskuja, jotka on luotu palvelulla Italialle yksilöllisessä **FatturaPA**-muodossa. Lisäksi siinä selitetään, miten käsittelyn tulokset arvioidaan.</span><span class="sxs-lookup"><span data-stu-id="4916b-107">It also guides you through the process for submitting electronic invoices that are generated in the Italy-specific **FatturaPA** format through the service, and it explains how to review the results of processing.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="4916b-108">Edellytykset</span><span class="sxs-lookup"><span data-stu-id="4916b-108">Prerequisites</span></span>

<span data-ttu-id="4916b-109">Ennen kuin suoritat tämän aiheen vaiheet, sinun on suoritettava aiheen [Sähköisen laskutuksen lisäosan käytön aloittaminen](e-invoicing-get-started.md) vaiheet.</span><span class="sxs-lookup"><span data-stu-id="4916b-109">Before you complete the steps in this topic, you must complete the steps in [Get started with the Electronic invoicing add-on](e-invoicing-get-started.md).</span></span>

## <a name="rcs-setup"></a><span data-ttu-id="4916b-110">RCS-asetukset</span><span class="sxs-lookup"><span data-stu-id="4916b-110">RCS setup</span></span>

<span data-ttu-id="4916b-111">RCS:n määrityksen aikana suoritat seuraavat tehtävät:</span><span class="sxs-lookup"><span data-stu-id="4916b-111">During the RCS setup, you will complete these tasks:</span></span>

1. <span data-ttu-id="4916b-112">Sähköisen laskutuksen toiminnon tuominen asiakkaiden sähköisten laskujen viemiseen **FatturaPA**-muodossa.</span><span class="sxs-lookup"><span data-stu-id="4916b-112">Import the e-Invoicing feature for the export of customer electronic invoices in the **FatturaPA** format.</span></span>
2. <span data-ttu-id="4916b-113">Sähköisiä laskuja koskevien vastausten luomiseen, lähettämiseen ja vastaanottamiseen vaadittavien muotomääritysten arvioiminen.</span><span class="sxs-lookup"><span data-stu-id="4916b-113">Review the format configurations that are required to generate, submit, and receive responses about electronic invoices.</span></span>
3. <span data-ttu-id="4916b-114">Määritä tapahtumat, jotka tukevat sähköisen laskun lähetysskenaarioita.</span><span class="sxs-lookup"><span data-stu-id="4916b-114">Configure the events that support the electronic invoice submission scenarios.</span></span>
4. <span data-ttu-id="4916b-115">Sähköisen laskutuksen toiminnon julkaiseminen.</span><span class="sxs-lookup"><span data-stu-id="4916b-115">Publish the e-Invoicing feature.</span></span>

> [!NOTE]
> <span data-ttu-id="4916b-116">Sähköisen laskutuksen toiminto on sen resurssin yleinen nimi, joka määritetään ja julkaistaan käytettäväksi sähköisen laskutuksen lisäosan palvelimella.</span><span class="sxs-lookup"><span data-stu-id="4916b-116">"The e-Invoicing feature" is the generic name for the resource that is configured and published to consume the Electronic invoicing add-on server.</span></span> <span data-ttu-id="4916b-117">Tässä tapauksessa määritettävä sähköisen laskutuksen toiminto on asiakkaiden sähköisten laskujen vienti.</span><span class="sxs-lookup"><span data-stu-id="4916b-117">In this case, the export of customer electronic invoices is the e-Invoicing feature that you will set up.</span></span>

## <a name="import-the-e-invoicing-feature"></a><span data-ttu-id="4916b-118">Sähköisen laskutuksen toiminnon tuominen</span><span class="sxs-lookup"><span data-stu-id="4916b-118">Import the e-Invoicing feature</span></span>

1. <span data-ttu-id="4916b-119">Kirjaudu RCS-tilille.</span><span class="sxs-lookup"><span data-stu-id="4916b-119">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="4916b-120">Valitse **Globalisointitoiminnot**-työtila ja **Toiminnot**-kohdan **Sähköinen laskutus** -ruutu.</span><span class="sxs-lookup"><span data-stu-id="4916b-120">In the **Globalization features** workspace, in the **Features** section, select the **e-Invoicing** tile.</span></span>
3. <span data-ttu-id="4916b-121">Valitse **Sähköisen laskutuksen toiminnot** -sivulla **Tuo** tuodaksesi sähköisen laskutuksen toiminnon yleisestä säilöstä.</span><span class="sxs-lookup"><span data-stu-id="4916b-121">On the **e-Invoicing Features** page, select **Import** to import the e-Invoicing feature from the Global repository.</span></span>

    > [!NOTE]
    > <span data-ttu-id="4916b-122">Jos käytettävissä olevien toimintojen luettelo ei ole näkyvissä, valitse **Synkronoi**.</span><span class="sxs-lookup"><span data-stu-id="4916b-122">If you don't see the list of available features, select **Synchronize**.</span></span> 

4. <span data-ttu-id="4916b-123">Valitse **Sähköisten laskujen vienti (IT)** -toiminto ja sitten **Tuo**.</span><span class="sxs-lookup"><span data-stu-id="4916b-123">Select the **e-Invoices Export (IT)** feature, and then select **Import**.</span></span>

![Sähköisten laskujen vienti (IT) -toiminnon tuominen](media/e-Invoicing-services-get-started-ITA-Select-Import-e-Invoicing-feature.png)

<span data-ttu-id="4916b-125">Kun tuot **Sähköisten laskujen vienti (IT)** -toiminnon yleisestä säilöstä, myös kaikki seuraavissa osissa kuvatut asetukset tuodaan.</span><span class="sxs-lookup"><span data-stu-id="4916b-125">When you import the **e-Invoices Export (IT)** feature from the Global repository, all the settings that are described in the next sections are also imported.</span></span>

## <a name="create-a-new-version-of-the-e-invoices-export-it-feature"></a><span data-ttu-id="4916b-126">Uuden versoin luominen Sähköisten laskujen vienti (IT) -toiminnosta</span><span class="sxs-lookup"><span data-stu-id="4916b-126">Create a new version of the e-Invoices Export (IT) feature</span></span>

1. <span data-ttu-id="4916b-127">Valitse **Sähköisen laskutuksen toiminnot** -sivun **Versiot**-välilehdellä **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="4916b-127">On the **e-Invoicing Features** page, on the **Versions** tab, select **New**.</span></span> 

    ![Uuden sähköisen laskutuksen toiminnon version lisääminen](media/e-Invoicing-services-get-started-ITA-Select-New-e-Invoicing-feature-version.png)

    <span data-ttu-id="4916b-129">Seuraavaksi määritetään sähköisen raportoinnin (ER) muodot, jotka liittyvät sähköisen laskutuksen toimintoon.</span><span class="sxs-lookup"><span data-stu-id="4916b-129">Next, you will configure the Electronic reporting (ER) formats that are associated with the e-Invoicing feature.</span></span>

2. <span data-ttu-id="4916b-130">Hallitse märitysversioita valitsemalla **Määritykset**-välilehdessä **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="4916b-130">On the **Configurations** tab, select **Add** to manage the configuration versions.</span></span>

    ![Sähköisen laskutuksen toiminnon määritysversioiden hallinta](media/e-Invoicing-services-get-started-ITA-Manage-e-Invoicing-feature-configurations.png)

    <span data-ttu-id="4916b-132">Tässä vaiheessa lisätään ja määritetään italialaisten sähköisten laskujen viemisessä käytettävien eri tiedostojen ER-muotoja.</span><span class="sxs-lookup"><span data-stu-id="4916b-132">In this step, you're adding and configuring the ER formats of different files that are used to export Italian e-invoices.</span></span> <span data-ttu-id="4916b-133">Italialaisissa sähköisissä FatturaPA-laskuissa käytetään joko seuraavia vakiomäärityksiä tai ajantasaisia mukautettuja määrityksiä, joita käytät sähköisessä laskutuksessa:</span><span class="sxs-lookup"><span data-stu-id="4916b-133">For Italian FatturaPA e-invoices, use either the following standard configurations or the actual customized configurations that you use for e-invoicing:</span></span>

    - <span data-ttu-id="4916b-134">Myyntilasku (IT)</span><span class="sxs-lookup"><span data-stu-id="4916b-134">Sales invoice (IT)</span></span>
    - <span data-ttu-id="4916b-135">Projektilasku (IT)</span><span class="sxs-lookup"><span data-stu-id="4916b-135">Project invoice (IT)</span></span>

    <span data-ttu-id="4916b-136">Kun luot sähköisen laskun toiminnon, joka johdetaan toisesta vastaavasta, kaikki ER-muodot periytyvät alkuperäisestä toiminnosta.</span><span class="sxs-lookup"><span data-stu-id="4916b-136">When you create an e-Invoicing feature that is derived from another e-Invoicing feature, all ER formats are inherited from the original feature.</span></span>

3. <span data-ttu-id="4916b-137">Valitse tietty tiedoston ER-muodon määritys.</span><span class="sxs-lookup"><span data-stu-id="4916b-137">Select a specific ER format file configuration.</span></span>
4. <span data-ttu-id="4916b-138">Avaa **Muodon suunnittelija** -sivu valitsemalla **Muokkaa** tai **Näytä**.</span><span class="sxs-lookup"><span data-stu-id="4916b-138">Select **Edit** or **View** to open the **Format designer** page.</span></span>

    ![Muodon suunnittelija -sivun avaaminen](media/e-Invoicing-services-get-started-ITA-Configuration-ER-format-designer.png)

5. <span data-ttu-id="4916b-140">Käytä **Muodon suunnittelija** -sivua muokataksesi ja tarkastellaksesi ER-muodon tiedostomäärityksiä.</span><span class="sxs-lookup"><span data-stu-id="4916b-140">Use the **Format designer** page to edit and view the ER format file configurations.</span></span>

    ![Muodon suunnittelutoiminto -sivu](media/e-Invoicing-services-get-started-ITA-ER-format-designer.png)

## <a name="manage-the-e-invoicing-feature-setups"></a><span data-ttu-id="4916b-142">Sähköisen laskutuksen toiminnon määritysten hallinta</span><span class="sxs-lookup"><span data-stu-id="4916b-142">Manage the e-Invoicing feature setups</span></span>

- <span data-ttu-id="4916b-143">Voit hallita sähköisen laskutuksen toiminnon määrityksiä valitsemalla **Sähköisen laskutuksen toiminnot** -sivun **Määritykset**-välilehdessä **Lisää**, **Poista** tai **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="4916b-143">On the **e-Invoicing Features** page, on the **Setups** tab, select **Add**, **Delete**, or **Edit** to manage the e-Invoicing feature setups.</span></span>

![Sähköisen laskutuksen toiminnon määritysten hallinta](media/e-Invoicing-services-get-started-ITA-Manage-e-Invoicing-feature-setup.png)

<span data-ttu-id="4916b-145">Tässä vaiheessa määritetään sähköisiin laskuihin sovellettavat tapahtumat, kuten XML-tulostetiedostojen luonti **FatturaPA**-muodossa ja digitaalinen allekirjoitus (tarvittaessa).</span><span class="sxs-lookup"><span data-stu-id="4916b-145">In this step, you configure the events that are applicable to electronic invoices, including generation of the XML output files in **FatturaPA** format and digital signing (if required).</span></span>

### <a name="configure-the-sales-invoice-feature-setup"></a><span data-ttu-id="4916b-146">Myyntilaskutoiminnon asetusten määrittäminen</span><span class="sxs-lookup"><span data-stu-id="4916b-146">Configure the Sales invoice feature setup</span></span>

1. <span data-ttu-id="4916b-147">Valitse **Sähköisen laskutuksen toiminnot** -sivun **Määritykset**-välilehden **Toiminnon määritys** -sarakkeessa **Myyntilasku**.</span><span class="sxs-lookup"><span data-stu-id="4916b-147">On the **e-Invoicing Features** page, on the **Setups** tab, in the **Feature setup** column, select **Sales invoice**.</span></span>
2. <span data-ttu-id="4916b-148">Valitse **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="4916b-148">Select **Edit**.</span></span>
3. <span data-ttu-id="4916b-149">Voit hallita toimiluetteloa valitsemalla **Toimintoversion määritys** -sivulla **Toimet**-välilehti.</span><span class="sxs-lookup"><span data-stu-id="4916b-149">On the **Feature version setup** page, select the **Actions** tab to manage the list of actions.</span></span> <span data-ttu-id="4916b-150">Toimet määrittävät luettelon toiminnoista, jotka on suoritettava peräkkäisessä järjestyksessä, jotta toiminto suoritetaan kokonaisuudessaan.</span><span class="sxs-lookup"><span data-stu-id="4916b-150">Actions define a list of operations that must be run in sequential order to accomplish full execution of the event.</span></span>

    ![Toimet-välilehti](media/e-Invoicing-services-get-started-ITA-Select-Actions.png)

    | <span data-ttu-id="4916b-152">Toimenpiteen tunnus</span><span class="sxs-lookup"><span data-stu-id="4916b-152">Action ID</span></span> | <span data-ttu-id="4916b-153">Toiminnon nimi</span><span class="sxs-lookup"><span data-stu-id="4916b-153">Action name</span></span>        | <span data-ttu-id="4916b-154">Toiminnon kuvaus</span><span class="sxs-lookup"><span data-stu-id="4916b-154">Action description</span></span>                                     |
    |-----------|--------------------|--------------------------------------------------------|
    | <span data-ttu-id="4916b-155">1</span><span class="sxs-lookup"><span data-stu-id="4916b-155">1</span></span>         | <span data-ttu-id="4916b-156">Muunna asiakirja</span><span class="sxs-lookup"><span data-stu-id="4916b-156">Transform document</span></span> | <span data-ttu-id="4916b-157">Luo sähköisen laskun XML-tiedosto **fatturaPA**-muodossa.</span><span class="sxs-lookup"><span data-stu-id="4916b-157">Create the e-invoice XML file in **FatturaPA** format.</span></span> |
    | <span data-ttu-id="4916b-158">2</span><span class="sxs-lookup"><span data-stu-id="4916b-158">2</span></span>         | <span data-ttu-id="4916b-159">Allekirjoita tiedosto</span><span class="sxs-lookup"><span data-stu-id="4916b-159">Sign document</span></span>      | <span data-ttu-id="4916b-160">Käytä XML-tiedostossa digitaalista allekirjoitusta.</span><span class="sxs-lookup"><span data-stu-id="4916b-160">Apply a digital signature to the XML file.</span></span>             |

4. <span data-ttu-id="4916b-161">Voit tarkastella ja hallita soveltuvuusääntöjä valitsemalla **Soveltuvuussäännöt**-välilehden.</span><span class="sxs-lookup"><span data-stu-id="4916b-161">Select the **Applicability rules** tab to view and maintain the applicability rules.</span></span> <span data-ttu-id="4916b-162">Soveltuvuussäännöt määrittävät kontekstin, jossa toimi suoritetaan.</span><span class="sxs-lookup"><span data-stu-id="4916b-162">Applicability rules define the context where the action will be run.</span></span>

    ![Soveltuvuussääntöjen välilehti](media/e-Invoicing-services-get-started-ITA-Select-Applicability-rules.png)

5. <span data-ttu-id="4916b-164">Voit tarkastella ja hallita muuttujia valitsemalla **Muuttujat**-välilehden.</span><span class="sxs-lookup"><span data-stu-id="4916b-164">Select the **Variables** tab to view and maintain the variables.</span></span>

    ![Muuttujat-välilehti](media/e-Invoicing-services-get-started-ITA-Select-Variables.png)

6. <span data-ttu-id="4916b-166">Määritä julkiset muuttujat, jotka tarvitaan toimien suorittamiseen.</span><span class="sxs-lookup"><span data-stu-id="4916b-166">Define the public variables that are required to run the actions.</span></span>

### <a name="configure-the-project-invoice-feature-setup"></a><span data-ttu-id="4916b-167">Projektilaskutoiminnon asetusten määrittäminen</span><span class="sxs-lookup"><span data-stu-id="4916b-167">Configure the Project invoice feature setup</span></span> 

<span data-ttu-id="4916b-168">Vaiheet ja asetukset, joita tarvitaan **Projektilasku** -toiminnon määrittämiseen ovat hyvin samankaltaisia kuin **Myyntilasku**-toiminnon määrittämisen vaiheet ja asetukset.</span><span class="sxs-lookup"><span data-stu-id="4916b-168">The steps and settings that are required to configure the **Project invoice** feature setup are very similar to the steps and settings for the **Sales invoice** feature setup.</span></span> <span data-ttu-id="4916b-169">Kun käytät projektilaskuja, katso myyntilaskujen menettelyt.</span><span class="sxs-lookup"><span data-stu-id="4916b-169">When you work with project invoices, see the procedures for sales invoices.</span></span>

## <a name="assign-the-e-invoicing-feature-to-the-environment"></a><span data-ttu-id="4916b-170">Sähköisen laskutuksen toiminnon määrittäminen ympäristölle</span><span class="sxs-lookup"><span data-stu-id="4916b-170">Assign the e-Invoicing feature to the environment</span></span>

1. <span data-ttu-id="4916b-171">Valitse **Sähköisen laskutuksen toiminnot** -sivun **Ympäristöt**-välilehdellä **Ota käyttöön**.</span><span class="sxs-lookup"><span data-stu-id="4916b-171">On the **e-Invoicing Features** page, on the **Environments** tab, select **Enable**.</span></span>
2. <span data-ttu-id="4916b-172">Valitse ympäristö **Ympäristöt**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="4916b-172">In the **Environment** field, select the environment.</span></span>
3. <span data-ttu-id="4916b-173">Valitse **Voimaantulo**-kentässä päivämäärä, jona uusi ympäristö on tarkoitus ottaa käyttöön.</span><span class="sxs-lookup"><span data-stu-id="4916b-173">In the **Effective from** field, select the date when the environment should become effective.</span></span>
4. <span data-ttu-id="4916b-174">Valitse **Ota käyttöön**.</span><span class="sxs-lookup"><span data-stu-id="4916b-174">Select **Enable**.</span></span> 

![Sähköisen laskutuksen ympäristön käyttöönotto](media/e-Invoicing-services-get-started-ITA-Enable-e-Invoicing-environment.png)

## <a name="publish-the-e-invoicing-feature"></a><span data-ttu-id="4916b-176">Sähköisen laskutuksen toiminnon julkaiseminen</span><span class="sxs-lookup"><span data-stu-id="4916b-176">Publish the e-invoicing feature</span></span>

<span data-ttu-id="4916b-177">Voit julkaista sähköisen laskutuksen toiminnon muuttamalla version tilaksi **Valmis** tai **Julkaistu**.</span><span class="sxs-lookup"><span data-stu-id="4916b-177">You can publish the e-Invoicing feature by changing the version status to **Completed** or **Published**.</span></span>

### <a name="change-the-version-status-to-completed"></a><span data-ttu-id="4916b-178">Version tilan muuttaminen valmiiksi</span><span class="sxs-lookup"><span data-stu-id="4916b-178">Change the version status to Completed</span></span>

1. <span data-ttu-id="4916b-179">Valitse **Sähköisen laskutuksen toiminnot** -sivun **Versiot**-välilehdessä se sähköisen laskutuksen toiminto, jonka tilana on **Luonnos**.</span><span class="sxs-lookup"><span data-stu-id="4916b-179">On the **e-Invoicing Features** page, on the **Versions** tab, select the version of the e-Invoicing feature that has a status of **Draft**.</span></span>
2. <span data-ttu-id="4916b-180">Valitse **Muutoksen tila \> Viimeistele**.</span><span class="sxs-lookup"><span data-stu-id="4916b-180">Select **Change status \> Complete**.</span></span> 

### <a name="change-the-version-status-to-published"></a><span data-ttu-id="4916b-181">Version tilan muuttaminen julkaistuksi</span><span class="sxs-lookup"><span data-stu-id="4916b-181">Change the version status to Published</span></span> 

1. <span data-ttu-id="4916b-182">Valitse **Sähköisen laskutuksen toiminnot** -sivun **Versiot**-välilehdessä se sähköisen laskutuksen toiminto, jonka tilana on **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="4916b-182">On the **e-Invoicing Features** page, on the **Versions** tab, select the version of the e-Invoicing feature that has a status of **Completed**.</span></span>
2. <span data-ttu-id="4916b-183">Valitse **Muuta tilaa \> Julkaise**.</span><span class="sxs-lookup"><span data-stu-id="4916b-183">Select **Change status \> Publish**.</span></span>

![Sähköisen laskutuksen toiminnon tilan muuttaminen](media/e-Invoicing-services-get-started-ITA-Change-status-of-e-Invoicing-feature.png)

## <a name="set-up-the-electronic-invoicing-add-on-integration-in-finance"></a><span data-ttu-id="4916b-185">Sähköisen laskutuksen lisäosan integroinnin määritys Financessa</span><span class="sxs-lookup"><span data-stu-id="4916b-185">Set up the Electronic invoicing add-on integration in Finance</span></span>

<span data-ttu-id="4916b-186">Financen määrityksen aikana suoritat seuraavat tehtävät:</span><span class="sxs-lookup"><span data-stu-id="4916b-186">During the setup of Finance, you will complete these tasks:</span></span>

1. <span data-ttu-id="4916b-187">Tuo ER-tietomalli, ER-tietomallin yhdistämismääritys ja CFDI-laskujen kontekstimääritykset sähköisiä FatturaPA-laskuja varten.</span><span class="sxs-lookup"><span data-stu-id="4916b-187">Import the ER data model, the ER data model mapping, and the context configurations for FatturaPA e-invoices.</span></span>
2. <span data-ttu-id="4916b-188">Määritä varmenne, joka vaaditaan italialaisten sähköisten laskujen digitaaliseen allekirjoittamiseen.</span><span class="sxs-lookup"><span data-stu-id="4916b-188">Configure the certificate that is required to digitally sign Italian e-invoices.</span></span>

### <a name="import-the-er-data-model-data-model-mapping-and-formats"></a><span data-ttu-id="4916b-189">ER-tietomallin, tietomallin yhdistämismäärityksen ja muotojen tuonti</span><span class="sxs-lookup"><span data-stu-id="4916b-189">Import the ER data model, data model mapping, and formats</span></span>

1. <span data-ttu-id="4916b-190">Varmista **Sähköinen raportointi**-työtilassa, että **Liiketoiminta-asiakirjapalvelu**-määrityspalvelun tilana on **Aktiivinen**.</span><span class="sxs-lookup"><span data-stu-id="4916b-190">In the **Electronic reporting** workspace, verify that the **Business Document Service** configuration provider is set to **Active**.</span></span>
2. <span data-ttu-id="4916b-191">Valitse **Säilöt**.</span><span class="sxs-lookup"><span data-stu-id="4916b-191">Select **Repositories**.</span></span>
3. <span data-ttu-id="4916b-192">Valitse **Yleinen resurssi \> Avaa**.</span><span class="sxs-lookup"><span data-stu-id="4916b-192">Select **Global resource \> Open**.</span></span>
4. <span data-ttu-id="4916b-193">Tuo **Laskumalli**, **Laskumallin yhdistämismääritys** ja **Asiakkaan laskukontekstimalli**.</span><span class="sxs-lookup"><span data-stu-id="4916b-193">Import **Invoice model**, **Invoice model mapping**, and **Customer invoice context model**.</span></span>

#### <a name="turn-on-the-feature-for-exporting-customer-electronic-invoices-for-italy"></a><span data-ttu-id="4916b-194">Ota käyttöön toiminto, jolla viedään asiakkaan sähköisiä laskuja Italiassa</span><span class="sxs-lookup"><span data-stu-id="4916b-194">Turn on the feature for exporting customer electronic invoices for Italy</span></span>

1. <span data-ttu-id="4916b-195">Siirry kohtaan **Organisaation hallinta \> Määritys \> Sähköisten asiakirjojen parametrit**.</span><span class="sxs-lookup"><span data-stu-id="4916b-195">Go to **Organization administration \> Setup \> Electronic document parameters**.</span></span>
2. <span data-ttu-id="4916b-196">Valitse **Toiminnot**-välilehdellä **Käytössä** -valintaruutu toimintoviitteen **IT00036** rivillä.</span><span class="sxs-lookup"><span data-stu-id="4916b-196">On the **Features** tab, select the **Enabled** check box in the row for feature reference **IT00036**.</span></span>

![FatturaPA-toiminnon käyttöönotto](media/e-Invoicing-services-get-started-ITA-Enable-FatturaPA-feature.png)

#### <a name="configure-electronic-documents"></a><span data-ttu-id="4916b-198">Sähköisten asiakirjojen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="4916b-198">Configure electronic documents</span></span>

1. <span data-ttu-id="4916b-199">Siirry kohtaan **Organisaation hallinta \> Määritys \> Sähköisten asiakirjojen parametrit**.</span><span class="sxs-lookup"><span data-stu-id="4916b-199">Go to **Organization administration \> Setup \> Electronic document parameters**.</span></span>
2. <span data-ttu-id="4916b-200">Valitse **Sähköinen asiakirja**-välilehdessä **Lisää** ja syötä taulukot, joita tarvitaan italialaisten sähköisten laskujen luonnissa:</span><span class="sxs-lookup"><span data-stu-id="4916b-200">On the **Electronic document** tab, select **Add**, and enter the tables that are required to generate Italian e-invoices:</span></span>

    - <span data-ttu-id="4916b-201">**Taulukon nimi:** Asiakkaan laskukirjauskansio</span><span class="sxs-lookup"><span data-stu-id="4916b-201">**Table name:** Customer invoice journal</span></span>
    - <span data-ttu-id="4916b-202">**Taulukon nimi** Projektilasku</span><span class="sxs-lookup"><span data-stu-id="4916b-202">**Table name:** Project invoice</span></span>

3. <span data-ttu-id="4916b-203">Määritä kullekin taulukolle liittyvä asiakirjakonteksti:</span><span class="sxs-lookup"><span data-stu-id="4916b-203">For each table, define a related document context:</span></span>

    - <span data-ttu-id="4916b-204">Valitse kohdassa **Asiakkaan laskukirjauskansio** **Asiakkaan laskukonteksti**.</span><span class="sxs-lookup"><span data-stu-id="4916b-204">For **Customer invoice journal**, select **Customer invoice context**.</span></span>
    - <span data-ttu-id="4916b-205">Valitse kohdassa **Projektilasku** **Projektilaskun konteksti**.</span><span class="sxs-lookup"><span data-stu-id="4916b-205">For **Project invoice**, select **Project invoice context**.</span></span>

![Vastaustyyppien määrittäminen](media/e-Invoicing-services-get-started-ITA-Set-up-response-types.png)

## <a name="electronic-invoice-processing"></a><span data-ttu-id="4916b-207">Sähköisen laskun käsittely</span><span class="sxs-lookup"><span data-stu-id="4916b-207">Electronic invoice processing</span></span>

<span data-ttu-id="4916b-208">Financessa käsittelyn aikana suoritat seuraavat tehtävät:</span><span class="sxs-lookup"><span data-stu-id="4916b-208">During processing in Finance, you will complete these tasks:</span></span>

1. <span data-ttu-id="4916b-209">Italialaisten sähköisten laskujen luominen sähköisen laskutuksen lisäosan kautta</span><span class="sxs-lookup"><span data-stu-id="4916b-209">Generate Italian e-invoices through the Electronic invoicing add-on</span></span>
2. <span data-ttu-id="4916b-210">Suorituslokien tarkasteleminen ja käsittelytulosten arvioiminen</span><span class="sxs-lookup"><span data-stu-id="4916b-210">View the execution logs and review the results of processing</span></span>

### <a name="generate-electronic-invoices"></a><span data-ttu-id="4916b-211">Sähköisten laskujen luominen</span><span class="sxs-lookup"><span data-stu-id="4916b-211">Generate electronic invoices</span></span>

<span data-ttu-id="4916b-212">Kun otat käyttöön **Määritettävä sähköisen laskutuksen lisäosan integrointi** -toiminnon ja aktivoit **IT00036** -toiminnon, Financen vanhaa prosessia italialaisten sähköisten laskujen luomiseen ei enää voi käyttää.</span><span class="sxs-lookup"><span data-stu-id="4916b-212">After you turn on the **Configurable Electronic invoicing add-on integration** feature and activate the **IT00036** feature, the old Finance process for generating Italian e-invoices can no longer be used.</span></span> <span data-ttu-id="4916b-213">Se korvataan uudella prosessilla, jonka nimi on **Lähetä sähköiset asiakirjat**.</span><span class="sxs-lookup"><span data-stu-id="4916b-213">It's replaced by a new process that is named **Submit electronic documents**.</span></span>

<span data-ttu-id="4916b-214">Voit lähettää asiakirjat manuaalisesti riippuen sähköisten laskujen asiakirjojen tarpeestasi.</span><span class="sxs-lookup"><span data-stu-id="4916b-214">You can submit the documents manually, based on your demand for e-invoice documents.</span></span>

> [!NOTE]
> <span data-ttu-id="4916b-215">Varmista ennen jatkamista, että italialaisten sähköisten laskujen edellyttämä määritys on tehty.</span><span class="sxs-lookup"><span data-stu-id="4916b-215">Before you continue, verify that the setup that is required for Italian e-invoices was completed.</span></span> <span data-ttu-id="4916b-216">Lisätietoja: [Asiakkaiden sähköiset laskut](https://docs.microsoft.com/dynamics365/finance/localizations/emea-ita-e-invoices).</span><span class="sxs-lookup"><span data-stu-id="4916b-216">For more information, see [Customer electronic invoices](https://docs.microsoft.com/dynamics365/finance/localizations/emea-ita-e-invoices).</span></span> <span data-ttu-id="4916b-217">Huomaa, että osa kyseisessä aiheessa kuvatuista määritysvaiheista ei välttämättä ole käytettävissä sähköisen laskutuksen lisäosan aktivoinnin vuoksi.</span><span class="sxs-lookup"><span data-stu-id="4916b-217">Be aware that some of the setup steps that are described in that topic might be unavailable because of Electronic invoicing add-on activation.</span></span>

1. <span data-ttu-id="4916b-218">Siirry kohtaan **Organisaation hallinta \> Säännölliset \> Sähköiset asiakirjat \> Lähetä sähköisiä asiakirjoja**.</span><span class="sxs-lookup"><span data-stu-id="4916b-218">Go to **Organization administration \> Periodic \> Electronic documents \> Submit electronic documents**.</span></span>
2. <span data-ttu-id="4916b-219">Kun mikä tahansa asiakirja lähetetään ensimmäistä kertaa, määritä **Lähetä asiakirjat uudelleen** -asetukseksi **Ei**.</span><span class="sxs-lookup"><span data-stu-id="4916b-219">For the first submission of any document, set the **Resubmit documents** option to **No**.</span></span> <span data-ttu-id="4916b-220">Jos sinun on lähetettävä asiakirja uudelleen palvelun kautta, määritä asetukseksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="4916b-220">If you must resubmit a document through the service, set this option to **Yes**.</span></span>
3. <span data-ttu-id="4916b-221">Valitse **Sisällytettävät tietueet** -pikavälilehdessä **Suodata** avataksesi **Kysely**-valintaruudun, jossa voit muodostaa kyselyn lähetettävien asiakirjojen valitsemista varten.</span><span class="sxs-lookup"><span data-stu-id="4916b-221">On the **Records to include** FastTab, select **Filter** to open the **Inquiry** dialog box, where you can build a query to select documents for submission.</span></span>

![Sähköisten asiakirjojen lähettämisen valintaruutu](media/e-Invoicing-services-get-started-ITA-Submission-form.png)

#### <a name="filter-query"></a><span data-ttu-id="4916b-223">Suodatinkysely</span><span class="sxs-lookup"><span data-stu-id="4916b-223">Filter query</span></span>

1. <span data-ttu-id="4916b-224">Määritä **Kysely**-valintaruudussa sekä myynti- että projektilaskujen suodatusehdot tai jätä ehdot tyhjiksi, jos haluat sisällyttää kaikki lähettämättömät laskut.</span><span class="sxs-lookup"><span data-stu-id="4916b-224">In the **Inquiry** dialog box, configure the filtering conditions for both sales invoices and project invoices, or leave the conditions blank to include all unsubmitted invoices.</span></span>

    ![Lähetyksen suodatusehtojen määrittäminen](media/e-Invoicing-services-get-started-ITA-Set-up-Submission-filter-criteria.png)

2. <span data-ttu-id="4916b-226">Valitse **OK**, jotta voit sulkea **Kysely**-valintaikkunan.</span><span class="sxs-lookup"><span data-stu-id="4916b-226">Select **OK** to close the **Inquiry** dialog box.</span></span>
3. <span data-ttu-id="4916b-227">Lähetä valitut asiakirjat valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="4916b-227">Select **OK** submit the selected documents.</span></span>

> <span data-ttu-id="4916b-228">![HUOMAA] Kun yrität lähettää asiakirjan palvelun kautta ensimmäisen kerran, järjestelmä pyytää vahvistamaan yhteyden sähköisen laskutuksen lisäosaan.</span><span class="sxs-lookup"><span data-stu-id="4916b-228">![NOTE] During your first attempt to submit a document through the service, you will be prompted to confirm the connection with the Electronic invoicing add-on.</span></span> <span data-ttu-id="4916b-229">Valitse **Yhdistä sähköisten asiakirjojen lähetyspalveluun napsauttamalla tätä**.</span><span class="sxs-lookup"><span data-stu-id="4916b-229">Select **Click here to connect to Electronic Document Submission Service**.</span></span>

#### <a name="view-submission-logs"></a><span data-ttu-id="4916b-230">Lähetyslokien tarkasteleminen</span><span class="sxs-lookup"><span data-stu-id="4916b-230">View submission logs</span></span>

<span data-ttu-id="4916b-231">Voit tarkastella kaikkien lähetettyjen asiakirjojen lähetyslokeja.</span><span class="sxs-lookup"><span data-stu-id="4916b-231">You can view the submission logs for all submitted documents.</span></span>

1. <span data-ttu-id="4916b-232">Siirry kohtaan **Organisaation hallinta \> Säännölliset \> Sähköiset asiakirjat \> Sähköisen asiakirjan lähetysloki**.</span><span class="sxs-lookup"><span data-stu-id="4916b-232">Go to **Organization administration \> Periodic \> Electronic documents \> Electronic document submission log**.</span></span>
2. <span data-ttu-id="4916b-233">Valitse **Asiakirjatyyppi**-kentässä **Asiakkaan laskukirjauskansio** tai **Projektilasku** suodattaaksesi vaadittavat sähköiset asiakirjat.</span><span class="sxs-lookup"><span data-stu-id="4916b-233">In the **Document type** field, select **Customer invoice journal** or **Project invoice** to filter for the required electronic documents.</span></span>

    ![Asiakirjatyypin valinta lähetyslokien tarkastelua varten](media/e-Invoicing-services-get-started-ITA-Select-Document-type-for-viewing-submission-log.png)

    <span data-ttu-id="4916b-235">**Lähetystila** -sarakkeessa näkyvä arvo edustaa lähetysprosessin tilaa.</span><span class="sxs-lookup"><span data-stu-id="4916b-235">The value that is shown in the **Submission status** column represents the status of the submission process.</span></span> <span data-ttu-id="4916b-236">Se ilmaisee, suoritettiinko prosessi määrityksen mukaisesti ja tarvitaanko lisätoimia.</span><span class="sxs-lookup"><span data-stu-id="4916b-236">It indicates whether the process ran as configured and whether additional action is required.</span></span>

3. <span data-ttu-id="4916b-237">Valitse toimintoruudussa **Kyselyt \> Lähetystiedot** tarkastellaksesi lähetyksen toteutuslokien tietoja.</span><span class="sxs-lookup"><span data-stu-id="4916b-237">On the Action Pane, select **Inquiries \> Submission details** to view the details of the submission execution logs.</span></span>

    ![Lähetyslokitietojen tarkastelu](media/e-Invoicing-services-get-started-ITA-View-Submission-log-details.png)

4. <span data-ttu-id="4916b-239">**Käsittelytoimet** -pikavälilehdessä näkyy RCS:ssä määritetyssä toimintoversiossa määritettyjen toimien suoritusloki.</span><span class="sxs-lookup"><span data-stu-id="4916b-239">On the **Processing actions** FastTab, you can view the execution log for the actions that are configured in the feature version that was set up in RCS.</span></span> <span data-ttu-id="4916b-240">**Tila**-sarakkeessa näkyy, suoritettiinko toimi onnistuneesti.</span><span class="sxs-lookup"><span data-stu-id="4916b-240">The **Status** column shows whether the action was successfully run.</span></span>
5. <span data-ttu-id="4916b-241">**Toimitiedostot**-pikavälilehdessä näkyvät välitiedostot, jotka luotiin toimien suorittamisen aikana.</span><span class="sxs-lookup"><span data-stu-id="4916b-241">On the **Action files** FastTab, you can view the intermediate files that were generated during execution of the actions.</span></span> <span data-ttu-id="4916b-242">Voit valita **Näytä** ladataksesi tulote-XML-tiedoston **FatturaPA**-muodossa ja tarkastellaksesi sen sisältöä.</span><span class="sxs-lookup"><span data-stu-id="4916b-242">You can select **View** to download the output XML file in **FatturaPA** format and view its content.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4916b-243">Liittyvät aiheet</span><span class="sxs-lookup"><span data-stu-id="4916b-243">Related topics</span></span>

- [<span data-ttu-id="4916b-244">Sähköisen laskutuksen yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="4916b-244">Electronic invoicing add-on overview</span></span>](e-invoicing-service-overview.md)
- [<span data-ttu-id="4916b-245">Sähköisen laskutuksen lisäosan käytön aloittaminen</span><span class="sxs-lookup"><span data-stu-id="4916b-245">Get started with the Electronic invoicing add-on</span></span>](e-invoicing-get-started.md)
- [<span data-ttu-id="4916b-246">Sähköisen laskutuksen lisäosan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="4916b-246">Set up the Electronic invoicing add-on</span></span>](e-invoicing-setup.md)
