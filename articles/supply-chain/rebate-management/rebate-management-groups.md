---
title: Ostohyvitysten hallintaryhmät
description: Tässä aiheessa käsitellään ostohyvitysten hallintaryhmien määrittämistä. Ostohyvitysten hallintaryhmiä voi käyttää ostohyvitysten laskennassa, ja ne voidaan liittää päätietueeseen.
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TAMRebateGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: ee5a195b3d2881ff70fb1f0d4063ed681e874648
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/17/2021
ms.locfileid: "6271074"
---
# <a name="rebate-management-groups"></a><span data-ttu-id="9983f-104">Ostohyvitysten hallintaryhmät</span><span class="sxs-lookup"><span data-stu-id="9983f-104">Rebate management groups</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9983f-105">Ostohyvityksen hallintalaskelmat voidaan määrittää ryhmien perusteella.</span><span class="sxs-lookup"><span data-stu-id="9983f-105">Rebate management calculations can be driven by groups.</span></span> <span data-ttu-id="9983f-106">Ostohyvitysten hallintaryhmiä voi luoda asiakkaille, toimittajille ja nimikkeille.</span><span class="sxs-lookup"><span data-stu-id="9983f-106">Rebate management groups can be created for customers, vendors, and items.</span></span> <span data-ttu-id="9983f-107">Ne voidaan liittää päätietueeseen.</span><span class="sxs-lookup"><span data-stu-id="9983f-107">They can be attached to a master record.</span></span>

## <a name="rebate-management-customer-groups"></a><span data-ttu-id="9983f-108">Ostohyvitysten hallinnan asiakasryhmät</span><span class="sxs-lookup"><span data-stu-id="9983f-108">Rebate management customer groups</span></span>

<span data-ttu-id="9983f-109">Asiakasryhmän laskenta luodaan usein yritysketjulle, kuten marketketjulle tai franchise-yritykselle.</span><span class="sxs-lookup"><span data-stu-id="9983f-109">The calculation for a group of customers is often created for a chain of companies, such as a supermarket chain or a franchise company.</span></span> <span data-ttu-id="9983f-110">Tämäntyyppinen laskentatapa liittyy yleensä ostohyvitykseen.</span><span class="sxs-lookup"><span data-stu-id="9983f-110">This type of calculation is usually related to a rebate.</span></span>

<span data-ttu-id="9983f-111">Vähennys lasketaan usein niin, että ei oteta huomioon sitä, kenelle hyväksytty tilaus on myyty.</span><span class="sxs-lookup"><span data-stu-id="9983f-111">A deduction is often calculated without considering who the qualifying order was sold to.</span></span> <span data-ttu-id="9983f-112">Tähän on kuitenkin poikkeuksia.</span><span class="sxs-lookup"><span data-stu-id="9983f-112">However, there are exceptions.</span></span> <span data-ttu-id="9983f-113">Lisenssinhaltija voi esimerkiksi luoda vähennysmallin, johon asiakasryhmä A saa 4 prosenttia, mutta asiakasryhmä B saa vain 3 prosenttia.</span><span class="sxs-lookup"><span data-stu-id="9983f-113">For example, a licensee might create a deduction scheme where customer group A will receive 4 percent, but customer group B will receive only 3 percent.</span></span>

### <a name="set-up-customer-groups"></a><span data-ttu-id="9983f-114">Määritä asiakasryhmät</span><span class="sxs-lookup"><span data-stu-id="9983f-114">Set up customer groups</span></span>

<span data-ttu-id="9983f-115">Voit käyttää ostohyvityksen hallinnan asiakasryhmiä kohdassa **Ostohyvitysten hallinta \> Ostohyvitysten hallintaryhmien asetukset \> Asiakasryhmät**.</span><span class="sxs-lookup"><span data-stu-id="9983f-115">To work with Rebate management customer groups, go to **Rebate management \> Rebate management groups setup \> Customer groups**.</span></span> <span data-ttu-id="9983f-116">Voit lisätä ja poistaa ryhmiä tarpeen mukaan käyttämällä toimintoruudun painikkeita.</span><span class="sxs-lookup"><span data-stu-id="9983f-116">You can use the buttons on the Action Pane to add and remove groups as required.</span></span> <span data-ttu-id="9983f-117">Määritä kullekin ryhmälle seuraavat kentät:</span><span class="sxs-lookup"><span data-stu-id="9983f-117">For each group, set the following fields:</span></span>

