---
title: Palkanlaskennan integroinnin ohjelmointirajapinnan esittely
description: Tässä aiheessa kuvataan Dynamics 365 Human Resources -palkanlaskenta-integroinnin sovellusliittymää.
author: twheeloc
ms.date: 02/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2021-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 3743561e3ea3c798c37d71d851eb6b197c8d1c41
ms.sourcegitcommit: d67f7edaf1a50077c2a7dd105e774f86fc586495
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/02/2022
ms.locfileid: "8533823"
---
# <a name="payroll-integration-api-introduction"></a>Palkanlaskennan integroinnin ohjelmointirajapinnan esittely


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Tässä ohjeessa kuvataan Dynamics 365 Human Resources -palkanlaskenta-integroinnin sovellusliittymää. Ohjelmointirajapinta mahdollistaa virtaviivaisen päästä päähän -integraation henkilöstöhallinnon ja kumppanuuspalkkajärjestelmien välillä. Integroitu kokemus alkaa henkilöstöhallinnosta työntekijän profiili-, palkka- ja vähennystieto- ja osallistumistiedoilla. Kun työntekijä palkataan ja tarvittavat profiilitiedot ja palkkatiedot otetaan henkilöstöhallintoon, palkanlaskentajärjestelmä ottaa käyttöön nämä tiedot, joita käytetään palkanlaskentaa käsiteltäessä. Työntekijään tehdyt tai maksutiedot päivitetään myös käytettäväksi myöhemmin maksuajoissa.

[![Palkanlaskennan integroinnin työnkulku.](media/hr-admin-integration-payroll-api-introduction-flow.png)](media/hr-admin-integration-payroll-api-introduction-flow-2.png#lightbox)

Integroinnin mahdollistamiseksi Human Resourcesiin kuuluvat seuraavat komponentit:

- [Toiminto, jonka avulla voidaan merkitä, että työntekijälle voidaan maksaa.](hr-compensation-payroll.md)
- Integroinnin API-sovellusliittymä, joka avaa uudet toiminnot integroiduille sovelluksille.

## <a name="microsoft-dataverse"></a>Microsoft Dataverse

Tämä sovellusliittymä perustuu Microsoft Dataverseen (aiemmin Common Data Service). Kaikki RESTful-vuorovaikutus tämän sovellusliittymän kanssa tapahtuu ODataa käyttävän Microsoft Dataverse -verkkoliittymän kautta. Tämä sovellusliittymä on Dataverse-verkkoliittymän osajoukko. Dataverse-verkkoliittymä määrittää ominaisuuksia, kuten todennuksen, SLA-sopimukset, erän, samanaikaisuustarkistuksen ja virheiden käsittelyn.

Yleisiä tietoja Microsoft Dataverse -verkkoliittymästä:

- [Mikä on Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)
- [Microsoft Dataverse -verkkoliittymän käyttäminen](/powerapps/developer/data-platform/webapi/overview)
- [Microsoft Dataversen kehittäjäopas](/powerapps/developer/data-platform)

Tämä dokumentaatio sisältää Dataversen Web-ohjelmointirajapinnan käytön yksityiskohtaisia tietoja ja kehittäjän ohjeita, joita ovat muun muassa seuraavat aiheet:

- [Todenna Microsoft Dataverse www-ohjelmointirajapinnan avulla](/powerapps/developer/data-platform/webapi/authenticate-web-api)
- [Toimintojen suorittamiseen www-ohjelmointirajapinnan avulla](/powerapps/developer/data-platform/webapi/perform-operations-web-api)
- [Postmanin käyttäminen www-ohjelmointirajapinnan kanssa](/powerapps/developer/data-platform/webapi/use-postman-web-api)
- [Muutosten seurannan avulla voit synkronoida tiedot ulkoisten järjestelmien kanssa](/powerapps/developer/data-platform/use-change-tracking-synchronize-data-external-systems)

### <a name="virtual-tables-for-human-resources-in-dataverse"></a>Human Resourcesin virtuaalitaulut Dataversessa

Palkanlaskentaintegroinnin API:n päätepisteet käyttävät Microsoft Dataversen virtuaalitaulujen ominaisuuksia. Oletusarvon mukaan virtuaalitauluja ja niihin liittyviä API-päätepisteitä ei ole otettu käyttöön Human Resources -ympäristöissä, minkä ansiosta organisaatiot voivat määrittää, mitkä OData-päätepisteet julkistetaan ympäristölle. Jotta sovellusliittymää voidaan käyttää, Human Resourcesin yksiköiden virtuaalitaulut on luotava ympäristöä varten.

Lisätietoja virtuaalitaulujen luomisesta liittymää varten on kohdassa [Dataverse-virtuaalitaulujen konfiguroiminen](./hr-admin-integration-common-data-service-virtual-entities.md).

## <a name="data-model"></a>Tietomalli

Seuraava kaavio kuvaa suhteita API:n sisällä. Useilla tyypeillä on viiteavaimet muihin Human Resourcesin aiemmin luotuihin yksiköihin, joita ei ole kuvattu tässä. Tässä asiakirjassa on tietoja yksiköistä, jotka liittyvät erityisesti palkanlaskennan integrointiskenaarioihin. Dataverse-www-ohjelmointirajapinnassa on kuitenkin useita muita yksiköitä henkilöstöhallinnolle, jotka voivat myös olla oleellisia integrointisi kannalta. Joihinkin näistä yksiköistä viitataan viiteavainsuhteissa tai siirtymisominaisuuksissa.

[![Palkanlaskennan integroinnin API-tietomalli.](media/hr-admin-payroll-api-data-model.png)](media/hr-admin-payroll-api-data-model.png#lightbox)

## <a name="payroll-employee-and-related-entities"></a>Palkanlaskennan työntekijä ja liittyvät entiteetit

Yksiköt:

- [Palkanlaskennan työntekijä](hr-admin-integration-payroll-api-payroll-employee.md)
- [Palkanlaskennan työntekijän osoite](hr-admin-integration-payroll-api-payroll-worker-address.md)
- [Palkanlaskennan kiinteän kompensaation suunnitelma](hr-admin-integration-payroll-api-payroll-fixed-compensation-plan.md)
- [Palkanlaskennan muuttava kompensaatiosuunnitelma](hr-admin-integration-payroll-api-payroll-variable-compensation-plan.md)
- [Palkanlaskennan työ](hr-admin-integration-payroll-api-payroll-position-job.md)
- [Palkanlaskennan toimi](hr-admin-integration-payroll-api-payroll-position.md)

## <a name="see-also"></a>Lisätietoja

[Luo ja arvostele palkanlaskennan yksiköitä](hr-admin-integration-payroll-api-generate-review-entities.md)<br>
[Määritä Human Resourcesin parametrit](hr-setup-parameters.md)<br>
[Määritä jaetut henkilöstöhallinnon parametrit](hr-setup-shared-parameters.md)<br>
[Mikä on Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)<br>
[Microsoft Dataverse -verkkoliittymän käyttäminen](/powerapps/developer/data-platform/webapi/overview)<br>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
