--- 
title: "Arvonlisäveron kirjanpidon kirjausryhmien määrittäminen"
description: "Arvonlisävero lasketaan ja kirjataan kirjanpidon kirjausryhmien päätileille."
author: ShylaThompson
manager: AnnBe
ms.date: 10/26/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ef3cad6538d9efbd1c1881f4b7d771382d9b1ba8
ms.openlocfilehash: e50fc2b6b8f4cd91e9a5593297fff2e9a6ef5525
ms.contentlocale: fi-fi
ms.lasthandoff: 10/26/2017

---
# <a name="set-up-ledger-posting-groups-for-sales-tax"></a>Arvonlisäveron kirjanpidon kirjausryhmien määrittäminen

[!include [task guide banner](../../includes/task-guide-banner.md)]

Arvonlisävero lasketaan ja kirjataan kirjanpidon kirjausryhmien päätileille. Kirjanpidon kirjausryhmät liitetään kuhunkin arvonlisäverokoodiin. Voit määrittää kullekin arvonlisäverokoodille kirjanpidon kirjausryhmät käyttämällä kaikissa arvonlisäverokoodeissa yhtä kirjanpidon kirjausryhmää tai liittämällä arvonlisäverokoodeille useita kirjanpidon kirjausryhmiä. Tässä tallenteessa käytetään esittely-yritystä DEMF. 

1. Siirry kohtaan Vero > Asetukset > Arvonlisävero > Kirjanpidon kirjausryhmät.
2. Valitse Uusi.
3. Kirjoita arvo Kirjanpidon kirjausryhmä -kenttään.
4. Kirjoita arvo Kuvaus-kenttään.
5. Valitse Maksettava arvonlisävero -kentässä päätili lähtevälle arvonlisäverolle, joka maksetaan veroviranomaiselle.
    * Arvonlisäverot kerätään veroviranomaisen puolesta, kun verollisia tavaroita ja palveluja myydään.  
6. Valitse Saatava arvonlisävero -kentässä päätili saapuvalle arvonlisäverolle, joka vastaanotetaan veroviranomaiselta.
    * Toimittajat keräävät verot veroviranomaisen puolesta, kun verollisia tavaroita ja palveluja ostetaan. Tämä kenttä ei ole käytettävissä, jos Käytä arvonlisäverotuksen sääntöjä -vaihtoehto on valittu Kirjanpitoparametrit-sivulla. Sen sijaan toimittajille maksettavat arvonlisäverot hyvitetään samalta tililtä kuin ostot.   
7. Valitse Käyttöverokulu-kentässä päätili niille vähennettäville käyttöveroille, joita veroviranomainen ei peri tai joita toimittajat eivät raportoi veroviranomaiselle osana EU:n käännettyä GOT/HS-veroa.
    * Tapahtumassa käytettävän arvonlisäveroryhmän arvonlisäverokoodin Käyttövero-vaihtoehto on valittava.  Tämä kenttä ei ole käytettävissä, jos Käytä arvonlisäverotuksen sääntöjä -vaihtoehto on valittu Kirjanpitoparametrit-sivulla.   
8. Valitse Maksettava käyttövero -kentässä päätili veroviranomaiselle maksettavien saapuvien käyttöverojen kirjaamista varten.
    * Arvonlisäveroryhmän arvonlisäverokoodin Käyttövero-vaihtoehto on valittava, kun käyttövero kirjataan. Jos kirjanpidon parametrien Käytä arvonlisäverotuksen sääntöjä -vaihtoehto on valittu, vastakirjaus kirjataan tapahtuman kulutilille.   
9. Valitse Tilitystili-kentässä päätili, jolle Maksettava käyttövero- ja Saatava arvonlisävero -kentässä määritettyjen kirjanpitotilien nettosaldo kirjataan.
    * Saldo luodaan, kun arvonlisäveron tilitys ja työn kirjaaminen suoritetaan.  Jos tilityskauden veroviranomainen on liitetty toimittajan tiliin, saldo kirjataan sen sijaan toimittajan tiliin.   
10. Valitse Toimittajan käteisalennus -kentässä päätili, jonne tähän kirjanpidon kirjausryhmän liitetyn arvonlisäverokoodin käteisalennukset kirjataan.
    * Tämä kenttä on valinnainen. Jos tiliä ei ole syötetty, käytetään käteisalennuksen koodien päätiliä. Kirjanpidon kirjausryhmässä saattaa kannattaa käyttää eri tilejä, jos käytössä on arvonlisäveroryhmien Mitätöi käteisalennuksen arvonlisävero -kohta.  
11. Valitse Asiakastapauksen alennus -kentässä päätili, jonne tähän kirjanpidon kirjausryhmän liitetyn arvonlisäverokoodin käteisalennukset kirjataan.
    * Tämä kenttä on valinnainen. Jos tiliä ei ole syötetty, käytetään käteisalennuksen koodien päätiliä. Kirjanpidon kirjausryhmässä saattaa kannattaa käyttää eri tilejä, jos käytössä on arvonlisäveroryhmien Mitätöi käteisalennuksen arvonlisävero -kohta.  
12. Valitse Tallenna.


