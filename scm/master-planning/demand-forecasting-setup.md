---
title: "Kysynnän ennusteiden asetukset"
description: "Tässä ohjeaiheessa kuvataan asetustehtävät, jotka sinun on suoritettava kysynnän ennusteita valmistellessasi."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ReqDemPlanDefaultAlgorithmParameters, ReqDemPlanForecastParameters
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 72653
ms.assetid: c5fa4b09-512d-4349-ac51-cc13da69a160
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: f629329f4f50bd7c8edcfd70641bace01a1c53aa
ms.lasthandoff: 03/31/2017


---

# <a name="demand-forecasting-setup"></a>Kysynnän ennusteiden asetukset

Tässä ohjeaiheessa kuvataan asetustehtävät, jotka sinun on suoritettava kysynnän ennusteita valmistellessasi.  

Määritystehtäviin kuuluu seuraavien tietojen ja parametrien asettaminen:

## <a name="item-allocation-key"></a>Nimikkeenkohdistustunnus
Kysynnän ennuste lasketaan nimikkeelle ja sen dimensioille vain, jos nimike on nimikkeen kohdistustunnuksen osa. Tämä sääntö on voimassa ryhmän suuren määrän kohteita, siten, että voidaan luoda myyntiennusteita nopeammin. Nimikkeen kohdistus prosentteina ohitetaan, kun kysynnän ennusteet luodaan. Ennusteet luodaan pelkästään historiallisten tietojen perusteella. 

Nimikkeen ja sen dimensioiden on oltava osa vain yhtä nimikkeen kohdistustunnusta, jos tätä nimikkeen kohdistustunnusta käytetään ennusteen luonnin aikana. 

Siirry lisättävä nimikkeenvaraustunnuksen varastointiyksikkö (SKU) **Master planning**&gt;**asennus**&gt;**kysynnän ennusteiden**&gt;**Nimikkeen kohdistustunnukset**. Määritä nimike kohdistustunnukselle **Määritä nimikkeet** -sivulla.

## <a name="intercompany-planning-groups"></a>Konsernin sisäiset suunnitteluryhmät
Kysynnän ennusteet luovat kaikki yritykset kattavia ennusteita. Microsoft Dynamics-365 operaatioille yritykset, jotka on suunniteltu yhdessä on ryhmitetty yhden konsernin sisäiseen suunnitteluryhmään. Yrityskohtainen Nimikekohdistuskoodeja mitä voidaan pitää kysynnän ennusteet, Määritä liittää nimikkeenvaraustunnuksen konsernin jäsen suunnittelu siirtymällä **Master planning**&gt;**asennus**&gt;**konsernin sisäisten suunnitteluryhmien**. 

Oletusarvon mukaan Jos Nimikekohdistuskoodeja ei ole liitetty konsernin sisäisen suunnitteluryhmän jäsenet, kysynnän ennuste lasketaan kaikille nimikkeille, jotka on määritelty kaikki Nimikekohdistuskoodeja kaikki Dynamics 365-yritysten toimintoja. Lisäsuodatusvaihtoehtoja yrityksille ja nimikkeen kohdistustunnuksille löytyy **Luo tilastollinen perusennuste** -sivulta. 

Tarkista nimikkeiden ennustettu lukumäärä. Tarpeettomat nimikkeet saattavat aiheuttaa lisäkustannuksia käyttäessäsi Microsoft Azure automaattianalyysipalvelua.

## <a name="demand-forecasting-parameters"></a>Kysynnän ennusteen parametrit
Kysynnän ennusteet parametrit määrittääksesi, siirry **Master planning**&gt;**asennus**&gt;**kysynnän ennusteet parametrit**. Koska kysynnän ennusteet suoritetaan kaikki yritykset kattavasti, asetukset yleiset. Asetukset koskevat toisin sanoen kaikkia yrityksiä. 

Kysynnän ennusteet luovat ennusteet lukumäärinä. Näin ollen mittayksikkö, jossa määrä ilmaistaan, on määritettävä **Kysynnän ennusteen yksikkö** -kentässä. Mittayksikön on oltava yksilöivä sen varmistamiseksi, että kooste ja prosenttijakauma ovat järkevät. Lisätietoja koosteesta ja prosenttijakaumasta on kohdassa [Manuaalisten muutosten tekeminen perusennusteeseen](manual-adjustments-baseline-forecast.md). Varmista, että jokaiselle mittayksikölle, jota käytetään kysynnän ennusteeseen sisältyvälle varastointiyksikölle, on muuntosääntö kyseiselle mittayksikölle ja yleinen ennusteen mittayksikkö. Kysynnän ennustetta luotaessa niiden nimikkeiden luettelo, joilla ei ole mittayksikön muuntoa, kirjataan niin, että voit helposti korjata asetukset. 

