---
title: Tuotteen määritystoiminnon vianmääritys
description: Tässä aiheessa käsitellään sellaisten ongelmien korjaamista, joita tuotteen määritystoiminnon käytössä voi esiintyä.
author: SmithaNataraj
ms.date: 11/04/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-11-04
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: f09ca4e69ca4bd3e87ee425c483b7a338045a0f28312a92b154fa07eb125927a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6772493"
---
# <a name="troubleshoot-the-product-configurator"></a>Tuotteen määritystoiminnon vianmääritys

Tässä aiheessa käsitellään sellaisten ongelmien korjaamista, joita tuotteen määritystoiminnon käytössä voi esiintyä.

## <a name="item-text-is-overwritten-when-i-configure-a-product-on-a-sales-order-line"></a>Nimikkeen teksti korvataan, kun tuote määritetään myyntitilauksen rivillä.

### <a name="issue-description"></a>Ongelman kuvaus

Tämä ongelma esiintyy, kun luot myyntitilauksen rivin määritettävälle nimikkeelle ja muokkaat sitten nimikkeen tekstiä. Kun määrität nimikkeen ja valitset **OK**, teksti korvataan vakiotekstillä.

### <a name="issue-resolution"></a>Ongelman ratkaisu

Tämä toiminta on tarkoituksellista. Tekstikenttä sisältää variantin nimen, joka täytetään vasta, kun rivi on määritetty. Tämän vuoksi tekstiä on muutettava vasta, kun rivi on määritetty, ei sitä ennen.

## <a name="integer-attributes-are-incorrectly-rounded-when-product-configuration-models-are-calculated"></a>Kokonaislukumääritteet pyöristetään virheellisesti, kun tuotemääritysmalleja lasketaan.

### <a name="issue-description"></a>Ongelman kuvaus

Tämä ongelma voi esiintyä, kun seuraavat toiminnot suoritetaan:

1. Määritä tuotannon määritysmallin seuraavat määritteet:

    - Syöte (kokonaisluku)
    - Prosentti (desimaaliluku)
    - Tulos (kokonaisluku)

2. Luo laskelma, jossa on seuraava lauseke:

    *Tulos* = *Syöte* × *prosentti* ÷ 100

Tässä tapauksessa kokonaislukutulosta ei aina pyöristetä oikein. Syöte on esimerkiksi 1 000 ja prosentti 2,40. Tämän vuoksi kokonaislukutuloksen odotetaan olevan 24, koska 2,40 prosenttia 1 000:sta on 24 (tai 24,00 desimaalimuodossa). Sen sijaan tuloksena näkyy 23. Kun prosenttina on sen sijaan 2,39, tulokseksi pyöristetään 24 eikä 23. Kun prosenttina on 2,50, laskelma pyöristystulos on odotettu 25.

### <a name="issue-resolution"></a>Ongelman ratkaisu

Tämä ongelma johtuu tavasta, jolla Microsoft Solver Foundation ilmaisee luvut sisäisesti murtolukuja käyttämällä. Edellisen esimerkin laskutoimituksen tulos prosentteina on 2,40, joka ilmaistaan muodossa 27021597764222975 ÷ 1125899906842624 = 23.99999999999999911182158029987476766109466552734375. Kun .NET näyttää tämän arvon kokonaislukuja, tuloksena 23.

Tätä toimintaa ei muuteta, koska muut skenaariot tarvitsevat sitä. Edellisen esimerkin ongelman voi korjata ottamalla käyttöön lisädesimaalimääritteen ja laskelman.

Voit esimerkiksi määrittää tuotannon määritysmallin seuraavat määritteet:

- Syöte (kokonaisluku)
- Prosentti (desimaaliluku)
- ResultDecimal (desimaali)
- ResultInteger (kokonaisluku)

Voit sitten lisätä seuraavat laskelmat:

- *ResultDecimal* = *Syöte* × *Prosentti* ÷ 100
- *ResultInteger* = *ResultDecimal*


[!INCLUDE[footer-include](../../includes/footer-banner.md)]