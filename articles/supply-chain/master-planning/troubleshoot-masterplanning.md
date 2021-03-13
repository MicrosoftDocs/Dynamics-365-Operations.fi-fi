---
title: Pääsuunnittelun vianmääritys
description: Tässä aiheessa käsitellään sellaisten ongelmien korjaamista, joita pääsuunnittelun käytössä voi esiintyä.
author: SmithaNataraj
manager: tfehr
ms.date: 11/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-11-04
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 44291f5bcd9ffedf717150f8efe32e9eeda02f2e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "5011344"
---
# <a name="troubleshoot-master-planning"></a><span data-ttu-id="de64a-103">Pääsuunnittelun vianmääritys</span><span class="sxs-lookup"><span data-stu-id="de64a-103">Troubleshoot master planning</span></span>

<span data-ttu-id="de64a-104">Tässä aiheessa käsitellään sellaisten ongelmien korjaamista, joita pääsuunnittelun käytössä voi esiintyä.</span><span class="sxs-lookup"><span data-stu-id="de64a-104">This topic describes how to fix issues that you might encounter while you work with master planning.</span></span>

## <a name="bill-of-materials-explosion-behaves-differently-for-firmed-production-orders-and-for-estimated-production-orders-for-manually-created-work"></a><span data-ttu-id="de64a-105">Tuoterakenteen hajotus toimii eri tavalla vahvistetuissa tuotantotilauksissa ja manuaalisesti luodun työn ennakkolasketuissa tuotantotilauksissa</span><span class="sxs-lookup"><span data-stu-id="de64a-105">Bill of materials explosion behaves differently for firmed production orders and for estimated production orders for manually created work.</span></span>

### <a name="issue-description"></a><span data-ttu-id="de64a-106">Ongelman kuvaus</span><span class="sxs-lookup"><span data-stu-id="de64a-106">Issue description</span></span>

<span data-ttu-id="de64a-107">Kun tuotantotilaus vahvistetaan, nimikkeitä ei hajoteta, kun tuoterakenne hajotetaan.</span><span class="sxs-lookup"><span data-stu-id="de64a-107">When a production order is firmed, the items aren't exploded when you explode the bill of materials (BOM).</span></span> <span data-ttu-id="de64a-108">Kun työtilaus kuitenkin luodaan manuaalisesti ja tuotantotilaukselle tehdään ennakkolaskenta, nimikkeet hajotetaan.</span><span class="sxs-lookup"><span data-stu-id="de64a-108">However, when you manually create a work order and then estimate the production order, the items are exploded.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="de64a-109">Ongelman ratkaisu</span><span class="sxs-lookup"><span data-stu-id="de64a-109">Issue resolution</span></span>

<span data-ttu-id="de64a-110">Järjestelmä toimii odotetusti.</span><span class="sxs-lookup"><span data-stu-id="de64a-110">The system is working as expected.</span></span> <span data-ttu-id="de64a-111">Tuotantotilausta vahvistettaessa tapahtuva hajotus osoittaa suunniteltuun tilaukseen, mutta ei vaikuta siltä, että suunniteltu tilaus on tällä hetkellä vahvistettu tässä tapauksessa.</span><span class="sxs-lookup"><span data-stu-id="de64a-111">The explosion that occurs when the production order is firmed will point to the planned order, but it doesn't appear that the planned order is currently firmed in this case.</span></span> <span data-ttu-id="de64a-112">Jos tuotantotilaus on kuitenkin ennakkolaskettu, hajotus käynnistetään vapautetusta tuotantotilauksesta, kun suunniteltua tilausta ei ole.</span><span class="sxs-lookup"><span data-stu-id="de64a-112">However, if the production order has been estimated, the explosion is triggered from the released production order where no planned order exists.</span></span>

## <a name="the-delay-value-isnt-updated-when-i-reschedule-a-planned-order"></a><span data-ttu-id="de64a-113">Viivearvo ei päivitetä, kun suunniteltu tilaus ajoitetaan uudelleen</span><span class="sxs-lookup"><span data-stu-id="de64a-113">The Delay value isn't updated when I reschedule a planned order.</span></span>

