---
title: Laadunhallinnan yleiskuvaus
description: Tässä ohjeaiheessa kerrotaan, miten Dynamics 365 Supply Chain Managementin laadunhallinnan avulla voidaan parantaa toimitusketjun tuotteiden laatua.
author: perlynne
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTestAssociationTable, InventTestGroup, InventTestItemQualityGroup, InventTestTable, InventTestVariable, InventTestVariableOutcome
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e1d7828e6bb9a3684c1d76e2cfac96174a8dfbf4
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4427145"
---
# <a name="quality-management-overview"></a><span data-ttu-id="29cc7-103">Laadunhallinnan yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="29cc7-103">Quality management overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="29cc7-104">Tässä ohjeaiheessa kerrotaan, miten Dynamics 365 Supply Chain Managementin laadunhallinnan avulla voidaan parantaa toimitusketjun tuotteiden laatua.</span><span class="sxs-lookup"><span data-stu-id="29cc7-104">This topic describes how you can use quality management in Dynamics 365 Supply Chain Management to help improve product quality within your supply chain.</span></span>

<span data-ttu-id="29cc7-105">Laadunhallinnan avulla voit hallita määrityksestä poikkeavien tuotteiden käsittelyaikaa niiden lähtöpisteestä riippumatta.</span><span class="sxs-lookup"><span data-stu-id="29cc7-105">Quality management can help you manage turnaround times when you handle nonconforming products, regardless of their point of origin.</span></span> <span data-ttu-id="29cc7-106">Koska vianmääritystyypit linkitetään korjausraportointiin, Supply Chain Management voi ajoittaa ongelmien korjaustehtävät ja estää ongelmien toistuminen.</span><span class="sxs-lookup"><span data-stu-id="29cc7-106">Because diagnostic types are linked to correction reporting, Supply Chain Management can schedule tasks to correct problems and prevent them from recurring.</span></span>

<span data-ttu-id="29cc7-107">Määrityksistä poikkeamisen hallintatoiminnon lisäksi laadunhallinta sisältää toiminnon ongelmien seuraamiseen ongelmantyypin perusteella (myös sisäiset ongelmat) sekä lyhyt- tai pitkäaikaisen ratkaisun tunnistamiseen.</span><span class="sxs-lookup"><span data-stu-id="29cc7-107">In addition to functionality for managing nonconformance, quality management includes functionality for tracking issues by problem type (even internal problems), and for identifying solutions as short-term or long-term.</span></span> <span data-ttu-id="29cc7-108">Suorituskykyilmaisimia (KPI) koskevat tilastot antavat tietoja aiemmista määrityksistä poikkeamiseen liittyvistä ongelmista ja niiden korjaamiseen käytetyistä ratkaisuista.</span><span class="sxs-lookup"><span data-stu-id="29cc7-108">Statistics about key performance indicators (KPIs) provide insight into the history of previous nonconformance issues and the solutions that were used to correct them.</span></span> <span data-ttu-id="29cc7-109">Voit tarkistaa historiallisten tietojen avulla, kuinka tehokkaita aiemmat laatutoimet ovat olleet, ja määrittää, mitkä toimet soveltuvat jatkossa käytettäviksi.</span><span class="sxs-lookup"><span data-stu-id="29cc7-109">You can use historical data to review the effectiveness of previous quality measures and determine appropriate measures to use in the future.</span></span>

<span data-ttu-id="29cc7-110">Kun määrität laatuliitoksen, Supply Chain Management voi luoda liiketoiminnan eri prosesseille, tapahtumille ja ehdoille laatutilauksia.</span><span class="sxs-lookup"><span data-stu-id="29cc7-110">When you set up a quality association, Supply Chain Management can generate quality orders for various business processes, events, and conditions.</span></span> <span data-ttu-id="29cc7-111">Laatuliitos voi koskea tiettyä nimikettä, tiettyä nimikeryhmää tai kaikkia nimikkeitä.</span><span class="sxs-lookup"><span data-stu-id="29cc7-111">The quality association can cover a specific item, a specific group of items, or all items.</span></span>

## <a name="examples-of-the-use-of-quality-management"></a><span data-ttu-id="29cc7-112">Esimerkkejä laadunhallinnan käytöstä</span><span class="sxs-lookup"><span data-stu-id="29cc7-112">Examples of the use of quality management</span></span>
<span data-ttu-id="29cc7-113">Laadunhallinta on joustavaa ja se voidaan toteuttaa eri tavoin vastaamaan toimitusketjun työvaiheiden tiettyjen tasojen vaatimuksia.</span><span class="sxs-lookup"><span data-stu-id="29cc7-113">Quality management is flexible and can be implemented in various ways to meet the requirements of specific levels of supply chain operations.</span></span> <span data-ttu-id="29cc7-114">Seuraavassa esimerkissä käsitellään näiden ominaisuuksien mahdollisia käyttötapoja:</span><span class="sxs-lookup"><span data-stu-id="29cc7-114">The following examples illustrate possible uses of these features:</span></span>

-   <span data-ttu-id="29cc7-115">Laadunvalvontaprosessin käynnistäminen automaattisesti ennaltamääritettyjen ehtojen perusteella (kun tietyn toimittajan ostotilaus rekisteröidään varastossa).</span><span class="sxs-lookup"><span data-stu-id="29cc7-115">Automatically start a quality control process, based on predefined criteria (upon warehouse registration of a purchase order from a specific vendor).</span></span>
-   <span data-ttu-id="29cc7-116">Varaston esto tarkastuksen aikana, jotta varastoa, jota ei ole hyväksytty, ei käytetä (ostotilausmäärien täysi esto).</span><span class="sxs-lookup"><span data-stu-id="29cc7-116">Block inventory during inspection to prevent non-approved inventory from being used (full blocking of purchase order quantities).</span></span>
-   <span data-ttu-id="29cc7-117">Nimikeotannan käyttö laatuliitoksen osana määritettäessä tarkastettavan fyysisen varaston tämän hetkistä määrää.</span><span class="sxs-lookup"><span data-stu-id="29cc7-117">Use item sampling as part of a quality association to define the amount of current physical inventory that must be inspected.</span></span> <span data-ttu-id="29cc7-118">Otanta voi perustua kiinteisiin määriin, prosenttiosuuteen tai täyteen rekisterikilpeen.</span><span class="sxs-lookup"><span data-stu-id="29cc7-118">Sampling can be based on fixed quantities, a percentage, or full license plate.</span></span>

> [!NOTE]
> <span data-ttu-id="29cc7-119">_Varastoprosessien laadunhallinta_ -ominaisuus laajentaa laadunhallinnan ominaisuuksia.</span><span class="sxs-lookup"><span data-stu-id="29cc7-119">The _Quality management for warehouse processes_ feature extends the capabilities of quality management.</span></span> <span data-ttu-id="29cc7-120">Jos käytät tätä toimintoa, katso kohdasta [Varaston prosessien laadunhallinta](quality-management-for-warehouses-processes.md) esimerkkejä siitä, miten laadunhallinta toimii, kun se otetaan käyttöön.</span><span class="sxs-lookup"><span data-stu-id="29cc7-120">If you are using this feature, then see [Quality management for warehouse processes](quality-management-for-warehouses-processes.md) for examples of how quality management works when it's enabled.</span></span>

-   <span data-ttu-id="29cc7-121">Luo laatutilaukset osittaisille vastaanotoille.</span><span class="sxs-lookup"><span data-stu-id="29cc7-121">Create quality orders for partial receipts.</span></span> <span data-ttu-id="29cc7-122">Tilauksen mukana fyysisesti vastaanotettuun määrään perustuva laatutilaus luodaan valitsemalla **Päivitettyä määrää kohden** -valintaruutu **Nimikeotanta**-lomakkeessa.</span><span class="sxs-lookup"><span data-stu-id="29cc7-122">To create a quality order that is based on the quantity that is physically received with an order, you must select the **Per updated quantity** check box on the **Item sampling** form.</span></span>
-   <span data-ttu-id="29cc7-123">Testin pienimmän, suurimman ja tavoiteltavan arvon sisältävien testityyppien luominen sekä sellaisen määrää ja laatua vertailevan testin suorittaminen, jolla on ennalta määritetyt tarkistustulokset.</span><span class="sxs-lookup"><span data-stu-id="29cc7-123">Create test types that include minimum, maximum, and target test values, and perform qualitative-versus-quantitative testing that has predefined validation results.</span></span>
-   <span data-ttu-id="29cc7-124">Hyväksyttävän laadun tason määrittäminen laadun mittaustoleranssien hallintaa varten.</span><span class="sxs-lookup"><span data-stu-id="29cc7-124">Specify an acceptable quality level (AQL) to control quality measure tolerances.</span></span>
-   <span data-ttu-id="29cc7-125">Tarkastustyövaiheiden edellyttämien resurssien, kuten testausalueen tai testin mittavälineiden, määrittäminen.</span><span class="sxs-lookup"><span data-stu-id="29cc7-125">Specify the resources that an inspection operation requires, such as a test area and test instruments.</span></span>

## <a name="working-with-quality-associations"></a><span data-ttu-id="29cc7-126">Laatuliitosten käsitteleminen</span><span class="sxs-lookup"><span data-stu-id="29cc7-126">Working with quality associations</span></span>
<span data-ttu-id="29cc7-127">Laatuliitosta käyttävä liiketoimintoprosessi voidaan liittää eri lähdeasiakirjoihin, kuten ostotilauksiin, myyntitilauksiin tai tuotantotilauksiin.</span><span class="sxs-lookup"><span data-stu-id="29cc7-127">The business process that uses a quality association can be related to various source documents, such as purchase orders, sales orders, or production orders.</span></span>

