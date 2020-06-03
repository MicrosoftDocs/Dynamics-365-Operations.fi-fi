---
title: IoT-analytiikan seuranta ja hallinta
description: Tässä ohjeaiheessa käsitellään IoT-analytiikan seurantaa ja hallintaa.
author: robinarh
manager: AnnBe
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: ''
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: ''
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 97a87b78a0178424f00e464262bb7f69e8a5b4a0
ms.sourcegitcommit: 261b70ea358b2c231e20f320ed8bd6adc1e7d715
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/19/2020
ms.locfileid: "3386508"
---
# <a name="monitor-and-manage-iot-intelligence"></a>IoT-analytiikan seuranta ja hallinta

[!include [banner](../../includes/banner.md)]

Tässä ohjeaiheessa käsitellään IoT-analytiikan seurantaa ja hallintaa.

## <a name="monitor-scenarios-in-microsoft-dynamics-365-supply-chain-management"></a><a id="monitor-scenarios"></a>Microsoft Dynamics 365 Supply Chain Managementin valvontaskenaariot

IoT-analytiikan käsittelyä voi seurata monessa paikassa:

+ **Moduulit \> Tuotannonhallinta \> Kyselyt ja raportit \> IoT-analytiikka \> Ilmoitukset** – ratkaisemattomia ilmoituksia sisältävän luettelon tarkasteleminen.
+ **Moduulit \> Tuotannonhallinta \> Kyselyt ja raportit \> IoT-analytiikka \> Suljetut ilmoitukset** – ratkaistut tai hylätyt ilmoitukset sisältävän luettelon tarkasteleminen.
+ **Moduulit \> Tuotannonhallinta \> Kyselyt ja raportit \> IoT-analytiikka \> Arvoavaimet** – **Resurssin tila** -aikasarjakaavioiden arvojen näyttäminen.
+ **Moduulit \> Tuotannonhallinta \> Tuotannonohjaus \> Resurssin tila** – tiettyjen mittarien seuranta **Määritä**-valintaikkunan avulla. Jos skenaario havaitsee poikkeuksen, ilmoitus näyttää poikkeuksen tiedot.
+ **Työtilat \> Tuotannon hallinta \> Ilmoitukset** – ratkaisemattomien ilmoitusten luettelon tarkasteleminen.

## <a name="modify-a-running-iot-intelligence-scenario"></a>Meneillään olevan IoT-analytiikkaskenaarion muokkaaminen

Meneillään olevaan skenaarioon voi tehdä seuraavat muutokset:

+ Uuden anturin rakennemäärityksen lisääminen.
+ Uusien signaalin tietoarvojen valitseminen.
+ Aiemmin luotujen signaalin tietoarvojen peruuttaminen.
+ Uuden signaalin tietoarvojen lisääminen ja yhdistäminen.
+ Raja-arvojen päivittäminen.

Seuraavat muutokset meneillään olevaan skenaarioon on kielletty:

+ Käyttöönotetun skenaarion parhaillaan käyttämien rakennemääritysten poistaminen tai muokkaaminen.
+ Käyttöönotetun skenaarion rakennepolkujen muuttaminen.

## <a name="simulation-options"></a>Simulointiasetukset

Tehtaan laitteen signaaleja voi simuloida. Lisätietoja on seuraavissa aiheissa:

+ [IoT DevKit AZ3166:n yhdistäminen Azuren IoT-keskittimeen](https://docs.microsoft.com/azure/iot-hub/iot-hub-arduino-iot-devkit-az3166-get-started)
+ [Raspberry Pi -verkkosimulaattorin yhdistäminen Azuren IoT-keskittimeen (Node.js)](https://docs.microsoft.com/azure/iot-hub/iot-hub-raspberry-pi-web-simulator-get-started)
+ [Laitesimulaatioratkaisun apuohjelman yleiskatsaus](https://docs.microsoft.com/azure/iot-accelerators/iot-accelerators-device-simulation-overview)
