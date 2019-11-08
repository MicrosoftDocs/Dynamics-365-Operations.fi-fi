---
title: Laadunhallinnan yleiskuvaus
description: Tässä ohjeaiheessa kerrotaan, miten Dynamics 365 Supply Chain Managementin laadunhallinnan avulla voidaan parantaa toimitusketjun tuotteiden laatua.
author: perlynne
manager: AnnBe
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTestAssociationTable, InventTestGroup, InventTestItemQualityGroup, InventTestTable, InventTestVariable, InventTestVariableOutcome
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ba38f9c43fed81768155a27dda88a4bfb4a7828e
ms.sourcegitcommit: 0099fb24f5f40ff442020b488ef4171836c35c48
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/23/2019
ms.locfileid: "2653553"
---
# <a name="quality-management-overview"></a><span data-ttu-id="72e00-103">Laadunhallinnan yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="72e00-103">Quality management overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="72e00-104">Tässä ohjeaiheessa kerrotaan, miten Dynamics 365 Supply Chain Managementin laadunhallinnan avulla voidaan parantaa toimitusketjun tuotteiden laatua.</span><span class="sxs-lookup"><span data-stu-id="72e00-104">This topic describes how you can use quality management in Dynamics 365 Supply Chain Management to help improve product quality within your supply chain.</span></span>

<span data-ttu-id="72e00-105">Laadunhallinnan avulla voit hallita määrityksestä poikkeavien tuotteiden käsittelyaikaa niiden lähtöpisteestä riippumatta.</span><span class="sxs-lookup"><span data-stu-id="72e00-105">Quality management can help you manage turnaround times when you handle nonconforming products, regardless of their point of origin.</span></span> <span data-ttu-id="72e00-106">Koska vianmääritystyypit linkitetään korjausraportointiin, Supply Chain Management voi ajoittaa ongelmien korjaustehtävät ja estää ongelmien toistuminen.</span><span class="sxs-lookup"><span data-stu-id="72e00-106">Because diagnostic types are linked to correction reporting, Supply Chain Management can schedule tasks to correct problems and prevent them from recurring.</span></span>

<span data-ttu-id="72e00-107">Määrityksistä poikkeamisen hallintatoiminnon lisäksi laadunhallinta sisältää toiminnon ongelmien seuraamiseen ongelmantyypin perusteella (myös sisäiset ongelmat) sekä lyhyt- tai pitkäaikaisen ratkaisun tunnistamiseen.</span><span class="sxs-lookup"><span data-stu-id="72e00-107">In addition to functionality for managing nonconformance, quality management includes functionality for tracking issues by problem type (even internal problems), and for identifying solutions as short-term or long-term.</span></span> <span data-ttu-id="72e00-108">Suorituskykyilmaisimia (KPI) koskevat tilastot antavat tietoja aiemmista määrityksistä poikkeamiseen liittyvistä ongelmista ja niiden korjaamiseen käytetyistä ratkaisuista.</span><span class="sxs-lookup"><span data-stu-id="72e00-108">Statistics about key performance indicators (KPIs) provide insight into the history of previous nonconformance issues and the solutions that were used to correct them.</span></span> <span data-ttu-id="72e00-109">Voit tarkistaa historiallisten tietojen avulla, kuinka tehokkaita aiemmat laatutoimet ovat olleet, ja määrittää, mitkä toimet soveltuvat jatkossa käytettäviksi.</span><span class="sxs-lookup"><span data-stu-id="72e00-109">You can use historical data to review the effectiveness of previous quality measures and determine appropriate measures to use in the future.</span></span>

<span data-ttu-id="72e00-110">Kun määrität laatuliitoksen, Supply Chain Management voi luoda liiketoiminnan eri prosesseille, tapahtumille ja ehdoille laatutilauksia.</span><span class="sxs-lookup"><span data-stu-id="72e00-110">When you set up a quality association, Supply Chain Management can generate quality orders for various business processes, events, and conditions.</span></span> <span data-ttu-id="72e00-111">Laatuliitos voi koskea tiettyä nimikettä, tiettyä nimikeryhmää tai kaikkia nimikkeitä.</span><span class="sxs-lookup"><span data-stu-id="72e00-111">The quality association can cover a specific item, a specific group of items, or all items.</span></span>

## <a name="examples-of-the-use-of-quality-management"></a><span data-ttu-id="72e00-112">Esimerkkejä laadunhallinnan käytöstä</span><span class="sxs-lookup"><span data-stu-id="72e00-112">Examples of the use of quality management</span></span>
<span data-ttu-id="72e00-113">Laadunhallinta on joustavaa ja se voidaan toteuttaa eri tavoin vastaamaan toimitusketjun työvaiheiden tiettyjen tasojen vaatimuksia.</span><span class="sxs-lookup"><span data-stu-id="72e00-113">Quality management is flexible and can be implemented in various ways to meet the requirements of specific levels of supply chain operations.</span></span> <span data-ttu-id="72e00-114">Seuraavassa esimerkissä käsitellään näiden ominaisuuksien mahdollisia käyttötapoja:</span><span class="sxs-lookup"><span data-stu-id="72e00-114">The following examples illustrate possible uses of these features:</span></span>

-   <span data-ttu-id="72e00-115">Laadunvalvontaprosessin käynnistäminen automaattisesti ennaltamääritettyjen ehtojen perusteella (kun tietyn toimittajan ostotilaus rekisteröidään varastossa).</span><span class="sxs-lookup"><span data-stu-id="72e00-115">Automatically start a quality control process, based on predefined criteria (upon warehouse registration of a purchase order from a specific vendor).</span></span>
-   <span data-ttu-id="72e00-116">Varaston esto tarkastuksen aikana, jotta varastoa, jota ei ole hyväksytty, ei käytetä (ostotilausmäärien täysi esto).</span><span class="sxs-lookup"><span data-stu-id="72e00-116">Block inventory during inspection to prevent non-approved inventory from being used (full blocking of purchase order quantities).</span></span>
-   <span data-ttu-id="72e00-117">Nimikeotannan käyttö laatuliitoksen osana määritettäessä tarkastettavan fyysisen varaston tämän hetkistä määrää.</span><span class="sxs-lookup"><span data-stu-id="72e00-117">Use item sampling as part of a quality association to define the amount of current physical inventory that must be inspected.</span></span> <span data-ttu-id="72e00-118">Otanta voi perustua kiinteisiin määriin tai prosenttiosuuteen.</span><span class="sxs-lookup"><span data-stu-id="72e00-118">Sampling can be based on fixed quantities or a percentage.</span></span>
-   <span data-ttu-id="72e00-119">Luo laatutilaukset osittaisille vastaanotoille.</span><span class="sxs-lookup"><span data-stu-id="72e00-119">Create quality orders for partial receipts.</span></span> <span data-ttu-id="72e00-120">Tilauksen mukana fyysisesti vastaanotettuun määrään perustuva laatutilaus luodaan valitsemalla **Päivitettyä määrää kohden** -valintaruutu **Nimikeotanta**-lomakkeessa.</span><span class="sxs-lookup"><span data-stu-id="72e00-120">To create a quality order that is based on the quantity that is physically received with an order, you must select the **Per updated quantity** check box on the **Item sampling** form.</span></span>
-   <span data-ttu-id="72e00-121">Testin pienimmän, suurimman ja tavoiteltavan arvon sisältävien testityyppien luominen sekä sellaisen määrää ja laatua vertailevan testin suorittaminen, jolla on ennalta määritetyt tarkistustulokset.</span><span class="sxs-lookup"><span data-stu-id="72e00-121">Create test types that include minimum, maximum, and target test values, and perform qualitative-versus-quantitative testing that has predefined validation results.</span></span>
-   <span data-ttu-id="72e00-122">Hyväksyttävän laadun tason määrittäminen laadun mittaustoleranssien hallintaa varten.</span><span class="sxs-lookup"><span data-stu-id="72e00-122">Specify an acceptable quality level (AQL) to control quality measure tolerances.</span></span>
-   <span data-ttu-id="72e00-123">Tarkastustyövaiheiden edellyttämien resurssien, kuten testausalueen tai testin mittavälineiden, määrittäminen.</span><span class="sxs-lookup"><span data-stu-id="72e00-123">Specify the resources that an inspection operation requires, such as a test area and test instruments.</span></span>

## <a name="working-with-quality-associations"></a><span data-ttu-id="72e00-124">Laatuliitosten käsitteleminen</span><span class="sxs-lookup"><span data-stu-id="72e00-124">Working with quality associations</span></span>
<span data-ttu-id="72e00-125">Laatuliitosta käyttävä liiketoimintoprosessi voidaan liittää eri lähdeasiakirjoihin, kuten ostotilauksiin, myyntitilauksiin tai tuotantotilauksiin.</span><span class="sxs-lookup"><span data-stu-id="72e00-125">The business process that uses a quality association can be related to various source documents, such as purchase orders, sales orders, or production orders.</span></span>

<span data-ttu-id="72e00-126">Jokaisessa laatuliitostietueessa määritetään joukko testejä, hyväksyttävän laadun taso ja otantasuunnitelma, jota käytetään muodostettavissa laatutilauksissa.</span><span class="sxs-lookup"><span data-stu-id="72e00-126">Each quality association record defines the set of tests, the AQL, and the sampling plan that applies to the quality orders that are generated.</span></span> <span data-ttu-id="72e00-127">Laatuliitostietue on määritettävä liiketoimintaprosessin jokaiselle muunnokselle.</span><span class="sxs-lookup"><span data-stu-id="72e00-127">You must define a quality association record for each variation in a business process.</span></span> <span data-ttu-id="72e00-128">Voit esimerkiksi määrittää laatuliitoksen, joka muodostaa laatutilauksen, kun ostotilauksen tuotteen vastaanotto päivitetään.</span><span class="sxs-lookup"><span data-stu-id="72e00-128">For example, you can set up a quality association that generates a quality order when a purchase order product receipt is updated.</span></span> <span data-ttu-id="72e00-129">Toimeenpanosuunnitelma määritysten mukaisesti käynnistävä prosessi voidaan estää, jos laatutilaus on avoinna. Myös seuraavat prosessit, kuten ostotilauksen laskutus, voidaan estää.</span><span class="sxs-lookup"><span data-stu-id="72e00-129">Depending on the setup of the execution plan, the triggering process itself can be blocked while there is an open quality order, or the next processes, such as purchase order invoicing, can be blocked.</span></span>

