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
ms.openlocfilehash: f7ee0b5aa4e72614205e129acd986376b33efc70
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172688"
---
# <a name="general-troubleshooting"></a><span data-ttu-id="3fb51-103">Yleinen vianmääritys</span><span class="sxs-lookup"><span data-stu-id="3fb51-103">General troubleshooting</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="3fb51-104">Tässä artikkelissa on yleisiä vianetsintätietoja kaksoiskirjoituksen integroinnista Finance and Operations -sovellusten ja Common Data Servicen välillä.</span><span class="sxs-lookup"><span data-stu-id="3fb51-104">This topic provides general troubleshooting information for dual-write integration between Finance and Operations apps and Common Data Service.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3fb51-105">Jotkin tämän ohjeaiheen osoitteet saattavat edellyttää joko järjestelmänvalvojan roolia tai Microsoftin Azure Active Directory (Azure AD) -vuokralaisen järjestelmänvalvojan valtuuksia.</span><span class="sxs-lookup"><span data-stu-id="3fb51-105">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="3fb51-106">Kussakin osassa selitetään, tarvitaanko tiettyä roolia tai tunnistetietoja.</span><span class="sxs-lookup"><span data-stu-id="3fb51-106">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="when-you-try-to-install-the-dual-write-package-by-using-the-package-deployer-tool-no-available-solutions-are-shown"></a><span data-ttu-id="3fb51-107">Kun kaksoiskirjoituspaketti yritetään asentaa paketin käyttöönottajan avulla, käytettävissä olevia ratkaisuja ei näytetä</span><span class="sxs-lookup"><span data-stu-id="3fb51-107">When you try to install the dual-write package by using the package deployer tool, no available solutions are shown</span></span>

