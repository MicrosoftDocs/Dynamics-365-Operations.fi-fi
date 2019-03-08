---
title: Laadunhallinnan yleiskuvaus
description: Tässä ohjeaiheessa kerrotaan, miten Microsoft Dynamics 365 for Finance and Operationsin laadunhallinnan avulla voidaan parantaa toimitusketjun tuotteiden laatua.
author: perlynne
manager: AnnBe
ms.date: 11/02/2017
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
ms.openlocfilehash: 1630d13437d7e930fdf32ed5fdc61fc62bc33817
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "338311"
---
# <a name="quality-management-overview"></a><span data-ttu-id="15f16-103">Laadunhallinnan yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="15f16-103">Quality management overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="15f16-104">Tässä ohjeaiheessa kerrotaan, miten Microsoft Dynamics 365 for Finance and Operationsin laadunhallinnan avulla voidaan parantaa toimitusketjun tuotteiden laatua.</span><span class="sxs-lookup"><span data-stu-id="15f16-104">This topic describes how you can use quality management in Microsoft Dynamics 365 for Finance and Operations to help improve product quality within your supply chain.</span></span>

<span data-ttu-id="15f16-105">Laadunhallinnan avulla voit hallita määrityksestä poikkeavien tuotteiden käsittelyaikaa niiden lähtöpisteestä riippumatta.</span><span class="sxs-lookup"><span data-stu-id="15f16-105">Quality management can help you manage turnaround times when you handle nonconforming products, regardless of their point of origin.</span></span> <span data-ttu-id="15f16-106">Koska vianmääritystyypit linkitetty korjausraportointiin, Microsoft Dynamics 365 for Finance and Operations voi ajoittaa ongelmien korjaustehtävät ja estää ongelmien toistuminen.</span><span class="sxs-lookup"><span data-stu-id="15f16-106">Because diagnostic types are linked to correction reporting, Microsoft Dynamics 365 for Finance and Operations can schedule tasks to correct problems and prevent them from recurring.</span></span>

<span data-ttu-id="15f16-107">Määrityksistä poikkeamisen hallintatoiminnon lisäksi laadunhallinta sisältää toiminnon ongelmien seuraamiseen ongelmantyypin perusteella (myös sisäiset ongelmat) sekä lyhyt- tai pitkäaikaisen ratkaisun tunnistamiseen.</span><span class="sxs-lookup"><span data-stu-id="15f16-107">In addition to functionality for managing nonconformance, quality management includes functionality for tracking issues by problem type (even internal problems), and for identifying solutions as short-term or long-term.</span></span> <span data-ttu-id="15f16-108">Suorituskykyilmaisimia (KPI) koskevat tilastot antavat tietoja aiemmista määrityksistä poikkeamiseen liittyvistä ongelmista ja niiden korjaamiseen käytetyistä ratkaisuista.</span><span class="sxs-lookup"><span data-stu-id="15f16-108">Statistics about key performance indicators (KPIs) provide insight into the history of previous nonconformance issues and the solutions that were used to correct them.</span></span> <span data-ttu-id="15f16-109">Voit tarkistaa historiallisten tietojen avulla, kuinka tehokkaita aiemmat laatutoimet ovat olleet, ja määrittää, mitkä toimet soveltuvat jatkossa käytettäviksi.</span><span class="sxs-lookup"><span data-stu-id="15f16-109">You can use historical data to review the effectiveness of previous quality measures and determine appropriate measures to use in the future.</span></span>

<span data-ttu-id="15f16-110">Kun määrität laatuliitoksen, Finance and Operations voi luoda liiketoiminnan eri prosesseille, tapahtumille ja ehdoille laatutilauksia.</span><span class="sxs-lookup"><span data-stu-id="15f16-110">When you set up a quality association, Finance and Operations can generate quality orders for various business processes, events, and conditions.</span></span> <span data-ttu-id="15f16-111">Laatuliitos voi koskea tiettyä nimikettä, tiettyä nimikeryhmää tai kaikkia nimikkeitä.</span><span class="sxs-lookup"><span data-stu-id="15f16-111">The quality association can cover a specific item, a specific group of items, or all items.</span></span>

## <a name="examples-of-the-use-of-quality-management"></a><span data-ttu-id="15f16-112">Esimerkkejä laadunhallinnan käytöstä</span><span class="sxs-lookup"><span data-stu-id="15f16-112">Examples of the use of quality management</span></span>
<span data-ttu-id="15f16-113">Laadunhallinta on joustavaa ja se voidaan toteuttaa eri tavoin vastaamaan toimitusketjun työvaiheiden tiettyjen tasojen vaatimuksia.</span><span class="sxs-lookup"><span data-stu-id="15f16-113">Quality management is flexible and can be implemented in various ways to meet the requirements of specific levels of supply chain operations.</span></span> <span data-ttu-id="15f16-114">Seuraavassa esimerkissä käsitellään näiden ominaisuuksien mahdollisia käyttötapoja:</span><span class="sxs-lookup"><span data-stu-id="15f16-114">The following examples illustrate possible uses of these features:</span></span>

-   <span data-ttu-id="15f16-115">Laadunvalvontaprosessin käynnistäminen automaattisesti ennaltamääritettyjen ehtojen perusteella (kun tietyn toimittajan ostotilaus rekisteröidään varastossa).</span><span class="sxs-lookup"><span data-stu-id="15f16-115">Automatically start a quality control process, based on predefined criteria (upon warehouse registration of a purchase order from a specific vendor).</span></span>
-   <span data-ttu-id="15f16-116">Varaston esto tarkastuksen aikana, jotta varastoa, jota ei ole hyväksytty, ei käytetä (ostotilausmäärien täysi esto).</span><span class="sxs-lookup"><span data-stu-id="15f16-116">Block inventory during inspection to prevent non-approved inventory from being used (full blocking of purchase order quantities).</span></span>
-   <span data-ttu-id="15f16-117">Nimikeotannan käyttö laatuliitoksen osana määritettäessä tarkastettavan fyysisen varaston tämän hetkistä määrää.</span><span class="sxs-lookup"><span data-stu-id="15f16-117">Use item sampling as part of a quality association to define the amount of current physical inventory that must be inspected.</span></span> <span data-ttu-id="15f16-118">Otanta voi perustua kiinteisiin määriin tai prosenttiosuuteen.</span><span class="sxs-lookup"><span data-stu-id="15f16-118">Sampling can be based on fixed quantities or a percentage.</span></span>
-   <span data-ttu-id="15f16-119">Luo laatutilaukset osittaisille vastaanotoille.</span><span class="sxs-lookup"><span data-stu-id="15f16-119">Create quality orders for partial receipts.</span></span> <span data-ttu-id="15f16-120">Tilauksen mukana fyysisesti vastaanotettuun määrään perustuva laatutilaus luodaan valitsemalla **Päivitettyä määrää kohden** -valintaruutu **Nimikeotanta**-lomakkeessa.</span><span class="sxs-lookup"><span data-stu-id="15f16-120">To create a quality order that is based on the quantity that is physically received with an order, you must select the **Per updated quantity** check box on the **Item sampling** form.</span></span>
-   <span data-ttu-id="15f16-121">Testin pienimmän, suurimman ja tavoiteltavan arvon sisältävien testityyppien luominen sekä sellaisen määrää ja laatua vertailevan testin suorittaminen, jolla on ennalta määritetyt tarkistustulokset.</span><span class="sxs-lookup"><span data-stu-id="15f16-121">Create test types that include minimum, maximum, and target test values, and perform qualitative-versus-quantitative testing that has predefined validation results.</span></span>
-   <span data-ttu-id="15f16-122">Hyväksyttävän laadun tason määrittäminen laadun mittaustoleranssien hallintaa varten.</span><span class="sxs-lookup"><span data-stu-id="15f16-122">Specify an acceptable quality level (AQL) to control quality measure tolerances.</span></span>
-   <span data-ttu-id="15f16-123">Tarkastustyövaiheiden edellyttämien resurssien, kuten testausalueen tai testin mittavälineiden, määrittäminen.</span><span class="sxs-lookup"><span data-stu-id="15f16-123">Specify the resources that an inspection operation requires, such as a test area and test instruments.</span></span>

