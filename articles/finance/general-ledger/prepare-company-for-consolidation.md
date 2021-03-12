---
title: Valmistele yritys konsolidointiprosessia varten
description: Konsolidoinnin aikana kerätään tapahtumia useilta yrityksen tileiltä yhteen yrityksen tilien joukkoon. Tässä ohjeaiheessa kerrotaan, miten yritys valmistellaan konsolidointia varten.
author: jinniew
manager: AnnBe
ms.date: 10/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2018-10-30
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: f6fce69724945448f961769dd383d1047a5d13c4
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4990298"
---
# <a name="prepare-a-legal-entity-for-the-consolidation-process"></a><span data-ttu-id="7a294-104">Valmistele yritys konsolidointiprosessia varten</span><span class="sxs-lookup"><span data-stu-id="7a294-104">Prepare a legal entity for the consolidation process</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7a294-105">Konsolidoinnin aikana kerätään tapahtumia useilta yrityksen tileiltä yhteen yrityksen tilien joukkoon.</span><span class="sxs-lookup"><span data-stu-id="7a294-105">During a consolidation, you gather transactions from several sets of legal entity accounts into a single set of legal entity accounts.</span></span> <span data-ttu-id="7a294-106">Tässä ohjeaiheessa kerrotaan, miten yritys valmistellaan konsolidointia varten.</span><span class="sxs-lookup"><span data-stu-id="7a294-106">This topic explains how to prepare a legal entity for a consolidation.</span></span>

> [!NOTE]
> <span data-ttu-id="7a294-107">On suositeltavaa käyttää Microsoft Dynamics 365 Financen Management Reporteria, kun haluat yhdistää useiden yrityksen taloudelliset tulokset konsolidointimuodossa.</span><span class="sxs-lookup"><span data-stu-id="7a294-107">We recommend that you use Management Reporter for Microsoft Dynamics 365 Finance to combine the financial results for multiple legal entities in a consolidated format.</span></span> <span data-ttu-id="7a294-108">Management Reporterin avulla voit luoda konsolidointiraportteja eri yrityksille, tuoda konsolidointitietoja muista lähteistä Excelin avulla ja muuntaa summat miksi tahansa raportointivaluutaksi ilman, että konsolidointiprosessia tarvitsee suorittaa Dynamics 365 Financessa.</span><span class="sxs-lookup"><span data-stu-id="7a294-108">Management Reporter lets you create consolidated financial reports across legal entities, use Excel to import consolidation data from other sources, and translate amounts into any number of reporting currencies without having to run the consolidation process in Dynamics 365 Finance.</span></span>

<span data-ttu-id="7a294-109">Voit tulostaa raportteja, esimerkiksi tilinpäätöksiä, konsolidoidusta yrityksestä.</span><span class="sxs-lookup"><span data-stu-id="7a294-109">You can print reports, such as financial statements, from the consolidated legal entity.</span></span> <span data-ttu-id="7a294-110">Ei voi kuitenkaan käyttää konsolidoitua yritystä päivittäisiä tapahtumia varten.</span><span class="sxs-lookup"><span data-stu-id="7a294-110">However, you can't use the consolidated legal entity for daily transactions.</span></span>

<span data-ttu-id="7a294-111">Voit konsolidoida tiedot yrityksistä, jotka käyttävät eri tietokantoja kuin konsolidoitu yritys.</span><span class="sxs-lookup"><span data-stu-id="7a294-111">You can consolidate data from legal entities that use different databases than the consolidated legal entity.</span></span> <span data-ttu-id="7a294-112">Tätä konsolidointiprosessia kutsutaan *tuontikonsolidoinniksi*.</span><span class="sxs-lookup"><span data-stu-id="7a294-112">This consolidation process is referred to as an *import consolidation*.</span></span> <span data-ttu-id="7a294-113">Vaihtoehtoisesti yritykset voivat käyttää samaa tietokantaa kuin konsolidoitu yritys.</span><span class="sxs-lookup"><span data-stu-id="7a294-113">Alternatively, the legal entities can use the same database as the consolidated legal entity.</span></span> <span data-ttu-id="7a294-114">Tätä konsolidointiprosessia kutsutaan *online-konsolidoinniksi*.</span><span class="sxs-lookup"><span data-stu-id="7a294-114">This consolidation process is referred to as an *online consolidation*.</span></span>