<span data-ttu-id="29cc7-128">Jokaisessa laatuliitostietueessa määritetään joukko testejä, hyväksyttävän laadun taso ja otantasuunnitelma, jota käytetään muodostettavissa laatutilauksissa.</span><span class="sxs-lookup"><span data-stu-id="29cc7-128">Each quality association record defines the set of tests, the AQL, and the sampling plan that applies to the quality orders that are generated.</span></span> <span data-ttu-id="29cc7-129">Laatuliitostietue on määritettävä liiketoimintaprosessin jokaiselle muunnokselle.</span><span class="sxs-lookup"><span data-stu-id="29cc7-129">You must define a quality association record for each variation in a business process.</span></span> <span data-ttu-id="29cc7-130">Voit esimerkiksi määrittää laatuliitoksen, joka muodostaa laatutilauksen, kun ostotilauksen tuotteen vastaanotto päivitetään.</span><span class="sxs-lookup"><span data-stu-id="29cc7-130">For example, you can set up a quality association that generates a quality order when a purchase order product receipt is updated.</span></span> <span data-ttu-id="29cc7-131">Toimeenpanosuunnitelma määritysten mukaisesti käynnistävä prosessi voidaan estää, jos laatutilaus on avoinna. Myös seuraavat prosessit, kuten ostotilauksen laskutus, voidaan estää.</span><span class="sxs-lookup"><span data-stu-id="29cc7-131">Depending on the setup of the execution plan, the triggering process itself can be blocked while there is an open quality order, or the next processes, such as purchase order invoicing, can be blocked.</span></span>

<span data-ttu-id="29cc7-132">**Huomautus:** Jos laatutilauksia on avoinna, varastomäärien otto estetään automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="29cc7-132">**Note:** While there are open quality orders, inventory quantities are automatically blocked from being issued.</span></span> <span data-ttu-id="29cc7-133">**Nimikeotanta**-sivun **Täysi esto** -asetuksen mukaan laatu on joko laatutilauksen määrä tai lähdeasiakirjan rivin määrä.</span><span class="sxs-lookup"><span data-stu-id="29cc7-133">Depending on the **Full blocking** setting on the **Item samplings** page, the quantity is either the quantity on the quality order or the quantity on the source document line.</span></span>

<span data-ttu-id="29cc7-134">Tietyn liiketoimintaprosessin laatuliitostietue tunnistaa tapahtuman ja ehdot, joille laatutilaus muodostetaan.</span><span class="sxs-lookup"><span data-stu-id="29cc7-134">For a given business process, the quality association record identifies the event and the conditions that a quality order is generated for.</span></span> <span data-ttu-id="29cc7-135">Ehdot voivat olla joko toimipaikka- tai yrityskohtaisia.</span><span class="sxs-lookup"><span data-stu-id="29cc7-135">The conditions can be specific to either a site or a legal entity.</span></span> <span data-ttu-id="29cc7-136">Tuhoavia testejä sisältävä laatutilaus voidaan muodostaa vain, kun tapahtumalla on käytettävissä oleva varasto.</span><span class="sxs-lookup"><span data-stu-id="29cc7-136">A quality order that involves destructive tests can be generated only when on-hand inventory exists for the event.</span></span>

<span data-ttu-id="29cc7-137">Seuraavassa esimerkeissä käsitellään, miten laatuliitostietue määritetään kunkin liiketoimintaprosessin variaatioille.</span><span class="sxs-lookup"><span data-stu-id="29cc7-137">The following examples illustrate how a quality association record is defined for the variations in each business process.</span></span> <span data-ttu-id="29cc7-138">Seuraavassa taulussa on jokaisen esimerkin yhteenveto laatuliitostietueessa määritetyistä tapahtumista ja ehdoista.</span><span class="sxs-lookup"><span data-stu-id="29cc7-138">For each example, the following table summarizes the events and conditions that are defined by a quality association record.</span></span>

