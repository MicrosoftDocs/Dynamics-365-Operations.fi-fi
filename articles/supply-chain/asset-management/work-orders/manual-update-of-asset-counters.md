---
title: Resurssilaskureiden manuaalinen päivitys
description: Tässä ohjeaiheessa kuvataan resurssilaskureiden manuaalista päivitystä resurssien hallinnassa.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 1e7c5ec288404c18b00f9dcd0e66f50744d0aa2f
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875632"
---
# <a name="manual-update-of-asset-counters"></a><span data-ttu-id="01369-103">Resurssilaskureiden manuaalinen päivitys</span><span class="sxs-lookup"><span data-stu-id="01369-103">Manual update of asset counters</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


<span data-ttu-id="01369-104">Laskurien avulla luodaan käyttöomaisuuserän rekisteröinnit, jotka koskevat esimerkiksi käytössä olevien tuntien määrää tai tuotettuja määriä.</span><span class="sxs-lookup"><span data-stu-id="01369-104">Counters are used to create registrations on an asset regarding, for example, number of hours in operation, or the number of quantities produced.</span></span>

<span data-ttu-id="01369-105">Jos laskurille valittu laskurityyppi on asetettu perimään laskuriarvot (**Resurssien hallinta** > **Asetukset** > **Resurssityypit** > **Laskurit** > **Yleiset**-pikavälilehti > **Peri resurssilaskurin arvot** -vaihtopainikkeen arvoksi "Kyllä"), ja kun luot uuden tämän tyypin laskuririvin, samaa laskurityyppiä käyttävät kaikki alemman tason resurssit päivitetään automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="01369-105">If the counter type selected for a counter is set to inherit counter values (**Asset management** > **Setup** > **Asset types** > **Counters** > **General** FastTab > **Inherit asset counter values** toggle button set to "Yes"), then, when you create a new counter line of that type, every child asset that uses the same counter type is automatically updated.</span></span>

<span data-ttu-id="01369-106">**Kaikki resurssit** -kohdassa voit luoda käyttöomaisuuserälle tuntien tai määrien laskurimerkintöjä käyttöomaisuuserän lukemien perusteella.</span><span class="sxs-lookup"><span data-stu-id="01369-106">In **All assets**, you create hours or quantity counter registrations on an asset, based on your readings on the asset.</span></span>

1. <span data-ttu-id="01369-107">Valitse **Resurssien hallinta**  >  **Yhteiset**  >  **Resurssit**  >  **Kaikki resurssit**.</span><span class="sxs-lookup"><span data-stu-id="01369-107">Click **Asset management** > **Common** > **Assets** > **All assets**.</span></span>

2. <span data-ttu-id="01369-108">Valitse käyttöomaisuus luettelosta ja valitse sitten **Laskurit**.</span><span class="sxs-lookup"><span data-stu-id="01369-108">Select the asset in the list, and click **Counters**.</span></span> <span data-ttu-id="01369-109">**Resurssilaskurit**-lomakkeessa näkyy luettelo valitun käyttöomaisuuserän kaikista aiemmista laskurirekisteröinneistä.</span><span class="sxs-lookup"><span data-stu-id="01369-109">In the **Asset counters** form, you see a list of all previous counter registrations on the selected asset.</span></span>

3. <span data-ttu-id="01369-110">Luo uusi rekisteröinti valitsemalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="01369-110">Click **New** to create a new registration.</span></span> <span data-ttu-id="01369-111">Resurssitunnus lisätään automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="01369-111">The asset ID is automatically inserted.</span></span>

4. <span data-ttu-id="01369-112">Valitse **Laskuri**-kentästä haluamasi laskuri.</span><span class="sxs-lookup"><span data-stu-id="01369-112">In the **Counter** field, select the relevant counter.</span></span> <span data-ttu-id="01369-113">Vain käyttöomaisuuserälle valittuun käyttöomaisuuslajiin liittyvät laskurit ovat käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="01369-113">Only counters related to the asset type selected on the asset are available.</span></span> <span data-ttu-id="01369-114">Liittyvä yksikkö lisätään automaattisesti **Yksikkö**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="01369-114">The related unit is automatically inserted in the **Unit** field.</span></span>

