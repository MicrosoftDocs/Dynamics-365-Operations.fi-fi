---
title: Laadunhallinnan testiryhmät
description: Tässä aiheessa kuvataan, kuinka testiryhmiä luodaan, jotta laatutilauksissa voidaan käyttää useita testejä Microsoft Dynamics 365 Supply Chain Managementissa.
author: rachel-profitt
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTestGroup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2e0adac76d7b5ecf993ab75c60eced41050034f8
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956641"
---
# <a name="quality-management-test-groups"></a><span data-ttu-id="04522-103">Laadunhallinnan testiryhmät</span><span class="sxs-lookup"><span data-stu-id="04522-103">Quality management test groups</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="04522-104">Tässä aiheessa kuvataan, kuinka testiryhmiä luodaan, jotta laatutilauksissa voidaan käyttää useita testejä Microsoft Dynamics 365 Supply Chain Managementissa.</span><span class="sxs-lookup"><span data-stu-id="04522-104">This topic describes how to create test groups, so that multiple tests can be used with quality orders in Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="04522-105">Voit määrittää, muokata ja tarkastella testiryhmiä ja testiryhmälle määritettyjä yksittäisiä testejä **Testiryhmä**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="04522-105">You use the **Test groups** page to set up, edit, and view test groups and the individual tests that are assigned to them.</span></span> <span data-ttu-id="04522-106">Sivun yläosassa näkyvät testiryhmät, ja alaosassa näkyvät valitulle testiryhmälle määritetyt testit.</span><span class="sxs-lookup"><span data-stu-id="04522-106">The upper part of the page shows the test groups, and the lower part shows the tests that are assigned to a selected test group.</span></span>

<span data-ttu-id="04522-107">Voit määrittää testiryhmälle useita käytäntöjä, kuten otantasuunnitelman, hyväksytyn laatutason ja destruktiivisen testin tarpeen.</span><span class="sxs-lookup"><span data-stu-id="04522-107">You assign several policies to a test group, such as a sampling plan, an acceptable quality level (AQL), and the requirement for destructive testing.</span></span> <span data-ttu-id="04522-108">Kun määrität testiryhmään yksittäisen testin, määrität samalla lisätietoja, kuten järjestyksen, asiakirjat ja voimassaolopäivät.</span><span class="sxs-lookup"><span data-stu-id="04522-108">Then, when you assign an individual test to a test group, you define additional information, such as the sequence, documents, and validity dates.</span></span> <span data-ttu-id="04522-109">Määrällisessä testissä määritetään myös hyväksyttävät mitta-arvot.</span><span class="sxs-lookup"><span data-stu-id="04522-109">For a quantitative test, the information that you define also includes the acceptable measurement values.</span></span> <span data-ttu-id="04522-110">Laadullisessa testissä tietoja ovat testimuuttuja ja oletustulos.</span><span class="sxs-lookup"><span data-stu-id="04522-110">For a qualitative test, the information includes the test variable and default outcome.</span></span>

<span data-ttu-id="04522-111">Laatutilaukseen määritetty testiryhmä määrittää oletustestit, jotka tietylle nimikkeelle on suoritettava.</span><span class="sxs-lookup"><span data-stu-id="04522-111">The test group that is assigned to a quality order defines the default set of tests that must be performed on the specified item.</span></span> <span data-ttu-id="04522-112">Voit kuitenkin lisätä, muuttaa ja poistaa laatutilauksen testejä.</span><span class="sxs-lookup"><span data-stu-id="04522-112">However, you can add, delete, or change tests for the quality order.</span></span> <span data-ttu-id="04522-113">Laatutilauksen jokaisen testin tulokset raportoidaan.</span><span class="sxs-lookup"><span data-stu-id="04522-113">Test results are reported for each test on a quality order.</span></span>

<span data-ttu-id="04522-114">Kun määrität testiryhmän, voit halutessasi määrittää nimikeotantamenetelmän.</span><span class="sxs-lookup"><span data-stu-id="04522-114">When you define a test group, you can optionally specify an item sampling.</span></span> <span data-ttu-id="04522-115">Nimikeotantoja käytetään testattavan tuotteen määrän määrittämiseen.</span><span class="sxs-lookup"><span data-stu-id="04522-115">Item samplings are used to define the amount of the product that must be tested.</span></span> <span data-ttu-id="04522-116">Lisätietoja on kohdassa [Laadunhallinnan nimikeotanta](quality-item-sampling.md).</span><span class="sxs-lookup"><span data-stu-id="04522-116">For more information, see [Quality management item sampling](quality-item-sampling.md).</span></span> <span data-ttu-id="04522-117">Voit myös määrittää, ovatko testiryhmän testit destruktiivisia.</span><span class="sxs-lookup"><span data-stu-id="04522-117">You can also indicate whether the tests in a test group are destructive.</span></span> <span data-ttu-id="04522-118">Destruktiivisessa testissä nimikeotanta tuhotaan ja määrä poistetaan käytettävissä olevasta varastosta.</span><span class="sxs-lookup"><span data-stu-id="04522-118">In a destructive test, the item sampling is destroyed, and the quantity is removed from the on-hand inventory.</span></span>

