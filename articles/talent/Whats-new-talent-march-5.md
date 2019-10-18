---
title: Dynamics 365 Talentin uudet tai muuttuneet ominaisuudet (5. maaliskuuta 2019)
description: Tässä ohjeaiheessa käsitellään Microsoft Dynamics 365 Talentin uusia tai muuttuneita ominaisuuksia.
author: Darinkramer
manager: AnnBe
ms.date: 03/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-03-05
ms.dyn365.ops.version: Talent
ms.openlocfilehash: c7ee8f4cf14197d6bd4549741058fc5fe95ae55d
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/24/2019
ms.locfileid: "2026667"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-march-5-2019"></a>Dynamics 365 Talentin uudet tai muuttuneet ominaisuudet (5. maaliskuuta 2019)

[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa käsitellään Talentin uusia tai muuttuneita ominaisuuksia.

## <a name="changes-in-attract"></a>Attractin muutokset

### <a name="extending-option-sets-in-attract"></a>Attractin asetusjoukkojen laajentaminen

Attractissa on useita kenttiä, jotka ovat Common Data Servicen asetusjoukkoja. Asetusjoukkojen laajentamiseen on käytössä uusia asetuksia, kuten **Hylkäyssyy**-kenttä, **Työsuhteen tyyppi** -kenttä ja **Virkaikätyyppi**-kenttä.

> [!IMPORTANT]
> Työpaikan LinkedIniin julkaisemistoiminto edellyttää **Työn tiedot** -sivun **Työsuhteen tyyppi**- ja **Virkaikätyyppi**-kenttien käyttöä. LinkedIn tukee näiden kenttien oletusarvoja, ja ne näkyvät, kun työpaikka julkaistaan. Jos julkaiset työpaikkoja LinkedIniin ja muokkaat näiden kenttien nykyisiä asetusjoukon arvoja, työpaikka kyllä julkaistaan mutta LinkedIn ei näytä mukautettuja **Työsuhteen tyyppi**- ja **Virkaikätyyppi**-arvoja.

## <a name="changes-in-onboarding"></a>Onboardingin muutokset

### <a name="private-preview-for-onboard-teams"></a>Onboard-ryhmien yksityinen esiversio
Malleja on nyt helppo jakaa ja niitä voi käyttää kätevästi koko organisaatiossa. Lisätietoja on kohdassa [Parhaiden käytäntöjen jakaminen organisaatiossa Onboard-ryhmien avulla](https://docs.microsoft.com/business-applications-release-notes/April19/dynamics365-talent/onboard/share-best-practices-teams).

### <a name="private-preview-for-assignee-placeholders"></a>Vastuuhenkilöiden paikkamerkkien yksityinen esiversio
Voit täydentää malleja määrittämällä tehtäviä rooleille henkilöiden sijaan. Roolit määritetään sitten henkilöille oppaan luonnin yhteydessä. Lisätietoja on kohdassa [Oppaan hallinnan sujuvoittaminen määrittämällä tehtäviä rooleille](https://docs.microsoft.com/business-applications-release-notes/April19/dynamics365-talent/onboard/assign-activities-roles).

## <a name="changes-in-core-hr"></a>Core HR:n muutokset
**Koontiversio 8.1.2178**

### <a name="configure-workflow-to-auto-approve-or-follow-workflow-when-an-hr-or-line-manager-submits-or-updates-time-off-requests"></a>Työnkulun määrittäminen hyväksymään työnkulku automaattisesti tai seuraamaan sitä, kun henkilöstöosasto tai linjaesimies lähettää tai päivittää poissaolopyyntöjä
Lisätyillä uusilla työnkulun ehdoilla lomapyynnöt voidaan hyväksyä automaattisesti, jos lähettäjä on työntekijän esimies tai henkilöstöosasto. Yksi tapa hyväksyä työnkulku automaattisesti on ottaa automaattinen toiminto käyttöön työnkulun hyväksymisessä.

Seuraavat ehdot on lisätty:

- Lähettäjä – käytetään arvioimaan pyynnön työnkulkuun lähettäneen käyttäjän järjestelmän käyttäjätunnus.
- Lähetetty seuraavan puolesta – käytetään arvioimaan, onko lomapyyntö lähetetty pyyntöön liitetyn työntekijän puolesta.
- Henkilöstöosaston lähettämä – käytetään arvioimaan, onko pyynnön työnkulkuun lähettäneellä järjestelmän käyttäjällä henkilöstöhallinnon rooli.
- Lähettäjänä esimies – käytetään arvioimaan, lomapyynnön työnkulkuun lähettänyt käyttäjä pyyntöön liitetyn työntekijän linjahierarkian esimies.

### <a name="enable-employee-fixed-compensation-for-future-position-assignments"></a>Työntekijän kiinteän kompensaation ottaminen käyttöön tulevissa toimimäärityksissä
Organisaatioon liittyvien työntekijöiden aloituspäivämäärä on tyypillisesti tulevaisuudessa. Tämän muutoksen ansiosta voidaan määrittää kiinteä kompensaatio työntekijöille, joiden toimimääritykset ovat tulevaisuudessa.

### <a name="position-payroll-fields-are-blank-when-editing-the-position"></a>Toimen palkanlaskentakentät ovat tyhjiä toimea muokatessa
Tämän muutoksen ansiosta palkanlaskentakenttien arvot palautuvat nyt nykyisiin arvoihin, kun nykyisiin toimiin pyydetään muutoksia.

### <a name="other-miscellaneous-bug-fixes"></a>Muita ohjelmakorjauksia
Tässä julkaisussa on muita vähäisiä ohjelmakorjauksia.

### <a name="upgrade-to-common-data-service"></a>Päivitä versioon Common Data Service
Common Data Service -versioon tapahtuvan päivityksen määräajat lähestyvät nopeasti. Kirjaudu sisään PowerApps-hallintakeskukseen ja tarkista, onko tietokantasi päivitettävä. Lisätietoja määräajoista ja päivityksen vaiheista on kohdassa [Päivittäminen Common Data Service](https://docs.microsoft.com/common-data-service/upgradecds/introduction-upgrade-cds).

## <a name="coming-soon"></a>Tulossa pian

###  <a name="advanced-compensation-security-fixed-and-variable"></a>Kompensaation lisäsuojaus (kiinteä ja muuttuva)
Monissa organisaatioissa etuuspäälliköt voivat käyttää vain tiettyjä kompensaatiotietueita, kuten johtajien tai alueellisten työntekijöiden tietueita. Tämä muutoksen ansiosta voit hallita ja ylläpitää organisaation erilaisten työntekijäryhmien kompensaatiosuunnitelmia. Kiinteille ja muuttuville suunnitelmille voidaan määrittää käyttöoikeusrooleja, jotka määrittävät kyseisten suunnitelmien ja niihin liittyvien työntekijätietojen, kuten palkkatietojen tai bonustietueiden, käyttöoikeuden. Vain roolit, joilla on tietty käyttöoikeus, voivat käsitellä kyseisten työntekijöiden kompensaatiota.

###  <a name="platform-update-24-for-finance-and-operations"></a>Finance and Operationsin käyttöympäristöpäivitys 24
Lisätietoja Finance and Operationsin käyttöympäristöpäivitys 24:stä on kohdassa [Finance and Operations -käyttöympäristöpäivitys 24:n uudet ja muuttuneet ominaisuudet (maaliskuu 2019)](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-24).
