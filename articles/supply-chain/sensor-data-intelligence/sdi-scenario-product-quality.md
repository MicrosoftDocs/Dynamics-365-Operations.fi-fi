---
title: Tuotteen laadun skenaario
description: Tässä artikkelissa on tietoja tuotteen laadun skenaariosta. Tässä skenaariossa käytetään tunnistinta tuote-erän laadun mittaamisessa. Jos mittausarvo on määritettyjen raja-arvojen ulkopuolella, luodaan hälytys.
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
ms.openlocfilehash: 8c4808ea3a0389c2a8699f0e11ea154705a6916d
ms.sourcegitcommit: 3d7ae22401b376d2899840b561575e8d5c55658c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/08/2022
ms.locfileid: "9428356"
---
# <a name="the-product-quality-scenario"></a>Tuotteen laadun skenaario

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

*Tuotteen laadun* skenaariossa tunnistin määritetään tuotannon tuote-erän laadun mittaamista varten. Jos mittausarvo ei ole tuotteelle määritettyjen raja-arvojen sisällä, esimiehen koontinäytössä näkyy ilmoitus. Tunnistin voi esimerkiksi mitata tuotantolinjalta tulevan ruokatuotteen kosteutta. Jos mittausarvo ei ole tuotteen kosteusarvon sallitun vähimmäis- ja enimmäisarvon sisällä, luodaan ilmoitus.

## <a name="scenario-dependencies"></a>Skenaarion riippuvuudet

*Tuotteen laadun* skenaariossa on seuraavat riippuvuudet:

- Hälytys voi käynnistyä vain, jos tuotantotilaus on käynnissä yhdistetyssä koneessa ja jos kone on valmistamassa tuotetta, jossa on yhdistetty erämäärite.
- IoT-keskittimeen lähetettävässä erämääritteen ilmaisevalla signaalilla on oltava yksilöivä ominaisuuden nimi.

## <a name="prepare-demo-data-for-the-product-quality-scenario"></a>Esittelytietojen valmisteleminen tuotteen laadun skenaariota varten

Jos haluat käyttää esittelyjärjestelmää *tuotteen laadun* skenaarion testaamisessa, käytä järjestelmää, jossa [esittelytiedot](../../fin-ops-core/fin-ops/get-started/demo-data.md) on asennettu. Valitse *USMF*-yritys ja valmistele esittelytiedot tässä osassa kuvatulla tavalla. Jos käytössä ovat omat tunnistimet ja tiedot, voit ohittaa tämän osan.

Tässä osassa määritetään esittelytiedot, jotta vapautettua tuotetta *P0111* (*komposiittilaukku*) voidaan käyttää *tuotteen laadun* skenaarion kanssa. Tässä skenaariossa järjestelmä seuraa, onko tunnistimen mittaama erämääritteen arvo tuotteeseen liitetyn erämääritteen raja-arvon ulkopuolella.

### <a name="set-up-a-sensor-simulator"></a>Tunnistinsimulaattorin määrittäminen

Jos haluat yrittää tätä skenaariota ilman fyysistä tunnistinta, voit määrittää simulaattorin vaadittujen signaalien luomista varten. Lisätietoja on kohdassa [Simuloidun tunnistimen määrittäminen testaamista varten](sdi-set-up-simulated-sensor.md).

### <a name="associate-a-batch-attribute-and-resource-with-product-p0111"></a>Erämääritteen ja resurssin liittäminen tuotteeseen P0111

Voit liittää erämääritteen tuotteeseen *P0111* (*komposiittilaukku*) ja vahvistaa, että siinä käytetään resurssia *3118* (*vaahtomuovia leikkaava kone*), seuraamalla alla olevia vaiheita.

