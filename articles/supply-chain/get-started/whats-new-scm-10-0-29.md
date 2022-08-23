---
title: Dynamics 365 Supply Chain Management 10.0.29:n esiversio (lokakuu 2022)
description: Tässä artikkelissa käsitellään Microsoft Dynamics 365 Supply Chain Managementin 10.0.29 uusia tai muuttuneita toimintoja.
author: kamaybac
ms.date: 08/12/2022
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2022-08-01
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: 7f5691c5784b7b381ff805b0431d8adb1a25f1cb
ms.sourcegitcommit: 8d072505f66f507aafbaae65bedf3b530eb6cb7b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9266395"
---
# <a name="preview-of-dynamics-365-supply-chain-management-10029-october-2022"></a>Dynamics 365 Supply Chain Management 10.0.29:n esiversio (lokakuu 2022)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Tässä artikkelissa käsitellään Microsoft Dynamics 365 Supply Chain Managementin esikatseluversion 10.0.29 uusia tai muuttuneita ominaisuuksia. Tämän version koontinumero on 10.0.1326. Se on käytettävissä seuraavan aikataulun mukaisesti:

- **Julkaisun esiversio:** Elokuu 2022
- **Version yleinen saatavuus (oma päivitys):** syyskuu 2022
- **Version yleinen saatavuus (automaattinen päivitys):** lokakuu 2022

## <a name="features-included-in-this-release"></a>Tähän julkaisuun sisältyvät toiminnot

Seuraavassa taulukossa on tämän julkaisun sisältämät toiminnot. Tämän artikkelin päivitys saattaa sisältää ominaisuuksia, jotka on lisätty koontiversioon tämän artikkelin alkuperäisen julkaisun jälkeen.

| Ominaisuusalue | Ominaisuus | Lisätietoja | Käyttöönottaja:   |
|---|---|---|---|
| Varasto ja logistiikka | [WMS-nimikkeiden allokointi ja varaaminen varaston näkyvyydessä](/dynamics365-release-plan/2022wave2/finance-operations/dynamics365-supply-chain-management/allocate-reserve-whs-items-inventory-visibility) | Tulossa pian | Oletusarvoisesti käytössä |
| Varasto ja logistiikka | [Käytettävissä olevan varaston virtaviivaistettujen luetteloiden esilataaminen](/dynamics365-release-plan/2022wave2/finance-operations/dynamics365-supply-chain-management/query-inventory-visibility-summary-entity) | Tulossa pian | Oletusarvoisesti käytössä |
| Tilauksesta valmistukseen -tarjonnan automatisointi | [Tilauksesta valmistukseen -tarjonnan automatisointi](/dynamics365-release-plan/2022wave2/finance-operations/dynamics365-supply-chain-management/make-to-order-supply-automation) | [Tilauksesta valmistukseen -tarjonnan automatisointi](../master-planning/make-to-order-supply-automation.md) | Toimintojen hallinta:<br>*Tilauksesta valmistukseen -tarjonnan automatisointi* |
| Suunnittelu | [Yksityiskohtaisten DDMRP-tietojen tarkasteleminen ja käyttö](/dynamics365-release-plan/2022wave2/finance-operations/dynamics365-supply-chain-management/view-apply-detailed-insights-ddmrp) | [Kysyntäperustainen materiaalitarvesuunnittelun yleiskatsaus](../master-planning/planning-optimization/ddmrp-overview.md) | Toimintojen hallinta:<br>*(Esiversio) DDMRP – suunnittelun optimointi* |
| Tuotannonhallinta | [Tee valmiista tavaroista fyysisesti saatavilla olevia ennen kirjauskansioihin kirjaamista](/dynamics365-release-plan/2022wave2/finance-operations/dynamics365-supply-chain-management/make-finished-goods-physically-before-posting) | [Tee valmiista tavaroista fyysisesti saatavilla olevia ennen kirjauskansioihin kirjaamista](../production-control/deferred-posting.md) | Toimintojen hallinta:<br>*(Esiversio) Tee valmiista tavaroista fyysisesti saatavilla olevia ennen kirjauskansioihin kirjaamista* |
| Varastonhallinta   | [Asiaankuuluvien tietojen haku Warehouse Mobile App -sovelluksesta](/dynamics365-release-plan/2022wave2/finance-operations/dynamics365-supply-chain-management/look-up-relevant-data-within-warehouse-mobile-app) | [Tietojen kyseleminen Warehouse Management ‑mobiilisovelluksen kiertoteillä](../warehousing/warehouse-app-data-inquiry.md) | Toimintojen hallinta:<br>*Warehouse Management -sovelluksen tietokyselyn kulku* |

## <a name="feature-enhancements-included-in-this-release"></a>Tähän julkaisuun sisältyvät toiminnon parannukset

