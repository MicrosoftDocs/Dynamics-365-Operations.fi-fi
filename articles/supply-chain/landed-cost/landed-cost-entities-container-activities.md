---
title: Konttitehtävien yksikkö
description: Tässä artikkelissa on tietoja konttitoiminnoista, joiden avulla seurataan lähetyskonttien etenemistä.
author: yufeihuang
ms.date: 05/27/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2022-05-27
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: 6a518003f8624ef05ac86be1b963c3f916420278
ms.sourcegitcommit: 5b34b41ae74269ba639e2876bc5862ef468da1cc
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/15/2022
ms.locfileid: "9167570"
---
# <a name="container-activities-entity"></a>Konttitoimintojen yksikkö

[!include [banner](../includes/banner.md)]

Konttitoimintojen avulla seurataan lähetyskonttien etenemistä. Tietue luodaan jokaiselle etapille, joka on määritetty matkan malliin, joka on valittu lähetyskontin luontihetkellä. Tietueet luodaan myös, kun lähetyskontti luodaan tietoyksikön kautta.

Tiedot kuljetettavan lähetyskontin etenemisestä vastaanotetaan usein ulkoisesta lähteestä. Konttitoimintojen yksikkö sallii ulkoisen lähteen, kuten huolitsijan, päivittää tietueen suoraan. Siksi tietoja ei tarvitse päivittää manuaalisesti.

## <a name="container-activities-itmcontaineractivityentity"></a>Konttitoiminnot (ITMContainerActivityEntity)

Voit käyttää konttitoimintojen yksikköä (`ITMContainerActivityEntity`) luodaksesi lisää toimintotietueita. Vaihtoehtoisesti huolitsija voi välittää päivityksiä vahvistetulle **Todellinen päättymispäivä** -arvolle.

| Nimi | Yhdistämismääritys | Tietotyyppi | Avain | Pakollinen |
|---|---|---|---|---|
| Todellinen päättymispäivä | ITMContainerActivityTable.ActualEndDate | Datetime | En | En |
| Toimitustapa | ITMContainerActivityTable.DlvModeId | Nvarchar(10) | En | En |
| Arvoitu päättymispäivä | ITMContainerActivityTable.EsimatedDate | Datetime | En | En |
| Rivinumero | ITMContainerActivityTable.LineNum | Numeric(32, 16) | **Kyllä** | En |
| Muistiinpanot | ITMContainerActivityTable.Notes | nvarchar(MAX) | En | En |
| Tehtävä | ITMContainerActivityTable.ShipActivityId | Nvarchar(10) | En | **Kyllä** |
| Lähetyskontti | ITMContainerActivityTable.ShipContainerId | Nvarchar(20) | **Kyllä** | **Kyllä** |
| Matka | ITMContainerActivityTable.ShipId | Nvarchar(20) | **Kyllä** | **Kyllä** |
| Etappi | ITMContainerActivityTable.ShipLegId | Nvarchar(20) | En | **Kyllä** |
| Palvelun tarjoaja | ITMContainerActivityTable.ShipServiceProvider | Nvarchar(20) | En | En |
| Lämpötila | ITMContainerActivityTable.ShipTemperature | Numeric(32, 6) | En | En |
| Alus | ITMContainerActivityTable.ShipVesselId | Nvarchar(20) | En | En |
| Aloituspäivämäärä | ITMContainerActivityTable.StartDate | Datetime | En | En |

## <a name="tracking-control"></a>Seurannan ohjaus

Seurannan ohjauskeskus mahdollistaa sen, että määritetyn kohdekentän päivitys voi käynnistää määritetyn lähdekentän päivityksen. Jos sekä lähdekentän että kohdekentän arvo päivitetään konttitoimintojen yksikköä käyttämällä, kohdekentässä näkyy yksikön arvo. Tämä toiminta liittyy seurantaohjaustietueisiin, joissa **Luo tyyppi** -arvo on *Läpimenoaika*.

Kustannusalueille, joilla on **Luo tyyppi** -arvo *Tilan päivitys* tai *Tyhjä* (joka on käyttäjän määrittämä arvo), järjestelmä päivittää matkan tilan tai kohdekentän seurannan ohjauksen konfiguraation mukaisesti.

## <a name="calculated-fields"></a>Lasketut kentät

Seuraavien konttitoimintojen tietuekenttien arvot lasketaan muiden kenttien arvojen perusteella. Vaikka näitä laskettuja kenttiä ei sisällytetä tietoyksikköön, ne määritetään, jos laskelman perustana olevat kentät annetaan.

- **Arvioidut päivät** = **Arvoitu päättymispäivä** – **Aloituspäivä**
- **Todelliset päivät** = **Todellinen päättymispäivä** – **Aloituspäivä**
