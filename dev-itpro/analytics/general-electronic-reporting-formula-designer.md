---
title: "Kaavojen suunnittelutoiminto sähköisessä raportoinnissa"
description: "Tässä aiheessa kerrotaan, miten kaavojen suunnittelutoimintoa käytetään sähköisessä raportoinnissa (ER). Kun tietyn sähköisen asiakirjan muotoa suunnitellaan ER:ssä, käytössä ovat Microsoftin Excel-tyyppiset kaavat, joiden avulla tiedot voidaan muuntaa vastaamaan asiakirjan toteuttamis- ja muotoiluvaatimuksia. Erityyppisiä toimintoja tuetaan - teksti, päivämäärä ja kellonaika, looginen, matemaattisia tietoja, tietojen muuntamisen ja muut (yrityksen toimialueeseen liittyvät toiminnot)."
author: kfend
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: ac8d6c064ca826cc1c2fed07578ca9ce0c66ef66
ms.lasthandoff: 03/31/2017


---

# <a name="formula-designer-in-electronic-reporting"></a>Kaavojen suunnittelutoiminto sähköisessä raportoinnissa

Tässä aiheessa kerrotaan, miten kaavojen suunnittelutoimintoa käytetään sähköisessä raportoinnissa (ER). Kun tietyn sähköisen asiakirjan muotoa suunnitellaan ER:ssä, käytössä ovat Microsoftin Excel-tyyppiset kaavat, joiden avulla tiedot voidaan muuntaa vastaamaan asiakirjan toteuttamis- ja muotoiluvaatimuksia. Erityyppisiä toimintoja tuetaan - teksti, päivämäärä ja kellonaika, looginen, matemaattisia tietoja, tietojen muuntamisen ja muut (yrityksen toimialueeseen liittyvät toiminnot).

<a name="formula-designer-overview"></a>Yleiskatsaus kaavan suunnittelutoimintoon
-------------------------

Sähköinen raportointi (ER) tukee kaavojen suunnittelutoimintoa. Tämän vuoksi voit määrittää suunnittelun yhteydessä lausekkeita, joita voidaan käyttää suorituksen aikana seuraavissa tehtävissä:

-   Microsoft Dynamics 365 for Operations -tietokannasta vastaanotettujen tietojen muuntaminen. Tiedot täytetään ER-tietomalliin, joka on suunniteltu ER-muotojen (suodatus, ryhmittely, tietotyypin muunnos jne.) tietolähteeksi
-   Niiden tietojen muotoileminen, jotka on lähetettävä luotavaan sähköiseen asiakirjaan tietyn ER-muodon asettelun ja ehtojen mukaisesti (pyydetyn kielen tai kulttuurin, koodauksen jne. mukaisesti)
-   Sähköisten asiakirjojen luontiprosessin (tiettyjen muodon elementtien tuloksen käyttöön ottaminen ja käytöstä poistaminen riippuen käsiteltävistä tiedoista, asiakirjan luonnin keskeyttämisestä, sanomien näyttäminen loppukäyttäjille jne.) hallitseminen.

Kaavojen suunnittelutoiminnon sivu voidaan avata, kun teet seuraavaa:

-   Tietolähteen nimikkeiden sidonta tietomallin komponentteihin
-   Tietolähteen nimikkeiden sidonta muotokomponentteihin
-   Laskettujen kenttien täydellinen ylläpito tietolähteiden osana
-   Käyttäjän syöttöparametrien näkyvyyden ehtojen määritys
-   Muodon muunnosten rakenne
-   Muotokomponenttien ehtojen käyttöönottamisen määritys
-   Muodon tiedostokomponenttien tiedostonimien määritys
-   Prosessin hallinnan tarkistusten ehtojen määritys
-   Prosessin hallinnan tarkistusten sanoman tekstin määritys

## <a name="designing-er-formulas"></a>ER-kaavojen suunnitteleminen
### <a name="data-binding"></a>Tietojen sidonta

ER-kaavojen suunnittelutoiminnon avulla voi määrittää lausekkeen, joka muuntaa tietolähteistä vastaanotetut tiedot niin, että tiedot voidaan täyttää tietojen käyttäjään suorituksen aikana:

-   Dynamics 365 for Operations -tietolähteistä ja suorituksen aikaisista parametreista ER-tietomalliin
-   ER-tietomallista ER-muotoon
-   Dynamics 365 for Operations -tietolähteistä ja suorituksen aikaisista parametreista ER-muotoon

Seuraavassa kuvassa esitellään tämäntyyppisen lausekkeen rakenne. Tässä esimerkissä lauseke palauttaa **Intrastat.AmountMST**-kentän arvon Dynamics 365 for Operationsin **Intrastat**-taulusta sen jälkeen, kun arvo on pyöristetty kahteen desimaaliin. [![Kuva-lauseke-sidonnan](./media/picture-expression-binding.jpg)](./media/picture-expression-binding.jpg) seuraavassa kuvassa näkyy, miten tämän lajin lauseke voidaan käyttää. Tässä esimerkissä suunniteltu lausekkeen tulos on täytetty **Transaction.InvoicedAmount** komponentin **ALV-raportoinnin model** tietomallin. [![Kuva-lauseke-binding2](./media/picture-expression-binding2.jpg)](./media/picture-expression-binding2.jpg) suorituksen aikana suunniteltu kaava **PYÖREÄ (Intrastat.AmountMST 2)**, pyöristää arvon **AmountMST** kentän jokaisen tietueen kohdalla **Intrastat** taulukon kahden desimaalin tarkkuudella ja täyttää pyöristetty arvo **Transaction.InvoicedAmount** komponentin **veroraporteissa** tietomallin.

### <a name="data-formatting"></a>Tietojen muotoilu

ER-kaavojen suunnittelutoiminnon avulla voi määrittää lausekkeen, joka muotoilee tietolähteistä vastaanotetut tiedot niin, että tiedot voidaan lähettää sähköisen asiakirjan luonnin osana. Jos määritettynä on muotoiluja, jotka on kohdistettava muodolle uudelleenkäytettävänä tyypillisenä sääntönä, voit käyttää muotoilua kerran muotoilukonfiguraatiossa nimettynä muunnoksena, jolla on muotoilulauseke. Tämän jälkeen nimetty muunnos voidaan linkittää useisiin muotokomponentteihin, joiden tulosten on oltava luodun lausekkeen mukaisesti muotoiltuja. Seuraavassa kuvassa esitellään tämäntyyppisen muotoilun rakenne. Tässä esimerkissä **TrimmedString**-muunnos ottaa saapuvat **merkkijono**-tyyppiset tiedot ja lyhentää ylimääräiset välilyönnit alusta ja lopusta, kun merkkijonon arvo palautetaan. [![Kuva-muunnos-rakenteen](./media/picture-transformation-design.jpg)](./media/picture-transformation-design.jpg) seuraavassa kuvassa näkyy, miten tämän tyypin muunnosta voi käyttää. Tässä esimerkissä useat muotokomponentit, jotka lähettävät tekstin tuloksena sähköisen asiakirjan luontiin suorituksen aikana, viittaavat **TrimmedString**-muunnokseen nimen mukaan. [![Kuva-muunnos-käyttö](./media/picture-transformation-usage.jpg)](./media/picture-transformation-usage.jpg) jolloin muodon osat viittaavat ** TrimmedString ** muunnos (esimerkiksi **partyName** edellisessä kuvassa osa) tämä lähettää tekstin lähtönä luotaessa asiakirja. Teksti ei sisällä edeltäviä eikä lopussa olevia välilyöntejä. Jos sinulla on muotoiluja, joita tulee kohdistaa yksitellen, voit käyttää muotoilua tietyn muotokomponentin sidonnan yksittäisenä lausekkeena. Seuraavassa kuvassa esitellään tämäntyyppinen lauseke. Tässä esimerkissä **partyType**-muotokomponentti on sidottu tietolähteeseen sen lausekkeen kautta, joka muuntaa saapuvat tiedot tietolähteen **Model.Company.RegistrationType**-kentästä isoilla kirjaimilla kirjoitetuksi tekstiksi ja lähettää tekstin tulosteena sähköiseen asiakirjaan. [![Kuva-sidonta-ja-kaava](./media/picture-binding-with-formula.jpg)](./media/picture-binding-with-formula.jpg)

### <a name="process-flow-control"></a>Prosessinkulun hallinta

ER-kaavojen suunnittelutoimintoa voidaan käyttää määritettäessä lausekkeita, joita käytetään hallitsemaan asiakirjojen luonnin prosessinkulkua. Voit tehdä seuraavat toimet:

-   Määritä ehdot, jotka määrittävät, milloin asiakirjan luontiprosessi on pysäytettävä.
-   Määritä lausekkeet, jotka luovat loppukäyttäjälle sanomia pysäytetyistä prosesseista tai näyttävät suorituslokin sanomia raportin luontiprosessin jatkamisesta.
-   Määritä asiakirjojen luonnin tiedostonimet ja ohjaa niiden luontiehtoja.

