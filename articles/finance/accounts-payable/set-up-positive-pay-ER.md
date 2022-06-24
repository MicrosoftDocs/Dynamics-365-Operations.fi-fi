---
title: Sähköisten raportointien avulla voit määrittää ja luoda positiivisia maksutiedostoja
description: Tässä artikkelissa käsitellään Positive pay -toiminnon määrittämistä käyttämällä elektronista raportointia.
author: panolte
ms.date: 03/20/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankPositivePayFormat
audience: Application User
ms.reviewer: twheeloc
ms.custom: 88433
ms.assetid: 73f3dcf6-040a-44ad-9512-7b3e0d17a571
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 491048c7274ba6bb52e0a4b7a6ea5cd0f5ff4741
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8878215"
---
# <a name="set-up-positive-pay-files-by-using-electronic-reporting"></a>Sähköisten raportointien avulla voit määrittää positiivisia maksutiedostoja

Tässä artikkelissa käsitellään Positive pay -toiminnon määrittämistä ja Positive pay -tiedostojen luomista sähköisen raportoinnin avulla.

> [!NOTE] 
> Ennen kuin käytät **Luo pankin Positive pay -tiedosto** -toimintoa, sinun on päivitettävä yksikköluettelo.
> Siirry **Tietojen hallinta > Tuonti / Vienti > Kehikkoparametrit** 
> **Yksikön asetukset** -pikavälilehti ja valitse **Päivitä yksikköluettelo**.


Määritä positiivinen maksu sähköisen luettelon luomiseksi pankille toimitettavista sekeistä. Kun sekki esitetään pankille, pankki vertaa sitä aiemmin lähetettyyn sekkiluetteloon. Jos sekki on sama kuin luettelossa, pankki selvittää sekin. Jos sekki ei vastaa luettelon sekkiä, pankki säilyttää sekin tarkistusta varten.

## <a name="security-for-positive-pay-files"></a>Positive pay -tiedostojen suojaus
Positiiviset maksutiedostot voivat sisältää luottamuksellisia tietoja maksun saajista ja sekkisummista. Varmista tämän vuoksi, että käytät riittäviä suojaustoimenpiteitä tiedostojen luontihetkestä pankin vastaanottoon asti. Positive pay -tiedostot ladataan selaimen määrittämään paikkaan. Positive pay -tiedostot saattavat sisältää henkilökohtaisia tietoja, joten on tärkeää, että vain valtuutetut käyttäjät voivat luoda ja tarkastella tietoja Microsoft Dynamics 365 Financessa. Käytä tarvittavien oikeuksien määrittämisessä apuna seuraavaa taulukkoa.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Tehtävä</th>
<th>Käyttöoikeus</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Luo Positive pay -tiedostoja <strong>Pankkitilit</strong>-luettelosivulla tai <strong>Pankkitilit</strong>-sivulla.</td>
<td><ul>
<li><strong>Ylläpidä pankin Positive pay -tietoja</strong> (BankPositivePayProcess)</li>
<li><strong>BankPositivePayExportEntityView</strong> (BankPositivePayExportEntityView)</li>
</ul></td>
</tr>
<tr class="even">
<td>Luo Positive pay -tiedostoja useille yrityksille ja pankkitileille <strong>Luo Positive pay -tiedosto</strong> -sivulla.</td>
<td><ul>
<li><strong>Ylläpidä pankin Positive pay -tietoja</strong> (BankPositivePayProcess)</li>
<li><strong>BankPositivePayExportEntityView</strong> (BankPositivePayExportEntityView)</li>
</ul></td>
</tr>
<tr class="odd">
<td>Tarkastele Positive pay -tiedostoja <strong>Positive pay -tiedoston yhteenveto</strong> -sivulla.</td>
<td><strong>Näytä pankin Positive pay -tiedot useita yrityksiä varten</strong> (BankPositivePayView)</td>
</tr>
<tr class="even">
<td>Vahvista pankin Positive pay -tiedosto <strong>Positive pay -tiedoston yhteenveto</strong> -sivulla.</td>
<td><strong>Vahvista Positive payment -tiedosto</strong> (BankPositivePayConfirm)</td>
</tr>
<tr class="odd">
<td>Peruuta pankin Positive pay -tiedosto <strong>Positive pay -tiedoston yhteenveto</strong> -sivulla.</td>
<td><strong>Peruuta Positive pay -tiedosto</strong> (BankPositivePayRecall)</td>
</tr>
</tbody>
</table>

## <a name="set-up-the-electronic-reporting-configuration"></a>Määritä sähköisen raportoinnin konfiguraatio

1. Valitse **Työtilat \> Sähköinen raportointi**.
2. Valitse **Microsoft**-määrityspalveluntarjoajan ruudusta **Arkistot**.
3. Valitse **Yleinen** ja valitse sitten **Avaa**.
4. Jos tietovarastoon on oltava yhteys, valitse sininen linkki valintaikkunasta.
5. Etsi ja valitse konfigurointiluettelosta **Positiivisen maksumallin \> positiivinen maksumuoto**.
6. Valitse **Versiot**-pikavälilehdellä valitun uusin versio ja valitse sitten **Tuo**.

## <a name="set-up-a-positive-pay-format"></a>Positive pay -muodon määrittäminen

1. Valitse **Maksuliikenteen hallinta \> Asetukset \> Positiiviset maksumuodot**.
2. Valitse **Uusi**.
3. Määritä **Maksun muoto**- ja **Kuvaus**-kentät.
4. Valitse **Yleinen sähköinen vientimuoto** -valintaruutu.
5. Aseta **Vientimuodon määritys** -kentän arvoksi **Positiivinen maksumuoto**.

