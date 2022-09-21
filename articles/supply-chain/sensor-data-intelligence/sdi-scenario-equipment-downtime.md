---
title: Koneen tilan skenaario
description: Tässä artikkelissa kerrotaan koneen tilan skenaario, jonka avulla voit käyttää tunnistimen tietoja laitteiston käytettävyyden seuraamista varten.
author: johanhoffmann
ms.date: 09/02/2022
ms.topic: article
ms.search.form: IoTIntCoreScenarioManagement, IoTIntCoreNotification, IoTIntMfgResourceStatusConfiguration, IoTIntMfgResourceStatus
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-09-02
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: 1f2b424dccf1963a7917059d412b5df7937496ee
ms.sourcegitcommit: 3d7ae22401b376d2899840b561575e8d5c55658c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/08/2022
ms.locfileid: "9428344"
---
# <a name="the-machine-status-scenario"></a>Koneen tilan skenaario

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

*Koneen tilan* skenaarion avulla voit käyttää tunnistimen tietoja laitteiston käytettävyyden seuraamista varten. Jos määrität tunnistimen, joka lähettää signaalin koneen resurssin tuotantotyön saadessa aikaan tuloksia, mutta tunnistimen signaalia ei vastaanoteta määritetyn aikavälin aikana, esimiehen koontinäytössä näkyy ilmoitus.

## <a name="scenario-dependencies"></a>Skenaarion riippuvuudet

*Koneen tilan* skenaariossa on seuraavat riippuvuudet:

- Ilmoitus luodaan vain, jos tuotantotyö on käynnissä yhdistetyssä koneessa.
- Signaali, joka edustaa *osa ulos* -signaalia, on lähetettävä IoT-keskittimeen.

## <a name="prepare-demo-data-for-the-machine-status-scenario"></a>Esittelytietojen valmisteleminen koneen tilan skenaariota varten

Jos haluat käyttää esittelyjärjestelmää *koneen tilan* skenaarion testaamisessa, käytä järjestelmää, jossa [esittelytiedot](../../fin-ops-core/fin-ops/get-started/demo-data.md) on asennettu. Valitse *USMF*-yritys ja valmistele esittelytiedot tässä osassa kuvatulla tavalla. Jos käytössä ovat omat tunnistimet ja tiedot, voit ohittaa tämän osan.

### <a name="set-up-a-sensor-simulator"></a>Tunnistinsimulaattorin määrittäminen

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

### <a name="configure-the-production-floor-execution-interface"></a><a name="config-pfe"></a>Tuotannon käyttöliittymän määrittäminen

Käytä tuotannon käyttöliittymää edellisessä osassa nimikenumerolle *P0111* ajoitetun ja vapautetun työn käynnistämisessä. Alla olevien vaiheiden avulla voit määrittää tuotannon käyttöliittymän.

1. Valitse **Tuotannonhallinta \> Tuotannonohjaus \> Tuotantoliittymä**.
1. Jos et ole määrittänyt liittymää aiemmin, näkyviin tulee sisäänkirjaussivu. Kirjota tunnistetiedot.
1. Valitse tervetulosivulla **Määritä**, jos haluat avata ohjatun **Määritä laite** -toiminnon.
1. Valitse **Määritä laite - vaihe 1 - valitse laite** -sivulla *oletusmääritys*.
1. Valitse **Seuraava**.
1. Määritä **Määritä laite - vaihe 2 - Määritä tuotantoalue** -sivulla **Resurssi**-kentän arvoksi *3118*.
1. Valitse **OK**.

### <a name="enable-the-search-option-in-the-production-floor-execution-interface"></a><a name="enable-pfe-search"></a>Ota käyttöön hakuvalinta tuotannon käyttöliittymässä

Ota hakuvalinta käyttöön tuotannon käyttöliittymässä alla olevien vaiheiden avulla, jos haluat helpottaa tuotantotyön etsimistä aiemmin vapautetusta tuotantotilauksesta.

