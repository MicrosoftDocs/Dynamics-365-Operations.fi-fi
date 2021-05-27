---
title: Laadunhallinnan testit
description: Tässä aiheessa kuvataan, kuinka luodaan testejä, joita voidaan käyttää laatutilauksissa Microsoft Dynamics 365 Supply Chain Managementissa.
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
ms.openlocfilehash: 95f759d051a520b577cb1cf3d595ce64e0dc4668
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021681"
---
# <a name="quality-management-tests"></a><span data-ttu-id="c6b17-103">Laadunhallinnan testit</span><span class="sxs-lookup"><span data-stu-id="c6b17-103">Quality management tests</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c6b17-104">Tässä aiheessa kuvataan, kuinka luodaan testejä, joita voidaan käyttää laatutilauksissa Microsoft Dynamics 365 Supply Chain Managementissa.</span><span class="sxs-lookup"><span data-stu-id="c6b17-104">This topic describes how to create tests that can be used for quality orders in Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="c6b17-105">Voit määrittää ja tarkastella **Testit**-sivulla yksittäisiä testejä, joiden mukaan määräytyy, ovatko tuotteet laatuvaatimusten mukaisia.</span><span class="sxs-lookup"><span data-stu-id="c6b17-105">You use the **Tests** page to define and view the individual tests that determine whether your products meet quality specifications.</span></span> <span data-ttu-id="c6b17-106">Voit määrittää testiryhmälle vähintään yhden yksittäisen testin.</span><span class="sxs-lookup"><span data-stu-id="c6b17-106">You can assign one or more individual tests to a test group.</span></span> <span data-ttu-id="c6b17-107">Siinä tapauksessa määrität myös testikohtaiset tiedot, kuten hyväksyttävät mitta-arvot.</span><span class="sxs-lookup"><span data-stu-id="c6b17-107">In this case, you also specify test-specific information, such as the acceptable measurement values.</span></span> <span data-ttu-id="c6b17-108">Mitta-arvoja käytetään määrällisissä testeissä.</span><span class="sxs-lookup"><span data-stu-id="c6b17-108">Measurement values are used for quantitative tests.</span></span> <span data-ttu-id="c6b17-109">Laadullisia testejä varten käytetään testimuuttujia.</span><span class="sxs-lookup"><span data-stu-id="c6b17-109">For qualitative tests, test variables are used.</span></span>

- <span data-ttu-id="c6b17-110">Määrällisissä testeissä **Tyyppi**-kentän arvoksi on määritetty *Kokonaisluku* tai *Murtoluku*.</span><span class="sxs-lookup"><span data-stu-id="c6b17-110">For quantitative tests, the **Type** field is set to *Integer* or *Fraction*.</span></span> <span data-ttu-id="c6b17-111">Myös mittayksikkö määritetään.</span><span class="sxs-lookup"><span data-stu-id="c6b17-111">A unit of measure is also specified.</span></span> <span data-ttu-id="c6b17-112">Laatumääritykset ja testitulokset ilmaistaan numeroina.</span><span class="sxs-lookup"><span data-stu-id="c6b17-112">Quality specifications and test results are expressed as numbers.</span></span>
- <span data-ttu-id="c6b17-113">Laadullisissa testeissä **Tyyppin**-kentän asetuksena on *Asetus*.</span><span class="sxs-lookup"><span data-stu-id="c6b17-113">For qualitative tests, the **Type** field is set to *Option*.</span></span> <span data-ttu-id="c6b17-114">Laadullista testiä varten tarvitaan lisätietoja mitattavasta testimuuttujasta ja sen numeroiduista vaihtoehdoista.</span><span class="sxs-lookup"><span data-stu-id="c6b17-114">Qualitative tests require additional information about the test variable that is being measured and its enumerated options.</span></span> <span data-ttu-id="c6b17-115">Laatumääritykset ja testitulokset ilmaistaan tuloksen perusteella.</span><span class="sxs-lookup"><span data-stu-id="c6b17-115">Quality specifications and test results are expressed according to an outcome.</span></span>

