---
title: Finance and Operationsin ja Common Data Servicen lähes reaaliaikainen integrointi
description: Tässä ohjeaiheessa on yleiskatsaus Microsoft Dynamics 365 for Finance and Operationsin ja Common Data Servicen integroinnista.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: aa614c8e6a79a3f7a4f8f2f99f1f1bd1a67ac921
ms.sourcegitcommit: efcc0dee8bde5f8f93f6291e7f059ad426843e57
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/31/2019
ms.locfileid: "1797225"
---
# <a name="near-real-time-data-integration-between-finance-and-operations-and-common-data-service"></a>Finance and Operationsin ja Common Data Servicen lähes reaaliaikainen integrointi

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

Nykyisessä digitaalisessa maailmassa liiketoiminnan ekosysteemit käyttävät Microsoft Dynamics 365 -sovelluspakettia kokonaisuutena. Koska henkilöiden, asiakkaiden, operaatioiden ja esineiden internetin (IoT) laitteiden tiedot virtaavat yhteen lähteeseen, on mahdollista, että digitaaliset palautesilmukat ovat käytettävissä. Tämän kokemuksen saavuttamiseksi Dynamics 365 for Finance and Operationsin ja Dynamics 365 for Customer Engagement -sovelluksen välinen integrointi on oleellinen. Customer Engagement -sovellukset on rakennettu Common Data Servicen päälle. Finance and Operationsin tietojen integrointi Common Data Servicen kanssa antaa Customer Engagement -sovelluksille mahdollisuuden kommunikoida johdonmukaisesti ja sujuvasti Finance and Operationsin kanssa.

Finance and Operations ja Common Data Service tarjoavat lähes reaaliaikaista tietojen synkronointia Finance and Operationsin ja Customer Engagement -sovellusten välillä kaksoiskirjoituskehyksen avulla. Kattavuus on laaja ja kattaa 28 Finance and Operationsin osa-aluetta. Tavoitteena on tarjota yksi yhdenmukainen Dynamics 365 -käyttäjäkokemus saumattomien tietovirtojen kautta, jotka yhdistävät liiketoimintaprosesseja eri sovelluksissa.

![Arkkitehtuurin yleiskuvauskaavio](media/dual-write-overview.jpg)

Asiakkaille on tarjolla seuraavat arvoehdotukset:

+ [Organisaatiohierarkia Common Data Servicessa](dual-write-organization.md)
+ [Yrityksen käsite Common Data Servicessa](dual-write-company.md)
+ [Integroidut asiakkaiden päätiedot](dual-write-customer.md)
+ [Integroidut toimittajien päätiedot](dual-write-vendor.md)
+ Yhdistetty päätuote

## <a name="system-requirements"></a>Järjestelmävaatimukset

Synkroniset, kaksisuuntaiset, lähes reaaliaikaiset tietovirrat vaativat seuraavat versiot:

+ Microsoft Dynamics 365 for Finance and Operationsin versio 10.0.4 (heinäkuu 2019) ja Platform update 28 tai uudempi
+ Microsoft Dynamics 365 for Customer Engagement, Platform -versio 9.1 (4.2) tai uudempi

## <a name="setup-instructions"></a>Määritysohjeet

Määritä Finance and Operationsin ja Common Data Service:n integrointi seuraavasti.
    
1. Kaksoiskirjoitusjärjestelmän asennusta varten katso [vaiheittainen opas](https://aka.ms/dualwrite-docs) kaksoiskirjoituksen esiversion julkistamisessa.
2. Lataa ja asenna ratkaisu Yammer-ryhmästä [Finance and Operations, Common Data Service, and Customer Engagement Integration](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=66052096). Paketti sisältää viisi ratkaisua:

    + Dynamics365Company
    + CurrencyExchangeRates
    + Dynamics365FinanceAndOperationsCommon
    + Dynamics365FinanceCommon
    + Dynamics365SupplyChainCommon

3. Noudata suoritusjärjestystä [alkuperäisten viitetietojen synkronoinnissa](dual-write-initial.md).
4. Jos kohtaat kaksoiskirjoitussynkronoinnin ongelmia, katso [tietojen integroinnin vianetsintäopas](dual-write-troubleshooting.md).

> [!IMPORTANT]
> Et voi suorittaa kaksoiskirjoitusta ja [Prospektista käteiseksi -prosessia](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/accounts-template-mapping-direct) rinnakkain. Jos käytössäsi on Prospektista käteiseksi -ratkaisu, sinun on poistettava sen asennus. Sinun on myös poistettava käytöstä asiakkaan ja toimittajan kaksoiskirjoitusmallit, jotka ovat osa Prospektista käteiseksi -ratkaisua.
