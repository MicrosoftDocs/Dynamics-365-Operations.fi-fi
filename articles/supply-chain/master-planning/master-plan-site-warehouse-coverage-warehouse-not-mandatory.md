---
title: Pääsuunnittelu – toimipaikan ja varaston kattavuus, varasto ei pakollinen
description: Tässä aiheessa kuvataan, miten suunnitellaan nimike, jolla on toimipaikka ja varasto kattavuusdimensiona. Varastodimensio ei ole pakollinen.
author: roxanadiaconu
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResStorageDimensionGroup, ReqItemTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2514
ms.assetid: 92d47bdd-df68-4f60-ac9a-96aa08236c26
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e47531c75e54b23054464a5e1b1841eb2d82e093
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4426813"
---
# <a name="master-planning-for-site-and-warehouse-coverage-warehouse-not-mandatory"></a>Pääsuunnittelu – toimipaikan ja varaston kattavuus, varasto ei pakollinen

[!include [banner](../includes/banner.md)]

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



<a name="additional-resources"></a>Lisäresurssit
--------

[Pääsuunnittelu ja multisite-toiminnot – yleiskatsaus](master-plan-multisite-functionality.md)

[Pääsuunnittelu toimipaikan kattavuudelle, varasto pakollinen](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[Toimipaikan ja varaston kattavuuden pääsuunnittelu, varasto pakollinen](master-plan-site-coverage-warehouse-mandatory.md)

[Toimipaikan ja varaston kattavuuden pääsuunnittelu, varasto ei pakollinen](master-plan-site-coverage-warehouse-not-mandatory.md)

[Tuoterakenneversion määrittäminen](master-plan-bom-version-determined.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]