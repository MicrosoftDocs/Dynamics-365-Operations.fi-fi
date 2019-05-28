---
title: Integrointi Microsoft Dynamics 365 for Field Service:n kanssa
description: Tässä ohjeaiheessa on yleiskatsaus Microsoft Dynamics 365 for Field Servicen integroinnista.
author: ChristianRytt
manager: AnnBe
ms.date: 02/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: efda4e39f63155785386ecec6d21973e01a0f69f
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/15/2019
ms.locfileid: "1564015"
---
# <a name="integration-with-microsoft-dynamics-365-for-field-service"></a>Integrointi Microsoft Dynamics 365 for Field Service:n kanssa

[!include[banner](../includes/banner.md)]

Microsoft Dynamics 365 for Finance and Operationsin avulla voi synkronoida liiketoimintaprosesseja Finance and Operationsin ja Microsoft Dynamics 365 for Field Servicen välillä. Integrointiskenaariot määritetään käyttämällä laajennettavia tietojen integrointitoiminnon malleja ja Common Data Service (CDS) -palvelua. Niiden avulla liiketoimintaprosessien synkronointi voidaan ottaa käyttöön.
Mukautettujen integrointiprojektien luontiin voidaan käyttää vakiomalleja. Näissä projekteissa lisävakiokenttiä ja mukautettuja kenttiä sekä yksiköitä yhdistämällä voidaan muokata integrointi liiketoimintatarpeita vastaavaksi. 

Field Service -integrointi perustuu aiempaan myyntimahdollisuudesta maksutapahtumaan -toimintoon.

![Liiketoimintaprosessien synkronointi Finance and Operationsin ja Field Servicen välillä](./media/field-service-integration.png)

Field Servicen ja Finance and Operationsin välisen integroinnin ensimmäinen vaihe keskittyy siihen, että Field Servicen työtilauksia ja sopimuksia voidaan laskuttaa Finance and Operationsissa. Tuettu työnkulku käynnistyy Field Servicessä, jossa työtilausten tiedot synkronoidaan Finance and Operationsiin myyntitilauksina. Finance and Operationsissa luodaan laskuasiakirjoja laskuttamalla myyntitilaukset. Myös Field Servicen sopimuslaskujen tiedot synkronoidaan Finance and Operationsiin. Microsoft Dynamics 365:n tietojen integrointitoiminto synkronoi tiedot käyttämällä mukautettavia projekteja. Mukautettujen integrointiprojektien luontiin voidaan käyttää vakiomalleja. Näissä projekteissa lisävakiokenttiä ja mukautettuja kenttiä sekä yksiköitä yhdistämällä voidaan muokata integrointi tarpeita vastaavaksi.

Field Servicen ja Finance and Operationsin ensimmäisen vaiheen integrointi mahdollistaa seuraavien nimikkeiden synkronoinnin:

- [Finance and Operationsin tuotteet Field Servicen tuotetyyppitietoja sisältäviin tuotteisiin](field-service-product.md)
- [Field Servicen työtilaukset Finance and Operationsin myyntitilauksiin](field-service-work-order.md)
- [Field Servicen laskut Finance and Operationsin vapaatekstilaskuihin](field-service-invoice.md)

