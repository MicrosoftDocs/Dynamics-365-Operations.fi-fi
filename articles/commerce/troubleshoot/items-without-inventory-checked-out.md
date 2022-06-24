---
title: Nimikkeet, joilla ei ole varastoa, voidaan kuitata ulos
description: Tämä artikkeli antaa vianmääritysohjeet, jotka voivat auttaa siinä, kun asiakkaat voivat lisätä varastosta loppuneita nimikkeitä ostoskoriin ja jatkaa kassalle.
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
ms.openlocfilehash: 24400953d2a17384be8ab3000aa829bf2bcb7192
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8877182"
---
# <a name="items-without-inventory-can-be-checked-out"></a>Nimikkeet, joilla ei ole varastoa, voidaan kuitata ulos

[!include [banner](../../includes/banner.md)]

Tämä artikkeli antaa vianmääritysohjeet, jotka voivat auttaa siinä, kun asiakkaat voivat lisätä varastosta loppuneita nimikkeitä ostoskoriin ja jatkaa kassalle.

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
