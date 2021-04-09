---
title: Jaetun tilausten hallinnan (JTH) kustannusten määrittäminen
description: Tässä aiheessa kuvataan Dynamics 365 Commerce -sovelluksen jaetun tilausten hallinnan (JTH) toimintojen kustannusten määrittämistä.
author: josaw1
ms.date: 12/05/2018
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-12-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: f3ed387bf7925785c33e2f0c07e9aba898334567
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795976"
---
# <a name="cost-configuration-for-distributed-order-management-dom"></a><span data-ttu-id="af54d-103">Jaetun tilausten hallinnan (JTH) kustannusten määrittäminen</span><span class="sxs-lookup"><span data-stu-id="af54d-103">Cost configuration for distributed order management (DOM)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="af54d-104">Organisaatiot käyttävät useita kustannuskomponentteja tilauksen täyttämisen optimaalisen sijainnin määrittämisessä.</span><span class="sxs-lookup"><span data-stu-id="af54d-104">Organizations consider multiple cost components to determine the optimal location to fulfill an order from.</span></span> <span data-ttu-id="af54d-105">Kustannuskomponentteja ovat esimerkiksi lähetys-, käsittely- ja pakkauskustannukset.</span><span class="sxs-lookup"><span data-stu-id="af54d-105">Some of these cost components are shipping cost, handling cost, and packaging cost.</span></span> <span data-ttu-id="af54d-106">Näiden kustannusten yhteenlaskettu kustannus määrittää tilauksen täyttämissijainnin.</span><span class="sxs-lookup"><span data-stu-id="af54d-106">A combination of these costs is calculated to determine the fulfillment location.</span></span>

<span data-ttu-id="af54d-107">Kun Dynamics 365 Commerce -sovelluksen jaetun tilausten hallinnan (JTH) ensimmäinen iteraatio optimoi tilausten määrityksen täyttämissijainteihin, se otetaan huomioon vain etäisyytenä.</span><span class="sxs-lookup"><span data-stu-id="af54d-107">When the first iteration of distributed order management (DOM) in Dynamics 365 Commerce optimized the assignment of orders to fulfillment locations, it factored in distance only.</span></span> <span data-ttu-id="af54d-108">Vaikka etäisyys voi korreloida kustannuksen kanssa, se ei ole sama kuin kustannus.</span><span class="sxs-lookup"><span data-stu-id="af54d-108">Although distance can be correlated with cost, it isn't the same as cost.</span></span> <span data-ttu-id="af54d-109">Esimerkiksi lähetystapa yön yli maksaa enemmän kuin kolmen tai seitsemän päivän lähetys samalla etäisyydellä.</span><span class="sxs-lookup"><span data-stu-id="af54d-109">For example, an overnight shipping method costs more than three-day shipping or seven-day shipping over the same distance.</span></span>

<span data-ttu-id="af54d-110">Kustannusten määritystoiminnon avulla jälleenmyyjät voivat määrittää lisäkustannuskomponentteja, jotka lasketaan ja otetaan huomioon tilausrivien toteuttamisessa käytettävän optimaalisen sijainnin määrittämisessä.</span><span class="sxs-lookup"><span data-stu-id="af54d-110">The cost configuration feature lets retailers define and configure additional cost components that will be calculated and factored in to determine the optimal location to fulfill order lines from.</span></span>

<span data-ttu-id="af54d-111">Kun kustannuskomponentit määritetään, JTH:n selvitystoiminto käyttää vain näitä kustannusten määrityksiä tilauksen toteuttamisen optimaalisen sijainnin määrittämisessä.</span><span class="sxs-lookup"><span data-stu-id="af54d-111">When cost components are configured, the DOM solver uses only those cost definitions to determine the optimal location for order fulfillment.</span></span> <span data-ttu-id="af54d-112">Se ei ota huomioon etäisyyskomponenttia kustannuksena.</span><span class="sxs-lookup"><span data-stu-id="af54d-112">It doesn't consider the distance component as a cost.</span></span> <span data-ttu-id="af54d-113">Jos kustannuskomponentteja ei kuitenkaan määritetä, JTH:n selvitystoiminto käyttää etäisyyskomponenttia kustannuksessa tilauksen toteuttamisen optimaalisen sijainnin määrittämisessä.</span><span class="sxs-lookup"><span data-stu-id="af54d-113">However, if no cost components are configured, the DOM solver does use the distance component as a cost to determine the optimal location for order fulfillment.</span></span>

