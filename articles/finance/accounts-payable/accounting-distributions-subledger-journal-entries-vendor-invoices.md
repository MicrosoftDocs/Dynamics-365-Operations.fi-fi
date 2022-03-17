---
title: Toimittajan laskujen kirjanpidolliset jaot ja kirjauskansioviennit
description: Kirjanpidon jakoja käytetään määrittämään, miten summa käsitellään, esimerkiksi miten kulu, vara, vero tai maksu käsitellään toimittajan laskussa. Jokaisella määrällä, joka on huomioitava toimittajan laskun kirjauksen yhteydessä, on yksi tai useampi kirjanpidollinen jako.
author: sunfzam
ms.date: 02/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: VendEditInvoice
audience: Application User
ms.reviewer: twheeloc
ms.custom: 26891
ms.assetid: 93dc608a-b5b4-4ec3-83c2-618e3d80a583
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f10ddf113f59da4800a97a48300ab1310bfb42dd
ms.sourcegitcommit: 9cbff8a2cdeaf606488fb0044b3de4ab4409c9dc
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/26/2022
ms.locfileid: "8358178"
---
# <a name="accounting-distributions-and-journal-entries-for-vendor-invoices"></a>Toimittajan laskujen kirjanpidolliset jaot ja kirjauskansioviennit

[!include [banner](../includes/banner.md)]

Kirjanpidon jakoja käytetään määrittämään, miten summa käsitellään, esimerkiksi miten kulu, vara, vero tai maksu käsitellään toimittajan laskussa. Jokaisella määrällä, joka on huomioitava toimittajan laskun kirjauksen yhteydessä, on yksi tai useampi kirjanpidollinen jako. 

## <a name="accounting-distributions"></a>Kirjanpidolliset jaot 

