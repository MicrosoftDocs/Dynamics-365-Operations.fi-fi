---
title: Sivujen näyttäminen rinnakkain Avaa uudessa ikkunassa -toiminnon avulla
description: Tässä artikkelissa kerrotaan, miten sivut voidaan näyttää rinnakkain.
author: aneesmsft
manager: AnnBe
ms.date: 11/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.custom: 17611
ms.assetid: fc589d76-3927-4486-ab83-e86b9b47ba2c
ms.search.region: Global
ms.author: aneesa
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5b770fe44e4e12c515ca53def697fa345ce3eba3
ms.sourcegitcommit: f5e31c34640add6d40308ac1365cc0ee60e60e24
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/08/2020
ms.locfileid: "4694442"
---
# <a name="show-pages-side-by-side-using-the-open-in-new-window-feature"></a>Sivujen näyttäminen rinnakkain Avaa uudessa ikkunassa -toiminnon avulla

[!include [banner](../includes/banner.md)]

Tässä artikkelissa kerrotaan, miten sivut voidaan näyttää rinnakkain.

Joskus tehtäviä halutaan suorittaa nopeasti ja tarkastella useita sivuja rinnakkain. Voit esimerkiksi haluta tarkistaa usean kirjauskansion rivejä tai syöttää niitä useaan kirjauskansioon. Yleensä oikeellisuustarkistuksen tekeminen tai rivien syöttäminen useampaan kuin yhteen kirjauskansioon vaatii palaamisen kirjauskansioluettelon sisältävälle sivulle ja takaisin tietyn kirjauskansion sisältävälle sivulle. **Avaa uudessa ikkunassa** -toiminnon avulla voit kuitenkin näyttää nämä sivut rinnakkain, jolloin tehtävien suorittaminen nopeutuu.

Kun haluat tarkastella rivejä, voit valita **Avaa uudessa ikkunassa** -kuvakkeen.

[![Napauta Avaa uudessa ikkunassa -kuvaketta.](./media/open-in-new-window-icon.png)](./media/open-in-new-window-icon.png)

Kun **Avaa uudessa ikkunassa** -kuvake valitaan, rivien sivu avataan uudessa selainikkunassa ponnahdusikkunana. Tämän jälkeen siirrytään takaisin alkuperäisen selaimen aiemmalle sivulle, joka on kirjauskansioluettelon sisältävä sivu. Tämän jälkeen sivut voidaan näyttää rinnakkain. Kun kirjauskansion tarkasteleminen on tehty, voit muuttaa kirjauskansiovalinnan kirjauskansioluettelosivulla. Tällöin ponnahdusikkunan rivien sivulla näytetään automaattisesti juuri valitun kirjauskansion rivit.

[![Sivut voidaan näyttää rinnakkain.](./media/pages-show-side-by-side.png)](./media/pages-show-side-by-side.png)

Dynaaminen linkitys ja päivittäminen tapahtuu näiden sivujen taustalla olevien tietojen suhteiden vuoksi. Jos järjestelmä ei ota huomioon tietojen välisiä suhteita, ponnahdusikkunaa ei päivitetä automaattisesti alkuperäisessä ikkunassa tehtävien muutosten perusteella.

Joillakin sivuilla on useita näkymiä, kuten ruudukko-, otsikko- ja tietonäkymä. **Avaa uudessa ikkunassa** -kuvake avaa koko sivun uudessa selainikkunassa. Tämän vuoksi **Avaa uudessa ikkunassa** -toiminnon avulla samaa sivua ei voi näyttää rinnakkain. Melkein kaikilla tällaisilla sivuilla on kuitenkin siirtymisluettelo, jonka avulla tietueiden välillä voi siirtyä. Tällöin käyttökokemus on samanlainen.

Määritä selaimen ponnahdusikkunoiden estotoiminto sallimaan ponnahdusikkunat sivuston URL-osoitteesta, ennen kuin käytät **Avaa uudessa ikkunassa** -toimintoa. Ponnahdusikkunat voidaan sallia esimerkiksi osoitteesta \*.dynamics.com.

**Avaa uudessa ikkunassa** -toiminto on käytettävissä vain, kun ikkunassa on avoinna useita sivuja. Ponnahdusikkunan suljetaan automaattisesti, kun sivuja ei ole enää avoinna (eli sitten, kun ikkunan viimeinen sivu suljetaan). Järjestelmä sulkee sivut myös silloin, kun siirryt sovelluksen toiselle alueelle. Jos ponnahdusikkunoita siis on avoinna silloin, kun siirryt sovelluksen toiselle alueelle, ponnahdusikkunat suljetaan automaattisesti, koska järjestelmä sulkee ikkunoissa olevat sivut.

Ponnahdusikkunoiden yläpalkeissa on tietoja yrityksestä, jolle sivu on avattu. Tiedot ovat vain luku -muodossa. Ponnahdusikkunat ovat riippuvaisia myös selainikkunasta. Jos pääikkuna suljetaan tai päivitetään, kaikki avoimet ponnahdusikkunat siirtyvät vain luku -tilaan. Jos näin tapahtuu, voit yhä tarkastella ikkunoiden tietoja, mutta et voi käsitellä niitä.
