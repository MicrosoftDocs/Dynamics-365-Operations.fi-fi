---
title: Standardikustannusten edellytykset
description: "Tässä ohjeaiheessa käsitellään standardikustannusten käyttämiseen liittyvät perusvaiheet."
author: AndersGirke
manager: AnnBe
ms.date: 01/17/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventStdCostConv, CostingVersion
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: f7f1cef3198462eab15c1c7d2de4c5d4a5576919
ms.contentlocale: fi-fi
ms.lasthandoff: 04/13/2018

---

# <a name="prerequisites-for-standard-costs"></a><span data-ttu-id="82e21-103">Standardikustannusten edellytykset</span><span class="sxs-lookup"><span data-stu-id="82e21-103">Prerequisites for standard costs</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="82e21-104">Tässä ohjeaiheessa käsitellään standardikustannusten käyttämiseen liittyvät perusvaiheet.</span><span class="sxs-lookup"><span data-stu-id="82e21-104">This topic describes the basic steps for using standard costs.</span></span> <span data-ttu-id="82e21-105">Sen jälkeen vaiheet määräytyvät yrityksen työvaiheiden mukaan.</span><span class="sxs-lookup"><span data-stu-id="82e21-105">Subsequent steps depend on the company's operations.</span></span> <span data-ttu-id="82e21-106">Vaiheet ovat esimerkiksi erilaiset muussa kuin valmistusympäristössä, valmistusympäristössä ilman työvaiheistuksia ja valmistusympäristössä, jossa käytetään työvaiheistuksia.</span><span class="sxs-lookup"><span data-stu-id="82e21-106">For example, the steps differ for a nonmanufacturing environment, a manufacturing environment that doesn't use routings, and a manufacturing environment that uses routings.</span></span> 

<span data-ttu-id="82e21-107">Voit määrittää standardikustannukset seuraavien ohjeiden mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="82e21-107">To set up standard costs, follow these steps.</span></span>

<span data-ttu-id="82e21-108">**1. Luo nimikemalliryhmä standardikustannuksia varten.**</span><span class="sxs-lookup"><span data-stu-id="82e21-108">**1. Create an item model group for standard costs.**</span></span>

<span data-ttu-id="82e21-109">Luo **Nimikemalliryhmät** -sivulla uusi standardikustannusten ryhmä ja määritä **Standardikustannus**-varastomalli.</span><span class="sxs-lookup"><span data-stu-id="82e21-109">Use the **Item model groups** page to create a new group for standard costs, and assign an inventory model of **Standard cost**.</span></span> <span data-ttu-id="82e21-110">Nimikkeen malliryhmän tunnuksen on oltava kuvaileva, kuten **Std-kustannus**.</span><span class="sxs-lookup"><span data-stu-id="82e21-110">The identifier for the item model group should be meaningful, such as **Std Cost**.</span></span> <span data-ttu-id="82e21-111">Valitse valintaruudut ilmaisemaan, että ryhmä sallii negatiivisen kirjanpitovaraston ja että sen on kirjattava varastotilanne ja kirjanpitovarasto.</span><span class="sxs-lookup"><span data-stu-id="82e21-111">Select the check boxes to indicate that the group should allow financial negative inventory, and that it should post physical inventory and financial inventory.</span></span> <span data-ttu-id="82e21-112">Tämä standardikustannusryhmä määritetään nimikkeille.</span><span class="sxs-lookup"><span data-stu-id="82e21-112">This standard cost group will be assigned to items.</span></span>

<span data-ttu-id="82e21-113">**2. Määritä standardikustannusvariansseihin liittyvät kirjanpitotilit.**</span><span class="sxs-lookup"><span data-stu-id="82e21-113">**2. Define ledger accounts that are related to standard cost variances.**</span></span> 

<span data-ttu-id="82e21-114">Määritä standardikustannusvariansseihin liittyvät kirjanpitotilit **Tilikartta**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="82e21-114">Use the **Chart of accounts** page to define ledger accounts that are related to standard cost variances.</span></span> <span data-ttu-id="82e21-115">Nämä kirjanpitotilit täytyy määrittää, ennen kuin ne voi määrittää **Kirjaus**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="82e21-115">These ledger accounts must be defined before they can be assigned on the **Posting** page.</span></span> <span data-ttu-id="82e21-116">Kirjanpitotilit voivat kuvastaa nimikeryhmiä ja kustannusryhmiä.</span><span class="sxs-lookup"><span data-stu-id="82e21-116">The ledger accounts can reflect item groups and cost groups.</span></span>

<span data-ttu-id="82e21-117">**3. Määritä standardikustannusvariansseihin liittyvät tilit varastokirjauksiin.**</span><span class="sxs-lookup"><span data-stu-id="82e21-117">**3. Assign ledger accounts to item postings that are related to standard cost variances.**</span></span> 

