---
title: Kirjanpitokalenterin muuttaminen tai määrittäminen uudelleen
description: Tässä ohjeaiheessa kerrotaan, miten kirjanpidon määritettyä kalenteria muutetaan ja miten uusi kalenteri määritetään kirjanpitoon.
author: kweekley
ms.date: 05/07/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2021-5-07
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 052b8944c0a015187d1d7c4ba3db878c52faeeea
ms.sourcegitcommit: 905a8c7a0c1bc06ada2acfba913dfe5f7b44ea16
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/14/2021
ms.locfileid: "6039947"
---
# <a name="change-or-reassign-a-ledger-calendar"></a><span data-ttu-id="5754a-103">Kirjanpitokalenterin muuttaminen tai määrittäminen uudelleen</span><span class="sxs-lookup"><span data-stu-id="5754a-103">Change or reassign a ledger calendar</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5754a-104">Tässä ohjeaiheessa kerrotaan, miten kirjanpidon määritettyä kalenteria muutetaan ja miten uusi kalenteri määritetään kirjanpitoon.</span><span class="sxs-lookup"><span data-stu-id="5754a-104">This topic explains how to change the calendar that is currently assigned to a ledger, and how to assign a new calendar to the ledger.</span></span>

## <a name="issue"></a><span data-ttu-id="5754a-105">Ongelma</span><span class="sxs-lookup"><span data-stu-id="5754a-105">Issue</span></span>

<span data-ttu-id="5754a-106">Joskus yritysten on joko muutettava olemassa olevaa kirjanpidon määritettyä kalenteria tai määritettävä uusi kalenteri.</span><span class="sxs-lookup"><span data-stu-id="5754a-106">Sometime, companies must either change the existing calendar that is assigned to a ledger or assign a new calendar.</span></span>

## <a name="resolution"></a><span data-ttu-id="5754a-107">Ratkaisu</span><span class="sxs-lookup"><span data-stu-id="5754a-107">Resolution</span></span>

<span data-ttu-id="5754a-108">Kirjanpitokalenterin muuttamiseksi tai sen määrittämiseksi uudelleen on kaksi eri skenaariota.</span><span class="sxs-lookup"><span data-stu-id="5754a-108">There are two scenarios for changing or reassigning a ledger calendar.</span></span> <span data-ttu-id="5754a-109">Ensimmäisessä skenaariossa muutetaan olemassa olevaa kalenteria, joka on jo määritetty kirjanpitoon.</span><span class="sxs-lookup"><span data-stu-id="5754a-109">The first scenario involves changing an existing calendar that is already assigned to the ledger.</span></span> <span data-ttu-id="5754a-110">Toisessa skenaariossa luodaan uusi kalenteri ja määritetään se kirjanpitoon.</span><span class="sxs-lookup"><span data-stu-id="5754a-110">The second scenario involves creating a new calendar and assigning it to the ledger.</span></span> <span data-ttu-id="5754a-111">Molemmat muutokset voidaan tehdä milloin tahansa. Ne voidaan tehdä jopa sen jälkeen, kun kirjanpitoon on kirjattu tapahtumia.</span><span class="sxs-lookup"><span data-stu-id="5754a-111">Both changes can be done at any time, even after transactions have been posted to the ledger.</span></span>

### <a name="change-an-existing-fiscal-calendar"></a><span data-ttu-id="5754a-112">Aiemmin luodun kirjanpidon kalenterin muuttaminen</span><span class="sxs-lookup"><span data-stu-id="5754a-112">Change an existing fiscal calendar</span></span>

<span data-ttu-id="5754a-113">Jos haluat muuttaa kirjanpidon määritettyä olemassa olevaa kalenteria, siirry kohtaan **Kirjanpito \> Kirjanpidon asetukset \> Kirjanpito** ja avaa **Kirjanpidon kalenterit** -sivu valitsemalla kirjanpidon kalenterin linkki.</span><span class="sxs-lookup"><span data-stu-id="5754a-113">To change an existing calendar that is assigned to your ledger, go to **General ledger \> Ledger setup \> Ledger**, and select the link for the fiscal calendar to open the **Ledger calendars** page.</span></span>

