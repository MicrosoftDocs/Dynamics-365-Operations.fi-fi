--- 
title: "Määritä hankintaluokkahierarkia"
description: "Tässä menettelyssä selvitetään, miten voit luoda uusia solmuja hankintaluokkahierarkiaan ja miten hankintaprosessissa käytettävä hankintaluokka määritetään."
author: mkirknel
manager: AnnBe
ms.date: 11/06/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 6ad5c8552a6989e9093d0b1325754bc0f6d19372
ms.openlocfilehash: 4541d029c9c3be3ee42332e5d8ff183dd503f13e
ms.contentlocale: fi-fi
ms.lasthandoff: 11/06/2017

---
# <a name="set-up-a-procurement-category-hierarchy"></a>Määritä hankintaluokkahierarkia

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tässä menettelyssä selvitetään, miten voit luoda uusia solmuja hankintaluokkahierarkiaan ja miten hankintaprosessissa käytettävä hankintaluokka määritetään. Yleensä ostopäällikkö tekee nämä tehtävät. Ennen menettelyn aloittamista on oltava Hankita-tyyppinen luokkahierarkia. Jos käytössä on demotietoyritys, voit suorittaa tämän menettelyn USMF-yrityksessä.


## <a name="add-a-new-procurement-category"></a>Lisää uusi hankintaluokka
1. Valitse Hankinta > Hankintaluokat.
2. Valitse Muokkaa luokkahierarkiaa.
    * Nykyisen hankintaluokkahierarkia näkyy sivun vasemmalla puolella. Olet muokkaamassa hierarkiaa.  
3. Valitse Uusi luokkasolmu.
    * Järjestelmä valitsee oletusarvoisesti ylimmän solmun. Jos käytät menettelyä tehtävän ohjauksena, voit napsauttaa Poista lukitus -painiketta ja valita toisen pääsolmun, johon voit lisätä uuden solmun. Kun tämä on tehty, lukitse tehtäväopas uudelleen ja napsauta Uusi luokka -solmua.  
4. Kirjoita arvo Nimi-kenttään.
5. Kirjoita arvo Kuvaus-kenttään.
6. Kirjoita Kutsumanimi-kenttään arvo.
    * Kutsumanimi on valinnainen. Se näkyy luokkahauissa yhdessä luokan nimen kanssa.  
7. Valitse Tallenna.

## <a name="add-products-to-your-new-procurement-category"></a>Lisää tuotteita uuteen hankintaluokkaan
1. Valitse Hankinta > Hankintaluokat.
    * Valitse juuri lisäämäsi solmu. Jos käytät menettelyä tehtävän ohjauksena, sinun on ehkä poistettava lukitus, ennen kuin voit valita solmun.  
2. Ota Tuotteet-osion laajennus käyttöön.
3. Liitä tuotteet hankintaluokkaan valitsemalla Lisää.
4. Valitse hankintaluokkaan lisättävä tuote.
5. Valitse tuote napsauttamalla nuolta.
6. Valitse toinen hankintaluokkaan lisättävä tuote.
7. Valitse tuote napsauttamalla nuolta.
8. Valitse OK.

## <a name="add-approved-and-preferred-vendors"></a>Lisää hyväksyttyjä tai ensisijaisia toimittajia
1. Ota käyttöön Toimittajat-osan laajennus.
2. ValitseLisää.
    * Voit lisätä toimittajan hankintaluokkaan ja määrittää, onko toimittaja luokassaan ensisijainen vai luokkaan vain hyväksytty toimittaja. Kun poistat toimittajan luokasta, toimittajan ja luokan aiempia tapahtumia ei poisteta.   
3. Etsi hankintaluokkaan lisättävä toimittaja.
4. Valitse toimittaja napsauttamalla nuolta.
5. Valitse OK.
6. Valitse sen toimittajan rivi, jonka tietoja haluat muokata.
7. Valitse vaihtoehto Toimittajan tila -kentässä.
    * Luokan käytäntösäännöissä oleva toimittajan valinta-asetus määrittää, onko ostoehdotuksissa valittavissa ensisijaiset, hyväksytyt vai kaikki toimittajat.   

## <a name="add-additional-information-to-the-category"></a>Lisää lisätiedot luokkaan
1. Ota Toimittajan arviointiehtoryhmät -osan laajennus käyttöön.
    * Voit määrittää tässä välilehdessä ehdot, joilla hankintaluokan toimittajat luokitellaan. Voit tehdä sen valitsemalla ensin Lisää ja valitse sitten sen toimittaja-arviointiryhmän, jonka ehtoja haluat käyttää.  
2. Ota Kyselylomakkeet-osan laajennus käyttöön.
    * Voit lisätä tässä välilehdessä varasto-ottoehdotuksessa näkyviä kyselylomakkeita, kunhan tehtävän tyypiksi on valittu Varasto-ottoehdotus. Pyynnön lähettäjän on sitten täytettävä kyselylomake, ennen kuin he voivat lähettää tietyn tuotteen tai hankintaluokan tuotteiden varasto-ottoehdotuksen.  
3. Ota Nimikkeiden arvonlisäveroryhmät -osan laajennus käyttöön.
4. Avaa haku valitsemalla Nimikkeen arvonlisäveroryhmä: -kentässä avattavan valikon painike.
5. Valitse arvonlisäveroryhmä.
6. Ota Luokkasivu--osan laajennus käyttöön.
    * Luokkasivut luodaan Luokkahierarkia-sivulla. Niissä on esimerkiksi seuraavia tietoja hankintaluokista: tiedot luokan tuotetyypeistä, luokan tuotteiden kuvat ja ilmoitukset, kuten luokassa käytettävissä olevat alennukset. Luokkasivulla olevat tiedot näytetään ostoehdotuksissa.  
7. Sulje sivu.


