---
title: Sähköisen raportoinnin (ER) kaavojen suunnittelutoiminto
description: Tässä aiheessa kerrotaan, miten kaavojen suunnittelutoimintoa käytetään sähköisessä raportoinnissa (ER).
author: NickSelin
manager: AnnBe
ms.date: 10/03/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1dc584355c8992ee701169fd5d29ad7b0300a498
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "331273"
---
# <a name="formula-designer-in-electronic-reporting-er"></a>Sähköisen raportoinnin (ER) kaavojen suunnittelutoiminto

[!include [banner](../includes/banner.md)]

Tässä aiheessa kerrotaan, miten kaavojen suunnittelutoimintoa käytetään sähköisessä raportoinnissa (ER). Kun tietyn sähköisen asiakirjan muotoa suunnitellaan ER:ssä, voit muuntaa tiedot kaavojen avulla vastaamaan asiakirjan toteuttamis- ja muotoiluvaatimuksia. Nämä kaavat muistuttavat Microsoft Excelin kaavoja. Kaavoissa tuetaan erilaisia toimintoja: teksti, päivämäärä ja aika, matemaattiset ja loogiset funktiot, tiedot, tietotyyppien muunnos ja muut (liiketoiminnan toimialuekohtaiset toiminnot).

## <a name="formula-designer-overview"></a>Yleiskatsaus kaavan suunnittelutoimintoon

Sähköinen raportointi tukee kaavojen suunnittelutoimintoa. Tämän vuoksi voit määrittää suunnittelun yhteydessä lausekkeita, joita voidaan käyttää suorituksen aikana seuraavissa tehtävissä:

- Microsoft Dynamics 365 for Finance and Operationsin tietokannasta vastaanotettujen tietojen muuntaminen. Tiedot täytetään ER-tietomalliin, joka on suunniteltu ER-muotojen (kuten suodatus, ryhmittely ja tietotyypin muunnos) tietolähteeksi. (Näitä muunnoksia ovat esimerkiksi suodatus, ryhmitys ja tietotyypin muunto.)
- Muodostettavaan sähköiseen asiakirjaan lähetettävien tietojen muotoilu tietyn ER-muodon asettelun ja ehtojen mukaisesti. (Muotoilu voidaan tehdä esimerkiksi pyydetyn kielen tai kulttuurin tai koodauksen mukaisesti.)
- Sähköisten asiakirjojen luontiprosessin hallinta. (Lausekkeet voivat esimerkiksi ottaa käyttöön muodon tiettyjen elementtien tuottamisen tai poistaa sen käytöstä käsiteltävien tietojen mukaan. Ne voivat myös keskeyttää asiakirjan luontiprosessin tai näyttää sanomia käyttäjille.)

Voit avata **Kaavojen suunnittelutoiminto** -sivun, kun teet jonkin seuraavista toiminnoista:

- Tietolähteen nimikkeiden sidonta tietomallin komponentteihin
- Tietolähteen nimikkeiden sidonta muotokomponentteihin
- Laskettujen kenttien täydellinen ylläpito tietolähteiden osana
- Käyttäjän syöttöparametrien näkyvyyden ehtojen määritys
- Muodon muunnosten rakenne
- Muotokomponenttien ehtojen käyttöönottamisen määritys
- Muodon tiedostokomponenttien tiedostonimien määritys
- Prosessin hallinnan tarkistusten ehtojen määritys
- Prosessin hallinnan tarkistusten sanoman tekstin määritys

## <a name="designing-er-formulas"></a>ER-kaavojen suunnitteleminen

### <a name="data-binding"></a>Tietojen sidonta

ER-kaavojen suunnittelutoiminnon avulla voi määrittää lausekkeen, joka muuntaa tietolähteistä vastaanotetut tiedot niin, että tiedot voidaan täyttää tietojen käyttäjään suorituksen aikana:

- Finance and Operationsin tietolähteistä ja suorituksen aikaisista parametreista ER-tietomalliin
- ER-tietomallista ER-muotoon
- Finance and Operationsin tietolähteistä ja suorituksen aikaisista parametreista ER-muotoon

Seuraavassa kuvassa esitellään tämäntyyppisen lausekkeen rakenne. Tässä esimerkissä lauseke pyöristää **Intrastat.AmountMST**-kentän arvon Finance and Operationsin Intrastat-taulussa kahteen desimaaliin ja palauttaa sitten pyöristetyn arvon.

[![Tietojen sidonta](./media/picture-expression-binding.jpg)](./media/picture-expression-binding.jpg)

Seuraavassa kuvassa esitellään, miten tämän tyyppistä lauseketta voidaan käyttää. Tässä esimerkissä suunnitellun lausekkeen tulos täytetään **Veroraportointimalli**-tietomallin **Transaction.InvoicedAmount**-komponentilla.

[![Tietojen sidontaa käytetään](./media/picture-expression-binding2.jpg)](./media/picture-expression-binding2.jpg)

Suorituksen aikana suunniteltu kaava, **ROUND (Intrastat.AmountMST, 2)** pyöristää kunkin Intrasat-taulun tietueen **AmountMST**-kentän arvon kahteen desimaaliin. Sen jälkeen pyöristetty arvo annetaan **Veroilmoitus**-tietomallin **Transaction.InvoicedAmount**-komponentissa.

### <a name="data-formatting"></a>Tietojen muotoilu

ER-kaavojen suunnittelutoiminnon avulla voi määrittää lausekkeen, joka muotoilee tietolähteistä vastaanotetut tiedot niin, että tiedot voidaan lähettää sähköisen asiakirjan luonnin osana. Käytössä voi olla muotoilu, jota on käytettävä tyypillisenä muotoiluna ja jota on käytettävä kaavassa uudelleen. Siinä tapauksessa voit käyttää kyseistä muotoilua kerran muodon määrityksessä nimettynä muunnoksena, jolla on muotoilulauseke. Tämän jälkeen nimetty muunnos voidaan linkittää useisiin muotokomponentteihin, joiden tulosten on oltava luodun muotoilulausekkeen mukaisesti muotoiltuja.

Seuraavassa kuvassa esitellään tämäntyyppisen muotoilun rakenne. Tässä esimerkissä **TrimmedString**-muunnos lyhentää **Merkkijono**-tyyppiset tiedot ja poistamalla ylimääräiset välilyönnit alusta ja lopusta. Se palauttaa sitten lyhennetyn merkkijonon arvon.

[![Muunnos](./media/picture-transformation-design.jpg)](./media/picture-transformation-design.jpg)

Seuraavassa kuvassa esitellään, miten tämäntyyppistä muunnosta voidaan käyttää. Tässä esimerkissä useat muotokomponentit lähettävä tekstin tuloksena suorituksen aikana muodostettavaan sähköiseen asiakirjaan. Kaikki nämä muotokomponentit viittaavat **TrimmedString**-muunnokseen nimellä.

[![Käytettävä muunnos](./media/picture-transformation-usage.jpg)](./media/picture-transformation-usage.jpg)

Kun muodon komponentit, kuten edellisen kuvan **partyName**-komponentti viittaavat **TrimmedString**-muunnokseen, muunnos lähettää tekstin tuotoksena muodostettava sähköiseen asiakirjaan. Tämä teksti ei sisällä edeltäviä eikä lopussa olevia välilyöntejä.

Jos sinulla on muotoiluja, joita tulee kohdistaa yksitellen, voit käyttää muotoilua tietyn muotokomponentin sidonnan yksittäisenä lausekkeena. Seuraavassa kuvassa esitellään tämäntyyppinen lauseke. Tässä esimerkissä **partyType**-muotokomponentti on sidottu tietolähteeseen sen lausekkeen kautta, joka muuntaa saapuvat tiedot tietolähteen **Model.Company.RegistrationType**-kentästä isoilla kirjaimilla kirjoitetuksi tekstiksi. Lauseke lähettää sitten tekstin tuloksena sähköiseen asiakirjaan.

[![Muotoilun käyttö yksittäisessä asiakirjassa](./media/picture-binding-with-formula.jpg)](./media/picture-binding-with-formula.jpg)

### <a name="process-flow-control"></a>Prosessinkulun hallinta

ER-kaavojen suunnittelutoimintoa voidaan käyttää määritettäessä lausekkeita, joilla hallitaan muodostettavien sähköisten asiakirjojen prosessinkulkua. Voit suorittaa seuraavat tehtävät:

- Määritä ehdot, jotka määrittävät, milloin asiakirjan luontiprosessi on pysäytettävä.
- Määritä lausekkeet, jotka luovat käyttäjälle sanomia pysäytetyistä prosesseista tai näyttävät suorituslokin sanomia raportin luontiprosessin jatkamisesta.
- Määritä sähköisten asiakirjojen luonnin tiedostonimet ja ohjaa niiden luontiehtoja.

Jokainen prosessinkulun hallinnan sääntö suunnitellaan yksittäiseksi tarkistukseksi. Seuraavassa kuvassa esitellään tämäntyyppinen tarkistus. Tässä on kyseisen esimerkin konfiguraation selitys:

- Tarkistus arvioidaan, kun **INSTAT**-solmu luodaan XML-tiedoston muodostuksen yhteydessä.
- Jos tapahtumaluettelo on tyhjä, tarkistus pysäyttää suoritusprosessin ja palauttaa **EPÄTOSI**-arvon.
- Tarkistus palauttaa virhesanoman Finance and Operationsin otsikolla SYS70894 käyttäjän ensisijaisella kielellä.

[![Vahvistus](./media/picture-validation.jpg)](./media/picture-validation.jpg)

ER-kaavan luontitoimintoa voidaan käyttää myös sähköisen asiakirjan luonnin tiedostonimen muodostamisessa ja tiedoston luontiprosessin hallinnassa. Seuraavassa kuvassa esitellään tämäntyyppisen prosessikulun hallinnan rakenne. Tässä on kyseisen esimerkin konfiguraation selitys:

- Luettelo **model.Intrastat**-tietolähteen tietueista on jaettu eriin. Kussakin erässä on enintään 1 000 tietuetta.
- Tulos luo zip-tiedoston, joka sisältää yhden XML-muodossa olevan tiedoston jokaisessa luodussa erässä.
- Lauseke palauttaa sähköisen asiakirjan luomiselle tiedostonimen liittämällä tiedostonimen ja tiedostonimen tunnisteen. Toisen erän ja seuraavien erien tiedostonimi sisältää erän tunnuksen loppuliitteenä.
- Lauseke ottaa käyttöön (palauttamalla **TOSI**-arvon) vähintään yhden tietueen sisältävien erien tiedoston luontiprosessin.

[![Tiedoston hallinta](./media/picture-file-control.jpg)](./media/picture-file-control.jpg)

### <a name="basic-syntax"></a>Perussyntaksi

ER-lausekkeet voivat sisältää joitakin seuraavia elementtejä tai kaikki seuraavat elementit:

- Vakiot
- Operaattorit
- Viitteet
- Polut
- Toiminnot

#### <a name="constants"></a>Vakiot

Voit käyttää lausekkeiden suunnittelussa tekstivakioita ja numeerisia vakioita (arvoja, joita ei lasketa). Esimerkiksi lauseke **ARVO ("100") + 20** käyttää numeerista vakiota **20** ja merkkijonovakiota **"100"**. Se palauttaa numeerisen arvon **120**. ER-kaavojen suunnittelutoimintoa tukee ohjausjaksoja. Niinpä voitkin määrittää lausekkeen merkkijonosta, jota on käsiteltävä eri tavalla. Esimerkiksi lauseke **"Leo Tolstoi ""Sota ja rauha"" Osa 1"** palauttaa tekstimerkkijonon **Leo Tolstoi "Sota ja rauha" Osa 1**.

#### <a name="operators"></a>Operaattorit

Seuraavassa taulukossa on aritmeettisia operaattoreita, joita voi käyttää matemaattisten perusoperaattoreiden, kuten lisäyksen, vähennyksen sekä kerto- ja jakolaskun suorittamiseen.

| Operaattori | Merkitys               | Esimerkki |
|----------|-----------------------|---------|
| +        | Lisäys              | 1+2     |
| -        | Vähennys, negaatio | 5-2, -1 |
| \*       | Kertolasku        | 7\*8    |
| /        | Jaosto              | 9/3     |

Seuraavassa taulukossa on tuetut vertailuoperaattorit. Näillä operaattoreilla voi verrata kahta arvoa.

