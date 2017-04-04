---
title: Luo muuttuvia kompensaatiosuunnitelmia
description: "Muuttuva kompensaatio muodostaa työntekijän epäsäännölliset maksut, kuten bonukset ja osakepalkkiot. Tässä aiheessa kuvataan osat, jotka on määritettävä ennen kuin voit käyttää muuttuvan kompensaation ja Työntekijän rekisteröiminen muuttuvan kompensaatiosuunnitelmaan."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
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
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9397e84f03ee5b340fa2aa0a64e582fc0078526e
ms.openlocfilehash: be156afa73de731e54985485b617bcbae883db3a
ms.lasthandoff: 03/31/2017


---

# <a name="create-variable-compensation-plans"></a>Luo muuttuvia kompensaatiosuunnitelmia

Muuttuva kompensaatio muodostaa työntekijän epäsäännölliset maksut, kuten bonukset ja osakepalkkiot. Tässä artikkelissa esitellään komponentit, jotka on määritettävä ennen muuttuvan kompensaation käyttämistä ja työntekijöiden määrittämistä muuttuvaan kompensaatiosuunnitelmaan.

Useat tekijät, kuten työntekijän suorituskyky, työntekijän kompensaatiotaso ja osaston suorituskyky, voivat vaikuttaa työntekijöiden muuttuvien kompensaatiosummien laskennassa.

## <a name="variable-compensation-components"></a>Muuttuvan kompensaation komponentit
### <a name="create-compensation-types"></a>Luo kompensaatiotyypit

**Muuttuvat kompensaatiotyypit **ovat pakollinen osa. Muuttuvien kompensaatiotyyppien avulla voidaan kuvata sellaisia muuttuvia kompensaatioita, joita organisaatiosi antaa. Niiden avulla voit määrittää, lasketaanko korvaus tai käteisenä vai ei-rahallisessa muodossa, esimerkiksi osakepääomana.

### <a name="describe-vesting-rules"></a>Kuvaile hyvityssäännöt

Vaihtoehtoisesti, yritykset voivat määrittää **hyvityssäännöt**. Hyvityssäännöt kuvaavat kuinka muuttuvan palkkion olisi jaettava ajan mittaan. Esimerkiksi hyvityssääntö ehkä mainittava, työntekijä saa 25 prosenttia hänen yhteensä palkinnon vuosittain seuraavan neljän vuoden ajan. Hyvityssäännöt ovat Tiedottava vain.

## <a name="variable-compensation-plans"></a>Muuttuvat kompensaatiosuunnitelmat
**Muuttuvassa kompensaatiosuunnitelmassa** on säännöt, laskentamenetelmät ja oletusarvot muuttuvan kompensaation laskemiseksi rekisteröityneille työntekijöille. Muuttuvan kompensaatiosuunnitelman luonnin muuttuvan kompensaation tyyppi on määritettävä. Muuttuvan kompensaation tyyppi määrittää, onko järjestelmä laskee valuuttasumma tai yksiköiden määrä kuin palkkion. Määritä myös laskentamenetelmä:

-   **Ajankohta** – muuttuvien palkkioiden laskeminen perustuu kiinteän kompensaation, jossa työntekijä oli tiettynä päivänä. Kun uusi korvaus summia käsitellään prosessitapahtuman tuona on määritetty.
-   **Yhdistelmä** – palkkiosumma lasketaan kullekin yksilölliselle kiinteän kompensaation palkkiolle, joka työntekijällä oli jakson alkamispäivämäärän ja prosessitapahtuman päättymispäivän välillä. Sen jälkeen lisätään yhdessä lopullisen palkkion määrittämiseen. Esimerkiksi syklin aikana työntekijä siirretään toiseen paikkaan, jossa oli eri taksaa. Tässä tapauksessa, muuttuvaa palkkiota oikaistaan sille aikavälille, jolla työntekijällä oli kukin palkka.

Muuttuvan palkkion summa voi perustua, joko prosenttiosuuteen työntekijän tavallisista perustuloista tai määritettyyn yksikkömäärään.

