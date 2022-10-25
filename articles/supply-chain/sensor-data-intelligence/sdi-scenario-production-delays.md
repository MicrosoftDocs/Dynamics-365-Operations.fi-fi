---
title: Tuotannon viiveiden skenaario
description: Tässä artikkelissa kerrotaan tuotannon viiveiden skenaariosta. Se luo ilmoituksen, jos tuotannon siirtomäärä on alle määritetyn raja-arvon.
author: johanhoffmann
ms.date: 09/02/2022
ms.topic: article
ms.search.form: IoTIntCoreScenarioManagement, IoTIntCoreScenarioConfigurationWizardV2, IoTIntMfgResourceStatusConfiguration, IoTIntMfgResourceStatus
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-09-02
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: 25ccbda1628544f14dc32d9bea3f2162ad47d79e
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/18/2022
ms.locfileid: "9690018"
---
# <a name="the-production-delays-scenario"></a>Tuotannon viiveiden skenaario

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!-- KFM: Preview until further notice -->

*Tuotannon viiveiden* skenaario luo ilmoituksen, jos tuotantokapasiteetti alittaa tietyn raja-arvon. Tässä skenaariossa kunkin tuotetun nimikkeen *osa ulos* -signaali lähetetään Microsoft Azure IoT -keskittimeen. Dynamics 365 Supply Chain Managementissa tilausviive lasketaan sen ajan perusteella, joka tuotantotilausta on tarkoitus suorittaa, tuotettavien nimikkeiden määrän perusteella, tehtävän käynnissäoloajan perusteella sekä vastaanotettujen *osa ulos* -signaalien perusteella. Viiveilmoitus luodaan, jos työn *osa ulos* -signaalien määrä alittaa raja-arvon.

## <a name="scenario-dependencies"></a>Skenaarion riippuvuudet

*Tuotannon viiveiden* skenaariossa on seuraavat riippuvuudet:

- Hälytys luodaan vain, jos tuotantotilaus on meneillään yhdistetyssä koneessa.
- Yhdistetyn koneen *osa ulos* -signaalia vastaava signaali on lähetettävä IoT-keskittimeen, ja signaalilla on oltava yksilöivä ominaisuuden nimi.
- Azuren IoT-keskittemen sanomassa on oltava UNIX-aikaleima-ominaisuus, jossa arvo ilmaistaan millisekunteina (ms).

## <a name="prepare-demo-data-for-the-product-delays-scenario"></a>Esittelytietojen valmisteleminen tuotteen viiveiden skenaariota varten

Jos haluat käyttää esittelyjärjestelmää *tuotteen viiveiden* skenaarion testaamisessa, käytä järjestelmää, jossa [esittelytiedot](../../fin-ops-core/fin-ops/get-started/demo-data.md) on asennettu. Valitse *USMF*-yritys ja valmistele esittelytiedot tässä osassa kuvatulla tavalla. Jos käytössä ovat omat tunnistimet ja tiedot, voit ohittaa tämän osan.

### <a name="set-up-sensor-simulator"></a>Tunnistinsimulaattorin määrittäminen

Jos haluat yrittää tätä skenaariota ilman fyysistä tunnistinta, voit määrittää simulaattorin vaadittujen signaalien luomista varten. Lisätietoja on kohdassa [Simuloidun tunnistimen määrittäminen testaamista varten](sdi-set-up-simulated-sensor.md).

### <a name="verify-that-resource-3118-is-used-for-product-p0111"></a>Vahvista, että tuotteessa P0111 käytetään resurssia 3118

Tuotantotilaus ajoitetaan ja vapautetaan. Tästä syystä tuotantotyö vapautetaan resurssille *3118* (*vaahtomuovia leikkaava kone*). Alla olevien vaiheiden avulla voit vahvistaa, että esittelytietojen tuotteessa *P0111* käytetään resurssia *3118*.

