--- 
title: Toimittajan laskun tallentaminen laskukirjauskansioon
description: "Tässä ohjauksessa näytetään, miten ostotilauksiin liittämättömät toimittajan laskut tallennetaan."
author: abruer
manager: AnnBe
ms.date: 11/15/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 127875443da1d43783440083b11afd423f2a12fe
ms.contentlocale: fi-fi
ms.lasthandoff: 07/27/2017

---
# <a name="record-a-vendor-invoice-in-the-invoice-journal"></a>Toimittajan laskun tallentaminen laskukirjauskansioon

[!include[task guide banner](../../includes/task-guide-banner.md)]

Tässä ohjauksessa näytetään, miten ostotilauksiin liittämättömät toimittajan laskut tallennetaan. Tällaisia laskuja ovat esimerkiksi tarvikkeiden tai palveluiden kulut.  Tässä tallenteessa käytetään esittely-yritystä USMF.

1. Siirry kohtaan Ostoreskontra > Työtilat > Toimittajan laskun syöttö.
2. Valitse Uusi laskukirjauskansio.
3. Valitse Uusi.
4. Avaa haku syöttämällä Nimi-kenttään kirjauskansion nimi tai valitsemalla avattavan valikon painike.
5. Kirjoita arvo Kuvaus-kenttään.
6. Valitse Rivit.
    * Syötä Päivämäärä-kenttään kirjauspäivämäärä, joka päivittää kirjanpidon.  
7. Määritä Toimittajan tili -kenttään haluamasi arvot.
8. Syötä Lasku-kenttään laskunumero.
9. Kirjoita Kuvaus-kenttään arvo.
10. Syötä Kredit-kenttään numero.
11. Avaa haku syöttämällä Vastatili-kenttään tilinumero nimi tai valitsemalla avattavan valikon painike
    * Arvonlisäveroryhmän oletusarvo saadaan toimittajan tililtä.  
    * Nimikkeen arvonlisäveroryhmän oletusarvo saadaan Vastatili-kentässä määritetyltä päätililtä.  
    * Eräpäivä lasketaan maksuehtojen perusteella.  
    * Käteisalennuksen oletusarvo saadaan toimittajan tililtä.  
12. Valitse Kirjaa.
13. Sulje sivu.


