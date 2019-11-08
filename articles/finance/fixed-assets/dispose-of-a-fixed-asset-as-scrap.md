---
title: Hävikiksi merkityn käyttöomaisuuden poistaminen
description: Tässä ohjeaiheessa käsitellään hävikkinä poistetun käyttöomaisuuden tapahtumien eliminointiprosessia.
author: moaamer
manager: Ann Beebe
ms.date: 08/14/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2019-08-14
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: 42eaa3df5ab09278ed96506d17e1b42d4fc2a9e1
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/10/2019
ms.locfileid: "2570261"
---
# <a name="dispose-of-a-fixed-asset-as-scrap"></a><span data-ttu-id="cd5d1-103">Hävikiksi merkityn käyttöomaisuuden poistaminen</span><span class="sxs-lookup"><span data-stu-id="cd5d1-103">Dispose of a fixed asset as scrap</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cd5d1-104">Tässä ohjeaiheessa käsitellään hävikkinä poistetun käyttöomaisuuden tapahtumien eliminointiprosessia.</span><span class="sxs-lookup"><span data-stu-id="cd5d1-104">The topic describes the process of eliminating transactions for a fixed asset that was disposed of as scrap.</span></span> <span data-ttu-id="cd5d1-105">Eliminoitavia tapahtumatyyppejä ovat esimerkiksi käyttöomaisuuden hankinta sekä kumuloituneet poistotapahtumat ja muut käyttöomaisuustapahtumat.</span><span class="sxs-lookup"><span data-stu-id="cd5d1-105">The transaction types that can be eliminated include an asset's acquisition and accumulated depreciation transactions and other fixed asset transactions.</span></span> <span data-ttu-id="cd5d1-106">Näiden tapahtumien eliminointi vaikuttaa tasetileihin, kuten hankintaoikaisu-, poisto-oikaisu-, uudelleenarvostus-, kirjanpitoarvon korotus- ja kirjanpitoarvon alentamistilit.</span><span class="sxs-lookup"><span data-stu-id="cd5d1-106">Elimination of these transactions affects balance sheet accounts, such as acquisition adjustment, depreciation adjustment, revaluation, write-up, and write-down accounts.</span></span>

| <span data-ttu-id="cd5d1-107">Tapahtuma</span><span class="sxs-lookup"><span data-stu-id="cd5d1-107">Transaction</span></span>                                         | <span data-ttu-id="cd5d1-108">Debet (Dr.)</span><span class="sxs-lookup"><span data-stu-id="cd5d1-108">Debit (Dr.)</span></span> | <span data-ttu-id="cd5d1-109">Kredit (Cr.)</span><span class="sxs-lookup"><span data-stu-id="cd5d1-109">Credit (Cr.)</span></span> |
|-----------------------------------------------------|-------------|--------------|
| <span data-ttu-id="cd5d1-110">Dr. kertynyt poisto</span><span class="sxs-lookup"><span data-stu-id="cd5d1-110">Dr. Accumulated depreciation</span></span>                        | <span data-ttu-id="cd5d1-111">X</span><span class="sxs-lookup"><span data-stu-id="cd5d1-111">X</span></span>           |              |
| <span data-ttu-id="cd5d1-112">Cr. käyttöomaisuuden voitto/tappio</span><span class="sxs-lookup"><span data-stu-id="cd5d1-112">Cr. Fixed assets gain/loss</span></span>                          |             | <span data-ttu-id="cd5d1-113">X</span><span class="sxs-lookup"><span data-stu-id="cd5d1-113">X</span></span>            |
| <span data-ttu-id="cd5d1-114">Dr. käyttöomaisuuden voitto/tappio</span><span class="sxs-lookup"><span data-stu-id="cd5d1-114">Dr. Fixed assets gain/loss</span></span>                          | <span data-ttu-id="cd5d1-115">X</span><span class="sxs-lookup"><span data-stu-id="cd5d1-115">X</span></span>           |              |
| <span data-ttu-id="cd5d1-116">Cr. käyttöomaisuuserän hankintatili</span><span class="sxs-lookup"><span data-stu-id="cd5d1-116">Cr. Fixed asset acquisition account</span></span>                 |             | <span data-ttu-id="cd5d1-117">X</span><span class="sxs-lookup"><span data-stu-id="cd5d1-117">X</span></span>            |
| <span data-ttu-id="cd5d1-118">Dr. käyttöomaisuuden voitto/tappio (nettokirjanpitoarvo \[NKPA\])</span><span class="sxs-lookup"><span data-stu-id="cd5d1-118">Dr. Fixed assets gain/loss (net book value \[NBV\])</span></span> | <span data-ttu-id="cd5d1-119">X</span><span class="sxs-lookup"><span data-stu-id="cd5d1-119">X</span></span>           |              |
| <span data-ttu-id="cd5d1-120">Cr. käyttöomaisuuden voitto/tappio (NKPA)</span><span class="sxs-lookup"><span data-stu-id="cd5d1-120">Cr. Fixed assets gain/loss (NBV)</span></span>                    |             | <span data-ttu-id="cd5d1-121">X</span><span class="sxs-lookup"><span data-stu-id="cd5d1-121">X</span></span>            |

