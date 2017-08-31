---
title: Toimitusvaihtoehdot
description: "Myyntitilausten vastaanottajat voivat löytää vaihtoehtoisia tilauksen toteutusvaihtoehtoja Toimitusvaihtoehdot-sivulta."
author: ChristianRytt
manager: AnnBe
ms.date: 04/10/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SalesLineDeliveryDetails
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 271623
ms.assetid: 527f6084-44fe-41bb-924f-4386e926358a
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: crytt
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: HT
ms.sourcegitcommit: 1945d137b337508a1850e3e679a60487aecb6b84
ms.openlocfilehash: 9240e86a80e23ed5e787bdb3dd1a72b0318e3cc0
ms.contentlocale: fi-fi
ms.lasthandoff: 07/27/2017

---

# <a name="delivery-alternatives"></a>Toimitusvaihtoehdot

[!include[banner](../includes/banner.md)]


Myyntitilausten vastaanottajat voivat löytää vaihtoehtoisia tilauksen toteutusvaihtoehtoja Toimitusvaihtoehdot-sivulta.

Myyntitilausten vastaanottajat voivat Microsoft Dynamics 365 for Operations -versiossa 1611 (marraskuu 2016) selvittää vaihtoehtoisia tilauksen toteutusvaihtoehtoja **Toimitusvaihtoehdot**-sivulla. Uudelleenjärjestelty sivuasettelu antaa paremman yleiskuvan kaikista vaihtoehdoista. Sen avulla tilausten vastaanottajat voivat nähdä toteutusmahdollisuuksia muistakin yrityksistä. Sen avulla he voivat nyt tarkastella sekä konsernin sisäisiä että ulkoisilta toimittajilta saatavia mahdollisuuksia. Myyntitilausten vastaanottajat saavat älykkään luettelon toimitusvaihtoehdoista suodattamalla vaihtoehtoja toimituspäivämäärän mukaan. Käytössä on lisäksi parametreja, jotka auttavat ehdotettujen toimitusten hallinnassa. Koska kuljetusaika voi vaikuttaa toimituspäiviin, myyntitilausten vastaanottajat voivat tarkastella rahdinkuljettajien tarjoamia kuljetusvaihtoehtoja. Kullekin ehdotukselle näytetään yksityiskohtaiset tiedot, joiden perusteella tilausten vastaanottajat voivat tehdä päätöksensä suoraan **Toimitusvaihtoehdot** -sivulla.

## <a name="open-the-delivery-alternatives-page"></a>Avaa Toimitusvaihtoehdot-sivu
Voit avata **Toimitus****vaihtoehdot**-sivun myyntitilausriviltä.

1.  Valitse **Tuotteet ja toimitus** &gt; **Toimitusvaihtoehdot**.
2.  Valitse **Rivin tiedot** &gt; **Toimitus** &gt; **Toimitusvaihtoehdot**.

Voit avata **Toimitusvaihtoehdot**-sivun myös avaamalla **Myyntitilausten käsittely ja kysely** -työtilan ja napsauttamalla **Tilaukset ja suosikit** &gt; **Viivästyneet tilausrivit** &gt; **Toimitusvaihtoehdot** **Huomautus:** Voit avata **Toimitusvaihtoehdot**-sivun vain, jos seuraavat ehdot täyttyvät:

-   Kaikki pakolliset myyntirivin tiedot täytetään.
-   **Toimituspäivämäärän tarkistus** -kentän arvoksi on määritetty jokin muu arvo kuin **Ei**.

