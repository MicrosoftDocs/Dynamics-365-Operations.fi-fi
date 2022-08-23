---
title: Sähköisen raportoinnin kaavakieli
description: Tässä artikkelissa on tietoja siitä, miten käyttää kaavakieltä sähköisessä raportoinnissa (ER).
author: kfend
ms.date: 05/04/2020
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: 7df29c74b2a430ed9d974cad709b975e4fd9cd35
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9283280"
---
# <a name="electronic-reporting-formula-language"></a>Sähköisen raportoinnin kaavakieli

[!include [banner](../includes/banner.md)]

Sähköinen raportointi (ER) tarjoaa tehokkaan tietojenmuunnoskokemuksen. Kieli, jota käytetään ilmaisemaan vaaditut tietojen manipuloinnit [ER -kaavojen suunnittelutoiminnossa](general-electronic-reporting-formula-designer.md) muistuttaa kaavan kieltä Microsoft Excelissä.

## <a name="basic-syntax"></a>Perussyntaksi

ER-lausekkeet voivat sisältää joitakin seuraavia elementtejä tai kaikki seuraavat elementit:

- [Vakiot](#Constants)
- [Operaattorit](#Operators)
- [Viitteet](#References)
- [Polut](#Paths)
- [Toiminnot](#Functions)

## <a name="constants"></a><a name="Constants"></a>Vakiot

Voit käyttää lausekkeiden suunnittelussa tekstivakioita ja numeerisia vakioita (arvoja, joita ei lasketa). Esimerkiksi lauseke `VALUE ("100") + 20` käyttää numeerista vakiota **20** ja merkkijonovakiota **"100"** ja se palauttaa numeerisen arvon **120**.

ER-kaavojen suunnittelutoimintoa tukee ohjausjaksoja. Niinpä voitkin määrittää lausekkeen merkkijonosta, jota on käsiteltävä eri tavalla. Lauseke `"Leo Tolstoy ""War and Peace"" Volume 1"` palauttaa esimerkiksi tekstimerkkijonon **Leo Tolstoy "War and Peace" Volume 1**.

## <a name="operators"></a><a name="Operators"></a>Operaattorit

Seuraavassa taulukossa on aritmeettisia operaattoreita, joita voi käyttää matemaattisten perusoperaattoreiden, kuten lisäyksen, vähennyksen sekä kerto- ja jakolaskun suorittamiseen.

| Käyttäjä | Merkitys               | Esimerkki     |
|----------|-----------------------|-------------|
| +        | Lisäys              | `1+2`       |
| -        | Vähennys, negaatio | `5-2`, `-1` |
| \*       | Kertolasku        | `7\*8`      |
| /        | Jaosto              | `9/3`       |

Seuraavassa taulukossa on tuetut vertailuoperaattorit. Näillä operaattoreilla voi verrata kahta arvoa.

| Käyttäjä | Merkitys                  | Esimerkki      |
|----------|--------------------------|--------------|
| =        | Yhtä suuri                    | `X=Y`        |
| &gt;     | Suurempi kuin             | `X>Y`        |
| &lt;     | Pienempi kuin                | `X<Y`        |
| &gt;=    | Suurempi tai yhtä suuri kuin | `X>=Y`       |
| &lt;=    | Pienempi tai yhtä suuri kuin    | `X<=Y`       |
| &lt;&gt; | Ei sama kuin             | `X<>Y`       |

Lisäksi &-merkkiä voi käyttää tekstin ketjutusoperaattorina. Tällä tavoin yksittäiseen tekstikappaleeseen voi liittää tai yhdistää yhden tekstimerkkijonon tai useita merkkijonoja.

| Käyttäjä | Merkitys     | Esimerkki                                               |
|----------|-------------|-------------------------------------------------------|
| &        | Liitä | `"Nothing to print:" & " " & "no records found"`      |

### <a name="operator-precedence"></a>Operaattoreiden käsittelyjärjestys

Järjestys, jossa yhdistelmälausekkeen osat lasketaan, on tärkeä. Esimerkiksi lausekkeen `1 + 4 / 2` tulos on erilainen sen mukaan, suoritetaanko ensi yhteenlasku- vai jakotoiminto. Sulkeiden avulla voit määrittää, miten lauseke lasketaan. Jos haluat esimerkiksi osoittaa, että yhteenlaskutoiminto suoritetaan ensin, voit muuttaa edeltävän lausekkeen muotoon `(1 + 4) / 2`. Jos et selkeästi ilmaise lausekkeen toimintojen suoritusjärjestystä, järjestys perustuu oletusarvoiseen tukioperaattoreiden määrittämään käsittelyjärjestykseen. Seuraavassa taulukossa kuhunkin operaattoriin liitetty käsittelyjärjestys. Operaattorit, joilla on korkeampi käsittelyjärjestys (esimerkiksi 7), suoritetaan ennen operaattoreita, joilla on alempi käsittelyjärjestys (esimerkiksi 1).

| Järjestys | Operaattorit      | Syntaksi                                                                  |
|------------|----------------|-------------------------------------------------------------------------|
| 7          | Ryhmittely       | ( … )                                                                   |
| 6          | Jäsenen käyttöoikeus  | … . …                                                                   |
| 5          | Funktiokutsu  | … ( … )                                                                 |
| 4          | Kertova | … \* …<br>… / …                                                         |
| 3          | Lisä       | … + …<br>… - …                                                          |
| 2          | Vertailu     | … &lt; …<br>… &lt;= …<br>… =&gt; …<br>… &gt; …<br>… = …<br>… &lt;&gt; … |
| 1          | Erottelu     | … , …                                                                   |

Jos lausekkeessa on useita peräkkäisiä operaattoreita, joilla on sama tärkeysjärjestys, kyseiset operaattorit suoritetaan vasemmalta oikealle. Esimerkiksi lauseke `1 + 6 / 2 \* 3 > 5` palauttaa arvon **tosi**. Käyttämällä sulkeita lausekkeiden haluttu laskentajärjestys voidaan ilmaista selkeästi, mikä myös helpottaa lausekkeiden lukemista ja ylläpitämistä.

## <a name="references"></a><a name="References"></a>Viitteet

Kaikkia nykyisen ER-komponentin tietolähteitä, jotka ovat käytettävissä lausekkeen suunnittelun yhteydessä, voidaan käyttää nimettyinä viitteinä. Nykyinen ER-osa voi olla mallin yhdistämismääritys tai muoto. Esimerkiksi nykyinen ER-mallin määritys sisältää **ReportingDate**-tietolähteen, joka palauttaa [*Päivämäärä/aika*](er-formula-supported-data-types-primitive.md#datetime)-tietotyypin arvon. Jotta kyseinen arvo saadaan muotoiltua oikein luotavassa asiakirjassa, siihen voidaan viitata lausekkeessa seuraavasti: `DATETIMEFORMAT (ReportingDate, "dd-MM-yyyy")`.

Kaikkien niiden viittaavan tietolähteen nimen merkkien, jotka eivät ole kirjaimia, edessä on oltava edessään puolilainausmerkki ('). Kaikilla viittaavan tietolähteen nimillä, jotka sisältävät ainakin yhden merkin, joka ei ole kirjain, on oltava puolilainausmerkkien sisällä. Näitä muita kuin kirjaimia voivat olla esimerkiksi välimerkit tai muut kirjoitetut merkit. Seuraavassa on muutamia esimerkkejä:

- **Today's date & time** -tietolähteeseen on viitattava ER-lausekkeessa seuraavasti: `'Today''s date & time'`.
- **Asiakkaat**-tietolähteen **name()**-menetelmän on viitattava ER-lausekkeeseen seuraavasti: `Customers.'name()'`.

Jos sovelluksen tietolähteiden menetelmillä on parametreja, kyseiset menetelmät kutsutaan seuraavalla syntaksilla:

- Jos **Järjestelmä**-tietolähteen, jossa [*Merkkijono*](er-formula-supported-data-types-primitive.md#string)-tietotyypin parametri on **EN-US**, **isLanguageRTL**-menetelmään on viitattava ER-lausekkeessa seuraavasti: `System.isLanguageRTL("EN-US")`.
- Lainausmerkit eivät ole pakollisia, kun menetelmän nimessä on vain aakkosnumeerisia merkkejä. Niitä on kuitenkin käytettävä taulun menetelmässä, jos hakasulkeet sisältyvät nimeen.

Kun **Järjestelmä**-tietolähde lisätään ER-yhdistämismääritykseen, jossa on viittauksena **Yleinen**-sovellusluokka, lauseke `System.isLanguageRTL("EN-US ")` palauttaa *totuusarvon* **EPÄTOSI**. Muokattu lauseke `System.isLanguageRTL("AR")` palauttaa *totuusarvon* **tosi**.

Voit rajoittaa tapaa, jolla arvot siirretään tämän tyyppisen menetelmän parametreihin:

- Vain vakioita voi siirtää tämän tyyppisiin menetelmiin. Vakioiden arvot määritetään suunnitteluvaiheessa.
- Tämän tyypin parametrit tukevat [alkeellisia](er-formula-supported-data-types-primitive.md) (perus)tietotyyppejä. Alkukantaisia tietotyyppejä ovat esimerkiksi *kokonaisluku*, *reaaliluku*, *totuusarvo* ja *merkkijono*.

## <a name="paths"></a><a name="Paths"></a>Polut

Kun lauseke viittaa rakenteelliseen tietolähteeseen, polun määritettä voidaan käyttää valittaessa tietolähteen tietty primitiivinen elementti. Piste (.) -merkkiä käytetään erottamaan rakenteisen tietolähteen yksittäiset elementit. Esimerkiksi nykyinen ER-mallin määritys sisältää **InvoiceTransactions**-tietolähteen, joka palauttaa tietueluettelon. **InvoiceTransactions**-tietuerakenne sisältää **AmountDebit**- ja **AmountCredit**-kentät, joista kumpikin palautta numeerisia arvoja. Tämän vuoksi voit suunnitella seuraavan lausekkeen laskutettavan summan laskemista varten: `InvoiceTransactions.AmountDebit - InvoiceTransactions.AmountCredit`. `InvoiceTransactions.AmountDebit`-rakenne tässä lausekkeessa on polku, jota käytetään **AmountDebit**-kentän **InvoiceTransactions**-tietolähteen *tietueluettelo*-tyyppiin pääsemiseksi.

### <a name="relative-path"></a>Suhteellinen polku

Jos rakenteisen tietolähteen polku alkaa at-merkillä (@), se on suhteellinen polku. At-merkki näytetään käytettävän hierarkkisen puurakenteen absoluuttisen polun jäljellä olevan osan sijasta. Seuraavassa kuvassa on esimerkki. Tässä absoluuttinen polku `Ledger.'accountingCurrency()'` ilmaisee, että kirjanpitovaluutan arvo **kirjanpidon** tietolähteestä syötetään **AccountingCurrency**-kenttään tietomallissa.

![Esimerkki absoluuttisesta polusta ER-mallin yhdistämismääritysten suunnittelusivulla.](./media/ER-FormulaLanguage-AbsolutePath.png)

Seuraavassa kuvassa oleva esimerkki osoittaa, miten suhteellinen polku on käytössä. Suhteellinen polku `@.AccountNum` ilmaisee, että **AccountNum**-kentän **Intrastat**-tietolähteen (joka näkyy tietomallin hierarkkisen puun **AccountNum**-kentän yläpuolella) käytetään syöttämään asiakkaan tai toimittajan tilinumero tietomallin **AccountNum**-kenttään.

![Esimerkki relatiivisesta polusta ER-mallin yhdistämismääritysten suunnittelusivulla.](./media/ER-FormulaLanguage-RelativePath1.png)

Jäljellä oleva osa absoluuttisesta polusta näkyy myös [ER kaavaeditorissa](general-electronic-reporting-formula-designer.md).

![ER-kaavan suunnittelijasivun absoluuttisen polun jäljellä oleva osa.](./media/ER-FormulaLanguage-RelativePath2.png)

Lue lisätietoja kohdasta [Suhteellisen polun käyttäminen ER-mallien ja-muotojen tietojen sidonnoissa](relative-path-data-bindings-er-models-format.md).

## <a name="functions"></a><a name="Functions"></a>Funktiot

ER:n sisäänrakennettuja funktioita voidaan käyttää ER-lausekkeissa. Kaikkia lausekekontekstin (kuten nykyinen ER-mallin määritys tai ER-muoto) tietolähteitä voidaan käyttää kutsufunktioiden parametreina kutsufunktioargumenttien luettelon mukaisesti. Myös vakioita voidaan käyttää kutsufunktioiden parametreina. Esimerkiksi nykyinen ER-mallin määritys sisältää **InvoiceTransactions**-tietolähteen, joka palauttaa tietueluettelon. **InvoiceTransactions**-tietuerakenne sisältää **AmountDebit**- ja **AmountCredit**-kentät, joista kumpikin palautta numeerisia arvoja. Voit siis laskea laskutetun määrän suunnittelemalla seuraavan lausekkeen, jossa käytetään sisäänrakennettua ER-pyöristystoimintoa: `ROUND (InvoiceTransactions.AmountDebit - InvoiceTransactions.AmountCredit, 2)`.

Kun suunnittelet ER-mallien yhdistämismäärityksiä ja ER-raportteja, voit käyttää ER-funktioita seuraavista luokista:

- [Päivämäärä- ja aikatoiminnot](er-functions-category-datetime.md)
- [Luettelotoiminnot](er-functions-category-list.md)
- [Loogiset toiminnot](er-functions-category-logical.md)
- [Matemaattinen toiminto](er-functions-category-mathematical.md)
- [Tallennustoiminnot](er-functions-category-record.md)
- [Tekstitoiminnot](er-functions-category-text.md)
- [Tietojen keruutoiminnot](er-functions-category-data-collection.md)
- [Muut (liiketoiminnan toimialuekohtaiset) toiminnot](er-functions-category-other.md)
- [Tyypin muuntamisen toiminnot](er-functions-category-type-conversion.md)

## <a name="functions-list-extension"></a>Toimintojen luettelon laajennus

ER:n avulla on mahdollista laajentaa luetteloa toiminnoista, joita käytetään ER-lausekkeissa. Tähän tarvitaan jonkin verran suunnittelutyötä. Lisätietoja on kohdassa [Sähköisen raportoinnin (ER) toimintojen luettelon laajentaminen](general-electronic-reporting-formulas-list-extension.md).

## <a name="compound-expressions"></a>Yhdistelmälausekkeet

Voit luoda yhdistelmälausekkeita, jotka käyttävät eri luokkien funktioita edellyttäen, että tietotyypit vastaavat toisiaan. Kun käytät funktioita yhdessä, vastaa tulosteen tietotyyppiä yhdestä toiminnosta toisen funktion edellyttämän syötetieto tyypin mukaan. Jos esimerkiksi haluat välttää mahdollisen "luettelo-tyhjä"-virheen kentän sidonnassa ER-muotoelementtiin, yhdistä [Luettelo](er-functions-category-list.md)-luokan funktiot [loogisen](er-functions-category-logical.md)-luokan funktiolla, kuten seuraavassa esimerkissä näytetään. Tässä kaavassa käytetään [IF](er-functions-logical-if.md)-funktiota, kun testataan, onko **IntrastatTotals**-luettelo tyhjä, ennen kuin se palauttaa vaaditun koosteen arvon kyseisestä luettelosta. Jos **IntrastatTotals**-luettelo on tyhjä, kaava palauttaa arvon **0** (nolla).

```vb
IF(ISEMPTY(IntrastatTotals), 0.0, IntrastatTotals.aggregated.'$AmountMSTRounded') 
```

## <a name="multiple-solutions"></a>Useita ratkaisuja

Usein voit saada samat tietojen muunnoksen tulokset monella tavalla käyttämällä eri luokkien tai eri toimintojen funktioita samasta luokasta. Esimerkiksi edellinen lauseke voidaan määrittää myös käyttämällä [MÄÄRÄ](er-functions-list-count.md)-funktiota [luettelo](er-functions-category-list.md)-luokasta.

```vb
IF(COUNT (IntrastatTotals)=0, 0.0, IntrastatTotals.aggregated.'$AmountMSTRounded') 
```

## <a name="additional-resources"></a>Lisäresurssit

[Sähköisen raportoinnin yleiskatsaus](general-electronic-reporting.md)

[Sähköisen raportoinnin kaavojen suunnittelutoiminto](general-electronic-reporting-formula-designer.md)

[Sähköisen raportoinnin toimintoluettelon laajentaminen](general-electronic-reporting-formulas-list-extension.md)

[Tuetut primitiiviset tietotyypit](er-formula-supported-data-types-primitive.md)

[Tuetut yhdistelmätietotyypit](er-formula-supported-data-types-composite.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