-   Valitse **Perusprosentti** -vaihtoehto syöttääksesi oletusarvoisen prosentin ja määritä, onko peruste työntekijän kiinteä taksa vai työntekijän kompensaatiotason ohjauspiste. Korvauksen taso on määritetty työntekijän työhön. Yksi-kompensaatiorakenteen viitepisteiden voidaan määrittää ohjausobjektin pisteenä kiinteään kompensaatiosuunnitelmaan. Järjestelmä käyttää työntekijän työstä kompensaatiotaso ja luoda ristiviitteen tarkistuspiste, joka näkyy työntekijän kiinteään kompensaatiosuunnitelmaan amerikkalaista control point työntekijän kompensaation tason kanssa. Ohjausobjektiin point summa käytetään sijasta työntekijän kiinteä palkkion perustana tekemisen.
-   Valitse **Yksikkömäärä**-vaihtoehto syöttääksesi oletusmäärä yksiköitä, kunkin yksikön arvo ja yksikköarvon valuutta, jos kompeesaatiosuunnitelma on ei-käteispalkkiolle (esimerkiksi 200 osakeyksikköä arvoltaan 40 USD) tai vain yksikkömäärä, jos kompensaatiosuunnitelman on käteispalkkiolle. Työntekijä saavat käteispalkkion, valuutta, jota käytetään hänen kiinteän kompensaatiosuunnitelmaan (esimerkiksi 500 yksikköä 1 USD) määritetty yksikkömäärä. Yksi yhteen-suhteen ohjausobjektia voidaan käyttää osoittamaan, onko suora lähdemallin yksiköiden ja yksikköarvon välillä. Kun luot muuttuvan kompensaatiosuunnitelman cash-suunnitelman yksiköiden avulla, tämä vaihtoehto on lukittu automaattisesti **Kyllä**, ja yksikkö on **1,0000**.

**Työhönottosäännön** asetusten avulla voit määrittää, onko kaikkien työntekijöiden olisi saatava sama kasvu oli Työhönottopäivä riippumatta (**työhönottosäännön** = **ei mitään**), tai onko työntekijät saavat palkkion, joka perustuu työskentelynsä aikana jakson pituuden prosenttiosuus (**työhönottosäännön** = **prosentin**). 

**Suorituskykykertoimen** avulla voit määrittää työntekijän palkkio, työntekijän osaston suorituskyvyn perusteella. Suorituskyvyn mittarit voidaan määrittää kullekin osastolle **osastot** sivun kohtaan **liittyvien lomakkeiden**&gt;**korvaus**&gt;**suorituskyvyn**. Joka kyseisen osaston työntekijät saavat palkkion arvo riippuu **tavoitteen saavuttamisen prosentti** kenttä, joka ilmaisee osaston toimintaa:

-   Jos osaston suorituskyky on 100 prosenttia, osaston työntekijöiden palkkio lasketaan prosenttiarvolla, joka on määritetty** Maksu tasolla 100 %**-kentässä.
-   Jos osaston suorituskyky on yli 100 prosenttia, järjestelmä lisää prosenttiosuuden, joka on määritetty **1 % objektiivin yli** -kentässä siihen prosenttiin, joka on määritetty **Maksu tasolla 100 %** -kentässä, kunnes arvo, joka on asetettu **Suurin sallittu maksu**-kentässä, saavutetaan.
-   Jos osaston suorituskyky on alle 100 prosenttia, järjestelmä vähentää prosenttiosuuden, joka on määritetty **1 % tavoitteen alle** -kenttään prosentista, joka on määritetty **maksu tasolla 100 %** kentässä, kunnes arvo, joka on asetettu **Pienin sallittu maksu**- kenttään, saavutetaan.

Voit määrittää** toleranssitasot** rajaprosenteille, niin että näkyviin tulee varoitussanoma, jos suorituskykykerroin määrittää prosentin raja-arvo prosentin ulkopuolelle. 

Oletusarvon mukaan järjestelmä etsii osasto, joka on määritetty työntekijän asemaan. Kuitenkin joidenkin työntekijöiden palkkion sisältö saattaa määräytyä useiden yksiköiden toiminnan. Tässä tapauksessa osastoilta ja prosentin palkkion, joka kohdistetaan kunkin osaston toimintaan voidaan asettaa työntekijän muuttuvan kompensaation voimaanastuminen. Lisätietoja on kohdassa "muuttuvan kompensaation voimaanastuminen", joka seuraa. 

Suorituskykykertointa käytetään vain, jos **Suoritusperusteinen palkka** valitaan kompensaatioprosessin suorittamisen yhteydessä. 

**Tasoilla ohitukset** -välilehden avulla voit ohittaa oletusprosentti tai yksiköitä, jotka perustuvat työntekijän kompensaatiotaso palkinnon. Jos **Ota ohittaa tasojen** on **Kyllä** työntekijöille, jotka ovat rekisteröityneet muuttuvan kompensaatiosuunnitelma, järjestelmä ottaa työntekijän työn taso ja sitten etsii sitä tasoilla ohittaa taulukon, voit määrittää kyseisen tason yksiköiden määrä tai prosenttiosuus. Jos tasoa ei löydy taso ohittaa taulukon, oletusprosentti tai yksiköiden määrä **yleisen** -välilehteä käytetään. Yksiköiden määrä ja prosenttiosuus myös voidaan ohittaa työntekijän rekisteröinti-muuttuvan kompensaatiosuunnitelma.

## <a name="variable-compensation-enrollment"></a>Muuttuvan kompensaation voimaanastuminen
### <a name="determine-who-is-eligible-for-the-plan"></a>Määritä, ketkä saavat käyttää suunnitelmaa

