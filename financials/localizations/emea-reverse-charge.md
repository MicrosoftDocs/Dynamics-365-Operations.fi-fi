---
title: "Käänteinen arvonlisävero | Microsoft Docs"
description: "Tässä ohjeaiheessa kerrotaan, miten käänteinen arvonlisävero määritetään Euroopan maissa."
author: epodkolz
manager: AnnBe
ms.date: 05/12/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations, UnifiedOperations
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: epodkolz
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 6cb473962f40ed9ef2f5f807f089098764f47009
ms.openlocfilehash: b3c94fa73410d9bdcaaec11dee04a7a239e4d45a
ms.contentlocale: fi-fi
ms.lasthandoff: 06/14/2017

---

# Käänteinen verovelvollisuus
<a id="reverse-charge-vat" class="xliff"></a>
Tässä ohjeaiheessa kerrotaan yleisesti eurooppalaisten maiden käänteisen arvonlisäveron määrittämisestä.

Käänteinen vero on veromalli, jossa ALV:n kirjanpito- ja raportointivastuu siirtyy myyjältä tavaran ja/tai palvelun ostajalle. Tämän vuoksi tavaroiden ja/tai palvelujen vastaanottaja ilmoitta ALV-ilmoituksessa sekä maksettavan veron (myyjän roolissa) että vähennettävän veron (ostajan roolissa)

EU-direktiivin mukaisesti jäsenmaat voivat määrittää, miten yleiset vaatimukset voidaan sopeuttaa paikallisiin vaatimuksiin. Niinpä joissakin maissa käänteinen veromalli koskee vain joitakin tavaroita ja/tai palveluja. Lisäksi myyntisummiin liittyy lisäehtoja tai rajoja. Toisissa maissa arvolisäveron maksuvelvollisuus määräytyy toimittajan ja ostajan tilan mukaan. Jos ostaja on ALV-verovelvollinen, se on ilmaistava selkeästi toimittajan kirjoittamassa laskussa. Laskussa on esimerkiksi oltava samat "käänteinen vero" ja siinä on ilmaistava, mitä kohtia käänteiseen veromalli koskee. 

Seuraavat asetukset on tehtävä käänteisen veron käyttöä varten.

## Määritä arvonlisäverokoodit
<a id="set-up-sales-tax-codes" class="xliff"></a>
Osto- ja myyntitoimintoihin kannattaa käyttää erillisiä arvonlisäverokoodeja.

<table>
<body>
<tr>
<td><strong>Myynnin arvonlisäverokoodi</strong></td>
<td>Luo myyntikoodi käänteisen veron myyntitoiminnoille (<strong>Verot</strong> > <strong>Välilliset verot</strong> > <strong>Arvonlisävero</strong> > <strong>Arvonlisäverokoodit</strong>).
</td>
</tr>
<tr>
<td><strong>Ostojen arvonlisäverokoodi</strong></td>
<td><p>Luo ostojen käänteinen verovelvollisuus positiivisille ja negatiivisille arvonlisäverokoodeille (<strong>Verot</strong> > <strong>Välilliset verot</strong> > <strong>Arvonlisävero</strong> > <strong>Arvonlisäverokoodit</strong>).</p>
<ol>
<li>Luo arvonlisäverokoodi, jolla on positiivinen arvo.</li>
<li>Luo arvonlisäverokoodi, jolla on negatiivinen arvo. Valitse <strong>Salli negatiivinen alv-prosentti</strong> -asetukseksi <strong>Kyllä</strong>.
Tämä negatiivinen arvonlisäverokoodi on määritettävä ensin nimikkeen arvonlisäveroryhmään ja nimikkeen arvonlisäveroryhmä on sitten määritettävä nimikkeisiin, joissa on käänteinen verovelvollisuus.</li>
</ol>
<p>Lisätietoja on seuraavassa kohdassa Arvonlisäveroryhmien ja nimikkeiden arvonlisäveroryhmien määrittäminen.</p>
</td>
</tr>
</tbody>
</table>

## Arvonlisäveroryhmien ja nimikkeiden arvonlisäveroryhmien määrittäminen
<a id="set-up-sales-tax-groups-and-item-sales-tax-groups" class="xliff"></a>
Osto- ja myyntitoimintoihin kannattaa käyttää erillisiä arvonlisäveroryhmiä.

<table>
<tr>
<td><strong>Myynnin arvonlisäveroryhmä</strong></td>
<td>Luo arvonlisäveroryhmä käänteisen veron myyntitoiminnoille (<strong>Verot</strong> > <strong>Välilliset verot</strong> > <strong>Arvonlisävero</strong> > <strong>Arvonlisäveroryhmät</strong>). Sisällytä <strong>Asetukset</strong>-välilehdessä tämän ryhmän käänteisen veron arvonlisäverokoodi. Valitse arvolisäkoodin <strong>Vapautus</strong>- ja <strong>Käänteinen vero</strong> -valintaruudut.</td>
</tr>
<tr>
<td><strong>Ostojen arvonlisäveroryhmät</strong></td>
<td>Luo arvonlisäveroryhmä käänteisen veron ostotoiminnoille (<strong>Verot</strong> > <strong>Välilliset verot</strong> > <strong>Arvonlisävero</strong> > <strong>Arvonlisäveroryhmät</strong>). Sisällytä <strong>Asetukset</strong>-välilehdessä tähän ryhmään sekä negatiiviset ja positiiviset arvonlisäverokoodit. Valitse <strong>Käänteinen vero</strong> -valintaruutu arvoltaan negatiiviselle arvonlisäverokoodille.</td>
</tr>
<tr>
<td><strong>Nimikkeen arvonlisäveroryhmät</strong></td>
<td>Luo tai päivitä arvoltaan negatiivinen arvolisäkoodillinen nimekkeen arvolisävero (<strong>Verot</strong> > <strong>Välilliset verot</strong> > <strong>Arvonlisävero</strong> > <strong>Nimikkeen arvolisäveroryhmät</strong>). Oletusarvoinen nimikkeen arvonlisäveroryhmä on määritettävä tuotteille ja luokille, joita käänteinen arvonlisävero koskee.</td>
</tr>
</table>

