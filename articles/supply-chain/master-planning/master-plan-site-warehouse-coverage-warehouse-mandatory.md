---
title: Pääsuunnittelu – toimipaikan ja varaston kattavuus, varasto pakollinen
description: Tässä aiheessa kuvataan, miten suunnitellaan nimike, jolla on toimipaikka ja varasto kattavuusdimensiona. Varastodimensio ei ole pakollinen.
author: t-benebo
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResStorageDimensionGroup, ReqItemTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2554
ms.assetid: 3211e95f-b91a-4d27-8d92-f328ae2bcf12
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9055969391f9aed3780de871cd34de80e367ff5e
ms.sourcegitcommit: ad1afc6893a8dc32d1363395666b0fe1d50e983a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/23/2022
ms.locfileid: "8468801"
---
# <a name="master-planning-for-site-and-warehouse-coverage-warehouse-mandatory"></a>Pääsuunnittelu – toimipaikan ja varaston kattavuus, varasto pakollinen

[!include [banner](../includes/banner.md)]

Tässä aiheessa kuvataan, miten suunnitellaan nimike, jolla on toimipaikka ja varasto kattavuusdimensiona. Varastodimensio ei ole pakollinen.

Tämä pääsuunnitteluskenaario sisältää seuraavat ehdot:

-   Sivuston dimensio on asetettu pakolliseksi ja se on kirjoitettava kysyntätapahtumassa.
-   Varaston dimensio on asetettu pakolliseksi ja se on määritettävä kysyntätapahtumassa.
-   Toimipaikan ja varaston dimensiot on määritetty kattavuuden suunnittelua varten. Myös muita dimensioita voidaan määrittää kattavuuden suunnittelua varten. Multisite-toiminnot eivät kuitenkaan vaikuta niihin.

Seuraava kuva osoittaa, miten pääsuunnittelu etenee. Kuvassa viitataan seuraaviin parametreihin:
-   Varaston asetukseksi on määritetty **Manuaalinen**. Valitse **Inventoinnin- ja varastonhallinta &gt; Asetukset &gt; Varastoerittely &gt; Varastot** Tarkista **Pääsuunnittelu**-pikavälilehden **Manuaalinen**-kenttä.
-   Nimikkeen kattavuus on määritetty nimikkeelle. Valitse **Tuotetietojen hallinta &gt; Tuotteet &gt; Vapautetut tuotteet**. Valitse ensin nimike ja sitten toimintoruudun **Suunnittelu**-välilehdessä **Nimikkeen kattavuus**.
-   Varastolle on määritetty täydennyssuhteet. Valitse **Inventoinnin- ja varastonhallinta &gt; Asetukset &gt; Varastoerittely &gt; Varastot** Tarkista **Pääsuunnittelu**-pikavälilehdessä **Päävarasto**-kenttäryhmä.
-   Oletustilauksen tyypiksi on määritetty Tuotanto, Ostotilaus tai Kanban. Valitse **Tuotetietojen hallinta &gt; Tuotteet &gt; Vapautetut tuotteet**. Valitse ensin nimike ja sitten toimintoruudun **Suunnittelu**-välilehdessä **Tilauksen oletusasetukset**. Tarkista **Tilauksen oletusasetukset** -lomakkeessa **Oletusarvoinen tilaustyyppi**.

![Kysynnän toimipaikka ja varaston kattavuus, varasto pakollinen.](./media/multisitedemandexplosionscenarioforsiteandwarehousecoveragewarehousemandatory.jpg)



## <a name="additional-resources"></a>Lisäresurssit

[Pääsuunnittelu ja multisite-toiminnot – yleiskatsaus](master-plan-multisite-functionality.md)

[Pääsuunnittelu toimipaikan kattavuudelle, varasto pakollinen](master-plan-site-coverage-warehouse-mandatory.md)

[Pääsuunnittelu toimipaikan kattavuudelle, varasto ei pakollinen](master-plan-site-coverage-warehouse-not-mandatory.md)

[Toimipaikan ja varaston kattavuuden pääsuunnittelu, varasto ei pakollinen](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[Tuoterakenneversion määrittäminen](master-plan-bom-version-determined.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]