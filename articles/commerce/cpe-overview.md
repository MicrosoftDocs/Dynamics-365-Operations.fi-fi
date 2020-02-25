---
title: Dynamics 365 Commercen esikatseluympäristön yleiskuvaus
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
ms.openlocfilehash: 1ff96aeb5963df9ddee56783a089dad129bbb71c
ms.sourcegitcommit: 4ed1d8ad8a0206a4172dbb41cc43f7d95073059c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/04/2020
ms.locfileid: "3024680"
---
# <a name="dynamics-365-commerce-preview-environment-overview"></a>Dynamics 365 Commercen esikatseluympäristön yleiskuvaus


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

[Dynamics 365 Commercen esiversioympäristön valmistelu](provisioning-guide.md)

[Dynamics 365 Commercen esikatseluympäristön määrittäminen](cpe-post-provisioning.md)

[Valinnaisten ominaisuuksien määrittäminen Dynamics 365 Commercen esikatseluympäristöä varten](cpe-optional-features.md)

[Dynamics 365 Commerce -esikatseluympäristön usein kysytyt kysymykset](cpe-faq.md)
