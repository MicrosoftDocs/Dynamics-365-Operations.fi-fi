---
title: IoT-analytiikkalisäosan asentaminen LCS:ssä
description: Tässä ohjeaiheessa käsitellään IoT-analytiikkalisäosan asentamista Microsoft Dynamics Lifecycle Servicesiin (LCS).
author: robinarh
manager: tfehr
ms.date: 07/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: rhaertle
ms.custom: ''
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 87d04c3df22e2d9ef56acb61e26304731a2a17a2
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5206049"
---
# <a name="install-the-iot-intelligence-add-in-in-lcs"></a>IoT-analytiikkalisäosan asentaminen LCS:ssä

[!include [banner](../../includes/banner.md)]

Tässä ohjeaiheessa käsitellään IoT-analytiikkalisäosan asentamista Microsoft Dynamics Lifecycle Servicesiin (LCS). Huomaa, että lisäosia ei voi asentaa esittely- tai kokeiluympäristöön. Ennen lisäosan asentamista on [luotava Azure-resurssit](iot-azure-setup.md).

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