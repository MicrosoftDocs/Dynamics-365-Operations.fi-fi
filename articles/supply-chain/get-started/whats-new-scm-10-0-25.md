---
title: Dynamics 365 Supply Chain Management -sovelluksen uudet tai muuttuneet ominaisuudet, versio 10.0.25 (huhtikuu 2022)
description: Tässä artikkelissa käsitellään Microsoft Dynamics 365 Supply Chain Managementin 10.0.25 uusia tai muuttuneita toimintoja.
author: kamaybac
ms.date: 03/14/2022
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-02-01
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: 1fa2ec6e21026552a4f14a67188db0720d3feae5
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8850783"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-10025-april-2022"></a>Dynamics 365 Supply Chain Management -sovelluksen uudet tai muuttuneet ominaisuudet, versio 10.0.25 (huhtikuu 2022)

[!include [banner](../includes/banner.md)]

Tässä artikkelissa käsitellään Microsoft Dynamics 365 Supply Chain Managementin version 10.0.25 uusia tai muuttuneita ominaisuuksia. Tämän version koontinumero on 10.0.1149. Se on käytettävissä seuraavasti:

- **Julkaisun esiversio:** helmikuu 2022
- **Julkaisun yleinen saatavuus (oma päivitys):** maaliskuu 2022
- **Julkaisun yleinen saatavuus (automaattinen päivitys):** huhtikuu 2022

## <a name="features-included-in-this-release"></a>Tähän julkaisuun sisältyvät toiminnot

Seuraavassa taulukossa on tämän julkaisun sisältämät toiminnot. Tämän artikkelin päivitys saattaa sisältää ominaisuuksia, jotka on otettu käyttöön koontiversiossa tämän artikkelin alkuperäisen julkaisin jälkeen.

| Ominaisuusalue | Ominaisuus | Lisätietoja | Käyttöönottaja:   |
|---|---|---|---|
| Varasto&nbsp;ja&nbsp;logistiikka | [Vaarallisten materiaalien parannukset](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/hazardous-materials-enhancements) | Tulossa pian | Toimintojen hallinta:<br>*Vaarallisten materiaalien parannukset* |
| Varasto&nbsp;ja&nbsp;logistiikka | [Pakkausasemien pakkaustyö](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/packing-work-packing-stations) | Tulossa pian | Toimintojen hallinta:<br>*Pakkausasemien pakkaustyö* |
| Varasto&nbsp;ja&nbsp;logistiikka | [Skannaa varaston viivakoodit GS1-muotostandardien avulla](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/scan-barcodes-warehouse-using-gs1-format-standards) | [GS1-viivakoodit ja QR-koodit](../warehousing/gs1-barcodes.md) | Toimintojen hallinta:<br>*Skannaa GS1-viivakoodit* |
| Valmistus | [Materiaalin kulutus ja varaukset tuotannon käyttöliittymässä](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/material-consumption-reservations-production-floor-execution-interface) | [Tuotannon käyttöliittymän käytön ohjeet työntekijöille](../production-control/production-floor-execution-use.md) | Toimintojen hallinta:<br>*(Esiversio) Rekisteröi materiaalin kulutus tuotannon käyttöliittymässä (muu kuin VHJ)*<br><br>Ja/tai:<br><br>Toimintojen hallinta:<br>*(Esiversio) Rekisteröi materiaalikulutus tuotannon käyttöliittymässä (käytössä WMS:ssä)* |
| Valmistus | [Rekisteröi materiaalikulutus skaalausyksiköissä](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/register-material-consumption-scale-units) | [Valmistuksen suorituksen kuormitukset pilven ja reunan asteikon yksiköitä varten](../cloud-edge/cloud-edge-workload-manufacturing.md) | Toimintojen hallinta:<br>*Rekisteröi materiaalikulutus skaalausyksikön mobiilisovelluksessa* |
| Suunnittelu | [Suunnittelun optimointi - keskitetty kalenterin ylläpito](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planning-optimization-centralized-calendar-maintenance) | [Kalenterit ja pääsuunnittelu](../master-planning/supply-chain-calendars-master-planning.md) | Oletusarvoisesti käytössä |
| Suunnittelu | [Optimointiehdotusten suunnittelu aiemmin luodun toimituksen optimointia varten](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planning-optimization-suggestions-optimize-existing-supply) | [Toimintosanomat](../master-planning/action-messages.md) | Oletusarvoisesti käytössä |
| Suunnittelu | Yksinkertaiset suunnitellut tilaukset | [Yksinkertaiset suunnitellut tilaukset](../master-planning/planning-optimization/planned-orders-simplified.md ) | Toimintojen hallinta:<br>*Yksinkertaiset suunnitellut tilaukset* |

