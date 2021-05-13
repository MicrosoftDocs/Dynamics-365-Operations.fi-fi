---
title: Määrityksistä poikkeamisten luonti ja käsittely
description: Tässä aiheessa kerrotaan, miten voit hallita määrityksistä poikkeamisia aiemmin luodun laatutilauksen perusteella.
author: perlynne
ms.date: 03/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 06a56a694f7a80d65cb46d08744e78d8361cee3b
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956203"
---
# <a name="create-and-process-nonconformances"></a><span data-ttu-id="d55ee-103">Määrityksistä poikkeamisten luonti ja käsittely</span><span class="sxs-lookup"><span data-stu-id="d55ee-103">Create and process nonconformances</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d55ee-104">Tässä aiheessa kerrotaan, miten voit hallita määrityksistä poikkeamisia aiemmin luodun laatutilauksen perusteella.</span><span class="sxs-lookup"><span data-stu-id="d55ee-104">This topic describes how to perform nonconformance management based on an existing quality order.</span></span> <span data-ttu-id="d55ee-105">Määrityksistä poikkeamisen hallinnan hoitaa yleensä laatutyöntekijä.</span><span class="sxs-lookup"><span data-stu-id="d55ee-105">Typically, nonconformance management is done by a quality clerk.</span></span> <span data-ttu-id="d55ee-106">Edellytyksenä laatutilauksen on oltava käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="d55ee-106">As a prerequisite, you must have a quality order available.</span></span> <span data-ttu-id="d55ee-107">(Lisätietoja laatutilauksen luomisesta on kohdassa [Tarkista tavaroiden laatu](inspect-quality-goods.md).)</span><span class="sxs-lookup"><span data-stu-id="d55ee-107">(For information about how to create a quality order, see [Inspect the quality of goods](inspect-quality-goods.md).)</span></span>

<span data-ttu-id="d55ee-108">Ennen kuin käyttäjä voi käsitellä määrityksistä poikkeamisen hyväksynnän, työntekijä on liitettävä niihin **Henkilö**-kentässä **Käyttäjät**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="d55ee-108">Before a user can process the approval of a nonconformance, a worker must be assigned to them in the **Person** field on the **Users** page.</span></span> <span data-ttu-id="d55ee-109">Ennen kuin käyttäjä voi käyttää asiakirjan huomautuksia, **Ota tiedoston käsittely käyttöön** -kentän arvoksi on asetettava *Kyllä* käyttäjän asetuksissa.</span><span class="sxs-lookup"><span data-stu-id="d55ee-109">Additionally, before the user can use the document notes, the **Enable document handling** option must be set to *Yes* in their user options.</span></span>

## <a name="create-a-nonconformance"></a><span data-ttu-id="d55ee-110">Luo määrityksistä poikkeaminen</span><span class="sxs-lookup"><span data-stu-id="d55ee-110">Create a nonconformance</span></span>

<span data-ttu-id="d55ee-111">Voit luoda määrityksistä poikkeamisen seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="d55ee-111">To create a nonconformance, follow these steps.</span></span>

1. <span data-ttu-id="d55ee-112">Siirry kohtaan **Varastonhallinta \> Kausittaiset tehtävät \> Laadunhallinta \> Määrityksistä poikkeamiset**.</span><span class="sxs-lookup"><span data-stu-id="d55ee-112">Go to **Inventory management \> Periodic tasks \> Quality management \> Non conformances**.</span></span>
1. <span data-ttu-id="d55ee-113">Valitse toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="d55ee-113">On the Action pane, select **New**.</span></span>
1. <span data-ttu-id="d55ee-114">Valitse **Luo määrityksistä poikkeaminen** -valintaikkunan **Ongelman tyyppi** -kentässä ongelman tyyppi, joka löydettiin tarkastusprosessin aikana.</span><span class="sxs-lookup"><span data-stu-id="d55ee-114">In the **Create non conformance** dialog box, in **Problem type** field, select the type of problem that was found during the inspection process.</span></span>
1. <span data-ttu-id="d55ee-115">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="d55ee-115">Select **OK**.</span></span>

## <a name="approve-or-reject-a-nonconformance"></a><span data-ttu-id="d55ee-116">Hyväksy tai hylkää määrityksistä poikkeaminen</span><span class="sxs-lookup"><span data-stu-id="d55ee-116">Approve or reject a nonconformance</span></span>

<span data-ttu-id="d55ee-117">Voit hyväksyä tai hylätä määrityksistä poikkeamisen seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="d55ee-117">To approve or reject a nonconformance, follow these steps.</span></span>

1. <span data-ttu-id="d55ee-118">Siirry kohtaan **Varastonhallinta \> Kausittaiset tehtävät \> Laadunhallinta \> Määrityksistä poikkeamiset**.</span><span class="sxs-lookup"><span data-stu-id="d55ee-118">Go to **Inventory management \> Periodic tasks \> Quality management \> Non conformances**.</span></span>
1. <span data-ttu-id="d55ee-119">Etsi ja valitse luettelosta päivitettävä määrityksistä poikkeaminen.</span><span class="sxs-lookup"><span data-stu-id="d55ee-119">In the list, select the nonconformance that you want to update.</span></span>

    > [!NOTE]
    > <span data-ttu-id="d55ee-120">Voit lisätä korjauksen vain hyväksyttyihin määrityksistä poikkeamisiin.</span><span class="sxs-lookup"><span data-stu-id="d55ee-120">You can add a correction only to nonconformances that are approved.</span></span>

