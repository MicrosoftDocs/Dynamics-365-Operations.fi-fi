---
title: "Pankin tiliotteen ja maksun täsmäytyksen yleiskatsaus EU:n osalta"
description: "Tässä aiheessa on yleiskatsaus toiminnoista, joiden avulla voit täsmäyttää maksutiedot pankeilta muodossa, joita käytetään Euroopan maissa."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BankAccountTable, CustPaymMode, VendPaymMode
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations, Core
ms.custom: 267994
ms.search.region: Belgium, Norway, Sweden, Switzerland
ms.author: v-lenest
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 5e4f3fdce97cf05a8f54873cd8d80364b1505bd3
ms.contentlocale: fi-fi
ms.lasthandoff: 06/13/2017


---

# Pankin tiliotteen ja maksun täsmäytyksen yleiskatsaus EU:n osalta
<a id="bank-statement-and-payment-reconciliation-overview-for-the-eu" class="xliff"></a>

[!include[banner](../includes/banner.md)]


Tässä aiheessa on yleiskatsaus toiminnoista, joiden avulla voit täsmäyttää maksutiedot pankeilta muodossa, joita käytetään Euroopan maissa.

Voit tuoda Microsoft Dynamics 365 for Finance and Operations, Enterprise Editionissa tapahtumia pankeista ja täsmäyttää nämä tapahtumat olemassa olevia tapahtumia vasten. Euroopassa voit tehdä tämän seuraavissa tapauksissa:

-   Tiliotteiden tuonti
-   Maksujen tuonti.
-   Palautustiedostojen tuonti.

## Tiliotteet
<a id="bank-statements" class="xliff"></a>
*Tiliote*** on yhteenveto kirjanpitotapahtumista, jotka ovat tapahtuneet rahoituslaitoksen pankkitilillä tiettynä ajanjaksona. Voit tuoda tiliotteita Finance and Operationsissa. On tärkeää täsmäyttää tuodut tapahtumat olemassa olevien tapahtumien kanssa sekä tarkistaa pankkitilien alku- ja loppusaldo. Seuraavassa luettelossa on Euroopan tuetut tiedostomuodot.

-   Pankkitilin täsmäytyksen lisätoimintojen Euroopan tiedostomuodot. Lisätietoja on ohjeaiheessa [Pankkitilin täsmäytyksen lisätoimintojen yleiskatsaus](../cash-bank-management/advanced-bank-reconciliation-overview.md).
-   ISO 20022 camt.053 – tiliotteen sanoman tiedostomuoto
-   CODA – tiliotteen tiedostomuoto Lisätietoja on ohjeaiheessa [CODA-tiliote](emea-bel-coda-bank-statement-import.md).

## Asiakkaan ja toimittajan maksujen tuonnin ja palautuksen viestit
<a id="customer-and-vendor-payments-import-and-return-messages" class="xliff"></a>
Tiliotteen lisäksi pankit voivat tarjota erityisiä asiakkaiden ja toimittajien maksuista tietoja sisältäviä viestejä, jotka voidaan tuoda Dynamics 365 Finance and Operationsiin sekä täsmäyttää asiakkaan ja toimittajan tapahtumien kanssa. Kun yritys haluaa vastaanottaa pankista tietoja saapuvista asiakkaan maksujen tapahtumista, voidaan käyttää näitä tuontimuotoja. Suoraveloitusta ja tilisiirtoa käyttävät yritykset voivat vastaanottaa palautusviestejä päivittääkseen aikaisemmin vietyjen maksujen tiloja. Tuonti- ja palautusmuotojen ero on se, että palautukset on tarkoitettu lähinnä päivittämään jo luotuja maksukirjauskansion rivejä (jotka on luotu joko suoraveloituksen tai tilisiirron yhteydessä) uusien rivien luonnin sijaan. Myös joihinkin monimutkaisiin tuontimuotoihin saattaa liittyä palautussanomia. Seuraavassa esimerkissä näytetään, kuinka tämä jako olisi pantava täytäntöön.

##### Tuontimuodot
<a id="import-formats" class="xliff"></a>

-   ISO 20022-camt.054 – pankin ilmoitussanoma
-   [Nets-tuontimuoto](emea-nor-nets-import-format.md) - Norjan maksumuotojen monimutkainen ominaisuus
-   ESR-asiakkaan maksujen tuonti
-   Maksujen tuontimuodot, Ruotsi - BankGirot Max- ja BankGirot OCR -muodot

##### Palautusmuodot
<a id="return-formats" class="xliff"></a>

-   ISO 20022-pain.002 – maksun tilaraportti
-   (DNK) BetalingsserviceBasis-returformat – palautusmuoto Betalingsservice-vientimuodolle
-   [Maksujen tuontimuodot, Ruotsi](emea-swe-payment-formats-import.md)  – Bankgirot Autogiro -palautukset
-   (SWE) BankGirot -palautus – Toimittajamaksujen palautusmuoto, joka vastaa Bankgirot-vientimuotoa



