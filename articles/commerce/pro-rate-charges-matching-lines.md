---
title: Otsikon kulujen jakaminen suhteellisesti vastaaville myyntiriveille
description: Tässä ohjeaiheessa käsitellään Commerce-kanavan tilausten automaattisten kulujen laskemisen ja kohdistamisen lisäominaisuuksia käyttämällä automaattista etukäteisveloitustoimintoa.
author: hhaines
manager: annbe
ms.date: 03/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 048885cac7a316e144b2df072da405d74096203f
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4411845"
---
# <a name="prorate-header-charges-to-matching-sales-lines"></a><span data-ttu-id="6ba6b-103">Otsikon kulujen jakaminen suhteellisesti vastaaville myyntiriveille</span><span class="sxs-lookup"><span data-stu-id="6ba6b-103">Prorate header charges to matching sales lines</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="6ba6b-104">Tässä ohjeaiheessa käsitellään otsikkotason automaattisten kulujen ryhmittämistoimintoa ja niiden jakamista suhteellisti kaupan myyntiriveille.</span><span class="sxs-lookup"><span data-stu-id="6ba6b-104">This topic describes the functionality for grouping header-level auto-charges and prorating them to commerce sales lines.</span></span> <span data-ttu-id="6ba6b-105">Tätä toimintoa voi käyttää tapahtumissa, josta on luotu myyntipisteessä Retail-versiolla 10.0.1 ja myynneissä, jotka on luotu puhelinkeskuksessa Retail-versiolla 10.0.2.</span><span class="sxs-lookup"><span data-stu-id="6ba6b-105">This functionality is available for transactions that are created at the point of sale (POS) in Retail version 10.0.1 and sales that are created in a call center in Retail version 10.0.2.</span></span>