<span data-ttu-id="7a294-115">Konsolidoitu yritys kerää tytäryhtiöiden tulokset ja saldot.</span><span class="sxs-lookup"><span data-stu-id="7a294-115">The consolidated legal entity collects the results and balances of the subsidiaries.</span></span> <span data-ttu-id="7a294-116">Noudata seuraavia vaiheita valmistellessasi konsolidoitua yritystä.</span><span class="sxs-lookup"><span data-stu-id="7a294-116">To prepare a consolidated legal entity for a consolidation, follow these steps.</span></span>

1. <span data-ttu-id="7a294-117">Siirry kohtaan **Kirjanpito \> Määritys \> Organisaatio \> Yritykset**.</span><span class="sxs-lookup"><span data-stu-id="7a294-117">Go to **General ledger \> Setup \> Organization \> Legal entities**.</span></span>
2. <span data-ttu-id="7a294-118">Valitse **Uusi** luodaksesi uuden yrityksen, josta tulee konsolidoitu yritys.</span><span class="sxs-lookup"><span data-stu-id="7a294-118">Select **New** to create the legal entity that will be the consolidated legal entity.</span></span>
3. <span data-ttu-id="7a294-119">Valitse **Käytä kirjanpidon konsolidointiprosessissa** -valintaruutu ja syötä konsolidointiyrityksen tiedot.</span><span class="sxs-lookup"><span data-stu-id="7a294-119">Select the **Use for financial consolidation process** check box, and then enter information about the consolidated legal entity.</span></span> <span data-ttu-id="7a294-120">Varmista, että kirjoitat tiedot täsmälleen samalla tavalla kuin haluat niiden näkyvän konsolidointiyrityksen raporteissa.</span><span class="sxs-lookup"><span data-stu-id="7a294-120">Be sure to enter this information exactly as you want it to appear on financial statements for the consolidated legal entity.</span></span>
4. <span data-ttu-id="7a294-121">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="7a294-121">Close the page.</span></span>
5. <span data-ttu-id="7a294-122">Valitse konsolidointiyritys kentässä sivun oikeassa yläkulmassa ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="7a294-122">Select the consolidated legal entity in the field in the upper-right corner of the page, and then select **OK**.</span></span>
6. <span data-ttu-id="7a294-123">Valitse **Kirjanpito \> Kirjanpidon asetukset \> Kirjanpito**.</span><span class="sxs-lookup"><span data-stu-id="7a294-123">Go to **General ledger \> Setup \> Ledger**.</span></span>
7. <span data-ttu-id="7a294-124">Valitse tilikartta, vuosikalenteri, kirjanpitovaluutta, valinnainen raportointivaluutta ja konsolidoidun yrityksen vaihtokurssin oletustyyppi.</span><span class="sxs-lookup"><span data-stu-id="7a294-124">Select the chart of accounts, the fiscal calendar, the accounting currency, an optional reporting currency, and the default type of exchange rate for the consolidated legal entity.</span></span> 
8. <span data-ttu-id="7a294-125">Siirry kohtaan **Kirjanpito \> Määritys \> Valuutta \> Valuutan vaihtokurssit**.</span><span class="sxs-lookup"><span data-stu-id="7a294-125">Go to **General ledger \> Setup \> Currency \> Currency exchange rates**.</span></span>
9. <span data-ttu-id="7a294-126">Määritä tytäryhtiöiden valuuttojen tarvittavien kausien vaihtokurssit.</span><span class="sxs-lookup"><span data-stu-id="7a294-126">Set up currency exchange rates in relevant periods for the currencies of the subsidiary legal entities.</span></span>
10. <span data-ttu-id="7a294-127">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="7a294-127">Close the page.</span></span>
11. <span data-ttu-id="7a294-128">Jos konsolidointiyrityksen yrityksellä on tytäryhtiöitä, jotka käyttävät ulkomaan valuuttoja, toimi seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="7a294-128">If the consolidated legal entity has subsidiaries that use foreign currencies, follow these steps:</span></span>

    1. <span data-ttu-id="7a294-129">Valitse **Kirjanpito \> Määritys \> Kirjaus \> Automaattisten tapahtumien tilit**.</span><span class="sxs-lookup"><span data-stu-id="7a294-129">Go to **General ledger \> Setup \> Posting \> Accounts for automatic transactions**.</span></span>
    2. <span data-ttu-id="7a294-130">Valitse asianmukainen tili **Kirjaustyyppi**-kentässä:</span><span class="sxs-lookup"><span data-stu-id="7a294-130">In the **Posting type** field, select an appropriate account:</span></span>

        - <span data-ttu-id="7a294-131">Jos yrityksellä on ulkomaisia tytäryhtiöitä, jotka ovat taloudellisesti tai taloudellisesti riippuvaisia emoyhtiön kanssa, valitse oikea tili **Tulos- ja tappiotili konsolidointieroille** -kirjaustyypille.</span><span class="sxs-lookup"><span data-stu-id="7a294-131">If the legal entity has foreign subsidiaries that are financially or operationally interdependent with the parent legal entity, select an appropriate account for the **Profit and loss account for consolidation differences** posting type.</span></span>
        - <span data-ttu-id="7a294-132">Jos konsolidoit tytäryhtiön, joka on taloudellisesti ja operatiivisesti riippumaton emoyhtiöstä, tai yrityksen, joka sisältää useiden emoyhtiöstä taloudellisesti ja operatiivisesti riippumattomien tytäryhtiöiden tulokset, ja jos käytät muuntomenetelmiä tietojen konsolidointiin, valitse oikea tili **Saldotili konsolidointieroille** -kirjaustyypille.</span><span class="sxs-lookup"><span data-stu-id="7a294-132">If you're consolidating a subsidiary that is financially and operationally independent of the parent legal entity, or a legal entity that contains the results of several subsidiaries that are financially and operationally independent of the parent legal entity, and if you're using translation methods to consolidate the data, select an appropriate account for the **Balance account for consolidation differences** posting type.</span></span>

    3. <span data-ttu-id="7a294-133">Valitse **Päätili**-kentästä päätilit, joita pitäisi käyttää ulkomaan valuutan uudelleenarvostuksen oikaisuihin.</span><span class="sxs-lookup"><span data-stu-id="7a294-133">In the **Main account** field, select the main accounts that should be used for foreign currency revaluation adjustments.</span></span>
    4. <span data-ttu-id="7a294-134">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="7a294-134">Close the page.</span></span>

    <span data-ttu-id="7a294-135">Jos luot konsolidointiyrityksen kauden alkuvaiheessa, vieraan valuutan summia voidaan arvioidan uudelleen vaihtokurssien muuttuessa konsolidointikauden aikana.</span><span class="sxs-lookup"><span data-stu-id="7a294-135">If you create the consolidated legal entity early in a period, you can revalue foreign currency amounts as exchange rates change during the consolidation period.</span></span>

