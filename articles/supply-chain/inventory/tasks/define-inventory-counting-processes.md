---
title: Varastoinventoinnin prosessien määrittäminen
description: Tässä aiheessa kuvataan, miten perusvarastoinventoinnin prosessien konfigurointi tehdään luomalla inventointiryhmä ja inventoinnin kirjauskansio.
author: MarkusFogelberg
manager: tfehr
ms.date: 07/26/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventCountGroup, InventJournalName, InventParameters, EcoResProductDetailsExtended, InventItemLocation, InventLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9df5db0e71f550e82820e15b1597d9e287071f83
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/02/2020
ms.locfileid: "3213995"
---
# <a name="define-inventory-counting-processes"></a>Varastoinventoinnin prosessien määrittäminen

[!include [banner](../../includes/banner.md)]

Tässä aiheessa kuvataan, miten perusvarastoinventoinnin prosessien konfigurointi tehdään luomalla inventointiryhmä ja inventoinnin kirjauskansio. Menettelyssä kerrotaan myös, miten varasto- ja nimiketason inventointikäytännöt otetaan käyttöön. Varaston esimies tekee yleensä nämä tehtävät. Edellytyksenä on, että olemassa on joitakin aiemmin määritettyjä vapautettuja tuotteita ja varastoja. Jos käytössä on esittelytietojen yritys, voit suorittaa tämän menettelyn käyttämällä USMF-yritystä ja mitä tahansa varastoitua nimikettä.


## <a name="create-a-counting-group"></a>Luo inventointiryhmä.
1. Valitse siirtymisruudussa **Moduulit > Inventoinnin- ja varastonhallinta > Asetukset > Varasto > Inventointiryhmät**.
2. Valitse **Uusi**.
3. Kirjoita arvo uuden rivin **Inventointiryhmä**-kenttään.
4. Kirjoita arvo **Nimi**-kenttään.
5. Valitse vaihtoehto **Inventointikoodi**-kentässä.

    - **Manuaalinen** – Sisältää rivit aina, kun suoritat työn. Voit siis päättää inventointiryhmän inventointivälin.  
    - **Kausi** – Lisää inventointikirjauskansion kauden, kun kausiväli on umpeutunut.  
    - **Varastosaldo nolla** – Jos käytettävissä oleva varasto laskee nollaan (0), ohjelma luo rivejä inventointikirjauskansioon, kun työ suoritetaan. Jos käytettävissä oleva varasto saavuttaa 0 laskemisen jälkeen, rivejä syntyy seuraavan kerran kun käynnistät laskennan.  
    - **Vähintään** - Lisää rivejä laskentakirjauskansioon, jos käytettävissä oleva varasto on yhtä suuri tai pienempi kuin määritelty vähimmäismäärä.  
    - Valinnainen: Jos olet määrittänyt **Inventointikoodi**-kentän arvoksi **Kausi**, kirjoita **Inventointikausi**-kenttään kauden aikaväli. Välien yksikkö on päivät.  
    - Kun suoritat inventoinnin kirjauskansiossa uusien rivien luontityön, uudet rivit luodaan tässä kentässä määritetyin välein siitä huolimatta, miten usein suoritat kyseisen työn. Jos esimerkiksi **Inventointikausi**-kentän arvoksi on määritetty 7, kirjauskansion rivit luotiin inventointia varten viimeksi tammikuun 1. päivä ja toinen työ on aloitettu tammikuun 5 päivä, seitsemää päivää ei ole kulunut eikä kyseisen kausivälin kirjauskansioon luoda rivejä. Jos aloitat työn uudelleen tammikuun 8. päivä., ohjelma luo kauden rivit inventoinnin kirjauskansioon, koska 7 päivää on kulunut.  

6. Valitse **Tallenna**.

