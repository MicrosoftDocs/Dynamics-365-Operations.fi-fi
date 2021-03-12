---
title: Työn jako
description: Tässä aiheessa on tietoja työn jakotoiminnosta. Tällä toiminnolla voidaan jakaa suuret työtilaukset useiksi pieniksi työtilauksiksi, jotka voidaan sitten määrittää useille varastotyöntekijöille. Tällä tavoin useat varastotyöntekijät voivat keräillä samaa työtä samanaikaisesti.
author: mirzaab
manager: tfehr
ms.date: 10/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: WHSWorkTableListPage
ms.author: mirzaab
ms.search.validFrom: 2020-10-15
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 8a530f3887c3c66295177d480a8c486dd0984153
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4965524"
---
# <a name="work-split"></a><span data-ttu-id="66956-105">Työn jako</span><span class="sxs-lookup"><span data-stu-id="66956-105">Work split</span></span>

<span data-ttu-id="66956-106">Työnjakotoiminnolla voidaan jakaa suuret työtunnukset (eli useita rivejä sisältävät työtilaukset) useiksi pieniksi työtunnuksiksi, jotka voidaan sitten määrittää useille varastotyöntekijöille.</span><span class="sxs-lookup"><span data-stu-id="66956-106">Work split functionality lets you split large work IDs (that is, work orders that have several lines) into several smaller work IDs that you can then assign to multiple warehouse workers.</span></span> <span data-ttu-id="66956-107">Tällä tavoin useat varastotyöntekijät voivat keräillä samaa työn luontinumeroa samanaikaisesti.</span><span class="sxs-lookup"><span data-stu-id="66956-107">In this way, the same work creation number can be picked simultaneously by several warehouse workers.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="66956-108">Vain sellaiset työtilaukset, joiden tila on *Avoin* tai *Käsittelyssä*, voidaan jakaa.</span><span class="sxs-lookup"><span data-stu-id="66956-108">You can split only work orders that have a status of *Open* or *In-progress*.</span></span>

## <a name="turn-on-the-work-split-functionality"></a><span data-ttu-id="66956-109">Työn jakotoiminnon ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="66956-109">Turn on the work split functionality</span></span>

<span data-ttu-id="66956-110">Ennen kuin työn jakotoimintoa voidaan käyttää, se ja sen edellytyksenä oleva toiminto on otettava käyttöön.</span><span class="sxs-lookup"><span data-stu-id="66956-110">Before you can use the work split functionality, you must turn on the feature and its prerequisite feature in your system.</span></span> <span data-ttu-id="66956-111">Järjestelmänvalvojat voivat tarkistaa [ominaisuuksien hallinnan](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) asetuksissa toimintojen tilan ja ottaa ne tarvittaessa käyttöön.</span><span class="sxs-lookup"><span data-stu-id="66956-111">Administrators can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the features and turn them on as required.</span></span>

<span data-ttu-id="66956-112">Jos edellytyksenä oleva *Organisaation laajuinen työn esto* -toiminto ei ole vielä käytössä, se on otettava käyttöön.</span><span class="sxs-lookup"><span data-stu-id="66956-112">First, turn on the prerequisite *Organization-wide work blocking* feature if it isn't already turned on.</span></span> <span data-ttu-id="66956-113">**Ominaisuuksien hallinta** -työtilassa tämä ominaisuus on luetteloitu seuraavalla tavalla:</span><span class="sxs-lookup"><span data-stu-id="66956-113">In the **Feature management** workspace, this feature is listed in the following way:</span></span>

- <span data-ttu-id="66956-114">**Moduuli:** *Varastonhallinta*</span><span class="sxs-lookup"><span data-stu-id="66956-114">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="66956-115">**Toiminnon nimi:** *Organisaation laajuinen työn esto*</span><span class="sxs-lookup"><span data-stu-id="66956-115">**Feature name:** *Organization-wide work blocking*</span></span>

> [!NOTE]
> <span data-ttu-id="66956-116">Kun tämä toiminto on aktivoitu, tietojen päivitys tapahtuu automaattisesti, kun toiminto on otettu käyttöön kaikissa yrityksissä.</span><span class="sxs-lookup"><span data-stu-id="66956-116">When this feature is activated, a data upgrade is automatically applied after the feature is turned on across all legal entities.</span></span>

