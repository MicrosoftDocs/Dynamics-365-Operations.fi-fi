---
title: Tilauslaskutuksen yleiskuvaus
description: Tässä ohjeaiheessa käsitellään tilauslaskutusta Microsoft Dynamics 365 Financessa.
author: JodiChristiansen
ms.date: 04/13/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustPosting, CustVendExternalItem
audience: Application User
ms.reviewer: twheeloc
ms.custom: 24651
ms.assetid: cb82245e-8c02-429c-b36e-8db0e3e6f7e5
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2022-02-09
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: 9d46492cca3cc435048fa497f6b1f3a28b77140a
ms.sourcegitcommit: d715e44b92b84b1703f5915d15d403ccf17c6606
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/27/2022
ms.locfileid: "8644524"
---
# <a name="subscription-billing-overview"></a>Tilauslaskutuksen yleiskuvaus

[!include [banner](../includes/banner.md)]

Tilauslaskutuksen avulla organisaatiot voivat hallita tilaustuottomahdollisuuksia ja toistuvaa laskutusta laskutusaikataulujen avulla. Monimutkaisia hinnoittelu- ja laskutusmalleja ja tuottojen kohdistusta voi hallita helposti, ja ne laskutetaan ja kirjataan rivitasolla. Moniosainen tuottojen kohdistus mahdollistaa, että tuottojen kohdistus on seuraavien standardien mukaista: kansainvälinen tilinpäätösstandardi 15 \[IFRS 15\] ja standardi Accounting Standards Codification Topic 606 \[ASC 606\].

Ratkaisussa on kolme moduulia, joita voidaan käyttää erikseen. Vaihtoehtoisesti kaikkia kolmea moduulia voidaan käyttää yhdessä.

- **Toistuva sopimuslaskutus** – Tämä moduuli mahdollistaa toistuvan laskutuksen ja hinnanhallinnan, joilla ohjataan hinnoittelu- ja laskutusparametreja, sopimusten uusimista ja konsolidoitua laskutusta.
- **Tuottojen ja kulujen lykkäykset** – Tämä moduuli poistaa manuaalisia prosesseja ja riippuvuuksia ulkoisista järjestelmistä hallitsemalla tuottoja ja mahdollistamalla reaaliaikaisten tietojen saamisen kuukausittaisista toistuvista tuotoista.
- **Moniosainen tuottojen kohdistus** – Tämä moduuli edistää tuottojen vaatimustenmukaisuutta käsittelemällä hinnoittelua ja tuottojen kohdistusta useiden nimikkeiden osalta.

Lisätietoja tilauslaskutuksesta on [Tilauslaskutuksen Power BI -sisällössä](sub-bill-power-bi.md).

Tilauslaskutus otetaan käyttöön **Toimintojen hallinnassa**. Sitä ei kuitenkaan voi käyttää yhdessä **Tuoton kirjaus** -toiminnon kanssa. Siksi kyseinen toiminto on poistettava käytöstä ennen tilauslaskutuksen käyttöönottoa.

1. Syötä **Toimintojen hallinta** -työtilan **Kaikki**-välilehden suodattimeen **Tuoton kirjaus** ja valitse sitten toiminnon nimi suodattimeksi.
2. Valitse **Tuoton kirjaus** -toiminto ja sitten **Poista käytöstä**.
3. Kirjoita **Toiminnon nimi** -suodattimeen **Tilauslaskutus** ja valitse sitten moduulisuodatin.
4. Valitse **Tilauslaskutus**-toiminto ja sitten **Ota käyttöön**.
5. Valitse jokin edellisen luettelon kolmesta moduulista ja sitten **Ota käyttöön**. Toista tämä kahden muun moduulin osalta.

    > [!IMPORTANT]
    > **Tilauslaskutus**-toiminnon on oltava käytössä, ennen kuin voit ottaa käyttöön jonkin kolmesta moduulista.
