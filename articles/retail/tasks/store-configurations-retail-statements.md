--- 
title: "Vähittäismyynnin laskelmien myymälän konfiguraatiot"
description: "Tässä menettelyssä esitellään vähittäismyymälän konfiguraatiot, jotka vaikuttavat vähittäismyynnin laskelmien luomiseen ja kirjaamiseen."
author: jashanno
manager: AnnBe
ms.date: 11/14/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: 441ba692f559f9966f3e2512c7760ad2f732b768
ms.contentlocale: fi-fi
ms.lasthandoff: 02/07/2018

---
# <a name="store-configurations-for-retail-statements"></a>Vähittäismyynnin laskelmien myymälän konfiguraatiot

[!include [task guide banner](../includes/task-guide-banner.md)]

Tässä menettelyssä esitellään vähittäismyymälän konfiguraatiot, jotka vaikuttavat vähittäismyynnin laskelmien luomiseen ja kirjaamiseen. Vähittäismyymälöiden taloushallinnon dimensioita käsitellään toisessa menettelyssä. Näissä toimintaohjeissa käytetään esittely-yritystä USRT.

1. Siirry kohtaan Vähittäismyynti ja kauppa > Kanavat > Vähittäismyymälät > Kaikki vähittäismyymälät.
2. Etsi haluamasi tietue luettelosta ja valitse se.
3. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
    * Laskelma/sulkeminen-osan asetukset vaikuttavat laskelman luomiseen, oikeellisuustarkistukseen ja kirjaamiseen myymälässä.  Avaa Laskelma/sulkeminen-osa.  
    * Valitse laskelmarivien ryhmittelyssä käytettävä tapa.  
    * Valitse Kyllä, jos päivää kohti luodaan vain yksi laskelma, kun laskelmia luodaan laskelman luonnin erätyön avulla.  
    * Kassan laskeminen maksuvälineittäin -kentässä määritetään, lisätäänkö kassan laskemiset yhteen vai käytetäänkö viimeistä kassan laskemista.  
    * Valitse kirjanpitotili, jolle pyöristyserot kirjataan.  
    * Pyöristyseron enimmäissumma -kenttään voi syöttää pyöristyseron sallitun enimmäissumman.  
    * Kirjaus-kenttään voi syöttää laskelman kirjauksen sallitun enimmäiskokonaiseron.  
    * Vuoro-kenttään voi syöttää laskelman enimmäiskokonaiseron.  
    * Tapahtuma-kenttään voi syöttää laskelmarivin enimmäiskokonaiseron.  
    * Sulkemistapa-kenttään voi määrittää, ovatko laskelmaan sisällytettävät tapahtumat osa suljettua vuoroa vai voivatko ne olla mitä tahansa määritetyn päivämäärä-/aikavälin tapahtumia.  
    * Työpäivän päätös -kenttään voi syöttää ajan, jos keskiyön jälkeiset tapahtumat tulee kirjata edelliselle päivälle.  
    * Valitse Kyllä, jos keskiyön jälkeiset tapahtumat kirjataan edellisen päivän osaksi.  
    * Valitse Kyllä, kun jokaiselle määritetylle laskelmatavalle luodut laskelmat haetaan. Tämä voi olla hyödyllistä, jos kirjauksen suoritustasoa on parannettava myymälöissä, joiden tapahtumamäärät ovat suuria, ja halutaan useita pieniä rinnakkain käsiteltäviä laskelmia.  
    * Valitse Oletusasiakas-kentässä myymälässä asioineiden asiakkaiden myynnissä käytettävä asiakastili.  


