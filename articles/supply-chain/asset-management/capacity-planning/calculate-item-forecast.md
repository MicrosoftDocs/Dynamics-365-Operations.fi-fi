---
title: Laske nimikkeen ennuste
description: Tässä ohjeaiheessa kerrotaan, kuinka nimike-ennuste lasketaan resurssien hallinnassa.
author: josaw1
manager: AnnBe
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 9091ff7a394cd08b68e78c8f668d7cd962003e6d
ms.sourcegitcommit: 109a6ef2d20758dc4a25c51b11e22dd2214a1cc4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/16/2019
ms.locfileid: "1886767"
---
# <a name="calculate-item-forecast"></a>Laske nimikkeen ennuste

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Samalla tavalla kuin voit suorittaa edellisessä osassa kuvatut kapasiteetin kuormituksen laskennat, voit myös tehdä nimikkeen ennustelaskelmia

- Ylläpitoaikataulun rivit  
- työtilauksille, joita ei ole vielä ajoitettu  
- Ajoitetut työtilaukset

Tästä on hyötyä, jos haluat saada yleiskuvan odotetusta nimikkeen kulutuksesta (varaosat sekä muut työtilausten täyttämisessä tarvittavat nimikkeet) tietyltä kaudelta. Nimike-ennusteen laskeminen voidaan tehdä kaikille käyttöomaisuuksille tai valituille käyttöomaisuuksille. Voit myös tehdä laskelmia ylläpidon käyttökatkon tehtäville (**Kaikki ylläpidon käyttökatkojen toiminnot** tai **Aktiiviset ylläpidon käyttökatkojen toiminnot**) tai työtilauspooleille (**Kaikki työtilauspoolit** tai **Aktiiviset työtilauspoolit**).

1. Valitse **Resurssien hallinta** > **Kyselyt** > **Nimike-ennuste** tai **Resurssien hallinta** > **Yhteiset** > **Työtilauspoolit** > **Kaikki työtilauspoolit** / **Aktiiviset työtilauspoolit** > valitse työtilauspooli listasta > **Nimike-ennuste** -painike tai **Resurssien hallinta** > **Yhteiset** > **Ylläpidon käyttökatkojen toiminnot** > **Kaikki ylläpidon käyttökatkojen toiminnot** / **Aktiiviset ylläpidon käyttökatkojen toiminnot** > valitse ylläpitokatkon toiminto listasta> **Nimike-ennuste** -painike.

2. Valitse **Laske nimike-ennuste** -valintaikkunassa laskennan kausi **Alkamispäivämäärä/-kellonaika**- ja **Päättymispäivämäärä/-kellonaika** -kentissä.

3. Valitse **Sisällytä ylläpitoaikataulu** -vaihtopainikkeen arvoksi Kyllä, jos haluat sisällyttää ylläpitoaikataulurivit ennustelaskelmiin.

4. Valitse **Sisällytä työtilaus** -vaihtopainikkeen arvoksi Kyllä, jos haluat sisällyttää työttilauksen työt ennustelaskelmiin.

5. **Taso** -kentän avulla voit määrittää, miten yksityiskohtaisia nimike-ennusteen riveistä haluat liittyen toiminnallisiin sijainteihin. Jos esimerkiksi lisäät kenttään arvon "1" ja kyseessä on monitasoineen toiminnallinen sijaintirakenne, kaikki toimintosijainnin ylläpitoaikataulun rivit ja työtilaukset näkyvät ylimmällä tasolla, joten rivin tunnit voidaan lisätä hierarkiassa alemmista toiminnallisista sijainneista. Jos lisäät arvon "0" **Taso**-kenttään, näkyviin tulee yksityiskohtainen tulos, jossa näkyvät kaikki kunnossapitoaikataulurivit ja kaikki työtilaukset kaikissa niissä toiminnallisissa sijaintitasoissa, joihin ne liittyvät.

6. Aloita laskenta valitsemalla **OK**.

7. Valitse toimintoruudun **Ryhmittely...** -ryhmissä asiaankuuluvia painikkeita tuodaksesi näkyviin laskun vaaditun yksityiskohtaisuuden tason. Valitut toimintoruudun ryhmäpainikkeet on korostettu sinisellä. Aktivoi painike tai poista se käytöstä napsauttamalla painiketta.

8. Valitse **Näytä dimensiot** -painike, jos haluat nähdä nimikkeisiin liittyvät tuote-, varastointi- tai seurantadimensiot. Valitse asiaankuuluvat valintaruudut ja napsauta sitten **OK**.

Alla oleva kuva näyttää näyttökuvan käyttöliittymästä.

![Kuva 1](media/02-capacity-planning.png)
