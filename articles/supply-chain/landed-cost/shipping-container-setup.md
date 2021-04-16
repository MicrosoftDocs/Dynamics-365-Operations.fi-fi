---
title: Lähetyskontit
description: Tässä aiheessa kuvataan, miten kuljetuskontteja määritetään Aiheutunut kustannus -moduulia varten.
author: sherry-zheng
ms.date: 12/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ITMContainerTypeTable, ITMContainerTable, ITMContainerUnitTypeTable, ITMRefrigerationTypeTable, ITMContainersListPage, ITMContainers
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-09
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 2f7e9435aa3d0d06e1cc51457a6343b807d76dc7
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5833710"
---
# <a name="shipping-container-setup"></a>Kuljetuskonttien määritys

[!include [banner](../../includes/banner.md)]

Tässä aiheessa kuvataan, miten kuljetuskontteja määritetään **Aiheutunut kustannus** -moduulia varten.

## <a name="set-up-shipping-container-types"></a><a id="shipping-container-types"></a>Kuljetuskonttityyppien määritys

Kuljetuskonttityypit määrittävät ne kuljetuskonttien tyypit, jotka ovat käytettävissä lähetyksissä ja matkoissa.

Kuljetuskonttityyppejä voit käsitellä valitsemalla **Aiheutunut kustannus \> Konttien määritys \> Kuljetuskonttityypit**. Näin voit tarkastella, lisätä ja poistaa konttityyppien tietueita. Seuraavassa taulukossa kuvataan kentät, jotka ovat käytettävissä kullekin tietueelle.

| Kenttä | kuvaus |
|---|---|
| Lähetyskontin tyyppi | Syötä kuljetuskonttityypille yksilöllinen nimi/numero. |
| kuvaus | Syötä kuljetuskonttityypille kuvaus. |
| Tilavuus | Syötä enimmäistilavuus, joka on sallittu tämäntyyppisille kuljetuskonteille. |
| Paino | Syötä enimmäispaino, joka on sallittu tämäntyyppisille kuljetuskonteille. |
| Palautettavissa | Määritä voidaanko tämäntyyppiset kuljetuskontit palauttaa toimittajalle, kun niitä on käytetty matkassa. Jos tämän asetuksen arvoksi määritetään *Kyllä*, tämäntyyppisten kuljetuskonttien lähtösatamaan palauttamiseen saatetaan soveltaa lisäkustannuksia. |

## <a name="set-up-shipping-containers"></a>Kuljetuskonttien määrittäminen

Kuljetuskonttien tietueilla yksilöidään kukin matkojen aikana käytettävä kontti. Kun luot matkan, voit valita sille tietyn kontin kaikkien täällä määrittämiesi kuljetuskonttitietueiden luettelosta. Tämä toiminto on erityisen hyödyllinen, jos yritys omistaa omat kuljetuskonttinsa.

Vain kerran käytettäville kuljetuskonteille ei tarvitse syöttää kuljetuskonttinumeroita. Sen sijaan voit lisätä kuljetuskontin numeron, kun luot matkan.

Kuljetuskonttitietueita käytetään vain Aiheutunut kustannus -kohdassa. Ne eivät ole käytössä vakiomuotoisessa **Kuljetuksenhallinta**-moduulissa (TMS).

Kuljetuskontteja voit käsitellä valitsemalla **Aiheutunut kustannus \> Konttien määritys \> Kuljetuskontit**. Näin voit tarkastella, lisätä ja poistaa konttien tietueita. Seuraavassa taulukossa kuvataan kentät, jotka ovat käytettävissä kullekin tietueelle.

| Kenttä | kuvaus |
|---|---|
| Lähetyskontti | Syötä kuljetuskontille yksilöllinen nimi/numero. |
| Lähetyskontin tyyppi | Valitse kuljetuskontin tyyppi. Lisätietoja on tämän aiheen aiemmassa kohdassa [Kuljetuskonttityyppien määrittäminen](#shipping-container-types). |

> [!NOTE]
> - Kuljetuskontin määrittäminen on valinnaista. Määritystä käytetään yleensä vain, jos yritys omistaa omat kuljetuskonttinsa tai käyttää usein uudelleen samoja kuljetuskontteja.
> - Kuljetuskonttinumeroille ei lasketa tarkistusnumeroita.

## <a name="set-up-unit-types"></a><a name="unit-types"></a>Yksikkötyyppien määrittäminen

Yksikkötyypit tarjoavat lisää ryhmittelyjä ja yksilöintimenetelmiä kuljetuskonteille. Yksikkötyyppiä käytetään yleensä sen kuljetuskonttityypin yksilöimiseen, johon tuotteet on pakattu. Tällaisia ovat esimerkiksi kuormalavat tai tynnyrit. Voit valita yksikkötyypin, kun määrität kontin **Kaikki kuljetuskontit** -sivulla.

Yksikkötyyppejä käytetään vain Aiheutunut kustannus -kohdassa. Ne eivät ole käytettävissä TMS:ssä.

Yksikkötyyppejä voit käsitellä valitsemalla **Aiheutunut kustannus \> Konttien määritys \> Yksikkötyypit**. Näin voit tarkastella, lisätä ja poistaa yksikkötyyppien tietueita. Seuraavassa taulukossa kuvataan kentät, jotka ovat käytettävissä kullekin tietueelle.

| Kenttä | kuvaus |
|---|---|
| Yksikkötyyppi | Syötä yksikkötyypille yksilöllinen nimi/numero. |
| kuvaus | Anna yksikkötyypin kuvaus. |

## <a name="set-up-refrigeration-types"></a><a name="refrigeration-types"></a>Jäähdytystyyppien määritys

Jäähdytystyyppejä käytetään lisäryhmittelyjen ja -yksilöintimenetelmien luomiseen kuljetuskonteille (yleensä jäähdytetyille kuljetuskonteille). Voit valita jäähdytystyypin, kun määrität kontin **Kaikki kuljetuskontit** -sivulla.

Jäähdytystyyppejä voit käsitellä valitsemalla **Aiheutunut kustannus \> Konttien määritys \> Jäähdytystyypit**. Näin voit tarkastella, lisätä ja poistaa jäähdytystyyppien tietueita. Seuraavassa taulukossa kuvataan kentät, jotka ovat käytettävissä kullekin tietueelle.

| Kenttä | kuvaus |
|---|---|
| Kylmäsäilytystyyppi | Syötä jäähdytystyypille yksilöllinen nimi/numero. |
| kuvaus | Kirjoita jäähdytystyypin lyhyt kuvaus. |
