---
title: Varastoinventoinnin syykoodit
description: "Tässä ohjeaiheessa käsitellään inventointitehtävin syykoodin määrittämistä ja käyttämistä."
author: Mirzaab
manager: AnnBe
ms.date: 03/15/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventCountingReasonCodePolicy
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 8.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 0d787dac50374af11d878652103145c9ae9b6877
ms.contentlocale: fi-fi
ms.lasthandoff: 05/08/2018

---

# <a name="reason-codes-for-inventory-counting"></a><span data-ttu-id="2e55d-103">Varastoinventoinnin syykoodit</span><span class="sxs-lookup"><span data-stu-id="2e55d-103">Reason codes for inventory counting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2e55d-104">Syykoodien avulla voit analysoida inventointiprosessin tuloksia ja prosessin aikana mahdollisesti esiintyviä ristiriitoja.</span><span class="sxs-lookup"><span data-stu-id="2e55d-104">Reason codes let you analyze the results of a counting process and any discrepancies that occur during that process.</span></span> <span data-ttu-id="2e55d-105">Voit määrittää inventoinnin syyn, kuten vioittuneen kuormalavan tai varasto-otantaan perustuvan varasto-oikaisun.</span><span class="sxs-lookup"><span data-stu-id="2e55d-105">You can specify the reason for doing the count, such as a broken pallet or a stock adjustment that is based on inventory samples.</span></span>

## <a name="recommendation"></a><span data-ttu-id="2e55d-106">Suositus</span><span class="sxs-lookup"><span data-stu-id="2e55d-106">Recommendation</span></span>

<span data-ttu-id="2e55d-107">Ennen järjestelmän määrittämistä kannattaa määrittää syykoodien käyttöstrategia.</span><span class="sxs-lookup"><span data-stu-id="2e55d-107">Before you set up the system, we recommend that you define a strategy for working with reason codes.</span></span> <span data-ttu-id="2e55d-108">Yritä vastata esimerkiksi seuraaviin kysymyksiin:</span><span class="sxs-lookup"><span data-stu-id="2e55d-108">For example, try to answer the following questions:</span></span>

- <span data-ttu-id="2e55d-109">Pitäisikö syykoodien olla pakollisia varastoissa?</span><span class="sxs-lookup"><span data-stu-id="2e55d-109">Should reason codes be mandatory on warehouses?</span></span>
- <span data-ttu-id="2e55d-110">Pitäisikö syykoodien käytön olla pakollista vai valinnaista joidenkin nimikkeiden kanssa?</span><span class="sxs-lookup"><span data-stu-id="2e55d-110">Should reason codes be mandatory or optional on some items?</span></span>
- <span data-ttu-id="2e55d-111">Kuinka monta syykoodia tarvitaan?</span><span class="sxs-lookup"><span data-stu-id="2e55d-111">How many reason codes do you require?</span></span>
- <span data-ttu-id="2e55d-112">Pitäisikö viivakoodinlukijoiden käyttäjien käyttää syykoodeja?</span><span class="sxs-lookup"><span data-stu-id="2e55d-112">How should users of barcode scanners use reason codes?</span></span> <span data-ttu-id="2e55d-113">Pitäisikö syykoodien olla ennalta valittuja, pakollisia tai ei-muokattavissa?</span><span class="sxs-lookup"><span data-stu-id="2e55d-113">Should the reason codes be preselected, mandatory, or not editable?</span></span>
- <span data-ttu-id="2e55d-114">Tarvitsevatko varastotyöntekijät syykoodin, jotka toimivat eri tavalla mobiililaitteissa?</span><span class="sxs-lookup"><span data-stu-id="2e55d-114">Do warehouse workers require different reason code behavior on mobile scanners?</span></span> <span data-ttu-id="2e55d-115">Jos vastaus on myönteinen, voit luoda lisää valikkokohteita ja määrittää ne eri henkilöille.</span><span class="sxs-lookup"><span data-stu-id="2e55d-115">If the answer is yes, you can create more menu items and assign them to different people.</span></span>

## <a name="where-reason-codes-apply"></a><span data-ttu-id="2e55d-116">Syykoodien käyttökohteet</span><span class="sxs-lookup"><span data-stu-id="2e55d-116">Where reason codes apply</span></span>