1. <span data-ttu-id="d55ee-121">Valitse toimintoruudussa **Toiminnot \> Hyväksy määrityksistä poikkeaminen** hyväksyäksesi määrityksistä poikkeamisen tai **Toiminnot \> Hylkää määrityksistä poikkeaminen** hylätäksesi sen.</span><span class="sxs-lookup"><span data-stu-id="d55ee-121">On the Action Pane, select **Functions \> Approve non conformance** to approve the nonconformance or **Functions \> Refuse non conformance** to reject it.</span></span> <span data-ttu-id="d55ee-122">Voit liittää hyväksytyt määrityksistä poikkeamisen [liittyviin toimintoihin](../quality-operations.md).</span><span class="sxs-lookup"><span data-stu-id="d55ee-122">You can associate approved nonconformances with [related operations](../quality-operations.md).</span></span> <span data-ttu-id="d55ee-123">Näin voit kirjata määrityksistä poikkeamisen käsittelyn ja korjauskäsittelyn osana tehtyä työtä.</span><span class="sxs-lookup"><span data-stu-id="d55ee-123">In this way, you can record work that is done as part of the nonconformance handling and the processing of correction handling.</span></span>
1. <span data-ttu-id="d55ee-124">Järjestelmä pyytää vahvistamaan valinnan.</span><span class="sxs-lookup"><span data-stu-id="d55ee-124">You're prompted to confirm your selection.</span></span> <span data-ttu-id="d55ee-125">Jatka valitsemalla **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="d55ee-125">Select **Yes** to continue.</span></span>

## <a name="add-operations-and-other-details-to-nonconformances"></a><span data-ttu-id="d55ee-126">Toimintojen ja muiden tietojen lisääminen määrityksistä poikkeamisiin</span><span class="sxs-lookup"><span data-stu-id="d55ee-126">Add operations and other details to nonconformances</span></span>

<span data-ttu-id="d55ee-127">Kun olet luonut määrityksistä poikkeamisen, voit alkaa lisätä siihen liittyviä toimintoja ja määrittää näiden toimintojen lisätietoja.</span><span class="sxs-lookup"><span data-stu-id="d55ee-127">After you've created a nonconformance, you can start to add related operations and specify additional information about those operations.</span></span> <span data-ttu-id="d55ee-128">Voit lisätä liittyvät toiminnot vain hyväksyttyihin määrityksistä poikkeamisiin.</span><span class="sxs-lookup"><span data-stu-id="d55ee-128">You can add related operations only to nonconformances that are approved.</span></span>

<span data-ttu-id="d55ee-129">Perustietojen lisäksi voit lisätä toimintoon seuraavia tietoja:</span><span class="sxs-lookup"><span data-stu-id="d55ee-129">Besides the basic information, you can add the following details to an operation:</span></span>

- <span data-ttu-id="d55ee-130">**Nimikkeet** – Voit luoda luettelon korjauksen suorittamiseen kulutetuista nimikkeistä.</span><span class="sxs-lookup"><span data-stu-id="d55ee-130">**Items** – You can create a list of items that are consumed to perform the correction.</span></span> <span data-ttu-id="d55ee-131">Nimikkeet voivat olla esimerkiksi tuotteita, joita tarvitaan valmiin tuotteen korjausta varten tarvittavien laitteiden tai ainesosien korjaamiseen.</span><span class="sxs-lookup"><span data-stu-id="d55ee-131">For example, the items might be products that are required to repair equipment or ingredients that are required to rework a finished product.</span></span>
- <span data-ttu-id="d55ee-132">**Laatukulut** – Voit luoda luettelon kuluista, jotka syntyvät tai laskutetaan ulkoisista lähteistä.</span><span class="sxs-lookup"><span data-stu-id="d55ee-132">**Quality charges** – You can create a list of charges that are incurred or billed out to external sources.</span></span>
- <span data-ttu-id="d55ee-133">**Työaikaraportti** – Voit luoda lokin ajasta, jonka kukin työntekijä käyttää toiminnossa.</span><span class="sxs-lookup"><span data-stu-id="d55ee-133">**Timesheet** – You can create a log of the time that each worker spends on the operation.</span></span>

<span data-ttu-id="d55ee-134">Muut asetukset ovat valinnaisia.</span><span class="sxs-lookup"><span data-stu-id="d55ee-134">The remaining settings are optional.</span></span> <span data-ttu-id="d55ee-135">Kunkin nimikkeen, laatukulujen ja aikaraportin kustannukset lasketaan yhteen, ja ne näkyvät toiminnossa.</span><span class="sxs-lookup"><span data-stu-id="d55ee-135">The cost for each item, quality charges, and the timesheet are summed and shown on the operation.</span></span> <span data-ttu-id="d55ee-136">Toiminnon **Kustannus**-kenttää ei voi muokata suoraan.</span><span class="sxs-lookup"><span data-stu-id="d55ee-136">You can't directly edit the **Cost** field on the operation.</span></span>

### <a name="create-an-operation-for-a-nonconformance"></a><span data-ttu-id="d55ee-137">Toiminnon luominen määrityksistä poikkeamiselle</span><span class="sxs-lookup"><span data-stu-id="d55ee-137">Create an operation for a nonconformance</span></span>

<span data-ttu-id="d55ee-138">Voit luoda toiminnon määrityksistä poikkeamiselle seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="d55ee-138">To create an operation for a nonconformance, follow these steps.</span></span>

