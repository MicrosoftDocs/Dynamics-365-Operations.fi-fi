---
title: Luo mukautettu sähköinen asiakirja muokkaamalla ER-muotoa
description: Tässä aiheessa kerrotaan, miten Microsoftin tarjoaman sähköisen raportoinnin (ER) muotoa voidaan säätää siten, että se luo mukautetun sähköisen asiakirjan.
author: NickSelin
manager: AnnBe
ms.date: 06/22/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERParameters, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner, EROperationDesigner, ERVendorTable
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3c643c913d9bc9233c891709593dff995284e2e5
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/09/2021
ms.locfileid: "5568994"
---
# <a name="adjust-an-er-format-to-generate-a-custom-electronic-document"></a><span data-ttu-id="65abf-103">Luo mukautettu sähköinen asiakirja muokkaamalla ER-muotoa</span><span class="sxs-lookup"><span data-stu-id="65abf-103">Adjust an ER format to generate a custom electronic document</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="65abf-104">Tämän ohjeen menettelyissä selitetään, miten järjestelmänvalvojan tai sähköisen raportoinnin toiminnallisen konsultin roolissa oleva käyttäjä voi tehdä nämä tehtävät:</span><span class="sxs-lookup"><span data-stu-id="65abf-104">The procedures in this topic explain how a user in the System Administrator or Electronic Reporting Functional Consultant role can perform these tasks:</span></span>

- <span data-ttu-id="65abf-105">Määritä [sähköisen raportoinnin (ER) kehyksen](general-electronic-reporting.md) parametrit.</span><span class="sxs-lookup"><span data-stu-id="65abf-105">Configure parameters for the [Electronic reporting (ER) framework](general-electronic-reporting.md).</span></span>
- <span data-ttu-id="65abf-106">Tuo ER-konfiguraatiot, jotka Microsoft tarjoaa ja joita käytetään maksutiedoston luomiseen, kun [toimittajan maksua](../../../finance/cash-bank-management/tasks/vendor-payment-overview.md) käsitellään.</span><span class="sxs-lookup"><span data-stu-id="65abf-106">Import ER configurations that are provided by Microsoft and used to generate a payment file while a [vendor payment](../../../finance/cash-bank-management/tasks/vendor-payment-overview.md) is being processed.</span></span>
- <span data-ttu-id="65abf-107">Luo mukautettu versio ER-muodon vakiokonfiguraatiosta, jonka MIcrosoft tarjoaa.</span><span class="sxs-lookup"><span data-stu-id="65abf-107">Create a custom version of a standard ER format configuration that is provided by Microsoft.</span></span>
- <span data-ttu-id="65abf-108">Muokkaa mukautettua ER-muodon konfiguraatiota siten, että se luo maksutiedostot, jotka täyttävät tietyn pankin vaatimukset.</span><span class="sxs-lookup"><span data-stu-id="65abf-108">Modify the custom ER format configuration so that it generates payment files that meets the requirements of a specific bank.</span></span>
- <span data-ttu-id="65abf-109">Ota käyttöön muutokset, jotka ER-muodon vakiokonfiguraatioon on tehty mukautetussa sähköisen raportoinnin muodon konfiguraatiossa.</span><span class="sxs-lookup"><span data-stu-id="65abf-109">Adopt changes that are made to the standard ER format configuration in the custom ER format configuration.</span></span>

<span data-ttu-id="65abf-110">Kaikki seuraavat toimenpiteet voidaan tehdä **GBSI**-yrityksessä.</span><span class="sxs-lookup"><span data-stu-id="65abf-110">All the following procedures can be done in the **GBSI** company.</span></span> <span data-ttu-id="65abf-111">Koodausta ei tarvita.</span><span class="sxs-lookup"><span data-stu-id="65abf-111">No coding is required.</span></span>

