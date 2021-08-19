---
title: Erän ja rekisterikilven tiedot
description: Tässä ohjeaiheessa kerrotaan erän ja rekisterikilven vahvistuksen määrittämisestä ja käyttämisestä mobiililaitteessa.
author: Mirzaab
ms.date: 11/11/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSRFAutoConfirm
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 13e246f9a496dcc38829eef788d09c50300c99fb95daffad134012733341e4af
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6726534"
---
# <a name="batch-and-license-plate-confirmation"></a>Erän ja rekisterikilven tiedot

[!include [banner](../includes/banner.md)]

Erän vahvistuksen avulla mobiililaitteessa voidaan vahvistaa, että kerättävä erä on oikea. Kun vain *erä-yllä\[sijainti\]* -nimikkeiden erän keräilytyö tehdään ensimmäisen kerran, erä-yllä ilmaisee, että erä on hakuhierarkiassa sijaintia korkeammalla, sinun on vahvistettava, että kerättävä erä vastaa työrivillä olevaa erää.

Rekisterikilven vahvistuksen avulla mobiililaitteessa voidaan vahvistaa, että kerättävä rekisterikilpi on oikea. Kun työ kerätään väliaikaisesta sijainnista, sinun on varmistettava, että kerättävä rekisterikilpi vastaa työhön liitettyä rekisterikilpeä. Jos työ aloitetaan rekisterikilven skannauksella, tämä vahvistusvaihe ohitetaan.

## <a name="where-it-applies"></a>Käyttö

Vahvistusta käytetään seuraavissa skenaarioissa:

- Erän vahvistusta käytetään yläpuolella olevan nimike-erän ensimmäisissä keräilytöissä.
- Rekisterikilven vahvistusta käytetään väliaikaisista sijainneista tehtävissä keräilyissä.

> [!IMPORTANT]
> Täydennystä ei tueta rekisterikilven vahvistuksessa. Täydennystyötä suoritettaessa ei luoda rekisterikilven vahvistusvaihetta.

## <a name="set-up-batch-and-license-plate-confirmation"></a>Erän ja rekisterikilven tietojen määrittäminen

Voit määrittää erän ja rekisterikilven tiedot mobiililaitteen valikkovaihtoehdoilla.

1. Anna työn vahvistusasetukset mobiililaitteen valikkovaihtoehdoissa.  
1. Valitse jo erän tai rekisterikilven vahvistusvaihtoehto. Kumpikin vaihtoehto on valittavissa keräilytyötyypeissä, joissa automaattista vahvistusta ei ole otettu käyttöön.  


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
