---
title: "Tilaustenkäsittelyn määräajat"
description: "Tässä artikkelissa on tietoja tilaustenkäsittelyn määräajoista. Tilaustenkäsittelyn määräaika on aika, joka määrittää, käsitelläänkö asiakastilausta siten kuin se olisi vastaanotettu samana päivänä tai seuraavana päivänä."
author: omulvad
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventOrderEntryDeadlineGroup, InventOrderEntryDeadlineParameters, InventOrderEntryDeadlineTable
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 7151
ms.assetid: bbc4f9a2-df4b-4d92-9f18-25282a85541f
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 4f3905f364ea67eab226323fd3450ebed30e4735
ms.contentlocale: fi-fi
ms.lasthandoff: 05/08/2018

---

# <a name="order-entry-deadlines"></a>Tilaustenkäsittelyn määräajat

[!include [banner](../includes/banner.md)]

Tässä artikkelissa on tietoja tilaustenkäsittelyn määräajoista. Tilaustenkäsittelyn määräaika on aika, joka määrittää, käsitelläänkö asiakastilausta siten kuin se olisi vastaanotettu samana päivänä tai seuraavana päivänä.

Useissa yrityksissä myyntitilaus on vastaanotettava ennen tiettyä kellonaikaa, jotta se voidaan käsitellä kyseisenä päivänä saapuneena. Kaikki tilaukset, jotka vastaanotetaan tämän kellonajan jälkeen, käsitellään kuin ne olisivat saapuneet seuraavana arkipäivänä. Tätä tilausten katkaisupäivämäärää kutsutaan tilaustenkäsittelyn määräajaksi.  

Tilaustenkäsittelyn määräaikoja käytetään syötteenä tilauksia koskevissa lupauksissa. Siten ne auttavat tilausten toimituksia koskevien asiakkaiden odotusten hallinnassa. Asiakkaat esimerkiksi näkevät, että jos he tekevät tilauksen ennen tiettyä kellonaikaa, sitoudut toimittamaan tuotteet samana päivänä. Jos tilaus tehdään tämän jälkeen, toimitusta voi odottaa vasta seuraavana arkipäivänä. Voit määrittää tilaustenkäsittelyn määräajat varasto-ominaisuuksien ja lähetyksen rahdinkuljettajan aikataulujen mukaisesti.  

Kaikkien viikonpäivien tilaustenkäsittelyn määräajat määritetään **Tilaustenkäsittelyn määräajat** -sivulla. Kaikki tilaukset, jotka vastaanotetaan tämän kellonajan jälkeen, käsitellään kuin ne olisivat saapuneet seuraavana arkipäivänä. Määräaikojen oletusarvo on 23:59 eli minuuttia ennen keskiyötä kunakin päivänä. Määräaikoja voi muuttaa niin, että ne vastaavat todellisia toimituksen tai vastaanoton määräaikoja.  

Voit määrittää tilaustenkäsittelyn määräajat tietylle asiakasryhmälle. Voit esimerkiksi määrittää tietylle asiakasryhmälle myöhäisemmän tilaustenkäsittelyn määräajan kuin muille asiakkaille. Tässä tapauksessa määritä ensin **Tilaustenkäsittelyn määräaikaryhmät**-sivulla ryhmät, joita tilaustenkäsittelyn määräajat koskevat. Määritä sitten ryhmät asiakkaille **Asiakkaat**-sivulla.  

Jos yrityksesi koostuu useasta toimipaikasta, voit määrittää tilaustenkäsittelyn määräajat toimipaikkakohtaisesti. Jos toimipisteet sijaitsevat eri aikavyöhykkeillä, tilaustenkäsittelyn määräajat määritetään toimipisteen aikavyöhykkeen mukaan. Myyntitilauksia ja myyntitarjouksia käsiteltäessä tilaustenkäsittelyn määräaika kuitenkin muunnetaan käyttäjän aikavyöhykkeen mukaiseksi **Käytettävissä olevat lähetys- ja vastaanottopäivämäärät** -sivulla.  

**Ota käyttöön tilaustenkäsittelyn määräaikayhdistelmät** -sivulla voit määrittää sallittuja toimipisteiden ja tilauskäsittelyn määräaikaryhmien yhdistelmiä.

