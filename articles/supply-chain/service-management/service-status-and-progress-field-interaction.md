---
title: Huollon tilan ja edistymisen kenttien vuorovaikutus
description: Huoltotilaukset-lomakkeessa huoltotilauksen otsikon Edistyminen-kenttä ilmaisee koko huoltotilauksen tilan ja Tila-kenttä yksittäisen huoltotilausrivin tilan.
author: sorenva
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0e83df9ca8ee19b5e29d4eccf2bd883ee6ddff62
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/03/2022
ms.locfileid: "8677643"
---
# <a name="service-status-and-progress-field-interaction"></a>Huollon tilan ja edistymisen kenttien vuorovaikutus

[!include [banner](../includes/banner.md)]

**Huoltotilaukset**-lomakkeessa huoltotilauksen otsikon **Edistyminen**-kenttä ilmaisee koko huoltotilauksen tilan ja **Tila**-kenttä yksittäisen huoltotilausrivin tilan.

<table>
<colgroup>
<col />
<col />
<col />
<col />
</colgroup>
<thead>
<tr class="header">
<th><p>Tila</p></th>
<th><p>Rivin 1 tila</p></th>
<th><p>Rivin 2 tila</p></th>
<th><p>Rivin 3 tila</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Käsittelyssä</strong></p></td>
<td><p><strong>Luotu</strong></p></td>
<td><p><strong>Luotu</strong></p></td>
<td><p><strong>Luotu</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>Käsittelyssä</strong></p></td>
<td><p><strong>Peruutettu</strong></p></td>
<td><p><strong>Luotu</strong></p></td>
<td><p><strong>Luotu</strong></p></td>
</tr>
<tr class="odd">
<td><p><strong>Käsittelyssä</strong></p></td>
<td><p><strong>Luotu</strong></p></td>
<td><p><strong>Peruutettu</strong></p></td>
<td><p><strong>Kirjattu</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>Peruutettu</strong></p></td>
<td><p><strong>Peruutettu</strong></p></td>
<td><p><strong>Peruutettu</strong></p></td>
<td><p><strong>Peruutettu</strong></p></td>
</tr>
<tr class="odd">
<td><p><strong>Kirjattu</strong></p></td>
<td><p><strong>Kirjattu</strong></p></td>
<td><p><strong>Kirjattu</strong></p></td>
<td><p><strong>Kirjattu</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>Kirjattu</strong></p></td>
<td><p><strong>Kirjattu</strong></p></td>
<td><p><strong>Peruutettu</strong></p></td>
<td><p><strong>Peruutettu</strong></p></td>
</tr>
</tbody>
</table>

Huoltotilauksen käsittely on meneillään, jos kaikkien rivien tilana on **Luotu**. Käsittely on meneillään myös silloin, jos joidenkin rivien tilana on **Peruutettu** tai **Kirjattu**.

Jos huoltotilauksen kaikkien rivien tilana on **Kirjattu**, huoltotilauksen tilana on **Kirjattu**. Jos joidenkin rivien tilana on **Kirjattu** ja joidenkin **Peruutettu**, koko tilauksen tilana on edelleen **Kirjattu**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
