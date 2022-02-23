---
title: Kuljetuskuorman osatoimitus
description: Tässä ohjeaiheessa käsitellään kuorman osittaista toimittamista ja kuormituksen kapasiteettisuunnittelun lykkäämistä.
author: Mirzaab
manager: tfehr
ms.date: 03/15/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSTransportLoad
audience: Application User
ms.reviewer: kamaybac
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 68a3d175e89e89d0909b140863b1aa61a184fce6
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4963282"
---
# <a name="partial-shipment-of-a-transport-load"></a>Kuljetuskuorman osatoimitus

[!include[banner](../includes/banner.md)]

Kun kuormille määritetään osatoimitus, voit käsitellä kuormia, joiden kapasiteettia ei voi määrittää, ennen kuin kaikki myyntirivit on lisätty kuormaan. Prosessi voidaan sitten viimeistellä, kuormalavojen tarkka määrä on tiedossa. Näin ollen sinun ei tarvitse päättää kuormalavojen määrittämistä tiettyyn kuljetukseen, ennen kuin kuljetus fyysisesti lastataan vaiheistetusta varastosta.

Tämä ominaisuus on vaihtoehto sellaisen jäykän rakenteen noudattamiselle, jos kuormalavat on määritettävä kuljetukseen ennen keräily- tai lastaustyön luontia. Käyttäjät voivat sen sijaan yksittäisiä kuormia osatoimituksen vahvistukseen. Kyseisten kuormien lastausprosessit ovat sitten mahdollisia. Kuljetuksen suunnitteluosasto voikin suunnitella kuormia ilman, että yksittäisten kuljetusten kapasiteetti olisi otettava huomioon.

Työntekijät voivat määrittää lastauksen aikana uuden kuljetuskuorman, johon kuormalava lastataan. Vaihtoehtoisesti he voivat tunnistaa aiemmin luodun kuljetuskuorman. Nämä tiedot voidaan tallentaa mobiililaitteella. Niinpä useat varastotyöntekijät voivat lastata samojen tai eri kuormien varastoa samaan kuorma-autoon. Kuormat voidaan sitten toimittaa kokonaan tai osittain.

> [!NOTE] 
> Jos kuorman varastoa voitaisiin lastata tiettyyn kuormaan tai kuorman osatoimitus voitaisiin tehdä, työ on luotava käyttämällä työmallin lastausluokkaa. Tavallista **Keräily**-tyypin keräilytyötä ei voi lastata kuljetuksen kuormaan, kuten kuorma-autoon.

## <a name="set-up-transport-loads-for-partial-shipment"></a>Osatoimituksen kuljetuskuorman määrittäminen

Kuormien osatoimitusten määrittäminen koostuu kahdesta menettelystä.

### <a name="set-the-loading-strategy"></a>Kuormitusstrategian määrittäminen

Osakuormitus on otettava käyttöön määrittämällä kuormitusstrategia. Voit määrittää kuormitusstrategian sen jälkeen, kun olet luonut kuorman.

1. Valitse **Varastonhallinta** \> **Kuormat** \> **Kaikki kuormat**.
2. Valitse ensin kuorma ja sitten **Ylätunniste**.
3. Valitse **Kuormitusstrategia**-kentässä **Osittaisen kuorman lähetys on sallittu**.

### <a name="create-a-menu-item-for-loading-of-transport-loads"></a>Valikkovaihtoehdon luominen kuljetuskuormien lastaamiselle

Sinun on luotava uusi valikkovaihtoehto, joka mahdollistaa kuljetuskuormien lastaamisen. Kuljetuskuorman avulla voi ryhmittää yhden tai usean kuorman työrivit. Kaikki kuljetuskuormaan lisättävä voidaan sitten lähettää käyttämällä mobiililaitetta.

1. Valitse **Varastonhallinta** \> **Asetukset** \> **Mobiililaite** \> **Mobiililaitteen valikkovaihtoehdot**.
2. Valitse ensin **Uusi** ja sitten **Menetelmä** -kentässä **Työ**.
3. Valitse **Käytä nykyistä työtä** -asetukseksi **Kyllä**.
4. Valitse **Yleinen**-välilehden **Ohjaaja**-kentässä **Kuljetuksen kuormaus**.
5. Voit ottaa käyttöön lähetyksen vahvistamisen mobiililaitteella valitsemalla **Sallittu lähetyksen vahvistuksen tyyppi** -kentässä **Kuljetuksen kuorma**.

## <a name="confirm-shipment-of-a-transport-load-from-the-client"></a>Kuljetuksen kuorman lähetyksen vahvistus asiakasohjelmasta

Tällä asetuksella voi vahvistaa, että täyden kuorman tai osakuorman sisältävä kuljetuksen kuorma voidaan lähettää.

1. Valitse **Varastonhallinta** \> **Kuormat** \> **Kuljetuksen kuormat**.
2. Valitse toimintoruudun **Lähetä ja vastaanota** -välilehden **Vahvista**-ryhmässä **Kuljetus**.
