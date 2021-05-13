---
title: Ostohyvitysten hallintaryhmät
description: Tässä aiheessa käsitellään ostohyvitysten hallintaryhmien määrittämistä. Ostohyvitysten hallintaryhmiä voi käyttää ostohyvitysten laskennassa, ja ne voidaan liittää päätietueeseen.
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TAMRebateGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: cef7abbbf2a94e26b6b9e66492cd7347d3b4d1f2
ms.sourcegitcommit: 890a0b3eb3c1f48d786b0789e5bb8641e0b8455e
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920058"
---
# <a name="rebate-management-groups"></a><span data-ttu-id="5db1f-104">Ostohyvitysten hallintaryhmät</span><span class="sxs-lookup"><span data-stu-id="5db1f-104">Rebate management groups</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5db1f-105">Ostohyvitys- ja vähennyslaskelmat voidaan määrittää ryhmien perusteella.</span><span class="sxs-lookup"><span data-stu-id="5db1f-105">Rebate and deduction calculations can be driven by groups.</span></span> <span data-ttu-id="5db1f-106">Ostohyvitysten hallintaryhmiä voi luoda asiakkaille, toimittajille ja nimikkeille.</span><span class="sxs-lookup"><span data-stu-id="5db1f-106">Rebate management groups can be created for customers, vendors, and items.</span></span> <span data-ttu-id="5db1f-107">Ne voidaan liittää päätietueeseen.</span><span class="sxs-lookup"><span data-stu-id="5db1f-107">They can be attached to a master record.</span></span>

## <a name="rebate-management-customer-groups"></a><span data-ttu-id="5db1f-108">Ostohyvitysten hallinnan asiakasryhmät</span><span class="sxs-lookup"><span data-stu-id="5db1f-108">Rebate management customer groups</span></span>

<span data-ttu-id="5db1f-109">Asiakasryhmän laskenta luodaan usein yritysketjulle, kuten marketketjulle tai franchise-yritykselle.</span><span class="sxs-lookup"><span data-stu-id="5db1f-109">The calculation for a group of customers is often created for a chain of companies, such as a supermarket chain or a franchise company.</span></span> <span data-ttu-id="5db1f-110">Tämäntyyppinen laskentatapa liittyy yleensä ostohyvitykseen.</span><span class="sxs-lookup"><span data-stu-id="5db1f-110">This type of calculation is usually related to a rebate.</span></span>

<span data-ttu-id="5db1f-111">Vähennys lasketaan usein niin, että ei oteta huomioon sitä, kenelle hyväksytty tilaus on myyty.</span><span class="sxs-lookup"><span data-stu-id="5db1f-111">A deduction is often calculated without considering who the qualifying order was sold to.</span></span> <span data-ttu-id="5db1f-112">Tähän on kuitenkin poikkeuksia.</span><span class="sxs-lookup"><span data-stu-id="5db1f-112">However, there are exceptions.</span></span> <span data-ttu-id="5db1f-113">Lisenssinhaltija voi esimerkiksi luoda vähennysmallin, johon asiakasryhmä A saa 4 prosenttia, mutta asiakasryhmä B saa vain 3 prosenttia.</span><span class="sxs-lookup"><span data-stu-id="5db1f-113">For example, a licensee might create a deduction scheme where customer group A will receive 4 percent, but customer group B will receive only 3 percent.</span></span>

### <a name="set-up-customer-groups"></a><span data-ttu-id="5db1f-114">Määritä asiakasryhmät</span><span class="sxs-lookup"><span data-stu-id="5db1f-114">Set up customer groups</span></span>

<span data-ttu-id="5db1f-115">Voit käyttää ostohyvityksen hallinnan asiakasryhmiä kohdassa **Ostohyvitysten hallinta \> Ostohyvitysten hallintaryhmien asetukset \> Asiakasryhmät**.</span><span class="sxs-lookup"><span data-stu-id="5db1f-115">To work with Rebate management customer groups, go to **Rebate management \> Rebate management groups setup \> Customer groups**.</span></span> <span data-ttu-id="5db1f-116">Voit lisätä ja poistaa ryhmiä tarpeen mukaan käyttämällä toimintoruudun painikkeita.</span><span class="sxs-lookup"><span data-stu-id="5db1f-116">You can use the buttons on the Action Pane to add and remove groups as required.</span></span> <span data-ttu-id="5db1f-117">Määritä kullekin ryhmälle seuraavat kentät:</span><span class="sxs-lookup"><span data-stu-id="5db1f-117">For each group, set the following fields:</span></span>

