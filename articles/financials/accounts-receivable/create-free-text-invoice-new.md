--- 
title: Luo tekstimuotoinen lasku
description: "Tässä artikkelissa näytetään miten tekstimuotoinen myyntilasku luodaan."
author: mikefalkner
manager: AnnBe
ms.date: 05/29/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f69505f0c6137121cae92d42d052b244326c8436
ms.openlocfilehash: 2a611bdd4dd97109709ed355eb80471e27413744
ms.contentlocale: fi-fi
ms.lasthandoff: 06/28/2018

---

# <a name="create-a-free-text-invoice"></a>Luo tekstimuotoinen lasku

[!include [banner](../includes/banner.md)]

Tässä artikkelissa näytetään miten tekstimuotoinen myyntilasku luodaan. Tässä menettelyssä käytetään USMF-demoyritystä.

## <a name="create-a-free-text-invoice"></a>Luo tekstimuotoinen lasku

1. Siirry kohtaan Myyntireskontra > Laskut > Kaikki vapaatekstilaskut.
2. Valitse Uusi.
3. Valitse arvo Asiakastili-kenttään.
    * Laskutustili on oletusarvoisesti sama kuin asiakastili.   
    * Kirjanpidon tila alkaa Käsittelyssä-tilasta, jos laskua ei ole kirjattu.   
    * Laskunumero liitetään, kun lasku on kirjattu.  
    * Kun käytössä ovat SEPA-valtakirjat, suoraveloitusvaltakirja täytetään automaattisesti asiakastilin valinnan yhteydessä.  
4. Kirjoita arvo Kuvaus-kenttään.
5. Määritä Päätili-kenttään tilinumero ilman dimensioita.
    * Voit myös syöttää päätilille yhden tai useamman merkin ja käyttää valintaa etsiessäsi tiliä. Dimensiot syötetään myöhemmin.  
6. Laajenna Rivin tiedot -pikavälilehti niin, että voit lisätä päätilille dimensioita.
7. Valitse Taloushallinnon dimensiot -välilehti.
    * Dimensiot kuuluvat vain valitulle riville.    
    * Arvonlisäveroryhmän tiedot täytetään asiakkaan tiedoilla. Jos asiakkaalla ei ole arvonlisäveroryhmää, käytetään päätilin arvonlisäveroryhmää.  
    * Nimikkeiden arvonlisäveroryhmän tiedot täytetään päätilin tiedoilla. Jos päätilillä ei ole nimikkeen arvonlisäveroryhmää, käytetään kirjanpidon arvolisäveroparametrin nimikkeen arvonlisäveroryhmää.    
8. Kirjoita numero Määrä-kenttään.
    * Määrä on valinnainen tieto.  
9. Syötä Yksikköhinta-kenttään numero.
    * Yksikköhinta on valinnainen tieto.  
    * Summa lasketaan kertomalla määrä yksikköhinnalla. Voit kuitenkin ohittaa laskennan ja syöttää summan.  
10. Tarkastele laskulle laskettua arvonlisäveroa valitsemalla Arvonlisävero.
    * Voit tarkastella tämän sivun arvonlisäverosummia tai korvata summat Oikaisu-välilehdessä.  
11. Valitse OK.
12. Lisää laskuun kulu valitsemalla Kulut. 
13. Kirjoita Kulujen koodi -kenttään arvo.
14. Syötä Kulujen arvo -kenttään numero.
15. Sulje sivu.
16. Tarkastele yhteenvetolaskun tietoja ja summia valitsemalla Summat.
17. Valitse Sulje.
18. Kirjaa lasku valitsemalla Kirjaa. Voit peruuttaa toiminnon ennen kirjaamista.
    * Voit muuttaa laskun tulostamisen aikataulua seuraavasti: Tulosta kukin lasku päivityksen yhteydessä valitsemalla Nykyinen, tai tulosta vasta kaikkien laskujen päivityksen jälkeen valitsemalla Jälkeen.  
    * Jos haluat muuttaa asiakkaan luottorajan ennen kirjaamista tapahtuvaa tarkistustapaa, muuta luottorajatyyppiä.  
    * Jos haluat tulostaa laskun, valitse Kyllä.  
    * Jos haluat kirjata laskun, valitse Kyllä. Voit tulostaa laskun ilman kirjaamista.  
19. Valitse OK.

## <a name="copy-lines"></a>Kopioi rivit
Valitse vähintään yksi rivi vapaatekstilaskun riveille ja valitse Kopioi valitut rivit. Voit määrittää montako kopiota haluat tehdä ja myös kopioida ilmoituksia ja liitteitä. Voit kopioida jakoja tai sallia niiden uudelleenluonnin, kun kirjaat. Kun kopioit rivejä, voit muokata tietoja tarpeen mukaan. 

## <a name="create-a-free-text-invoice-from-a-template"></a>Luo vapaatekstilasku mallin mukaan
Voit luoda vapaatekstilaskun mallin mukaan. Kun valitset Uusi Lasku-välilehden templaateista, voit valita templaatin nimen ja uuden tekstimuotoisen laskun asiakastilin. Voit valita oletusarvot, kuten maksuehdot ja maksutapa asiakkaan mukaan tai arvoja, jotka on tallennettu malliin. Uusi vapaatekstilasku luodaan ja voit muokata tämän laskun arvoja. 