- <span data-ttu-id="9983f-118">**Ostohyvitysten hallintaryhmä** – Anna ryhmän yksilöivä nimi.</span><span class="sxs-lookup"><span data-stu-id="9983f-118">**Rebate management group** – Enter a unique name for the group.</span></span>
- <span data-ttu-id="9983f-119">**Kuvaus** – Syötä ryhmän kuvaus, joka sisältää lisätietoja ryhmän käytöstä.</span><span class="sxs-lookup"><span data-stu-id="9983f-119">**Description** – Enter a description of the group to provide more information about how it should be used.</span></span>

### <a name="manage-customer-group-assignments"></a><span data-ttu-id="9983f-120">Asiakasryhmän määritysten hallinta</span><span class="sxs-lookup"><span data-stu-id="9983f-120">Manage customer group assignments</span></span>

<span data-ttu-id="9983f-121">Kukin asiakas voi kuulua mihin tahansa määrään ostohyvityksen hallintaryhmiä.</span><span class="sxs-lookup"><span data-stu-id="9983f-121">Each customer can belong to any number of Rebate management groups.</span></span> <span data-ttu-id="9983f-122">Jos haluat tarkastella ja liittää ryhmän jäseniä, voit aloittaa joko ryhmäluettelosta tai asiakasluettelosta.</span><span class="sxs-lookup"><span data-stu-id="9983f-122">To view and assign group members, you can start from either the group list or the customer list.</span></span>

<span data-ttu-id="9983f-123">Noudattamalla seuraavia ohjeita voit tarkastella, lisätä tai poistaa valitun ryhmän asiakkaita.</span><span class="sxs-lookup"><span data-stu-id="9983f-123">To view, add, or remove customers for a selected group, follow these steps.</span></span>

1. <span data-ttu-id="9983f-124">Siirry kohtaan **Ostohyvitysten hallinta \> Ostohyvitysten hallintaryhmien asetukset \> Asiakasryhmät**.</span><span class="sxs-lookup"><span data-stu-id="9983f-124">Go to **Rebate management \> Rebate management groups setup \> Customer groups**.</span></span>
1. <span data-ttu-id="9983f-125">Valitse hallittava ryhmä.</span><span class="sxs-lookup"><span data-stu-id="9983f-125">Select the group to manage.</span></span>
1. <span data-ttu-id="9983f-126">Valitse toimintoruudussa **Asiakkaat**.</span><span class="sxs-lookup"><span data-stu-id="9983f-126">On the Action Pane, select **Customers**.</span></span> <span data-ttu-id="9983f-127">Näkyviin tulee **Ostohyvityksen hallintaryhmät** -sivu, joka sisältää luettelon asiakkaista, jotka kuuluvat jo valittuun ryhmään.</span><span class="sxs-lookup"><span data-stu-id="9983f-127">The **Rebate management groups** page appears and shows a list of customers that are already members of the selected group.</span></span>
1. <span data-ttu-id="9983f-128">Lisää uusi asiakas ryhmään valitsemalla toimintoruudussa **Uusi**, mikä lisää rivin ruudukkoon.</span><span class="sxs-lookup"><span data-stu-id="9983f-128">To add a new customer to the group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="9983f-129">Määritä sitten uudelle rivillä seuraava kenttä:</span><span class="sxs-lookup"><span data-stu-id="9983f-129">Then set the following field for the new row:</span></span>

    - <span data-ttu-id="9983f-130">**Asiakastili** – Valitse asiakastilin tunnus.</span><span class="sxs-lookup"><span data-stu-id="9983f-130">**Customer account** – Select the customer account ID.</span></span>

