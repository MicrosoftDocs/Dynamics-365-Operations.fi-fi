---
title: Kysynnän ennustepalveluiden yleiskatsaus
description: Kysynnän ennusteita käytetään ennustamaan riippumatonta kysyntää myyntitilauksista ja sidonnaista kysyntää missä tahansa myyntitilausten erotuskohdassa. Tarkennetut ennustevähennyssäännöt tarjoavat ihanteellisen ratkaisun joukkomukauttamiseen.
author: t-benebo
ms.date: 07/07/2020
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: ReqDemPlanCreateForecastDialog
audience: Application User
ms.reviewer: kamaybac
ms.custom:
- "72004"
- intro-internal
ms.assetid: 916707c9-1333-460f-a0fa-4e95f6fda2ad
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5c764cc186b5c8742ccfd90b5928f6625f3360c8
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/29/2022
ms.locfileid: "9065594"
---
# <a name="demand-forecasting-overview"></a>Kysynnän ennustepalveluiden yleiskatsaus

[!include [banner](../includes/banner.md)]

Kysynnän ennusteita käytetään ennustamaan riippumatonta kysyntää myyntitilauksista ja sidonnaista kysyntää missä tahansa myyntitilausten erotuskohdassa. Tarkennetut ennustevähennyssäännöt tarjoavat ihanteellisen ratkaisun joukkomukauttamiseen.

Perusennusteen luonnissa historiallisten tapahtumien yhteenveto viedään Microsoft Azuren automaattianalyysiin, jota isännöidään Azuressa. Koska tätä palvelua ei jaeta käyttäjien kesken, sitä voidaan mukauttaa alakohtaisten vaatimusten täyttämiseksi. Voit käyttää Supply Chain Managementia ennusteen visualisointiin ja muuttamiseen sekä ennusteen tarkkuutta koskevien suorituskykyilmaisimien (KPI:t) tarkastelemiseen.

