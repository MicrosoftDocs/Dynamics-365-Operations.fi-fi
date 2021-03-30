---
title: Resurssilaskureiden manuaalinen päivitys
description: Tässä ohjeaiheessa kuvataan resurssilaskureiden manuaalista päivitystä resurssien hallinnassa.
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetCounter
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 6dfea7ca166948f507a1cdea20f3e4cce16080ce
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5219482"
---
# <a name="manual-update-of-asset-counters"></a><span data-ttu-id="68f64-103">Resurssilaskureiden manuaalinen päivitys</span><span class="sxs-lookup"><span data-stu-id="68f64-103">Manual update of asset counters</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="68f64-104">Laskureita käytetään resurssin rekisteröintien luomiseen. Nämä rekisteröinnit koskevat esimerkiksi resurssin käytössäolotunteja tai tuotettua määrää.</span><span class="sxs-lookup"><span data-stu-id="68f64-104">Counters are used to create registrations on an asset, such as registrations about the number of hours that the asset has been in operation or the quantity that has been produced.</span></span>

<span data-ttu-id="68f64-105">Laskurille valittu laskurityyppi voidaan määrittää perimään laskuriarvoja.</span><span class="sxs-lookup"><span data-stu-id="68f64-105">The counter type that is selected for a counter might be set to inherit counter values.</span></span> <span data-ttu-id="68f64-106">Toisin sanoen **Peri resurssilaskurin arvot** -asetuksen arvoksi asetetaan **Kyllä** **Laskurit**-sivun **Yleistä**-pikavälilehdessä (**Resurssienhallinta** > **Asetukset** > **Resurssityypit** > **Laskurit**).</span><span class="sxs-lookup"><span data-stu-id="68f64-106">In other words, the **Inherit asset counter values** option is set to **Yes** on the **General** FastTab of the **Counters** page (**Asset management** > **Setup** > **Asset types** > **Counters**).</span></span> <span data-ttu-id="68f64-107">Kun tässä tapauksessa luot kyseistä tyyppiä edustavan laskuririvin, jokainen samaa laskurityyppiä käyttävä alilaskuri päivitetään automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="68f64-107">In this case, when you create a new counter line of that type, every child asset that uses the same counter type is automatically updated.</span></span>

<span data-ttu-id="68f64-108">**Kaikki resurssit** -sivulla voit luoda resurssille tuntien tai määrien laskurimerkintöjä resurssin lukemien perusteella.</span><span class="sxs-lookup"><span data-stu-id="68f64-108">On the **All assets** page, you create hours or quantity counter registrations on an asset, based on your readings on the asset.</span></span>

1. <span data-ttu-id="68f64-109">Valitse **Resurssienhallinta** > **Yhteiset** > **Resurssit** > **Kaikki resurssit**.</span><span class="sxs-lookup"><span data-stu-id="68f64-109">Select **Asset management** > **Common** > **Assets** > **All assets**.</span></span>

2. <span data-ttu-id="68f64-110">Valitse resurssi ja sitten toimintoruudun **Resurssi**-välilehden **Ennaltaehkäisevä**-ryhmässä **Laskurit**.</span><span class="sxs-lookup"><span data-stu-id="68f64-110">Select the asset, and then, on the Action Pane, on the **Asset** tab, in the **Preventive** group, select **Counters**.</span></span> <span data-ttu-id="68f64-111">**Resurssilaskurit**-sivulla näkyy luettelo valitun resurssin kaikista aiemmista laskurirekisteröinneistä.</span><span class="sxs-lookup"><span data-stu-id="68f64-111">The **Asset counters** page shows a list of all previous counter registrations that have been made on the selected asset.</span></span>

3. <span data-ttu-id="68f64-112">Luo uusi rekisteröinti valitsemalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="68f64-112">Select **New** to create a registration.</span></span> <span data-ttu-id="68f64-113">Resurssitunnus syötetään automaattisesti **Resurssi**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="68f64-113">The asset ID is automatically entered in the **Asset** field.</span></span>

4. <span data-ttu-id="68f64-114">Valitse **Laskuri**-kentästä haluamasi laskuri.</span><span class="sxs-lookup"><span data-stu-id="68f64-114">In the **Counter** field, select the relevant counter.</span></span> <span data-ttu-id="68f64-115">Vain resurssille valittuun resurssityyppiin liittyvät laskurit ovat vallittavissa.</span><span class="sxs-lookup"><span data-stu-id="68f64-115">Only counters that are related to the asset type selected on the asset are available for selection.</span></span> <span data-ttu-id="68f64-116">Liittyvä yksikkö syötetään automaattisesti **Yksikkö**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="68f64-116">The related unit is automatically entered in the **Unit** field.</span></span>

5. <span data-ttu-id="68f64-117">Valitse **Rekisteröity**-kentässä laskurirekisteröinnin päivämäärä ja aika.</span><span class="sxs-lookup"><span data-stu-id="68f64-117">In the **Registered** field, select the date and time for the counter registration.</span></span>

