---
title: "Arvonlisäveron laskentatavat Alkuperä-kentässä"
description: "Tässä artikkelissa käsitellään arvonlisäveron koodisivun Peruste-kentän vaihtoehtoja sekä sitä, miten arvonlisävero lasketaan valitun vaihtoehdon perusteella arvonlisäverokoodille."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TaxTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 1473eeb2950296f5ae6250d7a53794af3d9cba81
ms.contentlocale: fi-fi
ms.lasthandoff: 08/08/2018

---

# <a name="sales-tax-calculation-methods-in-the-origin-field"></a><span data-ttu-id="e7172-103">Arvonlisäveron laskentatavat Alkuperä-kentässä</span><span class="sxs-lookup"><span data-stu-id="e7172-103">Sales tax calculation methods in the Origin field</span></span>

[!include [banner](../includes/banner.md)]

[!include [retail name](../includes/retail-name.md)]

<span data-ttu-id="e7172-104">Tässä artikkelissa käsitellään arvonlisäveron koodisivun Peruste-kentän vaihtoehtoja sekä sitä, miten arvonlisävero lasketaan valitun vaihtoehdon perusteella arvonlisäverokoodille.</span><span class="sxs-lookup"><span data-stu-id="e7172-104">This article explains the options in the Origin field on the sales tax codes page and how sales tax is calculated based on the selected option for a sales tax code.</span></span>

<span data-ttu-id="e7172-105">Kun luot arvonlisäverokoodeja Arvonlisäverokoodit-sivulla, sinun täytyy valita laskentatapa, jota käytetään Alkuperä-kentässä olevaan veron perustesummaan.</span><span class="sxs-lookup"><span data-stu-id="e7172-105">For each sales tax code that you create in the Sales tax codes page, you must select the method of calculation to apply to the tax base amount in the Origin field.</span></span>

## <a name="percentage-of-net-amount"></a><span data-ttu-id="e7172-106">Prosenttia nettosummasta</span><span class="sxs-lookup"><span data-stu-id="e7172-106">Percentage of net amount</span></span>
<span data-ttu-id="e7172-107">Prosenttia nettosummasta -laskentatapa on Alkuperä-kentässä oletusarvona.</span><span class="sxs-lookup"><span data-stu-id="e7172-107">The Percentage of net amount calculation method is the default value in the Origin field.</span></span> <span data-ttu-id="e7172-108">Arvonlisävero lasketaan osto- tai myyntihinnan prosenttiarvona, kun hintaan ei sisälly muita veroja.</span><span class="sxs-lookup"><span data-stu-id="e7172-108">The sales tax is calculated as a percentage of the purchase or sales amount, excluding any other sales taxes.</span></span>
### <a name="example"></a><span data-ttu-id="e7172-109">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="e7172-109">Example</span></span>

<span data-ttu-id="e7172-110">Veroprosentti on 25 %.</span><span class="sxs-lookup"><span data-stu-id="e7172-110">The tax rate is 25%.</span></span> <span data-ttu-id="e7172-111">Laskurivillä näkyvä nimikemäärä on 10 ja hinta 1,00/nimike, ja asiakkaalle myönnetään 10 %:n rivialennus.</span><span class="sxs-lookup"><span data-stu-id="e7172-111">The invoice line shows a quantity of 10 items at 1.00 each, and the customer is allowed a 10% line discount.</span></span> <span data-ttu-id="e7172-112">Nettosumma: (10 x 1,00) -10 % = 9,00 Arvonlisävero: 9,00 x 25 % = 2,25 Kokonaissumma: 9,00 + 2,25 = 11,25</span><span class="sxs-lookup"><span data-stu-id="e7172-112">Net amount: (10 x 1.00) -10% = 9.00 Sales tax: 9.00 x 25% = 2.25 Total amount: 9.00 + 2.25 = 11.25</span></span>