1. Mene **Tuotetietojen hallinta \> Tuotteet \> Vapautetut tuotteet**.
1. Etsi ja valitse tuote, jossa **Nimiketunnus**-kentän arvoksi on määritetty *P0111*.
1. Valitse toimintoruudun **Hallitse varastoa** -välilehden **Erämääritteet**-ryhmässä **Tuotekohtainen**.
1. Valitse **Tuotekohtainen**-sivulla **Uusi**, jos haluat luoda tuotekohtaisen erämääritteen.
1. Määritä otsikossa seuraavat kentät:

    - **Määritekoodi** – Valitse valvottavien määritteiden laajuus (*Taulu*, *Ryhmä* tai *Kaikki*). Valitse tätä skenaariota varten *Taulu*, koska valvot aina yhtä määritettä.
    - **Määritesuhde** – Valitse määrite, jota käytetään *tuotteen laadun* skenaariossa arvon valvonnassa. Valitse tässä esimerkissä *Pitoisuus*. Tämä määrite sisältyy vakioesittelytietoihin.

1. Määritä **Arvot**-pikavälilehden **Vähimmäisarvo**- ja **Enimmäisarvo**-kentissä niiden hyväksyttävien arvojen väli, jotka määritteen raportoitava laatutarkistuksen hyväksymistä varten. Jos tunnistin raportoi tämän välin ulkopuolelle jäävän arvon, järjestelmä määrittää sen laaturikkomukseksi. Muut tämän pikavälilehden kentät eivät ole olennaisia *tuotteen laadun* skenaariossa. Tällä hetkellä käytettävissä olevat oletusarvot saadaan esittelytiedoista. Älä siis muuta niitä, vaan sulje **Tuotekohtainen**-sivu ja palaa nimikkeen *P0111* **Vapautetun tuotteen tiedot** -sivulle.
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

## <a name="set-up-the-product-quality-scenario"></a>Tuotteen laadun skenaarion määrittäminen

Alla olevien vaiheiden avulla voit määrittää *tuotteen laadun* skenaarion Supply Chain Managementissa.

1. Siirry kohtaan **Tuotannonhallinta \> Määritys \> Sensor Data Intelligence \> Skenaariot**.
1. Valitse **tuotteen laadun** skenaarion ruudussa **Määritä**, jos haluat avata tämän skenaarion ohjatun asennuksen.
1. Valitse **Tunnistimet**-sivulla **Uusi** lisätäksesi tunnistimen ruudukkoon. Määritä sitten seuraavat kentät:

    - **Tunnistimen tunnus** – Syötä käytössä olevan tunnistimen tunnus. (Jos käytössä on Raspberry PI Azure IoT -verkkosimulaattori ja se on määritetty kohdan [Simuloidun tunnistimen määrittäminen testausta varten](sdi-set-up-simulated-sensor.md) ohjeiden mukaan, valitse *Quality*.)
    - **Tunnistimen kuvaus** – Syötä tunnistimen kuvaus.

1. Toista edellinen vaihe kullekin nyt lisättävälle lisätunnistimelle. Voit milloin tahansa palata takaisin ja lisätä tunnistimia.
1. Valitse **Seuraava**.
1. Valitse **Liiketoimintatietueen yhdistämismääritys** -sivun **Tunnistimet**-osassa jonkin juuri lisätyn tunnistimen tietue.
1. Valitse **Liiketoimintatietueen yhdistämismääritys** -osassa **Uusi** lisätäksesi ruudukkoon rivin.
1. Uudella rivillä **Liiketoimintatietueen tyyppi** -kentän arvoksi tulisi automaattisesti päivittyä *Resurssit(WrkCtrTable)*. Määritä **Liiketoimintatietue**-kenttä resurssissa, jossa valittu tunnistin on käytössä seurantaa varten. (Jos käytössä ovat aiemmin tässä artikkelissa luodut esittelytiedot, määritä arvoksi *3118, vaahtomuovia leikkaava kone*.)
1. Heti, kun edellisessä vaiheessa lisätylle riville on valittu liiketoimintatietueen tyyppi, ruudukkoon lisätään automaattisesti toinen rivi. Tällä rivillä **Liiketoimintatietueen tyyppi** -kentän arvoksi on määritettävä *Erämääritteet(PdsBatchAttrib)*. Määritä **Liiketoimintatietue**-kenttä erämääritteessä, jossa valittu tunnistin on käytössä seurantaa varten. (Jos käytössä ovat aiemmin tässä artikkelissa luodut esittelytiedot, määritä kentän arvoksi *Pitoisuus, pitoisuusprosentti*.)
1. Valitse **Seuraava**.
1. Valitse **Aktivoi tunnistimet** -sivulla lisätty tunnistin ja valitse sitten **Aktivoi**. Ruudukon jokaiselle aktivoidulle tunnistimelle tulee näkyviin valintamerkki **Aktiivinen**-sarakkeessa.
1. Valitse **Valmis**.

