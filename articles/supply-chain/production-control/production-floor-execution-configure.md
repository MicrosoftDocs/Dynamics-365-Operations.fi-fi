---
title: Tuotannon käyttöliittymän määrittäminen
description: Tässä artikkelissa käsitellään tuotannon käyttöliittymämääritysten luontia. Kun tuotannon käyttöliittymä avataan, se lataa automaattisesti selain- ja laitekohtaisen valitun määrityksen ja työsuodattimen. Määrityksessä määritetään käytännöt, joita on käytettävä tietyssä käyttötilanteessa.
author: johanhoffmann
ms.date: 10/05/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: JmgProductionFloorExecutionConfiguration
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-10-05
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 9eefde163473e11b01bfa0adf9b3694c830f1488
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8899408"
---
# <a name="configure-the-production-floor-execution-interface"></a>Tuotannon käyttöliittymän määrittäminen

[!include [banner](../includes/banner.md)]

Tuotannon työntekijät rekisteröivät tuotannon käyttöliittymällä päivittäisen työnsä, kuten töiden aloittamisen, töitä koskevan palautteen antamisen, epäsuorien tehtävien rekisteröimisen ja poissaolon raportoinnin. Nämä rekisteröinnit ovat perusta, jolla seurataan tuotantotilausten edistymistä ja kustannuksia sekä lasketaan työntekijöiden palkka.

Kun tuotannon käyttöliittymä avataan, se lataa automaattisesti selain- ja laitekohtaisen valitun määrityksen ja työsuodattimen. Määrityksessä määritetään käytännöt, joita on käytettävä tietyssä käyttötilanteessa. Esimerkkejä käytöstä:

- Laite on yrityksen aulassa, ja työntekijät kuittaavat itsensä sisään, kun he tulevat töihin, ja ulos, kun he lähtevät kotiin.
- Laite on tuotantotiloissa, ja koneen käyttäjät rekisteröivät milloin he aloittavat ja lopettavat työt. Tämän he rekisteröivät tauot ja epäsuorat tehtävät.

Tässä artikkelissa kuvataan eri vaihtoehdot tuotannon käyttöliittymän määritykselle kullekin toimipaikassa olevalle laitteelle.

## <a name="turn-on-the-production-floor-execution-interface-and-its-related-optional-features"></a>Tuotannon käyttöliittymän ja siihen liittyvien valinnaisten ominaisuuksien ottaminen käyttöön

Tuotannon käyttöliittymä sekä monet tässä artikkelissa käsiteltävät valinnaiset asetukset on otettava järjestelmässä käyttöön, ennen kuin niitä voi käyttää. Ota tarvittaessa näitä ominaisuuksia käyttöön [Ominaisuuksien hallinta](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) -sivulla seuraavissa alaosissa kuvatulla tavalla.

### <a name="the-production-floor-execution-interface"></a>Tuotannon käyttöliittymä

Tämä on ensisijainen tässä artikkelissa kuvattu toiminto ja edellytys kaikille muille tässä osassa mainitulle toiminnolle. Supply Chain Managementin versiosta 10.0.25 alkaen se on pakollinen, eikä sitä voi poistaa käytöstä. Jos käytät vanhempaa versiota kuin 10.0.25, järjestelmänvalvojat voivat ottaa tämän toiminnon käyttöön tai pois käytöstä hakemalla *Tuotannon toteutus* -toimintoa [Toimintojen hallinta](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) -työtilassa.

### <a name="generate-license-plates"></a>Rekisterikilpien muodostaminen

Näillä ominaisuuksilla rekisterikilpitoiminnot saadaan käyttöön tuotannon käyttöliittymässä. Jos haluat käyttää niitä, ota seuraavat ominaisuudet käyttöön [ominaisuuksien hallinnassa](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) (seuraavassa järjestyksessä):

1. *Rekisterikilpi valmiiksi raportointia varten on lisätty työkorttilaitteeseen*<br>(Supply Chain Managementin versiosta 10.0.21 alkaen tämä ominaisuus on oletusarvoisesti käytössä. Supply Chain Managementin versiosta 10.0.25 alkaen tämä ominaisuus on pakollinen.)
1. *Ota käyttöön rekisterikilven numeron automaattinen luonti, kun työkorttilaitteessa raportoidaan valmiiksi*<br>(Supply Chain Managementin versiosta 10.0.25 alkaen tämä ominaisuus on pakollinen.)

### <a name="print-labels"></a>Tulosta etiketit

