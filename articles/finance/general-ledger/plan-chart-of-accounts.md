---
title: Tilikartan suunnittelu
description: Tässä ohjeaiheessa on tietoja, joiden avulla voit suunnitella organisaation tilikartan.
author: aprilolson
manager: AnnBe
ms.date: 04/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DimensionConfigureAccountStructure, LedgerChartOfAccounts
audience: Application User
ms.reviewer: roschlom
ms.custom: 14051
ms.assetid: 10edb129-33f0-4cf9-b2a7-4b7ffa09b229
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6e568fca70ea2048d881681ff7ab8ebc6fad6450
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4990361"
---
# <a name="plan-your-chart-of-accounts"></a><span data-ttu-id="e58c1-103">Tilikartan suunnittelu</span><span class="sxs-lookup"><span data-stu-id="e58c1-103">Plan your chart of accounts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e58c1-104">Tässä ohjeaiheessa on tietoja, joiden avulla voit suunnitella organisaation tilikartan.</span><span class="sxs-lookup"><span data-stu-id="e58c1-104">This topic provides information that will help you plan the chart of accounts for your organization.</span></span>

<span data-ttu-id="e58c1-105">Seuraa ja ylläpidä taloushallinnon tietoja organisaatiossa määrittämällä tilikartta.</span><span class="sxs-lookup"><span data-stu-id="e58c1-105">To track and maintain financial information in an organization, you can set up a chart of accounts.</span></span> <span data-ttu-id="e58c1-106">Se on tilikokoelma, joka määrittää taloudellisen kehikon.</span><span class="sxs-lookup"><span data-stu-id="e58c1-106">A chart of accounts is a collection of accounts that define a financial framework.</span></span> <span data-ttu-id="e58c1-107">Voit parantaa näiden tilien tapahtumien seurantaa lisäämällä segmenttejä.</span><span class="sxs-lookup"><span data-stu-id="e58c1-107">To further track the transactions in these accounts, you can add segments.</span></span> <span data-ttu-id="e58c1-108">Näitä segmenttejä kutsutaan taloushallinnon dimensioiksi.</span><span class="sxs-lookup"><span data-stu-id="e58c1-108">These segments are known as financial dimensions.</span></span> <span data-ttu-id="e58c1-109">Kulutili saattaa sisältää esimerkiksi taloushallinnon dimensiot nimeltä osasto, kustannuspaikka ja tarkoitus.</span><span class="sxs-lookup"><span data-stu-id="e58c1-109">For example, an expense account might include financial dimensions that are named Department, Cost center, and Purpose.</span></span> <span data-ttu-id="e58c1-110">Käyttäjän määrittämät säännöt määrittävät, miten nämä taloushallinnon dimensiot liitetään päätileihin ja muihin taloushallinnon dimensioihin sekä miten tapahtumat kirjataan.</span><span class="sxs-lookup"><span data-stu-id="e58c1-110">User-defined rules determine how financial dimensions are attached to the main accounts and to other financial dimensions, and also how transactions are entered.</span></span> <span data-ttu-id="e58c1-111">Käyttäjän määrittämä sääntöjä kutsutaan myös tilirakenteeksi ja lisäsäännöiksi.</span><span class="sxs-lookup"><span data-stu-id="e58c1-111">These user-defined rules are known as account structures and advanced rules.</span></span>