## <a name="set-up-cost-components"></a><span data-ttu-id="af54d-114">Kustannuskomponenttien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="af54d-114">Set up cost components</span></span>

<span data-ttu-id="af54d-115">Järjestelmässä voidaan määrittää kaksi pääkustannuskomponenttia: **lähetys** ja **muu**.</span><span class="sxs-lookup"><span data-stu-id="af54d-115">Two major cost component types can be defined in the system: **Shipping** and **Other**.</span></span>

<span data-ttu-id="af54d-116">Molemmat kustannuskomponentin tyypit tukevat useita laskentaperusteita seuraavassa taulukossa esitetyllä tavalla.</span><span class="sxs-lookup"><span data-stu-id="af54d-116">Both cost component types support multiple calculation bases, as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="af54d-117">Kustannuskomponentin tyyppi</span><span class="sxs-lookup"><span data-stu-id="af54d-117">Cost component type</span></span></th>
<th><span data-ttu-id="af54d-118">Laskuperuste</span><span class="sxs-lookup"><span data-stu-id="af54d-118">Calculation basis</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="af54d-119">Lähetys</span><span class="sxs-lookup"><span data-stu-id="af54d-119">Shipping</span></span></td>
<td>
<ul>
<li><span data-ttu-id="af54d-120">Yksinkertainen</span><span class="sxs-lookup"><span data-stu-id="af54d-120">Simple</span></span></li>
<li><span data-ttu-id="af54d-121">Porrastettu</span><span class="sxs-lookup"><span data-stu-id="af54d-121">Tiered</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="af54d-122">Muu</span><span class="sxs-lookup"><span data-stu-id="af54d-122">Other</span></span></td>
<td>
<ul>
<li><span data-ttu-id="af54d-123">Myyntitilaus</span><span class="sxs-lookup"><span data-stu-id="af54d-123">Sales order</span></span></li>
<li><span data-ttu-id="af54d-124">Myyntirivi</span><span class="sxs-lookup"><span data-stu-id="af54d-124">Sales line</span></span></li>
<li><span data-ttu-id="af54d-125">Sijainti</span><span class="sxs-lookup"><span data-stu-id="af54d-125">Location</span></span></li>
</ul>
</td>
</tr>
</tbody>
</table>

### <a name="shipping-cost-component-type"></a><span data-ttu-id="af54d-126">Lähetyskustannuskomponentin tyyppi</span><span class="sxs-lookup"><span data-stu-id="af54d-126">Shipping cost component type</span></span>

<span data-ttu-id="af54d-127">Tässä osassa kerrotaan, miten kunkin **lähetys** kustannuskomponentin tyypin ja lähetyskustannusten laskentaperusteen yhdistelmä määritetään.</span><span class="sxs-lookup"><span data-stu-id="af54d-127">This section explains how to set up each combination of the **Shipping** cost component type and a calculation basis for shipping costs.</span></span> <span data-ttu-id="af54d-128">Osassa kerrotaan myös, miten JTH:n selvitystoiminto käyttää kutakin yhdistelmää.</span><span class="sxs-lookup"><span data-stu-id="af54d-128">It also explains how the DOM solver uses each combination.</span></span>

#### <a name="cost-component-type--shipping-and-calculation-basis--simple"></a><span data-ttu-id="af54d-129">Kustannuskomponentin tyyppi = lähetys ja laskentaperuste = yksinkertainen</span><span class="sxs-lookup"><span data-stu-id="af54d-129">Cost component type = Shipping and Calculation basis = Simple</span></span>

<span data-ttu-id="af54d-130">Jos käytetään **lähetys** kustannuksen tyyppiä ja **yksinkertaista** laskentaperustetta, toimitustavan lähetyskustannukset perustuvat kiinteään kustannukseen tai etäisyyteen.</span><span class="sxs-lookup"><span data-stu-id="af54d-130">If a combination of the **Shipping** cost component type and the **Simple** calculation basis is used, the shipping cost for a mode of delivery is based on either a flat cost or distance.</span></span>

