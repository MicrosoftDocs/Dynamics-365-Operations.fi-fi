---
title: "Kompensaation käsittely"
description: "Voit laskea kompensaation käsittelyssä työntekijöille uudet peruskompensaatiosummat pääoman oikaisujen, pätevyyteen liittyvien palkankorotustavoitteiden ja suorituksen perusteella."
author: kherr
manager: AnnBe
ms.date: 07/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2017-07-01
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 6e30357b0bca8745b69bff19a55828b180c3b829
ms.contentlocale: fi-fi
ms.lasthandoff: 06/13/2017


---

# Kompensaation käsittely
<a id="process-compensation" class="xliff"></a>
Voit laskea kompensaation käsittelyssä työntekijöille uudet peruskompensaatiosummat pääoman oikaisujen, pätevyyteen liittyvien palkankorotustavoitteiden ja suorituksen perusteella. Tässä blogikirjoituksessa käsitellään kiinteiden kompensaatiosuunnitelmien perustyöntyönkulku kompensaation käsittelyssä ilman, että suoritus huomioidaan.

## Uusien kompensaatiosummien ja -budjettien suunnittelu
<a id="plan-the-new-compensation-amounts-and-budgets" class="xliff"></a>
Jos haluat antaa työntekijöille pätevyyteen liittyvän palkankorotuksen, kiinteä lisäysbudjetti on ensin määritettävä kullekin osastolle: Kompensaation hallinta > Linkkejä > Pätevyyteen liittyvän palkankorotuksen tavoitteet. (Vaihtoehtoisesti voit avata tämän lomakkeen osaston kautta: Organisaatio > Osastot.) Voit nyt määrittää tarkemmin, onko tietyn ammattijärjestön tai toimipaikan työntekijöillä erilainen korotusprosentti. **Budjetti-** ja **Valuutta** -kentät on tarkoitettu vain tiedoksi, ja niiden avulla voi ilmoittaa budjetin valuuttasumman.

## Kompensaatioprosessin määrittäminen
<a id="set-up-the-compensation-process" class="xliff"></a>
Voit määrittä prosessitapahtumassa kompensaation käsittelyparametrit. Tähän sisältyy arviointipäiväjakso kompensaatiosummien määrittämistä varten.  Siinä on myös päivämäärä, jolloin uudet kompensaatiosummat tulevat voimaan.

Vaihtoehtoisesti voit sisällyttää kiinteään suhteellisesti jaettuun palkkioon liittyvän työhönottopäivämäärän, jos jossakin kiinteässä kompensaatiosuunnitelmassa työhönottosääntönä on Prosentti. Näissä suunnitelmissa kaikki, jotka otettiin töihin jakson alkamispäivän jälkeen ja ennen kiinteään suhteellisesti jaettuun palkkioon liittyvää työhönottopäivämäärää, saavat 100 % lasketusta pätevyyteen perustuvasta tai yleisestä palkankorotuksesta. Kaikki, jotka otettiin töihin kiinteään suhteellisesti jaettuun palkkioon liittyvän työhönottopäivämäärän jälkeen ja ennen jakson päättymispäivää, saavat osan lasketusta palkankorotuksesta sen perusteella, kuinka monta päivää koko jaksosta he olivat töissä. Jos jakso esimerkiksi alkaa 1.1. ja päättyy 31.12. ja jos kiinteään suhteellisesti jaettuun palkkioon liittyvä työhönottopäivämäärä on 1.4., maaliskuussa töihin otettu työntekijä saa koko lasketun palkankorotuksen, kun taas 1.7. töihin otettu työntekijä saa suhteessa noin puolet lasketusta palkankorotuksesta.

Prosessitapahtuman **-ajankohdan** päivämäärään käytetään vain tiettyjen muuttuvien kompensaatiosuunnitelmien käsittelyyn eikä niitä käsitellä tässä blogikirjoituksessa. **Tarkasta aikaraja** on määräaika, johon mennessä suositukset on tehtävä, jotta uudet uuden uudet kompensaatiosummat voidaan ladata työntekijän tietueeseen. Tarkastuspäivämäärä on tarkoitettu vain tiedoksi.

Kun prosessitapahtuman parametrit on tallennettu, voit ilmoittaa tähän prosessiajoon sisältyvät suunnitelmat napsauttamalla **Asetukset**-painiketta. Samalla voit ilmoittaa, mitä kiinteän kompensaation toimintoja tehdään kussakin suunnitelmassa.

