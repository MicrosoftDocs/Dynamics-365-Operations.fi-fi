---
title: Resurssien ja resurssityyppien takuut
description: Tässä artikkelissa kerrotaan, kuinka voit määrittää resurssien ja resurssityyppien takuut resurssien hallinnassa.
author: johanhoffmann
ms.date: 08/30/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: fa4fe7af46996e8de76ea61d5395327e7617e736
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8906121"
---
# <a name="warranties-on-assets-and-asset-types"></a>Resurssien ja resurssityyppien takuut

[!include [banner](../../includes/banner.md)]

 


Tässä artikkelissa kerrotaan, kuinka voit määrittää resurssien ja resurssityyppien takuut resurssien hallinnassa.

## <a name="set-up-a-warranty-on-an-asset-type"></a>Takuun määrittäminen resurssityypille

1. Valitse **Resurssien hallinta** \> **Asetukset** \> **Resurssityypit** \> **Resurssityypit**.
2. Valitse vasemmanpuoleisesta ruudusta käyttöomaisuustyyppi, johon toimittajan takuusopimus liitetään, ja valitse **Resurssin oletustyypit**.
3. Valitse sopimus **Yleiset**-pikavälilehden **Toimittajan takuu** -kentässä.

## <a name="set-up-a-warranty-on-an-asset"></a>Takuun määrittäminen resurssille

1. Valitse **Resurssien hallinta** \> **Yhteiset** \> **Resurssit** \> **Kaikki resurssit**.
2. Valitse käyttöomaisuuserä ja valitse sitten **Muokkaa**.
3. Valitse takuusopimus **Toimittaja**-pikavälilehden **Toimittajan takuu**-osan **Takuu**-kentässä.
4. Valitse **Takuun alkamispäivämäärä**- ja **Takuun päättymispäivämäärä** -kentissä alkamis- ja päättymispäivämäärät.

    > [!IMPORTANT]
    > Jos työtilauksen **Takuun alkamispäivämäärä** -kentässä on valittu päivämäärä, takuu on voimassa kyseisenä päivänä työtilaukselle. Kun luot työtilauksen, **Takuun alkamispäivämäärä** -kentän arvoksi tulee automaattisesti luontipäivämäärä. Voit kuitenkin muuttaa päivää niin, että se vastaa esimerkiksi takuusopimuksen alkamispäivämäärää.
    >
    > ![Työtilaussivu.](media/02-warranty.png)

> [!NOTE]
> Kun luot työtilauksen käyttöomaisuudelle, joka kuuluu toimittajan takuun piiriin ja jos työtilauksen odotettu alkamispäivämäärä on takuukauden aikana, saat takuusopimuksesta ilmoituksen. Tämän jälkeen voit peruuttaa työtilauksen tarpeen mukaan.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]