---
title: Asiakkaan maksun yhteenveto
description: Tässä tehtävän ohjauksessa kerrotaan asiakkaan maksujen syöttämisessä käytettävät tavat.
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, CustPaymEntry, CustTableLookup, LedgerJournalTransCustPaym, CustOpenTrans, BankAccountTableLookUp
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6e82be0d68165f62bbdc72a70b0675c7418b14ae
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/15/2019
ms.locfileid: "1566130"
---
# <a name="customer-payment-overview"></a>Asiakkaan maksun yhteenveto

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tässä tehtävän ohjauksessa kerrotaan asiakkaan maksujen syöttämisessä käytettävät tavat. Tässä tehtävässä käytetään esittely-yritystä USMF.

1. Siirry kohtaan Myyntireskontra > Maksut > Maksukirjauskansio.
2. Valitse Uusi.
3. Valitse maksukirjauskansio, johon asiakkaan maksut tallennetaan.
4. Valitse kirjauskansio tai syötä se manuaalisesti.
5. Valitse Lisää asiakkaan maksuja.
    * Lisää asiakkaan maksuja -sivua käytetään tallennettaessa yksi asiakkaan maksu kerralla. Voit syöttää samalla sivulla maksun tiedot (sivun yläosassa) ja maksun yhteydessä maksetut laskut.  
6. Syötä asiakas, jolta vastaanotit maksun.
    * Jos et tiedä asiakasta, mutta tiedät maksetun tapahtuman, voit syöttää maksun Tapahtuma-kenttään. Syötä tai valitse lasku Tapahtuma-kentässä. Asiakas haetaan automaattisesti tapahtuman valitsemisen jälkeen.  
7. Syötä Maksuviite-kenttään maksuviite.
    * Maksuviite voi olla asiakkaan sekkinumero tai asiakkaan sähköisen maksun viite. Maksuviite vaaditaan vain, jos maksu on merkitty talletuskuittiin sisällytettäväksi.  
8. Määritä, sisällytetäänkö maksu tallennuskuittiin. 
9. Syötä asiakkaan maksun summa.
    * Maksun summaa ei haeta automaattisesti. Se on syötettävä manuaalisesti.  
10. Merkitse asiakkaan maksamat laskut.
    * Jos maksu ennakkomaksu, laskuja ei tarvitse merkitä selvitystä varten. Maksun voi silti tallentaa ja kirjata. Laskun selvitys voidaan tehdä myöhemmin.  
11. Syötä sen maksun summa, joka selvitetään merkitylle laskulle. 
    * Tätä kenttää voi käyttää, kun maksu koskee osittaista maksua. Jos et syötä summaa, selvitettävä summa määritetään automaattisesti.  
12. Valitse Tallenna kirjauskansioon.
    * Ennen kuin tallennat maksun kirjauskansioon, varmista, että vastatili on määritetty. Kun kirjauskansiossa käytetään Tallenna-toimintoa, maksu tallennetaan ja siirretään kirjauskansioon. Tämän jälkeen voit jatkaa seuraavan maksun syöttämistä.  
13. Sulje sivu.
14. Valitse Rivit.
    * Kun avaat Rivit-kohdan, näkyviin tulevat Lisää asiakkaan maksuja -sivulla tallennetut ja kirjauskansioon siirretyt maksut. Tällä sivuilla voi myös syöttää uusia asiakkaan maksuja tai muokata aiemmin luotuja asiakkaan maksuja, ennen kuin ne kirjataan.  
15. Luo toinen maksu valitsemalla Uusi. 
16. Valitse asiakas, jolta vastaanotit maksun.
    * Jos et tiedä asiakasta, mutta tiedät, että maksun lasku on maksettu, syötä lasku manuaalisesti Lasku-kenttään tai valitse lasku siellä. Asiakas määritetään, kun lasku on valittu.  
17. Merkitse maksetut laskut valitsemalla Selvitä tapahtumat.
    * Yhdenkään laskun maksua ei tarvitse selvittää. Jos tämä on ennakkomaksu tai jos et tiedä maksettua laskua, voit syöttää ja kirjata maksun. Maksu voidaan tilittää laskulle myöhemmin.  
18. Merkitse maksussa maksetut laskut. 
19. Syötä sen maksun summa, joka selvitetään laskulle.
20. Valitse OK.
21. Syötä Maksuviite-kenttään maksuviite. .
    * Maksuviite vaaditaan vain, jos maksu on merkitty talletuskuittiin sisällytettäväksi.  
22. Kirjaa asiakkaan maksut. 