1. <span data-ttu-id="d55ee-139">Siirry kohtaan **Varastonhallinta \> Kausittaiset tehtävät \> Laadunhallinta \> Määrityksistä poikkeamiset**.</span><span class="sxs-lookup"><span data-stu-id="d55ee-139">Go to **Inventory management \> Periodic tasks \> Quality management \> Non conformances**.</span></span>
1. <span data-ttu-id="d55ee-140">Etsi ja valitse luettelosta päivitettävä määrityksistä poikkeaminen.</span><span class="sxs-lookup"><span data-stu-id="d55ee-140">In the list, select the nonconformance that you want to update.</span></span>

    > [!NOTE]
    > <span data-ttu-id="d55ee-141">Voit lisätä toimintoja tai päivittää niitä vain hyväksyttyihin määrityksistä poikkeamisiin.</span><span class="sxs-lookup"><span data-stu-id="d55ee-141">You can add or update operations only for nonconformances that are approved.</span></span>

1. <span data-ttu-id="d55ee-142">Valitse toimintoruudussa **Liittyvät toiminnot**.</span><span class="sxs-lookup"><span data-stu-id="d55ee-142">On the Action Pane, select **Related operations**.</span></span>
1. <span data-ttu-id="d55ee-143">Valitse **Liittyvät toiminnot** -sivulla toimintoruudussa **Uusi** lisätäksesi rivin ruudukkoon.</span><span class="sxs-lookup"><span data-stu-id="d55ee-143">On the **Related operations** page, on the Action pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="d55ee-144">Määritä sitten uudelle rivillä seuraavat kentät:</span><span class="sxs-lookup"><span data-stu-id="d55ee-144">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="d55ee-145">**Toiminto** – Valitse määrityksistä poikkeamista varten suoritettavan toiminnon koodi.</span><span class="sxs-lookup"><span data-stu-id="d55ee-145">**Operation** – Select the code of the operation that will be performed for the nonconformance.</span></span>
    - <span data-ttu-id="d55ee-146">**Syy** – Kirjoita yksityiskohtainen kuvaus, jossa kerrotaan, miksi toiminto on pakollinen.</span><span class="sxs-lookup"><span data-stu-id="d55ee-146">**Reason** – Enter a detailed description that explains why the operation is required.</span></span>
    - <span data-ttu-id="d55ee-147">**Myyntitilaus** – Jos valittu toimintokoodi liittyy myyntitilauksen tyyppiin, valitse myyntitilaus, johon linkität toiminnon.</span><span class="sxs-lookup"><span data-stu-id="d55ee-147">**Sales order** – If the selected operation code is related to the sales order type, select the sales order that you're linking the operation to.</span></span>
    - <span data-ttu-id="d55ee-148">**Ostotilaus** – Jos valittu toimintokoodi liittyy ostotilauksen tyyppiin, valitse ostotilaus, johon linkität toiminnon.</span><span class="sxs-lookup"><span data-stu-id="d55ee-148">**Purchase order** – If the selected operation code is related to the purchase order type, select the purchase order that you're linking the operation to.</span></span>

1. <span data-ttu-id="d55ee-149">Sulje sivut.</span><span class="sxs-lookup"><span data-stu-id="d55ee-149">Close the pages.</span></span>

### <a name="add-items-to-an-operation"></a><span data-ttu-id="d55ee-150">Nimikkeiden lisääminen toimintoon</span><span class="sxs-lookup"><span data-stu-id="d55ee-150">Add items to an operation</span></span>

<span data-ttu-id="d55ee-151">Voit lisätä nimikkeitä toimintoon noudattamalla seuraavia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="d55ee-151">To add items to an operation, follow these steps.</span></span>

1. <span data-ttu-id="d55ee-152">Siirry kohtaan **Varastonhallinta \> Kausittaiset tehtävät \> Laadunhallinta \> Määrityksistä poikkeamiset**.</span><span class="sxs-lookup"><span data-stu-id="d55ee-152">Go to **Inventory management \> Periodic tasks \> Quality management \> Non conformances**.</span></span>
1. <span data-ttu-id="d55ee-153">Etsi ja valitse luettelosta päivitettävä määrityksistä poikkeaminen.</span><span class="sxs-lookup"><span data-stu-id="d55ee-153">In the list, select the nonconformance that you want to update.</span></span>

    > [!NOTE]
    > <span data-ttu-id="d55ee-154">Voit lisätä toimintoja tai päivittää niitä vain hyväksyttyihin määrityksistä poikkeamisiin.</span><span class="sxs-lookup"><span data-stu-id="d55ee-154">You can add or update operations only for nonconformances that are approved.</span></span>