<span data-ttu-id="5754a-114">Kalenteriin ei voi tehdä mitä tahansa muutoksia.</span><span class="sxs-lookup"><span data-stu-id="5754a-114">There are limits to the changes that can be made to a calendar.</span></span> <span data-ttu-id="5754a-115">Esimerkiksi vuoden *jaksojen* aloitus- ja päättymispäivää voi muuttaa, mutta kalenterin *vuoden* aloitus- ja päättymispäivää ei voi muuttaa.</span><span class="sxs-lookup"><span data-stu-id="5754a-115">For example, you can change the start and end dates of the *periods* in a year, but you can't change the start and end dates of a *year* in the calendar.</span></span>

<span data-ttu-id="5754a-116">Jos haluat muuttaa vuoden jaksoja, valitse haluamasi kalenteri ja vuosi.</span><span class="sxs-lookup"><span data-stu-id="5754a-116">To change the periods in a year, select the appropriate calendar and year.</span></span> <span data-ttu-id="5754a-117">Poista ensin joitakin toimintajaksoja tai kaikki toimintajaksot **Poista jakso** -painikkeen avulla.</span><span class="sxs-lookup"><span data-stu-id="5754a-117">First, use the use the **Delete period** button to delete some or all of the existing operating periods.</span></span> <span data-ttu-id="5754a-118">Kaikki toimintajaksot voidaan poistaa ensimmäistä lukuun ottamatta.</span><span class="sxs-lookup"><span data-stu-id="5754a-118">All operating periods except the first can be deleted.</span></span> <span data-ttu-id="5754a-119">Jaa sitten jäljellä oleva jakso tai jäljellä olevat jaksot **Jaa jakso** -painikkeen avulla uusiksi jaksoiksi syöttämällä seuraavalle jaksolle soveltuva aloituspäivämäärä.</span><span class="sxs-lookup"><span data-stu-id="5754a-119">Then use the **Divide period** button to divide the remaining period or periods into new periods by entering an appropriate start date for the next period.</span></span>

<span data-ttu-id="5754a-120">Kun kalenterin jaksot on muutettu, suorita **Laske kirjanpidon jaksot uudelleen** -prosessi jokaisessa yrityksessä, jolle kalenteri on määritetty.</span><span class="sxs-lookup"><span data-stu-id="5754a-120">After you change the periods in a calendar, you must run the **Recalculate ledger periods** process in every legal entity (company) that the calendar is assigned to.</span></span> <span data-ttu-id="5754a-121">Vaikka tämän vaiheen suorittamisesta ei muistuteta varoitussanomalla, uudelleenlaskentaprosessi vaaditaan, jotta kirjanpidon kuhunkin kirjattuun tapahtumaan määritetty jakso päivitetään.</span><span class="sxs-lookup"><span data-stu-id="5754a-121">Although no warning message reminds you to complete this step, the recalculation process is required to update the period that is assigned to each posted transaction in General ledger.</span></span> <span data-ttu-id="5754a-122">Voit suorittaa uudelleenlaskentaprosessin valitsemalla **Laske kirjanpidon jaksot uudelleen** kunkin yrityksen **Kirjanpidon asetukset** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="5754a-122">To run the recalculation process, select **Recalculate ledger periods** on the **Ledger setup** page in each company.</span></span>

