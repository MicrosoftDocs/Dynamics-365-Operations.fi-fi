---
title: Kompensaation käsittely
description: Voit laskea kompensaation käsittelyssä työntekijöille uudet peruskompensaatiosummat pääoman oikaisujen, pätevyyteen liittyvien palkankorotustavoitteiden ja suorituksen perusteella.
author: twheeloc
ms.date: 08/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2017-07-01
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 228c891e8c29cf4309856b90139d0b88805a9812
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8886157"
---
# <a name="process-compensation"></a>Kompensaation käsittely


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Voit laskea kompensaation käsittelyssä työntekijöille uudet peruskompensaatiosummat pääoman oikaisujen, pätevyyteen liittyvien palkankorotustavoitteiden ja suorituksen perusteella. Tässä artikkelissa käsitellään kiinteiden kompensaatiosuunnitelmien perustyöntyönkulku kompensaation käsittelyssä ilman, että työntekijän suoritus huomioidaan.

## <a name="plan-the-new-compensation-amounts-and-budgets"></a>Uusien kompensaatiosummien ja -budjettien suunnittelu
Jos haluat antaa työntekijöille pätevyyteen liittyvän palkankorotuksen, kiinteä lisäysbudjetti on ensin määritettävä kullekin osastolle:  **Kompensaation hallinta** > **Linkit** > **Pätevyyteen liittyvän palkankorotuksen tavoitteet**. (Vaihtoehtoisesti voit avata tämän lomakkeen osaston kautta: **Organisaatio** > **Osastot**.) Voit määrittää tarkemmin, onko tietyn ammattijärjestön tai toimipaikan työntekijöillä erilainen korotusprosentti. **Budjetti-** ja **Valuutta** -kentät on tarkoitettu vain tiedoksi, ja niiden avulla voi ilmoittaa budjetin valuuttasumman.

## <a name="set-up-the-compensation-process"></a>Kompensaatioprosessin määrittäminen
**Kompensaatioprosessit** -sivulla voit määrittää kompensaatioprosessien parametrit. Tähän sisältyy arviointipäiväjakso kompensaatiosummien määrittämistä varten. Siinä on myös päivämäärä, jolloin uudet kompensaatiosummat tulevat voimaan.

Vaihtoehtoisesti voit sisällyttää **kiinteään suhteellisesti jaettuun palkkioon liittyvän työhönottopäivämäärän**, jos jossakin kiinteässä kompensaatiosuunnitelmassa työhönottosääntönä on Prosentti. Näissä suunnitelmissa kaikki, jotka otettiin töihin **jakson alkamispäivän** ja ennen **kiinteään suhteellisesti jaettuun palkkioon liittyvää työhönottopäivämäärää**, saavat 100 % lasketusta pätevyyteen perustuvasta tai yleisestä palkankorotuksesta. Kaikki, jotka otettiin töihin **kiinteään suhteellisesti jaettuun palkkioon liittyvän työhönottopäivämäärän** ja ennen **jakson päättymispäivää**, saavat osan lasketusta palkankorotuksesta sen perusteella, kuinka monta päivää koko jaksosta he olivat töissä. Jos jakso esimerkiksi alkaa 1.1. ja päättyy 31.12. ja jos kiinteään suhteellisesti jaettuun palkkioon liittyvä työhönottopäivämäärä on 1.4., maaliskuussa töihin otettu työntekijä saa koko lasketun palkankorotuksen, kun taas 1.7. töihin otettu työntekijä saa suhteessa noin puolet lasketusta palkankorotuksesta.

Prosessitapahtuman **-ajankohdan** päivämäärään käytetään vain tiettyjen muuttuvien kompensaatiosuunnitelmien käsittelyyn eikä niitä käsitellä nyt. **Tarkasta aikaraja** on määräaika, johon mennessä suositukset on tehtävä, jotta uudet uuden uudet kompensaatiosummat voidaan ladata työntekijän tietueeseen. Tarkastuspäivämäärä on tarkoitettu vain tiedoksi.

Kun prosessitapahtuman parametrit on tallennettu, voit valita tähän prosessiajoon sisältyvät suunnitelmat napsauttamalla **Asetukset**-painiketta. Samalla voit ilmoittaa, mitä kiinteän kompensaation toimintoja tehdään kussakin suunnitelmassa.

