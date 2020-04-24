---
title: Standardikustannusten edellytykset – yleiskatsaus
description: Tässä ohjeaiheessa käsitellään standardikustannusten käyttämiseen liittyvät perusvaiheet.
author: AndersGirke
manager: tfehr
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventStdCostConv, CostingVersion
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f66f7061c608379689016e3c0b9c5ba4ad23dc9e
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/02/2020
ms.locfileid: "3214507"
---
# <a name="prerequisites-for-standard-costs-overview"></a><span data-ttu-id="b2f95-103">Standardikustannusten edellytykset – yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="b2f95-103">Prerequisites for standard costs overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b2f95-104">Tässä ohjeaiheessa käsitellään standardikustannusten käyttämiseen liittyvät perusvaiheet.</span><span class="sxs-lookup"><span data-stu-id="b2f95-104">This topic describes the basic steps for using standard costs.</span></span> <span data-ttu-id="b2f95-105">Sen jälkeen vaiheet määräytyvät yrityksen työvaiheiden mukaan.</span><span class="sxs-lookup"><span data-stu-id="b2f95-105">Subsequent steps depend on the company's operations.</span></span> <span data-ttu-id="b2f95-106">Vaiheet ovat esimerkiksi erilaiset muussa kuin valmistusympäristössä, valmistusympäristössä ilman työvaiheistuksia ja valmistusympäristössä, jossa käytetään työvaiheistuksia.</span><span class="sxs-lookup"><span data-stu-id="b2f95-106">For example, the steps differ for a nonmanufacturing environment, a manufacturing environment that doesn't use routings, and a manufacturing environment that uses routings.</span></span> 

<span data-ttu-id="b2f95-107">Voit määrittää standardikustannukset seuraavien ohjeiden mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="b2f95-107">To set up standard costs, follow these steps.</span></span>

<span data-ttu-id="b2f95-108">**1. Luo nimikemalliryhmä standardikustannuksia varten.**</span><span class="sxs-lookup"><span data-stu-id="b2f95-108">**1. Create an item model group for standard costs.**</span></span>

<span data-ttu-id="b2f95-109">Luo **Nimikemalliryhmät** -sivulla uusi standardikustannusten ryhmä ja määritä **Standardikustannus**-varastomalli.</span><span class="sxs-lookup"><span data-stu-id="b2f95-109">Use the **Item model groups** page to create a new group for standard costs, and assign an inventory model of **Standard cost**.</span></span> <span data-ttu-id="b2f95-110">Nimikkeen malliryhmän tunnuksen on oltava kuvaileva, kuten **Std-kustannus**.</span><span class="sxs-lookup"><span data-stu-id="b2f95-110">The identifier for the item model group should be meaningful, such as **Std Cost**.</span></span> <span data-ttu-id="b2f95-111">Valitse valintaruudut ilmaisemaan, että ryhmä sallii negatiivisen kirjanpitovaraston ja että sen on kirjattava varastotilanne ja kirjanpitovarasto.</span><span class="sxs-lookup"><span data-stu-id="b2f95-111">Select the check boxes to indicate that the group should allow financial negative inventory, and that it should post physical inventory and financial inventory.</span></span> <span data-ttu-id="b2f95-112">Tämä standardikustannusryhmä määritetään nimikkeille.</span><span class="sxs-lookup"><span data-stu-id="b2f95-112">This standard cost group will be assigned to items.</span></span>

<span data-ttu-id="b2f95-113">**2. Määritä standardikustannusvariansseihin liittyvät kirjanpitotilit.**</span><span class="sxs-lookup"><span data-stu-id="b2f95-113">**2. Define ledger accounts that are related to standard cost variances.**</span></span> 