Lisää kompensaatiosuunnitelma prosessitapahtumaan napsauttamalla **Lisää**-painiketta ylimmässä välilehdessä. **Käytä muuta suorituskykykerrointa**-, **Suorituskykykerroin**- ja **Suorituskykykertoimen kuvaus** -sarakkeita käytetään vain muuttuvan kompensaation suunnitelmissa, eikä niitä käsitellä tässä blogikirjoituksessa.

Tallenna tietue ja lisää sitten valitun suunnitelman kiinteän kompensaation toiminnot napsauttamalla **Lisää**-painiketta alemmassa välilehdessä. Käytä suosituksen käyttöönottovaihtoehtoa, jos haluat, että toiminnon lasketusta ohjekorotuksesta poikkeava summa voidaan antaa. Jos haluat, että edellisen toiminnon tulosten perusteella laskettava toiminto linkitetään useisiin kompensaatiotoimintoihin, merkitse Käytä aiempaa tulosta valituksi. Kiinteän kompensaation toiminnot kompensaatiologiikan tyyppejä, joille voi antaa kuvailevan nimen. Palkkaluokka- ja Kompensaatioluokka-suunnitelmissa voit lisätä vain seuraavan tyyppisiä kiinteän kompensaation toimintoja:

| Kiinteän kompensaation toiminnon tyyppi | Toiminnallisuus                                                                                                                                                                                                                                                                                                                                                                                                    |
|-------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Oma pääoma                        | Oman pääoman toiminnoissa työntekijän palkkatasoa jakson päättymispäivänä verrataan työntekijän työhön liittyvän tason alhaisimpaan vertailukohtaan. Jos työntekijän palkkio on pienempi kuin pienin vertailukohta, korotus lasketaan niin, että työntekijän palkka nousisi alueen vähimmäistasolle.                                                                                |
| Ansio                         | Pätevyyteen liittyvissä toiminnoissa korotus lasketaan työntekijän jakson päättymispäivän palkkion sekä työntekijän osaston, ammattiliiton tai toimipaikan kiinteässä lisäysbudjetissa olevan korotusprosentin perusteella.                                                                                                                                                                                         |
| Yleiset                       | Yleisissä toiminnoissa korostus lasketaan koko prosentin perusteella tai työntekijälle annetaan kiinteä summa. Tämä määritetään kiinteän kompensaation Yleiset-välilehden asetusten perusteella.                                                                                                                                                                                                                        |
| Ylennys                     | Ylennystoiminnot on sijainti, jossa voit myöntää korotuksen, joten muista merkitä **Ota suosituksen käyttöön** -vaihtoehto valituksi, jotta voit tehdä suosituksia ylennettävistä työntekijöistä.  Työntekijöille, jotka eivät suositeltua korostusta, ei lisätä ylennystoimintoa heidän kiinteän kompensaation tietueisiinsa.                                                                       |
| Muu tason muutos            | Edellisessä esimerkissä kiinteän kompensaation toiminnon nimenä oli Palkanalennus ja sen tyyppi oli Muu tason muutos. Tällä tavoin luodun ohjekorotuksen arvo on 0 (nolla-muutos), joten voit muokata työntekijän palkkiota antamalla suositellun summan. (Varmista, että olet merkinnyt **Ota suositus käyttöön** -vaihtoehdon valituksi.) Tätä toimintoa ei lisätä niiden työntekijöiden kiinteän kompensaation tietueisiin, joilla ei ole suositusta. |

Voit lisätä vain niitä kiinteään kompensaatio toimintoja, joissa on vaiheittainen suunnitelmatyyppi.

| Kiinteän kompensaation toiminnon tyyppi | Toiminnallisuus                                                                                                                                                                                           |
|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Vaihe                           | Ilmoita Yleiset-välilehdessä, siirtääkö tämä vaihetoiminto työntekijää eteenpäin 0 vaihetta, 1 vaiheen vai 2 vaihetta.                                                                                  |
|                                | **0 vaihetta** – työntekijä saa palkkion nykyisen vaiheensa mukaan.                                                                                                                      |
|                                | **1 vaihe**– järjestelmä tarkistaa, onko työntekijä jo oman tasonsa viimeisessä viitepisteessä.                                                                                             |
|                                | **2 vaihetta** – järjestelmä siirtää työntekijän kaksi vaihetta eteenpäin nykyisellä tasolla. Järjestelmä voi siirtää työntekijän vain yhden vaiheen tai nolla vaihetta, jos he pääsevät tasonsa viimeiseen viitepisteeseen. |

