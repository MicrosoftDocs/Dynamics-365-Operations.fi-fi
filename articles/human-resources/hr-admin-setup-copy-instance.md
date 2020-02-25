---
title: Kopioi esiintymä
description: ''
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
ms.openlocfilehash: 0bbe325edb65cad0c1912e0a6ade559e5675dc58
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008836"
---
# <a name="copy-an-instance"></a><span data-ttu-id="5dde9-102">Kopioi esiintymä</span><span class="sxs-lookup"><span data-stu-id="5dde9-102">Copy an instance</span></span>

<span data-ttu-id="5dde9-103">Microsoft Dynamics 365 Human Resources -tietokannan voi kopioida eristysympäristöön Microsoft Dynamics Lifecycle Servicesin (LCS) avulla.</span><span class="sxs-lookup"><span data-stu-id="5dde9-103">You can use Microsoft Dynamics Lifecycle Services (LCS) to copy a Microsoft Dynamics 365 Human Resources database to a sandbox environment.</span></span> <span data-ttu-id="5dde9-104">Jos käytössä on toinen eristysympäristö, voit kopioida myös tietokannan siitä kohde-eristysympäristöön.</span><span class="sxs-lookup"><span data-stu-id="5dde9-104">If you have another sandbox environment, you can also copy the database from that environment to a targeted sandbox environment.</span></span>

<span data-ttu-id="5dde9-105">Jos haluat kopioida esiintymän, sinun on varmistettava seuraavat asiat:</span><span class="sxs-lookup"><span data-stu-id="5dde9-105">To copy an instance, you need to ensure the following:</span></span>

- <span data-ttu-id="5dde9-106">Korvattavan Human Resources -esiintymän on oltava eristysympäristö.</span><span class="sxs-lookup"><span data-stu-id="5dde9-106">The Human Resources instance you want to overwrite must be a sandbox environment.</span></span>

- <span data-ttu-id="5dde9-107">Kopioinnin lähde- ja kohdeympäristöjen on oltava samalla alueella.</span><span class="sxs-lookup"><span data-stu-id="5dde9-107">The environments you are copying from and to must be in the same region.</span></span> <span data-ttu-id="5dde9-108">Et voi kopioida eri alueiden välillä.</span><span class="sxs-lookup"><span data-stu-id="5dde9-108">You can't copy across regions.</span></span>

- <span data-ttu-id="5dde9-109">Sinun on oltava kohdeympäristön järjestelmänvalvoja, jotta voit kirjautua siihen, kun olet kopioinut esiintymän.</span><span class="sxs-lookup"><span data-stu-id="5dde9-109">You must be an Administrator in the target environment so you can sign into it after copying the instance.</span></span>

- <span data-ttu-id="5dde9-110">Kun kopioit Human Resourcesin tietokannan, et kopioi elementtejä (sovelluksia tai tietoja), jotka sisältyvät Microsoft PowerApps -ympäristöön.</span><span class="sxs-lookup"><span data-stu-id="5dde9-110">When you copy the Human Resources database, you don't copy the elements (apps or data) that are contained in a Microsoft PowerApps environment.</span></span> <span data-ttu-id="5dde9-111">Lisätietoja elementtien kopioinnista PowerApps-ympäristössä on kohdassa [Ympäristön kopioiminen](https://docs.microsoft.com/power-platform/admin/copy-environment).</span><span class="sxs-lookup"><span data-stu-id="5dde9-111">For information about how to copy elements in a PowerApps environment, see [Copy an environment](https://docs.microsoft.com/power-platform/admin/copy-environment).</span></span> <span data-ttu-id="5dde9-112">Korvattavan PowerApps-ympäristön on oltava eristysympäristö.</span><span class="sxs-lookup"><span data-stu-id="5dde9-112">The PowerApps environment you want to overwrite must be a sandbox environment.</span></span> <span data-ttu-id="5dde9-113">Sinun on oltava yleinen vuokraajan järjestelmänvalvoja, jotta voit muuttaa PowerApps-tuotantoympäristön eristysympäristöksi.</span><span class="sxs-lookup"><span data-stu-id="5dde9-113">You must be a global tenant admin to change a PowerApps production environment to a sandbox environment.</span></span> <span data-ttu-id="5dde9-114">Lisä tietoja PowerApps-ympäristön muuttamisesta on kohdassa [Esiintymän vaihtaminen](https://docs.microsoft.com/dynamics365/admin/switch-instance).</span><span class="sxs-lookup"><span data-stu-id="5dde9-114">For more information about changing a PowerApps environment, see [Switch an instance](https://docs.microsoft.com/dynamics365/admin/switch-instance).</span></span>

