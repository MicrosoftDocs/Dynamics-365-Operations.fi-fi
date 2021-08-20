---
title: Määritä tuoterakenneversio
description: Jos nimikkeen suunniteltuna oletustilaustyyppinä on kysynnän hajottamisen aikana Tuotanto, suunnitteluohjelma etsii kelvollisen tuoterakenneversion toimipaikan perusteella.
author: roxanadiaconu
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
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 91a55bfcd10ee0efbbf1170ad29194c17ea72d62cf5516e2661b43bad7446808
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6766071"
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