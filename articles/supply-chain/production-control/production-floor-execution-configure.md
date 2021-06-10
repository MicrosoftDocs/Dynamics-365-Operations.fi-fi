---
title: Tuotannon käyttöliittymän määrittäminen
description: Tässä ohjeaiheessa käsitellään tuotannon käyttöliittymämääritysten luontia. Kun tuotannon käyttöliittymä avataan, se lataa automaattisesti selain- ja laitekohtaisen valitun määrityksen ja työsuodattimen. Määrityksessä määritetään käytännöt, joita on käytettävä tietyssä käyttötilanteessa.
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
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 84d845055e175e6f4b8078fabeb3307ee96826f2
ms.sourcegitcommit: 588f8343aaa654309d2ff735fd437dba6acd9d46
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/28/2021
ms.locfileid: "6115020"
---
# <a name="configure-the-production-floor-execution-interface"></a>Tuotannon käyttöliittymän määrittäminen

[!include [banner](../includes/banner.md)]

Tuotannon työntekijät rekisteröivät tuotannon käyttöliittymällä päivittäisen työnsä, kuten töiden aloittamisen, töitä koskevan palautteen antamisen, epäsuorien tehtävien rekisteröimisen ja poissaolon raportoinnin. Nämä rekisteröinnit ovat perusta, jolla seurataan tuotantotilausten edistymistä ja kustannuksia sekä lasketaan työntekijöiden palkka.

Kun tuotannon käyttöliittymä avataan, se lataa automaattisesti selain- ja laitekohtaisen valitun määrityksen ja työsuodattimen. Määrityksessä määritetään käytännöt, joita on käytettävä tietyssä käyttötilanteessa. Esimerkkejä käytöstä:

- Laite on yrityksen aulassa, ja työntekijät kuittaavat itsensä sisään, kun he tulevat töihin, ja ulos, kun he lähtevät kotiin.
- Laite on tuotantotiloissa, ja koneen käyttäjät rekisteröivät milloin he aloittavat ja lopettavat työt. Tämän he rekisteröivät tauot ja epäsuorat tehtävät.

Tässä ohjeaiheessa kuvataan työkorttilaitteiden konfiguroinnissa käytettävissä olevat eri asetukset.

## <a name="turn-on-the-production-floor-execution-interface-and-its-related-optional-features"></a>Tuotannon käyttöliittymän ja siihen liittyvien valinnaisten ominaisuuksien ottaminen käyttöön

Tuotannon käyttöliittymä sekä monet tässä aiheessa käsiteltävät valinnaiset asetukset on otettava järjestelmässä käyttöön, ennen kuin niitä voi käyttää. Ota tarvittaessa näitä ominaisuuksia käyttöön [Ominaisuuksien hallinta](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) -sivulla seuraavissa alaosissa kuvatulla tavalla.

### <a name="the-production-floor-execution-interface"></a>Tuotannon käyttöliittymä

Tätä ominaisuutta käsitellään ensisijaisesti tässä aiheessa. Se lisää tuotannon käyttöliittymän järjestelmään. Ota se käyttöön ottamalla seuraava ominaisuus käyttöön [ominaisuuksien hallinnassa](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md):

- Tuotannon toteutus

### <a name="generate-license-plates"></a>Rekisterikilpien muodostaminen

Näillä ominaisuuksilla rekisterikilpitoiminnot saadaan käyttöön tuotannon käyttöliittymässä. Jos haluat käyttää niitä, ota seuraavat ominaisuudet käyttöön [ominaisuuksien hallinnassa](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) (seuraavassa järjestyksessä):

1. Rekisterikilpi valmiiksi raportointia varten on lisätty työkorttilaitteeseen
1. Ota käyttöön rekisterikilven numeron automaattinen luonti, kun työkorttilaitteessa raportoidaan valmiiksi

### <a name="print-labels"></a>Tulosta etiketit

Näillä ominaisuuksilla etikettitulostus saadaan käyttöön tuotannon käyttöliittymässä. Jos haluat käyttää niitä, ota seuraavat ominaisuudet käyttöön [ominaisuuksien hallinnassa](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) (seuraavassa järjestyksessä):

1. Rekisterikilpi valmiiksi raportointia varten on lisätty työkorttilaitteeseen
1. Tulosta etiketti työkorttilaitteesta

### <a name="allow-locking-the-touch-screen"></a>Kosketusnäytön lukitsemisen salliminen

Tämä ominaisuus lisää tuotannon käyttöliittymään painikkeen, jolla työntekijät voivat puhdistaa kosketusnäytön. Jos haluat käyttää sitä, ota seuraava ominaisuus käyttöön [ominaisuuksien hallinnassa](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md):

- Ominaisuus, jolla voi lukita työkorttilaitteen ja työkorttipäätteen desinfiointia varten

### <a name="asset-management-functionality-for-the-production-floor-execution-interface"></a>Tuotannonohjausliittymän käyttöomaisuuden hallintatoiminto

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]