<span data-ttu-id="5754a-123">Jos uudelleenlaskentaprosessia ei suoriteta, pääkirjan tai raporttien tapahtumien saldojen sisällytys jaksoihin voi olla virheellinen.</span><span class="sxs-lookup"><span data-stu-id="5754a-123">If the recalculation process isn't run, transaction balances on a trial balance or on financial statements might be incorrectly included in periods.</span></span> <span data-ttu-id="5754a-124">Tässä tapauksessa voit korjata saldot milloin tahansa suorittamalla uudelleenlaskentaprosessin.</span><span class="sxs-lookup"><span data-stu-id="5754a-124">In this case, you can correct the balances at any time by running the recalculation process.</span></span>

### <a name="assign-a-new-fiscal-calendar"></a><span data-ttu-id="5754a-125">Uuden kirjanpidon kalenterin määrittäminen</span><span class="sxs-lookup"><span data-stu-id="5754a-125">Assign a new fiscal calendar</span></span>

<span data-ttu-id="5754a-126">Jos haluat määrittää uuden kirjanpidon kalenterin, siirry kohtaan **Kirjanpito \> Kirjanpidon asetukset \> Kirjanpito** ja valitse **Muokkaa**. Tämän jälkeen **Kirjanpito**-sivu on muokkaustilassa.</span><span class="sxs-lookup"><span data-stu-id="5754a-126">To assign a new fiscal calendar, go to **General ledger \> Ledger setup \> Ledger**, and select **Edit** to put the **Ledger** page into edit mode.</span></span> <span data-ttu-id="5754a-127">Valitse sitten **Kirjanpidon kalenteri** -kenttä ja valitse uusi kirjanpidon kalenteri.</span><span class="sxs-lookup"><span data-stu-id="5754a-127">Then, in the **Fiscal calendar** field, select a new fiscal calendar.</span></span>

<span data-ttu-id="5754a-128">Kun kirjanpidon kalenteria on muutettu, suorita **Laske kirjanpidon jaksot uudelleen**.</span><span class="sxs-lookup"><span data-stu-id="5754a-128">After you change the fiscal calendar for a ledger, you must run the **Recalculate ledger periods**.</span></span> <span data-ttu-id="5754a-129">Kun määrität kirjanpitoon uuden kirjanpidon kalenterin, näyttöön tulee tämän vaiheen suorittamisesta muistuttava sanoma.</span><span class="sxs-lookup"><span data-stu-id="5754a-129">When you assign a new fiscal calendar to a ledger, a message reminds you to complete this step.</span></span> <span data-ttu-id="5754a-130">Uudelleenlaskentaprosessi ei ole valinnainen, vaikka sanomasta saattaa saada sellaisen kuvan.</span><span class="sxs-lookup"><span data-stu-id="5754a-130">Although the message might seem to indicate that the recalculation process is optional, it isn't.</span></span> <span data-ttu-id="5754a-131">Kirjanpidon kullekin kirjatulle tapahtumalle määritetty jakso on päivitettävä.</span><span class="sxs-lookup"><span data-stu-id="5754a-131">It's required to update the period that is assigned to each posted transaction in General ledger.</span></span> <span data-ttu-id="5754a-132">Jos haluat suorittaa uudelleenlaskentaprosessin, valitse **Laske kirjanpidon jaksot uudelleen** **Kirjanpidon asetukset** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="5754a-132">To run the recalculation process, select **Recalculate ledger periods** on the **Ledger setup** page.</span></span>

<span data-ttu-id="5754a-133">Jos uudelleenlaskentaprosessia ei suoriteta, pääkirjan tai raporttien tapahtumien saldojen sisällytys jaksoihin voi olla virheellinen.</span><span class="sxs-lookup"><span data-stu-id="5754a-133">If the recalculation process isn't run, transaction balances on a trial balance or on financial statements might be incorrectly included in periods.</span></span> <span data-ttu-id="5754a-134">Tässä tapauksessa voit korjata saldot milloin tahansa suorittamalla uudelleenlaskentaprosessin.</span><span class="sxs-lookup"><span data-stu-id="5754a-134">In this case, you can correct the balances at any time by running the recalculation process.</span></span>
