---
title: Luotujen ER-raporttien tulosten seuraamisen ja perusarvoihin vertaamisen parannukset
description: Tässä ohjeaiheessa on tietoja Microsoft Dynamics 365 for Finance and Operationsin versiossa 10.0.3 (kesäkuu 2019) ER-perusviivatoiminnon parannuksista.
author: NickSelin
manager: AnnBe
ms.date: 06/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.openlocfilehash: 222a415f686c8028fc2a414f97eed0291d850ae7
ms.sourcegitcommit: 9917df8c0c9320955c61186cd922c8df894a4f25
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/21/2019
ms.locfileid: "1700679"
---
# <a name="improvements-in-tracing-the-results-of-generated-er-reports-and-comparing-them-with-baseline-values"></a><span data-ttu-id="7d84c-103">Luotujen ER-raporttien tulosten seuraamisen ja perusarvoihin vertaamisen parannukset</span><span class="sxs-lookup"><span data-stu-id="7d84c-103">Improvements in tracing the results of generated ER reports and comparing them with baseline values</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="7d84c-104">Tässä ohjeaiheessa käsitellään ensimmäisiä sähköisen raportoinnin (ER) kehyksen perusviivatoimintoon parannuksia.</span><span class="sxs-lookup"><span data-stu-id="7d84c-104">This topic describes the first set of improvements that have been made to the baseline feature of the Electronic reporting (ER) framework.</span></span> <span data-ttu-id="7d84c-105">Nämä parannukset ovat käytettävissä Microsoft Dynamics 365 for Finance and Operationsin versiossa 10.0.3 (kesäkuu 2019) tai uudemmassa.</span><span class="sxs-lookup"><span data-stu-id="7d84c-105">These improvements are available in Microsoft Dynamics 365 for Finance and Operations version 10.0.3 (June 2019) and later.</span></span>

## <a name="automate-the-setting-of-baseline-rules"></a><span data-ttu-id="7d84c-106">Perusviivasääntöasetusten automatisointi</span><span class="sxs-lookup"><span data-stu-id="7d84c-106">Automate the setting of baseline rules</span></span>

<span data-ttu-id="7d84c-107">Ohjeaiheessa [Luotuja raporttitulosten seuraaminen ja vertaaminen perusarvoihin](er-trace-reports-compare-baseline.md) käsitellään ER-kehys määrittämistä keräämään tietoja ER-muodon suorituksista ja kyseisten suoritusten arviointia.</span><span class="sxs-lookup"><span data-stu-id="7d84c-107">The [Trace generated report results and compare them with baseline values](er-trace-reports-compare-baseline.md) topic explains how to configure the ER framework to collect information about ER format executions and evaluate the results of those executions.</span></span> <span data-ttu-id="7d84c-108">Tämän ohjeaiheen esimerkki sisältää suoritettavat vaiheet.</span><span class="sxs-lookup"><span data-stu-id="7d84c-108">The example in this topic shows the steps that must be completed.</span></span>

<span data-ttu-id="7d84c-109">Esimerkkejä vaiheista:</span><span class="sxs-lookup"><span data-stu-id="7d84c-109">Here are some of the steps:</span></span>

- <span data-ttu-id="7d84c-110">Luo lähtevä tiedosto suorittamalla ER-muoto ja tallentamalla tiedosto paikallisesti.</span><span class="sxs-lookup"><span data-stu-id="7d84c-110">Run an ER format to generate an outbound file, and store the file locally.</span></span>
- <span data-ttu-id="7d84c-111">Lisää paikallisesti tallennettu tiedosto ER-muotoon lisätyn perusrivin liitteenä.</span><span class="sxs-lookup"><span data-stu-id="7d84c-111">Add the locally stored file as an attachment of the baseline that was added for an ER format.</span></span>
- <span data-ttu-id="7d84c-112">Määritä lisätyn perusrivin perusrivisääntö.</span><span class="sxs-lookup"><span data-stu-id="7d84c-112">Configure the baseline rule for the added baseline.</span></span> <span data-ttu-id="7d84c-113">Tämä määritys sisältää seuraavat vaiheet:</span><span class="sxs-lookup"><span data-stu-id="7d84c-113">This configuration includes the following steps:</span></span>

    - <span data-ttu-id="7d84c-114">Määritä lähtevän tiedoston luontiin käytettävä ER-muotoelementti.</span><span class="sxs-lookup"><span data-stu-id="7d84c-114">Specify an ER format element that is used to generate an outbound file.</span></span>
    - <span data-ttu-id="7d84c-115">Valitse liite, joka viittaa luotuun lähtevään tiedostoon.</span><span class="sxs-lookup"><span data-stu-id="7d84c-115">Select the attachment that refers to the generated outbound file.</span></span>

> [!NOTE]
> <span data-ttu-id="7d84c-116">Nämä vaiheet on tehtävä manuaalisesti, vaikka ne voidaan automatisoida uusissa ER-ominaisuuksissa.</span><span class="sxs-lookup"><span data-stu-id="7d84c-116">These steps must be done manually, even though the new ER capabilities enable them to be automated.</span></span> <span data-ttu-id="7d84c-117">Saat lisätietoja tästä toiminnosta suorittamalla seuraavan esimerkin.</span><span class="sxs-lookup"><span data-stu-id="7d84c-117">To learn more about this feature, complete the following example.</span></span>

