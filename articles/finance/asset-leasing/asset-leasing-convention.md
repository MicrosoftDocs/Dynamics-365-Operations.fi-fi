---
title: Resurssien vuokrauksen käytännöt
description: Tässä ohjeaiheessa käsitellään vuokratun käyttöomaisuuden menetelmiä.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLease
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2021-1-28
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 5e0aabce46e47079b754b8ac674b205cf00b5e26
ms.sourcegitcommit: 04e6c1c9400e1b582180cf3e0e4767434e736c26
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/05/2022
ms.locfileid: "8711027"
---
# <a name="asset-leasing-conventions"></a>Resurssien vuokrauksen käytännöt

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Tässä ohjeaiheessa käsitellään vuokratun käyttöomaisuuden menetelmiä. Vuokramenetelmien avulla määritetään vuokrakirjan aloitusaika. Jos vuokramenetelmäksi on määritetty **Ei mitään**, aloitupäivämäärä on sama kuin vuokran alkamispäivämäärä (**Vuokran alkamispäivämäärä** -kentän arvo). Jos vuokramenetelmäksi määritetään **Täysi kuukausi**, aloituspäivä on sen kuukauden ensimmäinen päivä, johon vuokra alkaminen sijoittuu.

Aloituspäivä määrittää velan kuoletuksen ja käyttöomaisuuden poistoaikataulujen kauden alkamispäivämäärän. Korkokulut ja poistokulut kirjataan vastaavien aikataulujen kauden päättymispäivänä. Alkuperäinen kirjaus ja oikaisukirjauskansion kirjaus kirjataan aloituspäivänä.

> [!NOTE]
> Vuokramenetelmien ominaisuus voidaan ottaa käyttöön ominaisuuksien hallinnan avulla. Etsi ja valitse **Ominaisuuksien hallinta** -työtilassa toiminto, jonka nimi on **Käyttöomaisuuden vuokrauksen vuokramenetelmät** ja valitse sitten **Ota käyttöön nyt**.

Vuokramenetelmät liitetään vuokrakäyttöomaisuuskirjan asetuksiin.

Voit tarkastella tai määrittää vuokramenetelmän noudattamalla näitä vaiheita.

1. Siirry kohtaan **Resurssin vuokraus \> Asetukset \> Vuokrasopimuskirjat**.
2. Valitse **Vuokramenetelmä** -kentästä jokin seuraavista arvoista.

    | Leasing-käytäntö | kuvaus |
    |--------------------|-------------|
    | None               | Velan kuoletuksen ja käyttöomaisuuden poistosuunnitelmat alkavat vuokrauksen alkamispäivämääränä, koska aloituspäivä on sama kuin vuokrauksen alkamispäivämäärä. Päättymispäivä on kuukautta myöhempi. Tämä vuokramenetelmä ei takaa, että korko kirjataan kunkin kuukauden viimeisenä päivänä. |
    | Täysi kuukausi         | Jos vuokralla on alkamispäivämäärä, joka tapahtuu milloin tahansa kuukauden aikana, velan kuoletuksen ja käyttöomaisuuden poistosuunnitelmat alkavat kerryttää kuluja kyseisen kuukauden ensimmäisenä päivänä. Tämä vuokramenetelmä varmistaa, että korkoa kertyy kunkin kuukauden viimeisenä päivänä koko kuukaudelle. |

3. Valitse **Tallenna**.

Kun vuokra luodaan, kunkin kirjan aloituspäivä lisätään automaattisesti vuokralle syötettyyn alkamispäivämäärään ja kirjalle määritettyyn vuokramenetelmään.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
