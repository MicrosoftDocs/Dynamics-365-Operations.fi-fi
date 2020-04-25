---
title: Erän ja rekisterikilven tiedot
description: Tässä ohjeaiheessa kerrotaan erän ja rekisterikilven vahvistuksen määrittämisestä ja käyttämisestä mobiililaitteessa.
author: Mirzaab
manager: tfehr
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFAutoConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 020d33bfb7e23df7898414f5becf96d31307f2fa
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/02/2020
ms.locfileid: "3201315"
---
# <a name="batch-and-license-plate-confirmation"></a>Erän ja rekisterikilven tiedot

[!include [banner](../includes/banner.md)]

Erän vahvistuksen avulla mobiililaitteessa voidaan vahvistaa, että kerättävä erä on oikea. Kun vain yläpuolella olevien nimikkeiden erän keräilytyö tehdään ensimmäisen kerran, yläpuolella oleva erä ilmaiseen eräalueet, jotka ovat hakuhierarkiassa sijaintia korkeammalla, sinun on vahvistettava, että kerättävä erä vastaa työrivillä olevaa erää. 

Rekisterikilven vahvistuksen avulla mobiililaitteessa voidaan vahvistaa, että kerättävä rekisterikilpi on oikea. Kun työ kerätään väliaikaisesta sijainnista, sinun on varmistettava, että kerättävä rekisterikilpi vastaa työhön liitettyä rekisterikilpeä. Jos työ aloitetaan rekisterikilven skannauksella, tämä vahvistusvaihe ohitetaan.

## <a name="where-it-applies"></a>Käyttö
Vahvistusta käytetään seuraavissa skenaarioissa:

- Erän vahvistusta käytetään yläpuolella olevan nimike-erän ensimmäisissä keräilytöissä.
- Rekisterikilven vahvistusta käytetään väliaikaisista sijainneista tehtävissä keräilyissä.

## <a name="set-up-batch-and-license-plate-confirmation"></a>Erän ja rekisterikilven tietojen määrittäminen
Voit määrittää erän ja rekisterikilven tiedot mobiililaitteen valikkovaihtoehdoilla.  
1.  Anna työn vahvistusasetukset mobiililaitteen valikkovaihtoehdoissa.  
2.  Valitse jo erän tai rekisterikilven vahvistusvaihtoehto. Kumpikin vaihtoehto on valittavissa keräilytyötyypeissä, joissa automaattista vahvistusta ei ole otettu käyttöön.  
