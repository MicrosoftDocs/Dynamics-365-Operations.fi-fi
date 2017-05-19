---
title: "Rinnakkaisten sivujen näyttäminen Avaa uudessa ikkunassa -kuvakkeen avulla"
description: "Tässä artikkelissa kerrotaan, miten sivut näytetään rinnakkain Microsoft Dynamics 365 for Operations -järjestelmässä."
author: aneesmsft
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 17611
ms.assetid: fc589d76-3927-4486-ab83-e86b9b47ba2c
ms.search.region: Global
ms.author: aneesa
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: e29d436560590e844e92180a6d1e2ad53d019662
ms.contentlocale: fi-fi
ms.lasthandoff: 04/25/2017


---

# <a name="display-pages-side-by-side-using-the-open-in-new-window-icon"></a>Rinnakkaisten sivujen näyttäminen Avaa uudessa ikkunassa -kuvakkeen avulla

[!include[banner](../includes/banner.md)]


Tässä artikkelissa kerrotaan, miten sivut näytetään rinnakkain Microsoft Dynamics 365 for Operations -järjestelmässä.

Microsoft Dynamics 365 for Operations -järjestelmän avulla voit suorittaa tehtäviä tehokkaasti. Joskus haluat ehkä suorittaa tehtäviä nopeasti ja tarkastella useita sivuja rinnakkain. Voit esimerkiksi haluta tarkistaa usean kirjauskansion rivejä tai syöttää niitä useaan kirjauskansioon. Yleensä tämä vaatii palaamisen kirjauskansioluettelon sisältävälle sivulle ja takaisin tietyn kirjauskansion sisältävälle sivulle. **Avaa uudessa ikkunassa** -toiminnon avulla voit kuitenkin näyttää nämä sivut rinnakkain, jolloin tehtävien suorittaminen nopeutuu. Kun haluat tarkastella rivejä, voit valita **Avaa uudessa ikkunassa** -kuvakkeen. [![open-in-new-window-icon](./media/open-in-new-window-icon.png)](./media/open-in-new-window-icon.png) Kun **Avaa uudessa ikkunassa** -kuvake valitaan, rivien sivu avataan uudessa selainikkunassa ponnahdusikkunana. Tämän jälkeen siirrytään takaisin alkuperäisen selaimen aiemmalle sivulle, joka on kirjauskansioluettelon sisältävä sivu. Tämän jälkeen sivut voidaan näyttää rinnakkain. Kun kirjauskansion tarkasteleminen on tehty, voit muuttaa kirjauskansiovalinnan kirjauskansioluettelosivulla. Tällöin ponnahdusikkunan rivien sivulla näytetään automaattisesti juuri valitun kirjauskansion rivit. [![pages-show-side-by-side](./media/pages-show-side-by-side.png)](./media/pages-show-side-by-side.png) Dynaaminen linkitys ja päivittäminen tapahtuu näiden sivujen taustalla olevien tietojen suhteiden vuoksi. Jos järjestelmä ei ota huomioon tietojen välisiä suhteita, ponnahdusikkunaa ei päivitetä automaattisesti alkuperäisessä ikkunassa tehtävien muutosten perusteella. Joillakin sivuilla on useita näkymiä, kuten ruudukko-, otsikko- ja tietonäkymä. **Avaa uudessa ikkunassa** -kuvake avaa koko sivun uudessa selainikkunassa. Tämän vuoksi **Avaa uudessa ikkunassa** -toiminnon avulla samaa sivua ei voi näyttää rinnakkain. Melkein kaikilla tällaisilla sivuilla on kuitenkin siirtymisluettelo, jonka avulla tietueiden välillä voi siirtyä. Tällöin käyttökokemus on samanlainen. Määritä selaimen ponnahdusikkunoiden estotoiminto sallimaan ponnahdusikkunat Dynamics 365 for Operations -sivuston URL-osoitteesta, ennen kuin käytät **Avaa uudessa ikkunassa** -toimintoa. Ponnahdusikkunat voidaan sallia esimerkiksi osoitteesta \*.dynamics.com. **Avaa uudessa ikkunassa** -toiminto on käytettävissä vain, kun ikkunassa on avoinna useita sivuja. Ponnahdusikkunan suljetaan automaattisesti, kun sivuja ei ole enää avoinna (eli sitten, kun ikkunan viimeinen sivu suljetaan). Dynamics 365 for Operations sulkee sivut myös silloin, kun siirryt sovelluksen toiselle alueelle. Jos ponnahdusikkunoita siis on avoinna silloin, kun siirryt sovelluksen toiselle alueelle, ponnahdusikkunat suljetaan automaattisesti, koska järjestelmä sulkee ikkunoissa olevat sivut. Ponnahdusikkunoiden yläpalkeissa on tietoja yrityksestä, jolle sivu on avattu. Tiedot ovat vain luku -muodossa. Ponnahdusikkunat ovat riippuvaisia myös Dynamics 365 for Operations -selainikkunasta. Jos pääikkuna suljetaan tai päivitetään, kaikki avoimet ponnahdusikkunat siirtyvät vain luku -tilaan. Tällöin voit yhä tarkastella ikkunoiden tietoja, mutta et voi käsitellä niitä.