1. Mene **Tuotetietojen hallinta \> Tuotteet \> Vapautetut tuotteet**.
1. Etsi ja valitse tuote, jossa **Nimiketunnus**-kentän arvoksi on määritetty *P0111*.
1. Valitse toimintoruudun **Suunnittele**-välilehden **Näkymä**-ryhmässä **Reitti**.
1. Valitse **Reitti**-sivun alaosassa olevassa **Yleiskatsaus**-välilehdessä rivi, jossa **Työvaihenro**-kentän arvoksi on määritetty *30*.
1. Varmista sivun alaosassa olevassa **Resurssivaatimukset**-välilehdessä, että resurssi *3118* (*vaahtomuovia leikkaava kone*) on liitetty toimintoon.

### <a name="create-and-release-a-production-order-for-product-p0111"></a>Tuotteen P0111 tuotantotilauksen vapauttaminen ja luominen

Alla olevien vaiheiden avulla voit luoda ja vapauttaa tuotteen *P0111* tuotantotilauksen.

1. Siirry kohtaan **Tuotannonhallinta \> Tuotantotilaukset \> Kaikki tuotantotilaukset**.
1. Valitse **Kaikki tuotantotilaukset** -sivun toimintoruudussa **Uusi erätilaus**.
1. Määritä **Luo erä** -valintaikkunassa seuraavat arvot:

    - **Nimiketunnus:** *P0111*
    - **Määrä** *10*

1. Valitse **Luo** tilauksen luomiseksi ja palaa **Kaikki tuotantotilaukset** -sivulle.
1. Hae **Suodata**-kentän avulla tuotantotilaukset, joiden **Nimikenumero**-kentän arvoksi on määritetty *P0111*. Etsi ja valitse sitten juuri luomasi tuotantotilaus.
1. Valitse toimintoruudun **Tuotantotilaus**-välilehden **Käsittely**-ryhmässä **Arvio**.
1. Valitse **Arvioi**-valintaruudussa **OK** arvion suorittamiseksi.
1. Valitse toimintoruudun **Tuotantotilaus**-välilehden **Käsittely**-ryhmässä **Vapauta**.
1. Määritä **Vapauta**-valintaikkunassa juuri luotujen erätilausten määrä.
1. Vapauta tilaus valitsemalla **OK**.

### <a name="configure-the-production-floor-execution-interface"></a>Tuotannon käyttöliittymän määrittäminen

Määritä tuotannon käyttöliittymä näyttämään työt, jotka on määritetty resurssille *3118* (*vaahtomuovia leikkaava kone*), jos tätä ei ole vielä tehty. Lisätietoja on seuraavissa osissa:

- [Tuotannon käyttöliittymän määrittäminen](sdi-scenario-equipment-downtime.md#config-pfe)
- [Ota käyttöön hakuvalinta tuotannon käyttöliittymässä](sdi-scenario-equipment-downtime.md#enable-pfe-search)

### <a name="start-the-first-job-in-the-batch-order"></a>Erätilauksen ensimmäisen työn käynnistäminen

Aloita erätilauksen ensimmäinen työ noudattamalla näitä ohjeita.

1. Valitse **Tuotannonhallinta \> Tuotannonohjaus \> Tuotantoliittymä**.
1. Syötä **Merkin tunnus** -kenttään *123*. Valitse sitten **Kirjaudu sisään**.
1. Jos sinua pyydetään antamaan poissaolon syy, valitse jokin poissaolon kortti ja valitse sitten **OK**.
1. Syötä **Hae**-kenttään sen erätilauksen numero, josta tehtiin huomautus aiemmin. Valitse sitten **palautuksen** avain.
1. Valitse tilaus ja valitse sitten **Aloita työ**.
1. Valitse **Käynnistä työ** -valintaikkunassa **Käynnistä**.

## <a name="set-up-the-production-delays-scenario"></a>Tuotannon viiveiden skenaarion määrittäminen

Alla olevien vaiheiden avulla voit määrittää *tuotannon viiveiden* skenaarion Supply Chain Managementissa.

1. Siirry kohtaan **Tuotannonhallinta \> Määritys \> Sensor Data Intelligence \> Skenaariot**.
1. Valitse **tuotannon viiveiden** skenaarion ruudussa **Määritä**, jos haluat avata tämän skenaarion ohjatun asennuksen.
1. Valitse **Tunnistimet**-sivulla **Uusi** lisätäksesi tunnistimen ruudukkoon. Määritä sitten seuraavat kentät:

    - **Tunnistimen tunnus** – Syötä käytössä olevan tunnistimen tunnus. (Jos käytössä on Raspberry PI Azure IoT -verkkosimulaattori ja se on määritetty kohdan [Simuloidun tunnistimen määrittäminen testausta varten](sdi-set-up-simulated-sensor.md) ohjeiden mukaan, valitse *ProductionDelay*.)
    - **Tunnistimen kuvaus** – Syötä tunnistimen kuvaus.

1. Toista edellinen vaihe kullekin nyt lisättävälle lisätunnistimelle. Voit milloin tahansa palata takaisin ja lisätä tunnistimia.
1. Valitse **Seuraava**.
1. Valitse **Liiketoimintatietueen yhdistämismääritys** -sivun **Tunnistimet**-osassa jonkin juuri lisätyn tunnistimen tietue.
1. Valitse **Liiketoimintatietueen yhdistämismääritys** -osassa **Uusi** lisätäksesi ruudukkoon rivin.
1. Määritä uudella rivillä **Liiketoimintatietue** resurssissa, jossa valittu tunnistin on käytössä seurantaa varten. (Jos käytössä ovat aiemmin tässä artikkelissa luodut esittelytiedot, määritä arvoksi *3118, vaahtomuovia leikkaava kone*.)
1. Valitse **Seuraava**.
1. Jos **Tuotannon viiveen poikkeaman raja** -sivulla käytössä ovat esittelytiedot, jotka luotiin aiemmin tässä artikkelissa, noudata seuraavia vaiheita:

    1. Valitse **Nimikesuhde**-sarakkeen otsikko, jos haluat avata avattavan valintaikkunan, joka sisältää sarakkeen hakusuodattimet. Syötä hakuruutuun *P0111* ja valitse **Käytä**.
    2. Valitse rivi, jonka **Toiminto**-kentän arvoksi on määritetty *Lyhennä/leikkaa*. Määritä **Viiveen ilmoitusraja (%)** -kenttään raja-arvo (prosenttiosuutena), joka ilmoituksen tulee lähettää.

1. Valitse **Seuraava**.
1. Valitse **Aktivoi tunnistimet** -sivulla lisätty tunnistin ja valitse sitten **Aktivoi**. Ruudukon jokaiselle aktivoidulle tunnistimelle tulee näkyviin valintamerkki **Aktiivinen**-sarakkeessa.
1. Valitse **Valmis**.

## <a name="work-with-the-production-delays-scenario"></a>Tuotannon viiveiden skenaarion käsitteleminen

### <a name="view-production-delay-data-on-the-resource-status-page"></a>Tuotannon viiveen tietojen tarkasteleminen Resurssin tila -sivulla

**Resurssin tila** -sivulla esimiehet voivat seurata kuhunkin koneen resurssiin yhdistettyjen tunnistimien signaalien aikajanaa. Alla olevien vaiheiden avulla voit määrittää aikajanan.

1. Valitse **Tuotannonhallinta \> Tuotannonohjaus \> Resurssin tila**.
1. Määritä seuraavat kentät **Määritä**-valintaruudussa:

    - **Resurssi** – Valitse resurssit, joita haluat valvoa. (Jos työskentelet esittelytietojen parissa, valitse *3118*.)
    - **Aikasarja 1** – Valitse tietue (mittariavain), jolla on seuraava muoto nimessä: *ProductionJobDelayed:ActualQuantity:&lt;JobId&gt;*
    - **Näyttönimi** – Syötä *osat ulos -signaali*.
