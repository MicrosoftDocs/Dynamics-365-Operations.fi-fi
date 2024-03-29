---
title: Kompensaatioprosessin määrittäminen ja tulosten laskeminen
description: Kompensaatioprosesseja käytetään määrittämään kiinteisiin ja muuttuviin kompensaatiosuunnitelmiin rekisteröityjen työntekijöiden uudet kompensaatiosummat ja palkkiot.
author: twheeloc
ms.date: 08/25/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: HRMCompProcess, HRMCompProcessLine, HRMCompEvent, HRMCompEventEmpl, HcmCompensationWorkspace
audience: Application User
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 196c907521bba5440f12149abcb2fc446c2aa523
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/04/2022
ms.locfileid: "8687048"
---
# <a name="define-compensation-process-and-calculate-results"></a>Kompensaatioprosessin määrittäminen ja tulosten laskeminen


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Kompensaatioprosesseja käytetään määrittämään kiinteisiin ja muuttuviin kompensaatiosuunnitelmiin rekisteröityjen työntekijöiden uudet kompensaatiosummat ja palkkiot. Suorittamalla kompensaatioprosessit useita kertoja voidaan tehdä entä–jos-analyysi. Tällä tavoin voidaan tarkistaa, että kaikki muutokset ja asetukset ovat oikein. Tällä menettelyllä luodaan kompensaatioprosessi, suoritetaan se ja tarkastellaan tuloksia. Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.


## <a name="create-a-compensation-process"></a>Luo kompensaatioprosessi
1. Siirry kohtaan **Kompensaationhallinta** > **Käsittele** > **Kompensaatioprosessit**.
2. Valitse **Uusi kompensaatioprosessi**.
3. Kirjoita **Prosessikenttään** arvo.
4. Kirjoita **Kuvaus**-kenttään arvo.
5. Valitse vaihtoehto **Prosessityyppi**-kentässä.
    * Sykli määrittää kompensaation määrittämistä varten arvioitavan ajanjakson. Arvioinnissa otetaan huomioon esimerkiksi työntekijän työtehtävät, sisällytettävät suorituskykyluokitukset ja laskelma siitä, kuinka suuren osan ajasta työntekijä oli prosentuaalisesti työllistettynä syklin aikana. Sykli voi alkaa esimerkiksi edellisen tilivuoden ensimmäisenä päivänä.  
6. Anna **Jakson alku** -kentässä päivämäärä.
    * Syklin viimeinen päivä on tärkeä, sen perusteella määritetään työntekijät, jotka olivat aktiivisesti työllistettyjä ja rekisteröitynä vähintään yhteen kompensaatiosuunnitelmaan.  
7. Anna **Jakson loppu** -kentässä päivämäärä.
    * Tapahtuman aktivointipäivämäärä on päivä, jolloin uudet kompensaatiosuhteet tulevat voimaan. Monissa yrityksissä syklin päättymisen ja uusien kompensaatiosuhteiden voimaantuloajan välillä on muutama kuukausi. Lisäaika käytetään uuden kompensaation käsittelyyn ja tarkistamiseen.  
8. Anna **Tapahtuman aktivointipäivämäärä** -kentässä päivämäärä.
    * Ajankohtaan perustuvaa päivämäärää käytetään muuttuvissa kompensaatiosuunnitelmissa, jotka määrittävät työntekijän palkkiosumman kyseisen ajankohdan kompensaatiosuhteen perusteella.  
    * Kiinteään suhteellisesti jaettuun palkkioon liittyvä työhönottopäivämäärää käytetään kiinteissä kompensaatiosuunnitelmissa, joissa työhönottosääntönä on **Prosentti**. Työntekijät, jotka on palkattu syklin alkamispäivämäärän ja kiinteään suhteellisesti jaettuun palkkioon liittyvän työhönottopäivämäärän välillä, saavat 100 % lasketusta kompensaation jaetun prosenttiosuuden sijaan.  
9. Anna **Kiinteään suhteellisesti jaettuun palkkioon liittyvä työhönottopäivämäärä** -kentässä päivämäärä.
    * Tarkistuksen aikaraja on päivämäärä, johon mennessä kaikki käsittelyn tulokset on tarkistettava, jotta ne voidaan ladata työntekijän kompensaatiotietueeseen ennen tapahtuman aktivointipäivää. Tämä kenttä on vain tiedoksi.  
10. Anna **Tarkasta aikaraja** -kentässä päivämäärä.
11. Valitse **Tallenna**.

## <a name="set-up-the-compensation-plans-and-actions-for-a-compensation-process"></a>Määritä kompensaatiosuunnitelmien ja kompensaatioprosessin toiminnot
1. Valitse **Asetukset**.
    * **Asetukset**-sivulta valitaan suunnitelmat, jotka käsitellään tämän kompensaatioprosessin osana, sekä kussakin suunnitelmassa tehtävät toiminnot.  
