---
title: Myyntilaskun luominen
description: Myyntitilauksen myyntilasku on myyntiin liittyvä lasku, jonka organisaatio antaa asiakkaalle.
author: ShivamPandey-msft
ms.date: 03/04/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustFreeInvoice
audience: Application User
ms.reviewer: twheeloc
ms.custom: 77772
ms.assetid: 00b4b40c-1576-4098-9aed-ac376fdeb8c5
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a0d1221e07f6dc4a5a99aa205c4a7f6fb367f000
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/16/2022
ms.locfileid: "9780507"
---
# <a name="create-a-customer-invoice"></a>Myyntilaskun luominen

[!include [banner](../includes/banner.md)]

**Myyntitilauksen myyntilasku** on myyntiin liittyvä lasku, jonka organisaatio antaa asiakkaalle. Tämän tyyppinen myyntilasku luonti perustuu myyntitilaukseen, jossa on tilausrivit ja nimiketunnukset. Nimiketunnukset määritetään ja kirjataan kirjanpitoon. Alareskontran kirjauskansioviennit eivät ole käytettävissä myyntitilauksen asiakaslaskulle. Lisätietoja on ohjeaiheessa [Myyntitilauksen laskujen luominen](tasks/create-sales-order-invoices.md).

**Vapaatekstilasku** ei liity myyntitilaukseen. Sen tilausriveillä on antamasi kirjanpitotilit, vapaatekstikuvaukset ja myyntisumma. Tällaiseen laskuun ei voi kirjoittaa nimiketunnusta. Arvonlisäverotiedot on kirjoitettava. Myynnin päätili ilmaistaan jokaisella laskurivillä, ja voit jakaa sen useille kirjanpitotileille valitsemalla **Jaa summat** **Vapaatekstilasku**-sivulla. Myös asiakkaan saldo kirjataan vapaatekstilaskussa käytetystä kirjausprofiilista yhteenvetotilille.

Lisätietoja:
 - [Luo vapaatekstilaskut](../accounts-receivable/create-free-text-invoice-new.md)
 - [Luo vapaatekstilaskumalli](../accounts-receivable/create-free-text-invoice-template-new.md)
 - [Vapaatekstilaskun mallin määrittäminen asiakkaalle](tasks/assign-free-text-invoice-template-customer.md)
 - [Luo ja kirjaa toistuvat vapaatekstilaskut](tasks/post-recurring-free-text-invoices.md)


**Proformalasku** on lasku, joka laaditaan todellisten laskusummien ennusteena ennen laskun kirjaamista. **Proformalaskun** voi tulostaa joko myyntilauksen myyntilaskulle tai vapaatekstilaskulle. 

>[!NOTE]
> Jos järjestelmä keskeyttää myynnin proformalaskuprosessin aikana, proformalasku voi jäädä orvoksi. Orvoksi jäänyt proformalasku voidaan poistaa suorittamalla kausittainen **Poista proformalaskut manuaalisesti** -työ. Valitse **Myynti ja markkinointi > Kausittaiset tehtävät > Puhdista > Poista proformalaskut manuaalisesti**.

## <a name="using-sales-order-customer-invoice-data-entities"></a>Myyntitilauksen myyntilaskun tietoyksiköiden käyttäminen
Tietoyksiköiden avulla voit tuoda ja viedä myyntitilauksen myyntilaskun tietoja. Myyntilaskun otsikon ja myyntilaskurivien tietoihin on eri yksiköt.

Seuraavat entiteetit ovat käytettävissä myyntilaskun otsikon tietojen osalta:

- **Myyntilaskukirjauskansion otsikon** yksikkö (SalesInvoiceJournalHeaderEntity)
- **Myyntilaskun otsikot V2** -yksikkö (SalesInvoiceHeaderV2Entity)

On suositeltavaa käyttää **myyntilaskukirjauskansion otsikon** yksikköä, koska se tarjoaa enemmän suorituskykyä myynnin otsikon tuonnissa ja viennissä. Tämä yksikkö ei sisällä **arvonlisäveron summan** (INVOICEHEADERTAXAMOUNT) saraketta, joka edustaa myyntilaskun otsikon arvonlisäveroarvoa. Jos liiketoimintaskenaario edellyttää tätä tietoa, tuo ja vie myyntilaskun otsikon tiedot **Myyntilaskun otsikot V2** -yksikön avulla.

Seuraavat entiteetit ovat käytettävissä myyntilaskun rivien tietojen osalta:

- **Myyntilaskurivien** yksikkö (BusinessDocumentSalesInvoiceLineItemEntity)
- **Myyntilaskurivit V3** -yksikkö (SalesInvoiceLineV3Entity)

