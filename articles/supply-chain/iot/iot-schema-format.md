---
title: IoT Hub -sanomien sanaomarakenteen muodot
description: Tässä aiheessa kuvataan, miten kannattaa suunnitella IoT-analyysissä käytettäväksi soveltuva sanomarakenne.
author: robinarh
ms.date: 04/25/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2020-04-25
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5ecf4a70d69d24ea75f5448339057e7017cb93af
ms.sourcegitcommit: 614d79cba238e466d445767a7d0a012e785a9861
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/19/2021
ms.locfileid: "7651982"
---
# <a name="schema-formats-for-iot-hub-messages"></a>IoT Hub -sanomien sanaomarakenteen muodot

[!include [banner](../../includes/banner.md)]

Tässä aiheessa kuvataan, miten kannattaa suunnitella IoT-analyysissä käytettäväksi soveltuva sanomarakenne.

## <a name="message-requirements"></a>Sanomavaatimukset

Seuraavat säännöt koskevat sanomien valvontaa IoT-analyysissä:

+ Sanomarakenteiden on oltava JavaScript Object Notation (JSON) muodossa.
+ Microsoft Azure IoT -keskittemen sanomassa on oltava UNIX-**aikaleima**-ominaisuus, jossa arvo ilmaistaan millisekunteina (ms).
+ Sanomaa seurataan vain, jos se sisältää kaikki skenaarion asetuksissa määritetyt ominaisuudet. Jos esimerkiksi määrität ominaisuudet **tunnus**, **aikaleima** ja **arvo** ominaisuudet, seurataan seuraavaa sanomaa.

    ```json
    {
        "id": "IoTInt.Machine1225.PartOut",
        "timestamp": 1576016821614,
        "value": True
    }
    ```

    Tätä sanomaa ei valvota, koska **arvo**-ominaisuus puuttuu.

    ```json
    {
        "id": "IoTInt.Machine1225.PartOut",
        "timestamp": 1576016821614,
    }
    ```

+ IoT-analyysi ohittaa sanoman ominaisuudet, joita ei ole määritetty skenaarion määrityksessä. Jos esimerkiksi määrität ominaisuudet **tunnus**, **aikaleima** ja **arvo** ominaisuudet, IoT-analyysi seuraa kaikkia seuraavia sanomia.

    ```json
    {
        "id": "IoTInt.Machine1225.PartOut",
        "timestamp": 1576016821614,
        "value": True
    },
    {
        "id": "IoTInt.Machine1225.PartOut",
        "timestamp": 1576016821614,
        "value": True,
        "machine" : "Machine1225",
    },
    {
        "id": "IoTInt.Machine1225.PartOut",
        "timestamp": 1576016821614,
        "value": True,
         "activity": "PartOut"
    },
    ```

+ IoT-analyysi ohittaa hiljaisesti sanomat, jotka eivät vastaa skenaarion määrityskriteerejä.
+ Voit määrittää ja käyttää useanlaisia viestirakenteita.
+ Kaikkia sanomarakenteen tyyppejä ei tarvise määrittää. Vain IoT-analyysin skenaariossa käytettävät rakenteet on määritettävä.

## <a name="id-value-pair-schema"></a>Tunnusarvon parirakenne

Tunnusarvopari on yleinen IoT-analyysin sanomarakenteiden malli. Kun käytät tunnusarvoparia, varmistat, että sanomarakenteesi on sama kaikissa skenaarioissa. Tässä esimerkiksi on sanoma **Laitteen käyttökatko**- tai **Tuotantoviive**-skenaariolle.

```json
{
    "id": "IoTInt.Machine1225.PartOut",
    "timestamp": 1576016821614,
    "value": True
}
```

Tässä on sanoma **Tuotteen laatu** -skenaariota varten.

```json
{
    "id": "IoTInt.Machine1225.Temperature",
    "timestamp": 1576016821614,
    "value": 105
}
```

Molemmat edeltävät sanomat sisältävät ominaisuudet **tunnus** ja **arvo**. **Tunnus**-arvoille voidaan tehdä skenaarion määrittämisen aikana yhdistelmämääritys **Signaalitietoarvot**-tauluun. **Laitteiden käyttökatkot** -skenaariota varten suoritat yhdistämismäärityksen arvolle **IoTInt.Machine1225.PartOut.** **Tuotteen laatu** -skenaariota varten suoritat yhdistämismäärityksen arvolle **IoTInt.Machine1225.Temperature.**

Lisätietoja on kohdassa [Azure IoT Hub ohjeet](/azure/iot-hub/).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]