## <a name="effects-of-copying-a-human-resources-database"></a><span data-ttu-id="5dde9-115">Human Resources -tietokannan kopioinnin vaikutukset</span><span class="sxs-lookup"><span data-stu-id="5dde9-115">Effects of copying a Human Resources database</span></span>

<span data-ttu-id="5dde9-116">Human Resources -tietokannan kopioinnin yhteydessä tapahtuu seuraavaa:</span><span class="sxs-lookup"><span data-stu-id="5dde9-116">The following events occur when you copy a Human Resources database:</span></span>

- <span data-ttu-id="5dde9-117">Kopiointiprosessi poistaa aiemmin luodun tietokannan kohdeympäristöstä.</span><span class="sxs-lookup"><span data-stu-id="5dde9-117">The copy process erases the existing database in the target environment.</span></span> <span data-ttu-id="5dde9-118">Kun kopiointiprosessi on suoritettu, et voi palauttaa aiemmin luotua tietokantaa.</span><span class="sxs-lookup"><span data-stu-id="5dde9-118">After the copy process is completed, you can't recover the existing database.</span></span>

- <span data-ttu-id="5dde9-119">Kohdeympäristö ei ole käytettävissä, ennen kuin kopiointiprosessi on valmis.</span><span class="sxs-lookup"><span data-stu-id="5dde9-119">The target environment will be unavailable until the copy process is completed.</span></span>

- <span data-ttu-id="5dde9-120">Microsoft Azure Blob -tallennustilassa olevia asiakirjoja ei kopioida ympäristöstä toiseen.</span><span class="sxs-lookup"><span data-stu-id="5dde9-120">Documents in Microsoft Azure Blob storage aren't copied from one environment to another.</span></span> <span data-ttu-id="5dde9-121">Siksi liitettyjä asiakirjoja ja malleja ei kopioida, ja ne jäävät lähdeympäristöön.</span><span class="sxs-lookup"><span data-stu-id="5dde9-121">Therefore, any documents and templates that are attached won't be copied and will remain in the source environment.</span></span>

- <span data-ttu-id="5dde9-122">Mitkään käyttäjät, paitsi järjestelmänvalvojakäyttäjä ja muut sisäisen palvelun käyttäjätilit eivät ole käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="5dde9-122">All users except the Admin user and other internal service user accounts will be unavailable.</span></span> <span data-ttu-id="5dde9-123">Siten järjestelmänvalvojakäyttäjä voi poistaa tietoja tai piilottaa niitä näkyvistä, ennen kuin muut käyttäjät pääsevät takaisin järjestelmään.</span><span class="sxs-lookup"><span data-stu-id="5dde9-123">Therefore, the Admin user can delete or obfuscate data before other users are allowed back into the system.</span></span>

- <span data-ttu-id="5dde9-124">Järjestelmänvalvojakäyttäjän on suoritettava vaadittavat muutokset määrityksiin, kuten yhdistettävä integroinnin päätepisteet uudelleen tiettyihin palveluihin tai URL-osoitteisiin.</span><span class="sxs-lookup"><span data-stu-id="5dde9-124">The Admin user must make required configuration changes, such as reconnecting integration endpoints to specific services or URLs.</span></span>

## <a name="copy-the-human-resources-database"></a><span data-ttu-id="5dde9-125">Human Resources -tietokannan kopiointi</span><span class="sxs-lookup"><span data-stu-id="5dde9-125">Copy the Human Resources database</span></span>