- <span data-ttu-id="5db1f-118">**Ostohyvitysten hallintaryhmä** – Anna ryhmän yksilöivä nimi.</span><span class="sxs-lookup"><span data-stu-id="5db1f-118">**Rebate management group** – Enter a unique name for the group.</span></span>
- <span data-ttu-id="5db1f-119">**Kuvaus** – Syötä ryhmän kuvaus, joka sisältää lisätietoja ryhmän käytöstä.</span><span class="sxs-lookup"><span data-stu-id="5db1f-119">**Description** – Enter a description of the group to provide more information about how it should be used.</span></span>

### <a name="manage-customer-group-assignments"></a><span data-ttu-id="5db1f-120">Asiakasryhmän määritysten hallinta</span><span class="sxs-lookup"><span data-stu-id="5db1f-120">Manage customer group assignments</span></span>

<span data-ttu-id="5db1f-121">Kukin asiakas voi kuulua mihin tahansa määrään ostohyvityksen hallintaryhmiä.</span><span class="sxs-lookup"><span data-stu-id="5db1f-121">Each customer can belong to any number of Rebate management groups.</span></span> <span data-ttu-id="5db1f-122">Jos haluat tarkastella ja liittää ryhmän jäseniä, voit aloittaa joko ryhmäluettelosta tai asiakasluettelosta.</span><span class="sxs-lookup"><span data-stu-id="5db1f-122">To view and assign group members, you can start from either the group list or the customer list.</span></span>

<span data-ttu-id="5db1f-123">Noudattamalla seuraavia ohjeita voit tarkastella, lisätä tai poistaa valitun ryhmän asiakkaita.</span><span class="sxs-lookup"><span data-stu-id="5db1f-123">To view, add, or remove customers for a selected group, follow these steps.</span></span>

1. <span data-ttu-id="5db1f-124">Siirry kohtaan **Ostohyvitysten hallinta \> Ostohyvitysten hallintaryhmien asetukset \> Asiakasryhmät**.</span><span class="sxs-lookup"><span data-stu-id="5db1f-124">Go to **Rebate management \> Rebate management groups setup \> Customer groups**.</span></span>
1. <span data-ttu-id="5db1f-125">Valitse hallittava ryhmä.</span><span class="sxs-lookup"><span data-stu-id="5db1f-125">Select the group to manage.</span></span>
1. <span data-ttu-id="5db1f-126">Valitse toimintoruudussa **Asiakkaat**.</span><span class="sxs-lookup"><span data-stu-id="5db1f-126">On the Action Pane, select **Customers**.</span></span> <span data-ttu-id="5db1f-127">Näkyviin tulee **Ostohyvityksen hallintaryhmät** -sivu, joka sisältää luettelon asiakkaista, jotka kuuluvat jo valittuun ryhmään.</span><span class="sxs-lookup"><span data-stu-id="5db1f-127">The **Rebate management groups** page appears and shows a list of customers that are already members of the selected group.</span></span>
1. <span data-ttu-id="5db1f-128">Lisää uusi asiakas ryhmään valitsemalla toimintoruudussa **Uusi**, mikä lisää rivin ruudukkoon.</span><span class="sxs-lookup"><span data-stu-id="5db1f-128">To add a new customer to the group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="5db1f-129">Määritä sitten uudelle rivillä seuraavat kentät:</span><span class="sxs-lookup"><span data-stu-id="5db1f-129">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="5db1f-130">**Asiakastili** – Valitse asiakastilin tunnus.</span><span class="sxs-lookup"><span data-stu-id="5db1f-130">**Customer account** – Select the customer account ID.</span></span>
    - <span data-ttu-id="5db1f-131">**Nimi** – Kirjoita asiakkaan nimi ja/tai kuvaus.</span><span class="sxs-lookup"><span data-stu-id="5db1f-131">**Name** – Enter a name and/or description of the customer.</span></span>

