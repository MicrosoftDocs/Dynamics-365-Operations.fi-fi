---
title: Toiminnon haku
description: "Tässä artikkelissa kuvataan Microsoft Dynamics-365 työvaiheiden toiminto hakutoiminto. Toiminto Etsi auttaa, Etsi ja suorita toimet-sivulla."
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

Tässä artikkelissa kuvataan Microsoft Dynamics-365 työvaiheiden toiminto hakutoiminto. Toiminto Etsi auttaa, Etsi ja suorita toimet-sivulla.

<a name="introduction"></a>Johdanto
------------

Microsoft Dynamics-365 toimintojen sivujen altistaa ensisijaisesti komennot toimintoruutujen sekä vakio toimintoruudun, joka näkyy sivun yläreunassa ja työkalurivejä, jotka näkyvät sivun eri osissa. Aiemmissa versioissa avain vihjeitä-toiminnon avulla voit nopeasti painamalla Alt-näppäintä ja sitten sarja kirjaimia mikä tahansa toiminto-ruudussa-painiketta. 

[![keyTipsAX6](./media/keytipsax6.png)](./media/keytipsax6.png) kuitenkin Dynamics 365 toimintojen nykyisen version avain vihjeitä eivät enää ole käytettävissä, mutta on korvattu toiminto Etsi-toimintoa. Tämän uuden ominaisuuden avulla voit nopeasti etsiä ja suorittaa painikkeen mistä tahansa näkyvillä olevasta toimintoruudusta.

## <a name="using-action-search"></a>Toimintohaun käyttö
Suorita seuraavat vaiheet, kun haluat käyttää toimintohaku-ominaisuutta:

1.  Valitse toimintoruudussa **toimintohaku**-kenttää. (**toimintohaku**-kentässä on suurennuslasikuvake.)
2.  Kirjoita nimi, jonka haluat suorittaa painikkeen osaksi tai kokonaan. Voit myös etsiä käyttämällä sanoja painikkeen "polku." (Lisätietoja on tämän artikkelin seuraavassa osassa.) Yleensä painiketta näkyvät tulosluettelon yläosassa sen jälkeen, kun olet kirjoittanut merkit kahdesta neljään.
3.  Etsi ja suorita painike tulosluettelossa (käyttämällä hiirtäsi tai näppäimistöä).

Kun painike on suoritettu, huomio palautuu viimeiseen toimeesi sivulla niin, että voit jatkaa työskentelyä. 

[![Etsi-toiminto-kentän](./media/action-search-field.png)](./media/action-search-field.png)

Voit myös aloittaa toiminnon painamalla näppäinyhdistelmää Ctrl+/ tai Alt+Q. Paina pikanäppäintä uudelleen palataksesi edelliseen toimeesi sivulla.

## <a name="understanding-the-results-list"></a>Tulosluetteloon tutustuminen
Usein-Dynamics 365 toimintoja varten, sinun on tiedettävä sijainti sekä ymmärtävät täysin kyseistä painiketta painikkeen yhteydessä. Tämän vuoksi lisätiedot on jokaisesta nimikkeestä näkyvät tulosluettelon, voi auttaa sinua ymmärtämään täysin luettelossa näytettävät painikkeet. Erityisesti painikkeen "polku" näytetään. Tämä polku saattaa soveltuvin osin sisältää seuraavien käyttöliittymäelementtien otsikot:

-   Toimintoruutu-välilehti
-   Painikeryhmä
-   Valikkopainike (jos painike on valikkopainikkeen sisällä)
-   Valikon erotin (jos painike on valikkopainikkeen sisällä nimetyn ryhmän sisällä)
-   Sivulla oleva ryhmä tai välilehti (esimerkiksi pikavälilehden nimi).

Kirjoitit esimerkiksi **yht****toimintohaku**-kenttään ja tarkastelet nyt tulosluetteloa. Ensimmäinen tapahtuma painike, jonka nimi on **yhteensä**, näkyy korostettuna. Painiketta polku **myynti**&gt;**View** on myös esitetty. **Myyntitilaus** vastaa polun osaa **myyntitilaus** toiminto-ruudussa-välilehti ja **Näytä** polun osaa vastaa **Näytä** kyseisen välilehden ryhmän. Vastaavasti polku **kokonaisalennus** painike (**myydä**&gt;**laskeminen**) ilmoittaa, että tämä painike sijaitsee **Laske** ryhmittelyyn **myydä** välilehti toimintoruudun. Tämän vuoksi näiden tietojen avulla voit ymmärtää täsmälleen mitä painiketta käynnistämän toiminnon etsinnän (Jos valitset kyseisen painikkeen tulosten luettelossa). 

[![Etsi-kenttä-ja-tiedot](./media/action-search-field-with-data.png)](./media/action-search-field-with-data.png) 

Edellisessä esimerkissä toimintohakku näytti tulokset standardimuotoisesta toimintoruudusta sivun yläreunassa. Toimintohaku kuitenkin näyttää tulokset myös näkyvillä olevista työkaluriveistä, jotka sijaitsevat muissa sivun kohdissa. Esimerkiksi etsit **käytettävissä oleva varasto** painiketta, joka sijaitsee **myyntitilausrivit** pikavälilehti. Tässä tapauksessa tulosten luettelossa painiketta polku (**myyntitilausrivit**&gt;**varaston**&gt;**View**) ilmoittaa, että tämä painike sijaitsee **Näytä** otsikko- **varaston** valikkopainikkeen **myyntitilausrivit** pikavälilehti. 

[![Valitse-käytettävissä-varasto](./media/on-hand-inventory.png)](./media/on-hand-inventory.png)

## <a name="action-search-vs-navigation-search"></a>Toimintohaku vs. siirtymishaku
Etsi toiminto on tarkoitus suorittaa toiminnot-sivulla ja etsiä, on erillinen haku, etsiminen ja sivujen Dynamics 365 toimintojen siirtyminen mekanismi. Saat lisätietoja tämän ominaisuuden [siirtyminen haku](navigation-search.md) artiklassa.


