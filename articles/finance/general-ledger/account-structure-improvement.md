---
title: Tilirakenteen aktivoinnin suorituksen parannus
description: Tässä artikkelissa selitetään tilirakenteen aktivointiprosessin uusi suorituskykyparannus.
author: RyanCCarlson2
ms.date: 10/31/2022
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: rcarlson
ms.search.validFrom: 2022-10-08
ms.dyn365.ops.version: 10.0.31
ms.openlocfilehash: 42f8fcebba6465261489f74a9bb1dd46c2d5fa16
ms.sourcegitcommit: c6c2486be2359bd30106f7f52bda788239147d8c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/22/2022
ms.locfileid: "9713996"
---
# <a name="account-structure-activation-performance-enhancement"></a>Tilirakenteen aktivoinnin suorituksen parannus

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

Tämä suorituskykyparannuksen ansiosta voit nopeuttaa tilirakenteiden aktivoimista suorittamalla useita tapahtumapäivityksiä samanaikaisesti. Lisäksi itse rakenne merkitään aktiiviseksi sen vahvistamisen jälkeen, ja tapahtumien käsittelyä voi jatkaa sillä välin, kun aiemmin luotuja kirjaamattomia tapahtumia päivitetään uuteen rakenteeseen. Koska tapahtumapäivitykset voivat kestää jonkin aikaa, voit seurata aktivoinnin tilaa valitsemalla **Tilirakenteet**-sivun ruudukon yläpuolella olevan **Näytä aktivoinnin tila** ‑valintaruudun. Voit myös tarkastella aktivoinnin tilaa valitsemalla toimintoruudusta **Näytä** ja valitsemalla sitten avattavasta valikosta **Aktivoinnin tila**.

[![Tilirakenteet-sivu](./media/AccountStructure1.png)](./media/AccountStructure1.png)

Kun olet valinnut **Näytä aktivoinnin tila**, näyttöön tulee valintaikkuna, jossa näkyvät aktivointiprosessin osana käynnissä olevat yksittäiset tehtävät. Valintaikkunassa voit nähdä kunkin tehtävän tilan sekä tehtävän valmistumisen jälkeen sen valmistumispäivämäärän ja ‑ajan.

[![Tilirakenteen aktivoinnin aikajana.](./media/AccountStructureTimeline.png)](./media/AccountStructureTimeline.png)

## <a name="account-structure-activation-tips"></a>Tilirakenteen aktivointia koskevia vinkkejä

Tilirakenteen aktivoinnin valintaikkunassa, joka tulee näkyviin, kun valitset tilirakenneluonnokselle **Aktivoi**, on välilehtiosa nimeltä **Päivitä kirjaamattomat tapahtumat**. Tässä osassa on asetus nimeltä **Pakota päivitys**. Valitsemalla tämän vaihtoehdon voit päivittää kaikki kirjaamattomat tapahtumat nykyiseen rakenteeseen. Käytä tätä vaihtoehtoa kuitenkin vain, kun on tapahtunut virhe tai Microsoftin tuki on ohjeistanut sinua käyttämään sitä.

Seuraavassa on joitakin tekijöitä, jotka voivat vaikuttaa aktivointiprosessin suorituskykyyn:

- Suuri määrä kirjaamattomia kirjauskansiotietueita
- Suuri määrä avoimen lähdekoodin asiakirjatietueita, kuten vapaatekstilaskuja, toimittajien laskuja ja muita asiakirjoja, jotka käyttävät avoimen lähdekoodin asiakirjakehystä ja joilla on avoimia kirjanpidollisia jakoja
- TaxUncommitted-kohteessa olevien tietojen määrä
- Avoimien budjettitietojen määrä
- Kirjauskansion tietojen tuonti aktivointitehtävien ollessa yhä käynnissä

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