<span data-ttu-id="82e21-118">Määritä standardikustannusvariansseihin liittyvät kirjanpitotilit **Kirjaus**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="82e21-118">Use the **Posting** page to assign the ledger accounts that are related to standard cost variances.</span></span> <span data-ttu-id="82e21-119">Voit määrittää varianssin kirjanpitotilin nimikkeen (tai nimikeryhmän) ja kustannusryhmän (tai kustannusryhmän tyypin) mukaan. Vaihtoehtoisesti voit määrittää, että kirjanpitotilit koskevat kaikkia nimikkeitä ja kaikkia kustannusryhmiä.</span><span class="sxs-lookup"><span data-stu-id="82e21-119">You can specify a variance's ledger account by item (or item group) and by cost group (or cost group type), or you can specify that the ledger account applies to all items and all cost groups.</span></span> <span data-ttu-id="82e21-120">Nämä vaihtoehdot vastaavat taulukoiden, ryhmien sekä kaikkien kohteiden kustannussuhteita.</span><span class="sxs-lookup"><span data-stu-id="82e21-120">These options correspond to cost relations for tables, groups, and all.</span></span> 

<span data-ttu-id="82e21-121">Voit ottaa kustannussuhteet käyttöön (taulukoissa, ryhmissä ja kaikissa kohteissa) **Tapahtumayhdistelmät**-sivulla ennen nimikekirjaussääntöjen määrittämistä.</span><span class="sxs-lookup"><span data-stu-id="82e21-121">Before you define the item posting rules, use the **Transaction combinations** page to enable cost relations (for tables, groups, and all).</span></span>

<span data-ttu-id="82e21-122">**4. Määritä standardikustannuksiin liittyvät varastoparametrit.**</span><span class="sxs-lookup"><span data-stu-id="82e21-122">**4. Define inventory parameters that are related to standard costs.**</span></span> 

-  <span data-ttu-id="82e21-123">Määritä **Varastoparametrit**-sivun **Tuoterakenne**-välilehdellä kaksi standardikustannuksiin liittyvää parametria.</span><span class="sxs-lookup"><span data-stu-id="82e21-123">Use the **Bills of materials** tab on the **Inventory parameters** page to define two cost control parameters that are related to standard costs.</span></span> 

    -  <span data-ttu-id="82e21-124">Valitse **Kustannuserittely**-kentässä voit valita arvoksi **Ei mitään** tai **Alakirjanpito**.</span><span class="sxs-lookup"><span data-stu-id="82e21-124">In the **Cost breakdown** field, select **None** or **Sub ledger**.</span></span> <span data-ttu-id="82e21-125">Jos valitset **Alakirjanpito**, kustannuserittely on *aktiivinen* kustannuserittely.</span><span class="sxs-lookup"><span data-stu-id="82e21-125">If you select **Sub ledger**, the cost breakdown is an *active* cost breakdown.</span></span> <span data-ttu-id="82e21-126">Aktiivista kustannusseurantaa tarvitaan välttämättä, kun kustannusryhmien segmentointi lasketaan, säilytetään ja otetaan tarkasteluun monitasoisessa tuoterakenteessa standardikustannusnimikkeitä varten.</span><span class="sxs-lookup"><span data-stu-id="82e21-126">An active cost breakdown is critical for calculating, retaining, and viewing cost group segmentation across a multilevel product structure for standard cost items.</span></span> <span data-ttu-id="82e21-127">Kun kustannuserittely on aktiivinen, voit tehdä kustannusryhmäkohtaisia analyyseja ja raportteja varastoon liittyvistä tiedoista, keskeneräisistä töistä (KET-töistä) ja myytyjen tuotteiden kustannuksista (MTKUST) yksitasoisessa ja monitasoisessa muodossa sekä summamuodossa.</span><span class="sxs-lookup"><span data-stu-id="82e21-127">When the cost breakdown is active, you can report and analyze inventory, work in process (WIP), and cost of goods sold (COGS) per cost group in a single-level, multilevel, or total format.</span></span> <span data-ttu-id="82e21-128">Kun kustannuserittely on aktiivinen, valmistetun nimikkeen kustannuksen aktivointi aiheuttaa kustannusryhmän segmentoinnin tallentamisen nimikkeen kustannustietoihin.</span><span class="sxs-lookup"><span data-stu-id="82e21-128">When the cost breakdown is active, if you activate a manufactured item's cost, the cost group segmentation will be stored in the item's cost record.</span></span> 

    -  <span data-ttu-id="82e21-129">Jos valitset **Ei mitään**, standardikustannusnimikkeiden kustannusryhmäsegmentointia ei ylläpidetä.</span><span class="sxs-lookup"><span data-stu-id="82e21-129">If you select **None**, cost group segmentation won't be maintained for standard cost items.</span></span> <span data-ttu-id="82e21-130">Toisin sanoen valmistetun nimikkeen standardikustannus lasketaan ja ylläpidetään yksittäisenä summana ilman kustannusryhmän segmentointia.</span><span class="sxs-lookup"><span data-stu-id="82e21-130">In other words, a manufactured item's standard cost will be calculated and maintained as a single amount, without cost group segmentation.</span></span> <span data-ttu-id="82e21-131">Valmistettujen osien kustannusvaikutukset yhdistetään yhteen summaan.</span><span class="sxs-lookup"><span data-stu-id="82e21-131">The cost contributions of manufactured components will be aggregated into the single amount.</span></span>

