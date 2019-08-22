---
title: Projektin ostotilaukset
description: Tässä artikkelissa kuvataan eri menetelmiä, joiden avulla voi luoda ostotilauksia projektia varten. Käytettävä menetelmä määräytyy ostotilauksen tarkoituksen, ostettujen nimikkeiden kulutusajankohdan sekä ostettujen nimikkeiden veloitusajankohdan mukaan.
author: KimANelson
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 83972
ms.assetid: 247e4d72-610b-4fa5-9873-601ed0f4b2d6
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 971a4ea0abac43c160d8a6f46f385cbfc5134ffd
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/01/2019
ms.locfileid: "1838868"
---
# <a name="purchase-orders-for-a-project"></a>Projektin ostotilaukset

[!include [banner](../includes/banner.md)]

Tässä artikkelissa kuvataan eri menetelmiä, joiden avulla voi luoda ostotilauksia projektia varten. Käytettävä menetelmä määräytyy ostotilauksen tarkoituksen, ostettujen nimikkeiden kulutusajankohdan sekä ostettujen nimikkeiden veloitusajankohdan mukaan.

Voit luoda Microsoft Dynamics 365 for Finance and Operationsissa projektin ostotilauksia monella eri tavalla. Käytettävä menetelmä määräytyy ostotilauksen tarkoituksen, ostettujen nimikkeiden kulutusajankohdan sekä ostettujen nimikkeiden veloitusajankohdan mukaan.

### <a name="methods-for-creating-a-purchase-order"></a>Menetelmät ostotilauksen luomiseksi

Voit luoda ostotilauksen projektinhallinnassa ja kirjanpidossa käyttämällä jotakin seuraavista menetelmistä. Ostotilauksen tarkoitus määrittää ostotilauksen kulutusajankohdan ja tämän vuoksi myös sen, milloin nimikkeet veloitetaan projektissa.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Tapa</th>
<th>Tarkoitus</th>
<th>Nimikkeiden kulutus</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Luo ostotilaus suoraan projektista.</td>
<td>Tällä menetelmällä voit ostaa nimikkeitä ulkopuoliselta toimittajalta projektissa käytettäväksi. Voit luoda ostotilauksen kahdella tavalla:
<ul>
<li>Itse projektista. Tässä tapauksessa projekti on jo määritetty ostotilaukselle.</li>
<li>Siirtymällä projektin ostotilaukseen. Tällöin on valittava sekä toimittaja että projekti, jolle ostotilaus luodaan.</li>
</ul></td>
<td>Nimikkeet kulutetaan, kun toimittajalasku päivitetään.</td>
</tr>
<tr class="even">
<td>Ostotilauksen luominen myyntitilauksesta</td>
<td>Käytä tätä menetelmää nimikkeiden ostamiseen, kun projektista luodaan myyntitilaus.</td>
<td>Nimikkeet kulutetaan, kun myyntitilaus laskutetaan asiakkaalta.</td>
</tr>
<tr class="odd">
<td>Ostotilauksen luominen nimiketarpeen perusteella</td>
<td>Käytä tätä menetelmää nimikkeiden ostamiseen, kun luot projektista nimiketarpeen.</td>
<td>Nimikkeet kulutetaan, kun nimiketarpeen pakkausluettelo päivitetään.</td>
</tr>
</tbody>
</table>

> [!NOTE] 
> Kun toimittajalasku tai pakkausluettelo päivitetään, ohjelma pyytää päivittämään nimiketarpeen pakkausluettelon.

Lisätietoja on ohjeaiheessa [Ostotilauksen nimikkeiden vastaanotto nimiketarpeen perusteella](tasks/receive-items-purchase-order-item-requirement.md).

