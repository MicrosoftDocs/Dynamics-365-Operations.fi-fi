---
title: Täydennysmenetelmät ja määrän muokkaus
description: Tässä ohjeaiheessa on tietoja täydennystavoista suunnittelun optimoinnissa. Osassa kerrotaan myös, miten tuotteen usean tilauksen määrä vaikuttaa tulokseen.
author: crytt
ms.date: 6/1/2021
ms.topic: article
ms.search.form: ReqGroup, ReqItemTable, InventItemOrderSetup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-06-01
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d5e0e671e624de2646a47647ef08d3567599b884
ms.sourcegitcommit: 4cbd83e21a78459e4711a2dedba0f5a7acc3c841
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/15/2021
ms.locfileid: "6261693"
---
# <a name="replenishment-methods-and-quantity-modification"></a><span data-ttu-id="ecb92-104">Täydennysmenetelmät ja määrän muokkaus</span><span class="sxs-lookup"><span data-stu-id="ecb92-104">Replenishment methods and quantity modification</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ecb92-105">Tässä ohjeaiheessa on tietoja täydennystavoista suunnittelun optimoinnissa.</span><span class="sxs-lookup"><span data-stu-id="ecb92-105">This topic provides information about replenishment methods in Planning Optimization.</span></span> <span data-ttu-id="ecb92-106">Osassa kerrotaan myös, miten tuotteen usean tilauksen määrä vaikuttaa tulokseen.</span><span class="sxs-lookup"><span data-stu-id="ecb92-106">It also explains how the multiple order quantity for a product affects the result.</span></span>

<span data-ttu-id="ecb92-107">Täydennysmenetelmiä kutsutaan myös kattavuusmenetelmiksi ja eräsyiden koon menetelmiksi.</span><span class="sxs-lookup"><span data-stu-id="ecb92-107">Replenishment methods are also known as coverage methods and lot-sizing methods.</span></span>

## <a name="coverage-codes"></a><span data-ttu-id="ecb92-108">Kattavuuskoodit</span><span class="sxs-lookup"><span data-stu-id="ecb92-108">Coverage codes</span></span>

<span data-ttu-id="ecb92-109">Suunnittelun optimointi voidaan määrittää käyttämään erilaisia täydennysmenetelmiä.</span><span class="sxs-lookup"><span data-stu-id="ecb92-109">Planning Optimization can be configured to use different replenishment methods.</span></span> <span data-ttu-id="ecb92-110">Täydennysmenetelmät ovat tekniikoita, joiden avulla järjestelmä laskee vaatimuksia tuotteelle.</span><span class="sxs-lookup"><span data-stu-id="ecb92-110">The replenishment methods are the techniques that the system uses to calculate requirements for a product.</span></span> <span data-ttu-id="ecb92-111">Täydennysmenetelmät määritetään kattavuuskoodien avulla, jotka voit määrittää joko kattavuusryhmälle tai tuotteelle.</span><span class="sxs-lookup"><span data-stu-id="ecb92-111">Replenishment methods are defined by coverage codes that you can set up on either the coverage group or the product.</span></span>

<span data-ttu-id="ecb92-112">Suunnittelun optimoinnissa voidaan käyttää seuraavia kattavuuskoodeja:</span><span class="sxs-lookup"><span data-stu-id="ecb92-112">The following coverage codes can be used in Planning Optimization:</span></span>