<span data-ttu-id="6ba6b-106">Tämä toiminto on käytettävissä vain, jos [automaattiset etukäteisveloitukset](https://docs.microsoft.com/dynamics365/unified-operations/retail/omni-auto-charges) on otettu käyttöön **Commercen parametrit** -sivun asetuksella.</span><span class="sxs-lookup"><span data-stu-id="6ba6b-106">This functionality is available only if the [advanced auto-charges](https://docs.microsoft.com/dynamics365/unified-operations/retail/omni-auto-charges) feature is turned on by using the option on the **Commerce parameters** page.</span></span> <span data-ttu-id="6ba6b-107">Automaattisten kulujen laajennettua laskentamenetelmään voidaan lisäksi käyttää vain myyntitilauksissa, jotka on luotu myyntikanavissa (myyntipiste, puhelinkeskus ja Dynamicsin sähköinen kaupankäyntiympäristö).</span><span class="sxs-lookup"><span data-stu-id="6ba6b-107">Additionally, the enhanced calculation method for auto-charges can be applied only to sales orders that are created through commerce channels (the POS, a call center, and the Dynamics e-Commerce platform).</span></span>

<span data-ttu-id="6ba6b-108">Tämän uuden toiminnon avulla organisaatiot voivat laskea ja kohdistaa otsikkotason automaattiset kulut entistä joustavammin myyntitapahtumiin.</span><span class="sxs-lookup"><span data-stu-id="6ba6b-108">This new functionality gives organizations more flexibility in the way that header-level auto-charges are calculated and applied to sales transactions.</span></span>

<span data-ttu-id="6ba6b-109">Versiota 10.0.1 edeltävissä sovelluksen versioissa otsikkotason automaattiset kulut, joilla on tietty toimitustapasuhde, laskettiin vain, kun myyntitilauksen otsikossa oli vastaava toimitustapa.</span><span class="sxs-lookup"><span data-stu-id="6ba6b-109">In versions of the app earlier than version 10.0.1, header-level auto-charges that have a specific mode of delivery relation are calculated only when there is a match with the mode of delivery that is defined on the sales order header.</span></span>

<span data-ttu-id="6ba6b-110">Esimerkki: Otsikkotason automaattiset kulut on määritetty toimitustavoille **99** ja **11**.</span><span class="sxs-lookup"><span data-stu-id="6ba6b-110">For example, header-level auto-charges are defined for mode of delivery **99** and mode of delivery **11**.</span></span> <span data-ttu-id="6ba6b-111">Myyntitilaus luodaan, ja tilauksessa otsikossa toimitustavaksi on määritetty **99**.</span><span class="sxs-lookup"><span data-stu-id="6ba6b-111">A sales order is created, and mode of delivery **99** is defined on the order header.</span></span> <span data-ttu-id="6ba6b-112">Osa myyntiriveistä on kuitenkin määritetty siten, että niiden toimitukseen käytetään toimitustapaa **11**.</span><span class="sxs-lookup"><span data-stu-id="6ba6b-112">However, some of the sale lines are set up so that they're shipped by using mode of delivery **11**.</span></span> <span data-ttu-id="6ba6b-113">Tässä tapauksessa vain toimitustapaan **99** linkitetyt otsikkotason kulut otetaan huomioon ja kohdistetaan myyntitilaukseen.</span><span class="sxs-lookup"><span data-stu-id="6ba6b-113">In this case, only the header-level charges that are linked to mode of delivery **99** are considered and applied to the sales order.</span></span>

<span data-ttu-id="6ba6b-114">Commercessa otsikkotason kuluilla on lisäominaisuus, jonka avulla voi määrittää tilauksen arvoon perustuvan [maksutasomäärityksen](https://docs.microsoft.com/dynamics365/unified-operations/retail/configure-call-center-delivery).</span><span class="sxs-lookup"><span data-stu-id="6ba6b-114">In Commerce, the header-level charges have an additional feature that lets you define a [tiered charge configuration](https://docs.microsoft.com/dynamics365/unified-operations/retail/configure-call-center-delivery) that is based on the order value.</span></span> <span data-ttu-id="6ba6b-115">Esimerkki: Jos tilauksen arvo 50,00–200,00 $, organisaatio voi veloittaa rahtikuluina 5,00 $.</span><span class="sxs-lookup"><span data-stu-id="6ba6b-115">For example, if the order value is between $50.00 and $200.00, an organization might want to charge a freight charge of $5.00.</span></span> <span data-ttu-id="6ba6b-116">Jos tilauksen arvo on kuitenkin 200,01–500,00 $, rahtikulut voivat olla 4,00 $.</span><span class="sxs-lookup"><span data-stu-id="6ba6b-116">However, if the order value is between $200.01 and $500.00, the freight charge might be $4.00.</span></span>

<span data-ttu-id="6ba6b-117">Osa organisaatioista haluaa käyttää otsikkotason kuluista saatavat maksutasolaskennan edut.</span><span class="sxs-lookup"><span data-stu-id="6ba6b-117">Some organizations want the benefits of the tiered charge calculation that is provided with header-level charges.</span></span> <span data-ttu-id="6ba6b-118">Jos skenaario kuitenkin sisältää toimitustapayhdistelmän, nämä organisaatiot haluavat myös varmistaa, että laskettavat kulut perustuvat kullakin myyntirivillä määritettyyn toimitustapaan.</span><span class="sxs-lookup"><span data-stu-id="6ba6b-118">However, in scenarios that involve mixed modes of delivery, they also want to make sure that the charges that are calculated are based on a match with the mode of delivery that is defined on each sales line.</span></span>

<span data-ttu-id="6ba6b-119">Voit nyt määrittää otsikkotason automaattiset kulut siten, että kaikki tilauksen toimitustavat otetaan huomioon, kuluja laskettaessa.</span><span class="sxs-lookup"><span data-stu-id="6ba6b-119">You can now configure header-level auto-charges so that all modes of delivery on the order are considered when charges are calculated.</span></span> <span data-ttu-id="6ba6b-120">Tämä toiminto edellyttää, että otsikkotason kulujen laskemisessa käytetään monimutkaista kustannuslaskentalogiikkaa.</span><span class="sxs-lookup"><span data-stu-id="6ba6b-120">This functionality requires a more complex calculation logic to calculate the header-level charges.</span></span> <span data-ttu-id="6ba6b-121">Logiikka ryhmittää yhteen kaikki samalla toimitustavalla lähetettävät nimikkeet ja käsittelee tätä ryhmää nimikkeiden laskentaryhmänä, kun se laskee otsikkotason automaattiset kulut.</span><span class="sxs-lookup"><span data-stu-id="6ba6b-121">The logic groups together all the items that are shipped using the same mode of delivery, and it treats that group as the calculation group for the items when it calculates the header-level auto-charges.</span></span> <span data-ttu-id="6ba6b-122">Jos nimikkeillä on sama toimitustapa, automaattiset kulut lasketaan nimikkeiden yhdistetyn myyntiarvon perusteella.</span><span class="sxs-lookup"><span data-stu-id="6ba6b-122">For items that have the same mode of delivery, auto-charges are calculated based on the combined sales value of the items.</span></span> <span data-ttu-id="6ba6b-123">Tällä tavoin määritetään asianmukainen automaattinen kulutaso.</span><span class="sxs-lookup"><span data-stu-id="6ba6b-123">In this way, the appropriate auto-charge tier is determined.</span></span>

<span data-ttu-id="6ba6b-124">Kun samaa toimitustapaa käyttävien myyntirivien asianmukaiset otsikkotason kulut on saatu, lasketut kulut jaetaan suhteellisesti myyntirivitasolle.</span><span class="sxs-lookup"><span data-stu-id="6ba6b-124">After the appropriate header-level charges are obtained for the sales lines that are shipped using the same mode of delivery, the calculated charges are prorated down to the sales line level.</span></span> <span data-ttu-id="6ba6b-125">Koska nämä kulut ovat rivitasolla sen sijaan, että pidettäisiin otsikkotasolla, nimikkeen ja sille lasketun kuluarvon välille muodostuu tarkka linkki.</span><span class="sxs-lookup"><span data-stu-id="6ba6b-125">Because these charges are at the line level and not kept at the header level, a more specific link is made between the item and the charge value that calculated for it.</span></span> <span data-ttu-id="6ba6b-126">Tästä voi olla hyötyä osittaisissa palautuksissa, joissa organisaatio haluaa palauttaa koko kulun sijaan vain osan kulusta silloin, kun vain jotkin nimikkeet palautetaan.</span><span class="sxs-lookup"><span data-stu-id="6ba6b-126">This behavior can be useful in partial return scenarios, where an organization wants to refund only part of the charge instead of the whole charge when only some items are returned.</span></span>

## <a name="scenarios"></a><span data-ttu-id="6ba6b-127">Skenaariot</span><span class="sxs-lookup"><span data-stu-id="6ba6b-127">Scenarios</span></span>

<span data-ttu-id="6ba6b-128">Kahdessa seuraavassa malliskenaariossa havainnollistetaan, miten nämä kulut lasketaan silloin, kun uusi toiminto on käytössä ja silloin kun sitä ei käytetä.</span><span class="sxs-lookup"><span data-stu-id="6ba6b-128">The following two sample scenarios outline how these charges are calculated both when the new functionality is used and when it isn't used.</span></span>

### <a name="scenario-1"></a><span data-ttu-id="6ba6b-129">Skenaario 1</span><span class="sxs-lookup"><span data-stu-id="6ba6b-129">Scenario 1</span></span>

<span data-ttu-id="6ba6b-130">Tämä skenaario havainnollistaa, mitä tapahtuu, kun automaattisten kulujen asetuksissa **Jaa suhteellisesti vastaaville myyntiriveille** -asetuksen arvoksi valitaan **Ei**.</span><span class="sxs-lookup"><span data-stu-id="6ba6b-130">This scenario outlines the behavior when the **Pro-rate to matching sales lines** option is set to **No** in the auto-charge setup.</span></span> <span data-ttu-id="6ba6b-131">(Tämä toiminta vastaa otsikko tason kuluja versiota 10.0.1 edeltävissä sovellusversioissa.)</span><span class="sxs-lookup"><span data-stu-id="6ba6b-131">(The behavior is equivalent to the behavior of header-level charges in app versions that are earlier than version 10.0.1.)</span></span>

<span data-ttu-id="6ba6b-132">Tässä skenaariossa organisaatio on määrittänyt toimitustapasuhteiden **99** ja **11** otsikkotason kulut.</span><span class="sxs-lookup"><span data-stu-id="6ba6b-132">In this scenario, the organization has defined header-level charges for mode of delivery relation **99** and mode of delivery relation **11**.</span></span> <span data-ttu-id="6ba6b-133">Toimitustavalle **21** ei ole määritetty automaattisia kuluja.</span><span class="sxs-lookup"><span data-stu-id="6ba6b-133">No auto-charges are configured for mode of delivery **21**.</span></span>

![Toimitustavan 99 automaattiset kulut, kun vastaavan rivin suhteellinen jako on poistettu käytöstä](media/99_disabled.png)

![Toimitustavan 11 automaattiset kulut, kun vastaavan rivin suhteellinen jako on poistettu käytöstä](media/11_disabled.png)

<span data-ttu-id="6ba6b-136">Myyntitilaus luodaan puhelinkeskuksessa ja toimitustavaksi määritetään **99**.</span><span class="sxs-lookup"><span data-stu-id="6ba6b-136">A sales order is created in the call center, and the mode of delivery is set to **99**.</span></span> <span data-ttu-id="6ba6b-137">Tässä tilauksessa on viisi nimikettä.</span><span class="sxs-lookup"><span data-stu-id="6ba6b-137">This order contains five items.</span></span> <span data-ttu-id="6ba6b-138">Kaksi tilausriviä on määritetty käyttämään toimitustapaa **99**, kaksi riviä toimitustapaa **11** ja yksi rivi toimitustapaa **21** (katso seuraava taulukko).</span><span class="sxs-lookup"><span data-stu-id="6ba6b-138">Two order lines have been configured to use mode of delivery **99**, two lines have been configured to use mode of delivery **11**, and one line has been configured to use mode of delivery **21**, as shown in the following table.</span></span>

| <span data-ttu-id="6ba6b-139">Nimike</span><span class="sxs-lookup"><span data-stu-id="6ba6b-139">Item</span></span>  | <span data-ttu-id="6ba6b-140">Rivin määrä</span><span class="sxs-lookup"><span data-stu-id="6ba6b-140">Line quantity</span></span> | <span data-ttu-id="6ba6b-141">Toimitustapa</span><span class="sxs-lookup"><span data-stu-id="6ba6b-141">Delivery mode</span></span> | <span data-ttu-id="6ba6b-142">Yksikköhinta</span><span class="sxs-lookup"><span data-stu-id="6ba6b-142">Price per unit</span></span> |
|-------|---------------|---------------|----------------|
| <span data-ttu-id="6ba6b-143">81331</span><span class="sxs-lookup"><span data-stu-id="6ba6b-143">81331</span></span> | <span data-ttu-id="6ba6b-144">1</span><span class="sxs-lookup"><span data-stu-id="6ba6b-144">1</span></span>             | <span data-ttu-id="6ba6b-145">11</span><span class="sxs-lookup"><span data-stu-id="6ba6b-145">11</span></span>            | <span data-ttu-id="6ba6b-146">10 $</span><span class="sxs-lookup"><span data-stu-id="6ba6b-146">$10</span></span>            |
| <span data-ttu-id="6ba6b-147">81332</span><span class="sxs-lookup"><span data-stu-id="6ba6b-147">81332</span></span> | <span data-ttu-id="6ba6b-148">1</span><span class="sxs-lookup"><span data-stu-id="6ba6b-148">1</span></span>             | <span data-ttu-id="6ba6b-149">99</span><span class="sxs-lookup"><span data-stu-id="6ba6b-149">99</span></span>            | <span data-ttu-id="6ba6b-150">50 $</span><span class="sxs-lookup"><span data-stu-id="6ba6b-150">$50</span></span>            |
| <span data-ttu-id="6ba6b-151">81333</span><span class="sxs-lookup"><span data-stu-id="6ba6b-151">81333</span></span> | <span data-ttu-id="6ba6b-152">2</span><span class="sxs-lookup"><span data-stu-id="6ba6b-152">2</span></span>             | <span data-ttu-id="6ba6b-153">11</span><span class="sxs-lookup"><span data-stu-id="6ba6b-153">11</span></span>            | <span data-ttu-id="6ba6b-154">30 $</span><span class="sxs-lookup"><span data-stu-id="6ba6b-154">$30</span></span>            |
| <span data-ttu-id="6ba6b-155">81334</span><span class="sxs-lookup"><span data-stu-id="6ba6b-155">81334</span></span> | <span data-ttu-id="6ba6b-156">3</span><span class="sxs-lookup"><span data-stu-id="6ba6b-156">3</span></span>             | <span data-ttu-id="6ba6b-157">99</span><span class="sxs-lookup"><span data-stu-id="6ba6b-157">99</span></span>            | <span data-ttu-id="6ba6b-158">10 $</span><span class="sxs-lookup"><span data-stu-id="6ba6b-158">$10</span></span>            |
| <span data-ttu-id="6ba6b-159">81334</span><span class="sxs-lookup"><span data-stu-id="6ba6b-159">81334</span></span> | <span data-ttu-id="6ba6b-160">3</span><span class="sxs-lookup"><span data-stu-id="6ba6b-160">3</span></span>             | <span data-ttu-id="6ba6b-161">21</span><span class="sxs-lookup"><span data-stu-id="6ba6b-161">21</span></span>            | <span data-ttu-id="6ba6b-162">5 $</span><span class="sxs-lookup"><span data-stu-id="6ba6b-162">$5</span></span>             |

<span data-ttu-id="6ba6b-163">Tässä skenaariossa koko tilaus arvioidaan toimitustavan **99** automaattisen kulutaulukon perusteella.</span><span class="sxs-lookup"><span data-stu-id="6ba6b-163">In this scenario, the whole order is evaluated against the auto-charge table for mode of delivery **99**.</span></span> <span data-ttu-id="6ba6b-164">Kaikkien myyntirivien kokonaissumman perusteella määritetään automaattisen kulumäärityksen vastaava taso, ja tätä kulua käytetään tilauksen otsikkotasolla.</span><span class="sxs-lookup"><span data-stu-id="6ba6b-164">The full total of all sales lines is used to determine a matching tier in the auto-charge configuration, and this charge is applied at the order header level.</span></span> <span data-ttu-id="6ba6b-165">Tässä esimerkiksi tilauksen kokonaissumma on 165,00 $, ja tilauksen otsikkoon on kohdistettu 15,00 $:n rahtikulu.</span><span class="sxs-lookup"><span data-stu-id="6ba6b-165">In this example, the order total is $165.00, and the $15.00 freight charge is applied to the order header.</span></span> <span data-ttu-id="6ba6b-166">Toimitustavalle **11** määritettyjä automaattisia kustannuksia ei koskaan tarkisteta tai käytetä.</span><span class="sxs-lookup"><span data-stu-id="6ba6b-166">Auto-charges that are configured for mode of delivery **11** are never referenced or applied.</span></span>

<span data-ttu-id="6ba6b-167">Jos asiakas palauttaa tässä skenaariossa joitakin tilauksen nimikkeitä ja jos [kulukoodi on määritetty siten, että se palautetaan](https://docs.microsoft.com/dynamics365/unified-operations/retail/omni-auto-charges#setup-and-configuration-2), palautetukseen käytetään järjestelmällisesti otsikkotason kokonaiskulua, vaikka voi osa nimikkeistä palautetaan.</span><span class="sxs-lookup"><span data-stu-id="6ba6b-167">In this scenario, if a customer returns some of the items on the order, and if the [charge code has been configured so that it will be refunded](https://docs.microsoft.com/dynamics365/unified-operations/retail/omni-auto-charges#setup-and-configuration-2), the total header-level charge is systematically applied to the refund, even if only some of the items are returned.</span></span>

### <a name="scenario-2"></a><span data-ttu-id="6ba6b-168">Skenaario 2</span><span class="sxs-lookup"><span data-stu-id="6ba6b-168">Scenario 2</span></span>

<span data-ttu-id="6ba6b-169">Tässä skenaariossa on määritetty toimitustapasuhteiden **99** ja **11** otsikkotason kulut.</span><span class="sxs-lookup"><span data-stu-id="6ba6b-169">In this scenario, header-level charges are defined for mode of delivery relation **99** and mode of delivery relation **11**.</span></span> <span data-ttu-id="6ba6b-170">Näiden automaattisten kulutaulukkojen **Jaa suhteellisesti vastaaville myyntiriveille** -asetukseksi on määritetty **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="6ba6b-170">However, the **Pro-rate to matching sales lines** option is set to **Yes** for these auto-charge tables.</span></span>

![Toimitustavan 99 automaattiset kulut, kun vastaavan rivin suhteellinen jako on otettu käyttöön](media/99_enabled.png)

![Toimitustavan 11 automaattiset kulut, kun vastaavan rivin suhteellinen jako on otettu käyttöön](media/11_enabled.png)

<span data-ttu-id="6ba6b-173">Tässä skenaariossa käytetään samaa viisi riviä sisältävää myyntiriviä.</span><span class="sxs-lookup"><span data-stu-id="6ba6b-173">This scenario uses the same sales order that contains five lines.</span></span> <span data-ttu-id="6ba6b-174">Vaikka tilauksen otsikon toimitustavaksi määritetään **99**, myyntilauksen kunkin rivin toimitustapa määritetään seuraavaan taulukon mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="6ba6b-174">The mode of delivery on the order header is set to **99**, but the mode of delivery for each item on the sales order is configured as shown in the following table.</span></span>

| <span data-ttu-id="6ba6b-175">Nimike</span><span class="sxs-lookup"><span data-stu-id="6ba6b-175">Item</span></span>  | <span data-ttu-id="6ba6b-176">Rivin määrä</span><span class="sxs-lookup"><span data-stu-id="6ba6b-176">Line quantity</span></span> | <span data-ttu-id="6ba6b-177">Toimitustapa</span><span class="sxs-lookup"><span data-stu-id="6ba6b-177">Delivery mode</span></span> | <span data-ttu-id="6ba6b-178">Yksikköhinta</span><span class="sxs-lookup"><span data-stu-id="6ba6b-178">Price per unit</span></span> |
|-------|---------------|---------------|----------------|
| <span data-ttu-id="6ba6b-179">81331</span><span class="sxs-lookup"><span data-stu-id="6ba6b-179">81331</span></span> | <span data-ttu-id="6ba6b-180">1</span><span class="sxs-lookup"><span data-stu-id="6ba6b-180">1</span></span>             | <span data-ttu-id="6ba6b-181">11</span><span class="sxs-lookup"><span data-stu-id="6ba6b-181">11</span></span>            | <span data-ttu-id="6ba6b-182">10 $</span><span class="sxs-lookup"><span data-stu-id="6ba6b-182">$10</span></span>            |
| <span data-ttu-id="6ba6b-183">81332</span><span class="sxs-lookup"><span data-stu-id="6ba6b-183">81332</span></span> | <span data-ttu-id="6ba6b-184">1</span><span class="sxs-lookup"><span data-stu-id="6ba6b-184">1</span></span>             | <span data-ttu-id="6ba6b-185">99</span><span class="sxs-lookup"><span data-stu-id="6ba6b-185">99</span></span>            | <span data-ttu-id="6ba6b-186">50 $</span><span class="sxs-lookup"><span data-stu-id="6ba6b-186">$50</span></span>            |
| <span data-ttu-id="6ba6b-187">81333</span><span class="sxs-lookup"><span data-stu-id="6ba6b-187">81333</span></span> | <span data-ttu-id="6ba6b-188">2</span><span class="sxs-lookup"><span data-stu-id="6ba6b-188">2</span></span>             | <span data-ttu-id="6ba6b-189">11</span><span class="sxs-lookup"><span data-stu-id="6ba6b-189">11</span></span>            | <span data-ttu-id="6ba6b-190">30 $</span><span class="sxs-lookup"><span data-stu-id="6ba6b-190">$30</span></span>            |
| <span data-ttu-id="6ba6b-191">81334</span><span class="sxs-lookup"><span data-stu-id="6ba6b-191">81334</span></span> | <span data-ttu-id="6ba6b-192">3</span><span class="sxs-lookup"><span data-stu-id="6ba6b-192">3</span></span>             | <span data-ttu-id="6ba6b-193">99</span><span class="sxs-lookup"><span data-stu-id="6ba6b-193">99</span></span>            | <span data-ttu-id="6ba6b-194">10 $</span><span class="sxs-lookup"><span data-stu-id="6ba6b-194">$10</span></span>            |
| <span data-ttu-id="6ba6b-195">81334</span><span class="sxs-lookup"><span data-stu-id="6ba6b-195">81334</span></span> | <span data-ttu-id="6ba6b-196">3</span><span class="sxs-lookup"><span data-stu-id="6ba6b-196">3</span></span>             | <span data-ttu-id="6ba6b-197">21</span><span class="sxs-lookup"><span data-stu-id="6ba6b-197">21</span></span>            | <span data-ttu-id="6ba6b-198">5 $</span><span class="sxs-lookup"><span data-stu-id="6ba6b-198">$5</span></span>             |

<span data-ttu-id="6ba6b-199">Koska automaattinen kulumääritys on määritetty jaettavaksi suhteellisesti vastaaville myyntiriveille, järjestelmää suorittaa seuraavat laskelmat.</span><span class="sxs-lookup"><span data-stu-id="6ba6b-199">Because the auto-charge configuration is set to prorate to matching sales lines, the system performs the following calculation steps.</span></span>

1. <span data-ttu-id="6ba6b-200">Kaikki nimikkeet, joilla on sama toimitustapa, ryhmitetään yhteen, ja järjestelmä laskee ryhmän nimikkeiden tuotearvon yhteensä.</span><span class="sxs-lookup"><span data-stu-id="6ba6b-200">All items that have the same mode of delivery are grouped together, and the system calculates the total product value of the items in the group.</span></span>

    <span data-ttu-id="6ba6b-201">**Toimitustapa 11**</span><span class="sxs-lookup"><span data-stu-id="6ba6b-201">**Delivery mode 11**</span></span>

    - <span data-ttu-id="6ba6b-202">Nimike 81331, määrä 1 = 10 $</span><span class="sxs-lookup"><span data-stu-id="6ba6b-202">Item 81331, quantity 1 = $10</span></span>
    - <span data-ttu-id="6ba6b-203">Nimike 81333, määrä 2 = 60 $ netto (30 $/yksikkö)</span><span class="sxs-lookup"><span data-stu-id="6ba6b-203">Item 81333, quantity 2 = $60 net ($30 per unit)</span></span>
    - <span data-ttu-id="6ba6b-204">**Toimitustavan 11 tuotearvo yhteensä = 70 $**</span><span class="sxs-lookup"><span data-stu-id="6ba6b-204">**Total product value for delivery mode 11 = $70**</span></span>

    <span data-ttu-id="6ba6b-205">**Toimitustapa 99**</span><span class="sxs-lookup"><span data-stu-id="6ba6b-205">**Delivery mode 99**</span></span>

    - <span data-ttu-id="6ba6b-206">Nimike 81332, määrä 1 = 50 $</span><span class="sxs-lookup"><span data-stu-id="6ba6b-206">Item 81332, quantity 1 = $50</span></span>
    - <span data-ttu-id="6ba6b-207">Nimike 81334, määrä 3 = 30 $ netto</span><span class="sxs-lookup"><span data-stu-id="6ba6b-207">Item 81334, quantity 3 = $30 net</span></span>
    - <span data-ttu-id="6ba6b-208">**Toimitustavan 99 tuotearvo yhteensä = 80 $**</span><span class="sxs-lookup"><span data-stu-id="6ba6b-208">**Total product value for delivery mode 99 = $80**</span></span>

    <span data-ttu-id="6ba6b-209">**Toimitustapa 21**</span><span class="sxs-lookup"><span data-stu-id="6ba6b-209">**Delivery mode 21**</span></span>

    - <span data-ttu-id="6ba6b-210">Nimike 81334, määrä 3 = 15 $ netto</span><span class="sxs-lookup"><span data-stu-id="6ba6b-210">Item 81334, quantity 3 = $15 net</span></span>
    - <span data-ttu-id="6ba6b-211">**Toimitustavan 21 tuotearvo yhteensä = 15 $**</span><span class="sxs-lookup"><span data-stu-id="6ba6b-211">**Total product value for delivery mode 21 = $15**</span></span>

2. <span data-ttu-id="6ba6b-212">Järjestelmä etsii sellaisen otsikkotason automaattisten kulujen määrityksen, joka vastaa asiakkaan ja kunkin nimikeryhmän toimitustapa-asetuksia.</span><span class="sxs-lookup"><span data-stu-id="6ba6b-212">The system looks for the configuration for header-level auto-charges that matches the customer and mode of delivery settings for each group of items.</span></span> <span data-ttu-id="6ba6b-213">Jos määritys löytyy, järjestelmä etsii tasomäärityksestä käytettävän kulun toimitustaparyhmän nimikkeiden tuotearvon kokonaissumman perusteella.</span><span class="sxs-lookup"><span data-stu-id="6ba6b-213">If the configuration is found, the system looks in the tiered configuration to find the charge that should be applied, based on the total product value of items in the mode of delivery group.</span></span>

    <span data-ttu-id="6ba6b-214">**Toimitustapa 11**</span><span class="sxs-lookup"><span data-stu-id="6ba6b-214">**Delivery mode 11**</span></span>

    - <span data-ttu-id="6ba6b-215">Tuotteen kokonaisarvo = 70 $</span><span class="sxs-lookup"><span data-stu-id="6ba6b-215">Total product value = $70</span></span>
    - <span data-ttu-id="6ba6b-216">**Kulujen arvo = 7 $**</span><span class="sxs-lookup"><span data-stu-id="6ba6b-216">**Charge value = $7**</span></span>

    <span data-ttu-id="6ba6b-217">**Toimitustapa 99**</span><span class="sxs-lookup"><span data-stu-id="6ba6b-217">**Delivery mode 99**</span></span>

    - <span data-ttu-id="6ba6b-218">Tuotteen kokonaisarvo = 80 $</span><span class="sxs-lookup"><span data-stu-id="6ba6b-218">Total product value = $80</span></span>
    - <span data-ttu-id="6ba6b-219">**Kulujen arvo = 15 $**</span><span class="sxs-lookup"><span data-stu-id="6ba6b-219">**Charge value = $15**</span></span>

    <span data-ttu-id="6ba6b-220">**Toimitustapa 21**</span><span class="sxs-lookup"><span data-stu-id="6ba6b-220">**Delivery mode 21**</span></span>

    - <span data-ttu-id="6ba6b-221">Tuotteen kokonaisarvo = 15 $</span><span class="sxs-lookup"><span data-stu-id="6ba6b-221">Total product value = $15</span></span>
    - <span data-ttu-id="6ba6b-222">**Kulujen arvo = 0 $** (tälle asiakas- ja toimitustapayhdistelmälle ei ole määritetty automaattisia kuluja)</span><span class="sxs-lookup"><span data-stu-id="6ba6b-222">**Charge value = $0** (No auto-charges have been configured for this combination of a customer and a mode of delivery.)</span></span>

    ![Toimitustavan 11 kulut menevät korostettuun tasoon](media/step2mode11.png)

    ![Toimitustavan 99 kulut menevät korostettuun tasoon](media/step2mode99.png)

3. <span data-ttu-id="6ba6b-225">Järjestelmä laskee kullakin rivillä käytettävän kulujen arvon sellaisen suhteelliseen jaon logiikan mukaan, joka ottaa huomion rivin suhteellisen arvon suhteessa ryhmän tuotteen kokonaisarvoon.</span><span class="sxs-lookup"><span data-stu-id="6ba6b-225">The system calculates the charge value that should be applied to each line, based on proration logic that considers the proportional value of the line in relation to the group's total product value.</span></span>

    <span data-ttu-id="6ba6b-226">**Toimitustapa 11**</span><span class="sxs-lookup"><span data-stu-id="6ba6b-226">**Delivery mode 11**</span></span>

    - <span data-ttu-id="6ba6b-227">Kulujen arvo = 7 $</span><span class="sxs-lookup"><span data-stu-id="6ba6b-227">Charge value = $7</span></span>
    - <span data-ttu-id="6ba6b-228">Ryhmän tuotteen arvo = 70 $</span><span class="sxs-lookup"><span data-stu-id="6ba6b-228">Group product value = $70</span></span>
    - <span data-ttu-id="6ba6b-229">Rivin 1 arvo = 10 $ (= 14,2857 prosenttia ryhmän arvosta)</span><span class="sxs-lookup"><span data-stu-id="6ba6b-229">Line 1 value = $10 (= 14.2857 percent of the group value)</span></span>
    - <span data-ttu-id="6ba6b-230">Rivin 3 arvo = 60 $ (= 85,7143 prosenttia ryhmän arvosta)</span><span class="sxs-lookup"><span data-stu-id="6ba6b-230">Line 3 value = $60 (= 85.7143 percent of the group value)</span></span>
    - <span data-ttu-id="6ba6b-231">**Rivin 1 rivin kulu = 1 $**</span><span class="sxs-lookup"><span data-stu-id="6ba6b-231">**Line charge for line 1 = $1**</span></span>
    - <span data-ttu-id="6ba6b-232">**Rivin 3 rivin kulu = 6 $**</span><span class="sxs-lookup"><span data-stu-id="6ba6b-232">**Line charge for line 3 = $6**</span></span>

    <span data-ttu-id="6ba6b-233">**Toimitustapa 99**</span><span class="sxs-lookup"><span data-stu-id="6ba6b-233">**Delivery mode 99**</span></span>

    - <span data-ttu-id="6ba6b-234">Kulujen arvo = 15 $</span><span class="sxs-lookup"><span data-stu-id="6ba6b-234">Charge value = $15</span></span>
    - <span data-ttu-id="6ba6b-235">Ryhmän tuotteen arvo = 80 $</span><span class="sxs-lookup"><span data-stu-id="6ba6b-235">Group product value = $80</span></span>
    - <span data-ttu-id="6ba6b-236">Rivin 2 arvo = 50 $ (= 62,5 prosenttia ryhmän arvosta)</span><span class="sxs-lookup"><span data-stu-id="6ba6b-236">Line 2 value = $50 (= 62.5 percent of the group value)</span></span>
    - <span data-ttu-id="6ba6b-237">Rivin 4 arvo = 30 $ (= 37,5 prosenttia ryhmän arvosta)</span><span class="sxs-lookup"><span data-stu-id="6ba6b-237">Line 4 value = $30 (= 37.5 percent of the group value)</span></span>
    - <span data-ttu-id="6ba6b-238">**Rivin 2 rivin kulu = 9,38 $**</span><span class="sxs-lookup"><span data-stu-id="6ba6b-238">**Line charge for line 2 = $9.38**</span></span>
    - <span data-ttu-id="6ba6b-239">**Rivin 4 rivin kulu = 5,62 $**</span><span class="sxs-lookup"><span data-stu-id="6ba6b-239">**Line charge for line 4 = $5.62**</span></span>

    <span data-ttu-id="6ba6b-240">**Toimitustapa 21**</span><span class="sxs-lookup"><span data-stu-id="6ba6b-240">**Delivery mode 21**</span></span>

    - <span data-ttu-id="6ba6b-241">Kulujen arvo = 0 $</span><span class="sxs-lookup"><span data-stu-id="6ba6b-241">Charge value = $0</span></span>
    - <span data-ttu-id="6ba6b-242">Ryhmän tuotteen arvo = 15 $</span><span class="sxs-lookup"><span data-stu-id="6ba6b-242">Group product value = $15</span></span>
    - <span data-ttu-id="6ba6b-243">Rivin 5 arvo = 15 $ (= 100 prosenttia ryhmän arvosta)</span><span class="sxs-lookup"><span data-stu-id="6ba6b-243">Line 5 value = $15 (= 100 percent of the group value)</span></span>
    - <span data-ttu-id="6ba6b-244">**Rivin 5 rivin kulu = 0 $**</span><span class="sxs-lookup"><span data-stu-id="6ba6b-244">**Line charge for line 5 = $0**</span></span>

<span data-ttu-id="6ba6b-245">Tämän vuoksi tässä esimerkissä nimikkeelle 81334 määritetään rahtikuluksi 5,62 $.</span><span class="sxs-lookup"><span data-stu-id="6ba6b-245">Therefore, for this example, item 81334 will be assigned a freight charge of $5.62.</span></span> <span data-ttu-id="6ba6b-246">Voit tarkastella näitä kuluja myyntirivin **Kulujen ylläpito** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="6ba6b-246">You can view these charges on the **Maintain charges** page for the sales line.</span></span> <span data-ttu-id="6ba6b-247">Seuraava kuva osoittaa, miltä kyseinen sivu näyttää nimikkeelle 81334.</span><span class="sxs-lookup"><span data-stu-id="6ba6b-247">The following illustration shows what this page looks like for item 81334.</span></span>

![Nimikkeen 81334 myyntirivin suhteellisesti jaetut kulut](media/proratedlinecharge.png)

<span data-ttu-id="6ba6b-249">Kun tätä laskentamenetelmää käytetään osittaisen palautuksen skenaariossa, jossa kulukoodi on palautettavissa, vain osa kyseiselle riville kohdistetusta kulusta palautetaan nimikkeen palautuksen yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="6ba6b-249">When this method of calculation is used in a partial return scenario, if the charge code is refundable, only the part of the charge that is allocated to that line will be refunded when the item is returned.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6ba6b-250">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="6ba6b-250">Additional resources</span></span>

[<span data-ttu-id="6ba6b-251">Omnikanavan automaattiset etukäteisveloitukset</span><span class="sxs-lookup"><span data-stu-id="6ba6b-251">Omni-channel advanced auto charges</span></span>](omni-auto-charges.md)

[<span data-ttu-id="6ba6b-252">Automaattisten veloitusten käyttöönotto ja määritys kanavan mukaan</span><span class="sxs-lookup"><span data-stu-id="6ba6b-252">Enable and configure auto charges by channel</span></span>](auto-charges-by-channel.md)
