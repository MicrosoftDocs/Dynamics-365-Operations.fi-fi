---
title: "Ttuote- ja asiakashaku myyntipisteessä (POS)"
description: "Tässä ohjeaiheessa on yleiskatsauksen parannuksista, jotka on tehty Microsoft Dynamics 365 for Retailin tuote- ja asiakashakuihin."
author: ShalabhjainMSFT
manager: AnnBe
ms.date: 03/28/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application user
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 141393
ms.assetid: 
ms.search.region: Global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: Retail April 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 5098fb3339403b6f2779dfe3bb7ef5c4ca78051f
ms.openlocfilehash: 50b0cec27e343b3b6aba464a04c9883160ab263a
ms.contentlocale: fi-fi
ms.lasthandoff: 08/08/2018

---

# <a name="product-search-and-customer-search-in-the-point-of-sale-pos"></a>Ttuote- ja asiakashaku myyntipisteessä (POS)

[!include [banner](includes/banner.md)]

Modern Point of Sale (MPOS) ja pilvimyyntipiste (CPOS) sisältävät helppokäyttöisen tuotteiden ja asiakkaiden hakutoiminnon. Koska hakukenttä on aina näkyvissä MPOS- ja CPOS-ikkunoiden yläosassa, työntekijät voivat hakea nopeasti tuotteita ja asiakkaita.

Työtekijät voivat hakea tuotteita nykyiseen myymälään liitetyistä valikoimista ja luetteloista. He voivat hakea tuotteita myös yrityksen muihin myymälöihin liitetyistä valikoimista ja luetteloista. Tämän ansiosta kassalta voi myydä ja palauttaa tuotteita, jotka eivät kuulu myymälän valikoimaan. Työntekijät voivat hakea samalla tavoin asiakkaita, jotka on liitetty joko nykyiseen myymälään tai mihin tahansa muuhun yrityksen myymälään. Lisäksi työntekijät voivat hakea asiakkaita, jotka on liitetty ylätason organisaation toiseen yritykseen.

## <a name="product-search"></a>Tuotehaku

Tuotehaku tehdään oletusarvoisesti myymälän valikoimassa. Tällaista hakua kutsutaan *paikalliseksi tuotehauksi*. Työntekijät voivat kuitenkin vaihtaa hakuluettelon mihin tahansa nykyisen myymälän luetteloon tai hakea toisesta myymälästä. Tällaista hakua kutsutaan *tuotteen etähauksi*. Voit vaihtaa luettelon valitsemalla **Luokat**-painikkeen sivun vasemmasta laidasta. Valitse esiin tulevan ruudun ylälaidasta **Vaihda luettelo** -painike ja valitse sitten luettelo, jota haluat selata. Järjestelmä tuotteet valitusta luettelosta.

Työntekijät voivat valita minkä tahansa myymälän tai hakea tuotteita kaikista myymälöistä helposti **Vaihda luettelo** -sivulla.

![Luettelon vaihtaminen](./media/Changecatalog.png "Luettelon vaihtaminen")
 
Paikallinen tuotehaku kohdistuu seuraaviin tuotteen ominaisuuksiin:

- Tuotenumero
- Tuotteen nimi
- kuvaus
- Dimensiot
- Viivakoodi
- Hakunimi

### <a name="enhancements-to-local-product-searches"></a>Paikallisten tuotehakujen parannukset

Paikallisista tuotehaut ovat nyt käyttäjäystävällisempiä. Niihin on tehty seuraavat parannukset:

- Avattavat tuote- ja asiakasvalikot on lisätty hakukenttään, jotta työntekijät voivat valita joko **tuotteen** tai **asiakkaan** ennen hakua. Oletusarvon mukaan **tuote** on valittuna seuraavan kuvan mukaisesti.
- Useita sanoja käytettäessä (eli hakuehtoja käytettäessä) jälleenmyyjät voivat määrittää, sisältyykö hakutuloksiin kohteita, jotka vastaavat *mitä tahansa* hakuehtoja vai kohteita, jotka vastaavat *kaikkia* hakuehtoja. Tämä asetus on myyntipisteen toimintoprofiilin uudessa **Tuotehaku**-ryhmässä. Oletusarvo on **Kohdista mikä tahansa hakusana**. Tämä asetus on suositeltu asetus. **Kohdista mikä tahansa hakusana**-asetusta käytettäessä tulokseksi palautetaan kaikki tuotteet, jotka vastaavat osittain tai kokonaan vähintään yhtä hakuehtoa. Nämä tulokset järjestetään automaattisesti nousevaan järjestykseen siten, että tuotteet, jotka vastaavat parhaiten avainsanoja (kokonaan tai osittain), ovat ensimmäisenä.

    **Kohdista kaikki hakusanat** -asetus palauttaa vain tuotteita, jotka vastaavat kaikkia hakusanoja (kokonaan tai osittain). Tästä asetuksesta on hyötyä, kun tuotenimet ovat pitkiä ja työntekijät haluavat rajoitetumman joukon hakutuloksia. Näillä hauilla on kuitenkin kaksi rajoituista:

    - Haku tehdään yksittäisiin tuoteominaisuuksiin. Haku palauttaa esimerkiksi vain tuotteita, jolla on vähintään yksi tuoteominaisuus, joka sisältää kaikki hakusanat.
    - Haku ei koske dimensioita.

- Vähittäismyyjät voivat nyt määrittää tuotehaun näyttämään hakuehdotuksia käyttäjien kirjoittaessa tuotenimiä. Tämän toiminnon uusi asetus on myyntipisteen toimintoprofiilin uudessa **Tuotehaku**-ryhmässä. Asetuksen nimi on **Näytä hakuehdotukset kirjoittamisen aikana**. Työntekijät voivat käyttää tätä toimintoa löytämään etsimänsä tuotteet nopeasti, koska koko tuotenimeä ei tarvitse kirjoittaa.
- Tuotehaun algoritmi etsii hakusanoja nyt myös tuotteen **Hakunimi**-ominaisuudesta.

    ![Tuote-ehdotukset](./media/Productsuggestions.png "Tuote-ehdotukset")

## <a name="customer-search"></a>Asiakashaku

Asiakashakua käytetään asiakkaiden etsimiseen erilaisissa tarkoituksissa. Kassat voivat esimerkiksi haluta nähdä asiakkaan toivelistan tai ostohistorian, tai lisätä asiakkaan tapahtumaan. Asiakashaun algoritmi palauttaa usean hakusanan hauissa kaikki asiakkaat, jotka vastaavat mitä tahansa hakusanoista. Useimpia hakusanoja vastaavat asiakkaat näkyvät kuitenkin ensimmäisenä tuloksissa. Tämä vastaa tapaa, jolla muut hakukoneet näyttävät tuloksia. Näiden tuloksissa näytetään ensin eniten hakusanoja vastaavat tulokset ja sitten osittaisia hakusanoja vastaavat tulokset. Tämä helpottaa kassoja tilanteissa, joissa käytetään useita hakusanoja, mutta yhdessä hakusanoista on kirjoitusvirhe.

Asiakashaut tehdään oletusarvon mukaan myymälään liitettyihin osoitekirjoihin. Tällaista hakua kutsutaan *paikalliseksi asiakashauksi*. Työntekijät voivat myös hakea asiakkaita kaikkialta. Toisin sanoen, asiakkaita voidaan etsiä yrityksen kaikista myymälöistä sekä muista yrityksistä. Tällaista hakua kutsutaan *asiakkaan etähauksi*.

Työntekijät voivat suorittaa yleisen haun valitsemalla **Suodata tuloksia** -painikkeen sivun alalaidasta ja valitsemalla sitten **Hae kaikista myymälöistä** -vaihtoehdon, alla olevan kuvan mukaisesti. Tässä tapauksessa hakutulokset eivät sisällä ainoastaan asiakkaita. Kaikki osapuolet, jotka ovat missä tahansa pääkonttorin osoitekirjassa, sisältyvät myös tuloksiin. Osapuolet ovat toimittajia, työntekijöitä, yhteyshenkilöitä ja kilpailijoita.

> [!NOTE]
> Asiakkaan etähaun hakusanan on oltava vähintään neljä merkkiä pitkä, jotta järjestelmä näyttää tuloksia.

Asiakkaan etähauissa ei näytetä muiden yritysten asiakkaiden asiakastunnusta, koska näillä asiakkailla ei ole asiakastunnusta nykyisessä yrityksessä. Jos työntekijä kuitenkin avaa asiakkaan tietosivun, järjestelmä luo automaattisesti osapuolelle asiakastunnuksen ja liittää myymälän osoitekirjan asiakkaaseen. Tällöin asiakas näkyy myöhemmin tehtävissä paikallisissa hauissa.