<span data-ttu-id="72e00-130">**Huomautus:** Jos laatutilauksia on avoinna, varastomäärien otto estetään automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="72e00-130">**Note:** While there are open quality orders, inventory quantities are automatically blocked from being issued.</span></span> <span data-ttu-id="72e00-131">**Nimikeotanta**-sivun **Täysi esto** -asetuksen mukaan laatu on joko laatutilauksen määrä tai lähdeasiakirjan rivin määrä.</span><span class="sxs-lookup"><span data-stu-id="72e00-131">Depending on the **Full blocking** setting on the **Item samplings** page, the quantity is either the quantity on the quality order or the quantity on the source document line.</span></span>

<span data-ttu-id="72e00-132">Tietyn liiketoimintaprosessin laatuliitostietue tunnistaa tapahtuman ja ehdot, joille laatutilaus muodostetaan.</span><span class="sxs-lookup"><span data-stu-id="72e00-132">For a given business process, the quality association record identifies the event and the conditions that a quality order is generated for.</span></span> <span data-ttu-id="72e00-133">Ehdot voivat olla joko toimipaikka- tai yrityskohtaisia.</span><span class="sxs-lookup"><span data-stu-id="72e00-133">The conditions can be specific to either a site or a legal entity.</span></span> <span data-ttu-id="72e00-134">Tuhoavia testejä sisältävä laatutilaus voidaan muodostaa vain, kun tapahtumalla on käytettävissä oleva varasto.</span><span class="sxs-lookup"><span data-stu-id="72e00-134">A quality order that involves destructive tests can be generated only when on-hand inventory exists for the event.</span></span>

<span data-ttu-id="72e00-135">Seuraavassa esimerkeissä käsitellään, miten laatuliitostietue määritetään kunkin liiketoimintaprosessin variaatioille.</span><span class="sxs-lookup"><span data-stu-id="72e00-135">The following examples illustrate how a quality association record is defined for the variations in each business process.</span></span> <span data-ttu-id="72e00-136">Seuraavassa taulussa on jokaisen esimerkin yhteenveto laatuliitostietueessa määritetyistä tapahtumista ja ehdoista.</span><span class="sxs-lookup"><span data-stu-id="72e00-136">For each example, the following table summarizes the events and conditions that are defined by a quality association record.</span></span>

<table>
<tbody>
<tr>
<th><span data-ttu-id="72e00-137">Viitetyyppi</span><span class="sxs-lookup"><span data-stu-id="72e00-137">Reference type</span></span></th>
<th><span data-ttu-id="72e00-138">Tapahtumatyyppi</span><span class="sxs-lookup"><span data-stu-id="72e00-138">Event type</span></span></th>
<th><span data-ttu-id="72e00-139">Suoritus</span><span class="sxs-lookup"><span data-stu-id="72e00-139">Execution</span></span></th>
<th><span data-ttu-id="72e00-140">Tapahtuman esto</span><span class="sxs-lookup"><span data-stu-id="72e00-140">Event blocking</span></span></th>
<th><span data-ttu-id="72e00-141">Tiedostoviite</span><span class="sxs-lookup"><span data-stu-id="72e00-141">Document reference</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="72e00-142">Varasto</span><span class="sxs-lookup"><span data-stu-id="72e00-142">Inventory</span></span></td>
<td><span data-ttu-id="72e00-143">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="72e00-143">Not applicable</span></span></td>
<td><span data-ttu-id="72e00-144">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="72e00-144">Not applicable</span></span></td>
<td><span data-ttu-id="72e00-145">Ei mitään</span><span class="sxs-lookup"><span data-stu-id="72e00-145">None</span></span></td>
<td><span data-ttu-id="72e00-146">Kaikki</span><span class="sxs-lookup"><span data-stu-id="72e00-146">All</span></span></td>
</tr>
<tr>
<td rowspan="7"><span data-ttu-id="72e00-147">Myynti</span><span class="sxs-lookup"><span data-stu-id="72e00-147">Sales</span></span></td>
<td rowspan="4"><span data-ttu-id="72e00-148">Keräysprosessi on ajoitettu</span><span class="sxs-lookup"><span data-stu-id="72e00-148">Picking process is scheduled</span></span></td>
<td rowspan="4"><span data-ttu-id="72e00-149">Ennen</span><span class="sxs-lookup"><span data-stu-id="72e00-149">Before</span></span></td>
<td><span data-ttu-id="72e00-150">Ei mitään</span><span class="sxs-lookup"><span data-stu-id="72e00-150">None</span></span></td>
<td rowspan="22"><span data-ttu-id="72e00-151">Tietty tunnus, ryhmä tai vain kaikki</span><span class="sxs-lookup"><span data-stu-id="72e00-151">Specific ID, Group, or All only</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="72e00-152">Keräysprosessi</span><span class="sxs-lookup"><span data-stu-id="72e00-152">Picking process</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="72e00-153">Pakkausluettelo</span><span class="sxs-lookup"><span data-stu-id="72e00-153">Packing slip</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="72e00-154">Lasku</span><span class="sxs-lookup"><span data-stu-id="72e00-154">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="72e00-155">Pakkausluettelo</span><span class="sxs-lookup"><span data-stu-id="72e00-155">Packing slip</span></span></td>
<td rowspan="3"><span data-ttu-id="72e00-156">Ennen</span><span class="sxs-lookup"><span data-stu-id="72e00-156">Before</span></span></td>
<td><span data-ttu-id="72e00-157">Ei mitään</span><span class="sxs-lookup"><span data-stu-id="72e00-157">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="72e00-158">Pakkausluettelo</span><span class="sxs-lookup"><span data-stu-id="72e00-158">Packing slip</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="72e00-159">Lasku</span><span class="sxs-lookup"><span data-stu-id="72e00-159">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="15"><span data-ttu-id="72e00-160">Osto</span><span class="sxs-lookup"><span data-stu-id="72e00-160">Purchase</span></span></td>
<td rowspan="7"><span data-ttu-id="72e00-161">Vastaanottoluettelo</span><span class="sxs-lookup"><span data-stu-id="72e00-161">Receipt list</span></span></td>
<td rowspan="4"><span data-ttu-id="72e00-162">Ennen</span><span class="sxs-lookup"><span data-stu-id="72e00-162">Before</span></span></td>
<td><span data-ttu-id="72e00-163">Ei mitään</span><span class="sxs-lookup"><span data-stu-id="72e00-163">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="72e00-164">Vastaanottoluettelo</span><span class="sxs-lookup"><span data-stu-id="72e00-164">Receipt list</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="72e00-165">Tuotteen vastaanotto</span><span class="sxs-lookup"><span data-stu-id="72e00-165">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="72e00-166">Lasku</span><span class="sxs-lookup"><span data-stu-id="72e00-166">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="72e00-167">Jälkeen</span><span class="sxs-lookup"><span data-stu-id="72e00-167">After</span></span></td>
<td><span data-ttu-id="72e00-168">Ei mitään</span><span class="sxs-lookup"><span data-stu-id="72e00-168">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="72e00-169">Tuotteen vastaanotto</span><span class="sxs-lookup"><span data-stu-id="72e00-169">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="72e00-170">Lasku</span><span class="sxs-lookup"><span data-stu-id="72e00-170">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="72e00-171">Rekisteröinti</span><span class="sxs-lookup"><span data-stu-id="72e00-171">Registration</span></span></td>
<td rowspan="3"><span data-ttu-id="72e00-172">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="72e00-172">Not applicable</span></span></td>
<td><span data-ttu-id="72e00-173">Ei mitään</span><span class="sxs-lookup"><span data-stu-id="72e00-173">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="72e00-174">Tuotteen vastaanotto</span><span class="sxs-lookup"><span data-stu-id="72e00-174">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="72e00-175">Lasku</span><span class="sxs-lookup"><span data-stu-id="72e00-175">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="72e00-176">Tuotteen vastaanotto</span><span class="sxs-lookup"><span data-stu-id="72e00-176">Product receipt</span></span></td>
<td rowspan="3"><span data-ttu-id="72e00-177">Ennen</span><span class="sxs-lookup"><span data-stu-id="72e00-177">Before</span></span></td>
<td><span data-ttu-id="72e00-178">Ei mitään</span><span class="sxs-lookup"><span data-stu-id="72e00-178">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="72e00-179">Tuotteen vastaanotto</span><span class="sxs-lookup"><span data-stu-id="72e00-179">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="72e00-180">Lasku</span><span class="sxs-lookup"><span data-stu-id="72e00-180">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="72e00-181">Jälkeen</span><span class="sxs-lookup"><span data-stu-id="72e00-181">After</span></span></td>
<td><span data-ttu-id="72e00-182">Ei mitään</span><span class="sxs-lookup"><span data-stu-id="72e00-182">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="72e00-183">Lasku</span><span class="sxs-lookup"><span data-stu-id="72e00-183">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="8"><span data-ttu-id="72e00-184">Tuotanto</span><span class="sxs-lookup"><span data-stu-id="72e00-184">Production</span></span></td>
<td rowspan="3"><span data-ttu-id="72e00-185">Rekisteröinti</span><span class="sxs-lookup"><span data-stu-id="72e00-185">Registration</span></span></td>
<td rowspan="3"><span data-ttu-id="72e00-186">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="72e00-186">Not applicable</span></span></td>
<td><span data-ttu-id="72e00-187">Ei mitään</span><span class="sxs-lookup"><span data-stu-id="72e00-187">None</span></span></td>
<td rowspan="12"><span data-ttu-id="72e00-188">Kaikki</span><span class="sxs-lookup"><span data-stu-id="72e00-188">All</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="72e00-189">Ilmoita valmiiksi</span><span class="sxs-lookup"><span data-stu-id="72e00-189">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="72e00-190">Lopeta</span><span class="sxs-lookup"><span data-stu-id="72e00-190">End</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="72e00-191">Ilmoita valmiiksi</span><span class="sxs-lookup"><span data-stu-id="72e00-191">Report as finished</span></span></td>
<td rowspan="3"><span data-ttu-id="72e00-192">Ennen</span><span class="sxs-lookup"><span data-stu-id="72e00-192">Before</span></span></td>
<td><span data-ttu-id="72e00-193">Ei mitään</span><span class="sxs-lookup"><span data-stu-id="72e00-193">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="72e00-194">Ilmoita valmiiksi</span><span class="sxs-lookup"><span data-stu-id="72e00-194">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="72e00-195">Lopeta</span><span class="sxs-lookup"><span data-stu-id="72e00-195">End</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="72e00-196">Jälkeen</span><span class="sxs-lookup"><span data-stu-id="72e00-196">After</span></span></td>
<td><span data-ttu-id="72e00-197">Ei mitään</span><span class="sxs-lookup"><span data-stu-id="72e00-197">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="72e00-198">Lopeta</span><span class="sxs-lookup"><span data-stu-id="72e00-198">End</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="72e00-199">Karanteeni</span><span class="sxs-lookup"><span data-stu-id="72e00-199">Quarantine</span></span></td>
<td rowspan="3"><span data-ttu-id="72e00-200">Ilmoita valmiiksi</span><span class="sxs-lookup"><span data-stu-id="72e00-200">Report as finished</span></span></td>
<td rowspan="2"><span data-ttu-id="72e00-201">Ennen</span><span class="sxs-lookup"><span data-stu-id="72e00-201">Before</span></span></td>
<td><span data-ttu-id="72e00-202">Ilmoita valmiiksi</span><span class="sxs-lookup"><span data-stu-id="72e00-202">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="72e00-203">Lopeta</span><span class="sxs-lookup"><span data-stu-id="72e00-203">End</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="72e00-204">Jälkeen</span><span class="sxs-lookup"><span data-stu-id="72e00-204">After</span></span></td>
<td><span data-ttu-id="72e00-205">Lopeta</span><span class="sxs-lookup"><span data-stu-id="72e00-205">End</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="72e00-206">Lopeta</span><span class="sxs-lookup"><span data-stu-id="72e00-206">End</span></span></td>
<td><span data-ttu-id="72e00-207">Ennen</span><span class="sxs-lookup"><span data-stu-id="72e00-207">Before</span></span></td>
<td><span data-ttu-id="72e00-208">Lopeta</span><span class="sxs-lookup"><span data-stu-id="72e00-208">End</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="72e00-209">Reitityksen työvaihe</span><span class="sxs-lookup"><span data-stu-id="72e00-209">Route operation</span></span></td>
<td rowspan="3"><span data-ttu-id="72e00-210">Ilmoita valmiiksi</span><span class="sxs-lookup"><span data-stu-id="72e00-210">Report as finished</span></span></td>
<td rowspan="2"><span data-ttu-id="72e00-211">Ennen</span><span class="sxs-lookup"><span data-stu-id="72e00-211">Before</span></span></td>
<td><span data-ttu-id="72e00-212">Ei mitään</span><span class="sxs-lookup"><span data-stu-id="72e00-212">None</span></span></td>
<td rowspan="3"><span data-ttu-id="72e00-213">Tietty tunnus, ryhmä tai kaikki tai ryhmäkohtainen, ryhmä tai kaikki</span><span class="sxs-lookup"><span data-stu-id="72e00-213">Specific ID, Group, or All, and Resource specific, Group, or All</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="72e00-214">Ilmoita valmiiksi</span><span class="sxs-lookup"><span data-stu-id="72e00-214">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="72e00-215">Jälkeen</span><span class="sxs-lookup"><span data-stu-id="72e00-215">After</span></span></td>
<td><span data-ttu-id="72e00-216">Ei mitään</span><span class="sxs-lookup"><span data-stu-id="72e00-216">None</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="72e00-217">Oheistuotteen tuotanto</span><span class="sxs-lookup"><span data-stu-id="72e00-217">Co-product production</span></span></td>
<td><span data-ttu-id="72e00-218">Rekisteröinti</span><span class="sxs-lookup"><span data-stu-id="72e00-218">Registration</span></span></td>
<td><span data-ttu-id="72e00-219">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="72e00-219">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="72e00-220">Ei mitään</span><span class="sxs-lookup"><span data-stu-id="72e00-220">None</span></span></td>
<td rowspan="3"><span data-ttu-id="72e00-221">Kaikki</span><span class="sxs-lookup"><span data-stu-id="72e00-221">All</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="72e00-222">Ilmoita valmiiksi</span><span class="sxs-lookup"><span data-stu-id="72e00-222">Report as finished</span></span></td>
<td><span data-ttu-id="72e00-223">Ennen</span><span class="sxs-lookup"><span data-stu-id="72e00-223">Before</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="72e00-224">Jälkeen</span><span class="sxs-lookup"><span data-stu-id="72e00-224">After</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="72e00-225">Seuraavassa taulussa on lisätietoja laatutilausten muodostamisesta tietyntyyppisille prosesseille.</span><span class="sxs-lookup"><span data-stu-id="72e00-225">The following table provides more information about how quality orders can be generated for specific types of processes.</span></span>
<div class="tableSection">

