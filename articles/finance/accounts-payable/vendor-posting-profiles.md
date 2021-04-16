---
title: Toimittajan kirjausprofiilit
description: Toimittajan kirjausprofiilit ohjaavat toimittajatapahtumien kirjaamista kirjanpitoon.
author: abruer
ms.date: 06/12/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: VendPosting
audience: Application User
ms.reviewer: roschlom
ms.custom: 24691
ms.assetid: 18def866-7655-4f0b-b299-eec83098d23a
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 37fb7d2623451313475a6c234e820c7c6295be40
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5835481"
---
# <a name="vendor-posting-profiles"></a>Toimittajan kirjausprofiilit

[!include [banner](../includes/banner.md)]

Toimittajan kirjausprofiilit ohjaavat toimittajatapahtumien kirjaamista kirjanpitoon.

<a name="vendor-posting-profiles"></a>Toimittajan kirjausprofiilit
-----------------------

Voit määrittää toimittajan kirjausprofiilin avulla kirjanpitotilejä ja asiakirja-asetuksia kaikille toimittajille, toimittajaryhmälle tai yhdelle toimittajalle. Näitä asetuksia käytetään, kun luot ostotilauksia, toimittajan laskuja ja käteismaksuja. Voit valita joissakin tapahtumissa eri kirjausprofiilin, joka ohittaa tällä sivulla tapahtumille määritetyn kirjausprofiilin. Oletuskirjausprofiili määritetään **Ostoreskontran parametrit** -sivun **Kirjanpito ja arvonlisävero** -pikavälilehdessä. Oletuskirjausprofiili sisällytetään sitten automaattisesti uusien asiakirjojen otsikkoon, jossa voit vaihtaa tarvittaessa toisen kirjausprofiilin.

Voit liittää tapahtuman kirjaustyyppejä sisältäviä kirjausprofiileja myös **Tapahtuman kirjausmääritykset** -sivulla. Kirjausmäärityksillä määritetään toimittajatapahtumien kirjaus kirjanpitoon kirjausprofiilien sijasta.

## <a name="creating-a-posting-profile"></a>Kirjausprofiilin luonti
### <a name="setup"></a>**Asetukset**

Määritä valittua kirjausprofiilia käyttävät tapahtumien kirjaukset, joita käytetään kirjanpitotileillä. Valitse valitulle kirjausprofiilille tilikoodi ja mahdollinen tili- tai ryhmänumero. Kirjauksen aikana jokaiselle tapahtumalle sopivin kirjausprofiilin etsitään hakemalla sopivin tilikoodi-, tilinumero- tai ryhmä- ja numeroyhdistelmää seuraavassa järjestyksessä.

| **Tilikoodi**-kentän arvo | **Tilin/ryhmän numero** -kentän arvo        | Haun prioriteetti |
|------------------------------|---------------------------------------------|-----------------|
| **Taulu**                    | Tietty toimittajatili                     | 1               |
| **Ryhmä**                    | Toimittajaryhmä, johon toimittaja on määritetty | 2               |
| **Kaikki**                      | Tyhjä                                       | 3               |

Jos haluat määrittää kaikille toimittajatapahtumille saman kirjausprofiilin, määritä vain yksi kirjausprofiili **Tilikoodi**-kentässä arvolla **Kaikki**. Määritä kirjausprofiili määrittämällä seuraavat arvot.