<span data-ttu-id="2e55d-117">Voit luoda useita syykoodikäytäntöjä. Kullakin syykoodikäytännöllä voi olla kaksi inventoinnin syykoodikäytäntöä.</span><span class="sxs-lookup"><span data-stu-id="2e55d-117">You can create multiple reason code policies, and each reason code policy can have two counting reason code policies.</span></span> <span data-ttu-id="2e55d-118">Inventoinnin syykoodikäytäntöjä voidaan käyttää varasto- tai nimiketasolla.</span><span class="sxs-lookup"><span data-stu-id="2e55d-118">The counting reason code policies can be used at the warehouse level or the item level.</span></span>

## <a name="set-up-reason-code-policies"></a><span data-ttu-id="2e55d-119">Syykoodikäytäntöjen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="2e55d-119">Set up reason code policies</span></span>

1. <span data-ttu-id="2e55d-120">Valitse **Inventoinnin- ja varastonhallinta** \> **Asetukset** \> **Varasto** \> **Inventoinnin syykoodin käytännöt** ja luo uusi syykoodin käytäntö.</span><span class="sxs-lookup"><span data-stu-id="2e55d-120">Select **Inventory management** \> **Setup** \> **Inventory** \> **Counting reason code policies**, and create a new reason code policy.</span></span>
2. <span data-ttu-id="2e55d-121">Valitse **Inventoinnin syykoodin tyyppi** -kentässä joko **Pakollinen** tai **Valinnainen**. Voit määrittää tällä tavoin, onko syykoodin valinta valinnaista vai pakollista jossakin seuraavista inventointikirjauskansioissa:</span><span class="sxs-lookup"><span data-stu-id="2e55d-121">In the **Counting reason code type** field, select either **Mandatory** or **Optional** to specify whether selection of a reason code should be an optional or mandatory action in one of the following counting journals:</span></span>

    - <span data-ttu-id="2e55d-122">Inventointi (mobiililaite)</span><span class="sxs-lookup"><span data-stu-id="2e55d-122">Cycle Count (mobile device)</span></span>
    - <span data-ttu-id="2e55d-123">Pistoinventointi (mobiililaite)</span><span class="sxs-lookup"><span data-stu-id="2e55d-123">Spot Count (mobile device)</span></span>
    - <span data-ttu-id="2e55d-124">Rajainventointi (mobiililaite)</span><span class="sxs-lookup"><span data-stu-id="2e55d-124">Threshold Count (mobile device)</span></span>
    - <span data-ttu-id="2e55d-125">Oikaisu sisään (mobiililaite)</span><span class="sxs-lookup"><span data-stu-id="2e55d-125">Adjustment In (mobile device)</span></span>
    - <span data-ttu-id="2e55d-126">Oikaisu ulos (mobiililaite)</span><span class="sxs-lookup"><span data-stu-id="2e55d-126">Adjustment Out (mobile device)</span></span>
    - <span data-ttu-id="2e55d-127">Inventointikirjauskansio (raskas asiakas)</span><span class="sxs-lookup"><span data-stu-id="2e55d-127">Counting Journal (rich client)</span></span>

<span data-ttu-id="2e55d-128">Voit määrittää syykoodit myös yksittäisille varastoille ja tuotteille.</span><span class="sxs-lookup"><span data-stu-id="2e55d-128">You can also set up reason codes for individual warehouses and for products.</span></span> <span data-ttu-id="2e55d-129">Tuotteiden syykoodiasetukset voivat ohittaa varastojen asetukset.</span><span class="sxs-lookup"><span data-stu-id="2e55d-129">The reason code setup for products can disregard the setup for warehouses.</span></span>

## <a name="mandatory-reason-codes"></a><span data-ttu-id="2e55d-130">Pakolliset syykoodit</span><span class="sxs-lookup"><span data-stu-id="2e55d-130">Mandatory reason codes</span></span>

<span data-ttu-id="2e55d-131">Jos **Pakollinen**-parametri on määritetty varastojen tai nimikkeiden syykoodeissa, inventointikirjauskansiota ei voi viimeistellä ja sulkea, ennen kuin syykoodi on annettu.</span><span class="sxs-lookup"><span data-stu-id="2e55d-131">If the **Mandatory** parameter is set in the configuration of reason codes for warehouses or items, the counting journal can't be completed and closed until a reason code is provided.</span></span>

### <a name="set-up-reason-codes-for-warehouses"></a><span data-ttu-id="2e55d-132">Varastojen syykoodien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="2e55d-132">Set up reason codes for warehouses</span></span>