<table>
<tbody>
<tr>
<th><span data-ttu-id="29cc7-139">Viitetyyppi</span><span class="sxs-lookup"><span data-stu-id="29cc7-139">Reference type</span></span></th>
<th><span data-ttu-id="29cc7-140">Tapahtumatyyppi</span><span class="sxs-lookup"><span data-stu-id="29cc7-140">Event type</span></span></th>
<th><span data-ttu-id="29cc7-141">Suoritus</span><span class="sxs-lookup"><span data-stu-id="29cc7-141">Execution</span></span></th>
<th><span data-ttu-id="29cc7-142">Tapahtuman esto</span><span class="sxs-lookup"><span data-stu-id="29cc7-142">Event blocking</span></span></th>
<th><span data-ttu-id="29cc7-143">Tiedostoviite</span><span class="sxs-lookup"><span data-stu-id="29cc7-143">Document reference</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="29cc7-144">Varasto</span><span class="sxs-lookup"><span data-stu-id="29cc7-144">Inventory</span></span></td>
<td><span data-ttu-id="29cc7-145">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="29cc7-145">Not applicable</span></span></td>
<td><span data-ttu-id="29cc7-146">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="29cc7-146">Not applicable</span></span></td>
<td><span data-ttu-id="29cc7-147">Ei mitään</span><span class="sxs-lookup"><span data-stu-id="29cc7-147">None</span></span></td>
<td><span data-ttu-id="29cc7-148">Kaikki</span><span class="sxs-lookup"><span data-stu-id="29cc7-148">All</span></span></td>
</tr>
<tr>
<td rowspan="7"><span data-ttu-id="29cc7-149">Myynti</span><span class="sxs-lookup"><span data-stu-id="29cc7-149">Sales</span></span></td>
<td rowspan="4"><span data-ttu-id="29cc7-150">Keräysprosessi on ajoitettu</span><span class="sxs-lookup"><span data-stu-id="29cc7-150">Picking process is scheduled</span></span></td>
<td rowspan="4"><span data-ttu-id="29cc7-151">Ennen</span><span class="sxs-lookup"><span data-stu-id="29cc7-151">Before</span></span></td>
<td><span data-ttu-id="29cc7-152">Ei mitään</span><span class="sxs-lookup"><span data-stu-id="29cc7-152">None</span></span></td>
<td rowspan="22"><span data-ttu-id="29cc7-153">Tietty tunnus, ryhmä tai vain kaikki</span><span class="sxs-lookup"><span data-stu-id="29cc7-153">Specific ID, Group, or All only</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29cc7-154">Keräysprosessi</span><span class="sxs-lookup"><span data-stu-id="29cc7-154">Picking process</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29cc7-155">Pakkausluettelo</span><span class="sxs-lookup"><span data-stu-id="29cc7-155">Packing slip</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29cc7-156">Lasku</span><span class="sxs-lookup"><span data-stu-id="29cc7-156">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="29cc7-157">Pakkausluettelo</span><span class="sxs-lookup"><span data-stu-id="29cc7-157">Packing slip</span></span></td>
<td rowspan="3"><span data-ttu-id="29cc7-158">Ennen</span><span class="sxs-lookup"><span data-stu-id="29cc7-158">Before</span></span></td>
<td><span data-ttu-id="29cc7-159">Ei mitään</span><span class="sxs-lookup"><span data-stu-id="29cc7-159">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29cc7-160">Pakkausluettelo</span><span class="sxs-lookup"><span data-stu-id="29cc7-160">Packing slip</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29cc7-161">Lasku</span><span class="sxs-lookup"><span data-stu-id="29cc7-161">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="15"><span data-ttu-id="29cc7-162">Osto</span><span class="sxs-lookup"><span data-stu-id="29cc7-162">Purchase</span></span></td>
<td rowspan="7"><span data-ttu-id="29cc7-163">Vastaanottoluettelo</span><span class="sxs-lookup"><span data-stu-id="29cc7-163">Receipt list</span></span></td>
<td rowspan="4"><span data-ttu-id="29cc7-164">Ennen</span><span class="sxs-lookup"><span data-stu-id="29cc7-164">Before</span></span></td>
<td><span data-ttu-id="29cc7-165">Ei mitään</span><span class="sxs-lookup"><span data-stu-id="29cc7-165">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29cc7-166">Vastaanottoluettelo</span><span class="sxs-lookup"><span data-stu-id="29cc7-166">Receipt list</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29cc7-167">Tuotteen vastaanotto</span><span class="sxs-lookup"><span data-stu-id="29cc7-167">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29cc7-168">Lasku</span><span class="sxs-lookup"><span data-stu-id="29cc7-168">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="29cc7-169">Jälkeen</span><span class="sxs-lookup"><span data-stu-id="29cc7-169">After</span></span></td>
<td><span data-ttu-id="29cc7-170">Ei mitään</span><span class="sxs-lookup"><span data-stu-id="29cc7-170">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29cc7-171">Tuotteen vastaanotto</span><span class="sxs-lookup"><span data-stu-id="29cc7-171">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29cc7-172">Lasku</span><span class="sxs-lookup"><span data-stu-id="29cc7-172">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="29cc7-173">Rekisteröinti</span><span class="sxs-lookup"><span data-stu-id="29cc7-173">Registration</span></span></td>
<td rowspan="3"><span data-ttu-id="29cc7-174">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="29cc7-174">Not applicable</span></span></td>
<td><span data-ttu-id="29cc7-175">Ei mitään</span><span class="sxs-lookup"><span data-stu-id="29cc7-175">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29cc7-176">Tuotteen vastaanotto</span><span class="sxs-lookup"><span data-stu-id="29cc7-176">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29cc7-177">Lasku</span><span class="sxs-lookup"><span data-stu-id="29cc7-177">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="29cc7-178">Tuotteen vastaanotto</span><span class="sxs-lookup"><span data-stu-id="29cc7-178">Product receipt</span></span></td>
<td rowspan="3"><span data-ttu-id="29cc7-179">Ennen</span><span class="sxs-lookup"><span data-stu-id="29cc7-179">Before</span></span></td>
<td><span data-ttu-id="29cc7-180">Ei mitään</span><span class="sxs-lookup"><span data-stu-id="29cc7-180">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29cc7-181">Tuotteen vastaanotto</span><span class="sxs-lookup"><span data-stu-id="29cc7-181">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29cc7-182">Lasku</span><span class="sxs-lookup"><span data-stu-id="29cc7-182">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="29cc7-183">Jälkeen</span><span class="sxs-lookup"><span data-stu-id="29cc7-183">After</span></span></td>
<td><span data-ttu-id="29cc7-184">Ei mitään</span><span class="sxs-lookup"><span data-stu-id="29cc7-184">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29cc7-185">Lasku</span><span class="sxs-lookup"><span data-stu-id="29cc7-185">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="8"><span data-ttu-id="29cc7-186">Tuotanto</span><span class="sxs-lookup"><span data-stu-id="29cc7-186">Production</span></span></td>
<td rowspan="3"><span data-ttu-id="29cc7-187">Rekisteröinti</span><span class="sxs-lookup"><span data-stu-id="29cc7-187">Registration</span></span></td>
<td rowspan="3"><span data-ttu-id="29cc7-188">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="29cc7-188">Not applicable</span></span></td>
<td><span data-ttu-id="29cc7-189">Ei mitään</span><span class="sxs-lookup"><span data-stu-id="29cc7-189">None</span></span></td>
<td rowspan="12"><span data-ttu-id="29cc7-190">Kaikki</span><span class="sxs-lookup"><span data-stu-id="29cc7-190">All</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29cc7-191">Ilmoita valmiiksi</span><span class="sxs-lookup"><span data-stu-id="29cc7-191">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29cc7-192">Lopeta</span><span class="sxs-lookup"><span data-stu-id="29cc7-192">End</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="29cc7-193">Ilmoita valmiiksi</span><span class="sxs-lookup"><span data-stu-id="29cc7-193">Report as finished</span></span></td>
<td rowspan="3"><span data-ttu-id="29cc7-194">Ennen</span><span class="sxs-lookup"><span data-stu-id="29cc7-194">Before</span></span></td>
<td><span data-ttu-id="29cc7-195">Ei mitään</span><span class="sxs-lookup"><span data-stu-id="29cc7-195">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29cc7-196">Ilmoita valmiiksi</span><span class="sxs-lookup"><span data-stu-id="29cc7-196">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29cc7-197">Lopeta</span><span class="sxs-lookup"><span data-stu-id="29cc7-197">End</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="29cc7-198">Jälkeen</span><span class="sxs-lookup"><span data-stu-id="29cc7-198">After</span></span></td>
<td><span data-ttu-id="29cc7-199">Ei mitään</span><span class="sxs-lookup"><span data-stu-id="29cc7-199">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29cc7-200">Lopeta</span><span class="sxs-lookup"><span data-stu-id="29cc7-200">End</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="29cc7-201">Karanteeni</span><span class="sxs-lookup"><span data-stu-id="29cc7-201">Quarantine</span></span></td>
<td rowspan="3"><span data-ttu-id="29cc7-202">Ilmoita valmiiksi</span><span class="sxs-lookup"><span data-stu-id="29cc7-202">Report as finished</span></span></td>
<td rowspan="2"><span data-ttu-id="29cc7-203">Ennen</span><span class="sxs-lookup"><span data-stu-id="29cc7-203">Before</span></span></td>
<td><span data-ttu-id="29cc7-204">Ilmoita valmiiksi</span><span class="sxs-lookup"><span data-stu-id="29cc7-204">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29cc7-205">Lopeta</span><span class="sxs-lookup"><span data-stu-id="29cc7-205">End</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29cc7-206">Jälkeen</span><span class="sxs-lookup"><span data-stu-id="29cc7-206">After</span></span></td>
<td><span data-ttu-id="29cc7-207">Lopeta</span><span class="sxs-lookup"><span data-stu-id="29cc7-207">End</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29cc7-208">Lopeta</span><span class="sxs-lookup"><span data-stu-id="29cc7-208">End</span></span></td>
<td><span data-ttu-id="29cc7-209">Ennen</span><span class="sxs-lookup"><span data-stu-id="29cc7-209">Before</span></span></td>
<td><span data-ttu-id="29cc7-210">Lopeta</span><span class="sxs-lookup"><span data-stu-id="29cc7-210">End</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="29cc7-211">Reitityksen työvaihe</span><span class="sxs-lookup"><span data-stu-id="29cc7-211">Route operation</span></span></td>
<td rowspan="3"><span data-ttu-id="29cc7-212">Ilmoita valmiiksi</span><span class="sxs-lookup"><span data-stu-id="29cc7-212">Report as finished</span></span></td>
<td rowspan="2"><span data-ttu-id="29cc7-213">Ennen</span><span class="sxs-lookup"><span data-stu-id="29cc7-213">Before</span></span></td>
<td><span data-ttu-id="29cc7-214">Ei mitään</span><span class="sxs-lookup"><span data-stu-id="29cc7-214">None</span></span></td>
<td rowspan="3"><span data-ttu-id="29cc7-215">Tietty tunnus, ryhmä tai kaikki tai ryhmäkohtainen, ryhmä tai kaikki</span><span class="sxs-lookup"><span data-stu-id="29cc7-215">Specific ID, Group, or All, and Resource specific, Group, or All</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29cc7-216">Ilmoita valmiiksi</span><span class="sxs-lookup"><span data-stu-id="29cc7-216">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29cc7-217">Jälkeen</span><span class="sxs-lookup"><span data-stu-id="29cc7-217">After</span></span></td>
<td><span data-ttu-id="29cc7-218">Ei mitään</span><span class="sxs-lookup"><span data-stu-id="29cc7-218">None</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="29cc7-219">Oheistuotteen tuotanto</span><span class="sxs-lookup"><span data-stu-id="29cc7-219">Co-product production</span></span></td>
<td><span data-ttu-id="29cc7-220">Rekisteröinti</span><span class="sxs-lookup"><span data-stu-id="29cc7-220">Registration</span></span></td>
<td><span data-ttu-id="29cc7-221">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="29cc7-221">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="29cc7-222">Ei mitään</span><span class="sxs-lookup"><span data-stu-id="29cc7-222">None</span></span></td>
<td rowspan="3"><span data-ttu-id="29cc7-223">Kaikki</span><span class="sxs-lookup"><span data-stu-id="29cc7-223">All</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="29cc7-224">Ilmoita valmiiksi</span><span class="sxs-lookup"><span data-stu-id="29cc7-224">Report as finished</span></span></td>
<td><span data-ttu-id="29cc7-225">Ennen</span><span class="sxs-lookup"><span data-stu-id="29cc7-225">Before</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29cc7-226">Jälkeen</span><span class="sxs-lookup"><span data-stu-id="29cc7-226">After</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="29cc7-227">Seuraavassa taulussa on lisätietoja laatutilausten muodostamisesta tietyntyyppisille prosesseille.</span><span class="sxs-lookup"><span data-stu-id="29cc7-227">The following table provides more information about how quality orders can be generated for specific types of processes.</span></span>
<div class="tableSection">

