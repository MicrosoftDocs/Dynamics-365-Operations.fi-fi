---
title: Sekoittuneita varastotyyppejä käytettäessä lähetys- ja vastaanottoalueen hallintaprofiilia
description: Jotta lähetys- ja vastaanottoalueen hallintaprofiili voisi hallita varastojen sekoittamista, on ensin määritettävä työotsikon vaihto. Tällä sivulla kerrotaan, miten se tehdään.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: cc660a2f9839e886240c97a7f60d2e264653074a
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476212"
---
# <a name="inventory-types-are-being-mixed-when-using-a-dock-management-profile"></a>Varastotyypit sekoittuvat käytettäessä lähetys- ja vastaanottoalueen hallintaprofiilia

## <a name="symptoms"></a>Oireet

Käytät *lähetyksen konsolidoinnin käytäntöjä*. Olet määrittänyt *lähetys- ja vastaanottoalueen hallintaprofiilin* *sijaintiprofiilille*, mutta kun töitä luodaan, lopullisessa sijainnissa on erilaisia varastotyyppejä.

## <a name="resolution"></a>Ratkaisu

Lähetys- ja vastaanottoalueen hallintaprofiilit edellyttävät, että työt jaetaan etukäteen. Toisin sanoen lähetys- ja vastaanottoalueen hallintaprofiili odottaa, että työotsikolla ei ole useita asetussijainteja.

Jotta lähetys- ja vastaanottoalueen hallintaprofiili voisi hallita varastojen sekoittamista, on määritettävä työotsikon vaihto.

Tässä esimerkissä lähetys- ja vastaanottoalueen hallintaprofiili on määritetty siten, että **varastotyypit, joita ei pidä sekoittaa** on määritetty arvoon *Lähetystunnus*. Sitä varten määritetään työotsikon vaihto:

1. Siirry kohtaan **Varastonhallinta \> Asetukset \> Työ \> Työmallit**.
1. Valitse muokattava **Työtilauksen tyyppi** (kuten *Ostotilaukset*).
1. Valitse muokattava työmalli.
1. Valitse toimintoruudussa **Muokkaa kyselyä**.
1. Avaa **Lajittelu**-välilehti ja lisää rivi seuraavin asetuksin:
    - **Taulukko** - *Väliaikaiset työtapahtumat*
    - **Johdettu taulukko** - *Väliaikaiset työtapahtumat*
    - **Kenttä** - *Lähetystunnus*
1. Valitse **OK**.
1. Palaat **Työmallit**-sivulle. Valitse toimintoruudussa **Työn otsikoiden katkaisut**.
1. Valitse toimintoruudussa **Muokkaa**.
1. Valitse **Kenttänimeen** *Lähetystunnus* yhdistetty valintaruutu.
1. Valitse toimintoruudussa **Tallenna**.
