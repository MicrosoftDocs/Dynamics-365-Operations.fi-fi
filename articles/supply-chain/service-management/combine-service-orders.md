---
title: Yhdistä huoltotilaukset
description: Voit yhdistää huoltotilauksia.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 17fbed59b1fe7bec80f25f74451872efd61bed62
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4426861"
---
# <a name="combine-service-orders"></a>Yhdistä huoltotilaukset   

[!include [banner](../includes/banner.md)]


Kun luot huoltotilausrivejä automaattisesti **Huoltosopimukset**-lomakkeessa, voit valita jonkin seuraavista vaihtoehdoista määrittääksesi, miten haluat ryhmitellä ne:

  - **Huoltosopimuksen mukaan**

  - **Huoltotehtävän mukaan**

  - **Työntekijän mukaan**

  - **Huoltokohteen mukaan**

## <a name="example"></a>Esimerkki

Luot huoltosopimuksen alkamispäivämäärällä 31.3.2007. Valitset **Yhdistä huoltotilaukset** -kentässä **Huoltokohteen mukaan**. Sitten luot seuraavat huoltosopimusrivit:

<table style="width:100%;">
<colgroup>
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Sopimusrivin numero</p></th>
<th><p>Tapahtumalaji</p></th>
<th><p>kuvaus</p></th>
<th><p>Väli</p></th>
<th><p>Huoltokohde</p></th>
<th><p>Aloituspäivämäärä</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>1</p></td>
<td><p><strong>Tunti</strong></p></td>
<td><p>SAL1</p></td>
<td><p>Viikoittain</p></td>
<td><p>X-1</p></td>
<td><p>1.4.2007</p></td>
</tr>
<tr class="even">
<td><p>2</p></td>
<td><p><strong>Tunti</strong></p></td>
<td><p>SAL2</p></td>
<td><p>Kaksi kertaa viikossa</p></td>
<td><p>X-2</p></td>
<td><p>1.4.2007</p></td>
</tr>
<tr class="odd">
<td><p>3</p></td>
<td><p><strong>Tunti</strong></p></td>
<td><p>SAL3</p></td>
<td><p>Viikoittain</p></td>
<td><p>X-2</p></td>
<td><p>1.4.2007</p></td>
</tr>
</tbody>
</table>


Et määritä yhdellekään huoltosopimusriville aikaikkunaa. Sen vuoksi huoltotilausrivejä ei siirretä niiden laskentapäivästä.

Tämän jälkeen luot **Luo huoltotilauksia** -lomakkeessa huoltotilausrivit 1.4. - 30.4.2007 väliselle ajalle.

Luotavien huoltotilausten määrä on 10. Koska valitsemasi yhdistetty asetus oli **Huoltokohteen mukaan**, kaikilla luoduilla huoltotilauksilla on vain sellaisia huoltotilausrivejä, joilla on yksi tietty huoltokohde. Huoltosopimuksesta luotavat huoltotilausrivit, joilla on sama huoltopäivämäärä ja sama kohde, yhdistetään samaan huoltotilaukseen.


> [!NOTE]
> <P>Tässä esimerkissä <STRONG>Huoltoparametrit</STRONG>-lomakkeessa määritetyllä kalenterilla ei ole suljettuja päiviä.</P>



Huoltotilausrivien lisäryhmittely huoltotilauksiin tapahtuu huoltosopimusriveillä määrittämiesi aikaikkunoiden mukaan.

## <a name="see-also"></a>Lisätietoja

[Automaattisesti luodut huoltotilaukset](create-service-orders-automatically.md)

  


