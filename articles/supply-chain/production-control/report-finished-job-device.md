---
title: Ilmoita valmiiksi työkorttilaitteesta
description: Tässä aiheessa kuvataan, miten järjestelmä konfiguroidaan niin, että työkorttilaitteen käyttäjät voivat raportoida valmiit tuotteet tuotantotilauksesta varastoon.
author: johanhoffmann
manager: tfehr
ms.date: 05/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgRegistrationSetupTouch
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-05-18
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: f5d34893ddc8adc3785ec50dbd72438cf8f68c5d
ms.sourcegitcommit: 52ba8d3e6af72df5dab6c04b9684a61454d353ad
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/26/2020
ms.locfileid: "3403259"
---
# <a name="report-as-finished-from-the-job-card-device"></a><span data-ttu-id="77b40-103">Ilmoita valmiiksi työkorttilaitteesta</span><span class="sxs-lookup"><span data-stu-id="77b40-103">Report as finished from the job card device</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="77b40-104">Työntekijät käyttävät työkorttilaitteen **Raportin edistyminen** -sivua tuotantotyötä varten valmistuneiden määrien raportoinnissa.</span><span class="sxs-lookup"><span data-stu-id="77b40-104">Workers use the **Report progress** page on the job card device to report quantities that have been completed for a production job.</span></span>

## <a name="control-whether-quantities-that-are-reported-as-finished-are-added-to-inventory"></a><span data-ttu-id="77b40-105">Määrittää, lisätäänkö valmiiksi ilmoitetut määrät varastoon</span><span class="sxs-lookup"><span data-stu-id="77b40-105">Control whether quantities that are reported as finished are added to inventory</span></span>

<span data-ttu-id="77b40-106">Seuraavien vaiheiden avulla voit määrittää, lisätäänkö viimeisen työvaiheen valmiiksi ilmoitetut määrät varastoon.</span><span class="sxs-lookup"><span data-stu-id="77b40-106">To control whether and how the quantities that are reported as finished on the last operation should be added to inventory, follow these steps.</span></span>

1. <span data-ttu-id="77b40-107">Valitse **Tuotannonhallinta \> Asetukset \> Tuotannonohjaus \> Tuotantotilauksen oletusarvot**.</span><span class="sxs-lookup"><span data-stu-id="77b40-107">Go to **Product control \> Setup \> Manufacturing execution \> Production order defaults**.</span></span>
1. <span data-ttu-id="77b40-108">Määritä **Ilmoita valmiiksi** -välilehdessä **Päivitä valmis raportti verkossa** -kenttään jokin seuraavista arvoista:</span><span class="sxs-lookup"><span data-stu-id="77b40-108">On the **Report as finished** tab, set the **Update finished report on-line** field to one of the following values:</span></span>

    - <span data-ttu-id="77b40-109">**Ei** – Varastoon ei lisätä määrää, kun viimeisestä työvaiheesta raportoidaan määriä.</span><span class="sxs-lookup"><span data-stu-id="77b40-109">**No** – No quantity will be added to inventory when quantities are reported on the last operation.</span></span> <span data-ttu-id="77b40-110">Tuotantotilauksen tila ei muutu koskaan.</span><span class="sxs-lookup"><span data-stu-id="77b40-110">The status of the production order will never change.</span></span>
    - <span data-ttu-id="77b40-111">**Tila + määrä** – Tuotantotilauksen tilaksi tulee *Ilmoitettu valmiiksi*, ja määrä ilmoitetaan valmiiksi varastoon.</span><span class="sxs-lookup"><span data-stu-id="77b40-111">**Status + Quantity** – The status of the production order will change to *Reported as finished*, and the quantity will be reported as finished to inventory.</span></span>
    - <span data-ttu-id="77b40-112">**Määrä** – Määrän tilaksi tulee Ilmoitettu valmiiksi, mutta tuotantotilauksen tila ei muutu koskaan.</span><span class="sxs-lookup"><span data-stu-id="77b40-112">**Quantity** – The quantity will be reported as finished to inventory, but the status of the production order will never change.</span></span>
    - <span data-ttu-id="77b40-113">**Tila** – Vain tuotantotilauksen tila muuttuu.</span><span class="sxs-lookup"><span data-stu-id="77b40-113">**Status** – Only the status of the production order will change.</span></span> <span data-ttu-id="77b40-114">Varastoon ei lisätä määrää, kun viimeisestä työvaiheesta raportoidaan määriä.</span><span class="sxs-lookup"><span data-stu-id="77b40-114">No quantities will be added to inventory when quantities are reported on the last operation.</span></span>

