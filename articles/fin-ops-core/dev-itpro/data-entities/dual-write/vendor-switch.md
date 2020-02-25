---
title: Toimittajan mallien välillä siirtyminen
description: Tässä aiheessa käsitellään kuinka vaihtaa toimittajan tietojen integrointia Finance and Operations -sovellusten ja Common Data Servicen välillä.
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
ms.openlocfilehash: 587a9b98f28b11e303aff4b59e9726f220d956eb
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019753"
---
# <a name="switch-between-vendor-designs"></a>Toimittajan mallien välillä siirtyminen

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

## <a name="vendor-data-flow"></a>Toimittajatietojen virta 

Jos käytät muita Dynamics 365 -sovelluksia toimittajatietojen päähallintaan ja haluat eristää toimittajan tiedot asiakastiedoista, käytä tätä perustoimittajarakennetta.  

![Toimittajan perustyönkulku](media/dual-write-vendor-data-flow.png)
 
Jos käytät Dynamics 365 -sovelluksia toimittajatietojen päähallintaan ja jatkat toimittajan tietojen tallentamista **Tili**-yksikköön, käytä tätä uutta laajennettua toimittajarakennetta. Tässä rakenteessa laajennetut toimittajatiedot, kuten toimittajan pidossaolotila ja toimittajan profiili, tallennetaan **toimittajat**-yksikköön Common Data Servicessa. 

![Laajennettu toimittajatyönkulku](media/dual-write-vendor-detail.jpg)
 
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
    5. Aktivoi **Tili**- ja **Toimittaja**-yksiköissä luodut työnkulut ja aloita **Tili**-yksikön käyttäminen toimittajatietojen tallentamiseen. 
 