- <span data-ttu-id="ecb92-113">**Kausi** – Täydennysmenetelmä, joka yhdistää kausikohtaisen kysynnän tuotteen yhteen tilaukseen.</span><span class="sxs-lookup"><span data-stu-id="ecb92-113">**Period** – The replenishment method combines all the demand for a period into one order for the product.</span></span> <span data-ttu-id="ecb92-114">Tilaus suunnitellaan kauden ensimmäiselle päivälle, ja sen määrä täyttää määritetyn kauden nettotarpeet.</span><span class="sxs-lookup"><span data-stu-id="ecb92-114">The order will be planned for the first day of the period, and its quantity will fulfill the net requirements during the established period.</span></span> <span data-ttu-id="ecb92-115">Kausi alkaa tuotteen ensimmäisestä kysynnästä ja kattaa määritetyn ajanjakson.</span><span class="sxs-lookup"><span data-stu-id="ecb92-115">The period starts with the first demand of the product and covers the defined length of time.</span></span> <span data-ttu-id="ecb92-116">Seuraava kausi alkaa tuotteen seuraavista tarpeista.</span><span class="sxs-lookup"><span data-stu-id="ecb92-116">The next period will start with the next requirements of the product.</span></span> <span data-ttu-id="ecb92-117">*Kauden* kattavuuskoodia käytetään usein ei-ennustettavissa olevan varaston asettaan, vuodenajan vaikutteille tai suurille kustannuksille.</span><span class="sxs-lookup"><span data-stu-id="ecb92-117">The *Period* coverage code is often used for non-predictable inventory draw, season-influenced products, or high-cost products.</span></span> <span data-ttu-id="ecb92-118">Seuraavassa kuvassa on esimerkki.</span><span class="sxs-lookup"><span data-stu-id="ecb92-118">The following illustration shows an example.</span></span>

    <span data-ttu-id="ecb92-119">![Esimerkki kauden kattavuuskoodin käytöstä](./media/coverage-code-period.png "Esimerkki kauden kattavuuskoodin käytöstä")</span><span class="sxs-lookup"><span data-stu-id="ecb92-119">![Example of Period coverage code use](./media/coverage-code-period.png "Example of Period coverage code use")</span></span>

- <span data-ttu-id="ecb92-120">**Vaatimus** – Täydennysmenetelmä, jossa järjestelmä luo nimikkeelle tarpeen mukaan suunnitellun osto-, siirto- tai tuotantotilauksen.</span><span class="sxs-lookup"><span data-stu-id="ecb92-120">**Requirement** – In the replenishment method, the system creates a planned purchase, transfer, or production order per requirement for the product.</span></span> <span data-ttu-id="ecb92-121">Tätä menetelmää käytetään kalliita tuotteita varten, joilla on ajoittainen kysyntä.</span><span class="sxs-lookup"><span data-stu-id="ecb92-121">This method is used for expensive products that have intermittent demand.</span></span> <span data-ttu-id="ecb92-122">*Vaatimuksen* kattavuuskoodia käytetään usein konfiguroitavissa tuotteissa tai valmistus tilattaessa -tapauksissa.</span><span class="sxs-lookup"><span data-stu-id="ecb92-122">The *Requirement* coverage code is often used for configurable products or make-to-order scenarios.</span></span> <span data-ttu-id="ecb92-123">Seuraavassa kuvassa on esimerkki.</span><span class="sxs-lookup"><span data-stu-id="ecb92-123">The following illustration shows an example.</span></span>

    <span data-ttu-id="ecb92-124">![Esimerkki vaatimuksen kattavuuskoodin käytöstä](./media/coverage-code-requirement.png "Esimerkki vaatimuksen kattavuuskoodin käytöstä")</span><span class="sxs-lookup"><span data-stu-id="ecb92-124">![Example of Requirement coverage code use](./media/coverage-code-requirement.png "Example of Requirement coverage code use")</span></span>

