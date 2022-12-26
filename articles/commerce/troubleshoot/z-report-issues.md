---
title: Z-raportin tietojen täsmäytysongelmat
description: Tässä artikkelissa käsitellään ongelmia, joita käyttäjillä voi olla täsmäytettäessä Z-raportin tietoja Commerce headquartersissa. Siinä käsitellään myös mahdollisia pääsyitä ja ratkaisuja, jotka auttavat estämään ongelmien esiintymisen jatkossa.
author: Shajain
ms.date: 12/06/2022
ms.topic: Troubleshooting
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: shajain
ms.search.validFrom: 2021-01-31
ms.openlocfilehash: 9803134c4c77233e565525e96fd82af293d4c829
ms.sourcegitcommit: 0c927fcb3afd34d870391f05b5393a4673d916e5
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/08/2022
ms.locfileid: "9832121"
---
# <a name="issues-with-the-data-reconciliation-of-a-z-report"></a>Z-raportin tietojen täsmäytysongelmat

[!include [banner](../../includes/banner.md)]

Tässä artikkelissa on vianmääritysohjeita, joista voi olla apua Z-raportin tietojen täsmäyttämiseen liittyvissä ongelmissa Microsoft Dynamics 365 Commerce headquartersissa. Siinä käsitellään mahdollisia tietojen täsmäytyksen ongelmia, niiden pääsyitä ja ratkaisuja, joiden avulla voidaan estää ongelmien esiintyminen jatkossa.

## <a name="description"></a>kuvaus

- Z-raportissa näkyvät summat ja lasketussa laskelmassa näkyvät summat eivät vastaa toisiaan.
- Headquartersin tapahtuman rivinimikkeiden määrä on virheellinen tai rivisumma ja tapahtuman summa eivät vastaa toisiaan.
- Headquartersissa näkyvä vuoron tapahtumien määrä on pienempi kuin Z-raportissa olevien tapahtumien määrä.
- Laskelman kirjaus epäonnistui jonkin edellä mainitun syyn vuoksi.

### <a name="root-cause"></a>Pääsyy

Edellä kuvattujen oireiden yleisin pääsyy on tapahtumatunnusten kaksoiskappaleiden luonti kanavatietokannassa. Tapahtumatunnusten kaksoiskappaleita voidaan luoda seuraavista syistä:

- Modernin myyntipisteen (MPOS) paikallinen tietokantatallennus on vaurioitunut.
- Jotkin MPOS:n tapahtumat ovat offline-tilassa, ja se aktivoidaan uudelleen käyttämällä tiliä, jolla ei ole offline-tietokannan käyttöoikeutta.
- Mukauttamisessa on tapahtumatunnusten luontiin liittyvä ongelma.

## <a name="resolution"></a>Ratkaisu

Yleensä Commerce luo peräkkäisiä tapahtumatunnuksia numerosarjojen perusteella. Jos järjestelmä ei voi jostain syystä päätellä, mitä numerosarjaa on käytetty, tapahtumatunnuksen kaksoiskappale luodaan. 

Tapahtumatunnusten kaksoiskappaleisiin liittyvä ongelma ratkaistaan luomalla tukipalvelupyyntö, jolla tarkistetaan, voidaanko tapahtumatiedot korjata. Joissakin tapauksissa tietojen korjaaminen ei ole mahdollista tai sitä tarvita, kuten silloin jos tietoja ei ole menetetty headquartersissa.

Tämä ongelma voidaan estää jatkossa ottamalla käyttöön **Ota uusi tapahtumatunnus käyttöön tapahtumatunnusten kaksoiskappaleiden välttämiseksi** -ominaisuus headquartersissa. Tämä ominaisuus otettiin käyttöön Commercen versiossa 10.0.19. Se auttaa estämään peräkkäisten tapahtumatunnusten luomisen varmistamalla, että kullekin tapahtumalle luodaan yksilöivä tapahtumatunnus. Lisätietoja tästä ominaisuudesta on kohdassa [Tapahtumatunnusten kaksoiskappaleiden estäminen](../channel-setup-retail.md#ensure-unique-transaction-ids).