## <a name="example-of-a-test-group"></a><span data-ttu-id="04522-119">Esimerkki testiryhmästä</span><span class="sxs-lookup"><span data-stu-id="04522-119">Example of a test group</span></span>

<span data-ttu-id="04522-120">Tuotantoyritys määrittää testiryhmän kutakin laatuvaatimusversiotaan varten.</span><span class="sxs-lookup"><span data-stu-id="04522-120">A manufacturing company defines a test group for each variation of its quality guidelines.</span></span> <span data-ttu-id="04522-121">Eri testiryhmät edustavat eroja otantasuunnitelmissa, yhdessä suoritettavissa testeissä, hyväksytyissä mitta-arvoissa ja muissa seikoissa.</span><span class="sxs-lookup"><span data-stu-id="04522-121">The various test groups reflect differences in the sampling plans, the sets of tests that must be performed together, the AQL, and other factors.</span></span> <span data-ttu-id="04522-122">Määrällisissä testeissä eroja on hyväksyttävissä mitta-arvoissa.</span><span class="sxs-lookup"><span data-stu-id="04522-122">For quantitative tests, there are also differences in the acceptable measurement values.</span></span> <span data-ttu-id="04522-123">Laatuohjeidensa noudattamista varten yritys liittää testiryhmän kuhunkin sääntöön, jota käytetään laatutilausten tuottamiseen automaattisesti **Laatuliitokset**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="04522-123">To enforce its quality guidelines, the company assigns a test group to each rule that is used to automatically generate quality orders on the **Quality associations** page.</span></span> <span data-ttu-id="04522-124">Se liittää myös testiryhmän manuaalisesti luotuihin laatutilauksiin.</span><span class="sxs-lookup"><span data-stu-id="04522-124">It also assigns a test group to quality orders that are manually created.</span></span>

## <a name="create-a-test-group"></a><span data-ttu-id="04522-125">Testiryhmän luominen</span><span class="sxs-lookup"><span data-stu-id="04522-125">Create a test group</span></span>

<span data-ttu-id="04522-126">Voit luoda testiryhmän seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="04522-126">To create a test group, follow these steps.</span></span>

1. <span data-ttu-id="04522-127">Valitse **Varastonhallinta \> Asetukset \> Laadunvalvonta \> Testiryhmät**.</span><span class="sxs-lookup"><span data-stu-id="04522-127">Go to **Inventory management \> Setup \> Quality control \> Test groups**.</span></span>
1. <span data-ttu-id="04522-128">Valitse toimintoruudussa **Uusi** lisätäksesi rivin ruudukkoon sivun yläosassa.</span><span class="sxs-lookup"><span data-stu-id="04522-128">On the Action Pane, select **New** to add a row to the grid in the upper part of the page.</span></span> <span data-ttu-id="04522-129">Määritä sitten uudelle rivillä seuraavat kentät:</span><span class="sxs-lookup"><span data-stu-id="04522-129">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="04522-130">**Testiryhmä** – Määritä testiryhmän yksilöivä tunnus tai nimi.</span><span class="sxs-lookup"><span data-stu-id="04522-130">**Test group** – Enter a unique ID or name for the test group.</span></span>
    - <span data-ttu-id="04522-131">**Kuvaus** – Anna testiryhmän yksityiskohtainen kuvaus.</span><span class="sxs-lookup"><span data-stu-id="04522-131">**Description** – Enter a detailed description of the test group.</span></span>
    - <span data-ttu-id="04522-132">**Hyväksyttävän laadun taso** – Määritä testitulosten kokonaisprosentti, joka on hyväksyttävä, jotta testiryhmä voidaan katsoa hyväksytyksi.</span><span class="sxs-lookup"><span data-stu-id="04522-132">**Acceptable quality level** – Enter the total percentage of test results that must pass for the group of tests to be considered passed.</span></span>
    - <span data-ttu-id="04522-133">**Nimikeotanta** – Valitse nimikeotanta.</span><span class="sxs-lookup"><span data-stu-id="04522-133">**Item sampling** – Select an item sampling.</span></span> <span data-ttu-id="04522-134">Lisätietoja on kohdassa [Laadunhallinnan nimikeotanta](quality-item-sampling.md).</span><span class="sxs-lookup"><span data-stu-id="04522-134">For more information, see [Quality management item sampling](quality-item-sampling.md).</span></span>
    - <span data-ttu-id="04522-135">**Destruktiivinen** – Valitsemalla tämän valintaruudun voit määrittää, että testiryhmä tuhoaa testatut nimikkeet.</span><span class="sxs-lookup"><span data-stu-id="04522-135">**Destructive** – Select this check box to indicate that the test group will destroy the items that are tested.</span></span>

