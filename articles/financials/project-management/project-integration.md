---
title: Microsoft Project -asiakasintegrointi
description: Projektin aikataulun suunnittelu ja ylläpito voi olla monimutkaista, joten projektipäälliköt tarvitsevat työkaluja tämän tehtävän hallitsemiseen. Integrointi Microsoft Project -asiakkaan kanssa tukee projektityörakenteen avaamista ja hallintaa.
author: KimANelson
manager: AnnBe
ms.date: 12/11/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjWbsTemplate
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2017-12-04
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 04b76b6c097a82e73aba007bff82b58dbbd6eb17
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/01/2019
ms.locfileid: "1838340"
---
# <a name="microsoft-project-client-integration"></a><span data-ttu-id="4dd69-104">Microsoft Project -asiakasintegrointi</span><span class="sxs-lookup"><span data-stu-id="4dd69-104">Microsoft Project client integration</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4dd69-105">Projektin aikataulun suunnittelu ja ylläpito voi olla monimutkaista, joten projektipäälliköt tarvitsevat työkaluja tämän tehtävän hallitsemiseen.</span><span class="sxs-lookup"><span data-stu-id="4dd69-105">Planning and maintaining a project schedule can be complex, so project managers need to use tools that help them manage this task.</span></span> <span data-ttu-id="4dd69-106">Integrointi Microsoft Project -asiakkaan kanssa tukee projektityörakenteen avaamista ja hallintaa.</span><span class="sxs-lookup"><span data-stu-id="4dd69-106">Integration with Microsoft Project Client provides support to open and manage a project work breakdown structure.</span></span> <span data-ttu-id="4dd69-107">Projektipäällikkö voi julkaista muutokset takaisin Finance and Operationsin projektityörakenteeseen.</span><span class="sxs-lookup"><span data-stu-id="4dd69-107">The project manager can publish any changes back to the Finance and Operations project work breakdown structure.</span></span>

> [!NOTE]
> <span data-ttu-id="4dd69-108">Jos käytössä on Microsoft Dynamics 365 for Finance and Operationsin heinäkuun päivitys, KB 4054797 ja 4055884 on asennettava.</span><span class="sxs-lookup"><span data-stu-id="4dd69-108">If you are using Microsoft Dynamics 365 for Finance and Operations, July update, you must install KB 4054797 and 4055884.</span></span>

## <a name="configure-the-microsoft-project-client-add-in"></a><span data-ttu-id="4dd69-109">Microsoft Project -asiakkaan lisäosan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="4dd69-109">Configure the Microsoft Project Client add-in</span></span>
<span data-ttu-id="4dd69-110">Microsoft Project -asiakkaan integrointi edellyttää Microsoft Dynamics 365 -lisäosan asentamista käyttäjän Microsoft Project -asiakassovellukseen.</span><span class="sxs-lookup"><span data-stu-id="4dd69-110">To enable the integration with Microsoft Project Client, a Microsoft Dynamics 365 add-in is required to be installed in the user’s client Microsoft Project application.</span></span> <span data-ttu-id="4dd69-111">Asennus tehdään avaamalla **Projektinhallinta-työtila**.</span><span class="sxs-lookup"><span data-stu-id="4dd69-111">This is done by opening the **Project management workspace**.</span></span>

<span data-ttu-id="4dd69-112">•   Valitse **Määritä Project-asiakkaan lisäosa** valitsemalla työtilassa **Linkit** > **Asetukset**.</span><span class="sxs-lookup"><span data-stu-id="4dd69-112">•   Click **Configure project client add-in** from the **Links** > **Setup** section of the workspace.</span></span>

<span data-ttu-id="4dd69-113">•   Valitse ensin **Avaa** ja sitten pyydettäessä **Suorita**.</span><span class="sxs-lookup"><span data-stu-id="4dd69-113">•   Click **Open**, then click **Run** when prompted.</span></span>

