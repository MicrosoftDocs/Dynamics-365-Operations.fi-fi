---
title: Pääsuunnittelu ja multisite-toiminnot – yleiskatsaus
description: Pääsuunnittelussa otetaan huomioon toimipaikan ja varaston dimensioiden asetukset.
author: roxanadiaconu
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventLocation, InventSite
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2434
ms.assetid: 7f05c031-a446-4168-8cce-03a6305f5c4d
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4f05e3efd1716a27a659ae40145f37bb0b3d977f
ms.sourcegitcommit: e286572ce94a9442a5b3076c3ff5b429be0ed512
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/06/2019
ms.locfileid: "1865398"
---
# <a name="master-planning-and-multisite-functionality-overview"></a>Pääsuunnittelu ja multisite-toiminnot – yleiskatsaus

[!include [banner](../includes/banner.md)]

Pääsuunnittelussa otetaan huomioon toimipaikan ja varaston dimensioiden asetukset. 

Toimipaikkadimensio on pakollinen ja myös varastodimension voi määrittää pakolliseksi.

Kun dimensio on pakollinen, kaikkiin varastotapahtumiin on syötettävä dimension arvo. Sen vuoksi alkuperäisen kysynnän toimipaikka ja varasto ovat tunnettuja pääsuunnittelun aikana. Toimipaikkadimensio on myös yhdenmukainen, jolloin toimipaikan arvo ei muutu alemman tason kysynnän hajotuksen aikana.

Kun varastoa ei määritetä pakolliseksi, se ei välttämättä ole tunnettu alkuperäisessä kysynnässä. Suunnitteluohjelman on määritettävä käytettävä varasto nimikkeelle ja yksittäisille varastoille määritettyjen asetusten sekä tilausrivin tietojen perusteella.

Seuraavat aiheet kuvaavat suunnitteluohjelman toimintaa määritettäessä erilaisia asetuksia käytettävän varaston määrityksessä.

[Pääsuunnittelu – sivuston ja varaston kattavuus, varasto pakollinen](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[Pääsuunnittelu – sivuston kattavuus, varasto pakollinen](master-plan-site-coverage-warehouse-mandatory.md)

[Pääsuunnittelu – toimipaikan ja varaston kattavuus, varasto ei pakollinen](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[Pääsuunnittelu – sivuston kattavuus, varasto ei pakollinen](master-plan-site-coverage-warehouse-not-mandatory.md)

[Pääsuunnittelu – tuoterakenneversion määrittäminen](master-plan-bom-version-determined.md)