1. <span data-ttu-id="04522-136">Kun uusi rivi on vielä valittuna, valitse sivun yläosasta **Yleiset**-välilehti.</span><span class="sxs-lookup"><span data-stu-id="04522-136">While the new row is still selected, select the **General** tab in the upper part of the page.</span></span> <span data-ttu-id="04522-137">Osa **Yhteenveto**-välilehdessä valitun testiryhmän asetuksista toistetaan tässä.</span><span class="sxs-lookup"><span data-stu-id="04522-137">Some of the settings for the test group that is selected on the **Overview** tab are repeated here.</span></span> <span data-ttu-id="04522-138">Voit määrittää ryhmälle myös seuraavat kentät:</span><span class="sxs-lookup"><span data-stu-id="04522-138">In addition, you can set the following fields for the group:</span></span>

    - <span data-ttu-id="04522-139">**Päivitä varaston erämäärite** – Kun määrität tämän asetuksen arvoksi *Kyllä* tässä, arvoksi määritetään automaattisesti *Kyllä* kaikille uusille testeille, jotka lisätään sivun alaosan testiryhmään.</span><span class="sxs-lookup"><span data-stu-id="04522-139">**Update inventory batch attribute** – When you set this option to *Yes* here, it will automatically be set to *Yes* for every new test that is added to the test group in the lower part of the page.</span></span>
    - <span data-ttu-id="04522-140">**Päivitä eräkäsittely** – Kun määrität tämän asetuksen arvoksi *Kyllä*, jos testattavaa nimikettä ohjataan eräkäsittelyllä, eräkäsittely päivittyy automaattisesti arvolla, joka on valittu **Epäonnistuneen laatutilauserän käsittely**- tai **Onnistuneen laatutilauserän käsittely** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="04522-140">**Update batch disposition** – When you set this option to *Yes*, if the item that is being tested is batch controlled, the batch disposition will automatically be updated with the value that is selected in the **Failed quality order batch disposition** or **Passed quality order batch disposition** field.</span></span>
    - <span data-ttu-id="04522-141">**Epäonnistuneen laatutilauserän käsittely** – Valitse erän käsittelykoodi, joka on pitäisi määrittää, kun tämän testiryhmän sisältävä laatutilaus epäonnistuu, koska se ei täytä hyväksyttävän laadun tasoa.</span><span class="sxs-lookup"><span data-stu-id="04522-141">**Failed quality order batch disposition** – Select the batch disposition code that should be assigned when a quality order that includes this test group fails because it doesn't meet the AQL.</span></span>
    - <span data-ttu-id="04522-142">**Onnistuneen laatutilauserän käsittely** – Valitse erän käsittelykoodi, joka on pitäisi määrittää, kun tämän testiryhmän sisältävä laatutilaus onnistuu, koska se täyttää hyväksyttävän laadun tason.</span><span class="sxs-lookup"><span data-stu-id="04522-142">**Passed quality order batch disposition** – Select the batch disposition code that should be assigned when a quality order that includes this test group passes because it meets the AQL.</span></span>
    - <span data-ttu-id="04522-143">**Päivitä varaston tila** – Kun määrität tämän asetuksen arvoksi *Kyllä*, jos testattavan nimikkeen varastodimensioryhmän **Varastotila** on otettu käyttöön, tilaksi päivitetään automaattisesti tila, joka on valittuna **Epäonnistuneen laatutilauksen tila**- tai **Onnistuneen laatutilauksen tila** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="04522-143">**Update inventory status** – When you set this option to *Yes*, if **Inventory status** is enabled on the storage dimension group for the item that is being tested, the status will automatically be updated with the status that is selected in the **Failed quality order status** or **Passed quality order status** field.</span></span>
    - <span data-ttu-id="04522-144">**Epäonnistuneen laatutilauksen tila** – Valitse varastotila, joka on pitäisi määrittää nimikkeelle, kun tämän testiryhmän sisältävä laatutilaus epäonnistuu, koska se ei täytä hyväksyttävän laadun tasoa.</span><span class="sxs-lookup"><span data-stu-id="04522-144">**Failed quality order status** – Select the inventory status that should be assigned to the item when a quality order that includes this test group fails because it doesn't meet the AQL.</span></span>
    - <span data-ttu-id="04522-145">**Onnistuneen laatutilauksen tila** – Valitse varastotila, joka on pitäisi määrittää nimikkeelle, kun tämän testiryhmän sisältävä laatutilaus onnistuu, koska se täyttää hyväksyttävän laadun tason.</span><span class="sxs-lookup"><span data-stu-id="04522-145">**Passed quality order status** – Select the inventory status that should be assigned to the item when a quality order that includes this test group passes because it meets the AQL.</span></span>

