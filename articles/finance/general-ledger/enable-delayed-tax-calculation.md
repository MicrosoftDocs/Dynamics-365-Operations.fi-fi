---
title: Viivästyneen veron laskemisen ottaminen käyttöön kirjauskansioissa
description: Tässä aiheessa selitetään, miten Viivästyneen veron laskeminen -toiminto otetaan käyttöön auttamaan verolaskelmien suorittamista, kun kirjauskansion rivejä on erittäin paljon.
author: ericwang
manager: Ann Beebe
ms.date: 09/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2019-09-18
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: ed8e5f930bbb6b0fb570ba1eb23c0816210c1814
ms.sourcegitcommit: bfd6142569196a060e3f37893c78f00c40a2a18c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/09/2020
ms.locfileid: "2946163"
---
# <a name="enable-delayed-tax-calculation-on-journals"></a><span data-ttu-id="d24dd-103">Viivästyneen veron laskemisen ottaminen käyttöön kirjauskansioissa</span><span class="sxs-lookup"><span data-stu-id="d24dd-103">Enable delayed tax calculation on journals</span></span>
[!include [banner](../includes/banner.md)]


<span data-ttu-id="d24dd-104">Tässä aiheessa selitetään, miten voit viivästyttää arvonlisäveron laskemista kirjauskansioissa.</span><span class="sxs-lookup"><span data-stu-id="d24dd-104">This topic explains how you can delay sales tax calculation on journals.</span></span> <span data-ttu-id="d24dd-105">Tämä ominaisuus auttaa parantamaan verolaskelmien suorittamista, kun kirjauskansion rivejä on paljon.</span><span class="sxs-lookup"><span data-stu-id="d24dd-105">This capability helps improve the performance of tax calculations when there are many journal lines.</span></span>

<span data-ttu-id="d24dd-106">Oletusarvoisesti kirjauskansion rivien arvonlisäverosummat lasketaan aina, kun veroihin liittyviä kenttiä päivitetään.</span><span class="sxs-lookup"><span data-stu-id="d24dd-106">By default, sales tax amounts on journal lines are calculated whenever tax-related fields are updated.</span></span> <span data-ttu-id="d24dd-107">Näitä kenttiä ovat arvonlisäveroryhmien ja nimikkeiden arvonlisäryhmien kentät.</span><span class="sxs-lookup"><span data-stu-id="d24dd-107">These fields include the fields for sales tax groups and item sales tax groups.</span></span> <span data-ttu-id="d24dd-108">Kaikki kirjauskansiorivien päivitykset aiheuttavat verosummien uudelleenlaskennan kaikkien kirjauskansiorivien osalta.</span><span class="sxs-lookup"><span data-stu-id="d24dd-108">Any update to a journal line causes tax amounts to be recalculated for all journal lines.</span></span> <span data-ttu-id="d24dd-109">Vaikka tämä toimintatapa auttaa käyttäjiä näkemään reaaliaikaisesti laskettuja verosummia, se voi myös heikentää suorituskykyä, jos kirjauskansiorivejä on erittäin paljon.</span><span class="sxs-lookup"><span data-stu-id="d24dd-109">Although this behavior helps user see tax amounts calculated in real time, it can also affect performance if the number of journal lines is very large.</span></span>

<span data-ttu-id="d24dd-110">Viivästynyt veron laskenta -toiminnon avulla voit lykätä verojen laskemista kirjauskansioista, minkä vuoksi se auttaa suorituskykyongelmien ratkaisemisessa.</span><span class="sxs-lookup"><span data-stu-id="d24dd-110">The Delayed tax calculation feature lets you delay tax calculation on journals and therefore helps fix performance issues.</span></span> <span data-ttu-id="d24dd-111">Kun tämä toiminto on käytössä, verosummia lasketaan vain, kun käyttäjä tekee valinnan **Arvonlisävero** tai tekee kirjauksen kirjauskansioon.</span><span class="sxs-lookup"><span data-stu-id="d24dd-111">When this feature is turned on, tax amounts are calculated only when a user selects **Sales Tax** or posts the journal.</span></span>

<span data-ttu-id="d24dd-112">Voit viivästyttää arvonlisäverojen laskentaa kolmella tasolla:</span><span class="sxs-lookup"><span data-stu-id="d24dd-112">You can delay the calculation of sales taxes at three levels:</span></span>

- <span data-ttu-id="d24dd-113">Oikeushenkilö</span><span class="sxs-lookup"><span data-stu-id="d24dd-113">Legal entity</span></span>
- <span data-ttu-id="d24dd-114">Kirjauskansion nimi</span><span class="sxs-lookup"><span data-stu-id="d24dd-114">Journal name</span></span>
- <span data-ttu-id="d24dd-115">Kirjauskansion otsikko</span><span class="sxs-lookup"><span data-stu-id="d24dd-115">Journal header</span></span>