![Yleinen asiakashaku](./media/Globalcustomersearch.png "Yleinen asiakashaku")

### <a name="enhancements-to-local-customer-search"></a>Paikallisten asiakashakujen parannukset

Puhelinnumeroon perustuvia hakuja on yksinkertaistettu. Nämä haut ohittavat nyt erikoismerkit, kuten välilyönnit, tavuviivat ja sulkeet, jotka on mahdollisesti lisätty asiakasta luotaessa. Kassan ei tämän vuoksi tarvitse välittää puhelinnumeron muodosta hakujen yhteydessä. Asiakkaita voi hakea myös kirjoittamalla osittaisen puhelinnumeron. Jos puhelinnumerossa on erikoismerkkejä, se voidaan etsiä myös hakemalla erikoismerkin jälkeen tulevia numeroita. Jos esimerkiksi asiakkaan puhelinnumeroksi on tallennettu **123-456-7890**, kassa voi etsiä asiakkaan kirjoittamalla **123**, **456**, **7890** tai **1234567890**. Haun voi tehdä myös kirjoittamalla puhelinnumeron muutaman ensimmäisen numeron.

Perinteinen asiakashaku voi kestää kauan, koska haku kohdistuu useisiin kenttiin. Kassat voivat sen sijaan tehdä haun asiakkaan yhden ominaisuuden perusteella käyttämällä esimerkiksi nimeä, sähköpostiosoitetta tai puhelinnumeroa. Asiakkaan hakualgoritmin käyttämiä ominaisuuksia kutsutaan *asiakashaun ehdoiksi*. Järjestelmänvalvoja voi määrittää kätevästi vähintään yhden hakuehdon myyntipisteessä näkyväksi pikavalinnaksi. Koska haussa käytetään vain yhtä ehtoa, vain hakua vastaavat tulokset näytetään. Tämän vuoksi haku on tehokkaampi kuin tavallinen asiakashaku. Seuraavassa kuvassa on myyntipisteen asiakashaun pikavalinnat.

![Asiakashaun pikavalinnat](./media/SearchShortcutsPOS.png "Asiakashaun pikavalinnat")

Järjestelmänvalvoja voi määrittää hakuehdot pikavalinnoiksi avaamalla **Vähittäismyynnin parametrit** -sivun Microsoft Dynamics 365 for Finance and Operationsin ja valitsemalla sitten **Myyntipisteen hakuehdot** -välilehdessä kaikki pikavalintoina näytettävät ehdot.

![Haun pikavalintojen määrittäminen](./media/ConfigureShortcutsAX.png "Haun pikavalintojen määrittäminen")

> [!NOTE]
> Jos lisäät liian monta pikavalintaa, myyntipisteen hakuruudun avattava valikko muuttuu sekavaksi, mikä voi vaikuttaa työntekijän hakukokemukseen. Tämän vuoksi vain tarvittavat pikavalinnat kannattaa lisätä.

**Näyttöjärjestys**-kenttä määrittää, missä järjestyksessä pikavalinnat näytetään myyntipisteessä. Näytettävät ehdot ovat valmiita ominaisuuksia, joilla asiakashakualgoritmi hakee asiakkaita. Kumppanit voivat kuitenkin lisätä mukautettuja ominaisuuksia haun pikavalinnoiksi. Järjestelmänvalvoja voi lisätä mukautettuja ominaisuuksia haun pikavalinnoiksi laajentamalla asiakashaun hakuehdoissa käytettäviä laajennettavia valintalistoja ja merkitsemällä sitten kumppanin mukautetut ominaisuudet pikavalinnoiksi. Kumppanit vastaavat tuloksia etsivän koodin kirjoittamisesta, kun heidän mukautettuja pikavalintoja käytetään hauissa.

> [!NOTE]
> Valintalistaan lisättävä mukautettu ominaisuus ei vaikuta vakioasiakashaun algoritmiin. Asiakashakualgoritmi ei siis tee hakuja mukautetussa ominaisuudessa. Käyttäjät voivat käyttää mukautettua ominaisuutta haussa vain, jos kyseinen mukautettu ominaisuus on lisätty pikavalintoja tai jos oletushakualgoritmi on ohitettu.

