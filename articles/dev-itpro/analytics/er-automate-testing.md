---
title: Testauksen automatisointi sähköisen raportoinnin avulla
description: Tässä ohjeaiheessa selitetään, miten sähköisen raportointi- eli ER-kehyksen perustoiminnolla voi automatisoida Microsoft Dynamics 365 for Finance and Operationsin sähköistä raportointia käyttävien toimintojen testauksen.
author: NickSelin
manager: AnnBe
ms.date: 07/02/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, ERFormatBaselineTable, ERFormatMappingRunLogTable, ERParameters
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.openlocfilehash: 7d21bff6e7d5e8f206a0495408b75c0760a6f80f
ms.sourcegitcommit: 48004c98b16dcd93a7b2568322e058c4b3ff02d3
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/03/2019
ms.locfileid: "1726724"
---
# <a name="automate-testing-with-electronic-reporting"></a><span data-ttu-id="37974-103">Testauksen automatisointi sähköisen raportoinnin avulla</span><span class="sxs-lookup"><span data-stu-id="37974-103">Automate testing with Electronic reporting</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="37974-104">Tässä ohjeaiheessa selitetään, miten sähköisen raportointi- eli ER-kehyksellä automatisoidaan joidenkin Microsoft Dynamics 365 for Finance and Operationsin toimintojen testaus.</span><span class="sxs-lookup"><span data-stu-id="37974-104">This topic explains how you can use the Electronic reporting (ER) framework to automate testing of some functionality in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="37974-105">Ohjeaiheen esimerkin avulla näytetään, miten toimittajan maksujen käsittely automatisoidaan.</span><span class="sxs-lookup"><span data-stu-id="37974-105">The example in this topic shows how to automate the testing of vendor payment processing.</span></span>

<span data-ttu-id="37974-106">Finance and Operations luo ER-kehyksen avulla maksutiedostot ja vastaavat asiakirjat toimittajan maksujen käsittelyn aikana.</span><span class="sxs-lookup"><span data-stu-id="37974-106">Finance and Operations uses the ER framework to generate payment files and corresponding documents during vendor payment processing.</span></span> <span data-ttu-id="37974-107">ER-kehys sisältää tietomallin, mallien yhdistämismääritykset ja muoto-osia, jotka tukevat eri maksutyyppien maksujen käsittelyä ja eri muotoisten asiakirjojen luontia.</span><span class="sxs-lookup"><span data-stu-id="37974-107">The ER framework consists of a data model, model mappings, and format components that support payment processing for different payment types and the generation of documents in different formats.</span></span> <span data-ttu-id="37974-108">Nämä osat voi ladata Microsoft Dynamics Lifecycle Servicesistä (LCS) ja tuoda Finance and Operations -esiintymään.</span><span class="sxs-lookup"><span data-stu-id="37974-108">These components can be downloaded from Microsoft Dynamics Lifecycle Services (LCS) and imported into the Finance and Operations instance.</span></span>

<span data-ttu-id="37974-109">Voit myös mukauttaa kutakin Microsoft-osaa ja käyttää sitä oman mukautetun osan perustana.</span><span class="sxs-lookup"><span data-stu-id="37974-109">You also can customize each Microsoft component and use it as the basis of your own custom component.</span></span> <span data-ttu-id="37974-110">Luomalla mukautetun version voit tehdä tiettyjä tarpeita tukevia muutoksia.</span><span class="sxs-lookup"><span data-stu-id="37974-110">By creating a custom version, you can make changes that support specific requirements.</span></span> <span data-ttu-id="37974-111">Voit esimerkiksi säätää ER-tietomallin ja ER-mallin yhdistämismäärityksen käyttämään asiakaskohtaista sovellustietoa tai voit muuttaa ER-muodon muokkaamaan luodun asiakirjan asettelua.</span><span class="sxs-lookup"><span data-stu-id="37974-111">For example, you can adjust the ER data model and ER model mapping to access customer-specific application data, or you can change an ER format to modify the layout of a generated document.</span></span>

<span data-ttu-id="37974-112">Voit käyttää mukautettuja ER-muotoja Finance and Operations -esiintymässä toimittajan maksuja luovien maksutiedostojen käsittelyyn. Voit käsitellä niillä myös tarkistusraportteja.</span><span class="sxs-lookup"><span data-stu-id="37974-112">You can use customized ER formats in your Finance and Operations instance to process payment files that generate vendor payments and also to process control reports.</span></span> <span data-ttu-id="37974-113">Versiointia tuetaan ER-osissa.</span><span class="sxs-lookup"><span data-stu-id="37974-113">Versioning is supported in ER components.</span></span> <span data-ttu-id="37974-114">Microsoft voikin tämän vuoksi toimittaa toimittajan maksujen käsittelyn ER-ratkaisujen päivitetyt versiot, ja voit automaattisesti yhdistää päivitetyn version mukautettuun osaa pohjustamalla sen.</span><span class="sxs-lookup"><span data-stu-id="37974-114">Therefore, Microsoft can provide updated versions of ER solutions for vendor payment processing, and you can automatically merge the updated version with your customized component by rebasing it.</span></span> <span data-ttu-id="37974-115">Pohjustettu versio on kuitenkin testattava, jotta voidaan varmistaa, että toimii odotetulla tavalla.</span><span class="sxs-lookup"><span data-stu-id="37974-115">However, you must test the rebased version to make sure that it works as you expect.</span></span>

<span data-ttu-id="37974-116">ER-tietomallit ja ER-mallin yhdistämismääritykset ovat yleisiä useissa ER-muodoissa, joilla käsitellään eri tyyppisiä maksuja ja luodaan maa- tai aluekohtaisia maksuasiakirjoja.</span><span class="sxs-lookup"><span data-stu-id="37974-116">ER data models and ER model mappings are common for many ER formats that are used to process payments of different types and to generate country/region-specific payment documents.</span></span> <span data-ttu-id="37974-117">Tämän vuoksi käyttäjän hyväksynnän tai integroinnin testauksen automatisointi on erittäin toivottavaa, jolloin testaus voidaan tehdä automaattisesti useissa Finance and Operations -yrityksissä esimerkiksi siten, että kunkin kohdeyrityksen maa- tai aluekonteksti otetaan huomioon ja käytetään eri tietojoukkoja.</span><span class="sxs-lookup"><span data-stu-id="37974-117">Therefore, it's highly desirable to automate user acceptance and integration testing so that it's automatically done in multiple Finance and Operations companies but considers the country/region context of each target company, uses different datasets, and so on.</span></span>

<span data-ttu-id="37974-118">Lisätietoja konfiguraation lähteestä vastaanotettuun muotoon perustuvan muodon mukautetun version luomisesta on kohteessa [ER Muodon päivittäminen ottamalla käyttöön kyseisen muodon uusi perusversio](./tasks/er-upgrade-format.md).</span><span class="sxs-lookup"><span data-stu-id="37974-118">For more information about how to create a custom version of a format that is based on the format that you received from a configuration provider, see [ER Upgrade your format by adopting a new, base version of that format](./tasks/er-upgrade-format.md).</span></span>

## <a name="key-concepts"></a><span data-ttu-id="37974-119">Avainkäsitteet</span><span class="sxs-lookup"><span data-stu-id="37974-119">Key concepts</span></span>

<span data-ttu-id="37974-120">Tehotoimintokäyttäjät voivat laatia käyttäjän hyväksyntä- ja integrointitestauksen lähdekoodia kirjoittamatta.</span><span class="sxs-lookup"><span data-stu-id="37974-120">Functional power users can author user acceptance and integration testing without having to write source code.</span></span>

- <span data-ttu-id="37974-121">Vertaa luotuja asiakirjoja pääversioihin ER-perustoiminnolla.</span><span class="sxs-lookup"><span data-stu-id="37974-121">Use the ER baseline feature to compare generated documents to master copies.</span></span> <span data-ttu-id="37974-122">Lisätietoja on kohdassa [Luotujen raporttitulosten seuraaminen ja vertaaminen perusarvoihin](er-trace-reports-compare-baseline.md)</span><span class="sxs-lookup"><span data-stu-id="37974-122">For more information, see [Trace generated report results and compare them with baseline values](er-trace-reports-compare-baseline.md).</span></span>
- <span data-ttu-id="37974-123">Tallenna testitapauksen tehtävän tallennustoiminnolla ja sisällytä perusarviointi.</span><span class="sxs-lookup"><span data-stu-id="37974-123">Use Task recorder to record test cases, and include baseline assessment.</span></span> <span data-ttu-id="37974-124">Lisätietoja on kohdassa [Tehtävän tallennustoiminto](../user-interface/task-recorder.md).</span><span class="sxs-lookup"><span data-stu-id="37974-124">For more information, see [Task recorder](../user-interface/task-recorder.md).</span></span>
- <span data-ttu-id="37974-125">Ryhmitä tarvittavien testiskenaarioiden testitapaukset.</span><span class="sxs-lookup"><span data-stu-id="37974-125">Group test cases for required test scenarios.</span></span> <span data-ttu-id="37974-126">Lisätietoja on kohdassa [Käyttäjän hyväksyntätestauskirjastojen luominen tehtävätallenteiden ja BPM-määritysten avulla](../lifecycle-services/using-task-guides-and-bpm-to-create-user-acceptance-tests.md).</span><span class="sxs-lookup"><span data-stu-id="37974-126">For more information, see [Create user acceptance test libraries by using task recordings and BPM](../lifecycle-services/using-task-guides-and-bpm-to-create-user-acceptance-tests.md).</span></span>

    - <span data-ttu-id="37974-127">Muodosta käyttäjän hyväksyntätestien kirjastoja LCS:n liiketoimintaprosessien mallintajalla (BPM).</span><span class="sxs-lookup"><span data-stu-id="37974-127">Use Business process modeler (BPM) in LCS to make libraries for user acceptance tests.</span></span>
    - <span data-ttu-id="37974-128">Luo Microsoft Azure DevOps Servicesissä (Azure DevOps) testisuunnitelma ja testisarjoja BPM-testikirjastojen avulla.</span><span class="sxs-lookup"><span data-stu-id="37974-128">Use BPM test libraries to create a test plan and test suites in Microsoft Azure DevOps Services (Azure DevOps).</span></span>

