---
title: Määritä kanta-asiakasmallit
description: Tässä menettelyssä kerrotaan, miten kanta-asiakkuusmalli määritetään.
author: jashanno
manager: AnnBe
ms.date: 11/14/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: eb1afb0ebce742fa2f6accd65e553df6607107a4
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4972277"
---
# <a name="define-loyalty-schemes"></a>Määritä kanta-asiakasmallit

[!include [banner](../includes/banner.md)]

Tässä menettelyssä kerrotaan, miten kanta-asiakkuusmalli määritetään. Kanta-asiakkuusmallit ovat kanta-asiakasohjelman ansainta- ja lunastussääntöjä. Menettely käyttää esittelytietojen USRT-yritystä.

1. Siirry kohtaan Retail ja Commerce > Asiakkaat > Kanta-asiakkaat > Kanta-asiakasohjelmat.
2. Valitse Uusi.
3. Kirjoita Mallin tunnus -kenttään arvo.
4. Kirjoita arvo Kuvaus-kenttään.
5. Avaa haku valitsemalla Nimi-kentässä avattavan valikon painike.
    * Kanta-asiakasohjelma voi sisältää useita kanta-asiakkuusmalleja. Kanta-asiakkuusmallit voivat koskea kaikkia kanavia tai kanavien alajoukkoa.  
6. Etsi haluamasi tietue luettelosta ja valitse se.
7. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
8. Valitse Tallenna.
9. Valitse Lisää rivi.
10. Valitse Tehtävätyyppi-kentässä vaihtoehto.
    * Valitse Osta tuotteita summan mukaan, jos haluat, että asiakkaat ansaitsevat edut kulutuksen määrän mukaan. Valitse Osta tuotteita määrän mukaan, jos haluat, että asiakkaat ansaitsevat edut ostettujen tuotteiden lukumäärän mukaan.  Valitse Myyntitapahtuman summa, jos asiakkaat voivat ansaita edut kustakin myyntitapahtumasta riippumatta siitä, mitä tai miten paljon ostetaan.  
    * Valitse luokka. Luokka rajaa tuotteet, joihin tämä ansaintasääntö kohdistetaan.  
    * Jos haluat, että ansaintasääntöä käytetään kaikille asiakkaille, jätä tämä kenttä tyhjäksi.  
11. Syötä Tehtävän summa/määrä -kenttään numero.
    *  Jos tehtävän tyyppi on Myyntitapahtuman summa, arvoksi on aina syötettävä 1,0. Jos tehtävän tyyppi on Osta summan mukaan tai Osta määrän mukaan, tapahtuma, jonka arvo on syötettyä pienempi, ei käynnistä ansaintasääntöä. Jos esimerkiksi tehtävätyyppi on Osta summan mukaan, ja arvoksi syötetään 10,00, myyntitapahtumasta, jonka arvo on 9,00, ei ansaita etuja tämän ansaintasäännön mukaan.  
12. Syötä Tehtävän valuutta -kenttään arvo.
13. Avaa haku valitsemalla Palkkiopisteen tunnus -kentässä avattavan valikon painike.
14. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
15. Syötä Palkkiopisteet-kenttään numero.
    * Palkkiopisteet, joiden tyyppi on Summa, tallennetaan desimaalilukuina. Jos ansaintasääntö määrittää esimerkiksi 1 palkkiopisteen jokaista käytettyä euroa kohti, asiakas ansaitsee 1,25 palkkiopistettä, kun hän ostaa 1,25 eurolla. Palkkiopisteet, joiden tyyppi on Määrä, tallennetaan kokonaislukuina. Jos ansaintasääntö määrittää esimerkiksi 1 palkkiopisteen jokaista käytettyä euroa kohti, asiakas ansaitsee 1,0 eurolla palkkiopistettä, kun hän ostaa 1,25 eurolla.  
16. Valitse Tallenna.
17. Valitse Lisää rivi.
    * Lunastussääntöjä käytetään, kun käytössä on kanta-asiakkuuden maksutapa.  
18. Avaa haku valitsemalla Palkkiopisteen tunnus -kentässä avattavan valikon painike.
    * Näkyvissä ovat vain lunastettavat palkkiopisteet.  
19. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
20. Syötä Palkkiopisteet-kenttään numero.
21. Valitse Lunastustyyppi-kentässä vaihtoehto.
    * Jos valittuna on Maksu summan mukaan, Summa- tai Määrä-kenttää pidetään valuutan arvona. Tässä tapauksessa maksun valuuttayksiköissä käytettävä palkkiopisteiden summa on kiinteä taksa. Jos valittuna on Maksu määrän mukaan, Summa- tai Määrä-kenttää pidetään määrän arvona. Tässä tapauksessa maksun nimikkeen määrässä käytettävä palkkiopisteiden summa on kiinteä taksa. Valuuttasumma voi kuitenkin vaihdella, jos kanta-asiakkaan palkkiopisteiden nimikkeiden hinta vaihtelee tiettyä määrää kohti. Kanta-asiakkuuspistealennuksen lunastustyyppi on käytössä vain, kun maa-/aluekohtaisten ominaisuuksien määritysavain Venäjä on käytössä ja myyntipisteen toimintoprofiilien ISO-koodi on RU.  
    * Valitse luokka. Luokka rajaa tuotteet, joihin tämä lunastussääntö kohdistetaan.  
    * Jos haluat, että lunastussääntöä käytetään kaikille asiakkaille, jätä tämä kenttä tyhjäksi.  
22. Lisää Summa tai määrä -kenttään numero.
23. Kirjoita arvo Valuutta-kenttään.
24. Valitse Tallenna.
25. Valitse Lisää rivi.
    * Valitse vähintään yksi solmu Käytettävissä olevat organisaatiosolmut -luettelosta ja siirrä solmu/solmut Valitut organisaatiosolmut -luetteloon valitsemalla kahden luettelon välinen nuoli.  
26. Valitse OK.
27. Valitse Tallenna.
    * Käsittele kanta-asiakkuusmallit -kohta on suoritettava aina, kun kanta-asiakkuusmallin kanavia muutetaan. Näin kanavien kanta-asiakkuusmallit päivitetään.  