<table>
<tbody>
<tr>
<th><span data-ttu-id="29cc7-228">Prosessin tyyppi</span><span class="sxs-lookup"><span data-stu-id="29cc7-228">Type of process</span></span></th>
<th><span data-ttu-id="29cc7-229">Laatutilausten automaattinen luontiajankohta</span><span class="sxs-lookup"><span data-stu-id="29cc7-229">When quality orders can be automatically generated</span></span></th>
<th><span data-ttu-id="29cc7-230">Laatutilausten luontiajankohta, jos tuhoava testaus pakollinen</span><span class="sxs-lookup"><span data-stu-id="29cc7-230">When quality orders can be generated if destructive testing is required</span></span></th>
<th><span data-ttu-id="29cc7-231">Ehdon tiedot</span><span class="sxs-lookup"><span data-stu-id="29cc7-231">Condition information</span></span></th>
<th><span data-ttu-id="29cc7-232">Manuaalisen luonnin tiedot</span><span class="sxs-lookup"><span data-stu-id="29cc7-232">Manual generation information</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="29cc7-233">Ostotilaus</span><span class="sxs-lookup"><span data-stu-id="29cc7-233">Purchase order</span></span></td>
<td><span data-ttu-id="29cc7-234">Ennen kuin vastaanotetun materiaalin vastaanottoluettelo tai tuotteen vastaanotto on kirjattu tai sen jälkeen</span><span class="sxs-lookup"><span data-stu-id="29cc7-234">Before or after a receipts list or product receipt for the material that is received is posted</span></span></td>
<td><span data-ttu-id="29cc7-235">Vastaanotetun materiaalin tuotteen vastaanoton kirjauksen jälkeen, koska materiaalin on oltava käytettävissä tuhoavaa testausta varten</span><span class="sxs-lookup"><span data-stu-id="29cc7-235">After the product receipt for the material that is received is posted, because the material must be available for destructive testing</span></span></td>
<td><span data-ttu-id="29cc7-236">Laatutilausvaatimus voi liittyä toimipaikkaan, nimikkeeseen tai toimittajaan tai näiden ehtojen yhdistelmään.</span><span class="sxs-lookup"><span data-stu-id="29cc7-236">The requirement for a quality order can reflect a particular site, item, or vendor, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="29cc7-237">Manuaalisesti luotu ostotilaukseen viittaava laatutilaus voi käyttää laatuliitostietueen tietoja, kuten testin otantasuunnitelmaa.</span><span class="sxs-lookup"><span data-stu-id="29cc7-237">A manually generated quality order that refers to a purchase order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29cc7-238">Karanteenitilaus</span><span class="sxs-lookup"><span data-stu-id="29cc7-238">Quarantine order</span></span></td>
<td><span data-ttu-id="29cc7-239">Ennen karanteenitilauksen ilmoittamista valmiiksi tai päättyneeksi tai sen jälkeen</span><span class="sxs-lookup"><span data-stu-id="29cc7-239">Before or after the quarantine order is reported as finished or ended</span></span></td>
<td><span data-ttu-id="29cc7-240">Tuhoavia testejä edellyttäviä laatutilauksia ei voi luoda.</span><span class="sxs-lookup"><span data-stu-id="29cc7-240">Quality orders that require destructive tests can&#39;t be generated.</span></span> <span data-ttu-id="29cc7-241">Karanteenitilaustoiminnon oletetaan käsittelevän tuhottavan materiaalin käsittelyn.</span><span class="sxs-lookup"><span data-stu-id="29cc7-241">It&#39;s assumed that the quarantine order functionality handles the disposition of the material that is destroyed.</span></span></td>
<td><span data-ttu-id="29cc7-242">Laatutilausvaatimus voi liittyä toimipaikkaan, nimikkeeseen tai toimittajaan tai näiden ehtojen yhdistelmään.</span><span class="sxs-lookup"><span data-stu-id="29cc7-242">The requirement for a quality order can reflect a particular site, item, or vendor, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="29cc7-243">Manuaalisesti luotu ostotilaukseen viittaava karanteenitilaus voi käyttää laatuliitostietueen tietoja, kuten testin otantasuunnitelmaa.</span><span class="sxs-lookup"><span data-stu-id="29cc7-243">A manually generated quality order that refers to a quarantine order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29cc7-244">Myyntitilaus</span><span class="sxs-lookup"><span data-stu-id="29cc7-244">Sales order</span></span></td>
<td><span data-ttu-id="29cc7-245">Ennen lähettävien nimikkeiden ajoitettua keräysprosessia tai pakkausluettelon päivitystä</span><span class="sxs-lookup"><span data-stu-id="29cc7-245">Before a scheduled picking process or packing slip update for the items that are being shipped</span></span></td>
<td><span data-ttu-id="29cc7-246">Kaikissa vaiheissa</span><span class="sxs-lookup"><span data-stu-id="29cc7-246">At any step</span></span></td>
<td><span data-ttu-id="29cc7-247">Laatutilausvaatimus voi liittyä toimipaikkaan, nimikkeeseen tai asiakkaaseen tai näiden ehtojen yhdistelmään.</span><span class="sxs-lookup"><span data-stu-id="29cc7-247">The requirement for a quality order can reflect a particular site, item, or customer, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="29cc7-248">Manuaalisesti luotu myyntitilaukseen viittaava laatutilaus voi käyttää laatuliitostietueen tietoja, kuten testin otantasuunnitelmaa.</span><span class="sxs-lookup"><span data-stu-id="29cc7-248">A manually generated quality order that refers to a sales order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29cc7-249">Tuotantotilaus</span><span class="sxs-lookup"><span data-stu-id="29cc7-249">Production order</span></span></td>
<td><span data-ttu-id="29cc7-250">Ennen tuotantotilauksen valmiiksi raportointia tai sen jälkeen</span><span class="sxs-lookup"><span data-stu-id="29cc7-250">Before or after the finished quantity for the production order is reported</span></span></td>
<td><span data-ttu-id="29cc7-251">Tuotantotilauksen valmiiksi raportoinnin jälkeen</span><span class="sxs-lookup"><span data-stu-id="29cc7-251">After the finished quantity for the production order is reported</span></span></td>
<td><span data-ttu-id="29cc7-252">Laatutilausvaatimus voi liittyä toimipaikkaan tai nimikkeeseen tai näiden ehtojen yhdistelmään.</span><span class="sxs-lookup"><span data-stu-id="29cc7-252">The requirement for a quality order can reflect a particular site or item, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="29cc7-253">Manuaalisesti luotu tuotantotilaukseen viittaava laatutilaus voi käyttää laatuliitostietueen tietoja, kuten testin otantasuunnitelmaa.</span><span class="sxs-lookup"><span data-stu-id="29cc7-253">A manually generated quality order that refers to a production order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29cc7-254">Tuotantotilaus, jossa on reitityksen työvaihe</span><span class="sxs-lookup"><span data-stu-id="29cc7-254">Production order that has a route operation</span></span></td>
<td><span data-ttu-id="29cc7-255">Ennen työvaiheen raportin valmistumista tai sen jälkeen</span><span class="sxs-lookup"><span data-stu-id="29cc7-255">Before or after the report is finished for an operation</span></span></td>
<td><span data-ttu-id="29cc7-256">Viimeisen työvaiheen tuotannon valmiiksi raportoinnin jälkeen</span><span class="sxs-lookup"><span data-stu-id="29cc7-256">After the reporting production is finished for the last operation</span></span></td>
<td><span data-ttu-id="29cc7-257">Laatutilausvaatimus voi liittyä toimipaikkaan, nimikkeeseen tai operatiiviseen resurssiin tai näiden ehtojen yhdistelmään.</span><span class="sxs-lookup"><span data-stu-id="29cc7-257">The requirement for a quality order can reflect a particular, site, item, or operations resource, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="29cc7-258">Manuaalisesti luotu reitityksen työvaiheeseen viittaava laatutilaus voi käyttää laatuliitostietueen tietoja, kuten testin otantasuunnitelmaa.</span><span class="sxs-lookup"><span data-stu-id="29cc7-258">A manually generated quality order that refers to a route operation can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29cc7-259">Varasto</span><span class="sxs-lookup"><span data-stu-id="29cc7-259">Inventory</span></span></td>
<td><span data-ttu-id="29cc7-260">Laatutilausta ei voi luoda automaattisesti varastokirjauskansion tapahtumalle eikä siirtotilaustapahtumille.</span><span class="sxs-lookup"><span data-stu-id="29cc7-260">A quality order cannot be automatically generated for a transaction in an inventory journal or for transfer order transactions.</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="29cc7-261">Laatutilaus on luotava manuaalisesti nimikkeen varastomäärälle.</span><span class="sxs-lookup"><span data-stu-id="29cc7-261">A quality order must be created manually for an item&#39;s inventory quantity.</span></span> <span data-ttu-id="29cc7-262">Fyysistä käytettävissä olevaa varastoa edellytetään.</span><span class="sxs-lookup"><span data-stu-id="29cc7-262">Physical on-hand inventory is required.</span></span></td>
</tr>
</tbody>
</table>

## <a name="quality-order-auto-generation-examples"></a><span data-ttu-id="29cc7-263">Laatutilauksen automaattisen luonnin esimerkkejä</span><span class="sxs-lookup"><span data-stu-id="29cc7-263">Quality order auto-generation examples</span></span>

### <a name="purchasing"></a><span data-ttu-id="29cc7-264">Osto</span><span class="sxs-lookup"><span data-stu-id="29cc7-264">Purchasing</span></span>

<span data-ttu-id="29cc7-265">Jos asetat ostoissa **Tapahtumatyyppi**-kentän arvoksi **Tuotteen vastaanotto** ja **Suoritus**-kentän arvoksi **Jälkeen** **Laatuliitokset**-sivulla, saat seuraavat tulokset:</span><span class="sxs-lookup"><span data-stu-id="29cc7-265">In purchasing, if you set the **Event type** field to **Product receipt** and the **Execution** field to **After** on the **Quality associations** page, you get the following results:</span></span> 

- <span data-ttu-id="29cc7-266">Jos **Päivitettyä määrää kohden** -asetuksen arvoksi määritetään **Kyllä**, laatutilaus luodaan jokaista vastaanottoa varten ostotilauksen perusteella, jolloin otetaan huomioon vastaanotettu määrä sekä nimikeotannan asetukset.</span><span class="sxs-lookup"><span data-stu-id="29cc7-266">If the **Per updated quantity** option is set to **Yes**, a quality order is generated for every receipt against the purchase order, based on the received quantity and settings in the item sampling.</span></span> <span data-ttu-id="29cc7-267">Joka kerta, kun määrä vastaanotetaan ostotilauksen perusteella, luodaaan uusia laatutilauksia juuri saadun määrän perusteella.</span><span class="sxs-lookup"><span data-stu-id="29cc7-267">Every time that a quantity is received against the purchase order, new quality orders are generated based on the newly received quantity.</span></span>
- <span data-ttu-id="29cc7-268">Jos **Päivitettyä määrää kohden** -asetuksen arvoksi määritetään **Ei**, laatutilaus luodaan ensimmäistä vastaanottoa varten ostotilauksen perusteella, jolloin otetaan huomioon vastaanotettu määrä.</span><span class="sxs-lookup"><span data-stu-id="29cc7-268">If the **Per updated quantity** option is set to **No**, a quality order is generated for the first receipt against the purchase order, based on the received quantity.</span></span> <span data-ttu-id="29cc7-269">Lisäksi jäljelle jäävän määrän perusteella luodaan seurantadimensioiden mukaan vähintään yksi laatutilaus.</span><span class="sxs-lookup"><span data-stu-id="29cc7-269">Additionally, one or more quality orders are created based on the remaining quantity, depending on the tracking dimensions.</span></span> <span data-ttu-id="29cc7-270">Laatutilauksia ei luoda ostotilauksen perusteella seuraavien vastaanottojen osalta.</span><span class="sxs-lookup"><span data-stu-id="29cc7-270">Quality orders aren't generated for subsequent receipts against the purchase order.</span></span>

### <a name="production"></a><span data-ttu-id="29cc7-271">Tuotantoympäristö</span><span class="sxs-lookup"><span data-stu-id="29cc7-271">Production</span></span>

<span data-ttu-id="29cc7-272">Jos asetat tuotannossa **Tapahtumatyyppi**-kentän arvoksi **Ilmoita valmiiksi** ja **Suoritus**-kentän arvoksi **Jälkeen** **Laatuliitokset**-sivulla, saat seuraavat tulokset:</span><span class="sxs-lookup"><span data-stu-id="29cc7-272">In production, if you set the **Event type** field to **Report as finished** and the **Execution** field to **After** on the **Quality associations** page, you get the following results:</span></span>