> [!NOTE]
> <span data-ttu-id="77b40-115">Määriä ei seurata varastossa, jos ne työvaiheet, jotka ne on ilmoitettu valmiiksi, eivät ole määritelleet viimeistä työvaihetta.</span><span class="sxs-lookup"><span data-stu-id="77b40-115">Quantities aren't tracked in inventory if the operations that they are reported as finished on aren't defined as the last operation.</span></span> <span data-ttu-id="77b40-116">Näitä määriä voidaan kuitenkin käyttää edistymisen tarkastelemiseen.</span><span class="sxs-lookup"><span data-stu-id="77b40-116">However, those quantities can be used to view progress.</span></span> <span data-ttu-id="77b40-117">Ne voidaan myös sisällyttää sääntöihin, joissa määritetään, voivatko työntekijät aloittaa seuraavan työvaiheen, ennen kuin edellisessä työvaiheessa määritetty ilmoitettu määräraja saavutetaan.</span><span class="sxs-lookup"><span data-stu-id="77b40-117">They can also be included in rules that control whether workers can start the next operation before a defined threshold of reported quantities on the previous operation is reached.</span></span> <span data-ttu-id="77b40-118">Voit määrittää nämä säännöt **Tuotantotilauksen oletukset** -sivun **Määrän oikeellisuustarkistus** -välilehdessä.</span><span class="sxs-lookup"><span data-stu-id="77b40-118">You can define these rules on the **Quantity validation** tab of the **Production order defaults** page.</span></span>

<span data-ttu-id="77b40-119">Lisätietoja **Tuotantotilauksen oletukset** -sivun käyttämisestä on kohdassa [Tuotantoparametrit tuotannon suorituksessa](production-parameters-manufacturing-execution.md).</span><span class="sxs-lookup"><span data-stu-id="77b40-119">For more information about how to work with the **Production order defaults** page, see [Production parameters in Manufacturing execution](production-parameters-manufacturing-execution.md).</span></span>

## <a name="report-batch-controlled-items-as-finished"></a><span data-ttu-id="77b40-120">Eräohjattujen nimikkeiden ilmoittaminen valmiiksi</span><span class="sxs-lookup"><span data-stu-id="77b40-120">Report batch-controlled items as finished</span></span>

<span data-ttu-id="77b40-121">Työkorttilaite tukee kolmea eränimikkeiden raportointiskenaariota.</span><span class="sxs-lookup"><span data-stu-id="77b40-121">The job card device supports three scenarios for reporting on batch items.</span></span> <span data-ttu-id="77b40-122">Nämä skenaariot koskevat sekä nimikkeitä, jotka on otettu käyttöön lisävarastoprosesseja varten, että nimikkeitä, jotka eivät ole käytössä lisävarastoprosesseissa.</span><span class="sxs-lookup"><span data-stu-id="77b40-122">These scenarios apply both to items that are enabled for advanced warehouse processes and to items that aren't enabled for advanced warehouse processes.</span></span>

- <span data-ttu-id="77b40-123">**Manuaalisesti määritellyt eränumerot:** Työntekijät voivat määrittää mukautetun eränumeron.</span><span class="sxs-lookup"><span data-stu-id="77b40-123">**Manually assigned batch numbers:** Workers enter a custom batch number.</span></span> <span data-ttu-id="77b40-124">Tämä eränumero voi olla peräisin ulkoisesta lähteestä, jota järjestelmä ei tunne.</span><span class="sxs-lookup"><span data-stu-id="77b40-124">This batch number might come from an external source that isn't known to the system.</span></span>
- <span data-ttu-id="77b40-125">**Ennalta määritetyt eränumerot:** Työntekijät valitsevat eränumeron niiden eränumeroiden luettelosta, jotka järjestelmä luo automaattisesti, ennen kuin tuotantotilaus vapautetaan työkorttilaitteeseen.</span><span class="sxs-lookup"><span data-stu-id="77b40-125">**Predefined batch numbers:** Workers select a batch number in a list of batch numbers that the system automatically generates before the production order is released to the job card device.</span></span>
- <span data-ttu-id="77b40-126">**Kiinteät eränumerot:** Työntekijät eivät voi syöttää tai valita eränumeroa.</span><span class="sxs-lookup"><span data-stu-id="77b40-126">**Fixed batch numbers:** Workers don't enter or select a batch number.</span></span> <span data-ttu-id="77b40-127">Sen sijaan järjestelmä liittää tuotantotilaukseen automaattisesti eränumeron ennen kuin se on vapautettu.</span><span class="sxs-lookup"><span data-stu-id="77b40-127">Instead, the system automatically assigns a batch number to the production order before it's released.</span></span>

