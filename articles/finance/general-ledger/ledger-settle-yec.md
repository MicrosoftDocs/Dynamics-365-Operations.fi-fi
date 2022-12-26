---
title: Tietoja kirjanpidon selvityksestä -toiminto ennen tilikauden lopetusta
description: Tässä artikkelissa käsitellään Tietoja kirjanpidon selvityksestä -toiminnon käyttämistä ennen kirjanpidon tilikauden lopetusprosessin suorittamista.
author: kweekley
ms.date: 12/02/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2022-01-31
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: c79b6f50296560e1534be0621bb2aa8eaa2c1dc8
ms.sourcegitcommit: 0c927fcb3afd34d870391f05b5393a4673d916e5
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/08/2022
ms.locfileid: "9832158"
---
# <a name="awareness-between-ledger-settlement-feature-before-year-end-close"></a>Tietoja kirjanpidon selvityksestä -toiminto ennen tilikauden lopetusta

[!include [banner](../includes/banner.md)]

## <a name="preparing-for-the-ledger-settlement-awareness-feature-before-year-end-close"></a>Tietoja kirjanpidon selvityksestä -toiminnon valmistelu ennen tilikauden lopetusta

**Tietoja kirjanpidon selvityksestä ja tilinpäätöksestä** -ominaisuuteen (**Tietoja**-ominaisuus) on tehty merkittävä muutos siten, että kirjanpidon selvitystä ei voi suorittaa tilikausien välillä. Tilikausien välinen rajoitus koskee vain tapahtuman selvitystä, ei siis ostoreskontran ja myyntireskontran selvityksiä.

Ennen **Tietoja**-ominaisuuden käyttöönottoa lopetettavassa tilikaudessa ei saa olla yhtään tilikausien välillä selvitettyä kirjanpitotapahtumaa. Niinpä sellaisten siihen tilikauteen kirjattujen tapahtumien, jonka tilikauden lopetusta suoritetaan, selvitys on peruutettava, jotka kirjattiin toiselle tilikaudelle. Tapahtumat voidaan sitten selvittää uudelleen saman tilikauden tapahtumien perusteella.

Tässä artikkelissa käsitellään vaiheita, joiden avulla tunnistetaan tilikausien välillä selvitetyt kirjanpitotapahtumat, peruutetaan niiden selvitys ja selvitetään ne uudelleen. Käytettävässä esimerkissä tilikausi 2021 on lopetettu ja tilikauden 2022 tilikauden lopetuksen suorittamista valmistellaan.

## <a name="example-setup"></a>Esimerkkimääritykset

Seuraavassa kuvassa näkyy päätilille 110190 kirjatut tapahtumat. Vihreät kirjanpitotapahtumat on selvitetty samana tilikautena eikä niitä tarvitse muuttaa. Punaiset tapahtumat on selvitetty kirjanpitoon, mutta niiden tapahtumapäivät ovat eri tilikausilla. Nämä tapahtumat on tunnistettava ja tapahtuman selvitys on ehkä palautettava.

![Kirjanpitotapahtumat](./media/YEC1.png)

## <a name="example"></a>Esimerkki

Jos organisaatio haluaa käyttää **Tietoja**-ominaisuutta ennen tilikauden 2022 tilikauden lopetuksen suorittamista, toimi seuraavasti.

> [!NOTE]
> Tilikauden 2021 ja aiempien tilikausien tilikauden lopetus on suoritettava uudelleen vain, jos tilikaudelle 2021 tai aiemmille tilikausille kirjataan uusia tapahtumia. Seuraavalla tavalla toimittaessa uusi tapahtumia ei kirjata vuodelle 2021. Siksi tilivuoden lopetusta ei tarvitse suorittaa uudelleen.
>
> Eri tilikausille selvitetyt kirjanpitotapahtumat voivat jäädä kirjanpitoon selvitetyiksi, jos niitä ei ole selvitetty vuonna 2022 tai jälkeen kirjatun tapahtuman perusteella. Jos tapahtumat on selvitetty esimerkiksi vuosille 2019 ja 2020, ne voivat jäädä selvitetyiksi.

