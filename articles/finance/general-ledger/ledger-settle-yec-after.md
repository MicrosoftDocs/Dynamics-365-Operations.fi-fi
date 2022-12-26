---
title: Tietoja kirjanpidon selvityksestä -toiminto tilikauden lopetuksen jälkeen
description: Tässä artikkelissa käsitellään Tietoja kirjanpidon selvityksestä -toiminnon käyttämistä kirjanpidon tilikauden lopetusprosessin suorittamisen jälkeen.
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
ms.openlocfilehash: 7efa9d652d74bd836f51b5b1c5f6bfaf8934ea40
ms.sourcegitcommit: 0c927fcb3afd34d870391f05b5393a4673d916e5
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/08/2022
ms.locfileid: "9832159"
---
# <a name="awareness-between-ledger-settlement-feature-after-year-end-close"></a>Tietoja kirjanpidon selvityksestä -toiminto tilikauden lopetuksen jälkeen

[!include [banner](../includes/banner.md)]

## <a name="preparing-for-the-ledger-settlement-awareness-feature-after-year-end-close"></a>Tietoja kirjanpidon selvityksestä -toiminnon valmistelu tilikauden lopetuksen jälkeen

**Tietoja kirjanpidon selvityksestä ja tilinpäätöksestä** -ominaisuuteen (**Tietoja**-ominaisuus) on tehty merkittävä muutos siten, että kirjanpidon selvitystä ei voi suorittaa tilikausien välillä. Tilikausien välinen rajoitus koskee vain tapahtuman selvitystä, ei siis ostoreskontran ja myyntireskontran selvityksiä.

Ennen **Tietoja**-ominaisuuden käyttöönottoa lopetettavassa tilikaudessa ei saa olla yhtään tilikausien välillä selvitettyä kirjanpitotapahtumaa. Niinpä sellaisten siihen tilikauteen kirjattujen tapahtumien, jonka tilikauden lopetusta suoritetaan, selvitys on peruutettava, jotka kirjattiin toiselle tilikaudelle. Tapahtumat voidaan sitten selvittää uudelleen saman tilikauden tapahtumien perusteella.

Tässä artikkelissa käsitellään vaiheita, joiden avulla tunnistetaan tilikausien välillä selvitetyt kirjanpitotapahtumat, peruutetaan niiden selvitys ja selvitetään ne uudelleen. Käytetyssä esimerkissä tilikausi 2022 on lopetettu. Siinä keskitytään valmistelemaan kirjanpitotapahtumien selvitys hyvissä ajoin ennen vuoden 2023 tilikauden lopetuksen suorittamista.

## <a name="example-setup"></a>Esimerkkimääritykset

Seuraavassa kuvassa näkyy päätilille 110190 kirjatut tapahtumat. Vihreät kirjanpitotapahtumat on selvitetty samana tilikautena eikä niitä tarvitse muuttaa. Punaiset tapahtumat on selvitetty kirjanpitoon, mutta niiden tapahtumapäivät ovat eri tilikausilla. Nämä tapahtumat on tunnistettava ja tapahtuman selvitys on ehkä palautettava.

![Kirjanpitotapahtumat](./media/afterYEC1.png)

## <a name="example"></a>Esimerkki

Jos organisaatio haluaa käyttää **Tietoja**-ominaisuutta tilikauden 2022 tilikauden lopetuksen suorittamisen jälkeen, toimi seuraavasti.

> [!NOTE]
> Tilikauden 2022 ja aiempien tilikausien tilikauden lopetus on suoritettava uudelleen vain, jos tilikaudelle 2022 tai aiemmille tilikausille kirjataan uusia tapahtumia. Seuraavalla tavalla toimittaessa uusi tapahtumia ei kirjata vuodelle 2022. Siksi tilivuoden lopetusta ei tarvitse suorittaa uudelleen.
>
> Eri tilikausille selvitetyt kirjanpitotapahtumat voivat jäädä kirjanpitoon selvitetyiksi, jos niitä ei ole selvitetty vuonna 2023 tai jälkeen kirjatun tapahtuman perusteella. Jos tapahtumat on selvitetty esimerkiksi vuosille 2019 ja 2020, ne voivat jäädä selvitetyiksi.

