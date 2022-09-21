---
title: Resurssien ylläpitoskenaario
description: Tässä artikkelissa kerrotaan resurssien ylläpitoskenaariosta, jonka avulla voit käyttää tunnistimien tietoja koneen resurssin käyttöä seuraavien laskuritietueiden luomisessa.
author: johanhoffmann
ms.date: 09/02/2022
ms.topic: article
ms.search.form: IoTIntCoreScenarioManagement, IoTIntCoreScenarioConfigurationWizardV2, EntAssetCounter
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-09-02
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: ff3944b987314a688a5829b05f8627479e3e79ed
ms.sourcegitcommit: 3d7ae22401b376d2899840b561575e8d5c55658c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/08/2022
ms.locfileid: "9428343"
---
# <a name="the-asset-maintenance-scenario"></a>Resurssien ylläpitoskenaario

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

*Resurssien ylläpitoskenaarion* avulla voit käyttää tunnistimen tietoja laskuritietueiden luomisessa. Laskuritietueet seuraavat koneen resurssin käyttöä. Niitä käytetään tulosteina luotaessa koneen resurssien ylläpitoaikataulua.

## <a name="prepare-demo-data-for-the-asset-maintenance-scenario"></a>Esittelytietojen valmisteleminen resurssien ylläpitoskenaariota varten

Jos haluat käyttää esittelyjärjestelmää *resurssien ylläpitoskenaarion* testaamisessa, käytä järjestelmää, jossa [esittelytiedot](../../fin-ops-core/fin-ops/get-started/demo-data.md) on asennettu. Valitse *USMF*-yritys ja valmistele esittelytiedot tässä osassa kuvatulla tavalla. Jos käytössä ovat omat tunnistimet ja tiedot, voit ohittaa tämän osan.

Tässä osassa määritetään *AK-101, ilmaveitsi* -resurssi esittelytiedoissa esimerkkinä. Tämän jälkeen näet, miten tuleva ylläpitotyö voidaan ennustaa tunnistimien signaalien perusteella. Tunnistimet mittaavat niiden tuntien määrää, jonka ilmaveitsi on ollut käytössä. Voit myös määrittää ylläpitosuunnitelman, jossa ilmaveitsen ylläpito on tehtävä joka 10 000 tunnin välein.

### <a name="set-up-a-sensor-simulator"></a>Tunnistinsimulaattorin määrittäminen

Jos haluat yrittää tätä skenaariota ilman fyysistä tunnistinta, voit määrittää simulaattorin vaadittujen signaalien luomista varten. Lisätietoja on kohdassa [Simuloidun tunnistimen määrittäminen testaamista varten](sdi-set-up-simulated-sensor.md).

### <a name="create-an-asset-counter-to-track-production-hours"></a>Resurssin laskimen luominen tuotantotuntien seuraamista varten

Alla olevien vaiheiden avulla voit luoda resurssin laskimen tuotantotuntien seuraamista varten.

1. Valitse **Resurssien hallinta \> Asetukset \> Resurssityypit \> Laskurit**.
1. Valitse toimintoruudussa **Uusi** ja luo laskuri.
1. Määritä otsikossa seuraavat arvot:

    - **Laskuri:** *ProductionHr*
    - **Nimi:** *Tuotantotunnit*

1. Määritä **Yleiset**-pikavälilehdessä seuraavat arvot:

    - **Yksikkö:** *tunti*
    - **Päivitys:** *Manuaalinen*
    - **Koonti yhteensä:** *Summa*

1. Valitse **Resurssityypit**-pikavälilehdessä **Lisää rivi**.
1. Määritä uuden rivin **Resurssityyppi**-kentän arvoksi *Ilmaveitsi*.

### <a name="create-a-maintenance-plan-for-the-asset"></a>Ylläpitosuunnitelman luominen resurssille

Alla olevien vaiheiden avulla voit luoda ylläpitosuunnitelman resurssille.

1. Valitse **Resurssien hallinta \> Asetukset \>Ennalta ehkäisevä ylläpito \>Ylläpitosuunnitelma**.
1. Valitse toimintoruudussa **Uusi** luodaksesi ylläpitosuunnitelman.
1. Määritä otsikossa seuraavat arvot:

    - **Ylläpitosuunnitelma:** *AirKnife*
    - **Nimi:** *Suunnitelma ilmaveistä varten*

1. Määritä **Tiedot**-pikavälilehdessä seuraavat arvot:

    - **Suunnitelman päivämäärä:** Syötä kuluva päivämäärä.
    - **Aktiivinen:** *Kyllä*

1. Lisää uusi rivi ruudukkoon **Rivit**-pikavälilehdessä **Lisää resurssin laskurin rivi**. Määritä sille sitten seuraavat arvot:

    - **Työtilauksen kuvaus:** *Ylläpito ilmaveistä varten*
    - **Ylläpitotyön tyyppi:** *Ennaltaehkäisevä*
    - **Välin tyyppi:** *Toistetaan viimeisestä työtilauksesta*
    - **Kausifrekvenssi:** *10 000*
    - **Laskuri:** *ProductionHr*

