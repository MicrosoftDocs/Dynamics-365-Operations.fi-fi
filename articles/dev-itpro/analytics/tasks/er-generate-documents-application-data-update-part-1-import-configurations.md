--- 
title: "Tuo konfiguraatioita luodaksesi sovellustietoja sisältäviä asiakirjoja"
description: "ER Konfiguraation lähteen luominen ja sen merkitseminen aktiiviseksi -menettelyn vaiheet on suoritettava ennen tämän menettelyn vaiheiden suorittamista."
author: NickSelin
manager: AnnBe
ms.date: 11/02/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: 1637ba59525f5f8bd9fe41a00c34eca90f7a2751
ms.contentlocale: fi-fi
ms.lasthandoff: 08/08/2018

---
# <a name="import-configurations-to-generate-documents-that-have-application-data"></a>Tuo konfiguraatioita luodaksesi sovellustietoja sisältäviä asiakirjoja

[!include [task guide banner](../../includes/task-guide-banner.md)]

ER Konfiguraation lähteen luominen ja sen merkitseminen aktiiviseksi -menettelyn vaiheet on suoritettava ennen tämän menettelyn vaiheiden suorittamista.

Tämän menettelyn vaiheissa opastetaan, miten sähköisen raportoinnin (ER) konfiguraatiot suunnitellaan sähköisen asiakirjan luomista varten. Tässä menettelyssä tuodaan pakollisia ER-konfiguraatioita, jotka on luotu malliyritykselle Litware Inc. ja joita käytetään sähköisten asiakirjojen luomisessa. Tämä menettely on luotu käyttäjille, joille on määritetty järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooli. Nämä vaiheet voidaan suorittaa DEMF-tietojoukon avulla. Ennen kuin aloitat, lataa ja tallenna Sähköisten asiakirjojen luominen ja sovellustietojen päivittäminen sähköisen raportoinnin työkalulla -ohjeaiheen tiedostot (generate-electronic-documents-update-application-data/). Tiedostot ovat Intrastat (model).xml, Intrastat (mapping).xml ja Intrastat (format).xml.

1. Siirry kohtaan Organisaation hallinto > Työtilat > Sähköinen raportointi.
    * Varmista, onko Litware, Inc. -malliyrityksen konfiguraation lähde käytettävissä ja merkitty aktiiviseksi. Jos konfiguraation lähde ei ole näkyvissä, suorita Konfiguraation lähteen luominen ja sen merkitseminen aktiiviseksi -menettelyn vaiheet.  
    * Tämän menettelyn vaiheissa kerrotaan, miten sovellustietojen päivitys suoritetaan ER-ominaisuuksien avulla ja miten Intrastat-raportti luodaan. Raportointiprosessin tiedot arkistoidaan sovellustauluihin. Kun Intrastat-raportointiprosessi aktivoidaan Intrastat-lomakkeesta, arkistointi tehdään tällä hetkellä aiemmin määritetyssä lähdekoodissa ohjelmoidun logiikan perusteella. Tässä menettelyssä määritetään samanlainen mutta yksinkertaisempi sovelluslogiikka pelkän sähköisen raportoinnin avulla. Lähdekoodia ei muuteta.   

## <a name="import-er-configurations"></a>ER-konfiguraatioiden tuominen
1. Valitse Raportointikonfiguraatiot.
2. Valitse Vaihto.
3. Valitse Lataa XML-tiedostosta.
    * Tuo ER-mallin konfiguraatio, joka sisältää tietomallin, joka on tarkoitettu tietolähteeksi Intrastat-raportin luomista varten. Myöhemmin tätä tietomallin määritelmää laajennetaan niin, että sitä käytetään sovellustietojen päivityksessä, kun Intrastat-raportointiprosessin tiedot arkistoidaan.   
    * Valitse Selaa ja valitse sitten Intrastat (model).xml -tiedosto.  
4. Valitse OK.
5. Valitse puussa Intrastat (model).
6. Valitse Suunnittelutoiminto.
7. Laajenna puussa For outgoing document.
8. Laajenna puussa For outgoing document\Transactions.
    * Tarkista tuodun tietomallin rakenne. Ota huomioon, että lähtevän asiakirjan juurinimike on määritetty niin, että se määrittää sovelluksesta saatavan tietovirran, jota käytetään tietolähteenä Intrastat-raportin luomisessa. Tapahtumat (tietueluettelo) -kohtaa käytetään raportoitavien Intrastat-tapahtumien luettelon esittämisessä. Koska raportoidut kauppatavarakoodit arkistoidaan, tässä tietovirrassa tarvitaan yksittäisen kauppatavarakoodin tunnusta Kauppatavaratietueen tunnus (Int64).   
9. Sulje sivu.
10. Valitse Vaihto.
11. Valitse Lataa XML-tiedostosta.
    * Tuo ER-yhdistämismäärityksen konfiguraatio, joka määrittää tietovirran sovelluksen tietojen hakua varten. Tämän jälkeen tietovirtaa käytetään Intrastat-raportin luomisessa. Myöhemmin tätä mallin yhdistämismääritystä laajennetaan Intrastat-raportin tietojen hakua ja sovellustietojen päivitystä varten, kun Intrastat-raportointiprosessin tiedot arkistoidaan.   
    * Valitse Selaa ja valitse sitten Intrastat (mapping).xml -tiedosto.  
12. Valitse OK.
13. Laajenna puussa Intrastat (model).
14. Valitse puussa Intrastat (model)\Intrastat (mapping).
15. Valitse Suunnittelutoiminto.
    * Ota huomioon, että nykyinen mallin yhdistämismääritys sisältää Malliin-arvon Suunta-kentässä. Tämä tarkoittaa sitä, että mallin yhdistämismääritys on määritetty hakemaan tiedot sovelluksesta ja tallentamaan ne tietomalliin.  
16. Valitse Suunnittelutoiminto.
17. Laajenna puussa List.
18. Laajenna puussa Transactions= List.
    * Tarkista sen mallin yhdistämismärityksen rakenne, joka suodatetaan lähtevän asiakirjan juurinimikkeen perusteella. Huomaa, että lisätty tietolähde, Luettelo, sisältää vaadittujen sovellustietojen käyttöoikeudet (Intrastat-taulun tietueiden luettelo).  
19. Sulje sivu.
20. Sulje sivu.
21. Valitse Vaihto.
22. Valitse Lataa XML-tiedostosta.
    * Tuo ER-muodon konfiguraatio, joka määrittää Intrastat-raportin asettelun ja raportin tietojen täyttämisprosessin. Myöhemmin tätä muodon määritystä laajennetaan Intrastat-raportin tietojen siirtämiseksi tietomalliin. Tämän jälkeen sitä käytetään sovellustietojen päivityksessä, kun Intrastat-raportointiprosessin tiedot arkistoidaan.   
    * Valitse Selaa ja valitse sitten Intrastat (format).xml -tiedosto.  
23. Valitse OK.
24. Valitse puussa Intrastat (model)\Intrastat (format).
25. Valitse Suunnittelutoiminto.
26. Valitse Laajenna tai tiivistä.
27. Valitse puussa File\Declaration.
28. Valitse Yhdistämismääritys-välilehti.
29. Valitse puussa File.
    * Tarkista Intrastat-raportin luonnissa käytettävän muodon rakenne. Ota huomioon, että se on määritetty luomaan XML-tiedosto niin, että tiedot täytetään lähtevän asiakirjan juurinimikkeeseen perustuvasta tietomallista. Tarkista, että luodun tiedoston nimi on määritetty käyttäjän valintanäytössä (tässä käytetään fn-tietolähdettä).   
30. Sulje sivu.