1. Suorita vuoden 2022 tilikauden lopetus siten, että **Tietoja**-ominaisuus ei ole otettu käyttöön.
2. Valinnainen: Ota **Tietoja**-ominaisuus käyttöön vuoden 2022 tilikauden lopetuksen valmistumisen jälkeen. Tilikauden lopetuksen katsotaan valmistuneen, kun kaikki oikaisut on kirjattu eikä tilikauden lopetusprosessia suoriteta enää uudelleen.

    > [!IMPORTANT]
    > **Tietoja**-ominaisuus ei saa olla otettuna käyttöön, jos vuoden 2022 tilikauden lopetus suoritetaan uudelleen. Ominaisuuden käyttöönottamisella tässä vaiheessa on se etu, että käyttäjiä estetään selvittämästä eri tilikausille kirjattuja kirjanpitotapahtumia.

    Jos tilikauden lopetusprosessi ei ole valmistunut, seuraavat vaiheet voidaan suorittaa ilman **Tietoja**-ominaisuuden käyttöönottoa. Ominaisuus otetaan sitten ohjeiden mukaan käyttöön myöhemmässä vaiheessa.

3. Määritä **Tapahtuman selvitys** -sivulla kaikkien tilikausien 2022 ja 2023 välillä selvitettyjen tapahtumien kokonaismäärä. Huomaa, että vuoden 2021 tapahtumilla, jotka selvitetään vuoden 2022 tapahtumien perusteella, ei ole merkitystä, koska vuosi 2022 on jo lopetettu. Nämä tapahtuvat voivat jäädä selvitetyiksi.

    1. Määritä päivämääräalueeksi koko tilikausi 2022. Määritä päivämääräalueeksi esimerkiksi 1.1.2022–31.12.2022, jos kalenterivuotta käytetään tilikautena.
    2. Valitse **Tila**-kentässä **Selvitetty**.
    3. Suodata yksi kirjanpito kerrallaan.

        - Nämä vaiheet on toistettava kunkin kirjanpitotilin osalta, jossa tapahtuma selvitetään.
        - Jos muita kirjanpitotilejä ei enää määritetä tapahtuman selvitystä varten, ne on ehkä lisättävä väliaikaisesti takaisin tapahtuman selvityksen määrityksiin. Suorita sitten nämä vaiheet, jos kyseisillä kirjanpitotileillä on vuoden 2023 tapahtumia, jotka selvitettiin vuoden 2022 tai aiempien vuosien tapahtumien perusteella.

    4. Valitse **Tila**-sarake ja pidä se valittuna (tai napsauta sitä hiiren kakkospainikkeella) ja valitse sitten ryhmittely tämän sarakkeen perusteella.
    5. Valitse **Summa tapahtuman valuuttana**-sarake ja pidä se valittuna (tai napsauta sitä hiiren kakkospainikkeella) ja valitse se sitten sarakkeen kokonaissumman laskemista varten.

        - Jos tapahtumia selvitettiin vain vuonna 2022, summa on 0 (nolla).
        - Jos tapahtumia selvitettiin tilikausien välillä, summa ei ole 0 (nolla).

    6. Määritä, mitkä tapahtumat selvitettiin vuosien 2022 ja 2023 välillä käyttämällä suodatusperusteena **Selvityspäivä**-arvoa. Jos suodatusperusteena on selvityspäivä 1.1.–31.1.2023, summa on 700 $, mikä on kirjanpitoon vuosien 2022 ja 2023 selvitettyjen tapahtumien summa.

    ![Vuoden 2022 kirjanpitotapahtumien summa](./media/afterYEC2.png)

4. Toista vaihe 3 tilikaudelle 2023. Summan pitäisi olla sama 700 $ kuin vuonna 2022, sillä yhtään vuoden 2023 tapahtumaa ei ole selvitetty vuoden 2024 tapahtumien perusteella.

    ![Vuoden 2023 kirjanpitotapahtumien summa](./media/afterYEC3.png)