1. <span data-ttu-id="9983f-131">Jos haluat poistaa asiakkaan ryhmästä, valitse asiakas ja valitse sitten toimintoruudusta **Poista**.</span><span class="sxs-lookup"><span data-stu-id="9983f-131">To remove a customer from the group, select the customer, and then select **Delete** on the Action Pane.</span></span>

<span data-ttu-id="9983f-132">Noudattamalla seuraavia ohjeita voit tarkastella, lisätä tai poistaa valitun asiakkaan ryhmämäärityksiä.</span><span class="sxs-lookup"><span data-stu-id="9983f-132">To view, add, or remove group assignments for a selected customer, follow these steps.</span></span>

1. <span data-ttu-id="9983f-133">Siirry kohtaan **Myyntireskontra \> Asiakkaat \> Kaikki asiakkaat**.</span><span class="sxs-lookup"><span data-stu-id="9983f-133">Go to **Accounts receivable \> Customers \> All customers**.</span></span>
1. <span data-ttu-id="9983f-134">Valitse asiakas, jonka kanssa haluat työskennellä.</span><span class="sxs-lookup"><span data-stu-id="9983f-134">Select the customer to work with.</span></span>
1. <span data-ttu-id="9983f-135">Valitse toimintoruudun **Asiakas**-välilehden **Ostohyvitysten hallinta** -ryhmässä **Ostohyvitysten hallintaryhmät**.</span><span class="sxs-lookup"><span data-stu-id="9983f-135">On the Action Pane, on the **Customer** tab, in the **Rebate management** group, select **Rebate management groups**.</span></span> <span data-ttu-id="9983f-136">Näkyviin tulee **Ostohyvityksen hallintaryhmät** -sivu, joka sisältää luettelon ryhmistä, joihin valittu asiakas jo kuuluu.</span><span class="sxs-lookup"><span data-stu-id="9983f-136">The **Rebate management groups** page appears and shows a list of groups that the selected customer already belongs to.</span></span>
1. <span data-ttu-id="9983f-137">Lisää asiakas uuteen ryhmään valitsemalla toimintoruudussa **Uusi**, mikä lisää rivin ruudukkoon.</span><span class="sxs-lookup"><span data-stu-id="9983f-137">To add the customer to a new group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="9983f-138">Määritä sitten uudelle rivillä seuraava kenttä:</span><span class="sxs-lookup"><span data-stu-id="9983f-138">Then set the following field for the new row:</span></span>

    - <span data-ttu-id="9983f-139">**Ostohyvityksen hallintaryhmä** – Valitse ryhmä, johon asiakas lisätään.</span><span class="sxs-lookup"><span data-stu-id="9983f-139">**Rebate management group** – Select the group to add the customer to.</span></span>

1. <span data-ttu-id="9983f-140">Jos haluat poistaa asiakkaan ryhmästä, valitse ryhmä ja valitse sitten toimintoruudusta **Poista**.</span><span class="sxs-lookup"><span data-stu-id="9983f-140">To remove a customer from a group, select the group, and then select **Delete** on the Action Pane.</span></span>

## <a name="rebate-management-vendor-groups"></a><span data-ttu-id="9983f-141">Ostohyvitysten hallinnan toimittajaryhmät</span><span class="sxs-lookup"><span data-stu-id="9983f-141">Rebate management vendor groups</span></span>

<span data-ttu-id="9983f-142">Toimittajaryhmän laskenta luodaan usein toimituspisteiden ryhmälle.</span><span class="sxs-lookup"><span data-stu-id="9983f-142">The calculation for a group of vendors is often created for a group of delivery points.</span></span> <span data-ttu-id="9983f-143">Tämäntyyppinen laskentatapa liittyy yleensä ostohyvitykseen.</span><span class="sxs-lookup"><span data-stu-id="9983f-143">This type of calculation is usually related to a rebate.</span></span>

### <a name="set-up-vendor-groups"></a><span data-ttu-id="9983f-144">Toimittajaryhmien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="9983f-144">Set up vendor groups</span></span>