6. <span data-ttu-id="68f64-118">Syötä **Arvo**-kenttään edellisestä laskurirekisteröinnistä kulunut numero.</span><span class="sxs-lookup"><span data-stu-id="68f64-118">In the **Value** field, enter the number since the last counter registration.</span></span> <span data-ttu-id="68f64-119">Vaihtoehtoisesti voit syöttää laskurin kokonaisnumeron **Koostettu arvo** -kenttään.</span><span class="sxs-lookup"><span data-stu-id="68f64-119">Alternatively, in the **Aggregated value** field, enter the total count number.</span></span>

<span data-ttu-id="68f64-120">Huomaa seuraavat seikat:</span><span class="sxs-lookup"><span data-stu-id="68f64-120">Note the following points:</span></span>

- <span data-ttu-id="68f64-121">Jos asennat käyttöomaisuuserään uuden laskurin fyysisesti, sinun täytyy rekisteröidä käyttöomaisuuserän muutos **Resurssilaskurit**-sivulle.</span><span class="sxs-lookup"><span data-stu-id="68f64-121">If you physically install a new counter on an asset, you must register the change on the asset on the **Asset counters** page.</span></span> <span data-ttu-id="68f64-122">Seuraavaksi sinun on luotava kaksi rekisteröintiriviä, joilla on identtiset aikaleimat.</span><span class="sxs-lookup"><span data-stu-id="68f64-122">Next, you must create two registration lines that have identical timestamps.</span></span> <span data-ttu-id="68f64-123">Ensimmäisen rivin on oltava korvattavaa laskuria vartenn.</span><span class="sxs-lookup"><span data-stu-id="68f64-123">The first line must be for the counter that you're replacing.</span></span> <span data-ttu-id="68f64-124">Valitse uuteen laskuriin liittyvällä rivillä **Laskurin nollaus** -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="68f64-124">On the line that is related to the new counter, select the **Counter reset** check box.</span></span> <span data-ttu-id="68f64-125">**Summa**-kentässä laskurin kokonaissumma on kyseisen laskurityypin kaikkien kirjattujen arvojen laskurin summa.</span><span class="sxs-lookup"><span data-stu-id="68f64-125">In the **Totals** field, the total count number is the sum of the counter totals of all registered values on that counter type.</span></span>

- <span data-ttu-id="68f64-126">Jos resurssin **Laskurin nollaus** -valintaruutu on valittuna resurssille käyttämällä ylläpitosuunnitelmaa, jonka välityyppi on"Kerran alkaen..." tai "Kerran jälkeen...", laskuri on edelleen aktiivinen uudella laskuririvillä, koska luot erillisen laskuririvin ja aloitat alusta uuden laskurin avulla.</span><span class="sxs-lookup"><span data-stu-id="68f64-126">If the **Counter reset** check box is selected on an asset using a maintenance plan that has a "Once from..." or "Once reached..." interval type, the counter is still active on the new counter line, because you create a separate counter line and start over with a new counter.</span></span>

<span data-ttu-id="68f64-127">Seuraavassa kuvassa on esimerkki **Resurssilaskurit**-sivusta.</span><span class="sxs-lookup"><span data-stu-id="68f64-127">The illustration below shows an example of the **Asset counters** page.</span></span>

![Kuva 1](media/11-work-orders.png)

<span data-ttu-id="68f64-129">**Resurssilaskurit**-sivulla (**Resurssienhallinta** > **Kyselyt** > **Resurssit** > **Resurssilaskurit**), voit tarpeen mukaan suorittaa laskurirekisteröintejä useille resursseille samanaikaisesti</span><span class="sxs-lookup"><span data-stu-id="68f64-129">On the **Asset counters** page (**Asset management** > **Inquiries** > **Assets** > **Asset counters**), you can make counter registrations on several assets at the same time, as you require.</span></span>

>[!NOTE]
><span data-ttu-id="68f64-130">Voit määrittää välin määrittämään poikkeuksia manuaalisissa laskurirekisteröinneissä.</span><span class="sxs-lookup"><span data-stu-id="68f64-130">You can set up a range to define deviations in manual counter registrations.</span></span> <span data-ttu-id="68f64-131">Voit myös määrittää, minkälainen sanoma tulee näkyviin, jos rekisteröinnit poikkeavat määritetystä välistä.</span><span class="sxs-lookup"><span data-stu-id="68f64-131">You can also specify the type of message that is shown if registrations are outside the defined range.</span></span> <span data-ttu-id="68f64-132">Lisätietoja laskureiden määrittämisestä esitetään kohdassa [Laskurit](../setup-for-objects/counters.md).</span><span class="sxs-lookup"><span data-stu-id="68f64-132">For more information about how to set up counters, see [Counters](../setup-for-objects/counters.md).</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]