<span data-ttu-id="77b40-128">Kukin skenaario otetaan käyttöön seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="77b40-128">To enable each scenario, follow these steps.</span></span>

1. <span data-ttu-id="77b40-129">Mene **Tuotetietojen hallinta \> Tuotteet \> Vapautetut tuotteet**.</span><span class="sxs-lookup"><span data-stu-id="77b40-129">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="77b40-130">Valitse määritettävä tuote.</span><span class="sxs-lookup"><span data-stu-id="77b40-130">Select the product to configure.</span></span>
1. <span data-ttu-id="77b40-131">Valitse **Hallitse varastoa** -pikavälilehden **Eränumeroryhmä**-kentässä skenaarion tueksi määritetty seurantanumeroryhmä.</span><span class="sxs-lookup"><span data-stu-id="77b40-131">On the **Manage inventory** FastTab, in the **Batch number group** field, select the tracking number group that is set up to support your scenario.</span></span>

> [!NOTE]
> <span data-ttu-id="77b40-132">Jos eräohjattavia tuotteita varten ei ole määritetty eränumeroryhmää, työkorttilaite antaa eränumerolle manuaalisen merkinnän valmiiksi ilmoittamisen aikana.</span><span class="sxs-lookup"><span data-stu-id="77b40-132">By default, if no batch number group is assigned to a batch-controlled product, the job card device provides manual entry for the batch number during reporting as finished.</span></span>

<span data-ttu-id="77b40-133">Seuraavissa jaksoissa kuvataan, miten seurantanumeroryhmiä määritetään tukemaan kolmea eränimikkeiden raportointiskenaariota.</span><span class="sxs-lookup"><span data-stu-id="77b40-133">The following subsections describe how to set up tracking number groups to support each of the three scenarios for reporting on batch items.</span></span>

### <a name="enable-batch-number-reporting-on-the-job-card-device"></a><span data-ttu-id="77b40-134">Ota eränumeroiden raportointi käyttöön työkorttilaitteessa</span><span class="sxs-lookup"><span data-stu-id="77b40-134">Enable batch number reporting on the job card device</span></span>

<span data-ttu-id="77b40-135">Jos haluat, että työkorttilaitteet hyväksyvät eränumeron valmiiksi ilmoittamisen aikana, sinun on otettava seuraavat ominaisuudet käyttöön (tässä järjestyksessä) [ominaisuuksien hallinnan](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) avulla:</span><span class="sxs-lookup"><span data-stu-id="77b40-135">To enable your job card devices to accept a batch number during reporting as finished, you must use [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) to turn on the following features (in this order):</span></span>

1. <span data-ttu-id="77b40-136">Parannettu Raportointi on meneillään -valintaikkunan käyttäjäkokemus työkorttilaitteessa</span><span class="sxs-lookup"><span data-stu-id="77b40-136">Improved user experience for the Report progress dialog in the Job Card Device</span></span>
1. <span data-ttu-id="77b40-137">Ota erä- ja sarjanumeroiden antaminen käyttöön, kun valmistuminen ilmoitetaan työkorttilaitteesta (esiversio)</span><span class="sxs-lookup"><span data-stu-id="77b40-137">Enable to enter batch and serial numbers while reporting as finished from the Job Card Device (Preview)</span></span>

