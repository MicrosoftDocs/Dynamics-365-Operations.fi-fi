---
title: Varastosovelluksen kenttien nimien määrittäminen
description: Tässä ohjeaiheessa kerrotaan, miten varastosovelluksen kenttien nimet ja prioriteetit määritetään Dynamics 365 Supply Chain Managementissa.
author: MarkusFogelberg
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSMobileAppField, WHSMobileAppFieldPriority
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 269434
ms.assetid: 6cf3d7da-29bb-4d3d-aaf5-544ca9cc2980
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mafoge
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 7a4cfe62aa50c423adfd116a81d7962c30b25fcf
ms.sourcegitcommit: a7a7303004620d2e9cef0642b16d89163911dbb4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/01/2020
ms.locfileid: "3530486"
---
# <a name="configure-app-field-names-in-the-warehouse-app"></a>Varastosovelluksen kenttien nimien määrittäminen

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa kerrotaan, miten varastosovelluksen kenttien nimet ja prioriteetit määritetään Dynamics 365 Supply Chain Managementissa. 

> [!NOTE]
> Tämä ohjeaihe koskee varastonhallintamoduulin ominaisuuksia. Se ei koske inventaariohallintamoduulin ominaisuuksia. Varastointi on sovellus, jonka avulla voit suorittaa fyysisen varastoinnin tehtäviä. Voit määrittää ja konfiguroida kenttien nimet, joita käytetään sovelluksessa, sekä määrittää prioriteetin, johon kenttien nimet tulisi liittää. Tässä ohjeaiheessa kerrotaan, miten nämä varastosovelluksen kenttien nimet ja prioriteetit määritetään ja miten niitä käytetään varastointisovelluksessa. Lisätietoja yhteyden määrittämisestä varastosovellukseen on oppaassa [Varastosovelluksen asennuksen ja määrityksen yleiskatsaus](install-configure-warehousing-app.md).

## <a name="configure-warehouse-app-field-names"></a>Warehousing-sovelluksen kenttien nimien määrittäminen

Jos käytät varastointisovellusta mobiililaitteessa, voit määrittää **Varastointisovelluksen kenttien nimet** -sivulla, miten metatiedot näytetään laitteessa. Luo kaikkien varastoinnin mobiililaitteen työnkulussa käytettävien kenttien nimet valitsemalla uudessa yrityksessä **Luo oletusasetukset**, ja määritä sitten niihin ensisijainen syötetila ja syötteen tyyppi. Kun kaikkien kenttien nimet on luotu, voit valita syötteen seuraavista vaihtoehdoista.

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
<td>Tämä vaihtoehto määrittää, näytetäänkö skannauskenttä vai manuaalinen syöttökenttä valitulle kentän nimelle. Tämä on tarpeen sen erottamiseksi, jos viivakoodeja käytetään tälle kentälle. <strong>Huomautus:</strong> Niille kenttien nimille, joiden ensisijainen syöttötila on <strong>Skannaus</strong>, voit syöttää tiedot manuaalisesti jos viivakoodi on vioittunut tai lukukelvoton.</td>
</tr>
<tr class="even">
<td>Syötetyyppi</td>
<td>Tämä vaihtoehto määrittää, mitä syötetilaa pitäisi käyttää valitulle kentän nimelle. Käytettävissä on neljä asetusta:
<ul>
<li><strong>Valinta</strong> - sisältää asetusluettelon, josta voi valita. Tässä vaihtoehdossa kenttien nimiä ei voi muokata.</li>
<li><strong>Päivämäärä</strong> - kenttien nimet, jotka on määritetty päivämääriksi, näyttävät päivämäärämuodon otsikon yhteydessä. Näin varastotyöntekijät näkevät, missä muodossa kirjoittaa päivämäärä. Tässä vaihtoehdossa kenttien nimiä ei voi muokata.</li>
<li><strong>Alpha</strong> - jos tämä valitaan, laitteen näppäimistöä käytetään syötettäessä tietoja manuaalisesti sovellukseen. Näppäimistön käyttöä voidaan muuttaa sen mukaan, mitä laitetta käytetään.</li>
<li><strong>Numeerinen</strong> - kentän nimille, jotka käyttävät vain numeroita, voit valita tämän vaihtoehdon näyttääksesi mukautetun numeronäppäimistön syöttökentän yhteydessä laitteen näppäimistön sijaan.</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="configure-warehouse-app-field-priority"></a>Warehousing-sovelluksen kenttäprioriteetin määrittäminen

**Varastosovelluksen kenttäprioriteetti** -sivulla voit määrittää kenttänimet eri prioriteettiryhmiin. Näin voit päättää, mitä tietoja näytetään sivulla päätehtäväsivulla silloin, kun fyysisen varastoinnin työntekijät suorittavat tehtäviä sovelluksen avulla. Jos valitset **Luo oletusasetukset**, järjestelmä luo oletusarvoiset prioriteettiryhmät. On mahdollista luoda niin monta prioriteettiryhmiä kuin on tarpeen, mutta tehtäväsivulla näytetään vain kolme prioriteettiryhmää. Kun järjestelmä lähettää metatietoja sovellukseen, se määrittää kunkin kentän suhteellisen prioriteetin sen prioriteettiryhmän mukaan, ja sovellus näyttää ensimmäiset kolme metatietojen sisältämää prioriteettiryhmää. Loput metatiedot näytetään toissijaisten tietojen sivulla. Seuraavassa taulukossa on esimerkit viidestä prioriteettiryhmästä.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Prioriteettiryhmä</th>
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
<td> Prioriteetti 30</td>
<td><ul>
<li>Nimikkeen kuvaus</li>
</ul></td>
</tr>
<tr class="even">
<td> Prioriteetti 40</td>
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

Esimerkiksi kun varastotyöntekijä suorittaa tehtävän mobiililaitteella ja jos metatiedot, jotka näytetään sovelluksessa, koostuu seuraavista kentistä:

-   Nimike
-   Määrä
-   Mittayksikkö
-   Nimikkeen kuvaus
-   Koko ja sijainti

Yllä olevassa taulukossa määritettyjen varastosovelluksen kenttäprioriteettien perusteella seuraavat 3 tietoriviä näytetään tehtäväsivulla:

-   Rivi 1: Nimike, Määrä, Mittayksikkö
-   Rivi 2: Nimikkeen kuvaus
-   Rivi 3: koko

Jäljellä olevat metatiedot, esimerkiksi sijainti, ei näy tehtäväsivulla, mutta kylläkin tietosivulla. Lisätietoja ja esimerkkejä käyttöliittymästä saat blogikirjoituksesta [Finance and Operationsin varastointisovelluksen julkaisu](https://blogs.msdn.microsoft.com/dynamicsaxscm/2017/01/20/announcing-dynamics-365-for-operations-warehousing/).

<a name="additional-resources"></a>Lisäresurssit
--------

[Varastosovelluksen asentamisen ja määrittämisen yleiskatsaus](install-configure-warehousing-app.md)
