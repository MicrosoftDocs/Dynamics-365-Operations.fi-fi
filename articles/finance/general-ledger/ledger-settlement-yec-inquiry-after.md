---
title: Tietoja kirjanpidon selvityksestä -toiminto tilikauden lopetuksen jälkeen kyselysivua käyttämällä
description: Tässä artikkelissa käsitellään Tietoja kirjanpidon selvityksestä -toiminnon käyttämistä uuden kyselysivun avulla kirjanpidon tilikauden lopetuksen suorittamisen jälkeen.
author: kweekley
ms.date: 12/15/2022
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
ms.openlocfilehash: 921d2a17409ae10cd9c22eeca11557ba1248b9bc
ms.sourcegitcommit: 9f3a60a583da21382a14f32ce146fc9ce03f2a09
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/15/2022
ms.locfileid: "9853132"
---
# <a name="awareness-between-ledger-settlement-feature-after-year-end-close-using-the-inquiry-page"></a>Tietoja kirjanpidon selvityksestä -toiminto tilikauden lopetuksen jälkeen kyselysivua käyttämällä

**Tietoja kirjanpidon selvityksestä ja tilinpäätöksestä** -ominaisuuden (**Tietoja**-ominaisuuden) merkittävä muutos on se, että kirjanpidon selvitystä ei voi suorittaa tilikausien välillä. Tilikausien välinen rajoitus koskee vain tapahtuman selvitystä, ei siis ostoreskontran ja myyntireskontran selvityksiä.

Ennen **Tietoja**-ominaisuuden käyttöönottoa lopetettavassa tilikaudessa ei saa olla yhtään tilikausien välillä selvitettyä kirjanpitotapahtumaa. Niinpä sellaisten siihen tilikauteen kirjattujen tapahtumien, jonka tilikauden lopetusta suoritetaan, selvitys on peruutettava, jotka kirjattiin toiselle tilikaudelle. Tapahtumat voidaan sitten selvittää uudelleen saman tilikauden tapahtumien perusteella.

Tässä artikkelissa käsitellään vaiheita, joiden avulla tunnistetaan tilikausien välillä selvitetyt kirjanpitotapahtumat, peruutetaan niiden selvitys ja selvitetään ne uudelleen. Käytetyssä esimerkissä tilikausi 2022 on lopetettu. Siinä keskitytään valmistelemaan kirjanpitotapahtumien selvitys ennen vuoden 2023 tilikauden lopetuksen suorittamista.

Microsoft Dynamics 365 Finance -versiosta 10.0.29 alkaen kirjanpitotapahtumat voidaan tunnistaa sekä niiden selvitys voidaan peruuttaa ja sitten selvittää uudelleen uudella kyselysivulla. Jos Microsoft Dynamics 365 Finance 10.0.29 tai sitä uudempi ei ole käytössä, ohjeita kirjanpitotapahtumien tunnistamiseen sekä niiden selvityksen peruuttamiseen ja selvittämiseen uudelleen on seuraavissa artikkeleissa:

- [Tietoja kirjanpidon selvityksestä -toiminto ennen tilikauden lopetusta](ledger-settle-yec.md)
- [Tietoja kirjanpidon selvityksestä -toiminto tilikauden lopetuksen jälkeen](ledger-settle-yec-after.md)

Lisätietoja uudesta kyselyikkunasta on kohdassa [Tapahtuman selvityksen kysely](ledger-settlement-inquiry.md). 

## <a name="example-setup"></a>Esimerkkimääritykset

Seuraavassa kuvassa näkyy päätilille 110200 kirjatut tapahtumat. Vihreät tapahtumat selvitettiin kirjanpitoon samana tilikautena eikä niitä tarvitse muuttaa. Punaiset tapahtumat on selvitettiin kirjanpitoon, mutta niiden tapahtumapäivät ovat eri tilikausilla. Nämä tapahtumat on tunnistettava ja tapahtuman selvitys on ehkä palautettava.

![Kirjatut kirjanpitotapahtumat](./media/excel.png)

