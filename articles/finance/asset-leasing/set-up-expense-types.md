---
title: Kulutyyppien määrittäminen
description: Tässä artikkelissa kerrotaan, kuinka kulutyypit määritetään resurssien vuokrauksessa.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseExpenseTypeTable
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2019-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 9978041059437d5d3556236c7ac02c00db93f933
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8908035"
---
# <a name="set-up-expense-types"></a>Kulutyyppien määrittäminen

[!include [banner](../includes/banner.md)]

Tässä artikkelissa kerrotaan, kuinka kulutyypit määritetään resurssien vuokrauksessa. Kustannukset, joita ,maksuaikataulu ei sisällä, kutsutaan *kulukustannuksiksi*. Esimerkkejä näistä kustannuksista ovat kiinteistöverot, yleiset ylläpitokustannukset ja vakuutuskulut.

## <a name="add-an-administrative-expense-type"></a>Hallinnollisen kulutyypin lisääminen

1. Siirry kohtaan **Resurssin vuokraus \> Asetukset \> Kulutyypit**.
2. Valitse **Uusi**.
3. Anna soveltuviin kenttiin uusi kulutyyppi ja kuvaus.

## <a name="assign-accounts-to-administrative-costs"></a>Tilien määrittäminen hallintokuluille

Seuraavaksi sinun tulee liittää tilit kulutyyppeihin. Näitä tilejä veloitetaan, kun kuluaikatauluviennit kirjataan. Vastatili on määritetty **Toimeenpanokustannusten maksuaikataulu** -riveille jokaisessa vuokrasopimuksessa.

1. Siirry kohtaan **Resurssin vuokraus \> Asetukset \> Resurssin vuokrausparametrit**.
2. Valitse **Tilit**-välilehden **Toimeenpanokustannukset**-pikavälilehden **Kulutyyppi**-kentässä kulutyyppi.
3. Valitse **Lisää**.
4. Valitse **Kirjan tyyppi** -kentässä tyyppi, joka linkitetään hallinnollisiin kustannuksiin.

    > [!NOTE]
    > Samaan kulutiliin voi linkittää useita kirjatyyppejä.

5. Määritä **Tkoodi**-kentässä, mihin vuokrasopimuksiin kirja kohdistetaan:

    - **Kaikki** – Kirja kohdistetaan kaikkiin vuokrasopimuksiin.
    - **Ryhmä** – Kirja kohdistetaan tiettyyn vuokrasopimusryhmään.
    - **Taulukko** – Kirja kohdistetaan tiettyihin vuokrasopimuksiin.

6. Jos olet valinnut **Ryhmä** tai **Taulukko** **Tilikoodi**-kentässä, valitse tilinumero tai ryhmänumero **Tili-/ryhmänumero**-kentässä.
7. Valitse asianmukaisten kenttien rahoitusleasingsopimuksen päätili ja käyttöleasingsopimuksen päätili.

Kun olet tehnyt nämä vaiheet, voit lisätä kuluja valitun vuokrasopimuksen **Toimeenpanokustannusten maksuaikataulu** -riveillä **Vuokrauksen tiedot** -sivulla. Vaihtoehtoisesti voit lisätä kuluja, kun luot uuden vuokrasopimuksen.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
