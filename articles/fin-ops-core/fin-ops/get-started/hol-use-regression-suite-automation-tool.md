---
title: Regression Suite Automation Tool -oppaan käyttäminen
description: Tässä ohjeaiheessa käsitellään Regression Suite Automation Tool (RSAT) -työkalun käyttämistä. Siinä käsitellään erilaisia toimintoja ja annetaan esimerkkejä edistyneestä komentosarjojen käytöstä.
author: robinarh
manager: AnnBe
ms.date: 06/09/2019
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
ms.openlocfilehash: 798717b276e68949a9425350720bf683a37d6fb5
ms.sourcegitcommit: f5e31c34640add6d40308ac1365cc0ee60e60e24
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/08/2020
ms.locfileid: "4692987"
---
# <a name="regression-suite-automation-tool-tutorial"></a><span data-ttu-id="99aed-104">Regression Suite Automation Tool -opas</span><span class="sxs-lookup"><span data-stu-id="99aed-104">Regression suite automation tool tutorial</span></span>

[!include [banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="99aed-105">Lataa ja tallenna tämä ohje selaimen työkaluilla PDF-tiedostona.</span><span class="sxs-lookup"><span data-stu-id="99aed-105">Use your internet browser tools to download and save this page in pdf format.</span></span> 

<span data-ttu-id="99aed-106">Tässä oppaassa käsitellään yksityiskohtaisesti Regression Suite Automation Tool (RSAT) -työkalun lisätoimintoja. Se sisältää myös demon määrityksen ja siinä käsitellään strategiaa ja keskeisiä opittavia asioita.</span><span class="sxs-lookup"><span data-stu-id="99aed-106">This tutorial walks through some of the advanced features of the Regression suite automation tool (RSAT), includes a demo assignment, and describes strategy and key learning points.</span></span> 

## <a name="notable-features-of-rsat-and-task-recorder"></a><span data-ttu-id="99aed-107">RSAT:in ja tehtävien tallennustoiminnon merkittävimmät ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="99aed-107">Notable Features of RSAT and Task recorder</span></span>

### <a name="validate-a-field-value"></a><span data-ttu-id="99aed-108">Kentän arvon tarkistaminen</span><span class="sxs-lookup"><span data-stu-id="99aed-108">Validate a field value</span></span>

<span data-ttu-id="99aed-109">RSAT-toiminnon avulla voit sisällyttää odotettuihin arvoihin oikeellisuustarkistusvaiheet.</span><span class="sxs-lookup"><span data-stu-id="99aed-109">RSAT allows you to include validation steps within your test case to validate expected values.</span></span> <span data-ttu-id="99aed-110">Lisätietoja tästä ominaisuudesta on artikkelissa [Tarkista odotetut arvot](../../dev-itpro/perf-test/rsat/rsat-validate-expected.md).</span><span class="sxs-lookup"><span data-stu-id="99aed-110">For information about this feature, see the article [Validate expected values](../../dev-itpro/perf-test/rsat/rsat-validate-expected.md).</span></span>

<span data-ttu-id="99aed-111">Seuraava esimerkki osoittaa, miten tällä toiminnolla tarkistetaan, onko varastosaldo suurempi kuin 0 (nolla).</span><span class="sxs-lookup"><span data-stu-id="99aed-111">The following example shows how you can use this feature to validate whether the on-hand inventory is more than 0 (zero).</span></span>

1. <span data-ttu-id="99aed-112">Luo demotietojen **USMF**-yrityksessä tehtävätallenne, jossa on seuraavat vaiheet:</span><span class="sxs-lookup"><span data-stu-id="99aed-112">In the demo data in the **USMF** company, create a task recording that has the following steps:</span></span>

    1. <span data-ttu-id="99aed-113">Mene **Tuotetietojen hallinta \> Tuotteet \> Vapautetut tuotteet**.</span><span class="sxs-lookup"><span data-stu-id="99aed-113">Go to **Product information management \> Products \> Released products**.</span></span>
    2. <span data-ttu-id="99aed-114">Käytä pikasuodatinta tietueiden etsimiseen.</span><span class="sxs-lookup"><span data-stu-id="99aed-114">Use the Quick Filter to find records.</span></span> <span data-ttu-id="99aed-115">Voit esimerkiksi suodattaa **Nimiketunnus**-kenttää arvolla **1000**.</span><span class="sxs-lookup"><span data-stu-id="99aed-115">For example, filter on a value of **1000** for the **Item number** field.</span></span>
    3. <span data-ttu-id="99aed-116">Valitse **Käytettävissä oleva varasto**.</span><span class="sxs-lookup"><span data-stu-id="99aed-116">Select **On-hand inventory**.</span></span>
    4. <span data-ttu-id="99aed-117">Käytä pikasuodatinta tietueiden etsimiseen.</span><span class="sxs-lookup"><span data-stu-id="99aed-117">Use the Quick Filter to find records.</span></span> <span data-ttu-id="99aed-118">Voit esimerkiksi suodattaa **Toimipaikka**-kenttää arvolla **1**.</span><span class="sxs-lookup"><span data-stu-id="99aed-118">For example, filter on a value of **1** for the **Site** field.</span></span>
    5. <span data-ttu-id="99aed-119">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="99aed-119">In the list, mark the selected row.</span></span>
    6. <span data-ttu-id="99aed-120">Tarkista, että **Yhteensä käytettävissä** -kentän arvo on **411,0000000000000000**.</span><span class="sxs-lookup"><span data-stu-id="99aed-120">Validate that the value of the **Total available** field is **411.0000000000000000**.</span></span>

2. <span data-ttu-id="99aed-121">Tallenna tehtävätallenne ja liitä se testitapaukseen Azure DevOps -ohjelmassa.</span><span class="sxs-lookup"><span data-stu-id="99aed-121">Save the task recording and attach it to your test case in Azure Devops.</span></span>
3. <span data-ttu-id="99aed-122">Lisää testitapaus testisuunnitelmaan ja lataa testitapaus RSAT-työkaluun.</span><span class="sxs-lookup"><span data-stu-id="99aed-122">Add the test case to the test plan, and load the test case into RSAT.</span></span>
4. <span data-ttu-id="99aed-123">Avaa Excelin parametritiedosto.</span><span class="sxs-lookup"><span data-stu-id="99aed-123">Open the Excel parameter file.</span></span> <span data-ttu-id="99aed-124">**Inventonhandimitem**-välilehdessä on **Tarkista InventOnhandItem** -osa, jossa on **Operaattori**-kenttä.</span><span class="sxs-lookup"><span data-stu-id="99aed-124">On the **InventOnhandItem** tab, you will see a **Validate InventOnhandItem** section that includes an **Operator** field.</span></span>

    ![Operaattorikenttä](./media/use_rsa_tool_08.png)

5. <span data-ttu-id="99aed-126">Jos haluat tarkistaa, että varastosaldo on aina yli 0, muuta **Arvo**-kentän arvo **411** arvoksi **0** ja **Operaattori**-kentän yhtä suuri kuin -merkki (**=**) suurempi kuin -merkiksi (**\>**).</span><span class="sxs-lookup"><span data-stu-id="99aed-126">To validate whether the inventory on-hand will always be more than 0, change the value of the **Value** field from **411** to **0** and the value of the **Operator** field from an equal sign (**=**) to a greater than sign (**\>**).</span></span>

    ![Arvo-ja Operaattori-kenttien muuttuneet arvot](./media/use_rsa_tool_09.png)

6. <span data-ttu-id="99aed-128">Tallenna ja sulje Excelin parametritiedosto.</span><span class="sxs-lookup"><span data-stu-id="99aed-128">Save and close the Excel parameter file.</span></span>
7. <span data-ttu-id="99aed-129">Tallenna Excelin parametritiedostoon tehdyt muutokset Azure DevOpsiin valitsemalla **Lataa palvelimeen**.</span><span class="sxs-lookup"><span data-stu-id="99aed-129">Select **Upload** to save the changes that you made to the Excel parameter file to Azure DevOps.</span></span>

<span data-ttu-id="99aed-130">Huomaa, että jos tietyn nimikkeen **Yhteensä käytettävissä** -kentän arvo varastossa on suurempi kuin 0 (nolla), testi hyväksytään todellisen varastosaldon arvosta riippumatta.</span><span class="sxs-lookup"><span data-stu-id="99aed-130">Now, if the value of the **Total Available** field for the specified item in inventory is more than 0 (zero), tests will pass, regardless of the actual on-hand inventory value.</span></span>

### <a name="saved-variables-and-chaining-of-test-cases"></a><span data-ttu-id="99aed-131">Testitapausten tallennetut muuttujat ja ketjutus</span><span class="sxs-lookup"><span data-stu-id="99aed-131">Saved variables and chaining of test cases</span></span>

<span data-ttu-id="99aed-132">Yksi RSAT-työkalun keskeisistä ominaisuuksista on testitapausten ketjuttaminen, eli ominaisuus, jolla testi voi siirtää muuttujat toisiin testeihin.</span><span class="sxs-lookup"><span data-stu-id="99aed-132">One of the key features of RSAT is the chaining of test cases, that is, the ability of a test to pass variables to other tests.</span></span> <span data-ttu-id="99aed-133">Lisätietoja on artikkelissa [Kopioi muuttujat ketjutestitapauksiin](../../dev-itpro/perf-test/rsat/rsat-chain-test-cases.md).</span><span class="sxs-lookup"><span data-stu-id="99aed-133">For more information, see the article [Copy variables to chain test cases](../../dev-itpro/perf-test/rsat/rsat-chain-test-cases.md).</span></span>

### <a name="derived-test-case"></a><span data-ttu-id="99aed-134">Johdettu testitapaus</span><span class="sxs-lookup"><span data-stu-id="99aed-134">Derived test case</span></span>

<span data-ttu-id="99aed-135">RSAT-toiminnon avulla voit käyttää samaa tehtävätallennetta useissa testitapauksissa, jolloin tehtävä voidaan suorittaa eri tietokonfiguraatioiden avulla.</span><span class="sxs-lookup"><span data-stu-id="99aed-135">RSAT lets you use the same task recording with multiple test cases, enabling a task to run with different data configurations.</span></span> <span data-ttu-id="99aed-136">Lisätietoja on artikkelissa [Johdetut testitapaukset](../../dev-itpro/perf-test/rsat/rsat-derived-test-cases.md).</span><span class="sxs-lookup"><span data-stu-id="99aed-136">See the article [Derived test cases](../../dev-itpro/perf-test/rsat/rsat-derived-test-cases.md) for more information.</span></span>

### <a name="validate-notifications-and-messages"></a><span data-ttu-id="99aed-137">Ilmoitusten ja sanomien vahvistaminen</span><span class="sxs-lookup"><span data-stu-id="99aed-137">Validate notifications and messages</span></span>

<span data-ttu-id="99aed-138">Tällä toiminnolla tarkistetaan, tapahtuiko toiminto.</span><span class="sxs-lookup"><span data-stu-id="99aed-138">This feature can be used to validate whether an action occurred.</span></span> <span data-ttu-id="99aed-139">Kun esimerkiksi tuotantotilaus luodaan, arvioidaan ja aloitetaan, sovellus ilmoittaa Tuotanto - käynnistys -sanomalla, että tuotantotilaus on aloitettu.</span><span class="sxs-lookup"><span data-stu-id="99aed-139">For example, when a production order is created, estimated, and then started, the app shows a "Production – Start" message to notify you that the production order has been started.</span></span>

![Tuotanto - käynnistys -ilmoitus](./media/use_rsa_tool_05.png)

<span data-ttu-id="99aed-141">Voit tarkistaa tämän sanoman RSAT-työkalussa etsimällä kyseisen tallenteen antamalla sanoman tekstin Excelin parametritiedoston **Viestin tarkistus**-välilehdessä.</span><span class="sxs-lookup"><span data-stu-id="99aed-141">You can validate this message through RSAT by entering the message text on the **MessageValidation** tab of the Excel parameter file for the appropriate recording.</span></span>

![Viestin tarkistus -välilehti](./media/use_rsa_tool_06.png)

<span data-ttu-id="99aed-143">Kun testitapaus on suoritettu, Excelin parametritiedostoa verrataan näytettävään sanomaan.</span><span class="sxs-lookup"><span data-stu-id="99aed-143">After the test case is run, the message in the Excel parameter file is compared to the message that is shown.</span></span> <span data-ttu-id="99aed-144">Jos sanomat eivät vastaa toisiaan, testitapaus epäonnistuu.</span><span class="sxs-lookup"><span data-stu-id="99aed-144">If the messages don't match, the test case will fail.</span></span>

> [!NOTE]
> <span data-ttu-id="99aed-145">Voit antaa Excelin parametritiedoston **Viestitarkistus**-välilehdessä useita sanomia.</span><span class="sxs-lookup"><span data-stu-id="99aed-145">You can enter more than one message on the **MessageValidation** tab in the Excel parameter file.</span></span> <span data-ttu-id="99aed-146">Sanomat voivat myös olla virhe- tai varoitussanomia ilmoitussanomien sijaan.</span><span class="sxs-lookup"><span data-stu-id="99aed-146">The messages also can be error or warning messages instead of informational messages.</span></span>

### <a name="snapshot"></a><span data-ttu-id="99aed-147">Tilannevedos</span><span class="sxs-lookup"><span data-stu-id="99aed-147">Snapshot</span></span>

<span data-ttu-id="99aed-148">Tämä toiminto ottaa näyttökuvat tehtävätallenteen aikana suoritetuista vaiheista.</span><span class="sxs-lookup"><span data-stu-id="99aed-148">This feature takes screenshots of the steps that were performed during task recording.</span></span> <span data-ttu-id="99aed-149">Se on hyödyllinen tarkistus- tai virheenkorjaustarkoituksiin.</span><span class="sxs-lookup"><span data-stu-id="99aed-149">It is useful for auditing or debugging purposes.</span></span>

- <span data-ttu-id="99aed-150">Avaa tällä toiminnolla **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config**-tiedosto RSAT-asennuskansiossa (esimerkiksi kansiossa **C:\\Program Files (x86)\\Regression Suite Automation Tool**) ja muuta seuraavan elementin arvo **epätosi** arvoksi **tosi**.</span><span class="sxs-lookup"><span data-stu-id="99aed-150">To use this feature, open the **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** file under the RSAT installation folder (for example, **C:\\Program Files (x86)\\Regression Suite Automation Tool**), and change the value of the following element from **false** to **true**.</span></span>

    ```xml
    <add key="VerboseSnapshotsEnabled" value="false" />
    ```

<span data-ttu-id="99aed-151">Kun ajat testitapauksen, RSAT luo tilannevedoksia (kuvia) vaiheista, jotka näytetään työskentelyhakemistossa olevien testitapausten toistokansiossa.</span><span class="sxs-lookup"><span data-stu-id="99aed-151">When your run the test case, RSAT will generate snapshots (images) of the steps in the playback folder of the test cases in the working diretory.</span></span> <span data-ttu-id="99aed-152">Jos käytät vanhaa RSAT-versiota, kuvat tallennetaan kohteeseen **C:\\Käyttäjät\\\<Username\>\\AppData\\verkkovierailu\\regressionTool\\toisto**, erillinen kansio luodaan kullekin testitapaukselle, joka suoritetaan.</span><span class="sxs-lookup"><span data-stu-id="99aed-152">If you are using an older version of RSAT, the images are saved to **C:\\Users\\\<Username\>\\AppData\\Roaming\\regressionTool\\playback**, a separate folder is created for each test case that is run.</span></span>

## <a name="assignment"></a><span data-ttu-id="99aed-153">Toimeksianto</span><span class="sxs-lookup"><span data-stu-id="99aed-153">Assignment</span></span>

### <a name="scenario"></a><span data-ttu-id="99aed-154">Skenaario</span><span class="sxs-lookup"><span data-stu-id="99aed-154">Scenario</span></span>

1. <span data-ttu-id="99aed-155">Tuote suunnittelija luo uuden julkaistun tuotteen.</span><span class="sxs-lookup"><span data-stu-id="99aed-155">The product designer creates a new released product.</span></span>
2. <span data-ttu-id="99aed-156">Tuotantopäällikkö käynnistää tuotantotilauksen, joka nostaa varastotason kahteen kappaleeseen.</span><span class="sxs-lookup"><span data-stu-id="99aed-156">The production manager initiates a production order to bring the stock level to two pieces.</span></span>
3. <span data-ttu-id="99aed-157">Valmistus alkaa ja päättää tuotantotilauksen sekä varmistaa, että varastosaldo on kaksi kappaletta.</span><span class="sxs-lookup"><span data-stu-id="99aed-157">Manufacturing starts and ends the production order, and verifies that the on-hand quantity is two pieces.</span></span>
4. <span data-ttu-id="99aed-158">Myyntiryhmä vastaanottaa tilauksen, jossa on neljä kappaletta uutta tuotetta.</span><span class="sxs-lookup"><span data-stu-id="99aed-158">The sales team receives an order for four pieces of the new product.</span></span> <span data-ttu-id="99aed-159">Tämän vuoksi myyntiryhmä päivittää nettotarpeen dynaamisen suunnitelman kautta.</span><span class="sxs-lookup"><span data-stu-id="99aed-159">Therefore, the sales team updates the net requirements via the dynamic plan.</span></span> <span data-ttu-id="99aed-160">Koska lisäkapasiteettia ei ole käytettävissä, tilausten oletuskäytännöksi on määritetty ostaminen valmistamisen sijaan.</span><span class="sxs-lookup"><span data-stu-id="99aed-160">Because no additional capacity is available, the default order policy is set to "buy instead of make."</span></span> <span data-ttu-id="99aed-161">Tämän vuoksi luodaan suunnitellun ostotilauksen.</span><span class="sxs-lookup"><span data-stu-id="99aed-161">Therefore, a planned purchase order is created.</span></span>
5. <span data-ttu-id="99aed-162">Ostaja lisää toimittajan, vahvistaa suunnitellun ostotilauksen ja vahvistaa lopuksi ostotilauksen.</span><span class="sxs-lookup"><span data-stu-id="99aed-162">The buyer adds a vendor, firms the planned purchase order, and then confirms the purchase order.</span></span>
6. <span data-ttu-id="99aed-163">Kun ostetut tavarat saapuvat myymälään, myymäläkäyttäjä hakee liittyvän ostotilauksen ja vastaanottaa tavarat.</span><span class="sxs-lookup"><span data-stu-id="99aed-163">When the goods that were purchased arrive at the store, the store operator searches the related purchase order and receives the goods.</span></span> <span data-ttu-id="99aed-164">Koska tilaus on nyt valmis, tavarat voidaan kerätä ja pakata myyntitilauksen mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="99aed-164">Because the order is now completed, goods can be picked and packed against the sales order.</span></span>
7. <span data-ttu-id="99aed-165">Talousosasta kirjaa osto- ja myyntilaskun.</span><span class="sxs-lookup"><span data-stu-id="99aed-165">Finance posts the purchase invoice and sales invoice.</span></span>

<span data-ttu-id="99aed-166">Seuraavassa kuvassa on tämän skenaarion työnkulku.</span><span class="sxs-lookup"><span data-stu-id="99aed-166">The following illustration shows the flow for this scenario.</span></span>

![Demoskenaarion työnkulku](./media/use_rsa_tool_14.png)

<span data-ttu-id="99aed-168">Seuraavassa kuvassa näkyy tämän skenaarion liiketoimintaprosessien hierarkia LCS-liiketoimintaprosessin mallintajassa.</span><span class="sxs-lookup"><span data-stu-id="99aed-168">The following illustration shows the business processes hierarchy for this scenario in the LCS Business Process Modeler.</span></span>

![Demoskenaarion liiketoimintaprosessit](./media/use_rsa_tool_15.png)

## <a name="strategy--key-learning"></a><span data-ttu-id="99aed-170">Strategia – keskeinen opittava asia</span><span class="sxs-lookup"><span data-stu-id="99aed-170">Strategy – Key learning</span></span>

### <a name="data"></a><span data-ttu-id="99aed-171">Tiedot</span><span class="sxs-lookup"><span data-stu-id="99aed-171">Data</span></span>

- <span data-ttu-id="99aed-172">Varmista, että sinulla on tarvittavat tiedot (tuotanto-/ihannekonfiguraatiotietojen kopio ja siirretyt tiedot).</span><span class="sxs-lookup"><span data-stu-id="99aed-172">Make sure that you have representative data volumes (a copy of production/golden configuration data plus migrated data).</span></span>
- <span data-ttu-id="99aed-173">Jos luot uusia tietoja tehtävän tallennustoiminnon kautta, luo sellaiset testinimet, jotka eivät ole ristiriidassa aiemmin luotujen nimien kanssa. (Käytä esimerkiksi etuliitettä, kuten **RSATxxx**).</span><span class="sxs-lookup"><span data-stu-id="99aed-173">When you generate new data via Task recorder, create test names that won't conflict with existing names (for example, use a prefix such as **RSATxxx**).</span></span>
- <span data-ttu-id="99aed-174">Suorita testit uudelleen muissa kuin tason 1 ympäristöissä käyttämällä Azuren ajankohtaan perustuvaa palautusta.</span><span class="sxs-lookup"><span data-stu-id="99aed-174">Use Azure Point-In-Time restore to rerun tests in non-Tier 1 environments.</span></span>
- <span data-ttu-id="99aed-175">Vaikka voit muodostaa ainutlaatuisia yhdistelmiä Excelin **SATUNNAINEN**- ja **NYT**-funktioita, sen työmäärä on huomattavan suuri.</span><span class="sxs-lookup"><span data-stu-id="99aed-175">Although you can use the **RANDOM** and **NOW** Excel functions to generate a unique combination, the effort is considerably high.</span></span> <span data-ttu-id="99aed-176">Esimerkki:</span><span class="sxs-lookup"><span data-stu-id="99aed-176">Here is an example.</span></span>

    ```Excel
    product = "AT" &TEXT(NOW(),"yyymmddhhmm")
    ```

### <a name="task-recorder"></a><span data-ttu-id="99aed-177">Tehtävän tallennus</span><span class="sxs-lookup"><span data-stu-id="99aed-177">Task recorder</span></span>

- <span data-ttu-id="99aed-178">Määritä skenaariot ennen tallentamisen aloittamista.</span><span class="sxs-lookup"><span data-stu-id="99aed-178">Define scenarios before you start recording.</span></span> <span data-ttu-id="99aed-179">Hyvin hallitussa projektissa on ennalta määritetyt testiskenaariot.</span><span class="sxs-lookup"><span data-stu-id="99aed-179">A well-managed project has predefined test scenarios.</span></span> <span data-ttu-id="99aed-180">Kun muodostat testitapausta, mieti, kuinka ennakoitavia kyseisten testiskenaarioiden tulos on.</span><span class="sxs-lookup"><span data-stu-id="99aed-180">To build a test case, consider how predictable the outcome of those test scenarios is.</span></span>
- <span data-ttu-id="99aed-181">Jaa tallenteet, jos suorittajalla on eri rooli tai jos ennen seuraavaa vaihetta on odotettava tietty aika tai tiettyä ulkoista tapahtumaa.</span><span class="sxs-lookup"><span data-stu-id="99aed-181">Split recordings if they are performed by different roles, or if there is waiting time or an external event before the next step.</span></span>
- <span data-ttu-id="99aed-182">Vältä luettelossa olevien arvojen valitsemista.</span><span class="sxs-lookup"><span data-stu-id="99aed-182">Avoid selecting values in lists.</span></span> <span data-ttu-id="99aed-183">Käytä sen sijaan tekstimuotoja, kuten **FIFO**, **AudioRM** ja **SiteWH**.</span><span class="sxs-lookup"><span data-stu-id="99aed-183">Instead, use text formats, such as **FIFO**, **AudioRM**, and **SiteWH**.</span></span> <span data-ttu-id="99aed-184">Jos valinta tehdään luettelossa, arvon sijainti luettelossa tallennetaan eikä itse arvoa.</span><span class="sxs-lookup"><span data-stu-id="99aed-184">When you select in a list, the position of the value in the list is recorded, not the value itself.</span></span> <span data-ttu-id="99aed-185">Jos kyseiseen luetteloon lisätään nimikkeitä, arvon sijainti voi muuttua.</span><span class="sxs-lookup"><span data-stu-id="99aed-185">If items are added to that list, the position of the value can change.</span></span> <span data-ttu-id="99aed-186">Tämän vuoksi tallenne käyttää eri parametria, mikä voi vaikuttaa skenaarion muihin osiin.</span><span class="sxs-lookup"><span data-stu-id="99aed-186">Therefore, your recording will use a different parameter, and the rest of the scenario might be affected.</span></span>
- <span data-ttu-id="99aed-187">Mieti tilannetta, jossa käyttäjiä on useita.</span><span class="sxs-lookup"><span data-stu-id="99aed-187">Think about multi-user behavior.</span></span> <span data-ttu-id="99aed-188">Älä esimerkiksi oleta, että juuri luotu myyntitilaus valitaan aina automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="99aed-188">For example, don't assume that your newly created sales order will always be automatically selected.</span></span> <span data-ttu-id="99aed-189">Etsi sen sijaan oikea tilaus aina suodattimella.</span><span class="sxs-lookup"><span data-stu-id="99aed-189">Instead, always use the filter to find the correct order.</span></span>
- <span data-ttu-id="99aed-190">Tallenna juuri luodun tuotteen nimi tehtävän tallennustoiminnon kopiointitoiminnolla, jolloin sitä voidaan käyttää ketjutetuissa testitapauksissa.</span><span class="sxs-lookup"><span data-stu-id="99aed-190">Use the Copy function in Task recorder to save the name of a newly created product so it can be used in chained test cases.</span></span>
- <span data-ttu-id="99aed-191">Määritä tehtävän tallennustoiminnon tarkistustoiminnolla tarkistuspisteet tarkistamaan, että vaiheet on suoritettu oikein.</span><span class="sxs-lookup"><span data-stu-id="99aed-191">Use the Validate function in Task recorder to set checkpoints that verify that steps have been run correctly.</span></span>

### <a name="rsat"></a><span data-ttu-id="99aed-192">RSAT</span><span class="sxs-lookup"><span data-stu-id="99aed-192">RSAT</span></span>

- <span data-ttu-id="99aed-193">Jos suorittaa testin toisessa yrityksessä, voit vaihtaa yrityksen Excelin parametritiedoston **Yleiset**-välilehdessä.</span><span class="sxs-lookup"><span data-stu-id="99aed-193">To run the test in another company, you can change the company on the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="99aed-194">Varmista, että asetuksia ja tietoja voi käyttää juuri valitussa yrityksessä.</span><span class="sxs-lookup"><span data-stu-id="99aed-194">Make sure that settings and data are available in the newly selected company.</span></span>
- <span data-ttu-id="99aed-195">Voit vaihtaa testikäyttäjän Excelin parametritiedoston **Yleiset**-välilehdessä.</span><span class="sxs-lookup"><span data-stu-id="99aed-195">You can change the test user on the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="99aed-196">Määritä testitapauksen suorittavan käyttäjän sähköpostitunnus.</span><span class="sxs-lookup"><span data-stu-id="99aed-196">Specify the email ID of the user who will run the test case.</span></span> <span data-ttu-id="99aed-197">Tällä tavoin testitapaus voidaan suorittaa turvallisesti käyttämällä määritetyn käyttäjän suojausoikeuksia.</span><span class="sxs-lookup"><span data-stu-id="99aed-197">In this way, the test case can be run by using the security permissions of the specified user.</span></span>
- <span data-ttu-id="99aed-198">Jos haluat odottaa ennen testin aloittamista, voit määrittää tauon Excelin parametritiedoston **Yleiset**-välilehdessä.</span><span class="sxs-lookup"><span data-stu-id="99aed-198">To wait before the test is started, you can define a pause on the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="99aed-199">Tätä taukoa voidaan käyttää erätyössä (jos esimerkiksi työnkulku on suoritettava, ennen kuin seuraava vaihe voidaan suorittaa).</span><span class="sxs-lookup"><span data-stu-id="99aed-199">This pause can be used in a batch job (for example, if a workflow must be run before the next step can be performed.)</span></span>

## <a name="advanced-scripting"></a><span data-ttu-id="99aed-200">Edistyneet komentosarjat</span><span class="sxs-lookup"><span data-stu-id="99aed-200">Advanced scripting</span></span>

### <a name="cli"></a><span data-ttu-id="99aed-201">CLI</span><span class="sxs-lookup"><span data-stu-id="99aed-201">CLI</span></span>

<span data-ttu-id="99aed-202">RSAT voidaan kutsua **Komentokehote**- tai **PowerShell**-ikkunasta.</span><span class="sxs-lookup"><span data-stu-id="99aed-202">RSAT can be called from a **Command Prompt** or **PowerShell** window.</span></span>

> [!NOTE]
> <span data-ttu-id="99aed-203">Tarkista, että **TestRoot**-ympäristömuuttujan asetukseksi on määritetty RSAT-asennuspolku.</span><span class="sxs-lookup"><span data-stu-id="99aed-203">Verify that the **TestRoot** environment variable is set to the RSAT installation path.</span></span> <span data-ttu-id="99aed-204">(Avaa Microsoft Windowsissa **Ohjauspaneeli**, valitse sitten **Järjestelmä ja suojaus \> Järjestelmä \> Järjestelmän lisäasetukset** ja valitse lopuksi **Ympäristömuuttujat**.)</span><span class="sxs-lookup"><span data-stu-id="99aed-204">(In Microsoft Windows, open **Control Panel**, select **System and Security \> System \> Advanced system settings**, and then select **Environment Variables**.)</span></span>

1. <span data-ttu-id="99aed-205">Avaa **Komentokehote**- tai **PowerShell**-ikkuna järjestelmänvalvojana.</span><span class="sxs-lookup"><span data-stu-id="99aed-205">Open a **Command Prompt** or **PowerShell** window as an admin.</span></span>
2. <span data-ttu-id="99aed-206">Siirry RSAT-asennushakemistoon.</span><span class="sxs-lookup"><span data-stu-id="99aed-206">Navigate to the RSAT installation directory.</span></span>

    ```Console
    cd "c:\Program Files (x86)\Regression Suite Automation Tool\"
    ```

3. <span data-ttu-id="99aed-207">Luettele kaikki komennot.</span><span class="sxs-lookup"><span data-stu-id="99aed-207">List all commands.</span></span>

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

#### <a name=""></a><span data-ttu-id="99aed-208">?</span><span class="sxs-lookup"><span data-stu-id="99aed-208">?</span></span> 
<span data-ttu-id="99aed-209">Näyttää kaikkien käytettävissä olevien komentojen ja niiden parametrien ohjeen.</span><span class="sxs-lookup"><span data-stu-id="99aed-209">Shows help about all available commands and their parameters.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``?``**``[command]``

##### <a name="optional-parameters"></a><span data-ttu-id="99aed-210">Valinnaiset parametrit</span><span class="sxs-lookup"><span data-stu-id="99aed-210">Optional parameters</span></span>

**``command``**


<span data-ttu-id="99aed-211">Jossa ``[command]`` on yksi alla määritetyistä komennoista.</span><span class="sxs-lookup"><span data-stu-id="99aed-211">Where ``[command]`` is one of the commands specified below.</span></span>


#### <a name="about"></a><span data-ttu-id="99aed-212">tietoja</span><span class="sxs-lookup"><span data-stu-id="99aed-212">about</span></span>
<span data-ttu-id="99aed-213">Näyttää nykyisen version.</span><span class="sxs-lookup"><span data-stu-id="99aed-213">Displays the current version.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``about``**

#### <a name="cls"></a><span data-ttu-id="99aed-214">cls</span><span class="sxs-lookup"><span data-stu-id="99aed-214">cls</span></span>
<span data-ttu-id="99aed-215">Tyhjentää näytön.</span><span class="sxs-lookup"><span data-stu-id="99aed-215">Clears the screen.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``cls``**


#### <a name="download"></a><span data-ttu-id="99aed-216">lataa</span><span class="sxs-lookup"><span data-stu-id="99aed-216">download</span></span>
<span data-ttu-id="99aed-217">Lataa määritetyn testitapauksen liitteet tulostushakemistoon.</span><span class="sxs-lookup"><span data-stu-id="99aed-217">Downloads attachments for the specified test case to the output directory.</span></span> <span data-ttu-id="99aed-218">Voit käyttää ``list``-komentoa kaikkien käytettävissä olevien testitapausten hakemisessa.</span><span class="sxs-lookup"><span data-stu-id="99aed-218">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="99aed-219">Käytä mitä tahansa ensimmäisen sarakkeen arvoa **test_case_id**-parametrina.</span><span class="sxs-lookup"><span data-stu-id="99aed-219">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``download``**``[test_case_id] [output_dir]``

##### <a name="required-parameters"></a><span data-ttu-id="99aed-220">Pakolliset parametrit</span><span class="sxs-lookup"><span data-stu-id="99aed-220">Required parameters</span></span>
<span data-ttu-id="99aed-221">**``test_case_id``** - edustaa testitapauksen tunnusta.</span><span class="sxs-lookup"><span data-stu-id="99aed-221">**``test_case_id``** Represents the test case ID.</span></span>  
<span data-ttu-id="99aed-222">**``output_dir``** - edustaa tulostushakemistoa.</span><span class="sxs-lookup"><span data-stu-id="99aed-222">**``output_dir``** Represents the output directory.</span></span> <span data-ttu-id="99aed-223">Hakemisto on määritettävä.</span><span class="sxs-lookup"><span data-stu-id="99aed-223">The directory must exist.</span></span>

##### <a name="examples"></a><span data-ttu-id="99aed-224">Esimerkkejä</span><span class="sxs-lookup"><span data-stu-id="99aed-224">Examples</span></span>

``download 123 c:\temp\rsat``   
``download 765 c:\rsat\last``


#### <a name="edit"></a><span data-ttu-id="99aed-225">muokkaa</span><span class="sxs-lookup"><span data-stu-id="99aed-225">edit</span></span>
<span data-ttu-id="99aed-226">Voit avata parametritiedoston Excel-ohjelmassa ja muokata sitä.</span><span class="sxs-lookup"><span data-stu-id="99aed-226">Allows you to open parameters file in Excel program and edit it.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``edit``**``[excel_file]``

##### <a name="required-parameters"></a><span data-ttu-id="99aed-227">Pakolliset parametrit</span><span class="sxs-lookup"><span data-stu-id="99aed-227">Required parameters</span></span>
<span data-ttu-id="99aed-228">**``excel_file``** - olemassa olevan Excel-tiedoston täydellinen polku on oltava.</span><span class="sxs-lookup"><span data-stu-id="99aed-228">**``excel_file``** Must contain a full path to an existing Excel file.</span></span>

##### <a name="examples"></a><span data-ttu-id="99aed-229">Esimerkkejä</span><span class="sxs-lookup"><span data-stu-id="99aed-229">Examples</span></span>
``edit c:\RSAT\TestCase_123_Base.xlsx``  
``edit e:\temp\TestCase_456_Base.xlsx``


#### <a name="generate"></a><span data-ttu-id="99aed-230">luo</span><span class="sxs-lookup"><span data-stu-id="99aed-230">generate</span></span>
<span data-ttu-id="99aed-231">Luo testisuorituksen ja parametritiedostot määritetylle testitapaukselle tulostushakemistossa.</span><span class="sxs-lookup"><span data-stu-id="99aed-231">Generates test execution and parameter files for the specified test case in the output directory.</span></span>
<span data-ttu-id="99aed-232">Voit käyttää ``list``-komentoa kaikkien käytettävissä olevien testitapausten hakemisessa.</span><span class="sxs-lookup"><span data-stu-id="99aed-232">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="99aed-233">Käytä mitä tahansa ensimmäisen sarakkeen arvoa **test_case_id**-parametrina.</span><span class="sxs-lookup"><span data-stu-id="99aed-233">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generate``**``[test_case_id] [output_dir]``

##### <a name="required-parameters"></a><span data-ttu-id="99aed-234">Pakolliset parametrit</span><span class="sxs-lookup"><span data-stu-id="99aed-234">Required parameters</span></span>
<span data-ttu-id="99aed-235">**``test_case_id``** - edustaa testitapauksen tunnusta.</span><span class="sxs-lookup"><span data-stu-id="99aed-235">**``test_case_id``** Represents the test case ID.</span></span>  
<span data-ttu-id="99aed-236">**``output_dir``** - edustaa tulostushakemistoa.</span><span class="sxs-lookup"><span data-stu-id="99aed-236">**``output_dir``** Represents the output directory.</span></span> <span data-ttu-id="99aed-237">Hakemisto on määritettävä.</span><span class="sxs-lookup"><span data-stu-id="99aed-237">The directory must exist.</span></span>

##### <a name="examples"></a><span data-ttu-id="99aed-238">Esimerkkejä</span><span class="sxs-lookup"><span data-stu-id="99aed-238">Examples</span></span>
``generate 123 c:\temp\rsat``  
``generate 765 c:\rsat\last``


#### <a name="generatederived"></a><span data-ttu-id="99aed-239">generatederived</span><span class="sxs-lookup"><span data-stu-id="99aed-239">generatederived</span></span>
<span data-ttu-id="99aed-240">Luo uuden testitapauksen, joka johdetaan annetusta testitapauksesta.</span><span class="sxs-lookup"><span data-stu-id="99aed-240">Generates a new test case, derived from the provided test case.</span></span> <span data-ttu-id="99aed-241">Voit käyttää ``list``-komentoa kaikkien käytettävissä olevien testitapausten hakemisessa.</span><span class="sxs-lookup"><span data-stu-id="99aed-241">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="99aed-242">Käytä mitä tahansa ensimmäisen sarakkeen arvoa **test_case_id**-parametrina.</span><span class="sxs-lookup"><span data-stu-id="99aed-242">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatederived``**``[parent_test_case_id] [test_plan_id] [test_suite_id]``

##### <a name="required-parameters"></a><span data-ttu-id="99aed-243">Pakolliset parametrit</span><span class="sxs-lookup"><span data-stu-id="99aed-243">Required parameters</span></span>
<span data-ttu-id="99aed-244">**``parent_test_case_id``** - edustaa päätestitapauksen tunnusta.</span><span class="sxs-lookup"><span data-stu-id="99aed-244">**``parent_test_case_id``** Represents the parent test case ID.</span></span>  
<span data-ttu-id="99aed-245">**``test_plan_id``** - edustaa testisuunnitelman tunnusta.</span><span class="sxs-lookup"><span data-stu-id="99aed-245">**``test_plan_id``** Represents the test plan ID.</span></span>  
<span data-ttu-id="99aed-246">**``test_suite_id``** - edustaa testiohjelmistopaketin tunnusta.</span><span class="sxs-lookup"><span data-stu-id="99aed-246">**``test_suite_id``** Represents the test suite ID.</span></span>

##### <a name="examples"></a><span data-ttu-id="99aed-247">Esimerkkejä</span><span class="sxs-lookup"><span data-stu-id="99aed-247">Examples</span></span>
``generatederived 123 8901 678``


#### <a name="generatetestonly"></a><span data-ttu-id="99aed-248">generatetestonly</span><span class="sxs-lookup"><span data-stu-id="99aed-248">generatetestonly</span></span>
<span data-ttu-id="99aed-249">Luo vain testisuoritustiedoston määritetylle testitapaukselle tulostushakemistossa.</span><span class="sxs-lookup"><span data-stu-id="99aed-249">Generates only test execution file for the specified test case in the output directory.</span></span> <span data-ttu-id="99aed-250">Voit käyttää ``list``-komentoa kaikkien käytettävissä olevien testitapausten hakemisessa.</span><span class="sxs-lookup"><span data-stu-id="99aed-250">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="99aed-251">Käytä mitä tahansa ensimmäisen sarakkeen arvoa **test_case_id**-parametrina.</span><span class="sxs-lookup"><span data-stu-id="99aed-251">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatetestonly``**``[test_case_id] [output_dir]``

##### <a name="required-parameters"></a><span data-ttu-id="99aed-252">Pakolliset parametrit</span><span class="sxs-lookup"><span data-stu-id="99aed-252">Required parameters</span></span>
<span data-ttu-id="99aed-253">**``test_case_id``** - edustaa testitapauksen tunnusta.</span><span class="sxs-lookup"><span data-stu-id="99aed-253">**``test_case_id``** Represents the test case ID.</span></span>  
<span data-ttu-id="99aed-254">**``output_dir``** - edustaa tulostushakemistoa.</span><span class="sxs-lookup"><span data-stu-id="99aed-254">**``output_dir``** Represents the output directory.</span></span> <span data-ttu-id="99aed-255">Hakemisto on määritettävä.</span><span class="sxs-lookup"><span data-stu-id="99aed-255">The directory must exist.</span></span>

##### <a name="examples"></a><span data-ttu-id="99aed-256">Esimerkkejä</span><span class="sxs-lookup"><span data-stu-id="99aed-256">Examples</span></span>
``generatetestonly 123 c:\temp\rsat``  
``generatetestonly 765 c:\rsat\last``


#### <a name="generatetestsuite"></a><span data-ttu-id="99aed-257">generatetestsuite</span><span class="sxs-lookup"><span data-stu-id="99aed-257">generatetestsuite</span></span>
<span data-ttu-id="99aed-258">Luo määritetyn ohjelmistopaketin kaikki testitapaukset tulostushakemistoon.</span><span class="sxs-lookup"><span data-stu-id="99aed-258">Generates all test cases for the specified suite in the output directory.</span></span>
<span data-ttu-id="99aed-259">Voit käyttää ``listtestsuitenames``-komentoa kaikkien käytettävissä olevien testiohjelmistopakettien hakemisessa.</span><span class="sxs-lookup"><span data-stu-id="99aed-259">You can use ``listtestsuitenames`` command to get all available test suits.</span></span> <span data-ttu-id="99aed-260">Käytä mitä tahansa sarakkeen arvoa **test_suite_name**-parametrina.</span><span class="sxs-lookup"><span data-stu-id="99aed-260">Use any value from the column as a **test_suite_name** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatetestsuite``**``[test_suite_name] [output_dir]``

##### <a name="required-parameters"></a><span data-ttu-id="99aed-261">Pakolliset parametrit</span><span class="sxs-lookup"><span data-stu-id="99aed-261">Required parameters</span></span>
<span data-ttu-id="99aed-262">**``test_suite_name``** - edustaa testiohjelmistopaketin nimeä.</span><span class="sxs-lookup"><span data-stu-id="99aed-262">**``test_suite_name``** Represents the test suite name.</span></span>  
<span data-ttu-id="99aed-263">**``output_dir``** - edustaa tulostushakemistoa.</span><span class="sxs-lookup"><span data-stu-id="99aed-263">**``output_dir``** Represents the output directory.</span></span> <span data-ttu-id="99aed-264">Hakemisto on määritettävä.</span><span class="sxs-lookup"><span data-stu-id="99aed-264">The directory must exist.</span></span>

##### <a name="examples"></a><span data-ttu-id="99aed-265">Esimerkkejä</span><span class="sxs-lookup"><span data-stu-id="99aed-265">Examples</span></span>
``generatetestsuite Tests c:\temp\rsat``   
``generatetestsuite Purchase c:\rsat\last``


#### <a name="help"></a><span data-ttu-id="99aed-266">ohje</span><span class="sxs-lookup"><span data-stu-id="99aed-266">help</span></span>
<span data-ttu-id="99aed-267">Sama kuin [?](#section)</span><span class="sxs-lookup"><span data-stu-id="99aed-267">Identical to the [?](#section)</span></span> <span data-ttu-id="99aed-268">komento</span><span class="sxs-lookup"><span data-stu-id="99aed-268">command</span></span>


#### <a name="list"></a><span data-ttu-id="99aed-269">luettelo</span><span class="sxs-lookup"><span data-stu-id="99aed-269">list</span></span>
<span data-ttu-id="99aed-270">Luettelo kaikista käytettävissä olevista testitapauksista.</span><span class="sxs-lookup"><span data-stu-id="99aed-270">Lists all available test cases.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``list``**


#### <a name="listtestplans"></a><span data-ttu-id="99aed-271">listtestplans</span><span class="sxs-lookup"><span data-stu-id="99aed-271">listtestplans</span></span>
<span data-ttu-id="99aed-272">Luettelo kaikista käytettävissä olevista testisuunnitelmista.</span><span class="sxs-lookup"><span data-stu-id="99aed-272">Lists all available test plans.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestplans``**


#### <a name="listtestsuite"></a><span data-ttu-id="99aed-273">listtestsuite</span><span class="sxs-lookup"><span data-stu-id="99aed-273">listtestsuite</span></span>
<span data-ttu-id="99aed-274">Luettelo määritetyn testiohjelmistopaketin testitapauksista.</span><span class="sxs-lookup"><span data-stu-id="99aed-274">Lists test cases for the specified test suite.</span></span> <span data-ttu-id="99aed-275">Voit käyttää ``listtestsuitenames``-komentoa kaikkien käytettävissä olevien testiohjelmistopakettien hakemisessa.</span><span class="sxs-lookup"><span data-stu-id="99aed-275">You can use ``listtestsuitenames`` command to get all available test suites.</span></span> <span data-ttu-id="99aed-276">Käytä mitä tahansa ensimmäisen sarakkeen arvoa **suite_name**-parametrina.</span><span class="sxs-lookup"><span data-stu-id="99aed-276">Use any value from first column as **suite_name** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestsuite``**``[suite_name]``

##### <a name="required-parameters"></a><span data-ttu-id="99aed-277">Pakolliset parametrit</span><span class="sxs-lookup"><span data-stu-id="99aed-277">Required parameters</span></span>
<span data-ttu-id="99aed-278">**``suite_name``** - halutun ohjelmistopaketin nimi.</span><span class="sxs-lookup"><span data-stu-id="99aed-278">**``suite_name``** Name of the desired suite.</span></span>

##### <a name="examples"></a><span data-ttu-id="99aed-279">Esimerkkejä</span><span class="sxs-lookup"><span data-stu-id="99aed-279">Examples</span></span>
``listtestsuite "sample suite name"``  
``listtestsuite NameOfTheSuite``


#### <a name="listtestsuitenames"></a><span data-ttu-id="99aed-280">listtestsuitenames</span><span class="sxs-lookup"><span data-stu-id="99aed-280">listtestsuitenames</span></span>
<span data-ttu-id="99aed-281">Luettelo kaikista käytettävissä olevista testiohjelmistopaketeista.</span><span class="sxs-lookup"><span data-stu-id="99aed-281">Lists all available test suites.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestsuitenames``**


#### <a name="playback"></a><span data-ttu-id="99aed-282">toisto</span><span class="sxs-lookup"><span data-stu-id="99aed-282">playback</span></span>
<span data-ttu-id="99aed-283">Toistaa testitapauksen Excel-tiedoston avulla.</span><span class="sxs-lookup"><span data-stu-id="99aed-283">Plays back a test case using an Excel file.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playback``**``[excel_file]``

##### <a name="required-parameters"></a><span data-ttu-id="99aed-284">Pakolliset parametrit</span><span class="sxs-lookup"><span data-stu-id="99aed-284">Required parameters</span></span>
<span data-ttu-id="99aed-285">**``excel_file``** - Excel-tiedoston täydellinen polku.</span><span class="sxs-lookup"><span data-stu-id="99aed-285">**``excel_file``** A full path to the Excel file.</span></span> <span data-ttu-id="99aed-286">Tiedoston on oltava olemassa.</span><span class="sxs-lookup"><span data-stu-id="99aed-286">File must exist.</span></span> 

##### <a name="examples"></a><span data-ttu-id="99aed-287">Esimerkkejä</span><span class="sxs-lookup"><span data-stu-id="99aed-287">Examples</span></span>
``
playback c:\RSAT\TestCaseParameters\sample1.xlsx
playback e:\temp\test.xlsx
``


#### <a name="playbackbyid"></a><span data-ttu-id="99aed-288">playbackbyid</span><span class="sxs-lookup"><span data-stu-id="99aed-288">playbackbyid</span></span>
<span data-ttu-id="99aed-289">Toistaa useita testitapauksia kerralla.</span><span class="sxs-lookup"><span data-stu-id="99aed-289">Plays back multiple test cases at once.</span></span>
<span data-ttu-id="99aed-290">Voit käyttää ``list``-komentoa kaikkien käytettävissä olevien testitapausten hakemisessa.</span><span class="sxs-lookup"><span data-stu-id="99aed-290">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="99aed-291">Käytä mitä tahansa ensimmäisen sarakkeen arvoa **test_case_id**-parametrina.</span><span class="sxs-lookup"><span data-stu-id="99aed-291">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbackbyid``**``[test_case_id1] [test_case_id2] ... [test_case_idN]``

##### <a name="required-parameters"></a><span data-ttu-id="99aed-292">Pakolliset parametrit</span><span class="sxs-lookup"><span data-stu-id="99aed-292">Required parameters</span></span>
<span data-ttu-id="99aed-293">**``test_case_id1``** - olemassa olevan testitapauksen tunnus.</span><span class="sxs-lookup"><span data-stu-id="99aed-293">**``test_case_id1``** ID of exisiting test case.</span></span>  
<span data-ttu-id="99aed-294">**``test_case_id2``** - olemassa olevan testitapauksen tunnus.</span><span class="sxs-lookup"><span data-stu-id="99aed-294">**``test_case_id2``** ID of exisiting test case.</span></span>  
<span data-ttu-id="99aed-295">**``test_case_idN``** - olemassa olevan testitapauksen tunnus.</span><span class="sxs-lookup"><span data-stu-id="99aed-295">**``test_case_idN``** ID of exisiting test case.</span></span>  

##### <a name="examples"></a><span data-ttu-id="99aed-296">Esimerkkejä</span><span class="sxs-lookup"><span data-stu-id="99aed-296">Examples</span></span>
``playbackbyid 878``  
``playbackbyid 2345 667 135``


#### <a name="playbackmany"></a><span data-ttu-id="99aed-297">playbackmany</span><span class="sxs-lookup"><span data-stu-id="99aed-297">playbackmany</span></span>
<span data-ttu-id="99aed-298">Toistaa useita testitapauksia kerralla Excel-tiedostojen avulla.</span><span class="sxs-lookup"><span data-stu-id="99aed-298">Plays back many test cases at once, using Excel files.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbackmany``**``[excel_file1] [excel_file2] ... [excel_fileN]``

##### <a name="required-parameters"></a><span data-ttu-id="99aed-299">Pakolliset parametrit</span><span class="sxs-lookup"><span data-stu-id="99aed-299">Required parameters</span></span>
<span data-ttu-id="99aed-300">**``excel_file1``** - Excel-tiedoston täydellinen polku.</span><span class="sxs-lookup"><span data-stu-id="99aed-300">**``excel_file1``** Full path to the Excel file.</span></span> <span data-ttu-id="99aed-301">Tiedoston on oltava olemassa.</span><span class="sxs-lookup"><span data-stu-id="99aed-301">File must exist.</span></span>  
<span data-ttu-id="99aed-302">**``excel_file2``** - Excel-tiedoston täydellinen polku.</span><span class="sxs-lookup"><span data-stu-id="99aed-302">**``excel_file2``** Full path to the Excel file.</span></span> <span data-ttu-id="99aed-303">Tiedoston on oltava olemassa.</span><span class="sxs-lookup"><span data-stu-id="99aed-303">File must exist.</span></span>  
<span data-ttu-id="99aed-304">**``excel_fileN``** - Excel-tiedoston täydellinen polku.</span><span class="sxs-lookup"><span data-stu-id="99aed-304">**``excel_fileN``** Full path to the Excel file.</span></span> <span data-ttu-id="99aed-305">Tiedoston on oltava olemassa.</span><span class="sxs-lookup"><span data-stu-id="99aed-305">File must exist.</span></span>  

##### <a name="examples"></a><span data-ttu-id="99aed-306">Esimerkkejä</span><span class="sxs-lookup"><span data-stu-id="99aed-306">Examples</span></span>
``playbackmany c:\RSAT\TestCaseParameters\param1.xlsx``  
``playbackmany e:\temp\test.xlsx f:\rsat\sample1.xlsx c:\RSAT\sample2.xlsx``


#### <a name="playbacksuite"></a><span data-ttu-id="99aed-307">playbacksuite</span><span class="sxs-lookup"><span data-stu-id="99aed-307">playbacksuite</span></span>
<span data-ttu-id="99aed-308">Toistaa kaikki testitapaukset määritetystä testiohjelmistopaketista.</span><span class="sxs-lookup"><span data-stu-id="99aed-308">Plays back all test cases from the specified test suite.</span></span> <span data-ttu-id="99aed-309">Voit käyttää ``listtestsuitenames``-komentoa kaikkien käytettävissä olevien testiohjelmistopakettien hakemisessa.</span><span class="sxs-lookup"><span data-stu-id="99aed-309">You can use ``listtestsuitenames`` command to get all available test suites.</span></span> <span data-ttu-id="99aed-310">Käytä mitä tahansa ensimmäisen sarakkeen arvoa **suite_name**-parametrina.</span><span class="sxs-lookup"><span data-stu-id="99aed-310">Use any value from first column as **suite_name** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbacksuite``**``[suite_name]``

##### <a name="required-parameters"></a><span data-ttu-id="99aed-311">Pakolliset parametrit</span><span class="sxs-lookup"><span data-stu-id="99aed-311">Required parameters</span></span>
<span data-ttu-id="99aed-312">**``suite_name``** - halutun ohjelmistopaketin nimi.</span><span class="sxs-lookup"><span data-stu-id="99aed-312">**``suite_name``** Name of the desired suite.</span></span>

##### <a name="examples"></a><span data-ttu-id="99aed-313">Esimerkkejä</span><span class="sxs-lookup"><span data-stu-id="99aed-313">Examples</span></span>
``playbacksuite suiteName``  
``playbacksuite sample_suite``


#### <a name="quit"></a><span data-ttu-id="99aed-314">lopeta</span><span class="sxs-lookup"><span data-stu-id="99aed-314">quit</span></span>
<span data-ttu-id="99aed-315">Sulkee sovelluksen.</span><span class="sxs-lookup"><span data-stu-id="99aed-315">Closes the  application.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``quit``**


#### <a name="upload"></a><span data-ttu-id="99aed-316">lataa</span><span class="sxs-lookup"><span data-stu-id="99aed-316">upload</span></span>
<span data-ttu-id="99aed-317">Lataa kaikki määritettyyn testiohjelmistopakettiin tai määritettyihin testitapauksiin kuuluvat tiedostot.</span><span class="sxs-lookup"><span data-stu-id="99aed-317">Uploads all files belonging to the specified test suite or test cases.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``upload``**``[suite_name] [testcase_id]``

#### <a name="required-parameters"></a><span data-ttu-id="99aed-318">Pakolliset parametrit</span><span class="sxs-lookup"><span data-stu-id="99aed-318">Required parameters</span></span>
<span data-ttu-id="99aed-319">**``suite_name``** - kaikki tiettyyn testiohjelmistopakettiin kuuluvat tiedostot ladataan.</span><span class="sxs-lookup"><span data-stu-id="99aed-319">**``suite_name``** All files belonging to the specified test suite will be uploaded.</span></span>
<span data-ttu-id="99aed-320">**``testcase_id``** - kaikki tiettyihin testitapauksiin kuuluvat tiedostot ladataan.</span><span class="sxs-lookup"><span data-stu-id="99aed-320">**``testcase_id``** All files beloning to the specified test case(s) will be uploaded.</span></span>

##### <a name="examples"></a><span data-ttu-id="99aed-321">Esimerkkejä</span><span class="sxs-lookup"><span data-stu-id="99aed-321">Examples</span></span>
``upload sample_suite``  
``upload 123``  
``upload 123 456``


#### <a name="uploadrecording"></a><span data-ttu-id="99aed-322">uploadrecording</span><span class="sxs-lookup"><span data-stu-id="99aed-322">uploadrecording</span></span>
<span data-ttu-id="99aed-323">Lataa vain määritettyihin testitapauksiin kuuluvan tallennustiedoston.</span><span class="sxs-lookup"><span data-stu-id="99aed-323">Uploads only recording file belonging to the specified test cases.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``uploadrecording``**``[testcase_id]``

##### <a name="required-parameters"></a><span data-ttu-id="99aed-324">Pakolliset parametrit</span><span class="sxs-lookup"><span data-stu-id="99aed-324">Required parameters</span></span>
<span data-ttu-id="99aed-325">**``testcase_id``** - määritettyihin testitapauksiin kuuluva tallennustiedosto ladataan.</span><span class="sxs-lookup"><span data-stu-id="99aed-325">**``testcase_id``** Recording file belonging to the specified test cases will be uploaded.</span></span>

##### <a name="examples"></a><span data-ttu-id="99aed-326">Esimerkkejä</span><span class="sxs-lookup"><span data-stu-id="99aed-326">Examples</span></span>
``uploadrecording 123``  
``uploadrecording 123 456``


#### <a name="usage"></a><span data-ttu-id="99aed-327">käyttö</span><span class="sxs-lookup"><span data-stu-id="99aed-327">usage</span></span>
<span data-ttu-id="99aed-328">Näyttää kaksi tapaa, joilla tätä sovellusta voi kutsua: toisessa käytetään oletusasetustiedostoa ja toinen määrittää asetustiedoston.</span><span class="sxs-lookup"><span data-stu-id="99aed-328">Shows two ways to invoke this application: one using a default setting file, another one providing a setting file.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``usage``**


### <a name="windows-powershell-examples"></a><span data-ttu-id="99aed-329">Windows PowerShell -esimerkkejä</span><span class="sxs-lookup"><span data-stu-id="99aed-329">Windows PowerShell examples</span></span>

[!IMPORTANT] <span data-ttu-id="99aed-330">Alla olevat esimerkkikomentosarjat on tarkoitettu havainnollistamiseen, eikä Microsoft tue niitä.</span><span class="sxs-lookup"><span data-stu-id="99aed-330">The example scripts below are provided AS IS for illustration purposes and are not supported by Microsoft.</span></span>

#### <a name="run-a-test-case-in-a-loop"></a><span data-ttu-id="99aed-331">Testitapauksen suorittaminen silmukkana</span><span class="sxs-lookup"><span data-stu-id="99aed-331">Run a test case in a loop</span></span>

<span data-ttu-id="99aed-332">Sinulla on uuden asiakkaan luova testikomentosarja.</span><span class="sxs-lookup"><span data-stu-id="99aed-332">You have a test script that creates a new customer.</span></span> <span data-ttu-id="99aed-333">Tämä testisarja voidaan suorittaa komentosarjojen avulla silmukkana muodostamalla seuraavat tiedot satunnaisesti ennen kunkin iteraation suorittamista:</span><span class="sxs-lookup"><span data-stu-id="99aed-333">Via scripting, this test case can be run in a loop by randomizing the following data before each iteration is run:</span></span>

- <span data-ttu-id="99aed-334">Asiakastunnus</span><span class="sxs-lookup"><span data-stu-id="99aed-334">Customer ID</span></span>
- <span data-ttu-id="99aed-335">Asiakkaan nimi</span><span class="sxs-lookup"><span data-stu-id="99aed-335">Customer name</span></span>
- <span data-ttu-id="99aed-336">Asiakkaan osoite</span><span class="sxs-lookup"><span data-stu-id="99aed-336">Customer address</span></span>

<span data-ttu-id="99aed-337">Asiakastunnuksen muoto on seuraavanlainen: *ATCUS\<number\>*, jossa \<number\> on arvo on luku **000000001** ja **999999999** väliltä.</span><span class="sxs-lookup"><span data-stu-id="99aed-337">The customer ID will be in the format *ATCUS\<number\>*, where \<number\> is a value between **000000001** and **999999999**.</span></span>

<span data-ttu-id="99aed-338">Seuraavassa esimerkissä käytetään yhtä **aloitus**-parametria määrittämään ensimmäinen käytettävä numero.</span><span class="sxs-lookup"><span data-stu-id="99aed-338">The following example uses one parameter, **start**, to define the first number that is used.</span></span> <span data-ttu-id="99aed-339">Is käyttää seuraavaa parametria **nr** määrittämään luotavien asiakkaiden määrän.</span><span class="sxs-lookup"><span data-stu-id="99aed-339">Is uses a second parameter, **nr**, to define the number of customers that must be created.</span></span> <span data-ttu-id="99aed-340">Excelin parametritiedoston parametrit muutetaan kussakin iteraatiossa käyttämällä UpdateCustomer-funktiota.</span><span class="sxs-lookup"><span data-stu-id="99aed-340">For each iteration, the parameters in the Excel parameter file are changed by using an UpdateCustomer function.</span></span> <span data-ttu-id="99aed-341">RSAT-komentorivi kutsutaan sitten RunTestCase-funktiolla.</span><span class="sxs-lookup"><span data-stu-id="99aed-341">Then the RSAT command line is called in a RunTestCase function.</span></span>

<span data-ttu-id="99aed-342">Avaa integroitu Microsoft Windows PowerShell -komentosarjaympäristö (ISE) järjestelmänvalvojan tilassa ja liitä seuraava koodi **Untitled1.ps1**-nimiseen ikkunaan.</span><span class="sxs-lookup"><span data-stu-id="99aed-342">Open Microsoft Windows PowerShell Integrated Scripting Environment (ISE) in admin mode, and paste the following code into the window that is named **Untitled1.ps1**.</span></span>

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

#### <a name="run-a-script-that-depends-on-data-in-microsoft-dynamics-365"></a><span data-ttu-id="99aed-343">Microsoft Dynamics 365:n tiedoista riippuvaisen komentosarjan suorittaminen</span><span class="sxs-lookup"><span data-stu-id="99aed-343">Run a script that depends on data in Microsoft Dynamics 365</span></span>

<span data-ttu-id="99aed-344">Seuraavassa esimerkissä ostotilauksen tila etsitään Open Data Protocol (OData) -kutsun avulla.</span><span class="sxs-lookup"><span data-stu-id="99aed-344">The following example uses an Open Data Protocol (OData) call to find the order status of a purchase order.</span></span> <span data-ttu-id="99aed-345">Jos tila ei ole **invoiced**, voit esimerkiksi kutsua laskun kirjaavan RSAT-testitapauksen.</span><span class="sxs-lookup"><span data-stu-id="99aed-345">If the status isn't **invoiced**, you can, for example, call an RSAT test case that posts the invoice.</span></span>

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
