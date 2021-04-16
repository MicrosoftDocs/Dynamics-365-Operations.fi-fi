---
title: Ttuote- ja asiakashaku myyntipisteessä (POS)
description: Tämä ohjeaihe sisältää yleiskatsauksen parannuksista, jotka on tehty Dynamics 365 Commercen tuote- ja asiakashakuihin.
author: ShalabhjainMSFT
ms.date: 03/10/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.custom: 141393
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: Retail April 2017 update
ms.openlocfilehash: 1392b767815722c17b1cc72d27fe2bb8a7c32281
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5796363"
---
# <a name="product-search-and-customer-search-in-the-point-of-sale-pos"></a>Ttuote- ja asiakashaku myyntipisteessä (POS)

[!include [banner](includes/banner.md)]

Modern Point of Sale (MPOS) ja pilvimyyntipiste (CPOS) sisältävät helppokäyttöisen tuotteiden ja asiakkaiden hakutoiminnon. Koska hakukenttä on aina näkyvissä MPOS- ja CPOS-ikkunoiden yläosassa, työntekijät voivat hakea nopeasti tuotteita ja asiakkaita.

Työtekijät voivat hakea tuotteita nykyiseen myymälään liitetyistä valikoimista ja luetteloista. He voivat hakea tuotteita myös yrityksen muihin myymälöihin liitetyistä valikoimista ja luetteloista. Tämän ansiosta kassalta voi myydä ja palauttaa tuotteita, jotka eivät kuulu myymälän valikoimaan. Työntekijät voivat hakea samalla tavoin asiakkaita, jotka on liitetty joko nykyiseen myymälään tai mihin tahansa muuhun yrityksen myymälään. Lisäksi työntekijät voivat hakea asiakkaita, jotka on liitetty ylätason organisaation toiseen yritykseen.

## <a name="product-search"></a>Tuotehaku

Tuotehaku tehdään oletusarvoisesti myymälän valikoimassa. Tällaista hakua kutsutaan *paikalliseksi tuotehauksi*. Työntekijät voivat kuitenkin vaihtaa hakuluettelon mihin tahansa nykyisen myymälän luetteloon tai hakea toisesta myymälästä. Tällaista hakua kutsutaan *tuotteen etähauksi*. Voit vaihtaa luettelon valitsemalla **Luokat**-painikkeen sivun vasemmasta laidasta. Valitse esiin tulevan ruudun ylälaidasta **Vaihda luettelo** -painike ja valitse sitten luettelo, jota haluat selata. Järjestelmä tuotteet valitusta luettelosta.

Työntekijät voivat valita minkä tahansa myymälän tai hakea tuotteita kaikista myymälöistä helposti **Vaihda luettelo** -sivulla.

![Luettelon muuttaminen](./media/Changecatalog.png "Luettelon muuttaminen")

Paikallinen tuotehaku kohdistuu seuraaviin tuotteen ominaisuuksiin:

- Tuotetunnus
- Tuotteen nimi
- kuvaus
- Dimensiot
- Viivakoodi
- Hae nimellä

### <a name="additional-local-product-search-capabilities"></a>Paikalliset tuotteiden lisähakutoiminnot

- Useita sanoja käytettäessä (eli hakuehtoja käytettäessä) jälleenmyyjät voivat määrittää, sisältyykö hakutuloksiin kohteita, jotka vastaavat *mitä tahansa* hakuehtoja vai kohteita, jotka vastaavat *kaikkia* hakuehtoja. Tämän toiminnon asetus on myyntipisteen toimintoprofiilin uudessa **Tuotehaku**-ryhmässä. Oletusarvo on **Kohdista mikä tahansa hakusana**. Tämä asetus on suositeltu asetus. **Kohdista mikä tahansa hakusana**-asetusta käytettäessä tulokseksi palautetaan kaikki tuotteet, jotka vastaavat osittain tai kokonaan vähintään yhtä hakuehtoa. Nämä tulokset järjestetään automaattisesti nousevaan järjestykseen siten, että tuotteet, jotka vastaavat parhaiten avainsanoja (kokonaan tai osittain), ovat ensimmäisenä.

    **Kohdista kaikki hakusanat** -asetus palauttaa vain tuotteita, jotka vastaavat kaikkia hakusanoja (kokonaan tai osittain). Tästä asetuksesta on hyötyä, kun tuotenimet ovat pitkiä ja työntekijät haluavat rajoitetumman joukon hakutuloksia. Näillä hauilla on kuitenkin kaksi rajoituista:

    - Haku tehdään yksittäisiin tuoteominaisuuksiin. Haku palauttaa esimerkiksi vain tuotteita, jolla on vähintään yksi tuoteominaisuus, joka sisältää kaikki hakusanat.
    - Haku ei koske dimensioita.

