---
title: Lähetystietojen asetukset
description: Tässä aiheessa kuvataan, miten kuljetustietoja määritetään Aiheutunut kustannus -moduulia varten.
author: sherry-zheng
manager: tfehr
ms.date: 12/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ITMGoodsDescriptionTable, ITMVesselTable, ITMExporterTable, ITMCommodityCodeTable, ITMCustomsDescription
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-04
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 90794a154eb2a63f33277383cda80323dafd77b0
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/04/2021
ms.locfileid: "5500931"
---
# <a name="shipping-information-setup"></a>Lähetystietojen asetukset

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Tässä aiheessa kuvataan, miten kuljetustietoja määritetään **Aiheutunut kustannus** -moduulia varten.

## <a name="description-of-goods"></a><a name="description-of-goods"></a>Tavaroiden kuvaus

Tuotteiden kuvaukset auttavat tunnistamaan tuotteiden matkan, kuljetuskontin tai pakkauksen sekä niissä olevat tuotteet. Voit valita tuotekuvauksen kuljetuskontin otsikosta tai pakkauksen otsikosta.

Voit käyttää tuotekuvauksia valitsemalla **Aiheutunut kustannus \> Kuljetustietojen määritys \> Tuotteiden kuvaukset**. Tällöin voit tarkastella, avata, luoda ja poistaa tuotekuvauksia. Seuraavassa taulukossa kuvataan kentät, jotka ovat käytettävissä kullekin tietueelle.

| Kenttä | kuvaus |
|---|---|
| Tavaroiden kuvaus | Syötä niille tuotteille yksilöllinen tunnusnimi/-numero, joihin tätä kuvausta käytetään. |
| kuvaus | Syötä kuvaus tämä luokan tuotetyypille. |

## <a name="vessels"></a><a name="vessels"></a>Alukset

Alus on rahdinkuljettajan tai huolintaliikkeen käyttämä laivan tai aluksen yksilöllinen nimi. Kun luot matkan, sinun on joko valittava tai syötettävä sille alus. Jos käytät usein samoja aluksia, voit nopeuttaa ja helpottaa uuden matkan luomista luomalla kyseisille aluksille alustietueen. Tällöin käyttäjät voivat valita aluksen luettelosta eikä heidän tarvitse syöttää numeroa manuaalisesti joka kerta.

Aluksia voit käsitellä valitsemalla **Aiheutunut kustannus \> Kuljetustietojen määritys \> Alukset**. Tällöin voit tarkastella, avata, luoda ja poistaa alusten tietueita. Seuraavassa taulukossa kuvataan kentät, jotka ovat käytettävissä kullekin tietueelle.

| Kenttä | kuvaus |
|---|---|
| Alus | Syötä sille laivalle yksilöllinen tunnusnimi/-numero, jota käytetään tuotteiden kuljettamiseen matkalla. |
| kuvaus | Syötä aluksen kuvaus. Yleensä tämä kuvaus sisältää laivan sekä rahdinkuljettajan/huolintaliikkeen nimet. |
| Toimitustapa | Valitse aluksen käyttämä toimitustapa (kuten _Ilma_, _Meri_ tai _Juna_). |

## <a name="exporters"></a>Viejät

Kussakin viejätietuessa määritetään toimittaja tai viejä, joka voidaan määrittää matkan toimittajaksi. Viejä voidaan liittää matkaan ja viejää voidaan käyttää raportointiin.

Viejiä voit käsitellä valitsemalla **Aiheutunut kustannus \> Kuljetustietojen määritys \> Viejät**. Tällöin voit tarkastella, avata, luoda ja poistaa viejien tietueita. Seuraavassa taulukossa kuvataan kentät, jotka ovat käytettävissä kullekin tietueelle.

| Kenttä | kuvaus |
|---|---|
| Viejä | Syötä sille tuotteiden viejälle yksilöllinen tunnusnimi/-numero, jonka tuotteita kuljetetaan matkalla. |
| kuvaus | Syötä viejän kuvaus. Yleensä tämä kuvaus sisältää rahdinkuljettajan/huolintaliikkeen täyden nimen. |

## <a name="commodity-codes"></a>Kauppatavarakoodit

Kauppatavarakoodeja käytetään yksilöintiin tullia varten sekä matkan tuotteiden tullimaksujen laskemiseen. Voit valita kauppatavarakoodeja **Vapautetut tuotteet** -sivulla.

Kauppatavarakoodeja voit käsitellä valitsemalla **Aiheutunut kustannus \> Kuljetustietojen määritys \> Kauppatavarakoodit**. Tällöin voit tarkastella, avata, luoda ja poistaa kauppatavarakoodien tietueita. Seuraavassa taulukossa kuvataan kentät, jotka ovat käytettävissä kullekin tietueelle.

| Kenttä | kuvaus |
|---|---|
| Kauppatavarakoodi | Syötä tämäntyyppiselle kauppatavaralle yksilöllinen koodi. |
| kuvaus | Syötä kauppatavaratyypille kuvaus. |

## <a name="customs-description"></a>Tullin kuvaus

Tullin kuvaukset auttavat tunnistamaan tuotteet tullaustarkoituksia varten. Voit valita tullin kuvauksen **Vapautetut tuotteet** -sivulta tai ostotilauksen riveiltä.

Voit käyttää tullin kuvauksia valitsemalla **Aiheutunut kustannus \> Kuljetustietojen määritys \> Tullin kuvaukset**. Tällöin voit tarkastella, avata, luoda ja poistaa tullin kuvauksia. Seuraavassa taulukossa kuvataan kentät, jotka ovat käytettävissä kullekin tietueelle.

| Kenttä | kuvaus |
|---|---|
| Tullin kuvaus | Syötä tämäntyyppiselle tulliluokitukselle yksilöllinen koodi. Tätä koodia käytetään usein tulliviranomaisen tuotteiden kuvausta ja laadullista arvoa varten antamana virallisena kuvauksena. |
| kuvaus | Syötä tulliluokittelun kuvaus. |
