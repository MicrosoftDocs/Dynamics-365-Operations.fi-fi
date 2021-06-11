---
title: Luotujen sähköisen raportoinnin raporttien tulosten seuraamisen ja perusarvoihin vertaamisen parannukset
description: Tässä aiheessa käsitellään ER-perusrivitoiminnon parannuksia Microsoft Dynamics 365 for Finance and Operationsin versiossa 10.0.3 (kesäkuu 2019).
author: NickSelin
ms.date: 06/19/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.openlocfilehash: 49ca9a878b9289b02f9bb9346190425197e0ceea
ms.sourcegitcommit: 53b797ff1b524f581046b48cdde42f50b37495bc
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/28/2021
ms.locfileid: "6117032"
---
# <a name="improve-tracing-the-results-of-generated-er-reports-to-compare-with-baseline-values"></a><span data-ttu-id="353f8-103">Luotujen sähköisen raportoinnin raporttien tulosten seuraamisen ja perusarvoihin vertaamisen parannukset</span><span class="sxs-lookup"><span data-stu-id="353f8-103">Improve tracing the results of generated ER reports to compare with baseline values</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="353f8-104">Tässä ohjeaiheessa käsitellään ensimmäisiä sähköisen raportoinnin (ER) kehyksen perusviivatoimintoon parannuksia.</span><span class="sxs-lookup"><span data-stu-id="353f8-104">This topic describes the first set of improvements that have been made to the baseline feature of the Electronic reporting (ER) framework.</span></span> <span data-ttu-id="353f8-105">Nämä parannukset ovat käytettävissä Microsoft Dynamics 365 for Finance and Operationsin versiossa 10.0.3 (kesäkuu 2019) tai uudemmassa.</span><span class="sxs-lookup"><span data-stu-id="353f8-105">These improvements are available in Microsoft Dynamics 365 for Finance and Operations version 10.0.3 (June 2019) and later.</span></span>

## <a name="automate-the-setting-of-baseline-rules"></a><span data-ttu-id="353f8-106">Perusviivasääntöasetusten automatisointi</span><span class="sxs-lookup"><span data-stu-id="353f8-106">Automate the setting of baseline rules</span></span>

<span data-ttu-id="353f8-107">Ohjeaiheessa [Luotuja raporttitulosten seuraaminen ja vertaaminen perusarvoihin](er-trace-reports-compare-baseline.md) käsitellään ER-kehys määrittämistä keräämään tietoja ER-muodon suorituksista ja kyseisten suoritusten arviointia.</span><span class="sxs-lookup"><span data-stu-id="353f8-107">The [Trace generated report results and compare them with baseline values](er-trace-reports-compare-baseline.md) topic explains how to configure the ER framework to collect information about ER format executions and evaluate the results of those executions.</span></span> <span data-ttu-id="353f8-108">Tämän ohjeaiheen esimerkki sisältää suoritettavat vaiheet.</span><span class="sxs-lookup"><span data-stu-id="353f8-108">The example in this topic shows the steps that must be completed.</span></span>

<span data-ttu-id="353f8-109">Esimerkkejä vaiheista:</span><span class="sxs-lookup"><span data-stu-id="353f8-109">Here are some of the steps:</span></span>

- <span data-ttu-id="353f8-110">Luo lähtevä tiedosto suorittamalla ER-muoto ja tallentamalla tiedosto paikallisesti.</span><span class="sxs-lookup"><span data-stu-id="353f8-110">Run an ER format to generate an outbound file, and store the file locally.</span></span>
- <span data-ttu-id="353f8-111">Lisää paikallisesti tallennettu tiedosto ER-muotoon lisätyn perusrivin liitteenä.</span><span class="sxs-lookup"><span data-stu-id="353f8-111">Add the locally stored file as an attachment of the baseline that was added for an ER format.</span></span>
- <span data-ttu-id="353f8-112">Määritä lisätyn perusrivin perusrivisääntö.</span><span class="sxs-lookup"><span data-stu-id="353f8-112">Configure the baseline rule for the added baseline.</span></span> <span data-ttu-id="353f8-113">Tämä määritys sisältää seuraavat vaiheet:</span><span class="sxs-lookup"><span data-stu-id="353f8-113">This configuration includes the following steps:</span></span>

    - <span data-ttu-id="353f8-114">Määritä lähtevän tiedoston luontiin käytettävä ER-muotoelementti.</span><span class="sxs-lookup"><span data-stu-id="353f8-114">Specify an ER format element that is used to generate an outbound file.</span></span>
    - <span data-ttu-id="353f8-115">Valitse liite, joka viittaa luotuun lähtevään tiedostoon.</span><span class="sxs-lookup"><span data-stu-id="353f8-115">Select the attachment that refers to the generated outbound file.</span></span>

