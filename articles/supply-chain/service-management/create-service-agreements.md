---
title: Huoltosopimusten luominen
description: "Tässä aiheessa kuvataan, miten Huoltohallinta- ja Projektinhallinta ja kirjanpito -moduulien ominaisuuksia käytetään huoltosopimusten luonnissa."
author: YuyuScheller
manager: AnnBe
ms.date: 02/19/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAAgreementTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2a46173a3566a56a21add9d42c111d456b1ae7c1
ms.openlocfilehash: 517bc1b9de9b2512f42e4f32b4a19e517e349e8e
ms.contentlocale: fi-fi
ms.lasthandoff: 02/19/2018

---

# <a name="create-service-agreements"></a>Huoltosopimusten luominen

[!include[banner](../includes/banner.md)]

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

[Huoltosopimukset](service-agreements.md)



