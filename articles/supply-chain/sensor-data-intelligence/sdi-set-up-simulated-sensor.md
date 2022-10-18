---
title: Simuloidun tunnistiminen määrittäminen testaamista varten
description: Tässä artikkelissa kerrotaan, miten simulaattori määritetään Sensor Data Intelligencen testaamista varten ilman fyysisten tunnistimien asentamista.
author: johanhoffmann
ms.date: 09/02/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-09-02
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: dc8bd020a53214abab28ec51ffc6d6be74979932
ms.sourcegitcommit: c5f2cba3c2b0758e536eeaaa40506659a53085e1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/12/2022
ms.locfileid: "9643973"
---
# <a name="set-up-a-simulated-sensor-for-testing"></a>Simuloidun tunnistiminen määrittäminen testaamista varten

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

Jos haluat testata Sensor Data Intelligencen ilman fyysisten tunnistimien asentamista, voit käyttää *Raspberry PI Azure IoT -verkkosimulaattori* -palvelua tunnistimien signaalien emuloimiseksi ja lähettämiseksi Microsoft Azuren esineiden internet (IoT) -ratkaisulle. Lisätietoja simulaattorista on kohdassa [Raspberry Pi -verkkosimulaattorin yhdistäminen Azure IoT -keskittimeen (Node.js)](/azure/iot-hub/iot-hub-raspberry-pi-web-simulator-get-started).

## <a name="video-instructions"></a>Video-ohjeet

Seuraavassa videossa on tietoja simuloidun anturin määrittämistä testaamista varten. Tämän artikkelin jäljellä olevissa osissa on samat ohjeet tekstimuodossa.

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE588g6]

## <a name="create-a-device-in-azure-iot-hub"></a>Laitteen luominen Azure IoT -keskittimessä

Määritä ensin laite tunnistimen signaalien todentamiseksi Azure IoT -keskittimessä.

1. Siirry Azuressa sen resurssiryhmän resurssiluetteloon, joka luotiin Sensor Data Intelligencen kanssa käytettäväksi. (Lisätietoja on kohdassa [IoT-ratkaisun käyttöönotto Azuressa](sdi-deploy-iot-solution-on-azure.md).)
1. Etsi resurssiluettelossa tietue, jonka **Tyyppi**-kentän arvoksi on määritetty *IoT-keskitin*. Valitse **Nimi**-sarakkeessa nimi, jotta resurssin tietosivu avautuu.
1. Valitse vasemmassa siirtymisruudussa **Laitteet**.
1. Valitse **Laitteet**-sivulla **Lisää laite**.
1. Määritä **Luo laite** -sivulla seuraavat kentät:

    - **Laitteen tunnus** – Syötä uuden laitteen nimi (esimerkiksi *Oma-IoT-laite*).
    - **Todennustyyppi** – Valitse *Symmetriset avaimet*.
    - **Luo avaimet automaattisesti** – Valitse tämä valintaruutu.
    - **Muodosta yhteys tästä laitteesta IoT-keskittimeen** – Valitse *Ota käyttöön*.

1. Valitse **Tallenna**, jos haluat palata **Laitteet**-sivulle.
1. Etsi uusi laite luettelosta. Valitse **Laitteen tunnus** -sarakkeessa nimi, jotta laitteen tietosivu avautuu. Jos luettelossa ei ole uutta laitetta, päivitä sivu.
1. Kopioi **ensisijaisen yhteysmerkkijonon** arvo (esimerkiksi valitsemalla **Kopioi leikepöydälle** -painike). Tätä arvoa tarvitaan myöhemmin määritettäessä Raspberry Pi IoT -simulaattori tunnistimen signaalien emuloimisessa. Tämän vuoksi arvo kannattaa tässä vaiheessa liittää tekstitiedostoon.

## <a name="add-the-azure-connection-string-to-the-raspberry-pi-iot-simulator"></a>Azure-yhteysmerkkijonon lisääminen Raspberry Pi IoT -simulaattoriin

Alla olevien vaiheiden avulla voit lisätä yhteysmerkkijonon Azure IoT -keskittimen laitteesta Raspberry-palvelun komentosarjaan.