## <a name="percentage-of-gross-amount"></a><span data-ttu-id="e7172-113"> Prosenttia bruttosummasta</span><span class="sxs-lookup"><span data-stu-id="e7172-113">Percentage of gross amount</span></span>
<span data-ttu-id="e7172-114">Jos valitset Prosenttia bruttosummasta -laskentatavan, arvonlisävero lasketaan bruttomyyntihinnan prosenttiosuutena.</span><span class="sxs-lookup"><span data-stu-id="e7172-114">If you select the Percentage of gross amount method, the sales tax is calculated as a percentage of the gross sales amount.</span></span> <span data-ttu-id="e7172-115">Bruttosumma on rivin nettosumma sekä kaikki rivin verot ja maksut, lukuun ottamatta veroa, jossa Alkuperä = Prosenttia bruttosummasta.</span><span class="sxs-lookup"><span data-stu-id="e7172-115">The gross amount is the line net amount plus all taxes and fees for the line except the one tax with Origin = Percentage of gross amount.</span></span>
### <a name="example"></a><span data-ttu-id="e7172-116">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="e7172-116">Example</span></span>

<span data-ttu-id="e7172-117">Verottaja on säätänyt tätä kohdetta koskevia erikoismaksuja.</span><span class="sxs-lookup"><span data-stu-id="e7172-117">The tax authority has imposed special duties on an item.</span></span> <span data-ttu-id="e7172-118">Erikoismaksusummat lisätään nettosummaan ennen arvonlisäveron laskemista.</span><span class="sxs-lookup"><span data-stu-id="e7172-118">The duty amounts are added to the net amount before sales tax is calculated.</span></span> <span data-ttu-id="e7172-119">Käytetään seuraavia arvonlisäverokoodeja:</span><span class="sxs-lookup"><span data-stu-id="e7172-119">Given the following sales tax codes:</span></span>
-   <span data-ttu-id="e7172-120">MAKSU 1 = 10 %, Prosenttia nettosummasta -laskentatapa</span><span class="sxs-lookup"><span data-stu-id="e7172-120">DUTY 1 = 10%, using the Percentage of net amount calculation method</span></span>
-   <span data-ttu-id="e7172-121">MAKSU 2 = 20 %, Prosenttia nettosummasta -laskentatapa</span><span class="sxs-lookup"><span data-stu-id="e7172-121">DUTY 2 = 20%, using the Percentage of net amount calculation method</span></span>
-   <span data-ttu-id="e7172-122">ALV = 25 %, Prosenttia bruttosummasta -laskentatapa</span><span class="sxs-lookup"><span data-stu-id="e7172-122">SALESTAX = 25%, using the Percentage of gross amount calculation method</span></span>

<span data-ttu-id="e7172-123">Jos nettosumma on 10,00, niin MAKSU 1 on 1,00 (10,00 x 10 %) ja MAKSU 2 = 2,00 (10,00 x 20 %).</span><span class="sxs-lookup"><span data-stu-id="e7172-123">If the net amount is 10.00, then DUTY 1 is 1.00 (10.00 x 10%) and DUTY 2 = 2.00 (10.00 x 20%).</span></span> <span data-ttu-id="e7172-124">Summat ovat seuraavat: Bruttosumma: Nettosumma + MAKSU 1 -summa + MAKSU 2 -summa (10,00 + 1,00 + 2,00) = 13,00 ALV = 13,00 x 25 % = 3,25 MAKSUT ja ALV yhteensä: 1,00 + 2,00 + 3,25 = 6,25 Kokonaissumma: 10,00 + 6,25 = 16,25</span><span class="sxs-lookup"><span data-stu-id="e7172-124">The amounts would be as follows: Gross amount: Net amount + DUTY 1 amount + DUTY 2 amount (10.00 + 1.00 + 2.00) = 13.00 SALESTAX = 13.00 x 25% = 3.25 Total DUTIES and SALESTAX: 1.00 + 2.00 + 3.25 = 6.25 Total amount: 10.00 + 6.25 = 16.25</span></span>