<table>
<tbody>
<tr>
<th><span data-ttu-id="72e00-226">Prosessin tyyppi</span><span class="sxs-lookup"><span data-stu-id="72e00-226">Type of process</span></span></th>
<th><span data-ttu-id="72e00-227">Laatutilausten automaattinen luontiajankohta</span><span class="sxs-lookup"><span data-stu-id="72e00-227">When quality orders can be automatically generated</span></span></th>
<th><span data-ttu-id="72e00-228">Laatutilausten luontiajankohta, jos tuhoava testaus pakollinen</span><span class="sxs-lookup"><span data-stu-id="72e00-228">When quality orders can be generated if destructive testing is required</span></span></th>
<th><span data-ttu-id="72e00-229">Ehdon tiedot</span><span class="sxs-lookup"><span data-stu-id="72e00-229">Condition information</span></span></th>
<th><span data-ttu-id="72e00-230">Manuaalisen luonnin tiedot</span><span class="sxs-lookup"><span data-stu-id="72e00-230">Manual generation information</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="72e00-231">Ostotilaus</span><span class="sxs-lookup"><span data-stu-id="72e00-231">Purchase order</span></span></td>
<td><span data-ttu-id="72e00-232">Ennen kuin vastaanotetun materiaalin vastaanottoluettelo tai tuotteen vastaanotto on kirjattu tai sen jälkeen</span><span class="sxs-lookup"><span data-stu-id="72e00-232">Before or after a receipts list or product receipt for the material that is received is posted</span></span></td>
<td><span data-ttu-id="72e00-233">Vastaanotetun materiaalin tuotteen vastaanoton kirjauksen jälkeen, koska materiaalin on oltava käytettävissä tuhoavaa testausta varten</span><span class="sxs-lookup"><span data-stu-id="72e00-233">After the product receipt for the material that is received is posted, because the material must be available for destructive testing</span></span></td>
<td><span data-ttu-id="72e00-234">Laatutilausvaatimus voi liittyä toimipaikkaan, nimikkeeseen tai toimittajaan tai näiden ehtojen yhdistelmään.</span><span class="sxs-lookup"><span data-stu-id="72e00-234">The requirement for a quality order can reflect a particular site, item, or vendor, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="72e00-235">Manuaalisesti luotu ostotilaukseen viittaava laatutilaus voi käyttää laatuliitostietueen tietoja, kuten testin otantasuunnitelmaa.</span><span class="sxs-lookup"><span data-stu-id="72e00-235">A manually generated quality order that refers to a purchase order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="72e00-236">Karanteenitilaus</span><span class="sxs-lookup"><span data-stu-id="72e00-236">Quarantine order</span></span></td>
<td><span data-ttu-id="72e00-237">Ennen karanteenitilauksen ilmoittamista valmiiksi tai päättyneeksi tai sen jälkeen</span><span class="sxs-lookup"><span data-stu-id="72e00-237">Before or after the quarantine order is reported as finished or ended</span></span></td>
<td><span data-ttu-id="72e00-238">Tuhoavia testejä edellyttäviä laatutilauksia ei voi luoda.</span><span class="sxs-lookup"><span data-stu-id="72e00-238">Quality orders that require destructive tests can&#39;t be generated.</span></span> <span data-ttu-id="72e00-239">Karanteenitilaustoiminnon oletetaan käsittelevän tuhottavan materiaalin käsittelyn.</span><span class="sxs-lookup"><span data-stu-id="72e00-239">It&#39;s assumed that the quarantine order functionality handles the disposition of the material that is destroyed.</span></span></td>
<td><span data-ttu-id="72e00-240">Laatutilausvaatimus voi liittyä toimipaikkaan, nimikkeeseen tai toimittajaan tai näiden ehtojen yhdistelmään.</span><span class="sxs-lookup"><span data-stu-id="72e00-240">The requirement for a quality order can reflect a particular site, item, or vendor, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="72e00-241">Manuaalisesti luotu ostotilaukseen viittaava karanteenitilaus voi käyttää laatuliitostietueen tietoja, kuten testin otantasuunnitelmaa.</span><span class="sxs-lookup"><span data-stu-id="72e00-241">A manually generated quality order that refers to a quarantine order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="72e00-242">Myyntitilaus</span><span class="sxs-lookup"><span data-stu-id="72e00-242">Sales order</span></span></td>
<td><span data-ttu-id="72e00-243">Ennen lähettävien nimikkeiden ajoitettua keräysprosessia tai pakkausluettelon päivitystä</span><span class="sxs-lookup"><span data-stu-id="72e00-243">Before a scheduled picking process or packing slip update for the items that are being shipped</span></span></td>
<td><span data-ttu-id="72e00-244">Kaikissa vaiheissa</span><span class="sxs-lookup"><span data-stu-id="72e00-244">At any step</span></span></td>
<td><span data-ttu-id="72e00-245">Laatutilausvaatimus voi liittyä toimipaikkaan, nimikkeeseen tai asiakkaaseen tai näiden ehtojen yhdistelmään.</span><span class="sxs-lookup"><span data-stu-id="72e00-245">The requirement for a quality order can reflect a particular site, item, or customer, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="72e00-246">Manuaalisesti luotu myyntitilaukseen viittaava laatutilaus voi käyttää laatuliitostietueen tietoja, kuten testin otantasuunnitelmaa.</span><span class="sxs-lookup"><span data-stu-id="72e00-246">A manually generated quality order that refers to a sales order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="72e00-247">Tuotantotilaus</span><span class="sxs-lookup"><span data-stu-id="72e00-247">Production order</span></span></td>
<td><span data-ttu-id="72e00-248">Ennen tuotantotilauksen valmiiksi raportointia tai sen jälkeen</span><span class="sxs-lookup"><span data-stu-id="72e00-248">Before or after the finished quantity for the production order is reported</span></span></td>
<td><span data-ttu-id="72e00-249">Tuotantotilauksen valmiiksi raportoinnin jälkeen</span><span class="sxs-lookup"><span data-stu-id="72e00-249">After the finished quantity for the production order is reported</span></span></td>
<td><span data-ttu-id="72e00-250">Laatutilausvaatimus voi liittyä toimipaikkaan tai nimikkeeseen tai näiden ehtojen yhdistelmään.</span><span class="sxs-lookup"><span data-stu-id="72e00-250">The requirement for a quality order can reflect a particular site or item, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="72e00-251">Manuaalisesti luotu tuotantotilaukseen viittaava laatutilaus voi käyttää laatuliitostietueen tietoja, kuten testin otantasuunnitelmaa.</span><span class="sxs-lookup"><span data-stu-id="72e00-251">A manually generated quality order that refers to a production order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="72e00-252">Tuotantotilaus, jossa on reitityksen työvaihe</span><span class="sxs-lookup"><span data-stu-id="72e00-252">Production order that has a route operation</span></span></td>
<td><span data-ttu-id="72e00-253">Ennen työvaiheen raportin valmistumista tai sen jälkeen</span><span class="sxs-lookup"><span data-stu-id="72e00-253">Before or after the report is finished for an operation</span></span></td>
<td><span data-ttu-id="72e00-254">Viimeisen työvaiheen tuotannon valmiiksi raportoinnin jälkeen</span><span class="sxs-lookup"><span data-stu-id="72e00-254">After the reporting production is finished for the last operation</span></span></td>
<td><span data-ttu-id="72e00-255">Laatutilausvaatimus voi liittyä toimipaikkaan, nimikkeeseen tai operatiiviseen resurssiin tai näiden ehtojen yhdistelmään.</span><span class="sxs-lookup"><span data-stu-id="72e00-255">The requirement for a quality order can reflect a particular, site, item, or operations resource, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="72e00-256">Manuaalisesti luotu reitityksen työvaiheeseen viittaava laatutilaus voi käyttää laatuliitostietueen tietoja, kuten testin otantasuunnitelmaa.</span><span class="sxs-lookup"><span data-stu-id="72e00-256">A manually generated quality order that refers to a route operation can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="72e00-257">Varasto</span><span class="sxs-lookup"><span data-stu-id="72e00-257">Inventory</span></span></td>
<td><span data-ttu-id="72e00-258">Laatutilausta ei voi luoda automaattisesti varastokirjauskansion tapahtumalle eikä siirtotilaustapahtumille.</span><span class="sxs-lookup"><span data-stu-id="72e00-258">A quality order cannot be automatically generated for a transaction in an inventory journal or for transfer order transactions.</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="72e00-259">Laatutilaus on luotava manuaalisesti nimikkeen varastomäärälle.</span><span class="sxs-lookup"><span data-stu-id="72e00-259">A quality order must be created manually for an item&#39;s inventory quantity.</span></span> <span data-ttu-id="72e00-260">Fyysistä käytettävissä olevaa varastoa edellytetään.</span><span class="sxs-lookup"><span data-stu-id="72e00-260">Physical on-hand inventory is required.</span></span></td>
</tr>
</tbody>
</table>

