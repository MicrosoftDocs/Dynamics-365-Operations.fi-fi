---
title: "Materiaalikulutuksen rekisteröinti mobiililaitteella | Microsoft Docs"
description: "Tässä ohjeaiheessa käsitellään työnkulkua, jolla tuotannossa kulutettavat raaka-aineet voidaan rekisteröidä kämmenlaitteella."
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: AX 7.0.0, Operations, UnifiedOperations
ms.custom: 1706093
ms.assetid: 75ee68e0-4b9f-4f4d-b286-f498e0eb73fa
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 63160b9473c7f45b0eb0ca7139f9ed47c8e1446f
ms.openlocfilehash: 2c4b6637d35820e3ab7b7c43bbf7cecde516c46c
ms.contentlocale: fi-fi
ms.lasthandoff: 06/20/2017

---

# Materiaalikulutuksen rekisteröinti mobiililaitteella
<a id="register-material-consumption-using-a-mobile-device" class="xliff"></a>
Tässä ohjeaiheessa käsitellään työnkulkua, jolla tuotannossa kulutettavat raaka-aineet voidaan rekisteröidä kämmenlaitteella.

Johdanto
<a id="introduction" class="xliff"></a>
------------

Tämä työnkulku on hyödyllinen, jos materiaalin tarkka seuranta on välttämätöntä. Näissä tilanteissa materiaalin jäljitettävyyden ylläpito edellyttää kulutuksen tarkan ajan ja määrän ilmoittamista. Tämä prosessi voidaan nähdä esi- tai jälkipoiston peilikuvana, sillä näissä toiminnoissa rekisteröinnin ajankohta ja varsinaisen kulutuksen ajankohta poikkeavat toisistaan. Tämän vuoksi automaattista kulutusstrategiaa ei voi käyttää joissakin materiaaleissa, joissa on edellytyksenä jäljitettävyys. Tarkastellaan yksinkertainen skenaariota, joka selittää, miten määritetään työnkulku tuotannossa tapahtuvan raaka-aineiden kulutuksen rekisteröintiin kämmenlaitteella. [![](./media/scenario3.png)](./media/scenario3.png)

### Skenaarion tiedot
<a id="scenario-details" class="xliff"></a>

Jatkuva tuotantoprosessi (5) kuluttaa eräohjattua raaka-ainetta RM-100. Materiaali on käytettävissä varaston sijainnissa Bulk-001 (1), rekisterikilpi on PL-1 ja siinä on kaksi erää B1 ja B2, joiden kummankin määrä 100 lbs. RM-100:n varastotyö (2) vapautetaan ja käsitellään. Materiaali kerätään sijainnista Bulk-001 tuotannon varastoinnin sijaintiin PIL-01 (3), joka on määritetty rekisterikilpiohjatuksi sijainniksi. Koneenkäyttäjä punnitsee materiaalin tuotannon varastointisijainnissa (3) ja rekisteröi painon. Eränumero on kulutettu (4). Osa materiaalista lisätään tuotannon varastoinnin sijainnista tuotantoprosessiin määritetyin aikavälein. Kun koneenkäyttäjä lisää materiaalia, se punnitaan vaa'alla ja eränumero rekisteröidään.

## Työnkulun määrittäminen rekisteröimään kulutus kämmenlaitteella
<a id="set-up-the-workflow-to-register-consumption-using-a-handheld-device" class="xliff"></a>
Luo valmis tuote, FG 100, tuoterakenteella, jossa on eräohjattua raaka-ainetta RM-100. Lisää RM-100:n kaksi erää, B1 ja B2, joissa on määrä 100, sijaintiin Bulk-001, jossa on rekisterikilpi PL-1. RM-100:n tuoterakennerivin materiaaliottosäännöksi on valittu **Manuaalinen**. Määritä tuotannon varastoinnin sijainniksi PIL-01. Voit tehdä sen valitsemalla tämän sijainnin tuotannon varastoinnin oletussijainniksi varastossa 51.

1.  Luo uusi mobiililaitteen valikkovaihtoehto: 

-    **Valikkovaihtoehdon nimi** – Rekisteröi materiaalikulutus. 
-    **Ruutu** – Rekisteröi materiaalikulutus. 
-    **Menetelmä** – Epäsuora. 
-    **Toimintokoodi** – Rekisteröi materiaalikulutus.

2.  Lisää valikkovaihtoehto **tuotannon mobiililaitteen** valikkoon.
3.  Luo valmiin tuotteen tuotantotilaus: 

-    **Nimiketunnus** – FG-100 
-    **Toimipaikka** – 5 
-    **Varasto** – 51 
-    **Määrä** – 150

Tuotantotilaus on **arvioitu** ja **vapautettu** ja varastotyö on luotu.

4.  Suorita työ käyttämällä kämmenlaitteelle suunniteltua raaka-aineiden keräilyn työnkulkua.

Työnkulku siirtää materiaalin bulkkisijainnista tuotannon varastoinnin sijaintiin PIL-01. Kun työ on suoritettu, materiaalin tila on **kerätty tuotannon varastoinnin sijainnissa**. Työn käsittelyn jälkeen tila on joko **Keräilty** tai **Varattu fyysinen**. Tämä on määritetty parametrilla **Jälkeen-varasto-ottotila viety varastolomakkeeseen**.

5.  Käynnistä tuotantotilaus asiakasohjelmasta tai kämmenlaitteesta **Tuotannon käynnistys** -valikkovaihtoehdosta.

Kun tuotantotilaus on käynnistetty, voit rekisteröidä materiaalikulutuksen kämmenlaitteen työnkulussa. Aloitetaan rekisteröimällä 25 lbs:n kulutus erässä B1.

6.  Valitse kämmenlaitteen valikossa **Rekisteröi** **materiaalikulutus** ja anna seuraavat tiedot: 

-    Tuotantotilauksen numero. 
-    Sijainti, jossa materiaali aiotaan kuluttaa eli tässä tapauksessa PIL-01. 
-    Nimiketunnus RM-100. 
-    Eränumero B1. 
-    Määrä 25.

7.  Valitse **OK**.

Huomaa, että näyttöön avautuu sanoma Kirjauskansion rivi on luotu. Tuotantotilauksessa on avoin nimiketunnuksen RM-100 ja eränumeron B1 kirjauskansio, jonka tyyppi on **Tuotannon keräysluettelo**. 

Voit nyt valita rekisteröinnin jatkamisen esimerkiksi eränumerolla B2. Avoimeen kirjauskansioon lisätään silloin uusi kirjauskansion rivi aina, kun valitset **OK**. 

Kun rekisteröinti on valmis, kirjaa kirjauskansio ja lopeta työnkulku valitsemalla **Valmis**.

### Lisäkommentit
<a id="additional-comments" class="xliff"></a> 

-   Jos käyttäjä peruuttaa työnkulun kirjauskansion rivin luomisen jälkeen, kirjauskansio on kirjaamattomassa tilassa. Jos käyttäjä kuitenkin haluaa myöhemmin käyttää saman tuotantotilauksen työnkulkua, rivit lisätään avoimeen kirjauskansioon eikä uuteen kirjauskansioon.
-   Uusi työnkulku tukee myös sarjanumeroiden rekisteröintiä.
-   Nimiketunnus voidaan rekisteröidä vain, jos se on määritetty valitun tuotanto- tai erätilauksen tuoterakenteessa tai kaavassa.
-   Materiaali voidaan ylikuluttaa. Jos esimerkiksi materiaalin kulutusmääräksi arvioidaan 100 lbs, se voidaan sitten ylikuluttaa esimerkiksi määrällä 105 lbs.