<span data-ttu-id="d24dd-116">Järjestelmä kohtelee kirjauskansion otsikon asetusta ensisijaisena.</span><span class="sxs-lookup"><span data-stu-id="d24dd-116">The system gives priority to the setting for the journal header.</span></span> <span data-ttu-id="d24dd-117">Oletusarvoisesti tämä asetus perustuu kirjauskansion nimeen.</span><span class="sxs-lookup"><span data-stu-id="d24dd-117">By default, this setting is taken from the journal name.</span></span> <span data-ttu-id="d24dd-118">Oletusarvoisesti kirjauskansion nimen asetus perustuu **Kirjanpitoparametrit**-sivun asetukseen, kun kirjauskansion nimi luodaan.</span><span class="sxs-lookup"><span data-stu-id="d24dd-118">By default, the setting for the journal name is taken from the setting on the **General ledger parameters** page when the journal name is created.</span></span> <span data-ttu-id="d24dd-119">Seuraavissa osissa selitetään, miten viivästetty verojen laskeminen otetaan käyttöön yritysten, kirjauskansioiden nimien ja kirjauskansioiden otsikkojen osalta.</span><span class="sxs-lookup"><span data-stu-id="d24dd-119">The following sections explain how to turn on delayed tax calculation for legal entities, journal names, and journal headers.</span></span>

## <a name="turn-on-delayed-tax-calculation-at-the-legal-entity-level"></a><span data-ttu-id="d24dd-120">Viivästyneen verojen laskemisen käyttöönotto yritystasolla</span><span class="sxs-lookup"><span data-stu-id="d24dd-120">Turn on delayed tax calculation at the legal entity level</span></span>

1. <span data-ttu-id="d24dd-121">Siirry kohtaan **Kirjanpito \> Kirjanpidon asetukset \> Kirjanpitoparametrit**.</span><span class="sxs-lookup"><span data-stu-id="d24dd-121">Go to **General ledger \> Ledger setup \> General ledger parameters**.</span></span>
2. <span data-ttu-id="d24dd-122">Aseta **Arvonlisävero**-välilehden **Yleinen**-pikavälilehden **Viivästynyt veron laskenta** -asetuken arvoksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="d24dd-122">On the **Sales tax** tab, on the **General** FastTab, set the **Delayed tax calculation** option to **Yes**.</span></span>

![Kirjanpitoparametrien kuva](media/delayed-tax-calculation-gl.png)

## <a name="turn-on-delayed-tax-calculation-at-the-journal-name-level"></a><span data-ttu-id="d24dd-124">Viivästyneen verojen laskemisen käyttöönotto kirjauskansion nimen tasolla</span><span class="sxs-lookup"><span data-stu-id="d24dd-124">Turn on delayed tax calculation at the journal name level</span></span>

1. <span data-ttu-id="d24dd-125">Siirry kohtaan **Kirjanpito \> Kirjauskansion asetukset \> Kirjauskansioiden nimet**.</span><span class="sxs-lookup"><span data-stu-id="d24dd-125">Go to **General ledger \> Journal setup \> Journal names**.</span></span>
2. <span data-ttu-id="d24dd-126">Aseta **Viivästynyt veron laskenta** -asetuksen arvoksi **Kyllä** **Arvonlisävero**-osan **Yleiset**-pikavälilehdessä.</span><span class="sxs-lookup"><span data-stu-id="d24dd-126">On the **General** FastTab, in the **Sales tax** section, set the **Delayed tax calculation** option to **Yes**.</span></span>

![Kirjauskansioiden nimien kuva](media/delayed-tax-calculation-journal-name.png)

## <a name="turn-on-delayed-tax-calculation-at-the-journal-header-level"></a><span data-ttu-id="d24dd-128">Viivästyneen verojen laskemisen käyttöönotto otsikkotasolla</span><span class="sxs-lookup"><span data-stu-id="d24dd-128">Turn on delayed tax calculation at the journal header level</span></span>

1. <span data-ttu-id="d24dd-129">Siirry kohtaan **Kirjanpito \> Kirjauskansioviennit \> Yleiset kirjauskansiot**.</span><span class="sxs-lookup"><span data-stu-id="d24dd-129">Go to **General ledger \> Journal entries \> General journals**.</span></span>
2. <span data-ttu-id="d24dd-130">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="d24dd-130">Select **New**.</span></span>
3. <span data-ttu-id="d24dd-131">Valitse kirjauskansion nimi.</span><span class="sxs-lookup"><span data-stu-id="d24dd-131">Select a journal name.</span></span>
4. <span data-ttu-id="d24dd-132">Aseta **Asetukset**-välilehden **Viivästynyt veron laskenta** -asetuksen arvoksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="d24dd-132">On the **Setup** tab, set the **Delayed tax calculation** option to **Yes**.</span></span>

![Kirjauskansiosivun kuva](media/delayed-tax-calculation-journal-header.png)
