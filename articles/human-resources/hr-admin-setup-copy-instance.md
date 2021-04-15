---
title: Kopioi esiintymä
description: Microsoft Dynamics 365 Human Resources -tietokannan voi kopioida eristysympäristöön Microsoft Dynamics Lifecycle Servicesin (LCS) avulla.
author: andreabichsel
ms.date: 07/22/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6cb8050980b9b54480d09a59379430cd229ff141
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801092"
---
# <a name="copy-an-instance"></a><span data-ttu-id="8c99d-103">Kopioi esiintymä</span><span class="sxs-lookup"><span data-stu-id="8c99d-103">Copy an instance</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="8c99d-104">Microsoft Dynamics 365 Human Resources -tietokannan voi kopioida eristysympäristöön Microsoft Dynamics Lifecycle Servicesin (LCS) avulla.</span><span class="sxs-lookup"><span data-stu-id="8c99d-104">You can use Microsoft Dynamics Lifecycle Services (LCS) to copy a Microsoft Dynamics 365 Human Resources database to a sandbox environment.</span></span> <span data-ttu-id="8c99d-105">Jos käytössä on toinen eristysympäristö, voit kopioida myös tietokannan siitä kohde-eristysympäristöön.</span><span class="sxs-lookup"><span data-stu-id="8c99d-105">If you have another sandbox environment, you can also copy the database from that environment to a targeted sandbox environment.</span></span>

<span data-ttu-id="8c99d-106">Esiintymää kopioitaessa kannattaa muistaa seuraavat vinkit:</span><span class="sxs-lookup"><span data-stu-id="8c99d-106">To copy an instance, keep the following tips in mind:</span></span>

- <span data-ttu-id="8c99d-107">Korvattavan Human Resources -esiintymän on oltava eristysympäristö.</span><span class="sxs-lookup"><span data-stu-id="8c99d-107">The Human Resources instance you want to overwrite must be a sandbox environment.</span></span>

- <span data-ttu-id="8c99d-108">Kopioinnin lähde- ja kohdeympäristöjen on oltava samalla alueella.</span><span class="sxs-lookup"><span data-stu-id="8c99d-108">The environments you're copying from and to must be in the same region.</span></span> <span data-ttu-id="8c99d-109">Et voi kopioida eri alueiden välillä.</span><span class="sxs-lookup"><span data-stu-id="8c99d-109">You can't copy across regions.</span></span>

- <span data-ttu-id="8c99d-110">Sinun on oltava kohdeympäristön järjestelmänvalvoja, jotta voit kirjautua siihen, kun olet kopioinut esiintymän.</span><span class="sxs-lookup"><span data-stu-id="8c99d-110">You must be an Administrator in the target environment so you can sign into it after copying the instance.</span></span>

- <span data-ttu-id="8c99d-111">Kun kopioit Human Resourcesin tietokannan, et kopioi elementtejä (sovelluksia tai tietoja), jotka sisältyvät Microsoft Power Apps -ympäristöön.</span><span class="sxs-lookup"><span data-stu-id="8c99d-111">When you copy the Human Resources database, you don't copy the elements (apps or data) that are contained in a Microsoft Power Apps environment.</span></span> <span data-ttu-id="8c99d-112">Lisätietoja elementtien kopioinnista Power Apps-ympäristössä on kohdassa [Ympäristön kopioiminen](https://docs.microsoft.com/power-platform/admin/copy-environment).</span><span class="sxs-lookup"><span data-stu-id="8c99d-112">For information about how to copy elements in a Power Apps environment, see [Copy an environment](https://docs.microsoft.com/power-platform/admin/copy-environment).</span></span> <span data-ttu-id="8c99d-113">Korvattavan Power Apps-ympäristön on oltava eristysympäristö.</span><span class="sxs-lookup"><span data-stu-id="8c99d-113">The Power Apps environment you want to overwrite must be a sandbox environment.</span></span> <span data-ttu-id="8c99d-114">Sinun on oltava yleinen vuokraajan järjestelmänvalvoja, jotta voit muuttaa Power Apps-tuotantoympäristön eristysympäristöksi.</span><span class="sxs-lookup"><span data-stu-id="8c99d-114">You must be a global tenant admin to change a Power Apps production environment to a sandbox environment.</span></span> <span data-ttu-id="8c99d-115">Lisä tietoja Power Apps-ympäristön muuttamisesta on kohdassa [Esiintymän vaihtaminen](https://docs.microsoft.com/dynamics365/admin/switch-instance).</span><span class="sxs-lookup"><span data-stu-id="8c99d-115">For more information about changing a Power Apps environment, see [Switch an instance](https://docs.microsoft.com/dynamics365/admin/switch-instance).</span></span>

