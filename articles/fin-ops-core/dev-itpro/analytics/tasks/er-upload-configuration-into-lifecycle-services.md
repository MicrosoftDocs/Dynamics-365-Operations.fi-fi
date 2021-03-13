---
title: Konfiguraation lataaminen Lifecycle Services -palveluun
description: Tässä aiheessa käsitellään uuden sähköisen raportoinnin (ER) määrityksen luontia ja lataamista Microsoft Dynamics Lifecycle Servicesiin (LCS).
author: NickSelin
manager: AnnBe
ms.date: 09/14/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, ERDataModelDesigner, ERDataModelContentsItemCreationDialog, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 92fc6d7a8b2508c9a1f7b56ca8115adbd6ae00ea
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/30/2021
ms.locfileid: "5092538"
---
# <a name="upload-a-configuration-into-lifecycle-services"></a><span data-ttu-id="f2bf6-103">Konfiguraation lataaminen Lifecycle Services -palveluun</span><span class="sxs-lookup"><span data-stu-id="f2bf6-103">Upload a configuration into Lifecycle Services</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f2bf6-104">Tässä ohjeaiheessa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooli voi luoda uuden [sähköisen raportoinnin konfiguraation](../general-electronic-reporting.md#Configuration) ja ladata sen [projektitason resurssikirjastoon](../../lifecycle-services/asset-library.md) Microsoft Dynamics Lifecycle Services (LCS) -sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="f2bf6-104">This topic explains how a user in the System administrator or Electronic reporting developer role can create a new [Electronic reporting (ER) configuration](../general-electronic-reporting.md#Configuration) and upload it into the [project-level Asset library](../../lifecycle-services/asset-library.md) in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

