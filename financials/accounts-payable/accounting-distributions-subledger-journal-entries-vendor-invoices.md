---
title: "Toimittajan laskujen kirjanpidolliset jaot ja alatason kirjauskansion merkinnät"
description: "Kirjanpidon jakoja käytetään määrittämään, miten summa käsitellään, esimerkiksi miten kulu, vara, vero tai maksu käsitellään toimittajan laskussa. Jokaisella määrällä, joka on huomioitava toimittajan laskun kirjauksen yhteydessä, on yksi tai useampi kirjanpidollinen jako."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: VendEditInvoice
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 26891
ms.assetid: 93dc608a-b5b4-4ec3-83c2-618e3d80a583
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 35133c305457b53abdf761f7fd557bf81bc28cde
ms.contentlocale: fi-fi
ms.lasthandoff: 05/25/2017


---

# <a name="accounting-distributions-and-subledger-journal-entries-for-vendor-invoices"></a>Toimittajan laskujen kirjanpidolliset jaot ja alatason kirjauskansion merkinnät

[!include[banner](../includes/banner.md)]


Kirjanpidon jakoja käytetään määrittämään, miten summa käsitellään, esimerkiksi miten kulu, vara, vero tai maksu käsitellään toimittajan laskussa. Jokaisella määrällä, joka on huomioitava toimittajan laskun kirjauksen yhteydessä, on yksi tai useampi kirjanpidollinen jako. 

<a name="accounting-distributions"></a>Kirjanpidolliset jaot 
-------------------------

Seuraavilla Toimittajan lasku -sivun painikkeilla voit tarkastella ja mahdollisesti muokata kirjanpidollisia jakoja kullekin ostotilauksen summalle.
-   **Jakosummat** – Tarkastele muokkaa yksittäisen rivin ja sen alatason rivien kirjanpidollisia jakoja, kuten veroja tai maksuja. Voit tarkastella ja muokata alarivin kirjanpidollisia jakoja myös suoraan Arvonlisäverotapahtumat- tai Kulutapahtumat-sivulla.
    -   Muokkaa toimittajan laskun otsikon summia, kuten kuluja tai valuutan pyöristyssummia.
    -   Muokkaa toimittajalaskun rivisummia.
-   **Näytä jakaumat** – Näytä asiakirjan kaikkien rivien kirjanpidolliset jaot. Et voi muokata kirjanpidollisia jakoja tästä näkymästä.
    -   Näytä otsikon ja rivien summat.

Jos toimittajalasku viittaa ostotilaukseen, voit jakaa ja muokata kirjanpidon jaot riveille, jotka sisältävät nimikkeen, joka ei ole varastossa. Jos toimittajan laskurivi viittaa ostotilausriviin, voit poistaa kirjanpitojaon. Et voi jakaa tai poistaa kulujen, verojen ja rivialennusten rivejä. Voi muokata kirjanpitotiliä, mutta et voi muuttaa summia tai prosentteja.
> [!NOTE]                                                                                                                                 
> Jos ylätason rivillä on nimike, joka ei ole varastossa, ja kirjanpidon jaot jaetaan, rivin alempi taso jaetaan automaattisesti vastaamaan ylätason rivin taloushallinnon dimensioita. Alirivin kirjanpidollisia jakoja ei voi lisäksi jakaa tai poistaa, mutta alirivin asetuksista riippuen, voit mahdollisesti muuttaa alirivin kirjanpidollisten jakojen kirjanpitotiliä.

