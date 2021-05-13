---
title: Dynamics 365 Supply Chain Managementin version 10.0.18 uudet tai muuttuneet ominaisuudet (toukokuu 2021)
description: Tässä ohjeaiheessa käsitellään Dynamics 365 Supply Chain Managementin version 10.0.18 uusia tai muuttuneita ominaisuuksia.
author: kamaybac
ms.date: 03/01/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-03-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: d84520b8f551df847cb5d77d8dcbce1701d3795b
ms.sourcegitcommit: d77b2175a3364694b5c74e0062e317f612416796
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/22/2021
ms.locfileid: "5934964"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-version-10018-may-2021"></a>Dynamics 365 Supply Chain Managementin version 10.0.18 uudet tai muuttuneet ominaisuudet (toukokuu 2021)

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa kerrotaan Microsoft Dynamics 365 Supply Chain Managementin version 10.0.18 uudet tai muuttuneet ominaisuudet. Tämän version koontinumero on 10.0.793. Se on käytettävissä seuraavasti:

- **Julkaisun esikatselu:** Maaliskuu 2021
- **Julkaisun yleinen saatavuus (itsepäivitys):** Huhtikuu 2021
- **Julkaisun yleinen saatavuus (automaattinen päivitys):** Toukokuu 2021

## <a name="features-included-in-this-release"></a>Tähän julkaisuun sisältyvät toiminnot

Tämä julkaisu sisältää seuraavat toiminnot. Saat lisätietoja kunkin ominaisuuden virallisista julkaisupäivämääristä avaamalla [julkaisusuunnitelman](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/planned-features) linkkejä.

- Ostotilausten automaattinen vapautus (parannus [Varastonohjaukseen pilven scale unitien avulla](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/warehouse-execution-scale-units-cloud))<br> - Lisätietoja on kohdassa [Varaston hallinnan kuormitukset pilven ja reunan asteikon yksiköitä varten](../cloud-edge/cloud-edge-workload-warehousing.md).

- [Yritystason inventaariosuorituskyvyn parannukset ja arkistointi](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/enterprise-scale-inventory-performance-improvements-archiving)<br> - Lisätietoja: [Varastotapahtumien arkistointi](../inventory/archive-inventory-transactions.md)

- [Ostohyvitysten hallinta](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/rebate-management)<br> - Lisätietoja on kohdassa [Ostohyvitysten hallintamoduulin yleiskatsaus](../rebate-management/rebate-management-overview.md).

- [Myyntitietoyksikön viennin asetuskäytäntö](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/sales-data-entity-export-setup-policy)

- [Myyntipalautustilauksen rivin rekisteröinti desimaalitarkkuudella sekä todellisen painon kanssa että ilman todellista painoa](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/sales-return-order-line-registration-decimal-precision-without-catch-weight)

- [Myyntitilauksen vahvistus yhdellä napsautuksella](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/single-click-sales-order-confirmation)

- [Myyntitilauksesta ostotilausrivin poistokäytäntöön](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/sales-order-purchase-order-line-deletion-policy)

- Yksinkertainen liittymä vain töihin sisään- ja uloskirjautumiselle (parannus [Parannettuun valmistustuotannon toteutusliittymään](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/enhanced-production-floor-execution-interface-manufacturing))<br> - Lisätietoja on kohdassa [Tuotannon käyttöliittymän määrittäminen](../production-control/production-floor-execution-configure.md).

Useimmat näistä toiminnoista on otettava käyttöön [Toimintojen hallinta](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) -kohdassa ennen niiden käyttämistä.

## <a name="new-and-updated-documentation-resources"></a>Uudet ja päivitetyt asiakirjaresurssit

Seuraavat ohjeaiheet on lisätty äskettäin tai niitä on päivitetty merkittävästi. Ne eivät välttämättä liity tähän versioon liitettyihin uusiin ominaisuuksiin, jotka on mainittu edellisessä osassa, mutta ne voivat auttaa käyttämään nykyisiä ominaisuuksia tehokkaammin.

- [Varaston näkyvyyden apuohjelma](../inventory/inventory-visibility.md)
- [Aiheutunut kustannus -moduuli](../landed-cost/landed-cost-overview.md)
- [Materiaalin käsittelylaitteiden rajapinta (MHAX)](../warehousing/mhax.md)
- [Suunnittelun optimoinnin sopivuusanalyysi](../master-planning/planning-optimization/planning-optimization-fit-analysis.md)

## <a name="additional-resources"></a>Lisäresurssit

### <a name="platform-updates-for-finance-and-operations-apps"></a>Ympäristön päivitykset Finance and Operations -sovelluksille

Microsoft Dynamics 365 Supply Chain Management 10.0.18 sisältää Platform updateja. Lisätietoja on kohdassa [Finance and Operations -sovellusten (toukokuu 2021) käyttöympäristön päivitysversio 10.0.18](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-18.md).

### <a name="bug-fixes"></a>Ohjelmavirhekorjaukset

Saat lisätietoja version 10.0.18 virheenkorjauksista päivityksissä kirjautumalla sisään Lifecycle Services (LCS) -sovellukseen ja tarkastelemalla [Knowledge Base -artikkelia](https://fix.lcs.dynamics.com/Issue/Details?bugId=561679&dbType=3&qc=13bb1641c1be430ead8b21ae3d4e0f800d5b81c39b3a56e890db1de7ede59e46).

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