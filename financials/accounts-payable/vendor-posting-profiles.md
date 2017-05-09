---
title: Toimittajan kirjausprofiilit
description: Toimittajan kirjausprofiilit ohjaavat toimittajatapahtumien kirjaamista kirjanpitoon.
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: VendPosting
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 24691
ms.assetid: 18def866-7655-4f0b-b299-eec83098d23a
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 926ee087a0e0c4743f29315b1d82c7d37e95be28
ms.openlocfilehash: 76defe4dcb187ca948344ab9131eae981cbace3f
ms.lasthandoff: 03/31/2017


---

# <a name="vendor-posting-profiles"></a>Toimittajan kirjausprofiilit

[!include[banner](../includes/banner.md)]


Toimittajan kirjausprofiilit ohjaavat toimittajatapahtumien kirjaamista kirjanpitoon.

<a name="vendor-posting-profiles"></a>Toimittajan kirjausprofiilit
-----------------------

Voit määrittää toimittajan kirjausprofiilin avulla kirjanpitotilejä ja asiakirja-asetuksia kaikille toimittajille, toimittajaryhmälle tai yhdelle toimittajalle. Näitä asetuksia käytetään, kun luot ostotilauksia, toimittajan laskuja ja käteismaksuja. Voit valita joissakin tapahtumissa eri kirjausprofiilin, joka ohittaa tällä sivulla tapahtumille määritetyn kirjausprofiilin. Oletuskirjausprofiili määritetään Ostoreskontran parametrit -sivun Kirjanpito ja arvonlisävero -pikavälilehdessä. Oletuskirjausprofiili sisällytetään sitten automaattisesti uusien asiakirjojen otsikkoon, jossa voit vaihtaa tarvittaessa toisen kirjausprofiilin.

Voit liittää tapahtuman kirjaustyyppejä sisältäviä kirjausprofiileja myös Tapahtuman kirjausmääritykset -sivulla. Kirjausmäärityksillä määritetään toimittajatapahtumien kirjaus kirjanpitoon kirjausprofiilien sijasta.

## <a name="creating-a-posting-profile"></a>Kirjausprofiilin luonti
### <a name="setup"></a>**Asetukset**

Määritä valittua kirjausprofiilia käyttävät tapahtumien kirjaukset, joita käytetään kirjanpitotileillä. Valitse valitulle kirjausprofiilille tilikoodi ja mahdollinen tili- tai ryhmänumero. Kirjauksen aikana jokaiselle tapahtumalle sopivin kirjausprofiilin etsitään hakemalla sopivin tilikoodi-, tilinumero- tai ryhmä- ja numeroyhdistelmää seuraavassa järjestyksessä:

| **Tilikoodi**-kentän arvo | **Tilin/ryhmän numero** -kentän arvo        | Haun prioriteetti |
|------------------------------|---------------------------------------------|-----------------|
| **Taulu**                    | Tietty toimittajatili                     | 1               |
| **Ryhmä**                    | toimittajaryhmä, johon toimittaja on määritetty | 2               |
| **Kaikki**                      | Tyhjä                                       | 3               |