> [!NOTE]
> <span data-ttu-id="cd5d1-122">Yrityksen talousjohtajan tai controllerin kannattaa tehdä tiivistä yhteistyötä, jotta kullekin tapahtumatyypille tunnistetaan oikeat käytettävät tilit ja jotta voidaan varmistaa, että poistoprosessi ja sen luomat tapahtumat päivittävät kyseiset tilit oikein.</span><span class="sxs-lookup"><span data-stu-id="cd5d1-122">We recommend that you work closely with your company's chief financial officer (CFO) or controller to identify the correct accounts that should be used for each transaction type, and also to verify that the disposal process and the transactions that it generates update those accounts correctly.</span></span>

<span data-ttu-id="cd5d1-123">Ennen kuin käyttöomaisuus voidaan poistaa hävikkinä, on luotava kirjanpitotilit, jotka on liitetty käyttöoikeuden hankinta-arvoon, kuluvan vuoden poistoon, edellisten vuosien poistoon ja käyttöomaisuuden NKPA:han.</span><span class="sxs-lookup"><span data-stu-id="cd5d1-123">Before you dispose of a fixed asset as scrap, you must create ledger accounts that are associated with the asset's acquisition value, depreciation for the current year, depreciation for previous years, and the asset's NBV.</span></span> <span data-ttu-id="cd5d1-124">Käyttöomaisuuden tapahtumatyyppien luettelo on **Käyttöomaisuuden kirjausprofiilit** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="cd5d1-124">The fixed asset transaction types are listed on the **Fixed assets posting profile** page.</span></span> <span data-ttu-id="cd5d1-125">Valitse ensin **Käyttöomaisuuserät \> Asetukset \> Käyttöomaisuuserän kirjausprofiili** ja valitse sitten **Luovutus**-pikavälilehdessä **Hävikki** ruudulla yläpuolella olevassa kentässä.</span><span class="sxs-lookup"><span data-stu-id="cd5d1-125">Go to **Fixed assets \> Setup \> Fixed asset posting profiles**, and then, on the **Disposal** FastTab, select **Scrap** in the field above the grid.</span></span> <span data-ttu-id="cd5d1-126">Seuraavassa kuvassa on luettelo **Käyttöomaisuuserän kirjausprofiili** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="cd5d1-126">The following illustration shows the list of fixed asset transaction types on the **Fixed asset posting profiles** page.</span></span>


<span data-ttu-id="cd5d1-127">[![Käyttöomaisuuden poistaminen hävikkinä, kuva 1](./media/Fixed_asset_Disposal_scrap_scenario_1.png)](./media/Fixed_asset_Disposal_scrap_scenario_1.png)</span><span class="sxs-lookup"><span data-stu-id="cd5d1-127">[![Disposing of an asset as scap, Fig. 1](./media/Fixed_asset_Disposal_scrap_scenario_1.png)](./media/Fixed_asset_Disposal_scrap_scenario_1.png)</span></span>

