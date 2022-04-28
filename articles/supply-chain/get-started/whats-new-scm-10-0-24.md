---
title: Dynamics 365 Supply Chain Managementin uudet tai muuttuneet ominaisuudet, versio 10.0.24 (helmikuu 2022)
description: Tässä ohjeaiheessa käsitellään Microsoft Dynamics 365 Supply Chain Managementin version 10.0.24 uusia tai muuttuneita ominaisuuksia.
author: kamaybac
ms.date: 12/03/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-12-03
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: a8f0dc5c7498d04230e5e7356979e08ee3a86052
ms.sourcegitcommit: 197e6ddee84522fd587c6e4ee4f9089101e301c2
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/13/2022
ms.locfileid: "8570279"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-10024-february-2022"></a>Dynamics 365 Supply Chain Managementin uudet tai muuttuneet ominaisuudet, versio 10.0.24 (helmikuu 2022)

[!include [banner](../includes/banner.md)]

Tässä aiheessa käsitellään Microsoft Dynamics 365 Supply Chain Managementin version 10.0.24 uusia tai muuttuneita ominaisuuksia. Tämän version koontinumero on 10.0.1084. Se on käytettävissä seuraavasti:

- **Julkaisun esiversio:** Joulukuu 2021
- **Version yleinen saatavuus (oma päivitys):** tammikuu 2022
- **Version yleinen saatavuus (automaattinen päivitys):** helmikuu 2022

## <a name="features-included-in-this-release"></a>Tähän julkaisuun sisältyvät toiminnot

Seuraavassa taulukossa on tämän julkaisun sisältämät toiminnot. Tämän aiheen päivitys saattaa sisältää ominaisuuksia, jotka on otettu käyttöön koontiversiossa tämän ohjeaiheen alkuperäisen julkaisin jälkeen.

| Ominaisuusalue | Ominaisuus | Lisätietoja | Käyttöönottaja:   |
|---|---|---|---|
| Jaettu hybriditopologia | [Tehostettu varastonohjauksen toiminta skaalausyksiköissä](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/enhanced-warehouse-execution-workloads-scale-units) | [Varaston hallinnan kuormitukset pilven ja reunan asteikon yksiköitä varten](../cloud-edge/cloud-edge-workload-warehousing.md) | Oletusarvoisesti käytössä. |
| Jaettu hybriditopologia | [Aloita pilvi- ja reunamittakaavayksikön varastonhallinnan työmäärän tuotantotilaus](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/enhanced-manufacturing-execution-workloads-scale-units) | [Valmistuksen suorituksen kuormitukset pilven ja reunan asteikon yksiköitä varten](../cloud-edge/cloud-edge-workload-manufacturing.md) | Ominaisuuksien hallinta (*Käynnistä tuotantotilaus varaston hallinnan kuormituksessa nykyisen pilven ja reunan skaalausyksiköitä varten*)  |
| Suunnittelu | [Uudelleentilausmarginaalin ja varasto-ottomarginaalin suunnittelun optimointi](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planning-optimization-support-reorder-margin-issue-margin) | [Varmuusmarginaalit](../master-planning/planning-optimization/safety-margins.md) | Oletusarvoisesti käytössä. |

## <a name="feature-enhancements-included-in-this-release"></a>Tähän julkaisuun sisältyvät toiminnon parannukset

Seuraavassa taulukossa on tämän julkaisun sisältämät ominaisuuksien parannukset. Jokainen näistä parannuksista parantaa aiemmin luotua toimintoa lisäysten avulla. Koska ne ovat vain parannuksia, niitä ei ole lueteltu [vapautussuunnitelmassa](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planned-features). Jos kuitenkin haluat varmistaa, että nämä parannukset eivät ole ristiriidassa aiemmin luotujen mukautuksiesi tai asetuksesi kanssa, kaikki muutokset ovat oletusarvon mukaan pois käytöstä (ellei toisin ilmoiteta).