| <span data-ttu-id="e7172-125">**Huomautus**</span><span class="sxs-lookup"><span data-stu-id="e7172-125">**Note**</span></span>                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7172-126">Tapahtumassa voi käyttää vain yhtä verokoodia, jossa Alkuperä = Prosenttia bruttosummasta.</span><span class="sxs-lookup"><span data-stu-id="e7172-126">Only one tax code with Origin = Percentage of gross amount can be used for a transaction.</span></span> <span data-ttu-id="e7172-127">Jos tapahtumalle määritetään useita tällaisia verokoodeja, näyttöön tulee virhesanoma, jonka mukaan arvonlisäveroa ei voi laskea.</span><span class="sxs-lookup"><span data-stu-id="e7172-127">If more than one such tax code is determined for a transaction an error will be displayed that sales tax cannot be calculated.</span></span> |


<a name="percentage-of-sales-tax"></a><span data-ttu-id="e7172-128">Arvonlisäveroprosentti</span><span class="sxs-lookup"><span data-stu-id="e7172-128">Percentage of sales tax</span></span>
-----------------------

<span data-ttu-id="e7172-129">Kun valitset Alkuperä-kentästä Arvonlisäveroprosentti-vaihtoehdon, arvonlisävero lasketaan prosenttina Arvonlisäveron arvonlisävero -kentässä valitusta arvonlisäverosta.</span><span class="sxs-lookup"><span data-stu-id="e7172-129">When you select Percentage of sales tax in the Origin field, sales tax is calculated as a percentage of the sales tax that is selected in the Sales tax on sales tax field.</span></span> <span data-ttu-id="e7172-130">Arvonlisäveron arvonlisävero -kentästä valittu arvonlisävero lasketaan ensin.</span><span class="sxs-lookup"><span data-stu-id="e7172-130">The sales tax that is selected in the Sales tax on sales tax field is calculated first.</span></span> <span data-ttu-id="e7172-131">Toinen arvonlisävero lasketaan sitten ensimmäisen arvonlisäverosumman perusteella.</span><span class="sxs-lookup"><span data-stu-id="e7172-131">The second sales tax is then calculated based on the first sales tax amount.</span></span>
### <a name="example"></a><span data-ttu-id="e7172-132">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="e7172-132">Example</span></span>

<span data-ttu-id="e7172-133">Käytetään seuraavia arvonlisäverokoodeja:</span><span class="sxs-lookup"><span data-stu-id="e7172-133">Given the following sales tax codes:</span></span>
-   <span data-ttu-id="e7172-134">MAKSU 1 = 10 %, Prosenttia nettosummasta -laskentatapa</span><span class="sxs-lookup"><span data-stu-id="e7172-134">DUTY 1 = 10%, using the Percentage of net amount method</span></span>
-   <span data-ttu-id="e7172-135">MAKSU 2 = 20 %, Arvonlisäveroprosentti-laskentatapa ja Maksu 1 Arvonlisäveron arvonlisävero -kentästä</span><span class="sxs-lookup"><span data-stu-id="e7172-135">DUTY 2 = 20%, using the Percentage of sales tax method, with Duty 1 in the Sales tax on sales tax field</span></span>
-   <span data-ttu-id="e7172-136">ALV = 25 %, Prosenttia bruttosummasta -laskentatapa</span><span class="sxs-lookup"><span data-stu-id="e7172-136">SALESTAX = 25%, using the Percentage of gross amount method</span></span>

<span data-ttu-id="e7172-137">Nettosumma: 10,00 MAKSU 1: 10,00 x 10 % = 1,00 MAKSU 2: 1,00 x 20 % = 0,20 Bruttosumma: 10,00 + 1,00 + 0,20 = 11,20 ALV: 11,20 x 25 % = 2,80 MAKSUT ja ALV yhteensä: 1,00 + 0,20 + 2,80 = 4,00 Kokonaissumma: 10,00 + 4,00 = 14,00</span><span class="sxs-lookup"><span data-stu-id="e7172-137">Net amount: 10.00 DUTY 1: 10.00 x 10% = 1.00 DUTY 2: 1.00 x 20% = 0.20 Gross amount: 10.00 + 1.00 + 0.20 = 11.20 SALESTAX: 11.20 x 25% = 2.80 Total DUTIES and SALESTAX: 1.00 + 0.20 + 2.80 = 4.00 Total amount: 10.00 + 4.00 = 14.00</span></span>