Jos haluat määrittää kaikille toimittajatapahtumille saman kirjausprofiilin, määritä vain yksi kirjausprofiili Tilikoodi-kentässä arvolla Kaikki. Määritä kirjausprofiili määrittämällä seuraavat arvot:

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
<li><strong>Taulu</strong> – Kirjausprofiili koskee yksittäistä toimittajaa. Valitse toimittajatili Tilin/ryhmän numero -kentässä.</li>
<li><strong>Ryhmä</strong> – Kirjausprofiili koskee toimittajaryhmää. Valitse toimittajaryhmä Tilin/ryhmän numero -kentässä.</li>
<li><strong>Kaikki</strong> – Kirjausprofiili koskee kaikkia toimittajia. Jätä Tilin/ryhmän numero -kenttä tyhjäksi.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Tilin/ryhmän numero</strong></td>
<td>Jos Taulu on valittu Tilikoodi-kentässä, valitse kirjausprofiiliin liitetyn toimittajan tilinumero. Jos Ryhmä valitaan, valitse toimittajaryhmä. Jos Kaikki on valittu, jätä tämä kenttä tyhjäksi.</td>
</tr>
<tr class="odd">
<td><strong>Reskontratili</strong></td>
<td>Valitse kirjanpitotili, jota käytetään yhteenvetotilinä kirjausprofiiliin liitetyillä toimittajilla.
<div class="alert">
<table>
<thead>
<tr class="header">
<th><img src="https://i-technet.sec.s-msft.com/areas/global/content/clear.gif" title="Note" alt="Note" id="alert_note" class="cl_IC101471" /><strong>Huomautus</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Jos Kirjanpitoparametrit-sivulla valitaan Käytä kirjausmäärityksiä -asetus, yhteenvetotilin sijaista käytetään toimittajan laskutapahtuman kirjausmääritystä.</td>
</tr>
</tbody>
</table>
</div></td>
</tr>
<tr class="even">
<td><strong>Selvitystili</strong></td>
<td>Valitse kassavirtaennusteissa käytettävä maksuvalmiustili. Tämä kenttä on käytettävissä vain, kun kassavirtaennusteet on otettu käyttöön.</td>
</tr>
<tr class="odd">
<td><strong>Arvonlisäveron ennakkomaksut</strong></td>
<td>Valitse arvonlisäveron tili etuajassa saatuja maksuja varten.
<div class="alert">
<table>
<thead>
<tr class="header">
<th><img src="https://i-technet.sec.s-msft.com/areas/global/content/clear.gif" title="Note" alt="Note" id="alert_note" class="cl_IC101471" /><strong>Huomautus</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Kirjausprofiili, jota käytetään, kun maksu merkitään ennakkomaksuksi, valitaan Ostoreskontran parametrit -sivun Kirjanpito ja arvonlisävero -alueen Ennakkomaksukirjauskansion kirjausprofiili -kentässä.</td>
</tr>
</tbody>
</table>
</div></td>
</tr>
<tr class="even">
<td><strong>Saapuminen</strong></td>
<td>Valitse se kirjanpitotili, jolle hyväksymistä odottavien toimittajan laskujen tiedot kirjataan. Tiedot tallennetaan laskurekisterikirjauskansioon. Oletetaan esimerkiksi, että käyttäjä tallentaa toimittajan laskujen perustiedot laskurekisteriin, kun laskut vastaanotetaan. Kun laskurekisteri kirjataan, tapahtumat kirjataan tässä ja Vastatili-kentässä annetulle tilille. Kun laskut hyväksytään, velka siirretään saapumistililtä toimittajan reskontratilille.</td>
</tr>
<tr class="odd">
<td><strong>Vastatili</strong></td>
<td>Valitse se kirjanpitotili, jota käytetään hyväksymistä odottavien, laskurekisterin kautta päivitettävien toimittajan laskujen vastakirjauksiin. Vastatili toimii saapumistileille kirjattujen tapahtumien vastatilinä. Niinpä tili sisältääkin ostot toimittajilta, joita ei ole vielä hyväksytty.</td>
</tr>
</tbody>
</table>
 

### <a name="table-restrictions"></a>**Taulurajoitukset**

Määritä tapahtumille, joilla on valittu kirjausprofiili, tilitetäänkö tapahtumat automaattisesti, lasketaanko korko ja annetaanko maksukehotukset. Voit myös valita tili, jota käytetään, kun valittuun kirjausprofiiliin liittyvät tapahtumat suljetaan.

Määritä kirjausprofiili määrittämällä seuraavat arvot:

| Kenttä          | Kuvaus                                                                                                                                                                                                    |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Tilitys** | Ota tämän kirjausprofiilin sisältävien tapahtumien automaattinen tilitys käyttöön valitsemalla tämä asetus. Jos tämä asetus poistetaan käytöstä, tapahtumat on tilitettävä manuaalisesti Tilitä avoimet tapahtumat -sivulla. |
| **Peruuta**     | Valitse tämä asetus, jos haluat mahdollisuuden tämän kirjausprofiilin sisältävien tapahtumien peruuttamiseen.                                                                                                               |
| **Sulje**      | Valitse toinen kirjausprofiili, jota siirrytään käyttämään, kun tämän kirjausprofiilin tapahtumia suljetaan. Tapahtuma katsotaan suljetuksi, kun se on selvitetty kokonaan.                                       |






