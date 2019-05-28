---
title: Poistojen vaikutukset ja peruutukset
description: Tässä artikkelissa kuvataan käyttöomaisuustapahtuman peruuttamisen mahdolliset vaikutukset.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTrans
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 2961
ms.assetid: 63a3ac92-c321-4379-a86a-b1b14915f340
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d624fa998329680d9fa471fa325f6fcfd3920c6a
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/15/2019
ms.locfileid: "1556292"
---
# <a name="depreciation-effects-with-reversals"></a>Poistojen vaikutukset ja peruutukset

[!include [banner](../includes/banner.md)]

Tässä artikkelissa kuvataan käyttöomaisuustapahtuman peruuttamisen mahdolliset vaikutukset. 

Voit palauttaa käyttöomaisuustapahtumia sekä kyseiseen käyttöomaisuuserään liittyviä tapahtumia. Voit myös peruuttaa palautetun tapahtuman. 

Voit peruuttaa tai palauttaa tapahtuman, joka ei ollut viimeisin omaisuuden kirjaan kirjattu tapahtuma. Määritä ensin, onko poistotapahtumia kirjattu peruutettavan tapahtuman jälkeen. Tämä johtuu siitä, että poistoa ei lasketa uudelleen, kun palautat tapahtuman. Niinpä poisto jää usein liian suureksi tai liian pieneksi peruutuksen jälkeen, kuten esimerkeissä osoitetaan. 

Voit varmistaa, että poiston määrä säilyy oikeana tapahtumaa palautettaessa, kun et jatka palautustoimintoa, jos näyttöön tulee sanoma, jonka mukaan poistoa ei lasketa uudelleen. Palauta sen sijaan ensin poistotapahtuma, joka on kirjattu palautettavan tapahtuman jälkeen, ja jatka sitten tapahtuman palautusta. Tällöin järjestelmä ei varoita poiston uudelleenlaskennasta ja voit jatkaa palautusta. 

Seuraavissa esimerkeissä kuvataan laskutoimitukset, joita käytetään, jos jatkat varoitussanomasta huolimatta etkä palauta ensin poistotapahtumia.

## <a name="example-1-depreciation-is-overstated"></a> Esimerkki 1: Poisto raportoidaan liian suureksi
Käyttöomaisuuserälle määritetään viiden vuoden käyttöikä ja tasapoistomenetelmä (60 poistokautta). Tässä esimerkissä poisto raportoidaan liian suureksi.
#### <a name="asset-transaction-history"></a>Käyttöomaisuushistoria

| Päivämäärä       | Tapahtumatyyppi                                                          | Summa                                    |
|------------|---------------------------------------------------------------------------|-------------------------------------------|
| 1. tammikuuta  | Hankinta                                                               | 59 000,00                                 |
| 1. tammikuuta  | Hankintaoikaisu                                                    | 1 000,00                                  |
| 31. tammikuuta | Poisto (luodaan yhden poistokauden ehdotuksen avulla) | 1 000,00Laskelma: kirjanpitoarvo (59 000 + 1 000) / jäljellä olevien poistokausien lukumäärä (60) |

#### <a name="reversal-action"></a>Peruutustapahtuma

| Päivämäärä      | Tapahtumatyyppi                | Summa    |
|-----------|---------------------------------|-----------|
| 1. tammikuuta | Hankintaoikaisun peruutus | -1 000,00 |

#### <a name="depreciation-effect"></a>Poiston vaikutus

| Päivämäärä        | Tapahtumatyyppi        | Summa                                                                                |
|-------------|-------------------------|---------------------------------------------------------------------------------------|
| 28. helmikuuta | Poisto (ehdotus) | 983,05Laskelma: kirjanpitoarvo (59 000 - 1 000:n poisto) / jäljellä olevien poistokausien lukumäärä (59) |

Poisto raportoidaan 16,95 yksikköä liian suureksi (1000 - 983,05).

## <a name="example-2-depreciation-is-understated"></a> Esimerkki 2: Poisto raportoidaan liian pieneksi
Käyttöomaisuuserälle määritetään viiden vuoden käyttöikä ja tasapoistomenetelmä (60 poistokautta). Tässä esimerkissä poisto raportoidaan liian pieneksi.
#### <a name="asset-transaction-history"></a>Käyttöomaisuushistoria

| Päivämäärä       | Tapahtumatyyppi                                                          | Summa                                      |
|------------|---------------------------------------------------------------------------|---------------------------------------------|
| 1. tammikuuta  | Hankinta                                                               | 59 000,00                                   |
| 1. tammikuuta  | Kirjanpitoarvon alennus                                                     | 1 000,00                                    |
| 31. tammikuuta | Poisto (luodaan yhden poistokauden ehdotuksen avulla) | 966,67Laskelma: Kirjanpitoarvo (59 000 - 1 000) / jäljellä olevien poistokausien lukumäärä (60) |

#### <a name="reversal-action"></a>Peruutustapahtuma

| Päivämäärä      | Tapahtumatyyppi               | Summa    |
|-----------|--------------------------------|-----------|
| 1. tammikuuta | Kirjanpitoarvon alennuksen peruutus | -1 000,00 |

#### <a name="depreciation-effect"></a>Poiston vaikutus

| Päivämäärä        | Tapahtumatyyppi        | Summa                                                                                       |
|-------------|-------------------------|----------------------------------------------------------------------------------------------|
| 28. helmikuuta | Poisto (ehdotus) | 983,62Laskelma: Kirjanpitoarvo (59 000 - 966,67:n poisto) / jäljellä olevien poistokausien lukumäärä (59) |

Poisto raportoidaan 16,95 yksikköä liian pieneksi (983,62 - 966,67).



<a name="additional-resources"></a>Lisäresurssit
--------

[Käyttöomaisuuden poisto](fixed-asset-depreciation.md)



