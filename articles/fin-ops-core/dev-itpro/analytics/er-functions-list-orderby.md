---
title: ORDERBY ER-funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) ORDERBY-funktiota käytetään.
author: NickSelin
ms.date: 12/12/2019
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 963d55bcf98a9109c8b6ceb57edf5b55f15a2b0f
ms.sourcegitcommit: 89655f832e722cefbf796a95db10c25784cc2e8e
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/31/2022
ms.locfileid: "8075171"
---
# <a name="orderby-er-function"></a>ORDERBY ER-funktio

[!include [banner](../includes/banner.md)]

`ORDERBY`-funktio palauttaa määritetyn luettelon *Tietueluettelon* arvoksi sen jälkeen, kun se on lajiteltu määritettyjen argumenttien mukaan. Nämä argumentit voivaan määrittää lausekkeina.

## <a name="syntax-1"></a><a name="syntax-1"></a>Syntaksi 1

```vb
ORDERBY (list, expression 1[, expression 2, …, expression N])
```

## <a name="syntax-2"></a><a name="syntax-2"></a>Syntaksi 2

```vb
ORDERBY (location, list, expression 1[, expression 2, …, expression N])
```

> [!NOTE]
> Tätä syntaksia tuetaan Microsoft Dynamics 365 Finance -versiossa 10.0.25 ja sitä myöhemmissä versioissa.

## <a name="arguments"></a>Argumentit