5. Jos **Tietoja**-ominaisuus otettiin käyttöön vaiheessa 2, poista se käytöstä ennen siirtymistä vaiheeseen 6. Seuraavissa vaiheessa palautetaan tilikausien välinen tapahtuman selvitys. Jos **Tietoja**-ominaisuus on otettu käyttöön, tilikauden 2022 tapahtuman selvitystä ei voi palauttaa. Ominaisuus on tämän vuoksi poistettava käytöstä ennen jatkamista.
6. Kun **Tietoja**-ominaisuus on poistettu käytöstä, palauta eriteltyjen tapahtumien tapahtuman selvitys käyttämällä samoja suodattimia **Tapahtuman selvitys** -sivulla.

    1. Palaa **Tapahtuman selvitys** -sivulle ja suodata vuoden 2023 tapahtumapäivät. Etsi sitten eritellyt tapahtumat, joiden summaksi muodostuu 700 $. Näiden tietojen suodattaminen ei ole ehkä helppoa. Tiedot on ehkä lähetettävä Microsoft Exceliin arviointia varten.
    2. Kun tapahtumaluettelo on käytettävissä, valitse **Tapahtuman selvitys** -sivulla olevat kirjanpitotapahtumat ja valitse sitten **Merkitse valitut**. Selvitettyjen kirjanpitotapahtumien molempien puolien ei tarvitse olla näkyvissä. Jos joko debet tai kredit merkitään, kaikki saman **Tilitystunnus**-arvon kohteet palautetaan, vaikka **Merkitty summa** -arvo ei olisikaan **0** (nolla).
    3. Peruuta tapahtumien selvitys valitsemalla **Peru merkityt tapahtumat**.

    ![Tapahtumien palauttaminen](./media/afterYEC4.png)

7. Jaa vuoden 2023 alkusaldo kahdeksi summaksi kirjaamalla oikaiseva yleinen kirjauskansio: osa summasta on selvitetty kalenterivuoden 2022 tapahtuman perusteella ja osaa summasta ei ole vielä selvitetty vuonna 2023.

    - **Alkusaldon edellisen vuoden perusteella selvitetty osa:** ensimmäinen summa on 700 $, joka perustuu vuosien 2022 ja 2023 välillä selvitettyihin summiin.
    - **Alkusaldon osa, jota ei ole selvitetty edellisen vuoden perusteella:** Toinen summa alkusaldon ja ensimmäisen selvitetyn summan, 525 $, välinen erotus. Jäljellä oleva summa on 1 700 $–700 $ = 1 000 $.

    Tällä tavoin vuoden 2023 tapahtumat voidaan selvittää sen 700 $:n perusteella, joka selvitettiin alun perin vuoden 2022 tapahtuman perusteella. Tämä vaihe on pakollinen, koska tapahtuman selvitys ei salli osittaisia selvityksiä.

    1. Siirry yleiseen kirjauskansioon ja kirjaa oikaisu. Organisaation on päätettävä käytettävä tapahtumapäivä vuoden 2023 avoimien kausien perusteella.
    2. **Älä salli manuaalista määritystä** -parametri on ehkä poistettava väliaikaisesti käytöstä **Päätili**-sivulla. Oikaisua ei kirjata, jos päätili ei salli manuaalista määritystä.

    ![Oikaisua ei kirjata](./media/afterYEC5.png)

8. Tapahtumat, joiden selvitys on kumottu, voidaan nyt selvittää uudelleen. Palaa **Tapahtuman selvitys** -sivulle ja rajoita päivämääräalueeksi 1.1.2022–31.12.2022. Seuraavassa kuvassa on nyt käytössä olevat tapahtumat, joiden selvitykset on kumottu.

    ![Selvittämättömät tapahtumat](./media/afterYEC6.png)

    - Alkusaldo 1 700 $ voidaan selvittää oikaisun -1 700 $ perusteella.
    - Eritellyt tapahtumat, joiden -700 $:n selvitys kumottiin, voidaan nyt selvittää 700,00 $:n oikaisun perusteella.

9. Ota **Tietoja**-ominaisuus uudelleen käyttöön.
10. Kun **Tietoja**-ominaisuus on otettu käyttöön, tilikausien välinen tapahtuman selvitys ei ole mahdollista. Jäljellä oleva 1 000 $:n saldo on ehkä jaettava vielä pienemmiksi summiksi, ennen kuin selvitys voidaan tehdä uusien vuoden 2023 tapahtumien perusteella. Osa asiakkaista kirjaa tämän erittelyn vaiheessa 8, jossa 1 000 $ jaetaan ilmaisemaan vuoden 2022 selvittämättömät tapahtumat. Tämä menettely käytännössä vastaa **Tietoja**-ominaisuuden toimintaa, mutta kyse on kuluvasta vuodesta. Seuraavana vuonna se tehdään automaattisesti tapahtuman selvitysmääritysten **Säilytä tiedot** -asetuksen avulla.