1. <span data-ttu-id="2e55d-133">Valitse **Varastonhallinta** \> **Asetukset** \> **Varastoerittely** \> **Varastot**.</span><span class="sxs-lookup"><span data-stu-id="2e55d-133">Select **Inventory Management** \> **Setup** \> **Inventory breakdown** \> **Warehouses**.</span></span>
2. <span data-ttu-id="2e55d-134">Valitse **Varasto**-välilehden **Inventoinnin syykoodin käytäntö** -kentässä jokin seuraavista vaihtoehdoista:</span><span class="sxs-lookup"><span data-stu-id="2e55d-134">On the **Warehouse** tab, in the **Counting reason code policy** field, select one of the following options:</span></span>

    - <span data-ttu-id="2e55d-135">**Tyhjä** – nimikkeelle määritetty parametri määrittää, ovatko inventointikirjauskansiot pakollisia tuotteelle.</span><span class="sxs-lookup"><span data-stu-id="2e55d-135">**Blank** – The parameter that is set up for the item is used to determine whether counting journals are mandatory for the product.</span></span>
    - <span data-ttu-id="2e55d-136">**Pakollinen** – varaston inventointikirjauskansiossa on aina käytettävä syykoodia.</span><span class="sxs-lookup"><span data-stu-id="2e55d-136">**Mandatory** – A reason code is always required on counting journals for the warehouse.</span></span>
    - <span data-ttu-id="2e55d-137">**Valinnainen** – syykoodi ei ole pakollinen varaston inventointikirjauskansiossa.</span><span class="sxs-lookup"><span data-stu-id="2e55d-137">**Optional** – A reason code isn't required on counting journals for the warehouse.</span></span>

### <a name="set-up-reason-codes-for-products"></a><span data-ttu-id="2e55d-138">Tuotteiden syykoodien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="2e55d-138">Set up reason codes for products</span></span>

1. <span data-ttu-id="2e55d-139">Valitse **Tuotetietojen hallinta** \> **Tuotteet** \> **Vapautetut tuotteet**.</span><span class="sxs-lookup"><span data-stu-id="2e55d-139">Select **Product information management** \> **Products** \> **Released products**.</span></span>
2. <span data-ttu-id="2e55d-140">Valitse ensin **Tuote**-välilehdessä **Inventoinnin syykoodin käytäntö** ja sitten jokin seuraavista vaihtoehdoista:</span><span class="sxs-lookup"><span data-stu-id="2e55d-140">On the **Product** tab, select **Counting reason code policy**, and then select one of the following options:</span></span>

    - <span data-ttu-id="2e55d-141">**Tyhjä** – varastolle määritetty parametri määrittää, ovatko inventointikirjauskansiot pakollisia tuotteelle.</span><span class="sxs-lookup"><span data-stu-id="2e55d-141">**Blank** – The parameter that is set up for the warehouse is used to determine whether counting journals are mandatory for the product.</span></span>
    - <span data-ttu-id="2e55d-142">**Pakollinen** – Tuotteen inventointikirjauskansiossa on aina käytettävä syykoodia.</span><span class="sxs-lookup"><span data-stu-id="2e55d-142">**Mandatory** – A reason code is always required on counting journals for the product.</span></span> <span data-ttu-id="2e55d-143">Tämä asetus ohittaa varastotason syykoodiasetuksen.</span><span class="sxs-lookup"><span data-stu-id="2e55d-143">This setting overrides any reason code setting at the warehouse level.</span></span>
    - <span data-ttu-id="2e55d-144">**Valinnainen** – syykoodi ei ole pakollinen tuotteen inventointikirjauskansiossa.</span><span class="sxs-lookup"><span data-stu-id="2e55d-144">**Optional** – A reason code isn't required on counting journals for the product.</span></span> <span data-ttu-id="2e55d-145">Tämä asetus ohittaa varastotason syykoodiasetuksen.</span><span class="sxs-lookup"><span data-stu-id="2e55d-145">This setting overrides any reason code setting at the warehouse level.</span></span>

### <a name="use-reason-codes-in-counting-journals"></a><span data-ttu-id="2e55d-146">Syykoodien käyttäminen inventointikirjauskansioissa</span><span class="sxs-lookup"><span data-stu-id="2e55d-146">Use reason codes in counting journals</span></span>

<span data-ttu-id="2e55d-147">Voit lisätä inventointikirjauskansiossa syykoodit seuraaville inventointityypeille:</span><span class="sxs-lookup"><span data-stu-id="2e55d-147">In a counting journal, you can add reason codes for counts of the following types:</span></span>

