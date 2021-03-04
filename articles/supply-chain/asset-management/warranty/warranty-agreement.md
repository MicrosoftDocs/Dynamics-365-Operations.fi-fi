---
title: Takuusopimukset
description: Tässä ohjeaiheessa kerrotaan takuusopimuksista resurssien hallinnassa.
author: josaw1
manager: tfehr
ms.date: 08/24/2020
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
ms.openlocfilehash: f049165fd12dfae672293e0c30ddb186ad3ed12c
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4427213"
---
# <a name="warranty-agreements"></a>Takuusopimukset

[!include [banner](../../includes/banner.md)]

 


Käyttöomaisuuden hallinnassa voit määrittää takuuehdot, jotka voidaan liittää käyttöomaisuuserään tai käyttöomaisuuslajiin. Takuuehdot luodaan tietylle kaudelle. Takuun voi määrittää siten, että se sisältää täyden kattavuuden tai osittaisen kattavuuden, ja voit määrittää ehdot, jotka liittyvät tunteihin, kuluihin ja nimikkeisiin.

Ensimmäiseksi on luotava mahdolliset toimittajien takuusopimukset, jotka on tehty laitteillesi. Tämän jälkeen voit liittää takuusopimukset käyttöomaisuuseriin tai omaisuustyyppeihin. Toimittajien takuusopimuksia käytetään vain tiedotustarkoituksiin. Jos toimittajan takuu on määritetty käyttöomaisuuserään, voit nähdä käyttöomaisuuserän takuun kattavuuskauden.

## <a name="create-a-warranty-agreement"></a>Luo takuusopimus

Takuusopimukseen voi kuulua useita sopimusrivejä, jotka kattavat työajan, kulujen ja nimikkeiden takuun.

1. Valitse **Resurssien hallinta** \> **Asetukset** \> **Resurssit** \> **Takuu**.
2. Luo tuote valitsemalla **Uusi**.
3. Syötä **Takuu** -kenttään takuun tunnus. 
4. Anna kuvaus **nimi**-kenttään.

    **Tiedot**-pikavälilehden **Resurssit**-kentässä näkyy takuusopimusta käyttävien aktiivisten resurssien määrä.

5. Lisää takuusopimukseen sisällytettävät rivit **Takuurivit**-pikavälilehdessä seuraavasti:

    1. Voit lisätä uuden ehdon takuuseen valitsemalla **Lisää rivi**. **Rivi**-kenttään syötetään automaattisesti rivin järjestysnumero.
    2. Valitse **Kausi**-kentässä takuukauden tyyppi.
    3. Syötä numero **Väli**-kenttään. Tämä kenttä määrittää niiden kausien määrän, joiden takuun tulisi olla voimassa.
    4. Kirjoita takuurivin kattavuusprosentti **Prosentti**-kenttään. Prosenttiosuus ilmaisee, kuinka paljon yrityksesi kattaa takuuta.

![Takuusivu](media/01-warranty.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]