## <a name="example"></a>Esimerkki

Jos organisaatio haluaa käyttää **Tietoja**-ominaisuutta tilikauden 2022 tilikauden lopetuksen suorittamisen jälkeen, toimi seuraavasti.

> [!NOTE]
> Tilikauden 2022 ja aiempien tilikausien tilikauden lopetus on suoritettava uudelleen vain, jos tilikaudelle 2022 tai aiemmille tilikausille kirjataan uusia tapahtumia. Seuraavalla tavalla toimittaessa uusi tapahtumia ei kirjata vuodelle 2022. Siksi tilivuoden lopetusta ei tarvitse suorittaa uudelleen.
>
> Eri tilikausille selvitetyt kirjanpitotapahtumat voivat jäädä kirjanpitoon selvitetyiksi, jos niitä ei ole selvitetty vuonna 2022 tai jälkeen kirjatun tapahtuman perusteella. Jos tapahtumat on selvitetty esimerkiksi vuosina 2019 ja 2020, ne voivat jäädä selvitetyiksi.

1. Suorita vuoden 2022 tilikauden lopetus siten, että **Tietoja**-ominaisuus ei ole otettu käyttöön.
2. Määritä kaikki tapahtumat, jotka kirjattiin muille tilikausille mutta selvitettiin vuodelle 2023 (seuraavalle lopetettavalle tilikaudelle) kirjattujen tapahtumien perusteella.

    > [!NOTE]
    > Vuoden 2021 tapahtumilla, jotka selvitettiin vuoden 2022 tapahtumien perusteella, ei ole merkitystä, koska vuoden 2022 tilikausi on jo suljettu. Nämä tapahtuvat voivat jäädä selvitetyiksi.

    1. Valitse **Tapahtuman selvitykset** -sivulla **Tarkista vuosien väliset tilitykset**.
    2. Valitse tilikausi 2023, joka on seuraava tilikausi, jonka tilikauden lopetusprosessi halutaan suorittaa.
    3. Valitse **Taloushallinnon dimensioyhdistelmä** -kenttään arvo näyttämään kirjanpitotilillä tarkasteltavat taloushallinnon dimensiot. Päätili näytetään aina, myös silloin jos se ei sisälly valittuun dimensioyhdistelmään.
    4. Valitse **Näytä tapahtumat**.

    Kyselysivu näyttää kaikki sellaiset muiden tilikausien tapahtumat, jotka selvitettiin vuonna 2023 kirjattujen tapahtumien perusteella.

    ![Vuoden 2023 vuosien väliset selvitykset](./media/2023-cross-settlement.png)

3. Tee ruudukossa valinta ja pidä se valittuna (tai valitse hiiren kakkospainikkeella) ja valitse sitten **Vie kaikki rivit**. Näillä riveillä on kaikki tapahtumat, joiden selvitykset on peruttava vuoden 2022 tapahtumissa, ennen kuin seuraavan vuoden (2023) tilikauden lopetus voidaan suorittaa. Nämä tapahtumat on kirjattava muistiin.

    Kun kaikki vuoden 2022 eritellyt tapahtumat on viety Exceliin, tapahtumien selvityksen peruuttamisen voi aloittaa kyselysivun avulla.

4. Valitse kaikki tietueet ruudukossa ja valitse sitten **Kumoa merkittyjen tietueiden tilitys**. Kaikkien ruudukossa valittujen tapahtumien selvitys kumotaan.

    Kaksi varoistussanoma avautuu ja niiden avulla varmistetaan, että tapahtuman tiedot viedään Exceliin ennen tapahtumien selvityksen kumoamista. Jos kirjanpitotapahtuman selvitys kumotaan vahingossa ennen tietojen lähettämistä Exceliin, kumottua selvitystä ei voi palauttaa millään tavalla.

    ![Vuosien välisten selvitysten kumoaminen](./media/revert-settlement.png)

