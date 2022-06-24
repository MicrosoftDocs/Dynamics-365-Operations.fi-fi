---
title: Mobiililaitteen vanhimman erän kerääminen
description: Tässä artikkelissa kerrotaan mobiililaitteen vanhimman erän keräysvaihtoehdon määrittämisestä ja käyttämisestä.
author: Mirzaab
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSRFMenuItem
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ad1f2cfd029d71784d5efcc169178a791f0ae077
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8885635"
---
# <a name="pick-oldest-batch-on-a-mobile-device"></a>Mobiililaitteen vanhimman erän kerääminen

[!include [banner](../includes/banner.md)]

Voit käyttää **Valitse vanhin erä** -määritystä mobiililaitteen valikosta. Voit pakottaa sen avulla varastotyöntekijät keräämään vanhimman erän nykyisestä sijainnista tai varoittaa heitä siitä.  

## <a name="where-it-applies"></a>Käyttö
Vanhimman erän valinta on määritetty mobiililaitteen valikkovaihtoehdoissa ja se vaikuttaa erän alempien nimikkeiden keräilyyn.

## <a name="how-to-set-up-the-configuration-for-pick-oldest-batch"></a>Vanhimman erän valinnan määrittäminen 
Aiemmin luotua työtä käyttämään määritetyillä nimikkeillä **Valitse vanhin erä** -asetukseksi voidaan valita **Ei mitään**, **Varoita** tai **Pakota** mobiililaitteen valikossa.

**Ei mitään**: työntekijät eivät saa mitään ilmoituksia ja he saavat kerätä minkä tahansa erä omassa sijainnissaan.

**Varoita** ja **Pakota**: luettelo eristä, joilla on vanhimmat vanhentumispäivät, näytetään erähallinnan yläpuolella, kun työntekijä valitsee erän. Jos rekisterikilven sijainti on ohjattu, rekisterikilpiluettelo, jossa on vanhin erä, näkyy rekisterikilven ohjausobjektin yläpuolella. 
-   **Varoita**: jos työntekijä valitsee rekisterikilven tai erän, joka ei näy luettelossa, ohjausobjekti on tyhjennetty ja varoitus ilmoittaa, että valittavana on vanhempi erä. Työn jatkaminen on edellyttää, että työntekijä valitsee uudelleen saman rekisterikilven tai erän.  
-   **Pakota**: työntekijä saa edelleen ilmoituksia, että valittavana vanhempi erä.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]