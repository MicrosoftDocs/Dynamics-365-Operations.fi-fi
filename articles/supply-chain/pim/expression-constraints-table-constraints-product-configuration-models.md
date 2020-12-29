---
title: Lausekerajoitukset ja taulurajoitukset tuotemääritysmalleissa
description: Tässä ohjeaiheessa kuvataan lauseke- ja taulurajoitusten käyttö. Rajoittaa sellaisten määritearvojen hallitsemista, joita käytät tuotteiden määrittämiseen myyntitilaukselle, myyntitarjoukselle, ostotilaukselle tai tuotantotilaukselle. Voit käyttää lausekerajoituksia tai taulurajoituksia, riippuen siitä, kuinka haluat luoda rajoitukset.
author: cvocph
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PCGlobalTableConstraintEdit, PCProductConfigurationModelDetails, PCTableConstraintAttachAttributeTree, PCTableConstraintDefinition
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 53111
ms.assetid: 5c12b1f2-eb89-4648-a755-de412f2eadd6
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: be9d9ae48d21db077928ba7bd5615fea47ea5181
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4427271"
---
# <a name="expression-constraints-and-table-constraints-in-product-configuration-models"></a><span data-ttu-id="239d4-105">Lausekerajoitukset ja taulurajoitukset tuotemääritysmalleissa</span><span class="sxs-lookup"><span data-stu-id="239d4-105">Expression constraints and table constraints in product configuration models</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="239d4-106">Tässä ohjeaiheessa kuvataan lauseke- ja taulurajoitusten käyttö.</span><span class="sxs-lookup"><span data-stu-id="239d4-106">This topic describes the use of expression constraints and table constraints.</span></span> <span data-ttu-id="239d4-107">Rajoittaa sellaisten määritearvojen hallitsemista, joita käytät tuotteiden määrittämiseen myyntitilaukselle, myyntitarjoukselle, ostotilaukselle tai tuotantotilaukselle.</span><span class="sxs-lookup"><span data-stu-id="239d4-107">Constraints control the attribute values that you can select when you configure products for a sales order, sales quotation, purchase order, or production order.</span></span> <span data-ttu-id="239d4-108">Voit käyttää lausekerajoituksia tai taulurajoituksia, riippuen siitä, kuinka haluat luoda rajoitukset.</span><span class="sxs-lookup"><span data-stu-id="239d4-108">You can use expression constraints or table constraints, depending on how you prefer to build the constraints.</span></span> 

<span data-ttu-id="239d4-109">Rajoituksilla hallitaan valittavissa olevia määritearvoja, kun tuotteita määritetään myyntitilaukseen, myyntitarjoukseen, ostotilaukseen tai tuotantotilaukseen.</span><span class="sxs-lookup"><span data-stu-id="239d4-109">Constraints are used to control the attribute values that you can select when you configure products for a sales order, sales quotation, purchase order, or production order.</span></span> <span data-ttu-id="239d4-110">Voit käyttää lausekerajoituksia tai taulurajoituksia, riippuen siitä, kuinka haluat luoda rajoitukset.</span><span class="sxs-lookup"><span data-stu-id="239d4-110">You can use expression constraints or table constraints, depending on how you prefer to build the constraints.</span></span>

## <a name="what-are-expression-constraints"></a><span data-ttu-id="239d4-111">Mitä ovat lausekkeen rajoitukset?</span><span class="sxs-lookup"><span data-stu-id="239d4-111">What are expression constraints?</span></span>
<span data-ttu-id="239d4-112">Lausekerajoituksissa on lauseke, joka käyttää aritmeettisia tai Boolen operaattoreita ja funktioita.</span><span class="sxs-lookup"><span data-stu-id="239d4-112">Expression constraints are characterized by an expression that uses arithmetic and Boolean operators and functions.</span></span> <span data-ttu-id="239d4-113">Lausekerajoitus kirjoitetaan tuotemääritysmallin tietylle komponentille.</span><span class="sxs-lookup"><span data-stu-id="239d4-113">An expression constraint is written for a specific component in a product configuration model.</span></span> <span data-ttu-id="239d4-114">Sitä ei voi käyttää uudelleen tai jakaa toisen komponentin kanssa.</span><span class="sxs-lookup"><span data-stu-id="239d4-114">It can't be reused by or shared with another component.</span></span> <span data-ttu-id="239d4-115">Komponentin lausekerajoitukset voivat kuitenkin viitata komponentin alikomponenttien määritteisiin.</span><span class="sxs-lookup"><span data-stu-id="239d4-115">However, the expression constraints for a component can reference attributes of the component's subcomponents.</span></span>

## <a name="what-are-table-constraints"></a><span data-ttu-id="239d4-116">Mitä ovat taulukon rajoitukset?</span><span class="sxs-lookup"><span data-stu-id="239d4-116">What are table constraints?</span></span>
<span data-ttu-id="239d4-117">Taulurajoitukset kuvaavat sellaisia arvoyhdistelmiä, jotka sallitaan määritteille, kun määrität tuotetta.</span><span class="sxs-lookup"><span data-stu-id="239d4-117">Table constraints list the combinations of values that are allowed for attributes when you configure a product.</span></span> <span data-ttu-id="239d4-118">Taulurajoituksen määrityksiä voidaan käyttää yleisesti.</span><span class="sxs-lookup"><span data-stu-id="239d4-118">Table constraint definitions can be used generically.</span></span> <span data-ttu-id="239d4-119">Luodessasi taulurajoituksen komponentille tuotteen konfiguraatiomallissa, valitset taulukon rajoitusmäärityksen.</span><span class="sxs-lookup"><span data-stu-id="239d4-119">When you create a table constraint for a component in a product configuration model, you select a table constraint definition.</span></span> <span data-ttu-id="239d4-120">Jos haluat luoda sallittuja yhdistelmiä, lisää tietyn tyyppisiä määritteitä komponentteihin.</span><span class="sxs-lookup"><span data-stu-id="239d4-120">To create the combinations that are allowed, you add attributes of specific types to the components.</span></span> <span data-ttu-id="239d4-121">Jokaisella määritteen tyypillä on tietty arvo.</span><span class="sxs-lookup"><span data-stu-id="239d4-121">Each attribute type has a specific value.</span></span>

