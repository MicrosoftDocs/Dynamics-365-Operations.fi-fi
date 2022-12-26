---
title: Tietoja kirjanpidon selvityksestä -toiminto ennen tilikauden lopetusta kyselysivua käyttämällä
description: Tässä artikkelissa käsitellään Tietoja kirjanpidon selvityksestä -toiminnon käyttämistä uuden kyselysivun avulla ennen kirjanpidon tilikauden lopetuksen suorittamista.
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
ms.openlocfilehash: b138d2d5e88ff7f2ca2240cf256a4938f55a5606
ms.sourcegitcommit: 9f3a60a583da21382a14f32ce146fc9ce03f2a09
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/15/2022
ms.locfileid: "9853135"
---
# <a name="awareness-between-ledger-settlement-feature-before-year-end-close-using-the-inquiry-page"></a>Tietoja kirjanpidon selvityksestä -toiminto ennen tilikauden lopetusta kyselysivua käyttämällä

**Tietoja kirjanpidon selvityksestä ja tilinpäätöksestä** -ominaisuuden (**Tietoja**-ominaisuuden) merkittävä muutos on se, että kirjanpidon selvitystä ei voi suorittaa tilikausien välillä. Tilikausien välinen rajoitus koskee vain tapahtuman selvitystä, ei siis ostoreskontran ja myyntireskontran selvityksiä.

Ennen **Tietoja**-ominaisuuden käyttöönottoa lopetettavassa tilikaudessa ei saa olla yhtään tilikausien välillä selvitettyä kirjanpitotapahtumaa. Niinpä sellaisten siihen tilikauteen kirjattujen tapahtumien, jonka tilikauden lopetusta suoritetaan, selvitys on peruutettava, jotka kirjattiin toiselle tilikaudelle. Tapahtumat voidaan sitten selvittää uudelleen saman tilikauden tapahtumien perusteella.

Tässä artikkelissa käsitellään vaiheita, joiden avulla tunnistetaan tilikausien välillä selvitetyt kirjanpitotapahtumat, peruutetaan niiden selvitys ja selvitetään ne uudelleen. Käytettävässä esimerkissä tilikausi 2021 on lopetettu ja tilikauden 2022 tilikauden lopetuksen suorittamista valmistellaan.

Microsoft Dynamics 365 Finance -versiosta 10.0.29 alkaen kirjanpitotapahtumat voidaan tunnistaa sekä niiden selvitys voidaan peruuttaa ja sitten selvittää uudelleen uudella kyselysivulla. Jos Financen versio 10.0.29 tai sitä uudempi versio ei ole käytössä, ohjeita kirjanpitotapahtumien tunnistamiseen sekä niiden selvityksen peruuttamiseen ja selvittämiseen uudelleen on seuraavissa artikkeleissa:

- [Tietoja kirjanpidon selvityksestä -toiminto ennen tilikauden lopetusta](ledger-settle-yec.md)
- [Tietoja kirjanpidon selvityksestä -toiminto tilikauden lopetuksen jälkeen](ledger-settle-yec-after.md)

Lisätietoja uudesta kyselyikkunasta on kohdassa [Tapahtuman selvityksen kysely](ledger-settlement-inquiry.md). 

## <a name="example-setup"></a>Esimerkkimääritykset

Seuraavassa kuvassa näkyy päätilille 110200 kirjatut tapahtumat. Vihreät tapahtumat selvitettiin kirjanpitoon samana tilikautena eikä niitä tarvitse muuttaa. Punaiset tapahtumat on selvitettiin kirjanpitoon, mutta niiden tapahtumapäivät ovat eri tilikausilla. Nämä tapahtumat on tunnistettava ja tapahtuman selvitys on ehkä palautettava.

![Kirjatut kirjanpitotapahtumat](./media/ledgersettlement.png)

## <a name="example"></a>Esimerkki

Jos organisaatio haluaa käyttää **Tietoja**-ominaisuutta ennen tilikauden 2022 tilikauden lopetuksen suorittamista, toimi seuraavasti.

> [!NOTE]
> Tilikauden 2021 ja aiempien tilikausien tilikauden lopetus on suoritettava uudelleen vain, jos tilikaudelle 2021 tai aiemmille tilikausille kirjataan uusia tapahtumia. Seuraavalla tavalla toimittaessa uusi tapahtumia ei kirjata vuodelle 2021. Siksi tilivuoden lopetusta ei tarvitse suorittaa uudelleen.
>
> Eri tilikausille selvitetyt kirjanpitotapahtumat voivat jäädä kirjanpitoon selvitetyiksi, jos niitä ei ole selvitetty vuonna 2022 (lopetettava tilikausi) tai jälkeen kirjatun tapahtuman perusteella. Jos tapahtumat on selvitetty esimerkiksi vuosina 2019 ja 2020, ne voivat jäädä selvitetyiksi.

