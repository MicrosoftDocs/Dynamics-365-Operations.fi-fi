---
title: Dynamics 365 Supply Chain Managementin version 10.0.13 esiversio-ominaisuudet (lokakuu 2020)
description: Tässä ohjeaiheessa käsitellään Dynamics 365 Supply Chain Managementin version 10.0.13 uusia tai muuttuneita ominaisuuksia.
author: kamaybac
manager: tfehr
ms.date: 07/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-07-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: dae936ea9a72b865096cdda54d767f3e44816e20
ms.sourcegitcommit: 27233e0fda61dac541c5210ca8d94ab4ba74966f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/03/2020
ms.locfileid: "3652230"
---
# <a name="preview-features-in-dynamics-365-supply-chain-management-10013-october-2020"></a>Dynamics 365 Supply Chain Managementin version 10.0.13 esiversio-ominaisuudet (lokakuu 2020)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Tässä ohjeaiheessa käsitellään Microsoft Dynamics 365 Supply Chain Managementin esikatseluversion 10.0.13 uusia tai muuttuneita ominaisuuksia. Tämän version koontinumero on 10.0.569. Se on käytettävissä seuraavasti: 

- **Ennakkoesitys:** Elokuu 2020
- **Yleinen saatavuus (oma päivitys):** Syyskuu 2020
- **Automaattinen päivitys:** Lokakuu 2020

## <a name="features-included-in-this-release"></a>Tähän julkaisuun sisältyvät toiminnot

Tämä julkaisu sisältää seuraavat toiminnot. Toiminnon otsikoiden linkki lisätietoihin [Julkaisusuunnitelmat](https://docs.microsoft.com/dynamics365/release-plans/)-sivustossa. Lisälinkit osoittavat lisädokumentaatioon, jotka toiminnosta ovat tällä hetkellä saatavilla. Useimmat näistä toiminnoista on otettava käyttöön [Toimintojen hallinta](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) -kohdassa ennen niiden käyttämistä.

- [Sanaston muuttaminen termistä "varaston sulkemisen peruuttaminen" termiin "varaston sulkemisen palauttaminen"](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-supply-chain-management/change-terminology-inventory-closing-cancellation-inventory-closing-reverse)<br> - Lisätietoja on kohdassa [Varaston sulkeminen](../cost-management/inventory-close.md).

- [Vahvista lähtevät lähetykset erätöistä](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/finance-operations/dynamics365-supply-chain-management/confirm-outbound-shipments-batch-jobs)<br> - Lisätietoja on kohdassa [Lähtevien lähetysten vahvistaminen erätöistä](../warehousing/confirm-outbound-shipments-from-batch-jobs.md).

- [Useiden ostotyönimikkeiden delegoiminen](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-supply-chain-management/delegation-multiple-purchasing-work-items)<br> - Lisätietoja on kohdassa [Työnkulun työnimikkeiden delegoiminen](../../fin-ops-core/fin-ops/organization-administration/tasks/delegate-work-items-workflow.md).

- [Erä- ja sarjanumeroiden antaminen, kun valmistuminen ilmoitetaan työkorttilaitteesta](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/finance-operations/dynamics365-supply-chain-management/enter-serial-numbers-while-reporting-as-finished-job-card-device)<br> - Lisätietoja on kohdassa [Ilmoita valmiiksi työkorttilaitteesta](../production-control/report-finished-job-device.md).

- [Tuoteversion seurannan ja parannetun laajennettavuuden uudet varastodimensiot](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/finance-operations/dynamics365-supply-chain-management/new-inventory-dimensions-product-version-tracking-enhanced-extensibility)<br> - Lisätietoja on kohdassa [Tuotedimensiot](../pim/product-dimensions.md).

- [Rekisterikilpiin perustuva tilaussidonnainen varaus](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/finance-operations/dynamics365-supply-chain-management/order-committed-reservation-based-license-plates-lp-picking-processing)<br> - Lisätietoja on kohdassa [Joustavan rekisterikilven varaus](../warehousing/flexible-warehouse-level-dimension-reservation.md#flexible-license-plate-reservation).

- [Lähtevän kuormituksen visualisointi](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/finance-operations/dynamics365-supply-chain-management/warehouse-management--workload-visualization)

- [Työn keräilyrivin yhteenveto](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/finance-operations/dynamics365-supply-chain-management/work-pick-line-overview)

- [Saapuvan työn työkäytäntöjen parannukset](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/finance-operations/dynamics365-supply-chain-management/work-policy-enhancements-inbound-work)<br> - Lisätietoja on kohdassa [Varaston käytännöt](../warehousing/warehouse-work-policies.md).

## <a name="additional-resources"></a>Lisäresurssit

### <a name="platform-updates-for-finance-and-operations-apps"></a>Ympäristön päivitykset Finance and Operations -sovelluksille

Microsoft Dynamics 365 Supply Chain Management 10.0.13 sisältää Platform updateja. Lisätietoja on kohdassa [Finance and Operations -sovellusten (lokakuu 2020) käyttöympäristön päivitysversio 10.0.13](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-update-10-0-13.md).

### <a name="bug-fixes"></a>Ohjelmavirhekorjaukset

Saat lisätietoja version 10.0.13 virheenkorjauksista päivityksissä kirjautumalla sisään Lifecycle Services (LCS) -sovellukseen ja tarkastelemalla [Knowledge Base -artikkelia](https://fix.lcs.dynamics.com/Issue/Details?bugId=476824&dbType=3&qc=18d329e7d9887a622bada690791f5814dbbef22bb6f4eaada3718299f40132fd). 

### <a name="dynamics-365-2020-release-wave-2-plan"></a>Dynamics 365: vuoden 2020 julkaisuaallon 2 suunnitelma

Haluatko tietoja tulevien ja juuri julkaistujen yrityssovellustemme tai -ympäristöjemme ominaisuuksista?

Tutustu kohtaan [Dynamics 365: vuoden 2020 julkaisuaallon 2 suunnitelma](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/index). Olemme koonneet kaikki tarvittavat tiedot yhteen asiakirjaan, jota voit käyttää suunnittelun apuna.

### <a name="removed-and-deprecated-supply-chain-management-features"></a>Poistetut ja vanhentuneet Supply Chain Management -toiminnot

[Dynamics 365 Supply Chain Managementin poistetut tai vanhentuneet toiminnot](removed-deprecated-features-scm-updates.md) -ohjeaiheessa kerrotaan toiminnoista, jotka on ajoitettu poistettaviksi tai vanhentuviksi tai jotka on poistettu Supply Chain Managementissa.

- *Poistettu* ominaisuus ei ole enää käytettävissä tuotteessa.
- *Vanhentunutta* ominaisuutta ei enää kehitetä aktiivisesti ja se voidaan poistaa tulevassa päivityksessä.

Ennen kuin toiminto poistetaan tuotteesta, siitä annetaan vanhentunisilmoitus [Dynamics 365 Supply Chain Managementin poistetut tai vanhentuneet toiminnot](removed-deprecated-features-scm-updates.md) -ohjeaiheessa 12 kuukautta ennen poistoa.

Jos muutokset vaikuttavat vain käännösaikaan, mutta ne ovat binaarisesti yhteensopivia Sandbox- ja tuotantoympäristön kanssa, vanhentumisaika on lyhyempi kuin 12 kuukautta. Yleensä nämä toiminnalliset päivitykset on tehtävä kääntäjään.
