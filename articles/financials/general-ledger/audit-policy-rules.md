---
title: Tilinarkastuskäytännön säännöt
description: Voit käyttää tarkistuskäytäntöjä kuluraporttien, toimittajan laskujen ja ostotilausten arvioimiseen, jotta voit varmistua luomiesi käytäntösääntöjen noudattamisesta. Kaikki tarkastuskäytäntöön liittyvät säännöt suoritetaan erätilassa määrittämäsi aikataulun mukaisesti.  Jokainen käytäntösääntö on käytäntösäännön tyypin esiintymä. Jokaisella käytäntösääntötyypillä voi olla kerrallaan aktiivisena vain yksi käytäntösääntö.
author: ryansandness
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AuditPolicyAdditionalOption, AuditPolicyRule
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 12991
ms.assetid: 8d787017-71dc-418f-b8c2-4ea9763d9978
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 18b8a1649a26ebacc34b828ed25ec9646dd438a1
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/15/2019
ms.locfileid: "1567349"
---
# <a name="audit-policy-rules"></a><span data-ttu-id="ead5b-106">Tilinarkastuskäytännön säännöt</span><span class="sxs-lookup"><span data-stu-id="ead5b-106">Audit policy rules</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ead5b-107">Voit käyttää tarkistuskäytäntöjä kuluraporttien, toimittajan laskujen ja ostotilausten arvioimiseen, jotta voit varmistua luomiesi käytäntösääntöjen noudattamisesta.</span><span class="sxs-lookup"><span data-stu-id="ead5b-107">You can use audit policies to evaluate expense reports, vendor invoices, and purchase orders to make sure that they comply with policy rules that you create.</span></span> <span data-ttu-id="ead5b-108">Kaikki tarkastuskäytäntöön liittyvät säännöt suoritetaan erätilassa määrittämäsi aikataulun mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="ead5b-108">All of the rules that are associated with an audit policy are run in batch mode, according to a schedule that you specify.</span></span>  <span data-ttu-id="ead5b-109">Jokainen käytäntösääntö on käytäntösäännön tyypin esiintymä.</span><span class="sxs-lookup"><span data-stu-id="ead5b-109">Each policy rule is an instance of a policy rule type.</span></span> <span data-ttu-id="ead5b-110">Jokaisella käytäntösääntötyypillä voi olla kerrallaan aktiivisena vain yksi käytäntösääntö.</span><span class="sxs-lookup"><span data-stu-id="ead5b-110">For each policy rule type, only one policy rule can be active at a time.</span></span> 

<a name="queries-and-query-types"></a><span data-ttu-id="ead5b-111">Kyselyt ja Kyselytyypit</span><span class="sxs-lookup"><span data-stu-id="ead5b-111">Queries and query types</span></span>
-----------------------