- <span data-ttu-id="8c99d-116">Jos kopioit esiintymään eristysympäristöön ja haluat integroida eristysympäristön Dataversen kanssa, mukautetut kentät on otettava uudelleen Dataverse-taulukoissa.</span><span class="sxs-lookup"><span data-stu-id="8c99d-116">If you copy an instance into your sandbox environment and want to integrate your sandbox environment with Dataverse, you must reapply custom fields to Dataverse tables.</span></span> <span data-ttu-id="8c99d-117">Lisätietoja on kohdassa [Mukautettujen kenttien käyttäminen Dataversessä](hr-admin-setup-copy-instance.md?apply-custom-fields-to-common-data-service).</span><span class="sxs-lookup"><span data-stu-id="8c99d-117">See [Apply custom fields to Dataverse](hr-admin-setup-copy-instance.md?apply-custom-fields-to-common-data-service).</span></span>

## <a name="effects-of-copying-a-human-resources-database"></a><span data-ttu-id="8c99d-118">Human Resources -tietokannan kopioinnin vaikutukset</span><span class="sxs-lookup"><span data-stu-id="8c99d-118">Effects of copying a Human Resources database</span></span>

<span data-ttu-id="8c99d-119">Human Resources -tietokannan kopioinnin yhteydessä tapahtuu seuraavaa:</span><span class="sxs-lookup"><span data-stu-id="8c99d-119">The following events occur when you copy a Human Resources database:</span></span>

- <span data-ttu-id="8c99d-120">Kopiointiprosessi poistaa aiemmin luodun tietokannan kohdeympäristöstä.</span><span class="sxs-lookup"><span data-stu-id="8c99d-120">The copy process erases the existing database in the target environment.</span></span> <span data-ttu-id="8c99d-121">Kun kopiointiprosessi on suoritettu, et voi palauttaa aiemmin luotua tietokantaa.</span><span class="sxs-lookup"><span data-stu-id="8c99d-121">After the copy process is completed, you can't recover the existing database.</span></span>

- <span data-ttu-id="8c99d-122">Kohdeympäristö ei ole käytettävissä, ennen kuin kopiointiprosessi on valmis.</span><span class="sxs-lookup"><span data-stu-id="8c99d-122">The target environment will be unavailable until the copy process is completed.</span></span>

- <span data-ttu-id="8c99d-123">Microsoft Azure Blob -tallennustilassa olevia asiakirjoja ei kopioida ympäristöstä toiseen.</span><span class="sxs-lookup"><span data-stu-id="8c99d-123">Documents in Microsoft Azure Blob storage aren't copied from one environment to another.</span></span> <span data-ttu-id="8c99d-124">Tämän vuoksi liitettyjä asiakirjoja ja malleja ei kopioida, ja ne jäävät lähdeympäristöön.</span><span class="sxs-lookup"><span data-stu-id="8c99d-124">As a result, any documents and templates that are attached won't be copied and will remain in the source environment.</span></span>

- <span data-ttu-id="8c99d-125">Mitkään käyttäjät, paitsi järjestelmänvalvojakäyttäjä ja muut sisäisen palvelun käyttäjätilit eivät ole käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="8c99d-125">All users except the Admin user and other internal service user accounts will be unavailable.</span></span> <span data-ttu-id="8c99d-126">Järjestelmänvalvojakäyttäjä voi poistaa tietoja tai piilottaa niitä näkyvistä, ennen kuin muut käyttäjät pääsevät takaisin järjestelmään.</span><span class="sxs-lookup"><span data-stu-id="8c99d-126">The Admin user can delete or obfuscate data before other users are allowed back into the system.</span></span>

- <span data-ttu-id="8c99d-127">Järjestelmänvalvojakäyttäjän on suoritettava vaadittavat muutokset määrityksiin, kuten yhdistettävä integroinnin päätepisteet uudelleen tiettyihin palveluihin tai URL-osoitteisiin.</span><span class="sxs-lookup"><span data-stu-id="8c99d-127">The Admin user must make required configuration changes, such as reconnecting integration endpoints to specific services or URLs.</span></span>

