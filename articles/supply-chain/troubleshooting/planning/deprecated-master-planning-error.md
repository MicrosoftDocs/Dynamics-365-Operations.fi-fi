---
title: Näyttöön tulee virheilmoitus, kun käytössä on sisäinen pääsuunnittelumoduuli
description: Saat virheilmoituksen suorittaessasi vanhentuneen sisäisen pääsuunnittelumoduulin.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: Dialog_ReqCalcScheduleItemTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 9c950292a4f43319d21a7deafdfb341b7bef15d8
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294066"
---
# <a name="you-receive-an-error-when-running-the-built-in-master-planning-engine"></a>Näyttöön tulee virheilmoitus, kun käytössä on sisäinen pääsuunnittelumoduuli

Virhekoodi: ReqCalcScheduleItemTablePlanningOptimizationFitError

## <a name="symptoms"></a>Oireet

Suorittaessasi vanhentuneen sisäisen pääsuunnittelumoduulin, saat seuraavan virheilmoituksen:

> Tämä virhesanoma avautuu, koska sisäistä suunnittelumoduulia käytettiin suunnittelun optimoinnin tukemissa skenaarioissa. Suunnittelun optimointiin kannattaa siirtyä nyt, sillä nykyinen sisäinen pääsuunnittelu vanhentuu. Huomaa, että pääsuunnittelun suorittaminen onnistui. Jos siirrossa on vahvat riippuvuudet odottaviin toimintoihin, voidaan pyytää poikkeusta sisäisen pääsuunnittelumoduulin käytön jatkamista varten. Aloita täyttämällä seuraava kyselylomake ja pyydä tarvittaessa poikkeus suunnittelun optimointiin siirtymisessä. [Suunnittelun optimoinnin siirto- ja poikkeuskyselylomake](https://go.microsoft.com/fwlink/?linkid=2144962)

## <a name="cause"></a>Syy

Jos suoritat suunnittelua etkä käytä tuotannon hallintatoimintoja, harkitse tuotannon optimointiin siirtymistä. Sisäinen pääsuunnittelumoduuli on vanhentunut. Jos haluat jatkaa käyttöä ilman, että saat virhesanoman, sinun on anottava Microsoftilta poikkeusta.

## <a name="resolution"></a>Ratkaisu

Lisätietoja siitä, miten siirryt suunnittelun optimointiin tai miten poikkeusta sovelletaan, jotta voit edelleen käyttää vanhentunutta sisäistä pääsuunnittelumoduulia, on kohdassa [Siirtyminen suunnittelun optimointiin pääsuunnittelua varten](/dynamics365/supply-chain/master-planning/new-master-planning-engine).
