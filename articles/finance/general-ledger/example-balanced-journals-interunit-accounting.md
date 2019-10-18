---
title: Tasapainotetut kirjauskansiot yksiköiden väliselle kirjanpidolle
description: Tässä artikkelissa esitellään, kuinka kirjauskansio täsmäytetään automaattisesti, kun täsmäyttävä taloushallinnon dimensio on valittu Kirjanpito-sivulla.
author: ShylaThompson
manager: AnnBe
ms.date: 10/30/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 15791
ms.assetid: 301bd80e-f8b1-4f12-8194-e6d7de736084
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e84d96b5467b38e07a9ed31f142c27b638289284
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/27/2019
ms.locfileid: "2177496"
---
# <a name="balanced-journals-for-interunit-accounting"></a>Tasapainotetut kirjauskansiot yksiköiden väliselle kirjanpidolle

[!include [banner](../includes/banner.md)]

Tässä artikkelissa esitellään, kuinka kirjauskansio täsmäytetään automaattisesti, kun täsmäyttävä taloushallinnon dimensio on valittu Kirjanpito-sivulla. 

Jos kirjanpitomerkinnät eivät täsmää taloushallinnon dimension arvojen tasolla, kirjauskansion tasapainottamiseksi luodaan automaattisesti lisäkirjanpitomerkintöjä. Nämä kirjanpitomerkinnät käyttävät **Automaattisten tapahtumien tilit** -sivulla olevia **Yksiköiden välinen – debet**- ja **Yksiköiden välinen – kredit** -kirjaustyyppejä päätilin määrittämiseen. Esimerkki: Liiketoimintayksikkö, joka on kirjanpitotilin toinen segmentti, valitaan täsmäyttäväksi taloushallinnon dimensioksi, ja seuraavat kirjanpitomerkinnät on tarkoitus luoda.

|                      |           |
|----------------------|-----------|
| 6100 – MSP – OU\_256 | 100,00 DR |
| 6100 – NY – OU\_249  | 100,00 DR |
| 2100 – MSP – OU\_256 | 200,00 CR |

Tässä tapauksessa määritetään seuraavat saldot:

-   Liiketoimintayksikön MSP = 100,00 CR
-   Liiketoimintayksikön NY = 100,00 DR

Tällöin seuraavat kirjanpitomerkinnät luodaan automaattisesti, jotta kirjauskansio täsmää taloushallinnon dimensioiden arvojen tasolla.

|                                   |           |
|-----------------------------------|-----------|
| (Yksiköiden välinen – debet) – MSP – OU\_256 | 100,00 DR |
| (Yksiköiden välinen – kredit) – NY – OU\_249 | 100,00 CR |