Näillä ominaisuuksilla etikettitulostus saadaan käyttöön tuotannon käyttöliittymässä. Jos haluat käyttää niitä, ota seuraavat ominaisuudet käyttöön [ominaisuuksien hallinnassa](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) (seuraavassa järjestyksessä):

1. *Rekisterikilpi valmiiksi raportointia varten on lisätty työkorttilaitteeseen*<br>(Supply Chain Managementin versiosta 10.0.21 alkaen tämä ominaisuus on oletusarvoisesti käytössä. Supply Chain Managementin versiosta 10.0.25 alkaen tämä ominaisuus on pakollinen.)
1. *Tulosta etiketti työkorttilaitteesta*<br>(Supply Chain Managementin versiosta 10.0.25 alkaen tämä ominaisuus on pakollinen.)

### <a name="allow-locking-the-touch-screen"></a>Kosketusnäytön lukitsemisen salliminen

Tällä toiminnolla työntekijöiden voidaan sallia lukita kosketusnäyttö sen puhdistamista varten.

Supply Chain Managementin versiosta 10.0.21 alkaen tämä ominaisuus on poistettu oletusarvoisesti käytöstä. Supply Chain Managementin versiosta 10.0.25 alkaen tämä toiminto on pakollinen, eikä sitä voi poistaa käytöstä. Jos käytät vanhempaa versiota kuin 10.0.25, järjestelmänvalvojat voivat ottaa tämän toiminnon käyttöön tai pois käytöstä hakemalla *Toiminto, jolla voi lukita työkorttilaitteen ja työkorttipäätteen desinfiointia varten* -toimintoa [Toimintojen hallinta](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) -työtilasta.

### <a name="asset-management-functionality-for-the-production-floor-execution-interface"></a>Tuotannonohjausliittymän käyttöomaisuuden hallintatoiminto

Tämä toiminto lisää resurssien hallinnan välilehden tuotannon käyttöliittymään. Työtekijät voivat valita tässä välilehdessä siihen koneresurssiin liittyvän resurssin, joka on työluettelon valitussa suodattimessa. Työtekijä voi tarkastella valitun koneresurssin tilaa ja kuntoa enintään neljän valitun laskurin arvojen avulla. Jos haluat käyttää tätä toimintoa, ota seuraava toiminto käyttöön [ominaisuuksien hallinnassa](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md):

- *Tuotannonohjausliittymän käyttöomaisuuden hallintatoiminto*<br>(Supply Chain Managementin versiosta 10.0.25 alkaen tämä ominaisuus on oletusarvoisesti käytössä.)

### <a name="enable-job-search"></a>Työhaun ottaminen käyttöön

Tämän ominaisuuden avulla voit lisätä hakukentän työluetteloon. Työntekijät voivat etsiä tietyn työn syöttämällä työtunnuksen tai etsimällä tietyn tilauksen kaikki työt antamalla tilaustunnuksen. Työntekijät voivat syöttää tunnuksen näppäimistön avulla tai skannaamalla viivakoodia. Jos haluat käyttää sitä, ota seuraava ominaisuus käyttöön [ominaisuuksien hallinnassa](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md):

- *Töiden haku tuotannon työnohjausliittymälle*<br>(Supply Chain Managementin versiosta 10.0.25 alkaen tämä ominaisuus on oletusarvoisesti käytössä.)

### <a name="enable-reporting-on-co-products-and-by-products"></a>Oheis- ja sivutuotteiden raportoinnin käyttöönotto

Tämän ominaisuuden avulla työntekijät voivat käyttää tuotannon suoritusliittymää erätilausten edistymisen raportointiin. Tähän raportointiin kuuluu oheis- ja sivutuotteita koskeva raportointi. Jos haluat käyttää tätä toiminnallisuutta, ota seuraava ominaisuus käyttöön [Ominaisuuksienhallinnassa](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md):

- *Raportti tuotannon käyttöliittymän rinnakkais- ja sivutuotteista*

### <a name="enable-the-display-of-full-serial-batch-and-license-plate-numbers"></a>Ota käyttöön täysien sarjanumeroiden, eränumeroiden ja rekisterikilpinumeroiden näyttäminen

Tämä ominaisuus tarjoaa paremman käyttökokemuksen sarja-, erä- ja lisenssinumeroiden tarkastelusta tuotannonohjausliittymässä. Näyttö muuttuu korttinäkymästä niin, että näkyvissä on rajallinen määrä merkkejä luettelonäkymään, jossa on tarpeeksi tilaa näyttää kaikki arvot. Luettelossa on myös mahdollisuus etsiä tiettyjä numeroita.