5. <span data-ttu-id="01369-115">Valitse laskurin rekisteröinnille päivämäärä ja aika.</span><span class="sxs-lookup"><span data-stu-id="01369-115">Select date and time for the counter registration.</span></span>

6. <span data-ttu-id="01369-116">Lisää **Arvo**-kenttään numero edellisen laskurikirjauksen jälkeen tai lisää laskurin summaluku **Koostettu arvo** -kenttään.</span><span class="sxs-lookup"><span data-stu-id="01369-116">In the **Value** field, insert the number since the last counter registration, or, in the **Aggregated value** field, insert the total count number.</span></span>

- <span data-ttu-id="01369-117">Jos asennat käyttöomaisuuserään uuden laskurin fyysisesti, sinun täytyy rekisteröidä käyttöomaisuuserän muutos **Resurssilaskurit**-kohdassa.</span><span class="sxs-lookup"><span data-stu-id="01369-117">If you physically install a new counter on an asset, you need to register the change on the asset in **Asset counters**.</span></span> <span data-ttu-id="01369-118">Seuraavaksi sinun on luotava kaksi kirjausriviä, joilla on samat aikaleimat, ja uuden laskurin rivillä on valittava **Laskurin nollaus** -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="01369-118">Next, you must create two registration lines with identical timestamps, and on the line regarding the new counter, you select the **Counter reset** check box.</span></span> <span data-ttu-id="01369-119">Kun luot kaksi kirjausriviä, ensimmäisen rivin on oltava korvattavien laskurien kohdalla.</span><span class="sxs-lookup"><span data-stu-id="01369-119">When you create the two registration lines, the first line must be for the counter that you are replacing.</span></span> <span data-ttu-id="01369-120">**Summa-** kentässä laskurin kokonaissumma on kyseisen laskurityypin kaikkien kirjattujen arvojen laskurin summa.</span><span class="sxs-lookup"><span data-stu-id="01369-120">In the **Totals** field, the total count number is the sum of the counter total of all registered values on that counter type.</span></span>  
- <span data-ttu-id="01369-121">Jos resurssin **Laskurin nollaus** -valintaruutu on valittuna käyttöomaisuuserälle käyttämällä huoltosuunnitelmaa, jonka vältyyppi on"Kerran alkaen..." tai "Kerran jälkeen...", laskuri on edelleen aktiivinen uudella laskuririvillä, koska luot erillisen laskuririvin ja aloitat alusta uuden laskurin avulla.</span><span class="sxs-lookup"><span data-stu-id="01369-121">If the **Counter reset** check box is selected on an asset using a maintenance plan with a "Once from..." or "Once reached..." interval type, the counter is still active on the new counter line because you create a separate counter line and start over with a new counter.</span></span>

![Kuva 1](media/11-work-orders.png)


<span data-ttu-id="01369-123">Jos haluat tehdä laskurikirjauksia useille käyttöomaisuuserille, se voidaan tehdä kohdaas **Resurssien hallinta** > **Kyselyt** > **Resurssit** > **Resurssilaskurit.**</span><span class="sxs-lookup"><span data-stu-id="01369-123">If you need to make counter registrations on several assets, that can be done in **Asset management** > **Inquiries** > **Assets** > **Asset counters**.</span></span>

>[!NOTE]
><span data-ttu-id="01369-124">Voit määrittää alueen, joka määrittää manuaalisten laskurirekisteröintien poikkeamat, sekä sanoman tyypin, joka tulee näkyviin, jos rekisteröinnit ovat määritetyn alueen ulkopuolella.</span><span class="sxs-lookup"><span data-stu-id="01369-124">You can set up a range to define deviations in manual counter registrations, and the type of message that should be displayed if registrations are outside the defined range.</span></span> <span data-ttu-id="01369-125">Lisätietoja laskurien määrittämisestä on kohdassa [Laskurit](../setup-for-objects/counters.md).</span><span class="sxs-lookup"><span data-stu-id="01369-125">Refer to the [Counters](../setup-for-objects/counters.md) topic regarding setup of counters.</span></span>