## <a name="open-and-edit-an-existing-draft-work-breakdown-structure-in-microsoft-project-client"></a><span data-ttu-id="4dd69-114">Aiemmin luodun työrakenneluonnoksen avaaminen ja muokkaaminen Microsoft Project -asiakkaassa</span><span class="sxs-lookup"><span data-stu-id="4dd69-114">Open and edit an existing draft work breakdown structure in Microsoft Project Client</span></span>
<span data-ttu-id="4dd69-115">Jos Finance and Operationsin projektiin on jo luotu työrakenne, se voidaan avata Microsoft Project -asiakassovelluksessa, jos työrakenne on luonnostilassa.</span><span class="sxs-lookup"><span data-stu-id="4dd69-115">If a project in Finance and Operations already has a work breakdown structure created, the work breakdown structure can be opened in the Microsoft Project Client application if the work breakdown structure is in a draft status.</span></span> <span data-ttu-id="4dd69-116">Jos haluat avata sen **Projekti**-sivulta, napsauta **Avaa Microsoft Projectissa** -linkkiä **Suunnitelma**-välilehdessä. Tämä sivu voidaan avata myös Microsoft Project -asiakassovelluksessa valitsemalla **Avaa** **Microsoft Dynamics 365** -välilehdessä. Valitse luettelossa **Yritys** ja **Projekti**.</span><span class="sxs-lookup"><span data-stu-id="4dd69-116">To open from the **Project** page, click **Open in Microsoft Project** link from the **Plan** tab. This page can also be opened from within the Microsoft Project Client application by clicking **Open** in the **Microsoft Dynamics 365** tab. Select the **Legal entity** and **Project** from the list.</span></span>

> [!NOTE]
> <span data-ttu-id="4dd69-117">Jos käytät Internet Explorer -selainta, sinun on valittava **Tallenna** ja avattava tiedosto manuaalisesti siitä sijainnista, johon tiedosto ladattiin.</span><span class="sxs-lookup"><span data-stu-id="4dd69-117">If you're using Internet Explorer as your browser, you will need to click **Save** to manually open from the location that the file is downloaded to.</span></span> <span data-ttu-id="4dd69-118">Vaihtoehtoisesti voit avata tiedoston Microsoft Project -asiakkaassa valitsemalla **Tallenna ja avaa**.</span><span class="sxs-lookup"><span data-stu-id="4dd69-118">Or, click **Save and open** to open the file in Microsoft Project Client.</span></span> <span data-ttu-id="4dd69-119">Älä nimeä tiedostoa uudelleen tallennuksen yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="4dd69-119">Do not rename the file name when saving.</span></span>

<span data-ttu-id="4dd69-120">Sinun on kuitattava tiedosto ulos, ennen kuin voit muokata sitä Microsoft Project -asiakkaassa. Valitse **Kuittaa ulos** **Microsoft Dynamics 365** -välilehdessä. Muut käyttäjät eivät voi nyt muokata työrakennetta Finance and Operationsissa samanaikaisesti.</span><span class="sxs-lookup"><span data-stu-id="4dd69-120">Before making any edits to the file using Microsoft Project Client, you need to check it out. Click **Check out** in the **Microsoft Dynamics 365** tab. This will prevent other users from editing the work breakdown structure from within Finance and Operations at the same time.</span></span> <span data-ttu-id="4dd69-121">Voit julkaista työrakenteen muokkausten valmistumisen jälkeen valitsemalla **Kuittaa sisään** **Microsoft Dynamics 365** -välilehdessä.</span><span class="sxs-lookup"><span data-stu-id="4dd69-121">To publish the work breakdown structure after completing any edits, click **Check in** on the **Microsoft Dynamics 365** tab.</span></span>

<span data-ttu-id="4dd69-122">Jos projektiryhmä on jo lisätty projektiin Finance and Operationsissa, ryhmän jäsenet lisätään resurssiluetteloon.</span><span class="sxs-lookup"><span data-stu-id="4dd69-122">If a project team has already been added to the project in Finance and Operations, the resource list will be populated with the team members.</span></span> <span data-ttu-id="4dd69-123">Jos projektiryhmää ei ole vielä lisätty projektiin, voit valita resurssit ja muodostaa ryhmän Microsoft Project -asiakkaassa napsauttamalla **Resurssit**-painiketta **Microsoft Dynamics 365** -välilehdessä.</span><span class="sxs-lookup"><span data-stu-id="4dd69-123">If a project team has not yet been added to the project, you can select resources and build the team within Microsoft Project Client by clicking the **Resources** button on the **Microsoft Dynamics 365** tab.</span></span> 

<span data-ttu-id="4dd69-124">Seuraavat tiedot synkronoidaan takaisin Finance and Operationsin osana sisäänkuittausta:</span><span class="sxs-lookup"><span data-stu-id="4dd69-124">The following data will be synced back to Finance and Operations as part of the check in process:</span></span>

<span data-ttu-id="4dd69-125">•   Tehtävän nimi</span><span class="sxs-lookup"><span data-stu-id="4dd69-125">•   Task name</span></span>

<span data-ttu-id="4dd69-126">•   Aloituspäivä</span><span class="sxs-lookup"><span data-stu-id="4dd69-126">•   Start date</span></span>

