---
title: Myyntitilauksen tilasarakkeiden yhdistämismäärityksen ottaminen käyttöön
description: Tässä aiheessa käsitellään myyntitilausten tilasarakkeiden määrittämistä kaksoiskirjoitusta varten.
author: dasani-madipalli
manager: tonyafehr
ms.date: 06/25/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: damadipa
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-06-25
ms.openlocfilehash: cc70501d231390ea15104d508a36300a1b2cd44c
ms.sourcegitcommit: 7e1be696894731e1c58074d9b5e9c5b3acf7e52a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/17/2020
ms.locfileid: "4744296"
---
# <a name="set-up-the-mapping-for-the-sales-order-status-columns"></a><span data-ttu-id="cb776-103">Myyntitilauksen tilasarakkeiden yhdistämismäärityksen ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="cb776-103">Set up the mapping for the sales order status columns</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="cb776-104">Ostotilauksen tilan ilmoittavilla sarakkeilla on erilaiset luettelointiarvot Microsoft Dynamics 365 Supply Chain Managementissa ja Dynamics 365 Salesissa.</span><span class="sxs-lookup"><span data-stu-id="cb776-104">The columns that indicate sales order status have different enumeration values in Microsoft Dynamics 365 Supply Chain Management and Dynamics 365 Sales.</span></span> <span data-ttu-id="cb776-105">Näiden sarakkeiden yhdistämismääritys kaksoiskirjoituksessa edellyttää lisämäärityksiä.</span><span class="sxs-lookup"><span data-stu-id="cb776-105">Additional setup is required to map these columns in dual-write.</span></span>

## <a name="columns-in-supply-chain-management"></a><span data-ttu-id="cb776-106">Supply Chain Managementin sarakkeet</span><span class="sxs-lookup"><span data-stu-id="cb776-106">columns in Supply Chain Management</span></span>

<span data-ttu-id="cb776-107">Supply Chain Managementissa myyntitilauksen tilaan liittyy kaksi saraketta.</span><span class="sxs-lookup"><span data-stu-id="cb776-107">In Supply Chain Management, two columns reflect the status of the sales order.</span></span> <span data-ttu-id="cb776-108">Sarakkeet, joille on suoritettava yhdistämismääritys ovat **Tila** ja **Asiakirjan tila**.</span><span class="sxs-lookup"><span data-stu-id="cb776-108">The columns that you must map are **Status** and **Document Status**.</span></span>

<span data-ttu-id="cb776-109">**Tila**-luettelointi määrittää tilauksen yleisen tilan.</span><span class="sxs-lookup"><span data-stu-id="cb776-109">The **Status** enumeration specifies the overall status of the order.</span></span> <span data-ttu-id="cb776-110">Tämä tila näkyy tilauksen otsikossa.</span><span class="sxs-lookup"><span data-stu-id="cb776-110">This status is shown on the order header.</span></span>

<span data-ttu-id="cb776-111">**Tila**-luetteloinnilla on seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="cb776-111">The **Status** enumeration has the following values:</span></span>

- <span data-ttu-id="cb776-112">Avoin tilaus</span><span class="sxs-lookup"><span data-stu-id="cb776-112">Open Order</span></span>
- <span data-ttu-id="cb776-113">Toimitettu</span><span class="sxs-lookup"><span data-stu-id="cb776-113">Delivered</span></span>
- <span data-ttu-id="cb776-114">Laskutettu</span><span class="sxs-lookup"><span data-stu-id="cb776-114">Invoiced</span></span>
- <span data-ttu-id="cb776-115">Peruutettu</span><span class="sxs-lookup"><span data-stu-id="cb776-115">Cancelled</span></span>

