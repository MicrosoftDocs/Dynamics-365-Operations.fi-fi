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
ms.openlocfilehash: eb37b2761708770b82f23cfbed86248d30a59410
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/16/2021
ms.locfileid: "5017314"
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