Kun määrität viennissä käytettävää riviyksikköä, harkitse, käytetäänkö täyttä työntöä vai vähittäistä työntöä. Ota huomioon myös tietojen kokoonpano. **Myyntilaskurivit V3** -yksikkö tukee monimutkaisempia skenaarioita (esimerkiksi varastokenttiin määritystä). Se tukee myös täyden työnnön vientiskenaariota. Vähittäistä työntöä varten on suositeltavaa käyttää **Myyntilaskurivit**-yksikköä. Tämä yksikkö sisältää paljon yksinkertaisemman tietojen kokoonpanon kuin **Myyntilaskurivit V3** -yksikkö, ja sitä suositellaan erityisesti silloin, kun varastokentän integrointia ei tarvita. Erojen vuoksi, jotka liittyvät riviyksiköiden välisten vastaavuuksien tukeen, **Myyntilaskurivit**-yksikön suorituskyky on yleensä nopeampi kuin **Myyntilaskurivit V3** -yksiköllä.

## <a name="post-and-print-individual-customer-invoices-that-are-based-on-sales-orders"></a>Kirjaa ja tulosta yksittäisiä myyntilaskuja, jotka perustuvat myyntitilauksiin
Voit tämän prosessin avulla myyntitilaukseen perustuvan laskun. Tämä voi olla kätevää, jos päätät laskuttaa asiakasta ennen tavaroiden tai palvelujen toimittamista. 

Kun kirjaat laskun, jokaisen nimikkeen **Laskuttamatta**-määrä päivitetään valittujen myyntitilausten laskujen kokonaismäärän mukaiseksi. Jos myyntitilauksen kaikkien nimikkeiden **Laskuttamatta**-määrä ja **Jäljellä oleva määrä** on 0 (nolla), myyntitilauksen tilaksi muutetaan **Laskutettu**. Jos **Laskuttamatta**-määrä ei ole 0 (nolla), myyntitilauksen tilaa ei muuteta ja siihen voi lisätä laskuja.

Voit katsoa myyntitilausten tilaa **Kaikki myyntilaukset** -luettelosivulla. Voit tarkastella kirjattuja laskuja **Avoimet asiakaslaskut** -luettelosivulla.

## <a name="post-and-print-individual-customer-invoices-that-are-based-on-packing-slips-and-the-date"></a>Kirjaa ja tulosta yksittäisiä myyntilaskuja, jotka perustuvat pakkausluetteloihin ja päivämäärään
Käytä tätä prosessia, kun myyntitilaukselle on kirjattu vähintään yksi pakkausluettelo. Myyntilasku perustuu näiden tuotteiden pakkausluetteloihin ja vastaa niiden määriä. Laskun kirjanpitotiedot perustuvat tietoihin, jotka syötettiin laskujen kirjauksen yhteydessä. 

Voit luoda myyntilaskun niiden pakkausluettelon rivinimikkeiden perusteella, jotka on toimitettu tähän mennessä, vaikka kaikkia tietyn myyntitilauksen nimikkeitä ei olisi vielä toimitettu. Näin kannattaa tehdä esimerkiksi silloin, kun yritys lähettää asiakkaalle kuukaudessa yhden laskun, joka sisältää kaikki kuukauden aikana tehdyt toimitukset. Jokainen pakkausluettelo edustaa myyntitilauksen nimikkeiden osatoimitusta tai täydellistä toimitusta. 

Kun kirjaat laskun, jokaisen nimikkeen **Laskuttamatta**-määrä päivitetään valittujen pakkausluetteloiden toimitusten kokonaismäärällä. Jos myyntitilauksen kaikkien nimikkeiden **Laskuttamatta**-määrä ja **Jäljellä oleva määrä** on 0 (nolla), myyntitilauksen tilaksi muutetaan **Laskutettu**. Jos **Laskuttamatta**-määrä ei ole 0 (nolla), myyntitilauksen tilaa ei muuteta ja siihen voi lisätä laskuja. 

Varastotapahtumat päivitetään laskun numerolla ja myyntitilauksen **Rivin tila** -kentän tilaksi muutetaan **Laskutettu**. 

Voit tarkastella myyntitilausten tilaa **Kaikki myyntilaukset** -luettelosivulla.

## <a name="consolidate-sales-orders-or-packing-slips-for-posting"></a>Konsolidoi kirjattavat myyntitilaukset tai pakkausluettelot
Käytä tätä prosessia, kun vähintään yksi myyntitilaus on valmis laskutettavaksi ja haluat konsolidoida ne yhteen laskuun. 

