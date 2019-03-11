---
title: Vähittäismyynnin laskelmien myymälän konfiguraatiot
description: Tässä menettelyssä esitellään vähittäismyymälän konfiguraatiot, jotka vaikuttavat vähittäismyynnin laskelmien luomiseen ja kirjaamiseen.
author: jashanno
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailStoreTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9fddeb8434d916df1613d61da88110dec8fb4465
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "354710"
---
# <a name="store-configurations-for-retail-statements"></a>Vähittäismyynnin laskelmien myymälän konfiguraatiot

[!include[task guide banner](../includes/task-guide-banner.md)]

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

