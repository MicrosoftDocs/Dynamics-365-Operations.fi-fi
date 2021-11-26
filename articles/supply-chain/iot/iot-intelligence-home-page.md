---
title: IoT-analyysi – aloitussivu
description: Tässä aiheessa on linkkejä tietoihin IoT-analyysistä.
author: tonyafehr
ms.date: 12/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: tfehr
ms.custom: intro-internal
ms.search.region: Global
ms.author: tfehr
ms.search.validFrom: 2020-04-25
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6b6c179052cdb9d1ca808d9cba089163bde0d5d5
ms.sourcegitcommit: 9acfb9ddba9582751f53501b82a7e9e60702a613
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/10/2021
ms.locfileid: "7782678"
---
# <a name="iot-intelligence-home-page"></a>IoT-analyysi – aloitussivu

[!include [banner](../../includes/banner.md)]

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

+ **Tuotantoviiveet** – Tässä skenaariossa verrataan todellista jaksoaikaa suunniteltuun jaksoaikaan. Supply Chain Management ilmoittaa, kun tuotanto ei ole aikataulussa, jotta voit puuttua asiaan toimintatehokkuuden maksimoimiseksi ja tilausten viivästysten välttämiseksi.
+ **Laitteiden käyttökatko** – Tässä skenaariossa verrataan mitattua toiminta-aikaa käyttäjän määrittämiin parametreihin. Supply Chain Management ilmoittaa, kun käyttökatkoraja ylitetään, jotta voit ryhtyä toimenpiteisiin, kuten tuotannon työtilauksen uudelleenajoittamiseen tai ylläpitotyötilauksen luomiseen.
+ **Tuotteen laatu** – Tässä skenaariossa tunnistinlukemia, kuten kosteutta ja lämpötilaa, verrataan käyttäjän määrittämiin laatumittareihin. Supply Chain Management ilmoittaa ilmenevistä poikkeamista, jotta voit puuttua siihen laatustandardien ylläpitämiseksi ja hukan minimoimiseksi.

Seuraavassa kuvassa esitettään Azure IoT Hubin, IoT-analyysin ja Supply Chain Managementin yhteistoiminta.

![IoT Hub, IoT-analyysi, ja Supply Chain Management.](media/iot_intelligence.png)

## <a name="setup"></a>Asetusten määrittäminen

Voit määrittää IoT-analyysin ilman koodin kirjoittamista. Seuraavassa on perusvaiheet.

1. [Azure-resurssien määrittäminen](iot-azure-setup.md) – Luo IoT Hub, Redis-välimuisti ja avainsäilö, joita voi käyttää Supply Chain Managementista.
2. [IoT Hubin sanomarakenteen muodot](iot-schema-format.md) – Määritä laitteesi lähettämään sanomia IoT Hubille ja määritä JavaScript Object Notationin (JSON) sanomamuoto.
3. Ota ominaisuuksienhallinnassa käyttöön IoT-analyysin toimintomerkintä. 
4. [Asenna IoT-analyysin lisäosa Microsoft Dynamics Lifecycle Servicesiin (LCS)](iot-lcs-setup.md) – Asenna lisäosa LCS:ään ja määritä Azuren salaiset koodit.
5. [Mittareiden määrittäminen](iot-metrics-setup.md) – Määritä mittareita Supply Chain Managementissa.
6. [Skenaarion määritys](iot-scenario-setup.md) – Määritä skenaariot Supply Chain Managementissa.

## <a name="tracking-and-maintenance"></a>Jäljitys ja ylläpito

+ [Skenaarioiden seuraaminen Dynamics 365 Supply Chain Managementissa](iot-management.md#monitor-scenarios)
+ [Skenaarion poistaminen käytöstä](iot-scenario-setup.md#disable-a-scenario)
+ [Lisäosan asennuksen poistaminen](iot-lcs-setup.md#uninstall-addin)
+ [Meneillään olevan IoT-analytiikkaskenaarion muokkaaminen](iot-management.md#modify-a-running-iot-intelligence-scenario)
+ [Simulointiasetukset](iot-management.md#simulation-options)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]