1. **Älä** ota **Tietoja**-ominaisuutta käyttöön.
2. Valitse **Tapahtuman selvitykset** -sivulla **Tarkista vuosien väliset tilitykset**.
3. Määritä kaikki tapahtumat, jotka kirjattiin muille tilikausille mutta selvitettiin vuodelle 2022 kirjattujen tapahtumien perusteella.

    1. Valitse tilikausi 2022 eli tilikausi, jonka tilikauden lopetusprosessi halutaan suorittaa.
    2. Valitse **Taloushallinnon dimensioyhdistelmä** -kenttään arvo näyttämään kirjanpitotilillä tarkasteltavat taloushallinnon dimensiot. Päätili näytetään aina, myös silloin jos se ei sisälly valittuun dimensioyhdistelmään.
    3. Valitse **Näytä tapahtumat**.

    Kyselysivulla näkyy kaikkien kirjanpitotilien (vaikka ne eivät olisi enää tapahtuman selvityksen määrityksissä) kaikki sellaiset tapahtumat kaikilta muilta tilakausilta, jotka selvitettiin vuodelle 2022 kirjattujen tapahtumien perusteella. Näkyvissä on kolme kirjanpitotiliä.

    ![Vuoden 2022 vuosien väliset selvitykset](./media/review-cross-year.png)

3. Tee ruudukossa valinta ja pidä se valittuna (tai valitse hiiren kakkospainikkeella) ja valitse sitten **Vie kaikki rivit**. Näillä riveillä on kaikki tapahtumat, joiden selvitykset on peruttava vuoden 2022 tapahtumissa, ennen kuin tilikauden lopetus voidaan suorittaa. Tapahtumien oikeaa uudelleenselvittämistä varten tarvitaan eritelty tapahtumaluettelo.
4. Kirjaa muistiin tilikaudet, joihin tapahtumat kirjattiin. Tässä esimerkissä tapahtumia on vuosilla 2021 ja 2023.
5. Vaihda kyselysivulla tilakaudeksi 2021, joka on ensimmäinen vuoden 2022 tapahtumien perusteella selvitettyjä tapahtumia sisältävä tilikausi.
6. Suodata **Tapahtumapäivä**-sarakkeeseen vain tapahtumat, jotka kirjattiin vuodelle 2022. Nämä tapahtumat ovat eriteltyjä tapahtumia vuodelta 2022, ja ne selvitettiin vuoden 2021 tapahtumien perusteella.
7. Tee ruudukossa valinta ja pidä se valittuna (tai valitse hiiren kakkospainikkeella) ja valitse sitten **Vie kaikki rivit**.

    > [!IMPORTANT]
    > Seuraavissa vaiheissa näiden tapahtumien selvitys kumotaan ja sitten selvitetään uudelleen vuoden 2022 tapahtumien perusteella. Nämä tiedot on ehdottomasti tallennettava Exceliin.

    ![Vuoden 2021 vuosien väliset selvitykset](./media/review-cross-year.png)

8. Vaihda kyselysivulla tilakaudeksi 2023, joka on seuraava vuoden 2022 tapahtumien perusteella selvitettyjä tapahtumia sisältävä tilikausi. 
9. Suodata **Tapahtumapäivä**-sarakkeeseen vain tapahtumat, jotka kirjattiin vuodelle 2022. Nämä tapahtumat ovat eriteltyjä tapahtumia vuodelta 2023, ja ne selvitettiin vuoden 2022 tapahtumien perusteella. 
10. Tee ruudukossa valinta ja pidä se valittuna (tai valitse hiiren kakkospainikkeella) ja valitse sitten **Vie kaikki rivit**.

    > [!IMPORTANT]
    > Seuraavissa vaiheissa näiden tapahtumien selvitys kumotaan ja sitten selvitetään uudelleen vuoden 2022 tapahtumien perusteella. Nämä tiedot on ehdottomasti tallennettava Exceliin.

    ![Vuoden 2023 vuosien väliset selvitykset](./media/filter-transactions.png)

11. Toista edelliset vaiheet kunkin sellaisen tilikauden osalta, jossa tapahtumia on selvitetty vuoden 2022 tapahtumien perustella. Eritellyt tapahtumat on aina vietävä Exceliin.

    Kun kaikki vuosien 2021 ja 2023 eritellyt tapahtumat on viety Exceliin, tapahtumien selvityksen peruuttamisen voi aloittaa uuden kyselysivun avulla.

12. Muuta tilakaudeksi 2022.
13. Valitse kaikki tietueet ruudukossa ja valitse sitten **Kumoa merkittyjen tietueiden tilitys**. Kaikkien ruudukossa valittujen tapahtumien selvitys kumotaan.

    Kaksi varoistussanoma avautuu ja niiden avulla varmistetaan, että tapahtuman tiedot viedään Exceliin ennen tapahtumien selvityksen kumoamista. Jos kirjanpitotapahtuman selvitys kumotaan vahingossa ennen tietojen lähettämistä Exceliin, kumottua selvitystä ei voi palauttaa millään tavalla.

    ![Tapahtumien välisten selvitysten kumoaminen](./media/revert-unsettle.png)

