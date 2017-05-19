---
title: Asiakkaan kirjausprofiilit
description: Asiakkaan kirjausprofiilit ohjaavat asiakastapahtumien kirjausta kirjanpitoon.
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: CustPosting
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 24651
ms.assetid: cb82245e-8c02-429c-b36e-8db0e3e6f7e5
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 3df5d902db8afb3e6347a456f8a2d9d2e2253cb2
ms.contentlocale: fi-fi
ms.lasthandoff: 04/25/2017


---

# <a name="customer-posting-profiles"></a>Asiakkaan kirjausprofiilit

[!include[banner](../includes/banner.md)]


Asiakkaan kirjausprofiilit ohjaavat asiakastapahtumien kirjausta kirjanpitoon.

<a name="customer-posting-profiles"></a>Asiakkaan kirjausprofiilit
-------------------------

Voit määrittää asiakkaan kirjausprofiilin avulla kirjanpitotilejä ja asiakirja-asetuksia kaikille asiakkaille, asiakasryhmällä tai yhdelle asiakkaalle. Näitä asetuksia käytetään, kun luot myyntitilauksia, vapaatekstilaskuja, käteismaksuja, maksukehotuksia ja korkolaskuja. Voit valita joissakin tapahtumissa eri kirjausprofiilin, joka ohittaa tällä sivulla tapahtumille määritetyn kirjausprofiilin. 

Oletuskirjausprofiili määritetään Myyntireskontran parametrit -sivun Kirjanpito ja arvonlisävero -pikavälilehdessä. Oletuskirjausprofiili sisällytetään sitten automaattisesti uusien asiakirjojen otsikkoon, jossa voit vaihtaa tarvittaessa toisen kirjausprofiilin.

Voit liittää tapahtuman kirjaustyyppejä sisältäviä kirjausprofiileja myös Tapahtuman kirjausmääritykset -sivulla. Kirjausmäärityksillä määritetään asiakastapahtumien kirjaus kirjanpitoon kirjausprofiilien sijasta.

## <a name="creating-a-posting-profile"></a>Kirjausprofiilin luonti
Määritä valittua kirjausprofiilia käyttävät tapahtumien kirjaukset, joita käytetään kirjanpitotileillä. Valitse valitulle kirjausprofiilille tilikoodi ja mahdollinen tili- tai ryhmänumero. Kirjauksen aikana jokaiselle tapahtumalle sopivin kirjausprofiilin etsitään hakemalla sopivin tilikoodi-, tilinumero- tai ryhmä- ja numeroyhdistelmää seuraavassa järjestyksessä:

| **Tilikoodi**-kentän arvo | **Tilin/ryhmän numero** -kentän arvo            | Haun prioriteetti |
|------------------------------|-------------------------------------------------|-----------------|
| **Taulu**                    | Määrätty asiakastili                       | 1               |
| **Ryhmä**                    | Asiakkaalle määritetty asiakasryhmä | 2               |
| **Kaikki**                      | Tyhjä                                           | 3               |