Supply Chain Managementin versiosta 10.0.25 alkaen tämä ominaisuus on poistettu oletusarvoisesti käytöstä. Järjestelmänvalvojat voivat ottaa tämän toiminnon käyttöön tai pois käytöstä hakemalla *Näytä täydet sarja-, erä- ja rekisterinumerot tuotannon käyttöliittymässä* -toimintoa [Toimintojen hallinta](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) -työtilassa.

### <a name="enable-registering-of-material-consumption"></a>Ota käyttöön materiaalikulutuksen rekisteröinti

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]
<!-- KFM: preview until further notice -->

Tämän ominaisuuden avulla työntekijät voivat käyttää tuotannon työnohjausliittymää materiaalin kulutuksen, eränumeroiden ja sarjanumeroiden rekisteröimiseen. Joillekin valmistajille, erityisesti prosessiteollisuusalojen valmistajille, on nimenomaisesti rekisteröitävä kussakin erässä tai tuotantotilauksissa kulutettu materiaalimäärä. Työntekijät voivat esimerkiksi käyttää vaakaa punnitsemaan työssään kulutetun materiaalin määrän. Organisaatioiden on myös kirjattava kunkin tuotteen valmistamisen eränumerot varmistaakseen materiaalien jäljitettävyyden.

Tästä ominaisuudesta on kaksi versiota. Yksi toiminto tukee vain nimikkeitä, joita *ei ole* otettu käyttöön varaston lisäprosessien (WMS) käytössä. Toinen tukee nimikkeitä, jotka *on* otettu käyttöön käyttämään WMS:ää. Voit käyttää tätä toimintoa ottamalla käyttöön seuraavat ominaisuudet [ominaisuuksien hallinnassa](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) (tässä järjestyksessä) yhdellä tai molemmilla toiminnoilla sen mukaan, onko käytössä WMS-nimikkeitä:

- *(Esiversio) Rekisteröi materiaalin kulutus tuotannon käyttöliittymässä (muu kuin VHJ)*
- *(Esiversio) Rekisteröi materiaalikulutus tuotannon käyttöliittymässä (käytössä WMS:ssä)*

> [!IMPORTANT]
> Voit käyttää ei-WMS-toimintoa erikseen. Jos kuitenkin käytät WMS:ää, molemmat toiminnot on otettava käyttöön.

### <a name="enable-reporting-on-catch-weight-items"></a>Todellisen painon nimikkeiden raportoinnin ottaminen käyttöön

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]
<!-- KFM: preview until further notice -->

Työntekijät voivat käyttää tuotannon suoritusliittymää todellisen painon nimikkeiden erätilausten edistymisen raportointiin. Erätilaukset luodaan kaavojen perusteella, ja nämä kaavat voidaan määritellä siten, että niissä on todellisen painon nimikkeet kaavanimikkeinä, oheistuotteina ja sivutuotteina. Kaavan voi määrittää myös, jos kaavarivit on määritetty todellisen painon ainesosille. Todellisen painon nimikkeissä käytetään kahta mittayksikköä varaston seuraamiseksi: todellisen painon määrä ja varastomäärä. Esimerkiksi elintarviketeollisuudessa laatikollinen lihaa voidaan määrittää todellisen painon nimikkeeksi, jossa todellisen painon määrää käytetään laatikoiden määrän seuraamiseen, ja varastomäärää käytetään laatikoiden painon seuraamiseen.

Jos haluat käyttää tätä toiminnallisuutta, ota seuraava ominaisuus käyttöön [Ominaisuuksienhallinnassa](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md):

- *(Esiversio) Todellisen painon nimikkeiden raportointi tuotannon käyttöliittymästä*

### <a name="enable-the-my-day-dialog"></a>Päivän tehtävät -valintaikkunan ottaminen käyttöön

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]
<!-- KFM: preview until 10.0.27 GA -->

**Päivän tehtävät** -valintaikkunassa työntekijöille on yleiskuvaus päivittäisistä rekisteröinneistä ja palkallisen ajan, palkallisen ylityöajan, poissaolojen ja palkallisen poissaolon nykyisistä saldoista.

Jos haluat käyttää tätä toiminnallisuutta, ota seuraava ominaisuus käyttöön [Ominaisuuksienhallinnassa](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md):

- *Tuotannon käyttöliittymän Päivän tehtävät -näkymä*

