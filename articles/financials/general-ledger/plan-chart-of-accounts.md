---
title: Suunnittele tilikarttasi
description: "Tässä artikkelissa on tietoja, joiden avulla voit suunnitella organisaation tilikartan."
author: aprilolson
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DimensionConfigureAccountStructure, LedgerChartOfAccounts
audience: Application User
ms.reviewer: robinr
ms.search.scope: Core, Operations
ms.custom: 14051
ms.assetid: 10edb129-33f0-4cf9-b2a7-4b7ffa09b229
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 038886f0a6e1c133a33ee34725eb20352e64341a
ms.contentlocale: fi-fi
ms.lasthandoff: 11/03/2017

---

# <a name="plan-your-chart-of-accounts"></a><span data-ttu-id="295c1-103">Suunnittele tilikarttasi</span><span class="sxs-lookup"><span data-stu-id="295c1-103">Plan your chart of accounts</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="295c1-104">Tässä artikkelissa on tietoja, joiden avulla voit suunnitella organisaation tilikartan.</span><span class="sxs-lookup"><span data-stu-id="295c1-104">This article provides information that will help you plan the chart of accounts for your organization.</span></span>

<span data-ttu-id="295c1-105">Seuraa ja ylläpidä taloushallinnon tietoja organisaatiossa määrittämällä tilikartta.</span><span class="sxs-lookup"><span data-stu-id="295c1-105">To track and maintain financial information in an organization, you can set up a chart of accounts.</span></span> <span data-ttu-id="295c1-106">Se on tilikokoelma, joka määrittää taloudellisen kehikon.</span><span class="sxs-lookup"><span data-stu-id="295c1-106">A chart of accounts is a collection of accounts that define a financial framework.</span></span> <span data-ttu-id="295c1-107">Näillä tileillä olevien tapahtumien lisäseurantaa varten voi lisätä segmenttejä, joita kutsutaan taloushallinnon dimensioiksi.</span><span class="sxs-lookup"><span data-stu-id="295c1-107">To further track the transactions in these accounts, you can add segments, which are known as financial dimensions.</span></span> <span data-ttu-id="295c1-108">Kulutili saattaa sisältää esimerkiksi taloushallinnon dimensiot nimeltä osasto, kustannuspaikka ja tarkoitus.</span><span class="sxs-lookup"><span data-stu-id="295c1-108">For example, an expense account might include financial dimensions that are named Department, Cost center, and Purpose.</span></span> <span data-ttu-id="295c1-109">Käyttäjän määrittämät säännöt, joita kutsutaan tilirakenteiksi ja lisäsäännöksi, määrittävät, miten nämä taloushallinnon dimensiot liitetään päätileihin ja muihin taloushallinnon dimensioihin, ja miten tapahtumia voidaan syöttää.</span><span class="sxs-lookup"><span data-stu-id="295c1-109">User-defined rules, which are known as account structures and advanced rules, determine how financial dimensions are attached to the main accounts and other financial dimensions, and also how transactions are entered.</span></span> 

<span data-ttu-id="295c1-110">Tilikartta on yrityksen kirjanpitotilien rakenteinen luettelo.</span><span class="sxs-lookup"><span data-stu-id="295c1-110">The chart of accounts is a structured list of a legal entity’s general ledger accounts.</span></span> <span data-ttu-id="295c1-111">Luettelon avulla valmistellaan tilinpäätökset viranomaisia ja omistajia varten.</span><span class="sxs-lookup"><span data-stu-id="295c1-111">The list is used to prepare financial reports for authorities and owners.</span></span> <span data-ttu-id="295c1-112">Tilit on ryhmitelty tilityyppeihin ja yhdistetty suuremmiksi luokiksi.</span><span class="sxs-lookup"><span data-stu-id="295c1-112">The accounts are grouped into types of accounts and then further aggregated into larger categories.</span></span> <span data-ttu-id="295c1-113">Yleisimmällä tasolla tilit on ryhmitelty tuotoiksi ja kustannuksiksi (käyttötilit) sekä varallisuudeksi ja veloiksi (tasetilit).</span><span class="sxs-lookup"><span data-stu-id="295c1-113">At the most general level, the accounts are grouped as revenues and costs (operating accounts), and assets and liabilities (balance accounts).</span></span> 

<span data-ttu-id="295c1-114">Tilikartta voidaan jakaa käytettäväksi minkä tahansa organisaation yrityksen välillä.</span><span class="sxs-lookup"><span data-stu-id="295c1-114">A chart of accounts can be shared and used by any legal entity in an organization.</span></span> <span data-ttu-id="295c1-115">Yrityksen käyttämä tilikartta määritetään **Kirjanpito**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="295c1-115">The chart of accounts that is used by a legal entity is defined on the **Ledger** page.</span></span> 

<span data-ttu-id="295c1-116">Tilikartan rakennetta suunniteltaessa täytyy kiinnittää huomiota esimerkiksi seuraaviin seikkoihin:</span><span class="sxs-lookup"><span data-stu-id="295c1-116">Here are some of the factors that you must consider when you plan the structure of the chart of accounts for your organization:</span></span>

