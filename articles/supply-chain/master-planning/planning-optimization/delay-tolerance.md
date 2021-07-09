---
title: Viivetoleranssi (negatiiviset päivät)
description: Tässä ohjeaiheessa on tietoja viivetoleranssin laskennasta ja siitä, miten se vaikuttaa suunnitellun tilauksen luontiin suunnittelun optimoinnissa.
author: crytt
ms.date: 07/30/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-07-30
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 748e047e89747f2eabccc04a40c79bcb1e6f3dea
ms.sourcegitcommit: f21659f1c23bc2cd65bbe7fb7210910d5a8e1cb9
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/24/2021
ms.locfileid: "6306460"
---
# <a name="delay-tolerance-negative-days"></a><span data-ttu-id="30d1f-103">Viivetoleranssi (negatiiviset päivät)</span><span class="sxs-lookup"><span data-stu-id="30d1f-103">Delay tolerance (negative days)</span></span>

[!include [banner](../../includes/banner.md)]
[!INCLUDE [preview-banner](../../includes/preview-banner.md)]

<span data-ttu-id="30d1f-104">Viivetoleranssitoiminnon ansiosta suunnittelun optimointi voi ottaa huomioon kattavuusryhmille määritetyn **negatiivisten päivien** arvon.</span><span class="sxs-lookup"><span data-stu-id="30d1f-104">The delay tolerance functionality enables Planning Optimization to consider the **Negative days** value that is set for coverage groups.</span></span> <span data-ttu-id="30d1f-105">Sitä käytetään pääsuunnittelussa käytetyn viivetoleranssikauden pidennykseen.</span><span class="sxs-lookup"><span data-stu-id="30d1f-105">It's used to extend the delay tolerance period that is applied during master planning.</span></span> <span data-ttu-id="30d1f-106">Näin voidaan välttää uusien toimitustilausten luominen, jos olemassa oleva toimitus voi kattaa kysynnän lyhyen viiveen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="30d1f-106">In this way, you can avoid creating new supply orders if existing supply will be able to cover the demand after a short delay.</span></span> <span data-ttu-id="30d1f-107">Toiminnon tarkoitus on määrittää, onko tarpeen luoda uusi toimitustilaus annettua kysyntää varten.</span><span class="sxs-lookup"><span data-stu-id="30d1f-107">The purpose of the functionality is to determine whether it makes sense to create a new supply order for a given demand.</span></span>

## <a name="turn-on-the-feature-in-your-system"></a><span data-ttu-id="30d1f-108">Toiminnon ottaminen käyttöön järjestelmässä</span><span class="sxs-lookup"><span data-stu-id="30d1f-108">Turn on the feature in your system</span></span>

