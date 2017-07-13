---
title: "Kohdistusten käsittely"
description: "Tässä artikkelissa on tietoja kohdistuksista, niiden käsittelyvaihtoehdoista Microsoft Dynamics 365 for Finance and Operations, Enterprise Editionissa ja kohdistusten käyttämisestä budjettisuunnittelussa. Kohdistuksia käytetään jaettaessa summia useiden kirjanpitotiliyhdistelmien kesken. Niiden avulla varmistetaan, että kulut tai tuotto veloitetaan oikealta kohteelta kirjanpidossa."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AccountingDistribution, LedgerAllocationRule, MainAccount
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 17361
ms.assetid: 04c8548a-0af9-492b-954b-946b4f8ca023
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 298ac47e2253f8add1aa3938dda15afe186afbeb
ms.openlocfilehash: e6d88503972850f6163aba6b45547a111f44abab
ms.contentlocale: fi-fi
ms.lasthandoff: 06/20/2017


---

# Kohdistusten käsittely
<a id="process-allocations" class="xliff"></a>

[!include[banner](../includes/banner.md)]


Tässä artikkelissa on tietoja kohdistuksista, niiden käsittelyvaihtoehdoista Microsoft Dynamics 365 for Finance and Operations, Enterprise Editionissa ja kohdistusten käyttämisestä budjettisuunnittelussa. Kohdistuksia käytetään jaettaessa summia useiden kirjanpitotiliyhdistelmien kesken. Niiden avulla varmistetaan, että kulut tai tuotto veloitetaan oikealta kohteelta kirjanpidossa.

Microsoft Dynamics 365 for Finance and Operations tarjoaa seuraavat ominaisuudet tukemaan tätä prosessia:

-   Kohdista tapahtumasummat manuaalisesti käyttämällä jako-toimintoa kirjanpidollisessa jaossa tai käyttämällä asiakirjan taloushallinnon dimension oletusarvomalleja. Lisätietoja on kohdassa [Kirjanpidolliset jaot](../accounts-payable/accounting-distributions.md)
-   Kohdista automaattisesti tapahtumien summat perustuen yksittäisen päätilin määritettyihin kohdistusehtoihin. Jokaiselle kirjauskansiolle, joka perustuu prosenttiosuuteen ja kohteen kirjanpitotiliin aina kun kirjaus täyttää lähteenä pidetyn kirjanpitotilin kriteerit, kun luodaan kohdistus tilitapahtumiin.
-   Kohdista automaattisesti kirjanpitosaldot tai summat, jotka perustuvat kiinteisiin kirjanpidon sääntöihin. Kirjanpidon kohdistussäännöt käsitellään sännöllisin väliajoin käyttäen kohdistuksen kirjauskansioita. 

###  Budjettisuunnittelun kohdistukset
<a id="allocations-in-budget-planning" class="xliff"></a>

Kirjanpidon kohdistussääntöjä voidaan käyttää budjettisuunnitelmiin. Käytettäessä kirjanpidon kohdistussääntöjä budjettisuunnitelmassa, kohdistuksen säännöt toimivat samalla tavalla kuin tavallisessa kirjanpidossa, mutta lähdetietojen ja kohteen tiedot tulevat budjettisuunnitelmasta. Voit manuaalisesti valita kirjanpidon kohdistussäännöt, joita budjettisuunnitelmissa käytetään. Vaihtoehtoisesti voit käyttää kohdistusaikataulua, joka suoritetaan osana työnkulkuprosessia.

> [!NOTE]
> Et voi käyttää konsernin sisäisen kirjanpidon kohdistussääntöjä budjettisuunnittelussa.






