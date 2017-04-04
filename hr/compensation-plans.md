---
title: Kompensaatiosuunnitelmat
description: "Kompensaatio- ja etuuspäälliköt voiva käyttää kompensaation hallintaa organisaation työntekijöiden kiinteiden ja muuttuvien kompensaatiosuunnitelmien ylläpitämisessä ja käsittelemisessä."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: HcmCompensationLevel, HRCCompGrid, HRMCompFixedAction, HRMCompFixedBudget, HRMCompFixedPlanTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 6f4429202efd0506378d681188035c5cc69f56a1
ms.openlocfilehash: 1809a6679685e483694a53b7742d80f02ade2cd5
ms.lasthandoff: 03/31/2017


---

# <a name="compensation-plans"></a>Kompensaatiosuunnitelmat

Kompensaatio- ja etuuspäälliköt voiva käyttää kompensaation hallintaa organisaation työntekijöiden kiinteiden ja muuttuvien kompensaatiosuunnitelmien ylläpitämisessä ja käsittelemisessä.

### <a name="introduction"></a>Johdanto

Kompensaationhallinnan avulla ohjataan peruspalkan ja palkkioiden maksamista toimittaminen. Työntekijän kiinteän peruspalkan ja palkankorotusten hallitaan kiinteän kompensaatiosuunnitelmien avulla. Bonusmaksujen, suorituskykypalkkioiden, optioiden, lahjoitusten sekä muiden kannusteiden maksamista hallitaan muuttuvan kompensaation suunnitelmien avulla. 

Työntekijä voidaan liittää yhteen tai useaan suunnitelmaan, ja työntekijällä voidaan käyttää kumpaakin suunnitelmatyyppiä. Työntekijän on täytettävä seuraavat vaatimukset, ennen kuin hänet voi rekisteröidä kompensaatiosuunnitelmaan:
-   Työntekijällä on oltava aktiivinen toimen määritys.
-   Työntekijä on täytettävä kompensaatiosuunnitelman kelpoisuussääntöjen ehdot.

## <a name="compensation-setup"></a> Kompensaation määrittäminen
Seuraavassa taulukossa on luettelo kompensaatioprosessin komponenteista, jotka voivat olla olennaisia yrityksen kompensaatiosuunnitelmien määrittämisessä.