### <a name="set-up-a-tracking-number-group-that-lets-workers-manually-assign-a-batch-number"></a><span data-ttu-id="77b40-138">Määritä seurantanumeroryhmä, jonka avulla työntekijät määrittävät eränumeron manuaalisesti</span><span class="sxs-lookup"><span data-stu-id="77b40-138">Set up a tracking number group that lets workers manually assign a batch number</span></span>

<span data-ttu-id="77b40-139">Voit sallia manuaalisesti määritetyt eränumerot asettamalla seuraavien vaiheiden ryhmän seuraavien ohjeiden mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="77b40-139">To allow for manually assigned batch numbers, follow these steps to set up a tracking number group.</span></span>

1. <span data-ttu-id="77b40-140">Siirry kohtaan **Varaston hallinta \> Asetukset \> Dimensiot \> Seurantanumeroryhmät**.</span><span class="sxs-lookup"><span data-stu-id="77b40-140">Go to **Inventory management \> Setup \> Dimensions \> Tracking number groups**.</span></span>
1. <span data-ttu-id="77b40-141">Luo tai valitse määritettävä seurantanumeroryhmä.</span><span class="sxs-lookup"><span data-stu-id="77b40-141">Create or select the tracking number group to set up.</span></span>
1. <span data-ttu-id="77b40-142">Määritä **Yleinen**-pikavälilehden **Manuaalinen**-asetukseksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="77b40-142">On the **General** FastTab, set the **Manual** option to **Yes**.</span></span>

    <span data-ttu-id="77b40-143">![Seurantanumeroryhmät -sivu](media/tracking-number-group-manual.png "Seurantanumeroryhmät -sivu")</span><span class="sxs-lookup"><span data-stu-id="77b40-143">![Tracking number groups page](media/tracking-number-group-manual.png "Tracking number groups page")</span></span>

1. <span data-ttu-id="77b40-144">Määritä muut arvot tarpeen mukaan ja valitse sitten tämä seurantanumeroryhmä vapautettujen tuotteiden eränumeroksi, jota varten haluat käyttää tätä skenaariota.</span><span class="sxs-lookup"><span data-stu-id="77b40-144">Set other values as you require, and then select this tracking number group as the batch number group for released products that you want to use this scenario for.</span></span>

<span data-ttu-id="77b40-145">Kun käytät tätä skenaariota, työkorttilaitteen **Raportin edistyminen** -sivun **Eränumero**-kenttä on tekstiruutu, jossa työntekijät voivat syöttää minkä tahansa arvon.</span><span class="sxs-lookup"><span data-stu-id="77b40-145">When you use this scenario, the **Batch number** field that the **Report progress** page on the job card device provides is a text box where workers can enter any value.</span></span>

<span data-ttu-id="77b40-146">![Raportin edistymissivu, jossa on kenttä manuaalisia eränumeroita varten](media/job-card-device-batch-manual.png "Raportin edistymissivu, jossa on kenttä manuaalisia eränumeroita varten")</span><span class="sxs-lookup"><span data-stu-id="77b40-146">![Report progress page with a field for manual batch numbers](media/job-card-device-batch-manual.png "Report progress page with a field for manual batch numbers")</span></span>

### <a name="set-up-a-tracking-number-group-that-provides-a-list-of-predefined-batch-numbers"></a><span data-ttu-id="77b40-147">Määritä seurantanumeroryhmä, joka sisältää luettelon esimääritetyistä eränumeroista</span><span class="sxs-lookup"><span data-stu-id="77b40-147">Set up a tracking number group that provides a list of predefined batch numbers</span></span>

<span data-ttu-id="77b40-148">Voit tarjota luettelon esimääritetyistä eränumeroista asettamalla seuraavien vaiheiden ryhmän seuraavien ohjeiden mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="77b40-148">To provide a list of predefined batch numbers, follow these steps to set up a tracking number group.</span></span>

