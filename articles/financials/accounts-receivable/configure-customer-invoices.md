---
title: Myyntilaskun luominen
description: '**Myyntitilauksen myyntilasku** on myyntiin liittyvä lasku, jonka organisaatio antaa asiakkaalle.'
author: ShivamPandey-msft
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustFreeInvoice
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 77772
ms.assetid: 00b4b40c-1576-4098-9aed-ac376fdeb8c5
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: aa49b70b07ac3dc6cbc5989b11981098f22be89c
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/01/2019
ms.locfileid: "1835211"
---
# <a name="create-a-customer-invoice"></a>Myyntilaskun luominen

[!include [banner](../includes/banner.md)]

**Myyntitilauksen myyntilasku** on myyntiin liittyvä lasku, jonka organisaatio antaa asiakkaalle. Tämän tyyppinen myyntilasku luonti perustuu myyntitilaukseen, jossa on tilausrivit ja nimiketunnukset. Nimiketunnukset määritetään ja kirjataan kirjanpitoon. Alareskontran kirjauskansioviennit eivät ole käytettävissä myyntitilauksen asiakaslaskulle. Lisätietoja on ohjeaiheessa [Myyntitilauksen laskujen luominen](tasks/create-sales-order-invoices.md).

**Vapaatekstilasku** ei liity myyntitilaukseen. Sen tilausriveillä on antamasi kirjanpitotilit, vapaatekstikuvaukset ja myyntisumma. Tällaiseen laskuun ei voi kirjoittaa nimiketunnusta. Arvonlisäverotiedot on kirjoitettava. Myynnin päätili ilmaistaan jokaisella laskurivillä, ja voit jakaa sen useille kirjanpitotileille valitsemalla **Jaa summat** **Vapaatekstilasku**-sivulla. Myös asiakkaan saldo kirjataan vapaatekstilaskussa käytetystä kirjausprofiilista yhteenvetotilille.

Lisätietoja on kohdassa 

[Luo vapaatekstilasku](../accounts-receivable/create-free-text-invoice-new.md)

[Vapaatekstilaskumallin luominen](../accounts-receivable/create-free-text-invoice-template-new.md)

[Vapaatekstilaskumallin määrittäminen asiakkaalle](tasks/assign-free-text-invoice-template-customer.md)

[Luo ja kirjaa toistuvat vapaatekstilaskut](tasks/post-recurring-free-text-invoices.md)


**Proformalasku** on lasku, joka laaditaan todellisten laskusummien ennusteena ennen laskun kirjaamista. Proformalaskun voi tulostaa joko myyntilauksen myyntilaskulle tai vapaatekstilaskulle.

## <a name="post-and-print-individual-customer-invoices-that-are-based-on-sales-orders"></a>Kirjaa ja tulosta yksittäisiä myyntilaskuja, jotka perustuvat myyntitilauksiin
Voit tämän prosessin avulla myyntitilaukseen perustuvan laskun. Tämä voi olla kätevää, jos päätät laskuttaa asiakasta ennen tavaroiden tai palvelujen toimittamista. 

Kun kirjaat laskun, jokaisen nimikkeen **Laskuttamatta**-määrä päivitetään valittujen myyntitilausten laskujen kokonaismäärän mukaiseksi. Jos myyntitilauksen kaikkien nimikkeiden **Laskuttamatta**-määrä ja **Jäljellä oleva määrä** on 0 (nolla), myyntitilauksen tilaksi muutetaan **Laskutettu**. Jos **Laskuttamatta**-määrä ei ole 0 (nolla), myyntitilauksen tilaa ei muuteta ja siihen voi lisätä laskuja.

Voit katsoa myyntitilausten tilaa **Kaikki myyntilaukset** -luettelosivulla. Voit tarkastella kirjattuja laskuja **Avoimet asiakaslaskut** -luettelosivulla.

## <a name="post-and-print-individual-customer-invoices-that-are-based-on-packing-slips-and-the-date"></a>Kirjaa ja tulosta yksittäisiä myyntilaskuja, jotka perustuvat pakkausluetteloihin ja päivämäärään
Käytä tätä prosessia, kun myyntitilaukselle on kirjattu vähintään yksi pakkausluettelo. Myyntilasku perustuu näiden tuotteiden pakkausluetteloihin ja vastaa niiden määriä. Laskun kirjanpitotiedot perustuvat tietoihin, jotka syötettiin laskujen kirjauksen yhteydessä. 

Voit luoda myyntilaskun niiden pakkausluettelon rivinimikkeiden perusteella, jotka on toimitettu tähän mennessä, vaikka kaikkia tietyn myyntitilauksen nimikkeitä ei olisi vielä toimitettu. Näin kannattaa tehdä esimerkiksi silloin, kun yritys lähettää asiakkaalle kuukaudessa yhden laskun, joka sisältää kaikki kuukauden aikana tehdyt toimitukset. Jokainen pakkausluettelo edustaa myyntitilauksen nimikkeiden osatoimitusta tai täydellistä toimitusta. 