- <span data-ttu-id="ecb92-125">**Min./Maks.**</span><span class="sxs-lookup"><span data-stu-id="ecb92-125">**Min./Max.**</span></span> <span data-ttu-id="ecb92-126">– Täydennysmenetelmä perustuu varastotasoon.</span><span class="sxs-lookup"><span data-stu-id="ecb92-126">– The replenishment method is based on the inventory level.</span></span> <span data-ttu-id="ecb92-127">Se määrittää varaston täydennyksen tietylle tasolle, kun arvioitu käytettävissä olevan varaston taso alittaa tietyn raja-arvon.</span><span class="sxs-lookup"><span data-stu-id="ecb92-127">It defines the replenishment of inventory up to a specific level when the predicted on-hand level is below a specific threshold.</span></span> <span data-ttu-id="ecb92-128">Täydennysmäärä on enimmäistason ja ennustetun käytettävissä olevan tason välinen erotus.</span><span class="sxs-lookup"><span data-stu-id="ecb92-128">The replenishment quantity will be the difference between the maximum level and the predicted on-hand level.</span></span> <span data-ttu-id="ecb92-129">*Min./maks.*</span><span class="sxs-lookup"><span data-stu-id="ecb92-129">The *Min./Max.*</span></span> <span data-ttu-id="ecb92-130">-kattavuuskoodia käytetään usein ennustettavissa olevan varaston laatimiseen, korkean tason tai vähemmän kalliiden tuotteiden osalta.</span><span class="sxs-lookup"><span data-stu-id="ecb92-130">coverage code is often used for predictable inventory draw, high runners, or less expensive products.</span></span> <span data-ttu-id="ecb92-131">Seuraavassa kuvassa on esimerkki.</span><span class="sxs-lookup"><span data-stu-id="ecb92-131">The following illustration shows an example.</span></span>

    <span data-ttu-id="ecb92-132">![Esimerkki min.-/maks.-kattavuuskoodin käytöstä](./media/coverage-code-min-max.png "Esimerkki min.-/maks.-kattavuuskoodin käytöstä")</span><span class="sxs-lookup"><span data-stu-id="ecb92-132">![Example of Min./Max. coverage code use](./media/coverage-code-min-max.png "Example of Min./Max. coverage code use")</span></span>

- <span data-ttu-id="ecb92-133">**Manuaalinen** –Täydennysmenetelmä, jossa järjestelmä ei ehdota tuotteelle osto-, siirto- tai tuotantotilauksia.</span><span class="sxs-lookup"><span data-stu-id="ecb92-133">**Manual** – In the replenishment method, the system doesn't suggest purchase, transfer, or production orders for the product.</span></span> <span data-ttu-id="ecb92-134">Sen sijaan tuotteen suunnittelu vastaa tarvittavien tilausten luomisesta tuotteen täydentämiseen.</span><span class="sxs-lookup"><span data-stu-id="ecb92-134">Instead, the planner for the product is responsible for creating the required orders for the replenishment of the product.</span></span> <span data-ttu-id="ecb92-135">*Manuaalista* kattavuuskoodia käytetään usein niiden tuotteiden yhteydessä, joista järjestelmän luomia suunniteltuja tilauksia ei ole tarkoitus luoda.</span><span class="sxs-lookup"><span data-stu-id="ecb92-135">The *Manual* coverage code is often used for products that system-generated planned orders aren't wanted for.</span></span>

## <a name="impact-of-the-order-quantity-from-default-order-settings"></a><span data-ttu-id="ecb92-136">Tilauksen määrän vaikutus oletustilausasetuksista</span><span class="sxs-lookup"><span data-stu-id="ecb92-136">Impact of the order quantity from default order settings</span></span>

<span data-ttu-id="ecb92-137">Voit määrittää vapautetun tuotteen **oletustilausasetus**-sivulla **ostotilauksen**, **varaston** ja **myyntitilauksen** pikavälilehtien seuraavat määräasetukset.</span><span class="sxs-lookup"><span data-stu-id="ecb92-137">On the **Default order setting** page for a released product, you can specify each of following quantity settings on the **Purchase order**, **Inventory**, and **Sales order** FastTabs.</span></span> <span data-ttu-id="ecb92-138">( **Varasto**-pikavälilehtiä käytetään sekä siirtotilauksissa että tuotantotilauksissa.)</span><span class="sxs-lookup"><span data-stu-id="ecb92-138">(The **Inventory** FastTab is used for both transfer orders and production orders.)</span></span>

- <span data-ttu-id="ecb92-139">**Kerrannainen**– Suunnitelluista tilauksista tulee tämän määrän kerrannainen.</span><span class="sxs-lookup"><span data-stu-id="ecb92-139">**Multiple** – Planned orders will be a multiple of this quantity.</span></span>

    <span data-ttu-id="ecb92-140">Jos esimerkiksi **kerrannainen**-kentän arvo on *5*, tilauksen määrä voi olla 5, 10, 15, 20 ja niin edelleen.</span><span class="sxs-lookup"><span data-stu-id="ecb92-140">For example, if the **Multiple** field is set to *5*, an order can be for a quantity of 5, 10, 15, 20, and so on.</span></span>