- Vähittäismyyjät voivat määrittää tuotehaun näyttämään hakuehdotuksia käyttäjien kirjoittaessa tuotenimiä. Tämän toiminnon uusi asetus on myyntipisteen toimintoprofiilin uudessa **Tuotehaku**-ryhmässä. Asetuksen nimi on **Näytä hakuehdotukset kirjoittamisen aikana**. Työntekijät voivat käyttää tätä toimintoa löytämään etsimänsä tuotteet nopeasti, koska koko tuotenimeä ei tarvitse kirjoittaa.
- Tuotehaun algoritmi etsii hakusanoja nyt myös tuotteen **Hakunimi**-ominaisuudesta.

![Tuote-ehdotukset](./media/Productsuggestions.png "Tuote-ehdotukset")

## <a name="customer-search"></a>Asiakashaku

Asiakashakua käytetään asiakkaiden etsimiseen erilaisissa tarkoituksissa. Kassat voivat esimerkiksi haluta nähdä asiakkaan toivelistan tai ostohistorian, tai lisätä asiakkaan tapahtumaan. Hakualgoritmi vertaa hakuehtoja seuraavissa asiakkaan ominaisuuksissa oleviin arvoihin:

- Nimi
- Sähköpostiosoite
- Puhelinnumero
- Kanta-asiakaskortin numero
- Osoite
- Tilinumero

Näistä ominaisuuksista nimi on monipuolisin vaihtoehto useiden avainsanojen hauissa, sillä algoritmi palauttaa kaikki haettuja avainsanoja vastaavat asiakkaat. Useimpia hakusanoja vastaavat asiakkaat näkyvät ensimmäisenä tuloksissa. Tämä auttaa kassoja tilanteissa, joissa he tekevät hakuja kirjoittamalla koko nimen, mutta etu- ja sukunimi vaihtuivat tietojen syöttövaiheessa. Suorituskyvyn ylläpitämiseksi kaikki muut ominaisuudet kuitenkin säilyttävät avainsanojen järjestyksen. Jos haun avainsanojen järjestys ei vastaa järjestystä, jossa tiedot on tallennettu, tulosta ei tämän vuoksi palauteta.

Asiakashaut tehdään oletusarvon mukaan myymälään liitettyihin osoitekirjoihin. Tällaista hakua kutsutaan *paikalliseksi asiakashauksi*. Työntekijät voivat myös hakea asiakkaita kaikkialta. Toisin sanoen, asiakkaita voidaan etsiä yrityksen kaikista myymälöistä sekä muista yrityksistä. Tällaista hakua kutsutaan *asiakkaan etähauksi*.

Työntekijät voivat suorittaa yleisen haun valitsemalla **Suodata tuloksia** -painikkeen sivun alalaidasta ja valitsemalla sitten **Hae kaikista myymälöistä** -vaihtoehdon, alla olevan kuvan mukaisesti. Tässä tapauksessa hakutulokset eivät sisällä ainoastaan asiakkaita. Kaikki osapuolet, jotka ovat missä tahansa pääkonttorin osoitekirjassa, sisältyvät myös tuloksiin. Osapuolet ovat toimittajia, työntekijöitä, yhteyshenkilöitä ja kilpailijoita.

> [!NOTE]
> Asiakkaan etähaun hakusanan on oltava vähintään neljä merkkiä pitkä, jotta järjestelmä näyttää tuloksia.

Tuloksissa ei näytetä muiden yritysten asiakkaiden asiakastunnusta, koska näillä asiakkailla ei ole asiakastunnusta nykyisessä yrityksessä. Jos työntekijä kuitenkin avaa asiakkaan tietosivun, järjestelmä luo automaattisesti osapuolelle asiakastunnuksen ja liittää myymälän osoitekirjan asiakkaaseen. Tällöin asiakas näkyy myöhemmin tehtävissä paikallisissa hauissa.

