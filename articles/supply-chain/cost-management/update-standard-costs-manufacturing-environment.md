---
title: Standardikustannusten päivittäminen valmistusympäristössä
description: Tämä artikkeli sisältää ohjeita vakiokustannusten päivittämiseen tuotantoympäristössä.
author: JennySong-SH
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CostingVersion, InventStdCostConv
audience: Application User
ms.reviewer: kamaybac
ms.custom: 79663
ms.assetid: 3a7c3d13-8dbc-442d-a281-ac0ebe99ec83
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yanansong
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8acbcb79fa45ea2f225775068e0d061a44cba1f7
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/03/2022
ms.locfileid: "8675232"
---
# <a name="update-standard-costs-in-a-manufacturing-environment"></a>Standardikustannusten päivittäminen valmistusympäristössä

[!include [banner](../includes/banner.md)]

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





[!INCLUDE[footer-include](../../includes/footer-banner.md)]