1. <span data-ttu-id="d55ee-155">Valitse toimintoruudussa **Liittyvät toiminnot**.</span><span class="sxs-lookup"><span data-stu-id="d55ee-155">On the Action Pane, select **Related operations**.</span></span>
1. <span data-ttu-id="d55ee-156">Valitse **Liittyvät toiminnot** -sivulla toiminto, johon haluat lisätä nimikkeitä.</span><span class="sxs-lookup"><span data-stu-id="d55ee-156">On the **Related operations** page, select the operation that you want to add items to.</span></span>
1. <span data-ttu-id="d55ee-157">Valitse toimintoruudussa **Nimikkeet**.</span><span class="sxs-lookup"><span data-stu-id="d55ee-157">On the Action Pane, select **Items**.</span></span>
1. <span data-ttu-id="d55ee-158">Valitse **Liittyvät toiminnot** -sivulla toimintoruudussa **Uusi** lisätäksesi rivin ruudukkoon.</span><span class="sxs-lookup"><span data-stu-id="d55ee-158">On the **Related operations** page, on the Action pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="d55ee-159">Määritä sitten uudelle rivillä seuraavat kentät:</span><span class="sxs-lookup"><span data-stu-id="d55ee-159">Then set the following fields for new row:</span></span>

    - <span data-ttu-id="d55ee-160">**Nimiketunnus** – Valitse tuote, joka kulutetaan osana valittua toimintoa.</span><span class="sxs-lookup"><span data-stu-id="d55ee-160">**Item number** – Select the product that will be consumed as part of the selected operation.</span></span>
    - <span data-ttu-id="d55ee-161">**Määrä** – Kirjoita kulutettava nimikemäärä.</span><span class="sxs-lookup"><span data-stu-id="d55ee-161">**Quantity** – Enter the number of items that will be consumed.</span></span>

    > [!NOTE]
    > <span data-ttu-id="d55ee-162">Voit tarkastella nimikkeen kustannusta **Kustannus**-kentässä **Yleiset**-välilehdessä. Siellä näkyvä kustannus tulee **Vapautettu tuote** -sivulla määritettyjen kustannusten perusteella.</span><span class="sxs-lookup"><span data-stu-id="d55ee-162">You can view the cost for the item in the **Cost** field on the **General** tab. The cost that is shown there comes from the cost that is set up on the **Released product** page.</span></span> <span data-ttu-id="d55ee-163">Kustannusta ei voi päivittää suoraan **Liittyvä toimintonimike**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="d55ee-163">The cost can't be updated directly on the **Related operation item** page.</span></span> <span data-ttu-id="d55ee-164">Kaikkien **Liittyvät toimintonimikkeet** -sivulla lisättyjen nimikkeiden kustannus lisätään automaattisesti **Kustannus**-kenttään **Liittyvät toiminnot** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="d55ee-164">The cost of all items that are added on the **Related operation items** page is automatically added to the **Cost** field on the **Related operations** page.</span></span>

1. <span data-ttu-id="d55ee-165">Toista edellinen vaihe kullekin lisättävälle nimikkeelle.</span><span class="sxs-lookup"><span data-stu-id="d55ee-165">Repeat the previous step for each additional item that you must add.</span></span>
1. <span data-ttu-id="d55ee-166">Sulje sivut.</span><span class="sxs-lookup"><span data-stu-id="d55ee-166">Close the pages.</span></span>

### <a name="add-quality-charges-to-an-operation"></a><span data-ttu-id="d55ee-167">Laatukulujen lisääminen toimintoon</span><span class="sxs-lookup"><span data-stu-id="d55ee-167">Add quality charges to an operation</span></span>

<span data-ttu-id="d55ee-168">Voit lisätä laatukuluja toimintoon noudattamalla seuraavia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="d55ee-168">To add quality charges to an operation, follow these steps.</span></span>

1. <span data-ttu-id="d55ee-169">Siirry kohtaan **Varastonhallinta \> Kausittaiset tehtävät \> Laadunhallinta \> Määrityksistä poikkeamiset**.</span><span class="sxs-lookup"><span data-stu-id="d55ee-169">Go to **Inventory management \> Periodic tasks \> Quality management \> Non conformances**.</span></span>
1. <span data-ttu-id="d55ee-170">Etsi ja valitse luettelosta päivitettävä määrityksistä poikkeaminen.</span><span class="sxs-lookup"><span data-stu-id="d55ee-170">In the list, select the nonconformance that you want to update.</span></span>

    > [!NOTE]
    > <span data-ttu-id="d55ee-171">Voit lisätä toimintoja tai päivittää niitä vain hyväksyttyihin määrityksistä poikkeamisiin.</span><span class="sxs-lookup"><span data-stu-id="d55ee-171">You can add or update operations only for nonconformances that are approved.</span></span>

1. <span data-ttu-id="d55ee-172">Valitse toimintoruudussa **Liittyvät toiminnot**.</span><span class="sxs-lookup"><span data-stu-id="d55ee-172">On the Action Pane, select **Related operations**.</span></span>
1. <span data-ttu-id="d55ee-173">Valitse **Liittyvät toiminnot** -sivulla toiminto, johon haluat lisätä laatukuluja.</span><span class="sxs-lookup"><span data-stu-id="d55ee-173">On the **Related operations** page, select the operation that you want to add quality charges to.</span></span>
1. <span data-ttu-id="d55ee-174">Valitse toimintoruudussa **Laatukulut**.</span><span class="sxs-lookup"><span data-stu-id="d55ee-174">On the Action Pane, select **Quality charges**.</span></span>
1. <span data-ttu-id="d55ee-175">Valitse **Liittyvät toimintokulut** -sivulla toimintoruudussa **Uusi** lisätäksesi rivin ruudukkoon.</span><span class="sxs-lookup"><span data-stu-id="d55ee-175">On the **Related operation charges** page, on the Action pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="d55ee-176">Määritä sitten uudelle rivillä seuraavat kentät:</span><span class="sxs-lookup"><span data-stu-id="d55ee-176">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="d55ee-177">**Kulujen koodi** – Valitse lisättävä laatukulu.</span><span class="sxs-lookup"><span data-stu-id="d55ee-177">**Charges code** – Select the quality charge that you want to add.</span></span>
    - <span data-ttu-id="d55ee-178">**Kuvaus** – Anna kulun yksityiskohtainen kuvaus.</span><span class="sxs-lookup"><span data-stu-id="d55ee-178">**Description** – Enter a detailed description of the charge.</span></span>
    - <span data-ttu-id="d55ee-179">**Kulujen arvo** – Anna veloitettavan kulun summa.</span><span class="sxs-lookup"><span data-stu-id="d55ee-179">**Charges value** – Enter the amount of the charge.</span></span>