Lisää kompensaatiosuunnitelma prosessitapahtumaan napsauttamalla **Lisää**-painiketta **Suunnitelmat**-välilehdessä. **Käytä muuta suorituskykykerrointa**-, **Suorituskykykerroin**- ja **Suorituskykykertoimen kuvaus** -sarakkeita käytetään vain muuttuvan kompensaation suunnitelmissa, eikä niitä käsitellä tässä artikkelissa.

Tallenna tietue ja lisää sitten valitun suunnitelman kiinteän kompensaation toiminnot napsauttamalla **Lisää**-painiketta **Toiminnot**-välilehdessä. Käytä **Ota suositus käyttöön** -vaihtoehtoa, jos haluat antaa toiminnon lasketusta ohjekorotuksesta poikkeavan summan. Jos haluat laskea toiminnon, joka perustuu edellisen toiminnon tulokseen, linkittääksesi useita kompensaatiotoimintoja, merkitse **Käytä edellistä tulosta** -vaihtoehto. Kiinteän kompensaation toiminnot ovat kompensaatiologiikan tyyppejä, joille voit antaa kuvailevia nimiä. **Palkkaluokka**- ja **Kompensaatioluokka**-suunnitelmissa voit lisätä vain seuraavan tyyppisiä kiinteän kompensaation toimintoja:

| Kiinteän kompensaation toiminnon tyyppi | Toiminnallisuus                  |
|-------------------------------|-------------------------------------------------------------------------|
| Oma pääoma                        | Oman pääoman toiminnoissa työntekijän palkkatasoa jakson päättymispäivänä verrataan työntekijän työhön liittyvän tason alhaisimpaan vertailukohtaan. Jos työntekijän palkkio on pienempi kuin pienin vertailukohta, korotus lasketaan niin, että työntekijän palkka nousisi alueen vähimmäistasolle.                                                                                |
| Ansio                         | Pätevyyteen liittyvissä toiminnoissa korotus lasketaan työntekijän jakson päättymispäivän palkkion sekä työntekijän osaston, ammattiliiton tai toimipaikan kiinteässä lisäysbudjetissa olevan korotusprosentin perusteella.                                                                                                                                                                                         |
| Yleiset                       | Yleisissä toiminnoissa korostus lasketaan koko prosentin perusteella tai työntekijälle annetaan kiinteä summa. Tämä määritetään **Yleiset**-välilehden **Kiinteä kompensaatio** -asetusten perusteella.                                                                                                                                                                                                                        |
| Ylennys                     | Korotustoiminnot tarjoavat nimetyn paikan, jossa voit antaa palkankorotuksia. Merkitse **Ota käyttöön suositukset** -vaihtoehto syöttääksesi suosituksia työntekijöille, jotka saavat ylennyksiä.  Työntekijöille, joilla ei ole suositeltua korostusta, ei lisätä **Ylennys**-toimintoa heidän kiinteän kompensaation tietueisiinsa.                                                                       |
| Muu tason muutos            | Edellisessä esimerkissä **Kiinteän kompensaatio** -toiminnon nimenä oli **Palkanalennus** ja sen tyyppi oli **Muu tason muutos**. Tällä tavoin luodun ohjekorotuksen arvo on 0 (nolla-muutos), joten voit muokata työntekijän palkkiota antamalla suositellun summan. (Merkitse **Ota suositus käyttöön** -vaihtoehdon valituksi.) Tätä toimintoa ei lisätä niiden työntekijöiden kiinteän kompensaation tietueisiin, joilla ei ole suositusta. |

Voit lisätä vain niitä **Kiinteä kompensaatio** -toimintoja, joissa on vaiheittainen suunnitelmatyyppi.

| Kiinteän kompensaation toiminnon tyyppi | Toiminnallisuus                |
|--------------------------------|------------------------------|
| Vaihe                           | Ilmoita **Yleiset**-välilehdessä, siirtääkö tämä vaihetoiminto työntekijää eteenpäin 0 vaihetta, 1 vaiheen vai 2 vaihetta.                                                                                  |
|                                | **0 vaihetta** – työntekijä saa palkkion nykyisen vaiheensa mukaan.                                                                                                                      |
|                                | **1 vaihe**– järjestelmä tarkistaa, onko työntekijä jo oman tasonsa viimeisessä viitepisteessä.                                                                                             |
|                                | **2 vaihetta** – työntekijä siirtyy kaksi vaihetta eteenpäin nykyisellä tasolla. Työntekijä voi siirtyä vain yhden vaiheen tai nolla vaihetta, jos he pääsevät tasonsa viimeiseen viitepisteeseen. |