## <a name="example-order-entry-deadline"></a>Esimerkki: Tilaustenkäsittelyn määräaikaryhmä
Tilaustenkäsittelyn määräaika on tiistaisin klo 16:00. Yrität määrittää tiettynä tiistaina klo 17:00 kuluvan päivän toimituspäiväksi. (Huomaa, että tässä esimerkissä ei ole läpimenoaikaa.) Jos **Toimituspäivän tarkistus** -valintaruutu valitaan, näyttöön tulee varoitus, jossa ilmoitetaan, että päivämäärä ei ole kelvollinen. Varoitus näkyy **Käytettävissä olevat lähetys- ja vastaanottopäivämäärät** -sivulla, jolla voit valita vaihtoehtoiset päivämäärät.

## <a name="example-different-order-entry-deadlines-per-site"></a>Esimerkki: Erilaiset tilaustenkäsittelyn määräajat eri toimipisteissä
Yritys koostuu kahdesta toimipisteestä. Toimipisteet sijaitsevat eri aikavyöhykkeillä seuraavassa taulukossa esitetyllä tavalla.

| Toimipiste A                      | Toimipiste B                      |
|-----------------------------|-----------------------------|
| Kalifornia                  | Florida                     |
| PST (Tyynenmeren normaaliaika) | EST (Itäinen normaaliaika) |

Toimipisteet A ja B ovat määrittäneet seuraavat tilaustenkäsittelyn määräajat:

| Viikonpäivä             | A: Tilaustenkäsittelyn määräajat (PST) | B: Tilauskäsittelyn määräajat (EST) |
|-----------------------------|--------------------------------|--------------------------------|
| Maanantai                      | 13:00                          | 14:00                          |
| Tiistai                     | 13:00                          | 14:00                          |
| Keskiviikko                   | 13:00                          | 14:00                          |
| Torstai                    | 13:00                          | 14:00                          |
| Perjantai                      | 13:00                          | 14:00                          |

Olet tilausten käsittelijä Utahissa, jonka aikavyöhyke on MST (Kalliovuorten normaaliaika). Tämä tarkoittaa, että jos teet toimipisteen A tilaukset ennen kellonaikaa 14:00 MST ja toimipisteen B tilaukset ennen kellonaikaa 12:00 MST, saat tehtyä molempien toimipisteiden tilaukset tilaustenkäsittelyn määräaikaan mennessä.  

Seuraavassa taulukossa on toimipisteiden A ja B tilaustenkäsittelyn määräajat muunnettuina MST-aikavyöhykkeen ajaksi.

| Toimipiste A: PST         | Toimipiste A: MST        | Toimipiste B: EST           | Toimipiste B: MST        |
|---------------------|--------------------|-----------------------|--------------------|
| 13:00               | 14:00              | 14:00                 | 12:00              |

**Huomautus:** Jos kesäaika on käytössä, tilaustenkäsittelyn määräajat muutetaan sen mukaan.

## <a name="example-same-order-entry-deadline-per-site"></a>Esimerkki: Sama tilaustenkäsittelyn määräaika eri toimipisteissä
Yritys koostuu kahdesta toimipisteestä. Toimipisteet sijaitsevat eri aikavyöhykkeillä seuraavassa taulukossa esitetyllä tavalla.

| Toimipiste A                      | Toimipiste B                      |
|-----------------------------|-----------------------------|
| Kalifornia                  | Florida                     |
| PST (Tyynenmeren normaaliaika) | EST (Itäinen normaaliaika) |

Toimipisteet A ja B ovat määrittäneet seuraavat tilaustenkäsittelyn määräajat:

| Viikonpäivä | PST ja EST |
|-----------------|-------------|
| Maanantai          | 13:00       |
| Tiistai         | 13:00       |
| Keskiviikko       | 13:00       |
| Torstai        | 13:00       |
| Perjantai          | 13:00       |

Olet tilausten käsittelijä Utahissa, jonka aikavyöhyke on MST. Tämä tarkoittaa, että jos teet toimipisteen A tilaukset ennen kellonaikaa 14:00 MST ja toimipisteen B tilaukset ennen kellonaikaa 11:00 MST, saat tehtyä molempien toimipisteiden tilaukset tilaustenkäsittelyn määräaikaan mennessä. 

Seuraavassa taulukossa on toimipisteiden A ja B tilaustenkäsittelyn määräajat muunnettuina MST-aikavyöhykkeen ajaksi.

| Toimipiste A: PST         | Toimipiste A: MST        | Toimipiste B: EST           | Toimipiste B: MST        |
|---------------------|--------------------|-----------------------|--------------------|
| 13:00               | 14:00              | 13:00                 | 11:00              |

**Huomautus:** Jos kesäaika on käytössä, tilaustenkäsittelyn määräajat muutetaan sen mukaan.

<a name="additional-resources"></a>Lisäresurssit
--------

[Toimitusaikataulut](delivery-schedules.md)




