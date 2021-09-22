---
title: Virhe, kun tila muutetaan Ilmoitettu valmiiksi -tilasta tilaan Lopetus
description: Virhe voi ilmetä, kun tuotantotilauksen tila muutetaan Ilmoitettu valmiiksi -tilasta tilaan Lopetus. Tällä sivulla selitetään, miten ongelma korjataan.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 744637f5cccffe44b85f77c1a9df2034012fac40
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476234"
---
# <a name="error-when-changing-status-of-production-order-from-reported-as-finished-to-end"></a>Virhe, kun tuotantotilauksen tilaksi muutetaan Ilmoitettu valmiiksi -tilasta tilaan Lopetus

## <a name="symptoms"></a>Oireet

Kun tuotantotilauksen Ilmoitettu valmiiksi -tila vaihtuu tilaksi Lopetus, jokin seuraavista virhesanomaista avautuu:

> Päivitysristiriita. Standardikustannus ei vastaa kirjanpitovaraston arvoa päivityksen jälkeen.

> Vakava virhe toiminnossa InventCostMovement.checkVariance.

## <a name="cause"></a>Syy

Tämä ongelma esiintyy, koska toinen prosessi on muuttanut taustalla olevia tietoja. Prosessi yrittää päivittää tiedot enintään viisi kertaa. Jos ristiriita esiintyy vielä viidennen yrityksen jälkeen, saat jonkin edellä mainituista sanomista.

## <a name="resolution"></a>Ratkaisu

Tämä on suunniteltu ominaisuus. Korjaa ongelma jatkamalla erätyötä. Se suorittamisen pitäisi onnistua.

Jos erätyön suorittaminen epäonnistuu toistuvasti jatkamisen jälkeen, tarkista, että kirjanpidon oletusvaluutan pyöristystarkkuus on yhteensopiva InventSum-taulukossa käytettyjen arvojen pyöristyksen kanssa. Jos pyöristystarkkuus on vaihdettu ei-yhteensopivaksi arvoksi, se on luultavasti muutettava takaisin yhteensopivaksi arvoksi. Etsi **ModifiedDateTime**. Tässä tapauksessa arvo yleensä näyttää, että pyöristystarkkuutta on muutettu äskettäin.
