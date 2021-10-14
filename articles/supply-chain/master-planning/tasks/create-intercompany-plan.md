---
title: Konsernin sisäisen suunnitelman luominen
description: Tässä menettelyssä kuvataan, miten luot konsernin sisäisen suunnitelman.
author: ChristianRytt
ms.date: 08/13/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ReqIntercompanyPlanningGroupSetup,  ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7ef1484e6925427454f819a5effdc911f762b48b
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/29/2021
ms.locfileid: "7578269"
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

## <a name="create-an-intercompany-master-plan"></a>Konserniyritysten välisen pääsuunnitelman luominen

1. Siirry **siirtymisruudussa** **Moduulit > Pääsuunnittelu > Työtilat > Pääsunnittelu.**
2. Valitse **Konsernin sisäinen pääsuunnittelu**.  
3. Avaa haku napsauttamalla **Konsernin sisäinen suunnitteluryhmä** -kentässä avattavan valikon painiketta.
4. Valitse luettelossa valitulla rivillä oleva linkki. Valitse konsernin sisäinen suunnitteluryhmä 10.  
5. Kirjoita **Konsernin sisäisten suunnitteluiteraatioiden määrä** -kenttään arvo 2. Konsernin sisäisellä suunnitteluryhmällä 10 on kaksi jäsentä. Jotta viiveet voisi täyttää lähdeyrityksestä (USMF) asiakasyritykseen (DEMF), konsernin sisäinen suunnittelu on ajettava molemmissa yrityksissä kahdesti. Ensimmäinen iteraatio täyttää kysynnän ja tunnistaa lähdeyrityksen (USMF) viiveet. Toisen iteraatio täyttää viiveet yritysten välillä.  
6. Valitse Täydellinen laskenta -vaihtoehto **Ensimmäinen iteraatio** -kentässä.
7. Valitse Täydellinen laskenta -vaihtoehto **Seuraavat iteraatiot** -kentässä.
8. Syötä **Säikeiden määrä** -kenttään numero. Tämä vastaa suunnittelussa käytettävien rinnakkaisten säikeiden määrää.  
9. Valitse **OK**.

## <a name="view-the-result-of-the-plan"></a>Näytä suunnitelman tulos

1. Avaa haku valitsemalla **Suunnitelma**-kentässä avattavan valikon painike.
2. Valitse luettelossa valitulla rivillä oleva linkki. Valitse StaticPlan-linkki. Sinun on oltava USMF-yrityksessä.  
3. Valitse **Suunnitellut tilaukset**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]