1. <span data-ttu-id="77b40-149">Siirry kohtaan **Varaston hallinta \> Asetukset > Dimensiot \> Seurantanumeroryhmät**.</span><span class="sxs-lookup"><span data-stu-id="77b40-149">Go to **Inventory management \> Setup > Dimensions \> Tracking number groups**.</span></span>
1. <span data-ttu-id="77b40-150">Luo tai valitse määritettävä seurantanumeroryhmä.</span><span class="sxs-lookup"><span data-stu-id="77b40-150">Create or select the tracking number group to set up.</span></span>
1. <span data-ttu-id="77b40-151">Määritä **Yleinen**-pikavälilehden **Vain varastotransaktioille** -asetukseksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="77b40-151">On the **General** FastTab, set the **Only for inventory transactions** option to **Yes**.</span></span>
1. <span data-ttu-id="77b40-152">Käytä **per määrä** -kenttää, kun haluat jakaa eränumerot määrää kohden määrittämäsi arvon perusteella.</span><span class="sxs-lookup"><span data-stu-id="77b40-152">Use the **Per qty.** field to split batch numbers per quantity, based on the value that you enter.</span></span> <span data-ttu-id="77b40-153">Esimerkiksi tuotantotilaus on kymmenen kappaletta ja **per määrä** -kentän arvoksi on määritetty *2*.</span><span class="sxs-lookup"><span data-stu-id="77b40-153">For example, you have a production order for ten pieces, and the **Per qty.** field is set to *2*.</span></span> <span data-ttu-id="77b40-154">Tässä tapauksessa tuotantotilaukseen liitetään viisi eränumeroa, kun se luodaan.</span><span class="sxs-lookup"><span data-stu-id="77b40-154">In this case, five batch numbers will be assigned to the production order when it's created.</span></span>

    <span data-ttu-id="77b40-155">![Seurantanumeroryhmät -sivu](media/tracking-number-group-predefined.png "Seurantanumeroryhmät -sivu")</span><span class="sxs-lookup"><span data-stu-id="77b40-155">![Tracking number groups page](media/tracking-number-group-predefined.png "The Tracking number groups page")</span></span>

1. <span data-ttu-id="77b40-156">Määritä muut arvot tarpeen mukaan ja valitse sitten tämä seurantanumeroryhmä vapautettujen tuotteiden eränumeroksi, jota varten haluat käyttää tätä skenaariota.</span><span class="sxs-lookup"><span data-stu-id="77b40-156">Set other values as you require, and then select this tracking number group as the batch number group for released products that you want to use this scenario for.</span></span>

<span data-ttu-id="77b40-157">Kun käytät tätä skenaariota, työkorttilaitteen **Raportin edistyminen** -sivun **Eränumero**-kenttä on pudotusvalikko, josta työntekijöiden tulee valita esimääritetty arvo.</span><span class="sxs-lookup"><span data-stu-id="77b40-157">When you use this scenario, the **Batch number** field that the **Report progress** page on the job card device provides is a drop-down list where workers must select a predefined value.</span></span>

<span data-ttu-id="77b40-158">![Raportin edistymissivu, jossa on luettelo esimääritettyjä eränumeroita varten](media/job-card-device-batch-predefined.png "Raportin edistymissivu, jossa on luettelo esimääritettyjä eränumeroita varten")</span><span class="sxs-lookup"><span data-stu-id="77b40-158">![Report progress page with a list of predefined batch numbers](media/job-card-device-batch-predefined.png "Report progress page with a list of predefined batch numbers")</span></span>

### <a name="set-up-a-tracking-number-group-that-automatically-assigns-batch-numbers"></a><span data-ttu-id="77b40-159">Määritä seurantanumeroryhmä, joka automaattisesti määrittää eränumerot</span><span class="sxs-lookup"><span data-stu-id="77b40-159">Set up a tracking number group that automatically assigns batch numbers</span></span>

<span data-ttu-id="77b40-160">Jos eränumerot määritetään automaattisesti ilman työntekijän syöttöä, määritä seurantanumeroryhmä noudattamalla näitä ohjeita.</span><span class="sxs-lookup"><span data-stu-id="77b40-160">If batch numbers should be assigned automatically, without worker input, follow these steps to set up a tracking number group.</span></span>

