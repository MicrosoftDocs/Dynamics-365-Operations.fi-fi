---
title: Luo muuttuvia kompensaatiosuunnitelmia
description: "Muuttuva kompensaatio muodostaa työntekijän epäsäännölliset maksut, kuten bonukset ja osakepalkkiot. Tässä aiheessa esitellään komponentit, jotka on määritettävä ennen muuttuvan kompensaation käyttämistä ja työntekijöiden määrittämistä muuttuvaan kompensaatiosuunnitelmaan."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: HCMCompEligibility, HcmJobFunction, HcmWorker, HRMCompPerfPlan
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 16011
ms.assetid: fc3a394e-9ac6-4f8c-9162-dc16ec22720f
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 26ed9de01bffbcd468ac0cf1b9eb3f101707eb04
ms.contentlocale: fi-fi
ms.lasthandoff: 05/25/2017


---

# <a name="create-variable-compensation-plans"></a>Luo muuttuvia kompensaatiosuunnitelmia

[!include[banner](includes/banner.md)]


Muuttuva kompensaatio muodostaa työntekijän epäsäännölliset maksut, kuten bonukset ja osakepalkkiot. Tässä artikkelissa esitellään komponentit, jotka on määritettävä ennen muuttuvan kompensaation käyttämistä ja työntekijöiden määrittämistä muuttuvaan kompensaatiosuunnitelmaan.

Useat tekijät, kuten työntekijän suorituskyky, työntekijän kompensaatiotaso ja osaston suorituskyky, voivat vaikuttaa työntekijöiden muuttuvien kompensaatiosummien laskennassa.

## <a name="variable-compensation-components"></a>Muuttuvan kompensaation komponentit
### <a name="create-compensation-types"></a>Luo kompensaatiotyypit

**Muuttuvat kompensaatiotyypit**ovat pakollinen osa. Muuttuvien kompensaatiotyyppien avulla voidaan kuvata sellaisia muuttuvia kompensaatioita, joita organisaatiosi antaa. Niiden avulla voit määrittää, lasketaanko korvaus tai käteisenä vai ei-rahallisessa muodossa, esimerkiksi osakepääomana.

### <a name="describe-vesting-rules"></a>Kuvaile hyvityssäännöt

Vaihtoehtoisesti, yritykset voivat määrittää **hyvityssäännöt**. Hyvityssäännöt kuvaavat, kuinka muuttuva palkkio olisi jaettava ajan mittaan. Esimerkiksi hyvityssääntö saattaa määrittää, että työntekijä saa 25 prosenttia kokonaispalkkiostaan vuosittain seuraavan neljän vuoden ajan. Hyvityssäännöt ovat vain tiedoksi.

## <a name="variable-compensation-plans"></a>Muuttuvat kompensaatiosuunnitelmat
**Muuttuvassa kompensaatiosuunnitelmassa** on säännöt, laskentamenetelmät ja oletusarvot muuttuvan kompensaation laskemiseksi rekisteröityneille työntekijöille. Kun luot muuttuvan kompensaatiosuunnitelman, muuttuvan kompensaation tyyppi on määritettävä. Muuttuvan kompensaation tyyppi määrittää, onko laskeeko järjestelmä valuuttasumman tai yksiköiden määrän palkkioksi. Määritä myös laskentamenetelmä:

-   **Ajankohta** – muuttuvien palkkioiden laskeminen perustuu kiinteään kompensaatioon, joka työntekijällä oli tiettynä päivänä. Päivämäärä määritetään prosessitapahtumassa, kun uusia kompensaatiosummia käsitellään.
-   **Yhdistelmä** – palkkiosumma lasketaan kullekin yksilölliselle kiinteän kompensaation palkkiolle, joka työntekijällä oli jakson alkamispäivämäärän ja prosessitapahtuman päättymispäivän välillä. Sen jälkeen hinnat lisätään yhteen lopullisen palkkion määrittämiseksi. Esimerkiksi syklin aikana työntekijä siirretään toiseen toimeen, jossa on eri taksa. Tässä tapauksessa, muuttuvaa palkkiota oikaistaan sille aikavälille, jolla työntekijällä oli kukin palkka.

Muuttuvan palkkion summa voi perustua, joko prosenttiosuuteen työntekijän tavallisista perustuloista tai määritettyyn yksikkömäärään.

