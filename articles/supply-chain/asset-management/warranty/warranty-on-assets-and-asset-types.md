---
title: Resurssien ja resurssityyppien takuut
description: Tässä ohje aiheessa kerrotaan, kuinka voit määrittää resurssien ja resurssityyppien takuut resurssien hallinnassa.
author: josaw1
manager: tfehr
ms.date: 08/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 75de9a51560dcd8fea7998425fee14a27e891972
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/02/2020
ms.locfileid: "3215398"
---
# <a name="warranties-on-assets-and-asset-types"></a>Resurssien ja resurssityyppien takuut

[!include [banner](../../includes/banner.md)]

 


Tässä ohje aiheessa kerrotaan, kuinka voit määrittää resurssien ja resurssityyppien takuut resurssien hallinnassa.

## <a name="set-up-a-warranty-on-an-asset-type"></a>Takuun määrittäminen resurssityypille

1. Valitse **Resurssien hallinta** \> **Asetukset** \> **Resurssityypit** \> **Resurssityypit**.
2. Valitse vasemmanpuoleisesta ruudusta käyttöomaisuustyyppi, johon toimittajan takuusopimus liitetään, ja valitse **Resurssin oletustyypit**.
3. Valitse sopimus **Yleiset**-pikavälilehden **Toimittajan takuu** -kentässä.

## <a name="set-up-a-warranty-on-an-asset"></a>Takuun määrittäminen resurssille

1. Valitse **Resurssien hallinta** \> **Yhteiset** \> **Resurssit** \> **Kaikki resurssit**.
2. Valitse käyttöomaisuuserä ja valitse sitten **Muokkaa**.
3. Valitse takuusopimus**Toimittaja**-pikavälilehden **Toimittajan takuu**-osan **Takuu**-kentässä.
4. Valitse **Takuun alkamispäivämäärä**- ja **Takuun päättymispäivämäärä** -kentissä alkamis- ja päättymispäivämäärät.

    > [!IMPORTANT]
    > Jos työtilauksen **Takuun alkamispäivämäärä** -kentässä on valittu päivämäärä, takuu on voimassa kyseisenä päivänä työtilaukselle. Kun luot työtilauksen, **Takuun alkamispäivämäärä** -kentän arvoksi tulee automaattisesti luontipäivämäärä. Voit kuitenkin muuttaa päivää niin, että se vastaa esimerkiksi takuusopimuksen alkamispäivämäärää.
    >
    > ![Työtilaussivu](media/02-warranty.png)

> [!NOTE]
> Kun luot työtilauksen käyttöomaisuudelle, joka kuuluu toimittajan takuun piiriin ja jos työtilauksen odotettu alkamispäivämäärä on takuukauden aikana, saat takuusopimuksesta ilmoituksen. Tämän jälkeen voit peruuttaa työtilauksen tarpeen mukaan.