## <a name="distributing-amounts"></a>Summien jakaminen
Kun syötät toimittajan lasku, jokainen määrä jaetaan seuraavasti.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Toimittajan laskun rivin tyyppi</th>
<th>Tärkeysjärjestys, joka määrittää, mistä päätili näkyy.</th>
<th>Tärkeysjärjestys, joka määrittää, mikä oletusarvoinen taloushallinnon dimensio tulee näkyviin.</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Varastotuote</td>
<td><ol>
<li>Kirjanpidollinen jako ostotilausriville.</li>
<li>Päätili-kenttä, kun Kirjaus-sivulla on valittu Tuotteen ostomeno.</li>
</ol></td>
<td><ol>
<li>Jos laskurivi on viittaus ostotilausriviin, käytä tilin jakoa ostotilausriville.</li>
<li>Käytä taloushallinnon oletusdimensioarvoja toimittajan laskulla.</li>
</ol></td>
</tr>
<tr class="even">
<td>Hankintaluokka tai tuote, jota ei ole varastossa</td>
<td><ol>
<li>Kirjanpidollinen jako ostotilausriville, jos toimittajalaskurivi viittaa ostotilausriviin.</li>
<li>Päätili-kenttä, kun Kirjaus-sivulla on valittu Kulun ostomeno.</li>
</ol></td>
<td><ol>
<li>Jos laskurivi on viittaus ostotilausriviin, käytä tilin jakoa ostotilausriville.</li>
<li>Jos päätili on kohdistustili, käytä oletusarvoa kohdistustilin määrityksestä.</li>
<li>Käytä taloushallinnon oletusdimensioarvoja toimittajan laskulla.</li>
<li>Käytä taloushallinnon dimension arvoja toimittajan laskun riviltä.</li>
<li>Käytä taloushallinnon oletusdimensioarvoja Tilikartta-sivun päätililtä.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Käyttöomaisuus</td>
<td><ol>
<li>Kirjanpidollinen jako ostotilausriville, jos toimittajalaskurivi viittaa ostotilausriviin.</li>
<li>Jos Toimittajan lasku -lomakkeessa Tapahtumatyyppi-kentästä on valittu Hankinta, Päätili-kenttä, kun Käyttöomaisuuserän kirjausprofiilit -sivulla on valittuna Hankinta.</li>
<li>Jos Tapahtumatyyppi-kentästä on valittu Hankintaoikaisu, Päätili-kenttä, kun Käyttöomaisuuserän kirjausprofiilit -sivulla on valittuna Hankintaoikaisu.</li>
</ol></td>
<td><ol>
<li>Käytä ostotilausriville tilijakoa, jos laskun rivi viittaa ostotilauksen riviin.</li>
<li>Käytä taloushallinnon dimension arvoja toimittajan laskun riviltä.</li>
<li>Käytä taloushallinnon oletusdimensioarvoja Tilikartta-sivun päätililtä.</li>
</ol></td>
</tr>
<tr class="even">
<td>Toimittajalaskurivillä määritetty projekti</td>
<td><ol>
<li>Kirjanpidollinen jako ostotilausriville, jos laskurivi viittaa ostotilausriviin.</li>
<li>Jos Projektiryhmät-sivulla Kirjaa kustannukset - Nimike -sivulta on valittu Saldo, Päätili-kenttä, kun Kirjanpidon asetukset sivulta on valittu Kustannus.</li>
<li>Jos Projektiryhmät-sivulla Kirjaa kustannukset - Nimike -sivulta on valittu Tulos, Päätili-kenttä, kun Kirjanpidon asetukset sivulta on valittu Kustannukset - Nimike.</li>
</ol></td>
<td><ol>
<li>Jos laskurivi on viittaus ostotilausriviin, käytä tilin jakoa ostotilausriville.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Rivialennus</td>
<td><ol>
<li>Kirjanpidollinen jako ostotilausriville, jos laskurivi viittaa ostotilausriviin.</li>
<li>Päätili-kenttä, kun Kirjaus-sivulta on valittu Alennus.</li>
<li>Jos alennuspäätiliä ei ole määritetty kirjausprofiilissa, kirjanpidon jako kokonaishinnalle tilauksen ostorivillä.</li>
</ol></td>
<td><ol>
<li>Jos laskurivi on viittaus ostotilausriviin, käytä kirjanpidon jakoa ostotilausriville.</li>
<li>Käytä taloushallinnon dimensioita laajennetun hinnan kirjanpidollisesta jaosta toimittajan laskun riviltä.</li>
<li>Käytä toimittajan laskurivin taloushallinnon dimension arvoja.</li>
<li>Käytä taloushallinnon oletusdimensioarvoja Tilikartta-sivun päätililtä.</li>
</ol></td>
</tr>
<tr class="even">
<td>Oston kulut, jotka on syötetty ostotilausrivin Hinta ja alennus -välilehteen</td>
<td><ol>
<li>Kirjanpidollinen jako ostotilausriville, jos laskurivi viittaa ostotilausriviin.</li>
<li>Ostotilausrivin laajennetun hinnan kirjanpidollinen jako.</li>
</ol></td>
<td><ol>
<li>Jos laskurivi on viittaus ostotilausriviin, käytä tilin jakoa ostotilausriville.</li>
<li>Käytä taloushallinnon dimensioita laajennetun hinnan kirjanpidollisesta jaosta toimittajan laskun riviltä.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Rivin kulu</td>
<td><ol>
<li>Kirjanpidollinen jako ostotilausriville, jos laskurivi viittaa ostotilausriviin.</li>
<li>Jos Kulujen koodi -lomakkeen Veloituslaji-kentästä on valittu Kirjanpitotili, Kulujen koodi -sivun Debet-tili-kenttä.</li>
<li>Jos Kulujen koodi -lomakkeen Veloituslaji-kentästä on valittu Nimike, ostotilausrivin laajennetun hinnan kirjanpidollinen jako.</li>
<li>Jos Kulujen koodi -lomakkeen Veloituslaji-kentästä on valittu Asiakas/Toimittaja, Kulujen koodi -sivun Kredit-tili-kenttä.</li>
</ol></td>
<td><ol>
<li>Jos laskurivi on viittaus ostotilausriviin, käytä tilin jakoa ostotilausriville.</li>
<li>Käytä taloushallinnon dimensioita laajennetun hinnan kirjanpidollisesta jaosta toimittajan laskun riviltä.</li>
<li>Käytä taloushallinnon dimension arvoja toimittajan laskun riviltä.</li>
<li>Käytä taloushallinnon oletusdimensioarvoja Tilikartta-sivun päätililtä.</li>
</ol></td>
</tr>
<tr class="even">
<td>Vero, seuraavalla ehdolla:
<ul>
<li>Käytä Yhdysvaltojen verotussääntöjä -vaihtoehto valitaan Kirjanpitoparametrit-sivulta.</li>
</ul></td>
<td><ol>
<li>Kirjanpidollinen jako ostotilausriville, jos laskurivi viittaa ostotilausriviin.</li>
<li>Kulun tai laajennetun hinnan kirjanpidollinen jako.</li>
</ol></td>
<td><ol>
<li>Jos laskurivi on viittaus ostotilausriviin, käytä tilin jakoa ostotilausriville.</li>
<li>Käytä taloushallinnon dimensioita laajennetun hinnan kirjanpidollisesta jaosta toimittajan laskun riviltä.</li>
<li>Käytä taloushallinnon dimension arvoja toimittajan laskun riviltä.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Vero, seuraavilla ehdoilla:
<ul>
<li>Käytä Yhdysvaltojen verotussääntöjä -vaihtoehdon valinta poistetaan Kirjanpitoparametrit-sivulla.</li>
<li>Arvonlisäveroryhmän Käyttövero-kentän valinta poistetaan Arvonlisäveroryhmät-sivulla.</li>
</ul></td>
<td><ol>
<li>Jos verosumma on palautettavissa, Kirjanpidon kirjausryhmät -sivun Saatava arvonlisävero -kenttä.</li>
<li>Jos verosummaa ei voi palauttaa, kokonaishinta tai kulun kirjanpidollinen jako.</li>
</ol></td>
<td><ol>
<li>Jos laskurivi on viittaus ostotilausriviin, käytä tilin jakoa ostotilausriville.</li>
<li>Käytä taloushallinnon dimensioita laajennetusta hinnasta tai kulun kirjanpidollisesta jaosta toimittajan laskun riviltä.</li>
<li>Käytä taloushallinnon dimension arvoja toimittajan laskun riviltä.</li>
<li>Käytä taloushallinnon oletusdimensioarvoja Tilikartta-sivun päätililtä.</li>
</ol></td>
</tr>
<tr class="even">
<td>Vero, seuraavilla ehdoilla:
<ul>
<li>Käytä Yhdysvaltojen verotussääntöjä -vaihtoehdon valinta poistetaan Kirjanpitoparametrit-sivulla.</li>
<li>Arvonlisäveroryhmän Käyttövero-kenttä valitaan Arvonlisäveroryhmät-sivulta.</li>
</ul></td>
<td><ol>
<li>Jos verosumma on palautettavissa, Kirjanpidon kirjausryhmät -sivun Saatava arvonlisävero -kenttä.</li>
<li>Jos verosumma ei ole palautettavissa, Kirjanpidon kirjausryhmät -sivun Käyttöverokulu-kenttä.</li>
</ol></td>
<td><ol>
<li>Jos laskurivi on viittaus ostotilausriviin, käytä tilin jakoa ostotilausriville.</li>
<li>Käytä taloushallinnon dimensioita laajennetusta hinnasta tai kulun kirjanpidollisesta jaosta toimittajan laskun riviltä.</li>
<li>Käytä taloushallinnon dimension arvoja toimittajan laskun riviltä.</li>
<li>Käytä taloushallinnon oletusdimensioarvoja Tilikartta-sivun päätililtä.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Otsikkomaksu</td>
<td><ol>
<li>Jos Kulujen koodi -lomakkeen Veloituslaji-kentästä on valittu Kirjanpitotili, Kulujen koodi -sivun Debet-tili-kenttä.</li>
<li>Jos Kulujen koodi -lomakkeen Veloituslaji-kentästä on valittu Asiakas/Toimittaja, Kulujen koodi -sivun Kredit-tili-kenttä.</li>
</ol></td>
<td><ol>
<li>Jos laskurivi on viittaus ostotilausriviin, käytä tilin jakoa ostotilausriville.</li>
<li>Jos päätili on kohdistustili, käytä oletusarvoa kohdistustilin määrityksestä.</li>
<li>Käytä taloushallinnon dimension oletusmallin arvoja toimittajan laskun otsikosta.</li>
<li>Käytä taloushallinnon dimension arvoja toimittajan laskun riviltä.</li>
<li>Käytä taloushallinnon oletusdimensioarvoja Tilikartta-sivun päätililtä.</li>
</ol></td>
</tr>
<tr class="even">
<td>Otsikkoalennus</td>
<td><ol>
<li>Toimittajan laskun alennus -kirjaustyypin Päätili-kenttä Automaattisten tapahtumien tilit -sivulla.</li>
</ol></td>
<td><ol>
<li>Jos laskurivi on viittaus ostotilausriviin, käytä tilin jakoa ostotilausriville.</li>
<li>Käytä taloushallinnon dimensioita laajennetun hinnan kirjanpidollisesta jaosta toimittajan laskun riviltä.</li>
<li>Käytä taloushallinnon dimension arvoja toimittajan laskun riviltä.</li>
<li>Käytä taloushallinnon oletusdimensioarvoja Tilikartta-sivun päätililtä.</li>
</ol></td>
</tr>
</tbody>
</table>

 
<a name="distributing-taxes"></a>Verojen jakaminen
------------------