### <a name="example-of-a-table-constraint"></a><span data-ttu-id="239d4-122">Esimerkki taulurajoituksesta</span><span class="sxs-lookup"><span data-stu-id="239d4-122">Example of a table constraint</span></span>

<span data-ttu-id="239d4-123">Tämä esimerkki osoittaa, miten voit rajoittaa kaiuttimen kokoonpanon tiettyihin viimeistelyihin ja etulevyihin.</span><span class="sxs-lookup"><span data-stu-id="239d4-123">This example shows how you can limit the configuration of a speaker to specific cabinet finishes and fronts.</span></span> <span data-ttu-id="239d4-124">Ensimmäisessä taulukossa ovat ne kaappien viimeistelyt ja etulevyt, jotka kokoonpanolle on yleisesti saatavilla.</span><span class="sxs-lookup"><span data-stu-id="239d4-124">The first table shows the cabinet finishes and fronts that are generally available for configuration.</span></span> <span data-ttu-id="239d4-125">Arvot on määritetty **Kaapin viimeistely**- ja **Etusäleikkö**-määritetyypeille.</span><span class="sxs-lookup"><span data-stu-id="239d4-125">The values are defined for the **Cabinet finish** and **Front grill** attribute types.</span></span>

| <span data-ttu-id="239d4-126">Määritteen tyyppi</span><span class="sxs-lookup"><span data-stu-id="239d4-126">Attribute type</span></span> | <span data-ttu-id="239d4-127">Arvot</span><span class="sxs-lookup"><span data-stu-id="239d4-127">Values</span></span>                      |
|----------------|-----------------------------|
| <span data-ttu-id="239d4-128">Kaapin viimeistely</span><span class="sxs-lookup"><span data-stu-id="239d4-128">Cabinet finish</span></span> | <span data-ttu-id="239d4-129">Musta, tammi, ruusupuu, valkoinen</span><span class="sxs-lookup"><span data-stu-id="239d4-129">Black, Oak, Rosewood, White</span></span> |
| <span data-ttu-id="239d4-130">Etusäleikkö</span><span class="sxs-lookup"><span data-stu-id="239d4-130">Front grill</span></span>    | <span data-ttu-id="239d4-131">Musta, metalli, valkoinen</span><span class="sxs-lookup"><span data-stu-id="239d4-131">Black, Metal, White</span></span>         |

<span data-ttu-id="239d4-132">Seuraavassa taulukossa näkyvät **Väri ja viimeistely** -taulurajoituksen määrittämät yhdistelmät.</span><span class="sxs-lookup"><span data-stu-id="239d4-132">The next table shows the combinations that are defined by the **Color and finish** table constraint.</span></span> <span data-ttu-id="239d4-133">Tämän taulurajoituksen avulla voit määrittää kaiuttimen, jonka viimeistelynä on tammi ja jonka etusäleikkö on musta, jonka viimeistelynä on ruusupuu ja etusäleikkö valkoinen ja niin edelleen.</span><span class="sxs-lookup"><span data-stu-id="239d4-133">By using this table constraint, you can configure a speaker that has an oak finish and a black grill, a Rosewood finish and a white grill, and so on.</span></span>

| <span data-ttu-id="239d4-134">Lopetus</span><span class="sxs-lookup"><span data-stu-id="239d4-134">Finish</span></span>         | <span data-ttu-id="239d4-135">Säleikkö</span><span class="sxs-lookup"><span data-stu-id="239d4-135">Grill</span></span>                       |
|----------------|-----------------------------|
| <span data-ttu-id="239d4-136">Tammi</span><span class="sxs-lookup"><span data-stu-id="239d4-136">Oak</span></span>            | <span data-ttu-id="239d4-137">Musta</span><span class="sxs-lookup"><span data-stu-id="239d4-137">Black</span></span>                       |
| <span data-ttu-id="239d4-138">Ruusupuu</span><span class="sxs-lookup"><span data-stu-id="239d4-138">Rosewood</span></span>       | <span data-ttu-id="239d4-139">Valkoinen</span><span class="sxs-lookup"><span data-stu-id="239d4-139">White</span></span>                       |
| <span data-ttu-id="239d4-140">Valkoinen</span><span class="sxs-lookup"><span data-stu-id="239d4-140">White</span></span>          | <span data-ttu-id="239d4-141">Musta</span><span class="sxs-lookup"><span data-stu-id="239d4-141">Black</span></span>                       |
| <span data-ttu-id="239d4-142">Valkoinen</span><span class="sxs-lookup"><span data-stu-id="239d4-142">White</span></span>          | <span data-ttu-id="239d4-143">Valkoinen</span><span class="sxs-lookup"><span data-stu-id="239d4-143">White</span></span>                       |
| <span data-ttu-id="239d4-144">Musta</span><span class="sxs-lookup"><span data-stu-id="239d4-144">Black</span></span>          | <span data-ttu-id="239d4-145">Musta</span><span class="sxs-lookup"><span data-stu-id="239d4-145">Black</span></span>                       |
| <span data-ttu-id="239d4-146">Musta</span><span class="sxs-lookup"><span data-stu-id="239d4-146">Black</span></span>          | <span data-ttu-id="239d4-147">Metalli</span><span class="sxs-lookup"><span data-stu-id="239d4-147">Metal</span></span>                       | 

