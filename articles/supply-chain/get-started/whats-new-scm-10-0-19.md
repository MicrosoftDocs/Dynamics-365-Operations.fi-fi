---
title: Dynamics 365 Supply Chain Managementin 10.0.19:n esikatselu (heinäkuu 2021)
description: Tässä ohjeaiheessa käsitellään Dynamics 365 Supply Chain Managementin version 10.0.19 uusia tai muuttuneita ominaisuuksia.
author: kamaybac
ms.date: 04/23/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-04-23
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 8bb4a7c8085b40ab3eca72675dbe7a3be412d8c1
ms.sourcegitcommit: 2eb7a9ae544f504155657c5c584cbac66c21dba4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/29/2021
ms.locfileid: "5961678"
---
# <a name="preview-of-dynamics-365-supply-chain-management-10019-july-2021"></a>Dynamics 365 Supply Chain Managementin 10.0.19:n esikatselu (heinäkuu 2021)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Tässä ohjeaiheessa käsitellään Microsoft Dynamics 365 Supply Chain Managementin esiversion 10.0.19 uusia tai muuttuneita ominaisuuksia. Tämän version koontinumero on 10.0.837. Se on käytettävissä seuraavasti:

- **Julkaisun esiversio:** huhtikuu 2021
- **Julkaisun yleinen saatavuus (itsepäivitys):** kesäkuu 2021
- **Julkaisun yleinen saatavuus (automaattinen päivitys):** heinäkuu 2021

## <a name="features-included-in-this-release"></a>Tähän julkaisuun sisältyvät toiminnot

Seuraavassa taulukossa on tämän julkaisun sisältämät toiminnot. *Ominaisuus*-sarakkeessa on linkki [julkaisusuunnitelmaan](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/planned-features), jossa voit tarkastella kuinkin ominaisuuden virallisia julkaisupäiviä. *Lisätietoja*-sarakkeessa on linkkejä liittyvään dokumentaatioon.

Useimmat näistä toiminnoista on otettava käyttöön [Toimintojen hallinta](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) -kohdassa ennen niiden käyttämistä. Osa luettelon ominaisuuksista on vielä esiversioita, kun taas toiset ovat yleisesti saatavana.

| Ominaisuusalue | Ominaisuus | Lisätietoja |
|---|---|---|
| Varasto ja logistiikka | [Yhteyshenkilön tietoyksikön viennin optimointi](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/contact-person-data-entity-export-optimization)  | *Ei käytettävissä* |
| Varasto ja logistiikka | [Varastojen suoritustoimintojen asteittaiset parannukset scale uniteilla](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/incremental-enhancements-warehouse-execution-capabilities-scale-units) |[Sanoman käsittelijän sanomat](../cloud-edge/cloud-edge-message-processor-messages.md)<br><br>[Varasto-oikaisu](../cloud-edge/cloud-edge-warehouse-inventory-adjustment.md)<br><br>[Varaston hallinnan kuormitukset pilven ja reunan asteikon yksiköitä varten](../cloud-edge/cloud-edge-workload-warehousing.md) |
| Varasto ja logistiikka | [Hakutoiminnot asiakirjan esittely- ja loppulausekentissä Myyntitarjous-sivulla](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/lookup-functionality-document-introduction-document-conclusion-fields-sales-quotation-page) | *Ei käytettävissä* |
| Varasto ja logistiikka | [Varastonohjaus reunan scale uniteilla mukautetussa laitteistossa](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/warehouse-execution-edge-scale-units-custom-hardware) | [Ota reunan scale unitit käyttöön mukautetussa laitteistossa LBD:n avulla](../cloud-edge/cloud-edge-edge-scale-units-lbd.md) |
| Valmistus | [Tuotannonohjaus reunan scale uniteilla mukautetussa laitteistossa](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/manufacturing-execution-edge-scale-units-custom-hardware) | [Ota reunan scale unitit käyttöön mukautetussa laitteistossa LBD:n avulla](../cloud-edge/cloud-edge-edge-scale-units-lbd.md) |
| Suunnittelu | Kyselypohjainen suunniteltujen tilausten vahvistaminen | [Vahvista suunnitellut tilaukset](../master-planning/planning-optimization/planned-order-firming.md) |
| Tuotetietojen hallinta | [Muuttujaehdotukset-sivun parannukset](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/variant-suggestions-page-improvements) | [Luo ennalta määriteltyjä tuotevariantteja](../pim/tasks/create-predefined-product-variants.md) |

## <a name="new-and-updated-documentation-resources"></a>Uudet ja päivitetyt asiakirjaresurssit

Seuraavat ohjeaiheet on lisätty äskettäin tai niitä on päivitetty merkittävästi. Ne eivät välttämättä liity tähän versioon liitettyihin uusiin ominaisuuksiin, jotka on mainittu edellisessä osassa, mutta ne voivat auttaa käyttämään nykyisiä ominaisuuksia tehokkaammin.

| Ominaisuusalue | Uudet tai päivitetyt ohjeaiheet |
|---|---|
| Suunnittelun muutosten hallinta | [Suunnittelun muutosten hallinnan usein kysytyt kysymykset](../engineering-change-management/change-management-faq.md) |
| Hankinta | [Toimittajien luokkapyynnöt](../procurement/category-requests-from-vendors.md) |
| Tuotetietojen hallinta | [Mittayksikön hallinta](../pim/tasks/manage-unit-measure.md)<br><br>[Tuotekonfiguraatiomallin laskelmat](../pim/config-model-calculations.md) |
| Tuotannonhallinta | [Työtunnusten yhdistetty numerosarja](../production-control/unified-job-ids.md) |
| Kuljetustenhallinta | [LTL-luokat](../transportation/ltl-class.md)<br><br>[NMFC-koodit](../transportation/nmfc-codes.md) |
| Varastonhallinta   | [Varaston erä- ja sarjavaraushierarkioiden vianmääritys](../warehousing/troubleshoot-warehouse-batch-and-serial-reservation-hierarchies.md) |
| Varastonhallinta, aallon luonti ja käsittely | [Aaltojen luominen ja käsittely](../warehousing/wave-processing.md)<br><br>[Varaston parametrit aaltokäsittelyä varten](../warehousing/wave-warehouse-parameters.md)<br><br>[Aaltomallit](../warehousing/wave-templates.md)<br><br>[Aallon kohdistus](../warehousing/wave-allocation-method.md)<br><br>[Työn luomisen ajoitus aallon aikana](../warehousing/configure-wave-schedule-work-creation.md)<br><br>[Konttiinpakkaus](../warehousing/wave-containerization.md)<br><br>[Aallon suoritusilmoitukset](../warehousing/wave-execution-notifications.md) |

## <a name="additional-resources"></a>Lisäresurssit

### <a name="platform-updates-for-finance-and-operations-apps"></a>Ympäristön päivitykset Finance and Operations -sovelluksille

Microsoft Dynamics 365 Supply Chain Management 10.0.19 sisältää Platform updateja. Lisätietoja on kohdassa [Finance and Operations -sovellusten (kesäkuu 2021) käyttöympäristön päivitysversio 10.0.19](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-19.md).

### <a name="bug-fixes"></a>Ohjelmavirhekorjaukset

Saat lisätietoja version 10.0.19 virheenkorjauksista päivityksissä kirjautumalla sisään Lifecycle Services (LCS) -sovellukseen ja tarkastelemalla [Knowledge Base -artikkelia](https://fix.lcs.dynamics.com/Issue/Details?bugId=575415).

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