- <span data-ttu-id="29cc7-273">Jos **Päivitettyä määrää kohden** -asetuksen arvoksi määritetään **Kyllä**, laatutilaus luodaan jokaisen valmiin määrän ja nimikeotannan asetusten perusteella.</span><span class="sxs-lookup"><span data-stu-id="29cc7-273">If the **Per updated quantity** option is set to **Yes**, a quality order is generated based on every finished quantity and settings in the item sampling.</span></span> <span data-ttu-id="29cc7-274">Joka kerta, kun määrä ilmoitetaan valmiiksi tuotantotilauksen perusteella, luodaaan uusia laatutilauksia juuri valmiiksi saadun määrän perusteella.</span><span class="sxs-lookup"><span data-stu-id="29cc7-274">Every time that a quantity is reported as finished against the production order, new quality orders are generated based on newly finished quantity.</span></span> <span data-ttu-id="29cc7-275">Tämä luontilogiikka on yhdenmukainen oston kanssa.</span><span class="sxs-lookup"><span data-stu-id="29cc7-275">This generation logic is consistent with purchasing.</span></span>
- <span data-ttu-id="29cc7-276">Jos **Päivitettyä määrää kohden** -asetuksen arvoksi määritetään **Ei**, laatutilaus luodaan valmiiksi saadun määrän perusteella ensimmäisellä kerralla, kun määrä ilmoitetaan valmiiksi.</span><span class="sxs-lookup"><span data-stu-id="29cc7-276">If the **Per updated quantity** option is set to **No**, a quality order is generated the first time that a quantity is reported as finished, based on the finished quantity.</span></span> <span data-ttu-id="29cc7-277">Lisäksi jäljelle jäävän määrän perusteella luodaan nimikeotannan seurantadimensioiden mukaan vähintään yksi laatutilaus.</span><span class="sxs-lookup"><span data-stu-id="29cc7-277">Additionally, one or more quality orders are created based on the remaining quantity, depending on the tracking dimensions of the item sampling.</span></span> <span data-ttu-id="29cc7-278">Seuraaville valmiille määrille ei luoda laatutilauksia.</span><span class="sxs-lookup"><span data-stu-id="29cc7-278">Quality orders aren't generated for subsequent finished quantities.</span></span>

<table>
<tbody>
<tr>
<th><span data-ttu-id="29cc7-279">Laatumääritys</span><span class="sxs-lookup"><span data-stu-id="29cc7-279">Quality specification</span></span></th>
<th><span data-ttu-id="29cc7-280">Päivitettyä määrää kohden</span><span class="sxs-lookup"><span data-stu-id="29cc7-280">Per updated quantity</span></span></th>
<th><span data-ttu-id="29cc7-281">Seurantadimension mukaan</span><span class="sxs-lookup"><span data-stu-id="29cc7-281">Per tracking dimension</span></span></th>
<th><span data-ttu-id="29cc7-282">Tulos</span><span class="sxs-lookup"><span data-stu-id="29cc7-282">Result</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="29cc7-283">Prosenttiosuus: 10 %</span><span class="sxs-lookup"><span data-stu-id="29cc7-283">Percentage: 10%</span></span></td>
<td><span data-ttu-id="29cc7-284">Kyllä</span><span class="sxs-lookup"><span data-stu-id="29cc7-284">Yes</span></span></td>
<td>
<p><span data-ttu-id="29cc7-285">Eränumero: Ei</span><span class="sxs-lookup"><span data-stu-id="29cc7-285">Batch number: No</span></span></p>
<p><span data-ttu-id="29cc7-286">Sarjanumero: Ei</span><span class="sxs-lookup"><span data-stu-id="29cc7-286">Serial number: No</span></span></p>
</td>
<td>
<p><span data-ttu-id="29cc7-287">Tilausmäärä: 100</span><span class="sxs-lookup"><span data-stu-id="29cc7-287">Order quantity: 100</span></span></p>
<ol>
<li><span data-ttu-id="29cc7-288">Ilmoita valmiiksi 30:n osalta</span><span class="sxs-lookup"><span data-stu-id="29cc7-288">Report as finished for 30</span></span>
<ul>
<li><span data-ttu-id="29cc7-289">Laatutilaus #1 määrälle 3 (10 prosenttia 30:stä)</span><span class="sxs-lookup"><span data-stu-id="29cc7-289">Quality order #1 for 3 (10% of 30)</span></span></li>
</ul>
</li>
<li><span data-ttu-id="29cc7-290">Ilmoita valmiiksi 70:n osalta</span><span class="sxs-lookup"><span data-stu-id="29cc7-290">Report as finished for 70</span></span>
<ul>
<li><span data-ttu-id="29cc7-291">Laatutilaus #2 määrälle 7 (10 % jäljellä olevasta tilausmäärästä eli 70:stä)</span><span class="sxs-lookup"><span data-stu-id="29cc7-291">Quality order #2 for 7 (10% of the remaining order quantity, which equals 70 in this case)</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="29cc7-292">Kiinteä määrä: 1</span><span class="sxs-lookup"><span data-stu-id="29cc7-292">Fixed quantity: 1</span></span></td>
<td><span data-ttu-id="29cc7-293">Ei</span><span class="sxs-lookup"><span data-stu-id="29cc7-293">No</span></span></td>
<td>
<p><span data-ttu-id="29cc7-294">Eränumero: Ei</span><span class="sxs-lookup"><span data-stu-id="29cc7-294">Batch number: No</span></span></p>
<p><span data-ttu-id="29cc7-295">Sarjanumero: Ei</span><span class="sxs-lookup"><span data-stu-id="29cc7-295">Serial number: No</span></span></p>
</td>
<td><span data-ttu-id="29cc7-296">Tilausmäärä: 100</span><span class="sxs-lookup"><span data-stu-id="29cc7-296">Order quantity: 100</span></span>
<ol>
<li><span data-ttu-id="29cc7-297">Ilmoita valmiiksi 30:n osalta</span><span class="sxs-lookup"><span data-stu-id="29cc7-297">Report as finished for 30</span></span>
<ul>
<li><span data-ttu-id="29cc7-298">Laatutilaus #1 määrälle 1 (ensimmäiselle valmiiksi ilmoitetulle määrälle, jolla on kiinteä arvo 1)</span><span class="sxs-lookup"><span data-stu-id="29cc7-298">Quality order #1 for 1 (for the first reported-as-finished quantity, which has a fixed value of 1)</span></span></li>
<li><span data-ttu-id="29cc7-299">Laatutilaus #2 määrälle 1 (jäljelle olevalle määrälle, jolla on edelleen kiinteä arvo 1)</span><span class="sxs-lookup"><span data-stu-id="29cc7-299">Quality order #2 for 1 (for the remaining quantity, which still has a fixed value of 1)</span></span></li>
</ul>
</li>
<li><span data-ttu-id="29cc7-300">Ilmoita valmiiksi 10:n osalta</span><span class="sxs-lookup"><span data-stu-id="29cc7-300">Report as finished for 10</span></span>
<ul>
<li><span data-ttu-id="29cc7-301">Laatutilauksia ei luota.</span><span class="sxs-lookup"><span data-stu-id="29cc7-301">No quality orders are created.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="29cc7-302">Ilmoita valmiiksi 60:n osalta</span><span class="sxs-lookup"><span data-stu-id="29cc7-302">Report as finished for 60</span></span>
<ul>
<li><span data-ttu-id="29cc7-303">Laatutilauksia ei luota.</span><span class="sxs-lookup"><span data-stu-id="29cc7-303">No quality orders are created.</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="29cc7-304">Kiinteä määrä: 1</span><span class="sxs-lookup"><span data-stu-id="29cc7-304">Fixed quantity: 1</span></span></td>
<td><span data-ttu-id="29cc7-305">Kyllä</span><span class="sxs-lookup"><span data-stu-id="29cc7-305">Yes</span></span></td>
<td>
<p><span data-ttu-id="29cc7-306">Eränumero: Kyllä</span><span class="sxs-lookup"><span data-stu-id="29cc7-306">Batch number: Yes</span></span></p>
<p><span data-ttu-id="29cc7-307">Sarjanumero: Kyllä</span><span class="sxs-lookup"><span data-stu-id="29cc7-307">Serial number: Yes</span></span></p>
</td>
<td>
<p><span data-ttu-id="29cc7-308">Tilausmäärä: 10</span><span class="sxs-lookup"><span data-stu-id="29cc7-308">Order quantity: 10</span></span></p>
<ol>
<li><span data-ttu-id="29cc7-309">Ilmoita valmiiksi 3:n osalta: 1 erässä #b1, #s1; 1 erässä #b2, #s2; ja 1 erässä #b3, #s3</span><span class="sxs-lookup"><span data-stu-id="29cc7-309">Report as finished for 3: 1 for #b1, #s1; 1 for #b2, #s2; and 1 for #b3, #s3</span></span>
<ul>
<li><span data-ttu-id="29cc7-310">Laatutilaus #1 määrälle 1 erästä #b1, sarjanumero #s1</span><span class="sxs-lookup"><span data-stu-id="29cc7-310">Quality order #1 for 1 of batch #b1, serial #s1</span></span></li>
<li><span data-ttu-id="29cc7-311">Laatutilaus #2 määrälle 1 erästä #b2, sarjanumero #s2</span><span class="sxs-lookup"><span data-stu-id="29cc7-311">Quality order #2 for 1 of batch #b2, serial #s2</span></span></li>
<li><span data-ttu-id="29cc7-312">Laatutilaus #3 määrälle 1 erästä #b3, sarjanumero #s3</span><span class="sxs-lookup"><span data-stu-id="29cc7-312">Quality order #3 for 1 of batch #b3, serial #s3</span></span></li>
</ul>
</li>
<li><span data-ttu-id="29cc7-313">Ilmoita valmiiksi 2:n osalta: 1 erässä #b4, #s4; ja 1 erässä #b5, #s5</span><span class="sxs-lookup"><span data-stu-id="29cc7-313">Report as finished for 2: 1 for #b4, #s4; and 1 for #b5, #s5</span></span>
<ul>
<li><span data-ttu-id="29cc7-314">Laatutilaus #4 määrälle 1 erästä #b4, sarjanumero #s4</span><span class="sxs-lookup"><span data-stu-id="29cc7-314">Quality order #4 for 1 of batch #b4, serial #s4</span></span></li>
<li><span data-ttu-id="29cc7-315">Laatutilaus #5 määrälle 1 erästä #b5, sarjanumero #s5</span><span class="sxs-lookup"><span data-stu-id="29cc7-315">Quality order #5 for 1 of batch #b5, serial #s5</span></span></li>
</ul>
</li>
</ol>
<p><span data-ttu-id="29cc7-316"><strong>Huomautus:</strong> Erää voidaan käyttää uudelleen.</span><span class="sxs-lookup"><span data-stu-id="29cc7-316"><strong>Note:</strong> The batch can be reused.</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="29cc7-317">Kiinteä määrä: 2</span><span class="sxs-lookup"><span data-stu-id="29cc7-317">Fixed quantity: 2</span></span></td>
<td><span data-ttu-id="29cc7-318">Ei</span><span class="sxs-lookup"><span data-stu-id="29cc7-318">No</span></span></td>
<td>
<p><span data-ttu-id="29cc7-319">Eränumero: Kyllä</span><span class="sxs-lookup"><span data-stu-id="29cc7-319">Batch number: Yes</span></span></p>
<p><span data-ttu-id="29cc7-320">Sarjanumero: Kyllä</span><span class="sxs-lookup"><span data-stu-id="29cc7-320">Serial number: Yes</span></span></p>
</td>
<td>
<p><span data-ttu-id="29cc7-321">Tilausmäärä: 10</span><span class="sxs-lookup"><span data-stu-id="29cc7-321">Order quantity: 10</span></span></p>
<ol>
<li><span data-ttu-id="29cc7-322">Ilmoita valmiiksi 4:n osalta: 1 erässä #b1, #s1; 1 erässä #b2, #s2; 1 erässä #b3, #s3 ja 1 erässä #b4, #s4</span><span class="sxs-lookup"><span data-stu-id="29cc7-322">Report as finished for 4: 1 for #b1, #s1; 1 for #b2, #s2; 1 for #b3, #s3; and 1 for #b4, #s4</span></span>
<ul>
<li><span data-ttu-id="29cc7-323">Laatutilaus #1 määrälle 1 erästä #b1, sarjanumero #s1</span><span class="sxs-lookup"><span data-stu-id="29cc7-323">Quality order #1 for 1 of batch #b1, serial #s1</span></span></li>
<li><span data-ttu-id="29cc7-324">Laatutilaus #2 määrälle 1 erästä #b2, sarjanumero #s2</span><span class="sxs-lookup"><span data-stu-id="29cc7-324">Quality order #2 for 1 of batch #b2, serial #s2</span></span></li>
<li><span data-ttu-id="29cc7-325">Laatutilaus #3 määrälle 1 erästä #b3, sarjanumero #s3</span><span class="sxs-lookup"><span data-stu-id="29cc7-325">Quality order #3 for 1 of batch #b3, serial #s3</span></span></li>
<li><span data-ttu-id="29cc7-326">Laatutilaus #4 määrälle 1 erästä #b4, sarjanumero #s4</span><span class="sxs-lookup"><span data-stu-id="29cc7-326">Quality order #4 for 1 of batch #b4, serial #s4</span></span></li>
</ul>
<ul>
<li><span data-ttu-id="29cc7-327">Laatutilaus #5 määrälle 2 ilman viittausta erä- ja sarjanumeroon</span><span class="sxs-lookup"><span data-stu-id="29cc7-327">Quality order #5 for 2, without a reference to a batch and a serial number</span></span></li>
</ul>
</li>
<li><span data-ttu-id="29cc7-328">Ilmoita valmiiksi 6:n osalta: 1 erässä #b5, #s5; 1 erässä #b6, #s6; 1 erässä #b7, #s7; 1 erässä #b8, #s8; 1 erässä #b9, #s9; ja 1 erässä #b10, #s10</span><span class="sxs-lookup"><span data-stu-id="29cc7-328">Report as finished for 6: 1 for #b5, #s5; 1 for #b6, #s6; 1 for #b7, #s7; 1 for #b8, #s8; 1 for #b9, #s9; and 1 for #b10, #s10</span></span>
<ul>
<li><span data-ttu-id="29cc7-329">Laatutilauksia ei luota.</span><span class="sxs-lookup"><span data-stu-id="29cc7-329">No quality orders are created.</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="29cc7-330">*Varastoprosessien laadunhallinta* -ominaisuus lisää laatutilausten käsittelytoiminnot tuotannoille, joiden **Tapahtumatyyppi** on *Ilmoita valmiiksi* ja **Suorittamiseksi** on määritetty *Jälkeen*, sekä ostoille, joiden **Tapahtumatyyppi** on määritetty *Rekisteröimiseksi*.</span><span class="sxs-lookup"><span data-stu-id="29cc7-330">The *Quality management for warehouse processes* feature adds capabilities for quality order processing for production with **Event type** set to *Report as finished* and **Execution** set to *After*, and for purchases with **Event type** set to *Registration*.</span></span> <span data-ttu-id="29cc7-331">Lue lisätietoja kohdasta [Laadunhallinta varastoprosesseja varten](quality-management-for-warehouses-processes.md).</span><span class="sxs-lookup"><span data-stu-id="29cc7-331">For details, see [Quality management for warehouse processes](quality-management-for-warehouses-processes.md).</span></span>