<span data-ttu-id="37974-129">Tehotoimintakäyttäjät voivat suorittaa käyttäjän hyväksyntä- ja integrointitestejä.</span><span class="sxs-lookup"><span data-stu-id="37974-129">Functional power users can run user acceptance and integration tests.</span></span>

- <span data-ttu-id="37974-130">Suorita toivotun testisarjan testitapaukset Regression Suite Automation Tool (RSAT) -työkalulla.</span><span class="sxs-lookup"><span data-stu-id="37974-130">Use Regression suite automation tool (RSAT) to run test cases of the desired test suite.</span></span>
- <span data-ttu-id="37974-131">Raportoi testauksen tulokset Azure DevOpsiin ja tutustu kyseisiin tuloksiin tässä palvelussa.</span><span class="sxs-lookup"><span data-stu-id="37974-131">Report the results of the testing to Azure DevOps, and use this service to investigate those results.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="37974-132">Edellytykset</span><span class="sxs-lookup"><span data-stu-id="37974-132">Prerequisites</span></span>

<span data-ttu-id="37974-133">Ennen kuin voit suorittaa tämän ohjeaiheen tehtäviä, seuraavien edellytysten on toteuduttava:</span><span class="sxs-lookup"><span data-stu-id="37974-133">Before you can complete the tasks in this topic, you must complete the following prerequisites:</span></span>

- <span data-ttu-id="37974-134">Ota käyttöön testauksen automatisointia tukeva Finance and Operations -topologia.</span><span class="sxs-lookup"><span data-stu-id="37974-134">Deploy a Finance and Operations topology that supports test automation.</span></span> <span data-ttu-id="37974-135">Sinulla on oltava tämän topologian Finance and Operations -esiintymän **Järjestelmänvalvoja**-rooli.</span><span class="sxs-lookup"><span data-stu-id="37974-135">You must have access to the Finance and Operations instance of this topology for the **System administrator** role.</span></span> <span data-ttu-id="37974-136">Topologian on sisällettävä tässä esimerkissä käytettävät Finance and Operationsin demotiedot.</span><span class="sxs-lookup"><span data-stu-id="37974-136">This topology must contain the Finance and Operations demo data that will be used in this example.</span></span> <span data-ttu-id="37974-137">Lisätietoja on kohdassa [Jatkuvaa koonnin ja testauksen automaatiota tukevien topologioiden käyttöönotto](../perf-test/continuous-build-test-automation.md).</span><span class="sxs-lookup"><span data-stu-id="37974-137">For more information, see [Deploy topologies that support continuous build and test automation](../perf-test/continuous-build-test-automation.md).</span></span>
- <span data-ttu-id="37974-138">Voit suorittaa käyttäjän hyväksyntä- ja integrointitestit automaattisesti asentamalla RSAT-työkalu käytössä olevaan topologiaan ja tekemällä tarvittavat määritykset.</span><span class="sxs-lookup"><span data-stu-id="37974-138">To run user acceptance and integration tests automatically, you must install RSAT in the topology that you're using and configure it in the appropriate manner.</span></span> <span data-ttu-id="37974-139">Lisätietoja RSAT-työkalun asentamisesta ja sen määrittämisestä Finance and Operations- ja Azure DevOps -käyttöä varten on kohdassa [Dynamics 365 for Finance and Operations, Regression Suite Automation Tool](https://www.microsoft.com/download/details.aspx?id=57357).</span><span class="sxs-lookup"><span data-stu-id="37974-139">For information about how to install RSAT and configure it to work with Finance and Operations and Azure DevOps, see [Dynamics 365 for Finance and Operations, Regression Suite Automation Tool](https://www.microsoft.com/download/details.aspx?id=57357).</span></span> <span data-ttu-id="37974-140">Ota huomioon työkalun käytön edellytykset.</span><span class="sxs-lookup"><span data-stu-id="37974-140">Pay attention to the prerequisites for using the tool.</span></span> <span data-ttu-id="37974-141">Seuraavassa kuvassa on esimerkki RSAT-asetuksista.</span><span class="sxs-lookup"><span data-stu-id="37974-141">The following illustration shows an example of the RSAT settings.</span></span> <span data-ttu-id="37974-142">Sinisen suorakulmion sisällä ovat parametrit, jotka määrittävät Azure DevOps -käytön.</span><span class="sxs-lookup"><span data-stu-id="37974-142">The blue rectangle encloses the parameters that specify access to Azure DevOps.</span></span> <span data-ttu-id="37974-143">Vihreä suorakulmion sisällä on parametrit, jotka määrittävät Finance and Operations -esiintymän käytön.</span><span class="sxs-lookup"><span data-stu-id="37974-143">The green rectangle encloses the parameters that specify access to the Finance and Operations instance.</span></span>

    <span data-ttu-id="37974-144">![RSAT-asetukset](media/GER-Configure.png "Näyttökuva RSAT-asetukset-valintaikkunasta")</span><span class="sxs-lookup"><span data-stu-id="37974-144">![RSAT settings](media/GER-Configure.png "Screenshot of the RSAT Settings dialog box")</span></span>