-   <span data-ttu-id="295c1-117">Organisaatiosi toimintamaassa tai toiminta-alueella voimassa olevat raportointivaatimukset</span><span class="sxs-lookup"><span data-stu-id="295c1-117">The reporting requirements of the country/region where your organization is based</span></span>
-   <span data-ttu-id="295c1-118">Oman yrityksen voimassa olevat raportointivaatimukset</span><span class="sxs-lookup"><span data-stu-id="295c1-118">The reporting requirements of your legal entity</span></span>
-   <span data-ttu-id="295c1-119">Ulkoisten organisaatioiden ja organisaatiosi tarvitsemien tietojen tarkkuus</span><span class="sxs-lookup"><span data-stu-id="295c1-119">The degree of specification that is required, both for both external organizations and for your organization</span></span>

<span data-ttu-id="295c1-120">Voit määrittää tilikartat **Tilikartat**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="295c1-120">Create the chart of accounts on the **Chart of accounts** page.</span></span> <span data-ttu-id="295c1-121">Päätilit voidaan luoda **Tilikartat**- tai **Päätilit**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="295c1-121">Main accounts can be created from the **Chart of accounts** page or the **Main accounts** page.</span></span> <span data-ttu-id="295c1-122">Päätileillä ei tule käyttää erikoismerkkejä, joita käytetään tilikartoissa erottimina.</span><span class="sxs-lookup"><span data-stu-id="295c1-122">Your main accounts shouldn't use any special characters that are used as chart of accounts delimiters.</span></span> <span data-ttu-id="295c1-123">Jos päätilillä on erikoismerkki, jota käytetään tilikartan erottimena, toiminta saattaa olla epävakaata tai tilien ja dimensioiden yhdistelmien syöttämisessä on käytettävä jatkuvasti arvohakuja tai lisätietoikkunoita.</span><span class="sxs-lookup"><span data-stu-id="295c1-123">If you do have a special character that is the same as your chart of accounts delimiter, you may experience instability, or the need to always use lookups or the flyout when entering account and dimension combinations.</span></span> <span data-ttu-id="295c1-124">Lisätietoja on ohjeaiheessa [Päätilin luominen](tasks/create-account-structures.md).</span><span class="sxs-lookup"><span data-stu-id="295c1-124">For more information, see [Create a main account](tasks/create-account-structures.md).</span></span>


<span data-ttu-id="295c1-125">Päätilit kannattaa linkittää päätililuokkiin, jolloin oletusraportteja voidaan käyttää ilman muutoksia.</span><span class="sxs-lookup"><span data-stu-id="295c1-125">It's a good idea to link the main accounts to main account categories, so that you can take advantage of the default financial reports without having to make any modifications.</span></span> <span data-ttu-id="295c1-126">Tällöin voit suunnitella ja ylläpitää raportteja nopeasti ja helposti.</span><span class="sxs-lookup"><span data-stu-id="295c1-126">Therefore, you can more quickly and easily design and maintain reports.</span></span> 

<span data-ttu-id="295c1-127">**Määritä tilirakenteet** -sivun avulla voit luoda tilirakenteita.</span><span class="sxs-lookup"><span data-stu-id="295c1-127">Use the **Configure account structures** page to create account structures.</span></span> <span data-ttu-id="295c1-128">Tilirakenteet määrittävät sallitut yhdistelmät.</span><span class="sxs-lookup"><span data-stu-id="295c1-128">Account structures define valid combinations.</span></span> <span data-ttu-id="295c1-129">Yhdistelmät yhdessä päätilien kanssa muodostavat tilikartan.</span><span class="sxs-lookup"><span data-stu-id="295c1-129">The combinations, together with main accounts, form a chart of accounts.</span></span>  <span data-ttu-id="295c1-130">Lisätietoja on ohjeaiheessa [Tilirakenteen luominen](tasks/create-main-account.md).</span><span class="sxs-lookup"><span data-stu-id="295c1-130">For more information, see [Create account structures](tasks/create-main-account.md).</span></span>

<span data-ttu-id="295c1-131">**Yrityksen ohitukset**</span><span class="sxs-lookup"><span data-stu-id="295c1-131">**Legal entity overrides**</span></span> 

<span data-ttu-id="295c1-132">Kaikki päätilit eivät kelpaa kaikille yrityksille, ja jotkin päätilit saattavat olla olennaisia vain tietyn ajanjakson ajan.</span><span class="sxs-lookup"><span data-stu-id="295c1-132">Not all main accounts are valid for all legal entities and some may only be relevant for a specific time period.</span></span> <span data-ttu-id="295c1-133">Tässä skenaariossa Yrityksen ohitukset -osan avulla määritetään yritykset, joilta päätilin käyttö keskeytetään, omistaja sekä ajanjakso, jolloin dimensio on aktiivinen.</span><span class="sxs-lookup"><span data-stu-id="295c1-133">In this scenario the Legal entity overrides section can be used to identify which companies the main account should be suspended for, who the owner is and the time period the dimension is active.</span></span> <span data-ttu-id="295c1-134">Jaetun tason ohitukset eivät voi olla rajoittavampia kuin yritystason ohitukset.</span><span class="sxs-lookup"><span data-stu-id="295c1-134">The overrides at the shared level cannot be more restrictive than the overrides at the legal entity level.</span></span>

<span data-ttu-id="295c1-135">Lisätietoja on seuraavissa ohjeaiheissa: [Taloushallinnon dimensiot](financial-dimensions.md)
[Lisäsääntörakenteiden luominen ja määrittäminen](tasks/create-assign-advanced-rule-structures.md)</span><span class="sxs-lookup"><span data-stu-id="295c1-135">For more information, see the following topics: [Financial dimensions](financial-dimensions.md)
[Create and assign advanced rule structures](tasks/create-assign-advanced-rule-structures.md)</span></span>