## <a name="run-the-compensation-process"></a>Suorita kompensaatioprosessi
Kun prosessitapahtumaan on määritetty tarvittavat päivämääräkentät, suunnitelmat ja toiminnot, napsauta **Suorita prosessi** **Prosessitapahtuma**-sivulla. Sen jälkeen avautuu **Suorita kompensaatioprosessin tapahtumat** -valintaikkuna. Napsauta **Näytä käsittelyn tulokset** -vaihtoehto, niin näet, miten kompensaation summat on laskettu kullekin työntekijälle. Kun valitset **OK**, kaikkien valitussa kompensaatiosuunnitelmassa jakson päättymispäivänä olevien työntekijöiden kompensaatioprosessi suoritetaan.

## <a name="view-the-process-results"></a>Prosessitulosten näyttäminen
Voit tarkastella prosessin tuloksia avaamalla **Prosessin tulokset** -sivun. Uusi kompensaatiotapahtuma luodaan aina, kun prosessitapahtuma suoritetaan. Tällä tavoin voit tehdä kokeiluja, tehdä muutoksia ja suorittaa kompensaatiotapahtuman useita kertoja, jotta näet, miten erilaiset muutokset vaikuttavat työntekijän kompensaatioon.

**Prosessin tulos** -sivulla on tietoja prosessiajosta, kuten ajon suoritusajankohta, prosessin suorittaja ja mahdolliset prosessin suorittamisen aikana tapahtuneet virheet. Valitse **Lukittu**-valintaruutu, jolloin **Lataa kompensaatio** -painike poistetaan käytöstä eikä kukaan voi ladata kompensaatiotapahtumia työntekijätietueisiin. **Työntekijöiden tulokset** -painikkeella saadaan näkyviin luettelo ajoon sisältyvistä työntekijöistä.

**Työntekijän tulokset** -vaihtoehdossa on tietoja prosessista sekä prosessissa suoritetuista kompensaatiotoiminnoista. **Kiinteä kompensaatio** -osa sisältää kunkin kompensaatiosuunnitelman prosessitapahtumaan sisällytetyn toiminnon tietueen. **Nykyinen ohje**- ja **Suositus**-sarakkeissa on lisätietoja **Kiinteä kompensaatio** -osassa valitusta toiminnosta. Jos **Ota suositukset käyttöön** on valittu toiminnossa, **Suositus**-kenttiä voi muokata. Voit nyt muokata työntekijän summia manuaalisesti. Huomaa, että jos olet valinnut prosessitapahtuman toiminnossa **Käytä aiempaa tulosta**, riippuvien toimintojen summat on päivitettävä manuaalisesti.

Kun työntekijän kompensaatiosummat on arvoitu ja mahdolliset suositeltujen arvojen muutokset on tehty, voit muuttaa **Työntekijätapahtuma**-rivin **tilan**. Tämä ilmaisee, onko tapahtuma hyväksytty vai ohitetaanko se. Vaihtoehtoisesti voit poistaa kaikki työntekijän suositukseen tehdyt muutokset napsauttamalla **Laske uudelleen** -painiketta. Aiemmin luodun työntekijätapahtuman tila on nyt merkitty ohitetuksi ja uusi työntekijätapahtuma luodaan uudelleenlasketuilla arvoilla.

## <a name="loading-approved-compensation-changes"></a>Hyväksyttyjen kompensaation muutoksien lataaminen
Kun vähintään yhden työntekijätapahtuman tila on päivitetty tilaan **Hyväksytty**, kyseinen tapahtuma voidaan ladata työntekijän kiinteän kompensaation tietueisiin. Se voidaan tehdä joko valitsemalla työntekijätapahtumat yksi kerrallaan ja napsauttamalla **Lataa työntekijän kompensaatio** -painiketta **Työntekijän tulokset** -sivulla tai lataamalla kaikki hyväksytyt työntekijätapahtumat kerralla valitsemalla **Prosessin tulokset** -sivulla **Lataa kompensaatio**.

Kun **Lataa kompensaatio** -valintaikkunassa valitaan **OK**, muut kuin nolla kompensaation toimintorivit lisätään **Työntekijän kiinteä kompensaatio** -sivulla.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
