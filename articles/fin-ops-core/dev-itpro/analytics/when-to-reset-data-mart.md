---
title: Tietovaraston nollaaminen
description: Tässä aiheessa käsitellään tilanteita, joissa tietovaraston nollaamisesta voi olla apua, ja tilanteita, joissa tietovaraston nollaamisesta ei todennäköisesti ole apua.
author: jinniew
manager: AnnBe
ms.date: 12/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2020-12-15
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 1c1524c7a1a3fbe71c51b23571996d87641cdf7e
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/30/2021
ms.locfileid: "5093209"
---
# <a name="when-to-reset-a-data-mart"></a>Tietovaraston nollaaminen

Tietovaraston nollaaminen voi kestää kauan. Tämä toiminto ei välttämättä ole myöskään kaikkiin tilanteisiin sopiva ratkaisu. Tässä aiheessa käsitellään tilanteita, joissa tietovaraston nollaamisesta voi olla apua, sekä tilanteita, joissa tietovaraston nollaamisesta ei todennäköisesti ole apua.  

## <a name="when-do-you-need-to-do-a-data-mart-reset"></a>Milloin tietovarasto on nollattava?
Seuraavia kysymyksiä kannattaa pohtia ennen tietovaraston nollaamista. Jos vähintään yhteen kysymykseen vastataan myöntävästi, se voi olla osoitus siitä, että tietovaraston nollaamisesta voi olla hyötyä organisaatiolle.

- Sovellustietokanta on palautettu, mutta tietovaraston tietokantaa ei palautettu.
- Tilikauden tiedoissa on virheitä, eikä syy tähän ole raportin rakenteellinen ongelma.
- Tilikauden tiedoissa on virheitä ja raportin suunnitteluohjelman **Integroinnin tila** -sivun yritettyjen integrointien luettelossa on tietueita. (Käynnistä raportin suunnitteluohjelma ja valitset **Työkalut > Integroinnin tila**).
- Tukitapaus on avattu ja tukihenkilö on ohjeistanut nollaamaan tietovaraston vianmääritysvaiheen osana.
 
## <a name="when-its-not-appropriate-to-reset-a-data-mart"></a>Milloin tietovarastoa ei kannata nollata?
Joissakin tilanteissa tietovarastoa ei kannata nollata. Niitä ovat esimerkiksi seuraavat: 

- Nollauksen syytä ei mainita tässä aiheessa.
- Suorituskykyongelmat liittyvät tietojen synkronointiin. Tässä tilanteessa tietovaraston nollaamisesta ei ole luultavasti apua.
- Nollausmalli toistuu jonkin seuraavan syyn vuoksi: 
  - **Puuttuvat tiedot** – Sulje pois ensin raportin rakenteeseen ja tietojen synkronoinnin ajoittamiseen liittyvät ongelmat. Voit esimerkiksi huomata, että yhdistämismääritystä ei ole suoritettu puuttuvien tietojen kirjaamisen jälkeen.
  - **Juuttunut integroinnin tila** – jos integrointi tapahtuu hitaasti tai näyttää juuttuvan, tietovaraston nollaaminen ei todennäköisesti ratkaise ongelmaa.
  - **Nollaamisyritykset eivät ole onnistuneet** – jos nollaamista on yritetty useita kertoja eikä se ole onnistunut puuttuvien tietojen vuoksi, suosituksena on tukitapauksen avaaminen ja tilanteen analysointi yhdessä tukihenkilön kanssa, ennen kuin tietovaraston nollaamista yritetään seuraavan kerran.
  - **Vanhentuneet tietueet** – Tietueiden vanhentuminen ei välttämättä edellytä tietovaraston nollaamista. Jos tietovarasto on suuri, nollausprosessin suorittaminen kestää jonkin aikaa mutta tuloksena ei todennäköisesti ole parannuksia.
 
## <a name="what-a-data-mart-reset-does-not-do"></a>Tietovaraston nollaamisen ei ole vaikutusta seuraaviin  
- Nollaus käynnistyy vasta, kun nykyiset tehtävät valmistuvat. Näin varmistetaan, ettei vanhoja tietoja lisätä. Tässä vaiheessa voi avautua esimerkiksi seuraavanlainen sanoma: Tietovaraston nollausta ei voitu käsitellä aktiivisen tehtävän vuoksi. Yritä myöhemmin uudelleen.
- Nollaus poistaa integrointitehtävät käytöstä ja poistaa kaikki tietovaraston tiedot. Integrointi otetaan uudelleen käyttöön.

> [!NOTE]
> Seuraavaksi määritetään kaksi seikkaa, joita tietovaraston nollaus *ei* tee. <br>
> - Nollaukset eivät tyhjennä raportin rakenteita. <br>
> - Nollaukset eivät tyhjennä yritystietoja tai käyttäjätietoja, ellei niitä ole valittu.