Kun kirjaat laskun, jokaisen nimikkeen **Laskuttamatta**-määrä päivitetään valittujen pakkausluetteloiden toimitusten kokonaismäärällä. Jos myyntitilauksen kaikkien nimikkeiden **Laskuttamatta**-määrä ja **Jäljellä oleva määrä** on 0 (nolla), myyntitilauksen tilaksi muutetaan **Laskutettu**. Jos **Laskuttamatta**-määrä ei ole 0 (nolla), myyntitilauksen tilaa ei muuteta ja siihen voi lisätä laskuja. 

Varastotapahtumat päivitetään laskun numerolla ja myyntitilauksen **Rivin tila** -kentän tilaksi muutetaan **Laskutettu**. 

Voit katsoa myyntitilausten tilaa **Kaikki myyntilaukset** -luettelosivulla.

## <a name="consolidate-sales-orders-or-packing-slips-for-posting"></a>Konsolidoi kirjattavat myyntitilaukset tai pakkausluettelot
Käytä tätä prosessia, kun vähintään yksi myyntitilaus on valmis laskutettavaksi ja haluat konsolidoida ne yhteen laskuun. 

Voit valita **Myyntitilaus**-luettelosivulla useita laskuja ja konsolidoida ne sitten **Luo laskuja** -vaihtoehdolla. Voit muuttaa **Laskun kirjaus** -sivulla **Yhteenvetotilaus**-asetuksen muodostamaan yhteenvedon tilausnumeron mukaan (jossa yhdelle myyntitilaukselle on useita pakkausluetteloita) tai laskutustilin mukaan (jossa yhdellä laskutustilillä on useita myyntitilauksia). Konsolidoi myyntitilaukset yhdeksi laskuksi **Järjestä**-painikkeella **Yhteenvetotilaus**-asetusten perusteella.

