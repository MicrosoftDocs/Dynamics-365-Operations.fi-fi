---
title: Konfiguraation tuominen Lifecycle Services -palvelusta
description: Tässä ohjeaiheessa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooli voi tuoda uuden sähköisen raportoinnin konfiguraation version Microsoft Dynamics Lifecycle Services (LCS) -sovelluksesta.
author: NickSelin
manager: AnnBe
ms.date: 09/14/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionRepositoryTable, ERSolutionImport
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 59dbbf820f7a3de1e5fb31f781943320b8b1a60a
ms.sourcegitcommit: 9857d5cbdc0ab2fc9db049ac5ad118fc2b29bedc
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/14/2020
ms.locfileid: "3810640"
---
# <a name="import-a-configuration-from-lifecycle-services"></a><span data-ttu-id="6ee5a-103">Konfiguraation tuominen Lifecycle Services -palvelusta</span><span class="sxs-lookup"><span data-stu-id="6ee5a-103">Import a configuration from Lifecycle Services</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6ee5a-104">Tässä ohjeaiheessa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooli voi tuoda uuden [sähköisen raportoinnin konfiguraation](../general-electronic-reporting.md#Configuration) version ja ladata sen [projektitason resurssikirjastosta](../../lifecycle-services/asset-library.md) Microsoft Dynamics Lifecycle Services (LCS) -sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="6ee5a-104">This topic explains how a user in the System administrator or Electronic reporting developer role can import a new version of an [Electronic reporting (ER) configuration](../general-electronic-reporting.md#Configuration) from the [project-level Asset library](../../lifecycle-services/asset-library.md) in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

<span data-ttu-id="6ee5a-105">Tässä esimerkissä valitaan sopiva ER-konfiguraatio ja tuodaan se malliyritykselle nimeltä Litware, Inc. Nämä vaiheet voidaan suorittaa mille tahansa yritykselle, koska kaikki yritykset jakavat sähköisen raportoinnin konfiguraatiot.</span><span class="sxs-lookup"><span data-stu-id="6ee5a-105">In this example, you will select the desired version of the ER configuration and import it for a sample company that is named Litware, Inc. These steps can be completed in any company, because ER configurations are shared among companies.</span></span> <span data-ttu-id="6ee5a-106">Jos haluat tehdä nämä vaiheet, tee ensin vaiheet kohdassa [Konfiguraation lataaminen Lifecycle Services -palveluun](er-upload-configuration-into-lifecycle-services.md).</span><span class="sxs-lookup"><span data-stu-id="6ee5a-106">To complete these steps, you must first complete the steps in [Upload a configuration into Lifecycle Services](er-upload-configuration-into-lifecycle-services.md).</span></span> <span data-ttu-id="6ee5a-107">LCS:n käyttöoikeus vaaditaan myös.</span><span class="sxs-lookup"><span data-stu-id="6ee5a-107">Access to LCS is also required.</span></span>

1. <span data-ttu-id="6ee5a-108">Kirjaudu sovellukseen yhdellä seuraavista rooleista:</span><span class="sxs-lookup"><span data-stu-id="6ee5a-108">Sign in to the application by using one of the following roles:</span></span>

    - <span data-ttu-id="6ee5a-109">Sähköisen raportoinnin kehittäjä</span><span class="sxs-lookup"><span data-stu-id="6ee5a-109">Electronic reporting developer</span></span>
    - <span data-ttu-id="6ee5a-110">Järjestelmänvalvoja</span><span class="sxs-lookup"><span data-stu-id="6ee5a-110">System administrator</span></span>

2. <span data-ttu-id="6ee5a-111">Valitse **Organisaation hallinto** \> **Työtilat** \> **Sähköinen raportointi**.</span><span class="sxs-lookup"><span data-stu-id="6ee5a-111">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
3. <span data-ttu-id="6ee5a-112">Valitse **Konfiguraatiot**.</span><span class="sxs-lookup"><span data-stu-id="6ee5a-112">Select **Configurations**.</span></span>

