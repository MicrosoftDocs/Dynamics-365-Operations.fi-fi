---
title: Nimikkeen laaturyhmät
description: Tässä aiheessa kuvataan, kuinka ja luodaan nimikkeiden laaturyhmiä tuotteiden loogiseen ryhmittelemiseen siten, että ne voidaan liittää laatuliitoksiin laatutilausten automaattista luontia varten.
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestQualityGroup, InventTestItemQualityGroup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 272cb748e0a2722d9744fe6b357d767a1d6aeb26
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022249"
---
# <a name="item-quality-groups"></a><span data-ttu-id="7fda8-103">Nimikkeen laaturyhmät</span><span class="sxs-lookup"><span data-stu-id="7fda8-103">Item quality groups</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7fda8-104">Laaturyhmän avulla voidaan määrittää nimikkeiden yhteisiä testausvaatimuksia.</span><span class="sxs-lookup"><span data-stu-id="7fda8-104">A quality group represents common testing requirements for items.</span></span> <span data-ttu-id="7fda8-105">Tässä aiheessa kuvataan, kuinka ja luodaan nimikkeiden laaturyhmiä tuotteiden loogiseen ryhmittelemiseen siten, että ne voidaan liittää laatuliitoksiin laatutilausten automaattista luontia varten.</span><span class="sxs-lookup"><span data-stu-id="7fda8-105">This topic describes how to use and create item quality groups to logically group products so that they can be assigned to quality associations for the automatic generation of quality orders.</span></span>

<span data-ttu-id="7fda8-106">Voit määrittää, muokata ja tarkastella nimikkeitä, jotka on määritetty nimikkeelle määritettyihin laaturyhmiin, valitsemalla **Varastonhallinta \> Asetukset \> Laaturyhmät**.</span><span class="sxs-lookup"><span data-stu-id="7fda8-106">To set up, edit, and view the items that are assigned to a quality group, or the quality groups that are assigned to an item, go to **Inventory management \> Setup \> Quality groups**.</span></span> <span data-ttu-id="7fda8-107">Kun olet määrittänyt testivaatimukset **Testiryhmät**-sivulla, voit määrittää laatutilausten automaattisen luonnin säännöt.</span><span class="sxs-lookup"><span data-stu-id="7fda8-107">After you define the test requirements on the **Test groups** page, you can define the rules for automatically generating quality orders.</span></span> <span data-ttu-id="7fda8-108">Prosessin yksinkertaistamiseksi sääntöjä ei määritetä yksittäisille nimikkeille.</span><span class="sxs-lookup"><span data-stu-id="7fda8-108">To simplify the process, you don't define rules for individual items.</span></span> <span data-ttu-id="7fda8-109">Sen sijaan **Laatuliitokset**-sivulla määritetään laaturyhmän säännöt.</span><span class="sxs-lookup"><span data-stu-id="7fda8-109">Instead, you can define the rules for a quality group on the **Quality associations** page.</span></span>

## <a name="example-of-an-item-quality-group"></a><span data-ttu-id="7fda8-110">Esimerkki nimikkeen laaturyhmästä</span><span class="sxs-lookup"><span data-stu-id="7fda8-110">Example of an item quality group</span></span>

<span data-ttu-id="7fda8-111">Teollisuusyritys ostaa useita eri raaka-aineita, joilla on samat testausvaatimukset tulevaa tarkistusta varten.</span><span class="sxs-lookup"><span data-stu-id="7fda8-111">A manufacturing company purchases various raw materials that have the same testing requirements for incoming inspection.</span></span> <span data-ttu-id="7fda8-112">Siksi yritys määrittää ensin laaturyhmän ja sitten nimiketunnukset, jotka liittyvät kyseisen ryhmän raaka-aineisiin.</span><span class="sxs-lookup"><span data-stu-id="7fda8-112">Therefore, the company defines a quality group and then assigns the item numbers that are associated with the raw materials to that group.</span></span> <span data-ttu-id="7fda8-113">Yritys ostaa myöhemmin uutta raaka-ainetta, jolla on samat testausvaatimukset.</span><span class="sxs-lookup"><span data-stu-id="7fda8-113">Later, the company purchases a new type of raw material that has the same testing requirements.</span></span> <span data-ttu-id="7fda8-114">Yritys ei määritä uudelle raaka-aineelle uusia testausvaatimuksia vaan lisää uuden materiaalin nimiketunnuksen aiemmin luotuun laaturyhmään.</span><span class="sxs-lookup"><span data-stu-id="7fda8-114">Instead of setting up new testing requirements for the new material, the company adds the item number for the new material to the existing quality group.</span></span>

