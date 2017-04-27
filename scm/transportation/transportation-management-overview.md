---
title: Kuljetustenhallinnan yleiskatsaus
description: "Tämä aihe sisältää yleiskuvauksen Microsoft Dynamics 365 for Operations -ohjelman kuljetustenhallintatoiminnoista."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 30251
ms.assetid: d4e3550c-bca8-469c-82df-56ac0083e4ac
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 3136fd95c4c56495a391668d6c854a6ae1e36479
ms.lasthandoff: 03/31/2017


---

# <a name="transportation-management-overview"></a>Kuljetustenhallinnan yleiskatsaus

[!include[banner](../includes/banner.md)]


Tämä aihe sisältää yleiskuvauksen Microsoft Dynamics 365 for Operations -ohjelman kuljetustenhallintatoiminnoista.

Kuljetustenhallinnan avulla voit hallita yrityksen kuljetuksia sekä määrittää toimittajan ja reititysratkaisut lähteville ja saapuville tilauksille. Voit esimerkiksi tunnistaa nopeimman reitin tai edullisimman hinnan lähetykselle. Seuraavassa taulukossa kuvataan Microsoft Dynamics 365 for Operations -ohjelman kuljetustenhallinnan tärkeimmät käyttöskenaariot.

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

## <a name="planning-transportation-in-dynamics-365-for-operations"></a>Kuljetusten suunnittelu Dynamics 365 for Operations -ohjelmassa
Kuljetustenhallinnassa kuljetusten suunnittelu voidaan tehdä joko tilausten tai niistä luotujen lähetysten perusteella. Lähetykset tapahtuvat aina jossakin vaiheessa, mutta niitä ei tarvita kuljetusten suunnittelussa. Siirtotilaukset kuuluvat lähtevien tilausten skenaarioon, ja ne voidaan suunnitella yhdessä myyntitilausten kanssa. 

![Kuormapiirustus](./media/Load-drawing1-1024x477.jpg)

## <a name="inbound-transportation"></a>Saapuva kuljetus
Kun tilaat nimikkeitä toimittajalta, ja nimikkeet on toimitettava varastoosi, haluat ehkä järjestää nimikkeiden kuljetuksen itse. Dynamics 365 for Operations -ohjelmassa voit suunnitella saapuvan kuorman kuljetuksen ja vastaanoton. Seuraavat kuvat esittävät liiketoimintaprosessin kulkua saapuvan kuorman kuljetuksen suunnittelulle. 

![Saapuvien kuormakuljetusten liiketoimintaprosessin työnkulku](./media/Businessprocessflowforinboundloadtransportation.jpg)

## <a name="outbound-transportation"></a>Lähtevä kuljetus
Voit suunnitella ja käsitellä lähtevän kuorman tiettyjen nimikkeiden toimittamiseksi yrityksen varastosta asiakkaalle. Dynamics 365 for Operations -ohjelmassa voit suunnitella lähtevän kuorman lähetyksen ja kuljetuksen. Seuraavassa kuvassa on esitetty liiketoiminnan prosessin kulku lähtevien kuormien suunnittelemiseksi ja käsittelemiseksi lähetystä varten. 

![Lähtevien kuormien suunnittelu ja käsittely](./media/Planningandprocessingoutboundloads.jpg)

## <a name="load-building"></a>Kuormituksen luonti
Dynamics 365 for Operations sisältää Tilavuuteen perustuva kuormituksen luontistrategia -nimisen kuorman luontistrategian. Sen avulla voit käyttää kuormamallissa määritettyjä suurimpia korkeus- ja painoarvoja tai korvata asetukset syöttämällä uudet arvot. Jos haluat käyttää tätä strategiaa, valitse se **Kuormituksen luontistrategia** -kentässä **Asetukset**-pikavälilehdessä **Kuormituksen luonnin työtila** -sivulla. Voit lisätä myös oman kuormituksen rakennuksen strategioita luomalla uuden luokan sovellusobjektipuussa (AOT).




