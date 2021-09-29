---
title: Dynamics 365 Supply Chain Managementin uudet ja muuttuneet ominaisuudet 10.0.20. (elokuu 2021)
description: Tässä ohjeaiheessa käsitellään Dynamics 365 Supply Chain Managementin version 10.0.20 uusia tai muuttuneita ominaisuuksia.
author: kamaybac
ms.date: 05/28/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-05-28
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 99e95a7fbdce3d040ab7bf01474921ae1f616468
ms.sourcegitcommit: b5f2d88ff4e0a234fa6b9ee33516425e54ff2c3b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/21/2021
ms.locfileid: "7506828"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-10020-august-2021"></a>Dynamics 365 Supply Chain Managementin uudet ja muuttuneet ominaisuudet 10.0.20. (elokuu 2021)

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa käsitellään Microsoft Dynamics 365 Supply Chain Managementin version 10.0.20 uusia tai muuttuneita ominaisuuksia. Tämän version koontinumero on 10.0.886. Se on käytettävissä seuraavasti:

- **Julkaisun esiversio:** Toukokuu 2021
- **Julkaisun yleinen saatavuus (itsepäivitys):** heinäkuu 2021
- **Julkaisun yleinen saatavuus (automaattinen päivitys):** elokuu 2021

## <a name="features-included-in-this-release"></a>Tähän julkaisuun sisältyvät toiminnot

Seuraavassa taulukossa on tämän julkaisun sisältämät toiminnot. *Ominaisuus*-sarakkeessa on linkki [julkaisusuunnitelmaan](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/planned-features), jossa voit tarkastella kuinkin ominaisuuden virallisia julkaisupäiviä. *Lisätietoja*-sarakkeessa on lisätietoja ja/tai linkkejä liittyvään dokumentaatioon.

Useimmat näistä toiminnoista on otettava käyttöön [Toimintojen hallinta](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) -kohdassa ennen niiden käyttämistä.

| Ominaisuusalue | Ominaisuus | Lisätietoja |
|---|---|---|
| Varasto&nbsp;ja&nbsp;logistiikka | [Myyntitilauksen tietojen suorituskykyparannus](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/sales-order-details-performance-enhancement) | Tämä ominaisuus tekee käyttöliittymästä joustavamman, kun myyntitilauksia avataan, erityisesti monia rivejä sisältävät tilaukset. |
| Valmistus | [Prosessin automaation aktivoiminen laatutilausten luontia varten](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/invoke-process-automation-flows-create-quality-orders) | [Prosessin automaation aktivoiminen laatutilausten luontia varten](../production-control/process-automation-quality-orders.md ) |
| Valmistus | [Parannettu tuotantokerroksen tehtävän käyttöliittymä](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/enhanced-production-floor-execution-interface-manufacturing) | [Tuotannon käyttöliittymän määrittäminen](../production-control/production-floor-execution-configure.md) |
| Suunnittelu | [Suunnittelun optimoinnin ääretön kapasiteetin ajoitus](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/schedule-infinite-capacity-support-planning-optimization) | [Ajoitus rajattoman kapasiteetin avulla](../master-planning/planning-optimization/infinite-capacity-planning.md) |
| Tuotetietojen hallinta | [Reseptien ja niiden ainesosien muutosten hallinta](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/engineering-change-management-support-process-manufacturing) | [Kaavojen ja niiden osien muutosten hallinta](../engineering-change-management/manage-formula-changes.md) |
| Tuotetietojen hallinta | [Tuotteen valmiustarkistukset](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/product-readiness-checks) | [Tuotteen valmius](../engineering-change-management/product-readiness.md) |

## <a name="feature-enhancements-included-in-this-release"></a>Tähän julkaisuun sisältyvät toiminnon parannukset

