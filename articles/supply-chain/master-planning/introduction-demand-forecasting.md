---
title: Kysynnän ennustepalveluiden yleiskatsaus
description: Kysynnän ennusteita käytetään ennustamaan riippumatonta kysyntää myyntitilauksista ja sidonnaista kysyntää missä tahansa myyntitilausten erotuskohdassa. Tarkennetut ennustevähennyssäännöt tarjoavat ihanteellisen ratkaisun joukkomukauttamiseen.
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqDemPlanCreateForecastDialog
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 72004
ms.assetid: 916707c9-1333-460f-a0fa-4e95f6fda2ad
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a645ee6f7e6085abc6e872d490b078f512c15aa1
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "309998"
---
# <a name="demand-forecasting-overview"></a>Kysynnän ennustepalveluiden yleiskatsaus

[!include [banner](../includes/banner.md)]

Kysynnän ennusteita käytetään ennustamaan riippumatonta kysyntää myyntitilauksista ja sidonnaista kysyntää missä tahansa myyntitilausten erotuskohdassa. Tarkennetut ennustevähennyssäännöt tarjoavat ihanteellisen ratkaisun joukkomukauttamiseen.

Perusennusteen luonnissa historiallisten tapahtumien yhteenveto viedään Microsoft Azuren automaattianalyysipalveluun, jota isännöidään Azuressa. Koska tätä palvelua ei jaeta käyttäjien kesken, sitä voidaan mukauttaa alakohtaisten vaatimusten täyttämiseksi. Voit käyttää Finance and Operationsia ennusteen visualisointiin ja muuttamiseen sekä ennusteen tarkkuutta koskevien suorituskykyilmaisimien (KPI:t) tarkastelemiseen.

## <a name="key-features-of-demand-forecasting"></a>Kysynnän ennusteen tärkeimmät ominaisuudet
Tässä on muutamia kysynnän ennusteiden pääominaisuuksia:

-   Luo historiallisiin tietoihin perustuva tilastollinen perusennuste
-   Käytä ennustedimensioiden dynaaminen joukko
-   Visualisoi ennustetrendejä, luottamusvälejä ja ennusteeseen tehtyjä muutoksia.
-   Valtuuta oikaistu ennuste suunnitteluprosessien käyttöön.
-   Poista poikkeava arvo.
-   Luo ennusteen tarkkuuden mittarit.

## <a name="major-themes-in-demand-forecasting"></a>Kysynnän ennusteen pääteemat
Kysynnän ennusteissa käytetään kolmea pääteemaa:

-   **Modulaarisuus** – Kysynnän ennusteet ovat modulaarisia ja helposti määritettäviä. Voit ottaa toiminnon käyttöön ja poistaa sen käytöstä muuttamalla konfigurointiavain kohdassa **Kauppa** &gt; **Varastoennuste** &gt; **Kysynnän ennuste**.
-   **Microsoft-pinon uudelleenkäyttö** – Microsoft toi markkinoille automaattianalyysialustan helmikuussa 2015. Automaattianalyysipalvelu, joka on nyt osa Cortana Analytics Suite -ohjelmistoa, tarjoaa mahdollisuuden luoda nopeasti ja helposti ennustavia analyysikokeiluja kuten kysynnän arviokokeiluja, käyttämällä algoritmeja R tai Python-ohjelmointikieltä ja yksinkertaista vedä-ja-pudota käyttöliittymää.
    -   Voit ladata Finance and Operationsin kysynnän ennusteen kokeilut, muuttaa niitä niin, että ne vastaavat liiketoimintasi tarpeita, julkaista ne verkkopalvelussa Azuressa ja käyttää niitä kysynnän ennusteiden luomiseen. Kokeilut ovat ladattavissa, jos olet ostanut tuotannon suunnittelutoiminnon Finance and Operations -tilauksen yritystason käyttäjänä.
    -   Voit ladata minkä tahansa saatavilla olevan kysynnän ennustekokeilun kohdasta [Cortana Analytics -galleria](https://gallery.cortanaanalytics.com/). Finance and Operationsin kysynnän ennusteen kokeilut integroidaan automaattisesti Finance and Operationsiin, mutta asiakkaiden ja kumppanien on käsiteltävä niiden kokeilujen integraatiot, jotka he lataavat [Cortana Analytics -galleriasta](https://gallery.cortanaanalytics.com/). Näin ollen [Cortana Analytics -gallerian](https://gallery.cortanaanalytics.com/) kokeilujen käyttö ei ole yhtä suoraviivaista kuin Finance and Operationsin kysynnän ennusteen kokeilujen käyttö. Sinun on muokattava kokeilujen koodia niin, että ne käyttävät Finance and Operationsin ohjelmointirajapintaa.
    -   Voit luoda omat kokeilusi Microsoft Azuren automaattianalyysipalvelussa, julkaista ne Azuren palveluissa ja käyttää niitä kysynnän ennusteiden luomiseen.
    -   Jos et tarvitse korkeaa suorituskykyä tai jos sinun ei tarvitse käsitellä suurta tietojen määrää, voit käyttää automaattianalyysipalveluiden vapaata tasoa. Suosittelemme, että aloitat aina tältä tasolta, etenkin käyttöönotto- ja testausvaiheiden aikana. Jos tarvitset korkeampaa suorituskykyä ja lisätallennustilaa, voit käyttää automaattianalyysipalveluiden standarditasoa. Tämä taso vaatii Azure-tilauksen ja siihen liittyy lisäkustannuksia. Lisätietoja automaattianalyysipalvelun hinnoittelusta on kohdassa <http://aka.ms/machine-learning-price-info>.
-   **Ennusteen vähennys missä tahansa erotuskohdassa** – Kysynnän ennusteet perustuvat Finance and Operationsissa tälle toiminnolle, jonka avulla voit ennustaa sekä sidonnaista että riippumatonta kysyntää missä tahansa erotuskohdassa.

## <a name="basic-flow-in-demand-forecasting"></a>Kysynnän ennusteen peruskulku
Seuraavassa kaaviossa on kuvattu kysynnän ennusteen peruskulku. 

[![Kysynnän ennusteen esittelykaavio](./media/demand-forecasting-introduction.png)](./media/demand-forecasting-introduction.png)

Kysyntäennusteen luonti alkaa Finance and Operationsissa. Finance and Operationsin tapahtumatietokannan historialliset tiedot kootaan ja kirjoitetaan valmistelutaulukkoon. Valmistelutaulukko syötetään myöhemmin automaattianalyysipalveluun. Minimaalisilla mukautustoimilla voit kytkeä useita tietolähteitä valmistelutaulukkoon. Tietolähteet voivat sisältää Microsoft Excel -tiedostoja, pilkuin erotettujen arvojen (CSV)-tiedostoja, sekä tietoja Microsoft Dynamics AX 2009- ja Microsoft Dynamics AX 2012 -ohjelmista. Voit näin ollen luoda kysynnän ennusteita, jotka huomioivat useisiin järjestelmiin hajautettuja tietoja. Päätietojen, kuten nimikkeiden nimien ja mittayksiköiden, on kuitenkin oltava samat kaikissa tietolähteissä.

Jos käytät Finance and Operationsin kysynnän ennusteen automaattianalyysipalvelun kokeiluja, ne etsivät sopivinta viidestä aikasarjan ennustusmenetelmästä perusennusteen laskemiseen. Näiden ennustemenetelmien parametreja hallitaan Finance and Operationsissa. 

Ennusteet, historialliset tiedot ja kysynnän ennusteisiin aiemmissa iteraatioissa tehdyt muutokset ovat sitten käytettävissä Finance and Operationsissa. 

Voit käyttää Finance and Operationsia perusennusteiden visualisointiin ja muokkaukseen. Manuaaliset muutokset on valtuutettava ennen kuin ennusteita voidaan käyttää suunnitteluun.

## <a name="limitations"></a>Rajoitukset
Finance and Operationsin kysynnän ennuste on työkalu, joka auttaa valmistusteollisuuden asiakkaita luomaan ennusteprosesseja. Se tarjoaa kysynnän ennusteen ratkaisun perustoiminnot ja on suunniteltu helposti laajennettavaksi. Kysynnän ennusteet eivät ehkä sovellu parhaiten vähittäismyynti-, tukkukauppa-, varastointi-, kuljetus- tai muulla palvelualalla oleville asiakkaille.

<a name="additional-resources"></a>Lisäresurssit
--------

[Kysynnän ennusteiden asetukset](demand-forecasting-setup.md)

[Tilastollisen perusennusteen luonti](generate-statistical-baseline-forecast.md)

[Manuaalisten oikaisujen tekeminen perusennusteeseen](manual-adjustments-baseline-forecast.md)

[Oikaistun kysynnän ennusteen valtuuttaminen](authorize-adjusted-forecast.md)

[Ennusteen tarkkuuden valvonta](monitor-forecast-accuracy.md)

[Poista poikkeavat tiedot aiemmista tapahtumatiedoista laskettaessa ennustetarvetta](remove-historical-outliers-calculating-demand-forecast.md)

[Kysynnän ennustetoimintojen laajentaminen](https://www.youtube.com/watch?v=4OIKIXLiNjI&feature=youtu.be)



