---
title: Dynamics 365 Human Resourcesin uudet tai muuttuneet ominaisuudet 2. joulukuuta 2020
description: Tässä ohjeaiheessa käsitellään Microsoft Dynamics 365 Human Resourcesin 2. joulukuuta 2020 julkaistuja uusia tai muuttuneita ominaisuuksia.
author: marcelbf
manager: tfehr
ms.date: 12/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2020-12-02
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: aba35563266d1149131124f489f89da61432bfb2
ms.sourcegitcommit: 0354ca7e566fbd2eb0aabdd40000d4ac5c44ea78
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/04/2020
ms.locfileid: "4669164"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-december-2-2020"></a>Dynamics 365 Human Resourcesin uudet tai muuttuneet ominaisuudet 2. joulukuuta 2020

Tässä ohjeaiheessa käsitellään Dynamics 365 Human Resourcesin uusia, muuttuneita tai pian tulossa olevia ominaisuuksia.

Lisätietoja päivitysprosessista ja aikataulusta on kohdassa [Päivitysprosessi](hr-admin-setup-update-process.md).

Lisätietoja uusista ominaisuuksista ja niiden odotetuista yleisen saatavuuden päivämääristä on kohdassa [Dynamics 365 Human Resourcesin vuoden 2020 2. julkaisuaallon yleiskatsaus](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>Tässä julkaisussa

Tämä julkaisu sisältää seuraavat uudet ominaisuudet ja ohjelmakorjaukset. Muutokset koskevat koontiversion numeroa 8.1.3788.

### <a name="new-features"></a>Uudet ominaisuudet

Seuraavat ominaisuudet ovat yleisesti saatavana tässä julkaisussa.

| Ominaisuus | Julkaisusuunnitelma | Dokumentaatio |
| --- | --- | --- |
| Esimiehet voivat lähettää toimien työhönottopyyntöjä | [Esimiehet voivat lähettää avointen toimien työhönottopyyntöjä](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/manager-submit-request-recruit-open-positions) | [Työhönottopyynnön lisääminen](https://docs.microsoft.com/dynamics365/human-resources/hr-personnel-recruit#add-a-recruiting-request) |
| Henkilöstöhallinnon parannettu ehdokasprofiili | [Henkilöstöhallinnon parannettu ehdokasprofiili](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/enhanced-candidate-profile-personnel-management) | [Ehdokasprofiilin lisääminen tai muokkaaminen](https://docs.microsoft.com/dynamics365/human-resources/hr-personnel-recruit#add-or-edit-a-candidate-profile) |
| Yksinkertaisten integrointien käyttöönotto työhönoton palveluntarjoajien kanssa | [Yksinkertaisten integrointien käyttöönotto työhönoton palveluntarjoajien kanssa](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/enable-simplified-integration-recruiting-providers) | [Ehdokkaiden työhönotto](https://docs.microsoft.com/dynamics365/human-resources/hr-personnel-recruit) |
| Mukautetut linkit esimiehen itsepalvelussa | [Mukautetut linkit esimiehen itsepalvelussa](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/custom-links-manager-self-service) | [Mukautetut linkit esimiehen itsepalvelussa](https://aka.ms/MSSCustomLinks) |


### <a name="bug-fixes"></a>Ohjelmavirhekorjaukset

Tämä julkaisu sisältää seuraavat ohjelmakorjaukset.

> [!NOTE]
> Tavoitteena on, että nämä tiedot ovat käytettävissä mahdollisimman pian. Tämän ohjeaiheen päivitys saattaa sisältää ohjelmakorjauksia, jotka on otettu käyttöön koontiversiossa tämän ohjeaiheen alkuperäisen julkaisin jälkeen.

| Ongelman numero | Varasto-otto | kuvaus |
| --- | --- | --- |
| 514087 | BenefitEligibilityProcessResult-kohdassa tulee olla päivämäärä ja aika, joita käytettiin käsittelyssä. | BenefitEligibity-kohdan käsittelytuloksessa on nyt edellisen käsittelyn datetimestamp. Aiemmin tämä puuttui. |
| 526903 | Edun rekisteröiminen epäonnistuu huollettavia sisältävissä suunnitelmissa, jos **Valitse edustajat automaattisesti** -kohta on otettu käyttöön **Henkilöstöhallinnon jaetut parametrit** -kohdassa. | Ratkaistiin ongelma, jossa huollettavien edun rekisteröiminen epäonnistui, kun **Valitse edustajan automaattisesti** -vaihtoehto on otettu käyttöön oletusedustajille. |
| 521922 | **Näytä poissaolo ilman tietoja** -parametri näyttää poissaolopyyntöjen tiedot ryhmän poissaolokalenterissa. | Lomatyyppi, lomatyypin väri ja päivän tiedot näytettiin ryhmän poissaolokalenterissa, kun **Näytä poissaolo ilman tietoja** -kohdan arvoksi oli määritetty **Kyllä** **Loman ja poissaolon parametrit**. Tämä on korjattu, ja nyt lomatyyppiä ei näytetä ja oletuslomatyypin väriä (tummansininen) käytetään kaikkien ryhmän poissaolokalenterin lomatyyppien yhteydessä. |
| 527316 | Työn, toimen ja työntekijän ilmoitusten otsikkomuutoksia ei synkronoida. | Otsikon suhde lisättiin aiemmin työn, toimen ja työntekijän entiteetteihin. Tämän suhteen synkronointi Human Resourcesista Common Data Serviceen synkronoinnissa toimii. Se ei kuitenkaan toimimnut Common Data Servicen ilmoituksissa. Tämä ongelma on korjattu. |
| 512275 | Poista **Loma- ja poissaoloparametrit** -kohdan värivaihtoehdot. | Nyt kun värit on määritetty lomatyypissä, värivaihtoehtoja ei enää tarvita **loma- ja poissaoloparametreissa**. Tämän vuoksi ne on poistettu. |
| 437112 | Harhaanjohtava virhesanoman teksti työntekijän toimen määrityksen aikana. | Päivitetty virhesanoma, kun työntekijä otetaan töihin ja kun hänet yritetään määrittää passiiviseen toimeen. Päivitetty sanoma **Määritetty toimi ei ole aktiivinen työsuhteen alkamispäivänä. Tarkista tämän toimen kesto.** |
| 527816 | Suorituskykyyn liittyviä ongelmia **Poissaolo**-sivulla. | Suorituskykyä on parannettu **Poissaolo**-sivulla. |
| 523158 | BenefitPeriodMigrationUpgrade ja BenefitPlanMigrationUpgrade eivät toimi. | **Kausi**- ja **Suunnitelma**-kohtiin liittyvien edun siirtotöiden ongelmat on korjattu. |

## <a name="in-preview"></a>Esiversiossa

Seuraavat uudet ominaisuudet ovat esiversioita. Lisätietoja ominaisuuksien ottamisesta käyttöön tai poistamisesta käytöstä on kohdassa [Ominaisuuksien hallinta](hr-admin-manage-features.md).

| Ominaisuus | Julkaisusuunnitelma | Dokumentaatio |
| --- | --- | --- |
| Microsoft Teamsin Human Resources -sovellus | [Työntekijän loma- ja poissaolokokemus Microsoft Teamsissa](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) | [Teamsin Human Resources -sovellus](https://go.microsoft.com/fwlink/?linkid=2127841)<br>[Lomapyyntöjen hallinta Teamsissa](hr-teams-leave-app.md) |
| Työnkulun parannetut pyynnöt ja hyväksynnät | [Organisaation ja henkilöstöhallinnon työnkulkukokemuksen parannukset](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) | [Toimen Itselle määritetyt työnimikkeet -luettelon määritysasetus](https://docs.microsoft.com/dynamics365/human-resources/hr-whats-new-2020-09-03#configuration-option-to-position-work-items-assigned-to-me-list-477004) |
| LinkedIn Talent Hub -integrointi | [LinkedIn Talent Hub -integrointi](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/integration-linkedin-talent-hub) | [LinkedIn Talent Hub -integrointi](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-integration-linkedin) |
|Yritystenvälinen näkymä esimiesten lomia varten | [Yritystenvälinen näkymä työntekijöiden lomia varten](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/cross-company-view-employee-leave-managers) | [Loma- ja poissaoloparametrien määrittäminen](https://docs.microsoft.com/dynamics365/human-resources/hr-leave-and-absence-parameters) |
|Merkityksellisten lomasaldoja koskevien lisätietojen antaminen| [Merkityksellisten lomasaldoja koskevien lisätietojen antaminen](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/provide-additional-insight-into-leave-balances) | [Työntekijän loman hallinta](https://docs.microsoft.com/dynamics365/human-resources/hr-leave-and-absence-manage-employee-leave) |
| Esimiehet voivat lähettää toimien työhönottopyyntöjä | [Esimiehet voivat lähettää avointen toimien työhönottopyyntöjä](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/manager-submit-request-recruit-open-positions) | [Työhönottopyynnön lisääminen](https://docs.microsoft.com/dynamics365/human-resources/hr-personnel-recruit#add-a-recruiting-request) |
| Henkilöstöhallinnon parannettu ehdokasprofiili | [Henkilöstöhallinnon parannettu ehdokasprofiili](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/enhanced-candidate-profile-personnel-management) | [Ehdokasprofiilin lisääminen tai muokkaaminen](https://docs.microsoft.com/dynamics365/human-resources/hr-personnel-recruit#add-or-edit-a-candidate-profile) |
| Yksinkertaisten integrointien käyttöönotto työhönoton palveluntarjoajien kanssa | [Yksinkertaisten integrointien käyttöönotto työhönoton palveluntarjoajien kanssa](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/enable-simplified-integration-recruiting-providers) | [Ehdokkaiden työhönotto](https://docs.microsoft.com/dynamics365/human-resources/hr-personnel-recruit) |

## <a name="coming-soon"></a>Tulossa pian

Täydellinen luettelo suunnitelluista ominaisuuksista ja niiden aikataulutetuista julkaisuista on kohdassa [Dynamics 365 Human Resourcesin vuoden 2020 2. julkaisuaallon yleiskatsaus](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/).

## <a name="see-also"></a>Lisätietoja

[Human Resourcesin uudet ja muuttuneet ominaisuudet](hr-admin-whats-new.md)</br>
[Yhteenveto Dynamics 365 Human Resourcesin vuoden 2020 julkaisuaallosta 2](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/)</br>
[Päivitysprosessi](hr-admin-setup-update-process.md)</br>
[Ominaisuuksien hallinta](hr-admin-manage-features.md)