## <a name="set-up-the-asset-maintenance-scenario"></a>Resurssien ylläpitoskenaarion määrittäminen

Alla olevien vaiheiden avulla voit määrittää *resurssien ylläpitoskenaarion* Supply Chain Managementissa.

1. Siirry kohtaan **Resurssien hallinta \> Määritys \> Sensor Data Intelligence \> Skenaariot**.
1. Valitse **Resurssien ylläpitoskenaarion** ruudussa **Määritä**, jos haluat avata tämän skenaarion ohjatun asennuksen.
1. Valitse **Tunnistimet**-sivulla **Uusi** lisätäksesi tunnistimen ruudukkoon. Määritä sitten seuraavat kentät:

    - **Tunnistimen tunnus** – Syötä käytössä olevan tunnistimen tunnus. (Jos käytössä on Raspberry PI Azure IoT -verkkosimulaattori ja se on määritetty kohdan [Simuloidun tunnistimen määrittäminen testausta varten](sdi-set-up-simulated-sensor.md) ohjeiden mukaan, valitse *AssetMaintenance*.)
    - **Tunnistimen kuvaus** – Syötä tunnistimen kuvaus.

1. Toista edellinen vaihe kullekin nyt lisättävälle lisätunnistimelle. Voit milloin tahansa palata takaisin ja lisätä tunnistimia.
1. Valitse **Seuraava**.
1. Valitse **Liiketoimintatietueen yhdistämismääritys** -sivun **Tunnistimet**-osassa jonkin juuri lisätyn tunnistimen tietue.
1. Valitse **Liiketoimintatietueen yhdistämismääritys** -osassa **Uusi** lisätäksesi ruudukkoon rivin.
1. Uudella rivillä **Liiketoimintatietueen tyyppi** -kentän arvoksi tulisi automaattisesti päivittyä *Resurssit(EntAssetObjectTable)*. Määritä **Liiketoimintatietue**-kenttä resurssissa, jossa valittu tunnistin on käytössä seurantaa varten. (Jos käytössä ovat aiemmin tässä artikkelissa luodut esittelytiedot, määritä kentän arvoksi *AK-101, AK-101 ilmaveitsi linjalle 1*.)
1. Heti, kun edellisessä vaiheessa lisätylle riville on valittu liiketoimintatietueen tyyppi, ruudukkoon lisätään automaattisesti toinen rivi. Tällä rivillä **Liiketoimintatietueen tyyppi** -kentän arvoksi on määritettävä *Counters(EntAssetCounterType)*. Määritä **Liiketoimintatietue**-kenttä valitun tunnistimen signaalien mukaan päivitettävän resurssin laskurissa. (Jos käytössä ovat aiemmin tässä artikkelissa luodut esittelytiedot, määritä kentän arvoksi *ProductionHr, tuotantotunnit*.)
1. Valitse **Seuraava**.
1. Valitse **Aktivoi tunnistimet** -sivulla lisätty tunnistin ja valitse sitten **Aktivoi**. Ruudukon jokaiselle aktivoidulle tunnistimelle tulee näkyviin valintamerkki **Aktiivinen**-sarakkeessa.
1. Valitse **Valmis**.

## <a name="work-with-the-asset-maintenance-scenario"></a>Resurssien ylläpitoskenaarion käsitteleminen

### <a name="view-counter-values"></a>Laskurin arvojen tarkasteleminen

Kun tiedot on valmisteltu ja *resurssien ylläpitoskenaario* on määritetty ja aktivoitu, näet, miten resurssin laskurin tietueet lisätään tunnistimen tietojen perusteella.

1. Valitse **Resurssien hallinta \> Resurssit \> Kaikki resurssit**.
1. Etsi ja valitse tarkastettava resurssi. (Jos käytät aiemmin tässä artikkelissa luotuja esittelytietoja, valitse *AK-101*.)
1. Valitse toimintoruudun **Resurssi**-välilehden **Ennaltaehkäisevä**-ryhmässä **Laskurit**, jos haluat avata resurssin *AK-101* laskuritietueiden sivun.

### <a name="generate-maintenance-work-orders"></a>Ylläpitotyötilausten luominen

Kun *resurssien ylläpitoskenaario* on otettu käyttöön ja yläpitosuunnitelma on määritetty, voit suorittaa ylläpitoaikataulun ylläpitotyötilausten luomista varten. Lisätietoja ennaltaehkäisevän ylläpidon käsittelemisestä on kohdassa [Ennaltaehkäisevän ylläpidon yleiskatsaus](../asset-management/preventive-and-reactive-maintenance/preventive-maintenance-overview.md).
