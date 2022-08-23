---
title: Nimikkeet, joilla ei ole varastoa, voidaan kuitata ulos
description: Tämä artikkeli antaa vianmääritysohjeet, jotka voivat auttaa siinä, kun asiakkaat voivat lisätä varastosta loppuneita nimikkeitä ostoskoriin ja jatkaa kassalle.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.custom: ''
ms.assetid: ''
ms.search.industry: Retail
ms.openlocfilehash: 3bc924e44077886b942e19b25a84f0f1d4298c13
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9282731"
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
