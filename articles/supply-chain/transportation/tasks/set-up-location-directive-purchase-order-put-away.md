---
title: Määritä sijaintidirektiivi ostotilauksen poispanolle
description: Tässä menettelyssä näytetään, miten yksinkertainen sijaintidirektiivi määritetään.
author: ShylaThompson
manager: AnnBe
ms.date: 11/02/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9ca4b3c2598a268c065011daff31296521faa918
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/15/2019
ms.locfileid: "1551856"
---
# <a name="set-up-a-location-directive-for-purchase-order-put-away"></a>Määritä sijaintidirektiivi ostotilauksen poispanolle

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tässä menettelyssä näytetään, miten yksinkertainen sijaintidirektiivi määritetään. Näytetyssä esimerkissä luodaan sijaintidirektiivi, jolla määrätään, mihin ostotilaukseen vastaanotetut nimikkeet määritetään. Voit toistaa tämän tehtäväopastuksen mainituilla tiedoilla käyttämällä USMF-esittely-yrityksen tietoja. Edellytykset: Sinun on luotava käsittelykoodi. Tässä menettelyssä käytetään Relabel-käsittelykoodia. Jos olet luomassa sijaintidirektiivin omissa tiedoissasi, varastonhallinnan lisäasetusten on oltava määritettynä varastolle ja nimikkeille.  Tämä menettely on tarkoitettu varastopäällikölle.

1. Valitse Varastonhallinta > Asetukset > Sijaintidirektiivit.
2. Valitse Työtilaustyyppi-kentässä Ostotilaukset.

## <a name="create-a-location-directive-header"></a>Luo sijaintidirektiivin otsikko
1. Valitse Uusi.
2. Syötä Järjestysnumero-kenttään numero.
    * Tämä on järjestys, jonka perusteella valitun työtyypin sijaintidirektiivi käsitellään. Voit myös tarvittaessa muokata järjestystä.  
3. Kirjoita arvo Nimi-kenttään.
    * Tämä on direktiivin yksilöivä tunniste.  
4. Valitse Työtyyppi-kentässä Määritä.
    * Valitse suoritettavan työn tyyppi Jos direktiivin työtilauksen tyyppi on Ostotilaus, Määritä on ainoa tuettu arvo.  
5. Kirjoita arvo Toimipaikka-kenttään.
6. Kirjoita arvo Varasto-kenttään.
    * Jätä direktiivikoodi tyhjäksi.  Direktiivikoodeilla Määritä-tyypin työtilaustyypit linkitetään tiettyyn direktiiviin. Ostotilauksissa viimeisen Määritä-tyyppisen työtilausrivin sijainti ratkaistaan ennen työmallin määrittämistä. Työmallin viimeistä riviä ei voi tämän vuoksi yhdistää tiettyyn direktiiviin.   
7. Kirjoita arvo Käsittelykoodi-kenttään.
    * Käsittelykoodi rajoittaa sijaintidirektiivin käyttöä, joten sijaintidirektiiviä käytetään vain siinä tapauksessa, että varastotyöntekijä antaa tämän arvon rekisteröidessään nimikettä mobiililaitteella.  
8. Valitse Tallenna.

## <a name="edit-the-query-for-directive"></a>Muokkaa direktiivin kyselyä
1. Valitse Muokkaa kyselyä.
    * Tämän direktiivi on jo rajoitettu käytettäväksi määrittämäsi varastoon rekisteröidyissä nimikkeissä, joilla on määrittämäsi käsittelykoodi. Voit lisätä muita rajoituksia kyselyn avulla.  
2. Valitse OK.

## <a name="add-directive-lines"></a>Lisää direktiivirivit
1. Valitse Uusi.
    * Tämä on järjestys, jonka perusteella valitun työtyypin sijaintidirektiivin rivit käsitellään. Voit myös tarvittaessa muokata järjestystä.  
2. Lisää Määrästä-kenttään numero.
    * Tämä on vähimmäismäärä, jolla tämä direktiivirivi on voimassa.  