<span data-ttu-id="b2f95-114">Määritä standardikustannusvariansseihin liittyvät kirjanpitotilit **Tilikartta**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="b2f95-114">Use the **Chart of accounts** page to define ledger accounts that are related to standard cost variances.</span></span> <span data-ttu-id="b2f95-115">Nämä kirjanpitotilit täytyy määrittää, ennen kuin ne voi määrittää **Kirjaus**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="b2f95-115">These ledger accounts must be defined before they can be assigned on the **Posting** page.</span></span> <span data-ttu-id="b2f95-116">Kirjanpitotilit voivat kuvastaa nimikeryhmiä ja kustannusryhmiä.</span><span class="sxs-lookup"><span data-stu-id="b2f95-116">The ledger accounts can reflect item groups and cost groups.</span></span>

<span data-ttu-id="b2f95-117">**3. Määritä standardikustannusvariansseihin liittyvät tilit varastokirjauksiin.**</span><span class="sxs-lookup"><span data-stu-id="b2f95-117">**3. Assign ledger accounts to item postings that are related to standard cost variances.**</span></span> 

<span data-ttu-id="b2f95-118">Määritä standardikustannusvariansseihin liittyvät kirjanpitotilit **Kirjaus**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="b2f95-118">Use the **Posting** page to assign the ledger accounts that are related to standard cost variances.</span></span> <span data-ttu-id="b2f95-119">Voit määrittää varianssin kirjanpitotilin nimikkeen (tai nimikeryhmän) ja kustannusryhmän (tai kustannusryhmän tyypin) mukaan. Vaihtoehtoisesti voit määrittää, että kirjanpitotilit koskevat kaikkia nimikkeitä ja kaikkia kustannusryhmiä.</span><span class="sxs-lookup"><span data-stu-id="b2f95-119">You can specify a variance's ledger account by item (or item group) and by cost group (or cost group type), or you can specify that the ledger account applies to all items and all cost groups.</span></span> <span data-ttu-id="b2f95-120">Nämä vaihtoehdot vastaavat taulukoiden, ryhmien sekä kaikkien kohteiden kustannussuhteita.</span><span class="sxs-lookup"><span data-stu-id="b2f95-120">These options correspond to cost relations for tables, groups, and all.</span></span> 

<span data-ttu-id="b2f95-121">Voit ottaa kustannussuhteet käyttöön (taulukoissa, ryhmissä ja kaikissa kohteissa) **Tapahtumayhdistelmät**-sivulla ennen nimikekirjaussääntöjen määrittämistä.</span><span class="sxs-lookup"><span data-stu-id="b2f95-121">Before you define the item posting rules, use the **Transaction combinations** page to enable cost relations (for tables, groups, and all).</span></span>

<span data-ttu-id="b2f95-122">**4. Määritä standardikustannuksiin liittyvät varastoparametrit.**</span><span class="sxs-lookup"><span data-stu-id="b2f95-122">**4. Define inventory parameters that are related to standard costs.**</span></span> 