1. <span data-ttu-id="5db1f-132">Jos haluat poistaa asiakkaan ryhmästä, valitse asiakas ja valitse sitten toimintoruudusta **Poista**.</span><span class="sxs-lookup"><span data-stu-id="5db1f-132">To remove a customer from the group, select the customer, and then select **Delete** on the Action Pane.</span></span>

<span data-ttu-id="5db1f-133">Noudattamalla seuraavia ohjeita voit tarkastella, lisätä tai poistaa valitun asiakkaan ryhmämäärityksiä.</span><span class="sxs-lookup"><span data-stu-id="5db1f-133">To view, add, or remove group assignments for a selected customer, follow these steps.</span></span>

1. <span data-ttu-id="5db1f-134">Siirry kohtaan **Myyntireskontra \> Asiakkaat \> Kaikki asiakkaat**.</span><span class="sxs-lookup"><span data-stu-id="5db1f-134">Go to **Accounts receivable \> Customers \> All customers**.</span></span>
1. <span data-ttu-id="5db1f-135">Valitse asiakas, jonka kanssa haluat työskennellä.</span><span class="sxs-lookup"><span data-stu-id="5db1f-135">Select the customer to work with.</span></span>
1. <span data-ttu-id="5db1f-136">Valitse toimintoruudun **Asiakas**-välilehden **Ostohyvitysten hallinta** -ryhmässä **Ostohyvitysten hallintaryhmät**.</span><span class="sxs-lookup"><span data-stu-id="5db1f-136">On the Action Pane, on the **Customer** tab, in the **Rebate management** group, select **Rebate management groups**.</span></span> <span data-ttu-id="5db1f-137">Näkyviin tulee **Ostohyvityksen hallintaryhmät** -sivu, joka sisältää luettelon ryhmistä, joihin valittu asiakas jo kuuluu.</span><span class="sxs-lookup"><span data-stu-id="5db1f-137">The **Rebate management groups** page appears and shows a list of groups that the selected customer already belongs to.</span></span>
1. <span data-ttu-id="5db1f-138">Lisää asiakas uuteen ryhmään valitsemalla toimintoruudussa **Uusi**, mikä lisää rivin ruudukkoon.</span><span class="sxs-lookup"><span data-stu-id="5db1f-138">To add the customer to a new group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="5db1f-139">Määritä sitten uudelle rivillä seuraavat kentät:</span><span class="sxs-lookup"><span data-stu-id="5db1f-139">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="5db1f-140">**Ostohyvityksen hallintaryhmä** – Valitse ryhmä, johon asiakas lisätään.</span><span class="sxs-lookup"><span data-stu-id="5db1f-140">**Rebate management group** – Select the group to add the customer to.</span></span>
    - <span data-ttu-id="5db1f-141">**Kuvaus** – Kirjoita ryhmän kuvaus (esimerkiksi se, miksi asiakas on ryhmän jäsen).</span><span class="sxs-lookup"><span data-stu-id="5db1f-141">**Description** – Enter a description of the group (for example, to explain why the customer is a member of it).</span></span>

1. <span data-ttu-id="5db1f-142">Jos haluat poistaa asiakkaan ryhmästä, valitse ryhmä ja valitse sitten toimintoruudusta **Poista**.</span><span class="sxs-lookup"><span data-stu-id="5db1f-142">To remove a customer from a group, select the group, and then select **Delete** on the Action Pane.</span></span>

## <a name="rebate-management-vendor-groups"></a><span data-ttu-id="5db1f-143">Ostohyvitysten hallinnan toimittajaryhmät</span><span class="sxs-lookup"><span data-stu-id="5db1f-143">Rebate management vendor groups</span></span>

<span data-ttu-id="5db1f-144">Toimittajaryhmän laskenta luodaan usein toimituspisteiden ryhmälle.</span><span class="sxs-lookup"><span data-stu-id="5db1f-144">The calculation for a group of vendors is often created for a group of delivery points.</span></span> <span data-ttu-id="5db1f-145">Tämäntyyppinen laskentatapa liittyy yleensä ostohyvitykseen.</span><span class="sxs-lookup"><span data-stu-id="5db1f-145">This type of calculation is usually related to a rebate.</span></span>

### <a name="set-up-vendor-groups"></a><span data-ttu-id="5db1f-146">Toimittajaryhmien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="5db1f-146">Set up vendor groups</span></span>