<span data-ttu-id="f2bf6-105">Tässä esimerkissä luodaan konfiguraatio malliyritykselle nimeltä Litware, Inc. ja ladataan sen LCS-palveluun. Nämä vaiheet voidaan suorittaa mille tahansa yritykselle, koska kaikki yritykset jakavat sähköisen raportoinnin konfiguraatiot.</span><span class="sxs-lookup"><span data-stu-id="f2bf6-105">In this example, you will create a configuration and upload it into LCS for a sample company that is named Litware, Inc. These steps can be completed in any company, because ER configurations are shared among companies.</span></span> <span data-ttu-id="f2bf6-106">Näitä vaiheita varten on ensin suoritettava kohdassa [Konfiguroinnin tarjoajien luominen ja merkitseminen aktiivisiksi](er-configuration-provider-mark-it-active-2016-11.md) käsitellyt vaiheet.</span><span class="sxs-lookup"><span data-stu-id="f2bf6-106">To complete these steps, you must first complete the steps in [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> <span data-ttu-id="f2bf6-107">LCS:n käyttöoikeus vaaditaan myös.</span><span class="sxs-lookup"><span data-stu-id="f2bf6-107">Access to LCS is also required.</span></span>

1. <span data-ttu-id="f2bf6-108">Kirjaudu sovellukseen yhdellä seuraavista rooleista:</span><span class="sxs-lookup"><span data-stu-id="f2bf6-108">Sign in to the application by using one of the following roles:</span></span>

    - <span data-ttu-id="f2bf6-109">Sähköisen raportoinnin kehittäjä</span><span class="sxs-lookup"><span data-stu-id="f2bf6-109">Electronic reporting developer</span></span>
    - <span data-ttu-id="f2bf6-110">Järjestelmänvalvoja</span><span class="sxs-lookup"><span data-stu-id="f2bf6-110">System administrator</span></span>

2. <span data-ttu-id="f2bf6-111">Valitse **Organisaation hallinto** \> **Työtilat** \> **Sähköinen raportointi**.</span><span class="sxs-lookup"><span data-stu-id="f2bf6-111">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
3. <span data-ttu-id="f2bf6-112">Valitse **Litware, Inc.** ja merkitse se **aktiiviseksi**.</span><span class="sxs-lookup"><span data-stu-id="f2bf6-112">Select **Litware, Inc.**, and mark it as **Active**.</span></span>
4. <span data-ttu-id="f2bf6-113">Valitse **Konfiguraatiot**.</span><span class="sxs-lookup"><span data-stu-id="f2bf6-113">Select **Configurations**.</span></span>

<a name="accessconditions"></a>
> [!NOTE]
> <span data-ttu-id="f2bf6-114">Varmista, että nykyinen Dynamics 365 Finance -käyttäjä on sellaisen LCS-projektin jäsen, joka sisältää sähköisen raportoinnin konfiguraatioiden tuomisessa käytettävän[resurssikirjaston](../../lifecycle-services/asset-library.md#asset-library-support).</span><span class="sxs-lookup"><span data-stu-id="f2bf6-114">Make sure that the current Dynamics 365 Finance user is a member of the LCS project that contains the [Asset library](../../lifecycle-services/asset-library.md#asset-library-support) that is used to import ER configurations.</span></span>
>
> <span data-ttu-id="f2bf6-115">LCS-projektia ei voi käyttää sähköisen raportoinnin säilöstä, jos se on eri toimialueella kuin Financen käyttämä toimialue.</span><span class="sxs-lookup"><span data-stu-id="f2bf6-115">You can't access an LCS project from an ER repository that represents a different domain than the domain that is used in Finance.</span></span> <span data-ttu-id="f2bf6-116">Jos yrität tehdä niin, näkyviin tulee LCS-projektien tyhjä luettelo. Et voi tuoda sähköisen raportoinnin konfiguraatioita proektitason resurssikirjastosta LCS:ään.</span><span class="sxs-lookup"><span data-stu-id="f2bf6-116">If you try, an empty list of LCS projects will be shown, and you won't be able to import ER configurations from the project-level Asset library in LCS.</span></span> <span data-ttu-id="f2bf6-117">Jos haluat käyttää projektitason resurssikirjastoja sähköisen raportoinnin säilöstä, jota käytetään sähköisen raportoinnin konfiguraatioiden tuomiseen, kirjaudu sisään sen Finance-esiintymän vuokraajaan (toimialue) kuuluvan käyttäjän valtuustiedoilla, joka on valmisteltu.</span><span class="sxs-lookup"><span data-stu-id="f2bf6-117">To access project-level Asset libraries from an ER repository that is used to import ER configurations, sign in to Finance by using the credentials of a user who belongs to the tenant (domain) that the current Finance instance has been provisioned for.</span></span>

## <a name="create-a-new-data-model-configuration"></a><span data-ttu-id="f2bf6-118">Uuden tietomallin konfiguraation luominen</span><span class="sxs-lookup"><span data-stu-id="f2bf6-118">Create a new data model configuration</span></span>

1. <span data-ttu-id="f2bf6-119">Siirry kohtaan **Organisaation hallinto \> Sähköinen raportointi \> Konfiguraatiot**.</span><span class="sxs-lookup"><span data-stu-id="f2bf6-119">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
2. <span data-ttu-id="f2bf6-120">Valitse **Konfiguraatiot**-sivulla **Luo konfiguraatio** ja avaa avattava valintaikkuna.</span><span class="sxs-lookup"><span data-stu-id="f2bf6-120">On the **Configurations** page, select **Create configuration** to open the drop-down dialog box.</span></span>

    <span data-ttu-id="f2bf6-121">Tässä esimerkissä luodaan konfiguraatio, joka sisältää tietomalliesimerkin sähköisiä asiakirjoja varten.</span><span class="sxs-lookup"><span data-stu-id="f2bf6-121">In this example, you will create a configuration that contains a sample data model for electronic documents.</span></span> <span data-ttu-id="f2bf6-122">Tämä tietomallin konfiguraatio ladataan LCS:ään myöhemmin.</span><span class="sxs-lookup"><span data-stu-id="f2bf6-122">This data model configuration will be uploaded into LCS later.</span></span>

3. <span data-ttu-id="f2bf6-123">Syötä **Nimi**-kenttään **Näytemallikonfiguraatio**.</span><span class="sxs-lookup"><span data-stu-id="f2bf6-123">In the **Name** field, enter **Sample model configuration**.</span></span>
4. <span data-ttu-id="f2bf6-124">Syötä **Kuvaus**-kenttään **Näytemallikonfiguraatio**.</span><span class="sxs-lookup"><span data-stu-id="f2bf6-124">In the **Description** field, enter **Sample model configuration**.</span></span>
5. <span data-ttu-id="f2bf6-125">Valitse **Luo konfiguraatio**.</span><span class="sxs-lookup"><span data-stu-id="f2bf6-125">Select **Create configuration**.</span></span>
6. <span data-ttu-id="f2bf6-126">Valitse **Mallin suunnittelutoiminto**.</span><span class="sxs-lookup"><span data-stu-id="f2bf6-126">Select **Model designer**.</span></span>
7. <span data-ttu-id="f2bf6-127">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="f2bf6-127">Select **New**.</span></span>
8. <span data-ttu-id="f2bf6-128">Kirjoita **Nimi**-kenttään **Aloituspiste**.</span><span class="sxs-lookup"><span data-stu-id="f2bf6-128">In the **Name** field, enter **Entry point**.</span></span>
9. <span data-ttu-id="f2bf6-129">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="f2bf6-129">Select **Add**.</span></span>
10. <span data-ttu-id="f2bf6-130">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="f2bf6-130">Select **Save**.</span></span>
11. <span data-ttu-id="f2bf6-131">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="f2bf6-131">Close the page.</span></span>
12. <span data-ttu-id="f2bf6-132">Valitse **Muutoksen tila**.</span><span class="sxs-lookup"><span data-stu-id="f2bf6-132">Select **Change status**.</span></span>
13. <span data-ttu-id="f2bf6-133">Valitse **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="f2bf6-133">Select **Complete**.</span></span>
14. <span data-ttu-id="f2bf6-134">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="f2bf6-134">Select **OK**.</span></span>
15. <span data-ttu-id="f2bf6-135">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="f2bf6-135">Close the page.</span></span>

## <a name="register-a-new-repository"></a><span data-ttu-id="f2bf6-136">Rekisteröi uusi säilö</span><span class="sxs-lookup"><span data-stu-id="f2bf6-136">Register a new repository</span></span>

1. <span data-ttu-id="f2bf6-137">Siirry kohtaan **Organisaation hallinto \> Työtilat \> Sähköinen raportointi**.</span><span class="sxs-lookup"><span data-stu-id="f2bf6-137">Go to **Organization administration \> Workspaces \> Electronic reporting**.</span></span>

2. <span data-ttu-id="f2bf6-138">Valitse **Konfiguraation lähteet** -osassa **Litware, Inc.** -ruutu.</span><span class="sxs-lookup"><span data-stu-id="f2bf6-138">In the **Configuration providers** section, select the **Litware, Inc.** tile.</span></span>

3. <span data-ttu-id="f2bf6-139">Valitse **Litware, Inc.** -ruudusta **Säilöt**.</span><span class="sxs-lookup"><span data-stu-id="f2bf6-139">On the **Litware, Inc.** tile, select **Repositories**.</span></span>

    <span data-ttu-id="f2bf6-140">Nyt voit avata Litware, Inc. -konfiguraatiolähteen säilöluettelon.</span><span class="sxs-lookup"><span data-stu-id="f2bf6-140">You can now open the list of repositories for the Litware, Inc. configuration provider.</span></span>

4. <span data-ttu-id="f2bf6-141">Avaa avattava valintaikkuna valitsemalla **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="f2bf6-141">Select **Add** to open the drop-down dialog box.</span></span>

    <span data-ttu-id="f2bf6-142">Nyt voit lisätä uuden säilön.</span><span class="sxs-lookup"><span data-stu-id="f2bf6-142">You can now add a new repository.</span></span>

5. <span data-ttu-id="f2bf6-143">Valitse **Konfiguraatiosäilön syöttö** -kentässä **LCS**.</span><span class="sxs-lookup"><span data-stu-id="f2bf6-143">In the **Configuration repository enter** field, select **LCS**.</span></span>
6. <span data-ttu-id="f2bf6-144">Valitse **Luo säilö**.</span><span class="sxs-lookup"><span data-stu-id="f2bf6-144">Select **Create repository**.</span></span>
7. <span data-ttu-id="f2bf6-145">Syötä arvo **Projekti**-kenttään tai valitse kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="f2bf6-145">In the **Project** field, enter or select a value.</span></span>

    <span data-ttu-id="f2bf6-146">Tässä esimerkissä valitaan haluttu LCS-projekti.</span><span class="sxs-lookup"><span data-stu-id="f2bf6-146">For this example, select the desired LCS project.</span></span> <span data-ttu-id="f2bf6-147">Sinulla on oltava projektin [käyttöoikeus](#accessconditions).</span><span class="sxs-lookup"><span data-stu-id="f2bf6-147">You must have [access](#accessconditions) to the project.</span></span>

8. <span data-ttu-id="f2bf6-148">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="f2bf6-148">Select **OK**.</span></span>

    <span data-ttu-id="f2bf6-149">Luo uusi säilön merkintä.</span><span class="sxs-lookup"><span data-stu-id="f2bf6-149">Complete a new repository entry.</span></span>

9. <span data-ttu-id="f2bf6-150">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="f2bf6-150">In the list, mark the selected row.</span></span>

    <span data-ttu-id="f2bf6-151">Valitse tässä esimerkissä **LCS**-säilötietue.</span><span class="sxs-lookup"><span data-stu-id="f2bf6-151">For this example, select the **LCS** repository record.</span></span>

    <span data-ttu-id="f2bf6-152">Huomaa, että rekisteröity säilö on merkitty nykyisellä palveluntarjoalla.</span><span class="sxs-lookup"><span data-stu-id="f2bf6-152">Note that a registered repository is marked by the current provider.</span></span> <span data-ttu-id="f2bf6-153">Toisin sanoen vain kyseisen palveluntarjoajan omistamat konfiguraatiot voidaan sijoittaa tähän säilöön. Tämän vuoksi ne ladataan valittuun LCS-projektiin.</span><span class="sxs-lookup"><span data-stu-id="f2bf6-153">In other words, only configurations that are owned by that provider can be put in this repository and therefore uploaded into the selected LCS project.</span></span>

10. <span data-ttu-id="f2bf6-154">Valitse **Avaa**.</span><span class="sxs-lookup"><span data-stu-id="f2bf6-154">Select **Open**.</span></span>

    <span data-ttu-id="f2bf6-155">Avaa säilö, jotta voit tarkastella sähköisen raportoinnin konfiguraatioiden luetteloa.</span><span class="sxs-lookup"><span data-stu-id="f2bf6-155">You open the repository to view the list of ER configurations.</span></span> <span data-ttu-id="f2bf6-156">Jos valittua projektia ei ole vielä käytetty sähköisen raportoinnin konfiguraatioiden jakamiseen, luettelo on tyhjä.</span><span class="sxs-lookup"><span data-stu-id="f2bf6-156">If the selected project hasn't yet been used for ER configurations sharing, the list will be empty.</span></span>

11. <span data-ttu-id="f2bf6-157">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="f2bf6-157">Close the page.</span></span>
12. <span data-ttu-id="f2bf6-158">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="f2bf6-158">Close the page.</span></span>

## <a name="upload-a-configuration-into-lcs"></a><span data-ttu-id="f2bf6-159">Lataa konfiguraatio LCS-järjestelmään</span><span class="sxs-lookup"><span data-stu-id="f2bf6-159">Upload a configuration into LCS</span></span>

1. <span data-ttu-id="f2bf6-160">Siirry kohtaan **Organisaation hallinto \> Sähköinen raportointi \> Konfiguraatiot**.</span><span class="sxs-lookup"><span data-stu-id="f2bf6-160">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
2. <span data-ttu-id="f2bf6-161">Valitse **Konfiguraatiot**-sivun konfiguraatiopuussa **Näytemallikonfiguraatio**.</span><span class="sxs-lookup"><span data-stu-id="f2bf6-161">On the **Configurations** page, in the configurations tree, select **Sample model configuration**.</span></span>

    <span data-ttu-id="f2bf6-162">Valitse luotu konfiguraatio, joka on jo valmis.</span><span class="sxs-lookup"><span data-stu-id="f2bf6-162">You must select a created configuration that has been already completed.</span></span>

3. <span data-ttu-id="f2bf6-163">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="f2bf6-163">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="f2bf6-164">Valitse tässä esimerkissä valitun konfiguraation versio, jonka tila on **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="f2bf6-164">For this example, select the version of the selected configuration that has a status of **Completed**.</span></span>

4. <span data-ttu-id="f2bf6-165">Valitse **Muutoksen tila**.</span><span class="sxs-lookup"><span data-stu-id="f2bf6-165">Select **Change status**.</span></span>
5. <span data-ttu-id="f2bf6-166">Valitse **Jaa**.</span><span class="sxs-lookup"><span data-stu-id="f2bf6-166">Select **Share**.</span></span>

    <span data-ttu-id="f2bf6-167">Konfiguraation tila muutetaan **Valmis**-tilasta **Jaettu**-tilaksi, kun konfiguraatio julkaistaan LCS:ssä.</span><span class="sxs-lookup"><span data-stu-id="f2bf6-167">The status of the configuration is changed from **Completed** to **Shared** when the configuration is published in LCS.</span></span>

6. <span data-ttu-id="f2bf6-168">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="f2bf6-168">Select **OK**.</span></span>
7. <span data-ttu-id="f2bf6-169">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="f2bf6-169">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="f2bf6-170">Valitse tässä esimerkissä konfiguraation versio, jonka tila on **Jaettu**.</span><span class="sxs-lookup"><span data-stu-id="f2bf6-170">For this example, select the configuration version that has a status of **Shared**.</span></span>

    <span data-ttu-id="f2bf6-171">Huomaa, että valitun version on tila on muutetaan **Valmis**-tilasta **Jaettu**-tilaan.</span><span class="sxs-lookup"><span data-stu-id="f2bf6-171">Note that the status of the selected version was changed from **Completed** to **Shared**.</span></span>

8. <span data-ttu-id="f2bf6-172">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="f2bf6-172">Close the page.</span></span>
9. <span data-ttu-id="f2bf6-173">Valitse **Säilöt**.</span><span class="sxs-lookup"><span data-stu-id="f2bf6-173">Select **Repositories**.</span></span>

    <span data-ttu-id="f2bf6-174">Nyt voit avata Litware, Inc. -konfiguraatiolähteen säilöluettelon.</span><span class="sxs-lookup"><span data-stu-id="f2bf6-174">You can now open the list of repositories for the Litware, Inc. configuration provider.</span></span>

10. <span data-ttu-id="f2bf6-175">Valitse **Avaa**.</span><span class="sxs-lookup"><span data-stu-id="f2bf6-175">Select **Open**.</span></span>

    <span data-ttu-id="f2bf6-176">Valitse tässä esimerkissä **LCS**-säilötietue ja avaa se.«»</span><span class="sxs-lookup"><span data-stu-id="f2bf6-176">For this example, select the **LCS** repository, and open it.</span></span>

    <span data-ttu-id="f2bf6-177">Huomaa, että valittu konfiguraatio näytetään resurssina valitussa LCS-projektissa.</span><span class="sxs-lookup"><span data-stu-id="f2bf6-177">Notice that the selected configuration is shown as an asset of the selected LCS project.</span></span>

11. <span data-ttu-id="f2bf6-178">Avaa LCS siirtymällä osoitteeseen <https://lcs.dynamics.com>.</span><span class="sxs-lookup"><span data-stu-id="f2bf6-178">Open LCS by going to <https://lcs.dynamics.com>.</span></span>
12. <span data-ttu-id="f2bf6-179">Avaa projekti, jota käytettiin aiemmin säilön rekisteröinnissä.</span><span class="sxs-lookup"><span data-stu-id="f2bf6-179">Open a project that was used earlier for repository registration.</span></span>
13. <span data-ttu-id="f2bf6-180">Avaa projektin resurssikirjasto.</span><span class="sxs-lookup"><span data-stu-id="f2bf6-180">Open the Asset library of the project.</span></span>
14. <span data-ttu-id="f2bf6-181">Valitse **GER-konfiguraatio**-resurssityyppi.</span><span class="sxs-lookup"><span data-stu-id="f2bf6-181">Select the **GER configuration** asset type.</span></span>

    <span data-ttu-id="f2bf6-182">Ladattu sähköisen raportoinnin konfiguraatio näkyy luettelossa.</span><span class="sxs-lookup"><span data-stu-id="f2bf6-182">The ER configuration that you uploaded should be listed.</span></span>

    <span data-ttu-id="f2bf6-183">Huomaa, että ladattu LCS-konfiguraatio voidaan tuoda toiseen esiintymään, jos tarjoajilla on käyttöoikeus tähän LCS-projektiin.</span><span class="sxs-lookup"><span data-stu-id="f2bf6-183">Note that the uploaded LCS configuration can be imported into another instance if providers have access to this LCS project.</span></span>