3. Lisää Määrään-kenttään numero.
4. Kirjoita arvo Yksikkö-kenttään.
    * Yksikkö, jolla Määrästä ja Määrälle ilmoitetaan. Jos kenttä jätetään tyhjäksi, nimikkeen varastoyksikkö käytetään.  
5. Valitse Etsi määrä -kentässä vaihtoehto.
    * Ei mitään tai rekisterikilpien määrä: kullekin rekisterikilvelle rekisteröity määrä. Määrä, jolle määrätty yksikkö: koko rekisteröity määrä. Jäljellä oleva määrä: ostotilausriviltä vielä rekisteröitävä määrä. Odotettu määrä: ostotilausrivillä määritetty kokonaismäärä.  
6. Valitse Rajoita yksikön mukaan -valintaruutu tai poista sen valinta.
    * Jos valitset tämän vaihtoehdon ja määrität yksikön Rajoita yksikön mukaan -sivulla, sijaintiin voidaan määrittää vain nimikkeet, joilla on kyseinen mittayksikkö. Jos mittayksikkö on esimerkiksi kuormalava, vain kuormalavojen nimikkeet voidaan asettaa määritettyyn sijaintiin.  
7. Valitse Salli jakaminen -valintaruutu tai poista sen valinta.
    * Tällä tavoin direktiivi voi jakaa määrän eri sijainteihin.  
8. Valitse Tallenna.

## <a name="restrict-the-directive-line-to-a-specific-unit"></a>Rajoita direktiivirivi tiettyyn yksikköön
1. Valitse Rajoita yksikön mukaan.
    * Tämä painike on käytettävissä vain, kun Tallenna valitaan Tallenna Rajoita yksikön mukaan -valintaruudun valinnan jälkeen.  
2. Kirjoita arvo Yksikkö-kenttään.
3. Sulje sivu.

## <a name="add-a-location-directive-action-line"></a>Lisää sijaintidirektiivin toimintorivi
1. Valitse Uusi.
    * Tämä on järjestys, jonka perusteella valitun työtyypin sijaintidirektiivin toimintorivit käsitellään. Voit myös tarvittaessa muokata järjestystä.  
2. Kirjoita arvo Nimi-kenttään.
    * Tämä on direktiivin toiminnon yksilöivä tunniste.  
3. Valitse Kiinteän sijainnin käyttö -kentässä vaihtoehto.
    * Kiinteät ja ei-kiinteät sijainnit: kaikki ei-kiinteät sijainnit ovat kelvollisia samoin kuin tuotteen oma kiinteä kyselyn määrittämissä rajoissa.  Tuotteelle vain kiinteitä sijainteja: tuotteen kiinteät sijainnit ovat kelvollisia ja tuotevariantit jakavat saman kiinteiden sijaintien joukon. Tuotevariantille vain kiinteitä sijainteja: vain kullekin tuotevariantille määritetyt kiinteät sijainnit ovat kelvollisia.  
4. Valitse Strategia-kentässä vaihtoehto.
    * Ostotilaus-työtilaustyypit tukevat seuraavia strategioita: Ei mitään: nimike asetetaan ensimmäiseen löydettyyn sijaintiin. Konsolidoi: nimike sijoitetaan sijaintiin, jossa on jo vastaavia kohteita. Tyhjä sijainti ilman saapuvia töitä: Nimike sijoitetaan ensimmäiseen löytyvään tyhjään sijaintiin. Sijainnin katsotaan olevan tyhjä, jos sillä ei ole fyysistä varastoa eikä odotettuja saapuvia töitä.  
5. Valitse Tallenna.

## <a name="edit-the-query-for-directive-action-line"></a>Muokkaa direktiivin toimintorivin kyselyä
1. Valitse Muokkaa kyselyä.
2. ValitseLisää.
3. Kirjoita Kenttä-kenttään Sijainnin profiilitunnus.
    * Tässä esimerkissä mahdollisia sijainteja rajoitetaan sijaintiprofiilin tunnuksen avulla.  
4. Kirjoita arvo Ehdot-kenttään.
5. Valitse OK.
    * Voit jatkaa direktiivirivien ja -toimintojen lisäämistä, kunnes varaston kaikki mahdolliset skenaariot on otettu huomioon.  