Kysynnän ennusteita voidaan käyttää ennustamaan sekä riippuvaista että riippumatonta kysyntää. Jos esimerkiksi vain **Myyntitilaus**-valintaruutu on valittuna ja jos kaikki kysynnän ennusteessa huomioitavat nimikkeet ovat myytäviä nimikkeitä, järjestelmä laskee riippumattoman kysynnän. Tärkeitä alikomponentteja voidaan kuitenkin lisätä nimikkeen kohdistustunnuksille ja sisällyttää kysynnän ennusteisiin. Tässä tapauksessa, jos **Tuotantolinja**-valintaruutu on valittuna, lasketaan riippuvainen ennuste. 

Ennuste-operaatioille 365 Dynamics perusaikataulun luomiseen kahdella tavalla. Voit käyttää ennustemalleja historiallisten tietojen päällä, tai voit vain kopioida historialliset tiedot ennusteeseen. ** Kysynnän luontistrategia** -kentässä voit tehdä valinnan näiden kahden menetelmän välillä. Käytä ennustemalleja valitsemalla ** Azuren automaattianalyysipalvelu**. 

Napsauttamalla **Ennustedimensiot** sivun **Kysynnän ennusteen parametrit** vasemmassa ruudussa, voit myös valita kysynnän ennusteen luonnissa käytettävän ennustedimensioiden joukon. Ennustedimensio osoittaa ennusteelle määritetyn erittelytason. Yritys, toimipaikka ja nimikkeen kohdistustunnus ovat pakollisia ennustedimensioita, mutta voit myös luoda ennusteita varastossa, varaston tilan, asiakasryhmän, asiakastilin, maan/alueen, osavaltion ja nimikkeen sekä kaikkien nimikedimensioiden tasoilla. 

Voit missä tahansa vaiheessa lisätä ennustedimensioita kysynnän ennusteissa käytettävien dimensioiden luetteloon. Voit myös poistaa ennustedimensioita luettelosta. Manuaaliset muutokset kuitenkin menetetään, jos lisäät tai poistat ennustedimension. 

Kaikki nimikkeet eivät toimi samalla tavalla kysynnän ennusteiden näkökulmasta. Samanlaisia nimikkeitä voidaan ryhmittää yhteen nimikkeen kohdistustunnukseen ja tapahtumatyypin ja ennustemenetelmän asetusten kaltaisille parametreille voidaan määrittää asetuksia nimikkeen kohdistustunnuskohtaisesti. Valitse **Kysynnän ennusteen parametrit** -sivun vasemmanpuoleisesta ruudusta **Nimikkeen kohdistustunnukset**. 

Luo ennuste, Dynamics 365 työvaiheiden käyttää Machine Learning web-palveluun. Voit muodostaa yhteyden palveluun, sinun on annettava Dynamics 365 toiminnot seuraavat tiedot Jos kirjaudut Microsoftin Azure Machine Learning Studio:

-   Verkkopalvelun ohjelmointirajapinta- (API)-avain
-   Verkkopalvelun päätepisteen URL-osoite
-   Azuren tallennustilin nimi
-   Azuren tallennustilin avain

**Huomautus:** Azuren tallennustilin nimi ja avain tarvitaan vain, jos käytät mukautettua tallennustiliä. Jos otat paikalliseen versiolla, Azure, mukautettu varastointi-tilin on oltava niin, että Machine Learning-palvelu käyttää historiallisia tietoja. 

Luo kysynnän laskentamenetelmää, voit ottaa oman palvelun avulla toimia kysynnän ennusteet kokeisiin Machine Learning Studio- tai Dynamics-365. Dynamics-365 toimia kysynnän ennusteet kokeisiin WWW-palvelulle käyttöönotto-ohjeita on käytettävissä Dynamics 365 operaatioille. Valitse **Kysynnän ennusteen parametrit** -sivulla **Azuren automaattianalyysipalvelut** -välilehti.

## <a name="settings-for-the-dynamics-365-for-operations-demand-forecasting-machine-learning-service"></a>Kysynnän Ennustaminen machine learning palvelun asetukset saat toimintoihin Dynamics-365
Voit tarkastella parametrit, jotka voidaan määrittää Dynamics 365 kysynnän Ennustaminen palvelun toimintoja varten, **Pääsuunnittelu**&gt;**asennus**&gt;**kysynnän ennusteiden**&gt;**ennusteet algoritmiparametrit**. **Ennusteet algoritmiparametrit** sivu näyttää parametrien oletusarvot. Voit korvata nämä parametrit **kysynnän ennusteet parametrit** sivulla. Korvaa parametrit yleisesti**Yleinen** -välilehdessä, tai nimikkeen kohdistustunnuskohtaisesti **Nimikkeen kohdistustunnus** -välilehdessä. Nimikkeen kohdistustunnuksella korvattavat parametrit vaikuttavat vain kyseiseen nimikkeen kohdistustunnukseen määritettyjen nimikkeiden ennusteisiin.

<a name="see-also"></a>Lisätietoja
--------

[Introduction to demand forecasting](introduction-demand-forecasting.md)

[Generating a statistical baseline forecast](generate-statistical-baseline-forecast.md)

[Making manual adjustments to the baseline forecast](manual-adjustments-baseline-forecast.md)


