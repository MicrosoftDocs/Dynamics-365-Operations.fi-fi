---
title: Määritä sijaintidirektiivi ostotilauksen poispanolle
description: Tässä ohjeaiheessa käsitellään, kuinka määritetään yksinkertainen sijaintidirektiivi.
author: ShylaThompson
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WHSInventFixedLocation
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b11d99f026f4c06b1e2c8b88acc1d9926bbc493bf1ebb851ef1b7b78daff2a9c
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6722220"
---
# <a name="set-up-a-location-directive-for-purchase-order-put-away"></a>Määritä sijaintidirektiivi ostotilauksen poispanolle

[!include [banner](../../includes/banner.md)]

Tässä ohjeaiheessa käsitellään, kuinka määritetään yksinkertainen sijaintidirektiivi. Näytetyssä esimerkissä luodaan sijaintidirektiivi, jolla määrätään, mihin ostotilaukseen vastaanotetut nimikkeet määritetään. Voit toistaa tämän tehtäväopastuksen mainituilla tiedoilla käyttämällä USMF-esittely-yrityksen tietoja. Edellytykset: Sinun on luotava käsittelykoodi. Tässä menettelyssä käytetään Relabel-käsittelykoodia. Jos olet luomassa sijaintidirektiivin omissa tiedoissasi, varastonhallinnan lisäasetusten on oltava määritettynä varastolle ja nimikkeille. Tämä menettely on tarkoitettu varastopäällikölle.

1. Siirry kohtaan **Siirtymisruutu > Moduulit > Varastonhallinta > Asetukset > Sijaintidirektiivit**.
2. Valitse **Työtilaustyyppi**-kentässä **Ostotilaukset**.

## <a name="create-a-location-directive-header"></a>Luo sijaintidirektiivin otsikko
1. Valitse **Uusi**.
2. Syötä **Järjestysnumero**-kenttään numero. Tämä on järjestys, jonka perusteella valitun työtyypin sijaintidirektiivi käsitellään. Voit myös tarvittaessa muokata järjestystä.  
3. Kirjoita arvo **Nimi**-kenttään. Tämä on direktiivin yksilöivä tunniste.  
4. Valitse **Työtyyppi**-kentässä **Määritä**. Valitse suoritettavan työn tyyppi Jos työtilauksen tyyppinä on ostotilaus, direktiivissä tuetaan vain arvoa **Määritä**.  
5. Kirjoita arvo **Toimipaikka**-kenttään.
6. Kirjoita arvo **Varasto**-kenttään. Jätä direktiivikoodi tyhjäksi.  Direktiivikoodeilla Määritä-tyypin työtilaustyypit linkitetään tiettyyn direktiiviin. Ostotilauksissa viimeisen Määritä-tyyppisen työtilausrivin sijainti ratkaistaan ennen työmallin määrittämistä. Työmallin viimeistä riviä ei voi tämän vuoksi yhdistää tiettyyn direktiiviin.   
7. Kirjoita arvo **Käsittelykoodi**-kenttään. Käsittelykoodi rajoittaa sijaintidirektiivin käyttöä, joten sijaintidirektiiviä käytetään vain siinä tapauksessa, että varastotyöntekijä antaa tämän arvon rekisteröidessään nimikettä mobiililaitteella.  
8. Valitse **Tallenna**.

## <a name="edit-the-query-for-directive"></a>Muokkaa direktiivin kyselyä
1. Valitse **Muokkaa kyselyä**. Tämän direktiivi on jo rajoitettu käytettäväksi määrittämäsi varastoon rekisteröidyissä nimikkeissä, joilla on määrittämäsi käsittelykoodi. Voit lisätä muita rajoituksia kyselyn avulla.  
2. Valitse **OK**.

