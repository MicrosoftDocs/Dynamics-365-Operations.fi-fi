---
title: Et voi vahvistaa lähetystä, koska määrä ylittää ylitoimitusprosentin.
description: Et voi vahvistaa lähetystä, koska määrä ylittää ylitoimitusprosentin.
author: perlynne
ms.date: 04/21/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSShipConfirm,WHSLoadPlanningListPage_WHSShipConfirm,WHSLoadPlanningWorkbench_WHSShipConfirm,WHSTransportLoad_WHSShipConfirm,WHSShipPlanningListPage_WHSShipConfirm,WHSShipmentDetails_WHSShipConfirm,WHSWorkTable_WHSShipConfirm,WHSWorkTableListPage_WHSShipConfirm,Dialog_WHSOutboundShipConfirmController_WHSOutboundShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: lbc
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: b25050572662afebbeaa39fa5a96e70cef618ac671dceba189fab1315480ede2
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6755152"
---
# <a name="you-cant-confirm-a-shipment-because-the-quantity-exceeds-the-overdelivery-percentage"></a>Et voi vahvistaa lähetystä, koska määrä ylittää ylitoimitusprosentin.

Virhekoodi: WAX1687

## <a name="symptoms"></a>Oireet

Kun yrität vahvistaa lähetyksen, järjestelmä näyttää seuraavan virhesanoman:

> Kuormituksen %1 lähetystä ei voitu vahvistaa, koska nimikkeen %2 määrä ylittää ylitoimitukselle määritetyn prosenttiosuuden.

Et siis voi vahvistaa lähetystä kuormaa varten.

## <a name="cause"></a>Syy

Kuormituksen tai lähetyksen määrä on kerätty vain osittain. Määrä ylittää tällä hetkellä kerätyn määrän prosenttiosuutena, joka on sallitun ylitoimitusprosentin ulkopuolella.

## <a name="resolution"></a>Ratkaisu

Voit korjata ongelman tekemällä yhden seuraavista toimista:

- Määritä kuormitusrivin määrä.
- Määritä ylitoimitusprosentti.

### <a name="set-the-load-line-quantity"></a>Määritä kuormitusrivin määrä

Voit määrittää kuormitusrivin määrän noudattamalla seuraavia vaiheita.

1. Siirry kohtaan **Varastonhallinta \> Kuormat \> Kaikki kuormat**.
1. Valitse kuormitus, jolle ei voi vahvistaa lähetystä.
1. Valitse **Kuormitusrivit**-pikavälilehdessä nimikkeelle kuormitusrivi, joka ylittää ylitoimitusprosentin.
1. Valitse **Rivin erittely** -pikavälilehdessä **Tilaus**.
1. Määritä **Määrä**-kentässä arvo kerätyksi määräksi (eli **Työn luontimäärä** -arvoksi), jotta lähetysvahvistus voi tapahtua.

### <a name="set-the-overdelivery-percentage"></a>Määritä ylitoimitusprosentti

Voit määrittää alitoimitusprosentin noudattamalla seuraavia vaiheita.

1. Siirry kohtaan **Varastonhallinta \> Kuormat \> Kaikki kuormat**.
1. Valitse kuormitus, jolle ei voi vahvistaa lähetystä.
1. Valitse **Kuormitusrivit**-pikavälilehdessä nimikkeelle kuormitusrivi, joka ylittää ylitoimitusprosentin.
1. Valitse **Rivin erittely** -pikavälilehdessä **Yleinen**.
1. Määritä **Ylitoimitus**-kentässä arvoksi suurempi prosenttiarvo, joka sopii kerättyyn määrään suhteessa kuormituksen määrään, jotta lähetysvahvistus voi tapahtua.