<span data-ttu-id="af54d-131">Tälle yhdistelmälle on määritettävä seuraavat kentät:</span><span class="sxs-lookup"><span data-stu-id="af54d-131">You must set up the following fields for this combination:</span></span>

- <span data-ttu-id="af54d-132">**Kustannustekijä** – Anna kustannustekijän yksilöivä tunniste.</span><span class="sxs-lookup"><span data-stu-id="af54d-132">**Cost factor** – Enter a unique identifier for the cost factor.</span></span>
- <span data-ttu-id="af54d-133">**Kuvaus** – Anna kustannustekijän nimi ja kuvaus.</span><span class="sxs-lookup"><span data-stu-id="af54d-133">**Description** – Enter the name and description of the cost factor.</span></span>
- <span data-ttu-id="af54d-134">**Alkamis**- ja **päättymispäivä** – Näiden kenttien avulla kustannustekijän voi rajata koskemaan tiettyä ajanjaksoa.</span><span class="sxs-lookup"><span data-stu-id="af54d-134">**Start date** and **End date** – You can use these fields to limit the cost factor for a specific date range.</span></span> <span data-ttu-id="af54d-135">Jos nämä kentät jätetään tyhjiksi, kustannustekijä on voimassa toistaiseksi.</span><span class="sxs-lookup"><span data-stu-id="af54d-135">If you leave these fields blank, the cost factor is valid for an indefinite period.</span></span>
- <span data-ttu-id="af54d-136">**Aktiivinen** – Osoittaa, onko kustannustekijä aktiivinen.</span><span class="sxs-lookup"><span data-stu-id="af54d-136">**Active** – Indicate whether the cost factor is active.</span></span> <span data-ttu-id="af54d-137">JTH ottaa huomioon vain aktiiviset täyttämisprofiilin liitetyt kustannustekijät.</span><span class="sxs-lookup"><span data-stu-id="af54d-137">The DOM considers only active cost factors that are associated with the fulfillment profile.</span></span>
- <span data-ttu-id="af54d-138">**Yritys** – Määritä yritys, jolle kustannustekijä on määritetty.</span><span class="sxs-lookup"><span data-stu-id="af54d-138">**Company** – Specify the legal entity that the cost factor is configured for.</span></span> <span data-ttu-id="af54d-139">Kaikkien laskentakriteerien rivien on koskettava samaa yritystä.</span><span class="sxs-lookup"><span data-stu-id="af54d-139">All lines of the calculation criteria must be for the same legal entity.</span></span>
- <span data-ttu-id="af54d-140">**Toimitustavat** – Määritä toimitustavat, joille kustannus on määritetty.</span><span class="sxs-lookup"><span data-stu-id="af54d-140">**Modes of delivery** – Specify the modes of delivery that the cost is configured for.</span></span>
- <span data-ttu-id="af54d-141">**Laskentatyyppi** – Määritä, miten tietyn toimitustavan kustannus lasketaan.</span><span class="sxs-lookup"><span data-stu-id="af54d-141">**Calculation type** – Specify how the cost should be calculated for a specific mode of delivery.</span></span> <span data-ttu-id="af54d-142">Tuettuja laskentatyyppejä on kaksi:</span><span class="sxs-lookup"><span data-stu-id="af54d-142">Two calculation types are supported:</span></span>

    - <span data-ttu-id="af54d-143">**Kiinteä** – Toimitustavassa käytetään kiinteää kustannusta.</span><span class="sxs-lookup"><span data-stu-id="af54d-143">**Fixed** – A flat cost is used for the mode of delivery.</span></span> <span data-ttu-id="af54d-144">Jos valitset tämän laskentatyypin, **Kustannus**-kenttä määrittää kiinteän kustannuksen.</span><span class="sxs-lookup"><span data-stu-id="af54d-144">If you select this calculation type, the **Cost** field defines the flat cost.</span></span>
    - <span data-ttu-id="af54d-145">**Etäisyysyksikköä kohti** – Toimitustavan kustannus lasketaan kustannuksen arvona. Se määritetään kertomalla **Kustannus**-kentän arvo toimitusosoitteen ja sijaintien etäisyydellä.</span><span class="sxs-lookup"><span data-stu-id="af54d-145">**Per-distance unit** – The cost for the mode of delivery is calculated as the cost value that is specified in the **Cost** field times the distance between the delivery address and the locations.</span></span>

