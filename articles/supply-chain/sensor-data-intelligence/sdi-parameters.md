---
title: Sensor Data Intelligencen parametrit
description: Tässä artikkelissa on tietoja määritysasetuksista, jotka ovat käytettävissä Sensor Data Intelligencen parametrit -sivulla.
author: johanhoffmann
ms.date: 09/02/2022
ms.topic: article
ms.search.form: IoTIntCoreServiceParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-09-02
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: 5240537e3a6526ceb35253b9e68f46b1753c6a37
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/18/2022
ms.locfileid: "9689370"
---
# <a name="sensor-data-intelligence-parameters"></a>Sensor Data Intelligencen parametrit

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!-- KFM: Preview until further notice -->

**Sensor Data Intelligencen parametrit** -sivulla näkyvät muutamat asetukset, joiden avulla voit määrittää ominaisuuden. Nämä asetukset sisältävät Azure-yhteyden parametrit ja parametrin käyttäjälle tunnistimien mittausarvojen vastauksena lähetettävien hälytyssanomien eliniälle.

## <a name="read-and-change-connection-details-for-your-azure-iot-solution"></a>Azure IoT -ratkaisun yhteystietojen lukeminen ja muuttaminen

Yleensä Azure IoT -ratkaisu määritetään ja yhteys siitä muodostetaan Microsoft Dynamics 365 Supply Chain Managementiin **Ota Azure-resurssit käyttöön ja muodosta niihin yhteys** -sivulla. Sivulla on ohjeita molempiin menettelytapoihin. (Lisätietoja on kohdassa [IoT-ratkaisun käyttöönotto Azuressa](sdi-deploy-iot-solution-on-azure.md).) Voit tarkastella ja muokata yhteystietoja milloin tahansa Supply Chain Managementissa alla olevien vaiheiden avulla.

1. Siirry kohtaan **Järjestelmän hallinta \> Asetukset \> Sensor Data Intelligence \> Sensor Data Intelligencen parametrit**.
1. Syötä **Aikasarja**-välilehden **Redis-mittarin säilön yhteysmerkkijono** -kenttään **Ensisijainen yhteysmerkkijono(StackExchange.Redis)** -arvo Azure IoT -ratkaisulle, johon haluat muodostaa yhteyden. Lisätietoja tämän arvon löytämisestä on kohdassa [IoT-ratkaisun käyttöönotto Azuressa](sdi-deploy-iot-solution-on-azure.md).
1. Syötä **Integroinnit**-välilehden **Azure AD -sovelluksen asiakasohjelman tunnus** -kenttään **Asiakasohjelman tunnus** -arvo sille Azure IoT -ratkaisulle, johon haluat muodostaa yhteyden. Lisätietoja tämän arvon löytämisestä on kohdassa [IoT-ratkaisun käyttöönotto Azuressa](sdi-deploy-iot-solution-on-azure.md).

## <a name="set-the-lifetime-of-alert-messages"></a>Hälytyssanomien elinkaaren määritys

Aina, kun Sensor Data Intelligence havaitsee tilanteen, jossa tarvitaan käyttäjän toimia, se lähettää ilmoituksen kyseiselle käyttäjälle. Jos haluat estää näitä ilmoituksia kasaantumasta järjestelmään, määritä, että ilmoitukset vanhenevat muutaman päivän kuluttua.

1. Siirry kohtaan **Järjestelmän hallinta \> Asetukset \> Sensor Data Intelligence \> Sensor Data Intelligencen parametrit**.
1. Syötä **Ilmoitukset**-välilehden **Käytettävät ilmoittamispäivät** -kenttään niiden päivien määrä, joiden ajan ilmoitus säilytetään. Kun määritetty aika on kulunut, ilmoitus poistetaan.
