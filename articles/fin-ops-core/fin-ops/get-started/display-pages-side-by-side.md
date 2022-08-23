---
title: Sivujen näyttäminen rinnakkain Avaa uudessa ikkunassa -toiminnon avulla
description: Tässä artikkelissa kerrotaan, miten sivut voidaan näyttää rinnakkain.
author: jasongre
ms.date: 11/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 17611
ms.assetid: fc589d76-3927-4486-ab83-e86b9b47ba2c
ms.openlocfilehash: bfc2aa534da17529421af0a28d1c90ee3aeb40cb
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9288628"
---
# <a name="show-pages-side-by-side-using-the-open-in-new-window-feature"></a>Sivujen näyttäminen rinnakkain Avaa uudessa ikkunassa -toiminnon avulla

[!include [banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

Tässä artikkelissa käsitellään sivujen näyttämistä rinnakkain.

Joskus tehtäviä halutaan suorittaa nopeasti tarkastelemalla useita sivuja rinnakkain. Voit esimerkiksi haluta tarkistaa usean kirjauskansion rivejä tai syöttää niitä useaan kirjauskansioon. Yleensä oikeellisuustarkistuksen tekeminen tai rivien syöttäminen useampaan kuin yhteen kirjauskansioon vaatii palaamisen kirjauskansioluettelon sisältävälle sivulle ja takaisin tietyn kirjauskansion sisältävälle sivulle. **Avaa uudessa ikkunassa** -toiminnon avulla voit kuitenkin näyttää nämä sivut rinnakkain, jolloin tehtävien suorittaminen nopeutuu.

Kun haluat tarkastella rivejä, voit valita **Avaa uudessa ikkunassa** -kuvakkeen.

[![Napauta Avaa uudessa ikkunassa -kuvaketta.](./media/open-in-new-window-icon.png)](./media/open-in-new-window-icon.png)

Kun **Avaa uudessa ikkunassa** -kuvake valitaan, rivien sivu avataan uudessa selainikkunassa ponnahdusikkunana. Tämän jälkeen siirrytään takaisin alkuperäisen selaimen aiemmalle sivulle, joka on kirjauskansioluettelon sisältävä sivu. Tämän jälkeen sivut voidaan näyttää rinnakkain. Kirjauskansion tarkastelemisen jälkeen voit muuttaa kirjauskansiovalinnan kirjauskansioluettelosivulla. Tällöin ponnahdusikkunan rivien sivulla näytetään automaattisesti juuri valitun kirjauskansion rivit.

[![Sivut voidaan näyttää rinnakkain.](./media/pages-show-side-by-side.png)](./media/pages-show-side-by-side.png)

Dynaaminen linkitys ja päivittäminen tapahtuu näiden sivujen taustalla olevien tietojen suhteiden vuoksi. Jos järjestelmä ei ota huomioon tietojen välisiä suhteita, ponnahdusikkunaa ei päivitetä automaattisesti alkuperäisessä ikkunassa tehtävien muutosten perusteella.

Joillakin sivuilla on useita näkymiä, kuten ruudukko-, otsikko- ja tietonäkymä. **Avaa uudessa ikkunassa** -kuvake avaa koko sivun uudessa selainikkunassa. Tämän vuoksi **Avaa uudessa ikkunassa** -toiminnon avulla kahta saman sivun näkymää ei voi näyttää rinnakkain. Melkein kaikilla tällaisilla sivuilla on siirtymisluettelo, jonka avulla tietueiden välillä voi siirtyä. Tällöin käyttökokemus on samanlainen.

Määritä selaimen ponnahdusikkunoiden estotoiminto sallimaan ponnahdusikkunat sivuston URL-osoitteesta, ennen kuin käytät **Avaa uudessa ikkunassa** -toimintoa. Ponnahdusikkunat voidaan sallia esimerkiksi osoitteesta \*.dynamics.com.

**Avaa uudessa ikkunassa** -toiminto on käytettävissä vain, kun ikkunassa on avoinna useita sivuja. Ponnahdusikkuna suljetaan automaattisesti, kun sivuja ei ole enää avoinna (eli sitten, kun ikkunan viimeinen sivu suljetaan). Järjestelmä sulkee sivut myös silloin, kun siirryt sovelluksen toiselle alueelle. Niinpä jos ponnahdusikkunoita on avoinna silloin, kun siirryt sovelluksen toiselle alueelle, ponnahdusikkunat sulkeutuvat automaattisesti, koska järjestelmä sulki ikkunoissa olevat sivut.

Ponnahdusikkunoiden yläpalkeissa on tietoja yrityksestä, jolle sivu on avattu. Tiedot ovat vain luku -muodossa. Ponnahdusikkunat ovat riippuvaisia myös selainikkunasta. Jos pääikkuna suljetaan tai päivitetään, kaikki avoimet ponnahdusikkunat siirtyvät vain luku -tilaan. Jos näin tapahtuu, voit yhä tarkastella ikkunoiden tietoja, mutta et voi käsitellä niitä.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