Kun olet valmis rekisteröimään työntekijöitä muuttuvaan kompensaatiosuunnitelmaan, ensimmäinen askel on määrittää, kuka soveltuu suunnitelmassa määritettyyn kompensaatioon. Ennen kuin kelpoisuus on päätetty, suunnitelmaa ei voida määrittää kenellekään työntekijälle. Voit määrittää oikeutussääntöjä avaamalla **Oikeutussäännöt**-sivun luodaksesi uuden oikeutussäännön suunnitelmallesi ja määrittää ehdot, jotka työntekijän on täytettävä, jotta hän on soveltuva kompensaatiosuunnitelmaan. Voit rajoittaa sopivuutta osaston, ammattijärjestön, kompensaatioalueen (sijainnin), työn, työnkuvan, työn tyypin ja/tai kompensaatiotason mukaan. Vain ne työntekijät voidaan rekisteröidä kompensaatiosuunnitelmaan, jotka täyttävät oikeutussäännön **kaikki** ehdot. 

**Huomaa:** Oikeutussäännöt määrittelevät kelpoisuuden sekä kiinteisiin että muuttuviin kompensaatiosuunnitelmiin. Oikeutussäännöt käyttävät seuraavia toimikenttien arvoja työssä, toimissa ja työntekijätietueissa, määrittääkseen onko työntekijä oikeutettu kompensaatiosuunnitelmaan:

-   Napsauta **Työ**-sivulla:
    -   **Työ**-kenttä
    -   **Toiminto** ja **Työtyyppi** -kentät **Työn luokittelu** -välilehdessä
    -   **Taso**-kenttä **Kompensaatio**-välilehdessä
-   **Toimet**-sivulla: **Osasto-** ja **Kompensaatioalue**-kentät
-   - **Työntekijöiden** sivu: ammattijärjestöt, joka liittyy työntekijän tiedot **henkilökohtaisia tietoja**&gt;**ammattijärjestöt** -*** työntekijän ***-välilehti

### <a name="enable-enrollment-for-the-variable-compensation-plan"></a>Salli muuttuvan kompensaatiosuunnitelman voimaanastuminen

**Muuttuvat kompensaatiosuunnitelmat**-sivulla, määritä **Salli rekisteröinti** -vaihtoehto asentoon **Kyllä** salliaksesi käytettävissä olevien työntekijöiden rekisteröitymisen suunnitelmaan.

### <a name="enroll-the-employee"></a>Merkitse työntekijä

Nyt voit rekisteröidä työntekijäitä muuttuvan kompensaation suunnitelmaan. Rekisteröidäksesi työntekijän, mene **Työntekijät**-sivulle ja valitse työntekijä. Valitse toimintoruudussa **korvaus**&gt;**muuttuvan suunnitelman voimaanastuminen**. 

**Huomautus:** **Rekisteröinnin** on oltava asennossa **Kyllä** muuttuvassa kompensaatiosuunnitelmassa. **Suunnitelma** kentässä on suunnitelmia, jotka työntekijä on oikeutettu, sääntöjä, jotka on määritetty näiden suunnitelmien perusteella. Jos suunnitelma ei ole asetettu oikeutussäännön ei ole työntekijöitä on oikeutettu kyseiseen järjestelyyn. 

Varmista, että **voimaantulo** kenttä on määritetty oikein. Jos muuttuvan kompensaatiosuunnitelman **kooste** laskentatapaa, voimaantulo rekisteröinnin voidaan harkita työntekijän palkinnon laskennan aikana. 

Voit käyttää **ohittaa** välilehti, jos haluat korvata tietyt arvot työntekijän. Esimerkiksi jos **työhönottosäännön** on **prosenttia** suunnitelmaa, ja Työhönottopäivä on eri käytetään laskentaan työntekijän työsuhteen aikana, voit määrittää työsuhteen alkamispäivä **työhönottosäännön päivämäärä** kenttä. Voit myös ohittaa joko **palkkioprosentti** arvo tai **yksiköiden** arvo tietyn työntekijän, suunnitelman asetusten mukaan. Nämä arvot edelleen kehittyviin uuden työhönottosäännön ja suorituskyvyn kerrointen muiden asetusten suunnitelman mukaan. 

**Organisaation ohitukset** voidaan perustaa yksi tai useampi yksiköiden toiminnan työntekijän palkkio. Prosenttiosuus, joka jaetaan eri osastojen tulee olla yhteensä 100 prosenttia. Yksilön suorituskyvyn työntekijän katsotaan myös. Näitä asetuksia käytetään vain, jos **maksaa suorituskykyä** on valittu, kun kompensaatioprosessi suoritetaan.

<a name="see-also"></a>Lisätietoja
--------

[Kompensaatiosuunnitelmat](compensation-plans.md)


