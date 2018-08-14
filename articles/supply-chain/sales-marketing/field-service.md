---
title: Microsoft Dynamics 365 for Field Servicen integrointi
description: "Tässä ohjeaiheessa on yleiskatsaus Microsoft Dynamics 365 for Field Servicen integroinnista."
author: ChristianRytt
manager: AnnBe
ms.date: 04/25/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: a57e23691a6b4d48c6b8dd6d1f61fc9730365b39
ms.openlocfilehash: 0c1268d2fddcf7b28ecfc3197f21e9d30a5a5855
ms.contentlocale: fi-fi
ms.lasthandoff: 05/31/2018

---


# <a name="integration-with-microsoft-dynamics-365-for-field-service"></a>Microsoft Dynamics 365 for Field Servicen integrointi

[!include[banner](../includes/banner.md)]

Microsoft Dynamics 365 for Finance and Operationsin avulla voi synkronoida liiketoimintaprosesseja Finance and Operationsin ja Microsoft Dynamics 365 for Field Servicen välillä. Integrointiskenaariot määritetään käyttämällä laajennettavia tietojen integrointitoiminnon malleja ja Common Data Service (CDS) -palvelua. Niiden avulla liiketoimintaprosessien synkronointi voidaan ottaa käyttöön.

[![Liiketoimintaprosessien synkronointi Finance and Operationsin ja Field Servicen välillä](./media/field-service-integration.png)](./media/field-service-integration.png)

Field Servicen ja Finance and Operationsin välisen integroinnin ensimmäinen vaihe keskittyy siihen, että Field Servicen työtilauksia ja sopimuksia voidaan laskuttaa Finance and Operationsissa. Tuettu työnkulku käynnistyy Field Servicessä, jossa työtilausten tiedot synkronoidaan Finance and Operationsiin myyntitilauksina. Finance and Operationsissa luodaan laskuasiakirjoja laskuttamalla myyntitilaukset. Myös Field Servicen sopimuslaskujen tiedot synkronoidaan Finance and Operationsiin. Microsoft Dynamics 365:n tietojen integrointitoiminto synkronoi tiedot käyttämällä mukautettavia projekteja. Mukautettujen integrointiprojektien luontiin voidaan käyttää vakiomalleja. Näissä projekteissa lisävakiokenttiä ja mukautettuja kenttiä sekä yksiköitä yhdistämällä voidaan muokata integrointi tarpeita vastaavaksi.

Field Servicen ja Finance and Operationsin ensimmäisen vaiheen integrointi mahdollistaa seuraavien nimikkeiden synkronoinnin:

- [Finance and Operationsin tuotteet Field Servicen tuotetyyppitietoja sisältäviin tuotteisiin](field-service-product.md)
- [Field Servicen työtilaukset Finance and Operationsin myyntitilauksiin](field-service-work-order.md)
- [Field Servicen laskut Finance and Operationsin vapaatekstilaskuihin](field-service-invoice.md)

Esimerkki työtilauksen synkronoimisesta Field Servicen ja Finance and Operationsin välillä on lyhyessä YouTube-videossa [Työtilauksen  Dynamics 365 for Field Servicen ja Finance and Operationsin välillä](https://www.youtube.com/watch?v=hAB4TDVMjxU).

## <a name="system-requirements-for-finance-and-operations"></a>Finance and Operations -sovelluksen järjestelmävaatimukset
Field Servicen integrointi tukee seuraavia versioita:

### <a name="dynamics-365-for-finance-and-operations-version-80-april-2018-or-later"></a>Dynamics 365 for Finance and Operations -versio 8.0 (huhtikuu 2018) tai uudempi

- Dynamics 365 for Finance and Operations versio 8.0 (huhtikuu 2018) julkaistiin huhtikuussa 2018; sen koontiversionumero on 8.0.30.8020 ja ympäristöpäivitys 15 (7.0.4841.35234). 

## <a name="system-requirements-for-field-service"></a>Field Servicen järjestelmävaatimukset
Seuraavat komponentit on asennettava, jotta Field Service -integrointiratkaisua voi käyttää:

### <a name="microsoft-dynamics-365-for-field-service-90-or-later"></a>Microsoft Dynamics 365 for Field Service 9.0 tai uudempi

- Dynamics 365 for Field Servicen versio 1612 (9.0.1.733) (DB 9.0.1.733) online tai uudempi versio
- Dynamics 365:N prospektista käteiseksi (P2C) -ratkaisu, versio 1.15.0.1 tai uudempi versio. Ratkaisun voi ladata [AppSourcesta](https://appsource.microsoft.com/en-us/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).
- Dynamics 365:n Field Service -integrointiratkaisu, versio 1.0.0.0 tai uudempi versio. Ratkaisun voi ladata [AppSourcesta](https://appsource.microsoft.com/en-us/product/dynamics-365/mscrm.p2cfieldserviceintegration).

