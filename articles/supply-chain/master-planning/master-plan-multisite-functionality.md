---
title: Pääsuunnittelu ja multisite-toiminnot – yleiskatsaus
description: Pääsuunnittelussa otetaan huomioon toimipaikan ja varaston dimensioiden asetukset.
author: ChristianRytt
ms.date: 07/25/2019
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: InventLocation, InventSite
audience: Application User
ms.reviewer: kamaybac
ms.custom:
- "2434"
- intro-internal
ms.assetid: 7f05c031-a446-4168-8cce-03a6305f5c4d
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e594cfd71201c6a629c04d5557c117649e6b19b0
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2022
ms.locfileid: "7982326"
---
# <a name="master-planning-and-multisite-functionality-overview"></a>Pääsuunnittelu ja multisite-toiminnot – yleiskatsaus

[!include [banner](../includes/banner.md)]

Pääsuunnittelussa otetaan huomioon toimipaikan ja varaston dimensioiden asetukset. 

Toimipaikkadimensio on pakollinen ja myös varastodimension voi määrittää pakolliseksi.

Kun dimensio on pakollinen, kaikkiin varastotapahtumiin on syötettävä dimension arvo. Sen vuoksi alkuperäisen kysynnän toimipaikka ja varasto ovat tunnettuja pääsuunnittelun aikana. Toimipaikkadimensio on myös yhdenmukainen, jolloin toimipaikan arvo ei muutu alemman tason kysynnän hajotuksen aikana.

Kun varastoa ei määritetä pakolliseksi, se ei välttämättä ole tunnettu alkuperäisessä kysynnässä. Suunnitteluohjelman on määritettävä käytettävä varasto nimikkeelle ja yksittäisille varastoille määritettyjen asetusten sekä tilausrivin tietojen perusteella.

Seuraavat aiheet kuvaavat suunnitteluohjelman toimintaa määritettäessä erilaisia asetuksia käytettävän varaston määrityksessä.

[Toimipaikan ja varaston kattavuuden pääsuunnittelu, varasto pakollinen](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[Pääsuunnittelu toimipaikan kattavuudelle, varasto pakollinen](master-plan-site-coverage-warehouse-mandatory.md)

[Toimipaikan ja varaston kattavuuden pääsuunnittelu, varasto ei pakollinen](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[Pääsuunnittelu toimipaikan kattavuudelle, varasto ei pakollinen](master-plan-site-coverage-warehouse-not-mandatory.md)

[Tuoterakenneversion määrittäminen](master-plan-bom-version-determined.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]