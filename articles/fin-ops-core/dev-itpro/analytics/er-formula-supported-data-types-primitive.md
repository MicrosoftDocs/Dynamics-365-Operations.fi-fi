---
title: Sähköisen raportoinnin kaavan tukemat primitiiviset tietotyypit
description: Tässä artikkelissa on tietoja sähköisen raportoinnin (ER) kaavojen tukemista primitiivisistä tietotyypeistä.
author: NickSelin
ms.date: 06/02/2021
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 41cda188e774630e96c46fba1200fd2e640f9915
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8891872"
---
# <a name="supported-primitive-data-types-for-electronic-reporting-formulas"></a>Sähköisen raportoinnin kaavan tukemat primitiiviset tietotyypit

[!include [banner](../includes/banner.md)]

Tässä artikkelissa on tietoja [sähköisen raportoinnin (ER)](general-electronic-reporting.md) lausekkeiden tukemista primitiivisistä tietotyypeistä. Seuraavassa on luettelo primitiivisistä tietotyypeistä:

- [totuusarvo](#boolean)
- [päivämäärä](#date)
- [päivämäärä/aika](#datetime)
- [luettelointi](#enumeration)
- [guid](#guid)
- [kokonaisluku](#integer)
- [int64](#int64)
- [reaaliluku](#real)
- [merkkijono](#string)

## <a name="boolean"></a><a name="boolean"></a>Boolen arvo

*totuusarvo*-tietotyyppi sisältää arvon, joka arvioidaan joko arvoksi *tosi* tai *epätosi*. Varattuja literaalisia avainsanoja **Tosi** and **Epätosi** voidaan käyttää aina, kun *totuusarvo*-lauseketta odotetaan. Oletusarvo on *epätosi*.

*totuusarvo*-arvon sisäinen esitys on *kokonaisluku*. *kokonaisluku*-arvo 0 (nolla) arvioidaan *epätosi*-arvoksi ja kaikki muut *kokonaisluku*-arvot arvioidaan *tosi*-arvoina. Kun [tarkistat](general-electronic-reporting-formula-designer.md#TestFormula) konfiguroidun lausekkeen, joka palauttaa *totuusarvon* [ER-kaavojen suunnittelussa](er-advanced-formula-editor.md), testitulosruudussa näkyy arvo *0* (nolla), kun lauseke palauttaa arvon *epätosi*. Muussa tapauksessa testituloksen ruutu esittää *1*.

*Totuusarvo* ei muunnu epäsuorasti. [TEXT](er-functions-text-text.md)-toiminnolla voit kuitenkin nimenomaisesti muuntaa *totuusarvon* *merkkijonoksi*:

- *epätosi*-arvo muunnetaan merkkijonoksi **Epätosi**.
- *tosi*-arvo muunnetaan merkkijonoksi **Tosi**.

> [!NOTE]
> Tämä muunnos ei riipu tarjottavasta kielen ja kielialueen [kontekstista](er-design-multilingual-reports.md).

Vertailu [operaattorit](er-formula-language.md#Operators) ovat ainoa operaattorityyppi, jota voi käyttää *totuusarvo*-tietotyypin kanssa. Seuraavien operaattorien avulla voidaan vertailla kahta *totuusarvoa*: \<\> ja =.

## <a name="date"></a><a name="date"></a>Päivämäärä

Primitiivinen *päivämäärä*-tietotyyppi tallentaa päivän, kuukauden ja vuoden. Päivämäärät voidaan aloittaa seuraavien toimintojen avulla:

- [DATEVALUE](er-functions-datetime-datevalue.md)
- [NULLDATE](er-functions-datetime-nulldate.md)
- [SESSIONTODAY](er-functions-datetime-sessiontoday.md)
- [TODAY](er-functions-datetime-today.md)

*Päivämäärä*-tietotyyppi voi sisältää päiviä välillä 1.1.1900 - 31.12.2154. Oletusarvo on **tyhjäarvo** ja sen sisäinen esitys on päivämäärä 1.1.1900.

*Päivämäärä* ei muunnu epäsuorasti. Voit kuitenkin käyttää seuraavia täsmällisiä muuntotoimintoja:

- [DATEFORMAT](er-functions-datetime-dateformat.md)
- [DATETODATETIME](er-functions-datetime-datetodatetime.md)
- [TEXT](er-functions-text-text.md)

[ADDDAYS](er-functions-datetime-adddays.md)-toiminnolla voit lisätä ja vähentää päiviä päivämääristä. Näin voit siirtää päivämäärän tietyn määrän päiviä tulevaisuuteen tai menneisyyteen. [DAYS](er-functions-datetime-days.md)-toiminnolla voit vähentää päivämääriä toisistaan ja laskea päivien eron. Lisätietoja *päivämäärä*-arvojen muuntamisesta on [päivämäärä- ja aikaluokan ER-toimintojen luettelossa](er-functions-category-datetime.md).

Vertailu [operaattorit](er-formula-language.md#Operators) ovat ainoa operaattorityyppi, jota voi käyttää *päivämäärä*-tietotyypin kanssa. Seuraavien operaattorien avulla voidaan vertailla kahta *päivämäärä*-arvoa: \<\>, \<, \<=, =, \> ja \>=.

## <a name="datetime"></a><a name="datetime"></a>Datetime

Primitiivinen *päivämäärä/aika*-tietotyyppi yhdistää *päivämäärä*-tyypin ja arvon, joka vastaa keskiyöstä lähtien kulunutta aikaa. Aika ilmaistaan tunteina, minuutteina, sekunteina ja sekuntien osina. *päivämäärä/aika*-arvo sisältää myös aikavyöhykkeen tiedot.

*päivämäärä/aika*-tietotyyppi voi sisältää päivämääriä välillä 1.1.1900 (1900-01-01T00:00:00.0000000+00:00 round-trip[-muodossa](/dotnet/standard/base-types/standard-date-and-time-format-strings)) – 31.12.2154 (2154/12/31T11:59:59.9999999+00:00 round-trip-muodossa). *päivämäärä/aika*-tyypin pienin aikayksikkö on sekunnin 10 miljoonasosaa.

> [!NOTE]
> Kun **hh**-[-tarkenninta ](/dotnet/standard/base-types/standard-date-and-time-format-strings) käytetään tunneissa, isompia aika-arvoja kuin 12:59:59:9999999 ei voida tulkita kelvollisiksi ajoiksi.
>
> Kun **HH**-tarkenninta käytetään tunneissa, isompia aika-arvoja kuin 23:59:59:9999999 ei voida tulkita kelvollisiksi ajoiksi.

Oletusarvo on **tyhjäarvo** ja sisäinen esitys on päivämäärä 1.1.1900 (1900-01-01T00:00:00.0000000+00:00 round-trip-muodossa).

Päivämäärä/aika-arvot voidaan aloittaa seuraavien toimintojen avulla:

- [DATETIMEVALUE](er-functions-datetime-datetimevalue.md)
- [NULNULLDATETIMELDATE](er-functions-datetime-nulldatetime.md)
- [SESSIONNOW](er-functions-datetime-sessionnow.md)
- [NOW](er-functions-datetime-now.md)

*päivämäärä/aika* ei muunnu epäsuorasti. Voit kuitenkin käyttää seuraavia täsmällisiä muuntotoimintoja:

- [DATETIMEFORMAT](er-functions-datetime-datetimeformat.md)
- [TEXT](er-functions-text-text.md)

Lisätietoja *päivämäärä/aika*-arvojen muuntamisesta on [päivämäärä- ja aikaluokan ER-toimintojen luettelossa](er-functions-category-datetime.md).

Vertailu [operaattorit](er-formula-language.md#Operators) ovat ainoa operaattorityyppi, jota voi käyttää *päivämäärä/aika*-tietotyypin kanssa. Seuraavien operaattorien avulla voidaan vertailla kahta *päivämäärä/aika*-arvoa: \<\>, \<, \<=, =, \> ja \>=.

## <a name="enumeration"></a><a name="enumeration"></a>Luettelointi

Primitiivinen *luettelointi*-tietotyyppi on literaalien luettelo. Voit käyttää luetteloita, jotka on määritetty sovelluksen [lähdekoodissa](../dev-ref/xpp-data-primitive.md#enum). Voit myös esitellä omat listat ER-tietomallissa ja ER-muodon komponentissa.

Sovelluksen *luettelointia* voidaan käyttää minkä tahansa ER-mallimäärityksen ja ER-muodon lausekkeissa.

Seuraavassa kuvassa kerrotaan, miten voit lisätä **CustVendCorrectiveReasonCode**-mallin listan muokattavaan ER-tietomalliin.

[![Mallin luetteloinnin määritys ER-tietomallin suunnittelussa.](./media/er-formula-supported-data-types-primitive-enum1.gif)](./media/er-formula-supported-data-types-primitive-enum1.gif)

Mallien *luettelointia* voidaan käyttää minkä tahansa ER-mallin määrityksen ja ER-muodon lausekkeissa, jotka on luotu tietomallissa, jossa *luettelointi* on otettu käyttöön.

Seuraavassa kuvassa kerrotaan, miten **Luonnollisen käänteisen kulun alaluokkien Luettelo** -muodon luettelointi voidaan lisätä muokattavaan ER-muotoon.

[![Muodon luetteloinnin määritys ER-muodon suunnittelussa.](./media/er-formula-supported-data-types-primitive-enum2.gif)](./media/er-formula-supported-data-types-primitive-enum2.gif)

Muodon *luettelointia* voi käyttää vain sen ER-muodon lausekkeissa, jossa *luettelointi* on otettu käyttöön.

Käytä ER-tietolähteiden soveltuvaa tyyppiä, jotta määritetty luettelointi voidaan tuoda määritettyyn ER-komponenttiin vakiona tai arvona, jonka ER-ratkaisua suorittava käyttäjä määritti valintaikkunassa ajon aikana.

- Sovelluksen luettelointeja voi käyttää käyttämällä **Dynamics 365 for Operations \ Luettelointi**- ja **Yleinen \ Käyttäjän syöteparametrit** -tietolähteitä. Seuraavassa kuvassa kerrotaan, miten voit lisätä muokattavaan ER-muotoon **appenumNoYes**- ja **uipNoYes**-tietolähteet, jotka viittaavat **NoYes**-sovelluksen luettelointiin.

    [![Sovelluksen luettelointitietolähteiden lisääminen ER-muodon suunnittelussa.](./media/er-formula-supported-data-types-primitive-enum3a.gif)](./media/er-formula-supported-data-types-primitive-enum3a.gif)

- Tietomallin luettelointeja voi käyttää käyttämällä **Tietomalli \ Luettelointi**- ja **Yleinen \ Luetteloinnin käyttäjän syöteparametrit** -tietolähteitä. Seuraavassa kuvassa kerrotaan, miten voit lisätä muokattavaan ER-muotoon **CustVendCorrectiveReasonCode**-tietolähteen joka viittaa **CustVendCorrectiveReasonCode**-tietomallin luettelointiin.

    [![Mallin luettelointitietolähteiden lisääminen ER-muodon suunnittelussa.](./media/er-formula-supported-data-types-primitive-enum3b.gif)](./media/er-formula-supported-data-types-primitive-enum3b.gif)

- Muodon luettelointeja voi käyttää käyttämällä **Muoto \ Luettelointi**- ja **Muoto \ Luetteloinnin käyttäjän syöteparametrit** -tietolähteitä. Seuraavassa kuvassa kerrotaan, miten voit lisätä muokattavaan ER-muotoon **NaturaReverseCharge**-tietolähteen, joka viittaa **Luonnollisen käänteisen kulun alaluokat** -muodon luettelointiin.

    [![Muodon luettelointitietolähteiden lisääminen ER-muodon suunnittelussa.](./media/er-formula-supported-data-types-primitive-enum3c.gif)](./media/er-formula-supported-data-types-primitive-enum3c.gif)

*luettelointi* ei muunnu epäsuorasti. Voit kuitenkin muuntaa *luetteloinnin* [TEX](er-functions-text-text.md)-muuntotoiminnon avulla tekstimerkkijonoksi. Tämä muunnos ei riipu kielestä. Tietoja *luettelointi*-arvon ja asianmukaisten kielikohtaisten otsikkojen käytöstä on [LISTOFFIELDS](er-functions-list-listoffields.md)- ja [GETENUMVALUEBYNAME](er-functions-text-getenumvaluebyname.md)-funktioiden käyttöesimerkeissä.

Vertailu [operaattorit](er-formula-language.md#Operators) ovat ainoa operaattorityyppi, jota voi käyttää *luettelointi*-tietotyypin kanssa. Seuraavien operaattorien avulla voidaan vertailla kahta *luettelointi*: \<\> ja =.

## <a name="guid"></a><a name="guid"></a>Guid

Primitiivinen *guid*-tietotyyppi sisältää yleisen yksilöivän tunnisteen (GUID) arvon. GUID on arvo, jota voidaan käyttää kaikissa tietokoneissa ja verkoissa aina, kun se edellyttää yksilöivän tunnuksen. On epätodennäköistä, että numero monistetaan. Kelvollinen GUID vastaa kaikkia seuraavia määrityksiä:

- Tässä tunnuksessa on oltava 32 heksadesimaalimerkkiä.
- Lisäksi seuraavissa sijainnissa on oltava neljä yhdysviivamerkkiä: 8-4-4-4-12.
- Lisäksi valinnaiset sulkeet \{\} voi lisätä merkkijonon alkuun ja loppuun. Esimerkiksi sekä **\{2CDB0FE7-D7B3-4938-A0F0-FE28FB8FE212\}** että **2CDB0FE7-D7B3-4938-A0F0-FE28FB8FE212** ovat kelvollisia GUID-merkkijonoja.
- Sen vuoksi yhteensä on oltava 36 tai 38 merkkiä sen mukaan, lisätäänkö sulkeita.
- Heksadesimaalimerkeissä käytettävät kirjaimet voivat olla isoja kirjaimia (A–F), pieniä kirjaimia (a –f) tai näiden yhdistelmiä.

Voit käyttää seuraavia täsmällisiä muuntotoimintoja:

- [GUIDVALUE](er-functions-text-guidvalue.md)
- [TEXT](er-functions-text-text.md)

Vertailu [operaattorit](er-formula-language.md#Operators) ovat ainoa operaattorityyppi, jota voi käyttää *guid*-tietotyypin kanssa. Seuraavien operaattorien avulla voidaan vertailla kahta *guid*-arvoa: \<\> ja =.

## <a name="integer"></a><a name="integer"></a>Kokonaisluku

Primitiivinen *kokonaisluku* edustaa lukua, jolla ei ole desimaaleja. Kokonaislukuja käytetään toistuvien lauseiden ohjausmuuttujina tai tietueluetteloiden indekseinä.

*Kokonaisluku*-literaali on kokonaisluku, joka ilmaistaan suoraan ER-[lausekkeessa](general-electronic-reporting-formula-designer.md#formula-designer-overview) (kaavassa), esimerkiksi **12345**. *Kokonaisluku* on 32 bittiä leveä. Oletusarvo on **0** ja sisäinen esitys on pitkä luku. *Kokonaisluku* muunnetaan automaattisesti *reaaliluvuksi*.

Lisäksi voit käyttää seuraavia täsmällisiä muuntotoimintoja:

- [INTVALUE](er-functions-conversion-intvalue.md)
- [NUMBERFORMAT](er-functions-text-numberformat.md)
- [TEXT](er-functions-text-text.md)

*Kokonaisluku*-arvojen alue on \[-2 147 483 647 : 2 147 483 647\].  Kaikkia tämän alueen kokonaislukuja voidaan käyttää literaaleina.

Kaikkia vertailuoperaattoreita ja matemaattisia [operaattoreita](er-formula-language.md#Operators) voidaan käyttää *kokonaisluku*-tietotyypin kanssa.

## <a name="int64"></a><a name="int64"></a>Int64

Primitiivinen *int64* edustaa lukua, jolla ei ole desimaaleja. *Int64*-arvoja käytetään toistuvien lauseiden ohjausmuuttujina tai tietueiden tunnisteina.

*int64* on 64 bittiä leveä. Oletusarvo on **0** ja sisäinen esitys on pitkä luku. *int64* muunnetaan automaattisesti *reaaliluvuksi*.

Lisäksi voit käyttää seuraavia täsmällisiä muuntotoimintoja:

- [INT64VALUE](er-functions-conversion-int64value.md)
- [NUMBERFORMAT](er-functions-text-numberformat.md)
- [TEXT](er-functions-text-text.md)

*int64*-arvojen alue on \[-9 223 372 036 854 775 807 : 9 223 372 036 854 775 807\].

Kaikkia vertailuoperaattoreita ja matemaattisia [operaattoreita](er-formula-language.md#Operators) voidaan käyttää *int64*-tietotyypin kanssa.

## <a name="real"></a><a name="real"></a>Reaaliluku

Primitiivinen *reaaliluku*-tietotyyppi voi sisältää kokonaislukujen lisäksi myös desimaaliarvoja. Desimaaliliteraaleja voi käyttää missä tahansa, jossa odotetaan *reaalilukua*. Desimaaliliteraali on desimaaliluku, joka ilmaistaan suoraan koodissa, esimerkiksi **2.19**.

> [!NOTE]
> ER-lausekkeissa käytetään aina pistettä (.) desimaalierottimena.

Reaalilukuja voidaan käyttää kaikissa lausekkeissa, ja niitä voidaan käyttää sekä vertailu- että aritmeettisissa operaattoreissa. *Reaaliluvun* tarkkuus on 16 merkitsevää numeroa. *Reaaliluvun* oletusarvo on **0.0** ja sisäinen esitys on binaarikoodattu digitaalinen numero (BCD). BCD-koodaus mahdollistaa tarkan esityksen arvoista, jotka ovat kerrannaisia luvusta 0.1. *reaaliluku*-muuttujan alue on -(10)<sup>127</sup> – (10)<sup>127</sup>. Kaikkia tämän alueen reaalilukuja voidaan käyttää literaaleina ER-lausekkeissa.

*Reaaliluku* ei muunnu epäsuorasti. Seuraavien toimintojen avulla voit kuitenkin nimenomaisesti muuntaa *reaaliluvun* muiksi tietotyypeiksi ja muita tietotyyppejä: *reaaliluvuiksi*

- [INTVALUE](er-functions-conversion-intvalue.md)
- [INT64VALUE](er-functions-conversion-int64value.md)
- [NUMBERFORMAT](er-functions-text-numberformat.md)
- [TEXT](er-functions-text-text.md)
- [VALUE](er-functions-conversion-value.md)

Kaikkia vertailuoperaattoreita ja matemaattisia [operaattoreita](er-formula-language.md#Operators) voidaan käyttää *reaaliluku*-tietotyypin kanssa.

## <a name="string"></a><a name="string"></a>Merkkijono

Primitiivinen *merkkijono*-tietotyyppi edustaa merkkien sarjaa, jota käytetään teksteihin, tilinumeroihin, osoitteisiin ja puhelinnumeroihin.

*Merkkijono*-literaalit ovat merkkejä, jotka on kirjoitettu lainausmerkkeihin (""). *Merkkijono*-literaaleja voidaan käyttää aina, kun ER-lausekkeissa odotetaan *merkkijono*-arvoja. Voit käyttää merkkijonoja loogisissa lausekkeissa, kuten vertailuissa. Voit myös liittää *merkkijono*-arvoja **\&**-operaattorin tai [CONCATENATE](er-functions-text-concatenate.md)-toiminnon avulla.

> [!NOTE]
> Jos liität kaksi *merkkijono*-arvoa ja haluat, että tuloksena oleva *merkkijono* kattaa useamman kuin yhden rivin, käytä arvojen välissä rivinvaihdon erotinta. TEXT-tuloksessa erotin voi olla merkki, joka luodaan käyttämällä [CHAR](er-functions-text-char.md)(10)- tai CHAR(13)-lauseketta. HTML-koodissa se voi olla **\<br\>**-tunniste.

*Merkkijonon* oletusarvo on tyhjä tekstimerkkijono, jossa ei ole merkkejä, ja sisäinen esitys on merkkien luettelo.

Merkkijonoja varten ei ole automaattisia muunnoksia. Voit kuitenkin käyttää seuraavia täsmällisiä muuntotoimintoja:

- [CHAR](er-functions-text-char.md)
- [FORMAT](er-functions-text-format.md)
- [LEFT](er-functions-text-left.md)
- [LEN](er-functions-text-len.md)
- [MID](er-functions-text-mid.md)
- [PADLEFT](er-functions-text-padleft.md)
- [REPLACE](er-functions-text-replace.md)
- [RIGHT](er-functions-text-right.md)
- [TEXT](er-functions-text-text.md)
- [TRANSLATE](er-functions-text-translate.md)
- [TRIM](er-functions-text-trim.md)
- [UPPER](er-functions-text-upper.md)

Lisätietoja *merkkijono*-arvojen muuntamisesta on [tekstiluokan ER-toimintojen luettelossa](er-functions-category-text.md).

*Merkkijonossa* voi olla rajaton määrä merkkejä.

Kaikkia vertailu [operaattoreita](er-formula-language.md#Operators) voidaan käyttää *merkkijono*-tietotyypin kanssa.

## <a name="additional-resources"></a>Lisäresurssit

- [Sähköisen raportoinnin yleiskatsaus](general-electronic-reporting.md)
- [Sähköisen raportoinnin kaavakieli](er-formula-language.md)
- [Tuetut yhdistelmätietotyypit](er-formula-supported-data-types-composite.md)