<span data-ttu-id="9983f-145">Voit käyttää ostohyvityksen hallinnan toimittajaryhmiä kohdassa **Ostohyvitysten hallinta \> Ostohyvitysten hallintaryhmien asetukset \> Toimittajaryhmät**.</span><span class="sxs-lookup"><span data-stu-id="9983f-145">To work with Rebate management vendor groups, go to **Rebate management \> Rebate management groups setup \> Vendor groups**.</span></span> <span data-ttu-id="9983f-146">Voit lisätä ja poistaa ryhmiä tarpeen mukaan käyttämällä toimintoruudun painikkeita.</span><span class="sxs-lookup"><span data-stu-id="9983f-146">You can use the buttons on the Action Pane to add and remove groups as required.</span></span> <span data-ttu-id="9983f-147">Määritä kullekin ryhmälle seuraavat kentät:</span><span class="sxs-lookup"><span data-stu-id="9983f-147">For each group, set the following fields:</span></span>

- <span data-ttu-id="9983f-148">**Ostohyvitysten hallintaryhmä** – Anna ryhmän yksilöivä nimi.</span><span class="sxs-lookup"><span data-stu-id="9983f-148">**Rebate management group** – Enter a unique name for the group.</span></span>
- <span data-ttu-id="9983f-149">**Kuvaus** – Syötä ryhmän kuvaus, joka sisältää lisätietoja ryhmän käytöstä.</span><span class="sxs-lookup"><span data-stu-id="9983f-149">**Description** – Enter a description of the group to provide more information about how it should be used.</span></span>

### <a name="manage-vendor-group-assignments"></a><span data-ttu-id="9983f-150">Toimittajaryhmän määritysten hallinta</span><span class="sxs-lookup"><span data-stu-id="9983f-150">Manage vendor group assignments</span></span>

<span data-ttu-id="9983f-151">Kukin toimittaja voi kuulua mihin tahansa määrään ostohyvityksen hallintaryhmiä.</span><span class="sxs-lookup"><span data-stu-id="9983f-151">Each vendor can belong to any number of Rebate management groups.</span></span> <span data-ttu-id="9983f-152">Jos haluat tarkastella ja liittää ryhmän jäseniä, voit aloittaa joko ryhmäluettelosta tai toimittajaluettelosta.</span><span class="sxs-lookup"><span data-stu-id="9983f-152">To view and assign group members, you can start from either the group list or the vendor list.</span></span>

<span data-ttu-id="9983f-153">Noudattamalla seuraavia ohjeita voit tarkastella, lisätä tai poistaa valitun ryhmän toimittajia.</span><span class="sxs-lookup"><span data-stu-id="9983f-153">To view, add, or remove vendors for a selected group, follow these steps.</span></span>

1. <span data-ttu-id="9983f-154">Siirry kohtaan **Ostohyvitysten hallinta \> Ostohyvitysten hallintaryhmien asetukset \> Toimittajaryhmät**.</span><span class="sxs-lookup"><span data-stu-id="9983f-154">Go to **Rebate management \> Rebate management groups setup \> Vendor groups**.</span></span>
1. <span data-ttu-id="9983f-155">Valitse hallittava ryhmä.</span><span class="sxs-lookup"><span data-stu-id="9983f-155">Select the group to manage.</span></span>
1. <span data-ttu-id="9983f-156">Valitse toimintoruudussa **Toimittajat**.</span><span class="sxs-lookup"><span data-stu-id="9983f-156">On the Action Pane, select **Vendors**.</span></span> <span data-ttu-id="9983f-157">Näkyviin tulee **Ostohyvityksen hallintaryhmät** -sivu, joka sisältää luettelon toimittajista, jotka kuuluvat jo valittuun ryhmään.</span><span class="sxs-lookup"><span data-stu-id="9983f-157">The **Rebate management groups** page appears and shows a list of vendors that are already members of the selected group.</span></span>
1. <span data-ttu-id="9983f-158">Lisää uusi toimittaja ryhmään valitsemalla toimintoruudussa **Uusi**, mikä lisää rivin ruudukkoon.</span><span class="sxs-lookup"><span data-stu-id="9983f-158">To add a new vendor to the group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="9983f-159">Määritä sitten uudelle rivillä seuraava kenttä:</span><span class="sxs-lookup"><span data-stu-id="9983f-159">Then set the following field for the new row:</span></span>

    - <span data-ttu-id="9983f-160">**Toimittajatili** – Valitse toimittajatilin tunnus.</span><span class="sxs-lookup"><span data-stu-id="9983f-160">**Vendor account** – Select the vendor account ID.</span></span>