1. <span data-ttu-id="d55ee-180">Toista edellinen vaihe kullekin lisättävälle kululle.</span><span class="sxs-lookup"><span data-stu-id="d55ee-180">Repeat the previous step for each additional charge that you must add.</span></span>
1. <span data-ttu-id="d55ee-181">Sulje sivut.</span><span class="sxs-lookup"><span data-stu-id="d55ee-181">Close the pages.</span></span>

> [!NOTE]
> <span data-ttu-id="d55ee-182">**Kulujen arvo** -kentän summa lasketaan automaattisesti kaikkien laatukulujen osalta ja lisätään muihin summiin **Kustannus**-kentässä **Liittyvät toiminnot** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="d55ee-182">The amount in the **Charges value** field is automatically summed for all quality charges and added to any other amounts in the **Cost** field on the **Related operations** page.</span></span>

### <a name="create-a-timesheet-on-an-operation"></a><span data-ttu-id="d55ee-183">Aikaraportin luominen toimintoa varten</span><span class="sxs-lookup"><span data-stu-id="d55ee-183">Create a timesheet on an operation</span></span>

<span data-ttu-id="d55ee-184">Voit lisätä aikaraportin toimintoon noudattamalla seuraavia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="d55ee-184">To add a timesheet to an operation, follow these steps.</span></span>

1. <span data-ttu-id="d55ee-185">Siirry kohtaan **Varastonhallinta \> Kausittaiset tehtävät \> Laadunhallinta \> Määrityksistä poikkeamiset**.</span><span class="sxs-lookup"><span data-stu-id="d55ee-185">Go to **Inventory management \> Periodic tasks \> Quality management \> Non conformances**.</span></span>
1. <span data-ttu-id="d55ee-186">Etsi ja valitse luettelosta päivitettävä määrityksistä poikkeaminen.</span><span class="sxs-lookup"><span data-stu-id="d55ee-186">In the list, select the nonconformance that you want to update.</span></span>

    > [!NOTE]
    > <span data-ttu-id="d55ee-187">Voit lisätä toimintoja tai päivittää niitä vain hyväksyttyihin määrityksistä poikkeamisiin.</span><span class="sxs-lookup"><span data-stu-id="d55ee-187">You can add or update operations only for nonconformances that are approved.</span></span>

1. <span data-ttu-id="d55ee-188">Valitse toimintoruudussa **Liittyvät toiminnot**.</span><span class="sxs-lookup"><span data-stu-id="d55ee-188">On the Action Pane, select **Related operations**.</span></span>
1. <span data-ttu-id="d55ee-189">Valitse **Liittyvät toiminnot** -sivulla toiminto, johon haluat lisätä aikaraportin.</span><span class="sxs-lookup"><span data-stu-id="d55ee-189">On the **Related operations** page, select the operation that you want to add a timesheet to.</span></span>
1. <span data-ttu-id="d55ee-190">Valitse toimintoruudussa **Aikaraportti**.</span><span class="sxs-lookup"><span data-stu-id="d55ee-190">On the Action Pane, select **Timesheet**.</span></span>
1. <span data-ttu-id="d55ee-191">Valitse **Liittyvän toiminnon aikaraportit** -sivulla toimintoruudussa **Uusi** lisätäksesi rivin ruudukkoon.</span><span class="sxs-lookup"><span data-stu-id="d55ee-191">On the **Related operation time sheets** page, on the Action pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="d55ee-192">Määritä sitten uudelle rivillä seuraavat kentät:</span><span class="sxs-lookup"><span data-stu-id="d55ee-192">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="d55ee-193">**Päivämäärä** – Määritä päivämäärä, jolloin työ on tehty.</span><span class="sxs-lookup"><span data-stu-id="d55ee-193">**Date** – Specify the date when work was done.</span></span> <span data-ttu-id="d55ee-194">Oletusarvoisesti tämä kenttä on nykyinen päivämäärä.</span><span class="sxs-lookup"><span data-stu-id="d55ee-194">By default, this field is set to the current date.</span></span>
    - <span data-ttu-id="d55ee-195">**Työntekijät** – Valitse työntekijä, joka teki työn.</span><span class="sxs-lookup"><span data-stu-id="d55ee-195">**Worker** – Select the worker who did the work.</span></span> <span data-ttu-id="d55ee-196">Oletusarvon mukaan tässä kentässä on työntekijä, joka on määritetty nykyiselle käyttäjälle.</span><span class="sxs-lookup"><span data-stu-id="d55ee-196">By default, this field is set to the worker that is assigned to the current user.</span></span>
    - <span data-ttu-id="d55ee-197">**Toiminnon tunnit** – Kirjoita valitussa toiminnossa tehtyjen tuntien määrä.</span><span class="sxs-lookup"><span data-stu-id="d55ee-197">**Operation hours** – Enter the number of hours that were worked on the selected operation.</span></span>
    - <span data-ttu-id="d55ee-198">**Laskutettu** – Valitse tämä valintaruutu, jos aika on veloitettu laskussa asiakkaalle tai toimittajalle.</span><span class="sxs-lookup"><span data-stu-id="d55ee-198">**Invoiced** – Select this check box if the time has been charged to a customer or vendor on an invoice.</span></span>

    > [!NOTE]
    > <span data-ttu-id="d55ee-199">Voit tarkastella kustannusta **Kustannus**-kentässä **Yleiset**-välilehdessä. Kustannukset lasketaan käyttämällä **Varastonhallinnan parametrit** -sivulla määrittämääsi hintaa.</span><span class="sxs-lookup"><span data-stu-id="d55ee-199">You can view the cost in the **Cost** field on the **General** tab. The cost is calculated by using the rate that you define on the **Inventory management parameters** page.</span></span>

