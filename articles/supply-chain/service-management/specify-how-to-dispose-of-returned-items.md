---
title: "Palautettujen nimikkeiden poistotavan määrittäminen"
description: "Palautettujen nimikkeiden poistotavan määrittäminen."
author: ShylaThompson
manager: AnnBe
ms.date: 05/07/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventQuarantineOrder
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
ms.openlocfilehash: d25a53ac58b0ab44605af253f174ba2ec7b74174
ms.contentlocale: fi-fi
ms.lasthandoff: 05/08/2018

---

# <a name="specify-how-to-dispose-of-returned-items"></a>Palautettujen nimikkeiden poistotavan määrittäminen 

[!include [banner](../includes/banner.md)]


Kun käsittelet palautustilausta, sinun on määritettävä palautuksen syykoodi, jonka avulla tunnistetaan miksi tuote palautetaan. Sinun on myös myös määritettävä käsittelykoodi ja käsittelytoiminto määrittääksesi mitä itse palautetulle tuotteelle tulisi tehdä.

Voit käyttää käsittelykoodia, kun luot palautustilauksen, rekisteröit nimikkeen saapumisen tai päivität pakkausluettelon nimikkeen saapumisen yhteydessä ja päätät karanteenitilauksen.

Voit määrittää mitä tahansa tarvitsemiasi käsittelykoodeja liiketoimintaprosessien tukemiseen. Seuraavassa taulukossa on joukko tavallisesti palautusnimikkeen käsittelyyn käytettyjä koodeja.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Käsittelytyyppi</p></th>
<th><p>Yleinen koodi</p></th>
<th><p>kuvaus</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Luovutus</p></td>
<td><p>Š</p></td>
<td><p>Hävitä/tuhoa</p></td>
</tr>
<tr class="even">
<td><p>Luovutus</p></td>
<td><p>DC</p></td>
<td><p>Lahjoita hyväntekeväisyyteen</p></td>
</tr>
<tr class="odd">
<td><p>Luovutus</p></td>
<td><p>TD</p></td>
<td><p>Luovuta kolmannelle osapuolelle</p></td>
</tr>
<tr class="even">
<td><p>Luovutus</p></td>
<td><p>SL</p></td>
<td><p>Romuta</p></td>
</tr>
<tr class="odd">
<td><p>Luovutus</p></td>
<td><p>TS</p></td>
<td><p>Myy kolmannelle osapuolelle (jälkimarkkinat)</p></td>
</tr>
<tr class="even">
<td><p>Korjaa/muokkaa</p></td>
<td><p>RW</p></td>
<td><p>Käytä uudelleen</p></td>
</tr>
<tr class="odd">
<td><p>Korjaa/muokkaa</p></td>
<td><p>RF</p></td>
<td><p>Valmista uudelleen / kunnosta</p></td>
</tr>
<tr class="even">
<td><p>Korjaa/muokkaa</p></td>
<td><p>MD</p></td>
<td><p>Muokkaa</p></td>
</tr>
<tr class="odd">
<td><p>Korjaa/muokkaa</p></td>
<td><p>RP</p></td>
<td><p>Korjaa</p></td>
</tr>
<tr class="even">
<td><p>Korjaa/muokkaa</p></td>
<td><p>VASTAKIRJAUS</p></td>
<td><p>Palauta myyjälle</p></td>
</tr>
<tr class="odd">
<td><p>Muu</p></td>
<td><p>AI</p></td>
<td><p>Käytä sellaisenaan</p></td>
</tr>
<tr class="even">
<td><p>Muu</p></td>
<td><p>RS</p></td>
<td><p>Myy eteenpäin</p></td>
</tr>
<tr class="odd">
<td><p>Muu</p></td>
<td><p>EX</p></td>
<td><p>Vaihda</p></td>
</tr>
<tr class="even">
<td><p>Muu</p></td>
<td><p>MS</p></td>
<td><p>Muut</p></td>
</tr>
</tbody>
</table>


Sinun on määritettävä jokaiselle määrittämällesi käsittelykoodille käsittelytoiminto. Käsittelytoiminto määrittää käsittelykoodien fyysiset ja taloudelliset vaikutukset. Käsittelytoiminto määrittää esimerkiksi palautetun nimikkeen fyysisen käsittelyn, palautetun nimikkeen taloudellisen vaikutuksen, ja jos asiakkaalle on lähetettävä korvaavaa nimike. Voit määrittää rajattoman määrän käsittelykoodeja yrityksesi tarpeiden mukaisesti, mutta valittavissa on vain vain kuusi ennalta asetettua käsittelytapahtumaa. Seuraavassa taulukossa on esitelty käsittelytoiminnot ja niiden määritelmät.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Käsittelytoiminto</p></th>
<th><p>kuvaus</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Kredit</strong></p></td>
<td><p>Palauta nimike varastoon ja hyvitä asiakasta.</p></td>
</tr>
<tr class="even">
<td><p><strong>Vain hyvitys</strong></p></td>
<td><p>Palauta hyvitys asiakkaalle ilman vaatimusta tai oletusta nimikkeen palauttamisesta.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Hävikki</strong></p></td>
<td><p>Hävitä nimike ja hyvitä asiakkaalle.</p></td>
</tr>
<tr class="even">
<td><p><strong>Korvaus ja hyvitys</strong></p></td>
<td><p>Palauta nimike varastoon, luo korvaava tilaus ja hyvitä asiakkaalle.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Korvaus ja hävitys</strong></p></td>
<td><p>Hävitä nimike, luo korvaava tilaus ja hyvitä asiakkaalle.</p></td>
</tr>
<tr class="even">
<td><p><strong>Palautus asiakkaalle</strong></p></td>
<td><p>Hylkää palautettu nimike ja palauta se asiakkaalle.</p></td>
</tr>
</tbody>
</table>


## <a name="select-a-disposition-code-for-a-quarantine-order"></a>Karanteenitilauksen käsittelykoodin valitseminen

1.  Valitse **Varastonhallinta** \> **Kausittainen** \> **Laadunhallinta** \> **Karanteenitilaukset**.

2.  Jos kyseessä on aiemmin luotu karanteenitilaus, valitse **Käsittelykoodi**-kenttä **Yleiskatsaus**-välilehdestä.



## <a name="see-also"></a>Lisätietoja

[Karanteenitilaus (lomake)](https://technet.microsoft.com/en-us/library/aa554073(v=ax.60))

[Käsittelykoodit (lomake)](https://technet.microsoft.com/en-us/library/hh597113\(v=ax.60\))

  