1. <span data-ttu-id="9983f-161">Jos haluat poistaa toimittajan ryhmästä, valitse toimittaja ja valitse sitten toimintoruudusta **Poista**.</span><span class="sxs-lookup"><span data-stu-id="9983f-161">To remove a vendor from the group, select the vendor, and then select **Delete** on the Action Pane.</span></span>

<span data-ttu-id="9983f-162">Noudattamalla seuraavia ohjeita voit tarkastella, lisätä tai poistaa valitun toimittajan ryhmämäärityksiä.</span><span class="sxs-lookup"><span data-stu-id="9983f-162">To view, add, or remove group assignments for a selected vendor, follow these steps.</span></span>

1. <span data-ttu-id="9983f-163">Siirry kohtaan **Ostoreskontra \> Toimittajat \> Kaikki toimittajat**.</span><span class="sxs-lookup"><span data-stu-id="9983f-163">Go to **Accounts payable \> Vendors \> All vendors**.</span></span>
1. <span data-ttu-id="9983f-164">Valitse toimittaja, jonka kanssa haluat työskennellä.</span><span class="sxs-lookup"><span data-stu-id="9983f-164">Select the vendor to work with.</span></span>
1. <span data-ttu-id="9983f-165">Valitse toimintoruudun **Toimittaja**-välilehden **Ostohyvitysten hallinta** -ryhmässä **Ostohyvitysten hallintaryhmät**.</span><span class="sxs-lookup"><span data-stu-id="9983f-165">On the Action Pane, on the **Vendor** tab, in the **Rebate management** group, select **Rebate management groups**.</span></span> <span data-ttu-id="9983f-166">Näkyviin tulee **Ostohyvityksen hallintaryhmät** -sivu, joka sisältää luettelon ryhmistä, joihin valittu toimittaja jo kuuluu.</span><span class="sxs-lookup"><span data-stu-id="9983f-166">The **Rebate management groups** page appears and shows a list of groups that the selected vendor already belongs to.</span></span>
1. <span data-ttu-id="9983f-167">Lisää toimittaja uuteen ryhmään valitsemalla toimintoruudussa **Uusi**, mikä lisää rivin ruudukkoon.</span><span class="sxs-lookup"><span data-stu-id="9983f-167">To add the vendor to a new group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="9983f-168">Määritä sitten uudelle rivillä seuraava kenttä:</span><span class="sxs-lookup"><span data-stu-id="9983f-168">Then set the following field for the new row:</span></span>

    - <span data-ttu-id="9983f-169">**Ostohyvityksen hallintaryhmä** – Valitse ryhmä, johon toimittaja lisätään.</span><span class="sxs-lookup"><span data-stu-id="9983f-169">**Rebate management group** – Select the group to add the vendor to.</span></span>

1. <span data-ttu-id="9983f-170">Jos haluat poistaa toimittajan ryhmästä, valitse ryhmä ja valitse sitten toimintoruudusta **Poista**.</span><span class="sxs-lookup"><span data-stu-id="9983f-170">To remove a vendor from a group, select the group, and then select **Delete** on the Action Pane.</span></span>

## <a name="item-rebate-groups"></a><span data-ttu-id="9983f-171">Nimikkeen ostohyvitysryhmät</span><span class="sxs-lookup"><span data-stu-id="9983f-171">Item rebate groups</span></span>

