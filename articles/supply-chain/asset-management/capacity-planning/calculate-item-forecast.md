---
title: Laske nimikkeen ennuste
description: Tässä artikkelissa kerrotaan, kuinka nimike-ennuste lasketaan resurssien hallinnassa.
author: johanhoffmann
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetItemForecast
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 25e9b00533fb183b27c1bbe616cf6f414b44b5e7
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/15/2022
ms.locfileid: "9016098"
---
# <a name="calculate-item-forecast"></a>Laske nimikkeen ennuste

[!include [banner](../../includes/banner.md)]

 

Samalla tavalla kuin voit suorittaa edellisessä osassa kuvatut kapasiteetin kuormituksen laskennat, voit myös tehdä nimikkeen ennustelaskelmia:

- ylläpitoaikataulun riveille  
- työtilauksille, joita ei ole vielä ajoitettu  
- ajoitetuille työtilauksille.

Tästä on hyötyä, jos haluat saada yleiskuvan odotetusta nimikkeen kulutuksesta (varaosat sekä muut työtilausten täyttämisessä tarvittavat nimikkeet) tietyltä kaudelta. Nimike-ennusteen laskeminen voidaan tehdä kaikille käyttöomaisuuksille tai valituille käyttöomaisuuksille. Voit myös tehdä laskelmia ylläpidon käyttökatkon tehtäville (**Kaikki ylläpidon käyttökatkojen toiminnot** tai **Aktiiviset ylläpidon käyttökatkojen toiminnot**) tai työtilauspooleille (**Kaikki työtilauspoolit** tai **Aktiiviset työtilauspoolit**).

1. Valitse **Resurssien hallinta** > **Kyselyt** > **Nimike-ennuste** tai **Resurssien hallinta** > **Työtilauspoolit** > **Kaikki työtilauspoolit** / **Aktiiviset työtilauspoolit**. Valitse työtilauspooli luettelosta ja valitse sitten **Nimike-ennuste**-painike tai **Resurssien hallinta** > **Aktiiviset työtilauspoolit** > **Kaikki ylläpidon käyttökatkojen toiminnot** / **Aktiiviset ylläpidon käyttökatkojen toiminnot**. Valitse luettelosta ylläpitokatkon toiminto ja valitse sitten **Nimike-ennuste**-painike.

2. Valitse **Laske nimike-ennuste** -valintaikkunassa laskennan kausi **Alkamispäivämäärä/-kellonaika**- ja **Päättymispäivämäärä/-kellonaika** -kentissä.

3. Valitse **Sisällytä ylläpitoaikataulu** -vaihtopainikkeen arvoksi Kyllä, jos haluat sisällyttää ylläpitoaikataulurivit ennustelaskelmiin.

4. Valitse **Sisällytä työtilaus** -vaihtopainikkeen arvoksi Kyllä, jos haluat sisällyttää työttilauksen työt ennustelaskelmiin.

5. **Taso** -kentän avulla voit määrittää, miten yksityiskohtaisia nimike-ennusteen riveistä haluat liittyen toiminnallisiin sijainteihin. 

      Jos esimerkiksi lisäät kenttään arvon "1" ja kyseessä on monitasoineen toiminnallinen sijaintirakenne, kaikki toimintosijainnin ylläpitoaikataulun rivit ja työtilaukset näkyvät ylimmällä tasolla, joten rivin tunnit voidaan lisätä hierarkiassa alemmista toiminnallisista sijainneista. 
  
      Jos lisäät arvon "0" **Taso**-kenttään, näkyviin tulee yksityiskohtainen tulos, jossa näkyvät kaikki kunnossapitoaikataulurivit ja kaikki työtilaukset kaikissa niissä toiminnallisissa sijaintitasoissa, joihin ne liittyvät.

6. Aloita laskenta valitsemalla **OK**.

7. Valitse **Ryhmittely...**-ryhmissä asiaankuuluvia painikkeita tuodaksesi näkyviin laskun vaaditun yksityiskohtaisuuden tason. Alla olevassa näyttökuvassa valitut **Ryhmittele...**-painikkeet on korostettu sinisellä. Aktivoi painike tai poista se käytöstä napsauttamalla painiketta.

8. Valitse **Näytä dimensiot** -painike, jos haluat nähdä nimikkeisiin liittyvät tuote-, varastointi- tai seurantadimensiot. Valitse asiaankuuluvat valintaruudut ja napsauta sitten **OK**.

![Kuva 1.](media/02-capacity-planning.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]