---
title: "Warehousing app app kenttien nimien määrittäminen"
description: "Tässä aiheessa kuvataan, miten määrittäminen fyysisen varastoinnin app kenttien nimet ja painopisteet-operaatioille Dynamics 365."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: WHSMobileAppField, WHSMobileAppFieldPriority
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 269434
ms.assetid: 6cf3d7da-29bb-4d3d-aaf5-544ca9cc2980
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mafoge
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: f77012e7b64b7f153103e9bbe91e8ded202b509a
ms.openlocfilehash: ce8f6d6f7090995bc44db1ba0103a7d6c0416620
ms.lasthandoff: 03/31/2017


---

# <a name="configure-app-field-names-in-warehousing-app"></a>Warehousing app app kenttien nimien määrittäminen

Tässä aiheessa kuvataan, miten määrittäminen fyysisen varastoinnin app kenttien nimet ja painopisteet-operaatioille Dynamics 365. 

**Huomautus:** tämä aihe koskee fyysisen varastoinnin hallinnan toiminnot. Se ei koske Varastonhallinta ominaisuudet. Työvaiheiden - 365 Dynamics varastoinnista on sovellus, jonka avulla voit käyttää fyysisen varastoinnin tehtävien suorittamiseen. Voit määrittää ja määrittää kenttien nimet, joita käytetään sovelluksen, kuin sekä määrittää prioriteetti, johon kenttien nimet olisi liitetty. Tässä ohjeaiheessa kerrotaan, kuinka nämä fyysisen varastoinnin app kenttien nimet ja painopisteiden määrittäminen ja miten niitä käytetään Dynamics 365-toiminnot - varastoinnista. Lisätietoja Määritä yhteys Dynamics 365 työvaiheiden - varastointi, Katso opetusohjelma [asentaa ja määrittää työvaiheiden - varastoinnista 365 Dynamics](install-configure-warehousing-app.md).

<a name="configure-warehouse-app-field-names"></a>Määritä varasto app kenttien nimet
===================================

Kun käytät Operations - Dynamics 365 varastoinnista matkaviestimessä, voit määrittää miten metatiedot näytetään laite **varasto app kenttien nimet** sivun. Valitse uusi yrityksen toiminnoissa Dynamics 365, **luoda oletusasetukset** luomaan kaikkien kenttien nimet, joita käytetään varaston matkaviestimen työnkulkuja ja osoita heille ensisijainen input mode ja syötteen tyyppi. Kun kaikkien kenttien nimet on luotu, voit valita syötteen seuraavista vaihtoehdoista.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Vaihtoehto</th>
<th>kuvaus</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Ensisijainen syöttömenetelmä</td>
<td>Tämä vaihtoehto määrittää, onko kenttä skannauksen tai manuaalisen syötön syöttökentän näytetään valitun kentän nimen. Tämä on tarpeen erottaa kentät sen mukaan, jos viivakoodeja käytetään kentälle. <strong>Huomautus:</strong>, kenttien nimet ensisijainen syöttö-tilassa arvoksi <strong>Scanning</strong>, voit syöttää tiedot manuaalisesti jos viivakoodi on vioittunut tai lukukelvoton.</td>
</tr>
<tr class="even">
<td>Syötetyyppi</td>
<td>Tämä vaihtoehto määrittää ilmauksen lajin pitäisi käyttää valitun kenttänimi. Käytettävissä on neljä vaihtoehtoa:
<ul>
<li><strong>Valinta</strong> - sisältää luettelon vaihtoehtoa. Tässä vaihtoehdossa kenttien nimiä ei voi muokata.</li>
<li><strong>Päivä</strong> - kenttien nimiä kuten päivämäärä näyttää päivämäärämuoto, jonka nimi on määritetty. Näin varastotyöntekijät Katso mitä voit kirjoittaa päivämäärä muodossa. Tässä vaihtoehdossa kenttien nimiä ei voi muokata.</li>
<li><strong>Alfa</strong> -, jos laitteen näppäimistöä käytetään syötettäessä tietoja manuaalisesti app. Näppäimistön kokemuksia voidaan muuttaa sen mukaan, mitä laitetta käytetään.</li>
<li><strong>Numeerinen</strong> - varten kentän nimiä, Käytä numeroita vain, voit valita tämän vaihtoehdon saat näyttöön mukautetun numeronäppäimistö syöttökentän laitteen näppäimistön sijaan.</li>
</ul></td>
</tr>
</tbody>
</table>

