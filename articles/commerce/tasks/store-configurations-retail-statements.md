---
title: Vähittäismyynnin laskelmien myymälän konfiguraatiot
description: Tässä menettelyssä esitellään myymälän konfiguraatiot, jotka vaikuttavat Commercen laskelmien luomiseen ja kirjaamiseen.
author: jashanno
manager: AnnBe
ms.date: 08/08/2019
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
ms.openlocfilehash: 57081b9e737373641cd9d884919d03dcf62a2ffe
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140652"
---
# <a name="store-configurations-for-retail-statements"></a>Vähittäismyynnin laskelmien myymälän konfiguraatiot

[!include [banner](../includes/banner.md)]

Tässä menettelyssä esitellään myymälän konfiguraatiot, jotka vaikuttavat Commercen laskelmien luomiseen ja kirjaamiseen. Myymälöiden taloushallinnon dimensioita käsitellään toisessa menettelyssä. Näissä toimintaohjeissa käytetään esittely-yritystä USRT.

1. Siirry **Siirtymisruudussa** kohtaan **Moduulit > Retail ja Commerce > Kanavat > Myymälät > Kaikki myymälät**.
2. Etsi haluamasi tietue luettelosta ja valitse se.
3. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
4. Valitse **Muokkaa**.
5. **Laskelma/sulkeminen**-pikavälilehden asetukset vaikuttavat laskelman luomiseen, oikeellisuustarkistukseen ja kirjaamiseen myymälässä. Laajenna **Laskelma/sulkeminen**-pikavälilehti.  
6. Valitse **Laskelmatapa**-kentässä laskelmarivien ryhmittelyssä käytettävä tapa.  
7. Valitse **Yksi laskelma päivässä** -kohdassa Kyllä, jos päivää kohti luodaan vain yksi laskelma, kun laskelmia luodaan laskelman luonnin erätyön avulla.  
8. **Kassan laskeminen maksuvälineittäin** -kentässä määritetään, lisätäänkö kassan laskemiset yhteen vai käytetäänkö viimeistä kassan laskemista.  
9. Valitse **Pyöristys**-kentässä kirjanpitotili, jolle pyöristyserot kirjataan.  
10. **Pyöristyseron enimmäissumma** -kenttään voi syöttää pyöristyseron sallitun enimmäissumman.
11. **Kirjaus**-kenttään voi syöttää laskelman kirjauksen sallitun enimmäiskokonaiseron.
12. **Vuoro**-kenttään voi syöttää laskelman enimmäiskokonaiseron.  
13. **Tapahtuma**-kenttään voi syöttää laskelmarivin enimmäiskokonaiseron.  
14. **Sulkemistapa**-kenttään voi määrittää, ovatko laskelmaan sisällytettävät tapahtumat osa suljettua vuoroa vai voivatko ne olla mitä tahansa määritetyn päivämäärä-/aikavälin tapahtumia.  
15. **Työpäivän päätös** -kenttään voi syöttää ajan, jos keskiyön jälkeiset tapahtumat tulee kirjata edelliselle päivälle.  
16. Valitse **Kirjaa työpäivänä** -kohdassa Kyllä, jos keskiyön jälkeiset tapahtumat kirjataan edellisen päivän osaksi.  
17. Valitse **Jakoperusteena laskelmatapa** -kohdassa Kyllä, kun jokaiselle määritetylle laskelmatavalle luodut laskelmat haetaan. Tämä voi olla hyödyllistä, jos kirjauksen suoritustasoa on parannettava myymälöissä, joiden tapahtumamäärät ovat suuria, ja halutaan useita pieniä rinnakkain käsiteltäviä laskelmia.  
18. Valitse **Yleiset**-pikavälilehdessä **Oletusasiakas**-kentässä myymälässä asioineiden asiakkaiden myynnissä käytettävä asiakastili.  

