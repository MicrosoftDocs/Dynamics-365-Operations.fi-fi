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
ms.reviewer: roschlom
ms.custom: 14071
ms.assetid: e6fce826-c403-4d91-a78b-e9a58c44ac03
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e1e35f5fb4400f849e9a139e1a96b18e8b9df384
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4968776"
---
# <a name="enter-account-and-dimension-combinations-segmented-entry-control"></a><span data-ttu-id="ac47c-104">Kirjoita tilien ja dimensioiden yhdistelmät (komponentin segmentoidun tarkistus)</span><span class="sxs-lookup"><span data-stu-id="ac47c-104">Enter account and dimension combinations (segmented entry control)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ac47c-105">Tässä artikkelissa kerrotaan, miten tili- ja dimensioyhdistelmiä tai kirjanpitotilejä kirjataan.</span><span class="sxs-lookup"><span data-stu-id="ac47c-105">This article describes how to enter account and dimension combinations or ledger accounts.</span></span> <span data-ttu-id="ac47c-106">Kirjauskokokemusta sanotaan usein segmentoidun kirjauksen hallinnaksi.</span><span class="sxs-lookup"><span data-stu-id="ac47c-106">The entry experience is often referred to as segmented entry control.</span></span>

<span data-ttu-id="ac47c-107">Käyttäjät syöttävät tilien ja dimensioiden yhdistelmät eri sivuille, kuten kirjauskansioiden sivuille, budjetointiin ja kirjausmääritelmiin.</span><span class="sxs-lookup"><span data-stu-id="ac47c-107">Users enter account and dimension combinations on various pages, such as pages for general journals, budgeting, and posting definitions.</span></span> <span data-ttu-id="ac47c-108">Voimassaolevat tili- ja dimensioyhdistelmät riippuvat tilirakenteista, jotka on määritetty kirjanpidossa ja kehittyneistä säännöistä, jotka on määritetty tilirakenteisiin.</span><span class="sxs-lookup"><span data-stu-id="ac47c-108">The valid account and dimension combinations depend on the account structures that are assigned to the ledger and the advanced rules that are assigned to the account structures.</span></span> <span data-ttu-id="ac47c-109">Kun käyttäjät syöttävät yhdistelmän, he voivat joko syöttää arvot manuaalisesti tai hyödyntää syvää hakukokemusta.</span><span class="sxs-lookup"><span data-stu-id="ac47c-109">When users enter a combination, they can either manually type the values or take advantage of a rich, lookup experience.</span></span> <span data-ttu-id="ac47c-110">Kun syötät kenttään, voit aloittaa kirjoittamisen ja se etsii arvon ja kuvauksen.</span><span class="sxs-lookup"><span data-stu-id="ac47c-110">When you enter the field, you can start to type and it will search the value and the description.</span></span> <span data-ttu-id="ac47c-111">Esimerkiksi jos kirjoitat "180", se etsii kaikki arvot, jotka alkavat kyseisellä numerolla.</span><span class="sxs-lookup"><span data-stu-id="ac47c-111">For example, if you type 180 it will search any value that begins with that number combination.</span></span> <span data-ttu-id="ac47c-112">Tai voit kirjoittaa "Maksu", ja se etsii kaikki arvot, joilla on kuvaus, joka alkaa merkkijonolla Maksu.</span><span class="sxs-lookup"><span data-stu-id="ac47c-112">Or you may type Cash and it will search any value that has a description that begins with Cash.</span></span> <span data-ttu-id="ac47c-113">Voit käyttää myös yleismerkkejä, kuten \*Maksu tai \*180, etsimiseen, jos arvo tai kuvaus sisältää hakuehdon.</span><span class="sxs-lookup"><span data-stu-id="ac47c-113">You can also use a wildcard, such as \*Cash or \*180 to search if the value or description contain the search criteria.</span></span> 