<span data-ttu-id="e58c1-112">Tilikartta on yrityksen kirjanpitotilien rakenteinen luettelo.</span><span class="sxs-lookup"><span data-stu-id="e58c1-112">The chart of accounts is a structured list of a legal entity's general ledger accounts.</span></span> <span data-ttu-id="e58c1-113">Luettelon avulla valmistellaan tilinpäätökset viranomaisia ja omistajia varten.</span><span class="sxs-lookup"><span data-stu-id="e58c1-113">The list is used to prepare financial reports for authorities and owners.</span></span> <span data-ttu-id="e58c1-114">Tilit on ryhmitelty ensin tilityyppeihin ja yhdistetty sitten suuremmiksi luokiksi.</span><span class="sxs-lookup"><span data-stu-id="e58c1-114">The accounts are first grouped into types of accounts and then further aggregated into larger categories.</span></span> <span data-ttu-id="e58c1-115">Yleisimmällä tasolla tilit on ryhmitelty tuotoiksi ja kustannuksiksi (käyttötilit) sekä varallisuudeksi ja veloiksi (tasetilit).</span><span class="sxs-lookup"><span data-stu-id="e58c1-115">At the most general level, the accounts are grouped as revenues and costs (operating accounts), and assets and liabilities (balance accounts).</span></span>

<span data-ttu-id="e58c1-116">Tilikartta voidaan jakaa käytettäväksi minkä tahansa organisaation yrityksen välillä.</span><span class="sxs-lookup"><span data-stu-id="e58c1-116">A chart of accounts can be shared and used by any legal entity in an organization.</span></span> <span data-ttu-id="e58c1-117">Yrityksen käyttämä tilikartta määritetään **Kirjanpito**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="e58c1-117">The chart of accounts that is used by a legal entity is defined on the **Ledger** page.</span></span>

<span data-ttu-id="e58c1-118">Tilikartan rakennetta suunniteltaessa täytyy kiinnittää huomiota esimerkiksi seuraaviin seikkoihin:</span><span class="sxs-lookup"><span data-stu-id="e58c1-118">Here are some of the factors that you must consider when you plan the structure of the chart of accounts for your organization:</span></span>

- <span data-ttu-id="e58c1-119">Organisaatiosi toimintamaassa tai toiminta-alueella voimassa olevat raportointivaatimukset</span><span class="sxs-lookup"><span data-stu-id="e58c1-119">The reporting requirements of the country or region where your organization is based</span></span>
- <span data-ttu-id="e58c1-120">Oman yrityksen voimassa olevat raportointivaatimukset</span><span class="sxs-lookup"><span data-stu-id="e58c1-120">The reporting requirements of your legal entity</span></span>
- <span data-ttu-id="e58c1-121">Ulkoisten organisaatioiden ja organisaatiosi tarvitsemien tietojen tarkkuus</span><span class="sxs-lookup"><span data-stu-id="e58c1-121">The degree of specification that is required, both for both external organizations and for your organization</span></span>

<span data-ttu-id="e58c1-122">Voit luoda tilikarttoja **Tilikartat**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="e58c1-122">You create the chart of accounts on the **Chart of accounts** page.</span></span> <span data-ttu-id="e58c1-123">Voit luoda päätilejä **Tilikartat**- tai **Päätilit**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="e58c1-123">You can create main accounts from the **Chart of accounts** page or the **Main accounts** page.</span></span> <span data-ttu-id="e58c1-124">Päätileillä ei tule käyttää erikoismerkkejä, joita käytetään tilikartoissa erottimina.</span><span class="sxs-lookup"><span data-stu-id="e58c1-124">Your main accounts shouldn't use any special characters that are used as delimiters for chart of accounts.</span></span> <span data-ttu-id="e58c1-125">Muussa tapauksena seurauksena voi olla toiminnan epävakautta tai tilien ja dimensioiden yhdistelmien kirjaamiseen on ehkä aina käytettävä hakua ja valintaikkunaa.</span><span class="sxs-lookup"><span data-stu-id="e58c1-125">Otherwise, you might experience instability, or you might always have to use lookups or the dialog box when you enter combinations of accounts and dimensions.</span></span> <span data-ttu-id="e58c1-126">Lisätietoja on ohjeaiheessa [Päätilin luominen](tasks/create-main-account.md).</span><span class="sxs-lookup"><span data-stu-id="e58c1-126">For more information, see [Create a main account](tasks/create-main-account.md).</span></span>