<span data-ttu-id="30d1f-109">Voit ottaa viivetoleranssin toiminnon käyttöön järjestelmässäsi valitsemalla [Ominaisuuksien hallinta](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ja ottamalla *Suunnittelun optimoinnin negatiiviset päivät* -ominaisuuden käyttöön.</span><span class="sxs-lookup"><span data-stu-id="30d1f-109">To make the delay tolerance functionality available in your system, go to [Feature management](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), and turn on the *Negative days for Planning Optimization* feature.</span></span>

## <a name="delay-tolerance-in-planning-optimization"></a><span data-ttu-id="30d1f-110">Suunnittelun optimoinnin viivetoleranssi</span><span class="sxs-lookup"><span data-stu-id="30d1f-110">Delay tolerance in Planning Optimization</span></span>

<span data-ttu-id="30d1f-111">Viivetoleranssi tarkoittaa läpimenoajan ylittävän päivien määrää, jonka olet valmis odottamaan ennen uuden täydennyksen tilaamista, kun olemassa oleva toimitus on jo suunniteltu.</span><span class="sxs-lookup"><span data-stu-id="30d1f-111">Delay tolerance represents the number of days beyond the lead time that you're willing to wait before you order new replenishment when existing supply is already planned.</span></span> <span data-ttu-id="30d1f-112">Viivetoleranssi määritetään käyttämällä kalenteripäiviä, ei työpäiviä.</span><span class="sxs-lookup"><span data-stu-id="30d1f-112">Delay tolerance is defined by using calendar days, not business days.</span></span>

<span data-ttu-id="30d1f-113">Kun pääsuunnittelun aikana järjestelmä laskee viivetoleranssin, se ottaa huomioon **negatiivisten päivien** asetuksen.</span><span class="sxs-lookup"><span data-stu-id="30d1f-113">At the time of master planning, when the system calculates the delay tolerance, it considers the **Negative days** setting.</span></span> <span data-ttu-id="30d1f-114">Voit määrittää **Negatiiviset päivät** -arvon joko **Kattavuusryhmät**- tai **Nimikkeen kattavuus** -sivuilla.</span><span class="sxs-lookup"><span data-stu-id="30d1f-114">You can set the **Negative days** value on either the **Coverage groups** page or the **Item coverage** page.</span></span>

<span data-ttu-id="30d1f-115">Järjestelmä linkittää viivetoleranssin laskennan *aikaisimpaan täydennyspäivämäärään*, joka on sama kuin tämän päivän päivämäärä plus läpimenoaika.</span><span class="sxs-lookup"><span data-stu-id="30d1f-115">The system links the delay tolerance calculation to the *earliest replenishment date*, which equals today's date plus the lead time.</span></span> <span data-ttu-id="30d1f-116">Viivetoleranssi lasketaan seuraavan kaavan avulla, jossa *max()* hakee suuremman kahdesta arvosta:</span><span class="sxs-lookup"><span data-stu-id="30d1f-116">The delay tolerance is calculated by using following formula, where *max()* finds the larger of two values:</span></span>

<span data-ttu-id="30d1f-117">*max(aikaisin täydennyspäivämäärä, kysynnän määräpäivä)* – *kysynnän määräpäivä* + *Negatiiviset päivät*</span><span class="sxs-lookup"><span data-stu-id="30d1f-117">*max(Earliest replenishment date, Demand due date)* – *Demand due date* + *Negative days*</span></span>

<span data-ttu-id="30d1f-118">Tällä kaavalla varmistetaan, että pääsuunnittelu ei luo uusia toimitustilauksia, kun toimituksia on tarpeeksi olemassa tuotteen läpimenoajan aikana.</span><span class="sxs-lookup"><span data-stu-id="30d1f-118">This formula ensures that master planning doesn't create new supply orders when enough supply exists during the product lead time.</span></span>

> [!NOTE]
> <span data-ttu-id="30d1f-119">Suunnittelun optimoinnin viivetoleranssin laskenta käyttää aina sisäänrakennetun pääsuunnittelun dynaamista negatiivisten päivien laskentaa.</span><span class="sxs-lookup"><span data-stu-id="30d1f-119">The delay tolerance calculation in Planning Optimization always uses the dynamic negative days calculation from built-in master planning.</span></span> <span data-ttu-id="30d1f-120">**Käytä dynaamisia negatiivisia päiviä** -asetus **Pääsuunnittelun parametrit** -sivulla ei vaikuta tähän käyttäytymiseen.</span><span class="sxs-lookup"><span data-stu-id="30d1f-120">The **Use dynamic negative days** setting on the **Master planning parameters** page has no effect on this behavior.</span></span>

<span data-ttu-id="30d1f-121">Jos nykyinen toimitus merkitsee kysynnän viivettä, joka on pienempi tai yhtä suuri kuin laskettu viivetoleranssi, suunnittelun optimointi sovittaa olemassa olevan toimituksen ja kysynnän.</span><span class="sxs-lookup"><span data-stu-id="30d1f-121">If the existing supply implies a demand delay that is less than or equal to the calculated delay tolerance, Planning Optimization pegs existing supply with the demand.</span></span> <span data-ttu-id="30d1f-122">Joissain tapauksissa on parempi viivyttää kysyntää kuin päätyä ylitarjontaan.</span><span class="sxs-lookup"><span data-stu-id="30d1f-122">In some cases, it's better to delay the demand than to end up with oversupply.</span></span>

<span data-ttu-id="30d1f-123">Seuraavissa osa-alueissa on esimerkkejä, jotka osoittavat, kuinka viivetoleranssi vaikuttaa suunniteltujen tilausten luontiin suunnittelun optimoinnissa.</span><span class="sxs-lookup"><span data-stu-id="30d1f-123">The following subsections provide examples that show how delay tolerance affects the creation of planned orders in Planning Optimization.</span></span>

### <a name="example-1"></a><span data-ttu-id="30d1f-124">Esimerkki 1</span><span class="sxs-lookup"><span data-stu-id="30d1f-124">Example 1</span></span>

<span data-ttu-id="30d1f-125">Tuotteella on seuraava konfiguraatio:</span><span class="sxs-lookup"><span data-stu-id="30d1f-125">A product has the following configuration:</span></span>

- <span data-ttu-id="30d1f-126">**Läpimenoaika:** *10*</span><span class="sxs-lookup"><span data-stu-id="30d1f-126">**Lead time:** *10*</span></span>
- <span data-ttu-id="30d1f-127">**Negatiiviset päivät:** *2*</span><span class="sxs-lookup"><span data-stu-id="30d1f-127">**Negative days:** *2*</span></span>

<span data-ttu-id="30d1f-128">Tuotteella on seuraava tarjonta ja kysyntä:</span><span class="sxs-lookup"><span data-stu-id="30d1f-128">The following supply and demand exist for the product:</span></span>

- <span data-ttu-id="30d1f-129">**Tämän päivän kysyntä:** myyntitilaus, jonka määrä on 10</span><span class="sxs-lookup"><span data-stu-id="30d1f-129">**Demand for today:** A sales order for a quantity of 10</span></span>
- <span data-ttu-id="30d1f-130">**Toimitus 12 päivän sisällä:** ostotilaus, jonka määrä on 10</span><span class="sxs-lookup"><span data-stu-id="30d1f-130">**Supply in 12 days:** A purchase order for a quantity of 10</span></span>

<span data-ttu-id="30d1f-131">Olemassa oleva tarjonta voi kattaa kysynnän 12 päivän kuluessa ja että kausi on sama kuin viivetoleranssi.</span><span class="sxs-lookup"><span data-stu-id="30d1f-131">Existing supply can cover the demand within 12 days, and that period equals the delay tolerance.</span></span> <span data-ttu-id="30d1f-132">Näin ollen pääsuunnittelun ajossa ei luoda suunniteltuja tilauksia.</span><span class="sxs-lookup"><span data-stu-id="30d1f-132">Therefore, when master planning runs, no planned orders are created.</span></span>

### <a name="example-2"></a><span data-ttu-id="30d1f-133">Esimerkki 2</span><span class="sxs-lookup"><span data-stu-id="30d1f-133">Example 2</span></span>

<span data-ttu-id="30d1f-134">Tuotteella on seuraava konfiguraatio:</span><span class="sxs-lookup"><span data-stu-id="30d1f-134">A product has the following configuration:</span></span>

- <span data-ttu-id="30d1f-135">**Läpimenoaika:** *10*</span><span class="sxs-lookup"><span data-stu-id="30d1f-135">**Lead time:** *10*</span></span>
- <span data-ttu-id="30d1f-136">**Negatiiviset päivät:** *0*</span><span class="sxs-lookup"><span data-stu-id="30d1f-136">**Negative days:** *0*</span></span>

<span data-ttu-id="30d1f-137">Tuotteella on seuraava tarjonta ja kysyntä:</span><span class="sxs-lookup"><span data-stu-id="30d1f-137">The following supply and demand exist for the product:</span></span>

- <span data-ttu-id="30d1f-138">**Tämän päivän kysyntä:** myyntitilaus, jonka määrä on 10</span><span class="sxs-lookup"><span data-stu-id="30d1f-138">**Demand for today:** A sales order for a quantity of 10</span></span>
- <span data-ttu-id="30d1f-139">**Toimitus 12 päivän sisällä:** ostotilaus, jonka määrä on 10</span><span class="sxs-lookup"><span data-stu-id="30d1f-139">**Supply in 12 days:** A purchase order for a quantity of 10</span></span>

<span data-ttu-id="30d1f-140">Olemassa oleva tarjonta voi kattaa kysynnän vain 12 päivän kuluttua.</span><span class="sxs-lookup"><span data-stu-id="30d1f-140">Existing supply can cover the demand only after 12 days.</span></span> <span data-ttu-id="30d1f-141">Viivetoleranssi on kuitenkin 10 päivää.</span><span class="sxs-lookup"><span data-stu-id="30d1f-141">However, the delay tolerance is 10 days.</span></span> <span data-ttu-id="30d1f-142">Näin ollen pääsuunnittelun ajossa luodaan suunniteltu tilaus, jonka määrä on 10.</span><span class="sxs-lookup"><span data-stu-id="30d1f-142">Therefore, when master planning runs, a planned order for a quantity of 10 is created.</span></span>

### <a name="example-3"></a><span data-ttu-id="30d1f-143">Esimerkki 3</span><span class="sxs-lookup"><span data-stu-id="30d1f-143">Example 3</span></span>

<span data-ttu-id="30d1f-144">Tuotteella on seuraava konfiguraatio:</span><span class="sxs-lookup"><span data-stu-id="30d1f-144">A product has the following configuration:</span></span>

- <span data-ttu-id="30d1f-145">**Läpimenoaika:** *10*</span><span class="sxs-lookup"><span data-stu-id="30d1f-145">**Lead time:** *10*</span></span>
- <span data-ttu-id="30d1f-146">**Negatiiviset päivät:** *2*</span><span class="sxs-lookup"><span data-stu-id="30d1f-146">**Negative days:** *2*</span></span>

<span data-ttu-id="30d1f-147">Tuotteella on seuraava tarjonta ja kysyntä:</span><span class="sxs-lookup"><span data-stu-id="30d1f-147">The following supply and demand exist for the product:</span></span>

- <span data-ttu-id="30d1f-148">**Kysyntä 11 päivän aikana:** myyntitilaus, jonka määrä on 10</span><span class="sxs-lookup"><span data-stu-id="30d1f-148">**Demand in 11 days:** A sales order for a quantity of 10</span></span>
- <span data-ttu-id="30d1f-149">**Toimitus 14 päivän sisällä:** ostotilaus, jonka määrä on 10</span><span class="sxs-lookup"><span data-stu-id="30d1f-149">**Supply in 14 days:** A purchase order for a quantity of 10</span></span>

<span data-ttu-id="30d1f-150">Olemassa oleva tarjonta voi kattaa kysynnän vain kolmen päivän kuluttua.</span><span class="sxs-lookup"><span data-stu-id="30d1f-150">Existing supply can cover the demand only after three days.</span></span> <span data-ttu-id="30d1f-151">Viivetoleranssi on kuitenkin kaksi päivää.</span><span class="sxs-lookup"><span data-stu-id="30d1f-151">However, the delay tolerance is two days.</span></span> <span data-ttu-id="30d1f-152">(Tässä tapauksessa viivetoleranssi sisältää vain kaksi negatiivista päivää.</span><span class="sxs-lookup"><span data-stu-id="30d1f-152">(In this case, the delay tolerance includes only the two negative days.</span></span> <span data-ttu-id="30d1f-153">Kysyntäpäivämäärää ei sisällytetä, koska se on tuotteen läpimenoajan jälkeen.) Näin ollen pääsuunnittelun ajossa luodaan suunniteltu tilaus, jonka määrä on 10.</span><span class="sxs-lookup"><span data-stu-id="30d1f-153">The demand date isn't included because it's after the product lead time.) Therefore, when master planning runs, a planned order for a quantity of 10 is created.</span></span>
