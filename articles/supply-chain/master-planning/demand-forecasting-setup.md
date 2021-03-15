---
title: Kysynnän ennusteiden asetukset
description: Tässä ohjeaiheessa kuvataan asetustehtävät, jotka sinun on suoritettava kysynnän ennusteita valmistellessasi.
author: roxanadiaconu
manager: tfehr
ms.date: 01/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqDemPlanDefaultAlgorithmParameters, ReqDemPlanForecastParameters
audience: Application User
ms.reviewer: kamaybac
ms.custom: 72653
ms.assetid: c5fa4b09-512d-4349-ac51-cc13da69a160
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b7b0976494a8bb128ae6bb40cbcdf7c691185f23
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4970503"
---
# <a name="demand-forecasting-setup"></a>Kysynnän ennusteiden asetukset

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa kuvataan asetustehtävät, jotka sinun on suoritettava kysynnän ennusteita valmistellessasi.  

Määritystehtäviin kuuluu seuraavien tietojen ja parametrien asettaminen:

## <a name="item-allocation-key"></a>Nimikkeenkohdistustunnus
Kysynnän ennuste lasketaan nimikkeelle ja sen dimensioille vain, jos nimike on nimikkeen kohdistustunnuksen osa. Tätä sääntöä käytetään suurten nimikejoukkojen ryhmittämiseen niin, että kysynnän ennusteita voidaan luoda nopeammin. Nimikkeen kohdistustunnuksen prosenttiosuus ohitetaan kysynnän ennusteita luotaessa. Ennusteet luodaan pelkästään historiallisten tietojen perusteella. 

Nimikkeen ja sen dimensioiden on oltava osa vain yhtä nimikkeen kohdistustunnusta, jos tätä nimikkeen kohdistustunnusta käytetään ennusteen luonnin aikana. 

Varastointiyksikkö (SKU) lisätään nimikkeen kohdistustunnukselle kohdassa **Pääsuunnittelu** &gt; **Asetukset** &gt; **Kysynnän ennuste** &gt; **Nimikkeen kohdistustunnukset**. Määritä nimike kohdistustunnukselle **Määritä nimikkeet** -sivulla.

## <a name="intercompany-planning-groups"></a>Konsernin sisäiset suunnitteluryhmät
Kysynnän ennusteet luovat kaikki yritykset kattavia ennusteita. Dynamics 365 Supply Chain Managementissa yritykset, joiden suunnittelu suoritetaan yhdessä, ryhmitetään yhdeksi konsernin sisäiseksi suunnitteluryhmäksi. Määritelläksesi yrityskohtaisesti mitkä nimikkeen kohdistustunnukset tulisi ottaa huomioon kysynnän ennusteissa, liitä nimikkeen kohdistustunnus konsernin suunnitteluryhmän jäseneen menemällä kohtaan **Pääsuunnittelu** &gt; **Asetukset** &gt; **Konsernin sisäiset suunnitteluryhmät**. 

Jos nimikkeen kohdistustunnuksia ei ole määritetty konsernin sisäisen suunnitteluryhmän jäsenille, kysynnän ennuste lasketaan oletusarvoisesti kaikille niille nimikkeille, jotka on määritetty kaikkiin nimikkeen kohdistustunnuksiin kaikista yrityksistä. Lisäsuodatusvaihtoehtoja yrityksille ja nimikkeen kohdistustunnuksille löytyy **Luo tilastollinen perusennuste** -sivulta. 

Tarkista nimikkeiden ennustettu lukumäärä. Tarpeettomat nimikkeet saattavat aiheuttaa lisäkustannuksia käyttäessäsi Microsoft Azure automaattianalyysipalvelua.

## <a name="demand-forecasting-parameters"></a>Kysynnän ennusteen parametrit
Määritä kysynnän ennusteen parametrit kohdassa **Pääsuunnittelu** &gt; **Asetukset** &gt; **Kysynnän ennusteen parametrit**. Koska kysynnän ennusteet suoritetaan kaikki yritykset kattavasti, asetukset yleiset. Asetukset koskevat toisin sanoen kaikkia yrityksiä. 