![Globaali asiakashaku](./media/Globalcustomersearch.png "Globaali asiakashaku")

### <a name="additional-local-customer-search-capabilities"></a>Paikalliset asiakkaiden lisähakutoiminnot

Kun käyttäjä hakee puhelinnumeroa, järjestelmä ohittaa erikoismerkit (kuten välilyönnit, tavuviivat ja sulkeet) jotka on mahdollisesti lisätty asiakasta luotaessa. Kassan ei tämän vuoksi tarvitse välittää puhelinnumeron muodosta hakujen yhteydessä. Jos esimerkiksi asiakkaan puhelinnumeroksi on tallennettu **123-456-7890**, kassa voi etsiä asiakkaan kirjoittamalla **1234567890**. Haun voi tehdä myös kirjoittamalla puhelinnumeron muutaman ensimmäisen numeron.

> [!NOTE]
> Asiakkaalla voi olla useita puhelinnumeroita ja sähköpostiosoitteita. Asiakkaan hakualgoritmi hakee myös näiden toissijaisten sähköpostiosoitteiden ja puhelinnumeroista. Asiakkaan hakutulossivulla näytetään kuitenkin vain ensisijainen sähköpostiosoite ja puhelinnumero. Tämä saattaa aiheuttaa sekaannusta, koska palautetut asiakkaan tulokset eivät näytä haettua sähköpostiosoitetta tai puhelinnumeroa. Tulevissa julkaisuissa aiomme parantaa asiakkaan hakutulosnäyttöä näiden tietojen saamiseksi.

Perinteinen asiakashaku voi kestää kauan, koska haku kohdistuu useisiin kenttiin. Kassat voivat sen sijaan tehdä haun asiakkaan yhden ominaisuuden perusteella käyttämällä esimerkiksi nimeä, sähköpostiosoitetta tai puhelinnumeroa. Asiakkaan hakualgoritmin käyttämiä ominaisuuksia kutsutaan *asiakashaun ehdoiksi*. Järjestelmänvalvoja voi määrittää kätevästi vähintään yhden hakuehdon myyntipisteessä näkyväksi pikavalinnaksi. Koska haussa käytetään vain yhtä ehtoa, vain hakua vastaavat tulokset näytetään. Tämän vuoksi haku on tehokkaampi kuin tavallinen asiakashaku. Seuraavassa kuvassa on myyntipisteen asiakashaun pikavalinnat.

![Asiakashaun pikakuvakkeet](./media/SearchShortcutsPOS.png "Asiakashaun pikakuvakkeet")

Järjestelmänvalvoja voi määrittää hakuehdot pikavalinnoiksi avaamalla **Commercen parametrit** -sivun Commercessa ja valitsemalla sitten **Myyntipisteen hakuehdot** -välilehdessä kaikki pikavalintoina näytettävät ehdot.

![Määritä haun pikakuvakkeet](./media/ConfigureShortcutsAX.png "Määritä haun pikakuvakkeet")

> [!NOTE]
> Jos lisäät liian monta pikavalintaa, myyntipisteen hakuruudun avattava valikko muuttuu sekavaksi, mikä voi vaikuttaa työntekijän hakukokemukseen. Tämän vuoksi vain tarvittavat pikavalinnat kannattaa lisätä.

**Näyttöjärjestys**-kenttä määrittää, missä järjestyksessä pikavalinnat näytetään myyntipisteessä. Näytettävät ehdot ovat valmiita ominaisuuksia, joilla asiakashakualgoritmi hakee asiakkaita. Kumppanit voivat kuitenkin lisätä mukautettuja ominaisuuksia haun pikavalinnoiksi. Järjestelmänvalvoja voi lisätä mukautettuja ominaisuuksia haun pikavalinnoiksi laajentamalla asiakashaun hakuehdoissa käytettäviä laajennettavia valintalistoja ja merkitsemällä sitten kumppanin mukautetut ominaisuudet pikavalinnoiksi. Kumppanit vastaavat tuloksia etsivän koodin kirjoittamisesta, kun heidän mukautettuja pikavalintoja käytetään hauissa.

