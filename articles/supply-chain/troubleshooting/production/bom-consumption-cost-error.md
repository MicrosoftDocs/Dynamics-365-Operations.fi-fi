---
title: Tuoterakenteen consumptionCost-arvon virhe yritettäessä päättää tilausta
description: Kun tuotantotilausta yritetään päättää, saattaa ilmetä virhesanoma, jonka mukaan tuoterakenteen consumptionCost-arvon on oltava negatiivinen. Tämä ongelma on korjattu.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 737329d06022e899df8e4de5a27d76b21480da9e
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476235"
---
# <a name="cant-end-a-production-order-because-of-a-bom-consumptioncost-value-error"></a>Tuotantotilausta ei voi päättää tuoterakenteen consumptionCost-virheen vuoksi

## <a name="symptoms"></a>Oireet

Kun yrität päättää tuotantotilauksen, näyttöön tulee seuraava virhesanoma:

> Laskennallisen tuotantorakenteen consumptionCost-arvon on oltava negatiivinen, kun se otetaan varastosta.

## <a name="resolution"></a>Ratkaisu

Tämä ongelma korjattiin versiossa 10.0.15.