<span data-ttu-id="cd5d1-128">Seuraavassa esimerkissä käyttöomaisuus hankittiin 1.1.2018 ja se hävitetään 31.3.2019.</span><span class="sxs-lookup"><span data-stu-id="cd5d1-128">For the following example, a fixed asset was acquired on January 1, 2018, and it will be scrapped on March 31, 2019.</span></span>

- <span data-ttu-id="cd5d1-129">**Hankintahinta:** 24 000,00 Yhdysvaltain dollaria (USD)</span><span class="sxs-lookup"><span data-stu-id="cd5d1-129">**Acquisition price:** 24,000.00 US dollars (USD)</span></span>
- <span data-ttu-id="cd5d1-130">**Käyttöikä:** kaksi vuotta</span><span class="sxs-lookup"><span data-stu-id="cd5d1-130">**Service life:** Two years</span></span>
- <span data-ttu-id="cd5d1-131">**Poistomenetelmä:** Tasapoisto - käyttöaika</span><span class="sxs-lookup"><span data-stu-id="cd5d1-131">**Depreciation method:** Straight line service life</span></span>
- <span data-ttu-id="cd5d1-132">**Poistosumma:** 1 000,00 USD kuukaudessa</span><span class="sxs-lookup"><span data-stu-id="cd5d1-132">**Depreciation amount:** 1,000.00 USD per month</span></span>

<span data-ttu-id="cd5d1-133">Käyttöomaisuuden NKPA lasketaan seuraavan kaavan avulla:</span><span class="sxs-lookup"><span data-stu-id="cd5d1-133">The NBV of a fixed asset is calculated by using the following formula:</span></span>

<span data-ttu-id="cd5d1-134">Nettokirjanpitoarvo = hankintahinta – poisto</span><span class="sxs-lookup"><span data-stu-id="cd5d1-134">Net book value = Acquisition price – Depreciation</span></span>

<span data-ttu-id="cd5d1-135">Tässä esimerkissä käyttöomaisuus hankittiin ja siinä tehtiin poistoja 15 kuukautta tammikuusta 2018 maaliskuuhun 2019.</span><span class="sxs-lookup"><span data-stu-id="cd5d1-135">In this example, the fixed asset was acquired and was depreciated for 15 months, from January 2018 through March 2019.</span></span> <span data-ttu-id="cd5d1-136">Tämän vuoksi käyttöomaisuuserän NKPA on 9 000,00 USD (24 000,00 USD – 15 000,00 USD).</span><span class="sxs-lookup"><span data-stu-id="cd5d1-136">Therefore, the asset's NBV is 9,000.00 USD (24,000.00 USD – 15,000.00 USD).</span></span>

<span data-ttu-id="cd5d1-137">[![Käyttöomaisuuden poistoesimerkki](./media/Fixed_asset_Disposal_scrap_scenario_2.png)](./media/Fixed_asset_Disposal_scrap_scenario_2.png)</span><span class="sxs-lookup"><span data-stu-id="cd5d1-137">[![Fixed asset depreciation example](./media/Fixed_asset_Disposal_scrap_scenario_2.png)](./media/Fixed_asset_Disposal_scrap_scenario_2.png)</span></span>


<span data-ttu-id="cd5d1-138">Luo poistokirjanpito valitsemalla ensin **Käyttöomaisuuserät \> Kirjauskansioviennit \> Käyttöomaisuuden kirjauskansio** ja valitse sitten toimintoruudussa **Rivit**.</span><span class="sxs-lookup"><span data-stu-id="cd5d1-138">To create a disposal journal, go to **Fixed assets \> Journal entries \> Fixed assets journal**, and then, on the Action Pane, select **Lines**.</span></span> <span data-ttu-id="cd5d1-139">Valitse ensin **Poistohävikki** ja valitse sitten käyttöomaisuuserän tunnus.</span><span class="sxs-lookup"><span data-stu-id="cd5d1-139">Select **Disposal – scrap**, and then select a fixed asset ID.</span></span> <span data-ttu-id="cd5d1-140">Jotta käyttöomaisuus voitaisiin poistaa kokonaan, älä anna arvoa **Debet**- eikä **Kredit**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="cd5d1-140">To fully dispose of the asset, don't enter a value in either the **Debit** field or the **Credit** field.</span></span>