## <a name="working-with-quality-associations"></a><span data-ttu-id="15f16-124">Laatuliitosten käsitteleminen</span><span class="sxs-lookup"><span data-stu-id="15f16-124">Working with quality associations</span></span>
<span data-ttu-id="15f16-125">Laatuliitosta käyttävä liiketoimintoprosessi voidaan liittää eri lähdeasiakirjoihin, kuten ostotilauksiin, myyntitilauksiin tai tuotantotilauksiin.</span><span class="sxs-lookup"><span data-stu-id="15f16-125">The business process that uses a quality association can be related to various source documents, such as purchase orders, sales orders, or production orders.</span></span>

<span data-ttu-id="15f16-126">Jokaisessa laatuliitostietueessa määritetään joukko testejä, hyväksyttävän laadun taso ja otantasuunnitelma, jota käytetään muodostettavissa laatutilauksissa.</span><span class="sxs-lookup"><span data-stu-id="15f16-126">Each quality association record defines the set of tests, the AQL, and the sampling plan that applies to the quality orders that are generated.</span></span> <span data-ttu-id="15f16-127">Laatuliitostietue on määritettävä liiketoimintaprosessin jokaiselle muunnokselle.</span><span class="sxs-lookup"><span data-stu-id="15f16-127">You must define a quality association record for each variation in a business process.</span></span> <span data-ttu-id="15f16-128">Voit esimerkiksi määrittää laatuliitoksen, joka muodostaa laatutilauksen, kun ostotilauksen tuotteen vastaanotto päivitetään.</span><span class="sxs-lookup"><span data-stu-id="15f16-128">For example, you can set up a quality association that generates a quality order when a purchase order product receipt is updated.</span></span> <span data-ttu-id="15f16-129">Toimeenpanosuunnitelma määritysten mukaisesti käynnistävä prosessi voidaan estää, jos laatutilaus on avoinna. Myös seuraavat prosessit, kuten ostotilauksen laskutus, voidaan estää.</span><span class="sxs-lookup"><span data-stu-id="15f16-129">Depending on the setup of the execution plan, the triggering process itself can be blocked while there is an open quality order, or the next processes, such as purchase order invoicing, can be blocked.</span></span>

<span data-ttu-id="15f16-130">**Huomautus:** Jos laatutilauksia on avoinna, varastomäärien otto estetään automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="15f16-130">**Note:** While there are open quality orders, inventory quantities are automatically blocked from being issued.</span></span> <span data-ttu-id="15f16-131">**Nimikeotanta**-sivun **Täysi esto** -asetuksen mukaan laatu on joko laatutilauksen määrä tai lähdeasiakirjan rivin määrä.</span><span class="sxs-lookup"><span data-stu-id="15f16-131">Depending on the **Full blocking** setting on the **Item samplings** page, the quantity is either the quantity on the quality order or the quantity on the source document line.</span></span>

<span data-ttu-id="15f16-132">Tietyn liiketoimintaprosessin laatuliitostietue tunnistaa tapahtuman ja ehdot, joille laatutilaus muodostetaan.</span><span class="sxs-lookup"><span data-stu-id="15f16-132">For a given business process, the quality association record identifies the event and the conditions that a quality order is generated for.</span></span> <span data-ttu-id="15f16-133">Ehdot voivat olla joko toimipaikka- tai yrityskohtaisia.</span><span class="sxs-lookup"><span data-stu-id="15f16-133">The conditions can be specific to either a site or a legal entity.</span></span> <span data-ttu-id="15f16-134">Tuhoavia testejä sisältävä laatutilaus voidaan muodostaa vain, kun tapahtumalla on käytettävissä oleva varasto.</span><span class="sxs-lookup"><span data-stu-id="15f16-134">A quality order that involves destructive tests can be generated only when on-hand inventory exists for the event.</span></span>

<span data-ttu-id="15f16-135">Seuraavassa esimerkeissä käsitellään, miten laatuliitostietue määritetään kunkin liiketoimintaprosessin variaatioille.</span><span class="sxs-lookup"><span data-stu-id="15f16-135">The following examples illustrate how a quality association record is defined for the variations in each business process.</span></span> <span data-ttu-id="15f16-136">Seuraavassa taulussa on jokaisen esimerkin yhteenveto laatuliitostietueessa määritetyistä tapahtumista ja ehdoista.</span><span class="sxs-lookup"><span data-stu-id="15f16-136">For each example, the following table summarizes the events and conditions that are defined by a quality association record.</span></span>