> [!NOTE]
> Microsoft Azuren koneoppimisstudio (perinteinen) tarvitaan ennusteen luontiin koneoppimisen avulla. Joulukuun 1.12.2021 jälkeen et voi luoda uusia koneoppimisstudion (perinteinen) resursseja. Voit kuitenkin jatkaa koneoppimisstudion (perinteinen) -resurssien käyttöä 31.8.2024 saakka. Päivitettyjä tietoja on kohdassa [Azuren koneoppimisstudio](/azure/machine-learning/overview-what-is-machine-learning-studio#ml-studio-classic-vs-azure-machine-learning-studio).
> 
> Dynamics 365 Supply Chain Management -versio 10.0.23 ja sitä myöhemmät versiot tukevat uutta Azuren koneoppimisstudiota.

## <a name="key-features-of-demand-forecasting"></a>Kysynnän ennusteen tärkeimmät ominaisuudet

Tässä on muutamia kysynnän ennusteiden pääominaisuuksia:

- Luo historiallisiin tietoihin perustuva tilastollinen perusennuste
- Käytä ennustedimensioiden dynaaminen joukko
- Visualisoi ennustetrendejä, luottamusvälejä ja ennusteeseen tehtyjä muutoksia.
- Valtuuta oikaistu ennuste suunnitteluprosessien käyttöön.
- Poista poikkeava arvo.
- Luo ennusteen tarkkuuden mittarit.

## <a name="major-themes-in-demand-forecasting"></a>Kysynnän ennusteen pääteemat

Kysynnän ennusteissa käytetään kolmea pääteemaa:

- **Modulaarisuus** – Kysynnän ennusteet ovat modulaarisia ja helposti määritettäviä. Voit ottaa toiminnon käyttöön ja poistaa sen käytöstä muuttamalla konfigurointiavain kohdassa **Kauppa** &gt; **Varastoennuste** &gt; **Kysynnän ennuste**.
- **Microsoft Stackin uudelleenkäyttö** – Automaattianalyysipalvelu, joka on osa Microsoft Cortana Analytics Suite -ohjelmistoa, tarjoaa mahdollisuuden luoda nopeasti ja helposti ennustavia analyysikokeiluja, kuten kysynnän arviokokeiluja, käyttämällä algoritmeja R tai Python-ohjelmointikieltä sekä yksinkertaista vedä-ja-pudota-käyttöliittymää.
  - Voit ladata kysynnän ennusteen kokeilut, muuttaa niitä niin, että ne vastaavat liiketoimintasi tarpeita, julkaista ne verkkopalvelussa Azuressa ja käyttää niitä kysynnän ennusteiden luomiseen. Kokeilut ovat ladattavissa, jos olet ostanut tuotannon suunnittelutoiminnon Supply Chain Management -tilauksen yritystason käyttäjänä.
  - Voit ladata minkä tahansa saatavilla olevan kysynnän ennustekokeilun kohdasta [Cortana Analytics -galleria](https://gallery.cortanaanalytics.com/). Kysynnän ennusteen kokeilut integroidaan automaattisesti Supply Chain Managementiin, mutta asiakkaiden ja kumppanien on käsiteltävä niiden kokeilujen integraatiot, jotka he lataavat [Cortana Analytics -galleriasta](https://gallery.cortanaanalytics.com/). Näin ollen [Cortana Analytics -valikoiman](https://gallery.cortanaanalytics.com/) kokeilujen käyttö ei ole yhtä suoraviivaista kuin talous- ja toimintosovellusten kysynnän ennusteen kokeilujen käyttö. Sinun on muokattava kokeilujen koodia niin, että ne käyttävät talous- ja toimintosovellusten ohjelmointirajapintaa.
  - Voit luoda omat kokeilusi Microsoft Azuren automaattianalyysipalvelussa (perinteinen), julkaista ne Azuren palveluissa ja käyttää niitä kysynnän ennusteiden luomiseen.
  - Jos et tarvitse korkeaa suorituskykyä tai jos sinun ei tarvitse käsitellä suurta tietojen määrää, voit käyttää automaattianalyysipalveluiden vapaata tasoa. Suosittelemme, että aloitat aina tältä tasolta, etenkin käyttöönotto- ja testausvaiheiden aikana. Jos tarvitset korkeampaa suorituskykyä ja lisätallennustilaa, voit käyttää automaattianalyysipalveluiden standarditasoa. Tämä taso vaatii Azure-tilauksen ja siihen liittyy lisäkustannuksia. Saat lisätietoja automaattianalyysipalveluiden hinnoittelusta kohdassa [Automaattianalyysipalveluiden hinnoittelu](https://aka.ms/machine-learning-price-info).
- **Ennusteen vähennys missä tahansa erotuskohdassa** – Tähän toimintoon perustuvien koontien kysynnän ennusteessa, jonka avulla voit ennustaa sekä sidonnaista että riippumatonta kysyntää missä tahansa erotuskohdassa.

## <a name="basic-flow-in-demand-forecasting"></a>Kysynnän ennusteen peruskulku

Seuraavassa kaaviossa on kuvattu kysynnän ennusteen peruskulku.

[![Kysynnän ennusteen esittelykaavio.](./media/demand-forecasting-introduction.png)](./media/demand-forecasting-introduction.png)

Kysynnän ennusteen luonti aloitetaan Supply Chain Managementissa. Supply Chain Managementin tapahtumatietokannan historialliset tiedot kootaan ja kirjoitetaan valmistelutaulukkoon. Valmistelutaulukko syötetään myöhemmin automaattianalyysipalveluun. Minimaalisilla mukautustoimilla voit kytkeä useita tietolähteitä valmistelutaulukkoon. Tietolähteet voivat sisältää Microsoft Excel -tiedostoja, pilkuin erotettujen arvojen (CSV)-tiedostoja, sekä tietoja Microsoft Dynamics AX 2009- ja Microsoft Dynamics AX 2012 -ohjelmista. Voit näin ollen luoda kysynnän ennusteita, jotka huomioivat useisiin järjestelmiin hajautettuja tietoja. Päätietojen, kuten nimikkeiden nimien ja mittayksiköiden, on kuitenkin oltava samat kaikissa tietolähteissä.

Jos käytät automaattianalyysipalvelun kokeiluja, ne etsivät sopivinta viidestä aikasarjan ennustusmenetelmästä perusennusteen laskemiseen. Näiden ennustemenetelmien parametreja hallitaan Supply Chain Managementissa.

Ennusteet, historialliset tiedot ja kysynnän ennusteisiin aiemmissa iteraatioissa tehdyt muutokset ovat sitten käytettävissä Supply Chain Managementissa.

Voit käyttää Supply Chain Managementia perusennusteiden visualisointiin ja muokkaukseen. Manuaaliset muutokset on valtuutettava ennen kuin ennusteita voidaan käyttää suunnitteluun.

## <a name="limitations"></a>Rajoitukset

Kysynnän ennusteet on työkalu, joka auttaa teollisuuden alan asiakkaita luomaan ennusteprosesseja. Se tarjoaa kysynnän ennusteen ratkaisun perustoiminnot ja on suunniteltu helposti laajennettavaksi. Kysynnän ennusteet eivät ehkä sovellu parhaiten kaupan, tukkukaupan, varastoinnin, kuljetus- tai muulla palvelualalla oleville asiakkaille.

### <a name="demand-forecast-variant-conversion-limitation"></a>Kysynnän ennusteen varianttimuunnoksen rajoitus

Varianttimuuntokohtaista mittayksikköä ei tueta täysin kysynnän ennustetta luotaessa, jos varaston mittayksikkö ei ole sama kuin kysynnän ennusteen mittayksikkö.

Ennusteen luonti (**Varaston mittayksikkö > Kysynnän ennusteen mittayksikkö**) käyttää tuotteen mittayksikön muunnosta. Kun kysynnän ennusteen luonnin historiallisia tietoja ladataan, tuotetason mittayksikön muuntamista käytetään aina muunnettaessa varaston mittayksikköä kysynnän ennusteen mittayksikköön, vaikka muunnoksia olisi määritetty varianttitasolla:

Ennusteen valtuuttamisen ensimmäinen osa (**Kysynnän ennusteen mittayksikö > varaston mittayksikkö**) käyttää tuotannon mittayksikön muuntoa. Ennusteen valtuuttamisen toinen osa (**Varaston mittayksikkö > myynnin mittayksikkö**) käyttää variantin mittayksikön muuntoa. Kun luotu kysynnän ennuste valtuutetaan, muunto varaston mittayksikköön kysynnän ennusteen mittayksiköstä tehdään käyttämällä tuotetason mittayksikön muuntoa. Samanaikaiset varastoyksikön ja myynnin mittayksikön välinen muunto noudattaa varianttitason määrittämiä muuntoja.

Huomaa, että kysynnän ennusteen mittayksiköllä ei tarvitse tiettyä merkitystä. Se voidaan määrittää kysynnän ennusten yksiköksi. Kunkin tuotteen muuntosuhteeksi voidaan määrittää 1:1 varaston mittayksiköllä.

## <a name="additional-resources"></a>Lisäresurssit

- [Kysynnän ennusteiden asetukset](demand-forecasting-setup.md)
- [Tilastollisen perusennusteen luominen](generate-statistical-baseline-forecast.md)
- [Manuaalisten oikaisujen tekeminen perusennusteeseen](manual-adjustments-baseline-forecast.md)
- [Oikaistun ennusteen valtuuttaminen](authorize-adjusted-forecast.md)
- [Ennusteen tarkkuuden seuranta](monitor-forecast-accuracy.md)
- [Poista poikkeavat tiedot aiemmista tapahtumatiedoista laskettaessa ennustetarvetta](remove-historical-outliers-calculating-demand-forecast.md)
- [Video: Kysynnän ennustetoimintojen laajentaminen](https://www.youtube.com/watch?v=4OIKIXLiNjI&feature=youtu.be)
- [Verkkoseminaari: Kysynnän ennustaminen Azuren koneoppimispalvelun sarjojen avulla](https://aka.ms/DemandForecastingwithAzureMachineLearningSeries)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

