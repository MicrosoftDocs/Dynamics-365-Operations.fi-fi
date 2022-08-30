---
title: Kustannuslaskentataso
description: Tässä artikkelissa kuvataan tuoterakennetaso, jonka nimi on kustannuslaskennassa käytettävä taso. Tämä tuoterakennetaso ei sisällä tuotanto- ja erätilauksia laskelmista.
author: JennySong-SH
ms.date: 08/05/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2020-04-23
ms.dyn365.ops.version: 10.0.12
ms.openlocfilehash: e63a868696e36c1d4f5d19ea87bdf4d682c39f8c
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/23/2022
ms.locfileid: "9334952"
---
# <a name="cost-calculation-level"></a>Kustannuslaskentataso

[!include [banner](../includes/banner.md)]

Tuoterakennetaso, jonka nimi on **Kustannuslaskentataso**, jättää tuotantotilaukset ja erätilaukset pois laskelmista. Järjestelmä käyttää tätä tasoa, kun se suorittaa kustannuslaskelmia kustannuslaskelmaversioissa. Järjestelmä käyttää sen sijaan **Kustannuslaskentataso**-tuoterakennetasoa prosesseissa, kuten uudelleenlaskennassa ja varaston sulkemisessa.

## <a name="turn-the-cost-calculation-level-feature-on-or-off"></a>Kustannuslaskentataso-toiminnon käyttöönotto tai käytöstäpoisto

Jos haluat käyttää tätä ominaisuutta, se on otettava käyttöön järjestelmässä. Supply Chain Managementin versiosta 10.0.29 alkaen tämä ominaisuus on oletusarvoisesti käytössä. Järjestelmänvalvojat voivat ottaa tämän toiminnon käyttöön tai pois käytöstä hakemalla *Kustannuslaskentataso*-toimintoa [Toimintojen hallinta](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) -työtilassa.

## <a name="example-scenario"></a>Esimerkkiskenaario

Seuraavassa yksinkertaisessa skenaariossa näkyvät **kustannuslaskentatason** tuoterakennetason ja **Kustannustason** tuoterakennetason erot.

Sinulla on kolme tuotetta: A, B ja C. Tuote C on tuotteen B komponentti, ja tuote B on tuotteen A komponentti.

- **Kustannustaso** määrittää seuraavat tuoterakennetasot:

    - **Tuote A:** 0
    - **Tuote B:** 1
    - **Tuote C:** 2

- **Kustannuslaskentataso** määrittää seuraavat tuoterakennetasot:

    - **Tuote A:** 0
    - **Tuote B:** 1
    - **Tuote C:** 2

Tuotteen C tuotantotilaus luodaan ja tuote A lisätään tuotantotilauksen tuoterakenteeseen. Kun tilaus on arvioitu, tuoterakennetasot päivitetään seuraavalla tavalla:

- **Kustannustaso** määrittää seuraavat tuoterakennetasot:

    - **Tuote B:** 1
    - **Tuote C:** 2
    - **Tuote A:** 3

- **Kustannuslaskentataso** määrittää seuraavat tuoterakennetasot:

    - **Tuote A:** 0
    - **Tuote B:** 1
    - **Tuote C:** 2

Tämä toiminto varmistaa, että tuotantotilauksen tuoterakenteiden muutokset eivät vaikuta seuraaviin kustannuslaskelmiin.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]