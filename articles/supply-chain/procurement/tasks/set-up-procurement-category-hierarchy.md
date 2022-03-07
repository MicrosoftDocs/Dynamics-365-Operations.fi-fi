---
title: Määritä hankintaluokkahierarkia
description: Tässä menettelyssä selvitetään, miten voit luoda uusia solmuja hankintaluokkahierarkiaan ja miten hankintaprosessissa käytettävä hankintaluokka määritetään.
author: RichardLuan
manager: tfehr
ms.date: 06/21/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 44fd02d37ec4e6431ca25dc980ed1d1785e45fac
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5239347"
---
# <a name="set-up-a-procurement-category-hierarchy"></a>Määritä hankintaluokkahierarkia

[!include [banner](../../includes/banner.md)]

Tässä menettelyssä selvitetään, miten voit luoda uusia solmuja hankintaluokkahierarkiaan ja miten hankintaprosessissa käytettävä hankintaluokka määritetään. Yleensä ostopäällikkö tekee nämä tehtävät. Ennen menettelyn aloittamista on oltava Hankita-tyyppinen luokkahierarkia. Jos käytössä on demotietoyritys, voit suorittaa tämän menettelyn USMF-yrityksessä.


## <a name="add-a-new-procurement-category"></a>Lisää uusi hankintaluokka
1. Siirry kohtaan **Siirtymisruutu > Moduulit > Hankinta > Tavaralähetys > Hankintaluokat**.
2. Valitse toimintoruudussa **Muokkaa luokkahierarkiaa**. Nykyisen hankintaluokkahierarkia näkyy sivun vasemmalla puolella. Olet muokkaamassa hierarkiaa.  
3. Valitse toimintoruudussa **Uusi luokkasolmu**. Järjestelmä valitsee oletusarvoisesti ylimmän solmun. Jos käytät menettelyä tehtävän ohjauksena, voit napsauttaa Poista lukitus -painiketta ja valita toisen pääsolmun, johon voit lisätä uuden solmun. Kun tämä on tehty, lukitse tehtäväopas uudelleen ja napsauta Uusi luokka -solmua.  
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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]