> [!NOTE]
> <span data-ttu-id="e58c1-127">Voit muokata tilikartan erotinta Dynamics 365 for Finance and Operationsin version 8.0 (huhtikuu 2018) **Kirjanpitoparametrit**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="e58c1-127">In Dynamics 365 for Finance and Operations version 8.0 (April 2018), you can modify the chart of accounts delimiter from the **General ledger parameters** page.</span></span>

<span data-ttu-id="e58c1-128">Päätilit kannattaa linkittää päätililuokkiin, jolloin oletusraportteja voidaan käyttää ilman muutoksia.</span><span class="sxs-lookup"><span data-stu-id="e58c1-128">It's a good idea to link the main accounts to main account categories, so that you can take advantage of the default financial reports without having to make any modifications.</span></span> <span data-ttu-id="e58c1-129">Tällöin voit suunnitella ja ylläpitää raportteja nopeasti ja helposti.</span><span class="sxs-lookup"><span data-stu-id="e58c1-129">Therefore, you can more quickly and easily design and maintain reports.</span></span>

<span data-ttu-id="e58c1-130">Voit luoda tilirakenteita **Määritä tilirakenteet** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="e58c1-130">You create account structures on the **Configure account structures** page.</span></span> <span data-ttu-id="e58c1-131">Tilirakenteet määrittävät sallitut yhdistelmät.</span><span class="sxs-lookup"><span data-stu-id="e58c1-131">Account structures define valid combinations.</span></span> <span data-ttu-id="e58c1-132">Nämä yhdistelmät yhdessä päätilien kanssa muodostavat tilikartan.</span><span class="sxs-lookup"><span data-stu-id="e58c1-132">These combinations, together with main accounts, form a chart of accounts.</span></span> <span data-ttu-id="e58c1-133">Lisätietoja on ohjeaiheessa [Tilirakenteen luominen](tasks/create-account-structures.md).</span><span class="sxs-lookup"><span data-stu-id="e58c1-133">For more information, see [Create account structures](tasks/create-account-structures.md).</span></span>

<span data-ttu-id="e58c1-134">**Yrityksen ohitukset**</span><span class="sxs-lookup"><span data-stu-id="e58c1-134">**Legal entity overrides**</span></span>

<span data-ttu-id="e58c1-135">Kaikki päätilit eivät kelpaa kaikille yrityksille ja tietty päätili saattaa olla tarpeellinen vain tietyn kauden ajan.</span><span class="sxs-lookup"><span data-stu-id="e58c1-135">Not all main accounts are valid for all legal entities, and some main account might be relevant only for a specific period.</span></span> <span data-ttu-id="e58c1-136">Tässä skenaariossa voit määrittää **Yrityksen ohitukset** -osassa yritykset, joissa päätilin käyttö pitäisi keskeyttää, omistajan sekä kauden, jolloin dimensio on aktiivinen.</span><span class="sxs-lookup"><span data-stu-id="e58c1-136">In this scenario, you can use the **Legal entity overrides** section to identify the companies that the main account should be suspended for, the owner, and the period when the dimension is active.</span></span> <span data-ttu-id="e58c1-137">Jaetun tason ohitukset eivät voi olla rajoittavampia kuin yritystason ohitukset.</span><span class="sxs-lookup"><span data-stu-id="e58c1-137">The overrides at the shared level can't be more restrictive than the overrides at the legal entity level.</span></span>

<span data-ttu-id="e58c1-138">Lisätietoja on seuraavissa aiheissa:</span><span class="sxs-lookup"><span data-stu-id="e58c1-138">For more information, see the following topics:</span></span>

- [<span data-ttu-id="e58c1-139">Taloushallinnon dimensiot</span><span class="sxs-lookup"><span data-stu-id="e58c1-139">Financial dimensions</span></span>](financial-dimensions.md)
- [<span data-ttu-id="e58c1-140">Luo ja määritä lisäsääntörakenteet</span><span class="sxs-lookup"><span data-stu-id="e58c1-140">Create and assign advanced rule structures</span></span>](tasks/create-assign-advanced-rule-structures.md)
