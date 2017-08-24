---
title: "Myyntipisteen käteisvarojen arvojen määrittäminen"
description: "Seteleiden ja kolikoiden arvot voidaan määrittää taustajärjestelmässä kassojen, myyjien ja esimiesten käyttöön myymälän myyntipisteissä."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: annbe
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 16231
ms.assetid: f28a827c-3a50-4d5e-83eb-e5a768db70a1
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: d280a11670b5887ae5ae582cedf30c093b4b5d7c
ms.openlocfilehash: 9abcbb706d7120c6bcd91fc759b33cb518802a5b
ms.contentlocale: fi-fi
ms.lasthandoff: 07/27/2017

---

# <a name="configure-cash-denominations-for-pos"></a>Myyntipisteen käteisvarojen arvojen määrittäminen

[!include[banner](includes/banner.md)]

Seteleiden ja kolikoiden arvot voidaan määrittää taustajärjestelmässä kassojen, myyjien ja esimiesten käyttöön myymälän myyntipisteissä. Näitä arvoja voidaan käyttää helpottamaan käteisvarojen laskemista, kun kassa lasketaan päivän lopussa maksuvälineittäin tai myynnin nopeassa maksuvälinetapahtumassa.

## <a name="define-denominations"></a>Arvojen määrittäminen
Myymäläkohtaiset arvot määritetään **Asetukset** > **Myymäläominaisuuden kassatilitysasetus** -sivulla. 

![käteisvarojen arvot](./media/image1-denomination.png)

Arvon määrittäminen:
1. Valitse **Uusi**.
1. Määritä tyyppi (kolikko tai seteli).
1. Määritä summa (arvo).

![käteisvarojen arvot](./media/image2-denomination.png)

## <a name="configure-the-functionality-profile"></a>Toimintoprofiilin määrittäminen
Kun myyntipisteessä maksetaan käteisellä, käyttäjä voi antaa asiakkaan maksaman summan nopeasti käyttämällä setelin arvoja. Voit määrittää toimintoprofiilissa kaksi asetusta, jolla arvo näytetään myyntipisteessä.

**Suurempi tai yhtä suuri summa erääntyy**: Myyntipiste näyttää oletusarvoisesti vain arvot, jotka ovat suurempia kuin erääntyvä summa, mikä mahdollistaa yhden kosketuksen maksuvälinetapahtuman. Jos erääntyvä summa on esimerkiksi 7,50 $, myyntipiste näyttää seuraavat arvot: 10 $, 20 $, 50 $ ja 100 $. Jonkin edellä mainitun summan koskettaminen käsittelee automaattisesti kyseisen summan myynnin. 1 ja 5 dollarin arvoja ei näytetä, koska nämä summat ovat pienempiä kuin erääntyvä summa.

**Kaikki arvot**: Kun tämä asetus valitaan, kaikki setelin arvot näytetään aina myyntipisteessä erääntyvästä summasta riippumatta. Käyttäjä voikin määrittää erääntyvän summan käyttämällä seteliyhdistelmiä. Jos erääntyvä summa on esimerkiksi 25,00 $, käyttäjä voi viimeistellä myynnin valitsemalla 20 $ ja 5 $.