<span data-ttu-id="5db1f-147">Voit käyttää ostohyvityksen hallinnan toimittajaryhmiä kohdassa **Ostohyvitysten hallinta \> Ostohyvitysten hallintaryhmien asetukset \> Toimittajaryhmät**.</span><span class="sxs-lookup"><span data-stu-id="5db1f-147">To work with Rebate management vendor groups, go to **Rebate management \> Rebate management groups setup \> Vendor groups**.</span></span> <span data-ttu-id="5db1f-148">Voit lisätä ja poistaa ryhmiä tarpeen mukaan käyttämällä toimintoruudun painikkeita.</span><span class="sxs-lookup"><span data-stu-id="5db1f-148">You can use the buttons on the Action Pane to add and remove groups as required.</span></span> <span data-ttu-id="5db1f-149">Määritä kullekin ryhmälle seuraavat kentät:</span><span class="sxs-lookup"><span data-stu-id="5db1f-149">For each group, set the following fields:</span></span>

- <span data-ttu-id="5db1f-150">**Ostohyvitysten hallintaryhmä** – Anna ryhmän yksilöivä nimi.</span><span class="sxs-lookup"><span data-stu-id="5db1f-150">**Rebate management group** – Enter a unique name for the group.</span></span>
- <span data-ttu-id="5db1f-151">**Kuvaus** – Syötä ryhmän kuvaus, joka sisältää lisätietoja ryhmän käytöstä.</span><span class="sxs-lookup"><span data-stu-id="5db1f-151">**Description** – Enter a description of the group to provide more information about how it should be used.</span></span>

### <a name="manage-vendor-group-assignments"></a><span data-ttu-id="5db1f-152">Toimittajaryhmän määritysten hallinta</span><span class="sxs-lookup"><span data-stu-id="5db1f-152">Manage vendor group assignments</span></span>

<span data-ttu-id="5db1f-153">Kukin toimittaja voi kuulua mihin tahansa määrään ostohyvityksen hallintaryhmiä.</span><span class="sxs-lookup"><span data-stu-id="5db1f-153">Each vendor can belong to any number of Rebate management groups.</span></span> <span data-ttu-id="5db1f-154">Jos haluat tarkastella ja liittää ryhmän jäseniä, voit aloittaa joko ryhmäluettelosta tai toimittajaluettelosta.</span><span class="sxs-lookup"><span data-stu-id="5db1f-154">To view and assign group members, you can start from either the group list or the vendor list.</span></span>

<span data-ttu-id="5db1f-155">Noudattamalla seuraavia ohjeita voit tarkastella, lisätä tai poistaa valitun ryhmän toimittajia.</span><span class="sxs-lookup"><span data-stu-id="5db1f-155">To view, add, or remove vendors for a selected group, follow these steps.</span></span>

1. <span data-ttu-id="5db1f-156">Siirry kohtaan **Ostohyvitysten hallinta \> Ostohyvitysten hallintaryhmien asetukset \> Toimittajaryhmät**.</span><span class="sxs-lookup"><span data-stu-id="5db1f-156">Go to **Rebate management \> Rebate management groups setup \> Vendor groups**.</span></span>
1. <span data-ttu-id="5db1f-157">Valitse hallittava ryhmä.</span><span class="sxs-lookup"><span data-stu-id="5db1f-157">Select the group to manage.</span></span>
1. <span data-ttu-id="5db1f-158">Valitse toimintoruudussa **Toimittajat**.</span><span class="sxs-lookup"><span data-stu-id="5db1f-158">On the Action Pane, select **Vendors**.</span></span> <span data-ttu-id="5db1f-159">Näkyviin tulee **Ostohyvityksen hallintaryhmät** -sivu, joka sisältää luettelon toimittajista, jotka kuuluvat jo valittuun ryhmään.</span><span class="sxs-lookup"><span data-stu-id="5db1f-159">The **Rebate management groups** page appears and shows a list of vendors that are already members of the selected group.</span></span>
1. <span data-ttu-id="5db1f-160">Lisää uusi toimittaja ryhmään valitsemalla toimintoruudussa **Uusi**, mikä lisää rivin ruudukkoon.</span><span class="sxs-lookup"><span data-stu-id="5db1f-160">To add a new vendor to the group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="5db1f-161">Määritä sitten uudelle rivillä seuraavat kentät:</span><span class="sxs-lookup"><span data-stu-id="5db1f-161">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="5db1f-162">**Toimittajatili** – Valitse toimittajatilin tunnus.</span><span class="sxs-lookup"><span data-stu-id="5db1f-162">**Vendor account** – Select the vendor account ID.</span></span>
    - <span data-ttu-id="5db1f-163">**Nimi** – Kirjoita toimittajan nimi ja/tai kuvaus.</span><span class="sxs-lookup"><span data-stu-id="5db1f-163">**Name** – Enter a name and/or description of the vendor.</span></span>

