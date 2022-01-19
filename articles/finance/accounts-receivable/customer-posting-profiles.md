---
title: Asiakkaan kirjausprofiilit
description: Tässä aiheessa kuvataan asiakkaan kirjausprofiileita, joiden avulla määritetään asiakastapahtumien kirjaus kirjanpitoon.
author: JodiChristiansen
ms.date: 12/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustPosting, CustVendExternalItem
audience: Application User
ms.reviewer: roschlom
ms.custom: 24651
ms.assetid: cb82245e-8c02-429c-b36e-8db0e3e6f7e5
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 91432a401a8f8a499e9f5e2bbe7157408faac822
ms.sourcegitcommit: f5fd2122a889b04e14f18184aabd37f4bfb42974
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/10/2022
ms.locfileid: "7952568"
---
# <a name="customer-posting-profiles"></a>Asiakkaan kirjausprofiilit

[!include [banner](../includes/banner.md)]

Tässä aiheessa kuvataan asiakkaan kirjausprofiileita, joiden avulla määritetään asiakastapahtumien kirjaus kirjanpitoon.

## <a name="customer-posting-profiles"></a>Asiakkaan kirjausprofiilit

Voit määrittää asiakkaan kirjausprofiilin avulla kirjanpitotilejä ja asiakirja-asetuksia kaikille asiakkaille, asiakasryhmällä tai yhdelle asiakkaalle. Näitä asetuksia käytetään, kun luot myyntitilauslaskuja, vapaatekstilaskuja, projektilaskuja, maksukirjauskansioita, maksukehotuksia ja korkolaskuja. 

Oletuskirjausprofiili määritetään **Myyntireskontran parametrit** -sivun **Kirjanpito ja arvonlisävero** -välilehdessä. Se sisällytetään tällöin automaattisesti uusien tiedostojen otsikkoon. Voit muuttaa sitä siinä, jos eri kirjausprofiilia edellytetään. 

Jos organisaatiot hyväksyvät asiakkaiden ennakkomaksuja, ne konfiguroivat usein ennakkomaksuille toisen kirjausprofiilin ja linkittävät sen parametreissa ennakkomaksujen oletuskirjausprofiilina. Lisätietoja on kohdassa [Asiakkaan ennakkomaksut](customer-prepayments.md).

Voit liittää tapahtuman kirjaustyyppejä sisältäviä kirjausprofiileja myös **Tapahtuman kirjausmääritykset** -sivulla. Kirjausmäärityksillä määritetään asiakastapahtumien kirjaus kirjanpitoon kirjausprofiilien sijasta. Lisätietoja: [Kirjausmääritykset](../general-ledger/posting-definitions.md).

## <a name="creating-a-posting-profile"></a>Kirjausprofiilin luonti
Määritä valittua kirjausprofiilia käyttävät tapahtumien kirjaukset, joita käytetään kirjanpitotileillä. Valitse valitulle kirjausprofiilille tilikoodi ja mahdollinen tili- tai ryhmänumero. Kirjauksen aikana jokaiselle tapahtumalle sopivin kirjausprofiilin etsitään hakemalla sopivin tilikoodi-, tilinumero- tai ryhmä- ja numeroyhdistelmää seuraavassa järjestyksessä:

| Tilikoodi-kentän arvo | Tilin/ryhmän numero -kentän arvo                | Haun prioriteetti |
|--------------------------|-------------------------------------------------|-----------------|
| Taulukko                    | Määrätty asiakastili                       | 1               |
| Ryhmä                    | Asiakkaalle määritetty asiakasryhmä | 2               |
| Kaikki                      | Tyhjä                                           | 3               |

Jos haluat määrittää kaikille asiakastapahtumille saman kirjausprofiilin, määritä vain yksi kirjausprofiili, jossa **Tilikoodi**-kentässä on arvo **Kaikki**. Määritä kirjausprofiili määrittämällä seuraavat arvot.

