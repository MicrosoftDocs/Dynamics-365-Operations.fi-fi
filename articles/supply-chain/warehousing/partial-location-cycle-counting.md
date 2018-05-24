---
title: Sijainnin osittainen inventointi
description: "Inventointisuunnitelmat ohjaavat varsinaista inventointia. Voit pyytää vain tiettyjen tuotteiden tai tuotevarianttien inventointia sen sijaan, että toimipaikan koko käytettävissä oleva varasto inventoitaisiin."
author: perlynne
manager: AnnBe
ms.date: 11/02/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSCycleCountPlan, WHSWorkLineCycleCount, WHSWorkTemplateLineGroup, WHSWorkTemplateTable
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 643d9a07681beeffe90f39e5a0dc5ed9ad71b097
ms.contentlocale: fi-fi
ms.lasthandoff: 05/08/2018

---

# <a name="partial-location-cycle-counting"></a><span data-ttu-id="e1291-104">Sijainnin osittainen inventointi</span><span class="sxs-lookup"><span data-stu-id="e1291-104">Partial location cycle counting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e1291-105">Inventointisuunnitelmat ohjaavat varsinaista inventointia.</span><span class="sxs-lookup"><span data-stu-id="e1291-105">Cycle count plans guide the actual counting operations.</span></span> <span data-ttu-id="e1291-106">Voit pyytää vain tiettyjen tuotteiden tai tuotevarianttien inventointia sen sijaan, että toimipaikan koko käytettävissä oleva varasto inventoitaisiin.</span><span class="sxs-lookup"><span data-stu-id="e1291-106">You can request that only specific products and product variants be counted instead of all on-hand inventory in a location.</span></span>

<span data-ttu-id="e1291-107">Kun inventointityö luodaan inventointisuunnitelmien avulla, voit ohjata varsinaisia inventointitoimenpiteitä.</span><span class="sxs-lookup"><span data-stu-id="e1291-107">By using cycle count plans to create counting work, you can guide the actual counting operations.</span></span> <span data-ttu-id="e1291-108">Voit pyytää vain tiettyjen tuotteiden tai tuotevarianttien inventointia sen sijaan, että toimipaikan koko käytettävissä oleva varasto inventoitaisiin.</span><span class="sxs-lookup"><span data-stu-id="e1291-108">You can request that only specific products and product variants be counted instead of all on-hand inventory in a location.</span></span> <span data-ttu-id="e1291-109">Tiettyjen tuotteiden suodattaminen auttaa varastopäällikköä pienentämään tarkistuksen yleiskustannuksia, välttämään konsolidointi virheitä ja säästämään aikaa.</span><span class="sxs-lookup"><span data-stu-id="e1291-109">By filtering on specific products, the warehouse manager can reduce review overhead, avoid consolidation mistakes, and save time.</span></span>

## <a name="how-to-configure-partial-location-cycle-counting"></a><span data-ttu-id="e1291-110">Toimipaikan osittaisen inventoinnin määrittäminen</span><span class="sxs-lookup"><span data-stu-id="e1291-110">How to configure partial location cycle counting</span></span>
<span data-ttu-id="e1291-111">Kun inventoinnin työvaiheissa käytetään varastotyöprosessia, kullekin sijainnille luodaan työotsikko.</span><span class="sxs-lookup"><span data-stu-id="e1291-111">When you use the warehouse work process for counting operations, a work header is created for each location.</span></span> <span data-ttu-id="e1291-112">Kun määrität inventointisuunnitelmaa, voit rajoittaa luotavan inventointityön määrää käyttämällä **Valitse sijainnit** -kyselyä.</span><span class="sxs-lookup"><span data-stu-id="e1291-112">When you define the cycle count plan, you can use the **Select locations** query to limit the cycle counting work that is created.</span></span> <span data-ttu-id="e1291-113">Kun valitset inventointisuunnitelman tuotteita, voit tarkentaa inventointia valitsemalla sekä tuote- että tuotevarianttikyselyn.</span><span class="sxs-lookup"><span data-stu-id="e1291-113">When you select products for the cycle count plan, you can select both product and product variant queries to refine what is counted.</span></span> 