| <span data-ttu-id="e7172-138">**Huomautus**</span><span class="sxs-lookup"><span data-stu-id="e7172-138">**Note**</span></span>                                                                                                                                                                                                                    |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7172-139">Verolaskutoimituksissa ei voi käyttää monen tason veroja.</span><span class="sxs-lookup"><span data-stu-id="e7172-139">Multilevel tax on tax calculations are not possible.</span></span> <span data-ttu-id="e7172-140">Veroa ei voi laskea sellaisen veron perusteella, joka on jo laskettu toisen veron perusteella.</span><span class="sxs-lookup"><span data-stu-id="e7172-140">A tax cannot be calculated based on a tax which already is calculated based on another tax.</span></span> <span data-ttu-id="e7172-141">Tapahtumalle voi laskea useita verokoodeihin perustuvia yhden tason veroja.</span><span class="sxs-lookup"><span data-stu-id="e7172-141">Multiple single level tax on tax codes can be calculated on a transaction.</span></span> |

## <a name="amount-per-unit"></a><span data-ttu-id="e7172-142"> Summa per yksikkö</span><span class="sxs-lookup"><span data-stu-id="e7172-142">Amount per unit</span></span>
<span data-ttu-id="e7172-143">Kun Alkuperä-kentästä valitaan Summa per yksikkö, arvonlisävero lasketaan kiinteänä summana yksikköä kohti kerrottuna asiakirjan riville syötetyllä määrällä.</span><span class="sxs-lookup"><span data-stu-id="e7172-143">When you select Amount per unit in the Origin field, sales tax is calculated as a fixed amount per unit multiplied with the quantity entered on the document line.</span></span> <span data-ttu-id="e7172-144">Yksikkö on valittava Yksikkö-kentästä.</span><span class="sxs-lookup"><span data-stu-id="e7172-144">A unit has to be selected in the Unit field.</span></span> <span data-ttu-id="e7172-145">Yksikkökohtainen hinta määritetään Arvonlisäverokoodin arvot -sivulla.</span><span class="sxs-lookup"><span data-stu-id="e7172-145">The amount per unit is specified in the Sales tax code values page.</span></span>
### <a name="example"></a><span data-ttu-id="e7172-146">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="e7172-146">Example</span></span>

<span data-ttu-id="e7172-147">Arvonlisäverokoodiksi on määritetty: 1,20 USD / yksikkö = laatikko Myyntilaskurivillä nimikettä myydään 25 laatikkoa Arvonlisäveroksi lasketaan 25 x 1,20 = 30,00</span><span class="sxs-lookup"><span data-stu-id="e7172-147">Sales tax code is set up as: USD 1.20 per unit = box On a sales invoice line 25 boxes of an item are sold Sales tax is calculated as 25 x 1.20 = 30.00</span></span>

| <span data-ttu-id="e7172-148">**Huomautus**</span><span class="sxs-lookup"><span data-stu-id="e7172-148">**Note**</span></span>                                                                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7172-149">Jos tapahtumalla on eri yksikkö kuin arvonlisäverokoodissa määritetty, se muunnetaan automaattisesti Yksikkömuunnokset-sivulla määritettyjen yksikkömuunnosten perusteella.</span><span class="sxs-lookup"><span data-stu-id="e7172-149">If the transaction is entered in different unit than the unit specified on the sales tax code, it is converted automatically based on the unit conversions that are set up in the Unit conversions page.</span></span> |

###  <a name="amount-per-unit-additional-option"></a><span data-ttu-id="e7172-150"> Summa per yksikkö, lisävaihtoehto</span><span class="sxs-lookup"><span data-stu-id="e7172-150">Amount per unit, additional option</span></span>

