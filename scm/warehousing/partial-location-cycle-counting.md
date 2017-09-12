---
title: Sijainnin osittainen inventointi
description: "Inventointisuunnitelmat ohjaavat varsinaista inventointia. Voit pyytää vain tiettyjen tuotteiden tai tuotevarianttien inventointia sen sijaan, että toimipaikan koko käytettävissä oleva varasto inventoitaisiin."
author: perlynne
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
keywords: WHSCycleCountPlan WHSWorkLineCycleCount WHSWorkTemplateLineGroup, WHSWorkTemplateTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 2ee4de8eabc55271e272ca3026746787353f5fc3
ms.contentlocale: fi-fi
ms.lasthandoff: 07/18/2017

---

# <a name="partial-location-cycle-counting"></a><span data-ttu-id="a999e-105">Sijainnin osittainen inventointi</span><span class="sxs-lookup"><span data-stu-id="a999e-105">Partial location cycle counting</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="a999e-106">Inventointisuunnitelmat ohjaavat varsinaista inventointia.</span><span class="sxs-lookup"><span data-stu-id="a999e-106">Cycle count plans guide the actual counting operations.</span></span> <span data-ttu-id="a999e-107">Voit pyytää vain tiettyjen tuotteiden tai tuotevarianttien inventointia sen sijaan, että toimipaikan koko käytettävissä oleva varasto inventoitaisiin.</span><span class="sxs-lookup"><span data-stu-id="a999e-107">You can request that only specific products and product variants be counted instead of all on-hand inventory in a location.</span></span>

<span data-ttu-id="a999e-108">Kun inventointityö luodaan inventointisuunnitelmien avulla, voit ohjata varsinaisia inventointitoimenpiteitä.</span><span class="sxs-lookup"><span data-stu-id="a999e-108">By using cycle count plans to create counting work, you can guide the actual counting operations.</span></span> <span data-ttu-id="a999e-109">Voit pyytää vain tiettyjen tuotteiden tai tuotevarianttien inventointia sen sijaan, että toimipaikan koko käytettävissä oleva varasto inventoitaisiin.</span><span class="sxs-lookup"><span data-stu-id="a999e-109">You can request that only specific products and product variants be counted instead of all on-hand inventory in a location.</span></span> <span data-ttu-id="a999e-110">Tiettyjen tuotteiden suodattaminen auttaa varastopäällikköä pienentämään tarkistuksen yleiskustannuksia, välttämään konsolidointi virheitä ja säästämään aikaa.</span><span class="sxs-lookup"><span data-stu-id="a999e-110">By filtering on specific products, the warehouse manager can reduce review overhead, avoid consolidation mistakes, and save time.</span></span>

## <a name="how-to-configure-partial-location-cycle-counting"></a><span data-ttu-id="a999e-111">Toimipaikan osittaisen inventoinnin määrittäminen</span><span class="sxs-lookup"><span data-stu-id="a999e-111">How to configure partial location cycle counting</span></span>
<span data-ttu-id="a999e-112">Kun inventoinnin työvaiheissa käytetään varastotyöprosessia, kullekin sijainnille luodaan työotsikko.</span><span class="sxs-lookup"><span data-stu-id="a999e-112">When you use the warehouse work process for counting operations, a work header is created for each location.</span></span> <span data-ttu-id="a999e-113">Kun määrität inventointisuunnitelmaa, voit rajoittaa luotavan inventointityön määrää käyttämällä **Valitse sijainnit** -kyselyä.</span><span class="sxs-lookup"><span data-stu-id="a999e-113">When you define the cycle count plan, you can use the **Select locations** query to limit the cycle counting work that is created.</span></span> <span data-ttu-id="a999e-114">Kun valitset inventointisuunnitelman tuotteita, voit tarkentaa inventointia valitsemalla sekä tuote- että tuotevarianttikyselyn.</span><span class="sxs-lookup"><span data-stu-id="a999e-114">When you select products for the cycle count plan, you can select both product and product variant queries to refine what is counted.</span></span> 

<span data-ttu-id="a999e-115">Voit liittää **työmallin** inventointisuunnitelmaan määrittämään, miten inventointityö on luotava.</span><span class="sxs-lookup"><span data-stu-id="a999e-115">You can associate a **work template** with a cycle count plan to define how the cycle count work should be created.</span></span> <span data-ttu-id="a999e-116">Inventointitoimenpiteiden työmalliin on suora viittaus inventointisuunnitelmasta.</span><span class="sxs-lookup"><span data-stu-id="a999e-116">The work template for counting operations is directly referenced from the cycle count plan.</span></span> 

<span data-ttu-id="a999e-117">Voit käyttää työmallin tietojen määrittämiseen **Työrivin tauot** -asetusta. Voit määrittää tällä asetuksella, onko inventointityörivit ryhmiteltävä nimike- vai tuotevarianttitunnuksen mukaan.</span><span class="sxs-lookup"><span data-stu-id="a999e-117">When you define the work template details, you can use the **Work line breaks** option to specify whether the counting work lines must be grouped by item number or product variant number.</span></span> <span data-ttu-id="a999e-118">Tämä asetus on pakollinen, jos haluat inventoida sijainnissa vain tietyt käytettävissä olevan varaston tuotteet.</span><span class="sxs-lookup"><span data-stu-id="a999e-118">This setup is required if you want to count on-hand inventory only for specific products in a location.</span></span> <span data-ttu-id="a999e-119">Luoduilla inventointityöriveillä on tässä määritettävä tietotaso ja ohjattu inventointi käsitellään tämän tason perusteella.</span><span class="sxs-lookup"><span data-stu-id="a999e-119">The cycle counting work lines that are created will have the level of information that you define here, and the guided counting operation will be handled based on this level.</span></span> 