<span data-ttu-id="e1291-114">Voit liittää **työmallin** inventointisuunnitelmaan määrittämään, miten inventointityö on luotava.</span><span class="sxs-lookup"><span data-stu-id="e1291-114">You can associate a **work template** with a cycle count plan to define how the cycle count work should be created.</span></span> <span data-ttu-id="e1291-115">Inventointitoimenpiteiden työmalliin on suora viittaus inventointisuunnitelmasta.</span><span class="sxs-lookup"><span data-stu-id="e1291-115">The work template for counting operations is directly referenced from the cycle count plan.</span></span> 

<span data-ttu-id="e1291-116">Voit käyttää työmallin tietojen määrittämiseen **Työrivin tauot** -asetusta. Voit määrittää tällä asetuksella, onko inventointityörivit ryhmiteltävä nimike- vai tuotevarianttitunnuksen mukaan.</span><span class="sxs-lookup"><span data-stu-id="e1291-116">When you define the work template details, you can use the **Work line breaks** option to specify whether the counting work lines must be grouped by item number or product variant number.</span></span> <span data-ttu-id="e1291-117">Tämä asetus on pakollinen, jos haluat inventoida sijainnissa vain tietyt käytettävissä olevan varaston tuotteet.</span><span class="sxs-lookup"><span data-stu-id="e1291-117">This setup is required if you want to count on-hand inventory only for specific products in a location.</span></span> <span data-ttu-id="e1291-118">Luoduilla inventointityöriveillä on tässä määritettävä tietotaso ja ohjattu inventointi käsitellään tämän tason perusteella.</span><span class="sxs-lookup"><span data-stu-id="e1291-118">The cycle counting work lines that are created will have the level of information that you define here, and the guided counting operation will be handled based on this level.</span></span> 

<span data-ttu-id="e1291-119">Jos liität inventointisuunnitelmat työmalleihin **Työrivin tauot** -asetuksella, luodulle inventointityölle valitaan **Osittainen inventointi** -kenttä ja useita inventointityörivejä luodaan työmallin määritelmän perusteella.</span><span class="sxs-lookup"><span data-stu-id="e1291-119">If you associate cycle count plans with work templates by using the **Work lines breaks** option, the **Partial cycle count** field is selected for the cycle counting work that is created, and multiple cycle counting work lines will be created based on the definition of the work template.</span></span> 

<span data-ttu-id="e1291-120">Ennen osittaisen inventointityön käsittelyä mobiililaitteen valikosta on valittava ainakin **Näytä nimiketunnus** inventointiasetusten osana.</span><span class="sxs-lookup"><span data-stu-id="e1291-120">Before partial cycle count work can be processed, you must, at a minimum, select **Display item number** for the mobile device menu item as part of the cycle counting setup.</span></span> <span data-ttu-id="e1291-121">Varastotyöntekijää pyydetään kirjaamaan vain inventointiriveihin liittyvät inventointitiedot (nimiketunnukset ja tuotedimensiot).</span><span class="sxs-lookup"><span data-stu-id="e1291-121">The warehouse operator will be asked to record only counting information that is related to the counting lines (item numbers and product dimensions).</span></span> <span data-ttu-id="e1291-122">Muu käytettävissä oleva varasto ohitetaan tässä inventointiprosessissa.</span><span class="sxs-lookup"><span data-stu-id="e1291-122">All other on-hand inventory will be ignored for this counting process.</span></span> 

<span data-ttu-id="e1291-123">Osittaisessa inventointiprosessissa sijainnin **Edellinen inventointi** -asetuksen päivämäärää ja kellonaikaa ei päivitetä,</span><span class="sxs-lookup"><span data-stu-id="e1291-123">For the partial cycle count process, the **Last cycle count** date/time won’t be updated for the location.</span></span>

