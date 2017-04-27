---
title: Toiminnon haku
description: "Tässä artikkelissa kuvataan Microsoft Dynamics 365 for Operationsin toimintohakuominaisuutta. Toimintohaku auttaa sinua löytämään ja suorittamaan toimintoja sivulla."
author: jasongre
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 62303
ms.assetid: 62c70de0-fdde-4417-8e08-0583fb095a40
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 4bb647cfd3f012efbffa93a81462c538a24ac850
ms.openlocfilehash: 689d8f9fb0501c5007db21d41f126737af77b89e
ms.lasthandoff: 03/31/2017


---

# <a name="action-search"></a>Toiminnon haku

[!include[banner](../includes/banner.md)]


Tässä artikkelissa kuvataan Microsoft Dynamics 365 for Operationsin toimintohakuominaisuutta. Toimintohaku auttaa sinua löytämään ja suorittamaan toimintoja sivulla.

<a name="introduction"></a>Johdanto
------------

Microsoft Dynamics 365 for Operations näyttää ensisijaisesti komennot toimintoruuduissa – sekä vakiotoimintoruudussa, joka näkyy sivun yläreunassa, että työkalupalkeissa, jotka näkyvät sivun eri osissa. Aiemmissa versioissa Päävihjeet-toiminnon avulla pystyit nopeasti käyttämään mitä tahansa toimintoruudun painiketta painamalla Alt-näppäintä ja sitten sarjan kirjaimia. 

[![keyTipsAX6](./media/keytipsax6.png)](./media/keytipsax6.png)Nykyisessä Dynamics 365 for Operationsin versiossa Päävihjeet-toimintoa ei kuitenkaan ole enää saatavilla, vaan sen on korvannut toimintohaku-ominaisuus. Tämän uuden ominaisuuden avulla voit nopeasti etsiä ja suorittaa painikkeen mistä tahansa näkyvillä olevasta toimintoruudusta.

## <a name="using-action-search"></a>Toimintohaun käyttö
Suorita seuraavat vaiheet, kun haluat käyttää toimintohaku-ominaisuutta:

1.  Valitse toimintoruudussa **toimintohaku**-kenttää. (**toimintohaku**-kentässä on suurennuslasikuvake.)
2.  Kirjoita sen painikkeen nimi (tai osa nimestä), jonka haluat suorittaa. Voit myös etsiä käyttämällä sanoja painikkeen "polusta". (Lisätietoja on tämän artikkelin seuraavassa osassa.) Yleensä painike näkyy tulosluettelon yläosassa sen jälkeen, kun olet kirjoittanut merkit kahdesta neljään.
3.  Etsi ja suorita painike tulosluettelossa (käyttämällä hiirtäsi tai näppäimistöä).

Kun painike on suoritettu, huomio palautuu viimeiseen toimeesi sivulla niin, että voit jatkaa työskentelyä. 

[![action-search-field](./media/action-search-field.png)](./media/action-search-field.png)

Voit myös aloittaa toiminnon painamalla näppäinyhdistelmää Ctrl+/ tai Alt+Q. Paina pikanäppäintä uudelleen palataksesi edelliseen toimeesi sivulla.

## <a name="understanding-the-results-list"></a>Tulosluetteloon tutustuminen
Usein Dynamics 365 for Operationsissa sinun on tiedettävä painikkeesta sekä sijainti että konteksti, jotta ymmärtäisit täysin painikkeen tarkoituksen. Tämän vuoksi lisätiedot on jokaisesta nimikkeestä tulosluettelossa, jotta voit ymmärtää täysin luettelossa näytettävät painikkeet. Erityisesti painikkeen "polku" näytetään. Tämä polku saattaa soveltuvin osin sisältää seuraavien käyttöliittymäelementtien otsikot:

-   Toimintoruutu-välilehti
-   Painikeryhmä
-   Valikkopainike (jos painike on valikkopainikkeen sisällä)
-   Valikon erotin (jos painike on valikkopainikkeen sisällä nimetyn ryhmän sisällä)
-   Sivulla oleva ryhmä tai välilehti (esimerkiksi pikavälilehden nimi).

Kirjoitit esimerkiksi **yht****toimintohaku**-kenttään ja tarkastelet nyt tulosluetteloa. Ensimmäinen tulosluettelon painike **Summat** näkyy korostettuna. Näet myös painikkeen, jonka polku on **Sales**&gt;**Näytä**. Polun **Myyntitilaus**-osa vastaa toimintoruudun **Myyntitilaus**-välilehteä, ja polun **Näytä**-osa vastaa kyseisen välilehden **Näytä**-ryhmää. Vastaavasti painikkeen **Kokonaisalennus**-polku (**Myy** &gt; **Laske**) ilmoittaa, että tämä painike sijaitsee **Laske**-ryhmässä toimintoruudun **Myy**-välilehdessä. Tämän vuoksi näiden tietojen avulla voit ymmärtää täsmälleen mikä painike suoritetaan toimintohaun toimesta (jos valitset kyseisen painikkeen tulosten luettelossa). 

[![action-search-field-with-data](./media/action-search-field-with-data.png)](./media/action-search-field-with-data.png) 

Edellisessä esimerkissä toimintohakku näytti tulokset standardimuotoisesta toimintoruudusta sivun yläreunassa. Toimintohaku kuitenkin näyttää tulokset myös näkyvillä olevista työkaluriveistä, jotka sijaitsevat muissa sivun kohdissa. Esimerkiksi etsit **Käytettävissä oleva varasto** -painiketta, joka sijaitsee **Myyntitilausrivit**-pikavälilehdessä. Tässä tapauksessa tulosten luettelossa painikkeen polku (**Myyntitilausrivit** &gt; **Varasto** &gt; **Näytä**) ilmoittaa, että tämä painike sijaitsee **Näytä**-otsikossa **Varasto**-valikkopainikkeessa **Myyntitilausrivit**-pikavälilehdessä. 

[![on-hand-inventory](./media/on-hand-inventory.png)](./media/on-hand-inventory.png)

## <a name="action-search-vs-navigation-search"></a>Toimintohaku vs. siirtymishaku
Toimintohaun tarkoituksena on etsiä ja suorittaa toimintoja sivulla. Dynamics 365 for Operationsissa on myös erillinen hakumekanismi sivujen etsimiseen ja niille siirtymiseen. Lisätietoja tästä ominaisuudesta löydät artikkelista. [Siirtymishaku](navigation-search.md).




