---
title: Varastokirjauskansion työnkulun ehdot koskevat kirjauskansion tasoa, eivät rivitasoa
description: Varastokirjauskansion työnkulun ehtoja käytetään vain kirjauskansiotasolla, ei rivitasolla.
author: sherry-zheng
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 46bdde7f09c639fbefd46162431762b056d521ae
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476227"
---
# <a name="inventory-journal-workflow-conditions-apply-at-the-journal-level-not-line-level"></a>Varastokirjauskansion työnkulun ehdot koskevat kirjauskansion tasoa, eivät rivitasoa

## <a name="symptoms"></a>Oireet

Tämä ongelma voi esiintyä esimerkiksi yritettäessä määrittää varastokirjauskansion työnkulun ehtoa kustannuksen summan perusteella. Ehdon määrityksen mukaan vaihe 1 suoritetaan vain, kun kustannuksen summa on alle 100. Sen jälkeen toisen ehdon määrityksen mukaan vaihe 2 suoritetaan vain, kun kustannuksen summa on yhtä suuri tai suurempi kuin 100. Kun työnkulku sitten suoritetaan, työnkulkuhistoria näyttää vain yhden rivin ja ensimmäisen ehdon arviontina on aina *tosi* lähetetystä arvosta riippumatta.

## <a name="workaround"></a>Ongelman kiertäminen

Nykyisessä julkaisussa varastokirjauskansion työnkulun ehtoja käytetään vain kirjauskansiotasolla, ei rivitasolla. Tämä on suunniteltu ominaisuus. Ehdon ehdot kannattaa määrittää vain kirjauskansiotason määritteiden perusteella.