<a name="configure-warehouse-app-field-priority"></a>Määritä varasto app-kentässä prioriteetti
======================================

- **Varasto app-kentässä prioriteetti** -sivulla voit sijoittaa kenttien nimet prioriteetti eri ryhmiin. Näin voit päättää, mitä tietoja näytetään sivulla päätehtävä silloin, kun fyysisen varastoinnin työntekijöiden tehtävät sovelluksen avulla. Jos valitset **luoda oletusasetukset**, järjestelmä luo oletusarvoiset etusijalle. On mahdollista luoda niin monta ensisijaisesti ryhmiä tarpeen mukaan, mutta tehtävä-sivulla näytetään vain kolmelle prioriteetti. Kun Dynamics 365 työvaiheiden lähettää sovelluksen metatietoja, se määrittää kunkin kentän suhteellisen prioriteetin mukaan sen prioriteetti ryhmässä ja sovellus näyttää tehtävän sivulla metatietojen sisältämiä ensimmäisen kolmen prioriteetin ryhmät. Loput menevät metatiedot näytetään toissijainen tiedot-sivulla. Seuraavassa taulukossa on viisi prioriteettia ryhmät esimerkki.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Prioriteetti-ryhmä</th>
<th>Määritetyt kentät</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td> Prioriteetti 10</td>
<td><ul>
<li>Nimike</li>
<li>Määrä</li>
<li>Mittayksikkö</li>
</ul></td>
</tr>
<tr class="even">
<td> Prioriteetti 20</td>
<td><ul>
<li>Sijainti klusterissa</li>
<li>Klusteri</li>
</ul></td>
</tr>
<tr class="odd">
<td> 30 prioriteetti</td>
<td><ul>
<li>Nimikkeen kuvaus</li>
</ul></td>
</tr>
<tr class="even">
<td> 40 prioriteetti</td>
<td><ul>
<li>Konfiguraatio</li>
<li>Väri</li>
<li>Koko</li>
<li>Tyyli</li>
</ul></td>
</tr>
<tr class="odd">
<td> Prioriteetti 50</td>
<td><ul>
<li>Paikka</li>
<li>Rekisterikilpi</li>
</ul></td>
</tr>
</tbody>
</table>

Esimerkiksi kun Varastotyöntekijä suorittaa tehtävän mobiililaitteessa, jos metatietojen, joka näytetään sovelluksen koostuu seuraavista kentistä:

-   Nimike
-   Määrä
-   Mittayksikkö
-   Nimikkeen kuvaus
-   Koko ja sijainti

Yllä olevassa taulukossa määritetty varasto app kentän prioriteetin perusteella, seuraavat 3 tietorivistä näytetään tehtävän sivulla:

-   Rivi 1: Nimike, määrä, mittayksikön koodi
-   Rivi 2: Kuvaus
-   Rivin 3: koon

Jäljellä olevat metatiedot, esimerkiksi sijainti ei näy sivulla tehtävän, mutta tiedot-sivu tulee näkyviin. Lisätietoja ja esimerkkejä käyttöliittymän, voit viitata blogikirjoituksessa [toiminnot - varastoinnista Dynamics 365 julkaisu](https://blogs.msdn.microsoft.com/dynamicsaxscm/2017/01/20/announcing-dynamics-365-for-operations-warehousing/).

<a name="see-also"></a>Lisätietoja
--------

[Asenna ja määritä Microsoft Dynamics-365 työvaiheiden – varastoinnista](install-configure-warehousing-app.md)