## <a name="example-automate-the-setting-of-baseline-rules"></a><span data-ttu-id="7d84c-118">Esimerkki: Perusviivasääntöasetusten automatisointi</span><span class="sxs-lookup"><span data-stu-id="7d84c-118">Example: Automate the setting of baseline rules</span></span>

<span data-ttu-id="7d84c-119">Tämän esimerkin vaiheiden suorittaminen edellyttää, että suoritat ensin ohjeaiheen [Luotuja raporttitulosten seuraaminen ja vertaaminen perusarvoihin](er-trace-reports-compare-baseline.md) esimerkin vaiheet osaan Uuden perusrivin lisääminen suunniteltuun ER-muotoon saakka.</span><span class="sxs-lookup"><span data-stu-id="7d84c-119">To complete the steps in this example, you must first complete the steps in the example in the [Trace generated report results and compare them with baseline values](er-trace-reports-compare-baseline.md) topic, up through the "Add a new baseline for a designed ER format" section.</span></span>

### <a name="review-added-baseline"></a><span data-ttu-id="7d84c-120">Lisätyn perusrivin tarkasteleminen</span><span class="sxs-lookup"><span data-stu-id="7d84c-120">Review added baseline</span></span>

1. <span data-ttu-id="7d84c-121">Valitse **Organisaation hallinto** \> **Sähköinen raportointi** \> **Konfiguraatiot**.</span><span class="sxs-lookup"><span data-stu-id="7d84c-121">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="7d84c-122">Valitse **Perusrivit**.</span><span class="sxs-lookup"><span data-stu-id="7d84c-122">Select **Baselines**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="7d84c-123">Toimintoruudun **Perusrivit**-painike on käytettävissä vain, kun **Suorita viankorjaustilassa** -ER-käyttäjän parametri on otettu käyttöön nykyisessä yrityksessä.</span><span class="sxs-lookup"><span data-stu-id="7d84c-123">The **Baselines** button on the Action Pane is available only when the **Run in debug mode** ER user parameter is turned on for the current company.</span></span>

<span data-ttu-id="7d84c-124">Perusrivi on lisättyyn valittuun **ER-perusrivien oppimismuoto** -muotoon, mutta perusrivisääntöjä ei ole vielä lisätty tähän perusriviin.</span><span class="sxs-lookup"><span data-stu-id="7d84c-124">The baseline has been added for the selected **Format to learn ER baselines** format, but the baseline rules haven't yet been added for this baseline.</span></span>

<span data-ttu-id="7d84c-125">![Sähköisen raportointimuotojen perusrivit -sivu](media/GER-BaselineSample-AddBaseline2.PNG "Näyttökuva Sähköisen raportointimuotojen perusrivit -sivusta")</span><span class="sxs-lookup"><span data-stu-id="7d84c-125">![Electronic reporting format baselines page](media/GER-BaselineSample-AddBaseline2.PNG "Screenshot of the Electronic reporting format baselines page")</span></span>

### <a name="make-a-new-baseline-rule"></a><span data-ttu-id="7d84c-126">Uuden perusrivisäännön luominen</span><span class="sxs-lookup"><span data-stu-id="7d84c-126">Make a new baseline rule</span></span>

1. <span data-ttu-id="7d84c-127">Valitse **Organisaation hallinto** \> **Sähköinen raportointi** \> **Konfiguraatiot**.</span><span class="sxs-lookup"><span data-stu-id="7d84c-127">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="7d84c-128">Laajenna puussa **ER-perusrivien oppimismalli**.</span><span class="sxs-lookup"><span data-stu-id="7d84c-128">In the tree, expand **Model to learn ER baselines**.</span></span>
3. <span data-ttu-id="7d84c-129">Valitse puussa **ER-perusrivien oppimismalli\\ER-perusrivien oppimismuoto**.</span><span class="sxs-lookup"><span data-stu-id="7d84c-129">In the tree, select **Model to learn ER baselines\\Format to learn ER baselines**.</span></span>
4. <span data-ttu-id="7d84c-130">Valitse **Versiot**-pikavälilehdessä **Suorita**.</span><span class="sxs-lookup"><span data-stu-id="7d84c-130">On the **Versions** FastTab, select **Run**.</span></span>
5. <span data-ttu-id="7d84c-131">Kirjoita **Kirjoita tunnus** -kenttään **1**.</span><span class="sxs-lookup"><span data-stu-id="7d84c-131">In the **Enter Id** field, enter **1**.</span></span>
6. <span data-ttu-id="7d84c-132">Määritä **Luo perusrivitiedostot** -asetukseksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="7d84c-132">Set the **Make baseline files** option to **Yes**.</span></span>
7. <span data-ttu-id="7d84c-133">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="7d84c-133">Select **OK**.</span></span>

    <span data-ttu-id="7d84c-134">![Sähköisen raportin parametrit -valintaikkuna](media/GER-BaselineSample-FormatRunToMakeBaselineFile3.PNG "Näyttökuva Sähköisen raportin parametrit -valintaikkunasta")</span><span class="sxs-lookup"><span data-stu-id="7d84c-134">![Electronic report parameters dialog box](media/GER-BaselineSample-FormatRunToMakeBaselineFile3.PNG "Screenshot of the Electronic report parameters dialog box")</span></span>