<span data-ttu-id="ead5b-112">Kun luot tarkistuskäytännön sääntö, sinun on valittava käytäntösääntötyyppi.</span><span class="sxs-lookup"><span data-stu-id="ead5b-112">When you create an audit policy rule, you first select a policy rule type.</span></span> <span data-ttu-id="ead5b-113">Käytäntösäännön tyyppi määrittää sovellusobjektipuu (AOT) -kyselyn, jota käytetään aloituskohtana käytäntösäännön luomisessa.</span><span class="sxs-lookup"><span data-stu-id="ead5b-113">The policy rule type specifies the Application Object Tree (AOT) query to use as the starting point for creating the policy rule.</span></span> <span data-ttu-id="ead5b-114">Se määrittää myös käytäntösäännölle käytettävän kyselyn tyypin.</span><span class="sxs-lookup"><span data-stu-id="ead5b-114">It also specifies the query type to use for the policy rule.</span></span> <span data-ttu-id="ead5b-115">Kysely määrittää lähdeasiakirjan, jolle käytäntösääntötyyppi tulkitaan.</span><span class="sxs-lookup"><span data-stu-id="ead5b-115">The query determines the source document that the policy rule evaluates.</span></span> <span data-ttu-id="ead5b-116">Se määrittää myös lähdeasiakirjan kentät, joiden avulla tunnistetaan sekä yritys että käytettävä päivämäärä, kun asiakirjoja valitaan auditointiin.</span><span class="sxs-lookup"><span data-stu-id="ead5b-116">It also specifies the fields in the source document that identify both the legal entity and the date to use when documents are selected for audit.</span></span> <span data-ttu-id="ead5b-117">Kyselytyyppi hallitsee kyselysivun ja tilintarkastuskäytäntö sääntöjen sivun oletuskenttiä.</span><span class="sxs-lookup"><span data-stu-id="ead5b-117">The query type controls the default fields in the query page and in the Audit policy rule page.</span></span> <span data-ttu-id="ead5b-118">Seuraavassa taulukossa on kyselytyypit, joiden on oltava käytettävissä tarkistuksen käytäntösäännöille.</span><span class="sxs-lookup"><span data-stu-id="ead5b-118">The following table shows the query types that are available for audit policy rules.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ead5b-119">Kyselytyyppi</span><span class="sxs-lookup"><span data-stu-id="ead5b-119">Query type</span></span></th>
<th><span data-ttu-id="ead5b-120">Tarkoitus</span><span class="sxs-lookup"><span data-stu-id="ead5b-120">Purpose</span></span></th>
<th><span data-ttu-id="ead5b-121">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="ead5b-121">More information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ead5b-122">Ehdollinen</span><span class="sxs-lookup"><span data-stu-id="ead5b-122">Conditional</span></span></td>
<td><span data-ttu-id="ead5b-123">Arvioi lähdeasiakirjan määritteitä määritettyjen arvojen kanssa.</span><span class="sxs-lookup"><span data-stu-id="ead5b-123">Evaluate source document attributes against specified values.</span></span></td>
<td></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ead5b-124">Kooste</span><span class="sxs-lookup"><span data-stu-id="ead5b-124">Aggregate</span></span></td>
<td><span data-ttu-id="ead5b-125">Arvioi useita lähdeasiakirjoja tai lähdeasiakirjarivejä käytäntösäännön kanssa yhdistämällä numeroarvoja.</span><span class="sxs-lookup"><span data-stu-id="ead5b-125">Evaluate multiple source documents or source document lines against a policy rule by aggregating numeric values.</span></span></td>
<td></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ead5b-126">Otanta</span><span class="sxs-lookup"><span data-stu-id="ead5b-126">Sampling</span></span></td>
<td><span data-ttu-id="ead5b-127">Valitse satunnaisesti tietty lähde-tiedostojen prosenttiosuus arvioidaksesi käytännön rikkomuksia.</span><span class="sxs-lookup"><span data-stu-id="ead5b-127">Randomly select a specified percentage of the source documents to evaluate for policy violations.</span></span></td>
<td><span data-ttu-id="ead5b-128">Kun valitset tämän vaihtoehdon, käytä tilintarkastuksen käytäntösääntösivua määrittämään asiakirjojen prosenttiosuuden satunnaisesti valiten auditoinnin.</span><span class="sxs-lookup"><span data-stu-id="ead5b-128">When you select this option, use the Audit policy rule page to specify the percentage of documents to randomly select for audit.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ead5b-129">Monista</span><span class="sxs-lookup"><span data-stu-id="ead5b-129">Duplicate</span></span></td>
<td><span data-ttu-id="ead5b-130">Arvioi lähdeasiakirjat, jotta voit määrittää sisältävätkö ne kaksoismerkintöjä tietyissä kentissä.</span><span class="sxs-lookup"><span data-stu-id="ead5b-130">Evaluate source documents to determine whether they contain duplicate entries in specified fields.</span></span></td>
<td><span data-ttu-id="ead5b-131">Kun valitset tämän vaihtoehdon, käytä tilintarkastus käytäntösääntö sivua määrittämään päivien määrän, joka lisätään asiakirjan valitun päivämäärävälin alkuun asiakirjoja arvioitaessa kaksoiskappaleita varten.</span><span class="sxs-lookup"><span data-stu-id="ead5b-131">When you select this option, use the Audit policy rule page to specify the number of days to add to the start of the document selection date range when documents are evaluated for duplicate entries.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ead5b-132">Luettelohaku</span><span class="sxs-lookup"><span data-stu-id="ead5b-132">List search</span></span></td>
<td><span data-ttu-id="ead5b-133">Arvioi tiettyjen yksiköiden lähdeasiakirjat.</span><span class="sxs-lookup"><span data-stu-id="ead5b-133">Evaluate source documents for specific entities.</span></span></td>
<td><span data-ttu-id="ead5b-134">Kyselyn pääasiakirja määrittää auditoitavan asiakirjan.</span><span class="sxs-lookup"><span data-stu-id="ead5b-134">The root document of the query defines the document that is being audited.</span></span> <span data-ttu-id="ead5b-135">Kyselyn on oltava luettelokysely, joka sisältää viittauksen dirpartytable taulukkoon.</span><span class="sxs-lookup"><span data-stu-id="ead5b-135">The query must be a list query that includes a reference to the dirpartytable table.</span></span> <span data-ttu-id="ead5b-136">Tätä asetusta voidaan käyttää vain seuraavissa AOT-kyselyissä:</span><span class="sxs-lookup"><span data-stu-id="ead5b-136">This option can be used only with the following AOT queries:</span></span>
<ul>
<li><span data-ttu-id="ead5b-137"><span class="ui">Tilintarkastuskäytäntölista</span> (Kuluraporteissa valvonnassa olevat työntekijät)</span><span class="sxs-lookup"><span data-stu-id="ead5b-137"><span class="ui">AuditPolicyExpenseList</span> (Expense report monitored employees)</span></span></li>
<li><span data-ttu-id="ead5b-138"><span class="ui">TilintarkastuskäytäntöOstoLista</span> (Ostotilauksissa valvonnassa olevat toimittajat)</span><span class="sxs-lookup"><span data-stu-id="ead5b-138"><span class="ui">AuditPolicyPurchList</span> (Purchase order monitored vendors)</span></span></li>
<li><span data-ttu-id="ead5b-139"><span class="ui">TilintarkastuskäytäntöToimittajaLaskuLista</span> (Toimittajalaskuissa seuratut toimittajat)</span><span class="sxs-lookup"><span data-stu-id="ead5b-139"><span class="ui">AuditPolicyVendInvoiceList</span> (Vendor invoice monitored vendors)</span></span></li>
</ul>
<span data-ttu-id="ead5b-140">Kun valitset tämän vaihtoehdon, määritä valvotut kohteet Tilintarkastuskäytännön säännöt -sivulla.</span><span class="sxs-lookup"><span data-stu-id="ead5b-140">When you select this option, specify the monitored entities in the Audit policy rule page.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ead5b-141">Avainsanahaku</span><span class="sxs-lookup"><span data-stu-id="ead5b-141">Keyword search</span></span></td>
<td><span data-ttu-id="ead5b-142">Arvioi lähdeasiakirjat, jotta voit määrittää sisältävätkö ne tietyt sanat.</span><span class="sxs-lookup"><span data-stu-id="ead5b-142">Evaluate source documents to determine whether they contain certain words.</span></span></td>
<td><span data-ttu-id="ead5b-143">Kun valitset tämän vaihtoehdon, syötä sanat, joita etsitään Tilintarkastuskäytännön säännöt -sivulla.</span><span class="sxs-lookup"><span data-stu-id="ead5b-143">When you select this option, enter the words to look for in the Audit policy rule page.</span></span> <span data-ttu-id="ead5b-144">Tilintarkastussäännöt-sivu sisältää myös asetukset, joiden avulla voit määrittää taulut ja kentät kirjoittamiesi sanojen arvioimiseksi.</span><span class="sxs-lookup"><span data-stu-id="ead5b-144">The Audit policy rule page also includes options that let you specify the tables and fields to evaluate for the words you entered.</span></span></td>
</tr>
</tbody>
</table>

