---
title: "Erän ja rekisterikilven tiedot"
description: "Tässä ohjeaiheessa kerrotaan erän ja rekisterikilven vahvistuksen määrittämisestä ja käyttämisestä mobiililaitteessa."
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 63160b9473c7f45b0eb0ca7139f9ed47c8e1446f
ms.openlocfilehash: 70a8c18560f0cfc7a44625520f2f035a6004618a
ms.contentlocale: fi-fi
ms.lasthandoff: 06/20/2017

---

# <a name="batch-and-license-plate-confirmation"></a>Erän ja rekisterikilven tiedot

[!include[banner](../includes/banner.md)]

Erän vahvistuksen avulla mobiililaitteessa voidaan vahvistaa, että kerättävä erä on oikea. Kun vain yläpuolella olevien nimikkeiden erän keräilytyö tehdään ensimmäisen kerran, *yläpuolella oleva erä* ilmaiseen eräalueet, jotka ovat hakuhierarkiassa sijaintia korkeammalla, sinun on vahvistettava, että kerättävä erä vastaa työrivillä olevaa erää. 

Rekisterikilven vahvistuksen avulla mobiililaitteessa voidaan vahvistaa, että kerättävä rekisterikilpi on oikea. Kun työ kerätään väliaikaisesta sijainnista, sinun on varmistettava, että kerättävä rekisterikilpi vastaa työhön liitettyä rekisterikilpeä. Jos työ aloitetaan rekisterikilven skannauksella, tämä vahvistusvaihe ohitetaan.

## <a name="where-it-applies"></a>Käyttö
Vahvistusta käytetään seuraavissa skenaarioissa:

- Erän vahvistusta käytetään yläpuolella olevan nimike-erän ensimmäisissä keräilytöissä.
- Rekisterikilven vahvistusta käytetään väliaikaisista sijainneista tehtävissä keräilyissä.

## <a name="set-up-batch-and-license-plate-confirmation"></a>Erän ja rekisterikilven tietojen määrittäminen
Voit määrittää erän ja rekisterikilven tiedot mobiililaitteen valikkovaihtoehdoilla.  
1.  Anna työn vahvistusasetukset mobiililaitteen valikkovaihtoehdoissa.  
2.  Valitse jo erän tai rekisterikilven vahvistusvaihtoehto. Kumpikin vaihtoehto on valittavissa keräilytyötyypeissä, joissa automaattista vahvistusta ei ole otettu käyttöön.  

