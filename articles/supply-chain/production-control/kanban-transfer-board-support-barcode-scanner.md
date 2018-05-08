---
title: Kanban-siirron taulun tuki viivakoodinlukijoille
description: "Kanban-siirron taulu tukee skannerin toimia aina pienoisohjelman viivakoodiskannerista kanban-työn valitsemiseen, käynnistämiseen, päättämiseen ja tyhjentämiseen."
author: ChristianRytt
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: KanbanBoardTransferJob
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 19391
ms.assetid: a426f645-d59b-4c98-8d78-eba8d64a562e
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: a8393efd51032271d3023f1e0569425a16222cc3
ms.contentlocale: fi-fi
ms.lasthandoff: 11/03/2017

---

# <a name="kanban-transfer-board-support-for-barcode-scanners"></a>Kanban-siirron taulun tuki viivakoodinlukijoille

[!include [banner](../includes/banner.md)]

Kanban-siirron taulu tukee skannerin toimia aina pienoisohjelman viivakoodiskannerista kanban-työn valitsemiseen, käynnistämiseen, päättämiseen ja tyhjentämiseen.

<a name="registration-modes"></a>Rekisteröintitilat
------------------

**Skannerin rekisteröinti** -pikavälilehdessä voit valita rekisteröintitilan, joka ohjaa toimintoa, kun skannaat kanban-kortin numeron tai kirjoitat numeron manuaalisesti Kanban-kortin numero -kenttään.

| Määritä rekisteröintitila | Kuvaus                                                                                     |
|-----------------------|-------------------------------------------------------------------------------------------------|
| Aloitus                 | Rekisteröi Kanban-siirtotyön käsittelyssä olevaksi.                                                 |
| Täydellinen              | Rekisteröi Kanban-siirtotyön valmiiksi.                                                   |
| Tyhjä                 | Rekisteröi materiaalia käsittelevän yksikön, johon Kanban-kortti viittaa, tyhjäksi.              |
| Valitse                | Rekisteröi Kanban-kortin numeron ja valitsee viitatun työn automaattisesti Kanban-luettelosta. |

 
<a name="registration-mode-select"></a>Rekisteröintitilan valinta
------------------------

Kun käytät viivakoodinlukijaa työn valintaan, kanban-taulun näyttötila muuttuu. Tässä tilassa seuraavien ehtojen on täytyttävä:

-   Vain skannattu kanban-työ tulee näkyviin.
-   Valitun tehtävän tiedot näkyvät **Tiedot**-pikavälilehdessä.
-   **Sanomat**-pikavälilehdessä näkyvät vain valitun työn sanomat.
-   Voit muuttaa työn tilaa toimintoruudun toiminnoilla. Kanban-siirron taulussa näkyy edelleen vain yksi työ.
-   Voit päivittää tiedot työluetteloon manuaalisesti valitsemalla **Päivitä** (Vaihto+F5) toimintoruudussa. Kun olet päivittänyt tiedot, työn suodattimen kaikki tulokset näytetään uudelleen.

## <a name="job-status-and-possible-actions"></a>Työn tila ja mahdolliset toiminnot
Valitun työn tila sekä tapahtumien kanbanien tarvekohdistettujen töiden tila määrittävät, voidaanko työtä käsitellä lisää. Seuraavassa taulukossa on tietoja näistä tiloista ja tehtävistä:
-   Töille tai niiden viittaamille käsittely-yksiköille valittavissa olevat tilat.
-   Työlle suoritettavissa olevat tehtävät.

<table>
<colgroup>
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
</colgroup>
<thead>
<tr class="header">
<th>Työlaji</th>
<th>Työn tila tai käsittely-yksikön tila</th>
<th>Päivitä keräysluettelo</th>
<th>Aloitus</th>
<th>Päivitä rekisteröinti</th>
<th>Täydellinen</th>
<th>Tyhjä</th>
<th>Luo tapahtuma-kanbaneita</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Varastosiirto</td>
<td><ul>
<li>Ei suunniteltu</li>
<li>Ei tarvekohdistettuja töitä, tai tarvekohdistetut työt on suoritettu</li>
</ul></td>
<td>Kyllä</td>
<td>Kyllä</td>
<td>Kyllä</td>
<td>Kyllä</td>
<td>Ei</td>
<td>Kyllä</td>
</tr>
<tr class="even">
<td>Varastosiirto</td>
<td><ul>
<li>Ei suunniteltu</li>
<li>Tarvekohdistettu työ on kesken</li>
</ul></td>
<td>Kyllä</td>
<td>Ei</td>
<td>Kyllä</td>
<td>Ei</td>
<td>Ei</td>
<td>Ei</td>
</tr>
<tr class="odd">
<td>Varastosiirto</td>
<td>Käsittelyssä</td>
<td>Kyllä</td>
<td>Ei</td>
<td>Kyllä</td>
<td>Kyllä</td>
<td>Ei</td>
<td>Ei</td>
</tr>
<tr class="even">
<td>Varastosiirto</td>
<td>Valmis</td>
<td>Ei</td>
<td>Ei</td>
<td>Ei</td>
<td>Ei</td>
<td>Kyllä</td>
<td>Ei</td>
</tr>
<tr class="odd">
<td>Siirto tai käsittely</td>
<td>Tyhjä</td>
<td>Ei</td>
<td>Ei</td>
<td>Ei</td>
<td>Ei</td>
<td>Ei</td>
<td>Ei</td>
</tr>
<tr class="even">
<td>Siirto tai käsittely</td>
<td>Kanban-korttia ei löydy</td>
<td>Ei</td>
<td>Ei</td>
<td>Ei</td>
<td>Ei</td>
<td>Ei</td>
<td>Ei</td>
</tr>
<tr class="odd">
<td>Siirto tai käsittely</td>
<td>Kanban-kortti löytyy, mutta sitä ei ole liitetty kanbaniin</td>
<td>Ei</td>
<td>Ei</td>
<td>Ei</td>
<td>Ei</td>
<td>Ei</td>
<td>Ei</td>
</tr>
<tr class="even">
<td>Prosessoi</td>
<td><ul>
<li>Ei suunniteltu</li>
<li>Valmisteltu</li>
<li>Käsittelyssä</li>
</ul></td>
<td>Ei</td>
<td>Ei</td>
<td>Ei</td>
<td>Ei</td>
<td>Ei</td>
<td>Ei</td>
</tr>
<tr class="odd">
<td>Prosessoi</td>
<td>Valmis</td>
<td>Ei</td>
<td>Ei</td>
<td>Ei</td>
<td>Ei</td>
<td>Ei</td>
<td>Ei</td>
</tr>
</tbody>
</table>






