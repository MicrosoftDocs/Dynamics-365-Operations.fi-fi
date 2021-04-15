---
title: Testauksen automatisointi sähköisen raportoinnin avulla
description: Tässä ohjeaiheessa käsitellään sähköisen raportointi- eli ER-kehyksen perustoiminnolla tapahtuvaa toimintojen automaattista testaamista.
author: NickSelin
ms.date: 07/02/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERFormatBaselineTable, ERFormatMappingRunLogTable, ERParameters
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.openlocfilehash: 0d029773d9aa59b27f80d2f670984a352e163122
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5743868"
---
# <a name="automate-testing-with-electronic-reporting"></a><span data-ttu-id="6954d-103">Testauksen automatisointi sähköisen raportoinnin avulla</span><span class="sxs-lookup"><span data-stu-id="6954d-103">Automate testing with Electronic reporting</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="6954d-104">Tässä ohjeaiheessa selitetään, miten sähköisen raportointi- eli ER-kehyksellä automatisoidaan joidenkin toimintojen testaus.</span><span class="sxs-lookup"><span data-stu-id="6954d-104">This topic explains how you can use the Electronic reporting (ER) framework to automate testing of some functionality.</span></span> <span data-ttu-id="6954d-105">Ohjeaiheen esimerkin avulla näytetään, miten toimittajan maksujen käsittely automatisoidaan.</span><span class="sxs-lookup"><span data-stu-id="6954d-105">The example in this topic shows how to automate the testing of vendor payment processing.</span></span>

<span data-ttu-id="6954d-106">Sovellus luo ER-kehyksen avulla maksutiedostot ja vastaavat asiakirjat toimittajan maksujen käsittelyn aikana.</span><span class="sxs-lookup"><span data-stu-id="6954d-106">The application uses the ER framework to generate payment files and corresponding documents during vendor payment processing.</span></span> <span data-ttu-id="6954d-107">ER-kehys sisältää tietomallin, mallien yhdistämismääritykset ja muoto-osia, jotka tukevat eri maksutyyppien maksujen käsittelyä ja eri muotoisten asiakirjojen luontia.</span><span class="sxs-lookup"><span data-stu-id="6954d-107">The ER framework consists of a data model, model mappings, and format components that support payment processing for different payment types and the generation of documents in different formats.</span></span> <span data-ttu-id="6954d-108">Nämä osat voi ladata Microsoft Dynamics Lifecycle Servicesistä (LCS) ja tuoda esiintymään.</span><span class="sxs-lookup"><span data-stu-id="6954d-108">These components can be downloaded from Microsoft Dynamics Lifecycle Services (LCS) and imported into the instance.</span></span>

<span data-ttu-id="6954d-109">Voit myös mukauttaa kutakin Microsoft-osaa ja käyttää sitä oman mukautetun osan perustana.</span><span class="sxs-lookup"><span data-stu-id="6954d-109">You also can customize each Microsoft component and use it as the basis of your own custom component.</span></span> <span data-ttu-id="6954d-110">Luomalla mukautetun version voit tehdä tiettyjä tarpeita tukevia muutoksia.</span><span class="sxs-lookup"><span data-stu-id="6954d-110">By creating a custom version, you can make changes that support specific requirements.</span></span> <span data-ttu-id="6954d-111">Voit esimerkiksi säätää ER-tietomallin ja ER-mallin yhdistämismäärityksen käyttämään asiakaskohtaista sovellustietoa tai voit muuttaa ER-muodon muokkaamaan luodun asiakirjan asettelua.</span><span class="sxs-lookup"><span data-stu-id="6954d-111">For example, you can adjust the ER data model and ER model mapping to access customer-specific application data, or you can change an ER format to modify the layout of a generated document.</span></span>

<span data-ttu-id="6954d-112">Voit käyttää mukautettuja ER-muotoja toimittajan maksuja luovien maksutiedostojen käsittelyyn. Voit käsitellä niillä myös tarkistusraportteja.</span><span class="sxs-lookup"><span data-stu-id="6954d-112">You can use customized ER formats to process payment files that generate vendor payments and also to process control reports.</span></span> <span data-ttu-id="6954d-113">Versiointia tuetaan ER-osissa.</span><span class="sxs-lookup"><span data-stu-id="6954d-113">Versioning is supported in ER components.</span></span> <span data-ttu-id="6954d-114">Microsoft voikin tämän vuoksi toimittaa toimittajan maksujen käsittelyn ER-ratkaisujen päivitetyt versiot, ja voit automaattisesti yhdistää päivitetyn version mukautettuun osaa pohjustamalla sen.</span><span class="sxs-lookup"><span data-stu-id="6954d-114">Therefore, Microsoft can provide updated versions of ER solutions for vendor payment processing, and you can automatically merge the updated version with your customized component by rebasing it.</span></span> <span data-ttu-id="6954d-115">Pohjustettu versio on kuitenkin testattava, jotta voidaan varmistaa, että toimii odotetulla tavalla.</span><span class="sxs-lookup"><span data-stu-id="6954d-115">However, you must test the rebased version to make sure that it works as you expect.</span></span>

<span data-ttu-id="6954d-116">ER-tietomallit ja ER-mallin yhdistämismääritykset ovat yleisiä useissa ER-muodoissa, joilla käsitellään eri tyyppisiä maksuja ja luodaan maa- tai aluekohtaisia maksuasiakirjoja.</span><span class="sxs-lookup"><span data-stu-id="6954d-116">ER data models and ER model mappings are common for many ER formats that are used to process payments of different types and to generate country/region-specific payment documents.</span></span> <span data-ttu-id="6954d-117">Tämän vuoksi käyttäjän hyväksynnän tai integroinnin testauksen automatisointi on erittäin toivottavaa, jolloin testaus voidaan tehdä automaattisesti useissa yrityksissä esimerkiksi siten, että kunkin kohdeyrityksen maa- tai aluekonteksti otetaan huomioon ja käytetään eri tietojoukkoja.</span><span class="sxs-lookup"><span data-stu-id="6954d-117">Therefore, it's highly desirable to automate user acceptance and integration testing so that it's automatically done in multiple companies but considers the country/region context of each target company, uses different datasets, and so on.</span></span>

<span data-ttu-id="6954d-118">Lisätietoja konfiguraation lähteestä vastaanotettuun muotoon perustuvan muodon mukautetun version luomisesta on kohteessa [ER Muodon päivittäminen ottamalla käyttöön kyseisen muodon uusi perusversio](./tasks/er-upgrade-format.md).</span><span class="sxs-lookup"><span data-stu-id="6954d-118">For more information about how to create a custom version of a format that is based on the format that you received from a configuration provider, see [ER Upgrade your format by adopting a new, base version of that format](./tasks/er-upgrade-format.md).</span></span>

## <a name="key-concepts"></a><span data-ttu-id="6954d-119">Avainkäsitteet</span><span class="sxs-lookup"><span data-stu-id="6954d-119">Key concepts</span></span>

<span data-ttu-id="6954d-120">Tehotoimintokäyttäjät voivat laatia käyttäjän hyväksyntä- ja integrointitestauksen lähdekoodia kirjoittamatta.</span><span class="sxs-lookup"><span data-stu-id="6954d-120">Functional power users can author user acceptance and integration testing without having to write source code.</span></span>

- <span data-ttu-id="6954d-121">Vertaa luotuja asiakirjoja pääversioihin ER-perustoiminnolla.</span><span class="sxs-lookup"><span data-stu-id="6954d-121">Use the ER baseline feature to compare generated documents to master copies.</span></span> <span data-ttu-id="6954d-122">Lisätietoja on kohdassa [Luotujen raporttitulosten seuraaminen ja vertaaminen perusarvoihin](er-trace-reports-compare-baseline.md)</span><span class="sxs-lookup"><span data-stu-id="6954d-122">For more information, see [Trace generated report results and compare them with baseline values](er-trace-reports-compare-baseline.md).</span></span>
- <span data-ttu-id="6954d-123">Tallenna testitapauksen tehtävän tallennustoiminnolla ja sisällytä perusarviointi.</span><span class="sxs-lookup"><span data-stu-id="6954d-123">Use Task recorder to record test cases, and include baseline assessment.</span></span> <span data-ttu-id="6954d-124">Lisätietoja on kohdassa [Tehtävän tallennustoiminnon resurssit](../user-interface/task-recorder.md).</span><span class="sxs-lookup"><span data-stu-id="6954d-124">For more information, see [Task recorder resources](../user-interface/task-recorder.md).</span></span>
- <span data-ttu-id="6954d-125">Ryhmitä tarvittavien testiskenaarioiden testitapaukset.</span><span class="sxs-lookup"><span data-stu-id="6954d-125">Group test cases for required test scenarios.</span></span> <span data-ttu-id="6954d-126">Lisätietoja kohdassa [Käyttäjän hyväksymistestien luominen ja automatisointi](../lifecycle-services/using-task-guides-and-bpm-to-create-user-acceptance-tests.md).</span><span class="sxs-lookup"><span data-stu-id="6954d-126">For more information, see [Create and automate user acceptance tests](../lifecycle-services/using-task-guides-and-bpm-to-create-user-acceptance-tests.md).</span></span>

    - <span data-ttu-id="6954d-127">Muodosta käyttäjän hyväksyntätestien kirjastoja LCS:n liiketoimintaprosessien mallintajalla (BPM).</span><span class="sxs-lookup"><span data-stu-id="6954d-127">Use Business process modeler (BPM) in LCS to make libraries for user acceptance tests.</span></span>
    - <span data-ttu-id="6954d-128">Luo Microsoft Azure DevOps Services (Azure DevOps)issa testisuunnitelma ja testisarjoja BPM-testikirjastojen avulla.</span><span class="sxs-lookup"><span data-stu-id="6954d-128">Use BPM test libraries to create a test plan and test suites in Microsoft Azure DevOps Services (Azure DevOps).</span></span>

<span data-ttu-id="6954d-129">Tehotoimintakäyttäjät voivat suorittaa käyttäjän hyväksyntä- ja integrointitestejä.</span><span class="sxs-lookup"><span data-stu-id="6954d-129">Functional power users can run user acceptance and integration tests.</span></span>

