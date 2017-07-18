---
title: Projektin ostotilaukset
description: "Tässä artikkelissa kuvataan eri menetelmiä, joiden avulla voi luoda ostotilauksia projektia varten. Käytettävä menetelmä määräytyy ostotilauksen tarkoituksen, ostettujen nimikkeiden kulutusajankohdan sekä ostettujen nimikkeiden veloitusajankohdan mukaan."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 83972
ms.assetid: 247e4d72-610b-4fa5-9873-601ed0f4b2d6
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 9715d33598c0749ff1ad2523f2fa8834987998ed
ms.contentlocale: fi-fi
ms.lasthandoff: 06/13/2017

---

# <a name="purchase-orders-for-a-project"></a>Projektin ostotilaukset

[!include[banner](../includes/banner.md)]


Tässä artikkelissa kuvataan eri menetelmiä, joiden avulla voi luoda ostotilauksia projektia varten. Käytettävä menetelmä määräytyy ostotilauksen tarkoituksen, ostettujen nimikkeiden kulutusajankohdan sekä ostettujen nimikkeiden veloitusajankohdan mukaan.

Voit luoda Microsoft Dynamics 365 for Finance and Operations, Enterprise Editionissa projektin ostotilauksia monella eri tavalla. Käytettävä menetelmä määräytyy ostotilauksen tarkoituksen, ostettujen nimikkeiden kulutusajankohdan sekä ostettujen nimikkeiden veloitusajankohdan mukaan.

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




