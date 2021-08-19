---
title: Tarkista määritetty ER-komponentti estääksesi suorituksen aikaiset ongelmat
description: Tässä aiheessa selitetään, miten määritetyt Sähköisen raportoinnin (ER) komponentit voidaan tarkistaa mahdollisten suorituksen aikaisten ongelmien välttämiseksi.
author: NickSelin
ms.date: 03/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner, EROperationDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: dd4f2b00dd7634a44b75c76753f5d864b039391f4fcb29e750fb17e8a03e9b77
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6718620"
---
# <a name="inspect-the-configured-er-component-to-prevent-runtime-issues"></a>Tarkista määritetty ER-komponentti estääksesi suorituksen aikaiset ongelmat

[!include[banner](../includes/banner.md)]

Jokainen määritetty [Sähköisen raportoinnin (ER)](general-electronic-reporting.md) [muoto-](general-electronic-reporting.md#FormatComponentOutbound) ja [mallin yhdistämismääritys -](general-electronic-reporting.md#data-model-and-model-mapping-components) komponentti voidaan [oikeellisuustarkistaa](er-fillable-excel.md#validate-an-er-format) suunnittelun aikana. Tämän oikeellisuustarkistuksen aikana suoritettava yhdenmukaisuustarkistus auttaa estämään suorituksen aikaisia ongelmia, kuten suoritusvirheitä ja suorituskyvyn heikentymistä. Tarkistus ilmoittaa jokaiselle löydetylle ongelmalle ongelmallisen elementin polun. Automaattista korjausta voidaan käyttää joihinkin ongelmiin.

Oletusarvon mukaan oikeellisuustarkistusta käytetään seuraavissa tapauksissa automaattisesti ER-kokoonpanossa, joka sisältää aiemmin mainitut ER-komponentit:

- [Tuot](general-electronic-reporting.md#importing-an-er-component-from-lcs-to-use-it-internally) uuden ER-kokoonpanon [version](general-electronic-reporting.md#component-versioning) Microsoft Dynamics 365 Finance -esiintymääsi.
- Muutat muokattavan ER-määrityksen [tilan](general-electronic-reporting.md#component-versioning) arvosta **Luonnos** arvoksi **Valmis**.
- [Vaihdat perusversiota](general-electronic-reporting.md#upgrading-a-format-selecting-a-new-version-of-base-format-rebase) muokattavalle ER-määritykselle suorittamalla uuden perusversion.

Voit suorittaa tämän oikeellisuustarkistuksen eksplisiittisesti. Valitse jokin seuraavista kolmesta vaihtoehdosta ja noudata annettuja vaiheita:

- Valinta 1:

    1. Siirry kohtaan **Organisaation hallinto \> Sähköinen raportointi \> Konfiguraatiot**.
    2. Valitse vasemman ruudun määritykset-puussa haluamasi ER-määritys, joka sisältää ER-muodon tai ER-mallin yhdistämismäärityksen komponentin.
    3. Valitse **Versiot**-pikavälilehdellä valitun ER-konfiguraation haluttu versio.
    4. Valitse toimintoruudussa **Validoi**.

- Vaihtoehto 2, jos kyseessä on ER-muoto:

    1. Siirry kohtaan **Organisaation hallinto \> Sähköinen raportointi \> Konfiguraatiot**.
    2. Valitse vasemman ruudun määritykset-puussa haluamasi ER-määritys, joka sisältää ER-mallin yhdistämismäärityksen komponentin.
    3. Valitse **Versiot**-pikavälilehdellä valitun ER-konfiguraation haluttu versio.
    4. Valitse toimintoruudussa **Suunnittelija**.
    5. Valitse **Muodon suunnittelija**-sivulla hallintapaneelista **Oikeellisuustarkistus**.

- Vaihtoehto 3, jos kyseessä on ER-mallin yhdistämismääritys:

    1. Siirry kohtaan **Organisaation hallinto \> Sähköinen raportointi \> Konfiguraatiot**.
    2. Valitse vasemman ruudun määritykset-puussa haluamasi ER-määritys, joka sisältää ER-mallin yhdistämismäärityksen komponentin.
    3. Valitse **Versiot**-pikavälilehdellä valitun ER-konfiguraation haluttu versio.
    4. Valitse toimintoruudussa **Suunnittelija**.
    5. Valitse **Malli tietolähteen yhdistämismääritystä varten** -sivun toimintoruudussa **Suunnittelija**.
    6. Valitse **Mallin yhdistämismäärityksen suunnittelija** -sivun toimintoruudussa **Oikeellisuustarkistus**.

Voit ohittaa oikeellisuustarkistuksen määrityksiä tuotaessa noudattamalla näitä vaiheita.

1. Siirry kohtaan **Organisaation hallinto \> Sähköinen raportointi \> Konfiguraatiot**.
2. Valitse **Määritykset**-sivun toimintoruudun **Määritykset**-välilehden **Lisämääritykset**-ryhmässä **Käyttäjäparametrit**.
3. Määritä **Vahvista määritykset tuonnin jälkeen** -asetuksen arvoksi **Ei**.

Voit ohittaa oikeellisuustarkistuksen, kun version tila vaihdetaan tai palautetaan, noudattamalla seuraavia ohjeita.

1. Siirry kohtaan **Organisaation hallinto \> Sähköinen raportointi \> Konfiguraatiot**.
2. Valitse **Määritykset**-sivun toimintoruudun **Määritykset**-välilehden **Lisämääritykset**-ryhmässä **Käyttäjäparametrit**.
3. Määritä **Ohita oikeellisuustarkistus kun tila muuttuu tai perusta vaihtuu** -määritykseksi vaihtoehto **Kyllä**.

ER käyttää seuraavia luokkia yhdenmukaisuustarkistustarkastusten ryhmittelemiseen:

- **Suoritettavuus**-tarkistukset, jotka tunnistavat kriittiset ongelmat, jotka voivat tapahtua suorituksen aikana. Nämä ongelmat ovat useimmiten **Virhe**-tasolla. 
- **Suorituskyky**-tarkistukset, jotka tunnistavat ongelmat, jotka voivat aiheuttaa määritettyjen ER-komponenttien tehottoman suorituksen. Nämä ongelmat ovat useimmiten **Varoitus**-tasolla.
- **Tietojen eheys** -tarkistukset, jotka tunnistavat ongelmat, jotka voivat aiheuttaa tietojen menettämistä tai suorituksen aikaisia ongelmia. Nämä ongelmat ovat useimmiten **Varoitus**-tasolla.

## <a name="list-of-inspections"></a>Luettelo tarkistuksista

Seuraavassa taulukossa on yhteenveto ER:n tarjoamista tarkistuksista. Lisätietoja näistä tarkistuksista saat tämän aiheen asiaankuuluvista osista käyttämällä ensimmäisen sarakkeen linkkejä. Näissä osissa selitetään, minkä tyyppisille komponenteille ER tarjoaa tarkistuksia, ja miten voit määrittää komponentteja uudelleen, jotta ongelmat voidaan estää.

<table>
<thead>
<tr>
<th>Nimi</th>
<th>Luokka</th>
<th>Taso</th>
<th>Hallinta</th>
</tr>
</thead>
<tbody>
<tr>
<td><a href='#i1'>Tyypin muuntaminen</a></td>
<td>Suoritettavuus</td>
<td>Virhe</td>
<td>
<p>Lauseketta, jonka tyyppi on &lt;tyyppi&gt; ei voida muuttaa kenttätyypiksi &lt;tyyppi&gt;.</p>
<p><b>Suorituksenaikainen virhe:</b> tyypin poikkeus</p>
</td>
</tr>
<tr>
<td><a href='#i2'>Tyyppiyhteensopivuus</a></td>
<td>Suoritettavuus</td>
<td>Virhe</td>
<td>
<p>Määritettyä lauseketta ei voi käyttää sitovana nykyisessä muotoelementissä tietolähteelle, koska tämä lauseke palauttaa tietotyypin &lt;tyyppi&gt; arvon, joka on nykyisin muotoelementin, jonka tyyppi on &lt;tyyppi&gt;, tukemien tietotyyppien ulkopuolella.</p>
<p><b>Suorituksenaikainen virhe:</b> poikkeus tyyppiä</p>
</td>
</tr>
<tr>
<td><a href='#i3'>Puuttuva määrityselementti</a></td>
<td>Suoritettavuus</td>
<td>Virhe</td>
<td>
<p>Polkua ei löydy &lt;polku&gt;.</p>
<p><b>Suorituksenaikainen virhe:</b> määritys &lt;polun&gt; elementtiä ei löydy</p>
</td>
</tr>
<tr>
<td><a href='#i4'>FILTER-funktion sisältävän lausekkeen suoritettavuus</a></td>
<td>Suoritettavuus</td>
<td>Virhe</td>
<td>
<p>Suodatintoiminnon luettelolausekkeesta ei voi tehdä kyselyjä.</p>
<p><b>Suorituksenaikainen virhe:</b> suodatusta ei tueta. Vahvista määritykset saadaksesi tästä lisätietoja.</p>
</td>
</tr>
<tr>
<td rowspan='2'><a href='#i5'>GROUPBY-tietolähteen suoritettavuus</a></td>
<td>Suoritettavuus</td>
<td>Virhe</td>
<td>Polku &lt;polku&gt; ei tue kyselyjä.</td>
</tr>
<tr>
<td>Suoritettavuus</td>
<td>Virhe</td>
<td>
<p>Group by -funktiota ei voi suorittaa kyselyllä.</p>
<p><b>Runtime error:</b> Group by -funktiota ei voi suorittaa kyselyllä.</p>
</td>
</tr>
<tr>
<td><a href='#i6'>JOIN-tietolähteen suoritettavuus</a></td>
<td>Suoritettavuus</td>
<td>Virhe</td>
<td>
<p>Ei voi liittyä luettelo &lt;polkuun&gt;, joka ei ole suodatin kyselyssä.</p>
<p><b>Suorituksenaikainen virhe:</b> funktiolla liitetyn tietolähteen tulisi olla suodatuslauseke, laskettua kenttää on kutsuttu väärin.</p>
</td>
</tr>
<tr>
<td><a href='#i7'>FILTER-funktion suositeltavuus WHERE-funktion asemesta</a></td>
<td>Suoritustaso</td>
<td>Varoitus</td>
<td>FILTER-funktion käyttäminen lausekkeessa on suorituskykysyistä suositeltavampaa kuin WHERE-funktion. Valitse Korjaa, jos haluat korvata sen automaattisesti.</td>
</tr>
<tr>
<td><a href='#i8'>ALLITEMSQUERY-funktion suositeltavuus ALLIITEMS-funktion asemesta</a></td>
<td>Suoritustaso</td>
<td>Varoitus</td>
<td>ALLITEMSQUERY-funktion käyttäminen lausekkeessa on suorituskykysyistä suositeltavampaa kuin ALLITEMS-funktion. Valitse Korjaa, jos haluat korvata sen automaattisesti.</td>
</tr>
<tr>
<td><a href='#i9'>Tyhjien luettelotapausten käsittely</a></td>
<td>Suoritettavuus</td>
<td>Varoitus</td>
<td>
<p>Luettelon &lt;polulla&gt; ei ole tarkistusta tyhjään luettelotapausta varten, joten se voi aiheuttaa virheen suorituksen aikana. Lisää tarkistus tyhjään luettelotapaukseen.</p>
<p><b>Suorituksenaikainen virhe:</b> luettelo on tyhjä &lt;polussa&gt;</p>
<p><b><a href='#i9a'>Mahdollinen ongelma</a>:</b> rivi täyttyy kerran, kun taas tietolähde, josta se on täytetty, sisältää useita tietueita</p>
</td>
</tr>
<tr>
<td><a href='#i10'>FILTER-funktion sisältävän lausekkeen suoritettavuus (välimuistin käyttö)</a></td>
<td>Suoritettavuus</td>
<td>Virhe</td>
<td>
<p>FILTER-funktiota ei voi käyttää valitussa tietolähdetyypissä. Tietolähde, jonka tyyppi on Taulukkotietueet, on sovellettavissa ainoastaan, kun sitä ei viedä välimuistiin, ja sillä ei ole manuaalisesti lisättyjä sisäkkäisiä tietolähteitä.</p>
<p><b>Suorituksenaikainen virhe:</b> suodatusta ei tueta. Vahvista määritykset saadaksesi tästä lisätietoja.</p>
</td>
</tr>
<tr>
<td><a href='#i11'>Sidonta puuttuu</a></td>
<td>Suoritettavuus</td>
<td>Varoitus</td>
<td>
<p>Polku &lt;polulla&gt; ei ole sidontaa mihinkään tietolähteeseen mallin yhdistämismäärityksen käytössä.</p>
<p><b>Suorituksenaikainen virhe:</b> polku &lt;polkua&gt; ei ole sidottu</p>
</td>
</tr>
<tr>
<td><a href='#i12'>Ei linkitettyä mallia</a></td>
<td>Tietojen eheys</td>
<td>Varoitus</td>
<td>Tiedosto&lt;nimi&gt; on linkitetty ilman tiedostokomponentteja, ja se poistetaan määritysversion tilan muuttamisen jälkeen.</td>
</tr>
<tr>
<td><a href='#i13'>Ei synkronoitu muoto</a></td>
<td>Tietojen eheys</td>
<td>Varoitus</td>
<td>Määritettyä nimi&lt;komponentin nimeä&gt; ei ole Excel-taulukon &lt;taulukon nimessä&gt;</td>
</tr>
<tr>
<td><a href='#i14'>Ei synkronoitu muoto</a></td>
<td>Tietojen eheys</td>
<td>Varoitus</td>
<td>
<p>&lt;Merkittyä Word-sisällön ohjausobjektin&gt; tunnistetta ei ole Word-mallitiedostossa</p>
<p><b>Suoritusvirhe:</b> &lt;Merkittyä Word-sisällön ohjausobjektin&gt; tunnistetta ei ole Word-mallitiedostossa.</p>
</td>
</tr>
<tr>
<td><a href='#i15'>Ei oletusmääritystä</a></td>
<td>Tietojen eheys</td>
<td>Virhe</td>
<td>
<p>&lt;model name (root descriptor)&gt; -tietomallille on olemassa useita mallimäärityksiä konfiguroinneissa &lt;configuration names separated by comma&gt;. Määritä jokin määrityksistä oletukseksi</p>
<p><b>Suoritusvirhe:</b> &lt;model name (root descriptor)&gt; -tietomallille on olemassa useita mallimäärityksiä konfiguroinneissa &lt;configuration names separated by comma&gt;. Määritä jokin määrityksistä oletukseksi.</p>
</td>
</tr>
<tr>
<td><a href='#i16'>Ylä- tai alatunnistekomponenttien määrittäminen on ristiriidassa</a></td>
<td>Tietojen eheys</td>
<td>Virhe</td>
<td>
<p>Otsikot/alatunnisteet (&lt;component type: Header or Footer&gt;) ovat ristiriidassa</p>
<p><b>Suorituksen aikainen:</b> Viimeistä konfiguroitua osaa käytetään ajon aikana, jos konfiguroitu ER-muodon luonnosversio suoritetaan.</p>
</td>
</tr>
</tbody>
</table>

## <a name="type-conversion"></a><a id="i1"></a>Tyypin muuntaminen

ER tarkistaa, onko tietomallikentän tietotyyppi yhteensopiva sen lausekkeen tietotyypin kanssa, joka on määritetty kyseisen kentän sitovaksi. Jos tietotyypit eivät ole yhteensopivia, ER-mallin yhdistämismäärityksen suunnittelussa tapahtuu oikeellisuustarkistusvirhe. Näyttöön tulee sanoma, jonka mukaan ER ei voi muuntaa tyypin A lauseketta tyypin B kentäksi.

Seuraavissa vaiheissa näkyy, miten tämä ongelma voi ilmetä.

1. Aloita ER-tietomallin ja ER-mallin yhdistämismäärityskomponenttien määrittäminen samanaikaisesti.
2. Lisää tietomalli puussa **X**-niminen kenttä ja valitse tietotyypiksi **kokonaisluku**.

    ![X-kenttä ja kokonaislukutietotyyppi lisättyinä tietomuotopuuhun Tietomalli-sivulla.](./media/er-components-inspections-01.png)

3. Lisää mallin yhdistämismäärityksen suunnitteluohjelman **Tietolähteet**-ruudussa tietolähde, jonka tyyppi on **Laskettu kenttä**.
4. Nimeä uusi tietolähde nimellä **Y** ja määritä se siten, että se sisältää lausekkeen `INTVALUE(100)`.
5. Sido **X** kohteeseen **Y**.
6. Vaihda tietomallin suunnittelijassa **X**-kentän tietotyyppi **kokonaisluvusta** tyypiksi **Int64**.
7. Valitse **Oikeellisuustarkistus** tarkastellaksesi muokattavaa mallin yhdistämismäärityskomponenttia **Mallin yhdistämismäärityksen suunnittelija** -sivulla.

    ![Muokattavan mallin yhdistämismäärityskomponentin oikeellisuustarkistus Mallin yhdistämismäärityksen suunnittelija -sivulla.](./media/er-components-inspections-01.gif)

8. Valitse **Oikeellisuustarkistus** tarkastellaksesi mallin yhdistämismäärityskomponenttia valitussa ER-määrityksessä **Määritykset**-sivulla.

    ![Mallin yhdistämismäärityskomponentin tarkastaminen Määritykset-sivulla.](./media/er-components-inspections-01a.png)

9. Huomaa, että vahvistusvirhe ilmenee. Sanoma ilmoittaa, että **Kokonaisluku**-tyypin arvoa, jonka `INTVALUE(100)`-lauseke **Y**-tietolähteestä palauttaa, ei voida tallentaa **X**-tietomallikenttään, jonka tyyppi on **Int64**.

Seuraavassa kuvassa näkyy suorituksenaikainen virhe, joka ilmenee, jos ohitat varoituksen ja valitset **Suorita** suorittaaksesi muodon, joka on määritetty käyttämään mallin yhdistämismääritystä.

![Suorituksenaikaiset virheet Muodon suunnittelija -sivulla.](./media/er-components-inspections-01b.png)

### <a name="automatic-resolution"></a>Automaattinen ratkaisu

Tätä ongelmaa ei voi korjata automaattisesti.

### <a name="manual-resolution"></a>Manuaalinen ratkaisu

#### <a name="option-1"></a>Asetus 1

Päivitä tietomallin rakenne muuttamalla tietomallin kentän tietotyyppiä siten, että se vastaa kentän sidontaan määritetyn lausekkeen tietotyyppiä. Edellä olevassa esimerkissä **X**-kentän tietotyyppi on muutettava takaisin **Kokonaisluvuksi**.

#### <a name="option-2"></a>Asetus 2

Päivitä mallin yhdistämismääritys muuttamalla tietomalli-kenttään sidotun tietolähteen lauseketta. Yllä olevassa esimerkissä **Y**-tietolähteen lauseke on muutettava lausekkeeksi `INT64VALUE(100)`.

## <a name="type-compatibility"></a><a id="i2"></a>Tyyppiyhteensopivuus

ER tarkistaa, onko muotoelementin tietotyyppi yhteensopiva sen lausekkeen tietotyypin kanssa, joka on määritetty kyseisen muotoelementin sitovaksi. Jos tietotyypit eivät ole yhteensopivia, ER-toimintojen suunnittelijassa tapahtuu oikeellisuustarkistusvirhe. Vastaanottamasi viesti ilmoittaa, että määritettyä lauseketta ei voida käyttää sitomaan nykyistä muotoelementtiä tietolähteeseen, koska lauseke palauttaa arvon, jonka tietotyyppi on A, joka on nykyisen, tyyppiä B olevan muotoelementin tukemien tietotyyppien ulkopuolella.

Seuraavissa vaiheissa näkyy, miten tämä ongelma voi ilmetä.

1. Aloita ER-tietomallin ja ER-muotokomponenttien määrittäminen yhtäaikaisesti.
2. Lisää tietomalli puussa **X**-niminen kenttä ja valitse tietotyypiksi **kokonaisluku**.
3. Lisää muotorakenne puussa muotoelementti, jonka tyyppi on **Numero**.
4. Nimeä uusi muotoelementti elementiksi **Y** . Valitse **Numerotyyppi**-kentässä tietotyypiksi **Kokonaisluku**.
5. Sido **X** kohteeseen **Y**.
6. Muuta muotorakennepuussa **Y**-muotoelementin tyypiksi, joka aiemmin oli **Integer**, tyyppi **Int64**.
7. Valitse **Oikeellisuustarkistus** tarkastellaksesi muokattavaa muotokomponenttia **Muodon suunnittelija** -sivulla.

    ![Tyyppiyhteensopivuuden tarkistaminen Muodon suunnittelija -sivulla.](./media/er-components-inspections-02.gif)

8. Huomaa, että vahvistusvirhe ilmenee. Sanomassa ilmoitetaan, että määritetty lauseke voi hyväksyä vain **Int64**-arvoja. Siksi **X**-tietomallikentän arvoa, jonka tyyppi on **Kokonaisluku**, ei voida syöttää muotoelementtiin **Y**.

### <a name="automatic-resolution"></a>Automaattinen ratkaisu

Tätä ongelmaa ei voi korjata automaattisesti.

### <a name="manual-resolution"></a>Manuaalinen ratkaisu

#### <a name="option-1"></a>Asetus 1

Päivitä muotomallin rakenne muuttamalla **Numero**-muotoelementin tietotyyppiä siten, että se on sama kuin kyseisen elementin sitovaksi määritetyn lausekkeen tietotyyppi. Edellä olevassa esimerkissä **Numerotyyppi**-arvo, joka **X**-muotoelementillä on, on muutettava takaisin tietotyypiksi **Kokonaisluku**.

#### <a name="option-2"></a>Asetus 2

Päivitä **X**-muotoelementin muodon yhdistämismääritys muuttamalla lauseke arvosta `model.X` arvoksi `INT64VALUE(model.X)`.

## <a name="missing-configuration-element"></a><a id="i3"></a>Puuttuva määrityselementti

ER tarkistaa, sisältävätkö sidontalausekkeet vain muokattavaan ER-komponenttiin määritettyjä tietolähteitä. Jokaisen sellaisen sidonnan osalta, joka sisältää muokattavasta ER-komponentista puuttuvan tietolähteen, ER-toimintosuunnittelijassa tai ER-mallin yhdistämismäärityksen suunnittelijassa ilmenee oikeellisuustarkistusvirhe.

Seuraavissa vaiheissa näkyy, miten tämä ongelma voi ilmetä.

1. Aloita ER-tietomallin ja ER-mallin yhdistämismäärityskomponenttien määrittäminen samanaikaisesti.
2. Lisää tietomalli puussa **X**-niminen kenttä ja valitse tietotyypiksi **kokonaisluku**.

    ![Tietomallipuu, jossa on X-kenttä ja Kokonaisluku-tietotyyppi Tietomalli-sivulla.](./media/er-components-inspections-01.png)

3. Lisää mallin yhdistämismäärityksen suunnitteluohjelman **Tietolähteet**-ruudussa tietolähde, jonka tyyppi on **Laskettu kenttä**.
4. Nimeä uusi tietolähde nimellä **Y** ja määritä se siten, että se sisältää lausekkeen `INTVALUE(100)`.
5. Sido **X** kohteeseen **Y**.
6. Poista mallin yhdistämismäärityksen suunnittelijan **Tietolähteet**-ruudusta tietolähde **Y**.
7. Valitse **Oikeellisuustarkistus** tarkastellaksesi muokattavaa mallin yhdistämismäärityskomponenttia **Mallin yhdistämismäärityksen suunnittelija** -sivulla.

    ![Muokattavan ER-mallin yhdistämismäärityskomponentin tarkastaminen Mallin yhdistämismäärityksen suunnittelija -sivulla.](./media/er-components-inspections-03.gif)

8. Huomaa, että vahvistusvirhe ilmenee. Sanomassa todetaan, että **X**-tietomallikentän sidonta sisältää **Y**-tietolähteeseen viittaavan polun, mutta tätä tietolähdettä ei löydy.

### <a name="automatic-resolution"></a>Automaattinen ratkaisu

Valitse **Pura sidonta** korjataksesi tämän ongelman automaattisesti poistamalla puuttuvan tietolähteen sidonnan.

### <a name="manual-resolution"></a>Manuaalinen ratkaisu

#### <a name="option-1"></a>Asetus 1

Pura tietomallikentän **X** sidonta lopettaaksesi viittaamisen **Y**-tietolähteeseen, jota ei ole olemassa.

#### <a name="option-2"></a>Asetus 2

Lisää mallin yhdistämismääritysten suunnittelijan **Tietolähteet**-ruudussa tietolähde **Y** uudelleen.

## <a name="executability-of-an-expression-with-filter-function"></a><a id="i4"></a>FILTER-funktion sisältävän lausekkeen suoritettavuus

Sisäänrakennettua [FILTER](er-functions-list-filter.md)-ER-funktiota käytetään sovelluksen taulujen, näkymien tai tietoentiteettien käsittelyyn sijoittamalla yksittäinen SQL-kutsu hakemaan vaadittu tieto tietueluettelona. Tietolähdettä, jonka tyyppi on **Tietueluettelo**, käytetään tämän funktion argumenttina, ja se määrittää sovelluslähteen kutsulle. ER tarkistaa, voidaanko suora SQL-kysely määrittää tietolähteelle, johon viitataan `FILTER`-funktiossa. Jos suoraa kyselyä ei voi määrittää, ER-mallin yhdistämismäärityksen suunnittelijassa ilmenee oikeellisuustarkistusvirhe. Näyttöön tulee sanoma, jonka mukaan toiminnon sisältävä ER `FILTER` -funktio ei voi toimia suorituksen aikana.

Seuraavissa vaiheissa näkyy, miten tämä ongelma voi ilmetä.

1. Aloita ER-mallin yhdistämismäärityskomponentin määrittäminen.
2. Lisää tietolähde, jonka tietotyyppi on **Dynamics 365 for Operations \\ -taulutietueet**.
3. Anna uudelle tietolähteelle nimeksi **Vendor**. Valitse **Taulu**-kentässä **VendTable** määrittämään, että tämä tietolähde pyytää VendTable-taulua.
4. Lisää tietolähde, jonka tietotyyppi on **Laskettu kenttä**.
5. Anna uudelle tietolähteelle nimeksi **FilteredVendor** ja määritä se sisältämään lauseke `FILTER(Vendor, Vendor.AccountNum="US-101")`.
6. Valitse **Oikeellisuustarkistus** tarkastellaksesi muokattavaa mallin yhdistämismäärityskomponenttia **Mallin yhdistämismäärityksen suunnittelija** -sivulla ja varmista, että `FILTER(Vendor, Vendor.AccountNum="US-101")`-lauseke **Vendor**-tietolähteessä on kyseltävissä.
7. Muokkaa **Vendor**-tietolähdettä lisäämällä sisäkkäinen kenttä, jonka tyyppi on **Laskettu kenttä** saadaksesi lyhennetyn toimittajan tilin numeron.
8. Anna uudelle sisäkkäiselle kentälle nimeksi **$AccNumber** ja määritä se sisältämään lauseke `TRIM(Vendor.AccountNum)`.
9. Valitse **Oikeellisuustarkistus** tarkastellaksesi muokattavaa mallin yhdistämismäärityskomponenttia **Mallin yhdistämismäärityksen suunnittelija** -sivulla ja varmista, että `FILTER(Vendor, Vendor.AccountNum="US-101")`-lauseke **Vendor**-tietolähteessä on kyseltävissä.

    ![Lausekkeen kyseltävyyden tarkistaminen Mallin yhdistämismäärityksen suunnittelija -sivulla.](./media/er-components-inspections-04.gif)

10. Huomaa, että oikeellisuustarkistus virhe ilmenee, koska **Vendor**-tietolähde sisältää sisäkkäisen kentän tyyppiä **Laskettu kenttä**, joka ei salli **FilteredVendor**-tietolähteen lausekkeen kääntämistä suoraksi SQL-lausekkeeksi.

Seuraavassa kuvassa näkyy suorituksenaikainen virhe, joka ilmenee, jos ohitat varoituksen ja valitset **Suorita** suorittaaksesi muodon, joka on määritetty käyttämään mallin yhdistämismääritystä.

![Suorituksenaikaiset virheet, jotka ilmenevät, kun Muodon suunnittelija -sivulla suoritetaan muokattava muoto.](./media/er-components-inspections-04a.png)

### <a name="automatic-resolution"></a>Automaattinen ratkaisu

Tätä ongelmaa ei voi korjata automaattisesti.

### <a name="manual-resolution"></a>Manuaalinen ratkaisu

#### <a name="option-1"></a>Asetus 1

Sen sijaan, että lisättäisiin sisäkkäinen kenttä, jonka tyyppi on **Laskettu kenttä** tietolähteeseen **Vendor**, lisää sisäkkäinen kenttä **$AccNumber** tietolähteeseen **FilteredVendor** ja määritä se sisältämään `TRIM(FilteredVendor.AccountNum)`. Näin `FILTER(Vendor, Vendor.AccountNum="US-101")`-lauseke voidaan suorittaa SQL-tasolla ja laskea sisäkkäinen kenttä **$AccNumber** jälkeenpäin.

#### <a name="option-2"></a>Asetus 2

Muuta tietolähteen **FilteredVendor** lauseke arvosta `FILTER(Vendor, Vendor.AccountNum="US-101")` arvoksi `WHERE(Vendor, Vendor.AccountNum="US-101")`. Emme suosittele sellaisen taulukon lausekkeen muuttamista, jossa on suuri tietomäärä (tapahtumataulu), koska kaikki tiedot haetaan ja tarvittavien tietojen valinta tehdään muistissa. Näin ollen tämä lähestymistapa voi heikentää suorituskykyä. Lisätietoja on kohdassa [WHERE ER-funktio](er-functions-list-where.md).

## <a name="executability-of-a-groupby-data-source"></a><a id="i5"></a>GROUPBY-tietolähteen suoritettavuus

**GROUPBY**-tietolähde jakaa kyselyn tuloksen tietueryhmiin, yleensä yhden tai useamman koostamisen suorittamiseksi kullekin ryhmälle. Jokainen **GROUPBY**-tietolähde voidaan määrittää suoritettavaksi joko tietokannan tasolla tai muistissa. Kun **GROUPBY**-tietolähde on määritetty suoritettavaksi tietokantatasolla, ER tarkistaa, voidaanko suora SQL-kysely luoda tietolähteelle, johon viitataan kyseisessä tietolähteessä. Jos suoraa kyselyä ei voi määrittää, ER-mallin yhdistämismäärityksen suunnittelijassa ilmenee oikeellisuustarkistusvirhe. Vastaanotettava sanoma ilmoittaa, että määritettyä **GROUPBY**-tietolähdettä ei voida suorittaa suorituksenaikaisesti.

Seuraavissa vaiheissa näkyy, miten tämä ongelma voi ilmetä.

1. Aloita ER-mallin yhdistämismäärityskomponentin määrittäminen.
2. Lisää tietolähde, jonka tietotyyppi on **Dynamics 365 for Operations \\ -taulutietueet**.
3. Anna uudelle tietolähteelle nimeksi **Trans**. Valitse **Taulu**-kentässä **VendTrans** määrittääksesi, että tämä tietolähde pyytää VendTrans-taulua.
4. Lisää tietolähde, jonka tietotyyppi on **Group by**.
5. Anna uudelle tietolähteelle nimeksi **GroupedTrans** ja määritä se seuraavasti:

    - Valitse **Trans**-tietolähde ryhmiteltävien tietueiden lähteeksi.
    - Valitse **Suoritussijainti**-kentässä **Kysely** määrittääksesi, että haluat suorittaa tämän tietolähteen tietokannan tasolla.

    ![Tietolähteen määrittäminen ryhmittelyparametrien muokkaussivulla.](./media/er-components-inspections-05a.gif)

6. Valitse **Oikeellisuustarkistus** tarkastellaksesi muokattavaa mallin yhdistämismäärityskomponenttia **Mallin yhdistämismäärityksen suunnittelija** -sivulla ja varmista, että määritetty **GroupedTrans**-tietolähde on kyseltävissä.
7. Muokkaa **Trans**-tietolähdettä lisäämällä sisäkkäinen kenttä, jonka tyyppi on **Laskettu kenttä** saadaksesi lyhennetyn toimittajan tilin numeron.
8. Anna uudelle tietolähteelle nimeksi **$AccNumber** ja määritä se sisältämään lauseke `TRIM(Trans.AccountNum)`.

    ![Tietolähteen määrittäminen Mallin yhdistämismäärityksen suunnittelija -sivulla.](./media/er-components-inspections-05a.png)

9. Valitse **Oikeellisuustarkistus** tarkastellaksesi muokattavaa mallin yhdistämismäärityskomponenttia **Mallin yhdistämismäärityksen suunnittelija** -sivulla ja varmista, että määritetty **GroupedTrans**-tietolähde on kyseltävissä.

    ![Suoritetaan oikeellisuustarkistuta ER-mallin yhdistämismäärityskomponentille ja varmistetaan, että määritetty tietolähde GroupedTrans-tietolähde on kyseltävissä Mallin yhdistämismäärityksen suunnittelija -sivulla.](./media/er-components-inspections-05b.png)

10. Huomaa, että oikeellisuustarkistus virhe ilmenee, koska **Trans**-tietolähde sisältää sisäkkäisen kentän tyyppiä **Laskettu kenttä**, joka ei salli **GroupedTrans**-tietolähteen kutsua lausekkeen kääntämiseksi suoraksi SQL-lausekkeeksi.

Seuraavassa kuvassa näkyy suorituksenaikainen virhe, joka ilmenee, jos ohitat varoituksen ja valitset **Suorita** suorittaaksesi muodon, joka on määritetty käyttämään mallin yhdistämismääritystä.

![Suorituksenaikaiset virheet, jotka ilmenevät, kun varoitus ohitetaan Muodon suunnittelija -sivulla.](./media/er-components-inspections-05c.png)

### <a name="automatic-resolution"></a>Automaattinen ratkaisu

Tätä ongelmaa ei voi korjata automaattisesti.

### <a name="manual-resolution"></a>Manuaalinen ratkaisu

#### <a name="option-1"></a>Asetus 1

Sen sijaan, että lisättäisiin sisäkkäinen kenttä, jonka tyyppi on **Laskettu kenttä** tietolähteeseen **Trans**, lisää sisäkkäinen kenttä **$AccNumber** kohteeseen **GroupedTrans.lines** tietolähteessä **GroupedTrans** ja määritä se sisältämään lauseke `TRIM(GroupedTrans.lines.AccountNum)`. Täten **GroupedTrans**-tietolähde voidaan suorittaa SQL-tasolla ja laskea sisäkkäinen kenttä **$AccNumber** jälkeenpäin.

#### <a name="option-2"></a>Asetus 2

Muuta **Suoritussijainti**-kentän arvo **GroupedTrans**-tietolähteelle arvosta **Kysely** arvoksi **Muistissa**. Emme suosittele sellaisen taulun arvon muuttamista, jossa on suuri tietomäärä (tapahtumataulu), koska kaikki tiedot haetaan ja ryhmittely ja koostaminen tehdään muistissa. Näin ollen tämä lähestymistapa voi heikentää suorituskykyä.

## <a name="executability-of-a-join-data-source"></a><a id="i6"></a>JOIN-tietolähteen suoritettavuus

[JOIN](er-join-data-sources.md)-tietolähde yhdistää kahden tai useamman tietokantataulun tiedot toisiinsa liittyvien kenttien perusteella. Jokainen **JOIN**-tietolähde voidaan määrittää suoritettavaksi joko tietokannan tasolla tai muistissa. Kun **JOIN**-tietolähde on määritetty suoritettavaksi tietokantatasolla, ER tarkistaa, voidaanko suora SQL-kysely luoda tietolähteille, joihin viitataan kyseisessä tietolähteessä. Jos suoraa SQL-kyselyä ei voida määrittää vähintään yhdelle viitatulle tietolähteelle, ER-mallin yhdistämismäärityksen suunnittelijassa ilmenee oikeellisuustarkistusvirhe. Vastaanotettava sanoma ilmoittaa, että määritettyä **JOIN**-tietolähdettä ei voida suorittaa suorituksenaikaisesti.

Seuraavissa vaiheissa näkyy, miten tämä ongelma voi ilmetä.

1. Aloita ER-mallin yhdistämismäärityskomponentin määrittäminen.
2. Lisää tietolähde, jonka tietotyyppi on **Dynamics 365 for Operations \\ -taulutietueet**.
3. Anna uudelle tietolähteelle nimeksi **Vendor**. Valitse **Taulu**-kentässä **VendTable** määrittämään, että tämä tietolähde pyytää VendTable-taulua.
4. Lisää tietolähde, jonka tietotyyppi on **Dynamics 365 for Operations \\ -taulutietueet**.
5. Anna uudelle tietolähteelle nimeksi **Trans**. Valitse **Taulu**-kentässä **VendTrans** määrittääksesi, että tämä tietolähde pyytää VendTrans-taulua.
6. Lisää tietolähde, jonka tyyppi on **Laskettu kenttä** sisäkkäiseksi kentäksi **Vendor**-tietolähteeseen.
7. Anna uudelle tietolähteelle nimeksi **FilteredTrans** ja määritä se sisältämään lauseke `FILTER(Trans, Trans.AccountNum=Vendor.AccountNum)`.
8. Lisää tietolähde, jonka tietotyyppi on **Join**.
9. Anna uudelle tietolähteelle nimeksi **JoinedList** ja määritä se seuraavasti:

    1. Lisää **Vendor**-tietolähde ensimmäiseksi liitettävien tietueiden joukoksi.
    2. Lisää **Vendor.FilteredTrans**-tietolähde toiseksi liitettävien tietueiden joukoksi. Valitse tyypiksi **INNER**.
    3. Valitse **Suorita**-kentässä **Kysely** määrittääksesi, että haluat suorittaa tämän tietolähteen tietokannan tasolla.

    ![Tietolähteen määrittäminen Liitoksen suunnittelija -sivulla.](./media/er-components-inspections-06a.gif)

10. Valitse **Oikeellisuustarkistus** tarkastellaksesi muokattavaa mallin yhdistämismäärityskomponenttia **Mallin yhdistämismäärityksen suunnittelija** -suvulla ja varmista, että määritetty **JoinedList**-tietolähde on kyseltävissä.
11. Muuta tietolähteen **Vendor.FilteredTrans** lauseke arvosta `FILTER(Trans, Trans.AccountNum=Vendor.AccountNum)` arvoksi `WHERE(Trans, Trans.AccountNum=Vendor.AccountNum)`.
12. Valitse **Oikeellisuustarkistus** tarkastellaksesi muokattavaa mallin yhdistämismäärityskomponenttia **Mallin yhdistämismäärityksen suunnittelija** -suvulla ja varmista, että määritetty **JoinedList**-tietolähde on kyseltävissä.

    ![Suoritetaan oikeellisuustarkistusta muokattavan mallin yhdistämismäärityskomponentille ja varmistetaan, että JoinedList-tietolähde on kyseltävissä Mallin yhdistämismäärityksen suunnittelija -sivulla.](./media/er-components-inspections-06b.png)

13. Huomaa, että oikeellisuustarkistusvirhe tapahtuu, koska **Vendor.FilteredTrans**-tietolähdettä ei voida kääntää suoraksi SQL-kutsuksi. Lisäksi suora SQL-kutsu ei salli kutsua **JoinedList**-tietolähteen kääntämiseksi suoraksi SQL-lausekkeeksi.

    ![Suorituksenaikaiset virheet JoinedList-tietolähteen epäonnistuneesta oikeellisuustarkistuksesta Mallin yhdistämismäärityksen suunnittelija -sivulla.](./media/er-components-inspections-06c.png)

Seuraavassa kuvassa näkyy suorituksenaikainen virhe, joka ilmenee, jos ohitat varoituksen ja valitset **Suorita** suorittaaksesi muodon, joka on määritetty käyttämään mallin yhdistämismääritystä.

![Suorita muokattava muoto Muodon suunnittelija -sivulla.](./media/er-components-inspections-06e.png)

### <a name="automatic-resolution"></a>Automaattinen ratkaisu

Tätä ongelmaa ei voi korjata automaattisesti.

### <a name="manual-resolution"></a>Manuaalinen ratkaisu

#### <a name="option-1"></a>Asetus 1

Muuta tietolähteen **Vendor.FilteredTrans** lauseke arvosta `WHERE(Trans, Trans.AccountNum=Vendor.AccountNum)` takaisin arvoksi `FILTER(Trans, Trans.AccountNum=Vendor.AccountNum)`, kuten varoitus neuvoi.

![Mallin yhdistämismäärityksen suunnitteluohjelma-sivun tietolähteen päivitetty lauseke.](./media/er-components-inspections-06d.png)

#### <a name="option-2"></a>Asetus 2

Muuta **Suoritus**-kentän arvo **JoinedList**-tietolähteelle arvosta **Kysely** arvoksi **Muistissa**. Sellaisen taulun arvon muuttamista ei suositella, jossa on suuri tietomäärä (tapahtumataulu), koska kaikki tiedot haetaan ja yhdistäminen tehdään muistissa. Näin ollen tämä lähestymistapa voi heikentää suorituskykyä. Tästä riskistä ilmoitetaan oikeellisuustarkistusvaroituksen avulla.

## <a name="preferability-of-filter-vs-where-function"></a><a id="i7"></a>FILTER-funktion suositeltavuus WHERE-funktion asemesta

Sisäänrakennettua [FILTER](er-functions-list-filter.md)-ER-funktiota käytetään sovelluksen taulujen, näkymien tai tietoentiteettien käsittelyyn sijoittamalla yksittäinen SQL-kutsu hakemaan vaadittu tieto tietueluettelona. [WHERE ](er-functions-list-where.md)-funktio hakee kaikki tietyn lähteen tietueet ja suorittaa tietueiden valinnan muistissa. Tietolähdettä, jonka tyyppi on **Tietueluettelo**, käytetään molempien funktioiden argumenttina, ja se määrittää lähteen tietueiden haulle. ER tarkistaa, voidaanko suora SQL-kutsu määrittää tietolähteelle, johon viitataan **WHERE**-funktiossa. Jos suoraa kutsua ei voida määrittää, ER-mallin yhdistämismäärityksen suunnittelijassa ilmenee oikeellisuustarkistusvaroitus. Vastaanotettu sanoma suosittelee **FILTER**-funktion käyttöä **WHERE**-funktion asemesta suorituskyvyn parantamiseksi.

Seuraavissa vaiheissa näkyy, miten tämä ongelma voi ilmetä.

1. Aloita ER-mallin yhdistämismäärityskomponentin määrittäminen.
2. Lisää tietolähde, jonka tietotyyppi on **Dynamics 365 for Operations \\ -taulutietueet**.
3. Anna uudelle tietolähteelle nimeksi **Trans**. Valitse **Taulu**-kentässä **VendTrans** määrittääksesi, että tämä tietolähde pyytää VendTrans-taulua.
4. Lisää tietolähde, jonka tyyppi on **Laskettu kenttä** sisäkkäiseksi kentäksi **Vendor**-tietolähteeseen.
5. Anna uudelle tietolähteelle nimeksi **FilteredTrans** ja määritä se sisältämään lauseke `WHERE(Trans, Trans.AccountNum="US-101")`.
6. Lisää tietolähde, jonka tietotyyppi on **Dynamics 365 for Operations \\ -taulutietueet**.
7. Anna uudelle tietolähteelle nimeksi **Vendor**. Valitse **Taulu**-kentässä **VendTable** määrittämään, että tämä tietolähde pyytää VendTable-taulua.
8. Lisää tietolähde, jonka tietotyyppi on **Laskettu kenttä**.
9. Anna uudelle tietolähteelle nimeksi **FilteredVendor** ja määritä se sisältämään lauseke `WHERE(Vendor, Vendor.AccountNum="US-101")`.
10. Valitse **Oikeellisuustarkistus** tarkastellaksesi muokattavaa mallin yhdistämismäärityskomponenttia **Mallin yhdistämismäärityksen suunnittelija** -sivulla.

    ![Tarkastele muokattavaa mallin yhdistämismäärityskomponenttia Mallin yhdistämismäärityksen suunnittelija -sivulla.](./media/er-components-inspections-07a.png)

11. Huomaa, että oikeellisuustarkistusvaroitukset suosittelevat, että käytät **FILTER**-funktiota **WHERE**-funktion asemesta **FilteredVendor**- ja **FilteredTrans**-tietolähteille.

    ![Suositus käyttää FILTER-funktiota WHERE-funktion asemesta Mallin yhdistämismäärityksen suunnittelija -sivulla.](./media/er-components-inspections-07b.png)

### <a name="automatic-resolution"></a>Automaattinen ratkaisu

Valitse **Korjaa** korvataksesi automaattisesti **WHERE**-funktion **FILTER**-funktiolla kaikkien tietolähteiden lausekkeissa, jotka näkyvät ruudukossa **Varoitukset**-välilehdellä tämän tyyppiselle tarkistukselle.

Vaihtoehtoisesti voit valita ruudukon yksittäisen varoituksen rivin ja valita sitten **Korjaa valittu**. Tässä tapauksessa lauseketta muutetaan automaattisesti vain valitussa varoituksessa mainitussa tietolähteessä.

![Valitaan Korjaa, jotta korvataan WHERE-funktio automaattisesti FILTER-funktiolla Mallin yhdistämismäärityksen suunnittelija -sivulla.](./media/er-components-inspections-07c.png)

### <a name="manual-resolution"></a>Manuaalinen ratkaisu

Voit muokata lausekkeita kaikille tietolähteille oikeellisuustarkistusruudukossa korvaamalla **WHERE**-funktio **FILTER**-funktiolla.

## <a name="preferability-of-allitemsquery-vs-allitems-function"></a><a id="i8"></a>ALLITEMSQUERY-funktion suositeltavuus ALLIITEMS-funktion asemesta

Sisäänrakennetut [ALLITEMS](er-functions-list-allitems.md)- ja [ALLITEMSQUERY](er-functions-list-allitemsquery.md)-ER-funktiot palauttavat tasoitetun **Tietueluettelo**-arvon, jonka sisältämä tietueluettelo edustaa kaikkia määritettyä polkua vastaavia nimikkeitä. ER tarkistaa, voidaanko suora SQL-kutsu määrittää tietolähteelle, johon viitataan **ALLITEMS**-funktiossa. Jos suoraa kutsua ei voida määrittää, ER-mallin yhdistämismäärityksen suunnittelijassa ilmenee oikeellisuustarkistusvaroitus. Vastaanotettu sanoma suosittelee **ALLITEMSQUERY**-funktion käyttöä **ALLITEMS**-funktion asemesta suorituskyvyn parantamiseksi.

Seuraavissa vaiheissa näkyy, miten tämä ongelma voi ilmetä.

1. Aloita ER-mallin yhdistämismäärityskomponentin määrittäminen.
2. Lisää tietolähde, jonka tietotyyppi on **Dynamics 365 for Operations \\ -taulutietueet**.
3. Anna uudelle tietolähteelle nimeksi **Vendor**. Valitse **Taulu**-kentässä **VendTable** määrittämään, että tämä tietolähde pyytää VendTable-taulua.
4. Lisää **Laskettu kenttä** -tyyppinen tietolähde hakeaksesi tietueet useille toimittajille.
5. Anna uudelle tietolähteelle nimeksi **FilteredVendor** ja määritä se sisältämään lauseke `FILTER(Vendor, OR(Vendor.AccountNum="US-101",Vendor.AccountNum="US-102"))`.
6. Lisää **Laskettu kenttä** -tyyppinen tietolähde hakeaksesi tapahtumat kaikille suodatetuille toimittajille.
7. Anna uudelle tietolähteelle nimeksi **FilteredVendorTrans** ja määritä se sisältämään lauseke `ALLITEMS(FilteredVendor.'<Relations'.'VendTrans.VendTable_AccountNum')`.
8. Valitse **Oikeellisuustarkistus** tarkastellaksesi muokattavaa mallin yhdistämismäärityskomponenttia **Mallin yhdistämismäärityksen suunnittelija** -sivulla.

    ![Tarkastetaan muokattavaa mallin yhdistämismäärityskomponenttia Mallin yhdistämismäärityksen suunnittelija -sivulla.](./media/er-components-inspections-08a.png)

9. Huomaa, että oikeellisuustarkistusvaroitus ilmenee. Sanoma suosittelee **ALLITEMSQUERY**-funktion käyttämistä **ALLITEMS**-funktion asemesta **FilteredVendorTrans**-tietolähteelle.

    ![Suositus käyttää ALLITEMSQUERY-funktiota ALLITEMS-funktion asemesta Mallin yhdistämismäärityksen suunnittelija -sivulla.](./media/er-components-inspections-08b.png)

### <a name="automatic-resolution"></a>Automaattinen ratkaisu

Valitse **Korjaa** korvataksesi automaattisesti **ALLITEMS**-funktion **ALLITEMSQUERY**-funktiolla kaikkien tietolähteiden lausekkeissa, jotka näkyvät ruudukossa **Varoitukset**-välilehdellä tämän tyyppiselle tarkistukselle.

Vaihtoehtoisesti voit valita ruudukon yksittäisen varoituksen rivin ja valita sitten **Korjaa valittu**. Tässä tapauksessa lauseketta muutetaan automaattisesti vain valitussa varoituksessa mainitussa tietolähteessä.

![Valitaan Korjaa valitut Mallin yhdistämismäärityksen suunnittelija -sivulla.](./media/er-components-inspections-08c.png)

### <a name="manual-resolution"></a>Manuaalinen ratkaisu

Voit muokata lausekkeita kaikille tietolähteille, jotka on mainittu oikeellisuustarkistusruudukossa korvaamalla **ALLITEMS**-funktion **ALLITEMSQUERY**-funktiolla.

## <a name="consideration-of-empty-list-cases"></a><a id="i9"></a>Tyhjien luettelotapausten käsittely

Voit määrittää ER-muodon tai mallin yhdistämismäärityskomponentin hakemaan tietolähdekentän arvon, jonka tyyppi on **Tietueluettelo**. ER tarkistaa, otetaanko suunnittelussa huomioon tapausta, jossa kutsutulla tietolähteellä ei ole tietueita (eli se on tyhjä), jotta suorituksenaikaiset virheet voidaan estää, kun arvo haetaan tietueesta, jota ei ole.

Seuraavissa vaiheissa näkyy, miten tämä ongelma voi ilmetä.

1. Aloita ER-tietomallin, ER-mallin yhdistämismäärityksen ja ER-muodon komponenttien määrittäminen samanaikaisesti.
2. Lisää tietomalli puuhun juurinimike, jonka nimi on **Root3**.
3. Muokkaa **Root3**-nimikettä lisäämällä sisäkkäinen nimike, jonka tyyppi on **Tietueluettelo**.
4. Anna uudelle sisäkkäiselle nimikkeelle nimeksi **Vendor**.
5. Muokkaa **Vendor**-nimikettä seuraavalla tavalla:

    - Lisää sisäkkäinen kenttä, jonka tyyppi on **Merkkijono** ja anna sille nimeksi **Name**.
    - Lisää sisäkkäinen kenttä, jonka tyyppi on **Merkkijono** ja anna sille nimeksi **AccountNumber**.

    ![Sisäkkäisten kenttien lisääminen Tietomalli-sivulle.](./media/er-components-inspections-09a.png)

6. Lisää mallin yhdistämismäärityksen suunnitteluohjelman **Tietolähteet**-ruudussa tietolähde, jonka tyyppi on **Dynamics 365 for Operations \\ Taulukkotietueet**.
7. Anna uudelle tietolähteelle nimeksi **Vendor**. Valitse **Taulu**-kentässä **VendTable** määrittämään, että tämä tietolähde pyytää VendTable-taulua.
8. Lisää tietolähde, jonka tyyppi on **Yleinen \\ Käyttäjän syöteparametri** hakeaksesi toimittajan tilin suorituksenaikaisessa dialogiruudussa.
9. Anna uudelle tietolähteelle nimeksi **RequestedAccountNum**. Lisää **Selite**-kenttään **Toimittajan tilinumero**. Jätä **Toiminnon tietotyypin nimi** -kenttään oletusarvo **Kuvaus**.
10. Lisää **Laskettu kenttä** -tyyppinen tietolähde suodattaaksesi toimittajan, jota haetaan.
11. Anna uudelle tietolähteelle nimeksi **FilteredVendor** ja määritä se sisältämään lauseke `FILTER(Vendor, Vendor.AccountNum=RequestedAccountNum)`.
12. Sido tietomallin nimikkeet määritettyihin tietolähteisiin seuraavasti:

    - Sido **FilteredVendor** kohteeseen **Vendor**.
    - Sido **FilteredVendor.AccountNum** kohteeseen **Vendor.AccountNumber**.
    - Sido **FilteredVendor.'name()'** kohteeseen **Vendor.Name**.

    ![Tietomallin nimikkeiden sitominen Mallin yhdistämismäärityksen suunnittelija -sivulla.](./media/er-components-inspections-09b.png)

13. Luo muotorakenteen puussa seuraavat nimikkeet, jos haluat luoda XML-muodossa olevan lähtevän asiakirjan, joka sisältää toimittajan tiedot:

    1. Lisää XML-juurielementti **Lauseke**.
    2. Lisää XML-elementille **Lauseke** sisäkkäinen XML-elementti **Osapuoli**.
    3. Lisää seuraavat sisäkkäiset XML-määritteet XML-elementille **Osapuoli**.

        - Nimi
        - AccountNum

14. Sido muotoelementit annettuihin tietolähteisiin seuraavalla tavalla:

    - Sido muotoelementti **Lauseke\\Osapuoli\\Nimi** tietolähdekenttään **model.Vendor.Name**.
    - Sido muotoelementti **Lauseke\\Osapuoli\\AccountNum** tietolähdekenttään **model.Vendor.AccountNumber**.

15. Valitse **Oikeellisuustarkistus** tarkastellaksesi muokattavaa muotokomponenttia **Muodon suunnittelija** -sivulla.

    ![Suoritetaan oikeellisuustarkistusta muotoelementeille, jotka sidottiin tietolähteisiin Muodon suunnittelija -sivulla.](./media/er-components-inspections-09c.png)

16. Huomaa, että vahvistusvirhe ilmenee. Sanoma ilmoittaa, että määritetylle **Lauseke\\Osapuoli\\Nimi**- ja **Lauseke\\Osapuoli\\AccountNum**-muotokomponenteille saatetaan luoda virhe suorituksen aikana, jos `model.Vendor`-luettelo on tyhjä.

    ![Oikeellisuustarkistuksen virhe, joka ilmoittaa mahdollisesta virheestä määritetyissä muotokomponenteissa.](./media/er-components-inspections-09d.png)

Seuraavassa kuvassa näkyy suorituksenaikainen virhe, joka tapahtuu, jos ohitat varoituksen ja valitset **Suorita** suorittaaksesi muodon ja valitset olemattoman toimittajan tilinumeron. Koska pyydettyä toimittajaa ei ole, `model.Vendor`-luettelo on tyhjä (se ei sisällä yhtään tietuetta).

![Suorituksenaikaiset virheet, jotka tapahtuivat muodon yhdistymismäärityksen suorituksessa.](./media/er-components-inspections-09e.png)

### <a name="automatic-resolution"></a>Automaattinen ratkaisu

Voit valita **Varoitukset**-välilehden ruudukossa valitulle riville **Pura sidonta**. Sidonta, joka osoittaa **Polku**-sarakkeeseen, poistetaan automaattisesti muotoelementeistä.

### <a name="manual-resolution"></a>Manuaalinen ratkaisu

#### <a name="option-1"></a>Asetus 1

Voit sitoa muotoelementin **Lauseke\\Osapuoli\\Nimi** tietolähdenimikkeeseen `model.Vendor`. Suorituksen aikana tämä sidonta kutsuu ensin tietolähdettä `model.Vendor`. Kun `model.Vendor` palauttaa tyhjän tietueluettelon, sisäkkäiset muotoelementit eivät toimi. Tämän vuoksi tässä muotomäärityksessä ei tapahtu oikeellisuustarkistusvaroituksia.

![Sidotaan muotoelementtiä tietolähdenimikkeeseen Muodon suunnittelija -sivulla.](./media/er-components-inspections-09e.gif)

#### <a name="option-2"></a>Asetus 2

Muuta muotoelementin **Lauseke\\Osapuoli\\Nimi** sidonta arvosta `model.Vendor.Name` arvoksi `FIRSTORNULL(model.Vendor).Name`. Päivitetty sidonta muuntaa ehdollisesti tietolähteen `model.Vendor` ensimmäisen tietueen tyypin tietolähteen, jonka tyyppi on **Tietueluettelo**, uudeksi tietolähteeksi, jonka tyyppi on **Tietue**. Tämä uusi tietolähde sisältää saman kenttäjoukon.

- Jos tietolähteessä `model.Vendor` on käytettävissä vähintään yksi tietue, kyseisen tietueen kentät täytetään ensimmäisen `model.Vendor`-tietolähteen tietueen arvoilla. Tässä tapauksessa päivitetty sidonta palauttaa toimittajan nimen.
- Muussa tapauksissa kaikki luotavan tietueen kentät täytetään kentän tietotyypin oletusarvoilla. Tässä tapauksessa tyhjä merkkijono palautetaan **Merkkijono**-tietotyypin oletusarvona.

Täten oikeellisuustarkistusvaroituksia ei synny **Lauseke\\Osapuoli\\Nimi**-muotoelementille, kun se on sidottu lausekkeeseen `FIRSTORNULL(model.Vendor).Name`.

![Muutettu sidonta ratkaisee oikeellisuuden tarkistusvaroitukset Muodon suunnittelu -sivulla.](./media/er-components-inspections-09f.gif)

#### <a name="option-3"></a>Asetus 3

Jos haluat eksplisiittisesti määrittää tiedot, jotka annetaan luotuun asiakirjaan, kun tietolähde `model.Vendor`, jonka tietotyyppi on **Tietueluettelo** ei palauta arvoja (tässä esimerkissä tekstin **Not available**), muuta muotoelementin **Lauseke\\Osapuoli\\Nimi** sidonta arvosta `model.Vendor.Name` arvoksi `IF(NOT(ISEMPTY(model.Vendor)), model.Vendor.Name, "Not available")`. Voit myös käyttää lauseketta `IF(COUNT(model.Vendor)=0, model.Vendor.Name, "Not available")`.

### <a name="additional-consideration"></a><a id="i9a"></a>Lisähuomioita

Tarkastus myös varoittaa toisesta mahdollisesta ongelmasta. Oletusarvoisesti sidottaessa **Lauseke\\Osapuoli\\Nimi**- ja **Lauseke\\Osapuoli\\AccountNum**-muotoelementit tietolähteeseen `model.Vendor`, jonka tietotyyppi on **Tietueluettelo**, kyseiset sidonnat suoritetaan ja ne hakevat soveltuvien kenttien arvot tietolähteestä `model.Vendor`, jos kyseinen luettelo ei ole tyhjä.

Koska muotoelementtiä **Lauseke\\Osapuoli** ei ole sidottu tietolähteeseen `model.Vendor`, **Lauseke\\Osapuoli**-elementtiä ei toisteta jokaiselle tietueelle tietolähteessä `model.Vendor` muodon suorittamisen aikana. Sen sijaan luotu asiakirja täytetään ainoastaan tietueluettelon ensimmäisen tietueen tiedoilla, jos luettelossa on useita tietueita. Tämän vuoksi, jos muodon on tarkoitus täyttää luotu asiakirja kaikkien `model.Vendor`-tietolähteen toimittajien tiedoilla, voi syntyä ongelma. Korjaa ongelma sitomalla **Lauseke\\Osapuoli**-elementti tietolähteeseen `model.Vendor`.

## <a name="executability-of-an-expression-with-filter-function-caching"></a><a id="i10"></a>FILTER-funktion sisältävän lausekkeen suoritettavuus (välimuistin käyttö)

Useita sisäänrakennettuja ER-funktioita, kuten [FILTER](er-functions-list-filter.md)- ja [ALLITEMSQUERY](er-functions-list-allitemsquery.md)-funktioita, käytetään sovellustaulujen, näkymien tai tietoentiteettien käyttämiseen sijoittamalla yksittäinen SQL-kutsu tietojen hakemiseksi tietueluettelona. Tietolähdettä, jonka tyyppi on **Tietueluettelo**, käytetään kunkin tällaisen funktion argumenttina, ja se määrittää sovelluslähteen kutsulle. ER tarkistaa, voidaanko suora SQL-kutsu määrittää tietolähteelle, johon viitataan tällaisessa funktiossa. Jos suoraa kutsua ei voida toteuttaa, koska tiedolähde on merkitty [välimuistiin vietäväksi](trace-execution-er-troubleshoot-perf.md#improve-the-model-mapping-based-on-information-from-the-execution-trace), ER-mallin yhdistämismäärityksen suunnittelijassa tapahtuu virhe. Vastaanotettu sanoma ilmoittaa, että ER-lauseketta, joka sisältää yhden näistä funktioista, ei voida suorittaa suorituksen aikana.

Seuraavissa vaiheissa näkyy, miten tämä ongelma voi ilmetä.

1. Aloita ER-mallin yhdistämismäärityskomponentin määrittäminen.
2. Lisää tietolähde, jonka tietotyyppi on **Dynamics 365 for Operations \\ -taulutietueet**.
3. Anna uudelle tietolähteelle nimeksi **Vendor**. Valitse **Taulu**-kentässä **VendTable** määrittämään, että tämä tietolähde pyytää VendTable-taulua.
4. Lisää tietolähde, jonka tyyppi on **Yleinen \\ Käyttäjän syöteparametri** hakeaksesi toimittajan tilin suorituksenaikaisessa dialogiruudussa.
5. Anna uudelle tietolähteelle nimeksi **RequestedAccountNum**. Lisää **Selite**-kenttään **Toimittajan tilinumero**. Jätä **Toiminnon tietotyypin nimi** -kenttään oletusarvo **Kuvaus**.
6. Lisää **Laskettu kenttä** -tyyppinen tietolähde suodattaaksesi toimittajan, jota haetaan.
7. Anna uudelle tietolähteelle nimeksi **FilteredVendor** ja määritä se sisältämään lauseke `FILTER(Vendor, Vendor.AccountNum=RequestedAccountNum)`.
8. Merkitse määritetty **Vendor**-tietolähde vietäväksi välimuistiin.

    ![Määritetään mallin yhdistämismäärityskomponentti Mallin yhdistämismäärityksen suunnittelija -sivulla.](./media/er-components-inspections-10a.gif)

9. Valitse **Oikeellisuustarkistus** tarkastellaksesi muokattavaa mallin yhdistämismäärityskomponenttia **Mallin yhdistämismäärityksen suunnittelija** -sivulla.

    ![Suoritetaan oikeellisuustarkistus FILTER-funktiolle, jota käytetään välimuistin Toimittaja-tietolähteelle Mallin yhdistämismääritysten suunnittelija -sivulla.](./media/er-components-inspections-10a.png)

10. Huomaa, että vahvistusvirhe ilmenee. Sanomassa ilmoitetaan, että **FILTER**-funktiota ei voi käyttää välimuistiin viedyssä tietolähteessä **Toimittaja**.

Seuraavassa kuvassa näkyy suorituksenaikainen virhe, joka ilmenee, jos ohitat varoituksen ja valitset **Suorita** suorittaaksesi muodon.

![Suorituksenaikainen virhe joka ilmenee, kun Muodon suunnittelija -sivulla suoritetaan muodon yhdistämismääritykset.](./media/er-components-inspections-10b.png)

### <a name="automatic-resolution&quot;></a>Automaattinen ratkaisu

Tätä ongelmaa ei voi korjata automaattisesti.

### <a name=&quot;manual-resolution&quot;></a>Manuaalinen ratkaisu

#### <a name=&quot;option-1&quot;></a>Asetus 1

Poista **Välimuisti**-merkintä **Vendor**-tietolähteestä. Tietolähde **FilteredVendor** muuttuu silloin suorituskelpoiseksi, mutta tietolähdettä **Vendor** , johon viitataan taulussa VendTable table käytetään joka kerta, kun tietolähdettä **FilteredVendor** kutsutaan.

#### <a name=&quot;option-2&quot;></a>Asetus 2

Muuta tietolähteen **FilteredVendor** lauseke arvosta `FILTER(Vendor, Vendor.AccountNum=&quot;US-101")` arvoksi `WHERE(Vendor, Vendor.AccountNum="US-101")`. Tässä tapauksessa tietolähdettä **Vendor**, johon viitataan VendTable-taulussa, käytetään ainoastaan, kun tietolähdettä **Vendor** kutsutaan ensimmäisen kerran. Tietueiden valinta tapahtuu kuitenkin muistissa. Näin ollen tämä lähestymistapa voi heikentää suorituskykyä.

## <a name="missing-binding"></a><a id="i11"></a>Puuttuva sidonta

ER-muotokomponenttia määritettäessä perus-ER-tietomallia tarjotaan oletusarvoiseksi tietolähteeksi ER-muodolle. Kun konfiguroitu ER-muoto suoritetaan, [oletusarvoista mallin yhdistämismääritystä](er-country-dependent-model-mapping.md) perusmallista käytetään tietomallin täyttämiseen sovellustiedoilla. ER-muodon suunnittelija näyttää varoituksen, jos muotoelementti sidotaan tietomallin nimikkeeseen, jota ei ole sidottu mihinkään tietolähteeseen mallin yhdistämismäärityksessä, joka on valittu oletusarvoiseksi mallin yhdistämismääritykseksi muokattavalle muodolle. Tämän tyyppistä sidontaa ei voi suorittaa suorituksen aikana, koska muoto, joka suoritetaan, ei voi täyttää sidottua elementtiä sovellustiedoilla. Tämän vuoksi suorituksen aikana tapahtuu virhe.

Seuraavissa vaiheissa näkyy, miten tämä ongelma voi ilmetä.

1. Aloita ER-tietomallin, ER-mallin yhdistämismäärityksen ja ER-muodon komponenttien määrittäminen samanaikaisesti.
2. Lisää tietomalli puuhun juurinimike, jonka nimi on **Root3**.
3. Muokkaa **Root3**-nimikettä lisäämällä uusi sisäkkäinen nimike, jonka tyyppi on **Tietueluettelo**.
4. Anna uudelle sisäkkäiselle nimikkeelle nimeksi **Vendor**.
5. Muokkaa **Vendor**-nimikettä seuraavalla tavalla:

    - Lisää sisäkkäinen kenttä, jonka tyyppi on **Merkkijono** ja anna sille nimeksi **Name**.
    - Lisää sisäkkäinen kenttä, jonka tyyppi on **Merkkijono** ja anna sille nimeksi **AccountNumber**.

    ![Sisäkkäisten kenttien lisääminen Toimittaja-nimikkeeseen Tietomalli-sivulla.](./media/er-components-inspections-11a.png)

6. Lisää mallin yhdistämismäärityksen suunnitteluohjelman **Tietolähteet**-ruudussa tietolähde, jonka tyyppi on **Dynamics 365 for Operations \\ Taulukkotietueet**.
7. Anna uudelle tietolähteelle nimeksi **Vendor**. Valitse **Taulu**-kentässä **VendTable** määrittämään, että tämä tietolähde pyytää VendTable-taulua.
8. Lisää tietolähde, jonka tyyppi on **Yleinen \\ Käyttäjän syöteparametri** hakeaksesi toimittajan tiliä suorituksenaikaisessa dialogiruudussa.
9. Anna uudelle tietolähteelle nimeksi **RequestedAccountNum**. Lisää **Selite**-kenttään **Toimittajan tilinumero**. Jätä **Toiminnon tietotyypin nimi** -kenttään oletusarvo **Kuvaus**.
10. Lisää **Laskettu kenttä** -tyyppinen tietolähde suodattaaksesi toimittajan, jota haetaan.
11. Anna uudelle tietolähteelle nimeksi **FilteredVendor** ja määritä se sisältämään lauseke `FILTER(Vendor, Vendor.AccountNum=RequestedAccountNum)`.
12. Sido tietomallin nimikkeet määritettyihin tietolähteisiin seuraavasti:

    - Sido **FilteredVendor** kohteeseen **Vendor**.
    - Sido **FilteredVendor.AccountNum** kohteeseen **Vendor.AccountNumber**.

    > [!NOTE]
    > **Vendor.Name** -tietomallikenttä säilyy ei-sidottuna.

    ![Tietomallinimikkeet, jotka on sidottu määritettyihin tietolähteisiin ja tietomallinimike, joka säilyy sitomattomana Mallin yhdistämismääritysten suunnittelija -sivulla.](./media/er-components-inspections-11b.png)

13. Luo muotorakenteen puussa seuraavat nimikkeet, jos haluat luoda XML-muodossa olevan lähtevän asiakirjan, joka sisältää kyseltyjen toimittajien tiedot:

    1. Lisää XML-juurielementti **Lauseke**.
    2. Lisää XML-elementille **Lauseke** sisäkkäinen XML-elementti **Osapuoli**.
    3. Lisää seuraavat sisäkkäiset XML-määritteet XML-elementille **Osapuoli**.

        - Nimi
        - AccountNum

14. Sido muotoelementit annettuihin tietolähteisiin seuraavalla tavalla:

    - Sido **Lauseke\\Osapuoli**-muotoelementti `model.Vendor`-tietolähdenimikkeeseen.
    - Sido muotoelementti **Lauseke\\Osapuoli\\Nimi** tietolähdekenttään **model.Vendor.Name**.
    - Sido muotoelementti **Lauseke\\Osapuoli\\AccountNum** tietolähdekenttään **model.Vendor.AccountNumber**.

15. Valitse **Oikeellisuustarkistus** tarkastellaksesi muokattavaa muotokomponenttia **Muodon suunnittelija** -sivulla.

    ![Muotokomponentin oikeellisuustarkistus Muodon suunnittelija -sivulla.](./media/er-components-inspections-11c.png)

16. Huomaa, että oikeellisuustarkistusvaroitus ilmenee. Sanoma ilmaisee, että **model.Vendor.Name**-tietolähdekenttää ei ole sidottu mallin yhdistämismäärityksessä mihinkään tietolähteeseen, joka on määritetty muodon käyttöön. Tämän vuoksi muotoelementtiä **Lauseke\\Osapuoli\\Nimi** ei ehkä täytetä suorituksen aikana. Tällöin voi ilmetä suorituksenaikainen poikkeus.

    ![ER-muotokomponentin oikeellisuustarkistus Muodon suunnittelija -sivulla.](./media/er-components-inspections-11d.png)

Seuraavassa kuvassa näkyy suorituksenaikainen virhe, joka ilmenee, jos ohitat varoituksen ja valitset **Suorita** suorittaaksesi muodon.

![Muokattavan muodon suoritus Muodon suunnittelija -sivulla.](./media/er-components-inspections-11e.png)

### <a name="automatic-resolution"></a>Automaattinen ratkaisu

Tätä ongelmaa ei voi korjata automaattisesti.

### <a name="manual-resolution"></a>Manuaalinen ratkaisu

#### <a name="option-1"></a>Asetus 1

Muokkaa määritettyä mallin yhdistämismääritystä lisäämällä sidonta tietolähdekenttään **model.Vendor.Name**.

#### <a name="option-2"></a>Asetus 2

Muokkaa määritettyä muotoa poistamalla sidonta muodotelementistä **Lauseke\\Osapuoli\\Nimi**.

## <a name="not-linked-template"></a><a id="i12"></a>Ei linkitetty malli

Kun määrität [manuaalisesti](er-fillable-excel.md#manual-entry) ER-muotokomponentin käyttämään mallia lähtevän asiakirjan luomiseen, sinun on manuaalisesti lisättävä **Excel\\Tiedosto**-elementti, lisättävä vaadittu malli muokattavan komponentin liitteeksi ja valittava kyseinen liite lisätyssä **Excel\\Tiedosto**-elementissä. Tällä tavoin voit määrittää, että lisätty elementti täyttää valitun mallin suorituksen aikana. Kun määrität muotokomponentin version **Luonnos** [tilassa](general-electronic-reporting.md#component-versioning), saatat lisätä useita malleja muokattavaan komponenttiin ja sitten valita kunkin mallin **Excel\\Tiedosto**-elementissä suorittamaan ER-muodon. Näin voit nähdä, miten eri mallit täytetään suorituksen aikana. Jos sinulla on malleja, joita ei ole valittu missään **Excel\\Tiedosto**-elementissä, ER-muodon suunnittelija varoittaa, että kyseiset mallit poistetaan muokattavan ER-muodon komponenttiversiosta ,kun sen tila muutetaan arvosta **Luonnos** arvoksi **Valmis**.

Seuraavissa vaiheissa näkyy, miten tämä ongelma voi ilmetä.

1. Aloita ER-muotokomponentin määrittäminen.
2. Lisää muodon rakennepuussa **Excel\\Tiedosto**-elementti.
3. Lisää juuri lisäämällesi **Excel\\Tiedosto**-elementille liitteeksi Excel-työkirjatiedosto **A.xlsx**. Käytä asiakirjatyyppiä, joka on määritetty [ER-parametreissa](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) määrittämään ER-muotomallien tallennustilan.
4. Lisää **Excel\\Tiedosto**-elementille liitteeksi toinen Excel-työkirjatiedosto **B.xlsx**. Käytä samaa asiakirjatyyppiä, jota käytetään työkirjatiedostolle A.
5. Valitse **Excel\\Tiedosto**-elementissä työkirjatiedosto A.
6. Valitse **Oikeellisuustarkistus** tarkastellaksesi muokattavaa muotokomponenttia **Muodon suunnittelija** -sivulla.

    ![Työkirjatiedoston muokattavan muotokomponentin oikeellisuustarkistus Muodon suunnittelija -sivulla.](./media/er-components-inspections-12a.gif)

7. Huomaa, että oikeellisuustarkistusvaroitus ilmenee. Sanomassa ilmoitetaan, että työkirjatiedostoa B. xlsx ei ole linkitetty mihinkään komponenttiin ja että se poistetaan sen jälkeen, kun määritysversion tila on muutettu.

### <a name="automatic-resolution"></a>Automaattinen ratkaisu

Tätä ongelmaa ei voi korjata automaattisesti.

### <a name="manual-resolution"></a>Manuaalinen ratkaisu

Muokkaa määritettyä muotoa poistamalla kaikki mallit, joita ei ole linkitetty mihinkään **Excel\\Tiedosto**-elementtiin.

## <a name="not-synced-format"></a><a id="i13"></a>Ei synkronoitu muoto

Kun [määrität](er-fillable-excel.md) ER-muotokomponentin käyttämään Excel-mallia lähtevän asiakirjan luomiseen, voit lisätä manuaalisesti **Excel\\Tiedosto**-elementin, lisätä vaaditun mallin muokattavan komponentin liitteeksi ja valita kyseisen liitteen lisätyssä **Excel\\Tiedosto**-elementissä. Tällä tavoin voit määrittää, että lisätty elementti täyttää valitun mallin suorituksen aikana. Koska lisätty Excel-malli on suunniteltu ulkoisesti, muokattava ER-muoto voi sisältää Excelin nimiä, jotka puuttuvat lisätystä mallista. ER-muodon suunnittelija varoittaa mahdollisista epäjohdonmukaisuuksista ER-muodon elementeissä, jotka viittaavat nimiin, joita ei ole sisällytetty lisättyyn Excel-malliin.

Seuraavissa vaiheissa näkyy, miten tämä ongelma voi ilmetä.

1. Aloita ER-muotokomponentin määrittäminen.
2. Lisää muodon rakennepuussa **Excel\\Tiedosto**-elementti **Raportti**.
3. Lisää juuri lisäämällesi **Excel\\Tiedosto**-elementille liitteeksi Excel-työkirjatiedosto **A.xlsx**. Käytä asiakirjatyyppiä, joka on määritetty [ER-parametreissa](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) määrittämään ER-muotomallien tallennustilan.

    > [!IMPORTANT]
    > Varmista, että lisätty Excel-työkirja ei sisällä nimeä **ReportTitle**.

4. Lisää **Excel\\Solu**-elementti **Otsikko** sisäkkäiseksi elementiksi **Raportti**-elementtiin. Kirjoita **Excel-alue**-kenttään **ReportTitle**.
5. Valitse **Oikeellisuustarkistus** tarkastellaksesi muokattavaa muotokomponenttia **Muodon suunnittelija** -sivulla.

    ![Suoritetaan oikeellisuustarkistusta sisäkkäisille elementeille ja kentille Muodon suunnittelija -sivulla.](./media/er-components-inspections-13a.png)

6. Huomaa, että oikeellisuustarkistusvaroitus ilmenee. Viestissä todetaan, että nimeä **ReportTitle** ei ole olemassa taulukossa **Sheet1** käyttämässäsi Excel-mallissa.

    ![Oikeellisuustarkistusvaroitus, jonka mukaan nimeä ReportTitle ei ole Excel-mallin taulukossa Sheet1.](./media/er-components-inspections-13b.png)

### <a name="automatic-resolution"></a>Automaattinen ratkaisu

Tätä ongelmaa ei voi korjata automaattisesti.

### <a name="manual-resolution"></a>Manuaalinen ratkaisu

#### <a name="option-1"></a>Asetus 1

Muokkaa määritettyä muotoa poistamalla kaikki elementit, jotka viittaavat Excelin nimiin, jotka puuttuvat mallista.

#### <a name="option-2"></a>Asetus 2

[Päivitä](er-fillable-excel.md#template-import) muokattavaa ER-muotoa tuomalla Excel-malli. Muokattavan ER-muodon rakenne [synkronoidaan](modify-electronic-reporting-format-reapply-excel-template.md) tuodun Excel-mallin rakenteen kanssa.

### <a name="additional-consideration"></a>Lisähuomioita

Lisätietoja siitä, kuinka muodon rakenne voidaan synkronoida ER-mallin kanssa [Liiketoiminta-asiakirjojen hallinnan](er-business-document-management.md) mallieditorissa on kohdassa [Liiketoiminta-asiakirjan mallin rakenteen päivittäminen](er-bdm-update-structure.md).

## <a name="not-synced-with-a-word-template-format"></a><a id="i14"></a>Ei synkronoida Word-mallimuodon kanssa

Kun [määrität](er-fillable-excel.md) ER-muotokomponentin käyttämään Word-mallia lähtevän asiakirjan luomiseen, voit lisätä manuaalisesti **Excel\\Tiedosto**-elementin, lisätä vaaditun Word-mallin muokattavan komponentin liitteeksi ja valita kyseisen liitteen lisätyssä **Excel\\Tiedosto**-elementissä.

> [!NOTE]
> Kun Word-asiakirja on liitetty, ER-muodon suunnittelutoiminto näyttää muokattavissa olevan elementin seuraavasti: **Word\\Tiedosto**.

Tällä tavoin voit määrittää, että lisätty elementti täyttää valitun mallin suorituksen aikana. Koska lisätty Word-malli on suunniteltu ulkoisesti, muokattava ER-muoto voi sisältää viittauksia Wrd-sisällön ohjausobjekteihin, jotka puuttuvat lisätystä mallista. ER-muodon suunnittelija varoittaa mahdollisista epäjohdonmukaisuuksista ER-muodon elementeissä, jotka viittaavat sisällön ohjausobjekteihin, joita ei ole sisällytetty lisättyyn Word-malliin.

Esimerkki siitä, miten tämä ongelma saattaa ilmetä, on kohdassa [Konfiguroi muokattavissa oleva muoto piilottamaabn yhteenveto-osa](er-design-configuration-word-suppress-controls.md#configure-to-suppress-control).

### <a name="automatic-resolution"></a>Automaattinen ratkaisu

Tätä ongelmaa ei voi korjata automaattisesti.

### <a name="manual-resolution"></a>Manuaalinen ratkaisu

#### <a name="option-1"></a>Asetus 1

Muokkaa konfiguroitua muotoa poistamalla **Poistettu**-kaava oikeellisuustarkistuksen varoituksessa mainitusta muotoelementistä.

#### <a name="option-2"></a>Asetus 2

Muokkaa käytettyä Word-malli [lisäämällä](er-design-configuration-word-suppress-controls.md#tag-control) vaadittu tunniste asiaankuuluvaan Word-sisällön ohjausobjektiin.

## <a name="no-default-mapping"></a><a id="i15"></a>Ei oletusmääritystä

Kun [Puuttuvat sitovat](#i11) tarkastus suoritetaan, tarkastetut muodon sidonnat arvioidaan asiaankuuluvan mallimäärityskomponentin sidosten perusteella. Koska voit tuoda Finance-esiintymään [useita](./tasks/er-manage-model-mapping-configurations-july-2017.md) ER-mallin määrityskonfiguraatioita ja kukin konfiguraatio saattaa sisältää sovellettavan mallimäärityskomponenti, sinun on valittava yksi konfiguraatio oletuskonfiguraatioksi. Muutoin, jos yrität suorittaa, muokata tai tarkistaa tarkan ER-muodon, tulee poikkeus ja saat seuraavan sanoman: "\<model name (root descriptor)\> -tietomallille on olemassa useita mallimäärityksiä konfiguroinneissa \<configuration names separated by comma\>. Määritä jokin määrityksistä oletukseksi."

Esimerkki siitä, miten tämä ongelma saattaa ilmetä ja miten ongelma voidaan korjata, on kohdassa [Useiden johdettujen yhdistämismääritysten hallinta yksittäiselle mallin juurelle](er-multiple-model-mappings.md).

## <a name="inconsistent-setting-of-header-or-footer-components"></a><a id="i16"></a>Ylä- tai alatunnistekomponenttien määrittäminen on ristiriidassa

Kun [konfiguroit](er-fillable-excel.md) ER-muotokomponentin käyttämään Excel-mallia lähtevien tiedostojen luomiseen, voit lisätä **Excel\\Otsikko** -osan Excel-työkirjan laskentataulukon yläosan otsikoiden täyttämiseksi. Voit myös lisätä **Excel\\Alatunniste** -osan joka täyttää laskentataulukon alaosan alatunnisteet. Määritä sivut, joita varten komponentti suoritetaan, määrittämällä **Otsikon/alatunnisteen ulkoasu** -ominaisuus jokaiselle lisättävälle **Excel\\Otsikko**- tai **Excel\\Alatunniste** -osalle. Koska yhdelle **Laskentataulukko**-komponentille voi konfiguroida useita **Excel\\ Otsikko**- tai **Excel\\Alatunniste**-osia ja voit luoda erilaisia otsikoita tai alatunnisteita Excel-laskentataulukon eri sivutyypeille, sinun on määritettävä yksi **Excel\\Otsikko**- tai **Excel\\Alatunniste**-osa tietylle **Otsikon/alatunnisteen ulkoasu** -ominaisuuden arvolle. Jos useita **Excel\\Otsikko**- tai **Excel\\Alatunniste** -osia on määritetty tietylle **Otsikon/alatunnisteen ulkoasu** -ominaisuuden arvolle, näkyviin tulee oikeellisuustarkistusvirhe. Näyttöön tulee seuraava virhesanoma: "Otsikot/alatunnisteet (&lt;component type: Header or Footer&gt;) ovat ristiriidassa".

### <a name="automatic-resolution"></a>Automaattinen ratkaisu

Tätä ongelmaa ei voi korjata automaattisesti.

### <a name="manual-resolution"></a>Manuaalinen ratkaisu

#### <a name="option-1"></a>Asetus 1

Voit muokata konfiguroitua muotoa poistamalla yhden ristiriitaisista **Excel\\Otsikko**- tai **Excel\\Alatunniste**-osista.

#### <a name="option-2"></a>Asetus 2

Muokkaa yhden ristiriitaisen **Excel\\Otsikko**- tai **Excel\\Alatunniste**-osan **Otsikon/alatunnisteen ulkoasu** -ominaisuutta.

## <a name="additional-resources"></a>Lisäresurssit

[ALLITEMS ER-funktio](er-functions-list-allitems.md)

[ALLITEMSQUERY ER-funktio](er-functions-list-allitemsquery.md)

[INT64VALUE ER -funktio](er-functions-conversion-int64value.md)

[INTVALUE ER -funktio](er-functions-conversion-intvalue.md)

[FILTER ER-toiminto](er-functions-list-filter.md)

[WHERE ER-funktio](er-functions-list-where.md)

[Käytä JOIN-tietolähteitä tietojen hakemiseen useista sovellustauluista ER-mallin yhdistämismäärityksissä](er-join-data-sources.md)

[Sähköisen raportoinnin muotojen suorittamisen seuraaminen suorituskykyyn liittyvien ongelmien ratkaisemiseksi](trace-execution-er-troubleshoot-perf.md)

[Liiketoiminta-asiakirjojen hallinta – yleiskatsaus](er-business-document-management.md)

[Piilota Word-sisällön ohjausobjektit luoduissa raporteissa](er-design-configuration-word-suppress-controls.md)

[Useiden johdettujen yhdistämismääritysten hallinta yksittäiselle mallin juurelle](er-multiple-model-mappings.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