1. <span data-ttu-id="d55ee-200">Toista edellinen vaihe kullekin lisättävälle aikaraportin riville.</span><span class="sxs-lookup"><span data-stu-id="d55ee-200">Repeat the previous step for each additional timesheet line that you must add.</span></span>
1. <span data-ttu-id="d55ee-201">Sulje sivut.</span><span class="sxs-lookup"><span data-stu-id="d55ee-201">Close the pages.</span></span>

> [!NOTE]
> <span data-ttu-id="d55ee-202">**Kustannus**-kentän summa lasketaan kaikkien aikaraportin rivien osalta ja lisätään muihin summiin **Kustannus**-kentässä **Liittyvät toiminnot** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="d55ee-202">The amount in the **Cost** field is summed for all timesheet lines and added to any other amounts in the **Cost** field on the **Related operations** page.</span></span>

## <a name="add-a-correction-to-a-nonconformance"></a><span data-ttu-id="d55ee-203">Korjauksen lisääminen määrityksistä poikkeamiseen</span><span class="sxs-lookup"><span data-stu-id="d55ee-203">Add a correction to a nonconformance</span></span>

<span data-ttu-id="d55ee-204">Voit lisätä korjauksen määrityksistä poikkeamiseen seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="d55ee-204">To add a correction to a nonconformance, follow these steps.</span></span>

1. <span data-ttu-id="d55ee-205">Siirry kohtaan **Varastonhallinta \> Kausittaiset tehtävät \> Laadunhallinta \> Määrityksistä poikkeamiset**.</span><span class="sxs-lookup"><span data-stu-id="d55ee-205">Go to **Inventory management \> Periodic tasks \> Quality management \> Non conformances**.</span></span>
1. <span data-ttu-id="d55ee-206">Etsi ja valitse luettelosta päivitettävä määrityksistä poikkeaminen.</span><span class="sxs-lookup"><span data-stu-id="d55ee-206">In the list, select the nonconformance that you want to update.</span></span>

    > [!NOTE]
    > <span data-ttu-id="d55ee-207">Voit lisätä korjauksen vain hyväksyttyihin määrityksistä poikkeamisiin.</span><span class="sxs-lookup"><span data-stu-id="d55ee-207">You can add a correction only to nonconformances that are approved.</span></span>

1. <span data-ttu-id="d55ee-208">Valitse toimintoruudussa **Korjaukset**.</span><span class="sxs-lookup"><span data-stu-id="d55ee-208">On the Action Pane, select **Corrections**.</span></span>
1. <span data-ttu-id="d55ee-209">Valitse **Korjaukset**-sivulla toimintoruudussa **Uusi** lisätäksesi rivin ruudukkoon.</span><span class="sxs-lookup"><span data-stu-id="d55ee-209">On the **Corrections** page, on the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="d55ee-210">Määritä sitten uudelle rivillä seuraavat kentät:</span><span class="sxs-lookup"><span data-stu-id="d55ee-210">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="d55ee-211">**Diagnostiikka** – Valitse diagnostiikkatyyppi, joka määrittää luotavien korjausten tyypin.</span><span class="sxs-lookup"><span data-stu-id="d55ee-211">**Diagnostic** – Select the diagnostic type that identifies the type of correction that you're creating.</span></span>
    - <span data-ttu-id="d55ee-212">**Työntekijä** – Valitse henkilö, joka on vastuussa korjauksesta.</span><span class="sxs-lookup"><span data-stu-id="d55ee-212">**Worker** – Select the person who is responsible for the correction.</span></span>
    - <span data-ttu-id="d55ee-213">**Korjausjärjestys** – Valitse vaihtoehto, joka määrittää, miten korjaus priorisoidaan (*pieni*, *normaali* tai *suuri*).</span><span class="sxs-lookup"><span data-stu-id="d55ee-213">**Correction priority** – Select an option to indicate how the correction should be prioritized (*Low*, *Normal*, or *High*).</span></span>
    - <span data-ttu-id="d55ee-214">**Vaadittu päivämäärä** – Määritä päivämäärä, jolloin korjaustoimintoa pyydettiin.</span><span class="sxs-lookup"><span data-stu-id="d55ee-214">**Requested date** – Enter the date when the corrective action was requested.</span></span>
    - <span data-ttu-id="d55ee-215">**Suunniteltu päivämäärä** – Syötä päivämäärä, jolloin korjaus on tarkoitus tehdä loppuun.</span><span class="sxs-lookup"><span data-stu-id="d55ee-215">**Planned date** – Enter the date when the correction is expected to be completed.</span></span>
    - <span data-ttu-id="d55ee-216">**Lyhytaikainen ratkaisu** – Valitse tämä valintaruutu, jos korjaustoiminto korjaa määrityksistä poikkeamisen vain lyhyen ajan.</span><span class="sxs-lookup"><span data-stu-id="d55ee-216">**Short term solution** – Select this check box if the corrective action corrects the nonconformance only for a short time.</span></span>

