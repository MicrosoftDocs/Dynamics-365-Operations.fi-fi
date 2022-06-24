---
title: Asiakasohjelma katkaisee yhteyden
description: Tässä artikkelissa käsitellään toimintaa, jos asiakkaan yhteys ympäristöön katkeaa.
author: twheeloc
ms.date: 08/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 40605fd14384dbeed933057621d0160b698c938a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8869862"
---
# <a name="client-disconnects"></a>Asiakasohjelma katkaisee yhteyden


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

**Ympäristön tiedot** 

Tämä ongelma voi esiintyä kaikissa ympäristöissä.
 
**Oire** 

Asiakkaan yhteys ympäristöön katkeaa tuntemattomasta syystä. Asiakas saa jonkin seuraavista virhesanomista:

- Yhteys on katkennut. Jatka työskentelyä valitsemalla Sulje.
- Vaikuttaa siltä, että verkkoyhteys katkesi. Yritä uudelleen napsauttamalla Yritä uudelleen.

**Varoitusmerkki**

Tämä ongelma ilmenee usein silloin, kun käyttäjät ovat käyttöönottovaiheessa, kun he vertailevat tietoja eri tuotanto-ja testiympäristöistä ja kun he unohtavat, että siirtyvät istuntojen välillä. Tämä ongelma tulee esille todennäköisimmin, jos käyttäjät ovat tässä vaiheessa.

**Lähetä** 

**Selaintyypit:** Google Chrome, Internet Explorer ja Microsoft Edge

Microsoft Dynamics 365 Human Resources katkaisee käyttäjien yhteyden, kun samalla käyttäjällä on samanaikaisesti avoinna samassa selaintyypissä kaksi eri istuntoa. (Esimerkki: käyttäjä A katsoo sekä ympäristöä 1 että ympäristöä 2 Chromessa.) Sillä ei ole merkitystä, onko käyttäjä avannut eri selainikkunoita tai välilehtiä. Jos samoilla käyttäjän tunnistetiedoilla kirjaudutaan samanaikaisesti samassa selaintyypissä sekä ympäristöön 1 että ympäristöön 2, Human Resources katkaisee yhteyden toiseen istuntoon.

**Ratkaisu**

Varmista, että kussakin selaintyypissä on aina avoinna vain yksi ympäristö. Käyttäjät voivat avata useita saman ympäristön istuntoja (eli useita välilehtiä samassa selaimessa).

Jos käyttäjät haluavat siirtyä kahden ympäristön välillä samanaikaisesti, heidän on avattavat ympäristöt eri selaintyypissä. (Esimerkki: käyttäjä A voi tarkastella ympäristöä 1 Chromessa ja ympäristöä 2 Microsoft Edgessä.)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
