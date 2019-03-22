---
title: Rivin määrityksen solujen muokkaaminen
description: Tässä ohjeaiheessa käsitellään tietoja, joita talousraportin rivimäärityksen kussakin solussa on oltava ja selitetään, miten nämä tiedot annetaan.
author: ShylaThompson
manager: AnnBe
ms.date: 02/11/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 58881
ms.assetid: 0af492df-a84e-450c-8045-78ef1211abaf
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: d6f6e94fd8e7ddf92e89fedfab09ef0684505819
ms.sourcegitcommit: eb24b63b10c4d06f7550bba9fbd1910ba2719b0a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/12/2019
ms.locfileid: "379661"
---
# <a name="modify-row-definition-cells"></a>Rivin määrityksen solujen muokkaaminen

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa käsitellään tietoja, joita talousraportin rivimäärityksen kussakin solussa on oltava ja selitetään, miten nämä tiedot annetaan.

## <a name="specify-a-row-code-in-a-row-definition"></a>Rivin koodin määrittäminen rivin määrityksessä

Rivien määritysten **Rivin koodi** -solun numerot tai selitteet määrittävät rivin määrityksessä kunkin rivin. Määrittämällä rivikoodin voit viitata tietoihin laskelmissa ja kokonaissummissa.

### <a name="row-code-requirements"></a>Rivikoodivaatimukset

Rivikoodi on pakollinen jokaisella rivillä. Voit yhdistää rivin määrityksessä numeerisia, aakkosnumeerisia ja määrittämättömiä (tyhjiä) rivin koodeja. Rivin koodi voi olla mikä tahansa rivin määrittävä positiivinen kokonaisluku (alle 100 000 000) tai kuvaava selite. Kuvaavan selitteen on noudatettava seuraavia sääntöjä.

- Selitteen alussa on oltava kirjain (a-ö tai A-Ö). Selite voi olla mikä tahansa numeroiden ja kirjainten yhdistelmä, jossa on enintään 16 merkkiä.

    > [!NOTE]
    > Selite voi sisältää alaviivan (\_), mutta muut erikoismerkit eivät ole sallittuja.

- Selitteessä ei voi käyttää seuraavia varattuja sanoja: AND, OR, IF, THEN, ELSE, PERIODS, TO, BASEROW, UNIT, NULL, CPO ja RPO.

Seuraavissa esimerkeissä käytetään kelvollisia rivin koodeja.

- 320
- TL\_NET\_INCOME
- TL\_NET\_94

### <a name="change-a-row-code-in-a-row-definition"></a>Rivin koodin muuttaminen rivin määrityksessä

1. Valitse Report Designerissa **Rivien määritykset** ja avaa sitten muokattava rivin määritys.
2. Syötä uusi arvo sopivalle riville **Rivin koodi** -sarakkeen soluun.

### <a name="reset-numeric-row-codes"></a>Rivin numeeristen koodien nollaaminen

1. Valitse Report Designerissa **Rivien määritykset** ja avaa muokattava rivin määritys.
2. Valitse **Muokkaa**-valikosta **Numeroi rivit uudelleen**.
3. Määritä **Numeroi rivit uudelleen** -valintaikkunassa aloitusrivin koodin ja rivin koodin lisäyksen uudet arvot. Voit nollata rivin numeeriset koodit tasaisin välein olevin arvoin. Report Designer numeroi uudelleen kuitenkin vain ne rivin koodit, jotka alkavat numeroilla (esimerkiksi 130 tai 246). Se ei numeroi uudelleen rivin koodeja, jotka alkavat kirjaimilla (esimerkiksi INCOME\_93 tai TP0693).

> [!NOTE]
> Kun rivin koodeja numeroidaan uudelleen, Report Designer päivittää automaattisesti **TOT**- ja **CAL**-viitteet. Jos esimerkiksi **TOT**-rivi viittaa alueeseen, joka alkaa rivin koodilla 100, ja numeroit uudelleen rivit alkaen arvosta 90, alkavan **TOT**-viitteen arvo 100 muuttuu arvoksi 90.

## <a name="add-a-description"></a>Kuvauksen lisääminen
Kuvauksen solu sisältää raportin rivillä taloushallinnon tietojen kuvauksen, kuten Tuotto tai Nettotuotto. **Kuvaus**-solun teksti näkyy raportissa samanlaisena kuin rivin määritykseen syötetty kuvaus.

> [!NOTE]
> Raportin kuvaussarakkeen leveys määritetään sarakkeen määrityksessä. Jos rivin määrityksen **Kuvaus**-sarakkeen teksti on pitkä, tarkista **DESC**-sarakkeen leveys. Kun käytät **Lisää rivejä kohteesta** -valintaikkunaa, **Kuvaus**-sarakkeen arvot ovat taloushallinnon tietojen segmenttiarvoja tai dimensioarvoja. Lisäämällä rivejä voit lisätä kuvaavan tekstin, esimerkiksi yksikön otsikon tai kokonaissumman, ja voit lisätä muotoilua, esimerkiksi viivan kokonaissummarivin yläpuolelle. Jos raportti sisältää raportointipuun, voit sisällyttää lisätekstin, joka määritetään raportointipuun raportointiyksiköille. Voit myös rajoittaa lisätekstin tietylle raportointiyksikölle.

### <a name="add-the-description-for-a-line-on-a-report"></a>Rivin kuvauksen lisääminen raporttiin

1. Valitse Report Designerissa **Rivien määritykset** ja avaa muokattava rivin määritys.
2. Valitse **Kuvaus**-solu ja syötä sitten raportin rivin nimi.
3. Käytä muotoilua.

### <a name="add-additional-text-from-a-reporting-tree-in-the-description"></a>Lisätekstin lisääminen kuvauksen raportointipuusta

1. Valitse Report Designerissa **Rivien määritykset** ja avaa muokattava rivin määritys.
2. Syötä lisätekstin koodi ja mahdollinen muu teksti soveltuvaan **Kuvaus**-soluun.
3. Käytä muotoilua.

### <a name="limit-the-additional-text-to-a-specific-reporting-unit"></a>Lisätekstin rajoittaminen tietylle raportointiyksikölle

1. Valitse Report Designerissa **Rivien määritykset** ja avaa muokattava rivin määritys.
2. Etsi rivi, jolle lisäteksti luodaan, ja kaksoisnapsauta **Liittyvät kaavat/rivit/yksiköt** -sarakkeen solua.
3. Valitse **Raportointiyksikön valinta** -valintaikkunan **Raportointipuu**-kentässä raportointipuu.
4. Laajenna tai tiivistä raportointipuu **Valitse raportointiyksikkö rajoitukselle** -kentässä ja valitse sitten raportointiyksikkö.

## <a name="add-a-format-code"></a>Muotoilukoodin lisääminen
**Muotoilukoodi**-solun avulla on mahdollisuus valita rivin sisällöksi jonkin esimuotoillun vaihtoehdon. Jos **Muotoilukoodi**-solu on tyhjä, riviä käsitellään taloushallinnon tietojen erittelyrivinä.

> [!NOTE]
> Jos raportti sisältää muotoiltuja muita kuin summarivejä, jotka liittyvät piilotettuihin (esimerkiksi nollasaldoista johtuen) summariveihin, voit estää otsikon ja muotoilurivien tulostamisen **Liittyvät kaavat/rivit/yksiköt** -sarakkeen avulla.

### <a name="add-a-format-code-to-a-report-row"></a>Muotoilukoodin lisääminen raportin riviin