<span data-ttu-id="7a294-136">Konsolidoitu yritys on nyt määritetty kausittaiselle **Konsolidoi**-työlle.</span><span class="sxs-lookup"><span data-stu-id="7a294-136">The consolidated legal entity is now set up for the **Consolidate** periodic job.</span></span> <span data-ttu-id="7a294-137">Voit tehdä tuontikonsolidoinnin tai online-konsolidoinnin.</span><span class="sxs-lookup"><span data-stu-id="7a294-137">You can do either an import consolidation or an online consolidation.</span></span>

- <span data-ttu-id="7a294-138">Voit tehdä tuontikonsolidoinnin kohdassa **Kirjanpito \> Kausittainen \> Konsolidoi \> Konsolidoi \[Tuo kohteesta\]**.</span><span class="sxs-lookup"><span data-stu-id="7a294-138">To do an import consolidation, go to **General ledger \> Periodic \> Consolidate \> Consolidate \[Import from\]**.</span></span>
- <span data-ttu-id="7a294-139">Voit tehdä online konsolidoinnin kohdassa **Kirjanpito \> Kausittainen \> Konsolidoi \> Konsolidoi \[Online\]**.</span><span class="sxs-lookup"><span data-stu-id="7a294-139">To do an online consolidation, go to **General ledger \> Periodic \> Consolidate \> Consolidate \[Online\]**.</span></span>

> [!NOTE]
> <span data-ttu-id="7a294-140">Ennen konsolidoinnin suorittamista yritykset on valmisteltava konsolidointia varten.</span><span class="sxs-lookup"><span data-stu-id="7a294-140">Before you can process the consolidation, you must prepare the subsidiary legal entities for consolidation.</span></span> <span data-ttu-id="7a294-141">Lisätietoja on kohdassa [Määritä tytäryhtiö konsolidointia varten](set-up-subsidiary-company-for-consolidation.md).</span><span class="sxs-lookup"><span data-stu-id="7a294-141">For more information, see [Set up a subsidiary legal entity for consolidation](set-up-subsidiary-company-for-consolidation.md).</span></span>
