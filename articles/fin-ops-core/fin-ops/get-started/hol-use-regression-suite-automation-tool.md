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
ms.openlocfilehash: 6cdaa89fb6d50ebaaaefe7f92d7224a1567d17d1
ms.sourcegitcommit: 3dede95a3b17de920bb0adcb33029f990682752b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/18/2020
ms.locfileid: "3070817"
---
# <a name="use-the-regression-suite-automation-tool-tutorial"></a><span data-ttu-id="1c2a2-104">Regression Suite Automation Tool -oppaan käyttäminen</span><span class="sxs-lookup"><span data-stu-id="1c2a2-104">Use the Regression suite automation tool tutorial</span></span>

[!include [banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="1c2a2-105">Lataa ja tallenna tämä ohje selaimen työkaluilla PDF-tiedostona.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-105">Use your internet browser tools to download and save this page in pdf format.</span></span> 

<span data-ttu-id="1c2a2-106">Tässä oppaassa käsitellään yksityiskohtaisesti Regression Suite Automation Tool (RSAT) -työkalun lisätoimintoja. Se sisältää myös demon määrityksen ja siinä käsitellään strategiaa ja keskeisiä opittavia asioita.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-106">This tutorial walks through some of the advanced features of the Regression suite automation tool (RSAT), includes a demo assignment, and describes strategy and key learning points.</span></span>

## <a name="features-of-rsattask-recorder"></a><span data-ttu-id="1c2a2-107">RSAT-työkalun ja tehtävän tallennustoiminnon toiminnot</span><span class="sxs-lookup"><span data-stu-id="1c2a2-107">Features of RSAT/Task recorder</span></span>

### <a name="validate-a-field-value"></a><span data-ttu-id="1c2a2-108">Kentän arvon tarkistaminen</span><span class="sxs-lookup"><span data-stu-id="1c2a2-108">Validate a field value</span></span>

<span data-ttu-id="1c2a2-109">Lisätietoja tästä toiminnosta on kohdassa [Uuden tarkistustoiminnon sisältävän tehtävätallenteen luominen](./hol-set-up-regression-suite-automation-tool.md#create-a-new-task-recording-that-has-a-validate-function).</span><span class="sxs-lookup"><span data-stu-id="1c2a2-109">For information about this feature, see the [Create a new task recording that has a Validate function](./hol-set-up-regression-suite-automation-tool.md#create-a-new-task-recording-that-has-a-validate-function).</span></span>

### <a name="saved-variable"></a><span data-ttu-id="1c2a2-110">Tallennettu muuttuja</span><span class="sxs-lookup"><span data-stu-id="1c2a2-110">Saved variable</span></span>

<span data-ttu-id="1c2a2-111">Lisätietoja tästä toiminnosta on kohdassa [Tallennetun muuttujan luominen muokkaamalla aiemmin luotua tehtävätallennetta](./hol-set-up-regression-suite-automation-tool.md#modify-an-existing-task-recording-to-create-a-saved-variable).</span><span class="sxs-lookup"><span data-stu-id="1c2a2-111">For information about this feature, see the [Modify an existing task recording to create a saved variable](./hol-set-up-regression-suite-automation-tool.md#modify-an-existing-task-recording-to-create-a-saved-variable).</span></span>

### <a name="derived-test-case"></a><span data-ttu-id="1c2a2-112">Johdettu testitapaus</span><span class="sxs-lookup"><span data-stu-id="1c2a2-112">Derived test case</span></span>

1. <span data-ttu-id="1c2a2-113">Avaa Regression Suite Automation Tool (RSAT) ja valitse molemmat kohdassa [Regression Suite Automation Tool -opetusohjelman määrittäminen ja asentaminen](./hol-set-up-regression-suite-automation-tool.md) luodut testitapaukset.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-113">Open Regression suite automation tool (RSAT), and select both the test cases that you created in [Set up and install Regression suite automation tool tutorial](./hol-set-up-regression-suite-automation-tool.md).</span></span>
2. <span data-ttu-id="1c2a2-114">Valitse **Uusi \> Luo johdettu testitapaus**.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-114">Select **New \> Create derived test case**.</span></span>

    ![Luo johdettu testitapaus -komento Uusi-valikossa](./media/use_rsa_tool_01.png)

3. <span data-ttu-id="1c2a2-116">Näyttöön avautuva sanoma ilmoittaa, että jokaiselle nykyisessä testisarjassa valitulle testitapauksella luodaan johdettu testitapaus ja että jokaisella johdetulla testitapauksella on oma Excelin parametritiedoston kopio.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-116">You receive a message that states that a derived test case will be created for each selected test case in the current test suite, and that each derived test case will have its own copy of the Excel parameter file.</span></span> <span data-ttu-id="1c2a2-117">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-117">Select **OK**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="1c2a2-118">Suoritettava testitapaus käyttää päätestitapauksen tehtävätallennetta ja omaa Excelin parametritiedoston kopioita.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-118">When you run a derived test case, it uses the task recording of its parent test case and its own copy of the Excel parameter file.</span></span> <span data-ttu-id="1c2a2-119">Tällä tavoin voit suorittaa saman testi eri parametreilla käyttämällä samaa tehtävätallennetta.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-119">In this way, you can run the same test with different parameters, without having to maintain more than one task recording.</span></span> <span data-ttu-id="1c2a2-120">Johdetun testitapauksen ei tarvitse kuulua samaan testisarjaan kuin sen päätestitapaus.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-120">A derived test case doesn't have to be part of the same test suite as its parent test case.</span></span>

    ![Viestiruutu](./media/use_rsa_tool_02.png)

    <span data-ttu-id="1c2a2-122">Kaksi muuta johdettua testitapausta luodaan ja niille valitaan **Johdettu?** -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-122">Two additional derived test cases are created, and the **Derived?** check box is selected for them.</span></span>

    ![Luodut johdetut testitapaukset](./media/use_rsa_tool_03.png)

    <span data-ttu-id="1c2a2-124">Johdettu testitapaus luodaan automaattisesti Azure DevOpsissa.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-124">A derived test case is automatically created in Azure DevOps.</span></span> <span data-ttu-id="1c2a2-125">Se on **Luo uusi tuote** -testitapauksen alinimike ja siihen merkitään erityinen avainsana: **RSAT:DerivedTestSteps**.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-125">It's a child item of the **Create a new product** test case and is tagged with a special keyword: **RSAT:DerivedTestSteps**.</span></span> <span data-ttu-id="1c2a2-126">Lisäksi nämä testitapaukset lisätään automaattisesti testisuunnitelmaan Azure DevOpsissa.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-126">These test cases are also automatically added to the test plan in Azure DevOps.</span></span>

    ![RSAT: DerivedTestSteps-avainsana](./media/use_rsa_tool_04.png)

    > [!NOTE]
    > <span data-ttu-id="1c2a2-128">Jos luodut johdetut testitapaukset eivät jostain syytä ole oikeassa järjestyksessä, siirry Azure DevOps ja järjestä testisarjan testitapaukset uudelleen, jotta RSAT voi suorittaa ne oikeassa järjestyksessä.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-128">If, for any reason, the derived test cases that are created aren't in the correct order, go to Azure DevOps, and reorder the test cases in the test suite, so that RSAT can run them in the correct order.</span></span>

4. <span data-ttu-id="1c2a2-129">Valitse ensin johdetut testitapaukset ja avaa sitten vastaavat Excelin parametritiedostot valitsemalla **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-129">Select the derived test cases, and then select **Edit** to open the corresponding Excel parameter files.</span></span>
5. <span data-ttu-id="1c2a2-130">Muokkaa näitä Excelin parametritiedostoja samalla tavalla kuin muokkasit päätiedostoja.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-130">Edit these Excel parameter files in the same way that you edited the parent files.</span></span> <span data-ttu-id="1c2a2-131">Toisen sanoen varmista, että tuotetunnus on määritetty automaattisesti luotavaksi.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-131">In other words, make sure that the product ID is set so that it's automatically generated.</span></span> <span data-ttu-id="1c2a2-132">Varmista myös, että tallennettu muuttuja kopioidaan soveltuviin kenttiin.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-132">Also make sure that the saved variable is copied to the relevant fields.</span></span>
6. <span data-ttu-id="1c2a2-133">Päivitä Excelin parametritiedoston **Yleiset**-välilehdessä **Yritys**-kentän arvoksi **USSI**. Tällä tavoin johdetut testitapaukset suoritetaan eri yrityksen perusteella kuin päätestitapaus.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-133">On the **General** tab of both Excel parameter files, update the value of the **Company** field to **USSI**, so that the derived test cases will be run against a different legal entity than the parent test case.</span></span> <span data-ttu-id="1c2a2-134">Jos haluat suorittaa testitapauksia tietyn käyttäjän (tai tiettyyn käyttäjään liitetyn roolin) osalta, voit päivittää **Testikäyttäjä**-kentän arvon.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-134">To run the test cases against a specific user (or the role that is associated with a specific user), you can update the value of the **Test User** field.</span></span>
7. <span data-ttu-id="1c2a2-135">Valitse **Suorita** ja tarkista, että tuote on luotu sekä USMF-yrityksessä että USSI-yrityksessä.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-135">Select **Run**, and validate that the product is created in both the USMF legal entity and the USSI legal entity.</span></span>

### <a name="validate-notifications"></a><span data-ttu-id="1c2a2-136">Ilmoitusten tarkistaminen</span><span class="sxs-lookup"><span data-stu-id="1c2a2-136">Validate notifications</span></span>

<span data-ttu-id="1c2a2-137">Tällä toiminnolla tarkistetaan, tapahtuiko toiminto.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-137">This feature can be used to validate whether an action occurred.</span></span> <span data-ttu-id="1c2a2-138">Kun esimerkiksi tuotantotilaus luodaan, arvioidaan ja aloitetaan, sovellus ilmoittaa Tuotanto - käynnistys -sanomalla, että tuotantotilaus on aloitettu.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-138">For example, when a production order is created, estimated, and then started, the app shows a "Production – Start" message to notify you that the production order has been started.</span></span>

![Tuotanto - käynnistys -ilmoitus](./media/use_rsa_tool_05.png)

<span data-ttu-id="1c2a2-140">Voit tarkistaa tämän sanoman RSAT-työkalussa etsimällä kyseisen tallenteen antamalla sanoman tekstin Excelin parametritiedoston **Viestin tarkistus**-välilehdessä.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-140">You can validate this message through RSAT by entering the message text on the **MessageValidation** tab of the Excel parameter file for the appropriate recording.</span></span>

![Viestin tarkistus -välilehti](./media/use_rsa_tool_06.png)

<span data-ttu-id="1c2a2-142">Kun testitapaus on suoritettu, Excelin parametritiedostoa verrataan näytettävään sanomaan.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-142">After the test case is run, the message in the Excel parameter file is compared to the message that is shown.</span></span> <span data-ttu-id="1c2a2-143">Jos sanomat eivät vastaa toisiaan, testitapaus epäonnistuu.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-143">If the messages don't match, the test case will fail.</span></span>

> [!NOTE]
> <span data-ttu-id="1c2a2-144">Voit antaa Excelin parametritiedoston **Viestitarkistus**-välilehdessä useita sanomia.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-144">You can enter more than one message on the **MessageValidation** tab in the Excel parameter file.</span></span> <span data-ttu-id="1c2a2-145">Sanomat voivat myös olla virhe- tai varoitussanomia ilmoitussanomien sijaan.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-145">The messages also can be error or warning messages instead of informational messages.</span></span>

### <a name="validate-values-by-using-operators"></a><span data-ttu-id="1c2a2-146">Arvojen tarkistaminen operaattorien avulla</span><span class="sxs-lookup"><span data-stu-id="1c2a2-146">Validate values by using operators</span></span>

<span data-ttu-id="1c2a2-147">RSAT-työkalun edellisissä versioissa arvot voitiin vahvistaa vain, jos tarkistusarvo ja odotettu arvo olivat samat.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-147">In previous versions of RSAT, you could validate values only if a control value equaled an expected value.</span></span> <span data-ttu-id="1c2a2-148">Uudella toiminnolla voi tarkistaa, että muuttuja ei ole yhtä suuri kuin tai on pienempi tai suurempi kuin määritetty arvo.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-148">The new feature lets you validate that a variable isn't equal to, is less than, or is more than a specified value.</span></span>

- <span data-ttu-id="1c2a2-149">Avaa tällä toiminnolla **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config**-tiedosto RSAT-asennuskansiossa (esimerkiksi kansiossa **C:\\Program Files (x86)\\Regression Suite Automation Tool**) ja muuta seuraavan elementin arvo **epätosi** arvoksi **tosi**.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-149">To use this feature, open the **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** file under the RSAT installation folder (for example, **C:\\Program Files (x86)\\Regression Suite Automation Tool**), and change the value in the following element from **false** to **true**.</span></span>

    ```xml
    <add key="AddOperatorFieldsToExcelValidation" value="false" />
    ```

    <span data-ttu-id="1c2a2-150">Uusi **Operaattori**-kenttä tulee näkyviin Excelin parametritiedostossa.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-150">In the Excel parameter file, a new **Operator** field appears.</span></span>

    > [!NOTE]
    > <span data-ttu-id="1c2a2-151">Jos olet käyttänyt vanhaa RSAT-versiota, uudet Excelin parametritiedostot on luotava.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-151">If you've been using an older version of RSAT, you must generate new Excel parameter files.</span></span>

    ![Operaattorikenttä](./media/use_rsa_tool_07.png)

<span data-ttu-id="1c2a2-153">Seuraava esimerkki osoittaa, miten tällä toiminnolla tarkistetaan, onko varastosaldo suurempi kuin 0 (nolla).</span><span class="sxs-lookup"><span data-stu-id="1c2a2-153">The following example shows how you can use this feature to validate whether the on-hand inventory is more than 0 (zero).</span></span>

1. <span data-ttu-id="1c2a2-154">Luo demotietojen **USMF**-yrityksessä tehtävätallenne, jossa on seuraavat vaiheet:</span><span class="sxs-lookup"><span data-stu-id="1c2a2-154">In the demo data in the **USMF** company, create a task recording that has the following steps:</span></span>

    1. <span data-ttu-id="1c2a2-155">Mene **Tuotetietojen hallinta \> Tuotteet \> Vapautetut tuotteet**.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-155">Go to **Product information management \> Products \> Released products**.</span></span>
    2. <span data-ttu-id="1c2a2-156">Käytä pikasuodatinta tietueiden etsimiseen.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-156">Use the Quick Filter to find records.</span></span> <span data-ttu-id="1c2a2-157">Voit esimerkiksi suodattaa **Nimiketunnus**-kenttää arvolla **1000**.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-157">For example, filter on a value of **1000** for the **Item number** field.</span></span>
    3. <span data-ttu-id="1c2a2-158">Valitse **Käytettävissä oleva varasto**.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-158">Select **On-hand inventory**.</span></span>
    4. <span data-ttu-id="1c2a2-159">Käytä pikasuodatinta tietueiden etsimiseen.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-159">Use the Quick Filter to find records.</span></span> <span data-ttu-id="1c2a2-160">Voit esimerkiksi suodattaa **Toimipaikka**-kenttää arvolla **1**.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-160">For example, filter on a value of **1** for the **Site** field.</span></span>
    5. <span data-ttu-id="1c2a2-161">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-161">In the list, mark the selected row.</span></span>
    6. <span data-ttu-id="1c2a2-162">Tarkista, että **Yhteensä käytettävissä** -kentän arvo on **411,0000000000000000**.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-162">Validate that the value of the **Total available** field is **411.0000000000000000**.</span></span>

2. <span data-ttu-id="1c2a2-163">Tallenna tehtävätallenne LCS:n BPM-kirjastoon ja synkronoi se Azure DevOpsiin.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-163">Save the task recording to the BPM library in LCS, and sync it to Azure DevOps.</span></span>
3. <span data-ttu-id="1c2a2-164">Lisää testitapaus testisuunnitelmaan ja lataa testitapaus RSAT-työkaluun.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-164">Add the test case to the test plan, and load the test case into RSAT.</span></span>
4. <span data-ttu-id="1c2a2-165">Avaa Excelin parametritiedosto.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-165">Open the Excel parameter file.</span></span> <span data-ttu-id="1c2a2-166">**Inventonhandimitem**-välilehdessä on **Tarkista InventOnhandItem** -osa, jossa on **Operaattori**-kenttä.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-166">On the **InventOnhandItem** tab, you will see a **Validate InventOnhandItem** section that includes an **Operator** field.</span></span>

    ![Operaattorikenttä](./media/use_rsa_tool_08.png)

5. <span data-ttu-id="1c2a2-168">Jos haluat tarkistaa, että varastosaldo on aina yli 0, muuta **Arvo**-kentän arvo **411** arvoksi **0** ja **Operaattori**-kentän yhtä suuri kuin -merkki (**=**) suurempi kuin -merkiksi (**\>**).</span><span class="sxs-lookup"><span data-stu-id="1c2a2-168">To validate whether the inventory on-hand will always be more than 0, change the value of the **Value** field from **411** to **0** and the value of the **Operator** field from an equal sign (**=**) to a greater than sign (**\>**).</span></span>

    ![Arvo-ja Operaattori-kenttien muuttuneet arvot](./media/use_rsa_tool_09.png)

6. <span data-ttu-id="1c2a2-170">Tallenna ja sulje Excelin parametritiedosto.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-170">Save and close the Excel parameter file.</span></span>
7. <span data-ttu-id="1c2a2-171">Tallenna Excelin parametritiedostoon tehdyt muutokset Azure DevOpsiin valitsemalla **Lataa palvelimeen**.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-171">Select **Upload** to save the changes that you made to the Excel parameter file to Azure DevOps.</span></span>

<span data-ttu-id="1c2a2-172">Huomaa, että jos tietyn nimikkeen **Yhteensä käytettävissä** -kentän arvo varastossa on suurempi kuin 0 (nolla), testi hyväksytään todellisen varastosaldon arvosta riippumatta.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-172">Now, if the value of the **Total Available** field for the specified item in inventory is more than 0 (zero), tests will pass, regardless of the actual on-hand inventory value.</span></span>

### <a name="generator-logs"></a><span data-ttu-id="1c2a2-173">Generaattorin lokit</span><span class="sxs-lookup"><span data-stu-id="1c2a2-173">Generator logs</span></span>

<span data-ttu-id="1c2a2-174">Tämä toiminto luo kansion, joka sisältää suoritettujen testitapausten lokit.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-174">This feature creates a folder that contains the logs of the test cases that have been run.</span></span>

- <span data-ttu-id="1c2a2-175">Avaa tällä toiminnolla **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config**-tiedosto RSAT-asennuskansiossa (esimerkiksi kansiossa **C:\\Program Files (x86)\\Regression Suite Automation Tool**) ja muuta seuraavan elementin arvo **epätosi** arvoksi **tosi**.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-175">To use this feature, open the **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** file under the RSAT installation folder (for example, **C:\\Program Files (x86)\\Regression Suite Automation Tool**), and change the value in the following element from **false** to **true**.</span></span>

    ```xml
    <add key="LogGeneration" value="false" />
    ```

<span data-ttu-id="1c2a2-176">Suoritettujen testitapausten lokitiedostot sijaitsevat kansiossa **C:\\Käyttäjät\\\<Käyttäjänimi\>\\AppData\\Roaming\\regressionTool\\generatorLogs**.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-176">After the test cases are run, you can find the log files under **C:\\Users\\\<Username\>\\AppData\\Roaming\\regressionTool\\generatorLogs**.</span></span>

![GeneratorLogs-kansio](./media/use_rsa_tool_10.png)

> [!NOTE]
> <span data-ttu-id="1c2a2-178">Jos testitapauksia oli luotu ennen .config-tiedoston arvon muuttamista, kyseisten testitapausten lokeja ei luoda, ennen kuin uudet testin suoritustiedostot luodaan.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-178">If there were existing test cases before you changed the value in the .config file, logs won't be generated for those test cases until you generate new test execution files.</span></span>
> 
> ![Uusi-valikon Luo vain testin suoritustiedostot -komento](./media/use_rsa_tool_11.png)

### <a name="snapshot"></a><span data-ttu-id="1c2a2-180">Tilannevedos</span><span class="sxs-lookup"><span data-stu-id="1c2a2-180">Snapshot</span></span>

<span data-ttu-id="1c2a2-181">Tämä toiminto ottaa näyttökuvat tehtävätallenteen aikana suoritetuista vaiheista.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-181">This feature takes screenshots of the steps that were performed during task recording.</span></span>

- <span data-ttu-id="1c2a2-182">Avaa tällä toiminnolla **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config**-tiedosto RSAT-asennuskansiossa (esimerkiksi kansiossa **C:\\Program Files (x86)\\Regression Suite Automation Tool**) ja muuta seuraavan elementin arvo **epätosi** arvoksi **tosi**.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-182">To use this feature, open the **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** file under the RSAT installation folder (for example, **C:\\Program Files (x86)\\Regression Suite Automation Tool**), and change the value of the following element from **false** to **true**.</span></span>

    ```xml
    <add key="VerboseSnapshotsEnabled" value="false" />
    ```

<span data-ttu-id="1c2a2-183">Jokaiselle suoritettavalle testitapaukselle luodaan erillinen kansio kohdassa **C:\\Käyttäjät\\\<Käyttäjänimi\>\\AppData\\Roaming\\regressionTool\\playback**.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-183">Under **C:\\Users\\\<Username\>\\AppData\\Roaming\\regressionTool\\playback**, a separate folder is created for each test case that is run.</span></span>

![Testitapauksen tilannevedoskansio](./media/use_rsa_tool_12.png)

<span data-ttu-id="1c2a2-185">Kussakin näistä kansioista on tilannevedoksia testitapausten suorittamisen aikana suoritetuista vaiheista.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-185">In each of these folders, you can find snapshots of the steps that were performed while the test cases were run.</span></span>

![Tilannevedostiedostot](./media/use_rsa_tool_13.png)

## <a name="assignment"></a><span data-ttu-id="1c2a2-187">Määritys</span><span class="sxs-lookup"><span data-stu-id="1c2a2-187">Assignment</span></span>

### <a name="scenario"></a><span data-ttu-id="1c2a2-188">Skenaario</span><span class="sxs-lookup"><span data-stu-id="1c2a2-188">Scenario</span></span>

1. <span data-ttu-id="1c2a2-189">Tuote suunnittelija luo uuden julkaistun tuotteen.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-189">The product designer creates a new released product.</span></span>
2. <span data-ttu-id="1c2a2-190">Tuotantopäällikkö käynnistää tuotantotilauksen, joka nostaa varastotason kahteen kappaleeseen.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-190">The production manager initiates a production order to bring the stock level to two pieces.</span></span>
3. <span data-ttu-id="1c2a2-191">Valmistus alkaa ja päättää tuotantotilauksen sekä varmistaa, että varastosaldo on kaksi kappaletta.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-191">Manufacturing starts and ends the production order, and verifies that the on-hand quantity is two pieces.</span></span>
4. <span data-ttu-id="1c2a2-192">Myyntiryhmä vastaanottaa tilauksen, jossa on neljä kappaletta uutta tuotetta.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-192">The sales team receives an order for four pieces of the new product.</span></span> <span data-ttu-id="1c2a2-193">Tämän vuoksi myyntiryhmä päivittää nettotarpeen dynaamisen suunnitelman kautta.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-193">Therefore, the sales team updates the net requirements via the dynamic plan.</span></span> <span data-ttu-id="1c2a2-194">Koska lisäkapasiteettia ei ole käytettävissä, tilausten oletuskäytännöksi on määritetty ostaminen valmistamisen sijaan.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-194">Because no additional capacity is available, the default order policy is set to "buy instead of make."</span></span> <span data-ttu-id="1c2a2-195">Tämän vuoksi luodaan suunnitellun ostotilauksen.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-195">Therefore, a planned purchase order is created.</span></span>
5. <span data-ttu-id="1c2a2-196">Ostaja lisää toimittajan, vahvistaa suunnitellun ostotilauksen ja vahvistaa lopuksi ostotilauksen.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-196">The buyer adds a vendor, firms the planned purchase order, and then confirms the purchase order.</span></span>
6. <span data-ttu-id="1c2a2-197">Kun ostetut tavarat saapuvat myymälään, myymäläkäyttäjä hakee liittyvän ostotilauksen ja vastaanottaa tavarat.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-197">When the goods that were purchased arrive at the store, the store operator searches the related purchase order and receives the goods.</span></span> <span data-ttu-id="1c2a2-198">Koska tilaus on nyt valmis, tavarat voidaan kerätä ja pakata myyntitilauksen mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-198">Because the order is now completed, goods can be picked and packed against the sales order.</span></span>
7. <span data-ttu-id="1c2a2-199">Talousosasta kirjaa osto- ja myyntilaskun.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-199">Finance posts the purchase invoice and sales invoice.</span></span>

<span data-ttu-id="1c2a2-200">Seuraavassa kuvassa on tämän skenaarion työnkulku.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-200">The following illustration shows the flow for this scenario.</span></span>

![Demoskenaarion työnkulku](./media/use_rsa_tool_14.png)

<span data-ttu-id="1c2a2-202">Seuraavassa kuvassa on tämän skenaarion liiketoimintaprosessit RSAT-työkalussa.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-202">The following illustration shows the business processes for this scenario in RSAT.</span></span>

![Demoskenaarion liiketoimintaprosessit](./media/use_rsa_tool_15.png)

## <a name="strategy--key-learning"></a><span data-ttu-id="1c2a2-204">Strategia – keskeinen opittava asia</span><span class="sxs-lookup"><span data-stu-id="1c2a2-204">Strategy – Key learning</span></span>

### <a name="data"></a><span data-ttu-id="1c2a2-205">Tiedot</span><span class="sxs-lookup"><span data-stu-id="1c2a2-205">Data</span></span>

- <span data-ttu-id="1c2a2-206">Varmista, että sinulla on tarvittavat tiedot (tuotanto-/ihannekonfiguraatiotietojen kopio ja siirretyt tiedot).</span><span class="sxs-lookup"><span data-stu-id="1c2a2-206">Make sure that you have representative data volumes (a copy of production/golden configuration data plus migrated data).</span></span>
- <span data-ttu-id="1c2a2-207">Jos luot uusia tietoja tehtävän tallennustoiminnon kautta, luo sellaiset testinimet, jotka eivät ole ristiriidassa aiemmin luotujen nimien kanssa. (Käytä esimerkiksi etuliitettä, kuten **RSATxxx**).</span><span class="sxs-lookup"><span data-stu-id="1c2a2-207">When you generate new data via Task recorder, create test names that won't conflict with existing names (for example, use a prefix such as **RSATxxx**).</span></span>
- <span data-ttu-id="1c2a2-208">Suorita testit uudelleen muissa kuin tason 1 ympäristöissä käyttämällä Azuren ajankohtaan perustuvaa palautusta.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-208">Use Azure Point-In-Time restore to rerun tests in non-Tier 1 environments.</span></span>
- <span data-ttu-id="1c2a2-209">Vaikka voit muodostaa ainutlaatuisia yhdistelmiä Excelin **SATUNNAINEN**- ja **NYT**-funktioita, sen työmäärä on huomattavan suuri.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-209">Although you can use the **RANDOM** and **NOW** Excel functions to generate a unique combination, the effort is considerably high.</span></span> <span data-ttu-id="1c2a2-210">Esimerkki:</span><span class="sxs-lookup"><span data-stu-id="1c2a2-210">Here is an example.</span></span>

    ```Excel
    product = "AT" &TEXT(NOW(),"yyymmddhhmm")
    ```

### <a name="task-recorder"></a><span data-ttu-id="1c2a2-211">Tehtävän tallennus</span><span class="sxs-lookup"><span data-stu-id="1c2a2-211">Task recorder</span></span>

- <span data-ttu-id="1c2a2-212">Määritä skenaariot ennen tallentamisen aloittamista.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-212">Define scenarios before you start recording.</span></span> <span data-ttu-id="1c2a2-213">Hyvin hallitussa projektissa on ennalta määritetyt testiskenaariot.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-213">A well-managed project has predefined test scenarios.</span></span> <span data-ttu-id="1c2a2-214">Kun muodostat testitapausta, mieti, kuinka ennakoitavia kyseisten testiskenaarioiden tulos on.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-214">To build a test case, consider how predictable the outcome of those test scenarios is.</span></span>
- <span data-ttu-id="1c2a2-215">Jaa tallenteet, jos suorittajalla on eri rooli tai jos ennen seuraavaa vaihetta on odotettava tietty aika tai tiettyä ulkoista tapahtumaa.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-215">Split recordings if they are performed by different roles, or if there is waiting time or an external event before the next step.</span></span>
- <span data-ttu-id="1c2a2-216">Vältä luettelossa olevien arvojen valitsemista.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-216">Avoid selecting values in lists.</span></span> <span data-ttu-id="1c2a2-217">Käytä sen sijaan tekstimuotoja, kuten **FIFO**, **AudioRM** ja **SiteWH**.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-217">Instead, use text formats, such as **FIFO**, **AudioRM**, and **SiteWH**.</span></span> <span data-ttu-id="1c2a2-218">Jos valinta tehdään luettelossa, arvon sijainti luettelossa tallennetaan eikä itse arvoa.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-218">When you select in a list, the position of the value in the list is recorded, not the value itself.</span></span> <span data-ttu-id="1c2a2-219">Jos kyseiseen luetteloon lisätään nimikkeitä, arvon sijainti voi muuttua.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-219">If items are added to that list, the position of the value can change.</span></span> <span data-ttu-id="1c2a2-220">Tämän vuoksi tallenne käyttää eri parametria, mikä voi vaikuttaa skenaarion muihin osiin.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-220">Therefore, your recording will use a different parameter, and the rest of the scenario might be affected.</span></span>
- <span data-ttu-id="1c2a2-221">Mieti tilannetta, jossa käyttäjiä on useita.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-221">Think about multi-user behavior.</span></span> <span data-ttu-id="1c2a2-222">Älä esimerkiksi oleta, että juuri luotu myyntitilaus valitaan aina automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-222">For example, don't assume that your newly created sales order will always be automatically selected.</span></span> <span data-ttu-id="1c2a2-223">Etsi sen sijaan oikea tilaus aina suodattimella.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-223">Instead, always use the filter to find the correct order.</span></span>
- <span data-ttu-id="1c2a2-224">Tallenna juuri luodun tuotteen nimi tehtävän tallennustoiminnon kopiointitoiminnolla, jolloin sitä voidaan käyttää ketjutetuissa testitapauksissa.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-224">Use the Copy function in Task recorder to save the name of a newly created product so it can be used in chained test cases.</span></span>
- <span data-ttu-id="1c2a2-225">Määritä tehtävän tallennustoiminnon tarkistustoiminnolla tarkistuspisteet tarkistamaan, että vaiheet on suoritettu oikein.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-225">Use the Validate function in Task recorder to set checkpoints that verify that steps have been run correctly.</span></span>

### <a name="rsat"></a><span data-ttu-id="1c2a2-226">RSAT</span><span class="sxs-lookup"><span data-stu-id="1c2a2-226">RSAT</span></span>

- <span data-ttu-id="1c2a2-227">Jos suorittaa testin toisessa yrityksessä, voit vaihtaa yrityksen Excelin parametritiedoston **Yleiset**-välilehdessä.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-227">To run the test in another company, you can change the company on the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="1c2a2-228">Varmista, että asetuksia ja tietoja voi käyttää juuri valitussa yrityksessä.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-228">Make sure that settings and data are available in the newly selected company.</span></span>
- <span data-ttu-id="1c2a2-229">Voit vaihtaa testikäyttäjän Excelin parametritiedoston **Yleiset**-välilehdessä.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-229">You can change the test user on the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="1c2a2-230">Määritä testitapauksen suorittavan käyttäjän sähköpostitunnus.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-230">Specify the email ID of the user who will run the test case.</span></span> <span data-ttu-id="1c2a2-231">Tällä tavoin testitapaus voidaan suorittaa turvallisesti käyttämällä määritetyn käyttäjän suojausoikeuksia.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-231">In this way, the test case can be run by using the security permissions of the specified user.</span></span>
- <span data-ttu-id="1c2a2-232">Jos haluat odottaa ennen testin aloittamista, voit määrittää tauon Excelin parametritiedoston **Yleiset**-välilehdessä.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-232">To wait before the test is started, you can define a pause on the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="1c2a2-233">Tätä taukoa voidaan käyttää erätyössä (jos esimerkiksi työnkulku on suoritettava, ennen kuin seuraava vaihe voidaan suorittaa).</span><span class="sxs-lookup"><span data-stu-id="1c2a2-233">This pause can be used in a batch job (for example, if a workflow must be run before the next step can be performed.)</span></span>

## <a name="advanced-scripting"></a><span data-ttu-id="1c2a2-234">Edistyneet komentosarjat</span><span class="sxs-lookup"><span data-stu-id="1c2a2-234">Advanced scripting</span></span>

### <a name="cli"></a><span data-ttu-id="1c2a2-235">CLI</span><span class="sxs-lookup"><span data-stu-id="1c2a2-235">CLI</span></span>

<span data-ttu-id="1c2a2-236">RSAT voidaan kutsua **Komentokehote**- tai **PowerShell**-ikkunasta.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-236">RSAT can be called from a **Command Prompt** or **PowerShell** window.</span></span>

> [!NOTE]
> <span data-ttu-id="1c2a2-237">Tarkista, että **TestRoot**-ympäristömuuttujan asetukseksi on määritetty RSAT-asennuspolku.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-237">Verify that the **TestRoot** environment variable is set to the RSAT installation path.</span></span> <span data-ttu-id="1c2a2-238">(Avaa Microsoft Windowsissa **Ohjauspaneeli**, valitse sitten **Järjestelmä ja suojaus \> Järjestelmä \> Järjestelmän lisäasetukset** ja valitse lopuksi **Ympäristömuuttujat**.)</span><span class="sxs-lookup"><span data-stu-id="1c2a2-238">(In Microsoft Windows, open **Control Panel**, select **System and Security \> System \> Advanced system settings**, and then select **Environment Variables**.)</span></span>

1. <span data-ttu-id="1c2a2-239">Avaa **Komentokehote**- tai **PowerShell**-ikkuna järjestelmänvalvojana.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-239">Open a **Command Prompt** or **PowerShell** window as an admin.</span></span>
2. <span data-ttu-id="1c2a2-240">Siirry RSAT-asennushakemistoon.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-240">Navigate to the RSAT installation directory.</span></span>

    ```Console
    cd "c:\Program Files (x86)\Regression Suite Automation Tool\"
    ```

3. <span data-ttu-id="1c2a2-241">Luettele kaikki komennot.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-241">List all commands.</span></span>

    ```Console
    C:\Program Files (x86)\Regression Suite Automation Tool>Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe help

    Usage:
        Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe command
        or
        Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe /settings "C:\Path to\file.settings" command

    Available commands:
        ?
        about
        cls
        download
        edit
        generate
        generatederived
        generatetestonly
        generatetestsuite
        help
        list
        listtestplans
        listtestsuite
        listtestsuitenames
        playback
        playbackbyid
        playbackmany
        playbacksuite
        quit
        upload
        uploadrecording
        usage
    ```

#### <a name=""></a><span data-ttu-id="1c2a2-242">?</span><span class="sxs-lookup"><span data-stu-id="1c2a2-242">?</span></span> 
<span data-ttu-id="1c2a2-243">Näyttää kaikkien käytettävissä olevien komentojen ja niiden parametrien ohjeen.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-243">Shows help about all available commands and their parameters.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``?``**``[command]``

##### <a name="optional-parameters"></a><span data-ttu-id="1c2a2-244">Valinnaiset parametrit</span><span class="sxs-lookup"><span data-stu-id="1c2a2-244">Optional parameters</span></span>

**``command``**


<span data-ttu-id="1c2a2-245">Jossa ``[command]`` on yksi alla määritetyistä komennoista.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-245">Where ``[command]`` is one of the commands specified below.</span></span>


#### <a name="about"></a><span data-ttu-id="1c2a2-246">tietoja</span><span class="sxs-lookup"><span data-stu-id="1c2a2-246">about</span></span>
<span data-ttu-id="1c2a2-247">Näyttää nykyisen version.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-247">Displays the current version.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``about``**

#### <a name="cls"></a><span data-ttu-id="1c2a2-248">cls</span><span class="sxs-lookup"><span data-stu-id="1c2a2-248">cls</span></span>
<span data-ttu-id="1c2a2-249">Tyhjentää näytön.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-249">Clears the screen.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``cls``**


#### <a name="download"></a><span data-ttu-id="1c2a2-250">lataa</span><span class="sxs-lookup"><span data-stu-id="1c2a2-250">download</span></span>
<span data-ttu-id="1c2a2-251">Lataa määritetyn testitapauksen liitteet tulostushakemistoon.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-251">Downloads attachments for the specified test case to the output directory.</span></span> <span data-ttu-id="1c2a2-252">Voit käyttää ``list``-komentoa kaikkien käytettävissä olevien testitapausten hakemisessa.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-252">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="1c2a2-253">Käytä mitä tahansa ensimmäisen sarakkeen arvoa **test_case_id**-parametrina.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-253">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``download``**``[test_case_id] [output_dir]``

##### <a name="required-parameters"></a><span data-ttu-id="1c2a2-254">Pakolliset parametrit</span><span class="sxs-lookup"><span data-stu-id="1c2a2-254">Required parameters</span></span>
<span data-ttu-id="1c2a2-255">**``test_case_id``** - edustaa testitapauksen tunnusta.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-255">**``test_case_id``** Represents the test case ID.</span></span>  
<span data-ttu-id="1c2a2-256">**``output_dir``** - edustaa tulostushakemistoa.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-256">**``output_dir``** Represents the output directory.</span></span> <span data-ttu-id="1c2a2-257">Hakemisto on määritettävä.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-257">The directory must exist.</span></span>

##### <a name="examples"></a><span data-ttu-id="1c2a2-258">Esimerkkejä</span><span class="sxs-lookup"><span data-stu-id="1c2a2-258">Examples</span></span>

``download 123 c:\temp\rsat``   
``download 765 c:\rsat\last``


#### <a name="edit"></a><span data-ttu-id="1c2a2-259">muokkaa</span><span class="sxs-lookup"><span data-stu-id="1c2a2-259">edit</span></span>
<span data-ttu-id="1c2a2-260">Voit avata parametritiedoston Excel-ohjelmassa ja muokata sitä.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-260">Allows you to open parameters file in Excel program and edit it.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``edit``**``[excel_file]``

##### <a name="required-parameters"></a><span data-ttu-id="1c2a2-261">Pakolliset parametrit</span><span class="sxs-lookup"><span data-stu-id="1c2a2-261">Required parameters</span></span>
<span data-ttu-id="1c2a2-262">**``excel_file``** - olemassa olevan Excel-tiedoston täydellinen polku on oltava.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-262">**``excel_file``** Must contain a full path to an existing Excel file.</span></span>

##### <a name="examples"></a><span data-ttu-id="1c2a2-263">Esimerkkejä</span><span class="sxs-lookup"><span data-stu-id="1c2a2-263">Examples</span></span>
``edit c:\RSAT\TestCase_123_Base.xlsx``  
``edit e:\temp\TestCase_456_Base.xlsx``


#### <a name="generate"></a><span data-ttu-id="1c2a2-264">luo</span><span class="sxs-lookup"><span data-stu-id="1c2a2-264">generate</span></span>
<span data-ttu-id="1c2a2-265">Luo testisuorituksen ja parametritiedostot määritetylle testitapaukselle tulostushakemistossa.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-265">Generates test execution and parameter files for the specified test case in the output directory.</span></span>
<span data-ttu-id="1c2a2-266">Voit käyttää ``list``-komentoa kaikkien käytettävissä olevien testitapausten hakemisessa.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-266">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="1c2a2-267">Käytä mitä tahansa ensimmäisen sarakkeen arvoa **test_case_id**-parametrina.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-267">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generate``**``[test_case_id] [output_dir]``

##### <a name="required-parameters"></a><span data-ttu-id="1c2a2-268">Pakolliset parametrit</span><span class="sxs-lookup"><span data-stu-id="1c2a2-268">Required parameters</span></span>
<span data-ttu-id="1c2a2-269">**``test_case_id``** - edustaa testitapauksen tunnusta.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-269">**``test_case_id``** Represents the test case ID.</span></span>  
<span data-ttu-id="1c2a2-270">**``output_dir``** - edustaa tulostushakemistoa.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-270">**``output_dir``** Represents the output directory.</span></span> <span data-ttu-id="1c2a2-271">Hakemisto on määritettävä.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-271">The directory must exist.</span></span>

##### <a name="examples"></a><span data-ttu-id="1c2a2-272">Esimerkkejä</span><span class="sxs-lookup"><span data-stu-id="1c2a2-272">Examples</span></span>
``generate 123 c:\temp\rsat``  
``generate 765 c:\rsat\last``


#### <a name="generatederived"></a><span data-ttu-id="1c2a2-273">generatederived</span><span class="sxs-lookup"><span data-stu-id="1c2a2-273">generatederived</span></span>
<span data-ttu-id="1c2a2-274">Luo uuden testitapauksen, joka johdetaan annetusta testitapauksesta.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-274">Generates a new test case, derived from the provided test case.</span></span> <span data-ttu-id="1c2a2-275">Voit käyttää ``list``-komentoa kaikkien käytettävissä olevien testitapausten hakemisessa.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-275">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="1c2a2-276">Käytä mitä tahansa ensimmäisen sarakkeen arvoa **test_case_id**-parametrina.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-276">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatederived``**``[parent_test_case_id] [test_plan_id] [test_suite_id]``

##### <a name="required-parameters"></a><span data-ttu-id="1c2a2-277">Pakolliset parametrit</span><span class="sxs-lookup"><span data-stu-id="1c2a2-277">Required parameters</span></span>
<span data-ttu-id="1c2a2-278">**``parent_test_case_id``** - edustaa päätestitapauksen tunnusta.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-278">**``parent_test_case_id``** Represents the parent test case ID.</span></span>  
<span data-ttu-id="1c2a2-279">**``test_plan_id``** - edustaa testisuunnitelman tunnusta.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-279">**``test_plan_id``** Represents the test plan ID.</span></span>  
<span data-ttu-id="1c2a2-280">**``test_suite_id``** - edustaa testiohjelmistopaketin tunnusta.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-280">**``test_suite_id``** Represents the test suite ID.</span></span>

##### <a name="examples"></a><span data-ttu-id="1c2a2-281">Esimerkkejä</span><span class="sxs-lookup"><span data-stu-id="1c2a2-281">Examples</span></span>
``generatederived 123 8901 678``


#### <a name="generatetestonly"></a><span data-ttu-id="1c2a2-282">generatetestonly</span><span class="sxs-lookup"><span data-stu-id="1c2a2-282">generatetestonly</span></span>
<span data-ttu-id="1c2a2-283">Luo vain testisuoritustiedoston määritetylle testitapaukselle tulostushakemistossa.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-283">Generates only test execution file for the specified test case in the output directory.</span></span> <span data-ttu-id="1c2a2-284">Voit käyttää ``list``-komentoa kaikkien käytettävissä olevien testitapausten hakemisessa.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-284">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="1c2a2-285">Käytä mitä tahansa ensimmäisen sarakkeen arvoa **test_case_id**-parametrina.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-285">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatetestonly``**``[test_case_id] [output_dir]``

##### <a name="required-parameters"></a><span data-ttu-id="1c2a2-286">Pakolliset parametrit</span><span class="sxs-lookup"><span data-stu-id="1c2a2-286">Required parameters</span></span>
<span data-ttu-id="1c2a2-287">**``test_case_id``** - edustaa testitapauksen tunnusta.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-287">**``test_case_id``** Represents the test case ID.</span></span>  
<span data-ttu-id="1c2a2-288">**``output_dir``** - edustaa tulostushakemistoa.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-288">**``output_dir``** Represents the output directory.</span></span> <span data-ttu-id="1c2a2-289">Hakemisto on määritettävä.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-289">The directory must exist.</span></span>

##### <a name="examples"></a><span data-ttu-id="1c2a2-290">Esimerkkejä</span><span class="sxs-lookup"><span data-stu-id="1c2a2-290">Examples</span></span>
``generatetestonly 123 c:\temp\rsat``  
``generatetestonly 765 c:\rsat\last``


#### <a name="generatetestsuite"></a><span data-ttu-id="1c2a2-291">generatetestsuite</span><span class="sxs-lookup"><span data-stu-id="1c2a2-291">generatetestsuite</span></span>
<span data-ttu-id="1c2a2-292">Luo määritetyn ohjelmistopaketin kaikki testitapaukset tulostushakemistoon.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-292">Generates all test cases for the specified suite in the output directory.</span></span>
<span data-ttu-id="1c2a2-293">Voit käyttää ``listtestsuitenames``-komentoa kaikkien käytettävissä olevien testiohjelmistopakettien hakemisessa.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-293">You can use ``listtestsuitenames`` command to get all available test suits.</span></span> <span data-ttu-id="1c2a2-294">Käytä mitä tahansa sarakkeen arvoa **test_suite_name**-parametrina.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-294">Use any value from the column as a **test_suite_name** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatetestsuite``**``[test_suite_name] [output_dir]``

##### <a name="required-parameters"></a><span data-ttu-id="1c2a2-295">Pakolliset parametrit</span><span class="sxs-lookup"><span data-stu-id="1c2a2-295">Required parameters</span></span>
<span data-ttu-id="1c2a2-296">**``test_suite_name``** - edustaa testiohjelmistopaketin nimeä.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-296">**``test_suite_name``** Represents the test suite name.</span></span>  
<span data-ttu-id="1c2a2-297">**``output_dir``** - edustaa tulostushakemistoa.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-297">**``output_dir``** Represents the output directory.</span></span> <span data-ttu-id="1c2a2-298">Hakemisto on määritettävä.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-298">The directory must exist.</span></span>

##### <a name="examples"></a><span data-ttu-id="1c2a2-299">Esimerkkejä</span><span class="sxs-lookup"><span data-stu-id="1c2a2-299">Examples</span></span>
``generatetestsuite Tests c:\temp\rsat``   
``generatetestsuite Purchase c:\rsat\last``


#### <a name="help"></a><span data-ttu-id="1c2a2-300">ohje</span><span class="sxs-lookup"><span data-stu-id="1c2a2-300">help</span></span>
<span data-ttu-id="1c2a2-301">Sama kuin [?](####?)</span><span class="sxs-lookup"><span data-stu-id="1c2a2-301">Identical to the [?](####?)</span></span> <span data-ttu-id="1c2a2-302">komento</span><span class="sxs-lookup"><span data-stu-id="1c2a2-302">command</span></span>


#### <a name="list"></a><span data-ttu-id="1c2a2-303">luettelo</span><span class="sxs-lookup"><span data-stu-id="1c2a2-303">list</span></span>
<span data-ttu-id="1c2a2-304">Luettelo kaikista käytettävissä olevista testitapauksista.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-304">Lists all available test cases.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``list``**


#### <a name="listtestplans"></a><span data-ttu-id="1c2a2-305">listtestplans</span><span class="sxs-lookup"><span data-stu-id="1c2a2-305">listtestplans</span></span>
<span data-ttu-id="1c2a2-306">Luettelo kaikista käytettävissä olevista testisuunnitelmista.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-306">Lists all available test plans.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestplans``**


#### <a name="listtestsuite"></a><span data-ttu-id="1c2a2-307">listtestsuite</span><span class="sxs-lookup"><span data-stu-id="1c2a2-307">listtestsuite</span></span>
<span data-ttu-id="1c2a2-308">Luettelo määritetyn testiohjelmistopaketin testitapauksista.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-308">Lists test cases for the specified test suite.</span></span> <span data-ttu-id="1c2a2-309">Voit käyttää ``listtestsuitenames``-komentoa kaikkien käytettävissä olevien testiohjelmistopakettien hakemisessa.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-309">You can use ``listtestsuitenames`` command to get all available test suites.</span></span> <span data-ttu-id="1c2a2-310">Käytä mitä tahansa ensimmäisen sarakkeen arvoa **suite_name**-parametrina.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-310">Use any value from first column as **suite_name** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestsuite``**``[suite_name]``

##### <a name="required-parameters"></a><span data-ttu-id="1c2a2-311">Pakolliset parametrit</span><span class="sxs-lookup"><span data-stu-id="1c2a2-311">Required parameters</span></span>
<span data-ttu-id="1c2a2-312">**``suite_name``** - halutun ohjelmistopaketin nimi.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-312">**``suite_name``** Name of the desired suite.</span></span>

##### <a name="examples"></a><span data-ttu-id="1c2a2-313">Esimerkkejä</span><span class="sxs-lookup"><span data-stu-id="1c2a2-313">Examples</span></span>
``listtestsuite "sample suite name"``  
``listtestsuite NameOfTheSuite``


#### <a name="listtestsuitenames"></a><span data-ttu-id="1c2a2-314">listtestsuitenames</span><span class="sxs-lookup"><span data-stu-id="1c2a2-314">listtestsuitenames</span></span>
<span data-ttu-id="1c2a2-315">Luettelo kaikista käytettävissä olevista testiohjelmistopaketeista.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-315">Lists all available test suites.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestsuitenames``**


#### <a name="playback"></a><span data-ttu-id="1c2a2-316">toisto</span><span class="sxs-lookup"><span data-stu-id="1c2a2-316">playback</span></span>
<span data-ttu-id="1c2a2-317">Toistaa testitapauksen Excel-tiedoston avulla.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-317">Plays back a test case using an Excel file.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playback``**``[excel_file]``

##### <a name="required-parameters"></a><span data-ttu-id="1c2a2-318">Pakolliset parametrit</span><span class="sxs-lookup"><span data-stu-id="1c2a2-318">Required parameters</span></span>
<span data-ttu-id="1c2a2-319">**``excel_file``** - Excel-tiedoston täydellinen polku.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-319">**``excel_file``** A full path to the Excel file.</span></span> <span data-ttu-id="1c2a2-320">Tiedoston on oltava olemassa.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-320">File must exist.</span></span> 

##### <a name="examples"></a><span data-ttu-id="1c2a2-321">Esimerkkejä</span><span class="sxs-lookup"><span data-stu-id="1c2a2-321">Examples</span></span>
``
playback c:\RSAT\TestCaseParameters\sample1.xlsx
playback e:\temp\test.xlsx
``


#### <a name="playbackbyid"></a><span data-ttu-id="1c2a2-322">playbackbyid</span><span class="sxs-lookup"><span data-stu-id="1c2a2-322">playbackbyid</span></span>
<span data-ttu-id="1c2a2-323">Toistaa useita testitapauksia kerralla.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-323">Plays back multiple test cases at once.</span></span>
<span data-ttu-id="1c2a2-324">Voit käyttää ``list``-komentoa kaikkien käytettävissä olevien testitapausten hakemisessa.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-324">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="1c2a2-325">Käytä mitä tahansa ensimmäisen sarakkeen arvoa **test_case_id**-parametrina.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-325">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbackbyid``**``[test_case_id1] [test_case_id2] ... [test_case_idN]``

##### <a name="required-parameters"></a><span data-ttu-id="1c2a2-326">Pakolliset parametrit</span><span class="sxs-lookup"><span data-stu-id="1c2a2-326">Required parameters</span></span>
<span data-ttu-id="1c2a2-327">**``test_case_id1``** - olemassa olevan testitapauksen tunnus.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-327">**``test_case_id1``** ID of exisiting test case.</span></span>  
<span data-ttu-id="1c2a2-328">**``test_case_id2``** - olemassa olevan testitapauksen tunnus.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-328">**``test_case_id2``** ID of exisiting test case.</span></span>  
<span data-ttu-id="1c2a2-329">**``test_case_idN``** - olemassa olevan testitapauksen tunnus.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-329">**``test_case_idN``** ID of exisiting test case.</span></span>  

##### <a name="examples"></a><span data-ttu-id="1c2a2-330">Esimerkkejä</span><span class="sxs-lookup"><span data-stu-id="1c2a2-330">Examples</span></span>
``playbackbyid 878``  
``playbackbyid 2345 667 135``


#### <a name="playbackmany"></a><span data-ttu-id="1c2a2-331">playbackmany</span><span class="sxs-lookup"><span data-stu-id="1c2a2-331">playbackmany</span></span>
<span data-ttu-id="1c2a2-332">Toistaa useita testitapauksia kerralla Excel-tiedostojen avulla.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-332">Plays back many test cases at once, using Excel files.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbackmany``**``[excel_file1] [excel_file2] ... [excel_fileN]``

##### <a name="required-parameters"></a><span data-ttu-id="1c2a2-333">Pakolliset parametrit</span><span class="sxs-lookup"><span data-stu-id="1c2a2-333">Required parameters</span></span>
<span data-ttu-id="1c2a2-334">**``excel_file1``** - Excel-tiedoston täydellinen polku.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-334">**``excel_file1``** Full path to the Excel file.</span></span> <span data-ttu-id="1c2a2-335">Tiedoston on oltava olemassa.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-335">File must exist.</span></span>  
<span data-ttu-id="1c2a2-336">**``excel_file2``** - Excel-tiedoston täydellinen polku.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-336">**``excel_file2``** Full path to the Excel file.</span></span> <span data-ttu-id="1c2a2-337">Tiedoston on oltava olemassa.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-337">File must exist.</span></span>  
<span data-ttu-id="1c2a2-338">**``excel_fileN``** - Excel-tiedoston täydellinen polku.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-338">**``excel_fileN``** Full path to the Excel file.</span></span> <span data-ttu-id="1c2a2-339">Tiedoston on oltava olemassa.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-339">File must exist.</span></span>  

##### <a name="examples"></a><span data-ttu-id="1c2a2-340">Esimerkkejä</span><span class="sxs-lookup"><span data-stu-id="1c2a2-340">Examples</span></span>
``playbackmany c:\RSAT\TestCaseParameters\param1.xlsx``  
``playbackmany e:\temp\test.xlsx f:\rsat\sample1.xlsx c:\RSAT\sample2.xlsx``


#### <a name="playbacksuite"></a><span data-ttu-id="1c2a2-341">playbacksuite</span><span class="sxs-lookup"><span data-stu-id="1c2a2-341">playbacksuite</span></span>
<span data-ttu-id="1c2a2-342">Toistaa kaikki testitapaukset määritetystä testiohjelmistopaketista.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-342">Plays back all test cases from the specified test suite.</span></span> <span data-ttu-id="1c2a2-343">Voit käyttää ``listtestsuitenames``-komentoa kaikkien käytettävissä olevien testiohjelmistopakettien hakemisessa.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-343">You can use ``listtestsuitenames`` command to get all available test suites.</span></span> <span data-ttu-id="1c2a2-344">Käytä mitä tahansa ensimmäisen sarakkeen arvoa **suite_name**-parametrina.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-344">Use any value from first column as **suite_name** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbacksuite``**``[suite_name]``

##### <a name="required-parameters"></a><span data-ttu-id="1c2a2-345">Pakolliset parametrit</span><span class="sxs-lookup"><span data-stu-id="1c2a2-345">Required parameters</span></span>
<span data-ttu-id="1c2a2-346">**``suite_name``** - halutun ohjelmistopaketin nimi.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-346">**``suite_name``** Name of the desired suite.</span></span>

##### <a name="examples"></a><span data-ttu-id="1c2a2-347">Esimerkkejä</span><span class="sxs-lookup"><span data-stu-id="1c2a2-347">Examples</span></span>
``playbacksuite suiteName``  
``playbacksuite sample_suite``


#### <a name="quit"></a><span data-ttu-id="1c2a2-348">lopeta</span><span class="sxs-lookup"><span data-stu-id="1c2a2-348">quit</span></span>
<span data-ttu-id="1c2a2-349">Sulkee sovelluksen.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-349">Closes the  application.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``quit``**


#### <a name="upload"></a><span data-ttu-id="1c2a2-350">lataa</span><span class="sxs-lookup"><span data-stu-id="1c2a2-350">upload</span></span>
<span data-ttu-id="1c2a2-351">Lataa kaikki määritettyyn testiohjelmistopakettiin tai määritettyihin testitapauksiin kuuluvat tiedostot.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-351">Uploads all files belonging to the specified test suite or test cases.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``upload``**``[suite_name] [testcase_id]``

#### <a name="required-parameters"></a><span data-ttu-id="1c2a2-352">Pakolliset parametrit</span><span class="sxs-lookup"><span data-stu-id="1c2a2-352">Required parameters</span></span>
<span data-ttu-id="1c2a2-353">**``suite_name``** - kaikki tiettyyn testiohjelmistopakettiin kuuluvat tiedostot ladataan.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-353">**``suite_name``** All files belonging to the specified test suite will be uploaded.</span></span>
<span data-ttu-id="1c2a2-354">**``testcase_id``** - kaikki tiettyihin testitapauksiin kuuluvat tiedostot ladataan.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-354">**``testcase_id``** All files beloning to the specified test case(s) will be uploaded.</span></span>

##### <a name="examples"></a><span data-ttu-id="1c2a2-355">Esimerkkejä</span><span class="sxs-lookup"><span data-stu-id="1c2a2-355">Examples</span></span>
``upload sample_suite``  
``upload 123``  
``upload 123 456``


#### <a name="uploadrecording"></a><span data-ttu-id="1c2a2-356">uploadrecording</span><span class="sxs-lookup"><span data-stu-id="1c2a2-356">uploadrecording</span></span>
<span data-ttu-id="1c2a2-357">Lataa vain määritettyihin testitapauksiin kuuluvan tallennustiedoston.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-357">Uploads only recording file belonging to the specified test cases.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``uploadrecording``**``[testcase_id]``

##### <a name="required-parameters"></a><span data-ttu-id="1c2a2-358">Pakolliset parametrit</span><span class="sxs-lookup"><span data-stu-id="1c2a2-358">Required parameters</span></span>
<span data-ttu-id="1c2a2-359">**``testcase_id``** - määritettyihin testitapauksiin kuuluva tallennustiedosto ladataan.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-359">**``testcase_id``** Recording file belonging to the specified test cases will be uploaded.</span></span>

##### <a name="examples"></a><span data-ttu-id="1c2a2-360">Esimerkkejä</span><span class="sxs-lookup"><span data-stu-id="1c2a2-360">Examples</span></span>
``uploadrecording 123``  
``uploadrecording 123 456``


#### <a name="usage"></a><span data-ttu-id="1c2a2-361">käyttö</span><span class="sxs-lookup"><span data-stu-id="1c2a2-361">usage</span></span>
<span data-ttu-id="1c2a2-362">Näyttää kaksi tapaa, joilla tätä sovellusta voi kutsua: toisessa käytetään oletusasetustiedostoa ja toinen määrittää asetustiedoston.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-362">Shows two ways to invoke this application: one using a default setting file, another one providing a setting file.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``usage``**


### <a name="windows-powershell-examples"></a><span data-ttu-id="1c2a2-363">Windows PowerShell -esimerkkejä</span><span class="sxs-lookup"><span data-stu-id="1c2a2-363">Windows PowerShell examples</span></span>

#### <a name="run-a-test-case-in-a-loop"></a><span data-ttu-id="1c2a2-364">Testitapauksen suorittaminen silmukkana</span><span class="sxs-lookup"><span data-stu-id="1c2a2-364">Run a test case in a loop</span></span>

<span data-ttu-id="1c2a2-365">Sinulla on uuden asiakkaan luova testikomentosarja.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-365">You have a test script that creates a new customer.</span></span> <span data-ttu-id="1c2a2-366">Tämä testisarja voidaan suorittaa komentosarjojen avulla silmukkana muodostamalla seuraavat tiedot satunnaisesti ennen kunkin iteraation suorittamista:</span><span class="sxs-lookup"><span data-stu-id="1c2a2-366">Via scripting, this test case can be run in a loop by randomizing the following data before each iteration is run:</span></span>

- <span data-ttu-id="1c2a2-367">Asiakastunnus</span><span class="sxs-lookup"><span data-stu-id="1c2a2-367">Customer ID</span></span>
- <span data-ttu-id="1c2a2-368">Asiakkaan nimi</span><span class="sxs-lookup"><span data-stu-id="1c2a2-368">Customer name</span></span>
- <span data-ttu-id="1c2a2-369">Asiakkaan osoitetiedot</span><span class="sxs-lookup"><span data-stu-id="1c2a2-369">Customer address</span></span>

<span data-ttu-id="1c2a2-370">Asiakastunnuksen muoto on seuraavanlainen: *ATCUS\<numero\>*, jossa \<numeron\> arvo on **000000001**–**999999999**.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-370">The customer ID will be in the format *ATCUS\<number\>*, where \<number\> is a value between **000000001** and **999999999**.</span></span>

<span data-ttu-id="1c2a2-371">Seuraavassa esimerkissä käytetään yhtä **aloitus**-parametria määrittämään ensimmäinen käytettävä numero.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-371">The following example uses one parameter, **start**, to define the first number that is used.</span></span> <span data-ttu-id="1c2a2-372">Is käyttää seuraavaa parametria **nr** määrittämään luotavien asiakkaiden määrän.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-372">Is uses a second parameter, **nr**, to define the number of customers that must be created.</span></span> <span data-ttu-id="1c2a2-373">Excelin parametritiedoston parametrit muutetaan kussakin iteraatiossa käyttämällä UpdateCustomer-funktiota.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-373">For each iteration, the parameters in the Excel parameter file are changed by using an UpdateCustomer function.</span></span> <span data-ttu-id="1c2a2-374">RSAT-komentorivi kutsutaan sitten RunTestCase-funktiolla.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-374">Then the RSAT command line is called in a RunTestCase function.</span></span>

<span data-ttu-id="1c2a2-375">Avaa integroitu Microsoft Windows PowerShell -komentosarjaympäristö (ISE) järjestelmänvalvojan tilassa ja liitä seuraava koodi **Untitled1.ps1**-nimiseen ikkunaan.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-375">Open Microsoft Windows PowerShell Integrated Scripting Environment (ISE) in admin mode, and paste the following code into the window that is named **Untitled1.ps1**.</span></span>

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

#### <a name="run-a-script-that-depends-on-data-in-microsoft-dynamics-365"></a><span data-ttu-id="1c2a2-376">Microsoft Dynamics 365:n tiedoista riippuvaisen komentosarjan suorittaminen</span><span class="sxs-lookup"><span data-stu-id="1c2a2-376">Run a script that depends on data in Microsoft Dynamics 365</span></span>

<span data-ttu-id="1c2a2-377">Seuraavassa esimerkissä ostotilauksen tila etsitään Open Data Protocol (OData) -kutsun avulla.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-377">The following example uses an Open Data Protocol (OData) call to find the order status of a purchase order.</span></span> <span data-ttu-id="1c2a2-378">Jos tila ei ole **invoiced**, voit esimerkiksi kutsua laskun kirjaavan RSAT-testitapauksen.</span><span class="sxs-lookup"><span data-stu-id="1c2a2-378">If the status isn't **invoiced**, you can, for example, call an RSAT test case that posts the invoice.</span></span>

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
