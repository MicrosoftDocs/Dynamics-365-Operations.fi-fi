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
ms.openlocfilehash: 074be71d7b6ec1acab6307a79e397c2a2a045c39
ms.sourcegitcommit: 8cb031501a2b2505443599aabffcfece50e01263
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/09/2021
ms.locfileid: "7778422"
---
# <a name="the-unit-and-unit-quantity-arent-working-correctly-in-the-inventory-journal"></a>Yksikkö ja yksikkömäärä eivät toimi oikein varastokirjauskansiossa

## <a name="symptoms"></a>Oireet

Jompikumpi seuraavista ongelmista tai molemmat ongelmat voivat esiintyä, kun varastokirjauskansiossa käytetään yksikköjä ja määriä:

- Yksiköt tai yksikkömäärät eivät näy varastokirjauskansiossa, kun vapautetun tuotteen muunnosyksikkö on määritetty eikä yksikköä voi muuttaa varastokirjauskansiossa.
- Vaikka **Määrä**- ja **Yksikkö**-kentät näkyvät varastokirjauskansiossa, **Yksikkömäärä**-kenttä ei näy. Jos yksikköä muutetaan, määrä annetaan ja kirjauskansio kirjataan, kirjauskansiossa näkyy edelleen kyseiseen määrän alkuperäinen mittayksikkö.

## <a name="resolution"></a>Ratkaisu

Korjaa tämä ongelma seuraavien ohjeiden mukaisesti.

1. Varmista **Ominaisuuksien hallinta** -työtilassa, että *Mittayksikköä ja yksikkömäärää käytetään varastokirjauskansioissa* -toiminto on otettu käyttöön. Tämä toiminto lisää **Yksikkö**- ja **Yksikkömäärä**-kentät kirjauskansioon. (Supply Chain Managementin versiosta 10.0.21 alkaen tämä ominaisuus on poistettu oletusarvoisesti käytöstä.)
1. Kun toiminto on otettu käyttöön, käytä **Määrä**-, **Yksikkömäärä**- ja **Yksikkö**-kenttiä seuraavasti:

    - **Määrä** – Määritä määrä käyttämällä vapautetulle tuotteelle määritettyä oletusyksikköä. Oletusyksikköä ei kuitenkaan näytetä tässä. Jos muunto on määritetty oletusyksikön ja **Yksikkö**-kentässä valitun yksikön välille, **Määrä**-kenttä päivitetään automaattisesti **Yksikkömäärä**- ja **Yksikkö**-kenttien valintojen perusteella.
    - **Yksikkömäärä** – määritä määrä käyttämällä **Yksikkö**-kentässä valittua yksikköä.
    - **Yksikkö** – valitse **Yksikkömäärä**-kentässä olevassa arvossa käytettävä yksikkö.