<span data-ttu-id="4dd69-127">•   Valmistumispäivä</span><span class="sxs-lookup"><span data-stu-id="4dd69-127">•   Finish date</span></span>

<span data-ttu-id="4dd69-128">•   Edeltäjät</span><span class="sxs-lookup"><span data-stu-id="4dd69-128">•   Predecessors</span></span>

<span data-ttu-id="4dd69-129">•   Resurssinimet</span><span class="sxs-lookup"><span data-stu-id="4dd69-129">•   Resource names</span></span>

<span data-ttu-id="4dd69-130">•   Luokka</span><span class="sxs-lookup"><span data-stu-id="4dd69-130">•   Category</span></span>

<span data-ttu-id="4dd69-131">•   Resurssiluokka</span><span class="sxs-lookup"><span data-stu-id="4dd69-131">•   Resource category</span></span>

<span data-ttu-id="4dd69-132">•   Työtunnit</span><span class="sxs-lookup"><span data-stu-id="4dd69-132">•   Work hours</span></span>

<span data-ttu-id="4dd69-133">•   Muistiinpanot</span><span class="sxs-lookup"><span data-stu-id="4dd69-133">•   Notes</span></span>

<span data-ttu-id="4dd69-134">•   Prioriteetti</span><span class="sxs-lookup"><span data-stu-id="4dd69-134">•   Priority</span></span>

> [!NOTE]
> <span data-ttu-id="4dd69-135">Jos lisäät muita sarakkeita Microsoft Project -asiakastiedostoon, niitä ei tallenneta tiedostoon eivätkä ne näy, kun tiedosto avataan seuraavan kerran.</span><span class="sxs-lookup"><span data-stu-id="4dd69-135">If you add any other columns to your Microsoft Project Client file, they will not be saved to the file and will not be displayed when the file is opened again.</span></span>

## <a name="create-the-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a><span data-ttu-id="4dd69-136">Työrakenteen luominen aiemmin luodulle projektille Microsoft Project -asiakkaan avulla</span><span class="sxs-lookup"><span data-stu-id="4dd69-136">Create the work breakdown structure for an existing project using Microsoft Project Client</span></span>
<span data-ttu-id="4dd69-137">Voit luoda uuden työrakenteen projektille Microsoft Project -asiakkaan avulla seuraavien ohjeiden avulla:</span><span class="sxs-lookup"><span data-stu-id="4dd69-137">To create a new work breakdown structure using Microsoft Project Client, follow these steps:</span></span>


1.  <span data-ttu-id="4dd69-138">Avaa Microsoft Project -asiakas.</span><span class="sxs-lookup"><span data-stu-id="4dd69-138">Open Microsoft Project Client.</span></span>

2.  <span data-ttu-id="4dd69-139">Valitse **Microsoft Dynamics 365** -välilehdessä **Avaa**.</span><span class="sxs-lookup"><span data-stu-id="4dd69-139">On the **Microsoft Dynamics 365** tab, click **Open**.</span></span>

3.  <span data-ttu-id="4dd69-140">Valitse projektille **Yritys**.</span><span class="sxs-lookup"><span data-stu-id="4dd69-140">Select the **Legal entity** for the project.</span></span>

4.  <span data-ttu-id="4dd69-141">Valitse **Projekti**.</span><span class="sxs-lookup"><span data-stu-id="4dd69-141">Select the **Project**.</span></span>

5.  <span data-ttu-id="4dd69-142">Valitse **Kuittaa ulos** **Microsoft Dynamics 365** -välilehdessä.</span><span class="sxs-lookup"><span data-stu-id="4dd69-142">Click **Check out** on the **Microsoft Dynamics 365** tab.</span></span>

6.  <span data-ttu-id="4dd69-143">Kun olet valmis julkaisemaan Finance and Operationsiin, valitse **Kuittaa sisään** **Microsoft Dynamics 365** -välilehdessä.</span><span class="sxs-lookup"><span data-stu-id="4dd69-143">When ready to publish to Finance and Operations, click **Check in** on the **Microsoft Dynamics 365** tab.</span></span>

## <a name="replace-the-existing-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a><span data-ttu-id="4dd69-144">Aiemmin luodun projektin aiemmin luodun työrakenteen korvaaminen Microsoft Project -asiakkaan avulla</span><span class="sxs-lookup"><span data-stu-id="4dd69-144">Replace the existing work breakdown structure for an existing project using Microsoft Project Client</span></span>
<span data-ttu-id="4dd69-145">Voit luoda uuden työrakenteen käyttämällä Microsoft Project -asiakasta ja korvata aiemmin luodun projektin aiemmin luodun työrakenteen seuraavien ohjeiden avulla:</span><span class="sxs-lookup"><span data-stu-id="4dd69-145">To create a new work breakdown structure using Microsoft Project Client and replace an existing work breakdown structure for an existing project, follow these steps:</span></span>

