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
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 63160b9473c7f45b0eb0ca7139f9ed47c8e1446f
ms.openlocfilehash: ee45fed40b10dbe913c73e1186b726a39831816d
ms.contentlocale: fi-fi
ms.lasthandoff: 06/20/2017


---

# Mobiililaitteen vanhimman erän kerääminen
<a id="pick-oldest-batch-on-a-mobile-device" class="xliff"></a>

[!include[banner](../includes/banner.md)]

Voit käyttää **Valitse vanhin erä** -määritystä mobiililaitteen valikosta. Voit pakottaa sen avulla varastotyöntekijät keräämään vanhimman erän nykyisestä sijainnista tai varoittaa heitä siitä.  

## Käyttö
<a id="where-it-applies" class="xliff"></a>
Vanhimman erän valinta on määritetty mobiililaitteen valikkovaihtoehdoissa ja se vaikuttaa erän alempien nimikkeiden keräilyyn.

## Vanhimman erän valinnan määrittäminen
<a id="how-to-set-up-the-configuration-for-pick-oldest-batch" class="xliff"></a> 
Aiemmin luotua työtä käyttämään määritetyillä nimikkeillä **Valitse vanhin erä** -asetukseksi voidaan valita **Ei mitään**, **Varoita** tai **Pakota** mobiililaitteen valikossa.

**Ei mitään**: työntekijät eivät saa mitään ilmoituksia ja he saavat kerätä minkä tahansa erä omassa sijainnissaan.

**Varoita** ja **Pakota**: luettelo eristä, joilla on vanhimmat vanhentumispäivät, näytetään erähallinnan yläpuolella, kun työntekijä valitsee erän. Jos rekisterikilven sijainti on ohjattu, rekisterikilpiluettelo, jossa on vanhin erä, näkyy rekisterikilven ohjausobjektin yläpuolella. 
-   **Varoita**: jos työntekijä valitsee rekisterikilven tai erän, joka ei näy luettelossa, ohjausobjekti on tyhjennetty ja varoitus ilmoittaa, että valittavana on vanhempi erä. Työn jatkaminen on edellyttää, että työntekijä valitsee uudelleen saman rekisterikilven tai erän.  
-   **Pakota**: työntekijä saa edelleen ilmoituksia, että valittavana vanhempi erä.