## <a name="add-a-qualitative-test-to-a-test-group"></a><span data-ttu-id="04522-146">Laadullisen testin lisääminen testiryhmään</span><span class="sxs-lookup"><span data-stu-id="04522-146">Add a qualitative test to a test group</span></span>

<span data-ttu-id="04522-147">Voit lisätä laadullisen testin testiryhmään noudattamalla seuraavia vaiheita.</span><span class="sxs-lookup"><span data-stu-id="04522-147">To add a qualitative test to a test group, follow these steps.</span></span>

1. <span data-ttu-id="04522-148">Valitse **Varastonhallinta \> Asetukset \> Laadunvalvonta \> Testiryhmät**.</span><span class="sxs-lookup"><span data-stu-id="04522-148">Go to **Inventory management \> Setup \> Quality control \> Test groups**.</span></span>
1. <span data-ttu-id="04522-149">Valitse **Yhteenveto**-välilehdestä sivun yläosassa testiryhmä, johon haluat lisätä testin.</span><span class="sxs-lookup"><span data-stu-id="04522-149">On the **Overview** tab in the upper part of the page, select the test group that you want to add a test to.</span></span>
1. <span data-ttu-id="04522-150">Lisää rivi ruudukkoon valitsemalla sivun alaosan **Yhteenveto**-välilehdestä **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="04522-150">In the lower part of the page, on the **Overview** tab, select **Add** on the toolbar to add a row to the grid.</span></span> <span data-ttu-id="04522-151">Määritä sitten uudelle rivillä seuraavat kentät:</span><span class="sxs-lookup"><span data-stu-id="04522-151">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="04522-152">**Järjestysnumero** – Kirjoita kokonaisluku, joka määrittää järjestyksen, jossa testit on suoritettava.</span><span class="sxs-lookup"><span data-stu-id="04522-152">**Sequence number** – Enter an integer to specify the order that the tests should be performed in.</span></span> <span data-ttu-id="04522-153">Pienemmällä järjestysnumerolla olevat testit suoritetaan ennen kuin testejä, joilla on suuremmat järjestysnumerot.</span><span class="sxs-lookup"><span data-stu-id="04522-153">Tests that have smaller sequence numbers will be run before tests that have larger sequence numbers.</span></span>

        > [!NOTE]
        > <span data-ttu-id="04522-154">Suosittelemme, että jätät järjestysnumeroiden väliin välin.</span><span class="sxs-lookup"><span data-stu-id="04522-154">We recommend that you leave a gap between sequence numbers.</span></span> <span data-ttu-id="04522-155">Määritä esimerkiksi ensimmäisen testin **Järjestysnumero**-kentän arvoksi *10* ja lisää sitten kunkin lisätestin arvoa 10:llä.</span><span class="sxs-lookup"><span data-stu-id="04522-155">For example, set the **Sequence number** field to *10* for your first test, and then increment the value by 10 for each additional test.</span></span> <span data-ttu-id="04522-156">Näin voit lisätä uusia testejä myöhemmin ilman, että rivejä tarvitsee poistaa ja luoda uudelleen, jotta testit voidaan asettaa haluttuun järjestykseen.</span><span class="sxs-lookup"><span data-stu-id="04522-156">In this way, you can add new tests later without having to delete and re-create the lines to put them in the desired order.</span></span>

    - <span data-ttu-id="04522-157">**Testt** – Valitse suoritettava testi.</span><span class="sxs-lookup"><span data-stu-id="04522-157">**Test** – Select the test that you want to perform.</span></span> <span data-ttu-id="04522-158">Valitse laadullista testiä varten testi, jossa **Tyyppi**-kentän arvoksi on määritetty *Asetus*.</span><span class="sxs-lookup"><span data-stu-id="04522-158">For a qualitative test, select a test where the **Type** field is set to *Option*.</span></span>
    - <span data-ttu-id="04522-159">**Voimassa** – Valitse ensimmäinen päivämäärä, jolloin testi on voimassa.</span><span class="sxs-lookup"><span data-stu-id="04522-159">**Effective** – Select the first date when the test is valid.</span></span> <span data-ttu-id="04522-160">Jos jätät kentän tyhjäksi, rajaa ei ole.</span><span class="sxs-lookup"><span data-stu-id="04522-160">If you leave this field blank, there is no limit.</span></span>
    - <span data-ttu-id="04522-161">**Vanhentumisaika** – Valitse viimeinen päivämäärä, jolloin testi on voimassa.</span><span class="sxs-lookup"><span data-stu-id="04522-161">**Expiration** – Select the last date when the test is valid.</span></span> <span data-ttu-id="04522-162">Jos jätät tämän kentän tyhjäksi tai määrität sen arvoksi *Ei koskaan*, rajaa ei ole.</span><span class="sxs-lookup"><span data-stu-id="04522-162">If you leave this field blank or set it to *Never*, there is no limit.</span></span>
    - <span data-ttu-id="04522-163">**Testiarvon määritys** – Valitse, miten hyväksyttävän laadun taso määritetään, kun samalle testille kirjataan useita tuloksia.</span><span class="sxs-lookup"><span data-stu-id="04522-163">**Test value determination** – Select how an AQL should be determined when multiple results are recorded for the same test.</span></span> <span data-ttu-id="04522-164">Laadullista testiä varten voidaan valita vain *Manuaalinen*.</span><span class="sxs-lookup"><span data-stu-id="04522-164">For a qualitative test, only *Manual* can be selected.</span></span> <span data-ttu-id="04522-165">Jos valitset toisen arvoista (*Keskimääräinen*, *Minimi* tai *Maksimi*), näyttöön tulee virhesanoma, kun tallennat testiryhmän.</span><span class="sxs-lookup"><span data-stu-id="04522-165">If you select one of the other values (*Average*, *Minimum*, or *Maximum*), you will receive an error message when you save the test group.</span></span>
    - <span data-ttu-id="04522-166">**Määrite** – Jos haluat tallentaa testitulokset erämääritteeseen, valitse määrite tästä ja valitse **Päivitä varaston erämäärite** -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="04522-166">**Attribute** – If you want to record test results on a batch attribute, select the attribute here, and select the **Update inventory batch attribute** check box.</span></span>
    - <span data-ttu-id="04522-167">**Päivitä varaston erämäärite** – Valitse tämä valintaruutu, jos haluat tallentaa testituloksia erämääritteelle, joka on valittuna **Määrite**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="04522-167">**Update inventory batch attribute** – Select this check box to record test results for the batch attribute that is selected in the **Attribute** field.</span></span>

