---
title: "Pankin tiliotteen ja maksun täsmäytyksen yleiskatsaus EU:n osalta"
description: "Tässä aiheessa on yleiskatsaus toiminnoista, joiden avulla voit täsmäyttää maksutiedot pankeilta muodossa, joita käytetään Euroopan maissa."
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: BankAccountTable, CustPaymMode, VendPaymMode
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 267994
ms.assetid: 2bfb8ecc-e850-43cb-9a96-deb11716a391
ms.search.region: Belgium, Norway, Sweden, Switzerland
ms.author: v-lenest
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: f707d45290682e79ee439ba0d504852429defa90
ms.openlocfilehash: 22d93d7b3618d4f5931c6a7e39d681173734b0b9
ms.lasthandoff: 03/31/2017


---

# <a name="bank-statement-and-payment-reconciliation-overview-for-the-eu"></a>Pankin tiliotteen ja maksun täsmäytyksen yleiskatsaus EU:n osalta

[!include[banner](../includes/banner.md)]


Tässä aiheessa on yleiskatsaus toiminnoista, joiden avulla voit täsmäyttää maksutiedot pankeilta muodossa, joita käytetään Euroopan maissa.

Microsoft Dynamics 365 for Operationsissa voit tuoda tapahtumia pankeista ja täsmäyttää nämä tapahtumat olemassa olevia tapahtumia vasten. Euroopassa voit tehdä tämän seuraavissa tapauksissa:

-   Tiliotteiden tuonti
-   Maksujen tuonti.
-   Palautustiedostojen tuonti.

## <a name="bank-statements"></a>Tiliotteet
*Tiliote*** on yhteenveto kirjanpitotapahtumista, jotka ovat tapahtuneet rahoituslaitoksen pankkitilillä tiettynä ajanjaksona. Dynamics 365 for Operationsissa voit tuoda tiliotteita. On tärkeää täsmäyttää tuodut tapahtumat olemassa olevien tapahtumien kanssa sekä tarkistaa pankkitilien alku- ja loppusaldo. Seuraavassa luettelossa on Euroopan tuetut tiedostomuodot.

-   Pankkitilin täsmäytyksen lisätoimintojen Euroopan tiedostomuodot. Lisätietoja on ohjeaiheessa [Pankkitilin täsmäytyksen lisätoimintojen yleiskatsaus](../cash-bank-management/advanced-bank-reconciliation-overview.md).
-   ISO 20022 camt.053 – tiliotteen sanoman tiedostomuoto
-   CODA – tiliotteen tiedostomuoto Lisätietoja on ohjeaiheessa [CODA-tiliote](emea-bel-coda-bank-statement-import.md).

## <a name="customer-and-vendor-payments-import-and-return-messages"></a>Asiakkaan ja toimittajan maksujen tuonnin ja palautuksen viestit
Tiliotteen lisäksi pankit voivat tarjota erityisiä viestejä, jotka sisältävät tietoja asiakkaiden ja toimittajien maksuista, jotka voidaan tuoda Dynamics 365 for Operationsiin ja täsmäyttää asiakkaan ja toimittajan tapahtumien kanssa. Kun yritys haluaa vastaanottaa pankista tietoja saapuvista asiakkaan maksujen tapahtumista, voidaan käyttää näitä tuontimuotoja. Suoraveloitusta ja tilisiirtoa käyttävät yritykset voivat vastaanottaa palautusviestejä päivittääkseen aikaisemmin vietyjen maksujen tiloja. Tuonti- ja palautusmuotojen ero on se, että palautukset on tarkoitettu lähinnä päivittämään jo luotuja maksukirjauskansion rivejä (jotka on luotu joko suoraveloituksen tai tilisiirron yhteydessä) uusien rivien luonnin sijaan. Myös joihinkin monimutkaisiin tuontimuotoihin saattaa liittyä palautussanomia. Seuraavassa esimerkissä näytetään, kuinka tämä jako olisi pantava täytäntöön.

##### <a name="import-formats"></a>Tuontimuodot

-   ISO 20022-camt.054 – pankin ilmoitussanoma
-   [Nets-tuontimuoto](emea-nor-nets-import-format.md) - Norjan maksumuotojen monimutkainen ominaisuus
-   ESR-asiakkaan maksujen tuonti
-   Maksujen tuontimuodot, Ruotsi - BankGirot Max- ja BankGirot OCR -muodot

##### <a name="return-formats"></a>Palautusmuodot

-   ISO 20022-pain.002 – maksun tilaraportti
-   (DNK) BetalingsserviceBasis-returformat – palautusmuoto Betalingsservice-vientimuodolle
-   [Maksujen tuontimuodot, Ruotsi](emea-swe-payment-formats-import.md)  – Bankgirot Autogiro -palautukset
-   (SWE) BankGirot -palautus – Toimittajamaksujen palautusmuoto, joka vastaa Bankgirot-vientimuotoa



