---
title: "Kysynnän ennusteiden asetukset"
description: "Tässä ohjeaiheessa kuvataan asetustehtävät, jotka sinun on suoritettava kysynnän ennusteita valmistellessasi."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqDemPlanDefaultAlgorithmParameters, ReqDemPlanForecastParameters
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 72653
ms.assetid: c5fa4b09-512d-4349-ac51-cc13da69a160
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 74d520199410711b80b750a12ee726633e09d01c
ms.contentlocale: fi-fi
ms.lasthandoff: 06/13/2017

---

# <a name="demand-forecasting-setup"></a>Kysynnän ennusteiden asetukset

[!include[banner](../includes/banner.md)]


Tässä ohjeaiheessa kuvataan asetustehtävät, jotka sinun on suoritettava kysynnän ennusteita valmistellessasi.  

Määritystehtäviin kuuluu seuraavien tietojen ja parametrien asettaminen:

## <a name="item-allocation-key"></a>Nimikkeenkohdistustunnus
Kysynnän ennuste lasketaan nimikkeelle ja sen dimensioille vain, jos nimike on nimikkeen kohdistustunnuksen osa. Tätä sääntöä käytetään suurten nimikejoukkojen ryhmittämiseen niin, että kysynnän ennusteita voidaan luoda nopeammin. Nimikkeen kohdistustunnuksen prosenttiosuus ohitetaan kysynnän ennusteita luotaessa. Ennusteet luodaan pelkästään historiallisten tietojen perusteella. 

Nimikkeen ja sen dimensioiden on oltava osa vain yhtä nimikkeen kohdistustunnusta, jos tätä nimikkeen kohdistustunnusta käytetään ennusteen luonnin aikana. 

Varastointiyksikkö (SKU) lisätään nimikkeen kohdistustunnukselle kohdassa **Pääsuunnittelu** &gt; **Asetukset** &gt; **Kysynnän ennuste** &gt; **Nimikkeen kohdistustunnukset**. Määritä nimike kohdistustunnukselle **Määritä nimikkeet** -sivulla.

## <a name="intercompany-planning-groups"></a>Konsernin sisäiset suunnitteluryhmät
Kysynnän ennusteet luovat kaikki yritykset kattavia ennusteita. Microsoft Dynamics 365 for Finance and Operationsissa yritykset, joiden suunnittelu suoritetaan yhdessä, ryhmitetään yhdeksi konsernin sisäiseksi suunnitteluryhmäksi. Määritelläksesi yrityskohtaisesti mitkä nimikkeen kohdistustunnukset tulisi ottaa huomioon kysynnän ennusteissa, liitä nimikkeen kohdistustunnus konsernin suunnitteluryhmän jäseneen menemällä kohtaan **Pääsuunnittelu** &gt; **Asetukset** &gt; **Konsernin sisäiset suunnitteluryhmät**. 

Jos nimikkeen kohdistustunnuksia ei ole määritetty konsernin sisäisen suunnitteluryhmän jäsenille, kysynnän ennuste lasketaan oletusarvoisesti kaikille niille nimikkeille, jotka on määritetty kaikkiin nimikkeen kohdistustunnuksiin kaikista Finance and Operations -yrityksistä. Lisäsuodatusvaihtoehtoja yrityksille ja nimikkeen kohdistustunnuksille löytyy **Luo tilastollinen perusennuste** -sivulta. 

Tarkista nimikkeiden ennustettu lukumäärä. Tarpeettomat nimikkeet saattavat aiheuttaa lisäkustannuksia käyttäessäsi Microsoft Azure automaattianalyysipalvelua.

## <a name="demand-forecasting-parameters"></a>Kysynnän ennusteen parametrit
Määritä kysynnän ennusteen parametrit kohdassa **Pääsuunnittelu** &gt; **Asetukset** &gt; **Kysynnän ennusteen parametrit**. Koska kysynnän ennusteet suoritetaan kaikki yritykset kattavasti, asetukset yleiset. Asetukset koskevat toisin sanoen kaikkia yrityksiä. 

Kysynnän ennusteet luovat ennusteet lukumäärinä. Näin ollen mittayksikkö, jossa määrä ilmaistaan, on määritettävä **Kysynnän ennusteen yksikkö** -kentässä. Mittayksikön on oltava yksilöivä sen varmistamiseksi, että kooste ja prosenttijakauma ovat järkevät. Lisätietoja koosteesta ja prosenttijakaumasta on kohdassa [Manuaalisten muutosten tekeminen perusennusteeseen](manual-adjustments-baseline-forecast.md). Varmista, että jokaiselle mittayksikölle, jota käytetään kysynnän ennusteeseen sisältyvälle varastointiyksikölle, on muuntosääntö kyseiselle mittayksikölle ja yleinen ennusteen mittayksikkö. Kysynnän ennustetta luotaessa niiden nimikkeiden luettelo, joilla ei ole mittayksikön muuntoa, kirjataan niin, että voit helposti korjata asetukset. 