<span data-ttu-id="cb776-116">**Asiakirjan tila** -luettelointi määrittää viimeisimmän tilaukselle luodun asiakirjan.</span><span class="sxs-lookup"><span data-stu-id="cb776-116">The **Document Status** enumeration specifies the most recent document that was generated for the order.</span></span> <span data-ttu-id="cb776-117">Jos tilaus on esimerkiksi vahvistettu, tämä asiakirja on myyntitilauksen vahvistus.</span><span class="sxs-lookup"><span data-stu-id="cb776-117">For example, if the order is confirmed, this document is a sales order confirmation.</span></span> <span data-ttu-id="cb776-118">Jos myynti tilaus on laskutettu osittain ja jäännösrivi vahvistetaan, asiakirjan tilana pysyy **Lasku**, koska lasku luodaan myöhemmin prosessissa.</span><span class="sxs-lookup"><span data-stu-id="cb776-118">If a sales order is partially invoiced, and then the remaining line is confirmed, the document status remains **Invoice**, because the invoice is generated later in the process.</span></span>

<span data-ttu-id="cb776-119">**Asiakirjan tila** -luetteloinnilla on seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="cb776-119">The **Document Status** enumeration has the following values:</span></span>

- <span data-ttu-id="cb776-120">Vahvistus</span><span class="sxs-lookup"><span data-stu-id="cb776-120">Confirmation</span></span>
- <span data-ttu-id="cb776-121">Keräysluettelo</span><span class="sxs-lookup"><span data-stu-id="cb776-121">Picking List</span></span>
- <span data-ttu-id="cb776-122">Pakkausluettelo</span><span class="sxs-lookup"><span data-stu-id="cb776-122">Packing Slip</span></span>
- <span data-ttu-id="cb776-123">Lasku</span><span class="sxs-lookup"><span data-stu-id="cb776-123">Invoice</span></span>

## <a name="columns-in-sales"></a><span data-ttu-id="cb776-124">Salesin sarakkeet</span><span class="sxs-lookup"><span data-stu-id="cb776-124">columns in Sales</span></span>

<span data-ttu-id="cb776-125">Salesissa myyntitilauksen tilaan liittyy kaksi saraketta.</span><span class="sxs-lookup"><span data-stu-id="cb776-125">In Sales, two columns indicate the status of the order.</span></span> <span data-ttu-id="cb776-126">Sarakkeet, joille on suoritettava yhdistämismääritys, ovat **Tila** ja **Käsittelytila**.</span><span class="sxs-lookup"><span data-stu-id="cb776-126">The columns that you must map are **Status** and **Processing Status**.</span></span>

<span data-ttu-id="cb776-127">**Tila**-luettelointi määrittää tilauksen yleisen tilan.</span><span class="sxs-lookup"><span data-stu-id="cb776-127">The **Status** enumeration specifies the overall status of the order.</span></span> <span data-ttu-id="cb776-128">Sillä on seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="cb776-128">It has the following values:</span></span>

- <span data-ttu-id="cb776-129">Aktiiviset</span><span class="sxs-lookup"><span data-stu-id="cb776-129">Active</span></span>
- <span data-ttu-id="cb776-130">Lähetetty</span><span class="sxs-lookup"><span data-stu-id="cb776-130">Submitted</span></span>
- <span data-ttu-id="cb776-131">Täytetty</span><span class="sxs-lookup"><span data-stu-id="cb776-131">Fulfilled</span></span>
- <span data-ttu-id="cb776-132">Laskutettu</span><span class="sxs-lookup"><span data-stu-id="cb776-132">Invoiced</span></span>
- <span data-ttu-id="cb776-133">Peruutettu</span><span class="sxs-lookup"><span data-stu-id="cb776-133">Cancelled</span></span>

<span data-ttu-id="cb776-134">**Käsittelytila**-luettelointi otettiin käyttöön, jotta tilalle voidaan suorittaa tarkempi yhdistämismääritys Supply Chain Managementin kanssa.</span><span class="sxs-lookup"><span data-stu-id="cb776-134">The **Processing Status** enumeration was introduced so that the status can be mapped more accurately with Supply Chain Management.</span></span>