14. Etsi Excel-tietojen avulla niiden vuosien 2021 ja 2023 tapahtumien kokonaissumma, jotka selvitettiin vuoden 2022 tapahtumien perusteella. Tässä esimerkissä vuoden 2021 tapahtumien summa on 525 $ ja vuoden 2023 summa 700 $.
15. Jaa vuoden 2022 alkusaldo kahdeksi summaksi kirjaamalla oikaiseva yleinen kirjauskansio: osa summasta on selvitettiin tilikaudelle 2021 ja osaa summasta ei ole vielä selvitetty vuodelle 2022.

    - **Alkusaldon edelliseen vuoteen selvitetty osa:** ensimmäinen summa on 525 $, joka perustuu vuosien 2021 ja 2022 selvitettyihin summiin.
    - **Alkusaldon osa, jota ei selvitetty edelliseen vuoteen:** Toinen summa alkusaldon ja selvitetyn summan, 525 $, välinen erotus. Jäljellä oleva summa on 1 025 $–525 $ = 500 $.

    Tällä tavoin vuoden 2022 tapahtumat voidaan selvittää sen 525 $:n perusteella, joka selvitettiin alun perin vuoden 2021 tapahtuman perusteella. Tämä vaihe on pakollinen, koska tapahtuman selvitys ei salli osittaisia selvityksiä.

    1. Siirry yleiseen kirjauskansioon ja kirjaa oikaisu. Organisaation on päätettävä käytettävä tapahtumapäivä avoimien kausien perusteella. Nämä tapahtumat on ehkä selvitetty käyttämällä tapahtumapäivänä vuoden 2022 tammikuuta tai helmikuuta, mutta oikaisu on ehkä kirjattava joulukuussa, jos se on ainoa avoin kausi.
    2. Tilin 110200 **Älä salli manuaalista määritystä** -parametri on ehkä poistettava väliaikaisesti käytöstä **Päätili**-sivulla. Oikaisua ei kirjata, jos päätili ei salli manuaalista määritystä.

    ![Oikaisevan yleisen kirjauskansion kirjaaminen](./media/not-post.png)

16. Tapahtumat, joiden selvitys on kumottu, voidaan nyt selvittää uudelleen. Palaa **Tapahtuman selvitykset** -sivulle, määritä päivämääräalueeksi 1.1.–31.12.2022 ja suodata päätili 110200. Etsi sitten Exceliin vietyjen eriteltyjen tapahtumien avulla tapahtumat, jotka on kirjattava uudelleen. Seuraavassa kuvassa on nyt käytössä olevat tapahtumat, joiden selvitykset on kumottu.

    ![Selvittämättömät tapahtumat](./media/updated-unsettled.png)

    - Alkusaldo 1 025 $ voidaan selvittää oikaisun -1 025 $ perusteella.
    - Eritellyt tapahtumat, joiden -400 $:n, -50 $:n ja -75 $:n selvitys peruutettiin, voidaan nyt selvittää 25 $:n oikaisun perusteella.

17. Ota **Tietoja**-ominaisuus käyttöön. Tilikauden lopetus voidaan nyt suorittaa.

    - Ennen tilikauden lopetusta kannattaa harkita **Säilytä tiedot** -vaihtoehdon valitsemista kaikkien tasetilien tapahtuman selvityksen määrityksissä. Lisätietoja on kohdassa [Tietoja kirjanpidon selvityksestä ja tilinpäätöksestä](awareness-between-ledger-settlement-year-end-close.md).
    - Jos tapahtumia on silti selvitettynä tilikausien välillä, kun vuoden 2022 tilikauden lopetus aloitetaan, tilikauden lopetusprosessi ilmoittaa siitä heti. Tämä on mahdollista, jos käyttäjät selvittivät tapahtumia tilikausien välillä sen jälkeen, kun edelliset vaiheet suoritettiin.
    - Jos vuoden 2021 ja 2022 tapahtumia on edelleen selvitettynä, **Tietoja**-ominaisuus on poistettava uudelleen käytöstä ja kyseisten tapahtumien selvitys on sitten kumottava toistamalla edelliset vaiheet. Tämä on pakollista, sillä vuosi 2021 on lopetettu eikä lopetetun tilikauden tapahtumien selvitystä voi peruuttaa.
    - Jos vuoden 2022 ja 2023 tapahtumia on edelleen selvitettynä, **Tietoja**-ominaisuutta ei tarvitse poistaa käytöstä. Koska vuosi 2022 ja 2023 ei ole lopetettu, tapahtumien selvitys voidaan peruuttaa edellisten vaiheiden mukaan.

18. Vuoden 2023 700 $:n tapahtuma voidaan selvittää vuoden 2023 alkusaldoiksi siirrettyjen eriteltyjen tapahtumien perusteella. Tapahtumaa ei selvitetä vuoden 2022 alkuperäisen tapahtuman perusteella.

Kun vuoden 2022 tilikauden lopetus on suoritettu, **Tietoja**-ominaisuus voidaan jättää jatkossa käyttöönotetuksi.