## <a name="copy-the-human-resources-database"></a><span data-ttu-id="8c99d-128">Human Resources -tietokannan kopiointi</span><span class="sxs-lookup"><span data-stu-id="8c99d-128">Copy the Human Resources database</span></span>

<span data-ttu-id="8c99d-129">Jos haluat suorittaa tämän tehtävän, kopioi ensin esiintymä ja kirjaudu sitten Microsoft Power Platform -hallintakeskukseen ja kopioi Power Apps-ympäristösi.</span><span class="sxs-lookup"><span data-stu-id="8c99d-129">To complete this task, you first copy an instance, and then sign in to the Microsoft Power Platform Admin Center to copy your Power Apps environment.</span></span>

> [!WARNING]
> <span data-ttu-id="8c99d-130">Kun kopioit esiintymän, tietokanta poistetaan kohde-esiintymästä.</span><span class="sxs-lookup"><span data-stu-id="8c99d-130">When you copy an instance, the database is erased in the target instance.</span></span> <span data-ttu-id="8c99d-131">Kohde-esiintymä ei ole käytettävissä tämän prosessin aikana.</span><span class="sxs-lookup"><span data-stu-id="8c99d-131">The target instance is unavailable during this process.</span></span>

1. <span data-ttu-id="8c99d-132">Kirjaudu LCS:ään ja valitse LCS-projekti, joka sisältää kopioitavan esiintymän.</span><span class="sxs-lookup"><span data-stu-id="8c99d-132">Sign in to LCS, and select the LCS project that contains the instance that you want to copy.</span></span>

2. <span data-ttu-id="8c99d-133">Valitse LCS-projektin **Human Resources -sovelluksen hallinta** -ruutu.</span><span class="sxs-lookup"><span data-stu-id="8c99d-133">In your LCS project, select the **Human Resources App Management** tile.</span></span>

3. <span data-ttu-id="8c99d-134">Valitse kopioitava esiintymä ja sitten **Kopioi**.</span><span class="sxs-lookup"><span data-stu-id="8c99d-134">Select the instance to copy, and then select **Copy**.</span></span>

4. <span data-ttu-id="8c99d-135">Valitse korvattava esiintymä **Kopioi esiintymä** -tehtäväruudusta ja valitse sitten **Kopioi**.</span><span class="sxs-lookup"><span data-stu-id="8c99d-135">In the **Copy an instance** task pane, select the instance to overwrite, and then select **Copy**.</span></span> <span data-ttu-id="8c99d-136">Odota, että **Kopioi tila** -kentän arvoksi päivittyy **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="8c99d-136">Wait for the value of the **Copy status** field to be updated to **Completed**.</span></span>

   ![[<span data-ttu-id="8c99d-137">Valitse korvattava esiintymä</span><span class="sxs-lookup"><span data-stu-id="8c99d-137">Select instance to overwrite</span></span>](./media/copy-instance-select-target-instance.png)](./media/copy-instance-select-target-instance.png)

5. <span data-ttu-id="8c99d-138">Valitse **Power Platform** ja kirjaudu Microsoft Power Platform -hallintakeskukseen.</span><span class="sxs-lookup"><span data-stu-id="8c99d-138">Select **Power Platform**, and sign in to the Microsoft Power Platform Admin Center.</span></span>

   ![[<span data-ttu-id="8c99d-139">Valitse Power Platform</span><span class="sxs-lookup"><span data-stu-id="8c99d-139">Select Power Platform</span></span>](./media/copy-instance-select-power-platform.png)](./media/copy-instance-select-power-platform.png)

6. <span data-ttu-id="8c99d-140">Valitse kopioitava Power Apps-ympäristö ja sitten **Kopioi**.</span><span class="sxs-lookup"><span data-stu-id="8c99d-140">Select the Power Apps environment to copy, and then select **Copy**.</span></span>

