---
title: Tuotekonfiguraatiomallien yleiskatsaus
description: Tässä artikkelissa esitellään tuotekonfiguraatiomallieihin liittyvät ehdot ja käsitteet. Tuotekonfiguraatiomallien avulla voidaan luoda yleisiä tuoterakenteita, joita käytetään määritettäessä yhdestä tuotteesta useita tuotevariantteja.
author: cvocph
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PCProductConfigurationModelDetails, PCProductConfigurationModelListPage, PCModalWaitDialog, PCTemplateConfigurationManager, PCConfigurationUIGrouping
audience: Application User
ms.reviewer: kamaybac
ms.custom: 4031
ms.assetid: 70b968e8-e550-4731-823d-d713b8910f7b
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e82eb3fcfe4347b7faa4c775e9909a792e2b9baf
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4983313"
---
# <a name="product-configuration-models-overview"></a>Tuotekonfiguraatiomallien yleiskatsaus

[!include [banner](../includes/banner.md)]

Tässä artikkelissa esitellään tuotekonfiguraatiomallieihin liittyvät ehdot ja käsitteet. Tuotekonfiguraatiomallien avulla voidaan luoda yleisiä tuoterakenteita, joita käytetään määritettäessä yhdestä tuotteesta useita tuotevariantteja.

