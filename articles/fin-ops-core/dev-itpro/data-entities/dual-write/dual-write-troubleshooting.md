---
title: Yleinen vianmääritys
description: Tässä artikkelissa on yleisiä vianetsintätietoja kaksoiskirjoituksen integroinnista Finance and Operations -sovellusten ja Common Data Servicen välillä.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 8cc7c11233c745719af72222eba02fb71d7a8944
ms.sourcegitcommit: 4edc658448612afbf1c1663c166d12e08e4c4165
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/06/2020
ms.locfileid: "3340927"
---
# <a name="general-troubleshooting"></a><span data-ttu-id="e373a-103">Yleinen vianmääritys</span><span class="sxs-lookup"><span data-stu-id="e373a-103">General troubleshooting</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="e373a-104">Tässä artikkelissa on yleisiä vianetsintätietoja kaksoiskirjoituksen integroinnista Finance and Operations -sovellusten ja Common Data Servicen välillä.</span><span class="sxs-lookup"><span data-stu-id="e373a-104">This topic provides general troubleshooting information for dual-write integration between Finance and Operations apps and Common Data Service.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e373a-105">Jotkin tämän ohjeaiheen osoitteet saattavat edellyttää joko järjestelmänvalvojan roolia tai Microsoftin Azure Active Directory (Azure AD) -vuokralaisen järjestelmänvalvojan valtuuksia.</span><span class="sxs-lookup"><span data-stu-id="e373a-105">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="e373a-106">Kussakin osassa selitetään, tarvitaanko tiettyä roolia tai tunnistetietoja.</span><span class="sxs-lookup"><span data-stu-id="e373a-106">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="when-you-try-to-install-the-dual-write-package-by-using-the-package-deployer-tool-no-available-solutions-are-shown"></a><span data-ttu-id="e373a-107">Kun kaksoiskirjoituspaketti yritetään asentaa paketin käyttöönottajan avulla, käytettävissä olevia ratkaisuja ei näytetä</span><span class="sxs-lookup"><span data-stu-id="e373a-107">When you try to install the dual-write package by using the package deployer tool, no available solutions are shown</span></span>