1. Valitse **Tuotannonhallinta \> Asetukset \> Tuotannonohjaus \> Määritä tuotantoliittymä**.
1. Valitse *oletusmääritys*.
1. Valitse toimintoruudussa **Muokkaa**.
1. Määritä **Yleinen**-pikavälilehdessä **Ota haku käyttöön** -asetukseksi *Kyllä*.
1. Sulje sivu.

### <a name="start-the-first-job-in-the-batch-order"></a>Erätilauksen ensimmäisen työn käynnistäminen

Noudattamalla alla olevia vaiheita voit käynnistää resurssille *3118* ajoitetun työn.

1. Valitse **Tuotannonhallinta \> Tuotannonohjaus \> Tuotantoliittymä**.
1. Syötä **Merkin tunnus** -kenttään *123*. Valitse sitten **Kirjaudu sisään**.
1. Jos sinua pyydetään antamaan poissaolon syy, valitse jokin poissaolon kortti ja valitse sitten **OK**.
1. Syötä **Hae**-kenttään sen erätilauksen numero, josta tehtiin huomautus aiemmin. Valitse sitten **palautuksen** avain.
1. Valitse tilaus ja valitse sitten **Aloita työ**.
1. Valitse **Käynnistä työ** -valintaikkunassa **Käynnistä**.

## <a name="set-up-the-machine-status-scenario"></a>Koneen tilan skenaarion määrittäminen

Alla olevien vaiheiden avulla voit määrittää *koneen tilan* skenaarion Supply Chain Managementissa.

1. Siirry kohtaan **Tuotannonhallinta \> Määritys \> Sensor Data Intelligence \> Skenaariot**.
1. Valitse **Koneen tilan** skenaarion ruudussa **Määritä**, jos haluat avata tämän skenaarion ohjatun asennuksen.
1. Valitse **Tunnistimet**-sivulla **Uusi** lisätäksesi tunnistimen ruudukkoon. Määritä sitten seuraavat kentät:

    - **Tunnistimen tunnus** – Syötä käytössä olevan tunnistimen tunnus. (Jos käytössä on Raspberry PI Azure IoT -verkkosimulaattori ja se on määritetty kohdan [Simuloidun tunnistimen määrittäminen testausta varten](sdi-set-up-simulated-sensor.md) ohjeiden mukaan, valitse *MachineStatus*.)
    - **Tunnistimen kuvaus** – Syötä tunnistimen kuvaus.

1. Toista edellinen vaihe kullekin nyt lisättävälle lisätunnistimelle. Voit milloin tahansa palata takaisin ja lisätä tunnistimia.
1. Valitse **Seuraava**.
1. Valitse **Liiketoimintatietueen yhdistämismääritys** -sivun **Tunnistimet**-osassa jonkin juuri lisätyn tunnistimen tietue.
1. Valitse **Liiketoimintatietueen yhdistämismääritys** -osassa **Uusi** lisätäksesi ruudukkoon rivin.
1. Määritä uudella rivillä **Liiketoimintatietue**-kenttä resurssissa, jossa valittu tunnistin on käytössä seurantaa varten. (Jos käytössä ovat aiemmin tässä artikkelissa luodut esittelytiedot, määritä kentän arvoksi *3118, vaahtomuovia leikkaava kone*.)
1. Valitse **Seuraava**.
1. Määritä **Koneen tilan raja-arvo** -sivulla, miten kauan edellisen *osa ulos* -signaalin jälkeen järjestelmän on lähetettävä koneen tilan ilmoitus. Raja-arvon määrittämiseksi on kaksi seuraavaa tapaa:

    - **Oletusraja-arvo (minuutteja)** – Määritä tämä kenttä oletusraja-arvon määrittämistä varten. Arvoa käytetään tämän jälkeen kaikissa resursseissa, joissa **Raja-arvo, jolla määritetään koneen vastaamattomuusaika (minuutteina)** -kentän arvoksi on määritetty enintään kaksi minuuttia. Vähimmäisarvo on *2* (minuuttia).
    - **Raja-arvo, jolla määritetään koneen vastaamattomuusaika (minuutteina)** – Syötä ohitusarvo tähän kenttään kaikille ruudukon resursseille, joissa et halua käyttää oletusraja-arvoa. Resurssit, jotka on määritetty käyttämään enintään kahden minuutin raja-arvoa, käyttävät sen sijaan **Oletusraja-arvo (minuutteina)** -asetusta.

    > [!NOTE]
    > Yleensä koneen tilan seurannassa käytetään *osa ulos* -signaalia. Tämän vuoksi on varmistettava, että kunkin koneen resurssin raja-arvo on pidempi kuin koneen yksittäisen osan tuottamisessa vaadittu arvo.