-  <span data-ttu-id="b2f95-123">Määritä **Varastokirjanpitokäytänteiden järjestelmä**-sivun **Tuoterakenne**-välilehdellä kaksi standardikustannuksiin liittyvää parametria.</span><span class="sxs-lookup"><span data-stu-id="b2f95-123">Use the **Inventory accounting** tab on the **Inventory accounting policies setup > Parameters** page to define two cost control parameters that are related to standard costs.</span></span>

    -  <span data-ttu-id="b2f95-124">Valitse **Kustannuserittely**-kentässä voit valita arvoksi **Ei mitään** tai **Alakirjanpito**.</span><span class="sxs-lookup"><span data-stu-id="b2f95-124">In the **Cost breakdown** field, select **None** or **Sub ledger**.</span></span> <span data-ttu-id="b2f95-125">Jos valitset **Alakirjanpito**, kustannuserittely on *aktiivinen* kustannuserittely.</span><span class="sxs-lookup"><span data-stu-id="b2f95-125">If you select **Sub ledger**, the cost breakdown is an *active* cost breakdown.</span></span> <span data-ttu-id="b2f95-126">Aktiivista kustannusseurantaa tarvitaan välttämättä, kun kustannusryhmien segmentointi lasketaan, säilytetään ja otetaan tarkasteluun monitasoisessa tuoterakenteessa standardikustannusnimikkeitä varten.</span><span class="sxs-lookup"><span data-stu-id="b2f95-126">An active cost breakdown is critical for calculating, retaining, and viewing cost group segmentation across a multilevel product structure for standard cost items.</span></span> <span data-ttu-id="b2f95-127">Kun kustannuserittely on aktiivinen, voit tehdä kustannusryhmäkohtaisia analyyseja ja raportteja varastoon liittyvistä tiedoista, keskeneräisistä töistä (KET-töistä) ja myytyjen tuotteiden kustannuksista (MTKUST) yksitasoisessa ja monitasoisessa muodossa sekä summamuodossa.</span><span class="sxs-lookup"><span data-stu-id="b2f95-127">When the cost breakdown is active, you can report and analyze inventory, work in process (WIP), and cost of goods sold (COGS) per cost group in a single-level, multilevel, or total format.</span></span> <span data-ttu-id="b2f95-128">Kun kustannuserittely on aktiivinen, valmistetun nimikkeen kustannuksen aktivointi aiheuttaa kustannusryhmän segmentoinnin tallentamisen nimikkeen kustannustietoihin.</span><span class="sxs-lookup"><span data-stu-id="b2f95-128">When the cost breakdown is active, if you activate a manufactured item's cost, the cost group segmentation will be stored in the item's cost record.</span></span> 

    -  <span data-ttu-id="b2f95-129">Jos valitset **Ei mitään**, standardikustannusnimikkeiden kustannusryhmäsegmentointia ei ylläpidetä.</span><span class="sxs-lookup"><span data-stu-id="b2f95-129">If you select **None**, cost group segmentation won't be maintained for standard cost items.</span></span> <span data-ttu-id="b2f95-130">Toisin sanoen valmistetun nimikkeen standardikustannus lasketaan ja ylläpidetään yksittäisenä summana ilman kustannusryhmän segmentointia.</span><span class="sxs-lookup"><span data-stu-id="b2f95-130">In other words, a manufactured item's standard cost will be calculated and maintained as a single amount, without cost group segmentation.</span></span> <span data-ttu-id="b2f95-131">Valmistettujen osien kustannusvaikutukset yhdistetään yhteen summaan.</span><span class="sxs-lookup"><span data-stu-id="b2f95-131">The cost contributions of manufactured components will be aggregated into the single amount.</span></span>

-  <span data-ttu-id="b2f95-132">Valitse **Vakio-varianssit**-kentässä **Yhteensä** tai **Kustannusryhmittäin**.</span><span class="sxs-lookup"><span data-stu-id="b2f95-132">In the **Variances to standard** field, select **Summarized** or **Per cost group**.</span></span> <span data-ttu-id="b2f95-133">Jos valitset **Kustannusryhmittäin**, voit tunnistaa ostohinnan varianssit ja tuotannon varianssit kustannusryhmittäin.</span><span class="sxs-lookup"><span data-stu-id="b2f95-133">If you select **Per cost group**, you can identify purchase price variances and production variances by cost group.</span></span> <span data-ttu-id="b2f95-134">Voit myös määrittää neljäntyyppisiä tuotannon variansseja: erän koon, määrän, hinnan ja korvauksen varianssi.</span><span class="sxs-lookup"><span data-stu-id="b2f95-134">You can also identify the four types of production variances: the lot size, quantity, price, and substitution variances.</span></span> <span data-ttu-id="b2f95-135">Jos valitset **Yhteensä**, et voi määrittää variansseja kustannusryhmittäin etkä tunnistaa tuotannon varianssien neljää tyyppiä.</span><span class="sxs-lookup"><span data-stu-id="b2f95-135">If you select **Summarized**, you can't identify variances by cost group, and you can't identify the four types of production variances.</span></span> <span data-ttu-id="b2f95-136">Voit tarkastella vain tuotannon varianssien yhteenvetoa.</span><span class="sxs-lookup"><span data-stu-id="b2f95-136">You can just view a summarized production variance.</span></span>