<table>
<thead>
<tr class="header">
<th>Komponentti</th>
<th>Lisätietoja…</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Kiinteän kompensaation toiminnot</td>
<td>Kiinteän kompensaation toiminnot, joilla on kaksi tarkoitusta:
<ul>
<li>Toiminnoilla voidaan määrittää minkälaiset tiedot on kirjattava, kun työntekijän kompensaatio muuttuu. Voit esimerkiksi edellyttää, että muutoksen syy, kuten ylennys tai alennus, kirjataan.</li>
<li>Toiminnot voidaan varmistaa, että laskennassa käytetään, kun kiinteitä kompensaatiosuunnitelmia käsitellään.  Esimerkiksi Osakepääoma verrata työntekijöiden palkan ja työntekijän tasolla vähintään vertailukohteen ja varmistaa työntekijän hakeminen maksetaan vähintään vähimmäismäärän.</li>
</ul></td>
</tr>
<tr class="even">
<td>Tasot</td>
<td>Tasot on liitetty töihin ja mahdollisiin työviittaukseen liittyviin toimiin. Voit luoda yksittäisiä tasoja kolmelle kompensaatiosuunnitelmatyypille: palkkaluokka, kompensaatioluokka ja vaihe.</td>
</tr>
<tr class="odd">
<td>Palkka-alueen käyttöastematriisi</td>
<td>Palkka-alueen käyttöastematriisi auttaa siirtämään työntekijät työtä vastaavaan tarkistuspisteeseen. Voit myös ohjata palkka-alueen käyttöasteen avulla yrityksen palkkiopääomia huomioimatta yksittäisen työntekijän suoritustasoa tai yrityksen yleistä suoritustasoa. Esimerkiksi työntekijöille, joille maksetaan palkka-alueella pienempää palkkaa, annetaan suuremmat prosenttikorotukset kuin palkka-alueella suurempaa palkkaa saaville työntekijöille. Tällä tavoin voit järjestelmällisesti siirtää pääoman eroja. Palkka-alueen käyttöaste lasketaan seuraavasti: (kiinteä palkkio – alueen vähimmäisarvominimi) ÷ (alueen enimmäisarvo – alueen vähimmäisarvo).</td>
</tr>
<tr class="even">
<td>Viitepisteiden määritykset</td>
<td>Viitepisteiden määritykset sisältävät matriisin palkka-alueita kuvaavien viitepisteiden joukon. Kukin palkka-alue voidaan liittää palkkioon. Palkkaluokka suunnitelmissa käytetään viitepisteinä usein vähimmäisarvo, keskiarvoa ja enimmäisarvoa.</td>
</tr>
<tr class="odd">
<td>Kompensaatiomatriisi</td>
<td>Kompensaatiomatriisin on joukko viitepisteitä ja tasoja, joiden avulla luodaan kompensaatiorakenne.</td>
</tr>
<tr class="even">
<td>Kompensaatiorakenne</td>
<td>Kompensaatiorakenne on kompensaatiomatriisi, jossa palkkiot on liitetty kunkin tason viitepisteisiin.</td>
</tr>
<tr class="odd">
<td>Oikeutussäännöt</td>
<td>Oikeutussääntöjen avulla tunnistetaan tiettyjen töiden, työtehtävien, työtyyppien, osastojen, ammattijärjestöjen tai kompensaatioalueiden työntekijät, joita tietyt kompensaatiosuunnitelmat koskevat. Oikeutussäännöt on luotava sekä muuttuville että kiinteille kompensaatiosuunnitelmille, jotta työntekijä voidaan rekisteröidä suunnitelmaan. Kun kompensaatiosuunnitelman oikeutussäännöt on määritetty, voit määrittää tasot, joita sovelletaan suunnitelman kattamiin töihin.</td>
</tr>
<tr class="even">
<td>Maksutiheydet</td>
<td>Ajanjakso, jolle on määritetty korvaus käytetään maksutiheyksiä.  Esimerkiksi maksu taajuus-auttaa sinua ymmärtämään Jos korvauksen summa määritetään vuotuinen palkka hourly vs. palkkio. Maksutiheyksiä ovat myös käyttää Määritä muuntokertoimet muunnettaessa summia korvausta kuukausittain, viikoittain, kahden viikon ja hourly maksutiheydet vuosittain Maksutiheyden.</td>
</tr>
<tr class="odd">
<td>Kompensaatioalueet</td>
<td>Kompensaatioalueiden avulla määritetään työntekijän kompensaatio työpaikan sijainnin perusteella.</td>
</tr>
<tr class="even">
<td>Tarkistuspiste</td>
<td>Tarkistuspiste määrittää, mikä on ihanteellisen palkkio kompensaatiotason kaikille työntekijöille. Palkkaluokkasuunnitelmien rakenteissa tarkistuspisteet ovat yleensä palkka-alueen keskikohdassa. Kompensaatioluokkarakenteissa tarkistuspisteitä käytetään harvoin. Voit määrittää kiinteän kompensaatiosuunnitelman tarkistuspisteen Kiinteät kompensaatiosuunnitelmat -lomakkeessa.</td>
</tr>
<tr class="odd">
<td>Työtehtävät</td>
<td>Työtehtävien avulla luokitellaan ja suodatetaan tiettyjen töiden kompensaatiosuunnitelmat.</td>
</tr>
<tr class="even">
<td>Työtyypit</td>
<td>Työtyyppien avulla luokitellaan ja suodatetaan tiettyjen töiden kompensaatiosuunnitelmat.</td>
</tr>
<tr class="odd">
<td>Muuttuvan kompensaation tyypit</td>
<td>Muuttuvat kompensaatiotyypit, kuten osakepalkkiot ja käteispalkkiot, määritetään muuttuvissa kompensaatiosuunnitelmissa.</td>
</tr>
<tr class="even">
<td>Kompensaatioruudukot</td>
<td>Kompensaatioruudukot sisällä olevan kompensaatiosuunnitelman rakenne.  Kompensaatioruudukot voidaan käyttää yhden tai useamman kompensaatiosuunnitelmien mukaan.</td>
</tr>
<tr class="odd">
<td>Suorituskykysuunnitelmat</td>
<td>Suorituskykysuunnitelmien avulla voidaan liittää suorituskyky kohdistusmatriisiin käytettäväksi suoritusperusteisessa palkkastrategiassa.</td>
</tr>
<tr class="even">
<td>Suorituskykyluokitukset</td>
<td>Suorituskykyluokituksia käytetään suorituskykysuunnitelmissa määrittämään tulospalkkion tai suorituskykypalkkion summa.</td>
</tr>
</tbody>
</table>

## <a name="process-events"></a>Prosessitapahtumat
Prosessitapahtuma laskee tietyn kauden kompensaatiotiedot kaikille työntekijöille, jotka on rekisteröity vähintään yhteen kiinteään tai muuttuvaan kompensaatiosuunnitelmaan. Voit suorittaa prosessitapahtuman toistuvasti laskettujen kompensaatiotulosten testaamiseksi tai päivittämiseksi.

<a name="compensation-events"></a>Kompensaatiotapahtumat
-------------------

Prosessitapahtuma suoritetaan, aina korvausta tapahtuma luodaan.  Kompensaatiotapahtumat sisältää kunkin työntekijän kyseisen tapahtuman sisälly kompensaatioprosessi tuloksista.  Kun laskelmat ovat oikein, voit ladata kompensaation tietueiden päivittämistä työntekijöille, jotka vaikuttavat prosessitapahtuman kompensaatiotapahtuman.

## <a name="recommendations"></a> Suositukset
Voit suositella prosessitapahtuman suorittamisen jälkeen muutoksia työntekijän palkankorotus- tai palkkiosummaan prosessitapahtuman laskemien ohjeiden perusteella. Työntekijäsuositusten tekeminen edellyttää, että suositukset on otettu käyttöön, kun kompensaatiosuunnitelmat tai prosessitapahtuma määritettiin.


