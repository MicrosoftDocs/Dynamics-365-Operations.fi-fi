---
title: Yksikkö ja yksikkömäärä eivät toimi oikein varastokirjauskansiossa
description: Yksikkö ja yksikkömäärä eivät toimi oikein varastokirjauskansiossa
author: sherry-zheng
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 39f462ae325aa1104a25a8290daed70388e624ec
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476209"
---
# <a name="the-unit-and-unit-quantity-arent-working-correctly-in-the-inventory-journal"></a>Yksikkö ja yksikkömäärä eivät toimi oikein varastokirjauskansiossa

## <a name="symptoms"></a>Oireet

Jompikumpi seuraavista ongelmista tai molemmat ongelmat voivat esiintyä, kun varastokirjauskansiossa käytetään yksikköjä ja määriä:

- Yksiköt tai yksikkömäärät eivät näy varastokirjauskansiossa, kun vapautetun tuotteen muunnosyksikkö on määritetty eikä yksikköä voi muuttaa varastokirjauskansiossa.
- Vaikka **Määrä**- ja **Yksikkö**-kentät näkyvät varastokirjauskansiossa, **Yksikkömäärä**-kenttä ei näy. Jos yksikköä muutetaan, määrä annetaan ja kirjauskansio kirjataan, kirjauskansiossa näkyy edelleen kyseiseen määrän alkuperäinen mittayksikkö.

## <a name="resolution"></a>Ratkaisu

Korjaa tämä ongelma seuraavien ohjeiden mukaisesti.

1. Varmista **Ominaisuuksien hallinta** -työtilassa, että *Mittayksikköä ja yksikkömäärää käytetään varastokirjauskansioissa* -toiminto on otettu käyttöön. Tämä toiminto lisää **Yksikkö**- ja **Yksikkömäärä**-kentät kirjauskansioon.
1. Kun toiminto on otettu käyttöön, käytä **Määrä**-, **Yksikkömäärä**- ja **Yksikkö**-kenttiä seuraavasti:

    - **Määrä** – Määritä määrä käyttämällä vapautetulle tuotteelle määritettyä oletusyksikköä. Oletusyksikköä ei kuitenkaan näytetä tässä. Jos muunto on määritetty oletusyksikön ja **Yksikkö**-kentässä valitun yksikön välille, **Määrä**-kenttä päivitetään automaattisesti **Yksikkömäärä**- ja **Yksikkö**-kenttien valintojen perusteella.
    - **Yksikkömäärä** – määritä määrä käyttämällä **Yksikkö**-kentässä valittua yksikköä.
    - **Yksikkö** – valitse **Yksikkömäärä**-kentässä olevassa arvossa käytettävä yksikkö.
