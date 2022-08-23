---
title: RCS-parannettu suodatus RCS:ssä/yleisessä tietovarastossa
description: Tässä artikkelissa kuvataan parannetut suodatusominaisuudet RSC:n yleiselle tietovarastolle. Ominaisuuksia on parannettu niin, että ne sisältävät lisäsuodattimia.
author: kfend
ms.date: 04/24/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.custom: 97423
ms.assetid: ''
ms.search.form: ERSolutionTable, ERWorkspace
ms.openlocfilehash: e0408d0561c0cfead8781b9f49fdb84d5caf179a
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9274509"
---
# <a name="rcs-enhanced-filtering-options-for-finding-configurations-in-the-rcsglobal-repository"></a>RCS-parannetut suodatusvaihtoehdot konfiguraatioiden löytämiseksi RCS:stä/yleisestä tietovarastosta

[!include [banner](../includes/banner.md)]

Tässä artikkelissa kuvataan parannetut suodatusominaisuudet RSC:n (Regulatory Configuration Services) yleiselle tietovarastolle. Ominaisuuksia on parannettu niin, että ne sisältävät kyvyn suodattaa seuraavilla kriteereillä: 
- **Maa/alue** - Perustuu ISO-maakoodeihin  
- **Tunnisteet** tyypit:
  - Toiminnallinen alue
  - Ominaisuusalue
  - Toimiala 
  - Liiketoiminta-asiakirja 

Tehdäksesi helpommaksi löytää tiettyjä tai toisiinsa liittyviä konfiguraatioita, voit käyttää suodattimia joko yksitellen tai ryhminä. Jos esimerkiksi haluat löytää yhden tyyppisiä konfiguroitavissa olevia liiketoiminta-asiakirjoja, jotka liittyvät toimittajalaskuihin, voit käyttää **Liiketoiminta-asiakirjatyyppi**-suodatinta kyseisen asiakirjatyypin etsimiseen. 

[![Yleisen tietovaraston suodatusosa.](media/rcs-enhanced-filter-section.JPG)](./media/rcs-enhanced-filter-section.JPG) 

Voit tarkentaa hakua valitsemalla tiedostotyypin, esimerkiksi toimittajan lasku ja valitsemalla sitten **Käytä suodatinta**. Seuraavassa esimerkissä ovat tulokset, kun suodatetaan **Liiketoiminta-asiakirjan tyyppi**, kun asiakirjatyyppi on lisätty. 

[![Kohdistettu suodatin ja liiketoiminta-asiakirjan tyypin tuonti.](media/rcs-enhanced-filtering-applied.JPG)](./media/rcs-enhanced-filtering-applied.JPG) 

Suodatetut tulokset voidaan tuoda käyttäjien RCS-arkistoon tai Dynamics 365 Finance -ympäristöön joko yksittäin tai osana. Voit tehdä tämän valitsemalla konfiguraatioryhmän ja valitsemalla **Tuo**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
