---
title: ALV-/GST-mallin käänteinen veloitusmekanismi
description: Tässä ohjeaiheessa kerrotaan, miten käänteinen arvonlisävero määritetään Euroopan maissa, Saudi-Arabiassa ja Singaporessa.
author: epodkolz
manager: AnnBe
ms.date: 10/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Saudi Arabia, Spain, Sweden, United Kingdom, Singapore, Bahrain, Kuwait, Oman, Qatar
ms.author: epodkolz
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 007fab0594c443a3060d6b6640b032ec270f5298
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5236244"
---
# <a name="reverse-charge-mechanism-for-vatgst-scheme"></a>ALV-/GST-mallin käänteinen veloitusmekanismi

[!include [banner](../includes/banner.md)]

Tässä aiheessa kuvataan yleinen tapa määrittää käänteisen veloituksen toiminto maissa/alueilla, jotka käyttävät ALV-tai GST-malleja.
                                                                                 
Toiminnon saatavuutta maassa/alueella hallitaan seuraavilla **Ominaisuuksien hallinta** -työtilan ominaisuuksilla.

| Ominaisuus                                              | Maa tai alue                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Ei   erityistä ominaisuutta                                | Itävalta </br>Belgia </br>Bulgaria </br>Kroatia </br>Kypros </br>Tšekin tasavalta </br>Tanska  </br>Viro  </br>Suomi  </br>Ranska  </br>Saksa  </br>Unkari  </br>Islanti  </br>Irlanti  </br>Italia  </br>Latvia  </br>Liechtenstein  </br>Liettua  </br>Luxemburg  </br>Alankomaat  </br>Norja Puola </br>Portugali </br>Romania  </br>Saudi-Arabia </br>Singapore  </br>Slovakia  </br>Slovenia  </br>Espanja  </br>Ruotsi  </br>Sveitsi  </br>Iso-Britannia  </br>Yhdistyneet arabiemiirikunnat |
| Muiden maiden käänteinen   veloitus            | Bahrain  </br>Kuwait  </br>Oman  </br>Qatar                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Ota ALV/GST-veromallin käänteisen verovelvollisuuden mekanismi   käyttöön | Kaikki muut maat/alueet   lukuun ottamatta seuraavia:  </br>Brasilia  </br>Intia  </br>Venäjä                                                                                                                                                                                                                                                                                                                                                                                         |
 
 Lisätietoja on tämän aiheen kohdassa [ALV-/GST-malliominaisuuden käänteisen veloitusmekanismin ottaminen käyttöön](#enable-reverse-charge).

Käänteinen vero on veromalli, jossa ALV:n kirjanpito- ja raportointivastuu siirtyy myyjältä tavaran ja/tai palvelun ostajalle. Tämän vuoksi tavaroiden ja/tai palvelujen vastaanottaja ilmoitta ALV-ilmoituksessa sekä maksettavan veron (myyjän roolissa) että vähennettävän veron (ostajan roolissa)

Joissakin maissa tai joillakin alueilla käänteinen veromalli koskee vain joitakin tavaroita ja/tai palveluja. Lisäksi myyntisummiin liittyy lisäehtoja tai rajoja. Toisissa maissa tai toisilla alueilla arvolisäveron maksuvelvollisuus määräytyy toimittajan ja ostajan tilan mukaan. Jos ostaja on ALV-verovelvollinen, se on ilmaistava selkeästi toimittajan kirjoittamassa laskussa. Laskussa on esimerkiksi oltava samat "käänteinen vero" ja siinä on ilmaistava, mitä kohtia käänteiseen veromalli koskee. 

Seuraavat asetukset on tehtävä käänteisen veron käyttöä varten.

## <a name="set-up-sales-tax-codes"></a>Määritä arvonlisäverokoodit
Osto- ja myyntitoimintoihin kannattaa käyttää erillisiä arvonlisäverokoodeja.

<table>
<body>
<tr>
<td><strong>Myynnin arvonlisäverokoodi</strong></td>
<td>Luo myyntikoodi käänteisen veron myyntitoiminnoille (<strong>Verot</strong> &gt; <strong>Välilliset verot</strong> &gt; <strong>Arvonlisävero</strong> &gt; <strong>Arvonlisäverokoodit</strong>).
</td>
</tr>
<tr>
<td><strong>Ostojen arvonlisäverokoodi</strong></td>
<td><p>Luo ostojen käänteinen verovelvollisuus positiivisille ja negatiivisille arvonlisäverokoodeille (<strong>Verot</strong> &gt; <strong>Välilliset verot</strong> &gt; <strong>Arvonlisävero</strong> &gt; <strong>Arvonlisäverokoodit</strong>).</p>
<ol>
<li>Luo arvonlisäverokoodi, jolla on positiivinen arvo.</li>
<li>Luo arvonlisäverokoodi, jolla on negatiivinen arvo. Valitse <strong>Salli negatiivinen alv-prosentti</strong> -asetukseksi <strong>Kyllä</strong>.
Tämä negatiivinen arvonlisäverokoodi on määritettävä ensin nimikkeen arvonlisäveroryhmään ja nimikkeen arvonlisäveroryhmä on sitten määritettävä nimikkeisiin, joissa on käänteinen verovelvollisuus.</li>
</ol>
<p>Lisätietoja on seuraavassa kohdassa &quot;Arvonlisäveroryhmien ja nimikkeiden arvonlisäveroryhmien määrittäminen.&quot;</p>
</td>
</tr>
</tbody>
</table>

## <a name="set-up-sales-tax-groups-and-item-sales-tax-groups"></a><a name="sales-tax-item-sales-tax-groups"></a>Arvonlisäveroryhmien ja nimikkeiden arvonlisäveroryhmien määrittäminen
Osto- ja myyntitoimintoihin kannattaa käyttää erillisiä arvonlisäveroryhmiä.

<table>
<tr>
<td><strong>Myynnin arvonlisäveroryhmä</strong></td>
<td>Luo arvonlisäveroryhmä käänteisen veron myyntitoiminnoille (<strong>Verot</strong> &gt; <strong>Välilliset verot</strong> &gt; <strong>Arvonlisävero</strong> &gt; <strong>Arvonlisäveroryhmät</strong>). Sisällytä <strong>Asetukset</strong>-välilehdessä tämän ryhmän käänteisen veron arvonlisäverokoodi. Valitse arvolisäkoodin <strong>Vapautus</strong>- ja <strong>Käänteinen vero</strong> -valintaruudut.</td>
</tr>
<tr>
<td><strong>Ostojen arvonlisäveroryhmät</strong></td>
<td>Luo arvonlisäveroryhmä käänteisen veron ostotoiminnoille (<strong>Verot</strong> &gt; <strong>Välilliset verot</strong> &gt; <strong>Arvonlisävero</strong> &gt; <strong>Arvonlisäveroryhmät</strong>). Sisällytä <strong>Asetukset</strong>-välilehdessä tähän ryhmään sekä negatiiviset ja positiiviset arvonlisäverokoodit. Valitse <strong>Käänteinen vero</strong> -valintaruutu arvoltaan negatiiviselle arvonlisäverokoodille.</td>
</tr>
<tr>
<td><strong>Nimikkeen arvonlisäveroryhmät</strong></td>
<td>Luo tai päivitä arvoltaan negatiivinen arvolisäkoodillinen nimekkeen arvolisävero (<strong>Verot</strong> &gt; <strong>Välilliset verot</strong> &gt; <strong>Arvonlisävero</strong> &gt; <strong>Nimikkeen arvolisäveroryhmät</strong>). Oletusarvoinen nimikkeen arvonlisäveroryhmä on määritettävä tuotteille ja luokille, joita käänteinen arvonlisävero koskee.</td>
</tr>
</table>

## <a name="set-up-reverse-charge-item-groups"></a><a name="reverse-charge-item-group"></a>Määritä käänteisen veloituksen nimikeryhmät
Voit määrittää **Käänteisen veloituksen nimikeryhmät** -sivulla (**Verot** &gt; **Asetukset** &gt; **Arvonlisävero** &gt; **Käänteisen veloituksen nimikeryhmät**) tuote- tai palveluryhmät tai yksittäiset tuotteet tai palvelut, joissa voidaan käyttää käänteistä arvonlisäveroa. Määritä kullekin käänteisen veron nimikeryhmälle myynnin ja/tai ostojen nimike-, nimikeryhmä- tai luokkaluettelo.

## <a name="set-up-reverse-charge-rules"></a><a name="reverse-charge-rules"></a>Käänteisen verotuksen sääntöjen määrittäminen
Voit määrittää **Käänteinen veloituksen säännöt** -sivulla (**Verot** &gt; **Asetukset** &gt; **Arvonlisävero** &gt; **Käänteisen veloituksen säännöt**) soveltuvuussäännöt ostoja ja myyntiä varten. Voit määrittää käänteisen verotuksen soveltuvuussääntöjoukon. Määritä kullekin säännölle seuraavat kentät:

- **Tiedostotyyppi** – valitse **Ostotilaus**, **Toimittajan laskun kirjauskansio**, **Myyntitilaus**, **Vapaatekstilasku**, **Myyntilaskukirjauskansio** ja/tai **Toimittajan lasku**.
- **Kumppanin maan/alueen tyyppi** – Valitse **Kotimaa**, **EU**, **GCC** tai **Ulkomaa**. Jos sääntöä voi vaihtoehtoisesti käyttää kaikissa kauppakumppaneissa osoitteen maasta tai alueesta riippumatta, valitse **Kaikki**.
- **Kotimaantoimituksen osoite** – Kun tämä valintaruutu valitaan, sääntöä käytetään samassa maassa tai samalla alueella tehtäviin toimituksiin. Tätä valintaruutua ei voi valita, jos asiakirjan tyyppi on **Toimittajan laskun kirjauskansio** ja **Myyntilaskukirjauskansio**.
- **Käänteisen veloituksen nimikeryhmä** – valitse ryhmä, jossa sääntöä voidaan käyttää.
- **Raja-arvo** – Käänteistä veromallia käytetään laskussa vain, jos käänteisen verotuksen nimekeryhmään sisältyvien nimikkeiden ja/tai palvelujen arvo ylittää tässä määritetyn raja-arvon.

Voit määrittää myös säännön voimassaolojakson käyttämällä **Voimaantulopäivä**- ja **Vanhentumispäivä**-kenttiä.

Voit lisäksi määrittää, näkyvätkö ilmoitukset ja päivitetäänkö asiakirjan rivin oletusarvoisella käänteisellä arvonlisäveroryhmällä, jos kyseisen asiakirjarivin ehto täyttyy. Valittavissa ovat seuraavat vaihtoehdot:

- **Ei mitään** – asiakirjariviä ei päivitetä.
- **Kehote** – avautuva ilmoitus pyytää vahvistamaan, että käänteistä vero saa käyttää.
- **Määritä** – asiakirjarivi päivitetään ilman lisäilmoituksia.

## <a name="set-up-countryregion-properties"></a><a name="Set-up-Country/region-properties"></a>Maan/alueen ominaisuuksien määrittäminen
Määritä **Ulkomaankaupan parametrit** -sivun (**Vero** &gt; **Asetukset** &gt; **Arvonlisävero** &gt; **Ulkomaankauppa** &gt; **Ulkomaankaupan parametrit**) **Maan/alueen ominaisuudet** -välilehdessä nykyisen yrityksen maaksi/alueeksi *Kotimaa*. Määritä yrityksen kanssa EU-kauppaan osallistuvien EU-maiden-/alueiden **maan/alueen tyypiksi** *EU*. Määritä yrityksen kanssa GCC-kauppaan osallistuvien GCC-maiden/-alueiden **maan/alueen tyypiksi** *GCC*.

## <a name="set-up-default-parameters"></a>Oletusparametrien määrittäminen
Voit ottaa käänteisen verovelvollisuuden toiminnon käyttöön valitsemalla **Kirjanpitoparametrit**-sivun **Käänteinen veloitus**-välilehdessä **Ota käänteinen veloitus käyttöön** -asetukseksi **Kyllä**. Valitse **Ostotilauksen arvonlisäveroryhmä**- ja **Myyntitilauksen arvonlisäveroryhmä** -kentissä oletusarvoiset arvonlisäveroryhmät. Kun käänteisen veron soveltuvuusehto täyttyy, myynti- tai ostotilausrivi päivitetään näillä arvonlisäveroryhmillä.

## <a name="reverse-charge-on-a-sales-invoice"></a><a name="reverse-charge-sale"></a>Myyntilaskun käänteinen vero
Käänteisen veromallin alaisessa myynnissä myyjä ei voita arvolisäveroa. Laskussa ilmoitetaan sen sijaan sekä käänteisen verovelvollisuuden alaiset nimikkeet että käänteisen verovelvollisuuden kokonaissumma.

Kun kirjattavassa myyntilaskussa on käänteistä veroa, arvolisäverotapahtumissa on verosuuntana **Maksettava arvonlisävero**, arvonlisävero on nolla ja **Käänteinen veloitus**- ja **Vapautus**-valintaruudut on valittu.

## <a name="reverse-charge-on-a-purchase-invoice"></a><a name="reverse-charge-purchase"></a>Ostolaskun käänteinen vero
Käänteiseen veromalliin kuuluvissa ostoissa käänteisen veron sisältävän laskun vastaanottava ostaja toimii ostajana ja myyjänä arvonlisäveron kirjanpitoa varten.

Kun käänteisen veron sisältävä ostolasku kirjataan, kirjanpitoon luodaan kaksi arvonlisäverotapahtumaa. Toisen tapahtuman verosuunta on **Saatava arvonlisävero**. Toisessa tapahtumassa verosuunta on **Maksettava arvonlisävero** ja **Käänteinen veloitus** -valintaruutu on valittu.

Seuraavassa näyttökuvassa yhdessä tapahtumassa suuntana on **Saatava arvonlisävero** ja toisessa **Maksettava arvonlisävero**. 

![Kirjattu arvonlisävero](media/apac-sau-posted-sales-tax.png)

## <a name="enable-reverse-charge-mechanism-for-vatgst-scheme-feature"></a><a name="enable-reverse-charge"></a>Ota ALV/GST-veromalliominaisuuden käänteisen verovelvollisuuden mekanismi käyttöön
Hae ominaisuus **Ominaisuuksien hallinta** -työtilassa ja valitse **Ota käyttöön**.

Kun toiminto on otettu käyttöön, **Käänteinen veloitus** -välilehti on käytettävissä kaikissa yrityksissä. Ota Käänteinen veloitus -toiminnallisuus käyttöön yritykselle määrittämällä **Ota Käänteinen veloitus käyttöön** -valinnaksi **Kyllä**.

Seuraavat ominaisuusasetuksiin liittyvät sivut ja valikkovaihtoehdot ovat käytettävissä:
 - **Käänteisen veloituksen nimikeryhmät** (**Vero** > **Asetus** > **Arvonlisävero** > **Käänteisen veloituksen nimikeryhmät**). Lisätietoja on osassa [Määritä käänteisen veloituksen nimikeryhmät- ](#reverse-charge-item-group).
 - **Käänteisen veloituksen säännöt**  (**Vero** > **Asetukset** > **Arvonlisävero** > **Käänteisen veloituksen säännöt**). Katso [Käänteisen verotuksen sääntöjen määrittäminen](#reverse-charge-rules).
 - **Ulkomaankauppaparametrit** (**Vero** > **Asetus** > **Arvonlisävero** > **Ulkomaankauppa** > **Ulkomaankauppaparametrit**). Katso [Maan/alueen ominaisuuksien määrittäminen](#Set-up-Country/region-properties).

**Käänteinen veloitus** -valintaruutu on käytettävissä **Arvonlisäveroryhmä** ja **Kirjattu arvonlisävero** -sivuilla. Lisätietoja on kohdissa [Arvonlisäveroryhmien ja nimikkeen arvonlisäveroryhmien määrittäminen](#sales-tax-item-sales-tax-groups), [Myyntilaskun käänteinen veloitus](#reverse-charge-sale) ja [Ostolaskun käänteinen veloitus](#reverse-charge-purchase).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]