Jokainen prosessinkulun hallinnan sääntö suunnitellaan yksittäiseksi tarkistukseksi. Seuraavassa kuvassa esitellään tämäntyyppinen tarkistus. Tässä on kyseisen esimerkin konfiguraation selitys:

-   Tarkistus arvioidaan, kun **INSTAT**-solmu luodaan XML-tiedoston luonnin yhteydessä.
-   Jos tapahtumaluettelo on tyhjä, tarkistus pysäyttää suoritusprosessin ja palauttaa **EPÄTOSI**-arvon.
-   Tarkistus palauttaa virhesanoman otsikolla SYS70894 käyttäjän ensisijaisella kielellä.

[![Kuva-vahvistus](./media/picture-validation.jpg)](./media/picture-validation.jpg) ER reseptin suunnittelua voidaan myös luotaessa sähköisen asiakirjan tiedostonimi ja määrittää tiedoston luontia. Seuraavassa kuvassa esitellään tämäntyyppisen prosessikulun hallinnan rakenne. Tässä on kyseisen esimerkin konfiguraation selitys:

-   Tietueluettelo **model.Intrastat**-tietolähteestä jaetaan eriin. Yksi erä voi sisältää korkeintaan 1 000 tietuetta.
-   Tulos luo zip-tiedoston, joka sisältää yhden XML-muodossa olevan tiedoston jokaisessa luodussa erässä.
-   Lauseke palauttaa sähköisen asiakirjan luomiselle tiedostonimen liittämällä tiedostonimen ja tiedoston tunnisteen. Toisen erän ja seuraavien erien tiedostonimi sisältää erän tunnuksen loppuliitteenä.
-   Lauseke ottaa käyttöön (palauttamalla **TOSI**-arvon) tiedoston luontiprosessin erille, jotka sisältävät vähintään yhden tietueen.

[![Kuva-tiedosto-control](./media/picture-file-control.jpg)](./media/picture-file-control.jpg)

### <a name="basic-syntax"></a>Perussyntaksi

ER-lausekkeet voivat sisältää joitakin seuraavia elementtejä tai kaikki seuraavat elementit:

-   Vakiot
-   Operaattorit
-   Viitteet
-   Polut
-   Toiminnot

#### <a name="constants"></a>Vakiot

Voit käyttää teksti- ja numeerisia vakioita (arvoja, joita ei lasketa), kun suunnittelet lausekkeita. Esimerkiksi lauseke ** ("100") arvo + 20 ** käyttää numeerinen vakio 20 ja vakio "100"-merkkijonon ja palauttaa numeerisen arvon **120**. ER-kaavojen suunnittelutoiminto tukee ohitusjärjestyksiä, joten voit määrittää, että osaa lausekkeen merkkijonosta tulee käsitellä eri tavalla. Esimerkiksi lauseke **"Leo Tolstoi ""Sota ja rauha"" Osa 1"** palauttaa tekstimerkkijonon **Leo Tolstoi "Sota ja rauha" Osa 1**.

#### <a name="operators"></a>Operaattorit

Seuraavassa taulukossa näkyvät aritmeettiset operaattorit, joita voi käyttää matemaattisten perusoperaattoreiden, kuten lisäyksen, vähennyksen, jakolaskun ja kertolaskun suorittamiseen.

| Operaattori | Merkitys              | Esimerkki |
|----------|----------------------|---------|
| +        | Lisäys             | 1+2     |
| -        | Vähennyksen negaatio | 5-2 -1  |
| \*       | Kertolasku       | 7\*8    |
| /        | Jaosto             | 9/3     |

Seuraava taulukko sisältää vertailuoperaattorit, joita tuetaan. Niitä voi käyttää kahden arvon vertaamisessa.

| Operaattori | Merkitys                  | Esimerkki    |
|----------|--------------------------|------------|
| =        | Yhtä suuri                    | X=Y        |
| &gt;     | Suurempi kuin             | X&gt;Y     |
| &lt;     | Pienempi kuin                | X&lt;Y     |
| &gt;=    | Suurempi tai yhtä suuri | X&gt;=Y    |
| &lt;=    | Pienempi tai yhtä suuri    | X&lt;=Y    |
| &lt;&gt; | Ei sama kuin             | X&lt;&gt;Y |

Lisäksi &-merkkiä voidaan käyttää tekstin ketjutusoperaattorina, joka liittää tai yhdistää yhden tai useamman tekstimerkkijonon yksittäiseen tekstikappaleeseen.

| Operaattori | Merkitys     | Esimerkki                                        |
|----------|-------------|------------------------------------------------|
| &        | Liitä | "Ei tulostettavaa" & ": " & "tietueita ei löytynyt" |

#### <a name="operator-precedence"></a>Operaattoreiden käsittelyjärjestys

Järjestys, jossa yhdistelmälausekkeen osat lasketaan, on tärkeä. Esimerkiksi tulos lauseke ** 1 + 4 / 2 ** vaihtelee sen mukaan onko yhteenlasku tai jakaminen suoritetaan ensin. Sulkeiden avulla voit määrittää, miten lauseke lasketaan. Jos haluat esimerkiksi osoittaa, että yhteenlaskutoiminto suoritetaan ensin, voit muokata edeltävän lausekkeen muotoon **(1 + 4) / 2**. Jos lausekkeen toimintojen suoritusjärjestystä ei ole määritetty eksplisiittisesti, järjestys perustuu oletusarvoiseen tukioperaattoreiden määrittämään käsittelyjärjestykseen. Seuraavassa taulukossa esitellään operaattorit ja niihin liitetyt käsittelyjärjestykset. Operaattorit, joilla on korkeampi käsittelyjärjestys (esimerkiksi 7) suoritetaan ennen operaattoreita, joilla on alempi käsittelyjärjestys (esimerkiksi 1).

| Järjestys | Operaattorit      | Syntaksi                                                   |
|------------|----------------|----------------------------------------------------------|
| 7          | Ryhmittely       | ( … )                                                    |
| 6          | Jäsenen käyttöoikeus  | … Neuvo kaikkia ryhmän jäseniä käynnistämään <token>Axapta</token>-asiakasohjelma uudelleen. …                                                    |
| 5          | Funktiokutsu  | … ( … )                                                  |
| 4          | Kertova | … \* … … / …                                             |
| 3          | Lisä       | … + … … - …                                              |
| 2          | Vertailu     | … &lt; … … &lt;= … … =&gt; … … &gt; … … = … … &lt;&gt; … |
| 1          | Erottelu     | … , …                                                    |

Samalla rivillä olevilla operaattoreilla on sama käsittelyjärjestys. Jos lauseke sisältää useamman kuin yhden näistä operaattoreista, lauseke lasketaan vasemmalta oikealle. Esimerkiksi lauseke **1 + 6 / 2 \*3 &gt;5** palauttaa **tosi**. Suosittelemme sulkeiden käyttämistä, kun lausekkeiden haluttu laskentajärjestys halutaan ilmaista ja kun lausekkeista halutaan tehdä helpommin luettavia ja ylläpidettäviä.

#### <a name="references"></a>Viitteet