<span data-ttu-id="e7172-151">Laskenta-välilehdessä voit valita, lasketaanko yksikkökohtaiseen summaan perustuva vero ennen muita verokoodeja ja lisätäänkö se nettosummaan ennen muita verokoodeja, joille käytetty laskentatapa on Alkuperä = Prosenttia nettosummasta.</span><span class="sxs-lookup"><span data-stu-id="e7172-151">On the Calculation tab, you can select whether an amount per unit calculated tax is calculated before other tax codes and added to the net amount before other tax codes with Origin = Percentage of net amount are calculated.</span></span>

### <a name="examples"></a><span data-ttu-id="e7172-152">Esimerkkejä</span><span class="sxs-lookup"><span data-stu-id="e7172-152">Examples</span></span>

<span data-ttu-id="e7172-153">Oletetaan, että tapahtumalle lasketaan 2 verokoodia:</span><span class="sxs-lookup"><span data-stu-id="e7172-153">Assume we calculate 2 tax codes on a transaction:</span></span>

-   <span data-ttu-id="e7172-154">MAKSU: Alkuperä = Summa per yksikkö ja arvonlisävero, arvoksi määritetään 5,00 per yksikkö = kpl</span><span class="sxs-lookup"><span data-stu-id="e7172-154">DUTY: Origin = Amount per unit and a sales tax, the value is set to 5.00 per unit = pcs</span></span>
-   <span data-ttu-id="e7172-155">ALV: Alkuperä = kuten alla olevissa esimerkeissä, arvoksi määritetään 25 %</span><span class="sxs-lookup"><span data-stu-id="e7172-155">SALESTAX: Origin = as shown in the examples below, the value is set to 25%</span></span>

<span data-ttu-id="e7172-156">Nimikettä myydään 1 kappale yksikköhintaan 10,00</span><span class="sxs-lookup"><span data-stu-id="e7172-156">We sell 1 piece of an item at a unit price of 10.00</span></span>
#### <a name="example-1"></a><span data-ttu-id="e7172-157">Esimerkki 1</span><span class="sxs-lookup"><span data-stu-id="e7172-157">Example 1</span></span>

<span data-ttu-id="e7172-158">ALV: Alkuperä = Prosenttia bruttosummasta -laskutapa Laske ennen arvonlisäveroa -vaihtoehdolla ei ole vaikutusta, koska ALV lasketaan prosenttina bruttosummasta.</span><span class="sxs-lookup"><span data-stu-id="e7172-158">SALESTAX: Origin = Percentage of gross amount method The Calculate before sales tax option has no effect, because SALESTAX is calculated as a percentage of the gross amount.</span></span> <span data-ttu-id="e7172-159">MAKSU: 1 x 5,00 = 5,00 Bruttosumma: 10,00 + 5,00 = 15,00 ALV: 15,00 x 25 % = 3,75 Arvonlisävero yhteensä: 5,00 + 3,75 = 8,75 Kokonaissumma: 10,00 + 8,75 = 18,75</span><span class="sxs-lookup"><span data-stu-id="e7172-159">DUTY: 1 x 5.00 = 5.00 Gross amount: 10.00 + 5.00 = 15.00 SALESTAX: 15.00 x 25% = 3.75 Total sales tax: 5.00 + 3.75 = 8.75 Total amount: 10.00 + 8.75 = 18.75</span></span>

#### <a name="example-2"></a><span data-ttu-id="e7172-160">Esimerkki 2</span><span class="sxs-lookup"><span data-stu-id="e7172-160">Example 2</span></span>

<span data-ttu-id="e7172-161">ALV: Alkuperä = Prosenttia nettosummasta Laske ennen arvonlisäveroa -vaihtoehtoa ei valita MAKSU-laskennalle.</span><span class="sxs-lookup"><span data-stu-id="e7172-161">SALESTAX: Origin = Percentage of net amount The Calculate before sales tax option is not selected for the DUTY calculation.</span></span> <span data-ttu-id="e7172-162">Nettosumma: 10,00 MAKSU: 1 x 5,00 = 5,00 ALV: 10,00 x 25 % = 2,50 Arvonlisävero yhteensä: 5,00 + 2,50 = 7,50 Kokonaissumma: 10,00 + 7,50 = 17,50</span><span class="sxs-lookup"><span data-stu-id="e7172-162">Net amount: 10.00 DUTY: 1 x 5.00 = 5.00 SALESTAX: 10.00 x 25% = 2.50 Total sales tax: 5.00 + 2.50 = 7.50 Total amount: 10.00 + 7.50 = 17.50</span></span>

