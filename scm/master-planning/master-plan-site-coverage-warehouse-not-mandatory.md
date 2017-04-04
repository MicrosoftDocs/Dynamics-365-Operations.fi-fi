---
title: "Pääsuunnittelun toimipaikan kattavuutta varten, varasto ei pakollinen"
description: "Tässä aiheessa kuvataan, miten suunnitellaan nimike, jolle on suunniteltu toimipaikan dimensio kattavuutta varten."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: EcoResStorageDimensionGroup, ReqItemTable
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 2474
ms.assetid: 316da918-67ae-43c5-baea-00ae559e29b0
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 28607f0fc8db99c9fc8e96b4514763b8cf589dd8
ms.lasthandoff: 03/31/2017


---

# <a name="master-planning-for-site-coverage-warehouse-not-mandatory"></a>Pääsuunnittelun toimipaikan kattavuutta varten, varasto ei pakollinen

Tässä aiheessa kuvataan, miten suunnitellaan nimike, jolle on suunniteltu toimipaikan dimensio kattavuutta varten.

Tämä pääsuunnitteluskenaario sisältää seuraavat ehdot:

-   Sivuston dimensio on asetettu pakolliseksi ja se on kirjoitettava kysyntätapahtumassa.
-   Varastodimensiota ei ole määritetty pakolliseksi. Varasto on ehkä tiedossa, mutta sitä ei käytetä pääsuunnittelun laskennassa.
-   Toimipaikan dimensio on määritetty kattavuuden suunnittelua varten.
-   Varaston dimensiota ei ole määritetty kattavuuden suunnittelua varten. Tämän vuoksi tarjonta ja kysyntä yhdistetään toimipaikkakohtaisesti ja ehkä myös muiden sellaisten dimensioiden mukaan, joille on tehty kattavuussuunnitelma.

Seuraava kuva osoittaa, miten pääsuunnittelu etenee. Kuvassa viitataan seuraaviin parametreihin:
-   Nimikkeen kattavuus on määritetty nimikkeelle. Valitse **tuotetietojen hallinta &gt;tuotteita&gt; vapautetut tuotteet**. Valitse nimike ja valitse sitten **suunnitelma &gt;nimikkeen kattavuus**.
-   Varastolle on määritetty täydennyssuhteet. Valitse **Inventory management &gt;asennus &gt;varastoerittelyä &gt;varastot**. Valitse **Pääsuunnittelu**-välilehdessä **Päävarasto**-kenttäryhmä.
-   Oletustilauksen tyypiksi on määritetty Tuotanto, Ostotilaus tai Kanban. Valitse **tuotetietojen hallinta &gt;tuotteita&gt; vapautetut tuotteet**. Valitse nimike ja valitse sitten **suunnitelma &gt;tilauksen oletusasetukset**. Tarkista **Tilauksen oletusasetukset** -lomakkeesta **Oletusarvoinen tilaustyyppi** -kenttä.

![Toimipaikan kattavuuden kysyntä, varasto ei pakollinen    ](./media/multisitedemandexplosionscenarioforsitecoveragewarehousenotmandatory.jpg)



<a name="see-also"></a>Lisätietoja
--------

[Master planning and multisite functionality](master-plan-multisite-functionality.md)

[Pääsuunnittelu – sivuston kattavuus, varasto pakollinen](master-plan-site-coverage-warehouse-mandatory.md)

[Pääsuunnittelu – toimipaikan ja varaston kattavuus, varasto ei pakollinen](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[Pääsuunnittelu – sivuston ja varaston kattavuus, varasto pakollinen](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[Pääsuunnittelu - miten määräytyy Tuoterakenteen versio](master-plan-bom-version-determined.md)