## <a name="quality-order-auto-generation-examples"></a><span data-ttu-id="72e00-261">Laatutilauksen automaattisen luonnin esimerkkejä</span><span class="sxs-lookup"><span data-stu-id="72e00-261">Quality order auto-generation examples</span></span>

### <a name="purchasing"></a><span data-ttu-id="72e00-262">Osto</span><span class="sxs-lookup"><span data-stu-id="72e00-262">Purchasing</span></span>

<span data-ttu-id="72e00-263">Jos asetat ostoissa **Tapahtumatyyppi**-kentän arvoksi **Tuotteen vastaanotto** ja **Suoritus**-kentän arvoksi **Jälkeen** **Laatuliitokset**-sivulla, saat seuraavat tulokset:</span><span class="sxs-lookup"><span data-stu-id="72e00-263">In purchasing, if you set the **Event type** field to **Product receipt** and the **Execution** field to **After** on the **Quality associations** page, you get the following results:</span></span> 

- <span data-ttu-id="72e00-264">Jos **Päivitettyä määrää kohden** -asetuksen arvoksi määritetään **Kyllä**, laatutilaus luodaan jokaista vastaanottoa varten ostotilauksen perusteella, jolloin otetaan huomioon vastaanotettu määrä sekä nimikeotannan asetukset.</span><span class="sxs-lookup"><span data-stu-id="72e00-264">If the **Per updated quantity** option is set to **Yes**, a quality order is generated for every receipt against the purchase order, based on the received quantity and settings in the item sampling.</span></span> <span data-ttu-id="72e00-265">Joka kerta, kun määrä vastaanotetaan ostotilauksen perusteella, luodaaan uusia laatutilauksia juuri saadun määrän perusteella.</span><span class="sxs-lookup"><span data-stu-id="72e00-265">Every time that a quantity is received against the purchase order, new quality orders are generated based on the newly received quantity.</span></span>
- <span data-ttu-id="72e00-266">Jos **Päivitettyä määrää kohden** -asetuksen arvoksi määritetään **Ei**, laatutilaus luodaan ensimmäistä vastaanottoa varten ostotilauksen perusteella, jolloin otetaan huomioon vastaanotettu määrä.</span><span class="sxs-lookup"><span data-stu-id="72e00-266">If the **Per updated quantity** option is set to **No**, a quality order is generated for the first receipt against the purchase order, based on the received quantity.</span></span> <span data-ttu-id="72e00-267">Lisäksi jäljelle jäävän määrän perusteella luodaan seurantadimensioiden mukaan vähintään yksi laatutilaus.</span><span class="sxs-lookup"><span data-stu-id="72e00-267">Additionally, one or more quality orders are created based on the remaining quantity, depending on the tracking dimensions.</span></span> <span data-ttu-id="72e00-268">Laatutilauksia ei luoda ostotilauksen perusteella seuraavien vastaanottojen osalta.</span><span class="sxs-lookup"><span data-stu-id="72e00-268">Quality orders aren't generated for subsequent receipts against the purchase order.</span></span>

<table>
<tbody>
<tr>
<th><span data-ttu-id="72e00-269">Laatumääritys</span><span class="sxs-lookup"><span data-stu-id="72e00-269">Quality specification</span></span></th>
<th><span data-ttu-id="72e00-270">Päivitettyä määrää kohden</span><span class="sxs-lookup"><span data-stu-id="72e00-270">Per updated quantity</span></span></th>
<th><span data-ttu-id="72e00-271">Seurantadimension mukaan</span><span class="sxs-lookup"><span data-stu-id="72e00-271">Per tracking dimension</span></span></th>
<th><span data-ttu-id="72e00-272">Tulos</span><span class="sxs-lookup"><span data-stu-id="72e00-272">Result</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="72e00-273">Prosenttiosuus: 10 %</span><span class="sxs-lookup"><span data-stu-id="72e00-273">Percentage: 10%</span></span></td>
<td><span data-ttu-id="72e00-274">Kyllä</span><span class="sxs-lookup"><span data-stu-id="72e00-274">Yes</span></span></td>
<td>
<p><span data-ttu-id="72e00-275">Eränumero: Ei</span><span class="sxs-lookup"><span data-stu-id="72e00-275">Batch number: No</span></span></p>
<p><span data-ttu-id="72e00-276">Sarjanumero: Ei</span><span class="sxs-lookup"><span data-stu-id="72e00-276">Serial number: No</span></span></p>
</td>
<td>
<p><span data-ttu-id="72e00-277">Tilausmäärä: 100</span><span class="sxs-lookup"><span data-stu-id="72e00-277">Order quantity: 100</span></span></p>
<ol>
<li><span data-ttu-id="72e00-278">Ilmoita valmiiksi 30:n osalta</span><span class="sxs-lookup"><span data-stu-id="72e00-278">Report as finished for 30</span></span>
<ul>
<li><span data-ttu-id="72e00-279">Laatutilaus #1 määrälle 3 (10 prosenttia 30:stä)</span><span class="sxs-lookup"><span data-stu-id="72e00-279">Quality order #1 for 3 (10% of 30)</span></span></li>
</ul>
</li>
<li><span data-ttu-id="72e00-280">Ilmoita valmiiksi 70:n osalta</span><span class="sxs-lookup"><span data-stu-id="72e00-280">Report as finished for 70</span></span>
<ul>
<li><span data-ttu-id="72e00-281">Laatutilaus #2 määrälle 7 (10 % jäljellä olevasta tilausmäärästä eli 70:stä)</span><span class="sxs-lookup"><span data-stu-id="72e00-281">Quality order #2 for 7 (10% of the remaining order quantity, which equals 70 in this case)</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="72e00-282">Kiinteä määrä: 1</span><span class="sxs-lookup"><span data-stu-id="72e00-282">Fixed quantity: 1</span></span></td>
<td><span data-ttu-id="72e00-283">Ei</span><span class="sxs-lookup"><span data-stu-id="72e00-283">No</span></span></td>
<td>
<p><span data-ttu-id="72e00-284">Eränumero: Ei</span><span class="sxs-lookup"><span data-stu-id="72e00-284">Batch number: No</span></span></p>
<p><span data-ttu-id="72e00-285">Sarjanumero: Ei</span><span class="sxs-lookup"><span data-stu-id="72e00-285">Serial number: No</span></span></p>
</td>
<td><span data-ttu-id="72e00-286">Tilausmäärä: 100</span><span class="sxs-lookup"><span data-stu-id="72e00-286">Order quantity: 100</span></span>
<ol>
<li><span data-ttu-id="72e00-287">Ilmoita valmiiksi 30:n osalta</span><span class="sxs-lookup"><span data-stu-id="72e00-287">Report as finished for 30</span></span>
<ul>
<li><span data-ttu-id="72e00-288">Laatutilaus #1 luodaan määrälle 1 (ensimmäiselle valmiiksi ilmoitetulle määrälle, jolla on kiinteä arvo 1).</span><span class="sxs-lookup"><span data-stu-id="72e00-288">Quality order #1 is created for 1 (for the first reported-as-finished quantity, which has a fixed value of 1).</span></span></li>
<li><span data-ttu-id="72e00-289">Jäljelle jäävää määrää varten ei luoda enempää laatutilauksia.</span><span class="sxs-lookup"><span data-stu-id="72e00-289">No more quality orders are created against the remaining quantity.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="72e00-290">Ilmoita valmiiksi 10:n osalta</span><span class="sxs-lookup"><span data-stu-id="72e00-290">Report as finished for 10</span></span>
<ul>
<li><span data-ttu-id="72e00-291">Laatutilauksia ei luota.</span><span class="sxs-lookup"><span data-stu-id="72e00-291">No quality orders are created.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="72e00-292">Ilmoita valmiiksi 60:n osalta</span><span class="sxs-lookup"><span data-stu-id="72e00-292">Report as finished for 60</span></span>
<ul>
<li><span data-ttu-id="72e00-293">Laatutilauksia ei luota.</span><span class="sxs-lookup"><span data-stu-id="72e00-293">No quality orders are created.</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="72e00-294">Kiinteä määrä: 1</span><span class="sxs-lookup"><span data-stu-id="72e00-294">Fixed quantity: 1</span></span></td>
<td><span data-ttu-id="72e00-295">Kyllä</span><span class="sxs-lookup"><span data-stu-id="72e00-295">Yes</span></span></td>
<td>
<p><span data-ttu-id="72e00-296">Eränumero: Kyllä</span><span class="sxs-lookup"><span data-stu-id="72e00-296">Batch number: Yes</span></span></p>
<p><span data-ttu-id="72e00-297">Sarjanumero: Kyllä</span><span class="sxs-lookup"><span data-stu-id="72e00-297">Serial number: Yes</span></span></p>
</td>
<td>
<p><span data-ttu-id="72e00-298">Tilausmäärä: 10</span><span class="sxs-lookup"><span data-stu-id="72e00-298">Order quantity: 10</span></span></p>
<ol>
<li><span data-ttu-id="72e00-299">Ilmoita valmiiksi 3:n osalta</span><span class="sxs-lookup"><span data-stu-id="72e00-299">Report as finished for 3</span></span>
<ul>
<li><span data-ttu-id="72e00-300">Laatutilaus #1 määrälle 1 erästä #b1, sarjanumero #s1</span><span class="sxs-lookup"><span data-stu-id="72e00-300">Quality order #1 for 1 of batch #b1, serial #s1</span></span></li>
<li><span data-ttu-id="72e00-301">Laatutilaus #2 määrälle 1 erästä #b2, sarjanumero #s2</span><span class="sxs-lookup"><span data-stu-id="72e00-301">Quality order #2 for 1 of batch #b2, serial #s2</span></span></li>
<li><span data-ttu-id="72e00-302">Laatutilaus #3 määrälle 1 erästä #b3, sarjanumero #s3</span><span class="sxs-lookup"><span data-stu-id="72e00-302">Quality order #3 for 1 of batch #b3, serial #s3</span></span></li>
</ul>
</li>
<li><span data-ttu-id="72e00-303">Ilmoita valmiiksi 2:n osalta</span><span class="sxs-lookup"><span data-stu-id="72e00-303">Report as finished for 2</span></span>
<ul>
<li><span data-ttu-id="72e00-304">Laatutilaus #4 määrälle 1 erästä #b4, sarjanumero #s4</span><span class="sxs-lookup"><span data-stu-id="72e00-304">Quality order #4 for 1 of batch #b4, serial #s4</span></span></li>
<li><span data-ttu-id="72e00-305">Laatutilaus #5 määrälle 1 erästä #b5, sarjanumero #s5</span><span class="sxs-lookup"><span data-stu-id="72e00-305">Quality order #5 for 1 of batch #b5, serial #s5</span></span></li>
</ul>
</li>
</ol>
<p><span data-ttu-id="72e00-306"><strong>Huomautus:</strong> Erää voidaan käyttää uudelleen.</span><span class="sxs-lookup"><span data-stu-id="72e00-306"><strong>Note:</strong> The batch can be reused.</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="72e00-307">Kiinteä määrä: 2</span><span class="sxs-lookup"><span data-stu-id="72e00-307">Fixed quantity: 2</span></span></td>
<td><span data-ttu-id="72e00-308">Ei</span><span class="sxs-lookup"><span data-stu-id="72e00-308">No</span></span></td>
<td>
<p><span data-ttu-id="72e00-309">Eränumero: Kyllä</span><span class="sxs-lookup"><span data-stu-id="72e00-309">Batch number: Yes</span></span></p>
<p><span data-ttu-id="72e00-310">Sarjanumero: Kyllä</span><span class="sxs-lookup"><span data-stu-id="72e00-310">Serial number: Yes</span></span></p>
</td>
<td>
<p><span data-ttu-id="72e00-311">Tilausmäärä: 10</span><span class="sxs-lookup"><span data-stu-id="72e00-311">Order quantity: 10</span></span></p>
<ol>
<li><span data-ttu-id="72e00-312">Ilmoita valmiiksi 4:n osalta</span><span class="sxs-lookup"><span data-stu-id="72e00-312">Report as finished for 4</span></span>
<ul>
<li><span data-ttu-id="72e00-313">Laatutilaus #1 määrälle 1 erästä #b1, sarjanumero #s1.</span><span class="sxs-lookup"><span data-stu-id="72e00-313">Quality order #1 for 1 of batch #b1, serial #s1.</span></span></li>
<li><span data-ttu-id="72e00-314">Laatutilaus #2 määrälle 1 erästä #b2, sarjanumero #s2.</span><span class="sxs-lookup"><span data-stu-id="72e00-314">Quality order #2 for 1 of batch #b2, serial #s2.</span></span></li>
<li><span data-ttu-id="72e00-315">Laatutilaus #3 määrälle 1 erästä #b3, sarjanumero #s3.</span><span class="sxs-lookup"><span data-stu-id="72e00-315">Quality order #3 for 1 of batch #b3, serial #s3.</span></span></li>
<li><span data-ttu-id="72e00-316">Laatutilaus #4 määrälle 1 erästä #b4, sarjanumero #s4.</span><span class="sxs-lookup"><span data-stu-id="72e00-316">Quality order #4 for 1 of batch #b4, serial #s4.</span></span></li>
<li><span data-ttu-id="72e00-317">Jäljelle jäävää määrää varten ei luoda enempää laatutilauksia.</span><span class="sxs-lookup"><span data-stu-id="72e00-317">No more quality orders are created against the remaining quantity.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="72e00-318">Ilmoita valmiiksi 6:n osalta</span><span class="sxs-lookup"><span data-stu-id="72e00-318">Report as finished for 6</span></span>
<ul>
<li><span data-ttu-id="72e00-319">Laatutilauksia ei luota.</span><span class="sxs-lookup"><span data-stu-id="72e00-319">No quality orders are created.</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
</tbody>
</table>

