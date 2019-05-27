---
title: Taloushallinnon dimensiot ja kirjaaminen
description: Tilikarttaa suunniteltaessa ja määritettäessä on mietittävä, miten eri komponentit toimivat yhdessä, kun kirjaat asiakirjan tai kirjauskansion. Näitä komponentteja ovat tilirakenteet, lisäsäännöt sekä täsmäyttävä ja kiinteä dimensio. Tässä ohjeaiheessa kerrotaan, mitä kukin komponentti tarkoittaa ja miten komponentit toimivat yhdessä.
author: aprilolson
manager: AnnBe
ms.date: 08/04/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerChartofAccounts,DimensionDetails
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 89bc6f1f01f77dac4c24419705737783b07e4ac7
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/15/2019
ms.locfileid: "1554756"
---
# <a name="financial-dimensions-and-posting"></a>Taloushallinnon dimensiot ja kirjaaminen 

[!include [banner](../includes/banner.md)]

Tilikarttaa suunniteltaessa ja määritettäessä on mietittävä, miten eri komponentit toimivat yhdessä, kun kirjaat asiakirjan tai kirjauskansion. Näitä komponentteja ovat tilirakenteet, lisäsäännöt sekä täsmäyttävä ja kiinteä dimensio. Tässä ohjeaiheessa kerrotaan, mitä kukin komponentti tarkoittaa ja miten komponentit toimivat yhdessä.

## <a name="chart-of-accounts-and-financial-dimension-components"></a>Tilikartan ja taloushallinnon dimension komponentit

Microsoft Dynamics 365 for Finance and Operationsissa on monipuolinen sääntöihin perustuva järjestelmä kelvollisten päätilien ja taloushallinnon dimensioarvojen yhdistelmien määrittämiseen. Tässä osassa esitellään lyhyesti kunkin komponentin toiminnot ja selitetään, missä komponentti sijaitsee.

### <a name="account-structures"></a>Tilirakenteet

Tilirakenne on pakko luoda kirjanpitoa määritettäessä. Vähintään yksi tilirakenne on määritettävä ja aktivoitava, ja se on määritettävä kirjanpitoon. Tilirakenteessa on oltava päätili. Voit määrittää segmentit yrityksen kannalta toimivimpaan järjestykseen. Kun päätili on määritetty, järjestelmä voi määrittää käytettävän tilirakenteen. Päätilin sijoittaminen tilirakenteessa ensimmäiseksi tai rakenteen yläosaan auttaa rajoittamaan arvoja. Se myös auttaa järjestelmää käyttämään viimeisintä tunnettua kelvollista arvo oletusarvona. Tilirakenteessa voi olla enintään 10 taloushallinnon lisädimensioita. Tilirakenne määrittää, mitä dimensioarvoja saa käyttää yhdessä muiden arvojen kanssa. Se määrittää myös, onko dimensioarvo annettava.

### <a name="advanced-rules"></a>Lisäsäännöt

Lisäsäännöt on valinnainen komponentti tilikarttaa määritettäessä. Voit lisätä tilirakenteeseen haluamasi määrän lisäsääntöjä. Lisäsääntöjä käytetään usein käsittelemään skenaarioita, joissa ylimääräisiä taloushallinnon dimensioita on seurattava, kun tietyt ehdot täyttyvät. Jos esimerkiksi käytät jos Matkakulut-tiliä, haluat ehkä seurata myös lisätietoja, kuten tapahtumaa, johon työntekijä matkustaa. Jos lisäsääntöjä on useita, niitä käytetään säännön nimeen perustuvassa aakkosjärjestyksessä. Säännön lisäämiä segmenttejä voi käyttää vasta tilirakenteen segmenttien jälkeen.

### <a name="balancing-dimension"></a>Täsmäytysdimensio

Vaihtoehtoisesti voit täsmäyttävän taloushallinnon dimension. Voit määrittää **Kirjanpito**-sivulla täsmäytettävän taloushallinnon dimension. Kun kyseiseen taloushallinnon dimensioon kirjataan sitten tapahtumia, järjestelmä luo ja kirjaa automaattisesti merkinnät, jotka täsmäyttävät taloushallinnon dimension.

### <a name="defaultfixed-financial-dimensions-on-the-main-account"></a>Päätilin oletusarvoiset tai kiinteät taloushallinnon dimensiot.