1. <span data-ttu-id="d55ee-217">Sulje sivut.</span><span class="sxs-lookup"><span data-stu-id="d55ee-217">Close the pages.</span></span>

## <a name="mark-a-correction-as-completed"></a><span data-ttu-id="d55ee-218">Korjauksen merkitseminen valmiiksi</span><span class="sxs-lookup"><span data-stu-id="d55ee-218">Mark a correction as completed</span></span>

<span data-ttu-id="d55ee-219">Voit merkitä määrityksistä poikkeamisen korjauksen valmiiksi seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="d55ee-219">To mark a nonconformance correction as completed, follow these steps.</span></span>

1. <span data-ttu-id="d55ee-220">Siirry kohtaan **Varastonhallinta \> Kausittaiset tehtävät \> Laadunhallinta \> Määrityksistä poikkeamiset**.</span><span class="sxs-lookup"><span data-stu-id="d55ee-220">Go to **Inventory management \> Periodic tasks \> Quality management \> Non conformances**.</span></span>
1. <span data-ttu-id="d55ee-221">Etsi ja valitse luettelosta päivitettävä määrityksistä poikkeaminen.</span><span class="sxs-lookup"><span data-stu-id="d55ee-221">In the list, select the nonconformance that you want to update.</span></span>

    > [!NOTE]
    > <span data-ttu-id="d55ee-222">Voit lisätä korjauksen vain hyväksyttyihin määrityksistä poikkeamisiin.</span><span class="sxs-lookup"><span data-stu-id="d55ee-222">You can add a correction only to nonconformances that are approved.</span></span>

1. <span data-ttu-id="d55ee-223">Valitse toimintoruudussa **Korjaukset**.</span><span class="sxs-lookup"><span data-stu-id="d55ee-223">On the Action Pane, select **Corrections**.</span></span>
1. <span data-ttu-id="d55ee-224">Valitse **Korjaukset**-sivun ruudukosta korjaus, jonka haluat merkitä valmiiksi.</span><span class="sxs-lookup"><span data-stu-id="d55ee-224">On the **Corrections** page, in the grid, select the correction that you want to mark as completed.</span></span>
1. <span data-ttu-id="d55ee-225">Valitse toimintoruudussa **Merkitse valmiiksi**.</span><span class="sxs-lookup"><span data-stu-id="d55ee-225">On the Action Pane, select **Mark complete**.</span></span>
1. <span data-ttu-id="d55ee-226">Järjestelmä pyytää vahvistamaan valinnan.</span><span class="sxs-lookup"><span data-stu-id="d55ee-226">You're prompted to confirm your selection.</span></span> <span data-ttu-id="d55ee-227">Jatka valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="d55ee-227">Select **OK** to continue.</span></span> <span data-ttu-id="d55ee-228">**Valmistumispäivämäärä ja -aika** -kentän arvoksi tulee nykyinen päivämäärä ja aika, ja **Valmis**-valintaruutu on valittuna.</span><span class="sxs-lookup"><span data-stu-id="d55ee-228">The **Completion date and time** field is set to the current date and time, and the **Completed** check box is selected.</span></span>
1. <span data-ttu-id="d55ee-229">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="d55ee-229">Close the page.</span></span>

## <a name="reopen-a-completed-correction"></a><span data-ttu-id="d55ee-230">Valmiin korjauksen avaaminen uudelleen</span><span class="sxs-lookup"><span data-stu-id="d55ee-230">Reopen a completed correction</span></span>

<span data-ttu-id="d55ee-231">Voit avata valmiin korjauksen uudelleen seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="d55ee-231">To reopen a completed correction, follow these steps.</span></span>

1. <span data-ttu-id="d55ee-232">Siirry kohtaan **Varastonhallinta \> Kausittaiset tehtävät \> Laadunhallinta \> Määrityksistä poikkeamiset**.</span><span class="sxs-lookup"><span data-stu-id="d55ee-232">Go to **Inventory management \> Periodic tasks \> Quality management \> Non conformances**.</span></span>
1. <span data-ttu-id="d55ee-233">Etsi ja valitse luettelosta päivitettävä määrityksistä poikkeaminen.</span><span class="sxs-lookup"><span data-stu-id="d55ee-233">In the list, select the nonconformance that you want to update.</span></span>
1. <span data-ttu-id="d55ee-234">Valitse toimintoruudussa **Korjaukset**.</span><span class="sxs-lookup"><span data-stu-id="d55ee-234">On the Action pane, select **Corrections**.</span></span>
1. <span data-ttu-id="d55ee-235">Valitse **Korjaukset**-sivun ruudukosta korjaus, jonka haluat avata uudelleen.</span><span class="sxs-lookup"><span data-stu-id="d55ee-235">On the **Corrections** page, in the grid, select the correction that you want to reopen.</span></span>
1. <span data-ttu-id="d55ee-236">Valitse toimintoruudussa **Avaa uudelleen**.</span><span class="sxs-lookup"><span data-stu-id="d55ee-236">On the Action Pane, select **Reopen**.</span></span>
1. <span data-ttu-id="d55ee-237">Järjestelmä pyytää vahvistamaan valinnan.</span><span class="sxs-lookup"><span data-stu-id="d55ee-237">You're prompted to confirm your selection.</span></span> <span data-ttu-id="d55ee-238">Jatka valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="d55ee-238">Select **OK** to continue.</span></span> <span data-ttu-id="d55ee-239">Arvo poistetaan **Valmistumispäivämäärä ja -aika** -kentästä, ja **Valmis**-valintaruudun valinta poistetaan.</span><span class="sxs-lookup"><span data-stu-id="d55ee-239">The value is cleared from the **Completion date and time** field, and the **Completed** check box is cleared.</span></span>
1. <span data-ttu-id="d55ee-240">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="d55ee-240">Close the page.</span></span>

