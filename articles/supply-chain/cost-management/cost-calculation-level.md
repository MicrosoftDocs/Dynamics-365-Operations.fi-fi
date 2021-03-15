---
title: Kustannuslaskentataso
description: Tässä aiheessa kuvataan tuoterakennetaso, jonka nimi on kustannuslaskennassa käytettävä taso. Tämä tuoterakennetaso ei sisällä tuotanto- ja erätilauksia laskelmista.
author: AndersGirke
manager: tfehr
ms.date: 04/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2020-04-23
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: 42088d8c005cf3fc04e768f1b8e8c8ca0b8c6993
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4967723"
---
# <a name="cost-calculation-level"></a>Kustannuslaskentataso

Tuoterakennetaso, jonka nimi on **Kustannuslaskentataso**, jättää tuotantotilaukset ja erätilaukset pois laskelmista. Järjestelmä käyttää tätä tasoa, kun se suorittaa kustannuslaskelmia kustannuslaskelmaversioissa. Järjestelmä käyttää sen sijaan **Kustannuslaskentataso**-tuoterakennetasoa prosesseissa, kuten uudelleenlaskennassa ja varaston sulkemisessa.

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