- <span data-ttu-id="2e55d-148">Inventointi</span><span class="sxs-lookup"><span data-stu-id="2e55d-148">Cycle Count</span></span>
- <span data-ttu-id="2e55d-149">Pistoinventointi</span><span class="sxs-lookup"><span data-stu-id="2e55d-149">Spot Count</span></span>
- <span data-ttu-id="2e55d-150">Rajainventointi</span><span class="sxs-lookup"><span data-stu-id="2e55d-150">Threshold Count</span></span>
- <span data-ttu-id="2e55d-151">Oikaisu sisään</span><span class="sxs-lookup"><span data-stu-id="2e55d-151">Adjustment In</span></span>
- <span data-ttu-id="2e55d-152">Oikaisu ulos</span><span class="sxs-lookup"><span data-stu-id="2e55d-152">Adjustment Out</span></span>

<span data-ttu-id="2e55d-153">Syykoodit lisätään **Inventointikirjauskansio**-tyypin inventointikirjauskansioiden riveille.</span><span class="sxs-lookup"><span data-stu-id="2e55d-153">Reason codes are added to the journal lines in counting journals of the **Counting journal** type.</span></span>

1. <span data-ttu-id="2e55d-154">Valitse **Inventoinnin- ja varastonhallinta** \> **Kirjauskansioviennit** \> **Inventointi** \> **Inventointi**.</span><span class="sxs-lookup"><span data-stu-id="2e55d-154">Select **Inventory management** \> **Journal entries** \> **Item counting** \> **Counting**.</span></span>
2. <span data-ttu-id="2e55d-155">Valitse vaihtoehto inventointikirjauskansion tietojen **Inventoinnin syykoodi** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="2e55d-155">In the line details of the counting journal, in the **Counting reason code** field, select an option.</span></span>

### <a name="view-the-counting-history-as-its-recorded-by-reason-codes"></a><span data-ttu-id="2e55d-156">Inventointihistorian näyttäminen syykoodien mukaan kirjattuna</span><span class="sxs-lookup"><span data-stu-id="2e55d-156">View the counting history as it's recorded by reason codes</span></span>

- <span data-ttu-id="2e55d-157">Valitse ensin **Inventoinnin- ja varastonhallinta** \> **Kyselyt ja raportit** \> **Inventointihistoria** ja sitten tarkastele sitten **Inventoinnin syykoodi** -kentässä syykoodin kautta kirjattua inventointihistoriaa.</span><span class="sxs-lookup"><span data-stu-id="2e55d-157">Select **Inventory management** \> **Inquiries and reports** \> **Counting history**, and then, in the **Counting reason code** field, view the counting history that has been recorded through a reason code.</span></span>

### <a name="use-a-reason-code-for-a-quantity-adjustment"></a><span data-ttu-id="2e55d-158">Määrän muutoksen syykoodin käyttäminen</span><span class="sxs-lookup"><span data-stu-id="2e55d-158">Use a reason code for a quantity adjustment</span></span>

1. <span data-ttu-id="2e55d-159">Valitse **Käytettävissä oleva varasto** -sivulla **Säädä määrää**.</span><span class="sxs-lookup"><span data-stu-id="2e55d-159">On the **On-hand inventory** page, select **Adjust quantity**.</span></span> <span data-ttu-id="2e55d-160">Voit avata **Käytettävissä oleva varasto** -sivu useilla eri tavoilla.</span><span class="sxs-lookup"><span data-stu-id="2e55d-160">You can open the **On-hand inventory** page in several ways.</span></span> <span data-ttu-id="2e55d-161">Valitse esimerkiksi **Inventoinnin- ja varastonhallinta** \> **Kyselyt ja raportit** \> **Käytettävissä oleva varasto**.</span><span class="sxs-lookup"><span data-stu-id="2e55d-161">For example, select **Inventory management** \> **Inquiries and reports** \> **On-hand inventory**.</span></span>
2. <span data-ttu-id="2e55d-162">Valitse ensin **Säädä määrää** ja sitten **Inventoinnin syykoodi** -kentässä syykoodi.</span><span class="sxs-lookup"><span data-stu-id="2e55d-162">Select **Adjust quantity**, and then, in the **Counting reason code** field, select a reason code.</span></span>

### <a name="configure-reason-codes-for-mobile-device-menu-items"></a><span data-ttu-id="2e55d-163">Mobiililaitteen valikkovaihtoehtojen syykoodien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="2e55d-163">Configure reason codes for mobile device menu items</span></span>

