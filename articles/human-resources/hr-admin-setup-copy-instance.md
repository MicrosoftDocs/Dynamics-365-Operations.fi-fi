---
title: Kopioi esiintymä
description: Microsoft Dynamics 365 Human Resources -tietokannan voi kopioida eristysympäristöön Microsoft Dynamics Lifecycle Servicesin (LCS) avulla.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: bb363369994d99f358be0c23cdaf1dbc80b644e5
ms.sourcegitcommit: f38302b9430f2ab3efe91d0a7beff946bc610e8f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/28/2020
ms.locfileid: "3092289"
---
# <a name="copy-an-instance"></a><span data-ttu-id="bc7e1-103">Kopioi esiintymä</span><span class="sxs-lookup"><span data-stu-id="bc7e1-103">Copy an instance</span></span>

<span data-ttu-id="bc7e1-104">Microsoft Dynamics 365 Human Resources -tietokannan voi kopioida eristysympäristöön Microsoft Dynamics Lifecycle Servicesin (LCS) avulla.</span><span class="sxs-lookup"><span data-stu-id="bc7e1-104">You can use Microsoft Dynamics Lifecycle Services (LCS) to copy a Microsoft Dynamics 365 Human Resources database to a sandbox environment.</span></span> <span data-ttu-id="bc7e1-105">Jos käytössä on toinen eristysympäristö, voit kopioida myös tietokannan siitä kohde-eristysympäristöön.</span><span class="sxs-lookup"><span data-stu-id="bc7e1-105">If you have another sandbox environment, you can also copy the database from that environment to a targeted sandbox environment.</span></span>

<span data-ttu-id="bc7e1-106">Jos haluat kopioida esiintymän, sinun on varmistettava seuraavat asiat:</span><span class="sxs-lookup"><span data-stu-id="bc7e1-106">To copy an instance, you need to ensure the following:</span></span>

- <span data-ttu-id="bc7e1-107">Korvattavan Human Resources -esiintymän on oltava eristysympäristö.</span><span class="sxs-lookup"><span data-stu-id="bc7e1-107">The Human Resources instance you want to overwrite must be a sandbox environment.</span></span>

- <span data-ttu-id="bc7e1-108">Kopioinnin lähde- ja kohdeympäristöjen on oltava samalla alueella.</span><span class="sxs-lookup"><span data-stu-id="bc7e1-108">The environments you are copying from and to must be in the same region.</span></span> <span data-ttu-id="bc7e1-109">Et voi kopioida eri alueiden välillä.</span><span class="sxs-lookup"><span data-stu-id="bc7e1-109">You can't copy across regions.</span></span>

- <span data-ttu-id="bc7e1-110">Sinun on oltava kohdeympäristön järjestelmänvalvoja, jotta voit kirjautua siihen, kun olet kopioinut esiintymän.</span><span class="sxs-lookup"><span data-stu-id="bc7e1-110">You must be an Administrator in the target environment so you can sign into it after copying the instance.</span></span>

- <span data-ttu-id="bc7e1-111">Kun kopioit Human Resourcesin tietokannan, et kopioi elementtejä (sovelluksia tai tietoja), jotka sisältyvät Microsoft PowerApps -ympäristöön.</span><span class="sxs-lookup"><span data-stu-id="bc7e1-111">When you copy the Human Resources database, you don't copy the elements (apps or data) that are contained in a Microsoft PowerApps environment.</span></span> <span data-ttu-id="bc7e1-112">Lisätietoja elementtien kopioinnista PowerApps-ympäristössä on kohdassa [Ympäristön kopioiminen](https://docs.microsoft.com/power-platform/admin/copy-environment).</span><span class="sxs-lookup"><span data-stu-id="bc7e1-112">For information about how to copy elements in a PowerApps environment, see [Copy an environment](https://docs.microsoft.com/power-platform/admin/copy-environment).</span></span> <span data-ttu-id="bc7e1-113">Korvattavan PowerApps-ympäristön on oltava eristysympäristö.</span><span class="sxs-lookup"><span data-stu-id="bc7e1-113">The PowerApps environment you want to overwrite must be a sandbox environment.</span></span> <span data-ttu-id="bc7e1-114">Sinun on oltava yleinen vuokraajan järjestelmänvalvoja, jotta voit muuttaa PowerApps-tuotantoympäristön eristysympäristöksi.</span><span class="sxs-lookup"><span data-stu-id="bc7e1-114">You must be a global tenant admin to change a PowerApps production environment to a sandbox environment.</span></span> <span data-ttu-id="bc7e1-115">Lisä tietoja PowerApps-ympäristön muuttamisesta on kohdassa [Esiintymän vaihtaminen](https://docs.microsoft.com/dynamics365/admin/switch-instance).</span><span class="sxs-lookup"><span data-stu-id="bc7e1-115">For more information about changing a PowerApps environment, see [Switch an instance](https://docs.microsoft.com/dynamics365/admin/switch-instance).</span></span>