1. <span data-ttu-id="5db1f-164">Jos haluat poistaa toimittajan ryhmästä, valitse toimittaja ja valitse sitten toimintoruudusta **Poista**.</span><span class="sxs-lookup"><span data-stu-id="5db1f-164">To remove a vendor from the group, select the vendor, and then select **Delete** on the Action Pane.</span></span>

<span data-ttu-id="5db1f-165">Noudattamalla seuraavia ohjeita voit tarkastella, lisätä tai poistaa valitun toimittajan ryhmämäärityksiä.</span><span class="sxs-lookup"><span data-stu-id="5db1f-165">To view, add, or remove group assignments for a selected vendor, follow these steps.</span></span>

1. <span data-ttu-id="5db1f-166">Siirry kohtaan **Ostoreskontra \> Toimittajat \> Kaikki toimittajat**.</span><span class="sxs-lookup"><span data-stu-id="5db1f-166">Go to **Accounts payable \> Vendors \> All vendors**.</span></span>
1. <span data-ttu-id="5db1f-167">Valitse toimittaja, jonka kanssa haluat työskennellä.</span><span class="sxs-lookup"><span data-stu-id="5db1f-167">Select the vendor to work with.</span></span>
1. <span data-ttu-id="5db1f-168">Valitse toimintoruudun **Toimittaja**-välilehden **Ostohyvitysten hallinta** -ryhmässä **Ostohyvitysten hallintaryhmät**.</span><span class="sxs-lookup"><span data-stu-id="5db1f-168">On the Action Pane, on the **Vendor** tab, in the **Rebate management** group, select **Rebate management groups**.</span></span> <span data-ttu-id="5db1f-169">Näkyviin tulee **Ostohyvityksen hallintaryhmät** -sivu, joka sisältää luettelon ryhmistä, joihin valittu toimittaja jo kuuluu.</span><span class="sxs-lookup"><span data-stu-id="5db1f-169">The **Rebate management groups** page appears and shows a list of groups that the selected vendor already belongs to.</span></span>
1. <span data-ttu-id="5db1f-170">Lisää toimittaja uuteen ryhmään valitsemalla toimintoruudussa **Uusi**, mikä lisää rivin ruudukkoon.</span><span class="sxs-lookup"><span data-stu-id="5db1f-170">To add the vendor to a new group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="5db1f-171">Määritä sitten uudelle rivillä seuraavat kentät:</span><span class="sxs-lookup"><span data-stu-id="5db1f-171">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="5db1f-172">**Ostohyvityksen hallintaryhmä** – Valitse ryhmä, johon toimittaja lisätään.</span><span class="sxs-lookup"><span data-stu-id="5db1f-172">**Rebate management group** – Select the group to add the vendor to.</span></span>
    - <span data-ttu-id="5db1f-173">**Kuvaus** – Kirjoita ryhmän kuvaus (esimerkiksi se, miksi toimittaja on ryhmän jäsen).</span><span class="sxs-lookup"><span data-stu-id="5db1f-173">**Description** – Enter a description of the group (for example, to explain why the vendor is a member of it).</span></span>

1. <span data-ttu-id="5db1f-174">Jos haluat poistaa toimittajan ryhmästä, valitse ryhmä ja valitse sitten toimintoruudusta **Poista**.</span><span class="sxs-lookup"><span data-stu-id="5db1f-174">To remove a vendor from a group, select the group, and then select **Delete** on the Action Pane.</span></span>

## <a name="item-rebate-groups"></a><span data-ttu-id="5db1f-175">Nimikkeen ostohyvitysryhmät</span><span class="sxs-lookup"><span data-stu-id="5db1f-175">Item rebate groups</span></span>