<span data-ttu-id="d55ee-241">Korjaukseen voi nyt tehdä lisämuokkauksia tai päivityksiä.</span><span class="sxs-lookup"><span data-stu-id="d55ee-241">You can now make additional edits or updates to the correction.</span></span> <span data-ttu-id="d55ee-242">Kun olet valmis, voit merkitä korjauksen valmiiksi uudelleen.</span><span class="sxs-lookup"><span data-stu-id="d55ee-242">When you've finished, you can mark the correction as completed again.</span></span>

## <a name="close-a-nonconformance"></a><span data-ttu-id="d55ee-243">Sulje määrityksistä poikkeaminen</span><span class="sxs-lookup"><span data-stu-id="d55ee-243">Close a nonconformance</span></span>

<span data-ttu-id="d55ee-244">Voit sulkea määrityksistä poikkeamisen seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="d55ee-244">To close a nonconformance, follow these steps.</span></span>

1. <span data-ttu-id="d55ee-245">Siirry kohtaan **Varastonhallinta \> Kausittaiset tehtävät \> Laadunhallinta \> Laatutilaukset**.</span><span class="sxs-lookup"><span data-stu-id="d55ee-245">Go to **Inventory management \> Periodic tasks \> Quality management \> Quality orders**.</span></span>
1. <span data-ttu-id="d55ee-246">Valitse ruudukosta laatutilaus.</span><span class="sxs-lookup"><span data-stu-id="d55ee-246">Select a quality order in the grid.</span></span>
1. <span data-ttu-id="d55ee-247">Valitse toimintoruudussa **Tiedustelut \> Määrityksistä poikkeamiset**.</span><span class="sxs-lookup"><span data-stu-id="d55ee-247">On the Action Pane, select **Inquiries \> Non conformances**.</span></span>
1. <span data-ttu-id="d55ee-248">Valitse **Määrityksistä poikkeamiset** -sivulla ruudukosta kohteena oleva määrityksistä poikkeaminen.</span><span class="sxs-lookup"><span data-stu-id="d55ee-248">On the **Non conformances** page, select the target nonconformance in the grid.</span></span>
1. <span data-ttu-id="d55ee-249">Valitse toimintoruudussa **Toiminnot \> Sulje määrityksistä poikkeaminen**.</span><span class="sxs-lookup"><span data-stu-id="d55ee-249">On the Action Pane, select **Functions \> Close non conformance**.</span></span>
1. <span data-ttu-id="d55ee-250">Järjestelmä pyytää vahvistamaan valinnan.</span><span class="sxs-lookup"><span data-stu-id="d55ee-250">You're prompted to confirm your selection.</span></span> <span data-ttu-id="d55ee-251">Jatka valitsemalla **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="d55ee-251">Select **Yes** to continue.</span></span>
1. <span data-ttu-id="d55ee-252">Sulje sivut.</span><span class="sxs-lookup"><span data-stu-id="d55ee-252">Close the pages.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d55ee-253">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="d55ee-253">Additional resources</span></span>

- [<span data-ttu-id="d55ee-254">Laadunhallinnan yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="d55ee-254">Quality management overview</span></span>](../quality-management-processes.md)
- [<span data-ttu-id="d55ee-255">Laadun ja määrityksistä poikkeamisen hallinnan ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="d55ee-255">Enable quality and nonconformance management</span></span>](../enable-quality-management.md)
- [<span data-ttu-id="d55ee-256">Määrityksistä poikkeamisia hyväksyvät työntekijät</span><span class="sxs-lookup"><span data-stu-id="d55ee-256">Workers responsible for approving nonconformances</span></span>](../quality-responsible-workers.md)
- [<span data-ttu-id="d55ee-257">Määrityksistä poikkeamisia koskevat karanteenivyöhykkeet</span><span class="sxs-lookup"><span data-stu-id="d55ee-257">Quarantine zones for nonconformances</span></span>](../quality-quarantine-zones.md)
- [<span data-ttu-id="d55ee-258">Määrityksistä poikkeamisten diagnostiikkatyypit</span><span class="sxs-lookup"><span data-stu-id="d55ee-258">Diagnostic types for nonconformances</span></span>](../quality-diagnostic-types.md)
- [<span data-ttu-id="d55ee-259">Määrityksistä poikkeamisten laatukulut</span><span class="sxs-lookup"><span data-stu-id="d55ee-259">Quality charges for nonconformances</span></span>](../quality-charges.md)
- [<span data-ttu-id="d55ee-260">Toiminnot määrityksistä poikkeamisille</span><span class="sxs-lookup"><span data-stu-id="d55ee-260">Operations for nonconformances</span></span>](../quality-operations.md)
- [<span data-ttu-id="d55ee-261">Laadunhallinta varastoprosesseja varten</span><span class="sxs-lookup"><span data-stu-id="d55ee-261">Quality management for warehouse processes</span></span>](../quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
