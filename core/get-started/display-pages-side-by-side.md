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
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 940d086f9c99af54bfcc7911ee7272f9eccba464
ms.lasthandoff: 03/31/2017


---

# <a name="display-pages-side-by-side-using-the-open-in-new-window-icon"></a>Rinnakkaisten sivujen näyttäminen Avaa uudessa ikkunassa -kuvakkeen avulla

Tässä artikkelissa kerrotaan, miten sivut näytetään rinnakkain Microsoft Dynamics 365 for Operations -järjestelmässä.

Microsoft Dynamics 365 for Operations -järjestelmän avulla voit suorittaa tehtäviä tehokkaasti. Joskus haluat ehkä suorittaa tehtäviä nopeasti ja tarkastella useita sivuja rinnakkain. Voit esimerkiksi haluta tarkistaa usean kirjauskansion rivejä tai syöttää niitä useaan kirjauskansioon. Yleensä tämä vaatii palaamisen kirjauskansioluettelon sisältävälle sivulle ja takaisin tietyn kirjauskansion sisältävälle sivulle. **Avaa uudessa ikkunassa** -toiminnon avulla voit kuitenkin näyttää nämä sivut rinnakkain, jolloin tehtävien suorittaminen nopeutuu. Kun haluat tarkastella rivejä, voit valita **Avaa uudessa ikkunassa** -kuvakkeen. [![Avaa-,-uusi-ikkuna-kuvake](./media/open-in-new-window-icon.png)](./media/open-in-new-window-icon.png) Clicking **Avaa uudessa ikkunassa** kuvake sivu avautuu selaimessa uuteen, ponnahdusikkunoiden ja siirtyy sitten takaisin alkuperäiseen selaimen historia sivulle, joka näyttää kirjauskansioiden luettelo. Tämän jälkeen sivut voidaan näyttää rinnakkain. Kun kirjauskansion tarkasteleminen on tehty, voit muuttaa kirjauskansiovalinnan kirjauskansioluettelosivulla. Tällöin ponnahdusikkunan rivien sivulla näytetään automaattisesti juuri valitun kirjauskansion rivit. [![sivut-Näytä---rinnakkain](./media/pages-show-side-by-side.png)](./media/pages-show-side-by-side.png) dynaamista linkitystä ja päivittäminen tapahtuu, koska suhteet, jotka välillä varmuuskopioiminen on näillä sivuilla olevat tiedot. Jos järjestelmä ei ota huomioon tietojen välisiä suhteita, ponnahdusikkunaa ei päivitetä automaattisesti alkuperäisessä ikkunassa tehtävien muutosten perusteella. Joillakin sivuilla on useita näkymiä, kuten ruudukko-, otsikko- ja tietonäkymä. **Avaa uudessa ikkunassa** -kuvake avaa koko sivun uudessa selainikkunassa. Tämän vuoksi **Avaa uudessa ikkunassa** -toiminnon avulla samaa sivua ei voi näyttää rinnakkain. Melkein kaikilla tällaisilla sivuilla on kuitenkin siirtymisluettelo, jonka avulla tietueiden välillä voi siirtyä. Tällöin käyttökokemus on samanlainen. Määritä selaimen ponnahdusikkunoiden estotoiminto sallimaan ponnahdusikkunat Dynamics 365 for Operations -sivuston URL-osoitteesta, ennen kuin käytät **Avaa uudessa ikkunassa** -toimintoa. Esimerkiksi saattaa sallia ponnahdusikkunat "\*. dynamics.com". **Avaa uudessa ikkunassa** -toiminto on käytettävissä vain, kun ikkunassa on avoinna useita sivuja. Ponnahdusikkunan suljetaan automaattisesti, kun sivuja ei ole enää avoinna (eli sitten, kun ikkunan viimeinen sivu suljetaan). Dynamics 365 for Operations sulkee sivut myös silloin, kun siirryt sovelluksen toiselle alueelle. Jos ponnahdusikkunoita siis on avoinna silloin, kun siirryt sovelluksen toiselle alueelle, ponnahdusikkunat suljetaan automaattisesti, koska järjestelmä sulkee ikkunoissa olevat sivut. Ponnahdusikkunoiden yläpalkeissa on tietoja yrityksestä, jolle sivu on avattu. Tiedot ovat vain luku -muodossa. Ponnahdusikkunat ovat riippuvaisia myös Dynamics 365 for Operations -selainikkunasta. Jos pääikkuna suljetaan tai päivitetään, kaikki avoimet ponnahdusikkunat siirtyvät vain luku -tilaan. Tällöin voit yhä tarkastella ikkunoiden tietoja, mutta et voi käsitellä niitä.