<span data-ttu-id="5db1f-176">Nimikkeitä ryhmittelemällä saat enemmän joustavuutta ostohyvitysten ja vähennysten laskennan ajoitukseen.</span><span class="sxs-lookup"><span data-stu-id="5db1f-176">By grouping items, you have more flexibility when rebates and deductions are calculated.</span></span> <span data-ttu-id="5db1f-177">Tämä on usein tehokkaampi tapa määrittää asiakkaille ja toimittajille ostohyvitykset ja vähennykset.</span><span class="sxs-lookup"><span data-stu-id="5db1f-177">This approach is often a more efficient way to set up rebates and deductions for customers and vendors.</span></span>

### <a name="set-up-item-groups"></a><span data-ttu-id="5db1f-178">Määritä nimikeryhmät</span><span class="sxs-lookup"><span data-stu-id="5db1f-178">Set up item groups</span></span>

<span data-ttu-id="5db1f-179">Voit käyttää ostohyvityksen hallinnan nimikeryhmiä kohdassa **Ostohyvitysten hallinta \> Ostohyvitysten hallintaryhmien asetukset \> Nimikeryhmät**.</span><span class="sxs-lookup"><span data-stu-id="5db1f-179">To work with Rebate management item groups, go to **Rebate management \> Rebate management groups setup \> Item groups**.</span></span> <span data-ttu-id="5db1f-180">Voit lisätä ja poistaa ryhmiä tarpeen mukaan käyttämällä toimintoruudun painikkeita.</span><span class="sxs-lookup"><span data-stu-id="5db1f-180">You can use the buttons on the Action Pane to add and remove groups as required.</span></span> <span data-ttu-id="5db1f-181">Määritä kullekin ryhmälle seuraavat kentät:</span><span class="sxs-lookup"><span data-stu-id="5db1f-181">For each group, set the following fields:</span></span>

- <span data-ttu-id="5db1f-182">**Ostohyvitysten hallintaryhmä** – Anna ryhmän yksilöivä nimi.</span><span class="sxs-lookup"><span data-stu-id="5db1f-182">**Rebate management group** – Enter a unique name for the group.</span></span>
- <span data-ttu-id="5db1f-183">**Kuvaus** – Syötä ryhmän kuvaus, joka sisältää lisätietoja ryhmän käytöstä.</span><span class="sxs-lookup"><span data-stu-id="5db1f-183">**Description** – Enter a description of the group to provide more information about how it should be used.</span></span>

### <a name="manage-item-group-assignments"></a><span data-ttu-id="5db1f-184">Nimikeryhmän määritysten hallinta</span><span class="sxs-lookup"><span data-stu-id="5db1f-184">Manage item group assignments</span></span>

<span data-ttu-id="5db1f-185">Kukin nimike voi kuulua mihin tahansa määrään ostohyvityksen hallintaryhmiä.</span><span class="sxs-lookup"><span data-stu-id="5db1f-185">Each item can belong to any number of Rebate management groups.</span></span> <span data-ttu-id="5db1f-186">Jos haluat tarkastella ja liittää ryhmän jäseniä, voit aloittaa joko ryhmäluettelosta tai nimikeluettelosta.</span><span class="sxs-lookup"><span data-stu-id="5db1f-186">To view and assign group members, you can start from either the group list or the item list.</span></span> <span data-ttu-id="5db1f-187">Voit myös lisätä nimikkeitä luokkahierarkian mukaan.</span><span class="sxs-lookup"><span data-stu-id="5db1f-187">You can also add items based on your category hierarchy.</span></span>

<span data-ttu-id="5db1f-188">Noudattamalla seuraavia ohjeita voit tarkastella, lisätä tai poistaa valitun ryhmän nimikkeitä.</span><span class="sxs-lookup"><span data-stu-id="5db1f-188">To view, add, or remove items for a selected group, follow these steps.</span></span>

