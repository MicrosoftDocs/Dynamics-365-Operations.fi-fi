---
title: Ylläpitopyynnön tyypit
description: Tässä ohjeaiheessa kerrotaan, kuinka ylläpitopitopyynnön tyypit määritetään resurssien hallinnassa.
author: josaw1
manager: AnnBe
ms.date: 07/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-07-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 19d529df6c8aab036de59502b4f14101e1a07707
ms.sourcegitcommit: 2c73749779274e0b0abbcb4041bbc1df0fb6d6e4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/26/2019
ms.locfileid: "1790489"
---
# <a name="maintenance-request-types"></a>Ylläpitopyynnön tyypit

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Ylläpitopyynnön tyyppejä käytetään ylläpitopyyntöjen luokittelemiseen. Sinulla voi esimerkiksi olla ylläpitopyyntötyyppejä, jotka liittyvät ennakoivaan ja korjaavaan ylläpitoon. Tai sinulla voi olla erityinen ylläpitopyynnön tyyppi, jota käytetään resurssin korjauksen hallintaan (varastokorjaus).

Ylläpitopyynnön tyyppi määrittää liitoksen ylläpitopyynnön elinkaaren tilaryhmään (ylläpidon elinkaarimalli). Ylläpitopyynnön elinkaarimallit määrittävät elinkaaritilat, jotka voidaan määrittää ylläpitopyynnölle. (Esimerkkejä ylläpitopyynnön elinkaaren tiloista ovat**Luotu**,**Aktiivinen** ja **Päättynyt**.)

1. Valitse **Resurssien hallinta** \> **Asetukset** \> **Ylläpitopyynnöt** \> **Ylläpitopyynnön tyypit**.
2. Luo ylläpitopyyntötyyppi valitsemalla **Uusi**.
3. Kirjoita **Ylläpitopyynnön tyyppi** -kenttään ylläpitopyynnön tyypin tunnus.
4. Anna nimi **Nimi**-kenttään.
5. Valitse **Yleiset**-pikavälilehdessä **Ylläpitopyynnön elinkaarimalli** -kentässä ylläpitopyynnön elinkaarimalli.
6. Valitse **Työtilaustyyppi**-kentässä työtilauksen tyyppi. Kun ylläpitopyyntö muunnetaan työtilaukseksi, työtilaus hakee automaattisesti työtilauksen tyypin, joka liittyy ylläpitopitopyynnön tyyppiin.

Seuraavassa kuvassa on esimerkki **Ylläpitopyynnön tyypit** -luettelosivusta.

![Kuva 1](media/07-setup-for-requests.png)