### <a name="enable-teams"></a>Ota ryhmät käyttöön

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]
<!-- KFM: preview until 10.0.27 GA -->

Kun samaan tuotantotyöhön on liitetty useita työntekijöitä, he voivat muodostaa ryhmän. Tiimi voi nimetä yhden työntekijän vetäjäksi. Jäljellä olevista työntekijöistä tulee tämän jälkeen automaattisesti tämän vetäjän avustajia. Tuloksena olevassa ryhmässä vain vetäjän on rekisteröitävä työn tila. Aikatietueita käytetään kaikille ryhmän jäsenille.

Jos haluat käyttää tätä toiminnallisuutta, ota seuraava ominaisuus käyttöön [Ominaisuuksienhallinnassa](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md):

- *Tuotantoryhmät tuotannon käyttöliittymässä*

### <a name="enable-additional-configuration-in-the-production-floor-execution-interface"></a>Ota käyttöön lisämääritys tuotannon käyttöliittymässä

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]
<!-- KFM: preview until 10.0.27 GA -->

Tämä ominaisuus lisää seuraavien toimintojen asetukset **Määritä tuotannon suoritus** -sivulle:

- Avaa **Aloita työ**-valintaikkuna automaattisesti, kun haku on valmis.
- Avaa **Raportointi on meneillään**-valintaikkuna automaattisesti, kun haku on valmis.
- Voit täyttää jäljellä olevan määrän valmiiksi **Raportointi on meneillään** -valintaikkunassa.
- Ota käyttöön materiaalikulutuksen oikaisut **Raportointi on meneillään** -valintaikkunassa. (Tämä toiminto edellyttää myös *Rekisteröi materiaalin kulutus tuotannon käyttöliittymässä (muu kuin VHJ)* -toimintoa.)
- Ota projektin tunnus käyttöön hakuperusteena.

Tietoja asetusten käytöstä on jäljempänä tässä artikkelissa.

Jos haluat käyttää tätä toiminnallisuutta, ota seuraava ominaisuus käyttöön [Ominaisuuksienhallinnassa](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md):

- *Lisämääritys tuotannon käyttöliittymässä*


## <a name="work-with-production-floor-execution-configurations"></a>Tuotannon käyttöliittymämääritysten käyttäminen

Voit luoda ja ylläpitää tuotannon toteutuksen määrityksiä valitsemalla **Tuotannonhallinta \> Määritys \> Tuotannonohjaus \> Määritä tuotantoliittymä**. **Määritä tuotantoliittymä** -sivulla on luettelo aiemmin luoduista määrityksistä. Tällä sivulla voi tehdä seuraavia toimenpiteitä:

- Valitse vasemmassa sarakkeessa oleva tuotantomääritykset, jos haluat tarkastella ja muokata niitä.
- Valitse toimintoruudusta **Uusi**, kun haluat lisätä luetteloon uuden konfiguraation. Anna sitten **Määritys**-kenttään nimi, jolla uusi määritys on helppo tunnistaa. Annetun nimen oltava yksilöivä kaikkien määritysten joukossa, eikä sitä voi muokata myöhemmin. Voit valinnaisesti antaa määrityksen kuvauksen **Kuvaus**-kentässä.

Määritä seuraavaksi valitun konfiguraation eri asetukset seuraavissa aliosissa kuvatulla tavalla.

### <a name="the-general-fasttab"></a>Yleiset-pikavälilehti

**Yleiset** -pikavälilehdessä on seuraavat tiedot.