Tämä toiminto lisää resurssien hallinnan välilehden tuotannon käyttöliittymään. Työtekijät voivat valita tässä välilehdessä siihen koneresurssiin liittyvän resurssin, joka on työluettelon valitussa suodattimessa. Työtekijä voi tarkastella valitun koneresurssin tilaa ja kuntoa enintään neljän valitun laskurin arvojen avulla. Jos haluat käyttää tätä toimintoa, ota seuraava toiminto käyttöön [ominaisuuksien hallinnassa](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md):

- Tuotannonohjausliittymän käyttöomaisuuden hallintatoiminto

### <a name="enable-job-search"></a>Työhaun ottaminen käyttöön

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]

Tämän ominaisuuden avulla voit lisätä hakukentän työluetteloon. Työntekijät voivat etsiä tietyn työn syöttämällä työtunnuksen tai etsimällä tietyn tilauksen kaikki työt antamalla tilaustunnuksen. Työntekijät voivat syöttää tunnuksen näppäimistön avulla tai skannaamalla viivakoodia. Jos haluat käyttää sitä, ota seuraava ominaisuus käyttöön [ominaisuuksien hallinnassa](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md):

- Töiden haku tuotannon työnohjausliittymälle

## <a name="work-with-production-floor-execution-configurations"></a>Tuotannon käyttöliittymämääritysten käyttäminen

Voit luoda ja ylläpitää laitemäärityksiä valitsemalla **Tuotannonhallinta \> Määritys \> Tuotannonohjaus \> Määritä tuotantoliittymä**. **Määritä tuotantoliittymä** -sivulla on luettelo aiemmin luoduista määrityksistä. Tällä sivulla voi tehdä seuraavia toimenpiteitä:

- Valitse vasemmassa sarakkeessa oleva tuotantomääritykset, jos haluat tarkastella ja muokata niitä.
- Valitse toimintoruudusta **Uusi**, kun haluat lisätä luetteloon uuden laitekonfiguraation. Anna sitten **Määritys**-kenttään nimi, jolla uusi määritys on helppo tunnistaa. Annetun nimen oltava yksilöivä kaikkien laitemääritysten joukossa, eikä sitä voi muokata myöhemmin.

Määritä seuraavaksi valitun laitemäärityksen asetukset. Seuraavat kentät ovat käytettävissä:

- **Vain sisään- ja uloskirjaus** – Määritä tämän asetuksen arvoksi *Kyllä*, jos haluat luoda yksinkertaistetun liittymän, jossa on vain sisään- ja uloskirjaustoiminnot. Tällöin suurin osa sivun muista asetuksista poistuu käytöstä. Ennen tämän asetuksen käyttöönottoa on poistettava kaikki rivit **Välilehtivalinta**-pikavälilehdestä.
- **Ota haku käyttöön** - Määritä tämän asetuksen arvoksi *Kyllä*, jos haluat sisällyttää työluetteloon hakukentän. Työntekijät voivat etsiä tietyn työn syöttämällä työtunnuksen tai etsimällä tietyn tilauksen kaikki työt antamalla tilaustunnuksen. Työntekijät voivat syöttää tunnuksen näppäimistön avulla tai skannaamalla viivakoodia.
- **Ilmoita määrä uloskuittauksessa** – Määritä asetukseksi *Kyllä*, jos haluat, että työntekijöitä pyydetään antamaan palautetta meneillään olevista töistä, kun he kuittaavat itsensä ulos. Jos asetuksena on *Ei*, työntekijät eivät saa tätä kehotetta.
- **Lukitse työntekijä** – Jos asetuksena on *Ei*, työntekijät kirjautuvat ulos heti, kun he tekevät rekisteröinnin (kuten uuden työn): Laite palaa sitten kirjautumissivulle. Kun asetuksena on *Kyllä*, työntekijät pysyvät kirjautuneena työkorttilaitteeseen. Työntekijä voi kuitenkin kirjautua ulos manuaalisesti, jolloin toinen työntekijä voi kirjautua sisään, jolloin työkorttilaitetta käytetään edelleen samalla järjestelmäkäyttäjätilillä. Lisätietoja tämän tyyppisistä tileistä on kohdassa [Määritetyt käyttäjät](config-job-card-device.md#assigned-users).
- **Käytä todellista kirjaamisaikaa** – Jos asetuksen on *Kyllä*, kukin uusi kirjaus vastaa tarkkaa aikaa, jolloin työntekijä on lähettänyt rekisteröitymisen. Jos asetuksena on *Ei*, käytössä on kirjautumisaika. Yleensä tämä asetus on *Kyllä*, jos **Lukitse työntekijä**- ja/tai **Yksittäinen työntekijä** -asetuksena on *Kyllä* tilanteissa, joissa työntekijät pysyvät usein kirjautuneina pitkiä aikoja.
- **Yksittäinen työntekijä** – Asetuksena voi olla *Kyllä*, jos vain yksi työntekijä käyttää kutakin työkorttilaitetta, jossa tämä määritys on aktiivinen. Kun asetuksena on *Kyllä*, **Lukitse työntekijä** -asetuksen on automaattisesti *Kyllä*. Lisäksi tämä asetus poistaa edellytyksen (ja mahdollisuuden), jonka mukaan työntekijä kirjautuu sisään käyttämällä nimilapun tunnusta (tai vastaavaa tunnusta). Työntekijä kirjautuu sen sijaan Microsoft Dynamics 365 Supply Chain Managementiin käyttämällä järjestelmän käyttäjätiliä, joka on linkitetty *aikarekisteröityyn työntekijään* (*työntekijät*-taulukosta). Samanaikaisesti kirjaudutaan myös työkorttilaitteeseen.
- **Salli kosketusnäytön lukitseminen** – Jos asetuksena on *Kyllä*, työntekijät voivat lukita työkorttilaitteen kosketusnäytön, jotta he voivat puhdistaa sen. Jos asetuksena on *Kyllä*, laitteen kirjautumissivulla on **Lukitse näyttö puhdistusta varten** -painike. Kun työntekijä valitsee tämän painikkeen, kosketusnäyttö lukittuu tilapäisesti tahattoman syötön estämiseksi. Näkyvissä on myös ajastin. Työntekijä voi sitten puhdistaa laitteen ja näytön turvallisesti. Kun ajastimen aika päättyy, kosketusnäyttö avautuu automaattisesti.
- **Näytön lukituksen kesto** – Jos **Salli kosketusnäytön lukitus** -asetuksena on *Kyllä*, tällä asetuksella voi määrittää, kuinka monta sekuntia kosketusnäyttö on lukittu puhdistusta varten. Keston on oltava 5 – 120 sekunnin välillä.
- **Luo rekisterikilpi** – Jos asetuksena on *Kyllä*, voit luoda uuden rekisterikilven aina, kun työntekijä ilmoittaa työkorttilaiteella olevansa valmis. Rekisterikilpinumero muodostetaan **Varastonhallinnan parametrit** -sivulla määritetystä numerosarjasta. Kun asetus on *Ei*, työntekijöiden on määritettävä aiemmin määritetty rekisterikilpi, kun he ilmoittavat työn valmistumisesta.
- **Tulosta etiketti** – Jos asetuksena on *Kyllä*, voit haluat tulostaa rekisterikilven otsikon, kun työntekijä ilmoittaa valmistumisesta työkorttilaitteella. Etiketin konfiguraatio määritetään tiedoston reitityksessä, kuten on kuvattu kohteessa [Rekisterimerkintöjen asiakirjan reititysasettelu](../warehousing/document-routing-layout-for-license-plates.md).
- **Välilehtivalinta** – Tämän osan asetuksilla valitaan, mitkä välilehdet näytetään tuotannon käyttöliittymässä, kun nykyinen määritys on aktiivinen. Voit määrittää tarvittavan määrän välilehtiä sekä lisätä ja järjestää ne sitten täällä tarpeen mukaan. Lisätietoja välilehtien suunnittelemisesta ja näiden asetusten käyttämisestä on kohdassa [Tuotannon käyttöliittymän suunnitteleminen](production-floor-execution-tabs.md).

## <a name="clean-up-job-configurations"></a>Työmääritysten poistaminen

Tuotannon työnjohtaja valitsee tuotannon käyttöliittymän määrityksen yhteydessä määrityksen ja työsuodattimen. Nämä valinnat tallennetaan viitetaulukkoon Supply Chain Managementissa, ja selain etsii oikean rivin kyseisestä taulukosta käyttämällä paikalliseen evästeeseen tallennettua tunnusta. Tähän taulukkoon kirjataan myös päivämäärä ja kellonaika, jolloin työntekijä on viimeksi kirjautunut kuhunkin laitteeseen.

Erätyö poistaa säännöllisesti viitetaulukoista niiden laitteiden merkinnät, joihin ei ole kirjattu mitään aktiviteetteja kuluneen 60 päivän aikana. Merkintöjä voi poistaa myös manuaalisesti koska tahansa seuraavasti:

1. Valitse **Tuotannonhallinta \> Asetukset \> Tuotannonohjaus \> Määritä tuotantoliittymä**.
1. Valitse toimintoruudussa **Tyhjennä asiakasohjelmamäärityksiä**.
1. Määritä **Tyhjennä asiakasohjelmamäärityksiä** -valintaikkunan **Päivien määrä** -kentässä, kuinka monta päivää (ennen kuluvaa päivää) ilman toimintaa otetaan huomioon. Kaikkien niiden laitteiden määritykset ja kirjautumistietueet poistetaan, jotka eivät ole olleet aktiivisia kyseisenä aikana.
1. Tyhjennä soveltuvat määritykset **Päivien määrä** -asetuksen perusteella valitsemalla **OK**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