Tuotekonfiguraatiomallit luodaan vastaamaan yleistä tuoterakennetta. Kun tuotekonfiguraatiomalli on määritetty, voit määrittää erillisen tuotevariantin, jolla on yksilöllinen tuoterakenne ja yksilöllinen reititys. Tuotekonfiguraatiomalleja käytetään sekä määrittävinä rajoituksina että pakottavina laskelmina. Niiden avulla käsitellään eri tuotevarianttien välisiä suhteita ja rajoituksia. Voit määrittää nimikkeitä myyntitilauksissa, myyntitarjouksissa, ostotilauksissa ja tuotantotilauksissa. Seuraavassa taulukossa kuvataan taulurajoituksiin perustuvia ehtoja ja käsitteitä.
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Komponentit</td>
<td>Komponentit ovat tuotekonfiguraatiomallin tärkeimmät rakenneosat. Komponentit näytetään puurakenteena <strong>Rajoituspohjaisen tuotemääritysmallin tiedot</strong> -sivulla. Komponentit voivat sisältää seuraavat elementit:
<ul>
<li>Määritteet</li>
<li>Rajoitukset</li>
<li>Laskelmat</li>
<li>Alikomponentit</li>
<li>Käyttäjän vaatimukset</li>
<li>Tuoterakenteen rivit</li>
<li>Reitityksen työvaihe</li>
</ul></td>
</tr>
<tr class="even">
<td>Määritteet</td>
<td>Ominaisuudet kuvaavat kaikki tuotekonfiguraatiomallin ominaisuudet. Määritysten avulla voit määrittää ominaisuudet, jotka voidaan valita, erillistä tuotetta konfiguroitaessa. Määritteitä käytetään rajoituksina ja ehtoina. Kun määritteitä luodaan ja lisätään tuotekonfiguraatiomalliin, liittyviin määritetyyppeihin luodaan viittaukset. Määritteelle voidaan asettaa oletusarvo. Oletusarvoa käytetään konfiguroinnin käyttöliittymässä (UI) tuotekonfiguraatiomallia määritettäessä. Voit määrittää, että määrite on pakollinen, vain luku -tyyppinen tai piilotettu.
<ul>
<li><strong>Pakollinen</strong> – määritteelle on asetettava arvo, kun tuotetta määritetään.</li>
<li><strong>Vain luku</strong> – määritteen arvo näkyy konfigurointi-istunnon aikana, mutta sitä ei voi muuttaa.</li>
<li><strong>Piilotettu</strong> – määritteen arvo sisältyy rajoituksiin ja ehtoihin, mutta sitä ei näytetä määritysistunnon aikana.</li>
</ul>
Voit määrittää ehdon myös määritteille. Jos ehto täyttyy, pakolliselle määritteelle on kirjoitettava arvo. Ehdot ovat lausekkeita, jotka on täytettävä tuotekonfiguraatiomalliin sisällytettäville määritteille, tuoterakenneriveille ja reitityksen työvaiheille. Mikä tahansa ehdossa viitattava määrite muuttuu pakolliseksi. On suositeltavaa, että määritteet määritetään pakollisiksi <strong>Määritteet</strong>-välilehdessä. Tämä voi helpottaa tunnistamaan pakolliset määritteet. Määritteiden arvot ovat tärkeä osa konfiguraatioiden uudelleen käyttöä. Järjestelmä käyttää määritearvoja määrittääkseen, onko olemassa konfiguraatiota, joka vastaa käyttäjän konfigurointi-istunnon aikana suorittamia valintoja.</td>
</tr>
<tr class="odd">
<td>Määritetyypit</td>
<td>Määritetyypit määrittävät määritteille joukon tuotemääritysmallissa käytettäviä tietotyyppejä. Seuraavat määritetyypit ovat käytössä:
<ul>
<li><strong>Kokonaisluku</strong>, jolla voi tarvittaessa olla alue</li>
<li><strong>Desimaali</strong></li>
<li><strong>Teksti</strong>, jolla voi tarvittaessa olla kiinteä luettelo</li>
<li><strong>Totuusarvo</strong></li>
</ul>
Jos määritetyyppinä on <strong>Totuusarvo</strong>, <strong>Kokonaisluku</strong> ja alue tai <strong>Teksti</strong> ja kiinteä luettelo, arvojoukko on käytettävissä, kun tuotekonfiguraatiomalli määritetään. <strong>Huomautus:</strong> Tuotekonfiguraation selvitin tunnistaa vain seuraavat määritetyypit: <strong>Totuusarvo</strong>, <strong>Teksti</strong> ja kiinteäluettelo sekä <strong>Kokonaisluku</strong> ja alue. Tämän vuoksi vain näitä määritetyyppejä voidaan käyttää lausekkeen rajoituksissa ja ehdoissa.</td>
</tr>
<tr class="even">
<td>Rajoitukset</td>
<td>Rajoitukset kuvaavat tuotemallikonfiguraation rajoituksia. Rajoituksilla taataan vain kelvollisten arvojen valinta tuotetta määritettäessä. Rajoitteet voivat olla joko lausekerajoituksia tai taulukkorajoituksia:
<ul>
<li>Lausekerajoituksia voidaan käyttää vain komponentille johon ne on sidottu. Komponentin lausekerajoitukset voivat viitata komponentin alikomponenttien määritteisiin. Tuotekonfiguraation selvittimellä ratkaistaan rajoitukset ja rajoitukset on laadittava selvittimen syntaksin mukaisesti. Lisätietoja on lauseke- ja taulurajoituksia käsittelevässä aiheessa.</li>
<li>Taulun rajoituksia ei voi käyttää tuotekonfiguraatiomallin osassa, ennen kuin ne on määritetty. Taulun rajoitukset voivat olla joko käyttäjän tai järjestelmän määrittämiä. Käyttäjän määrittämä taulurajoitus on matriisi, jonka avulla voidaan kuvata joukko yhdistelmiä määritearvoille, jotka määritetyypit ovat määrittäneet. Jos valmistetaan esimerkiksi kaiuttimia, käyttäjän määrittämän taulurajoituksen matriisi voi sisältää kaiuttimen viimeistelyn ja säleikön sarakkeet.</li>
</ul>
<strong>Esimerkki</strong> Kaiuttimissa on valittavana neljä viimeistelyä: musta, tammi, palisanteri ja valkoinen. Kaiuttimilla on kolme etusäleikkövaihtoehtoa: musta, metalli tai valkoinen. Musta viimeistely on valittavana kaikkiin säleikköihin, mutta kahta muuta voi käyttää vain tietyissä säleiköissä. Seuraavassa on taulussa esimerkki tiedoista, jotka näkyvät <strong>Muokkaa taulurajoitusta</strong> -sivun <strong>Sallitut yhdistelmät</strong> -välilehdessä.
<table>
<thead>
<tr class="header">
<th>Kaapin viimeistely</th>
<th>Etusäleikkö</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Musta</td>
<td>Musta</td>
</tr>
<tr class="even">
<td>Musta</td>
<td>Metalli</td>
</tr>
<tr class="odd">
<td>Musta</td>
<td>Valkoinen</td>
</tr>
<tr class="even">
<td>Tammi</td>
<td>Musta</td>
</tr>
<tr class="odd">
<td>Palisanteri</td>
<td>Valkoinen</td>
</tr>
<tr class="even">
<td>Valkoinen</td>
<td>Musta</td>
</tr>
<tr class="odd">
<td>Valkoinen</td>
<td>Valkoinen</td>
</tr>
</tbody>
</table>
Järjestelmän määrittämä taulurajoitus vastaa Supply Chain Management -taulukon määritetyypin ja kentän yhdistämismääritystä. Järjestelmän määrittämä taulurajoitus linkittää dynaamisesti määritetyypin kenttään. Linkin avulla tuotekonfiguraatiomallin määrite vastaa Supply Chain Management -taulun kentän tietoja.</td>
</tr>
<tr class="odd">
<td>Laskelmat</td>
<td>Laskelmat täydentävät rajoituksia. Laskemilla voi tehdä laskutoimituksia <strong>Desimaali</strong>- ja <strong>Kokonaisluku</strong>-määritetyypeissä tai loogisia toimintoja määritteissä, joiden tyyppi on <strong>Teksti</strong> ja kiinteä luettelo sekä <strong>Totuusarvo</strong>. Laskelmalla on kohdemäärite, johon laskelmalausekkeen tulos sijoitetaan. Laskelmalauseke muodostetaan lauseke-editorilla.</td>
</tr>
<tr class="even">
<td>Alikomponentit</td>
<td>Alikomponentit kuvaavat tuotekonfiguraatiomallin puurakennetta. Voit luoda tuotekonfiguraatiomallin rakenteen alikomponenttien avulla. Alikomponentit viittaavat olemassa oleviin komponentteihin. Tämän vuoksi alikomponentit edistävät komponenttien uudelleenkäyttöä useissa tuotekonfiguraatiomalleissa. Alikomponentin <strong>Tuoterakennerivin tiedot</strong> -sivulla alikomponentille voi valita erillisen arvon. Vaihtoehtoisesti voit valita määritteen, jonka arvo on valittu, kun tuotekonfiguraatiomalli on määritetty. Jotta tuotteen voisi sisällyttää komponenttina tai alikomponenttina, seuraavat <strong>Luo tuote</strong> -sivun tiedot on määritettävä tuotteen luonnin yhteydessä:
<ul>
<li>Valitse <strong>Tuotetyyppi</strong>-kentässä <strong>Nimike</strong>.</li>
<li>Valitse <strong>Tuotteen alatyyppi</strong> -kentässä <strong>Päätuote</strong>.</li>
<li>Valitse <strong>Määritysmenetelmä</strong> -kentässä <strong>Rajoituspohjainen määritys</strong>.</li>
</ul>
Voit tarkastella <strong>Vapautetun tuotteen tiedot</strong> -sivun <strong>Yleiset</strong>-välilehdessä, voiko vapautettua tuotetta käyttää komponenttina tai alikomponenttina. Jos <strong>Rajoituspohjainen määritys</strong> on valittu <strong>Määritysmenetelmä</strong>-kentässä, tuotetta voi käyttää komponenttina tai alikomponenttina. Voit piilottaa alikomponentit siten, että käyttäjä ei näe niitä määritysistunnon aikana. Myös alikomponenttiin liittyvät määritteet, alikomponentit ja käyttäjävaatimukset piilotetaan.</td>
</tr>
<tr class="odd">
<td>Käyttäjän vaatimukset</td>
<td>Käyttäjän vaatimukset kuvaavat abstraktiota käyttäjän vaatimusten ja tiettyjen komponenttien ja määritteiden välillä. Et voi yhdistää käyttäjän vaatimusta nimikkeeseen. Esimerkiksi asiakas ostaa kotiteatterijärjestelmää. Myyntiedustaja saattaa kysyä huoneen kokoa johon asiakas asentaa järjestelmän määrittääkseen kuinka monta wattia vaaditaan. Tässä esimerkissä huoneen koko voi olla käyttäjän vaatimus, joka auttaa määrittämään sopivan määritearvon tietylle komponentille. Voit piilottaa käyttäjän vaatimukset siten, että niitä ei näytetä käyttäjälle tuotemääritysistunnon aikana. Myös käyttäjän vaatimukseen liittyvät määritteet, alikomponentit ja käyttäjän vaatimukset piilotetaan. Voit kirjoittaa ehdon, joka hallitsee voidaanko käyttäjän vaatimus piilottaa. Ehto kirjoitetaan OML (Optimization Modeling Language) -syntaksina.</td>
</tr>
<tr class="even">
<td>Tuoterakenteen rivit</td>
<td>Tuoterakenteen rivit vastaavat yksittäisiä komponenttien materiaaleja tuotekonfiguraatiomallissa. <strong>Tuoterakennerivin tiedot</strong> -sivun kaikki nimikkeet ovat valittavissa. Tuoterakenteen riville voidaan lisätä tuotekonfiguraatiomallia määritettäessä ehto, jonka mukaan erilliselle tuotevariantille valitut tuoterakennerivit voivat vaihdella käyttäjän valinnan mukaan. Ehdot ovat lausekkeita, jotka on täytettävä tuotekonfiguraatiomalliin sisällytettäville määritteille, tuoterakenneriveille ja reitityksen työvaiheille. Voit valita <strong>Tuoterakennerivin tiedot</strong> -sivulla erillisen arvon. Vaihtoehtoisesti voit yhdistää määritteeseen, jonka arvo valittiin tuotekonfiguraatiomallin määrityksen yhteydessä.</td>
</tr>
<tr class="odd">
<td>Reitityksen työvaihe</td>
<td>Voit valita <strong>Reitityksen työvaiheen tiedot</strong> -sivulla erillisen arvon. Vaihtoehtoisesti voit yhdistää määritteeseen, jonka arvo valittiin tuotekonfiguraatiomallin määrityksen yhteydessä. Ehdot kirjoitetaan vastaavalla tavalla kuin lausekerajoitukset. Ehdot ovat lausekkeita, jotka on täytettävä tuotekonfiguraatiomalliin sisällytettäville määritteille, tuoterakenneriveille ja reitityksen työvaiheille.</td>
</tr>
</tbody>
</table>







[!INCLUDE[footer-include](../../includes/footer-banner.md)]