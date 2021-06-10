---
title: Kontin painon ja tilavuuden sisällyttäminen kuormaan
description: Tässä aiheessa käsitellään kuormaan konttipainon- ja tilavuuden lisäämistoiminnon määrittämistä ja käyttöä.
author: Henrikan
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TMSRateRouteWorkbench, TMSDriverLogListPage, TMSTransportationTender
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2017-09-20
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9196e9c4ce1a8aa629400b8bf379e7164a797b85
ms.sourcegitcommit: 0cc89dd42c1924ca0ec735c6566bc56b39cc5f7d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/26/2021
ms.locfileid: "6102635"
---
# <a name="include-container-weight-and-volume-on-load"></a>Kontin painon ja tilavuuden sisällyttäminen kuormaan

[!include [banner](../includes/banner.md)]

Toiminnallisuus, jolla lisätään konttipaino- ja tilavuus kuormaan antaa selkeän kuvan kuormaan lastattavien konttien ja nimikkeiden kokonaispainosta- ja tilavuudesta.

Kuorma voi sisältää yhden tai useampia lähetyksiä, ja nämä lähetykset sisältävät erilaisia nimikkeitä, jotka voivat kuulua yhteen tai useampaan myyntitilaukseen. Nimikkeet on tallennettu konttiin, ja kontit kuormataan kuormaan. Kuormassa voi olla myös kontin ulkopuolisia nimikkeitä. Järjestelmä laskee näiden ehtojen perusteella arvon kuorman painolle ja tilavuudelle ottamalla huomioon sekä konttien että nimikkeiden painot.

Jos lasketut arvot eivät ole tarkkoja, voit muokata niitä syöttämällä todelliset paino- ja tilavuusarvot kuormaan. Paino- ja tilavuusarvoja käytetään kuljetusten hallintaprosessissa. Arvoja käytetään esimerkiksi hinnan ja reitin työtilassa, jossa niillä määritetään kuormien hintaa ja reittiä; niitä käytetään myös kuljetustarjouksissa ja kuljettajan sisäänkuittauksessa.

## <a name="where-it-applies"></a>Käyttö

Kontin painon ja tilavuuden lisäämistoimintoa käytetään kuljetuksenhallintaprosesseissa, kuten hinnan ja reitin työtilassa, kuljetustarjouksissa ja kuljettajan sisäänkuittauksessa.

## <a name="how-it-is-set-up"></a>Määritysohjeet

Konttien määrä, joka tulisi ottaa huomioon kuormassa lasketaan kontin painon ja tilavuuden sekä kontin käyttöasteen perusteella.

-   Kontin painon ja tilavuuden voi määrittää kohdassa **Varastonhallinta** \> **Asetukset** \> **Kontit** \> **Konttityypit**.

-   Kontin käyttöaste valitsemalla asetetaan kohdassa **Varastonhallinta** \> **Asetukset** \> **Kontit** \> **Konttiryhmät** kirjoittamalla arvo **Kontin käyttöaste** -kenttään.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]