1. Avaa [Raspberry Pi IoT -simulaattori](https://azure-samples.github.io/raspberry-pi-web-simulator/).
1. Etsi koodieditorin ruudusta rivi, joka sisältää seuraavan komennon.

    `const connectionString = '[Your IoT hub device connection string]';`

1. Korvaa ohjeteksti, myös hakasulkeet, edellisessä osassa kopioidulla **ensisijaisen yhteysmerkkijonon** arvolla. Tuloksen pitäisi muistuttaa seuraavaa esimerkkiä:

    `const connectionString = 'HostName=XXX;DeviceId=YYY;SharedAccessKey=ZZZ';`

## <a name="add-sensor-ids-and-values-to-the-payload-in-the-raspberry-pi-iot-simulator"></a>Lisää tunnistimen tunnukset ja arvot Raspberry Pi IoT -simulaattorin tietoihin

Määritä nyt Raspberry Pi IoT -simulaattorissa simuloidut tunnistimet ja arvot niin, että ne lähetetään tietoina.

- Etsi Raspberry Pi IoT -simulaattorin koodieditorissa funktio `getMessage` ja muokkaa sitä niin, että se vastaa seuraavaa koodia. (Tunnistimet määritetään riveillä `cb()`.)

    ```cpp
    function getMessage(cb) {
        messageId++;
        sensor.readSensorData()
        .then(function (data) {
            cb(JSON.stringify({ value: 1, sensorId: 'MachineStatus' }), false);
            cb(JSON.stringify({ value: 70, sensorId: 'Quality' }), false);
            cb(JSON.stringify({ value: 1, sensorId: 'AssetMaintenance' }), false);
            cb(JSON.stringify({ value: 1, sensorId: 'ProductionDelay' }), false);
            cb(JSON.stringify({ value: 20, sensorId: 'AssetDowntime' }), false);
        })
        .catch(function (err) {
            console.error('Failed to read out sensor data: ' + err);
        });
    }
    ```

    > [!IMPORTANT]
    > Raspberry Pi IoT -simulaattorille koodieditorissa määritettyjen tunnistinten tunnusten on oltava samanlaiset kuin myöhemmin Supply Chain Managementin skenaarioissa määritetyt tunnistinten tunnukset. Edeltävässä esimerkissä koodi käyttää luettavia tunnistinten tunnuksia. Todellisessa skenaariossa tunnistinten tunnukset ovat kuitenkin GUID-arvoja, jotka tunnistimen valmistaja määrittää. Tässä esimerkkikoodissa käytettäviä luettavassa muodossa olevia tunnistimien tunnuksia käytetään myös esimerkeissä [Tuotteen laadun skenaario](sdi-scenario-product-quality.md), [Resurssien ylläpitoskenaario](sdi-scenario-asset-maintenance.md), [Tuotannon viiveiden skenaario](sdi-scenario-production-delays.md) ja [Koneen tilan skenaario](sdi-scenario-equipment-downtime.md)). Käytä tämän vuoksi tätä koodia, jos käsittelet näitä skenaarioita.

## <a name="edit-the-interval-for-sending-sensor-signals"></a>Tunnistinten signaalien lähettämisvälin muokkaaminen

Määritä nyt väli, jonka mukaan Raspberry Pi IoT -simulaattorin on lähetettävä emuloitujen tunnistinten signaaleja.

1. Etsi seuraava funktion kutsu Raspberry Pi IoT -simulaattorin koodieditorista.

    `setInterval(sendMessage, 2000);`

2. Oletusarvoisesti Raspberry Pi IoT -simulaattori lähettää tunnistimen signaalin 2 000 millisekunnin (kahden sekunnin) välein. Voit muuttaa arvoa tarvittaessa.

## <a name="run-the-raspberry-pi-iot-simulator"></a>Raspberry Pi IoT -simulaattorin suorittaminen

- Käynnistä simulaattori valitsemalla **Suorita** ja aloita simuloitujen tunnistinten tietojen lähettäminen.
