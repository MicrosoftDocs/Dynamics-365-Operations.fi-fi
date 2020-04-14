---
title: Määritä hankintaluokkahierarkia
description: Tässä menettelyssä selvitetään, miten voit luoda uusia solmuja hankintaluokkahierarkiaan ja miten hankintaprosessissa käytettävä hankintaluokka määritetään.
author: mkirknel
manager: AnnBe
ms.date: 06/21/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c7010fb702d16dc276bfee397066ccf95bf5d25a
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/18/2020
ms.locfileid: "3147270"
---
# <a name="set-up-a-procurement-category-hierarchy"></a>Määritä hankintaluokkahierarkia

[!include [banner](../../includes/banner.md)]

Tässä menettelyssä selvitetään, miten voit luoda uusia solmuja hankintaluokkahierarkiaan ja miten hankintaprosessissa käytettävä hankintaluokka määritetään. Yleensä ostopäällikkö tekee nämä tehtävät. Ennen menettelyn aloittamista on oltava Hankita-tyyppinen luokkahierarkia. Jos käytössä on demotietoyritys, voit suorittaa tämän menettelyn USMF-yrityksessä.


## <a name="add-a-new-procurement-category"></a>Lisää uusi hankintaluokka
1. Siirry kohtaan **Siirtymisruutu > Moduulit > Hankinta > Tavaralähetys > Hankintaluokat**.
2. Valitse toimintoruudusta **Muokkaa luokkahierarkiaa**. Nykyisen hankintaluokkahierarkia näkyy sivun vasemmalla puolella. Olet muokkaamassa hierarkiaa.  
3. Valitse toimintoruudusta **Uusi luokkasolmu**. Järjestelmä valitsee oletusarvoisesti ylimmän solmun. Jos käytät menettelyä tehtävän ohjauksena, voit napsauttaa Poista lukitus -painiketta ja valita toisen pääsolmun, johon voit lisätä uuden solmun. Kun tämä on tehty, lukitse tehtäväopas uudelleen ja napsauta Uusi luokka -solmua.  
4. Kirjoita arvo **Nimi**-kenttään.
5. Kirjoita **Kuvaus**-kenttään arvo.
6. Kirjoita **Kutsumanimi**-kenttään arvo. Kutsumanimi on valinnainen. Se näkyy luokkahauissa yhdessä luokan nimen kanssa.  
7. Valitse **Tallenna**.

## <a name="add-products-to-your-new-procurement-category"></a>Lisää tuotteita uuteen hankintaluokkaan
1. Siirry kohtaan **Hankinta > Tavaralähetys > Hankintaluokat**. Valitse juuri lisäämäsi solmu. Jos käytät menettelyä tehtävän ohjauksena, sinun on ehkä poistettava lukitus, ennen kuin voit valita solmun.  
2. Ota **Tuotteet**-osion laajennus käyttöön.
3. Liitä tuotteet hankintaluokkaan valitsemalla **Lisää**.
4. Valitse hankintaluokkaan lisättävät tuotteet.
5. Lisää tuotteet **Valitut**-taulukkoon nuolen avulla.
6. Valitse **OK**.
