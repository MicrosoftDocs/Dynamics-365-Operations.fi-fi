---
title: Automaattinen vahvistus ja suunnittelun optimointi
description: Tässä ohjeaiheessa käsitellään automaattista vahvistusta ja suunnittelun optimointia.
author: ChristianRytt
manager: tfehr
ms.date: 11/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-11-30
ms.dyn365.ops.version: AX 10.0.7
ms.openlocfilehash: d014fcd542462e092f6e88232dff8fd5ee2253c1
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4963457"
---
# <a name="autofirming-with-planning-optimization"></a>Automaattinen vahvistus ja suunnittelun optimointi

[!include [banner](../../includes/banner.md)]

Automaattisen vahvistuksen avulla voit vahvistaa (eli vapauttaa) suunnitellut tilaukset pääsuunnitteluprosessin osana. Kun suunnitellut tilaukset vahvistetaan, ne muunnetaan varsinaisiksi osto-, siirto- tai tuotantotilauksiksi. Kun suunnittelun optimointia käytetään, suunnitellut tilaukset vahvistetaan pääsuunnitteluajon aikana silloin, kun tilauspäivä (eli aloituspäivä) on vahvistuksen aikarajan sisällä.

> [!NOTE]
> Suunnitellut ostotilauksen automaattinen vahvistus on mahdollista vain, jos nimike on liitetty toimittajaan.

## <a name="turn-on-autofirming"></a>Automaattisen vahvistuksen ottaminen käyttöön

Automaattinen vahvistus otetaan käyttöön seuraavasti:

1. Valitse **Toimintojen hallinta** -työtilan **Uusi**-lehden luettelossa **Suunnittelun optimoinnin automaattinen vahvistus**. Jos toiminto ei ole **Uusi**-välilehdessä, tarkista myös **Ei käytössä**- ja **Kaikki**-välilehdet.
1. Valitse **Ota käyttöön nyt**. Vaihtoehtoisesti voi valita **Aikataulu** ja valita sitten ajan, jolloin haluat ottaa toiminnon käyttöön.

## <a name="set-up-the-firming-time-fence"></a>Vahvistuksen aikarajan määrittäminen

Vahvistuksen aikaraja lasketaan eteenpäin pääsuunnittelun ajopäivämäärästä. Se määritetään sen mukaan, kuinka monta päivää ilmoitat. Vahvistuksen aikarajaa voi hallita seuraavilla tavoilla:

- Voit määrittää kattavuusryhmän vahvistuksen oletusaikarajan valitsemalla ensin **Pääsuunnittelu** \> **Asetukset** \> **Kattavuus** \> **Kattavuusryhmät** ja valitsemalla sitten kattavuusryhmän. Anna sitten päivien määrä **Muu**-pikavälilehden **Automaattisen vahvistuksen aikaraja (päivää)** -kentässä.
- Voit ohittaa tietyn nimikkeen kattavuusryhmälle määritetyn vahvistuksen aikarajan valitsemalla ensin **Tuotetietojen hallinta** \> **Vapautetut tuotteet**, sitten toimintoruudussa **Suunnitelma** ja lopuksi **Nimikkeen kattavuus**. Valitse tämän jälkeen **Yleiset**-välilehdessä **Ohita aikarajat** ja anna päivien määrä **Automaattisen vahvistuksen aikaraja (päivää)** -kentässä.
- Voit ohittaa tietylle kattavuusryhmälle määritetyn aikarajan ja tietyn pääsuunnitelman nimikkeen kattavuuden valitsemalla ensin **Pääsuunnittelu** \> **Asetukset** \> **Pääsuunnitelmat** ja valitsemalla sitten pääsuunnitelman. Anna sitten päivien määrä valitsemalla **Aikarajat päivinä** -pikavälilehdessä **Vahvistus**-asetukseksi **Kyllä**.

Jos automaattinen vahvistus on otettu käyttöön suunnittelun optimointia käyttävässä pääsuunnitteluajossa, automaattinen vahvistusprosessi tehdään automaattisten vahvistusasetusten mukaisesti. Jos automaattinen vahvistusta ei ole otettu käyttöön tai jos suunnittelu käynnistetään **Nettotarpeet**-sivulta, automaattinen vahvistusprosessi ohitetaan.

## <a name="planning-optimization-vs-the-built-in-supply-chain-management-planning-engine"></a>Suunnittelun optimoinnin ja Supply Chain Managementin sisäisen suunnittelumoduulin vertailu

Sekä suunnittelun optimointia että Microsoft Dynamics 365 Supply Chain Managementiin sisältyvää suunnittelumoduulia voi käyttää suunniteltujen tilausten automaattiseen vahvistamiseen. Niillä on kuitenkin tärkeitä eroavaisuuksiakin. Esimerkiksi siinä missä suunnittelun optimointi käyttää tilauspäivää (eli aloituspäivää) määrittämään, mitkä suunnitellut tilaukset vahvistetaan, Supply Chain Managementin sisäinen suunnittelumoduuli käyttää tarvepäivää (eli päättymispäivää). Yhteenveto eroista:

**Suunnittelun optimointi**

- Automaattinen vahvistus perustuu tilauspäivään (aloituspäivään).
- Koska tilauspäivä (aloituspäivä) käynnistää vahvistuksen, läpimenoaikaa ei tarvitse sisällyttää vahvistuksen aikarajaan.
- Jos haluat vahvistaa kaikki tilaukset, joiden on käynnistyttävä kuluvana viikkona, vahvistuksen aikarajan on oltava yksi viikko.

**Supply Chain Managementin sisäinen suunnittelumoduuli**

- Automaattinen vahvistus perustuu tarvepäivään (päättymispäivään).
- Vahvistuksen aikarajan on oltava pidempi kuin läpimenoajan, jotta voidaan varmistaa, että tilaukset vahvistetaan ajoissa.
- Jos haluat vahvistaa kaikki tilaukset, joiden on käynnistyttävä kuluvana viikkona, vahvistuksen aikarajan on oltava läpimenoaika plus yksi viikko.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]