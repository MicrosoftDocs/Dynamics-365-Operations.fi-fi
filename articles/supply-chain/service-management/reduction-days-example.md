---
title: "Esimerkki vähennyspäivistä"
description: "Esimerkki vähennyspäivistä."
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMASubscriptionTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 69e4b1b0fe100b17e5b2c59be81604019347956f
ms.contentlocale: fi-fi
ms.lasthandoff: 05/08/2018

---


# <a name="reduction-days-example"></a>Esimerkki vähennyspäivistä 

[!include [banner](../includes/banner.md)]


Olet luonut asiakkaan ylläpitosopimukselle ylläpitosopimustapahtuman seuraavassa taulukossa esitetyllä tavalla.

<table>
<colgroup>
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
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
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
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

  