> [!NOTE]
> Valintalistaan lisättävä mukautettu ominaisuus ei vaikuta vakioasiakashaun algoritmiin. Asiakashakualgoritmi ei siis tee hakuja mukautetussa ominaisuudessa. Käyttäjät voivat käyttää mukautettua ominaisuutta haussa vain, jos kyseinen mukautettu ominaisuus on lisätty pikavalintoja tai jos oletushakualgoritmi on ohitettu.

Vähittäismyyjät voivat myös määrittää asiakashaun oletustilaksi myyntipisteessähakea **Hae kaikista myymälöistä**. Tämä määritys voi olla hyödyllinen tilanteissa, joissa myyntipisteen ulkopuolella luotuja asiakkaita on haettava heti (esimerkiksi ennen jakelutyön ajamista). Tätä varten vähittäismyyjän on otettava käyttöön myyntipisteen toimintoprofiilissa **Asiakkaan oletushakutila** -asetus. Kun sen arvona on **Kyllä**, jokainen asiakashakuyritys tekee sitten reaaliaikaisen kutsun pääkonttoriin.

Odottamattomat suorituskykyongelmien estämiseksi tämä määritys on piilotettu versioversiotestaukseen nimeltä **CUSTOMERSEARCH_ENABLE_DEFAULTSEARCH_FLIGHTING**. Tämän vuoksi **Asiakkaan oletushakutila** -asetuksen näyttäminen käyttöliittymässä edellyttää, että jälleenmyyjä luo tukipalvelupyynnön käyttäjän hyväksyntätestaus- ja tuotantoympäristöjä varten. Kun pyyntö on vastaanotettu, kehitysryhmä varmistaa yhteistyössä vähittäismyyjän kanssa, että tämän testaus tapahtuu muussa kuin tuotantoympäristössä, sillä tällä tavoin voidaan arvioida suorituskyly ja ottaa käyttöön mahdollisesti tarvittavat optimoinnit.

## <a name="cloud-powered-customer-search"></a>Pilvipohjainen asiakashaku

Azure Cognitive Search -palvelua käyttävän asiakkaan hakuominaisuuden julkinen esiversio on julkaistu osana Commerce 10.0.18 -versiota. Suorituskyvyn parannusten lisäksi palvelun käyttäjät hyötyvät myös tarkennuksista ja parannuksista. Suorituskykyyn liittyvät parannukset ovat erityisen selkeitä, kun myyntipisteen yleistä hakutoimintoa (Hae kaikista myymälöistä) käytetään. Tämä johtuu siitä, että hakutulokset haetaan Azure-hakuindeksistä sen sijaan että tiedot kyseltäisiin Commerce headquartersista. 

### <a name="enable-the-cloud-powered-search-feature"></a>Ota käyttöön pilvipohjainen hakutoiminto

> [!NOTE]
> On tarpeen päivittää sekä Commerce headquarters että Commerce Scale Unit versioksi 10.0.18. Myyntipisteen päivitystä ei tarvita.

Jos haluat ottaa käyttöön pilvipohjaisen hakutoiminnon Commerce headquarters -sovelluksessa, toimi seuraavasti.

1. Valitse **Järjestelmänvalvoja \> Työtilat \> Ominaisuuksien hallinta**.
1. Etsi ja valitse **(Esiversio) Pilvipohjainen asiakashaku** -toiminto ja valitse sitten **Ota käyttöön nyt**.
1. Siirry kohtaan **Retail ja Commerce > Headquartersin asetukset > Commerce-ajastus > Alusta Commerce-ajoitus** ja valitse **OK** näyttäksesi uuden **1010_CustomerSearch**-työn **Jakeluaikataulu**-lomakkeessa.
1. Mene kohtaan **Retail ja Commerce > Retail ja Commerce IT > Jakeluaikataulu**.
1. Suorita **1010_CustomerSearch**-työ. Tämä työ julkaisee päivämäärän Azure-hakuindeksiin. Kun indeksi on julkaistu, työn tilaksi tulee **Käytössä**.
1. Kun **1010_CustomerSearch**-työn tila on **Käytössä**, suorita **1110 - Yleinen määritys** -työ päivittääksesi myyntipistekanavat uudelle ominaisuudelle **ominaisuuksien hallinnassa**.
1. Suorita sen jälkeen **1010_CustomerSearch**-työ säännöllisesti lähettääksesi asiakaspäivitykset hakuindeksiin.