- **Vain sisään- ja uloskirjaus** – Määritä tämän asetuksen arvoksi *Kyllä*, jos haluat luoda yksinkertaistetun liittymän, jossa on vain sisään- ja uloskirjaustoiminnot. Tämä asetus poistaa suurimman osan sivun muista asetuksista käytöstä. Ennen tämän asetuksen käyttöönottoa on poistettava kaikki rivit **Välilehtivalinta**-pikavälilehdestä.
- **Ota haku käyttöön** – Määritä tämän asetuksen arvoksi *Kyllä*, jos haluat sisällyttää työluetteloon hakukentän. Työntekijät voivat etsiä tietyn työn syöttämällä työtunnuksen tai etsimällä tietyn tilauksen kaikki työt antamalla tilaustunnuksen. Työntekijät voivat syöttää tunnuksen näppäimistön avulla tai skannaamalla viivakoodia.
- **Ota projektin tunnus käyttöön hakuperusteena** – Määritä tämän asetuksen arvoksi *Kyllä*, kun haluat, että työntekijät voivat tehdä hakuja projektin tunnuksen (työtunnuksen ja tilaustunnuksen lisäksi) perusteella tuotannon käyttöliittymän hakukentässä. Voit määrittää tämän asetuksen arvoksi *Kyllä* vain, jos **Ota haku käyttöön** -asetuksen arvoksi on myös määritetty *Kyllä*.
- **Avaa aloitusikkuna automaattisesti** – *Kyllä*-vaihtoehtoa käytettäessä **Aloita työ** -valintaikkuna avautuu automaattisesti, kun työntekijät etsivät työtä hakurivin avulla.
- **Avaa Raportointi on meneillään -ikkuna automaattisesti** – *Kyllä*-vaihtoehtoa käytettäessä **Raportointi on meneillään** -valintaikkuna avautuu automaattisesti, kun työntekijät etsivät työtä hakurivin avulla.
- **Ota materiaalin oikaisu käyttöön** – Ota **Materiaalin oikaiseminen** käyttöön **Raportointi on meneillään** -valintaikkunassa valitsemalla *Kyllä*. Työntekijät voivat säätää kunkin tuotantotyön materiaalikulutusta valitsemalla tämän painikkeen.
- **Ilmoita määrä uloskuittauksessa** – Määritä asetukseksi *Kyllä*, jos haluat, että työntekijöitä pyydetään antamaan palautetta meneillään olevista töistä, kun he kuittaavat itsensä ulos. Jos asetuksena on *Ei*, työntekijät eivät saa tätä kehotetta.
- **Lukitse työntekijä** – Jos asetuksena on *Ei*, työntekijät kirjautuvat ulos heti, kun he tekevät rekisteröinnin (kuten uuden työn): Käyttöliittymä palaa sitten kirjautumissivulle. Kun asetuksena on *Kyllä*, työntekijät pysyvät kirjautuneena tuotannon käyttöliittymään. Työntekijä voi kuitenkin kirjautua ulos manuaalisesti, jolloin toinen työntekijä voi kirjautua sisään, jolloin tuotannon käyttöliittymää käytetään edelleen samalla järjestelmäkäyttäjätilillä. Lisätietoja tämän tyyppisistä tileistä on kohdassa [Määritetyt käyttäjät](config-job-card-device.md#assigned-users).
- **Käytä todellista kirjaamisaikaa** – Jos asetuksen on *Kyllä*, kukin uusi kirjaus vastaa tarkkaa aikaa, jolloin työntekijä on lähettänyt rekisteröitymisen. Jos asetuksena on *Ei*, käytössä on kirjautumisaika. Yleensä tämä asetus on *Kyllä*, jos **Lukitse työntekijä**- ja/tai **Yksittäinen työntekijä** -asetuksena on *Kyllä* tilanteissa, joissa työntekijät pysyvät usein kirjautuneina pitkiä aikoja.
- **Yksittäinen työntekijä** – Asetuksena voi olla *Kyllä*, jos vain yksi työntekijä käyttää kutakin tuotannon käyttöliittymää, jossa tämä määritys on aktiivinen. Kun asetuksena on *Kyllä*, **Lukitse työntekijä** -asetuksen on automaattisesti *Kyllä*. Lisäksi tämä asetus poistaa edellytyksen (ja mahdollisuuden), jonka mukaan työntekijä kirjautuu sisään käyttämällä nimilapun tunnusta (tai vastaavaa tunnusta). Työntekijä kirjautuu sen sijaan Microsoft Dynamics 365 Supply Chain Managementiin käyttämällä järjestelmän käyttäjätiliä, joka on linkitetty *aikarekisteröityyn työntekijään* (*työntekijät*-taulukosta). Samanaikaisesti kirjaudutaan myös tuotannon käyttöliittymään.
- **Salli kosketusnäytön lukitseminen** – Jos asetuksena on *Kyllä*, työntekijät voivat lukita työkorttilaitteen tuotannon käyttöliittymän, jotta he voivat puhdistaa sen. Jos asetuksena on *Kyllä*, kirjautumissivulla on **Lukitse näyttö puhdistusta varten** -painike. Kun työntekijä valitsee tämän painikkeen, kosketusnäyttö lukittuu tilapäisesti tahattoman syötön estämiseksi. Näkyvissä on myös ajastin. Työntekijä voi sitten puhdistaa laitteen ja näytön turvallisesti. Kun ajastimen aika päättyy, kosketusnäyttö avautuu automaattisesti.
- **Näytön lukituksen kesto** – Jos **Salli kosketusnäytön lukitus** -asetuksena on *Kyllä*, tällä asetuksella voi määrittää, kuinka monta sekuntia kosketusnäyttö on lukittu puhdistusta varten. Keston on oltava 5 – 120 sekunnin välillä.
- **Luo rekisterikilpi** – Jos asetuksena on *Kyllä*, voit luoda uuden rekisterikilven aina, kun työntekijä ilmoittaa tuotannon käyttöliittymässä olevansa valmis. Rekisterikilpinumero muodostetaan **Varastonhallinnan parametrit** -sivulla määritetystä numerosarjasta. Kun asetus on *Ei*, työntekijöiden on määritettävä aiemmin määritetty rekisterikilpi, kun he ilmoittavat työn valmistumisesta.
- **Tulosta etiketti** – Jos asetuksena on *Kyllä*, voit haluat tulostaa rekisterikilven otsikon, kun työntekijä ilmoittaa valmistumisesta tuotannon käyttöliittymällä. Etiketin konfiguraatio määritetään tiedoston reitityksessä, kuten on kuvattu kohteessa [Rekisterimerkintöjen asiakirjan reititysasettelu](../warehousing/document-routing-layout-for-license-plates.md).

### <a name="the-tab-selection-fasttab"></a>Välilehden valinta -pikavälilehti

**Välilehden valinta** -pikavälilehden asetuksilla valitaan, mitkä välilehdet näytetään tuotannon käyttöliittymässä, kun nykyinen määritys on aktiivinen. Voit suunnitella niin monta välilehteä kuin on tarpeen, ja sen jälkeen voit lisätä ja järjestää niitä tarpeen mukaan käyttämällä pikavälilehtityökalurivin painikkeita. Lisätietoja välilehtien suunnittelemisesta ja näiden asetusten käyttämisestä on kohdassa [Tuotannon käyttöliittymän suunnitteleminen](production-floor-execution-tabs.md).

### <a name="the-report-progress-fasttab"></a>Raportointi on meneillään -pikavälilehti

**Raportointi on meneillään** -pikavälilehdessä on seuraavat tiedot:

- **Ota materiaalin oikaisu käyttöön** – Sisällytä **Materiaalin oikaiseminen** **Raportointi on meneillään** -valintaikkunaan valitsemalla *Kyllä*. Työntekijät voivat säätää kunkin tuotantotyön materiaalikulutusta valitsemalla tämän painikkeen.
- **Oletusarvoinen jäljellä oleva määrä** – Määritä tämän asetuksen arvoksi *Kyllä*, jos haluat täyttää tuotantotyön odotetun jäljellä olevan määrän ennakkoon **Raportointi on meneillään** -valintaikkunassa.

## <a name="clean-up-job-configurations"></a>Työmääritysten poistaminen

Tuotannon työnjohtaja valitsee tuotannon käyttöliittymän määrityksen yhteydessä määrityksen ja työsuodattimen. Nämä valinnat tallennetaan viitetaulukkoon Supply Chain Managementissa, ja selain etsii oikean rivin kyseisestä taulukosta käyttämällä paikalliseen evästeeseen tallennettua tunnusta. Tähän taulukkoon kirjataan myös päivämäärä ja kellonaika, jolloin työntekijä on viimeksi kirjautunut kuhunkin laitteeseen.

Erätyö poistaa säännöllisesti viitetaulukoista niiden laitteiden merkinnät, joihin ei ole kirjattu mitään aktiviteetteja kuluneen 60 päivän aikana. Merkintöjä voi poistaa myös manuaalisesti koska tahansa seuraavasti:

1. Valitse **Tuotannonhallinta \> Asetukset \> Tuotannonohjaus \> Määritä tuotantoliittymä**.
1. Valitse toimintoruudussa **Tyhjennä asiakasohjelmamäärityksiä**.
1. Määritä **Tyhjennä asiakasohjelmamäärityksiä** -valintaikkunan **Päivien määrä** -kentässä, kuinka monta päivää (ennen kuluvaa päivää) ilman toimintaa otetaan huomioon. Kaikkien niiden laitteiden määritykset ja kirjautumistietueet poistetaan, jotka eivät ole olleet aktiivisia kyseisenä aikana.
1. Tyhjennä soveltuvat määritykset **Päivien määrä** -asetuksen perusteella valitsemalla **OK**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
