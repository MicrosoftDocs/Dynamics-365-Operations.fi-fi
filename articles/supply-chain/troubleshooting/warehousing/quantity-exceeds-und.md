---
title: Et voi vahvistaa lähetystä, koska määrä ylittää alitoimitusprosentin.
description: Et voi vahvistaa lähetystä, koska määrä ylittää alitoimitusprosentin.
author: perlynne
ms.date: 04/21/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSShipConfirm,WHSLoadPlanningListPage_WHSShipConfirm,WHSLoadPlanningWorkbench_WHSShipConfirm,WHSTransportLoad_WHSShipConfirm,WHSShipPlanningListPage_WHSShipConfirm,WHSShipmentDetails_WHSShipConfirm,WHSWorkTable_WHSShipConfirm,WHSWorkTableListPage_WHSShipConfirm,Dialog_WHSOutboundShipConfirmController_WHSOutboundShipConfirm,WHSContainerCloseDiag_WHSShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: lbc
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: a6a5b1140d1bc5d09a1bc582fb1d2ac9446fae0920cbb9957797dbdea4c684e6
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6760319"
---
# <a name="you-cant-confirm-a-shipment-because-the-quantity-exceeds-the-underdelivery-percentage"></a>Et voi vahvistaa lähetystä, koska määrä ylittää alitoimitusprosentin.

Virhekoodi: WAX1686

## <a name="symptoms"></a>Oireet

Kun yrität vahvistaa lähetyksen, järjestelmä näyttää seuraavan virhesanoman:

> Kuormituksen %1 lähetystä ei voitu vahvistaa, koska nimikkeen %2 määrä ylittää alitoimitukselle määritetyn prosenttiosuuden.

Et siis voi vahvistaa lähetystä kuormaa varten.

## <a name="cause"></a>Syy

Kuormituksen tai lähetyksen määrä on kerätty vain osittain. Määrä alittaa tällä hetkellä kerätyn määrän prosenttiosuutena, joka on sallitun alitoimitusprosentin ulkopuolella.

## <a name="resolution"></a>Ratkaisu

Voit korjata ongelman tekemällä yhden seuraavista toimista:

- Määritä kuormitusrivin määrä.
- Määritä alitoimitusprosentti.

### <a name="set-the-load-line-quantity"></a>Määritä kuormitusrivin määrä

Voit määrittää kuormitusrivin määrän noudattamalla seuraavia vaiheita.

1. Siirry kohtaan **Varastonhallinta \> Kuormat \> Kaikki kuormat**.
1. Valitse kuormitus, jolle ei voi vahvistaa lähetystä.
1. Valitse **Kuormitusrivit**-pikavälilehdessä nimikkeelle kuormitusrivi, joka ylittää alitoimitusprosentin.
1. Valitse **Rivin erittely** -pikavälilehdessä **Tilaus**.
1. Määritä **Määrä**-kentässä arvo kerätyksi määräksi (eli **Työn luontimäärä** -arvoksi), jotta lähetysvahvistus voi tapahtua.

### <a name="set-the-underdelivery-percentage"></a>Määritä alitoimitusprosentti

Voit määrittää alitoimitusprosentin noudattamalla seuraavia vaiheita.

1. Siirry kohtaan **Varastonhallinta \> Kuormat \> Kaikki kuormat**.
1. Valitse kuormitus, jolle ei voi vahvistaa lähetystä.
1. Valitse **Kuormitusrivit**-pikavälilehdessä nimikkeelle kuormitusrivi, joka ylittää alitoimitusprosentin.
1. Valitse **Rivin erittely** -pikavälilehdessä **Yleinen**.
1. Määritä **Alitoimitus**-kentässä arvoksi suurempi prosenttiarvo, joka sopii kerättyyn määrään suhteessa kuormituksen määrään, jotta lähetysvahvistus voi tapahtua.