1. <span data-ttu-id="5db1f-189">Siirry kohtaan **Ostohyvitysten hallinta \> Ostohyvitysten hallintaryhmien asetukset \> Nimikeryhmät**.</span><span class="sxs-lookup"><span data-stu-id="5db1f-189">Go to **Rebate management \> Rebate management groups setup \> Item groups**.</span></span>
1. <span data-ttu-id="5db1f-190">Valitse hallittava ryhmä.</span><span class="sxs-lookup"><span data-stu-id="5db1f-190">Select the group to manage.</span></span>
1. <span data-ttu-id="5db1f-191">Valitse toimintoruudussa **Nimikkeet**.</span><span class="sxs-lookup"><span data-stu-id="5db1f-191">On the Action Pane, select **Items**.</span></span> <span data-ttu-id="5db1f-192">Näkyviin tulee **Ostohyvityksen hallintaryhmät** -sivu, joka sisältää luettelon nimikkeistä, jotka kuuluvat jo valittuun ryhmään.</span><span class="sxs-lookup"><span data-stu-id="5db1f-192">The **Rebate management groups** page appears and shows a list of items that are already members of the selected group.</span></span>
1. <span data-ttu-id="5db1f-193">Lisää uusi nimike ryhmään valitsemalla toimintoruudussa **Uusi**, mikä lisää rivin ruudukkoon.</span><span class="sxs-lookup"><span data-stu-id="5db1f-193">To add a new item to the group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="5db1f-194">Määritä sitten uudelle rivillä seuraavat kentät:</span><span class="sxs-lookup"><span data-stu-id="5db1f-194">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="5db1f-195">**Nimikejatili** – Valitse nimiketilin tunnus.</span><span class="sxs-lookup"><span data-stu-id="5db1f-195">**Item account** – Select the item account ID.</span></span>
    - <span data-ttu-id="5db1f-196">**Tuotteen nimi** – Kirjoita nimikkeen nimi ja/tai kuvaus.</span><span class="sxs-lookup"><span data-stu-id="5db1f-196">**Product name** – Enter a name and/or description of the item.</span></span>

1. <span data-ttu-id="5db1f-197">Jos haluat poistaa nimikkeen ryhmästä, valitse nimike ja valitse sitten toimintoruudusta **Poista**.</span><span class="sxs-lookup"><span data-stu-id="5db1f-197">To remove an item from the group, select the item, and then select **Delete** on the Action Pane.</span></span>

<span data-ttu-id="5db1f-198">Noudattamalla seuraavia ohjeita voit tarkastella, lisätä tai poistaa valitun nimikkeen ryhmämäärityksiä.</span><span class="sxs-lookup"><span data-stu-id="5db1f-198">To view, add, or remove group assignments for a selected item, follow these steps.</span></span>

1. <span data-ttu-id="5db1f-199">Mene **Tuotetietojen hallinta \> Tuotteet \> Vapautetut tuotteet**.</span><span class="sxs-lookup"><span data-stu-id="5db1f-199">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="5db1f-200">Valitse nimike, jonka kanssa haluat työskennellä.</span><span class="sxs-lookup"><span data-stu-id="5db1f-200">Select the item to work with.</span></span>
1. <span data-ttu-id="5db1f-201">Valitse toimintoruudun **Tuote**-välilehden **Ostohyvitysten hallinta** -ryhmässä **Ostohyvitysten hallintaryhmät**.</span><span class="sxs-lookup"><span data-stu-id="5db1f-201">On the Action Pane, on the **Product** tab, in the **Rebate management** group, select **Rebate management groups**.</span></span> <span data-ttu-id="5db1f-202">Näkyviin tulee **Ostohyvityksen hallintaryhmät** -sivu, joka sisältää luettelon ryhmistä, joihin valittu nimike jo kuuluu.</span><span class="sxs-lookup"><span data-stu-id="5db1f-202">The **Rebate management groups** page appears and shows a list of groups that the selected item already belongs to.</span></span>
1. <span data-ttu-id="5db1f-203">Lisää nimike uuteen ryhmään valitsemalla toimintoruudussa **Uusi**, mikä lisää rivin ruudukkoon.</span><span class="sxs-lookup"><span data-stu-id="5db1f-203">To add the item to a new group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="5db1f-204">Määritä sitten uudelle rivillä seuraavat kentät:</span><span class="sxs-lookup"><span data-stu-id="5db1f-204">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="5db1f-205">**Ostohyvityksen hallintaryhmä** – Valitse ryhmä, johon nimike lisätään.</span><span class="sxs-lookup"><span data-stu-id="5db1f-205">**Rebate management group** – Select the group to add the item to.</span></span>
    - <span data-ttu-id="5db1f-206">**Kuvaus** – Kirjoita ryhmän kuvaus (esimerkiksi se, miksi nimike on ryhmän jäsen).</span><span class="sxs-lookup"><span data-stu-id="5db1f-206">**Description** – Enter a description of the group (for example, to explain why the item is a member of it).</span></span>