<span data-ttu-id="9983f-172">Nimikkeitä ryhmittelemällä saat enemmän joustavuutta ostohyvitysten ja vähennysten laskennan ajoitukseen.</span><span class="sxs-lookup"><span data-stu-id="9983f-172">By grouping items, you have more flexibility when rebates and deductions are calculated.</span></span> <span data-ttu-id="9983f-173">Tämä on usein tehokkaampi tapa määrittää asiakkaille ja toimittajille ostohyvitykset ja vähennykset.</span><span class="sxs-lookup"><span data-stu-id="9983f-173">This approach is often a more efficient way to set up rebates and deductions for customers and vendors.</span></span>

### <a name="set-up-item-groups"></a><span data-ttu-id="9983f-174">Määritä nimikeryhmät</span><span class="sxs-lookup"><span data-stu-id="9983f-174">Set up item groups</span></span>

<span data-ttu-id="9983f-175">Voit käyttää ostohyvityksen hallinnan nimikeryhmiä kohdassa **Ostohyvitysten hallinta \> Ostohyvitysten hallintaryhmien asetukset \> Nimikeryhmät**.</span><span class="sxs-lookup"><span data-stu-id="9983f-175">To work with Rebate management item groups, go to **Rebate management \> Rebate management groups setup \> Item groups**.</span></span> <span data-ttu-id="9983f-176">Voit lisätä ja poistaa ryhmiä tarpeen mukaan käyttämällä toimintoruudun painikkeita.</span><span class="sxs-lookup"><span data-stu-id="9983f-176">You can use the buttons on the Action Pane to add and remove groups as required.</span></span> <span data-ttu-id="9983f-177">Määritä kullekin ryhmälle seuraavat kentät:</span><span class="sxs-lookup"><span data-stu-id="9983f-177">For each group, set the following fields:</span></span>

- <span data-ttu-id="9983f-178">**Ostohyvitysten hallintaryhmä** – Anna ryhmän yksilöivä nimi.</span><span class="sxs-lookup"><span data-stu-id="9983f-178">**Rebate management group** – Enter a unique name for the group.</span></span>
- <span data-ttu-id="9983f-179">**Kuvaus** – Syötä ryhmän kuvaus, joka sisältää lisätietoja ryhmän käytöstä.</span><span class="sxs-lookup"><span data-stu-id="9983f-179">**Description** – Enter a description of the group to provide more information about how it should be used.</span></span>

### <a name="manage-item-group-assignments"></a><span data-ttu-id="9983f-180">Nimikeryhmän määritysten hallinta</span><span class="sxs-lookup"><span data-stu-id="9983f-180">Manage item group assignments</span></span>

<span data-ttu-id="9983f-181">Kukin nimike voi kuulua mihin tahansa määrään ostohyvityksen hallintaryhmiä.</span><span class="sxs-lookup"><span data-stu-id="9983f-181">Each item can belong to any number of Rebate management groups.</span></span> <span data-ttu-id="9983f-182">Jos haluat tarkastella ja liittää ryhmän jäseniä, voit aloittaa joko ryhmäluettelosta tai nimikeluettelosta.</span><span class="sxs-lookup"><span data-stu-id="9983f-182">To view and assign group members, you can start from either the group list or the item list.</span></span> <span data-ttu-id="9983f-183">Voit myös lisätä nimikkeitä luokkahierarkian mukaan.</span><span class="sxs-lookup"><span data-stu-id="9983f-183">You can also add items based on your category hierarchy.</span></span>

<span data-ttu-id="9983f-184">Noudattamalla seuraavia ohjeita voit tarkastella, lisätä tai poistaa valitun ryhmän nimikkeitä.</span><span class="sxs-lookup"><span data-stu-id="9983f-184">To view, add, or remove items for a selected group, follow these steps.</span></span>

