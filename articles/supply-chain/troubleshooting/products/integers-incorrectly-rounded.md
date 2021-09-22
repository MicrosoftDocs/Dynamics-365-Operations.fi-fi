---
title: Kokonaisluvut pyöristetään väärin tuotemääritysmallien laskennoissa
description: Kokonaislukutuloksia ei aina pyöristetä oikein, kun tuotemääritysmalleja lasketaan. Korjaa ongelma lisätyllä desimaalimääritteellä ja laskennalla.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: b17145d7d17cb784fe11b3fbf65ddf5aa5530f27
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476247"
---
# <a name="integers-incorrectly-rounded-when-product-configuration-models-are-calculated"></a>Kokonaisluvut pyöristetään väärin, kun tuotemääritysmalleja lasketaan

## <a name="symptoms"></a>Oireet

Tämä ongelma voi esiintyä, kun seuraavat toiminnot suoritetaan:

1. Määritä tuotannon määritysmallin seuraavat määritteet:

    - Syöte (kokonaisluku)
    - Prosentti (desimaaliluku)
    - Tulos (kokonaisluku)

2. Luo laskelma, jossa on seuraava lauseke:

    *Tulos* = *Syöte* × *prosentti* ÷ 100

Tässä tapauksessa kokonaislukutulosta ei aina pyöristetä oikein. Jos syötteenä esimerkiksi on 1 000 ja prosenttiosuutena on 2,40, kokonaislukutuloksen olettaa olevan 24, koska 2,40 prosenttia 1 000:sta on 24 (tai desimaalimuodossa 24,00). Sen sijaan tuloksena näkyy 23. Kun prosenttina on sen sijaan 2,39, tulokseksi pyöristetään 24 eikä 23. Kun prosenttina on 2,50, laskelma pyöristystulos on odotettu 25.

## <a name="cause"></a>Syy

Tämä ongelma johtuu tavasta, jolla Microsoft Solver Foundation ilmaisee luvut sisäisesti murtolukuja käyttämällä. Edellisen esimerkin laskutoimituksen tulos prosentteina on 2,40, joka ilmaistaan muodossa 27021597764222975 ÷ 1125899906842624 = 23.99999999999999911182158029987476766109466552734375. Kun .NET näyttää tämän arvon kokonaislukuja, tuloksena 23.

## <a name="resolution"></a>Ratkaisu

Tätä toimintaa ei muuteta, koska muut skenaariot tarvitsevat sitä. Edellisen esimerkin ongelman voi korjata ottamalla käyttöön lisädesimaalimääritteen ja laskelmat.

Voit esimerkiksi määrittää tuotannon määritysmallin seuraavat määritteet:

- Syöte (kokonaisluku)
- Prosentti (desimaaliluku)
- ResultDecimal (desimaali)
- ResultInteger (kokonaisluku)

Voit sitten lisätä seuraavat laskelmat:

- *ResultDecimal* = *Syöte* × *Prosentti* ÷ 100
- *ResultInteger* = *ResultDecimal*
