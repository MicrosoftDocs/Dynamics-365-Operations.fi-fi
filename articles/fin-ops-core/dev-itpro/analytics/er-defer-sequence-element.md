---
title: ER-muotoisten sarjaelementtien suorittamisen lykkäys
description: Tässä ohjeaiheessa selitetään, miten sähköisen raportoinnin (ER) muotoisten sarjaelementtien suorittamista lykätään.
author: NickSelin
manager: kfend
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: EROperationDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-07-01
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 6efa4466dbf7f5ca1d3945acf15fac65d628d691
ms.sourcegitcommit: 1d5a4f70a931e78b06811add97c1962e8d93689b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/13/2020
ms.locfileid: "3124540"
---
# <a name="defer-the-execution-of-sequence-elements-in-er-formats"></a>ER-muotoisten sarjaelementtien suorittamisen lykkäys

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

## <a name="overview"></a>Yleiskatsaus

Voit käyttää [Sähköisen raportoinnin (ER)](general-electronic-reporting.md) kehyksen toimintojen suunnitteluohjelmaa [määrittääksesi](tasks/er-format-configuration-2016-11.md) lähtevien tekstimuotoisten asiakirjojen luomiseen käytettävän ER-ratkaisun [muotokomponenttia](general-electronic-reporting.md#FormatComponentOutbound). Määritetyn muotokomponentin hierarkiarakenne koostuu erityyppisistä muotoelementeistä. Näitä muotoelementtejä käytetään luotujen asiakirjojen suorituksenaikaiseen täyttämiseen tarvittavilla tiedoilla. Kun ER-muoto suoritetaan, muotoelementit suoritetaan oletusarvoisesti samassa järjestyksessä kuin ne esitetään muotohierarkiassa: yksi kerrallaan, ylhäältä alas. Suunnittelun aikana voit kuitenkin muuttaa kaikkien määritetyn muotokomponentin sarjaelementtien suoritusjärjestystä.

Ottamalla käyttöön määritetyssä muodossa olevan muotosarjaelementin <a name="DeferredSequenceExecution"></a>**Lykätty suorittaminen** -asetuksen voit lykätä (siirtää myöhemmäksi) kyseisen elementin suorittamista. Tällöin elementtiä ei suoriteta, ennen kuin kaikki muut sen pääelementin osat on suoritettu.

Saat lisätietoja tästä toiminnosta suorittamalla tämän ohjeaiheen seuraavan esimerkin.

## <a name="limitations"></a>Rajoitukset

**Lykätty suorittaminen** -asetusta tuetaan vain sellaisten sarjaelementtien osalta, jotka on määritetty **lähtevien** tekstimuotoisten asiakirjojen luonnissa käytettävää ER-muotoa varten.

**Lykätty suorittaminen** -asetusta ei voi käyttää sarjoissa, jotka on määritetty enimmäispituudeltaan rajoitetuiksi katkaistuiksi sarjoiksi.

## <a name="example-defer-the-execution-of-a-sequence-element-in-an-er-format"></a><a name="Example"></a>Esimerkki: ER-muotoisen sarjaelementin suorituksen lykkäys

Seuraavissa vaiheissa selitetään, miten järjestelmänvalvojan sähköisen raportoinnin toiminnallinen konsultin [rooli](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/sysadmin/tasks/assign-users-security-roles) voi määrittää ER-muodon, joka sisältää sarjaelementin, jossa suoritusjärjestys eroaa muotohierarkian järjestyksestä.

Nämä vaiheet voidaan suorittaa Microsoft Dynamics 365 Financen **USMF**-esimerkkiyrityksessä.

### <a name="prerequisites"></a>Edellytykset

Tämän esimerkin suorittaminen edellyttää Financessa jonkin seuraavan roolin käyttöoikeutta **USMF**-yrityksessä:

- Sähköisen raportoinnin toiminnallinen konsultti
- Järjestelmänvalvoja

Jos et ole vielä suorittanut tätä esimerkkiä ohjeaiheessa [ER-muotoisten XML-elementtien suorittamisen lykkäys](er-defer-xml-element.md#Example), lataa seuraavat esimerkkinä käytettävän ER-ratkaisun [määritykset](general-electronic-reporting.md#Configuration).

| Sisällön kuvaus            | Tiedostonimi |
|--------------------------------|-----------|
| ER-tietomallin konfigurointi    | [Model to learn deferred elements.version.1.xml](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |
| ER-mallin yhdistämismääritys | [Mapping to learn deferred elements.version.1.1.xml](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |

Ennen kuin aloitat, sinun on myös ladattava ja tallennettava seuraavat esimerkkinä käytettävän ER-ratkaisun määritykset.

| Sisällön kuvaus     |Tiedostonimi |
|-------------------------|----------|
| ER-muodon konfigurointi | [Format to learn deferred sequences.version.1.1.xml](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |

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
    2. Valitse **Selaa**, etsi ja valitse tiedosto **Format to learn deferred sequences.1.1.xml** ja valitse sitten **OK**.

6. Laajenna määrityspuussa **Malli lykättyjen elementtien oppimiseen**.
7. Tarkista tuotujen ER-määritysten luettelo määrityspuussa.

    ![Tuodut ER-määritykset määrityssivulla](./media/ER-DeferredSequence-Configurations.png)

### <a name="activate-a-configurations-provider"></a>Aktivoi konfiguraatiolähde

1. Valitse **Organisaation hallinto** \> **Työtilat** \> **Sähköinen raportointi**.
2. Tarkista**Lokalisointikonfiguroinnit**-sivun **Konfiguraation lähteet** -osassa, että näyteyrityksen Litware, Inc. [konfiguraation lähde on luettelossa ja että sen tila on](general-electronic-reporting.md#Provider) aktiivinen (`http://www.litware.com`). Jos tämä määrityspalvelu ei ole luettelossa tai jos se ei ole merkittynä aktiiviseksi, noudata ohjeaiheen [Konfiguraation lähteen luominen ja sen merkitseminen aktiiviseksi](./tasks/er-configuration-provider-mark-it-active-2016-11.md) vaiheita.

    ![Lokalisointimääritykset-sivun esimerkkiyritys Litware, Inc.](./media/ER-DeferredSequence-ElectronicReportingWorkspace.png)

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

        ![Muokkaa GroupBy-parametreja -sivun TotalSum koostekenttä](./media/ER-DeferredSequence-GroupByParameters.png)

9. Tarkista, miten määritetyt tietolähteet on sidottu tietomalliin ja miten ne näyttävät käytetyt tiedot, jotta ne ovat käytettävissä ER-muodossa:

    - **Suodatettu**-tietolähde on sidottu tietomallin **Data.List**-kenttään.
    - **Suodatettu**-tietolähteen **\$TaxAmount**-kenttä on sidottu tietomallin **Data.List.Value**-kenttään.
    - **Ryhmitelty**-tietolähteen **TotalSum**-kenttä on sidottu tietomallin **Data.Summary.Total**-kenttään.

    ![Mallimäärityksen suunnittelun sivu](./media/ER-DeferredSequence-ModelMapping.png)

10. Sulje sivut **Mallimäärityksen suunnittelu** ja **Mallimääritykset**.

### <a name="review-the-imported-format"></a>Tuodun muodon tarkistaminen

1. Valitse **Määritykset**-sivun määrityspuusta määritys **Muoto lykättyjen sarjojen oppimiseen**.
2. Tarkista muototiedot valitsemalla **Suunnittelutoiminto**.
3. Valitse **Näytä tiedot**.
4. Tarkista niiden ER-muotokomponenttien asetukset, jotka on määritetty luomaan lähtevä verotapahtumien tietoja sisältävä asiakirja tekstimuodossa:

    - **Raportti\\Rivit** -sarjamuotoelementti määritetään täyttämään lähtevä asiakirja yksittäisellä rivillä, joka luodaan sisäkkäisten sarjaelementtien (**Otsikko**, **Tietue** ja **Yhteenveto**) perusteella.

        ![Rivien sarjamuotoelementti ja sisäkkäiset elementit Muodon suunnittelun sivulla](./media/ER-DeferredSequence-Format.png)

    - **Raportti\\Rivit\\Otsikko** -sarjamuotoelementti määritetään täyttämään lähtevä asiakirja yksittäisellä otsikkorivillä, jossa näkyvät prosessin aloituspäivä ja -aika.
    - **Raportti \\Rivit\\Tietue** -sarjamuotoelementti määritetään täyttämään lähtevä asiakirja yksittäisellä rivillä, jossa näkyvät yksittäisten verotapahtumien tiedot. Nämä verotapahtumat erotetaan puolipisteellä.

        ![Tietueen sarjamuotoelementti, jossa erottimena käytetään puolipistettä](./media/ER-DeferredSequence-Format1.png)

    - **Raportti\\Rivit\\Yhteenveto** -sarjamuotoelementti määritetään täyttämään lähtevä asiakirja yksittäisellä yhteenvetorivillä, joka sisältää käsiteltyjen verotapahtumien veroarvojen summan.

4. Tarkista seuraavat tiedot **Määritys**-välilehdessä:

    - **Raportti\\Rivit\\Otsikko** -elementin ei tarvitse olla tietolähteeseen sidottu, jotta se loisi yksittäisen rivin lähtevässä asiakirjassa.
    - **Prefix1**-elementti luo **P1**-symboleja ilmaisemaan, että lisätty rivi on raportin otsikkorivi.
    - **ExecutionDateTime**-elementti luo otsikkorivin lisäämisen päivän ja ajan (millisekunteihin asti).
    - **Raportti\\Rivit\\Tietue** -elementti on sidottu **model.Data.List**-luetteloon, jotta luodaan yksittäinen rivi jokaiselle sidotun luettelon tietueelle.
    - **Prefix2**-elementti luo **P2**-symboleja ilmaisemaan, että lisätty rivi on verotapahtumien tietoja varten.
    - **TaxAmount**-elementti on sidottu arvoon **model.Data.List.Value** (joka näkyy muodossa **\@.Value** suhteellisen polun näkymässä), jotta luodaan kulloisenkin verotapahtuman veroarvo.
    - **RunningTotal**-elementti on paikkamerkki veroarvojen juoksevalle summalle. Tällä hetkellä tällä elementillä ei ole tulosta, koska sille ei ole määritetty sitovaa eikä oletusarvoista arvoa.
    - **ExecutionDateTime**-elementti luo päivän ja ajan (millisekunteihin asti) sille, milloin kulloinenkin tapahtuma käsitellään raportissa.
    - **Raportti\\Rivit\\Yhteenveto** -elementin ei tarvitse olla tietolähteeseen sidottu, jotta se loisi yksittäisen rivin lähtevässä asiakirjassa.
    - **Prefix3**-elementti luo **P3**-symboleja ilmaisemaan, että lisätty rivi sisältää veroarvon yhteensä.
    - **TotalTaxAmount**-elementti on sidottu **model.Data.Summary.Total**, jotta luodaan käsiteltyjen verotapahtumien veroarvojen summa.
    - **ExecutionDateTime**-elementti luo yhteenvetorivin lisäämisen päivän ja ajan (millisekunteihin asti).

    ![Yhdistämismääritys-välilehti Muodon suunnittelu -sivulla](./media/ER-DeferredSequence-Format2.png)

### <a name="run-the-imported-format"></a>Tuodun muodon suorittaminen

1. Vallitse **Muodon suunnittelu** -sivulla **Suorita**.
2. Lataa verkkoselaimen tarjoama tiedosto ja avaa se tarkistusta varten.

    ![Ladattu tiedosto](./media/ER-DeferredSequence-Run.png)

Huomaa, että yhteenvetorivillä 22 on käsiteltyjen tapahtumien veroarvojen summa. Koska muoto on määritetty käyttämään arvoa **model.Data.Summary.Total** sitovasti tämän summan palauttamista varten, summa lasketaan kutsumalla mallin yhdistämismääritystä käyttävän *GroupBy*-tyypin **Ryhmitelty**-tietolähteen **TotalSum**-kooste. Tämän koosteen laskemiseksi mallin yhdistämismääritys iteroi kaikki tapahtumat, jotka on valittu **Suodatettu**-tietolähteessä. Vertaamalla rivien 21 ja 22 suoritusaikoja voidaan päätellä, että summan laskemiseen kului 10 millisekuntia (ms). Vertaamalla rivien 2 ja 21 suoritusaikoja voidaan päätellä, että kaikkien tapahtumarivien luomiseen kului 7 millisekuntia. Siten yhteisaika oli 17 ms.

### <a name="modify-the-format-so-that-the-summing-is-based-on-generated-output"></a>Muodon muokkaaminen siten, että summien laskeminen perustuu luotuun tulokseen

Jos tapahtumien määrä on huomattavasti suurempi kuin tässä esimerkissä, summien laskemiseen voi kulua enemmän aikaa, ja se voi aiheuttaa suorituskykyongelmia. Muodon asetusta vaihtamalla voit ehkäistä näitä suorituskykyongelmia. Koska käytät veroarvoja lisätäksesi ne luotavaan raporttiin, voit käyttää näitä tietoja uudelleen veroarvojen summien laskemiseen. Lisä tietoja on kohdassa [Määritä muoto suorittamaan laskenta ja summaus](./tasks/er-format-counting-summing-1.md).

1. Valitse **Muodon suunnittelija**-sivun **Muoto**-välilehden muotopuussa **Raportti**-tiedostoelementti.
2. Määritä **Kerää tulostiedot** -asetukseksi **Kyllä**. Voit nyt määrittää tämän muodon käyttämällä aiemmin luodun raportin sisältöä tietolähteenä, jota voidaan käyttää sisäisillä ER-toiminnoilla [Tietojen keräys](er-functions-category-data-collection.md) -luokassa.
3. Valitse **Yhdistämismääritys**-välilehdessä **Raportti\\Rivit** -sarjaelementti.
4. Määritä **Kerätyn tietoavaimen nimi** -lausekkeen arvoksi `WsColumn`.
5. Määritä **Kerätyn tietoavaimen arvo** -lausekkeen arvoksi `WsRow`.

    ![Rivien sarjaelementti Muodon suunnittelija -sivulla](./media/ER-DeferredSequence-Format3.png)

6. Valitse numeerinen **Raportti\\Rivit\\Tietue\\TaxAmount** -elementti.
7. Määritä **Kerätyn tietoavaimen nimi** -lausekkeen arvoksi `SummingAmountKey`.

    ![Numeerinen TaxAmount-elementti Muodon suunnittelija -sivulla](./media/ER-DeferredSequence-Format4.png)

    Voit katsoa tämän asetuksen virtuaalisen laskentataulukon täyttämiseksi, jossa solun A1 arvo lisätään jokaisen käsitellyn verotapahtuman verosumman arvoon.

8. Valitse numeerinen **Raportti\\Rivit\\Tietue\\RunningTotal** -elementti ja sitten **Muokkaa kaava**.
9. Määritä `SUMIF(SummingAmountKey, WsColumn, WsRow)` -lauseke käyttämällä [SUMIF](er-functions-datacollection-sumif.md) ER -toimintoa.
10. Valitse **Tallenna**.

    ![SUMIF-lauseke](./media/ER-DeferredSequence-FormulaDesigner.png)

11. Sulje **Reseptien suunnittelu** -sivu.
12. Valitse ensin **Tallenna** ja sitten **Suorita**.
13. Lataa ja tarkista verkkoselaimen tarjoama tiedosto.

    ![Ladattu tiedosto](./media/ER-DeferredSequence-Run1.png)

    Rivi 21 sisältää kaikille käsitellyille tapahtumille luotua tulosta tietolähteenä käyttäen lasketun veroarvojen juoksevan summan. Tämä tietolähde alkaa raportin alusta ja jatkuu viimeisimpään verotapahtumaan asti. Rivi 22 sisältää kaikkien sellaisten käsiteltyjen tapahtumien veroarvojen summan, jotka on laskettu mallin yhdistämismäärityksessä käyttämällä *GroupBy* -tyypin tietolähdettä. Huomaa, että nämä arvot ovat samat. Siksi voidaan käyttää tulokseen perustuvaa yhteenlaskua **GroupBy**-tyypin käytön sijaan. Vertaamalla rivien 2 ja 21 suoritusaikoja voidaan päätellä, että kaikkien tapahtumarivien luomiseen ja summien laskemiseen kului 9 millisekuntia. Siksi muokattu muoto on noin kaksi kertaa alkuperäistä muotoa nopeampi tietorivien luomisessa ja veroarvojen summien laskemisessa.

14. Valitse numeerinen **Raportti\\Rivit\\Yhteenveto\\TotalTaxAmount** -elementti ja sitten **Muokkaa kaava**.
15. Kirjoita `SUMIF(SummingAmountKey, WsColumn, WsRow)` -lauseke olemassa olevan lausekkeen sijaan.
16. Valitse ensin **Tallenna** ja sitten **Suorita**.
17. Lataa ja tarkista verkkoselaimen tarjoama tiedosto.

    ![Ladattu tiedosto](./media/ER-DeferredSequence-Run2.png)

    Huomaa, että veroarvojen juokseva summa viimeisellä tapahtumatietojen rivillä vastaa nyt yhteenvetorivin summaa.

### <a name="put-values-of-output-based-summing-in-the-report-header"></a>Tulosperusteisten summien laskemisen arvojen määritys raportin otsikossa

Jos sinun on esimerkiksi esitettävä veroarvojen summa raportin otsikossa, voit muokata muotoa.

1. Valitse **Muodon suunnittelija** -sivun **Muoto**-välilehdessä sarjaelementti **Raportti\\Rivit\\Yhteenveto**.
2. Valitse **Siirrä ylös**.
3. Valitse ensin **Tallenna** ja sitten **Suorita**.
4. Lataa ja tarkista verkkoselaimen tarjoama tiedosto.

    ![Ladattu tiedosto](./media/ER-DeferredSequence-Run3.png)

    Huomaa, että yhteenvetorivin 2 veroarvojen summa on nyt 0 (nolla), koska tämä summa lasketaan nyt luodun tuloksen perusteella. Kun rivi 2 luodaan, luotu tulos ei vielä sisällä rivejä, joilla on tapahtumatietoja. Voit määrittää tämän muodon lykkäämään **Raportti\\Rivit\\Yhteenveto** -sarjaelementtiä siihen asti, että **Raportti\\Rivit\\Tietue** -sarjaelementti on suoritettu kaikkien verotapahtumien osalta.

### <a name="defer-the-execution-of-the-summary-sequence-so-that-the-calculated-total-is-used"></a>Yhteenvetosarjan suorittamisen lykkääminen siten, että käytetään laskettua summaa

1. Valitse **Muodon suunnittelija** -sivun **Muoto**-välilehdessä sarjaelementti **Raportti\\Rivit\\Yhteenveto**.
2. Määritä **Lykätty suorittaminen** -asetukseksi **Kyllä**.

    ![Muodon suunnittelija -sivun yhteenvetosarjaelementin lykätyn suorittamisen vaihtoehto](./media/ER-DeferredSequence-Format5.png)

3. Valitse ensin **Tallenna** ja sitten **Suorita**.
4. Lataa ja tarkista verkkoselaimen tarjoama tiedosto.

    ![Ladattu tiedosto](./media/ER-DeferredSequence-Run4.png)

    **Raportti\\Rivit\\Yhteenveto** -sarjaelementti suoritetaan nyt vasta, kun kaikki muut sen pääelementin **Raportti\\Rivit** alaiset kohteet on suoritettu. Siten se suoritetaan sen jälkeen, kun **Raportti\\Rivit\\Tietue** -sarjaelementti on suoritettu kaikkien **model.Data.List** -tietolähteen verotapahtumien osalta. Tämä ilmenee rivien 1, 2 ja 3 ja viimeisen rivin 22 suoritusajoista.

## <a name="additional-resources"></a>Lisäresurssit

- [Määritä muoto suorittamaan laskenta ja summaus](./tasks/er-format-counting-summing-1.md)
- [Sähköisen raportoinnin muodon suorittamisen seuraaminen suorituskykyyn liittyvien ongelmien ratkaisemiseksi](trace-execution-er-troubleshoot-perf.md)
- [ER-muotoisten XML-elementtien suorittamisen lykkäys](er-defer-xml-element.md#Example)