8. <span data-ttu-id="7d84c-135">Valitse **Perusrivit**.</span><span class="sxs-lookup"><span data-stu-id="7d84c-135">Select **Baselines**.</span></span>

    <span data-ttu-id="7d84c-136">![Sähköisen raportointimuotojen perusrivit -sivu](media/GER-BaselineSample-ReviewAddedBaselineLine.PNG "Näyttökuva Sähköisen raportointimuotojen perusrivit -sivusta")</span><span class="sxs-lookup"><span data-stu-id="7d84c-136">![Electronic reporting format baselines page](media/GER-BaselineSample-ReviewAddedBaselineLine.PNG "Screenshot of the Electronic reporting format baselines page")</span></span>

    <span data-ttu-id="7d84c-137">Luotu lähtevä tiedosto on liitetty automaattisesti suoritetun ER-muodon perusriville.</span><span class="sxs-lookup"><span data-stu-id="7d84c-137">The generated outbound file has been automatically attached to the baseline of the executed ER format.</span></span> <span data-ttu-id="7d84c-138">Perusrivisääntö on lisätty automaattisesti tälle perusriville. Lisäksi se sisältää viittauksen liitettyyn tiedostoon.</span><span class="sxs-lookup"><span data-stu-id="7d84c-138">The baseline rule has been automatically added to this baseline and also contains the reference to the attached file.</span></span>

9. <span data-ttu-id="7d84c-139">Kirjoita **Nimi**-kenttään **Perusrivi 1**.</span><span class="sxs-lookup"><span data-stu-id="7d84c-139">In the **Name** field, enter **Baseline 1**.</span></span>
10. <span data-ttu-id="7d84c-140">Kirjoita **Tiedostonimen peite** -kenttään **.xml**.</span><span class="sxs-lookup"><span data-stu-id="7d84c-140">In the **File name mask** field, enter **.xml**.</span></span>
11. <span data-ttu-id="7d84c-141">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="7d84c-141">Select **Save**.</span></span>

### <a name="run-the-format"></a><span data-ttu-id="7d84c-142">Muodon suorittaminen</span><span class="sxs-lookup"><span data-stu-id="7d84c-142">Run the format</span></span>

<span data-ttu-id="7d84c-143">Voit nyt suorittaa ohjeaiheen [Luotuja raporttitulosten seuraaminen ja vertaaminen perusarvoihin](er-trace-reports-compare-baseline.md) loput vaiheet alkaen osasta Suunnitellun ER-muodon suorittaminen ja tulosten analysointi lokia tarkastelemalla.</span><span class="sxs-lookup"><span data-stu-id="7d84c-143">You're now ready to complete the remaining steps in the example in the [Trace generated report results and compare them with baseline values](er-trace-reports-compare-baseline.md) topic, starting from the "Run the designed ER format and review the log to analyze the results" section.</span></span>

> [!NOTE]
> <span data-ttu-id="7d84c-144">Jos poistat automaattisesti lisätyn perusrivisäännön **Perusrivit**-pikavälilehdessä, viitattua liitettä ei poisteta automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="7d84c-144">When you delete the automatically added baseline rule on the **Baselines** FastTab, the referenced attachment isn't automatically deleted.</span></span>

## <a name="configure-the-baseline-so-that-it-ignores-constantly-changing-parts-of-the-er-output"></a><span data-ttu-id="7d84c-145">Perusrivin määrittäminen ohittamaan ER-tuloksen jatkuvasti muuttuvat osat</span><span class="sxs-lookup"><span data-stu-id="7d84c-145">Configure the baseline so that it ignores constantly changing parts of the ER output</span></span>

<span data-ttu-id="7d84c-146">Jos ER-muoto on suunniteltu sisältämään tietoja, jotka muuttuvat, kun muoto suoritetaan, muodon on käytettävä ER-perusrivitoimintoa, kun luotuja tuloksia verrataan perusriviarvoihin.</span><span class="sxs-lookup"><span data-stu-id="7d84c-146">When an ER format has been designed to contain information that is changed when the format is run, the format must be required to use the ER baseline feature to compare the generated results with baseline values.</span></span> <span data-ttu-id="7d84c-147">Tietoja voivat olla esimerkiksi käsittelypäivämäärä ja -aika tai luodun asiakirjan yksilöllinen tunniste eri muotoisina (kuten \[GUID\]-tunnus).</span><span class="sxs-lookup"><span data-stu-id="7d84c-147">For example, the information might be the processing date and time or the unique identifier of a generated document in different formats (globally unique identifier \[GUID\], and so on).</span></span> <span data-ttu-id="7d84c-148">Uusilla ER-ominaisuuksilla voi määrittää perusrivisäännön siten, että se ohittaa ER-muodon muuttuvat elementit, kun muodon suorittamisella on tarkoitus verrata perusriviarvoja ja muodon suorittamisen tuloksia.</span><span class="sxs-lookup"><span data-stu-id="7d84c-148">The new ER capabilities let you configure the baseline rule so that it ignores changeable elements of an ER format when the format is run with the purpose of comparing baseline values with the results of the format's execution.</span></span> <span data-ttu-id="7d84c-149">Saat lisätietoja tästä toiminnosta suorittamalla seuraavan esimerkin.</span><span class="sxs-lookup"><span data-stu-id="7d84c-149">To learn more about this feature, complete the following example.</span></span>

