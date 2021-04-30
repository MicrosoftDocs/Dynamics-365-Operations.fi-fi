---
title: Dynamics 365 Human Resourcesin uudet tai muuttuneet ominaisuudet 21.1.2021
description: Tässä ohjeaiheessa käsitellään Microsoft Dynamics 365 Human Resourcesin 21. tammikuuta 2021 julkaistuja uusia tai muuttuneita ominaisuuksia.
author: marcelbf
ms.date: 01/21/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-01-21
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2bf587933aa24e772e6cebca94ee6e8648ec7f10
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/13/2021
ms.locfileid: "5890672"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-january-21-2021"></a>Dynamics 365 Human Resourcesin uudet tai muuttuneet ominaisuudet 21.1.2021

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Tässä ohjeaiheessa käsitellään Dynamics 365 Human Resourcesin uusia, muuttuneita tai pian tulossa olevia ominaisuuksia.

Lisätietoja päivitysprosessista ja aikataulusta on kohdassa [Päivitysprosessi](hr-admin-setup-update-process.md).

Lisätietoja uusista ominaisuuksista ja niiden odotetuista yleisen saatavuuden päivämääristä on kohdassa [Dynamics 365 Human Resourcesin vuoden 2020 2. julkaisuaallon yleiskatsaus](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/).


## <a name="in-this-release"></a>Tässä julkaisussa

Tämä julkaisu sisältää seuraavat uudet ominaisuudet ja ohjelmakorjaukset. Muutokset koskevat koontiversion numeroa 8.1.3866.

### <a name="new-features"></a>Uudet ominaisuudet

Seuraavat ominaisuudet ovat yleisesti saatavana tässä julkaisussa.

