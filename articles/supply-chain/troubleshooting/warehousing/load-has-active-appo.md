---
title: Lähetystä ei voi vahvistaa kalenterin ongelman vuoksi
description: Lähetystä ei voi vahvistaa kalenterin ongelman vuoksi
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
ms.openlocfilehash: f1fccd10d8867252f32b37c77f9a3bad54157bdd
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938464"
---
# <a name="you-cant-confirm-a-shipment-because-of-an-issue-with-the-calendar"></a>Lähetystä ei voi vahvistaa kalenterin ongelman vuoksi

Virhekoodi: TRX2716

## <a name="symptoms"></a>Oireet

Kun yrität vahvistaa lähetyksen, järjestelmä näyttää seuraavan virhesanoman:

> Kalenterityyppi %1 edellyttää tapaamisen %2 sisään- ja uloskuittausta.

Et siis voi vahvistaa lähetystä kuormaa varten.

## <a name="cause"></a>Syy

Kuormitusta varten on aktiivisia tapaamisia. On esimerkiksi sääntö, joka edellyttää kuljettajan sisäänkuittausta. Näin ollen kuorma on tilassa, jossa lähetysvahvistus epäonnistuu.

## <a name="resolution"></a>Ratkaisu

Kuormitukseen linkitettyihin aktiivisisiin tapaamisiin liittyvät ongelmat on selvitettävä ja korjattava.

1. Siirry kohtaan **Varastonhallinta \> Kuormat \> Kaikki kuormat**.
1. Valitse kuormitus, jolle ei voi vahvistaa lähetystä.
1. Valitse sitten toimintoruudussa **Kuljetus**-välilehden **Tapaamiset**-ryhmässä **Tapaamisen ajoittaminen**.
1. Noudata seuraavia ohjeita:

    - Varmista, että kuljettajan sisään- tai uloskuittaus on valmis.
    - Tee tapaaminen valmiiksi tai peruuta se.
    - Poista liittyvän tapaamissäännön **Kuljettajan sisäänkuittaus tarvitaan** -vaihtoehto käytöstä.