<table>
<thead>
<tr>
<th>Kenttä</th>
<th>Kuvaus</th>
</tr>
</thead>
<tbody>
<tr>
<td>Kirjausprofiili</td>
<td>Anna kirjausprofiilin koodi. Voit esimerkiksi luoda kaksi kirjausprofiilia, jotta asiakassaldot saadaan yhdelle tilille kansallisena valuuttana ja toiselle ulkomaan valuuttana. Ensimmäisen tilin nimi voi olla vaikkapa Kansallinen ja toisen Ulkomainen.</td>
</tr>
<tr>
<td>Kuvaus</td>
<td>Anna kirjausprofiilin kuvaus. Tätä käytetään vain helpottamaan kirjausprofiilin tunnistamista, kun sivua tarkastellaan.</td>
</tr>
<tr>
<td>Tilikoodi</td>
<td>Määritä, koskeeko kirjausprofiili yhtä asiakasta, asiakasryhmää vai kaikki asiakkaita:
<ul>
<li><b>Taulu</b> – Kirjausprofiili koskee yksittäistä asiakasta. Valitse asiakastili <b>Tilin/ryhmän numero</b> -kentässä.</li>
<li><b>Ryhmä</b> – Kirjausprofiili koskee asiakasryhmää. Valitse asiakasryhmä <b>Tilin/ryhmän numero</b> -kentässä.</li>
<li><b>Kaikki</b> – Kirjausprofiili koskee kaikkia asiakkaita. Jätä <b>Tilin/ryhmän numero</b> -kenttä tyhjäksi.</li>
</ul>
</td>
</tr>
<tr>
<td>Tilin/ryhmän numero</td>
<td>Jos <b>Taulu</b> on valittu <b>Tilikoodi</b>-kentässä, valitse kirjausprofiiliin liitetyn asiakkaan tilinumero. Jos <b>Ryhmä</b> on valittu, valitse asiakasryhmä. Jos <b>Kaikki</b> on valittu, jätä tämä kenttä tyhjäksi.</td>
</tr>
<tr>
<td>Reskontratili</td>
<td>Valitse päätili, jota käytetään myyntireskontran kauppatilinä kirjausprofiiliin liitetyillä asiakkailla. Tämä tili on <b>Asiakkaan saldo</b> -kirjaustyypin tili.</td>
</tr>
<tr>
<td>Maksujen rahatili</td>
<td>Valitse kassavirtaennusteissa käytettävä maksuvalmiustili. Tämä kenttä näkyy vain, jos kassavirtaennusteet ovat käytössä.</td>
</tr>
<tr>
<td>Arvonlisäveron ennakkomaksut</td>
<td><p>Valitse arvonlisäveron tili etuajassa saatuja maksuja varten.</p>
<p><strong>Huomautus:</strong> Määritä <b>Myyntireskontran parametrit</b> -sivulla kirjausprofiili, jota käytetään, kun maksu on merkitty ennakkomaksuksi.</p>
</td>
</tr>
<tr>
<td>Alennustili</td>
<td>Valitse alennusvelkojen kirjanpitotili</td>
</tr>
<tr>
<td>Maksukehotukset</td>
<td>Valitse maksukehotussarjan tunnus, jota käytetään asiakkaille, joille kirjausprofiili on määritetty.</td>
</tr>
<tr>
<td>Korkoryhmä</td>
<td>Valitse korkokoodi, jolla lasketaan korko asiakkaille, joille kirjausprofiili on määritetty.</td>
</tr>
</tbody>
</table>

## <a name="posting-examples"></a>Kirjausesimerkkejä

Seuraavassa taulukossa on esimerkkejä oletuskirjaustyypeistä sekä esimerkkejä päätileistä ja kuvauksista. **Debet/kredit**-sarake osoittaa, onko tapahtuma tavallisesti debet vai kredit tai joissakin tapauksissa voi kirjata jommankumman. **Selvitystili**-sarake ilmaisee, että kirjaustyyppi on selvitystili. Tämä tarkoittaa, että tälle tilille kirjattu summa palautetaan automaattisesti, kun myöhempi tapahtuma kirjataan. 

| Kirjaustyyppi | Päätiliesimerkki. | Päätilin nimen esimerkki | Tilityyppi | Veloitus/hyvitys | Selvitystili | Kuvaus |
|--------------|----------------------|---------------------------|--------------|--------------|------------------|-------------|
| Asiakkaan saldo | 130100 | Myyntireskontran kauppa | Resurssi | Molemmat | Ei | Määritä **Yhteenvetotili**-kenttään tili.|
| Ei mikään | 110110 | Pankkitili | Resurssi | Molemmat | Ei | Määritä **Rahatili maksuja varten** -kentässä päätili. Tätä tiliä ei käytetä kirjaamiseen. Sitä käytetään vain kassavirtaennusteissa. |
| Arvonlisäveron ennakkomaksut | 202900 | Arvonlisäveron selvitys | Velat | Molemmat | Kyllä | Valitse arvonlisäveron tili etuajassa saatuja maksuja varten. |
| Alennustili | 250600 | Lykätyt tuotot ja alennukset | Velat | Molemmat | Kyllä | Valitse alennusvelkojen kirjanpitotili.|     

### <a name="table-restrictions"></a>Taulurajoitukset

Määritä tapahtumille, joilla on valittu kirjausprofiili, tilitetäänkö tapahtumat automaattisesti, lasketaanko korko ja annetaanko maksukehotukset. Voit myös valita tili, jota käytetään, kun valittuun kirjausprofiiliin liittyvät tapahtumat suljetaan.

Määritä kirjausprofiili määrittämällä seuraavat arvot:

| Kenttä                 | Kuvaus                                           |
|-----------------------|-------------------------------------------------------|
| Tilitys        | Ota tämän kirjausprofiilin sisältävien tapahtuvien automaattinen tilitys käyttöön valitsemalla tämä asetus. Jos tämä asetus poistetaan käytöstä, tapahtumat on tilitettävä manuaalisesti **Tilitä avoimet tapahtumat**- tai **Lisää asiakkaan maksuja** -sivulla. |
| Kiinnostuksen kohteet          | Valitse tämä asetus, jos korko on laskettava tätä profiilia käyttävien asiakastilien jäljellä oleville saldoille. Jos tämän asetuksen valinta poistetaan, korkoa ei lasketa näille asiakkaille.                                           |
| Maksukehotus | Valitse tämä asetus, jos maksukehotuksen on luotava tätä profiilia käyttäville asiakastileille. Jos tämän asetuksen valinta poistetaan, maksukehotuksia ei luoda näille asiakkaille.                                                 |
| Sulje             | Valitse toinen kirjausprofiili, jota siirrytään käyttämään, kun tämän kirjausprofiilin tapahtumia suljetaan. Tapahtuma katsotaan suljetuksi, kun se on selvitetty kokonaan.             |



Lisätietoja on ohjeaiheessa [Asiakkaan maksujen yleiskatsaus](../cash-bank-management/tasks/customer-payment-overview.md).



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
