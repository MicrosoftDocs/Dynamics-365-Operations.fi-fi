---
title: "Määritä tuoterakenneversio"
description: "Aikana Kysynnän hajottaminen, jos nimikkeellä oletusarvoinen tilaustyyppi tuotannon, suunnitteluohjelma etsii kelvollisen tuoterakenneversion toimipaikan perusteella."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: BOMConsistOf, BOMDesigner, BOMTable, InventItemOrderSetup
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 2534
ms.assetid: a5b64301-a011-4469-afaf-e4c9164ef9c6
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 4e4f5f02dfa986669decbc8854148b5eff928c2a
ms.lasthandoff: 03/31/2017


---

# <a name="determine-the-bom-version"></a>Määritä tuoterakenneversio

Aikana Kysynnän hajottaminen, jos nimikkeellä oletusarvoinen tilaustyyppi tuotannon, suunnitteluohjelma etsii kelvollisen tuoterakenneversion toimipaikan perusteella. 

Toimipaikan dimensio on aina tiedossa. Se ilmoitetaan kysyntätapahtumassa. Seuraavan prosessin avulla määritetään käytettävä tuoterakenneversio:

-   Jos nimikkeelle on määritetty tuoterakenneversio kysynnän toimipaikassa, käytössä on toimipaikkakohtainen tuoterakenne.
-   Jos nimikkeelle ei ole määritetty toimipaikkakohtaista tuoterakenneversiota kysynnän toimipaikassa, käytössä on yleinen tuoterakenne. Yleinen tuoterakenne ei ilmaise toimipaikkaa, ja sitä voi käyttää useissa toimipaikoissa. Jos yleinen tuoterakenne on käytettävissä, ohjelma käyttää sitä.
-   Jos käytettävissä ei ole yleistä tuoterakenneversiota, kysynnän hajottaminen keskeytyy.

Kaikkien kelvollisten toimipaikkakohtaisten tai yleisten tuoterakenneversioiden on täytettävä tarvittavat päivämäärä- ja määräehdot.