Esimerkki työtilauksen synkronoimisesta Field Servicen ja Finance and Operationsin välillä on lyhyessä YouTube-videossa [Työtilauksen synkronointi Microsoft Dynamics 365:n integroinnilla](https://www.youtube.com/watch?v=46ylO7raZAo).

## <a name="integration-with-microsoft-dynamics-365-for-field-service-including-inventory-and-project-information"></a>Integrointi Microsoft Dynamics 365 for Field Servicen kanssa varasto- ja projektitiedot mukaan lukien

Tämä toisen vaiheen lisätoiminto keskittyi antamaan kenttätyöntekijöille käsityksen Finance and Operationsin varastotiedoista, jotta he voivat päivittää varastotasot ja tehdä materiaalisiirtoja. Lisäksi myytyjä hyödykkeitä asentavat tai huoltavat yritykset pystyvät hallitsemaan entistä paremmin koko myynti- ja huoltoprosessia sekä saavat paremman näkyvyyden tähän prosessiin projektien integroinnin ansiosta.

### <a name="functionality-includes-integration-of"></a>Toiminto sisältää seuraavien tietojen integroinnin:
- Varastotiedot
- Käytettävissä olevan varaston tiedot
- Varastosiirrot
- Varasto-oikaisut
- Dynamics 365 for Finance and Operationsin Dynamics 365 for Field Servicen työtilauksiin yhdistetyt projektit
- Dynamics 365 for Field Servicen työtilaukset, joissa on linkki Dynamics 365 for Finance and Operations -projekteihin, käyttävät tätä projektinumeroa Dynamics 365 for Finance and Operationsin myyntitilauksessa, mikä mahdollistaa laskutuksen projektista. 

![Liiketoimintaprosessien synkronointi Finance and Operationsin ja Field Servicen välillä](./media/FSv2overview.png)

### <a name="the-second-phase-of-the-integration-between-field-service-and-finance-and-operations-enables-synchronization-with-the-following-templates"></a>Field Servicen ja Finance and Operationsin toisen vaiheen integrointi mahdollistaa seuraavien mallien synkronoinnin:
- Varastot (Fin and Opsista Field Serviceen) – varastot Finance and Operationsista Field Serviceen [Lisäkysely] 
- Tuotevarasto (Fin and Opsista Field Serviceen) – varastotasotiedot Finance and Operationsista Field Serviceen [Lisäkysely] 
- Varasto-oikaisu (Field Servicestä Fin and Opsiiin) – varasto-oikaisut Field Servicestä Finance and Operationsiin [Lisäkysely] 
- Varastosiirrot (Field Servicestä Fin and Opsiiin) – varastosiirrot Field Servicestä Finance and Operationsiin [Lisäkysely] 
- Projektit (Fin and Opsista Field Serviceen) – projektiluettelot Finance and Operationsista Field Serviceen 
- Projektin työtilaukset (Field Servicestä Fin and Opsiin) – Field Servicen projektin työtilaukset Finance and Operationsin myyntilaukset ja projektituki [Lisäkysely] 
- Field Servicen tuotteet, joissa varastoyksikkö (Fin and Opsista Salesiin) – Finance and Operationsin Myytävät vapautetut tuotteet Salesin Field Serviceen tuotteisiin, joissa varastoyksiköt 

## <a name="system-requirements"></a>Järjestelmävaatimukset

### <a name="system-requirements-for-finance-and-operations"></a>Finance and Operations -sovelluksen järjestelmävaatimukset
Field Servicen integrointi tukee seuraavia versioita:

- Dynamics 365 for Finance and Operationsin versio 8.1.2 (joulukuu 2018) julkaistiin joulukuussa 2018; sen koontiversionumero on 8.1.195 ja Platform Update 22 (7.0.5095). 

### <a name="system-requirements-for-field-service"></a>Field Servicen järjestelmävaatimukset
Seuraavat komponentit on asennettava, jotta Field Service -integrointiratkaisua voi käyttää:

- Field Service for Dynamics 365 (versio 8.2.0.286) tai uusi versio Dynamics 365 9.1.x – julkaistiin marraskuussa 2018
- Dynamics 365:N prospektista käteiseksi (P2C) -ratkaisu, versio 1.15.0.1 tai uudempi versio. Ratkaisun voi ladata [AppSourcesta](https://appsource.microsoft.com/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).
- Dynamics 365:n Field Servicen integrointi-, projekti- ja varastoratkaisu, versio 2.0.0.0 tai uudempi versio. Ratkaisun voi ladata [AppSourcesta](https://appsource.microsoft.com/product/dynamics-365/mscrm.p2cfieldserviceintegrationv2).
