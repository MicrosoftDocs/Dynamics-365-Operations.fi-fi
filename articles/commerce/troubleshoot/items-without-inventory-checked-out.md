---
title: Nimikkeet, joilla ei ole varastoa, voidaan kuitata ulos
description: Tämä ohjeaihe antaa vianmääritysohjeet, jotka voivat auttaa siinä, kun asiakkaat voivat lisätä varastosta loppuneita nimikkeitä ostoskoriin ja jatkaa kassalle.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 1458328056a3ace8e5600a4c2d188e05b66c8110acbe44c869294a6b6e251e84
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6753691"
---
# <a name="items-without-inventory-can-be-checked-out"></a>Nimikkeet, joilla ei ole varastoa, voidaan kuitata ulos

[!include [banner](../../includes/banner.md)]

Tämä ohjeaihe antaa vianmääritysohjeet, jotka voivat auttaa siinä, kun asiakkaat voivat lisätä varastosta loppuneita nimikkeitä ostoskoriin ja jatkaa kassalle.

## <a name="description"></a>kuvaus

Käyttäjät voivat lisätä nimikkeen ostoskoriin, vaikka myymälässä ei olisikaan käytettävissä varastoa, ja jatkaa sitten kassasivulle.

## <a name="resolution"></a>Ratkaisu

### <a name="enable-the-show-out-of-stock-errors-property-in-commerce-site-builder"></a>Näytä loppu varastosta -virhe ominaisuuden ottaminen käyttöön Commercen sivuston luontiohjelmassa

Ota **Näytä loppu varastosta -virhe** -ominaisuus käyttöön Commercen sivuston luontiohjelmassa seuraavasti.

1. Valitse sivusto, jota käsittelet.
1. Valitse vasemmanpuoleisessa siirtymisruudussa kohtaan **Sivut**.
1. Avaa **CartPage** valitsemalla.
1. Valitse **Cart 1** -paikka, valitse **Muokkaa** ja valitse sitten ominaisuusruudusta **Näytä loppu varastosta -virhe** -valintaruutu.
1. Tallenna ja julkaise sivu.

## <a name="additional-resources"></a>Lisäresurssit

[Varastoasetusten käyttäminen](../inventory-settings.md)

[Vähittäismyyntikanavien varaston käytettävyyden laskeminen](../calculated-inventory-retail-channels.md)

[Varastopuskureiden ja varastotasojen konfiguroiminen](../inventory-buffers-levels.md)