<span data-ttu-id="de64a-114">Päivitä suunniteltujen tilausten viive avaamalla suunnitellun tilauksen **Ajoitetaan uudelleen** -valintaikkuna.</span><span class="sxs-lookup"><span data-stu-id="de64a-114">To update the delay for planned orders, open the **Rescheduling** dialog box for the planned order.</span></span> <span data-ttu-id="de64a-115">Varmista **Hajotus**-pikavälilehdessä, että **Suorita hajotus uudelleenajoittamisen jälkeen** -vaihtoehdon asetuksena on *Kyllä*.</span><span class="sxs-lookup"><span data-stu-id="de64a-115">On the **Explosion** FastTab, make sure that the **Perform explosion after rescheduling** option is set to *Yes*.</span></span>

## <a name="production-scheduling-doesnt-consider-the-safety-margins-that-are-set-on-the-item-coverage-for-pegged-supply"></a><span data-ttu-id="de64a-116">Tuotannon ajoitus ei ota huomioon varmuusmarginaaleja, jotka on määritetty tarvekohdistetun nimikkeen kattavuudessa</span><span class="sxs-lookup"><span data-stu-id="de64a-116">Production scheduling doesn't consider the safety margins that are set on the item coverage for pegged supply.</span></span>

### <a name="issue-description"></a><span data-ttu-id="de64a-117">Ongelman kuvaus</span><span class="sxs-lookup"><span data-stu-id="de64a-117">Issue description</span></span>

<span data-ttu-id="de64a-118">Pääsuunnittelu ottaa varmuusmarginaalit huomioon.</span><span class="sxs-lookup"><span data-stu-id="de64a-118">Master planning considers the safety margins.</span></span> <span data-ttu-id="de64a-119">Varmuusmarginaalit kuitenkin ohitetaan, kun suunnittelut tuotantotilaukset ajoitetaan.</span><span class="sxs-lookup"><span data-stu-id="de64a-119">However, the safety margins are ignored when planned production orders are scheduled.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="de64a-120">Ongelman ratkaisu</span><span class="sxs-lookup"><span data-stu-id="de64a-120">Issue resolution</span></span>

<span data-ttu-id="de64a-121">Marginaalit otetaan huomioon vain pääsuunnittelun aikana mutta ei manuaalisen ajoituksen aikana.</span><span class="sxs-lookup"><span data-stu-id="de64a-121">Margins are considered only during master planning, not during manual scheduling.</span></span> <span data-ttu-id="de64a-122">Marginaalit suunnitellaan toimimaan puskureina suunnitteluvaiheen aikana tuomaan varsinaiseen prosessiin pelivaraa.</span><span class="sxs-lookup"><span data-stu-id="de64a-122">Margins are designed to act as a buffer during the planning phase, to give some "margin" for the actual process.</span></span>

<span data-ttu-id="de64a-123">Halutun tuloksen saa poistamalla marginaalin.</span><span class="sxs-lookup"><span data-stu-id="de64a-123">To get the desired result, you can remove the margin.</span></span> <span data-ttu-id="de64a-124">Reititys on päivitettävä sisältämään toivottu aika (esimerkiksi jonotusaikana):</span><span class="sxs-lookup"><span data-stu-id="de64a-124">The route must then be updated so that it includes the desired time (for example, as queue time).</span></span> <span data-ttu-id="de64a-125">Pääsuunnittelun ja manuaalisen ajoituksen tuloksen pitäisi sitten olla sama.</span><span class="sxs-lookup"><span data-stu-id="de64a-125">Both master planning and manual scheduling should then produce the same result.</span></span>

## <a name="planned-orders-are-generated-even-though-we-have-items-in-stock-and-production-orders-already-exist-for-them"></a><span data-ttu-id="de64a-126">Suunnitellut tilaukset luodaan, vaikka nimikkeitä on varastossa ja niillä on jo tuotantotilaukset.</span><span class="sxs-lookup"><span data-stu-id="de64a-126">Planned orders are generated even though we have items in stock and production orders already exist for them.</span></span>