Kysynnän ennusteet luovat ennusteet lukumäärinä. Näin ollen mittayksikkö, jossa määrä ilmaistaan, on määritettävä **Kysynnän ennusteen yksikkö** -kentässä. Mittayksikön on oltava yksilöivä sen varmistamiseksi, että kooste ja prosenttijakauma ovat järkevät. Lisätietoja koosteesta ja prosenttijakaumasta on kohdassa [Manuaalisten muutosten tekeminen perusennusteeseen](manual-adjustments-baseline-forecast.md). Varmista, että jokaiselle mittayksikölle, jota käytetään kysynnän ennusteeseen sisältyvälle varastointiyksikölle, on muuntosääntö kyseiselle mittayksikölle ja yleinen ennusteen mittayksikkö. Kysynnän ennustetta luotaessa niiden nimikkeiden luettelo, joilla ei ole mittayksikön muuntoa, kirjataan niin, että voit helposti korjata asetukset. 

Kysynnän ennusteita voidaan käyttää ennustamaan sekä riippuvaista että riippumatonta kysyntää. Jos esimerkiksi vain **Myyntitilaus**-valintaruutu on valittuna ja jos kaikki kysynnän ennusteessa huomioitavat nimikkeet ovat myytäviä nimikkeitä, järjestelmä laskee riippumattoman kysynnän. Tärkeitä alikomponentteja voidaan kuitenkin lisätä nimikkeen kohdistustunnuksille ja sisällyttää kysynnän ennusteisiin. Tässä tapauksessa, jos **Tuotantolinja**-valintaruutu on valittuna, lasketaan riippuvainen ennuste. 

Perusennuste voidaan luoda kahdella tavalla. Voit käyttää ennustemalleja historiallisten tietojen päällä, tai voit vain kopioida historialliset tiedot ennusteeseen. **Kysynnän luontistrategia** -kentässä voit tehdä valinnan näiden kahden menetelmän välillä. Käytä ennustemalleja valitsemalla **Azuren automaattianalyysipalvelu**. 

Napsauttamalla **Ennustedimensiot** sivun **Kysynnän ennusteen parametrit** vasemmassa ruudussa, voit myös valita kysynnän ennusteen luonnissa käytettävän ennustedimensioiden joukon. Ennustedimensio osoittaa ennusteelle määritetyn erittelytason. Yritys, toimipaikka ja nimikkeen kohdistustunnus ovat pakollisia ennustedimensioita, mutta voit myös luoda ennusteita varastossa, varaston tilan, asiakasryhmän, asiakastilin, maan/alueen, osavaltion ja nimikkeen sekä kaikkien nimikedimensioiden tasoilla. 

Voit missä tahansa vaiheessa lisätä ennustedimensioita kysynnän ennusteissa käytettävien dimensioiden luetteloon. Voit myös poistaa ennustedimensioita luettelosta. Manuaaliset muutokset kuitenkin menetetään, jos lisäät tai poistat ennustedimension. 

Kaikki nimikkeet eivät toimi samalla tavalla kysynnän ennusteiden näkökulmasta. Samanlaisia nimikkeitä voidaan ryhmittää yhteen nimikkeen kohdistustunnukseen ja tapahtumatyypin ja ennustemenetelmän asetusten kaltaisille parametreille voidaan määrittää asetuksia nimikkeen kohdistustunnuskohtaisesti. Valitse **Kysynnän ennusteen parametrit** -sivun vasemmanpuoleisesta ruudusta **Nimikkeen kohdistustunnukset**. 

Supply Chain Management käyttää automaattianalyysipalveluiden verkkopalvelua ennusteen luomiseen. Muodosta yhteys palveluun antamalla seuraavat tiedot Microsoft Azuren automaattianalyysistudioon kirjautumista varten (perinteinen):

-   Verkkopalvelun ohjelmointirajapinta- (API)-avain
-   Verkkopalvelun päätepisteen URL-osoite
-   Azuren tallennustilin nimi
-   Azuren tallennustilin avain

> [!NOTE]
> Azuren tallennustilin nimi ja avain tarvitaan vain, jos käytät mukautettua tallennustiliä. Jos käytät paikallista versiota, sinulla on oltava mukautettu tallennustili Azuressa niin, että automaattianalyysi voi käyttää historiallisia tietoja. 