#### <a name="example-3"></a><span data-ttu-id="e7172-163">Esimerkki 3</span><span class="sxs-lookup"><span data-stu-id="e7172-163">Example 3</span></span>

<span data-ttu-id="e7172-164">ALV: Alkuperä = Prosenttia nettosummasta Laske ennen arvonlisäveroa -vaihtoehto valitaan MAKSU-laskennalle.</span><span class="sxs-lookup"><span data-stu-id="e7172-164">SALESTAX: Origin = Percentage of net amount The Calculate before sales tax option is selected for the DUTY calculation.</span></span> <span data-ttu-id="e7172-165">Nettosumma: 10,00 MAKSU: 1 x 5,00 = 5,00 ALV: (10,00 + 5,00) x 25 % = 3,75 Arvonlisävero yhteensä: 5,00 + 3,75 = 8,75 Kokonaissumma: 10,00 + 8,75 = 18,75</span><span class="sxs-lookup"><span data-stu-id="e7172-165">Net amount: 10.00 DUTY: 1 x 5.00 = 5.00 SALESTAX: (10.00 + 5.00) x 25% = 3.75 Total sales tax: 5.00 + 3.75 = 8.75 Total amount: 10.00 + 8.75 = 18.75</span></span>

#### <a name="example-4"></a><span data-ttu-id="e7172-166">Esimerkki 4</span><span class="sxs-lookup"><span data-stu-id="e7172-166">Example 4</span></span>

<span data-ttu-id="e7172-167">Esimerkkien 3 ja 1 tulos on sama, koska erikoismaksuja on vain yksi.</span><span class="sxs-lookup"><span data-stu-id="e7172-167">The result of Example 3 and Example 1 is the same, because there is only one duty.</span></span> <span data-ttu-id="e7172-168">Oletetaan, että MAKSUJA on kaksi ja vain toinen niistä sisältyy arvonlisäveron laskennan nettosummaan: MAKSU 1: 5,00 käyttämällä Summa peri yksikkö -tapaa ja Laske ennen arvonlisävero -vaihtoehto on valittuna MAKSU 2: 2,50 käyttämällä Summa per yksikkö -tapaa ja Laske ennen arvonlisävero -vaihtoehtoa ei ole valittu Arvonlisävero: 25 % käyttämällä Prosenttia nettosummasta -tapaa Nettosumma: 10,00 MAKSU 1: 1 x 5,00 = 5,00 MAKSU 2: 1 x 2,50 = 2,50 Nettosumma, josta arvonlisäveroa maksetaan: 10,00 + 5,00 = 15,00 ALV: 15,00 x 25 % = 3.75 Arvonlisäverot yhteensä erikoismaksut mukaan lukien: 5,00 + 2,50 + 3,75 = 11,25 Kokonaissumma: 10,00 + 11,25 = 21,25 25 %:n ALV lasketaan nettosumman summalle (10,00) + MAKSU 1 (5,00) = 15,00.</span><span class="sxs-lookup"><span data-stu-id="e7172-168">Assume that you have two DUTIES, and only one of them is included in the net amount for the sales tax calculation: DUTY 1: 5.00, using the Amount per unit method, and the Calculate before sales tax option is selected DUTY 2: 2.50, using the Amount per unit method, and the Calculate before sales tax option is not selected Sales tax: 25%, using the Percentage of net amount method Net amount: 10.00 DUTY 1: 1 x 5.00 = 5.00 DUTY 2: 1 x 2.50 = 2.50 Net amount subject to sales tax: 10.00 + 5.00 = 15.00 SALESTAX: 15.00 x 25% = 3.75 Total sales taxes, including duties: 5.00 + 2.50 + 3.75 = 11.25 Total amount: 10.00 + 11.25 = 21.25 The 25% SALESTAX is calculated for the sum of the net amount (10.00) + DUTY 1 (5.00) = 15.00.</span></span> <span data-ttu-id="e7172-169">MAKSU 2 lisätään verosummaan, kun arvonlisävero on laskettu.</span><span class="sxs-lookup"><span data-stu-id="e7172-169">DUTY 2 is added to the tax amount after the sales tax is calculated.</span></span>

