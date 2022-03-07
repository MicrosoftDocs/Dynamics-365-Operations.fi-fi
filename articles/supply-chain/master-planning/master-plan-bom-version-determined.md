---
title: Määritä tuoterakenneversio
description: Jos nimikkeen suunniteltuna oletustilaustyyppinä on kysynnän hajottamisen aikana Tuotanto, suunnitteluohjelma etsii kelvollisen tuoterakenneversion toimipaikan perusteella.
author: ChristianRytt
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BOMConsistOf, BOMDesigner, InventItemOrderSetup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2534
ms.assetid: a5b64301-a011-4469-afaf-e4c9164ef9c6
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 370091eed4ee050031d5d135aa7b1d8d0fe82491
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/29/2021
ms.locfileid: "7570966"
---
# <a name="determine-the-bom-version"></a>Määritä tuoterakenneversio

[!include [banner](../includes/banner.md)]

Jos nimikkeen suunniteltuna oletustilaustyyppinä on kysynnän hajottamisen aikana Tuotanto, suunnitteluohjelma etsii kelvollisen tuoterakenneversion toimipaikan perusteella. 

Toimipaikan dimensio on aina tiedossa. Se ilmoitetaan kysyntätapahtumassa. Seuraavan prosessin avulla määritetään käytettävä tuoterakenneversio:

-   Jos nimikkeelle on määritetty tuoterakenneversio kysynnän toimipaikassa, käytössä on toimipaikkakohtainen tuoterakenne.
-   Jos nimikkeelle ei ole määritetty toimipaikkakohtaista tuoterakenneversiota kysynnän toimipaikassa, käytössä on yleinen tuoterakenne. Yleinen tuoterakenne ei ilmaise toimipaikkaa, ja sitä voi käyttää useissa toimipaikoissa. Jos yleinen tuoterakenne on käytettävissä, ohjelma käyttää sitä.
-   Jos käytettävissä ei ole yleistä tuoterakenneversiota, kysynnän hajottaminen keskeytyy.

Kaikkien kelvollisten toimipaikkakohtaisten tai yleisten tuoterakenneversioiden on täytettävä tarvittavat päivämäärä- ja määräehdot.







[!INCLUDE[footer-include](../../includes/footer-banner.md)]