<span data-ttu-id="de64a-127">Tämä ongelma on ehkä mahdollista korjata lisäämällä soveltuvien ryhmien **Positiiviset päivät** -arvoa **Kattavuusryhmä**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="de64a-127">You might be able to fix this issue by increasing the **Positive days** value for the relevant groups on the **Coverage group** page.</span></span> <span data-ttu-id="de64a-128">Tämä muutos saa järjestelmän määrittää, voiko käytettävissä olevaa varastoa käyttää kysyntään.</span><span class="sxs-lookup"><span data-stu-id="de64a-128">This change will cause the system to determine whether on-hand inventory can be used for the demand.</span></span> <span data-ttu-id="de64a-129">Silloin uutta suunniteltua tilausta ei luoda varastossa oleville nimikkeille.</span><span class="sxs-lookup"><span data-stu-id="de64a-129">Then a new planned order won't be generated for the items that are in stock.</span></span>

## <a name="master-planning-doesnt-seem-to-respect-capacity-limitations-and-is-scheduling-more-than-the-available-capacity"></a><span data-ttu-id="de64a-130">Pääsuunnittelu ei näytä noudattavan kapasiteettirajoituksia ja sen aikataulutus ylittää käytettävissä olevan kapasiteetin</span><span class="sxs-lookup"><span data-stu-id="de64a-130">Master planning doesn't seem to respect capacity limitations and is scheduling more than the available capacity.</span></span>

### <a name="issue-description"></a><span data-ttu-id="de64a-131">Ongelman kuvaus</span><span class="sxs-lookup"><span data-stu-id="de64a-131">Issue description</span></span>

<span data-ttu-id="de64a-132">Jos käytettävässä toiminnon aikatauluttamisessa on rajallinen kapasiteetti ja reititys määrittää yhdistelmätarpeet sekä resurssiryhmälle että yksittäisille resursseille, on olemassa pieni ylivarauksen mahdollisuus, joka johtuu algoritmin tavasta tarkistaa kapasiteettiristiriidat.</span><span class="sxs-lookup"><span data-stu-id="de64a-132">When you use operation scheduling where there is finite capacity, and where the route specifies a mix of requirements for both a resource group and individual resources, there is a small chance of overbooking because of the way that the algorithm validates for capacity conflicts.</span></span> <span data-ttu-id="de64a-133">Tämä ylivaraus voi esiintyä, kun pääsuunnittelun suorittamiseen käytetään lisätyöasemia.</span><span class="sxs-lookup"><span data-stu-id="de64a-133">This overbooking can occur when you use helpers to run master planning.</span></span> <span data-ttu-id="de64a-134">Se tapahtuu todennäköisimmin siinä tapauksessa, että useilla töillä on suhteellisen lyhyt suoritusaika.</span><span class="sxs-lookup"><span data-stu-id="de64a-134">It's most likely to occur if there are many jobs that have a relatively short runtime.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="de64a-135">Ongelman ratkaisu</span><span class="sxs-lookup"><span data-stu-id="de64a-135">Issue resolution</span></span>

<span data-ttu-id="de64a-136">Jos on ylivarauksia ei saa missään tapauksessa esiintyä toimintojen ajoittamisessa, voit tehdä pääsuunnittelun ajoituksesta yksisäikeisen ottamalla **Tarkka rajallinen kapasiteetti toimintojen ajoituksessa** -asetuksen käyttöön **Pääsuunnittelun parametrit** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="de64a-136">If it's essential that no overbooking occur for operation scheduling, you can make the scheduling part of master planning single-threaded by turning on the **Accurate finite capacity for Operation Scheduling** option on the **Master planning parameters** page.</span></span> <span data-ttu-id="de64a-137">Tämä asetus ei ole oletusarvoisesti käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="de64a-137">This option isn't available by default.</span></span> <span data-ttu-id="de64a-138">Se on lisättävä manuaalisesti sivulle mukautustoimintojen avulla.</span><span class="sxs-lookup"><span data-stu-id="de64a-138">You must manually add it to the page by using personalization features.</span></span> <span data-ttu-id="de64a-139">Tätä asetusta käytettäessä ajoitus hidastuu, koska rinnakkainen käsittely ei ole käytössä.</span><span class="sxs-lookup"><span data-stu-id="de64a-139">When you use this option, scheduling will run more slowly because of the lack of parallel processing.</span></span>

