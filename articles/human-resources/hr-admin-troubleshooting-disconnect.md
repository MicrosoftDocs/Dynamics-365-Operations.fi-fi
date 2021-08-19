---
title: Asiakasohjelma katkaisee yhteyden
description: Tässä artikkelissa kerrotaan, miten toimitaan, jos asiakkaan yhteys ympäristöön katkeaa tuntemattomasta syystä.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 3ee3bb4547cb9d77b7559ce4ba54b478f63cb045caefefec0583b3f9b03cf53b
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6770477"
---
# <a name="client-disconnects"></a>Asiakasohjelma katkaisee yhteyden

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