- <span data-ttu-id="af54d-146">**Kustannus** – Määritä kustannusarvo, jota käytetään yhdessä **Laskentatyyppi**-kentän arvon kanssa, kun toimitustavan kustannus lasketaan.</span><span class="sxs-lookup"><span data-stu-id="af54d-146">**Cost** – Specify the cost value that is used in conjunction with the **Calculation type** field to compute the cost for a mode of delivery.</span></span>

#### <a name="cost-component-type--shipping-and-calculation-basis--tiered"></a><span data-ttu-id="af54d-147">Kustannuskomponentin tyyppi = lähetys ja laskentaperuste = porrastettu</span><span class="sxs-lookup"><span data-stu-id="af54d-147">Cost component type = Shipping and Calculation basis = Tiered</span></span>

<span data-ttu-id="af54d-148">Jos käytetään **lähetys** kustannuksen tyyppiä ja **porrastettua** laskentaperustetta, toimitustavan lähetyskustannukset perustuvat kiinteään kustannukseen tai etäisyyteen.</span><span class="sxs-lookup"><span data-stu-id="af54d-148">If a combination of the **Shipping** cost component type and the **Tiered** calculation basis is used, the shipping cost for a mode of delivery is based on either a flat cost or distance.</span></span> <span data-ttu-id="af54d-149">Tässä yhdistelmässä etäisyys perustuu kuitenkin etäisyyksien porrastettuun väliin.</span><span class="sxs-lookup"><span data-stu-id="af54d-149">However, in this combination, the distance is based on a tiered range of distances.</span></span>

<span data-ttu-id="af54d-150">Tälle yhdistelmälle on määritettävä seuraavat kentät:</span><span class="sxs-lookup"><span data-stu-id="af54d-150">You must set up the following fields for this combination:</span></span>