## <a name="example-configure-the-baseline-so-that-it-ignores-constantly-changing-parts-of-the-er-output"></a><span data-ttu-id="7d84c-150">Esimerkki: Perusrivin määrittäminen ohittamaan ER-tuloksen jatkuvasti muuttuvat osat</span><span class="sxs-lookup"><span data-stu-id="7d84c-150">Example: Configure the baseline so that it ignores constantly changing parts of the ER output</span></span>

<span data-ttu-id="7d84c-151">Tämän esimerkin vaiheiden suorittaminen edellyttää, että suoritat ensin ohjeaiheen [Luotuja raporttitulosten seuraaminen ja vertaaminen perusarvoihin](er-trace-reports-compare-baseline.md) esimerkin vaiheet.</span><span class="sxs-lookup"><span data-stu-id="7d84c-151">To complete the steps in this example, you must first complete the steps in the example in the [Trace generated report results and compare them with baseline values](er-trace-reports-compare-baseline.md) topic.</span></span>

### <a name="modify-a-configured-er-format"></a><span data-ttu-id="7d84c-152">Määritetyn ER-muodon muokkaaminen</span><span class="sxs-lookup"><span data-stu-id="7d84c-152">Modify a configured ER format</span></span>

1. <span data-ttu-id="7d84c-153">Valitse **Organisaation hallinto** \> **Sähköinen raportointi** \> **Konfiguraatiot**.</span><span class="sxs-lookup"><span data-stu-id="7d84c-153">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="7d84c-154">Laajenna puussa **ER-perusrivien oppimismalli**.</span><span class="sxs-lookup"><span data-stu-id="7d84c-154">In the tree, expand **Model to learn ER baselines**.</span></span>
3. <span data-ttu-id="7d84c-155">Valitse puussa **ER-perusrivien oppimismalli\\ER-perusrivien oppimismuoto**.</span><span class="sxs-lookup"><span data-stu-id="7d84c-155">In the tree, select **Model to learn ER baselines\\Format to learn ER baselines**.</span></span>
4. <span data-ttu-id="7d84c-156">Valitse **Suunnittelu**.</span><span class="sxs-lookup"><span data-stu-id="7d84c-156">Select **Designer**.</span></span>
5. <span data-ttu-id="7d84c-157">Valitse puussa **Tuloste\\Asiakirja**.</span><span class="sxs-lookup"><span data-stu-id="7d84c-157">In the tree, select **Output\\Document**.</span></span>
6. <span data-ttu-id="7d84c-158">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="7d84c-158">Select **Add**.</span></span>
7. <span data-ttu-id="7d84c-159">Valitse puun avattavassa valikossa **XML\\Attribute**.</span><span class="sxs-lookup"><span data-stu-id="7d84c-159">In the drop-down dialog box, in the tree, select **XML\\Attribute**.</span></span>
8. <span data-ttu-id="7d84c-160">Kirjoita **Nimi**-kenttään **ProcessingDateTime**.</span><span class="sxs-lookup"><span data-stu-id="7d84c-160">In the **Name** field, enter **ProcessingDateTime**.</span></span>
9. <span data-ttu-id="7d84c-161">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="7d84c-161">Select **OK**.</span></span>
10. <span data-ttu-id="7d84c-162">Valitse puun **Yhdistämismääritys**-välilehdessä **Output\\Document\\ProcessingDateTime**.</span><span class="sxs-lookup"><span data-stu-id="7d84c-162">On the **Mapping** tab, in the tree, select **Output\\Document\\ProcessingDateTime**.</span></span>
11. <span data-ttu-id="7d84c-163">Valitse **Muokkaa kaavaa**.</span><span class="sxs-lookup"><span data-stu-id="7d84c-163">Select **Edit formula**.</span></span>
12. <span data-ttu-id="7d84c-164">Lisää **Kaava**-kentässä seuraava lauseke: **DATETIMEFORMAT(NOW(), "O")**</span><span class="sxs-lookup"><span data-stu-id="7d84c-164">In the **Formula** field, enter the following expression: **DATETIMEFORMAT(NOW(), "O")**</span></span>
13. <span data-ttu-id="7d84c-165">Valitse ensin **Tallenna** ja sitten **Testi**.</span><span class="sxs-lookup"><span data-stu-id="7d84c-165">Select **Save**, and then select **Test**.</span></span>
14. <span data-ttu-id="7d84c-166">Testaa määritetty lauseke uudelleen valitsemalla **Testi** uudelleen.</span><span class="sxs-lookup"><span data-stu-id="7d84c-166">Select **Test** again to retest the configured expression.</span></span>

    <span data-ttu-id="7d84c-167">![Reseptien suunnittelu -sivu](media/GER-BaselineSample-DefineProcessingDTExpression.PNG "Näyttökuva Reseptien suunnittelu -sivusta")</span><span class="sxs-lookup"><span data-stu-id="7d84c-167">![Formula designer page](media/GER-BaselineSample-DefineProcessingDTExpression.PNG "Screenshot of the Formula designer page")</span></span>

    > [!NOTE]
    > <span data-ttu-id="7d84c-168">**Testin tulos** -välilehdestä havaitaan, että määritetty lauseke palauttaa eri päivämäärä- ja aika-arvon aina, kun se kutsutaan.</span><span class="sxs-lookup"><span data-stu-id="7d84c-168">The **Test result** tab shows that the configured expression returns a different date and time value whenever it's called.</span></span>