## <a name="effects-of-copying-a-human-resources-database"></a><span data-ttu-id="bc7e1-116">Human Resources -tietokannan kopioinnin vaikutukset</span><span class="sxs-lookup"><span data-stu-id="bc7e1-116">Effects of copying a Human Resources database</span></span>

<span data-ttu-id="bc7e1-117">Human Resources -tietokannan kopioinnin yhteydessä tapahtuu seuraavaa:</span><span class="sxs-lookup"><span data-stu-id="bc7e1-117">The following events occur when you copy a Human Resources database:</span></span>

- <span data-ttu-id="bc7e1-118">Kopiointiprosessi poistaa aiemmin luodun tietokannan kohdeympäristöstä.</span><span class="sxs-lookup"><span data-stu-id="bc7e1-118">The copy process erases the existing database in the target environment.</span></span> <span data-ttu-id="bc7e1-119">Kun kopiointiprosessi on suoritettu, et voi palauttaa aiemmin luotua tietokantaa.</span><span class="sxs-lookup"><span data-stu-id="bc7e1-119">After the copy process is completed, you can't recover the existing database.</span></span>

- <span data-ttu-id="bc7e1-120">Kohdeympäristö ei ole käytettävissä, ennen kuin kopiointiprosessi on valmis.</span><span class="sxs-lookup"><span data-stu-id="bc7e1-120">The target environment will be unavailable until the copy process is completed.</span></span>

- <span data-ttu-id="bc7e1-121">Microsoft Azure Blob -tallennustilassa olevia asiakirjoja ei kopioida ympäristöstä toiseen.</span><span class="sxs-lookup"><span data-stu-id="bc7e1-121">Documents in Microsoft Azure Blob storage aren't copied from one environment to another.</span></span> <span data-ttu-id="bc7e1-122">Siksi liitettyjä asiakirjoja ja malleja ei kopioida, ja ne jäävät lähdeympäristöön.</span><span class="sxs-lookup"><span data-stu-id="bc7e1-122">Therefore, any documents and templates that are attached won't be copied and will remain in the source environment.</span></span>

- <span data-ttu-id="bc7e1-123">Mitkään käyttäjät, paitsi järjestelmänvalvojakäyttäjä ja muut sisäisen palvelun käyttäjätilit eivät ole käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="bc7e1-123">All users except the Admin user and other internal service user accounts will be unavailable.</span></span> <span data-ttu-id="bc7e1-124">Siten järjestelmänvalvojakäyttäjä voi poistaa tietoja tai piilottaa niitä näkyvistä, ennen kuin muut käyttäjät pääsevät takaisin järjestelmään.</span><span class="sxs-lookup"><span data-stu-id="bc7e1-124">Therefore, the Admin user can delete or obfuscate data before other users are allowed back into the system.</span></span>

- <span data-ttu-id="bc7e1-125">Järjestelmänvalvojakäyttäjän on suoritettava vaadittavat muutokset määrityksiin, kuten yhdistettävä integroinnin päätepisteet uudelleen tiettyihin palveluihin tai URL-osoitteisiin.</span><span class="sxs-lookup"><span data-stu-id="bc7e1-125">The Admin user must make required configuration changes, such as reconnecting integration endpoints to specific services or URLs.</span></span>

## <a name="copy-the-human-resources-database"></a><span data-ttu-id="bc7e1-126">Human Resources -tietokannan kopiointi</span><span class="sxs-lookup"><span data-stu-id="bc7e1-126">Copy the Human Resources database</span></span>

