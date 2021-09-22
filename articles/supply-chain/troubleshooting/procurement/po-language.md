---
title: Ostotilaukset eivät vastaa yrityksen kieliasetuksia
description: Osto tilauksen tuotenimi näkyy järjestelmän kielellä sen kielen sijaan, joka on määritetty sille yrityksellä, jossa ostotilaus on luotu.
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
ms.openlocfilehash: 4deec493b5480dc570ac82876243bc31a2ae87aa
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476217"
---
# <a name="purchase-orders-dont-reflect-the-language-settings-of-the-legal-entity"></a>Ostotilaukset eivät vastaa yrityksen kieliasetuksia


## <a name="symptoms"></a>Oireet

Osto tilauksen tuotenimi näkyy järjestelmän kielellä sen kielen sijaan, joka on määritetty sille yrityksellä, jossa ostotilaus on luotu.

## <a name="reproduce-the-issue"></a>Ongelman toistaminen

Seuraavassa esitetään yksi tapa ongelman toistamiseen.

1. Määritä järjestelmän kieleksi *EN-US* (Yhdysvaltojen englanti).
1. Varmista, että käytettävissä tuote, jossa kielet *EN-US* ja *DE* (saksa) ovat käytössä tuotenimen käännöksiä varten.
1. Muuta yrityksen kieleksi *DE*.
1. Luo siinä yrityksessä, jossa kieleksi on määritetty *DE*, tuotteen sisältävä ostotilaus.
1. Huomaa, että tuotteen nimi näkyy edelleen kielellä Yhdysvaltojen englanti (järjestelmän kieli).

## <a name="resolution"></a>Ratkaisu

Tämä on suunniteltu ominaisuus. Ostotilauksissa tuote näkyy aina järjestelmän kielellä. Ostotilauksen kieltä käytetään luotaessa vahvistuskirjauskansiota.
