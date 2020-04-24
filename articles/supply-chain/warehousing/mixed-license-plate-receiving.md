---
title: Yhdistetyn rekisterikilven vastaanotto
description: Tässä ohjeaiheessa kerrotaan, miten yhdistetyn rekisterikilven vastaanotolla rekisteröidään ja luodaan työ useille nimikkeille mobiililaitteessa.
author: Mirzaab
manager: tfehr
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFAutoConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 15c058887da33b522c5d9a1a8d2c45a5d1566a5d
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/02/2020
ms.locfileid: "3215766"
---
# <a name="mixed-license-plate-receiving"></a>Yhdistetyn rekisterikilven vastaanotto

[!include [banner](../includes/banner.md)]

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
