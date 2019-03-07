---
title: Kirjoita tilien ja dimensioiden yhdistelmät (komponentin segmentoidun tarkistus)
description: Tässä artikkelissa kerrotaan, miten tili- ja dimensioyhdistelmiä tai kirjanpitotilejä kirjataan. Kirjauskokokemusta sanotaan usein segmentoidun kirjauksen hallinnaksi.
author: aprilolson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DimensionConfigureAccountStructure
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 14071
ms.assetid: e6fce826-c403-4d91-a78b-e9a58c44ac03
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c9addb2897bac68115a38f0239764ab65af2378c
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "315656"
---
# <a name="enter-account-and-dimension-combinations-segmented-entry-control"></a><span data-ttu-id="1a9ad-104">Kirjoita tilien ja dimensioiden yhdistelmät (komponentin segmentoidun tarkistus)</span><span class="sxs-lookup"><span data-stu-id="1a9ad-104">Enter account and dimension combinations (segmented entry control)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1a9ad-105">Tässä artikkelissa kerrotaan, miten tili- ja dimensioyhdistelmiä tai kirjanpitotilejä kirjataan.</span><span class="sxs-lookup"><span data-stu-id="1a9ad-105">This article describes how to enter account and dimension combinations or ledger accounts.</span></span> <span data-ttu-id="1a9ad-106">Kirjauskokokemusta sanotaan usein segmentoidun kirjauksen hallinnaksi.</span><span class="sxs-lookup"><span data-stu-id="1a9ad-106">The entry experience is often referred to as segmented entry control.</span></span>

<span data-ttu-id="1a9ad-107">Käyttäjät syöttävät tilien ja dimensioiden yhdistelmät eri sivuille, kuten kirjauskansioiden sivuille, budjetointiin ja kirjausmääritelmiin.</span><span class="sxs-lookup"><span data-stu-id="1a9ad-107">Users enter account and dimension combinations on various pages, such as pages for general journals, budgeting, and posting definitions.</span></span> <span data-ttu-id="1a9ad-108">Voimassaolevat tili- ja dimensioyhdistelmät riippuvat tilirakenteista, jotka on määritetty kirjanpidossa ja kehittyneistä säännöistä, jotka on määritetty tilirakenteisiin.</span><span class="sxs-lookup"><span data-stu-id="1a9ad-108">The valid account and dimension combinations depend on the account structures that are assigned to the ledger and the advanced rules that are assigned to the account structures.</span></span> <span data-ttu-id="1a9ad-109">Kun käyttäjät syöttävät yhdistelmän, he voivat joko syöttää arvot manuaalisesti tai hyödyntää syvää hakukokemusta.</span><span class="sxs-lookup"><span data-stu-id="1a9ad-109">When users enter a combination, they can either manually type the values or take advantage of a rich, lookup experience.</span></span> <span data-ttu-id="1a9ad-110">Kun syötät kenttään, voit aloittaa kirjoittamisen ja se etsii arvon ja kuvauksen.</span><span class="sxs-lookup"><span data-stu-id="1a9ad-110">When you enter the field, you can start to type and it will search the value and the description.</span></span> <span data-ttu-id="1a9ad-111">Esimerkiksi jos kirjoitat "180", se etsii kaikki arvot, jotka alkavat kyseisellä numerolla.</span><span class="sxs-lookup"><span data-stu-id="1a9ad-111">For example, if you type 180 it will search any value that begins with that number combination.</span></span> <span data-ttu-id="1a9ad-112">Tai voit kirjoittaa "Maksu", ja se etsii kaikki arvot, joilla on kuvaus, joka alkaa merkkijonolla Maksu.</span><span class="sxs-lookup"><span data-stu-id="1a9ad-112">Or you may type Cash and it will search any value that has a description that begins with Cash.</span></span> <span data-ttu-id="1a9ad-113">Voit käyttää myös yleismerkkejä, kuten \*Maksu tai \*180, etsimiseen, jos arvo tai kuvaus sisältää hakuehdon.</span><span class="sxs-lookup"><span data-stu-id="1a9ad-113">You can also use a wildcard, such as \*Cash or \*180 to search if the value or description contain the search criteria.</span></span> 