<table>
<tbody>
<tr>
<th><span data-ttu-id="15f16-137">Viitetyyppi</span><span class="sxs-lookup"><span data-stu-id="15f16-137">Reference type</span></span></th>
<th><span data-ttu-id="15f16-138">Tapahtumatyyppi</span><span class="sxs-lookup"><span data-stu-id="15f16-138">Event type</span></span></th>
<th><span data-ttu-id="15f16-139">Suoritus</span><span class="sxs-lookup"><span data-stu-id="15f16-139">Execution</span></span></th>
<th><span data-ttu-id="15f16-140">Tapahtuman esto</span><span class="sxs-lookup"><span data-stu-id="15f16-140">Event blocking</span></span></th>
<th><span data-ttu-id="15f16-141">Tiedostoviite</span><span class="sxs-lookup"><span data-stu-id="15f16-141">Document reference</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="15f16-142">Varasto</span><span class="sxs-lookup"><span data-stu-id="15f16-142">Inventory</span></span></td>
<td><span data-ttu-id="15f16-143">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="15f16-143">Not applicable</span></span></td>
<td><span data-ttu-id="15f16-144">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="15f16-144">Not applicable</span></span></td>
<td><span data-ttu-id="15f16-145">Ei mitään</span><span class="sxs-lookup"><span data-stu-id="15f16-145">None</span></span></td>
<td><span data-ttu-id="15f16-146">Kaikki</span><span class="sxs-lookup"><span data-stu-id="15f16-146">All</span></span></td>
</tr>
<tr>
<td rowspan="7"><span data-ttu-id="15f16-147">Myynti</span><span class="sxs-lookup"><span data-stu-id="15f16-147">Sales</span></span></td>
<td rowspan="4"><span data-ttu-id="15f16-148">Keräysprosessi on ajoitettu</span><span class="sxs-lookup"><span data-stu-id="15f16-148">Picking process is scheduled</span></span></td>
<td rowspan="4"><span data-ttu-id="15f16-149">Ennen</span><span class="sxs-lookup"><span data-stu-id="15f16-149">Before</span></span></td>
<td><span data-ttu-id="15f16-150">Ei mitään</span><span class="sxs-lookup"><span data-stu-id="15f16-150">None</span></span></td>
<td rowspan="22"><span data-ttu-id="15f16-151">Tietty tunnus, ryhmä tai vain kaikki</span><span class="sxs-lookup"><span data-stu-id="15f16-151">Specific ID, Group, or All only</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="15f16-152">Keräysprosessi</span><span class="sxs-lookup"><span data-stu-id="15f16-152">Picking process</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="15f16-153">Pakkausluettelo</span><span class="sxs-lookup"><span data-stu-id="15f16-153">Packing slip</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="15f16-154">Lasku</span><span class="sxs-lookup"><span data-stu-id="15f16-154">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="15f16-155">Pakkausluettelo</span><span class="sxs-lookup"><span data-stu-id="15f16-155">Packing slip</span></span></td>
<td rowspan="3"><span data-ttu-id="15f16-156">Ennen</span><span class="sxs-lookup"><span data-stu-id="15f16-156">Before</span></span></td>
<td><span data-ttu-id="15f16-157">Ei mitään</span><span class="sxs-lookup"><span data-stu-id="15f16-157">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="15f16-158">Pakkausluettelo</span><span class="sxs-lookup"><span data-stu-id="15f16-158">Packing slip</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="15f16-159">Lasku</span><span class="sxs-lookup"><span data-stu-id="15f16-159">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="15"><span data-ttu-id="15f16-160">Osto</span><span class="sxs-lookup"><span data-stu-id="15f16-160">Purchase</span></span></td>
<td rowspan="7"><span data-ttu-id="15f16-161">Vastaanottoluettelo</span><span class="sxs-lookup"><span data-stu-id="15f16-161">Receipt list</span></span></td>
<td rowspan="4"><span data-ttu-id="15f16-162">Ennen</span><span class="sxs-lookup"><span data-stu-id="15f16-162">Before</span></span></td>
<td><span data-ttu-id="15f16-163">Ei mitään</span><span class="sxs-lookup"><span data-stu-id="15f16-163">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="15f16-164">Vastaanottoluettelo</span><span class="sxs-lookup"><span data-stu-id="15f16-164">Receipt list</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="15f16-165">Tuotteen vastaanotto</span><span class="sxs-lookup"><span data-stu-id="15f16-165">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="15f16-166">Lasku</span><span class="sxs-lookup"><span data-stu-id="15f16-166">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="15f16-167">Jälkeen</span><span class="sxs-lookup"><span data-stu-id="15f16-167">After</span></span></td>
<td><span data-ttu-id="15f16-168">Ei mitään</span><span class="sxs-lookup"><span data-stu-id="15f16-168">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="15f16-169">Tuotteen vastaanotto</span><span class="sxs-lookup"><span data-stu-id="15f16-169">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="15f16-170">Lasku</span><span class="sxs-lookup"><span data-stu-id="15f16-170">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="15f16-171">Rekisteröinti</span><span class="sxs-lookup"><span data-stu-id="15f16-171">Registration</span></span></td>
<td rowspan="3"><span data-ttu-id="15f16-172">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="15f16-172">Not applicable</span></span></td>
<td><span data-ttu-id="15f16-173">Ei mitään</span><span class="sxs-lookup"><span data-stu-id="15f16-173">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="15f16-174">Tuotteen vastaanotto</span><span class="sxs-lookup"><span data-stu-id="15f16-174">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="15f16-175">Lasku</span><span class="sxs-lookup"><span data-stu-id="15f16-175">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="15f16-176">Tuotteen vastaanotto</span><span class="sxs-lookup"><span data-stu-id="15f16-176">Product receipt</span></span></td>
<td rowspan="3"><span data-ttu-id="15f16-177">Ennen</span><span class="sxs-lookup"><span data-stu-id="15f16-177">Before</span></span></td>
<td><span data-ttu-id="15f16-178">Ei mitään</span><span class="sxs-lookup"><span data-stu-id="15f16-178">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="15f16-179">Tuotteen vastaanotto</span><span class="sxs-lookup"><span data-stu-id="15f16-179">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="15f16-180">Lasku</span><span class="sxs-lookup"><span data-stu-id="15f16-180">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="15f16-181">Jälkeen</span><span class="sxs-lookup"><span data-stu-id="15f16-181">After</span></span></td>
<td><span data-ttu-id="15f16-182">Ei mitään</span><span class="sxs-lookup"><span data-stu-id="15f16-182">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="15f16-183">Lasku</span><span class="sxs-lookup"><span data-stu-id="15f16-183">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="8"><span data-ttu-id="15f16-184">Tuotanto</span><span class="sxs-lookup"><span data-stu-id="15f16-184">Production</span></span></td>
<td rowspan="3"><span data-ttu-id="15f16-185">Rekisteröinti</span><span class="sxs-lookup"><span data-stu-id="15f16-185">Registration</span></span></td>
<td rowspan="3"><span data-ttu-id="15f16-186">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="15f16-186">Not applicable</span></span></td>
<td><span data-ttu-id="15f16-187">Ei mitään</span><span class="sxs-lookup"><span data-stu-id="15f16-187">None</span></span></td>
<td rowspan="12"><span data-ttu-id="15f16-188">Kaikki</span><span class="sxs-lookup"><span data-stu-id="15f16-188">All</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="15f16-189">Ilmoita valmiiksi</span><span class="sxs-lookup"><span data-stu-id="15f16-189">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="15f16-190">Lopeta</span><span class="sxs-lookup"><span data-stu-id="15f16-190">End</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="15f16-191">Ilmoita valmiiksi</span><span class="sxs-lookup"><span data-stu-id="15f16-191">Report as finished</span></span></td>
<td rowspan="3"><span data-ttu-id="15f16-192">Ennen</span><span class="sxs-lookup"><span data-stu-id="15f16-192">Before</span></span></td>
<td><span data-ttu-id="15f16-193">Ei mitään</span><span class="sxs-lookup"><span data-stu-id="15f16-193">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="15f16-194">Ilmoita valmiiksi</span><span class="sxs-lookup"><span data-stu-id="15f16-194">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="15f16-195">Lopeta</span><span class="sxs-lookup"><span data-stu-id="15f16-195">End</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="15f16-196">Jälkeen</span><span class="sxs-lookup"><span data-stu-id="15f16-196">After</span></span></td>
<td><span data-ttu-id="15f16-197">Ei mitään</span><span class="sxs-lookup"><span data-stu-id="15f16-197">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="15f16-198">Lopeta</span><span class="sxs-lookup"><span data-stu-id="15f16-198">End</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="15f16-199">Karanteeni</span><span class="sxs-lookup"><span data-stu-id="15f16-199">Quarantine</span></span></td>
<td rowspan="3"><span data-ttu-id="15f16-200">Ilmoita valmiiksi</span><span class="sxs-lookup"><span data-stu-id="15f16-200">Report as finished</span></span></td>
<td rowspan="2"><span data-ttu-id="15f16-201">Ennen</span><span class="sxs-lookup"><span data-stu-id="15f16-201">Before</span></span></td>
<td><span data-ttu-id="15f16-202">Ilmoita valmiiksi</span><span class="sxs-lookup"><span data-stu-id="15f16-202">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="15f16-203">Lopeta</span><span class="sxs-lookup"><span data-stu-id="15f16-203">End</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="15f16-204">Jälkeen</span><span class="sxs-lookup"><span data-stu-id="15f16-204">After</span></span></td>
<td><span data-ttu-id="15f16-205">Lopeta</span><span class="sxs-lookup"><span data-stu-id="15f16-205">End</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="15f16-206">Lopeta</span><span class="sxs-lookup"><span data-stu-id="15f16-206">End</span></span></td>
<td><span data-ttu-id="15f16-207">Ennen</span><span class="sxs-lookup"><span data-stu-id="15f16-207">Before</span></span></td>
<td><span data-ttu-id="15f16-208">Lopeta</span><span class="sxs-lookup"><span data-stu-id="15f16-208">End</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="15f16-209">Reitityksen työvaihe</span><span class="sxs-lookup"><span data-stu-id="15f16-209">Route operation</span></span></td>
<td rowspan="3"><span data-ttu-id="15f16-210">Ilmoita valmiiksi</span><span class="sxs-lookup"><span data-stu-id="15f16-210">Report as finished</span></span></td>
<td rowspan="2"><span data-ttu-id="15f16-211">Ennen</span><span class="sxs-lookup"><span data-stu-id="15f16-211">Before</span></span></td>
<td><span data-ttu-id="15f16-212">Ei mitään</span><span class="sxs-lookup"><span data-stu-id="15f16-212">None</span></span></td>
<td rowspan="3"><span data-ttu-id="15f16-213">Tietty tunnus, ryhmä tai kaikki tai ryhmäkohtainen, ryhmä tai kaikki</span><span class="sxs-lookup"><span data-stu-id="15f16-213">Specific ID, Group, or All, and Resource specific, Group, or All</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="15f16-214">Ilmoita valmiiksi</span><span class="sxs-lookup"><span data-stu-id="15f16-214">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="15f16-215">Jälkeen</span><span class="sxs-lookup"><span data-stu-id="15f16-215">After</span></span></td>
<td><span data-ttu-id="15f16-216">Ei mitään</span><span class="sxs-lookup"><span data-stu-id="15f16-216">None</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="15f16-217">Oheistuotteen tuotanto</span><span class="sxs-lookup"><span data-stu-id="15f16-217">Co-product production</span></span></td>
<td><span data-ttu-id="15f16-218">Rekisteröinti</span><span class="sxs-lookup"><span data-stu-id="15f16-218">Registration</span></span></td>
<td><span data-ttu-id="15f16-219">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="15f16-219">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="15f16-220">Ei mitään</span><span class="sxs-lookup"><span data-stu-id="15f16-220">None</span></span></td>
<td rowspan="3"><span data-ttu-id="15f16-221">Kaikki</span><span class="sxs-lookup"><span data-stu-id="15f16-221">All</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="15f16-222">Ilmoita valmiiksi</span><span class="sxs-lookup"><span data-stu-id="15f16-222">Report as finished</span></span></td>
<td><span data-ttu-id="15f16-223">Ennen</span><span class="sxs-lookup"><span data-stu-id="15f16-223">Before</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="15f16-224">Jälkeen</span><span class="sxs-lookup"><span data-stu-id="15f16-224">After</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="15f16-225">Seuraavassa taulussa on lisätietoja laatutilausten muodostamisesta tietyntyyppisille prosesseille.</span><span class="sxs-lookup"><span data-stu-id="15f16-225">The following table provides more information about how quality orders can be generated for specific types of processes.</span></span>
<div class="tableSection">