Oletusdimensiot voidaan saadaan useista lähteistä, kuten päätietueista (esimerkiksi asiakkaan tai toimittajan tietuetuista), asiakirjan otsikoista ja päätilistä. Tässä ohjeaiheessa käsitellään lähinnä yrityksen päätilin oletusdimensioita. Voit määrittää, onko kunkin sellaisen taloushallinnon dimension päätilin arvona **Ei kiinnitetty** tai **Kiinteä**, jota käytetään kaikissa kirjanpidon tilirakenteissa. Jos taloushallinnon dimension on **Ei kiinnitetty**, se käyttää oletusarvoa mutta kyseinen arvo voidaan korvata. Tämä toiminto koskee kaikkia järjestelmän oletusarvoja – myös päätietueista saatavia oletusarvoja. Jos taloushallinnon arvoksi on valittu **Kiinteä**, kyseistä arvoa käytetään aina riippumatta siitä, saatiinko se jostain oletusarvona vai antoiko käyttäjä sen.

## <a name="order-in-which-default-dimensions-are-applied-during-posting"></a>Kirjauksen aikana käytettävä oletusdimensioiden järjestys

Usein kysytään, missä järjestyksessä eri komponentit suoritetaan. Dimensioiden käyttöjärjestys on tärkeä tietää, sillä se vaikuttaa tapaan, jossa määritys tehdään.

> [!NOTE]
> Nämä tiedot koskevat vain sovelluksen oletusdimensioiden käyttöä. Jos tuot tietoja Microsoft Excelin tai Data Management Frameworkin avulla, toiminta on erilainen.

### <a name="example-1"></a>Esimerkki 1

**Tilirakenne**

| Päätili            | Liiketoimintayksikkö           | Osasto              | Kustannuspaikka             |
|-------------------------|-------------------------|-------------------------|-------------------------|
| Kaikki arvot ovat sallittuja. | Kaikki arvot ovat sallittuja. | Kaikki arvot ovat sallittuja. | Kaikki arvot ovat sallittuja. |

**Päätili**

| Päätili | Nimi          | Oikeushenkilö | Osasto                                 |
|--------------|---------------|--------------|--------------------------------------------|
| 401100       | Tuotemyynti | USMF         | Kiinteä – 022 Myynti- ja markkinointiosasto |

Seuraavassa kuvassa on kiinteä oletusdimensio, joka on määritetty päätilillä 401100.

[![Taloushallinnon oletusdimensiot](./media/default-dimensions.png)](./media/default-dimensions.png)

Tässä yksinkertaisessa esimerkissä lisätään kirjauskansio, jossa Osasto-dimensio on määritetty käyttämään oletusarvoa **023** (Toiminnot). Kirjapitotili annetaan ja kirjataan. Seuraavassa kuvassa on oletusarvoinen taloushallinnon dimension kirjanpidon otsikossa.

[![Yleiset kirjauskansiot](./media/general-journal.png)](./media/general-journal.png)

Kirjauskansion otsikon oletusdimensio aiheuttaa sen, että osastoa 023 käytetään oletusarvoisesti myyntitilirivillä. Seuraavassa kuvassa on kirjauskansiorivi, jossa on käytetty otsikon oletusdimension arvoa **023**.

[![Kirjaustosite](./media/journal-voucher.png)](./media/journal-voucher.png)

Riviä kirjatessa käytetään kuitenkin kiinteää dimensiota ja rivi kirjataan osastolle 022. Seuraavassa kuvassa on kirjattu tosite, jossa kiinteää dimensiota käytetään myyntitilille.

[![Tositetapahtumat](./media/voucher-transactions.png)](./media/voucher-transactions.png)

### <a name="example-2"></a>Esimerkki 2

Tässä esimerkissä käytetään samoja asetuksia kuin ensimmäisessä esimerkissä. Nyt kuitenkin lisätään toinen komponentti ja käytetään Osasto-dimensiota täsmäyttävänä dimensiona. Seuraavassa kuvassa **Osasto** on määritetty USMF-kirjanpidon täsmäyttäväksi taloushallinnon dimensioksi.

[![Kirjanpito](./media/ledger.png)](./media/ledger.png)

