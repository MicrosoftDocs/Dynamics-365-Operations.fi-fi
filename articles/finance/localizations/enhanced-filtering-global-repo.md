---
title: RCS-parannettu suodatus RCS:ssä/yleisessä tietovarastossa
description: Tässä ohjeaiheessa kuvataan parannetut suodatusominaisuudet RSC:n yleiselle tietovarastolle. Ominaisuuksia on parannettu niin, että ne sisältävät lisäsuodattimia.
author: JaneA07
manager: AnnBe
ms.date: 04/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, ERWorkspace
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: a67a4345271cbeffc100fc1d9077cc866846a4d4
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "5005839"
---
# <a name="rcs-enhanced-filtering-options-for-finding-configurations-in-the-rcsglobal-repository"></a>RCS-parannetut suodatusvaihtoehdot konfiguraatioiden löytämiseksi RCS:stä/yleisestä tietovarastosta

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa kuvataan parannetut suodatusominaisuudet RSC:n (Regulatory Configuration Services) yleiselle tietovarastolle. Ominaisuuksia on parannettu niin, että ne sisältävät kyvyn suodattaa seuraavilla kriteereillä: 
- **Maa/alue** - Perustuu ISO-maakoodeihin  
- **Tunnisteet** tyypit:
  - Toiminnallinen alue
  - Ominaisuusalue
  - Toimiala 
  - Liiketoiminta-asiakirja 

Tehdäksesi helpommaksi löytää tiettyjä tai toisiinsa liittyviä konfiguraatioita, voit käyttää suodattimia joko yksitellen tai ryhminä. Jos esimerkiksi haluat löytää yhden tyyppisiä konfiguroitavissa olevia liiketoiminta-asiakirjoja, jotka liittyvät toimittajalaskuihin, voit käyttää **Liiketoiminta-asiakirjatyyppi**-suodatinta kyseisen asiakirjatyypin etsimiseen. 

[![Yleisen tietovaraston suodatusosa](media/rcs-enhanced-filter-section.JPG)](./media/rcs-enhanced-filter-section.JPG) 

Voit tarkentaa hakua valitsemalla tiedostotyypin, esimerkiksi toimittajan lasku ja valitsemalla sitten **Käytä suodatinta**. Seuraavassa esimerkissä ovat tulokset, kun suodatetaan **Liiketoiminta-asiakirjan tyyppi**, kun asiakirjatyyppi on lisätty. 

[![Kohdistettu suodatin ja liiketoiminta-asiakirjan tyypin tuonti](media/rcs-enhanced-filtering-applied.JPG)](./media/rcs-enhanced-filtering-applied.JPG) 

Suodatetut tulokset voidaan tuoda käyttäjien RCS-arkistoon tai Dynamics 365 Finance -ympäristöön joko yksittäin tai osana. Voit tehdä tämän valitsemalla konfiguraatioryhmän ja valitsemalla **Tuo**.