1. Valitse **Seuraava**.
1. Valitse **Aktivoi tunnistimet** -sivulla lisätty tunnistin ja valitse sitten **Aktivoi**. Ruudukon jokaiselle aktivoidulle tunnistimelle tulee näkyviin valintamerkki **Aktiivinen**-sarakkeessa.
1. Valitse **Valmis**.

## <a name="work-with-the-machine-status-scenario"></a>Koneen tilan skenaarion käsitteleminen

Kun tunnistimet on asennettu ja skenaario määritetty, voit tarkastella koneen tilan tapahtumia Supply Chain Managementissa. Tässä osassa kerrotaan, missä ja miten näitä tietoja voi tarkastella.

### <a name="view-machine-status-data-on-the-resource-status-page"></a>Koneen tilatietojen tarkasteleminen Resurssin tila -sivulla

**Resurssin tila** -sivulla esimiehet voivat seurata kuhunkin koneen resurssiin yhdistettyjen tunnistimien *osa ulos* -signaalin aikajanaa. Alla olevien vaiheiden avulla voit määrittää aikajanan.

1. Valitse **Tuotannonhallinta \> Tuotannonohjaus \> Resurssin tila**.
1. Määritä seuraavat kentät **Määritä**-valintaruudussa:

    - **Resurssi** – Valitse resurssit, joita haluat valvoa. (Jos työskentelet esittelytietojen parissa, valitse *3118*.)
    - **Aikasarja 1** – Valitse tietue (mittariavain), jolla on seuraava muoto nimessä: *MachineReportingStatus:&lt;Sensor&gt;*
    - **Näyttönimi** – Syötä *osat ulos -signaali*.

Seuraavassa kuvassa on esimerkki koneen tilan tiedoista **Resurssin tilat** -sivulla vakiotoiminnon aikana.

![Koneen tilatiedot Resurssin tila -sivulla vakiotoiminnon aikana.](media/sdi-resource-status-downtime-up.png "Koneen tilan tiedot Resurssin tila -sivulla vakiotoiminnon aikana")

Seuraavassa kuvassa on esimerkki koneen tilan tiedoista, kun käyttämättömyysaikaa havaitaan.

![Koneen tilan tiedot Resurssin tila -sivulla, kun käyttämättömyysaikaa havaitaan.](media/sdi-resource-status-downtime-down.png "Koneen tilan tiedot Resurssin tila -sivulla, kun käyttämättömyysaikaa havaitaan")

### <a name="view-machine-status-on-the-notifications-page"></a>Koneen tilan tarkasteleminen Ilmoitukset-sivulla

Esimiehet voivat tarkastella **Ilmoitukset**-sivulla ilmoituksia, jotka luodaan, kun liian kauan aikaa on kulunut tunnistimen *osa ulos* -signaalin edellisestä toimittamisesta. Kukin ilmoitus antaa yhteenvedon tuotantotyöstä, johon käyttökatko vaikuttaa, ja antaa mahdollisuuden määrittää kyseinen työ uudelleen toiselle resurssille.

Avaa **Ilmoitukset**-sivu ja siirry kohtaan **Tuotannonhallinta \> Kyselyt ja raportit \> Sensor Data Intelligence \> Ilmoitukset**.

Seuraavassa kuvassa on koneen tilan ilmoituksen esimerkki.

![Esimerkki koneen tilan ilmoituksesta.](media/sdi-resource-status-downtime-notification.png "Esimerkki koneen tilan ilmoituksesta")
