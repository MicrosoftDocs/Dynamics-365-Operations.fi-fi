---
title: IoT-analyysi – aloitussivu
description: Tässä artikkelissa on linkkejä tietoihin IoT-analyysistä.
author: johanhoffmann
ms.date: 08/04/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.custom: intro-internal
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-04-25
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0d8b2be25abaeff7404d7f4ef3cd825a50147fef
ms.sourcegitcommit: e0905a3af85d8cdc24a22e0c041cb3a391c036cb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/06/2022
ms.locfileid: "9228354"
---
# <a name="iot-intelligence-home-page"></a>IoT-analyysi – aloitussivu

[!include [banner](../../includes/banner.md)]
[!INCLUDE [iot-sdi-announcement](../../includes/iot-sdi-announcement.md)]

> [!IMPORTANT]
> Tämä ominaisuus on tällä hetkellä käytettävissä vain seuraavissa maissa ja seuraavilla alueilla:
>
> - US (Amerikan Yhdysvallat)
> - EU (Euroopan unioni)
> - AU (Australia)
> - CA (Kanada)
> - UK (Yhdistynyt kuningaskunta)

IoT-analyysi on Microsoft Dynamics 365 Supply Chain Managementin lisäosa. Se integroi esineiden internetin (IoT) signaaleja Supply Chain Managementin tietoihin luodakseen toiminnallisia merkityksellisiä tietoja.

IoT-analyysi tukee seuraavia skenaarioita:

- **Tuotantoviiveet** – Tässä skenaariossa verrataan todellista jaksoaikaa suunniteltuun jaksoaikaan. Supply Chain Management ilmoittaa, kun tuotanto ei ole aikataulussa, jotta voit puuttua asiaan toimintatehokkuuden maksimoimiseksi ja tilausten viivästysten välttämiseksi.
- **Laitteiden käyttökatko** – Tässä skenaariossa verrataan mitattua toiminta-aikaa käyttäjän määrittämiin parametreihin. Supply Chain Management ilmoittaa, kun käyttökatkoraja ylitetään, jotta voit ryhtyä toimenpiteisiin, kuten tuotannon työtilauksen uudelleenajoittamiseen tai ylläpitotyötilauksen luomiseen.
- **Tuotteen laatu** – Tässä skenaariossa tunnistinlukemia, kuten kosteutta ja lämpötilaa, verrataan käyttäjän määrittämiin laatumittareihin. Supply Chain Management ilmoittaa ilmenevistä poikkeamista, jotta voit puuttua siihen laatustandardien ylläpitämiseksi ja hukan minimoimiseksi.

Seuraavassa kuvassa esitettään Azure IoT Hubin, IoT-analyysin ja Supply Chain Managementin yhteistoiminta.

![IoT Hub, IoT-analyysi, ja Supply Chain Management.](media/iot_intelligence.png)

<!-- KFM: hide setup info for now

## Setup

You can set up and configure IoT Intelligence without writing any code. Here are the basic steps.

1. [Set up Azure resources](iot-azure-setup.md) – Create an IoT hub, a Redis cache, and a key vault that can be accessed from Supply Chain Management.
2. [Message schema formats for IoT Hub](iot-schema-format.md) – Configure your devices to send messages to IoT Hub, and define the JavaScript Object Notation (JSON) message format.
3. In Feature Management, enable the IoT Intelligence feature flag. 
4. [Install the IoT Intelligence add-in in Microsoft Dynamics Lifecycle Services (LCS)](iot-lcs-setup.md) – Install the add-in in LCS, and configure the Azure secrets.
5. [Set up metrics](iot-metrics-setup.md) – Set up metrics in Supply Chain Management.
6. [Scenario setup](iot-scenario-setup.md) – Set up the scenarios in Supply Chain Management.

-->

## <a name="tracking-and-maintenance"></a>Jäljitys ja ylläpito

- [Skenaarioiden seuraaminen Dynamics 365 Supply Chain Managementissa](iot-management.md#monitor-scenarios)
- [Skenaarion poistaminen käytöstä](iot-scenario-setup.md#disable-a-scenario)
- [Meneillään olevan IoT-analytiikkaskenaarion muokkaaminen](iot-management.md#modify-a-running-iot-intelligence-scenario)
- [Simulointiasetukset](iot-management.md#simulation-options)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]