Seuraavilla Toimittajan lasku -sivun painikkeilla voit tarkastella ja mahdollisesti muokata kirjanpidollisia jakoja kullekin ostotilauksen summalle.
-   **Jakosummat** – Tarkastele muokkaa yksittäisen rivin ja sen alatason rivien kirjanpidollisia jakoja, kuten veroja tai maksuja. Voit tarkastella ja muokata alarivin kirjanpidollisia jakoja myös suoraan **Arvonlisäverotapahtumat**- tai **Kulutapahtumat**-sivulla.
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
<li><strong>Päätili</strong>-kenttä, kun <strong>Kirjaus</strong>-sivulla on valittu Tuotteen ostomeno.</li>
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
<li><strong>Päätili</strong>-kenttä, kun <strong>Kirjaus</strong>-sivulla on valittu Kulun ostomeno.</li>
</ol></td>
<td><ol>
<li>Jos laskurivi on viittaus ostotilausriviin, käytä tilin jakoa ostotilausriville.</li>
<li>Jos päätili on kohdistustili, käytä oletusarvoa kohdistustilin määrityksestä.</li>
<li>Käytä taloushallinnon oletusdimensioarvoja toimittajan laskulla.</li>
<li>Käytä taloushallinnon dimension arvoja toimittajan laskun riviltä.</li>
<li>Käytä taloushallinnon oletusdimensioarvoja <strong>Tilikartta</strong>-sivun päätililtä.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Käyttöomaisuuserä</td>
<td><ol>
<li>Kirjanpidollinen jako ostotilausriville, jos toimittajalaskurivi viittaa ostotilausriviin.</li>
<li>Jos <strong>Toimittajan lasku</strong> -lomakkeessa <strong>Tapahtumatyyppi</strong>-kentästä on valittu <strong>Hankinta</strong>, <strong>Päätili</strong>-kenttä, kun <strong>Käyttöomaisuuserän kirjausprofiilit</strong> -sivulla on valittuna <strong>Hankinta</strong>.</li>
<li>Jos <strong>Tapahtumatyyppi</strong>-kentästä on valittu <strong>Hankintaoikaisu</strong>, <strong>Päätili</strong>-kenttä, kun <strong>Käyttöomaisuuserän kirjausprofiilit</strong> -sivulla on valittuna <strong>Hankintaoikaisu</strong>.</li>
</ol></td>
<td><ol>
<li>Käytä ostotilausriville tilijakoa, jos laskun rivi viittaa ostotilauksen riviin.</li>
<li>Käytä taloushallinnon dimension arvoja toimittajan laskun riviltä.</li>
<li>Käytä taloushallinnon oletusdimensioarvoja <strong>Tilikartta</strong>-sivun päätililtä.</li>
</ol></td>
</tr>
<tr class="even">
<td>Toimittajalaskurivillä määritetty projekti</td>
<td><ol>
<li>Kirjanpidollinen jako ostotilausriville, jos laskurivi viittaa ostotilausriviin.</li>
<li>Jos <strong>Projektiryhmät</strong>-sivulla <strong>Kirjaa kustannukset - Nimike</strong> -sivulta on valittu <strong>Saldo</strong>, <strong>Päätili</strong>-kenttä, kun <strong>Kirjanpidon asetukset</strong> -sivulta on valittu <strong>Kustannus</strong>.</li>
<li>Jos <strong>Projektiryhmät</strong>-sivulla <strong>Kirjaa kustannukset - Nimike</strong> -sivulta on valittu <strong>Tulos</strong>, <strong>Päätili</strong>-kenttä, kun <strong>Kirjanpidon asetukset</strong> -sivulta on valittu <strong>Kustannukset - Nimike</strong>.</li>
</ol></td>
<td><ol>
<li>Jos laskurivi on viittaus ostotilausriviin, käytä tilin jakoa ostotilausriville.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Rivialennus</td>
<td><ol>
<li>Kirjanpidollinen jako ostotilausriville, jos laskurivi viittaa ostotilausriviin.</li>
<li><strong>Päätili</strong>-kenttä, kun <strong>Kirjaus</strong>-sivulta on valittu <strong>Alennus</strong>.</li>
<li>Jos alennuspäätiliä ei ole määritetty kirjausprofiilissa, kirjanpidon jako kokonaishinnalle tilauksen ostorivillä.</li>
</ol></td>
<td><ol>
<li>Jos laskurivi on viittaus ostotilausriviin, käytä kirjanpidon jakoa ostotilausriville.</li>
<li>Käytä taloushallinnon dimensioita laajennetun hinnan kirjanpidollisesta jaosta toimittajan laskun riviltä.</li>
<li>Käytä toimittajan laskurivin taloushallinnon dimension arvoja.</li>
<li>Käytä taloushallinnon oletusdimensioarvoja <strong>Tilikartta</strong>-sivun päätililtä.</li>
</ol></td>
</tr>
<tr class="even">
<td>Oston kulut, jotka on syötetty ostotilausrivin <strong>Hinta ja alennus</strong> -välilehteen</td>
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
<li>Jos <strong>Kulujen koodi</strong> -lomakkeen <strong>Veloituslaji</strong>-kentästä on valittu <strong>Kirjanpitotili</strong>, <strong>Kulujen koodi</strong> -sivun <strong>Debet-tili</strong>-kenttä.</li>
<li>Jos <strong>Kulujen koodi</strong> -sivun <strong>Veloituslaji</strong>-kentästä on valittu <strong>Nimike</strong>, ostotilausrivin laajennetun hinnan kirjanpidollinen jako.</li>
<li>Jos <strong>Kulujen koodi</strong> -sivun <strong>Veloituslaji</strong>-kentästä on valittu <strong>Asiakas/Toimittaja</strong>, <strong>Kulujen koodi</strong> -sivun <strong>Kredit-tili</strong>-kenttä.</li>
</ol></td>
<td><ol>
<li>Jos laskurivi on viittaus ostotilausriviin, käytä tilin jakoa ostotilausriville.</li>
<li>Käytä taloushallinnon dimensioita laajennetun hinnan kirjanpidollisesta jaosta toimittajan laskun riviltä.</li>
<li>Käytä taloushallinnon dimension arvoja toimittajan laskun riviltä.</li>
<li>Käytä taloushallinnon oletusdimensioarvoja <strong>Tilikartta</strong>-sivun päätililtä.</li>
</ol></td>
</tr>
<tr class="even">
<td>Vero, seuraavalla ehdolla:
<ul>
<li>Käytä <strong>Yhdysvaltojen verotussääntöjä</strong> -vaihtoehto valitaan <strong>Kirjanpitoparametrit</strong>-sivulta.</li>
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
<li><strong>Käytä Yhdysvaltojen verotussääntöjä</strong> -vaihtoehdon valinta poistetaan <strong>Kirjanpitoparametrit</strong>-sivulla.</li>
<li>Arvonlisäveroryhmän <strong>Käyttövero</strong>-kentän valinta poistetaan <strong>Arvonlisäveroryhmät</strong>-sivulla.</li>
</ul></td>
<td><ol>
<li>Jos verosumma on palautettavissa, <strong>Kirjanpidon kirjausryhmät</strong> -sivun <strong>Saatava arvonlisävero</strong> -kenttä.</li>
<li>Jos verosummaa ei voi palauttaa, kokonaishinta tai kulun kirjanpidollinen jako.</li>
</ol></td>
<td><ol>
<li>Jos laskurivi on viittaus ostotilausriviin, käytä tilin jakoa ostotilausriville.</li>
<li>Käytä taloushallinnon dimensioita laajennetusta hinnasta tai kulun kirjanpidollisesta jaosta toimittajan laskun riviltä.</li>
<li>Käytä taloushallinnon dimension arvoja toimittajan laskun riviltä.</li>
<li>Käytä taloushallinnon oletusdimensioarvoja <strong>Tilikartta</strong>-sivun päätililtä.</li>
</ol></td>
</tr>
<tr class="even">
<td>Vero, seuraavilla ehdoilla:
<ul>
<li>Käytä Yhdysvaltojen verotussääntöjä -vaihtoehdon valinta poistetaan <strong>Kirjanpitoparametrit</strong>-sivulla.</li>
<li>Arvonlisäveroryhmän <strong>Käyttövero</strong>-kenttä valitaan <strong>Arvonlisäveroryhmät</strong>-sivulta.</li>
</ul></td>
<td><ol>
<li>Jos verosumma on palautettavissa, <strong>Kirjanpidon kirjausryhmät</strong> -sivun <strong>Saatava arvonlisävero</strong> -kenttä.</li>
<li>Jos verosumma ei ole palautettavissa, <strong>Kirjanpidon kirjausryhmät</strong> -sivun <strong>Käyttöverokulu</strong>-kenttä.</li>
</ol></td>
<td><ol>
<li>Jos laskurivi on viittaus ostotilausriviin, käytä tilin jakoa ostotilausriville.</li>
<li>Käytä taloushallinnon dimensioita laajennetusta hinnasta tai kulun kirjanpidollisesta jaosta toimittajan laskun riviltä.</li>
<li>Käytä taloushallinnon dimension arvoja toimittajan laskun riviltä.</li>
<li>Käytä taloushallinnon oletusdimensioarvoja <strong>Tilikartta</strong>-sivun päätililtä.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Otsikkomaksu</td>
<td><ol>
<li>Jos <strong>Kulujen koodi</strong> -lomakkeen <strong>Veloituslaji</strong>-kentästä on valittu <strong>Kirjanpito</strong>-tili, <strong>Kulujen koodi</strong> -sivun <strong>Debet-tili</strong>-kenttä.</li>
<li>Jos <strong>Kulujen koodi</strong> -sivun <strong>Veloituslaji</strong>-kentästä on valittu <strong>Asiakas/Toimittaja</strong>, <strong>Kulujen koodi</strong> -sivun <strong>Kredit-tili</strong>-kenttä.</li>
</ol></td>
<td><ol>
<li>Jos laskurivi on viittaus ostotilausriviin, käytä tilin jakoa ostotilausriville.</li>
<li>Jos päätili on kohdistustili, käytä oletusarvoa kohdistustilin määrityksestä.</li>
<li>Käytä taloushallinnon dimension oletusmallin arvoja toimittajan laskun otsikosta.</li>
<li>Käytä taloushallinnon dimension arvoja toimittajan laskun riviltä.</li>
<li>Käytä taloushallinnon oletusdimensioarvoja <strong>Tilikartta</strong>-sivun päätililtä.</li>
</ol></td>
</tr>
<tr class="even">
<td>Otsikkoalennus</td>
<td><ol>
<li><strong>Toimittajan laskun alennus -kirjaustyypin</strong> <strong>Päätili</strong>-kenttä <strong>Automaattisten tapahtumien tilit</strong> -sivulla.</li>
</ol></td>
<td><ol>
<li>Jos laskurivi on viittaus ostotilausriviin, käytä tilin jakoa ostotilausriville.</li>
<li>Käytä taloushallinnon dimensioita laajennetun hinnan kirjanpidollisesta jaosta toimittajan laskun riviltä.</li>
<li>Käytä taloushallinnon dimension arvoja toimittajan laskun riviltä.</li>
<li>Käytä taloushallinnon oletusdimensioarvoja <strong>Tilikartta</strong>-sivun päätililtä.</li>
</ol></td>
</tr>
</tbody>
</table>