1. Valitse Report Designerissa **Rivien määritykset** ja valitse sitten muokattava rivin määritys.
2. Kaksoisnapsauta **Muotoilukoodi**-solua.
3. Valitse luettelosta muotoilukoodi. Seuraavassa taulukossa esitellään muotoilukoodit ja niiden toiminnot.

    | Muotoilukoodi                   | Muotoilukoodin kuvaus | Toiminto |
    |-------------------------------|-----------------------------------|--------|
    | (Ei mitään)                        |                                   | Tyhjentää **Muotoilukoodi**-solun. |
    | TOT                           | Yhteensä                             | Määrittää rivin, joka käyttää **Liittyvät kaavat/rivit/yksiköt** -sarakkeessa matemaattisia operaattoreita. Yhteensä-koodi sisältää yksinkertaisia operaattoreita, kuten **+** ja **-**. |
    | CAL                           | Laskelma                       | Määrittää rivin, joka käyttää **Liittyvät kaavat/rivit/yksiköt** -sarakkeessa matemaattisia operaattoreita. Laskelmat sisältävät monimutkaisia operaattoreita, kuten **+**, **-**, **\***, **/** ja **IF/THEN/ELSE** -lausekkeet. |
    | DES                           | kuvaus                       | Määrittää raportin otsikkorivin tai tyhjän rivin. |
    | LFT RGT CEN                   | Vasen, Oikea, Keskitys                 | Tasaa rivin kuvaustekstin raporttisivulla tekstin sarakkeen määrityksessä olevasta sijoittelusta huolimatta. |
    | CBR                           | Vaihda perusrivi                   | Määrittää rivin, joka määrittää sarakkeiden laskelmien perusrivin. |
    | COLUMN                        | Sarakkeen vaihto                      | Aloittaa raportin uuden sarakkeen. |
    | PAGE                          | Sivunvaihto                        | Aloittaa raportin uuden sivun. |
    | \---                          | Yksinkertainen alleviivaus                  | Alleviivaa raportin kaikkien summasarakkeiden rivin yhdellä viivalla. |
    | ===                           | Kaksoisalleviivaus                  | Alleviivaa raportin kaikkien summasarakkeiden rivin kaksoisviivalla. |
    | LINE1                         | Ohut viiva                         | Piirtää sivulle ohuen viivan. |
    | VIIVA2                         | Paksu viiva                        | Piirtää sivun poikki yhden paksun viivan. |
    | VIIVA3                         | Pisteviiva                       | Piirtää sivulle pisteviivan. |
    | LINE4                         | Paksu ja ohut viiva          | Piirtää sivulle kaksoisviivan. Ylempi viiva on paksu ja alempi ohut. |
    | LINE5                         | Ohut ja paksu viiva          | Piirtää sivulle kaksoisviivan. Ylempi viiva on ohut ja alempi paksu. |
    | BXB BXC                       | Kehystetty rivi                         | Piirtää raportin rivin ympärille ruudun, joka alkaa **BXB**-riviltä ja päättyy **BXC**-riville. |
    | HUOM                           | Huomautus                            | Määrittää rivin, joka on kommenttirivi ja jota ei tulosteta raporttiin. Huomautusrivillä voidaan esimerkiksi selittää muotoilutapoja. |
    | SORT ASORT SORTDESC ASORTDESC | Lajittele                              | Lajittelee kulut ja tuotot, toteutuneen tai budjetin varianssin raportin suurimman varianssin mukaan tai rivin kuvaukset aakkosjärjestykseen. |

## <a name="specify-related-formulasrowsunits"></a>Liittyvien kaavojen/rivien/yksiköiden määrittäminen
**Liittyvät kaavat/rivit/yksiköt** -solulla on useita tarkoituksia. Rivityypistä riippuen **Liittyvät kaavat/rivit/yksiköt** -solu voi suorittaa jonkin seuraavista toiminnoista:

- Laskelmaan sisällytettävien rivien määritys, kun käytössä on **TOT**- tai **CAL**-muotoilukoodi.
- Muotoilurivin linkittäminen summariviin niin, että muotoilu tulostetaan vain, kun liitetty summa tulostetaan.
- Rivin rajoittaminen tiettyyn raportointiyksikköön.
- Laskelmien perusrivin määrittäminen, kun käytössä on **BASEROW**-muotoilukoodi.
- Rivien määrittäminen lajittelua varten silloin, kun lajittelun muotoilukoodit ovat käytössä.

### <a name="use-a-row-total-in-a-row-definition"></a>Rivin summan käyttäminen rivin määrityksessä

Käytä rivin summakaavaa muiden rivien summien lisäämisessä tai vähentämisessä. Rivin summan luonnissa käytettävä kaava voi sisältää operaattorin + ja -, kun yksittäisiä rivin koodeja ja alueita yhdistetään. Alueet osoitetaan kaksoispisteellä (:). Kaava voi sisältää enintään 1 024 merkkiä. Vakiosummakaavan esimerkki: 400+420+430+450+460LIABILITIES+EQUITY520:546520:546-LIABILITIES

### <a name="components-of-a-row-total-formula"></a>Rivisummakaavan osat

Kun luot rivisummakaavan, sinun on määritettävä rivikoodien avulla, mitä rivejä lisäät tai vähennät nykyisessä rivimäärityksessä. Määritä operaattorien avulla, miten rivit yhdistetään. Kokonaissumma- ja summarivejä voi käyttää missä tahansa yhdistelmässä.

> [!NOTE]
> Kaikki alueen sisällä olevat kokonaissummarivit jätetään pois. Voit luoda kokonaissumman määrittämällä rivialueen. Jos alueen ensimmäinen rivi on kokonaissummarivi, se sisällytetään uuteen summaan. Seuraavassa taulukossa kerrotaan, miten operaattoreita käytetään rivin summakaavoissa.

| Operaattori | Esimerkkikaava | kuvaus                                                 |
|----------|-----------------|-------------------------------------------------------------|
| +        | 100+330         | Lisää rivin 100 summan rivin 330 summaan.        |
| :        | 100:330         | Laskee kaikki rivien 100–330 summat yhteen.    |
| -        | 100-330         | Vähentää rivin 100 summan rivin 330 summasta. |

### <a name="create-a-row-total"></a>Rivisumman luominen

1. Valitse raporttien suunnitteluohjelmassa **Rivimääritykset** ja avaa sitten muokattava rivimääritys.
2. Kaksoisnapsauta rivin määrityksen **Muotoilukoodi**-solua ja valitse **TOT**.
3. Syötä summakaava **Liittyvät kaavat/rivit/yksiköt** -soluun.

### <a name="relate-a-format-row-to-an-amount-row"></a>Muotoilurivin liittäminen summariviin

Rivin määrityksen **Muotoilukoodi**-sarakkeessa muotoilukoodit **DES**-, **LFT**-, **RGT**-, **CEN**-, **---** ja **===** kohdistavat muotoilun muihin kuin summariveihin. Voit estää muotoilua tulostumasta silloin, kun liittyvät summarivit on piilotettu (esimerkiksi jos summarivit sisältävät nolla-arvoja tai kaudella ei ole toimintaa), liitä muotoilurivit vastaaviin summariveihin. Tämä toiminto on hyödyllinen, kun halutaan estää välisummiin liittyvien otsikoiden tai muotoilun tulostuminen silloin, kun kauteen ei liity tulostettavia tietoja.

> [!NOTE]
> Voit estää myös yksityiskohtaisten summarivien tulostamisen tyhjentämällä niiden rivien näyttövalinnan, jotka eivät sisällä summia. Tämä vaihtoehto sijaitsee raportin määrityksen **Asetukset**-välilehdessä. Oletusarvoisesti raporteissa piilotetaan ne tapahtumatietojen tilit, joilla on nollasaldo tai joilla ei ole toimintaa kaudella. Saat nämä tapahtumatietojen tilit näkyviin valitsemalla raportin määrityksessä **Asetukset**-välilehden **Näytä rivit, joilla ei ole summia** -valintaruudun.

### <a name="relate-a-format-row-to-an-amount-row"></a>Muotoilurivin liittäminen summariviin

1. Valitse Report Designerissa **Rivien määritykset** ja valitse sitten muokattava rivin määritys.
2. Syötä **Liittyvät kaavat/rivit/yksiköt** -solun muotoiluriville piilotettavan summarivin koodi.

    > [!NOTE]
    > Jos haluat estää summarivin, rivin saldon on oltava 0 (nolla). Summariviä, jolla on saldo, ei piiloteta.

3. Valitse **Tiedosto**-valikosta **Tallenna**.

### <a name="example-of-preventing-printing-of-rows"></a>Esimerkki rivien tulostamisen estämisestä

Seuraavassa esimerkissä Paula haluaa estää raportin **Käteinen yhteensä** -rivin otsikon ja alleviivausten tulostamisen, koska kummallakaan käteistilillä ei ole ollut toimintaa. Tämän vuoksi Paula syöttää rivin 220 (joka on muotoilurivi, kuten muotoilukoodi **---** osoittaa) **Liittyvät kaavat/rivit/yksiköt** -soluun **250**, joka on sen summarivin koodi, jonka hän haluaa piilottaa.

[![RelatedRowsRowDefinition](./media/relatedrowsrowdefinition-1024x144.png)](./media/relatedrowsrowdefinition.png)

## <a name="select-the-base-row-for-a-column-calculation"></a>Sarakelaskelman perusrivin valitseminen
Suhteellisessa raportoinnissa rivin määritykseen liitetään yksi perusrivi tai useita perusrivejä **CBR** (vaihda perusrivi) -muotoilukoodin avulla. Tämän jälkeen perusriviin viitataan sarakkeen määrityksen laskelmassa. Seuraavassa on joitakin tavallisia esimerkkejä CBR-laskelmista:

- kokonaistuoton prosenttiosuus, kun se liittyy yksittäisiin tuottonimikkeisiin
- kokonaiskulujen prosenttiosuus, kun ne liittyvät yksittäisiin kulunimikkeisiin
- käyttökatteen prosenttiosuus, kun se liittyy jaoston tai osaston tietoihin.

Rivin määrityksessä määritetään vähintään yksi perusrivi. Sarakkeen määrityksessä määritetään suhde, jolle perusrivi raportoidaan. Sarakekaavassa käytettävä koodi on **BASEROW**. **BASEROW**-koodin kanssa käytetään seuraavia matemaattisia perusoperaattoreita: jakolasku, kertolasku, lisäys ja vähennys. Useimmiten **BASEROW**-koodin kanssa käytettävä toiminto on jakolasku, jonka tulos näytetään prosenttilukuna. **BASEROW**-koodia kaavassa käyttävät sarakelaskelmat käyttävät liittyvän perusrivin koodien rivin määritystä. **CBR**-riveillä on seuraavat ominaisuudet:

- **CBR**-rivejä ei tulosteta valmiiseen raporttiin.
- **CBR**-muotoilukoodi ja sen liittyvä rivin koodi sijoitetaan rivin tai liittyvät laskelmat näyttävän osan yläpuolelle.

Sarakemäärityksessä **LASK**-saraketyypillä määritetään sarake, joka määrittää **Kaava**-rivin kaavan. Tämä kaava käsittelee kyseisen sarakkeen tietoja raportissa. Se käyttää Baserow (perusrivi) -avainsanaa rivin **CBR**-muotoilukoodien laskelmien perustana. Rivin määrityksen **CBR**-muotoilukoodi määrittää niiden sarakkeiden perusrivin, jotka laskevat prosenttiosuuden tai kertovat kunkin raportin rivin perusrivillä. Rivimuotoilussa voi olla useita **CBR**-muotoilukoodeja esimerkiksi nettomyyntiä, bruttomyyntiä ja kokonaiskuluja varten. Yleensä **CBR**-muotoilukoodia käytetään kokonaissummariviin vertailtavien tilien prosenttiosuuden luomisessa. Perusriviä käytetään kaikissa laskelmissa siihen asti, kunnes toinen perusrivi määritetään. Määritä aloittava **CBR**-muotoilukoodi ja lopettava **CBR**-muotoilukoodi. Voit määrittää esimerkiksi kulut nettomyynnin prosenttiosuutena jakamalla arvon kullekin kuluriville nettomyyntirivin arvon perusteella. Tässä tapauksessa nettomyyntirivi on perusrivi. Voit määrittää nykyiset ja vuoden alusta saadut tulokset raportoivan sarakkeen määrityksen yhdessä kunkin tuloksen perusprosentin kanssa seuraavassa esimerkissä osoitetulla tavalla. Aloita yksityiskohtaisen tuloslaskelman määrittämisellä.

### <a name="select-the-base-row-in-a-row-definition-for-a-column-calculation"></a>Rivin määrityksen perusrivin valitseminen sarakelaskelmaa varten

1. Valitse Report Designer -ohjelmassa **Sarakkeiden määritykset** ja avaa tuloslaskelman sarakkeen määritys.
2. Lisää sarakkeen määritykseen uusi sarake ja määritä sarakelajiksi **CALC**.
3. Syötä uuden sarakkeen **Kaava**-soluun **X/BASEROW**-kaava, jossa **X** on **FD**-sarakelaji, joka näyttää prosenttiosuuden.
4. Kaksoisnapsauta **Muotoilu / valuutan ohitus** -solua.
5. Valitse **Muotoilun ohitus** -valintaikkunan **Muotoiluluokka**-luettelosta **Prosentti** ja valitse sitten **OK**.
6. Valitse **Tiedosto**-valikosta **Tallenna nimellä**, kun haluat tallentaa sarakkeen määrityksen uudella nimellä. Liitä **CBR** nykyiseen tiedostonimeen (esimerkiksi **CUR\_YTD\_CBR**). Tämä sarakkeen määritys on perusrivin sarakkeen määritys.
7. Valitse Report Designer -ohjelmassa **Rivien määritykset** ja avaa rivin määritys, kun muokkaus tehdään perusrivin laskelman avulla.
8. Lisää uusi rivi sen rivin yläpuolelle, jolta perusrivin laskelma alkaa.
9. Kaksoisnapsauta rivin määrityksen **Muotoilukoodi**-solua ja valitse **CBR**.
10. Syötä **Liittyvät kaavat/rivit/yksiköt** -soluun perusrivin koodin numero.

### <a name="example-of-base-row-calculation"></a>Esimerkki perusrivin laskelmasta

Seuraavassa rivin määrityksen esimerkissä rivi 100 osoittaa, että laskelmien perusrivi on rivi 280.

[![Esimerkki perusrivin laskelmasta](./media/cbrrowdefinition.png)](./media/cbrrowdefinition.png)

Seuraavassa sarakkeen määrityksessä laskelmat käyttävät **CBR**-muotoilukoodia. Sarakkeen C laskelmassa jaetaan raportin sarake B sarakkeen B rivin 280 arvolla. Sarakkeen B muotoilun ohitus tulostaa laskelman tuloksen prosenttiosuutena. Samaan tapaan jokainen sarakkeen E summa on sarakkeen D summa nettomyynnin prosenttiosuutena.

[![Sarakkeen määrityksen esimerkki.](./media/cbrcolumndefinition2.png)](./media/cbrcolumndefinition2.png)

Seuraava esimerkki sisältää edellisten laskelmien perusteella luotavan raportin.

[![Esimerkkiraportti, joka perustuu edellisen esimerkin laskelmin.](./media/cbrreport-1024x272.png)](./media/cbrreport.png)

## <a name="select-a-sorting-code-for-a-row-definition"></a>Rivin määrityksen lajittelukoodin valitseminen
Lajittelukoodit lajittelevat tilit tai arvot, toteutuneen tai budjetin varianssin raportin suurimman varianssin mukaan tai rivin kuvaukset aakkosjärjestykseen. Käytettävissä olevat lajittelukoodit ovat seuraavat:

- **SORT** – Lajittelee raportin nousevaan järjestykseen määritetyn sarakkeen arvojen perusteella.
- **ASORT** – Lajittelee raportin nousevaan järjestykseen määritetyn sarakkeen arvojen absoluuttisen arvon perusteella. Toisin sanoen kunkin arvon etumerkki ohitetaan arvojen lajittelun yhteydessä. Tämä muotoilukoodi järjestää arvot varianssin suuruuden mukaan siitä huolimatta, onko varianssi positiivinen vai negatiivinen.
- **SORTDESC** – Lajittelee raportin laskevaan järjestykseen määritetyn sarakkeen arvojen perusteella.
- **ASORTDESC** – Lajittelee raportin laskevaan järjestykseen määritetyn sarakkeen arvojen absoluuttisen arvon perusteella.

### <a name="select-a-sorting-code"></a>Lajittelukoodin valitseminen

1. Valitse Report Designerissa **Rivien määritykset** ja avaa muokattava rivin määritys.
2. Kaksoisnapsauta **Muotoilukoodi** -solua ja valitse sitten lajittelukoodi.
3. Määritä **Liittyvät kaavat/rivit/yksiköt** -soluun lajiteltavien rivien koodien alue. Voit määrittää alueen syöttämällä ensimmäisen rivin koodin, kaksoispisteen (:) ja lopuksi viimeisen rivin koodin. Voit syöttää esimerkiksi **160:490**-arvon, kun alue on rivistä 160 riviin 490.
4. Syötä **Sarakkeen rajoitus** -soluun lajittelussa käytettävän raporttisarakkeen kirjain.

    > [!NOTE]
    > Ota lajittelun laskelmaan mukaan vain summarivit.

### <a name="examples-of-ascending-and-descending-column-values"></a>Esimerkkejä nousevista ja laskevista sarakearvoista

Seuraavassa esimerkissä raportin sarakkeen D arvot lajitellaan nousevassa järjestyksessä riveille 160–490. Lisäksi lajitellaan raportin sarakkeen G absoluuttiset arvot laskevassa järjestyksessä riveille 610–940.

| Rivin koodi | Kuvaus                                         | Muotoilukoodi | Liittyvät kaavat/rivit/yksiköt | Normaalisaldo | Sarakerajoitus | Linkki taloushallinnon dimensioihin |
|----------|-----------------------------------------------------|-------------|-----------------------------|----------------|--------------------|------------------------------|
| 100      | Lajitteluperuste kuukauden varianssi nousevassa järjestyksessä       | DES         |                             |                |                    |                              |
| 130      |                                                     | SORT        | 160:490                     |                | D                  |                              |
| 160      | Myynti                                               |             |                             | C              |                    | 4100                         |
| 190      | Myyntipalautukset                                       |             |                             |                |                    | 4110                         |
|          | ...                                                 |             |                             |                |                    |                              |
| 490      | Korkotulot                                     |             |                             | C              |                    | 7000                         |
| 520      |                                                     | DES         |                             |                |                    |                              |
| 550      | Lajitteluperuste absoluuttinen varianssi vuoden alusta laskevassa järjestyksessä | DES         |                             |                |                    |                              |
| 580      |                                                     | ASORTDESC   | 610:940                     |                | G                  |                              |
| 610      | Myynti                                               |             |                             | Y              |                    | 4100                         |
| 640      | Myyntipalautukset                                       |             |                             |                |                    | 4110                         |
|          | ...                                                 |             |                             |                |                    |                              |
| 940      | Korkotulot                                     |             |                             | Y              |                    | 7000                         |


## <a name="specify-a-format-override-cell"></a>Muotoilun ohitus -solun määrittäminen
**Muotoilun ohitus** -solu määrittä muotoilun, jota rivillä käytetään raportin tulostuksen yhteydessä. Tämä muotoilu korvaa sarakkeen ja raportin määrityksessä määritetyn muotoilun. Oletusarvoisesti näissä määrityksissä määritetty muotoilu on valuutta. Jos raportin jokin rivi sisältää käyttöomaisuuserien määrän, kuten rakennusten määrän, ja toinen rivi kyseisten käyttöomaisuuserien rahamääräisen arvon, voit ohittaa valuutan muotoilun ja syöttää rakennusten määrän sisältävälle riville numeerisen muotoilun. Voit määrittää nämä tiedot **Muotoilun ohitus** -valintaikkunassa. Käytettävissä olevat vaihtoehdot riippuvat valitusta muotoiluluokasta. Valintaikkunan **Malli**-alue sisältää esimerkkimuotoiluja. Käytettävissä ovat seuraavat muotoiluluokat:

- Valuutan muotoileminen
- Numeerinen muotoileminen
- Prosenttiosuuden muotoileminen
- Mukautettu muotoilu

### <a name="override-cell-formatting"></a>Solun muotoilemisen ohittaminen

1. Avaa Report Designer -ohjelmassa muokattava rivin määritys.
2. Kaksoisnapsauta ohitettavan muotoilun sisältävän rivin **Muotoilun ohitus** -sarakkeen solua.
3. Valitse **Muotoilun ohitus** -valintaikkunassa raportin kyseisellä rivillä käytettävät muotoiluasetukset.
4. Napsauta **OK**.

### <a name="currency-formatting"></a>Valuutan muotoileminen

Valuutan muotoileminen koskee tilikauden summaa. Se sisältää valuuttasymbolin. Käytettävissä ovat seuraavat asetukset:

- **Valuuttasymboli** – raportin valuuttasymboli. Tämä arvo ohittaa yrityksen tietojen **Alueelliset asetukset** -asetuksen.
- **Negatiiviset luvut** – negatiivisilla luvuilla on miinusmerkki (-) ja ne näkyvät suluissa tai niihin on liitetty kolmio (∆).
- **Desimaalit** – desimaalipilkun jälkeen näytettävien desimaalien määrä.
- **Nolla-arvon ohituksen teksti** – Teksti, joka sisällytetään raporttiin, kun summa on 0 (nolla). Teksti näkyy **Malli**-alueen viimeisellä rivillä.

    > [!NOTE]
    > Jos tulostus on poistettu käytöstä nolla-arvojen kohdalla tai niiltä kausilta, joilla ei ole toimintaa, tämä teksti piilotetaan.

### <a name="numeric-formatting"></a>Numeerinen muotoileminen

Numeerinen muotoileminen koskee mitä tahansa summaa. Se ei sisällä valuuttasymbolia. Valittavissa ovat seuraavat vaihtoehdot:

- **Negatiiviset luvut** – negatiivisilla luvuilla on miinusmerkki (-) ja ne näkyvät suluissa tai niihin on liitetty kolmio (∆).
- **Desimaalit** – desimaalipilkun jälkeen näytettävien desimaalien määrä.
- **Nolla-arvon ohituksen teksti** – Teksti, joka sisällytetään raporttiin, kun summa on 0 (nolla). Teksti näkyy **Malli**-alueen viimeisellä rivillä.

    > [!NOTE]
    > Jos tulostus on poistettu käytöstä nolla-arvojen kohdalla tai niiltä kausilta, joilla ei ole toimintaa, tämä teksti piilotetaan.

### <a name="percentage-formatting"></a>Prosenttiosuuden muotoileminen

Prosenttiosuuden muotoileminen sisältää prosenttimerkin (%). Valittavissa ovat seuraavat vaihtoehdot:

- **Negatiiviset luvut** – negatiivisilla luvuilla on miinusmerkki (-) ja ne näkyvät suluissa tai niihin on liitetty kolmio (∆).
- **Desimaalit** – desimaalipilkun jälkeen näytettävien desimaalien määrä.
- **Nolla-arvon ohituksen teksti** – Teksti, joka sisällytetään raporttiin, kun summa on 0 (nolla). Teksti näkyy **Malli**-alueen viimeisellä rivillä.

    > [!NOTE]
    > Jos tulostus on poistettu käytöstä nolla-arvojen kohdalla tai niiltä kausilta, joilla ei ole toimintaa, tämä teksti piilotetaan.

### <a name="custom-formatting"></a>Mukautettu muotoileminen

Luo mukautettu muotoilun ohitus mukautetun muotoiluluokan avulla. Valittavissa ovat seuraavat vaihtoehdot:

- **Tyyppi** – mukautettu muotoilu.
- **Nolla-arvon ohituksen teksti** – Teksti, joka sisällytetään raporttiin, kun summa on 0 (nolla). Teksti näkyy **Malli**-alueen viimeisellä rivillä.

    > [!NOTE]
    > Jos tulostus on poistettu käytöstä nolla-arvojen kohdalla tai niiltä kausilta, joilla ei ole toimintaa, tämä teksti piilotetaan.

Tyyppi edustaa positiivista ja negatiivista arvoa. Yleensä syötetään samanlainen muoto, joka erottelee positiiviset ja negatiiviset arvot. Kun haluat määrittää esimerkiksi, että positiivisilla ja negatiivisilla arvoilla on kaksi desimaalia, mutta negatiiviset arvot näkyvät suluissa, syötä **0.00;(0.00)**. Seuraavassa taulukossa ovat mukautetut muodot, joiden avulla arvojen muotoja hallitaan. Kaikki esimerkit alkavat arvosta 1234,56.

| Muoto                         | Positiivinen   | Negatiivinen     | Nolla    |
|--------------------------------|------------|--------------|---------|
| 0                              | 1235       | -1235        | 0       |
| 0;0                            | 1235       | 1235         | 0       |
| 0;(0);-                        | 1235       | 1235         | -       |
| \#,\#\#\#;(\#,\#\#\#);""       | 1 235      | (1 235)      | (Tyhjä) |
| \#,\#\#0.00;(\#,\#\#0.00);nolla | 1 234,56   | (1 234,56)   | nolla    |
| 0.00%;(0.00%)                  | 123456.00% | (123456.00%) | 0.00%   |

## <a name="specify-a-normal-balance-cell"></a>Normaali saldo -solun määrittäminen
Rivin määrityksen **Normaali saldo** -solu ohjaa rivin summien etumerkin käyttämistä. Voit vaihtaa rivin etumerkin syöttämällä kyseisen rivin **Normaali saldo** -soluun **C**. Tee näin myös silloin, kun tilin normaali saldo on kredit. Raportin suunnitteluohjelma vaihtaa rivin kaikkien kreditsaldojen tilien etumerkin. Kun Report Designer muuntaa nämä tilit, se poistaa debet/kredit-ominaisuuden kaikilta summilta. Tämän vuoksi summaus on helppoa. Jos haluat laskea esimerkiksi nettotuoton, kulut vähennetään tuotosta. Yleensä **C**-koodi ei vaikuta summattuihin ja laskettuihin riveihin. Sarakkeen määrityksen **XCR**-tulostuksenohjaus kuitenkin vaihtaa minkä tahansa rivin etumerkin, joka sisältää **Normaali saldo** -sarakkeessa **C**-arvon. Tämä muotoilu on tärkeää erityisesti silloin, kun kaikki kielteiset varianssit halutaan näyttää negatiivisina summina. Jos summatun tai lasketun numeron etumerkki on väärä, syötä rivin **Normaali saldo** -soluun **C**, jolloin merkki vaihdetaan.

## <a name="specify-a-row-modifier-cell"></a>Rivimääre-solun määrittäminen
Rivin määrityksen **Rivimääre**-solun sisältö ohittaa kyseisen rivin tilikaudet, jaksot ja muut sarakkeen määrityksessä määritetyt tiedot. Valittua määrettä käytetään rivin jokaisella tilillä. Voit muokata kutakin riviä käyttämällä yhtä tai useaa seuraavaa määretyyppiä:

- Tilimääreet
- Kirjakoodimääreet
- Tili- ja tapahtumamääritteet

### <a name="override-a-column-definition"></a>Sarakkeen määrityksen ohitus

1. Avaa Report Designer -ohjelmassa muokattava rivin määritys.
2. Kaksoisnapsauta ohitettavan sarakkeen määrityksen sisältävällä rivillä **Rivimääre**-solua.
3. Valitse **Rivimääre**-valintaikkunan **Tilimääre**-kenttään vaihtoehto. Lisätietoja vaihtoehdoista on Tilimääre-osassa.
4. Valitse **Kirjakoodimääre**-kentässä rivillä käytettävä kirjakoodi.
5. Lisää **Määritteet**-kohtaan kunkin rivin koodiin sisällytettävän määritteen syöttö näiden vaiheiden mukaan:

    1. Kaksoisnapsauta **Määrite**-solua ja valitse määritteen nimi.

        > [!IMPORTANT]
        > Voit korvata ristikkomerkin (\#) numeerisella arvolla.

    2. Kaksoisnapsauta **Mistä**-solua ja syötä alueen ensimmäinen arvo.
    3. Kaksoisnapsauta **Mihin**-solua ja syötä alueen viimeinen arvo.

6. Napsauta **OK**.

### <a name="account-modifiers"></a>Tilimääreet

Kun valitset tietyn tilin, Report Designer yleensä yhdistää tilin ja tilikaudet, jaksot ja muut sarakkeen määrityksessä määritetyt tiedot. Voit käyttää eri riveillä erilaisia tietoja, kuten eri tilikausia. Seuraavassa taulukossa näkyvät käytettävissä olevat tilimääreet. Korvaa numeromerkki (\#) arvolla, joka on sama tai pienempi kuin tilikauden jaksojen määrä.

| Tilimääre | Tulostettavat tiedot                                                                           |
|------------------|-------------------------------------------------------------------------------------------|
| /BB              | Tilin alkusaldo.                                                     |
| /\#              | Määritetyn kauden saldo.                                                     |
| /-\#             | Kauden saldo, joka on \# kautta ennen kuluvaa kautta.                  |
| /+\#             | Kauden saldo, joka on \# kautta kuluvan kauden jälkeen.                   |
| /C               | Kuluvan kauden saldo.                                                       |
| /C-\#            | Kauden saldo, joka on \# kautta ennen kuluvaa kautta.                  |
| /C+\#            | Kauden saldo, joka on \# kautta kuluvan kauden jälkeen.                   |
| /Y               | Kuluvan kauden saldo vuoden alusta.                                      |
| /Y-\#            | Sen kauden saldo vuoden alusta, joka on \# kautta ennen nykyistä kautta. |
| /Y+\#            | Sen kauden saldo vuoden alusta, joka on \# kautta nykyisen kauden jälkeen.  |

### <a name="book-code-modifiers"></a>Kirjakoodimääreet

Voit rajoittaa rivin aiemmin luotua kirjakoodia varten. Sarakkeen määrityksessä on oltava vähintään yksi kirjakoodin sisältävä **FD**-sarake.

> [!NOTE]
> Rivin kirjakoodin rajoitus ohittaa kyseisen rivin sarakkeen määrityksen kirjakoodin rajoitukset.

### <a name="account-and-transaction-attributes"></a>tili- ja tapahtumamääritteet.

Joissakin kirjanpitojärjestelmissä tuetaan taloushallinnon tietojen tili- ja tapahtumamääritteitä. Nämä määritteet toimivat kuten virtuaaliset tilisegmentit. Ne voivat sisältää tiliä tai tapahtumaa koskevia lisätietoja. Lisätiedot voivat olla tilien tunnuksia, erien tunnuksia, postinumeroita tai muita määritteitä. Jos käytössä oleva kirjanpitojärjestelmä tukee määritteitä, voit käyttää tili- tai tapahtumamääritteitä rivin määrityksen rivimääreinä. Lisätietoja rivin tietojen ohituksesta on Sarakkeen määrityksen ohitus -osassa, joka löytyy tämän artikkelin alkuosasta.

## <a name="specify-a-link-to-financial-dimensions-cell"></a>Linkin määrittäminen Taloushallinnon dimensiot -soluun
**Linkki taloushallinnon dimensioihin** -solu sisältää linkin raportin jokaiselle riville sisällytettäviin taloushallinnon tietoihin. Tämä solu sisältää dimensioarvot. Voit avata **Dimensiont**-valintaikkunan kaksoisnapsauttamalla **Linkki taloushallinnon dimensioihin** -solua.

> [!NOTE]
> Raporttien suunnitteluohjelma ei voi valita Microsoft Dynamics ERP -järjestelmästä niitä tilejä, dimensioita tai kenttiä, jotka sisältävät seuraavat varatut merkit: &, \*, \[, \], {, tai }. Voit määrittää rivimääritykseen jo lisätyn rivin tiedot lisäämällä tiedot **Linkki taloushallinnon dimensioihin** -soluun. Voit lisätä taloushallinnon tietoihin linkittyviä uusia rivejä **Lisää rivit kohteesta** -valintaikkunassa luomalla uusia rivejä raportin määrityksessä. Sarakkeen otsikko muuttuu sen mukaan, miten sarake on konfiguroitu, seuraavassa taulukossa esitetyllä tavalla.

| Valitun linkin tyyppi       | Kuvaus, jollaiseksi Linkki-sarakkeen kuvaus muuttuu |
|----------------------------------|----------------------------------------------------|
| Taloushallinnon dimensiot             | Linkki taloushallinnon dimensioihin                       |
| Raportin laskentataulukko                 | Taloushallinnon raportti                         |

### <a name="specify-a-dimension-or-range"></a>Dimension tai alueen määrittäminen

1. Avaa raporttien suunnitteluohjelmassa rivimääritys, jota haluat muokata.
2. Kaksoisnapsauta **Linkki taloushallinnon dimensioihin** -sarakkeen solua.
3. Kaksoisnapsauta **Dimensiot**-valintaikkunassa dimension nimen alapuolella olevaa solua.
4. Valitse dimension valintaikkunassa **Yksittäinen tai alue**.
5. Syötä **Mistä**-kenttään aloittava dimensio tai hae käytettävissä olevat dimensiot valitsemalla ![Selaa](https://i-technet.sec.s-msft.com/dynimg/IC679490.gif "Selaa"). Voit syöttää dimensioalueen syöttämällä lopettavan dimension **Mihin**-kenttään.
6. Sulje dimension valintaikkuna valitsemalla **OK**. **Dimensiont**-valintaikkunassa näkyy päivitetty dimensio tai alue.
7. Sulje **Dimensiot**-valintaikkuna valitsemalla **OK**.

## <a name="display-zero-balance-accounts-in-a-row-definition"></a>Nollasaldotilien näyttäminen rivin määrityksessä
Oletusarvoisesti Report Designer ei tulosta rivejä, joilla ei ole vastaavaa saldoa taloushallinnon tiedoissa. Tämän vuoksi voit luoda yhden rivin määrityksen, joka sisältää kaikki luonnollisen segmentin arvot tai dimensioarvot, ja käyttää tätä rivin määritystä millä tahansa osastolla.

### <a name="modify-zero-balance-settings"></a>Nollasaldoasetusten muokkaaminen

1. Avaa Report Designer -ohjelmassa muokattava raportin määritys.
2. Valitse **Muu muotoilu** -kohdan **Asetukset**-välilehdessä rivin määrityksen ne asetukset, joita käytetään raportin määrityksessä.
3. Tallenna muutokset valitsemalla **Tiedosto**-valikosta **Tallenna**.

## <a name="use-wildcard-characters-and-ranges-in-a-row-definition"></a>Yleismerkkien ja alueiden käyttäminen rivin määrityksessä
Jos haluat syöttää luonnollisen segmentin arvon **Dimensiot**-valintaikkunaan, voit syöttää mihin tahansa segmentin kohtaan yleismerkin (? tai \*). Raportin suunnitteluohjelma poimii määritettyjen sijaintien arvot, eikä ota yleismerkkejä huomioon. Tässä esimerkissä rivin määritys sisältää vain luonnollisen segmentin arvoja. Luonnollisilla segmenteillä on neljä merkkiä. Jos annat arvoksi **6???** Report Designer ottaa huomioon kaikki tilit, joiden luonnollisen segmentin arvo alkaa numerolla 6. Jos annat arvoksi **6\***, palautettavat tulokset ovat samat, mutta tulokset voivat sisältää myös muun pituisia arvoja, kuten **60** ja **600000** Report Designer korvaa kunkin yleismerkin (?) arvoilla, jotka voivat sisältää sekä kirjaimia että erikoismerkkejä. Jos alueeksi määritetään **12?0**–**12?4**, **12?0**-arvon yleismerkki korvataan merkistön alimmalla arvolla ja **12?4**-arvon yleismerkki merkistön korkeimmalla arvolla.

> [!NOTE]
> Vältä yleismerkkien käyttämistä alueiden aloitus- ja lopetustileissä. Jos aloitus- tai lopetustilissä käytetään yleismerkkiä, tulokset voivat olla odottamattomia.

### <a name="single-segment-or-single-dimension-ranges"></a>Yhden segmentin tai yhden dimension alueet

Voit määrittää segmentti- tai dimensioarvoille alueen. Jos alue määritetään, rivin määritystä ei tarvitse päivittää aina, kun taloushallinnon tietoihin lisätään uusi segmentti- tai dimensioarvo. Esimerkiksi alue **+tili=\[6100:6900\]** noutaa rivin summaan arvot tileiltä 6100–6900. Kun alue sisältää yleismerkin (?), Report Designer ei arvioi aluetta merkkiperusteisesti. Sen sijaan määritetään alueen alku ja loppu, jonka jälkeen loppuarvot ja kaikki niiden väliset arvot sisällytetään arviointiin.

> [!NOTE]
> Raporttien suunnitteluohjelma ei voi valita Microsoft Dynamics ERP -järjestelmästä niitä tilejä, dimensioita tai kenttiä, jotka sisältävät seuraavat varatut merkit: &, \*, \[, \], {, tai }. Voit lisätä et-merkin (&) vain silloin, kun rivin määritykset muodostetaan automaattisesti **Lisää rivejä dimensioista** -valintaikkunan avulla.

### <a name="multiple-segment-or-multiple-dimension-ranges"></a>Useiden segmenttien tai useiden dimensioiden alueita

Kun alue syötetään useiden dimensioarvojen yhdistelmien avulla, alueen vertailu tehdään dimensioperusteisesti (..\\financial-dimensions\\dimension-by-dimension). Alueen vertailua ei voi tehdä merkkiperusteisesti tai osittaisen segmentin perusteella. Esimerkiksi alue **+tili=\[5000:6000\], osasto=\[1000:2000\], kustannuspaikka=\[00\]** sisältää vain kutakin segmenttiä vastaavat rivit. Tässä skenaariossa ensimmäisen dimension alueen on oltava 5000–6000, toisen dimension alueen 1000–2000 ja viimeisen dimension alueen 00. Esimerkiksi **+tili=\[5100\], osasto=\[1100\], kustannuspaikka=\[01\]** ei oteta mukaan raporttiin, koska viimeinen segmentti ei kuulu määritettyyn alueeseen. Jos segmentin arvo sisältää välilyöntejä, käytä arvossa hakasulkeita (\[ \]). Seuraavat arvot ovat sallittuja neljä merkkiä sisältävälle segmentille: **\[ 234\], \[123 \], \[1 34\]**. Dimensioarvoissa on käytettävä hakasulkeita (\[ \]). Report Designer lisää sulkeet puolestasi. Kun useita segmenttejä tai useita dimensioita sisältävä alue sisältää yleismerkkejä (? tai \*), koko useita segmenttejä tai dimensioita sisältävän alueen alin ja ylin arvo määritetään. Tämän jälkeen sisällytetään loppuarvot ja kaikki niiden väliset arvot. Jos alue on suuri, kuten tilit väliltä 40 000–99 999, kelvollinen aloittava ja lopettava tili on määritettävä aina, kun se on mahdollista.

> [!NOTE] 
> Raporttien suunnitteluohjelma ei voi valita Microsoft Dynamics ERP -järjestelmästä niitä tilejä, dimensioita tai kenttiä, jotka sisältävät seuraavat varatut merkit: &, \*, \[, \], {, tai }. Voit lisätä et-merkin (&) vain silloin, kun rivin määritykset muodostetaan automaattisesti **Lisää rivejä dimensioista** -valintaikkunan avulla.

## <a name="add-or-subtract-from-other-accounts-in-a-row-definition"></a>Lisääminen tai vähentäminen muista tileistä rivin määrityksessä
Voit lisätä tai vähentää rahamääräisiä summia tilien välillä käyttämällä plus (+)- ja miinusmerkkiä (-) **Linkki taloushallinnon dimensioihin** -solussa. Seuraavassa taulukossa näkyvät taloushallinnon tietojen linkkien lisäämisen ja vähentämisen hyväksyttävät muodot.

| Toiminto                                                                               | Käytä tätä muotoa                                                                                              |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| Lisää kaksi täydellistä tiliä.                                                       | +jaosto=\[000\], tili=\[1205\], osasto=\[00\]+jaosto=\[100\], tili=\[1205\], osasto=\[00\] |
| Lisää kaksi segmenttiarvoa.                                                                 | +tili=\[1205\]+tili=\[1210\]                                                                           |
| Lisää yleismerkkejä sisältäviä segmenttiarvoja.                                    | +tili=\[120?+tili=\[11??\]                                                                             |
| Lisää täydellisten tilien alue.                                                | +jaosto=\[000:100\], tili=\[1205\], osasto=\[00\]                                                   |
| Lisää segmenttiarvojen alue.                                                          | +Tili=\[1200:1205\]                                                                                       |
| Lisää yleismerkkejä sisältävien segmenttiarvojen alue.                         | +Tili=\[120?:130?\]                                                                                       |
| Vähennä yksi täydellinen tili toisesta täydellisestä tilistä.              | +jaosto=\[000\], tili=\[1205\], osasto=\[00\]-jaosto=\[100\], tili=\[1205\], osasto=\[00\] |
| Vähennä yksi segmenttiarvo toisesta segmenttiarvosta.                                  | +tili=\[1205\]-tili=\[1210\]                                                                           |
| Vähennä yleismerkin sisältävä segmenttiarvo toisesta segmenttiarvosta. | +tili=\[1200\]-tili=\[11??\]                                                                           |
| Vähennä täydellisten tilien alue.                                           | -jaosto=\[000:100\], tili=\[1200:1205\], osasto=\[00:01\]                                           |
| Vähennä segmenttiarvojen alue.                                                     | -Tili=\[1200:1205\]                                                                                       |
| Vähennä yleismerkkejä sisältävien segmenttiarvojen alue.                    | -Tili=\[120?:130?\]                                                                                       |

Vaikka voit muokata tilejä suoraan, voit ottaa taloushallinnon tietojen linkeissä oikean muotoilun käyttöön myös **Dimensiot**-valintaikkunan avulla. Mitkä tahansa arvot voivat sisältää yleismerkkejä (? tai \*). Raporttien suunnitteluohjelma ei kuitenkaan voi valita Microsoft Dynamics ERP -järjestelmästä niitä tilejä, dimensioita tai kenttiä, jotka sisältävät seuraavat varatut merkit: &, \*, \[, \], {, tai }.

> [!NOTE]
> Jos haluat vähentää arvoja, kirjoita ne sulkeisiin. Jos annat esimerkiksi arvon **450?-(4509)**, se näkyy arvona **+tili=\[4509\]-tili=\[450?\]**. Tällöin Report Designer vähentää tilisegmentin 4509 summan minkä tahansa arvolla 450 alkavan tilisegmentin summasta.

### <a name="add-or-subtract-accounts-from-other-accounts"></a>Tilien lisääminen muihin tileihin tai niiden vähentäminen muista tileistä

1. Avaa Report Designer -ohjelmassa muokattava rivin määritys.
2. Kaksoisnapsauta oikealla rivillä **Linkki taloushallinnon dimensioihin** -sarakkeen solua.
3. Noudata seuraavia vaiheita **Dimensiot**-valintaikkunan ensimmäisellä rivillä.

    1. Valitse ensimmäisessä kentässä kaikki dimensiot (oletusarvo) tai avaa **Hallitse dimensioyhdistelmiä** -valintaikkuna napsauttamalla. Valintaikkunassa voit luoda, muokata, kopioida tai poistaa yhdistelmän.
    2. Kaksoisnapsauta **Operaattori +/-** -solua ja valitse plus (**+**)- tai miinus (**-**) -operaattori, jota käytetään rivin yhdessä tai useassa dimensioarvossa tai -yhdistelmässä.
    3. Avaa **Dimensiot**-valintaikkuna kaksoisnapsauttamalla soveltuvan dimensioarvon sarakkeen solua. Määritä sitten, onko kyseinen dimensioarvo tarkoitettu yksittäiselle arvolle vai alueelle, dimensioarvoyhdistelmälle vai summatileille. **Dimensiot**-valintaikkunan kenttien kuvaukset löytyvät Dimension kuvaus -valintaikkuna -osasta.
    4. Syötä segmenttiarvot **Mistä**- ja **Mihin**-sarakkeeseen.

4. Voit lisätä operaattoreita tekemällä kohtien 2–3 toimet uudelleen.

> [!NOTE]
> Operaattori otetaan käyttöön rivin kaikille dimensioille.

## <a name="description-of-the-dimensions-dialog-box"></a>Dimensioiden kuvaus -valintaikkuna
Seuraavassa taulukossa esitellään **Dimensiot**-valintaikkunan kentät.

| Nimike                | Kuvaus |
|---------------------|-------------|
| Yksittäinen tai alue | Syötä **Mistä**-kenttään tilin nimi tai etsi tili valitsemalla **Selaa**-painike ![Selaa](https://i-technet.sec.s-msft.com/dynimg/IC679490.gif "Selaa"). Voit valita alueen syöttämällä arvon **Mihin**-kenttään tai etsimällä sen kentässä. |
| Dimensioarvoyhdistelmä | Syötä **Nimi**-kenttään dimensioarvoyhdistelmän nimi. Voit luoda, muokata, kopioida tai poistaa yhdistelmän valitsemalla **Dimensioarvoyhdistelmien hallinta**. Rivin määrityksen tämän dimensioarvoyhdistelmän **Kaava**-kenttään täytetään **Linkki taloushallinnon dimensioihin** -solun kaava. |
| Summatilit   | Syötä **Nimi**-kenttään summatilien dimensio tai etsi se kentässä. Raportin määrityksen summatilin **Kaava**-kenttään täytetään **Linkki taloushallinnon dimensioihin** -solun kaava. |

## <a name="add-dimension-value-sets-in-a-row-definition"></a>Dimensioarvoyhdistelmien lisääminen rivin määritykseen
Dimensioarvoyhdistelmä on dimensioarvojen nimetty ryhmä. Dimensioarvoyhdistelmä voi sisältää vain yhden dimension arvoja, mutta dimensioarvoyhdistelmää voidaan käyttää myös useiden rivien, sarakkeiden, raportointipuiden ja raporttien määrityksissä. Dimensioarvoyhdistelmiä voidaan yhdistää myös raportin määrityksessä. Kun taloushallinnon tietojen muuttaminen edellyttää dimensioarvoyhdistelmän muuttamista, voit päivittää dimensioarvoyhdistelmän määrityksen. Päivitys kohdistetaan kaikille dimensioarvoyhdistelmää käyttäville alueille. Jos esimerkiksi määrität usein arvoalueen, kuten esimerkiksi 5100–5600, taloushallinnon tietojen linkittämistä varten, voit liittää tämän alueen tiliyhdistelmään, jonka nimi on Myynti. Kun luot dimensioarvojen joukon, voit valita sen taloushallintotietojen linkiksi. Jos sinulla on arvot 5100–5600 määritettynä esimerkiksi Myynti-kohteeseen ja arvo 4175 määritettynä Alennukset-kohteeseen, voit määrittää kokonaismyynnin vähentämällä Alennukset-summan Myynti-summasta, eli lausekkeella (5100:5600)-4175. Tämä toiminto osoitetaan näin: **(5100:5600)-4175**.

### <a name="create-a-set-of-dimension-values"></a>Dimensioarvoyhdistelmän luominen

1. Avaa Report Designer -ohjelmassa muokattava rivin, sarakkeen tai puun määritys.
2. Valitse **Muokkaa**-valikossa **Dimensioarvoyhdistelmien hallinta**.
3. Valitse **Dimensioarvoyhdistelmien hallinta** -valintaikkunan **Dimensio**-kentässä luotavan dimensioarvoyhdistelmän tyyppi ja valitse sitten **Uusi**.
4. Syötä **Uusi**-valintaruutuun yhdistelmän nimi ja kuvaus.
5. Kaksoisnapsauta **Mistä**-sarakkeen solua.
6. Valitse **Tili**-valintaikkunan luettelosta tilin nimi tai hae syöttö **Hae**-kentässä. Valitse sitten **OK**.
7. Toista vaiheet 5 ja 6 **Mihin**-sarakkeessa ja määritä operaattorille kaava.
8. Kun kaava on valmis, valitse **OK**.
9. Valitse **Dimensioyhdistelmien hallinta** -valintaikkunassa **Sulje**.

### <a name="update-a-set-of-dimension-values"></a>Dimensioarvojoukon päivittäminen

1. Avaa raporttien suunnitteluohjelmassa rivi-, sarake- tai puumääritys, jota haluat muokata.
2. Valitse **Muokkaa**-valikossa **Dimensioarvoyhdistelmien hallinta**.
3. Valitse **Dimensioarvoyhdistelmien hallinta** -valintaikkunan **Dimensio**-kentässä dimensiotyyppi.
4. Valitse luettelosta päivitettävä dimensioarvoyhdistelmä ja valitse sitten **Muokkaa**.
5. Muokkaa **Muokkaa**-valintaikkunassa yhdistelmään sisällytettävän kaavan arvoja.

    > [!NOTE]
    > Jos lisäät uusia tilejä tai dimensioita, varmista, että muokkaat aiemmin luodut dimensioarvoyhdistelmät, jotta muutokset otetaan huomioon.

6. Kaksoisnapsauta solua ja valitse sopiva operaattori **Mistä**- ja **Mihin**-tilille.
7. Valitse **OK**, kun haluat sulkea **Muokkaa**-valintaikkunan ja tallentaa muutokset.

### <a name="copy-a-dimension-set"></a>Dimensioyhdistelmän kopioiminen

1. Avaa Report Designer -ohjelmassa muokattava rivin, sarakkeen tai puun määritys.
2. Valitse **Muokkaa**-valikossa **Dimensioarvoyhdistelmien hallinta**.
3. Valitse **Dimensioarvoyhdistelmien hallinta** -valintaikkunan **Dimensio**-kentässä dimensiotyyppi.
4. Valitse luettelosta kopioitava yhdistelmä ja valitse sitten **Tallenna nimellä**.
5. Määritä kopioidulle yhdistelmälle uusi nimi ja valitse **OK**.

### <a name="delete-a-dimension-set"></a>Dimensioyhdistelmän poistaminen

1. Avaa raporttien suunnitteluohjelmassa rivi-, sarake- tai puumääritys, jota haluat muokata.
2. Valitse **Muokkaa**-valikossa **Dimensioarvoyhdistelmien hallinta**.
3. Valitse **Dimensioarvoyhdistelmien hallinta** -valintaikkunan **Dimensio**-kentässä dimensiotyyppi.
4. Valitse poistettava yhdistelmä ja valitse sitten **Poista**. Poista dimensioarvojoukko pysyvästi valitsemalla **Kyllä**.

## <a name="additional-resources"></a>Lisäresurssit

[Talousraportointi](financial-reporting-intro.md)