> [!NOTE]
> <span data-ttu-id="353f8-116">Nämä vaiheet on tehtävä manuaalisesti, vaikka ne voidaan automatisoida uusissa ER-ominaisuuksissa.</span><span class="sxs-lookup"><span data-stu-id="353f8-116">These steps must be done manually, even though the new ER capabilities enable them to be automated.</span></span> <span data-ttu-id="353f8-117">Saat lisätietoja tästä toiminnosta suorittamalla seuraavan esimerkin.</span><span class="sxs-lookup"><span data-stu-id="353f8-117">To learn more about this feature, complete the following example.</span></span>

## <a name="example-automate-the-setting-of-baseline-rules"></a><span data-ttu-id="353f8-118">Esimerkki: Perusviivasääntöasetusten automatisointi</span><span class="sxs-lookup"><span data-stu-id="353f8-118">Example: Automate the setting of baseline rules</span></span>

<span data-ttu-id="353f8-119">Tämän esimerkin vaiheiden suorittaminen edellyttää, että suoritat ensin ohjeaiheen [Luotuja raporttitulosten seuraaminen ja vertaaminen perusarvoihin](er-trace-reports-compare-baseline.md) esimerkin vaiheet osaan Uuden perusrivin lisääminen suunniteltuun ER-muotoon saakka.</span><span class="sxs-lookup"><span data-stu-id="353f8-119">To complete the steps in this example, you must first complete the steps in the example in the [Trace generated report results and compare them with baseline values](er-trace-reports-compare-baseline.md) topic, up through the "Add a new baseline for a designed ER format" section.</span></span>

### <a name="review-added-baseline"></a><span data-ttu-id="353f8-120">Lisätyn perusrivin tarkasteleminen</span><span class="sxs-lookup"><span data-stu-id="353f8-120">Review added baseline</span></span>

1. <span data-ttu-id="353f8-121">Valitse **Organisaation hallinto** \> **Sähköinen raportointi** \> **Konfiguraatiot**.</span><span class="sxs-lookup"><span data-stu-id="353f8-121">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="353f8-122">Valitse **Perusrivit**.</span><span class="sxs-lookup"><span data-stu-id="353f8-122">Select **Baselines**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="353f8-123">Toimintoruudun **Perusrivit**-painike on käytettävissä vain, kun **Suorita viankorjaustilassa** -ER-käyttäjän parametri on otettu käyttöön nykyisessä yrityksessä.</span><span class="sxs-lookup"><span data-stu-id="353f8-123">The **Baselines** button on the Action Pane is available only when the **Run in debug mode** ER user parameter is turned on for the current company.</span></span>

<span data-ttu-id="353f8-124">Perusrivi on lisättyyn valittuun **ER-perusrivien oppimismuoto** -muotoon, mutta perusrivisääntöjä ei ole vielä lisätty tähän perusriviin.</span><span class="sxs-lookup"><span data-stu-id="353f8-124">The baseline has been added for the selected **Format to learn ER baselines** format, but the baseline rules haven't yet been added for this baseline.</span></span>

<span data-ttu-id="353f8-125">![Sähköisen raportointimuotojen perusrivit -sivu, jossa ei ole vielä sääntöjä](media/GER-BaselineSample-AddBaseline2.PNG "Näyttökuva Sähköisen raportointimuotojen perusrivit -sivusta")</span><span class="sxs-lookup"><span data-stu-id="353f8-125">![Electronic reporting format baselines page, no rules yet](media/GER-BaselineSample-AddBaseline2.PNG "Screenshot of the Electronic reporting format baselines page")</span></span>

### <a name="make-a-new-baseline-rule"></a><span data-ttu-id="353f8-126">Uuden perusrivisäännön luominen</span><span class="sxs-lookup"><span data-stu-id="353f8-126">Make a new baseline rule</span></span>

1. <span data-ttu-id="353f8-127">Valitse **Organisaation hallinto** \> **Sähköinen raportointi** \> **Konfiguraatiot**.</span><span class="sxs-lookup"><span data-stu-id="353f8-127">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="353f8-128">Laajenna puussa **ER-perusrivien oppimismalli**.</span><span class="sxs-lookup"><span data-stu-id="353f8-128">In the tree, expand **Model to learn ER baselines**.</span></span>
3. <span data-ttu-id="353f8-129">Valitse puussa **ER-perusrivien oppimismalli\\ER-perusrivien oppimismuoto**.</span><span class="sxs-lookup"><span data-stu-id="353f8-129">In the tree, select **Model to learn ER baselines\\Format to learn ER baselines**.</span></span>
4. <span data-ttu-id="353f8-130">Valitse **Versiot**-pikavälilehdessä **Suorita**.</span><span class="sxs-lookup"><span data-stu-id="353f8-130">On the **Versions** FastTab, select **Run**.</span></span>
5. <span data-ttu-id="353f8-131">Kirjoita **Kirjoita tunnus** -kenttään **1**.</span><span class="sxs-lookup"><span data-stu-id="353f8-131">In the **Enter Id** field, enter **1**.</span></span>
6. <span data-ttu-id="353f8-132">Määritä **Luo perusrivitiedostot** -asetukseksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="353f8-132">Set the **Make baseline files** option to **Yes**.</span></span>
7. <span data-ttu-id="353f8-133">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="353f8-133">Select **OK**.</span></span>
8. <span data-ttu-id="353f8-134">Valitse **Perusrivit**.</span><span class="sxs-lookup"><span data-stu-id="353f8-134">Select **Baselines**.</span></span>

    <span data-ttu-id="353f8-135">![Sähköisen raportointimuodon perusrivit -sivu, perusrivit valittu](media/GER-BaselineSample-ReviewAddedBaselineLine.PNG "Näyttökuva Sähköisen raportointimuotojen perusrivit -sivusta")</span><span class="sxs-lookup"><span data-stu-id="353f8-135">![Electronic reporting format baselines page, baselines selected](media/GER-BaselineSample-ReviewAddedBaselineLine.PNG "Screenshot of the Electronic reporting format baselines page")</span></span>

    <span data-ttu-id="353f8-136">Luotu lähtevä tiedosto on liitetty automaattisesti suoritetun ER-muodon perusriville.</span><span class="sxs-lookup"><span data-stu-id="353f8-136">The generated outbound file has been automatically attached to the baseline of the executed ER format.</span></span> <span data-ttu-id="353f8-137">Perusrivisääntö on lisätty automaattisesti tälle perusriville. Lisäksi se sisältää viittauksen liitettyyn tiedostoon.</span><span class="sxs-lookup"><span data-stu-id="353f8-137">The baseline rule has been automatically added to this baseline and also contains the reference to the attached file.</span></span>