15. <span data-ttu-id="7d84c-169">Sulje **Reseptien suunnittelu** -sivu ja valitse sitten **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="7d84c-169">Close the **Formula designer** page, and then select **Save**.</span></span>

    <span data-ttu-id="7d84c-170">![Muodon suunnittelija -sivu](media/GER-BaselineSample-FormatMappingDesign2.PNG "Näyttökuva Muodon suunnittelija -sivusta")</span><span class="sxs-lookup"><span data-stu-id="7d84c-170">![Format designer page](media/GER-BaselineSample-FormatMappingDesign2.PNG "Screenshot of the Format designer page")</span></span>

16. <span data-ttu-id="7d84c-171">Sulje **Muodon suunnittelija** -sivu.</span><span class="sxs-lookup"><span data-stu-id="7d84c-171">Close the **Format designer** page.</span></span>

### <a name="remove-an-existing-baseline-rule"></a><span data-ttu-id="7d84c-172">Aiemmin luodun perusrivisäännön poistaminen</span><span class="sxs-lookup"><span data-stu-id="7d84c-172">Remove an existing baseline rule</span></span>

1. <span data-ttu-id="7d84c-173">Valitse **Organisaation hallinto** \> **Sähköinen raportointi** \> **Konfiguraatiot**.</span><span class="sxs-lookup"><span data-stu-id="7d84c-173">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="7d84c-174">Valitse **Perusrivit**.</span><span class="sxs-lookup"><span data-stu-id="7d84c-174">Select **Baselines**.</span></span>
3. <span data-ttu-id="7d84c-175">Valitse perusriviluettelossa **ER-perusrivien oppimismuoto** -muodolle määritetty perusrivi.</span><span class="sxs-lookup"><span data-stu-id="7d84c-175">In the list of baselines, select the baseline that is configured for the **Format to learn ER baselines** format.</span></span>
4. <span data-ttu-id="7d84c-176">Poista aiemmin määritetty perusrivisääntö valitsemalla **Perusrivit**-pikavälilehdessä **Poista**.</span><span class="sxs-lookup"><span data-stu-id="7d84c-176">On the **Baselines** FastTab, select **Delete** to remove the baseline rule that you configured earlier.</span></span>

<span data-ttu-id="7d84c-177">![Sähköisen raportointimuotojen perusrivit -sivu](media/GER-BaselineSample-AddBaseline3.PNG "Näyttökuva Sähköisen raportointimuotojen perusrivit -sivusta")</span><span class="sxs-lookup"><span data-stu-id="7d84c-177">![Electronic reporting format baselines page](media/GER-BaselineSample-AddBaseline3.PNG "Screenshot of the Electronic reporting format baselines page")</span></span>

### <a name="define-replacements-for-bindings-of-designed-er-format"></a><span data-ttu-id="7d84c-178">Suunnitellun ER-muodon sidosten korvaamisen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="7d84c-178">Define replacements for bindings of designed ER format</span></span>

1. <span data-ttu-id="7d84c-179">Valitse **Konfiguroinnit**-sivulla **Korvaava**-pikavälilehdellä **Valitse osat**.</span><span class="sxs-lookup"><span data-stu-id="7d84c-179">On the **Configurations** page, on the **Replacements** FastTab, select **Select components**.</span></span>
2. <span data-ttu-id="7d84c-180">Laajenna muoto-osapuussa ensin**Tuloste** ja sitten **Tuloste\\Asiakirja**. Valitse sitten **Tuloste\\Asiakirja\\ProcessingDateTime** -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="7d84c-180">In the format components tree, expand **Output**, expand **Output\\Document**, and then select the check box for **Output\\Document\\ProcessingDateTime**.</span></span>

    <span data-ttu-id="7d84c-181">![Valitse osat -valintaikkuna](media/GER-BaselineSample-SelectComponentForBindingReplacement.PNG "Näyttökuva Valitse osat -valintaikkunasta")</span><span class="sxs-lookup"><span data-stu-id="7d84c-181">![Select Components dialog box](media/GER-BaselineSample-SelectComponentForBindingReplacement.PNG "Screenshot of the Select Components dialog box")</span></span>

3. <span data-ttu-id="7d84c-182">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="7d84c-182">Select **OK**.</span></span>

<span data-ttu-id="7d84c-183">![Sähköisen raportointimuotojen perusrivit -sivu](media/GER-BaselineSample-AddBaseline4.PNG "Näyttökuva Sähköisen raportointimuotojen perusrivit -sivusta")</span><span class="sxs-lookup"><span data-stu-id="7d84c-183">![Electronic reporting format baselines page](media/GER-BaselineSample-AddBaseline4.PNG "Screenshot of the Electronic reporting format baselines page")</span></span>

<span data-ttu-id="7d84c-184">Valittu ER-muoto-osa on lisätty osaluetteloon **Korvaava**-pikavälilehteen.</span><span class="sxs-lookup"><span data-stu-id="7d84c-184">The selected ER format component has been added to the list of components on the **Replacements** FastTab.</span></span> <span data-ttu-id="7d84c-185">Kun ER-perusmuoto suoritetaan virheenkorjaustilassa, muodon kunkin osan sidonta korvataan sidonnalla, joka näkyy **Sidonta**-sarakkeessa.</span><span class="sxs-lookup"><span data-stu-id="7d84c-185">When the base ER format is run in debug mode, the format's binding for each component will be replaced by the binding that is shown in the **Binding** column.</span></span> <span data-ttu-id="7d84c-186">Voit muuttaa **Korvaava**-pikavälilehdessä mainitun osan oletussidonnan valitsemalla **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="7d84c-186">To change the default binding for a component that is listed on the **Replacements** FastTab, select **Edit**.</span></span>

