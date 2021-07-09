---
title: Konfiguraation tuominen Lifecycle Services -palvelusta
description: Tässä aiheessa käsitellään sähköisen raportoinnin (ER) määrityksen uuden version tuontia Microsoft Dynamics Lifecycle Servicesista (LCS).
author: NickSelin
ms.date: 06/17/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionRepositoryTable, ERSolutionImport
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b58ecb8a7d6f52631dbca7642a4acbcf6ff895a3
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/17/2021
ms.locfileid: "6270834"
---
# <a name="import-a-configuration-from-lifecycle-services"></a><span data-ttu-id="3f37a-103">Konfiguraation tuominen Lifecycle Services -palvelusta</span><span class="sxs-lookup"><span data-stu-id="3f37a-103">Import a configuration from Lifecycle Services</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3f37a-104">Tässä ohjeaiheessa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooli voi tuoda uuden [sähköisen raportoinnin konfiguraation](../general-electronic-reporting.md#Configuration) version ja ladata sen [projektitason resurssikirjastosta](../../lifecycle-services/asset-library.md) Microsoft Dynamics Lifecycle Services (LCS) -sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="3f37a-104">This topic explains how a user in the System administrator or Electronic reporting developer role can import a new version of an [Electronic reporting (ER) configuration](../general-electronic-reporting.md#Configuration) from the [project-level Asset library](../../lifecycle-services/asset-library.md) in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3f37a-105">Lifecycle Services (LCS) -palveluiden käyttö sähköisen raportoinnin (ER) konfiguraatioiden tallennusvarastona on [vanhentunut](../../../../finance/get-started/removed-deprecated-features-finance.md#features-removed-or-deprecated-in-the-finance-10017-release).</span><span class="sxs-lookup"><span data-stu-id="3f37a-105">The use of LCS as a storage repository for ER configurations is being [deprecated](../../../../finance/get-started/removed-deprecated-features-finance.md#features-removed-or-deprecated-in-the-finance-10017-release).</span></span> <span data-ttu-id="3f37a-106">Lue lisätietoja kohdasta [Regulatory Configuration Service (RCS) – Lifecycle Services (LCS) -tallennustilan vanhentuminen](../../../../finance/localizations/rcs-lcs-repo-dep-faq.md).</span><span class="sxs-lookup"><span data-stu-id="3f37a-106">For more information, see [Regulatory Configuration Service (RCS) – Lifecycle Services (LCS) storage deprecation](../../../../finance/localizations/rcs-lcs-repo-dep-faq.md).</span></span>

<span data-ttu-id="3f37a-107">Tässä esimerkissä valitaan sopiva ER-konfiguraatio ja tuodaan se malliyritykselle nimeltä Litware, Inc. Nämä vaiheet voidaan suorittaa mille tahansa yritykselle, koska kaikki yritykset jakavat sähköisen raportoinnin konfiguraatiot.</span><span class="sxs-lookup"><span data-stu-id="3f37a-107">In this example, you will select the desired version of the ER configuration and import it for a sample company that is named Litware, Inc. These steps can be completed in any company, because ER configurations are shared among companies.</span></span> <span data-ttu-id="3f37a-108">Jos haluat tehdä nämä vaiheet, tee ensin vaiheet kohdassa [Konfiguraation lataaminen Lifecycle Services -palveluun](er-upload-configuration-into-lifecycle-services.md).</span><span class="sxs-lookup"><span data-stu-id="3f37a-108">To complete these steps, you must first complete the steps in [Upload a configuration into Lifecycle Services](er-upload-configuration-into-lifecycle-services.md).</span></span> <span data-ttu-id="3f37a-109">LCS:n käyttöoikeus vaaditaan myös.</span><span class="sxs-lookup"><span data-stu-id="3f37a-109">Access to LCS is also required.</span></span>