9. <span data-ttu-id="353f8-138">Kirjoita **Nimi**-kenttään **Perusrivi 1**.</span><span class="sxs-lookup"><span data-stu-id="353f8-138">In the **Name** field, enter **Baseline 1**.</span></span>
10. <span data-ttu-id="353f8-139">Kirjoita **Tiedostonimen peite** -kenttään **.xml**.</span><span class="sxs-lookup"><span data-stu-id="353f8-139">In the **File name mask** field, enter **.xml**.</span></span>
11. <span data-ttu-id="353f8-140">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="353f8-140">Select **Save**.</span></span>

### <a name="run-the-format"></a><span data-ttu-id="353f8-141">Muodon suorittaminen</span><span class="sxs-lookup"><span data-stu-id="353f8-141">Run the format</span></span>

<span data-ttu-id="353f8-142">Voit nyt suorittaa ohjeaiheen [Luotuja raporttitulosten seuraaminen ja vertaaminen perusarvoihin](er-trace-reports-compare-baseline.md) loput vaiheet alkaen osasta Suunnitellun ER-muodon suorittaminen ja tulosten analysointi lokia tarkastelemalla.</span><span class="sxs-lookup"><span data-stu-id="353f8-142">You're now ready to complete the remaining steps in the example in the [Trace generated report results and compare them with baseline values](er-trace-reports-compare-baseline.md) topic, starting from the "Run the designed ER format and review the log to analyze the results" section.</span></span>

> [!NOTE]
> <span data-ttu-id="353f8-143">Jos poistat automaattisesti lisätyn perusrivisäännön **Perusrivit**-pikavälilehdessä, viitattua liitettä ei poisteta automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="353f8-143">When you delete the automatically added baseline rule on the **Baselines** FastTab, the referenced attachment isn't automatically deleted.</span></span>

## <a name="configure-the-baseline-so-that-it-ignores-constantly-changing-parts-of-the-er-output"></a><span data-ttu-id="353f8-144">Perusrivin määrittäminen ohittamaan ER-tuloksen jatkuvasti muuttuvat osat</span><span class="sxs-lookup"><span data-stu-id="353f8-144">Configure the baseline so that it ignores constantly changing parts of the ER output</span></span>

<span data-ttu-id="353f8-145">Jos ER-muoto on suunniteltu sisältämään tietoja, jotka muuttuvat, kun muoto suoritetaan, muodon on käytettävä ER-perusrivitoimintoa, kun luotuja tuloksia verrataan perusriviarvoihin.</span><span class="sxs-lookup"><span data-stu-id="353f8-145">When an ER format has been designed to contain information that is changed when the format is run, the format must be required to use the ER baseline feature to compare the generated results with baseline values.</span></span> <span data-ttu-id="353f8-146">Tietoja voivat olla esimerkiksi käsittelypäivämäärä ja -aika tai luodun asiakirjan yksilöllinen tunniste eri muotoisina (kuten \[GUID\]-tunnus).</span><span class="sxs-lookup"><span data-stu-id="353f8-146">For example, the information might be the processing date and time or the unique identifier of a generated document in different formats (globally unique identifier \[GUID\], and so on).</span></span> <span data-ttu-id="353f8-147">Uusilla ER-ominaisuuksilla voi määrittää perusrivisäännön siten, että se ohittaa ER-muodon muuttuvat elementit, kun muodon suorittamisella on tarkoitus verrata perusriviarvoja ja muodon suorittamisen tuloksia.</span><span class="sxs-lookup"><span data-stu-id="353f8-147">The new ER capabilities let you configure the baseline rule so that it ignores changeable elements of an ER format when the format is run with the purpose of comparing baseline values with the results of the format's execution.</span></span> <span data-ttu-id="353f8-148">Saat lisätietoja tästä toiminnosta suorittamalla seuraavan esimerkin.</span><span class="sxs-lookup"><span data-stu-id="353f8-148">To learn more about this feature, complete the following example.</span></span>