1. <span data-ttu-id="9983f-185">Siirry kohtaan **Ostohyvitysten hallinta \> Ostohyvitysten hallintaryhmien asetukset \> Nimikeryhmät**.</span><span class="sxs-lookup"><span data-stu-id="9983f-185">Go to **Rebate management \> Rebate management groups setup \> Item groups**.</span></span>
1. <span data-ttu-id="9983f-186">Valitse hallittava ryhmä.</span><span class="sxs-lookup"><span data-stu-id="9983f-186">Select the group to manage.</span></span>
1. <span data-ttu-id="9983f-187">Valitse toimintoruudussa **Nimikkeet**.</span><span class="sxs-lookup"><span data-stu-id="9983f-187">On the Action Pane, select **Items**.</span></span> <span data-ttu-id="9983f-188">Näkyviin tulee **Ostohyvityksen hallintaryhmät** -sivu, joka sisältää luettelon nimikkeistä, jotka kuuluvat jo valittuun ryhmään.</span><span class="sxs-lookup"><span data-stu-id="9983f-188">The **Rebate management groups** page appears and shows a list of items that are already members of the selected group.</span></span>
1. <span data-ttu-id="9983f-189">Lisää uusi nimike ryhmään valitsemalla toimintoruudussa **Uusi**, mikä lisää rivin ruudukkoon.</span><span class="sxs-lookup"><span data-stu-id="9983f-189">To add a new item to the group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="9983f-190">Määritä sitten uudelle rivillä seuraava kenttä:</span><span class="sxs-lookup"><span data-stu-id="9983f-190">Then set the following field for the new row:</span></span>

    - <span data-ttu-id="9983f-191">**Nimikejatili** – Valitse nimiketilin tunnus.</span><span class="sxs-lookup"><span data-stu-id="9983f-191">**Item account** – Select the item account ID.</span></span>

1. <span data-ttu-id="9983f-192">Jos haluat poistaa nimikkeen ryhmästä, valitse nimike ja valitse sitten toimintoruudusta **Poista**.</span><span class="sxs-lookup"><span data-stu-id="9983f-192">To remove an item from the group, select the item, and then select **Delete** on the Action Pane.</span></span>

<span data-ttu-id="9983f-193">Noudattamalla seuraavia ohjeita voit tarkastella, lisätä tai poistaa valitun nimikkeen ryhmämäärityksiä.</span><span class="sxs-lookup"><span data-stu-id="9983f-193">To view, add, or remove group assignments for a selected item, follow these steps.</span></span>

1. <span data-ttu-id="9983f-194">Mene **Tuotetietojen hallinta \> Tuotteet \> Vapautetut tuotteet**.</span><span class="sxs-lookup"><span data-stu-id="9983f-194">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="9983f-195">Valitse nimike, jonka kanssa haluat työskennellä.</span><span class="sxs-lookup"><span data-stu-id="9983f-195">Select the item to work with.</span></span>
1. <span data-ttu-id="9983f-196">Valitse toimintoruudun **Tuote**-välilehden **Ostohyvitysten hallinta** -ryhmässä **Ostohyvitysten hallintaryhmät**.</span><span class="sxs-lookup"><span data-stu-id="9983f-196">On the Action Pane, on the **Product** tab, in the **Rebate management** group, select **Rebate management groups**.</span></span> <span data-ttu-id="9983f-197">Näkyviin tulee **Ostohyvityksen hallintaryhmät** -sivu, joka sisältää luettelon ryhmistä, joihin valittu nimike jo kuuluu.</span><span class="sxs-lookup"><span data-stu-id="9983f-197">The **Rebate management groups** page appears and shows a list of groups that the selected item already belongs to.</span></span>
1. <span data-ttu-id="9983f-198">Lisää nimike uuteen ryhmään valitsemalla toimintoruudussa **Uusi**, mikä lisää rivin ruudukkoon.</span><span class="sxs-lookup"><span data-stu-id="9983f-198">To add the item to a new group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="9983f-199">Määritä sitten uudelle rivillä seuraava kenttä:</span><span class="sxs-lookup"><span data-stu-id="9983f-199">Then set the following field for the new row:</span></span>

    - <span data-ttu-id="9983f-200">**Ostohyvityksen hallintaryhmä** – Valitse ryhmä, johon nimike lisätään.</span><span class="sxs-lookup"><span data-stu-id="9983f-200">**Rebate management group** – Select the group to add the item to.</span></span>