## <a name="calculated-percentage-of-net-amount"></a><span data-ttu-id="e7172-170"> Laskettu nettosummaprosentti</span><span class="sxs-lookup"><span data-stu-id="e7172-170">Calculated percentage of net amount</span></span>
<span data-ttu-id="e7172-171">Laskettu nettosummaprosentti käsittelee verojen laskennan eri tavalla asiakirjan tai kirjauskansion Summat sisältävät arvonlisäveron -parametrin asetuksen mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="e7172-171">The Calculated percentage of net amount handles tax calculation differently depending on the setting of the Amounts include sales tax parameter for the document or journal.</span></span>
### <a name="example-1"></a><span data-ttu-id="e7172-172">Esimerkki 1</span><span class="sxs-lookup"><span data-stu-id="e7172-172">Example 1</span></span>

<span data-ttu-id="e7172-173">Asiakirjan/kirjauskansion asetukseksi on määritetty Summat sisältävät arvonlisäveron = Kyllä Tapahtuman rivisumma: 10,00 Veroprosentti: 25 % Arvonlisävero: Tapahtuman rivisumma x veroprosentti (10,00 x 25 %) = 2,50 Veron perustesumma (alkuperäinen määrä): Tapahtumarivin summa - Arvonlisävero (10,00 - 2,50) = 7,50</span><span class="sxs-lookup"><span data-stu-id="e7172-173">Document / journal is set to Amounts include sales tax = Yes Transaction line amount: 10.00 Tax rate: 25% Sales tax: Transaction line amount x tax rate (10.00 x 25%) = 2.50 Tax base amount (origin amount): Transaction line amount - Sales tax (10.00 - 2.50) = 7.50</span></span>

### <a name="example-2"></a><span data-ttu-id="e7172-174">Esimerkki 2</span><span class="sxs-lookup"><span data-stu-id="e7172-174">Example 2</span></span>

<span data-ttu-id="e7172-175">Asiakirjan/kirjauskansion asetukseksi on määritetty Summat sisältävät arvonlisäveron = Ei Tapahtuman rivisumma: 10,00 Veroprosentti: 25 % Arvonlisävero: (Tapahtuman rivisumma x veroprosentti) / (100 - veroprosentti) (10,00 x 25 %) / (100 % - 25 %) = 3,33 Veron perustesumma (alkuperäinen määrä): Tapahtumarivin summa = 10,00</span><span class="sxs-lookup"><span data-stu-id="e7172-175">Document / journal is set to Amounts include sales tax = No Transaction line amount: 10.00 Tax rate: 25% Sales tax: (Transaction line amount x tax rate) / (100 - tax rate) (10.00 x 25%) / (100% - 25%) = 3.33 Tax base amount (origin amount): Transaction line amount = 10.00</span></span>



<a name="additional-resources"></a><span data-ttu-id="e7172-176">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="e7172-176">Additional resources</span></span>
--------

[<span data-ttu-id="e7172-177">Arvonlisäveroprosenttien määrittäminen Alv-rajan peruste- ja Laskentatapa-kenttien perusteella</span><span class="sxs-lookup"><span data-stu-id="e7172-177">Determining sale tax rates based on the Marginal base and Calculation method fields</span></span>](marginal-base-field.md)

[<span data-ttu-id="e7172-178">Alv-koodien koko summa- ja väli-laskentavaihtoehdot</span><span class="sxs-lookup"><span data-stu-id="e7172-178">Whole amount and Interval calculation options for sales tax codes</span></span>](whole-amount-interval-options-sales-tax-codes.md)