1. Valinnainen: **Tietoja**-ominaisuuden ottaminen väliaikaisesti käyttöön.

    - Jos ominaisuus otetaan käyttöön, se on poistettava myöhemmissä vaiheissa käytöstä, kun asiasta mainitaan. Ominaisuuden käyttöönottamisella tässä vaiheessa on se etu, että käyttäjiä estetään väliaikaisesti selvittämästä kirjanpitotapahtumia, jotka kirjattiin eri tilikausille.
    - Jos ominaisuutta ei oteta käyttöön, tiimiä kannattaa pyytää olemaan selvittämättä tapahtumia tilikausien välillä. Jos tilikausien välinen selvitys tapahtuu seuraavien vaiheiden suorittamisen jälkeen, kirjanpitotapahtumat on tunnistettava ja selvitys poistettava toistamalla vaiheet.

2. Määritä **Tapahtuman selvitys** -sivulla kaikkien tilikausien 2021 ja 2022 välillä selvitettyjen tapahtumien kokonaismäärä.

    1. Määritä päivämääräalueeksi koko tilikausi 2021. Anna päivämääräalueeksi esimerkiksi 1.1.2021–31.12.2021, jos kalenterivuotta käytetään tilikautena.

        Jos **Tietoja**-ominaisuus on otettu käyttöön, varoitus ilmoittaa, että lopetetun tilikauden tapahtumia ei voi selvittää eikä selvitystä peruuttaa. Varoituksella ei ole merkitystä, koska tässä vaiheessa ei tehdä selvityksiä tai selvitysten peruutuksia.

    2. Valitse **Tila**-kentässä **Selvitetty**.
    3. Suodata yksi kirjanpito kerrallaan.

        - Nämä vaiheet on toistettava kunkin kirjanpitotilin osalta, jossa tapahtuma selvitetään.
        - Jos muita kirjanpitotilejä ei enää määritetä tapahtuman selvitystä varten, ne on ehkä lisättävä väliaikaisesti takaisin tapahtuman selvityksen määrityksiin. Suorita sitten nämä vaiheet, jos kyseisillä kirjanpitotileillä on vuonna 2022 tapahtumia, jotka selvitettiin toisen tilikauden tapahtumien perusteella.

    4. Valitse **Tila**-sarake ja pidä se valittuna (tai napsauta sitä hiiren kakkospainikkeella) ja valitse sitten ryhmittely tämän sarakkeen perusteella.
    5. Valitse **Summa tapahtuman valuuttana**-sarake ja pidä se valittuna (tai napsauta sitä hiiren kakkospainikkeella) ja valitse se sitten sarakkeen kokonaissumman laskemista varten.

        - Tapahtumia selvitettiin vain vuonna 2021, summa on 0 (nolla).
        - Jos tapahtumia selvitettiin tilikausien välillä, summa ei ole 0 (nolla).

        Seuraavassa kuvassa saldo on 525,00 $. Tämä saldo on eri tilikausien tapahtumien perusteella selvitettyjen tapahtumien summa. Summa voi sisältää tapahtumat, jotka selvitettiin vuosien 2021 ja 2022 välillä, sekä tapahtumat, jotka selvitettiin vuosien 2022 ja 2023 välillä.

        ![Kirjanpitotapahtumat 2021–2022](./media/YEC2.png)

    6. Määritä, mitkä tapahtumat selvitettiin vuosien 2020 ja 2021 välillä käyttämällä lisäsuodatusperusteena **Selvityspäivä**-arvoa. Määritä suodattimen päivämääräalueeksi 1.1.2021–31.12.2021. Yhtään tapahtumaa ei näytetä, koska yhtään vuoden 2020 tapahtumaa ei selvitetty vuodelle 2021 kirjattujen tapahtumien perusteella.
    7. Määritä, mitkä tapahtumat selvitettiin vuosien 2021 ja 2022 välillä muuttamalla päivämääräsuodattimen **Selvityspäivä**-arvoa. Määritä suodattimen päivämääräalueeksi 1.1.2022–31.12.2022. Tapahtumat näytetään uudelleen ja summa on 525,00 $, koska kaikki tapahtumat selvitettiin vuosien 2021 ja 2022 välillä.