<a name="accessconditions"></a>
> [!NOTE]
> <span data-ttu-id="6ee5a-113">Varmista, että nykyinen Dynamics 365 Finance -käyttäjä on sellaisen LCS-projektin jäsen, joka sisältää sen resurssikirjaston, jonka [käyttöoikeuden](../../lifecycle-services/asset-library.md#asset-library-support) käyttäjä haluaa sähköisen raportoinnin konfiguraatioiden tuomista varten.</span><span class="sxs-lookup"><span data-stu-id="6ee5a-113">Make sure that the current Dynamics 365 Finance user is a member of the LCS project that contains the Asset library that the user wants to [access](../../lifecycle-services/asset-library.md#asset-library-support) to import ER configurations.</span></span>
>
> <span data-ttu-id="6ee5a-114">LCS-projektia ei voi käyttää sähköisen raportoinnin säilöstä, jos se on eri toimialueella kuin Financen käyttämä toimialue.</span><span class="sxs-lookup"><span data-stu-id="6ee5a-114">You can't access an LCS project from an ER repository that represents a different domain than the domain that is used in Finance.</span></span> <span data-ttu-id="6ee5a-115">Jos yrität tehdä niin, näkyviin tulee LCS-projektien tyhjä luettelo. Et voi tuoda sähköisen raportoinnin konfiguraatioita proektitason resurssikirjastosta LCS:ään.</span><span class="sxs-lookup"><span data-stu-id="6ee5a-115">If you try, an empty list of LCS projects will be shown, and you won't be able to import ER configurations from the project-level Asset library in LCS.</span></span> <span data-ttu-id="6ee5a-116">Jos haluat käyttää projektitason resurssikirjastoja sähköisen raportoinnin säilöstä, jota käytetään sähköisen raportoinnin konfiguraatioiden tuomiseen, kirjaudu sisään sen Finance-esiintymän vuokraajaan (toimialue) kuuluvan käyttäjän valtuustiedoilla, joka on valmisteltu.</span><span class="sxs-lookup"><span data-stu-id="6ee5a-116">To access project-level Asset libraries from an ER repository that is used to import ER configurations, sign in to Finance by using the credentials of a user who belongs to the tenant (domain) that the current Finance instance has been provisioned for.</span></span>

## <a name="delete-a-shared-version-of-a-data-model-configuration"></a><span data-ttu-id="6ee5a-117">Poista tietomallin konfiguraation jaettu versio</span><span class="sxs-lookup"><span data-stu-id="6ee5a-117">Delete a shared version of a data model configuration</span></span>

1. <span data-ttu-id="6ee5a-118">Valitse **Konfiguraatiot**-sivun konfiguraatiopuussa **Näytemallikonfiguraatio**.</span><span class="sxs-lookup"><span data-stu-id="6ee5a-118">On the **Configurations** page, in the configurations tree, select **Sample model configuration**.</span></span>

    <span data-ttu-id="6ee5a-119">Ensimmäinen näytetietomallin konfiguraatio luotiin ja julkaistiin LCS:ään, kun kohdan [Konfiguraation lataaminen Lifecycle Services -palveluun](er-upload-configuration-into-lifecycle-services.md) vaiheet suoritettiin.</span><span class="sxs-lookup"><span data-stu-id="6ee5a-119">You created the first version of a sample data model configuration and published it to LCS when you completed the steps in [Upload a configuration into Lifecycle Services](er-upload-configuration-into-lifecycle-services.md).</span></span> <span data-ttu-id="6ee5a-120">Tässä menettelyssä poistetaan kyseinen ER-konfiguraation versio.</span><span class="sxs-lookup"><span data-stu-id="6ee5a-120">In this procedure, you will delete that version of the ER configuration.</span></span> <span data-ttu-id="6ee5a-121">Tämän jälkeen voit tuoda version LCS:stä myöhemmin tähän aiheeseen.</span><span class="sxs-lookup"><span data-stu-id="6ee5a-121">You will then import that version from LCS later in this topic.</span></span>

2. <span data-ttu-id="6ee5a-122">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="6ee5a-122">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="6ee5a-123">Valitse tässä esimerkissä konfiguraation versio, jonka tila on **Jaettu**.</span><span class="sxs-lookup"><span data-stu-id="6ee5a-123">For this example, select the version of the configuration that has a status of **Shared**.</span></span> <span data-ttu-id="6ee5a-124">Tämä tila ilmaisee, että konfiguraatio on julkaistu LCS:ään.</span><span class="sxs-lookup"><span data-stu-id="6ee5a-124">This status indicates that the configuration has been published to LCS.</span></span>

3. <span data-ttu-id="6ee5a-125">Valitse **Muutoksen tila**.</span><span class="sxs-lookup"><span data-stu-id="6ee5a-125">Select **Change status**.</span></span>
4. <span data-ttu-id="6ee5a-126">Valitse **Keskeytä**.</span><span class="sxs-lookup"><span data-stu-id="6ee5a-126">Select **Discontinue**.</span></span>

    <span data-ttu-id="6ee5a-127">Jos muutat valitun version tilan **Jaettu**-tilasta **Keskeytetty**-tilaksi, versio voidaan poistaa.</span><span class="sxs-lookup"><span data-stu-id="6ee5a-127">By changing the status of the selected version from **Shared** to **Discontinued**, you make the version available for deletion.</span></span>

5. <span data-ttu-id="6ee5a-128">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="6ee5a-128">Select **OK**.</span></span>
6. <span data-ttu-id="6ee5a-129">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="6ee5a-129">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="6ee5a-130">Valitse tässä esimerkissä konfiguraation versio, jonka tila on **Keskeytetty**.</span><span class="sxs-lookup"><span data-stu-id="6ee5a-130">For this example, select the version of the configuration that has a status of **Discontinued**.</span></span>

7. <span data-ttu-id="6ee5a-131">Valitse **Poista**.</span><span class="sxs-lookup"><span data-stu-id="6ee5a-131">Select **Delete**.</span></span>
8. <span data-ttu-id="6ee5a-132">Valitse **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="6ee5a-132">Select **Yes**.</span></span>

    <span data-ttu-id="6ee5a-133">Huomaa, että vain valitun tietomallin konfiguraation luonnosversio 2 on nyt käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="6ee5a-133">Notice that the only draft version 2 of the selected data model configuration is now available.</span></span>

9. <span data-ttu-id="6ee5a-134">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="6ee5a-134">Close the page.</span></span>

## <a name="import-a-shared-version-of-a-data-model-configuration-from-lcs"></a><span data-ttu-id="6ee5a-135">Tuo tietomallin konfiguraation jaettu versio LCS:stä</span><span class="sxs-lookup"><span data-stu-id="6ee5a-135">Import a shared version of a data model configuration from LCS</span></span>

1. <span data-ttu-id="6ee5a-136">Siirry kohtaan **Organisaation hallinto \> Työtilat \> Sähköinen raportointi**.</span><span class="sxs-lookup"><span data-stu-id="6ee5a-136">Go to **Organization administration \> Workspaces \> Electronic reporting**.</span></span>

2. <span data-ttu-id="6ee5a-137">Valitse **Konfiguraation lähteet** -osassa **Litware, Inc.** -ruutu.</span><span class="sxs-lookup"><span data-stu-id="6ee5a-137">In the **Configuration providers** section, select the **Litware, Inc.** tile.</span></span>

3. <span data-ttu-id="6ee5a-138">Valitse **Litware, Inc.** -ruudusta **Säilöt**.</span><span class="sxs-lookup"><span data-stu-id="6ee5a-138">On the **Litware, Inc.** tile, select **Repositories**.</span></span>

    <span data-ttu-id="6ee5a-139">Nyt voit avata Litware, Inc. -konfiguraatiolähteen säilöluettelon.</span><span class="sxs-lookup"><span data-stu-id="6ee5a-139">You can now open the list of repositories for the Litware, Inc. configuration provider.</span></span>

4. <span data-ttu-id="6ee5a-140">Valitse **Avaa**.</span><span class="sxs-lookup"><span data-stu-id="6ee5a-140">Select **Open**.</span></span>

    <span data-ttu-id="6ee5a-141">Valitse tässä esimerkissä **LCS**-säilötietue ja avaa se.«»</span><span class="sxs-lookup"><span data-stu-id="6ee5a-141">For this example, select the **LCS** repository, and open it.</span></span> <span data-ttu-id="6ee5a-142">Sinulla on oltava [käyttöoikeus](#accessconditions) LCS-projektiin ja resurssikirjastoon, jota valittu sähköisen raportoinnin säilö käyttää.</span><span class="sxs-lookup"><span data-stu-id="6ee5a-142">You must have [access](#accessconditions) to the LCS project and to the Asset library that is accessed by the selected ER repository.</span></span>

5. <span data-ttu-id="6ee5a-143">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="6ee5a-143">In the list, mark the selected row.</span></span>

    <span data-ttu-id="6ee5a-144">Valitse tässä esimerkissä versioluettelosta ensimmäinen **näytemallikonfiguraatio**.</span><span class="sxs-lookup"><span data-stu-id="6ee5a-144">For this example, select the first version of **Sample model configuration** in the version list.</span></span>

6. <span data-ttu-id="6ee5a-145">Valitse **Tuo**.</span><span class="sxs-lookup"><span data-stu-id="6ee5a-145">Select **Import**.</span></span>
7. <span data-ttu-id="6ee5a-146">Vahvista valitun version tuonti LCS:stä valitsemalla **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="6ee5a-146">Select **Yes** to confirm the import of the selected version from LCS.</span></span>

    <span data-ttu-id="6ee5a-147">Tietosanoma vahvistaa, että valittu versio on tuotu.</span><span class="sxs-lookup"><span data-stu-id="6ee5a-147">An informational message confirms that the selected version was successfully imported.</span></span>

8. <span data-ttu-id="6ee5a-148">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="6ee5a-148">Close the page.</span></span>
9. <span data-ttu-id="6ee5a-149">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="6ee5a-149">Close the page.</span></span>
10. <span data-ttu-id="6ee5a-150">Valitse **Konfiguraatiot**.</span><span class="sxs-lookup"><span data-stu-id="6ee5a-150">Select **Configurations**.</span></span>
11. <span data-ttu-id="6ee5a-151">Valitse puussa **Näytemallikonfiguraatio**.</span><span class="sxs-lookup"><span data-stu-id="6ee5a-151">In the tree, select **Sample model configuration**.</span></span>
12. <span data-ttu-id="6ee5a-152">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="6ee5a-152">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="6ee5a-153">Valitse tässä esimerkissä konfiguraation versio, jonka tila on **Jaettu**.</span><span class="sxs-lookup"><span data-stu-id="6ee5a-153">For this example, select the version of the configuration that has a status of **Shared**.</span></span>

    <span data-ttu-id="6ee5a-154">Huomaa, että valitun tietomallin konfiguraation jaettu versio 1 on nyt myös käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="6ee5a-154">Notice that shared version 1 of the selected data model configuration is also available now.</span></span>