<span data-ttu-id="cb776-135">Seuraavassa taulukossa esitetään **Käsittelytila**-arvon yhdistämismääritys Supply Chain Managementissa.</span><span class="sxs-lookup"><span data-stu-id="cb776-135">The following table shows the mapping of **Processing Status** in Supply Chain Management.</span></span>

| <span data-ttu-id="cb776-136">Käsittelyn tila</span><span class="sxs-lookup"><span data-stu-id="cb776-136">Processing Status</span></span>   | <span data-ttu-id="cb776-137">Tila Supply Chain Managementissa</span><span class="sxs-lookup"><span data-stu-id="cb776-137">Status in Supply Chain Management</span></span> | <span data-ttu-id="cb776-138">Asiakirjan tila Supply Chain Managementissa</span><span class="sxs-lookup"><span data-stu-id="cb776-138">Document Status in Supply Chain Management</span></span> |
|---------------------|-----------------------------------|--------------------------------------------|
| <span data-ttu-id="cb776-139">Aktiiviset</span><span class="sxs-lookup"><span data-stu-id="cb776-139">Active</span></span>              | <span data-ttu-id="cb776-140">Avoin tilaus</span><span class="sxs-lookup"><span data-stu-id="cb776-140">Open Order</span></span>                        | <span data-ttu-id="cb776-141">None</span><span class="sxs-lookup"><span data-stu-id="cb776-141">None</span></span>                                       |
| <span data-ttu-id="cb776-142">Vahvistettu</span><span class="sxs-lookup"><span data-stu-id="cb776-142">Confirmed</span></span>           | <span data-ttu-id="cb776-143">Avoin tilaus</span><span class="sxs-lookup"><span data-stu-id="cb776-143">Open Order</span></span>                        | <span data-ttu-id="cb776-144">Vahvistus</span><span class="sxs-lookup"><span data-stu-id="cb776-144">Confirmation</span></span>                               |
| <span data-ttu-id="cb776-145">Keräilty</span><span class="sxs-lookup"><span data-stu-id="cb776-145">Picked</span></span>              | <span data-ttu-id="cb776-146">Avoin tilaus</span><span class="sxs-lookup"><span data-stu-id="cb776-146">Open Order</span></span>                        | <span data-ttu-id="cb776-147">Keräysluettelo</span><span class="sxs-lookup"><span data-stu-id="cb776-147">Picking List</span></span>                               |
| <span data-ttu-id="cb776-148">Osittain toimitettu</span><span class="sxs-lookup"><span data-stu-id="cb776-148">Partially Delivered</span></span> | <span data-ttu-id="cb776-149">Avoin tilaus</span><span class="sxs-lookup"><span data-stu-id="cb776-149">Open Order</span></span>                        | <span data-ttu-id="cb776-150">Pakkausluettelo</span><span class="sxs-lookup"><span data-stu-id="cb776-150">Packing Slip</span></span>                               |
| <span data-ttu-id="cb776-151">Toimitettu</span><span class="sxs-lookup"><span data-stu-id="cb776-151">Delivered</span></span>           | <span data-ttu-id="cb776-152">Toimitettu</span><span class="sxs-lookup"><span data-stu-id="cb776-152">Delivered</span></span>                         | <span data-ttu-id="cb776-153">Pakkausluettelo</span><span class="sxs-lookup"><span data-stu-id="cb776-153">Packing Slip</span></span>                               |
| <span data-ttu-id="cb776-154">Osittain laskutettu</span><span class="sxs-lookup"><span data-stu-id="cb776-154">Partially Invoiced</span></span>  | <span data-ttu-id="cb776-155">Toimitettu</span><span class="sxs-lookup"><span data-stu-id="cb776-155">Delivered</span></span>                         | <span data-ttu-id="cb776-156">Lasku</span><span class="sxs-lookup"><span data-stu-id="cb776-156">Invoice</span></span>                                    |
| <span data-ttu-id="cb776-157">Laskutettu</span><span class="sxs-lookup"><span data-stu-id="cb776-157">Invoiced</span></span>            | <span data-ttu-id="cb776-158">Laskutettu</span><span class="sxs-lookup"><span data-stu-id="cb776-158">Invoiced</span></span>                          | <span data-ttu-id="cb776-159">Lasku</span><span class="sxs-lookup"><span data-stu-id="cb776-159">Invoice</span></span>                                    |
| <span data-ttu-id="cb776-160">Peruutettu</span><span class="sxs-lookup"><span data-stu-id="cb776-160">Cancelled</span></span>           | <span data-ttu-id="cb776-161">Peruutettu</span><span class="sxs-lookup"><span data-stu-id="cb776-161">Cancelled</span></span>                         | <span data-ttu-id="cb776-162">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="cb776-162">Not applicable</span></span>                             |