## <a name="example-configure-the-baseline-so-that-it-ignores-constantly-changing-parts-of-the-er-output"></a><span data-ttu-id="353f8-149">Esimerkki: Perusrivin määrittäminen ohittamaan ER-tuloksen jatkuvasti muuttuvat osat</span><span class="sxs-lookup"><span data-stu-id="353f8-149">Example: Configure the baseline so that it ignores constantly changing parts of the ER output</span></span>

<span data-ttu-id="353f8-150">Tämän esimerkin vaiheiden suorittaminen edellyttää, että suoritat ensin ohjeaiheen [Luotuja raporttitulosten seuraaminen ja vertaaminen perusarvoihin](er-trace-reports-compare-baseline.md) esimerkin vaiheet.</span><span class="sxs-lookup"><span data-stu-id="353f8-150">To complete the steps in this example, you must first complete the steps in the example in the [Trace generated report results and compare them with baseline values](er-trace-reports-compare-baseline.md) topic.</span></span>

### <a name="modify-a-configured-er-format"></a><span data-ttu-id="353f8-151">Määritetyn ER-muodon muokkaaminen</span><span class="sxs-lookup"><span data-stu-id="353f8-151">Modify a configured ER format</span></span>

1. <span data-ttu-id="353f8-152">Valitse **Organisaation hallinto** \> **Sähköinen raportointi** \> **Konfiguraatiot**.</span><span class="sxs-lookup"><span data-stu-id="353f8-152">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="353f8-153">Laajenna puussa **ER-perusrivien oppimismalli**.</span><span class="sxs-lookup"><span data-stu-id="353f8-153">In the tree, expand **Model to learn ER baselines**.</span></span>
3. <span data-ttu-id="353f8-154">Valitse puussa **ER-perusrivien oppimismalli\\ER-perusrivien oppimismuoto**.</span><span class="sxs-lookup"><span data-stu-id="353f8-154">In the tree, select **Model to learn ER baselines\\Format to learn ER baselines**.</span></span>
4. <span data-ttu-id="353f8-155">Valitse **Suunnittelu**.</span><span class="sxs-lookup"><span data-stu-id="353f8-155">Select **Designer**.</span></span>
5. <span data-ttu-id="353f8-156">Valitse puussa **Tuloste\\Asiakirja**.</span><span class="sxs-lookup"><span data-stu-id="353f8-156">In the tree, select **Output\\Document**.</span></span>
6. <span data-ttu-id="353f8-157">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="353f8-157">Select **Add**.</span></span>
7. <span data-ttu-id="353f8-158">Valitse puun avattavassa valikossa **XML\\Attribute**.</span><span class="sxs-lookup"><span data-stu-id="353f8-158">In the drop-down dialog box, in the tree, select **XML\\Attribute**.</span></span>
8. <span data-ttu-id="353f8-159">Kirjoita **Nimi**-kenttään **ProcessingDateTime**.</span><span class="sxs-lookup"><span data-stu-id="353f8-159">In the **Name** field, enter **ProcessingDateTime**.</span></span>
9. <span data-ttu-id="353f8-160">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="353f8-160">Select **OK**.</span></span>
10. <span data-ttu-id="353f8-161">Valitse puun **Yhdistämismääritys**-välilehdessä **Output\\Document\\ProcessingDateTime**.</span><span class="sxs-lookup"><span data-stu-id="353f8-161">On the **Mapping** tab, in the tree, select **Output\\Document\\ProcessingDateTime**.</span></span>
11. <span data-ttu-id="353f8-162">Valitse **Muokkaa kaavaa**.</span><span class="sxs-lookup"><span data-stu-id="353f8-162">Select **Edit formula**.</span></span>
12. <span data-ttu-id="353f8-163">Lisää **Kaava**-kentässä seuraava lauseke: **DATETIMEFORMAT(NOW(), "O")**</span><span class="sxs-lookup"><span data-stu-id="353f8-163">In the **Formula** field, enter the following expression: **DATETIMEFORMAT(NOW(), "O")**</span></span>
13. <span data-ttu-id="353f8-164">Valitse ensin **Tallenna** ja sitten **Testi**.</span><span class="sxs-lookup"><span data-stu-id="353f8-164">Select **Save**, and then select **Test**.</span></span>
14. <span data-ttu-id="353f8-165">Testaa määritetty lauseke uudelleen valitsemalla **Testi** uudelleen.</span><span class="sxs-lookup"><span data-stu-id="353f8-165">Select **Test** again to retest the configured expression.</span></span>

    <span data-ttu-id="353f8-166">![Reseptien suunnittelu -sivu.](media/GER-BaselineSample-DefineProcessingDTExpression.PNG "Näyttökuva Reseptien suunnittelu -sivusta")</span><span class="sxs-lookup"><span data-stu-id="353f8-166">![Formula designer page](media/GER-BaselineSample-DefineProcessingDTExpression.PNG "Screenshot of the Formula designer page")</span></span>

    > [!NOTE]
    > <span data-ttu-id="353f8-167">**Testin tulos** -välilehdestä havaitaan, että määritetty lauseke palauttaa eri päivämäärä- ja aika-arvon aina, kun se kutsutaan.</span><span class="sxs-lookup"><span data-stu-id="353f8-167">The **Test result** tab shows that the configured expression returns a different date and time value whenever it's called.</span></span>