## <a name="distributing-taxes"></a>Verojen jakaminen

verojen kirjanpidollisia jakoja ei voi luoda ennen verojen laskentaa. Jotta voit laskea arvonlisäverot, sinun on suoritettava jokin seuraavista **Toimittajan lasku** -sivun tehtävistä:
-   Näytä laskun summa.
-   Näytä arvonlisävero.
-   Näytä alareskontran kirjauskansio.
-   Näytä kirjanpidolliset jaot koko toimittajan laskulle.
-   Sijoita toimittajan lasku pitoon.
-   Kirjaa toimittajalasku.

## <a name="subledger-journals-for-vendor-invoices"></a>Alareskontran kirjauskansiot toimittajalaskuille
Ennen kuin kirjaat toimittajalaskun, voit tarkastella laskun koko kirjanpitokirjausta, joka sisältää hyvitykset ja veloitukset, jotta voit varmistaa, että lasku kirjataan oikeille tileille. Tämä kirjanpitomerkinnän koko näkymä tunnetaan nimellä alareskontran kirjauskansio. 

Jos alareskontran kirjaus on virheellinen esikatsellessa, et voi muokata sitä ennen kuin kirjaat toimittajatilauksen. Sen sijaan sinun on muokattava kirjanpidollisia jakoja tai kirjausprofiilia. Kirjanpidollisia jakoja käytetään määrittämään yksi kirjanpitomerkinnän puolista, debet tai kredit. Alareskontran kirjauskansion kirjanpitoviennin vastakirjaus luodaan käyttämällä kirjausprofiileja, kuten toimittajatili tai vero.







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
