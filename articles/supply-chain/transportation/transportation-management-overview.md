---
title: Kuljetustenhallinnan yleiskatsaus
description: Tässä ohjeaiheessa on Microsoft Dynamics 365 for Finance and Operationsin kuljetustenhallinnan toimintojen yleiskatsaus.
author: MarkusFogelberg
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSParameters,TMSRateRouteWorkbench, WHSLoadPlanningWorkbench
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 30251
ms.assetid: d4e3550c-bca8-469c-82df-56ac0083e4ac
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 918167a3ab72b3d3665cf710d8e509417b94a056
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "355607"
---
# <a name="transportation-management-overview"></a>Kuljetustenhallinnan yleiskatsaus

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa on Microsoft Dynamics 365 for Finance and Operationsin kuljetustenhallinnan toimintojen yleiskatsaus.

Kuljetustenhallinnan avulla voit hallita yrityksen kuljetuksia sekä määrittää toimittajan ja reititysratkaisut lähteville ja saapuville tilauksille. Voit esimerkiksi tunnistaa nopeimman reitin tai edullisimman hinnan lähetykselle. Seuraavassa taulukossa kuvataan Microsoft Dynamics 365 for Finance and Operationsin kuljetustenhallinnan tärkeimmät käyttöskenaariot.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Skenaario</th>
<th>Missä kuljetustenhallinnasta on apua</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Ulkoisten logistiikkatoimittajien käyttö kuljetustehtävissä.</td>
<td>Kuljetustenhallinnan käyttö saapuvissa ja lähtevissä kuljetuksissa.</td>
</tr>
<tr class="even">
<td>Yrityksen omaa kalustoa voidaan käyttää toimituksissa ja noudoissa, ja toimituskulut siirretään asiakkaille.</td>
<td>Lähtevissä prosesseissa voit kuljetustenhallinnan avulla määrittää kuljetuskulut ja siirtää ne asiakkaille. Rahdinkuljettajan laskun täsmäytysprosessia ei kuitenkaan tarvita.</td>
</tr>
<tr class="odd">
<td>Yrityksen omaa kalustoa voidaan käyttää toimituksissa ja noudoissa, mutta toimituskulut eivät siirry asiakkaille, koska kuljetus sisältyy tuotehintoihin.</td>
<td>Läheskään kaikki kuljetustenhallinnan toiminnot eivät ole pakollisia. Kuljetustenhallinnan avulla voit kuitenkin määrittää kuljetushinnat ja tarkistaa myyntihintoja niiden mukaan.</td>
</tr>
<tr class="even">
<td>Logistiikkapalvelua tarjoaa toinen samaan yhtiöön kuuluva yritys.</td>
<td><ul>
<li>Kuljetustenhallinnan avulla voit käsitellä toista yritystä kuin mitä tahansa muuta rahdinkuljettajaa. Yritysten välisiä taloudellisia tapahtumia ei voi automatisoida. Siksi nämä tapahtumat on käsiteltävä manuaalisesti (esimerkiksi luomalla ostotilaus).</li>
<li>Yritys, joka tarjoaa logistiikkapalveluja, voi käyttää kuljetustenhallintaa kuljetushintojen määrittämiseen.</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="planning-transportation-in-finance-and-operations"></a>Kuljetusten suunnittelu Finance and Operationsissa
Kuljetustenhallinnassa kuljetusten suunnittelu voidaan tehdä joko tilausten tai niistä luotujen lähetysten perusteella. Lähetykset tapahtuvat aina jossakin vaiheessa, mutta niitä ei tarvita kuljetusten suunnittelussa. Siirtotilaukset kuuluvat lähtevien tilausten skenaarioon, ja ne voidaan suunnitella yhdessä myyntitilausten kanssa. 

![Kuormapiirustus](./media/Load-drawing1-1024x477.jpg)

## <a name="inbound-transportation"></a>Saapuva kuljetus
Kun tilaat nimikkeitä toimittajalta, ja nimikkeet on toimitettava varastoosi, haluat ehkä järjestää nimikkeiden kuljetuksen itse. Dynamics 365 for Finance and Operations -ohjelmassa voit suunnitella saapuvan kuorman kuljetuksen ja vastaanoton. Seuraavat kuvat esittävät liiketoimintaprosessin kulkua saapuvan kuorman kuljetuksen suunnittelulle. 

![Saapuvien kuormakuljetusten liiketoimintaprosessin työnkulku](./media/Businessprocessflowforinboundloadtransportation.jpg)

## <a name="outbound-transportation"></a>Lähtevä kuljetus
Voit suunnitella ja käsitellä lähtevän kuorman tiettyjen nimikkeiden toimittamiseksi yrityksen varastosta asiakkaalle. Finance and Operations -ohjelmassa voit suunnitella lähtevän kuorman kuljetuksen ja toimituksen. Seuraavassa kuvassa on esitetty liiketoiminnan prosessin kulku lähtevien kuormien suunnittelemiseksi ja käsittelemiseksi lähetystä varten. 

![Lähtevien kuormien suunnittelu ja käsittely](./media/Planningandprocessingoutboundloads.jpg)

## <a name="load-building"></a>Kuormituksen luonti
Finance and Operations sisältää Tilavuuteen perustuva kuormituksen luontistrategia -nimisen kuorman luontistrategian. Sen avulla voit käyttää kuormamallissa määritettyjä suurimpia korkeus- ja painoarvoja tai korvata asetukset syöttämällä uudet arvot. Jos haluat käyttää tätä strategiaa, valitse se **Kuormituksen luontistrategia** -kentässä **Asetukset**-pikavälilehdessä **Kuormituksen luonnin työtila** -sivulla. Voit lisätä myös oman kuormituksen rakennuksen strategioita luomalla uuden luokan sovellusobjektipuussa (AOT).



