---
title: Dynamics 365 Commerce -arviointiympäristön yleiskatsaus
description: Tässä ohjeaiheessa on yleiskatsaus Microsoft Dynamics 365 Commerce -arviointiympäristöstä.
author: v-chgri
manager: annbe
ms.date: 07/16/2020
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
ms.openlocfilehash: 25c0574e8d4502bcb846fba0ddf913d81eded87b
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4411865"
---
# <a name="dynamics-365-commerce-evaluation-environment-overview"></a>Dynamics 365 Commerce -arviointiympäristön yleiskatsaus

[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa on yleiskatsaus Microsoft Dynamics 365 Commerce -arviointiympäristöstä.

> [!NOTE]
> Commercen arviointiympäristöt eivät ole yleisesti saatavana, ja ne myönnetään kumppaneille ja asiakkaille pyyntökohtaisesti. Pyydä lisätietoja Microsoft-kumppanilta.

## <a name="overview"></a>Yleiskuvaus

Commercen arviointiympäristö on kokonaisvaltainen valinnainen Dynamics 365 Commercen ympäristö, jonka avulla kumppanit ja potentiaaliset asiakkaat voivat kokeilla Commerce-tuotetta.

Arviointiympäristöt on määritetty osittain valmiiksi, mikä vähentää valmistelun jälkeisten vaiheiden tarvetta.

Lukuun ottamatta joitakin pieniä rajoituksia, jotka eivät vaikuta ominaisuuksiin tai toimintoihin, Commercen arviointiympäristö on täydellinen Commerce-kokemus, jonka avulla asiakkaat ja toteutuskumppanit voivat arvioida tuotetta, antaa palautetta sekä tehdä sopivuus- ja aukkoanalyysiin.

## <a name="limitations-of-the-commerce-evaluation-environment"></a>Commercen arviointiympäristön rajoitukset

Vaikka Commercen arviointiympäristö sisältää täydet Commercen ominaisuudet ja toiminnot, siinä on joitakin vähäisiä rajoituksia:

- Vaikka Commercen arviointiympäristössä itsessään ei ole maantieteellisiä rajoituksia, ympäristön osia, kuten Retail Cloud Scale Unit (RCSU) ja sähköisen kaupankäynnin sovelluksia voidaan valmistella vain Yhdysvalloissa.
- Commercen arviointiympäristön käyttö on rajoitettu 30 päivään siitä päivästä, jolloin sähköinen kaupankäynti on valmisteltu.
- Commercen arviointiympäristön käyttöönotto ja alustus onnistuu vain ympäristössä, jossa käytetään demotopologiaa ja jossa kaikki ympäristön osat otetaan käyttöön yhdessä pilvessä käytettävässä virtuaalikoneessa (VM). Topologian pääasiallinen rajoitus on samanaikaisten käyttäjien määrä, jota ympäristö voi tukea.

## <a name="get-started"></a>Aloittaminen

Lisätietoja Commercen arviointiympäristön valmistelusta on kohdassa [Commercen arviointiympäristön valmisteleminen](provisioning-guide.md).

## <a name="additional-resources"></a>Lisäresurssit

[Dynamics 365 Commerce -arviointiympäristön valmisteleminen](provisioning-guide.md)

[Dynamics 365 Commerce -arviointiympäristön määritykset](cpe-post-provisioning.md)

[BOPIS:n määritykset Dynamics 365 Commerce -arviointiympäristössä](cpe-bopis.md)

[Dynamics 365 Commerce -arviointiympäristön valinnaisten ominaisuuksien määritykset](cpe-optional-features.md)

[Dynamics 365 Commerce -arviointiympäristön usein kysytyt kysymykset](cpe-faq.md)