1. <span data-ttu-id="9983f-201">Jos haluat poistaa nimikkeen ryhmästä, valitse ryhmä ja valitse sitten toimintoruudusta **Poista**.</span><span class="sxs-lookup"><span data-stu-id="9983f-201">To remove an item from a group, select the group, and then select **Delete** on the Action Pane.</span></span>

<span data-ttu-id="9983f-202">Voit lisätä nimikkeitä ryhmään luokkahierarkian mukaan noudattamalla seuraavia vaiheita.</span><span class="sxs-lookup"><span data-stu-id="9983f-202">To add items to a group based on your category hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="9983f-203">Siirry kohtaan **Ostohyvitysten hallinta \> Ostohyvitysten hallintaryhmien asetukset \> Nimikeryhmät**.</span><span class="sxs-lookup"><span data-stu-id="9983f-203">Go to **Rebate management \> Rebate management groups setup \> Item groups**.</span></span>
1. <span data-ttu-id="9983f-204">Valitse hallittava ryhmä.</span><span class="sxs-lookup"><span data-stu-id="9983f-204">Select the group to manage.</span></span>
1. <span data-ttu-id="9983f-205">Valitse toimintoruudussa **Lisää nimikkeitä**.</span><span class="sxs-lookup"><span data-stu-id="9983f-205">On the Action Pane, select **Add items**.</span></span>
1. <span data-ttu-id="9983f-206">Valitse **Lisää nimikkeitä** -valintaikkunan **Luokkahierarkia**-kentästä ylätason luokka.</span><span class="sxs-lookup"><span data-stu-id="9983f-206">In the **Add items** dialog box, in the **Category hierarchy** field, select a top-level category.</span></span>
1. <span data-ttu-id="9983f-207">Nimikehierarkia avataan vasemmassa ruudussa.</span><span class="sxs-lookup"><span data-stu-id="9983f-207">The item hierarchy is opened in the left pane.</span></span> <span data-ttu-id="9983f-208">Valitse etsi haluamasi hierarkiataso.</span><span class="sxs-lookup"><span data-stu-id="9983f-208">Select the hierarchy level that you're looking for.</span></span> 
1. <span data-ttu-id="9983f-209">Valitun hierarkian ja hierarkiatason nimikkeet näkyvät nyt oikeanpuoleisessa ruudussa.</span><span class="sxs-lookup"><span data-stu-id="9983f-209">Items from the selected hierarchy and hierarchy level are now listed in the right pane.</span></span> <span data-ttu-id="9983f-210">Noudata seuraavia ohjeita, kun haluat käyttää ruutua:</span><span class="sxs-lookup"><span data-stu-id="9983f-210">Follow these steps to work with the pane:</span></span>

    - <span data-ttu-id="9983f-211">Valitse jokaisen lisättävän nimikkeen valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="9983f-211">Select the check box for each item that you want to add.</span></span>
    - <span data-ttu-id="9983f-212">Valitse kaikki luettelon nimikkeet valitsemalla ruudukon otsikon valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="9983f-212">Select the check box on the grid header to select all the items that are listed.</span></span>
    - <span data-ttu-id="9983f-213">Valitse **Näytä valitut** -painike, kun haluat suodattaa ruudukon siten, että siinä näkyvät vain tähän mennessä valitsemasi nimikkeet.</span><span class="sxs-lookup"><span data-stu-id="9983f-213">Select the **Show selected** button to filter the grid so that it shows only the items that you've selected so far.</span></span> <span data-ttu-id="9983f-214">Voit palata koko luetteloon valitsemalla painikkeen uudelleen.</span><span class="sxs-lookup"><span data-stu-id="9983f-214">Select the button again to return to the full list.</span></span>

1. <span data-ttu-id="9983f-215">Ota nimikevalinta käyttöön valitussa ryhmässä valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="9983f-215">Select **OK** to apply your item selection to the selected group.</span></span>
