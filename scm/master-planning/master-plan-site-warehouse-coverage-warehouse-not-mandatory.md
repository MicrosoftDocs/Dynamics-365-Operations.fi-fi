---
title: "Pääsuunnittelu – toimipaikan ja varaston kattavuus, varasto ei pakollinen"
description: "Tässä aiheessa kuvataan, miten suunnitellaan nimike, jolla on toimipaikka ja varasto kattavuusdimensiona. Varastodimensio ei ole pakollinen."
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
ms.custom: 2514
ms.assetid: 92d47bdd-df68-4f60-ac9a-96aa08236c26
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 3671024dc097c94638b1579d7cacc8447c49e97b
ms.lasthandoff: 03/31/2017


---

# <a name="master-planning-for-site-and-warehouse-coverage-warehouse-not-mandatory"></a>Pääsuunnittelu – toimipaikan ja varaston kattavuus, varasto ei pakollinen

[!include[banner](../includes/banner.md)]


Tässä aiheessa kuvataan, miten suunnitellaan nimike, jolla on toimipaikka ja varasto kattavuusdimensiona. Varastodimensio ei ole pakollinen.

Tämä pääsuunnitteluskenaario sisältää seuraavat ehdot:

-   Sivuston dimensio on asetettu pakolliseksi ja se on kirjoitettava kysyntätapahtumassa. Tätä asetusta ei voi muokata.
-   Varastodimensiota ei ole määritetty pakolliseksi. Varasto on ehkä tiedossa, mutta sitä ei käytetä pääsuunnittelun laskennassa.
-   Toimipaikan ja varaston dimensiot on määritetty kattavuuden suunnittelua varten. Myös muita dimensioita voidaan määrittää kattavuuden suunnittelua varten. Multisite-toiminnot eivät kuitenkaan vaikuta niihin.

Seuraava kuva osoittaa, miten pääsuunnittelu etenee. Kuvassa viitataan seuraaviin parametreihin:
-   Varaston asetukseksi on määritetty Manuaalinen. Valitse **Inventoinnin- ja varastonhallinta &gt; Asetukset &gt; Varastoerittely &gt; Varastot** Tarkista **Pääsuunnittelu**-pikavälilehden **Manuaalinen**-kenttä.
-   Nimikkeen kattavuus on määritetty nimikkeelle. Valitse **Tuotetietojen hallinta &gt; Tuotteet &gt; Vapautetut tuotteet**. Valitse ensin nimike ja sitten toimintoruudun **Suunnittelu**-välilehdessä **Nimikkeen kattavuus**.
-   Varastolle on määritetty täydennyssuhteet. Valitse **Inventoinnin- ja varastonhallinta &gt; Asetukset &gt; Varastoerittely &gt; Varastot** Tarkista **Pääsuunnittelu**-pikavälilehdessä **Päävarasto**-kenttäryhmä.
-   Oletustilauksen tyypiksi on määritetty Tuotanto, Ostotilaus tai Kanban. Valitse **Tuotetietojen hallinta &gt; Tuotteet &gt; Vapautetut tuotteet**. Valitse ensin nimike ja sitten toimintoruudun **Suunnittelu**-välilehdessä **Tilauksen oletusasetukset**. Tarkista **Tilauksen oletusasetukset** -lomakkeessa **Oletusarvoinen tilaustyyppi**.

![Toimipaikan ja varaston kysyntä, ei varastoa](./media/multisitedemandexplosionscenarioforsiteandwarehousecoveragewarehousenotmandatory.jpg)

 
-



<a name="see-also"></a>Lisätietoja
--------

[Pääsuunnittelu ja multisite-toiminnot](master-plan-multisite-functionality.md)

[Pääsuunnittelu – sivuston ja varaston kattavuus, varasto pakollinen](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[Pääsuunnittelu – sivuston kattavuus, varasto pakollinen](master-plan-site-coverage-warehouse-mandatory.md)

[Pääsuunnittelu – sivuston kattavuus, varasto ei pakollinen](master-plan-site-coverage-warehouse-not-mandatory.md)

[Pääsuunnittelu – tuoterakenneversion määrittäminen](master-plan-bom-version-determined.md)