<span data-ttu-id="e373a-108">Jotkin paketin käyttöönottajan työkalun versiot eivät ole yhteensopivia kaksoiskirjoituksen ratkaisupaketin kanssa.</span><span class="sxs-lookup"><span data-stu-id="e373a-108">Some versions of the package deployer tool are incompatible with the dual-write solution package.</span></span> <span data-ttu-id="e373a-109">Jos haluat asentaa paketin onnistuneesti, varmista, että käytössä on paketin käyttöönottajan työkalun [versio 9.1.0.20](https://www.nuget.org/packages/Microsoft.CrmSdk.XrmTooling.PackageDeployment.Wpf/9.1.0.20) tai uudempi.</span><span class="sxs-lookup"><span data-stu-id="e373a-109">To successfully install the package, be sure to use [version 9.1.0.20](https://www.nuget.org/packages/Microsoft.CrmSdk.XrmTooling.PackageDeployment.Wpf/9.1.0.20) or later of the package deployer tool.</span></span>

<span data-ttu-id="e373a-110">Kun olet asentanut paketin käyttöönottajatyökalun, asenna ratkaisupaketti noudattamalla näitä ohjeita.</span><span class="sxs-lookup"><span data-stu-id="e373a-110">After you install the package deployer tool, install the solution package by following these steps.</span></span>

1. <span data-ttu-id="e373a-111">Lataa uusin ratkaisupakettitiedosto kohteesta Yammer.com.</span><span class="sxs-lookup"><span data-stu-id="e373a-111">Download the latest solution package file from Yammer.com.</span></span> <span data-ttu-id="e373a-112">Kun paketin zip-tiedosto on ladattu, napsauta sitä hiiren kakkospainikkeella ja valitse **Ominaisuudet**.</span><span class="sxs-lookup"><span data-stu-id="e373a-112">After the package zip file is downloaded, right-click it, and select **Properties**.</span></span> <span data-ttu-id="e373a-113">Valitse **Poista esto** -valintaruutu ja valitse sitten **Käytä**.</span><span class="sxs-lookup"><span data-stu-id="e373a-113">Select the **Unblock** check box, and then select **Apply**.</span></span> <span data-ttu-id="e373a-114">Jos et näe **Poista esto** -valintaruutua, zip-tiedosto on jo avattu ja voit ohittaa tämän vaiheen.</span><span class="sxs-lookup"><span data-stu-id="e373a-114">If you don't see the **Unblock** check box, the zip file is already unblocked, and you can skip this step.</span></span>

    ![Ominaisuudet -valintaikkuna](media/unblock_option.png)

2. <span data-ttu-id="e373a-116">Pura paketin zip-tiedosto ja kopioi kaikki tiedostot **Dynamics365FinanceAndOperationsCommon.PackageDeployer.2.0.438** -kansioon.</span><span class="sxs-lookup"><span data-stu-id="e373a-116">Extract the package zip file, and copy all the files in the **Dynamics365FinanceAndOperationsCommon.PackageDeployer.2.0.438** folder.</span></span>

    ![Dynamics365FinanceAndOperationsCommon.PackageDeployer.2.0.438-kansion sisältö](media/extract_package.png)

3. <span data-ttu-id="e373a-118">Liitä kaikki kopioidut tiedostot paketin käyttöönottajan **Työkalu**-kansioon.</span><span class="sxs-lookup"><span data-stu-id="e373a-118">Paste all the copied files into the **Tools** folder of the package deployer tool.</span></span> 
4. <span data-ttu-id="e373a-119">Valitse Common Data Service -ympäristö ja asenna ratkaisut suorittamalla **PackageDeployer.exe**-asiakirja.</span><span class="sxs-lookup"><span data-stu-id="e373a-119">Run **PackageDeployer.exe** to select the Common Data Service environment and install the solutions.</span></span>

    ![Työkalut-kansion sisältö](media/paste_copied_files.png)

## <a name="enable-and-view-the-plug-in-trace-log-in-common-data-service-to-view-error-details"></a><span data-ttu-id="e373a-121">Ota käyttöön ja tarkastele laajennuksen jäljitysloki, Common Data Servicessä, kun haluat tarkastella virheen tietoja</span><span class="sxs-lookup"><span data-stu-id="e373a-121">Enable and view the plug-in trace log in Common Data Service to view error details</span></span>

<span data-ttu-id="e373a-122">**Jäljityslokin ottaminen käyttöön ja virheiden tarkasteleminen:** järjestelmän hallintarooli</span><span class="sxs-lookup"><span data-stu-id="e373a-122">**Required role to turn on the trace log and view errors:** System admin</span></span>

<span data-ttu-id="e373a-123">Jäljitysloki otetaan käyttöön seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="e373a-123">To turn on the trace log, follow these steps.</span></span>

1. <span data-ttu-id="e373a-124">Kirjaudu mallipohjaiseen sovellukseen Dynamics 365:ssa, avaa **Asetukset**-sivu ja valitse sitten **Järjestelmä**-kohdasta **Hallinta**.</span><span class="sxs-lookup"><span data-stu-id="e373a-124">Sign in to the model-driven app in Dynamics 365, open the **Settings** page, and then, under **System**, select **Administration**.</span></span>
2. <span data-ttu-id="e373a-125">Valitse **Hallinta**-sivulla **Järjestelmäasetukset**.</span><span class="sxs-lookup"><span data-stu-id="e373a-125">On the **Administration** page, select **System Settings**.</span></span>
3. <span data-ttu-id="e373a-126">Ota laajennuksen jäljitysloki käyttöön valitsemalla **Mukauttaminen**-välilehden **Laajennuksen ja mukautetun työnkulun tehtävän jäljitys**-kentästä **Kaikki**.</span><span class="sxs-lookup"><span data-stu-id="e373a-126">On the **Customization** tab, in the **Plug-in and custom workflow activity tracing** field, select **All** to enable the plug-in trace log.</span></span> <span data-ttu-id="e373a-127">Jos haluat kirjata jäljityslokit vain, kun poikkeuksia ilmenee, voit valita kohdan **Poikkeus** sen sijaan.</span><span class="sxs-lookup"><span data-stu-id="e373a-127">If you want to log trace logs only when exceptions occur, you can select **Exception** instead.</span></span>


<span data-ttu-id="e373a-128">Jäljitysloki näytetään seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="e373a-128">To view the trace log, follow these steps.</span></span>

1. <span data-ttu-id="e373a-129">Kirjaudu mallipohjaiseen sovellukseen Dynamics 365:ssa, avaa **Asetukset**-sivu ja valitse sitten **Mukautus**-kohdasta **Laajennuksen jäljitysloki**.</span><span class="sxs-lookup"><span data-stu-id="e373a-129">Sign in to the model-driven app in Dynamics 365, open the **Settings** page, and then, under **Customization**, select **Plug-in Trace Log**.</span></span>
2. <span data-ttu-id="e373a-130">Etsi jäljityslokit, joiden **Tyyppinimi**-kentän arvoksi on määritetty **Microsoft.Dynamics.Integrator.DualWriteRuntime.Plugins.PreCommmitPlugin**.</span><span class="sxs-lookup"><span data-stu-id="e373a-130">Find the trace logs where the **Type Name** field is set to **Microsoft.Dynamics.Integrator.DualWriteRuntime.Plugins.PreCommmitPlugin**.</span></span>
3. <span data-ttu-id="e373a-131">Voit tarkastella koko lokia kaksoisnapsauttamalla kohdetta ja tarkistaa sitten **Suoritus**-pikavälilehdessä **Sanomalohko**-tekstin.</span><span class="sxs-lookup"><span data-stu-id="e373a-131">Double-click an item to view the full log, and then, on the **Execution** FastTab, review the **Message Block** text.</span></span>

## <a name="enable-debug-mode-to-troubleshoot-live-synchronization-issues-in-finance-and-operations-apps"></a><span data-ttu-id="e373a-132">Virheenkorjaustilan käyttöönotto Finance and Operations -sovellusten live-synkronointiongelmien vianmäärityksessä</span><span class="sxs-lookup"><span data-stu-id="e373a-132">Enable debug mode to troubleshoot live synchronization issues in Finance and Operations apps</span></span>

<span data-ttu-id="e373a-133">**Virheiden tarkastelemiseen tarvittava rooli:** Järjestelmänvalvojan kaksoiskirjoitusvirheet, jotka ovat peräisin Common Data Servicestä voivat näkyä Finance and Operations -sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="e373a-133">**Required role to view the errors:** System admin Dual-write errors that originate in Common Data Service can appear in the Finance and Operations app.</span></span> <span data-ttu-id="e373a-134">Joissakin tapauksissa virhesanoman koko teksti ei ole käytettävissä, koska sanoma on liian pitkä tai sisältää henkilökohtaisia tunnistetietoja (PII).</span><span class="sxs-lookup"><span data-stu-id="e373a-134">In some cases, the full text of the error message isn't available because the message is too long or contains personally identifying information (PII).</span></span> <span data-ttu-id="e373a-135">Noudattamalla seuraavia ohjeita voit ottaa käyttöön sanallisen kirjaamisen.</span><span class="sxs-lookup"><span data-stu-id="e373a-135">You can turn on verbose logging for errors by following these steps.</span></span>

1. <span data-ttu-id="e373a-136">Kaikilla Finance and Operations -sovellusten projektikokoonpanoilla on **IsDebugMode**-ominaisuus **DualWriteProjectConfiguration**-yksikössä.</span><span class="sxs-lookup"><span data-stu-id="e373a-136">All project configurations in Finance and Operations apps have an **IsDebugMode** property in the **DualWriteProjectConfiguration** entity.</span></span> <span data-ttu-id="e373a-137">Avaa **DualWriteProjectConfiguration**-yksikkö käyttämällä Excel-lisäosaa.</span><span class="sxs-lookup"><span data-stu-id="e373a-137">Open the **DualWriteProjectConfiguration** entity by using the Excel add-in.</span></span>

    > [!TIP]
    > <span data-ttu-id="e373a-138">Helppo tapa avata yksikkö on ottaa **Suunnittelu**-tila käyttöön Excel-lisäosalla ja lisätä sitten taulukkoon **DualWriteProjectConfigurationEntity**.</span><span class="sxs-lookup"><span data-stu-id="e373a-138">An easy way to open the entity is to turn on **Design** mode in the Excel add-in and then add **DualWriteProjectConfigurationEntity** to the worksheet.</span></span> <span data-ttu-id="e373a-139">Lisätietoja kohdassa [Avaa yksikön tiedot Excelissä ja päivittä ne käyttämällä Excel-lisäosaa](../../office-integration/use-excel-add-in.md).</span><span class="sxs-lookup"><span data-stu-id="e373a-139">For more information, see [Open entity data in Excel and update it by using the Excel add-in](../../office-integration/use-excel-add-in.md).</span></span>

2. <span data-ttu-id="e373a-140">Aseta **sDebugMode**-ominaisuuden arvoksi projektille **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="e373a-140">Set the **IsDebugMode** property to **Yes** for the project.</span></span>
3. <span data-ttu-id="e373a-141">Suorita virheitä tuottava skenaario.</span><span class="sxs-lookup"><span data-stu-id="e373a-141">Run the scenario that is generating errors.</span></span>
4. <span data-ttu-id="e373a-142">Sanalliset lokit ovat käytettävissä DualWriteErrorLog-taulussa.</span><span class="sxs-lookup"><span data-stu-id="e373a-142">The verbose logs are available in the DualWriteErrorLog table.</span></span> <span data-ttu-id="e373a-143">Voit etsiä tietoja taulukkoselaimesta käyttämällä seuraavaa URL-osoitetta (korvaa **XXX** tarvittaessa):</span><span class="sxs-lookup"><span data-stu-id="e373a-143">To look up data in the table browser, use the following URL (replace **XXX** as appropriate):</span></span>

    `https://XXXaos.cloudax.dynamics.com/?mi=SysTableBrowser&tableName=>DualWriteErrorLog`

## <a name="check-synchronization-errors-on-the-virtual-machine-for-the-finance-and-operations-app"></a><span data-ttu-id="e373a-144">Finance and Operations -sovelluksen virtuaalikoneen synkronointivirheiden tarkistaminen</span><span class="sxs-lookup"><span data-stu-id="e373a-144">Check synchronization errors on the virtual machine for the Finance and Operations app</span></span>

<span data-ttu-id="e373a-145">**Virheiden tarkastelemiseen tarvittava rooli:** Järjestelmänvalvoja</span><span class="sxs-lookup"><span data-stu-id="e373a-145">**Required role to view the errors:** System administrator</span></span>

1. <span data-ttu-id="e373a-146">Kirjaudu Microsoft Dynamics Lifecycle Servicesiin (LCS).</span><span class="sxs-lookup"><span data-stu-id="e373a-146">Sign in to Microsoft Dynamics Lifecycle Services (LCS).</span></span>
2. <span data-ttu-id="e373a-147">Avaa LCS-projekti, jonka valitsit kaksoiskirjoitustestauksen suorittamista varten.</span><span class="sxs-lookup"><span data-stu-id="e373a-147">Open the LCS project that you chose to do the dual-write testing for.</span></span>
3. <span data-ttu-id="e373a-148">Valitse **Pilvipalveluympäristöt**-ruutu.</span><span class="sxs-lookup"><span data-stu-id="e373a-148">Select the **Cloud-hosted environments** tile.</span></span>
4. <span data-ttu-id="e373a-149">Voit kirjautua Finance and Operations -sovelluksen virtuaalikoneeseen (VM) etätyöpöydän avulla.</span><span class="sxs-lookup"><span data-stu-id="e373a-149">Use Remote Desktop to sign in to the virtual machine (VM) for the Finance and Operations app.</span></span> <span data-ttu-id="e373a-150">Käytä LCS:ssä näkyvää paikallista tiliä.</span><span class="sxs-lookup"><span data-stu-id="e373a-150">Use the local account that is shown in LCS.</span></span>
5. <span data-ttu-id="e373a-151">Avaa tapahtumien katseluohjelma.</span><span class="sxs-lookup"><span data-stu-id="e373a-151">Open Event viewer.</span></span>
6. <span data-ttu-id="e373a-152">Valitse **Sovellusten ja palveluiden lokit \> Microsoft \> Dynamics \> AX -DualWriteSync \> Toiminnassa**.</span><span class="sxs-lookup"><span data-stu-id="e373a-152">Select **Applications and Services Logs \> Microsoft \> Dynamics \> AX-DualWriteSync \> Operational**.</span></span>
7. <span data-ttu-id="e373a-153">Tarkista viimeaikaisten virheiden luettelo.</span><span class="sxs-lookup"><span data-stu-id="e373a-153">Review the list of recent errors.</span></span>

## <a name="unlink-and-link-another-common-data-service-environment-from-a-finance-and-operations-app"></a><span data-ttu-id="e373a-154">Toisen Common Data Service -ympäristön linkityksen poistaminen Finance and Operations -sovelluksesta</span><span class="sxs-lookup"><span data-stu-id="e373a-154">Unlink and link another Common Data Service environment from a Finance and Operations app</span></span>

<span data-ttu-id="e373a-155">**Ympäristön linkityksen poistamiseen vaadittu rooli:** Joko Finance and Operations -sovelluksen tai Common Data Service -ohjelman järjestelmänvalvoja.</span><span class="sxs-lookup"><span data-stu-id="e373a-155">**Required role to unlink the environment:** System administrator for either Finance and Operations app or Common Data Service.</span></span>

1. <span data-ttu-id="e373a-156">Kirjautuminen Finance and Operations -sovellukseen.</span><span class="sxs-lookup"><span data-stu-id="e373a-156">Sign in to the Finance and Operations app.</span></span>
2. <span data-ttu-id="e373a-157">Siirry kohtaan **Työtilat \> Tietojen hallinta** ja valitse **Kaksoiskirjoitus**-ruutu.</span><span class="sxs-lookup"><span data-stu-id="e373a-157">Go to **Workspaces \> Data management**, and select the **Dual Write** tile.</span></span>
3. <span data-ttu-id="e373a-158">Valitse kaikki käynnissä olevat yhdistämismääritykset ja valitse sitten **Pysäytä**.</span><span class="sxs-lookup"><span data-stu-id="e373a-158">Select all running mappings, and then select **Stop**.</span></span>
4. <span data-ttu-id="e373a-159">Valitse **Poista ympäristön linkitys**.</span><span class="sxs-lookup"><span data-stu-id="e373a-159">Select **Unlink environment**.</span></span>
5. <span data-ttu-id="e373a-160">Vahvista toiminto valitsemalla **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="e373a-160">Select **Yes** to confirm the operation.</span></span>

<span data-ttu-id="e373a-161">Nyt voit linkittää uuden ympäristön.</span><span class="sxs-lookup"><span data-stu-id="e373a-161">You can now link a new environment.</span></span>

## <a name="unable-to-view-the-sales-order-line-information-form"></a><span data-ttu-id="e373a-162">Myyntitilausrivin tietolomaketta ei voi tarkastella</span><span class="sxs-lookup"><span data-stu-id="e373a-162">Unable to view the sales order line Information form</span></span> 

<span data-ttu-id="e373a-163">Kun luot myyntitilauksen Dynamics 365 Salesissa, **+ Lisää tuotteet** -vaihtoehdon napsauttaminen saattaa ohjata sinut Dynamics 365 Project Operationsin tilausrivilomakkeeseen.</span><span class="sxs-lookup"><span data-stu-id="e373a-163">When you create a sales order in Dynamics 365 Sales, clicking on **+ Add products** might redirect you to the Dynamics 365 Project Operations order line form.</span></span> <span data-ttu-id="e373a-164">Kyseisessä lomakkeessa ei ole mitään tapaa tarkastella myyntitilausrivin **Tieto**-lomaketta.</span><span class="sxs-lookup"><span data-stu-id="e373a-164">There is no way from that form to view the sales order line **Information** form.</span></span> <span data-ttu-id="e373a-165">**Tietoja**-vaihtoehto ei näy **Uuden tilausrivin** alla olevassa avattavassa valikossa.</span><span class="sxs-lookup"><span data-stu-id="e373a-165">The option for **Information** does not appear in the dropdown below **New Order Line**.</span></span> <span data-ttu-id="e373a-166">Näin tapahtuu, koska Project Operations on asennettu ympäristöösi.</span><span class="sxs-lookup"><span data-stu-id="e373a-166">This happens because Project Operations has been installed in your environment.</span></span>

<span data-ttu-id="e373a-167">Voit ottaa **Tieto**-lomakevaihtoehdon uudelleen käyttöön seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="e373a-167">To re-enable the **Information** form option, follow these steps:</span></span>
1. <span data-ttu-id="e373a-168">Siirry **Tilausrivi**-yksikköön.</span><span class="sxs-lookup"><span data-stu-id="e373a-168">Navigate to the **Order Line** entity.</span></span>
2. <span data-ttu-id="e373a-169">Etsi **Tieto**-lomake lomakkeet-solmussa.</span><span class="sxs-lookup"><span data-stu-id="e373a-169">Find the **Information** form under the forms node.</span></span> 
3. <span data-ttu-id="e373a-170">Valitse **Tieto**-lomake ja valitse **Ota käyttöön käyttöoikeusroolit**.</span><span class="sxs-lookup"><span data-stu-id="e373a-170">Select the **Information** form and click **Enable security roles**.</span></span> 
4. <span data-ttu-id="e373a-171">Muuta suojausasetukseksi **Näytä kaikille**.</span><span class="sxs-lookup"><span data-stu-id="e373a-171">Change the security setting to **Display to everyone**.</span></span>