-  <span data-ttu-id="b2f95-137">Vakiovarianssia koskeva käytäntö on erillinen kustannuserittelykäytännöstä.</span><span class="sxs-lookup"><span data-stu-id="b2f95-137">The policy about variance to standard works independently of the cost breakdown policy.</span></span> <span data-ttu-id="b2f95-138">Voit siis toisin sanoen valita kustannuserittelykäytännöksi **Ei mitään** ja varianssit kustannusryhmittäin niin, että tuotannon varianssit kerätään silti kustannusryhmittäin.</span><span class="sxs-lookup"><span data-stu-id="b2f95-138">In other words, you can select a cost breakdown policy of **None** and select variances per cost group, so that production variances by cost group will still be captured.</span></span>

<span data-ttu-id="b2f95-139">**5. Luo kustannuslaskentaversiot standardikustannuksia varten.**</span><span class="sxs-lookup"><span data-stu-id="b2f95-139">**5. Create costing versions for standard costs.**</span></span> 

<span data-ttu-id="b2f95-140">Luo **Kustannuslaskentaversion määritys** -sivulla standardikustannuksille vähintään yksi kustannuslaskentaversio.</span><span class="sxs-lookup"><span data-stu-id="b2f95-140">Use the **Costing version setup** page to create one or more costing versions for standard costs.</span></span> <span data-ttu-id="b2f95-141">Jokaisen kustannuslaskentaversion määritys on tehtävä **Standardikustannus**-kustannuslaskentatyypillä ja kustannustietojen sisällyttäminen on sallittava.</span><span class="sxs-lookup"><span data-stu-id="b2f95-141">Each costing version must be designated by a costing type of **Standard cost** and must allow content to include cost data.</span></span>

<span data-ttu-id="b2f95-142">**6. Valmistele aiemmin luotu asiakas käyttämään standardikustannuksia.**</span><span class="sxs-lookup"><span data-stu-id="b2f95-142">**6. Prepare an existing customer to use standard costs.**</span></span> 

<span data-ttu-id="b2f95-143">Jos asiakas haluaa muuttaa aiemmin luodut nimikkeensä standardikustannusvarastomallin mukaisiksi, hänen on käytettävä **Standardikustannusmuunnot**-sivua.</span><span class="sxs-lookup"><span data-stu-id="b2f95-143">Customers who want to change their existing items to a standard cost inventory model must use the **Standard cost conversions** page.</span></span>


<a name="related-topics"></a><span data-ttu-id="b2f95-144">Liittyvät aiheet</span><span class="sxs-lookup"><span data-stu-id="b2f95-144">Related topics</span></span>
--------

[<span data-ttu-id="b2f95-145">Standardikustannuksen muuntamisen yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="b2f95-145">Standard cost conversion overview</span></span>](standard-cost-conversion-overview.md)

### <a name="blogs"></a><span data-ttu-id="b2f95-146">Blogit</span><span class="sxs-lookup"><span data-stu-id="b2f95-146">Blogs</span></span>

#### <a name="community-blogs"></a><span data-ttu-id="b2f95-147">Yhteisöblogit</span><span class="sxs-lookup"><span data-stu-id="b2f95-147">Community blogs</span></span>

- [<span data-ttu-id="b2f95-148">Suorien materiaalien standardikustannusten määrittäminen Dynamics 365 for Finance and Operationsissa</span><span class="sxs-lookup"><span data-stu-id="b2f95-148">How to set up standard costs for direct materials in Dynamics 365 for Finance and Operations</span></span>](https://financefunction.tech/2018/06/07/how-to-set-up-standard-costs-for-direct-materials-in-dynamics-365-for-finance-and-operations)
- [<span data-ttu-id="b2f95-149">Vakiintuneet välittömät työkustannukset Dynamics 365 for Finance and Operationsissa</span><span class="sxs-lookup"><span data-stu-id="b2f95-149">Standard direct labor costs in Dynamics 365 for Finance and Operations</span></span>](https://financefunction.tech/2018/07/16/standard-direct-labor-cost-in-dynamics-365-for-finance-and-operations)
