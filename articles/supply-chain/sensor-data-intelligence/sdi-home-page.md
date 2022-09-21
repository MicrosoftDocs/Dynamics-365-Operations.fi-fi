---
title: Sensor Data Intelligencen aloitussivu
description: Tässä artikkelissa on yleiskuvaus Sensor Data Intelligencesta. Organisaatiot voivat käyttää tätä ominaisuutta tehostaakseen Microsoft Dynamics 365 Supply Chain Managementin liiketoimintaprosesseja esineiden internetin (IoT) signaalien ja tuotannon laitteiston perusteella.
author: johanhoffmann
ms.date: 09/02/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-09-02
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: 2e4cd8d4d4ffcd10d02fbf26615f12cdd6ccca9e
ms.sourcegitcommit: 3d7ae22401b376d2899840b561575e8d5c55658c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/08/2022
ms.locfileid: "9428367"
---
# <a name="sensor-data-intelligence-home-page"></a>Sensor Data Intelligencen aloitussivu

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

Microsoft Dynamics 365 Supply Chain Managementin Sensor Data Intelligence ottaa käyttöön organisaatiot, jotka tehostavat Supply Chain Managementin liiketoimintaprosesseja esineiden internetin (IoT) signaalien ja tuotannon laitteiston perusteella. Tämä on päivitetty, uudelleennimetty versio *IoT-analyysi*-ominaisuudesta, joka oli aiemmin käytettävissä Supply Chain Managementissa.

Sensor Data Intelligencen avulla voi suorittaa seuraavia tehtäviä:

- Tietojen kerääminen koneista ja laitteista ylläpidettävän resurssin laskuriarvojen päivittämiseksi Supply Chain Managementissa sekä ennakoivan ylläpidon tehostaminen.
- Ratkaisun määrittäminen käyttämällä yksinkertaista perehdytyksen ohjattua toimintoa manuaalisen asentamisen ja komponenttien määrittämisen sijaan Microsoft Dynamics Lifecycle Services (LCS) -ratkaisussa.
- Komponenttien käyttöönotto omassa tilauksessa niin, että Azure-komponenttien hallinta on aiempaa joustavampaa.
- Ratkaisun määrittäminen, skaalaaminen ja laajentaminen liiketoimintalogiikaksi, jonka Azure-komponentit suorittavat. Näitä komponentteja hallitaan nyt omassa tilauksessasi. Tämän vuoksi ne voidaan mukauttaa vaadittavalla tavalla yksilöllisiä liiketoimintatarpeita vastaaviksi.

## <a name="business-scenarios"></a>Liiketoimintaskenaariot

Sensor Data Intelligence mahdollistaa useiden toimintotyyppien käyttämisen järjestelmässä. Jokaisella tyypillä on tietty *skenaario*. Kukin skenaario sisältää tietyn määritysjoukon asetukset järjestelmässä seuraavassa taulukossa esitetyllä tavalla.

| Skenaario | Kuvaus |
|---|---|
| [Resurssin käyttämättömyysaika](sdi-scenario-asset-downtime.md) | Voit seurata koneen resurssien tehokkuutta tarkasti käyttämällä tunnisteen tietoja koneen käyttämättömyysajan seuraamiseksi. |
| [Resurssien ylläpito](sdi-scenario-asset-maintenance.md) | Minimoi ylläpitokustannuksia ja laajenna resurssin käyttöikää parantamalla ylläpitosuunnitelmiakoneen resurssien kriittisten hallintapisteiden tunnistimien lukemien perusteella. |
| [Koneen tila](sdi-scenario-equipment-downtime.md) | Varmista toiminnon tehokkuus käyttämällä tunnistimien lukemia ja ilmoittamalla suunnittelijoille koneiden käyttökatkoista sekä antamalla vaihtoehtoja mahdollisten viiveiden vähentämiseksi. |
| [Tuotteen laatu](sdi-scenario-product-quality.md) | Varmista tuote-erien laatu vertaamalla tunnistimien lukemia kunkin tuote-erän todellisissa ominaisuuksissa, kuten kosteudessa, lämpötilassa ja mukautetuissa laatumittareissa. Järjestelmä ilmoittaa käyttäjille poikkeamista. |
| [Tuotannon viiveet](sdi-scenario-production-delays.md) | Tunnistimien lukemien avulla voit vertailla todellista ja suunniteltua syklin kestoa sekä ilmoittaa esimiehille, kun tuotanto ei ole aikataulussa. Tämän jälkeen esimiehet voivat puuttua asiaan tarvittaessa ja varmistaa, että toimintotehokkuus on paras mahdollinen. |

## <a name="architecture"></a>Arkkitehtuuri

Seuraavassa arkkitehtuurin kaaviossa on ratkaisun ja sen komponenttien yleiskatsaus.

![Sensor Data Intelligencen arkkitehtuurin kaavio.](media/sdi-architecture.png "Sensor Data Intelligencen arkkitehtuurin kaavio")
