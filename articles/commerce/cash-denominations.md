---
title: Määritä käteisvarojen arvot myyntipisteeseen
description: Seteleiden ja kolikoiden arvot voidaan määrittää taustajärjestelmässä kassojen, myyjien ja esimiesten käyttöön myymälän myyntipisteissä.
author: jblucher
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailStoreTable, RetailStoreCashDeclarationTable
audience: Application User
ms.reviewer: josaw
ms.custom: 16231
ms.assetid: f28a827c-3a50-4d5e-83eb-e5a768db70a1
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 0ff4eb5bc7c5e2c0192a5349219301b26e479ac6be978eb05063b68f348b4e55
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6743455"
---
# <a name="configure-cash-denominations-for-the-point-of-sale-pos"></a>Määritä käteisvarojen arvot myyntipisteeseen

[!include [banner](includes/banner.md)]

Seteleiden ja kolikoiden arvot voidaan määrittää taustajärjestelmässä kassojen, myyjien ja esimiesten käyttöön myymälän myyntipisteissä. Näitä arvoja voidaan käyttää helpottamaan käteisvarojen laskemista, kun kassa lasketaan päivän lopussa maksuvälineittäin tai myynnin nopeassa maksuvälinetapahtumassa.

## <a name="define-denominations"></a>Arvojen määrittäminen

Myymäläkohtaiset arvot määritetään **Asetukset** \> **Myymäläominaisuuden kassatilitysasetus** -sivulla.

![Kassatilitysasetus.](./media/image1-denomination.png)

Arvon määrittäminen:

1. Valitse **Uusi**.
1. Määritä tyyppi (kolikko tai seteli).
1. Määritä summa (arvo).

![Kassatilityksen arvot -sivu.](./media/image2-denomination.png)

## <a name="configure-the-functionality-profile"></a>Toimintoprofiilin määrittäminen

Kun myyntipisteessä maksetaan käteisellä, käyttäjä voi antaa asiakkaan maksaman summan nopeasti käyttämällä setelin arvoja. Voit määrittää toimintoprofiilissa kaksi asetusta, jolla arvo näytetään myyntipisteessä.

- **Suurempi tai yhtä suuri summa erääntyy** – Myyntipiste näyttää oletusarvoisesti vain arvot, jotka ovat suurempia kuin erääntyvä summa, mikä mahdollistaa yhden kosketuksen maksuvälinetapahtuman. Jos erääntyvä summa on esimerkiksi 7,50 $, myyntipiste näyttää seuraavat arvot: 10 $, 20 $, 50 $ ja 100 $. Jonkin edellä mainitun summan koskettaminen käsittelee automaattisesti kyseisen summan myynnin. 1 ja 5 dollarin arvoja ei näytetä, koska nämä summat ovat pienempiä kuin erääntyvä summa.
- **Kaikki arvot** – Kun tämä asetus valitaan, kaikki setelin arvot näytetään aina myyntipisteessä erääntyvästä summasta riippumatta. Käyttäjä voikin määrittää erääntyvän summan käyttämällä seteliyhdistelmiä. Jos erääntyvä summa on esimerkiksi 25,00 $, käyttäjä voi viimeistellä myynnin valitsemalla 20 $ ja 5 $.


[!INCLUDE[footer-include](../includes/footer-banner.md)]