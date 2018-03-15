---
title: "Tuote- ja asiakashaku myyntipisteessä"
description: "Tämä ohjeaihe sisältää yleiskatsauksen parannuksista, jotka on tehty Dynamics 365 for Retailin tuote- ja asiakashakuihin."
author: ShalabhjainMSFT
manager: AnnBe
ms.date: 08/16/2017
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
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: 2af45de0d63b01e71b5009e2f62cfdff6844da7d
ms.contentlocale: fi-fi
ms.lasthandoff: 02/07/2018

---

# <a name="overview-of-product-and-customer-search-in-point-of-sale"></a>Yleiskatsaus tuote- ja asiakashauista myyntipisteessä

[!include[banner](includes/banner.md)]

Modern Point of Sale (MPOS) ja pilvimyyntipiste (CPOS) sisältävät helppokäyttöisen hakutoiminnon, jolla työntekijät voivat hakea tuotteita ja asiakkaita nopeasti. Hakukenttä on aina käytettävissä MPOS- ja CPOS-myyntipisteiden ylälaidassa, jotta työntekijät voivat löytää tuotteet ja asiakkaat nopeasti.

Työntekijät voivat hakea tuotteita myymälään sekä muihin yrityksen myymälöihin liitetyistä valikoimista ja luetteloista. Tämän ansiosta kassalta voi myydä ja palauttaa tuotteita, jotka eivät kuulu myymälän valikoimaan. Vastaavasti työntekijät voivat etsiä asiakkaita, jotka on liitetty joko nykyiseen myymälään tai mihin tahansa muuhun yrityksen myymälään. Lisäksi työntekijät voivat hakea asiakkaita, jotka liittyvät ylätason organisaation toiseen yritykseen.

## <a name="product-search"></a>Tuotehaku 

Oletusarvon mukaan tuotehaku tehdään myymälän valikoimaan. Tällaista hakua kutsutaan *paikalliseksi tuotehauksi*. Työntekijät voivat kuitenkin vaihtaa hakuluettelon mihin tahansa nykyisen myymälän luetteloon tai hakea toisesta myymälästä. Tällaista hakua kutsutaan *tuotteen etähauksi*. Voit vaihtaa luettelon valitsemalla **Luokat**-painikkeen sivun vasemmasta laidasta. Valitse esiin tulevan ruudun ylälaidasta **Vaihda luettelo** -painike ja valitse sitten luettelo, jota haluat selata. Järjestelmä tuotteet valitusta luettelosta.

Työntekijät voivat valita minkä tahansa myymälän tai hakea tuotteita kaikista myymälöistä helposti **Vaihda luettelo** -sivulla.

![Luettelon vaihtaminen](./media/Changecatalog.png "Luettelon vaihtaminen")
 
Paikallinen tuotehaku etsii seuraavista tuotteen ominaisuuksista:

- Tuotenumero
- Tuotteen nimi
- kuvaus
- Dimensiot
- Viivakoodi
- Hakunimi

### <a name="enhancements-to-local-product-searches"></a>Paikallisten tuotehakujen parannukset

Paikallisista tuotehauista on tehty käyttäjäystävällisempiä. Niihin on tehty seuraavat parannukset:

- Avattavat tuote- ja asiakasvalikot on lisätty hakukenttään, jotta työntekijät voivat valita joko **tuotteen** tai **asiakkaan** ennen hakua. Oletusarvon mukaan **tuote** on valittuna seuraavan kuvan mukaisesti.
- Useita sanoja käytettäessä (eli hakuehtoja käytettäessä) jälleenmyyjät voivat määrittää, sisältyykö hakutuloksiin kohteita, jotka vastaavat mitä tahansa hakuehtoja vai kohteita, jotka vastaavat kaikkia hakuehtoja. Tämä asetus löytyy myyntipisteen toimintoprofiilin uudesta ryhmästä, **Tuotehaku**. Oletusarvo on **Kohdista mikä tahansa hakusana**. Tämä asetus on suositeltu asetus. Kun **Kohdista mikä tahansa hakusana** -asetusta käytetään, kaikki tuotteet, jotka vastaavat osittain tai kokonaan yhtä useampaa hakusanaa palautetaan tulosluetteloon, ja luettelo järjestetään automaattisesti sen mukaan, millä tuotteilla on eniten hakusanojen vastaavuuksia (kokonaan tai osittain).

    **Kohdista kaikki hakusanat** -asetus palauttaa vain tuotteita, jotka vastaavat kaikkia hakusanoja (kokonaan tai osittain). Tästä asetuksesta on hyötyä, kun tuotenimet ovat pitkiä ja työntekijät haluavat rajoitetumman joukon hakutuloksia. Näillä hauilla on kuitenkin kaksi rajoituista:

    - Haku tehdään yksittäisiin tuoteominaisuuksiin. Haku palauttaa esimerkiksi vain tuotteita, jolla on vähintään yksi tuoteominaisuus, joka sisältää kaikki hakusanat.
    - Haku ei koske dimensioita.

- Vähittäismyyjät voivat nyt määrittää tuotehaun näyttämään hakuehdotuksia käyttäjien kirjoittaessa tuotenimiä. Uusi asetus tälle toiminnallisuudelle löytyy myyntipisteen toimintoprofiilin uudesta ryhmästä, **Tuotehaku**. Asetuksen nimi on **Näytä hakuehdotukset kirjoittamisen aikana**. Työntekijät voivat käyttää tätä toimintoa löytämään etsimänsä tuotteet nopeasti, koska koko tuotenimeä ei tarvitse kirjoittaa.
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

### <a name="enhancements-to-local-customer-searches"></a>Paikallisten asiakashakujen parannukset

Paikalliset asiakashaut löytävät asiakkaat nopeasti puhelinnumeron perusteella. Työntekijöiden ei tarvitse kirjoittaa mitään asiakkaan puhelinnumerossa olevia erikoismerkkejä, kuten välilyöntejä, yhdysmerkkejä tai sulkeita. Vaikka kassat voivat tallentaa puhelinnumerot missä tahansa muodossa (ne voivat sisältää esimerkiksi sulkeita, yhdysmerkkejä, erikoismerkkejä jne.), he voivat hakea asiakkaita kirjoittamalla puhelinnumeron osittain. Jos kassa on käyttänyt erikoismerkkejä tallentaessaan puhelinnumeron, muut kassat voivat löytää asiakkaan kirjoittamalla erikoismerkkien jälkeen tulevat numerot. Jos esimerkiksi asiakkaan puhelinnumeroksi on tallennettu **123-456-7890**, kassanhoitaja voi etsiä asiakkaan kirjoittamalla **123**, **456**, **7890**, tai **1234567890**. Haun voi myös tehdä osittaisena kirjoittamalla puhelinnumeron muutaman ensimmäisen numeron.

