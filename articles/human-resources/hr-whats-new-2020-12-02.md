---
title: Dynamics 365 Human Resourcesin uudet tai muuttuneet ominaisuudet 2. joulukuuta 2020
description: Tässä ohjeaiheessa käsitellään Microsoft Dynamics 365 Human Resourcesin 2. joulukuuta 2020 julkaistuja uusia tai muuttuneita ominaisuuksia.
author: marcelbf
ms.date: 12/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2020-12-02
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6e02586ad3e6b4428f2ba826851db6ebc3172bdf1760b483032f5159e7864a81
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6782656"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-december-2-2020"></a>Dynamics 365 Human Resourcesin uudet tai muuttuneet ominaisuudet 2. joulukuuta 2020

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Tässä ohjeaiheessa käsitellään Dynamics 365 Human Resourcesin uusia, muuttuneita tai pian tulossa olevia ominaisuuksia.

Lisätietoja päivitysprosessista ja aikataulusta on kohdassa [Päivitysprosessi](hr-admin-setup-update-process.md).

Lisätietoja uusista ominaisuuksista ja niiden odotetuista yleisen saatavuuden päivämääristä on kohdassa [Dynamics 365 Human Resourcesin vuoden 2020 2. julkaisuaallon yleiskatsaus](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>Tässä julkaisussa

Tämä julkaisu sisältää seuraavat uudet ominaisuudet ja ohjelmakorjaukset. Muutokset koskevat koontiversion numeroa 8.1.3788.

### <a name="new-features"></a>Uudet ominaisuudet

Seuraavat ominaisuudet ovat yleisesti saatavana tässä julkaisussa.

| Ominaisuus | Julkaisusuunnitelma | Dokumentaatio |
| --- | --- | --- |
| Esimiehet voivat lähettää toimien työhönottopyyntöjä | [Esimiehet voivat lähettää avointen toimien työhönottopyyntöjä](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/manager-submit-request-recruit-open-positions) | [Työhönottopyynnön lisääminen](./hr-personnel-recruit.md#add-a-recruiting-request) |
| Henkilöstöhallinnon parannettu ehdokasprofiili | [Henkilöstöhallinnon parannettu ehdokasprofiili](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/enhanced-candidate-profile-personnel-management) | [Ehdokasprofiilin lisääminen tai muokkaaminen](./hr-personnel-recruit.md#add-or-edit-a-candidate-profile) |
| Yksinkertaisten integrointien käyttöönotto työhönoton palveluntarjoajien kanssa | [Yksinkertaisten integrointien käyttöönotto työhönoton palveluntarjoajien kanssa](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/enable-simplified-integration-recruiting-providers) | [Ehdokkaiden työhönotto](./hr-personnel-recruit.md) |
| Mukautetut linkit esimiehen itsepalvelussa | [Mukautetut linkit esimiehen itsepalvelussa](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/custom-links-manager-self-service) | [Mukautetut linkit esimiehen itsepalvelussa](./hr-employee-manager-self-service-custom-links.md) |


### <a name="bug-fixes"></a>Ohjelmavirhekorjaukset

Tämä julkaisu sisältää seuraavat ohjelmakorjaukset.

> [!NOTE]
> Tavoitteena on, että nämä tiedot ovat käytettävissä mahdollisimman pian. Tämän ohjeaiheen päivitys saattaa sisältää ohjelmakorjauksia, jotka on otettu käyttöön koontiversiossa tämän ohjeaiheen alkuperäisen julkaisin jälkeen.

| Ongelman numero | Varasto-otto | kuvaus |
| --- | --- | --- |
| 514087 | BenefitEligibilityProcessResult-kohdassa tulee olla päivämäärä ja aika, joita käytettiin käsittelyssä. | BenefitEligibity-kohdan käsittelytuloksessa on nyt edellisen käsittelyn datetimestamp. Aiemmin tämä puuttui. |
| 526903 | Edun rekisteröiminen epäonnistuu huollettavia sisältävissä suunnitelmissa, jos **Valitse edustajat automaattisesti** -kohta on otettu käyttöön **Henkilöstöhallinnon jaetut parametrit** -kohdassa. | Ratkaistiin ongelma, jossa huollettavien edun rekisteröiminen epäonnistui, kun **Valitse edustajan automaattisesti** -vaihtoehto on otettu käyttöön oletusedustajille. |
| 521922 | **Näytä poissaolo ilman tietoja** -parametri näyttää poissaolopyyntöjen tiedot ryhmän poissaolokalenterissa. | Lomatyyppi, lomatyypin väri ja päivän tiedot näytettiin ryhmän poissaolokalenterissa, kun **Näytä poissaolo ilman tietoja** -kohdan arvoksi oli määritetty **Kyllä** **Loman ja poissaolon parametrit**. Tämä on korjattu, ja nyt lomatyyppiä ei näytetä ja oletuslomatyypin väriä (tummansininen) käytetään kaikkien ryhmän poissaolokalenterin lomatyyppien yhteydessä. |
| 527316 | Työn, toimen ja työntekijän ilmoitusten otsikkomuutoksia ei synkronoida. | Otsikon suhde lisättiin aiemmin työn, toimen ja työntekijän entiteetteihin. Tämän suhteen synkronointi Human Resourcesista Dataverseen synkronoinnissa toimii. Se ei kuitenkaan toimimnut Dataversen ilmoituksissa. Tämä ongelma on korjattu. |
| 512275 | Poista **Loma- ja poissaoloparametrit** -kohdan värivaihtoehdot. | Nyt kun värit on määritetty lomatyypissä, värivaihtoehtoja ei enää tarvita **loma- ja poissaoloparametreissa**. Tämän vuoksi ne on poistettu. |
| 437112 | Harhaanjohtava virhesanoman teksti työntekijän toimen määrityksen aikana. | Päivitetty virhesanoma, kun työntekijä otetaan töihin ja kun hänet yritetään määrittää passiiviseen toimeen. Päivitetty sanoma **Määritetty toimi ei ole aktiivinen työsuhteen alkamispäivänä. Tarkista tämän toimen kesto.** |
| 527816 | Suorituskykyyn liittyviä ongelmia **Poissaolo**-sivulla. | Suorituskykyä on parannettu **Poissaolo**-sivulla. |
| 523158 | BenefitPeriodMigrationUpgrade ja BenefitPlanMigrationUpgrade eivät toimi. | **Kausi**- ja **Suunnitelma**-kohtiin liittyvien edun siirtotöiden ongelmat on korjattu. |

## <a name="in-preview"></a>Esiversiossa

Seuraavat uudet ominaisuudet ovat esiversioita. Lisätietoja ominaisuuksien ottamisesta käyttöön tai poistamisesta käytöstä on kohdassa [Ominaisuuksien hallinta](hr-admin-manage-features.md).

| Ominaisuus | Julkaisusuunnitelma | Dokumentaatio |
| --- | --- | --- |
| Microsoft Teamsin Human Resources -sovellus | [Työntekijän loma- ja poissaolokokemus Microsoft Teamsissa](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) | [Teamsin Human Resources -sovellus](./hr-admin-teams-leave-app.md)<br>[Lomapyyntöjen hallinta Teamsissa](hr-teams-leave-app.md) |
| Työnkulun parannetut pyynnöt ja hyväksynnät | [Organisaation ja henkilöstöhallinnon työnkulkukokemuksen parannukset](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) | [Toimen Itselle määritetyt työnimikkeet -luettelon määritysasetus](./hr-whats-new-2020-09-03.md#configuration-option-to-position-work-items-assigned-to-me-list-477004) |
| LinkedIn Talent Hub -integrointi | [LinkedIn Talent Hub -integrointi](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/integration-linkedin-talent-hub) | [LinkedIn Talent Hub -integrointi](./hr-admin-integration-linkedin.md) |
|Yritystenvälinen näkymä esimiesten lomia varten | [Yritystenvälinen näkymä työntekijöiden lomia varten](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/cross-company-view-employee-leave-managers) | [Loma- ja poissaoloparametrien määrittäminen](./hr-leave-and-absence-parameters.md) |
|Merkityksellisten lomasaldoja koskevien lisätietojen antaminen| [Merkityksellisten lomasaldoja koskevien lisätietojen antaminen](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/provide-additional-insight-into-leave-balances) | [Työntekijän loman hallinta](./hr-leave-and-absence-manage-employee-leave.md) |
| Esimiehet voivat lähettää toimien työhönottopyyntöjä | [Esimiehet voivat lähettää avointen toimien työhönottopyyntöjä](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/manager-submit-request-recruit-open-positions) | [Työhönottopyynnön lisääminen](./hr-personnel-recruit.md#add-a-recruiting-request) |
| Henkilöstöhallinnon parannettu ehdokasprofiili | [Henkilöstöhallinnon parannettu ehdokasprofiili](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/enhanced-candidate-profile-personnel-management) | [Ehdokasprofiilin lisääminen tai muokkaaminen](./hr-personnel-recruit.md#add-or-edit-a-candidate-profile) |
| Yksinkertaisten integrointien käyttöönotto työhönoton palveluntarjoajien kanssa | [Yksinkertaisten integrointien käyttöönotto työhönoton palveluntarjoajien kanssa](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/enable-simplified-integration-recruiting-providers) | [Ehdokkaiden työhönotto](./hr-personnel-recruit.md) |

## <a name="coming-soon"></a>Tulossa pian

Täydellinen luettelo suunnitelluista ominaisuuksista ja niiden aikataulutetuista julkaisuista on kohdassa [Dynamics 365 Human Resourcesin vuoden 2020 2. julkaisuaallon yleiskatsaus](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/).

## <a name="see-also"></a>Lisätietoja

[Human Resourcesin uudet ja muuttuneet ominaisuudet](hr-admin-whats-new.md)</br>
[Yhteenveto Dynamics 365 Human Resourcesin vuoden 2020 julkaisuaallosta 2](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/)</br>
[Päivitysprosessi](hr-admin-setup-update-process.md)</br>
[Ominaisuuksien hallinta](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]