---
title: Varasto-objektin arvot
description: Tässä artikkelissa on tietoja siitä, miten varasto-objektien arvot lasketaan.
author: AndersGirke
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventCostOnhandItem
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19111
ms.assetid: 56a7c8ba-bf4a-4b1d-918d-56bb96926c4f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6564df5bd9c768f647138714875c60ddd6df3c85
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/29/2021
ms.locfileid: "7568948"
---
# <a name="inventory-object-values"></a>Varasto-objektin arvot

[!include [banner](../includes/banner.md)]

Tässä artikkelissa on tietoja siitä, miten varasto-objektien arvot lasketaan. 

**Fyysinen määrä**-nimisen uuden toiminnon avulla näet tietyn varasto-objektin arvot. 

Kustannusobjekti edustaa sen yksikön tasoa, jolla varaston kirjanpito suoritetaan. Lisätietoja kustannusobjekteista on kohdassa [Kustannusobjektit](cost-object.md). 

Saat tietyn varasto-objektin arvot näkyviin valitsemalla **Fyysinen määrä** **Kustannusobjekti** -sivulla. Varasto-objektin arvo lasketaan seuraavasti: 

Varasto-objekti.Arvo = Kustannusobjekti.Keskimääräinen yksikkökustannus × Varasto-objekti.Määrä 

Seuraavassa esimerkissä näytetään, miten varasto-objektin ja kustannusobjektin arvot lasketaan. Nimikkeelle A on rekisteröity kaksi tuotteen vastaanottotapahtumaa.

-   Tuotteen vastaanotto 1: määrä = 100 kpl, summa = 1 000,00 €, toimipaikka = 1, varasto =11, eränumero = B1
-   Tuotteen vastaanotto 2: määrä = 50 kpl, summa = 800,00 €, toimipaikka = 1, varasto =11, eränumero = B2

Seuraava taulukko sisältää kustannusobjektin laskennan tulokset. Voit tarkastella tuloksia **Kustannusobjekti**-sivulla.

<table>
<colgroup>
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
</colgroup>
<thead>
<tr class="header">
<th>Objektityyppi</th>
<th>Nimiketunnus</th>
<th>Sivusto</th>
<th>Määrä</th>
<th>Varastoyksikkö</th>
<th>Arvo</th>
<th>Keskimääräinen yksikkökustannus</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Kustannusobjekti</td>
<td>A</td>
<td>1</td>
<td>150</td>
<td>Kpl.</td>
<td><p>1 800,00 €</p></td>
<td><p>12,00 €</p></td>
</tr>
</tbody>
</table>

Seuraava taulukko sisältää varasto-objektin laskennan tulokset. Voit tarkastella tuloksia valitsemalla **Kustannusobjekti**-sivun **Fyysinen määrä** -kohdan.

<table>
<colgroup>
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
</colgroup>
<thead>
<tr class="header">
<th>Objektityyppi</th>
<th>Nimiketunnus</th>
<th>Sivusto</th>
<th>Varasto</th>
<th>Eränumero.</th>
<th>Määrä</th>
<th>Varastoyksikkö</th>
<th>Arvo</th>
<th>Keskimääräinen yksikkökustannus</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Varasto-objekti</td>
<td>A</td>
<td>1</td>
<td>11</td>
<td>B1</td>
<td>100</td>
<td>Kpl.</td>
<td><p>1 200,00 €</p></td>
<td><p>12,00 €</p></td>
</tr>
<tr class="even">
<td>Varasto-objekti</td>
<td>A</td>
<td>1</td>
<td>11</td>
<td>B2</td>
<td>50</td>
<td>Kpl.</td>
<td><p>600,00 €</p></td>
<td><p>12,00 €</p></td>
</tr>
</tbody>
</table>



## <a name="additional-resources"></a>Lisäresurssit

[Kustannusobjektit](cost-object.md)

[Kustannusmerkinnät](cost-entries.md)

[Uudet ja muuttuneet ominaisuudet](../../fin-ops-core/fin-ops/get-started/whats-new-changed.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]