<span data-ttu-id="1a9ad-114">Seuraavassa taulukossa kuvataan pikanäppäimiä, joita voidaan käyttää, kun haku on suljettu.</span><span class="sxs-lookup"><span data-stu-id="1a9ad-114">The following table describes the keyboard shortcuts that can be used when the lookup is closed.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1a9ad-115">Pikanäppäin</span><span class="sxs-lookup"><span data-stu-id="1a9ad-115">Keyboard shortcut</span></span></th>
<th><span data-ttu-id="1a9ad-116">Toiminto</span><span class="sxs-lookup"><span data-stu-id="1a9ad-116">Action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1a9ad-117">Alt+Alanuoli</span><span class="sxs-lookup"><span data-stu-id="1a9ad-117">Alt+Down Arrow</span></span></td>
<td><span data-ttu-id="1a9ad-118">Avaa haku</span><span class="sxs-lookup"><span data-stu-id="1a9ad-118">Open the lookup.</span></span> <span data-ttu-id="1a9ad-119">Jos painat Alt+Alanuoli toisen kerran, kohdistus siirtyy pohjakassan segmenteihin.</span><span class="sxs-lookup"><span data-stu-id="1a9ad-119">If you press Alt+Down Arrow a second time, the focus moves to the segments in the flyout.</span></span></td>
</tr>
<tr class="even">
<td><ul>
<li><span data-ttu-id="1a9ad-120">Enter ja Shift+Enter</span><span class="sxs-lookup"><span data-stu-id="1a9ad-120">Enter and Shift+Enter</span></span></li>
<li><span data-ttu-id="1a9ad-121">Tilikartan erotin</span><span class="sxs-lookup"><span data-stu-id="1a9ad-121">Chart of accounts delimiter</span></span></li>
<li><span data-ttu-id="1a9ad-122">Oikea nuoli ja Vasen nuoli</span><span class="sxs-lookup"><span data-stu-id="1a9ad-122">Right Arrow and Left Arrow</span></span></li>
</ul></td>
<td><span data-ttu-id="1a9ad-123">Siirry seuraavaan tai edelliseen segmenttiin.</span><span class="sxs-lookup"><span data-stu-id="1a9ad-123">Move to the next or previous segment.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1a9ad-124">Välilehti</span><span class="sxs-lookup"><span data-stu-id="1a9ad-124">Tab</span></span></td>
<td><span data-ttu-id="1a9ad-125">Siirry seuraavaan kenttään ruudukossa.</span><span class="sxs-lookup"><span data-stu-id="1a9ad-125">Move to the next field in the grid.</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="1a9ad-126">Seuraavassa taulukossa kuvataan pikanäppäimiä, joita voidaan käyttää, kun haku on auki.</span><span class="sxs-lookup"><span data-stu-id="1a9ad-126">The following table describes the keyboard shortcuts that can be used when the lookup is open.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1a9ad-127">Pikanäppäin</span><span class="sxs-lookup"><span data-stu-id="1a9ad-127">Keyboard shortcut</span></span></th>
<th><span data-ttu-id="1a9ad-128">Toiminto</span><span class="sxs-lookup"><span data-stu-id="1a9ad-128">Action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1a9ad-129">Esc</span><span class="sxs-lookup"><span data-stu-id="1a9ad-129">Esc</span></span></td>
<td><span data-ttu-id="1a9ad-130">Sulje haku.</span><span class="sxs-lookup"><span data-stu-id="1a9ad-130">Close the lookup.</span></span></td>
</tr>
<tr class="even">
<td><ul>
<li><span data-ttu-id="1a9ad-131">Ylänuoli ja alanuoli</span><span class="sxs-lookup"><span data-stu-id="1a9ad-131">Up Arrow and Down Arrow</span></span></li>
<li><span data-ttu-id="1a9ad-132">Page Up ja Page Down</span><span class="sxs-lookup"><span data-stu-id="1a9ad-132">Page Up and Page Down</span></span></li>
<li><span data-ttu-id="1a9ad-133">Home ja End</span><span class="sxs-lookup"><span data-stu-id="1a9ad-133">Home and End</span></span></li>
</ul></td>
<td><span data-ttu-id="1a9ad-134">Siirry edelliseen tai seuraavaan arvoon luetteloissa, edelliseen tai seuraavaan arvoryhmään tai ensimmäiseen tai viimeiseen elementtiin haussa.</span><span class="sxs-lookup"><span data-stu-id="1a9ad-134">Move to the previous or next value in the lists, to the previous or next group of values, or to the first or last element in the lookup.</span></span></td>
</tr>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="1a9ad-135">Tilikartan erotin</span><span class="sxs-lookup"><span data-stu-id="1a9ad-135">Chart of accounts delimiter</span></span></li>
<li><span data-ttu-id="1a9ad-136">Oikea nuoli ja vasen nuoli</span><span class="sxs-lookup"><span data-stu-id="1a9ad-136">Right Arrow and Left Arrow</span></span></li>
</ul></td>
<td><span data-ttu-id="1a9ad-137">Siirry seuraavaan tai edelliseen segmenttiin.</span><span class="sxs-lookup"><span data-stu-id="1a9ad-137">Move to the next or previous segment.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1a9ad-138">Välilehti</span><span class="sxs-lookup"><span data-stu-id="1a9ad-138">Tab</span></span></td>
<td><span data-ttu-id="1a9ad-139">Siirry seuraavaan kenttään ruudukossa.</span><span class="sxs-lookup"><span data-stu-id="1a9ad-139">Move to the next field in the grid.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1a9ad-140">Alt+W</span><span class="sxs-lookup"><span data-stu-id="1a9ad-140">Alt+W</span></span></td>
<td><span data-ttu-id="1a9ad-141">Siirry <strong>Näytä kaikki</strong> ja <strong>Näytä kelvolliset</strong> -tilojen välillä.</span><span class="sxs-lookup"><span data-stu-id="1a9ad-141">Switch between <strong>Show all</strong> and <strong>Show valid</strong>.</span></span></td>
</tr>
</tbody>
</table>