<span data-ttu-id="7fda8-115">Sama yritys myös tuottaa nimikkeitä, joilla on samat tuotannon testausvaatimukset, sekä lähettää nimikkeitä, joilla on samat vaatimukset lähetystä edeltävien testien suorittamiseksi.</span><span class="sxs-lookup"><span data-stu-id="7fda8-115">The same company also produces items that have the same production testing requirements and ships items that have the same requirement for pre-shipment testing.</span></span> <span data-ttu-id="7fda8-116">Siksi yritys määrittää ensin kaksi laaturyhmää lisää ja sitten kumpaankin soveltuvat nimiketunnukset.</span><span class="sxs-lookup"><span data-stu-id="7fda8-116">Therefore, the company defines two additional quality groups and then assigns the relevant item numbers to each group.</span></span>

## <a name="create-a-quality-group"></a><span data-ttu-id="7fda8-117">Laaturyhmän luominen</span><span class="sxs-lookup"><span data-stu-id="7fda8-117">Create a quality group</span></span>

<span data-ttu-id="7fda8-118">Voit luoda laaturyhmän seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="7fda8-118">To create a quality group, follow these steps.</span></span>

1. <span data-ttu-id="7fda8-119">Valitse **Varastonhallinta \> Asetukset \> Laadunvalvonta \> Laaturyhmät**.</span><span class="sxs-lookup"><span data-stu-id="7fda8-119">Go to **Inventory management \> Setup \> Quality control \> Quality groups**.</span></span>
1. <span data-ttu-id="7fda8-120">Lisää ruudukkoon uusi rivi valitsemalla toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="7fda8-120">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="7fda8-121">Määritä sitten uudelle rivillä seuraavat kentät:</span><span class="sxs-lookup"><span data-stu-id="7fda8-121">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="7fda8-122">**Laaturyhmä** – Määritä laaturyhmän yksilöivä tunnus tai nimi.</span><span class="sxs-lookup"><span data-stu-id="7fda8-122">**Quality group** – Enter a unique ID or name for the quality group.</span></span>
    - <span data-ttu-id="7fda8-123">**Kuvaus** – Anna laaturyhmän yksityiskohtainen kuvaus.</span><span class="sxs-lookup"><span data-stu-id="7fda8-123">**Description** – Enter a detailed description of the quality group.</span></span>

1. <span data-ttu-id="7fda8-124">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="7fda8-124">Close the page.</span></span>

## <a name="manually-add-items-to-a-quality-group"></a><span data-ttu-id="7fda8-125">Lisää nimikkeet laaturyhmään manuaalisesti</span><span class="sxs-lookup"><span data-stu-id="7fda8-125">Manually add items to a quality group</span></span>

<span data-ttu-id="7fda8-126">Voit lisätä laaturyhmään nimikkeitä manuaalisesti noudattamalla seuraavia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="7fda8-126">To manually add items to a quality group, follow these steps.</span></span>

1. <span data-ttu-id="7fda8-127">Valitse **Varastonhallinta \> Asetukset \> Laadunvalvonta \> Laaturyhmät**.</span><span class="sxs-lookup"><span data-stu-id="7fda8-127">Go to **Inventory management \> Setup \> Quality control \> Quality groups**.</span></span>
1. <span data-ttu-id="7fda8-128">Valitse laaturyhmä, johon haluat lisätä nimikkeitä.</span><span class="sxs-lookup"><span data-stu-id="7fda8-128">Select the quality group that you want to add items to.</span></span>
1. <span data-ttu-id="7fda8-129">Valitse toimintoruudussa **Nimikkeet**.</span><span class="sxs-lookup"><span data-stu-id="7fda8-129">On the Action Pane, select **Items**.</span></span>
1. <span data-ttu-id="7fda8-130">Valitse **Laaturyhmän nimikkeet** -sivulla toimintoruudussa **Uusi** lisätäksesi rivin ruudukkoon.</span><span class="sxs-lookup"><span data-stu-id="7fda8-130">On the **Items in quality groups** page, on the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="7fda8-131">Määritä sitten uudelle riville **Nimiketunnus**-kentän arvoksi lisättävä nimiketunnus.</span><span class="sxs-lookup"><span data-stu-id="7fda8-131">Then, for the new row, set the **Item number** field to the item number that you want to add.</span></span>
1. <span data-ttu-id="7fda8-132">Toista edellinen vaihe kullekin lisättävälle nimikkeelle.</span><span class="sxs-lookup"><span data-stu-id="7fda8-132">Repeat the previous step for each additional item that must be added.</span></span>
1. <span data-ttu-id="7fda8-133">Sulje sivut.</span><span class="sxs-lookup"><span data-stu-id="7fda8-133">Close the pages.</span></span>

