---
title: Takuusopimukset
description: Tässä ohjeaiheessa kerrotaan takuusopimuksista resurssien hallinnassa.
author: josaw1
manager: AnnBe
ms.date: 08/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 71905d5b362c80d48b78210b59cacfb1e7899757
ms.sourcegitcommit: 802dbf0a744d70f9e546632d419415b0993331ab
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/13/2019
ms.locfileid: "1874690"
---
# <a name="warranty-agreements"></a>Takuusopimukset

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


Käyttöomaisuuden hallinnassa voit määrittää takuuehdot, jotka voidaan liittää käyttöomaisuuserään tai käyttöomaisuuslajiin. Takuuehdot luodaan tietylle kaudelle. Takuun voi määrittää siten, että se sisältää täyden kattavuuden tai osittaisen kattavuuden, ja voit määrittää ehdot, jotka liittyvät tunteihin, kuluihin ja nimikkeisiin.

Ensimmäiseksi on luotava mahdolliset toimittajien takuusopimukset, jotka on tehty laitteillesi. Tämän jälkeen voit liittää takuusopimukset käyttöomaisuuseriin tai omaisuustyyppeihin. Toimittajien takuusopimuksia käytetään vain tiedotustarkoituksiin. Jos toimittajan takuu on määritetty käyttöomaisuuserään, voit nähdä käyttöomaisuuserän takuun kattavuuskauden.

## <a name="create-a-warranty-agreement"></a>Luo takuusopimus

Takuusopimukseen voi kuulua useita sopimusrivejä, jotka kattavat työajan, kulujen ja nimikkeiden takuun.

1. Valitse **Resurssien hallinta** \> **Asetukset** \> **Resurssit** \> **Takuu**.
2. Luo tuote valitsemalla **Uusi**.
3. Syötä **Takuu** -kenttään takuun tunnus.
4. Anna kuvaus **nimi**-kenttään.

    **Tiedot**-pikavälilehden **Resurssit**-kentässä näkyy takuusopimusta käyttävien aktiivisten resurssien määrä.

5. Tee **Tuntitakuu**- ja **Nimiketakuu**-pikavälilehdissä seuraavat vaiheet, kun haluat lisätä rivejä tunteja tai nimikkeitä koskevaan takuusopimukseen:

    1. Voit lisätä uuden ehdon takuuseen valitsemalla **Lisää rivi**. **Rivi**-kenttään syötetään automaattisesti rivin järjestysnumero.
    2. Valitse **Kausi**-kentässä takuukauden tyyppi.
    3. Syötä numero **Väli**-kenttään. Tämä kenttä määrittää niiden kausien määrän, joiden takuun tulisi olla voimassa.
    4. Kirjoita takuurivin kattavuusprosentti **Prosentti**-kenttään. Prosenttiosuus ilmaisee, kuinka paljon yrityksesi kattaa takuuta.

![Kuva 1](media/01-warranty.png)