### <a name="production"></a><span data-ttu-id="72e00-320">Tuotanto</span><span class="sxs-lookup"><span data-stu-id="72e00-320">Production</span></span>

<span data-ttu-id="72e00-321">Jos asetat tuotannossa **Tapahtumatyyppi**-kentän arvoksi **Ilmoita valmiiksi** ja **Suoritus**-kentän arvoksi **Jälkeen** **Laatuliitokset**-sivulla, saat seuraavat tulokset:</span><span class="sxs-lookup"><span data-stu-id="72e00-321">In production, if you set the **Event type** field to **Report as finished** and the **Execution** field to **After** on the **Quality associations** page, you get the following results:</span></span>

- <span data-ttu-id="72e00-322">Jos **Päivitettyä määrää kohden** -asetuksen arvoksi määritetään **Kyllä**, laatutilaus luodaan jokaisen valmiin määrän ja nimikeotannan asetusten perusteella.</span><span class="sxs-lookup"><span data-stu-id="72e00-322">If the **Per updated quantity** option is set to **Yes**, a quality order is generated based on every finished quantity and settings in the item sampling.</span></span> <span data-ttu-id="72e00-323">Joka kerta, kun määrä ilmoitetaan valmiiksi tuotantotilauksen perusteella, luodaaan uusia laatutilauksia juuri valmiiksi saadun määrän perusteella.</span><span class="sxs-lookup"><span data-stu-id="72e00-323">Every time that a quantity is reported as finished against the production order, new quality orders are generated based on newly finished quantity.</span></span> <span data-ttu-id="72e00-324">Tämä luontilogiikka on yhdenmukainen oston kanssa.</span><span class="sxs-lookup"><span data-stu-id="72e00-324">This generation logic is consistent with purchasing.</span></span>
- <span data-ttu-id="72e00-325">Jos **Päivitettyä määrää kohden** -asetuksen arvoksi määritetään **Ei**, laatutilaus luodaan valmiiksi saadun määrän perusteella ensimmäisellä kerralla, kun määrä ilmoitetaan valmiiksi.</span><span class="sxs-lookup"><span data-stu-id="72e00-325">If the **Per updated quantity** option is set to **No**, a quality order is generated the first time that a quantity is reported as finished, based on the finished quantity.</span></span> <span data-ttu-id="72e00-326">Lisäksi jäljelle jäävän määrän perusteella luodaan nimikeotannan seurantadimensioiden mukaan vähintään yksi laatutilaus.</span><span class="sxs-lookup"><span data-stu-id="72e00-326">Additionally, one or more quality orders are created based on the remaining quantity, depending on the tracking dimensions of the item sampling.</span></span> <span data-ttu-id="72e00-327">Seuraaville valmiille määrille ei luoda laatutilauksia.</span><span class="sxs-lookup"><span data-stu-id="72e00-327">Quality orders aren't generated for subsequent finished quantities.</span></span>

