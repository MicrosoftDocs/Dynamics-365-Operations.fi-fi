---
title: Joukkotyöhönottoprojektit
description: Henkilöstöhallinnon asiantuntija voi luoda useita toimia ja palkata useita työntekijöitä näihin toimiin joukkotyöhönottoprojektien avulla.
author: andreabichsel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HRMMassHireProject
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.custom: 7481
ms.assetid: 5f5eb271-76eb-4305-bd1c-5d171dafccc9
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f7dacc8b0ca8659d3ae69c81385918ef6fa39c04
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/07/2019
ms.locfileid: "1510744"
---
# <a name="mass-hire-projects"></a>Joukkotyöhönottoprojektit

[!include [banner](../includes/banner.md)]

Henkilöstöhallinnon asiantuntija voi luoda useita toimia ja palkata useita työntekijöitä näihin toimiin joukkotyöhönottoprojektien avulla.

## <a name="overview"></a>Yleiskuvaus

Jos otat työhön samalla kertaa useita työntekijöitä esimerkiksi sesonkitarpeen vuoksi, kannattaa luoda joukkotyöhönottoprojekti. Joukkotyöhönottoprojektin luominen on kannattavaa, koska voit luoda toimitietueet, työntekijätietueet ja työntekijämääritykset toimille samanaikaisesti. Kun luot toimia joukkotyöhönottoprojektiin, voit määrittää seuraavat tiedot:

- Luotavien toimien määrä
- Työntekijätyyppi, joita palkkaat toimiin
- Osasto ja työ, jotka liittyvät toimiin
- Toimen kokoaikaisuutta vastaava arvo

## <a name="example"></a>Esimerkki

Kesällä palkataan yleensä 15-20 osa-aikaista opiskelijaa yrityksen kesäharjoittelupaikkoihin. Tänä vuonna haluat palkata viisi kirjanpitäjää, viisi tilauskäsittelijää ja viisi kassanhoitajaa. Sen sijaan että loisit jokaisen toimi- ja työntekijätietueen erikseen, voit luoda yhden joukkotyöhönottoprojektin nimellä SummerInterns. Projektin aloitus- ja päättymispäivämäärät vastaavat joukkotyöhönottoprojektille luomiesi toimien aloitus- ja päättymispäivämääriä.

Valitse **Joukkotyöhönottoprojektit**-sivulla SummerInterns-projekti ja valitse sitten **Avaa projekti**. Valitse avoimet joukkotyöhönottoprojektissa **Luo toimia** ja kirjoita kirjanpitäjätoimen tiedot. Voit määrittää, että viisi kirjanpitäjän toimea on luotava samoilla tiedoilla, ja napsauttaa sitten OK. Toista nämä vaiheet tilauskäsittelijän ja kassanhoitajan toimille.

Valittuasi kesäharjoittelijoiksi palkattavat opiskelijat, voit antaa opiskelijoiden tiedot niiden toimien **Toimen tiedot** -kohtaan, johon olet kunkin opiskelijan valinnut. Kun olet syöttänyt kaikkien toimien tiedot, valitse toimi Joukkotyöhönottoprojektit-sivulta ja napsauta sitten **Ota palvelukseen**. Jokaiselle toimelle luodaan toimitietue ja jokaiselle työhön ottamallesi henkilölle luodaan työntekijätietue, joka liitetään asiaankuuluvaan toimeen.

## <a name="mass-hire-project-statuses"></a>Joukkotyöhönottoprojektin tilat

Joukkotyöhönottoprojektin tila voi olla jokin seuraavista.

- Luotu
- Avoin
- Suljettu

Napsauta **Joukkotyöhönottoprojekti**-sivulla **Avaa projekti** tai **Sulje projekti** muuttaaksesi joukkotyöhönottoprojektin tilaa. Seuraavassa taulukossa on kuvattu, mitä voit tehdä projektille sen tilan mukaan.

<table>
<thead>
<tr>
<th>Tila</th>
<th>Kuvaus</th>
</tr>
</thead>
<tbody>
<tr>
<td>Luotu</td>
<td>Voit luoda ja muokata tietoja, mutta et luoda toimia projektille. Tämä on uusien projektien oletustila.</td>
</tr>
<tr>
<td>Avoin</td>
<td>Voit muokata projektin tietoja, luoda toimia joukkotyöhönottoprojektin ja palkata henkilöitä toimiin. Tämä on aktiivisten projektien tila.</td>
</tr>
<tr>
<td>Suljettu</td>
<td>Et voi lisätä toimia projektiin. Lisätäksesi toimia joukkotyöhönottoprojektiin, avaa projekti uudelleen. Tämä on valmiiden projektien tila.
<blockquote>[!NOTE] Ennen joukkotyöhönottoprojektin sulkemista kaikkien projektin toimien tilan on oltava joko Luotu tai Suljettu.</blockquote>
</td>
</tr>
</tbody>
</table>
