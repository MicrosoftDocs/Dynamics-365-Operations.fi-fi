---
title: Et voi vahvistaa lähetystä, koska asiakas on pidossa
description: Et voi vahvistaa lähetystä, koska asiakas on pidossa.
author: GalynaFedorova
ms.date: 07/30/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSShipConfirm,WHSLoadPlanningListPage_WHSShipConfirm,WHSLoadPlanningWorkbench_WHSShipConfirm,WHSTransportLoad_WHSShipConfirm,WHSShipPlanningListPage_WHSShipConfirm,WHSShipmentDetails_WHSShipConfirm,WHSWorkTable_WHSShipConfirm,WHSWorkTableListPage_WHSShipConfirm,Dialog_WHSOutboundShipConfirmController_WHSOutboundShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-07-30
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 801778fc8f04b106bf168a3dcd5a89767a837740
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/13/2021
ms.locfileid: "7344261"
---
# <a name="you-cant-confirm-a-shipment-because-the-customer-is-on-hold"></a>Et voi vahvistaa lähetystä, koska asiakas on pidossa

Virhekoodi: WAX:CustomerOnHoldShipmentCannotBeConfirmed

## <a name="symptoms"></a>Oireet

Kun yrität vahvistaa lähetyksen, järjestelmä näyttää seuraavan virhesanoman:

> Lähetystä %1 ei voitu vahvistaa, koska asiakas on pidossa kohteelle %2.

Et siis voi vahvistaa lähetystä kuormaa varten.

## <a name="cause"></a>Syy

Kuormituksen tai lähetyksen asiakastili on pidossa. Näin ollen asiakkaan tila estää lähetysvahvistuksen.

## <a name="resolution"></a>Ratkaisu

Seuraavia ohjeita noudattamalla voit poistaa asiakastilin eston.

1. Siirry kohtaan **Myyntireskontra \> Asiakkaat \> Kaikki asiakkaat**.
1. Avaa asiakastili, jota ei voi vahvistaa toimitukselle.
1. Määritä **Hyvitys ja perintä** -pikavälilehdellä **Pidossa oleva laskutus ja toimitus** -kentän arvoksi *Ei*.
1. Toista nämä vaiheet kaikille estetyille asiakkaille kuormaa varten.