1. <span data-ttu-id="77b40-161">Siirry kohtaan **Varaston hallinta \> Asetukset \> Dimensiot \> Seurantanumeroryhmät**.</span><span class="sxs-lookup"><span data-stu-id="77b40-161">Go to **Inventory management \> Setup \> Dimensions \> Tracking number groups**.</span></span>
1. <span data-ttu-id="77b40-162">Luo tai valitse määritettävä seurantanumeroryhmä.</span><span class="sxs-lookup"><span data-stu-id="77b40-162">Create or select the tracking number group to set up.</span></span>
1. <span data-ttu-id="77b40-163">Määritä **Yleinen**-pikavälilehden **Vain varastotransaktioille** -asetukseksi **Ei**.</span><span class="sxs-lookup"><span data-stu-id="77b40-163">On the **General** FastTab, set the **Only for inventory transactions** option to **No**.</span></span>
1. <span data-ttu-id="77b40-164">Määritä kohdan **Manuaalinen** asetukseksi **Ei**.</span><span class="sxs-lookup"><span data-stu-id="77b40-164">Set the **Manual** option to **No**.</span></span>

    <span data-ttu-id="77b40-165">![Seurantanumeroryhmät -sivu](media/tracking-number-group-fixed.png "Seurantanumeroryhmät -sivu")</span><span class="sxs-lookup"><span data-stu-id="77b40-165">![Tracking number groups page](media/tracking-number-group-fixed.png "Tracking number groups page")</span></span>

1. <span data-ttu-id="77b40-166">Määritä muut arvot tarpeen mukaan ja valitse sitten tämä seurantanumeroryhmä vapautettujen tuotteiden eränumeroksi, jota varten haluat käyttää tätä skenaariota.</span><span class="sxs-lookup"><span data-stu-id="77b40-166">Set other values as you require, and then select this tracking number group as the batch number group for released products that you want to use this scenario for.</span></span>

<span data-ttu-id="77b40-167">Kun käytät tätä skenaariota, työkorttilaitteen **Raportin edistyminen** -sivun **Eränumero**-kenttä näyttää arvon, mutta työntekijät eivät voi muokata sitä.</span><span class="sxs-lookup"><span data-stu-id="77b40-167">When you use this scenario, the **Batch number** field that the **Report progress** page on the job card device provides shows a value, but workers can't edit it.</span></span>

<span data-ttu-id="77b40-168">![Raportin edistymissivu, jossa on kiinteä eränumero](media/job-card-device-batch-fixed.png "Raportin edistymissivu, jossa on kiinteä eränumero")</span><span class="sxs-lookup"><span data-stu-id="77b40-168">![Report progress page with a fixed batch number](media/job-card-device-batch-fixed.png "Report progress page with a fixed batch number")</span></span>

## <a name="report-as-finished-to-a-license-plate"></a><span data-ttu-id="77b40-169">Ilmoita valmistuneeksi rekisterikilpeen</span><span class="sxs-lookup"><span data-stu-id="77b40-169">Report as finished to a license plate</span></span>

<span data-ttu-id="77b40-170">Lisävarastoprosessit voivat käyttää käyttöoikeuskilpi-dimensiota tähän tarkoitukseen määritettyjen varastosijaintien varastonseurantaan.</span><span class="sxs-lookup"><span data-stu-id="77b40-170">Advanced warehouse processes can use the license plate dimension to track inventory on warehouse locations that have been set up for this purpose.</span></span> <span data-ttu-id="77b40-171">Tässä tapauksessa rekisterinumero on pakollinen, kun työntekijä ilmoittaa määrät valmiiksi.</span><span class="sxs-lookup"><span data-stu-id="77b40-171">In this case, the license plate number is required when a worker reports quantities as finished.</span></span>

### <a name="enable-license-plate-reporting-and-label-printing"></a><span data-ttu-id="77b40-172">Rekisterikilven raportoinnin ja etiketin tulostuksen ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="77b40-172">Enable license plate reporting and label printing</span></span>

<span data-ttu-id="77b40-173">Tässä osassa kuvattujen toimintojen käyttäminen edellyttää, että otat seuraavat ominaisuudet käyttöön [ominaisuuksien hallinnan](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) avulla (tässä järjestyksessä):</span><span class="sxs-lookup"><span data-stu-id="77b40-173">To use the features that are described in this section, you must use [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) to turn on the following features (in this order):</span></span>