## <a name="quality-management-pages"></a><span data-ttu-id="29cc7-332">Laadunhallinnan sivut</span><span class="sxs-lookup"><span data-stu-id="29cc7-332">Quality management pages</span></span>
<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="29cc7-333">Sivu</span><span class="sxs-lookup"><span data-stu-id="29cc7-333">Page</span></span></th>
<th><span data-ttu-id="29cc7-334">kuvaus</span><span class="sxs-lookup"><span data-stu-id="29cc7-334">Description</span></span></th>
<th><span data-ttu-id="29cc7-335">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="29cc7-335">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="29cc7-336">Laatuliitokset</span><span class="sxs-lookup"><span data-stu-id="29cc7-336">Quality associations</span></span></td>
<td><span data-ttu-id="29cc7-337">Katso artikkelin edelliset osat.</span><span class="sxs-lookup"><span data-stu-id="29cc7-337">See the previous sections of this article.</span></span></td>
<td><span data-ttu-id="29cc7-338">Laatuliitos määrittää kaikki seuraavat muodostettavan laatutilauksen tiedot:</span><span class="sxs-lookup"><span data-stu-id="29cc7-338">A quality association defines all the following information for a quality order that is generated:</span></span>
<ul>
<li><span data-ttu-id="29cc7-339">Tapahtuma</span><span class="sxs-lookup"><span data-stu-id="29cc7-339">The transaction event</span></span></li>
<li><span data-ttu-id="29cc7-340">Nimikkeissä suoritettavat testit</span><span class="sxs-lookup"><span data-stu-id="29cc7-340">The set of tests that must be performed on the items</span></span></li>
<li><span data-ttu-id="29cc7-341">Hyväksyttävän laadun taso</span><span class="sxs-lookup"><span data-stu-id="29cc7-341">The AQL</span></span></li>
<li><span data-ttu-id="29cc7-342">Otantasuunnitelma</span><span class="sxs-lookup"><span data-stu-id="29cc7-342">The sampling plan</span></span></li>
</ul>
<span data-ttu-id="29cc7-343">Laatuliitos on määritettävä kutakin sellaista liiketoimintaprosessin muutosta varten, joka edellyttää automaattista laatutilausten luontia.</span><span class="sxs-lookup"><span data-stu-id="29cc7-343">You must define a quality association for each variation in a business process that requires automatic generation of quality orders.</span></span> <span data-ttu-id="29cc7-344">Laatutilaus voidaan esimerkiksi muodostaa ostotilausten, karanteenitilausten, myyntitilausten ja tuotantotilausten liiketoimintaprosesseille.</span><span class="sxs-lookup"><span data-stu-id="29cc7-344">For example, a quality order can be generated in the business processes for purchase orders, quarantine orders, sales orders, and production orders.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="29cc7-345">Testit</span><span class="sxs-lookup"><span data-stu-id="29cc7-345">Tests</span></span></td>
<td><span data-ttu-id="29cc7-346">Voit määrittää ja tarkastella tällä sivulla yksittäisiä testejä, joiden mukaan määräytyy, ovatko tuotteet laatuvaatimusten mukaisia.</span><span class="sxs-lookup"><span data-stu-id="29cc7-346">Use this page to define and view the individual tests that determine whether your products meet quality specifications.</span></span> <span data-ttu-id="29cc7-347">Voit määrittää testiryhmälle vähintään yhden yksittäisen testin.</span><span class="sxs-lookup"><span data-stu-id="29cc7-347">You can assign one or more individual tests to a test group.</span></span> <span data-ttu-id="29cc7-348">Siinä tapauksessa määrität myös testikohtaiset tiedot, kuten hyväksyttävät mitta-arvot.</span><span class="sxs-lookup"><span data-stu-id="29cc7-348">In this case, you also specify test-specific information, such as the acceptable measurement values.</span></span> <span data-ttu-id="29cc7-349">Mitta-arvoja käytetään määrällisissä testeissä, kun taas laadullisissa testeissä käytetään testimuuttujia.</span><span class="sxs-lookup"><span data-stu-id="29cc7-349">Measurement values are used for quantitative tests, and test variables are used for qualitative tests.</span></span>
<ul>
<li><span data-ttu-id="29cc7-350">Määrällisen testin testityyppi on <strong>Kokonaisluku</strong> tai <strong>Nimellinen</strong>. Lisäksi siihen on määritetty mittayksikkö.</span><span class="sxs-lookup"><span data-stu-id="29cc7-350">A quantitative test has a test type of <strong>Integer</strong> or <strong>Fraction</strong>, and also has a designated unit of measure.</span></span> <span data-ttu-id="29cc7-351">Laatumääritykset ja testitulokset ilmaistaan numeroina.</span><span class="sxs-lookup"><span data-stu-id="29cc7-351">Quality specifications and test results are expressed as numbers.</span></span></li>
<li><span data-ttu-id="29cc7-352">Laadullisen testin testityyppi on <strong>Vaihtoehto</strong>.</span><span class="sxs-lookup"><span data-stu-id="29cc7-352">A qualitative test has a test type of <strong>Option</strong>.</span></span> <span data-ttu-id="29cc7-353">Laadullista testiä varten tarvitaan lisätietoja mitattavasta testimuuttujasta ja sen numeroiduista vaihtoehdoista.</span><span class="sxs-lookup"><span data-stu-id="29cc7-353">Qualitative tests require additional information about the test variable that is being measured and its enumerated options.</span></span> <span data-ttu-id="29cc7-354">Laatumääritykset ja testitulokset ilmaistaan tuloksen perusteella.</span><span class="sxs-lookup"><span data-stu-id="29cc7-354">Quality specifications and test results are expressed according to an outcome.</span></span></li>
</ul></td>
<td><span data-ttu-id="29cc7-355">Teollisuusyritys suorittaa ostamalleen materiaalille kaksi testiä: materiaalin laatua koskevan määrällisen testin ja pakkausvahinkoja koskevan laadullisen testin.</span><span class="sxs-lookup"><span data-stu-id="29cc7-355">A manufacturing company performs two tests on purchased material: a quantitative test about material quality and a qualitative test about packaging damage.</span></span> <span data-ttu-id="29cc7-356">Yritys määrittää laadullisen testin lisätiedoiksi testimuuttujan (vioittunut pakkaus) ja sen mahdolliset tulokset.</span><span class="sxs-lookup"><span data-stu-id="29cc7-356">The company defines additional information about the qualitative test to identify the test variable (damaged packaging) and its outcomes.</span></span> <span data-ttu-id="29cc7-357">Yritys määrittää <strong>Testiryhmät</strong>-sivulla kaksi testiä testiryhmään. Lisäksi testikohtaiset tiedot määritetään.</span><span class="sxs-lookup"><span data-stu-id="29cc7-357">The company uses the <strong>Test groups</strong> page to assign the two tests to a test group and to specify the test-specific information.</span></span> <span data-ttu-id="29cc7-358">Testiryhmä määritetään laatutilaukseen, jotta yritys voi raportoida näiden kahden testin testitulokset.</span><span class="sxs-lookup"><span data-stu-id="29cc7-358">The test group is assigned to a quality order, so that the company can report test results for the two tests.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="29cc7-359">Testiryhmät</span><span class="sxs-lookup"><span data-stu-id="29cc7-359">Test groups</span></span></td>
<td><span data-ttu-id="29cc7-360">Voit määrittää, muokata ja tarkastella tällä sivulla testiryhmiä ja testiryhmälle määritettyjä yksittäisiä testejä.</span><span class="sxs-lookup"><span data-stu-id="29cc7-360">Use this page to set up, edit, and view test groups and the individual tests that are assigned to a test group.</span></span> <span data-ttu-id="29cc7-361">Yläruudussa näkyvät testiryhmät, ja alaruudussa näkyvät valitulle testiryhmälle määritetyt testit.</span><span class="sxs-lookup"><span data-stu-id="29cc7-361">The upper pane displays test groups, and the lower pane displays the tests that are assigned to a selected test group.</span></span> <span data-ttu-id="29cc7-362">Voit määrittää testiryhmälle useita käytäntöjä, kuten otantasuunnitelman, hyväksytyn laatutason ja tuhoavan testin tarpeen.</span><span class="sxs-lookup"><span data-stu-id="29cc7-362">You assign several policies to a test group, such as a sampling plan, an AQL, and the requirement for destructive testing.</span></span> <span data-ttu-id="29cc7-363">Kun määrität testiryhmään yksittäisen testin, määrität samalla lisätietoja, kuten järjestyksen, asiakirjat ja voimassaolopäivät.</span><span class="sxs-lookup"><span data-stu-id="29cc7-363">When you assign an individual test to a test group, you define additional information, such as the sequence, documents, and validity dates.</span></span> <span data-ttu-id="29cc7-364">Määrällisessä testissä määritetään myös hyväksyttävät mitta-arvot.</span><span class="sxs-lookup"><span data-stu-id="29cc7-364">For a quantitative test, the information that you define also includes the acceptable measurement values.</span></span> <span data-ttu-id="29cc7-365">Laadullisessa testissä tietoja ovat testimuuttuja ja oletustulos.</span><span class="sxs-lookup"><span data-stu-id="29cc7-365">For a qualitative test, the information includes the test variable and default outcome.</span></span> <span data-ttu-id="29cc7-366">Laatutilaukseen määritetty testiryhmä määrittää oletustestit, jotka tietylle nimikkeelle on suoritettava.</span><span class="sxs-lookup"><span data-stu-id="29cc7-366">The test group that is assigned to a quality order defines the default set of tests that must be performed on the specified item.</span></span> <span data-ttu-id="29cc7-367">Voit kuitenkin lisätä, muuttaa ja poistaa laatutilauksen testejä.</span><span class="sxs-lookup"><span data-stu-id="29cc7-367">However, you can add, delete, or change tests on the quality order.</span></span> <span data-ttu-id="29cc7-368">Laatutilauksen jokaisen testin tulokset raportoidaan.</span><span class="sxs-lookup"><span data-stu-id="29cc7-368">Test results are reported for each test on a quality order.</span></span></td>
<td><span data-ttu-id="29cc7-369">Tuotantoyritys määrittää testiryhmän kutakin laatuvaatimusversiotaan varten.</span><span class="sxs-lookup"><span data-stu-id="29cc7-369">A manufacturing company defines a test group for each variation of its quality guidelines.</span></span> <span data-ttu-id="29cc7-370">Eri testiryhmät edustavat eroja otantasuunnitelmissa, yhdessä suoritettavissa testeissä, hyväksytyissä mitta-arvoissa ja muissa seikoissa.</span><span class="sxs-lookup"><span data-stu-id="29cc7-370">The various test groups reflect differences in the sampling plans, the sets of tests that must be performed together, the AQL, and other factors.</span></span> <span data-ttu-id="29cc7-371">Määrällisissä testeissä eroja on hyväksyttävissä mitta-arvoissa.</span><span class="sxs-lookup"><span data-stu-id="29cc7-371">For quantitative tests, there are also differences in the acceptable measurement values.</span></span> <span data-ttu-id="29cc7-372">Jotta yritys voisi ottaa laatuvaatimuksensa käyttöön, se määrittää kullekin säännölle testiryhmän automaattista laatutilausten luontia varten <strong>Laatuliitokset</strong>-sivulla. Lisäksi se määrittää testiryhmän manuaalisesti luoduille laatutilauksille.</span><span class="sxs-lookup"><span data-stu-id="29cc7-372">To enforce its quality guidelines, the company assigns a test group to each rule for automatically generating quality orders on the <strong>Quality associations</strong> page, and also assigns a test group to quality orders that are manually created.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="29cc7-373">Nimikkeen laaturyhmät</span><span class="sxs-lookup"><span data-stu-id="29cc7-373">Item quality groups</span></span></td>
<td><span data-ttu-id="29cc7-374">Voit määrittää, muokata ja tarkastella tällä sivulla nimikkeitä, jotka on määritetty nimikkeelle määritettyihin laaturyhmiin.</span><span class="sxs-lookup"><span data-stu-id="29cc7-374">Use this page to set up, edit, and view the items that are assigned to a quality group or the quality groups that are assigned to an item.</span></span> <span data-ttu-id="29cc7-375">Laaturyhmän avulla voidaan määrittää nimikkeiden yhteisiä testausvaatimuksia.</span><span class="sxs-lookup"><span data-stu-id="29cc7-375">A quality group represents common testing requirements for items.</span></span> <span data-ttu-id="29cc7-376">Kun olet määrittänyt testivaatimukset <strong>Testiryhmät</strong>-sivulla, voit määrittää laatutilausten automaattisen luonnin säännöt.</span><span class="sxs-lookup"><span data-stu-id="29cc7-376">After you define the test requirements on the <strong>Test groups</strong> page, you can define the rules for automatically generating quality orders.</span></span> <span data-ttu-id="29cc7-377">Prosessin yksinkertaistamiseksi sääntöjä ei määritetä yksittäisille nimikkeille.</span><span class="sxs-lookup"><span data-stu-id="29cc7-377">To simplify the process, you don&#39;t define rules for individual items.</span></span> <span data-ttu-id="29cc7-378">Sen sijaan <strong>Laatuliitokset</strong>-sivulla määritetään laaturyhmän säännöt.</span><span class="sxs-lookup"><span data-stu-id="29cc7-378">Instead, you define rules for a quality group, by using the <strong>Quality associations</strong> page.</span></span> <span data-ttu-id="29cc7-379">Voit myös määrittää valitun laaturyhmän <strong>Nimikkeen laaturyhmät</strong> -sivulla kyseiseen ryhmään liittyvät nimikkeet.</span><span class="sxs-lookup"><span data-stu-id="29cc7-379">You can also use the <strong>Item quality groups</strong> page for a selected quality group to assign relevant items to that group.</span></span> <span data-ttu-id="29cc7-380">Voit myös määrittää valitun nimikkeen <strong>Nimikkeen laaturyhmät</strong> -sivulla kyseiseen nimikkeeseen liittyvät laaturyhmät.</span><span class="sxs-lookup"><span data-stu-id="29cc7-380">You can also use the <strong>Item quality groups</strong> page for a selected item to assign relevant quality groups to that item.</span></span></td>
<td><span data-ttu-id="29cc7-381">Teollisuusyritys ostaa useita eri raaka-aineita, joilla on samat testausvaatimukset tulevaa tarkistusta varten.</span><span class="sxs-lookup"><span data-stu-id="29cc7-381">A manufacturing company purchases various raw materials that have the same testing requirements for incoming inspection.</span></span> <span data-ttu-id="29cc7-382">Yritys määrittää ensin laaturyhmän ja sitten nimiketunnukset, jotka liittyvät kyseisen ryhmän raaka-aineisiin.</span><span class="sxs-lookup"><span data-stu-id="29cc7-382">The company defines a quality group and then assigns the item numbers that are associated with the raw materials to that group.</span></span> <span data-ttu-id="29cc7-383">Yritys ostaa myöhemmin uutta raaka-ainetta, jolla on samat testausvaatimukset.</span><span class="sxs-lookup"><span data-stu-id="29cc7-383">Later, the company purchases a new type of raw material that has the same testing requirements.</span></span> <span data-ttu-id="29cc7-384">Yritys ei määritä uudelle raaka-aineelle uusia testausvaatimuksia vaan lisää uuden materiaalin nimiketunnuksen aiemmin luotuun laaturyhmään.</span><span class="sxs-lookup"><span data-stu-id="29cc7-384">Instead of setting up new testing requirements for the new material, the company adds the item number for the new material to the existing quality group.</span></span> <span data-ttu-id="29cc7-385">Sama teollisuusyritys myös tuottaa nimikkeitä, joilla on samat tuotannon testausvaatimukset, sekä lähettää nimikkeitä, joilla on samat vaatimukset lähetystä edeltävien testien suorittamiseksi.</span><span class="sxs-lookup"><span data-stu-id="29cc7-385">The same manufacturing company also produces items that have the same production testing requirements and ships items that have the same requirement for pre-shipment testing.</span></span> <span data-ttu-id="29cc7-386">Yritys määrittää ensin kaksi laaturyhmää lisää ja sitten kumpaankin soveltuvat nimiketunnukset.</span><span class="sxs-lookup"><span data-stu-id="29cc7-386">The company defines two additional quality groups and then assigns the relevant item numbers to each group.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="29cc7-387">Testimuuttujat</span><span class="sxs-lookup"><span data-stu-id="29cc7-387">Test variables</span></span></td>
<td><span data-ttu-id="29cc7-388">Voit määrittää ja tarkastella tällä sivulla laadulliseen testiin liitettyjä muuttujia.</span><span class="sxs-lookup"><span data-stu-id="29cc7-388">Use this page to define and view the variables that are associated with a qualitative test.</span></span> <span data-ttu-id="29cc7-389">Jokaiselle muuttujalle määritetään numeroitu tulos, joka ilmaisee mahdollisen vaihtoehdon.</span><span class="sxs-lookup"><span data-stu-id="29cc7-389">For each variable, you define enumerated outcomes that represent the possible options.</span></span> <span data-ttu-id="29cc7-390">Testit määritetään <strong>Testit</strong>-sivulla.</span><span class="sxs-lookup"><span data-stu-id="29cc7-390">You define tests on the <strong>Tests</strong> page.</span></span> <span data-ttu-id="29cc7-391">Laadullisten testien testityypiksi on valittava <strong>Vaihtoehto</strong>.</span><span class="sxs-lookup"><span data-stu-id="29cc7-391">For qualitative tests, you must set the test type to <strong>Option</strong>.</span></span> <span data-ttu-id="29cc7-392">Määritä yksittäisen testin testimuuttuja <strong>Testiryhmät</strong>-sivulla.</span><span class="sxs-lookup"><span data-stu-id="29cc7-392">Use the <strong>Test groups</strong> page to assign a test variable to an individual test.</span></span></td>
<td><span data-ttu-id="29cc7-393">Pikkuleipiä valmistava teollisuusyritys tarkastaa lopputuotteen testillä.</span><span class="sxs-lookup"><span data-stu-id="29cc7-393">A manufacturing company that produces cookies uses an inspection test for the finished product.</span></span> <span data-ttu-id="29cc7-394">Tarkastuksessa on useita muuttujia.</span><span class="sxs-lookup"><span data-stu-id="29cc7-394">This inspection test has several variables.</span></span> <span data-ttu-id="29cc7-395">Ensimmäinen muuttuja on maku, jonka mahdollisia tuloksia ovat hyvä ja paha.</span><span class="sxs-lookup"><span data-stu-id="29cc7-395">One variable is taste, and the possible outcomes for this variable are good and bad.</span></span> <span data-ttu-id="29cc7-396">Toinen muuttuja on väri, jonka mahdollisia tuloksia ovat liian tumma, liian vaalea ja oikea.</span><span class="sxs-lookup"><span data-stu-id="29cc7-396">A second variable is color, and the possible outcomes are too dark, too light, and correct.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="29cc7-397">Testimuuttujien tulokset</span><span class="sxs-lookup"><span data-stu-id="29cc7-397">Test variable outcomes</span></span></td>
<td><span data-ttu-id="29cc7-398">Voit määrittää, muokata ja tarkastella tällä sivulla laadulliseen testiin liittyvän testimuuttujan mahdollisia testituloksia.</span><span class="sxs-lookup"><span data-stu-id="29cc7-398">Use this page to set up, edit, and to view the possible test results for a test variable that is associated with a qualitative test.</span></span> <span data-ttu-id="29cc7-399">Kunkin tuloksen tilaksi määritetään joko <strong>hyväksytty</strong> tai <strong>hylätty</strong>.</span><span class="sxs-lookup"><span data-stu-id="29cc7-399">For each outcome, you assign a <strong>pass</strong> or <strong>fail</strong> status.</span></span> <span data-ttu-id="29cc7-400">Jokaiselle <strong>Testit</strong>-sivulla määritetylle laadulliselle testille on määritettävä muuttuja ja tulokset.</span><span class="sxs-lookup"><span data-stu-id="29cc7-400">You must define a variable and its outcomes for each qualitative test that is defined on the <strong>Tests</strong> page.</span></span> <span data-ttu-id="29cc7-401">(Laadullisten testien tyypiksi on määritetty <strong>Vaihtoehto</strong> <strong>Testit</strong>-sivulla.) Käytä <strong>Testiryhmät</strong>-sivua määrittääksesi yksittäisen laadullisen testin testimuuttujan ja oletustuloksen.</span><span class="sxs-lookup"><span data-stu-id="29cc7-401">(For qualitative tests, the test type is set to <strong>Option</strong> on the <strong>Tests</strong> page.) Use the <strong>Test groups</strong> page to assign a test variable and the default outcome to an individual qualitative test.</span></span></td>
<td><span data-ttu-id="29cc7-402">Pikkuleipiä valmistava teollisuusyritys tarkastaa lopputuotteen testillä.</span><span class="sxs-lookup"><span data-stu-id="29cc7-402">A manufacturing company that produces cookies uses an inspection test for the finished product.</span></span> <span data-ttu-id="29cc7-403">Tarkastuksessa on useita muuttujia.</span><span class="sxs-lookup"><span data-stu-id="29cc7-403">This inspection test has of several variables.</span></span> <span data-ttu-id="29cc7-404">Ensimmäinen muuttuja on maku, jonka mahdollisia tuloksia ovat hyvä ja paha.</span><span class="sxs-lookup"><span data-stu-id="29cc7-404">One variable is taste, and the possible outcomes for this variable are good and bad.</span></span> <span data-ttu-id="29cc7-405">Toinen muuttuja on väri, jonka mahdollisia tuloksia ovat liian tumma, liian vaalea ja oikea.</span><span class="sxs-lookup"><span data-stu-id="29cc7-405">A second variable is color, and the possible outcomes are too dark, too light, and correct.</span></span> <span data-ttu-id="29cc7-406">Kunkin tuloksen tilaksi määritetään <strong>hyväksytty</strong> tai <strong>hylätty</strong>.</span><span class="sxs-lookup"><span data-stu-id="29cc7-406">A status of <strong>pass</strong> or <strong>fail</strong> is assigned to each outcome.</span></span> <span data-ttu-id="29cc7-407">Kunkin muuttujan tarkastuksen aikana tarkastaja raportoi testin tuloksen valitsemalla yhden tuloksista.</span><span class="sxs-lookup"><span data-stu-id="29cc7-407">During the inspection test for each variable, the inspector reports the test result by selecting one of the outcomes.</span></span></td>
</tr>
</tbody>
</table>



<a name="additional-resources"></a><span data-ttu-id="29cc7-408">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="29cc7-408">Additional resources</span></span>
--------

[<span data-ttu-id="29cc7-409">Laadunhallintaprosessit</span><span class="sxs-lookup"><span data-stu-id="29cc7-409">Quality management processes</span></span>](quality-management-processes.md)

[<span data-ttu-id="29cc7-410">Määrityksistä poikkeamisen hallinta</span><span class="sxs-lookup"><span data-stu-id="29cc7-410">Nonconformance management</span></span>](enable-nonconformance-management.md)

[<span data-ttu-id="29cc7-411">Laadunhallinta varastoprosesseja varten</span><span class="sxs-lookup"><span data-stu-id="29cc7-411">Quality management for warehouse processes</span></span>](quality-management-for-warehouses-processes.md)