`location`: *[Merkkijono](er-formula-supported-data-types-primitive.md#string)*

Paikka, jossa lajittelu suoritetaan. Seuraavat asetukset ovat kelvollisia:

- "Query"
- "InMemory"

`list`: *[Tietueluettelo](er-formula-supported-data-types-composite.md#record-list)*

*Tietueluettelo*-tietotyypin tietolähteen kelvollinen polku.

`expression 1`: *Kenttä*

Tietolähteen kentän kelvollinen polku, johon kutsutun funktion `list`-argumentti viittaa. Viitatun kentän on oltava primitiivisen tietotyypin kenttä. Tämä argumentti on pakollinen.

`expression N`: *Kenttä*

Tietolähteen kentän kelvollinen polku, johon kutsutun funktion `list`-argumentti viittaa. Viitatun kentän on oltava primitiivisen tietotyypin kenttä. Nämä lisäargumentit ovat valinnaisia.

## <a name="return-values"></a>Palautusarvot

*Tietueluettelo*

Tuloksena oleva tietueluettelo.

## <a name="usage-notes"></a>Käyttöhuomautukset

### <a name="syntax-1"></a>Syntaksi 1

Tietojen lajittelu tapahtuu aina sovelluspalvelimen muistissa. Lisätietoja on kohdassa [esimerkki 1](#example-1).

### <a name="syntax-2"></a>Syntaksi 2

### <a name="sorting-in-memory"></a>Lajitteleminen muistissa

Kun `location`-argumentin arvo on **InMemory**, tietojen lajittelu tapahtuu sovelluspalvelimen muistissa. Lisätietoja on kohdassa [esimerkki 2](#example-2).

### <a name="sorting-in-database"></a>Lajitteleminen tietokannassa

Kun `location`-argumentin arvoksi määritetään **Query**, tietojen lajittelu tapahtuu tietokantatasolla. Tässä tapauksessa `list`-argumentin on osoitettava johonkin seuraavista [sähköisen raportoinnin (ER)](general-electronic-reporting.md) tietolähteistä, jotka määrittävät sovelluslähteen, jota varten voidaan muodostaa suora tietokantakysely:

- *Taulukon tietueet* -tyypin tietolähde
- *Taulukon tietueet* -tyypin tietolähteen suhde
- *Laskentakenttä*-tyypin tietolähde

`expression 1`- ja `expression N`-argumenttien on osoitettava ER-tietolähteen kenttiin, jotka määrittävät sen sovelluslähteen sovellettavat kentät, jota varten voidaan muodostaa suora tietokantakysely.

Jos suoraa tietokantakyselyä ei voi määrittää, ER-mallin yhdistämismäärityksen suunnittelijassa ilmenee [oikeellisuustarkistusvirhe](er-components-inspections.md#i18). Näyttöön tulee sanoma, jonka mukaan toiminnon sisältävä ER `ORDERBY` -funktio ei voi toimia suorituksen aikana.

Suorituskyvyn parantamiseksi on suositeltavaa käyttää **Query**-asetusta, kun lajittelu on konfiguroitu sovellustietolähteille, jotka saattavat sisältää suuren määrän tietueita (esimerkiksi tapahtumiin liittyvät sovellustaulut).

> [!NOTE]
> `ORDEBY`-toimintoa sellaisenaan ei voi kääntää suoraksi tietokantakyselyksi. Siksi tämän toiminnon sisältävään ER-tietolähteeseen ei voi kohdistaa kyselyitä. Sitä ei myöskään voi käyttää ER-toimintojen, kuten [FILTER](er-functions-list-filter.md)- ja [ALLITEMSQUERY](er-functions-list-allitemsquery.md)-toimintojen, käyttöalueessa, jossa voidaan käyttää vain kyselykelpoisia tietolähteitä.

Lisätietoja on [esimerkissä 3](#example-3) ja [esimerkissä 4](#example-4).

### <a name="comparability"></a>Vertailukelpoisuus

Koska SQL-tietokantamoduuli ja Finance-sovelluspalvelin voivat käyttää eri järjestysarvoa yksittäiselle merkille, tietueluettelon lajittelutulos voi olla erilainen, kun lajittelussa käytetään [Merkkijono](er-formula-supported-data-types-primitive.md#string)-kenttää. Lisätietoja on kohdassa [esimerkki 5](#example-5).

## <a name="example-1-in-memory-default-execution"></a><a name="example-1"></a>Esimerkki 1: Oletussuoritus muistin sisällä

Jos syötät *Lasketun kenttä*-tyypin **DS**-tietolähteen, ja se sisältää lausekkeen `SPLIT ("C|B|A", "|")`, lauseke `FIRST( ORDERBY( DS, DS. Value)).Value` palauttaa tekstiarvon **A**.

## <a name="example-2-in-memory-explicit-execution"></a><a name="example-2"></a>Esimerkki 2: Erillinen suoritus muistin sisällä

Jos **Toimittaja** on määritetty *Taulukon tietueet* -tyypin ER-tietolähteeksi, joka viittaa **VendTable**-tauluun, sekä lauseke `ORDERBY (Vendor, Vendor.'name()')` että lauseke `ORDERBY ("InMemory", Vendor, Vendor.'name()')` palauttavat toimittajaluettelon, joka on lajiteltu nimen mukaan nousevassa järjestyksessä.

Kun lauseke `ORDERBY ("Query", Vendor, Vendor.'name()')` konfiguroidaan ER-mallin määrityksen suunnittelussa, [tarkistusvirhe](er-components-inspections.md#i8) tapahtuu suunnittelun aikana, koska polku `Vendor.'name()'` viittaa sovellusmenetelmään, jonka logiikkaa ei voi muuntaa suoraksi tietokantakyselyksi.

## <a name="example-3-database-query"></a><a name="example-3"></a>Esimerkki 3: Tietokantakysely

Jos **TaxTransaction** on määritetty *Taulukon tietueet* -tyypin ER-tietolähteeksi, joka viittaa **TaxTrans**-taulukkoon, lauseke `ORDERBY ("Query", TaxTransaction, TaxTransaction.TaxCode)` lajittelee tietueet sovellustietokannan tasolla ja palauttaa verotapahtumien luettelon, joka on lajiteltu verokoodin mukaan nousevassa järjestyksessä.

## <a name="example-4-queryable-data-sources"></a><a name="example-4"></a>Esimerkki 4: Kyselykelpoiset tietolähteet

Jos **TaxTransaction** on määritetty *Taulukon tietueet* -tyypin ER-tietolähteeksi, joka viittaa **TaxTrans**-taulukkoon ER-tietolähde **TaxTransactionFiltered**, voidaan konfiguroida niin, että se sisältää lausekkeen `FILTER(TaxTransaction, TaxCode="VAT19")`, joka hakee tapahtumia määritetylle verokoodille. Koska konfiguroitu  ER-tietolähde **TaxTransactionFiltered** on kyselykelpoinen, lauseke `ORDERBY ("Query", TaxTransactionFiltered, TaxTransactionFiltered.TransDate)` voidaan konfiguroida palauttamaan suodatettujen verotapahtumien luettelo, joka on lajiteltu tapahtumapäivämäärän mukaan nousevassa järjestyksessä.

Jos **TaxTransactionOrdered** määritetään *Laskettu kenttä* -tyypin ER-tietolähteeksi, joka sisältää lausekkeen `ORDERBY ("Query", TaxTransaction, TaxTransaction.TransDate)` ja *Laskettu kenttä* -tyypin ER-tietolähteeksi, joka sisältää lausekkeen `FILTER(TaxTransactionOrdered, TaxCode="VAT19")`, ER-mallin määrityksen suunnittelun aikana tapahtuu [oikeellisuustarkistusvirhe](er-components-inspections.md#i18). Tämä virhe ilmenee, koska [FILTER](er-functions-list-filter.md#usage-notes)-toiminnon ensimmäisen argumentin täytyy viitata kyselykelpoiseen ER-tietolähteeseen, mutta `ORDERBY`-toiminnon sisältävä **TaxTransactionOrdered**-tietolähde ei ole kyselykelpoinen.

## <a name="example-5-comparability"></a><a name="example-5"></a>Esimerkki 5: Vertailukelpoisuus

### <a name="prerequisites"></a>Edellytykset

1. *Laskettu kenttä* -tyypin **DS1**-tietolähde, joka sisältää lausekkeen `SPLIT ("D1|_D2|D3", "|")`.
2. Avaa **[Taloushallinnon dimensioiden arvot](../../../finance/general-ledger/financial-dimensions.md)** -sivu ja valitse **CostCenter**-dimensio.
3. Syötä seuraavat dimensioarvot: **D1**, **\_D2** ja **D3**.

### <a name="sorting-in-memory"></a>Lajitteleminen muistissa

1. Määritä *Laskettu kenttä* -tyypin **DS2**-tietolähde, joka sisältää lausekkeen `ORDERBY("InMemory", DS1, DS1.Value)`.
2. Huomaa, että lauseke `FIRST(DS2).Value` palauttaa tekstiarvon **"D1"**, lauseke `INDEX(DS2, COUNT(DS2)).Value` palauttaa tekstiarvon **"\_D2"**, ja lauseke `STRINGJOIN(DS2, DS2.Value, "|")` palauttaa tekstiarvon **"D1\|D3\|\_D2"**.

### <a name="sorting-in-database"></a>Lajitteleminen tietokannassa

1. Määritä **DS3**-tietolähde, joka on *Taulukkotietueet*-tyyppiä, joka viittaa **FinancialDimensionValueEntity**-entiteettiin.
2. Määritä *Laskettu kenttä* -tyypin **DS4**-tietolähde, joka sisältää lausekkeen `FILTER(DS3, DS3.FinancialDimension="CostCenter")`.
3. Määritä *Laskettu kenttä* -tyypin **DS5**-tietolähde, joka sisältää lausekkeen `ORDERBY(DS4, DS4.DimensionValue)`.
4. Huomaa, että lauseke `FIRST(DS5).Value` palauttaa tekstiarvon **"\_D2"**, lauseke `INDEX(DS5, COUNT(DS5)).Value` palauttaa tekstiarvon **"D3"**, ja lauseke `STRINGJOIN(DS5, DS5.Value, "|")` palauttaa tekstiarvon **"\_D2\|D1\|D3"**.

## <a name="additional-resources"></a>Lisäresurssit

[Luettelotoiminnot](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