7. <span data-ttu-id="8c99d-141">Kun kopiointiprosessi on valmis, kirjaudu kohde-esiintymään ja ota Dataverse -integrointi käyttöön.</span><span class="sxs-lookup"><span data-stu-id="8c99d-141">When the copy process is completed, sign in to the target instance, and enable Dataverse integration.</span></span> <span data-ttu-id="8c99d-142">Lisätietoja ja -ohjeita on kohdassa [Dataverse -integroinnin määrittäminen](https://docs.microsoft.com/dynamics365/talent/hr-common-data-service-integration).</span><span class="sxs-lookup"><span data-stu-id="8c99d-142">For more information and instructions, see [Configure Dataverse integration](https://docs.microsoft.com/dynamics365/talent/hr-common-data-service-integration).</span></span>

## <a name="data-elements-and-statuses"></a><span data-ttu-id="8c99d-143">Tietoelementit ja tilat</span><span class="sxs-lookup"><span data-stu-id="8c99d-143">Data elements and statuses</span></span>

<span data-ttu-id="8c99d-144">Seuraavia tietoelementtejä ei kopioida, kun kopioit Human Resources -esiintymän:</span><span class="sxs-lookup"><span data-stu-id="8c99d-144">The following data elements aren't copied when you copy a Human Resources instance:</span></span>

- <span data-ttu-id="8c99d-145">Sähköpostiosoitteet **LogisticsElectronicAddress**-taulukossa</span><span class="sxs-lookup"><span data-stu-id="8c99d-145">Email addresses in the **LogisticsElectronicAddress** table</span></span>

- <span data-ttu-id="8c99d-146">Erätyöhistoria taulukoissa **BatchJobHistory**, **BatchHistory** ja **BatchConstraintHistory**</span><span class="sxs-lookup"><span data-stu-id="8c99d-146">The batch job history in the **BatchJobHistory**, **BatchHistory**, and **BatchConstraintHistory** tables</span></span>

- <span data-ttu-id="8c99d-147">Simple Mail Transfer Protocol (SMTP) -salasanaa **SysEmailSMTPPassword**-taulukossa</span><span class="sxs-lookup"><span data-stu-id="8c99d-147">The Simple Mail Transfer Protocol (SMTP) password in the **SysEmailSMTPPassword** table</span></span>

- <span data-ttu-id="8c99d-148">SMTP-välityspalvelin **SysEmailParameters**-taulukossa</span><span class="sxs-lookup"><span data-stu-id="8c99d-148">The SMTP Relay server in the **SysEmailParameters** table</span></span>

- <span data-ttu-id="8c99d-149">Tulostuksenhallinta-asetukset taulukoissa **PrintMgmtSettings** ja **PrintMgmtDocInstance**</span><span class="sxs-lookup"><span data-stu-id="8c99d-149">Print Management settings in the **PrintMgmtSettings** and **PrintMgmtDocInstance** tables</span></span>

- <span data-ttu-id="8c99d-150">Ympäristökohtaiset tietueet taulukoissa **SysServerConfig**, **SysServerSessions**, **SysCorpNetPrinters**, **SysClientSessions**, **BatchServerConfig** ja **BatchServerGroup**</span><span class="sxs-lookup"><span data-stu-id="8c99d-150">Environment-specific records in the **SysServerConfig**, **SysServerSessions**, **SysCorpNetPrinters**, **SysClientSessions**, **BatchServerConfig**, and **BatchServerGroup** tables</span></span>

- <span data-ttu-id="8c99d-151">Asiakirjojen liitteet DocuValue-taulukossa.</span><span class="sxs-lookup"><span data-stu-id="8c99d-151">Document attachments in the DocuValue table.</span></span> <span data-ttu-id="8c99d-152">Nämä liitteet sisältävät kaikki lähdeympäristössä korvatut Microsoft Office -mallit</span><span class="sxs-lookup"><span data-stu-id="8c99d-152">These attachments include any Microsoft Office templates that were overwritten in the source environment</span></span>

- <span data-ttu-id="8c99d-153">Yhteysmerkkijono taulukossa **PersonnelIntegrationConfiguration**</span><span class="sxs-lookup"><span data-stu-id="8c99d-153">The connection string in the **PersonnelIntegrationConfiguration** table</span></span>

<span data-ttu-id="8c99d-154">Osaa näistä elementeistä ei kopioida, koska ne ovat ympäristökohtaisia.</span><span class="sxs-lookup"><span data-stu-id="8c99d-154">Some of these elements aren't copied because they're environment-specific.</span></span> <span data-ttu-id="8c99d-155">Esimerkkejä tästä ovat tietueet **BatchServerConfig** ja **SysCorpNetPrinters**.</span><span class="sxs-lookup"><span data-stu-id="8c99d-155">Examples include **BatchServerConfig** and **SysCorpNetPrinters** records.</span></span> <span data-ttu-id="8c99d-156">Toisia elementtejä ei kopioida palvelupyyntöjen suuren määrän vuoksi.</span><span class="sxs-lookup"><span data-stu-id="8c99d-156">Other elements aren't copied because of the volume of support tickets.</span></span> <span data-ttu-id="8c99d-157">Esimerkki:</span><span class="sxs-lookup"><span data-stu-id="8c99d-157">For example:</span></span>

- <span data-ttu-id="8c99d-158">Sähköpostien kaksoiskappaleita saatetaan lähettää, koska SMTP on edelleen käytössä käyttäjän hyväksyntätestauksen ympäristössä (eristys).</span><span class="sxs-lookup"><span data-stu-id="8c99d-158">Duplicate emails might be sent because SMTP is still enabled in the user acceptance testing (sandbox) environment.</span></span>

- <span data-ttu-id="8c99d-159">Virheellisiä integrointisanomia saatetaan lähettää, koska erätyöt ovat yhä käytössä.</span><span class="sxs-lookup"><span data-stu-id="8c99d-159">Invalid integration messages might be sent because batch jobs are still enabled.</span></span>

- <span data-ttu-id="8c99d-160">Käyttäjät saattavat olla käytössä, ennen kuin järjestelmänvalvojat voivat suorittaa päivityksen jälkeiset puhdistustoiminnot.</span><span class="sxs-lookup"><span data-stu-id="8c99d-160">Users might be enabled before admins can perform post-refresh cleanup actions.</span></span>

<span data-ttu-id="8c99d-161">Myös seuraavat tilat muuttuvat, kun esiintymä kopioidaan:</span><span class="sxs-lookup"><span data-stu-id="8c99d-161">Also, the following statuses change when you copy an instance:</span></span>

- <span data-ttu-id="8c99d-162">Kaikkien käyttäjien tilaksi järjestelmänvalvojaa lukuun ottamatta asetetaan **Pois käytöstä**.</span><span class="sxs-lookup"><span data-stu-id="8c99d-162">All users except Admin are set to **Disabled**.</span></span>

- <span data-ttu-id="8c99d-163">Kaikki erätyöt joitakin järjestelmätöitä lukuun ottamatta asetetaan tilaan **Pidätä**.</span><span class="sxs-lookup"><span data-stu-id="8c99d-163">All batch jobs, except for some system jobs, are set to **Withhold**.</span></span>

## <a name="environment-admin"></a><span data-ttu-id="8c99d-164">Ympäristön järjestelmänvalvoja</span><span class="sxs-lookup"><span data-stu-id="8c99d-164">Environment admin</span></span>

<span data-ttu-id="8c99d-165">Kaikki eristetyn kohdeympäristön käyttäjät, myös järjestelmänvalvojat, korvataan lähdeympäristön käyttäjillä.</span><span class="sxs-lookup"><span data-stu-id="8c99d-165">All users in the target sandbox environment, including Administrators, are replaced by the users of the source environment.</span></span> <span data-ttu-id="8c99d-166">Varmista ennen esiintymän kopioimista, että olet lähdeympäristön järjestelmänvalvoja.</span><span class="sxs-lookup"><span data-stu-id="8c99d-166">Before you copy an instance, be sure that you're an Administrator in the source environment.</span></span> <span data-ttu-id="8c99d-167">Jos et ole, et voi kirjautua eristettyyn kohdeympäristöön, kun kopiointi on valmis.</span><span class="sxs-lookup"><span data-stu-id="8c99d-167">If you aren't, you can't sign in to the target sandbox environment after the copy has completed.</span></span>

<span data-ttu-id="8c99d-168">Kaikki muut kuin järjestelmänvalvojakäyttäjät poistetaan käytöstä eristetyssä kohdeympäristössä, jotta estetään ei-toivotut kirjautumiset siihen.</span><span class="sxs-lookup"><span data-stu-id="8c99d-168">All non-Administrator users in the target sandbox environment are disabled to prevent unwanted sign-ins in the sandbox environment.</span></span> <span data-ttu-id="8c99d-169">Järjestelmänvalvojat voivat tarvittaessa ottaa käyttäjiä uudelleen käyttöön.</span><span class="sxs-lookup"><span data-stu-id="8c99d-169">Administrators can reenable users if needed.</span></span>

## <a name="apply-custom-fields-to-dataverse"></a><span data-ttu-id="8c99d-170">Mukautettujen kenttien käyttäminen Dataversessä</span><span class="sxs-lookup"><span data-stu-id="8c99d-170">Apply custom fields to Dataverse</span></span>

<span data-ttu-id="8c99d-171">Jos kopioit esiintymään eristysympäristöön ja haluat integroida eristysympäristön Dataversen kanssa, mukautetut kentät on otettava uudelleen Dataverse-taulukoissa.</span><span class="sxs-lookup"><span data-stu-id="8c99d-171">If you copy an instance into your sandbox environment and want to integrate your sandbox environment with Dataverse, you must reapply custom fields to Dataverse tables.</span></span>

<span data-ttu-id="8c99d-172">Tee seuraavat jokaisen Dataverse-taulukoissa näkyvän mukautetun kentän kohdalla:</span><span class="sxs-lookup"><span data-stu-id="8c99d-172">For each custom field that's exposed on Dataverse tables, do the following steps:</span></span>

1. <span data-ttu-id="8c99d-173">Siirry mukautettuun kenttään ja valitse **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="8c99d-173">Go to the custom field and select **Edit**.</span></span>

2. <span data-ttu-id="8c99d-174">Poista kunkin sellaisen cdm_\*-entiteetin **Käytössä**-kentän valinta, jossa mukautettu kenttä on otettu käyttöön.</span><span class="sxs-lookup"><span data-stu-id="8c99d-174">Unselect the **Enabled** field for each cdm_\* entity that the custom field is enabled on.</span></span>

3. <span data-ttu-id="8c99d-175">Valitse **Ota muutokset käyttöön**.</span><span class="sxs-lookup"><span data-stu-id="8c99d-175">Select **Apply Changes**.</span></span>

4. <span data-ttu-id="8c99d-176">Valitse **Muokkaa** uudelleen.</span><span class="sxs-lookup"><span data-stu-id="8c99d-176">Select **Edit** again.</span></span>

5. <span data-ttu-id="8c99d-177">Valitse kunkin sellaisen cdm_\*-entiteetin **Käytössä**-kenttä, jossa mukautettu kenttä on otettu käyttöön.</span><span class="sxs-lookup"><span data-stu-id="8c99d-177">Select the **Enabled** field for each cdm_\* entity that the custom field is enabled on.</span></span>

6. <span data-ttu-id="8c99d-178">Valitse **Ota muutokset käyttöön** uudelleen.</span><span class="sxs-lookup"><span data-stu-id="8c99d-178">Select **Apply Changes** again.</span></span>

<span data-ttu-id="8c99d-179">Valinnan poistamisprosessi, muutosten käyttöönottaminen, uudelleen valitseminen ja muutosten ottaminen uudelleen käyttöön saa rakenteen päivittämään Dataversen sisällyttämään mukautetut kentät.</span><span class="sxs-lookup"><span data-stu-id="8c99d-179">The process of unselecting, applying changes, reselecting, and reapplying changes prompts the schema to update in Dataverse to include the custom fields.</span></span>

<span data-ttu-id="8c99d-180">Lisätietoja mukautetuista kentistä on kohdassa [Mukautettujen kenttien luonti ja käyttö](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/user-defined-fields).</span><span class="sxs-lookup"><span data-stu-id="8c99d-180">For more information about custom fields, see [Create and work with custom fields](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/user-defined-fields).</span></span>

## <a name="see-also"></a><span data-ttu-id="8c99d-181">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="8c99d-181">See also</span></span>

[<span data-ttu-id="8c99d-182">Valmistele Human Resources</span><span class="sxs-lookup"><span data-stu-id="8c99d-182">Provision Human Resources</span></span>](hr-admin-setup-provision.md)</br>
[<span data-ttu-id="8c99d-183">Poista esiintymä</span><span class="sxs-lookup"><span data-stu-id="8c99d-183">Remove an instance</span></span>](hr-admin-setup-remove-instance.md)</br>
[<span data-ttu-id="8c99d-184">Päivitysprosessi</span><span class="sxs-lookup"><span data-stu-id="8c99d-184">Update process</span></span>](hr-admin-setup-update-process.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]