<span data-ttu-id="bc7e1-127">Jos haluat suorittaa tämän tehtävän, kopioi ensin esiintymä ja kirjaudu sitten Microsoft Power Platform -hallintakeskukseen ja kopioi PowerApps-ympäristösi.</span><span class="sxs-lookup"><span data-stu-id="bc7e1-127">To complete this task, you first copy an instance, and then sign in to the Microsoft Power Platform Admin Center to copy your PowerApps environment.</span></span>

> [!WARNING]
> <span data-ttu-id="bc7e1-128">Kun kopioit esiintymän, tietokanta poistetaan kohde-esiintymästä.</span><span class="sxs-lookup"><span data-stu-id="bc7e1-128">When you copy an instance, the database is erased in the target instance.</span></span> <span data-ttu-id="bc7e1-129">Kohde-esiintymä ei ole käytettävissä tämän prosessin aikana.</span><span class="sxs-lookup"><span data-stu-id="bc7e1-129">The target instance is unavailable during this process.</span></span>

1. <span data-ttu-id="bc7e1-130">Kirjaudu LCS:ään ja valitse LCS-projekti, joka sisältää kopioitavan esiintymän.</span><span class="sxs-lookup"><span data-stu-id="bc7e1-130">Sign in to LCS, and select the LCS project that contains the instance that you want to copy.</span></span>

2. <span data-ttu-id="bc7e1-131">Valitse LCS-projektin **Human Resources -sovelluksen hallinta** -ruutu.</span><span class="sxs-lookup"><span data-stu-id="bc7e1-131">In your LCS project, select the **Human Resources App Management** tile.</span></span>

3. <span data-ttu-id="bc7e1-132">Valitse kopioitava esiintymä ja sitten **Kopioi**.</span><span class="sxs-lookup"><span data-stu-id="bc7e1-132">Select the instance to copy, and then select **Copy**.</span></span>

4. <span data-ttu-id="bc7e1-133">Valitse korvattava esiintymä **Kopioi esiintymä** -tehtäväruudusta ja valitse sitten **Kopioi**.</span><span class="sxs-lookup"><span data-stu-id="bc7e1-133">In the **Copy an instance** task pane, select the instance to overwrite, and then select **Copy**.</span></span> <span data-ttu-id="bc7e1-134">Odota, että **Kopioi tila** -kentän arvoksi päivittyy **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="bc7e1-134">Wait for the value of the **Copy status** field to be updated to **Completed**.</span></span>

   ![[<span data-ttu-id="bc7e1-135">Valitse esiintymä, joka korvataan</span><span class="sxs-lookup"><span data-stu-id="bc7e1-135">Select instance to overwrite</span></span>](./media/copy-instance-select-target-instance.png)](./media/copy-instance-select-target-instance.png)

5. <span data-ttu-id="bc7e1-136">Valitse **Power Platform** ja kirjaudu Microsoft Power Platform -hallintakeskukseen.</span><span class="sxs-lookup"><span data-stu-id="bc7e1-136">Select **Power Platform**, and sign in to the Microsoft Power Platform Admin Center.</span></span>

   ![[<span data-ttu-id="bc7e1-137">Valitse Power Platform</span><span class="sxs-lookup"><span data-stu-id="bc7e1-137">Select Power Platform</span></span>](./media/copy-instance-select-power-platform.png)](./media/copy-instance-select-power-platform.png)

6. <span data-ttu-id="bc7e1-138">Valitse kopioitava PowerApps-ympäristö ja sitten **Kopioi**.</span><span class="sxs-lookup"><span data-stu-id="bc7e1-138">Select the PowerApps environment to copy, and then select **Copy**.</span></span>