Seuraavassa taulukossa on tämän julkaisun sisältämät ominaisuuksien parannukset. Jokainen näistä parannuksista parantaa aiemmin luotua toimintoa lisäysten avulla. Koska ne ovat vain parannuksia, niitä ei ole lueteltu [vapautussuunnitelmassa](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planned-features). Jos kuitenkin haluat varmistaa, että nämä parannukset eivät ole ristiriidassa aiemmin luotujen mukautuksiesi tai asetuksesi kanssa, kaikki muutokset ovat oletusarvon mukaan pois käytöstä (ellei toisin ilmoiteta).

Jos haluat ottaa jonkin näistä ominaisuuksista käyttöön tai poistaa ne käytöstä, sinun on tehtävä se [ominaisuuksienhallinnassa](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

| Moduuli | Ominaisuuden nimi ominaisuuksienhallinnassa | Lisätietoja |
|---|---|---|
| Kustannushintojen hallinta | Rinnakkaistuotteen optimointi odottavan hinnan laskennassa | Tämä ominaisuus korjaa ristiriidan, joka voi joskus ilmetä, kun rinnakkaistuotteiden hintoja lasketaan käyttämällä useita säikeitä. Se saa järjestelmän varmistamaan, että jokaisen rinnakkaistuotteen hinta lasketaan vain kerran. Tämän laskutoimen tulosta käytetään kaikkien muiden laskutoimien syötteenä. Jos odottava hinta on jo olemassa, sitä käytetään. |
| Pääsuunnittelu | Ryhmittele tapahtumat suunnittelun optimoinnissa | Tämä ominaisuus voi auttaa vähentämään yhden myyntitilausrivin toimitusta varten luotujen suunniteltujen tilausten määrää, kun käytät suunnittelun optimointia. Kun tämä ominaisuus on käytössä, suunnittelun optimointi ryhmittelee tilausrivin kaikki varastotapahtumat yhdeksi vaatimukseksi koko määrälle. (Tämä toimintatapa vastaa sisäisen suunnittelumoduulin toimintaa). Tarjonta ja kysyntä ryhmitellään erikseen. Näin ollen tämä ominaisuus auttaa vähentämään tapahtumien määrää, kun sinulla on jaettuja tapahtumia ja kun käytät dimensioita (kuten eränumeroita tai sarjanumeroita), jotka eivät ole kattavuusdimensioita. |
| Hankinta | Aseta toimittaja pitoon ostotilausten osalta | Tämän ominaisuuden avulla voit asettaa toimittajan pitoon ostotilausten osalta. Se lisää uuden *Ostotilaus*-pitotyypin, joka merkitsee toimittajan olevan pidossa ostotilausten osalta. Et voi luoda uusia ostotilauksia toimittajille, jotka ovat pidossa ostotilausten osalta, mutta voit edelleen jatkaa näiden toimittajien avoimia laskuja tai maksuja. |
| Myynti ja markkinointi | Laske rivin nettosumma tuonnin yhteydessä | Tämän ominaisuuden avulla voit hallita, tulisiko järjestelmän laskea rivien kokonaissummat uudelleen, kun tuot tietoja *Myyntitilausrivit*-, *Myyntitarjousrivit*- tai *Palautustilausrivit*-entiteetin kautta käyttämällä ODataa tai kaksoiskirjoitusta. Se on voimassa vain, kun sinulla on käytössä myös kauppasopimusten arviointikäytäntöjä, jotka rajoittavat myyntitilausrivien, myyntitarjousrivien ja/tai palautustilausrivien **Nettosumma**-kentän muutoksia. Se lisää **Laske rivin nettosumma** -asetuksen **Myyntireskontra > Asetukset > Myyntireskontran parametrit** -sivulle. Kun määrität tämän asetuksen arvoksi *Kyllä*, järjestelmä laskee rivien summat aina uudelleen tarvittaessa (ja jättää siten kaikki kauppasopimusten arviointikäytännöt huomiotta rivin nettosumman osalta). Kun asetuksen arvoksi on määritetty *Ei*, järjestelmä ei laske rivin nettosummaa koskaan automaattisesti, vaikka rivin hintaan, määrään ja/tai alennukseen tehdyt muutokset osoittaisivat, että nettosummaa pitäisi laskea uudelleen. Tämä ominaisuus on oletusarvoisesti käytössä ja **Laske rivin nettosumma** -asetus on alustavasti *Kyllä*. *Ei*-asetus vastaa järjestelmän toimintatapaa ennen versiota 10.0.23, ja se on tarkoitettu ensisijaisesti vanhojen integrointiskenaarioiden tueksi.<br><br>Lisätietoja on kohdassa [Rivin nettosummien laskeminen uudelleen myyntitilausten, tarjousten ja palautusten tuomisen aikana](../sales-marketing/calc-line-net-amounts-import.md). |
| Myynti ja markkinointi | Laske kokonaismyynti käyttämällä useita säikeitä | Tämä ominaisuus auttaa parantamaan suorituskykyä sallimalla järjestelmän käyttää rinnakkaiskäsittelyä, kun se laskee kokonaismyynnit erässä. Ominaisuus lisää **Laske kokonaismyynti** -valintaikkunaan uuden **Säkeiden määrä** -kentän. Jos päätät suorittaa laskennan erässä, voit käyttää tätä kenttää määrittääksesi säikeiden enimmäismäärän. Jos määrität arvoksi *0* (nolla) tai *1*, järjestelmä käyttää yhtä säiettä. Arvot, jotka ovat yli 1, ottavat monisäikeisyyden käyttöön. |
| Myynti ja markkinointi | Päivitä manuaalisesti syötetyt konsernin sisäiset hinnat ja alennukset | Tämä ominaisuus lisää konsernin sisäisten tilausten manuaalisen muutoskäytäntöjen tuen. Se sisältää tuen manuaalisten muutoskäytäntöjen siirtämiseen konsernin sisäisten myynti- ja ostotilausten välillä. Aiemmin manuaalisia muutoskäytäntöjä tuettiin vain konsernin sisäisille tilauksille. Kun tämä ominaisuus on käytössä, järjestelmä antaa sinulle mahdollisuuden päivittää hinnat ja alennukset, kun tallennat muutoksia konsernin sisäiseen tilaukseen. Tämä ominaisuus sallii sinun valita, käytetäänkö uusia hintoja ja alennuksia konsernin sisäisessä tilauksessa vai jätetäänkö tilaus ennalleen. |

## <a name="new-and-updated-documentation-resources"></a>Uudet ja päivitetyt asiakirjaresurssit

Seuraavat ohjeartikkelit on lisätty äskettäin tai niitä on päivitetty merkittävästi. Nämä artikkelit eivät välttämättä liity tällä julkaisulla lisättyihin, edellisissä osissa lueteltuihin uusiin ominaisuuksiin. Niiden avulla saatat kuitenkin saada enemmän irti olemassa olevista ominaisuuksista.

| Ominaisuusalue | Uudet tai päivitetyt artikkelit |
|---|---|
| Pääsuunnittelu, saatavuus (CTP) | [Myyntitilauksen toimituspäivien laskeminen saatavuudella](../master-planning/planning-optimization/calculate-delivery-dates-using-ctp.md) |
| Pääsuunnittelu, DDMRP | [Kysyntäperustainen materiaalitarvesuunnittelun yleiskatsaus](../master-planning/planning-optimization/ddmrp-overview.md)<br>[DDMRP-ominaisuuden ottaminen käyttöön järjestelmässä](../master-planning/planning-optimization/ddmrp-enable.md)<br>[Varaston asemointi](../master-planning/planning-optimization/ddmrp-inventory-positioning.md)<br>[Puskuriprofiili ja -tasot](../master-planning/planning-optimization/ddmrp-buffer-profile-and-levels.md)<br>[Kysyntäperustainen suunnittelu](../master-planning/planning-optimization/ddmrp-planning.md)<br>[Visualisoinnin ja yhteistyön toteutus](../master-planning/planning-optimization/ddmrp-visual-and-collaborative-execution.md) |
| Varastonhallinta   | [Lähetettävien konttien pakkaaminen](../warehousing/packing-containers.md)<br>[Lähtevien konttien pakkaaminen ja toimitusten käsittely](../warehousing/packing-work.md) |

## <a name="feature-state-changes-in-this-release"></a>Tämän julkaisun toiminnon tilan muutokset

Seuraavassa taulukossa luetellaan ominaisuudet, jotka tulivat pakollisiksi tai oletusarvoisesti käyttöön versiossa 10.0.29. Kaikki nämä ominaisuudet otetaan automaattisesti käyttöön järjestelmässäsi heti, kun päivität versioon 10.0.29. Pakollisia ominaisuuksia ei voi poistaa käytöstä, mutta oletusarvoisesti käytössä olevia ominaisuuksia voi poistaa käytöstä [Ominaisuuksien hallinta](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) -työtilasta.

Taulukko sisältää myös ominaisuudet, jotka olivat aiemmin julkisen esiversion vaiheessa, mutta jotka ovat yleisesti saatavilla versiossa 10.0.29. Tämä muutos tarkoittaa sitä, että niitä suositellaan käytettäviksi tuotantoympäristöissä. Nämä ominaisuudet eivät ole oletusarvoisesti käytössä, ellei toisin ole mainittu. Jos haluat siis käyttää niitä, sinun täytyy ottaa ne käyttöön [Ominaisuuksien hallinta](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) -työtilasta.

| Moduuli | Toiminnon nimi | Uuden ominaisuuden tila |
| --- | --- | --- |
| Resurssien hallinta | [Käytä sääntöjä työtilausten ryhmittelyyn ylläpitosuunnitelman ollessa käynnissä](../asset-management/preventive-and-reactive-maintenance/creating-work-orders.md) | Pakollinen |
| Resurssien hallinta | [Tuotannonohjausliittymän käyttöomaisuuden hallintatoiminto](../production-control/production-floor-execution-configure.md) | Pakollinen |
| Resurssien hallinta | [Vastaperusteiset ylläpitoparannukset](../asset-management/preventive-and-reactive-maintenance/maintenance-plans.md) | Käytössä oletusarvoisesti |
| Resurssien hallinta | [Työtilauksen laskutus](../asset-management/integration-to-project-management-and-accounting/customer-billing.md) | Pakollinen |
| Kustannushintojen hallinta | [Muuta peruutuksen otsikkoa sulkemisen ja palautusoikaisun yhteydessä](/dynamics365-release-plan/2020wave1/dynamics365-supply-chain-management/change-terminology-inventory-closing-cancellation-inventory-closing-reverse) | Pakollinen |
| Kustannushintojen hallinta | Tyhjennä tuoterakenteen laskennan erittelyn liittyvät kustannuslaskentaversiot | Pakollinen |
| Kustannushintojen hallinta | [Nimikkeiden hintavertailun tallennus](../cost-management/compare-item-price.md) | Pakollinen |
| Kustannushintojen hallinta | [Kustannuslaskentataso](../cost-management/cost-calculation-level.md) | Käytössä oletusarvoisesti |
| Kustannushintojen hallinta | Ota käyttöön käyttäjän määrittämät eränumeroasetukset varaston käänteistä sulkutoimenpidettä varten | Käytössä oletusarvoisesti |
| Kustannushintojen hallinta | [Varaston sulkemisen edistymistiedot](whats-new-scm-10-0-21.md) | Käytössä oletusarvoisesti |
| Kustannushintojen hallinta | [Varastoarvoraporttien säiliö](../cost-management/inventory-value-report-storage.md) | Pakollinen |
| Kustannushintojen hallinta | Varaston arvon raportin tietojen puhdistus | Pakollinen |
| Kustannushintojen hallinta | Liukuva keskiarvo varalla oleva kustannusjärjestys | Pakollinen |
| Kustannushintojen hallinta | Näytä varaston sulkemisen loki ruudukossa | Pakollinen |
| Kustannushintojen hallinta | Näytä yhteenvetomuodossa nimikkeet, joilla on tapahtumia, joita ei ole selvitetty kokonaan | Pakollinen |
| Varastonhallinta | Salli tyhjät erämääritteiden arvot | Pakollinen |
| Varastonhallinta | Varaston siirtotilausrivien automaattinen rivinumeroiden lisäys | Pakollinen |
| Varastonhallinta | Luo siirtotilaus myyntiriviltä | Pakollinen |
| Varastonhallinta | Poista varastokirjauskansion rivin kenttä käytöstä työnkulussa | Pakollinen |
| Varastonhallinta | Ota käyttöön varaston laadunhallinnan parametrien varoitusominaisuus | Pakollinen |
| Varastonhallinta | (Kiina) Jätä pois fyysisten vastaanottojen ja varasto-ottojen kustannukset kuukausittaisesta keskiarvokustannuksesta | Käytössä oletusarvoisesti |
| Varastonhallinta | [Varaston kirjauskansion hyväksynnän työnkulku](../inventory/inventory-journal-workflow.md) | Pakollinen |
| Varastonhallinta | [Käytettävissä olevan varaston raporttitallennus](/dynamics365-release-plan/2020wave1/dynamics365-supply-chain-management/inventory-on-hand-report-storage) | Pakollinen |
| Varastonhallinta | [Inventoinnin- ja varastonhallinnan tallennetut näkymät](saved-views-scm.md) | Pakollinen |
| Varastonhallinta | Siirtotilauksen peruutus | Pakollinen |
| Varastonhallinta | Käytetään mittayksikköä ja yksikkömäärää varastokirjauskansioissa | Pakollinen |
| Varastonhallinta | Avaa varastokirjauskansion lukitus | Pakollinen |
| Valmistus | [Varastomateriaalien automaattinen keräily automaattisesti kirjattuja keräysluetteloita varten](whats-new-scm-10-0-23.md) | Yleisesti saatavilla |
| Valmistus | Ota käyttöön varastodimensiot tuotantoreititystoimintojen materiaaliluettelossa | Käytössä oletusarvoisesti |
| Valmistus | [Ota erä- ja sarjanumeroiden antaminen käyttöön, kun valmistuminen ilmoitetaan työkorttilaitteesta](../production-control/report-finished-job-device.md) | Käytössä oletusarvoisesti |
| Valmistus | Parantunut tuotannon todellisen painon määrän keräily | Käytössä oletusarvoisesti |
| Valmistus | [Töiden haku tuotannon työnohjausliittymälle](../production-control/production-floor-execution-configure.md) | Pakollinen |
| Valmistus | [Valmistuksenohjausjärjestelmän integrointi](../production-control/mes-integration.md) | Käytössä oletusarvoisesti |
| Valmistus | [Tuotannon käyttöliittymän Päivän tehtävät -näkymä](../production-control/production-floor-execution-configure.md) | Käytössä oletusarvoisesti |
| Valmistus | [Tuotantotilausten käytettävissä olevan materiaalin saatavuustarkistus](whats-new-scm-10-0-24.md) | Käytössä oletusarvoisesti |
| Valmistus | [Ohita oletustuotantovaraus](../production-control/override-default-reservation-principle.md) | Pakollinen |
| Valmistus | [Rekisteröi materiaalinkulutus tuotannon käyttöliittymässä (muu kuin WMS)](../production-control/production-floor-execution-configure.md) | Yleisesti saatavilla |
| Valmistus | [Todellisen painon nimikkeiden raportointi tuotannon käyttöliittymästä](../production-control/production-floor-execution-configure.md) | Yleisesti saatavilla |
| Valmistus | [Raportti tuotannon käyttöliittymän rinnakkais- ja sivutuotteista](../production-control/production-floor-execution-configure.md) | Käytössä oletusarvoisesti |
| Valmistus | [Suunnittelunimikkeitä koskeva raportti tuotannon käyttöliittymässä](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/enhanced-production-floor-execution-interface-process-manufacturing) | Käytössä oletusarvoisesti |
| Valmistus | [Tuotannonhallinnan tallennetut näkymät](saved-views-scm.md) | Pakollinen |
| Valmistus | [Näytä täydet sarja-, erä- ja rekisterinumerot tuotannon käyttöliittymässä](../production-control/production-floor-execution-configure.md) | Pakollinen |
| Valmistus | [Raaka-aineiden vanhenemisen tarkistaminen suunnitellun käyttöpäivän perusteella](whats-new-scm-10-0-23.md) | Käytössä oletusarvoisesti |
| Pääsuunnittelu | [Suunnittelun optimoinnin automaattinen vahvistus](../master-planning/planning-optimization/planned-order-firming.md) | Pakollinen |
| Pääsuunnittelu | [Suunniteltujen suur- ja pakkauserätilausten eräkelpoinen vahvistaminen ja konsolidointi](whats-new-scm-10-0-20.md) | Käytössä oletusarvoisesti |
| Pääsuunnittelu | [Sisällytä nimikkeet, joilla on käytettävissä olevaa varastoa, kun esikäsittelysuodattimet ovat käytössä](/dynamics365-release-plan/2020wave1/dynamics365-supply-chain-management/master-planning-include-items-on-hand-when-pre-processing-filters-are-enabled) | Käytössä oletusarvoisesti |
| Pääsuunnittelu | [Suunnittelun optimoinnin ääretön kapasiteetin ajoitus](../master-planning/planning-optimization/infinite-capacity-planning.md) | Käytössä oletusarvoisesti |
| Pääsuunnittelu | [Suunnittelun optimoinnin marginaalit](../master-planning/planning-optimization/safety-margins.md) | Pakollinen |
| Pääsuunnittelu | [Negatiiviset päivät suunnittelun optimoinnissa](../master-planning/planning-optimization/delay-tolerance.md) | Pakollinen |
| Pääsuunnittelu | [Oikaistun kysynnän ennusteen rinnakkainen valtuuttaminen](whats-new-scm-10-0-20.md) | Pakollinen |
| Pääsuunnittelu | [Suunnitellun tilauksen vahvistaminen suodatuksen kanssa](../master-planning/planning-optimization/planned-order-firming.md) | Pakollinen |
| Pääsuunnittelu | [Suunnittelun optimoinnin suunnitellut tuotantotilaukset](../master-planning/planning-optimization/production-planning.md) | Pakollinen |
| Pääsuunnittelu | [Ostokauppasopimukset suunnittelun optimointia varten](../master-planning/planning-optimization/purchase-trade-agreement.md) | Pakollinen |
| Pääsuunnittelu | Resurssien suunnittelu ja ylläpito | Pakollinen |
| Pääsuunnittelu | [Suunniteltujen tilausten tallennetut näkymät](saved-views-scm.md) | Pakollinen |
| Hankinta | Ostotilausten veloitusten lähde- ja kohdesummat | Pakollinen |
| Hankinta | Poista ostoehdotuksen jakelun palautuspainike käytöstä | Käytössä oletusarvoisesti |
| Hankinta | [Ota käyttöön hankintaan liittyvien työnkulkujen nollaus](whats-new-scm-10-0-20.md) | Käytössä oletusarvoisesti |
| Hankinta | [Rajoita ostotilausrivien määrää erätehtävää kohden](whats-new-scm-10-0-27.md) | Käytössä oletusarvoisesti |
| Hankinta | [Yhdistä sen toimittajan taloushallinnon dimensiot, jolla on aktiivisen dimension linkin taloushallinnon dimensio ostotilauksessa](whats-new-scm-10-0-25.md) | Pakollinen |
| Hankinta | [Estä yleisten budjettivarausten ylikulutus, kun työnkulussa on useita ostoehdotuksia](whats-new-scm-10-0-21.md) | Käytössä oletusarvoisesti |
| Hankinta | [Ostosopimuksen vastuullinen osapuoli](../procurement/purchase-agreements.md) | Pakollinen |
| Hankinta | [Ostotilausten tallennetut näkymät](saved-views-scm.md) | Pakollinen |
| Tuotetietojen hallinta | Tuoterakenteen raportin esikäsittely aikakatkaisun välttämiseksi | Pakollinen |
| Tuotetietojen hallinta | Taloushallinnon oletusdimensiot erikseen, kun käytetään nimikemalleja | Pakollinen |
| Tuotetietojen hallinta | Ota tuotedimensioryhmät käyttöön nimikemalleille | Pakollinen |
| Tuotetietojen hallinta | [Parannettu suunnittelun muutostenhallinnan määritteiden periytyvyys](../engineering-change-management/engineering-attributes-and-search.md) | Pakollinen |
| Tuotetietojen hallinta | Nimike–viivakoodiyksikön parannukset | Pakollinen |
| Tuotetietojen hallinta | Luo tuotevarianttien nimet uudelleen nimikkeistön perusteella | Pakollinen |
| Tuotetietojen hallinta | [Julkaistujen tuotteiden tallennetut näkymät](saved-views-scm.md) | Pakollinen |
| Tuotetietojen hallinta | [Muuttujaehdotukset-sivun parannukset](../pim/tasks/create-predefined-product-variants.md) | Pakollinen |
| Myynti ja markkinointi | [Myyntitilauksen kulujen kohdistus](/dynamics365-release-plan/2020wave1/dynamics365-supply-chain-management/miscellaneous-charges-enhancements) | Pakollinen |
| Myynti ja markkinointi | Tyhjennä myyntitilauksen päivityshistoria | Pakollinen |
| Myynti ja markkinointi | [Myynnin päivityshistorian tyhjentäminen iän perusteella](../sales-marketing/sales-update-history-cleanup-performance-improvements.md) | Pakollinen |
| Myynti ja markkinointi | [Yhteyshenkilön tietoyksikön viennin optimointi](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/contact-person-data-entity-export-optimization) | Pakollinen |
| Myynti ja markkinointi | Kopioi myynnin hyvityslaskun kokonaisalennusryhmä | Pakollinen |
| Myynti ja markkinointi | [Ota käyttöön myyntitarjousasiakirjan esittely ja asiakirjojen loppulausekentät](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/lookup-functionality-document-introduction-document-conclusion-fields-sales-quotation-page) | Pakollinen |
| Myynti ja markkinointi | [Paranna 100 parasta -asiakasraportin suorituskykyä](whats-new-scm-10-0-23.md) | Pakollinen |
| Myynti ja markkinointi | Sisällytä odottavat tietueet historian puhdistustehtäviin | Pakollinen |
| Myynti ja markkinointi | Rajoita myyntitilausrivien määrää erätehtävää kohden | Käytössä oletusarvoisesti |
| Myynti ja markkinointi | [Rajoita kirjausta varten valittavien myyntitilausten määrää](whats-new-scm-10-0-21.md) | Pakollinen |
| Myynti ja markkinointi | Laske arvioitu asiakkaan saldo uudelleen | Pakollinen |
| Myynti ja markkinointi | [Myyntipalautustilauksen rivin rekisteröinti desimaalitarkkuudella sekä todellisen painon kanssa että ilman todellista painoa](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/sales-return-order-line-registration-decimal-precision-without-catch-weight) | Pakollinen |
| Myynti ja markkinointi | [Myynnin ja markkinoinnin tallennetut näkymät](saved-views-scm.md) | Pakollinen |
| Myynti ja markkinointi | [Myyntitilauksen vahvistus yhdellä napsautuksella](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/single-click-sales-order-confirmation) | Pakollinen |
| Kuljetustenhallinta | Salli rahtilaskujen täsmäytyksen poistaminen rahtilaskun riveiltä ilman kirjatun toimittajan laskun kirjauskansiota | Käytössä oletusarvoisesti |
| Kuljetustenhallinta | [Ota käyttöön toimittajan laskukirjauskansion luonti rahtilaskun hylkäämisen yhteydessä](whats-new-scm-10-0-20.md) | Käytössä oletusarvoisesti |
| Kuljetustenhallinta | [Pienten pakettien lähetys](../warehousing/small-parcel-shipping.md) | Käytössä oletusarvoisesti |
| Kuljetustenhallinta | [USMCA-alkuperätodistusasiakirja](../transportation/usmca-certification-of-origin.md) | Käytössä oletusarvoisesti |
| Varastonhallinta   | [Sijainnin lisävyöhyke](../warehousing/additional-location-zones.md) | Pakollinen |
| Varastonhallinta   | [Peruuta työ](../warehousing/cancel-warehouse-work.md) | Pakollinen |
| Varastonhallinta   | [Konsolidoi lähetys](../warehousing/configure-shipment-consolidation-policies.md) | Käytössä oletusarvoisesti |
| Varastonhallinta   | [Luo ja käsittele siirtotilauksia varastosovelluksesta](../warehousing/create-transfer-order-from-warehouse-app.md) | Pakollinen |
| Varastonhallinta   | Cross-docking-mallit ja sijaintidirektiivit | Käytössä oletusarvoisesti |
| Varastonhallinta   | [Erota hyllytys lähetysilmoituksista (ASN)](whats-new-scm-10-0-21.md) | Käytössä oletusarvoisesti |
| Varastonhallinta   | [Lykätyt hyllytystoiminnot](../warehousing/deferred-processing-manual-inventory-movement.md) | Käytössä oletusarvoisesti |
| Varastonhallinta   | Lykätty hyllytys – kontti | Käytössä oletusarvoisesti |
| Varastonhallinta   | Lykätyn hyllytyksen käsittely – ota käyttöön tarkistusmallin ominaisuudelle, jonka käynnistintapahtumaksi on määritetty Aiempi | Pakollinen |
| Varastonhallinta   | [Poista odotettujen vastaanottojen käyttö laatutilauksissa, joihin varastot ovat estotilassa](../inventory/inventory-blocking.md) | Käytössä oletusarvoisesti |
| Varastonhallinta   | Ota käyttöön varaston mobiililaitteiden nopea oikeellisuustarkistus | Pakollinen |
| Varastonhallinta   | [Joustava varastotason dimensiovaraus](../warehousing/flexible-warehouse-level-dimension-reservation.md) | Käytössä oletusarvoisesti |
| Varastonhallinta   | [Joustava tilaukseen sidottu rekisterikilven varaus](../warehousing/flexible-warehouse-level-dimension-reservation.md) | Käytössä oletusarvoisesti |
| Varastonhallinta   | [Lähtevän kuormituksen visualisointi](../warehousing/outbound-workload-visualization.md) | Pakollinen |
| Varastonhallinta   | [Nimikkeen konsolidointisijainnin käyttöaste](../warehousing/item-consolidation-location-utilization.md) | Käytössä oletusarvoisesti |
| Varastonhallinta   | Rekisterikilven vastaanottohistoria | Käytössä oletusarvoisesti |
| Varastonhallinta   | [Manuaalisen lähetyksen konsolidointi](../warehousing/consolidate-shipments-manual-workbench.md) | Käytössä oletusarvoisesti |
| Varastonhallinta   | [Materiaalin käsittelylaitteiden rajapinta](../warehousing/mhax.md) | Pakollinen |
| Varastonhallinta   | [Suunniteltu cross-docking](../warehousing/planned-cross-docking.md) | Käytössä oletusarvoisesti |
| Varastonhallinta   | [Käsittele varastosovelluksen tapahtumat](../warehousing/warehouse-app-events.md) | Pakollinen |
| Varastonhallinta   | Rinnakkaistuotteen ja sivutuotteen poispanon työmallin kyselyn parannus | Pakollinen |
| Varastonhallinta   | [Pyöristä määrät alaspäin lähimpään myyntiyksikköön varastoon vapautuksen yhteydessä](whats-new-scm-10-0-19.md) | Pakollinen |
| Varastonhallinta   | [Tallennettu näkymä kuormasuunnittelun työtilaa varten](saved-views-scm.md) | Pakollinen |
| Varastonhallinta   | [Työn tietosivun tallennettu näkymä](saved-views-scm.md) | Pakollinen |
| Varastonhallinta   | [Tallennettu näkymä aallon käsittelyä varten](saved-views-scm.md) | Pakollinen |
| Varastonhallinta   | [Tallennetut näkymät kuorman käsittelyä varten](saved-views-scm.md) | Pakollinen |
| Varastonhallinta   | [Tallennetut näkymät lähetyksen käsittelyä varten](saved-views-scm.md) | Pakollinen |
| Varastonhallinta   | Lähetysaallon etikettien tiedot | Käytössä oletusarvoisesti |
| Varastonhallinta   | [Paikoita yhdistetyt yksiköt](whats-new-scm-10-0-21.md) | Pakollinen |
| Varastonhallinta   | [Käytä nopeampaa ohjelmointirajapintaa konttien sulkemiseen/uudelleenavaamiseen pakkausasemalla](whats-new-scm-10-0-21.md) | Käytössä oletusarvoisesti |
| Varastonhallinta   | [Tarkista täydennystöitä varten valitut mallit](whats-new-scm-10-0-20.md) | Käytössä oletusarvoisesti |
| Varastonhallinta   | [Varastosovelluksen ylemmälle tasolle siirretyt kentät](../warehousing/warehouse-app-promoted-fields.md) | Käytössä oletusarvoisesti |
| Varastonhallinta   | [Varastosovelluksen vaiheohjeet](../warehousing/mobile-app-titles-instructions.md) | Käytössä oletusarvoisesti |
| Varastonhallinta   | [Varastosijainnin tila](../warehousing/warehouse-location-status.md) | Käytössä oletusarvoisesti |
| Varastonhallinta   | [Warehouse Management -sovelluksen kiertotie](../warehousing/warehouse-app-detours.md) | Käytössä oletusarvoisesti |
| Varastonhallinta   | [Aallon erätyön tiedot](../warehousing/wave-processing.md) | Pakollinen |
| Varastonhallinta   | [Aallon suoritusilmoitukset](../warehousing/wave-execution-notifications.md) | Pakollinen |

## <a name="additional-resources"></a>Lisäresurssit

### <a name="platform-updates-for-finance-and-operations-apps"></a>Taloushallinnon ja toimintojen sovellusten ympäristöpäivitykset

Microsoft Dynamics 365 Supply Chain Management 10.0.29 sisältää Platform updateja. Lisätietoja on kohdassa [taloushallinnon ja toimintojen sovellusten (kesäkuu 2022) käyttöympäristön päivitysversio 10.0.29.](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-29.md). <!--KFM: Confirm link -->

### <a name="bug-fixes"></a>Ohjelmavirhekorjaukset

Saat lisätietoja version 10.0.29 virheenkorjauksista eri päivityksissä kirjautumalla sisään Lifecycle Services (LCS) -sovellukseen ja lukemalla [Knowledge Base -artikkelin](https://fix.lcs.dynamics.com/Issue/Details?bugId=726559).

### <a name="dynamics-365-and-industry-clouds-2022-release-wave-1-plan"></a>Dynamics 365:n ja toimialan pilvipalvelu: 2022 julkaisuaalto 1 -suunnitelma

Haluatko tietoja tulevien ja juuri julkaistujen yrityssovellustemme tai -ympäristöjemme ominaisuuksista?

Katso [Dynamics 365:n ja toimialan pilvipalvelu: 2022 julkaisuaalto 2 -suunnitelma](/dynamics365-release-plan/2022wave2/). Olemme koonneet kaikki tarvittavat tiedot yhteen asiakirjaan, jota voit käyttää suunnittelun apuna.

### <a name="removed-and-deprecated-supply-chain-management-features"></a>Poistetut ja vanhentuneet Supply Chain Management -toiminnot

[Dynamics 365 Supply Chain Managementin poistetut tai vanhentuneet toiminnot](removed-deprecated-features-scm-updates.md) -artikkelissa kerrotaan toiminnoista, jotka on ajoitettu poistettaviksi tai vanhentuviksi tai jotka on poistettu Supply Chain Managementissa.

- *Poistettu* ominaisuus ei ole enää käytettävissä tuotteessa.
- *Vanhentunutta* ominaisuutta ei enää kehitetä aktiivisesti ja se voidaan poistaa tulevassa päivityksessä.

Ennen kuin toiminto poistetaan tuotteesta, siitä annetaan vanhentumisilmoitus [Dynamics 365 Supply Chain Managementin poistetut tai vanhentuneet toiminnot](removed-deprecated-features-scm-updates.md) -artikkelissa 12 kuukautta ennen poistoa.

Jos muutokset vaikuttavat vain käännösaikaan, mutta ne ovat binaarisesti yhteensopivia Sandbox- ja tuotantoympäristön kanssa, vanhentumisaika on lyhyempi kuin 12 kuukautta. Yleensä nämä toiminnalliset päivitykset on tehtävä kääntäjään.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