## Suorita kompensaatioprosessi
<a id="run-the-compensation-process" class="xliff"></a>
Kun prosessitapahtumaan on määritetty tarvittavat päivämääräkentät, suunnitelmat ja toiminnot, voit valita Prosessitapahtuma-sivulla **Suorita prosessi**. Se avaa kompensaation prosessitapahtumien valintaikkunan. Jos valitset tässä valintaikkunassa **Näytä käsittelyn tulokset** -vaihtoehdon, näet, miten kompensaation summat on laskettu kullekin työntekijälle. Kun valitset **OK**, kaikkien valitussa kompensaatiosuunnitelmassa jakson päättymispäivänä olevien työntekijöiden kompensaatioprosessi suoritetaan.

## Prosessitulosten näyttäminen
<a id="view-the-process-results" class="xliff"></a>
Voit tarkastella prosessin tuloksia avaamalla **Prosessin tulokset** -sivun. Uusi kompensaatiotapahtuma luodaan aina, kun prosessitapahtuma suoritetaan. Tällä tavoin voit tehdä kokeiluja, tehdä muutoksia ja suorittaa kompensaatiotapahtuman useita kertoja, jotta näet, miten erilaiset muutokset vaikuttavat työntekijän kompensaatioon.

Prosessin tulos -sivulla on tietoja prosessiajosta, kuten ajon suoritusajankohta, prosessin suorittaja ja mahdolliset prosessin suorittamisen aikana tapahtuneet virheet. Voit myös valita **Lukittu**-valintaruudun, jolloin **Lataa kompensaatio** -painike poistetaan käytöstä eikä kukaan voi ladata kompensaatiotapahtumia työntekijätietueisiin. **Työntekijöiden tulokset** -painikkeella saadaan näkyviin luettelo ajoon sisältyvistä työntekijöistä.

Työntekijän tuloksissa on tietoja itse prosessista sekä prosessissa tehdyistä kompensaation toiminnoista. Kiinteätä kompensaatiota käsittelevässä osassa on kunkin kompensaatiosuunnitelman prosessitapahtumaan sisältyvän toiminnon tietue. Nykyisen ohjeen ja suosituksen sarakkeissa on lisätietoja kiinteän kompensaation osassa valitusta toiminnosta. Jos suositusten käyttöönotto on valittu toiminnossa, suosituskenttiä voi muokata. Voit nyt muokata työntekijän summia manuaalisesti. Huomautus: jos olet valinnut prosessitapahtuman toiminnossa Käytä aiempaa tulosta, riippuvien toimintojen summat on päivitettävä manuaalisesti.

Kun työntekijän kompensaatiosummat on arvoitu ja mahdolliset suositeltujen arvojen muutokset on tehty, voit muuttaa **Työntekijätapahtuma**-rivin **tilan**. Tämä ilmaisee, onko tapahtuma hyväksytty vai ohitetaanko se. Vaihtoehtoisesti voit poistaa kaikki työntekijän suositukseen tehdyt muutokset napsauttamalla **Laske uudelleen** -painiketta. Aiemmin luodun työntekijätapahtuman tila on nyt merkitty ohitetuksi ja uusi työntekijätapahtuma luodaan uudelleenlasketuilla arvoilla.

## Hyväksyttyjen kompensaation muutoksien lataaminen
<a id="loading-approved-compensation-changes" class="xliff"></a>
Kun vähintään yhden työntekijätapahtuman tila on päivitetty hyväksytyksi, kyseinen tapahtuma voidaan ladata työntekijän kiinteän kompensaation tietueisiin. Se voidaan tehdä joko valitsemalla työntekijätapahtumat yksi kerrallaan ja napsauttamalla työntekijän kompensaation latauspainiketta työntekijän tulossivulla tai lataamalla kaikki hyväksytyt työntekijätapahtumat kerralla valitsemalla prosessin tulossivulla **Lataa kompensaatio**.

Kun **Lataa kompensaatio** -valintaikkunassa valitaan **OK**, muut kuin nolla kompensaation toimintorivit lisätään **Työntekijän kiinteä kompensaatio** -sivulla.