-  <span data-ttu-id="82e21-132">Valitse **Vakio-varianssit**-kentässä **Yhteensä** tai **Kustannusryhmittäin**.</span><span class="sxs-lookup"><span data-stu-id="82e21-132">In the **Variances to standard** field, select **Summarized** or **Per cost group**.</span></span> <span data-ttu-id="82e21-133">Jos valitset **Kustannusryhmittäin**, voit tunnistaa ostohinnan varianssit ja tuotannon varianssit kustannusryhmittäin.</span><span class="sxs-lookup"><span data-stu-id="82e21-133">If you select **Per cost group**, you can identify purchase price variances and production variances by cost group.</span></span> <span data-ttu-id="82e21-134">Voit myös määrittää neljäntyyppisiä tuotannon variansseja: erän koon, määrän, hinnan ja korvauksen varianssi.</span><span class="sxs-lookup"><span data-stu-id="82e21-134">You can also identify the four types of production variances: the lot size, quantity, price, and substitution variances.</span></span> <span data-ttu-id="82e21-135">Jos valitset **Yhteensä**, et voi määrittää variansseja kustannusryhmittäin etkä tunnistaa tuotannon varianssien neljää tyyppiä.</span><span class="sxs-lookup"><span data-stu-id="82e21-135">If you select **Summarized**, you can't identify variances by cost group, and you can't identify the four types of production variances.</span></span> <span data-ttu-id="82e21-136">Voit tarkastella vain tuotannon varianssien yhteenvetoa.</span><span class="sxs-lookup"><span data-stu-id="82e21-136">You can just view a summarized production variance.</span></span>

-  <span data-ttu-id="82e21-137">Vakiovarianssia koskeva käytäntö on erillinen kustannuserittelykäytännöstä.</span><span class="sxs-lookup"><span data-stu-id="82e21-137">The policy about variance to standard works independently of the cost breakdown policy.</span></span> <span data-ttu-id="82e21-138">Voit siis toisin sanoen valita kustannuserittelykäytännöksi **Ei mitään** ja varianssit kustannusryhmittäin niin, että tuotannon varianssit kerätään silti kustannusryhmittäin.</span><span class="sxs-lookup"><span data-stu-id="82e21-138">In other words, you can select a cost breakdown policy of **None** and select variances per cost group, so that production variances by cost group will still be captured.</span></span>

<span data-ttu-id="82e21-139">**5. Luo kustannuslaskentaversiot standardikustannuksia varten.**</span><span class="sxs-lookup"><span data-stu-id="82e21-139">**5. Create costing versions for standard costs.**</span></span> 

<span data-ttu-id="82e21-140">Luo **Kustannuslaskentaversion määritys** -sivulla standardikustannuksille vähintään yksi kustannuslaskentaversio.</span><span class="sxs-lookup"><span data-stu-id="82e21-140">Use the **Costing version setup** page to create one or more costing versions for standard costs.</span></span> <span data-ttu-id="82e21-141">Jokaisen kustannuslaskentaversion määritys on tehtävä **Standardikustannus**-kustannuslaskentatyypillä ja kustannustietojen sisällyttäminen on sallittava.</span><span class="sxs-lookup"><span data-stu-id="82e21-141">Each costing version must be designated by a costing type of **Standard cost** and must allow content to include cost data.</span></span>

<span data-ttu-id="82e21-142">**6. Valmistele aiemmin luotu asiakas käyttämään standardikustannuksia.**</span><span class="sxs-lookup"><span data-stu-id="82e21-142">**6. Prepare an existing customer to use standard costs.**</span></span> 

<span data-ttu-id="82e21-143">Jos asiakas haluaa muuttaa aiemmin luodut nimikkeensä standardikustannusvarastomallin mukaisiksi, hänen on käytettävä **Standardikustannusmuunnot**-sivua.</span><span class="sxs-lookup"><span data-stu-id="82e21-143">Customers who want to change their existing items to a standard cost inventory model must use the **Standard cost conversions** page.</span></span>


<a name="related-topics"></a><span data-ttu-id="82e21-144">Liittyvät aiheet</span><span class="sxs-lookup"><span data-stu-id="82e21-144">Related topics</span></span>
--------

[<span data-ttu-id="82e21-145">Standardikustannuksen muuntamisen yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="82e21-145">Standard cost conversion overview</span></span>](standard-cost-conversion-overview.md)