- [<span data-ttu-id="65abf-112">Määritä ER-kehys</span><span class="sxs-lookup"><span data-stu-id="65abf-112">Configure the ER framework</span></span>](#ConfigureFramework)

    - [<span data-ttu-id="65abf-113">Konfiguroi ER-parametrit</span><span class="sxs-lookup"><span data-stu-id="65abf-113">Configure ER parameters</span></span>](#ConfigureParameters)
    - [<span data-ttu-id="65abf-114">Aktivoi ER-konfiguraation lähde</span><span class="sxs-lookup"><span data-stu-id="65abf-114">Activate an ER configuration provider</span></span>](#ActivateProvider)

        - [<span data-ttu-id="65abf-115">Tarkista ER-konfiguraation lähteiden luettelo</span><span class="sxs-lookup"><span data-stu-id="65abf-115">Review the list of ER configuration providers</span></span>](#ReviewProvidersList)
        - [<span data-ttu-id="65abf-116">Lisää uusi ER-konfiguraation lähde</span><span class="sxs-lookup"><span data-stu-id="65abf-116">Add a new ER configuration provider</span></span>](#ActivateProvider)
        - [<span data-ttu-id="65abf-117">Aktivoi ER-konfiguraation lähde</span><span class="sxs-lookup"><span data-stu-id="65abf-117">Activate an ER configuration provider</span></span>](#ActivateAddedProvider)

- [<span data-ttu-id="65abf-118">Tuo ER-muodon vakiokonfiguraatiot</span><span class="sxs-lookup"><span data-stu-id="65abf-118">Import the standard ER format configurations</span></span>](#ImportERSolution1)

    - [<span data-ttu-id="65abf-119">Tuo ER-vakiokonfiguraatiot</span><span class="sxs-lookup"><span data-stu-id="65abf-119">Import the standard ER configurations</span></span>](#ImportERFormat1)
    - [<span data-ttu-id="65abf-120">Tarkista tuodut ER-konfiguraatiot</span><span class="sxs-lookup"><span data-stu-id="65abf-120">Review the imported ER configurations</span></span>](#ReviewImportedERSolution)

- [<span data-ttu-id="65abf-121">Valmistele toimittajamaksu käsittelyä varten</span><span class="sxs-lookup"><span data-stu-id="65abf-121">Prepare a vendor payment for processing</span></span>](#PrepareVendorPayment)

    - [<span data-ttu-id="65abf-122">Lisää toimittajatilin pankkitiedot</span><span class="sxs-lookup"><span data-stu-id="65abf-122">Add bank information for a vendor account</span></span>](#AddBankAccount)
    - [<span data-ttu-id="65abf-123">Lisää toimittajamaksu</span><span class="sxs-lookup"><span data-stu-id="65abf-123">Enter a vendor payment</span></span>](#EnterVendorPayment)

- [<span data-ttu-id="65abf-124">Käsittele toimittajamaksu käyttämällä ER-vakiomuotoa</span><span class="sxs-lookup"><span data-stu-id="65abf-124">Process a vendor payment by using the standard ER format</span></span>](#ProcessVendorPayment1)

    - [<span data-ttu-id="65abf-125">Määritä sähköinen maksutapa</span><span class="sxs-lookup"><span data-stu-id="65abf-125">Set up the electronic payment method</span></span>](#ConfigureMethodOfPayment1)
    - [<span data-ttu-id="65abf-126">Käsittele toimittajamaksu</span><span class="sxs-lookup"><span data-stu-id="65abf-126">Process a vendor payment</span></span>](#ProcessPayment1)

- [<span data-ttu-id="65abf-127">Mukauta ER-vakiomuotoa</span><span class="sxs-lookup"><span data-stu-id="65abf-127">Customize the standard ER format</span></span>](#CustomizeProvidedFormat)

    - [<span data-ttu-id="65abf-128">Luo mukautettu muoto</span><span class="sxs-lookup"><span data-stu-id="65abf-128">Create a custom format</span></span>](#DeriveProvidedFormat)
    - [<span data-ttu-id="65abf-129">Muokkaa mukautettua muotoa</span><span class="sxs-lookup"><span data-stu-id="65abf-129">Edit a custom format</span></span>](#ConfigureDerivedFormat)
    - [<span data-ttu-id="65abf-130">Merkitse mukautettu muoto suoritettavaksi</span><span class="sxs-lookup"><span data-stu-id="65abf-130">Mark a custom format as runnable</span></span>](#MarkFormatRunnable)

- [<span data-ttu-id="65abf-131">Käsittele toimittajamaksu käyttämällä mukautettua ER-muotoa</span><span class="sxs-lookup"><span data-stu-id="65abf-131">Process a vendor payment by using the custom ER format</span></span>](#ProcessVendorPayment2)

    - [<span data-ttu-id="65abf-132">Määritä sähköinen maksutapa</span><span class="sxs-lookup"><span data-stu-id="65abf-132">Set up the electronic payment method</span></span>](#ConfigureMethodOfPayment2)
    - [<span data-ttu-id="65abf-133">Käsittele toimittajamaksu</span><span class="sxs-lookup"><span data-stu-id="65abf-133">Process a vendor payment</span></span>](#ProcessPayment2)

- [<span data-ttu-id="65abf-134">Tuo ER-muodon vakiokonfiguraatioiden uudet versiot</span><span class="sxs-lookup"><span data-stu-id="65abf-134">Import new versions of the standard ER format configurations</span></span>](#ImportERSolution2)

    - [<span data-ttu-id="65abf-135">Tuo ER-vakiokonfiguraatioiden uudet versiot</span><span class="sxs-lookup"><span data-stu-id="65abf-135">Import new versions of the standard ER configurations</span></span>](#ImportERFormat2)
    - [<span data-ttu-id="65abf-136">Tarkista tuodut ER-muodon konfiguraatiot</span><span class="sxs-lookup"><span data-stu-id="65abf-136">Review the imported ER format configurations</span></span>](#ReviewImportedERFormat)

- [<span data-ttu-id="65abf-137">Ota uudessa versiossa käyttöön tuodun muodon muutokset mukautetussa muodossa</span><span class="sxs-lookup"><span data-stu-id="65abf-137">Adopt the changes in the new version of an imported format in a custom format</span></span>](#AdoptNewBaseVersion)

    - [<span data-ttu-id="65abf-138">Viimeistele mukautetun muodon nykyinen luonnosversio</span><span class="sxs-lookup"><span data-stu-id="65abf-138">Complete the current draft version of a custom format</span></span>](#CompleteDerivedFormat)
    - [<span data-ttu-id="65abf-139">Pohjusta mukautettu muoto uuteen perusversioon</span><span class="sxs-lookup"><span data-stu-id="65abf-139">Rebase a custom format to a new base version</span></span>](#RebaseDerivedFormat)
    - [<span data-ttu-id="65abf-140">Käsittele toimittajamaksu käyttämällä pohjustettua ER-muotoa</span><span class="sxs-lookup"><span data-stu-id="65abf-140">Process a vendor payment by using a rebased ER format</span></span>](#ProcessPayment3)

- [<span data-ttu-id="65abf-141">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="65abf-141">Additional resources</span></span>](#References)

## <a name="configure-the-er-framework"></a><a id="ConfigureFramework"></a><span data-ttu-id="65abf-142">Määritä ER-kehys</span><span class="sxs-lookup"><span data-stu-id="65abf-142">Configure the ER framework</span></span>

<span data-ttu-id="65abf-143">Sähköisen raportoinnin toiminnallisen konsultin roolissa olevan käyttäjän on määritettävä sähköisen raportoinnin parametrien vähimmäisjoukko, ennen kuin voit alkaa käyttää ER-kehystä mukautetun version kehittämiseen ER-vakiomuodosta.</span><span class="sxs-lookup"><span data-stu-id="65abf-143">As a user in the Electronic Reporting Functional Consultant role, you must configure the minimal set of ER parameters before you can start to use the ER framework to design a custom version of a standard ER format.</span></span>

### <a name="configure-er-parameters"></a><a id="ConfigureParameters"></a><span data-ttu-id="65abf-144">Konfiguroi ER-parametrit</span><span class="sxs-lookup"><span data-stu-id="65abf-144">Configure ER parameters</span></span>

1. <span data-ttu-id="65abf-145">Valitse **Organisaation hallinto** \> **Työtilat** \> **Sähköinen raportointi**.</span><span class="sxs-lookup"><span data-stu-id="65abf-145">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="65abf-146">Valitse **Lokalisoinnin konfiguraatiot**-sivun **Liittyvät linkit** -osassa **Sähköisen raportoinnin parametrit**.</span><span class="sxs-lookup"><span data-stu-id="65abf-146">On the **Localization configurations** page, in the **Related links** section, select **Electronic reporting parameters**.</span></span>
3. <span data-ttu-id="65abf-147">Määritä **Sähköisen raportoinnin parametrit** -sivun **Yleinen**-välilehdessä **Ota käyttöön suunnittelutila** -asetukseksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="65abf-147">On the **Electronic reporting parameters** page, on the **General** tab, set the **Enable design mode** option to **Yes**.</span></span>
4. <span data-ttu-id="65abf-148">Määritä **Liitteet**-välilehdessä seuraavat parametrit:</span><span class="sxs-lookup"><span data-stu-id="65abf-148">On the **Attachments** tab, set the following parameters:</span></span>

    - <span data-ttu-id="65abf-149">Valitse **Konfiguraatiot**-kentässä **Tiedosto**-tyyppi **USMF**-yritykselle.</span><span class="sxs-lookup"><span data-stu-id="65abf-149">In the **Configurations** field, select the **File** type for the **USMF** company.</span></span>
    - <span data-ttu-id="65abf-150">Valitse **Työarkisto**-, **Väliaikainen**-, **Perusrivi**- ja **Muut**-kentissä **Tiedosto**-tyyppi.</span><span class="sxs-lookup"><span data-stu-id="65abf-150">In the **Job archive**, **Temporary**, **Baseline**, and **Others** fields, select the **File** type.</span></span>

<span data-ttu-id="65abf-151">Lisätietoja ER-parametreista on kohdassa [Määritä ER-kehys](electronic-reporting-er-configure-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="65abf-151">For more information about ER parameters, see [Configure the ER framework](electronic-reporting-er-configure-parameters.md).</span></span>

### <a name="activate-an-er-configuration-provider"></a><a id="ActivateProvider"></a><span data-ttu-id="65abf-152">Aktivoi ER-konfiguraation lähde</span><span class="sxs-lookup"><span data-stu-id="65abf-152">Activate an ER configuration provider</span></span>

<span data-ttu-id="65abf-153">Jokainen lisätty ER-konfiguraatio merkitään ER-konfiguraation lähteen omistamaksi.</span><span class="sxs-lookup"><span data-stu-id="65abf-153">Every ER configuration that is added is marked as owned by an ER configuration provider.</span></span> <span data-ttu-id="65abf-154">ER-konfiguraation lähdettä, joka on aktivoitu **Sähköinen raportointi** -työtilassa, käytetään tähän tarkoitukseen.</span><span class="sxs-lookup"><span data-stu-id="65abf-154">The ER configuration provider that is activated in the **Electronic reporting** workspace is used for this purpose.</span></span> <span data-ttu-id="65abf-155">Siksi sinun on aktivoitava ER-konfiguraation lähde **Sähköinen raportointi** -työtilassa, ennen kuin voit alkaa lisätä tai muokata ER-konfiguraatioita.</span><span class="sxs-lookup"><span data-stu-id="65abf-155">Therefore, you must activate an ER configuration provider in the **Electronic reporting** workspace before you start to add or edit ER configurations.</span></span>

> [!NOTE]
> <span data-ttu-id="65abf-156">Vain ER-konfiguraation omistaja voi muokata sitä.</span><span class="sxs-lookup"><span data-stu-id="65abf-156">Only the owner of an ER configuration can edit it.</span></span> <span data-ttu-id="65abf-157">Siksi ennen kuin ER-konfiguraatiota voi muokata, asianmukainen ER-konfiguraation lähde on aktivoitava **Sähköinen raportointi** -työtilassa.</span><span class="sxs-lookup"><span data-stu-id="65abf-157">Therefore, before an ER configuration can be edited, the appropriate ER configuration provider must be activated in the **Electronic reporting** workspace.</span></span>

#### <a name="review-the-list-of-er-configuration-providers"></a><a id="ReviewProvidersList"></a><span data-ttu-id="65abf-158">Tarkista ER-konfiguraation lähteiden luettelo</span><span class="sxs-lookup"><span data-stu-id="65abf-158">Review the list of ER configuration providers</span></span>

1. <span data-ttu-id="65abf-159">Valitse **Organisaation hallinto** \> **Työtilat** \> **Sähköinen raportointi**.</span><span class="sxs-lookup"><span data-stu-id="65abf-159">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="65abf-160">Valitse **Lokalisoinnin konfiguraatiot**-sivun **Liittyvät linkit**-osassa **Konfiguraation lähteet**-ruutu.</span><span class="sxs-lookup"><span data-stu-id="65abf-160">On the **Localization configurations** page, in the **Related links** section, select **Configuration providers**.</span></span>
3. <span data-ttu-id="65abf-161">**Konfiguraation lähdetaulu** -sivulla jokaisen lähteen tietueella on yksilöllinen nimi ja URL-osoite.</span><span class="sxs-lookup"><span data-stu-id="65abf-161">On the **Configuration provider table** page, each provider record has a unique name and URL.</span></span> <span data-ttu-id="65abf-162">Tarkista tämän sivun sisältö.</span><span class="sxs-lookup"><span data-stu-id="65abf-162">Review the contents of this page.</span></span> <span data-ttu-id="65abf-163">Jos **Litware, Inc.** (`https://www.litware.com`) -tietue on jo olemassa, ohita seuraava menettely, [Lisää uusi ER-konfiguraation lähde](#ActivateProvider).</span><span class="sxs-lookup"><span data-stu-id="65abf-163">If a record for **Litware, Inc.** (`https://www.litware.com`) already exists, skip the next procedure, [Add a new ER configuration provider](#ActivateProvider).</span></span>

#### <a name="add-a-new-er-configuration-provider"></a><a id="ActivateProvider"></a><span data-ttu-id="65abf-164">Lisää uusi ER-konfiguraation lähde</span><span class="sxs-lookup"><span data-stu-id="65abf-164">Add a new ER configuration provider</span></span>

1. <span data-ttu-id="65abf-165">Valitse **Organisaation hallinto** \> **Työtilat** \> **Sähköinen raportointi**.</span><span class="sxs-lookup"><span data-stu-id="65abf-165">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="65abf-166">Valitse **Lokalisoinnin konfiguraatiot**-sivun **Liittyvät linkit**-osassa **Konfiguraation lähteet**-ruutu.</span><span class="sxs-lookup"><span data-stu-id="65abf-166">On the **Localization configurations** page, in the **Related links** section, select **Configuration providers**.</span></span>
3. <span data-ttu-id="65abf-167">Valitse **Konfiguraation lähteet**-sivulla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="65abf-167">On the **Configuration providers** page, select **New**.</span></span>
4. <span data-ttu-id="65abf-168">Kirjoita **Nimi**-kenttään **Litware, Inc.**</span><span class="sxs-lookup"><span data-stu-id="65abf-168">In the **Name** field, enter **Litware, Inc.**</span></span>
5. <span data-ttu-id="65abf-169">Kirjoita **Internetosoite**-kenttään `https://www.litware.com`.</span><span class="sxs-lookup"><span data-stu-id="65abf-169">In the **Internet address** field, enter `https://www.litware.com`.</span></span>
6. <span data-ttu-id="65abf-170">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="65abf-170">Select **Save**.</span></span>

#### <a name="activate-an-er-configuration-provider"></a><a id="ActivateAddedProvider"></a><span data-ttu-id="65abf-171">Aktivoi ER-konfiguraation lähde</span><span class="sxs-lookup"><span data-stu-id="65abf-171">Activate an ER configuration provider</span></span>

1. <span data-ttu-id="65abf-172">Valitse **Organisaation hallinto** \> **Työtilat** \> **Sähköinen raportointi**.</span><span class="sxs-lookup"><span data-stu-id="65abf-172">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="65abf-173">Valitse **Lokalisoinnin konfiguraatiot**-sivun **Konfiguraation lähteet**-osassa **Litware, Inc.** -ruutu ja valitse sitten **Aseta aktiiviseksi**.</span><span class="sxs-lookup"><span data-stu-id="65abf-173">On the **Localization configurations** page, in the **Configuration providers** section, select the **Litware, Inc.** tile, and then select **Set active**.</span></span>

<span data-ttu-id="65abf-174">Lisätietoja ER-konfiguraation lähteistä on kohdassa [Konfiguraation lähteiden luonti ja merkitseminen aktiiviseksi](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="65abf-174">For more information about ER configuration providers, see [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>

## <a name="import-the-standard-er-format-configurations"></a><a id="ImportERSolution1"></a><span data-ttu-id="65abf-175">Tuo ER-muodon vakiokonfiguraatiot</span><span class="sxs-lookup"><span data-stu-id="65abf-175">Import the standard ER format configurations</span></span>

### <a name="import-the-standard-er-configurations"></a><a id="ImportERFormat1"></a><span data-ttu-id="65abf-176">Tuo ER-vakiokonfiguraatiot</span><span class="sxs-lookup"><span data-stu-id="65abf-176">Import the standard ER configurations</span></span>

<span data-ttu-id="65abf-177">Jos haluat lisätä ER-vakiokonfiguraatiot nykyiseen Microsoft Dynamics 365 Finance -esiintymääsi, sinun on tuotava ne ER-[säilöstä](general-electronic-reporting.md#Repository), joka määritettiin kyseiselle esiintymälle.</span><span class="sxs-lookup"><span data-stu-id="65abf-177">To add the standard ER configurations to your current instance of Microsoft Dynamics 365 Finance, you must import them from the ER [repository](general-electronic-reporting.md#Repository) that was configured for that instance.</span></span>

1. <span data-ttu-id="65abf-178">Valitse **Organisaation hallinto** \> **Työtilat** \> **Sähköinen raportointi**.</span><span class="sxs-lookup"><span data-stu-id="65abf-178">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="65abf-179">Valitse **Lokalisoinnin konfiguraatiot**-sivun **Konfiguraation lähteet** -osassa **Microsoft**-ruutu ja valitse sitten **Säilöt** nähdäksesi luettelon Microsoft-toimittajan säilöistä.</span><span class="sxs-lookup"><span data-stu-id="65abf-179">On the **Localization configurations** page, in the **Configuration providers** section, select the **Microsoft** tile, and then select **Repositories** to view the list of repositories for the Microsoft provider.</span></span>
3. <span data-ttu-id="65abf-180">Valitse **Konfiguraatiosäilöt**-sivun ruudukossa oleva säilö, jonka tyyppi on **Yleinen** ja valitse sitten **Avaa**.</span><span class="sxs-lookup"><span data-stu-id="65abf-180">On the **Configuration repositories** page, select the repository of the **Global** type, and then select **Open**.</span></span> <span data-ttu-id="65abf-181">Jos sinulta pyydetään valtuutusta Regulatory Configuration Service -palveluun yhdistämiseen, noudata valtuutusohjeita.</span><span class="sxs-lookup"><span data-stu-id="65abf-181">If you're prompted for authorization to connect to Regulatory Configuration Service, follow the authorization instructions.</span></span>
4. <span data-ttu-id="65abf-182">Valitse **Konfiguraatiosäilö**-sivun vasemmassa ruudussa olevasta konfiguraatiopuusta **BACS (Iso-Britannia)** -muotoinen konfiguraatio.</span><span class="sxs-lookup"><span data-stu-id="65abf-182">On the **Configuration repository** page, in the configuration tree in the left pane, select the **BACS (UK)** format configuration.</span></span>
5. <span data-ttu-id="65abf-183">Valitse **Versiot**-pikavälilehdestä valitun ER-muodon konfiguraation versio **1.1**.</span><span class="sxs-lookup"><span data-stu-id="65abf-183">On the **Versions** FastTab, select version **1.1** of the selected ER format configuration.</span></span>
6. <span data-ttu-id="65abf-184">Lataa valittu versio yleisestä säilöpalvelusta nykyiseen Finance-esiintymään valitsemalla **Tuo**.</span><span class="sxs-lookup"><span data-stu-id="65abf-184">Select **Import** to download the selected version from the Global repository to the current Finance instance.</span></span>

![Konfiguraatiosäilön sivu](./media/er-quick-start2-import-solution1.png)

> [!TIP]
> <span data-ttu-id="65abf-186">Jos sinulla on ongelmia [yleiseen säilöön](er-download-configurations-global-repo.md) pääsyssä, voit [ladata konfiguraatiot](download-electronic-reporting-configuration-lcs.md) sen sijaan Microsoft Dynamics Lifecycle Services (LCS) -palvelusta.</span><span class="sxs-lookup"><span data-stu-id="65abf-186">If you have trouble accessing the [Global repository](er-download-configurations-global-repo.md), you can [download configurations](download-electronic-reporting-configuration-lcs.md) from Microsoft Dynamics Lifecycle Services (LCS) instead.</span></span>

### <a name="review-the-imported-er-configurations"></a><a id="ReviewImportedERSolution"></a><span data-ttu-id="65abf-187">Tarkista tuodut ER-konfiguraatiot</span><span class="sxs-lookup"><span data-stu-id="65abf-187">Review the imported ER configurations</span></span>

1. <span data-ttu-id="65abf-188">Valitse **Organisaation hallinto** \> **Työtilat** \> **Sähköinen raportointi**.</span><span class="sxs-lookup"><span data-stu-id="65abf-188">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="65abf-189">Valitse **Lokalisointimääritykset**-sivun **Konfiguroinnit**-osassa **Raportointimääritykset**-ruutu.</span><span class="sxs-lookup"><span data-stu-id="65abf-189">On the **Localization configurations** page, in the **Configurations** section, select the **Reporting configurations** tile.</span></span>
3. <span data-ttu-id="65abf-190">Valitse **Konfiguraatiot**-sivun konfiguraatiopuu vasemmasta ruudusta ja laajenna **Maksumalli**.</span><span class="sxs-lookup"><span data-stu-id="65abf-190">On the **Configurations** page, in the configuration tree in the left pane, expand **Payment model**.</span></span>
4. <span data-ttu-id="65abf-191">Huomaa, että valitun **BACS (Iso-Britannia)** -ER-muodon lisäksi myös muita tarvittavia ER-konfiguraatioita tuotiin.</span><span class="sxs-lookup"><span data-stu-id="65abf-191">Notice that, in addition to the selected **BACS (UK)** ER format, other required ER configurations were imported.</span></span> <span data-ttu-id="65abf-192">Varmista, että konfiguraatiopuussa ovat saatavilla seuraavat ER-konfiguraatiot:</span><span class="sxs-lookup"><span data-stu-id="65abf-192">Make sure that the following ER configurations are available in the configuration tree:</span></span>

    - <span data-ttu-id="65abf-193">**Maksumalli** – tämä konfiguraatio sisältää [tietomallin](general-electronic-reporting.md#data-model-and-model-mapping-components) ER-osan, joka esittää maksun liiketoimintatoimialueen tietorakenteen.</span><span class="sxs-lookup"><span data-stu-id="65abf-193">**Payment model** – This configuration contains the [data model](general-electronic-reporting.md#data-model-and-model-mapping-components) ER component that represents the data structure of the payment business domain.</span></span>
    - <span data-ttu-id="65abf-194">**Maksumallin määritys 1611** – tämä konfiguraatio sisältää [mallin määrityksen](general-electronic-reporting.md#data-model-and-model-mapping-components) ER-osan, joka kuvaa, miten tietomalli täytetään hakemuksen tiedoilla suorituspalvelussa.</span><span class="sxs-lookup"><span data-stu-id="65abf-194">**Payment model mapping 1611** – This configuration contains the [model mapping](general-electronic-reporting.md#data-model-and-model-mapping-components) ER component that describes how the data model is filled in with application data at runtime.</span></span>
    - <span data-ttu-id="65abf-195">**BACS (Iso-Britannia)** – tämä konfiguraatio sisältää [muodon](general-electronic-reporting.md#FormatComponentOutbound) ja muodon määrityksen ER-osat.</span><span class="sxs-lookup"><span data-stu-id="65abf-195">**BACS (UK)** – This configuration contains the [format](general-electronic-reporting.md#FormatComponentOutbound) and format mapping ER components.</span></span> <span data-ttu-id="65abf-196">Muoto-osa määrittää raportin asettelun.</span><span class="sxs-lookup"><span data-stu-id="65abf-196">The format component specifies the report layout.</span></span> <span data-ttu-id="65abf-197">Muodon määritysosa sisältää mallin tietolähteen ja määrittää, miten raportin asettelu täytetään käyttämällä tätä tietolähdettä suorituspalvelussa.</span><span class="sxs-lookup"><span data-stu-id="65abf-197">The format mapping component contains the model data source and specifies how the report layout is filled in by using this data source at runtime.</span></span>

![Konfiguroinnit-sivu](./media/er-quick-start2-imported-solution1.png)

## <a name="prepare-a-vendor-payment-for-processing"></a><a id="PrepareVendorPayment"></a><span data-ttu-id="65abf-199">Valmistele toimittajamaksu käsittelyä varten</span><span class="sxs-lookup"><span data-stu-id="65abf-199">Prepare a vendor payment for processing</span></span>

### <a name="add-bank-information-for-a-vendor-account"></a><a id="AddBankAccount"></a><span data-ttu-id="65abf-200">Lisää toimittajatilin pankkitiedot</span><span class="sxs-lookup"><span data-stu-id="65abf-200">Add bank information for a vendor account</span></span>

<span data-ttu-id="65abf-201">Sinun on lisättävä pankkitiedot toimittajatilille, johon viitataan myöhemmin rekisteröidyssä maksussa.</span><span class="sxs-lookup"><span data-stu-id="65abf-201">You must add bank information for a vendor account that will be referred to later in a registered payment.</span></span>

1. <span data-ttu-id="65abf-202">Siirry kohtaan **Ostoreskontra** \> **Toimittajat** \> **Kaikki toimittajat**.</span><span class="sxs-lookup"><span data-stu-id="65abf-202">Go to **Accounts payable** \> **Vendors** \> **All vendors**.</span></span>
2. <span data-ttu-id="65abf-203">Valitse **Kaikki toimittajat** -sivulla **GB_SI_000001**-toimittajatili ja sitten toimintoruudun **Toimittaja**-välilehden **Määritä**-ryhmässä **Pankkitilit**.</span><span class="sxs-lookup"><span data-stu-id="65abf-203">On the **All vendors** page, select the **GB_SI_000001** vendor account, and then, on the Action Pane, on the **Vendor** tab, in the **Set up** group, select **Bank accounts**.</span></span>
3. <span data-ttu-id="65abf-204">Valitse **Toimittajan pankkitilit** -sivulla **Uusi** ja lisää sitten seuraavat tiedot:</span><span class="sxs-lookup"><span data-stu-id="65abf-204">On the **Vendor bank accounts** page, select **New**, and then enter the following information:</span></span>

    1. <span data-ttu-id="65abf-205">Lisää **Pankkitili**-kenttään **GBP OPER**.</span><span class="sxs-lookup"><span data-stu-id="65abf-205">In the **Bank account** field, enter **GBP OPER**.</span></span>
    2. <span data-ttu-id="65abf-206">Valitse **Pankkiryhmä**-kentässä **BankGBP**.</span><span class="sxs-lookup"><span data-stu-id="65abf-206">In the **Bank groups** field, select **BankGBP**.</span></span>
    3. <span data-ttu-id="65abf-207">Lisää **Pankkitilin numero** -kenttään **202015**.</span><span class="sxs-lookup"><span data-stu-id="65abf-207">In the **Bank account number** field, enter **202015**.</span></span>
    4. <span data-ttu-id="65abf-208">Kirjoita **SWIFT-koodi**-kenttään <a id="DefineSWIFTCode"></a>**CHASDEFXXXX**.</span><span class="sxs-lookup"><span data-stu-id="65abf-208">In the **SWIFT code** field, enter <a id="DefineSWIFTCode"></a>**CHASDEFXXXX**.</span></span>
    5. <span data-ttu-id="65abf-209">Kirjoita **IBAN**-kenttään **GB33BUKB20201555555555**.</span><span class="sxs-lookup"><span data-stu-id="65abf-209">In the **IBAN** field, enter **GB33BUKB20201555555555**.</span></span>
    6. <span data-ttu-id="65abf-210">Pidä **Pankkikoodi**-kentän oletusarvo, <a id="DefineRoutingNumber"></a>**123456**.</span><span class="sxs-lookup"><span data-stu-id="65abf-210">In the **Routing number** field, keep the default value, <a id="DefineRoutingNumber"></a>**123456**.</span></span>

    ![Toimittajan pankkitilit -sivu](./media/er-quick-start2-bank-account.png)

4. <span data-ttu-id="65abf-212">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="65abf-212">Select **Save**.</span></span>
5. <span data-ttu-id="65abf-213">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="65abf-213">Close the page.</span></span>
6. <span data-ttu-id="65abf-214">Avaa **Kaikki toimittajat** -sivulla **GB_SI_000001**-toimittajan tili.</span><span class="sxs-lookup"><span data-stu-id="65abf-214">On the **All vendors** page, open the **GB_SI_000001** vendor account.</span></span>
7. <span data-ttu-id="65abf-215">Valitse toimittajan tietosivulla **Muokkaa**, jotta voit muokata sivua tarvittaessa.</span><span class="sxs-lookup"><span data-stu-id="65abf-215">On the vendor details page, select **Edit** to make the page editable, if required.</span></span>
8. <span data-ttu-id="65abf-216">Valitse **Maksu**-pikavälilehden **Pankkitili**-kentässä **GBP OPER**.</span><span class="sxs-lookup"><span data-stu-id="65abf-216">On the **Payment** FastTab, in the **Bank account** field, select **GBP OPER**.</span></span>

    ![Toimittajan tiedot -sivu](./media/er-quick-start2-bank-account-reference.png)

9. <span data-ttu-id="65abf-218">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="65abf-218">Select **Save**.</span></span>
10. <span data-ttu-id="65abf-219">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="65abf-219">Close the page.</span></span>

### <a name="enter-a-vendor-payment"></a><a id="EnterVendorPayment"></a><span data-ttu-id="65abf-220">Lisää toimittajamaksu</span><span class="sxs-lookup"><span data-stu-id="65abf-220">Enter a vendor payment</span></span>

<span data-ttu-id="65abf-221">Sinun on lisättävä uusi toimittajamaksu käyttämällä [maksuehdotusta](https://docs.microsoft.com/dynamics365/finance/accounts-payable/create-vendor-payments-payment-proposal).</span><span class="sxs-lookup"><span data-stu-id="65abf-221">You must enter a new vendor payment by using a [payment proposal](https://docs.microsoft.com/dynamics365/finance/accounts-payable/create-vendor-payments-payment-proposal).</span></span>

1. <span data-ttu-id="65abf-222">Valitse **Ostoreskontra** \> **Maksut** \> **Toimittajan maksukirjauskansio**.</span><span class="sxs-lookup"><span data-stu-id="65abf-222">Go to **Accounts payable** \> **Payments** \> **Vendor payment journal**.</span></span>
2. <span data-ttu-id="65abf-223">Valitse **Toimittajan maksukirjauskansio**-sivulla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="65abf-223">On the **Vendor payment journal** page, select **New**.</span></span>
3. <span data-ttu-id="65abf-224">Valitse **Nimi**-kenttään **VendPay**.</span><span class="sxs-lookup"><span data-stu-id="65abf-224">In the **Name** field, select **VendPay**.</span></span>
4. <span data-ttu-id="65abf-225">Valitse **Rivit**.</span><span class="sxs-lookup"><span data-stu-id="65abf-225">Select **Lines**.</span></span>
5. <span data-ttu-id="65abf-226">Valitse **Maksuehdotus** \> **Luo maksuehdotus**.</span><span class="sxs-lookup"><span data-stu-id="65abf-226">Select **Payment proposal** \> **Create payment proposal**.</span></span>
6. <span data-ttu-id="65abf-227">Määritä **Toimittajan maksuehdotus** -valintaikkunassa ehdot tietueiden suodattamiseen vain **GB_SI_000001** -toimittajatililtä ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="65abf-227">In the **Vendor payment proposal** dialog box, configure conditions to filter for records for the **GB_SI_000001** vendor account only, and then select **OK**.</span></span>
7. <span data-ttu-id="65abf-228">Valitse **00000007_Inv**-laskun rivi ja valitse sitten **Luo maksu**.</span><span class="sxs-lookup"><span data-stu-id="65abf-228">Select the line for the **00000007_Inv** invoice, and then select **Create payment**.</span></span>

    ![Toimittajamaksun ehdotus -valintaikkuna](./media/er-quick-start2-payment-proposal.png)

8. <span data-ttu-id="65abf-230">Varmista, että lisättävä maksu määritetään käyttämään **sähköistä** maksutapaa.</span><span class="sxs-lookup"><span data-stu-id="65abf-230">Verify that the payment that is entered is configured to use the **Electronic** method of payment.</span></span>

    ![Toimittajan maksut -sivu](./media/er-quick-start2-payment-line.png)

## <a name="process-a-vendor-payment-by-using-the-standard-er-format"></a><a id="ProcessVendorPayment1"></a><span data-ttu-id="65abf-232">Käsittele toimittajamaksu käyttämällä ER-vakiomuotoa</span><span class="sxs-lookup"><span data-stu-id="65abf-232">Process a vendor payment by using the standard ER format</span></span>

### <a name="set-up-the-electronic-payment-method"></a><a id="ConfigureMethodOfPayment1"></a><span data-ttu-id="65abf-233">Määritä sähköinen maksutapa</span><span class="sxs-lookup"><span data-stu-id="65abf-233">Set up the electronic payment method</span></span>

<span data-ttu-id="65abf-234">Sinun on määritettävä sähköinen maksutapa, jolloin se käyttää tuotua ER-muodon konfiguraatiota.</span><span class="sxs-lookup"><span data-stu-id="65abf-234">You must configure the electronic method of payment so that it uses the imported ER format configuration.</span></span>

1. <span data-ttu-id="65abf-235">Valitse **Ostoreskontra** \> **Maksun asetukset** \> **Maksutavat**.</span><span class="sxs-lookup"><span data-stu-id="65abf-235">Go to **Accounts payable** \> **Payment setup** \> **Methods of payment**.</span></span>
2. <span data-ttu-id="65abf-236">Valitse **Maksutapa - Toimittajat** -sivulla **Sähköinen** maksumenetelmä vasemmasta ruudusta.</span><span class="sxs-lookup"><span data-stu-id="65abf-236">On the **Methods of payment - vendors** page, select the **Electronic** method of payment in the left pane.</span></span>
3. <span data-ttu-id="65abf-237">Valitse **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="65abf-237">Select **Edit**.</span></span>
4. <span data-ttu-id="65abf-238">Määritä **Tiedostomuoto**-pikavälilehdessä **Yleinen sähköinen vientimuoto** -asetukseksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="65abf-238">On the **File formats** FastTab, set the **General electronic Export format** option to **Yes**.</span></span>
5. <span data-ttu-id="65abf-239">Valitse **Vientimuodon konfigurointi** -kentässä **BACS (Iso-Britannia)** -muotoinen konfiguraatio.</span><span class="sxs-lookup"><span data-stu-id="65abf-239">In the **Export format configuration** field, select the **BACS (UK)** format configuration.</span></span>

    ![Maksutapa - Toimittajat -sivu](./media/er-quick-start2-method-of-payment1.png)

6. <span data-ttu-id="65abf-241">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="65abf-241">Select **Save**.</span></span>

### <a name="process-a-vendor-payment"></a><a id="ProcessPayment1"></a><span data-ttu-id="65abf-242">Käsittele toimittajamaksu</span><span class="sxs-lookup"><span data-stu-id="65abf-242">Process a vendor payment</span></span>

1. <span data-ttu-id="65abf-243">Valitse **Ostoreskontra** \> **Maksut** \> **Toimittajan maksukirjauskansio**.</span><span class="sxs-lookup"><span data-stu-id="65abf-243">Go to **Accounts payable** \> **Payments** \> **Vendor payment journal**.</span></span>
2. <span data-ttu-id="65abf-244">Valitse **Toimittajan maksukirjauskansio** -sivulla aiemmin lisäämäsi kirjauskansio ja valitse sitten **Rivit**.</span><span class="sxs-lookup"><span data-stu-id="65abf-244">On the **Vendor payment journal** page, select the payment journal that you added earlier, and then select **Lines**.</span></span>
3. <span data-ttu-id="65abf-245">Valitse **Toimittajamaksut**-sivulla **Muodosta maksut**.</span><span class="sxs-lookup"><span data-stu-id="65abf-245">On the **Vendor payments** page, select **Generate payments**.</span></span>
4. <span data-ttu-id="65abf-246">Anna seuraavat tiedot **Muodosta maksut** -valintaikkunassa:</span><span class="sxs-lookup"><span data-stu-id="65abf-246">In the **Generate payments** dialog box, enter the following information:</span></span>

    - <span data-ttu-id="65abf-247">Valitse **Maksutapa**-kentässä **Sähköinen**.</span><span class="sxs-lookup"><span data-stu-id="65abf-247">In the **Method of payment** field, select **Electronic**.</span></span>
    - <span data-ttu-id="65abf-248">Valitse **Pankkitili**-kentässä **GBSI OPER**.</span><span class="sxs-lookup"><span data-stu-id="65abf-248">In the **Bank account** field, select **GBSI OPER**.</span></span>

5. <span data-ttu-id="65abf-249">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="65abf-249">Select **OK**.</span></span>
6. <span data-ttu-id="65abf-250">Määritä **Sähköisen raportin parametrit** -valintaikkunassa **Tulosta valvontaraportti** -asetukseksi **Kyllä** ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="65abf-250">In the **Electronic report parameters** dialog box, set the **Print control report** option to **Yes**, and then select **OK**.</span></span>

    ![Sähköisen raportin parametrit -valintasivu](./media/er-quick-start2-payment-dialog1.png)

    > [!NOTE]
    > <span data-ttu-id="65abf-252">Maksutiedoston lisäksi voit nyt luoda valvontaraportin.</span><span class="sxs-lookup"><span data-stu-id="65abf-252">In addition to the payment file, you can now generate the control report.</span></span>

7. <span data-ttu-id="65abf-253">Lataa zip-tiedosto ja pura siitä sitten seuraavat tiedostot:</span><span class="sxs-lookup"><span data-stu-id="65abf-253">Download the zip file, and then extract the following files from it:</span></span>

    - <span data-ttu-id="65abf-254">Valvontaraportti Excel-muodossa</span><span class="sxs-lookup"><span data-stu-id="65abf-254">The control report in Excel format</span></span>
    - <span data-ttu-id="65abf-255">Maksutiedosto TXT-muodossa</span><span class="sxs-lookup"><span data-stu-id="65abf-255">The payment file in TXT format</span></span>

        <span data-ttu-id="65abf-256">Huomaa, että annetun ER-muodon [rakenteen](#PositionRoutingNumber) mukaisesti luodun tiedoston maksurivi alkaa pankkikoodilla, joka [määritettiin](#DefineRoutingNumber) määritetylle pankkitilille.</span><span class="sxs-lookup"><span data-stu-id="65abf-256">Notice that, in accordance with the [structure](#PositionRoutingNumber) of the provided ER format, the payment line in the generated file starts with the routing number that was [defined](#DefineRoutingNumber) for the configured bank account.</span></span>

        ![Maksutiedosto TXT-muodossa](./media/er-quick-start2-payment-file1.png)

## <a name="customize-the-standard-er-format"></a><a id="CustomizeProvidedFormat"></a><span data-ttu-id="65abf-258">Mukauta ER-vakiomuotoa</span><span class="sxs-lookup"><span data-stu-id="65abf-258">Customize the standard ER format</span></span>

<span data-ttu-id="65abf-259">Tässä osassa näkyvässä esimerkissä haluat käyttää ER-konfiguraatioita, jotka Microsoft tarjoaa toimittajan maksutiedostojen luomiseen BACS-muodossa, mutta sinun on lisättävä mukautus tukeaksesi tietyn pankin vaatimuksia.</span><span class="sxs-lookup"><span data-stu-id="65abf-259">For the example that is shown in this section, you want to use the ER configurations that are provided by Microsoft to generate vendor payment files in BACS format, but you must add a customization to support the requirements of a specific bank.</span></span> <span data-ttu-id="65abf-260">Haluat myös pystyä päivittämään mukautettua muotoasi, kun ER-konfiguraatioista tulee uusia versioita saataville.</span><span class="sxs-lookup"><span data-stu-id="65abf-260">You also want to be able to upgrade your custom format when new versions of ER configurations become available.</span></span> <span data-ttu-id="65abf-261">Haluat kuitenkin voida päivittää mahdollisimman pienillä kustannuksilla.</span><span class="sxs-lookup"><span data-stu-id="65abf-261">However, you want to be able to do the upgrade at the lowest cost.</span></span>

<span data-ttu-id="65abf-262">Tässä tapauksessa Litware, Inc. -yhtiön edustajana sinun on luotava uusi ER-muodon konfiguraatio käyttämällä Microsoftin toimittamaa **BACS (Iso-Britannia)** -konfiguraatiota pohjana.</span><span class="sxs-lookup"><span data-stu-id="65abf-262">In this case, as the representative of Litware, Inc., you must create (derive) a new ER format configuration by using the **BACS (UK)** Microsoft-provided configuration as a base.</span></span>

### <a name="create-a-custom-format"></a><a id="DeriveProvidedFormat"></a><span data-ttu-id="65abf-263">Luo mukautettu muoto</span><span class="sxs-lookup"><span data-stu-id="65abf-263">Create a custom format</span></span>

1. <span data-ttu-id="65abf-264">Valitse **Organisaation hallinto** \> **Sähköinen raportointi** \> **Konfiguraatiot**.</span><span class="sxs-lookup"><span data-stu-id="65abf-264">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="65abf-265">Valitse **Konfiguraatiot**-sivun konfiguraatiopuu vasemmasta ruudusta, laajenna **Maksumalli** ja valitse sitten **BACS (Iso-Britannia)**.</span><span class="sxs-lookup"><span data-stu-id="65abf-265">On the **Configurations** page, in the configuration tree in the left pane, expand **Payment model**, and then select **BACS (UK)**.</span></span> <span data-ttu-id="65abf-266">Litware, Inc. käyttää tämän ER-muodon konfiguraation versiota 1.1 mukautetun version pohjana.</span><span class="sxs-lookup"><span data-stu-id="65abf-266">Litware, Inc. will use version 1.1 of this ER format configuration as the base for the custom version.</span></span>
3. <span data-ttu-id="65abf-267">Avaa pudotusvalintaikkuna valitsemalla **Luo konfigurointi**.</span><span class="sxs-lookup"><span data-stu-id="65abf-267">Select **Create configuration** to open the drop-down dialog box.</span></span> <span data-ttu-id="65abf-268">Voit käyttää tätä valintaikkunaa luodaksesi uuden konfiguroinnin mukautetulle maksumuodolle.</span><span class="sxs-lookup"><span data-stu-id="65abf-268">You can use this dialog box to create a new configuration for a custom payment format.</span></span>
4. <span data-ttu-id="65abf-269">Valitse **Uusi**-kenttäryhmässä **Johda nimestä: BACS (Iso-Britannia), Microsoft** -vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="65abf-269">In the **New** field group, select the **Derive from Name: BACS (UK), Microsoft** option.</span></span>
5. <span data-ttu-id="65abf-270">Kirjoita **Nimi**-kenttään **BACS (Iso-Britannia, mukautettu)**.</span><span class="sxs-lookup"><span data-stu-id="65abf-270">In the **Name** field, enter **BACS (UK custom)**.</span></span>

    ![Avattava Luo konfigurointi -luettelo -valintaruutu](./media/er-quick-start2-add-derived-format.png)

6. <span data-ttu-id="65abf-272">Valitse **Luo konfiguraatio**.</span><span class="sxs-lookup"><span data-stu-id="65abf-272">Select **Create configuration**.</span></span>

<span data-ttu-id="65abf-273">**BACS (Iso-Britannia, mukautettu)** -ER-muotokonfiguraation versio 1.1.1 luodaan.</span><span class="sxs-lookup"><span data-stu-id="65abf-273">Version 1.1.1 of the **BACS (UK custom)** ER format configuration is created.</span></span> <span data-ttu-id="65abf-274">Tämän version [tila](general-electronic-reporting.md#component-versioning) on **Luonnos**, ja sitä voidaan muokata.</span><span class="sxs-lookup"><span data-stu-id="65abf-274">This version has a [status](general-electronic-reporting.md#component-versioning) of **Draft** and can be edited.</span></span> <span data-ttu-id="65abf-275">Mukautetun ER-muodon nykyinen sisältö vastaa Microsoftin toimittaman muodon sisältöä.</span><span class="sxs-lookup"><span data-stu-id="65abf-275">The current content of your custom ER format matches the content of the format that is provided by Microsoft.</span></span>

![Konfiguroinnit-sivu](./media/er-quick-start2-derived-format-configuration1.png)

### <a name="edit-a-custom-format"></a><a id="ConfigureDerivedFormat"></a><span data-ttu-id="65abf-277">Muokkaa mukautettua muotoa</span><span class="sxs-lookup"><span data-stu-id="65abf-277">Edit a custom format</span></span>

<span data-ttu-id="65abf-278">Sinun on määritettävä mukautettu muoto, jotta se täyttää pankkikohtaiset vaatimukset.</span><span class="sxs-lookup"><span data-stu-id="65abf-278">You must configure your custom format so that it meets bank-specific requirements.</span></span> <span data-ttu-id="65abf-279">Pankki voi esimerkiksi edellyttää, että luotavat maksutiedostot sisältävät sen pankin Society of Worldwide Interbank Financial Telecommunication (SWIFT) -koodin, jolle on määritetty edustajan rooli käsitellyssä toimittajamaksussa.</span><span class="sxs-lookup"><span data-stu-id="65abf-279">For example, a bank might require that payment files that are generated include the Society for Worldwide Interbank Financial Telecommunication (SWIFT) code of a bank that is assigned the agent role in the processed vendor payment.</span></span> <span data-ttu-id="65abf-280">SWIFT-koodit ovat kansainvälisiä pankkikoodeja, jotka tunnistavat tietyn pankin kaikkialla maailmassa.</span><span class="sxs-lookup"><span data-stu-id="65abf-280">SWIFT codes are international bank codes that identify specific banks worldwide.</span></span> <span data-ttu-id="65abf-281">Niitä kutsutaan myös pankin tunnistekoodeiksi (Bank Identifier Code, BIC).</span><span class="sxs-lookup"><span data-stu-id="65abf-281">They are also known as Bank Identifier Codes (BICs).</span></span> <span data-ttu-id="65abf-282">SWIFT-koodin on oltava 11 merkkiä pitkä ja se on lisättävä jokaisen maksurivin alkuun luodussa maksutiedostossa.</span><span class="sxs-lookup"><span data-stu-id="65abf-282">The SWIFT code must be 11 characters long, and it must be entered at the beginning of every payment line in a generated payment file.</span></span>

1. <span data-ttu-id="65abf-283">Valitse **Organisaation hallinto** \> **Sähköinen raportointi** \> **Konfiguraatiot**.</span><span class="sxs-lookup"><span data-stu-id="65abf-283">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="65abf-284">Valitse **Konfiguraatiot**-sivun konfiguraatiopuu vasemmasta ruudusta, laajenna **Maksumalli** ja valitse sitten **BACS (Iso-Britannia, mukautettu)**.</span><span class="sxs-lookup"><span data-stu-id="65abf-284">On the **Configurations** page, in the configuration tree in the left pane, expand **Payment model**, and then select **BACS (UK custom)**.</span></span>
3. <span data-ttu-id="65abf-285">Valitse **Versiot**-pikavälilehdestä valitun konfiguraation versio **1.1.1**.</span><span class="sxs-lookup"><span data-stu-id="65abf-285">On the **Versions** FastTab, select version **1.1.1** of the selected configuration.</span></span>
4. <span data-ttu-id="65abf-286">Valitse **Suunnittelu**.</span><span class="sxs-lookup"><span data-stu-id="65abf-286">Select **Designer**.</span></span>
5. <span data-ttu-id="65abf-287">Valitse **Muodon suunnittelija** -sivulla **Näytä tiedot**, jotta näkisit lisätietoja muoto-osista.</span><span class="sxs-lookup"><span data-stu-id="65abf-287">On the **Format designer** page, select **Show details** to view more information about the format elements.</span></span>
6. <span data-ttu-id="65abf-288">Laajenna ja tarkastele seuraavia elementtejä:</span><span class="sxs-lookup"><span data-stu-id="65abf-288">Expand and review the following elements:</span></span>

    - <span data-ttu-id="65abf-289">**Kansio**-tyypin **BACSReportsFolder**-elementti.</span><span class="sxs-lookup"><span data-stu-id="65abf-289">The **BACSReportsFolder** element of the **Folder** type.</span></span> <span data-ttu-id="65abf-290">Tätä elementtiä käytetään tuotoksen luomiseen ZIP-muodossa.</span><span class="sxs-lookup"><span data-stu-id="65abf-290">This element is used to generate output in ZIP format.</span></span>
    - <span data-ttu-id="65abf-291">**Tiedosto**-tyypin **tiedosto**-elementti.</span><span class="sxs-lookup"><span data-stu-id="65abf-291">The **file** element of the **File** type.</span></span> <span data-ttu-id="65abf-292">Tätä elementtiä käytetään maksutiedoston luomiseen TXT-muodossa.</span><span class="sxs-lookup"><span data-stu-id="65abf-292">This element is used to generate a payment file in TXT format.</span></span>
    - <span data-ttu-id="65abf-293">**Järjestys**-tyypin **tapahtumat**-elementti.</span><span class="sxs-lookup"><span data-stu-id="65abf-293">The **transactions** element of the **Sequence** type.</span></span> <span data-ttu-id="65abf-294">Tätä elementtiä käytetään yhden maksurivin luomiseen maksutiedostossa.</span><span class="sxs-lookup"><span data-stu-id="65abf-294">This element is used to generate a single payment line in a payment file.</span></span>
    - <span data-ttu-id="65abf-295">**Järjestys**-tyypin **tapahtuma**-elementti.</span><span class="sxs-lookup"><span data-stu-id="65abf-295">The **transaction** element of the **Sequence** type.</span></span> <span data-ttu-id="65abf-296">Tätä elementtiä käytetään yhden maksurivin yksittäisten kenttien luomiseen.</span><span class="sxs-lookup"><span data-stu-id="65abf-296">This element is used to generate individual fields of a single payment line.</span></span>

7. <span data-ttu-id="65abf-297">Valitse **tapahtuma**-elementti.</span><span class="sxs-lookup"><span data-stu-id="65abf-297">Select the **transaction** element.</span></span>

    ![Tapahtumaelementti ER-toimintojen suunnitteluohjelmassa](./media/er-quick-start2-derived-format0.png)

    > [!NOTE]
    > <span data-ttu-id="65abf-299">Toimitettu raportti on määritetty siten, että <a id="PositionRoutingNumber"></a>jokainen maksurivi alkaa pankkikoodilla.</span><span class="sxs-lookup"><span data-stu-id="65abf-299">The provided report is configured so that <a id="PositionRoutingNumber"></a>every payment line starts with the bank routing number.</span></span> <span data-ttu-id="65abf-300">**vendBankRouteNum**-muotoelementtiä käytetään tähän tarkoitukseen.</span><span class="sxs-lookup"><span data-stu-id="65abf-300">The **vendBankRouteNum** format element is used for this purpose.</span></span> 

8. <span data-ttu-id="65abf-301">Valitse **Lisää** ja valitse sitten lisäämäsi muotoelementin **Teksti\\merkkijono** -tyyppi:</span><span class="sxs-lookup"><span data-stu-id="65abf-301">Select **Add**, and then select the **Text\\String** type of the format element that you're adding:</span></span>

    1. <span data-ttu-id="65abf-302">Syötä **Nimi**-kenttään **vendBankSWIFT**.</span><span class="sxs-lookup"><span data-stu-id="65abf-302">In the **Name** field, enter **vendBankSWIFT**.</span></span>
    2. <span data-ttu-id="65abf-303">Syötä **Vähimmäispituus**-kenttään **11**.</span><span class="sxs-lookup"><span data-stu-id="65abf-303">In the **Minimum length** field, enter **11**.</span></span>
    3. <span data-ttu-id="65abf-304">Syötä **Enimmäispituus**-kenttään **11**.</span><span class="sxs-lookup"><span data-stu-id="65abf-304">In the **Maximum length** field, enter **11**.</span></span>
    4. <span data-ttu-id="65abf-305">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="65abf-305">Select **OK**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="65abf-306">**vendBankSWIFT**-elementtiä käytetään toimittajapankin SWIFT-koodin syöttämiseen luotuihin tiedostoihin.</span><span class="sxs-lookup"><span data-stu-id="65abf-306">The **vendBankSWIFT** element will be used to enter the SWIFT code of a vendor bank in generated files.</span></span>

9. <span data-ttu-id="65abf-307">Valitse muotorakennepuussa **vendBankSWIFT**.</span><span class="sxs-lookup"><span data-stu-id="65abf-307">In the format structure tree, select **vendBankSWIFT**.</span></span>
10. <span data-ttu-id="65abf-308">Siirrä valittu muotoelementti yhden tason verran ylöspäin valitsemalla **Siirrä ylös**.</span><span class="sxs-lookup"><span data-stu-id="65abf-308">Select **Move up** to move the selected format element up one level.</span></span> <span data-ttu-id="65abf-309">Toista tätä vaihetta, kunnes **vendBankSWIFT**-elementti on <a id="PositionSWIFTCode"></a>ensimmäinen elementti pää **tapahtuma** elementin alla.</span><span class="sxs-lookup"><span data-stu-id="65abf-309">Repeat this step until the **vendBankSWIFT** element is the <a id="PositionSWIFTCode"></a>first element under the parent **transaction** element.</span></span>

    ![VendBankSWIFT ensimmäisenä elementtinä tapahtuman alla ER-toimintojen suunnitteluohjelmassa](./media/er-quick-start2-derived-format1.png)

11. <span data-ttu-id="65abf-311">Kun **vendBankSWIFT** on edelleen valittuna muotorakennepuussa, valitse **Kartoitus**-välilehti ja laajenna sitten **malli**-tietolähdettä.</span><span class="sxs-lookup"><span data-stu-id="65abf-311">While the **vendBankSWIFT** is still selected in the format structure tree, select the **Mapping** tab, and then expand the **model** data source.</span></span>
12. <span data-ttu-id="65abf-312">Laajenna **model.Payment** \> **model.Payment.CreditorAgent** ja valitse **model.Payment.CreditorAgent.BICFI**-tietolähdekenttä.</span><span class="sxs-lookup"><span data-stu-id="65abf-312">Expand **model.Payment** \> **model.Payment.CreditorAgent**, and select the **model.Payment.CreditorAgent.BICFI** data source field.</span></span> <span data-ttu-id="65abf-313">Tämä tietolähdekenttä näyttää sen toimittajapankin SWIFT-koodin, jolle on määritetty edustajan rooli käsitellyssä toimittajamaksussa.</span><span class="sxs-lookup"><span data-stu-id="65abf-313">This data source field exposes the SWIFT code of a vendor bank that is assigned the agent role in the processed vendor payment.</span></span>
13. <span data-ttu-id="65abf-314">Valitse **Sido**.</span><span class="sxs-lookup"><span data-stu-id="65abf-314">Select **Bind**.</span></span> <span data-ttu-id="65abf-315">**vendBankSWIFT**-muotoelementti on nyt sidottu **model.Payment.CreditorAgent.BICFI**-tietolähdekenttään, jotta SWIFT-koodit syötetään luotuihin maksutiedostoihin.</span><span class="sxs-lookup"><span data-stu-id="65abf-315">The **vendBankSWIFT** format element is now bound with the **model.Payment.CreditorAgent.BICFI** data source field, so that SWIFT codes will be entered in generated payment files.</span></span>

    ![vendBankSWIFT-muotoelementti sidottuna model.Payment.CreditorAgent.BICFI-tietolähdekenttään ER-toimintojen suunnitteluohjelmassa](./media/er-quick-start2-derived-format2.png)

14. <span data-ttu-id="65abf-317">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="65abf-317">Select **Save**.</span></span>
15. <span data-ttu-id="65abf-318">Sulje suunnitteluohjelmasivu.</span><span class="sxs-lookup"><span data-stu-id="65abf-318">Close the designer page.</span></span>

### <a name="mark-a-custom-format-as-runnable"></a><a id="MarkFormatRunnable"></a><span data-ttu-id="65abf-319">Merkitse mukautettu muoto suoritettavaksi</span><span class="sxs-lookup"><span data-stu-id="65abf-319">Mark a custom format as runnable</span></span>

<span data-ttu-id="65abf-320">Nyt kun mukautetun muotosi ensimmäinen versio on luotu, ja sen tila on **Luonnos**, voit suorittaa sen testaustarkoituksia varten.</span><span class="sxs-lookup"><span data-stu-id="65abf-320">Now that the first version of your custom format has been created and has a status of **Draft**, you can run it for testing purposes.</span></span> <span data-ttu-id="65abf-321">Raportin suorittamista varten sinun on käsiteltävä toimittajamaksu käyttämällä maksutapaa, joka viittaa mukautettuun ER-muotoosi.</span><span class="sxs-lookup"><span data-stu-id="65abf-321">To run the report, you must process a vendor payment by using the payment method that refers to your custom ER format.</span></span> <span data-ttu-id="65abf-322">Oletuksena kun kutsut ER-muodon sovelluksesta, vain versiot, joiden tila on **Valmis** tai **Jaettu**, otetaan [huomioon](general-electronic-reporting.md#component-versioning).</span><span class="sxs-lookup"><span data-stu-id="65abf-322">By default, when you call an ER format from the application, only versions that have a status of **Completed** or **Shared** are [considered](general-electronic-reporting.md#component-versioning).</span></span> <span data-ttu-id="65abf-323">Tämä käytös auttaa estämään sellaisten ER-muotojen käyttöä, joiden mallit eivät ole valmiit.</span><span class="sxs-lookup"><span data-stu-id="65abf-323">This behavior helps prevent ER formats that have unfinished designs from being used.</span></span> <span data-ttu-id="65abf-324">Testiajoissasi voit kuitenkin pakottaa sovelluksen käyttämään ER-muotosi versiota, jonka tila on **Luonnos**.</span><span class="sxs-lookup"><span data-stu-id="65abf-324">However, for your test runs, you can force the application to use the version of your ER format that has a status of **Draft**.</span></span> <span data-ttu-id="65abf-325">Tällä tavoin voit säätää nykyistä muotoversiota, jos muokkauksia tarvitaan.</span><span class="sxs-lookup"><span data-stu-id="65abf-325">In this way, you can adjust the current format version if any modifications are required.</span></span> <span data-ttu-id="65abf-326">Lisätietoja on kohdassa [Soveltuvuus](electronic-reporting-destinations.md#applicability).</span><span class="sxs-lookup"><span data-stu-id="65abf-326">For more information, see [Applicability](electronic-reporting-destinations.md#applicability).</span></span>

<span data-ttu-id="65abf-327">Käyttääksesi ER-muodon luonnosversiota sinun on merkittävä ER-muoto selkeästi.</span><span class="sxs-lookup"><span data-stu-id="65abf-327">To use the draft version of an ER format, you must explicitly mark the ER format.</span></span>

1. <span data-ttu-id="65abf-328">Valitse **Organisaation hallinto** \> **Sähköinen raportointi** \> **Konfiguraatiot**.</span><span class="sxs-lookup"><span data-stu-id="65abf-328">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="65abf-329">Valitse **Määritykset**-sivun toimintoruudun **Määritykset**-välilehden **Lisämääritykset**-ryhmässä **Käyttäjäparametrit**.</span><span class="sxs-lookup"><span data-stu-id="65abf-329">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3. <span data-ttu-id="65abf-330">**Käyttäjän parametrit** -valintaikkunassa määritä **Suorita asetukset** -valinnaksi **Kyllä**, ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="65abf-330">In the **User parameters** dialog box, set the **Run settings** option to **Yes**, and then select **OK**.</span></span>
4. <span data-ttu-id="65abf-331">Tee tarvittaessa nykyisestä sivusta muokattava valitsemalla **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="65abf-331">Select **Edit** to make the current page editable, as required.</span></span>
5. <span data-ttu-id="65abf-332">Valitse vasemman ruudun konfiguraatiopuussa **BACS (Iso-Britannia, mukautettu)**.</span><span class="sxs-lookup"><span data-stu-id="65abf-332">In the configuration tree in the left pane, select **BACS (UK custom)**.</span></span>
6. <span data-ttu-id="65abf-333">Määritä **Suorita luonnos** -vaihtoehdoksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="65abf-333">Set the **Run Draft** option to **Yes**.</span></span>

    ![Suorita luonnos -vaihtoehto Konfiguroinnit-sivulla](./media/er-quick-start2-derived-format-configuration2.png)

## <a name="process-a-vendor-payment-by-using-the-custom-er-format"></a><a id="ProcessVendorPayment2"></a><span data-ttu-id="65abf-335">Käsittele toimittajamaksu käyttämällä mukautettua ER-muotoa</span><span class="sxs-lookup"><span data-stu-id="65abf-335">Process a vendor payment by using the custom ER format</span></span>

### <a name="set-up-the-electronic-payment-method"></a><a id="ConfigureMethodOfPayment2"></a><span data-ttu-id="65abf-336">Määritä sähköinen maksutapa</span><span class="sxs-lookup"><span data-stu-id="65abf-336">Set up the electronic payment method</span></span>

<span data-ttu-id="65abf-337">Sinun on määritettävä sähköinen maksutapa siten, että mukautettua ER-muotoasi käytetään toimittajamaksujen käsittelyyn.</span><span class="sxs-lookup"><span data-stu-id="65abf-337">You must configure the electronic method of payment so that your custom ER format is used to process vendor payments.</span></span>

1. <span data-ttu-id="65abf-338">Valitse **Ostoreskontra** \> **Maksun asetukset** \> **Maksutavat**.</span><span class="sxs-lookup"><span data-stu-id="65abf-338">Go to **Accounts payable** \> **Payment setup** \> **Methods of payment**.</span></span>
2. <span data-ttu-id="65abf-339">Valitse **Maksutapa - Toimittajat** -sivulla **Sähköinen** maksumenetelmä vasemmasta ruudusta.</span><span class="sxs-lookup"><span data-stu-id="65abf-339">On the **Methods of payment - vendors** page, select the **Electronic** method of payment in the left pane.</span></span>
3. <span data-ttu-id="65abf-340">Valitse **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="65abf-340">Select **Edit**.</span></span>
4. <span data-ttu-id="65abf-341">Määritä **Tiedostomuoto**-pikavälilehdessä **Yleinen sähköinen vientimuoto** -asetukseksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="65abf-341">On the **File format** FastTab, set the **General electronic export format** option to **Yes**.</span></span>
5. <span data-ttu-id="65abf-342">Valitse **Vientimuodon konfigurointi** -kentässä **BACS (Iso-Britannia, mukautettu)** -muotoinen konfiguraatio.</span><span class="sxs-lookup"><span data-stu-id="65abf-342">In the **Export format configuration** field, select the **BACS (UK custom)** format configuration.</span></span>

    ![Maksutapa - Toimittajat -sivu](./media/er-quick-start2-method-of-payment2.png)

6. <span data-ttu-id="65abf-344">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="65abf-344">Select **Save**.</span></span>

### <a name="process-a-vendor-payment"></a><a id="ProcessPayment2"></a><span data-ttu-id="65abf-345">Käsittele toimittajamaksu</span><span class="sxs-lookup"><span data-stu-id="65abf-345">Process a vendor payment</span></span>

1. <span data-ttu-id="65abf-346">Valitse **Ostoreskontra** \> **Maksut** \> **Toimittajan maksukirjauskansio**.</span><span class="sxs-lookup"><span data-stu-id="65abf-346">Go to **Accounts payable** \> **Payments** \> **Vendor payment journal**.</span></span>
2. <span data-ttu-id="65abf-347">Valitse **Toimittajan maksukirjauskansio** -sivulla aiemmin luomasi kirjauskansio.</span><span class="sxs-lookup"><span data-stu-id="65abf-347">On the **Vendor payment journal** page, select the payment journal that you created earlier.</span></span>
3. <span data-ttu-id="65abf-348">Valitse **Rivit**.</span><span class="sxs-lookup"><span data-stu-id="65abf-348">Select **Lines**.</span></span>
4. <span data-ttu-id="65abf-349">Valitse **Toimittajan maksut** -sivulla, ruudukon yläpuolella **Maksun tila** \> **Ei mikään**.</span><span class="sxs-lookup"><span data-stu-id="65abf-349">On the **Vendor payments** page, above the grid, select **Payment status** \> **None**.</span></span>
5. <span data-ttu-id="65abf-350">Valitse **Luo maksu**.</span><span class="sxs-lookup"><span data-stu-id="65abf-350">Select **Generate payment**.</span></span>
6. <span data-ttu-id="65abf-351">Anna seuraavat tiedot **Muodosta maksut** -valintaikkunassa:</span><span class="sxs-lookup"><span data-stu-id="65abf-351">In the **Generate payments** dialog box, enter the following information:</span></span>

    - <span data-ttu-id="65abf-352">Valitse **Maksutapa**-kentässä **Sähköinen**.</span><span class="sxs-lookup"><span data-stu-id="65abf-352">In the **Method of payment** field, select **Electronic**.</span></span>
    - <span data-ttu-id="65abf-353">Valitse **Pankkitili**-kentässä **GBSI OPER**.</span><span class="sxs-lookup"><span data-stu-id="65abf-353">In the **Bank account** field, select **GBSI OPER**.</span></span>

7. <span data-ttu-id="65abf-354">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="65abf-354">Select **OK**.</span></span>
8. <span data-ttu-id="65abf-355">Määritä **Sähköisen raportin parametrit** -valintaikkunassa **Tulosta valvontaraportti** -asetukseksi **Kyllä** ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="65abf-355">In the **Electronic report parameters** dialog box, set the **Print control report** option to **Yes**, and then select **OK**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="65abf-356">Maksutiedoston lisäksi voit luoda vain valvontaraportin.</span><span class="sxs-lookup"><span data-stu-id="65abf-356">In addition to the payment file, you can generate only the control report.</span></span>

9. <span data-ttu-id="65abf-357">Lataa zip-tiedosto ja pura siitä sitten seuraavat tiedostot:</span><span class="sxs-lookup"><span data-stu-id="65abf-357">Download the zip file, and then extract the following files from it:</span></span>

    - <span data-ttu-id="65abf-358">Valvontaraportti Excel-muodossa</span><span class="sxs-lookup"><span data-stu-id="65abf-358">The control report in Excel format</span></span>
    - <span data-ttu-id="65abf-359">Maksutiedosto TXT-muodossa</span><span class="sxs-lookup"><span data-stu-id="65abf-359">The payment file in TXT format</span></span>

        <span data-ttu-id="65abf-360">Huomaa, että mukautetun ER-muotosi rakenteen mukaisesti luodun tiedoston maksurivi [alkaa](#PositionSWIFTCode) nyt SWIFT-koodilla, joka [syötettiin](#DefineSWIFTCode) sen toimittajan pankkitilille, jonka maksu on käsitelty.</span><span class="sxs-lookup"><span data-stu-id="65abf-360">Notice that, in accordance with the structure of your custom ER format, the payment line in the generated file now [starts](#PositionSWIFTCode) with the SWIFT code that was [entered](#DefineSWIFTCode) for the bank account of the vendor whose payment has been processed.</span></span>

        ![Maksutiedosto TXT-muodossa](./media/er-quick-start2-payment-file2.png)

## <a name="import-new-versions-of-the-standard-er-format-configurations"></a><a id="ImportERSolution2"></a><span data-ttu-id="65abf-362">Tuo ER-muodon vakiokonfiguraatioiden uudet versiot</span><span class="sxs-lookup"><span data-stu-id="65abf-362">Import new versions of the standard ER format configurations</span></span>

<span data-ttu-id="65abf-363">Tässä osiossa näkyvää esimerkkiä varten saat ilmoituksen Knowledge Base -artikkelista [KB3763330](https://fix.lcs.dynamics.com/Issue/Details?kb=3182046).</span><span class="sxs-lookup"><span data-stu-id="65abf-363">For the example that is shown in this section, you receive a notification about Knowledge Base article [KB3763330](https://fix.lcs.dynamics.com/Issue/Details?kb=3182046).</span></span> <span data-ttu-id="65abf-364">Tämä ilmoitus kertoo sinulle Microsoftin julkaiseman **BACS (Iso-Britannia)** -ER-muodon uuden version.</span><span class="sxs-lookup"><span data-stu-id="65abf-364">This notification informs you about the new version of the **BACS (UK)** ER format that has been published by Microsoft.</span></span> <span data-ttu-id="65abf-365">Valvontaraportin lisäksi tämä uusi versio antaa käyttäjien luoda maksuehdotusraportin ja osallistumishuomautusraportin, kun toimittajamaksua käsitellään.</span><span class="sxs-lookup"><span data-stu-id="65abf-365">In addition to the control report, this new version lets users generate the payment advice report and the attending note report while a vendor payment is being processed.</span></span> <span data-ttu-id="65abf-366">Haluat alkaa käyttää kyseistä toimintoa.</span><span class="sxs-lookup"><span data-stu-id="65abf-366">You want to start to use that functionality.</span></span>

### <a name="import-new-versions-of-the-standard-er-configurations"></a><a id="ImportERFormat2"></a><span data-ttu-id="65abf-367">Tuo ER-vakiokonfiguraatioiden uudet versiot</span><span class="sxs-lookup"><span data-stu-id="65abf-367">Import new versions of the standard ER configurations</span></span>

<span data-ttu-id="65abf-368">Jos haluat lisätä ER-konfiguraatioiden uusia versioita nykyiseen Finance-esiintymään, sinun on tuotava ne ER-[säilöstä](general-electronic-reporting.md#Repository), jonka olet määrittänyt.</span><span class="sxs-lookup"><span data-stu-id="65abf-368">To add new versions of the ER configurations to the current Finance instance, you must import them from the ER [repository](general-electronic-reporting.md#Repository) that you've configured.</span></span>

1. <span data-ttu-id="65abf-369">Valitse **Organisaation hallinto** \> **Työtilat** \> **Sähköinen raportointi**.</span><span class="sxs-lookup"><span data-stu-id="65abf-369">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="65abf-370">Valitse **Lokalisoinnin konfiguraatiot**-sivun **Konfiguraation lähteet** -osassa **Microsoft**-ruutu ja valitse sitten **Säilöt** nähdäksesi luettelon Microsoft-toimittajan säilöistä.</span><span class="sxs-lookup"><span data-stu-id="65abf-370">On the **Localization configurations** page, in the **Configuration providers** section, select the **Microsoft** tile, and then select **Repositories** to view the list of repositories for the Microsoft provider.</span></span>
3. <span data-ttu-id="65abf-371">Valitse **Konfiguraatiosäilöt**-sivun ruudukossa oleva säilö, jonka tyyppi on **Yleinen** ja valitse sitten **Avaa**.</span><span class="sxs-lookup"><span data-stu-id="65abf-371">On the **Configuration repositories** page, select the repository of the **Global** type, and then select **Open**.</span></span> <span data-ttu-id="65abf-372">Jos sinulta pyydetään valtuutusta Regulatory Configuration Service -palveluun yhdistämiseen, noudata valtuutusohjeita.</span><span class="sxs-lookup"><span data-stu-id="65abf-372">If you're prompted for authorization to connect to Regulatory Configuration Service, follow the authorization instructions.</span></span>
4. <span data-ttu-id="65abf-373">Valitse **Konfiguraatiosäilö**-sivun vasemmassa ruudussa olevasta konfiguraatiopuusta **BACS (Iso-Britannia)** -muotoinen konfiguraatio.</span><span class="sxs-lookup"><span data-stu-id="65abf-373">On the **Configuration repository** page, in the configuration tree in the left pane, select the **BACS (UK)** format configuration.</span></span>
5. <span data-ttu-id="65abf-374">Valitse **Versiot**-pikavälilehdestä valitun ER-muodon konfiguraation versio **3.3**.</span><span class="sxs-lookup"><span data-stu-id="65abf-374">On the **Versions** FastTab, select version **3.3** of the selected ER format configuration.</span></span>
6. <span data-ttu-id="65abf-375">Lataa valittu versio yleisestä säilöpalvelusta nykyiseen Finance-esiintymään valitsemalla **Tuo**.</span><span class="sxs-lookup"><span data-stu-id="65abf-375">Select **Import** to download the selected version from the Global repository to the current Finance instance.</span></span>

![Konfiguraatiosäilön sivu](./media/er-quick-start2-import-solution2.png)

> [!TIP]
> <span data-ttu-id="65abf-377">Jos sinulla on ongelmia [yleiseen säilöön](er-download-configurations-global-repo.md) pääsyssä, voit [ladata konfiguraatiot](download-electronic-reporting-configuration-lcs.md) sen sijaan LCS-palvelusta.</span><span class="sxs-lookup"><span data-stu-id="65abf-377">If you have trouble accessing the [Global repository](er-download-configurations-global-repo.md), you can [download configurations](download-electronic-reporting-configuration-lcs.md) from LCS instead.</span></span>

### <a name="review-the-imported-er-format-configurations"></a><a id="ReviewImportedERFormat"></a><span data-ttu-id="65abf-378">Tarkista tuodut ER-muodon konfiguraatiot</span><span class="sxs-lookup"><span data-stu-id="65abf-378">Review the imported ER format configurations</span></span>

1. <span data-ttu-id="65abf-379">Valitse **Organisaation hallinto** \> **Työtilat** \> **Sähköinen raportointi**.</span><span class="sxs-lookup"><span data-stu-id="65abf-379">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="65abf-380">Valitse **Lokalisointimääritykset**-sivun **Konfiguroinnit**-osassa **Raportointimääritykset**-ruutu.</span><span class="sxs-lookup"><span data-stu-id="65abf-380">On the **Localization configurations** page, in the **Configurations** section, select the **Reporting configurations** tile.</span></span>
3. <span data-ttu-id="65abf-381">Valitse **Konfiguraatiot**-sivun konfiguraatiopuu vasemmasta ruudusta, laajenna **Maksumalli** ja valitse sitten **BACS (Iso-Britannia)**.</span><span class="sxs-lookup"><span data-stu-id="65abf-381">On the **Configurations** page, in the configuration tree in the left pane, expand **Payment model**, and then select **BACS (UK)**.</span></span>
4. <span data-ttu-id="65abf-382">Valitse **Versiot**-pikavälilehdessä versio **3.3**.</span><span class="sxs-lookup"><span data-stu-id="65abf-382">On the **Versions** FastTab, select version **3.3**.</span></span>
5. <span data-ttu-id="65abf-383">Valitse **Suunnittelu**.</span><span class="sxs-lookup"><span data-stu-id="65abf-383">Select **Designer**.</span></span>
6. <span data-ttu-id="65abf-384">Laajenna **Muodon suunnittelija** -sivulla **BACSReportsFolder**-muotoelementti.</span><span class="sxs-lookup"><span data-stu-id="65abf-384">On the **Format designer** page, expand the **BACSReportsFolder** format element.</span></span>
7.  <span data-ttu-id="65abf-385">Huomaa, että versio 3.3 sisältää **PaymentAdviceReport**-muotoelementin, jota käytetään maksuehdotusraportin luomiseen, kun toimittajamaksua käsitellään.</span><span class="sxs-lookup"><span data-stu-id="65abf-385">Notice that version 3.3 contains the **PaymentAdviceReport** format element that is used to generate a payment advice report when a vendor payment is processed.</span></span>

    ![PaymentAdviceReport-muotoelementti ER-toimintojen suunnitteluohjelmassa](./media/er-quick-start2-imported-solution2.png)

8. <span data-ttu-id="65abf-387">Sulje suunnitteluohjelmasivu.</span><span class="sxs-lookup"><span data-stu-id="65abf-387">Close the designer page.</span></span>

## <a name="adopt-the-changes-in-the-new-version-of-an-imported-format-in-a-custom-format"></a><a id="AdoptNewBaseVersion"></a><span data-ttu-id="65abf-388">Ota uudessa versiossa käyttöön tuodun muodon muutokset mukautetussa muodossa</span><span class="sxs-lookup"><span data-stu-id="65abf-388">Adopt the changes in the new version of an imported format in a custom format</span></span>

### <a name="complete-the-current-draft-version-of-a-custom-format"></a><a id="CompleteDerivedFormat"></a><span data-ttu-id="65abf-389">Viimeistele mukautetun muodon nykyinen luonnosversio</span><span class="sxs-lookup"><span data-stu-id="65abf-389">Complete the current draft version of a custom format</span></span>

<span data-ttu-id="65abf-390">Jos haluat säilyttää mukautetun muotosi nykyisen tilan, viimeistele luonnosversio 1.1.1 muuttamalla sen tila **Luonnos** tilaksi **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="65abf-390">If you want to keep the current state of your custom format, complete the draft version 1.1.1 by changing its status from **Draft** to **Completed**.</span></span>

1. <span data-ttu-id="65abf-391">Valitse **Organisaation hallinto** \> **Työtilat** \> **Sähköinen raportointi**.</span><span class="sxs-lookup"><span data-stu-id="65abf-391">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="65abf-392">Valitse **Lokalisointimääritykset**-sivun **Konfiguroinnit**-osassa **Raportointimääritykset**-ruutu.</span><span class="sxs-lookup"><span data-stu-id="65abf-392">On the **Localization configurations** page, in the **Configurations** section, select the **Reporting configurations** tile.</span></span>
3. <span data-ttu-id="65abf-393">Valitse **Konfiguraatiot**-sivun konfiguraatiopuu vasemmasta ruudusta, laajenna **Maksumalli**, laajenna **BACS (Iso-Britannia)** ja valitse sitten **BACS (Iso-Britannia, mukautettu)**.</span><span class="sxs-lookup"><span data-stu-id="65abf-393">On the **Configurations** page, in the configuration tree in the left pane, expand **Payment model**, expand **BACS (UK)**, and then select **BACS (UK custom)**.</span></span>
4. <span data-ttu-id="65abf-394">Valitse **Versiot**-pikavälilehdessä **Muuta tila** \> **Valmis** ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="65abf-394">On the **Versions** FastTab, select **Change status** \> **Complete**, and then select **OK**.</span></span>

<span data-ttu-id="65abf-395">Version 1.1.1 tila muuttuu tilasta **Luonnos** tilaksi **Valmis** ja versio muuttuu vain luku -tilaan.</span><span class="sxs-lookup"><span data-stu-id="65abf-395">The status of version 1.1.1 is changed from **Draft** to **Completed**, and the version becomes read-only.</span></span> <span data-ttu-id="65abf-396">Uusi muokattava versio 1.1.2 on lisätty, ja sen tila on **Luonnos**.</span><span class="sxs-lookup"><span data-stu-id="65abf-396">A new editable version, 1.1.2, has been added and has a status of **Draft**.</span></span> <span data-ttu-id="65abf-397">Voit käyttää tätä versiota tehdäksesi lisämuutoksia mukautettuun ER-muotoosi.</span><span class="sxs-lookup"><span data-stu-id="65abf-397">You can use this version to make further changes in your custom ER format.</span></span>

### <a name="rebase-a-custom-format-to-a-new-base-version"></a><a id="RebaseDerivedFormat"></a><span data-ttu-id="65abf-398">Pohjusta mukautettu muoto uuteen perusversioon</span><span class="sxs-lookup"><span data-stu-id="65abf-398">Rebase a custom format to a new base version</span></span>

<span data-ttu-id="65abf-399">Jos haluat alkaa käyttää **BACS (Iso-Britannia)** -muodon version 3.3 uutta toimintoa mukauttamisessasi, sinun on muutettava mukautetun **BACS (Iso-Britannia, mukautettu)** -konfiguraation peruskonfiguraatioversiota.</span><span class="sxs-lookup"><span data-stu-id="65abf-399">To start to use the new functionality of version 3.3 of the **BACS (UK)** format in your customization, you must change the base configuration version for the custom configuration, **BACS (UK custom)**.</span></span> <span data-ttu-id="65abf-400">Tätä prosessia kutsutaan [pohjustamiseksi](general-electronic-reporting.md#upgrading-a-format-selecting-a-new-version-of-base-format-rebase).</span><span class="sxs-lookup"><span data-stu-id="65abf-400">This process is known as [rebasing](general-electronic-reporting.md#upgrading-a-format-selecting-a-new-version-of-base-format-rebase).</span></span> <span data-ttu-id="65abf-401">Käytä **BACS (Iso-Britannia)** -version 1.1 sijaan versiota 3.3.</span><span class="sxs-lookup"><span data-stu-id="65abf-401">Instead of version 1.1 of **BACS (UK)**, use version 3.3.</span></span>

1. <span data-ttu-id="65abf-402">Valitse **Organisaation hallinto** \> **Sähköinen raportointi** \> **Konfiguraatiot**.</span><span class="sxs-lookup"><span data-stu-id="65abf-402">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="65abf-403">Valitse **Konfiguraatiot**-sivun konfiguraatiopuu vasemmasta ruudusta, laajenna **Maksumalli** ja valitse sitten **BACS (Iso-Britannia, mukautettu)**.</span><span class="sxs-lookup"><span data-stu-id="65abf-403">On the **Configurations** page, in the configuration tree in the left pane, expand **Payment model**, and then select **BACS (UK custom)**.</span></span>
3. <span data-ttu-id="65abf-404">Valitse **Versiot**-pikavälilehdessä versio **1.1.2** ja valitse sitten **Pohjusta**.</span><span class="sxs-lookup"><span data-stu-id="65abf-404">On the **Versions** FastTab, select version **1.1.2**, and then select **Rebase**.</span></span>
4. <span data-ttu-id="65abf-405">Valitse **Pohjusta**-valintaikkunan **Kohdeversio**-kentässä peruskonfiguraation versio **3.3** käyttääksesi sitä uutena perusteena ja käyttääksesi sitä konfiguraation päivittämiseen.</span><span class="sxs-lookup"><span data-stu-id="65abf-405">In the **Rebase** dialog box, in the **Target version** field, select version **3.3** of the base configuration to apply it as the new base and use it to update the configuration.</span></span>

    ![Pohjusta-valintaikkuna](./media/er-quick-start2-rebase1.png)

5. <span data-ttu-id="65abf-407">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="65abf-407">Select **OK**.</span></span>
6. <span data-ttu-id="65abf-408">Huomaa, että luonnosversion numero on muuttunut numerosta **1.1.2** numeroksi **3.3.2** heijastamaan perusversion muutosta.</span><span class="sxs-lookup"><span data-stu-id="65abf-408">Notice that the number of the draft version has been changed from **1.1.2** to **3.3.2** to reflect the change in the base version.</span></span>

    <span data-ttu-id="65abf-409">Kun mukautettu versio ja uusi perusversio yhdistetään, saatetaan havaita joitakin konflikteja, jotka johtuvat muodon muutoksista, joita ei voida yhdistää automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="65abf-409">When the custom version and a new base version are merged, some conflicts might be discovered because of format changes that can't be merged automatically.</span></span>

    ![Uudelleenpohjustettu konfiguraatio, jossa on konflikteja, Konfiguraatiot-sivulla](./media/er-quick-start2-rebase2.png)

    <span data-ttu-id="65abf-411">Jos konflikteja havaitaan, ne on ratkaistava manuaalisesti muodon suunnitteluohjelmassa.</span><span class="sxs-lookup"><span data-stu-id="65abf-411">If conflicts are discovered, they must be manually resolved in the format designer.</span></span>

7. <span data-ttu-id="65abf-412">Valitse **Versiot**-pikavälilehdessä versio **3.3.2**.</span><span class="sxs-lookup"><span data-stu-id="65abf-412">On the **Versions** FastTab, select version **3.3.2**.</span></span>
8. <span data-ttu-id="65abf-413">Valitse **Suunnittelu**.</span><span class="sxs-lookup"><span data-stu-id="65abf-413">Select **Designer**.</span></span>
9. <span data-ttu-id="65abf-414">Valitse **Muodon suunnittelija** -sivun **Tiedot**-pikavälilehdessä uudelleenpohjustettu konfliktitietue ja valitse sitten **Kohdista perusarvo**.</span><span class="sxs-lookup"><span data-stu-id="65abf-414">On the **Format designer** page, on the **Details** FastTab, select a rebase conflict record, and then select **Apply base value**.</span></span>

    ![Uudelleenpohjustettu konfliktitietue ER-toimintojen suunnitteluohjelmassa](./media/er-quick-start2-rebase3.png)

10. <span data-ttu-id="65abf-416">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="65abf-416">Select **Save**.</span></span>

    <span data-ttu-id="65abf-417">Uudelleenpohjustetun konfliktitietueen ei pitäisi enää näkyä **Tiedot**-pikavälilehdessä.</span><span class="sxs-lookup"><span data-stu-id="65abf-417">The rebase conflict record should no longer appear on the **Details** FastTab.</span></span>

    ![Konflikti ratkaistu ER-toimintojen suunnitteluohjelmassa](./media/er-quick-start2-rebase4.png)

    > [!NOTE]
    > <span data-ttu-id="65abf-419">Ratkaisit konfliktin vahvistamalla, että perusmallin versiota 3 pitää käyttää tässä ER-muodossa.</span><span class="sxs-lookup"><span data-stu-id="65abf-419">You resolved the conflict by confirming that version 3 of the base model must be used in this ER format.</span></span>

11. <span data-ttu-id="65abf-420">Laajenna **BACSReportsFolder** \> **-tiedosto** \> **tapahtumat** \> **tapahtuma**.</span><span class="sxs-lookup"><span data-stu-id="65abf-420">Expand **BACSReportsFolder** \> **file** \> **transactions** \> **transaction**.</span></span>
12. <span data-ttu-id="65abf-421">Huomaa **Kartoitus**-välilehdessä, että mukautetun ER-muotosi versio 3.3.2 sisältää sekä mukautetun (**vendBankSWIFT**-muotoelementti ja sen sidonta) että uuden Microsoftin tarjoaman ER-muodon version 3.3 toiminnon (**PaymentAdviceReport**-muotoelementti yhdessä sen sisäkkäisten elementtien ja määritettyjen sidontojen kanssa).</span><span class="sxs-lookup"><span data-stu-id="65abf-421">On the **Mapping** tab, notice that version 3.3.2 of your custom ER format contains both your customization (the **vendBankSWIFT** format element and its binding) and the new functionality of version 3.3 of the base ER format that was provided by Microsoft (the **PaymentAdviceReport** format element together with its nested elements and configured bindings).</span></span> <span data-ttu-id="65abf-422">Vain muutamalla hiiren napsautuksella olet ottanut uuden perusversion muokkaukset käyttöön yhdistämällä ne mukautuksesi kanssa.</span><span class="sxs-lookup"><span data-stu-id="65abf-422">In just a few mouse clicks, you adopted the modifications of a new base version by merging them with your customization.</span></span>

    ![Yhdistetty muoto ER-toimintojen suunnitteluohjelmassa](./media/er-quick-start2-rebase5.png)

13. <span data-ttu-id="65abf-424">Sulje suunnitteluohjelmasivu.</span><span class="sxs-lookup"><span data-stu-id="65abf-424">Close the designer page.</span></span>

> [!NOTE]
> <span data-ttu-id="65abf-425">Uudelleenpohjustustoimintoa ei voi perua.</span><span class="sxs-lookup"><span data-stu-id="65abf-425">The rebase action is reversible.</span></span> <span data-ttu-id="65abf-426">Voit peruuttaa tämän uudelleenpohjustuksen valitsemalla version **1.1.1** **BACS (Iso-Britannia, mukautettu)** -muodosta **Versiot**-pikavälilehdessä ja valitsemalla sitten **Nouda tämä versio**.</span><span class="sxs-lookup"><span data-stu-id="65abf-426">To cancel this rebase, select version **1.1.1** of the **BACS (UK custom)** format on the **Versions** FastTab, and then select **Get this version**.</span></span> <span data-ttu-id="65abf-427">Versio 3.3.2 saa sitten uuden numeron 1.1.2 ja luonnosversion 1.1.2 sisältö vastaa version 1.1.1 sisältöä.</span><span class="sxs-lookup"><span data-stu-id="65abf-427">Version 3.3.2 will then be renumbered 1.1.2, and the content of draft version 1.1.2 will match the content of version 1.1.1.</span></span>

### <a name="process-a-vendor-payment-by-using-a-rebased-er-format"></a><a id="ProcessPayment3"></a><span data-ttu-id="65abf-428">Käsittele toimittajamaksu käyttämällä pohjustettua ER-muotoa</span><span class="sxs-lookup"><span data-stu-id="65abf-428">Process a vendor payment by using a rebased ER format</span></span>

1. <span data-ttu-id="65abf-429">Valitse **Ostoreskontra** \> **Maksut** \> **Toimittajan maksukirjauskansio**.</span><span class="sxs-lookup"><span data-stu-id="65abf-429">Go to **Accounts payable** \> **Payments** \> **Vendor payment journal**.</span></span>
2. <span data-ttu-id="65abf-430">Valitse **Toimittajan maksukirjauskansio** -sivulla aiemmin luomasi kirjauskansio.</span><span class="sxs-lookup"><span data-stu-id="65abf-430">On the **Vendor payment journal** page, select the payment journal that you created earlier.</span></span>
3. <span data-ttu-id="65abf-431">Valitse **Rivit**.</span><span class="sxs-lookup"><span data-stu-id="65abf-431">Select **Lines**.</span></span>
4. <span data-ttu-id="65abf-432">Valitse **Toimittajan maksut** -sivulla, ruudukon yläpuolella **Maksun tila** \> **Ei mikään**.</span><span class="sxs-lookup"><span data-stu-id="65abf-432">On the **Vendor payments** page, above the grid, select **Payment status** \> **None**.</span></span>
5. <span data-ttu-id="65abf-433">Valitse **Luo maksu**.</span><span class="sxs-lookup"><span data-stu-id="65abf-433">Select **Generate payment**.</span></span>
6. <span data-ttu-id="65abf-434">Anna seuraavat tiedot **Muodosta maksut** -valintaikkunassa:</span><span class="sxs-lookup"><span data-stu-id="65abf-434">In the **Generate payments** dialog box, enter the following information:</span></span>

    - <span data-ttu-id="65abf-435">Valitse **Maksutapa**-kentässä **Sähköinen**.</span><span class="sxs-lookup"><span data-stu-id="65abf-435">In the **Method of payment** field, select **Electronic**.</span></span>
    - <span data-ttu-id="65abf-436">Valitse **Pankkitili**-kentässä **GBSI OPER**.</span><span class="sxs-lookup"><span data-stu-id="65abf-436">In the **Bank account** field, select **GBSI OPER**.</span></span>

7. <span data-ttu-id="65abf-437">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="65abf-437">Select **OK**.</span></span>
8. <span data-ttu-id="65abf-438">Anna seuraavat tiedot **Sähköisen raportin parametrit** -valintaikkunassa:</span><span class="sxs-lookup"><span data-stu-id="65abf-438">In the **Electronic report parameters** dialog box, enter the following information:</span></span>

    - <span data-ttu-id="65abf-439">Määritä **Tulosta valvontaraportti** -asetukseksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="65abf-439">Set the **Print control report** option to **Yes**.</span></span>
    - <span data-ttu-id="65abf-440">Määritä **Tulosta maksuilmoitus** -asetukseksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="65abf-440">Set the **Print payment advice** option to **Yes**.</span></span>

    ![Sähköisen raportin parametrit -valintaikkuna](./media/er-quick-start2-payment-dialog2.png)

    > [!NOTE]
    > <span data-ttu-id="65abf-442">Maksutiedoston lisäksi voit nyt luoda sekä valvontaraportin että maksuehdotusraportin.</span><span class="sxs-lookup"><span data-stu-id="65abf-442">In addition to the payment file, you can now generate both the control report and the payment advice report.</span></span>

9. <span data-ttu-id="65abf-443">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="65abf-443">Select **OK**.</span></span>
10. <span data-ttu-id="65abf-444">Lataa zip-tiedosto ja pura siitä sitten seuraavat tiedostot:</span><span class="sxs-lookup"><span data-stu-id="65abf-444">Download the zip file, and then extract the following files from it:</span></span>

    - <span data-ttu-id="65abf-445">Valvontaraportti Excel-muodossa</span><span class="sxs-lookup"><span data-stu-id="65abf-445">The control report in Excel format</span></span>
    - <span data-ttu-id="65abf-446">Maksuehdotusraportti Excel-muodossa</span><span class="sxs-lookup"><span data-stu-id="65abf-446">The payment advice report in Excel format</span></span>

        ![Maksuehdotusraportti Excel-muodossa](./media/er-quick-start2-payment-advice-report.png)

    - <span data-ttu-id="65abf-448">Maksutiedosto TXT-muodossa</span><span class="sxs-lookup"><span data-stu-id="65abf-448">The payment file in TXT format</span></span>

        <span data-ttu-id="65abf-449">Huomaa, että luodun tiedoston maksurivi alkaa SWIFT-koodilla, joka syötettiin sen toimittajan pankkitilille, jonka maksu on käsitelty.</span><span class="sxs-lookup"><span data-stu-id="65abf-449">Notice that the payment line in the generated file starts  with the SWIFT code that was entered for the bank account of a vendor whose payment has been processed.</span></span>

        ![Maksutiedosto TXT-muodossa](./media/er-quick-start2-payment-file3.png)

## <a name="additional-resources"></a><a id="References"></a><span data-ttu-id="65abf-451">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="65abf-451">Additional resources</span></span>

- [<span data-ttu-id="65abf-452">Sähköisen raportoinnin yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="65abf-452">Electronic Reporting overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="65abf-453">ER-konfiguraatioiden lataaminen Lifecycle Services -palvelusta</span><span class="sxs-lookup"><span data-stu-id="65abf-453">Download ER configurations from Lifecycle Services</span></span>](download-electronic-reporting-configuration-lcs.md)
- [<span data-ttu-id="65abf-454">Lataa ER-konfiguraatiot konfigurointipalvelun yleisestä varastosta</span><span class="sxs-lookup"><span data-stu-id="65abf-454">Download ER configurations from Global repository of Configuration service</span></span>](er-download-configurations-global-repo.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]