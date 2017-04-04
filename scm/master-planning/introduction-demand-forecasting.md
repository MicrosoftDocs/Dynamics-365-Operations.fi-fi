---
title: "Kysynnän Ennustaminen yleiskuvaus"
description: "Kysynnän ennusteita käytetään ennustamaan riippumatonta kysyntää myyntitilauksista ja sidonnaista kysyntää missä tahansa myyntitilausten erotuskohdassa. Parannettu myyntiennusteen vähentäminen säännöissä ihanteellinen ratkaisu massa mukauttamiseen."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ReqDemPlanCreateForecastDialog
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 72004
ms.assetid: 916707c9-1333-460f-a0fa-4e95f6fda2ad
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 9152616b81e7873426f296376b5e57c94439379d
ms.lasthandoff: 03/31/2017


---

# <a name="demand-forecasting-overview"></a>Kysynnän Ennustaminen yleiskuvaus

Kysynnän ennusteita käytetään ennustamaan riippumatonta kysyntää myyntitilauksista ja sidonnaista kysyntää missä tahansa myyntitilausten erotuskohdassa. Parannettu myyntiennusteen vähentäminen säännöissä ihanteellinen ratkaisu massa mukauttamiseen.

Perusennusteen luonnissa historiallisten tapahtumien yhteenveto viedään Microsoft Azuren automaattianalyysipalveluun, jota isännöidään Azuressa. Koska tätä palvelua ei jaeta käyttäjien kesken, sitä voidaan mukauttaa alakohtaisten vaatimusten täyttämiseksi. Dynamics 365 toimintojen avulla voit visualisoida ennuste, ennuste säätää ja tarkastella tietoja ennusteen tarkkuus Suorituskyvyn mittareiden (KPI: T).

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