<span data-ttu-id="cb776-163">Seuraavassa taulukossa esitetään **Käsittelytila**-arvon yhdistämismääritys Salesin ja Supply Chain Managementin välillä.</span><span class="sxs-lookup"><span data-stu-id="cb776-163">The following table shows the mapping of **Processing Status** between Sales and Supply Chain Management.</span></span>

| <span data-ttu-id="cb776-164">Käsittelyn tila</span><span class="sxs-lookup"><span data-stu-id="cb776-164">Processing Status</span></span>   | <span data-ttu-id="cb776-165">Tila Salesissa</span><span class="sxs-lookup"><span data-stu-id="cb776-165">Status in Sales</span></span> | <span data-ttu-id="cb776-166">Tila Supply Chain Managementissa</span><span class="sxs-lookup"><span data-stu-id="cb776-166">Status in Supply Chain Management</span></span> |
|---------------------|-----------------|-----------------------------------|
| <span data-ttu-id="cb776-167">Aktiiviset</span><span class="sxs-lookup"><span data-stu-id="cb776-167">Active</span></span>              | <span data-ttu-id="cb776-168">Aktiiviset</span><span class="sxs-lookup"><span data-stu-id="cb776-168">Active</span></span>          | <span data-ttu-id="cb776-169">Avoin tilaus</span><span class="sxs-lookup"><span data-stu-id="cb776-169">Open Order</span></span>                        |
| <span data-ttu-id="cb776-170">Vahvistettu</span><span class="sxs-lookup"><span data-stu-id="cb776-170">Confirmed</span></span>           | <span data-ttu-id="cb776-171">Lähetetty</span><span class="sxs-lookup"><span data-stu-id="cb776-171">Submitted</span></span>       | <span data-ttu-id="cb776-172">Avoin tilaus</span><span class="sxs-lookup"><span data-stu-id="cb776-172">Open Order</span></span>                        |
| <span data-ttu-id="cb776-173">Keräilty</span><span class="sxs-lookup"><span data-stu-id="cb776-173">Picked</span></span>              | <span data-ttu-id="cb776-174">Lähetetty</span><span class="sxs-lookup"><span data-stu-id="cb776-174">Submitted</span></span>       | <span data-ttu-id="cb776-175">Avoin tilaus</span><span class="sxs-lookup"><span data-stu-id="cb776-175">Open Order</span></span>                        |
| <span data-ttu-id="cb776-176">Osittain toimitettu</span><span class="sxs-lookup"><span data-stu-id="cb776-176">Partially Delivered</span></span> | <span data-ttu-id="cb776-177">Aktiiviset</span><span class="sxs-lookup"><span data-stu-id="cb776-177">Active</span></span>          | <span data-ttu-id="cb776-178">Avoin tilaus</span><span class="sxs-lookup"><span data-stu-id="cb776-178">Open Order</span></span>                        |
| <span data-ttu-id="cb776-179">Osittain laskutettu</span><span class="sxs-lookup"><span data-stu-id="cb776-179">Partially Invoiced</span></span>  | <span data-ttu-id="cb776-180">Aktiiviset</span><span class="sxs-lookup"><span data-stu-id="cb776-180">Active</span></span>          | <span data-ttu-id="cb776-181">Avoin tilaus</span><span class="sxs-lookup"><span data-stu-id="cb776-181">Open Order</span></span>                        |
| <span data-ttu-id="cb776-182">Osittain laskutettu</span><span class="sxs-lookup"><span data-stu-id="cb776-182">Partially Invoiced</span></span>  | <span data-ttu-id="cb776-183">Täytetty</span><span class="sxs-lookup"><span data-stu-id="cb776-183">Fulfilled</span></span>       | <span data-ttu-id="cb776-184">Toimitettu</span><span class="sxs-lookup"><span data-stu-id="cb776-184">Delivered</span></span>                         |
| <span data-ttu-id="cb776-185">Laskutettu</span><span class="sxs-lookup"><span data-stu-id="cb776-185">Invoiced</span></span>            | <span data-ttu-id="cb776-186">Laskutettu</span><span class="sxs-lookup"><span data-stu-id="cb776-186">Invoiced</span></span>        | <span data-ttu-id="cb776-187">Laskutettu</span><span class="sxs-lookup"><span data-stu-id="cb776-187">Invoiced</span></span>                          |
| <span data-ttu-id="cb776-188">Peruutettu</span><span class="sxs-lookup"><span data-stu-id="cb776-188">Cancelled</span></span>           | <span data-ttu-id="cb776-189">Peruutettu</span><span class="sxs-lookup"><span data-stu-id="cb776-189">Cancelled</span></span>       | <span data-ttu-id="cb776-190">Peruutettu</span><span class="sxs-lookup"><span data-stu-id="cb776-190">Cancelled</span></span>                         |

