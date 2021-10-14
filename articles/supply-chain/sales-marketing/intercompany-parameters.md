---
title: Konsernin sisäiset parametrit
description: Tässä aiheessa käsitellään konsernin sisäisiä parametreja.
author: GalynaFedorova
ms.date: 09/01/2021
ms.topic: article
ms.search.form: PurchTable, PurchTablePart, PurchLineOpenOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 705efee84b255105ba39c603d23d2509e77b331a
ms.sourcegitcommit: fcfd85a508c0de52cfe11d1986892219e39ef406
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/23/2021
ms.locfileid: "7548241"
---
# <a name="intercompany-parameters"></a>Konsernin sisäiset parametrit

[!include [banner](../../includes/banner.md)]

Konsernin sisäisessä organisaatiossa voidaan parametrien avulla määrittää, miten kaupankäynti tapahtuu eri yritysten välillä. Valitut kentät määrittävät nämä parametrit. Erilaisiin kaupankäyntiskenaarioihin voidaan valita erilaisia parametriyhdistelmiä.

Seuraavassa kahdessa esimerkissä käsitellään konsernin sisäisiä organisaatioita, joista toisessa on kaksi tasoa ja toisessa kolme tasoa.

## <a name="example-1-two-level-intercompany-chain"></a>Esimerkki 1: kaksitasoinen konserniyritys

Konsernin sisäinen organisaatio sisältää seuraavat yritykset:

- Yritys A – Myynti ulkoisille asiakkaille; ei omaa varastoa. Tämä yritys ostaa yritykseltä B.
- Yritys B – myyntiä vain yritykselle A.

Nämä yritykset voivat myydä toisilleen ja ostaa toisiltaan.

Tässä esimerkissä ulkoista asiakasta koskevan alkuperäisen myyntitilauksen hinnoittelu perustuu aina myyntihintaan. Konsernin sisäisen myyntitilauksen ja ostotilauksen hinnoittelu määräytyy yrityksen B konsernin sisäisen myyntitilauksen sisäisten myynti- tai ostohintojen mukaan.

Tilauksen otsikkotiedot tulevat ulkopuolisen asiakkaan alkuperäisestä ostotilauksesta. Mahdolliset muutokset konsernin sisäisessä myyntitilauksessa eivät siirry alkuperäiseen myyntitilaukseen.

Valitse yrityksen A toimittajien **Konsernin sisäinen** -sivulla **Ostotilauskäytännöt**. Valitse seuraavat kentät **Alkuperäinen myyntitilaus (suoratoimitus)** -kenttäryhmässä:

- **Tulosta pakkausluettelo automaattisesti**
- **Kirjaa lasku automaattisesti**
- **Tulosta lasku automaattisesti**

Valitse seuraava kenttä **Konsernin sisäinen myyntitilaus (suoratoimitus)** -kenttäryhmässä:

- **Kirjaa lasku automaattisesti**

Valitse seuraavat kentät **Alkuperäinen myyntitilaus <->Konsernin sisäinen ostotilaus** -ryhmässä:

- **Asiakkaan tiedot**
- **RMA-numero**

Valitse seuraavat kentät **Konsernin sisäinen ostotilaus <->Konsernin sisäinen myyntitilaus** -kenttäryhmässä:

- **Asiakkaan tiedot**
- **RMA-numero**
- **Eränumero**
- **Sarjanumero**

Valitse yrityksen B asiakkaiden **Konsernin sisäinen** -sivulla **Myyntitilauskäytännöt**. Valitse seuraavat kentät **Konsernin sisäisen myyntitilauksen luonti** -kenttäryhmässä:

- **Myyntitilausten numerointi** : **Yritys + alkuperäinen numero**
- **Salli alkuperäiselle asiakkaalle tiedostojen päivitysyhteenveto**

Valitse seuraavat kentät **Konsernin sisäisen myyntitilauksen hinnat** -kenttäryhmässä:

- **Hinnan ja alennuksen haku**
- **Salli hinnan muokkaus**
- **Salli alennuksen muokkaus**

Valitse seuraavat kentät **Konsernin sisäinen myyntitilaus \> Konsernin sisäinen ostotilaus** -kenttäryhmässä:

- **Eränumero**
- **Sarjanumero**

## <a name="example-2-three-level-intercompany-chain"></a>Esimerkki 2: kolmitasoinen konserniyritys

Konsernin sisäinen organisaatio sisältää seuraavat yritykset:

- Yritys A – myyntiyritys, joka myy ulkoisille asiakkaille ja ostaa yritykseltä B.
- Yritys B – tuotanto- tai jakeluyritys, joka ei voi toimittaa tuotteita ja joka ostaa yritykseltä C.
- Yritys C – tuotanto- tai jakeluyritys, joka toimittaa tuotteita yritykselle B.

Yrityksen B ja C välinen sisäinen myyntihinnoittelu on kustannushinta ketjun aloittavalta myyntiyritykseltä. Se on myös kustannushinta yritykselle A, joka myy ulkoisille asiakkaille. Alkuperäisen ulkoista asiakasta koskevan myyntitilauksen hinnoittelu perustuu kuitenkin aina myyntihintoihin.

