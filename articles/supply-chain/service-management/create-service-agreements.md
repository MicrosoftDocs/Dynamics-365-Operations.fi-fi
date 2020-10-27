---
title: Huoltosopimusten luominen
description: Tässä aiheessa kuvataan, miten Huoltohallinta- ja Projektinhallinta ja kirjanpito -moduulien ominaisuuksia käytetään huoltosopimusten luonnissa.
author: ShylaThompson
manager: tfehr
ms.date: 02/19/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAAgreementTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7a1a47761869a4190eac6dc9e069a6b520bf7a1d
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/10/2020
ms.locfileid: "3985139"
---
# <a name="create-service-agreements"></a>Huoltosopimusten luominen

[!include [banner](../includes/banner.md)]

Tässä aiheessa kuvataan, miten Huoltohallinta- ja Projektinhallinta ja kirjanpito -moduulien ominaisuuksia käytetään huoltosopimusten luonnissa.

## <a name="create-a-service-agreement-from-service-management"></a>Huoltosopimuksen luominen Huoltohallinnassa

1. Siirry **huoltohallintaan**.
2. Luo uusi huoltosopimus sivun otsikossa valitsemalla **Huoltosopimukset**. 
3. Valitse **Uusi**. Anna kuvaus, valitse viittaus projektiin **Projektitunnus**-kentässä ja täytä huoltosopimuksen muut kentät ja rivit. Valitse **Tallenna**.
4. Luo huoltokohteen suhteet tai huoltotehtäväsuhteet huoltosopimusta varten valitsemalla **Suhteet**-välilehdessä **Huoltokohteet** tai **Huoltotehtävät**. Huoltokohteet ja -tehtävät, joita varten olet luonut suhteet, voidaan liittää huoltosopimuksen riveihin.
5. Luo sivun alaosaan huoltosopimusrivejä kopioimalla rivejä huoltomallista tai toisesta huoltosopimuksesta. Vaihtoehtoisesti voit luoda huoltosopimusrivit manuaalisesti.

> [!NOTE]
> Jos kopioit rivejä huoltosopimukseen toisesta huoltosopimuksesta, voit määrittää, haluatko kopioida myös huoltokohteen ja huoltotehtävän suhteet. Jos kopioit nämä suhteet, ne lisätään huoltosopimuksen aiemmin luotuihin suhteisiin. Jos kopioit huoltosopimusrivejä huoltomallista, huoltokohteen ja huoltotehtävän suhteet kopioidaan automaattisesti huoltokohteen ja huoltotehtävän suhteina uusiin huoltosopimusriveihin.

## <a name="create-service-agreement-lines-manually"></a>Huoltosopimusrivien luominen manuaalisesti

1. Lisää huoltosopimusrivit riviruudukossa **Huoltosopimukset**-sivulla. 
2. Anna asiaankuuluvat tiedot huoltosopimusriville. 
3. Tallenna rivi painamalla näppäinyhdistelmää **CTRL+S** ja sulje sitten sivu.

## <a name="create-a-service-agreement-from-project"></a>Huoltosopimuksen luominen projektista

1. Valitse **Projektinhallinta ja kirjanpito**.
2. Valitse **Kaikki projektit**.
3. Valitse projekti luettelosta.
4. Valitse **toimintoruudussa** **Hallitse**. Valitse **Uusi**-toimintoryhmässä ensin **Huolto** ja sitten **Huoltosopimus**.
5. Anna projektiviite noudattamalla osan **Huoltosopimuksen luominen** vaiheita, kuten on kuvattu aiemmin tässä ohjeaiheessa.


## <a name="related-topics"></a>Liittyvät aiheet

[Huoltosopimusten laatiminen ja luominen – yleiskatsaus](service-agreements.md)