verojen kirjanpidollisia jakoja ei voi luoda ennen verojen laskentaa. Jotta voit laskea arvonlisäverot, sinun on suoritettava jokin seuraavista Toimittajan lasku -sivun tehtävistä:
-   Näytä laskun summa.
-   Näytä arvonlisävero.
-   Näytä alareskontran kirjauskansio.
-   Näytä kirjanpidolliset jaot koko toimittajan laskulle.
-   Sijoita toimittajan lasku pitoon.
-   Kirjaa toimittajalasku.

## <a name="subledger-journals-for-vendor-invoices"></a>Alareskontran kirjauskansiot toimittajalaskuille
Ennen kuin kirjaat toimittajalaskun, voit tarkastella laskun koko kirjanpitokirjausta, joka sisältää hyvitykset ja veloitukset, jotta voit varmistaa, että lasku kirjataan oikeille tileille. Tämä kirjanpitomerkinnän koko näkymä tunnetaan nimellä alareskontran kirjauskansio. 

Jos alareskontran kirjaus on virheellinen esikatsellessa, et voi muokata sitä ennen kuin kirjaat toimittajatilauksen. Sen sijaan sinun on muokattava kirjanpidollisia jakoja tai kirjausprofiilia. Kirjanpidollisia jakoja käytetään määrittämään yksi kirjanpitomerkinnän puolista, debet tai kredit. Alareskontran kirjauskansion kirjanpitoviennin vastakirjaus luodaan käyttämällä kirjausprofiileja, kuten toimittajatili tai vero.