<span data-ttu-id="3fb51-108">Jotkin paketin käyttöönottajan työkalun versiot eivät ole yhteensopivia kaksoiskirjoituksen ratkaisupaketin kanssa.</span><span class="sxs-lookup"><span data-stu-id="3fb51-108">Some versions of the package deployer tool are incompatible with the dual-write solution package.</span></span> <span data-ttu-id="3fb51-109">Jos haluat asentaa paketin onnistuneesti, varmista, että käytössä on paketin käyttöönottajan työkalun [versio 9.1.0.20](https://www.nuget.org/packages/Microsoft.CrmSdk.XrmTooling.PackageDeployment.Wpf/9.1.0.20) tai uudempi.</span><span class="sxs-lookup"><span data-stu-id="3fb51-109">To successfully install the package, be sure to use [version 9.1.0.20](https://www.nuget.org/packages/Microsoft.CrmSdk.XrmTooling.PackageDeployment.Wpf/9.1.0.20) or later of the package deployer tool.</span></span>

<span data-ttu-id="3fb51-110">Kun olet asentanut paketin käyttöönottajatyökalun, asenna ratkaisupaketti noudattamalla näitä ohjeita.</span><span class="sxs-lookup"><span data-stu-id="3fb51-110">After you install the package deployer tool, install the solution package by following these steps.</span></span>

1. <span data-ttu-id="3fb51-111">Lataa uusin ratkaisupakettitiedosto kohteesta Yammer.com.</span><span class="sxs-lookup"><span data-stu-id="3fb51-111">Download the latest solution package file from Yammer.com.</span></span> <span data-ttu-id="3fb51-112">Kun paketin zip-tiedosto on ladattu, napsauta sitä hiiren kakkospainikkeella ja valitse **Ominaisuudet**.</span><span class="sxs-lookup"><span data-stu-id="3fb51-112">After the package zip file is downloaded, right-click it, and select **Properties**.</span></span> <span data-ttu-id="3fb51-113">Valitse **Poista esto** -valintaruutu ja valitse sitten **Käytä**.</span><span class="sxs-lookup"><span data-stu-id="3fb51-113">Select the **Unblock** check box, and then select **Apply**.</span></span> <span data-ttu-id="3fb51-114">Jos et näe **Poista esto** -valintaruutua, zip-tiedosto on jo avattu ja voit ohittaa tämän vaiheen.</span><span class="sxs-lookup"><span data-stu-id="3fb51-114">If you don't see the **Unblock** check box, the zip file is already unblocked, and you can skip this step.</span></span>

    ![Ominaisuudet -valintaikkuna](media/unblock_option.png)

2. <span data-ttu-id="3fb51-116">Pura paketin zip-tiedosto ja kopioi kaikki tiedostot **Dynamics365FinanceAndOperationsCommon.PackageDeployer.2.0.438** -kansioon.</span><span class="sxs-lookup"><span data-stu-id="3fb51-116">Extract the package zip file, and copy all the files in the **Dynamics365FinanceAndOperationsCommon.PackageDeployer.2.0.438** folder.</span></span>

    ![Dynamics365FinanceAndOperationsCommon.PackageDeployer.2.0.438-kansion sisältö](media/extract_package.png)

3. <span data-ttu-id="3fb51-118">Liitä kaikki kopioidut tiedostot paketin käyttöönottajan **Työkalu**-kansioon.</span><span class="sxs-lookup"><span data-stu-id="3fb51-118">Paste all the copied files into the **Tools** folder of the package deployer tool.</span></span> 
4. <span data-ttu-id="3fb51-119">Valitse Common Data Service -ympäristö ja asenna ratkaisut suorittamalla **PackageDeployer.exe**-asiakirja.</span><span class="sxs-lookup"><span data-stu-id="3fb51-119">Run **PackageDeployer.exe** to select the Common Data Service environment and install the solutions.</span></span>

    ![Työkalut-kansion sisältö](media/paste_copied_files.png)

## <a name="enable-and-view-the-plug-in-trace-log-in-common-data-service-to-view-error-details"></a><span data-ttu-id="3fb51-121">Ota käyttöön ja tarkastele laajennuksen jäljitysloki, Common Data Servicessä, kun haluat tarkastella virheen tietoja</span><span class="sxs-lookup"><span data-stu-id="3fb51-121">Enable and view the plug-in trace log in Common Data Service to view error details</span></span>

<span data-ttu-id="3fb51-122">**Jäljityslokin ottaminen käyttöön ja virheiden tarkasteleminen:** järjestelmän hallintarooli</span><span class="sxs-lookup"><span data-stu-id="3fb51-122">**Required role to turn on the trace log and view errors:** System admin</span></span>

<span data-ttu-id="3fb51-123">Jäljitysloki otetaan käyttöön seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="3fb51-123">To turn on the trace log, follow these steps.</span></span>

1. <span data-ttu-id="3fb51-124">Kirjaudu Finance and Operations -sovellukseen, avaa **Asetukset**-sivu ja valitse sitten **Järjestelmä**-kohdasta **Hallinta**.</span><span class="sxs-lookup"><span data-stu-id="3fb51-124">Sign in to the Finance and Operations app, open the **Settings** page, and then, under **System**, select **Administration**.</span></span>
2. <span data-ttu-id="3fb51-125">Valitse **Hallinta**-sivulla **Järjestelmäasetukset**.</span><span class="sxs-lookup"><span data-stu-id="3fb51-125">On the **Administration** page, select **System Settings**.</span></span>
3. <span data-ttu-id="3fb51-126">Ota laajennuksen jäljitysloki käyttöön valitsemalla **Mukauttaminen**-välilehden **Laajennuksen ja mukautetun työnkulun tehtävän jäljitys**-kentästä **Kaikki**.</span><span class="sxs-lookup"><span data-stu-id="3fb51-126">On the **Customization** tab, in the **Plug-in and custom workflow activity tracing** field, select **All** to enable the plug-in trace log.</span></span> <span data-ttu-id="3fb51-127">Jos haluat kirjata jäljityslokit vain, kun poikkeuksia ilmenee, voit valita kohdan **Poikkeus** sen sijaan.</span><span class="sxs-lookup"><span data-stu-id="3fb51-127">If you want to log trace logs only when exceptions occur, you can select **Exception** instead.</span></span>


<span data-ttu-id="3fb51-128">Jäljitysloki näytetään seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="3fb51-128">To view the trace log, follow these steps.</span></span>

1. <span data-ttu-id="3fb51-129">Kirjaudu Finance and Operations -sovellukseen, avaa **Asetukset**-sivu ja valitse sitten **Mukautus**-kohdasta **Laajennuksen jäljitysloki**.</span><span class="sxs-lookup"><span data-stu-id="3fb51-129">Sign in to the Finance and Operations app, open the **Settings** page, and then, under **Customization**, select **Plug-in Trace Log**.</span></span>
2. <span data-ttu-id="3fb51-130">Etsi jäljityslokit, joiden **Tyyppinimi**-kentän arvoksi on määritetty **Microsoft.Dynamics.Integrator.CrmPlugins.Plugin**.</span><span class="sxs-lookup"><span data-stu-id="3fb51-130">Find the trace logs where the **Type Name** field is set to **Microsoft.Dynamics.Integrator.CrmPlugins.Plugin**.</span></span>
3. <span data-ttu-id="3fb51-131">Voit tarkastella koko lokia kaksoisnapsauttamalla kohdetta ja tarkistaa sitten **Suoritus**-pikavälilehdessä **Sanomalohko**-tekstin.</span><span class="sxs-lookup"><span data-stu-id="3fb51-131">Double-click an item to view the full log, and then, on the **Execution** FastTab, review the **Message Block** text.</span></span>

## <a name="enable-debug-mode-to-troubleshoot-live-synchronization-issues-in-finance-and-operations-apps"></a><span data-ttu-id="3fb51-132">Virheenkorjaustilan käyttöönotto Finance and Operations -sovellusten live-synkronointiongelmien vianmäärityksessä</span><span class="sxs-lookup"><span data-stu-id="3fb51-132">Enable debug mode to troubleshoot live synchronization issues in Finance and Operations apps</span></span>

<span data-ttu-id="3fb51-133">**Virheiden tarkastelemiseen tarvittava rooli:** Järjestelmänvalvoja</span><span class="sxs-lookup"><span data-stu-id="3fb51-133">**Required role to view the errors:** System admin</span></span>

<span data-ttu-id="3fb51-134">Sovellukseen perustuvat kaksoiskirjoitusvirheet Common Data Servicessä voivat näkyä Finance and Operations -sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="3fb51-134">Dual-write errors that originate in Common Data Service can appear in the Finance and Operations app.</span></span> <span data-ttu-id="3fb51-135">Joissakin tapauksissa virhesanoman koko teksti ei ole käytettävissä, koska sanoma on liian pitkä tai sisältää henkilökohtaisia tunnistetietoja (PII).</span><span class="sxs-lookup"><span data-stu-id="3fb51-135">In some cases, the full text of the error message isn't available because the message is too long or contains personally identifying information (PII).</span></span> <span data-ttu-id="3fb51-136">Noudattamalla seuraavia ohjeita voit ottaa käyttöön sanallisen kirjaamisen.</span><span class="sxs-lookup"><span data-stu-id="3fb51-136">You can turn on verbose logging for errors by following these steps.</span></span>

1. <span data-ttu-id="3fb51-137">Kaikilla Finance and Operations -sovellusten projektikokoonpanoilla on **IsDebugMode**-ominaisuus **DualWriteProjectConfiguration**-yksikössä.</span><span class="sxs-lookup"><span data-stu-id="3fb51-137">All project configurations in Finance and Operations apps have an **IsDebugMode** property in the **DualWriteProjectConfiguration** entity.</span></span> <span data-ttu-id="3fb51-138">Avaa **DualWriteProjectConfiguration**-yksikkö käyttämällä Excel-lisäosaa.</span><span class="sxs-lookup"><span data-stu-id="3fb51-138">Open the **DualWriteProjectConfiguration** entity by using the Excel add-in.</span></span>

    > [!TIP]
    > <span data-ttu-id="3fb51-139">Helppo tapa avata yksikkö on ottaa **Suunnittelu**-tila käyttöön Excel-lisäosalla ja lisätä sitten taulukkoon **DualWriteProjectConfigurationEntity**.</span><span class="sxs-lookup"><span data-stu-id="3fb51-139">An easy way to open the entity is to turn on **Design** mode in the Excel add-in and then add **DualWriteProjectConfigurationEntity** to the worksheet.</span></span> <span data-ttu-id="3fb51-140">Lisätietoja kohdassa [Avaa yksikön tiedot Excelissä ja päivittä ne käyttämällä Excel-lisäosaa](../../office-integration/use-excel-add-in.md).</span><span class="sxs-lookup"><span data-stu-id="3fb51-140">For more information, see [Open entity data in Excel and update it by using the Excel add-in](../../office-integration/use-excel-add-in.md).</span></span>

2. <span data-ttu-id="3fb51-141">Aseta **sDebugMode**-ominaisuuden arvoksi projektille **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="3fb51-141">Set the **IsDebugMode** property to **Yes** for the project.</span></span>
3. <span data-ttu-id="3fb51-142">Suorita virheitä tuottava skenaario.</span><span class="sxs-lookup"><span data-stu-id="3fb51-142">Run the scenario that is generating errors.</span></span>
4. <span data-ttu-id="3fb51-143">Sanalliset lokit ovat käytettävissä DualWriteErrorLog-taulussa.</span><span class="sxs-lookup"><span data-stu-id="3fb51-143">The verbose logs are available in the DualWriteErrorLog table.</span></span> <span data-ttu-id="3fb51-144">Voit etsiä tietoja taulukkoselaimesta käyttämällä seuraavaa URL-osoitetta (korvaa **XXX** tarvittaessa):</span><span class="sxs-lookup"><span data-stu-id="3fb51-144">To look up data in the table browser, use the following URL (replace **XXX** as appropriate):</span></span>

    `https://XXXaos.cloudax.dynamics.com/?mi=SysTableBrowser&tableName=>DualWriteErrorLog`

## <a name="check-synchronization-errors-on-the-virtual-machine-for-the-finance-and-operations-app"></a><span data-ttu-id="3fb51-145">Finance and Operations -sovelluksen virtuaalikoneen synkronointivirheiden tarkistaminen</span><span class="sxs-lookup"><span data-stu-id="3fb51-145">Check synchronization errors on the virtual machine for the Finance and Operations app</span></span>

<span data-ttu-id="3fb51-146">**Virheiden tarkastelemiseen tarvittava rooli:** Järjestelmänvalvoja</span><span class="sxs-lookup"><span data-stu-id="3fb51-146">**Required role to view the errors:** System admin</span></span>

1. <span data-ttu-id="3fb51-147">Kirjaudu Microsoft Dynamics Lifecycle Servicesiin (LCS).</span><span class="sxs-lookup"><span data-stu-id="3fb51-147">Sign in to Microsoft Dynamics Lifecycle Services (LCS).</span></span>
2. <span data-ttu-id="3fb51-148">Avaa LCS-projekti, jonka valitsit kaksoiskirjoitustestauksen suorittamista varten.</span><span class="sxs-lookup"><span data-stu-id="3fb51-148">Open the LCS project that you chose to do the dual-write testing for.</span></span>
3. <span data-ttu-id="3fb51-149">Valitse **Pilvipalveluympäristöt**-ruutu.</span><span class="sxs-lookup"><span data-stu-id="3fb51-149">Select the **Cloud-hosted environments** tile.</span></span>
4. <span data-ttu-id="3fb51-150">Voit kirjautua Finance and Operations -sovelluksen virtuaalikoneeseen (VM) etätyöpöydän avulla.</span><span class="sxs-lookup"><span data-stu-id="3fb51-150">Use Remote Desktop to sign in to the virtual machine (VM) for the Finance and Operations app.</span></span> <span data-ttu-id="3fb51-151">Käytä LCS:ssä näkyvää paikallista tiliä.</span><span class="sxs-lookup"><span data-stu-id="3fb51-151">Use the local account that is shown in LCS.</span></span>
5. <span data-ttu-id="3fb51-152">Avaa tapahtumien katseluohjelma.</span><span class="sxs-lookup"><span data-stu-id="3fb51-152">Open Event viewer.</span></span>
6. <span data-ttu-id="3fb51-153">Valitse **Sovellusten ja palveluiden lokit \> Microsoft \> Dynamics \> AX -DualWriteSync \> Toiminnassa**.</span><span class="sxs-lookup"><span data-stu-id="3fb51-153">Select **Applications and Services Logs \> Microsoft \> Dynamics \> AX-DualWriteSync \> Operational**.</span></span>
7. <span data-ttu-id="3fb51-154">Tarkista viimeaikaisten virheiden luettelo.</span><span class="sxs-lookup"><span data-stu-id="3fb51-154">Review the list of recent errors.</span></span>

## <a name="unlink-and-link-another-common-data-service-environment-from-a-finance-and-operations-app"></a><span data-ttu-id="3fb51-155">Toisen Common Data Service -ympäristön linkityksen poistaminen Finance and Operations -sovelluksesta</span><span class="sxs-lookup"><span data-stu-id="3fb51-155">Unlink and link another Common Data Service environment from a Finance and Operations app</span></span>

<span data-ttu-id="3fb51-156">**Ympäristön linkityksen edellyttämät tunnistetiedot:** Azure AD -vuokralaisten hallinta</span><span class="sxs-lookup"><span data-stu-id="3fb51-156">**Required credentials to unlink the environment:** Azure AD tenant admin</span></span>

1. <span data-ttu-id="3fb51-157">Kirjautuminen Finance and Operations -sovellukseen.</span><span class="sxs-lookup"><span data-stu-id="3fb51-157">Sign in to the Finance and Operations app.</span></span>
2. <span data-ttu-id="3fb51-158">Siirry kohtaan **Työtilat \> Tietojen hallinta** ja valitse **Kaksoiskirjoitus**-ruutu.</span><span class="sxs-lookup"><span data-stu-id="3fb51-158">Go to **Workspaces \> Data management**, and select the **Dual Write** tile.</span></span>
3. <span data-ttu-id="3fb51-159">Valitse kaikki käynnissä olevat yhdistämismääritykset ja valitse sitten **Pysäytä**.</span><span class="sxs-lookup"><span data-stu-id="3fb51-159">Select all running mappings, and then select **Stop**.</span></span>
4. <span data-ttu-id="3fb51-160">Valitse **Poista ympäristön linkitys**.</span><span class="sxs-lookup"><span data-stu-id="3fb51-160">Select **Unlink environment**.</span></span>
5. <span data-ttu-id="3fb51-161">Vahvista toiminto valitsemalla **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="3fb51-161">Select **Yes** to confirm the operation.</span></span>

<span data-ttu-id="3fb51-162">Nyt voit linkittää uuden ympäristön.</span><span class="sxs-lookup"><span data-stu-id="3fb51-162">You can now link a new environment.</span></span>