1. <span data-ttu-id="04522-168">Valitse sivun alaosasta **Yleiset**-välilehti. Osa **Yhteenveto**-välilehdessä valitun testin asetuksista toistetaan tässä.</span><span class="sxs-lookup"><span data-stu-id="04522-168">In the lower part of the page, select the **General** tab. Some of the settings for the test that is selected on the **Overview** tab are repeated here.</span></span> <span data-ttu-id="04522-169">Voit määrittää testille myös seuraavat kentät:</span><span class="sxs-lookup"><span data-stu-id="04522-169">In addition, you can set the following fields for the test:</span></span>

    - <span data-ttu-id="04522-170">**Analyysitodistusraportti** – Määritä tämän asetuksen arvoksi *Kyllä*, kun haluat, että testitulokset tulostetaan analyysitodistukseen (CoA).</span><span class="sxs-lookup"><span data-stu-id="04522-170">**Certificate of analysis report** – Set this option to *Yes* to indicate that the test results should be printed on the certificate of analysis (CoA).</span></span> <span data-ttu-id="04522-171">Tämän raportin voi luoda laatutilauksesta.</span><span class="sxs-lookup"><span data-stu-id="04522-171">This report can be generated from the quality order.</span></span>
    - <span data-ttu-id="04522-172">**Virheen yhteydessä tehtävä toiminto** – Valitse joko *Hyväksy* tai *Epäonnistuminen* ilmaistaksesi, hyväksytäänkö vai hylätäänkö testi, jos sen hyväksyttävän laadun taso ei täyty.</span><span class="sxs-lookup"><span data-stu-id="04522-172">**Action on failure** – Select either *Accept* or *Fail* to indicate whether the test should pass or fail if the AQL for it isn't met.</span></span>
    - <span data-ttu-id="04522-173">**Hyväksyttävän laadun taso** – Määritä testitulosten kokonaisprosentti, joka on hyväksyttävä, jotta testi voidaan katsoa hyväksytyksi.</span><span class="sxs-lookup"><span data-stu-id="04522-173">**Acceptable quality level** – Enter the total percentage of test results that must pass for the test to be considered passed.</span></span>

