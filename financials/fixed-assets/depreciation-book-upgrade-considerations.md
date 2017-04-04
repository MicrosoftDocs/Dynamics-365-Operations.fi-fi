---
title: "Poistokirjan päivityksen yleiskatsaus"
description: "Aiemmissa versioissa oli kaksi arvostus käsitteiden käyttöomaisuus - arvomallit ja poistokirjat. Microsoft Dynamics 365 for Operations -versiossa 1611 arvomallin toiminnot ja poistokirjatoiminnot on yhdistetty yhdeksi käsitteeksi, josta käytetään nimitystä &quot;kirja&quot;. Tämä aihe käsittelee päivityksessä huomioitavia seikkoja."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, Developer
ms.search.scope: Operations, Core
ms.custom: 221624
ms.assetid: cf434099-36f9-4b0f-a7c8-bed091e34f39
ms.search.region: global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: bec019d218d80ba059d5a1c232072f46b1ae3ee2
ms.openlocfilehash: d29cb7bc5acc29be93332b4211adebc4486a7a25
ms.lasthandoff: 03/31/2017


---

# <a name="depreciation-book-upgrade-overview"></a>Poistokirjan päivityksen yleiskatsaus

Aiemmissa versioissa oli kaksi arvostus käsitteiden käyttöomaisuus - arvomallit ja poistokirjat. Microsoft Dynamics 365 for Operations -versiossa 1611 arvomallin toiminnot ja poistokirjatoiminnot on yhdistetty yhdeksi käsitteeksi, josta käytetään nimitystä "kirja". Tämä aihe käsittelee päivityksessä huomioitavia seikkoja. 

Päivitysprosessi siirtää aiemmin määritetyt asetukset ja kaikki olemassa olevat tapahtumat uuden kirjan rakenteeseen. Arvomallit säilyvät nykyisellään, kirjana joka tekee kirjauksia kirjanpitoon. Poistokirjat siirretään kirjaan, jonka **Kirjaa kirjanpitoon** -asetus on **Ei**. Poistokirjan kirjauskansioiden nimet siirretään kirjanpidon Kirjauskansionimi jonka Kirjaustaso määrittää **ei mitään**. Poistokirjatapahtumat siirretään käyttöomaisuustapahtumia. 

Ennen tietojen päivityksen suorittamista sinun on hyvä ymmärtää käytettävissä olevat kaksi vaihtoehtoa poistokirjan kirjauskansion rivien päivittämiseksi tapahtumatositteisiin, ja numerosarja, jota käytetään tositesarjaan. 

Vaihtoehto 1: **Järjestelmän määrittämä numerosarjan**: tämä on oletusasetus päivityksen suorituskyvyn parantamiseksi. Päivitys ei käytä numerosarjojen kehystä, mutta sen sijaan kohdistaa tositteet joukkoon perustuvan mallin pohjalta. Päivityksen jälkeen, järjestelmä luo uuden numerosarjan kanssa **seuraavan määritettynä** asianmukaisesti päivitetty tapahtumien perusteella. Oletusarvon mukaan käytettävä numerosarja on FADBUpgr\#\#\#\#\#\#\#\#\# muodossa. Voit säätää tätä lähestymistapaa käytettäessä muotoilu on muutamia parametreja:

-   **Numerojärjestyskoodi** – voit määrittää numerosarjan koodi. Tämä numerosarja ei voi olla koska se luodaan päivityksen.
    -   Vakion nimi: **NumberSequenceDefaultCode**
    -   Oletusarvo: "FADBUpgr"
-   **Etuliite**: kiinteä merkkijonon arvo, jota käytetään etuliitteenä tositenumeroissa.
    -   Vakion nimi: **NumberSequenceDefaultParameterPrefix**
    -   Oletusarvo: "FADBUpgr"
-   **Aakkosnumeerinen pituus**: aakkosnumeerisen segmentin numerosarjan pituus.
    -   Vakiona nimi: ** NumberSequenceDefaultParameterAlpanumericLength **
    -   Oletusarvo: 9
-   **Ensimmäinen numero**: numerosarjan ensimmäinen numero.
    -   Vakiona nimi: ** NumberSequenceDefaultParameterStartNumber **
    -   Oletusarvo: 1

Vaihtoehto 2: **aiemmin luotu käyttäjän määrittämä numerosarja** -tämän vaihtoehdon avulla voit määrittää numerosarja, jota voidaan käyttää päivitystä varten. Harkitse tämän vaihtoehdon numero järjestyksessä kokoonpano tarvittaessa. Käytettävä numerosarja on muokattava päivityksen luokka ReleaseUpdateDB70\_FixedAssetJournalDepBookRemovalDepBookJournalTrans, jossa on seuraavat tiedot:

-   **Numerosarjan koodi**: Numerosarjan koodi.
    -   Vakiona nimi: ** NumberSequenceExistingCode **
    -   Oletusarvo: Ei oletusarvoa, tämä on päivitettävä numerosarjan koodiksi.
-   **Jaettu numerosarja**: totuusarvo, jolla tunnistetaan numerosarjan vaikutusalue. Käytä jaetun numerosarjan arvoa "tosi" kaikissa yrityksissä ja arvoa "false" yrityskohtaisella alueella. Käytettäessä "false", on oltava jokaisessa yrityksessä, joka sisältää poistokirjatapahtumat numerosarja, jolla on määritetty nimi. Jokaista osiota, joka sisältää poistokirjatapahtumat ole jaettu numerosarjoja.
    -   Vakiona nimi: ** NumberSequenceExistingIsShared **
    -   Oletusarvo: tosi

Parametrit sijaitsevat ReleaseUpdateDB70 alussa\_FixedAssetJournalDepBookRemovalDepBookJournalTrans-luokkaa. 

*Parempi lähestymistapa tositteet kohdistuksen määrittäminen*<ph id="t1">
</ph>*/ / arvo on true, jos haluat käyttää aiemmin numerosarjakoodi*<ph id="t2">
</ph>*/ / arvo on false, jos aiot käyttää järjestelmän määrittämiä numerosarja (oletus)* vakio boolean NumberSequenceUseExistingCode = false;  

*Jos järjestelmän määrittämä numero sarja lähestymistapa, Määritä numerosarja parametrit. *<ph id="t3">
</ph>*/ / Uusi nimiketunnus numerosarjaan luodaan näillä parametreilla.* Const str NumberSequenceDefaultCode = 'FADBUpgr'; Const str NumberSequenceDefaultParameterPrefix = 'FADBUpgr'; CONST int NumberSequenceDefaultParameterAlpanumericLength = 9; CONST int NumberSequenceDefaultParameterStartNumber = 1;   

*Jos olemassa oleva numero sarja lähestymistapa, Määritä nykyisen numerosarjakoodi. *<ph id="t4">
</ph>*/ / Tositteen kohdistus siirtyy rivin rivin osalta olemassa olevia numerosarjoja.* Const str NumberSequenceExistingCode = ''; */ / Soveltamisala nykyisen numerosarjakoodi*<ph id="t5">
</ph>*/ / arvo on TOSI, jos määritetty numerosarja on jaettu*<ph id="t6">
</ph>*/ / arvo on false, jos määritetty numerosarja on yrityskohtainen*<ph id="t7">
</ph>*/ / järjestelmän määrittämiä oletusnumerojärjestystä käytetään, jos ei löydy määritetyn alueen kanssa numerosarjakoodi.* const boolean NumberSequenceExistingIsShared = true; 

Muodosta uudelleen projekti, joka sisältää luokan vakioiden muuttamisen jälkeen. 

Järjestelmä luo numeron sarja lähestymistapa (vaihtoehto 1) käytettäessä päivitystä käyttää joukko tapahtuva käsittely kohdistamaan tositenumeroita määriteltyjä päivityksen Komentosarjaparametrit. Se luo myös uuden numerosarjan annetuilla parametreilla kohdistuksen jälkeen. 

Käytettäessä käyttäjän määrittämää numerosarjaa (vaihtoehto 2) tietopäivitys tarkistaa, esiintyykö määritetyllä alueella vaikuttava numerosarja jokaisen osion tietokannassa ja yrityksessä, jolla on poistokirjatapahtumia. Jos sitä ole päivitys käyttää rivin rivin käsittelyn kohdistamaan tositenumeroita numero sarja puitteiden avulla numerosarjan mukaisesti. Jos numerosarja ei ole määritetyn alueen, päivitys käyttää oletusarvoisesti järjestelmän määrittämiä numero sarja lähestymistapa varata tositenumeroiden ja luo uusi numerosarja on määritetty oletusparametrit kohdistuksen jälkeen.

Kummassakin menetelmässä tietojen päivityskomentosarja käyttää myös numerosarjaa **Tositesarja**-kentässä uusissa kirjauskansion nimissä, jotka luotiin vanhan poistokirjan kirjauskansion nimiä varten.