2. Anna tai valitse **Suunnitelma**-kentässä arvo.
3. Valitse **Tallenna**.
4. Valitse **Lisää**.
5. Valitse **Toiminto**-kentässä toimintotyypiksi **Oma pääoma**.
6. Valitse **Lisää**.
7. Valitse **Toiminto**-kentässä toimintotyypiksi **Ansio**.
    * Kompensaatiotoiminnot voidaan ketjuttaa yhteen **Käytä aiempaa tulosta** -kentän avulla ilmaisemaan, käytetäänkö valittua toimintoa työntekijöiden peruspalkkana vai ovatko edellisen toiminnot tulokset tämän toiminnon laskennan lähtökohta.  
8. Valitse **Käytä aiempaa tulosta** -kentässä **Kyllä**.
9. Valitse **Lisää**.
10. Valitse **Toiminto**-kentässä toimintotyypiksi **Yleinen**.
    * Kompensaation toimintotyyppi määrittää käytettävissä olevat kentät. Jos kompensaation toimintotyyppi on Yleinen, prosentin tai summan kasvu määritetään.  
11. Valitse **Valitse lisäyssumma** -vaihtoehto.
12. Lisää **Lisäyssumma**-kenttään numero.
13. Valitse **Lisää**.
14. Valitse **Toiminto**-kentässä toimintotyypiksi **Ylennys**.
    * Käyttäjät voivat tehdä manuaalisia muutoksia työntekijän kompensaation Ylennys- ja Muu tason muutos -toimintotyypeissä. Suositukset voidaan käyttöön näissä ja muissa toimintotyypeissä, jolloin työntekijälle voidaan antaa uusi kompensaation suositusarvo.  
15. Valitse **Lisää**.
16. Valitse vaihtoehto **Tyyppi**-kentässä.
    * Samassa kompensaatioprosessissa voi käyttää kiinteitä ja muuttuvia kompensaatiosuunnitelmia.  
17. Anna tai valitse **Suunnitelma**-kentässä arvo.
    * Voit määrittää **Ota käyttöön suoristusperusteinen palkka** -valintaikkunan avulla, säädetäänkö kiinteitä ja muuttumia kompensaatiosummia työntekijän suorituskykyluokituksen perusteella.  
    * Suorituskykykerroin voidaan ohittaa muuttuvissa kompensaatiosuunnitelmissa.  
18. Valitse **Tallenna**.
19. Valitse **Lisää**.
20. Sulje sivu.

## <a name="run-the-compensation-process"></a>Suorita kompensaatioprosessi
1. Valitse **Suorita prosessi**.
    * **Näytä käsittelyn tulokset** -vaihtoehdon avulla voit tarkastella valmiin kompensaatioprosessin käsittelyviestejä, kun käsittely on päättynyt.  
2. Valitse **Näytä käsittelyn tulokset** -kentässä **Kyllä**.
3. Valitse **OK**.

## <a name="view-the-results"></a>Näytä tulokset
1. Valitse **Prosessin tulokset**.
2. Valitse **Työntekijätulokset**.
3. Etsi haluamasi tietue luettelosta ja valitse se.
4. Laajenna **Kiinteä kompensaatio** -osa.
    * Voit avata käsittelyn tulokset laajentamalla pikavälilehdet. Jos kompensaatiotoiminnossa valittiin **Ota suosituksen käyttöön**, **Suositus**-kentät otetaan käyttöön kyseisessä toiminnossa.  
5. Etsi haluamasi tietue luettelosta ja valitse se.
    * Yhden työntekijän tuloksia voi tarkastella napsauttamalla **Näytä tulokset** -painiketta.  
    * Voit korvata lasketun kompensaatiosumman muokkaamalla **Suositus**-kentissä prosenttiosuutta tai suurentamalla summaa.  
6. Lisää **Suositeltu prosentti** -kenttään numero.
7. Etsi haluamasi tietue luettelosta ja valitse se.
8. Lisää **Suositeltu prosentti** -kenttään numero.
    * Laske uudelleen -toiminnolla voidaan ohittaa aiemmin luotuun tietueeseen tehdyt muutokset ja luoda valitulle työntekijälle uusi kompensaatiotulos.  
    * Kun työntekijän kaikki muutokset on tehty, vaihda tilaksi **Hyväksytty**.  
9. Valitse **Muuta tila**.
10. Valitse **Hyväksytty**.
    * Kun tietue on hyväksytty, se voidaan ladata työntekijän viralliseen kompensaatiotietueeseen. Uusi kompensaatio astuu voimaan kompensaatioprosessissa määritettynä tapahtumapäivämääränä.  



[!INCLUDE[footer-include](../includes/footer-banner.md)]