3. Määritä **Tapahtuman selvitys** -sivulla kaikkien tilikausien 2021 ja 2022 välillä selvitettyjen tapahtumien kokonaismäärä.

    1. Määritä päivämääräalueeksi koko tilikausi 2022. Määritä päivämääräalueeksi esimerkiksi 1.1.2022–31.12.2022, jos kalenterivuotta käytetään tilikautena.
    2. Valitse **Tila**-kentässä **Selvitetty**.
    3. Suodata yksi kirjanpito kerrallaan.
    4. Valitse **Tila**-sarake ja pidä se valittuna (tai napsauta sitä hiiren kakkospainikkeella) ja valitse sitten ryhmittely tämän sarakkeen perusteella.
    5. Valitse **Summa tapahtuman valuuttana**-sarake ja pidä se valittuna (tai napsauta sitä hiiren kakkospainikkeella) ja valitse se sitten sarakkeen kokonaissumman laskemista varten.

        ![Kirjanpitotapahtuman kokonaissummat](./media/YEC3.png)

    6. Lisää **Selvityspäivä**-arvoon lisäsuodatin. Määritä suodattimen päivämääräalueeksi 1.1.2022–31.12.2022. Sama summa 525,00 $ näytetään. Tämä tulos vahvistaa, että vuosien 2021 ja 2022 välillä selvitettyjen tapahtumien kokonaissumma on 525,00 $.

        ![Vuoden 2022 ja 2023 selvityspäivien kirjanpitotapahtumat](./media/YEC4.png)

    7. Vaihda **Selvityspäivä**-arvon lisäsuodatin. Määritä suodattimen päivämääräalueeksi 1.1.2023–31.12.2023. Näkyviin tulee uusi summa, 700 $. Tämä summa on vuosien 2022 ja 2023 välillä selvitettyjen tapahtumien kokonaissumma.
 
4. Toista vaihe 3 tilikaudelle 2023. Summan pitäisi olla sama 700 $ kuin vuonna 2022, sillä yhtään vuoden 2023 tapahtumaa ei ole selvitetty vuoden 2024 tapahtumien perusteella.
5. Jos **Tietoja**-ominaisuus otettiin käyttöön vaiheessa 1, poista se käytöstä ennen siirtymistä vaiheeseen 6. Seuraavissa vaiheessa palautetaan tilikausien välinen tapahtuman selvitys. Jos **Tietoja**-ominaisuus on otettu käyttöön, tilikauden 2021 tapahtuman selvitystä ei voi palauttaa. Ominaisuus on tämän vuoksi poistettava käytöstä ennen jatkamista.
6. Kun **Tietoja**-ominaisuus on poistettu käytöstä, palauta eriteltyjen tapahtumien tapahtuman selvitys käyttämällä samoja suodattimia **Tapahtuman selvitys** -sivulla.

    1. Palaa **Tapahtuman selvitys** -sivulle ja suodata vuoden 2021 tapahtumapäivät. Lisää **Selvityspäivä**-arvoon lisäsuodatin. Määritä suodattimen päivämääräalueeksi 1.1.2022–31.12.2022. Etsi sitten eritellyt tapahtumat, joiden summaksi muodostuu 525 $. Näiden tietojen suodattaminen ei ole ehkä helppoa. Tiedot on ehkä lähetettävä Microsoft Exceliin arviointia varten.
    2. Kun tapahtumaluettelo on käytettävissä, valitse **Tapahtuman selvitys** -sivulla olevat kirjanpitotapahtumat ja valitse sitten **Merkitse valitut**. Selvitettyjen kirjanpitotapahtumien molempien puolien ei tarvitse olla näkyvissä. Jos joko debet tai kredit merkitään, kaikki saman **Tilitystunnus**-arvon kohteet palautetaan, vaikka **Merkitty summa** -arvo ei olisikaan **0** (nolla).
    3. Peruuta tapahtumien selvitys valitsemalla **Peru merkityt tapahtumat**.

    ![Merkittyjen tapahtumien peruminen](./media/YEC5.png)

7. Peru vuosien 2022 ja 2023 välillä selvitettyjen tapahtumien selvitys toistamalla vaihe 6.

    ![Kirjanpitotapahtumien peruminen](./media/YEC6.png)