15. <span data-ttu-id="353f8-168">Sulje **Reseptien suunnittelu** -sivu ja valitse sitten **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="353f8-168">Close the **Formula designer** page, and then select **Save**.</span></span>

    <span data-ttu-id="353f8-169">![Muodon suunnittelutoiminto -sivu](media/GER-BaselineSample-FormatMappingDesign2.PNG "Näyttökuva Muodon suunnittelija -sivusta")</span><span class="sxs-lookup"><span data-stu-id="353f8-169">![Format designer page](media/GER-BaselineSample-FormatMappingDesign2.PNG "Screenshot of the Format designer page")</span></span>

16. <span data-ttu-id="353f8-170">Sulje **Muodon suunnittelija** -sivu.</span><span class="sxs-lookup"><span data-stu-id="353f8-170">Close the **Format designer** page.</span></span>

### <a name="remove-an-existing-baseline-rule"></a><span data-ttu-id="353f8-171">Aiemmin luodun perusrivisäännön poistaminen</span><span class="sxs-lookup"><span data-stu-id="353f8-171">Remove an existing baseline rule</span></span>

1. <span data-ttu-id="353f8-172">Valitse **Organisaation hallinto** \> **Sähköinen raportointi** \> **Konfiguraatiot**.</span><span class="sxs-lookup"><span data-stu-id="353f8-172">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="353f8-173">Valitse **Perusrivit**.</span><span class="sxs-lookup"><span data-stu-id="353f8-173">Select **Baselines**.</span></span>
3. <span data-ttu-id="353f8-174">Valitse perusriviluettelossa **ER-perusrivien oppimismuoto** -muodolle määritetty perusrivi.</span><span class="sxs-lookup"><span data-stu-id="353f8-174">In the list of baselines, select the baseline that is configured for the **Format to learn ER baselines** format.</span></span>
4. <span data-ttu-id="353f8-175">Poista aiemmin määritetty perusrivisääntö valitsemalla **Perusrivit**-pikavälilehdessä **Poista**.</span><span class="sxs-lookup"><span data-stu-id="353f8-175">On the **Baselines** FastTab, select **Delete** to remove the baseline rule that you configured earlier.</span></span>

<span data-ttu-id="353f8-176">![Sähköisen raportointimuotojen perusrivit -sivu, poistettu](media/GER-BaselineSample-AddBaseline3.PNG "Näyttökuva Sähköisen raportointimuotojen perusrivit -sivusta")</span><span class="sxs-lookup"><span data-stu-id="353f8-176">![Electronic reporting format baselines page, deleted](media/GER-BaselineSample-AddBaseline3.PNG "Screenshot of the Electronic reporting format baselines page")</span></span>

### <a name="define-replacements-for-bindings-of-designed-er-format"></a><span data-ttu-id="353f8-177">Suunnitellun ER-muodon sidosten korvaamisen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="353f8-177">Define replacements for bindings of designed ER format</span></span>

1. <span data-ttu-id="353f8-178">Valitse **Konfiguroinnit**-sivulla **Korvaava**-pikavälilehdellä **Valitse osat**.</span><span class="sxs-lookup"><span data-stu-id="353f8-178">On the **Configurations** page, on the **Replacements** FastTab, select **Select components**.</span></span>
2. <span data-ttu-id="353f8-179">Laajenna muoto-osapuussa ensin **Tuloste** ja sitten **Tuloste\\Asiakirja**. Valitse sitten **Tuloste\\Asiakirja\\ProcessingDateTime** -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="353f8-179">In the format components tree, expand **Output**, expand **Output\\Document**, and then select the check box for **Output\\Document\\ProcessingDateTime**.</span></span>
3. <span data-ttu-id="353f8-180">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="353f8-180">Select **OK**.</span></span>

<span data-ttu-id="353f8-181">![Sähköisen raportointimuotojen perusrivit -sivu, osat](media/GER-BaselineSample-AddBaseline4.PNG "Näyttökuva Sähköisen raportointimuotojen perusrivit -sivusta")</span><span class="sxs-lookup"><span data-stu-id="353f8-181">![Electronic reporting format baselines page, components](media/GER-BaselineSample-AddBaseline4.PNG "Screenshot of the Electronic reporting format baselines page")</span></span>

