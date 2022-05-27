---
title: Tasapainotetut kirjauskansiot yksiköiden väliselle kirjanpidolle
description: Tässä artikkelissa esitellään, kuinka kirjauskansio täsmäytetään automaattisesti, kun täsmäyttävä taloushallinnon dimensio on valittu Kirjanpito-sivulla.
author: kweekley
ms.date: 10/30/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerParameters
audience: Application User
ms.reviewer: kfend
ms.custom: 15791
ms.assetid: 301bd80e-f8b1-4f12-8194-e6d7de736084
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 38a7d88602dcd0121eb331dab8bf35a815287f8c
ms.sourcegitcommit: 04e6c1c9400e1b582180cf3e0e4767434e736c26
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/05/2022
ms.locfileid: "8712311"
---
# <a name="balanced-journals-for-interunit-accounting"></a>Tasapainotetut kirjauskansiot yksiköiden väliselle kirjanpidolle

[!include [banner](../includes/banner.md)]

Tässä artikkelissa esitellään, kuinka kirjauskansio täsmäytetään automaattisesti, kun täsmäyttävä taloushallinnon dimensio on valittu Kirjanpito-sivulla. 

Jos kirjanpitomerkinnät eivät täsmää taloushallinnon dimension arvojen tasolla, kirjauskansion tasapainottamiseksi luodaan automaattisesti lisäkirjanpitomerkintöjä. Nämä kirjanpitomerkinnät käyttävät **Automaattisten tapahtumien tilit** -sivulla olevia **Yksiköiden välinen – debet**- ja **Yksiköiden välinen – kredit** -kirjaustyyppejä päätilin määrittämiseen. Esimerkki: Liiketoimintayksikkö, joka on kirjanpitotilin toinen segmentti, valitaan täsmäyttäväksi taloushallinnon dimensioksi, ja seuraavat kirjanpitomerkinnät on tarkoitus luoda.

| &nbsp;               | &nbsp;    |
|----------------------|-----------|
| 6100 – MSP – OU\_256 | 100,00 DR |
| 6100 – NY – OU\_249  | 100,00 DR |
| 2100 – MSP – OU\_256 | 200,00 CR |

Tässä tapauksessa määritetään seuraavat saldot:

-   Liiketoimintayksikön MSP = 100,00 CR
-   Liiketoimintayksikön NY = 100,00 DR

Tällöin seuraavat kirjanpitomerkinnät luodaan automaattisesti, jotta kirjauskansio täsmää taloushallinnon dimensioiden arvojen tasolla.

| &nbsp;                            | &nbsp;    |
|-----------------------------------|-----------|
| (Yksiköiden välinen – debet) – MSP – OU\_256 | 100,00 DR |
| (Yksiköiden välinen – kredit) – NY – OU\_249 | 100,00 CR |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
