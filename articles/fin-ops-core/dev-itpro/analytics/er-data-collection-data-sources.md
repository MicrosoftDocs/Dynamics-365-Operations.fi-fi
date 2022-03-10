---
title: DATA COLLECTION -tietolähteiden käyttäminen sähköisissä raportointimuodoissa
description: Tässä aiheessa käsitellään DATA COLLECTION -tietolähteiden käyttöä sähköisissä raportointimuodoissa (ER-muodoissa).
author: NickSelin
ms.date: 08/23/2021
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
ms.search.validFrom: 2021-01-01
ms.dyn365.ops.version: AX 10.0.16
ms.openlocfilehash: 185fb9a33cb4cc655dfdf640b4c239d617426c64
ms.sourcegitcommit: d5d6b81bd8b08de20cc018c2251436065982489e
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/17/2022
ms.locfileid: "8323898"
---
# <a name="use-data-collection-data-sources-in-electronic-reporting-formats"></a>DATA COLLECTION -tietolähteiden käyttäminen sähköisissä raportointimuodoissa

[!include [banner](../includes/banner.md)]

[Sähköisen raportoinnin (ER)](general-electronic-reporting.md) kehyksen toimintojen suunnitteluohjelmaa voidaan käyttää määrittämään sen ER-ratkaisun muoto-osassa, jolla luodaan erimuotoisia lähteviä asiakirjoja. Määritetyn muoto-osan hierarkiarakenne koostuu erilaisista muotoelementtityypeistä. Näitä muotoelementtejä käytetään luotujen asiakirjojen suorituksenaikaiseen täyttämiseen tarvittavilla tiedoilla. Kun ER-muoto suoritetaan, muotoelementit suoritetaan oletusarvoisesti samassa järjestyksessä, jossa ne ovat muotohierarkiassa: yksi kerrallaan, ylhäältä alas.

Kun ER suorittaa sidonnan sisältävän muotoelementin, kyseisen sidonnan kaava suoritetaan ja muotoelementti lisää arvon luotuun asiakirjaan. Sidonta voi välittää esimerkiksi tietomallin kentän arvon muotoelementtiin. DATA COLLECTION -tietolähde voidaan määrittää keräämään tietomallikenttien arvot suorituksen aikana, tuottamaan arvojen summat ja täyttämään kerätyt arvot luotuun asiakirjaan. Tämän menetelmän käyttäminen edellyttää alkuperäisen sidonnan muuttamista siten, että määritetty DATA COLLECTION -tietolähde välittää tietomallikentän arvon muotoelementtiin. Kun arvot siirretään DATA COLLECTION -tietolähteen kautta, tarvittavat tiedot voidaan kerätä tulevaa käyttöä varten.

DATA COLLECTION -tietolähdettä määritettäessä määritetään arvotyyppi, jotta hallitaan tietolähteessä. Tällä hetkellä arvojen keräämistä varten tuetaan seuraavia [tietotyyppejä](er-formula-supported-data-types-primitive.md):

- Boolen arvo
- Päivämäärä
- Päivämäärä ja aika
- GUID
- Int64
- Kokonaisluku
- Reaaliluku
- Merkkijono
- Aika

DATA COLLECTION -tietolähteen `Collect(Value)`-menetelmää voi käyttää arvon siirtämiseen tietolähteeseen kerättäväksi. Tässä menetelmässä `Value`-argumentti on joko vakio tai soveltuvan tietotyypin tietolähdekentän kelvollinen polku.