<span data-ttu-id="353f8-182">Valittu ER-muoto-osa on lisätty osaluetteloon **Korvaava**-pikavälilehteen.</span><span class="sxs-lookup"><span data-stu-id="353f8-182">The selected ER format component has been added to the list of components on the **Replacements** FastTab.</span></span> <span data-ttu-id="353f8-183">Kun ER-perusmuoto suoritetaan virheenkorjaustilassa, muodon kunkin osan sidonta korvataan sidonnalla, joka näkyy **Sidonta**-sarakkeessa.</span><span class="sxs-lookup"><span data-stu-id="353f8-183">When the base ER format is run in debug mode, the format's binding for each component will be replaced by the binding that is shown in the **Binding** column.</span></span> <span data-ttu-id="353f8-184">Voit muuttaa **Korvaava**-pikavälilehdessä mainitun osan oletussidonnan valitsemalla **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="353f8-184">To change the default binding for a component that is listed on the **Replacements** FastTab, select **Edit**.</span></span>

### <a name="make-a-new-baseline-rule"></a><span data-ttu-id="353f8-185">Uuden perusrivisäännön luominen</span><span class="sxs-lookup"><span data-stu-id="353f8-185">Make a new baseline rule</span></span>

<span data-ttu-id="353f8-186">Noudata tämän ohjeaiheen aiemman Esimerkki: Perusviivasääntöasetusten automatisointi -osan ohjeita.</span><span class="sxs-lookup"><span data-stu-id="353f8-186">Follow the steps in the "Example: Automate the setting of baseline rules" section earlier in this topic.</span></span> <span data-ttu-id="353f8-187">Ilmoitus varoittaa, että lähtevä tiedosto on luotu käyttämällä perusrivin asetuksia ja että muodon sidontojen pakotettu korvaus on tehty.</span><span class="sxs-lookup"><span data-stu-id="353f8-187">A notification warns you that the outbound file has been generated by using baseline settings, and that a forced replacement of the format bindings has occurred.</span></span>

<span data-ttu-id="353f8-188">![Ilmoitus Konfiguroinnit-sivulla](media/GER-BaselineSample-FormatRunToMakeBaselineFile4.PNG "Näyttökuva ilmoituksesta Konfiguroinnit-sivulla")</span><span class="sxs-lookup"><span data-stu-id="353f8-188">![Notification on the Configurations page](media/GER-BaselineSample-FormatRunToMakeBaselineFile4.PNG "Screenshot of the notification on the Configurations page")</span></span>

### <a name="suppress-warnings-about-the-replacement-of-format-bindings"></a><span data-ttu-id="353f8-189">Muodon sidosten korvaamista koskevien varoitusten piilottaminen</span><span class="sxs-lookup"><span data-stu-id="353f8-189">Suppress warnings about the replacement of format bindings</span></span>

<span data-ttu-id="353f8-190">Määrittämällä tietyt ER-parametrit voit piilottaa muodon sidosten korvaamisesta varoittavat ilmoitukset.</span><span class="sxs-lookup"><span data-stu-id="353f8-190">By setting specific ER parameters, you can suppress notifications that warn about the replacement of format bindings.</span></span> <span data-ttu-id="353f8-191">Tällaisesta piilottamisesta voi olla hyötyä, jos muodon sidokset korvataan valvomattomassa tilassa Regression Suite Automation Tool -työkalulla.</span><span class="sxs-lookup"><span data-stu-id="353f8-191">This suppression can be useful when format bindings are replaced in an unattended mode by using the Regression Suite Automation Tool.</span></span> <span data-ttu-id="353f8-192">Siinä tapauksessa varoituksen voidaan ilmaisevan, että suoritettava testitapaus on epäonnistunut.</span><span class="sxs-lookup"><span data-stu-id="353f8-192">In this case, the warning can be considered a failure of the test case that is running.</span></span>

1. <span data-ttu-id="353f8-193">Valitse **Konfiguroinnit**-sivun toimintoruudun **Konfiguroinnit**-välilehdessä **Käyttäjän parametrit**.</span><span class="sxs-lookup"><span data-stu-id="353f8-193">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, select **User parameters**.</span></span>
2. <span data-ttu-id="353f8-194">Määritä **Piilota perusrivivaroitukset** -asetukseksi **Kyllä** ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="353f8-194">Set the **Suppress baseline warnings** option to **Yes**, and then select **OK**.</span></span>

### <a name="review-the-generated-baseline-file"></a><span data-ttu-id="353f8-195">Luodun perusrivitiedoston tarkasteleminen</span><span class="sxs-lookup"><span data-stu-id="353f8-195">Review the generated baseline file</span></span>

1. <span data-ttu-id="353f8-196">Valitse **Organisaation hallinto** \> **Sähköinen raportointi** \> **Konfiguraatiot**.</span><span class="sxs-lookup"><span data-stu-id="353f8-196">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="353f8-197">Valitse **Perusrivit**.</span><span class="sxs-lookup"><span data-stu-id="353f8-197">Select **Baselines**.</span></span>
3. <span data-ttu-id="353f8-198">Valitse **Liitteet**.</span><span class="sxs-lookup"><span data-stu-id="353f8-198">Select **Attachments**.</span></span>
    > [!NOTE]
    > <span data-ttu-id="353f8-199">Luotu tiedosto sisältää käsittelypäivämäärän ja -ajan tekstin (**"#"**) lisätyssä perusrivisäännössä määritetystä sidoksesta eikä muodon sidoksesta.</span><span class="sxs-lookup"><span data-stu-id="353f8-199">The generated file contains the processing date and time text (**"#"**) from the binding that was configured in the added baseline rule, not from the format's binding.</span></span>
    