Konsernin sisäinen myyntitilaus määrittää kaikkien konsernin sisäisten myynti- ja ostotilausten hinnoittelun. Se määräytyy ketjun alussa. Niinpä yritys C, joka myy yritykselle B, määrittää hinnan. Konsernin sisäisen myyntitilauksen hinnoittelu perustuu sisäiseen myynti- tai siirtohinnoitteluun, joka määritetään yrityksessä C.

Tilauksen otsikkotiedot tulevat ulkopuolisen asiakkaan alkuperäisestä ostotilauksesta. Konsernin sisäisissä tilauksissa mahdollisesti tapahtuvia muutoksia ei synkronoida alkuperäiseen myyntitilaukseen.

Seuraavat parametrit on valittava:

Valitse yrityksen A toimittajien **Konsernin sisäinen** -sivulla **Ostotilauskäytännöt**. Valitse seuraavat kentät **Alkuperäinen myyntitilaus (suoratoimitus)** -kenttäryhmässä:

- **Tulosta pakkausluettelo automaattisesti**
- **Kirjaa lasku automaattisesti**
- **Tulosta lasku automaattisesti**

Valitse seuraava kenttä **Konsernin sisäinen myyntitilaus (suoratoimitus)** -kenttäryhmässä:

- **Kirjaa lasku automaattisesti**

Valitse seuraavat kentät **Alkuperäinen myyntitilaus <->Konsernin sisäinen ostotilaus** -kenttäryhmässä:

- **Asiakkaan tiedot**
- **RMA-numero**

Valitse seuraavat kentät **Konsernin sisäinen ostotilaus <->Konsernin sisäinen myyntitilaus** -kenttäryhmässä:

- **Asiakkaan tiedot**
- **RMA-numero**
- **Eränumero**
- **Sarjanumero**

Valitse yrityksen B asiakkaiden **Konsernin sisäinen** -sivulla **Myyntitilauskäytännöt**. Valitse seuraavat kentät **Konsernin sisäisen myyntitilauksen luonti** -kenttäryhmässä:

- **Myyntitilausten numerointi** : **Yritys + alkuperäinen numero**
- **Salli alkuperäiselle asiakkaalle tiedostojen päivitysyhteenveto**

Valitse seuraavat kentät **Konsernin sisäinen myyntitilaus \> Konsernin sisäinen ostotilaus** -kenttäryhmässä:

- **Eränumero**
- **Sarjanumero**

Valitse seuraavat kentät **Konsernin sisäisen myyntilaskun kirjaus** -kenttäryhmässä:

- **Yksikköhinta on yhtä kuin kustannushinta**
- **Aloita alkuperäisen myyntilaskun kirjaus**

Valitse yrityksen B toimittajien **Konsernin sisäinen** -sivulla **Ostotilauskäytännöt**. Valitse seuraavat kentät **Alkuperäinen myyntitilaus (suoratoimitus)** -kenttäryhmässä:

- **Tulosta pakkausluettelo automaattisesti**
- **Kirjaa lasku automaattisesti**
- **Tulosta lasku automaattisesti**

Valitse seuraava kenttä **Konsernin sisäinen myyntitilaus (suoratoimitus)** -kenttäryhmässä:

- **Kirjaa lasku automaattisesti**

Valitse seuraavat kentät **Alkuperäinen myyntitilaus <-> Konsernin sisäinen ostotilaus** -kenttäryhmässä:

- **Asiakkaan tiedot**
- **RMA-numero**
- **Hinta ja alennus**

Valitse seuraavat kentät **Konsernin sisäinen ostotilaus <->Konsernin sisäinen myyntitilaus** -kenttäryhmässä:

- **Asiakkaan tiedot**
- **RMA-numero**
- **Eränumero**
- **Sarjanumero**

Valitse yrityksen C asiakkaiden **Konsernin sisäinen** -sivulla **Myyntitilauskäytännöt**. Valitse seuraavat kentät **Konsernin sisäisen myyntitilauksen luonti** -kenttäryhmässä:

- **Myyntitilauksen numerointi** : **Numerosarjan koodi**
- **Salli alkuperäiselle asiakkaalle tiedostojen päivitysyhteenveto**

Valitse seuraava kenttä **Konsernin sisäisen myyntitilauksen hinnat** -kenttäryhmässä:

- **Hinnan ja alennuksen haku**

Valitse seuraavat kentät **Konsernin sisäisen myyntilaskun kirjaus** -kenttäryhmässä:

- **Yksikköhinta on yhtä kuin kustannushinta**
- **Aloita alkuperäisen myyntilaskun kirjaus**

Valitse seuraavat kentät **Konsernin sisäinen myyntitilaus <->Konsernin sisäinen ostotilaus** -kenttäryhmässä:

- **Eränumero**
- **Sarjanumero**

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