<span data-ttu-id="66956-117">Ota seuraavaksi *Työn jako* -toiminto, joka ilmaistaan seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="66956-117">Next, turn on the *Work split* feature, which is listed in the following way:</span></span>

- <span data-ttu-id="66956-118">**Moduuli:** *Varastonhallinta*</span><span class="sxs-lookup"><span data-stu-id="66956-118">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="66956-119">**Toiminnon jako:** *Työn jako*</span><span class="sxs-lookup"><span data-stu-id="66956-119">**Feature name:** *Work split*</span></span>

## <a name="enhancements-to-the-work-details-and-all-work-pages"></a><span data-ttu-id="66956-120">Työn tiedot- ja Kaikki työt -sivujen laajennukset</span><span class="sxs-lookup"><span data-stu-id="66956-120">Enhancements to the Work details and All work pages</span></span>

<span data-ttu-id="66956-121">*Työn jako* -toiminto lisää seuraavat kaksi painiketta **Työn tiedot**- ja **Kaikki työt** -sivujen toimintoruudun **Työ**-välilehteen:</span><span class="sxs-lookup"><span data-stu-id="66956-121">The *Work split* feature adds the following two buttons to the **Work** tab on the Action Pane of the **Work details** and **All work** pages:</span></span>

- <span data-ttu-id="66956-122">**Jaa työ** – jaa nykyinen työtunnus useiksi pieniksi työtunnuksiksi, joita eri työntekijät voivat käsitellä.</span><span class="sxs-lookup"><span data-stu-id="66956-122">**Split work** – Split the current work ID into multiple smaller work IDs that can be processed by separate workers.</span></span>
- <span data-ttu-id="66956-123">**Peruuta työn jakoistunto** – peruuta työn jakoistunto ja anna mahdollisuus työn käsittelyyn.</span><span class="sxs-lookup"><span data-stu-id="66956-123">**Cancel work split session** – Cancel the work split session, and make the work available for processing.</span></span>

<span data-ttu-id="66956-124">![Jaa työ- ja Peruuta työn jakoistunto -painikkeet](media/Work_split_buttons.png "Jaa työ- ja Peruuta työn jakoistunto -painikkeet")</span><span class="sxs-lookup"><span data-stu-id="66956-124">![Split work and Cancel work split session buttons](media/Work_split_buttons.png "Split work and Cancel work split session buttons")</span></span>