-   Valitse **Perusprosentti** -vaihtoehto syöttääksesi oletusarvoisen prosentin ja määritä, onko peruste työntekijän kiinteä taksa vai työntekijän kompensaatiotason ohjauspiste. Korvauksen taso on määritetty työntekijän työhön. Yksi kompensaatiorakenteen viitepisteistä voidaan määrittää hallintapisteeksi kiinteään kompensaatiosuunnitelmaan. Järjestelmä käyttää työntekijän työn kompensaatiotasoa ja viittaa siihen sen tarkistuspisteen kanssa, joka näkyy työntekijän kiinteässä kompensaatiosuunnitelmassa, löytääkseen työntekijän kompensaation tason tarkistuspistesumman. Tarkistuspistesummaa käytetään työntekijän kiinteän palkan sijasta palkkion perustana.
-   Valitse **Yksikkömäärä**-vaihtoehto syöttääksesi oletusmäärä yksiköitä, kunkin yksikön arvo ja yksikköarvon valuutta, jos kompeesaatiosuunnitelma on ei-käteispalkkiolle (esimerkiksi 200 osakeyksikköä arvoltaan 40 USD) tai vain yksikkömäärä, jos kompensaatiosuunnitelman on käteispalkkiolle. Käteispalkkiona työntekijä saa määritetyn määrän yksikköjä valuutassa, jota käytetään hänen kiinteässä kompensaatiosuunnitelmassaan (esimerkiksi 500 yksikköä, valuutta 1 USD). Yksi-yhteen-suhteen tarkistusta voidaan käyttää osoittamaan, onko olemassa suora vastaavuus yksiköiden ja yksikköarvon välillä. Kun luot muuttuvan kompensaatiosuunnitelman käteiseen perustuvalle suunnitelmalle yksiköiden avulla, tämä vaihtoehto on lukittu automaattisesti arvoon **Kyllä** ja yksikköarvo on **1,0000**.

**Työhönottosääntö**-asetuksien avulla voit määrittää kaikkien työntekijöiden vastaanottavan saman lisäyksen riippumatta päivämäärästä, jolloin heidät palkattiin (**Työhönottosääntö**  =  **Ei yhtään**), tai saavatko työntekijät prosenttiosuuden palkasta, joka perustuu siihen kauanko he työskentelivät kauden aikana (**Työhönottosääntö**  =  **Prosentti**). 

**Suorituskykykertoimen** avulla voit määrittää työntekijän palkkion työntekijän osaston suorituskyvyn perusteella. Suorituskyvyn mittarit voidaan määrittää kullekin osastolle **Osastot**-sivulla kohdassa **Liittyvät lomakkeet** &gt; **Kompensaatio** &gt; **Suorituskyky**. Kyseisen osaston työntekijöiden saama palkkio riippuu **Tavoitteesta saavutettu prosentti** -kentän arvosta, joka kertoo osaston suorituskyvystä:

-   Jos osaston suorituskyky on 100 prosenttia, osaston työntekijöiden palkkio lasketaan prosenttiarvolla, joka on määritetty**Maksu tasolla 100 %**-kentässä.
-   Jos osaston suorituskyky on yli 100 prosenttia, järjestelmä lisää prosenttiosuuden, joka on määritetty **1 % objektiivin yli** -kentässä siihen prosenttiin, joka on määritetty **Maksu tasolla 100 %** -kentässä, kunnes arvo, joka on asetettu **Suurin sallittu maksu**-kentässä, saavutetaan.
-   Jos osaston suorituskyky on alle 100 prosenttia, järjestelmä vähentää prosenttiosuuden, joka on määritetty **1 % tavoitteen alle** -kenttään prosentista, joka on määritetty **maksu tasolla 100 %** kentässä, kunnes arvo, joka on asetettu **Pienin sallittu maksu**- kenttään, saavutetaan.

Voit määrittää**toleranssitasot** rajaprosenteille, niin että näkyviin tulee varoitussanoma, jos suorituskykykerroin määrittää prosentin raja-arvo prosentin ulkopuolelle. 

Oletusarvon mukaan järjestelmä etsii osaston, joka on määritetty työntekijän toimelle. Kuitenkin joidenkin työntekijöiden palkkio saattaa määräytyä useiden yksiköiden suorituskyvyn mukaan. Tällöin eri osastot ja palkkion prosentti, joka kohdistetaan kunkin osaston suorituskykyyn, voidaan määrittää työntekijän muuttuvan kompensaation voimaan astuessa. Lisätietoja on kohdassa "Muuttuvan kompensaation voimaanastuminen", joka on seuraavana. 

Suorituskykykertointa käytetään vain, jos **Suoritusperusteinen palkka** valitaan kompensaatioprosessin suorittamisen yhteydessä. 

**Tasojen ohitukset** -välilehden avulla voit ohittaa palkkion oletusprosentin tai kappalemäärän perustuen työntekijän kompensaatiotasoon. Jos **Salli tasojen ohitukset** on **Kyllä** kaikille työntekijöille, jotka ovat rekisteröityneet muuttuvaan kompensaatiosuunnitelmaan, järjestelmä ottaa tason työntekijän projektista ja sitten etsii sen "Tasojen ohitukset" -taulussa, määrittääkseen oletusprosentin tai yksikköjen määrän sille tasolle. Jos tasoa ei löydy Tasojen ohitukset -taulukossa, oletusprosenttia tai yksikköjen määrää **Yleiset**-välilehdessä käytetään. Prosenttiosuus ja yksikköjen määrä voidaan myös ohittaa työntekijän rekisteröinnissä muuttuvan kompensaation suunnitelmassa.

## <a name="variable-compensation-enrollment"></a>Muuttuvan kompensaation voimaanastuminen
### <a name="determine-who-is-eligible-for-the-plan"></a>Määritä, ketkä saavat käyttää suunnitelmaa