- <span data-ttu-id="af54d-151">**Kustannustekijä** – Anna kustannustekijän yksilöivä tunniste.</span><span class="sxs-lookup"><span data-stu-id="af54d-151">**Cost factor** – Enter a unique identifier for the cost factor.</span></span>
- <span data-ttu-id="af54d-152">**Kuvaus** – Anna kustannustekijän nimi ja kuvaus.</span><span class="sxs-lookup"><span data-stu-id="af54d-152">**Description** – Enter the name and description of the cost factor.</span></span>
- <span data-ttu-id="af54d-153">**Oletuskustannus** – Määritä kustannus, jota käytetään toimitustavassa silloin, kun toimitusosoitteen ja sijainnin etäisyys ei ole mikään toimitustavan porrastetuista etäisyyksistä.</span><span class="sxs-lookup"><span data-stu-id="af54d-153">**Default cost** – Specify the cost that should be used for a mode of delivery if the distance between the delivery address and the location doesn't fall into any of the tiered distances for the mode of delivery.</span></span>
- <span data-ttu-id="af54d-154">**Alkamis**- ja **päättymispäivä** – Näiden kenttien avulla kustannustekijän voi rajata koskemaan tiettyä ajanjaksoa.</span><span class="sxs-lookup"><span data-stu-id="af54d-154">**Start date** and **End date** – You can use these fields to limit the cost factor for a specific date range.</span></span> <span data-ttu-id="af54d-155">Jos nämä kentät jätetään tyhjiksi, kustannustekijä on voimassa toistaiseksi.</span><span class="sxs-lookup"><span data-stu-id="af54d-155">If you leave these fields blank, the cost factor is valid for an indefinite period.</span></span>
- <span data-ttu-id="af54d-156">**Aktiivinen** – Osoittaa, onko kustannustekijä aktiivinen.</span><span class="sxs-lookup"><span data-stu-id="af54d-156">**Active** – Indicate whether the cost factor is active.</span></span> <span data-ttu-id="af54d-157">JTH ottaa huomioon vain aktiiviset täyttämisprofiilin liitetyt kustannustekijät.</span><span class="sxs-lookup"><span data-stu-id="af54d-157">The DOM considers only active cost factors that are associated with the fulfillment profile.</span></span>
- <span data-ttu-id="af54d-158">**Yritys** – Määritä yritys, jolle kustannustekijä on määritetty.</span><span class="sxs-lookup"><span data-stu-id="af54d-158">**Company** – Specify the legal entity that the cost factor is configured for.</span></span> <span data-ttu-id="af54d-159">Kaikkien laskentakriteerien rivien on koskettava samaa yritystä.</span><span class="sxs-lookup"><span data-stu-id="af54d-159">All lines of the calculation criteria must be for the same legal entity.</span></span>
- <span data-ttu-id="af54d-160">**Toimitustavat** – Määritä toimitustavat, joille kustannus on määritetty.</span><span class="sxs-lookup"><span data-stu-id="af54d-160">**Modes of delivery** – Specify the modes of delivery that the cost is configured for.</span></span>
- <span data-ttu-id="af54d-161">**Etäisyyden tyyppi** – Määritä, onko porrastettu etäisyys määritetty linnuntietä vai teitä pitkin.</span><span class="sxs-lookup"><span data-stu-id="af54d-161">**Distance type** – Specify whether the tiered distance definition is an aerial distance or a road distance.</span></span>
- <span data-ttu-id="af54d-162">**Etäisyyden yksiköt** – Määritä yksikkö, jossa porrastettu etäisyys mitataan.</span><span class="sxs-lookup"><span data-stu-id="af54d-162">**Distance units** – Specify the unit that the tiered distance is measured in.</span></span>
- <span data-ttu-id="af54d-163">**Etäisyys kohteesta** – Määritä porrastetun etäisyyden aloitusalue.</span><span class="sxs-lookup"><span data-stu-id="af54d-163">**Distance from** – Specify the start range for the tiered distance.</span></span>
- <span data-ttu-id="af54d-164">**Etäisyys kohteeseen** – Määritä porrastetun etäisyyden lopetusalue.</span><span class="sxs-lookup"><span data-stu-id="af54d-164">**Distance to** – Specify the end range for the tiered distance.</span></span>
- <span data-ttu-id="af54d-165">**Laskentatyyppi** – Määritä, miten tietyn toimitustavan ja porrastetun etäisyyden kustannus lasketaan.</span><span class="sxs-lookup"><span data-stu-id="af54d-165">**Calculation type** – Specify how the cost should be calculated for a specific mode of delivery and tiered distance.</span></span> <span data-ttu-id="af54d-166">Tuettuja laskentatyyppejä on kaksi:</span><span class="sxs-lookup"><span data-stu-id="af54d-166">Two calculation types are supported:</span></span>

    - <span data-ttu-id="af54d-167">**Kiinteä** – Toimitustavassa käytetään kiinteää kustannusta.</span><span class="sxs-lookup"><span data-stu-id="af54d-167">**Fixed** – A flat cost is used for the mode of delivery.</span></span> <span data-ttu-id="af54d-168">Jos valitset tämän laskentatyypin, **Kustannus**-kenttä määrittää kiinteän kustannuksen.</span><span class="sxs-lookup"><span data-stu-id="af54d-168">If you select this calculation type, the **Cost** field defines the flat cost.</span></span>
    - <span data-ttu-id="af54d-169">**Etäisyysyksikköä kohti** – Toimitustavan ja porrastetun etäisyyden kustannus lasketaan kustannuksen arvona. Se määritetään kertomalla **Kustannus**-kentän arvo toimitusosoitteen ja sijaintien etäisyydellä.</span><span class="sxs-lookup"><span data-stu-id="af54d-169">**Per distance unit** – The cost for the mode of delivery and tiered distance is calculated as the cost value that is specified in the **Cost** field times the distance between the delivery address and the locations.</span></span>

- <span data-ttu-id="af54d-170">**Kustannus** – Määritä kustannusarvo, jota käytetään yhdessä **Laskentatyyppi**-kentän arvon kanssa, kun toimitustavan kustannus lasketaan.</span><span class="sxs-lookup"><span data-stu-id="af54d-170">**Cost** – Specify the cost value that is used in conjunction with the **Calculation type** field to compute the cost for a mode of delivery.</span></span>

