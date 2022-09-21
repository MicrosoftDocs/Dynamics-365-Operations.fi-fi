---
title: Resurssin käyttökatkon skenaario
description: Tässä artikkelissa kerrotaan resurssin käyttökatkon skenaario, jonka avulla voit käyttää tunnistimen tietoja resurssien käytettävyyden seuraamista varten.
author: johanhoffmann
ms.date: 09/02/2022
ms.topic: article
ms.search.form: IoTIntCoreScenarioManagement, IoTIntCoreScenarioConfigurationWizardV2, EntAssetObjectProductionStop
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-09-02
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: 944818557deebed06c02c00fd69de6e8f08bda83
ms.sourcegitcommit: 3d7ae22401b376d2899840b561575e8d5c55658c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/08/2022
ms.locfileid: "9428377"
---
# <a name="the-asset-downtime-scenario"></a>Resurssin käyttökatkon skenaario

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

Käyttöomaisuuden käyttökatkon skenaario luo ylläpidon käyttökatkon tietueen, jos signaalia ei vastaanoteta koneesta määritetyssä ajassa edellisen signaalin vastaanottamisen jälkeen. Skenaario edellyttää, että koneessa on tunnistin, joka lähettää signaalin Azure IoT -keskittimeen säännöllisesti samalla, kun konetta käytetään, mutta ei lähetä signaalia, kun kone ei ole käytössä

## <a name="set-up-the-asset-downtime-scenario"></a>Resurssin käyttökatkon skenaarion määrittäminen

Alla olevien vaiheiden avulla voit määrittää *resurssin käyttökatkon* skenaarion Supply Chain Managementissa.

1. Siirry kohtaan **Resurssien hallinta \> Asetukset \> Sensor Data Intelligence \> Skenaariot** ja avaa **Skenaariot**-sivu.
2. Valitse **resurssin käyttökatkon** skenaarion ruudussa **Määritä**, jos haluat avata tämän skenaarion ohjatun asennuksen.
3. Valitse **Tunnistimet**-sivulla **Uusi** lisätäksesi tunnistimen ruudukkoon. Määritä sitten seuraavat kentät:

    - **Tunnistimen tunnus** – Syötä käytössä olevan tunnistimen tunnus. (Jos käytössä on Raspberry PI Azure IoT -verkkosimulaattori ja se on määritetty kohdan [Simuloidun tunnistimen määrittäminen testausta varten](sdi-set-up-simulated-sensor.md) ohjeiden mukaan, valitse *AssetDownTime*.)
    - **Tunnistimen kuvaus** – Syötä tunnistimen kuvaus.

4. Toista edellinen vaihe kullekin nyt lisättävälle lisätunnistimelle. Voit milloin tahansa palata takaisin ja lisätä tunnistimia.
5. Valitse **Seuraava**.
6. Valitse **Liiketoimintatietueen yhdistämismääritys** -sivun **Tunnistimet**-osassa jonkin juuri lisätyn tunnistimen tietue.
7. Valitse **Liiketoimintatietueen yhdistämismääritys** -osassa **Uusi** lisätäksesi ruudukkoon rivin.
8. Määritä uudella rivillä **Liiketoimintatietue**-kenttä resurssissa, jossa valittu tunnistin on käytössä seurantaa varten. (Jos käytössä ovat esittelytiedot, valitse *AK-101, ilmaveitsi linjalle 1*.)
9. Valitse **Seuraava**.
10. Määritä **resurssin käyttökatkon raja-arvon** sivulla, miten kauan edellisen signaalin jälkeen järjestelmän tulee odottaa, ennen kuin resurssin käyttökatkon ilmoitus lähetetään. Raja-arvon määrittämiseksi on kaksi seuraavaa tapaa:

    - **Oletusraja-arvo (minuutteja)** – Määritä tämä kenttä oletusraja-arvon määrittämistä varten. Tätä arvoa käytetään kaikissa resursseissa, joissa **Ilmoituksen raja-arvo (minuutteina)** -kentän arvoksi määritetään enintään kaksi minuuttia. Vähimmäisarvo on *2* (minuuttia).
    - **Raja-arvo, jolla määritetään koneen vastaamattomuusaika (minuutteina)** – Syötä ohitusarvo tähän kenttään kaikille ruudukon resursseille, joissa et halua käyttää oletusraja-arvoa. Resurssit, jotka on määritetty käyttämään enintään kahden minuutin raja-arvoa, käyttävät sen sijaan **Oletusraja-arvo (minuutteina)** -asetusta.
11. Valitse **Seuraava**.
12. Valitse **Aktivoi tunnistimet** -sivulla määritetty tunnistin ja valitse sitten **Aktivoi**. Ruudukon jokaiselle aktivoidulle tunnistimelle tulee näkyviin valintamerkki **Aktiivinen**-sarakkeessa.
13. Valitse **Valmis**.

## <a name="work-with-the-asset-downtime-scenario"></a>Resurssin käyttökatkon skenaarion käsitteleminen

Jos tunnistimen signaalia ei vastaanoteta resurssilta skenaarion määrityksen raja-arvon määrittämänä aikana, järjestelmä luo resurssille ylläpidon käyttökatkotietueen. Esimiesten tulee säännöllisesti tarkistaa käyttökatkotietueet (esimerkiksi kerran jokaisen työvuoron aikana) ja käyttää soveltuvia syykoodeja sekä lopetusaikoja kaikissa käyttökatkon rekisteröinneissä. Seuraavien vaiheiden avulla voit tarkastella resurssin ylläpidon käyttökatkotietueita:

1. Siirry kohtaan **Resurssien hallinta > Resurssit > Kaikki resurssit**.
2. Etsi ja valitse tarkastettava resurssi. (Jos käytät esittelytietoja, valitse *AK-101*.)
3. Avaa toimintoruudussa **Resurssi**-välilehti ja valitse **Työtilaus**-ryhmässä **Ylläpidon käyttökatkos**, jos haluat avata valitun resurssin ylläpidon käyttökatkostietueiden sivun.