| Operaattori | Merkitys                  | Esimerkki    |
|----------|--------------------------|------------|
| =        | Yhtä suuri                    | X=Y        |
| &gt;     | Suurempi kuin             | X&gt;Y     |
| &lt;     | Pienempi kuin                | X&lt;Y     |
| &gt;=    | Suurempi tai yhtä suuri | X&gt;=Y    |
| &lt;=    | Pienempi tai yhtä suuri    | X&lt;=Y    |
| &lt;&gt; | Ei sama kuin             | X&lt;&gt;Y |

Lisäksi &-merkkiä voi käyttää tekstin ketjutusoperaattorina. Tällä tavoin yksittäiseen tekstikappaleeseen voi liittää tai yhdistää yhden tekstimerkkijonon tai useita merkkijonoja.

| Operaattori | Merkitys     | Esimerkki                                             |
|----------|-------------|-----------------------------------------------------|
| &        | Liitä | Ei tulostettavaa & :&nbsp;& tietueita ei löytynyt |

##### <a name="operator-precedence"></a>Operaattoreiden käsittelyjärjestys

Järjestys, jossa yhdistelmälausekkeen osat lasketaan, on tärkeä. Esimerkiksi lausekkeen **1 + 4 / 2** tulos on erilainen sen mukaan, suoritetaanko ensi yhteenlasku- vai jakotoiminto. Sulkeiden avulla voit määrittää, miten lauseke lasketaan. Jos haluat esimerkiksi osoittaa, että yhteenlaskutoiminto suoritetaan ensin, voit muuttaa edeltävän lausekkeen muotoon **(1 + 4) / 2**. Jos et selkeästi ilmaise lausekkeen toimintojen suoritusjärjestystä, järjestys perustuu oletusarvoiseen tukioperaattoreiden määrittämään käsittelyjärjestykseen. Seuraavassa taulukossa kuhunkin operaattoriin liitetty käsittelyjärjestys. Operaattorit, joilla on korkeampi käsittelyjärjestys (esimerkiksi 7), suoritetaan ennen operaattoreita, joilla on alempi käsittelyjärjestys (esimerkiksi 1).

| Järjestys | Operaattorit      | Syntaksi                                                                  |
|------------|----------------|-------------------------------------------------------------------------|
| 7          | Ryhmittely       | ( … )                                                                   |
| 6          | Jäsenen käyttöoikeus  | … . …                                                                   |
| 5          | Funktiokutsu  | … ( … )                                                                 |
| 4          | Kertova | … \* …<br>… / …                                                         |
| 3          | Lisä       | … + …<br>… - …                                                          |
| 2          | Vertailu     | … &lt; …<br>… &lt;= …<br>… =&gt; …<br>… &gt; …<br>… = …<br>… &lt;&gt; … |
| 1          | Erottelu     | … , …                                                                   |

Jos lausekkeessa on useita peräkkäisiä operaattoreita, joilla on sama tärkeysjärjestys, kyseiset operaattorit suoritetaan vasemmalta oikealle. Esimerkiksi lauseke **1 + 6 / 2 \* 3 &gt; 5** palauttaa arvon **tosi**. Käyttämällä sulkeita lausekkeiden haluttu laskentajärjestys voidaan ilmaista selkeästi, mikä myös helpottaa lausekkeiden lukemista ja ylläpitämistä.

#### <a name="references"></a>Viitteet

Kaikkia nykyisen ER-komponentin tietolähteitä, jotka ovat käytettävissä lausekkeen suunnittelun yhteydessä, voidaan käyttää nimettyinä viitteinä. (Valittu ER-komponentti voi olla joko malli tai muoto.) Esimerkiksi nykyinen ER-tietomalli sisältää **ReportingDate**-tietolähteen, joka palauttaa **DATETIME**-tietotyypin arvon. Jotta kyseinen arvo saadaan muotoiltua oikein luotavassa asiakirjassa, siihen voidaan viitata lausekkeessa seuraavasti: **DATETIMEFORMAT (ReportingDate, "dd-MM-yyyy")**.

