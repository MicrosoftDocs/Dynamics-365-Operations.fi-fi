---
title: IoT-analytiikan mittareiden
description: Tässä ohjeaiheessa käsitellään IoT-analytiikan mittareiden määrittämistä.
author: tonyafehr
ms.date: 04/25/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: tfehr
ms.custom: ''
ms.search.region: Global
ms.author: tfehr
ms.search.validFrom: 2020-04-25
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 85db0211c32ad4e27c3a9a65d2c74c5a39687f9c
ms.sourcegitcommit: 9acfb9ddba9582751f53501b82a7e9e60702a613
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/10/2021
ms.locfileid: "7783095"
---
# <a name="set-up-metrics-for-iot-intelligence"></a>IoT-analytiikan mittareiden

[!include [banner](../../includes/banner.md)]

## <a name="configure-metrics"></a>Mittareiden määritys

Jos haluat tarkastella Microsoft Dynamics 365 Supply Chain Managementin viestiesi aikasarjakaavioita, sinun on määritettävä mittarit seuraavalla tavalla.

1. Kopioi yhteysmerkkijono Redis-välimuistia varten:

    1. Siirry Azure-portaalissa Redis-välimuistiin.
    2. Siirry kohtaan **Asteukset** \> **Käyttöoikeusavaimet**.
    3. Kopioi **Ensisijainen yhteysmerkkijono** -kentän arvo.

2. Siirry Supply Chain Managementissa kohtaan **Tuotannonhallinta \> Asetukset \> IoT-analytiikka \> Skenaarioparametrit**.
3. Liitä aiemmin kopioitu yhteysmerkkijono **Skenaarioparametrit **-sivun** Aikasarjat**-välilehden **Redis-mittareiden myymäläyhteysmerkkijono** -kenttään. Tällä vaiheella mahdollistetaan Azuren IoT-keskittimen mittareiden visualisointi Supply Chain Managementissa. Kun liität arvon kenttään, se näkyy muodossa **\*\*\*\*\*\***.

    > [!NOTE]
    > Aina kun Redis-välimuistin yhteysmerkkijono päivitetään, myös tämä kenttä on päivitettävä.

4. Siirry kohtaan **Tuotannonhallina \> Kyselyt ja raportit \> IoT-analyysi \> Mittariavaimet**.
5. Valitse **Mittariavaimet**-sivulla **Päivitä**.
6. Huomaa **Päivitä mittariavaimet** -valintaikkunassa, että kentässä on valittuna **Suorita taustalla**. Valitse **OK**.

Kaikki Radis-välimuistin mittariavaimet noudetaan ja lisätään **Mittariavaimet**-luetteloon. Mittausarvot eivät näy, ennen kuin [otat skenaariot käyttöön](iot-scenario-setup.md).

## <a name="configure-the-resource-status-time-series"></a>Resurssin tilan aikasarjan määritys

**Resurssin tila** -aikasarja määritetään seuraavasti.

1. Siirry Supply Chain Managementissa kohtaan **Tuotannonhallinta \> Valmistuksen suoritus \> Resurssin tila**.
2. Valitse **Resurssin tila**-sivulla **Määritä**.
2. Valitse **Resurssi**-luettelon **Määritä**-valintaikkunassa valvottava kohde.
3. Valitse **Muokkaa** aikasarjan **Aikasarja 1** osalta.
4. Valitse mittari ruudukosta **Valitse aikasarja** -valintaikkunassa. (Voit myös käyttää **Päivitä mittariavaimet** -linkkiä mittariavaimien päivittämiseen tästä valintaikkunasta.)
5. Palaa **Määritä**-valintaikkunaan valitsemalla **OK**.
6. Anna näytönimi.
7. Valitse aikaväli **Näytä tiedot alkaen** -kentässä.
8. Valitse **OK**.

Kaavio tulee näkyviin.

## <a name="delete-a-metric-key"></a>Mittariavaimen poistaminen

1. Siirry Supply Chain Managementissa kohtaan **Tuotannonhallina \> Kyselyt ja raportit \> IoT-analyysi \> Mittariavaimet**.
2. Valitse **Mittariavaimet**-sivulla poistettava mittariavain.
3. Valitse **Poista**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]