<span data-ttu-id="a999e-120">Jos liität inventointisuunnitelmat työmalleihin **Työrivin tauot** -asetuksella, luodulle inventointityölle valitaan **Osittainen inventointi** -kenttä ja useita inventointityörivejä luodaan työmallin määritelmän perusteella.</span><span class="sxs-lookup"><span data-stu-id="a999e-120">If you associate cycle count plans with work templates by using the **Work lines breaks** option, the **Partial cycle count** field is selected for the cycle counting work that is created, and multiple cycle counting work lines will be created based on the definition of the work template.</span></span> 

<span data-ttu-id="a999e-121">Ennen osittaisen inventointityön käsittelyä mobiililaitteen valikosta on valittava ainakin **Näytä nimiketunnus** inventointiasetusten osana.</span><span class="sxs-lookup"><span data-stu-id="a999e-121">Before partial cycle count work can be processed, you must, at a minimum, select **Display item number** for the mobile device menu item as part of the cycle counting setup.</span></span> <span data-ttu-id="a999e-122">Varastotyöntekijää pyydetään kirjaamaan vain inventointiriveihin liittyvät inventointitiedot (nimiketunnukset ja tuotedimensiot).</span><span class="sxs-lookup"><span data-stu-id="a999e-122">The warehouse operator will be asked to record only counting information that is related to the counting lines (item numbers and product dimensions).</span></span> <span data-ttu-id="a999e-123">Muu käytettävissä oleva varasto ohitetaan tässä inventointiprosessissa.</span><span class="sxs-lookup"><span data-stu-id="a999e-123">All other on-hand inventory will be ignored for this counting process.</span></span> 

<span data-ttu-id="a999e-124">Osittaisessa inventointiprosessissa sijainnin **Edellinen inventointi** -asetuksen päivämäärää ja kellonaikaa ei päivitetä,</span><span class="sxs-lookup"><span data-stu-id="a999e-124">For the partial cycle count process, the **Last cycle count** date/time won’t be updated for the location.</span></span>

## <a name="example"></a><span data-ttu-id="a999e-125">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="a999e-125">Example</span></span>
<span data-ttu-id="a999e-126">Tässä esimerkissä vain nimiketunnus A0001 on inventoitava varastossa 61.</span><span class="sxs-lookup"><span data-stu-id="a999e-126">For this example, only item number A0001 must be counted in warehouse 61.</span></span>

1.  <span data-ttu-id="a999e-127">Inventoinnille luodaan uusi työmalli.</span><span class="sxs-lookup"><span data-stu-id="a999e-127">A new work template for cycle counting is created.</span></span> <span data-ttu-id="a999e-128">**Työrivin tauot** -asetus ryhmittelee inventointityörivit nimiketunnuksen mukaan.</span><span class="sxs-lookup"><span data-stu-id="a999e-128">The **Work line breaks** option is used to group counting work lines by item number.</span></span> <span data-ttu-id="a999e-129">Tämän vuoksi luodussa inventointityössä on nimiketunnuskohtaiset rivit.</span><span class="sxs-lookup"><span data-stu-id="a999e-129">Therefore, the cycle counting work that is created will have lines per item number.</span></span> <span data-ttu-id="a999e-130">Voit ryhmittää rivit myös tuotevarianttitunnuksen mukaan.</span><span class="sxs-lookup"><span data-stu-id="a999e-130">You can also group the lines by product variant number.</span></span>
2.  <span data-ttu-id="a999e-131">Luodaan uusi inventointisuunnitelma, joka viittaa juuri luotuun työmalliin.</span><span class="sxs-lookup"><span data-stu-id="a999e-131">A new cycle counting plan is created that references the newly created work template.</span></span> <span data-ttu-id="a999e-132">Inventointisuunnitelma sisältää kaikki varaston 61 sijainnit (**Valitse sijainnit** -kysely), joissa on varastossa nimiketunnusta A0001.</span><span class="sxs-lookup"><span data-stu-id="a999e-132">The cycle counting plan includes all locations in warehouse 61 (**Select locations** query) that hold inventory for item number A0001.</span></span> <span data-ttu-id="a999e-133">Tiettyjen tuotteiden valinta on määritetty **Inventoinnin tuotevalinnat** -osassa.</span><span class="sxs-lookup"><span data-stu-id="a999e-133">The selection of specific products is defined in the **Cycle count product selections** section.</span></span>
3.  <span data-ttu-id="a999e-134">Voit valita inventointisuunnitelman tuotteet valitsemalla **Tyhjät sijainnit** -kentässä **Älä sisällytä tyhjiä**. Kun inventointisuunnitelma käsitellään, nimiketunnuksen A0001 osittainen inventointityö luodaan.</span><span class="sxs-lookup"><span data-stu-id="a999e-134">You can select products for cycle counting plans by setting the **Empty locations** field to **Exclude empty**.When the cycle counting plan is processed, partial cycle count work for item number A0001 is created.</span></span> <span data-ttu-id="a999e-135">Varsinainen inventointiprosessi voidaan suorittaa käyttämällä ohjatun inventoinnin mobiililaitteen valikkovaihtoehtoa.</span><span class="sxs-lookup"><span data-stu-id="a999e-135">The actual counting process can be performed by using a mobile device menu item for guided cycle counting.</span></span>



<a name="see-also"></a><span data-ttu-id="a999e-136">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="a999e-136">See also</span></span>
--------

[<span data-ttu-id="a999e-137">Inventointi</span><span class="sxs-lookup"><span data-stu-id="a999e-137">Cycle counting</span></span>](cycle-counting.md)


