---
title: "Pääsuunnittelu toimipaikan kattavuudelle, varasto pakollinen"
description: "Tässä aiheessa kuvataan, miten suunnitellaan nimike, jolle on suunniteltu toimipaikka kattavuuden dimensiona. Varasto ei ole pakollinen dimensio."
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
ms.custom: 2454
ms.assetid: aa135030-f98c-48bf-902c-e52f680dc247
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 9e25769fef4d4a9263523f486a7e1782341fd496
ms.contentlocale: fi-fi
ms.lasthandoff: 04/25/2017


---

# <a name="master-planning-for-site-coverage-mandatory-warehouse"></a>Pääsuunnittelu toimipaikan kattavuudelle, varasto pakollinen

[!include[banner](../includes/banner.md)]


Tässä aiheessa kuvataan, miten suunnitellaan nimike, jolle on suunniteltu toimipaikka kattavuuden dimensiona. Varasto ei ole pakollinen dimensio.

Tämä pääsuunnitteluskenaario sisältää seuraavat ehdot:

-   Sivuston dimensio on asetettu pakolliseksi ja se on kirjoitettava kysyntätapahtumassa. Tätä asetusta ei voi muokata.
-   Varaston dimensio on asetettu pakolliseksi ja se on määritettävä kysyntätapahtumassa.
-   Toimipaikan dimensio on määritetty kattavuuden suunnittelua varten. Myös muita dimensioita voidaan määrittää kattavuuden suunnittelua varten. Multisite-toiminnot eivät kuitenkaan vaikuta niihin.
-   Varaston dimensiota ei ole määritetty kattavuuden suunnittelua varten. Tämän vuoksi tarjonta ja kysyntä yhdistetään toimipaikkakohtaisesti ja ehkä myös muiden sellaisten dimensioiden mukaan, joille on tehty kattavuussuunnitelma.

Seuraava kuva osoittaa, miten pääsuunnittelu etenee. Kuvassa viitataan seuraaviin parametreihin:
-   Nimikkeen kattavuus on määritetty nimikkeelle. Valitse **Tuotetietojen hallinta &gt; Tuotteet &gt; Vapautetut tuotteet**. Valitse nimike ja valitse sitten **Suunnitelma &gt; Nimikkeen kattavuus**.
-   Varastolle on määritetty täydennyssuhteet. Valitse **Inventoinnin- ja varastonhallinta &gt; Asetukset &gt; Varastoerittely &gt; Varastot** Valitse **Pääsuunnittelu**-välilehdessä **Päävarasto**-kenttäryhmä.
-   Oletustilauksen tyypiksi on määritetty Tuotanto, Ostotilaus tai Kanban. Valitse **Tuotetietojen hallinta &gt; Tuotteet &gt; Vapautetut tuotteet**. Valitse nimike ja valitse sitten **Suunnitelma &gt; Tilauksen oletusasetukset**. Tarkista **Tilauksen oletusasetukset** -lomakkeessa **Oletusarvoinen tilaustyyppi**.

![Toimipaikan kattavuuden kysyntä, varasto pakollinen](./media/multisitedemandexplosionscenarioforsitecoveragewarehousemandatory.jpg)



<a name="see-also"></a>Lisätietoja
--------

[Pääsuunnittelu ja multisite-toiminnot](master-plan-multisite-functionality.md)

[Pääsuunnittelu – sivuston ja varaston kattavuus, varasto pakollinen](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[Pääsuunnittelu – toimipaikan kattavuus, varasto pakollinen](master-plan-site-coverage-warehouse-mandatory.md)

[Pääsuunnittelu – toimipaikan ja varaston kattavuus, varasto ei pakollinen](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[Pääsuunnittelu – tuoterakenneversion määrittäminen](master-plan-bom-version-determined.md)




