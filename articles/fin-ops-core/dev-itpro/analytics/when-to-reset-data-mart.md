---
title: Tietovaraston nollaaminen
description: Tässä aiheessa käsitellään tilanteita, joissa tietovaraston nollaamisesta voi olla apua, ja tilanteita, joissa tietovaraston nollaamisesta ei todennäköisesti ole apua.
author: jinniew
ms.date: 05/06/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2021-05-06
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: bc2c4ee490f3bebd6e7c91609a06f8dfedfcb628
ms.sourcegitcommit: 5916ea2a94ab9af7aac21f0fc44e194d5ce82917
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/07/2021
ms.locfileid: "5988989"
---
# <a name="when-to-reset-a-data-mart"></a>Tietovaraston nollaaminen

Tietovaraston nollaaminen voi kestää kauan. Tämä toiminto ei välttämättä ole myöskään kaikkiin tilanteisiin sopiva ratkaisu. Tässä aiheessa käsitellään tilanteita, joissa tietovaraston nollaamisesta voi olla apua, sekä tilanteita, joissa tietovaraston nollaamisesta ei todennäköisesti ole apua.  

## <a name="when-do-i-need-to-do-a-data-mart-reset"></a>Milloin tietovarasto on nollattava?
Seuraavia kysymyksiä kannattaa pohtia ennen tietovaraston nollaamista. Jos vähintään yhteen kysymykseen vastataan myöntävästi, se voi olla osoitus siitä, että tietovaraston nollaamisesta voi olla hyötyä organisaatiolle.

- Palautettiinko sovellustietokanta?
- Onko tukitapaus avattu ja tukihenkilö on ohjeistanut nollaamaan tietovaraston vianmääritysvaiheen osana?
 
## <a name="when-is-it-not-appropriate-to-reset-a-data-mart"></a>Milloin tietovarastoa ei kannata nollata?
Joissakin tilanteissa tietovarastoa ei kannata nollata. Niitä ovat esimerkiksi seuraavat: 

- Sinulla on suorituskykyongelmia, jotka liittyvät tietojen synkronointiin. 
- Nollausmalli toistuu jonkin seuraavan syyn vuoksi: 
  - **Puuttuvat tiedot** 
  - **Juuttunut integroinnin tila** 
  - **Vanhentuneet tietueet** – Tietueiden vanhentuminen ei välttämättä edellytä tietovaraston nollaamista. Jos tietovarasto on suuri, nollausprosessin suorittaminen kestää jonkin aikaa mutta tuloksena ei todennäköisesti ole parannuksia.
 
## <a name="what-is-a-data-mart-reset"></a>Mikä on tietovaraston osajoukon palauttaminen?
- Nollaus käynnistyy vasta, kun nykyiset tehtävät valmistuvat. Näin varmistetaan, ettei vanhoja tietoja lisätä. Tässä vaiheessa voi avautua esimerkiksi seuraavanlainen sanoma: Tietovaraston nollausta ei voitu käsitellä aktiivisen tehtävän vuoksi. Yritä myöhemmin uudelleen.
- Nollaus poistaa integrointitehtävät käytöstä ja poistaa kaikki tietovaraston tiedot. Integrointi otetaan uudelleen käyttöön.

## <a name="if-i-reset-the-data-mart-will-i-lose-reports-that-ive-already-designed"></a>Jos tietovaraston osajoukko palautetaan, menetetäänkö jo suunnitellut raportit? 
Ei, raportit tallennetaan SQL-tauluihin, joihin tietovaraston osajoukon nollaaminen ei vaikuta. Jos olet huolissasi suunnittelemiesi raporttien menettämisestä, voit varmuuskopioida mallit, joita et halua menettää. Voit varmuuskopioida ne avaamalla Report Designerin ja valitsemalla **Yritys > Yritykset > Rakenneosat > Vie**.
 
## <a name="is-it-necessary-for-all-users-to-exit-the-system-to-reset-the-data-mart"></a>Onko kaikkien käyttäjien tarpeen poistua järjestelmästä tietovaraston osajoukon nollaamiseksi?
Ei, käyttäjät voivat jatkaa järjestelmässä työskentelyä tietovaraston osajoukon nollaamisen aikana. He eivät kuitenkaan voi käyttää Financial Reporterilla luotuja raportteja, ennen kuin nollaus on valmis. 

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
