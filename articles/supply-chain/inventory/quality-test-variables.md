---
title: Laadunhallinnan testimuuttujat
description: Tässä aiheessa kuvataan, kuinka luodaan testimuuttujia, joita voidaan käyttää laadullisissa testeissä Microsoft Dynamics 365 Supply Chain Managementissa.
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b5102d09f5762a390d6fd3aadafcb2ed23820982
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021705"
---
# <a name="quality-management-test-variables"></a><span data-ttu-id="f376e-103">Laadunhallinnan testimuuttujat</span><span class="sxs-lookup"><span data-stu-id="f376e-103">Quality management test variables</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f376e-104">Tässä aiheessa kuvataan, kuinka luodaan testimuuttujia, joita voidaan käyttää laadullisissa testeissä Microsoft Dynamics 365 Supply Chain Managementissa.</span><span class="sxs-lookup"><span data-stu-id="f376e-104">This topic describes how to create test variables that can be used for qualitative tests on quality orders in Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="f376e-105">Jokaiselle **Testit**-sivulla määritetylle laadulliselle testille on määritettävä testimuuttuja ja mahdolliset tulokset.</span><span class="sxs-lookup"><span data-stu-id="f376e-105">For every qualitative test that is defined on the **Tests** page, you must define a test variable and its possible outcomes (results).</span></span> <span data-ttu-id="f376e-106">(Laadullisten testien kohdalla **Tyyppi**-kentän asetuksena **Testit**-sivulla on *Asetus*.)</span><span class="sxs-lookup"><span data-stu-id="f376e-106">(For qualitative tests, the **Type** field on the **Tests** page is set to *Option*.)</span></span>

<span data-ttu-id="f376e-107">Voit määrittää, muokata ja tarkastella **Testimuuttujat**-sivulla laadulliseen testiin liittyvän testimuuttujan mahdollisia tuloksia.</span><span class="sxs-lookup"><span data-stu-id="f376e-107">You use the **Test variables** page to set up, edit, and view the possible outcomes for a test variable that is associated with a qualitative test.</span></span> <span data-ttu-id="f376e-108">Määritä kunkin tuloksen tulostilaksi joko *Hyväksytty* tai *Epäonnistuminen*. Näin ilmaistaan, hyväksytäänkö tai hylätäänkö testi, kun tulos valitaan testitulokseksi.</span><span class="sxs-lookup"><span data-stu-id="f376e-108">For each outcome, you assign an outcome status of either *Pass* or *Fail* to indicate whether the test is passed or failed when that outcome is selected as a test result.</span></span> <span data-ttu-id="f376e-109">Määritä yksittäisen laadullisen testin testimuuttuja ja oletustulos **Testiryhmät**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="f376e-109">You use the **Test groups** page to assign a test variable and a default outcome for it to an individual qualitative test.</span></span>

<span data-ttu-id="f376e-110">Jokaiselle testimuuttujalle on suositeltavaa määrittää vähintään kaksi tulosta: yksi, jonka tulostilana on *Hyväksytty*, ja yksi, jonka tulostilana on *Epäonnistuminen*.</span><span class="sxs-lookup"><span data-stu-id="f376e-110">For every test variable, we recommend that you define at least two outcomes: one that has an outcome status of *Pass* and one that has an outcome status of *Fail*.</span></span> <span data-ttu-id="f376e-111">Määritettävien muuttujien tai tulosten kokonaismäärää ei ole rajoitettu.</span><span class="sxs-lookup"><span data-stu-id="f376e-111">There is no limit on the total number of variables or outcomes that can be defined.</span></span> <span data-ttu-id="f376e-112">Lisäksi useat testit voivat käyttää samoja testimuuttujia tulosten kirjaamiseksi.</span><span class="sxs-lookup"><span data-stu-id="f376e-112">Additionally, multiple tests can use the same test variables to record results.</span></span>

## <a name="examples-of-test-variables"></a><span data-ttu-id="f376e-113">Esimerkkejä testimuuttujista</span><span class="sxs-lookup"><span data-stu-id="f376e-113">Examples of test variables</span></span>

### <a name="example-1"></a><span data-ttu-id="f376e-114">Esimerkki 1</span><span class="sxs-lookup"><span data-stu-id="f376e-114">Example 1</span></span>

<span data-ttu-id="f376e-115">Teollisuusyritys suorittaa kaksi testiä valmistetuille materiaaleille.</span><span class="sxs-lookup"><span data-stu-id="f376e-115">A manufacturing company performs two tests on manufactured materials.</span></span> <span data-ttu-id="f376e-116">Yhdessä testissä pH-taso liitetään värinauhaan.</span><span class="sxs-lookup"><span data-stu-id="f376e-116">In one test, the pH level is associated with a color strip.</span></span> <span data-ttu-id="f376e-117">Hyväksyttävät pH-tasot ovat vaaleampia, ja hylätyt pH-tasot ovat tummempia.</span><span class="sxs-lookup"><span data-stu-id="f376e-117">Acceptable pH levels are in lighter colors, and unacceptable pH levels are in darker colors.</span></span> <span data-ttu-id="f376e-118">Toisessa testissä suoritetaan useita visuaalisia tarkastuksia, ja laatutyöntekijät määrittävät, läpäiseekö nimike visuaalisen tarkastuksen vai ei.</span><span class="sxs-lookup"><span data-stu-id="f376e-118">In another test, multiple visual inspections are performed, and quality workers use their judgement to determine whether the item passes or fails the visual inspection.</span></span>

### <a name="example-2"></a><span data-ttu-id="f376e-119">Esimerkki 2</span><span class="sxs-lookup"><span data-stu-id="f376e-119">Example 2</span></span>

