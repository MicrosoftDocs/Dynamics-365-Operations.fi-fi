---
title: Commercen esikatseluympäristön yleiskuvaus
description: Tässä ohjeaiheessa on yleiskatsaus Microsoft Dynamics 365 Commerce -esikatseluympäristössä.
author: v-chgri
manager: annbe
ms.date: 12/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: v-chgri
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 901583afde4739be5313fa129ff0e52f11326881
ms.sourcegitcommit: 610d5c3efadbaf11752b46f24680af619bcd70a6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/10/2019
ms.locfileid: "2906067"
---
# <a name="commerce-preview-environment-overview"></a>Commercen esikatseluympäristön yleiskuvaus

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa on yleiskatsaus Microsoft Dynamics 365 Commerce -esikatseluympäristössä.

## <a name="overview"></a>Yleiskatsaus

Commercen esikatseluympäristö on valinnainen Dynamics 365 Commercen päästä päähän -esikatseluympäristö, jonka avulla potentiaaliset asiakkaat voivat kokeilla Commerce-tuotetta ennen sen yleistä julkaisua yleisölle.

Lukuun ottamatta joitakin pieniä rajoituksia, jotka eivät vaikuta ominaisuuksiin tai toimintoihin, Commerce-esikatseluympäristö tarjoaa täydellisen kaupankäynnin kokemuksen, ja asiakkaat ja toteutuskumppanit voivat käyttää sitä tuotteen arviointiin, palautteen tarjoamiseen ja sopivuus- ja aukkoanalyysiin.

## <a name="limitations-of-the-commerce-preview-environment"></a>Commerce-esikatseluympäristön rajoitukset

Vaikka Commercen esiversioympäristö tarjoaa täydet Commercen ominaisuudet ja toiminnot, siinä on joitakin pieniä rajoituksia:

- Vaikka Commercen esiversioympäristössä itsessään ei ole maantieteellisiä rajoituksia, ympäristön osia, kuten Retail Cloud Scale Unit (RCSU) ja sähköisen kaupankäynnin sovelluksia voidaan valmistella vain Yhdysvalloissa.
- Commercen esikatseluympäristön käyttö on rajoitettu 30 päivään siitä päivästä, jolloin sähköinen kaupankäynti on valmisteltu.
- Commerce esikatseluympäristön voi onnistuneesti ottaa käyttöön ja alustaa vain ympäristössä, joka käyttää demotopologiaa, jossa kaikki ympäristön osat otetaan käyttöön yhdessä näennäiskoneessa (VM). Tämän OneBox VM -topologian pääasiallinen rajoitus on samanaikaisten käyttäjien määrä, jota esikatseluympäristö voi tukea.
- Commercen esikatseluympäristöä voi arvioida vain, kunnes Commerce-tuote on yleisesti saatavilla (GA). Uudet esittely-ympäristöt ovat käytettävissä GA:n jälkeen.

## <a name="get-started"></a>Aloittaminen

Katso Commercen esikatseluympäristön tarjoaminen kohdasta [Commercen esikatseluympäristön tarjoaminen](provisioning-guide.md).

## <a name="additional-resources"></a>Lisäresurssit

[Commercen esikatseluympäristön valmisteleminen](provisioning-guide.md)

[Commercen esikatseluympäristön määrittäminen](cpe-post-provisioning.md)

[Valinnaisten ominaisuuksien määrittäminen Commercen esikatseluympäristöä varten](cpe-optional-features.md)

[Commercen esikatseluympäristön usein kysytyt kysymykset](cpe-faq.md)
