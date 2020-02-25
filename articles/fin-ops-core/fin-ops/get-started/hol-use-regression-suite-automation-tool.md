---
title: Regression Suite Automation Tool -oppaan käyttäminen
description: Tässä ohjeaiheessa käsitellään Regression Suite Automation Tool (RSAT) -työkalun käyttämistä. Siinä käsitellään erilaisia toimintoja ja annetaan esimerkkejä edistyneestä komentosarjojen käytöstä.
author: kfend
manager: AnnBe
ms.date: 06/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 21761
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: AX 7.0.0, Operations
ms.openlocfilehash: 026d1d743b5150f152ef70aa642dcf6841a4e398
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025801"
---
# <a name="use-the-regression-suite-automation-tool-tutorial"></a><span data-ttu-id="35e05-104">Regression Suite Automation Tool -oppaan käyttäminen</span><span class="sxs-lookup"><span data-stu-id="35e05-104">Use the Regression suite automation tool tutorial</span></span>

[!include [banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="35e05-105">Lataa ja tallenna tämä ohje selaimen työkaluilla PDF-tiedostona.</span><span class="sxs-lookup"><span data-stu-id="35e05-105">Use your internet browser tools to download and save this page in pdf format.</span></span> 

<span data-ttu-id="35e05-106">Tässä oppaassa käsitellään yksityiskohtaisesti Regression Suite Automation Tool (RSAT) -työkalun lisätoimintoja. Se sisältää myös demon määrityksen ja siinä käsitellään strategiaa ja keskeisiä opittavia asioita.</span><span class="sxs-lookup"><span data-stu-id="35e05-106">This tutorial walks through some of the advanced features of the Regression suite automation tool (RSAT), includes a demo assignment, and describes strategy and key learning points.</span></span>

## <a name="features-of-rsattask-recorder"></a><span data-ttu-id="35e05-107">RSAT-työkalun ja tehtävän tallennustoiminnon toiminnot</span><span class="sxs-lookup"><span data-stu-id="35e05-107">Features of RSAT/Task recorder</span></span>

### <a name="validate-a-field-value"></a><span data-ttu-id="35e05-108">Kentän arvon tarkistaminen</span><span class="sxs-lookup"><span data-stu-id="35e05-108">Validate a field value</span></span>

<span data-ttu-id="35e05-109">Lisätietoja tästä toiminnosta on kohdassa [Uuden tarkistustoiminnon sisältävän tehtävätallenteen luominen](./hol-set-up-regression-suite-automation-tool.md#create-a-new-task-recording-that-has-a-validate-function).</span><span class="sxs-lookup"><span data-stu-id="35e05-109">For information about this feature, see the [Create a new task recording that has a Validate function](./hol-set-up-regression-suite-automation-tool.md#create-a-new-task-recording-that-has-a-validate-function).</span></span>

### <a name="saved-variable"></a><span data-ttu-id="35e05-110">Tallennettu muuttuja</span><span class="sxs-lookup"><span data-stu-id="35e05-110">Saved variable</span></span>

<span data-ttu-id="35e05-111">Lisätietoja tästä toiminnosta on kohdassa [Tallennetun muuttujan luominen muokkaamalla aiemmin luotua tehtävätallennetta](./hol-set-up-regression-suite-automation-tool.md#modify-an-existing-task-recording-to-create-a-saved-variable).</span><span class="sxs-lookup"><span data-stu-id="35e05-111">For information about this feature, see the [Modify an existing task recording to create a saved variable](./hol-set-up-regression-suite-automation-tool.md#modify-an-existing-task-recording-to-create-a-saved-variable).</span></span>

### <a name="derived-test-case"></a><span data-ttu-id="35e05-112">Johdettu testitapaus</span><span class="sxs-lookup"><span data-stu-id="35e05-112">Derived test case</span></span>

1. <span data-ttu-id="35e05-113">Avaa Regression Suite Automation Tool (RSAT) ja valitse molemmat kohdassa [Regression Suite Automation Tool -opetusohjelman määrittäminen ja asentaminen](./hol-set-up-regression-suite-automation-tool.md) luodut testitapaukset.</span><span class="sxs-lookup"><span data-stu-id="35e05-113">Open Regression suite automation tool (RSAT), and select both the test cases that you created in [Set up and install Regression suite automation tool tutorial](./hol-set-up-regression-suite-automation-tool.md).</span></span>
2. <span data-ttu-id="35e05-114">Valitse **Uusi \> Luo johdettu testitapaus**.</span><span class="sxs-lookup"><span data-stu-id="35e05-114">Select **New \> Create derived test case**.</span></span>

    ![Luo johdettu testitapaus -komento Uusi-valikossa](./media/use_rsa_tool_01.png)

3. <span data-ttu-id="35e05-116">Näyttöön avautuva sanoma ilmoittaa, että jokaiselle nykyisessä testisarjassa valitulle testitapauksella luodaan johdettu testitapaus ja että jokaisella johdetulla testitapauksella on oma Excelin parametritiedoston kopio.</span><span class="sxs-lookup"><span data-stu-id="35e05-116">You receive a message that states that a derived test case will be created for each selected test case in the current test suite, and that each derived test case will have its own copy of the Excel parameter file.</span></span> <span data-ttu-id="35e05-117">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="35e05-117">Select **OK**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="35e05-118">Suoritettava testitapaus käyttää päätestitapauksen tehtävätallennetta ja omaa Excelin parametritiedoston kopioita.</span><span class="sxs-lookup"><span data-stu-id="35e05-118">When you run a derived test case, it uses the task recording of its parent test case and its own copy of the Excel parameter file.</span></span> <span data-ttu-id="35e05-119">Tällä tavoin voit suorittaa saman testi eri parametreilla käyttämällä samaa tehtävätallennetta.</span><span class="sxs-lookup"><span data-stu-id="35e05-119">In this way, you can run the same test with different parameters, without having to maintain more than one task recording.</span></span> <span data-ttu-id="35e05-120">Johdetun testitapauksen ei tarvitse kuulua samaan testisarjaan kuin sen päätestitapaus.</span><span class="sxs-lookup"><span data-stu-id="35e05-120">A derived test case doesn't have to be part of the same test suite as its parent test case.</span></span>

    ![Viestiruutu](./media/use_rsa_tool_02.png)

    <span data-ttu-id="35e05-122">Kaksi muuta johdettua testitapausta luodaan ja niille valitaan **Johdettu?** -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="35e05-122">Two additional derived test cases are created, and the **Derived?** check box is selected for them.</span></span>

    ![Luodut johdetut testitapaukset](./media/use_rsa_tool_03.png)

    <span data-ttu-id="35e05-124">Johdettu testitapaus luodaan automaattisesti Azure DevOpsissa.</span><span class="sxs-lookup"><span data-stu-id="35e05-124">A derived test case is automatically created in Azure DevOps.</span></span> <span data-ttu-id="35e05-125">Se on **Luo uusi tuote** -testitapauksen alinimike ja siihen merkitään erityinen avainsana: **RSAT:DerivedTestSteps**.</span><span class="sxs-lookup"><span data-stu-id="35e05-125">It's a child item of the **Create a new product** test case and is tagged with a special keyword: **RSAT:DerivedTestSteps**.</span></span> <span data-ttu-id="35e05-126">Lisäksi nämä testitapaukset lisätään automaattisesti testisuunnitelmaan Azure DevOpsissa.</span><span class="sxs-lookup"><span data-stu-id="35e05-126">These test cases are also automatically added to the test plan in Azure DevOps.</span></span>

    ![RSAT: DerivedTestSteps-avainsana](./media/use_rsa_tool_04.png)

    > [!NOTE]
    > <span data-ttu-id="35e05-128">Jos luodut johdetut testitapaukset eivät jostain syytä ole oikeassa järjestyksessä, siirry Azure DevOps ja järjestä testisarjan testitapaukset uudelleen, jotta RSAT voi suorittaa ne oikeassa järjestyksessä.</span><span class="sxs-lookup"><span data-stu-id="35e05-128">If, for any reason, the derived test cases that are created aren't in the correct order, go to Azure DevOps, and reorder the test cases in the test suite, so that RSAT can run them in the correct order.</span></span>

4. <span data-ttu-id="35e05-129">Valitse ensin johdetut testitapaukset ja avaa sitten vastaavat Excelin parametritiedostot valitsemalla **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="35e05-129">Select the derived test cases, and then select **Edit** to open the corresponding Excel parameter files.</span></span>
5. <span data-ttu-id="35e05-130">Muokkaa näitä Excelin parametritiedostoja samalla tavalla kuin muokkasit päätiedostoja.</span><span class="sxs-lookup"><span data-stu-id="35e05-130">Edit these Excel parameter files in the same way that you edited the parent files.</span></span> <span data-ttu-id="35e05-131">Toisen sanoen varmista, että tuotetunnus on määritetty automaattisesti luotavaksi.</span><span class="sxs-lookup"><span data-stu-id="35e05-131">In other words, make sure that the product ID is set so that it's automatically generated.</span></span> <span data-ttu-id="35e05-132">Varmista myös, että tallennettu muuttuja kopioidaan soveltuviin kenttiin.</span><span class="sxs-lookup"><span data-stu-id="35e05-132">Also make sure that the saved variable is copied to the relevant fields.</span></span>
6. <span data-ttu-id="35e05-133">Päivitä Excelin parametritiedoston **Yleiset**-välilehdessä **Yritys**-kentän arvoksi **USSI**. Tällä tavoin johdetut testitapaukset suoritetaan eri yrityksen perusteella kuin päätestitapaus.</span><span class="sxs-lookup"><span data-stu-id="35e05-133">On the **General** tab of both Excel parameter files, update the value of the **Company** field to **USSI**, so that the derived test cases will be run against a different legal entity than the parent test case.</span></span> <span data-ttu-id="35e05-134">Jos haluat suorittaa testitapauksia tietyn käyttäjän (tai tiettyyn käyttäjään liitetyn roolin) osalta, voit päivittää **Testikäyttäjä**-kentän arvon.</span><span class="sxs-lookup"><span data-stu-id="35e05-134">To run the test cases against a specific user (or the role that is associated with a specific user), you can update the value of the **Test User** field.</span></span>
7. <span data-ttu-id="35e05-135">Valitse **Suorita** ja tarkista, että tuote on luotu sekä USMF-yrityksessä että USSI-yrityksessä.</span><span class="sxs-lookup"><span data-stu-id="35e05-135">Select **Run**, and validate that the product is created in both the USMF legal entity and the USSI legal entity.</span></span>

### <a name="validate-notifications"></a><span data-ttu-id="35e05-136">Ilmoitusten tarkistaminen</span><span class="sxs-lookup"><span data-stu-id="35e05-136">Validate notifications</span></span>

<span data-ttu-id="35e05-137">Tällä toiminnolla tarkistetaan, tapahtuiko toiminto.</span><span class="sxs-lookup"><span data-stu-id="35e05-137">This feature can be used to validate whether an action occurred.</span></span> <span data-ttu-id="35e05-138">Kun esimerkiksi tuotantotilaus luodaan, arvioidaan ja aloitetaan, sovellus ilmoittaa Tuotanto - käynnistys -sanomalla, että tuotantotilaus on aloitettu.</span><span class="sxs-lookup"><span data-stu-id="35e05-138">For example, when a production order is created, estimated, and then started, the app shows a "Production – Start" message to notify you that the production order has been started.</span></span>

![Tuotanto - käynnistys -ilmoitus](./media/use_rsa_tool_05.png)

<span data-ttu-id="35e05-140">Voit tarkistaa tämän sanoman RSAT-työkalussa etsimällä kyseisen tallenteen antamalla sanoman tekstin Excelin parametritiedoston **Viestin tarkistus**-välilehdessä.</span><span class="sxs-lookup"><span data-stu-id="35e05-140">You can validate this message through RSAT by entering the message text on the **MessageValidation** tab of the Excel parameter file for the appropriate recording.</span></span>

![Viestin tarkistus -välilehti](./media/use_rsa_tool_06.png)

<span data-ttu-id="35e05-142">Kun testitapaus on suoritettu, Excelin parametritiedostoa verrataan näytettävään sanomaan.</span><span class="sxs-lookup"><span data-stu-id="35e05-142">After the test case is run, the message in the Excel parameter file is compared to the message that is shown.</span></span> <span data-ttu-id="35e05-143">Jos sanomat eivät vastaa toisiaan, testitapaus epäonnistuu.</span><span class="sxs-lookup"><span data-stu-id="35e05-143">If the messages don't match, the test case will fail.</span></span>

> [!NOTE]
> <span data-ttu-id="35e05-144">Voit antaa Excelin parametritiedoston **Viestitarkistus**-välilehdessä useita sanomia.</span><span class="sxs-lookup"><span data-stu-id="35e05-144">You can enter more than one message on the **MessageValidation** tab in the Excel parameter file.</span></span> <span data-ttu-id="35e05-145">Sanomat voivat myös olla virhe- tai varoitussanomia ilmoitussanomien sijaan.</span><span class="sxs-lookup"><span data-stu-id="35e05-145">The messages also can be error or warning messages instead of informational messages.</span></span>

### <a name="validate-values-by-using-operators"></a><span data-ttu-id="35e05-146">Arvojen tarkistaminen operaattorien avulla</span><span class="sxs-lookup"><span data-stu-id="35e05-146">Validate values by using operators</span></span>

<span data-ttu-id="35e05-147">RSAT-työkalun edellisissä versioissa arvot voitiin vahvistaa vain, jos tarkistusarvo ja odotettu arvo olivat samat.</span><span class="sxs-lookup"><span data-stu-id="35e05-147">In previous versions of RSAT, you could validate values only if a control value equaled an expected value.</span></span> <span data-ttu-id="35e05-148">Uudella toiminnolla voi tarkistaa, että muuttuja ei ole yhtä suuri kuin tai on pienempi tai suurempi kuin määritetty arvo.</span><span class="sxs-lookup"><span data-stu-id="35e05-148">The new feature lets you validate that a variable isn't equal to, is less than, or is more than a specified value.</span></span>

- <span data-ttu-id="35e05-149">Avaa tällä toiminnolla **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config**-tiedosto RSAT-asennuskansiossa (esimerkiksi kansiossa **C:\\Program Files (x86)\\Regression Suite Automation Tool**) ja muuta seuraavan elementin arvo **epätosi** arvoksi **tosi**.</span><span class="sxs-lookup"><span data-stu-id="35e05-149">To use this feature, open the **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** file under the RSAT installation folder (for example, **C:\\Program Files (x86)\\Regression Suite Automation Tool**), and change the value in the following element from **false** to **true**.</span></span>

    ```xml
    <add key="AddOperatorFieldsToExcelValidation" value="false" />
    ```

    <span data-ttu-id="35e05-150">Uusi **Operaattori**-kenttä tulee näkyviin Excelin parametritiedostossa.</span><span class="sxs-lookup"><span data-stu-id="35e05-150">In the Excel parameter file, a new **Operator** field appears.</span></span>

    > [!NOTE]
    > <span data-ttu-id="35e05-151">Jos olet käyttänyt vanhaa RSAT-versiota, uudet Excelin parametritiedostot on luotava.</span><span class="sxs-lookup"><span data-stu-id="35e05-151">If you've been using an older version of RSAT, you must generate new Excel parameter files.</span></span>

    ![Operaattorikenttä](./media/use_rsa_tool_07.png)

<span data-ttu-id="35e05-153">Seuraava esimerkki osoittaa, miten tällä toiminnolla tarkistetaan, onko varastosaldo suurempi kuin 0 (nolla).</span><span class="sxs-lookup"><span data-stu-id="35e05-153">The following example shows how you can use this feature to validate whether the on-hand inventory is more than 0 (zero).</span></span>

1. <span data-ttu-id="35e05-154">Luo demotietojen **USMF**-yrityksessä tehtävätallenne, jossa on seuraavat vaiheet:</span><span class="sxs-lookup"><span data-stu-id="35e05-154">In the demo data in the **USMF** company, create a task recording that has the following steps:</span></span>

    1. <span data-ttu-id="35e05-155">Mene **Tuotetietojen hallinta \> Tuotteet \> Vapautetut tuotteet**.</span><span class="sxs-lookup"><span data-stu-id="35e05-155">Go to **Product information management \> Products \> Released products**.</span></span>
    2. <span data-ttu-id="35e05-156">Käytä pikasuodatinta tietueiden etsimiseen.</span><span class="sxs-lookup"><span data-stu-id="35e05-156">Use the Quick Filter to find records.</span></span> <span data-ttu-id="35e05-157">Voit esimerkiksi suodattaa **Nimiketunnus**-kenttää arvolla **1000**.</span><span class="sxs-lookup"><span data-stu-id="35e05-157">For example, filter on a value of **1000** for the **Item number** field.</span></span>
    3. <span data-ttu-id="35e05-158">Valitse **Käytettävissä oleva varasto**.</span><span class="sxs-lookup"><span data-stu-id="35e05-158">Select **On-hand inventory**.</span></span>
    4. <span data-ttu-id="35e05-159">Käytä pikasuodatinta tietueiden etsimiseen.</span><span class="sxs-lookup"><span data-stu-id="35e05-159">Use the Quick Filter to find records.</span></span> <span data-ttu-id="35e05-160">Voit esimerkiksi suodattaa **Toimipaikka**-kenttää arvolla **1**.</span><span class="sxs-lookup"><span data-stu-id="35e05-160">For example, filter on a value of **1** for the **Site** field.</span></span>
    5. <span data-ttu-id="35e05-161">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="35e05-161">In the list, mark the selected row.</span></span>
    6. <span data-ttu-id="35e05-162">Tarkista, että **Yhteensä käytettävissä** -kentän arvo on **411,0000000000000000**.</span><span class="sxs-lookup"><span data-stu-id="35e05-162">Validate that the value of the **Total available** field is **411.0000000000000000**.</span></span>

2. <span data-ttu-id="35e05-163">Tallenna tehtävätallenne LCS:n BPM-kirjastoon ja synkronoi se Azure DevOpsiin.</span><span class="sxs-lookup"><span data-stu-id="35e05-163">Save the task recording to the BPM library in LCS, and sync it to Azure DevOps.</span></span>
3. <span data-ttu-id="35e05-164">Lisää testitapaus testisuunnitelmaan ja lataa testitapaus RSAT-työkaluun.</span><span class="sxs-lookup"><span data-stu-id="35e05-164">Add the test case to the test plan, and load the test case into RSAT.</span></span>
4. <span data-ttu-id="35e05-165">Avaa Excelin parametritiedosto.</span><span class="sxs-lookup"><span data-stu-id="35e05-165">Open the Excel parameter file.</span></span> <span data-ttu-id="35e05-166">**Inventonhandimitem**-välilehdessä on **Tarkista InventOnhandItem** -osa, jossa on **Operaattori**-kenttä.</span><span class="sxs-lookup"><span data-stu-id="35e05-166">On the **InventOnhandItem** tab, you will see a **Validate InventOnhandItem** section that includes an **Operator** field.</span></span>

    ![Operaattorikenttä](./media/use_rsa_tool_08.png)

5. <span data-ttu-id="35e05-168">Jos haluat tarkistaa, että varastosaldo on aina yli 0, muuta **Arvo**-kentän arvo **411** arvoksi **0** ja **Operaattori**-kentän yhtä suuri kuin -merkki (**=**) suurempi kuin -merkiksi (**\>**).</span><span class="sxs-lookup"><span data-stu-id="35e05-168">To validate whether the inventory on-hand will always be more than 0, change the value of the **Value** field from **411** to **0** and the value of the **Operator** field from an equal sign (**=**) to a greater than sign (**\>**).</span></span>

    ![Arvo-ja Operaattori-kenttien muuttuneet arvot](./media/use_rsa_tool_09.png)

6. <span data-ttu-id="35e05-170">Tallenna ja sulje Excelin parametritiedosto.</span><span class="sxs-lookup"><span data-stu-id="35e05-170">Save and close the Excel parameter file.</span></span>
7. <span data-ttu-id="35e05-171">Tallenna Excelin parametritiedostoon tehdyt muutokset Azure DevOpsiin valitsemalla **Lataa palvelimeen**.</span><span class="sxs-lookup"><span data-stu-id="35e05-171">Select **Upload** to save the changes that you made to the Excel parameter file to Azure DevOps.</span></span>

<span data-ttu-id="35e05-172">Huomaa, että jos tietyn nimikkeen **Yhteensä käytettävissä** -kentän arvo varastossa on suurempi kuin 0 (nolla), testi hyväksytään todellisen varastosaldon arvosta riippumatta.</span><span class="sxs-lookup"><span data-stu-id="35e05-172">Now, if the value of the **Total Available** field for the specified item in inventory is more than 0 (zero), tests will pass, regardless of the actual on-hand inventory value.</span></span>

### <a name="generator-logs"></a><span data-ttu-id="35e05-173">Generaattorin lokit</span><span class="sxs-lookup"><span data-stu-id="35e05-173">Generator logs</span></span>

<span data-ttu-id="35e05-174">Tämä toiminto luo kansion, joka sisältää suoritettujen testitapausten lokit.</span><span class="sxs-lookup"><span data-stu-id="35e05-174">This feature creates a folder that contains the logs of the test cases that have been run.</span></span>

- <span data-ttu-id="35e05-175">Avaa tällä toiminnolla **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config**-tiedosto RSAT-asennuskansiossa (esimerkiksi kansiossa **C:\\Program Files (x86)\\Regression Suite Automation Tool**) ja muuta seuraavan elementin arvo **epätosi** arvoksi **tosi**.</span><span class="sxs-lookup"><span data-stu-id="35e05-175">To use this feature, open the **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** file under the RSAT installation folder (for example, **C:\\Program Files (x86)\\Regression Suite Automation Tool**), and change the value in the following element from **false** to **true**.</span></span>

    ```xml
    <add key="LogGeneration" value="false" />
    ```

<span data-ttu-id="35e05-176">Suoritettujen testitapausten lokitiedostot sijaitsevat kansiossa **C:\\Käyttäjät\\\<Käyttäjänimi\>\\AppData\\Roaming\\regressionTool\\generatorLogs**.</span><span class="sxs-lookup"><span data-stu-id="35e05-176">After the test cases are run, you can find the log files under **C:\\Users\\\<Username\>\\AppData\\Roaming\\regressionTool\\generatorLogs**.</span></span>

![GeneratorLogs-kansio](./media/use_rsa_tool_10.png)

> [!NOTE]
> <span data-ttu-id="35e05-178">Jos testitapauksia oli luotu ennen .config-tiedoston arvon muuttamista, kyseisten testitapausten lokeja ei luoda, ennen kuin uudet testin suoritustiedostot luodaan.</span><span class="sxs-lookup"><span data-stu-id="35e05-178">If there were existing test cases before you changed the value in the .config file, logs won't be generated for those test cases until you generate new test execution files.</span></span>
> 
> ![Uusi-valikon Luo vain testin suoritustiedostot -komento](./media/use_rsa_tool_11.png)

### <a name="snapshot"></a><span data-ttu-id="35e05-180">Tilannevedos</span><span class="sxs-lookup"><span data-stu-id="35e05-180">Snapshot</span></span>

<span data-ttu-id="35e05-181">Tämä toiminto ottaa näyttökuvat tehtävätallenteen aikana suoritetuista vaiheista.</span><span class="sxs-lookup"><span data-stu-id="35e05-181">This feature takes screenshots of the steps that were performed during task recording.</span></span>

- <span data-ttu-id="35e05-182">Avaa tällä toiminnolla **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config**-tiedosto RSAT-asennuskansiossa (esimerkiksi kansiossa **C:\\Program Files (x86)\\Regression Suite Automation Tool**) ja muuta seuraavan elementin arvo **epätosi** arvoksi **tosi**.</span><span class="sxs-lookup"><span data-stu-id="35e05-182">To use this feature, open the **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** file under the RSAT installation folder (for example, **C:\\Program Files (x86)\\Regression Suite Automation Tool**), and change the value of the following element from **false** to **true**.</span></span>

    ```xml
    <add key="VerboseSnapshotsEnabled" value="false" />
    ```

<span data-ttu-id="35e05-183">Jokaiselle suoritettavalle testitapaukselle luodaan erillinen kansio kohdassa **C:\\Käyttäjät\\\<Käyttäjänimi\>\\AppData\\Roaming\\regressionTool\\playback**.</span><span class="sxs-lookup"><span data-stu-id="35e05-183">Under **C:\\Users\\\<Username\>\\AppData\\Roaming\\regressionTool\\playback**, a separate folder is created for each test case that is run.</span></span>

![Testitapauksen tilannevedoskansio](./media/use_rsa_tool_12.png)

<span data-ttu-id="35e05-185">Kussakin näistä kansioista on tilannevedoksia testitapausten suorittamisen aikana suoritetuista vaiheista.</span><span class="sxs-lookup"><span data-stu-id="35e05-185">In each of these folders, you can find snapshots of the steps that were performed while the test cases were run.</span></span>

![Tilannevedostiedostot](./media/use_rsa_tool_13.png)

## <a name="assignment"></a><span data-ttu-id="35e05-187">Määritys</span><span class="sxs-lookup"><span data-stu-id="35e05-187">Assignment</span></span>

### <a name="scenario"></a><span data-ttu-id="35e05-188">Skenaario</span><span class="sxs-lookup"><span data-stu-id="35e05-188">Scenario</span></span>

1. <span data-ttu-id="35e05-189">Tuote suunnittelija luo uuden julkaistun tuotteen.</span><span class="sxs-lookup"><span data-stu-id="35e05-189">The product designer creates a new released product.</span></span>
2. <span data-ttu-id="35e05-190">Tuotantopäällikkö käynnistää tuotantotilauksen, joka nostaa varastotason kahteen kappaleeseen.</span><span class="sxs-lookup"><span data-stu-id="35e05-190">The production manager initiates a production order to bring the stock level to two pieces.</span></span>
3. <span data-ttu-id="35e05-191">Valmistus alkaa ja päättää tuotantotilauksen sekä varmistaa, että varastosaldo on kaksi kappaletta.</span><span class="sxs-lookup"><span data-stu-id="35e05-191">Manufacturing starts and ends the production order, and verifies that the on-hand quantity is two pieces.</span></span>
4. <span data-ttu-id="35e05-192">Myyntiryhmä vastaanottaa tilauksen, jossa on neljä kappaletta uutta tuotetta.</span><span class="sxs-lookup"><span data-stu-id="35e05-192">The sales team receives an order for four pieces of the new product.</span></span> <span data-ttu-id="35e05-193">Tämän vuoksi myyntiryhmä päivittää nettotarpeen dynaamisen suunnitelman kautta.</span><span class="sxs-lookup"><span data-stu-id="35e05-193">Therefore, the sales team updates the net requirements via the dynamic plan.</span></span> <span data-ttu-id="35e05-194">Koska lisäkapasiteettia ei ole käytettävissä, tilausten oletuskäytännöksi on määritetty ostaminen valmistamisen sijaan.</span><span class="sxs-lookup"><span data-stu-id="35e05-194">Because no additional capacity is available, the default order policy is set to "buy instead of make."</span></span> <span data-ttu-id="35e05-195">Tämän vuoksi luodaan suunnitellun ostotilauksen.</span><span class="sxs-lookup"><span data-stu-id="35e05-195">Therefore, a planned purchase order is created.</span></span>
5. <span data-ttu-id="35e05-196">Ostaja lisää toimittajan, vahvistaa suunnitellun ostotilauksen ja vahvistaa lopuksi ostotilauksen.</span><span class="sxs-lookup"><span data-stu-id="35e05-196">The buyer adds a vendor, firms the planned purchase order, and then confirms the purchase order.</span></span>
6. <span data-ttu-id="35e05-197">Kun ostetut tavarat saapuvat myymälään, myymäläkäyttäjä hakee liittyvän ostotilauksen ja vastaanottaa tavarat.</span><span class="sxs-lookup"><span data-stu-id="35e05-197">When the goods that were purchased arrive at the store, the store operator searches the related purchase order and receives the goods.</span></span> <span data-ttu-id="35e05-198">Koska tilaus on nyt valmis, tavarat voidaan kerätä ja pakata myyntitilauksen mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="35e05-198">Because the order is now completed, goods can be picked and packed against the sales order.</span></span>
7. <span data-ttu-id="35e05-199">Talousosasta kirjaa osto- ja myyntilaskun.</span><span class="sxs-lookup"><span data-stu-id="35e05-199">Finance posts the purchase invoice and sales invoice.</span></span>

<span data-ttu-id="35e05-200">Seuraavassa kuvassa on tämän skenaarion työnkulku.</span><span class="sxs-lookup"><span data-stu-id="35e05-200">The following illustration shows the flow for this scenario.</span></span>

![Demoskenaarion työnkulku](./media/use_rsa_tool_14.png)

<span data-ttu-id="35e05-202">Seuraavassa kuvassa on tämän skenaarion liiketoimintaprosessit RSAT-työkalussa.</span><span class="sxs-lookup"><span data-stu-id="35e05-202">The following illustration shows the business processes for this scenario in RSAT.</span></span>

![Demoskenaarion liiketoimintaprosessit](./media/use_rsa_tool_15.png)

## <a name="strategy--key-learning"></a><span data-ttu-id="35e05-204">Strategia – keskeinen opittava asia</span><span class="sxs-lookup"><span data-stu-id="35e05-204">Strategy – Key learning</span></span>

### <a name="data"></a><span data-ttu-id="35e05-205">Tiedot</span><span class="sxs-lookup"><span data-stu-id="35e05-205">Data</span></span>

- <span data-ttu-id="35e05-206">Varmista, että sinulla on tarvittavat tiedot (tuotanto-/ihannekonfiguraatiotietojen kopio ja siirretyt tiedot).</span><span class="sxs-lookup"><span data-stu-id="35e05-206">Make sure that you have representative data volumes (a copy of production/golden configuration data plus migrated data).</span></span>
- <span data-ttu-id="35e05-207">Jos luot uusia tietoja tehtävän tallennustoiminnon kautta, luo sellaiset testinimet, jotka eivät ole ristiriidassa aiemmin luotujen nimien kanssa. (Käytä esimerkiksi etuliitettä, kuten **RSATxxx**).</span><span class="sxs-lookup"><span data-stu-id="35e05-207">When you generate new data via Task recorder, create test names that won't conflict with existing names (for example, use a prefix such as **RSATxxx**).</span></span>
- <span data-ttu-id="35e05-208">Suorita testit uudelleen muissa kuin tason 1 ympäristöissä käyttämällä Azuren ajankohtaan perustuvaa palautusta.</span><span class="sxs-lookup"><span data-stu-id="35e05-208">Use Azure Point-In-Time restore to rerun tests in non-Tier 1 environments.</span></span>
- <span data-ttu-id="35e05-209">Vaikka voit muodostaa ainutlaatuisia yhdistelmiä Excelin **SATUNNAINEN**- ja **NYT**-funktioita, sen työmäärä on huomattavan suuri.</span><span class="sxs-lookup"><span data-stu-id="35e05-209">Although you can use the **RANDOM** and **NOW** Excel functions to generate a unique combination, the effort is considerably high.</span></span> <span data-ttu-id="35e05-210">Esimerkki:</span><span class="sxs-lookup"><span data-stu-id="35e05-210">Here is an example.</span></span>

    ```Excel
    product = "AT" &TEXT(NOW(),"yyymmddhhmm")
    ```

### <a name="task-recorder"></a><span data-ttu-id="35e05-211">Tehtävän tallennus</span><span class="sxs-lookup"><span data-stu-id="35e05-211">Task recorder</span></span>

- <span data-ttu-id="35e05-212">Määritä skenaariot ennen tallentamisen aloittamista.</span><span class="sxs-lookup"><span data-stu-id="35e05-212">Define scenarios before you start recording.</span></span> <span data-ttu-id="35e05-213">Hyvin hallitussa projektissa on ennalta määritetyt testiskenaariot.</span><span class="sxs-lookup"><span data-stu-id="35e05-213">A well-managed project has predefined test scenarios.</span></span> <span data-ttu-id="35e05-214">Kun muodostat testitapausta, mieti, kuinka ennakoitavia kyseisten testiskenaarioiden tulos on.</span><span class="sxs-lookup"><span data-stu-id="35e05-214">To build a test case, consider how predictable the outcome of those test scenarios is.</span></span>
- <span data-ttu-id="35e05-215">Jaa tallenteet, jos suorittajalla on eri rooli tai jos ennen seuraavaa vaihetta on odotettava tietty aika tai tiettyä ulkoista tapahtumaa.</span><span class="sxs-lookup"><span data-stu-id="35e05-215">Split recordings if they are performed by different roles, or if there is waiting time or an external event before the next step.</span></span>
- <span data-ttu-id="35e05-216">Vältä luettelossa olevien arvojen valitsemista.</span><span class="sxs-lookup"><span data-stu-id="35e05-216">Avoid selecting values in lists.</span></span> <span data-ttu-id="35e05-217">Käytä sen sijaan tekstimuotoja, kuten **FIFO**, **AudioRM** ja **SiteWH**.</span><span class="sxs-lookup"><span data-stu-id="35e05-217">Instead, use text formats, such as **FIFO**, **AudioRM**, and **SiteWH**.</span></span> <span data-ttu-id="35e05-218">Jos valinta tehdään luettelossa, arvon sijainti luettelossa tallennetaan eikä itse arvoa.</span><span class="sxs-lookup"><span data-stu-id="35e05-218">When you select in a list, the position of the value in the list is recorded, not the value itself.</span></span> <span data-ttu-id="35e05-219">Jos kyseiseen luetteloon lisätään nimikkeitä, arvon sijainti voi muuttua.</span><span class="sxs-lookup"><span data-stu-id="35e05-219">If items are added to that list, the position of the value can change.</span></span> <span data-ttu-id="35e05-220">Tämän vuoksi tallenne käyttää eri parametria, mikä voi vaikuttaa skenaarion muihin osiin.</span><span class="sxs-lookup"><span data-stu-id="35e05-220">Therefore, your recording will use a different parameter, and the rest of the scenario might be affected.</span></span>
- <span data-ttu-id="35e05-221">Mieti tilannetta, jossa käyttäjiä on useita.</span><span class="sxs-lookup"><span data-stu-id="35e05-221">Think about multi-user behavior.</span></span> <span data-ttu-id="35e05-222">Älä esimerkiksi oleta, että juuri luotu myyntitilaus valitaan aina automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="35e05-222">For example, don't assume that your newly created sales order will always be automatically selected.</span></span> <span data-ttu-id="35e05-223">Etsi sen sijaan oikea tilaus aina suodattimella.</span><span class="sxs-lookup"><span data-stu-id="35e05-223">Instead, always use the filter to find the correct order.</span></span>
- <span data-ttu-id="35e05-224">Tallenna juuri luodun tuotteen nimi tehtävän tallennustoiminnon kopiointitoiminnolla, jolloin sitä voidaan käyttää ketjutetuissa testitapauksissa.</span><span class="sxs-lookup"><span data-stu-id="35e05-224">Use the Copy function in Task recorder to save the name of a newly created product so it can be used in chained test cases.</span></span>
- <span data-ttu-id="35e05-225">Määritä tehtävän tallennustoiminnon tarkistustoiminnolla tarkistuspisteet tarkistamaan, että vaiheet on suoritettu oikein.</span><span class="sxs-lookup"><span data-stu-id="35e05-225">Use the Validate function in Task recorder to set checkpoints that verify that steps have been run correctly.</span></span>

### <a name="rsat"></a><span data-ttu-id="35e05-226">RSAT</span><span class="sxs-lookup"><span data-stu-id="35e05-226">RSAT</span></span>

- <span data-ttu-id="35e05-227">Jos suorittaa testin toisessa yrityksessä, voit vaihtaa yrityksen Excelin parametritiedoston **Yleiset**-välilehdessä.</span><span class="sxs-lookup"><span data-stu-id="35e05-227">To run the test in another company, you can change the company on the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="35e05-228">Varmista, että asetuksia ja tietoja voi käyttää juuri valitussa yrityksessä.</span><span class="sxs-lookup"><span data-stu-id="35e05-228">Make sure that settings and data are available in the newly selected company.</span></span>
- <span data-ttu-id="35e05-229">Voit vaihtaa testikäyttäjän Excelin parametritiedoston **Yleiset**-välilehdessä.</span><span class="sxs-lookup"><span data-stu-id="35e05-229">You can change the test user on the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="35e05-230">Määritä testitapauksen suorittavan käyttäjän sähköpostitunnus.</span><span class="sxs-lookup"><span data-stu-id="35e05-230">Specify the email ID of the user who will run the test case.</span></span> <span data-ttu-id="35e05-231">Tällä tavoin testitapaus voidaan suorittaa turvallisesti käyttämällä määritetyn käyttäjän suojausoikeuksia.</span><span class="sxs-lookup"><span data-stu-id="35e05-231">In this way, the test case can be run by using the security permissions of the specified user.</span></span>
- <span data-ttu-id="35e05-232">Jos haluat odottaa ennen testin aloittamista, voit määrittää tauon Excelin parametritiedoston **Yleiset**-välilehdessä.</span><span class="sxs-lookup"><span data-stu-id="35e05-232">To wait before the test is started, you can define a pause on the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="35e05-233">Tätä taukoa voidaan käyttää erätyössä (jos esimerkiksi työnkulku on suoritettava, ennen kuin seuraava vaihe voidaan suorittaa).</span><span class="sxs-lookup"><span data-stu-id="35e05-233">This pause can be used in a batch job (for example, if a workflow must be run before the next step can be performed.)</span></span>

## <a name="advanced-scripting"></a><span data-ttu-id="35e05-234">Edistyneet komentosarjat</span><span class="sxs-lookup"><span data-stu-id="35e05-234">Advanced scripting</span></span>

### <a name="command-line"></a><span data-ttu-id="35e05-235">Komentorivi</span><span class="sxs-lookup"><span data-stu-id="35e05-235">Command line</span></span>

<span data-ttu-id="35e05-236">RSAT voidaan kutsua **Komentokehote**-ikkunasta.</span><span class="sxs-lookup"><span data-stu-id="35e05-236">RSAT can be called from a **Command Prompt** window.</span></span>

> [!NOTE]
> <span data-ttu-id="35e05-237">Tarkista, että **TestRoot**-ympäristömuuttujan asetukseksi on määritetty RSAT-asennuspolku.</span><span class="sxs-lookup"><span data-stu-id="35e05-237">Verify that the **TestRoot** environment variable is set to the RSAT installation path.</span></span> <span data-ttu-id="35e05-238">(Avaa Microsoft Windowsissa **Ohjauspaneeli**, valitse sitten **Järjestelmä ja suojaus \> Järjestelmä \> Järjestelmän lisäasetukset** ja valitse lopuksi **Ympäristömuuttujat**.)</span><span class="sxs-lookup"><span data-stu-id="35e05-238">(In Microsoft Windows, open **Control Panel**, select **System and Security \> System \> Advanced system settings**, and then select **Environment Variables**.)</span></span>

1. <span data-ttu-id="35e05-239">Avaa **Komentokehote**-ikkuna järjestelmänvalvojana.</span><span class="sxs-lookup"><span data-stu-id="35e05-239">Open a **Command Prompt** window as an admin.</span></span>
2. <span data-ttu-id="35e05-240">Suorita työkalu asennushakemistosta.</span><span class="sxs-lookup"><span data-stu-id="35e05-240">Run the tool from the installation directory.</span></span>

    ```Console
    cd "c:\Program Files (x86)\Regression Suite Automation Tool\"
    ```

3. <span data-ttu-id="35e05-241">Luettele kaikki komennot.</span><span class="sxs-lookup"><span data-stu-id="35e05-241">List all commands.</span></span>

    ```Console
    C:\Program Files (x86)\Regression Suite Automation Tool>Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe help

    Usage:
        Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe command
        or
        Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe /settings "C:\Path to\file.settings" command

    Available commands:
        list
        listtestsuite suite_name
        download test_case_id output_dir
        generate test_case_id output_dir
        generatederived parent_test_case_id test_plan_id test_suite_id
        generatetestonly test_case_id output_dir
        edit excel_file
        playback excel_file
        playbackmany excel_file1 [excel_file2 [.. excel_fileN]]
        playbackbyid test_case_id1 [test_case_id2 [.. test_case_idN]]
        playbacksuite suite_name
        clear
        help
        about
        quit
    ```

### <a name="windows-powershell-examples"></a><span data-ttu-id="35e05-242">Windows PowerShell -esimerkkejä</span><span class="sxs-lookup"><span data-stu-id="35e05-242">Windows PowerShell examples</span></span>

#### <a name="run-a-test-case-in-a-loop"></a><span data-ttu-id="35e05-243">Testitapauksen suorittaminen silmukkana</span><span class="sxs-lookup"><span data-stu-id="35e05-243">Run a test case in a loop</span></span>

<span data-ttu-id="35e05-244">Sinulla on uuden asiakkaan luova testikomentosarja.</span><span class="sxs-lookup"><span data-stu-id="35e05-244">You have a test script that creates a new customer.</span></span> <span data-ttu-id="35e05-245">Tämä testisarja voidaan suorittaa komentosarjojen avulla silmukkana muodostamalla seuraavat tiedot satunnaisesti ennen kunkin iteraation suorittamista:</span><span class="sxs-lookup"><span data-stu-id="35e05-245">Via scripting, this test case can be run in a loop by randomizing the following data before each iteration is run:</span></span>

- <span data-ttu-id="35e05-246">Asiakastunnus</span><span class="sxs-lookup"><span data-stu-id="35e05-246">Customer ID</span></span>
- <span data-ttu-id="35e05-247">Asiakkaan nimi</span><span class="sxs-lookup"><span data-stu-id="35e05-247">Customer name</span></span>
- <span data-ttu-id="35e05-248">Asiakkaan osoitetiedot</span><span class="sxs-lookup"><span data-stu-id="35e05-248">Customer address</span></span>

<span data-ttu-id="35e05-249">Asiakastunnuksen muoto on seuraavanlainen: *ATCUS\<numero\>*, jossa \<numeron\> arvo on **000000001**–**999999999**.</span><span class="sxs-lookup"><span data-stu-id="35e05-249">The customer ID will be in the format *ATCUS\<number\>*, where \<number\> is a value between **000000001** and **999999999**.</span></span>

<span data-ttu-id="35e05-250">Seuraavassa esimerkissä käytetään yhtä **aloitus**-parametria määrittämään ensimmäinen käytettävä numero.</span><span class="sxs-lookup"><span data-stu-id="35e05-250">The following example uses one parameter, **start**, to define the first number that is used.</span></span> <span data-ttu-id="35e05-251">Is käyttää seuraavaa parametria **nr** määrittämään luotavien asiakkaiden määrän.</span><span class="sxs-lookup"><span data-stu-id="35e05-251">Is uses a second parameter, **nr**, to define the number of customers that must be created.</span></span> <span data-ttu-id="35e05-252">Excelin parametritiedoston parametrit muutetaan kussakin iteraatiossa käyttämällä UpdateCustomer-funktiota.</span><span class="sxs-lookup"><span data-stu-id="35e05-252">For each iteration, the parameters in the Excel parameter file are changed by using an UpdateCustomer function.</span></span> <span data-ttu-id="35e05-253">RSAT-komentorivi kutsutaan sitten RunTestCase-funktiolla.</span><span class="sxs-lookup"><span data-stu-id="35e05-253">Then the RSAT command line is called in a RunTestCase function.</span></span>

<span data-ttu-id="35e05-254">Avaa integroitu Microsoft Windows PowerShell -komentosarjaympäristö (ISE) järjestelmänvalvojan tilassa ja liitä seuraava koodi **Untitled1.ps1**-nimiseen ikkunaan.</span><span class="sxs-lookup"><span data-stu-id="35e05-254">Open Microsoft Windows PowerShell Integrated Scripting Environment (ISE) in admin mode, and paste the following code into the window that is named **Untitled1.ps1**.</span></span>

```powershell
param ( [int]$start = 1, [int]$nr = 1 )
function UpdateCustomer
{
    param ([string]$paramFilename, [string]$sheetName, [string]$CustId)
    $xl = New-Object -COM "Excel.Application"
    $xl.Visible = $false
    $wb = $xl.Workbooks.Open($paramFilename)
    $ws = $wb.Sheets.Item($sheetName)
    $ws.Cells.Item(3, 2).Value = "ATCUS" + $CustId
    $ws.Cells.Item(4, 2).Value = "Automated Test Customer " + $CustId
    $ws.Cells.Item(8, 2).Value = "Automated Test Street " + $CustId
    $wb.Save()
    $wb.Close()
    $xl.Quit()
    [System.Runtime.Interopservices.Marshal]::ReleaseComObject($xl)
}
function RunTestCase
{
    param ( [string]$filename )
    $cmd = "cd c:\Program Files (x86)\Regression Suite Automation Tool\ &&  "
    $cmd = $cmd + "Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe playback "
    $cmd = $cmd + $filename
    cmd /c $cmd
}
$excelFilename = "full path to excel file parameter file"
l$sheetName = "DirPartyQuickCreateForm"
for ($i = $start; $i -lt $start + $nr; $i++ )
{
    $CustomerId = $i.ToString("000000000")
    Write-Host "customer : " $CustomerId
    UpdateCustomer $excelFilename $sheetName $CustomerId
    RunTestCase $excelFilename
```

#### <a name="run-a-script-that-depends-on-data-in-microsoft-dynamics-365"></a><span data-ttu-id="35e05-255">Microsoft Dynamics 365:n tiedoista riippuvaisen komentosarjan suorittaminen</span><span class="sxs-lookup"><span data-stu-id="35e05-255">Run a script that depends on data in Microsoft Dynamics 365</span></span>

<span data-ttu-id="35e05-256">Seuraavassa esimerkissä ostotilauksen tila etsitään Open Data Protocol (OData) -kutsun avulla.</span><span class="sxs-lookup"><span data-stu-id="35e05-256">The following example uses an Open Data Protocol (OData) call to find the order status of a purchase order.</span></span> <span data-ttu-id="35e05-257">Jos tila ei ole **invoiced**, voit esimerkiksi kutsua laskun kirjaavan RSAT-testitapauksen.</span><span class="sxs-lookup"><span data-stu-id="35e05-257">If the status isn't **invoiced**, you can, for example, call an RSAT test case that posts the invoice.</span></span>

```xpp
function Odata_Get
{
    Param ( [string] $environment, [string] $cmd )
    [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12
    $tenant = "your tenant"
    $creds = @{
        grant_type = "client_credentials"
        client_id = "your client application Id"
        client_secret = "your client secret"
        resource = $environment
    }
    $headers = $null
    $bearer = Invoke-RestMethod https://login.microsoftonline.com/$tenant/oauth2/token -Method Post -Body $creds -Headers $headers;
    $headers = @{
        Authorization = "Bearer " + $bearer.access_token
    }
    $Odata_cmd = $environment + '/data/' + $cmd
    return (Invoke-RestMethod -Uri $Odata_cmd -Method Get -Headers $headers -ContentType application/json )
}
function PurchaseOrderStatus
{
    Param ( [string] $environment, [string] $purchaseOrderNumber )
    $cmd = 'PurchaseOrderHeaders?$filter=PurchaseOrderNumber eq '
    $cmd = $cmd + "'" + $purchaseOrderNumber + "'"
    $response = Odata_Get -environment $environment -cmd $cmd
    return $response.value.PurchaseOrderStatus
}
$environment = "https://your environment"
$orderStatus = PurchaseOrderStatus -environment $environment -purchaseOrderNumber '000003'
if ($orderStatus -eq $null) {   write-host 'doesn''t exist'}
elseif ($orderStatus -ne 'invoiced') { RunTestCase "PostInvoice" }
```
