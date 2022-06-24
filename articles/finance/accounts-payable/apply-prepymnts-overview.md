---
title: Ennakkomaksujen kohdistaminen automaattisesti toimittajan laskuihin
description: Tässä artikkelissa kuvataan ennakkomaksujen automattisen toimittajan laskuihin kohdistamisen ominaisuus.
author: sunfzam
ms.date: 10/19/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-08-30
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: 547573d187460a900df7f4927ac062bd9d456729
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8900068"
---
# <a name="automatically-apply-to-vendor-invoices"></a>Automaattinen kohdistaminen toimittajan laskuihin

[!include [banner](../includes/banner.md)]

Tässä artikkelissa kuvataan ennakkomaksujen automattisen toimittajan laskuihin kohdistamisen ominaisuus. Ostotilaukselle voidaan luoda ennakkomaksu osana ostosopimusta. Kun toimittajan lasku on vastaanotettu, ennakkomaksua voidaan käyttää toimittajan laskun ostoreskontran tilittämiseen. Uuden ominaisuuden ansiosta järjestelmä voi automaattisesti käyttää toimittajan laskun numeroita ostotilauksessa vastaavien ennakkomaksujen hakemiseen, kun toimittajan lasku tuodaan.

Jos ennakkomaksuja löytyy ja niitä voidaan käyttää, olemassa oleviin laskuriveihin lisätään rivejä niitä varten. Ennakkomaksurivejä ei koskaan oteta huomioon laskun täsmäytysprosessissa.

Seuraavissa kohdissa kuvaillaan, miten ennakkomaksuja käytetään, kun noudatetaan eri ostoprosesseja:

- **Yksi toimittajan lasku ostotilausta kohden** – Ostotilauksen ennakkomaksua sovelletaan toimittajan laskuun.
- **Yksi toimittajan lasku useaa ostotilausta kohden** – Kaikkien ostotilausten ennakkomaksuja sovelletaan toimittajan laskuun.
- **Useita toimittajan laskuja ostotilausta kohden** – Ostotilauksen ennakkomaksua sovelletaan ensimmäisenä tuotuun toimittajan laskuun. Jos ennakkomaksun summa ylittää laskun summan, ennakkomaksun soveltaminen epäonnistuu, jolloin ennakkomaksu on määritettävä manuaalisesti.
- **Useita toimittajan laskuja useille ostotilauksille** – Ostotilausten ennakkomaksuja sovelletaan ensimmäiseen merkitykselliseen toimittajan laskuun. Jos ennakkomaksun summa ylittää laskun summan, ennakkomaksun soveltaminen epäonnistuu, jolloin ennakkomaksut on määritettävä manuaalisesti. Jos ennakkomaksujen ensimmäiseen laskuun kohdistamisen jälkeen on jäljellä ennakkomaksuja, ne voidaan kohdistaa seuraaviin laskuihin.

Jos ennakkomaksun käyttö epäonnistuu, **Estä seurannan automaattinen prosessi ennakkomaksun kohdistusvirheen sattuessa** -asetus määrittää seuraavat vaiheet:

- **Kyllä** – Virhesanoma Ennakkomaksun automattinen kohdistus: epäonnistui lisätään automaatiohistoriaan, ja lasku jää odottavien toimittajien laskujen luetteloon. Lasku pysyy estettynä, kunnes kohdistat ennakkomaksun manuaalisesti.

Manuaalista ennakkomaksujen kohdistusta varten on siirryttävä odottavaan laskuun. Määritä **Laskun tiedot** -sivulla **Sisällytä automaattiseen käsittelyyn** -asetuksen arvoksi estetyn laskun osalta **Ei**. Nyt voit kohdistaa ennakkomaksun manuaalisesti. Kun ennakkomaksu on kohdistettu, palauta **Sisällytä automaattiseen käsittelyyn** -asetuksen arvoksi **Kyllä**, jotta lasku voidaan käsitellä automaattisesti.

Voit myös ohittaa ennakkomaksun automaattisen kohdistuksen määrittämällä **Sisällytä automaattiseen käsittelyyn** -asetuksen arvoksi **Ei** ja palauttamalla sen arvoksi **Kyllä**. Saat seuraavan sanoman: Ostotilaukselle on jo olemassa ennakkomaksu. Haluatko ohittaa sen valitussa toimittajan laskussa? Valitse **Kyllä**. Sanoma Ennakkomaksun kohdistus ohitettu manuaalisesti lisätään automaatiohistoriaan, ja toimittajan lasku ei ole estettynä, kun automaattinen käsittely suoritetaan uudelleen.

- **Ei** – Seuranta-automaation prosessit jatkuvat. Voit silti kohdistaa ennakkomaksun tilityksen yhteydessä.