> [!NOTE]
> Ensimmäisessä indeksin julkaisussa **1010_CustomerSearch**-työ voi kestää joitakin tunteja, sillä se lähettää kaikki asiakastietueet Azure-hakuindeksiin. Seuraavien päivitysten pitäisi kestää muutaman minuutin. Sen aikajakson aikana, jolloin pilvipalveluun perustuva hakutoiminto on käytössä, mutta indeksin julkaisu ei ole vielä valmis, asiakashaun oletusarvo myyntipisteessä on olemassa oleva SQL-pohjainen haku. Näin varmistetaan, että myymälän toimintoihin ei tule keskeytyksiä.

### <a name="functional-differences-from-the-existing-search"></a>Toiminnalliset erot nykyiseen hakuun

Seuraavassa luettelossa kerrotaan, miten pilvipohjainen asiakashakutoiminto eroaa olemassa olevasta hakutoiminnosta. 

- Commerce headquartersissa luodut ja muokatut asiakkaat lähetetään Azure-hakuindeksiin, kun **1010_CustomerSearch**-työ suoritetaan. Näiden päivitysten tekeminen indeksiin kestää vähintään 15–20 minuuttia. Myyntipisteen käyttäjät voivat etsiä uusia asiakkaita (tai etsiä päivitettyjen tietojen perusteella) noin 15-20 minuuttia Commerce headquartersin päivitysten jälkeen. Jos liiketoimintaprosessi edellyttää, että Commerce headquarters -sovelluksessa luodut asiakkaat ovat heti haettavissa myyntipisteessä, tämä ei ehkä ole oikea palvelu tarpeisiisi.
- Uudet myyntipisteessä luodut asiakkaat lähetetään Azure-hakuindeksiin Commerce Scale Unitista, ja he ovat heti haettavissa mistä tahansa myymälästä. Jos asynkroninen asiakkaan luontiominaisuus on kuitenkin käytössä, uusia asiakastietueita ei julkaista Commerce Scale Unitista Azure-hakuindeksiin, eikä niitä voi hakea myyntipisteestä, ennen kuin asiakastiedot synkronoidaan Commerce headquarters -sovelluksen kanssa ja asiakastunnukset luodaan asynkronisille asiakkaille. Tämän jälkeen **1010_CustomerSearch**-työ voi lähettää asynkroniset asiakastietueet Azure-hakuindeksiin. Keskimäärin kestää noin 30 minuuttia, kun uusia asynkronisia asiakkaita voidaan hakea myyntipisteessä. Tässä arviossa oletetaan, että **1010_CustomerSearch**-työ, **P-työ** ja **Synkronoi asiakkaat ja yrityskumppanit asynkronisesta tilasta** -työ suoritetaan 15 minuutin välein.
- Pilvipohjainen haku etsii myös asiakkaiden toissijaisia sähköpostiosoitteita ja puhelinnumeroita, mutta tällä hetkellä asiakashakutuloksissa näkyy vain asiakkaiden ensisijainen puhelinnumero ja ensisijainen sähköpostiosoite. Aluksi saattaa vaikuttaa siltä, että hakutuloksissa on asiaan liittymättömiä tuloksia, mutta hakutuloksissa olevan asiakkaan toissijaisen sähköpostiosoitteen ja puhelinnumeron tarkistaminen voi auttaa varmistamaan, onko avainsanasta saatu hakutulos oikea vastaavuus. Sekaannuksen välttämiseksi on suunnitelmia parantaa hakutulossivua, jotta käyttäjät voivat helposti ymmärtää, miksi hakutulos palautettiin.
- Tässä palvelussa ei ole rajoitusta tehdä hakuja vähintään neljällä merkillä kuten yleishaussa ("Hae kaikista myymälöistä").

> [!NOTE]
> Azure Cognitive Search -palvelua käyttävä asiakshaku on ksaatavilla esiversiona vain rajoitetulla määrällä alueita. Asiakashakutoiminto *ei* ole käytettävissä seuraavilla alueilla:
> - Brasilia
> - Intia
> - Kanada
> - Iso-Britannia

[!INCLUDE[footer-include](../includes/footer-banner.md)]