1. <span data-ttu-id="77b40-174">Rekisterikilpi valmiiksi raportointia varten on lisätty työkorttilaitteeseen</span><span class="sxs-lookup"><span data-stu-id="77b40-174">License plate for reporting as finished added to the Job Card Device</span></span>
1. <span data-ttu-id="77b40-175">Ota käyttöön rekisterikilven numeron automaattinen luonti, kun työkorttilaitteessa raportoidaan valmiiksi</span><span class="sxs-lookup"><span data-stu-id="77b40-175">Enable automatic generation of license plate number when reporting as finished in the job card device</span></span>
1. <span data-ttu-id="77b40-176">Tulosta etiketti työkorttilaitteesta</span><span class="sxs-lookup"><span data-stu-id="77b40-176">Print label from Job Card Device</span></span>

### <a name="set-up-reporting-as-finished-to-a-license-plate"></a><span data-ttu-id="77b40-177">Aseta raportointi valmistuneeksi rekisterikilpeen</span><span class="sxs-lookup"><span data-stu-id="77b40-177">Set up reporting as finished to a license plate</span></span>

<span data-ttu-id="77b40-178">Noudattamalla seuraavia ohjeita voit määrittää, pitääkö työntekijöiden käyttää uudelleen aiemmin luotua rekisterikilpeä vai luoda uusi rekisterikilpi, kun he raportoivat määrät valmiiksi.</span><span class="sxs-lookup"><span data-stu-id="77b40-178">To control whether workers should reuse an existing license plate or generate a new license plate when they report quantities as finished, follow these steps.</span></span>

1. <span data-ttu-id="77b40-179">Valitse **Tuotannonhallinta \> Asetukset \> Tuotannonohjaus \> Konfiguroi työkortti laitteita varten**.</span><span class="sxs-lookup"><span data-stu-id="77b40-179">Go to **Production control \> Setup \> Manufacturing execution \> Configure job card for devices**.</span></span>
2. <span data-ttu-id="77b40-180">Aseta seuraavat asetukset kullekin laitteelle:</span><span class="sxs-lookup"><span data-stu-id="77b40-180">Set the following options for each device:</span></span>

    - <span data-ttu-id="77b40-181">**Luo rekisterikilpi** – Määritä tämän asetuksen arvoksi **Kyllä**, jos haluat luoda uuden rekisterikilven kullekin valmistuneelle raportille.</span><span class="sxs-lookup"><span data-stu-id="77b40-181">**Generate license plate** – Set this option to **Yes** to generate a new license plate for each report as finished.</span></span> <span data-ttu-id="77b40-182">Aseta arvoksi **Ei**, jos aiemmin luotua rekisterikilpeä käytetään jokaisen valmiiksi määritetyn raportin yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="77b40-182">Set it to **No** if an existing license plate should be used for each report as finished.</span></span>
    - <span data-ttu-id="77b40-183">**Tulosta etiketti** – Määritä tämän asetuksen arvoksi **Kyllä**, jos työntekijän tulee tulostaa käyttöoikeuskilven otsikon kullekin valmiille raportille.</span><span class="sxs-lookup"><span data-stu-id="77b40-183">**Print label** – Set this option to **Yes** if the worker must print a license plate label for each report as finished.</span></span> <span data-ttu-id="77b40-184">Määritä arvoksi **Ei**, jos etikettiä ei tarvita.</span><span class="sxs-lookup"><span data-stu-id="77b40-184">Set it to **No** if no label is required.</span></span> 

<span data-ttu-id="77b40-185">![Konfiguroi työkortti laitteita varten -sivu](media/config-job-card-raf.png "Konfiguroi työkortti laitteita varten -sivu")</span><span class="sxs-lookup"><span data-stu-id="77b40-185">![Configure job card for devices page](media/config-job-card-raf.png "Configure job card for devices page")</span></span>

> [!NOTE]
> <span data-ttu-id="77b40-186">Määrittääksesi etiketin, siirry kohtaan **Varastonhallinta \> Asetukset \> Asiakirjan reititys \> Asiakirjan reititysasettelut**.</span><span class="sxs-lookup"><span data-stu-id="77b40-186">To configure the label, go to **Warehouse management \> Setup \> Document routing \> Document routing**.</span></span> <span data-ttu-id="77b40-187">Lisätietoja on kohdassa [Rekisterikilven tarratulostuksen ottaminen käyttöön](../warehousing/tasks/license-plate-label-printing.md).</span><span class="sxs-lookup"><span data-stu-id="77b40-187">For more information, see [Enable license plate label printing](../warehousing/tasks/license-plate-label-printing.md).</span></span>
