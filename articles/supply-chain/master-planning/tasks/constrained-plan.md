---
title: Rajoitetun suunnitelman luominen
description: Tässä aiheessa kerrotaan, miten luodaan suunnitelma, jossa huomioidaan sekä kapasiteetti- ja materiaalirajoitukset.
author: ShylaThompson
manager: AnnBe
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, ReqPlanSched
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 126122d7be36cf1585f372adbae3ced8d6b15134
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/18/2020
ms.locfileid: "3150352"
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

