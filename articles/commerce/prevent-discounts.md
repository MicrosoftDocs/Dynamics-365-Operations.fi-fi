---
title: Vaihtoehdot vähittäismyyntituotteiden alennusten estämiselle
description: Jälleenmyyjillä voi olla erilaisia syitä, miksi he haluavat estää joidenkin tuotteiden hintojen alentamisen joko kampanjan tai myyntipisteellä tapahtuvan myynnin aikana.
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailPeriodicDiscount
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 85183
ms.assetid: e8c5a24f-7edd-4fd6-af80-5e0ac9f03127
ms.search.region: Global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 6a683ffce487dc4388711ad160c2e8dc55a690dd
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4411901"
---
# <a name="options-for-preventing-discounts-for-retail-products"></a>Vaihtoehdot vähittäismyyntituotteiden alennusten estämiselle

[!include [banner](includes/banner.md)]

Jälleenmyyjillä voi olla erilaisia syitä, miksi he haluavat estää joidenkin tuotteiden hintojen alentamisen joko kampanjan tai myyntipisteellä tapahtuvan myynnin aikana.

Seuraavat asetukset sijaitsevat vapautettujen tuotteiden **Commerce**-välilehdissä, ja niiden avulla tuote voidaan määrittää estämään kaikki alennukset tai manuaaliset alennukset. Asetukset voidaan määrittää myös luokkahierarkian luokkatasolla.

- **Estä kaikki alennukset** – Valitse tämä asetus, jos haluat estää kaikenlaisten alennusten käytön tässä tuotteessa. Esto koskee kampanjoita, kuten yhdistelmä- ja määräalennuksia sekä alennuksia rajan ylittyessä, samoin kuin manuaalisia rivi- ja tapahtuma-alennuksia, joita myyntipisteen käyttäjä käyttää myyntitapahtuman aikana.
- **Estä manuaaliset alennukset** – Valitse tämä asetus, jos haluat estää vain manuaaliset rivi- tai tapahtuma-alennukset, joita myyntipisteen käyttäjä käyttää myyntitapahtuman aikana. Tuotteissa, joissa tämä asetus on valittu, voidaan edelleen käyttää kampanja-alennuksia, kuten yhdistelmä- ja määräalennuksia sekä alennuksia rajan ylittyessä.

> [!NOTE]
> Nämä asetukset eivät rajoita hinnan ohitustoimintoa, koska se määrittää perushinnan, jota ei pidetä alennuksena.

[![Estä alennukset -kenttä](./media/prevent-discounts.png)](./media/prevent-discounts.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]