<span data-ttu-id="5dde9-126">Jos haluat suorittaa tämän tehtävän, kopioi ensin esiintymä ja kirjaudu sitten Microsoft Power Platform -hallintakeskukseen ja kopioi PowerApps-ympäristösi.</span><span class="sxs-lookup"><span data-stu-id="5dde9-126">To complete this task, you first copy an instance, and then sign in to the Microsoft Power Platform Admin Center to copy your PowerApps environment.</span></span>

> [!WARNING]
> <span data-ttu-id="5dde9-127">Kun kopioit esiintymän, tietokanta poistetaan kohde-esiintymästä.</span><span class="sxs-lookup"><span data-stu-id="5dde9-127">When you copy an instance, the database is erased in the target instance.</span></span> <span data-ttu-id="5dde9-128">Kohde-esiintymä ei ole käytettävissä tämän prosessin aikana.</span><span class="sxs-lookup"><span data-stu-id="5dde9-128">The target instance is unavailable during this process.</span></span>

1. <span data-ttu-id="5dde9-129">Kirjaudu LCS:ään ja valitse LCS-projekti, joka sisältää kopioitavan esiintymän.</span><span class="sxs-lookup"><span data-stu-id="5dde9-129">Sign in to LCS, and select the LCS project that contains the instance that you want to copy.</span></span>

2. <span data-ttu-id="5dde9-130">Valitse LCS-projektin **Human Resources -sovelluksen hallinta** -ruutu.</span><span class="sxs-lookup"><span data-stu-id="5dde9-130">In your LCS project, select the **Human Resources App Management** tile.</span></span>

3. <span data-ttu-id="5dde9-131">Valitse kopioitava esiintymä ja sitten **Kopioi**.</span><span class="sxs-lookup"><span data-stu-id="5dde9-131">Select the instance to copy, and then select **Copy**.</span></span>

4. <span data-ttu-id="5dde9-132">Valitse korvattava esiintymä **Kopioi esiintymä** -tehtäväruudusta ja valitse sitten **Kopioi**.</span><span class="sxs-lookup"><span data-stu-id="5dde9-132">In the **Copy an instance** task pane, select the instance to overwrite, and then select **Copy**.</span></span> <span data-ttu-id="5dde9-133">Odota, että **Kopioi tila** -kentän arvoksi päivittyy **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="5dde9-133">Wait for the value of the **Copy status** field to be updated to **Completed**.</span></span>

   ![[<span data-ttu-id="5dde9-134">Valitse korvattava esiintymä</span><span class="sxs-lookup"><span data-stu-id="5dde9-134">Select instance to overwrite</span></span>](./media/copy-instance-select-target-instance.png)](./media/copy-instance-select-target-instance.png)

5. <span data-ttu-id="5dde9-135">Valitse **Power Platform** ja kirjaudu Microsoft Power Platform -hallintakeskukseen.</span><span class="sxs-lookup"><span data-stu-id="5dde9-135">Select **Power Platform**, and sign in to the Microsoft Power Platform Admin Center.</span></span>

   ![[<span data-ttu-id="5dde9-136">Valitse Power Platform</span><span class="sxs-lookup"><span data-stu-id="5dde9-136">Select Power Platform</span></span>](./media/copy-instance-select-power-platform.png)](./media/copy-instance-select-power-platform.png)

6. <span data-ttu-id="5dde9-137">Valitse kopioitava PowerApps-ympäristö ja sitten **Kopioi**.</span><span class="sxs-lookup"><span data-stu-id="5dde9-137">Select the PowerApps environment to copy, and then select **Copy**.</span></span>