Voit valita **Myyntitilaus**-luettelosivulla useita laskuja ja konsolidoida ne sitten **Luo laskuja** -vaihtoehdolla. Voit muuttaa **Laskun kirjaus** -sivulla **Yhteenvetotilaus**-asetuksen muodostamaan yhteenvedon tilausnumeron mukaan (jossa yhdelle myyntitilaukselle on useita pakkausluetteloita) tai laskutustilin mukaan (jossa yhdellä laskutustilillä on useita myyntitilauksia). Konsolidoi myyntitilaukset yhdeksi laskuksi **Järjestä**-painikkeella **Yhteenvetotilaus**-asetusten perusteella.

## <a name="split-sales-order-invoices-by-site-and-delivery-information"></a>Myyntitilauslaskujen jakaminen toimipaikka- ja toimitustietojen mukaan
**Myyntireskontran parametrit** -sivun **Yhteenvedon päivitys** -välilehdessä voit konfiguroida myyntitilauksen myyntilaskujen jakamisen toimipaikan tai toimitusosoitteen mukaan. 
 - Valitse **Jaa laskun toimipaikan perusteella** -vaihtoehto, kun haluat luoda kirjauksen yhteydessä yhden laskun toimipaikkaa kohti. 
 - Valitse **Jaa laskun toimitustietojen perusteella** -vaihtoehto, kun haluat luoda yhden laskun yhtä myyntitilausrivin toimitusosoitetta kohden. 

## <a name="post-to-revenue-account-for-sales-order-lines-that-have-no-price-and-no-cost"></a>Kirjaa Tuotto-tilille myyntitilauksen rivit, joilla ei ole hintaa eikä kustannusta
Voit myös päivittää **kirjanpidon** **Tuotto**-tilin myyntitilausriveille, joilla ei ole hintaa eikä kustannusta. 

Voit määrittää nämä tiedot tai tarkastella niitä seuraavasti:
1. Siirry **Myyntireskontran parametri** -sivun **Kirjanpito ja arvonlisävero** -välilehden **Kirjaa Tuotto-tilille myyntitilauslaskun rivit, joiden hinta ja kustannus on nolla** -kohtaan. (**Myyntireskontra > Asetukset > Myyntireskontran parametrit**). 
2. Valitse **Kyllä**, jos haluat päivittää sellaisen myyntitilauslaskurivin **Tuotto** tilin, jolla ei ole hintaa eikä kustannusta. 
 - Jos tämä vaihtoehto on valittuna, tosite sisältää 0,00 merkintää **Asiakkaan saldo**- ja **Tuotto**-kirjaustyypeiltä. Tuottotili määritetään **Varastokirjaus**-parametrin sivulla **Myyntitilaus**-tilin määrityksen välilehdessä. 
 - Jos tätä vaihtoehtoa ei ole valittu, **tuottotilille** ei kirjata rivejä, joilla ei ole hinta- tai kustannustietoja. Tämän sijaan tosite sisältää 0,00 merkintää **Asiakkaan saldo** -kirjaustyypiltä.

## <a name="line-creation-sequence-number-information"></a>Rivin luonnin järjestysnumeron tiedot
Myyntilaskun rivejä kirjatessa on mahdollista luoda peräkkäiset rivin luonnin järjestysnumerot. Rivin luonnin järjestysnumerot määritetään kirjausprosessin aikana. Myyntilaskujen kirjauksen suorituskykyä voi parantaa sallimalla muun kuin peräkkäisen numeroinnin. Peräkkäistä numerointia odottavat kolmannen osapuolen integroinnit voivat käyttää rivin luonnin järjestysnumeroita. Lisätietoja rivin luonnin järjestysnumerot integroivista laajennuksista voi pyytää lisätietoja IT-osastolta.

Nämä tiedot määritetään tai niitä voi tarkastella määrittämällä **Määritä peräkkäiset rivinumerot myyntilaskun rivejä kirjattaessa** -vaihtoehdon **Myyntireskontran parametrit** -sivun **Päivitykset**-sivulla:

- Valitse **Ei**, jos rivin luonnin järjestysnumeroissa käytetään ei-peräkkäisiä numeroita.
- Valitse **Kyllä**, jos käytetään peräkkäisiä numeroita. Valinnaksi on määritettävä **Kyllä**, jos yrityksen ensisijainen osoite on Italiassa. Valinnaksi on määritettävä **Kyllä** myös silloin, jos **CustInvoiceTransRandLineCreationSeqNumFlight**-väliversio on poistettu käytöstä.

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







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