> [!NOTE]
> - <span data-ttu-id="af54d-171">Kun määrität porrastetut etäisyydet, järjestelmä tarkistaa, että etäisyyksiä ei puutu ja että ne eivät ole päällekkäisiä.</span><span class="sxs-lookup"><span data-stu-id="af54d-171">When you define tiered distances, the system validates that there are no missing or overlapping distances.</span></span>
> - <span data-ttu-id="af54d-172">Toimitustavassa käytettävän etäisyyden tyypin on oltava sama kaikissa porrastetuissa etäisyyksissä.</span><span class="sxs-lookup"><span data-stu-id="af54d-172">The distance type that is used for a mode of delivery must be the same across all the tiered distances.</span></span>

### <a name="other-cost-component-type"></a><span data-ttu-id="af54d-173">Muu kustannuskomponentin tyyppi</span><span class="sxs-lookup"><span data-stu-id="af54d-173">Other cost component type</span></span>

<span data-ttu-id="af54d-174">Tässä osassa kerrotaan, miten kunkin **muun** kustannuskomponentin tyypin ja muun kuin lähetyskustannusten muun kustannustyypin laskentaperusteen yhdistelmä määritetään.</span><span class="sxs-lookup"><span data-stu-id="af54d-174">This section explains how to set up each combination of the **Other** cost component type and an other cost type for non-shipping costs.</span></span> <span data-ttu-id="af54d-175">Osassa kerrotaan myös, miten JTH:n selvitystoiminto käyttää kutakin yhdistelmää.</span><span class="sxs-lookup"><span data-stu-id="af54d-175">It also explains how the DOM solver uses each combination.</span></span>

#### <a name="cost-component-type--other-and-other-cost-type--sales-order"></a><span data-ttu-id="af54d-176">Kustannuskomponentin tyyppi = muu ja muun kustannuksen tyyppi = myyntitilaus</span><span class="sxs-lookup"><span data-stu-id="af54d-176">Cost component type = Other and Other cost type = Sales order</span></span>

<span data-ttu-id="af54d-177">**Muun** kustannuskomponentin tyypin ja **myyntitilauksen** muun kustannuksen tyypin yhdistelmää käytetään määritettäessä muita kuin lähetyskustannuksia myyntitilauksen tasolla.</span><span class="sxs-lookup"><span data-stu-id="af54d-177">A combination of the **Other** cost component type and the **Sales order** other cost type is used to define non-shipping costs at the sales order level.</span></span>

<span data-ttu-id="af54d-178">Tälle yhdistelmälle on määritettävä seuraavat kentät:</span><span class="sxs-lookup"><span data-stu-id="af54d-178">You must set up the following fields for this combination:</span></span>

- <span data-ttu-id="af54d-179">**Kustannustekijä** – Anna kustannustekijän yksilöivä tunniste.</span><span class="sxs-lookup"><span data-stu-id="af54d-179">**Cost factor** – Enter a unique identifier for the cost factor.</span></span>
- <span data-ttu-id="af54d-180">**Kuvaus** – Anna kustannustekijän nimi ja kuvaus.</span><span class="sxs-lookup"><span data-stu-id="af54d-180">**Description** – Enter the name and description of the cost factor.</span></span>
- <span data-ttu-id="af54d-181">**Alkamis**- ja **päättymispäivä** – Näiden kenttien avulla kustannustekijän voi rajata koskemaan tiettyä ajanjaksoa.</span><span class="sxs-lookup"><span data-stu-id="af54d-181">**Start date** and **End date** – You can use these fields to limit the cost factor for a specific date range.</span></span> <span data-ttu-id="af54d-182">Jos nämä kentät jätetään tyhjiksi, kustannustekijä on voimassa toistaiseksi.</span><span class="sxs-lookup"><span data-stu-id="af54d-182">If you leave these fields blank, the cost factor is valid for an indefinite period.</span></span>
- <span data-ttu-id="af54d-183">**Aktiivinen** – Osoittaa, onko kustannustekijä aktiivinen.</span><span class="sxs-lookup"><span data-stu-id="af54d-183">**Active** – Indicate whether the cost factor is active.</span></span> <span data-ttu-id="af54d-184">JTH ottaa huomioon vain aktiiviset täyttämisprofiilin liitetyt kustannustekijät.</span><span class="sxs-lookup"><span data-stu-id="af54d-184">The DOM considers only active cost factors that are associated with the fulfillment profile.</span></span>
- <span data-ttu-id="af54d-185">**Kustannus** – Määritä muiden kuin lähetyskustannusten kustannusarvo myyntitilauksen tasolla.</span><span class="sxs-lookup"><span data-stu-id="af54d-185">**Cost** – Specify the cost value for a non-shipping cost at the sales order level.</span></span>