- <span data-ttu-id="ecb92-141">**Tilauksen vähimmäismäärä** – Suunniteltujen tilausten määrä ei ole pienempi kuin määritetty arvo.</span><span class="sxs-lookup"><span data-stu-id="ecb92-141">**Min. order quantity** – Planned orders won't be less than the specified value.</span></span>

    <span data-ttu-id="ecb92-142">Jos tilauksen **vähimmäistilausmäärä**-kentän arvoksi määritetään esimerkiksi *10*, luodaan 10:n määrän suunniteltu tilaus, vaikka kysynnän täyttämiseen tarvitaan vain neljä.</span><span class="sxs-lookup"><span data-stu-id="ecb92-142">For example, if the **Min. order quantity** field is set to *10*, a planned order for a quantity of 10 will be created, even if only four are required to fulfill the demand.</span></span>

- <span data-ttu-id="ecb92-143">**Tilauksen enimmäismäärä** – Suunniteltujen tilausten määrä ei ylitä määritettyä arvoa.</span><span class="sxs-lookup"><span data-stu-id="ecb92-143">**Max. order quantity** – Planned orders won't exceed the specified value.</span></span> <span data-ttu-id="ecb92-144">Jos kysyntä on suurempi kuin **Tilauksen enimmäismäärä** -arvo, luodaan useita suunniteltuja tilauksia sen kattamiseksi.</span><span class="sxs-lookup"><span data-stu-id="ecb92-144">If the demand is more than the **Max. order quantity** value, multiple planned orders will be created to cover it.</span></span>

    <span data-ttu-id="ecb92-145">Jos esimerkiksi **Tilauksen enimmäismäärä** -kentän arvoksi määritetään *100* ja kysyntä on 450, ohjelma luo neljä suunniteltua tilausta määrälle 100 ja yhden suunnitellun tilauksen määräksi 50.</span><span class="sxs-lookup"><span data-stu-id="ecb92-145">For example, if the **Max. order quantity** field is set to *100*, and the demand is 450, four planned orders for a quantity of 100 and one planned order for a quantity of 50 will be created.</span></span>

## <a name="examples-of-replenishment-that-use-the-minmax-coverage-code"></a><span data-ttu-id="ecb92-146">Esimerkkejä täydennyksestä, jotka käyttävät min./maks.-kohdetta.</span><span class="sxs-lookup"><span data-stu-id="ecb92-146">Examples of replenishment that use the Min./Max.</span></span> <span data-ttu-id="ecb92-147">kattavuuskoodi</span><span class="sxs-lookup"><span data-stu-id="ecb92-147">coverage code</span></span>

<span data-ttu-id="ecb92-148">Jos tuotteen **Kerrannais**-kentässä ei ole arvoa **oletustilausasetus** sivulla ja jos käytössä on *minimi-/maksimiarvo*.</span><span class="sxs-lookup"><span data-stu-id="ecb92-148">If you don't specify a value in the **Multiple** field for a product on the **Default order setting** page, and if you're using the *Min./Max.*</span></span> <span data-ttu-id="ecb92-149">täydennysmenetelmä, suunnittelun optimointi täydentää varaston, kun arvioitu käytettävissä olevan varaston taso alittaa tietyn raja-arvon.</span><span class="sxs-lookup"><span data-stu-id="ecb92-149">replenishment method, Planning Optimization will replenish the inventory up to a specific level when the predicted on-hand level is below a specific threshold.</span></span>

<span data-ttu-id="ecb92-150">Jos määrität tuotteelle useita määriä, *minimi-/maksimimäärä*</span><span class="sxs-lookup"><span data-stu-id="ecb92-150">If you define a multiple quantity for a product, the *Min./Max.*</span></span> <span data-ttu-id="ecb92-151">täydennysmenetelmä muuttaa toimintatapaansa ja ottaa **kerrannais**-arvon huomioon.</span><span class="sxs-lookup"><span data-stu-id="ecb92-151">replenishment method changes its behavior and considers the **Multiple** value.</span></span>

