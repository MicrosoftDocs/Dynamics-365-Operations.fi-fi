---
title: Tekstiä korvataan, kun nimike määritetään myyntitilausrivillä
description: Kun tuote määritetään myyntitilausrivillä, muokattu teksti korvataan vakiotekstillä. Muuta tekstiä rivin määrittämisen jälkeen äläkä sitä ennen.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 20239b9b0eecb355274e909a8b8b39450e468c7e
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476182"
---
# <a name="item-text-is-overwritten-when-a-product-is-configured-on-a-sales-order-line"></a>Nimikkeen teksti korvataan, kun tuote määritetään myyntitilausrivillä

## <a name="symptoms"></a>Oireet

Tämä ongelma esiintyy, kun luot myyntitilauksen rivin määritettävälle nimikkeelle ja muokkaat sitten nimikkeen tekstiä. Kun määrität nimikkeen ja valitset **OK**, teksti korvataan vakiotekstillä.

## <a name="resolution"></a>Ratkaisu

Tämä toiminta on tarkoituksellista. Tekstikenttä sisältää variantin nimen, joka täytetään vasta, kun rivi on määritetty. Tämän vuoksi tekstiä on muutettava vasta, kun rivi on määritetty, ei sitä ennen.
