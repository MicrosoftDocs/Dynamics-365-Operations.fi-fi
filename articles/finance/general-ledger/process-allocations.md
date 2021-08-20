---
title: Kohdistusten käsittely
description: Tässä artikkelissa on tietoja kohdistuksista, niiden käsittelyvaihtoehdoista Microsoft Dynamics 365 Financessa ja kohdistusten käyttämisestä budjettisuunnittelussa. Kohdistuksia käytetään jaettaessa summia useiden kirjanpitotiliyhdistelmien kesken. Niiden avulla varmistetaan, että kulut tai tuotot veloitetaan oikealta kohteelta kirjanpidossa.
author: ShylaThompson
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AccountingDistribution, LedgerAllocationRule, MainAccount
audience: Application User
ms.reviewer: roschlom
ms.custom: 17361
ms.assetid: 04c8548a-0af9-492b-954b-946b4f8ca023
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4f57991e0c7eb533a070724b9d23996128342d91d8473614e1bb1a996707545c
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6774302"
---
# <a name="process-allocations"></a>Kohdistusten käsittely

[!include [banner](../includes/banner.md)]

Tässä artikkelissa on tietoja kohdistuksista, niiden käsittelyvaihtoehdoista ja kohdistusten käyttämisestä budjettisuunnittelussa. Kohdistuksia käytetään jaettaessa summia useiden kirjanpitotiliyhdistelmien kesken. Niiden avulla varmistetaan, että kulut tai tuotot veloitetaan oikealta kohteelta kirjanpidossa.

Seuraavat ominaisuudet tukevat tätä prosessia:

-   Kohdista tapahtumasummat manuaalisesti käyttämällä jako-toimintoa kirjanpidollisessa jaossa tai käyttämällä asiakirjan taloushallinnon dimension oletusarvomalleja. Lisätietoja on kohdassa [Kirjanpidolliset jaot](../accounts-payable/accounting-distributions.md)
-   Kohdista automaattisesti tapahtumien summat perustuen yksittäisen päätilin määritettyihin kohdistusehtoihin. Jokaiselle kirjauskansiolle, joka perustuu prosenttiosuuteen ja kohteen kirjanpitotiliin aina kun kirjaus täyttää lähteenä pidetyn kirjanpitotilin kriteerit, kun luodaan kohdistus tilitapahtumiin. Lisätietoja on ohjeaiheessa [Päätilin kohdistusehdot](../general-ledger/main-account-allocation-terms.md)
-   Kohdista automaattisesti kirjanpitosaldot tai summat, jotka perustuvat kiinteisiin kirjanpidon sääntöihin. Kirjanpidon kohdistussäännöt käsitellään sännöllisin väliajoin käyttäen kohdistuksen kirjauskansioita. Lisätietoja on kohdassa [Kohdistussäännöt](../general-ledger/ledger-allocation-rules.md).

###  <a name="allocations-in-budget-planning"></a>Budjettisuunnittelun kohdistukset

Kirjanpidon kohdistussääntöjä voidaan käyttää budjettisuunnitelmiin. Käytettäessä kirjanpidon kohdistussääntöjä budjettisuunnitelmassa, kohdistuksen säännöt toimivat samalla tavalla kuin tavallisessa kirjanpidossa, mutta lähdetietojen ja kohteen tiedot tulevat budjettisuunnitelmasta. Voit manuaalisesti valita kirjanpidon kohdistussäännöt, joita budjettisuunnitelmissa käytetään. Vaihtoehtoisesti voit käyttää kohdistusaikataulua, joka suoritetaan osana työnkulkuprosessia.

> [!NOTE]
> Et voi käyttää konsernin sisäisen kirjanpidon kohdistussääntöjä budjettisuunnittelussa.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]