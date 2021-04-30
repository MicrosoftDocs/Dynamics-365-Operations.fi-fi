---
title: ER-muotoisten XML-elementtien suorittamisen lykkäys
description: Tässä ohjeaiheessa selitetään, miten sähköisen raportoinnin (ER) muotoisten XML-elementtien suorittamista lykätään.
author: NickSelin
ms.date: 03/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EROperationDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-01-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 361e16b0dba3aa46c71477efaa89a2661a3bcd75
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/13/2021
ms.locfileid: "5894049"
---
# <a name="defer-the-execution-of-xml-elements-in-er-formats"></a>ER-muotoisten XML-elementtien suorittamisen lykkäys

[!include [banner](../includes/banner.md)]

## <a name="overview"></a>Yleiskatsaus

Voit käyttää [Sähköisen raportoinnin (ER)](general-electronic-reporting.md) kehyksen toimintojen suunnitteluohjelmaa [määrittääksesi](./tasks/er-format-configuration-2016-11.md) lähtevien XML-muotoisten asiakirjojen luomiseen käytettävän ER-ratkaisun [muotokomponenttia](general-electronic-reporting.md#FormatComponentOutbound). Määritetyn muotokomponentin hierarkiarakenne koostuu erityyppisistä muotoelementeistä. Näitä muotoelementtejä käytetään luotujen asiakirjojen suorituksenaikaiseen täyttämiseen tarvittavilla tiedoilla. Kun ER-muoto suoritetaan, muotoelementit suoritetaan oletusarvoisesti samassa järjestyksessä kuin ne esitetään muotohierarkiassa: yksi kerrallaan, ylhäältä alas. Suunnittelun aikana voit kuitenkin muuttaa kaikkien määritetyn muotokomponentin XML-elementtien suoritusjärjestystä.

Ottamalla käyttöön määritetyssä muodossa olevan XML-elementin <a name="DeferredXmlElementExecution"></a>**Lykätty suorittaminen** -asetuksen voit lykätä (siirtää myöhemmäksi) kyseisen elementin suorittamista. Tällöin elementtiä ei suoriteta, ennen kuin kaikki muut sen pääelementin osat on suoritettu.

Saat lisätietoja tästä toiminnosta suorittamalla tämän ohjeaiheen seuraavan esimerkin.

## <a name="limitations"></a>Rajoitukset

**Lykätty suorittaminen** -asetusta tuetaan vain sellaisten XML-elementtien osalta, jotka on määritetty **lähtevien** XML-muotoisten asiakirjojen luonnissa käytettävää ER-muotoa varten.

**Lykätty suorittaminen** -aseusta tuetaan vain sellaisten XML-elementtien osalta, jotka sijaitsevat vain yhdessä muussa XML-elementissä. Siten sitä ei voi soveltaa XML-elementteihin, jotka sijaitsevat muunlaisissa muotoleementeissä (kutan **XML-sarja**-elementissä).

**Lykätty suorittaminen** -vaihtoehtoa ei tueta sellaisten XML-elementtien osalta, jotka sijaitsevat muotoelementissä **Yleinen\\Tiedosto**, kun **Jaa tiedosto** -asetuksen arvona on **Kyllä**. Lisätietoja XML-tietojen jakamisesta on kohdassa [Luotujen XML-tiedostojen jakaminen tiedoston koon ja sisällön määrän perusteella](er-split-files.md).

## <a name="example-defer-the-execution-of-an-xml-element-in-an-er-format"></a><a name="Example"></a>Esimerkki: ER-muotoisen XML-elementin suorituksen lykkäys

Seuraavissa vaiheissa selitetään, miten järjestelmänvalvojan sähköisen raportoinnin toiminnallinen konsultin [rooli](../sysadmin/tasks/assign-users-security-roles.md) voi määrittää ER-muodon, joka sisältää XML-elementin, jossa suoritusjärjestys eroaa muotohierarkian järjestyksestä.

Nämä vaiheet voidaan suorittaa Microsoft Dynamics 365 Financen **USMF**-esimerkkiyrityksessä.

### <a name="prerequisites"></a>Edellytykset

Tämän esimerkin suorittaminen edellyttää Financessa jonkin seuraavan roolin käyttöoikeutta **USMF**-yrityksessä:

- Sähköisen raportoinnin toiminnallinen konsultti
- Järjestelmänvalvoja

Jos et ole vielä suorittanut tätä esimerkkiä ohjeaiheessa [ER-muotoisten sarjaelementtien suorittamisen lykkäys](er-defer-sequence-element.md#Example), lataa seuraavat esimerkkinä käytettävän ER-ratkaisun [määritykset](general-electronic-reporting.md#Configuration).

| Sisällön kuvaus            | Tiedostonimi |
|--------------------------------|-----------|
| ER-tietomallin konfigurointi    | [Model to learn deferred elements.version.1.xml](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |
| ER-mallin yhdistämismääritys | [Mapping to learn deferred elements.version.1.1.xml](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |

Ennen kuin aloitat, sinun on myös ladattava ja tallennettava seuraavat esimerkkinä käytettävän ER-ratkaisun määritykset paikalliselle tietokoneellesi.

| Sisällön kuvaus     | Tiedostonimi |
|-------------------------|-----------|
| ER-muodon konfigurointi | [Format to learn deferred XML elements.version.1.1.xml](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |

### <a name="import-the-sample-er-configurations"></a>ER-mallikonfiguraation tuonti

1. Valitse **Organisaation hallinto** \> **Työtilat** \> **Sähköinen raportointi**.
2. Valitse **Raportointikonfiguraatiot**.
3. Jos **Määritykset**-sivun **Malli lykättyjen elementtien oppimiseen** -määritys ei ole saatavilla määrityspuussa, tuo ER-tietomallimääritys:

    1. Vallitse **Vaihto** ja sitten **Lataa XML-tiedostosta**.
    2. Valitse **Selaa**, etsi ja valitse tiedosto **Model to learn deferred elements.1.xml** ja valitse sitten **OK**.

4. Jos **Yhdistäminen lykättyjen elementtien oppimista varten** -määritys ei ole saatavilla määrityspuussa, tuo ER-malliyhdistämismääritys:

    1. Vallitse **Vaihto** ja sitten **Lataa XML-tiedostosta**.
    2. Valitse **Selaa**, etsi ja valitse tiedosto **Mapping to learn deferred elements.1.xml** ja valitse sitten **OK**.

5. Tuo ER-muotokonfiguraatio:

    1. Vallitse **Vaihto** ja sitten **Lataa XML-tiedostosta**.
    2. Valitse **Selaa**, etsi ja valitse tiedosto **Format to learn deferred XML elements.1.1.xml** ja valitse sitten **OK**.

6. Laajenna määrityspuussa **Malli lykättyjen elementtien oppimiseen**.
7. Tarkista tuotujen ER-määritysten luettelo määrityspuussa.

    ![Tuodut ER-määritykset määrityssivulla](./media/ER-DeferredXml-Configurations.png)

### <a name="activate-a-configuration-provider"></a>Aktivoi määrityslähde

1. Valitse **Organisaation hallinto** \> **Työtilat** \> **Sähköinen raportointi**.
2. Tarkista **Lokalisointikonfiguroinnit**-sivun **Konfiguraation lähteet** -osassa, että näyteyrityksen Litware, Inc. [konfiguraation lähde on luettelossa ja että sen tila on](general-electronic-reporting.md#Provider) aktiivinen (`http://www.litware.com`). Jos tämä määrityspalvelu ei ole luettelossa tai jos se ei ole merkittynä aktiiviseksi, noudata ohjeaiheen [Konfiguraation lähteen luominen ja sen merkitseminen aktiiviseksi](./tasks/er-configuration-provider-mark-it-active-2016-11.md) vaiheita.

    ![Lokalisointimääritykset-sivun esimerkkiyritys Litware, Inc.](./media/ER-DeferredXml-ElectronicReportingWorkspace.png)

### <a name="review-the-imported-model-mapping"></a>Tuodun tietomallimäärityksen tarkistaminen

Tarkista sen ER-mallimäärityskomponentin asetukset, joka on määritetty käyttämään verotapahtumia ja näyttämään käytetyt tiedot pyynnöstä.

1. Valitse **Organisaation hallinto** \> **Työtilat** \> **Sähköinen raportointi**.
2. Valitse **Raportointikonfiguraatiot**.
3. Valitse **Määritykset**-sivun määrityspuu ja laajenna **Malli lykättyjen elementtien oppimiseen**.
4. Valitse **Yhdistäminen lykättyjen elementtien oppimista varten** -määritys.
5. Avaa määritysluettelo valitsemalla **Suunnittelutoiminto**.
6. Tarkista määritystiedot valitsemalla **Suunnittelutoiminto**.
7. Valitse **Näytä tiedot**.
8. Tarkista tietolähteet, jotka on määritetty käyttämään verotapahtumia:

    - *Taulukkotietue* -tyypin **Tapahtumat**-tietolähde on määritetty käyttämään **TaxTrans**-sovellustaulukon käyttötietueita.
    - *Laskettu kenttä* -tyypin **Tositteet**-tietolähde on määritetty palauttamaan vaadittavat tositekoodit (**INV-10000349** ja **INV-10000350**) tietueluettelon muodossa.
    - *Laskettu kenttä* -tyypin **Suodatettu**-tietolähde on määritetty valitsemaan **Tapahtumat**-tietolähteestä vain vaadittavien tositteiden verotapahtumia.
    - *Laskettu kenttä* -tyypin **\$TaxAmount**-kenttä lisätään, jotta **Suodatettu** tietolähde näyttää veroarvon, jolla on vastakkainen etumerkki.
    - *Ryhmittely* -tyypin **Ryhmitelty**-tietolähde määritetään ryhmittelemään **Suodatettu**-tietolähteen suodatettuja verotapahtumia.
    - **Ryhmitelty**-tietolähteen **TotalSum**-koostekenttä määritetään laskemaan yhteen **Suodatettu**-tietolähteen **\$TaxAmount**-kentän arvot kaikkein kyseisen tietolähteen suodatettujen verotapahtumien osalta.

        ![Muokkaa GroupBy-parametreja -sivun TotalSum koostekenttä](./media/ER-DeferredXml-GroupByParameters.png)

9. Tarkista, miten määritetyt tietolähteet on sidottu tietomalliin ja miten ne näyttävät käytetyt tiedot, jotta ne ovat käytettävissä ER-muodossa:

    - **Suodatettu**-tietolähde on sidottu tietomallin **Data.List**-kenttään.
    - **Suodatettu**-tietolähteen **\$TaxAmount**-kenttä on sidottu tietomallin **Data.List.Value**-kenttään.
    - **Ryhmitelty**-tietolähteen **TotalSum**-kenttä on sidottu tietomallin **Data.Summary.Total**-kenttään.

    ![Mallimäärityksen suunnittelun sivu](./media/ER-DeferredXml-ModelMapping.png)

10. Sulje sivut **Mallimäärityksen suunnittelu** ja **Mallimääritykset**.

### <a name="review-the-imported-format"></a>Tuodun muodon tarkistaminen

1. Valitse **Määritykset**-sivun määrityspuusta määritys **Muoto lykättyjen XML-elementtien oppimiseen**.
2. Tarkista muototiedot valitsemalla **Suunnittelutoiminto**.
3. Valitse **Näytä tiedot**.
4. Tarkista niiden ER-muotokomponenttien asetukset, jotka on määritetty luomaan lähtevä verotapahtumien tietoja sisältävä asiakirja XML-muodossa:

    - XML-elementti **Raportti\\Sanoma** määritetään täyttämään lähtevä asiakirja yksittäisellä solmulla, joka sisältää sisäkkäiset XML-elementit (**Otsikko**, **Tietue** ja **Yhteenveto**).
    - XML-elementti **Raportti\\Sanoma\\Otsikko** määritetään täyttämään lähtevä asiakirja yksittäisellä otsikkosolmulla, jossa näkyvät prosessin aloituspäivä ja -aika.
    - XML-elementti **Raportti \\Sanoma\\Tietue** määritetään täyttämään lähtevä asiakirja yksittäisellä tietuesolmulla, jossa näkyvät yksittäisen verotapahtuman tiedot.
    - XML-elementti **Raportti\\Sanoma\\Yhteenveto** määritetään täyttämään lähtevä asiakirja yksittäisellä yhteenvetosolmulla, joka sisältää käsiteltyjen verotapahtumien veroarvojen summan.

    ![Sanoma-XML-elementti ja sisäkkäiset XML-elementit Muodon suunnittelun sivulla](./media/ER-DeferredXml-Format.png)

5. Tarkista seuraavat tiedot **Määritys**-välilehdessä:

    - **Raportti\\Sanoma\\Otsikko** -elementin ei tarvitse olla lähteeseen sidottu, jotta se loisi yksittäisen solmun lähtevässä asiakirjassa.
    - **ExecutionDateTime**-määrite luo otsikkosolmun lisäämisen päivän ja ajan (millisekunteihin asti).
    - **Raportti\\Sanoma\\Tietue** -elementti on sidottu **model.Data.List**-luetteloon, jotta luodaan yksittäinen tietuesolmu jokaiselle sidotun luettelon tietueelle.
    - **TaxAmount**-määrite on sidottu arvoon **model.Data.List.Value** (joka näkyy muodossa **\@.Value** suhteellisen polun näkymässä), jotta luodaan kulloisenkin verotapahtuman veroarvo.
    - **RunningTotal**-määrite on paikkamerkki veroarvojen juoksevalle summalle. Tällä hetkellä tällä määritteellä ei ole tulosta, koska sille ei ole määritetty sitovaa eikä oletusarvoista arvoa.
    - **ExecutionDateTime**-määrite luo päivän ja ajan (millisekunteihin asti) sille, milloin kulloinenkin tapahtuma käsitellään raportissa.
    - **Raportti\\Sanoma\\Yhteenveto** -elementin ei tarvitse olla tietolähteeseen sidottu, jotta se loisi yksittäisen solmun lähtevässä asiakirjassa.
    - **TotalTaxAmount**-määrite on sidottu **model.Data.Summary.Total**, jotta luodaan käsiteltyjen verotapahtumien veroarvojen summa.
    - **ExecutionDateTime**-määrite luo yhteenvetosolmun lisäämisen päivän ja ajan (millisekunteihin asti).

    ![Yhdistämismääritys-välilehti Muodon suunnittelu -sivulla](./media/ER-DeferredXml-Format2.png)

### <a name="run-the-imported-format"></a>Tuodun muodon suorittaminen

1. Vallitse **Muodon suunnittelu** -sivulla **Suorita**.
2. Lataa verkkoselaimen tarjoama tiedosto ja avaa se tarkistusta varten.

    ![Ladattu tiedosto](./media/ER-DeferredXml-Run.png)

Huomaa, että yhteenvetosolmussa on käsiteltyjen tapahtumien veroarvojen summa. Koska muoto on määritetty käyttämään arvoa **model.Data.Summary.Total** sitovasti tämän summan palauttamista varten, summa lasketaan kutsumalla mallin yhdistämismäärityksen *GroupBy*-tyypin **Ryhmitelty**-tietolähteen **TotalSum**-kooste. Tämän koosteen laskemiseksi mallin yhdistämismääritys iteroi kaikki tapahtumat, jotka on valittu **Suodatettu**-tietolähteessä. Kun verrataan yhteenvetosolmun ja viimeisimmän tietuesolmun suoritusaikoja, voidaan päätellä, että summan laskeminen kesti 12 millisekuntia (ms). Vertaamalla ensimmäisen ja viimeisen tietuesolmun suoritusaikoja voidaan päätellä, että kaikkien tietuesolmujen luominen kesti 9 millisekuntia. Siten yhteisaika oli 21 ms.

### <a name="modify-the-format-so-that-the-calculation-is-based-on-generated-output"></a>Muodon muokkaaminen siten, että laskeminen perustuu luotuun tulokseen

Jos tapahtuman suuruus on huomattavasti suurempi kuin tässä esimerkissä, laskemiseen voi kulua enemmän aikaa, ja se voi aiheuttaa suorituskykyongelmia. Muodon asetusta vaihtamalla voit ehkäistä näitä suorituskykyongelmia. Koska käytät veroarvoja lisätäksesi ne luotavaan raporttiin, voit käyttää näitä tietoja uudelleen veroarvojen laskemiseen. Lisä tietoja on kohdassa [Määritä muoto suorittamaan laskenta ja summaus](./tasks/er-format-counting-summing-1.md).

1. Valitse **Muodon suunnittelija**-sivun **Muoto**-välilehden muotopuussa **Raportti**-tiedostoelementti.
2. Määritä **Kerää tulostiedot** -asetukseksi **Kyllä**. Voit nyt määrittää tämän muodon käyttämällä luodun raportin sisältöä tietolähteenä, jota voidaan käyttää sisäisillä ER-toiminnoilla [Tietojen keräys](er-functions-category-data-collection.md) -luokassa.
3. Valitse **yhdistämismääritys**-välilehdessä XML-elementti **Raportti\\Sanoma\\Tietue**.
4. Määritä **Kerätyn tietoavaimen nimi** -lausekkeen arvoksi `WsColumn`.
5. Määritä **Kerätyn tietoavaimen arvo** -lausekkeen arvoksi `WsRow`.

    ![Tietue-XML-elementti Muodon suunnittelija -sivulla](./media/ER-DeferredXml-Format3.png)

6. Valitse **Raportti\\Sanoma\\Tietue\\TaxAmount** -määrite.
7. Määritä **Kerätyn tietoavaimen nimi** -lausekkeen arvoksi `SummingAmountKey`.

    ![TaxAmount-määrite Muodon suunnittelija -sivulla](./media/ER-DeferredXml-Format4.png)

    Voit katsoa tämän asetuksen virtuaalisen laskentataulukon täyttämiseksi, jossa solun A1 arvo lisätään jokaisen käsitellyn verotapahtuman verosumman arvoon.

8. Valitse **Raportti\\Sanoma\\Tietue\\RunningTotal** -määrite ja sitten **Muokkaa kaava**.
9. Määritä `SUMIF(SummingAmountKey, WsColumn, WsRow)` -lauseke käyttämällä sisäistä [SUMIF](er-functions-datacollection-sumif.md) ER -toimintoa ja valitsemalla **Tallenna**.

    ![SUMIF-lauseke](./media/ER-DeferredXml-FormulaDesigner.png)

10. Sulje **Reseptien suunnittelu** -sivu.
11. Valitse ensin **Tallenna** ja sitten **Suorita**.
12. Lataa ja tarkista verkkoselaimen tarjoama tiedosto.

    ![Ladattu tiedosto](./media/ER-DeferredXml-Run1.png)

    Viimeinen tietuesolmu sisältää kaikille käsitellyille tapahtumille luotua tulosta tietolähteenä käyttäen lasketun veroarvojen juoksevan summan. Tämä tietolähde alkaa raportin alusta ja jatkuu viimeisimpään verotapahtumaan asti. Yhteenvetosolmu sisältää kaikkien sellaisten käsiteltyjen tapahtumien veroarvojen summan, jotka on laskettu mallin yhdistämismäärityksessä käyttämällä *GroupBy* -tyypin tietolähdettä. Huomaa, että nämä arvot ovat samat. Siksi voidaan käyttää tulokseen perustuvaa yhteenlaskua **GroupBy**-tyypin käytön sijaan. Vertaamalla ensimmäisen tietuesolmun ja yhteenvetosolmun suoritusaikoja voidaan päätellä, että kaikkien tietuesolmujen luominen ja laskeminen kesti 11 millisekuntia. Siten muokattu muoto on noin kaksi kertaa alkuperäistä muotoa nopeampi tietuesolmujen luomisessa ja veroarvojen summien laskemisessa.

13. Valitse **Raportti\\Sanoma\\Yhteenveto\\TotalTaxAmount** -määrite ja sitten **Muokkaa kaava**.
14. Kirjoita `SUMIF(SummingAmountKey, WsColumn, WsRow)` -lauseke olemassa olevan lausekkeen sijaan.
15. Valitse ensin **Tallenna** ja sitten **Suorita**.
16. Lataa ja tarkista verkkoselaimen tarjoama tiedosto.

    ![Ladattu tiedosto](./media/ER-DeferredXml-Run2.png)

    Huomaa, että veroarvojen juokseva summa viimeisessä tietuesolmussa vastaa nyt yhteenvetosolmun summaa.

### <a name="put-values-of-output-based-summing-in-the-report-header"></a>Tulosperusteisten summien laskemisen arvojen määritys raportin otsikossa

Jos sinun on esimerkiksi esitettävä veroarvojen summa raportin otsikossa, voit muokata muotoa.

1. Valitse **Muodon suunnittelija** -sivun **Muoto**-välilehdessä XML-elementti **Raportti\\Sanoma\\Yhteenveto**.
2. Valitse **Siirrä ylös**.
3. Valitse ensin **Tallenna** ja sitten **Suorita**.
4. Lataa ja tarkista verkkoselaimen tarjoama tiedosto.

    ![Ladattu tiedosto](./media/ER-DeferredXml-Run3.png)

    Huomaa, että yhteenvetosolmun veroarvojen summa on nyt 0 (nolla), koska tämä summa lasketaan nyt luodun tuloksen perusteella. Kun ensimmäinen tietuesolmu luodaan, luotu tulos ei vielä sisällä tietuesolmuja, joilla on tapahtumatietoja. Voit määrittää tämän muodon lykkäämään **Raportti\\Sanoma\\Yhteenveto** -sarjaelementtiä siihen asti, että **Raportti\\Sanoma\\Tietue** -sarjaelementti on suoritettu kaikkien verotapahtumien osalta.

### <a name="defer-the-execution-of-the-summary-xml-element-so-that-the-calculated-total-is-used"></a>XML-elementin suorittamisen lykkääminen siten, että käytetään laskettua summaa

1. Valitse **Muodon suunnittelija** -sivun **Muoto**-välilehdessä XML-elementti **Raportti\\Sanoma\\Yhteenveto**.
2. Määritä **Lykätty suorittaminen** -asetukseksi **Kyllä**.

    ![Muodon suunnittelija -sivun XML-elementin lykätyn suorittamisen vaihtoehto](./media/ER-DeferredXml-Format5.png)

3. Valitse ensin **Tallenna** ja sitten **Suorita**.
4. Lataa ja tarkista verkkoselaimen tarjoama tiedosto.

    ![Ladattu tiedosto](./media/ER-DeferredXml-Run4.png)

    **Raportti\\Sanoma\\Yhteenveto** -elementti suoritetaan nyt vasta, kun kaikki muut sen pääelementin **Raportti\\Sanoma** alaiset kohteet on suoritettu. Siten se suoritetaan sen jälkeen, kun **Raportti\\Sanoma\\Tietue** -sarjaelementti on suoritettu kaikkien **model.Data.List** -tietolähteen verotapahtumien osalta. Tämä ilmenee ensimmäisen ja viimeisen tietuesolmun sekä otsikko- ja yhteenvetosolmujen suoritusajoista.

## <a name="additional-resources"></a>Lisäresurssit

- [Määritä muoto suorittamaan laskenta ja summaus](./tasks/er-format-counting-summing-1.md)
- [Sähköisen raportoinnin muodon suorittamisen seuraaminen suorituskykyyn liittyvien ongelmien ratkaisemiseksi](trace-execution-er-troubleshoot-perf.md)
- [ER-muotoisten sarjaelementtien suorittamisen lykkäys](er-defer-sequence-element.md#Example)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]