Kaikkia nykyisen ER-komponentin (joko malli tai muoto) tietolähteitä, jotka ovat käytettävissä lausekkeen suunnittelun yhteydessä, voidaan käyttää nimettyinä viitteinä. Esimerkiksi nykyinen ER-tietomalli sisältää **ReportingDate**-tietolähteen, joka palauttaa **DATETIME**-tietotyypin arvon. Voit muotoilla asiakirjaa luotaessa arvo oikein, voit viitata lausekkeen tietolähde seuraavasti: **DATETIMEFORMAT (ReportingDate, "pp-kk-vvvv")** viittaava tietolähteen nimen, kaikki merkit, jotka kuvaavat aakkosten kirjain ei täytyy edeltää heittomerkki ('). Jos tietolähteeseen viittaava nimi sisältää vähintään yhden merkin, joka ei vastaa (esimerkiksi välimerkit tai muut merkit kirjallista) aakkosten kirjain, nimi on kirjoitettava puolilainausmerkkeihin. Seuraavassa on muutamia esimerkkejä:

-   **Tämän päivän päivämäärä & aika** -tietolähteeseen on viitattava ER-lausekkeessa seuraavasti: **'Tämän päivän päivämäärä & aika'**
-   **Asiakkaat**-tietolähteen **name()**-menetelmän on viitattava ER-lausekkeeseen seuraavasti: **Customers.'name()'**

#### <a name="path"></a>Polku

Kun lauseke viittaa rakenteelliseen tietolähteeseen, polun määritettä voidaan käyttää valittaessa tietolähteen tietty primitiivinen elementti. Piste (.) -merkkiä käytetään erottamaan rakenteisen tietolähteen yksittäiset elementit. Esimerkiksi nykyinen ER-tietomalli sisältää **InvoiceTransactions**-tietolähteen, joka palauttaa tietueluettelon. ** InvoiceTransactions**-tietuerakenne sisältää **AmountDebit**- ja **AmountCredit**-kentän, jotka palauttavat numeerisia arvoja. Voit siis suunnitella seuraavan lausekkeen, jolla lasketaan laskutettu määrä: **InvoiceTransactions.AmountDebit - InvoiceTransactions.AmountCredit**

#### <a name="functions"></a>Toiminnot

Seuraavassa osassa esitellään toiminnot, joita voidaan käyttää ER-lausekkeissa. Kaikkia lausekekontekstin (nykyinen ER-tietomalli tai ER-muoto) tietolähteitä, ja myös rajoituksia, voidaan käyttää kutsuvien toimintojen parametreina kutsutoimintoargumenttien luettelon mukaisesti. Esimerkiksi nykyinen ER-tietomalli sisältää **InvoiceTransactions**-tietolähteen, joka palauttaa tietueluettelon. ** InvoiceTransactions**-tietuerakenne sisältää **AmountDebit**- ja **AmountCredit**-kentän, jotka palauttavat numeerisia arvoja. Voit siis laskea laskutetun määrän suunnittelemalla seuraavan lausekkeen, jossa käytetään sisäänrakennettua ER-pyöristystoimintoa: **PYÖRISTYS (InvoiceTransactions.AmountDebit - InvoiceTransactions.AmountCredit, 2)**

## <a name="supported-functions"></a>Tuetut toiminnot
Seuraavassa taulukossa esitellään tietojenkäsittelytoiminnot, jotka ovat käytettävissä ER-tietomallien ja ER-raporttien suunnitteluun. Toimintoluettelo ei ole pysyvä, vaan kehittäjät voivat laajentaa sitä. ER-kaavojen suunnittelutoiminto -ruudusta löydät käytettävissä olevien toimintojen luettelon.

### <a name="date-and-time-functions"></a>Päivämäärä- ja aikatoiminnot

| Toiminto                                   | Kuvaus                                                                                                                                                                                                                                                                                                                                                      | Esimerkki                                                                                                                                                                                                                                                                                               |
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ADDDAYS (päivämäärä ja aika, päivät)                   | Lisää määritetylle päivämäärän ja ajan arvolle määritetty päivien lukumäärä.                                                                                                                                                                                                                                                                                                | **ADDDAYS (NOW(), 7)** palauttaa päivämäärän ja ajan seitsemän päivän kuluttua.                                                                                                                                                                                                                            |
| DATETODATETIME (päivämäärä)                      | Muuntaa määritetyn päivämäärän arvon päivämäärän ja ajan arvoksi.                                                                                                                                                                                                                                                                                                            | **DATETODATETIME (CompInfo. ' getCurrentDate()')** palauttaa nykyisen Dynamics 365 työvaiheiden istunnon päivämäärä, 12/24/2015 **24/12/2015 12:00:00 AM**. Tässä esimerkissä **CompInfo** on ** 365 for Operations / taulukko** -tyypin ER-tietolähde, joka viittaa CompanyInfo-taulukkoon. |
| NOW ()                                     | Palauttaa nykyisen Dynamics 365 for Operations -sovelluspalvelimen päivämäärän ja kellonajan päivämäärä/aika-arvona.                                                                                                                                                                                                                                                             |                                                                                                                                                                                                                                                                                                       |
| TODAY ()                                   | Palauttaa nykyisen Dynamics 365 for Operations -sovelluspalvelimen päivämäärän päivämäärä-arvona.                                                                                                                                                                                                                                                                          |                                                                                                                                                                                                                                                                                                       |
| NULLDATE ()                                | Palauttaa **tyhjän** päivämäärän arvon.                                                                                                                                                                                                                                                                                                                                    |                                                                                                                                                                                                                                                                                                       |
| NULLDATETIME ()                            | Palauttaa **tyhjän** päivämäärän ja ajan arvon.                                                                                                                                                                                                                                                                                                                                |                                                                                                                                                                                                                                                                                                       |
| DATETIMEFORMAT (päivämäärä ja aika, muoto)          | Muunna määritetty päivämäärän ja ajan arvo tietyssä muodossa olevaksi merkkijonoksi. (Lisätietoja tuetuista muodoista on kohdassa [vakio](https://msdn.microsoft.com/en-us/library/az4se3k1(v=vs.110).aspx) ja [mukautettu](https://msdn.microsoft.com/en-us/library/8kb3ddd4(v=vs.110).aspx).)                                                                        | **DATETIMEFORMAT (NOW(), "pp-kk vvvv")** palauttaa nykyisen Dynamics 365 for Operations -sovelluspalvelimen päivämäärän 24.12.2015 **"24-12 2015"** määritetyn mukautetun muodon mukaisesti.                                                                                                          |
| DATETIMEFORMAT (päivämäärä ja aika, maa-asetukset) | Muunna määritetty päivämäärän ja ajan arvo merkkijonoksi, joka on määritetyssä muodossa ja jolla on määritetyt [maa-asetukset](https://msdn.microsoft.com/en-us/goglobal/bb896001.aspx). (Lisätietoja tuetuista muodoista on kohdassa [vakio](https://msdn.microsoft.com/en-us/library/az4se3k1(v=vs.110).aspx) ja [mukautettu](https://msdn.microsoft.com/en-us/library/8kb3ddd4(v=vs.110).aspx).) | **DATETIMEFORMAT (NOW(), "d", "de")** palauttaa nykyisen Dynamics 365 for Operations -sovelluspalvelimen päivämäärän 24.12.2015 **"24.12.2015"** valitun Saksan maa-asetuksen mukaisesti.                                                                                                             |
| SESSIONTODAY ()                            | Palauttaa nykyisen Dynamics 365 for Operations -istunnon päivämäärän päivämäärän arvona.                                                                                                                                                                                                                                                                                      |                                                                                                                                                                                                                                                                                                       |
| SESSIONNOW ()                              | Palauttaa nykyisen Dynamics 365 for Operations -istunnon päivämäärän ja kellonajan päivämäärä/aika-arvona.                                                                                                                                                                                                                                                                         |                                                                                                                                                                                                                                                                                                       |
| DATEFORMAT (päivämäärä, muoto)                  | Palauttaa päivämäärän merkkijonoesityksen käyttämällä määritettyä muotoa.                                                                                                                                                                                                                                                                                                    | **DATEFORMAT (SESSIONTODAY (), "dd-MM-yyyy")** palauttaa nykyisen Dynamics 365 for Operations -sovelluspalvelimen päivämäärän 24.12.2015 “**24-12-2015**” määritetyn mukautetun muodon mukaisesti.                                                                                                                      |
| DATEFORMAT (päivämäärä, muoto, maa-asetus)         | Muunna määritetty päivämäärän arvo merkkijonoksi, joka on määritetyssä muodossa ja jolla on määritetyt [maa-asetukset](https://msdn.microsoft.com/en-us/goglobal/bb896001.aspx). (Lisätietoja tuetuista muodoista on kohdassa [vakio](https://msdn.microsoft.com/en-us/library/az4se3k1(v=vs.110).aspx) ja [mukautettu](https://msdn.microsoft.com/en-us/library/8kb3ddd4(v=vs.110).aspx).)     | **DATETIMEFORMAT (SESSIONNOW (), "d", "de")** palauttaa nykyisen Dynamics 365 for Operations -istunnon päivämäärän 24.12.2015 **“24.12.2015”** valitun Saksan maa-asetuksen mukaisesti.                                                                                                                       |

### <a name="list-functions"></a>Luettelotoiminnot

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Toiminto</th>
<th>kuvaus</th>
<th>Esimerkki</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>SPLIT (syöte, pituus)</td>
<td>Jaa määritetty syötemerkkijono alimerkkijonoiksi, joilla on tietty pituus. Palauttaa tuloksen uutena luettelona.</td>
<td><strong>Jaa (&quot;abcd&quot;, 3)</strong> palauttaa luettelon, joka koostuu kaksi tietuetta, joilla <strong>MERKKIJONON</strong> kenttä. Ensimmäisen tietueen kentässä on teksti <strong>&quot;abc&quot;</strong>, ja toisessa tietueen kentässä teksti <strong>&quot;d&quot;</strong>.</td>
</tr>
<tr class="even">
<td>SPLITLIST (luettelo, numero)</td>
<td>Jaa määritetty luettelo eriksi, joissa on tietty määrä tietueita. Palauttaa tuloksen uutena eräluettelona, joka sisältää seuraavat elementit:
<ul>
<li>Erät tavallisina luetteloina (<strong>arvo</strong>-komponentti)</li>
<li>Nykyinen eränumero (<strong>BatchNumber</strong>-komponentti)</li>
</ul></td>
<td>Seuraavassa esimerkissä <strong>Rivit</strong>-tietolähde luodaan tietueluettelona, joka sisältää kolme tietuetta. Se on jaettu eriin, joista jokainen sisältää enintään kaksi tietuetta. <a href="./media/picture-splitlist-datasource.jpg"><img src="./media/picture-splitlist-datasource.jpg" alt="Data source that is divided into batches" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a>Tämä on suunniteltu muoto, asettelu jossa sidontoja <strong>rivien</strong> tietolähde luodaan, jos haluat luoda XML-muodossa, joka esittää yksittäisten solmut ja jokaisen erän tietueet. <a href="./media/picture-splitlist-format.jpg"><img src="./media/picture-splitlist-format.jpg" alt="Format layout that has bindings to a data source" class="alignnone wp-image-290691 size-full" width="374" height="161" /></a>Seuraavassa on suunniteltu muoto tulos. <a href="./media/picture-splitlist-result.jpg"><img src="./media/picture-splitlist-result.jpg" alt="Result of running the format" class="alignnone wp-image-290701 size-full" width="358" height="191" /></a></td>
</tr>
<tr class="odd">
<td>LIST (tietue 1 [, tietue 2, ...])</td>
<td>Palauttaa uuden luettelon, joka on luotu määritetyistä argumenteista.</td>
<td><strong>LIST (model.MainData, model.OtherData)</strong> palauttaa tyhjän tietueen, jonka sisältämä kenttäluettelo sisältää kaikki <strong>MainData</strong>- ja <strong>OtherData</strong>-tietueluettelon kentät.</td>
</tr>
<tr class="even">
<td>LISTJOIN (luettelo 1, luettelo 2, ...)</td>
<td>Palauttaa yhdistetyn luettelon, joka on luotu määritettyjen argumenttien luetteloista.</td>
<td><strong>LISTJOIN (Jaa (&quot;abc&quot;, 1), Jaa (&quot;def&quot;, 1))</strong> palauttaa kuusi tietueiden luettelo, kun yksi kenttään <strong>MERKKIJONON</strong> tietotyyppi on kirjain.</td>
</tr>
<tr class="odd">
<td>ISEMPTY (luettelo)</td>
<td>Palauttaa <strong>TOSI</strong>-arvon, jos määritetty luettelo ei sisällä yhtään elementtiä. Muussa tapauksessa palauttaa <strong>EPÄTOSI</strong>-arvon.</td>
<td></td>
</tr>
<tr class="even">
<td>EMPTYLIST (luettelo)</td>
<td>Palauttaa tyhjän luettelon käyttämällä määritettyä luetteloa luettelorakenteen lähteenä.</td>
<td><strong>EMPTYLIST (Jaa (&quot;abc&quot;, 1))</strong> palauttaa uusi tyhjä luettelo, jossa on sama rakenne kuin luettelo, joka palautetaan <strong>jakaa</strong> funktio.</td>
</tr>
<tr class="odd">
<td>FIRST (luettelo)</td>
<td>Palauttaa määritetyn luettelon ensimmäisen tietueen, jos kyseinen tietue ei ole tyhjä. Muussa tapauksessa annetaan poikkeus.</td>
<td></td>
</tr>
<tr class="even">
<td>FIRSTORNULL (luettelo)</td>
<td>Palauttaa määritetyn luettelon ensimmäisen tietueen, jos kyseinen tietue ei ole tyhjä. Muussa tapauksessa palauttaa <strong>tyhjän</strong> tietueen.</td>
<td></td>
</tr>
<tr class="odd">
<td>LISTOFFIRSTITEM (luettelo)</td>
<td>Palauttaa luettelon, joka sisältää vain määritetyn luettelon ensimmäisen nimikkeen.</td>
<td></td>
</tr>
<tr class="even">
<td>ALLITEMS (polku)</td>
<td>Palauttaa uuden tasoitetun luettelon, joka edustaa kaikkia nimikkeitä, jotka vastaavat määritettyä polkua. Polku on määritettävä sallituksi tietolähteen poluksi tietueluettelo-tietotyypin tietolähteen elementtiin. Polku merkkijono-, päivämäärä- ym. tietoelementteihin käynnistää virheen suunnitteluaikana ER-lausekkeenmuodostimessa.</td>
<td>Jos syötät <strong>jakaa (&quot;abcdef&quot;, 2)</strong> (DS) tietolähteenä <strong>määrä (ALLITEMS (DS. (Arvo))</strong> palauttaa <strong>3</strong>.</td>
</tr>
<tr class="odd">
<td>ORDERBY (luettelo [, lauseke 1, lauseke 2, …])</td>
<td>Palauttaa määritetyn luettelon, joka on lajiteltu sellaisten määritettyjen argumenttien perusteella, jotka on voitu määrittää lausekkeiksi.</td>
<td>Kun <strong>Toimittaja </strong>on määritetty ER-tietolähteeksi, joka viittaa VendTable-taulukkoon,<strong> ORDERBY (Vendors, Vendors.'name()')</strong> palauttaa toimittajaluettelon, joka on lajiteltu nimen mukaan nousevassa järjestyksessä.</td>
</tr>
<tr class="even">
<td>REVERSE (luettelo)</td>
<td>Palauttaa määritetyn luettelon käänteisessä lajittelujärjestyksessä.</td>
<td>Kun <strong>Toimittaja </strong>on määritetty ER-tietolähteeksi, joka viittaa VendTable-taulukkoon, <strong>REVERSE (ORDERBY (Vendors, Vendors.'name()')) )</strong> palauttaa toimittajaluettelon, joka on lajiteltu nimen mukaan laskevassa järjestyksessä.</td>
</tr>
<tr class="odd">
<td>WHERE (luettelo, ehto)</td>
<td>Palauttaa määritetyn luettelon, joka on suodatettu tietyn ehdon perusteella. Toisin kuin <strong>SUODATIN</strong>-toimintoa, määritettyä ehtoa käytetään muistissa olevaan luetteloon.</td>
<td>Kun <strong>toimittajan</strong> ER-tietolähde, joka viittaa VendTable-taulukkoon ole määritetty <strong>jossa (toimittajat, Vendors.VendGroup = &quot;40&quot;)</strong> palauttaa 40 toimittajaryhmään kuuluvien toimittajien luettelo.</td>
</tr>
<tr class="even">
<td>ENUMERATE (luettelo)</td>
<td>Palauttaa uuden luettelon, joka sisältää määritetyn luettelon numeroituja tietueita ja paljastaa seuraavat elementit:
<ul>
<li>Määritetyn luettelon tietueet tavallisina luetteloita (<strong>arvo</strong>-komponentti)</li>
<li>Nykyisen tietueen indeksi (<strong>numero</strong>-komponentti)</li>
</ul></td>
<td>Seuraavassa esimerkissä <strong>Numeroitu</strong>-tietolähde luodaan toimittajan tietueiden numeroituna luettelona <strong>Toimittajat</strong>-tietolähteestä, joka viittaa<strong>VendTable</strong>-taulukkoon. <a href="./media/picture-enumerate-datasource.jpg"><img src="./media/picture-enumerate-datasource.jpg" alt="Enumerated data source" class="alignnone wp-image-290711 size-full" width="387" height="136" /></a>Tässä on muoto, jossa tietosidonnat luodaan, jos haluat luoda XML-muodossa, joka esittää yksittäisten toimittajien Valintalistan solmuina. <a href="./media/picture-enumerate-format.jpg"><img src="./media/picture-enumerate-format.jpg" alt="Format that has data bindings" class="alignnone wp-image-290721 size-full" width="414" height="138" /></a>Tämä on seurausta käynnissä suunniteltu muodossa. <a href="./media/picture-enumerate-result.jpg"><img src="./media/picture-enumerate-result.jpg" alt="Result of running the format" class="alignnone wp-image-290731 size-full" width="567" height="176" /></a></td>
</tr>
<tr class="odd">
<td>COUNT (luettelo)</td>
<td>Palauttaa määritetyn luettelon tietueiden lukumäärän, jos luettelo ei ole tyhjä. Muussa tapauksessa palauttaa arvon <strong>0</strong> (nolla).</td>
<td><strong>MÄÄRÄ (jakaa (&quot;abcd&quot;, 3))</strong> palauttaa <strong>2</strong>, koska <strong>jakaa</strong> -toiminto luo luettelon, joka koostuu kaksi tietuetta.</td>
</tr>
<tr class="even">
<td>LISTOFFIELDS (polku)</td>
<td>Palauttaa argumentista luodun tietueluettelon, jonka tyyppi voi olla jokin seuraavista:
<ul>
<li>Mallin luettelointi</li>
<li>Muodon luettelointi</li>
<li>Kontti</li>
</ul>
Luotu luettelo koostuu tietueista, joilla on seuraavat kentät:
<ul>
<li>Nimi</li>
<li>Etiketti</li>
<li>kuvaus</li>
</ul>
Otsikko- ja Kuvaus-kentät palauttavat suorituksen aikana muodon kieliasetuksiin perustuvat arvot.</td>
<td>Seuraavassa esimerkissä kuvataan tietomalliin tuotu luettelointi. <a href="./media/ger-listoffields-function-model-enumeration.png"><img src="./media/ger-listoffields-function-model-enumeration-e1474545790761.png" alt="GER LISTOFFIELDS function - model enumeration" class="alignnone wp-image-1203943 size-full" width="514" height="155" /></a>Seuraavassa esimerkissä:
<ul>
<li>Mallin luettelointi lisätään raporttiin tietolähteenä.</li>
<li>ER-lauseke, joka on suunniteltu käyttämään mallin luettelointia tämän toiminnon parametrina.</li>
<li>Tietueluettelon tyypin tietolähde lisätään raporttiin käyttäen luotua ER-lauseketta.</li>
</ul><ph id="t1">
< href="./media/ger-listoffields-function-in-format-expression.png" ></ph><img src="./media/ger-listoffields-function-in-format-expression-e1474546110395.png" alt="GER LISTOFFIELDS function - in format expression" class="alignnone wp-image-1204033 size-full" width="549" height="318" /></a> seuraavassa esimerkissä ER muotoillaksesi osia, jotka on sidottu tietolähteen tietueiden luettelolaji, joka on luotu LISTOFFIELDS-funktiolla. <a href="./media/ger-listoffields-function-format-design.png"><img src="./media/ger-listoffields-function-format-design.png" alt="GER LISTOFFIELDS function - format design" class="alignnone size-full wp-image-1204043" width="466" height="221" /></a>On suunniteltu muoto suorittamisen tuloksen. <a href="./media/ger-listoffields-function-format-output.png"><img src="./media/ger-listoffields-function-format-output.png" alt="GER LISTOFFIELDS function - format output" class="alignnone size-full wp-image-1204053" width="585" height="158" /></a><strong>Huomautus:</strong> Translated tekstin otsikot ja kuvaukset on täytetty ER muotoilun tuotoksen mukaisesti määritetty pää tiedoston ja kansion muodossa osien asetuksia.</td>
</tr>
<tr class="odd">
<td>STRINGJOIN (luettelo, kenttänimi, erotin)</td>
<td>Palauttaa kentän yhdistettyjen arvojen merkkijonon valitulla erottimella erotetusta luettelosta.</td>
<td>Jos olet määrittänyt SPLIT(“abc” , 1) tietolähteen tietojoukoksi, lauseke STRINGJOIN (DS, DS.Value, “:”) palauttaa tuloksen “a:b:c”</td>
</tr>
<tr class="even">
<td>SPLITLISTBYLIMIT (luettelo, raja-arvo, lähderaja-arvo)</td>
<td>Jakaa luettelon uudeksi aliluetteloiden luetteloksi ja palauttaa tuloksen tietueluettelonsisältöön. Raja-arvoparametri määrittää arvon, joka jakaa alkuperäisen luettelon. Lähderaja-arvo-parametri määrittää vaiheen, jonka mukaan kokonaissummaa kasvatetaan. Rajaa ei käytetä tietyn luettelon yhteen nimikkeeseen, kun lähderaja ylittää määritetyn rajan.</td>
<td>Seuraavassa esimerkissä esitetään esimerkkimuoto tietolähteitä käyttäen. <a href="./media/ger-splitlistbylimit-format.png"><img src="./media/ger-splitlistbylimit-format.png" alt="GER SPLITLISTBYLIMIT - format" class="alignnone size-full wp-image-1204063" width="396" height="195" /></a><a href="./media/ger-splitlistbylimit-datasources.png"><img src="./media/ger-splitlistbylimit-datasources.png" alt="GER SPLITLISTBYLIMIT - datasources" class="alignnone size-full wp-image-1204073" width="320" height="208" /></a>Tämä on tulos muodossa suoritus, joka esittää kauppatavaran kohteita jäsentämätön luettelo. <a href="./media/ger-splitlistbylimit-output.png"><img src="./media/ger-splitlistbylimit-output.png" alt="GER SPLITLISTBYLIMIT - output" class="alignnone size-full wp-image-1204083" width="462" height="204" /></a>Seuraavassa esimerkissä samaa muotoa, joka esittää kauppatavaran kohteiden luettelo erät, kun yhden erän on oltava hyödykkeiden kanssa, jonka ei tulisi ylittää rajan 9 kokonaispaino on muutettu. <a href="./media/ger-splitlistbylimit-format-1.png"><img src="./media/ger-splitlistbylimit-format-1.png" alt="GER SPLITLISTBYLIMIT - format 1" class="alignnone size-full wp-image-1204103" width="466" height="438" /></a><a href="./media/ger-splitlistbylimit-datasources-1.png"><img src="./media/ger-splitlistbylimit-datasources-1.png" alt="GER SPLITLISTBYLIMIT - datasources 1" class="alignnone size-full wp-image-1204093" width="645" height="507" /></a>On muutettu muoto suorittamisen tuloksen. <a href="./media/ger-splitlistbylimit-output-1.png"><img src="./media/ger-splitlistbylimit-output-1.png" alt="GER SPLITLISTBYLIMIT - output 1" class="alignnone size-full wp-image-1204113" width="676" height="611" /></a><strong>Huomautus:</strong> rajaa ei käytetä alkuperä luettelon viimeisen kohteen kuin sen raja lähde (paino) (11) arvo ylittää määritetyn rajan (9). Käytä joko toimintoa <strong>WHERE</strong> tai vastaavan muodon elementin <strong>Enabled</strong> (käytössä) lauseketta ohittaaksesi (skip) alaluettelot raporttia muodostettaessa (tarvittaessa).</td>
</tr>
<tr class="odd">
<td>FILTER (luettelo, ehto)</td>
<td>Palauttaa tietyn luettelon suodatettuna annettua ehtoa varten muuttamalla kyselyä. Toisin kuin <strong>WHERE</strong>-toimintoa, annettua ehtoa käytetään tietokannan tasolla kaikkiin Table-tietuetyyppin ER-tietolähteisiin.</td>
<td>SUODATIN (toimittajat, Vendors.VendGroup = &quot;40&quot;) palauttaa vain ne toimittajat "40"-ryhmään kuuluvat toimittajien luettelon, kun <strong>toimittajan</strong> viittaavat ER tietolähteen nimi on määritetty <strong>VendTable</strong> taulukko</td>
</tr>
</tbody>
</table>

### <a name="logical-functions"></a>Loogiset toiminnot

| Toiminto                                                                                | kuvaus                                                                                                                                                                                                                                                                     | Esimerkki                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| TAPAUS (lauseke, vaihtoehto 1, aiheuttaa 1 \[, vaihtoehto 2, aiheuttaa 2\] ... \[, oletus tulos\]) | Laskee määritetyn lausekkeen arvon määritetyille vaihtoehtoisille valinnoille. Palauttaa sen valinnan tuloksen, joka on sama kuin lausekkeen arvo. Muussa tapauksessa palauttaa vaihtoehtoisesti syötetyn oletustuloksen (viimeinen parametri, jonka jälkeen ei tule valintaa). | **CASE( DATETIMEFORMAT( NOW(), "MM"), "10", "WINTER", "11", "WINTER", "12", "WINTER", "")** palauttaa merkkijonon **"WINTER"** kun nykyisen Dynamics 365 for Operations -istunnon päivämäärä on loka-joulukuussa. Muussa tapauksessa se palauttaa tyhjän merkkijonon. |
| IF (ehto, arvo 1, arvo 2)                                                        | Palauttaa määritetyn arvon 1, kun annetut ehdot täyttyvät. Muussa tapauksessa palauttaa arvon 2. Jos 1 ja 2-arvon tietueita tai tietueiden luetteloita, tulos on vain ne kentät, jotka ovat molemmat luettelot.                                                                     | **IF (1=2, "ehto täyttyy", "ehto ei täyty")** palauttaa merkkijonon **"ehto ei täyty"**.                                                                                                                                                      |
| NOT (ehto)                                                                         | Palauttaa määritetyn ehdon käänteisen loogisen arvon.                                                                                                                                                                                                                   | **NOT (TOSI)** palauttaa arvon **EPÄTOSI**.                                                                                                                                                                                                                            |
| JA (ehto 1\[, ehto 2... \])                                                 | Palauttaa arvon **TOSI**, jos *kaikki *määritetyt ehdot ovat tosia. Muussa tapauksessa palauttaa **EPÄTOSI**-arvon.                                                                                                                                                                                            | **AND (1=1, "a"="a")** palauttaa arvon **TOSI**. **AND (1=2, "a"="a")** palauttaa arvon **EPÄTOSI**.                                                                                                                                                                           |
| TAI (ehto 1\[, ehto 2... \])                                                  | Palauttaa arvon **EPÄTOSI**, jos *kaikki *määritetyt ehdot ovat epätosia. Palauttaa arvon **TOSI**, jos *jokin *määritetyistä ehdoista on tosi.                                                                                                                                                                 | **OR (1=2, "a"="a")** palauttaa arvon **TOSI**.                                                                                                                                                                                                                      |

### <a name="mathematical-functions"></a>Matemaattinen toiminto

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Toiminto</th>
<th>Kuvaus</th>
<th>Esimerkki</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ABS (numero)</td>
<td>Palauttaa määritetyn numeron absoluuttisen arvon (numerolla ei ole etumerkkiä).</td>
<td><strong>ABS (-1)</strong> palauttaa arvon <strong>1</strong>.</td>
</tr>
<tr class="even">
<td>POWER (numero, potenssi)</td>
<td>Palauttaa tuloksen, joka on nostettu määritettyyn positiiviseen potenssiin.</td>
<td><strong>POWER (10, 2)</strong> palauttaa arvon <strong>100</strong>.</td>
</tr>
<tr class="odd">
<td>NUMBERVALUE (merkkijono, desimaalierotin, numeron ryhmittelyin erotin)</td>
<td>Muuntaa määritetyn merkkijonon numeroksi. Määritettyä symbolia käytetään kokonaisluvun ja desimaalinumeron murtolukujen erottelussa. Käytössä on myös määritetty tuhaterotin.</td>
<td><strong>NUMBERVALUE (&quot;1 234,56&quot;, &quot;,&quot;, &quot;&quot;)</strong> palauttaa arvon <strong>1234.56</strong>.</td>
</tr>
<tr class="even">
<td>VALUE (merkkijono)</td>
<td>Muuntaa määritetyn merkkijonon numeroksi. Pilkkuja ja pisteitä (.) pidetään desimaalierottimina. Alussa olevaa tavuviivaa (-) pidetään miinusmerkkinä. Annetaan poikkeus, jos määritetystä merkkijonosta löytyy merkkejä, jotka eivät ole numeerisia.</td>
<td><strong>ARVO (&quot;1 234,56&quot;)</strong> ilmoittaa poikkeuksen.</td>
</tr>
<tr class="odd">
<td>ROUND (numero, desimaalit)</td>
<td>Palauttaa määritetyn numeron, joka on pyöristetty määritettyyn määrään desimaaleja seuraavasti:
<ul>
<li>Jos määritettyjen desimaalien määrä on enemmän kuin 0 (nolla), numero pyöristetään määritettyyn määrään desimaaleja.</li>
<li>Jos määritettyjen desimaalien arvo on 0 (nolla), numero pyöristetään lähimpään kokonaislukuun.</li>
<li>Jos määritettyjen desimaalien määrä on vähemmän kuin 0 (nolla), numero pyöristetään desimaalipilkusta vasemmalle.</li>
</ul></td>
<td><strong>ROUND (1200.767, 2)</strong> pyöristää kahteen desimaaliin ja palauttaa arvon <strong>1200.77</strong>. <strong>ROUND (1200.767, -3)</strong> pyöristää lähimpään tuhanteen ja palauttaa arvon <strong>1000</strong>.</td>
</tr>
<tr class="even">
<td>ROUNDDOWN (numero, desimaalit)</td>
<td>Palauttaa määritetyn numeron, joka on pyöristetty alaspäin (kohti nollaa) määritettyyn määrään desimaaleja. <strong>Huomautus:</strong> Tämä toiminto käyttäytyy kuten <strong>ROUND</strong>, mutta se pyöristää määritetyn numeron aina alaspäin.</td>
<td><strong>ROUNDDOWN (1200.767, 2)</strong> pyöristää alaspäin kahteen desimaaliin ja palauttaa arvon <strong>1200.76</strong>. <strong>ROUNDDOWN (1700.767, -3)</strong> pyöristää alaspäin lähimpään tuhanteen ja palauttaa arvon <strong>1000</strong>.</td>
</tr>
<tr class="odd">
<td>ROUNDUP (numero, desimaalit)</td>
<td>Palauttaa määritetyn numeron, joka on pyöristetty ylöspäin (pois nollasta) määritettyyn määrään desimaaleja. <strong>Huomautus:</strong> Tämä toiminto käyttäytyy kuten <strong>ROUND</strong>, mutta se pyöristää määritetyn numeron aina ylöspäin.</td>
<td><strong>ROUNDUP (1200.763, 2)</strong> pyöristää ylöspäin kahteen desimaaliin ja palauttaa arvon <strong>1200.77</strong>. <strong>ROUNDUP (1200.767, -3)</strong> pyöristää ylöspäin lähimpään tuhanteen ja palauttaa arvon <strong>2000</strong>.</td>
</tr>
</tbody>
</table>

### <a name="record-functions"></a>Tallennustoiminnot

| Toiminto             | Kuvaus                                                                                                                                                                                                                                     | Esimerkki                                                                                                                                             |
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| NULLCONTAINER (luettelo) | Palauttaa **tyhjän** tietueen, jonka rakenne on sama kuin määritetyn tietueluettelon tai tietueen. **Huomautus: **Tämä toiminto on vanhentunut. Käytä sen sijaan **EMPTYRECORD**-toimintoa.                                                                                  | **NULLCONTAINER (SPLIT ("abc", 1))** palauttaa uuden tyhjän tietueen, jonka rakenne on sama kuin **SPLIT**-toiminnon palauttamalla luettelolla. |
| EMPTYRECORD (tietue) | Palauttaa **tyhjän** tietueen, jonka rakenne on sama kuin määritetyn tietueluettelon tai tietueen. **Huomautus:** A **null** tietue on tietue, jossa kaikki kentät on tyhjää arvoa (**0**\[0\] numerot, merkkijonot ja niin edelleen tyhjä merkkijono). | **EMPTYRECORD (SPLIT ("abc", 1))** palauttaa uuden tyhjän tietueen, jonka rakenne on sama kuin **SPLIT**-toiminnon palauttamalla luettelolla.   |

### <a name="text-functions"></a>Tekstitoiminnot

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Toiminto</th>
<th>Kuvaus</th>
<th>Esimerkki</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>UPPER (merkkijono)</td>
<td>Palauttaa määritetyn merkkijonon, joka on muutettu isoiksi kirjaimiksi.</td>
<td><strong>YLEMPI (&quot;näyte&quot;)</strong> palauttaa <strong>&quot;NÄYTE&quot;</strong>.</td>
</tr>
<tr class="even">
<td>LOWER (merkkijono)</td>
<td>Palauttaa määritetyn merkkijonon, joka on muutettu pieniksi kirjaimiksi.</td>
<td><strong>ALEMPI (&quot;näyte&quot;)</strong> palauttaa <strong>&quot;näyte&quot;</strong>.</td>
</tr>
<tr class="odd">
<td>LEFT (merkkijono, merkkien määrä)</td>
<td>Palauttaa määritetyn määrän merkkejä merkkijonon alusta.</td>
<td><strong>VASEMMALLA (&quot;näyte&quot;, 3)</strong> palauttaa <strong>&quot;Sam&quot;</strong>.</td>
</tr>
<tr class="even">
<td>RIGHT (merkkijono, merkkien määrä)</td>
<td>Palauttaa määritetyn määrän merkkejä merkkijonon lopusta.</td>
<td><strong>OIKEALLE (&quot;näyte&quot;, 3)</strong> palauttaa <strong>&quot;ple&quot;</strong>.</td>
</tr>
<tr class="odd">
<td>MID (merkkijono, alkukohta, merkkien määrä)</td>
<td>Palauttaa määritetyn määrän merkkejä määritetyn merkkijonon tietystä kohdasta.</td>
<td><strong>MID (&quot;näyte&quot;, 2, 3)</strong> palauttaa <strong>&quot;&&quot;</strong>.</td>
</tr>
<tr class="even">
<td>LEN (merkkijono)</td>
<td>Palauttaa määritetyn merkkijonon merkkien määrän.</td>
<td><strong>LEN (&quot;näyte&quot;)</strong> palauttaa <strong>6</strong>.</td>
</tr>
<tr class="odd">
<td>CHAR (numero)</td>
<td>Palauttaa merkkijonon, johon määritetty unicode-numero viittaa.</td>
<td><strong>CHAR (255)</strong> palauttaa <strong>&quot;ÿ&quot;</strong>. <strong>Huomautus:</strong> Palautettu merkkijono määräytyy koodauksen mukaan, joka on valittu ylemmän tason FILE-muotoisessa elementissä. Tuettujen koodausten luettelo löytyy <a href="https://msdn.microsoft.com/en-us/library/system.text.encoding(v=vs.110).aspx">Koodausluokka</a>-aiheesta.</td>
</tr>
<tr class="even">
<td>CONCATENATE (1 merkkijono [, merkkijono 2, …])</td>
<td>Palauttaa kaikki määritetyt tekstimerkkijonot, jotka on liitetty yhteen merkkijonoon.</td>
<td><strong>YHDISTÄÄ (&quot;abc&quot;, &quot;def&quot;)</strong> palauttaa <strong>&quot;abcdef&quot;</strong>. <strong>Huomautus:</strong> ilmaisulla <strong>&quot;abc&quot;&amp;&quot;def&quot;</strong> palauttaa <strong>&quot;abcdef&quot;</strong>.</td>
</tr>
<tr class="odd">
<td>TRANSLATE (merkkijono, malli, korvaus)</td>
<td>Palauttaa määritetyn merkkijonon, jossa määritetyn mallimerkkijonon kaikkien merkkien esiintymät korvataan määritetyn korvausmerkkijonon vastaavassa kohdassa olevilla merkeillä.</td>
<td><strong>KÄÄNNÄ (&quot;abcdef&quot;, &quot;cd&quot;, &quot;GH&quot;)</strong> kuvio korvaa <strong>&quot;cd&quot;</strong> merkkijonolla <strong>&quot;GH&quot;</strong> ja <strong>&quot;abGHef&quot;</strong>.</td>
</tr>
<tr class="even">
<td>REPLACE (merkkijono, malli, korvaus, säännönmukaisen lausekkeen merkki)</td>
<td>Palauttaa määritetyn merkkijonon, kun määritetty säännöllisen lausekkeen merkki on <strong>tosi</strong>. Merkkijonoa muokataan kohdistamalla säännöllinen lauseke, joka on määritetty tämän toiminnon malliargumentiksi. Tätä lauseketta käytetään etsittäessä korvattavia merkkejä. Määritetyn korvausargumentin merkkejä käytetään löydettyjen merkkien korvaamisessa. Kun määritetyn säännöllisen lausekkeen merkki on <strong>epätosi</strong>, tämä toiminto toimii kuten <strong>TRANSLATE</strong>.</td>
<td>  <strong>KORVATA (&quot;+1 923 456 4971&quot;, &quot;[^ 0-9]&quot;, &quot;&quot;, TOSI)</strong> koskee säännöllinen lauseke, joka poistaa kaikki muiden kuin numeeristen merkkien ja palauttaa <strong>&quot;19234564971&quot;</strong>. <strong>KORVATA (&quot;abcdef&quot;, &quot;cd&quot;, &quot;GH&quot;, false)</strong> kuvio korvaa <strong>&quot;cd&quot;</strong> merkkijonolla <strong>&quot;GH&quot;</strong> ja palauttaa <strong>&quot;abGHef&quot;</strong>.</td>
</tr>
<tr class="odd">
<td>TEXT (syöte)</td>
<td>Palauttaa määritetyn syötteen, joka muunnetaan tekstimerkkijonoksi. Se puolestaan muotoillaan nykyisen Dynamics 365 for Operations -esiintymän palvelimen aluekohtaisten asetusten perusteella. <strong>Reaali</strong>-tyyppisten arvojen merkkijonon muunnos on rajoitettu kahteen desimaaliin.</td>
<td>Jos on määritetty Operations esiintymän palvelimen kielialueen Dynamics-365 <strong>fi</strong>, <strong>teksti (nyt ())</strong> palauttaa nykyisen Dynamics 365 työvaiheiden istunnon päivämäärä, 12/17/2015 teksti merkkijonossa <strong>&quot;12/17/2015 07:59:23 AM&quot;</strong>. <strong>TEKSTI (1/3)</strong> palauttaa <strong>&quot;järjestelmä luo 0,33&quot;</strong>.</td>
</tr>
<tr class="even">
<td>FORMAT (merkkijono 1, merkkijono 2[, merkkijono 3, ...])</td>
<td>Palauttaa määritetyn merkkijonon, jota on muotoiltu korvaamalla kaikki <strong>%N</strong>-esiintymät <em>n.</em> argumentilla. Argumentit ovat merkkijonoja. Jos argumentti ei ole parametria, parametri palautetaan <strong>&quot;%N&quot;</strong> -merkkijonossa. <strong>Reaali</strong>-tyyppisten arvojen merkkijonon muunnos on rajoitettu kahteen desimaaliin.</td>
<td>Tässä esimerkissä <strong>PaymentModel</strong>-tietolähde palauttaa asiakastietueluettelon <strong>asiakas</strong>-komponentin kautta ja käsittelyn päivämäärän arvon <strong>ProcessingDate</strong>-kentän kautta. <a href="./media/picture-format-datasource.jpg"><img src="./media/picture-format-datasource.jpg" alt="PaymentModel data source" class="alignnone wp-image-290751 size-full" width="293" height="143" /></a>ER-muodossa, jonka tarkoituksena on luoda sähköisen tiedoston valittujen asiakkaiden <strong>PaymentModel</strong> on valittu tietolähde ja ohjaa prosessin kulkua. Loppukäyttäjille annetaan poikkeus, kun valittu asiakas pysäytetään raportin käsittelypäivämääränä. Tälle käsittelyn ohjausobjektin tyypille muotoiltua kaavaa käytetään seuraavissa resursseissa:
<ul>
<li>Dynamics 365 for Operations otsikko SYS70894, jolla on seuraava teksti:
<ul>
<li><strong>EN-US kielellä:</strong>&quot;ei tulosteta&quot;</li>
<li><strong>DE kielen:</strong>&quot;Nichts zu drucken&quot;</li>
</ul></li>
<li>Dynamics 365 for Operations otsikko SYS18389, jolla on seuraava teksti:
<ul>
<li><strong>EN-US kielellä:</strong>&quot;asiakas %1 on keskeytetty: %2.&quot;</li>
<li><strong>DE kielen:</strong>&quot;Debitor '%1' wird für %2 gesperrt.&quot;</li>
</ul></li>
</ul>
Tässä on kaava, joka on suunniteltu: FORMAT (KETJUTA-FUNKTION (@&quot;SYS70894&quot;,&quot;. &quot;@&quot;SYS18389&quot;), model.Customer.Name, DATETIMEFORMAT (malli. ProcessingDate, &quot;d&quot;)) Jos raportti käsitellään <strong>Litware vähittäiskaupan asiakkaan</strong>, 17. joulukuuta 2015- <strong>EN-US</strong> kulttuuri ja <strong>EN-US</strong> kieltä, tämä kaava palauttaa seuraavan tekstin, joka voidaan esittää seuraavasti: Poikkeus käyttäjän: &quot;ei tulosteta. 12/17/2015 vähittäiskaupan asiakkaan Litware pysähtyy.&quot; Jos samaa raporttia käsitellään<strong> Litware vähittäiskaupan asiakkaan</strong>, 17. joulukuuta 2015- <strong>DE</strong> kulttuuri ja <strong>DE</strong> kieltä, tämä kaava palauttaa seuraavan tekstin, joka käyttää eri päivämäärämuoto: &quot;Nichts zu drucken. Debitor "Litware Retail" wird für 17.12.2015 gesperrt.&quot; <strong>Huomautus: </strong>Otsikoiden ER-kaavoissa käytetään seuraavaa syntaksia:
<ul>
<li><strong>Tarrojen Dynamics 365-toimintoja resurssien:</strong> <strong>@&quot;X&quot;</strong>, jossa X on Etikettitunnus sovellusobjektipuun (AOT)</li>
<li><strong>Tarrat, jotka sijaitsevat ER kokoonpanoissa:</strong> <strong>@&quot;ER_LABEL:X&quot;</strong>, jossa X on ER-kokoonpanossa Etikettitunnus</li>
</ul></td>
</tr>
<tr class="odd">
<td>NUMBERFORMAT (numero, muoto)</td>
<td>Palauttaa määritetyssä muodossa olevan määritetyn numeron merkkijonon esityksen. (Lisätietoja tuetuista muodoista on <a href="https://msdn.microsoft.com/en-us/library/dwhawy9k(v=vs.110).aspx">Vakio</a> ja <a href="https://msdn.microsoft.com/en-us/library/0c899ak8(v=vs.110).aspx">mukautetun</a>.) Maa-asetuksen, jota käytetään lukujen muotoileminen määrittää kontekstin, jossa tämä toiminto suoritetaan.</td>
<td>EN-US-kulttuurin <strong>NUMBERFORMAT (0,45, &quot;p&quot;)</strong> palauttaa <strong>&quot;45,00 %&quot;</strong>. <strong>NUMBERFORMAT (10.45, &quot;#&quot;)</strong> palauttaa <strong>&quot;10&quot;</strong>.</td>
</tr>
<tr class="even">
<td>NUMERALSTOTEXT (määrä, kieli, valuutta, tulosta valuutan nimi -merkki, desimaalit)</td>
<td>Palauttaa numeron kirjoitettuna (muunnettuna) merkkijonoiksi määritetyllä kielellä. Kielikoodi on valinnainen: kun se on määritetty tyhjänä merkkijonona, sen sijaan käytetään suorituskontekstin kielikoodia (määritetty luotavalle kansiolle tai tiedostolle). Valuuttakoodi on valinnainen. Kun se on määritetty tyhjänä merkkijonona, käytetään yrityksen valuuttaa. Huomaa että <strong>Tulosta valuutan nimi</strong> parametri ja <strong>Desimaalit</strong>-parametrit analysoidaan vain seuraaville kielikoodeille: <strong>CS</strong>, <strong>ET</strong>, <strong>HU</strong>, <strong>LT</strong>, <strong>LV</strong>, <strong>PL</strong>, <strong>RU</strong>. Huomautus <strong>Tulosta valuutan nimi</strong> -parametri analysoidaan vain Dynamics 365 for Operations -yrityksissä, joiden maakonteksti tukee valuutan nimen taivutusta.</td>
<td>NUMERALSTOTEXT (1234.56, &quot;fi&quot;, &quot;&quot;, arvo on EPÄTOSI, 2) palauttaa-1 tuhat kahteen sataan kolmeenkymmeneen 4 ja 56-NUMERALSTOTEXT (120, &quot;PL&quot;, &quot;&quot;, arvo on EPÄTOSI, 0) palauttaa "Lopeta dwadzieścia" NUMERALSTOTEXT (120.21, &quot;RU&quot;, &quot;EUROA&quot;, TOSI, 2) palauttaa "Сто двадцать евро 21 евроцент"</td>
</tr>
<tr class="odd">
<td>PADLEFT (merkkijono, pituus, täyttömerkit)</td>
<td>Palauttaa määritetyn pituisen merkkijonon, jossa nykyisen merkkijonon alkua on täydennetty määritetyillä merkeillä.</td>
<td>PADLEFT (“1234”, 10, “ “) palauttaa tekstimerkkijonon “      1234”</td>
</tr>
</tbody>
</table>

### <a name="data-collection-functions"></a>Tietojen keruutoiminnot

Toiminto

kuvaus

Esimerkki

FORMATELEMENTNAME ()

Palauttaa nykyisen muodon elementin nimen. Palauttaa tyhjän merkkijonon, jos nykyisten tiedostojen **Kerää tulostiedot** -lippu on poistettu käytöstä.

Tehtäväopas **ER Käytä tulostusmuotoa laskennassa ja summauksessa** (osa **IT-palvelujen ja -ratkaisujen komponenttien hankkiminen ja kehittäminen** -liiketoimintaprosessia) sisältää lisätietoja näiden toimintojen käytöstä.

ERILAINEN (avain Summaava ehdot Alue1 merkkijono, ehdot arvo1 merkkijono merkkijono \[, ehdot alue2 merkkijono, ehdot arvo2 merkkijono,... \])

Palauttaa XML-solmujen arvojen summan (avaimeksi on määritetty nimi), joka on kerätty tämän muodon suorittamisen aikana ja joka täyttää annetut ehdot (alue-arvoparit). Palauttaa nolla-arvon, jos nykyisten tiedostojen **Kerää tulostiedot** -lippu on poistettu käytöstä.

SUMIF (summauksen avainmerkkijono, ehtoalueen merkkijono, ehdon arvon merkkijono)

Palauttaa XML-solmujen arvojen summan (avaimeksi on määritetty nimi), joka on kerätty tämän muodon suorittamisen aikana ja joka täyttää annetun ehdon (alue ja arvo). Palauttaa nolla-arvon, jos nykyisten tiedostojen **Kerää tulostiedot** -lippu on poistettu käytöstä.

COUNTIFS (ehdot Alue1 merkkijono, ehdot arvo1 merkkijono \[, ehdot alue2 merkkijono, ehdot arvo2 merkkijono,... \])

Palauttaa XML-solmujen arvojen lukumäärän, joka on kerätty tämän muodon suorittamisen aikana ja joka täyttää annetut ehdot (alue-arvoparit). Palauttaa nolla-arvon, jos nykyisten tiedostojen **Kerää tulostiedot** -lippu on poistettu käytöstä.

COUNTIF (ehtoalueen merkkijono,ehdon arvon merkkijono)

Palauttaa XML-solmujen arvojen lukumäärän, joka on kerätty tämän muodon suorittamisen aikana ja joka täyttää annetun ehdon (alue ja arvo). Palauttaa nolla-arvon, jos nykyisten tiedostojen **Kerää tulostiedot** -lippu on poistettu käytöstä.

COLLECTEDLIST (kriteerit Alue1 merkkijono, ehdot arvo1 merkkijono \[, ehdot alue2 merkkijono, ehdot arvo2 merkkijono,... \])

Palauttaa XML-solmujen arvoluettelonn, joka on kerätty tämän muodon suorittamisen aikana ja joka täyttää annetut ehdot (alue ja arvo). Palauttaa tyhjän luettelon, jos nykyisten tiedostojen **Kerää tulostiedot **-lippu on poistettu käytöstä.

### <a name="other-business-domainspecific-functions"></a>Muut (liiketoiminnan toimialuekohtaiset) toiminnot

| Toiminto                                                                         | kuvaus                                                                                                                                                                                                                                                        | Esimerkki                                                                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CONVERTCURRENCY (summa, lähdevaluutta, kohdevaluutta, päivämäärä, yritys)        | Muuntaa määritetyn rahasumman lähdevaluutasta kohdevaluuttaan käyttämällä määritetyn Dynamics 365 for Operations -yrityksen asetuksia tiettynä päivänä.                                                                            | **CONVERTCURRENCY (1, "EUR", "USD", TODAY(), "DEMF")** palauttaa yhden euron suuruisen määrän Yhdysvaltojen dollareita nykyisen istunnon päivämääränä DEMF-yrityksen asetusten perusteella.                                                                                                                                  |
| ROUNDAMOUNT (määrä, desimaalit, pyöristyssääntö)                                       | Pyöristää määritetyn summan tietyn pyöristyssäännön ja desimaalien määrän perusteella. **Huomautus:** Pyöristyssääntö on määritettävä Dynamics 365 for Operations **RoundOffType**-numeroinnin arvoksi.                          | Jos **malli. RoundOff** -parametrin arvoksi *** Downward *** **ROUNDAMOUNT (1000.787, 2-malli. RoundOff)** palauttaa arvon **1000.78**. Jos **model.RoundOff**-parametrin arvoksi on määritetty **Normaali** tai **Ylöspäin**, **ROUNDAMOUNT (1000.787, 2, model.RoundOff)** palauttaa arvon **1000.79**. |
| CURCredRef (numerot)                                                              | Palauttaa laskuttajan viitteen määritetyn laskunumeron lukujen perusteella.                                                                                                                                                                                  | **CURCredRef ("VEND-200002")** palauttaa arvon **"2200002"**.                                                                                                                                                                                                                                                         |
| MOD\_97 (merkkiä)                                                                 | Palauttaa laskuttajan viitteen MOD97-lausekkeena määritetyn laskunumeron lukujen perusteella.                                                                                                                                                            | **MOD\_97 ("VEND-200002")** palauttaa **"20000285"**.                                                                                                                                                                                                                                                           |
| ISOCredRef (numerot)                                                              | Palauttaa laskuttajan ISO-viitteen määritetyn laskunumeron lukujen ja aakkosten merkkien perusteella. **Huomautus: **Voit poistaa ne aakkosten merkit, jotka eivät ole ISO-yhteensopivia, jos syöttöparametri on käännetty ennen kuin se välitetään tälle toiminnolle. | **ISOCredRef ("VEND-200002")** palauttaa arvon **"RF23VEND-200002"**.                                                                                                                                                                                                                                                 |
| CN\_GBT\_AdditionalDimensionID (merkkijono, numero)                                  | Hae taloushallinnan lisädimension tunnus. Dimensiot esitetään tässä merkkijonossa pilkuilla erotettuina tunnuksina. Lukumäärä määrittää pyydetyn dimension järjestyskoodin tässä merkkijonossa.                                                                            | CN\_GBT\_AdditionalDimensionID ("AA, BB, CC, pp, EE, LL, GG, HH"-3) palauttaa "Kopio"                                                                                                                                                                                                                                      |
| GetCurrentCompany ()                                                             | Palauttaa kirjautuneen yrityksen koodin.                                                                                                                                                                                                                    |                                                                                                                                                                                                                                                                                                               |
| CH\_pankin\_MOD\_10 (merkkiä)                                                       | Palauttaa laskuttajan viitteen MOD10-lausekkeena määritetyn laskunumeron lukujen perusteella.                                                                                                                                                                      | CH\_pankin\_MOD\_10 ("VEND-200002") palauttaa arvon 3                                                                                                                                                                                                                                                                   |
| KO\_summa (kiinteä hyödykkeen koodin, mallin koodi, alkamispäivämäärä, päättymispäivämäärä)               | Palauttaa kauden käyttöomaisuussummien valmistellun tietosäilön.                                                                                                                                                                                         | KO\_summa ("COMP-000001", "Nykyinen", päivämäärä1, päivämäärä2) palauttaa valmistetut tietosäilön käyttöomaisuuserän "COMP 000001" ja arvomalli "Nykyinen" ajaksi päivämäärä1 päivämäärä2.                                                                                                                        |
| KO\_(kiinteä hyödykkeen koodin arvon mallin koodi Raportointivuosi, ilmoituspäivämäärä) saldo | Palauttaa käyttöomaisuuden saldojen valmistellun tietosäilön. Raportointivuosi pitää määrittää Dynamics 365 for Operations luettelointiarvona **AssetYear**.                                                                                           | KO\_summa ("COMP-000001", "Nykyinen", AxEnumAssetYear.ThisYear, SESSIONTODAY ()) palauttaa käyttöomaisuuden saldot valmistellut tiedot säilön "COMP-000001" ja arvomalli "Nykyinen" Nykyinen 365-operaatioille istunnon päivämäärä.                                                                |

### <a name="functions-list-extension"></a>Toimintojen luettelon laajennus

ER:n avulla on mahdollista laajentaa luetteloa toiminnoista, joita käytetään ER-lausekkeissa. Tähän tarvitaan jonkin verran suunnittelutyötä. Lisätietoja on kohdassa [Sähköisen raportoinnin toimintojen luettelon laajentaminen](general-electronic-reporting-formulas-list-extension.md).

<a name="see-also"></a>Lisätietoja
--------

[Sähköisen raportoinnin yleiskatsaus](general-electronic-reporting.md)

[Sähköisen raportoinnin (ER) toimintojen luettelon laajentaminen](general-electronic-reporting-formulas-list-extension.md)