Kun olet valmis rekisteröimään työntekijöitä muuttuvaan kompensaatiosuunnitelmaan, ensimmäinen askel on määrittää, kuka soveltuu suunnitelmassa määritettyyn kompensaatioon. Ennen kuin kelpoisuus on päätetty, suunnitelmaa ei voida määrittää kenellekään työntekijälle. Voit määrittää oikeutussääntöjä avaamalla **Oikeutussäännöt**-sivun luodaksesi uuden oikeutussäännön suunnitelmallesi ja määrittää ehdot, jotka työntekijän on täytettävä, jotta hän on soveltuva kompensaatiosuunnitelmaan. Voit rajoittaa sopivuutta osaston, ammattijärjestön, kompensaatioalueen (sijainnin), työn, työnkuvan, työn tyypin ja/tai kompensaatiotason mukaan. Vain ne työntekijät voidaan rekisteröidä kompensaatiosuunnitelmaan, jotka täyttävät oikeutussäännön **kaikki** ehdot. 

**Huomaa:** Oikeutussäännöt määrittelevät kelpoisuuden sekä kiinteisiin että muuttuviin kompensaatiosuunnitelmiin. Oikeutussäännöt käyttävät seuraavia toimikenttien arvoja työssä, toimissa ja työntekijätietueissa, määrittääkseen onko työntekijä oikeutettu kompensaatiosuunnitelmaan:

-   Napsauta **Työ**-sivulla:
    -   **Työ**-kenttä
    -   **Toiminto** ja **Työtyyppi** -kentät **Työn luokittelu** -välilehdessä
    -   **Taso**-kenttä **Kompensaatio**-välilehdessä
-   **Toimet**-sivulla: **Osasto-** ja **Kompensaatioalue**-kentät
-   **Työntekijät**-sivulla: tiedot ammattiliitoista, jotka liittyvät työntekijään kohdassa **Henkilökohtaiset tiedot** &gt; **Ammattijärjestöt** ****Työntekijä****-välilehdessä

### <a name="enable-enrollment-for-the-variable-compensation-plan"></a>Salli muuttuvan kompensaatiosuunnitelman voimaanastuminen

**Muuttuvat kompensaatiosuunnitelmat**-sivulla, määritä **Salli rekisteröinti** -vaihtoehto asentoon **Kyllä** salliaksesi käytettävissä olevien työntekijöiden rekisteröitymisen suunnitelmaan.

### <a name="enroll-the-employee"></a>Merkitse työntekijä

Nyt voit rekisteröidä työntekijäitä muuttuvan kompensaation suunnitelmaan. Rekisteröidäksesi työntekijän, mene **Työntekijät**-sivulle ja valitse työntekijä. Sitten, valitse toimintoruudussa **Kompensaatio** &gt; **Muuttuva kompensaatiosuunnitelma**. 

**Huomautus:** **Rekisteröinnin** on oltava asennossa **Kyllä** muuttuvassa kompensaatiosuunnitelmassa. **Suunnitelma**-kentässä näkyvät vain ne suunnitelmat, joihin työntekijä on oikeutettu, niiden oikeutussääntöjen mukaisesti, jotka on määritetty jokaiselle suunnitelmalle. Jos oikeutussääntöä ei ole määritetty suunnitelmalle, kukaan työntekijä ei ole oikeutettu suunnitelmaan. 

Varmista, että **Voimaantulopäivä**-kenttä on määritetty oikein. Jos muuttuva kompensaatiosuunnitelma käyttää **Yhdistelmä**-laskentatapaa, rekisteröinnin voimaantulopäivämäärä voidaan ottaa huomioon työntekijän palkkion laskennan aikana. 

Voit käyttää **Ohitukset**-välilehteä, jos haluat ohittaa työntekijän tietyt arvot. Esimerkiksi jos **Työhönottosääntö** on suunnitelmassa **Prosentti** ja pitäisi käyttää eri työhönottopäivää työntekijän työsuhteen prosentin laskentaan, voit määrittää työsuhteen alkamispäivän **Työhönottosäännön päivämäärä** -kentässä. Voit myös ohittaa joko **Palkkioprosentti** -arvon tai **Yksiköiden määrä** -arvon tietyn työntekijän osalta suunnitelman asetusten mukaan. Näitä arvoja kuitenkin lasketaan työhönottosäännön, suorituskykykertoimien ja muiden suunnitelman asetuksien mukaan. 

**Organisaation ohituksia** käytetään perustana työntekijän palkinnolle yhden tai useamman osaston toiminnasta. Prosentin, joka kohdistetaan osastojen kesken, tulee olla yhteensä 100 prosenttia. Työntekijän yksilösuorituskyky otetaan myös huomioon. Näitä asetuksia käytetään vain, jos **Suoritusperusteinen palkka** valitaan kompensaatioprosessin suorittamisen yhteydessä.

<a name="see-also"></a>Lisätietoja
--------

[Kompensaatiosuunnitelmat](compensation-plans.md)




