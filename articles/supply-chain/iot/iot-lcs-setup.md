---
title: IoT-analytiikkalisäosan asentaminen LCS:ssä
description: Tässä artikkelissa käsitellään IoT-analytiikkalisäosan asentamista Microsoft Dynamics Lifecycle Servicesiin (LCS).
author: johanhoffmann
ms.date: 08/04/2022
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
ms.openlocfilehash: e18b05be1f2ba78c71515e4e76f180355d044b98
ms.sourcegitcommit: e0905a3af85d8cdc24a22e0c041cb3a391c036cb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/06/2022
ms.locfileid: "9227831"
---
# <a name="install-the-iot-intelligence-add-in-in-lcs"></a>IoT-analytiikkalisäosan asentaminen LCS:ssä

[!include [banner](../../includes/banner.md)]
[!INCLUDE [iot-sdi-announcement](../../includes/iot-sdi-announcement.md)]

Tässä artikkelissa käsitellään IoT-analytiikkalisäosan asentamista Microsoft Dynamics Lifecycle Servicesiin (LCS). Huomaa, että lisäosia ei voi asentaa esittely- tai kokeiluympäristöön. Ennen lisäosan asentamista on [luotava Azure-resurssit](iot-azure-setup.md).

Voit määrittää IoT-analyysin ilman koodin kirjoittamista. Seuraavassa on perusvaiheet.

1. [Azure-resurssien määrittäminen](iot-azure-setup.md) – Luo IoT Hub, Redis-välimuisti ja avainsäilö, joita voi käyttää Supply Chain Managementista.
2. [IoT Hubin sanomarakenteen muodot](iot-schema-format.md) – Määritä laitteesi lähettämään sanomia IoT Hubille ja määritä JavaScript Object Notationin (JSON) sanomamuoto.
3. Ota ominaisuuksienhallinnassa käyttöön IoT-analyysin toimintomerkintä.
4. Asenna IoT-analyysin lisäosa Microsoft Dynamics Lifecycle Servicesiin (LCS) – Asenna lisäosa LCS:ään ja määritä Azuren salaiset koodit (kuten kuvattu tässä artikkelissa).
5. [Mittareiden määrittäminen](iot-metrics-setup.md) – Määritä mittareita Supply Chain Managementissa.
6. [Skenaarion määritys](iot-scenario-setup.md) – Määritä skenaariot Supply Chain Managementissa.

## <a name="set-up-the-lcs-environment"></a>LCS-ympäristön määrittäminen

1. Avaa LCS ja siirry Microsoft Dynamics 365 Supply Chain Management -ympäristöön.
2. Vieritä **Ympäristön lisäosat** -osaan.
3. Valitse **Asenna uusi lisäosa**, jolloin näkyviin tulee luettelo ympäristössä käyttöönotetuista lisäosista.
4. Valitse **Valitse asennettava lisäosa** -valintaikkunassa **IoT-analytiikka**.
5. Anna **Määritä lisäosa** -valintaikkunassa IoT-keskittimen ja Redis-välimuistin tiedot. Tarvittavat arvot sijaitsevat avainsäilössä, joka luotiin kohdassa [Azure-resurssien luonti](iot-azure-setup.md).

    + **Vuokraajan tunnus** – Siirry Azure-portaalissa avainsäilöön ja valitse sitten vasemmassa siirtymisruudussa **Yleiskatsaus** ja kopioi **Hakemistotunnus**-arvo. Liitä tämä arvo **Määritä lisäosa** -valintaikkunaan.
    + **IoT-tapahtuman keskittimen kanssa yhteensopiva päätepisteen avainsäilön URI** – Siirry avainsäilöön, valitse vasemmassa siirtymisruudussa **Yleiskatsaus** ja kopioi **DNS-nimi**-arvo. Liitä tämä arvo **Määritä lisäosa** -valintaikkunaan.
    + **IoT-tapahtuman keskittimen kanssa yhteensopivan päätepisteen salaisuuden nimi** – Siirry avainsäilöön ja valitse sitten vasemmassa siirtymisruudussa **Salaisuudet** ja kopioi salaisuuden nimi sinne, mihin IoT-keskittimen tapahtuman keskittimen yhteysmerkkijono on tallennettu. Liitä tämä arvo **Määritä lisäosa** -valintaikkunaan.
    + **Redis-välimuistin avainsäilön URI** – Siirry avainsäilöön, valitse vasemmassa siirtymisruudussa **Yleiskatsaus** ja kopioi **DNS-nimi**-arvo. Liitä tämä arvo **Määritä lisäosa** -valintaikkunaan.
    + **Redis-välimuistin päätepisteen salaisuuden nimi** – Siirry avainsäilöön ja valitse sitten vasemmassa siirtymisruudussa **Salaisuudet** ja kopioi salaisuuden nimi sinne, mihin Redis-välimuistin yhteysmerkkijono on tallennettu. Liitä tämä arvo **Määritä lisäosa** -valintaikkunaan.

6. Hyväksy ehdot valitsemalla valintaruutu.
7. Valitse **Asenna**.
8. Avautuva sanomaruutu ilmoitta, että lisäosan käynnistäminen asennettavaksi onnistui. Valitse **OK**.

LCS-määritys on nyt valmis. Seuraavaksi [määritetään skenaariot](iot-scenario-setup.md).

## <a name="uninstall-the-add-in"></a><a id="uninstall-addin"></a>Lisäosan asennuksen poistaminen

1. [Poista skenaariot käytöstä](iot-scenario-setup.md#disable-a-scenario) Supply Chain Managementissa.
2. Siirry LCS:ssä Supply Chain Management -ympäristön tietoihin.
3. Vieritä **Ympäristön lisäosat** -osaan.
4. Valitse IoT-analytiikkalisäosan osalta **Poista asennus**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]