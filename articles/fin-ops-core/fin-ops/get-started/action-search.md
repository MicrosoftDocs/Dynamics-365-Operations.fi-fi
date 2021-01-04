---
title: Toimintohaku
description: Tässä artikkelissa käsitellään toimintohakutoimintoa. Toimintohaku auttaa sinua löytämään ja suorittamaan toimintoja sivulla.
author: jasongre
manager: AnnBe
ms.date: 03/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.custom: 62303
ms.assetid: 62c70de0-fdde-4417-8e08-0583fb095a40
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8b5d2e678b01f052db29d5a1c47eae27d27cd04f
ms.sourcegitcommit: f5e31c34640add6d40308ac1365cc0ee60e60e24
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/08/2020
ms.locfileid: "4694185"
---
# <a name="action-search"></a>Toimintohaku

[!include [banner](../includes/banner.md)]

Tässä artikkelissa käsitellään toimintohakutoimintoa. Toimintohaku auttaa sinua löytämään ja suorittamaan toimintoja sivulla.

## <a name="introduction"></a>Johdanto

Sivuilla näytetään ensisijaisesti toimintoruutujen komennot sekä vakiotoimintoruudussa, joka näkyy sivun yläreunassa, että työkaluriveillä, jotka näkyvät sivun eri osissa. Aiemmissa versioissa Päävihjeet-toiminnon avulla pystyit nopeasti käyttämään mitä tahansa toimintoruudun painiketta painamalla Alt-näppäintä ja sitten sarjan kirjaimia.

[![keyTipsAX6](./media/keytipsax6.png)](./media/keytipsax6.png)

Päävihjeet eivät ole enää käytettävissä, vaan niiden tilalla on toimintohakutoiminto. Tämän uuden ominaisuuden avulla voit nopeasti etsiä ja suorittaa painikkeen mistä tahansa näkyvillä olevasta toimintoruudusta.

## <a name="using-action-search"></a>Toimintohaun käyttö

Suorita seuraavat vaiheet, kun haluat käyttää toimintohaku-ominaisuutta:

1. Valitse toimintoruudussa **toimintohaku**-kenttää. (**toimintohaku**-kentässä on suurennuslasikuvake.)
2. Kirjoita sen painikkeen nimi (tai osa nimestä), jonka haluat suorittaa. Voit myös etsiä käyttämällä sanoja painikkeen "polusta". (Lisätietoja on tämän artikkelin seuraavassa osassa.) Yleensä painike näkyy tulosluettelon yläosassa sen jälkeen, kun olet kirjoittanut merkit kahdesta neljään.
3. Etsi ja suorita painike tulosluettelossa (käyttämällä hiirtäsi tai näppäimistöä).

Kun painike on suoritettu, huomio palautuu viimeiseen toimeesi sivulla niin, että voit jatkaa työskentelyä.

[![action-search-field](./media/action-search-field.png)](./media/action-search-field.png)

Voit myös aloittaa toiminnon painamalla näppäinyhdistelmää Ctrl+/ tai Alt+Q. Paina pikanäppäintä uudelleen palataksesi edelliseen toimeesi sivulla.

## <a name="understanding-the-results-list"></a>Tulosluetteloon tutustuminen

Usein on tiedettävä sekä painikkeen sijainti että konteksti, jotta ymmärtäisit täysin painikkeen tarkoituksen. Tämän vuoksi lisätiedot on jokaisesta nimikkeestä tulosluettelossa, jotta voit ymmärtää täysin luettelossa näytettävät painikkeet. Erityisesti painikkeen "polku" näytetään. Tämä polku saattaa soveltuvin osin sisältää seuraavien käyttöliittymäelementtien otsikot:

- Toimintoruutu-välilehti
- Painikeryhmä
- Valikkopainike (jos painike on valikkopainikkeen sisällä)
- Valikon erotin (jos painike on valikkopainikkeen sisällä nimetyn ryhmän sisällä)
- Sivulla oleva ryhmä tai välilehti (esimerkiksi pikavälilehden nimi).

Kirjoitit esimerkiksi **yht** **toimintohaku**-kenttään ja tarkastelet nyt tulosluetteloa. Ensimmäinen tulosluettelon painike **Summat** näkyy korostettuna. Näet myös painikkeen, jonka polku on **Sales**&gt;**Näytä**. Polun **Myyntitilaus**-osa vastaa toimintoruudun **Myyntitilaus**-välilehteä, ja polun **Näytä**-osa vastaa kyseisen välilehden **Näytä**-ryhmää. Vastaavasti painikkeen **Kokonaisalennus**-polku (**Myy** &gt; **Laske**) ilmoittaa, että tämä painike sijaitsee **Laske**-ryhmässä toimintoruudun **Myy**-välilehdessä. Tämän vuoksi näiden tietojen avulla voit ymmärtää täsmälleen mikä painike suoritetaan toimintohaun toimesta (jos valitset kyseisen painikkeen tulosten luettelossa).

[![action-search-field-with-data](./media/action-search-field-with-data.png)](./media/action-search-field-with-data.png)

Edellisessä esimerkissä toimintohakku näytti tulokset standardimuotoisesta toimintoruudusta sivun yläreunassa. Toimintohaku kuitenkin näyttää tulokset myös näkyvillä olevista työkaluriveistä, jotka sijaitsevat muissa sivun kohdissa. Esimerkiksi etsit **Käytettävissä oleva varasto** -painiketta, joka sijaitsee **Myyntitilausrivit**-pikavälilehdessä. Tässä tapauksessa tulosten luettelossa painikkeen polku (**Myyntitilausrivit** &gt; **Varasto** &gt; **Näytä**) ilmoittaa, että tämä painike sijaitsee **Näytä**-otsikossa **Varasto**-valikkopainikkeessa **Myyntitilausrivit**-pikavälilehdessä.

[![on-hand-inventory](./media/on-hand-inventory.png)](./media/on-hand-inventory.png)

> [!NOTE]
> Jotkin painikkeet eivät näy toimintohaussa. Näitä ovat valintaikkunan ja alilomakkeiden painikkeet. 

## <a name="action-search-vs-navigation-search"></a>Toimintohaku vs. siirtymishaku

Toimintohaun tarkoituksena on etsiä ja suorittaa toimintoja sivulla, mutta sivujen etsimiseen ja niissä siirtymisessä on myös erillinen hakumekanismi. Lisätietoja tästä ominaisuudesta löydät artikkelista. [Siirtymishaku](navigation-search.md).
