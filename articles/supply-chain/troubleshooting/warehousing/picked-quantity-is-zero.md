---
title: Et voi vahvistaa lähetystä, koska määrä on nolla.
description: Et voi vahvistaa lähetystä, koska määrä on nolla.
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
ms.openlocfilehash: b2f9f8deaca30e318d0393fb1d7911eebf63060ccca83dc6f1de9b04b9e30e11
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6712883"
---
# <a name="you-cant-confirm-a-shipment-because-there-is-zero-quantity"></a>Et voi vahvistaa lähetystä, koska määrä on nolla.

Virhekoodi: LoadLineWarningUpdatedToZero

## <a name="symptoms"></a>Oireet

Kun yrität vahvistaa lähetyksen, järjestelmä näyttää seuraavan virhesanoman:

> Nimikkeen %1 ja lähetyksen %2 kuormariville on päivitetty nollamäärä, koska alitoimituksen asetukset sallivat, ettei tämän nimikkeen määriä lähetetä.

Et siis voi vahvistaa lähetystä kuormaa varten.

## <a name="cause"></a>Syy

Järjestelmä arvioi, onko kerätty määrä odotettujen rajojen sisällä kerätyn määrän, kuormitusrivin määrän ja alitoimitusprosentin perusteella. Jos järjestelmä havaitsee, että kerätty määrä kuormitusrivillä on 0 (nolla), lähetystä ei voi vahvistaa. Tämä ongelma voi ilmetä esimerkiksi, jos työ on peruutettu ja kuormitusrivin alitoimitusprosentti on 100 prosenttia.

## <a name="resolution"></a>Ratkaisu

Tarkista kuormitusrivit ja varmista, että alitoimitusprosentti ja määrät ovat suhteessa kerättyyn työhön.

1. Siirry kohtaan **Varastonhallinta \> Kuormat \> Kaikki kuormat**.
1. Valitse kuormitus, jolle ei voi vahvistaa lähetystä.
1. Valitse **Kuormitusrivit**-pikavälilehdessä nimikkeelle kuormitusrivi, joka ylittää alitoimitusprosentin.
1. Muuta tarvittaessa **Alitoimitus**-kentän tai **Määrä**-kentän arvoa.

> [!TIP]
> Jos ongelmaa ei ole vielä korjattu, liittyvien myyntitilausten tai siirtotilausten keräystöitä on ehkä vielä jatkettava, kunnes käytettävissä oleva määrä on kohdistettu kuormituksen tai lähetyksen kanssa.
