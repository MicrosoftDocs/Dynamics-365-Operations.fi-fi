---
title: Toimittajan mallien välillä siirtyminen
description: ''
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 09/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-09-20
ms.openlocfilehash: 4e97ff0b0e6195b5e3703e15a0bb0de7644ef8d1
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/06/2019
ms.locfileid: "2772361"
---
# <a name="switch-between-vendor-designs"></a>Toimittajan mallien välillä siirtyminen

[!include [banner](../includes/banner.md)]

## <a name="vendor-data-flow"></a>Toimittajatietojen virta 

Jos käytät muita Dynamics 365 -sovelluksia toimittajatietojen päähallintaan ja haluat eristää toimittajan tiedot asiakastiedoista, käytä tätä perustoimittajarakennetta.  

![Toimittajan perustyönkulku](media/dual-write-switch-1.png)
 
Jos käytät Dynamics 365 -sovelluksia toimittajatietojen päähallintaan ja jatkat toimittajan tietojen tallentamista **Tili**-yksikköön, käytä tätä uutta laajennettua toimittajarakennetta. Tässä rakenteessa laajennetut toimittajatiedot, kuten toimittajan pidossaolotila ja toimittajan profiili, tallennetaan **toimittajat**-yksikköön Common Data Servicessa. 

![Laajennettu toimittajatyönkulku](media/dual-write-switch-2.png)
 
Käytä laajennettua toimittajarakennetta seuraavien ohjeiden mukaisesti: 
 
1. **SupplyChainCommon**-ratkaisupaketti sisältää työnkulun prosessimallit, jotka näkyvät seuraavassa kuvassa.
    > [!div class="mx-imgBorder"]
    > ![Työnkulun prosessimallit](media/dual-write-switch-3.png)
2. Uusien työnkulkuprosessien luominen työnkulun prosessimallien avulla: 
    1. Luo **Toimittaja**-yksikön uusi työnkulkuprosessi käyttämällä työnkulun **Luo toimittajia tiliyksikössä** -prosessimallia ja valitse **OK**. Tämä työnkulku käsittelee **Tilli**-yksikön toimittajan luontiskenaarion.
        > [!div class="mx-imgBorder"]
        > ![Toimittajien luonti Tili-yksikössä](media/dual-write-switch-4.png)
    2. Luo **Toimittaja**-yksikön uusi työnkulkuprosessi käyttämällä työnkulun **Päivitä tiliyksikkö** -prosessimallia ja valitse **OK**. Tämä työnkulku käsittelee **Tilli**-yksikön toimittajan päivitysskenaarion. 
        > [!div class="mx-imgBorder"]
        > ![Tiliyksikön päivittäminen](media/dual-write-switch-5.png)
    3. Luo uusia työnkulkuprosesseja **Tilit**-yksikössä luoduista malleista. 
        > [!div class="mx-imgBorder"]
        > ![Toimittajien luonti toimittajat-yksikössä](media/dual-write-switch-6.png)
        > [!div class="mx-imgBorder"]
        > ![Toimittajat-yksikön päivittäminen](media/dual-write-switch-7.png)
    4. Voit määrittää työnkulut tarpeen mukaan reaaliaikaisiksi tai taustatyönkuluiksi. 
        > [!div class="mx-imgBorder"]
        > ![Taustatyönkuluksi muuntaminen](media/dual-write-switch-8.png)
    5. Aktivoi **Tili**- ja **Toimittaja**-yksiköissä luodut työnkulut ja aloita Customer Engagementin **Tili**-yksikön käyttäminen toimittajatietojen tallentamiseen. 
 