| Ominaisuus | Julkaisusuunnitelma | Dokumentaatio |
| --- | --- | --- |
| Platform update 10.0.16(40) | -- | [Finance and Operations -sovellusten version 10.0.16 Platform update -päivitykset (helmikuu 2021)](../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-16.md) |
| Työnkulun parannetut pyynnöt ja hyväksynnät | [Organisaation ja henkilöstöhallinnon työnkulkukokemuksen parannukset](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) | [Toimen Itselle määritetyt työnimikkeet -luettelon määritysasetus](./hr-whats-new-2020-09-03.md#configuration-option-to-position-work-items-assigned-to-me-list-477004) |
| Affordable Care Act (ACA) -säännöstenmukaisuuden päivitykset 1095-C-lomakkeelle, lomakkeelle 1095-B ja sähköiselle raportoinnille vanhassa Edut-työtilassa | -- | -- | 
| Etujen hallinta tukee nyt ACA-yhteensopivuuden raportointia Yhdysvalloissa toimiville yrityksille. | -- | [ACA-raporttien luominen etujen hallinnassa](hr-benefits-management-aca-reports.md) |
| Etujen hallinta on nyt määrittänyt etuprosenttitasot ja etuprosentin kaksoistasot.  | -- | -- |

### <a name="bug-fixes"></a>Ohjelmavirhekorjaukset

Tämä julkaisu sisältää seuraavat ohjelmakorjaukset.

> [!NOTE]
> Tavoitteena on, että nämä tiedot ovat käytettävissä mahdollisimman pian. Tämän ohjeaiheen päivitys saattaa sisältää ohjelmakorjauksia, jotka on otettu käyttöön koontiversiossa tämän ohjeaiheen alkuperäisen julkaisin jälkeen.

| Ongelman numero | Varasto-otto |  kuvaus |
| --- | --- | --- |
| 533079 | Siirtymisvirhe"Lomaketta kutsuttiin väärin", kun vähennyksiä yritetään tarkastella. | Korjattu virhe tarkasteltaessa etuvähennyksiä näkymässä **Alkupäivämäärä**. |
| 543641 | Postinumeroa ei täytetä sähköiseen raportointiin.  | Korjattu sisäinen virhe, jossa postinumero ei näy ACA:n sähköisissä etujen hallinnan raporteissa, kun kattavuuskoodi on M–Q. |
| 542815 | Työntekijän itsepalvelun henkilökohtaisten yhteystietojen näytössä työntekijät voivat tarkastella muiden henkilökohtaisia yhteystietoja. | Korjattu virhe, jossa työntekijän itsepalvelun henkilökohtaisten yhteyshenkilöiden **Muokkaa**-lomake ei rajoita kyselyä niin, että vain yksi henkilökohtainen yhteyshenkilö noudetaan ja jossa käyttäjä voi käyttää pikanäppäimiä muiden ihmisten yhteyshenkilöiden tarkastelemista varten. |
| 536157 | Järjestelmänhallinnassa ei voi avata **Microsoft Dataverse -integrointi** -sivua, koska on kutsuttu funktiota IsVirtualEntityPackageInstalled(). | Ongelma estää **Microsoft Dataverse-integrointi** -sivun lataamisen Human Resourcesissa. |
| 533079 | Siirtymisvirhe"Lomaketta kutsuttiin väärin", kun vähennyksiä yritetään tarkastella. | Korjattu virhe, kun etujen hallinnan **Vähennykset**-lomakkeessa tarkastellaan näkymää **Alkupäivämääränä**. |
| 537264 | Hakijan tietueesta puuttuu **Henkilökohtaiset tiedot** -pikavälilehti. | Hakijan henkilökohtaiset tiedot ovat nyt käytettävissä hakijan tietueessa. |
| 537267 | **Ammattikokemus** ei näy sisäisten hakijoiden tietueissa. | **Ammattikokemus**-pikavälilehti näkyy nyt sisäisten hakijoiden tietueissa. Aiemmin, jos hakija oli sisäinen, **Ammattikokemus** korvattiin **työhistorialla**, joka on hakijan työhistoria organisaatiossa. Molemmat ovat asianmukaisia, ja niiden on oltava näkyvissä sisäisille ehdokkaille. |
| 537067 | **Saa ottaa yhteyttä työnantajaan** ei näy. | **Saa ottaa yhteyttä työnantajaan** -ohjausobjekti on lisätty hakijatietueen **Muokkaa ammattikokemusta** -ruutuun. |
| 525957 | **Hakijan tila** ei päivity sisäisille hakijoille, kun siirto on valmis. | Kun siirto on valmis (**Muuta toimea**- tai **Jatka**-painike valitaan **Siirrä työntekijä uuden toimen tehtävään** -sivulla) hakijatietueen **Tila**-arvoksi pitää tulla **Otettu työhön**. |
| 537051 | Intian rupian ja Turkin liiran valuuttatunnukset eivät synkronoidu oikein Dataverseen. | Intian rupian ja Turkin liiran tunnukset synkronoituvat nyt oikein Dataverseen. |
| 534846 | Työhönottotaulut on otettava käyttöön tietojen hallintaa varten. | Työhönottopyyntöjä ja hakijoita varten luodut uudet taulut ovat nyt käytössä tietojen hallintaa varten. Näin taulukoiden muutosten seuranta on mahdollista ja OData-muutosten seuranta on mahdollista Dataverse-virtuaalitauluissa. |
| 533474 | Korjaa puuttuva viite kohteeseen Microsoft.SqlServer.XEvent.dll. | Microsoft.SqlServer.XEvent.dll-tiedoston kokoonpanon latauspoikkeukset esivät Dataverse-virtuaalitaulujen määritystä joissakin ympäristöissä. |
| 481122 | **Henkilö**-työtila näyttää keskeytyneey toimet. | Käytöstä poistetut toimet näytettiin avoimina toimina **Henkilö**-työtilassa. Käytöstä poistettuja toimia ei enää näytetä. | 
| 541978 | Lisää ensisijainen sähköpostiosoite BaseWorker-yksikköön. | Tämä muutos lisäsi työntekijän ensisijaisen sähköpostiosoitteen HcmWorkerBaseEntity-kohteeseen. |

## <a name="in-preview"></a>Esiversiossa

Seuraavat uudet ominaisuudet ovat esiversioita. Lisätietoja ominaisuuksien ottamisesta käyttöön tai poistamisesta käytöstä on kohdassa [Ominaisuuksien hallinta](hr-admin-manage-features.md).

| Ominaisuus | Julkaisusuunnitelma | Dokumentaatio |
| --- | --- | --- |
| Microsoft Teamsin Human Resources -sovellus | [Työntekijän loma- ja poissaolokokemus Microsoft Teamsissa](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) | [Teamsin Human Resources -sovellus](./hr-admin-teams-leave-app.md)<br>[Lomapyyntöjen hallinta Teamsissa](hr-teams-leave-app.md) |
| LinkedIn Talent Hub -integrointi | [LinkedIn Talent Hub -integrointi](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/integration-linkedin-talent-hub) | [LinkedIn Talent Hub -integrointi](./hr-admin-integration-linkedin.md) |
| Yritystenvälinen näkymä esimiesten lomia varten | [Yritystenvälinen näkymä työntekijöiden lomia varten](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/cross-company-view-employee-leave-managers) | [Loma- ja poissaoloparametrien määrittäminen](./hr-leave-and-absence-parameters.md) |
|Merkityksellisten lomasaldoja koskevien lisätietojen antaminen| [Merkityksellisten lomasaldoja koskevien lisätietojen antaminen](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/provide-additional-insight-into-leave-balances) | [Työntekijän loman hallinta](./hr-leave-and-absence-manage-employee-leave.md) |
| Esimiehet voivat lähettää toimien työhönottopyyntöjä | [Esimiehet voivat lähettää avointen toimien työhönottopyyntöjä](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/manager-submit-request-recruit-open-positions) | [Työhönottopyynnön lisääminen](./hr-personnel-recruit.md#add-a-recruiting-request) |
| Henkilöstöhallinnon parannettu ehdokasprofiili | [Henkilöstöhallinnon parannettu ehdokasprofiili](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/enhanced-candidate-profile-personnel-management) | [Ehdokasprofiilin lisääminen tai muokkaaminen](./hr-personnel-recruit.md#add-or-edit-a-candidate-profile) |
| Yksinkertaisten integrointien käyttöönotto työhönoton palveluntarjoajien kanssa | [Yksinkertaisten integrointien käyttöönotto työhönoton palveluntarjoajien kanssa](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/enable-simplified-integration-recruiting-providers) | [Ehdokkaiden työhönotto](./hr-personnel-recruit.md) |

## <a name="coming-soon"></a>Tulossa pian
| Ominaisuus | Tietoja |
| --- | --- |
| Etujen rekisteröinnin sähköpostivahvistus | Tämä toiminto antaa mahdollisuuden lähettää vahvistussähköposti lähetetään työntekijöille näiden poistuessa etuihin rekisteröitymisen kokemuksesta työntekijän itsepalvelussa. Lisätietoja: [Etujen hallinnan parametrien määrittäminen yritystä kohti](hr-benefits-setup-parameters-per-company.md). |
| Työnkulku voi hyväksyä työntekijöidensä esimiehen syöttämät osaamisalueet automaattisesti. | Tulossa pian. |

Täydellinen luettelo suunnitelluista ominaisuuksista ja niiden aikataulutetuista julkaisuista on kohdassa [Dynamics 365 Human Resourcesin vuoden 2020 2. julkaisuaallon yleiskatsaus](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/).

## <a name="terminology-updates-for-microsoft-dataverse"></a>Microsoft Dataversen terminologiapäivitykset

Marraskuusa 2020 alkaen Common Data Servicen niimeksi on muutettu [Microsoft Dataverse](/powerapps/maker/data-platform/data-platform-intro). Lisätietoja: [virallinen ilmoitus](https://powerapps.microsoft.com/blog/reshape-the-future-of-work-with-microsoft-dataverse-for-teams-now-generally-available/) Power Apps -blogissa. Nimen muutoksen yhteydessä on päivitetty hieman Dataversen termistöä. Esimerkiksi *entiteetti* on nyt *taulukko* ja *kenttä* *sarake*. Lisätietoja on kohdassa [Termistön päivitykset](/powerapps/maker/data-platform/data-platform-intro#terminology-updates).

Tässä versiossa Dataversen ja Dynamics 365 Human Resources -integrointiin liittyvät termit on päivitetty sovelluksen läpi näiden muutosten huomioonottamista varten. Esimerkiksi **Common Data Service -integrointi** -lomake **Microsoft Dataverse -integrointi**.

Lisätietoja Microsoft Dataversen ja Dynamics 365 Human Resourcesin integroinnista on kohdassa [Microsoft Dataverse -integroinnin määritys](./hr-admin-integration-common-data-service.md) ja [Microsoft Dataverse -virtuaalitaulujen määritys](./hr-admin-integration-common-data-service-virtual-entities.md).

## <a name="see-also"></a>Lisätietoja

[Human Resourcesin uudet ja muuttuneet ominaisuudet](hr-admin-whats-new.md)</br>
[Yhteenveto Dynamics 365 Human Resourcesin vuoden 2020 julkaisuaallosta 2](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/)</br>
[Päivitysprosessi](hr-admin-setup-update-process.md)</br>
[Ominaisuuksien hallinta](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]