1. <span data-ttu-id="04522-174">Määritä sivun alaosan **Testi**-välilehdessä seuraavat kentät:</span><span class="sxs-lookup"><span data-stu-id="04522-174">In the lower part of the page, on the **Test** tab, set the following fields:</span></span>

    - <span data-ttu-id="04522-175">**Muuttuja** – Valitse testimuuttuja laadullisen testin tulosten tallentamista varten.</span><span class="sxs-lookup"><span data-stu-id="04522-175">**Variable** – Select the test variable to record the qualitative test results for.</span></span>
    - <span data-ttu-id="04522-176">**Oletustulos** – Valitse oletustulos, joka pitäisi tallentaa testituloksille.</span><span class="sxs-lookup"><span data-stu-id="04522-176">**Default outcome** – Select the default outcome that should be recorded for the test results.</span></span>
    - <span data-ttu-id="04522-177">**Testin mittaväline** – Valitse laite, jota testissä on käytettävä.</span><span class="sxs-lookup"><span data-stu-id="04522-177">**Test instrument** – Select the device that should be used for the test.</span></span> <span data-ttu-id="04522-178">Jos testille on määritetty mittaväline, se syötetään testiryhmän testille automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="04522-178">If a test instrument is defined, it's automatically entered for the test in the test group.</span></span>

1. <span data-ttu-id="04522-179">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="04522-179">Close the page.</span></span>

## <a name="add-a-quantitative-test-to-a-test-group"></a><span data-ttu-id="04522-180">Määrällisen testin lisääminen testiryhmään</span><span class="sxs-lookup"><span data-stu-id="04522-180">Add a quantitative test to a test group</span></span>

<span data-ttu-id="04522-181">Voit lisätä määrällisen testin testiryhmään noudattamalla seuraavia vaiheita.</span><span class="sxs-lookup"><span data-stu-id="04522-181">To add a quantitative test to a test group, follow these steps.</span></span>

1. <span data-ttu-id="04522-182">Valitse **Varastonhallinta \> Asetukset \> Laadunvalvonta \> Testiryhmät**.</span><span class="sxs-lookup"><span data-stu-id="04522-182">Go to **Inventory management \> Setup \> Quality control \> Test groups**.</span></span>
1. <span data-ttu-id="04522-183">Valitse **Yhteenveto**-välilehdestä sivun yläosassa testiryhmä, johon haluat lisätä testin.</span><span class="sxs-lookup"><span data-stu-id="04522-183">On the **Overview** tab in the upper part of the page, select the test group that you want to add a test to.</span></span>
1. <span data-ttu-id="04522-184">Lisää rivi ruudukkoon valitsemalla sivun alaosan **Yhteenveto**-välilehdestä **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="04522-184">In the lower part of the page, on the **Overview** tab, select **Add** on the toolbar to add a row to the grid.</span></span> <span data-ttu-id="04522-185">Määritä sitten uudelle rivillä seuraavat kentät:</span><span class="sxs-lookup"><span data-stu-id="04522-185">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="04522-186">**Järjestysnumero** – Kirjoita kokonaisluku, joka määrittää järjestyksen, jossa testit on suoritettava.</span><span class="sxs-lookup"><span data-stu-id="04522-186">**Sequence number** – Enter an integer to specify the order that the tests should be performed in.</span></span> <span data-ttu-id="04522-187">Pienemmällä järjestysnumerolla olevat testit suoritetaan ennen kuin testejä, joilla on suuremmat järjestysnumerot.</span><span class="sxs-lookup"><span data-stu-id="04522-187">Tests that have smaller sequence numbers will be run before tests that have larger sequence numbers.</span></span>

        > [!NOTE]
        > <span data-ttu-id="04522-188">Suosittelemme, että jätät järjestysnumeroiden väliin välin.</span><span class="sxs-lookup"><span data-stu-id="04522-188">We recommend that you leave a gap between sequence numbers.</span></span> <span data-ttu-id="04522-189">Määritä esimerkiksi ensimmäisen testin **Järjestysnumero**-kentän arvoksi *10* ja lisää sitten kunkin lisätestin arvoa 10:llä.</span><span class="sxs-lookup"><span data-stu-id="04522-189">For example, set the **Sequence number** field to *10* for your first test, and then increment the value by 10 for each additional test.</span></span> <span data-ttu-id="04522-190">Näin voit lisätä uusia testejä myöhemmin ilman, että rivejä tarvitsee poistaa ja luoda uudelleen, jotta testit voidaan asettaa haluttuun järjestykseen.</span><span class="sxs-lookup"><span data-stu-id="04522-190">In this way, you can add new tests later without having to delete and re-create the lines to put them in the desired order.</span></span>

    - <span data-ttu-id="04522-191">**Testt** – Valitse suoritettava testi.</span><span class="sxs-lookup"><span data-stu-id="04522-191">**Test** – Select the test that you want to perform.</span></span> <span data-ttu-id="04522-192">Valitse määrällistä testiä varten testi, jossa **Tyyppi**-kentän arvoksi on määritetty *Murtoluku* tai *Kokonaisluku*.</span><span class="sxs-lookup"><span data-stu-id="04522-192">For a quantitative test, select a test where the **Type** field is set to *Fraction* or *Integer*.</span></span>
    - <span data-ttu-id="04522-193">**Voimassa** – Valitse ensimmäinen päivämäärä, jolloin testi on voimassa.</span><span class="sxs-lookup"><span data-stu-id="04522-193">**Effective** – Select the first date when the test is valid.</span></span> <span data-ttu-id="04522-194">Jos jätät kentän tyhjäksi, rajaa ei ole.</span><span class="sxs-lookup"><span data-stu-id="04522-194">If you leave this field blank, there is no limit.</span></span>
    - <span data-ttu-id="04522-195">**Vanhentumisaika** – Valitse viimeinen päivämäärä, jolloin testi on voimassa.</span><span class="sxs-lookup"><span data-stu-id="04522-195">**Expiration** – Select the last date when the test is valid.</span></span> <span data-ttu-id="04522-196">Jos jätät tämän kentän tyhjäksi tai määrität sen arvoksi *Ei koskaan*, rajaa ei ole.</span><span class="sxs-lookup"><span data-stu-id="04522-196">If you leave this field blank or set it to *Never*, there is no limit.</span></span>
    - <span data-ttu-id="04522-197">**Testiarvon määritys** – Valitse, miten hyväksyttävän laadun taso määritetään, kun samalle testille kirjataan useita tuloksia.</span><span class="sxs-lookup"><span data-stu-id="04522-197">**Test value determination** – Select how an AQL should be determined when multiple results are recorded for the same test.</span></span> <span data-ttu-id="04522-198">Käytettävissä olevat asetukset ovat *Keskimääräinen*, *Minimi*, *Maksimi* ja *Manuaalinen*.</span><span class="sxs-lookup"><span data-stu-id="04522-198">The available options are *Average*, *Minimum*, *Maximum*, and *Manual*.</span></span>
    - <span data-ttu-id="04522-199">**Määrite** – Jos haluat tallentaa testitulokset erämääritteeseen, valitse määrite tästä ja valitse **Päivitä varaston erämäärite** -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="04522-199">**Attribute** – If you want to record test results on a batch attribute, select the attribute here, and select the **Update inventory batch attribute** check box.</span></span>
    - <span data-ttu-id="04522-200">**Päivitä varaston erämäärite** – Valitse tämä valintaruutu, jos haluat tallentaa testituloksia erämääritteelle, joka on valittuna **Määrite**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="04522-200">**Update inventory batch attribute** – Select this check box to record test results for the batch attribute that is selected in the **Attribute** field.</span></span>

