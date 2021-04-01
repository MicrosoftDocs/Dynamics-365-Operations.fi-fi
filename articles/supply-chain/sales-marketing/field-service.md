---
title: Microsoft Dynamics 365 Field Service -integroinnin yleiskatsaus
description: Tässä ohjeaiheessa on yleiskatsaus Microsoft Dynamics 365 Field Servicen integroinnista.
author: ChristianRytt
manager: tfehr
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 9b0fafd46143979a734151b4011e537991347862
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5237891"
---
# <a name="integration-with-microsoft-dynamics-365-field-service-overview"></a>Microsoft Dynamics 365 Field Service -integroinnin yleiskatsaus

[!include[banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Supply Chain Management mahdollistaa liiketoimintaprosessien synkronoinnin Dynamics 365 Supply Chain Managementin ja Dynamics 365 Field Servicen välillä Integrointiskenaariot määritetään käyttämällä laajennettavia tietojen integrointitoiminnon malleja ja Microsoft Dataverse -palvelua. Niiden avulla liiketoimintaprosessien synkronointi voidaan ottaa käyttöön.
Mukautettujen integrointiprojektien luontiin voidaan käyttää vakiomalleja. Näissä projekteissa lisävakiosarakkeita ja mukautettuja sarakkeita ja taulukoita yhdistämällä voidaan muokata integrointi liiketoimintatarpeita vastaavaksi. 

Field Service -integrointi perustuu aiempaan myyntimahdollisuudesta maksutapahtumaan -toimintoon.

![Liiketoimintaprosessien synkronointi Supply Chain Managementin ja Field Servicen välillä](./media/field-service-integration.png)

Field Servicen ja Supply Chain Managementin välisen integroinnin ensimmäinen vaihe keskittyy siihen, että Field Servicen työtilauksia ja sopimuksia voidaan laskuttaa Supply Chain Managementissa. Tuettu työnkulku käynnistyy Field Servicessä, jossa työtilausten tiedot synkronoidaan Supply Chain Managementiin myyntitilauksina. Supply Chain Managementissa myyntitilaukset laskutetaan, jotta laskuasiakirjat voidaan luoda. Myös Field Servicen sopimuslaskujen tiedot synkronoidaan Supply Chain Managementiin. Microsoft Dynamics 365:n tietojen integrointitoiminto synkronoi tiedot käyttämällä mukautettavia projekteja. Mukautettujen integrointiprojektien luontiin voidaan käyttää vakiomalleja. Näissä projekteissa lisävakiosarakkeita ja mukautettuja sarakkeita sekä taulukoita yhdistämällä voidaan muokata integrointi tarpeita vastaavaksi.

Field Servicen ja Supply Chain Managementin ensimmäisen vaiheen integrointi mahdollistaa seuraavien nimikkeiden synkronoinnin:

- [Supply Chain Managementin tuotteiden synkronointi Field Servicen tuotteisiin](field-service-product.md)
- [Field Servicen työtilausten synkronointi Supply Chain Managementin myyntitilauksiin](field-service-work-order.md)
- [Field Servicen sopimuslaskujen synkronointi Supply Chain Managementin vapaatekstilaskuihin](field-service-invoice.md)

Esimerkki työtilauksen synkronoimisesta Field Servicen ja Supply Chain Managementin välillä on lyhyessä YouTube-videossa [Työtilauksen synkronointi Microsoft Dynamics 365:n integroinnilla](https://www.youtube.com/watch?v=46ylO7raZAo).

## <a name="integration-with-field-service-including-inventory-and-project-information"></a>Integrointi Field Servicen kanssa varasto- ja projektitiedot mukaan lukien

Tämä toisen vaiheen lisätoiminto keskittyi antamaan kenttätyöntekijöille käsityksen Supply Chain Managementin varastotiedoista, jotta he voivat päivittää varastotasot ja tehdä materiaalisiirtoja. Lisäksi myytyjä hyödykkeitä asentavat tai huoltavat yritykset pystyvät hallitsemaan entistä paremmin koko myynti- ja huoltoprosessia sekä saavat paremman näkyvyyden tähän prosessiin projektien integroinnin ansiosta.

### <a name="functionality-includes-integration-of"></a>Toiminto sisältää seuraavien tietojen integroinnin:
- Varastotiedot
- Käytettävissä olevan varaston tiedot
- Varastosiirrot
- Varasto-oikaisut
- Supply Chain Management -projektit, jotka liittyvät Dynamics 365 Field Service -työtilauksiin
- Dynamics 365 Field Servicen työtilaukset, joissa on linkki Supply Chain Management -projekteihin, käyttävät tätä projektinumeroa myyntitilauksessa, mikä mahdollistaa laskutuksen projektista. 

![Liiketoimintaprosessien synkronointi Supply Chain Managementin ja Field Servicen välillä](./media/FSv2overview.png)

### <a name="the-second-phase-of-the-integration-between-field-service-and-supply-chain-management-enables-synchronization-with-the-following-templates"></a>Field Servicen ja Supply Chain Managementin toisen vaiheen integrointi mahdollistaa seuraavien mallien synkronoinnin:
- Varastot (Supply Chain Managementista Field Serviceen) - varastot Supply Chain Managementista Field Serviceen [edistynyt kysely] 
- Tuotevarasto (Supply Chain Managementista Field Serviceen) - varastosaldotiedot Supply Chain Managementista Field Serviceen [edistynyt kysely] 
- Varastomuutos (Field Servicesta Supply Chain Managementiin) - Varaston muutokset Field Servicesta Supply Chain Managementiin [edistynyt kysely] 
- Varastosiirrot (Field Servicesta Supply Chain Managementiin) - Varaston siirrot Field Servicesta Supply Chain Managementiin [edistynyt kysely] 
- Projektit (Supply Chain Managementista Field Serviceen) - projektiluettelo Supply Chain Managementista Field Serviceen 
- Projektin työtilaukset (Field Servicestä Supply Chain Managementiin) – Field Servicen työtilaukset Supply Chain Managementin myyntilauksiin ja projektituki [Lisäkysely] 
- Field Servicen tuotteet, joissa varastoyksikkö (Supply Chain Managementista Salesiin) – Supply Chain Managementin Myytävät vapautetut tuotteet Salesin Field Serviceen tuotteisiin, joissa varastoyksiköt 

## <a name="system-requirements"></a>Järjestelmävaatimukset

### <a name="system-requirements-for-supply-chain-management"></a>Supply Chain Managementin järjestelmävaatimukset
Field Servicen integrointi tukee seuraavia versioita:

- Dynamics 365 for Finance and Operationsin versio 8.1.2 (joulukuu 2018) julkaistiin joulukuussa 2018; sen koontiversionumero on 8.1.195 ja Platform update 22 (7.0.5095). 

### <a name="system-requirements-for-field-service"></a>Field Servicen järjestelmävaatimukset
Seuraavat komponentit on asennettava, jotta Field Service -integrointiratkaisua voi käyttää:

- Field Service (versio 8.2.0.286) tai uusi versio Dynamics 365 9.1.x – julkaistiin marraskuussa 2018
- Dynamics 365:N prospektista käteiseksi (P2C) -ratkaisu, versio 1.15.0.1 tai uudempi versio. Ratkaisun voi ladata [AppSourcesta](https://appsource.microsoft.com/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).
- Dynamics 365:n Field Servicen integrointi-, projekti- ja varastoratkaisu, versio 2.0.0.0 tai uudempi versio. Ratkaisun voi ladata [AppSourcesta](https://appsource.microsoft.com/product/dynamics-365/mscrm.p2cfieldserviceintegrationv2).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]