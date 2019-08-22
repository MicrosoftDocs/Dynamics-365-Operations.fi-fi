---
title: Arvonlisäveron kirjanpidon kirjausryhmien määrittäminen
description: Arvonlisävero lasketaan ja kirjataan kirjanpidon kirjausryhmien päätileille.
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxAccountGroup
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6de914b5ca08b360db0bdb1ccb185b208d8d8ca6
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/01/2019
ms.locfileid: "1846292"
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