1. <span data-ttu-id="3f37a-110">Kirjaudu sovellukseen yhdellä seuraavista rooleista:</span><span class="sxs-lookup"><span data-stu-id="3f37a-110">Sign in to the application by using one of the following roles:</span></span>

    - <span data-ttu-id="3f37a-111">Sähköisen raportoinnin kehittäjä</span><span class="sxs-lookup"><span data-stu-id="3f37a-111">Electronic reporting developer</span></span>
    - <span data-ttu-id="3f37a-112">Järjestelmänvalvoja</span><span class="sxs-lookup"><span data-stu-id="3f37a-112">System administrator</span></span>

2. <span data-ttu-id="3f37a-113">Valitse **Organisaation hallinto** \> **Työtilat** \> **Sähköinen raportointi**.</span><span class="sxs-lookup"><span data-stu-id="3f37a-113">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
3. <span data-ttu-id="3f37a-114">Valitse **Konfiguraatiot**.</span><span class="sxs-lookup"><span data-stu-id="3f37a-114">Select **Configurations**.</span></span>

<a name="accessconditions"></a>
> [!NOTE]
> <span data-ttu-id="3f37a-115">Varmista, että nykyinen Dynamics 365 Finance -käyttäjä on sellaisen LCS-projektin jäsen, joka sisältää sen resurssikirjaston, jonka [käyttöoikeuden](../../lifecycle-services/asset-library.md#asset-library-support) käyttäjä haluaa sähköisen raportoinnin konfiguraatioiden tuomista varten.</span><span class="sxs-lookup"><span data-stu-id="3f37a-115">Make sure that the current Dynamics 365 Finance user is a member of the LCS project that contains the Asset library that the user wants to [access](../../lifecycle-services/asset-library.md#asset-library-support) to import ER configurations.</span></span>
>
> <span data-ttu-id="3f37a-116">LCS-projektia ei voi käyttää sähköisen raportoinnin säilöstä, jos se on eri toimialueella kuin Financen käyttämä toimialue.</span><span class="sxs-lookup"><span data-stu-id="3f37a-116">You can't access an LCS project from an ER repository that represents a different domain than the domain that is used in Finance.</span></span> <span data-ttu-id="3f37a-117">Jos yrität tehdä niin, näkyviin tulee LCS-projektien tyhjä luettelo. Et voi tuoda sähköisen raportoinnin konfiguraatioita proektitason resurssikirjastosta LCS:ään.</span><span class="sxs-lookup"><span data-stu-id="3f37a-117">If you try, an empty list of LCS projects will be shown, and you won't be able to import ER configurations from the project-level Asset library in LCS.</span></span> <span data-ttu-id="3f37a-118">Jos haluat käyttää projektitason resurssikirjastoja sähköisen raportoinnin säilöstä, jota käytetään sähköisen raportoinnin konfiguraatioiden tuomiseen, kirjaudu sisään sen Finance-esiintymän vuokraajaan (toimialue) kuuluvan käyttäjän valtuustiedoilla, joka on valmisteltu.</span><span class="sxs-lookup"><span data-stu-id="3f37a-118">To access project-level Asset libraries from an ER repository that is used to import ER configurations, sign in to Finance by using the credentials of a user who belongs to the tenant (domain) that the current Finance instance has been provisioned for.</span></span>

## <a name="delete-a-shared-version-of-a-data-model-configuration"></a><span data-ttu-id="3f37a-119">Poista tietomallin konfiguraation jaettu versio</span><span class="sxs-lookup"><span data-stu-id="3f37a-119">Delete a shared version of a data model configuration</span></span>

1. <span data-ttu-id="3f37a-120">Valitse **Konfiguraatiot**-sivun konfiguraatiopuussa **Näytemallikonfiguraatio**.</span><span class="sxs-lookup"><span data-stu-id="3f37a-120">On the **Configurations** page, in the configurations tree, select **Sample model configuration**.</span></span>

    <span data-ttu-id="3f37a-121">Ensimmäinen näytetietomallin konfiguraatio luotiin ja julkaistiin LCS:ään, kun kohdan [Konfiguraation lataaminen Lifecycle Services -palveluun](er-upload-configuration-into-lifecycle-services.md) vaiheet suoritettiin.</span><span class="sxs-lookup"><span data-stu-id="3f37a-121">You created the first version of a sample data model configuration and published it to LCS when you completed the steps in [Upload a configuration into Lifecycle Services](er-upload-configuration-into-lifecycle-services.md).</span></span> <span data-ttu-id="3f37a-122">Tässä menettelyssä poistetaan kyseinen ER-konfiguraation versio.</span><span class="sxs-lookup"><span data-stu-id="3f37a-122">In this procedure, you will delete that version of the ER configuration.</span></span> <span data-ttu-id="3f37a-123">Tämän jälkeen voit tuoda version LCS:stä myöhemmin tähän aiheeseen.</span><span class="sxs-lookup"><span data-stu-id="3f37a-123">You will then import that version from LCS later in this topic.</span></span>

2. <span data-ttu-id="3f37a-124">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="3f37a-124">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="3f37a-125">Valitse tässä esimerkissä konfiguraation versio, jonka tila on **Jaettu**.</span><span class="sxs-lookup"><span data-stu-id="3f37a-125">For this example, select the version of the configuration that has a status of **Shared**.</span></span> <span data-ttu-id="3f37a-126">Tämä tila ilmaisee, että konfiguraatio on julkaistu LCS:ään.</span><span class="sxs-lookup"><span data-stu-id="3f37a-126">This status indicates that the configuration has been published to LCS.</span></span>

3. <span data-ttu-id="3f37a-127">Valitse **Muutoksen tila**.</span><span class="sxs-lookup"><span data-stu-id="3f37a-127">Select **Change status**.</span></span>
4. <span data-ttu-id="3f37a-128">Valitse **Keskeytä**.</span><span class="sxs-lookup"><span data-stu-id="3f37a-128">Select **Discontinue**.</span></span>

    <span data-ttu-id="3f37a-129">Jos muutat valitun version tilan **Jaettu**-tilasta **Keskeytetty**-tilaksi, versio voidaan poistaa.</span><span class="sxs-lookup"><span data-stu-id="3f37a-129">By changing the status of the selected version from **Shared** to **Discontinued**, you make the version available for deletion.</span></span>

5. <span data-ttu-id="3f37a-130">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="3f37a-130">Select **OK**.</span></span>
6. <span data-ttu-id="3f37a-131">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="3f37a-131">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="3f37a-132">Valitse tässä esimerkissä konfiguraation versio, jonka tila on **Keskeytetty**.</span><span class="sxs-lookup"><span data-stu-id="3f37a-132">For this example, select the version of the configuration that has a status of **Discontinued**.</span></span>

7. <span data-ttu-id="3f37a-133">Valitse **Poista**.</span><span class="sxs-lookup"><span data-stu-id="3f37a-133">Select **Delete**.</span></span>
8. <span data-ttu-id="3f37a-134">Valitse **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="3f37a-134">Select **Yes**.</span></span>

    <span data-ttu-id="3f37a-135">Huomaa, että vain valitun tietomallin konfiguraation luonnosversio 2 on nyt käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="3f37a-135">Notice that the only draft version 2 of the selected data model configuration is now available.</span></span>

9. <span data-ttu-id="3f37a-136">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="3f37a-136">Close the page.</span></span>

## <a name="import-a-shared-version-of-a-data-model-configuration-from-lcs"></a><span data-ttu-id="3f37a-137">Tuo tietomallin konfiguraation jaettu versio LCS:stä</span><span class="sxs-lookup"><span data-stu-id="3f37a-137">Import a shared version of a data model configuration from LCS</span></span>

1. <span data-ttu-id="3f37a-138">Siirry kohtaan **Organisaation hallinto \> Työtilat \> Sähköinen raportointi**.</span><span class="sxs-lookup"><span data-stu-id="3f37a-138">Go to **Organization administration \> Workspaces \> Electronic reporting**.</span></span>

2. <span data-ttu-id="3f37a-139">Valitse **Konfiguraation lähteet** -osassa **Litware, Inc.** -ruutu.</span><span class="sxs-lookup"><span data-stu-id="3f37a-139">In the **Configuration providers** section, select the **Litware, Inc.** tile.</span></span>

3. <span data-ttu-id="3f37a-140">Valitse **Litware, Inc.** -ruudusta **Säilöt**.</span><span class="sxs-lookup"><span data-stu-id="3f37a-140">On the **Litware, Inc.** tile, select **Repositories**.</span></span>

    <span data-ttu-id="3f37a-141">Nyt voit avata Litware, Inc. -konfiguraatiolähteen säilöluettelon.</span><span class="sxs-lookup"><span data-stu-id="3f37a-141">You can now open the list of repositories for the Litware, Inc. configuration provider.</span></span>

4. <span data-ttu-id="3f37a-142">Valitse **Avaa**.</span><span class="sxs-lookup"><span data-stu-id="3f37a-142">Select **Open**.</span></span>

    <span data-ttu-id="3f37a-143">Valitse tässä esimerkissä **LCS**-säilötietue ja avaa se.«»</span><span class="sxs-lookup"><span data-stu-id="3f37a-143">For this example, select the **LCS** repository, and open it.</span></span> <span data-ttu-id="3f37a-144">Sinulla on oltava [käyttöoikeus](#accessconditions) LCS-projektiin ja resurssikirjastoon, jota valittu sähköisen raportoinnin säilö käyttää.</span><span class="sxs-lookup"><span data-stu-id="3f37a-144">You must have [access](#accessconditions) to the LCS project and to the Asset library that is accessed by the selected ER repository.</span></span>

5. <span data-ttu-id="3f37a-145">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="3f37a-145">In the list, mark the selected row.</span></span>

    <span data-ttu-id="3f37a-146">Valitse tässä esimerkissä versioluettelosta ensimmäinen **näytemallikonfiguraatio**.</span><span class="sxs-lookup"><span data-stu-id="3f37a-146">For this example, select the first version of **Sample model configuration** in the version list.</span></span>

6. <span data-ttu-id="3f37a-147">Valitse **Tuo**.</span><span class="sxs-lookup"><span data-stu-id="3f37a-147">Select **Import**.</span></span>
7. <span data-ttu-id="3f37a-148">Vahvista valitun version tuonti LCS:stä valitsemalla **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="3f37a-148">Select **Yes** to confirm the import of the selected version from LCS.</span></span>

    <span data-ttu-id="3f37a-149">Tietosanoma vahvistaa, että valittu versio on tuotu.</span><span class="sxs-lookup"><span data-stu-id="3f37a-149">An informational message confirms that the selected version was successfully imported.</span></span>

8. <span data-ttu-id="3f37a-150">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="3f37a-150">Close the page.</span></span>
9. <span data-ttu-id="3f37a-151">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="3f37a-151">Close the page.</span></span>
10. <span data-ttu-id="3f37a-152">Valitse **Konfiguraatiot**.</span><span class="sxs-lookup"><span data-stu-id="3f37a-152">Select **Configurations**.</span></span>
11. <span data-ttu-id="3f37a-153">Valitse puussa **Näytemallikonfiguraatio**.</span><span class="sxs-lookup"><span data-stu-id="3f37a-153">In the tree, select **Sample model configuration**.</span></span>
12. <span data-ttu-id="3f37a-154">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="3f37a-154">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="3f37a-155">Valitse tässä esimerkissä konfiguraation versio, jonka tila on **Jaettu**.</span><span class="sxs-lookup"><span data-stu-id="3f37a-155">For this example, select the version of the configuration that has a status of **Shared**.</span></span>

    <span data-ttu-id="3f37a-156">Huomaa, että valitun tietomallin konfiguraation jaettu versio 1 on nyt myös käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="3f37a-156">Notice that shared version 1 of the selected data model configuration is also available now.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