## <a name="additional-settings-that-change-the-posting-behavior"></a>Kirjaustoimintoa muuttavat lisäasetukset
Seuraavat kentät muuttaa kirjausprosessin toimintaa.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Kenttä</th>
<th>Kuvaus</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Määrä</td>
<td>Valitse määrät, joihin asiakirjan kirjaaminen perustuu. Kentän vaihtoehdot vaihtelevat ja määräytyvät kirjattavan asiakirjan tyypin mukaan. Asiakirja voi olla esimerkiksi pakkausluettelo tai lasku.
<ul>
<li><strong>Toimita nyt</strong> – Valitse kaikki <strong>Toimita nyt</strong> -kenttään annetut määrät. Tällä vaihtoehdolla voit tehdä osittaisen tilausvahvistuksen tai toimituksen.</li>
<li><strong>Keräilty</strong> – valitse kaikki kerätyt määrät.</li>
<li><strong>Kaikki</strong> – valitse kaikki myyntitilausmäärät, joita ei ole vielä päivitetty nykyisellä asiakirjatyypillä.</li>
<li><strong>Pakkausluettelo</strong> – valitse kaikki määrät, jotka on päivitetty pakkausluettelolla.</li>
<li><strong>Kerätty määrä ja muut kuin varastoidut tuotteet</strong> – valitse kaikki kerätyt määrät ja kaikki tuotemäärät, joita ei ole varastoitu.</li>
</ul></td>
</tr>
<tr class="even">
<td>Kirjaus</td>
<td><ul>
<li>Valitse tämä vaihtoehto, jos haluat kirjata myyntitilauksen.</li>
<li>Poista tämän vaihtoehdon valinta, jos haluat tulostaa proformamyyntitilauksen. <strong>Huomautus:</strong> Jos sovit maksusuunnitelman, maksusuunnitelma ei näy proformamyyntitilauksessa. Maksusuunnitelmat näkyvät vain varsinaisessa myyntitilauksessa.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Myöhäinen valinta</td>
<td>Valitse tämä vaihtoehto, jos haluat käyttää valittua kyselyä myöhemmin. Tätä vaihtoehtoa käytetään komentojonotöissä. Kysely suoritetaan, kun komentojonotyö suoritetaan.</td>
</tr>
<tr class="even">
<td>Vähennä määrää</td>
<td>Valitse tämä vaihtoehto, jos haluat automaattisesti vähentää toimitettua määrää tiedostoa kirjatessa, jotta toimitettu määrä vastaisi käytettävissä olevaa varastoa.</td>
</tr>
<tr class="odd">
<td>Tulosta</td>
<td>Valitse, milloin asiakirjat tulostetaan:
<ul>
<li><strong>Valittu</strong> – tulosta asiakirjat, kun lasku on päivitetty.</li>
<li><strong>Jälkeen</strong> – tulosta asiakirjat, kun kaikki laskut on päivitetty.</li>
</ul>
<strong>Huomautus:</strong> <strong>Tulosta</strong>-kenttä on käytettävissä vain, jos <strong>Tulosta lasku</strong>-, <strong>Tulosta vahvistus</strong>-, <strong>Tulosta keräysluettelo</strong>- tai <strong>Tulosta pakkausluettelo</strong> -vaihtoehto on valittu. Voit esimerkiksi määrittää <strong>Lomakkeen lajittelu</strong> -sivulla järjestelmän lajittelemaan tiedot laskutustilin perusteella. Voit sitten valita <strong>Jälkeen</strong>, jos haluat tulostaa asiakirjat laskutilin mukaan lajitelluissa erissä. Muussa tapauksessa asiakirjat tulostetaan ennen kuin niiden käsittely on valmis, eikä asiakirjoja lajitella <strong>Lomakkeen lajittelu</strong> -sivulla määritetyssä järjestyksessä.</td>
</tr>
<tr class="even">
<td>Tulosta lasku</td>
<td>Valitse tämä vaihtoehto, kun haluat tulostaa laskun. Jos tämä vaihtoehto on poistettu käytöstä, voit kirjata laskun sitä tulostamatta.</td>
</tr>
<tr class="odd">
<td>Lähetä sähköposti</td>
<td>Valitsemalla tämän voit lähettää myyntitilauksen laskun asiakkaalle sähköpostin liitteenä laskun kirjaamisen jälkeen. Liitteet lähetetään PDF- ja XML-tiedostoina. Tämä vaihtoehto on käytettävissä vain, jos valitset <strong>Ota CFD käyttöön (sähköiset laskut)</strong> -vaihtoehdon <strong>Sähköisten laskujen parametrit</strong> -sivulla. <strong>Huomautus:</strong> (MEX) Tämä ohjausobjekti on vain niiden yritysten käytettävissä, joiden ensisijainen osoite on Meksikossa.</td>
</tr>
<tr class="even">
<td>Käytä tulostuksenhallinnan kohdetta</td>
<td>Valitsemalla tämän vaihtoehdon voit käyttää tapahtumalle, asiakirjalle tai moduulille <strong>Tulostuksenhallinnan asetukset</strong> -sivulla määritettyjä tulostusasetuksia.</td>
</tr>
<tr class="odd">
<td>Tarkista luottoraja</td>
<td>Valitse, mitä luottorajan tarkistuksessa analysoidaan.
<ul>
<li><strong>Ei mitään</strong> – Luottorajatarkistusta ei tarvitse tehdä.</li>
<li><strong>Saldo</strong> – Luottorajaa verrataan asiakkaan saldoon.</li>
<li><strong>Saldo + pakkausluettelo tai tuotteen vastaanotto</strong> – luottorajaa verrataan asiakkaan saldoon ja toimituksiin.</li>
<li><strong>Saldo+Kaikki</strong> – Luottorajaa verrataan asiakkaan saldoon, toimituksiin ja avoimiin tilauksiin.</li>
</ul></td>
</tr>
<tr class="even">
<td>Hyvityksen oikaisu</td>
<td>Valitse tämä vaihtoehto, jos haluat näyttää hyvityslaskun veloituksena tositetapahtumissa.</td>
</tr>
<tr class="odd">
<td>Jäljelle jäävän luoton määrä</td>
<td>Valitse tämä vaihtoehto, jos kirjaat hyvityslaskua ja haluat säilyttää jäljelle jäävän määrän tilauksessa. Jos tämän vaihtoehdon valinta poistetaan, jäljelle jääväksi määräksi määritetään 0 (nolla).</td>
</tr>
<tr class="even">
<td>Päivitysyhteenveto mille:</td>
<td>Valitse, miten useista myyntitilauksista luodaan yhteenveto:
<ul>
<li><strong>Ei mitään</strong> – Älä luo myyntitilauksista yhteenvetoa. Kutakin myyntitilausta varten luodaan esimerkiksi erillinen lasku.</li>
<li><strong>Laskutustili</strong> – tee yhteenveto kaikista valituista tilauksista <strong>Yhteenvedon päivitysparametrit</strong> -sivulla määritettyjen ehtojen mukaisesti.</li>
<li><strong>Tilaus</strong> – Luo valitusta tilausvalikoimasta yhteenveto yhdeksi määrittämäksesi tilaukseksi. Tilauksista luodaan yhteenveto <strong>Yhteenvedon päivitysparametrit</strong> -sivulla määritettyjen ehtojen mukaisesti. Jos valitset tämän vaihtoehdon, myös <strong>Myyntitilaus</strong>-kentästä on valittava arvo.</li>
<li><strong>Automaattinen yhteenveto</strong> – Jos yhteenvetopäivitykset on määritetty <strong>Yhteenvedon päivitys</strong> -sivulla, luo kaikista valituista tilauksista yhteenveto <strong>Yhteenvedon päivitysparametrit</strong> -sivulla määritettyjen ehtojen perusteella. Jos yhteenvetopäivityksiä ei ole määritetty, tilaus kirjataan erikseen.</li>
<li><strong>Pakkausluettelo</strong> – Luo valitusta tilausvalikoimasta yksi yhteenvetolasku pakkausluetteloa kohden. Tämä vaihtoehto on käytettävissä vain, jos <strong>Määrä</strong>-kentästä on valittu <strong>Pakkausluettelo</strong>.</li>
</ul></td>
</tr>
</tbody>
</table>