<span data-ttu-id="239d4-148">Voit luoda järjestelmän määrittämiä ja käyttäjän määrittämiä taulukkorajoitteita.</span><span class="sxs-lookup"><span data-stu-id="239d4-148">You can create system-defined and user-defined table constraints.</span></span> <span data-ttu-id="239d4-149">Lisätietoja on kohdassa [Järjestelmän ja käyttäjän määrittämät taulurajoitukset](system-defined-user-defined-table-constraints.md).</span><span class="sxs-lookup"><span data-stu-id="239d4-149">For more information, see [System-defined and user-defined table constraints](system-defined-user-defined-table-constraints.md).</span></span>

## <a name="what-syntax-should-be-used-to-write-constraints"></a><span data-ttu-id="239d4-150">Mitä syntaksia pitäisi käyttää rajoitusten kirjoittamiseen?</span><span class="sxs-lookup"><span data-stu-id="239d4-150">What syntax should be used to write constraints?</span></span>
<span data-ttu-id="239d4-151">Käytä rajoituksia kirjoittaessasi Optimization Modeling Language (OML) -syntaksia.</span><span class="sxs-lookup"><span data-stu-id="239d4-151">You must use Optimization Modeling Language (OML) syntax when you write constraints.</span></span> <span data-ttu-id="239d4-152">Järjestelmä käyttää Microsoft Solver Foundation -rajoitusratkaisinta rajoitusten selvittämiseen.</span><span class="sxs-lookup"><span data-stu-id="239d4-152">The system uses Microsoft Solver Foundation constraint solver to solve the constraints.</span></span>

## <a name="should-i-use-table-constraints-or-expression-constraints"></a><span data-ttu-id="239d4-153">Tulisiko minun käyttää taulurajoituksia vai lausekerajoituksia?</span><span class="sxs-lookup"><span data-stu-id="239d4-153">Should I use table constraints or expression constraints?</span></span>
<span data-ttu-id="239d4-154">Voit käyttää joko lausekerajoituksia tai taulurajoituksia sen mukaan, miten haluat luoda rajoitukset.</span><span class="sxs-lookup"><span data-stu-id="239d4-154">You can use either expression constraints or table constraints, depending on how you prefer to build the constraints.</span></span> <span data-ttu-id="239d4-155">Taulurajoitus kootaan matriisiksi, kun taas lausekerajoitus on yksittäinen lauseke.</span><span class="sxs-lookup"><span data-stu-id="239d4-155">You build a table constraint as a matrix, whereas an expression constraint is an individual statement.</span></span> <span data-ttu-id="239d4-156">Määrittäessäsi tuotteen se ei ole merkitystä millaista rajoitetta käytetään.</span><span class="sxs-lookup"><span data-stu-id="239d4-156">When you configure a product, it doesn't matter what kind of constraint is used.</span></span> <span data-ttu-id="239d4-157">Seuraava esimerkki osoittaa näiden menetelmien erot.</span><span class="sxs-lookup"><span data-stu-id="239d4-157">The following example shows how the two methods differ.</span></span>  

<span data-ttu-id="239d4-158">Nämä yhdistelmät ovat sallittuja, kun määrität tuotteen käyttämällä seuraavia rajoitusasetuksia:</span><span class="sxs-lookup"><span data-stu-id="239d4-158">When you configure a product by using the following constraint setups, these combinations are allowed:</span></span>

-   <span data-ttu-id="239d4-159">Tuote, väri Musta, koko 30 tai 50</span><span class="sxs-lookup"><span data-stu-id="239d4-159">A product in the color Black, and in size 30 or 50</span></span>
-   <span data-ttu-id="239d4-160">Tuote, väri Punainen, koko 20</span><span class="sxs-lookup"><span data-stu-id="239d4-160">A product in the color Red and in size 20</span></span>

### <a name="table-constraint-setup"></a><span data-ttu-id="239d4-161">Taulurajoituksen asetukset</span><span class="sxs-lookup"><span data-stu-id="239d4-161">Table constraint setup</span></span>

| <span data-ttu-id="239d4-162">Väri</span><span class="sxs-lookup"><span data-stu-id="239d4-162">Color</span></span> | <span data-ttu-id="239d4-163">Koko</span><span class="sxs-lookup"><span data-stu-id="239d4-163">Size</span></span> |
|-------|------|
| <span data-ttu-id="239d4-164">Musta</span><span class="sxs-lookup"><span data-stu-id="239d4-164">Black</span></span> | <span data-ttu-id="239d4-165">30</span><span class="sxs-lookup"><span data-stu-id="239d4-165">30</span></span>   |
| <span data-ttu-id="239d4-166">Musta</span><span class="sxs-lookup"><span data-stu-id="239d4-166">Black</span></span> | <span data-ttu-id="239d4-167">50</span><span class="sxs-lookup"><span data-stu-id="239d4-167">50</span></span>   |
| <span data-ttu-id="239d4-168">Punainen</span><span class="sxs-lookup"><span data-stu-id="239d4-168">Red</span></span>   | <span data-ttu-id="239d4-169">20</span><span class="sxs-lookup"><span data-stu-id="239d4-169">20</span></span>   |

### <a name="expression-constraint-setup"></a><span data-ttu-id="239d4-170">Lausekerajoituksen asetukset</span><span class="sxs-lookup"><span data-stu-id="239d4-170">Expression constraint setup</span></span>