## <a name="work-with-the-product-quality-scenario"></a>Tuotteen laadun skenaarion käsitteleminen

### <a name="view-product-quality-data-on-the-resource-status-page"></a>Tuotteen laatutietojen tarkasteleminen Resurssin tila -sivulla

**Resurssin tila** -sivulla esimiehet voivat seurata kuhunkin koneen resurssiin yhdistettyjen tunnistimien tuotteen laatusignaalin aikajanaa. Alla olevien vaiheiden avulla voit määrittää aikajanan.

1. Valitse **Tuotannonhallinta \> Tuotannonohjaus \> Resurssin tila**.
1. Määritä seuraavat kentät **Määritä**-valintaruudussa:

    - **Resurssi** – Valitse resurssit, joita haluat valvoa. (Jos työskentelet esittelytietojen parissa, valitse *3118*.)
    - **Aikasarja 1** – Valitse tietue (mittariavain), jolla on seuraava muoto nimessä: *ProductQuality:&lt;JobId&gt;:&lt;AttributeName&gt;*
    - **Näyttönimi** – Syötä *erämääritteen arvot*.

Seuraavassa kuvassa on esimerkki **Resurssin tila** -sivun tuotteen laatutiedoista, kun arvo hyväksytään.

![Tuotteen laatutiedot Resurssin tila -sivulla, kun arvo on sallitulla arvoalueella.](media/sdi-product-quality-in-range.png "Tuotteen laatutiedot Resurssin tila -sivulla, kun arvo on sallitulla arvoalueella")

Seuraavassa kuvassa on esimerkki tuotteen laatutiedoista, kun havaitaan arvoalueen ulkopuolinen arvo.

![Tuotteen laatutiedot Resurssin tila -sivulla, kun havaitaan sallitun arvoalueen ulkopuolinen arvo.](media/sdi-product-quality-out-of-range.png "Tuotteen laatutiedot Resurssin tila -sivulla, kun havaitaan sallitun arvoalueen ulkopuolinen arvo")

### <a name="view-product-quality-data-on-the-notifications-page"></a>Tuotteen laatutietojen tarkasteleminen Ilmoitukset-sivulla

**Ilmoitukset**-sivulla esimiehet voivat tarkastella ilmoitusta, joka luodaan tunnistimen mitatessa erämääritteen arvon, joka on erämääritteelle määritettyjen raja-arvojen ulkopuolella. Kukin ilmoitus antaa yhteenvedon tuotantotyöstä, johon käyttökatko vaikuttaa, ja antaa mahdollisuuden määrittää kyseinen työ uudelleen toiselle resurssille.

Avaa **Ilmoitukset**-sivu ja siirry kohtaan **Tuotannonhallinta \> Kyselyt ja raportit \> Sensor Data Intelligence \> Ilmoitukset**.

Seuraavassa kuvassa on tuotteen laadun ilmoituksen esimerkki.

![Esimerkki tuotteen laadun ilmoituksesta.](media/sdi-product-quality-notification.png "Esimerkki tuotteen laadun ilmoituksesta")