<span data-ttu-id="ac47c-114">Seuraavassa taulukossa kuvataan pikanäppäimiä, joita voidaan käyttää, kun haku on suljettu.</span><span class="sxs-lookup"><span data-stu-id="ac47c-114">The following table describes the keyboard shortcuts that can be used when the lookup is closed.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ac47c-115">Pikanäppäin</span><span class="sxs-lookup"><span data-stu-id="ac47c-115">Keyboard shortcut</span></span></th>
<th><span data-ttu-id="ac47c-116">Toiminto</span><span class="sxs-lookup"><span data-stu-id="ac47c-116">Action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ac47c-117">Alt+Alanuoli</span><span class="sxs-lookup"><span data-stu-id="ac47c-117">Alt+Down Arrow</span></span></td>
<td><span data-ttu-id="ac47c-118">Avaa haku</span><span class="sxs-lookup"><span data-stu-id="ac47c-118">Open the lookup.</span></span> <span data-ttu-id="ac47c-119">Jos painat Alt+Alanuoli toisen kerran, kohdistus siirtyy pohjakassan segmenteihin.</span><span class="sxs-lookup"><span data-stu-id="ac47c-119">If you press Alt+Down Arrow a second time, the focus moves to the segments in the flyout.</span></span></td>
</tr>
<tr class="even">
<td><ul>
<li><span data-ttu-id="ac47c-120">Enter ja Shift+Enter</span><span class="sxs-lookup"><span data-stu-id="ac47c-120">Enter and Shift+Enter</span></span></li>
<li><span data-ttu-id="ac47c-121">Tilikartan erotin</span><span class="sxs-lookup"><span data-stu-id="ac47c-121">Chart of accounts delimiter</span></span></li>
<li><span data-ttu-id="ac47c-122">Oikea nuoli ja Vasen nuoli</span><span class="sxs-lookup"><span data-stu-id="ac47c-122">Right Arrow and Left Arrow</span></span></li>
</ul></td>
<td><span data-ttu-id="ac47c-123">Siirry seuraavaan tai edelliseen segmenttiin.</span><span class="sxs-lookup"><span data-stu-id="ac47c-123">Move to the next or previous segment.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ac47c-124">Välilehti</span><span class="sxs-lookup"><span data-stu-id="ac47c-124">Tab</span></span></td>
<td><span data-ttu-id="ac47c-125">Siirry seuraavaan kenttään ruudukossa.</span><span class="sxs-lookup"><span data-stu-id="ac47c-125">Move to the next field in the grid.</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="ac47c-126">Seuraavassa taulukossa kuvataan pikanäppäimiä, joita voidaan käyttää, kun haku on auki.</span><span class="sxs-lookup"><span data-stu-id="ac47c-126">The following table describes the keyboard shortcuts that can be used when the lookup is open.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ac47c-127">Pikanäppäin</span><span class="sxs-lookup"><span data-stu-id="ac47c-127">Keyboard shortcut</span></span></th>
<th><span data-ttu-id="ac47c-128">Toiminto</span><span class="sxs-lookup"><span data-stu-id="ac47c-128">Action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ac47c-129">Esc</span><span class="sxs-lookup"><span data-stu-id="ac47c-129">Esc</span></span></td>
<td><span data-ttu-id="ac47c-130">Sulje haku.</span><span class="sxs-lookup"><span data-stu-id="ac47c-130">Close the lookup.</span></span></td>
</tr>
<tr class="even">
<td><ul>
<li><span data-ttu-id="ac47c-131">Ylänuoli ja alanuoli</span><span class="sxs-lookup"><span data-stu-id="ac47c-131">Up Arrow and Down Arrow</span></span></li>
<li><span data-ttu-id="ac47c-132">Page Up ja Page Down</span><span class="sxs-lookup"><span data-stu-id="ac47c-132">Page Up and Page Down</span></span></li>
<li><span data-ttu-id="ac47c-133">Home ja End</span><span class="sxs-lookup"><span data-stu-id="ac47c-133">Home and End</span></span></li>
</ul></td>
<td><span data-ttu-id="ac47c-134">Siirry edelliseen tai seuraavaan arvoon luetteloissa, edelliseen tai seuraavaan arvoryhmään tai ensimmäiseen tai viimeiseen elementtiin haussa.</span><span class="sxs-lookup"><span data-stu-id="ac47c-134">Move to the previous or next value in the lists, to the previous or next group of values, or to the first or last element in the lookup.</span></span></td>
</tr>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="ac47c-135">Tilikartan erotin</span><span class="sxs-lookup"><span data-stu-id="ac47c-135">Chart of accounts delimiter</span></span></li>
<li><span data-ttu-id="ac47c-136">Oikea nuoli ja vasen nuoli</span><span class="sxs-lookup"><span data-stu-id="ac47c-136">Right Arrow and Left Arrow</span></span></li>
</ul></td>
<td><span data-ttu-id="ac47c-137">Siirry seuraavaan tai edelliseen segmenttiin.</span><span class="sxs-lookup"><span data-stu-id="ac47c-137">Move to the next or previous segment.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ac47c-138">Välilehti</span><span class="sxs-lookup"><span data-stu-id="ac47c-138">Tab</span></span></td>
<td><span data-ttu-id="ac47c-139">Siirry seuraavaan kenttään ruudukossa.</span><span class="sxs-lookup"><span data-stu-id="ac47c-139">Move to the next field in the grid.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ac47c-140">Alt+W</span><span class="sxs-lookup"><span data-stu-id="ac47c-140">Alt+W</span></span></td>
<td><span data-ttu-id="ac47c-141">Siirry <strong>Näytä kaikki</strong> ja <strong>Näytä kelvolliset</strong> -tilojen välillä.</span><span class="sxs-lookup"><span data-stu-id="ac47c-141">Switch between <strong>Show all</strong> and <strong>Show valid</strong>.</span></span></td>
</tr>
</tbody>
</table>