<span data-ttu-id="c6b17-116">Voit määrittää testille myös testin mittavälineen.</span><span class="sxs-lookup"><span data-stu-id="c6b17-116">You can optionally assign a test instrument to a test.</span></span> <span data-ttu-id="c6b17-117">Testin mittavälineitä ei kuitenkaan tarvita laatutilausten testien luomiseen ja käyttöön.</span><span class="sxs-lookup"><span data-stu-id="c6b17-117">However, test instruments aren't required to create and use tests with quality orders.</span></span> <span data-ttu-id="c6b17-118">Lisätietoja on kohdassa [Laadunhallinnan testin mittavälineet](quality-test-instruments.md).</span><span class="sxs-lookup"><span data-stu-id="c6b17-118">For more information, see [Quality management test instruments](quality-test-instruments.md).</span></span>

<span data-ttu-id="c6b17-119">Voit myös halutessasi määrittää testille yksikön, joka ilmaisee, missä mittayksikössä testitulokset kirjataan.</span><span class="sxs-lookup"><span data-stu-id="c6b17-119">You can also optionally specify a unit for a test, to indicate the unit of measure that test results are recorded in.</span></span> <span data-ttu-id="c6b17-120">Esimerkiksi lämpötilatesti voi sisältää yksikön joko Fahrenheit- tai Celsius-asteina.</span><span class="sxs-lookup"><span data-stu-id="c6b17-120">For example, a test for temperature might include a unit of either degrees Fahrenheit or degrees Celsius.</span></span>

## <a name="example-of-a-test"></a><span data-ttu-id="c6b17-121">Esimerkki testistä</span><span class="sxs-lookup"><span data-stu-id="c6b17-121">Example of a test</span></span>

<span data-ttu-id="c6b17-122">Teollisuusyritys suorittaa ostamalleen materiaalille kaksi testiä: materiaalin laatua koskevan määrällisen testin ja pakkausvahinkoja koskevan laadullisen testin.</span><span class="sxs-lookup"><span data-stu-id="c6b17-122">A manufacturing company performs two tests on purchased material: a quantitative test for material quality and a qualitative test for packaging damage.</span></span> <span data-ttu-id="c6b17-123">Yritys määrittää laadullisen testin lisätiedoiksi testimuuttujan (esimerkiksi vioittunut pakkaus) ja sen mahdolliset tulokset.</span><span class="sxs-lookup"><span data-stu-id="c6b17-123">The company specifies additional information about the qualitative test to define the test variable (for example, damaged packaging) and its outcomes.</span></span> <span data-ttu-id="c6b17-124">Yritys määrittää **Testiryhmät**-sivulla kaksi testiä testiryhmään. Lisäksi testikohtaiset tiedot määritetään.</span><span class="sxs-lookup"><span data-stu-id="c6b17-124">The company uses the **Test groups** page to assign the two tests to a test group and to specify the test-specific information.</span></span> <span data-ttu-id="c6b17-125">Testiryhmä määritetään laatutilaukseen, jotta yritys voi raportoida näiden kahden testin testitulokset.</span><span class="sxs-lookup"><span data-stu-id="c6b17-125">The test group is assigned to a quality order so that the company can report test results for the two tests.</span></span>

## <a name="create-a-test"></a><span data-ttu-id="c6b17-126">Testin luominen</span><span class="sxs-lookup"><span data-stu-id="c6b17-126">Create a test</span></span>

<span data-ttu-id="c6b17-127">Luo testi seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="c6b17-127">Follow these steps to create a test.</span></span>