#### <a name="cost-component-type--other-and-other-cost-type--sales-line"></a><span data-ttu-id="af54d-186">Kustannuskomponentin tyyppi = muu ja muun kustannuksen tyyppi = myyntirivi</span><span class="sxs-lookup"><span data-stu-id="af54d-186">Cost component type = Other and Other cost type = Sales line</span></span>

<span data-ttu-id="af54d-187">**Muun** kustannuskomponentin tyypin ja **myyntirivin** muun kustannuksen tyypin yhdistelmää käytetään määritettäessä muita kuin lähetyskustannuksia myyntitilausrivin tasolla.</span><span class="sxs-lookup"><span data-stu-id="af54d-187">A combination of the **Other** cost component type and the **Sales line** other cost type is used to define non-shipping costs at the sales order line level.</span></span>

<span data-ttu-id="af54d-188">Tälle yhdistelmälle on määritettävä seuraavat kentät:</span><span class="sxs-lookup"><span data-stu-id="af54d-188">You must set up the following fields for this combination:</span></span>

- <span data-ttu-id="af54d-189">**Kustannustekijä** – Anna kustannustekijän yksilöivä tunniste.</span><span class="sxs-lookup"><span data-stu-id="af54d-189">**Cost factor** – Enter a unique identifier for the cost factor.</span></span>
- <span data-ttu-id="af54d-190">**Kuvaus** – Anna kustannustekijän nimi ja kuvaus.</span><span class="sxs-lookup"><span data-stu-id="af54d-190">**Description** – Enter the name and description of the cost factor.</span></span>
- <span data-ttu-id="af54d-191">**Alkamis**- ja **päättymispäivä** – Näiden kenttien avulla kustannustekijän voi rajata koskemaan tiettyä ajanjaksoa.</span><span class="sxs-lookup"><span data-stu-id="af54d-191">**Start date** and **End date** – You can use these fields to limit the cost factor for a specific date range.</span></span> <span data-ttu-id="af54d-192">Jos nämä kentät jätetään tyhjiksi, kustannustekijä on voimassa toistaiseksi.</span><span class="sxs-lookup"><span data-stu-id="af54d-192">If you leave these fields blank, the cost factor is valid for an indefinite period.</span></span>
- <span data-ttu-id="af54d-193">**Aktiivinen** – Osoittaa, onko kustannustekijä aktiivinen.</span><span class="sxs-lookup"><span data-stu-id="af54d-193">**Active** – Indicate whether the cost factor is active.</span></span> <span data-ttu-id="af54d-194">JTH ottaa huomioon vain aktiiviset täyttämisprofiilin liitetyt kustannustekijät.</span><span class="sxs-lookup"><span data-stu-id="af54d-194">The DOM considers only active cost factors that are associated with the fulfillment profile.</span></span>
- <span data-ttu-id="af54d-195">**Kustannus** – Määritä muiden kuin lähetyskustannusten kustannusarvo myyntitilausrivin tasolla.</span><span class="sxs-lookup"><span data-stu-id="af54d-195">**Cost** – Specify the cost value for a non-shipping cost at the sales order line level.</span></span>

#### <a name="cost-component-type--other-and-other-cost-type--location"></a><span data-ttu-id="af54d-196">Kustannuskomponentin tyyppi = muu ja muun kustannuksen tyyppi = sijainti</span><span class="sxs-lookup"><span data-stu-id="af54d-196">Cost component type = Other and Other cost type = Location</span></span>

