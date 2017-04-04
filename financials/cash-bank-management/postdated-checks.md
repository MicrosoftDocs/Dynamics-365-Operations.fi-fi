---
title: "Myöhemmäksi päivätyt sekit"
description: "Tässä artikkelissa on tietoja Microsoft Dynamics-365 työvaiheiden myöhemmäksi päivitettyjen sekkien tuki. Myöhemmäksi päivätyt sekit ovat sekkejä, jotka on asetettu tulevan päivämäärän omaavien maksujen vastaanottamista varten. Tämän vuoksi sekkiä ei voi lunastaa ennen määritettyä päivämäärää."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 21741
ms.assetid: 4eb7c7da-1e6b-4d35-9f41-373b66103229
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 4bb647cfd3f012efbffa93a81462c538a24ac850
ms.openlocfilehash: 7349771b7f9a1ad4cd5b239f1d10bd3229d2d0df
ms.lasthandoff: 03/31/2017


---

# <a name="postdated-checks"></a>Myöhemmäksi päivätyt sekit

Tässä artikkelissa on tietoja Microsoft Dynamics-365 työvaiheiden myöhemmäksi päivitettyjen sekkien tuki. Myöhemmäksi päivätyt sekit ovat sekkejä, jotka on asetettu tulevan päivämäärän omaavien maksujen vastaanottamista varten. Tämän vuoksi sekkiä ei voi lunastaa ennen määritettyä päivämäärää.

Microsoft Dynamics-365 työvaiheiden tukee täyden hallinnan kehä sekä myyntireskontran ja ostoreskontran ja myöhemmäksi päivätyt sekit seuraavassa taulukossa esitetyllä tavalla.
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Skenaario</th>
<th>Erittely</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Aseta jälkeen päin päivitetyt laskut</td>
<td>Määritä uusi maksutapa ja maksurutiini lähetettyjen ja vastaanotettujen sekkien sekä ennakonpidätyksen selvitystileille.</td>
</tr>
<tr class="even">
<td>Kirjaa ja lähetä toimittajalle jälkeen päin päivitetty lasku</td>
<td>Rekisteröi toimittajalle kirjoittamasi myöhemmäksi päivätyn sekin tiedot. Kun maksu kirjataan, toimittajan vastuu on tunnistettu, mutta pankkitili ei ole vielä hyvityslasku. Sen sijaan käytetään selvitystiliä.</td>
</tr>
<tr class="odd">
<td>Rekisteröi ja kirjaa asiakkaan myöhemmäksi päivitetty sekki</td>
<td>Rekisteröi asiakkaalta saadun myöhemmäksi päivätyn sekin tiedot. Kun maksu kirjataan, myyntireskontran asiakas on luotto, mutta pankkitili ei ole vielä veloittaa. Sen sijaan käytetään selvitystiliä.</td>
</tr>
<tr class="even">
<td>Rekisteröi ja kirjaa asiakkaan tai toimittajan myöhemmäksi päivättyjen korvaavan valinta</td>
<td>
Jos toimittajalle lähetetty tai asiakkaalta vastaanotettu alkuperäinen sekki on kadonnut tai vahingoittunut, voit asettaa korvaavan myöhemmäksi päivätyn sekin. Kun rekisteröit sekin tiedot, määritä viittaus alkuperäiseen sekkiin ja osoita, että uusi sekki korvaa alkuperäisen sekin. Voit myös kirjata korvaavan sekin.</td>
</tr>
<tr class="odd">
<td>Asiakkaan myöhemmäksi päivätyn sekin siirtäminen toimittajalle</td>
<td>Kun vastaanotat asiakkaalta myöhemmäksi päivätyn sekin, voit siirtää kyseisen sekin toimittajalle maksuna.</td>
</tr>
<tr class="even">
<td>Sovi jälkeen päin päivitetty lasku asiakkaalle tai toimittajalle</td>
<td>Tilitä asiakkaan tai toimittajan välitilille kirjattu myöhemmäksi päivätty sekki sitten, kun sekki lopulta erääntyy. Kun sekki on tilitetty, pankille määritetään veloitus tai hyvitys aiemmin käytetylle selvitystilille.</td>
</tr>
<tr class="odd">
<td>Peruuta toimittajalle osoitettu myöhemmäksi päivätty shekki</td>
<td>Voit peruuttaa kirjattujen myöhemmäksi päivättyjen sekkien seuraavissa tilanteissa:-pankin sekin palautetaan.
Väärä lasku on käytössä-valintaruutu.
-Cash maksu suoritetaan tarkistusta vastaan.
</td>
</tr>
<tr class="even">
<td>Lopeta jälkikirjatun sekin maksu</td>
<td>Voit lopettaa toimittajalle myönnetyn myöhemmäksi päivätyn sekkimaksun esimerkiksi seuraavista syistä: varat eivät riitä, sopimusehtojen toimittajan kanssa muuttuvat, toimittaja on toimittanut viallisia tavaroita tai tavaroita palautetaan toimittajalle. Voit pysäyttää maksu vain tarkistaa, että et ole poistettu.</td>
</tr>
</tbody>
</table>





