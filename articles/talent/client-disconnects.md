---
title: Talent-asiakkaan yhteys katkeaa
description: Tässä ohjeaiheessa kerrotaan, miten toimitaan, jos asiakkaan yhteys ympäristöön katkeaa tuntemattomasta syystä.
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 4f96b986059c179268f8a96ea7e7725831a93524
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "304181"
---
# <a name="talent-client-disconnects"></a>Talent-asiakkaan yhteys katkeaa

[!include [banner](includes/banner.md)]

**Ympäristön tiedot** 

Tämä ongelma voi esiintyä kaikissa ympäristöissä.
 
**Oire** 

Asiakkaan yhteys ympäristöön katkeaa tuntemattomasta syystä. Asiakas saa jonkin seuraavista virhesanomista:

- Yhteys on katkennut. Jatka työskentelyä valitsemalla Sulje.
- Vaikuttaa siltä, että verkkoyhteys katkesi. Yritä uudelleen napsauttamalla Yritä uudelleen.

**Varoitusmerkki**

Tämä ongelma ilmenee usein silloin, kun käyttäjät ovat käyttöönottovaiheessa, kun he vertailevat tietoja eri tuotanto-ja testiympäristöistä ja kun he unohtavat, että siirtyvät istuntojen välillä. Tämä ongelma tulee esille todennäköisimmin, jos käyttäjät ovat tässä vaiheessa.

**Varasto-otto** 

**Selaintyypit:** Google Chrome, Internet Explorer ja Microsoft Edge

Microsoft Dynamics 365 for Talent -ympäristö katkaisee käyttäjien yhteyden, kun samalla käyttäjällä on samanaikaisesti avoinna samassa selaintyypissä kaksi eri istuntoa. (Esimerkki: käyttäjä A katsoo sekä ympäristöä 1 että ympäristöä 2 Chromessa.) Sillä ei ole merkitystä, onko käyttäjä avannut eri selainikkunoita tai välilehtiä. Jos samoilla käyttäjän tunnistetiedoilla kirjaudutaan samanaikaisesti samassa selaintyypissä sekä ympäristöön 1 että ympäristöön 2, Talent katkaisee yhteyden toiseen istuntoon.

**Ratkaisu**

Varmista, että kussakin selaintyypissä on aina avoinna vain yksi ympäristö. Käyttäjät voivat avata useita saman ympäristön istuntoja (eli useita välilehtiä samassa selaimessa).

Jos käyttäjät haluavat siirtyä kahden ympäristön välillä samanaikaisesti, heidän on avattavat ympäristöt eri selaintyypissä. (Esimerkki: käyttäjä A voi tarkastella ympäristöä 1 Chromessa ja ympäristöä 2 Microsoft Edgessä.)
