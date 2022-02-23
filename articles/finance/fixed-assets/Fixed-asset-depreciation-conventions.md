---
title: Käyttöomaisuuden poistomenetelmät
description: Tässä ohjeaiheessa käsitellään käyttöomaisuuden poistomenetelmiä.
author: saraschi2
manager: AnnBe
ms.date: 09/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: roschlom
ms.custom: 13891
ms.assetid: 36d1112d-921c-4fff-abe0-0ff2429848d3
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bd0153b5d735e1d565b67db6c66c854ff738509c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4969200"
---
# <a name="fixed-asset-depreciation-conventions"></a>Käyttöomaisuuden poistomenetelmät

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa käsitellään käyttöomaisuuden poistomenetelmiä. Poistomenetelmien avulla määritetään miten ja milloin poisto lasketaan sekä vuodelle, jolloin käyttöomaisuus hankitaan, että vuodelle, jolloin käyttöomaisuus poistetaan käytöstä.

Poistomenetelmät voidaan määrittää käyttöomaisuusryhmän kirjan asetuksiin. Voit tarkastella poistomenetelmää tai määrittää sen valitsemalla käyttöomaisuuden määritysalueella **Käyttöomaisuus**-ryhmät. Valitse **Kirjat**-painike. Tässä tapauksessa määritettyjä poistomenetelmiä käytetään oletusarvoina käyttöomaisuuskirjoja luotaessa. Poistomenetelmät voidaan määrittää myös yksittäiseen käyttöomaisuuskirjaan. Tee se valitsemalla käyttöomaisuuden määritysalueella ensin **Kirjat** ja sitten **Käyttöomaisuusryhmät**.

| Poistomenetelmä   | Kuvaus |
|---------------------------|-------------|
| Ei mitään                      | Käyttöomaisuuden arvonalennus alkaa <strong>Käyttöönotto</strong>-päivämääränä. |
| Puolivuosi                 | Puolivuotispoisto tehdään sekä ensimmäisenä vuonna, jolloin omaisuutta vähennetään, että viimeisenä vuotena. Koko vuoden poisto tehdään joka toinen vuosi palautuskauden aikana. |
| Täysi kuukausi                | Käyttöomaisuuden, jonka <strong>Käyttöönotto</strong>-päivämäärä on jonakin kuukauden päivänä, arvonalennus alkaa kyseisen kuun ensimmäisenä päivänä. Käyttöomaisuus katsotaan poiston kannalta käytöstä poistetuksi edellisen kuukauden viimeisenä päivänä. Sillä, minä kuukauden päivänä käytöstä poisto varsinaisesti tapahtui, ei ole merkitystä. |
| Vuosineljänneksen puoliväli               | Voit laskea poistovähennyksen sille vuodelle, jolloin omaisuus otettiin käyttöön, kertomalla koko vuoden poiston sen vuosineljänneksen prosenttiosuudella, jolloin omaisuus otettiin käyttöön. Seuraavassa taulukossa näytetään, miten se tehdään.<table><thead><tr><th>Vuosineljännes</th><th>Prosentti</th></tr></thead><tbody><tr><td>Ensimmäinen</td><td>87,5</td></tr><tr><td>Toinen</td><td>62,5</td></tr><tr><td>Kolmas</td><td>37,5</td></tr><tr><td>Neljäs</td><td>12.5</td></tr></tbody></table>Puolet poiston vuosineljänneksestä otetaan käyttöomaisuuden poiston vuosineljänneksellä (tai neljänneksellä, jolloin se poistettiin kokonaan). |
| Kuukauden puoliväli (kuukauden 1. päivä)  | Käyttöomaisuuden, jonka <strong>Käyttöönotto</strong>-päivämäärä on kuukauden ensimmäisellä puoliskolla (1.–15. päivä), arvonalennus alkaa <strong>Käyttöönotto</strong>-kuukauden ensimmäisestä päivästä. Käyttöomaisuuden, jonka <strong>Käyttöönotto</strong>-päivämäärä on kuukauden jälkimmäisellä (16. päivästä kuukauden loppuun), arvonalennus alkaa <strong>Käyttöönotto</strong>-päivämäärää seuraavan kuukauden ensimmäisestä päivästä. Kuukauden ensimmäisellä puoliskolla (1.–15. päivä) käytöstä poistettu käyttöomaisuus katsotaan poiston kannalta käytöstä poistetuksi edellisen kuukauden viimeisenä päivänä. Kuukauden jälkimmäisellä puoliskolla (16. päivästä kuukauden loppuun) käytöstä poistettu käyttöomaisuus katsotaan poiston kannalta käytöstä poistetuksi käytöstäpoistokuukauden viimeisenä päivänä. |
| Kuukauden puoliväli (kuukauden 15. päivä) | Voit laskea omaisuuden käyttöönottovuoden poistovähennyksen kertomalla koko vuoden poiston murtoluvulla. Tämän murtoluvun osoittaja (ylempi numero) on niiden kuukausien määrä vuodessa, jolloin omaisuutta on käytetty ja johon on lisätty 1/2 tai (0,5). Nimittäjä on (alempi numero) on 12. Voit poistaa ominaisuuden käytöstä ennen palautuskauden päättymistä, laske samalla menetelmällä poistovuoden poistovähennys. |
| Puolivuosi (vuoden alku) | Käyttöomaisuuden, jonka <strong>Käyttöönotto</strong>-päivämäärä on vuoden ensimmäisellä puoliskolla, arvonalennus alkaa vuoden (koko vuosi) ensimmäisenä päivänä. Käyttöomaisuuden, jonka <strong>Käyttöönotto</strong>-päivämäärä on vuoden jälkimmäisellä puoliskolla, arvonalennus alkaa vuoden puolivälissä. |
| Puolivuosi (seuraava vuosi)     | Käyttöomaisuuden, jonka <strong>Käyttöönotto</strong>-päivämäärä on vuoden ensimmäisellä puoliskolla, arvonalennus alkaa vuoden (koko vuosi) ensimmäisenä päivänä. Käyttöomaisuuden, jonka <strong>Käyttöönotto</strong>-päivämäärä on vuoden jälkimmäisellä puoliskolla, arvonalennus alkaa seuraavan vuoden ensimmäisenä päivänä. Vuoden ensimmäisellä puoliskolla käytöstä poistettu käyttöomaisuus katsotaan poiston kannalta käytöstä poistetuksi edellisen vuoden viimeisenä päivänä. Kuluvalle vuodelle kirjatut poistot on palautettava tai oikaistava ulos. Vuoden jälkimmäisellä puoliskolla käytöstä poistettu käyttöomaisuus katsotaan poiston kannalta käytöstä poistetuksi käytöstäpoistovuoden viimeisenä päivänä. |
