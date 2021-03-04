---
title: Konsernin sisäisen suunnitelman luominen
description: Tässä menettelyssä kuvataan, miten luot konsernin sisäisen suunnitelman.
author: ShylaThompson
manager: tfehr
ms.date: 08/13/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqIntercompanyPlanningGroupSetup,  ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3ae3d8a7c437ffd41a4864bd8548aa84c8ab8f32
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4426933"
---
# <a name="create-an-intercompany-plan"></a>Konsernin sisäisen suunnitelman luominen

[!include [banner](../../includes/banner.md)]

Tässä menettelyssä kuvataan, miten luot konsernin sisäisen suunnitelman. Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.


## <a name="set-up-an-intercompany-planning-group"></a>Määritä konsernin sisäinen suunnitteluryhmä 
1. Siirry **siirtymisruudussa** **Moduulit > Pääsuunnittelu > Asetukset > Konsernin sisäiset suunnitteluryhmät.** 
2. Käytä pikasuodatinta tietueiden etsimiseen. Voit esimerkiksi suodattaa Nimi-kenttää arvolla 10.
3. Merkitse valittu rivi luettelossa.
4. Valitse **Poista**. Tämä vaihe on tarpeen konsernin sisäisen suunnitelma-ajon lyhentämiseksi.   Konsernin sisäisessä suunnittelussa ajetaan kaikkien suunnitteluryhmän yritysten pääsuunnittelu, ajoitusjärjestyksessä pienimmästä alkaen.  
5. Valitse **Kyllä**.
6. Sulje sivu.

## <a name="create-an-intercompany-plan"></a>Konserniyritysten välisen suunnitelman luominen
1. Siirry **siirtymisruudussa** **Moduulit > Pääsuunnittelu > Työtilat > Pääsunnittelu.**
2. Valitse **Konsernin sisäinen pääsuunnittelu**.  
3. Avaa haku napsauttamalla **Konsernin sisäinen suunnitteluryhmä** -kentässä avattavan valikon painiketta.
4. Napsauta luettelossa valitulla rivillä olevaa linkkiä. Valitse konsernin sisäinen suunnitteluryhmä 10.  
5. Kirjoita **Konsernin sisäisten suunnitteluiteraatioiden määrä** -kenttään arvo 2. Konsernin sisäisellä suunnitteluryhmällä 10 on kaksi jäsentä. Jotta viiveet voisi täyttää lähdeyrityksestä (USMF) asiakasyritykseen (DEMF), konsernin sisäinen suunnittelu on ajettava molemmissa yrityksissä kahdesti. Ensimmäinen iteraatio täyttää kysynnän ja tunnistaa lähdeyrityksen (USMF) viiveet. Toisen iteraatio täyttää viiveet yritysten välillä.  
6. Valitse Täydellinen laskenta -vaihtoehto **Ensimmäinen iteraatio** -kentässä.
7. Valitse Täydellinen laskenta -vaihtoehto **Seuraavat iteraatiot** -kentässä.
8. Syötä **Säikeiden määrä** -kenttään numero. Tämä vastaa suunnittelussa käytettävien rinnakkaisten säikeiden määrää.  
9. Valitse **OK**.

## <a name="view-the-result-of-the-plan"></a>Näytä suunnitelman tulos
1. Avaa haku valitsemalla **Suunnitelma**-kentässä avattavan valikon painike.
2. Napsauta luettelossa valitulla rivillä olevaa linkkiä. Napsauta StaticPlan-linkkiä. Sinun on oltava USMF-yrityksessä.  
3. Valitse **Suunnitellut tilaukset**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]