> [!IMPORTANT]
> <span data-ttu-id="66956-125">**Jaa työ** -painike ei ole käytettävissä, jos jokin seuraavista ehdoista toteutuu.</span><span class="sxs-lookup"><span data-stu-id="66956-125">The **Split work** button won't be available if any of the following conditions are met:</span></span>
>
> - <span data-ttu-id="66956-126">Työn tila on jokin muu kuin *Avoin* tai *Käsittelyssä*.</span><span class="sxs-lookup"><span data-stu-id="66956-126">The work status is something other than *Open* or *In progress*.</span></span>
> - <span data-ttu-id="66956-127">Konttitunnus on liitetty työtunnukseen.</span><span class="sxs-lookup"><span data-stu-id="66956-127">A container ID is associated with the work ID.</span></span> <span data-ttu-id="66956-128">(Konttia ei voi jakaa järjestelmässä, sillä se edellyttää fyysisiä toimia.)</span><span class="sxs-lookup"><span data-stu-id="66956-128">(A container can't be systematically split, because it requires physical actions.)</span></span>
> - <span data-ttu-id="66956-129">Työ on liitetty klusteriin.</span><span class="sxs-lookup"><span data-stu-id="66956-129">The work is associated with a cluster.</span></span>
> - <span data-ttu-id="66956-130">Työtilauksen tyyppi ei ole jokin seuraavista:</span><span class="sxs-lookup"><span data-stu-id="66956-130">The work order type is something other than one of the following types:</span></span>
>
>    - <span data-ttu-id="66956-131">Myyntitilaukset</span><span class="sxs-lookup"><span data-stu-id="66956-131">Sales orders</span></span>
>    - <span data-ttu-id="66956-132">Raaka-aineiden keräily</span><span class="sxs-lookup"><span data-stu-id="66956-132">Raw material picking</span></span>
>    - <span data-ttu-id="66956-133">Siirtovarasto-otto</span><span class="sxs-lookup"><span data-stu-id="66956-133">Transfer issue</span></span>
>
> - <span data-ttu-id="66956-134">Toinen käyttäjä jakaa parhaillaan työtä.</span><span class="sxs-lookup"><span data-stu-id="66956-134">The work is currently being split by another user.</span></span> <span data-ttu-id="66956-135">Jos yrität avata sellaisen työn jakosivun, jota toinen käyttäjä jo jakaa, seuraava virhesanoma avautuu: Työtä, jonka tunnus on \#\#\#\#, jaetaan parhaillaan.</span><span class="sxs-lookup"><span data-stu-id="66956-135">If you try to open the splitting page for work that is already being split by another user, you receive the following error message: "The work with ID \#\#\#\# is currently being split.</span></span> <span data-ttu-id="66956-136">Yritä uudelleen muutaman minuutin kuluttua.</span><span class="sxs-lookup"><span data-stu-id="66956-136">Retry in a few minutes.</span></span> <span data-ttu-id="66956-137">Jos näet tämän sanoman uudelleen, ota yhteys työnjohtajaan.</span><span class="sxs-lookup"><span data-stu-id="66956-137">If you continue to receive this message, contact a supervisor."</span></span>

<span data-ttu-id="66956-138">Uusi työn estosyy, *Jaa työ*, ilmaisee, kun työtunnusta ollaan jakamassa.</span><span class="sxs-lookup"><span data-stu-id="66956-138">A new work blocking reason, *Split work*, indicates when the work ID is in the process of being split.</span></span> <span data-ttu-id="66956-139">Se näkyy sekä **Jaa työt** -sivulla että varastosovelluksessa, jos käyttäjä yrittää suorittaa työn.</span><span class="sxs-lookup"><span data-stu-id="66956-139">It's shown both on the **Split work** page and in the warehouse app if a user tries to run the work.</span></span> <span data-ttu-id="66956-140">Jos eston syitä käytetään, työtunnuksen **Estetty aalto** -kentän arvoksi vaihtuu **Estetty**.</span><span class="sxs-lookup"><span data-stu-id="66956-140">When blocking reasons are used, the name of the **Blocked wave** field from the work ID is changed to **Blocked**.</span></span>

## <a name="initiate-a-work-split"></a><span data-ttu-id="66956-141">Työn jaon aloittaminen</span><span class="sxs-lookup"><span data-stu-id="66956-141">Initiate a work split</span></span>

<span data-ttu-id="66956-142">Toiminto lisää uuden **Jaa työ** -sivun, jossa käyttäjät voivat jakaa työtunnuksen työrivejä.</span><span class="sxs-lookup"><span data-stu-id="66956-142">The feature adds a new **Split work** page that lets users split work lines from the work ID.</span></span> <span data-ttu-id="66956-143">Kun sivu avataan ensimmäisen kerran, siinä on näkyvissä rivit, joiden työn tila on *Avoin* ja jotka ovat jaettavissa.</span><span class="sxs-lookup"><span data-stu-id="66956-143">When the page is first opened, it shows lines that have a work status of *Open* and that are available to be split.</span></span> <span data-ttu-id="66956-144">Käsittele valittu työ valitsemalla toimintoruudussa **Jaa työ**.</span><span class="sxs-lookup"><span data-stu-id="66956-144">On the Action Pane, select **Split work** to process the selected work.</span></span>

<span data-ttu-id="66956-145">Työ jaetaan seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="66956-145">To split work, follow these steps.</span></span>

1. <span data-ttu-id="66956-146">Avaa jokin seuraavista työsivuista:</span><span class="sxs-lookup"><span data-stu-id="66956-146">Open one of the following work pages:</span></span>

    - <span data-ttu-id="66956-147">**Työn tiedot** (**Varastonhallinta \> Työ \> Työn tiedot**)</span><span class="sxs-lookup"><span data-stu-id="66956-147">**Work details** (**Warehouse management \> Work \> Work details**)</span></span>
    - <span data-ttu-id="66956-148">**Kaikki työt** (**Varastonhallinta \> Työ \> Kaikki työt**)</span><span class="sxs-lookup"><span data-stu-id="66956-148">**All work** (**Warehouse management \> Work \> All work**)</span></span>

1. <span data-ttu-id="66956-149">Valitse ruudukossa jaettava työtunnus.</span><span class="sxs-lookup"><span data-stu-id="66956-149">In the grid, select a work ID to split.</span></span> <span data-ttu-id="66956-150">**Työtilaustyyppi**-kentän arvoksi on määritettävä jokin seuraavista arvoista:</span><span class="sxs-lookup"><span data-stu-id="66956-150">The **Work order type** field must be set to one of the following values:</span></span>

    - <span data-ttu-id="66956-151">Myyntitilaukset</span><span class="sxs-lookup"><span data-stu-id="66956-151">Sales orders</span></span>
    - <span data-ttu-id="66956-152">Raaka-aineiden keräily</span><span class="sxs-lookup"><span data-stu-id="66956-152">Raw material picking</span></span>
    - <span data-ttu-id="66956-153">Siirtovarasto-otto</span><span class="sxs-lookup"><span data-stu-id="66956-153">Transfer issue</span></span>

1. <span data-ttu-id="66956-154">Valitse toimintoruudun **Työ**-välilehden **Työ**-ryhmässä **Jaa työ**.</span><span class="sxs-lookup"><span data-stu-id="66956-154">On the Action Pane, on the **Work** tab, in the **Work** group, select **Split work**.</span></span>

    <span data-ttu-id="66956-155">**Jaa työ** -sivu avautuu, ja näkyvissä on avoimet ja jaettavissa olevat työrivit.</span><span class="sxs-lookup"><span data-stu-id="66956-155">The **Split work** page appears and shows the work lines that are open and available to be split.</span></span> <span data-ttu-id="66956-156">Oletusarvoisesti vain käytettävissä olevat työrivit näytetään.</span><span class="sxs-lookup"><span data-stu-id="66956-156">By default, only available work lines are shown.</span></span> <span data-ttu-id="66956-157">Voit tarkastella kaikki työtunnuksen rivit (kuten rivit, joiden työtyyppi on *Aseta*) valitsemalla **Näytä kaikki rivit** -valintaruudun ruudukon yläpuolella.</span><span class="sxs-lookup"><span data-stu-id="66956-157">To view all lines for the work ID (for example, lines that have a work type of *Put*), select the **Show all lines** check box above the grid.</span></span>

    <span data-ttu-id="66956-158">Seuraava sanoma avautuu: Käyttäjät eivät voi käsitellä työn rivejä, ennen kuin jakaminen on lopetettu ja tämä sivu suljettu.</span><span class="sxs-lookup"><span data-stu-id="66956-158">The following message is shown: "Users can't process lines of the work until you finish splitting and close this page."</span></span>

    <span data-ttu-id="66956-159">Nykyisen työn **Työn eston syy** -kentän asetukseksi määritetään *Jaa työ* ja työ estetään.</span><span class="sxs-lookup"><span data-stu-id="66956-159">The **Work blocking reason** field for the current work will be set to *Split work*, and the work will be blocked.</span></span>

    <span data-ttu-id="66956-160">![Eston syy](media/Blocking_reason.png "Eston syy")</span><span class="sxs-lookup"><span data-stu-id="66956-160">![Blocking reason](media/Blocking_reason.png "Blocking reason")</span></span>

1. <span data-ttu-id="66956-161">Valitse nykyisestä työtunnuksesta poistettavat rivit ja lisää uusi työtunnus.</span><span class="sxs-lookup"><span data-stu-id="66956-161">Select the lines to remove from the current work ID and add to a new work ID.</span></span> <span data-ttu-id="66956-162">Seuraavat tapahtumat:</span><span class="sxs-lookup"><span data-stu-id="66956-162">The following events occur:</span></span>

    - <span data-ttu-id="66956-163">Kun työ jaetaan, alkuperäisestä työtunnukset valitut rivit peruutetaan ja kopioidaan sitten uuteen työtunnukseen.</span><span class="sxs-lookup"><span data-stu-id="66956-163">When you split the work, the selected line or lines from the original work ID are canceled and then copied to a new work ID.</span></span>
    - <span data-ttu-id="66956-164">Aiemmin luodun työmallin rakenne ja asettamisen sijainti (sekä tulevat keräily/hyllytys-parit) säilytetään.</span><span class="sxs-lookup"><span data-stu-id="66956-164">The existing work template structure and the location of the put (and also future pick/put pairs) are preserved.</span></span> <span data-ttu-id="66956-165">Seuraavien työtunnuskenttien arvot kopioidaan alkuperäisestä työstä uuteen työhön:</span><span class="sxs-lookup"><span data-stu-id="66956-165">Values for the following work ID fields are copied from the original work to the new work:</span></span>

        - <span data-ttu-id="66956-166">Kuormatunnus</span><span class="sxs-lookup"><span data-stu-id="66956-166">Load ID</span></span>
        - <span data-ttu-id="66956-167">Lähetyksen tunnus</span><span class="sxs-lookup"><span data-stu-id="66956-167">Shipment ID</span></span>
        - <span data-ttu-id="66956-168">Työtilaustyyppi</span><span class="sxs-lookup"><span data-stu-id="66956-168">Work order type</span></span>
        - <span data-ttu-id="66956-169">Tilauksen numero</span><span class="sxs-lookup"><span data-stu-id="66956-169">Order number</span></span>
        - <span data-ttu-id="66956-170">Toimipaikka</span><span class="sxs-lookup"><span data-stu-id="66956-170">Site</span></span>
        - <span data-ttu-id="66956-171">Varasto</span><span class="sxs-lookup"><span data-stu-id="66956-171">Warehouse</span></span>
        - <span data-ttu-id="66956-172">Työn prioriteetti</span><span class="sxs-lookup"><span data-stu-id="66956-172">Work priority</span></span>
        - <span data-ttu-id="66956-173">Työpoolin tunnus</span><span class="sxs-lookup"><span data-stu-id="66956-173">Work pool ID</span></span>
        - <span data-ttu-id="66956-174">Aallon tunnus</span><span class="sxs-lookup"><span data-stu-id="66956-174">Wave ID</span></span>
        - <span data-ttu-id="66956-175">Työn luontinumero</span><span class="sxs-lookup"><span data-stu-id="66956-175">Work creation number</span></span>

    - <span data-ttu-id="66956-176">Seuraavia kenttiä ei kopioida uuteen työtunnukseen:</span><span class="sxs-lookup"><span data-stu-id="66956-176">The following fields aren't copied to the new work ID:</span></span>

        - <span data-ttu-id="66956-177">**Työtunnus** – uusi työtunnus luodaan soveltuvasta numerosarjasta.</span><span class="sxs-lookup"><span data-stu-id="66956-177">**Work ID** – A new work ID is generated from the appropriate number sequence.</span></span>
        - <span data-ttu-id="66956-178">**Työn tila** – tämän kentän arvoksi määritetään *Avoin*.</span><span class="sxs-lookup"><span data-stu-id="66956-178">**Work status** – This field is set to *Open*.</span></span>
        - <span data-ttu-id="66956-179">**Lukitsija** – tämä kenttä jää aluksi tyhjäksi.</span><span class="sxs-lookup"><span data-stu-id="66956-179">**Locked by** – This field is initially set to blank.</span></span>
        - <span data-ttu-id="66956-180">**Kohderekisterikilven tunnus** – tämä kenttä jätetään tyhjäksi.</span><span class="sxs-lookup"><span data-stu-id="66956-180">**Target license plate ID** – This field is left blank.</span></span>
        - <span data-ttu-id="66956-181">**Luonnin päivämäärä ja aika** – tämän kentän asetuksena on kuluva päivämäärä ja aika.</span><span class="sxs-lookup"><span data-stu-id="66956-181">**Created date and time** – This field is set to the current date and time.</span></span>
        - <span data-ttu-id="66956-182">**Estetty aalto / lukittu** – tämä kenttä lasketaan uudelleen alkuperäiselle työtunnukselle ja uudelle työtunnukselle.</span><span class="sxs-lookup"><span data-stu-id="66956-182">**Blocked wave/frozen** – This field is recomputed for the original work ID and the new work ID.</span></span>

1. <span data-ttu-id="66956-183">Valitse toimintoruudussa **Jaa työ**.</span><span class="sxs-lookup"><span data-stu-id="66956-183">On the Action Pane, select **Split work**.</span></span>

<span data-ttu-id="66956-184">Työtä jaettaessa avautuu seuraava sanoma: Käsitellään toimintoa – jaa työ.</span><span class="sxs-lookup"><span data-stu-id="66956-184">While the work is being split, the following message is shown: "Processing operation - Split work".</span></span> <span data-ttu-id="66956-185">Kun tämä sanoma on näkyvissä, voit peruuttaa toiminnon valitsemalla sanomaruudussa **Peruuta**.</span><span class="sxs-lookup"><span data-stu-id="66956-185">While this message is visible, you can cancel the operation by selecting **Cancel** in the message box.</span></span>

<span data-ttu-id="66956-186">Jos **Näytä kaikki rivit** -valintaruutua ei ole valittu, jaettu ja peruutettu rivi ei enää näy ruudukossa.</span><span class="sxs-lookup"><span data-stu-id="66956-186">If the **Show all lines** check box is cleared, the line that was split off and canceled will no longer appear in the grid.</span></span> <span data-ttu-id="66956-187">Jos valintaruutu on valittu, kyseisen rivin **Työn tila** -kentän arvoksi olisi pitänyt vaihtua *Peruutettu*.</span><span class="sxs-lookup"><span data-stu-id="66956-187">If the check box is selected, you should see that the value of the **Work status** field for that line has changed to *Canceled*.</span></span>

<span data-ttu-id="66956-188">Seuraava ilmoitus näytetään osoittamaan, että uusi työtunnus on luotu: Työ \#\#\#\# on luotu jakamalla se alkuperäisestä työstä \#\#\#\#.</span><span class="sxs-lookup"><span data-stu-id="66956-188">The following notification is shown to indicate that the new work ID has been created: "Work \#\#\#\# has been created by splitting off from original work \#\#\#\#."</span></span>

<span data-ttu-id="66956-189">Muut alkuperäisen työtunnuksen työrivit (kuten *Aseta*-rivit) oikaistaan tarvittaessa ilmaisemaan peruutetut työn rivit.</span><span class="sxs-lookup"><span data-stu-id="66956-189">Other work lines from the original work ID (such as *Put* lines) will be adjusted as required to reflect the lines of work that have been canceled.</span></span> <span data-ttu-id="66956-190">Jos esimerkiksi alkuperäisen työntunnuksen *Aseta*-rivin määrä oli 15 ja *Keräily*-rivien yhteismäärä oli 10 ja ne peruutettiin, alkuperäisen työtunnuksen uusi *Aseta*-määrä on nyt 5.</span><span class="sxs-lookup"><span data-stu-id="66956-190">For example, if the original work ID had a *Put* line for a quantity of 15, and *Pick* lines that have a total quantity of 10 were canceled, the new *Put* quantity on the original work ID will now be 5.</span></span>

<span data-ttu-id="66956-191">Uutta työtä ei määritetä heti yhdellekään käyttäjälle.</span><span class="sxs-lookup"><span data-stu-id="66956-191">The new work won't immediately be assigned to any user.</span></span> <span data-ttu-id="66956-192">Voit kuitenkin määrittää sen nyt tarvittaessa käyttäjälle käyttämällä **Työn tiedot** -sivun vakiotoimintoa.</span><span class="sxs-lookup"><span data-stu-id="66956-192">However, you can assign it to a user now, as required, by using the standard functionality of the **Work details** page.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="66956-193">Vain sellaiset työtunnukset voidaan jakaa, joissa on vähintään kaksi käytettävissä olevaa työriviä.</span><span class="sxs-lookup"><span data-stu-id="66956-193">You can split only work IDs that contain two or more available work lines.</span></span> <span data-ttu-id="66956-194">Jos valitse **Jaa työ**, kun käytössä on vain yksi työrivi, seuraava virhesanoma avautuu: Alkuperäiseen työhön on jäätävä vähintään yksi työrivi.</span><span class="sxs-lookup"><span data-stu-id="66956-194">If you select **Split work** when there is only one work line, you will receive the following error message: "At least one work line must remain on initial work."</span></span> <span data-ttu-id="66956-195">Tässä tapauksessa jakoa ei tehdä.</span><span class="sxs-lookup"><span data-stu-id="66956-195">In this case, no splitting will occur.</span></span>

## <a name="finish-a-work-split"></a><span data-ttu-id="66956-196">Työn jaon lopettaminen</span><span class="sxs-lookup"><span data-stu-id="66956-196">Finish a work split</span></span>

<span data-ttu-id="66956-197">Työn jakamisen lopettaminen edellyttää, että *Jaa työ* eston syynä on poistettava.</span><span class="sxs-lookup"><span data-stu-id="66956-197">To finish splitting work, the *Split work* blocking reason must be removed.</span></span> <span data-ttu-id="66956-198">Sen voi tehdä kahdella tavalla:</span><span class="sxs-lookup"><span data-stu-id="66956-198">There are two ways to complete this step:</span></span>

- <span data-ttu-id="66956-199">Työn jakava käyttäjä sulkee **Jaa työ** -sivun valitsemalla **Sulje**-painikkeen (**X**) sivun oikeassa yläkulmassa.</span><span class="sxs-lookup"><span data-stu-id="66956-199">The user who is splitting the work closes the **Split work** page by selecting the **Close** button (**X**) in the upper-right corner.</span></span> <span data-ttu-id="66956-200">Kun sivu suljetaan, *Jaa työ* eston syynä poistetaan.</span><span class="sxs-lookup"><span data-stu-id="66956-200">When the page is closed, the *Split Work* blocking reason will be removed.</span></span> <span data-ttu-id="66956-201">Tämän työn *Estetty*-tila käsitellään uudelleen ja jos työllä ei ole muita eston syitä, työn esto poistetaan.</span><span class="sxs-lookup"><span data-stu-id="66956-201">The *Blocked* state of this work will be recomputed and, if there are no remaining blocking reasons for this work, the work will be unblocked.</span></span>
- <span data-ttu-id="66956-202">Joku käyttäjä avaa työtunnuksen ja valitsee toimintoruudussa **Peruuta työn jakoistunto** -painikkeen.</span><span class="sxs-lookup"><span data-stu-id="66956-202">Any user opens the work ID and selects the **Cancel work split session** button on the Action Pane.</span></span> <span data-ttu-id="66956-203">*Jaa työ* poistetaan eston syynä ja työn *Estetty*-tila käsitellään uudelleen samalla tavoin kuin **Jaa työ** -sivua suljettaessa.</span><span class="sxs-lookup"><span data-stu-id="66956-203">The *Split work* blocking reason will be removed, and the *Blocked* state of this work will be recomputed, just as when the **Split work** page is closed.</span></span>

<span data-ttu-id="66956-204">Kun *Jaa työ* on poistettu eston syynä, työ voidaan suorittaa mobiililaitteessa, mikäli **Estetty**-tilan asetuksena on työtunnuksessa *Ei*.</span><span class="sxs-lookup"><span data-stu-id="66956-204">After the *Split work* blocking reason is removed, the work can be run on the mobile device, provided that the **Blocked** state is set to *No* on the work ID.</span></span>

## <a name="user-blocking-on-the-warehouse-app"></a><span data-ttu-id="66956-205">Käyttäjän estäminen varastosovelluksessa</span><span class="sxs-lookup"><span data-stu-id="66956-205">User blocking on the warehouse app</span></span>

<span data-ttu-id="66956-206">Jos yrität suorittaa keräilytyön varastosovelluksessa sellaisen tunnuksen osalta, jota jaetaan, seuraava virhesanoma avautuu: Työtä, jonka tunnus on \#\#\#\#, jaetaan parhaillaan.</span><span class="sxs-lookup"><span data-stu-id="66956-206">If you try to use the warehouse app to run picking work against a work ID that is being split, you will receive the following error message: "The work with ID \#\#\#\# is currently being split."</span></span> <span data-ttu-id="66956-207">Jos tämä sanoma avautuu, valitse **Peruuta**.</span><span class="sxs-lookup"><span data-stu-id="66956-207">If you receive this message, select **Cancel**.</span></span> <span data-ttu-id="66956-208">Voit sitten jatkaa muiden töiden käsittelyä.</span><span class="sxs-lookup"><span data-stu-id="66956-208">You can then continue to process other work.</span></span>

## <a name="other-blocked-operations"></a><span data-ttu-id="66956-209">Muut estetyt toiminnot</span><span class="sxs-lookup"><span data-stu-id="66956-209">Other blocked operations</span></span>

<span data-ttu-id="66956-210">Kaikki sellaiset jaettavaan työhön liittyvät toiminnot, jotka muokkaavat työrivejä, työn varastotapahtumia tai täydennyslinkkejä, epäonnistuvat ja seuraava sanoma avautuu: Työtä, jonka tunnus on \#\#\#\#, jaetaan parhaillaan.</span><span class="sxs-lookup"><span data-stu-id="66956-210">Any operations that modify work lines, work inventory transactions, or replenishment links that are related to work that is being split will fail, and the following error message will be shown: "The work with ID \#\#\#\# is currently being split."</span></span>
