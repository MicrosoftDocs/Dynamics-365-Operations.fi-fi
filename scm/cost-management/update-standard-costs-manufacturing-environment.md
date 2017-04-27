---
title: "Standardikustannusten päivittäminen valmistusympäristössä"
description: "Tämä artikkeli sisältää ohjeita vakiokustannusten päivittämiseen tuotantoympäristössä."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: CostingVersion, InventStdCostConv
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 79663
ms.assetid: 3a7c3d13-8dbc-442d-a281-ac0ebe99ec83
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 9a7199b62ea0037e709da983b6fd53aaadeca4ad
ms.lasthandoff: 03/31/2017


---

# <a name="update-standard-costs-in-a-manufacturing-environment"></a>Standardikustannusten päivittäminen valmistusympäristössä

[!include[banner](../includes/banner.md)]


Tämä artikkeli sisältää ohjeita vakiokustannusten päivittämiseen tuotantoympäristössä. 

Päivitykset voivat johtua uusista nimikkeistä, kustannusluokista tai epäsuorien kustannusten laskentakaavoista. Ne voivat johtua myös korjauksista ja kustannusmuutoksista. Kuten seuraavista esimerkkitapauksista selviää, päivityksen tyyppi vaikuttaa siihen, mitä toimia standardikustannusten päivittäminen edellyttää.

-   Lisää ostettujen nimikkeiden odotetut standardikustannusten muutokset ja muuta sitten nimikkeen kustannustietueiden tila **aktiiviseksi** asianmukaisena päivämääränä. Älä kuitenkaan laske ostettuja nimikkeitä käyttävien valmistettujen nimikkeiden kustannuksia uudelleen.
-   Lisää uuden ostetun nimikkeen standardikustannukset, mutta älä laske sellaisten valmistettujen nimikkeiden kustannuksia uudelleen, joiden tuoterakenneversiossa on uusi ostettu nimike komponenttina.
-   Korjaa tai muuta ostetun nimikkeen kustannuksia tai muuta ostettuun nimikkeeseen määritettyä kustannusryhmää. Laske myös kaikkien sellaisten valmistettujen nimikkeiden kustannukset, joiden tuoterakenneversiossa on ostettu nimike komponenttina.
-   Muuta kustannusluokan kustannusta ja laske kaikkien sellaisten valmistettujen nimikkeiden kustannukset, joiden reititysversiossa on kustannusluokkaa käyttäviä reitityksen työvaiheita.
-   Muuta kustannusluokkia, jotka on määritetty reitityksen työvaiheisiin, tai kustannusryhmää, joka on määritetty kustannusluokkiin. Laske sitten kaikkien sellaisten valmistettujen nimikkeiden kustannukset, joiden reititysversiossa on kustannusluokkaa käyttäviä reitityksen työvaiheita.
-   Muuta epäsuorien kustannusten laskentakaavaa ja laske kaikkien sellaisten valmistettujen nimikkeiden kustannukset, joihin muutos vaikuttaa.
-   Muuta tai lisää valmistetulle nimikkeelle valmistustoimipaikka ja laske nimikkeen toimipaikkakohtaiset valmistuskustannukset.
-   Laske valmistetun nimikkeen kustannukset tai laske ne uudelleen. Laske sitten kaikkien sellaisten valmistettujen nimikkeiden kustannukset uudelleen, joiden tuoterakenneversiossa on valmistettu nimike komponenttina.
-   Laske uuden valmistetun nimikkeen kustannukset sen määritettyjen, hyväksyttyjen ja aktiivisten tuoterakenne- ja reititystietojen perusteella.

Jokainen tilanne vaatii tarkkaa harkintaa siitä, kuinka vakiokustannukset pitäisi päivittää.