7. <span data-ttu-id="bc7e1-139">Kun kopiointiprosessi on valmis, kirjaudu kohde-esiintymään ja ota Common Data Service -integrointi käyttöön.</span><span class="sxs-lookup"><span data-stu-id="bc7e1-139">When the copy process is completed, sign in to the target instance, and enable Common Data Service integration.</span></span> <span data-ttu-id="bc7e1-140">Lisätietoja ja -ohjeita on kohdassa [Common Data Service -integroinnin määrittäminen](https://docs.microsoft.com/dynamics365/talent/hr-common-data-service-integration).</span><span class="sxs-lookup"><span data-stu-id="bc7e1-140">For more information and instructions, see [Configure Common Data Service integration](https://docs.microsoft.com/dynamics365/talent/hr-common-data-service-integration).</span></span>

## <a name="data-elements-and-statuses"></a><span data-ttu-id="bc7e1-141">Tietoelementit ja tilat</span><span class="sxs-lookup"><span data-stu-id="bc7e1-141">Data elements and statuses</span></span>

<span data-ttu-id="bc7e1-142">Seuraavia tietoelementtejä ei kopioida, kun kopioit Human Resources -esiintymän:</span><span class="sxs-lookup"><span data-stu-id="bc7e1-142">The following data elements aren't copied when you copy a Human Resources instance:</span></span>

- <span data-ttu-id="bc7e1-143">Sähköpostiosoitteet **LogisticsElectronicAddress**-taulukossa</span><span class="sxs-lookup"><span data-stu-id="bc7e1-143">Email addresses in the **LogisticsElectronicAddress** table</span></span>

- <span data-ttu-id="bc7e1-144">Erätyöhistoria taulukoissa **BatchJobHistory**, **BatchHistory** ja **BatchConstraintHistory**</span><span class="sxs-lookup"><span data-stu-id="bc7e1-144">The batch job history in the **BatchJobHistory**, **BatchHistory**, and **BatchConstraintHistory** tables</span></span>

- <span data-ttu-id="bc7e1-145">Simple Mail Transfer Protocol (SMTP) -salasanaa **SysEmailSMTPPassword**-taulukossa</span><span class="sxs-lookup"><span data-stu-id="bc7e1-145">The Simple Mail Transfer Protocol (SMTP) password in the **SysEmailSMTPPassword** table</span></span>

- <span data-ttu-id="bc7e1-146">SMTP-välityspalvelin **SysEmailParameters**-taulukossa</span><span class="sxs-lookup"><span data-stu-id="bc7e1-146">The SMTP Relay server in the **SysEmailParameters** table</span></span>

- <span data-ttu-id="bc7e1-147">Tulostuksenhallinta-asetukset taulukoissa **PrintMgmtSettings** ja **PrintMgmtDocInstance**</span><span class="sxs-lookup"><span data-stu-id="bc7e1-147">Print Management settings in the **PrintMgmtSettings** and **PrintMgmtDocInstance** tables</span></span>

- <span data-ttu-id="bc7e1-148">Ympäristökohtaiset tietueet taulukoissa **SysServerConfig**, **SysServerSessions**, **SysCorpNetPrinters**, **SysClientSessions**, **BatchServerConfig** ja **BatchServerGroup**</span><span class="sxs-lookup"><span data-stu-id="bc7e1-148">Environment-specific records in the **SysServerConfig**, **SysServerSessions**, **SysCorpNetPrinters**, **SysClientSessions**, **BatchServerConfig**, and **BatchServerGroup** tables</span></span>

- <span data-ttu-id="bc7e1-149">Asiakirjojen liitteet DocuValue-taulukossa.</span><span class="sxs-lookup"><span data-stu-id="bc7e1-149">Document attachments in the DocuValue table.</span></span> <span data-ttu-id="bc7e1-150">Nämä liitteet sisältävät kaikki lähdeympäristössä korvatut Microsoft Office -mallit</span><span class="sxs-lookup"><span data-stu-id="bc7e1-150">These attachments include any Microsoft Office templates that were overwritten in the source environment</span></span>

- <span data-ttu-id="bc7e1-151">Yhteysmerkkijono taulukossa **PersonnelIntegrationConfiguration**</span><span class="sxs-lookup"><span data-stu-id="bc7e1-151">The connection string in the **PersonnelIntegrationConfiguration** table</span></span>

<span data-ttu-id="bc7e1-152">Osaa näistä elementeistä ei kopioida, koska ne ovat ympäristökohtaisia.</span><span class="sxs-lookup"><span data-stu-id="bc7e1-152">Some of these elements aren't copied because they are environment-specific.</span></span> <span data-ttu-id="bc7e1-153">Esimerkkejä tästä ovat tietueet **BatchServerConfig** ja **SysCorpNetPrinters**.</span><span class="sxs-lookup"><span data-stu-id="bc7e1-153">Examples include **BatchServerConfig** and **SysCorpNetPrinters** records.</span></span> <span data-ttu-id="bc7e1-154">Toisia elementtejä ei kopioida palvelupyyntöjen suuren määrän vuoksi.</span><span class="sxs-lookup"><span data-stu-id="bc7e1-154">Other elements aren't copied because of the volume of support tickets.</span></span> <span data-ttu-id="bc7e1-155">Esimerkiksi sähköpostien kaksoiskappaleita saatetaan lähettää, koska SMTP on edelleen käytössä käyttäjän hyväksyntätestauksen ympäristössä (eristys), virheellisiä integrointisanomia saatetaan lähettää, koska erätyöt ovat yhä käytössä ja käyttäjät saattavat olla käytössä, ennen kuin järjestelmänvalvojat voivat suorittaa päivityksen jälkeiset puhdistustoiminnot.</span><span class="sxs-lookup"><span data-stu-id="bc7e1-155">For example, duplicate emails might be sent because SMTP is still enabled in the user acceptance testing (sandbox) environment, invalid integration messages might be sent because batch jobs are still enabled, and users might be enabled before admins can perform post-refresh cleanup actions.</span></span>

<span data-ttu-id="bc7e1-156">Lisäksi seuraavat tilat muuttuvat, kun esiintymä kopioidaan:</span><span class="sxs-lookup"><span data-stu-id="bc7e1-156">In addition, the following statuses change when you copy an instance:</span></span>

- <span data-ttu-id="bc7e1-157">Kaikkien käyttäjien tilaksi järjestelmänvalvojaa lukuun ottamatta asetetaan **Pois käytöstä**.</span><span class="sxs-lookup"><span data-stu-id="bc7e1-157">All users except Admin are set to **Disabled**.</span></span>

- <span data-ttu-id="bc7e1-158">Kaikki erätyöt joitakin järjestelmätöitä lukuun ottamatta asetetaan tilaan **Pidätä**.</span><span class="sxs-lookup"><span data-stu-id="bc7e1-158">All batch jobs, except for some system jobs, are set to **Withhold**.</span></span>

## <a name="environment-admin"></a><span data-ttu-id="bc7e1-159">Ympäristön järjestelmänvalvoja</span><span class="sxs-lookup"><span data-stu-id="bc7e1-159">Environment admin</span></span>

<span data-ttu-id="bc7e1-160">Kaikki eristetyn kohdeympäristön käyttäjät, myös järjestelmänvalvojat, korvataan lähdeympäristön käyttäjillä.</span><span class="sxs-lookup"><span data-stu-id="bc7e1-160">All users in the target sandbox environment, including Administrators, are replaced by the users of the source environment.</span></span> <span data-ttu-id="bc7e1-161">Varmista ennen esiintymän kopioimista, että olet kohdeympäristön järjestelmänvalvoja.</span><span class="sxs-lookup"><span data-stu-id="bc7e1-161">Before you copy an instance, be sure that you're an Administrator in the target environment.</span></span> <span data-ttu-id="bc7e1-162">Jos et ole, et voi kirjautua eristettyyn kohdeympäristöön, kun kopiointi on valmis.</span><span class="sxs-lookup"><span data-stu-id="bc7e1-162">If you aren't, you won't be able to sign in to the target sandbox environment after the copy has completed.</span></span>

<span data-ttu-id="bc7e1-163">Kaikki muut kuin järjestelmänvalvojakäyttäjät poistetaan käytöstä eristetyssä kohdeympäristössä, jotta estetään ei-toivotut kirjautumiset siihen.</span><span class="sxs-lookup"><span data-stu-id="bc7e1-163">All non-Administrator users in the target sandbox environment are disabled to prevent unwanted sign-ins in the sandbox environment.</span></span> <span data-ttu-id="bc7e1-164">Järjestelmänvalvojat voivat tarvittaessa ottaa käyttäjiä uudelleen käyttöön.</span><span class="sxs-lookup"><span data-stu-id="bc7e1-164">Administrators can reenable users if needed.</span></span>