## <a name="planned-orders-take-a-long-time-to-update"></a><span data-ttu-id="de64a-140">Suunniteltujen tilausten päivittäminen kestää kauan</span><span class="sxs-lookup"><span data-stu-id="de64a-140">Planned orders take a long time to update.</span></span>

### <a name="issue-description"></a><span data-ttu-id="de64a-141">Ongelman kuvaus</span><span class="sxs-lookup"><span data-stu-id="de64a-141">Issue description</span></span>

<span data-ttu-id="de64a-142">Suunnittelun tilauksen tarpeen määrää ja/tai toimituspäivää päivitettäessä päivityksen tallentaminen kestää tilauskohtaisesti tyypillisesti vähintään 30 sekuntia.</span><span class="sxs-lookup"><span data-stu-id="de64a-142">When updating the requirement quantity and/or delivery date on a planned order, it typically takes at least 30 seconds per order to save the update.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="de64a-143">Ongelman ratkaisu</span><span class="sxs-lookup"><span data-stu-id="de64a-143">Issue resolution</span></span>

<span data-ttu-id="de64a-144">Tämä on tunnettu sisäisen pääsuunnittelumoduulin ongelma.</span><span class="sxs-lookup"><span data-stu-id="de64a-144">This is a known issue with the built-in master planning engine.</span></span> <span data-ttu-id="de64a-145">Se johtuu taustalla olevasta tuoterakenteen automaattisesta hajotuksesta muokkausten aikana.</span><span class="sxs-lookup"><span data-stu-id="de64a-145">It is caused by the underlying auto explosion through the BOM structure during edits.</span></span> <span data-ttu-id="de64a-146">Tämä ongelma korjataan suunnittelun optimoinnissa, jossa suunnittelija voi päivittää ja hyväksyä tilauksia ja sitten halutessaan käynnistää suunnitteluajon, joka päivittää taustatuoterakenteen suunnittelutilaukset.</span><span class="sxs-lookup"><span data-stu-id="de64a-146">This issue is addressed in Planning Optimization, where a planner can update and approve the relevant orders and, when desired, trigger a planning run to update planned orders for the underlying BOM structure.</span></span>

<span data-ttu-id="de64a-147">Sisäisen pääsuunnittelumoduulin suorituskykyä voi parantaa seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="de64a-147">One way to improve performance with the built-in master planning engine is to do the following:</span></span>

1. <span data-ttu-id="de64a-148">Siirry kohtaan **Pääsuunnittelu \> Määritykset \> Suunnitelmat \> Pääsuunnitelmat**.</span><span class="sxs-lookup"><span data-stu-id="de64a-148">Go to **Master planning \> Setup \> Plans \> Master plans**.</span></span>
1. <span data-ttu-id="de64a-149">Valitse suunnitelma.</span><span class="sxs-lookup"><span data-stu-id="de64a-149">Select a plan.</span></span>
1. <span data-ttu-id="de64a-150">Laajenna **Aikarajat päivissä** -pikavälilehti.</span><span class="sxs-lookup"><span data-stu-id="de64a-150">Expand the **Time fence in days** FastTab.</span></span>
1. <span data-ttu-id="de64a-151">Määritä **Hajotus**-asetukseksi *Kyllä* ja määritä tämän asetuksen alla olevaan kenttään 0 (nolla).</span><span class="sxs-lookup"><span data-stu-id="de64a-151">Set **Explosion** to *Yes*, and set the field below this setting to 0 (zero).</span></span>

> [!NOTE]
> <span data-ttu-id="de64a-152">Tämä rajoittaa kyseisessä pääsuunnitelmassa suoritetut hajotukset yhteen päivään.</span><span class="sxs-lookup"><span data-stu-id="de64a-152">This will limit the period for explosions performed for this master plan to a single day.</span></span>