<table>
<thead>
<tr class="header">
<th>Kenttä</th>
<th>Kuvaus</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Kirjausprofiili</strong></td>
<td>Anna kirjausprofiilin koodi. Voit esimerkiksi luoda kaksi kirjausprofiilia, jotta toimittajasaldot saadaan yhdelle tilille kansallisena valuuttana ja toiselle ulkomaan valuuttana. Ensimmäisen tilin nimi voi olla vaikkapa Kansallinen ja toisen Ulkomainen.</td>
</tr>
<tr class="even">
<td><strong>Kuvaus</strong></td>
<td>Anna kirjausprofiilin kuvaus.</td>
</tr>
<tr class="odd">
<td><strong>Tilikoodi</strong></td>
<td>Määritä, käytetäänkö kirjausprofiilia tietyn toimittajan, toimittajaryhmän vai kaikkien toimittajien kohdalla:
<ul>
<li><strong>Taulu</strong> – Kirjausprofiili koskee yksittäistä toimittajaa. Valitse toimittajatili <strong>Tilin/ryhmän numero</strong> -kentässä.</li>
<li><strong>Ryhmä</strong> – Kirjausprofiili koskee toimittajaryhmää. Valitse toimittajaryhmä <strong>Tilin/ryhmän numero</strong> -kentässä.</li>
<li><strong>Kaikki</strong> – Kirjausprofiili koskee kaikkia toimittajia. Jätä <strong>Tilin/ryhmän numero</strong> -kenttä tyhjäksi.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Tilin/ryhmän numero</strong></td>
<td>Jos <strong>Taulu</strong> on valittu <strong>Tilikoodi</strong>-kentässä, valitse kirjausprofiiliin liitetyn toimittajan tilinumero. Jos <strong>Ryhmä</strong> valitaan, valitse toimittajaryhmä. Jos <strong>Kaikki</strong> on valittu, jätä tämä kenttä tyhjäksi.</td>
</tr>
<tr class="odd">
<td><strong>Reskontratili</strong></td>
<td>Valitse kirjanpitotili, jota käytetään yhteenvetotilinä kirjausprofiiliin liitetyillä toimittajilla. Tämän päätilin <strong>Älä salli manuaalista määritystä</strong> -parametri merkitään. Jos poistat tämän tilin myöhemmin kirjausprofiilista, tarkista <strong>Älä salli manuaalista määritystä</strong> -asetus <strong>Päätilit</strong>-sivulla. 
<p><strong>Huomautus:</strong>Jos <strong>Kirjanpitoparametrit</strong>-sivulla valitaan <strong>Käytä kirjausmäärityksiä</strong> -asetus, yhteenvetotilin sijaista käytetään toimittajan laskutapahtuman kirjausmääritystä.</p>
</td>
</tr>
<tr class="even">
<td><strong>Selvitystili</strong></td>
<td>Valitse kassavirtaennusteissa käytettävä maksuvalmiustili. Tämä kenttä on käytettävissä vain, kun kassavirtaennusteet on otettu käyttöön.</td>
</tr>
<tr class="odd">
<td><strong>Arvonlisäveron ennakkomaksut</strong></td>
<td>Valitse arvonlisäveron tili etuajassa saatuja maksuja varten.
<p><strong>Huomautus:</strong> <strong>Kirjaus</strong>-profiili, jota käytetään, kun maksu merkitään ennakkomaksuksi, valitaan <strong>Ostoreskontran parametrit</strong> -sivun <strong>Kirjanpito ja arvonlisävero</strong> -alueen <strong>Ennakkomaksukirjauskansion kirjausprofiili</strong> -kentässä.</p>
</td>
</tr>
<tr class="even">
<td><strong>Saapuminen</strong></td>
<td>Valitse se kirjanpitotili, jolle hyväksymistä odottavien toimittajan laskujen tiedot kirjataan. Tiedot tallennetaan laskurekisterikirjauskansioon. Oletetaan esimerkiksi, että käyttäjä tallentaa toimittajan laskujen perustiedot laskurekisteriin, kun laskut vastaanotetaan. Kun laskurekisteri kirjataan, tapahtumat kirjataan tässä ja <strong>Vastatili</strong>-kentässä annetulle tilille. Kun laskut hyväksytään, velka siirretään saapumistililtä toimittajan reskontratilille.</td>
</tr>
<tr class="odd">
<td><strong>Vastatili</strong></td>
<td>Valitse se kirjanpitotili, jota käytetään hyväksymistä odottavien, laskurekisterin kautta päivitettävien toimittajan laskujen vastakirjauksiin. Vastatili toimii saapumistileille kirjattujen tapahtumien vastatilinä. Niinpä tili sisältääkin ostot toimittajilta, joita ei ole vielä hyväksytty.</td>
</tr>
</tbody>
</table>


### <a name="table-restrictions"></a>**Taulurajoitukset**

Määritä tapahtumille, joilla on valittu kirjausprofiili, tilitetäänkö tapahtumat automaattisesti, lasketaanko korko ja annetaanko maksukehotukset. Voit myös valita tili, jota käytetään, kun valittuun kirjausprofiiliin liittyvät tapahtumat suljetaan.

Määritä kirjausprofiili määrittämällä seuraavat arvot

| Kenttä          | Kuvaus                                                                                                                                                                                                    |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Tilitys** | Ota tämän kirjausprofiilin sisältävien tapahtumien automaattinen tilitys käyttöön valitsemalla tämä asetus. Jos tämä asetus poistetaan käytöstä, tapahtumat on tilitettävä manuaalisesti **Tilitä avoimet tapahtumat** -sivulla. |
| **Peruuta**     | Valitse tämä asetus, jos haluat mahdollisuuden tämän kirjausprofiilin sisältävien tapahtumien peruuttamiseen.                                                                                                               |
| **Sulje**      | Valitse toinen kirjausprofiili, jota siirrytään käyttämään, kun tämän kirjausprofiilin tapahtumia suljetaan. Tapahtuma katsotaan suljetuksi, kun se on selvitetty kokonaan.                                       |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]