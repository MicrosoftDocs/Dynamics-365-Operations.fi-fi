---
title: Pyyntö- ja istuntotietojen välinen odottamaton ero testauksen aikana
description: Odottamaton ero tapahtuu varastosovelluksen tehtävätarkistuksen tulosten pyyntö- ja istuntotietojen välillä.
author: mamuszal
ms.date: 03/11/2022
ms.topic: troubleshooting
ms.search.form: WHSValidatorRunInstance_executeRun
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mamuszal
ms.search.validFrom: 2022-03-11
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: da8f0506a76b0d0cc02bfc2e1bff01b4ddccb578
ms.sourcegitcommit: 941119133be1765f653d5d5270dfdf58466e1d07
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/17/2022
ms.locfileid: "8456936"
---
# <a name="unexpected-difference-between-request-and-session-data-during-testing"></a>Pyyntö- ja istuntotietojen välinen odottamaton ero testauksen aikana

Virhekoodi: WarehouseMobileDeviceRequestInputValidationError

## <a name="symptoms"></a>Oireet

Kun käytät [varastosovelluksen tehtävänvahvistuskehystä](/dynamics365-release-plan/2019wave2/dynamics365-supply-chain-management/warehouse-app-task-validation-rsat), tarkistus palauttaa seuraavan virhesanoman:

> Pyyntö- ja istuntotietojen välinen odottamaton ero. Varaston matkaviestinlaitteiden XML-protokollaa rikotaan.REQUEST_XML_TAMPERING

## <a name="cause"></a>Syy

Virhe ilmenee, kun testin suorittamisen aikana onnistuneesti suoritettu viimeisen vaiheen tuloste ei vastaa seuraavan vaiheen tallennettua syöttöä. Tämä tilanne voi syntyä, koska tehtävän validoija ei käytä edellisen vaiheen tulosta sen syötteenä seuraavaan vaiheeseen. Sen sijaan se käyttää tallennettua XML:ää kunkin vaiheen syötteenä.

Useimmissa tapauksissa virhe ilmenee, kun suoritat tehtävän uudelleen, mutta testi edellyttää tietueita, joita saman tehtävän edellisen ajon muokannut tai poistanut.

## <a name="resolution"></a>Ratkaisu

Varastosovelluksen tehtävän oikeellisuustarkistuksen testiajo ei ole idempotenttinen toiminto, vaan muuttaa pohjana olevia tietoja. Ennen kuin suorittaa tehtävän uudelleen, asianmukaiset tiedot on ehkä palautettava.

1. Tarkista viimeisen onnistuneen testin vaiheen tuloste-XML ja määritä, mistä testi suoritetaan.
1. Tarkista testi ja varmista, että kaikki tarvittavat myyntitilaukset, siirtotilaukset, työotsikot ja muut tietueet ovat yhä olemassa ja odotetussa tilassa.
1. Luo tai muokkaa uudelleen puuttuvia tai muokattuja tietueita. Voit myös luoda uusia testiasetuksia ja suunnitella testin, jotta aiemmin luotuja tietueita voidaan käyttää.