## <a name="assign-a-positive-pay-format-to-a-bank-account"></a>Positive pay -muodon määrittäminen pankkitileille
Jokaiselle pankkitilille, jolle haluat luoda Positive pay -tiedot, on määritettävä edellisessä toimenpiteessä määritetty Positive pay -muoto. Valitse Pankkitilit-sivulla Positive pay -muoto, joka vastaa pankkitiliä. Lisää **Positive pay -aloituspäivä** -kenttään ensimmäinen päivämäärä, jona Positive pay -tiedostot luodaan. 

>[!Important]
> Syötä **Positiivisen maksun aloituspäivä** -kenttään päivämäärä. Jos kenttä jätetään tyhjäksi, ensimmäinen luotu Positive pay -tiedosto sisältää kaikki pankkitilille luodut sekit.

1. Valitse **Maksuliikenteen hallinta \> Pankin tilit \> Pankkitilit**.
2. Avaa pankkitili.
3. Määritä **Yleinen**-pikavälilehdessä **Positiivisen maksun muoto** -kentän arvoksi aiemmin luotu muoto.
4. Määritä **Positiivisen maksun aloituspäivä** -kenttään nykyinen päivämäärä.

## <a name="assign-a-number-sequence-for-positive-pay-files"></a>Numerojärjestyksen määrittäminen Positive pay -tiedostoille
Jokaisella positive pay -tiedostolla on oltava yksilöivä numero. Luo numerojärjestys Positive pay -tiedostoille **Maksuliikennetiedot**-sivun **Numerojärjestykset**-välilehdessä.

## <a name="generate-a-positive-pay-file-for-a-single-bank-account"></a>Positive pay -tiedoston luominen yksittäiselle pankkitilille
Voit luoda Positive pay -tiedoston yksittäiselle yritykselle ja pankkitilille. Seuraavassa osassa on tietoja Positive pay -tiedostojen luomisesta useille yrityksille ja pankkitileille samalla kertaa. Jos haluat luoda Positive pay -tiedoston yksittäiselle yritykselle ja yksittäiselle pankkitilille, avaa **Luo Positive pay -tiedosto** -valintaikkuna **Pankkitilit**-sivulta. Kirjoita **Katkaisupäivämäärä**-kenttään viimeinen sekin päivämäärä, joka otetaan mukaan Positive pay -tiedostoon. Tiedosto sisältää kaikki sekit, joita ei ole sisällytetty Positive pay -tiedostoon sekin päivämäärään saakka.

1. Valitse **Maksuliikenteen hallinta \> Pankkitilit \> Pankkitilit**.
2. Avaa pankkitili, jonka positiivinen maksu on määritetty.
3. Valitse **Hallitse maksuja \> Positiivinen maksu \> Positiivinen maksutiedosto**.
4. Määritä **Määräpäivämäärä**-kenttä. Ennen tätä päivämäärää luodut sekit sisällytetään raporttiin.

## <a name="generate-a-positive-pay-file-for-multiple-bank-accounts"></a>Positive pay -tiedoston luominen useille pankkitileille
Luo Positive pay -tiedostoja useille yrityksille ja pankkitileille kausittaisen **Positive pay -tiedosto** -tehtävän avulla. Valitse tiedostolle Positive pay -muoto ja määritä, luodaanko tiedosto kaikille yrityksille vai vain valitulle yritykselle. Voit myös luoda Positive pay -tiedoston kaikille pankkitileille, joissa käytetään määritettyä Positive pay -muotoa,tai vain valitulle pankkitilille. Kirjoita **Katkaisupäivämäärä**-kenttään viimeinen sekin päivämäärä, joka otetaan mukaan Positive pay -tiedostoon. Tiedosto sisältää kaikki sekit, joita ei ole sisällytetty Positive pay -tiedostoon sekin päivämäärään saakka.

## <a name="view-the-results-of-positive-pay-file-generation"></a>Positive pay -tiedoston luonnin tulosten tarkastelu
Kun Positive pay -tiedosto on luotu, voit tarkastella tuloksia **Positive pay -tiedoston yhteenveto** -sivulla. Jos haluat tarkastella yksittäisten sekkien tietoja, siirry **Positive pay -tiedoston tiedot** -sivulle.

## <a name="confirm-a-positive-pay-file"></a>Vahvista Positive pay -tiedosto
Kun positive pay -tiedostossa listatut sekit on maksettu, saat pankiltasi vahvistusnumeron. Tämän jälkeen voit vahvistaa Positive pay -tiedoston. Valitse **Positive pay -tiedoston yhteenveto** -sivulla Positive pay -tiedosto, jonka tila on **Luotu**, ja valitse sitten **Anna vahvistus** -toiminto. Kun vahvistat Positive pay -tiedoston, pankilta saamasi vahvistusnumero tallennetaan.

## <a name="recall-a-positive-pay-file"></a>Peruuta Positive pay -tiedosto
Jos haluat muuttaa Positive pay -tiedosto, voit kutsua sen takaisin. Valitse **Positive pay -tiedoston yhteenveto** -sivulla Positive pay -tiedosto, jonka tila on **Luotu**, ja valitse sitten **Peruuta**-toiminto. Jokaisen Positive pay -tiedostossa olevan sekin kenttä ilmaisee, onko Positive pay -tiedostoon sisältyvä sekki peruutettu. Tämän jälkeen voit luoda uuden Positive pay -tiedoston, joka sisältää peruutetun sekin.


Tuloksena saatava XML-tiedosto ladataan.