1. <span data-ttu-id="04522-201">Valitse sivun alaosasta **Yleiset**-välilehti. Osa **Yhteenveto**-välilehdessä valitun testin asetuksista toistetaan tässä.</span><span class="sxs-lookup"><span data-stu-id="04522-201">In the lower part of the page, select the **General** tab. Some of the settings for the test that is selected on the **Overview** tab are repeated here.</span></span> <span data-ttu-id="04522-202">Voit määrittää testille myös seuraavat kentät:</span><span class="sxs-lookup"><span data-stu-id="04522-202">In addition, you can set the following fields for the test:</span></span>

    - <span data-ttu-id="04522-203">**Analyysitodistusraportti** – Määritä tämän asetuksen arvoksi *Kyllä*, kun haluat, että testitulokset tulostetaan analyysitodistukseen (CoA).</span><span class="sxs-lookup"><span data-stu-id="04522-203">**Certificate of analysis report** – Set this option to *Yes* to indicate that the test results should be printed on the CoA.</span></span> <span data-ttu-id="04522-204">Tämän raportin voi luoda laatutilauksesta.</span><span class="sxs-lookup"><span data-stu-id="04522-204">This report can be generated from the quality order.</span></span>
    - <span data-ttu-id="04522-205">**Virheen yhteydessä tehtävä toiminto** – Valitse joko *Hyväksy* tai *Epäonnistuminen* ilmaistaksesi, hyväksytäänkö vai hylätäänkö testi, jos sen hyväksyttävän laadun taso ei täyty.</span><span class="sxs-lookup"><span data-stu-id="04522-205">**Action on failure** – Select either *Accept* or *Fail* to indicate whether the test should pass or fail if the AQL for it isn't met.</span></span>
    - <span data-ttu-id="04522-206">**Hyväksyttävän laadun taso** – Määritä testitulosten kokonaisprosentti, joka on hyväksyttävä, jotta testi voidaan katsoa hyväksytyksi.</span><span class="sxs-lookup"><span data-stu-id="04522-206">**Acceptable quality level** – Enter the total percentage of test results that must pass for the test to be considered passed.</span></span>