## <a name="delivery-date-control-methods"></a>Toimituspäivämäärän tarkistusmenetelmät
Toimituspäivämäärän tarkistusmenetelmä määrittää, miten järjestelmä määrää toimituspäivämäärät, miten toimitusvaihtoehdot lasketaan, ja mitä tietoja näytetään. Huomaa, että toimitustietojen tarkistus ottaa kalenterit huomioon. Seuraavat kalenterit voivat tämän vuoksi vaikuttaa ehdotettuun vastaanottopäivään: Varaston kalenteri, Toimituskalenteri, Toimittajan kalenteri ja Asiakkaan kalenteri. Seuraavassa taulukossa kuvataan toimituspäivämäärän tarkistusmenetelmät.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Tapa</strong></td>
<td><strong>Kuvaus</strong></td>
</tr>
<tr class="even">
<td><strong>Ei mitään</strong></td>
<td><ul>
<li>Myyntirivien toimitusvaihtoehdot eivät ole tuettuja. Tämä asetus poistaa toimitustietojen tarkistuksen käytöstä.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Myynnin läpimenoaika</strong></td>
<td><ul>
<li>Toimitusvaihtoehdot lasketaan ennalta määritetyn myynnin läpimenoajan perusteella. Kuljetuspäivät lasketaan toimitustavan perusteella.</li>
<li>Toimitusvaihtoehdot sisältävät varastot, joilla on käytettävissä olevaa varastoa ja kysyntä-/tarjontatilauksiin.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>ATP</strong></td>
<td><ul>
<li>Toimitusvaihtoehdot lasketaan luvattavissa olevan määrän (ATP) logiikalla. Huomioon otetaan päivän saatavuus ja odotettu tuleva saatavuus. Kuljetuspäivät lasketaan toimitustavan perusteella.</li>
<li>Toimitusvaihtoehdot sisältävät varastot, joilla on käytettävissä olevaa varastoa ja kysyntä-/tarjontatilauksiin.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>ATP + toimitusmarginaali</strong></td>
<td><ul>
<li>Toimitusvaihtoehdot lasketaan ATP-menetelmällä, mutta laskelmaan sisältyy toimitusmarginaali.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Saatavuus (CTP)</strong></td>
<td><ul>
<li>Toimitusvaihtoehdot lasketaan saatavuuden (CTP) logiikalla. Saatavuus lasketaan tarvesuunnittelun hajotuksen avulla. Huomaa, että CTP-menetelmä siirtää toimituspäiviä eteenpäin vähintään myynnin läpimenoajalla. Kuljetuspäivät lasketaan toimitustavan perusteella.</li>
<li>Toimitusvaihtoehdot sisältävät ehdotuksia seuraavista varastoista:
<ul>
<li>Nykyinen varasto</li>
<li>Oletusvarasto</li>
<li>Kaikki varastot, joilla on käytettävissä olevaa varastoa</li>
<li>Kaikki varastot, joilla on toimitustilauksia</li>
<li>Kaikki varastot, joilla on aktiivisia tuoterakenneversioita</li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="view-information-about-delivery-alternatives"></a>Toimitusvaihtoehtojen tietojen tarkasteleminen
Tässä osassa kuvataan kussakin **Toimitusvaihtoehdot**-sivun välilehdessä käytettävissä olevat toimitusvaihtoehtojen tiedot.

### <a name="products"></a>Tuotteet

Tässä välilehdessä on yhteenveto nykyisen myyntirivin tuotteesta ja tiedoista.

### <a name="delivery-alternatives"></a>Toimitusvaihtoehdot

Tässä välilehdessä näytetään luettelo vastaanottotietojen perusteella lajitelluista toimitusvaihtoehdoista. Voit valita ehdotuksen perusteena olevat vaihtoehdot luettelon yläpuolelta. Voit myös toimitustavan, joka määrittää kuljetuspäivät. Valittavissa ovat seuraavat vaihtoehdot:

-   **Sisällytä muut tuotevariantit** - Tämä vaihtoehto on saatavilla tuotteille, joilla on tuotevariantteja. Se sisältää toimitusvaihtoehtoja tuotteen muille varianteille. Tämä vaihtoehto ei ole käytettävissä saatavuusmallille.
-   **Sisällytä osittainen määrä** - Oletusarvon mukaan vain ehdotukset, jotka sisältävät myyntirivin täyden määrän sisällytetään. Valitsemalla tämän vaihtoehdot voit sisällyttää ehdotukset, jotka täyttävät tilausrivin vain osittain. Tämä on hyödyllistä silloin, kun asiakas pyytää aikaisempaa toimituspäivää ja hyväksy osatoimituksen.
-   **Sisällytä myöhemmät päivämäärät** - oletusarvon mukaan näytetään vain ehdotukset, jotka ovat parempia (aiempia) kuin nykyinen myyntirivin päivämäärä. Sisällytä myöhemmät päivämäärät valitsemalla tämä vaihtoehto Tämä vaihtoehto voi olla hyödyllinen, kun muut parametrit kuin päivämäärä ovat tärkeämpiä. Tietty toimittaja tai varasto voi esimerkiksi olla ensisijainen.
-   **Toimitustapa** - Valitse ensisijainen toimitustapa ajan ja kustannusten optimointia varten. Näet välittömästi vaikutuksen toimitusvaihtoehtojen ehdotuksissa. Tämän ansiosta vaihtoehtojen vertailu on helppoa.
-   **Sisällytä hankinta** - Kun hankinta on valittuna, toimitusvaihtoehtojen ehdotuksiin sisällytetään vaihtoehto hankinnasta sekä ulkoisilta toimittajilta että konsernin muilta yrityksiltä (konsernin sisäinen hankinta). **Sisällytä hankinnat** -vaihtoehto on tuettu toimituspäivän ATP- ja ATP + toimitusmarginaalitarkistuksissa. Hankintavaihtoehdot tuotteen oletusostotoimittajasta tuotteen kaikkiin hyväksyttyihin toimittajiin ovat mukana.
-   Ulkoisten toimittajien laskelma perustuu oston läpimenoaikaan.
-   Konsernin sisäisessä hankinnassa laskelma ottaa huomioon lähdeyrityksen saatavuuden kyseisen yrityksen toimituspäivämäärätarkistuksen perusteella.
-   **Toimitustyyppi** (hankintaa varten)
    -   **Varasto** - Tuotteet toimitetaan lähdevarastosta myyntirivillä olevaan sijaintiin/varastoon. Sieltä ne lähetetään edelleen asiakkaalle.
    -   **Suoratoimitus** - Tuotteet toimitetaan lähdevarastolta suoraan asiakkaalle.

### <a name="availability-information"></a>Käytettävyystiedot

Tällä välilehdellä on valittuun toimitusvaihtoehdon riviin liittyviä tietoja. Seuraavat tiedot näytetään myyntirivin toimituspäivämäärän tarkistuksesta riippuen:

-   **Myynnin läpimenoaika**
    -   **Käytettävissä tänään** - Näyttää tämänhetkisen fyysisen käytettävissä olevan, fyysisen varatun ja saatavilla olevan fyysisen varaston.
    -   **Parametrit** - Näytä varaston yksikön ja myynnin läpimenoajat.

-   **ATP ja ATP + toimitusmarginaali**
    -   **Käytettävissä tänään** - Näyttää tämänhetkisen fyysisen käytettävissä olevan, fyysisen varatun ja saatavilla olevan fyysisen varaston.
    -   **Parametrit** - Näytä varaston yksikön ja myynnin läpimenoajat.
    -   **Saatavuus tulevaisuudessa** - Näyttää graafisen esityksen tämänhetkisestä ja tulevaisuuden saatavuudesta valitussa sijainnissa ja varastossa **Toimitusvaihtoehdot**-kohdassa. Saat lisätietoja tuotteen saatavuudesta napsauttamalla kaavion sarakkeita. Liukusäädin esittää luettelon asiaankuuluvista kysyntä- ja toimitustilauksista ATP-aikarajan sisällä.

-   **Saatavuus**
    -   **Käytettävissä tänään** - Näyttää tämänhetkisen fyysisen käytettävissä olevan, fyysisen varatun ja saatavilla olevan fyysisen varaston.
    -   **Parametrit** - Näytä varaston yksikön ja myynnin läpimenoajat.
    -   **Hajotus** – Näytä valitun toimitusvaihtoehdon hajotus. Voit muuttaa hajotusnäkymässä näytettäviä kenttiä ja varastodimensioita **Asetuksissa**.

### <a name="impact-of-selected-alternative"></a>Valitun vaihtoehdon vaikutus

Tässä välilehdessä korostetaan valitun toimitusvaihtoehdon vaikutusta. Jos valitset **OK**, myynnin riville päivitetään VALITUISSA sarakkeissa olevat, korostetut arvot. Huomaa, että, jos valitun toimitusvaihtoehdon määrä on pienempi kuin myyntirivin määrä, luodaan toimitusaikataulu ja tilausrivi jaetaan kahdelle riville: yksi valitulle määrälle ja toinen jäljelle jäävälle määrälle. Voit myös päivittää kaupallisen rivin niin, että se vastaa aikataulurivejä ja vaikuttaa hinnoitteluun.

<a name="see-also"></a>Lisätietoja
--------

[Luvatut tilaukset](delivery-dates-available-promise-calculations.md)