DATA COLLECTION -tietolähteen `Result`-ominaisuutta voi käyttää kerätyt arvot sisältävän luettelon käyttämiseen. Tämä ominaisuus palauttaa [tietueluettelon](er-formula-supported-data-types-composite.md#record-list). Tietueluettelon tietueissa on `Value`-kenttä, jonka avulla kerättyjä arvoja voidaan käyttää.

DATA COLLECTION -tietolähde kerää oletusarvoisesti vain yksilöiviä arvoja.

Kaikki arvot voidaan kerätä määrittämällä määritetyn DATA COLLECTION -tietolähteen **Kerää kaikki arvot** -kentän arvoksi **Kyllä**. Kun **Kerää kaikki arvot** -kentän asetuksena on **Kyllä**, parametrisoitu `Sum(Flag)`-ominaisuus on käytettävissä. Tämän ominaisuuden avulla saadaan kaikkien tällä hetkellä kerättyinä olevien arvon kokonaismäärä. Tämän ominaisuuden `Flag`-argumentti on [totuusarvo](er-formula-supported-data-types-primitive.md#boolean), joka ilmaisee, onko kokonaisarvo nollattava.

- Jos arvona on **Epätosi**, summaamista jatketaan aiemmin kerätystä määrästä.
- Jos arvona on **Tosi**, uusi summaaminen aloitetaan.

Tällä hetkellä summaamisessa tuetaan seuraavia tietotyyppejä:

- Int64
- Kokonaisluku
- Reaaliluku

Lisätietoja tästä ominaisuudesta saa suorittamalla seuraavan esimerkin.

## <a name="example-configure-an-er-format-to-do-counting-and-summing-by-using-a-data-collection-data-source"></a>Esimerkki: ER-muodon määrittäminen laskemaan ja summaamaan DATA COLLECTION -tietolähteen avulla

Tämä esimerkki osoittaa, miten järjestelmänvalvojan tai sähköisen raportoinnin toiminnallisen konsultin roolin omaava käyttäjä voi määrittää DATA COLLECTION -tietolähdettä käyttävän ER-muodon sekä miten tällä tavoin lasketaan juoksevia summia ja kerätään yhteenlaskettuja arvoja.

Tässä esimerkissä ohjeaiheessa käsitellyt toimenpiteet voidaan suorittaa USMF-yrityksessä Microsoft Dynamics 365 Financessa.

### <a name="upload-and-use-the-provided-er-solution"></a>Annetun ER-ratkaisun lataaminen ja käyttäminen

1. [ER-mallimääritysten tuonti](er-defer-sequence-element.md#import-the-sample-er-configurations)
2. [Aktivoi määrityslähde](er-defer-sequence-element.md#activate-a-configurations-provider).
3. [Tuodun mallin yhdistämismäärityksen tarkistaminen](er-defer-sequence-element.md#review-the-imported-model-mapping)
4. [Tuodun muodon tarkistaminen](er-defer-sequence-element.md#review-the-imported-format)
5. [Tuodun muodon suorittaminen](er-defer-sequence-element.md#run-the-imported-format)

### <a name="run-the-format-of-the-provided-er-solution"></a>Annetun ER-ratkaisun muodon suorittaminen

1. Vallitse **Muodon suunnittelu** -sivulla **Suorita**.
2. Valitse **Sähköisen raportin parametrit** -valintaikkunasta **OK**.
3. Lataa ja tarkista verkkoselaimen tarjoama tiedosto.

    ![Alkuperäisen muodon suorittamisen tulokset sisältävä ladattu tiedosto](./media/er-data-collection-data-sources-01.png)

### <a name="modify-the-format-of-the-er-solution-to-calculate-the-running-tax-total"></a>Juoksevan verosumman laskeminen muokkaamalla ER-ratkaisun muotoa

Jos tapahtumien määrä on huomattavasti suurempi kuin tässä esimerkissä, summien laskeminen voi kestää kauemmin ja aiheuttaa suorituskykyongelmia. Muodon asetuksia muuttamalla voidaan ehkäistä näitä suorituskykyongelmia. Koska veroarvojen lisääminen luotavaan raporttiin edellyttää niiden käyttämistä, näitä tietoja voidaan käyttää uudelleen veroarvojen yhteen laskemiseen.

1. Valitse **Muodon suunnittelija** -sivun **Yhdistämismääritys**-välilehdessä **Lisää juuri**.
2. Valitse **Lisää tietolähde** -valintaikkunassa **Funktiot** \> **Tietojenkeruu**.
3. Toimi **Data collection -tietolähteen ominaisuudet** -valintaikkunassa seuraavasti:

    1. Anna **Nimi**-kentässä **CollectedTaxValues**.
    2. Valitse **Nimiketyyppi**-kentässä **Reaaliluku**.
    3. Valitse **Kerää kaikki arvot** -kentässä **Kyllä**.
    4. Valitse **OK**.

4. Valitse numeerinen **Raportti\\Rivit\\Tietue\\TaxAmount** -muotoelementti.

    > [!NOTE]
    > Tällä hetkellä tähän elementtiin on määritetty `@.Value`-sidonta. Niinpä luotuun asiakirjaan täytetään `model.Data.List.Value`-kentän veroarvot.

5. Valitse **Muokkaa kaavaa**.
6. Toimi **Kaavan suunnitteluohjelma** -sivulla seuraavasti:

    1. Vaihda **Kaava**-kentässä `@.Value`-ominaisuuden tilalle `CollectedTaxValues.Collect(@.Value)`.
    2. Tallenna muutokset ja sulje sivu.

    > [!NOTE]
    > Uusi sidonta siirtää samat veroarvot luotuun asiakirjaan. Kyseiset arvot kerätään kuitenkin myös **CollectedTaxValues**-tietolähteessä.

7. Valitse numeerinen **Raportti\\Rivit\\Tietue\\RunningTotal**-muotoelementti.
8. Valitse **Muokkaa kaavaa**.
9. Toimi **Kaavan suunnitteluohjelma** -sivulla seuraavasti:

    1. Anna **Kaava**-kentässä `CollectedTaxValues.Sum(false)`.
    2. Tallenna muutokset ja sulje sivu.

    > [!NOTE]
    > Uusi sidonta siirtää luotuun asiakirjaan jo annettujen veroarvojen kokonaismäärän.

    ![Päivitetyt sidonnat sisältävät numeeriset elementit Muodon suunnittelija -sivulla](./media/er-data-collection-data-sources-02.png)

10. Valitse ensin **Tallenna** ja sitten **Suorita**.
11. Valitse **Sähköisen raportin parametrit** -valintaikkunasta **OK**.
12. Lataa ja tarkista verkkoselaimen tarjoama tiedosto.

    ![Muokatun muodon suorittamisen tulokset sisältävä ladattu tiedosto](./media/er-data-collection-data-sources-03.png)

### <a name="modify-the-format-to-evaluate-the-list-of-collected-tax-values"></a>Muodon muokkaaminen arvioimaan kerättyjen veroarvojen luetteloa

1. Valitse **Muodon suunnittelija** -sivun **Muoto**-välilehdessä numeerinen **Raportti\\Rivit\\Tietue\\RunningTotal**-muotoelementti ja toimi seuraavasti:

    1. Vaihda **Numerotyyppi**-kentän arvo **Reaaliluku** arvoksi **Kokonaisluku**.
    2. Muuta **Numeromuoto**-kentän arvo **F2** arvoksi **F0**.

3. Valitse **yhdistämismääritys**-välilehdessä **Muokkaa kaavaa**.
4. Toimi **Kaavan suunnitteluohjelma** -sivulla seuraavasti:

    1. Anna **Kaava**-kentässä `COUNT(CollectedTaxValues.Result)`.
    2. Tallenna muutokset ja sulje sivu.

    > [!NOTE]
    > Uusi sidonta siirtää luotuun asiakirjaan tietueiden määrän siinä luettelossa, johon veroarvot kerätään.

5. Valitse ensin **Tallenna** ja sitten **Suorita**.
6. Valitse **Sähköisen raportin parametrit** -valintaikkunasta **OK**.
7. Lataa ja tarkista verkkoselaimen tarjoama tiedosto.

    ![Toisen muokatun muodon suorittamisen tulokset sisältävä ladattu tiedosto](./media/er-data-collection-data-sources-04.png)

## <a name="frequently-asked-questions"></a>Usein kysytyt kysymykset

### <a name="if-i-have-to-calculate-running-totals-and-collect-data-what-is-the-difference-between-using-a-data-collection-data-source-and-using-the-built-in-data-collection-functions"></a>Jos juoksevat summat on laskettava ja tiedot kerättävä, mitä eroa on DATA COLLECTION -tietolähteen käyttämisellä ja valmiiden DATA COLLECTION -funktioiden käyttämisellä?

Sekä DATA COLLECTION -tietolähdettä että valmiita [DATA COLLECTION](er-functions-category-data-collection.md) -funktioita voidaan käyttää tietojen keräämiseen, yhteenlaskemiseen ja laskemiseen niiden tietojen perusteella, jotka on siirretty luotuun lähtevään asiakirjaan. Tekniikkaa valittaessa on otettava huomioon seuraavat seikat:

| Tietolähde | Valmiit funktiot |
|-------------| ------------------ |
| Vain arvot kerätään. | <p>Arvojen nimet kerätään. Tämän vuoksi voidaan laskea summia erillisille arvoryhmille.</p><p>Lisäksi ryhmät voidaan poimia luettelona.</p><p>Myös tekstiarvoja voidaan kerätä.</p> |
| Yksilöivät arvot kerätään automaattisesti. | Yksilöivien arvojen luettelon poimiminen kerätyistä arvoista edellyttää lisäasetuksia. |
| Suorituskyky määräytyy kerättyjen arvojen määrän mukaan. | Käytännössä suorituskyky ei määräydy kerättyjen arvojen määrän mukaan. |
| Tätä tekniikkaa voi käyttää kaikissa lähtevissä asiakirjatyypeissä. | Tätä tekniikkaa voi käyttää vain teksti- ja XML-tiedostoissa. |

## <a name="additional-resources"></a>Lisäresurssit

- [Määritä muoto suorittamaan laskenta ja summaus](./tasks/er-format-counting-summing-1.md)
- [Sähköisen raportoinnin muotojen sarjaelementtien suorittamisen lykkääminen](er-defer-sequence-element.md#Example)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