## <a name="example"></a><span data-ttu-id="e1291-124">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="e1291-124">Example</span></span>
<span data-ttu-id="e1291-125">Tässä esimerkissä vain nimiketunnus A0001 on inventoitava varastossa 61.</span><span class="sxs-lookup"><span data-stu-id="e1291-125">For this example, only item number A0001 must be counted in warehouse 61.</span></span>

1.  <span data-ttu-id="e1291-126">Inventoinnille luodaan uusi työmalli.</span><span class="sxs-lookup"><span data-stu-id="e1291-126">A new work template for cycle counting is created.</span></span> <span data-ttu-id="e1291-127">**Työrivin tauot** -asetus ryhmittelee inventointityörivit nimiketunnuksen mukaan.</span><span class="sxs-lookup"><span data-stu-id="e1291-127">The **Work line breaks** option is used to group counting work lines by item number.</span></span> <span data-ttu-id="e1291-128">Tämän vuoksi luodussa inventointityössä on nimiketunnuskohtaiset rivit.</span><span class="sxs-lookup"><span data-stu-id="e1291-128">Therefore, the cycle counting work that is created will have lines per item number.</span></span> <span data-ttu-id="e1291-129">Voit ryhmittää rivit myös tuotevarianttitunnuksen mukaan.</span><span class="sxs-lookup"><span data-stu-id="e1291-129">You can also group the lines by product variant number.</span></span>
2.  <span data-ttu-id="e1291-130">Luodaan uusi inventointisuunnitelma, joka viittaa juuri luotuun työmalliin.</span><span class="sxs-lookup"><span data-stu-id="e1291-130">A new cycle counting plan is created that references the newly created work template.</span></span> <span data-ttu-id="e1291-131">Inventointisuunnitelma sisältää kaikki varaston 61 sijainnit (**Valitse sijainnit** -kysely), joissa on varastossa nimiketunnusta A0001.</span><span class="sxs-lookup"><span data-stu-id="e1291-131">The cycle counting plan includes all locations in warehouse 61 (**Select locations** query) that hold inventory for item number A0001.</span></span> <span data-ttu-id="e1291-132">Tiettyjen tuotteiden valinta on määritetty **Inventoinnin tuotevalinnat** -osassa.</span><span class="sxs-lookup"><span data-stu-id="e1291-132">The selection of specific products is defined in the **Cycle count product selections** section.</span></span>
3.  <span data-ttu-id="e1291-133">Voit valita inventointisuunnitelman tuotteet valitsemalla **Tyhjät sijainnit** -kentän arvoksi **Älä sisällytä tyhjiä**.</span><span class="sxs-lookup"><span data-stu-id="e1291-133">You can select products for cycle counting plans by setting the **Empty locations** field to **Exclude empty**.</span></span> <span data-ttu-id="e1291-134">Kun inventointisuunnitelma käsitellään, luodaan nimiketunnuksen A0001 osittainen inventointityö.</span><span class="sxs-lookup"><span data-stu-id="e1291-134">When the cycle counting plan is processed, partial cycle count work for item number A0001 is created.</span></span> <span data-ttu-id="e1291-135">Varsinainen inventointiprosessi voidaan suorittaa käyttämällä ohjatun inventoinnin mobiililaitteen valikkovaihtoehtoa.</span><span class="sxs-lookup"><span data-stu-id="e1291-135">The actual counting process can be performed by using a mobile device menu item for guided cycle counting.</span></span>



<a name="additional-resources"></a><span data-ttu-id="e1291-136">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="e1291-136">Additional resources</span></span>
--------

[<span data-ttu-id="e1291-137">Inventointi</span><span class="sxs-lookup"><span data-stu-id="e1291-137">Cycle counting</span></span>](cycle-counting.md)