Jos haluat määrittää kaikille asiakastapahtumille saman kirjausprofiilin, määritä vain yksi kirjausprofiili Tilikoodi-kentässä arvolla Kaikki. Määritä kirjausprofiili määrittämällä seuraavat arvot:

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
<td>Anna kirjausprofiilin koodi. Voit esimerkiksi luoda kaksi kirjausprofiilia, jotta asiakassaldot saadaan yhdelle tilille kansallisena valuuttana ja toiselle ulkomaan valuuttana. Ensimmäisen tilin nimi voi olla vaikkapa Kansallinen ja toisen Ulkomainen.</td>
</tr>
<tr class="even">
<td><strong>Kuvaus</strong></td>
<td>Anna kirjausprofiilin kuvaus. Tätä käytetään vain helpottamaan kirjausprofiilin tunnistamista, kun sivua tarkastellaan.</td>
</tr>
<tr class="odd">
<td><strong>Tilikoodi</strong></td>
<td>Määritä, koskeeko kirjausprofiili yhtä asiakasta, asiakasryhmää vai kaikki asiakkaita:
<ul>
<li><strong>Taulu</strong> – Kirjausprofiili koskee yksittäistä asiakasta. Valitse asiakastili Tilin/ryhmän numero -kentässä.</li>
<li><strong>Ryhmä</strong> – Kirjausprofiili koskee asiakasryhmää. Valitse asiakasryhmä Tilin/ryhmän numero -kentässä.</li>
<li><strong>Kaikki</strong> – Kirjausprofiili koskee kaikkia asiakkaita. Jätä Tilin/ryhmän numero -kenttä tyhjäksi.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Tilin/ryhmän numero</strong></td>
<td>Jos Taulu on valittu Tilikoodi-kentässä, valitse kirjausprofiiliin liitetyn asiakkaan tilinumero. Jos Ryhmä on valittu, valitse asiakasryhmä. Jos Kaikki on valittu, jätä tämä kenttä tyhjäksi.</td>
</tr>
<tr class="odd">
<td><strong>Reskontratili</strong></td>
<td>Valitse kirjanpitotili, jota käytetään asiakkaan yhteenvetotilinä kirjausprofiiliin liitetyillä asiakkailla.</td>
</tr>
<tr class="even">
<td><strong>Selvitystili</strong></td>
<td>Valitse kassavirtaennusteissa käytettävä maksuvalmiustili. Tämä kentässä näkyy vain, jos kassavirtaennusteet ovat käytössä.</td>
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
<td>Määritä Myyntireskontran parametrit -sivulla kirjausprofiili, jota käytetään, kun maksu on merkitty ennakkomaksuksi.</td>
</tr>
</tbody>
</table>
</div></td>
</tr>
<tr class="even">
<td><strong>Alennustili</strong></td>
<td>Valitse alennusvelkojen kirjanpitotili</td>
</tr>
<tr class="odd">
<td><strong>Maksukehotukset</strong></td>
<td>Valitse maksukehotussarjan tunnus, jota käytetään asiakkaille, joille kirjausprofiili on määritetty.</td>
</tr>
<tr class="even">
<td><strong>Korkoryhmä</strong></td>
<td>Valitse korkokoodi, jolla lasketaan korko asiakkaille, joille kirjausprofiili on määritetty.</td>
</tr>
</tbody>
</table>

### 

### <a name="table-restrictions"></a>**Taulurajoitukset**

Määritä tapahtumille, joilla on valittu kirjausprofiili, tilitetäänkö tapahtumat automaattisesti, lasketaanko korko ja annetaanko maksukehotukset. Voit myös valita tili, jota käytetään, kun valittuun kirjausprofiiliin liittyvät tapahtumat suljetaan.

Määritä kirjausprofiili määrittämällä seuraavat arvot:

| Kenttä                 | Kuvaus                                                                                                                                                                                                                                        |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Tilitys**        | Ota tämän kirjausprofiilin sisältävien tapahtuvien automaattinen tilitys käyttöön valitsemalla tämä asetus. Jos tämä asetus poistetaan käytöstä, tapahtumat on tilitettävä manuaalisesti Tilitä avoimet tapahtumat- tai Lisää asiakkaan maksuja -sivulla. |
| **Kiinnostuksen kohteet**          | Valitse tämä asetus, jos korko on laskettava tätä profiilia käyttävien asiakastilien jäljellä oleville saldoille. Jos tämän asetuksen valinta poistetaan, korkoa ei lasketa näille asiakkaille.                                           |
| **Maksukehotus** | Valitse tämä asetus, jos maksukehotuksen on luotava tätä profiilia käyttäville asiakastileille. Jos tämän asetuksen valinta poistetaan, maksukehotuksia ei luoda näille asiakkaille.                                                 |
| **Sulje**             | Valitse toinen kirjausprofiili, jota siirrytään käyttämään, kun tämän kirjausprofiilin tapahtumia suljetaan. Tapahtuma katsotaan suljetuksi, kun se on selvitetty kokonaan.                                                                           |