## <a name="common-parameters"></a><span data-ttu-id="ead5b-145">Yleiset parametrit</span><span class="sxs-lookup"><span data-stu-id="ead5b-145">Common parameters</span></span>
<span data-ttu-id="ead5b-146">Kaikilla tietyn tarkastuskäytännön säännöillä on samat eräparametrit ja sama asiakirjan valinnan päivämääräväli.</span><span class="sxs-lookup"><span data-stu-id="ead5b-146">All of the policy rules for a particular audit policy share the same batch parameters and the same document selection date range.</span></span> <span data-ttu-id="ead5b-147">Nämä parametrit on määritetty käytännölle Lisävaihtoehdot-sivulla.</span><span class="sxs-lookup"><span data-stu-id="ead5b-147">These parameters are specified for the policy in the Additional options page.</span></span>



<a name="additional-resources"></a><span data-ttu-id="ead5b-148">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="ead5b-148">Additional resources</span></span>
--------

<span data-ttu-id="ead5b-149">[Tarkistuskäytäntörikkomukset ja -tapaukset](audit-policy-violations-cases.md)
[Tarkistuskäytäntöjen määrittäminen lähdeasiakirjoille](tasks/define-audit-policies-source-documents.md)</span><span class="sxs-lookup"><span data-stu-id="ead5b-149">[Audit policy violations and cases](audit-policy-violations-cases.md)
[Define audit policies for source documents](tasks/define-audit-policies-source-documents.md)</span></span>


