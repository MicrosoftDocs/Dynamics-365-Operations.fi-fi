---
title: Parannettu suodatus RCS:ssä / yleisessä tietovarastossa
description: Tässä ohjeaiheessa kuvataan parannetut suodatusominaisuudet RSC:n yleiselle tietovarastolle. Ominaisuuksia on parannettu niin, että ne sisältävät lisäsuodattimia.
author: JaneA07
manager: AnnBe
ms.date: 03/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, ERWorkspace
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 1adbd690795139778dc77a574e9d5f91a4bdeb3c
ms.sourcegitcommit: ff6dde637d2f5d2bd18a582eb41573d4c69acdd6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/08/2020
ms.locfileid: "3249162"
---
# <a name="enhanced-filtering-options-for-finding-configurations-in-the-global-repository"></a>Parannetut suodatusvaihtoehdot yleisten tietovaraston kokoonpanojen etsimiseen

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa kuvataan parannetut suodatusominaisuudet RSC:n (Regulatory Configuration Services) yleiselle tietovarastolle. Ominaisuuksia on parannettu niin, että ne sisältävät seuraavat suodattimet: 
- **Maa/alue** - perustuu ISO-maakoodeihin  
- **Tunnisteet** - toiminnallinen alue / toimintoalue; toimiala; liiketoiminta-asiakirjan tyyppi 

Voit käyttää suodattimia joko yksitellen tai ryhminä, jos haluat etsiä tiettyjä tai toisiinsa liittyviä konfiguraatioita. Jos esimerkiksi haluat etsiä kaikki konfiguroitavat liiketoiminta-asiakirjat, jotka liittyvät toimittajan laskuihin, voit käyttää **Liiketoiminta-asiakirjan tyyppi** -suodatinta. 

Voit muokata hakua lisää valitsemalla maakoodin ja valitsemalla sitten **Käytä suodatinta**.  

[![Yleisen tietovaraston suodatusosa](media/rcs-enhanced-filter-section.JPG)](./media/rcs-enhanced-filter-section.JPG) 

Seuraavassa esimerkissä ovat tulokset, kun suodatetaan **Liiketoiminta-asiakirjan tyyppi**. 

[![Kohdistettu suodatin ja liiketoiminta-asiakirjan tyypin tuonti](media/rcs-enhanced-filtering-applied.JPG)](./media/rcs-enhanced-filtering-applied.JPG) 

Suodatetut tulokset voidaan tuoda käyttäjille RCS- tai Dynamics 365 Finance -ympäristössä yksitellen tai joukkona (valitsemalla konfiguraatioiden ryhmä) ja valitsemalla **Tuo**.