<span data-ttu-id="2e55d-164">Voit määrittää syykoodit mille tahansa mobiililaitteen valikkoehdon inventointityypille.</span><span class="sxs-lookup"><span data-stu-id="2e55d-164">You can configure reason codes for any type of count on a mobile device menu item.</span></span> <span data-ttu-id="2e55d-165">Mobiililaitteen valikkovaihtoehdon määritys sisältää seuraavat tiedot:</span><span class="sxs-lookup"><span data-stu-id="2e55d-165">The configuration of the mobile device menu item includes the following information:</span></span>

- <span data-ttu-id="2e55d-166">Syykoodin mahdollinen näyttäminen mobiililaitteen käyttäjälle inventoinnin aikana.</span><span class="sxs-lookup"><span data-stu-id="2e55d-166">Whether the reason code is shown to the mobile device worker during counting.</span></span>
- <span data-ttu-id="2e55d-167">Mobiililaitteen valikkovaihtoehdossa näytettävä oletussyykoodi.</span><span class="sxs-lookup"><span data-stu-id="2e55d-167">The default reason code that is shown on a mobile device menu item.</span></span>
- <span data-ttu-id="2e55d-168">Käyttäjän tekemä syykoodin mahdollinen muokkaus.</span><span class="sxs-lookup"><span data-stu-id="2e55d-168">Whether the user can edit the reason code.</span></span>

### <a name="set-up-reason-codes-on-a-mobile-device"></a><span data-ttu-id="2e55d-169">Syykoodien määrittäminen mobiililaitteessa</span><span class="sxs-lookup"><span data-stu-id="2e55d-169">Set up reason codes on a mobile device</span></span>

1. <span data-ttu-id="2e55d-170">Valitse **Varastonhallinta** \> **Asetukset** \> **Mobiililaite** \> **Mobiililaitteen valikkovaihtoehdot**.</span><span class="sxs-lookup"><span data-stu-id="2e55d-170">Select **Warehouse management** \> **Setup** \> **Mobile device** \> **Mobile device menu items**.</span></span>
2. <span data-ttu-id="2e55d-171">Valitse **Inventointi**-välilehdessä **Inventointi**.</span><span class="sxs-lookup"><span data-stu-id="2e55d-171">On the **Cycle count** tab, select **Cycle counting**.</span></span>
3. <span data-ttu-id="2e55d-172">Määritä **Inventoinnin oletussyykoodi** -kentässä oletussyykoodi, joka on kirjattava, kun inventointi tehdään käyttämällä mobiililaitteen valikkovaihtoehtoa.</span><span class="sxs-lookup"><span data-stu-id="2e55d-172">In the **Default counting reason code** field, set the default reason code that should be recorded when counting is done by using the mobile device menu item.</span></span>
4. <span data-ttu-id="2e55d-173">Valitse **Näytä inventoinnin syykoodi** -kentässä **Rivi** näyttämään syykoodi, kun kukin varianssi on kirjattu.</span><span class="sxs-lookup"><span data-stu-id="2e55d-173">In the **Display counting reason code** field, select **Line** to show the reason code after each variance is recorded.</span></span> <span data-ttu-id="2e55d-174">Vaihtoehtoisesti voit valita **Piilota**, jos syykoodia ei näytetä.</span><span class="sxs-lookup"><span data-stu-id="2e55d-174">Alternatively, select **Hide** if the reason code shouldn't be shown.</span></span>
5. <span data-ttu-id="2e55d-175">Valitse **Muokkaa inventoinnin syykoodia** -asetukseksi joko **Kyllä** tai **Ei**.</span><span class="sxs-lookup"><span data-stu-id="2e55d-175">Set the **Edit counting reason code** option to either **Yes** or **No**.</span></span> <span data-ttu-id="2e55d-176">Jos valitse tässä asetuksessa **Kyllä**, työntekijä voi muokata syykoodia, kun se näytetään mobiililaitteessa inventoinnin aikana.</span><span class="sxs-lookup"><span data-stu-id="2e55d-176">If you set this option to **Yes**, the worker can edit the reason code when it's shown on the mobile device during counting.</span></span>

> [!NOTE]
> <span data-ttu-id="2e55d-177">**Inventointi**-painike voidaan ottaa käyttöön missä tahansa mobiililaitteen valikkovaihtoehdossa, jos inventointi voidaan tehdä.</span><span class="sxs-lookup"><span data-stu-id="2e55d-177">The **Cycle counting** button can be enabled on any mobile device menu item where counting can be done.</span></span> <span data-ttu-id="2e55d-178">Esimerkissä on pistoinventoinnin, käyttäjän ohjaaman työn ja järjestelmän ohjaaman työn valikkovaihtoehtoja.</span><span class="sxs-lookup"><span data-stu-id="2e55d-178">Example include the menu items for spot counts, user-directed work, and system-directed work.</span></span>