Kaikkien niiden viittaavan tietolähteen nimen merkkien, jotka eivät ole kirjaimia, edessä on oltava edessään puolilainausmerkki ('). Kaikilla viittaavan tietolähteen nimillä, jotka sisältävät ainakin yhden merkin, joka ei ole kirjain, on oltava puolilainausmerkkien sisällä. (Näitä muita kuin kirjaimia voivat olla esimerkiksi välimerkit tai muut kirjoitetut merkit.) Esimerkkejä:

- **Tämän päivän päivämäärä ja aika** -tietolähteeseen on viitattava ER-lausekkeessa seuraavasti: **'Tämän päivän päivämäärä ja aika'**.
- **Asiakkaat**-tietolähteen **name()**-menetelmän on viitattava ER-lausekkeeseen seuraavasti: **Customers.'name()'**.

Jos Finance and Operations -tietolähteiden menetelmillä on parametreja, kyseiset menetelmät kutsutaan seuraavalla syntaksilla:

- Jos **Järjestelmä**-tietolähteen, jossa **Merkkijono**-tietotyypin parametri on **EN-US**, **isLanguageRTL**-menetelmään on viitattava ER-lausekkeessa seuraavasti: **System.'isLanguageRTL'("EN-US")**.
- Lainausmerkit eivät ole pakollisia, kun menetelmän nimessä on vain aakkosnumeerisia merkkejä. Niitä on kuitenkin käytettävä taulun menetelmässä, jos hakasulkeet sisältyvät nimeen.

Kun **Järjestelmä**-tietolähde lisätään ER-yhdistämismääritykseen, jossa on viittauksena Finance and Operationsin **Yleinen**-sovellusluokka, lauseke palauttaa totuusarvon **EPÄTOSI**. Muokattu lauseke **System.' isLanguageRTL'("AR")** palauttaa totuusarvon **TOSI**.

Voit rajoittaa tapaa, jolla arvot siirretään tämän tyyppisen menetelmän parametreihin:

- Vain vakioita voi siirtää tämän tyyppisiin menetelmiin. Vakioiden arvot määritetään suunnitteluvaiheessa.
- Tämän tyypin parametrit tukevat alkeellisia (perus) tietotyyppejä. (Alkukantaisia tietotyyppejä ovat esimerkiksi kokonaisluku, reaaliluku, totuusarvo ja merkkijono.)

#### <a name="paths"></a>Polut

Kun lauseke viittaa rakenteelliseen tietolähteeseen, polun määritettä voidaan käyttää valittaessa tietolähteen tietty primitiivinen elementti. Piste (.) -merkkiä käytetään erottamaan rakenteisen tietolähteen yksittäiset elementit. Esimerkiksi nykyinen ER-tietomalli sisältää **InvoiceTransactions**-tietolähteen, joka palauttaa tietueluettelon. **InvoiceTransactions**-tietuerakenne sisältää **AmountDebit**- ja **AmountCredit**-kentät, joista kumpikin palautta numeerisia arvoja. Voit siis suunnitella seuraavan lausekkeen, jolla lasketaan laskutettu määrä: **InvoiceTransactions.AmountDebit - InvoiceTransactions.AmountCredit**.

#### <a name="functions"></a>Toiminnot

Seuraavassa osassa esitellään toiminnot, joita voidaan käyttää ER-lausekkeissa. Kaikkia lausekekontekstin (nykyinen ER-tietomalli tai ER-muoto) tietolähteitä voidaan käyttää kutsufunktioiden parametreina kutsufunktioargumenttien luettelon mukaisesti. Myös vakioita voidaan käyttää kutsufunktioiden parametreina. Esimerkiksi nykyinen ER-tietomalli sisältää **InvoiceTransactions**-tietolähteen, joka palauttaa tietueluettelon. **InvoiceTransactions**-tietuerakenne sisältää **AmountDebit**- ja **AmountCredit**-kentät, joista kumpikin palautta numeerisia arvoja. Voit siis laskea laskutetun määrän suunnittelemalla seuraavan lausekkeen, jossa käytetään sisäänrakennettua ER-pyöristystoimintoa: **PYÖRISTYS (InvoiceTransactions.AmountDebit - InvoiceTransactions.AmountCredit, 2)**.

## <a name="supported-functions"></a>Tuetut toiminnot

Seuraavassa taulukossa esitellään tietojenkäsittelytoiminnot, jotka ovat käytettävissä ER-tietomallien ja ER-raporttien suunnitteluun. Funktioluettelo ei ole kiinteä. Kehittäjät voivat laajentaa sitä. Näet käytettävien funktioiden luettelon avaamalla ER-kaavojen suunnittelutoiminnon funktioruudun.

### <a name="date-and-time-functions"></a>Päivämäärä- ja aikatoiminnot

| Toiminto | Kuvaus | Esimerkki |
|----------|-------------|---------|
| ADDDAYS (päivämäärä ja aika, päivät) | Lisää määritetylle päivämäärän ja ajan arvolle määritetyn päivien lukumäärän. | **ADDDAYS (NOW(), 7)** palauttaa päivämäärän ja ajan seitsemän päivän kuluttua. |
| DATETODATETIME (päivämäärä) | Muuntaa määritetyn päivämäärän arvon päivämäärän ja ajan arvoksi. | **DATETODATETIME (CompInfo. 'getCurrentDate()')** palauttaa nykyisen Finance and Operations -istunnon päivämäärän 24.12.2015 muodossa **24.12.2015 00.00.00**. Tässä esimerkissä **CompInfo** on **Finance and Operations / taulu** -tyypin ER-tietolähde, joka viittaa CompanyInfo-tauluun. |
| NOW () | Palauttaa nykyisen Finance and Operations -sovelluspalvelimen päivämäärän ja kellonajan päivämäärän ja ajan arvona. | |
| TODAY () | Palauttaa nykyisen Finance and Operations -sovelluspalvelimen päivämäärän päivämääräarvona. | |
| NULLDATE () | Palauttaa **tyhjän** päivämäärän arvon. | |
| NULLDATETIME () | Palauttaa **tyhjän** päivämäärän ja ajan arvon. | |
| DATETIMEFORMAT (päivämäärä ja aika, muoto) | Muuntaa määritetyn päivämäärän ja ajan arvon tietyssä muodossa olevaksi merkkijonoksi. (Lisätietoja tuetuista muodoista on kohdassa [vakio](https://msdn.microsoft.com/en-us/library/az4se3k1(v=vs.110).aspx) ja [mukautettu](https://msdn.microsoft.com/en-us/library/8kb3ddd4(v=vs.110).aspx).) | **DATETIMEFORMAT (NOW(), "dd-MM-yyyy")** palauttaa nykyisen Finance and Operations -sovelluspalvelimen päivämäärän 24.12.2015 muodossa **24-12-2015** määritetyn mukautetun muodon mukaisesti. |
| DATETIMEFORMAT (päivämäärä ja aika, maa-asetukset) | Muuntaa määritetty päivämäärän ja ajan arvon merkkijonoksi, joka on määritetyssä muodossa ja jolla on määritetyt [maa-asetukset](https://msdn.microsoft.com/en-us/goglobal/bb896001.aspx). (Lisätietoja tuetuista muodoista on kohdassa [vakio](https://msdn.microsoft.com/en-us/library/az4se3k1(v=vs.110).aspx) ja [mukautettu](https://msdn.microsoft.com/en-us/library/8kb3ddd4(v=vs.110).aspx).) | **DATETIMEFORMAT (NOW(), "d", "de")** palauttaa nykyisen Finance and Operations -sovelluspalvelimen päivämäärän 24.12.2015 muodossa **24.12.2015** valitun Saksan maa-asetuksen mukaisesti. |
| SESSIONTODAY () | Palauttaa nykyisen Finance and Operations -istunnon päivämäärän päivämääräarvona. | |
| SESSIONNOW () | Palauttaa nykyisen Finance and Operations -istunnon päivämäärän ja kellonajan päivämäärän ja ajan arvona. | |
| DATEFORMAT (päivämäärä, muoto) | Palauttaa määritetyssä muodossa olevan määritetyn päivämäärän merkkijonon esityksen. | **DATEFORMAT (SESSIONTODAY (), "dd-MM-yyyy")** palauttaa nykyisen Finance and Operations -istunnon päivämäärän 24.12.2015 muodossa **24-12-2015** määritetyn mukautetun muodon mukaisesti. |
| DATEFORMAT (päivämäärä, muoto, maa-asetus) | Muunna määritetty päivämäärän arvo merkkijonoksi, joka on määritetyssä muodossa ja jolla on määritetyt [maa-asetukset](https://msdn.microsoft.com/en-us/goglobal/bb896001.aspx). (Lisätietoja tuetuista muodoista on kohdassa [vakio](https://msdn.microsoft.com/en-us/library/az4se3k1(v=vs.110).aspx) ja [mukautettu](https://msdn.microsoft.com/en-us/library/8kb3ddd4(v=vs.110).aspx).) | **DATETIMEFORMAT (SESSIONNOW (), "d", "de")** palauttaa nykyisen Finance and Operations -istunnon päivämäärän 24.12.2015 muodossa **24.12.2015** valitun Saksan maa-asetuksen mukaisesti. |
| DAYOFYEAR (päivämäärä) | Palauttaa tammikuun 1. päivän ja määritetyn päivämäärän välisten päivien määrän kokonaislukuna. | **DAYOFYEAR (DATEVALUE ("01-03-2016", "dd-MM-yyyy"))** palauttaa arvon **61**. **DAYOFYEAR (DATEVALUE ("01-01-2016", "dd-MM-yyyy"))** palauttaa arvon **1**. |
| DAYS (päivämäärä 1, päivämäärä 2) | Palauttaa ensimmäisen ja toisen määritetyn päivämäärän välisten päivien määrän. Palauttaa positiivisen arvon, kun ensimmäinen päivämäärä on myöhemmin kuin toinen päivämäärä, palauttaa arvon **0** (nolla), kun ensimmäinen päivämäärä on sama kuin toinen päivämäärä. Palauttaa negatiivisen arvon, kun ensimmäinen päivämäärä on aikaisempi kuin toinen päivämäärä. | **DAYS (TODAY (), DATEVALUE( DATETIMEFORMAT( ADDDAYS(NOW(), 1), "yyyyMMdd"), "yyyyMMdd"))** palauttaa arvon **-1**. |

### <a name="data-conversion-functions"></a>Tietojen muuntotoiminnot

| Toiminto | kuvaus | Esimerkki |
|----------|-------------|---------|
| DATETODATETIME (päivämäärä) | Muuntaa määritetyn päivämäärän arvon päivämäärän ja ajan arvoksi. | **DATETODATETIME (CompInfo. 'getCurrentDate()')** palauttaa nykyisen Finance and Operations -istunnon päivämäärän 24.12.2015 muodossa **24.12.2015 00.00.00**. Tässä esimerkissä **CompInfo** on **Finance and Operations / taulu** -tyypin ER-tietolähde, joka viittaa CompanyInfo-tauluun. |
| DATEVALUE (merkkijono, muoto) | Palauttaa määritetyssä muodossa olevan määritetyn merkkijonon päivämäärän esityksen. | **DATEVALUE ("21-Dec-2016", "dd-MMM-yyyy")** palauttaa päivämäärän 21.12.2016 määritetyn mukautetun muodon ja oletussovelluksen **EN-US**-maa-asetuksen mukaisesti. |
| DATEVALUE (merkkijono, muoto, maa/alue) | Palauttaa määritetyssä muodossa ja maa-asetuksessa olevan määritetyn merkkijonon päivämäärän esityksen. | **DATEVALUE ("21-Gen-2016", "dd-MMM-yyyy", "IT")** palauttaa päivämäärän 21.1.2016 määritetyn mukautetun muodon ja maa-asetuksen perusteella. Kuitenkin **DATEVALUE ("21-Gen-2016", "dd-MMM-yyyy", "EN-US")** aiheuttaa poikkeuksen, joka ilmoittaa käyttäjälle, että määritettyä merkkijonoa ei tunnisteta kelvolliseksi päivämääräksi. |
| DATETIMEVALUE (merkkijono, muoto) | Palauttaa määritetyssä muodossa olevan määritetyn merkkijonon päivämäärän ja ajan esityksen. | **DATETIMEVALUE ("21-Dec-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss")** palauttaa ajankohdan 02:55:00 21.12.2016 määritetyn mukautetun muodon oletussovelluksen **EN-US**-maa-asetuksen perusteella. |
| DATETIMEVALUE (merkkijono, muoto, maa/alue) | Palauttaa määritetyssä muodossa ja maa-asetuksessa olevan määritetyn merkkijonon päivämäärän ja ajan esityksen. | **DATETIMEVALUE ("21-Gen-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss", "IT")** palauttaa ajankohdan 02:55:00 21.12.2016 määritetyn mukautetun muodon ja maa-asetuksen perusteella. Kuitenkin **DATETIMEVALUE ("21-Gen-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss", "EN-US")** aiheuttaa poikkeuksen, joka ilmoittaa käyttäjälle, että määritettyä merkkijonoa ei tunnisteta kelvolliseksi päivämääräksi ja ajaksi. |

### <a name="list-functions"></a>Luettelotoiminnot

<table>
<thead>
<tr>
<th>Toiminto</th>
<th>kuvaus</th>
<th>Esimerkki</th>
</tr>
</thead>
<tbody>
<tr>
<td>SPLIT (syöte, pituus)</td>
<td>Jaa määritetty syötemerkkijono alimerkkijonoiksi, joilla on tietty pituus. Palauttaa tuloksen uutena luettelona.</td>
<td><strong>SPLIT (&quot;abcd&quot;, 3)</strong> palauttaa uuden luettelon. Luettelo sisältää kaksi tietuetta, joilla on <strong>STRING</strong>-kenttä. Ensimmäisen tietueen kenttä sisältää tekstin <strong>&quot;abc&quot;</strong> ja toisen tietueen kenttä tekstin <strong>&quot;d&quot;</strong>.</td>
</tr>
<tr>
<td>SPLIT (syöte, erotin)</td>
<td>Jaa määritetty syötemerkkijono alimerkkijonoiksi määritetyn erottimen perusteella.</td>
<td><strong>SPLIT (&quot;XAb aBy&quot;, &quot;aB&quot;)</strong> palauttaa uuden luettelon. Luettelossa on kolme tietuetta, joissa on <strong>STRING</strong>-kenttä. Ensimmäisen tietueen kentässä on teksti <strong>&quot;X&quot;</strong>, toisen tietueen kentässä teksti &quot;&nbsp;&quot; ja kolmen tietueen kentässä teksti <strong>&quot;y&quot;</strong>. Jos erotin on tyhjä, palautettavassa uudessa luettelossa on yksi tietue, jonka <strong>STRING</strong>-kenttää sisältää syötteen tekstin. Jos syöte on tyhjä, palautettava uusi luettelo on tyhjä.
Jos syöte tai erotin on määrittämättä (tyhjäarvo), sovellus antaa poikkeuksen.</td>
</tr>
<tr>
<td>SPLITLIST (luettelo, numero)</td>
<td>Jaa määritetty luettelo eriksi, joissa on tietty määrä tietueita. Palauttaa tuloksen uutena eräluettelona, joka sisältää seuraavat elementit:
<ul>
<li>Erät tavallisina luetteloina (<strong>arvo</strong>-komponentti)</li>
<li>Nykyinen eränumero (<strong>BatchNumber</strong>-komponentti)</li>
</ul>
</td>
<td>Seuraavassa kuvassa <strong>Rivit</strong>-tietolähde luodaan kolmen tietueen tietueluetteloksi. Tämä luettelo on jaettu eriin, joista kussakin on enintään kaksi tietuetta.
<p><a href="./media/picture-splitlist-datasource.jpg"><img src="./media/picture-splitlist-datasource.jpg" alt="Data source that is divided into batches" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a></p>
<p>Seuraavassa kuvassa on suunnitellun muodon asettelu. Tässä muodon asettelussa sidonnat <strong>Rivit</strong>-tietolähde luodaan muodostamaan tulos XML-muodossa. Tämä tulos esittää kunkin erän erilliset solmut ja sen tietueet.</p>
<p><a href="./media/picture-splitlist-format.jpg"><img src="./media/picture-splitlist-format.jpg" alt="Format layout that has bindings to a data source" class="alignnone wp-image-290691 size-full" width="374" height="161" /></a></p>
<p>Seuraavassa kuvassa on tulos, kun suunniteltu muoto suoritetaan.</p>
<a href="./media/picture-splitlist-result.jpg"><img src="./media/picture-splitlist-result.jpg" alt="Result of running the format" class="alignnone wp-image-290701 size-full" width="358" height="191" /></a>
</td>
</tr>
<tr>
<td>LIST (tietue 1 [, tietue 2, ...])</td>
<td>Palauttaa uuden luettelon, joka on luotu määritetyistä argumenteista.</td>
<td><strong>LIST (model.MainData, model.OtherData)</strong> palauttaa tyhjän tietueen, jonka sisältämä kenttäluettelo sisältää kaikki <strong>MainData</strong>- ja <strong>OtherData</strong>-tietueluettelon kentät.</td>
</tr>
<tr>
<td>LISTJOIN (luettelo 1, luettelo 2, ...)</td>
<td>Palauttaa yhdistetyn luettelon, joka on luotu määritettyjen argumenttien luetteloista.</td>
<td><strong>LISTJOIN (SPLIT (&quot;abc&quot;, 1), SPLIT (&quot;def&quot;, 1))</strong> palauttaa kuuden tietueen luettelon, jossa yksi <strong>STRING</strong>-tietotyypin kenttä sisältää yksittäisiä kirjaimia.</td>
</tr>
<tr>
<td>ISEMPTY (luettelo)</td>
<td>Palauttaa <strong>TOSI</strong>-arvon, jos määritetty luettelo ei sisällä yhtään elementtiä. Muussa tapauksessa palauttaa <strong>EPÄTOSI</strong>-arvon.</td>
<td></td>
</tr>
<tr>
<td>EMPTYLIST (luettelo)</td>
<td>Palauttaa tyhjän luettelon käyttämällä määritettyä luetteloa luettelorakenteen lähteenä.</td>
<td><strong>EMPTYLIST (SPLIT (&quot;abc&quot;, 1))</strong> palauttaa uuden tyhjän luettelon, jonka rakenne on sama kuin <strong>SPLIT</strong>-toiminnon palauttamalla luettelolla.</td>
</tr>
<tr>
<td>FIRST (luettelo)</td>
<td>Palauttaa määritetyn luettelon ensimmäisen tietueen, jos kyseinen tietue ei ole tyhjä. Muussa tapauksessa annetaan poikkeus.</td>
<td></td>
</tr>
<tr>
<td>FIRSTORNULL (luettelo)</td>
<td>Palauttaa määritetyn luettelon ensimmäisen tietueen, jos kyseinen tietue ei ole tyhjä. Muussa tapauksessa palauttaa <strong>tyhjän</strong> tietueen.</td>
<td></td>
</tr>
<tr>
<td>LISTOFFIRSTITEM (luettelo)</td>
<td>Palauttaa luettelon, joka sisältää vain määritetyn luettelon ensimmäisen nimikkeen.</td>
<td></td>
</tr>
<tr>
<td>ALLITEMS (polku)</td>
<td>Tämä toiminto suoritetaan muistin sisäisenä valintana. Se palauttaa uuden tasoitetun luettelon, joka edustaa kaikkia nimikkeitä, jotka vastaavat määritettyä polkua. Polku on määritettävä sallituksi tietolähteen poluksi tietueluettelo-tietotyypin tietolähteen elementtiin. Tietoelementit, kuten polun merkkijono ja päivämäärä, käynnistävät virheen ER-lausekkeenmuodostimessa suunnitteluaikana.</td>
<td>Jos syötät tietolähteeksi (DS) <strong>SPLIT(&quot;abcdef&quot; , 2)</strong>, <strong>COUNT( ALLITEMS (DS.Value))</strong> palauttaa <strong>3</strong>.</td>
</tr>
<tr>
<td>ALLITEMSQUERY (polku)</td>
<td>Tämä toiminto suoritetaan liitettynä SQL-kyselynä. Se palauttaa uuden tasoitetun luettelon, joka edustaa kaikkia nimikkeitä, jotka vastaavat määritettyä polkua. Määritetty polku on määritettävä sallituksi tietolähteen poluksi tietueluettelo-tietotyypin tietolähteen elementtiin ja sen pitää sisältää vähintään yksi suhde. Tietoelementit, kuten polun merkkijono ja päivämäärä, käynnistävät virheen ER-lausekkeenmuodostimessa suunnitteluaikana.</td>
<td>Määritä seuraavat tietolähteet omassa mallimäärityksessäsi:
<ul>
<li><strong>CustInv</strong> (<strong>Taulukkotietueet</strong>-tyypi), joka viittaa CustInvoiceTable-tauluun</li> 
<li><strong>FilteredInv</strong> (<strong>Laskettu kenttä</strong> -tyyppi), joka sisältää lausekkeen <strong>FILTER (CustInv, CustInv.InvoiceAccount = &quot;US-001&quot;)</strong></li>
<li><strong>JourLines</strong> (<strong>Laskettu kenttä</strong> -tyyppi), joka sisältää lausekkeen <strong>ALLITEMSQUERY (FilteredInv.'&lt;Relations'.CustInvoiceJour.'&lt;Relations'.CustInvoiceTrans)</strong></li>
</ul>
<p>Kun suoritat mallimäärityksen kutsumaan <strong>JourLines</strong>-tietolähdettä, seuraava SQL-lauseke suoritetaan:</p>
SELECT ... FROM CUSTINVOICETABLE T1 CROSS JOIN CUSTINVOICEJOUR T2 CROSS JOIN CUSTINVOICETRANS T3 WHERE...
</td>
</tr>
<tr>
<td>ORDERBY (luettelo [, lauseke 1, lauseke 2, …])</td>
<td>Palauttaa määritetyn luettelon sen jälkeen, kun se lajiteltu määritettyjen argumenttien mukaan. Nämä argumentit voivaan määrittää lausekkeina.</td>
<td>Jos <strong>Toimittaja</strong> on määritetty ER-tietolähteeksi, joka viittaa VendTable-tauluun, <strong>ORDERBY (Vendors, Vendors.'name()')</strong> palauttaa toimittajaluettelon, joka on lajiteltu nimen mukaan nousevassa järjestyksessä.</td>
</tr>
<tr>
<td>REVERSE (luettelo)</td>
<td>Palauttaa määritetyn luettelon käänteisessä lajittelujärjestyksessä.</td>
<td>Jos <strong>Toimittaja</strong> on määritetty ER-tietolähteeksi, joka viittaa VendTable-tauluun, <strong>REVERSE (ORDERBY (Vendors, Vendors.'name()')) )</strong> palauttaa toimittajaluettelon, joka on lajiteltu nimen mukaan laskevassa järjestyksessä.</td>
</tr>
<tr>
<td>WHERE (luettelo, ehto)</td>
<td>Palauttaa määritetyn luettelon sen jälkeen, kun se suodatettu määritetyn ehdon mukaan. Määritettyä hakuehtoa käytetään muistin luetteloon. Tällä tavalla <strong>WHERE</strong>-funktio eroaa <strong>FILTER</strong>-funktiosta.</td>
<td>Jos <strong>Toimittaja</strong> on määritetty VendTable-tauluun viittaavaksi ER-tietolähteeksi, <strong>WHERE(Vendors, Vendors.VendGroup = &quot;40&quot;)</strong> palauttaa toimittajaluettelon, joka kuuluu toimittajaryhmään 40.</td>
</tr>
<tr>
<td>ENUMERATE (luettelo)</td>
<td>Palauttaa uuden luettelon, joka sisältää määritetyn luettelon numeroituja tietueita ja paljastaa seuraavat elementit:
<ul>
<li>Määritetyn luettelon tietueet tavallisina luetteloita (<strong>arvo</strong>-komponentti)</li>
<li>Nykyisen tietueen indeksi (<strong>numero</strong>-komponentti)</li>
</ul>
</td>
<td>Seuraavassa kuvassa <strong>Numeroitu</strong>-tietolähde luodaan toimittajan tietueiden numeroituna luettelona <strong>Toimittajat</strong>-tietolähteestä, joka viittaa VendTable-tauluun.
<p><a href="./media/picture-enumerate-datasource.jpg"><img src="./media/picture-enumerate-datasource.jpg" alt="Enumerated data source" class="alignnone wp-image-290711 size-full" width="387" height="136" /></a></p>
<p>Muoto näkyy seuraavassa kuvassa. Tässä muodossa tiedon sidonnat luodaan muodostamaan tulos XML-muodossa. Tämä tulos esittää yksittäiset toimittajat luetteloituina solmuina.</p>
<p><a href="./media/picture-enumerate-format.jpg"><img src="./media/picture-enumerate-format.jpg" alt="Format that has data bindings" class="alignnone wp-image-290721 size-full" width="414" height="138" /></a></p>
<p>Seuraavassa kuvassa on tulos, kun suunniteltu muoto suoritetaan.</p>
<a href="./media/picture-enumerate-result.jpg"><img src="./media/picture-enumerate-result.jpg" alt="Result of running the format" class="alignnone wp-image-290731 size-full" width="567" height="176" /></a>
</td>
</tr>
<tr>
<td>COUNT (luettelo)</td>
<td>Palauttaa määritetyn luettelon tietueiden lukumäärän, jos luettelo ei ole tyhjä. Muussa tapauksessa palauttaa arvon <strong>0</strong> (nolla).</td>
<td><strong>COUNT (SPLIT(&quot;abcd&quot; , 3))</strong> palauttaa arvon <strong>2</strong>, koska <strong>SPLIT</strong>-toiminto luo luettelon, jossa on kaksi tietuetta.</td>
</tr>
<tr>
<td>LISTOFFIELDS (polku)</td>
<td>Palauttaa tietueluettelon, joka on luotu jostakin seuraavan tyyppisestä argumentista:
<ul>
<li>Mallin luettelointi</li>
<li>Muodon luettelointi</li>
<li>Kontti</li>
</ul>
<p>Luotu luettelo koostuu tietueista, jossa on seuraavat kentät:</p>
<ul>
<li>Nimi</li>
<li>Nimiö</li>
<li>kuvaus</li>
</ul>
<strong>Otsikko</strong>- ja <strong>Kuvaus</strong>-kentät palauttavat suorituksen aikana muodon kieliasetuksiin perustuvat arvot.
</td>
<td>Seuraavassa kuvan on tietomallin luettelointi.
<p><a href="./media/ger-listoffields-function-model-enumeration.png"><img src="./media/ger-listoffields-function-model-enumeration-e1474545790761.png" alt="Enumeration in a model" class="alignnone wp-image-1203943 size-full" width="514" height="155" /></a></p>
<p>Seuraavassa kuvassa on nämä tiedot:</p>
<ul>
<li>Mallin luettelointi lisätään raporttiin tietolähteenä.</li>
<li>ER-lauseke käyttää mallin luettelointia <strong>LISTOFFIELDS</strong>-funktion parametrina.</li>
<li>Tietueluettelon tyypin tietolähde lisätään raporttiin luodun ER-lausekkeen avulla.</li>
</ul>
<p><a href="./media/ger-listoffields-function-in-format-expression.png"><img src="./media/ger-listoffields-function-in-format-expression-e1474546110395.png" alt="Format" class="alignnone wp-image-1204033 size-full" width="549" height="318" /></a></p>
<p>Seuraavassa esimerkissä on ER-lomakkeen elementit, jotka on sidottu <strong>LISTOFFIELDS</strong>-funktiolla luotuun tietueluettelotyypin tietolähteeseen.</p>
<p><a href="./media/ger-listoffields-function-format-design.png"><img src="./media/ger-listoffields-function-format-design.png" alt="Format design" class="alignnone size-full wp-image-1204043" width="466" height="221" /></a></p>
<p>Seuraavassa kuvassa on tulos, kun suunniteltu muoto suoritetaan.</p>
<p><a href="./media/ger-listoffields-function-format-output.png"><img src="./media/ger-listoffields-function-format-output.png" alt="Format output" class="alignnone size-full wp-image-1204053" width="585" height="158" /></a></p>
<blockquote>[!NOTE] Selitteiden ja kuvausten käännetty teksti annetaan ER-lomakkeeseen FILE- ja FOLDER-päälomake-elementeille määritettyjen kieliasetusten perusteella</blockquote>
</td>
</tr>
<tr>
<td>LISTOFFIELDS (polku, kieli)</td>
<td>Palauttaa argumentista luodun tietueluettelon, kuten mallin luettelointi, lomakkeen luettelointi tai säilö. Luotu luettelo koostuu tietueista, jossa on seuraavat kentät:
<ul>
<li>Nimi</li>
<li>Nimiö</li>
<li>kuvaus</li>
<li>Käännetty</li>
</ul>
<strong>Otsikko</strong>- ja <strong>Kuvaus</strong>-kentät palauttavat suorituksen aikana muodon kieliasetuksiin ja määritettyyn kieleen perustuvat arvot. <strong>Käännetty</strong>-kenttä ilmaisee, että <strong>Otsikko</strong>-kenttä on käännetty määritetylle kielelle.
</td>
<td>Voit esimerkiksi määrittää <strong>Laskettu kenttä</strong>-tietolähdetyypin määrittämään <strong>enumType_de</strong>- ja <strong>enumType_deCH</strong>-tietolähteet <strong>enumType</strong>-tietomallin luettelointia varten.
<ul>
<li>enumType_de = <strong>LISTOFFIELDS</strong> (enumType, &quot;de&quot;)</li>
<li>enumType_deCH = <strong>LISTOFFIELDS</strong> (enumType, &quot;de-CH&quot;)</li>
</ul>
<p>Voit hakea tässä tapauksessa otsikon sveitsinsaksan luettelointiarvon, jos käännös on käytettävissä, käyttämällä seuraavaa lauseketta. Jos sveitsinsaksan käännös ei ole käytettävissä, otsikko on saksankielinen.</p>
IF (NOT (enumType_deCH.IsTranslated), enumType_de.Label, enumType_deCH.Label)
</td>
</tr>
<tr>
<td>STRINGJOIN (luettelo, kenttänimi, erotin)</td>
<td>Palauttaa määritetystä luettelosta merkkijonon, jossa on määritetyn kentän lyhennetyt arvot. Arvot erotetaan määritetyllä erottimella.</td>
<td>Jos annat tietolähteeksi (DS) <strong>SPLIT(&quot;abc&quot; , 1)</strong>, <strong>STRINGJOIN (DS, DS.Value, &quot;-&quot;)</strong> palauttaa <strong>&quot;a-b-c&quot;</strong>.</td>
</tr>
<tr>
<td>SPLITLISTBYLIMIT (luettelo, raja-arvo, lähderaja-arvo)</td>
<td>Jakaa määritetyn luettelon uudeksi aliluetteloiden luetteloksi ja palauttaa tuloksen tietueluettelonsisältöön. <strong>Raja-arvo</strong>-parametri määrittää arvon, joka jakaa alkuperäisen luettelon. <strong>Lähderaja-arvo</strong>-parametri määrittää vaiheen, jonka mukaan kokonaissummaa kasvatetaan. Rajaa ei käytetä tietyn alkuperäisen luettelon yhteen nimikkeeseen, jos lähderaja ylittää määritetyn rajan.</td>
<td>Muoto näkyy seuraavassa kuvassa. 
<p><a href="./media/ger-splitlistbylimit-format.png"><img src="./media/ger-splitlistbylimit-format.png" alt="Format" class="alignnone size-full wp-image-1204063" width="396" height="195" /></a></p>
<p>Seuraavissa kuvissa näkyvät muodossa käytetyt tietolähteet.</p>
<p><a href="./media/ger-splitlistbylimit-datasources.png"><img src="./media/ger-splitlistbylimit-datasources.png" alt="Data sources" class="alignnone size-full wp-image-1204073" width="320" height="208" /></a></p>
<p>Seuraavassa kuvassa on tulos, kun muoto suoritetaan. Tässä tapauksessa tuloksena muoto, joka on kauppatavaroiden jäsentämätön luettelo.</p>
<p><a href="./media/ger-splitlistbylimit-output.png"><img src="./media/ger-splitlistbylimit-output.png" alt="Output" class="alignnone size-full wp-image-1204083" width="462" height="204" /></a></p>
<p>Seuraavissa kuvissa sama muoto on säädetty ilmaisemaan kauppatavarat erinä, kun yhdessä erässä on oltava kauppatavaroita, joiden kokonaispaino ei saa olla suurempi kuin 9.</p>
<p><a href="./media/ger-splitlistbylimit-format-1.png"><img src="./media/ger-splitlistbylimit-format-1.png" alt="Adjusted format" class="alignnone size-full wp-image-1204103" width="466" height="438" /></a></p>
<p><a href="./media/ger-splitlistbylimit-datasources-1.png"><img src="./media/ger-splitlistbylimit-datasources-1.png" alt="Data sources for the adjusted format" class="alignnone size-full wp-image-1204093" width="645" height="507" /></a></p>
<p>Seuraavassa kuvassa on tulos, kun säädetty muoto suoritetaan.</p>
<p><a href="./media/ger-splitlistbylimit-output-1.png"><img src="./media/ger-splitlistbylimit-output-1.png" alt="Output of the adjusted format" class="alignnone size-full wp-image-1204113" width="676" height="611" /></a></p>
<blockquote>[!NOTE] Rajaa ei sovellettu alkuperäisen luettelon viimeiseen nimikkeeseen, koska arvo (11) ylittää lähteen (painon) määritetyn raja-arvon (9). Käytä joko <strong>WHERE</strong>-funktiota tai vastaavan muodon elementin <strong>Käytössä</strong>-lauseketta ohittamaan tarvittaessa alaluettelot raporttia muodostettaessa.</blockquote>
</td>
</tr>
<tr>
<td>FILTER (luettelo, ehto)</td>
<td>Palauttaa määritetyn luettelon sen jälkeen, kun kysely on suodatettu määritetyn ehdon mukaan. Funktio eroaa <strong>WHERE</strong>-funktiosta, koska määritettyä ehtoa käytetään tietokannan tasolla kaikkiin <strong>Taulukkotietue</strong>-tyypin ER-tietolähteisiin. Luettelo ja ehto voidaan määrittää tauluja ja suhteita käyttämällä.</td>
<td>Jos <strong>Toimittaja</strong> on määritetty VendTable-tauluun viittaavaksi ER-tietolähteeksi, <strong>FILTER(Vendors, Vendors.VendGroup = &quot;40&quot;)</strong> palauttaa toimittajaluettelon, joka kuuluu toimittajaryhmään 40. Jos <strong>Toimittaja</strong> määritetään VendTable-tauluun viittaavaksi ER-tietolähteeksi ja ER-tietolähteeksi määritetty <strong>parmVendorBankGroup</strong> palauttaa <strong>String</strong>-tietotyypin arvon, <strong>FILTER (Vendor.'&lt;Relations'.VendBankAccount, Vendor.'&lt;Relations'.VendBankAccount.BankGroupID = parmVendorBankGroup)</strong> palauttaa luettelon vain niistä toimittajatileistä, jotka kuuluvat tiettyyn pankkiryhmään.</td>
</tr>
</tbody>
</table>

### <a name="logical-functions"></a>Loogiset toiminnot

| Toiminto | kuvaus | Esimerkki |
|----------|-------------|---------|
| CASE (lauseke, valinta 1, tulos 1 \[, valinta 2, tulos 2\]... \[, oletustulos\]) | Laskee määritetyn lausekkeen arvon määritetyille vaihtoehtoisille valinnoille. Palauttaa sen valinnan tuloksen, joka on sama kuin lausekkeen arvo. Muussa tapauksessa palautetaan oletustulos, jos oletustulos on määritetty. (Oletustulos on viimeinen parametri, jonka jälkeen ei tule valintaa). | **CASE( DATETIMEFORMAT( NOW(), "MM"), "10", "WINTER", "11", "WINTER", "12", "WINTER", "")** palauttaa merkkijonon **TALVI**, kun nykyisen Finance and Operations -istunnon päivämäärä on loka- ja joulukuun välissä. Muussa tapauksessa se palauttaa tyhjän merkkijonon. |
| IF (ehto, arvo 1, arvo 2) | Palauttaa ensimmäisen määritetyn arvon, kun määritetyt ehdot täyttyvät. Muussa tapauksessa palautetaan toinen määritetty arvo. Jos arvo 1 ja arvo 2 ovat tietueita tai tietueluetteloita, tuloksessa on vain kentät, jotka ovat molemmissa luetteloissa. | **IF (1=2, "ehto täyttyy", "ehto ei täyty")** palauttaa merkkijonon **"ehto ei täyty"**. |
| NOT (ehto) | Palauttaa määritetyn ehdon käänteisen loogisen arvon. | **NOT (TOSI)** palauttaa arvon **EPÄTOSI**. |
| AND (ehto 1\[, ehto 2, ...\]) | Palauttaa arvon **TOSI**, jos *kaikki* määritetyt ehdot ovat tosia. Muussa tapauksessa palauttaa **EPÄTOSI**-arvon. | **AND (1=1, "a"="a")** palauttaa arvon **TOSI**. **AND (1=2, "a"="a")** palauttaa arvon **EPÄTOSI**. |
| OR (ehto 1\[, ehto 2, ...\]) | Palauttaa arvon **EPÄTOSI**, jos *kaikki* määritetyt ehdot ovat epätosia. Palauttaa arvon **TOSI**, jos *jokin* määritetyistä ehdoista on tosi. | **OR (1=2, "a"="a")** palauttaa arvon **TOSI**. |
| VALUEIN (syöte, luettelo, luettelokohteen lauseke) | Määrittää, vastaako määritetty syöte määritetyn luettelokohteen jotakin arvoa. **TOSI** palautetaan, jos määritetty syöte vastaa ainakin yhden tietueen tulosta, joka saadaan suorittamalla määritetty lauseke. Muussa tapauksessa palauttaa **EPÄTOSI**-arvon. **Syöte**-parametri viittaa tietolähde-elementin polkuun. Tämän elementin arvon vastaavuus määritetään. **Luettelo**-parametri viittaa tietueluettelotyypin tietolähde-elementin polkuun lausekkeen sisältävänä tietueluettelona. Tämä elementin arvoa verrataan määritettyyn syötteeseen. **Luettelokohteen lauseke** -argumentti viittaa lausekkeeseen, joka joko osoittaa yhteen määritetyn luettelon kenttään tai sisältää sen. Vastaavuus määritetään tämän kentän perusteella. | Esimerkkejä on seuraavaksi tulevassa kohdassa [Esimerkkejä: VALUEIN (syöte, luettelo, luettelokohteen lauseke)](#examples-valuein-input-list-list-item-expression). |

#### <a name="examples-valuein-input-list-list-item-expression"></a>Esimerkkejä: VALUEIN (syöte, luettelo, luettelokohteen lauseke)
Yleensä **VALUEIN**-funktio muunnetaan **OR**-ehtojoukoksi:

(input = list.item1.value) OR (input = list.item2.value) OR …

##### <a name="example-1"></a>Esimerkki 1
Mallin yhdistämismäärityksessä määritetään seuraava tietolähde: **Luettelo** (**Laskettu kenttä** -tyyppi). Tässä tietolähteessä on lauseke **SPLIT ("a,b,c", ",")**.

Kun tietolähde, joka on määritetty **VALUEIN ("B", List, List.Value)** -lausekkeena, kutsutaan, se palauttaa arvon **TOSI**. Tässä tapauksessa **VALUEIN**-funktio muunnetaan seuraavaksi ehtojoukoksi:

**(("B" = "a") tai ("B" = "b") tai ("B" = "c"))**, jossa **("B" = "b")** on yhtä kuin **TOSI**

Kun tietolähde, joka on määritetty **VALUEIN ("B", List, LEFT(List.Value, 0))** -lausekkeena, kutsutaan, se palauttaa arvon **EPÄTOSI**. Tässä tapauksessa **VALUEIN**-funktio muunnetaan seuraavaksi ehdoksi:

**(”B” = ””)**, joka ei ole sama kuin **TOSI**

Huomaa, että kyseisen ehdon tekstin suurin merkkimäärä on 32 768 merkkiä. Älä tämän vuoksi luo tietolähteitä, jotka voivat ylittää suorituksen aikana tämän rajan. Jos raja ylitetään, sovellus pysähtyy ja annetaan poikkeus. Tämä tilanne voi esiintyä esimerkiksi silloin, jos tietolähteeksi on määritetty **WHERE (List1, VALUEIN (List1.ID, List2, List2.ID)** ja **List1**- ja **List2**-luetteloissa on suuria määriä tietueita.

Joissakin tapauksissa **VALUEIN**-funktio muunnetaan tietokantalausekkeeksi **EXISTS JOIN** -operaattorin avulla. Näin tapahtuu, kun käytetään **FILTER**-funktiota ja seuraavat ehdot täyttyvät:

- **KYSY KYSELYÄ** -asetus on poistettu käytöstä siinä **VALUEIN**-funktion tietolähteessä, joka viittaa tietueluetteloon. (Tässä tietolähteessä ei käytetä suorituksen aikana mitään lisäehtoja.)
- Tietueluetteloon viittaavaan **VALUEIN**-funktion tietolähteeseen ei ole määritetty upotettuja lausekkeita.
- **VALUEIN**-funktion luettelokohde viittaa määritetyn tietolähteen kenttään (eikä lausekkeeseen tai menetelmään).

Harkitse tämän vaihtoehdon käyttöä **WHERE**-funktion sijaan aiemmin tässä esimerkissä kuvatulla tavalla.

##### <a name="example-2"></a>Esimerkki 2

Määritä seuraavat tietolähteet omassa mallimäärityksessäsi:

- **In** (**Taulukkotietueet**-tyyppi), joka viittaa Intrastat-tauluun
- **Port** (**Taulukkotietueet**-tyyppi), joka viittaa IntrastatPort-tauluun

Kun **FILTER (In, VALUEIN(In.Port, Port, Port.PortId)** -lausekkeena määritetty tietolähde kutsutaan, luodaan seuraava SQL-lauseke palauttamaan Intrastat-taulun suodatetut tietueet:

```
select … from Intrastat
exists join TableId from IntrastatPort
where IntrastatPort.PortId = Intrastat.Port
```

**dataAreaId**-kenttien lopullinen SQL-lauseke luodaan käyttämällä **IN**-operaattoria.

##### <a name="example-3"></a>Esimerkki 3

Määritä seuraavat tietolähteet omassa mallimäärityksessäsi:

- **Le** (**Laskettu kenttä** -tyyppi), joka sisältää lausekkeen **SPLIT ("DEMF,GBSI,USMF", ",")**
- **In** (**Taulukkotietueet**-tyyppi), joka viittaa Intrastat-tauluun ja jonka **Yritysten välinen** -asetus on otettu käyttöön

Kun **FILTER (In, VALUEIN (In.dataAreaId, Le, Le.Value)** -lausekkeena määritetty tietolähde kutsutaan, lopullinen SQL-lauseke sisältää seuraavan ehdon:

```
Intrastat.dataAreaId IN ('DEMF', 'GBSI', 'USMF')
```

### <a name="mathematical-functions"></a>Matemaattinen toiminto

| Toiminto | kuvaus | Esimerkki |
|----------|-------------|---------|
| ABS (numero) | Palauttaa määritetyn luvun itseisarvon. (Toisin sanoen palautettavalla luvulla ei ole etumerkkiä.) | **ABS (-1)** palauttaa arvon **1**. |
| POWER (numero, potenssi) | Palauttaa tuloksen, joka on nostettu määritettyyn positiiviseen potenssiin. | **POWER (10, 2)** palauttaa arvon **100**. |
| NUMBERVALUE (merkkijono, desimaalierotin, numeron ryhmittelyin erotin) | Muuntaa määritetyn merkkijonon numeroksi. Määritettyä desimaalia käytetään desimaaliluvun kokonais- ja murtolukuosien välissä. Määritettyä numeroryhmittelyn erotinta käytetään tuhaterottimena. | **NUMBERVALUE("1 234,56", ",", " ")** palauttaa arvon **1234.56**. |
| VALUE (merkkijono) | Muuntaa määritetyn merkkijonon numeroksi. Pilkkuja ja pisteitä (.) pidetään desimaalierottimina. Alussa olevaa tavuviivaa (-) pidetään miinusmerkkinä. Annetaan poikkeus, jos määritetyssä merkkijonossa on muita kuin numeerisia merkkejä. | **VALUE ("1 234,56")** antaa poikkeuksen. |
| ROUND (numero, desimaalit) | Palauttaa määritetyn numeron sen jälkeen, kun se on pyöristetty määritettyyn määrään desimaaleja:<ul><li>Jos **desimaali**-parametrien arvo on yli 0 (nolla), numero pyöristetään kyseiseen määrään desimaaleja.</li><li>Jos **desimaali**-parametrin arvo on **0** (nolla), numero pyöristetään lähimpään kokonaislukuun.</li><li>Jos **desimaali**-parametrin arvo on vähemmän kuin 0 (nolla), numero pyöristetään desimaalipilkusta vasemmalle.</li></ul> | **ROUND (1200.767, 2)** pyöristää kahteen desimaaliin ja palauttaa arvon **1200.77**. **ROUND (1200.767, -3)** pyöristää lähimpään tuhanteen ja palauttaa arvon **1000**. |
| ROUNDDOWN (numero, desimaalit) | Palauttaa määritetyn luvun sen jälkeen, kun se on pyöristetty alaspäin määritettyyn määrään desimaaleja.<blockquote>[!NOTE] Tämä funktio toimii kuin **ROUND**, mutta se pyöristää määritetyn numeron aina alaspäin (kohti nollaa).</blockquote> | **ROUNDDOWN (1200.767, 2)** pyöristää alaspäin kahteen desimaaliin ja palauttaa arvon **1200.76**. **ROUNDDOWN (1700.767, -3)** pyöristää alaspäin lähimpään tuhanteen ja palauttaa arvon **1000**. |
| ROUNDUP (numero, desimaalit) | Palauttaa määritetyn luvun sen jälkeen, kun se on pyöristetty ylöspäin määritettyyn määrään desimaaleja.<blockquote>[!NOTE] Tämä funktio toimii kuin **ROUND**, mutta se pyöristää määritetyn numeron aina ylöspäin (pois päin nollasta).</blockquote> | **ROUNDUP (1200.763, 2)** pyöristää ylöspäin kahteen desimaaliin ja palauttaa arvon **1200.77**. **ROUNDUP (1200.767, -3)** pyöristää ylöspäin lähimpään tuhanteen ja palauttaa arvon **2000**. |

### <a name="data-conversion-functions"></a>Tietojen muuntotoiminnot

| Toiminto | kuvaus | Esimerkki |
|----------|-------------|---------|
| VALUE (merkkijono) | Muuntaa määritetyn merkkijonon numeroksi. Pilkkuja ja pisteitä (.) pidetään desimaalierottimina. Alussa olevaa tavuviivaa (-) pidetään miinusmerkkinä. Annetaan poikkeus, jos määritetyssä merkkijonossa on muita kuin numeerisia merkkejä. | **VALUE ("1 234,56")** antaa poikkeuksen. |
| NUMBERVALUE (merkkijono, desimaalierotin, numeron ryhmittelyin erotin) | Muuntaa määritetyn merkkijonon numeroksi. Määritettyä desimaalia käytetään desimaaliluvun kokonais- ja murtolukuosien välissä. Määritettyä numeroryhmittelyn erotinta käytetään tuhaterottimena. | **NUMBERVALUE("1 234,56", ",", " ")** palauttaa arvon **1234.56**. |
| INTVALUE (merkkijono) | Palauttaa määritetyn merkkijonon kokonaislukumuodon. Kaikki desimaalit lyhennetään. | **INTVALUE ("100.77")** palauttaa arvon **100**. |
| INTVALUE (numero) | Palauttaa määritetyn luvun kokonaislukumuodon. Kaikki desimaalit lyhennetään. | **INTVALUE (-100.77)** palauttaa arvon **-100**. |
| INT64VALUE (merkkijono) | Palauttaa määritetyn merkkijonon int64-muodon. Kaikki desimaalit lyhennetään. | **INT64VALUE ("22565422744")** palauttaa arvon **22565422744**. |
| INT64VALUE (numero) | Palauttaa määritetyn luvun int64-muodon. Kaikki desimaalit lyhennetään. | **INT64VALUE (22565422744.00)** palauttaa arvon **22565422744**. |

### <a name="record-functions"></a>Tallennustoiminnot

| Toiminto | kuvaus | Esimerkki |
|----------|-------------|---------|
| NULLCONTAINER (luettelo) | Palauttaa **tyhjän** tietueen, jonka rakenne on sama kuin määritetyn tietueluettelon tai tietueen.<blockquote>[!NOTE] Tämä toiminto on vanhentunut. Käytä sen sijaan **EMPTYRECORD**-toimintoa.</blockquote> | **NULLCONTAINER (SPLIT ("abc", 1))** palauttaa uuden tyhjän tietueen, jonka rakenne on sama kuin **SPLIT**-toiminnon palauttamalla luettelolla. |
| EMPTYRECORD (tietue) | Palauttaa **tyhjän** tietueen, jonka rakenne on sama kuin määritetyn tietueluettelon tai tietueen.<blockquote>[!NOTE] **Tyhjä**-tietue on tietue, jossa kaikissa kentissä on tyhjä arvo. Tyhjä arvo numeroilla **0** (nolla), merkkijonoilla tyhjä merkkijono jne.</blockquote> | **EMPTYRECORD (SPLIT ("abc", 1))** palauttaa uuden tyhjän tietueen, jonka rakenne on sama kuin **SPLIT**-toiminnon palauttamalla luettelolla. |

### <a name="text-functions"></a>Tekstitoiminnot

<table>
<thead>
<tr>
<th>Toiminto</th>
<th>kuvaus</th>
<th>Esimerkki</th>
</tr>
</thead>
<tbody>
<tr>
<td>UPPER (merkkijono)</td>
<td>Palauttaa määritetyn merkkijonon sen jälkeen, kun se on muutettu isoiksi kirjaimiksi.</td>
<td><strong>UPPER(&quot;Sample&quot;)</strong> palauttaa arvon <strong>&quot;SAMPLE&quot;</strong>.</td>
</tr>
<tr>
<td>LOWER (merkkijono)</td>
<td>Palauttaa määritetyn merkkijonon sen jälkeen, kun se on muutettu pieniksi kirjaimiksi.</td>
<td><strong>LOWER (&quot;Sample&quot;)</strong> palauttaa arvon <strong>&quot;sample&quot;</strong>.</td>
</tr>
<tr>
<td>LEFT (merkkijono, merkkien määrä)</td>
<td>Palauttaa määritetyn määrän merkkejä merkkijonon alusta.</td>
<td><strong>LEFT (&quot;Sample&quot;, 3)</strong> palauttaa arvon <strong>&quot;Sam&quot;</strong>.</td>
</tr>
<tr>
<td>RIGHT (merkkijono, merkkien määrä)</td>
<td>Palauttaa määritetyn määrän merkkejä merkkijonon lopusta.</td>
<td><strong>RIGHT (&quot;Sample&quot;, 3)</strong> palauttaa arvon <strong>&quot;ple&quot;</strong>.</td>
</tr>
<tr>
<td>MID (merkkijono, alkukohta, merkkien määrä)</td>
<td>Palauttaa määritetyn määrän merkkejä määritetyn merkkijonon tietystä kohdasta.</td>
<td><strong>MID (&quot;Sample&quot;, 2, 3)</strong> palauttaa arvon <strong>&quot;amp&quot;</strong>.</td>
</tr>
<tr>
<td>LEN (merkkijono)</td>
<td>Palauttaa määritetyn merkkijonon merkkien määrän.</td>
<td><strong>LEN (&quot;Sample&quot;)</strong> palauttaa arvon <strong>6</strong>.</td>
</tr>
<tr>
<td>CHAR (numero)</td>
<td>Palauttaa merkkijonon, johon määritetty unicode-numero viittaa.</td>
<td><strong>CHAR (255)</strong> palauttaa arvon <strong>&quot;ÿ&quot;</strong>.
<blockquote>[!NOTE] Tämän funktion palauttama merkkijono määräytyy koodauksen mukaan, joka on valittu ylemmän tason FILE-muotoisessa elementissä. Luettelo tuetuista koodauksista on kohdassa <a href="https://msdn.microsoft.com/en-us/library/system.text.encoding(v=vs.110).aspx">Koodausluokka</a>.</blockquote>
</td>
</tr>
<tr>
<td>CONCATENATE (1 merkkijono [, merkkijono 2, …])</td>
<td>Palauttaa kaikki määritetyt tekstimerkkijonot sen jälkeen, kun ne on liitetty yhteen merkkijonoon.</td>
<td><strong>CONCATENATE (&quot;abc&quot;, &quot;def&quot;)</strong> palauttaa arvon <strong>&quot;abcdef&quot;</strong>.
<blockquote>[!NOTE] Myös lauseke <strong>&quot;abc&quot; &amp; &quot;def&quot;</strong> palauttaa lausekkeen <strong>&quot;abcdef&quot;</strong>.</blockquote>
</td>
</tr>
<tr>
<td>TRANSLATE (merkkijono, malli, korvaus)</td>
<td>Palauttaa määritetyn merkkijonon sen jälkeen, kun määritetyn mallimerkkijonon kaikkien merkkien esiintymät korvataan määritetyn korvausmerkkijonon vastaavassa kohdassa olevilla merkeillä.</td>
<td><strong>TRANSLATE (&quot;abcdef&quot;, &quot;cd&quot;, &quot;GH&quot;)</strong> korvaa mallin <strong>&quot;cd&quot;</strong> merkkijonolla <strong>&quot;GH&quot;</strong> ja palauttaa arvon <strong>&quot;abGHef&quot;</strong>.</td>
</tr>
<tr>
<td>REPLACE (merkkijono, malli, korvaus, säännönmukaisen lausekkeen merkki)</td>
<td>Palauttaa määritetyn merkkijonon sen jälkeen, kun määritetty <strong>säännöllisen lausekkeen merkki</strong> on <strong>tosi</strong>. Merkkijonoa muokataan kohdistamalla säännöllinen lauseke, joka on määritetty tämän toiminnon <strong>malliargumentiksi</strong>. Tätä lauseketta käytetään etsittäessä korvattavia merkkejä. Määritetyn <strong>korvausargumentin</strong> merkkejä käytetään löydettyjen merkkien korvaamisessa. Kun määritetyn <strong>säännöllisen lausekkeen merkki</strong> on <strong>epätosi</strong>, tämä toiminto toimii kuten <strong>TRANSLATE</strong>.</td>
<td><strong>REPLACE (&quot;+1 923 456 4971&quot;, &quot;[^0-9]&quot;, &quot;&quot;, true)</strong> on käytössä säännöllisessä lausekkeessa, joka poistaa kaikki muut kuin numeeriset merkit ja palauttaa arvon <strong>&quot;19234564971&quot;</strong>. <strong>REPLACE (&quot;abcdef&quot;, &quot;cd&quot;, &quot;GH&quot;, false)</strong> korvaa mallin <strong>&quot;cd&quot;</strong> merkkijonolla <strong>&quot;GH&quot;</strong> ja palauttaa arvon <strong>&quot;abGHef&quot;</strong>.</td>
</tr>
<tr>
<td>TEXT (syöte)</td>
<td>Palauttaa määritetyn syötteen sen jälkeen, kun se on muunnettu tekstimerkkijonoksi. Se puolestaan muotoillaan nykyisen Finance and Operations -esiintymän palvelimen aluekohtaisten asetusten perusteella. <strong>Reaali</strong>-tyyppisten arvojen merkkijonon muunnos on rajoitettu kahteen desimaaliin.</td>
<td>Jos Finance and Operations -esiintymän palvelimen aluekohtaisiksi asetuksiksi on määritetty <strong>FI-FI</strong>, <strong>TEXT (NOW ())</strong> palauttaa nykyisen Finance and Operations -istunnon päivämäärän 17.12.2015 tekstimerkkijonona <strong>&quot;17.12.2015 07.59.23&quot;</strong>. <strong>TEXT (1/3)</strong> palauttaa arvon <strong>&quot;0.33&quot;</strong>.</td>
</tr>
<tr>
<td>FORMAT (merkkijono 1, merkkijono 2[, merkkijono 3, …])</td>
<td>Palauttaa määritetyn merkkijonon sen jälkeen, kun se on muotoiltu korvaamalla kaikki <strong>%N</strong>-esiintymät <em>n</em>:llä argumentilla. Argumentit ovat merkkijonoja. Jos parametrille ei ole annettu argumenttia, parametri palautetaan merkkijonoon arvona <strong>&quot;%N&quot;</strong>. <strong>Reaali</strong>-tyyppisten arvojen merkkijonon muunnos on rajoitettu kahteen desimaaliin.</td>
<td>Seuraavassa kuvassa <strong>PaymentModel</strong>-tietolähde palauttaa asiakastietueluettelon <strong>Asiakas</strong>-komponentin kautta ja käsittelyn päivämäärän arvon <strong>ProcessingDate</strong>-kentän kautta.
<p><a href="./media/picture-format-datasource.jpg"><img src="./media/picture-format-datasource.jpg" alt="PaymentModel data source" class="alignnone wp-image-290751 size-full" width="293" height="143" /></a></p>
<p>ER-muodossa, joka on suunniteltu sähköisen tiedoston luomiseen valituille asiakkaille, tietolähteeksi valitaan <strong>PaymentModel</strong>. Se ohjaa prosessin kulkua. Loppukäyttäjille annettu poikkeus ilmaisee, kun valittu asiakas pysäytetään raportin käsittelypäivämääränä. Tälle käsittelyn ohjausobjektin tyypille muotoiltua kaavaa käytetään seuraavissa resursseissa:</p>
<ul>
<li>Finance and Operationsin otsikko SYS70894, jossa on seuraava teksti:
<ul>
<li><strong>Kielelle EN-US:</strong> &quot;Nothing to print&quot;</li>
<li><strong>Kielelle FI:</strong> &quot;Ei mitään tulostettavaa&quot;</li>
</ul></li>
<li>Finance and Operationsin otsikko SYS18389, jossa on seuraava teksti:
<ul>
<li><strong>Kielelle EN-US:</strong> Customer %1 is stopped for %2.</li>
<li><strong>Kielelle FI:</strong> Asiakas %1 on pysäytetty %2.</li>
</ul></li>
</ul>
<p>Tässä on kaava, jota voi muotoilla:</p>
<p>FORMAT (CONCATENATE (@&quot;SYS70894&quot;, &quot;. &quot;, @&quot;SYS18389&quot;), model.Customer.Name, DATETIMEFORMAT (model.ProcessingDate, &quot;d&quot;))</p>
<p>Jos raporttia käsitellään asiakkaalle <strong>Litware Retail</strong> 17.12.2015 ja maa-asetuksina on <strong>EN-US</strong> ja kielenä on <strong>EN-US</strong>, tämä kaava palauttaa seuraavan tekstin, joka voidaan esittää poikkeussanomana käyttäjälle:</p>
<p>&quot;Nothing to print. Customer Litware Retail is stopped for 12/17/2015.&quot;</p>
<p>Jos sama raportti käsitellään asiakkaalle <strong>Litware Retail</strong> 17.12.2015 ja maa-asetuksina on <strong>FI</strong> ja kielenä on <strong>FI</strong>, tämä kaava palauttaa seuraavan tekstin, jossa on eri päivämäärämuoto:</p>
<p>&quot;Ei tulostettavaa. Debitor 'Litware Retail' wird für 17.12.2015 gesperrt.&quot;</p>
<blockquote>[!NOTE] Otsikoiden ER-kaavoissa käytetään seuraavaa syntaksia:
<ul>
<li><strong>Finance and Operations -resurssien otsikot:</strong> <strong>@&quot;X&quot;</strong>, jos <strong>X</strong> on sovellusobjektipuun (AOT) otsikon tunnus.</li>
<li><strong>ER-määrityksissä sijaitsevat otsikot:</strong> <strong>@&quot;GER_LABEL:X&quot;</strong>, jossa <strong>X</strong> on ER-määrityksen otsikon tunnus.</li>
</ul>
</blockquote>
</td>
</tr>
<tr>
<td>NUMBERFORMAT (numero, muoto)</td>
<td>Palauttaa määritetyssä muodossa olevan määritetyn numeron merkkijonomuodon. (Lisätietoja tuetuista muodoista: <a href="https://msdn.microsoft.com/en-us/library/dwhawy9k(v=vs.110).aspx">vakio</a> ja <a href="https://msdn.microsoft.com/en-us/library/0c899ak8(v=vs.110).aspx">mukautettu</a>.)</td>
<td>Maa-asetuksella EN-US <strong>NUMBERFORMAT (0.45, &quot;p&quot;)</strong> palauttaa arvon <strong>&quot;45.00 %&quot;</strong>. <strong>NUMBERFORMAT (10.45, &quot;#&quot;)</strong> palauttaa arvon <strong>&quot;10&quot;</strong>.</td>
</tr>
<tr>
<td>NUMERALSTOTEXT (määrä, kieli, valuutta, tulosta valuutan nimi -merkki, desimaalit)</td>
<td>Palauttaa määritetyn luvun sen jälkeen, kun se kirjoitettu (muunnettu) määritetyllä kielellä tekstimerkkijonoksi. Kielikoodi on valinnainen. Kun se on määritetty tyhjänä merkkijonona, suorituskontekstin kielikoodia käytetään. (Suorituskontekstin kielikoodi määritetään muodostettavalla kansiolle tai tiedostolle.) Myös valuuttakoodi on valinnainen. Kun se on määritetty tyhjänä merkkijonona, käytetään yrityksen valuuttaa.
<blockquote>[!NOTE] <strong>Tulosta valuutan nimimerkintä</strong>- ja <strong>Desimaalit</strong>-parametrit analysoidaan vain seuraaville kielikoodeille: <strong>CS</strong>, <strong>ET</strong>, <strong>HU</strong>, <strong>LT</strong>, <strong>LV</strong>, <strong>PL</strong> ja <strong>RU</strong>. <strong>Tulosta valuutan nimimerkintä</strong> -parametri analysoidaan vain niissä Finance and Operations -yrityksissä, joiden maa- tai alueyhteys tukee valuutan nimen taivutusta.</blockquote>
</td>
<td><strong>NUMERALSTOTEXT (1234.56, &quot;EN&quot;, &quot;&quot;, false, 2)</strong> palauttaa arvon <strong>&quot;One Thousand Two Hundred Thirty Four and 56&quot;</strong>. <strong>NUMERALSTOTEXT (120, &quot;PL&quot;, &quot;&quot;, false, 0)</strong> palauttaa arvon <strong>&quot;Sto dwadzieścia&quot;</strong>. <strong>NUMERALSTOTEXT (120.21, &quot;RU&quot;, &quot;EUR&quot;, true, 2)</strong> palauttaa arvon <strong>&quot;Сто двадцать евро 21 евроцент&quot;</strong>.</td>
</tr>
<tr>
<td>PADLEFT (merkkijono, pituus, täyttömerkit)</td>
<td>Palauttaa määritetyn pituisen merkkijonon, jossa määritetyn merkkijonon alkua on täydennetty määritetyillä merkeillä.</td>
<td><strong>PADLEFT (&quot;1234&quot;, 10, &quot;&nbsp;&quot;)</strong> palauttaa tekstimerkkijonon <strong>&quot;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1234&quot;</strong>.</td>
</tr>
<tr>
<td>TRIM (merkkijono)</td>
<td>Palauttaa määritetyn tekstimerkkijonon sen jälkeen, kun edeltävät ja lopussa olevat välilyönnit on poistettu ja sanojen välissä olevat moninkertaiset välilyönnit on poistettu.</td>
<td><strong>TRIM (&quot;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Sample&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;text&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&quot;)</strong> palauttaa arvon <strong>&quot;Sample text&quot;</strong>.</td>
</tr>
<tr>
<td>GETENUMVALUEBYNAME (luetteloinnin tietolähteen polku, luettelointiarvon etikettiteksti)</td>
<td>Palauttaa määritetyn luetteloinnin tietolähteen luettelointiotsikon määritetyn tekstin perusteella.</td>
<td>Seuraavassa kuvassa on tietomallin <strong>ReportDirection</strong>-luettelointi. Huomaa, että luettelointiarvoille on määritetty otsikot.
<p><a href="./media/ER-data-model-enumeration-values.PNG"><img src="./media/ER-data-model-enumeration-values.PNG" alt="Available values for data model enumeration" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a></p>
<p>Seuraavassa kuvassa on nämä tiedot:</p>
<ul>
<li>Mallin luettelointi <strong>ReportDirection</strong> lisätään raporttiin tietolähteenä <strong>$Direction</strong>.</li>
<li>ER-lauseke <strong>$IsArrivals</strong> on suunniteltu käyttämään mallin luettelointia tämän toiminnon parametrina. Lausekkeen arvo on <strong>TOSI</strong>.</li>
</ul>
<a href="./media/ER-data-model-enumeration-usage.PNG"><img src="./media/ER-data-model-enumeration-usage.PNG" alt="Example of data model enumeration" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a>
</td>
</tr>
<tr>
<td>GUIDVALUE (syöte)</td>
<td>Muuntaa <strong>String</strong>-tietotyypin määritetyn syötteen <strong>GUID</strong>-tietotyypin tietokohteeksi.<blockquote>[!NOTE] Voit tehdä muunnon vastakkaiseen suuntaan käyttämällä <strong>TEXT()</strong>-funktiota. (<strong>GUID</strong>-tietotyypin määritetty syöte siis muunnetaan <strong>String</strong>-tietotyypin tietokohteeksi.)</blockquote></td>
<td>Määritä seuraavat tietolähteet omassa mallimäärityksessäsi:
<ul>
<li><strong>myID</strong> (<strong>Laskettu kenttä</strong> -tyyppi), ,joka sisältää lausekkeen <strong>GUIDVALUE(&quot;AF5CCDAC-F728-4609-8C8B- A4B30B0C0AA0&quot;)</strong></li>
<li><strong>Users</strong> (<strong>Taulukkotietueet</strong>-tyypi), joka viittaa UserInfo-tauluun</li>
</ul>
Kun nämä tietolähteet määritetään, voit käyttää lauseketta kuten <strong>FILTER (Users, Users.objectId = myID)</strong> suodattaaksesi UserInfo-taulun <strong>objectId</strong>-kentän mukaan, joka on <strong>GUID</strong>-tietotyyppiä.
</td>
</tr>
<tr>
<td>JSONVALUE (tunnus, polku)</td>
<td>Jäsennä tiedot JavaScript Object Notation (JSON) -muodossa, jota käyettään tietyssä polussa, jotta voidaan purkaa skalaariarvo, joka perustuu tiettyyn tunnukseen.</td>
<td>Tietolähde <strong>$JsonField</strong> sisältää seuraavat tiedot JSON-muodossa: <strong>{&quot;BuildNumber&quot;:&quot;7.3.1234.1&quot;, &quot;KeyThumbprint&quot;:&quot;7366E&quot;}</strong>. Tälle tietotyypille </strong>JSONVALUE ( &quot;BuildNumber&quot;, $JsonField)</strong> palauttaa arvon <strong>7.3.1234.1</strong>, joka on<strong>String</strong>-tietotyyppiä.</td>
</tr>
</tbody>
</table>

### <a name="data-conversion-functions"></a>Tietojen muuntotoiminnot

| Toiminto | kuvaus | Esimerkki |
|----------|-------------|---------|
| TEXT (syöte) | Palauttaa määritetyn syötteen sen jälkeen, kun se on muunnettu tekstimerkkijonoksi. Se puolestaan muotoillaan nykyisen Finance and Operations -esiintymän palvelimen aluekohtaisten asetusten perusteella. **Reaali**-tyyppisten arvojen merkkijonon muunnos on rajoitettu kahteen desimaaliin. | Jos Finance and Operations -esiintymän palvelimen aluekohtaisiksi asetuksiksi on määritetty **FI-FI**, **TEXT (NOW ())** palauttaa nykyisen Finance and Operations -istunnon päivämäärän 17.12.2015 tekstimerkkijonona **"17.12.2015 07.59.23"**. **TEXT (1/3)** palauttaa arvon **"0.33"**. |
| QRCODE (merkkijono) | Palauttaa määritetyn merkkijonon Quick Response Code (QR) -koodin kuvan base64-binaarimuodossa. | **QRCODE ("Sample text")** palauttaa arvon **U2FtcGxlIHRleHQ=**. |

### <a name="data-collection-functions"></a>Tietojen keruutoiminnot

| Toiminto | kuvaus | Esimerkki |
|----------|-------------|---------|
| FORMATELEMENTNAME () | Palauttaa nykyisen muodon elementin nimen. Palauttaa tyhjän merkkijonon, jos nykyisten tiedostojen **Kerää tulostiedot** -merkintä on poistettu käytöstä. | Lisätietoja tämän toiminnon käytöstä on tehtäväoppaassa **ER Käytä tulostusmuotoa laskennassa ja summauksessa**, joka on osa **IT-palvelujen ja -ratkaisujen komponenttien hankkiminen ja kehittäminen** -liiketoimintaprosessia. |
| SUMIFS (summauksen avainmerkkijono, ehtoalueen1 merkkijono,ehdon arvon1 merkkijono \[, ehtoalueen2 merkkijono,ehdon arvon2 merkkijono, …\]) | Palauttaa XML-solmujen arvojen summan (jossa nimi on määritetty avaimeksi), joka on kerätty tämän muodon suorittamisen aikana ja joka täyttää määritetyt ehdot (alue- ja arvoparit). Palauttaa **0** (nolla) -arvon, jos nykyisten tiedostojen **Kerää tulostiedot** -merkintä on poistettu käytöstä. | |
| SUMIF (summauksen avainmerkkijono, ehtoalueen merkkijono, ehdon arvon merkkijono) | Palauttaa XML-solmujen arvojen summan (jossa nimi on määritetty avaimeksi), joka on kerätty tämän muodon suorittamisen aikana ja joka täyttää määritetyt ehdon (alue ja arvo). Palauttaa **0** (nolla) -arvon, jos nykyisten tiedostojen **Kerää tulostiedot** -merkintä on poistettu käytöstä. | |
| COUNTIFS (ehtoalueen1 merkkijono,ehdon arvon1 merkkijono \[, ehtoalueen2 merkkijono,ehdon arvon2 merkkijono, …\]) | Palauttaa XML-solmujen määrän, joka on kerätty tämän muodon suorittamisen aikana ja joka täyttää määritetyt ehdot (alue- ja arvoparit). Palauttaa **0** (nolla) -arvon, jos nykyisten tiedostojen **Kerää tulostiedot** -merkintä on poistettu käytöstä. | |
| COUNTIF (ehtoalueen merkkijono,ehdon arvon merkkijono) | Palauttaa XML-solmujen määrän, joka on kerätty tämän muodon suorittamisen aikana ja joka täyttää määritetyn ehdon (alue ja arvopari). Palauttaa **0** (nolla) -arvon, jos nykyisten tiedostojen **Kerää tulostiedot** -merkintä on poistettu käytöstä. | |
| COLLECTEDLIST (ehtoalueen1 merkkijono,ehdon arvon1 merkkijono \[, ehtoalueen2 merkkijono,ehdon arvon2 merkkijono, …\]) | Palauttaa XML-solmujen arvoluettelon, joka kerättiin tämän muodon suorittamisen aikana ja joka täyttää määritetyn ehdon (alue ja arvopari). Palauttaa tyhjän luettelon, jos nykyisten tiedostojen **Kerää tulostiedot**-merkintä on poistettu käytöstä. | |

### <a name="other-business-domainspecific-functions"></a>Muut (liiketoiminnan toimialuekohtaiset) toiminnot

| Toiminto | kuvaus | Esimerkki |
|----------|-------------|---------|
| CONVERTCURRENCY (summa, lähdevaluutta, kohdevaluutta, päivämäärä, yritys) | Määritetty rahasumma muunnetaan lähdevaluutasta määritettyyn kohdevaluuttaan käyttämällä määritetyn Finance and Operations -yrityksen asetuksia tiettynä päivänä. | **CONVERTCURRENCY (1, "EUR", "USD", TODAY(), "DEMF")** palauttaa yhden euron suuruisen määrän Yhdysvaltojen dollareita nykyisen istunnon päivämääränä DEMF-yrityksen asetusten perusteella. |
| ROUNDAMOUNT (määrä, desimaalit, pyöristyssääntö) | Pyöristää määritetyn summan määritetyllä desimaalitarkkuudella määritetyn pyöristyssäännön mukaisesti.<blockquote>[!NOTE] Pyöristyssääntö on määritettävä Finance and Operations **RoundOffType**-luetteloinnin arvoksi.</blockquote> | Jos **model.RoundOff**-parametrin arvoksi on määritetty **Alaspäin**, **ROUNDAMOUNT (1000.787, 2, model.RoundOff)** palauttaa arvon **1000.78**. Jos **model.RoundOff**-parametrin arvoksi on määritetty **Normaali** tai **Ylöspäin**, **ROUNDAMOUNT (1000.787, 2, model.RoundOff)** palauttaa arvon **1000.79**. |
| CURCredRef (numerot) | Palauttaa laskuttajan viitteen määritetyn laskunumeron lukujen perusteella. | **CURCredRef ("VEND-200002")** palauttaa arvon **"2200002"**. |
| MOD\_97 (numerot) | Palauttaa laskuttajan viitteen MOD97-lausekkeena määritetyn laskunumeron lukujen perusteella. | **MOD\_97 ("VEND-200002")** palauttaa arvon **"20000285"**. |
| ISOCredRef (numerot) | Palauttaa laskuttajan ISO (International Organization for Standardization) -viitteen määritetyn laskunumeron lukujen ja kirjainmerkkien perusteella.<blockquote>[!NOTE] Voit poistaa ne aakkosmerkit, jotka eivät ole ISO-yhteensopivia, jos syöttöparametri on käännetty ennen kuin se välitetään tälle toiminnolle.</blockquote> | **ISOCredRef ("VEND-200002")** palauttaa arvon **"RF23VEND-200002"**. |
| CN\_GBT\_AdditionalDimensionID (merkkijono, lukumäärä) | Hae määritetty taloushallinnon lisädimension tunnus. **String**-parametrissa dimensiot esitetään pilkuin erotettuina tunnuksina. **Number**-parametri määrittää pyydetyn dimension järjestyskoodin tässä merkkijonossa. | **CN\_GBT\_AdditionalDimensionID ("AA,BB,CC,DD,EE,FF,GG,HH",3)** palauttaa arvon **"CC"**. |
| GetCurrentCompany () | Palauttaa sen yrityksen koodin tekstimuodon, johon käyttäjä on tällä hetkellä kirjautunut. | **GETCURRENTCOMPANY ()** palauttaa arvon **USMF** käyttäjälle, joka on kirjautunut Finance and Operations -yritykseen **Contoso Entertainment System USA**. |
| CH\_BANK\_MOD\_10 (merkkiä) | Palauttaa laskuttajan viitteen MOD10-lausekkeena määritetyn laskunumeron lukujen perusteella. | **CH\_BANK\_MOD\_10 ("VEND-200002")** palauttaa arvon **3**. |
| FA\_SUM (käyttöomaisuuden koodi, arvomallin koodi, alkamispäivämäärä, päättymispäivämäärä) | Palauttaa määritetyn kauden käyttöomaisuussummien valmistellun tietosäilön. | **FA\_SUM ("COMP-000001", "Current", Date1, Date2)** palauttaa käyttöomaisuuden **"COMP-000001"** valmistellun tietosäilön, jonka arvomalli on **“Current”** kaudella **Date1** - **Date2**. |
| FA\_BALANCE (käyttöomaisuuden koodi, arvomallin koodi, raportointivuosi, raportointipäivä) | Palauttaa käyttöomaisuuden saldon valmistellun tietosäilön. Raportointivuosi on määritettävä Finance and Operationsin luettelointiarvona **AssetYear**. | **FA\_SUM ("COMP-000001", "Current", AxEnumAssetYear.ThisYear, SESSIONTODAY ())** palauttaa käyttöomaisuuden **COMP-000001** saldojen valmistellun tietosäilön, jonka arvomalli on **Current** kyseisenä Finance and Operations -istunnon päivämääränä. |
| TABLENAME2ID (merkkijono) | Palauttaa määritetyn taulun nimen taulukkotunnuksen kokonaislukumuodon. | **TABLENAME2ID ("Intrastat")** palauttaa arvon **1510**. |
| ISVALIDCHARACTERISO7064 (merkkijono) | Palauttaa totuusarvon **TOSI**, kun määritetty merkkijono vastaa kelvollista kansainvälistä tilinumeroa (IBAN). Muussa tapauksessa palautetaan totuusarvo **EPÄTOSI**. | **ISVALIDCHARACTERISO7064 ("AT61 1904 3002 3457 3201")** palauttaa arvon **TOSI**. **ISVALIDCHARACTERISO7064 ("AT61")** palauttaa arvon **EPÄTOSI**. |
| NUMSEQVALUE (numerosarjan koodi, vaikutusalue, vaikutusalueen tunnus) | Palauttaa numerosarjan juuri luodun arvon määritetyn numerosarjan koodin, vaikutusalueen ja vaikutusalueen tunnuksen perusteella. Vaikutusalue on määritettävä **ERExpressionNumberSequenceScopeType**-luetteloinnin arvona (**Jaettu**, **Yritys** tai **Yhtiö**). Määritä **Jaettu**-vaikutusalueelle tyhjä merkkijonoa vaikutusalueen tunnuksena. Määritä **Yhtiö**- ja **Yritys**-vaikutusalueille yhtiön koodi vaikutusalueen tunnuksena. Jos määrität **Yhtiö**- ja **Yritys**-vaikutusalueille tyhjän merkkijono vaikutusalueen tunnuksena, käytetään nykyistä yhtiön koodia. | Määritä seuraavat tietolähteet omassa mallimäärityksessäsi:<ul><li>**enumScope** (**Dynamics 365 for Operationsin luettelointi** -tyyppi), joka viittaa **ERExpressionNumberSequenceScopeType**-luettelointiin.</li><li>**NumSeq** (**Laskettu kenttä** -tyyppi), joka sisältää lausekkeen **NUMSEQVALUE ("Gene\_1", enumScope.Company, "")**</li></ul>Kun **NumSeq**-tietolähde kutsutaan, se palauttaa juuri luodun **Gene\_1**-numerosarjan arvon. Tämä arvo määritettiin yritykselle, ja se antaa kontekstin, jossa ER-muoto suoritetaan. |
| NUMSEQVALUE (numerosarjan koodi) | Palauttaa juuri luodun numerosarjan arvon. Tämä arvo perustuu määritettyyn numerosarjaan, **Yhtiö**-vaikutusalueeseen ja (vaikutusalueen tunnuksena) sen yrityksen koodiin, joka antaa kontekstin, jossa ER-muoto suoritetaan. | Mallin yhdistämismäärityksessä määritetään seuraava tietolähde: **NumSeq** (**Laskettu kenttä** -tyyppi). Tässä tietolähteessä on lauseke **NUMSEQVALUE ("Gene\_1")**. Kun **NumSeq**-tietolähde kutsutaan, se palauttaa juuri luodun **Gene\_1**-numerosarjan arvon. Tämä arvo määritettiin yritykselle, ja se antaa kontekstin, jossa ER-muoto suoritetaan. |
| NUMSEQVALUE (numerosarjan tietuetunnus) | Palauttaa numerosarjan juuri luodun arvon määritetyn numerosarjan tietuetunnuksen perusteella. | Määritä seuraavat tietolähteet omassa mallimäärityksessäsi:<ul><li>**LedgerParms** (**Taulu**-tyyppi), joka viittaa LedgerParameters-tauluun</li><li>**NumSeq** (**Laskettu kenttä** -tyyppi), joka sisältää lausekkeen **NUMSEQVALUE (LedgerParameters.'numRefJournalNum()'.NumberSequenceId)**</li></ul>Kun **NumSeq**-tietolähde kutsutaan, se palauttaa juuri luodun numerosarjan arvon. Tämä arvo määritettiin sen yrityksen kirjanpitoparametreissa, ja se antaa kontekstin, jossa ER-muoto suoritetaan. Tämä numerosarja yksilöi kirjauskansiot ja toimii tapahtumat yhteen liittävänä eränumerona. |

### <a name="functions-list-extension"></a>Toimintojen luettelon laajennus

ER:n avulla on mahdollista laajentaa luetteloa toiminnoista, joita käytetään ER-lausekkeissa. Tähän tarvitaan jonkin verran suunnittelutyötä. Lisätietoja on kohdassa [Sähköisen raportoinnin toimintojen luettelon laajentaminen](general-electronic-reporting-formulas-list-extension.md).

## <a name="additional-resources"></a>Lisäresurssit

- [Sähköisen raportoinnin yleiskatsaus](general-electronic-reporting.md)
- [Sähköisen raportoinnin (ER) toimintojen luettelon laajentaminen](general-electronic-reporting-formulas-list-extension.md)
