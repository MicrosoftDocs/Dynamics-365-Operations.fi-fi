---
title: Lähetystä ei voi vahvistaa keskeneräisen tai puuttuvan työn vuoksi
description: Lähetystä ei voi vahvistaa keskeneräisen tai puuttuvan työn vuoksi
author: perlynne
ms.date: 04/21/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSShipConfirm,WHSLoadPlanningListPage_WHSShipConfirm,WHSLoadPlanningWorkbench_WHSShipConfirm,WHSTransportLoad_WHSShipConfirm,WHSShipPlanningListPage_WHSShipConfirm,WHSShipmentDetails_WHSShipConfirm,WHSWorkTable_WHSShipConfirm,WHSWorkTableListPage_WHSShipConfirm,Dialog_WHSOutboundShipConfirmController_WHSOutboundShipConfirm, WHSContainerCloseDiag_WHSShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: lbc
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 59def4427f9fff32fd3839bb9f9b5d5cccdc7720f92a84f1af3adad596d8b352
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6730055"
---
# <a name="you-cant-confirm-a-shipment-because-of-incomplete-or-missing-work"></a>Lähetystä ei voi vahvistaa keskeneräisen tai puuttuvan työn vuoksi

Virhekoodi: WAX515

## <a name="symptoms"></a>Oireet

Kun yrität vahvistaa lähetyksen, järjestelmä näyttää seuraavan virhesanoman:

> Kuorman %1 lähetystä ei voitu vahvistaa, koska kuorman kaiken työn on oltava valmis.

Et siis voi vahvistaa lähetystä kuormaa varten.

## <a name="cause"></a>Syy

Kuorma tai lähetys on tilassa, jossa lähetysvahvistus epäonnistuu. Ennen lähetyksen vahvistusta kuormitukselle on oltava tehtynä edes vähän työtä, ja työn tilan on oltava *Suljettu* tai *Peruutettu*.

## <a name="resolution"></a>Ratkaisu

Tarkista kuormitukseen tai lähetykseen liittyvät myyntitilaukset tai siirtotilaukset ja varmista, että kaikki asiaan liittyvät työt on tehty tai peruutettu.

Voit käyttää lähetyksiä ja kuormituksia useilla sivuilla. Seuraavissa aliosissa on esimerkkejä.

### <a name="all-loads-page"></a>Kaikki kuormat -sivu

1. Siirry kohtaan **Varastonhallinta \> Kuormat \> Kaikki kuormat**.
1. Valitse kuormitus, jolle ei voi vahvistaa lähetystä.
1. Valitse toimintoruudun **Kuormat**-välilehden **Aiheeseen liittyvät tiedot**-ryhmässä **Työ**.
1. Tarkista kunkin työtunnuksen tila. Seuraa jokaista työtunnusta, jonka tilana ei ole *Suljettu* tai *Peruutettu*.
1. Kun jokaisen työtunnuksen tila on *Suljettu* tai *Peruutettu*, vahvista lähetys uudelleen.

### <a name="all-shipments-page"></a>Kaikki lähetykset -sivu

1. Valitse **Varastonhallinta \> Lähetykset \> Kaikki lähetykset**.
1. Valitse lähetys, jota ei voi vahvistaa.
1. Valitse toimintoruudun **Lähetykset**-välilehden **Työ**-ryhmässä **Työn tiedot**.
1. Tarkista kunkin työtunnuksen tila. Seuraa jokaista työtunnusta, jonka tilana ei ole *Suljettu* tai *Peruutettu*.
1. Kun jokaisen työtunnuksen tila on *Suljettu* tai *Peruutettu*, vahvista lähetys uudelleen.

### <a name="all-work-page"></a>Kaikki työt -sivut

1. Valitse **Varastonhallinta \> Työ\> Kaikki työt**.
1. Valitse sen tilausnumeron työ, jonka lähetystä ei voi vahvistaa.
1. Valitse toimintoruudun **Lähetys** -välilehden **Lähetys**-ryhmässä **Vahvista lähetys**.
1. Tarkista kunkin työtunnuksen tila. Seuraa jokaista työtunnusta, jonka tilana ei ole *Suljettu* tai *Peruutettu*.
1. Kun jokaisen työtunnuksen tila on *Suljettu* tai *Peruutettu*, vahvista lähetys uudelleen.