7. <span data-ttu-id="5dde9-138">Kun kopiointiprosessi on valmis, kirjaudu kohde-esiintymään ja ota Common Data Service -integrointi käyttöön.</span><span class="sxs-lookup"><span data-stu-id="5dde9-138">When the copy process is completed, sign in to the target instance, and enable Common Data Service integration.</span></span> <span data-ttu-id="5dde9-139">Lisätietoja ja -ohjeita on kohdassa [Common Data Service -integroinnin määrittäminen](https://docs.microsoft.com/dynamics365/talent/hr-common-data-service-integration).</span><span class="sxs-lookup"><span data-stu-id="5dde9-139">For more information and instructions, see [Configure Common Data Service integration](https://docs.microsoft.com/dynamics365/talent/hr-common-data-service-integration).</span></span>

## <a name="data-elements-and-statuses"></a><span data-ttu-id="5dde9-140">Tietoelementit ja tilat</span><span class="sxs-lookup"><span data-stu-id="5dde9-140">Data elements and statuses</span></span>

<span data-ttu-id="5dde9-141">Seuraavia tietoelementtejä ei kopioida, kun kopioit Human Resources -esiintymän:</span><span class="sxs-lookup"><span data-stu-id="5dde9-141">The following data elements aren't copied when you copy a Human Resources instance:</span></span>

- <span data-ttu-id="5dde9-142">Sähköpostiosoitteet **LogisticsElectronicAddress**-taulukossa</span><span class="sxs-lookup"><span data-stu-id="5dde9-142">Email addresses in the **LogisticsElectronicAddress** table</span></span>

- <span data-ttu-id="5dde9-143">Erätyöhistoria taulukoissa **BatchJobHistory**, **BatchHistory** ja **BatchConstraintHistory**</span><span class="sxs-lookup"><span data-stu-id="5dde9-143">The batch job history in the **BatchJobHistory**, **BatchHistory**, and **BatchConstraintHistory** tables</span></span>

- <span data-ttu-id="5dde9-144">Simple Mail Transfer Protocol (SMTP) -salasanaa **SysEmailSMTPPassword**-taulukossa</span><span class="sxs-lookup"><span data-stu-id="5dde9-144">The Simple Mail Transfer Protocol (SMTP) password in the **SysEmailSMTPPassword** table</span></span>

- <span data-ttu-id="5dde9-145">SMTP-välityspalvelin **SysEmailParameters**-taulukossa</span><span class="sxs-lookup"><span data-stu-id="5dde9-145">The SMTP Relay server in the **SysEmailParameters** table</span></span>

- <span data-ttu-id="5dde9-146">Tulostuksenhallinta-asetukset taulukoissa **PrintMgmtSettings** ja **PrintMgmtDocInstance**</span><span class="sxs-lookup"><span data-stu-id="5dde9-146">Print Management settings in the **PrintMgmtSettings** and **PrintMgmtDocInstance** tables</span></span>

- <span data-ttu-id="5dde9-147">Ympäristökohtaiset tietueet taulukoissa **SysServerConfig**, **SysServerSessions**, **SysCorpNetPrinters**, **SysClientSessions**, **BatchServerConfig** ja **BatchServerGroup**</span><span class="sxs-lookup"><span data-stu-id="5dde9-147">Environment-specific records in the **SysServerConfig**, **SysServerSessions**, **SysCorpNetPrinters**, **SysClientSessions**, **BatchServerConfig**, and **BatchServerGroup** tables</span></span>

- <span data-ttu-id="5dde9-148">Asiakirjojen liitteet DocuValue-taulukossa.</span><span class="sxs-lookup"><span data-stu-id="5dde9-148">Document attachments in the DocuValue table.</span></span> <span data-ttu-id="5dde9-149">Nämä liitteet sisältävät kaikki lähdeympäristössä korvatut Microsoft Office -mallit</span><span class="sxs-lookup"><span data-stu-id="5dde9-149">These attachments include any Microsoft Office templates that were overwritten in the source environment</span></span>

- <span data-ttu-id="5dde9-150">Yhteysmerkkijono taulukossa **PersonnelIntegrationConfiguration**</span><span class="sxs-lookup"><span data-stu-id="5dde9-150">The connection string in the **PersonnelIntegrationConfiguration** table</span></span>

<span data-ttu-id="5dde9-151">Osaa näistä elementeistä ei kopioida, koska ne ovat ympäristökohtaisia.</span><span class="sxs-lookup"><span data-stu-id="5dde9-151">Some of these elements aren't copied because they are environment-specific.</span></span> <span data-ttu-id="5dde9-152">Esimerkkejä tästä ovat tietueet **BatchServerConfig** ja **SysCorpNetPrinters**.</span><span class="sxs-lookup"><span data-stu-id="5dde9-152">Examples include **BatchServerConfig** and **SysCorpNetPrinters** records.</span></span> <span data-ttu-id="5dde9-153">Toisia elementtejä ei kopioida palvelupyyntöjen suuren määrän vuoksi.</span><span class="sxs-lookup"><span data-stu-id="5dde9-153">Other elements aren't copied because of the volume of support tickets.</span></span> <span data-ttu-id="5dde9-154">Esimerkiksi sähköpostien kaksoiskappaleita saatetaan lähettää, koska SMTP on edelleen käytössä käyttäjän hyväksyntätestauksen ympäristössä (eristys), virheellisiä integrointisanomia saatetaan lähettää, koska erätyöt ovat yhä käytössä ja käyttäjät saattavat olla käytössä, ennen kuin järjestelmänvalvojat voivat suorittaa päivityksen jälkeiset puhdistustoiminnot.</span><span class="sxs-lookup"><span data-stu-id="5dde9-154">For example, duplicate emails might be sent because SMTP is still enabled in the user acceptance testing (sandbox) environment, invalid integration messages might be sent because batch jobs are still enabled, and users might be enabled before admins can perform post-refresh cleanup actions.</span></span>

<span data-ttu-id="5dde9-155">Lisäksi seuraavat tilat muuttuvat, kun esiintymä kopioidaan:</span><span class="sxs-lookup"><span data-stu-id="5dde9-155">In addition, the following statuses change when you copy an instance:</span></span>

- <span data-ttu-id="5dde9-156">Kaikkien käyttäjien tilaksi järjestelmänvalvojaa lukuun ottamatta asetetaan **Pois käytöstä**.</span><span class="sxs-lookup"><span data-stu-id="5dde9-156">All users except Admin are set to **Disabled**.</span></span>

- <span data-ttu-id="5dde9-157">Kaikki erätyöt joitakin järjestelmätöitä lukuun ottamatta asetetaan tilaan **Pidätä**.</span><span class="sxs-lookup"><span data-stu-id="5dde9-157">All batch jobs, except for some system jobs, are set to **Withhold**.</span></span>

## <a name="environment-admin"></a><span data-ttu-id="5dde9-158">Ympäristön järjestelmänvalvoja</span><span class="sxs-lookup"><span data-stu-id="5dde9-158">Environment admin</span></span>

<span data-ttu-id="5dde9-159">Kaikki eristetyn kohdeympäristön käyttäjät, myös järjestelmänvalvojat, korvataan lähdeympäristön käyttäjillä.</span><span class="sxs-lookup"><span data-stu-id="5dde9-159">All users in the target sandbox environment, including Administrators, are replaced by the users of the source environment.</span></span> <span data-ttu-id="5dde9-160">Varmista ennen esiintymän kopioimista, että olet kohdeympäristön järjestelmänvalvoja.</span><span class="sxs-lookup"><span data-stu-id="5dde9-160">Before you copy an instance, be sure that you're an Administrator in the target environment.</span></span> <span data-ttu-id="5dde9-161">Jos et ole, et voi kirjautua eristettyyn kohdeympäristöön, kun kopiointi on valmis.</span><span class="sxs-lookup"><span data-stu-id="5dde9-161">If you aren't, you won't be able to sign in to the target sandbox environment after the copy has completed.</span></span>

<span data-ttu-id="5dde9-162">Kaikki muut kuin järjestelmänvalvojakäyttäjät poistetaan käytöstä eristetyssä kohdeympäristössä, jotta estetään ei-toivotut kirjautumiset siihen.</span><span class="sxs-lookup"><span data-stu-id="5dde9-162">All non-Administrator users in the target sandbox environment are disabled to prevent unwanted sign-ins in the sandbox environment.</span></span> <span data-ttu-id="5dde9-163">Järjestelmänvalvojat voivat tarvittaessa ottaa käyttäjiä uudelleen käyttöön.</span><span class="sxs-lookup"><span data-stu-id="5dde9-163">Administrators can reenable users if needed.</span></span>