<span data-ttu-id="239d4-171">(Color == "Black" & (size == "30" | size == "50")) | (color == "Red" & size = "20")</span><span class="sxs-lookup"><span data-stu-id="239d4-171">(Color == "Black" & (size == "30" | size == "50")) | (color == "Red" & size = "20")</span></span>

## <a name="should-i-use-operators-or-infix-notation-when-i-write-expression-constraints"></a><span data-ttu-id="239d4-172">Tulisiko minun käyttää operaattoreita vai infix-merkintää, kun kirjoitan lausekerajoituksia?</span><span class="sxs-lookup"><span data-stu-id="239d4-172">Should I use operators or infix notation when I write expression constraints?</span></span>
<span data-ttu-id="239d4-173">Voit kirjoittaa lausekerajoituksen käyttämällä joko käytettävissä olevia etuliiteoperaattoreita tai infix-merkintää.</span><span class="sxs-lookup"><span data-stu-id="239d4-173">You can write an expression constraint by using either the available prefix operators or infix notation.</span></span> <span data-ttu-id="239d4-174">**Min**-, **Max**- ja **Abs**-operaattorien kanssa ei voi käyttää infix-merkintää.</span><span class="sxs-lookup"><span data-stu-id="239d4-174">For the **Min**, **Max**, and **Abs** operators, you can't use infix notation.</span></span> <span data-ttu-id="239d4-175">Nämä operaattorit sisältyvät vakiona useimpiin ohjelmointikieliin.</span><span class="sxs-lookup"><span data-stu-id="239d4-175">These operators are included as standard operators in most programming languages.</span></span>