## <a name="setup"></a><span data-ttu-id="cb776-191">Luo perustiedot</span><span class="sxs-lookup"><span data-stu-id="cb776-191">Setup</span></span>

<span data-ttu-id="cb776-192">Voit määrittää myyntitilauksen tilasarakkeiden yhdistämismäärityksen ottamalla käyttöön määritteet **IsSOPIntegrationEnabled** ja **isIntegrationUser**.</span><span class="sxs-lookup"><span data-stu-id="cb776-192">To set up the mapping for the sales order status columns, you must enable the **IsSOPIntegrationEnabled** and **isIntegrationUser** attributes.</span></span>

<span data-ttu-id="cb776-193">Voit ottaa **IsSOPIntegrationEnabled**-määritteen käyttöön seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="cb776-193">To enable the **IsSOPIntegrationEnabled** attribute, follow these steps.</span></span>

1. <span data-ttu-id="cb776-194">Siirry selaimessa osoitteeseen `https://<test-name>.crm.dynamics.com/api/data/v9.0/organizations`.</span><span class="sxs-lookup"><span data-stu-id="cb776-194">In a browser, go to `https://<test-name>.crm.dynamics.com/api/data/v9.0/organizations`.</span></span> <span data-ttu-id="cb776-195">Korvaa **\<test-name\>** yrityksesi Sales-linkillä.</span><span class="sxs-lookup"><span data-stu-id="cb776-195">Replace **\<test-name\>** with your company's link to Sales.</span></span>
2. <span data-ttu-id="cb776-196">Etsi avatulla sivulla **organizationid** ja kirjoita arvo muistiin.</span><span class="sxs-lookup"><span data-stu-id="cb776-196">On the page that is opened, find **organizationid**, and make a note of the value.</span></span>

    ![organizationid-arvon etsiminen](media/sales-map-orgid.png)

3. <span data-ttu-id="cb776-198">Avaa selainkonsoli Salesissa ja suorita seuraava komentosarja.</span><span class="sxs-lookup"><span data-stu-id="cb776-198">In Sales, open the browser console, and run following script.</span></span> <span data-ttu-id="cb776-199">Käytä vaiheen 2 **organizationid**-arvoa.</span><span class="sxs-lookup"><span data-stu-id="cb776-199">Use the **organizationid** value from step 2.</span></span>

    ```javascript
    Xrm.WebApi.updateRecord("organization",
    "d9a7c5f7-acbf-4aa9-86e8-a891c43f748c", {"issopintegrationenabled" :
    true}).then(
        function success(result) {
            console.log("Account updated");
            // perform operations on row update
        },
        function (error) {
            console.log(error.message);
            // handle error conditions
        }
    );
    ```

    ![JavaScript-koodi selainkonsolissa](media/sales-map-script.png)