1.  <span data-ttu-id="4dd69-146">Avaa Microsoft Project -asiakas.</span><span class="sxs-lookup"><span data-stu-id="4dd69-146">Open the Microsoft Project Client.</span></span>

2.  <span data-ttu-id="4dd69-147">Luo Microsoft Project -asiakkaassa aikataulu.</span><span class="sxs-lookup"><span data-stu-id="4dd69-147">Create the schedule in Microsoft Project Client.</span></span>

3.  <span data-ttu-id="4dd69-148">Valitse **Microsoft Dynamics 365** -välilehdessä **Tallenna muutokset** > **Korvaa aiemmin luotu projekti**.</span><span class="sxs-lookup"><span data-stu-id="4dd69-148">On the **Microsoft Dynamics 365** tab, click **Save changes** > **Replace existing project**.</span></span>

4.  <span data-ttu-id="4dd69-149">Valitse projektille **Yritys**.</span><span class="sxs-lookup"><span data-stu-id="4dd69-149">Select the **Legal entity** for the project.</span></span>

5.  <span data-ttu-id="4dd69-150">Valitse **Projekti**.</span><span class="sxs-lookup"><span data-stu-id="4dd69-150">Select the **Project**.</span></span>

6.  <span data-ttu-id="4dd69-151">Napsauta **OK**.</span><span class="sxs-lookup"><span data-stu-id="4dd69-151">Click **OK**.</span></span>

## <a name="create-a-new-project-from-within-microsoft-project-client"></a><span data-ttu-id="4dd69-152">Uuden projektin luominen Microsoft Project -asiakkaassa</span><span class="sxs-lookup"><span data-stu-id="4dd69-152">Create a new project from within Microsoft Project Client</span></span>


1.  <span data-ttu-id="4dd69-153">Avaa Microsoft Project -asiakas.</span><span class="sxs-lookup"><span data-stu-id="4dd69-153">Open the Microsoft Project Client.</span></span>

2.  <span data-ttu-id="4dd69-154">Luo Microsoft Project -asiakkaassa aikataulu.</span><span class="sxs-lookup"><span data-stu-id="4dd69-154">Create the schedule in Microsoft Project Client.</span></span>

3.  <span data-ttu-id="4dd69-155">Valitse **Microsoft Dynamics 365** -välilehdessä **Tallenna muutokset** > **Tallenna uuteen projektiin**.</span><span class="sxs-lookup"><span data-stu-id="4dd69-155">On the **Microsoft Dynamics 365** tab, click **Save changes** > **Save to new Project**.</span></span>

4.  <span data-ttu-id="4dd69-156">Valitse projektille **Yritys**.</span><span class="sxs-lookup"><span data-stu-id="4dd69-156">Select the **Legal entity** for the project.</span></span>

5.  <span data-ttu-id="4dd69-157">Anna **projektitunnus** tarvittaessa.</span><span class="sxs-lookup"><span data-stu-id="4dd69-157">Enter the **Project ID**, if necessary.</span></span>

6.  <span data-ttu-id="4dd69-158">Anna **projektin nimi**.</span><span class="sxs-lookup"><span data-stu-id="4dd69-158">Enter the **Project name**.</span></span>

7.  <span data-ttu-id="4dd69-159">Valitse **Projektityyppi**, **Projektiryhmä** ja **Projektisopimuksen tunnus**.</span><span class="sxs-lookup"><span data-stu-id="4dd69-159">Select the **Project type**, **Project group** and the **Project contract ID**.</span></span> <span data-ttu-id="4dd69-160">Vaihtoehtoisesti voit luoda uuden projektisopimuksen valitsemalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="4dd69-160">Alternatively, you can create a new project contract by clicking **New**.</span></span>

8.  <span data-ttu-id="4dd69-161">Valitse resursoinnissa käytettävä **kalenteri**.</span><span class="sxs-lookup"><span data-stu-id="4dd69-161">Select the **Calendar** to be used for resourcing.</span></span>

11. <span data-ttu-id="4dd69-162">Napsauta **OK**.</span><span class="sxs-lookup"><span data-stu-id="4dd69-162">Click **OK**.</span></span>