## <a name="feature-enhancements-included-in-this-release"></a>Tähän julkaisuun sisältyvät toiminnon parannukset

Seuraavassa taulukossa on tämän julkaisun sisältämät ominaisuuksien parannukset. Jokainen näistä parannuksista parantaa aiemmin luotua toimintoa lisäysten avulla. Koska ne ovat vain parannuksia, niitä ei ole lueteltu [vapautussuunnitelmassa](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planned-features). Jos kuitenkin haluat varmistaa, että nämä parannukset eivät ole ristiriidassa aiemmin luotujen mukautuksiesi tai asetuksesi kanssa, kaikki muutokset ovat oletusarvon mukaan pois käytöstä (ellei toisin ilmoiteta).

Jos haluat ottaa jonkin näistä ominaisuuksista käyttöön tai poistaa ne käytöstä, sinun on tehtävä se [ominaisuuksienhallinnassa](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

| Moduuli | Ominaisuuden nimi ominaisuuksienhallinnassa | Lisätietoja |
|---|---|---|
| Varastonhallinta | (Puola) Salli useiden SAD-laskujen linkitys yhden SAD:n yhteen ostotilausriviin | Tämän ominaisuuden avulla voit jakaa ostotilausrivejä ja linkittää ne yhteen valvonta-asiakirjaan (SAD), kun nämä ostotilausrivit on kirjattu useassa eri laskussa (esimerkiksi eri lähetyksille). |
| Hankinta | Konsolidoi useat ostoehdotukset yhdeksi ostotilaukseksi kirjauspäivän mukaan | Tämän ominaisuuden avulla useita ostoehdotuksia voidaan konsolidoida yhdeksi ostotilaukseksi, jos eri ostoehdotuksilla on eri kirjanpitopäivät. Ostotilausten luomisen ja kysynnän konsolidoinnin ostokäytännön säännöt voidaan määrittää automatisoimaan päätös, joka koskee ehdotusrivien ryhmittelyä kirjanpitopäivän mukaan ostotilaustasolla. Ostotilausten konsolidointia kirjanpitopäivämäärän mukaan ei tueta, jos budjetin hallinta on käytössä, koska kirjanpidon päivämäärää käytetään budjettivarauksissa ja varauksissa. Siksi se on säilytettävä siirryttäessä ostoehdotuksesta ostotilaukseen. |
| Hankinta | Näytä vanhat tarjouspyynnön oletusvastauskenttäasetukset | Tämä ominaisuus palauttaa vanhat tarjouspyynnön oletusvastauskentän asetukset, jotka on aiemmin poistettu käyttöliittymästä. Nämä asetukset eivät toimita mitään toimintoja valmiina, mutta niitä voi mukauttaa toimittamaan niitä tarvittaessa. Ota tämä toiminto käyttöön, jos organisaatiosi on jo lisännyt toimintoja tarjouspyynnön oletusvastauskentän asetuksiin tai aikoo käyttää lisätä niitä. Kun tämä ominaisuus on käytössä, voit käyttää asetuksia **hankintaparametrien** sivulla,avaamalla **Tarjouspyyntö**-välilehden ja valitsemalla **tarjouksen oletusvastauskentät**. |
| Hankinta | Yhdistä sen toimittajan taloushallinnon dimensiot, jolla on aktiivisen dimension linkin taloushallinnon dimensio ostotilauksessa | Tämän ominaisuuden avulla voit yhdistää toimittajien taloushallinnon dimensiot aktiivisen dimension kanssa. Linkitä taloushallinnon dimensiot ostoehdotuksen hyväksymisen jälkeen, jos määrität linkin taloushallinnon dimension ja toimipaikan varastodimension välille. Ostotilauksen luomisen ja kysynnän konsolidoinnin oston käytäntösäännöt voidaan määrittää edistämään päätöstä taloushallinnon dimensioiden yhdistämisestä toimittajilta aktiivisen dimension kanssa. Linkitä taloushallinnon dimensio ostotilauksen otsikon tasolla. |
| Tuotannonhallinta | (Venäjä) Ota käyttöön tuotannon kaavan / tuoterakenteen ja automaattisen GTD-varauksen/-kulutuksen oletussijainnin määritys tuotannossa | Tämä ominaisuus ottaa käyttöön lisäasetuksia tuotantoon tuoduista raaka-aineista (vain Venäjän lokalisointi).<ul><li>Automaattisen oletussijainnin määrittäminen tuotantokaavoille ja tuoterakenteelle sekä resurssiryhmissä että varastoissa.</li><li>Raaka-aineiden automaattinen varaus *GTD-numero*-dimension mukaan WMS-aktivoidussa varastoissa ei-WMS-varausalgoritmin mukaan. Tämä pätee, kun *raaka-aineiden keräilyä* koskeva työkäytäntö on käytössä ja **työn luontimenetelmänä** on *Ei koskaan* ja varasto, sijainti ja nimiketunnus vastaavat tuotanto(erä)tilauksen varastotapahtumia.</li><li>Automaattinen raaka-aineiden kulutus *GTD-numero*-dimension mukaan keräysluettelon kirjaamisen yhteydessä aiemmin kuvatun hankitun varauksen mukaisesti.</li></ul> |
| Varastonhallinta   | (Esiversio) Saapuvien ja lähtevien varastotilausten skaalausyksikön tuki | Tämän toiminnon avulla järjestelmä luo lähtevät varastotilaukset vapautus varastoon -prosessin aikana sekä luo saapuvia varastotilauksia, kun siirtotilaukset kirjataan toimitetuiksi. Järjestelmä synkronoi sitten kunkin saapuvan tai lähtevän varastotilauksen toimituksesta tai vastaanottamisesta vastaavalle skaalausyksikölle. Huomaa, että kun tämä ominaisuus on otettu käyttöön, varaston suorituksen kuormitukset on päivitettävä. Lisätietoja on kohdassa [Varaston hallinnan kuormitukset pilven ja reunan asteikon yksiköitä varten](../cloud-edge/cloud-edge-workload-warehousing.md).<br><br>Tämä ominaisuus vaatii *Erota hyllytys lähetysilmoituksista (ASN)* -toiminnon, ja se mahdollistaa siirtotilausten vastaanottamisen Warehouse Management -mobiilisovelluksessa rekisterikilpeä käyttäen. |

## <a name="feature-state-changes-in-this-release"></a>Tämän julkaisun toiminnon tilan muutokset

Seuraavassa taulukossa luetellaan ominaisuudet, jotka tulivat pakollisiksi tai oletusarvoisesti käyttöön versiossa 10.0.25. Kaikki nämä toiminnot tulevat automaattisesti käyttöön järjestelmässä heti, kun päivität versioksi 10.0.25. Pakollisia ominaisuuksia ei voi poistaa käytöstä, mutta oletusarvoisesti käytössä olevia ominaisuuksia voi silti poistaa käytöstä käyttämällä [ominaisuuksien hallintaa](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

Taulukossa luetellaan myös aiemmat julkisen esiversion ominaisuudet, mutta jotka ovat muuttuneet yleisesti käytettäviksi versiossa 10.0.25, mikä tarkoittaa sitä, että niitä suositellaan käytettäviksi tuotantoympäristöissä. Nämä toiminnot ovat oletusarvon mukaan pois käytöstä, ellei toisin ilmoiteta, joten ne on otettava käyttöön käyttämällä [ominaisuuksien hallintaa](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), jos haluat käyttää niitä.

| Moduuli | Toiminnon nimi | Ominaisuuden tila |
| --- | --- | --- |
| Resurssien hallinta | [Käytä sääntöjä työtilausten ryhmittelyyn ylläpitosuunnitelman ollessa käynnissä](../asset-management/preventive-and-reactive-maintenance/creating-work-orders.md) | Yleisesti saatavilla |
| Resurssien hallinta | [Vastaperusteiset ylläpitoparannukset](../asset-management/preventive-and-reactive-maintenance/maintenance-plans.md) | Yleisesti saatavilla |
| Kustannushintojen hallinta | [Kustannuslaskentataso](../cost-management/cost-calculation-level.md) | Yleisesti saatavilla |
| Kustannushintojen hallinta | Ota käyttöön käyttäjän määrittämät eränumeroasetukset varaston käänteistä sulkutoimenpidettä varten | Yleisesti saatavilla |
| Kustannushintojen hallinta | [Varaston sulkemisen edistymistiedot](whats-new-scm-10-0-21.md) | Yleisesti saatavilla |
| Kustannushintojen hallinta | [Varastokustannuksen uudelleenarvostuksen taloushallinnon dimensioiden oletusasetukset](../cost-management/manage-standard-cost-updates.md) | Yleisesti saatavilla |
| Kustannushintojen hallinta | Varaston arvon raportin tietojen puhdistus | Käytössä oletusarvoisesti |
| Kustannushintojen hallinta | [Varastoarvoraporttien säiliö](../cost-management/inventory-value-report-storage.md) | Käytössä oletusarvoisesti |
| Kustannushintojen hallinta | Näytä varaston sulkemisen loki ruudukossa | Käytössä oletusarvoisesti |
| Suunnittelun muutosten hallinta | [Aiemmin luotujen tuotteiden muutostenhallinnan ottaminen käyttöön](../engineering-change-management/change-management-existing-products.md) | Käytössä oletusarvoisesti |
| Suunnittelun muutosten hallinta | [Suunnittelun muutosten hallinta](../engineering-change-management/product-engineering-overview.md) | Käytössä oletusarvoisesti |
| Suunnittelun muutosten hallinta | [Suunnittelun ilmoitukset tuotannolle](../engineering-change-management/engineering-change-management.md) | Käytössä oletusarvoisesti |
| Suunnittelun muutosten hallinta | [Parannettu suunnittelun muutostenhallinnan määritteiden periytyvyys](../engineering-change-management/engineering-attributes-and-search.md) | Käytössä oletusarvoisesti |
| Suunnittelun muutosten hallinta | [Hallitse kaavojen ja niiden ainesosien muutoksia](../engineering-change-management/manage-formula-changes.md) | Käytössä oletusarvoisesti |
| Suunnittelun muutosten hallinta | [Tuotteen valmiustarkistukset](../engineering-change-management/product-readiness.md) | Käytössä oletusarvoisesti |
| Suunnittelun muutosten hallinta | [Muuttujien luominen suunnittelun tuotteille](../engineering-change-management/engineering-variants.md) | Käytössä oletusarvoisesti |
| Varastonhallinta | Siirtyminen tuoterakenneriveiltä tuoterakenneversioon. | Pakollinen |
| Pääsuunnittelu | [Suunniteltujen suur- ja pakkauserätilausten eräkelpoinen vahvistaminen ja konsolidointi](whats-new-scm-10-0-20.md) | Yleisesti saatavilla |
| Pääsuunnittelu | Resurssien suunnittelu ja ylläpito | Yleisesti saatavilla |
| Pääsuunnittelu | Ota käyttöön pääsuunnitelman asetusten ohjatun toiminnon ominaisuudet | Pakollinen |
| Pääsuunnittelu | [Ennustemallinvalinta kysynnän ennusteen tiedoissa](../master-planning/manual-adjustments-baseline-forecast.md) | Pakollinen |
| Pääsuunnittelu | [Pääsuunnittelun edistymisen visualisointi](../master-planning/tasks/monitor-master-planning-run.md) | Pakollinen |
| Pääsuunnittelu | [Suunniteltujen tilausten rinnakkainen vahvistaminen](../master-planning/planning-optimization/planned-order-firming.md) | Pakollinen |
| Pääsuunnittelu | [Suunnitellun tilauksen vahvistaminen suodatuksen kanssa](../master-planning/planning-optimization/planned-order-firming.md) | Käytössä oletusarvoisesti |
| Pääsuunnittelu | [Suunniteltujen tilausten tallennetut näkymät](saved-views-scm.md) | Käytössä oletusarvoisesti |
| Hankinta | Poista ostoehdotuksen jakelun palautuspainike käytöstä | Yleisesti saatavilla |
| Hankinta | [Ota käyttöön hankintaan liittyvien työnkulkujen nollaus](whats-new-scm-10-0-20.md) | Yleisesti saatavilla |
| Hankinta | Mahdollisuus vahvistaa hyväksytyt ostotilaukset toimittajayhteistyöstä erässä | Pakollinen |
| Hankinta | Ostosopimuksen Suljettu-tila | Pakollinen |
| Hankinta | Lisää rivejä ostosopimukseen liittyviin ostotilauslaskuihin | Käytössä oletusarvoisesti |
| Hankinta | Lisää Tilattu määrä -kenttä Tuotteen vastaanoton kirjaus -sivulle | Käytössä oletusarvoisesti |
| Hankinta | [Salli toimittajien käyttää hankintaluokkia toimittajayhteistyön avulla](../procurement/category-requests-from-vendors.md) | Käytössä oletusarvoisesti |
| Hankinta | Ostotilausten veloitusten lähde- ja kohdesummat | Käytössä oletusarvoisesti |
| Hankinta | Veloitusten määritys toimipaikan ja varaston mukaan | Käytössä oletusarvoisesti |
| Hankinta | Ota käyttöön ostoveron laskeminen vuosittaisen tariffin perusteella | Käytössä oletusarvoisesti |
| Hankinta | [Ostosopimuksen vastuullinen osapuoli](../procurement/purchase-agreements.md) | Käytössä oletusarvoisesti |
| Hankinta | [Ostotilausten tallennetut näkymät](saved-views-scm.md) | Käytössä oletusarvoisesti |
| Tuotetietojen hallinta | [Oletustilausmäärien tarkka vahvistus](../production-control/default-order-settings.md) | Pakollinen |
| Tuotetietojen hallinta | Tuoterakenteen raportin esikäsittely aikakatkaisun välttämiseksi | Käytössä oletusarvoisesti |
| Tuotetietojen hallinta | Taloushallinnon oletusdimensiot erikseen, kun käytetään nimikemalleja | Käytössä oletusarvoisesti |
| Tuotetietojen hallinta | Ota tuotedimensioryhmät käyttöön nimikemalleille | Käytössä oletusarvoisesti |
| Tuotetietojen hallinta | Luo tuotevarianttien nimet uudelleen nimikkeistön perusteella | Käytössä oletusarvoisesti |
| Tuotetietojen hallinta | [Muuttujaehdotukset-sivun parannukset](../pim/tasks/create-predefined-product-variants.md) | Käytössä oletusarvoisesti |
| Tuotannonhallinta | Parantunut tuotannon todellisen painon määrän keräily | Yleisesti saatavilla |
| Tuotannonhallinta | Työkorttipääte-sivulle on lisätty uusi Lopeta tauko -painike | Pakollinen |
| Tuotannonhallinta | [Ota käyttöön rekisterikilven numeron automaattinen luonti, kun työkorttilaitteessa raportoidaan valmiiksi](../production-control/production-floor-execution-configure.md) | Pakollinen |
| Tuotannonhallinta | Ota käyttöön alihankintana hankittujen nimikkeiden osittainen vastaanotto ja korjaa Toimittaja-tyypin tuoterakennerivien hävikkilaskennan ongelma | Pakollinen |
| Tuotannonhallinta | [Ominaisuus, jolla voi lukita työkorttilaitteen ja työkorttipäätteen desinfiointia varten](../production-control/production-floor-execution-configure.md) | Pakollinen |
| Tuotannonhallinta | Töiden hyväksynnän ja siirron valintaikkunoiden parannukset | Pakollinen |
| Tuotannonhallinta | [Rekisterikilpi valmiiksi raportointia varten on lisätty työkorttilaitteeseen](../production-control/production-floor-execution-configure.md) | Pakollinen |
| Tuotannonhallinta | [Tulosta etiketti työkorttilaitteesta](../production-control/production-floor-execution-configure.md) | Pakollinen |
| Tuotannonhallinta | [Tuotannon suoritus](../production-control/production-floor-execution-configure.md) | Pakollinen |
| Tuotannonhallinta | [Tuotannonohjausliittymän käyttöomaisuuden hallintatoiminto](../production-control/production-floor-execution-configure.md) | Käytössä oletusarvoisesti |
| Tuotannonhallinta | [Töiden haku tuotannon työnohjausliittymälle](../production-control/production-floor-execution-configure.md) | Käytössä oletusarvoisesti |
| Tuotannonhallinta | [Ohita oletustuotantovaraus](../production-control/override-default-reservation-principle.md) | Käytössä oletusarvoisesti |
| Tuotannonhallinta | [Näytä täydet sarja-, erä- ja rekisterinumerot tuotannon käyttöliittymässä](whats-new-scm-10-0-21.md) | Käytössä oletusarvoisesti |
| Myynti ja markkinointi | [Myyntitilauksen tietojen suorituskykyparannus](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/sales-order-details-performance-enhancement) | Yleisesti saatavilla |
| Myynti ja markkinointi | Myyntitarjouksen tietojen suorituskykyparannus | Yleisesti saatavilla |
| Myynti ja markkinointi | Myyntitilauksen viitattujen tietojen vientikäytäntö | Pakollinen |
| Myynti ja markkinointi | [Myyntitilauksesta ostotilausrivin poistokäytäntöön](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/sales-order-purchase-order-line-deletion-policy) | Pakollinen |
| Myynti ja markkinointi | [Myyntitarjouksen viitattujen tietojen vientikäytäntö](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/sales-quotation-referenced-data-export-policy)| Pakollinen |
| Myynti ja markkinointi | [Yhteyshenkilön tietoyksikön viennin optimointi](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/contact-person-data-entity-export-optimization) | Käytössä oletusarvoisesti |
| Myynti ja markkinointi | Ota käyttöön myyntitarjousasiakirjan esittely ja asiakirjojen loppulausekentät | Käytössä oletusarvoisesti |
| Myynti ja markkinointi | [Paranna 100 parasta -asiakasraportin suorituskykyä](whats-new-scm-10-0-23.md) | Käytössä oletusarvoisesti |
| Myynti ja markkinointi | Laske arvioitu asiakkaan saldo uudelleen | Käytössä oletusarvoisesti |
| Myynti ja markkinointi | [Myyntipalautustilauksen rivin rekisteröinti desimaalitarkkuudella sekä todellisen painon kanssa että ilman todellista painoa](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/sales-return-order-line-registration-decimal-precision-without-catch-weight) | Käytössä oletusarvoisesti |
| Myynti ja markkinointi | [Myynnin ja markkinoinnin tallennetut näkymät](saved-views-scm.md) | Käytössä oletusarvoisesti |
| Myynti ja markkinointi | Myyntitilauksen vahvistus yhdellä napsautuksella | Käytössä oletusarvoisesti |
| Varastonhallinta   | [Cross docking -mallit ja sijaintidirektiivit](../warehousing/planned-cross-docking.md) | Yleisesti saatavilla |
| Varastonhallinta   | [Poista odotettujen vastaanottojen käyttö laatutilauksissa, joihin varastot ovat estotilassa](../inventory/inventory-blocking.md) | Yleisesti saatavilla |
| Varastonhallinta   | Rekisterikilven vastaanottohistoria | Yleisesti saatavilla |
| Varastonhallinta   | [Materiaalin käsittelylaitteiden rajapinta](../warehousing/mhax.md) | Yleisesti saatavilla |
| Varastonhallinta   | [Pyöristä määrät alaspäin lähimpään myyntiyksikköön varastoon vapautuksen yhteydessä](whats-new-scm-10-0-19.md) | Yleisesti saatavilla |
| Varastonhallinta   | Varastosovelluksen työluetteloiden yksikkötuki | Yleisesti saatavilla |
| Varastonhallinta   | Lähetysaallon etikettien tiedot | Yleisesti saatavilla |
| Varastonhallinta   | [Käytä nopeampaa ohjelmointirajapintaa konttien sulkemiseen/uudelleenavaamiseen pakkausasemalla](whats-new-scm-10-0-21.md) | Yleisesti saatavilla |
| Varastonhallinta   | [Tarkista täydennystöitä varten valitut mallit](whats-new-scm-10-0-20.md) | Yleisesti saatavilla |
| Varastonhallinta   | Salli täydennysmallin käyttää olemassa olevaa välitöntä täydennystyötä (yksiköiden välillä) | Pakollinen |
| Varastonhallinta   | Automaattinen GUID-tunnusten määrittäminen WHS-käyttäjän luonnissa | Pakollinen |
| Varastonhallinta   | Tallenna tuotevariantit ja seurantadimensiot varastointisovelluksessa kuormanimikkeen vastaanoton aikana | Pakollinen |
| Varastonhallinta   | [Muuta seurantadimensioilla hallittujen nimikkeiden varastotilaa](../inventory/inventory-statuses.md) | Pakollinen |
| Varastonhallinta   | [Työpoolin vaihtaminen työssä](../warehousing/change-work-pool-on-work.md) | Pakollinen |
| Varastonhallinta   | [Klusterisijainti täynnä](../warehousing/cluster-position-full.md) | Pakollinen |
| Varastonhallinta   | [Klusterin hyllytysominaisuus](../warehousing/putaway-clusters.md) | Pakollinen |
| Varastonhallinta   | [Vahvistus ja siirtäminen](../warehousing/confirm-and-transfer.md) | Pakollinen |
| Varastonhallinta   | [Vahvista lähtevät lähetykset erätöistä](../warehousing/confirm-outbound-shipments-from-batch-jobs.md) | Pakollinen |
| Varastonhallinta   | [Määritä, näytetäänkö vastaanoton yhteenvetosivu mobiililaitteissa](../warehousing/warehousing-mobile-device-app-license-plate-receiving.md) | Pakollinen |
| Varastonhallinta   | [Manuaalisen varastosiirtotoiminnon lykätty käsittely](../warehousing/deferred-processing-manual-inventory-movement.md) | Pakollinen |
| Varastonhallinta   | Älä salli sellaisten kuormien luomista, jotka eivät täytä aallon kuormanrakennusmallin vaatimuksia | Pakollinen |
| Varastonhallinta   | [Laajennetut rekisterikilpien etikettien asettelut](../warehousing/document-routing-layout-for-license-plates.md) | Pakollinen |
| Varastonhallinta   | [Arvioi kaikki useiden varastointiyksiköiden sijaintidirektiivien toiminnot](../troubleshooting/warehousing/evaluate-multiple-location-directive-actions.md) | Pakollinen |
| Varastonhallinta   | Piilota Kokonaisarvo-kenttä Kaikki kuormat- ja Kuorman tiedot -sivuilla | Pakollinen |
| Varastonhallinta   | Rekisterikilven etiketin koontiversiomääritys | Pakollinen |
| Varastonhallinta   | Kuormarivin manuaalinen korjaus järjestelmänvalvojille tai vastaaville luotettaville käyttäjille | Pakollinen |
| Varastonhallinta   | [Toimipaikan rekisterikilpien paikannus](../warehousing/location-license-plate-positioning.md) | Pakollinen |
| Varastonhallinta   | [Tuotedimensioiden yhdistäminen sijainnissa](../warehousing/location-product-dimension-mixing.md) | Pakollinen |
| Varastonhallinta   | Tee mobiililaitteen varastosiirron varaston tilan kentästä muokattava | Pakollinen |
| Varastonhallinta   | Manuaalinen myyntirivin keräyspalvelu järjestelmänvalvojalle tai vastaaville luotettaville käyttäjille | Pakollinen |
| Varastonhallinta   | [Estä siirtotilauksen lähetettyjen rekisterikilpien käyttäminen muissa varastoissa kuin kohdevarastossa.](../warehousing/warehousing-mobile-device-app-license-plate-receiving.md) | Pakollinen |
| Varastonhallinta   | Moniselitteisten sijainnin ja rekisterikilven nimien ratkaisukehote | Pakollinen |
| Varastonhallinta   | [Laaduntarkistus](../warehousing/quality-check.md) | Pakollinen |
| Varastonhallinta   | [Uuden varastosovelluksen käyttäjäasetukset, kuvakkeet ja vaiheotsikot](../warehousing/install-configure-warehouse-management-app.md) | Pakollinen |
| Varastonhallinta   | [Sijainnin lisävyöhyke](../warehousing/additional-location-zones.md) | Käytössä oletusarvoisesti |
| Varastonhallinta   | [Luo ja käsittele siirtotilauksia varastosovelluksesta](../warehousing/create-transfer-order-from-warehouse-app.md) | Käytössä oletusarvoisesti |
| Varastonhallinta   | Ota käyttöön varaston mobiililaitteiden nopea oikeellisuustarkistus | Käytössä oletusarvoisesti |
| Varastonhallinta   | [Varastonhallinnan käytettävissä olevan varaston merkintöjen siivoustyön enimmäissuoritusaika](../warehousing/onhand-cleanup.md) | Käytössä oletusarvoisesti |
| Varastonhallinta   | [Lähtevän kuormituksen visualisointi](../warehousing/outbound-workload-visualization.md) | Käytössä oletusarvoisesti |
| Varastonhallinta   | [Käsittele varastosovelluksen tapahtumat](../warehousing/warehouse-app-events.md) | Käytössä oletusarvoisesti |
| Varastonhallinta   | [Tallennettu näkymä kuormasuunnittelun työtilaa varten](saved-views-scm.md) | Käytössä oletusarvoisesti |
| Varastonhallinta   | [Työn tietosivun tallennettu näkymä](saved-views-scm.md) | Käytössä oletusarvoisesti |
| Varastonhallinta   | [Tallennettu näkymä aallon käsittelyä varten](saved-views-scm.md) | Käytössä oletusarvoisesti |
| Varastonhallinta   | [Tallennetut näkymät kuorman käsittelyä varten](saved-views-scm.md) | Käytössä oletusarvoisesti |
| Varastonhallinta   | [Tallennetut näkymät lähetyksen käsittelyä varten](saved-views-scm.md) | Käytössä oletusarvoisesti |
| Varastonhallinta   | [Aallon erätyön tiedot](../warehousing/wave-processing.md) | Käytössä oletusarvoisesti |
| Varastonhallinta   | [Aallon suoritusilmoitukset](../warehousing/wave-execution-notifications.md) | Käytössä oletusarvoisesti |

## <a name="additional-resources"></a>Lisäresurssit

### <a name="platform-updates-for-finance-and-operations-apps"></a>Taloushallinnon ja toimintojen sovellusten ympäristöpäivitykset

Microsoft Dynamics 365 Supply Chain Management 10.0.25 sisältää Platform updateja. Lisätietoja on kohdassa [taloushallinnon ja toimintojen sovellusten (huhtikuu 2022) käyttöympäristön päivitysversio 10.0.25.](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-25.md).

### <a name="bug-fixes"></a>Ohjelmavirhekorjaukset

Saat lisätietoja version 10.0.25 virheenkorjauksista päivityksissä kirjautumalla sisään Lifecycle Services (LCS) -sovellukseen ja tarkastelemalla [Knowledge Base -artikkelia](https://fix.lcs.dynamics.com/Issue/Details?bugId=654580&dbType=3&qc=3799fa965b008dd980d27cf740e4582e6384ec6601ae8a35b7eaec6f1287a868).

### <a name="dynamics-365-and-industry-clouds-2022-release-wave-1-plan"></a>Dynamics 365:n ja toimialan pilvipalvelu: 2022 julkaisuaalto 1 -suunnitelma

Haluatko tietoja tulevien ja juuri julkaistujen yrityssovellustemme tai -ympäristöjemme ominaisuuksista?

Katso [Dynamics 365:n ja toimialan pilvipalvelu: 2022 julkaisuaalto 1 -suunnitelma](/dynamics365-release-plan/2022wave1/). Olemme koonneet kaikki tarvittavat tiedot yhteen asiakirjaan, jota voit käyttää suunnittelun apuna.

### <a name="removed-and-deprecated-supply-chain-management-features"></a>Poistetut ja vanhentuneet Supply Chain Management -toiminnot

[Dynamics 365 Supply Chain Managementin poistetut tai vanhentuneet toiminnot](removed-deprecated-features-scm-updates.md) -artikkelissa kerrotaan toiminnoista, jotka on ajoitettu poistettaviksi tai vanhentuviksi tai jotka on poistettu Supply Chain Managementissa.

- *Poistettu* ominaisuus ei ole enää käytettävissä tuotteessa.
- *Vanhentunutta* ominaisuutta ei enää kehitetä aktiivisesti ja se voidaan poistaa tulevassa päivityksessä.

Ennen kuin toiminto poistetaan tuotteesta, siitä annetaan vanhentumisilmoitus [Dynamics 365 Supply Chain Managementin poistetut tai vanhentuneet toiminnot](removed-deprecated-features-scm-updates.md) -artikkelissa 12 kuukautta ennen poistoa.

Jos muutokset vaikuttavat vain käännösaikaan, mutta ne ovat binaarisesti yhteensopivia Sandbox- ja tuotantoympäristön kanssa, vanhentumisaika on lyhyempi kuin 12 kuukautta. Yleensä nämä toiminnalliset päivitykset on tehtävä kääntäjään.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