<span data-ttu-id="cd5d1-141">[![Käyttöomaisuuden kirjauskansio](./media/Fixed_asset_Disposal_scrap_scenario_3.png)](./media/Fixed_asset_Disposal_scrap_scenario_3.png)</span><span class="sxs-lookup"><span data-stu-id="cd5d1-141">[![Fixed assets journal](./media/Fixed_asset_Disposal_scrap_scenario_3.png)](./media/Fixed_asset_Disposal_scrap_scenario_3.png)</span></span>

<span data-ttu-id="cd5d1-142">Käyttöomaisuuden poistohävikkitapahtuma muuttaa käyttöomaisuuskirjan kentän arvoja seuraavin tavoin:</span><span class="sxs-lookup"><span data-stu-id="cd5d1-142">The fixed asset disposal scrap transaction changes the field values for the fixed asset book in the following ways:</span></span>

- <span data-ttu-id="cd5d1-143">**Saldo**-osan **Tila**-kenttään on päivitetty **Romutettu**.</span><span class="sxs-lookup"><span data-stu-id="cd5d1-143">In the **Balance** section, the **Status** field is updated to **Scrapped**.</span></span>
- <span data-ttu-id="cd5d1-144">**Otto**-osan **Myyntipäivä**-kentän arvoksi määritetään päivämäärä, jolloin käyttöomaisuus hävitettiin.</span><span class="sxs-lookup"><span data-stu-id="cd5d1-144">In the **Issue** section, the **Disposal date** field is set to the date when the asset was scrapped.</span></span>

<span data-ttu-id="cd5d1-145">[![Käyttöomaisuuden kirjauskansion tiedot](./media/Fixed_asset_Disposal_scrap_scenario_4.png)](./media/Fixed_asset_Disposal_scrap_scenario_4.png)</span><span class="sxs-lookup"><span data-stu-id="cd5d1-145">[![Fixed assets journal detail](./media/Fixed_asset_Disposal_scrap_scenario_4.png)](./media/Fixed_asset_Disposal_scrap_scenario_4.png)</span></span>

<span data-ttu-id="cd5d1-146">Seuraavassa kuvassa on käyttöomaisuussaldo.</span><span class="sxs-lookup"><span data-stu-id="cd5d1-146">The following illustration shows the fixed asset balance.</span></span>

<span data-ttu-id="cd5d1-147">[![Käyttöomaisuussaldo](./media/Fixed_asset_Disposal_scrap_scenario_5.png)](./media/Fixed_asset_Disposal_scrap_scenario_5.png)</span><span class="sxs-lookup"><span data-stu-id="cd5d1-147">[![Fixed asset balance](./media/Fixed_asset_Disposal_scrap_scenario_5.png)](./media/Fixed_asset_Disposal_scrap_scenario_5.png)</span></span>

<span data-ttu-id="cd5d1-148">Seuraavassa kuvassa on kirjattu tosite.</span><span class="sxs-lookup"><span data-stu-id="cd5d1-148">The following illustration shows the voucher that is posted.</span></span>

<span data-ttu-id="cd5d1-149">[![Nettokirjanpitoarvo](./media/Fixed_asset_Disposal_scrap_scenario_6.png)](./media/Fixed_asset_Disposal_scrap_scenario_6.png)</span><span class="sxs-lookup"><span data-stu-id="cd5d1-149">[![Net book value](./media/Fixed_asset_Disposal_scrap_scenario_6.png)](./media/Fixed_asset_Disposal_scrap_scenario_6.png)</span></span>
