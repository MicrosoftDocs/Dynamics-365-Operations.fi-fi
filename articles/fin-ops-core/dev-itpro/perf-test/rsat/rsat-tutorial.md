---
title: Regression Suite Automation Tool -opas
description: Tässä ohjeaiheessa käsitellään Regression Suite Automation Tool (RSAT) -työkalun käyttämistä. Siinä käsitellään erilaisia toimintoja ja annetaan esimerkkejä edistyneestä komentosarjojen käytöstä.
author: robinarh
manager: AnnBe
ms.date: 01/15/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: rhaertle
ms.custom: 21761
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: AX 7.0.0, Operations
ms.openlocfilehash: 7c4c0f9340085341ab60f97b55dacf36624e5f46
ms.sourcegitcommit: b337b647a1be4908fc361fb6d962e96a69f301a9
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/21/2021
ms.locfileid: "5036707"
---
# <a name="regression-suite-automation-tool-tutorial"></a><span data-ttu-id="d895f-104">Regression Suite Automation Tool -opas</span><span class="sxs-lookup"><span data-stu-id="d895f-104">Regression suite automation tool tutorial</span></span>

[!include [banner](../../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="d895f-105">Lataa ja tallenna tämä ohje selaimen työkaluilla PDF-tiedostona.</span><span class="sxs-lookup"><span data-stu-id="d895f-105">Use your internet browser tools to download and save this page in pdf format.</span></span>

<span data-ttu-id="d895f-106">Tässä oppaassa käsitellään yksityiskohtaisesti Regression Suite Automation Tool (RSAT) -työkalun lisätoimintoja. Se sisältää myös demon määrityksen ja siinä käsitellään strategiaa ja keskeisiä opittavia asioita.</span><span class="sxs-lookup"><span data-stu-id="d895f-106">This tutorial walks through some of the advanced features of the Regression suite automation tool (RSAT), includes a demo assignment, and describes strategy and key learning points.</span></span>

## <a name="notable-features-of-rsat-and-task-recorder"></a><span data-ttu-id="d895f-107">RSAT:in ja tehtävien tallennustoiminnon merkittävimmät ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="d895f-107">Notable Features of RSAT and Task recorder</span></span>

### <a name="validate-a-field-value"></a><span data-ttu-id="d895f-108">Kentän arvon tarkistaminen</span><span class="sxs-lookup"><span data-stu-id="d895f-108">Validate a field value</span></span>

<span data-ttu-id="d895f-109">RSAT-toiminnon avulla voit sisällyttää odotettuihin arvoihin oikeellisuustarkistusvaiheet.</span><span class="sxs-lookup"><span data-stu-id="d895f-109">RSAT allows you to include validation steps within your test case to validate expected values.</span></span> <span data-ttu-id="d895f-110">Lisätietoja tästä ominaisuudesta on artikkelissa [Tarkista odotetut arvot](rsat-validate-expected.md).</span><span class="sxs-lookup"><span data-stu-id="d895f-110">For information about this feature, see the article [Validate expected values](rsat-validate-expected.md).</span></span>

<span data-ttu-id="d895f-111">Seuraava esimerkki osoittaa, miten tällä toiminnolla tarkistetaan, onko varastosaldo suurempi kuin 0 (nolla).</span><span class="sxs-lookup"><span data-stu-id="d895f-111">The following example shows how you can use this feature to validate whether the on-hand inventory is more than 0 (zero).</span></span>

1. <span data-ttu-id="d895f-112">Luo demotietojen **USMF**-yrityksessä tehtävätallenne, jossa on seuraavat vaiheet:</span><span class="sxs-lookup"><span data-stu-id="d895f-112">In the demo data in the **USMF** company, create a task recording that has the following steps:</span></span>

    1. <span data-ttu-id="d895f-113">Mene **Tuotetietojen hallinta \> Tuotteet \> Vapautetut tuotteet**.</span><span class="sxs-lookup"><span data-stu-id="d895f-113">Go to **Product information management \> Products \> Released products**.</span></span>
    2. <span data-ttu-id="d895f-114">Käytä pikasuodatinta tietueiden etsimiseen.</span><span class="sxs-lookup"><span data-stu-id="d895f-114">Use the Quick Filter to find records.</span></span> <span data-ttu-id="d895f-115">Voit esimerkiksi suodattaa **Nimiketunnus**-kenttää arvolla **1000**.</span><span class="sxs-lookup"><span data-stu-id="d895f-115">For example, filter on a value of **1000** for the **Item number** field.</span></span>
    3. <span data-ttu-id="d895f-116">Valitse **Käytettävissä oleva varasto**.</span><span class="sxs-lookup"><span data-stu-id="d895f-116">Select **On-hand inventory**.</span></span>
    4. <span data-ttu-id="d895f-117">Käytä pikasuodatinta tietueiden etsimiseen.</span><span class="sxs-lookup"><span data-stu-id="d895f-117">Use the Quick Filter to find records.</span></span> <span data-ttu-id="d895f-118">Voit esimerkiksi suodattaa **Toimipaikka**-kenttää arvolla **1**.</span><span class="sxs-lookup"><span data-stu-id="d895f-118">For example, filter on a value of **1** for the **Site** field.</span></span>
    5. <span data-ttu-id="d895f-119">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="d895f-119">In the list, mark the selected row.</span></span>
    6. <span data-ttu-id="d895f-120">Tarkista, että **Yhteensä käytettävissä** -kentän arvo on **411,0000000000000000**.</span><span class="sxs-lookup"><span data-stu-id="d895f-120">Validate that the value of the **Total available** field is **411.0000000000000000**.</span></span>

2. <span data-ttu-id="d895f-121">Tallenna tehtävätallenne **kehittäjän tallenteena** ja liitä se testitapaukseen Azure DevOpsissa.</span><span class="sxs-lookup"><span data-stu-id="d895f-121">Save the task recording as a **developer recording** and attach it to your test case in Azure Devops.</span></span>
3. <span data-ttu-id="d895f-122">Lisää testitapaus testisuunnitelmaan ja lataa testitapaus RSAT-työkaluun.</span><span class="sxs-lookup"><span data-stu-id="d895f-122">Add the test case to the test plan, and load the test case into RSAT.</span></span>
4. <span data-ttu-id="d895f-123">Avaa Excel-parametritiedosto ja siirry **TestCaseSteps**-välilehteen.</span><span class="sxs-lookup"><span data-stu-id="d895f-123">Open the Excel parameter file and go to the **TestCaseSteps** tab.</span></span>
5. <span data-ttu-id="d895f-124">Jos haluat tarkistaa, että käytettävissä oleva varasto on aina yli **0**, muuta **Yhteensä käytettävissä olevan tarkistaminen** -vaiheessa tämä arvo arvosta **411** arvoksi **0**.</span><span class="sxs-lookup"><span data-stu-id="d895f-124">To validate whether the inventory on-hand will always be more than **0**, go to the **Validate Total Available** step and change its value from **411** to **0**.</span></span> <span data-ttu-id="d895f-125">Muuta **Operaattori**-kentän arvo, yhtäsuuruusmerkki (**=**), suurempi kuin -merkiksi (**\>**).</span><span class="sxs-lookup"><span data-stu-id="d895f-125">Change the value of the **Operator** field from an equal sign (**=**) to a greater than sign (**\>**).</span></span>
6. <span data-ttu-id="d895f-126">Tallenna ja sulje Excelin parametritiedosto.</span><span class="sxs-lookup"><span data-stu-id="d895f-126">Save and close the Excel parameter file.</span></span>
7. <span data-ttu-id="d895f-127">Tallenna Excelin parametritiedostoon tehdyt muutokset Azure DevOpsiin valitsemalla **Lataa palvelimeen**.</span><span class="sxs-lookup"><span data-stu-id="d895f-127">Select **Upload** to save the changes that you made to the Excel parameter file to Azure DevOps.</span></span>

<span data-ttu-id="d895f-128">Huomaa, että jos tietyn nimikkeen **Yhteensä käytettävissä** -kentän arvo varastossa on suurempi kuin 0 (nolla), testi hyväksytään todellisen varastosaldon arvosta riippumatta.</span><span class="sxs-lookup"><span data-stu-id="d895f-128">Now, if the value of the **Total Available** field for the specified item in inventory is more than 0 (zero), tests will pass, regardless of the actual on-hand inventory value.</span></span>

### <a name="saved-variables-and-chaining-of-test-cases"></a><span data-ttu-id="d895f-129">Testitapausten tallennetut muuttujat ja ketjutus</span><span class="sxs-lookup"><span data-stu-id="d895f-129">Saved variables and chaining of test cases</span></span>

<span data-ttu-id="d895f-130">Yksi RSAT-työkalun keskeisistä ominaisuuksista on testitapausten ketjuttaminen, eli ominaisuus, jolla testi voi siirtää muuttujat toisiin testeihin.</span><span class="sxs-lookup"><span data-stu-id="d895f-130">One of the key features of RSAT is the chaining of test cases, that is, the ability of a test to pass variables to other tests.</span></span> <span data-ttu-id="d895f-131">Lisätietoja on artikkelissa [Kopioi muuttujat ketjutestitapauksiin](rsat-chain-test-cases.md).</span><span class="sxs-lookup"><span data-stu-id="d895f-131">For more information, see the article [Copy variables to chain test cases](rsat-chain-test-cases.md).</span></span>

### <a name="derived-test-case"></a><span data-ttu-id="d895f-132">Johdettu testitapaus</span><span class="sxs-lookup"><span data-stu-id="d895f-132">Derived test case</span></span>

<span data-ttu-id="d895f-133">RSAT-toiminnon avulla voit käyttää samaa tehtävätallennetta useissa testitapauksissa, jolloin tehtävä voidaan suorittaa eri tietokonfiguraatioiden avulla.</span><span class="sxs-lookup"><span data-stu-id="d895f-133">RSAT lets you use the same task recording with multiple test cases, enabling a task to run with different data configurations.</span></span> <span data-ttu-id="d895f-134">Lisätietoja on artikkelissa [Johdetut testitapaukset](rsat-derived-test-cases.md).</span><span class="sxs-lookup"><span data-stu-id="d895f-134">See the article [Derived test cases](rsat-derived-test-cases.md) for more information.</span></span>

### <a name="validate-notifications-and-messages"></a><span data-ttu-id="d895f-135">Ilmoitusten ja sanomien vahvistaminen</span><span class="sxs-lookup"><span data-stu-id="d895f-135">Validate notifications and messages</span></span>

<span data-ttu-id="d895f-136">Tällä toiminnolla tarkistetaan, tapahtuiko toiminto.</span><span class="sxs-lookup"><span data-stu-id="d895f-136">This feature can be used to validate whether an action occurred.</span></span> <span data-ttu-id="d895f-137">Kun esimerkiksi tuotantotilaus luodaan, arvioidaan ja aloitetaan, sovellus ilmoittaa Tuotanto - käynnistys -sanomalla, että tuotantotilaus on aloitettu.</span><span class="sxs-lookup"><span data-stu-id="d895f-137">For example, when a production order is created, estimated, and then started, the app shows a "Production – Start" message to notify you that the production order has been started.</span></span>

![Tuotanto - käynnistys -ilmoitus](./media/use_rsa_tool_05.png)

<span data-ttu-id="d895f-139">Voit tarkistaa tämän sanoman RSAT-työkalussa etsimällä kyseisen tallenteen antamalla sanoman tekstin Excelin parametritiedoston **Viestin tarkistus**-välilehdessä.</span><span class="sxs-lookup"><span data-stu-id="d895f-139">You can validate this message through RSAT by entering the message text on the **MessageValidation** tab of the Excel parameter file for the appropriate recording.</span></span>

![Viestin tarkistus -välilehti](./media/use_rsa_tool_06.png)

<span data-ttu-id="d895f-141">Kun testitapaus on suoritettu, Excelin parametritiedostoa verrataan näytettävään sanomaan.</span><span class="sxs-lookup"><span data-stu-id="d895f-141">After the test case is run, the message in the Excel parameter file is compared to the message that is shown.</span></span> <span data-ttu-id="d895f-142">Jos sanomat eivät vastaa toisiaan, testitapaus epäonnistuu.</span><span class="sxs-lookup"><span data-stu-id="d895f-142">If the messages don't match, the test case will fail.</span></span>

> [!NOTE]
> <span data-ttu-id="d895f-143">Voit antaa Excelin parametritiedoston **Viestitarkistus**-välilehdessä useita sanomia.</span><span class="sxs-lookup"><span data-stu-id="d895f-143">You can enter more than one message on the **MessageValidation** tab in the Excel parameter file.</span></span> <span data-ttu-id="d895f-144">Sanomat voivat myös olla virhe- tai varoitussanomia ilmoitussanomien sijaan.</span><span class="sxs-lookup"><span data-stu-id="d895f-144">The messages also can be error or warning messages instead of informational messages.</span></span>

### <a name="snapshot"></a><span data-ttu-id="d895f-145">Tilannevedos</span><span class="sxs-lookup"><span data-stu-id="d895f-145">Snapshot</span></span>

<span data-ttu-id="d895f-146">Tämä toiminto ottaa näyttökuvat tehtävätallenteen aikana suoritetuista vaiheista.</span><span class="sxs-lookup"><span data-stu-id="d895f-146">This feature takes screenshots of the steps that were performed during task recording.</span></span> <span data-ttu-id="d895f-147">Se on hyödyllinen tarkistus- tai virheenkorjaustarkoituksiin.</span><span class="sxs-lookup"><span data-stu-id="d895f-147">It is useful for auditing or debugging purposes.</span></span>

- <span data-ttu-id="d895f-148">Avaa tällä toiminnolla **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config**-tiedosto RSAT-asennuskansiossa (esimerkiksi kansiossa **C:\\Program Files (x86)\\Regression Suite Automation Tool**) ja muuta seuraavan elementin arvo **epätosi** arvoksi **tosi**.</span><span class="sxs-lookup"><span data-stu-id="d895f-148">To use this feature, open the **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** file under the RSAT installation folder (for example, **C:\\Program Files (x86)\\Regression Suite Automation Tool**), and change the value of the following element from **false** to **true**.</span></span>

    ```xml
    <add key="VerboseSnapshotsEnabled" value="false" />
    ```

<span data-ttu-id="d895f-149">Kun ajat testitapauksen, RSAT luo tilannevedoksia (kuvia) vaiheista, jotka näytetään työskentelyhakemistossa olevien testitapausten toistokansiossa.</span><span class="sxs-lookup"><span data-stu-id="d895f-149">When your run the test case, RSAT will generate snapshots (images) of the steps in the playback folder of the test cases in the working diretory.</span></span> <span data-ttu-id="d895f-150">Jos käytät vanhaa RSAT-versiota, kuvat tallennetaan kohteeseen **C:\\Käyttäjät\\\<Username\>\\AppData\\verkkovierailu\\regressionTool\\toisto**, erillinen kansio luodaan kullekin testitapaukselle, joka suoritetaan.</span><span class="sxs-lookup"><span data-stu-id="d895f-150">If you are using an older version of RSAT, the images are saved to **C:\\Users\\\<Username\>\\AppData\\Roaming\\regressionTool\\playback**, a separate folder is created for each test case that is run.</span></span>

## <a name="assignment"></a><span data-ttu-id="d895f-151">Toimeksianto</span><span class="sxs-lookup"><span data-stu-id="d895f-151">Assignment</span></span>

### <a name="scenario"></a><span data-ttu-id="d895f-152">Skenaario</span><span class="sxs-lookup"><span data-stu-id="d895f-152">Scenario</span></span>

1. <span data-ttu-id="d895f-153">Tuote suunnittelija luo uuden julkaistun tuotteen.</span><span class="sxs-lookup"><span data-stu-id="d895f-153">The product designer creates a new released product.</span></span>
2. <span data-ttu-id="d895f-154">Tuotantopäällikkö käynnistää tuotantotilauksen, joka nostaa varastotason kahteen kappaleeseen.</span><span class="sxs-lookup"><span data-stu-id="d895f-154">The production manager initiates a production order to bring the stock level to two pieces.</span></span>
3. <span data-ttu-id="d895f-155">Valmistus alkaa ja päättää tuotantotilauksen sekä varmistaa, että varastosaldo on kaksi kappaletta.</span><span class="sxs-lookup"><span data-stu-id="d895f-155">Manufacturing starts and ends the production order, and verifies that the on-hand quantity is two pieces.</span></span>
4. <span data-ttu-id="d895f-156">Myyntiryhmä vastaanottaa tilauksen, jossa on neljä kappaletta uutta tuotetta.</span><span class="sxs-lookup"><span data-stu-id="d895f-156">The sales team receives an order for four pieces of the new product.</span></span> <span data-ttu-id="d895f-157">Tämän vuoksi myyntiryhmä päivittää nettotarpeen dynaamisen suunnitelman kautta.</span><span class="sxs-lookup"><span data-stu-id="d895f-157">Therefore, the sales team updates the net requirements via the dynamic plan.</span></span> <span data-ttu-id="d895f-158">Koska lisäkapasiteettia ei ole käytettävissä, tilausten oletuskäytännöksi on määritetty ostaminen valmistamisen sijaan.</span><span class="sxs-lookup"><span data-stu-id="d895f-158">Because no additional capacity is available, the default order policy is set to "buy instead of make."</span></span> <span data-ttu-id="d895f-159">Tämän vuoksi luodaan suunnitellun ostotilauksen.</span><span class="sxs-lookup"><span data-stu-id="d895f-159">Therefore, a planned purchase order is created.</span></span>
5. <span data-ttu-id="d895f-160">Ostaja lisää toimittajan, vahvistaa suunnitellun ostotilauksen ja vahvistaa lopuksi ostotilauksen.</span><span class="sxs-lookup"><span data-stu-id="d895f-160">The buyer adds a vendor, firms the planned purchase order, and then confirms the purchase order.</span></span>
6. <span data-ttu-id="d895f-161">Kun ostetut tavarat saapuvat myymälään, myymäläkäyttäjä hakee liittyvän ostotilauksen ja vastaanottaa tavarat.</span><span class="sxs-lookup"><span data-stu-id="d895f-161">When the goods that were purchased arrive at the store, the store operator searches the related purchase order and receives the goods.</span></span> <span data-ttu-id="d895f-162">Koska tilaus on nyt valmis, tavarat voidaan kerätä ja pakata myyntitilauksen mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="d895f-162">Because the order is now completed, goods can be picked and packed against the sales order.</span></span>
7. <span data-ttu-id="d895f-163">Talousosasta kirjaa osto- ja myyntilaskun.</span><span class="sxs-lookup"><span data-stu-id="d895f-163">Finance posts the purchase invoice and sales invoice.</span></span>

<span data-ttu-id="d895f-164">Seuraavassa kuvassa on tämän skenaarion työnkulku.</span><span class="sxs-lookup"><span data-stu-id="d895f-164">The following illustration shows the flow for this scenario.</span></span>

![Demoskenaarion työnkulku](./media/use_rsa_tool_14.png)

<span data-ttu-id="d895f-166">Seuraavassa kuvassa näkyy tämän skenaarion liiketoimintaprosessien hierarkia LCS-liiketoimintaprosessin mallintajassa.</span><span class="sxs-lookup"><span data-stu-id="d895f-166">The following illustration shows the business processes hierarchy for this scenario in the LCS Business Process Modeler.</span></span>

![Demoskenaarion liiketoimintaprosessit](./media/use_rsa_tool_15.png)

## <a name="strategy--key-learning"></a><span data-ttu-id="d895f-168">Strategia – keskeinen opittava asia</span><span class="sxs-lookup"><span data-stu-id="d895f-168">Strategy – Key learning</span></span>

### <a name="data"></a><span data-ttu-id="d895f-169">Tiedot</span><span class="sxs-lookup"><span data-stu-id="d895f-169">Data</span></span>

- <span data-ttu-id="d895f-170">Varmista, että sinulla on tarvittavat tiedot (tuotanto-/ihannekonfiguraatiotietojen kopio ja siirretyt tiedot).</span><span class="sxs-lookup"><span data-stu-id="d895f-170">Make sure that you have representative data volumes (a copy of production/golden configuration data plus migrated data).</span></span>
- <span data-ttu-id="d895f-171">Jos luot uusia tietoja tehtävän tallennustoiminnon kautta, luo sellaiset testinimet, jotka eivät ole ristiriidassa aiemmin luotujen nimien kanssa. (Käytä esimerkiksi etuliitettä, kuten **RSATxxx**).</span><span class="sxs-lookup"><span data-stu-id="d895f-171">When you generate new data via Task recorder, create test names that won't conflict with existing names (for example, use a prefix such as **RSATxxx**).</span></span>
- <span data-ttu-id="d895f-172">Suorita testit uudelleen muissa kuin tason 1 ympäristöissä käyttämällä Azuren ajankohtaan perustuvaa palautusta.</span><span class="sxs-lookup"><span data-stu-id="d895f-172">Use Azure Point-In-Time restore to rerun tests in non-Tier 1 environments.</span></span>
- <span data-ttu-id="d895f-173">Vaikka voit muodostaa ainutlaatuisia yhdistelmiä Excelin **SATUNNAINEN**- ja **NYT**-funktioita, sen työmäärä on huomattavan suuri.</span><span class="sxs-lookup"><span data-stu-id="d895f-173">Although you can use the **RANDOM** and **NOW** Excel functions to generate a unique combination, the effort is considerably high.</span></span> <span data-ttu-id="d895f-174">Esimerkki:</span><span class="sxs-lookup"><span data-stu-id="d895f-174">Here is an example.</span></span>

    ```Excel
    product = "AT" &TEXT(NOW(),"yyymmddhhmm")
    ```

### <a name="task-recorder"></a><span data-ttu-id="d895f-175">Tehtävän tallennus</span><span class="sxs-lookup"><span data-stu-id="d895f-175">Task recorder</span></span>

- <span data-ttu-id="d895f-176">Määritä skenaariot ennen tallentamisen aloittamista.</span><span class="sxs-lookup"><span data-stu-id="d895f-176">Define scenarios before you start recording.</span></span> <span data-ttu-id="d895f-177">Hyvin hallitussa projektissa on ennalta määritetyt testiskenaariot.</span><span class="sxs-lookup"><span data-stu-id="d895f-177">A well-managed project has predefined test scenarios.</span></span> <span data-ttu-id="d895f-178">Kun muodostat testitapausta, mieti, kuinka ennakoitavia kyseisten testiskenaarioiden tulos on.</span><span class="sxs-lookup"><span data-stu-id="d895f-178">To build a test case, consider how predictable the outcome of those test scenarios is.</span></span>
- <span data-ttu-id="d895f-179">Jaa tallenteet, jos suorittajalla on eri rooli tai jos ennen seuraavaa vaihetta on odotettava tietty aika tai tiettyä ulkoista tapahtumaa.</span><span class="sxs-lookup"><span data-stu-id="d895f-179">Split recordings if they are performed by different roles, or if there is waiting time or an external event before the next step.</span></span>
- <span data-ttu-id="d895f-180">Vältä luettelossa olevien arvojen valitsemista.</span><span class="sxs-lookup"><span data-stu-id="d895f-180">Avoid selecting values in lists.</span></span> <span data-ttu-id="d895f-181">Käytä sen sijaan tekstimuotoja, kuten **FIFO**, **AudioRM** ja **SiteWH**.</span><span class="sxs-lookup"><span data-stu-id="d895f-181">Instead, use text formats, such as **FIFO**, **AudioRM**, and **SiteWH**.</span></span> <span data-ttu-id="d895f-182">Jos valinta tehdään luettelossa, arvon sijainti luettelossa tallennetaan eikä itse arvoa.</span><span class="sxs-lookup"><span data-stu-id="d895f-182">When you select in a list, the position of the value in the list is recorded, not the value itself.</span></span> <span data-ttu-id="d895f-183">Jos kyseiseen luetteloon lisätään nimikkeitä, arvon sijainti voi muuttua.</span><span class="sxs-lookup"><span data-stu-id="d895f-183">If items are added to that list, the position of the value can change.</span></span> <span data-ttu-id="d895f-184">Tämän vuoksi tallenne käyttää eri parametria, mikä voi vaikuttaa skenaarion muihin osiin.</span><span class="sxs-lookup"><span data-stu-id="d895f-184">Therefore, your recording will use a different parameter, and the rest of the scenario might be affected.</span></span>
- <span data-ttu-id="d895f-185">Mieti tilannetta, jossa käyttäjiä on useita.</span><span class="sxs-lookup"><span data-stu-id="d895f-185">Think about multi-user behavior.</span></span> <span data-ttu-id="d895f-186">Älä esimerkiksi oleta, että juuri luotu myyntitilaus valitaan aina automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="d895f-186">For example, don't assume that your newly created sales order will always be automatically selected.</span></span> <span data-ttu-id="d895f-187">Etsi sen sijaan oikea tilaus aina suodattimella.</span><span class="sxs-lookup"><span data-stu-id="d895f-187">Instead, always use the filter to find the correct order.</span></span>
- <span data-ttu-id="d895f-188">Tallenna juuri luodun tuotteen nimi tehtävän tallennustoiminnon kopiointitoiminnolla, jolloin sitä voidaan käyttää ketjutetuissa testitapauksissa.</span><span class="sxs-lookup"><span data-stu-id="d895f-188">Use the Copy function in Task recorder to save the name of a newly created product so it can be used in chained test cases.</span></span>
- <span data-ttu-id="d895f-189">Määritä tehtävän tallennustoiminnon tarkistustoiminnolla tarkistuspisteet tarkistamaan, että vaiheet on suoritettu oikein.</span><span class="sxs-lookup"><span data-stu-id="d895f-189">Use the Validate function in Task recorder to set checkpoints that verify that steps have been run correctly.</span></span>

### <a name="rsat"></a><span data-ttu-id="d895f-190">RSAT</span><span class="sxs-lookup"><span data-stu-id="d895f-190">RSAT</span></span>

- <span data-ttu-id="d895f-191">Jos suorittaa testin toisessa yrityksessä, voit vaihtaa yrityksen Excelin parametritiedoston **Yleiset**-välilehdessä.</span><span class="sxs-lookup"><span data-stu-id="d895f-191">To run the test in another company, you can change the company on the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="d895f-192">Varmista, että asetuksia ja tietoja voi käyttää juuri valitussa yrityksessä.</span><span class="sxs-lookup"><span data-stu-id="d895f-192">Make sure that settings and data are available in the newly selected company.</span></span>
- <span data-ttu-id="d895f-193">Voit vaihtaa testikäyttäjän Excelin parametritiedoston **Yleiset**-välilehdessä.</span><span class="sxs-lookup"><span data-stu-id="d895f-193">You can change the test user on the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="d895f-194">Määritä testitapauksen suorittavan käyttäjän sähköpostitunnus.</span><span class="sxs-lookup"><span data-stu-id="d895f-194">Specify the email ID of the user who will run the test case.</span></span> <span data-ttu-id="d895f-195">Tällä tavoin testitapaus voidaan suorittaa turvallisesti käyttämällä määritetyn käyttäjän suojausoikeuksia.</span><span class="sxs-lookup"><span data-stu-id="d895f-195">In this way, the test case can be run by using the security permissions of the specified user.</span></span>
- <span data-ttu-id="d895f-196">Jos haluat odottaa ennen testin aloittamista, voit määrittää tauon Excelin parametritiedoston **Yleiset**-välilehdessä.</span><span class="sxs-lookup"><span data-stu-id="d895f-196">To wait before the test is started, you can define a pause on the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="d895f-197">Tätä taukoa voidaan käyttää erätyössä (jos esimerkiksi työnkulku on suoritettava, ennen kuin seuraava vaihe voidaan suorittaa).</span><span class="sxs-lookup"><span data-stu-id="d895f-197">This pause can be used in a batch job (for example, if a workflow must be run before the next step can be performed.)</span></span>

## <a name="advanced-scripting"></a><span data-ttu-id="d895f-198">Edistyneet komentosarjat</span><span class="sxs-lookup"><span data-stu-id="d895f-198">Advanced scripting</span></span>

### <a name="cli"></a><span data-ttu-id="d895f-199">CLI</span><span class="sxs-lookup"><span data-stu-id="d895f-199">CLI</span></span>

<span data-ttu-id="d895f-200">RSAT voidaan kutsua **Komentokehote**- tai **PowerShell**-ikkunasta.</span><span class="sxs-lookup"><span data-stu-id="d895f-200">RSAT can be called from a **Command Prompt** or **PowerShell** window.</span></span>

> [!NOTE]
> <span data-ttu-id="d895f-201">Tarkista, että **TestRoot**-ympäristömuuttujan asetukseksi on määritetty RSAT-asennuspolku.</span><span class="sxs-lookup"><span data-stu-id="d895f-201">Verify that the **TestRoot** environment variable is set to the RSAT installation path.</span></span> <span data-ttu-id="d895f-202">(Avaa Microsoft Windowsissa **Ohjauspaneeli**, valitse sitten **Järjestelmä ja suojaus \> Järjestelmä \> Järjestelmän lisäasetukset** ja valitse lopuksi **Ympäristömuuttujat**.)</span><span class="sxs-lookup"><span data-stu-id="d895f-202">(In Microsoft Windows, open **Control Panel**, select **System and Security \> System \> Advanced system settings**, and then select **Environment Variables**.)</span></span>

1. <span data-ttu-id="d895f-203">Avaa **Komentokehote**- tai **PowerShell**-ikkuna järjestelmänvalvojana.</span><span class="sxs-lookup"><span data-stu-id="d895f-203">Open a **Command Prompt** or **PowerShell** window as an admin.</span></span>
2. <span data-ttu-id="d895f-204">Siirry RSAT-asennushakemistoon.</span><span class="sxs-lookup"><span data-stu-id="d895f-204">Navigate to the RSAT installation directory.</span></span>

    ```Console
    cd "c:\Program Files (x86)\Regression Suite Automation Tool\"
    ```

3. <span data-ttu-id="d895f-205">Luettele kaikki komennot.</span><span class="sxs-lookup"><span data-stu-id="d895f-205">List all commands.</span></span>

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

#### <a name=""></a><span data-ttu-id="d895f-206">?</span><span class="sxs-lookup"><span data-stu-id="d895f-206">?</span></span>

<span data-ttu-id="d895f-207">Näyttää kaikkien käytettävissä olevien komentojen ja niiden parametrien ohjeen.</span><span class="sxs-lookup"><span data-stu-id="d895f-207">Shows help about all available commands and their parameters.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``?``**``[command]``

##### <a name="-optional-parameters"></a><span data-ttu-id="d895f-208">?: Valinnaiset parametrit</span><span class="sxs-lookup"><span data-stu-id="d895f-208">?: Optional parameters</span></span>

<span data-ttu-id="d895f-209">`command`: jossa ``[command]`` on yksi alla määritetyistä komennoista.</span><span class="sxs-lookup"><span data-stu-id="d895f-209">`command`: Where ``[command]`` is one of the commands specified below.</span></span>

#### <a name="about"></a><span data-ttu-id="d895f-210">tietoja</span><span class="sxs-lookup"><span data-stu-id="d895f-210">about</span></span>

<span data-ttu-id="d895f-211">Näyttää nykyisen version.</span><span class="sxs-lookup"><span data-stu-id="d895f-211">Displays the current version.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``about``**

#### <a name="cls"></a><span data-ttu-id="d895f-212">cls</span><span class="sxs-lookup"><span data-stu-id="d895f-212">cls</span></span>

<span data-ttu-id="d895f-213">Tyhjentää näytön.</span><span class="sxs-lookup"><span data-stu-id="d895f-213">Clears the screen.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``cls``**

#### <a name="download"></a><span data-ttu-id="d895f-214">lataa</span><span class="sxs-lookup"><span data-stu-id="d895f-214">download</span></span>

<span data-ttu-id="d895f-215">Lataa määritetyn testitapauksen liitteet tulostushakemistoon.</span><span class="sxs-lookup"><span data-stu-id="d895f-215">Downloads attachments for the specified test case to the output directory.</span></span>
<span data-ttu-id="d895f-216">Voit käyttää ``list``-komentoa kaikkien käytettävissä olevien testitapausten hakemisessa.</span><span class="sxs-lookup"><span data-stu-id="d895f-216">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="d895f-217">Käytä mitä tahansa ensimmäisen sarakkeen arvoa **test_case_id**-parametrina.</span><span class="sxs-lookup"><span data-stu-id="d895f-217">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``download``**``[test_case_id] [output_dir]``

##### <a name="download-required-parameters"></a><span data-ttu-id="d895f-218">lataaminen: pakolliset parametrit</span><span class="sxs-lookup"><span data-stu-id="d895f-218">download: required parameters</span></span>

+ <span data-ttu-id="d895f-219">`test_case_id`: ilmaisee testitapauksen tunnuksen.</span><span class="sxs-lookup"><span data-stu-id="d895f-219">`test_case_id`: Represents the test case ID.</span></span>
+ <span data-ttu-id="d895f-220">`output_dir`: Ilmaisee tulostushakemiston.</span><span class="sxs-lookup"><span data-stu-id="d895f-220">`output_dir`: Represents the output directory.</span></span> <span data-ttu-id="d895f-221">Hakemisto on määritettävä.</span><span class="sxs-lookup"><span data-stu-id="d895f-221">The directory must exist.</span></span>

##### <a name="download-examples"></a><span data-ttu-id="d895f-222">lataa: esimerkit</span><span class="sxs-lookup"><span data-stu-id="d895f-222">download: examples</span></span>

`download 123 c:\temp\rsat`

`download 765 c:\rsat\last`

#### <a name="edit"></a><span data-ttu-id="d895f-223">muokkaa</span><span class="sxs-lookup"><span data-stu-id="d895f-223">edit</span></span>

<span data-ttu-id="d895f-224">Voit avata parametritiedoston Excel-ohjelmassa ja muokata sitä.</span><span class="sxs-lookup"><span data-stu-id="d895f-224">Allows you to open parameters file in Excel program and edit it.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``edit``**``[excel_file]``

##### <a name="edit-required-parameters"></a><span data-ttu-id="d895f-225">muokkaa: pakolliset parametrit</span><span class="sxs-lookup"><span data-stu-id="d895f-225">edit: required parameters</span></span>

+ <span data-ttu-id="d895f-226">`excel_file`: on sisällettävä täydellinen polku aiemmin luotuun Excel-tiedostoon.</span><span class="sxs-lookup"><span data-stu-id="d895f-226">`excel_file`: Must contain a full path to an existing Excel file.</span></span>

##### <a name="edit-examples"></a><span data-ttu-id="d895f-227">muokkaa: esimerkit</span><span class="sxs-lookup"><span data-stu-id="d895f-227">edit: examples</span></span>

`edit c:\RSAT\TestCase_123_Base.xlsx`

`edit e:\temp\TestCase_456_Base.xlsx`

#### <a name="generate"></a><span data-ttu-id="d895f-228">luo</span><span class="sxs-lookup"><span data-stu-id="d895f-228">generate</span></span>

<span data-ttu-id="d895f-229">Luo testisuorituksen ja parametritiedostot määritetylle testitapaukselle tulostushakemistossa.</span><span class="sxs-lookup"><span data-stu-id="d895f-229">Generates test execution and parameter files for the specified test case in the output directory.</span></span> <span data-ttu-id="d895f-230">Voit käyttää ``list``-komentoa kaikkien käytettävissä olevien testitapausten hakemisessa.</span><span class="sxs-lookup"><span data-stu-id="d895f-230">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="d895f-231">Käytä mitä tahansa ensimmäisen sarakkeen arvoa **test_case_id**-parametrina.</span><span class="sxs-lookup"><span data-stu-id="d895f-231">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generate``**``[test_case_id] [output_dir]``

##### <a name="generate-required-parameters"></a><span data-ttu-id="d895f-232">luo: pakolliset parametrit</span><span class="sxs-lookup"><span data-stu-id="d895f-232">generate: required parameters</span></span>

+ <span data-ttu-id="d895f-233">`test_case_id`: ilmaisee testitapauksen tunnuksen.</span><span class="sxs-lookup"><span data-stu-id="d895f-233">`test_case_id`: Represents the test case ID.</span></span>
+ <span data-ttu-id="d895f-234">`output_dir`: Ilmaisee tulostushakemiston.</span><span class="sxs-lookup"><span data-stu-id="d895f-234">`output_dir`: Represents the output directory.</span></span> <span data-ttu-id="d895f-235">Hakemisto on määritettävä.</span><span class="sxs-lookup"><span data-stu-id="d895f-235">The directory must exist.</span></span>

##### <a name="generate-examples"></a><span data-ttu-id="d895f-236">luo: esimerkit</span><span class="sxs-lookup"><span data-stu-id="d895f-236">generate: examples</span></span>

`generate 123 c:\temp\rsat`

`generate 765 c:\rsat\last`

#### <a name="generatederived"></a><span data-ttu-id="d895f-237">generatederived</span><span class="sxs-lookup"><span data-stu-id="d895f-237">generatederived</span></span>

<span data-ttu-id="d895f-238">Luo uuden testitapauksen, joka johdetaan annetusta testitapauksesta.</span><span class="sxs-lookup"><span data-stu-id="d895f-238">Generates a new test case, derived from the provided test case.</span></span> <span data-ttu-id="d895f-239">Voit käyttää ``list``-komentoa kaikkien käytettävissä olevien testitapausten hakemisessa.</span><span class="sxs-lookup"><span data-stu-id="d895f-239">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="d895f-240">Käytä mitä tahansa ensimmäisen sarakkeen arvoa **test_case_id**-parametrina.</span><span class="sxs-lookup"><span data-stu-id="d895f-240">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatederived``**``[parent_test_case_id] [test_plan_id] [test_suite_id]``

##### <a name="generatederived-required-parameters"></a><span data-ttu-id="d895f-241">generatederived: pakolliset parametrit</span><span class="sxs-lookup"><span data-stu-id="d895f-241">generatederived: required parameters</span></span>

+ <span data-ttu-id="d895f-242">`parent_test_case_id`: ilmaisee päätestitapauksen tunnuksen.</span><span class="sxs-lookup"><span data-stu-id="d895f-242">`parent_test_case_id`: Represents the parent test case ID.</span></span>
+ <span data-ttu-id="d895f-243">`test_plan_id`: ilmaisee testisuunnitelman tunnuksen.</span><span class="sxs-lookup"><span data-stu-id="d895f-243">`test_plan_id`: Represents the test plan ID.</span></span>
+ <span data-ttu-id="d895f-244">`test_suite_id`: ilmaisee testiohjelmistopaketin tunnusta.</span><span class="sxs-lookup"><span data-stu-id="d895f-244">`test_suite_id`: Represents the test suite ID.</span></span>

##### <a name="generatederived-examples"></a><span data-ttu-id="d895f-245">generatederived: esimerkit</span><span class="sxs-lookup"><span data-stu-id="d895f-245">generatederived: examples</span></span>

`generatederived 123 8901 678`

#### <a name="generatetestonly"></a><span data-ttu-id="d895f-246">generatetestonly</span><span class="sxs-lookup"><span data-stu-id="d895f-246">generatetestonly</span></span>

<span data-ttu-id="d895f-247">Luo vain testisuoritustiedoston määritetylle testitapaukselle tulostushakemistossa.</span><span class="sxs-lookup"><span data-stu-id="d895f-247">Generates only test execution file for the specified test case in the output directory.</span></span> <span data-ttu-id="d895f-248">Voit käyttää ``list``-komentoa kaikkien käytettävissä olevien testitapausten hakemisessa.</span><span class="sxs-lookup"><span data-stu-id="d895f-248">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="d895f-249">Käytä mitä tahansa ensimmäisen sarakkeen arvoa **test_case_id**-parametrina.</span><span class="sxs-lookup"><span data-stu-id="d895f-249">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatetestonly``**``[test_case_id] [output_dir]``

##### <a name="generatetestonly-required-parameters"></a><span data-ttu-id="d895f-250">generatetestonly: pakolliset parametrit</span><span class="sxs-lookup"><span data-stu-id="d895f-250">generatetestonly: required parameters</span></span>

+ <span data-ttu-id="d895f-251">`test_case_id`: ilmaisee testitapauksen tunnuksen.</span><span class="sxs-lookup"><span data-stu-id="d895f-251">`test_case_id`: Represents the test case ID.</span></span>
+ <span data-ttu-id="d895f-252">`output_dir`: Ilmaisee tulostushakemiston.</span><span class="sxs-lookup"><span data-stu-id="d895f-252">`output_dir`: Represents the output directory.</span></span> <span data-ttu-id="d895f-253">Hakemisto on määritettävä.</span><span class="sxs-lookup"><span data-stu-id="d895f-253">The directory must exist.</span></span>

##### <a name="generatetestonly-examples"></a><span data-ttu-id="d895f-254">generatetestonly: esimerkit</span><span class="sxs-lookup"><span data-stu-id="d895f-254">generatetestonly: examples</span></span>

`generatetestonly 123 c:\temp\rsat`

`generatetestonly 765 c:\rsat\last`

#### <a name="generatetestsuite"></a><span data-ttu-id="d895f-255">generatetestsuite</span><span class="sxs-lookup"><span data-stu-id="d895f-255">generatetestsuite</span></span>

<span data-ttu-id="d895f-256">Luo määritetyn ohjelmistopaketin kaikki testitapaukset tulostushakemistoon.</span><span class="sxs-lookup"><span data-stu-id="d895f-256">Generates all test cases for the specified suite in the output directory.</span></span> <span data-ttu-id="d895f-257">Voit käyttää ``listtestsuitenames``-komentoa kaikkien käytettävissä olevien testiohjelmistopakettien hakemisessa.</span><span class="sxs-lookup"><span data-stu-id="d895f-257">You can use ``listtestsuitenames`` command to get all available test suits.</span></span> <span data-ttu-id="d895f-258">Käytä mitä tahansa sarakkeen arvoa **test_suite_name**-parametrina.</span><span class="sxs-lookup"><span data-stu-id="d895f-258">Use any value from the column as a **test_suite_name** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatetestsuite``**``[test_suite_name] [output_dir]``

##### <a name="generatetestsuite-required-parameters"></a><span data-ttu-id="d895f-259">generatetestsuite: pakolliset parametrit</span><span class="sxs-lookup"><span data-stu-id="d895f-259">generatetestsuite: required parameters</span></span>

+ <span data-ttu-id="d895f-260">`test_suite_name`: ilmaisee testiohjelmistopaketin nimen.</span><span class="sxs-lookup"><span data-stu-id="d895f-260">`test_suite_name`: Represents the test suite name.</span></span>
+ <span data-ttu-id="d895f-261">`output_dir`: Ilmaisee tulostushakemiston.</span><span class="sxs-lookup"><span data-stu-id="d895f-261">`output_dir`: Represents the output directory.</span></span> <span data-ttu-id="d895f-262">Hakemisto on määritettävä.</span><span class="sxs-lookup"><span data-stu-id="d895f-262">The directory must exist.</span></span>

##### <a name="generatetestsuite-examples"></a><span data-ttu-id="d895f-263">generatetestsuite: esimerkit</span><span class="sxs-lookup"><span data-stu-id="d895f-263">generatetestsuite: examples</span></span>

`generatetestsuite Tests c:\temp\rsat`

`generatetestsuite Purchase c:\rsat\last`

#### <a name="help"></a><span data-ttu-id="d895f-264">ohje</span><span class="sxs-lookup"><span data-stu-id="d895f-264">help</span></span>

<span data-ttu-id="d895f-265">Sama kuin [?](#section)</span><span class="sxs-lookup"><span data-stu-id="d895f-265">Identical to the [?](#section)</span></span> <span data-ttu-id="d895f-266">-komento.</span><span class="sxs-lookup"><span data-stu-id="d895f-266">command.</span></span>

#### <a name="list"></a><span data-ttu-id="d895f-267">luettelo</span><span class="sxs-lookup"><span data-stu-id="d895f-267">list</span></span>

<span data-ttu-id="d895f-268">Luettelo kaikista käytettävissä olevista testitapauksista.</span><span class="sxs-lookup"><span data-stu-id="d895f-268">Lists all available test cases.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``list``**

#### <a name="listtestplans"></a><span data-ttu-id="d895f-269">listtestplans</span><span class="sxs-lookup"><span data-stu-id="d895f-269">listtestplans</span></span>

<span data-ttu-id="d895f-270">Luettelo kaikista käytettävissä olevista testisuunnitelmista.</span><span class="sxs-lookup"><span data-stu-id="d895f-270">Lists all available test plans.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestplans``**

#### <a name="listtestsuite"></a><span data-ttu-id="d895f-271">listtestsuite</span><span class="sxs-lookup"><span data-stu-id="d895f-271">listtestsuite</span></span>

<span data-ttu-id="d895f-272">Luettelo määritetyn testiohjelmistopaketin testitapauksista.</span><span class="sxs-lookup"><span data-stu-id="d895f-272">Lists test cases for the specified test suite.</span></span> <span data-ttu-id="d895f-273">Voit käyttää ``listtestsuitenames``-komentoa kaikkien käytettävissä olevien testiohjelmistopakettien hakemisessa.</span><span class="sxs-lookup"><span data-stu-id="d895f-273">You can use ``listtestsuitenames`` command to get all available test suites.</span></span> <span data-ttu-id="d895f-274">Käytä mitä tahansa ensimmäisen sarakkeen arvoa **suite_name**-parametrina.</span><span class="sxs-lookup"><span data-stu-id="d895f-274">Use any value from first column as **suite_name** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestsuite``**``[suite_name]``

##### <a name="listtestsuite-required-parameters"></a><span data-ttu-id="d895f-275">listtestsuite: pakolliset parametrit</span><span class="sxs-lookup"><span data-stu-id="d895f-275">listtestsuite: required parameters</span></span>

+ <span data-ttu-id="d895f-276">`suite_name`: toivotun ohjelmistopaketin nimi.</span><span class="sxs-lookup"><span data-stu-id="d895f-276">`suite_name`: Name of the desired suite.</span></span>

##### <a name="listtestsuite-examples"></a><span data-ttu-id="d895f-277">listtestsuite: esimerkit</span><span class="sxs-lookup"><span data-stu-id="d895f-277">listtestsuite: examples</span></span>

`listtestsuite "sample suite name"`

`listtestsuite NameOfTheSuite`

#### <a name="listtestsuitenames"></a><span data-ttu-id="d895f-278">listtestsuitenames</span><span class="sxs-lookup"><span data-stu-id="d895f-278">listtestsuitenames</span></span>

<span data-ttu-id="d895f-279">Luettelo kaikista käytettävissä olevista testiohjelmistopaketeista.</span><span class="sxs-lookup"><span data-stu-id="d895f-279">Lists all available test suites.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestsuitenames``**

#### <a name="playback"></a><span data-ttu-id="d895f-280">toisto</span><span class="sxs-lookup"><span data-stu-id="d895f-280">playback</span></span>

<span data-ttu-id="d895f-281">Toistaa testitapauksen Excel-tiedoston avulla.</span><span class="sxs-lookup"><span data-stu-id="d895f-281">Plays back a test case using an Excel file.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playback``**``[excel_file]``

##### <a name="playback-required-parameters"></a><span data-ttu-id="d895f-282">toisto: pakolliset parametrit</span><span class="sxs-lookup"><span data-stu-id="d895f-282">playback: required parameters</span></span>

+ <span data-ttu-id="d895f-283">`excel_file`: Excel-tiedoston täydellinen polku.</span><span class="sxs-lookup"><span data-stu-id="d895f-283">`excel_file`: A full path to the Excel file.</span></span> <span data-ttu-id="d895f-284">Tiedoston on oltava olemassa.</span><span class="sxs-lookup"><span data-stu-id="d895f-284">File must exist.</span></span>

##### <a name="playback-examples"></a><span data-ttu-id="d895f-285">toisto: esimerkit</span><span class="sxs-lookup"><span data-stu-id="d895f-285">playback: examples</span></span>

`playback c:\RSAT\TestCaseParameters\sample1.xlsx`

`playback e:\temp\test.xlsx`

#### <a name="playbackbyid"></a><span data-ttu-id="d895f-286">playbackbyid</span><span class="sxs-lookup"><span data-stu-id="d895f-286">playbackbyid</span></span>

<span data-ttu-id="d895f-287">Toistaa useita testitapauksia kerralla.</span><span class="sxs-lookup"><span data-stu-id="d895f-287">Plays back multiple test cases at once.</span></span> <span data-ttu-id="d895f-288">Voit käyttää ``list``-komentoa kaikkien käytettävissä olevien testitapausten hakemisessa.</span><span class="sxs-lookup"><span data-stu-id="d895f-288">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="d895f-289">Käytä mitä tahansa ensimmäisen sarakkeen arvoa **test_case_id**-parametrina.</span><span class="sxs-lookup"><span data-stu-id="d895f-289">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbackbyid``**``[test_case_id1] [test_case_id2] ... [test_case_idN]``

##### <a name="playbackbyid-required-parameters"></a><span data-ttu-id="d895f-290">playbackbyid: pakolliset parametrit</span><span class="sxs-lookup"><span data-stu-id="d895f-290">playbackbyid: required parameters</span></span>

+ <span data-ttu-id="d895f-291">`test_case_id1`: aiemmin luodun testitapauksen tunnus.</span><span class="sxs-lookup"><span data-stu-id="d895f-291">`test_case_id1`: ID of exisiting test case.</span></span>
+ <span data-ttu-id="d895f-292">`test_case_id2`: aiemmin luodun testitapauksen tunnus.</span><span class="sxs-lookup"><span data-stu-id="d895f-292">`test_case_id2`: ID of exisiting test case.</span></span>
+ <span data-ttu-id="d895f-293">`test_case_idN`: aiemmin luodun testitapauksen tunnus.</span><span class="sxs-lookup"><span data-stu-id="d895f-293">`test_case_idN`: ID of exisiting test case.</span></span>

##### <a name="playbackbyid-examples"></a><span data-ttu-id="d895f-294">playbackbyid: esimerkit</span><span class="sxs-lookup"><span data-stu-id="d895f-294">playbackbyid: examples</span></span>

`playbackbyid 878`

`playbackbyid 2345 667 135`

#### <a name="playbackmany"></a><span data-ttu-id="d895f-295">playbackmany</span><span class="sxs-lookup"><span data-stu-id="d895f-295">playbackmany</span></span>

<span data-ttu-id="d895f-296">Toistaa useita testitapauksia kerralla Excel-tiedostojen avulla.</span><span class="sxs-lookup"><span data-stu-id="d895f-296">Plays back many test cases at once, using Excel files.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbackmany``**``[excel_file1] [excel_file2] ... [excel_fileN]``

##### <a name="playbackmany-required-parameters"></a><span data-ttu-id="d895f-297">playbackmany: pakolliset parametrit</span><span class="sxs-lookup"><span data-stu-id="d895f-297">playbackmany: required parameters</span></span>

+ <span data-ttu-id="d895f-298">`excel_file1`: Excel-tiedoston täydellinen polku.</span><span class="sxs-lookup"><span data-stu-id="d895f-298">`excel_file1`: Full path to the Excel file.</span></span> <span data-ttu-id="d895f-299">Tiedoston on oltava olemassa.</span><span class="sxs-lookup"><span data-stu-id="d895f-299">File must exist.</span></span>
+ <span data-ttu-id="d895f-300">`excel_file2`: Excel-tiedoston täydellinen polku.</span><span class="sxs-lookup"><span data-stu-id="d895f-300">`excel_file2`: Full path to the Excel file.</span></span> <span data-ttu-id="d895f-301">Tiedoston on oltava olemassa.</span><span class="sxs-lookup"><span data-stu-id="d895f-301">File must exist.</span></span>
+ <span data-ttu-id="d895f-302">`excel_fileN`: Excel-tiedoston täydellinen polku.</span><span class="sxs-lookup"><span data-stu-id="d895f-302">`excel_fileN`: Full path to the Excel file.</span></span> <span data-ttu-id="d895f-303">Tiedoston on oltava olemassa.</span><span class="sxs-lookup"><span data-stu-id="d895f-303">File must exist.</span></span>

##### <a name="playbackmany-examples"></a><span data-ttu-id="d895f-304">playbackmany: esimerkit</span><span class="sxs-lookup"><span data-stu-id="d895f-304">playbackmany: examples</span></span>

`playbackmany c:\RSAT\TestCaseParameters\param1.xlsx`

`playbackmany e:\temp\test.xlsx f:\rsat\sample1.xlsx c:\RSAT\sample2.xlsx`

#### <a name="playbacksuite"></a><span data-ttu-id="d895f-305">playbacksuite</span><span class="sxs-lookup"><span data-stu-id="d895f-305">playbacksuite</span></span>

<span data-ttu-id="d895f-306">Toistaa kaikki testitapaukset määritetystä testiohjelmistopaketista.</span><span class="sxs-lookup"><span data-stu-id="d895f-306">Plays back all test cases from the specified test suite.</span></span>
<span data-ttu-id="d895f-307">Voit käyttää ``listtestsuitenames``-komentoa kaikkien käytettävissä olevien testiohjelmistopakettien hakemisessa.</span><span class="sxs-lookup"><span data-stu-id="d895f-307">You can use ``listtestsuitenames`` command to get all available test suites.</span></span> <span data-ttu-id="d895f-308">Käytä mitä tahansa ensimmäisen sarakkeen arvoa **suite_name**-parametrina.</span><span class="sxs-lookup"><span data-stu-id="d895f-308">Use any value from first column as **suite_name** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbacksuite``**``[suite_name]``

##### <a name="playbacksuite-required-parameters"></a><span data-ttu-id="d895f-309">playbacksuite: pakolliset parametrit</span><span class="sxs-lookup"><span data-stu-id="d895f-309">playbacksuite: required parameters</span></span>

+ <span data-ttu-id="d895f-310">`suite_name`: toivotun ohjelmistopaketin nimi.</span><span class="sxs-lookup"><span data-stu-id="d895f-310">`suite_name`: Name of the desired suite.</span></span>

##### <a name="playbacksuite-examples"></a><span data-ttu-id="d895f-311">playbacksuite: esimerkit</span><span class="sxs-lookup"><span data-stu-id="d895f-311">playbacksuite: examples</span></span>

`playbacksuite suiteName`

`playbacksuite sample_suite`

#### <a name="quit"></a><span data-ttu-id="d895f-312">lopeta</span><span class="sxs-lookup"><span data-stu-id="d895f-312">quit</span></span>

<span data-ttu-id="d895f-313">Sulkee sovelluksen.</span><span class="sxs-lookup"><span data-stu-id="d895f-313">Closes the  application.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``quit``**

#### <a name="upload"></a><span data-ttu-id="d895f-314">lataa</span><span class="sxs-lookup"><span data-stu-id="d895f-314">upload</span></span>

<span data-ttu-id="d895f-315">Lataa kaikki määritettyyn testiohjelmistopakettiin tai määritettyihin testitapauksiin kuuluvat tiedostot.</span><span class="sxs-lookup"><span data-stu-id="d895f-315">Uploads all files belonging to the specified test suite or test cases.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``upload``**``[suite_name] [testcase_id]``

#### <a name="upload-required-parameters"></a><span data-ttu-id="d895f-316">upload: pakolliset parametrit</span><span class="sxs-lookup"><span data-stu-id="d895f-316">upload: required parameters</span></span>

+ <span data-ttu-id="d895f-317">`suite_name`: kaikki tiettyyn testiohjelmistopakettiin kuuluvat tiedostot ladataan.</span><span class="sxs-lookup"><span data-stu-id="d895f-317">`suite_name`: All files belonging to the specified test suite will be uploaded.</span></span>
+ <span data-ttu-id="d895f-318">`testcase_id`: kaikki tiettyihin testitapauksiin kuuluvat tiedostot ladataan.</span><span class="sxs-lookup"><span data-stu-id="d895f-318">`testcase_id`: All files beloning to the specified test case(s) will be uploaded.</span></span>

##### <a name="upload-examples"></a><span data-ttu-id="d895f-319">upload: esimerkit</span><span class="sxs-lookup"><span data-stu-id="d895f-319">upload: examples</span></span>

`upload sample_suite`

`upload 123`

`upload 123 456`

#### <a name="uploadrecording"></a><span data-ttu-id="d895f-320">uploadrecording</span><span class="sxs-lookup"><span data-stu-id="d895f-320">uploadrecording</span></span>

<span data-ttu-id="d895f-321">Lataa vain määritettyihin testitapauksiin kuuluvan tallennustiedoston.</span><span class="sxs-lookup"><span data-stu-id="d895f-321">Uploads only recording file belonging to the specified test cases.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``uploadrecording``**``[testcase_id]``

##### <a name="uploadrecording-required-parameters"></a><span data-ttu-id="d895f-322">uploadrecording: pakolliset parametrit</span><span class="sxs-lookup"><span data-stu-id="d895f-322">uploadrecording: required parameters</span></span>

+ <span data-ttu-id="d895f-323">`testcase_id`: määritettyihin testitapauksiin kuuluva tallennustiedosto ladataan.</span><span class="sxs-lookup"><span data-stu-id="d895f-323">`testcase_id`: Recording file belonging to the specified test cases will be uploaded.</span></span>

##### <a name="uploadrecording-examples"></a><span data-ttu-id="d895f-324">uploadrecording: esimerkit</span><span class="sxs-lookup"><span data-stu-id="d895f-324">uploadrecording: examples</span></span>

`uploadrecording 123`

`uploadrecording 123 456`

#### <a name="usage"></a><span data-ttu-id="d895f-325">käyttö</span><span class="sxs-lookup"><span data-stu-id="d895f-325">usage</span></span>

<span data-ttu-id="d895f-326">Näyttää kaksi tapaa, joilla tätä sovellusta voi kutsua: toisessa käytetään oletusasetustiedostoa ja toinen määrittää asetustiedoston.</span><span class="sxs-lookup"><span data-stu-id="d895f-326">Shows two ways to invoke this application: one using a default setting file, another one providing a setting file.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``usage``**

### <a name="windows-powershell-examples"></a><span data-ttu-id="d895f-327">Windows PowerShell -esimerkkejä</span><span class="sxs-lookup"><span data-stu-id="d895f-327">Windows PowerShell examples</span></span>

#### <a name="run-a-test-case-in-a-loop"></a><span data-ttu-id="d895f-328">Testitapauksen suorittaminen silmukkana</span><span class="sxs-lookup"><span data-stu-id="d895f-328">Run a test case in a loop</span></span>

<span data-ttu-id="d895f-329">Sinulla on uuden asiakkaan luova testikomentosarja.</span><span class="sxs-lookup"><span data-stu-id="d895f-329">You have a test script that creates a new customer.</span></span> <span data-ttu-id="d895f-330">Tämä testisarja voidaan suorittaa komentosarjojen avulla silmukkana muodostamalla seuraavat tiedot satunnaisesti ennen kunkin iteraation suorittamista:</span><span class="sxs-lookup"><span data-stu-id="d895f-330">Via scripting, this test case can be run in a loop by randomizing the following data before each iteration is run:</span></span>

- <span data-ttu-id="d895f-331">Asiakastunnus</span><span class="sxs-lookup"><span data-stu-id="d895f-331">Customer ID</span></span>
- <span data-ttu-id="d895f-332">Asiakkaan nimi</span><span class="sxs-lookup"><span data-stu-id="d895f-332">Customer name</span></span>
- <span data-ttu-id="d895f-333">Asiakkaan osoite</span><span class="sxs-lookup"><span data-stu-id="d895f-333">Customer address</span></span>

<span data-ttu-id="d895f-334">Asiakastunnuksen muoto on seuraavanlainen: *ATCUS\<number\>*, jossa \<number\> on arvo on luku **000000001** ja **999999999** väliltä.</span><span class="sxs-lookup"><span data-stu-id="d895f-334">The customer ID will be in the format *ATCUS\<number\>*, where \<number\> is a value between **000000001** and **999999999**.</span></span>

<span data-ttu-id="d895f-335">Seuraavassa esimerkissä käytetään yhtä **aloitus**-parametria määrittämään ensimmäinen käytettävä numero.</span><span class="sxs-lookup"><span data-stu-id="d895f-335">The following example uses one parameter, **start**, to define the first number that is used.</span></span> <span data-ttu-id="d895f-336">Is käyttää seuraavaa parametria **nr** määrittämään luotavien asiakkaiden määrän.</span><span class="sxs-lookup"><span data-stu-id="d895f-336">Is uses a second parameter, **nr**, to define the number of customers that must be created.</span></span> <span data-ttu-id="d895f-337">Excelin parametritiedoston parametrit muutetaan kussakin iteraatiossa käyttämällä UpdateCustomer-funktiota.</span><span class="sxs-lookup"><span data-stu-id="d895f-337">For each iteration, the parameters in the Excel parameter file are changed by using an UpdateCustomer function.</span></span> <span data-ttu-id="d895f-338">RSAT-komentorivi kutsutaan sitten RunTestCase-funktiolla.</span><span class="sxs-lookup"><span data-stu-id="d895f-338">Then the RSAT command line is called in a RunTestCase function.</span></span>

<span data-ttu-id="d895f-339">Avaa integroitu Microsoft Windows PowerShell -komentosarjaympäristö (ISE) järjestelmänvalvojan tilassa ja liitä seuraava koodi **Untitled1.ps1**-nimiseen ikkunaan.</span><span class="sxs-lookup"><span data-stu-id="d895f-339">Open Microsoft Windows PowerShell Integrated Scripting Environment (ISE) in admin mode, and paste the following code into the window that is named **Untitled1.ps1**.</span></span>

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
$excelFilename = "full path to Excel parameter file"
l$sheetName = "DirPartyQuickCreateForm"
for ($i = $start; $i -lt $start + $nr; $i++ )
{
    $CustomerId = $i.ToString("000000000")
    Write-Host "customer : " $CustomerId
    UpdateCustomer $excelFilename $sheetName $CustomerId
    RunTestCase $excelFilename
```

#### <a name="run-a-script-that-depends-on-data-in-microsoft-dynamics-365"></a><span data-ttu-id="d895f-340">Microsoft Dynamics 365:n tiedoista riippuvaisen komentosarjan suorittaminen</span><span class="sxs-lookup"><span data-stu-id="d895f-340">Run a script that depends on data in Microsoft Dynamics 365</span></span>

<span data-ttu-id="d895f-341">Seuraavassa esimerkissä ostotilauksen tila etsitään Open Data Protocol (OData) -kutsun avulla.</span><span class="sxs-lookup"><span data-stu-id="d895f-341">The following example uses an Open Data Protocol (OData) call to find the order status of a purchase order.</span></span> <span data-ttu-id="d895f-342">Jos tila ei ole **invoiced**, voit esimerkiksi kutsua laskun kirjaavan RSAT-testitapauksen.</span><span class="sxs-lookup"><span data-stu-id="d895f-342">If the status isn't **invoiced**, you can, for example, call an RSAT test case that posts the invoice.</span></span>

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