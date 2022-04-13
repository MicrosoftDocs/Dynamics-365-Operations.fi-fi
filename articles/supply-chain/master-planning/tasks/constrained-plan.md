---
title: Rajoitetun suunnitelman luominen
description: Tässä aiheessa kerrotaan, miten luodaan suunnitelma, jossa huomioidaan sekä kapasiteetti- ja materiaalirajoitukset.
author: t-benebo
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, ReqPlanSched
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f8372f4e35b34ff66ef55c0961b867a1aff7a5e6
ms.sourcegitcommit: ad1afc6893a8dc32d1363395666b0fe1d50e983a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/23/2022
ms.locfileid: "8468941"
---
# <a name="generate-a-constrained-plan"></a>Rajoitetun suunnitelman luominen

[!include [banner](../../includes/banner.md)]

Tässä aiheessa kerrotaan, miten luodaan suunnitelma, jossa huomioidaan sekä kapasiteetti- ja materiaalirajoitukset. Suunnitelma varmistaa, että valmistus aloitetaan vasta sitten, kun materiaalit ovat käytettävissä. Se myös estää resurssien ylivaraamisen. 

Tämän menettelyn luomisessa käytetty esittely-yritys on USMF. Tämä menettely on tarkoitettu tuotannon suunnittelijalle.


## <a name="set-up-a-constrained-plan"></a>Rajoitetun suunnitelman määrittäminen
1. Valitse aloitussivulla **Pääsuunnittelu**-työtila.
2. Valitse **Pääsuunnitelmat** työtilan äärimmäisenä oikealla puolella olevasta linkkiluettelosta.
3. Etsi haluamasi tietue luettelosta ja valitse se. Esimerkki: **StaticPlan**  
4. Valitse **Rajallinen kapasiteetti** -kentässä **Kyllä**.
5. Syötä **Rajallisen kapasiteetin aikaraja** -kenttään `30`.
6. Laajenna **Aikarajat päivissä** -osa.
7. Valitse **Kapasiteetti**-kentässä **Kyllä**.
8. Syötä **Kapasiteetin aikataulutuksen aikaraja (päivää)** -kenttään numero. Esimerkki: `60`  
9. Valitse **Lasketut viiveet** -kentässä **Kyllä**.
10. Syötä **Laskettujen viiveiden aikaraja (päivää)** -kenttään numero. Esimerkki: `60` 
11. Laajenna **Lasketut viiveet** -osa.
12. Valitse kaikissa **Lisää laskettu viive tarvepäivämäärään** -kentissä **Kyllä**.
13. Sulje sivu.

## <a name="create-a-constrained-plan"></a>Rajoitetun suunnitelman luominen
1. Valitse **Suorita**.
2. Kirjoita tai valitse **Pääsuunnitelma**-kentässä suunnitelma, jolle olet määrittänyt rajoituksia.  
3. Valitse **OK**.
4. Valitse **Suunnitellut tilaukset**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]