Seuraavassa taulukossa on tämän julkaisun sisältämät toimintojen parannukset. Jokainen näistä parantaa aiemmin luotua toimintoa lisäysten avulla. Koska ne ovat vain parannuksia, niitä ei ole lueteltu [vapautussuunnitelmassa](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/planned-features). Jos kuitenkin haluat varmistaa, että nämä parannukset eivät ole ristiriidassa aiemmin luotujen mukautuksiesi tai asetuksesi kanssa, kaikki muutokset ovat oletusarvon mukaan pois käytöstä (ellei toisin ilmoiteta). Jos haluat käyttää mitä tahansa näistä ominaisuuksista, ne on nimenomaisesti otettava käyttöön [ominaisuuksienhallinnassa](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

| Ominaisuusalue | Ominaisuuden&nbsp;nimi&nbsp;ominaisuuksien&nbsp;hallinnassa | Lisätietoja |
|---|---|---|
| Pääsuunnittelu | Oikaistun kysynnän ennusteen rinnakkainen valtuuttaminen | Tämä ominaisuus sallii oikaistun tarve-ennusteen rinnakkaisen valtuuttamisen **oikaistun kysynnän ennuste** -sivulta. Tämän ominaisuuden tarkoituksena on parantaa suorituskykyä, kun suuri määrä ennusteita on valtuutettu. Valtuutettaessa käyttäjä voi määrittää **säikeiden määrän** valtuuttamisen valintaikkunassa. |
| Pääsuunnittelu | (Esiversio) Suunniteltujen bulkki- ja pakkauserätilausten eräkelpoinen vahvistaminen ja konsolidointi | Tämän ominaisuuden avulla voit käyttää erätöitä bulkki- ja pakkaustilausten vahvistamiseen ja konsolidointiin. |
| Tuotannonhallinta | Kopioi yleiset reitit | Tämä ominaisuus parantaa reitityskopioita, jotta käyttäjät voivat kopioida reitityksiä, jotka eivät ole nimikekohtaisia. Sen avulla järjestelmä voi päivittää kaikki merkitykselliset tiedot (kuten toimipaikka, reititysryhmä, resurssivaatimukset ja eri ajat) sen jälkeen, kun kopiointireititystoimintoa on käytetty korvaamaan nimikkeeseen vielä käyttämättä olevan reitityksen. |
| Tuotannonhallinta | Päivitä liittyvät resurssivaatimukset, kun reittitoimintoa muutetaan | Tämän ominaisuuden avulla järjestelmä voi päivittää liittyvät resurssivaatimukset sen jälkeen, kun käyttäjä on muuttanut aiemmin luodun reittivaiheen toimintoa. |
| Tuotetietojen hallinta | Tuoterakenneraportin esikäsittely aikakatkaisun estämiseksi | Tämä ominaisuus aiheuttaa tuoterakenneraportin esikäsiteltävän toiminnon. Näin vältytaan aikakatkaisulta, kun raportissa on suuri tietokuormitus. |
| Hankinta | Ota käyttöön hankintaan liittyvien työnkulkujen nollaus | Tämän esikatselutoiminnon avulla voit palauttaa seuraavat työnkulut luonnostilaan: Ostotilaus, Toimittajan muutos ja Ostoehdotukset. |
| Kuljetustenhallinta | Ota käyttöön toimittajan laskukirjauskansion luonti rahtilaskun hylkäämisen yhteydessä | Kun tämä ominaisuus on käytössä, vastaava toimittajan laskukirjauskansio luodaan täsmäytysyistä vain, kun käytät maksun toimittaja -vaihtoehtoa. Muussa tapauksessa laskukirjauskansio luodaan aina. |
| Varastonhallinta   | Tarkista täydennystöitä varten valitut mallit | Tämän ominaisuuden avulla voit varmistaa, että käyttäjät valitsevat kelvollisia täydennysmalleja, kun määrität täydennystyötä. Se estää käyttäjiä luomasta täydennystyötä ilman mallia ja valitsemasta malleja, joiden tyyppi on *Aallon kysyntä*, mikä ei luo täydennystyötä, ja työn käsittely voi kestää kauan. |

## <a name="new-and-updated-documentation-resources"></a>Uudet ja päivitetyt asiakirjaresurssit

Seuraavat ohjeaiheet on lisätty äskettäin tai niitä on päivitetty merkittävästi. Ne eivät välttämättä liity tähän versioon liitettyihin uusiin ominaisuuksiin, jotka on mainittu edellisessä osassa, mutta ne voivat auttaa käyttämään nykyisiä ominaisuuksia tehokkaammin.

| Ominaisuusalue | Uudet tai päivitetyt ohjeaiheet |
|---|---|
| Suunnittelun muutosten hallinta | [Tuotteen elinkaaren tilat ja tapahtumat](../engineering-change-management/product-lifecycle-state-transactions.md) |
| Inventoinnin- ja varastonhallinta | [Varaston näkyvyyden apuohjelma](../inventory/inventory-visibility.md)<br><br>[Laadun ja määrityksistä poikkeamisen yhteenveto](../inventory/quality-management-processes.md) (sekä kaikki liittyvät laadunhallinnan ohjeaiheet) |
| Hankinta | [Toimittajan varmenteen ylläpitäminen](../../finance/public-sector/manage-vendor-certification.md) |
| Tuotannonhallinta | [Tuotannon käyttöliittymän suunnitteleminen](../production-control/production-floor-execution-styles.md) |
| Varastonhallinta   | [Warehouse Management -mobiilisovelluksen vaihekuvakkeiden ja otsikoiden määrittäminen](../warehousing/step-icons-titles.md)<br><br>[Manuaalisen varastosiirron lykätty käsittely](../warehousing/deferred-processing-manual-inventory-movement.md) |

## <a name="additional-resources"></a>Lisäresurssit

### <a name="platform-updates-for-finance-and-operations-apps"></a>Ympäristön päivitykset Finance and Operations -sovelluksille

Microsoft Dynamics 365 Supply Chain Management 10.0.20 sisältää Platform updateja. Lisätietoja on kohdassa [Finance and Operations -sovellusten (kesäkuu 2021) käyttöympäristön päivitysversio 10.0.20](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-20.md).

### <a name="bug-fixes"></a>Ohjelmavirhekorjaukset

Saat lisätietoja version 10.0.20 virheenkorjauksista päivityksissä kirjautumalla sisään Lifecycle Services (LCS) -sovellukseen ja tarkastelemalla [Knowledge Base -artikkelia](https://fix.lcs.dynamics.com/Issue/Details?bugId=586707&dbType=3&qc=d0dad8eee2af234e8c288e2a7df14c579004518673d014be511f900cfed008f8). 

### <a name="dynamics-365-2021-release-wave-1-plan"></a>Dynamics 365: vuoden 2021 julkaisuaallon 1 suunnitelma

Haluatko tietoja tulevien ja juuri julkaistujen yrityssovellustemme tai -ympäristöjemme ominaisuuksista?

Tutustu kohtaan [Dynamics 365: vuoden 2021 julkaisuaallon 1 suunnitelma](/dynamics365-release-plan/2021wave1/). Olemme koonneet kaikki tarvittavat tiedot yhteen asiakirjaan, jota voit käyttää suunnittelun apuna.

### <a name="removed-and-deprecated-supply-chain-management-features"></a>Poistetut ja vanhentuneet Supply Chain Management -toiminnot

[Dynamics 365 Supply Chain Managementin poistetut tai vanhentuneet toiminnot](removed-deprecated-features-scm-updates.md) -ohjeaiheessa kerrotaan toiminnoista, jotka on ajoitettu poistettaviksi tai vanhentuviksi tai jotka on poistettu Supply Chain Managementissa.

- *Poistettu* ominaisuus ei ole enää käytettävissä tuotteessa.
- *Vanhentunutta* ominaisuutta ei enää kehitetä aktiivisesti ja se voidaan poistaa tulevassa päivityksessä.

Ennen kuin toiminto poistetaan tuotteesta, siitä annetaan vanhentunisilmoitus [Dynamics 365 Supply Chain Managementin poistetut tai vanhentuneet toiminnot](removed-deprecated-features-scm-updates.md) -ohjeaiheessa 12 kuukautta ennen poistoa.

Jos muutokset vaikuttavat vain käännösaikaan, mutta ne ovat binaarisesti yhteensopivia Sandbox- ja tuotantoympäristön kanssa, vanhentumisaika on lyhyempi kuin 12 kuukautta. Yleensä nämä toiminnalliset päivitykset on tehtävä kääntäjään.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
