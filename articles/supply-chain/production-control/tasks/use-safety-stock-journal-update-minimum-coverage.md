--- 
title: "Varmuusvaraston kirjauskansion käyttäminen minimikattavuuden päivittämiseen"
description: "Seuraavassa menettelyssä kuvataan, miten voit laskea vähimmäiskattavuuden ehdotukset historiatapahtumiin perustuen ja päivittää nimikekattavuuden ehdotusten mukaiseksi."
author: ChristianRytt
manager: AnnBe
ms.date: 10/27/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: d278b20724006ec3b3aa557738e8b130ca2bba15
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---
# Varmuusvaraston kirjauskansion käyttäminen minimikattavuuden päivittämiseen

[!include[task guide banner](../../includes/task-guide-banner.md)]

Seuraavassa menettelyssä kuvataan, miten voit laskea vähimmäiskattavuuden ehdotukset historiatapahtumiin perustuen ja päivittää nimikekattavuuden ehdotusten mukaiseksi. Tämä tehdään varmuusvaraston kirjauskansion avulla. Tämän tehtävän luomisessa käytetty esittely-yritys on USMF. Tämä tehtävä on tarkoitettu tuotannon suunnittelijalle minimikattavuuden ylläpitoa varten.


## Uuden varmuusvaraston kirjauskansion nimen luominen
1. Siirry kohtaan Varmuusvarastokirjauskansion nimet.
2. Valitse Uusi.
3. Kirjoita "Materiaali" nimi-kenttään.
4. Kirjoita Kuvaus-kentän arvoksi Materiaali.
5. Sulje sivu.

## Luo varmuusvaraston kirjauskansio
1. Siirry kohtaan Varmuusvaraston laskenta.
2. Valitse Uusi.
3. Syötä tai valitse arvo Nimi-kenttään.
    * Valitse luomasi varmuusvaraston kirjauskansion nimi, esimerkiksi Materiaali.  
4. Valitse Luo rivit.
5. Syötä päivämäärä Päivämäärästä-kenttään.
    * Aseta päiväksi "2015-01-02".  
6. Kirjoita päivämäärä Päivämäärään-kenttään.
    * Aseta päiväksi "2015-12-30".  
7. Valitse OK.
    * Tämä luo rivit dimensioille, joilla on varastotapahtumia.  

## Laske ehdotus
1. Napsauta kohtaa Laske ehdotus.
2. Valitse Käytä keskimääräistä varasto-ottoa läpimenoaikana -vaihtoehto.
3. Aseta kerroinarvoksi 10.
    * Kerroinarvoa käytetään ehdotuksen oikaisemiseen. Koska esittelytiedoissa on vain muutamia tapahtumia, kerroin on määritettävä, jos haluat realistisen ehdotuksen.  
4. Valitse OK.
    * Etsi M0002 ja M0003 alaspäin selaamalla. Näytä Laskettu vähimmäismäärä -sarake.   

## Päivitä vähimmäismäärä
1. Syötä numero Uusi vähimmäismäärä -kenttään.
    * Päivitä uusi vähimmäismäärä vastaavaan lasketun vähimmäismäärän arvoa. Jos laskettu vähimmäismäärä on nolla, voit syöttää haluamasi tulevan arvon. Voit esimerkiksi syöttää lasketun vähimmäismäärän tähän kenttään M0002 sisältävälle varastolle 12.  
2. Etsi haluamasi tietue luettelosta ja valitse se.
    * Voit valita esimerkiksi M0002 sisältävän varaston 12.  
3. Syötä numero Uusi vähimmäismäärä -kenttään.
    * Päivitä uusi vähimmäismäärä vastaavaan lasketun vähimmäismäärän arvoa. Jos laskettu vähimmäismäärä on nolla, voit syöttää haluamasi tulevan arvon.  

## Kirjaa uusi vähimmäismäärä ja vahvista tulos
1. Valitse Kirjaa.
2. Valitse OK.
3. Käytä Nimiketunnus-kentän linkkiä napsauttamalla.
4. Käytä Nimiketunnus-kentän linkkiä napsauttamalla.
5. Valitse toimintoruudussa Suunnitelma.
6. Valitse Nimikekattavuus.
    * Huomaa, että vähimmäismääräksi on päivitetty uusi vähimmäismäärä varmuusvaraston kirjauskansiosta.  