## <a name="create-a-counting-journal-name"></a>Inventoinnin kirjauskansion nimen luominen
1. Valitse siirtymisruudussa **Moduulit > Inventoinnin- ja varastonhallinta > Asetukset > Kirjauskansioiden nimet > Varasto**.
2. Valitse **Uusi**.
3. Kirjoita arvo **Nimi**-kenttään.
4. Kirjoita **Kuvaus**-kenttään arvo.
5. Valitse **Kirjauskansion tyyppi** -kentässä **Inventointi**. Valinnainen: Voit valita eri tositesarjan tunnuksen, jos haluat inventoinnin kirjauskansioiden luonnin yhteydessä luotujen tositteiden tunnuksille tietyn numerosarjan. Tositesarjat luodaan **Numerosarjat**-sivulla.  
6. Valitse vaihtoehto **Erittelytaso**-kentässä.  

    - Erittelytaso, jota käytetään, kun kirjauskansio kirjataan.  
    - Valinnainen: Voit muuttaa arvoa Varaus-kentässä. Tämä on nimikkeiden varaustapa inventoinnin aikana.   
    - **Manuaalinen** – Nimikkeet on varattu manuaalisesti varauslomakkeessa.  
    - **Automaattinen** – Tilauksen määrä varataan nimikkeen käytettävissä olevasta varastosta.   
    - **Hajotus** – Varaus on osa tapahtuman pääsuunnittelua.  

7. Valitse **Tallenna**.

## <a name="set-standard-counting-journal-name"></a>Vakioinventoinnin kirjauskansion nimen määrittäminen
1. Siirry kohtaan **Siirtymisruutu > Moduulit > Varastonhallinta > Asetukset > Varasto ja varastonhallinnan parametrit**.
2. Valitse **Kirjauskansiot**-välilehti.
3. Valitse **Inventointi**-kentän avattavasta valikosta aiemmin luomasi kirjauskansio. Tämä kirjauskansio on oletuskirjauskansio varastokirjauskansioille, joiden tyyppinä on **Inventointi**.  
4. Valitse **Yleiset**-välilehti. Valinnainen: Valitse tämä asetus, kun haluat lukita nimikkeen inventoinnin ajaksi. Tällä estetään pakkausluetteloiden, keräysluetteloiden ja keräysluettelon rekisteröintien päivitykset.  

## <a name="set-the-counting-policy-for-an-item"></a>Nimikkeen inventointikäytännön määrittäminen
1. Valitse siirtymisruudussa **Moduulit > Tuotetietojen hallinta > Tuotteet > Vapautetut tuotteet**.
2. Valitse luettelosta sen tuotteen nimiketunnuksen linkki, jonka inventointikäytännöt haluat määrittää. Sinun on valittava nimike, jota seurataan varastossa. Varastoimattomia tuotteita ei voi inventoida. Jos käytössä on USMF-esittelytietoja, voit valita nimikkeen A0001.  
3. Valitse **Muokkaa**.
4. Ota käyttöön **Varastonhallinta**-osan laajennus.
5. Valitse **Inventointiryhmä**-kentän avattavasta valikosta aiemmin luomasi inventointiryhmä. Tämä tuote lisätään, kun varaston inventoinnin kirjauskansion rivit luodaan tämän inventointiryhmän avulla.  
6. Valitse **Tallenna**.

## <a name="set-the-counting-policy-for-an-item-in-a-specific-warehouse"></a>Tietyn varaston nimikkeen inventointikäytännön määrittäminen
1. Valitse toimintoruudussa **Varastonhallinta**.
2. Valitse **Varastonimikkeet**.
3. Valitse **Uusi**.
4. Valitse **Varasto**-kentän avattavasta valikosta varasto, jolle haluat määrittää tiettyjä inventointikäytäntöjä.
5. Valitse inventointiryhmä **Inventointiryhmä**-kentän avattavasta valikosta. Voit valita tietyn inventointiryhmän, jota käytetään valitsemasi tietyn varaston nimikkeessä. Kun kyseisen varaston inventointi suoritetaan, inventointikäytäntö korvaa nimikkeen yleisen inventointikäytännön.  
6. Valitse **Tallenna**.

