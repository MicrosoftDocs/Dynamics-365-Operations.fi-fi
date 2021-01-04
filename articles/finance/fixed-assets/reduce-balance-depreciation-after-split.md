---
title: Jäännöspoisto jaon jälkeen
description: Tässä ohjeaiheessa kuvataan menetelmä, jota käytetään resurssissa poiston laskemiseen sen jälkeen, kun resurssi on jaettu käyttämällä jäännöspoistomenetelmää.
author: moaamer
manager: Ann Beebe
ms.date: 11/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-11-17
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 615d17c71b904d426081d4c57492ba7e95c2c749
ms.sourcegitcommit: 65f9e2584c0530b1a71655aae09101691726b47f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/01/2020
ms.locfileid: "4650659"
---
# <a name="reduce-balance-depreciation-after-a-split"></a><span data-ttu-id="6d816-103">Jäännöspoisto jaon jälkeen</span><span class="sxs-lookup"><span data-stu-id="6d816-103">Reduce balance depreciation after a split</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6d816-104">Tässä ohjeaiheessa kuvataan menetelmä, jota käytetään resurssissa poiston laskemiseen sen jälkeen, kun resurssi on jaettu toiseen resurssiin käyttämällä jäännöspoistomenetelmää.</span><span class="sxs-lookup"><span data-stu-id="6d816-104">This topic describes the method that is used in Fixed assets to calculate depreciation after an asset is split to another asset by using the reduce balance method.</span></span> <span data-ttu-id="6d816-105">Käyttöomaisuuskirjaan määritetty poistovuosi on tilikausi.</span><span class="sxs-lookup"><span data-stu-id="6d816-105">The depreciation year that is configured in the asset book is the fiscal year.</span></span> <span data-ttu-id="6d816-106">Lisätietoja on kohdassa [Jäännöspoisto](reduce-balance-depreciation.md) ja [Käyttöomaisuuserän jakaminen](tasks/split-fixed-asset.md).</span><span class="sxs-lookup"><span data-stu-id="6d816-106">For more information, see [Reduce balance depreciation](reduce-balance-depreciation.md) and [Split a fixed asset](tasks/split-fixed-asset.md).</span></span>

<span data-ttu-id="6d816-107">Jos jaat resurssin sellaisen tilikauden aikana, joka on myöhempi kuin resurssin hankinnan tilikausi, jäännöspoisto ottaa huomioon resurssin nettokirjanpitoarvon edelliseltä vuodelta.</span><span class="sxs-lookup"><span data-stu-id="6d816-107">If you split a fixed asset during a fiscal period that is later than the period when the asset was acquired, the reduced balance depreciation will account for the asset's net book value (NBV) for the previous year.</span></span> <span data-ttu-id="6d816-108">Se myös ottaa huomioon hankinta- ja poistooikaisutapahtumat, jotka on luotu resurssin jakamasta tapahtumasta.</span><span class="sxs-lookup"><span data-stu-id="6d816-108">It will also account for the acquisition and depreciation adjustment transactions that were generated from the transaction that split the asset.</span></span> <span data-ttu-id="6d816-109">Tämä toiminto olettaa, että resurssi on hankittu yhden tilivuoden aikana ja jaettu seuraavan tilivuoden aikana.</span><span class="sxs-lookup"><span data-stu-id="6d816-109">This behavior assumes that the asset was acquired in one fiscal year and split in a later fiscal year.</span></span> <span data-ttu-id="6d816-110">Summa, joka on poistettava alkuperäisestä resurssista jakamisen jälkeen, vastaa resurssin nettokirjanpitoarvoa ennen resurssin jakamista ja jaolle kirjattua poiston oikaisutapahtumaa.</span><span class="sxs-lookup"><span data-stu-id="6d816-110">The amount that must be depreciated for the original asset after the split reflects the asset's NBV before the asset was split, and the acquisition and depreciation adjustment transaction that was posted for the split.</span></span>

<span data-ttu-id="6d816-111">Esimerkiksi seuraavat ehdot ovat voimassa:</span><span class="sxs-lookup"><span data-stu-id="6d816-111">For example, the following conditions are in effect:</span></span>

- <span data-ttu-id="6d816-112">Tilikausi on 30.6.-1.7.</span><span class="sxs-lookup"><span data-stu-id="6d816-112">The fiscal period is from June 30 to July 1.</span></span>
- <span data-ttu-id="6d816-113">Jäännösarvoprosentti on 18 ja resurssi hankitaan kesäkuussa 2019. Hankintahinta on 10 000 $.</span><span class="sxs-lookup"><span data-stu-id="6d816-113">The reducing balance percentage is 18 percent, and an asset is acquired in June 2019 at an acquisition price of $10,000.</span></span>
- <span data-ttu-id="6d816-114">Ensimmäisen tilivuoden poisto on 18 000 $, kuukausittainen poisto on 150 $ ja resurssi on poistettu marraskuussa 2019, summa 738,75 $.</span><span class="sxs-lookup"><span data-stu-id="6d816-114">The depreciation of the first fiscal year equals $18,000, the monthly depreciation equals $150, and the asset is then depreciated until November 2019, in the amount of $738.75.</span></span>
- <span data-ttu-id="6d816-115">Marraskuussa 2019 80 prosenttia resurssista jaetaan toiselle käyttöomaisuuserälle.</span><span class="sxs-lookup"><span data-stu-id="6d816-115">In November 2019, 80 percent of the asset is split to another fixed asset.</span></span>

<span data-ttu-id="6d816-116">[![Jäännöspoisto jaon jälkeen](./media/reduce-balance-depreciation-after-split.png)](./media/reduce-balance-depreciation-after-split.png)</span><span class="sxs-lookup"><span data-stu-id="6d816-116">[![Reduce balance depreciation after a split](./media/reduce-balance-depreciation-after-split.png)](./media/reduce-balance-depreciation-after-split.png)</span></span>

<span data-ttu-id="6d816-117">Alkuperäisen käyttöomaiosuuserän poistettava summa on 1 822,25 $.</span><span class="sxs-lookup"><span data-stu-id="6d816-117">The amount to depreciate for the original asset is $1,822.25.</span></span> <span data-ttu-id="6d816-118">Tämä summa on sama kuin nettokirjanpitoarvo ennen jakotapahtumaa, kirjattuna (9 111,25 $) lisättynä hankinnan oikaisulla, joka luodaan jakotapahtuman kirjauksen aikana (-8 000 $) lisättynä poiston oikaisulla, joka luodaan jakotapahtuman aikana (711 $).</span><span class="sxs-lookup"><span data-stu-id="6d816-118">This amount equals the NBV before the split transaction is posted ($9,111.25), plus the acquisition adjustment that is generated during posting of the split transaction (-$8,000), plus the depreciation adjustment that is generated during the split transaction ($711).</span></span> <span data-ttu-id="6d816-119">Tämän vuoksi toisen vuoden poisto on (1 822,25 × 18 prosenttia) ÷ 12 = 27,33 $.</span><span class="sxs-lookup"><span data-stu-id="6d816-119">Therefore, the depreciation for the second year is (1,822.25 × 18 percent) ÷ 12 = $27.33.</span></span>

<span data-ttu-id="6d816-120">Uuden käyttöomaisuudenkäyttöomaisuuserän poistosumma ensimmäisenä vuonna on (8 000 × 18 prosenttia) ÷ 12 = 120 $.</span><span class="sxs-lookup"><span data-stu-id="6d816-120">The amount to depreciate for the new fixed asset in the first year is (8,000 × 18 percent) ÷ 12 = $120.</span></span>
