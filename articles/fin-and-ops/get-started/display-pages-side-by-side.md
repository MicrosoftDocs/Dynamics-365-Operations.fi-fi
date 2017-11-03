---
title: "Rinnakkaisten sivujen näyttäminen Avaa uudessa ikkunassa -kuvakkeen avulla"
description: "Tässä artikkelissa kerrotaan, miten sivut näytetään rinnakkain Microsoft Dynamics 365 for Finance and Operationsissa."
author: aneesmsft
manager: AnnBe
ms.date: 09/07/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 17611
ms.assetid: fc589d76-3927-4486-ab83-e86b9b47ba2c
ms.search.region: Global
ms.author: aneesa
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: b375e87af24a17633d6d1590277ece9e2df189da
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---

# <a name="display-pages-side-by-side-using-the-open-in-new-window-icon"></a>Rinnakkaisten sivujen näyttäminen Avaa uudessa ikkunassa -kuvakkeen avulla

[!include[banner](../includes/banner.md)]


Tässä artikkelissa kerrotaan, miten sivut näytetään rinnakkain Microsoft Dynamics 365 for Finance and Operationsissa.

Microsoft Dynamics 365 for Finance and Operationsin avulla voit suorittaa tehtäviä tehokkaasti. Joskus haluat ehkä suorittaa tehtäviä nopeasti ja tarkastella useita sivuja rinnakkain. Voit esimerkiksi haluta tarkistaa usean kirjauskansion rivejä tai syöttää niitä useaan kirjauskansioon. Yleensä tämä vaatii palaamisen kirjauskansioluettelon sisältävälle sivulle ja takaisin tietyn kirjauskansion sisältävälle sivulle. **Avaa uudessa ikkunassa** -toiminnon avulla voit kuitenkin näyttää nämä sivut rinnakkain, jolloin tehtävien suorittaminen nopeutuu. 

Kun haluat tarkastella rivejä, voit valita **Avaa uudessa ikkunassa** -kuvakkeen. 

[![open-in-new-window-icon](./media/open-in-new-window-icon.png)](./media/open-in-new-window-icon.png) 

Kun **Avaa uudessa ikkunassa** -kuvake valitaan, rivien sivu avataan uudessa selainikkunassa ponnahdusikkunana. Tämän jälkeen siirrytään takaisin alkuperäisen selaimen aiemmalle sivulle, joka on kirjauskansioluettelon sisältävä sivu. Tämän jälkeen sivut voidaan näyttää rinnakkain. Kun kirjauskansion tarkasteleminen on tehty, voit muuttaa kirjauskansiovalinnan kirjauskansioluettelosivulla. Tällöin ponnahdusikkunan rivien sivulla näytetään automaattisesti juuri valitun kirjauskansion rivit. 

[![pages-show-side-by-side](./media/pages-show-side-by-side.png)](./media/pages-show-side-by-side.png) 

Dynaaminen linkitys ja päivittäminen tapahtuu näiden sivujen taustalla olevien tietojen suhteiden vuoksi. Jos järjestelmä ei ota huomioon tietojen välisiä suhteita, ponnahdusikkunaa ei päivitetä automaattisesti alkuperäisessä ikkunassa tehtävien muutosten perusteella. 

Joillakin sivuilla on useita näkymiä, kuten ruudukko-, otsikko- ja tietonäkymä. **Avaa uudessa ikkunassa** -kuvake avaa koko sivun uudessa selainikkunassa. Tämän vuoksi **Avaa uudessa ikkunassa** -toiminnon avulla samaa sivua ei voi näyttää rinnakkain. Melkein kaikilla tällaisilla sivuilla on kuitenkin siirtymisluettelo, jonka avulla tietueiden välillä voi siirtyä. Tällöin käyttökokemus on samanlainen. 

Määritä selaimen ponnahdusikkunoiden estotoiminto sallimaan ponnahdusikkunat Finance and Operations -sivuston URL-osoitteesta, ennen kuin käytät **Avaa uudessa ikkunassa** -toimintoa. Ponnahdusikkunat voidaan sallia esimerkiksi osoitteesta \*.dynamics.com. 

**Avaa uudessa ikkunassa** -toiminto on käytettävissä vain, kun ikkunassa on avoinna useita sivuja. Ponnahdusikkunan suljetaan automaattisesti, kun sivuja ei ole enää avoinna (eli sitten, kun ikkunan viimeinen sivu suljetaan). Finance and Operations sulkee sivut myös silloin, kun siirryt sovelluksen toiselle alueelle. Jos ponnahdusikkunoita siis on avoinna silloin, kun siirryt sovelluksen toiselle alueelle, ponnahdusikkunat suljetaan automaattisesti, koska järjestelmä sulkee ikkunoissa olevat sivut. 

Ponnahdusikkunoiden yläpalkeissa on tietoja yrityksestä, jolle sivu on avattu. Tiedot ovat vain luku -muodossa. Ponnahdusikkunat ovat riippuvaisia myös Finance and Operations -selainikkunasta. Jos pääikkuna suljetaan tai päivitetään, kaikki avoimet ponnahdusikkunat siirtyvät vain luku -tilaan. Tällöin voit yhä tarkastella ikkunoiden tietoja, mutta et voi käsitellä niitä.




