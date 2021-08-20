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
ms.openlocfilehash: 7c0c674818a21d3ad422661fc427b0b9c4aad52b8d44d08791d2d703be528fe3
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6751718"
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