## Käänteisten veroryhmien määrittäminen
<a id="set-up-reverse-charge-groups" class="xliff"></a>
Voit määrittää **Käänteisen veloituksen nimikeryhmät** -sivulla (**Verot** > **Asetukset** > **Arvonlisävero** > **Käänteisen veloituksen nimikeryhmät**) tuote- tai palveluryhmät tai yksittäiset tuotteet tai palvelut, joissa voidaan käyttää käänteistä arvonlisäveroa. Määritä kullekin käänteisen veron nimikeryhmälle myynnin ja/tai ostojen nimike-, nimikeryhmä- tai luokkaluettelo.

## Käänteisen verotuksen sääntöjen määrittäminen
<a id="set-up-reverse-charge-rules" class="xliff"></a>
Voit määrittää **Käänteinen veloituksen säännöt** -sivulla (**Verot** > **Asetukset** > **Arvonlisävero** > **Käänteisen veloituksen säännöt**) soveltuvuussäännöt ostoja ja myyntiä varten. Voit määrittää käänteisen verotuksen soveltuvuussääntöjoukon. Määritä kullekin säännölle seuraavat kentät:

- **Tiedostotyyppi** – valitse **Ostotilaus**, **Toimittajan laskun kirjauskansio**, **Myyntitilaus**, **Vapaatekstilasku**, **Myyntilaskukirjauskansio** ja/tai **Toimittajan lasku**.
- **Kumppanin maan/alueen tyyppi** – Valitse **kotimaa**, **EU** tai **Ulkomainen**. Jos sääntöä voi vaihtoehtoisesti käyttää kaikissa kauppakumppaneissa osoitteen maasta tai alueesta riippumatta, valitse **Kaikki**.
- **Kotimaantoimituksen osoite** – Kun tämä valintaruutu valitaan, sääntöä käytetään samassa maassa tai samalla alueella tehtäviin toimituksiin. Tätä valintaruutua ei voi valita, jos asiakirjan tyyppi on **Toimittajan laskun kirjauskansio** ja **Myyntilaskukirjauskansio**.
- **Käänteisen veloituksen nimikeryhmä** – valitse ryhmä, jossa sääntöä voidaan käyttää.
- **Raja-arvo** – Käänteistä veromallia käytetään laskussa vain, jos käänteisen verotuksen nimekeryhmään sisältyvien nimikkeiden ja/tai palvelujen arvo ylittää tässä määritetyn raja-arvon.

Voit määrittää säännön voimassaolojakson käyttämällä **Voimaantulopäivä**- ja **Vanhentumispäivä** -kenttiä.

Voit lisäksi määrittää, näkyvätkö ilmoitukset ja päivitetäänkö asiakirjan rivin oletusarvoisella käänteisellä arvonlisäveroryhmällä, jos kyseisen asiakirjarivin ehto täyttyy. Valittavissa ovat seuraavat vaihtoehdot:

- **Ei mitään** – asiakirjariviä ei päivitetä.
- **Kehote** – avautuva ilmoitus pyytää vahvistamaan, että käänteistä vero saa käyttää.
- **Määritä** – asiakirjarivi päivitetään ilman lisäilmoituksia.

## Oletusparametrien määrittäminen
<a id="set-up-default-parameters" class="xliff"></a>
Voit ottaa toiminnon käyttöön valitsemalla **Kirjanpitoparametrit**-sivun **Käänteinen veloitus**-välilehdessä **Ota käänteinen veloitus käyttöön** -asetukseksi **Kyllä**. Valitse **Ostotilauksen arvonlisäveroryhmä**- ja **Myyntitilauksen arvonlisäveroryhmä** -kentissä oletusarvoiset arvonlisäveroryhmät. Kun käänteisen veron soveltuvuusehto täyttyy, myynti- tai ostotilausrivi päivitetään näillä arvonlisäveroryhmillä.

## Myyntilaskun käänteinen vero
<a id="reverse-charge-on-a-sales-invoice" class="xliff"></a>
Käänteisen veromallin alaisessa myynnissä myyjä ei voita arvolisäveroa. Laskussa ilmoitetaan sen sijaan sekä käänteisen verovelvollisuuden alaiset nimikkeet että käänteisen verovelvollisuuden kokonaissumma.

Kun kirjattavassa myyntilaskussa on käänteistä veroa, arvolisäverotapahtumissa on verosuuntana **Maksettava arvonlisävero** ja arvonlisävero on nolla ja **Käänteinen veloitus** -valintaruutu on valittu.

## Ostolaskun käänteinen vero
<a id="reverse-charge-on-a-purchase-invoice" class="xliff"></a>
Käänteiseen veromalliin kuuluvissa ostoissa käänteisen veron sisältävän laskun vastaanottava ostaja toimii ostajana ja myyjänä arvonlisäveron kirjanpitoa varten.

Kun käänteisen veron sisältävä ostolasku kirjataan, kirjanpitoon luodaan kaksi arvonlisäverotapahtumaa. Toisen tapahtuman verosuunta on **Saatava arvonlisävero**. Toisessa tapahtumassa verosuunta on **Maksettava arvonlisävero** ja **Käänteinen veloitus** -valintaruutu on valittu.