- <span data-ttu-id="37974-145">Voit varmistaa testitapausten oikean suoritusjärjestyksen järjestämällä testitapaukset sarjoiksi. Voit kerätä tällä tavoin testauksen suorituslokeja lisäraportointia ja perehtymistä varten. Tätä varten tarvitaan käyttöönotetun Finance and Operations -topologian Azure DevOpsin käyttöoikeus.</span><span class="sxs-lookup"><span data-stu-id="37974-145">To organize test cases in suites to help guarantee the correct execution sequence, so that you can collect logs of test executions for further reporting and investigation, you must have access to Azure DevOps from the deployed Finance and Operations topology.</span></span>
- <span data-ttu-id="37974-146">Tämän ohjeaiheen esimerkin suorittamista varten kannattaa ladata [RSAT-testien ER-käyttö](https://go.microsoft.com/fwlink/?linkid=874684).</span><span class="sxs-lookup"><span data-stu-id="37974-146">To complete the example in this topic, we recommend that you download [ER usage for RSAT tests](https://go.microsoft.com/fwlink/?linkid=874684).</span></span> <span data-ttu-id="37974-147">Tämä zip-tiedosto sisältää seuraavat tehtäväoppaat:</span><span class="sxs-lookup"><span data-stu-id="37974-147">This zip file contains the following task guides:</span></span>

    | <span data-ttu-id="37974-148">Sisältö</span><span class="sxs-lookup"><span data-stu-id="37974-148">Content</span></span>                                           | <span data-ttu-id="37974-149">Tiedoston nimi ja sijainti</span><span class="sxs-lookup"><span data-stu-id="37974-149">File name and location</span></span> |
    |---------------------------------------------------|------------------------|
    | <span data-ttu-id="37974-150">Tehtävätallennenäyte tietojen valmisteluun testausta varten</span><span class="sxs-lookup"><span data-stu-id="37974-150">Sample task recording to prepare data for testing</span></span> | <span data-ttu-id="37974-151">Prepare\\Recording.xml</span><span class="sxs-lookup"><span data-stu-id="37974-151">Prepare\\Recording.xml</span></span> |
    | <span data-ttu-id="37974-152">Tehtävätallennenäyte toimittajan maksujen käsittelyyn</span><span class="sxs-lookup"><span data-stu-id="37974-152">Sample task recording to process vendor payment</span></span>   | <span data-ttu-id="37974-153">Process\\Recording.xml</span><span class="sxs-lookup"><span data-stu-id="37974-153">Process\\Recording.xml</span></span> |

## <a name="prepare-the-accounts-payable-module-to-process-vendor-payments"></a><span data-ttu-id="37974-154">Ostoreskontra-moduulin valmisteleminen käsittelemään toimittajan maksuja</span><span class="sxs-lookup"><span data-stu-id="37974-154">Prepare the Accounts payable module to process vendor payments</span></span>

1. <span data-ttu-id="37974-155">Kirjaudu omaan Finance and Operations -esiintymään.</span><span class="sxs-lookup"><span data-stu-id="37974-155">Sign in to your Finance and Operations instance.</span></span>
2. <span data-ttu-id="37974-156">Lataa seuraavat ER-konfiguraatiot LCS:stä.</span><span class="sxs-lookup"><span data-stu-id="37974-156">Download the following ER configurations from LCS.</span></span> <span data-ttu-id="37974-157">Ohjeet ovat kohdassa [ER Tuo konfiguraatio Lifecycle Services -palvelusta](./tasks/er-import-configuration-lifecycle-services.md).</span><span class="sxs-lookup"><span data-stu-id="37974-157">For instructions, see [ER Import a configuration from Lifecycle Services](./tasks/er-import-configuration-lifecycle-services.md).</span></span>

    - <span data-ttu-id="37974-158">**Maksumalli** ER-mallikonfiguraatio</span><span class="sxs-lookup"><span data-stu-id="37974-158">**Payment model** ER model configuration</span></span>
    - <span data-ttu-id="37974-159">**Maksumallin yhdistämismääritys 1611** ER-mallin yhdistämismääritys</span><span class="sxs-lookup"><span data-stu-id="37974-159">**Payment model mapping 1611** ER model mapping configuration</span></span>
    - <span data-ttu-id="37974-160">**BACS (UK)** ER-muotokonfiguraatio</span><span class="sxs-lookup"><span data-stu-id="37974-160">**BACS (UK)** ER format configuration</span></span>

    <span data-ttu-id="37974-161">![Sähköisen raportoinnin konfiguraatiot](media/GER-Configurations.png "Näyttökuva sähköisen raportoinnin Konfiguroinnit-sivusta")</span><span class="sxs-lookup"><span data-stu-id="37974-161">![Electronic reporting configurations](media/GER-Configurations.png "Screenshot of the Configurations page in Electronic reporting")</span></span>

3. <span data-ttu-id="37974-162">**GBSI**-demotietoyritys, sillä sen alue- tai maakonteksti on Iso-Britannia.</span><span class="sxs-lookup"><span data-stu-id="37974-162">Select the **GBSI** demo data company, which has a country/region context in Great Britain.</span></span>
4. <span data-ttu-id="37974-163">Määritä ostoreskontran parametrit:</span><span class="sxs-lookup"><span data-stu-id="37974-163">Configure Accounts payable parameters:</span></span>

    1. <span data-ttu-id="37974-164">Valitse **Ostoreskontra \> Maksun asetukset \> Maksutavat**.</span><span class="sxs-lookup"><span data-stu-id="37974-164">Go to **Accounts payable \> Payment setup \> Methods of payment**.</span></span>
    2. <span data-ttu-id="37974-165">Valitse maksutavaksi **Sähköinen**.</span><span class="sxs-lookup"><span data-stu-id="37974-165">Select the **Electronic** method of payment.</span></span>
    3. <span data-ttu-id="37974-166">Määritä valittu maksutapa käyttämään aiemmin toimittajan maksujen käsittelyä varten ladattua **BACS (UK)** -ER-muotoa:</span><span class="sxs-lookup"><span data-stu-id="37974-166">Configure the selected method of payment so that it uses the **BACS (UK)** ER format that you downloaded earlier for vendor payment processing:</span></span>

        1. <span data-ttu-id="37974-167">Määritä **Tiedostomuodot**-pikavälilehden **Yleinen sähköinen vientimuoto** -asetukseksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="37974-167">On the **File formats** FastTab, set the **Generic electronic Export format** option to **Yes**.</span></span>
        2. <span data-ttu-id="37974-168">Valitse **Vie muotokonfiguraatio** -kentässä **BACS (UK)**.</span><span class="sxs-lookup"><span data-stu-id="37974-168">In the **Export format configuration** field, select **BACS (UK)**.</span></span>

    <span data-ttu-id="37974-169">![Maksutavat-sivu](media/GER-APParameters.png "Näyttökuva Maksutavat-sivusta")</span><span class="sxs-lookup"><span data-stu-id="37974-169">![Methods of payment page](media/GER-APParameters.png "Screenshot of the Methods of payment page")</span></span>

    > [!NOTE]
    > <span data-ttu-id="37974-170">Jos sinulla on tämän ER-muodon johdettu versio, joka luotiin tukemaan mukautuksia, voit valita tämän konfiguraation **Sähköinen**-maksutavassa.</span><span class="sxs-lookup"><span data-stu-id="37974-170">If you have the derived version of this ER format that was created to support customizations, you can select this configuration in the **Electronic** method of payment.</span></span>

5. <span data-ttu-id="37974-171">Luo toimittajan maksuesimerkki:</span><span class="sxs-lookup"><span data-stu-id="37974-171">Create an example vendor payment:</span></span>

    1. <span data-ttu-id="37974-172">Valitse **Ostoreskontra \> Maksut \> Maksukirjauskansio**.</span><span class="sxs-lookup"><span data-stu-id="37974-172">Go to **Accounts payable \> Payments \> Payment journal**.</span></span>
    2. <span data-ttu-id="37974-173">Varmista, ettei maksukirjauskansioon ole tehty kirjausta.</span><span class="sxs-lookup"><span data-stu-id="37974-173">Make sure that you haven't posted the payment journal.</span></span>

        <span data-ttu-id="37974-174">![Maksukirjauskansio-sivu](media/GER-APJournal.png "Näyttökuva Maksukirjauskansio-sivusta")</span><span class="sxs-lookup"><span data-stu-id="37974-174">![Payment journal page](media/GER-APJournal.png "Screenshot of the Payment journal page")</span></span>

    3. <span data-ttu-id="37974-175">Valitse **Rivit**ja lisää rivi, jossa on seuraavat tiedot.</span><span class="sxs-lookup"><span data-stu-id="37974-175">Select **Lines**, and enter a line that has the following information.</span></span>

        | <span data-ttu-id="37974-176">Kenttä</span><span class="sxs-lookup"><span data-stu-id="37974-176">Field</span></span>               | <span data-ttu-id="37974-177">Esimerkkiarvo</span><span class="sxs-lookup"><span data-stu-id="37974-177">Example value</span></span>   |
        |---------------------|-----------------|
        | <span data-ttu-id="37974-178">Toimittajan nimi</span><span class="sxs-lookup"><span data-stu-id="37974-178">Vendor name</span></span>         | <span data-ttu-id="37974-179">GB\_SI\_000001</span><span class="sxs-lookup"><span data-stu-id="37974-179">GB\_SI\_000001</span></span>  |
        | <span data-ttu-id="37974-180">Veloitus</span><span class="sxs-lookup"><span data-stu-id="37974-180">Debit</span></span>               | <span data-ttu-id="37974-181">1,000.00</span><span class="sxs-lookup"><span data-stu-id="37974-181">1,000.00</span></span>        |
        | <span data-ttu-id="37974-182">Valuutta</span><span class="sxs-lookup"><span data-stu-id="37974-182">Currency</span></span>            | <span data-ttu-id="37974-183">GBP</span><span class="sxs-lookup"><span data-stu-id="37974-183">GBP</span></span>             |
        | <span data-ttu-id="37974-184">Vastatilityyppi</span><span class="sxs-lookup"><span data-stu-id="37974-184">Offset account type</span></span> | <span data-ttu-id="37974-185">Pankki</span><span class="sxs-lookup"><span data-stu-id="37974-185">Bank</span></span>            |
        | <span data-ttu-id="37974-186">Vastatili</span><span class="sxs-lookup"><span data-stu-id="37974-186">Offset account</span></span>      | <span data-ttu-id="37974-187">GBSI OPER</span><span class="sxs-lookup"><span data-stu-id="37974-187">GBSI OPER</span></span>       |
        | <span data-ttu-id="37974-188">Maksutapa</span><span class="sxs-lookup"><span data-stu-id="37974-188">Method of payment</span></span>   | <span data-ttu-id="37974-189">Sähköinen</span><span class="sxs-lookup"><span data-stu-id="37974-189">Electronic</span></span>      |

    <span data-ttu-id="37974-190">![Toimittaja maksut -sivu](media/GER-APJournalLines.png "Näyttökuva Toimittajan maksut -sivusta")</span><span class="sxs-lookup"><span data-stu-id="37974-190">![Vendor payments page](media/GER-APJournalLines.png "Screenshot of the Vendor payments page")</span></span>

## <a name="prepare-the-er-framework-to-test-vendor-payment-processing"></a><span data-ttu-id="37974-191">ER-kehyksen valmisteleminen toimittajan maksujen käsittelyn testaamiseen</span><span class="sxs-lookup"><span data-stu-id="37974-191">Prepare the ER framework to test vendor payment processing</span></span>

### <a name="configure-er-parameters"></a><span data-ttu-id="37974-192">Konfiguroi ER-parametrit</span><span class="sxs-lookup"><span data-stu-id="37974-192">Configure ER parameters</span></span>

1. <span data-ttu-id="37974-193">Valitse **Organisaation hallinto \> Sähköinen raportointi \> Sähköisen raportoinnin parametrit**.</span><span class="sxs-lookup"><span data-stu-id="37974-193">Go to **Organization administration \> Electronic reporting \> Electronic reporting parameters**.</span></span>
2. <span data-ttu-id="37974-194">Valitse **Liitteet**-välilehden **Perusrivi**-kentässä **Tiedosto** asiakirjatyypiksi, jota tiedostonhallinta- eli DM-kehys käyttää säilyttämään perustoimintoon DM-liitteinä liittyviä tiedostoja.</span><span class="sxs-lookup"><span data-stu-id="37974-194">On the **Attachments** tab, in the **Baseline** field, select **File** as the document type that the Document management (DM) framework uses to keep documents that are related to the baseline feature as DM attachments.</span></span>

    <span data-ttu-id="37974-195">![Sähköisen raportoinnin parametrit -sivu](media/GER-ERParameters.png "Näyttökuva sähköisen raportoinnin parametrit -sivusta")</span><span class="sxs-lookup"><span data-stu-id="37974-195">![Electronic reporting parameters page](media/GER-ERParameters.png "Screenshot of the Electronic reporting parameters page")</span></span>

### <a name="generate-baseline-copies-of-vendor-paymentrelated-documents"></a><span data-ttu-id="37974-196">Toimittajan maksuihin liittyvien asiakirjojen peruskopioiden luominen</span><span class="sxs-lookup"><span data-stu-id="37974-196">Generate baseline copies of vendor payment–related documents</span></span>

1. <span data-ttu-id="37974-197">Valitse **Ostoreskontra \> Maksut \> Maksukirjauskansio**.</span><span class="sxs-lookup"><span data-stu-id="37974-197">Go to **Accounts payable \> Payments \> Payment journal**.</span></span>
2. <span data-ttu-id="37974-198">Valitse **Rivit**.</span><span class="sxs-lookup"><span data-stu-id="37974-198">Select **Lines**.</span></span>
3. <span data-ttu-id="37974-199">Valitse **Muodosta maksut**.</span><span class="sxs-lookup"><span data-stu-id="37974-199">Select **Generate payments**.</span></span>
4. <span data-ttu-id="37974-200">Valitse maksutavaksi **Sähköinen**.</span><span class="sxs-lookup"><span data-stu-id="37974-200">Select the **Electronic** method of payment.</span></span>
5. <span data-ttu-id="37974-201">Valitse **GBSI OPER** -pankkitili.</span><span class="sxs-lookup"><span data-stu-id="37974-201">Select the **GBSI OPER** bank account.</span></span>
6. <span data-ttu-id="37974-202">Määritä **Tulosta valvontaraportti** -asetukseksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="37974-202">Set the **Print control report** option to **Yes**.</span></span>
7. <span data-ttu-id="37974-203">Lataa tulos zip-tiedostona.</span><span class="sxs-lookup"><span data-stu-id="37974-203">Download the generated output as a zip file.</span></span>
8. <span data-ttu-id="37974-204">Avaa ladattu tiedosto.</span><span class="sxs-lookup"><span data-stu-id="37974-204">Open the downloaded file.</span></span>
9. <span data-ttu-id="37974-205">Pura seuraavat tiedostot ladatusta tiedostosta:</span><span class="sxs-lookup"><span data-stu-id="37974-205">Extract following files from the downloaded file:</span></span>

    - <span data-ttu-id="37974-206">**Tiedosto**-maksutiedosto tekstimuotoisena</span><span class="sxs-lookup"><span data-stu-id="37974-206">**File** payment file in text format</span></span>
    - <span data-ttu-id="37974-207">**ERVendOutPaymControlReport**-valvontaraporttitiedosto XLSX-muodossa</span><span class="sxs-lookup"><span data-stu-id="37974-207">**ERVendOutPaymControlReport** control report file in XLSX format</span></span>

    <span data-ttu-id="37974-208">![Puretut tiedostot](media/GER-APJournalProcessed.png "Näyttökuva puretuista tiedostonimissä Windowsin Resurssienhallinnassa")</span><span class="sxs-lookup"><span data-stu-id="37974-208">![Extracted files](media/GER-APJournalProcessed.png "Screenshot of extracted file names in Windows explorer")</span></span>

### <a name="turn-on-the-er-baseline-feature"></a><span data-ttu-id="37974-209">ER-perusrivitoiminnon ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="37974-209">Turn on the ER baseline feature</span></span>

1. <span data-ttu-id="37974-210">Siirry kohtaan **Organisaation hallinto \> Sähköinen raportointi \> Konfiguraatiot**.</span><span class="sxs-lookup"><span data-stu-id="37974-210">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
2. <span data-ttu-id="37974-211">Valitse toimintoruudun **Konfiguroinnit**-välilehdessä **Käyttäjän parametrit**.</span><span class="sxs-lookup"><span data-stu-id="37974-211">On the Action Pane, on the **Configurations** tab, select **User parameters**.</span></span>
3. <span data-ttu-id="37974-212">Määritä **Suorita virheenkorjaustila** -asetukseksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="37974-212">Set the **Run in debug mode** option to **Yes**.</span></span>

<span data-ttu-id="37974-213">**Suorita vianmääritystilassa** -parametrin ottaminen käyttöön pakottaa ER-kehyksen suorittamaan seuraavat toiminnot sen jälkeen, kun lähteviä asiakirjoja luova ER-muoto on suoritettu:</span><span class="sxs-lookup"><span data-stu-id="37974-213">By turning on the **Run in debug mode** parameter, you force the ER framework to perform the following actions after the execution of any ER format that generates outgoing documents:</span></span>

1. <span data-ttu-id="37974-214">Määritetään, määritettiinkö millekään suoritetun ER-muodon osalle perusrivi.</span><span class="sxs-lookup"><span data-stu-id="37974-214">Determine whether a baseline was configured for any of components of the executed ER format.</span></span>
2. <span data-ttu-id="37974-215">Määritetään, yksi kerrallaan soveltuuko määritetty perusrivi nykyiseen tilanteeseen (esimerkiksi kirjautuneen yrityksen yrityskoodi sekä tuloksen tiedostonimi ja tiedostotunniste).</span><span class="sxs-lookup"><span data-stu-id="37974-215">Determine whether each configured baseline is applicable in the current conditions (company code of the signed-in company, file name and file name extension of the generated output, and so on).</span></span>
3. <span data-ttu-id="37974-216">Kunkin soveltuvan perusrivin kohdalla tehdään seuraavat toiminnot:</span><span class="sxs-lookup"><span data-stu-id="37974-216">For each applicable baseline, perform the following actions:</span></span>

    1. <span data-ttu-id="37974-217">ER-muodon suorituksen aikana luotua tulosta verrataan vastaavaan perusriviin.</span><span class="sxs-lookup"><span data-stu-id="37974-217">Compare the output that is generated during execution of the ER format with the corresponding baseline.</span></span>
    2. <span data-ttu-id="37974-218">Vertailun tulokset tallennetaan ER-konfiguraatioiden virheenkorjauslokiin.</span><span class="sxs-lookup"><span data-stu-id="37974-218">Store the results of the comparison in the ER configurations debug log.</span></span>

### <a name="configure-er-baselines-for-vendor-payment-processing"></a><span data-ttu-id="37974-219">ER-perusrivien määrittäminen toimittajan maksujen käsittelyä varten</span><span class="sxs-lookup"><span data-stu-id="37974-219">Configure ER baselines for vendor payment processing</span></span>

1. <span data-ttu-id="37974-220">Siirry kohtaan **Organisaation hallinto \> Sähköinen raportointi \> Konfiguraatiot**.</span><span class="sxs-lookup"><span data-stu-id="37974-220">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
2. <span data-ttu-id="37974-221">Valitse **Perusrivit**.</span><span class="sxs-lookup"><span data-stu-id="37974-221">Select **Baselines**.</span></span>
3. <span data-ttu-id="37974-222">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="37974-222">Select **New**.</span></span>
4. <span data-ttu-id="37974-223">Valitse **Viite**-kentässä **BACS (UK)** -muoto.</span><span class="sxs-lookup"><span data-stu-id="37974-223">In the **Reference** field, select the **BACS (UK)** format.</span></span>
5. <span data-ttu-id="37974-224">Valitse **Liitteet**.</span><span class="sxs-lookup"><span data-stu-id="37974-224">Select **Attachments**.</span></span>
6. <span data-ttu-id="37974-225">Lisää uusi toimittajan maksutiedoston perusrivi:</span><span class="sxs-lookup"><span data-stu-id="37974-225">Add a new baseline for the vendor payment file:</span></span>

    1. <span data-ttu-id="37974-226">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="37974-226">Select **New**.</span></span>
    2. <span data-ttu-id="37974-227">Tallenna perusrivin tiedot valitsemalla **Tyyppi**-kentässä se**Tiedosto**-DM-asiakirjatyyppi, jonka määritit ER-parametreissa.</span><span class="sxs-lookup"><span data-stu-id="37974-227">In the **Type** field, select the **File** DM document type that you configured in the ER parameters to store baseline artifacts.</span></span>
    3. <span data-ttu-id="37974-228">Siirry valitsemaan paikallisesti tallennettu tekstimuotoinen **Tiedosto**-maksutiedosto.</span><span class="sxs-lookup"><span data-stu-id="37974-228">Browse to select the locally saved **File** payment file in text format.</span></span>
    4. <span data-ttu-id="37974-229">Kirjoita **Kuvaus**-kenttään **Maksun TXT-tiedosto**.</span><span class="sxs-lookup"><span data-stu-id="37974-229">In the **Description** field, enter **Payment TXT file**.</span></span>

7. <span data-ttu-id="37974-230">Lisää toimittajan maksujen seurantaraportin uusi perusrivi:</span><span class="sxs-lookup"><span data-stu-id="37974-230">Add a new baseline for the control report for the vendor payment:</span></span>

    1. <span data-ttu-id="37974-231">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="37974-231">Select **New**.</span></span>
    2. <span data-ttu-id="37974-232">Tallenna perusrivin tiedot valitsemalla **Tyyppi**-kentässä se**Tiedosto**-DM-asiakirjatyyppi, jonka määritit ER-parametreissa.</span><span class="sxs-lookup"><span data-stu-id="37974-232">In the **Type** field, select the **File** DM document type that you configured in the ER parameters to store baseline artifacts.</span></span>
    3. <span data-ttu-id="37974-233">Siirry valitsemaan paikallisesti tallennettu XLSX-muotoinen **ERVendOutPaymControlReport**-seurantatiedosto.</span><span class="sxs-lookup"><span data-stu-id="37974-233">Browse to select the locally saved **ERVendOutPaymControlReport** control report file in XLSX format.</span></span>
    4. <span data-ttu-id="37974-234">Kirjoita **Kuvaus**-kenttään **Maksun XLSX-seurantaraportti**.</span><span class="sxs-lookup"><span data-stu-id="37974-234">In the **Description** field, enter **Payment XLSX control report**.</span></span>

    <span data-ttu-id="37974-235">![Toimittajan maksutiedoston ja seurantaraportin perusrivit](media/GER-BaselineAttachments.png "Näyttökuva Konfiguroinnit-sivusta, jossa valittuna Maksun XLSX-seurantaraportti")</span><span class="sxs-lookup"><span data-stu-id="37974-235">![Baselines for the vendor payment file and control report](media/GER-BaselineAttachments.png "Screenshot of the Configurations page with the Payment XLSX control report selected")</span></span>

8. <span data-ttu-id="37974-236">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="37974-236">Close the page.</span></span>
9. <span data-ttu-id="37974-237">Määritä maksutiedoston perusrivi valitsemalla **Perusrivit**-pikavälilehdessä **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="37974-237">On the **Baselines** FastTab, select **New** to configure a baseline for the payment file:</span></span>

    1. <span data-ttu-id="37974-238">Anna rivin nimeksi **Maksutiedoston perusriviasetus**.</span><span class="sxs-lookup"><span data-stu-id="37974-238">Name the line **Baseline setting for payment file**.</span></span>
    2. <span data-ttu-id="37974-239">Valitse **Tiedosto-osan nimi**-kentässä **tiedosto**. Tätä perusriviä käytetään nyt ER-muodon tuloksessa, joka luo maksutiedoston BACS (UK) -tekstimuodossa.</span><span class="sxs-lookup"><span data-stu-id="37974-239">In the **File component name** field, select **file** to apply this baseline to the ER format output that generates the payment file in BACS (UK) text format.</span></span>
    3. <span data-ttu-id="37974-240">Valitsemalla **Yritykset**-kentässä **GBSI** voit käyttää tätä perusriviä, kun **BACS (UK)** -ER-muoto suoritetaan GBSI-yrityksessä.</span><span class="sxs-lookup"><span data-stu-id="37974-240">In the **Companies** field, select **GBSI** to apply this baseline when the **BACS (UK)** ER format is run in the GBSI company.</span></span>
    4. <span data-ttu-id="37974-241">Jos **Tiedostonimen peite** -kentässä annetaan **\*.TXT**, tätä perusriviä käytetään vain niissä **tiedosto**-muoto-osan tuloksissa, joiden tiedostotunniste on **.txt**.</span><span class="sxs-lookup"><span data-stu-id="37974-241">In **File name mask** field, enter **\*.TXT** to apply this baseline only to outputs of the **file** format component that have the **.txt** file name extension.</span></span>
    5. <span data-ttu-id="37974-242">Valitse **Perusrivi**-kentässä **Maksun TXT-tiedosto**, jolloin tätä perusriviä käytetään verratessa luotua tulosta.</span><span class="sxs-lookup"><span data-stu-id="37974-242">In the **Baseline** field, select **Payment TXT file** so that this baseline is used for comparison with the generated output.</span></span>

10. <span data-ttu-id="37974-243">Määritä seurantaraportin perusrivi valitsemalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="37974-243">Select **New** to configure a baseline for the control report:</span></span>

    1. <span data-ttu-id="37974-244">Anna rivin nimeksi **Seurantaraportin perusriviasetus**.</span><span class="sxs-lookup"><span data-stu-id="37974-244">Name the line **Baseline setting for control report**.</span></span>
    2. <span data-ttu-id="37974-245">Valitse **Tiedosto-osan nimi**-kentässä **ERVendOutPaymControlReport**. Tätä perusriviä käytetään nyt ER-muodon tuloksessa, joka luo seurantaraportin.</span><span class="sxs-lookup"><span data-stu-id="37974-245">In the **File component name** field, select **ERVendOutPaymControlReport** to apply this baseline to the ER format output that generates the control report.</span></span>
    3. <span data-ttu-id="37974-246">Valitsemalla **Yritykset**-kentässä **GBSI** voit käyttää tätä perusriviä, kun **BACS (UK)** -ER-muoto suoritetaan GBSI-yrityksessä.</span><span class="sxs-lookup"><span data-stu-id="37974-246">In the **Companies** field, select **GBSI** to apply this baseline when the **BACS (UK)** ER format is run in the GBSI company.</span></span>
    4. <span data-ttu-id="37974-247">Jos **Tiedostonimen peite** -kentässä annetaan **\*.XLSX**, tätä perusriviä käytetään vain niissä **ERVendOutPaymControlReport**-muoto-osan tuloksissa, joiden tiedostotunniste on **.xslx**.</span><span class="sxs-lookup"><span data-stu-id="37974-247">In **File name mask** field, enter **\*.XLSX** to apply this baseline only to outputs of the **ERVendOutPaymControlReport** format component that have the **.xslx** file name extension.</span></span>
    5. <span data-ttu-id="37974-248">Valitse **Perusrivi**-kentässä **Maksun XLSX-seurantaraportti**, jolloin tätä perusriviä käytetään verratessa luotua tulosta.</span><span class="sxs-lookup"><span data-stu-id="37974-248">In the **Baseline** field, select **Payment XLSX control report** so that this baseline is used for comparison with the generated output.</span></span>

    <span data-ttu-id="37974-249">![Konfigurointi-sivun Perusrivit-pikavälilehti](media/GER-BaselineRules.png "Näyttökuva Konfigurointi-sivun Perusrivit-pikavälilehdestä")</span><span class="sxs-lookup"><span data-stu-id="37974-249">![Baselines FastTab on the Configurations page](media/GER-BaselineRules.png "Screenshot of the Baselines FastTab on the Configurations page")</span></span>

## <a name="record-tests-to-validate-vendor-payment-processing"></a><span data-ttu-id="37974-250">Testien tallentaminen toimittajan maksujen käsittelyn tarkistamiseen</span><span class="sxs-lookup"><span data-stu-id="37974-250">Record tests to validate vendor payment processing</span></span>

<span data-ttu-id="37974-251">Voit tehotoimintakäyttäjänä tallentaa ovat toimittajan maksujen käsittelyn testivaiheet.</span><span class="sxs-lookup"><span data-stu-id="37974-251">As a functional power user, you can record your own steps to test vendor payment processing.</span></span> <span data-ttu-id="37974-252">Aiemmin ladattu **Prepare\\Recording.xml** -tehtävätallenne kannattaa toistaa (ja muokata tarvittaessa).</span><span class="sxs-lookup"><span data-stu-id="37974-252">We recommend that you play (and edit, as required) the **Prepare\\Recording.xml** task recording that you downloaded earlier.</span></span> <span data-ttu-id="37974-253">Tämän tallenteen avulla voi määrittää oikean tilan kaikille testitiedoille.</span><span class="sxs-lookup"><span data-stu-id="37974-253">This recording is used to set all testing data to the correct state.</span></span> <span data-ttu-id="37974-254">Kyseinen vaihe on pakolinen, sillä testaus voidaan tehdä useita kertoja ja jokaisen testin on käytettävä tietoja, joilla on sama tila.</span><span class="sxs-lookup"><span data-stu-id="37974-254">That step is required because the testing can be done many times, and every test must use data that is in the same state.</span></span>

### <a name="reset-user-settings"></a><span data-ttu-id="37974-255">Käyttäjäasetusten nollaaminen</span><span class="sxs-lookup"><span data-stu-id="37974-255">Reset user settings</span></span>

1. <span data-ttu-id="37974-256">Avaa Finance and Operationsin oletuskoontinäyttö.</span><span class="sxs-lookup"><span data-stu-id="37974-256">Open the default Finance and Operations dashboard.</span></span>
2. <span data-ttu-id="37974-257">Valitse **Asetukset**-painike (rataskuvake).</span><span class="sxs-lookup"><span data-stu-id="37974-257">Select the **Settings** button (the gear symbol).</span></span>
3. <span data-ttu-id="37974-258">Valitse **Käyttäjäasetukset**.</span><span class="sxs-lookup"><span data-stu-id="37974-258">Select **User options**.</span></span>
4. <span data-ttu-id="37974-259">Valitse **Käyttötiedot**.</span><span class="sxs-lookup"><span data-stu-id="37974-259">Select **Usage data**.</span></span>
5. <span data-ttu-id="37974-260">Valitse **Nollaa**.</span><span class="sxs-lookup"><span data-stu-id="37974-260">Select **Reset**.</span></span>
6. <span data-ttu-id="37974-261">Vahvista, että haluat nollata käyttötiedot valitsemalla **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="37974-261">Select **Yes** to confirm that you want to reset usage data.</span></span>
7. <span data-ttu-id="37974-262">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="37974-262">Close the page.</span></span>

### <a name="record-the-steps-to-prepare-data-for-testing"></a><span data-ttu-id="37974-263">Tiedostojen testauksen valmisteluvaiheiden tallentaminen</span><span class="sxs-lookup"><span data-stu-id="37974-263">Record the steps to prepare data for testing</span></span>

1. <span data-ttu-id="37974-264">Valitse **Asetukset**-painike (rataskuvake).</span><span class="sxs-lookup"><span data-stu-id="37974-264">Select the **Settings** button (the gear symbol).</span></span>
2. <span data-ttu-id="37974-265">Valitse **Tehtävän tallennustoiminto**.</span><span class="sxs-lookup"><span data-stu-id="37974-265">Select **Task recorder**.</span></span>
3. <span data-ttu-id="37974-266">Valitset **Toista tallenne**.</span><span class="sxs-lookup"><span data-stu-id="37974-266">Select **Playback recording**.</span></span>
4. <span data-ttu-id="37974-267">Valitse **Avaa tältä tietokoneelta**.</span><span class="sxs-lookup"><span data-stu-id="37974-267">Select **Open from this PC**.</span></span>
5. <span data-ttu-id="37974-268">Valitse **Selaa** ja tallenna sitten **Prepare\\Recording.xml**-tiedosto paikallisesti.</span><span class="sxs-lookup"><span data-stu-id="37974-268">Select **Browse**, and select the locally save **Prepare\\Recording.xml** file.</span></span>
6. <span data-ttu-id="37974-269">Valitse **Aloita**.</span><span class="sxs-lookup"><span data-stu-id="37974-269">Select **Start**.</span></span>
7. <span data-ttu-id="37974-270">Valitse **Toista seuraava odottava vaihe** niin monta kertaa, että kaikki tallenteen vaiheet on toistettu.</span><span class="sxs-lookup"><span data-stu-id="37974-270">Keep selecting **Play next pending step** until all the steps in the recording have been played.</span></span>

<span data-ttu-id="37974-271">Tämä tehtävätallenne suorittaa seuraavat toimenpiteet:</span><span class="sxs-lookup"><span data-stu-id="37974-271">This task recording performs the following actions:</span></span>

1. <span data-ttu-id="37974-272">Käsitellyn maksurivin tilaksi määritetään **Ei mitään**.</span><span class="sxs-lookup"><span data-stu-id="37974-272">Set the status of the processed payment line to **None**.</span></span>

    <span data-ttu-id="37974-273">![Tehtävätallenteen vaiheet 3–4](media/GER-Recording1Review1.png "Näyttökuva tehtävätallenteen vaiheista 3–4")</span><span class="sxs-lookup"><span data-stu-id="37974-273">![Task recording steps 3 through 4](media/GER-Recording1Review1.png "Screenshot of task recording steps 3 through 4")</span></span>

2. <span data-ttu-id="37974-274">Ota käyttäjän **Suorita virheenkorjaustilassa** -ER-parametri käyttöön.</span><span class="sxs-lookup"><span data-stu-id="37974-274">Turn on the **Run in debug mode** ER user parameter.</span></span>

    <span data-ttu-id="37974-275">![Tehtävätallenteen vaiheet 9–10](media/GER-Recording1Review2.png "Näyttökuva tehtävätallenteen vaiheista 9–10")</span><span class="sxs-lookup"><span data-stu-id="37974-275">![Task recording steps 9 through 10](media/GER-Recording1Review2.png "Screenshot of task recording steps 9 through 10")</span></span>

3. <span data-ttu-id="37974-276">Tyhjennä ER-virheenkorjausloki, joka sisältää luotujen tiedostojen ja perusrivien vertailutulokset.</span><span class="sxs-lookup"><span data-stu-id="37974-276">Clean up the ER debug log that contains the results of the comparison of generated files to baselines.</span></span>

    <span data-ttu-id="37974-277">![Tehtävätallenteen vaiheet 13–15](media/GER-Recording1Review3.png "Näyttökuva tehtävätallenteen vaiheista 13–15")</span><span class="sxs-lookup"><span data-stu-id="37974-277">![Task recording steps 13 through 15](media/GER-Recording1Review3.png "Screenshot of task recording steps 13 through 15")</span></span>

### <a name="record-the-steps-to-test-vendor-payment-processing"></a><span data-ttu-id="37974-278">Toimittajan maksujen käsittelyn testausvaiheiden tallentaminen</span><span class="sxs-lookup"><span data-stu-id="37974-278">Record the steps to test vendor payment processing</span></span>

<span data-ttu-id="37974-279">Aiemmin ladattu **Process\\Recording.xml** -tehtävätallenne kannattaa toistaa (ja muokata tarvittaessa).</span><span class="sxs-lookup"><span data-stu-id="37974-279">We recommend that you play (and edit, as required) the **Process\\Recording.xml** task recording that you downloaded earlier.</span></span> <span data-ttu-id="37974-280">Tätä tallennetta käytetään toimittajan maksujen käsittelemiseen sekä luotujen asiakirjojen ja vastaavien perusrivien vertailutulosten tarkistamiseen.</span><span class="sxs-lookup"><span data-stu-id="37974-280">This recording is used to process vendor payments and validate the results of the comparison of generated documents to corresponding baselines.</span></span>

1. <span data-ttu-id="37974-281">Valitse **Asetukset**-painike (rataskuvake).</span><span class="sxs-lookup"><span data-stu-id="37974-281">Select the **Settings** button (the gear symbol).</span></span>
2. <span data-ttu-id="37974-282">Valitse **Tehtävän tallennustoiminto**.</span><span class="sxs-lookup"><span data-stu-id="37974-282">Select **Task recorder**.</span></span>
3. <span data-ttu-id="37974-283">Valitset **Toista tallenne**.</span><span class="sxs-lookup"><span data-stu-id="37974-283">Select **Playback recording**.</span></span>
4. <span data-ttu-id="37974-284">Valitse **Avaa tältä tietokoneelta**.</span><span class="sxs-lookup"><span data-stu-id="37974-284">Select **Open from this PC**.</span></span>
5. <span data-ttu-id="37974-285">Valitse **Selaa** ja valitse sitten paikallisesti tallennettu **Process\\Recording.xml**-tiedosto.</span><span class="sxs-lookup"><span data-stu-id="37974-285">Select **Browse**, and select the locally saved **Process\\Recording.xml** file.</span></span>
6. <span data-ttu-id="37974-286">Valitse **Aloita**.</span><span class="sxs-lookup"><span data-stu-id="37974-286">Select **Start**.</span></span>
7. <span data-ttu-id="37974-287">Valitse **Toista seuraava odottava vaihe** niin monta kertaa, että kaikki tallenteen vaiheet on toistettu.</span><span class="sxs-lookup"><span data-stu-id="37974-287">Keep selecting **Play next pending step** until all the steps in the recording have been played.</span></span>

<span data-ttu-id="37974-288">Tämä tehtävätallenne suorittaa seuraavat toimenpiteet:</span><span class="sxs-lookup"><span data-stu-id="37974-288">This task recording performs the following actions:</span></span>

1. <span data-ttu-id="37974-289">Aloita toimittajan maksujen käsittely.</span><span class="sxs-lookup"><span data-stu-id="37974-289">Start vendor payment processing.</span></span>
2. <span data-ttu-id="37974-290">Valitse oikeat suorituksenaikaiset parametrit ja ota seurantaraportin luonti käyttöön.</span><span class="sxs-lookup"><span data-stu-id="37974-290">Select the correct runtime parameters, and turn on generation of a control report.</span></span>

    <span data-ttu-id="37974-291">![Tehtävätallenteen vaiheet 3–8](media/GER-Recording2Review1.png "Näyttökuva tehtävätallenteen vaiheista 3–8")</span><span class="sxs-lookup"><span data-stu-id="37974-291">![Task recording steps 3 through 8](media/GER-Recording2Review1.png "Screenshot of task recording steps 3 through 8")</span></span>

3. <span data-ttu-id="37974-292">Siirry ER-virheenkorjauslokiin kirjaamaan luotujen tulosten ja vastaavien perusrivien vertailutulokset.</span><span class="sxs-lookup"><span data-stu-id="37974-292">Access the ER debug log to record the results of the comparison of generated outputs to corresponding baselines.</span></span>

    <span data-ttu-id="37974-293">Vertailun tulokset näkyvät ER-virheenkorjauslokissa **Luotu teksti** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="37974-293">In the ER debug log, the results of the comparison appear in the **Generated text** field.</span></span> <span data-ttu-id="37974-294">**Muoto-osa**- ja **Lokimerkinnän aiheuttaneen muodon polku** -kentät viittaavat tiedosto-osaan, jolle luotua tulosta on verrattu perusriviin.</span><span class="sxs-lookup"><span data-stu-id="37974-294">The **Format component** and **Format path that caused a log entry** fields refer to the file component for which the generated output has been compared to the baseline.</span></span>

    <span data-ttu-id="37974-295">![Sähköisen raportoinnin ajon lokit -sivun merkinnät](media/GER-ERDebugLog.png "Näyttökuva Sähköisen raportoinnin ajon lokit -sivusta")</span><span class="sxs-lookup"><span data-stu-id="37974-295">![Entries on the Electronic reporting run logs page](media/GER-ERDebugLog.png "Screenshot of entries on the Electronic reporting run logs page")</span></span>

4. <span data-ttu-id="37974-296">Nykyisen tuloksen ja perusrivin vertailu tallennetaan käyttämällä tehtävän tallennustoiminnon **Tarkista**-asetusta ja valitsemalla **Nykyinen arvo**.</span><span class="sxs-lookup"><span data-stu-id="37974-296">The comparison of the current output to the baseline is recorded by using the **Validate** Task recorder option and selecting  **Current Value**.</span></span>

    <span data-ttu-id="37974-297">![Tarkista-asetuksen käyttäminen nykyisen arvon vertailussa](media/GER-TRRecordValidation.png "Näyttökuva Tarkista-asetuksen käyttämisestä nykyisen arvon vertailussa")</span><span class="sxs-lookup"><span data-stu-id="37974-297">![Using the Validate option for comparison with the current value](media/GER-TRRecordValidation.png "Screenshot of using the Validate option for comparison with the current value")</span></span>

    <span data-ttu-id="37974-298">Seuraava kuva osoittaa, miltä tallennetut tarkistusvaiheet näyttävät tehtävätallenteessa.</span><span class="sxs-lookup"><span data-stu-id="37974-298">The following illustration shows what the recorded validation steps look like in the task recording.</span></span>

    <span data-ttu-id="37974-299">![Tehtävätallenteen vaiheet 13 ja 15](media/GER-Recording2Review2.png "Näyttökuva tehtävätallenteen vaiheista 13 ja 15")</span><span class="sxs-lookup"><span data-stu-id="37974-299">![Task recording steps 13 and 15](media/GER-Recording2Review2.png "Screenshot of task recording steps 13 and 15")</span></span>

## <a name="add-the-recorded-tests-to-azure-devops"></a><span data-ttu-id="37974-300">Tallennettujen testien lisääminen Azure DevOpsiin</span><span class="sxs-lookup"><span data-stu-id="37974-300">Add the recorded tests to Azure DevOps</span></span>

1. <span data-ttu-id="37974-301">Avaa Azure DevOps -ympäristö.</span><span class="sxs-lookup"><span data-stu-id="37974-301">Open the Azure DevOps environment.</span></span>
2. <span data-ttu-id="37974-302">Valitse projekti, jonka määritit RSAT-parametreissa [työkalua määritettäessä](#prerequisites).</span><span class="sxs-lookup"><span data-stu-id="37974-302">Select the project that you defined in the RSAT parameters when you [configured the tool](#prerequisites).</span></span>
3. <span data-ttu-id="37974-303">Valitse testisuunnitelma, jonka määritit RSAT-parametreissa [työkalua määritettäessä](#prerequisites).</span><span class="sxs-lookup"><span data-stu-id="37974-303">Select the test plan that you defined in the RSAT parameters when you [configured the tool](#prerequisites).</span></span>
4. <span data-ttu-id="37974-304">Luo uusi testitapaus valitulle testisuunnitelmalle:</span><span class="sxs-lookup"><span data-stu-id="37974-304">Create a new test case for the selected test plan:</span></span>

    1. <span data-ttu-id="37974-305">Anna testitapaukselle nimi **Tietojen valmistelu testaamaan toimittajan sähköisten maksujen käsittelyä**.</span><span class="sxs-lookup"><span data-stu-id="37974-305">Name the test case **Prepare data to test processing of vendor's electronic payment**.</span></span>
    2. <span data-ttu-id="37974-306">Liitä aiemmin ladattu **Recording.xml**-tiedosto **Prepare**-kansiosta.</span><span class="sxs-lookup"><span data-stu-id="37974-306">Attach the **Recording.xml** file from the **Prepare** folder that you downloaded earlier.</span></span>

5. <span data-ttu-id="37974-307">Luo uusi testitapaus valitulle testisuunnitelmalle:</span><span class="sxs-lookup"><span data-stu-id="37974-307">Create a new test case for the selected test plan:</span></span>

    1. <span data-ttu-id="37974-308">Anna testitapaukselle nimeksi **Toimittajan maksujen testaaminen käyttämällä ER-muotoa BACS (UK)**.</span><span class="sxs-lookup"><span data-stu-id="37974-308">Name the test case **Test processing of vendor payments by using ER format BACS (UK)**.</span></span>
    2. <span data-ttu-id="37974-309">Liitä aiemmin ladattu **Recording.xml**-tiedosto **Process**-kansiosta.</span><span class="sxs-lookup"><span data-stu-id="37974-309">Attach the **Recording.xml** file from the **Process** folder that you downloaded earlier.</span></span>

    <span data-ttu-id="37974-310">![Valitun testisuunnitelman uudet testitapaukset](media/GER-RSAT-DevOps-Tests-Passed.png "Näyttökuva valitun testisuunnitelman uusista testitapauksista")</span><span class="sxs-lookup"><span data-stu-id="37974-310">![New test cases for the selected test plan](media/GER-RSAT-DevOps-Tests-Passed.png "Screenshot of the new test cases for the selected test plan")</span></span>

> [!NOTE]
> <span data-ttu-id="37974-311">Varmista, että testit lisätään oikeassa suoritusjärjestyksessä.</span><span class="sxs-lookup"><span data-stu-id="37974-311">Pay attention to the correct execution order of the tests that are added.</span></span>

## <a name="prepare-rsat-to-run-the-recorded-tests"></a><span data-ttu-id="37974-312">RSAT-valmistelu suorittamaan tallennetut testit</span><span class="sxs-lookup"><span data-stu-id="37974-312">Prepare RSAT to run the recorded tests</span></span>

### <a name="load-the-tests-from-azure-devops-to-rsat"></a><span data-ttu-id="37974-313">Testien lataaminen Azure DevOpsista RSAT-työkaluun</span><span class="sxs-lookup"><span data-stu-id="37974-313">Load the tests from Azure DevOps to RSAT</span></span>

1. <span data-ttu-id="37974-314">Avaa paikallinen RSAT-sovellus nykyisessä topologiassa.</span><span class="sxs-lookup"><span data-stu-id="37974-314">Open the local RSAT application in the current topology.</span></span>
2. <span data-ttu-id="37974-315">Lataa tällä hetkellä Azure DevOpsissa sijaitsevat testit RSAT-työkaluun valitsemalla **Lataa**.</span><span class="sxs-lookup"><span data-stu-id="37974-315">Select **Load** to load the tests that currently reside in Azure DevOps into RSAT.</span></span>

    <span data-ttu-id="37974-316">![RSAT-työkaluun ladatut testit](media/GER-RSAT-RSAT-Tests-Loaded.png "Näyttökuva RSAT-työkaluun ladatuista testeistä")</span><span class="sxs-lookup"><span data-stu-id="37974-316">![Tests loaded into RSAT](media/GER-RSAT-RSAT-Tests-Loaded.png "Screenshot of the tests loaded into RSAT")</span></span>

### <a name="create-automation-and-parameters-files"></a><span data-ttu-id="37974-317">Automaatio- ja parametritiedostojen luominen</span><span class="sxs-lookup"><span data-stu-id="37974-317">Create automation and parameters files</span></span>

1. <span data-ttu-id="37974-318">Valitse RSAT-työkalussa Azure DevOpsista ladatut testit.</span><span class="sxs-lookup"><span data-stu-id="37974-318">In RSAT, select the tests that you loaded from Azure DevOps.</span></span>
2. <span data-ttu-id="37974-319">Luo RSAT-työkalun automaatio- ja parametritiedostot valitsemalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="37974-319">Select **New** to create RSAT automation and parameters files.</span></span>

    <span data-ttu-id="37974-320">![RSAT-työkalussa luodut automaatio- ja parametritiedostot](media/GER-RSAT-RSAT-Tests-Initiated.png "Näyttökuva RSAT-työkalussa luoduista automaatio- ja parametritiedostoista")</span><span class="sxs-lookup"><span data-stu-id="37974-320">![RSAT automation and parameters files created in RSAT](media/GER-RSAT-RSAT-Tests-Initiated.png "Screenshot of the RSAT automation and parameters files created in RSAT")</span></span>

### <a name="modify-the-parameters-files"></a><span data-ttu-id="37974-321">Parametritiedostojen muokkaaminen</span><span class="sxs-lookup"><span data-stu-id="37974-321">Modify the parameters files</span></span>

1. <span data-ttu-id="37974-322">Valitse RSAT-työkalussa **Tietojen valmistelu testaamaan toimittajan sähköisten maksujen käsittelyä** -testitapaus.</span><span class="sxs-lookup"><span data-stu-id="37974-322">In RSAT, select the **Prepare data to test processing of vendor's electronic payment** test case.</span></span>
2. <span data-ttu-id="37974-323">Valitse **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="37974-323">Select **Edit**.</span></span>
3. <span data-ttu-id="37974-324">Muuta avatun Microsoft Excel -työkirjan **Yleiset**-laskentataulukossa yrityksen koodiksi **GBSI**, sillä tätä yritystä käytetään testiä suorittamiseen.</span><span class="sxs-lookup"><span data-stu-id="37974-324">In the Microsoft Excel workbook that is opened, on the **General** worksheet, change the company code to **GBSI**, because this company will be used for test execution.</span></span>
4. <span data-ttu-id="37974-325">Valitse RSAT-työkalussa **Toimittajan maksujen testaaminen käyttämällä ER-muotoa BACS (UK)** -testitapaus.</span><span class="sxs-lookup"><span data-stu-id="37974-325">In RSAT, select the **Test processing of vendor payments by using ER format BACS (UK)** test case.</span></span>
5. <span data-ttu-id="37974-326">Valitse **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="37974-326">Select **Edit**.</span></span>
6. <span data-ttu-id="37974-327">Muuta avoimen Excel-työkirjan **Yleiset**-laskentataulukossa yrityksen koodiksi **GBSI**.</span><span class="sxs-lookup"><span data-stu-id="37974-327">In the Excel workbook that is opened, on the **General** worksheet, change the company code to **GBSI**.</span></span>
7. <span data-ttu-id="37974-328">Huomaa, että **ERFormatMappingRunLogTable**-laskentataulukon soluissa A:3 and C:3 niiden ER-virheenkorjauslokitaulun kenttien teksti, joilla tarkistettiin tuloksen ja perusrivin vertailun tulokset.</span><span class="sxs-lookup"><span data-stu-id="37974-328">On the **ERFormatMappingRunLogTable** worksheet, notice that cells A:3 and C:3 contain the text of the fields in the ER debug log table that are used to validate the results of the comparison of the output to the baseline.</span></span> <span data-ttu-id="37974-329">Näillä teksteillä arvioidaan testin suorittamisen aikana luotavia ER-virheenkorjauslokin tietueita.</span><span class="sxs-lookup"><span data-stu-id="37974-329">These texts will be used to evaluate ER debug log records that are created during test execution.</span></span>

    <span data-ttu-id="37974-330">![ERFormatMappingRunLogTable-laskentataulukko](media/GER-RSAT-RSAT-ExcelParameters.png "Näyttökuva ERFormatMappingRunLogTable-laskentataulukosta")</span><span class="sxs-lookup"><span data-stu-id="37974-330">![ERFormatMappingRunLogTable worksheet](media/GER-RSAT-RSAT-ExcelParameters.png "Screenshot of the ERFormatMappingRunLogTable worksheet")</span></span>

## <a name="run-the-tests-and-analyze-the-results"></a><span data-ttu-id="37974-331">Testien suorittaminen ja tulosten analysoiminen</span><span class="sxs-lookup"><span data-stu-id="37974-331">Run the tests and analyze the results</span></span>

### <a name="run-the-tests-in-rsat"></a><span data-ttu-id="37974-332">Testien suorittaminen RSAT-työkalussa</span><span class="sxs-lookup"><span data-stu-id="37974-332">Run the tests in RSAT</span></span>

1. <span data-ttu-id="37974-333">Valitse ladatut testit RSAT-työkalussa.</span><span class="sxs-lookup"><span data-stu-id="37974-333">In RSAT, select the loaded tests.</span></span>
2. <span data-ttu-id="37974-334">Valitse **Suorita**.</span><span class="sxs-lookup"><span data-stu-id="37974-334">Select **Run**.</span></span>

<span data-ttu-id="37974-335">Huomaa, että testitapaukset suoritetaan automaattisesti Finance and Operationsin selainta käyttämällä.</span><span class="sxs-lookup"><span data-stu-id="37974-335">Notice that test cases are automatically run in Finance and Operations by using a web browser.</span></span>

### <a name="analyze-the-results-of-test-execution"></a><span data-ttu-id="37974-336">Suoritetun testin tulosten analysoiminen</span><span class="sxs-lookup"><span data-stu-id="37974-336">Analyze the results of test execution</span></span>

<span data-ttu-id="37974-337">Suoritetun testin tulokset tallennetaan RSAT-työkaluun.</span><span class="sxs-lookup"><span data-stu-id="37974-337">The results of the test execution are stored in RSAT.</span></span> <span data-ttu-id="37974-338">Huomaa, että molemmat testit hyväksyttiin.</span><span class="sxs-lookup"><span data-stu-id="37974-338">Notice that both tests were passed.</span></span>

<span data-ttu-id="37974-339">![RSAT-työkalussa hyväksytyt testi](media/GER-RSAT-RSAT-Tests-Passed.png "Näyttökuva RSAT-työkalussa hyväksytyistä testeistä")</span><span class="sxs-lookup"><span data-stu-id="37974-339">![Tests that passed in RSAT](media/GER-RSAT-RSAT-Tests-Passed.png "Screenshot of tests that passed in RSAT")</span></span>

<span data-ttu-id="37974-340">Huomaa, että suoritetun testin tulokset lähetetään myös Azure DevOpsiin lisäanalyyseja varten.</span><span class="sxs-lookup"><span data-stu-id="37974-340">Notice that the results of the test execution are also sent to Azure DevOps so that you can do further analysis.</span></span>

<span data-ttu-id="37974-341">![Suoritetun testin tulokset Azure DevOpsissa](media/GER-RSAT-DevOps-Tests-Added.png "Näyttökuva suoritetun testin tuloksista Azure DevOpsiin")</span><span class="sxs-lookup"><span data-stu-id="37974-341">![Results of test execution in Azure DevOps](media/GER-RSAT-DevOps-Tests-Added.png "Screenshot of the results of test execution in Azure DevOps")</span></span>

### <a name="simulate-a-situation-where-tests-fail"></a><span data-ttu-id="37974-342">Testien epäonnistumistilanteen simulointi</span><span class="sxs-lookup"><span data-stu-id="37974-342">Simulate a situation where tests fail</span></span>

<span data-ttu-id="37974-343">Tämän testisarjan on epäonnistuttava, kun ainakin yksi luoduista tuloksista ei vastaa vastaavaa perusriviä.</span><span class="sxs-lookup"><span data-stu-id="37974-343">This test suite must fail when at least one of the generated outputs doesn't match the corresponding baseline.</span></span> <span data-ttu-id="37974-344">Tämä tilanne saadaan käyttämällä **BACS (UK)** -muodosta johdettua versiota, jonka luomassa maksutiedostossa on eri sisältö kuin vastaavalla perusrivillä.</span><span class="sxs-lookup"><span data-stu-id="37974-344">To achieve this situation, you can use your derived version of the **BACS (UK)** format that will generate a payment file that has different content than the corresponding baseline.</span></span> <span data-ttu-id="37974-345">Voit simuloida tilanteen käyttämällä samaa **BACS (UK)** -muotoa mutta vaihtamalla maksun summan käsitellyllä maksurivillä.</span><span class="sxs-lookup"><span data-stu-id="37974-345">To simulate this situation, you can use the same **BACS (UK)** format but change the payment amount on the processed payment line.</span></span>

1. <span data-ttu-id="37974-346">Avaa Finance and Operations selaimessa.</span><span class="sxs-lookup"><span data-stu-id="37974-346">Open Finance and Operations in a web browser.</span></span>
2. <span data-ttu-id="37974-347">Valitse **Ostoreskontra \> Maksut \> Maksukirjauskansio**.</span><span class="sxs-lookup"><span data-stu-id="37974-347">Go to **Accounts payable \> Payments \> Payment journal**.</span></span>
3. <span data-ttu-id="37974-348">Valitse **Rivit**.</span><span class="sxs-lookup"><span data-stu-id="37974-348">Select **Lines**.</span></span>
4. <span data-ttu-id="37974-349">Valitse ensin maksurivi ja sitten **Maksun tila \> Ei mitään**.</span><span class="sxs-lookup"><span data-stu-id="37974-349">Select the payment line, and then select **Payment status \> None**.</span></span>
5. <span data-ttu-id="37974-350">Muuta **Veloitus**-kentän arvo**1 000,00** arvoksi **2 000,00**.</span><span class="sxs-lookup"><span data-stu-id="37974-350">In the **Debit** field, change the value from **1,000.00** to **2,000.00**.</span></span>
6. <span data-ttu-id="37974-351">Tallenna muutokset valitsemalla **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="37974-351">Select **Save** to save your changes.</span></span>

### <a name="run-the-tests-in-rsat"></a><span data-ttu-id="37974-352">Testien suorittaminen RSAT-työkalussa</span><span class="sxs-lookup"><span data-stu-id="37974-352">Run the tests in RSAT</span></span>

1. <span data-ttu-id="37974-353">Valitse ladatut testit RSAT-työkalussa.</span><span class="sxs-lookup"><span data-stu-id="37974-353">In RSAT, select the loaded tests.</span></span>
2. <span data-ttu-id="37974-354">Valitse **Suorita**.</span><span class="sxs-lookup"><span data-stu-id="37974-354">Select **Run**.</span></span>

<span data-ttu-id="37974-355">Huomaa, että testitapaukset suoritetaan automaattisesti Finance and Operationsin selainta käyttämällä.</span><span class="sxs-lookup"><span data-stu-id="37974-355">Notice that test cases are automatically run in Finance and Operations by using a web browser.</span></span>

### <a name="analyze-the-results-of-test-execution"></a><span data-ttu-id="37974-356">Suoritetun testin tulosten analysoiminen</span><span class="sxs-lookup"><span data-stu-id="37974-356">Analyze the results of test execution</span></span>

<span data-ttu-id="37974-357">Suoritetun testin tulokset tallennetaan RSAT-työkaluun.</span><span class="sxs-lookup"><span data-stu-id="37974-357">The results of the test execution are stored in RSAT.</span></span> <span data-ttu-id="37974-358">Huomaa, että toinen testi epäonnistui toisen suorituksen aikana.</span><span class="sxs-lookup"><span data-stu-id="37974-358">Notice that the second test failed during the second execution.</span></span>

<span data-ttu-id="37974-359">![Epäonnistuneet testitulokset RSAT-työkalussa](media/GER-RSAT-RSAT-Tests-Failed.png "Näyttökuva epäonnistuneista testituloksista RSAT-työkalussa")</span><span class="sxs-lookup"><span data-stu-id="37974-359">![Failed test results in RSAT](media/GER-RSAT-RSAT-Tests-Failed.png "Screenshot of the failed test results in RSAT")</span></span>

<span data-ttu-id="37974-360">Huomaa, että suoritetun testin tulokset lähetetään myös Azure DevOpsiin lisäanalyyseja varten.</span><span class="sxs-lookup"><span data-stu-id="37974-360">Notice that the results of the test execution are also sent to Azure DevOps so that you can do further analysis.</span></span>

<span data-ttu-id="37974-361">![Epäonnistuneet testitulokset Azure DevOpsissa](media/GER-RSAT-DevOps-Tests-Failed.png "Näyttökuva epäonnistuneista testituloksista Azure DevOpsissa")</span><span class="sxs-lookup"><span data-stu-id="37974-361">![Failed test results in Azure DevOps](media/GER-RSAT-DevOps-Tests-Failed.png "Screenshot of the failed test results in Azure DevOps")</span></span>

<span data-ttu-id="37974-362">Pääset käyttämään kunkin testin tilaa.</span><span class="sxs-lookup"><span data-stu-id="37974-362">You can access the status of each test.</span></span> <span data-ttu-id="37974-363">Pääset käyttämään myös suorituslokia, joten voit analysoida virheen syyt.</span><span class="sxs-lookup"><span data-stu-id="37974-363">You can also access the execution log so that you analyze the reasons for any failure.</span></span> <span data-ttu-id="37974-364">Seuraavan kuvan suorituslokissa näkyy, että virhe johtui luodun maksutiedoston ja sen perusrivin sisällön välisestä erosta.</span><span class="sxs-lookup"><span data-stu-id="37974-364">In the following illustration, the execution log shows that the failure occurred because of the difference in content between the generated payment file and its baseline.</span></span>

<span data-ttu-id="37974-365">![Virheiden analysointiin Azure DevOpsissa käytettävä suoritusloki](media/GER-RSAT-DevOps-Tests-Failed-Log.png "Näyttökuva virheiden analysointiin Azure DevOpsissa käytettävä suoritusloki")</span><span class="sxs-lookup"><span data-stu-id="37974-365">![Execution log for analyzing failure in Azure DevOps](media/GER-RSAT-DevOps-Tests-Failed-Log.png "Screenshot of the execution log for analyzing failure in Azure DevOps")</span></span>

<span data-ttu-id="37974-366">Tämän vuoksi ER-muodon toimintaa voidaan arvioida osoitetulla tavalla automaattisesti käyttämällä RSAT-työkalua testausympäristönä ja tehtävän tallennustoimintoon perustuvia testitapauksia, jotka käyttävät ER-perusrivitoimintoa.</span><span class="sxs-lookup"><span data-stu-id="37974-366">Therefore, as you've seen, the functioning of any ER format can be evaluated automatically by using RSAT as the testing platform and by using Task recorder-based test cases that use the ER baseline feature.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="37974-367">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="37974-367">Additional resources</span></span>

- [<span data-ttu-id="37974-368">Tehtävän tallennus</span><span class="sxs-lookup"><span data-stu-id="37974-368">Task recorder</span></span>](../user-interface/task-recorder.md)
- [<span data-ttu-id="37974-369">Regression Suite Automation Tool</span><span class="sxs-lookup"><span data-stu-id="37974-369">Regression suite automation tool</span></span>](https://www.microsoft.com/download/details.aspx?id=57357)
- [<span data-ttu-id="37974-370">Käyttäjän hyväksyntätestauskirjastojen luominen tehtävätallenteiden ja BPM-määritysten avulla</span><span class="sxs-lookup"><span data-stu-id="37974-370">Create user acceptance test libraries by using task recordings and BPM</span></span>](../lifecycle-services/using-task-guides-and-bpm-to-create-user-acceptance-tests.md)
- [<span data-ttu-id="37974-371">Jatkuvaa koonnin ja testauksen automaatiota tukevien topologioiden käyttöönotto</span><span class="sxs-lookup"><span data-stu-id="37974-371">Deploy topologies that support continuous build and test automation</span></span>](../perf-test/continuous-build-test-automation.md)
- [<span data-ttu-id="37974-372">Luotuja raporttitulosten seuraaminen ja vertaaminen ER-perusarvoihin</span><span class="sxs-lookup"><span data-stu-id="37974-372">Trace generated report results and compare them with ER baseline values</span></span>](er-trace-reports-compare-baseline.md)
- [<span data-ttu-id="37974-373">ER-muodon päivittäminen ottamalla käyttöön sitä koskeva uusi perusversio</span><span class="sxs-lookup"><span data-stu-id="37974-373">Upgrade your ER format by adopting a new, base version of that format</span></span>](tasks/er-upgrade-format.md)
- [<span data-ttu-id="37974-374">Tuo ER-konfiguraatio Lifecycle Services -palvelusta</span><span class="sxs-lookup"><span data-stu-id="37974-374">Import ER configuration from Lifecycle Services</span></span>](tasks/er-import-configuration-lifecycle-services.md)