1. <span data-ttu-id="c6b17-128">Valitse **Varastonhallinta \> Asetukset \> Laadunvalvonta \> Testit**.</span><span class="sxs-lookup"><span data-stu-id="c6b17-128">Go to **Inventory management \> Setup \> Quality control \> Tests**.</span></span>
1. <span data-ttu-id="c6b17-129">Lisää ruudukkoon uusi rivi valitsemalla toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="c6b17-129">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="c6b17-130">Määritä sitten uudelle rivillä seuraavat kentät:</span><span class="sxs-lookup"><span data-stu-id="c6b17-130">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="c6b17-131">**Testi** – Määritä testin yksilöivä tunnus tai nimi.</span><span class="sxs-lookup"><span data-stu-id="c6b17-131">**Test** – Enter a unique ID or name for the test.</span></span>
    - <span data-ttu-id="c6b17-132">**Kuvaus** – Anna testin yksityiskohtainen kuvaus.</span><span class="sxs-lookup"><span data-stu-id="c6b17-132">**Description** – Enter a detailed description of the test.</span></span>
    - <span data-ttu-id="c6b17-133">**Tyyppi** – Valitse testin tuottamien tulosten tyyppi.</span><span class="sxs-lookup"><span data-stu-id="c6b17-133">**Type** – Select the type of results that the test produces.</span></span> <span data-ttu-id="c6b17-134">Valitse määrällisissä testeissä *Murtoluku* tai *Kokonaisluku*.</span><span class="sxs-lookup"><span data-stu-id="c6b17-134">For quantitative tests, select *Fraction* or *Integer*.</span></span> <span data-ttu-id="c6b17-135">Valitse laadullisia testejä varten *Asetus*.</span><span class="sxs-lookup"><span data-stu-id="c6b17-135">For qualitative tests, select *Option*.</span></span>
    - <span data-ttu-id="c6b17-136">**Testin mittaväline** – Valitse [testin mittaväline](quality-test-instruments.md), jota testissä on käytettävä.</span><span class="sxs-lookup"><span data-stu-id="c6b17-136">**Test instrument** – Select a [test instrument](quality-test-instruments.md) that should be used for the test.</span></span>
    - <span data-ttu-id="c6b17-137">**Yksikkö** – Jos valitsit **Tyyppi**-kentässä *Murtoluku* tai *Kokonaisluku* (jos testi on määrällinen testi), valitse mittayksikkö, jossa testitulokset kirjataan.</span><span class="sxs-lookup"><span data-stu-id="c6b17-137">**Unit** – If you selected *Fraction* or *Integer* in the **Type** field (that is, if the test is a quantitative test), select the unit of measure that test results should be recorded in.</span></span>

1. <span data-ttu-id="c6b17-138">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="c6b17-138">Close the page.</span></span>

> [!NOTE]
> <span data-ttu-id="c6b17-139">Kun olet tallentanut testin, et voi enää muokata ruudukon **Tyyppi**-kenttää.</span><span class="sxs-lookup"><span data-stu-id="c6b17-139">After you save a test, you can no longer edit the **Type** field in the grid.</span></span> <span data-ttu-id="c6b17-140">Jos testille tallennettavan testin tulosten tyyppiä on muutettava, valitse toimintoruudusta **Muuta laatutestin tyyppiä**.</span><span class="sxs-lookup"><span data-stu-id="c6b17-140">If you must change the type of test results that will be recorded for a test, select **Change quality test type** on the Action Pane.</span></span> <span data-ttu-id="c6b17-141">Määritä **Muuta laatutestin tyyppiä** -valintaikkunassa haluamasi tyyppinen **Uusi tyyppi** -kenttä ja sulje valintaikkuna valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="c6b17-141">In the **Change quality test type** dialog box, set the **New type** field to the desired type, and then select **OK** to close the dialog box.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c6b17-142">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="c6b17-142">Additional resources</span></span>

- [<span data-ttu-id="c6b17-143">Laadunhallinnan testin mittavälineet</span><span class="sxs-lookup"><span data-stu-id="c6b17-143">Quality management test instruments</span></span>](quality-test-instruments.md)
- [<span data-ttu-id="c6b17-144">Laadunhallinnan testiryhmät</span><span class="sxs-lookup"><span data-stu-id="c6b17-144">Quality management test groups</span></span>](quality-test-groups.md)
- [<span data-ttu-id="c6b17-145">Laadunhallinnan testimuuttujat</span><span class="sxs-lookup"><span data-stu-id="c6b17-145">Quality management test variables</span></span>](quality-test-variables.md)
- [<span data-ttu-id="c6b17-146">Laatuliitokset</span><span class="sxs-lookup"><span data-stu-id="c6b17-146">Quality associations</span></span>](quality-associations.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