4. <span data-ttu-id="353f8-200">Sulje **Liitteet**-sivu.</span><span class="sxs-lookup"><span data-stu-id="353f8-200">Close the **Attachments** page.</span></span>

### <a name="run-the-designed-er-format-and-review-the-log-to-analyze-the-results"></a><span data-ttu-id="353f8-201">Suunnitellun ER-muoto suorittaminen ja tulosten analysointi lokia tarkastelemalla</span><span class="sxs-lookup"><span data-stu-id="353f8-201">Run the designed ER format and review the log to analyze the results</span></span>

1. <span data-ttu-id="353f8-202">Valitse **Organisaation hallinto** \> **Sähköinen raportointi** \> **Konfiguraatiot**.</span><span class="sxs-lookup"><span data-stu-id="353f8-202">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="353f8-203">Laajenna puussa **ER-perusrivien oppimismalli**.</span><span class="sxs-lookup"><span data-stu-id="353f8-203">In the tree, expand **Model to learn ER baselines**.</span></span>
3. <span data-ttu-id="353f8-204">Valitse puussa **ER-perusrivien oppimismalli\\ER-perusrivien oppimismuoto**.</span><span class="sxs-lookup"><span data-stu-id="353f8-204">In the tree, select **Model to learn ER baselines\\Format to learn ER baselines**.</span></span>
4. <span data-ttu-id="353f8-205">Valitse **Versiot**-pikavälilehdessä **Suorita**.</span><span class="sxs-lookup"><span data-stu-id="353f8-205">On the **Versions** FastTab select **Run**.</span></span>
5. <span data-ttu-id="353f8-206">Kirjoita **Kirjoita tunnus** -kenttään **1**.</span><span class="sxs-lookup"><span data-stu-id="353f8-206">In the **Enter Id** field, type **1**.</span></span>
6. <span data-ttu-id="353f8-207">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="353f8-207">Select **OK**.</span></span>
7. <span data-ttu-id="353f8-208">Valitse **Organisaation hallinto** \> **Sähköinen raportointi** \> **Määritysten virheenkorjauslokit**.</span><span class="sxs-lookup"><span data-stu-id="353f8-208">Go to **Organization administration** \> **Electronic reporting** \> **Configuration debug logs**.</span></span>

<span data-ttu-id="353f8-209">Suorituslokissa sisältää tietoja luodun tiedoston ja määritetyn perusrivin vertailutuloksista.</span><span class="sxs-lookup"><span data-stu-id="353f8-209">The execution log contains information about the results of the comparison of the generated file with the configured baseline.</span></span> <span data-ttu-id="353f8-210">Loki ilmaisee, että luotu tiedosto ja perusrivi ovat samanlaiset, vaikka suoritetussa muodossa on sidonta, jolla annetaan jatkuvasti muuttuva päivämäärä- ja aika-arvo lähtevässä tiedostossa.</span><span class="sxs-lookup"><span data-stu-id="353f8-210">The log indicates that the generated file and the baseline are equal, even though the executed format contains the binding to enter a constantly changing date and time value in the outbound file.</span></span>

> [!NOTE]
> <span data-ttu-id="353f8-211">Vaikka lähtevä tiedosto on luotu käyttämällä perusriviasetuksia, jotka pakottavat muodon sidosten korvaamisen, korvaamisesta ei saada varoituksia.</span><span class="sxs-lookup"><span data-stu-id="353f8-211">Although the outbound file has been generated by using baseline settings that force the replacement of the format's bindings, you don't receive any warnings about the replacement.</span></span>

## <a name="exchange-baseline-settings-between-environments"></a><span data-ttu-id="353f8-212">Perusriviasetusten vaihtaminen ympäristöjen välillä</span><span class="sxs-lookup"><span data-stu-id="353f8-212">Exchange baseline settings between environments</span></span>

### <a name="export-baseline-settings"></a><span data-ttu-id="353f8-213">Perusriviasetusten vieminen</span><span class="sxs-lookup"><span data-stu-id="353f8-213">Export baseline settings</span></span>

<span data-ttu-id="353f8-214">Uusilla ER-ominaisuuksilla voi viedä valitun ER-muodon perusriviasetukset nykyisestä ympäristöstä ja tallentaa ne XML-tiedostona.</span><span class="sxs-lookup"><span data-stu-id="353f8-214">The new ER capabilities let you export baseline settings for the selected ER format from the current environment and store them as XML files.</span></span> 

<span data-ttu-id="353f8-215">Voit viedä perusriviasetukset valitsemalla **Sähköisen raportointimuotojen perusrivit** -sivulla **Vie**.</span><span class="sxs-lookup"><span data-stu-id="353f8-215">To export baseline settings, on the **Electronic reporting format baselines** page, select **Export**.</span></span>