## <a name="cycle-count-approvals"></a><span data-ttu-id="2e55d-179">Inventoinnin hyväksynnät</span><span class="sxs-lookup"><span data-stu-id="2e55d-179">Cycle count approvals</span></span>

<span data-ttu-id="2e55d-180">Käyttäjä voi muuttaa inventointiin liitettyä syykoodia ennen inventoinnin hyväksymistä.</span><span class="sxs-lookup"><span data-stu-id="2e55d-180">Before a count is approved, the user can change the reason code that is associated with the count.</span></span> <span data-ttu-id="2e55d-181">Kun inventointi on hyväksytty, syykoodi annetaan inventointikirjauskansion riveille.</span><span class="sxs-lookup"><span data-stu-id="2e55d-181">When the count is approved, the reason code is entered on the counting journal lines.</span></span>

### <a name="modify-cycle-count-approvals"></a><span data-ttu-id="2e55d-182">Inventoinnin hyväksymisten muokkaaminen</span><span class="sxs-lookup"><span data-stu-id="2e55d-182">Modify cycle count approvals</span></span>

1. <span data-ttu-id="2e55d-183">Valitse **Varastonhallinta** \> **Inventointi** \> **Tarkistusta odottava inventointityö**.</span><span class="sxs-lookup"><span data-stu-id="2e55d-183">Select **Warehouse management** \> **Cycle counting** \> **Cycle count work pending review**.</span></span>
2. <span data-ttu-id="2e55d-184">Valitse ensin **Inventointi** ja sitten **Syykoodi**-kentässä uusi syykoodi.</span><span class="sxs-lookup"><span data-stu-id="2e55d-184">Select **Cycle counting**, and then, in the **Reason code** field, select a new reason code.</span></span>

### <a name="modify-the-mobile-device-menu-item-for-adjustment-in-and-adjustment-out"></a><span data-ttu-id="2e55d-185">Mobiililaitteen Oikaisu sisään- ja Oikaisu ulos -valikkovaihtoehdon muokkaaminen</span><span class="sxs-lookup"><span data-stu-id="2e55d-185">Modify the mobile device menu item for Adjustment in and Adjustment out</span></span>

1. <span data-ttu-id="2e55d-186">Valitse ensin **Varastonhallinta** \> **Asetukset** \> **Mobiililaite** \> **Mobiililaitteen valikkovaihtoehdot** ja sitten **Oikaisu sisään ja ulos**.</span><span class="sxs-lookup"><span data-stu-id="2e55d-186">Select **Warehouse management** \> **Setup** \> **Mobile device** \> **Mobile device menu items**, and then select **Adjustment in and out**.</span></span>
2. <span data-ttu-id="2e55d-187">Valitse **Käytä nykyistä työtä** -vaihtoehdossa **Ei**.</span><span class="sxs-lookup"><span data-stu-id="2e55d-187">Set the **Use existing work** option to **No**.</span></span>
3. <span data-ttu-id="2e55d-188">Valitse **Työn luontiprosessi** -kentässä **Oikaisu sisään**.</span><span class="sxs-lookup"><span data-stu-id="2e55d-188">In the **Work creation process** field, select **Adjustment in**.</span></span>

<span data-ttu-id="2e55d-189">Seuraavat kentät lisätään mobiililaitteen valikkovaihtoehtoon, kun **Oikaisu sisään** tai **Oikaisu ulos** valitaan työn luontiprosessin aikana:</span><span class="sxs-lookup"><span data-stu-id="2e55d-189">The following fields will be added to the mobile device menu item when **Adjustment in** or **Adjustment out** is selected during the work creation process:</span></span>

- <span data-ttu-id="2e55d-190">Inventoinnin oletussyykoodi</span><span class="sxs-lookup"><span data-stu-id="2e55d-190">Default counting reason code</span></span>
- <span data-ttu-id="2e55d-191">Näytä inventoinnin syykoodi</span><span class="sxs-lookup"><span data-stu-id="2e55d-191">Display counting reason code</span></span>
- <span data-ttu-id="2e55d-192">Muokkaa inventoinnin syykoodia</span><span class="sxs-lookup"><span data-stu-id="2e55d-192">Edit counting reason code</span></span>