<table>
<tbody>
<tr>
<th><span data-ttu-id="72e00-328">Laatumääritys</span><span class="sxs-lookup"><span data-stu-id="72e00-328">Quality specification</span></span></th>
<th><span data-ttu-id="72e00-329">Päivitettyä määrää kohden</span><span class="sxs-lookup"><span data-stu-id="72e00-329">Per updated quantity</span></span></th>
<th><span data-ttu-id="72e00-330">Seurantadimension mukaan</span><span class="sxs-lookup"><span data-stu-id="72e00-330">Per tracking dimension</span></span></th>
<th><span data-ttu-id="72e00-331">Tulos</span><span class="sxs-lookup"><span data-stu-id="72e00-331">Result</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="72e00-332">Prosenttiosuus: 10 %</span><span class="sxs-lookup"><span data-stu-id="72e00-332">Percentage: 10%</span></span></td>
<td><span data-ttu-id="72e00-333">Kyllä</span><span class="sxs-lookup"><span data-stu-id="72e00-333">Yes</span></span></td>
<td>
<p><span data-ttu-id="72e00-334">Eränumero: Ei</span><span class="sxs-lookup"><span data-stu-id="72e00-334">Batch number: No</span></span></p>
<p><span data-ttu-id="72e00-335">Sarjanumero: Ei</span><span class="sxs-lookup"><span data-stu-id="72e00-335">Serial number: No</span></span></p>
</td>
<td>
<p><span data-ttu-id="72e00-336">Tilausmäärä: 100</span><span class="sxs-lookup"><span data-stu-id="72e00-336">Order quantity: 100</span></span></p>
<ol>
<li><span data-ttu-id="72e00-337">Ilmoita valmiiksi 30:n osalta</span><span class="sxs-lookup"><span data-stu-id="72e00-337">Report as finished for 30</span></span>
<ul>
<li><span data-ttu-id="72e00-338">Laatutilaus #1 määrälle 3 (10 prosenttia 30:stä)</span><span class="sxs-lookup"><span data-stu-id="72e00-338">Quality order #1 for 3 (10% of 30)</span></span></li>
</ul>
</li>
<li><span data-ttu-id="72e00-339">Ilmoita valmiiksi 70:n osalta</span><span class="sxs-lookup"><span data-stu-id="72e00-339">Report as finished for 70</span></span>
<ul>
<li><span data-ttu-id="72e00-340">Laatutilaus #2 määrälle 7 (10 % jäljellä olevasta tilausmäärästä eli 70:stä)</span><span class="sxs-lookup"><span data-stu-id="72e00-340">Quality order #2 for 7 (10% of the remaining order quantity, which equals 70 in this case)</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="72e00-341">Kiinteä määrä: 1</span><span class="sxs-lookup"><span data-stu-id="72e00-341">Fixed quantity: 1</span></span></td>
<td><span data-ttu-id="72e00-342">Ei</span><span class="sxs-lookup"><span data-stu-id="72e00-342">No</span></span></td>
<td>
<p><span data-ttu-id="72e00-343">Eränumero: Ei</span><span class="sxs-lookup"><span data-stu-id="72e00-343">Batch number: No</span></span></p>
<p><span data-ttu-id="72e00-344">Sarjanumero: Ei</span><span class="sxs-lookup"><span data-stu-id="72e00-344">Serial number: No</span></span></p>
</td>
<td><span data-ttu-id="72e00-345">Tilausmäärä: 100</span><span class="sxs-lookup"><span data-stu-id="72e00-345">Order quantity: 100</span></span>
<ol>
<li><span data-ttu-id="72e00-346">Ilmoita valmiiksi 30:n osalta</span><span class="sxs-lookup"><span data-stu-id="72e00-346">Report as finished for 30</span></span>
<ul>
<li><span data-ttu-id="72e00-347">Laatutilaus #1 määrälle 1 (ensimmäiselle valmiiksi ilmoitetulle määrälle, jolla on kiinteä arvo 1)</span><span class="sxs-lookup"><span data-stu-id="72e00-347">Quality order #1 for 1 (for the first reported-as-finished quantity, which has a fixed value of 1)</span></span></li>
<li><span data-ttu-id="72e00-348">Laatutilaus #2 määrälle 1 (jäljelle olevalle määrälle, jolla on edelleen kiinteä arvo 1)</span><span class="sxs-lookup"><span data-stu-id="72e00-348">Quality order #2 for 1 (for the remaining quantity, which still has a fixed value of 1)</span></span></li>
</ul>
</li>
<li><span data-ttu-id="72e00-349">Ilmoita valmiiksi 10:n osalta</span><span class="sxs-lookup"><span data-stu-id="72e00-349">Report as finished for 10</span></span>
<ul>
<li><span data-ttu-id="72e00-350">Laatutilauksia ei luota.</span><span class="sxs-lookup"><span data-stu-id="72e00-350">No quality orders are created.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="72e00-351">Ilmoita valmiiksi 60:n osalta</span><span class="sxs-lookup"><span data-stu-id="72e00-351">Report as finished for 60</span></span>
<ul>
<li><span data-ttu-id="72e00-352">Laatutilauksia ei luota.</span><span class="sxs-lookup"><span data-stu-id="72e00-352">No quality orders are created.</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="72e00-353">Kiinteä määrä: 1</span><span class="sxs-lookup"><span data-stu-id="72e00-353">Fixed quantity: 1</span></span></td>
<td><span data-ttu-id="72e00-354">Kyllä</span><span class="sxs-lookup"><span data-stu-id="72e00-354">Yes</span></span></td>
<td>
<p><span data-ttu-id="72e00-355">Eränumero: Kyllä</span><span class="sxs-lookup"><span data-stu-id="72e00-355">Batch number: Yes</span></span></p>
<p><span data-ttu-id="72e00-356">Sarjanumero: Kyllä</span><span class="sxs-lookup"><span data-stu-id="72e00-356">Serial number: Yes</span></span></p>
</td>
<td>
<p><span data-ttu-id="72e00-357">Tilausmäärä: 10</span><span class="sxs-lookup"><span data-stu-id="72e00-357">Order quantity: 10</span></span></p>
<ol>
<li><span data-ttu-id="72e00-358">Ilmoita valmiiksi 3:n osalta: 1 erässä #b1, #s1; 1 erässä #b2, #s2; ja 1 erässä #b3, #s3</span><span class="sxs-lookup"><span data-stu-id="72e00-358">Report as finished for 3: 1 for #b1, #s1; 1 for #b2, #s2; and 1 for #b3, #s3</span></span>
<ul>
<li><span data-ttu-id="72e00-359">Laatutilaus #1 määrälle 1 erästä #b1, sarjanumero #s1</span><span class="sxs-lookup"><span data-stu-id="72e00-359">Quality order #1 for 1 of batch #b1, serial #s1</span></span></li>
<li><span data-ttu-id="72e00-360">Laatutilaus #2 määrälle 1 erästä #b2, sarjanumero #s2</span><span class="sxs-lookup"><span data-stu-id="72e00-360">Quality order #2 for 1 of batch #b2, serial #s2</span></span></li>
<li><span data-ttu-id="72e00-361">Laatutilaus #3 määrälle 1 erästä #b3, sarjanumero #s3</span><span class="sxs-lookup"><span data-stu-id="72e00-361">Quality order #3 for 1 of batch #b3, serial #s3</span></span></li>
</ul>
</li>
<li><span data-ttu-id="72e00-362">Ilmoita valmiiksi 2:n osalta: 1 erässä #b4, #s4; ja 1 erässä #b5, #s5</span><span class="sxs-lookup"><span data-stu-id="72e00-362">Report as finished for 2: 1 for #b4, #s4; and 1 for #b5, #s5</span></span>
<ul>
<li><span data-ttu-id="72e00-363">Laatutilaus #4 määrälle 1 erästä #b4, sarjanumero #s4</span><span class="sxs-lookup"><span data-stu-id="72e00-363">Quality order #4 for 1 of batch #b4, serial #s4</span></span></li>
<li><span data-ttu-id="72e00-364">Laatutilaus #5 määrälle 1 erästä #b5, sarjanumero #s5</span><span class="sxs-lookup"><span data-stu-id="72e00-364">Quality order #5 for 1 of batch #b5, serial #s5</span></span></li>
</ul>
</li>
</ol>
<p><span data-ttu-id="72e00-365"><strong>Huomautus:</strong> Erää voidaan käyttää uudelleen.</span><span class="sxs-lookup"><span data-stu-id="72e00-365"><strong>Note:</strong> The batch can be reused.</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="72e00-366">Kiinteä määrä: 2</span><span class="sxs-lookup"><span data-stu-id="72e00-366">Fixed quantity: 2</span></span></td>
<td><span data-ttu-id="72e00-367">Ei</span><span class="sxs-lookup"><span data-stu-id="72e00-367">No</span></span></td>
<td>
<p><span data-ttu-id="72e00-368">Eränumero: Kyllä</span><span class="sxs-lookup"><span data-stu-id="72e00-368">Batch number: Yes</span></span></p>
<p><span data-ttu-id="72e00-369">Sarjanumero: Kyllä</span><span class="sxs-lookup"><span data-stu-id="72e00-369">Serial number: Yes</span></span></p>
</td>
<td>
<p><span data-ttu-id="72e00-370">Tilausmäärä: 10</span><span class="sxs-lookup"><span data-stu-id="72e00-370">Order quantity: 10</span></span></p>
<ol>
<li><span data-ttu-id="72e00-371">Ilmoita valmiiksi 4:n osalta: 1 erässä #b1, #s1; 1 erässä #b2, #s2; 1 erässä #b3, #s3 ja 1 erässä #b4, #s4</span><span class="sxs-lookup"><span data-stu-id="72e00-371">Report as finished for 4: 1 for #b1, #s1; 1 for #b2, #s2; 1 for #b3, #s3; and 1 for #b4, #s4</span></span>
<ul>
<li><span data-ttu-id="72e00-372">Laatutilaus #1 määrälle 1 erästä #b1, sarjanumero #s1</span><span class="sxs-lookup"><span data-stu-id="72e00-372">Quality order #1 for 1 of batch #b1, serial #s1</span></span></li>
<li><span data-ttu-id="72e00-373">Laatutilaus #2 määrälle 1 erästä #b2, sarjanumero #s2</span><span class="sxs-lookup"><span data-stu-id="72e00-373">Quality order #2 for 1 of batch #b2, serial #s2</span></span></li>
<li><span data-ttu-id="72e00-374">Laatutilaus #3 määrälle 1 erästä #b3, sarjanumero #s3</span><span class="sxs-lookup"><span data-stu-id="72e00-374">Quality order #3 for 1 of batch #b3, serial #s3</span></span></li>
<li><span data-ttu-id="72e00-375">Laatutilaus #4 määrälle 1 erästä #b4, sarjanumero #s4</span><span class="sxs-lookup"><span data-stu-id="72e00-375">Quality order #4 for 1 of batch #b4, serial #s4</span></span></li>
</ul>
<ul>
<li><span data-ttu-id="72e00-376">Laatutilaus #5 määrälle 2 ilman viittausta erä- ja sarjanumeroon</span><span class="sxs-lookup"><span data-stu-id="72e00-376">Quality order #5 for 2, without a reference to a batch and a serial number</span></span></li>
</ul>
</li>
<li><span data-ttu-id="72e00-377">Ilmoita valmiiksi 6:n osalta: 1 erässä #b5, #s5; 1 erässä #b6, #s6; 1 erässä #b7, #s7; 1 erässä #b8, #s8; 1 erässä #b9, #s9; ja 1 erässä #b10, #s10</span><span class="sxs-lookup"><span data-stu-id="72e00-377">Report as finished for 6: 1 for #b5, #s5; 1 for #b6, #s6; 1 for #b7, #s7; 1 for #b8, #s8; 1 for #b9, #s9; and 1 for #b10, #s10</span></span>
<ul>
<li><span data-ttu-id="72e00-378">Laatutilauksia ei luota.</span><span class="sxs-lookup"><span data-stu-id="72e00-378">No quality orders are created.</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
</tbody>
</table>