### <a name="import-baseline-settings"></a><span data-ttu-id="353f8-216">Tuo perustason asetukset</span><span class="sxs-lookup"><span data-stu-id="353f8-216">Import baseline settings</span></span>

<span data-ttu-id="353f8-217">Viedyt perusriviasetukset voidaan viedä toiseen ympäristöön.</span><span class="sxs-lookup"><span data-stu-id="353f8-217">Exported baseline settings can be imported into a different environment.</span></span> <span data-ttu-id="353f8-218">Ympäristö on vietävä ensin ER-muodossa.</span><span class="sxs-lookup"><span data-stu-id="353f8-218">The environment must first be imported as an ER format.</span></span> <span data-ttu-id="353f8-219">Voit sitten viedä perusriviasetukset.</span><span class="sxs-lookup"><span data-stu-id="353f8-219">You can then import the baseline settings.</span></span>

<span data-ttu-id="353f8-220">Voit tuoda perusriviasetukset paikallisesti tallennetusta XML-tiedostosta valitsemalla XML-tiedoston valitsemalla **Sähköisen raportointimuotojen perusrivit** -sivulla ensin **Tuo** ja sitten **Selaa**.</span><span class="sxs-lookup"><span data-stu-id="353f8-220">To import baseline settings from a locally stored XML file, on the **Electronic reporting format baselines** page, select **Import**, and then select **Browse** to select the XML file.</span></span>

<span data-ttu-id="353f8-221">![Tuo perustason asetukset -valintaikkuna](media/GER-BaselineSample-ImportBaseline1.PNG "Näyttökuva Tuo perusriviasetukset -valintaikkunasta")</span><span class="sxs-lookup"><span data-stu-id="353f8-221">![Import baseline settings dialog box](media/GER-BaselineSample-ImportBaseline1.PNG "Screenshot of the Import baseline settings dialog box")</span></span>

<span data-ttu-id="353f8-222">Voit tuoda perusriviasetukset Microsoft SharePoint Serveriin tallennetusta XML-tiedostosta nykyisten tiedoston hallinta-asetusten ja valitun asiakirjatyypin perusteella valitsemalla **Sähköisen raportointimuotojen perusrivit** -sivulla **Tuo lähteestä**.</span><span class="sxs-lookup"><span data-stu-id="353f8-222">To import baseline settings from an XML file that is stored on the Microsoft SharePoint Server, based on the current Document management settings and the selected document type, on the **Electronic reporting format baselines** page, select **Import from source**.</span></span> <span data-ttu-id="353f8-223">Valitse sitten asiakirjatyyppi ja XML-tiedosto.</span><span class="sxs-lookup"><span data-stu-id="353f8-223">Then select the document type and the XML file.</span></span> <span data-ttu-id="353f8-224">SharePoint-kansion käyttämiseen tarvittava asiakirjatyyppi on määritettävä etukäteen.</span><span class="sxs-lookup"><span data-stu-id="353f8-224">The required document type to access the SharePoint folder must be configured in advance.</span></span>

<span data-ttu-id="353f8-225">![Tuo lähteestä -valintaikkuna](media/GER-BaselineSample-ImportBaseline2.PNG "Näyttökuva Tuo lähteestä -valintaikkunasta")</span><span class="sxs-lookup"><span data-stu-id="353f8-225">![Import from source dialog box](media/GER-BaselineSample-ImportBaseline2.PNG "Screenshot of the Import from source dialog box")</span></span>

> [!NOTE]
> <span data-ttu-id="353f8-226">Voit tallentaa pakollisen asiakirjatyypin valintavaiheet tehtävän tallennustoiminnolla ja tiedoston nimen **Tuo lähteestä** -valintaikkunassa.</span><span class="sxs-lookup"><span data-stu-id="353f8-226">You can use Task recorder to record the steps for selecting the required document type and the file name in the **Import from source** dialog box.</span></span> <span data-ttu-id="353f8-227">Tällä tavoin voit pitää pakolliset perusriviasetukset SharePoint Serverissä ja tuoda ne sitten toistamalla tehtävätallenne, kun automatisoituja testejä suoritetaan Regression Suite Automation Tool -työkalulla.</span><span class="sxs-lookup"><span data-stu-id="353f8-227">In this way, you can keep required baseline settings on SharePoint Server and then automatically import them by playing a task recording when you run automated tests by using the Regression Suite Automation Tool.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="353f8-228">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="353f8-228">Additional resources</span></span>

- [<span data-ttu-id="353f8-229">Luotuja raporttitulosten seuraaminen ja vertaaminen perusarvoihin</span><span class="sxs-lookup"><span data-stu-id="353f8-229">Trace generated report results and compare them with baseline values</span></span>](er-trace-reports-compare-baseline.md)
- [<span data-ttu-id="353f8-230">Tehtävän tallennustoiminnon resurssit</span><span class="sxs-lookup"><span data-stu-id="353f8-230">Task recorder resources</span></span>](../user-interface/task-recorder.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