### <a name="make-a-new-baseline-rule"></a><span data-ttu-id="7d84c-187">Uuden perusrivisäännön luominen</span><span class="sxs-lookup"><span data-stu-id="7d84c-187">Make a new baseline rule</span></span>

<span data-ttu-id="7d84c-188">Noudata tämän ohjeaiheen aiemman Esimerkki: Perusviivasääntöasetusten automatisointi -osan ohjeita.</span><span class="sxs-lookup"><span data-stu-id="7d84c-188">Follow the steps in the "Example: Automate the setting of baseline rules" section earlier in this topic.</span></span> <span data-ttu-id="7d84c-189">Ilmoitus varoittaa, että lähtevä tiedosto on luotu käyttämällä perusrivin asetuksia ja että muodon sidontojen pakotettu korvaus on tehty.</span><span class="sxs-lookup"><span data-stu-id="7d84c-189">A notification warns you that the outbound file has been generated by using baseline settings, and that a forced replacement of the format bindings has occurred.</span></span>

<span data-ttu-id="7d84c-190">![Ilmoitus Konfiguroinnit-sivulla](media/GER-BaselineSample-FormatRunToMakeBaselineFile4.PNG "Näyttökuva ilmoituksesta Konfiguroinnit-sivulla")</span><span class="sxs-lookup"><span data-stu-id="7d84c-190">![Notification on the Configurations page](media/GER-BaselineSample-FormatRunToMakeBaselineFile4.PNG "Screenshot of the notification on the Configurations page")</span></span>

### <a name="suppress-warnings-about-the-replacement-of-format-bindings"></a><span data-ttu-id="7d84c-191">Muodon sidosten korvaamista koskevien varoitusten piilottaminen</span><span class="sxs-lookup"><span data-stu-id="7d84c-191">Suppress warnings about the replacement of format bindings</span></span>

<span data-ttu-id="7d84c-192">Määrittämällä tietyt ER-parametrit voit piilottaa muodon sidosten korvaamisesta varoittavat ilmoitukset.</span><span class="sxs-lookup"><span data-stu-id="7d84c-192">By setting specific ER parameters, you can suppress notifications that warn about the replacement of format bindings.</span></span> <span data-ttu-id="7d84c-193">Tällaisesta piilottamisesta voi olla hyötyä, jos muodon sidokset korvataan valvomattomassa tilassa Regression Suite Automation Tool -työkalulla.</span><span class="sxs-lookup"><span data-stu-id="7d84c-193">This suppression can be useful when format bindings are replaced in an unattended mode by using the Regression Suite Automation Tool.</span></span> <span data-ttu-id="7d84c-194">Siinä tapauksessa varoituksen voidaan ilmaisevan, että suoritettava testitapaus on epäonnistunut.</span><span class="sxs-lookup"><span data-stu-id="7d84c-194">In this case, the warning can be considered a failure of the test case that is running.</span></span>

1. <span data-ttu-id="7d84c-195">Valitse **Konfiguroinnit**-sivun toimintoruudun **Konfiguroinnit**-välilehdessä **Käyttäjän parametrit**.</span><span class="sxs-lookup"><span data-stu-id="7d84c-195">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, select **User parameters**.</span></span>
2. <span data-ttu-id="7d84c-196">Määritä **Piilota perusrivivaroitukset** -asetukseksi **Kyllä** ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="7d84c-196">Set the **Suppress baseline warnings** option to **Yes**, and then select **OK**.</span></span>

<span data-ttu-id="7d84c-197">![Käyttäjän parametrit -valintaruutu](media/GER-BaselineSample-ERUserParameters1.png "Näyttökuva Käyttäjän parametrit -valintaikkunasta")</span><span class="sxs-lookup"><span data-stu-id="7d84c-197">![User parameters dialog box](media/GER-BaselineSample-ERUserParameters1.png "Screenshot of the User parameters dialog box")</span></span>

### <a name="review-the-generated-baseline-file"></a><span data-ttu-id="7d84c-198">Luodun perusrivitiedoston tarkasteleminen</span><span class="sxs-lookup"><span data-stu-id="7d84c-198">Review the generated baseline file</span></span>

