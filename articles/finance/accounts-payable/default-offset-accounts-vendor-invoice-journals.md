---
title: Toimittajan laskujen ja laskujen hyväksynnän kirjauskansioiden oletusvastatilit
description: Tämän ohjeaiheen avulla voit päättää, mihin oletustilit ja vastatilit määritetään laskujen kirjauskansioissa.
author: abruer
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 62093
ms.assetid: 553933ca-928d-4031-bb8c-f9cff458320b
ms.search.region: global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3e67bebcfb934a3e6dae78cafd7bb2b01c05e450
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5250623"
---
# <a name="default-offset-accounts-for-vendor-invoice-and-invoice-approval-journals"></a>Toimittajan laskujen ja laskujen hyväksynnän kirjauskansioiden oletusvastatilit

[!include [banner](../includes/banner.md)]

Oletusvastatilejä käytetään seuraavilla toimittajan laskun kirjauskansion sivuilla:

-   Laskukirjauskansio
-   Hyväksyttyjen laskujen kirjauskansio

Seuraavan taulukon avulla voit päättää, mihin oletustilit ja vastatilit määritetään laskujen kirjauskansioissa.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th>Määritä oletustilit täällä</th>
<th>Missä oletustilit tarjotaan</th>
<th>Tämän asetuksen vaikutus käsittelyyn</th>
<th>Milloin asetusta tulisi käyttää</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Toimittajaryhmä</strong> – Määritä toimittajaryhmien oletusvastatilit <strong>Oletustilin määritys</strong> -sivulla, jonka voit avata <strong>Toimittajaryhmät</strong>-sivulta.</td>
<td><ul>
<li>Toimittajatili</li>
<li>Kirjauskansioviennit toimittajatileille toimittajaryhmässä, jos toimittajatileille ei ole määritetty oletustilejä</li>
</ul></td>
<td>Toimittajaryhmien oletusvastatilit näytetään toimittajien oletusvastatileinä <strong>Oletustilin määritys</strong> -sivulla. Voit avata sivun <strong>Kaikki toimittajat</strong> -luettelosivulta.</td>
<td>Käytä tätä vaihtoehtoa, jos yleensä maksat samantyyppisistä asioista samoille toimittajaryhmille ajan kuluessa.</td>
</tr>
<tr class="even">
<td><strong>Toimittajan tili</strong> – Määritä toimittajan tilien oletusvastatilit <strong>Oletustilin määritys</strong> -sivulla, jonka voit avata <strong>Toimittajat</strong>-sivulta.</td>
<td>Kirjauskansioviennit toimittajatilille</td>
<td>Toimittajatilien oletusvastatilit näytetään oletusvastatileinä toimittajatilin kirjauskansiomerkinnöille.</td>
<td>Käytä tätä vaihtoehtoa, jos yleensä maksat samantyyppisistä asioista samoille toimittajille ajan kuluessa.</td>
</tr>
<tr class="odd">
<td><strong>Kirjauskansioiden nimet</strong> – Määritä kirjauskansioiden oletusvastatilit <strong>Kirjauskansioiden nimet</strong> -sivulla. Valitse <strong>Kiinteä vastatili</strong> -asetus. Huomaa, että et voi määrittää kirjauskansioiden nimille oletusvastatilejä, jos kirjauskansioiden nimien kirjauskansiotyyppi on <strong>Laskurekisteri</strong> tai <strong>Hyväksyntä</strong>.</td>
<td><ul>
<li>Kirjauskansion otsikko, joka käyttää kirjauskansion nimeä.</li>
<li>Kirjauskansioviennit kirjauskansionimeä käyttävissä kirjauskansioissa.</li>
</ul></td>
<td>Jos <strong>Kiinteä vastatili</strong> -valintaruutu on valittuna <strong>Kirjauskansioiden nimet -sivulla</strong>, kirjauskansion nimen vastatili ohittaa toimittajan tai toimittajaryhmän oletusvastatilin.</td>
<td>Käytä tätä vaihtoehtoa kirjauskansioiden määrittämiseen tietyille kuluille tai kustannuksille, jotka veloitetaan tietyiltä tileiltä siitä riippumatta, kuka toimittaja on tai mihin toimittajaryhmään toimittaja kuuluu.</td>
</tr>
<tr class="even">
<td><strong>Kirjauskansioiden nimet</strong> – Määritä kirjauskansioiden oletusvastatilit <strong>Kirjauskansioiden nimet</strong> -sivulla. Poista <strong>Kiinteä vastatili</strong> -asetus. Huomaa, että et voi määrittää kirjauskansioiden nimille oletusvastatilejä, jos kirjauskansioiden nimien kirjauskansiotyyppi on <strong>Laskurekisteri</strong> tai <strong>Hyväksyntä</strong>.</td>
<td><ul>
<li>Kirjauskansion otsikko</li>
<li>Kirjauskansioviennit kirjauskansionimeä käyttävissä kirjauskansioissa.</li>
</ul></td>
<td>Näitä oletusarvoisia merkintöjä käytetään kirjauskansion otsikkosivuilla ja kirjauskansion otsikkosivun vastatiliä käytetään oletusmerkintänä kirjauskansion tositesivuilla. <strong>Kirjauskansioiden nimet</strong> -lomakkeen oletustilejä käytetään vain, jos toimittajan tilille ei ole määritetty oletustilejä.</td>
<td>Tätä vaihtoehtoa käyttämällä voidaan määrittää käytettävät oletustilit, kun toimittajan oletusvastatiliä ei ole määritetty.</td>
</tr>
<tr class="odd">
<td><strong>Kirjauskansion otsikko</strong> – Määritä kirjauskansion oletusvastatili käytettäväksi oletusmerkintänä kirjauskansion tositesivuilla. Huomaa, että et voi määrittää kirjauskansioiden otsikoille oletusvastatilejä, jos kirjauskansioiden nimien kirjauskansiotyyppi on <strong>Laskurekisteri</strong> tai <strong>Hyväksyntä</strong>.</td>
<td>Kirjauskansioviennit kirjauskansiossa</td>
<td>Kirjauskansion oletusvastatiliä käytetään oletusmerkintänä kirjauskansion tositesivuilla.</td>
<td>Tämän vaihtoehdon avulla voit nopeuttaa tietojen kirjaamista, jos useimmilla kirjauskansion kirjauksilla on sama vastatili.</td>
</tr>
</tbody>
</table>







[!INCLUDE[footer-include](../../includes/footer-banner.md)]