Kysynnän ennusteita voidaan käyttää ennustamaan sekä riippuvaista että riippumatonta kysyntää. Jos esimerkiksi vain **Myyntitilaus**-valintaruutu on valittuna ja jos kaikki kysynnän ennusteessa huomioitavat nimikkeet ovat myytäviä nimikkeitä, järjestelmä laskee riippumattoman kysynnän. Tärkeitä alikomponentteja voidaan kuitenkin lisätä nimikkeen kohdistustunnuksille ja sisällyttää kysynnän ennusteisiin. Tässä tapauksessa, jos **Tuotantolinja**-valintaruutu on valittuna, lasketaan riippuvainen ennuste. 

Perusennuste voidaan luoda Finance and Operationsissa kahdella tavalla. Voit käyttää ennustemalleja historiallisten tietojen päällä, tai voit vain kopioida historialliset tiedot ennusteeseen. **Kysynnän luontistrategia** -kentässä voit tehdä valinnan näiden kahden menetelmän välillä. Käytä ennustemalleja valitsemalla **Azuren automaattianalyysipalvelu**. 

Napsauttamalla **Ennustedimensiot** sivun **Kysynnän ennusteen parametrit** vasemmassa ruudussa, voit myös valita kysynnän ennusteen luonnissa käytettävän ennustedimensioiden joukon. Ennustedimensio osoittaa ennusteelle määritetyn erittelytason. Yritys, toimipaikka ja nimikkeen kohdistustunnus ovat pakollisia ennustedimensioita, mutta voit myös luoda ennusteita varastossa, varaston tilan, asiakasryhmän, asiakastilin, maan/alueen, osavaltion ja nimikkeen sekä kaikkien nimikedimensioiden tasoilla. 

Voit missä tahansa vaiheessa lisätä ennustedimensioita kysynnän ennusteissa käytettävien dimensioiden luetteloon. Voit myös poistaa ennustedimensioita luettelosta. Manuaaliset muutokset kuitenkin menetetään, jos lisäät tai poistat ennustedimension. 

Kaikki nimikkeet eivät toimi samalla tavalla kysynnän ennusteiden näkökulmasta. Samanlaisia nimikkeitä voidaan ryhmittää yhteen nimikkeen kohdistustunnukseen ja tapahtumatyypin ja ennustemenetelmän asetusten kaltaisille parametreille voidaan määrittää asetuksia nimikkeen kohdistustunnuskohtaisesti. Valitse **Kysynnän ennusteen parametrit** -sivun vasemmanpuoleisesta ruudusta **Nimikkeen kohdistustunnukset**. 

Finance and Operations käyttää automaattianalyysipalveluiden verkkopalvelua ennusteen luomiseen. Muodosta yhteys palveluun antamalla Finance and Operationsille seuraavat tiedot Microsoft Azuren automaattianalyysipalveluun kirjautumista varten:

-   Verkkopalvelun ohjelmointirajapinta- (API)-avain
-   Verkkopalvelun päätepisteen URL-osoite
-   Azuren tallennustilin nimi
-   Azuren tallennustilin avain

**Huomautus:** Azuren tallennustilin nimi ja avain tarvitaan vain, jos käytät mukautettua tallennustiliä. Jos käytät paikallista versiota, sinulla on oltava mukautettu tallennustili Azuressa niin, että automaattianalyysipalvelu voi käyttää historiallisia tietoja. 

Voit käyttää omaa palveluasi kysynnän ennusteiden luomiseen automaattianalyysipalvelun tai Finance and Operationsin kysynnän ennusteiden luomisen kokeilujen avulla. Ohjeet Dynamics 365 for Finance and Operationsin kysynnän ennusteiden luomisen kokeilujen käyttämiseen verkkopalveluna löytyy Finance and Operationsista. Valitse **Kysynnän ennusteen parametrit** -sivulla **Azuren automaattianalyysipalvelut** -välilehti.

## <a name="settings-for-the-finance-and-operations-demand-forecasting-machine-learning-service"></a>Finance and Operationsin kysynnän ennusteiden automaattianalyysipalvelun asetukset
Jos haluat tarkastella parametreja, jotka voidaan määrittää Finance and Operationsin kysynnän ennusteiden automaattianalyysipalveluille, siirry kohtaan **Pääsuunnittelu** &gt; **Asetukset** &gt; **Kysynnän ennuste** &gt; **Ennustealgoritmin parametrit**. **Ennustealgoritmin parametrit** sivu näyttää parametrien oletusarvot. Voit korvata nämä parametrit **Kysynnän ennusteen parametrit** -sivulla. Korvaa parametrit yleisesti **Yleinen** -välilehdessä, tai nimikkeen kohdistustunnuskohtaisesti **Nimikkeen kohdistustunnus** -välilehdessä. Nimikkeen kohdistustunnuksella korvattavat parametrit vaikuttavat vain kyseiseen nimikkeen kohdistustunnukseen määritettyjen nimikkeiden ennusteisiin.

<a name="see-also"></a>Lisätietoja
--------

[Kysynnän ennusteen esittely](introduction-demand-forecasting.md)

[Tilastollisen perusennusteen luonti](generate-statistical-baseline-forecast.md)

[Manuaalisten oikaisujen tekeminen perusennusteeseen](manual-adjustments-baseline-forecast.md)