Voit käyttää omaa palveluasi kysynnän ennusteiden luomiseen automaattianalyysistudion tai Supply Chain Managementin kysynnän ennusteiden luomisen kokeilujen avulla. Supply Chain Managementissa on ohjeita kysynnän ennusteiden luomiskokeilujen käyttöönottamisesta verkkopalveluna. Valitse **Kysynnän ennusteen parametrit** -sivulla **Azuren automaattianalyysipalvelut** -välilehti.

## <a name="settings-for-the-demand-forecasting-machine-learning-service"></a>Kysynnän ennusteiden automaattianalyysipalveluiden asetukset
Jos haluat tarkastella parametreja, jotka voidaan määrittää kysynnän ennustepalvelulle, valitse **Pääsuunnittelu** &gt; **Asetukset** &gt; **Kysynnän ennuste** &gt; **Ennustealgoritmin parametrit**. **Ennustealgoritmin parametrit** sivu näyttää parametrien oletusarvot. Voit korvata nämä parametrit **Kysynnän ennusteen parametrit** -sivulla. Korvaa parametrit yleisesti **Yleinen** -välilehdessä, tai nimikkeen kohdistustunnuskohtaisesti **Nimikkeen kohdistustunnus** -välilehdessä. Nimikkeen kohdistustunnuksella korvattavat parametrit vaikuttavat vain kyseiseen nimikkeen kohdistustunnukseen määritettyjen nimikkeiden ennusteisiin.

### <a name="forecast-algorithm-parameters"></a>Ennustealgoritmin parametrit

Voit määrittää **Kohdistustunnukset**-välilehdessä kunkin kohdistustunnuksen **Ennustealgoritmin parametrit**. Valittavissa ovat seuraavat vaihtoehdot.
- **Luotettavuustasoprosentti**: Luottamusväli koostuu arvoalueesta, joka toimii hyvinä ennusteina kysynnän ennusteelle. 95 prosentin luotettavuustasoprosentti osoittaa, että on 5 prosentin riski siitä, että tuleva kysyntä on luottamusvälin ulkopuolella.
- **Pakota kausivaihtelu**: Määrittää, pakotetaanko malli käyttämään tietyn kausivaihtelutyyppiä. Koskee vain vaihtoehtoja ARIMA ja ETS. Vaihtoehdot: AUTO(oletus), NONE, ADDITIVE, MULTIPLICATIVE.
- **Ennustemalli**: vaihtoehdot: ARIMA, ETS, STL, ETS+ARIMA, ETS+STL, ALL. Valitse parhaiten sopiva malli käyttämällä **ALL**-vaihtoehtoa.
- **Ennusteen enimmäisarvo**: Määrittää ennusteissa käytettävän enimmäisarvon. Muoto: +1E[n] tai numeerinen vakio.
- **Ennusteen vähimmäisarvo**: Määrittää ennusteissa käytettävän vähimmäisarvon. Muoto: -1E[n] tai numeerinen vakio.
- **Puuttuvan arvon korvaus**: Määrittää, miten historiallisten tietojen aukot täytetään. Vaihtoehdot: numeerinen arvo, KESKIARVO, EDELLINEN, INTERPOLOI LINEAARINEN, INTERPOLOI POLYNOMINEN.
- **Puuttuvan arvon korvausalue**: Määrittää, koskeeko arvon korvaus vain kunkin yksittäisen rakeisuusmääritteen päivämääräaluetta vai koko tietojoukkoa. Vaihtoehdot: GRANULARITY_ATTRIBUTE(oletus), GLOBAL.
- **Kausivaihtelun vihje**: Anna ennustemallia varten kausivaihtelutietojen vihje ennusteen tarkkuuden parantamiseksi. Muoto: kokonaisluku, joka kuvaa niiden jaksojen pituutta, jolloin kysyntäkuvio toistuu. Syötä esimerkiksi luku 6, jos tiedot toistuvat kuuden kuukauden välein.
- **Testijoukon koon prosenttiosuus**: Historiatietojen prosenttiosuus käytettäväksi testiaineistona ennusteen tarkkuuden laskennassa. 

<a name="additional-resources"></a>Lisäresurssit
--------

[Kysynnän ennustepalveluiden yleiskatsaus](introduction-demand-forecasting.md)

[Tilastollisen perusennusteen luominen](generate-statistical-baseline-forecast.md)

[Manuaalisten oikaisujen tekeminen perusennusteeseen](manual-adjustments-baseline-forecast.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]