## <a name="add-multiple-items-to-a-quality-group"></a><span data-ttu-id="7fda8-134">Lisää useita nimikkeitä laaturyhmään</span><span class="sxs-lookup"><span data-stu-id="7fda8-134">Add multiple items to a quality group</span></span>

<span data-ttu-id="7fda8-135">Voit lisätä laaturyhmään useita nimikkeitä noudattamalla seuraavia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="7fda8-135">To add multiple items to a quality group, follow these steps.</span></span>

1. <span data-ttu-id="7fda8-136">Valitse **Varastonhallinta \> Asetukset \> Laadunvalvonta \> Laaturyhmät**.</span><span class="sxs-lookup"><span data-stu-id="7fda8-136">Go to **Inventory management \> Setup \> Quality control \> Quality groups**.</span></span>
1. <span data-ttu-id="7fda8-137">Luo tai valitse laaturyhmä, johon haluat lisätä nimikkeitä.</span><span class="sxs-lookup"><span data-stu-id="7fda8-137">Create or select the quality group that you want to add items to.</span></span>
1. <span data-ttu-id="7fda8-138">Valitse toimintoruudussa **Lisää nimikkeitä**.</span><span class="sxs-lookup"><span data-stu-id="7fda8-138">On the Action Pane, select **Add items**.</span></span>
1. <span data-ttu-id="7fda8-139">Anna lisättävien nimikkeiden suodatusehdot **Kysely**-valintaikkunaan.</span><span class="sxs-lookup"><span data-stu-id="7fda8-139">In the **Inquiry** dialog box, enter the filter criteria for the items that you want to add.</span></span> <span data-ttu-id="7fda8-140">Voit esimerkiksi suodattaa tietyn nimikeryhmän kaikki nimikkeet.</span><span class="sxs-lookup"><span data-stu-id="7fda8-140">For example, you might filter for all items in a specific item group.</span></span>
1. <span data-ttu-id="7fda8-141">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="7fda8-141">Select **OK**.</span></span>
1. <span data-ttu-id="7fda8-142">**Lisää nimikkeitä** -valintaikkunassa ruudukko näyttää kaikki kyselyä vastaavat nimikkeet.</span><span class="sxs-lookup"><span data-stu-id="7fda8-142">In the **Add items** dialog box, a grid shows all the items that match your query.</span></span> <span data-ttu-id="7fda8-143">Tarkastele tuloksia.</span><span class="sxs-lookup"><span data-stu-id="7fda8-143">Review the results.</span></span>

    <span data-ttu-id="7fda8-144">Jos muutoksia tarvitaan, valitse **Valitse** palataksesi **Kysely**-valintaikkunaan ja muokkaa kyselyä.</span><span class="sxs-lookup"><span data-stu-id="7fda8-144">If any changes are required, select **Select** to return to the **Inquiry** dialog box, and adjust your query.</span></span>

1. <span data-ttu-id="7fda8-145">Kun tulokset sisältävät kaikki lisättävät nimikkeet, valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="7fda8-145">When the results include all the items that you want to add, select **OK**.</span></span>
1. <span data-ttu-id="7fda8-146">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="7fda8-146">Close the page.</span></span>

## <a name="manually-associate-an-item-with-a-quality-group"></a><span data-ttu-id="7fda8-147">Nimikkeen liittäminen laaturyhmään manuaalisesti</span><span class="sxs-lookup"><span data-stu-id="7fda8-147">Manually associate an item with a quality group</span></span>

<span data-ttu-id="7fda8-148">Voit liittää laaturyhmään nimikkeen manuaalisesti noudattamalla seuraavia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="7fda8-148">To manually associate an item with a quality group, follow these steps.</span></span>

1. <span data-ttu-id="7fda8-149">Valitse **Varastonhallinta \> Asetukset \> Laadunvalvonta \> Nimikkeen laaturyhmät**.</span><span class="sxs-lookup"><span data-stu-id="7fda8-149">Go to **Inventory management \> Setup \> Quality control \> Item quality groups**.</span></span>
1. <span data-ttu-id="7fda8-150">Lisää ruudukkoon uusi rivi valitsemalla toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="7fda8-150">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="7fda8-151">Määritä sitten uudelle rivillä seuraavat kentät:</span><span class="sxs-lookup"><span data-stu-id="7fda8-151">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="7fda8-152">**Nimiketunnus** – Valitse lisättävä nimiketunnus.</span><span class="sxs-lookup"><span data-stu-id="7fda8-152">**Item number** – Select the item number to add.</span></span>
    - <span data-ttu-id="7fda8-153">**Laaturyhmä** – Valitse nimikkeeseen määritettävä laaturyhmä.</span><span class="sxs-lookup"><span data-stu-id="7fda8-153">**Quality group** – Select the quality group to assign to the item.</span></span>