- <span data-ttu-id="6954d-130">Suorita toivotun testisarjan testitapaukset Regression Suite Automation Tool (RSAT) -työkalulla.</span><span class="sxs-lookup"><span data-stu-id="6954d-130">Use Regression suite automation tool (RSAT) to run test cases of the desired test suite.</span></span>
- <span data-ttu-id="6954d-131">Raportoi testauksen tulokset Azure DevOpsiin ja tutustu kyseisiin tuloksiin tässä palvelussa.</span><span class="sxs-lookup"><span data-stu-id="6954d-131">Report the results of the testing to Azure DevOps, and use this service to investigate those results.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="6954d-132">Edellytykset</span><span class="sxs-lookup"><span data-stu-id="6954d-132">Prerequisites</span></span>

<span data-ttu-id="6954d-133">Ennen kuin voit suorittaa tämän ohjeaiheen tehtäviä, seuraavien edellytysten on toteuduttava:</span><span class="sxs-lookup"><span data-stu-id="6954d-133">Before you can complete the tasks in this topic, you must complete the following prerequisites:</span></span>

- <span data-ttu-id="6954d-134">Ota käyttöön testauksen automatisointia tukeva topologia.</span><span class="sxs-lookup"><span data-stu-id="6954d-134">Deploy a topology that supports test automation.</span></span> <span data-ttu-id="6954d-135">Sinulla on oltava tämän topologiaesiintymän **Järjestelmänvalvoja**-rooli.</span><span class="sxs-lookup"><span data-stu-id="6954d-135">You must have access to the instance of this topology for the **System administrator** role.</span></span> <span data-ttu-id="6954d-136">Topologian on sisällettävä tässä esimerkissä käytettävät demotiedot.</span><span class="sxs-lookup"><span data-stu-id="6954d-136">This topology must contain the demo data that will be used in this example.</span></span> <span data-ttu-id="6954d-137">Lisätietoja on kohdassa [Jatkuvaa koonnin ja testauksen automaatiota tukevien topologioiden käyttöönotto ja käyttäminen](../perf-test/continuous-build-test-automation.md).</span><span class="sxs-lookup"><span data-stu-id="6954d-137">For more information, see [Deploy and use an environment that supports continuous build and test automation](../perf-test/continuous-build-test-automation.md).</span></span>
- <span data-ttu-id="6954d-138">Voit suorittaa käyttäjän hyväksyntä- ja integrointitestit automaattisesti asentamalla RSAT-työkalu käytössä olevaan topologiaan ja tekemällä tarvittavat määritykset.</span><span class="sxs-lookup"><span data-stu-id="6954d-138">To run user acceptance and integration tests automatically, you must install RSAT in the topology that you're using and configure it in the appropriate manner.</span></span> <span data-ttu-id="6954d-139">Lisätietoja RSAT:in asentamisesta ja määrittämisestä toimimaan Finance and Operations -sovellusten ja Azure DevOpsin kanssa on kohdassa [Regression Suite Automation Tool](https://www.microsoft.com/download/details.aspx?id=57357).</span><span class="sxs-lookup"><span data-stu-id="6954d-139">For information about how to install and configure RSAT and configure it to work with Finance and Operations apps and Azure DevOps, see [Regression Suite Automation Tool](https://www.microsoft.com/download/details.aspx?id=57357).</span></span> <span data-ttu-id="6954d-140">Ota huomioon työkalun käytön edellytykset.</span><span class="sxs-lookup"><span data-stu-id="6954d-140">Pay attention to the prerequisites for using the tool.</span></span> <span data-ttu-id="6954d-141">Seuraavassa kuvassa on esimerkki RSAT-asetuksista.</span><span class="sxs-lookup"><span data-stu-id="6954d-141">The following illustration shows an example of the RSAT settings.</span></span> <span data-ttu-id="6954d-142">Sinisen suorakulmion sisällä ovat parametrit, jotka määrittävät Azure DevOps -käytön.</span><span class="sxs-lookup"><span data-stu-id="6954d-142">The blue rectangle encloses the parameters that specify access to Azure DevOps.</span></span> <span data-ttu-id="6954d-143">Vihreän suorakulmion sisällä on parametrit, jotka määrittävät esiintymän käyttöoikeudet.</span><span class="sxs-lookup"><span data-stu-id="6954d-143">The green rectangle encloses the parameters that specify access to the instance.</span></span>

    <span data-ttu-id="6954d-144">![RSAT-asetukset](media/GER-Configure.png "Näyttökuva RSAT-asetukset-valintaikkunasta")</span><span class="sxs-lookup"><span data-stu-id="6954d-144">![RSAT settings](media/GER-Configure.png "Screenshot of the RSAT Settings dialog box")</span></span>