<table>
<tbody>
<tr>
<th><span data-ttu-id="15f16-226">Prosessin tyyppi</span><span class="sxs-lookup"><span data-stu-id="15f16-226">Type of process</span></span></th>
<th><span data-ttu-id="15f16-227">Laatutilausten automaattinen luontiajankohta</span><span class="sxs-lookup"><span data-stu-id="15f16-227">When quality orders can be automatically generated</span></span></th>
<th><span data-ttu-id="15f16-228">Laatutilausten luontiajankohta, jos tuhoava testaus pakollinen</span><span class="sxs-lookup"><span data-stu-id="15f16-228">When quality orders can be generated if destructive testing is required</span></span></th>
<th><span data-ttu-id="15f16-229">Ehdon tiedot</span><span class="sxs-lookup"><span data-stu-id="15f16-229">Condition information</span></span></th>
<th><span data-ttu-id="15f16-230">Manuaalisen luonnin tiedot</span><span class="sxs-lookup"><span data-stu-id="15f16-230">Manual generation information</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="15f16-231">Ostotilaus</span><span class="sxs-lookup"><span data-stu-id="15f16-231">Purchase order</span></span></td>
<td><span data-ttu-id="15f16-232">Ennen kuin vastaanotetun materiaalin vastaanottoluettelo tai tuotteen vastaanotto on kirjattu tai sen jälkeen</span><span class="sxs-lookup"><span data-stu-id="15f16-232">Before or after a receipts list or product receipt for the material that is received is posted</span></span></td>
<td><span data-ttu-id="15f16-233">Vastaanotetun materiaalin tuotteen vastaanoton kirjauksen jälkeen, koska materiaalin on oltava käytettävissä tuhoavaa testausta varten</span><span class="sxs-lookup"><span data-stu-id="15f16-233">After the product receipt for the material that is received is posted, because the material must be available for destructive testing</span></span></td>
<td><span data-ttu-id="15f16-234">Laatutilausvaatimus voi liittyä toimipaikkaan, nimikkeeseen tai toimittajaan tai näiden ehtojen yhdistelmään.</span><span class="sxs-lookup"><span data-stu-id="15f16-234">The requirement for a quality order can reflect a particular site, item, or vendor, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="15f16-235">Manuaalisesti luotu ostotilaukseen viittaava laatutilaus voi käyttää laatuliitostietueen tietoja, kuten testin otantasuunnitelmaa.</span><span class="sxs-lookup"><span data-stu-id="15f16-235">A manually generated quality order that refers to a purchase order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="15f16-236">Karanteenitilaus</span><span class="sxs-lookup"><span data-stu-id="15f16-236">Quarantine order</span></span></td>
<td><span data-ttu-id="15f16-237">Ennen karanteenitilauksen ilmoittamista valmiiksi tai päättyneeksi tai sen jälkeen</span><span class="sxs-lookup"><span data-stu-id="15f16-237">Before or after the quarantine order is reported as finished or ended</span></span></td>
<td><span data-ttu-id="15f16-238">Tuhoavia testejä edellyttäviä laatutilauksia ei voi luoda.</span><span class="sxs-lookup"><span data-stu-id="15f16-238">Quality orders that require destructive tests can&#39;t be generated.</span></span> <span data-ttu-id="15f16-239">Karanteenitilaustoiminnon oletetaan käsittelevän tuhottavan materiaalin käsittelyn.</span><span class="sxs-lookup"><span data-stu-id="15f16-239">It&#39;s assumed that the quarantine order functionality handles the disposition of the material that is destroyed.</span></span></td>
<td><span data-ttu-id="15f16-240">Laatutilausvaatimus voi liittyä toimipaikkaan, nimikkeeseen tai toimittajaan tai näiden ehtojen yhdistelmään.</span><span class="sxs-lookup"><span data-stu-id="15f16-240">The requirement for a quality order can reflect a particular site, item, or vendor, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="15f16-241">Manuaalisesti luotu ostotilaukseen viittaava karanteenitilaus voi käyttää laatuliitostietueen tietoja, kuten testin otantasuunnitelmaa.</span><span class="sxs-lookup"><span data-stu-id="15f16-241">A manually generated quality order that refers to a quarantine order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="15f16-242">Myyntitilaus</span><span class="sxs-lookup"><span data-stu-id="15f16-242">Sales order</span></span></td>
<td><span data-ttu-id="15f16-243">Ennen lähettävien nimikkeiden ajoitettua keräysprosessia tai pakkausluettelon päivitystä</span><span class="sxs-lookup"><span data-stu-id="15f16-243">Before a scheduled picking process or packing slip update for the items that are being shipped</span></span></td>
<td><span data-ttu-id="15f16-244">Kaikissa vaiheissa</span><span class="sxs-lookup"><span data-stu-id="15f16-244">At any step</span></span></td>
<td><span data-ttu-id="15f16-245">Laatutilausvaatimus voi liittyä toimipaikkaan, nimikkeeseen tai asiakkaaseen tai näiden ehtojen yhdistelmään.</span><span class="sxs-lookup"><span data-stu-id="15f16-245">The requirement for a quality order can reflect a particular site, item, or customer, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="15f16-246">Manuaalisesti luotu myyntitilaukseen viittaava laatutilaus voi käyttää laatuliitostietueen tietoja, kuten testin otantasuunnitelmaa.</span><span class="sxs-lookup"><span data-stu-id="15f16-246">A manually generated quality order that refers to a sales order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="15f16-247">Tuotantotilaus</span><span class="sxs-lookup"><span data-stu-id="15f16-247">Production order</span></span></td>
<td><span data-ttu-id="15f16-248">Ennen tuotantotilauksen valmiiksi raportointia tai sen jälkeen</span><span class="sxs-lookup"><span data-stu-id="15f16-248">Before or after the finished quantity for the production order is reported</span></span></td>
<td><span data-ttu-id="15f16-249">Tuotantotilauksen valmiiksi raportoinnin jälkeen</span><span class="sxs-lookup"><span data-stu-id="15f16-249">After the finished quantity for the production order is reported</span></span></td>
<td><span data-ttu-id="15f16-250">Laatutilausvaatimus voi liittyä toimipaikkaan tai nimikkeeseen tai näiden ehtojen yhdistelmään.</span><span class="sxs-lookup"><span data-stu-id="15f16-250">The requirement for a quality order can reflect a particular site or item, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="15f16-251">Manuaalisesti luotu tuotantotilaukseen viittaava laatutilaus voi käyttää laatuliitostietueen tietoja, kuten testin otantasuunnitelmaa.</span><span class="sxs-lookup"><span data-stu-id="15f16-251">A manually generated quality order that refers to a production order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="15f16-252">Tuotantotilaus, jossa on reitityksen työvaihe</span><span class="sxs-lookup"><span data-stu-id="15f16-252">Production order that has a route operation</span></span></td>
<td><span data-ttu-id="15f16-253">Ennen työvaiheen raportin valmistumista tai sen jälkeen</span><span class="sxs-lookup"><span data-stu-id="15f16-253">Before or after the report is finished for an operation</span></span></td>
<td><span data-ttu-id="15f16-254">Viimeisen työvaiheen tuotannon valmiiksi raportoinnin jälkeen</span><span class="sxs-lookup"><span data-stu-id="15f16-254">After the reporting production is finished for the last operation</span></span></td>
<td><span data-ttu-id="15f16-255">Laatutilausvaatimus voi liittyä toimipaikkaan, nimikkeeseen tai operatiiviseen resurssiin tai näiden ehtojen yhdistelmään.</span><span class="sxs-lookup"><span data-stu-id="15f16-255">The requirement for a quality order can reflect a particular, site, item, or operations resource, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="15f16-256">Manuaalisesti luotu reitityksen työvaiheeseen viittaava laatutilaus voi käyttää laatuliitostietueen tietoja, kuten testin otantasuunnitelmaa.</span><span class="sxs-lookup"><span data-stu-id="15f16-256">A manually generated quality order that refers to a route operation can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="15f16-257">Varasto</span><span class="sxs-lookup"><span data-stu-id="15f16-257">Inventory</span></span></td>
<td><span data-ttu-id="15f16-258">Laatutilausta ei voi luoda automaattisesti varastokirjauskansion tapahtumalle eikä siirtotilaustapahtumille.</span><span class="sxs-lookup"><span data-stu-id="15f16-258">A quality order cannot be automatically generated for a transaction in an inventory journal or for transfer order transactions.</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="15f16-259">Laatutilaus on luotava manuaalisesti nimikkeen varastomäärälle.</span><span class="sxs-lookup"><span data-stu-id="15f16-259">A quality order must be created manually for an item&#39;s inventory quantity.</span></span> <span data-ttu-id="15f16-260">Fyysistä käytettävissä olevaa varastoa edellytetään.</span><span class="sxs-lookup"><span data-stu-id="15f16-260">Physical on-hand inventory is required.</span></span></td>
</tr>
</tbody>
</table>