## <a name="add-directive-lines"></a>Lisää direktiivirivit
1. Valitse **Uusi**. Tämä on järjestys, jonka perusteella valitun työtyypin sijaintidirektiivin rivit käsitellään. Voit myös tarvittaessa muokata järjestystä.  
2. Lisää **Määrästä**-kenttään numero. Tämä on vähimmäismäärä, jolla tämä direktiivirivi on voimassa.  
3. Lisää **Määrään**-kenttään numero.
4. Kirjoita arvo **Yksikkö**-kenttään. Yksikkö, jolla Määrästä ja Määrälle ilmoitetaan. Jos kenttä jätetään tyhjäksi, nimikkeen varastoyksikkö käytetään.  
5. Valitse **Etsi määrä** -kentässä vaihtoehto.
    - Ei mitään tai rekisterikilpien määrä: kullekin rekisterikilvelle rekisteröity määrä.  
    - - Määrä, jolle määrätty yksikkö: koko rekisteröity määrä.  
    - Jäljellä oleva määrä: ostotilausriviltä vielä rekisteröitävä määrä.  
    - Odotettu määrä: ostotilausrivillä määritetty kokonaismäärä.  
6. Valitse **Rajoita yksikön mukaan** -valintaruutu tai poista sen valinta. Jos valitset tämän vaihtoehdon ja määrität yksikön **Rajoita yksikön mukaan** -sivulla, sijaintiin voidaan määrittää vain nimikkeet, joilla on kyseinen mittayksikkö. Jos mittayksikkö on esimerkiksi kuormalava, vain kuormalavojen nimikkeet voidaan asettaa määritettyyn sijaintiin.  
7. Valitse **Salli jakaminen** -valintaruutu tai poista sen valinta. Tällä tavoin direktiivi voi jakaa määrän eri sijainteihin.  
8. Valitse **Tallenna**.

## <a name="restrict-the-directive-line-to-a-specific-unit"></a>Rajoita direktiivirivi tiettyyn yksikköön
1. Valitse **Rajoita yksikön mukaan**. Tämä painike on käytettävissä vain, kun **Tallenna** valitaan **Rajoita yksikön mukaan** -valintaruudun valinnan jälkeen.  
2. Kirjoita arvo **Yksikkö**-kenttään.
3. Sulje sivu.

## <a name="add-a-location-directive-action-line"></a>Lisää sijaintidirektiivin toimintorivi
1. Valitse **Uusi**. Tämä on järjestys, jonka perusteella valitun työtyypin sijaintidirektiivin toimintorivit käsitellään. Voit myös tarvittaessa muokata järjestystä.  
2. Kirjoita arvo **Nimi**-kenttään. Tämä on direktiivin toiminnon yksilöivä tunniste.  
3. Valitse **Kiinteän sijainnin käyttö** -kentässä vaihtoehto.
    - Kiinteät ja ei-kiinteät sijainnit: kaikki ei-kiinteät sijainnit ovat kelvollisia samoin kuin tuotteen oma kiinteä kyselyn määrittämissä rajoissa.  
    - Tuotteelle vain kiinteitä sijainteja: tuotteen kiinteät sijainnit ovat kelvollisia ja tuotevariantit jakavat saman kiinteiden sijaintien joukon.  
    - Tuotevariantille vain kiinteitä sijainteja: vain kullekin tuotevariantille määritetyt kiinteät sijainnit ovat kelvollisia.  
4. Valitse **Strategia**-kentässä vaihtoehto. Ostotilaustyyppiset työtilaukset tukevat seuraavia strategioita: 
    - Ei mitään: nimike sijoitetaan ensimmäiseen sijaintiin, joka löytyy.  
    - Konsolidoi: nimike sijoitetaan sijaintiin, jossa on jo vastaavia kohteita.  
    - Tyhjä sijainti ilman saapuvia töitä: Nimike sijoitetaan ensimmäiseen löytyvään tyhjään sijaintiin. Sijainnin katsotaan olevan tyhjä, jos sillä ei ole fyysistä varastoa eikä odotettuja saapuvia töitä.  
5. Valitse **Tallenna**.

## <a name="edit-the-query-for-directive-action-line"></a>Muokkaa direktiivin toimintorivin kyselyä
1. Valitse **Muokkaa kyselyä**.
2. Valitse **Lisää**.
3. Kirjoita **Kenttä**-kenttään `location profile ID`. Tässä esimerkissä mahdollisia sijainteja rajoitetaan sijaintiprofiilin tunnuksen avulla.  
4. Kirjoita arvo **Ehdot**-kenttään.
5. Valitse **OK**. Voit jatkaa direktiivirivien ja -toimintojen lisäämistä, kunnes varaston kaikki mahdolliset skenaariot on otettu huomioon.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]