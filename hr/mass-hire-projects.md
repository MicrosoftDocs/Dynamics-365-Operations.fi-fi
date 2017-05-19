---
title: "Joukkotyöhönottoprojektit"
description: "Henkilöstöhallinnon asiantuntija voi luoda useita toimia ja palkata useita työntekijöitä näihin toimiin joukkotyöhönottoprojektien avulla."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: HRMMassHireProject
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 7481
ms.assetid: 5f5eb271-76eb-4305-bd1c-5d171dafccc9
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 5ba5816b65bcaa3a71ab3367cfbe6a115e52062a
ms.contentlocale: fi-fi
ms.lasthandoff: 04/25/2017


---

# <a name="mass-hire-projects"></a>Joukkotyöhönottoprojektit

[!include[banner](includes/banner.md)]


Henkilöstöhallinnon asiantuntija voi luoda useita toimia ja palkata useita työntekijöitä näihin toimiin joukkotyöhönottoprojektien avulla.

<a name="overview"></a>Yleiskuvaus
--------

Jos otat työhön samalla kertaa useita työntekijöitä esimerkiksi sesonkitarpeen vuoksi, kannattaa luoda joukkotyöhönottoprojekti. Joukkotyöhönottoprojektin luominen on kannattavaa, koska voit luoda toimitietueet, työntekijätietueet ja työntekijämääritykset toimille samanaikaisesti. Kun luot toimia joukkotyöhönottoprojektiin, voit määrittää seuraavat tiedot:
-   Luotavien toimien määrä
-   Työntekijätyyppi, joita palkkaat toimiin
-   Osasto ja työ, jotka liittyvät toimiin
-   Toimen kokoaikaisuutta vastaava arvo

## <a name="example"></a>Esimerkki
Kesällä palkataan yleensä 15-20 osa-aikaista opiskelijaa yrityksen kesäharjoittelupaikkoihin. Tänä vuonna haluat palkata viisi kirjanpitäjää, viisi tilauskäsittelijää ja viisi kassanhoitajaa. Sen sijaan, että loisit jokaisen toimi- ja työntekijätietueen erikseen, voit luoda yhden joukkotyöhönottoprojektin nimellä "SummerInterns". Projektin aloitus- ja päättymispäivämäärät vastaavat joukkotyöhönottoprojektille luomiesi toimien aloitus- ja päättymispäivämääriä. 

Valitse **Joukkotyöhönottoprojektit** -sivulla "SummerInterns"-projekti ja napsauta sitten **Avaa projekti**. Valitse avoimet joukkotyöhönottoprojektissa **Luo toimia** ja kirjoita kirjanpitäjätoimen tiedot. Voit määrittää, että viisi kirjanpitäjän toimea on luotava samoilla tiedoilla, ja napsauttaa sitten OK. Toista nämä vaiheet tilauskäsittelijän ja kassanhoitajan toimille. 

Valittuasi kesäharjoittelijoiksi palkattavat opiskelijat, voit syöttää opiskelijoiden tiedot niiden toimien **Toimen tiedot** kohtaan, johon olet kunkin opiskelijan valinnut. Kun olet syöttänyt kaikkien toimien tiedot, valitse toimi Joukkotyöhönottoprojektit-sivulta ja napsauta sitten **Ota palvelukseen**. Jokaiselle toimelle luodaan toimitietue ja jokaiselle työhön ottamallesi henkilölle luodaan työntekijätietue, joka liitetään asiaankuuluvaan toimeen.

## <a name="mass-hire-project-statuses"></a>Joukkotyöhönottoprojektin tilat
Joukkotyöhönottoprojektin tila voi olla jokin seuraavista.
-   Luotu
-   Avoin
-   Suljettu

Napsauta **Joukkotyöhönottoprojekti**-sivulla **Avaa projekti** tai **Sulje projekti** muuttaaksesi joukkotyöhönottoprojektin tilaa. Seuraavassa taulukossa on kuvattu, mitä voit tehdä projektille sen tilan mukaan.

<table>
<thead>
<tr class="header">
<th>Tila</th>
<th>Kuvaus</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Luotu</td>
<td>Voit luoda ja muokata tietoja, mutta et luoda toimia projektille. Tämä on uusien projektien oletustila.</td>
</tr>
<tr class="even">
<td>Avoin</td>
<td>Voit muokata projektin tietoja, luoda toimia joukkotyöhönottoprojektin ja palkata henkilöitä toimiin. Tämä on aktiivisten projektien tila.</td>
</tr>
<tr class="odd">
<td>Suljettu</td>
<td>Et voi lisätä toimia projektiin. Lisätäksesi toimia joukkotyöhönottoprojektiin, avaa projekti uudelleen. Tämä on valmiiden projektien tila.
<div class="alert">
<table>
<thead>
<tr class="header">
<th><strong>Huomautus </strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Ennen joukkotyöhönottoprojektin sulkemista kaikkien projektin toimien tilan on oltava joko Luotu tai Suljettu.</td>
</tr>
</tbody>
</table>
</div></td>
</tr>
</tbody>
</table>

 






