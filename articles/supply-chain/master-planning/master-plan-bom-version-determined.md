---
title: Määritä tuoterakenneversio
description: Jos nimikkeen suunniteltuna oletustilaustyyppinä on kysynnän hajottamisen aikana Tuotanto, suunnitteluohjelma etsii kelvollisen tuoterakenneversion toimipaikan perusteella.
author: roxanadiaconu
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMConsistOf, BOMDesigner, InventItemOrderSetup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2534
ms.assetid: a5b64301-a011-4469-afaf-e4c9164ef9c6
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: efc980e3a3dfff6d163812396613a1493f4428a4
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/02/2020
ms.locfileid: "3213788"
---
# <a name="determine-the-bom-version"></a>Määritä tuoterakenneversio

[!include [banner](../includes/banner.md)]

Jos nimikkeen suunniteltuna oletustilaustyyppinä on kysynnän hajottamisen aikana Tuotanto, suunnitteluohjelma etsii kelvollisen tuoterakenneversion toimipaikan perusteella. 

Toimipaikan dimensio on aina tiedossa. Se ilmoitetaan kysyntätapahtumassa. Seuraavan prosessin avulla määritetään käytettävä tuoterakenneversio:

-   Jos nimikkeelle on määritetty tuoterakenneversio kysynnän toimipaikassa, käytössä on toimipaikkakohtainen tuoterakenne.
-   Jos nimikkeelle ei ole määritetty toimipaikkakohtaista tuoterakenneversiota kysynnän toimipaikassa, käytössä on yleinen tuoterakenne. Yleinen tuoterakenne ei ilmaise toimipaikkaa, ja sitä voi käyttää useissa toimipaikoissa. Jos yleinen tuoterakenne on käytettävissä, ohjelma käyttää sitä.
-   Jos käytettävissä ei ole yleistä tuoterakenneversiota, kysynnän hajottaminen keskeytyy.

Kaikkien kelvollisten toimipaikkakohtaisten tai yleisten tuoterakenneversioiden on täytettävä tarvittavat päivämäärä- ja määräehdot.





