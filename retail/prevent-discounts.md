---
title: "Vähittäismyyntituotteiden alennusten estäminen"
description: "Jälleenmyyjillä voi olla erilaisia syitä, miksi he haluavat estää joidenkin tuotteiden hintojen alentamisen joko kampanjan tai myyntipisteellä tapahtuvan myynnin aikana."
author: jeffbl
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 85183
ms.assetid: e8c5a24f-7edd-4fd6-af80-5e0ac9f03127
ms.search.region: Global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: c124ecf104bdb3de786c9dd98c2b07a4c9c04041
ms.openlocfilehash: 0debfe984a83295dde145fe4b8c2deb836345cd6
ms.contentlocale: fi-fi
ms.lasthandoff: 07/31/2017

---

# <a name="prevent-discounts-for-retail-products"></a>Vähittäismyyntituotteiden alennusten estäminen

[!include[banner](includes/banner.md)]

Jälleenmyyjillä voi olla erilaisia syitä, miksi he haluavat estää joidenkin tuotteiden hintojen alentamisen joko kampanjan tai myyntipisteellä tapahtuvan myynnin aikana.

Seuraavat asetukset sijaitsevat vapautettujen tuotteiden **Vähittäismyynti**-välilehdissä, ja niiden avulla tuote voidaan määrittää estämään kaikki alennukset tai manuaaliset alennukset. Asetukset voidaan määrittää myös vähittäismyynnin luokkahierarkian luokkatasolla.

**Estä kaikki alennukset**: Valitse tämä asetus, jos haluat estää kaikenlaisten alennusten käytön tässä tuotteessa. Esto koskee kampanjoita, kuten yhdistelmä- ja määräalennuksia sekä alennuksia rajan ylittyessä, samoin kuin manuaalisia rivi- ja tapahtuma-alennuksia, joita myyntipisteen käyttäjä käyttää myyntitapahtuman aikana.

**Estä manuaaliset alennukset**: Valitse tämä asetus, jos haluat estää vain manuaaliset rivi- tai tapahtuma-alennukset, joita myyntipisteen käyttäjä käyttää myyntitapahtuman aikana. Tuotteissa, joissa tämä asetus on valittu, voidaan edelleen käyttää kampanja-alennuksia, kuten yhdistelmä- ja määräalennuksia sekä alennuksia rajan ylittyessä.

**Huomautus**: nämä asetukset eivät rajoita hinnan ohitustoimintoa, koska se määrittää perushinnan, jota ei pidetä alennuksena.  

![estä alennukset -kenttä](/media/prevent-discounts.png)