<span data-ttu-id="ecb92-152">Toisin sanoen suunnittelun optimointi täydentää varastoa määritetylle maksimitasolle, kun käytettävissä olevan varaston arvioitu taso on pienempi kuin määritetty minimitaso.</span><span class="sxs-lookup"><span data-stu-id="ecb92-152">In other words, Planning Optimization will still replenish the inventory up to the defined maximum level when the predicted on-hand level is less than the defined minimum level.</span></span> <span data-ttu-id="ecb92-153">Täydennysmäärän on kuitenkin oltava **Kerrannainen**-arvon kerrannainen.</span><span class="sxs-lookup"><span data-stu-id="ecb92-153">However, the replenishment quantity must be a multiple of the **Multiple** value.</span></span>

<span data-ttu-id="ecb92-154">Jos täydennysmäärä (maksimitason ja arvioidun varastotason välinen ero) ei ole määritetyn usean määrän kerrannainen, suunnittelun optimointi käyttää ensimmäistä mahdollista arvoa, joka yhdessä arvioidun käytettävissä olevan tason kanssa alittaa maksimitason.</span><span class="sxs-lookup"><span data-stu-id="ecb92-154">If the replenishment quantity (the difference between the maximum level and the predicted on-hand level) isn't a multiple of the defined multiple quantity, Planning Optimization uses the first possible value that, together with predicted on-hand level, will be below the maximum level.</span></span> <span data-ttu-id="ecb92-155">Jos summa on pienempi kuin vähimmäistaso, suunnittelun optimointi käyttää ensimmäistä arvoa, joka yhdessä arvioidun varastoarvon kanssa on maksimitasoa suurempi.</span><span class="sxs-lookup"><span data-stu-id="ecb92-155">If the sum is less than the minimum level, Planning Optimization uses the first value that, together with predicted on-hand, will be above the maximum level.</span></span>

<span data-ttu-id="ecb92-156">Seuraavissa osa-alueen esimerkeissä on esimerkkejä, jotka osoittavat, miten tuotteen usean tilauksen määrä vaikuttaa *minimi-/maksimi*-kentän tulokseen.</span><span class="sxs-lookup"><span data-stu-id="ecb92-156">The following subsections provide some examples that show how the multiple order quantity for a product affects the result of the *Min./Max.*</span></span> <span data-ttu-id="ecb92-157">täydennysmenetelmä.</span><span class="sxs-lookup"><span data-stu-id="ecb92-157">replenishment method.</span></span>

### <a name="example-1"></a><span data-ttu-id="ecb92-158">Esimerkki 1</span><span class="sxs-lookup"><span data-stu-id="ecb92-158">Example 1</span></span>

<span data-ttu-id="ecb92-159">Tuotteella on seuraava konfiguraatio:</span><span class="sxs-lookup"><span data-stu-id="ecb92-159">A product has the following configuration:</span></span>

- <span data-ttu-id="ecb92-160">**Kattavuuskoodi:** *Min./Maks.*</span><span class="sxs-lookup"><span data-stu-id="ecb92-160">**Coverage code:** *Min./Max.*</span></span>
- <span data-ttu-id="ecb92-161">**Minimi:** *15*</span><span class="sxs-lookup"><span data-stu-id="ecb92-161">**Minimum:** *15*</span></span>
- <span data-ttu-id="ecb92-162">**Maksimi:** *22*</span><span class="sxs-lookup"><span data-stu-id="ecb92-162">**Maximum:** *22*</span></span>
- <span data-ttu-id="ecb92-163">**Kerrannainen:** *0*</span><span class="sxs-lookup"><span data-stu-id="ecb92-163">**Multiple:** *0*</span></span>

<span data-ttu-id="ecb92-164">Tuotteella on 10 kappaletta käyttövarastoa, eikä siinä ole muuta kysyntää tai toimitusta.</span><span class="sxs-lookup"><span data-stu-id="ecb92-164">There are 10 pieces of on-hand inventory for the product, and there is no other demand or supply.</span></span>

<span data-ttu-id="ecb92-165">Pääsuunnittelun ajon yhteydessä luodaan suunniteltu 12 kappaleen tilaus, joka täydentää varastoa maksimimäärään.</span><span class="sxs-lookup"><span data-stu-id="ecb92-165">When master planning runs, a planned order for 12 pieces is created to replenish inventory to the maximum quantity.</span></span>

