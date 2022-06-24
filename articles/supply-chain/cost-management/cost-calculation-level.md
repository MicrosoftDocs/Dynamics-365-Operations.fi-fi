---
title: Kustannuslaskentataso
description: Tässä artikkelissa kuvataan tuoterakennetaso, jonka nimi on kustannuslaskennassa käytettävä taso. Tämä tuoterakennetaso ei sisällä tuotanto- ja erätilauksia laskelmista.
author: JennySong-SH
ms.date: 04/23/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2020-04-23
ms.dyn365.ops.version: 10.0.12
ms.openlocfilehash: 647ef4b13b864cfdbb7905fe7a0d340e85f6c1e6
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8850870"
---
# <a name="cost-calculation-level"></a>Kustannuslaskentataso

[!include [banner](../includes/banner.md)]

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