1. <span data-ttu-id="04522-207">Määritä sivun alaosan **Testi**-välilehdessä seuraavat kentät:</span><span class="sxs-lookup"><span data-stu-id="04522-207">In the lower part of the page, on the **Test** tab, set the following fields:</span></span>

    - <span data-ttu-id="04522-208">**Vakio** – Määritä testitulosten odotettu summa (kokonaisluku tai murtoluku).</span><span class="sxs-lookup"><span data-stu-id="04522-208">**Standard** – Enter the amount (integer or fraction) that is expected for the test results.</span></span> <span data-ttu-id="04522-209">Syötetty arvo syötetään oletusarvon mukaan testituloksiin.</span><span class="sxs-lookup"><span data-stu-id="04522-209">The value that you enter will be entered by default in the test results.</span></span> <span data-ttu-id="04522-210">Lisäksi se syötetään automaattisesti oletusarvoksi **Minimi**- ja **Maksimi**-kenttiin.</span><span class="sxs-lookup"><span data-stu-id="04522-210">Additionally, it will automatically be entered as a default value in the **Min** and **Max** fields.</span></span>
    - <span data-ttu-id="04522-211">**Minimi** – Määritä testitulosten pienin sallittu arvo.</span><span class="sxs-lookup"><span data-stu-id="04522-211">**Min** – Enter the minimum allowed value for the test results.</span></span> <span data-ttu-id="04522-212">Kirjoitettavan arvon on oltava pienempi kuin **Vakio**-kentässä määritetty summa.</span><span class="sxs-lookup"><span data-stu-id="04522-212">The value that you enter must be less than the amount that is set in the **Standard** field.</span></span> <span data-ttu-id="04522-213">Kun päivität **Minimi**-kentän, **Vähimmäistoleranssi (%)** -kenttä päivitetään automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="04522-213">When you update the **Min** field, the **Min tolerance (%)** field is automatically updated.</span></span> <span data-ttu-id="04522-214">Samoin kun päivität **Vähimmäistoleranssi (%)** -kentän, **Minimi**-kenttä päivitetään automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="04522-214">Likewise, when you update the **Min tolerance (%)** field, the **Min** field is automatically updated.</span></span>
    - <span data-ttu-id="04522-215">**Maksimi** – Määritä testitulosten suurin sallittu arvo.</span><span class="sxs-lookup"><span data-stu-id="04522-215">**Max** – Enter the maximum allowed value for the test results.</span></span> <span data-ttu-id="04522-216">Kirjoitettavan arvon on oltava suurempi kuin **Vakio**-kentässä määritetty summa.</span><span class="sxs-lookup"><span data-stu-id="04522-216">The value that you enter must be more than the amount that is set in the **Standard** field.</span></span> <span data-ttu-id="04522-217">Kun päivität **Maksimi**-kentän, **Enimmäistoleranssi (%)** -kenttä päivitetään automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="04522-217">When you update the **Max** field, the **Max tolerance (%)** field is automatically updated.</span></span> <span data-ttu-id="04522-218">Samoin kun päivität **Enimmäistoleranssi (%)** -kentän, **Maksimi**-kenttä päivitetään automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="04522-218">Likewise, when you update the **Max tolerance (%)** field, the **Max** field is automatically updated.</span></span>
    - <span data-ttu-id="04522-219">**Testin mittaväline** – Valitse laite, jota testissä on käytettävä.</span><span class="sxs-lookup"><span data-stu-id="04522-219">**Test instrument** – Select the device that should be used for the test.</span></span> <span data-ttu-id="04522-220">Jos testille on määritetty mittaväline, se syötetään testiryhmän testille automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="04522-220">If a test instrument is defined, it's automatically entered for the test in the test group.</span></span>

1. <span data-ttu-id="04522-221">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="04522-221">Close the page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="04522-222">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="04522-222">Additional resources</span></span>

- [<span data-ttu-id="04522-223">Laadunhallinnan testin mittavälineet</span><span class="sxs-lookup"><span data-stu-id="04522-223">Quality management test instruments</span></span>](quality-management-processes.md)
- [<span data-ttu-id="04522-224">Laadunhallinnan testit</span><span class="sxs-lookup"><span data-stu-id="04522-224">Quality management tests</span></span>](quality-management-processes.md)
- [<span data-ttu-id="04522-225">Laadunhallinnan testimuuttujat</span><span class="sxs-lookup"><span data-stu-id="04522-225">Quality management test variables</span></span>](quality-management-processes.md)
- [<span data-ttu-id="04522-226">Laatuliitokset</span><span class="sxs-lookup"><span data-stu-id="04522-226">Quality associations</span></span>](quality-management-processes.md)
- [<span data-ttu-id="04522-227">Erämääritteet</span><span class="sxs-lookup"><span data-stu-id="04522-227">Batch attributes</span></span>](/supply-chain/production-control/batch-attributes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]