## <a name="quality-management-pages"></a><span data-ttu-id="72e00-379">Laadunhallinnan sivut</span><span class="sxs-lookup"><span data-stu-id="72e00-379">Quality management pages</span></span>
<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="72e00-380">Sivu</span><span class="sxs-lookup"><span data-stu-id="72e00-380">Page</span></span></th>
<th><span data-ttu-id="72e00-381">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="72e00-381">Description</span></span></th>
<th><span data-ttu-id="72e00-382">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="72e00-382">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="72e00-383">Laatuliitokset</span><span class="sxs-lookup"><span data-stu-id="72e00-383">Quality associations</span></span></td>
<td><span data-ttu-id="72e00-384">Katso artikkelin edelliset osat.</span><span class="sxs-lookup"><span data-stu-id="72e00-384">See the previous sections of this article.</span></span></td>
<td><span data-ttu-id="72e00-385">Laatuliitos määrittää kaikki seuraavat muodostettavan laatutilauksen tiedot:</span><span class="sxs-lookup"><span data-stu-id="72e00-385">A quality association defines all the following information for a quality order that is generated:</span></span>
<ul>
<li><span data-ttu-id="72e00-386">Tapahtuma</span><span class="sxs-lookup"><span data-stu-id="72e00-386">The transaction event</span></span></li>
<li><span data-ttu-id="72e00-387">Nimikkeissä suoritettavat testit</span><span class="sxs-lookup"><span data-stu-id="72e00-387">The set of tests that must be performed on the items</span></span></li>
<li><span data-ttu-id="72e00-388">Hyväksyttävän laadun taso</span><span class="sxs-lookup"><span data-stu-id="72e00-388">The AQL</span></span></li>
<li><span data-ttu-id="72e00-389">Otantasuunnitelma</span><span class="sxs-lookup"><span data-stu-id="72e00-389">The sampling plan</span></span></li>
</ul>
<span data-ttu-id="72e00-390">Laatuliitos on määritettävä kutakin sellaista liiketoimintaprosessin muutosta varten, joka edellyttää automaattista laatutilausten luontia.</span><span class="sxs-lookup"><span data-stu-id="72e00-390">You must define a quality association for each variation in a business process that requires automatic generation of quality orders.</span></span> <span data-ttu-id="72e00-391">Laatutilaus voidaan esimerkiksi muodostaa ostotilausten, karanteenitilausten, myyntitilausten ja tuotantotilausten liiketoimintaprosesseille.</span><span class="sxs-lookup"><span data-stu-id="72e00-391">For example, a quality order can be generated in the business processes for purchase orders, quarantine orders, sales orders, and production orders.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="72e00-392">Testit</span><span class="sxs-lookup"><span data-stu-id="72e00-392">Tests</span></span></td>
<td><span data-ttu-id="72e00-393">Voit määrittää ja tarkastella tällä sivulla yksittäisiä testejä, joiden mukaan määräytyy, ovatko tuotteet laatuvaatimusten mukaisia.</span><span class="sxs-lookup"><span data-stu-id="72e00-393">Use this page to define and view the individual tests that determine whether your products meet quality specifications.</span></span> <span data-ttu-id="72e00-394">Voit määrittää testiryhmälle vähintään yhden yksittäisen testin.</span><span class="sxs-lookup"><span data-stu-id="72e00-394">You can assign one or more individual tests to a test group.</span></span> <span data-ttu-id="72e00-395">Siinä tapauksessa määrität myös testikohtaiset tiedot, kuten hyväksyttävät mitta-arvot.</span><span class="sxs-lookup"><span data-stu-id="72e00-395">In this case, you also specify test-specific information, such as the acceptable measurement values.</span></span> <span data-ttu-id="72e00-396">Mitta-arvoja käytetään määrällisissä testeissä, kun taas laadullisissa testeissä käytetään testimuuttujia.</span><span class="sxs-lookup"><span data-stu-id="72e00-396">Measurement values are used for quantitative tests, and test variables are used for qualitative tests.</span></span>
<ul>
<li><span data-ttu-id="72e00-397">Määrällisen testin testityyppi on <strong>Kokonaisluku</strong> tai <strong>Nimellinen</strong>. Lisäksi siihen on määritetty mittayksikkö.</span><span class="sxs-lookup"><span data-stu-id="72e00-397">A quantitative test has a test type of <strong>Integer</strong> or <strong>Fraction</strong>, and also has a designated unit of measure.</span></span> <span data-ttu-id="72e00-398">Laatumääritykset ja testitulokset ilmaistaan numeroina.</span><span class="sxs-lookup"><span data-stu-id="72e00-398">Quality specifications and test results are expressed as numbers.</span></span></li>
<li><span data-ttu-id="72e00-399">Laadullisen testin testityyppi on <strong>Vaihtoehto</strong>.</span><span class="sxs-lookup"><span data-stu-id="72e00-399">A qualitative test has a test type of <strong>Option</strong>.</span></span> <span data-ttu-id="72e00-400">Laadullista testiä varten tarvitaan lisätietoja mitattavasta testimuuttujasta ja sen numeroiduista vaihtoehdoista.</span><span class="sxs-lookup"><span data-stu-id="72e00-400">Qualitative tests require additional information about the test variable that is being measured and its enumerated options.</span></span> <span data-ttu-id="72e00-401">Laatumääritykset ja testitulokset ilmaistaan tuloksen perusteella.</span><span class="sxs-lookup"><span data-stu-id="72e00-401">Quality specifications and test results are expressed according to an outcome.</span></span></li>
</ul></td>
<td><span data-ttu-id="72e00-402">Teollisuusyritys suorittaa ostamalleen materiaalille kaksi testiä: materiaalin laatua koskevan määrällisen testin ja pakkausvahinkoja koskevan laadullisen testin.</span><span class="sxs-lookup"><span data-stu-id="72e00-402">A manufacturing company performs two tests on purchased material: a quantitative test about material quality and a qualitative test about packaging damage.</span></span> <span data-ttu-id="72e00-403">Yritys määrittää laadullisen testin lisätiedoiksi testimuuttujan (vioittunut pakkaus) ja sen mahdolliset tulokset.</span><span class="sxs-lookup"><span data-stu-id="72e00-403">The company defines additional information about the qualitative test to identify the test variable (damaged packaging) and its outcomes.</span></span> <span data-ttu-id="72e00-404">Yritys määrittää <strong>Testiryhmät</strong>-sivulla kaksi testiä testiryhmään. Lisäksi testikohtaiset tiedot määritetään.</span><span class="sxs-lookup"><span data-stu-id="72e00-404">The company uses the <strong>Test groups</strong> page to assign the two tests to a test group and to specify the test-specific information.</span></span> <span data-ttu-id="72e00-405">Testiryhmä määritetään laatutilaukseen, jotta yritys voi raportoida näiden kahden testin testitulokset.</span><span class="sxs-lookup"><span data-stu-id="72e00-405">The test group is assigned to a quality order, so that the company can report test results for the two tests.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="72e00-406">Testiryhmät</span><span class="sxs-lookup"><span data-stu-id="72e00-406">Test groups</span></span></td>
<td><span data-ttu-id="72e00-407">Voit määrittää, muokata ja tarkastella tällä sivulla testiryhmiä ja testiryhmälle määritettyjä yksittäisiä testejä.</span><span class="sxs-lookup"><span data-stu-id="72e00-407">Use this page to set up, edit, and view test groups and the individual tests that are assigned to a test group.</span></span> <span data-ttu-id="72e00-408">Yläruudussa näkyvät testiryhmät, ja alaruudussa näkyvät valitulle testiryhmälle määritetyt testit.</span><span class="sxs-lookup"><span data-stu-id="72e00-408">The upper pane displays test groups, and the lower pane displays the tests that are assigned to a selected test group.</span></span> <span data-ttu-id="72e00-409">Voit määrittää testiryhmälle useita käytäntöjä, kuten otantasuunnitelman, hyväksytyn laatutason ja tuhoavan testin tarpeen.</span><span class="sxs-lookup"><span data-stu-id="72e00-409">You assign several policies to a test group, such as a sampling plan, an AQL, and the requirement for destructive testing.</span></span> <span data-ttu-id="72e00-410">Kun määrität testiryhmään yksittäisen testin, määrität samalla lisätietoja, kuten järjestyksen, asiakirjat ja voimassaolopäivät.</span><span class="sxs-lookup"><span data-stu-id="72e00-410">When you assign an individual test to a test group, you define additional information, such as the sequence, documents, and validity dates.</span></span> <span data-ttu-id="72e00-411">Määrällisessä testissä määritetään myös hyväksyttävät mitta-arvot.</span><span class="sxs-lookup"><span data-stu-id="72e00-411">For a quantitative test, the information that you define also includes the acceptable measurement values.</span></span> <span data-ttu-id="72e00-412">Laadullisessa testissä tietoja ovat testimuuttuja ja oletustulos.</span><span class="sxs-lookup"><span data-stu-id="72e00-412">For a qualitative test, the information includes the test variable and default outcome.</span></span> <span data-ttu-id="72e00-413">Laatutilaukseen määritetty testiryhmä määrittää oletustestit, jotka tietylle nimikkeelle on suoritettava.</span><span class="sxs-lookup"><span data-stu-id="72e00-413">The test group that is assigned to a quality order defines the default set of tests that must be performed on the specified item.</span></span> <span data-ttu-id="72e00-414">Voit kuitenkin lisätä, muuttaa ja poistaa laatutilauksen testejä.</span><span class="sxs-lookup"><span data-stu-id="72e00-414">However, you can add, delete, or change tests on the quality order.</span></span> <span data-ttu-id="72e00-415">Laatutilauksen jokaisen testin tulokset raportoidaan.</span><span class="sxs-lookup"><span data-stu-id="72e00-415">Test results are reported for each test on a quality order.</span></span></td>
<td><span data-ttu-id="72e00-416">Tuotantoyritys määrittää testiryhmän kutakin laatuvaatimusversiotaan varten.</span><span class="sxs-lookup"><span data-stu-id="72e00-416">A manufacturing company defines a test group for each variation of its quality guidelines.</span></span> <span data-ttu-id="72e00-417">Eri testiryhmät edustavat eroja otantasuunnitelmissa, yhdessä suoritettavissa testeissä, hyväksytyissä mitta-arvoissa ja muissa seikoissa.</span><span class="sxs-lookup"><span data-stu-id="72e00-417">The various test groups reflect differences in the sampling plans, the sets of tests that must be performed together, the AQL, and other factors.</span></span> <span data-ttu-id="72e00-418">Määrällisissä testeissä eroja on hyväksyttävissä mitta-arvoissa.</span><span class="sxs-lookup"><span data-stu-id="72e00-418">For quantitative tests, there are also differences in the acceptable measurement values.</span></span> <span data-ttu-id="72e00-419">Jotta yritys voisi ottaa laatuvaatimuksensa käyttöön, se määrittää kullekin säännölle testiryhmän automaattista laatutilausten luontia varten <strong>Laatuliitokset</strong>-sivulla. Lisäksi se määrittää testiryhmän manuaalisesti luoduille laatutilauksille.</span><span class="sxs-lookup"><span data-stu-id="72e00-419">To enforce its quality guidelines, the company assigns a test group to each rule for automatically generating quality orders on the <strong>Quality associations</strong> page, and also assigns a test group to quality orders that are manually created.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="72e00-420">Nimikkeen laaturyhmät</span><span class="sxs-lookup"><span data-stu-id="72e00-420">Item quality groups</span></span></td>
<td><span data-ttu-id="72e00-421">Voit määrittää, muokata ja tarkastella tällä sivulla nimikkeitä, jotka on määritetty nimikkeelle määritettyihin laaturyhmiin.</span><span class="sxs-lookup"><span data-stu-id="72e00-421">Use this page to set up, edit, and view the items that are assigned to a quality group or the quality groups that are assigned to an item.</span></span> <span data-ttu-id="72e00-422">Laaturyhmän avulla voidaan määrittää nimikkeiden yhteisiä testausvaatimuksia.</span><span class="sxs-lookup"><span data-stu-id="72e00-422">A quality group represents common testing requirements for items.</span></span> <span data-ttu-id="72e00-423">Kun olet määrittänyt testivaatimukset <strong>Testiryhmät</strong>-sivulla, voit määrittää laatutilausten automaattisen luonnin säännöt.</span><span class="sxs-lookup"><span data-stu-id="72e00-423">After you define the test requirements on the <strong>Test groups</strong> page, you can define the rules for automatically generating quality orders.</span></span> <span data-ttu-id="72e00-424">Prosessin yksinkertaistamiseksi sääntöjä ei määritetä yksittäisille nimikkeille.</span><span class="sxs-lookup"><span data-stu-id="72e00-424">To simplify the process, you don&#39;t define rules for individual items.</span></span> <span data-ttu-id="72e00-425">Sen sijaan <strong>Laatuliitokset</strong>-sivulla määritetään laaturyhmän säännöt.</span><span class="sxs-lookup"><span data-stu-id="72e00-425">Instead, you define rules for a quality group, by using the <strong>Quality associations</strong> page.</span></span> <span data-ttu-id="72e00-426">Voit myös määrittää valitun laaturyhmän <strong>Nimikkeen laaturyhmät</strong> -sivulla kyseiseen ryhmään liittyvät nimikkeet.</span><span class="sxs-lookup"><span data-stu-id="72e00-426">You can also use the <strong>Item quality groups</strong> page for a selected quality group to assign relevant items to that group.</span></span> <span data-ttu-id="72e00-427">Voit myös määrittää valitun nimikkeen <strong>Nimikkeen laaturyhmät</strong> -sivulla kyseiseen nimikkeeseen liittyvät laaturyhmät.</span><span class="sxs-lookup"><span data-stu-id="72e00-427">You can also use the <strong>Item quality groups</strong> page for a selected item to assign relevant quality groups to that item.</span></span></td>
<td><span data-ttu-id="72e00-428">Teollisuusyritys ostaa useita eri raaka-aineita, joilla on samat testausvaatimukset tulevaa tarkistusta varten.</span><span class="sxs-lookup"><span data-stu-id="72e00-428">A manufacturing company purchases various raw materials that have the same testing requirements for incoming inspection.</span></span> <span data-ttu-id="72e00-429">Yritys määrittää ensin laaturyhmän ja sitten nimiketunnukset, jotka liittyvät kyseisen ryhmän raaka-aineisiin.</span><span class="sxs-lookup"><span data-stu-id="72e00-429">The company defines a quality group and then assigns the item numbers that are associated with the raw materials to that group.</span></span> <span data-ttu-id="72e00-430">Yritys ostaa myöhemmin uutta raaka-ainetta, jolla on samat testausvaatimukset.</span><span class="sxs-lookup"><span data-stu-id="72e00-430">Later, the company purchases a new type of raw material that has the same testing requirements.</span></span> <span data-ttu-id="72e00-431">Yritys ei määritä uudelle raaka-aineelle uusia testausvaatimuksia vaan lisää uuden materiaalin nimiketunnuksen aiemmin luotuun laaturyhmään.</span><span class="sxs-lookup"><span data-stu-id="72e00-431">Instead of setting up new testing requirements for the new material, the company adds the item number for the new material to the existing quality group.</span></span> <span data-ttu-id="72e00-432">Sama teollisuusyritys myös tuottaa nimikkeitä, joilla on samat tuotannon testausvaatimukset, sekä lähettää nimikkeitä, joilla on samat vaatimukset lähetystä edeltävien testien suorittamiseksi.</span><span class="sxs-lookup"><span data-stu-id="72e00-432">The same manufacturing company also produces items that have the same production testing requirements and ships items that have the same requirement for pre-shipment testing.</span></span> <span data-ttu-id="72e00-433">Yritys määrittää ensin kaksi laaturyhmää lisää ja sitten kumpaankin soveltuvat nimiketunnukset.</span><span class="sxs-lookup"><span data-stu-id="72e00-433">The company defines two additional quality groups and then assigns the relevant item numbers to each group.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="72e00-434">Testimuuttujat</span><span class="sxs-lookup"><span data-stu-id="72e00-434">Test variables</span></span></td>
<td><span data-ttu-id="72e00-435">Voit määrittää ja tarkastella tällä sivulla laadulliseen testiin liitettyjä muuttujia.</span><span class="sxs-lookup"><span data-stu-id="72e00-435">Use this page to define and view the variables that are associated with a qualitative test.</span></span> <span data-ttu-id="72e00-436">Jokaiselle muuttujalle määritetään numeroitu tulos, joka ilmaisee mahdollisen vaihtoehdon.</span><span class="sxs-lookup"><span data-stu-id="72e00-436">For each variable, you define enumerated outcomes that represent the possible options.</span></span> <span data-ttu-id="72e00-437">Testit määritetään <strong>Testit</strong>-sivulla.</span><span class="sxs-lookup"><span data-stu-id="72e00-437">You define tests on the <strong>Tests</strong> page.</span></span> <span data-ttu-id="72e00-438">Laadullisten testien testityypiksi on valittava <strong>Vaihtoehto</strong>.</span><span class="sxs-lookup"><span data-stu-id="72e00-438">For qualitative tests, you must set the test type to <strong>Option</strong>.</span></span> <span data-ttu-id="72e00-439">Määritä yksittäisen testin testimuuttuja <strong>Testiryhmät</strong>-sivulla.</span><span class="sxs-lookup"><span data-stu-id="72e00-439">Use the <strong>Test groups</strong> page to assign a test variable to an individual test.</span></span></td>
<td><span data-ttu-id="72e00-440">Pikkuleipiä valmistava teollisuusyritys tarkastaa lopputuotteen testillä.</span><span class="sxs-lookup"><span data-stu-id="72e00-440">A manufacturing company that produces cookies uses an inspection test for the finished product.</span></span> <span data-ttu-id="72e00-441">Tarkastuksessa on useita muuttujia.</span><span class="sxs-lookup"><span data-stu-id="72e00-441">This inspection test has several variables.</span></span> <span data-ttu-id="72e00-442">Ensimmäinen muuttuja on maku, jonka mahdollisia tuloksia ovat hyvä ja paha.</span><span class="sxs-lookup"><span data-stu-id="72e00-442">One variable is taste, and the possible outcomes for this variable are good and bad.</span></span> <span data-ttu-id="72e00-443">Toinen muuttuja on väri, jonka mahdollisia tuloksia ovat liian tumma, liian vaalea ja oikea.</span><span class="sxs-lookup"><span data-stu-id="72e00-443">A second variable is color, and the possible outcomes are too dark, too light, and correct.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="72e00-444">Testimuuttujien tulokset</span><span class="sxs-lookup"><span data-stu-id="72e00-444">Test variable outcomes</span></span></td>
<td><span data-ttu-id="72e00-445">Voit määrittää, muokata ja tarkastella tällä sivulla laadulliseen testiin liittyvän testimuuttujan mahdollisia testituloksia.</span><span class="sxs-lookup"><span data-stu-id="72e00-445">Use this page to set up, edit, and to view the possible test results for a test variable that is associated with a qualitative test.</span></span> <span data-ttu-id="72e00-446">Kunkin tuloksen tilaksi määritetään joko <strong>hyväksytty</strong> tai <strong>hylätty</strong>.</span><span class="sxs-lookup"><span data-stu-id="72e00-446">For each outcome, you assign a <strong>pass</strong> or <strong>fail</strong> status.</span></span> <span data-ttu-id="72e00-447">Jokaiselle <strong>Testit</strong>-sivulla määritetylle laadulliselle testille on määritettävä muuttuja ja tulokset.</span><span class="sxs-lookup"><span data-stu-id="72e00-447">You must define a variable and its outcomes for each qualitative test that is defined on the <strong>Tests</strong> page.</span></span> <span data-ttu-id="72e00-448">(Laadullisten testien tyypiksi on määritetty <strong>Vaihtoehto</strong> <strong>Testit</strong>-sivulla.) Käytä <strong>Testiryhmät</strong>-sivua määrittääksesi yksittäisen laadullisen testin testimuuttujan ja oletustuloksen.</span><span class="sxs-lookup"><span data-stu-id="72e00-448">(For qualitative tests, the test type is set to <strong>Option</strong> on the <strong>Tests</strong> page.) Use the <strong>Test groups</strong> page to assign a test variable and the default outcome to an individual qualitative test.</span></span></td>
<td><span data-ttu-id="72e00-449">Pikkuleipiä valmistava teollisuusyritys tarkastaa lopputuotteen testillä.</span><span class="sxs-lookup"><span data-stu-id="72e00-449">A manufacturing company that produces cookies uses an inspection test for the finished product.</span></span> <span data-ttu-id="72e00-450">Tarkastuksessa on useita muuttujia.</span><span class="sxs-lookup"><span data-stu-id="72e00-450">This inspection test has of several variables.</span></span> <span data-ttu-id="72e00-451">Ensimmäinen muuttuja on maku, jonka mahdollisia tuloksia ovat hyvä ja paha.</span><span class="sxs-lookup"><span data-stu-id="72e00-451">One variable is taste, and the possible outcomes for this variable are good and bad.</span></span> <span data-ttu-id="72e00-452">Toinen muuttuja on väri, jonka mahdollisia tuloksia ovat liian tumma, liian vaalea ja oikea.</span><span class="sxs-lookup"><span data-stu-id="72e00-452">A second variable is color, and the possible outcomes are too dark, too light, and correct.</span></span> <span data-ttu-id="72e00-453">Kunkin tuloksen tilaksi määritetään <strong>hyväksytty</strong> tai <strong>hylätty</strong>.</span><span class="sxs-lookup"><span data-stu-id="72e00-453">A status of <strong>pass</strong> or <strong>fail</strong> is assigned to each outcome.</span></span> <span data-ttu-id="72e00-454">Kunkin muuttujan tarkastuksen aikana tarkastaja raportoi testin tuloksen valitsemalla yhden tuloksista.</span><span class="sxs-lookup"><span data-stu-id="72e00-454">During the inspection test for each variable, the inspector reports the test result by selecting one of the outcomes.</span></span></td>
</tr>
</tbody>
</table>



<a name="additional-resources"></a><span data-ttu-id="72e00-455">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="72e00-455">Additional resources</span></span>
--------

[<span data-ttu-id="72e00-456">Laadunhallintaprosessit</span><span class="sxs-lookup"><span data-stu-id="72e00-456">Quality management processes</span></span>](quality-management-processes.md)

[<span data-ttu-id="72e00-457">Määrityksistä poikkeamisen hallinnan ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="72e00-457">Enabling nonconformance management</span></span>](enable-nonconformance-management.md)