<span data-ttu-id="f376e-120">Pikkuleipiä valmistava teollisuusyritys tarkastaa lopputuotteen testillä.</span><span class="sxs-lookup"><span data-stu-id="f376e-120">A manufacturing company that produces cookies uses an inspection test for the finished product.</span></span> <span data-ttu-id="f376e-121">Tarkastuksessa on useita muuttujia.</span><span class="sxs-lookup"><span data-stu-id="f376e-121">This inspection test has several variables.</span></span> <span data-ttu-id="f376e-122">Ensimmäinen muuttuja on maku, jonka mahdollisia tuloksia ovat hyvä ja paha.</span><span class="sxs-lookup"><span data-stu-id="f376e-122">One variable is taste, and the possible outcomes for it are good and bad.</span></span> <span data-ttu-id="f376e-123">Toinen muuttuja on väri, jonka mahdollisia tuloksia ovat liian tumma, liian vaalea ja oikea.</span><span class="sxs-lookup"><span data-stu-id="f376e-123">A second variable is color, and the possible outcomes for it are too dark, too light, and correct.</span></span>

## <a name="create-a-test-variable"></a><span data-ttu-id="f376e-124">Testimuuttujan luominen</span><span class="sxs-lookup"><span data-stu-id="f376e-124">Create a test variable</span></span>

<span data-ttu-id="f376e-125">Voit luoda testimuuttujan seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="f376e-125">Follow these steps to create a test variable.</span></span>

1. <span data-ttu-id="f376e-126">Valitse **Varastonhallinta \> Asetukset \> Laadunvalvonta \> Testimuuttujat**.</span><span class="sxs-lookup"><span data-stu-id="f376e-126">Go to **Inventory management \> Setup \> Quality control \> Test variables**.</span></span>
1. <span data-ttu-id="f376e-127">Lisää ruudukkoon uusi rivi valitsemalla toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="f376e-127">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="f376e-128">Määritä sitten uudelle rivillä seuraavat kentät:</span><span class="sxs-lookup"><span data-stu-id="f376e-128">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="f376e-129">**Muuttuja** – Määritä muuttujan yksilöivä tunnus tai nimi.</span><span class="sxs-lookup"><span data-stu-id="f376e-129">**Variable** – Enter a unique ID or name for the variable.</span></span>
    - <span data-ttu-id="f376e-130">**Kuvaus** – Anna muuttujan yksityiskohtainen kuvaus.</span><span class="sxs-lookup"><span data-stu-id="f376e-130">**Description** – Enter a detailed description of the variable.</span></span>

1. <span data-ttu-id="f376e-131">Kun uusi rivi on vielä valittuna, valitse **Tulokset** toimintoruudusta.</span><span class="sxs-lookup"><span data-stu-id="f376e-131">While the new row is still selected, select **Outcomes** on the Action Pane.</span></span>
1. <span data-ttu-id="f376e-132">Valitse **Testimuuttujien tulokset** -sivulla toimintoruudussa **Uusi** lisätäksesi rivin ruudukkoon.</span><span class="sxs-lookup"><span data-stu-id="f376e-132">On the **Test variable outcomes** page, on the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="f376e-133">Määritä sitten uudelle rivillä seuraavat kentät:</span><span class="sxs-lookup"><span data-stu-id="f376e-133">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="f376e-134">**Tulos** – Määritä tuloksen yksilöivä tunnus tai nimi.</span><span class="sxs-lookup"><span data-stu-id="f376e-134">**Outcome** – Enter a unique ID or name for the outcome.</span></span>
    - <span data-ttu-id="f376e-135">**Kuvaus** – Anna tuloksen yksityiskohtainen kuvaus.</span><span class="sxs-lookup"><span data-stu-id="f376e-135">**Description** – Enter a detailed description of the outcome.</span></span>
    - <span data-ttu-id="f376e-136">**Tuloksen tila** – Valitse joko *Hyväksytty* tai *Epäonnistuminen*. Näin ilmaistaan, hyväksytäänkö tai hylätäänkö testi, kun tulos valitaan testitulokseksi.</span><span class="sxs-lookup"><span data-stu-id="f376e-136">**Outcome status** – Select either *Pass* or *Fail* to indicate whether the test is passed or failed when the outcome is selected as a test result.</span></span>

1. <span data-ttu-id="f376e-137">Toista edellinen vaihe kullekin lisätulokselle.</span><span class="sxs-lookup"><span data-stu-id="f376e-137">Repeat the previous step for each additional outcome.</span></span> <span data-ttu-id="f376e-138">Varmista, että vähintään yhden tuloksen tilana on *Hyväksytty* ja vähintään yhden tilana on *Epäonnistuminen*.</span><span class="sxs-lookup"><span data-stu-id="f376e-138">Make sure that at least one outcome has an outcome status of *Pass* and at least one has an outcome status of *Fail*.</span></span>
1. <span data-ttu-id="f376e-139">Sulje sivut.</span><span class="sxs-lookup"><span data-stu-id="f376e-139">Close the pages.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f376e-140">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="f376e-140">Additional resources</span></span>

- [<span data-ttu-id="f376e-141">Laadunhallinnan testin mittavälineet</span><span class="sxs-lookup"><span data-stu-id="f376e-141">Quality management test instruments</span></span>](quality-test-instruments.md)
- [<span data-ttu-id="f376e-142">Laadunhallinnan testit</span><span class="sxs-lookup"><span data-stu-id="f376e-142">Quality management tests</span></span>](quality-tests.md)
- [<span data-ttu-id="f376e-143">Laadunhallinnan testiryhmät</span><span class="sxs-lookup"><span data-stu-id="f376e-143">Quality management test groups</span></span>](quality-test-groups.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
