---
title: Pääsuunnittelu – toimipaikan kattavuus, varasto ei pakollinen
description: Tässä artikkelissa kuvataan, miten suunnitellaan nimike, jolle on suunniteltu toimipaikan dimensio kattavuutta varten.
author: t-benebo
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResStorageDimensionGroup, ReqItemTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2474
ms.assetid: 316da918-67ae-43c5-baea-00ae559e29b0
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6b03bd1970aa7a2f3276186a0a9f8c2cd2880956
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/03/2022
ms.locfileid: "9741146"
---
# <a name="master-planning-for-site-coverage-warehouse-not-mandatory"></a>Pääsuunnittelu – toimipaikan kattavuus, varasto ei pakollinen

[!include [banner](../includes/banner.md)]

Tässä artikkelissa kuvataan, miten suunnitellaan nimike, jolle on suunniteltu toimipaikan dimensio kattavuutta varten.

Tämä pääsuunnitteluskenaario sisältää seuraavat ehdot:

-   Sivuston dimensio on asetettu pakolliseksi ja se on kirjoitettava kysyntätapahtumassa.
-   Varastodimensiota ei ole määritetty pakolliseksi. Varasto on ehkä tiedossa, mutta sitä ei käytetä pääsuunnittelun laskennassa.
-   Toimipaikan dimensio on määritetty kattavuuden suunnittelua varten.
-   Varaston dimensiota ei ole määritetty kattavuuden suunnittelua varten. Tämän vuoksi tarjonta ja kysyntä yhdistetään toimipaikkakohtaisesti ja ehkä myös muiden sellaisten dimensioiden mukaan, joille on tehty kattavuussuunnitelma.

Seuraava kuva osoittaa, miten pääsuunnittelu etenee. Kuvassa viitataan seuraaviin parametreihin:
-   Nimikkeen kattavuus on määritetty nimikkeelle. Valitse **Tuotetietojen hallinta &gt; Tuotteet &gt; Vapautetut tuotteet**. Valitse nimike ja valitse sitten **Suunnitelma &gt; Nimikkeen kattavuus**.
-   Varastolle on määritetty täydennyssuhteet. Valitse **Inventoinnin- ja varastonhallinta &gt; Asetukset &gt; Varastoerittely &gt; Varastot** Valitse **Pääsuunnittelu**-välilehdessä **Päävarasto**-kenttäryhmä.
-   Oletustilauksen tyypiksi on määritetty Tuotanto, Ostotilaus tai Kanban. Valitse **Tuotetietojen hallinta &gt; Tuotteet &gt; Vapautetut tuotteet**. Valitse nimike ja valitse sitten **Suunnitelma &gt; Tilauksen oletusasetukset**. Tarkista **Tilauksen oletusasetukset** -lomakkeesta **Oletusarvoinen tilaustyyppi** -kenttä.

![Toimipaikan kattavuuden kysyntä, varasto ei pakollinen.](./media/multisitedemandexplosionscenarioforsitecoveragewarehousenotmandatory.jpg)



## <a name="additional-resources"></a>Lisäresurssit

- [Pääsuunnittelu ja multisite-toiminnot – yleiskatsaus](master-plan-multisite-functionality.md)
- [Toimipaikan ja varaston kattavuuden pääsuunnittelu, varasto pakollinen](master-plan-site-coverage-warehouse-mandatory.md)
- [Pääsuunnittelu toimipaikan kattavuudelle, varasto pakollinen](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)
- [Pääsuunnittelu toimipaikan kattavuudelle, varasto ei pakollinen](master-plan-site-warehouse-coverage-warehouse-mandatory.md)
- [Tuoterakenneversion määrittäminen](master-plan-bom-version-determined.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]