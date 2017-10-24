---
title: "Mobiililaitteen vanhimman erän kerääminen"
description: "Tässä ohjeaiheessa kerrotaan mobiililaitteen vanhimman erän keräysvaihtoehdon määrittämisestä ja käyttämisestä."
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
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 25056886b1a18dbaef12c8732a1fd0bd92a6d04b
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---

# <a name="pick-oldest-batch-on-a-mobile-device"></a>Mobiililaitteen vanhimman erän kerääminen

[!include[banner](../includes/banner.md)]

Voit käyttää **Valitse vanhin erä** -määritystä mobiililaitteen valikosta. Voit pakottaa sen avulla varastotyöntekijät keräämään vanhimman erän nykyisestä sijainnista tai varoittaa heitä siitä.  

## <a name="where-it-applies"></a>Käyttö
Vanhimman erän valinta on määritetty mobiililaitteen valikkovaihtoehdoissa ja se vaikuttaa erän alempien nimikkeiden keräilyyn.

## <a name="how-to-set-up-the-configuration-for-pick-oldest-batch"></a>Vanhimman erän valinnan määrittäminen 
Aiemmin luotua työtä käyttämään määritetyillä nimikkeillä **Valitse vanhin erä** -asetukseksi voidaan valita **Ei mitään**, **Varoita** tai **Pakota** mobiililaitteen valikossa.

**Ei mitään**: työntekijät eivät saa mitään ilmoituksia ja he saavat kerätä minkä tahansa erä omassa sijainnissaan.

**Varoita** ja **Pakota**: luettelo eristä, joilla on vanhimmat vanhentumispäivät, näytetään erähallinnan yläpuolella, kun työntekijä valitsee erän. Jos rekisterikilven sijainti on ohjattu, rekisterikilpiluettelo, jossa on vanhin erä, näkyy rekisterikilven ohjausobjektin yläpuolella. 
-   **Varoita**: jos työntekijä valitsee rekisterikilven tai erän, joka ei näy luettelossa, ohjausobjekti on tyhjennetty ja varoitus ilmoittaa, että valittavana on vanhempi erä. Työn jatkaminen on edellyttää, että työntekijä valitsee uudelleen saman rekisterikilven tai erän.  
-   **Pakota**: työntekijä saa edelleen ilmoituksia, että valittavana vanhempi erä.