<span data-ttu-id="af54d-197">**Muun** ja **sijainnin** muun kustannustyypin yhdistelmää käytetään sijaintiryhmien tai yksittäisen sijainnin muiden kuin lähetyskustannusten määrittämisessä.</span><span class="sxs-lookup"><span data-stu-id="af54d-197">A combination of the **Other** cost component type and the **Location** other cost type is used to define non-shipping costs for a group of locations or an individual location.</span></span>

<span data-ttu-id="af54d-198">Tälle yhdistelmälle on määritettävä seuraavat kentät:</span><span class="sxs-lookup"><span data-stu-id="af54d-198">You must set up the following fields for this combination:</span></span>

- <span data-ttu-id="af54d-199">**Kustannustekijä** – Anna kustannustekijän yksilöivä tunniste.</span><span class="sxs-lookup"><span data-stu-id="af54d-199">**Cost factor** – Enter a unique identifier for the cost factor.</span></span>
- <span data-ttu-id="af54d-200">**Kuvaus** – Anna kustannustekijän nimi ja kuvaus.</span><span class="sxs-lookup"><span data-stu-id="af54d-200">**Description** – Enter the name and description of the cost factor.</span></span>
- <span data-ttu-id="af54d-201">**Alkamis**- ja **päättymispäivä** – Näiden kenttien avulla kustannustekijän voi rajata koskemaan tiettyä ajanjaksoa.</span><span class="sxs-lookup"><span data-stu-id="af54d-201">**Start date** and **End date** – You can use these fields to limit the cost factor for a specific date range.</span></span> <span data-ttu-id="af54d-202">Jos nämä kentät jätetään tyhjiksi, kustannustekijä on voimassa toistaiseksi.</span><span class="sxs-lookup"><span data-stu-id="af54d-202">If you leave these fields blank, the cost factor is valid for an indefinite period.</span></span>
- <span data-ttu-id="af54d-203">**Aktiivinen** – Osoittaa, onko kustannustekijä aktiivinen.</span><span class="sxs-lookup"><span data-stu-id="af54d-203">**Active** – Indicate whether the cost factor is active.</span></span> <span data-ttu-id="af54d-204">JTH ottaa huomioon vain aktiiviset täyttämisprofiilin liitetyt kustannustekijät.</span><span class="sxs-lookup"><span data-stu-id="af54d-204">The DOM considers only active cost factors that are associated with the fulfillment profile.</span></span>
- <span data-ttu-id="af54d-205">**Täyttämisryhmä** – Määritä niiden sijaintien ryhmä, joille muun kuin lähetyksen kustannus määritetään.</span><span class="sxs-lookup"><span data-stu-id="af54d-205">**Fulfillment group** – Specify the group of locations that the non-shipping cost is defined for.</span></span>
- <span data-ttu-id="af54d-206">**Täyttämissijainti** – Määritä se sijainti, jolle muun kuin lähetyksen kustannus määritetään.</span><span class="sxs-lookup"><span data-stu-id="af54d-206">**Fulfillment location** – Specify the location that the non-shipping cost is defined for.</span></span>

    > [!NOTE]
    > <span data-ttu-id="af54d-207">Et voi määrittää täyttämisryhmää ja -sijaintia samalle sijaintiin perustuvalle laskentakriteerien riville.</span><span class="sxs-lookup"><span data-stu-id="af54d-207">You can't specify a fulfillment group and a fulfillment location on the same line for location-based calculation criteria.</span></span>

- <span data-ttu-id="af54d-208">**Kustannus** – Määritä muun kuin lähetyskustannuksen kustannusarvo täyttämisryhmän tai täyttämissijainnin tasolla.</span><span class="sxs-lookup"><span data-stu-id="af54d-208">**Cost** – Specify the cost value for a non-shipping cost at the fulfillment group level or fulfillment location level.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="af54d-209">Lisää kustannustekijä soveltuvaan täyttämisprofiiliin, jotta JTH voi käyttää näitä kustannuksia suorittamisen aikana.</span><span class="sxs-lookup"><span data-stu-id="af54d-209">For DOM to consider these costs when it's run, you must add the cost factor to the relevant fulfillment profile.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]