-   **Modulaarisuus** – Kysynnän ennusteet ovat modulaarisia ja helposti määritettäviä. Voit ottaa toimintoja käyttöön ja poistaa käytöstä muuttamalla konfigurointiavain on **kaupan**&gt;**ennustettu varaston**&gt;**kysynnän ennusteiden**.
-   **Uudelleenkäyttöä Microsoft pinon** – Microsoft käynnisti koneen oppimisen ympäristö-helmikuu 2015. Machine Learning, joka on nyt osa Microsoft Cortana Analytics, voit nopeasti ja helposti luoda tehdä ennakoivia analyysejä kokeista, kysynnän arvioinnin kokeisiin kuten algoritmit R tai Python ohjelmointikielet ja yksinkertaisella vedä ja pudota-käyttöliittymän avulla.
    -   Voit ladata Dynamics 365 toimia kysynnän ennusteet kokeita, muuttaa ne oman yrityksesi tarpeita vastaavan, julkaista ne Azure WWW-palveluna ja käyttää niitä luoda myyntiennusteita. Kokeet ovat ladattavissa, jos olet hankkinut Dynamics-365 toimintojen tilauksen tuotannon suunnittelija, enterprise-tason käyttäjänä.
    -   Voit ladata minkä tahansa saatavilla olevan kysynnän ennustekokeilun kohdasta [Cortana Analytics -galleria](https://gallery.cortanaanalytics.com/). Olisi toimia kysynnän ennusteet kokeisiin Dynamics-365 on integroitu automaattisesti työvaiheiden Dynamics 365, asiakkaat ja kumppanit on käsiteltävä ne ladataan, kokeista integrointi [Cortana Analytics valikoima](https://gallery.cortanaanalytics.com/). Siksi kokeilua [Cortana Analytics valikoima](https://gallery.cortanaanalytics.com/) eivät ole aivan yhtä helppo käyttää Dynamics 365 toimia kysynnän ennusteet kokeisiin. Kokeet koodia on muokattava siten, että ne käyttävät Dynamics 365 toimintojen sovellusohjelmointiliittymää (API).
    -   Voit luoda omat kokeilusi Microsoft Azuren automaattianalyysipalvelussa, julkaista ne Azuren palveluissa ja käyttää niitä kysynnän ennusteiden luomiseen.
    -   Jos et tarvitse korkeaa suorituskykyä tai jos sinun ei tarvitse käsitellä suurta tietojen määrää, voit käyttää automaattianalyysipalveluiden vapaata tasoa. Suosittelemme, että aloitat aina tältä tasolta, etenkin käyttöönotto- ja testausvaiheiden aikana. Jos tarvitset korkeampaa suorituskykyä ja lisätallennustilaa, voit käyttää automaattianalyysipalveluiden standarditasoa. Tämä taso vaatii Azure-tilauksen ja siihen liittyy lisäkustannuksia. Saat lisätietoja automaattianalyysipalveluiden hinnoittelusta kohdassa <http://aka.ms/machine-learning-price-info>.
-   **Ennusteen vähennys irtautus milloin tahansa** – kysynnän ennusteet Dynamicsissa 365 koontiversiot Operations-toiminto, jonka avulla voit ennustaa milloin tahansa irtautus sekä itsenäistä ja erillistä kysyntää.

## <a name="basic-flow-in-demand-forecasting"></a>Kysynnän ennusteen peruskulku
Seuraavassa kaaviossa on kuvattu kysynnän ennusteen peruskulku. 

[![kysynnän Ennustaminen johdanto-kaavio](./media/demand-forecasting-introduction.png)](./media/demand-forecasting-introduction.png)

Myyntiennusteen sukupolven alkaa-Dynamics 365 operaatioille. Historiallinen tapahtumatietoihin toimia tapahtumapohjaista tietokannan Dynamics-365-kerätään ja täyttää väliaikainen taulukko. Tämä väliaikainen taulukko on myöhemmin tuli Machine Learning-palveluun. Suorittamalla minimal customization voit kytkeä eri tietolähteistä väliaikaiseen taulukkoon. Mitä voi sisältää Microsoft Excel tiedostot, pilkuin erotettujen arvojen (CSV)-tiedostoja ja tietoja Microsoft Dynamics AX 2009: n ja Microsoft Dynamics AX 2012: n. Siksi voit luoda myyntiennusteita, harkitse historiatietoja, joka leviää joukossa useita järjestelmiä. Päätietojen, kuten nimikkeiden nimien ja mittayksiköiden, on kuitenkin oltava samat kaikissa tietolähteissä.

Jos käytät Dynamics 365 toimia kysynnän ennusteet Machine Learning kokeita, hänen on etsittävä Sovita kesken viiden kerran sarja ennustamismenetelmistä perusaikataulun ennusteen laskemiseen. Ennustaminen-menetelmien parametrit hallitaan Dynamics 365 operaatioille. 

Ennusteet ja historiallisten tietojen muutokset, jotka tehtiin edellisen iteraatioiden-kysynnän ennusteet voidaan käyttää Dynamics 365 operaatioille. 

Dynamics 365 toimintojen avulla voit visualisoida ja muokata perusaikataulun ennusteet. Manuaaliset muutokset on valtuutettava ennen kuin ennusteita voidaan käyttää suunnitteluun.

## <a name="limitations"></a>Rajoitukset
Kysynnän ennusteiden Dynamics 365 toiminnoissa on työkalu, joka auttaa asiakkaiden valmistus teollisuudessa luoda Ennustaminen prosesseja. Se tarjoaa ratkaisun ennusteet kysynnän perustoimintoihin ja on suunniteltu niin, että se voi helposti laajentaa. Ennusteiden tekeminen saattaa olla paras sovi kuten vähittäiskaupan, teollisuuden asiakkaiden tukku, varastointi, kuljetus tai muiden ammatillisten palvelujen kysyntä.

<a name="see-also"></a>Lisätietoja
--------

[Demand forecasting setup](demand-forecasting-setup.md)

[Generating a statistical baseline forecast](generate-statistical-baseline-forecast.md)

[Making manual adjustments to the baseline forecast](manual-adjustments-baseline-forecast.md)

[Authorizing the adjusted forecast](authorize-adjusted-forecast.md)

[Monitoring forecast accuracy](monitor-forecast-accuracy.md)

[Remove outliers from historical transaction data when calculating a demand forecast](remove-historical-outliers-calculating-demand-forecast.md)