## <a name="what-operators-and-infix-notation-can-i-use-when-i-write-expression-constraints"></a><span data-ttu-id="239d4-176">Mitä operaattoreita ja infix-merkintöjä voin käyttää kirjoittaessani lausekerajoituksia?</span><span class="sxs-lookup"><span data-stu-id="239d4-176">What operators and infix notation can I use when I write expression constraints?</span></span>
<span data-ttu-id="239d4-177">Seuraavissa taulukoissa on kuvattu operaattorit ja infix-merkinnät, joita voidaan käyttää, kun tuotemääritysmallin komponentille kirjoitetaan lausekerajoitus.</span><span class="sxs-lookup"><span data-stu-id="239d4-177">The following tables list the operators and infix notation that you can use when you write an expression constraint for a component in a product configuration model.</span></span> <span data-ttu-id="239d4-178">Ensimmäisen taulukon esimerkit osoittavat, miten lauseke kirjoitetaan käyttämällä joko infix-merkintää tai operaattoreita.</span><span class="sxs-lookup"><span data-stu-id="239d4-178">The examples in the first table show how to write an expression by using either infix notation or operators.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="239d4-179">Käyttäjä</span><span class="sxs-lookup"><span data-stu-id="239d4-179">Operator</span></span></th>
<th><span data-ttu-id="239d4-180">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="239d4-180">Description</span></span></th>
<th><span data-ttu-id="239d4-181">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="239d4-181">Syntax</span></span></th>
<th><span data-ttu-id="239d4-182">Esimerkkejä</span><span class="sxs-lookup"><span data-stu-id="239d4-182">Examples</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="239d4-183">Sisältää</span><span class="sxs-lookup"><span data-stu-id="239d4-183">Implies</span></span></td>
<td><span data-ttu-id="239d4-184">Tämä on tosi, jos ensimmäinen ehto on epätosi, toinen ehto on tosi tai molemmat.</span><span class="sxs-lookup"><span data-stu-id="239d4-184">This is true if the first condition is false, the second condition is true, or both.</span></span></td>
<td><span data-ttu-id="239d4-185">Implies[a, b], infix: a -: b</span><span class="sxs-lookup"><span data-stu-id="239d4-185">Implies[a, b], infix: a -: b</span></span></td>
<td><ul>
<li><span data-ttu-id="239d4-186"><strong>Operaattori:</strong> Implies[x != 0, y &gt;= 0]</span><span class="sxs-lookup"><span data-stu-id="239d4-186"><strong>Operator:</strong> Implies[x != 0, y &gt;= 0]</span></span></li>
<li><span data-ttu-id="239d4-187"><strong>Infix-merkintä:</strong> x != 0 -: y &gt;= 0</span><span class="sxs-lookup"><span data-stu-id="239d4-187"><strong>Infix notation:</strong> x != 0 -: y &gt;= 0</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="239d4-188">Ja</span><span class="sxs-lookup"><span data-stu-id="239d4-188">And</span></span></td>
<td><span data-ttu-id="239d4-189">Tämä on tosi vain, jos kaikki ehdot ovat tosia.</span><span class="sxs-lookup"><span data-stu-id="239d4-189">This is true only if all conditions are true.</span></span> <span data-ttu-id="239d4-190">Jos ehtojen määrä on 0 (nolla), tuloksena on <strong>Tosi</strong>.</span><span class="sxs-lookup"><span data-stu-id="239d4-190">If the number of conditions is 0 (zero), it produces <strong>True</strong>.</span></span></td>
<td><span data-ttu-id="239d4-191">And[args], infix: a &amp; b &amp; ... &amp; z</span><span class="sxs-lookup"><span data-stu-id="239d4-191">And[args], infix: a &amp; b &amp; ... &amp; z</span></span></td>
<td><ul>
<li><span data-ttu-id="239d4-192"><strong>Operaattori:</strong> And[x == 2, y &lt;= 2]</span><span class="sxs-lookup"><span data-stu-id="239d4-192"><strong>Operator:</strong> And[x == 2, y &lt;= 2]</span></span></li>
<li><span data-ttu-id="239d4-193"><strong>Infix-merkintä:</strong> x == 2 &amp; y &lt;= 2</span><span class="sxs-lookup"><span data-stu-id="239d4-193"><strong>Infix notation:</strong> x == 2 &amp; y &lt;= 2</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="239d4-194">Tai</span><span class="sxs-lookup"><span data-stu-id="239d4-194">Or</span></span></td>
<td><span data-ttu-id="239d4-195">Näin tapahtuu, jos mikä tahansa ehto on tosi.</span><span class="sxs-lookup"><span data-stu-id="239d4-195">This is true if any condition is true.</span></span> <span data-ttu-id="239d4-196">Jos ehtojen määrä on 0 (nolla), tuloksena on <strong>Epätosi</strong>.</span><span class="sxs-lookup"><span data-stu-id="239d4-196">If the number of conditions is 0 (zero), it produces <strong>False</strong>.</span></span></td>
<td><span data-ttu-id="239d4-197">Or[args], infix: a | b | ... | z</span><span class="sxs-lookup"><span data-stu-id="239d4-197">Or[args], infix: a | b | ... | z</span></span></td>
<td><ul>
<li><span data-ttu-id="239d4-198"><strong>Operaattori:</strong> Or[x == 2, y &lt;= 2]</span><span class="sxs-lookup"><span data-stu-id="239d4-198"><strong>Operator:</strong> Or[x == 2, y &lt;= 2]</span></span></li>
<li><span data-ttu-id="239d4-199"><strong>Infix-merkintä:</strong> x == 2 | y &lt;= 2</span><span class="sxs-lookup"><span data-stu-id="239d4-199"><strong>Infix notation:</strong> x == 2 | y &lt;= 2</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="239d4-200">Plus</span><span class="sxs-lookup"><span data-stu-id="239d4-200">Plus</span></span></td>
<td><span data-ttu-id="239d4-201">Tämä koostaa sen ehdot.</span><span class="sxs-lookup"><span data-stu-id="239d4-201">This sums its conditions.</span></span> <span data-ttu-id="239d4-202">Jos ehtojen määrä on 0 (nolla), tuloksena on <strong>0</strong>.</span><span class="sxs-lookup"><span data-stu-id="239d4-202">If the number of conditions is 0 (zero), it produces <strong>0</strong>.</span></span></td>
<td><span data-ttu-id="239d4-203">Plus[args], infix: a + b + ... + z</span><span class="sxs-lookup"><span data-stu-id="239d4-203">Plus[args], infix: a + b + ... + z</span></span></td>
<td><ul>
<li><span data-ttu-id="239d4-204"><strong>Operaattori:</strong> Plus[x, y, 2] == z</span><span class="sxs-lookup"><span data-stu-id="239d4-204"><strong>Operator:</strong> Plus[x, y, 2] == z</span></span></li>
<li><span data-ttu-id="239d4-205"><strong>Infix-merkintä:</strong> x + y + 2 == z</span><span class="sxs-lookup"><span data-stu-id="239d4-205"><strong>Infix notation:</strong> x + y + 2 == z</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="239d4-206">Miinus</span><span class="sxs-lookup"><span data-stu-id="239d4-206">Minus</span></span></td>
<td><span data-ttu-id="239d4-207">Tämä kääntää sen argumentin.</span><span class="sxs-lookup"><span data-stu-id="239d4-207">This negates its argument.</span></span> <span data-ttu-id="239d4-208">Ehtoja on oltava täsmälleen yksi.</span><span class="sxs-lookup"><span data-stu-id="239d4-208">It must have exactly one condition.</span></span></td>
<td><span data-ttu-id="239d4-209">Minus[expr], infix: -expr</span><span class="sxs-lookup"><span data-stu-id="239d4-209">Minus[expr], infix: -expr</span></span></td>
<td><ul>
<li><span data-ttu-id="239d4-210"><strong>Operaattori:</strong> Minus[x] == y</span><span class="sxs-lookup"><span data-stu-id="239d4-210"><strong>Operator:</strong> Minus[x] == y</span></span></li>
<li><span data-ttu-id="239d4-211"><strong>Infix-merkintä:</strong> -x == y</span><span class="sxs-lookup"><span data-stu-id="239d4-211"><strong>Infix notation:</strong> -x == y</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="239d4-212">Abs</span><span class="sxs-lookup"><span data-stu-id="239d4-212">Abs</span></span></td>
<td><span data-ttu-id="239d4-213">Tämä vaatii ehtoonsa itseisarvon.</span><span class="sxs-lookup"><span data-stu-id="239d4-213">This takes the absolute value of its condition.</span></span> <span data-ttu-id="239d4-214">Ehtoja on oltava täsmälleen yksi.</span><span class="sxs-lookup"><span data-stu-id="239d4-214">It must have exactly one condition.</span></span></td>
<td><span data-ttu-id="239d4-215">Abs[expr]</span><span class="sxs-lookup"><span data-stu-id="239d4-215">Abs[expr]</span></span></td>
<td><span data-ttu-id="239d4-216"><strong>Operaattori:</strong> Abs[x]</span><span class="sxs-lookup"><span data-stu-id="239d4-216"><strong>Operator:</strong> Abs[x]</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="239d4-217">Ajat</span><span class="sxs-lookup"><span data-stu-id="239d4-217">Times</span></span></td>
<td><span data-ttu-id="239d4-218">Tämä vaatii tuotteen ehtoonsa.</span><span class="sxs-lookup"><span data-stu-id="239d4-218">This takes the product of its conditions.</span></span> <span data-ttu-id="239d4-219">Jos ehtojen määrä on 0 (nolla), tuloksena on <strong>1</strong>.</span><span class="sxs-lookup"><span data-stu-id="239d4-219">If the number of conditions is 0 (zero), it produces <strong>1</strong>.</span></span></td>
<td><span data-ttu-id="239d4-220">Times[args], infix: a \* b \* ... \* z</span><span class="sxs-lookup"><span data-stu-id="239d4-220">Times[args], infix: a \* b \* ... \* z</span></span></td>
<td><ul>
<li><span data-ttu-id="239d4-221"><strong>Operaattori:</strong> Times[x, y, 2] == z</span><span class="sxs-lookup"><span data-stu-id="239d4-221"><strong>Operator:</strong> Times[x, y, 2] == z</span></span></li>
<li><span data-ttu-id="239d4-222"><strong>Infix-merkintä:</strong> x \* y \* 2 == z</span><span class="sxs-lookup"><span data-stu-id="239d4-222"><strong>Infix notation:</strong> x \* y \* 2 == z</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="239d4-223">Teho</span><span class="sxs-lookup"><span data-stu-id="239d4-223">Power</span></span></td>
<td><span data-ttu-id="239d4-224">Tämä vaatii eksponentiaalin.</span><span class="sxs-lookup"><span data-stu-id="239d4-224">This takes an exponential.</span></span> <span data-ttu-id="239d4-225">Tämä koskee potenssiinkorotusta oikealta vasemmalle.</span><span class="sxs-lookup"><span data-stu-id="239d4-225">It applies exponentiation from right to left.</span></span> <span data-ttu-id="239d4-226">(Toisin sanoen se on oikeus-assosiatiivinen.) Tämän vuoksi <strong>Power[a, b, c]</strong> on sama kuin <strong>Power[a, Power[b, c]]</strong>.</span><span class="sxs-lookup"><span data-stu-id="239d4-226">(In other words, it&#39;s right-associative.) Therefore, <strong>Power[a, b, c]</strong> is equivalent to <strong>Power[a, Power[b, c]]</strong>.</span></span> <span data-ttu-id="239d4-227"><strong>Power</strong>-operaattoria voidaan käyttää vain, jos eksponentti on positiivinen vakio.</span><span class="sxs-lookup"><span data-stu-id="239d4-227"><strong>Power</strong> can be used only if the exponent is a positive constant.</span></span></td>
<td><span data-ttu-id="239d4-228">Power[args], infix: a ^ b ^ ... ^ z</span><span class="sxs-lookup"><span data-stu-id="239d4-228">Power[args], infix: a ^ b ^ ... ^ z</span></span></td>
<td><ul>
<li><span data-ttu-id="239d4-229"><strong>Operaattori:</strong> Power[x, 2] == y</span><span class="sxs-lookup"><span data-stu-id="239d4-229"><strong>Operator:</strong> Power[x, 2] == y</span></span></li>
<li><span data-ttu-id="239d4-230"><strong>Infix-merkintä:</strong> x ^ 2 == y</span><span class="sxs-lookup"><span data-stu-id="239d4-230"><strong>Infix notation:</strong> x ^ 2 == y</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="239d4-231">Enintään</span><span class="sxs-lookup"><span data-stu-id="239d4-231">Max</span></span></td>
<td><span data-ttu-id="239d4-232">Tämä tuottaa suurimman ehdon.</span><span class="sxs-lookup"><span data-stu-id="239d4-232">This produces the largest condition.</span></span> <span data-ttu-id="239d4-233">Jos ehtojen määrä on 0 (nolla), tuloksena on <strong>Ääretön</strong>.</span><span class="sxs-lookup"><span data-stu-id="239d4-233">If the number of conditions is 0 (zero), it produces <strong>Infinity</strong>.</span></span></td>
<td><span data-ttu-id="239d4-234">Max[args]</span><span class="sxs-lookup"><span data-stu-id="239d4-234">Max[args]</span></span></td>
<td><span data-ttu-id="239d4-235"><strong>Operaattori:</strong> Max[x, y, 2] == z</span><span class="sxs-lookup"><span data-stu-id="239d4-235"><strong>Operator:</strong> Max[x, y, 2] == z</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="239d4-236">Min</span><span class="sxs-lookup"><span data-stu-id="239d4-236">Min</span></span></td>
<td><span data-ttu-id="239d4-237">Tämä tuottaa pienimmän ehdon.</span><span class="sxs-lookup"><span data-stu-id="239d4-237">This produces the smallest condition.</span></span> <span data-ttu-id="239d4-238">Jos ehtojen määrä on 0 (nolla), tuloksena on <strong>Ääretön</strong>.</span><span class="sxs-lookup"><span data-stu-id="239d4-238">If the number of conditions is 0 (zero), it produces <strong>Infinity</strong>.</span></span></td>
<td><span data-ttu-id="239d4-239">Min[args]</span><span class="sxs-lookup"><span data-stu-id="239d4-239">Min[args]</span></span></td>
<td><span data-ttu-id="239d4-240"><strong>Operaattori:</strong> Min[x, y, 2] == z</span><span class="sxs-lookup"><span data-stu-id="239d4-240"><strong>Operator:</strong> Min[x, y, 2] == z</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="239d4-241">Ei</span><span class="sxs-lookup"><span data-stu-id="239d4-241">Not</span></span></td>
<td><span data-ttu-id="239d4-242">Tämä tuottaa loogisen käänteisen version ehdostansa.</span><span class="sxs-lookup"><span data-stu-id="239d4-242">This produces the logical inverse of its condition.</span></span> <span data-ttu-id="239d4-243">Ehtoja on oltava täsmälleen yksi.</span><span class="sxs-lookup"><span data-stu-id="239d4-243">It must have exactly one condition.</span></span></td>
<td><span data-ttu-id="239d4-244">Not[expr], infix: !expr</span><span class="sxs-lookup"><span data-stu-id="239d4-244">Not[expr], infix: !expr</span></span></td>
<td><ul>
<li><span data-ttu-id="239d4-245"><strong>Operaattori:</strong> Not[x] &amp; Not[y == 3]</span><span class="sxs-lookup"><span data-stu-id="239d4-245"><strong>Operator:</strong> Not[x] &amp; Not[y == 3]</span></span></li>
<li><span data-ttu-id="239d4-246"><strong>Infix-merkintä:</strong> !x!(y == 3)</span><span class="sxs-lookup"><span data-stu-id="239d4-246"><strong>Infix notation:</strong> !x!(y == 3)</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

<span data-ttu-id="239d4-247">Seuraavan taulukon esimerkit kuvaavat, kuinka infix-merkintä kirjoitetaan.</span><span class="sxs-lookup"><span data-stu-id="239d4-247">The examples in the next table show how to write infix notation.</span></span>


|  <span data-ttu-id="239d4-248">Operandien välinen merkintä</span><span class="sxs-lookup"><span data-stu-id="239d4-248">Infix notation</span></span>   |                                          <span data-ttu-id="239d4-249">kuvaus</span><span class="sxs-lookup"><span data-stu-id="239d4-249">Description</span></span>                                          |
|-------------------|-----------------------------------------------------------------------------------------------|
|     <span data-ttu-id="239d4-250">x + y + z</span><span class="sxs-lookup"><span data-stu-id="239d4-250">x + y + z</span></span>     |                                           <span data-ttu-id="239d4-251">Lisäys</span><span class="sxs-lookup"><span data-stu-id="239d4-251">Addition</span></span>                                            |
|    <span data-ttu-id="239d4-252">x \* y \* z</span><span class="sxs-lookup"><span data-stu-id="239d4-252">x \* y \* z</span></span>    |                                        <span data-ttu-id="239d4-253">Kertolasku</span><span class="sxs-lookup"><span data-stu-id="239d4-253">Multiplication</span></span>                                         |
|       <span data-ttu-id="239d4-254">x - y</span><span class="sxs-lookup"><span data-stu-id="239d4-254">x - y</span></span>       | <span data-ttu-id="239d4-255">Binäärimuotoinen vähennys tehdään samalla tavalla kuin binäärimuotoinen lisäys käänteisen toisen kanssa.</span><span class="sxs-lookup"><span data-stu-id="239d4-255">Binary subtraction is translated the same as binary addition where there is a negated second.</span></span> |
|     <span data-ttu-id="239d4-256">x ^ y ^ z</span><span class="sxs-lookup"><span data-stu-id="239d4-256">x ^ y ^ z</span></span>     |                          <span data-ttu-id="239d4-257">Potenssiinkorotus, jolla on oikea-assosiatiivisuus</span><span class="sxs-lookup"><span data-stu-id="239d4-257">Exponentiation that has right associativity</span></span>                          |
|        <span data-ttu-id="239d4-258">!x</span><span class="sxs-lookup"><span data-stu-id="239d4-258">!x</span></span>         |                                          <span data-ttu-id="239d4-259">Totuusarvo ei</span><span class="sxs-lookup"><span data-stu-id="239d4-259">Boolean not</span></span>                                          |
|      <span data-ttu-id="239d4-260">x -: y</span><span class="sxs-lookup"><span data-stu-id="239d4-260">x -: y</span></span>       |                                      <span data-ttu-id="239d4-261">Looginen vaikutus</span><span class="sxs-lookup"><span data-stu-id="239d4-261">Boolean implication</span></span>                                      |
|         <span data-ttu-id="239d4-262">x</span><span class="sxs-lookup"><span data-stu-id="239d4-262">x</span></span>         |                                               <span data-ttu-id="239d4-263">y</span><span class="sxs-lookup"><span data-stu-id="239d4-263">y</span></span>                                               |
|     <span data-ttu-id="239d4-264">x & y & z</span><span class="sxs-lookup"><span data-stu-id="239d4-264">x & y & z</span></span>     |                                          <span data-ttu-id="239d4-265">Totuusarvo ja</span><span class="sxs-lookup"><span data-stu-id="239d4-265">Boolean and</span></span>                                          |
|    <span data-ttu-id="239d4-266">x == y == z</span><span class="sxs-lookup"><span data-stu-id="239d4-266">x == y == z</span></span>    |                                           <span data-ttu-id="239d4-267">Yhtäsuuruus</span><span class="sxs-lookup"><span data-stu-id="239d4-267">Equality</span></span>                                            |
|    <span data-ttu-id="239d4-268">x != y != z</span><span class="sxs-lookup"><span data-stu-id="239d4-268">x != y != z</span></span>    |                                           <span data-ttu-id="239d4-269">Erilliset</span><span class="sxs-lookup"><span data-stu-id="239d4-269">Distinct</span></span>                                            |
|  <span data-ttu-id="239d4-270">x &lt; y &lt; z</span><span class="sxs-lookup"><span data-stu-id="239d4-270">x &lt; y &lt; z</span></span>  |                                           <span data-ttu-id="239d4-271">Pienempi kuin</span><span class="sxs-lookup"><span data-stu-id="239d4-271">Less than</span></span>                                           |
|  <span data-ttu-id="239d4-272">x &gt; y &gt; z</span><span class="sxs-lookup"><span data-stu-id="239d4-272">x &gt; y &gt; z</span></span>  |                                         <span data-ttu-id="239d4-273">Suurempi kuin</span><span class="sxs-lookup"><span data-stu-id="239d4-273">Greater than</span></span>                                          |
| <span data-ttu-id="239d4-274">x &lt;= y &lt;= z</span><span class="sxs-lookup"><span data-stu-id="239d4-274">x &lt;= y &lt;= z</span></span> |                                     <span data-ttu-id="239d4-275">Pienempi tai yhtä suuri</span><span class="sxs-lookup"><span data-stu-id="239d4-275">Less than or equal to</span></span>                                     |
| <span data-ttu-id="239d4-276">x &gt;= y &gt;= z</span><span class="sxs-lookup"><span data-stu-id="239d4-276">x &gt;= y &gt;= z</span></span> |                                   <span data-ttu-id="239d4-277">Suurempi tai yhtä suuri</span><span class="sxs-lookup"><span data-stu-id="239d4-277">Greater than or equal to</span></span>                                    |
|        <span data-ttu-id="239d4-278">(x)</span><span class="sxs-lookup"><span data-stu-id="239d4-278">(x)</span></span>        |                           <span data-ttu-id="239d4-279">Sulkeet ohittavat oletusarvoisen tärkeysjärjestyksen.</span><span class="sxs-lookup"><span data-stu-id="239d4-279">Parentheses override default precedence.</span></span>                            |

## <a name="why-arent-my-expression-constraints-validated-correctly"></a><span data-ttu-id="239d4-280">Miksi lausekerajoitusteni vahvistaminen ei onnistu?</span><span class="sxs-lookup"><span data-stu-id="239d4-280">Why aren't my expression constraints validated correctly?</span></span>
<span data-ttu-id="239d4-281">Et voi käyttää varattuja avainsanoja ratkaisimen niminä määritteille, komponenteille tai alikomponenteille tuotemääritysmallissa.</span><span class="sxs-lookup"><span data-stu-id="239d4-281">You can't use reserved keywords as solver names for attributes, components, or subcomponents in a product configuration model.</span></span><span data-ttu-id="239d4-282"> Seuraavassa luettelossa on varatut sanat, jotka eivät ole käytettävissä:</span><span class="sxs-lookup"><span data-stu-id="239d4-282"> Here is a list of the reserved keywords that you can't use:</span></span>

-   <span data-ttu-id="239d4-283">Katto</span><span class="sxs-lookup"><span data-stu-id="239d4-283">Ceiling</span></span>
-   <span data-ttu-id="239d4-284">Elementti</span><span class="sxs-lookup"><span data-stu-id="239d4-284">Element</span></span>
-   <span data-ttu-id="239d4-285">Yhtäläinen</span><span class="sxs-lookup"><span data-stu-id="239d4-285">Equal</span></span>
-   <span data-ttu-id="239d4-286">Kerros</span><span class="sxs-lookup"><span data-stu-id="239d4-286">Floor</span></span>
-   <span data-ttu-id="239d4-287">Jos</span><span class="sxs-lookup"><span data-stu-id="239d4-287">If</span></span>
-   <span data-ttu-id="239d4-288">Pienempi</span><span class="sxs-lookup"><span data-stu-id="239d4-288">Less</span></span>
-   <span data-ttu-id="239d4-289">Suurempi</span><span class="sxs-lookup"><span data-stu-id="239d4-289">Greater</span></span>
-   <span data-ttu-id="239d4-290">Sisältää</span><span class="sxs-lookup"><span data-stu-id="239d4-290">Implies</span></span>
-   <span data-ttu-id="239d4-291">Loki</span><span class="sxs-lookup"><span data-stu-id="239d4-291">Log</span></span>
-   <span data-ttu-id="239d4-292">Enintään</span><span class="sxs-lookup"><span data-stu-id="239d4-292">Max</span></span>
-   <span data-ttu-id="239d4-293">Min</span><span class="sxs-lookup"><span data-stu-id="239d4-293">Min</span></span>
-   <span data-ttu-id="239d4-294">Miinus</span><span class="sxs-lookup"><span data-stu-id="239d4-294">Minus</span></span>
-   <span data-ttu-id="239d4-295">Plus</span><span class="sxs-lookup"><span data-stu-id="239d4-295">Plus</span></span>
-   <span data-ttu-id="239d4-296">Teho</span><span class="sxs-lookup"><span data-stu-id="239d4-296">Power</span></span>
-   <span data-ttu-id="239d4-297">Ajat</span><span class="sxs-lookup"><span data-stu-id="239d4-297">Times</span></span>
-   <span data-ttu-id="239d4-298">Aika</span><span class="sxs-lookup"><span data-stu-id="239d4-298">Slot</span></span>
-   <span data-ttu-id="239d4-299">Malli</span><span class="sxs-lookup"><span data-stu-id="239d4-299">Model</span></span>
-   <span data-ttu-id="239d4-300">Päätöksenteko</span><span class="sxs-lookup"><span data-stu-id="239d4-300">Decision</span></span>
-   <span data-ttu-id="239d4-301">Tavoite</span><span class="sxs-lookup"><span data-stu-id="239d4-301">Goal</span></span>


<a name="additional-resources"></a><span data-ttu-id="239d4-302">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="239d4-302">Additional resources</span></span>
--------

[<span data-ttu-id="239d4-303">Luo lausekerajoitus</span><span class="sxs-lookup"><span data-stu-id="239d4-303">Create an expression constraint</span></span>](tasks/add-expression-constraint-product-configuration-model.md)

[<span data-ttu-id="239d4-304">Lisää laskelma tuotemääritysmalliin</span><span class="sxs-lookup"><span data-stu-id="239d4-304">Add a calculation to a product configuration model</span></span>](tasks/add-calculation-product-configuration-model.md)