## <a name="quality-management-pages"></a><span data-ttu-id="15f16-261">Laadunhallinnan sivut</span><span class="sxs-lookup"><span data-stu-id="15f16-261">Quality management pages</span></span>
<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="15f16-262">Sivu</span><span class="sxs-lookup"><span data-stu-id="15f16-262">Page</span></span></th>
<th><span data-ttu-id="15f16-263">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="15f16-263">Description</span></span></th>
<th><span data-ttu-id="15f16-264">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="15f16-264">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="15f16-265">Laatuliitokset</span><span class="sxs-lookup"><span data-stu-id="15f16-265">Quality associations</span></span></td>
<td><span data-ttu-id="15f16-266">Katso artikkelin edelliset osat.</span><span class="sxs-lookup"><span data-stu-id="15f16-266">See the previous sections of this article.</span></span></td>
<td><span data-ttu-id="15f16-267">Laatuliitos määrittää kaikki seuraavat muodostettavan laatutilauksen tiedot:</span><span class="sxs-lookup"><span data-stu-id="15f16-267">A quality association defines all the following information for a quality order that is generated:</span></span>
<ul>
<li><span data-ttu-id="15f16-268">Tapahtuma</span><span class="sxs-lookup"><span data-stu-id="15f16-268">The transaction event</span></span></li>
<li><span data-ttu-id="15f16-269">Nimikkeissä suoritettavat testit</span><span class="sxs-lookup"><span data-stu-id="15f16-269">The set of tests that must be performed on the items</span></span></li>
<li><span data-ttu-id="15f16-270">Hyväksyttävän laadun taso</span><span class="sxs-lookup"><span data-stu-id="15f16-270">The AQL</span></span></li>
<li><span data-ttu-id="15f16-271">Otantasuunnitelma</span><span class="sxs-lookup"><span data-stu-id="15f16-271">The sampling plan</span></span></li>
</ul>
<span data-ttu-id="15f16-272">Laatuliitos on määritettävä kutakin sellaista liiketoimintaprosessin muutosta varten, joka edellyttää automaattista laatutilausten luontia.</span><span class="sxs-lookup"><span data-stu-id="15f16-272">You must define a quality association for each variation in a business process that requires automatic generation of quality orders.</span></span> <span data-ttu-id="15f16-273">Laatutilaus voidaan esimerkiksi muodostaa ostotilausten, karanteenitilausten, myyntitilausten ja tuotantotilausten liiketoimintaprosesseille.</span><span class="sxs-lookup"><span data-stu-id="15f16-273">For example, a quality order can be generated in the business processes for purchase orders, quarantine orders, sales orders, and production orders.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="15f16-274">Testit</span><span class="sxs-lookup"><span data-stu-id="15f16-274">Tests</span></span></td>
<td><span data-ttu-id="15f16-275">Voit määrittää ja tarkastella tällä sivulla yksittäisiä testejä, joiden mukaan määräytyy, ovatko tuotteet laatuvaatimusten mukaisia.</span><span class="sxs-lookup"><span data-stu-id="15f16-275">Use this page to define and view the individual tests that determine whether your products meet quality specifications.</span></span> <span data-ttu-id="15f16-276">Voit määrittää testiryhmälle vähintään yhden yksittäisen testin.</span><span class="sxs-lookup"><span data-stu-id="15f16-276">You can assign one or more individual tests to a test group.</span></span> <span data-ttu-id="15f16-277">Siinä tapauksessa määrität myös testikohtaiset tiedot, kuten hyväksyttävät mitta-arvot.</span><span class="sxs-lookup"><span data-stu-id="15f16-277">In this case, you also specify test-specific information, such as the acceptable measurement values.</span></span> <span data-ttu-id="15f16-278">Mitta-arvoja käytetään määrällisissä testeissä, kun taas laadullisissa testeissä käytetään testimuuttujia.</span><span class="sxs-lookup"><span data-stu-id="15f16-278">Measurement values are used for quantitative tests, and test variables are used for qualitative tests.</span></span>
<ul>
<li><span data-ttu-id="15f16-279">Määrällisen testin testityyppi on <strong>Kokonaisluku</strong> tai <strong>Nimellinen</strong>. Lisäksi siihen on määritetty mittayksikkö.</span><span class="sxs-lookup"><span data-stu-id="15f16-279">A quantitative test has a test type of <strong>Integer</strong> or <strong>Fraction</strong>, and also has a designated unit of measure.</span></span> <span data-ttu-id="15f16-280">Laatumääritykset ja testitulokset ilmaistaan numeroina.</span><span class="sxs-lookup"><span data-stu-id="15f16-280">Quality specifications and test results are expressed as numbers.</span></span></li>
<li><span data-ttu-id="15f16-281">Laadullisen testin testityyppi on <strong>Vaihtoehto</strong>.</span><span class="sxs-lookup"><span data-stu-id="15f16-281">A qualitative test has a test type of <strong>Option</strong>.</span></span> <span data-ttu-id="15f16-282">Laadullista testiä varten tarvitaan lisätietoja mitattavasta testimuuttujasta ja sen numeroiduista vaihtoehdoista.</span><span class="sxs-lookup"><span data-stu-id="15f16-282">Qualitative tests require additional information about the test variable that is being measured and its enumerated options.</span></span> <span data-ttu-id="15f16-283">Laatumääritykset ja testitulokset ilmaistaan tuloksen perusteella.</span><span class="sxs-lookup"><span data-stu-id="15f16-283">Quality specifications and test results are expressed according to an outcome.</span></span></li>
</ul></td>
<td><span data-ttu-id="15f16-284">Teollisuusyritys suorittaa ostamalleen materiaalille kaksi testiä: materiaalin laatua koskevan määrällisen testin ja pakkausvahinkoja koskevan laadullisen testin.</span><span class="sxs-lookup"><span data-stu-id="15f16-284">A manufacturing company performs two tests on purchased material: a quantitative test about material quality and a qualitative test about packaging damage.</span></span> <span data-ttu-id="15f16-285">Yritys määrittää laadullisen testin lisätiedoiksi testimuuttujan (vioittunut pakkaus) ja sen mahdolliset tulokset.</span><span class="sxs-lookup"><span data-stu-id="15f16-285">The company defines additional information about the qualitative test to identify the test variable (damaged packaging) and its outcomes.</span></span> <span data-ttu-id="15f16-286">Yritys määrittää <strong>Testiryhmät</strong>-sivulla kaksi testiä testiryhmään. Lisäksi testikohtaiset tiedot määritetään.</span><span class="sxs-lookup"><span data-stu-id="15f16-286">The company uses the <strong>Test groups</strong> page to assign the two tests to a test group and to specify the test-specific information.</span></span> <span data-ttu-id="15f16-287">Testiryhmä määritetään laatutilaukseen, jotta yritys voi raportoida näiden kahden testin testitulokset.</span><span class="sxs-lookup"><span data-stu-id="15f16-287">The test group is assigned to a quality order, so that the company can report test results for the two tests.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="15f16-288">Testiryhmät</span><span class="sxs-lookup"><span data-stu-id="15f16-288">Test groups</span></span></td>
<td><span data-ttu-id="15f16-289">Voit määrittää, muokata ja tarkastella tällä sivulla testiryhmiä ja testiryhmälle määritettyjä yksittäisiä testejä.</span><span class="sxs-lookup"><span data-stu-id="15f16-289">Use this page to set up, edit, and view test groups and the individual tests that are assigned to a test group.</span></span> <span data-ttu-id="15f16-290">Yläruudussa näkyvät testiryhmät, ja alaruudussa näkyvät valitulle testiryhmälle määritetyt testit.</span><span class="sxs-lookup"><span data-stu-id="15f16-290">The upper pane displays test groups, and the lower pane displays the tests that are assigned to a selected test group.</span></span> <span data-ttu-id="15f16-291">Voit määrittää testiryhmälle useita käytäntöjä, kuten otantasuunnitelman, hyväksytyn laatutason ja tuhoavan testin tarpeen.</span><span class="sxs-lookup"><span data-stu-id="15f16-291">You assign several policies to a test group, such as a sampling plan, an AQL, and the requirement for destructive testing.</span></span> <span data-ttu-id="15f16-292">Kun määrität testiryhmään yksittäisen testin, määrität samalla lisätietoja, kuten järjestyksen, asiakirjat ja voimassaolopäivät.</span><span class="sxs-lookup"><span data-stu-id="15f16-292">When you assign an individual test to a test group, you define additional information, such as the sequence, documents, and validity dates.</span></span> <span data-ttu-id="15f16-293">Määrällisessä testissä määritetään myös hyväksyttävät mitta-arvot.</span><span class="sxs-lookup"><span data-stu-id="15f16-293">For a quantitative test, the information that you define also includes the acceptable measurement values.</span></span> <span data-ttu-id="15f16-294">Laadullisessa testissä tietoja ovat testimuuttuja ja oletustulos.</span><span class="sxs-lookup"><span data-stu-id="15f16-294">For a qualitative test, the information includes the test variable and default outcome.</span></span> <span data-ttu-id="15f16-295">Laatutilaukseen määritetty testiryhmä määrittää oletustestit, jotka tietylle nimikkeelle on suoritettava.</span><span class="sxs-lookup"><span data-stu-id="15f16-295">The test group that is assigned to a quality order defines the default set of tests that must be performed on the specified item.</span></span> <span data-ttu-id="15f16-296">Voit kuitenkin lisätä, muuttaa ja poistaa laatutilauksen testejä.</span><span class="sxs-lookup"><span data-stu-id="15f16-296">However, you can add, delete, or change tests on the quality order.</span></span> <span data-ttu-id="15f16-297">Laatutilauksen jokaisen testin tulokset raportoidaan.</span><span class="sxs-lookup"><span data-stu-id="15f16-297">Test results are reported for each test on a quality order.</span></span></td>
<td><span data-ttu-id="15f16-298">Tuotantoyritys määrittää testiryhmän kutakin laatuvaatimusversiotaan varten.</span><span class="sxs-lookup"><span data-stu-id="15f16-298">A manufacturing company defines a test group for each variation of its quality guidelines.</span></span> <span data-ttu-id="15f16-299">Eri testiryhmät edustavat eroja otantasuunnitelmissa, yhdessä suoritettavissa testeissä, hyväksytyissä mitta-arvoissa ja muissa seikoissa.</span><span class="sxs-lookup"><span data-stu-id="15f16-299">The various test groups reflect differences in the sampling plans, the sets of tests that must be performed together, the AQL, and other factors.</span></span> <span data-ttu-id="15f16-300">Määrällisissä testeissä eroja on hyväksyttävissä mitta-arvoissa.</span><span class="sxs-lookup"><span data-stu-id="15f16-300">For quantitative tests, there are also differences in the acceptable measurement values.</span></span> <span data-ttu-id="15f16-301">Jotta yritys voisi ottaa laatuvaatimuksensa käyttöön, se määrittää kullekin säännölle testiryhmän automaattista laatutilausten luontia varten <strong>Laatuliitokset</strong>-sivulla. Lisäksi se määrittää testiryhmän manuaalisesti luoduille laatutilauksille.</span><span class="sxs-lookup"><span data-stu-id="15f16-301">To enforce its quality guidelines, the company assigns a test group to each rule for automatically generating quality orders on the <strong>Quality associations</strong> page, and also assigns a test group to quality orders that are manually created.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="15f16-302">Nimikkeen laaturyhmät</span><span class="sxs-lookup"><span data-stu-id="15f16-302">Item quality groups</span></span></td>
<td><span data-ttu-id="15f16-303">Voit määrittää, muokata ja tarkastella tällä sivulla nimikkeitä, jotka on määritetty nimikkeelle määritettyihin laaturyhmiin.</span><span class="sxs-lookup"><span data-stu-id="15f16-303">Use this page to set up, edit, and view the items that are assigned to a quality group or the quality groups that are assigned to an item.</span></span> <span data-ttu-id="15f16-304">Laaturyhmän avulla voidaan määrittää nimikkeiden yhteisiä testausvaatimuksia.</span><span class="sxs-lookup"><span data-stu-id="15f16-304">A quality group represents common testing requirements for items.</span></span> <span data-ttu-id="15f16-305">Kun olet määrittänyt testivaatimukset <strong>Testiryhmät</strong>-sivulla, voit määrittää laatutilausten automaattisen luonnin säännöt.</span><span class="sxs-lookup"><span data-stu-id="15f16-305">After you define the test requirements on the <strong>Test groups</strong> page, you can define the rules for automatically generating quality orders.</span></span> <span data-ttu-id="15f16-306">Prosessin yksinkertaistamiseksi sääntöjä ei määritetä yksittäisille nimikkeille.</span><span class="sxs-lookup"><span data-stu-id="15f16-306">To simplify the process, you don&#39;t define rules for individual items.</span></span> <span data-ttu-id="15f16-307">Sen sijaan <strong>Laatuliitokset</strong>-sivulla määritetään laaturyhmän säännöt.</span><span class="sxs-lookup"><span data-stu-id="15f16-307">Instead, you define rules for a quality group, by using the <strong>Quality associations</strong> page.</span></span> <span data-ttu-id="15f16-308">Voit myös määrittää valitun laaturyhmän <strong>Nimikkeen laaturyhmät</strong> -sivulla kyseiseen ryhmään liittyvät nimikkeet.</span><span class="sxs-lookup"><span data-stu-id="15f16-308">You can also use the <strong>Item quality groups</strong> page for a selected quality group to assign relevant items to that group.</span></span> <span data-ttu-id="15f16-309">Voit myös määrittää valitun nimikkeen <strong>Nimikkeen laaturyhmät</strong> -sivulla kyseiseen nimikkeeseen liittyvät laaturyhmät.</span><span class="sxs-lookup"><span data-stu-id="15f16-309">You can also use the <strong>Item quality groups</strong> page for a selected item to assign relevant quality groups to that item.</span></span></td>
<td><span data-ttu-id="15f16-310">Teollisuusyritys ostaa useita eri raaka-aineita, joilla on samat testausvaatimukset tulevaa tarkistusta varten.</span><span class="sxs-lookup"><span data-stu-id="15f16-310">A manufacturing company purchases various raw materials that have the same testing requirements for incoming inspection.</span></span> <span data-ttu-id="15f16-311">Yritys määrittää ensin laaturyhmän ja sitten nimiketunnukset, jotka liittyvät kyseisen ryhmän raaka-aineisiin.</span><span class="sxs-lookup"><span data-stu-id="15f16-311">The company defines a quality group and then assigns the item numbers that are associated with the raw materials to that group.</span></span> <span data-ttu-id="15f16-312">Yritys ostaa myöhemmin uutta raaka-ainetta, jolla on samat testausvaatimukset.</span><span class="sxs-lookup"><span data-stu-id="15f16-312">Later, the company purchases a new type of raw material that has the same testing requirements.</span></span> <span data-ttu-id="15f16-313">Yritys ei määritä uudelle raaka-aineelle uusia testausvaatimuksia vaan lisää uuden materiaalin nimiketunnuksen aiemmin luotuun laaturyhmään.</span><span class="sxs-lookup"><span data-stu-id="15f16-313">Instead of setting up new testing requirements for the new material, the company adds the item number for the new material to the existing quality group.</span></span> <span data-ttu-id="15f16-314">Sama teollisuusyritys myös tuottaa nimikkeitä, joilla on samat tuotannon testausvaatimukset, sekä lähettää nimikkeitä, joilla on samat vaatimukset lähetystä edeltävien testien suorittamiseksi.</span><span class="sxs-lookup"><span data-stu-id="15f16-314">The same manufacturing company also produces items that have the same production testing requirements and ships items that have the same requirement for pre-shipment testing.</span></span> <span data-ttu-id="15f16-315">Yritys määrittää ensin kaksi laaturyhmää lisää ja sitten kumpaankin soveltuvat nimiketunnukset.</span><span class="sxs-lookup"><span data-stu-id="15f16-315">The company defines two additional quality groups and then assigns the relevant item numbers to each group.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="15f16-316">Testimuuttujat</span><span class="sxs-lookup"><span data-stu-id="15f16-316">Test variables</span></span></td>
<td><span data-ttu-id="15f16-317">Voit määrittää ja tarkastella tällä sivulla laadulliseen testiin liitettyjä muuttujia.</span><span class="sxs-lookup"><span data-stu-id="15f16-317">Use this page to define and view the variables that are associated with a qualitative test.</span></span> <span data-ttu-id="15f16-318">Jokaiselle muuttujalle määritetään numeroitu tulos, joka ilmaisee mahdollisen vaihtoehdon.</span><span class="sxs-lookup"><span data-stu-id="15f16-318">For each variable, you define enumerated outcomes that represent the possible options.</span></span> <span data-ttu-id="15f16-319">Testit määritetään <strong>Testit</strong>-sivulla.</span><span class="sxs-lookup"><span data-stu-id="15f16-319">You define tests on the <strong>Tests</strong> page.</span></span> <span data-ttu-id="15f16-320">Laadullisten testien testityypiksi on valittava <strong>Vaihtoehto</strong>.</span><span class="sxs-lookup"><span data-stu-id="15f16-320">For qualitative tests, you must set the test type to <strong>Option</strong>.</span></span> <span data-ttu-id="15f16-321">Määritä yksittäisen testin testimuuttuja <strong>Testiryhmät</strong>-sivulla.</span><span class="sxs-lookup"><span data-stu-id="15f16-321">Use the <strong>Test groups</strong> page to assign a test variable to an individual test.</span></span></td>
<td><span data-ttu-id="15f16-322">Pikkuleipiä valmistava teollisuusyritys tarkastaa lopputuotteen testillä.</span><span class="sxs-lookup"><span data-stu-id="15f16-322">A manufacturing company that produces cookies uses an inspection test for the finished product.</span></span> <span data-ttu-id="15f16-323">Tarkastuksessa on useita muuttujia.</span><span class="sxs-lookup"><span data-stu-id="15f16-323">This inspection test has several variables.</span></span> <span data-ttu-id="15f16-324">Ensimmäinen muuttuja on maku, jonka mahdollisia tuloksia ovat hyvä ja paha.</span><span class="sxs-lookup"><span data-stu-id="15f16-324">One variable is taste, and the possible outcomes for this variable are good and bad.</span></span> <span data-ttu-id="15f16-325">Toinen muuttuja on väri, jonka mahdollisia tuloksia ovat liian tumma, liian vaalea ja oikea.</span><span class="sxs-lookup"><span data-stu-id="15f16-325">A second variable is color, and the possible outcomes are too dark, too light, and correct.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="15f16-326">Testimuuttujien tulokset</span><span class="sxs-lookup"><span data-stu-id="15f16-326">Test variable outcomes</span></span></td>
<td><span data-ttu-id="15f16-327">Voit määrittää, muokata ja tarkastella tällä sivulla laadulliseen testiin liittyvän testimuuttujan mahdollisia testituloksia.</span><span class="sxs-lookup"><span data-stu-id="15f16-327">Use this page to set up, edit, and to view the possible test results for a test variable that is associated with a qualitative test.</span></span> <span data-ttu-id="15f16-328">Kunkin tuloksen tilaksi määritetään joko <strong>hyväksytty</strong> tai <strong>hylätty</strong>.</span><span class="sxs-lookup"><span data-stu-id="15f16-328">For each outcome, you assign a <strong>pass</strong> or <strong>fail</strong> status.</span></span> <span data-ttu-id="15f16-329">Jokaiselle <strong>Testit</strong>-sivulla määritetylle laadulliselle testille on määritettävä muuttuja ja tulokset.</span><span class="sxs-lookup"><span data-stu-id="15f16-329">You must define a variable and its outcomes for each qualitative test that is defined on the <strong>Tests</strong> page.</span></span> <span data-ttu-id="15f16-330">(Laadullisten testien tyypiksi on määritetty <strong>Vaihtoehto</strong> <strong>Testit</strong>-sivulla.) Käytä <strong>Testiryhmät</strong>-sivua määrittääksesi yksittäisen laadullisen testin testimuuttujan ja oletustuloksen.</span><span class="sxs-lookup"><span data-stu-id="15f16-330">(For qualitative tests, the test type is set to <strong>Option</strong> on the <strong>Tests</strong> page.) Use the <strong>Test groups</strong> page to assign a test variable and the default outcome to an individual qualitative test.</span></span></td>
<td><span data-ttu-id="15f16-331">Pikkuleipiä valmistava teollisuusyritys tarkastaa lopputuotteen testillä.</span><span class="sxs-lookup"><span data-stu-id="15f16-331">A manufacturing company that produces cookies uses an inspection test for the finished product.</span></span> <span data-ttu-id="15f16-332">Tarkastuksessa on useita muuttujia.</span><span class="sxs-lookup"><span data-stu-id="15f16-332">This inspection test has of several variables.</span></span> <span data-ttu-id="15f16-333">Ensimmäinen muuttuja on maku, jonka mahdollisia tuloksia ovat hyvä ja paha.</span><span class="sxs-lookup"><span data-stu-id="15f16-333">One variable is taste, and the possible outcomes for this variable are good and bad.</span></span> <span data-ttu-id="15f16-334">Toinen muuttuja on väri, jonka mahdollisia tuloksia ovat liian tumma, liian vaalea ja oikea.</span><span class="sxs-lookup"><span data-stu-id="15f16-334">A second variable is color, and the possible outcomes are too dark, too light, and correct.</span></span> <span data-ttu-id="15f16-335">Kunkin tuloksen tilaksi määritetään <strong>hyväksytty</strong> tai <strong>hylätty</strong>.</span><span class="sxs-lookup"><span data-stu-id="15f16-335">A status of <strong>pass</strong> or <strong>fail</strong> is assigned to each outcome.</span></span> <span data-ttu-id="15f16-336">Kunkin muuttujan tarkastuksen aikana tarkastaja raportoi testin tuloksen valitsemalla yhden tuloksista.</span><span class="sxs-lookup"><span data-stu-id="15f16-336">During the inspection test for each variable, the inspector reports the test result by selecting one of the outcomes.</span></span></td>
</tr>
</tbody>
</table>



<a name="additional-resources"></a><span data-ttu-id="15f16-337">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="15f16-337">Additional resources</span></span>
--------

[<span data-ttu-id="15f16-338">Laadunhallintaprosessit</span><span class="sxs-lookup"><span data-stu-id="15f16-338">Quality management processes</span></span>](quality-management-processes.md)

[<span data-ttu-id="15f16-339">Määrityksistä poikkeamisen hallinnan ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="15f16-339">Enabling nonconformance management</span></span>](enable-nonconformance-management.md)
