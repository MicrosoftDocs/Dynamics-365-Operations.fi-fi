---
title: IoT-analytiikan seuranta ja hallinta
description: Tässä artikkelissa käsitellään IoT-analytiikan seurantaa ja hallintaa.
author: johanhoffmann
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: a640b523adac619377e19d670f932d4d85cfb6a9
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8852415"
---
# <a name="monitor-and-manage-iot-intelligence"></a>IoT-analytiikan seuranta ja hallinta

[!include [banner](../../includes/banner.md)]

Tässä artikkelissa käsitellään IoT-analytiikan seurantaa ja hallintaa.

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

Tehtaan laitteen signaaleja voi simuloida. Lisätietoja on seuraavissa artikkeleissa:

+ [IoT DevKit AZ3166:n yhdistäminen Azuren IoT-keskittimeen](/azure/iot-hub/iot-hub-arduino-iot-devkit-az3166-get-started)
+ [Raspberry Pi -verkkosimulaattorin yhdistäminen Azuren IoT-keskittimeen (Node.js)](/azure/iot-hub/iot-hub-raspberry-pi-web-simulator-get-started)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