1. <span data-ttu-id="5db1f-207">Jos haluat poistaa nimikkeen ryhmästä, valitse ryhmä ja valitse sitten toimintoruudusta **Poista**.</span><span class="sxs-lookup"><span data-stu-id="5db1f-207">To remove an item from a group, select the group, and then select **Delete** on the Action Pane.</span></span>

<span data-ttu-id="5db1f-208">Voit lisätä nimikkeitä ryhmään luokkahierarkian mukaan noudattamalla seuraavia vaiheita.</span><span class="sxs-lookup"><span data-stu-id="5db1f-208">To add items to a group based on your category hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="5db1f-209">Siirry kohtaan **Ostohyvitysten hallinta \> Ostohyvitysten hallintaryhmien asetukset \> Nimikeryhmät**.</span><span class="sxs-lookup"><span data-stu-id="5db1f-209">Go to **Rebate management \> Rebate management groups setup \> Item groups**.</span></span>
1. <span data-ttu-id="5db1f-210">Valitse hallittava ryhmä.</span><span class="sxs-lookup"><span data-stu-id="5db1f-210">Select the group to manage.</span></span>
1. <span data-ttu-id="5db1f-211">Valitse toimintoruudussa **Lisää nimikkeitä**.</span><span class="sxs-lookup"><span data-stu-id="5db1f-211">On the Action Pane, select **Add items**.</span></span>
1. <span data-ttu-id="5db1f-212">Valitse **Lisää nimikkeitä** -valintaikkunan **Luokkahierarkia**-kentästä ylätason luokka.</span><span class="sxs-lookup"><span data-stu-id="5db1f-212">In the **Add items** dialog box, in the **Category hierarchy** field, select a top-level category.</span></span>
1. <span data-ttu-id="5db1f-213">Nimikehierarkia avataan vasemmassa ruudussa.</span><span class="sxs-lookup"><span data-stu-id="5db1f-213">The item hierarchy is opened in the left pane.</span></span> <span data-ttu-id="5db1f-214">Valitse etsi haluamasi hierarkiataso.</span><span class="sxs-lookup"><span data-stu-id="5db1f-214">Select the hierarchy level that you're looking for.</span></span> 
1. <span data-ttu-id="5db1f-215">Valitun hierarkian ja hierarkiatason nimikkeet näkyvät nyt oikeanpuoleisessa ruudussa.</span><span class="sxs-lookup"><span data-stu-id="5db1f-215">Items from the selected hierarchy and hierarchy level are now listed in the right pane.</span></span> <span data-ttu-id="5db1f-216">Noudata seuraavia ohjeita, kun haluat käyttää ruutua:</span><span class="sxs-lookup"><span data-stu-id="5db1f-216">Follow these steps to work with the pane:</span></span>

    - <span data-ttu-id="5db1f-217">Valitse jokaisen lisättävän nimikkeen valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="5db1f-217">Select the check box for each item that you want to add.</span></span>
    - <span data-ttu-id="5db1f-218">Valitse kaikki luettelon nimikkeet valitsemalla ruudukon otsikon valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="5db1f-218">Select the check box on the grid header to select all the items that are listed.</span></span>
    - <span data-ttu-id="5db1f-219">Valitse **Näytä valitut** -painike, kun haluat suodattaa ruudukon siten, että siinä näkyvät vain tähän mennessä valitsemasi nimikkeet.</span><span class="sxs-lookup"><span data-stu-id="5db1f-219">Select the **Show selected** button to filter the grid so that it shows only the items that you've selected so far.</span></span> <span data-ttu-id="5db1f-220">Voit palata koko luetteloon valitsemalla painikkeen uudelleen.</span><span class="sxs-lookup"><span data-stu-id="5db1f-220">Select the button again to return to the full list.</span></span>

1. <span data-ttu-id="5db1f-221">Ota nimikevalinta käyttöön valitussa ryhmässä valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="5db1f-221">Select **OK** to apply your item selection to the selected group.</span></span>