5. Etsi Excel-tietojen avulla niiden vuoden 2022 tapahtumien kokonaissumma, jotka selvitettiin vuoden 2023 tapahtumiin. Tässä esimerkissä vuoden 2023 tapahtumien summa on 700 $.
6. Jaa vuoden 2022 alkusaldo kahdeksi summaksi kirjaamalla oikaiseva yleinen kirjauskansio: osa summasta on selvitettiin tilikauden 2022 tapahtuman perusteella ja osaa summasta ei ole vielä selvitetty vuonna 2023.

    - **Alkusaldon edelliseen vuoteen selvitetty osa:** ensimmäinen summa on 700 $, joka perustuu vuosien 2021 ja 2022 selvitettyihin summiin.
    - **Alkusaldon osa, jota ei selvitetty edelliseen vuoteen:** Toinen summa alkusaldon ja selvitetyn summan, 700 $, välinen erotus. Jäljellä oleva summa on 1 700 $–700 $ = 1 000 $.

    Tällä tavoin vuoden 2023 tapahtumat voidaan selvittää sen 700 $:n perusteella, joka selvitettiin alun perin vuoden 2022 tapahtuman perusteella. Tämä vaihe on pakollinen, koska tapahtuman selvitys ei salli osittaisia selvityksiä.

    1. Siirry yleiseen kirjauskansioon ja kirjaa oikaisu. Organisaation on päätettävä käytettävä tapahtumapäivä vuoden 2023 avoimien kausien perusteella.
    2. **Älä salli manuaalista määritystä** -parametri on ehkä poistettava väliaikaisesti käytöstä **Päätili**-sivulla. Oikaisua ei kirjata, jos päätili ei salli manuaalista määritystä.

    ![Oikaisevan yleisen kirjauskansion kirjaaminen](./media/no-manual4.png)

7. Tapahtumat, joiden selvitys on kumottu, voidaan nyt selvittää uudelleen. Palaa **Tapahtuman selvitykset** -sivulle ja rajoita päivämääräalueeksi 1.1.–31.12.2023. Etsi sitten Exceliin vietyjen eriteltyjen tapahtumien avulla tapahtumat, jotka on kirjattava uudelleen. Seuraavassa kuvassa on nyt käytössä olevat tapahtumat, joiden selvitykset on kumottu.

    ![Vuoden 2023 selvittämättömät tapahtumat](./media/2023-unsettled5.png)

    - Alkusaldo 1 700 $ voidaan selvittää oikaisun -1 700 $ perusteella.
    - Eritellyt tapahtumat, joiden -700 $:n selvitys kumottiin, voidaan nyt selvittää 700,00 $:n oikaisun perusteella.

8. Ota **Tietoja**-ominaisuus käyttöön. Tilikauden lopetus voidaan nyt suorittaa.

    - Ennen vuoden 2023 tilikauden lopetusta kannattaa harkita **Säilytä tiedot** -vaihtoehdon valitsemista kaikkiin tasetileihin tapahtuman selvityksen määrityksissä. Lisätietoja on kohdassa [Tietoja kirjanpidon selvityksestä ja tilinpäätöksestä](awareness-between-ledger-settlement-year-end-close.md).
    - Jos tapahtumia on silti selvitettynä tilikausien välillä, kun vuoden 2023 tilikauden lopetus aloitetaan, tilikauden lopetusprosessi ilmoittaa siitä heti. Tämä on mahdollista, jos käyttäjät selvittivät tapahtumia tilikausien välillä ennen **Tietoja**-ominaisuuden ottamista käyttöön.
    - Jos vuoden 2022 ja 2023 tapahtumia on edelleen selvitettynä, **Tietoja**-ominaisuus on poistettava uudelleen käytöstä ja kyseisten tapahtumien selvitys on sitten kumottava toistamalla edelliset vaiheet. Tämä on pakollista, sillä vuosi 2022 on lopetettu eikä lopetetun tilikauden tapahtumien selvitystä voi peruuttaa.

Kun vuoden 2022 tilikauden lopetus on suoritettu, **Tietoja**-ominaisuus voidaan jättää jatkossa käyttöönotetuksi.
