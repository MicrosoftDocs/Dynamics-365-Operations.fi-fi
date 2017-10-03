---
title: Yhdistetyn rekisterikilven vastaanotto
description: "Tässä ohjeaiheessa kerrotaan, miten yhdistetyn rekisterikilven vastaanotolla rekisteröidään ja luodaan työ useille nimikkeille mobiililaitteessa."
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 0e785d71e7ae3c5f60d36d8b190001b5e356c626
ms.contentlocale: fi-fi
ms.lasthandoff: 07/27/2017

---

# <a name="mixed-license-plate-receiving"></a>Yhdistetyn rekisterikilven vastaanotto

[!include[banner](../includes/banner.md)]

Yhdistetyn rekisterikilven vastaanoton avulla voit muodostaa useista nimikkeistä koostuvia rekisterikilpiä ennen rekisteröintiä painopanotyön luontia. 

Useista nimikkeistä koostuvaa rekisterikilpeä ei tarvitse jakaa vastaanottolaiturilla kunkin nimikkeen rekisteröintiä varten. 

Kun lähdeasiakirjanrivien tunnistamiseen käytetään nimikeperusteista työnkulkua, voit skannata viivakoodit nimikehallinnassa. Jos viivakoodiin on määritetty määrä ja mittayksikkö, nimike ja määrä lisätään automaattisesti yhdistettyyn rekisterikilpeen ja näyttö palautuu uuden nimikkeen skannaustilaan. Voit tällä tavoin tarkastaa kaikki nimikkeet nopeasti ilman, että jokainen vaihe on vahvistettava. 

Voit näyttää yhdistetyn rekisterikilven vastaanottovirrassa luettelon nimikkeistä, jotka on jo skannattu rekisterikilpeen. Voit myös muokata tai korvat nimikkeen määrän siellä.

## <a name="where-it-applies"></a>Käyttö

Yhdistetyn rekisterikilven vastaanotto on mobiililaitteen vastaanottovirta useiden rivien tai nimikkeiden samanaikaista rekisteröintiä ja työn luomista varten. Tämä on kätevää, jos vastaanotat saapuvia rekisterikilpiä, joissa on useita nimikkeitä. 

## <a name="how-to-set-up-mixed-license-plate-receiving"></a>Yhdistetyn rekisterikilven vastaanoton määrittäminen
Yhdistetyn rekisterikilven vastaanotto määritetään mobiililaitteen valikkovaihtoehtona.

Sinun on luotava uusi valikkovaihtoehto, jossa tilaksi on määritetty työ, joka ei käytä aiemmin luotua työtä ja joka käyttää jotakin seuraavista menetelmiä:

- Yhdistetyn rekisterikilven vastaanotto
- Yhdistetyn rekisterikilven vastaanotto ja poispano

Lähdeasiakirjarivien tunnistamisvaihtoehdot ovat ostotilausnimike, ostotilausrivi, palautustilaus, siirtotilausnimike ja siirtotilausrivi. Nämä vaihtoehdot voivat muuttaa yhden rekisterikilven vastaanottotilauksen. Viimeinen vaihtoehto on kuormanimikkeen mukaan. Voit lisätä rekisterikilpeen useita nimikkeitä mutta vaihtelu useiden kuormien välillä ei ole mahdollista.