1. <span data-ttu-id="7d84c-199">Valitse **Organisaation hallinto** \> **Sähköinen raportointi** \> **Konfiguraatiot**.</span><span class="sxs-lookup"><span data-stu-id="7d84c-199">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="7d84c-200">Valitse **Perusrivit**.</span><span class="sxs-lookup"><span data-stu-id="7d84c-200">Select **Baselines**.</span></span>
3. <span data-ttu-id="7d84c-201">Valitse **Liitteet**.</span><span class="sxs-lookup"><span data-stu-id="7d84c-201">Select **Attachments**.</span></span>

    <span data-ttu-id="7d84c-202">![Liitteet-sivu](media/GER-BaselineSample-AttachedBaselineFile.PNG "Näyttökuva Liitteet-sivusta")</span><span class="sxs-lookup"><span data-stu-id="7d84c-202">![Attachments page](media/GER-BaselineSample-AttachedBaselineFile.PNG "Screenshot of the Attachments page")</span></span>

    > [!NOTE]
    > <span data-ttu-id="7d84c-203">Luotu tiedosto sisältää käsittelypäivämäärän ja -ajan tekstin (**"#"**) lisätyssä perusrivisäännössä määritetystä sidoksesta eikä muodon sidoksesta.</span><span class="sxs-lookup"><span data-stu-id="7d84c-203">The generated file contains the processing date and time text (**"#"**) from the binding that was configured in the added baseline rule, not from the format's binding.</span></span>

4. <span data-ttu-id="7d84c-204">Sulje **Liitteet**-sivu.</span><span class="sxs-lookup"><span data-stu-id="7d84c-204">Close the **Attachments** page.</span></span>

### <a name="run-the-designed-er-format-and-review-the-log-to-analyze-the-results"></a><span data-ttu-id="7d84c-205">Suunnitellun ER-muoto suorittaminen ja tulosten analysointi lokia tarkastelemalla</span><span class="sxs-lookup"><span data-stu-id="7d84c-205">Run the designed ER format and review the log to analyze the results</span></span>

1. <span data-ttu-id="7d84c-206">Valitse **Organisaation hallinto** \> **Sähköinen raportointi** \> **Konfiguraatiot**.</span><span class="sxs-lookup"><span data-stu-id="7d84c-206">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="7d84c-207">Laajenna puussa **ER-perusrivien oppimismalli**.</span><span class="sxs-lookup"><span data-stu-id="7d84c-207">In the tree, expand **Model to learn ER baselines**.</span></span>
3. <span data-ttu-id="7d84c-208">Valitse puussa **ER-perusrivien oppimismalli\\ER-perusrivien oppimismuoto**.</span><span class="sxs-lookup"><span data-stu-id="7d84c-208">In the tree, select **Model to learn ER baselines\\Format to learn ER baselines**.</span></span>
4. <span data-ttu-id="7d84c-209">Valitse **Versiot**-pikavälilehdessä **Suorita**.</span><span class="sxs-lookup"><span data-stu-id="7d84c-209">On the **Versions** FastTab select **Run**.</span></span>
5. <span data-ttu-id="7d84c-210">Kirjoita **Kirjoita tunnus** -kenttään **1**.</span><span class="sxs-lookup"><span data-stu-id="7d84c-210">In the **Enter Id** field, type **1**.</span></span>
6. <span data-ttu-id="7d84c-211">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="7d84c-211">Select **OK**.</span></span>
7. <span data-ttu-id="7d84c-212">Valitse **Organisaation hallinto** \> **Sähköinen raportointi** \> **Määritysten virheenkorjauslokit**.</span><span class="sxs-lookup"><span data-stu-id="7d84c-212">Go to **Organization administration** \> **Electronic reporting** \> **Configuration debug logs**.</span></span>

<span data-ttu-id="7d84c-213">Suorituslokissa sisältää tietoja luodun tiedoston ja määritetyn perusrivin vertailutuloksista.</span><span class="sxs-lookup"><span data-stu-id="7d84c-213">The execution log contains information about the results of the comparison of the generated file with the configured baseline.</span></span> <span data-ttu-id="7d84c-214">Loki ilmaisee, että luotu tiedosto ja perusrivi ovat samanlaiset, vaikka suoritetussa muodossa on sidonta, jolla annetaan jatkuvasti muuttuva päivämäärä- ja aika-arvo lähtevässä tiedostossa.</span><span class="sxs-lookup"><span data-stu-id="7d84c-214">The log indicates that the generated file and the baseline are equal, even though the executed format contains the binding to enter a constantly changing date and time value in the outbound file.</span></span>

> [!NOTE]
> <span data-ttu-id="7d84c-215">Vaikka lähtevä tiedosto on luotu käyttämällä perusriviasetuksia, jotka pakottavat muodon sidosten korvaamisen, korvaamisesta ei saada varoituksia.</span><span class="sxs-lookup"><span data-stu-id="7d84c-215">Although the outbound file has been generated by using baseline settings that force the replacement of the format's bindings, you don't receive any warnings about the replacement.</span></span>

## <a name="exchange-baseline-settings-between-environments"></a><span data-ttu-id="7d84c-216">Perusriviasetusten vaihtaminen ympäristöjen välillä</span><span class="sxs-lookup"><span data-stu-id="7d84c-216">Exchange baseline settings between environments</span></span>

### <a name="export-baseline-settings"></a><span data-ttu-id="7d84c-217">Perusriviasetusten vieminen</span><span class="sxs-lookup"><span data-stu-id="7d84c-217">Export baseline settings</span></span>

<span data-ttu-id="7d84c-218">Uusilla ER-ominaisuuksilla voi viedä valitun ER-muodon perusriviasetukset nykyisestä Finance and Operations -ympäristöstä ja tallentaa ne XML-tiedostona.</span><span class="sxs-lookup"><span data-stu-id="7d84c-218">The new ER capabilities let you export baseline settings for the selected ER format from the current Finance and Operations environment and store them as XML files.</span></span> 

