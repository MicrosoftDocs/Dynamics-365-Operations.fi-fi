---
title: Lähes reaaliaikainen tietojen integrointi Common Data Servicen kanssa
description: Tässä ohjeaiheessa on yleiskatsaus Finance and Operationsin ja Common Data Servicen integroinnista.
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
ms.openlocfilehash: 072564446b74318ffc8e8e6ad4fd16f4421e7854
ms.sourcegitcommit: d0322d1ed6c798301058e44dae76227a0e1f49ac
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/26/2019
ms.locfileid: "2853903"
---
# <a name="near-real-time-data-integration-with-common-data-service"></a>Lähes reaaliaikainen tietojen integrointi Common Data Servicen kanssa

[!include [banner](../includes/banner.md)]

Nykyisessä digitaalisessa maailmassa liiketoiminnan ekosysteemit käyttävät Microsoft Dynamics 365 -sovelluksia kokonaisuutena. Koska henkilöiden, asiakkaiden, operaatioiden ja esineiden internetin (IoT) laitteiden tiedot virtaavat yhteen lähteeseen, on mahdollista, että digitaaliset palautesilmukat ovat käytettävissä. Tämän kokemuksen saavuttamiseksi Finance and Operations -sovellusten ja Dynamics 365 -sovellusten välinen integrointi on välttämätöntä. Jotkin sovellukset perustuvat Common Data Serviceen. Finance and Operations -sovellusten tietojen ja Common Data Servicen integrointi antaa muille sovelluksille mahdollisuuden viestiä johdonmukaisesti ja sujuvasti Finance and Operationsin kanssa.

Finance and Operations -sovellukset ja Common Data Service mahdollistavat lähes reaaliaikaista tietojen synkronointia Finance and Operations -sovellusten ja muiden Dynamics 365 -sovellusten välillä kaksoiskirjoituskehyksen avulla. Kattavuus on laaja ja kattaa 28 sovelluksen osa-aluetta. Tavoitteena on tarjota yksi yhdenmukainen Dynamics 365 -käyttäjäkokemus saumattomien tietovirtojen kautta, jotka yhdistävät liiketoimintaprosesseja eri sovelluksissa.

![Arkkitehtuurin yleiskuvauskaavio](media/dual-write-overview.jpg)

Käytössä on seuraavat arvoehdotukset:

+ [Organisaatiohierarkia Common Data Servicessa](dual-write-organization.md)
+ [Yrityksen käsite Common Data Servicessa](dual-write-company.md)
+ [Integroidut asiakkaiden päätiedot](dual-write-customer.md)
+ [Integroitu kirjanpito](dual-write-ledger.md)
+ [Yhtenäinen tuotekokemus](dual-write-product.md)
+ [Integroidut toimittajien päätiedot](dual-write-vendor.md)
+ [Integroidut toimipaikat ja varastot](dual-write-sites-and-warehouses.md)
+ [Integroidut veron päätiedot](dual-write-tax.md)

## <a name="system-requirements"></a>Järjestelmävaatimukset

Synkroniset, kaksisuuntaiset, lähes reaaliaikaiset tietovirrat vaativat seuraavat versiot:

+ Microsoft Dynamics 365 for Finance and Operationsin versio 10.0.4 (heinäkuu 2019) ja Platform update 28 tai uudempi
+ Microsoft Dynamics 365 for Customer Engagement, Platform -versio 9.1 (4.2) tai uudempi

## <a name="setup-instructions"></a>Määritysohjeet

Määritä Finance and Operations -sovellusten ja Common Data Servicen integrointi seuraavasti.
    
1. Kaksoiskirjoitusjärjestelmän asennusta varten katso [vaiheittainen opas](https://aka.ms/dualwrite-docs) kaksoiskirjoituksen esiversion julkistamisessa.
2. Lataa ja asenna ratkaisu [FIN Ops- ja CDS/CE-integraatiosta kaksoiskirjoitus-](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=66052096) Yammer-ryhmän kautta. Paketti sisältää viisi ratkaisua:

    + Dynamics365Company
    + CurrencyExchangeRates
    + Dynamics365FinanceAndOperationsCommon
    + Dynamics365FinanceCommon
    + Dynamics365SupplyChainCommon

3. Noudata suoritusjärjestystä [alkuperäisten viitetietojen synkronoinnissa](dual-write-initial.md).
4. Jos kohtaat kaksoiskirjoitussynkronoinnin ongelmia, katso [tietojen integroinnin vianetsintäopas](dual-write-troubleshooting.md).

> [!IMPORTANT]
> Et voi suorittaa kaksoiskirjoitusta ja [Prospektista käteiseksi -prosessia](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/accounts-template-mapping-direct) rinnakkain. Jos käytössäsi on Prospektista käteiseksi -ratkaisu, sinun on poistettava sen asennus. Sinun on myös poistettava käytöstä asiakkaan ja toimittajan kaksoiskirjoitusmallit, jotka ovat osa Prospektista käteiseksi -ratkaisua.
