---
title: "\"Kohdeviitettä ei määritetty\" -virhe näkyy ostotilauksen vahvistuksen aikana"
description: "\"Kohdeviitettä ei määritetty\" -virhe näkyy ostotilauksen vahvistuksen aikana"
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 78e5e365f7197c1a0c25bf6eb63bcd5bd0f482ed
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476249"
---
# <a name="error-object-reference-not-set-occurs-during-purchase-order-confirmation"></a>"Kohdeviitettä ei määritetty" -virhe näkyy ostotilauksen vahvistuksen aikana

## <a name="symptoms"></a>Oireet

Seuraava poikkeus ilmenee, kun ostotilaus vahvistetaan:

> Objektiviitettä ei ole määritetty

## <a name="cause"></a>Syy

Tämä ongelma voi esiintyä, kun ostotilausten jaoissa on epäjohdonmukaisuuksia.

## <a name="resolution"></a>Ratkaisu

Voit poistaa tämän ongelman eston ja palauttaa ostotilauksen *Luonnos* siirtymällä kohtaan **Ostot ja hankinnat \> Säännölliset tehtävät \> Tyhjennys \> Ostotilauksen jaon palautus**. Lisä tietoja on seuraavassa blogikirjoituksessa: [Ostotilausten jakovirheiden korjaaminen Dynamics 365 Supply Chain Managementissa](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).