1. <span data-ttu-id="7fda8-154">Toista edellinen vaihe kullekin nimikkeen lisäyhdistelmälle ja lisättävälle laaturyhmälle.</span><span class="sxs-lookup"><span data-stu-id="7fda8-154">Repeat the previous step for each additional combination of an item and a quality group that must be added.</span></span>
1. <span data-ttu-id="7fda8-155">Sulje sivut.</span><span class="sxs-lookup"><span data-stu-id="7fda8-155">Close the pages.</span></span>

## <a name="manually-add-a-quality-group-from-the-released-products-page"></a><span data-ttu-id="7fda8-156">Laaturyhmän lisääminen manuaalisesti Vapautetut tuotteet -sivulta</span><span class="sxs-lookup"><span data-stu-id="7fda8-156">Manually add a quality group from the Released products page</span></span>

<span data-ttu-id="7fda8-157">Laaturyhmän lisäämiseksi manuaalisesti **Vapautetut tuotteet** -sivulta noudata näitä vaiheita.</span><span class="sxs-lookup"><span data-stu-id="7fda8-157">To manually add a quality group from the **Released products** page, follow these steps.</span></span>

1. <span data-ttu-id="7fda8-158">Mene **Tuotetietojen hallinta \> Tuotteet \> Vapautetut tuotteet**.</span><span class="sxs-lookup"><span data-stu-id="7fda8-158">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="7fda8-159">Valitse tuote, johon haluat liittää laaturyhmän.</span><span class="sxs-lookup"><span data-stu-id="7fda8-159">Select the product that you want to assign a quality group to.</span></span>
1. <span data-ttu-id="7fda8-160">Valitse toimintoruudun **Varastonhallinta**-välilehden **Laatu**-ryhmässä **Nimikkeen laaturyhmät**.</span><span class="sxs-lookup"><span data-stu-id="7fda8-160">On the Action Pane, on the **Manage inventory** tab, in the **Quality** group, select **Item quality groups**.</span></span>
1. <span data-ttu-id="7fda8-161">Valitse **Laaturyhmän nimikkeet** -sivulla toimintoruudussa **Uusi** lisätäksesi rivin ruudukkoon.</span><span class="sxs-lookup"><span data-stu-id="7fda8-161">On the **Items in quality groups** page, on the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="7fda8-162">Määritä sitten uudelle riville **Laaturyhmä**-kentän arvoksi laaturyhmä, jonka haluat määrittää tuotteeseen.</span><span class="sxs-lookup"><span data-stu-id="7fda8-162">Then, for the new row, set the **Quality group** field to the quality group that you want to assign to the product.</span></span>
1. <span data-ttu-id="7fda8-163">Toista edellinen vaihe kunkin tuotteeseen määritettävän laaturyhmän osalta.</span><span class="sxs-lookup"><span data-stu-id="7fda8-163">Repeat the previous step for each additional quality group that you want to assign to the product.</span></span>
1. <span data-ttu-id="7fda8-164">Sulje sivut.</span><span class="sxs-lookup"><span data-stu-id="7fda8-164">Close the pages.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7fda8-165">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="7fda8-165">Additional resources</span></span>

- [<span data-ttu-id="7fda8-166">Laadunhallinnan testin mittavälineet</span><span class="sxs-lookup"><span data-stu-id="7fda8-166">Quality management test instruments</span></span>](quality-test-instruments.md)
- [<span data-ttu-id="7fda8-167">Laadunhallinnan testit</span><span class="sxs-lookup"><span data-stu-id="7fda8-167">Quality management tests</span></span>](quality-tests.md)
- [<span data-ttu-id="7fda8-168">Laadunhallinnan testiryhmät</span><span class="sxs-lookup"><span data-stu-id="7fda8-168">Quality management test groups</span></span>](quality-test-groups.md)
- [<span data-ttu-id="7fda8-169">Laadunhallinnan testimuuttujat</span><span class="sxs-lookup"><span data-stu-id="7fda8-169">Quality management test variables</span></span>](quality-test-variables.md)
- [<span data-ttu-id="7fda8-170">Laatuliitokset</span><span class="sxs-lookup"><span data-stu-id="7fda8-170">Quality associations</span></span>](quality-associations.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
