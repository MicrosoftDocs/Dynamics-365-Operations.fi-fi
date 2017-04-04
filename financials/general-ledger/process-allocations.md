---
title: "Kohdistusten käsittely"
description: "Tässä artikkelissa on tietoja, käsitellään niitä Microsoft Dynamics-365 toiminnoissa ja miten niitä voidaan käyttää budjetin suunnittelussa vaihtoehtoja. Kohdistuksia käytetään jaettaessa summia useiden kirjanpitotiliyhdistelmien kesken. Niiden avulla varmistetaan, että kulut tai tuotto veloitetaan oikealta kohteelta kirjanpidossa."
author: twheeloc
manager: AnnBe
ms.date: 2017-04-04
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: AccountingDistribution, LedgerAllocationRule, MainAccount
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 17361
ms.assetid: 04c8548a-0af9-492b-954b-946b4f8ca023
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9f4d7fdd8cfa7a540fce219f6ae4792e57dfbe44
ms.openlocfilehash: 37f4df5d0b79208a8c565bc9101ddde193a6ef5b
ms.lasthandoff: 03/31/2017


---

# <a name="process-allocations"></a>Kohdistusten käsittely

Tässä artikkelissa on tietoja, käsitellään niitä Microsoft Dynamics-365 toiminnoissa ja miten niitä voidaan käyttää budjetin suunnittelussa vaihtoehtoja. Kohdistuksia käytetään jaettaessa summia useiden kirjanpitotiliyhdistelmien kesken. Niiden avulla varmistetaan, että kulut tai tuotto veloitetaan oikealta kohteelta kirjanpidossa.

Microsoft Dynamics-365 toiminnoissa on tukea tätä prosessia seuraavia ominaisuuksia:

-   Tapahtumasummat manuaalisesti kohdistaa kirjanpidolliset jaot Jaa-toiminnolla tai käyttämällä taloushallinnon dimension oletusmallit asiakirjaan. Lisätietoja on ohjeaiheessa [kirjanpidolliset jaot.](\accounts-payable\accounting-distributions.md)
-   Kohdista automaattisesti tapahtumien summat perustuen yksittäisen päätilin määritettyihin kohdistusehtoihin. Jokaiselle kirjauskansiolle, joka perustuu prosenttiosuuteen ja kohteen kirjanpitotiliin aina kun kirjaus täyttää lähteenä pidetyn kirjanpitotilin kriteerit, kun luodaan kohdistus tilitapahtumiin.
-   Kohdista automaattisesti kirjanpitosaldot tai summat, jotka perustuvat kiinteisiin kirjanpidon sääntöihin. Kirjanpidon kohdistussäännöt käsitellään sännöllisin väliajoin käyttäen kohdistuksen kirjauskansioita. 

###  <a name="allocations-in-budget-planning"></a>Budjettisuunnittelun kohdistukset

Kirjanpidon kohdistussääntöjä voidaan käyttää budjettisuunnitelmiin. Käytettäessä kirjanpidon kohdistussääntöjä budjettisuunnitelmassa, kohdistuksen säännöt toimivat samalla tavalla kuin tavallisessa kirjanpidossa, mutta lähdetietojen ja kohteen tiedot tulevat budjettisuunnitelmasta. Voit manuaalisesti valita kirjanpidon kohdistussäännöt, joita budjettisuunnitelmissa käytetään. Vaihtoehtoisesti voit käyttää kohdistusaikataulua, joka suoritetaan osana työnkulkuprosessia.

> [!NOTE]
> Et voi käyttää konsernin sisäisen kirjanpidon kohdistussääntöjä budjettisuunnittelussa.




