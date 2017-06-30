---
title: "Kirjoita tilien ja dimensioiden yhdistelmät (komponentin segmentoidun tarkistus)"
description: "Tässä artikkelissa kerrotaan, miten tili- ja dimensioyhdistelmiä tai kirjanpitotilejä kirjataan. Kirjauskokokemusta sanotaan usein segmentoidun kirjauksen hallinnaksi."
author: RobinARH
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 14071
ms.assetid: e6fce826-c403-4d91-a78b-e9a58c44ac03
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 1535ef5c5eec1389272ce8fd2c2c183f532785b1
ms.contentlocale: fi-fi
ms.lasthandoff: 05/25/2017


---

# <a name="enter-account-and-dimension-combinations-segmented-entry-control"></a>Kirjoita tilien ja dimensioiden yhdistelmät (komponentin segmentoidun tarkistus)

[!include[banner](../includes/banner.md)]


Tässä artikkelissa kerrotaan, miten tili- ja dimensioyhdistelmiä tai kirjanpitotilejä kirjataan. Kirjauskokokemusta sanotaan usein segmentoidun kirjauksen hallinnaksi.

Käyttäjät syöttävät tilien ja dimensioiden yhdistelmät eri sivuille, kuten kirjauskansioiden sivuille, budjetointiin ja kirjausmääritelmiin. Voimassaolevat tili- ja dimensioyhdistelmät riippuvat tilirakenteista, jotka on määritetty kirjanpidossa ja kehittyneistä säännöistä, jotka on määritetty tilirakenteisiin. Kun käyttäjät syöttävät yhdistelmän, he voivat joko syöttää arvot manuaalisesti tai hyödyntää syvää hakukokemusta. Kun syötät kenttään, voit aloittaa kirjoittamisen ja se etsii arvon ja kuvauksen. Esimerkiksi jos kirjoitat "180", se etsii kaikki arvot, jotka alkavat kyseisellä numerolla. Tai voit kirjoittaa "Maksu", ja se etsii kaikki arvot, joilla on kuvaus, joka alkaa merkkijonolla Maksu. Voit käyttää myös yleismerkkejä, kuten \*Maksu tai \*180, etsimiseen, jos arvo tai kuvaus sisältää hakuehdon. 

Seuraavassa taulukossa kuvataan pikanäppäimiä, joita voidaan käyttää, kun haku on suljettu.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Pikanäppäin</th>
<th>Toiminto</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Alt+Alanuoli</td>
<td>Avaa haku Jos painat Alt+Alanuoli toisen kerran, kohdistus siirtyy pohjakassan segmenteihin.</td>
</tr>
<tr class="even">
<td><ul>
<li>Enter ja Shift+Enter</li>
<li>Tilikartan erotin</li>
<li>Oikea nuoli ja Vasen nuoli</li>
</ul></td>
<td>Siirry seuraavaan tai edelliseen segmenttiin.</td>
</tr>
<tr class="odd">
<td>Välilehti</td>
<td>Siirry seuraavaan kenttään ruudukossa.</td>
</tr>
</tbody>
</table>

Seuraavassa taulukossa kuvataan pikanäppäimiä, joita voidaan käyttää, kun haku on auki.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Pikanäppäin</th>
<th>Toiminto</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Esc</td>
<td>Sulje haku.</td>
</tr>
<tr class="even">
<td><ul>
<li>Ylänuoli ja alanuoli</li>
<li>Page Up ja Page Down</li>
<li>Home ja End</li>
</ul></td>
<td>Siirry edelliseen tai seuraavaan arvoon luetteloissa, edelliseen tai seuraavaan arvoryhmään tai ensimmäiseen tai viimeiseen elementtiin haussa.</td>
</tr>
<tr class="odd">
<td><ul>
<li>Tilikartan erotin</li>
<li>Oikea nuoli ja vasen nuoli</li>
</ul></td>
<td>Siirry seuraavaan tai edelliseen segmenttiin.</td>
</tr>
<tr class="even">
<td>Välilehti</td>
<td>Siirry seuraavaan kenttään ruudukossa.</td>
</tr>
<tr class="odd">
<td>Alt+W</td>
<td>Siirry <strong>Näytä kaikki</strong> ja <strong>Näytä kelvolliset</strong> -tilojen välillä.</td>
</tr>
</tbody>
</table>

 