Jos haluat ottaa jonkin näistä ominaisuuksista käyttöön tai poistaa ne käytöstä, sinun on tehtävä se [ominaisuuksienhallinnassa](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

| Moduuli | Ominaisuuden nimi ominaisuuksienhallinnassa | Lisätietoja |
|---|---|---|
| Tuotannonhallinta | Tuotantotilausten käytettävissä olevan materiaalin saatavuustarkistus | Tämä ominaisuus nopeuttaa **tuotantotilausten avaamista vapautus**-sivulle, joka on käytettävissä **tuotannonhallinnan** työtilassa. Jos tätä toimintoa ei ole, järjestelmä tarkistaa automaattisesti, onko kaikkien luetteloitujen tuotantotilausten käytettävissä materiaaleja heti, kun avaat sivun. Tämä voi kestää huomattavan kauan, jos tilauksia on paljon. Kun tämä ominaisuus on käytössä, järjestelmä käyttää työkalurivin painiketta, jonka avulla voit käynnistää materiaalien tarkistamisen vain valittujen tilausten osalta ja tarvittaessa. |
| Tuotannonhallinta | (Esiversio) Rekisteröi materiaalin kulutus tuotannon käyttöliittymässä (muu kuin VHJ) | Tämän ominaisuuden avulla työntekijät voivat käyttää tuotannon työnohjausliittymää materiaalin kulutuksen, eränumeroiden ja sarjanumeroiden rekisteröimiseen. Tämä toiminto tukee vain nimikkeitä, joita ei ole otettu käyttöön varaston lisäprosessien (WMS) käytössä. WMS-käytössä olevien nimikkeiden tuki on ajoitettu tulevaan versioon.<p>Joidenkin valmistajille, erityisesti prosessiteollisuusalojen valmistajille, on nimenomaisesti rekisteröitävä kussakin erässä tai tuotantotilauksissa kulutettu materiaalimäärä. Työntekijät voivat esimerkiksi käyttää vaakaa punnitsemaan työssään kulutetun materiaalin määrän. Organisaatioiden on myös kirjattava kunkin tuotteen valmistamisen eränumerot varmistaakseen, että materiaalista ei ole mitään materiaalia valmistava. |
| Tuotannonhallinta | Raportoi valmiiksi pilvi- ja reunamittakaavayksikön varastonhallinnan työmäärästä | Tämän ominaisuuden avulla työntekijät voivat Warehouse Management -mobiilisovelluksen avulla ilmoittaa tuotannon tai erätilauksen valmiiksi, kun sovellus on käynnissä varastonhallinnan kuormitusta pilvipalvelussa tai reunalla. Lisätietoja on kohdassa [Ilmoita valmiiksi ja aseta mittayksikköön](../cloud-edge/cloud-edge-workload-manufacturing.md#RAF). |
| Varastonhallinta   | Uudet kuormasuunnittelun työtilan sivut | Ottaa käyttöön uudet kuormasuunnittelun työtilan sivut: **Saapuvan kuormasuunnittelun työtila** ja **Lähtevän kuormasuunnittelun työtila**. |

## <a name="new-and-updated-documentation-resources"></a>Uudet ja päivitetyt asiakirjaresurssit

Seuraavat ohjeaiheet on lisätty äskettäin tai niitä on päivitetty merkittävästi. Nämä ohjeaiheet eivät välttämättä liity tällä julkaisulla lisättyihin, edellisessä osassa lueteltuihin uusiin ominaisuuksiin. Niiden avulla saatat kuitenkin saada enemmän irti olemassa olevista ominaisuuksista.

| Ominaisuusalue | Uudet tai päivitetyt ohjeaiheet |
|---|---|
| Kustannushintojen hallinta | [Varastoarvon raportit](../cost-management/inventory-value-report-storage.md) |
| Kustannushintojen hallinta | [Varaston arvon raporttien esimerkit ja logiikka](../cost-management/inventory-value-report-examples.md) |
| Pääsuunnittelu | [Suunnittelun optimoinnissa käytetyt päivämäärä- ja aikaparametrit](../master-planning/planning-optimization/date-time-used.md) |
| Pääsuunnittelu | [Kysynnän ennusteiden asetukset](../master-planning/demand-forecasting-setup.md) |
| Pääsuunnittelu | [Varmuusvaraston kirjauskansion käyttäminen nimikkeiden minimikattavuuden päivittämiseen](../master-planning/safety-stock-journal.md) |
| Tuotannonhallinta | [Tuotannon käyttöliittymän mukauttaminen](../production-control/production-floor-execution-customize.md) |
| Tuotannonhallinta | [Tuotannon käyttöliittymän suunnitteleminen](../production-control/production-floor-execution-styles.md) |
| Myynti ja markkinointi | [Myyntihistorian tietojen tyhjennyksen ajoitus](../sales-marketing/sales-update-history-cleanup-performance-improvements.md) |
| Varastonhallinta   | [Mobiililaitteen käyttäjätilit](../warehousing/mobile-device-work-users.md) |

## <a name="additional-resources"></a>Lisäresurssit

### <a name="platform-updates-for-finance-and-operations-apps"></a>Taloushallinnon ja toimintojen sovellusten ympäristöpäivitykset

Microsoft Dynamics 365 Supply Chain Management 10.0.24 sisältää Platform updateja. Lisätietoja on kohdassa [taloushallinnon ja toimintojen sovellusten (helmikuu 2022) käyttöympäristön päivitysversio 10.0.24.](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-24.md).

### <a name="bug-fixes"></a>Ohjelmavirhekorjaukset

Saat lisätietoja version 10.0.24 virheenkorjauksista päivityksissä kirjautumalla sisään Lifecycle Services (LCS) -sovellukseen ja tarkastelemalla [Knowledge Base -artikkelia](https://fix.lcs.dynamics.com/Issue/Details?bugId=641306&dbType=3&qc=5b1d5e49c96b8a5cfb5601889a413e6f3773ba6500f9bc47310dcc5c54fff42f).

### <a name="dynamics-365-and-industry-clouds-2021-release-wave-2-plan"></a>Dynamics 365:n ja toimialan pilvipalvelu: 2021 julkaisuaalto 2 -suunnitelma

Haluatko tietoja tulevien ja juuri julkaistujen yrityssovellustemme tai -ympäristöjemme ominaisuuksista?

Katso [Dynamics 365:n ja toimialan pilvipalvelu: 2021 julkaisuaalto 2 -suunnitelma](/dynamics365-release-plan/2021wave2/). Olemme koonneet kaikki tarvittavat tiedot yhteen asiakirjaan, jota voit käyttää suunnittelun apuna.

### <a name="removed-and-deprecated-supply-chain-management-features"></a>Poistetut ja vanhentuneet Supply Chain Management -toiminnot

[Dynamics 365 Supply Chain Managementin poistetut tai vanhentuneet toiminnot](removed-deprecated-features-scm-updates.md) -ohjeaiheessa kerrotaan toiminnoista, jotka on ajoitettu poistettaviksi tai vanhentuviksi tai jotka on poistettu Supply Chain Managementissa.

- *Poistettu* ominaisuus ei ole enää käytettävissä tuotteessa.
- *Vanhentunutta* ominaisuutta ei enää kehitetä aktiivisesti ja se voidaan poistaa tulevassa päivityksessä.

Ennen kuin toiminto poistetaan tuotteesta, siitä annetaan vanhentunisilmoitus [Dynamics 365 Supply Chain Managementin poistetut tai vanhentuneet toiminnot](removed-deprecated-features-scm-updates.md) -ohjeaiheessa 12 kuukautta ennen poistoa.

Jos muutokset vaikuttavat vain käännösaikaan, mutta ne ovat binaarisesti yhteensopivia Sandbox- ja tuotantoympäristön kanssa, vanhentumisaika on lyhyempi kuin 12 kuukautta. Yleensä nämä toiminnalliset päivitykset on tehtävä kääntäjään.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
