---
title: Monietappisen matkan määritys
description: Tässä aiheessa kuvataan, miten monietappisia matkoja määritetään Aiheutunut kustannus -moduulia varten.
author: sherry-zheng
ms.date: 12/04/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ITMLegTable, ITMJourneyTable, ITMActivityTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-04
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 57d49af9ca9f2f7e0e4b038c62578ae1993779d6
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/29/2021
ms.locfileid: "7577573"
---
# <a name="multi-leg-journey-setup"></a>Monietappisen matkan määritys

[!include [banner](../../includes/banner.md)]

Tässä aiheessa kuvataan, miten monietappisia matkoja määritetään **Aiheutunut kustannus** -moduulia varten.

## <a name="legs"></a>Etapit

Etappeja käytetään matkan eri osien yksilöintiin. Kukin etappi muodostetaan valitsemalla lähtö- ja kohdesatama sekä käytettävä kuljetusmenetelmä. Kullekin etapille voi määrittää läpimenoajan. Läpimenoajat voivat auttaa lähetyksen jäljittämisessä, ja niitä voi käyttää myös matkalla olevien tuotteiden arvioidun toimituspäivän laskemiseen. Lisäksi, kun matkan etappi on päättynyt, matkan, kuljetuskontin ja niihin liittyvien ostotilausrivien tilat voidaan päivittää jäljityksenhallinnan määritysten avulla. Etappeja voidaan käyttää yksittäisessä matkamallissa tai niitä voidaan käyttää uudelleen useissa matkamalleissa. Konttien lastaus, tulli ja paikalliskuljetus määritetään yleensä etapeiksi ja niissä käytetään määrittelemätöntä satamaa.

Voit käyttää etappeja valitsemalla **Aiheutunut kustannus \> Monietappisen matkan määritys \> Etapit**. Tällöin voit tarkastella, avata, luoda ja poistaa etappien tietueita. Seuraavassa taulukossa kuvataan kentät, jotka ovat käytettävissä kullekin tietueelle.

| Kenttä | kuvaus |
|---|---|
| Etappi | Syötä matkan etapille yksilöllinen nimi/numero. |
| kuvaus | Syötä matkan etapille kuvaus. Yleensä tämä kuvaus sisältää lähtö- ja kohdesatamat tai matkan vaiheen. |
| Lähtösatama | Syötä etapin tuotteiden lähtöpaikka. |
| Satamaan | Syötä etapin tuotteiden määränpää. |
| Toimitustapa | Syötä etapille kuljetusmenetelmä. |

## <a name="journey-templates"></a>Matkamallit

Matkamallissa määritetään kahden sellaisen sataman välinen monietappinen matka, joiden kautta tuotteet kulkevat matkan aikana. Matkan etapit yhdistetään sen ajan määrittämiseksi, joka tarvitaan tuotteiden kulkemiseen toimittajan lähtöpaikasta lopulliseen kohdevarastoon. Kun etapit järjestetään matkamallissa tiettyyn järjestykseen, kukin etapin päivämäärä, matkan tila, kuljetuskontti ja ostotilausrivit määritetään läpimenoaikojen mukaan. [Jäljityksen hallintakeskusta](delivery-information-setup.md) käytetään kunkin matkamalliin kuuluvan etapin läpimenoaikojen määrittämiseen. Matkamallia käytetään myös, kun määritetään matkan automaattisia kustannuksia. Kun matka on määritetty, tuotteiden kuljetukseen liittyvä kustannus voidaan määrittää automaattisten kustannusten sivulla.

Voit käyttää matkamalleja valitsemalla **Aiheutunut kustannus \> Monietappisen matkan määritys \> Matkamallit**. Tällöin voit tarkastella, avata, luoda ja poistaa matkamalleja.

Määritä kullekin matkamallille otsikossa seuraavat kentät.

| Kenttä | kuvaus |
|---|---|
| Matkamalli | Syötä matkamallille yksilöllinen nimi/numero. Matkamalli määrittää yleensä matkan lähtöpaikan ja määränpään. |
| kuvaus | Syötä matkanmallille kuvaus. Kuvaus sisältää yleensä lähtö- ja kohdesatamat sekä matkalajin. |

Lisää **Rivit**-osassa rivi matkan jokaiselle riville ja järjestä rivit. Työkalurivin **Ylös**- ja **Alas**-nuolilla voit muuttaa rivien järjestystä. Seuraavassa taulukossa kuvataan kentät, jotka ovat käytettävissä kunkin rivin osalta.

| Kenttä | kuvaus |
|---|---|
| Etappi | Valitse matkaan lisättävä etappi. |
| kuvaus | Etapin kuvaus. |
| Lähtösatama | Etapin tuotteiden lähtöpaikkana oleva satama. Tämä satama on kohdesatama, jota käytetään matkan automaattisten kustannusten määrittämiseen. |
| Satamaan | Etapin tuotteiden määränpäänä oleva satama. |
| Toimitustapa | Etapilla käytettävä toimitustapa. |
| Matkan lähtösatama | Jos etapille määritettyä satamaa käytetään automaattisten kustannusten määrittämiseen, valitse tämä satama matkan lähtösatamaksi valitsemalla tämä valintaruutu. Tämä satama tulee näkyviin matkan otsikossa. |
| Matkan kohdesatama | Jos etapille määritettyä satamaa käytetään automaattisten kustannusten määrittämiseen, valitse tämä satama matkan kohdesatamaksi valitsemalla tämä valintaruutu. Tämä satama tulee näkyviin matkan otsikossa. |
| Kuljetusyritys | Valitse etapilla käytettävä rahdinkuljettaja. |

## <a name="activities"></a>Tehtävät

**Tehtävät**-sivun asetuksilla määritetään ne tehtävät, jotka voidaan suorittaa etapin kohdesatamassa. **Kaikki kuljetuskontit** -sivua käyttävät käyttäjät voivat valita näistä arvoista, kun he arvioivat kunkin tehtävän keston ja kirjaavat todellisen keston vertailutarkoituksia varten.

Määritä tehtävät valitsemalla **Aiheutunut kustannus \> Monietappisten matkojen määritys \> Tehtävät**. Tällöin voit lisätä, poistaa ja muokata tehtäviä käyttämällä toimintoruudun painikkeita.

Seuraavassa taulukossa kuvataan kentät, jotka ovat käytettävissä ruudukon kunkin tehtävän osalta.

| Kenttä | kuvaus |
|---|---|
| Tehtävä | Tehtävän nimi. |
| kuvaus | Tehtävän kuvaus. |
| Kuljetusyritys | Tehtävään liittyvän rahdinkuljettajan toimittajatili. |