### <a name="example-2"></a><span data-ttu-id="ecb92-166">Esimerkki 2</span><span class="sxs-lookup"><span data-stu-id="ecb92-166">Example 2</span></span>

<span data-ttu-id="ecb92-167">Tuotteella on seuraava konfiguraatio:</span><span class="sxs-lookup"><span data-stu-id="ecb92-167">A product has the following configuration:</span></span>

- <span data-ttu-id="ecb92-168">**Kattavuuskoodi:** *Min./Maks.*</span><span class="sxs-lookup"><span data-stu-id="ecb92-168">**Coverage code:** *Min./Max.*</span></span>
- <span data-ttu-id="ecb92-169">**Minimi:** *15*</span><span class="sxs-lookup"><span data-stu-id="ecb92-169">**Minimum:** *15*</span></span>
- <span data-ttu-id="ecb92-170">**Maksimi:** *22*</span><span class="sxs-lookup"><span data-stu-id="ecb92-170">**Maximum:** *22*</span></span>
- <span data-ttu-id="ecb92-171">**Kerrannainen:** *5*</span><span class="sxs-lookup"><span data-stu-id="ecb92-171">**Multiple:** *5*</span></span>

<span data-ttu-id="ecb92-172">Tuotteella on 10 kappaletta käyttövarastoa, eikä siinä ole muuta kysyntää tai toimitusta.</span><span class="sxs-lookup"><span data-stu-id="ecb92-172">There are 10 pieces of on-hand inventory for the product, and there is no other demand or supply.</span></span>

<span data-ttu-id="ecb92-173">Kun pääsuunnittelu suoritetaan, luodaan suunniteltu 10 kappaleen tilaus (koska 15 kappaletta täydennystä sekä 10 käytettävissä olevan varaston kappaletta ylittävät enimmäismäärän).</span><span class="sxs-lookup"><span data-stu-id="ecb92-173">When master planning runs, a planned order for 10 pieces is created (because 15 pieces of replenishment plus 10 pieces of on-hand inventory will exceed the maximum quantity).</span></span>

### <a name="example-3"></a><span data-ttu-id="ecb92-174">Esimerkki 3</span><span class="sxs-lookup"><span data-stu-id="ecb92-174">Example 3</span></span>

<span data-ttu-id="ecb92-175">Tuotteella on seuraava konfiguraatio:</span><span class="sxs-lookup"><span data-stu-id="ecb92-175">A product has the following configuration:</span></span>

- <span data-ttu-id="ecb92-176">**Kattavuuskoodi:** *Min./Maks.*</span><span class="sxs-lookup"><span data-stu-id="ecb92-176">**Coverage code:** *Min./Max.*</span></span>
- <span data-ttu-id="ecb92-177">**Minimi:** *21*</span><span class="sxs-lookup"><span data-stu-id="ecb92-177">**Minimum:** *21*</span></span>
- <span data-ttu-id="ecb92-178">**Maksimi:** *24*</span><span class="sxs-lookup"><span data-stu-id="ecb92-178">**Maximum:** *24*</span></span>
- <span data-ttu-id="ecb92-179">**Kerrannainen:** *5*</span><span class="sxs-lookup"><span data-stu-id="ecb92-179">**Multiple:** *5*</span></span>

<span data-ttu-id="ecb92-180">Tuotteella on 10 kappaletta käyttövarastoa, eikä siinä ole muuta kysyntää tai toimitusta.</span><span class="sxs-lookup"><span data-stu-id="ecb92-180">There are 10 pieces of on-hand inventory for the product, and there is no other demand or supply.</span></span>

<span data-ttu-id="ecb92-181">Kun pääsuunnittelu suoritetaan, luodaan suunniteltu 15 kappaleen tilaus (koska 10 kappaletta täydennystä sekä 10 käytettävissä olevan varaston kappaletta alittavat vähimmäismäärän).</span><span class="sxs-lookup"><span data-stu-id="ecb92-181">When master planning runs, the planned order for 15 pieces is created (because 10 pieces of replenishment plus 10 pieces of on-hand inventory will be less than the minimum quantity).</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