8. Jaa vuoden 2022 alkusaldo kahdeksi summaksi kirjaamalla oikaiseva yleinen kirjauskansio: osa summasta on selvitetty kalenterivuoden 2021 tapahtuman perusteella ja osaa summasta ei ole vielä selvitetty vuonna 2022.

    - **Alkusaldon edellisen vuoden perusteella selvitetty osa:** ensimmäinen summa on 525 $, joka perustuu vuosien 2021 ja 2022 selvitettyihin summiin.
    - **Alkusaldon osa, jota ei ole selvitetty edellisen vuoden perusteella:** Toinen summa alkusaldon ja selvitetyn summan, 525 $, välinen erotus. Jäljellä oleva summa on 1 025 $–525 $ = 500 $.

    Tällä tavoin vuoden 2022 tapahtumat voidaan selvittää sen 525 $:n perusteella, joka selvitettiin alun perin vuoden 2021 tapahtuman perusteella. Tämä vaihe on pakollinen, koska tapahtuman selvitys ei salli osittaisia selvityksiä.

    1. Siirry yleiseen kirjauskansioon ja kirjaa oikaisu. Organisaation on päätettävä käytettävä tapahtumapäivä avoimien kausien perusteella. Nämä tapahtumat on ehkä selvitetty käyttämällä tapahtumapäivänä vuoden 2022 tammikuuta tai helmikuuta, mutta oikaisu on ehkä kirjattava joulukuussa, jos se on ainoa avoin kausi.
    2. **Älä salli manuaalista määritystä** -parametri on ehkä poistettava väliaikaisesti käytöstä **Päätili**-sivulla. Oikaisua ei kirjata, jos päätili ei salli manuaalista määritystä.

    ![Oikaisua ei kirjata](./media/YEC7.png)

9. Tapahtumat, joiden selvitys on kumottu, voidaan nyt selvittää uudelleen. Palaa **Tapahtuman selvitys** -sivulle ja rajoita päivämääräalueeksi 1.1.2022–31.12.2022. Seuraavassa kuvassa on nyt käytössä olevat tapahtumat, joiden selvitykset on kumottu.

    ![Selvittämättömät tapahtumat](./media/YEC8.png)

    - Alkusaldo 1 025 $ voidaan selvittää oikaisun -1 025 $ perusteella.
    - Eritellyt tapahtumat, joiden -400 $:n, -50 $:n ja -75 $:n selvitys peruutettiin, voidaan nyt selvittää 525,00 $:n oikaisun perusteella.

    ![Eritellyt tapahtumat](./media/YEC9.png)

10. Ota **Tietoja**-ominaisuus käyttöön. Tilikauden lopetus voidaan nyt suorittaa.

    - Ennen tilikauden lopetusta kannattaa harkita **Säilytä tiedot** -vaihtoehdon valitsemista kaikkien tasetilien tapahtuman selvityksen määrityksissä. Lisätietoja tämän vaiheen suorittamisesta on Tietoja-ominaisuuden ohjeissa.
    - Jos tapahtumia on silti selvitetty tilikausien välillä, kun vuoden 2022 tilikauden lopetus aloitetaan, tilikauden lopetusprosessi ilmoittaa siitä heti.
    - Jos vuoden 2021 ja 2022 tapahtumia on edelleen selvitettynä, **Tietoja**-ominaisuus on poistettava uudelleen käytöstä ja tapahtumien selvitys peruutettava toistamalla edelliset vaiheet. Tämä on pakollista, sillä vuosi 2021 on lopetettu eikä lopetetun tilikauden tapahtumien selvitystä voi peruuttaa.
    - Jos vuoden 2022 ja 2023 tapahtumia on edelleen selvitettynä, **Tietoja**-ominaisuutta **ei** tarvitse poistaa käytöstä. Koska vuosi 2022 ja 2023 ei ole lopetettu, tapahtumien selvitys voidaan peruuttaa edellisten vaiheiden mukaan.

Kun vuoden 2022 tilikauden lopetus on suoritettu, **Tietoja**-ominaisuus voidaan jättää jatkossa käyttöönotetuksi.