Kun käytetään samoja kirjauskansion otsikon asetuksia ja sama tapahtuma kirjataan, käytetään ensin kiinteää dimensiota. Tämän jälkeen käytetään täsmäytyslogiikkaa varmistamaan, että jokaisella osastolla on täsmätty merkintä. Seuraavassa kuvassa on täsmäytysmerkinnän sisältävät tositetapahtumat, kun kiinteä dimensiota on käytetty.

[![Tositetapahtumat](./media/voucher-transactions2.png)](./media/voucher-transactions2.png)

### <a name="example-3"></a>Esimerkki 3

Tässä esimerkissä lisätään lisäsääntö. Lisäsääntö määrittää, että myyntitiliä 401100 ja osastoa 022 (Myynti ja markkinointi) käytettäessä järjestelmän on seurattava Asiakas-nimistä lisäsegmenttiä.

Tämä esimerkki on tärkeä, siinä on mukana järjestys. Tilirakenne määritetään päätilin antamisen jälkeen. Jos viittaat tilirakenteen määritykseen, järjestelmä voi päätellä, että päätili, liiketoimintayksikkö, osasto ja kustannuspaikka tarvitaan. Tässä vaiheessa lisäsääntö ei ole käynnistynyt, koska kiinteitä dimensioita ei käytetä, ennen kuin oletusdimensioita on käytetty kirjauskansiotositteeseen kirjauksen aikana. Asiakas-segmentti ei näy seuraavassa kuvassa, koska lisäsäännön ehdot eivät täyttyneet.

[![Kirjanpitotili](./media/drop-down.png)](./media/drop-down.png)

Kirjaus ei onnistu, koska kiinteää dimensiota käytettiin prosessin lopussa. Dimension oikeellisuustarkistus määrittää, että Asiakas-segmenttiä tarvitaan, jos päätili on 401100 ja osasto 022. Kirjausta ei voi tehdä oikeellisuustarkistusvirheen vuoksi. Seuraavassa kuvassa on sanoma, joka avautuu, dimension oikeellisuustarkistus määrittää, että Asiakas on pakollinen segmentti.

[![Sanoman tiedot](./media/message.png)](./media/message.png)

Tässä esimerkissä oletusarvo on korvattava siten, että lisäsääntö käynnistyy ja voit antaa Asiakas-segmentin. Tätä ratkaisua ei kuitenkaan voi aina käyttää, ja osa käyttäjistä ei ole edes tietoinen kirjaussäännöistä. Tämän vuoksi on tärkeää, että tiedät tilikarttaa määritettäessä, missä järjestyksessä oletusdimensioita käytetään.

Jotta tämän esimerkin tavoite saavutettaisiin, määritystä voi muuttaa eri tavoin. Voit esimerkiksi luoda uuden myyntitilien tilirakenteen ja sisällyttää Asiakas-segmentin rakenteeseen. Voit myös lisätä rivejä aiemmin luotu tiilirakenteeseen sekä määrittää päätilin ja voimassa olevat osaston arvot. Lisäksi asiakkaan lisärakenteessa on ehkä syytä olla erillinen myyntitilien tilirakenne, jossa on Asiakas-segmentti.

## <a name="additional-resources"></a>Lisäresurssit 

Osa seuraavista resursseita viittaa Finance and Operationsin aiempiin versioihin. Suuri osa sovelluksen oletusdimensioita ja monia käsitteitä koskevat tiedot ovat kuitenkin samoja kuin aiemmassa versiossa, ja viittaukset ovat edelleen käyttökelpoisia.

[Yksiköiden välisen kirjanpidon tasapainotetut kirjauskansiot](example-balanced-journals-interunit-accounting.md)

[Tilikartan suunnittelu](plan-chart-of-accounts.md) 

[Tilikartan suunnitteleminen AX 2012 -blogissa](https://blogs.msdn.microsoft.com/axsa/2014/06/12/planning-your-chart-of-accounts-in-ax-2012-part-1-of-7/) – tämä linkki avaa 7-osaisen sarjan 1. osan.

[Dimension oletusarvot kirjanpidollisissa jaoissa](https://blogs.msdn.microsoft.com/ax_gfm_framework_team_blog/2013/12/16/dimension-defaulting-in-accounting-distributions-part-1-introduction/)

[Dimension oletusarvot dimensiokehyksessä](https://blogs.msdn.microsoft.com/ax_gfm_framework_team_blog/2014/09/)