<span data-ttu-id="7d84c-219">Voit viedä perusriviasetukset valitsemalla **Sähköisen raportointimuotojen perusrivit** -sivulla **Vie**.</span><span class="sxs-lookup"><span data-stu-id="7d84c-219">To export baseline settings, on the **Electronic reporting format baselines** page, select **Export**.</span></span>

### <a name="import-baseline-settings"></a><span data-ttu-id="7d84c-220">Tuo perustason asetukset</span><span class="sxs-lookup"><span data-stu-id="7d84c-220">Import baseline settings</span></span>

<span data-ttu-id="7d84c-221">Viedyt perusriviasetukset voidaan viedä toiseen Finance and Operations -ympäristöön.</span><span class="sxs-lookup"><span data-stu-id="7d84c-221">Exported baseline settings can be imported into a different Finance and Operations environment.</span></span> <span data-ttu-id="7d84c-222">Ympäristö on vietävä ensin ER-muodossa.</span><span class="sxs-lookup"><span data-stu-id="7d84c-222">The environment must first be imported as an ER format.</span></span> <span data-ttu-id="7d84c-223">Voit sitten viedä perusriviasetukset.</span><span class="sxs-lookup"><span data-stu-id="7d84c-223">You can then import the baseline settings.</span></span>

<span data-ttu-id="7d84c-224">Voit tuoda perusriviasetukset paikallisesti tallennetusta XML-tiedostosta valitsemalla XML-tiedoston valitsemalla **Sähköisen raportointimuotojen perusrivit** -sivulla ensin **Tuo** ja sitten **Selaa**.</span><span class="sxs-lookup"><span data-stu-id="7d84c-224">To import baseline settings from a locally stored XML file, on the **Electronic reporting format baselines** page, select **Import**, and then select **Browse** to select the XML file.</span></span>

<span data-ttu-id="7d84c-225">![Tuo perusriviasetukset -valintaikkuna](media/GER-BaselineSample-ImportBaseline1.PNG "Näyttökuva Tuo perusriviasetukset -valintaikkunasta")</span><span class="sxs-lookup"><span data-stu-id="7d84c-225">![Import baseline settings dialog box](media/GER-BaselineSample-ImportBaseline1.PNG "Screenshot of the Import baseline settings dialog box")</span></span>

<span data-ttu-id="7d84c-226">Voit tuoda perusriviasetukset Microsoft SharePoint Serveriin tallennetusta XML-tiedostosta nykyisten tiedoston hallinta-asetusten ja valitun asiakirjatyypin perusteella valitsemalla **Sähköisen raportointimuotojen perusrivit** -sivulla **Tuo lähteestä**.</span><span class="sxs-lookup"><span data-stu-id="7d84c-226">To import baseline settings from an XML file that is stored on the Microsoft SharePoint Server, based on the current Document management settings and the selected document type, on the **Electronic reporting format baselines** page, select **Import from source**.</span></span> <span data-ttu-id="7d84c-227">Valitse sitten asiakirjatyyppi ja XML-tiedosto.</span><span class="sxs-lookup"><span data-stu-id="7d84c-227">Then select the document type and the XML file.</span></span> <span data-ttu-id="7d84c-228">SharePoint-kansion käyttämiseen tarvittava asiakirjatyyppi on määritettävä etukäteen.</span><span class="sxs-lookup"><span data-stu-id="7d84c-228">The required document type to access the SharePoint folder must be configured in advance.</span></span>

<span data-ttu-id="7d84c-229">![Tuo lähteestä -valintaikkuna](media/GER-BaselineSample-ImportBaseline2.PNG "Näyttökuva Tuo lähteestä -valintaikkunasta")</span><span class="sxs-lookup"><span data-stu-id="7d84c-229">![Import from source dialog box](media/GER-BaselineSample-ImportBaseline2.PNG "Screenshot of the Import from source dialog box")</span></span>

> [!NOTE]
> <span data-ttu-id="7d84c-230">Voit tallentaa pakollisen asiakirjatyypin valintavaiheet tehtävän tallennustoiminnolla ja tiedoston nimen **Tuo lähteestä** -valintaikkunassa.</span><span class="sxs-lookup"><span data-stu-id="7d84c-230">You can use Task recorder to record the steps for selecting the required document type and the file name in the **Import from source** dialog box.</span></span> <span data-ttu-id="7d84c-231">Tällä tavoin voit pitää pakolliset perusriviasetukset SharePoint Serverissä ja tuoda ne sitten toistamalla tehtävätallenne, kun automatisoituja testejä suoritetaan Regression Suite Automation Tool -työkalulla.</span><span class="sxs-lookup"><span data-stu-id="7d84c-231">In this way, you can keep required baseline settings on SharePoint Server and then automatically import them by playing a task recording when you run automated tests by using the Regression Suite Automation Tool.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7d84c-232">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="7d84c-232">Additional resources</span></span>

- [<span data-ttu-id="7d84c-233">Seuraa luotuja raporttituloksia ja vertaa niitä perusarvoihin</span><span class="sxs-lookup"><span data-stu-id="7d84c-233">Trace generated report results and compare them with baseline values</span></span>](er-trace-reports-compare-baseline.md)
- [<span data-ttu-id="7d84c-234">Tehtävän tallennus</span><span class="sxs-lookup"><span data-stu-id="7d84c-234">Task recorder</span></span>](../user-interface/task-recorder.md)
