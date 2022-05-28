---
title: Esimerkki vähennyspäivistä
description: Esimerkki vähennyspäivistä.
author: sorenva
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMASubscriptionTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 85e588273244c88ffa208e88b66800dc7ce20d68
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/03/2022
ms.locfileid: "8674810"
---
# <a name="reduction-days-example"></a>Esimerkki vähennyspäivistä

[!include [banner](../includes/banner.md)]

Olet luonut asiakkaan ylläpitosopimukselle ylläpitosopimustapahtuman seuraavassa taulukossa esitetyllä tavalla.

<table>
<colgroup>
<col />
<col />
<col />
<col />
<col />
<col />
<col />
<col />
</colgroup>
<thead>
<tr class="header">
<th><p>Päivämäärästä</p></th>
<th><p>Päivämäärään</p></th>
<th><p>Ylläpitosopimus</p></th>
<th><p>Ylläpitosopimustyyppi</p></th>
<th><p>Project</p></th>
<th><p>Luokka</p></th>
<th><p>Myyntivaluutta</p></th>
<th><p>Myyntihinta</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>01. maaliskuuta 2011</p></td>
<td><p>31. maaliskuuta 2011</p></td>
<td><p>NR-2</p></td>
<td><p><strong>Säännöllinen</strong></p></td>
<td><p>9013</p></td>
<td><p>SubCat2</p></td>
<td><p>Euro</p></td>
<td><p>200,00</p></td>
</tr>
</tbody>
</table>

Asiakas raportoi, että hän ei tarvitse huollon kattavuutta kahden päivän aikana (maaliskuun 10. ja 11. päivänä). Suostut pienentämään ylläpitosopimusta näiden kahden päivän aikana.

Luot uuden **Vähennyspäivät**-tyyppisen tapahtuman seuraavassa taulukossa esitetyllä tavalla.

<table>
<colgroup>
<col />
<col />
<col />
<col />
<col />
<col />
<col />
<col />
</colgroup>
<thead>
<tr class="header">
<th><p>Päivämäärästä</p></th>
<th><p>Päivämäärään</p></th>
<th><p>Ylläpitosopimus</p></th>
<th><p>Ylläpitosopimustyyppi</p></th>
<th><p>Project</p></th>
<th><p>Luokka</p></th>
<th><p>Myyntivaluutta</p></th>
<th><p>Myyntihinta</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>10. maaliskuuta 2011</p></td>
<td><p>11. maaliskuuta 2011</p></td>
<td><p>NR-2</p></td>
<td><p><strong>Vähennyspäivät</strong></p></td>
<td><p>9013</p></td>
<td><p>SubCat2</p></td>
<td><p>Euro</p></td>
<td><p>-12,90</p></td>
</tr>
</tbody>
</table>

Kun maaliskuun 2011 tapahtumat laskutetaan, 200 euron myyntihinnasta vähennetään 12,90 euroa. Ylläpitosopimustapahtuman veloitettava summa on siis 187,10 euroa, ja kaksi tapahtumaa laskutetaan yhteissummalla 187,10 euroa.

## <a name="see-also"></a>Lisätietoja

[Ylläpitosopimusmaksujen päivien vähentäminen](reduce-the-days-on-subscription-fees.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]