- <span data-ttu-id="6954d-145">Voit varmistaa testitapausten oikean suoritusjärjestyksen järjestämällä testitapaukset sarjoiksi. Voit kerätä tällä tavoin testauksen suorituslokeja lisäraportointia ja perehtymistä varten. Tätä varten tarvitaan käyttöönotetun topologian Azure DevOpsin käyttöoikeus.</span><span class="sxs-lookup"><span data-stu-id="6954d-145">To organize test cases in suites to help guarantee the correct execution sequence, so that you can collect logs of test executions for further reporting and investigation, you must have access to Azure DevOps from the deployed topology.</span></span>
- <span data-ttu-id="6954d-146">Tämän ohjeaiheen esimerkin suorittamista varten kannattaa ladata [RSAT-testien ER-käyttö](https://go.microsoft.com/fwlink/?linkid=874684).</span><span class="sxs-lookup"><span data-stu-id="6954d-146">To complete the example in this topic, we recommend that you download [ER usage for RSAT tests](https://go.microsoft.com/fwlink/?linkid=874684).</span></span> <span data-ttu-id="6954d-147">Tämä zip-tiedosto sisältää seuraavat tehtäväoppaat:</span><span class="sxs-lookup"><span data-stu-id="6954d-147">This zip file contains the following task guides:</span></span>

    | <span data-ttu-id="6954d-148">Sisältö</span><span class="sxs-lookup"><span data-stu-id="6954d-148">Content</span></span>                                           | <span data-ttu-id="6954d-149">Tiedoston nimi ja sijainti</span><span class="sxs-lookup"><span data-stu-id="6954d-149">File name and location</span></span> |
    |---------------------------------------------------|------------------------|
    | <span data-ttu-id="6954d-150">Tehtävätallennenäyte tietojen valmisteluun testausta varten</span><span class="sxs-lookup"><span data-stu-id="6954d-150">Sample task recording to prepare data for testing</span></span> | <span data-ttu-id="6954d-151">Prepare\\Recording.xml</span><span class="sxs-lookup"><span data-stu-id="6954d-151">Prepare\\Recording.xml</span></span> |
    | <span data-ttu-id="6954d-152">Tehtävätallennenäyte toimittajan maksujen käsittelyyn</span><span class="sxs-lookup"><span data-stu-id="6954d-152">Sample task recording to process vendor payment</span></span>   | <span data-ttu-id="6954d-153">Process\\Recording.xml</span><span class="sxs-lookup"><span data-stu-id="6954d-153">Process\\Recording.xml</span></span> |

## <a name="prepare-the-accounts-payable-module-to-process-vendor-payments"></a><span data-ttu-id="6954d-154">Ostoreskontra-moduulin valmisteleminen käsittelemään toimittajan maksuja</span><span class="sxs-lookup"><span data-stu-id="6954d-154">Prepare the Accounts payable module to process vendor payments</span></span>

1. <span data-ttu-id="6954d-155">Kirjaudu sisään esiintymääsi.</span><span class="sxs-lookup"><span data-stu-id="6954d-155">Sign in to your instance.</span></span>
2. <span data-ttu-id="6954d-156">Lataa seuraavat ER-konfiguraatiot LCS:stä.</span><span class="sxs-lookup"><span data-stu-id="6954d-156">Download the following ER configurations from LCS.</span></span> <span data-ttu-id="6954d-157">Ohjeet ovat kohdassa [ER Tuo konfiguraatio Lifecycle Services -palvelusta](./tasks/er-import-configuration-lifecycle-services.md).</span><span class="sxs-lookup"><span data-stu-id="6954d-157">For instructions, see [ER Import a configuration from Lifecycle Services](./tasks/er-import-configuration-lifecycle-services.md).</span></span>

    - <span data-ttu-id="6954d-158">**Maksumalli** ER-mallikonfiguraatio</span><span class="sxs-lookup"><span data-stu-id="6954d-158">**Payment model** ER model configuration</span></span>
    - <span data-ttu-id="6954d-159">**Maksumallin yhdistämismääritys 1611** ER-mallin yhdistämismääritys</span><span class="sxs-lookup"><span data-stu-id="6954d-159">**Payment model mapping 1611** ER model mapping configuration</span></span>
    - <span data-ttu-id="6954d-160">**BACS (UK)** ER-muotokonfiguraatio</span><span class="sxs-lookup"><span data-stu-id="6954d-160">**BACS (UK)** ER format configuration</span></span>

    <span data-ttu-id="6954d-161">![Sähköisen raportoinnin konfiguraatiot](media/GER-Configurations.png "Näyttökuva sähköisen raportoinnin Konfiguroinnit-sivusta")</span><span class="sxs-lookup"><span data-stu-id="6954d-161">![Electronic reporting configurations](media/GER-Configurations.png "Screenshot of the Configurations page in Electronic reporting")</span></span>

3. <span data-ttu-id="6954d-162">**GBSI**-demotietoyritys, sillä sen alue- tai maakonteksti on Iso-Britannia.</span><span class="sxs-lookup"><span data-stu-id="6954d-162">Select the **GBSI** demo data company, which has a country/region context in Great Britain.</span></span>
4. <span data-ttu-id="6954d-163">Määritä ostoreskontran parametrit:</span><span class="sxs-lookup"><span data-stu-id="6954d-163">Configure Accounts payable parameters:</span></span>

    1. <span data-ttu-id="6954d-164">Valitse **Ostoreskontra \> Maksun asetukset \> Maksutavat**.</span><span class="sxs-lookup"><span data-stu-id="6954d-164">Go to **Accounts payable \> Payment setup \> Methods of payment**.</span></span>
    2. <span data-ttu-id="6954d-165">Valitse maksutavaksi **Sähköinen**.</span><span class="sxs-lookup"><span data-stu-id="6954d-165">Select the **Electronic** method of payment.</span></span>
    3. <span data-ttu-id="6954d-166">Määritä valittu maksutapa käyttämään aiemmin toimittajan maksujen käsittelyä varten ladattua **BACS (UK)** -ER-muotoa:</span><span class="sxs-lookup"><span data-stu-id="6954d-166">Configure the selected method of payment so that it uses the **BACS (UK)** ER format that you downloaded earlier for vendor payment processing:</span></span>

        1. <span data-ttu-id="6954d-167">Määritä **Tiedostomuodot**-pikavälilehden **Yleinen sähköinen vientimuoto** -asetukseksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="6954d-167">On the **File formats** FastTab, set the **Generic electronic Export format** option to **Yes**.</span></span>
        2. <span data-ttu-id="6954d-168">Valitse **Vie muotokonfiguraatio** -kentässä **BACS (UK)**.</span><span class="sxs-lookup"><span data-stu-id="6954d-168">In the **Export format configuration** field, select **BACS (UK)**.</span></span>

    <span data-ttu-id="6954d-169">![Maksutavat-sivu](media/GER-APParameters.png "Näyttökuva Maksutavat-sivusta")</span><span class="sxs-lookup"><span data-stu-id="6954d-169">![Methods of payment page](media/GER-APParameters.png "Screenshot of the Methods of payment page")</span></span>

    > [!NOTE]
    > <span data-ttu-id="6954d-170">Jos sinulla on tämän ER-muodon johdettu versio, joka luotiin tukemaan mukautuksia, voit valita tämän konfiguraation **Sähköinen**-maksutavassa.</span><span class="sxs-lookup"><span data-stu-id="6954d-170">If you have the derived version of this ER format that was created to support customizations, you can select this configuration in the **Electronic** method of payment.</span></span>

5. <span data-ttu-id="6954d-171">Luo toimittajan maksuesimerkki:</span><span class="sxs-lookup"><span data-stu-id="6954d-171">Create an example vendor payment:</span></span>

    1. <span data-ttu-id="6954d-172">Valitse **Ostoreskontra \> Maksut \> Maksukirjauskansio**.</span><span class="sxs-lookup"><span data-stu-id="6954d-172">Go to **Accounts payable \> Payments \> Payment journal**.</span></span>
    2. <span data-ttu-id="6954d-173">Varmista, ettei maksukirjauskansioon ole tehty kirjausta.</span><span class="sxs-lookup"><span data-stu-id="6954d-173">Make sure that you haven't posted the payment journal.</span></span>

        <span data-ttu-id="6954d-174">![Maksukirjauskansio-sivu](media/GER-APJournal.png "Näyttökuva Maksukirjauskansio-sivusta")</span><span class="sxs-lookup"><span data-stu-id="6954d-174">![Payment journal page](media/GER-APJournal.png "Screenshot of the Payment journal page")</span></span>

    3. <span data-ttu-id="6954d-175">Valitse **Rivit** ja lisää rivi, jossa on seuraavat tiedot.</span><span class="sxs-lookup"><span data-stu-id="6954d-175">Select **Lines**, and enter a line that has the following information.</span></span>

        | <span data-ttu-id="6954d-176">Kenttä</span><span class="sxs-lookup"><span data-stu-id="6954d-176">Field</span></span>               | <span data-ttu-id="6954d-177">Esimerkkiarvo</span><span class="sxs-lookup"><span data-stu-id="6954d-177">Example value</span></span>   |
        |---------------------|-----------------|
        | <span data-ttu-id="6954d-178">Toimittajan nimi</span><span class="sxs-lookup"><span data-stu-id="6954d-178">Vendor name</span></span>         | <span data-ttu-id="6954d-179">GB\_SI\_000001</span><span class="sxs-lookup"><span data-stu-id="6954d-179">GB\_SI\_000001</span></span>  |
        | <span data-ttu-id="6954d-180">Veloitus</span><span class="sxs-lookup"><span data-stu-id="6954d-180">Debit</span></span>               | <span data-ttu-id="6954d-181">1,000.00</span><span class="sxs-lookup"><span data-stu-id="6954d-181">1,000.00</span></span>        |
        | <span data-ttu-id="6954d-182">Valuutta</span><span class="sxs-lookup"><span data-stu-id="6954d-182">Currency</span></span>            | <span data-ttu-id="6954d-183">GBP</span><span class="sxs-lookup"><span data-stu-id="6954d-183">GBP</span></span>             |
        | <span data-ttu-id="6954d-184">Vastatilityyppi</span><span class="sxs-lookup"><span data-stu-id="6954d-184">Offset account type</span></span> | <span data-ttu-id="6954d-185">Pankki</span><span class="sxs-lookup"><span data-stu-id="6954d-185">Bank</span></span>            |
        | <span data-ttu-id="6954d-186">Vastatili</span><span class="sxs-lookup"><span data-stu-id="6954d-186">Offset account</span></span>      | <span data-ttu-id="6954d-187">GBSI OPER</span><span class="sxs-lookup"><span data-stu-id="6954d-187">GBSI OPER</span></span>       |
        | <span data-ttu-id="6954d-188">Maksutapa</span><span class="sxs-lookup"><span data-stu-id="6954d-188">Method of payment</span></span>   | <span data-ttu-id="6954d-189">Sähköinen</span><span class="sxs-lookup"><span data-stu-id="6954d-189">Electronic</span></span>      |

    <span data-ttu-id="6954d-190">![Toimittajan maksut -sivu](media/GER-APJournalLines.png "Näyttökuva Toimittajan maksut -sivusta")</span><span class="sxs-lookup"><span data-stu-id="6954d-190">![Vendor payments page](media/GER-APJournalLines.png "Screenshot of the Vendor payments page")</span></span>

## <a name="prepare-the-er-framework-to-test-vendor-payment-processing"></a><span data-ttu-id="6954d-191">ER-kehyksen valmisteleminen toimittajan maksujen käsittelyn testaamiseen</span><span class="sxs-lookup"><span data-stu-id="6954d-191">Prepare the ER framework to test vendor payment processing</span></span>

### <a name="configure-er-parameters"></a><span data-ttu-id="6954d-192">Konfiguroi ER-parametrit</span><span class="sxs-lookup"><span data-stu-id="6954d-192">Configure ER parameters</span></span>

1. <span data-ttu-id="6954d-193">Valitse **Organisaation hallinto \> Sähköinen raportointi \> Sähköisen raportoinnin parametrit**.</span><span class="sxs-lookup"><span data-stu-id="6954d-193">Go to **Organization administration \> Electronic reporting \> Electronic reporting parameters**.</span></span>
2. <span data-ttu-id="6954d-194">Valitse **Liitteet**-välilehden **Perusrivi**-kentässä **Tiedosto** asiakirjatyypiksi, jota tiedostonhallinta- eli DM-kehys käyttää säilyttämään perustoimintoon DM-liitteinä liittyviä tiedostoja.</span><span class="sxs-lookup"><span data-stu-id="6954d-194">On the **Attachments** tab, in the **Baseline** field, select **File** as the document type that the Document management (DM) framework uses to keep documents that are related to the baseline feature as DM attachments.</span></span>

    <span data-ttu-id="6954d-195">![Sähköisen raportoinnin parametrit -sivu](media/GER-ERParameters.png "Näyttökuva Sähköisen raportoinnin parametrit -sivusta")</span><span class="sxs-lookup"><span data-stu-id="6954d-195">![Electronic reporting parameters page](media/GER-ERParameters.png "Screenshot of the Electronic reporting parameters page")</span></span>

### <a name="generate-baseline-copies-of-vendor-paymentrelated-documents"></a><span data-ttu-id="6954d-196">Toimittajan maksuihin liittyvien asiakirjojen peruskopioiden luominen</span><span class="sxs-lookup"><span data-stu-id="6954d-196">Generate baseline copies of vendor payment–related documents</span></span>

1. <span data-ttu-id="6954d-197">Valitse **Ostoreskontra \> Maksut \> Maksukirjauskansio**.</span><span class="sxs-lookup"><span data-stu-id="6954d-197">Go to **Accounts payable \> Payments \> Payment journal**.</span></span>
2. <span data-ttu-id="6954d-198">Valitse **Rivit**.</span><span class="sxs-lookup"><span data-stu-id="6954d-198">Select **Lines**.</span></span>
3. <span data-ttu-id="6954d-199">Valitse **Muodosta maksut**.</span><span class="sxs-lookup"><span data-stu-id="6954d-199">Select **Generate payments**.</span></span>
4. <span data-ttu-id="6954d-200">Valitse maksutavaksi **Sähköinen**.</span><span class="sxs-lookup"><span data-stu-id="6954d-200">Select the **Electronic** method of payment.</span></span>
5. <span data-ttu-id="6954d-201">Valitse **GBSI OPER** -pankkitili.</span><span class="sxs-lookup"><span data-stu-id="6954d-201">Select the **GBSI OPER** bank account.</span></span>
6. <span data-ttu-id="6954d-202">Määritä **Tulosta valvontaraportti** -asetukseksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="6954d-202">Set the **Print control report** option to **Yes**.</span></span>
7. <span data-ttu-id="6954d-203">Lataa tulos zip-tiedostona.</span><span class="sxs-lookup"><span data-stu-id="6954d-203">Download the generated output as a zip file.</span></span>
8. <span data-ttu-id="6954d-204">Avaa ladattu tiedosto.</span><span class="sxs-lookup"><span data-stu-id="6954d-204">Open the downloaded file.</span></span>
9. <span data-ttu-id="6954d-205">Pura seuraavat tiedostot ladatusta tiedostosta:</span><span class="sxs-lookup"><span data-stu-id="6954d-205">Extract following files from the downloaded file:</span></span>

    - <span data-ttu-id="6954d-206">**Tiedosto**-maksutiedosto tekstimuotoisena</span><span class="sxs-lookup"><span data-stu-id="6954d-206">**File** payment file in text format</span></span>
    - <span data-ttu-id="6954d-207">**ERVendOutPaymControlReport**-valvontaraporttitiedosto XLSX-muodossa</span><span class="sxs-lookup"><span data-stu-id="6954d-207">**ERVendOutPaymControlReport** control report file in XLSX format</span></span>

    <span data-ttu-id="6954d-208">![Puretut tiedostot](media/GER-APJournalProcessed.png "Näyttökuva puretuista tiedostonimissä Windowsin Resurssienhallinnassa")</span><span class="sxs-lookup"><span data-stu-id="6954d-208">![Extracted files](media/GER-APJournalProcessed.png "Screenshot of extracted file names in Windows explorer")</span></span>

### <a name="turn-on-the-er-baseline-feature"></a><span data-ttu-id="6954d-209">ER-perusrivitoiminnon ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="6954d-209">Turn on the ER baseline feature</span></span>

1. <span data-ttu-id="6954d-210">Siirry kohtaan **Organisaation hallinto \> Sähköinen raportointi \> Konfiguraatiot**.</span><span class="sxs-lookup"><span data-stu-id="6954d-210">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
2. <span data-ttu-id="6954d-211">Valitse toimintoruudun **Konfiguroinnit**-välilehdessä **Käyttäjän parametrit**.</span><span class="sxs-lookup"><span data-stu-id="6954d-211">On the Action Pane, on the **Configurations** tab, select **User parameters**.</span></span>
3. <span data-ttu-id="6954d-212">Määritä **Suorita virheenkorjaustila** -asetukseksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="6954d-212">Set the **Run in debug mode** option to **Yes**.</span></span>

<span data-ttu-id="6954d-213">**Suorita vianmääritystilassa** -parametrin ottaminen käyttöön pakottaa ER-kehyksen suorittamaan seuraavat toiminnot sen jälkeen, kun lähteviä asiakirjoja luova ER-muoto on suoritettu:</span><span class="sxs-lookup"><span data-stu-id="6954d-213">By turning on the **Run in debug mode** parameter, you force the ER framework to perform the following actions after the execution of any ER format that generates outgoing documents:</span></span>

1. <span data-ttu-id="6954d-214">Määritetään, määritettiinkö millekään suoritetun ER-muodon osalle perusrivi.</span><span class="sxs-lookup"><span data-stu-id="6954d-214">Determine whether a baseline was configured for any of components of the executed ER format.</span></span>
2. <span data-ttu-id="6954d-215">Määritetään, yksi kerrallaan soveltuuko määritetty perusrivi nykyiseen tilanteeseen (esimerkiksi kirjautuneen yrityksen yrityskoodi sekä tuloksen tiedostonimi ja tiedostotunniste).</span><span class="sxs-lookup"><span data-stu-id="6954d-215">Determine whether each configured baseline is applicable in the current conditions (company code of the signed-in company, file name and file name extension of the generated output, and so on).</span></span>
3. <span data-ttu-id="6954d-216">Kunkin soveltuvan perusrivin kohdalla tehdään seuraavat toiminnot:</span><span class="sxs-lookup"><span data-stu-id="6954d-216">For each applicable baseline, perform the following actions:</span></span>

    1. <span data-ttu-id="6954d-217">ER-muodon suorituksen aikana luotua tulosta verrataan vastaavaan perusriviin.</span><span class="sxs-lookup"><span data-stu-id="6954d-217">Compare the output that is generated during execution of the ER format with the corresponding baseline.</span></span>
    2. <span data-ttu-id="6954d-218">Vertailun tulokset tallennetaan ER-konfiguraatioiden virheenkorjauslokiin.</span><span class="sxs-lookup"><span data-stu-id="6954d-218">Store the results of the comparison in the ER configurations debug log.</span></span>

### <a name="configure-er-baselines-for-vendor-payment-processing"></a><span data-ttu-id="6954d-219">ER-perusrivien määrittäminen toimittajan maksujen käsittelyä varten</span><span class="sxs-lookup"><span data-stu-id="6954d-219">Configure ER baselines for vendor payment processing</span></span>

1. <span data-ttu-id="6954d-220">Siirry kohtaan **Organisaation hallinto \> Sähköinen raportointi \> Konfiguraatiot**.</span><span class="sxs-lookup"><span data-stu-id="6954d-220">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
2. <span data-ttu-id="6954d-221">Valitse **Perusrivit**.</span><span class="sxs-lookup"><span data-stu-id="6954d-221">Select **Baselines**.</span></span>
3. <span data-ttu-id="6954d-222">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="6954d-222">Select **New**.</span></span>
4. <span data-ttu-id="6954d-223">Valitse **Viite**-kentässä **BACS (UK)** -muoto.</span><span class="sxs-lookup"><span data-stu-id="6954d-223">In the **Reference** field, select the **BACS (UK)** format.</span></span>
5. <span data-ttu-id="6954d-224">Valitse **Liitteet**.</span><span class="sxs-lookup"><span data-stu-id="6954d-224">Select **Attachments**.</span></span>
6. <span data-ttu-id="6954d-225">Lisää uusi toimittajan maksutiedoston perusrivi:</span><span class="sxs-lookup"><span data-stu-id="6954d-225">Add a new baseline for the vendor payment file:</span></span>

    1. <span data-ttu-id="6954d-226">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="6954d-226">Select **New**.</span></span>
    2. <span data-ttu-id="6954d-227">Tallenna perusrivin tiedot valitsemalla **Tyyppi**-kentässä se **Tiedosto**-DM-asiakirjatyyppi, jonka määritit ER-parametreissa.</span><span class="sxs-lookup"><span data-stu-id="6954d-227">In the **Type** field, select the **File** DM document type that you configured in the ER parameters to store baseline artifacts.</span></span>
    3. <span data-ttu-id="6954d-228">Siirry valitsemaan paikallisesti tallennettu tekstimuotoinen **Tiedosto**-maksutiedosto.</span><span class="sxs-lookup"><span data-stu-id="6954d-228">Browse to select the locally saved **File** payment file in text format.</span></span>
    4. <span data-ttu-id="6954d-229">Kirjoita **Kuvaus**-kenttään **Maksun TXT-tiedosto**.</span><span class="sxs-lookup"><span data-stu-id="6954d-229">In the **Description** field, enter **Payment TXT file**.</span></span>

7. <span data-ttu-id="6954d-230">Lisää toimittajan maksujen seurantaraportin uusi perusrivi:</span><span class="sxs-lookup"><span data-stu-id="6954d-230">Add a new baseline for the control report for the vendor payment:</span></span>

    1. <span data-ttu-id="6954d-231">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="6954d-231">Select **New**.</span></span>
    2. <span data-ttu-id="6954d-232">Tallenna perusrivin tiedot valitsemalla **Tyyppi**-kentässä se **Tiedosto**-DM-asiakirjatyyppi, jonka määritit ER-parametreissa.</span><span class="sxs-lookup"><span data-stu-id="6954d-232">In the **Type** field, select the **File** DM document type that you configured in the ER parameters to store baseline artifacts.</span></span>
    3. <span data-ttu-id="6954d-233">Siirry valitsemaan paikallisesti tallennettu XLSX-muotoinen **ERVendOutPaymControlReport**-seurantatiedosto.</span><span class="sxs-lookup"><span data-stu-id="6954d-233">Browse to select the locally saved **ERVendOutPaymControlReport** control report file in XLSX format.</span></span>
    4. <span data-ttu-id="6954d-234">Kirjoita **Kuvaus**-kenttään **Maksun XLSX-seurantaraportti**.</span><span class="sxs-lookup"><span data-stu-id="6954d-234">In the **Description** field, enter **Payment XLSX control report**.</span></span>

    <span data-ttu-id="6954d-235">![Toimittajan maksutiedoston ja seurantaraportin perusrivit](media/GER-BaselineAttachments.png "Näyttökuva Konfiguroinnit-sivusta, jossa valittuna Maksun XLSX-seurantaraportti")</span><span class="sxs-lookup"><span data-stu-id="6954d-235">![Baselines for the vendor payment file and control report](media/GER-BaselineAttachments.png "Screenshot of the Configurations page with the Payment XLSX control report selected")</span></span>

8. <span data-ttu-id="6954d-236">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="6954d-236">Close the page.</span></span>
9. <span data-ttu-id="6954d-237">Määritä maksutiedoston perusrivi valitsemalla **Perusrivit**-pikavälilehdessä **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="6954d-237">On the **Baselines** FastTab, select **New** to configure a baseline for the payment file:</span></span>

    1. <span data-ttu-id="6954d-238">Anna rivin nimeksi **Maksutiedoston perusriviasetus**.</span><span class="sxs-lookup"><span data-stu-id="6954d-238">Name the line **Baseline setting for payment file**.</span></span>
    2. <span data-ttu-id="6954d-239">Valitse **Tiedosto-osan nimi**-kentässä **tiedosto**. Tätä perusriviä käytetään nyt ER-muodon tuloksessa, joka luo maksutiedoston BACS (UK) -tekstimuodossa.</span><span class="sxs-lookup"><span data-stu-id="6954d-239">In the **File component name** field, select **file** to apply this baseline to the ER format output that generates the payment file in BACS (UK) text format.</span></span>
    3. <span data-ttu-id="6954d-240">Valitsemalla **Yritykset**-kentässä **GBSI** voit käyttää tätä perusriviä, kun **BACS (UK)** -ER-muoto suoritetaan GBSI-yrityksessä.</span><span class="sxs-lookup"><span data-stu-id="6954d-240">In the **Companies** field, select **GBSI** to apply this baseline when the **BACS (UK)** ER format is run in the GBSI company.</span></span>
    4. <span data-ttu-id="6954d-241">Jos **Tiedostonimen peite** -kentässä annetaan **\*.TXT**, tätä perusriviä käytetään vain niissä **tiedosto**-muoto-osan tuloksissa, joiden tiedostotunniste on **.txt**.</span><span class="sxs-lookup"><span data-stu-id="6954d-241">In **File name mask** field, enter **\*.TXT** to apply this baseline only to outputs of the **file** format component that have the **.txt** file name extension.</span></span>
    5. <span data-ttu-id="6954d-242">Valitse **Perusrivi**-kentässä **Maksun TXT-tiedosto**, jolloin tätä perusriviä käytetään verratessa luotua tulosta.</span><span class="sxs-lookup"><span data-stu-id="6954d-242">In the **Baseline** field, select **Payment TXT file** so that this baseline is used for comparison with the generated output.</span></span>

10. <span data-ttu-id="6954d-243">Määritä seurantaraportin perusrivi valitsemalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="6954d-243">Select **New** to configure a baseline for the control report:</span></span>

    1. <span data-ttu-id="6954d-244">Anna rivin nimeksi **Seurantaraportin perusriviasetus**.</span><span class="sxs-lookup"><span data-stu-id="6954d-244">Name the line **Baseline setting for control report**.</span></span>
    2. <span data-ttu-id="6954d-245">Valitse **Tiedosto-osan nimi**-kentässä **ERVendOutPaymControlReport**. Tätä perusriviä käytetään nyt ER-muodon tuloksessa, joka luo seurantaraportin.</span><span class="sxs-lookup"><span data-stu-id="6954d-245">In the **File component name** field, select **ERVendOutPaymControlReport** to apply this baseline to the ER format output that generates the control report.</span></span>
    3. <span data-ttu-id="6954d-246">Valitsemalla **Yritykset**-kentässä **GBSI** voit käyttää tätä perusriviä, kun **BACS (UK)** -ER-muoto suoritetaan GBSI-yrityksessä.</span><span class="sxs-lookup"><span data-stu-id="6954d-246">In the **Companies** field, select **GBSI** to apply this baseline when the **BACS (UK)** ER format is run in the GBSI company.</span></span>
    4. <span data-ttu-id="6954d-247">Jos **Tiedostonimen peite** -kentässä annetaan **\*.XLSX**, tätä perusriviä käytetään vain niissä **ERVendOutPaymControlReport**-muoto-osan tuloksissa, joiden tiedostotunniste on **.xslx**.</span><span class="sxs-lookup"><span data-stu-id="6954d-247">In **File name mask** field, enter **\*.XLSX** to apply this baseline only to outputs of the **ERVendOutPaymControlReport** format component that have the **.xslx** file name extension.</span></span>
    5. <span data-ttu-id="6954d-248">Valitse **Perusrivi**-kentässä **Maksun XLSX-seurantaraportti**, jolloin tätä perusriviä käytetään verratessa luotua tulosta.</span><span class="sxs-lookup"><span data-stu-id="6954d-248">In the **Baseline** field, select **Payment XLSX control report** so that this baseline is used for comparison with the generated output.</span></span>

    <span data-ttu-id="6954d-249">![Konfigurointi-sivun Perusrivit-pikavälilehti](media/GER-BaselineRules.png "Näyttökuva Konfigurointi-sivun Perusrivit-pikavälilehdestä")</span><span class="sxs-lookup"><span data-stu-id="6954d-249">![Baselines FastTab on the Configurations page](media/GER-BaselineRules.png "Screenshot of the Baselines FastTab on the Configurations page")</span></span>

## <a name="record-tests-to-validate-vendor-payment-processing"></a><span data-ttu-id="6954d-250">Testien tallentaminen toimittajan maksujen käsittelyn tarkistamiseen</span><span class="sxs-lookup"><span data-stu-id="6954d-250">Record tests to validate vendor payment processing</span></span>

<span data-ttu-id="6954d-251">Voit tehotoimintakäyttäjänä tallentaa ovat toimittajan maksujen käsittelyn testivaiheet.</span><span class="sxs-lookup"><span data-stu-id="6954d-251">As a functional power user, you can record your own steps to test vendor payment processing.</span></span> <span data-ttu-id="6954d-252">Aiemmin ladattu **Prepare\\Recording.xml** -tehtävätallenne kannattaa toistaa (ja muokata tarvittaessa).</span><span class="sxs-lookup"><span data-stu-id="6954d-252">We recommend that you play (and edit, as required) the **Prepare\\Recording.xml** task recording that you downloaded earlier.</span></span> <span data-ttu-id="6954d-253">Tämän tallenteen avulla voi määrittää oikean tilan kaikille testitiedoille.</span><span class="sxs-lookup"><span data-stu-id="6954d-253">This recording is used to set all testing data to the correct state.</span></span> <span data-ttu-id="6954d-254">Kyseinen vaihe on pakolinen, sillä testaus voidaan tehdä useita kertoja ja jokaisen testin on käytettävä tietoja, joilla on sama tila.</span><span class="sxs-lookup"><span data-stu-id="6954d-254">That step is required because the testing can be done many times, and every test must use data that is in the same state.</span></span>

### <a name="reset-user-settings"></a><span data-ttu-id="6954d-255">Käyttäjäasetusten nollaaminen</span><span class="sxs-lookup"><span data-stu-id="6954d-255">Reset user settings</span></span>

1. <span data-ttu-id="6954d-256">Avaa oletuskoontinäyttö.</span><span class="sxs-lookup"><span data-stu-id="6954d-256">Open the default dashboard.</span></span>
2. <span data-ttu-id="6954d-257">Valitse **Asetukset**-painike (rataskuvake).</span><span class="sxs-lookup"><span data-stu-id="6954d-257">Select the **Settings** button (the gear symbol).</span></span>
3. <span data-ttu-id="6954d-258">Valitse **Käyttäjäasetukset**.</span><span class="sxs-lookup"><span data-stu-id="6954d-258">Select **User options**.</span></span>
4. <span data-ttu-id="6954d-259">Valitse **Käyttötiedot**.</span><span class="sxs-lookup"><span data-stu-id="6954d-259">Select **Usage data**.</span></span>
5. <span data-ttu-id="6954d-260">Valitse **Nollaa**.</span><span class="sxs-lookup"><span data-stu-id="6954d-260">Select **Reset**.</span></span>
6. <span data-ttu-id="6954d-261">Vahvista, että haluat nollata käyttötiedot valitsemalla **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="6954d-261">Select **Yes** to confirm that you want to reset usage data.</span></span>
7. <span data-ttu-id="6954d-262">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="6954d-262">Close the page.</span></span>

### <a name="record-the-steps-to-prepare-data-for-testing"></a><span data-ttu-id="6954d-263">Tiedostojen testauksen valmisteluvaiheiden tallentaminen</span><span class="sxs-lookup"><span data-stu-id="6954d-263">Record the steps to prepare data for testing</span></span>

1. <span data-ttu-id="6954d-264">Valitse **Asetukset**-painike (rataskuvake).</span><span class="sxs-lookup"><span data-stu-id="6954d-264">Select the **Settings** button (the gear symbol).</span></span>
2. <span data-ttu-id="6954d-265">Valitse **Tehtävän tallennustoiminto**.</span><span class="sxs-lookup"><span data-stu-id="6954d-265">Select **Task recorder**.</span></span>
3. <span data-ttu-id="6954d-266">Valitset **Toista tallenne**.</span><span class="sxs-lookup"><span data-stu-id="6954d-266">Select **Playback recording**.</span></span>
4. <span data-ttu-id="6954d-267">Valitse **Avaa tältä tietokoneelta**.</span><span class="sxs-lookup"><span data-stu-id="6954d-267">Select **Open from this PC**.</span></span>
5. <span data-ttu-id="6954d-268">Valitse **Selaa** ja tallenna sitten **Prepare\\Recording.xml**-tiedosto paikallisesti.</span><span class="sxs-lookup"><span data-stu-id="6954d-268">Select **Browse**, and select the locally save **Prepare\\Recording.xml** file.</span></span>
6. <span data-ttu-id="6954d-269">Valitse **Aloita**.</span><span class="sxs-lookup"><span data-stu-id="6954d-269">Select **Start**.</span></span>
7. <span data-ttu-id="6954d-270">Valitse **Toista seuraava odottava vaihe** niin monta kertaa, että kaikki tallenteen vaiheet on toistettu.</span><span class="sxs-lookup"><span data-stu-id="6954d-270">Keep selecting **Play next pending step** until all the steps in the recording have been played.</span></span>

<span data-ttu-id="6954d-271">Tämä tehtävätallenne suorittaa seuraavat toimenpiteet:</span><span class="sxs-lookup"><span data-stu-id="6954d-271">This task recording performs the following actions:</span></span>

1. <span data-ttu-id="6954d-272">Käsitellyn maksurivin tilaksi määritetään **Ei mitään**.</span><span class="sxs-lookup"><span data-stu-id="6954d-272">Set the status of the processed payment line to **None**.</span></span>

    <span data-ttu-id="6954d-273">![Tehtävätallenteen vaiheet 3–4](media/GER-Recording1Review1.png "Näyttökuva tehtävätallenteen vaiheista 3–4")</span><span class="sxs-lookup"><span data-stu-id="6954d-273">![Task recording steps 3 through 4](media/GER-Recording1Review1.png "Screenshot of task recording steps 3 through 4")</span></span>

2. <span data-ttu-id="6954d-274">Ota käyttäjän **Suorita virheenkorjaustilassa** -ER-parametri käyttöön.</span><span class="sxs-lookup"><span data-stu-id="6954d-274">Turn on the **Run in debug mode** ER user parameter.</span></span>

    <span data-ttu-id="6954d-275">![Tehtävätallenteen vaiheet 9–10](media/GER-Recording1Review2.png "Näyttökuva tehtävätallenteen vaiheista 9–10")</span><span class="sxs-lookup"><span data-stu-id="6954d-275">![Task recording steps 9 through 10](media/GER-Recording1Review2.png "Screenshot of task recording steps 9 through 10")</span></span>

3. <span data-ttu-id="6954d-276">Tyhjennä ER-virheenkorjausloki, joka sisältää luotujen tiedostojen ja perusrivien vertailutulokset.</span><span class="sxs-lookup"><span data-stu-id="6954d-276">Clean up the ER debug log that contains the results of the comparison of generated files to baselines.</span></span>

    <span data-ttu-id="6954d-277">![Tehtävätallenteen vaiheet 13–15](media/GER-Recording1Review3.png "Näyttökuva tehtävätallenteen vaiheista 13–15")</span><span class="sxs-lookup"><span data-stu-id="6954d-277">![Task recording steps 13 through 15](media/GER-Recording1Review3.png "Screenshot of task recording steps 13 through 15")</span></span>

### <a name="record-the-steps-to-test-vendor-payment-processing"></a><span data-ttu-id="6954d-278">Toimittajan maksujen käsittelyn testausvaiheiden tallentaminen</span><span class="sxs-lookup"><span data-stu-id="6954d-278">Record the steps to test vendor payment processing</span></span>

<span data-ttu-id="6954d-279">Aiemmin ladattu **Process\\Recording.xml** -tehtävätallenne kannattaa toistaa (ja muokata tarvittaessa).</span><span class="sxs-lookup"><span data-stu-id="6954d-279">We recommend that you play (and edit, as required) the **Process\\Recording.xml** task recording that you downloaded earlier.</span></span> <span data-ttu-id="6954d-280">Tätä tallennetta käytetään toimittajan maksujen käsittelemiseen sekä luotujen asiakirjojen ja vastaavien perusrivien vertailutulosten tarkistamiseen.</span><span class="sxs-lookup"><span data-stu-id="6954d-280">This recording is used to process vendor payments and validate the results of the comparison of generated documents to corresponding baselines.</span></span>

1. <span data-ttu-id="6954d-281">Valitse **Asetukset**-painike (rataskuvake).</span><span class="sxs-lookup"><span data-stu-id="6954d-281">Select the **Settings** button (the gear symbol).</span></span>
2. <span data-ttu-id="6954d-282">Valitse **Tehtävän tallennustoiminto**.</span><span class="sxs-lookup"><span data-stu-id="6954d-282">Select **Task recorder**.</span></span>
3. <span data-ttu-id="6954d-283">Valitset **Toista tallenne**.</span><span class="sxs-lookup"><span data-stu-id="6954d-283">Select **Playback recording**.</span></span>
4. <span data-ttu-id="6954d-284">Valitse **Avaa tältä tietokoneelta**.</span><span class="sxs-lookup"><span data-stu-id="6954d-284">Select **Open from this PC**.</span></span>
5. <span data-ttu-id="6954d-285">Valitse **Selaa** ja valitse sitten paikallisesti tallennettu **Process\\Recording.xml**-tiedosto.</span><span class="sxs-lookup"><span data-stu-id="6954d-285">Select **Browse**, and select the locally saved **Process\\Recording.xml** file.</span></span>
6. <span data-ttu-id="6954d-286">Valitse **Aloita**.</span><span class="sxs-lookup"><span data-stu-id="6954d-286">Select **Start**.</span></span>
7. <span data-ttu-id="6954d-287">Valitse **Toista seuraava odottava vaihe** niin monta kertaa, että kaikki tallenteen vaiheet on toistettu.</span><span class="sxs-lookup"><span data-stu-id="6954d-287">Keep selecting **Play next pending step** until all the steps in the recording have been played.</span></span>

<span data-ttu-id="6954d-288">Tämä tehtävätallenne suorittaa seuraavat toimenpiteet:</span><span class="sxs-lookup"><span data-stu-id="6954d-288">This task recording performs the following actions:</span></span>

1. <span data-ttu-id="6954d-289">Aloita toimittajan maksujen käsittely.</span><span class="sxs-lookup"><span data-stu-id="6954d-289">Start vendor payment processing.</span></span>
2. <span data-ttu-id="6954d-290">Valitse oikeat suorituksenaikaiset parametrit ja ota seurantaraportin luonti käyttöön.</span><span class="sxs-lookup"><span data-stu-id="6954d-290">Select the correct runtime parameters, and turn on generation of a control report.</span></span>

    <span data-ttu-id="6954d-291">![Tehtävätallenteen vaiheet 3–8](media/GER-Recording2Review1.png "Näyttökuva tehtävätallenteen vaiheista 3–8")</span><span class="sxs-lookup"><span data-stu-id="6954d-291">![Task recording steps 3 through 8](media/GER-Recording2Review1.png "Screenshot of task recording steps 3 through 8")</span></span>

3. <span data-ttu-id="6954d-292">Siirry ER-virheenkorjauslokiin kirjaamaan luotujen tulosten ja vastaavien perusrivien vertailutulokset.</span><span class="sxs-lookup"><span data-stu-id="6954d-292">Access the ER debug log to record the results of the comparison of generated outputs to corresponding baselines.</span></span>

    <span data-ttu-id="6954d-293">Vertailun tulokset näkyvät ER-virheenkorjauslokissa **Luotu teksti** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="6954d-293">In the ER debug log, the results of the comparison appear in the **Generated text** field.</span></span> <span data-ttu-id="6954d-294">**Muoto-osa**- ja **Lokimerkinnän aiheuttaneen muodon polku** -kentät viittaavat tiedosto-osaan, jolle luotua tulosta on verrattu perusriviin.</span><span class="sxs-lookup"><span data-stu-id="6954d-294">The **Format component** and **Format path that caused a log entry** fields refer to the file component for which the generated output has been compared to the baseline.</span></span>

    <span data-ttu-id="6954d-295">![Merkinnät Sähköisen raportoinnin ajolokit -sivulla](media/GER-ERDebugLog.png "Näyttökuva Sähköisen raportoinnin ajon lokit -sivusta")</span><span class="sxs-lookup"><span data-stu-id="6954d-295">![Entries on the Electronic reporting run logs page](media/GER-ERDebugLog.png "Screenshot of entries on the Electronic reporting run logs page")</span></span>

4. <span data-ttu-id="6954d-296">Nykyisen tuloksen ja perusrivin vertailu tallennetaan käyttämällä tehtävän tallennustoiminnon **Tarkista**-asetusta ja valitsemalla **Nykyinen arvo**.</span><span class="sxs-lookup"><span data-stu-id="6954d-296">The comparison of the current output to the baseline is recorded by using the **Validate** Task recorder option and selecting  **Current Value**.</span></span>

    <span data-ttu-id="6954d-297">![Tarkista-asetuksen käyttäminen nykyisen arvon vertailussa](media/GER-TRRecordValidation.png "Näyttökuva Tarkista-asetuksen käyttämisestä nykyisen arvon vertailussa")</span><span class="sxs-lookup"><span data-stu-id="6954d-297">![Using the Validate option for comparison with the current value](media/GER-TRRecordValidation.png "Screenshot of using the Validate option for comparison with the current value")</span></span>

    <span data-ttu-id="6954d-298">Seuraava kuva osoittaa, miltä tallennetut tarkistusvaiheet näyttävät tehtävätallenteessa.</span><span class="sxs-lookup"><span data-stu-id="6954d-298">The following illustration shows what the recorded validation steps look like in the task recording.</span></span>

    <span data-ttu-id="6954d-299">![Tehtävätallenteen vaiheet 13–15](media/GER-Recording2Review2.png "Näyttökuva tehtävätallenteen vaiheista 13–15")</span><span class="sxs-lookup"><span data-stu-id="6954d-299">![Task recording steps 13 and 15](media/GER-Recording2Review2.png "Screenshot of task recording steps 13 and 15")</span></span>

## <a name="add-the-recorded-tests-to-azure-devops"></a><span data-ttu-id="6954d-300">Tallennettujen testien lisääminen Azure DevOpsiin</span><span class="sxs-lookup"><span data-stu-id="6954d-300">Add the recorded tests to Azure DevOps</span></span>

1. <span data-ttu-id="6954d-301">Avaa Azure DevOps -ympäristö.</span><span class="sxs-lookup"><span data-stu-id="6954d-301">Open the Azure DevOps environment.</span></span>
2. <span data-ttu-id="6954d-302">Valitse projekti, jonka määritit RSAT-parametreissa [työkalua määritettäessä](#prerequisites).</span><span class="sxs-lookup"><span data-stu-id="6954d-302">Select the project that you defined in the RSAT parameters when you [configured the tool](#prerequisites).</span></span>
3. <span data-ttu-id="6954d-303">Valitse testisuunnitelma, jonka määritit RSAT-parametreissa [työkalua määritettäessä](#prerequisites).</span><span class="sxs-lookup"><span data-stu-id="6954d-303">Select the test plan that you defined in the RSAT parameters when you [configured the tool](#prerequisites).</span></span>
4. <span data-ttu-id="6954d-304">Luo uusi testitapaus valitulle testisuunnitelmalle:</span><span class="sxs-lookup"><span data-stu-id="6954d-304">Create a new test case for the selected test plan:</span></span>

    1. <span data-ttu-id="6954d-305">Anna testitapaukselle nimi **Tietojen valmistelu testaamaan toimittajan sähköisten maksujen käsittelyä**.</span><span class="sxs-lookup"><span data-stu-id="6954d-305">Name the test case **Prepare data to test processing of vendor's electronic payment**.</span></span>
    2. <span data-ttu-id="6954d-306">Liitä aiemmin ladattu **Recording.xml**-tiedosto **Prepare**-kansiosta.</span><span class="sxs-lookup"><span data-stu-id="6954d-306">Attach the **Recording.xml** file from the **Prepare** folder that you downloaded earlier.</span></span>

5. <span data-ttu-id="6954d-307">Luo uusi testitapaus valitulle testisuunnitelmalle:</span><span class="sxs-lookup"><span data-stu-id="6954d-307">Create a new test case for the selected test plan:</span></span>

    1. <span data-ttu-id="6954d-308">Anna testitapaukselle nimeksi **Toimittajan maksujen testaaminen käyttämällä ER-muotoa BACS (UK)**.</span><span class="sxs-lookup"><span data-stu-id="6954d-308">Name the test case **Test processing of vendor payments by using ER format BACS (UK)**.</span></span>
    2. <span data-ttu-id="6954d-309">Liitä aiemmin ladattu **Recording.xml**-tiedosto **Process**-kansiosta.</span><span class="sxs-lookup"><span data-stu-id="6954d-309">Attach the **Recording.xml** file from the **Process** folder that you downloaded earlier.</span></span>

    <span data-ttu-id="6954d-310">![Valitun testisuunnitelman uudet testitapaukset](media/GER-RSAT-DevOps-Tests-Passed.png "Näyttökuva valitun testisuunnitelman uusista testitapauksista")</span><span class="sxs-lookup"><span data-stu-id="6954d-310">![New test cases for the selected test plan](media/GER-RSAT-DevOps-Tests-Passed.png "Screenshot of the new test cases for the selected test plan")</span></span>

> [!NOTE]
> <span data-ttu-id="6954d-311">Varmista, että testit lisätään oikeassa suoritusjärjestyksessä.</span><span class="sxs-lookup"><span data-stu-id="6954d-311">Pay attention to the correct execution order of the tests that are added.</span></span>

## <a name="prepare-rsat-to-run-the-recorded-tests"></a><span data-ttu-id="6954d-312">RSAT-valmistelu suorittamaan tallennetut testit</span><span class="sxs-lookup"><span data-stu-id="6954d-312">Prepare RSAT to run the recorded tests</span></span>

### <a name="load-the-tests-from-azure-devops-to-rsat"></a><span data-ttu-id="6954d-313">Testien lataaminen Azure DevOpsista RSAT-työkaluun</span><span class="sxs-lookup"><span data-stu-id="6954d-313">Load the tests from Azure DevOps to RSAT</span></span>

1. <span data-ttu-id="6954d-314">Avaa paikallinen RSAT-sovellus nykyisessä topologiassa.</span><span class="sxs-lookup"><span data-stu-id="6954d-314">Open the local RSAT application in the current topology.</span></span>
2. <span data-ttu-id="6954d-315">Lataa tällä hetkellä Azure DevOpsissa sijaitsevat testit RSAT-työkaluun valitsemalla **Lataa**.</span><span class="sxs-lookup"><span data-stu-id="6954d-315">Select **Load** to load the tests that currently reside in Azure DevOps into RSAT.</span></span>

    <span data-ttu-id="6954d-316">![RSAT-työkaluun ladatut testit](media/GER-RSAT-RSAT-Tests-Loaded.png "Näyttökuva RSAT-työkaluun ladatuista testeistä")</span><span class="sxs-lookup"><span data-stu-id="6954d-316">![Tests loaded into RSAT](media/GER-RSAT-RSAT-Tests-Loaded.png "Screenshot of the tests loaded into RSAT")</span></span>

### <a name="create-automation-and-parameters-files"></a><span data-ttu-id="6954d-317">Automaatio- ja parametritiedostojen luominen</span><span class="sxs-lookup"><span data-stu-id="6954d-317">Create automation and parameters files</span></span>

1. <span data-ttu-id="6954d-318">Valitse RSAT-työkalussa Azure DevOpsista ladatut testit.</span><span class="sxs-lookup"><span data-stu-id="6954d-318">In RSAT, select the tests that you loaded from Azure DevOps.</span></span>
2. <span data-ttu-id="6954d-319">Luo RSAT-työkalun automaatio- ja parametritiedostot valitsemalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="6954d-319">Select **New** to create RSAT automation and parameters files.</span></span>

    <span data-ttu-id="6954d-320">![RSAT-työkalussa luodut automaatio- ja parametritiedostot](media/GER-RSAT-RSAT-Tests-Initiated.png "Näyttökuva RSAT-työkalussa luoduista automaatio- ja parametritiedostoista")</span><span class="sxs-lookup"><span data-stu-id="6954d-320">![RSAT automation and parameters files created in RSAT](media/GER-RSAT-RSAT-Tests-Initiated.png "Screenshot of the RSAT automation and parameters files created in RSAT")</span></span>

### <a name="modify-the-parameters-files"></a><span data-ttu-id="6954d-321">Parametritiedostojen muokkaaminen</span><span class="sxs-lookup"><span data-stu-id="6954d-321">Modify the parameters files</span></span>

1. <span data-ttu-id="6954d-322">Valitse RSAT-työkalussa **Tietojen valmistelu testaamaan toimittajan sähköisten maksujen käsittelyä** -testitapaus.</span><span class="sxs-lookup"><span data-stu-id="6954d-322">In RSAT, select the **Prepare data to test processing of vendor's electronic payment** test case.</span></span>
2. <span data-ttu-id="6954d-323">Valitse **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="6954d-323">Select **Edit**.</span></span>
3. <span data-ttu-id="6954d-324">Muuta avatun Microsoft Excel -työkirjan **Yleiset**-laskentataulukossa yrityksen koodiksi **GBSI**, sillä tätä yritystä käytetään testiä suorittamiseen.</span><span class="sxs-lookup"><span data-stu-id="6954d-324">In the Microsoft Excel workbook that is opened, on the **General** worksheet, change the company code to **GBSI**, because this company will be used for test execution.</span></span>
4. <span data-ttu-id="6954d-325">Valitse RSAT-työkalussa **Toimittajan maksujen testaaminen käyttämällä ER-muotoa BACS (UK)** -testitapaus.</span><span class="sxs-lookup"><span data-stu-id="6954d-325">In RSAT, select the **Test processing of vendor payments by using ER format BACS (UK)** test case.</span></span>
5. <span data-ttu-id="6954d-326">Valitse **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="6954d-326">Select **Edit**.</span></span>
6. <span data-ttu-id="6954d-327">Muuta avoimen Excel-työkirjan **Yleiset**-laskentataulukossa yrityksen koodiksi **GBSI**.</span><span class="sxs-lookup"><span data-stu-id="6954d-327">In the Excel workbook that is opened, on the **General** worksheet, change the company code to **GBSI**.</span></span>
7. <span data-ttu-id="6954d-328">Huomaa, että **ERFormatMappingRunLogTable**-laskentataulukon soluissa A:3 and C:3 niiden ER-virheenkorjauslokitaulun kenttien teksti, joilla tarkistettiin tuloksen ja perusrivin vertailun tulokset.</span><span class="sxs-lookup"><span data-stu-id="6954d-328">On the **ERFormatMappingRunLogTable** worksheet, notice that cells A:3 and C:3 contain the text of the fields in the ER debug log table that are used to validate the results of the comparison of the output to the baseline.</span></span> <span data-ttu-id="6954d-329">Näillä teksteillä arvioidaan testin suorittamisen aikana luotavia ER-virheenkorjauslokin tietueita.</span><span class="sxs-lookup"><span data-stu-id="6954d-329">These texts will be used to evaluate ER debug log records that are created during test execution.</span></span>

    <span data-ttu-id="6954d-330">![ERFormatMappingRunLogTable-laskentataulukko](media/GER-RSAT-RSAT-ExcelParameters.png "Näyttökuva ERFormatMappingRunLogTable-laskentataulukosta")</span><span class="sxs-lookup"><span data-stu-id="6954d-330">![ERFormatMappingRunLogTable worksheet](media/GER-RSAT-RSAT-ExcelParameters.png "Screenshot of the ERFormatMappingRunLogTable worksheet")</span></span>

## <a name="run-the-tests-and-analyze-the-results"></a><span data-ttu-id="6954d-331">Testien suorittaminen ja tulosten analysoiminen</span><span class="sxs-lookup"><span data-stu-id="6954d-331">Run the tests and analyze the results</span></span>

### <a name="run-the-tests-in-rsat"></a><span data-ttu-id="6954d-332">Testien suorittaminen RSAT-työkalussa</span><span class="sxs-lookup"><span data-stu-id="6954d-332">Run the tests in RSAT</span></span>

1. <span data-ttu-id="6954d-333">Valitse ladatut testit RSAT-työkalussa.</span><span class="sxs-lookup"><span data-stu-id="6954d-333">In RSAT, select the loaded tests.</span></span>
2. <span data-ttu-id="6954d-334">Valitse **Suorita**.</span><span class="sxs-lookup"><span data-stu-id="6954d-334">Select **Run**.</span></span>

<span data-ttu-id="6954d-335">Huomaa, että testitapaukset suoritetaan automaattisesti sovelluksessa selainta käyttämällä.</span><span class="sxs-lookup"><span data-stu-id="6954d-335">Notice that test cases are automatically run in the application by using a web browser.</span></span>

### <a name="analyze-the-results-of-test-execution"></a><span data-ttu-id="6954d-336">Suoritetun testin tulosten analysoiminen</span><span class="sxs-lookup"><span data-stu-id="6954d-336">Analyze the results of test execution</span></span>

<span data-ttu-id="6954d-337">Suoritetun testin tulokset tallennetaan RSAT-työkaluun.</span><span class="sxs-lookup"><span data-stu-id="6954d-337">The results of the test execution are stored in RSAT.</span></span> <span data-ttu-id="6954d-338">Huomaa, että molemmat testit hyväksyttiin.</span><span class="sxs-lookup"><span data-stu-id="6954d-338">Notice that both tests were passed.</span></span>

<span data-ttu-id="6954d-339">![RSAT-työkalussa hyväksytyt testit](media/GER-RSAT-RSAT-Tests-Passed.png "Näyttökuva RSAT-työkalussa hyväksytyistä testeistä")</span><span class="sxs-lookup"><span data-stu-id="6954d-339">![Tests that passed in RSAT](media/GER-RSAT-RSAT-Tests-Passed.png "Screenshot of tests that passed in RSAT")</span></span>

<span data-ttu-id="6954d-340">Huomaa, että suoritetun testin tulokset lähetetään myös Azure DevOpsiin lisäanalyyseja varten.</span><span class="sxs-lookup"><span data-stu-id="6954d-340">Notice that the results of the test execution are also sent to Azure DevOps so that you can do further analysis.</span></span>

<span data-ttu-id="6954d-341">![Suoritetun testin tulokset Azure DevOpsissa](media/GER-RSAT-DevOps-Tests-Added.png "Näyttökuva suoritetun testin tuloksista Azure DevOpsissa")</span><span class="sxs-lookup"><span data-stu-id="6954d-341">![Results of test execution in Azure DevOps](media/GER-RSAT-DevOps-Tests-Added.png "Screenshot of the results of test execution in Azure DevOps")</span></span>

### <a name="simulate-a-situation-where-tests-fail"></a><span data-ttu-id="6954d-342">Testien epäonnistumistilanteen simulointi</span><span class="sxs-lookup"><span data-stu-id="6954d-342">Simulate a situation where tests fail</span></span>

<span data-ttu-id="6954d-343">Tämän testisarjan on epäonnistuttava, kun ainakin yksi luoduista tuloksista ei vastaa vastaavaa perusriviä.</span><span class="sxs-lookup"><span data-stu-id="6954d-343">This test suite must fail when at least one of the generated outputs doesn't match the corresponding baseline.</span></span> <span data-ttu-id="6954d-344">Tämä tilanne saadaan käyttämällä **BACS (UK)** -muodosta johdettua versiota, jonka luomassa maksutiedostossa on eri sisältö kuin vastaavalla perusrivillä.</span><span class="sxs-lookup"><span data-stu-id="6954d-344">To achieve this situation, you can use your derived version of the **BACS (UK)** format that will generate a payment file that has different content than the corresponding baseline.</span></span> <span data-ttu-id="6954d-345">Voit simuloida tilanteen käyttämällä samaa **BACS (UK)** -muotoa mutta vaihtamalla maksun summan käsitellyllä maksurivillä.</span><span class="sxs-lookup"><span data-stu-id="6954d-345">To simulate this situation, you can use the same **BACS (UK)** format but change the payment amount on the processed payment line.</span></span>

1. <span data-ttu-id="6954d-346">Avaa sovellus ja valitse **Ostoreskontra \> Maksut \> Maksukirjauskansio**.</span><span class="sxs-lookup"><span data-stu-id="6954d-346">Open the application and go to **Accounts payable \> Payments \> Payment journal**.</span></span>
2. <span data-ttu-id="6954d-347">Valitse **Rivit**.</span><span class="sxs-lookup"><span data-stu-id="6954d-347">Select **Lines**.</span></span>
3. <span data-ttu-id="6954d-348">Valitse ensin maksurivi ja sitten **Maksun tila \> Ei mitään**.</span><span class="sxs-lookup"><span data-stu-id="6954d-348">Select the payment line, and then select **Payment status \> None**.</span></span>
4. <span data-ttu-id="6954d-349">Muuta **Veloitus**-kentän arvo **1 000,00** arvoksi **2 000,00**.</span><span class="sxs-lookup"><span data-stu-id="6954d-349">In the **Debit** field, change the value from **1,000.00** to **2,000.00**.</span></span>
5. <span data-ttu-id="6954d-350">Tallenna muutokset valitsemalla **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="6954d-350">Select **Save** to save your changes.</span></span>

### <a name="run-the-tests-in-rsat"></a><span data-ttu-id="6954d-351">Testien suorittaminen RSAT-työkalussa</span><span class="sxs-lookup"><span data-stu-id="6954d-351">Run the tests in RSAT</span></span>

1. <span data-ttu-id="6954d-352">Valitse ladatut testit RSAT-työkalussa.</span><span class="sxs-lookup"><span data-stu-id="6954d-352">In RSAT, select the loaded tests.</span></span>
2. <span data-ttu-id="6954d-353">Valitse **Suorita**.</span><span class="sxs-lookup"><span data-stu-id="6954d-353">Select **Run**.</span></span>

<span data-ttu-id="6954d-354">Huomaa, että testitapaukset suoritetaan automaattisesti sovelluksessa selainta käyttämällä.</span><span class="sxs-lookup"><span data-stu-id="6954d-354">Notice that test cases are automatically run in the application by using a web browser.</span></span>

### <a name="analyze-the-results-of-test-execution"></a><span data-ttu-id="6954d-355">Suoritetun testin tulosten analysoiminen</span><span class="sxs-lookup"><span data-stu-id="6954d-355">Analyze the results of test execution</span></span>

<span data-ttu-id="6954d-356">Suoritetun testin tulokset tallennetaan RSAT-työkaluun.</span><span class="sxs-lookup"><span data-stu-id="6954d-356">The results of the test execution are stored in RSAT.</span></span> <span data-ttu-id="6954d-357">Huomaa, että toinen testi epäonnistui toisen suorituksen aikana.</span><span class="sxs-lookup"><span data-stu-id="6954d-357">Notice that the second test failed during the second execution.</span></span>

<span data-ttu-id="6954d-358">![Epäonnistuneet testitulokset RSAT-työkalussa](media/GER-RSAT-RSAT-Tests-Failed.png "Näyttökuva epäonnistuneista testituloksista RSAT-työkalussa")</span><span class="sxs-lookup"><span data-stu-id="6954d-358">![Failed test results in RSAT](media/GER-RSAT-RSAT-Tests-Failed.png "Screenshot of the failed test results in RSAT")</span></span>

<span data-ttu-id="6954d-359">Huomaa, että suoritetun testin tulokset lähetetään myös Azure DevOpsiin lisäanalyyseja varten.</span><span class="sxs-lookup"><span data-stu-id="6954d-359">Notice that the results of the test execution are also sent to Azure DevOps so that you can do further analysis.</span></span>

<span data-ttu-id="6954d-360">![Epäonnistuneet testitulokset Azure DevOpsissa](media/GER-RSAT-DevOps-Tests-Failed.png "Näyttökuva epäonnistuneista testituloksista Azure DevOpsissa")</span><span class="sxs-lookup"><span data-stu-id="6954d-360">![Failed test results in Azure DevOps](media/GER-RSAT-DevOps-Tests-Failed.png "Screenshot of the failed test results in Azure DevOps")</span></span>

<span data-ttu-id="6954d-361">Pääset käyttämään kunkin testin tilaa.</span><span class="sxs-lookup"><span data-stu-id="6954d-361">You can access the status of each test.</span></span> <span data-ttu-id="6954d-362">Pääset käyttämään myös suorituslokia, joten voit analysoida virheen syyt.</span><span class="sxs-lookup"><span data-stu-id="6954d-362">You can also access the execution log so that you analyze the reasons for any failure.</span></span> <span data-ttu-id="6954d-363">Seuraavan kuvan suorituslokissa näkyy, että virhe johtui luodun maksutiedoston ja sen perusrivin sisällön välisestä erosta.</span><span class="sxs-lookup"><span data-stu-id="6954d-363">In the following illustration, the execution log shows that the failure occurred because of the difference in content between the generated payment file and its baseline.</span></span>

<span data-ttu-id="6954d-364">![Virheiden analysointiin Azure DevOpsissa käytettävä suoritusloki](media/GER-RSAT-DevOps-Tests-Failed-Log.png "Näyttökuva virheiden analysointiin Azure DevOpsissa käytettävästä suorituslokista")</span><span class="sxs-lookup"><span data-stu-id="6954d-364">![Execution log for analyzing failure in Azure DevOps](media/GER-RSAT-DevOps-Tests-Failed-Log.png "Screenshot of the execution log for analyzing failure in Azure DevOps")</span></span>

<span data-ttu-id="6954d-365">Tämän vuoksi ER-muodon toimintaa voidaan arvioida osoitetulla tavalla automaattisesti käyttämällä RSAT-työkalua testausympäristönä ja tehtävän tallennustoimintoon perustuvia testitapauksia, jotka käyttävät ER-perusrivitoimintoa.</span><span class="sxs-lookup"><span data-stu-id="6954d-365">Therefore, as you've seen, the functioning of any ER format can be evaluated automatically by using RSAT as the testing platform and by using Task recorder-based test cases that use the ER baseline feature.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6954d-366">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="6954d-366">Additional resources</span></span>

- [<span data-ttu-id="6954d-367">Tehtävän tallennustoiminnon resurssit</span><span class="sxs-lookup"><span data-stu-id="6954d-367">Task recorder resources</span></span>](../user-interface/task-recorder.md)
- [<span data-ttu-id="6954d-368">Regression Suite Automation Tool</span><span class="sxs-lookup"><span data-stu-id="6954d-368">Regression suite automation tool</span></span>](https://www.microsoft.com/download/details.aspx?id=57357)
- [<span data-ttu-id="6954d-369">Käyttäjän hyväksymistestien luominen ja automatisointi</span><span class="sxs-lookup"><span data-stu-id="6954d-369">Create and automate user acceptance tests</span></span>](../lifecycle-services/using-task-guides-and-bpm-to-create-user-acceptance-tests.md)
- [<span data-ttu-id="6954d-370">Jatkuvaa koonnin ja testauksen automaatiota tukevien topologioiden käyttöönotto ja käyttäminen</span><span class="sxs-lookup"><span data-stu-id="6954d-370">Deploy and use an environment that supports continuous build and test automation</span></span>](../perf-test/continuous-build-test-automation.md)
- [<span data-ttu-id="6954d-371">Luotuja raporttitulosten seuraaminen ja vertaaminen perusarvoihin</span><span class="sxs-lookup"><span data-stu-id="6954d-371">Trace generated report results and compare them with baseline values</span></span>](er-trace-reports-compare-baseline.md)
- [<span data-ttu-id="6954d-372">ER Muodon päivittäminen ottamalla käyttöön sitä koskeva uusi perusversio</span><span class="sxs-lookup"><span data-stu-id="6954d-372">ER Upgrade your format by adopting a new, base version of that format</span></span>](tasks/er-upgrade-format.md)
- [<span data-ttu-id="6954d-373">ER Tuo kokoonpano Lifecycle Services -palvelusta</span><span class="sxs-lookup"><span data-stu-id="6954d-373">ER Import a configuration from Lifecycle Services</span></span>](tasks/er-import-configuration-lifecycle-services.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]