4. <span data-ttu-id="cb776-201">Varmista, että **IsSOPIntegrationEnabled**-arvona on **tosi**.</span><span class="sxs-lookup"><span data-stu-id="cb776-201">Verify that **IsSOPIntegrationEnabled** is set to **true**.</span></span> <span data-ttu-id="cb776-202">Tarkista arvo vaiheen 1 URL-osoitteen avulla.</span><span class="sxs-lookup"><span data-stu-id="cb776-202">Use the URL from step 1 to check the value.</span></span>

    ![IsSOPIntegrationEnabled-arvona on tosi](media/sales-map-integration-enabled.png)

<span data-ttu-id="cb776-204">Voit ottaa **isIntegrationUser**-määritteen käyttöön seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="cb776-204">To enable the **isIntegrationUser** attribute, follow these steps.</span></span>

1. <span data-ttu-id="cb776-205">Valitse Salesissa **Asetus \> Mukauttaminen \> Järjestelmän mukauttaminen**, valitse **Käyttäjätaulu** ja avaa sitten **Lomake \> Käyttäjä**.</span><span class="sxs-lookup"><span data-stu-id="cb776-205">In Sales, go to **Setting \> Customization \> Customize the System**, select **User table**, and then open **Form \> User**.</span></span>

    ![Käyttäjälomakkeen avaaminen](media/sales-map-user.png)

2. <span data-ttu-id="cb776-207">Etsi kenttähaussa **Integrointikäyttäjän tila** ja lisää se lomakkeeseen kaksoisnapsauttamalla.</span><span class="sxs-lookup"><span data-stu-id="cb776-207">In Field Explorer, find **Integration user mode**, and double-click it to add it to the form.</span></span> <span data-ttu-id="cb776-208">Tallenna muutos.</span><span class="sxs-lookup"><span data-stu-id="cb776-208">Save your change.</span></span>

    ![Integrointikäyttäjän tila -sarakkeen lisääminen lomakkeeseen](media/sales-map-field-explorer.png)

3. <span data-ttu-id="cb776-210">Siirry Salesissa kohtaan **Asetus \> Suojaus \> Käyttäjät** ja vaihda näkymästä **Käytössä olevat käyttäjät** näkymään **Sovelluksen käyttäjät**.</span><span class="sxs-lookup"><span data-stu-id="cb776-210">In Sales, go to **Setting \> Security \> Users**, and change the view from **Enabled Users** to **Application Users**.</span></span>

    ![Näkymän vaihtaminen käytössä olevista käyttäjistä sovelluksen käyttäjiin](media/sales-map-enabled-users.png)

4. <span data-ttu-id="cb776-212">Valitse kohdan **DualWrite IntegrationUser** kaksi merkintää.</span><span class="sxs-lookup"><span data-stu-id="cb776-212">Select the two entries for **DualWrite IntegrationUser**.</span></span>

    ![Sovelluksen käyttäjien luettelo](media/sales-map-user-mode.png)

5. <span data-ttu-id="cb776-214">Muuta **Integrointikäyttäjän tila** -sarakkeen arvoksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="cb776-214">Change the value of the **Integration user mode** column to **Yes**.</span></span>

    ![Integrointikäyttäjän tila -sarakkeen arvon muuttaminen](media/sales-map-user-mode-yes.png)

<span data-ttu-id="cb776-216">Myyntitilauksillesi on nyt suoritettu yhdistämismääritys.</span><span class="sxs-lookup"><span data-stu-id="cb776-216">Your sales orders are now mapped.</span></span>
