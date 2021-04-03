---
title: Dynamics 365 Human Resources:n uudet tai muuttuneet ominaisuudet 26. syyskuuta 2020
description: Tässä ohjeaiheessa käsitellään Microsoft Dynamics 365 Human Resourcesin 26. syyskuuta 2020 julkaistuja uusia tai muuttuneita ominaisuuksia.
author: jcart1106
manager: tfehr
ms.date: 09/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f56371519f0f0fcd6e90c8bc107dd8b1326132b4
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/17/2021
ms.locfileid: "5466998"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-september-26-2020"></a>Dynamics 365 Human Resources:n uudet tai muuttuneet ominaisuudet 26. syyskuuta 2020

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Tässä ohjeaiheessa käsitellään Dynamics 365 Human Resourcesin uusia, muuttuneita tai pian tulossa olevia ominaisuuksia. Lisätietoja päivitysprosessista ja aikataulusta on kohdassa [Päivitysprosessi](hr-admin-setup-update-process.md).

Lisätietoja uusista ominaisuuksista ja niiden odotetuista yleisen saatavuuden päivämääristä on kohdassa [Dynamics 365 Human Resourcesin vuoden 2020 2. julkaisuaallon yleiskatsaus](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>Tässä julkaisussa

Tämä julkaisu sisältää seuraavat uudet ominaisuudet ja ohjelmakorjaukset. Muutokset koskevat koontiversion numeroa 8.1.3589-hf.3.

### <a name="new-features"></a>Uudet ominaisuudet

Seuraava ominaisuus on yleisesti saatavana tässä julkaisussa:

- **Platform update 10.0.13 on nyt saatavana**: lisätietoja päivityksestä on kohdassa [Finance and Operations -sovellusten version 10.0.13 Platform update -päivitykset (lokakuu 2020)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-13).

### <a name="bug-fixes"></a>Ohjelmavirhekorjaukset

Tämä julkaisu sisältää seuraavat ohjelmakorjaukset.

> [!NOTE]
> Tavoitteena on, että nämä tiedot ovat käytettävissä mahdollisimman pian. Tämän ohjeaiheen päivitykset saattavat sisältää ohjelmakorjauksia, jotka on otettu käyttöön koontiversiossa tämän ohjeaiheen alkuperäisen julkaisin jälkeen.

| Ongelman numero | Varasto-otto | kuvaus |
| --- | --- | --- |
| 469495 | Taloushallinnon oletusruudukon ja valintaikkunan päivittäminen | Taloushallinnon dimension oletusruudukko ja valintaikkuna päivitetään Human Resourcesissa. |
| 474887 | Lomapyynnön työnimike avaa väärän linkin manuaalisessa päätöksessä | Jos työnkulkumääritys sisältää manuaalisen päätöksen, siirtyminen lomapyyntöön **Minulle määritetyt työnimikkeet** -kohdasta avaa väärän linkin, jolloin avautuu joko tyhjä lomake tai nykyisen käyttäjän luoma lomapyyntö eikä manuaalista päätöstä varten määritetty pyyntö. |
| 474962 | Loma- ja poissaoloparametrien entiteetissä on kenttiä, jossa on moniselitteisiä selitteinä | Loma- ja poissaoloparametrien entiteetin selitteet on päivitetty entistä selkeämmiksi. |
| 481401 | Jaksotuksen käsittely jumiutuu, kun jaksotuksen päivämääräperuste on jaksotuksen alkamispäivän jälkeen kuun lopussa. | Jaksotuksen käsittely on päivitetty siten, että siinä ei ole viivettä, kun jaksotuksen päivämääräperuste on jaksotuksen alkamispäivän jälkeen kuun lopussa |
| 447167 | Vanhentuvien tietueiden luettelossa on ei-aktiivisia työntekijöitä | **Henkilöstöhallinto**-kohdan **Vanhentuvat tietueet** -välilehti sisälsi ei-aktiivisia työntekijöitä. Nyt se sisältää vain aktiiviset työntekijät. |
| 486840 | **Minulle määritetyt työnimikkeet** -kohdasta avautuu väärä poissaolopyyntö. | Poissaolopyynnön valitseminen **Minulle määritetyt työnimikkeet** -kohdassa ei enää avaa uusinta nykyiselle käyttäjälle määritettyä poissaolopyyntöä. |
| 506868 | Dataversen **Otsikko**-kenttä ei ole määritetty **Tehtävänimike**-entiteetille | **Työ**- ja **Tehtävänimike**-entiteettien **Otsikko**-kenttä näkyi määrittämättömänä. **Otsikko**-kenttä näkyy nyt. |
| 430359 | Käytöstäpoiston tarkistusluettelon tehtäviä ei voi käyttää määritetyillä esimiehen ja työntekijän rooleilla | Työntekijät, joiden työsuhteen päättymispäivä on tulevaisuudessa, eivät voineet käyttää tarkistusluettelon tehtäviä, jos heillä oli vain työntekijän tai esimiehen rooli. Nyt käyttäjät, joilla on vain työntekijän tai esimiehen rooli, voivat käyttää käytöstäpoistotehtäviä, joiden työsuhteen päättymispäivä on tulevaisuudessa. |
| 458102 | Uusi työntekijä ei näy luotaessa **Työntekijän palkanlaskentatiedot** -entiteetissä. | Uudet työntekijät sisältyvät työntekijän palkanlaskenta tietojen entiteettiin ilman, että työntekijän palkanlaskentatiedot olisi avattava ennen entiteetin vientiä. |

## <a name="in-preview"></a>Esiversiossa

Seuraavat uudet ominaisuudet ovat esiversioita. Lisätietoja ominaisuuksien ottamisesta käyttöön tai poistamisesta käytöstä on kohdassa [Ominaisuuksien hallinta](hr-admin-manage-features.md).

| Ominaisuus | Julkaisusuunnitelma | Dokumentaatio |
| --- | --- | --- |
| Microsoft Teamsin Human Resources -sovellus | [Työntekijän loma- ja poissaolokokemus Microsoft Teamsissa](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) | [Teamsin Human Resources -sovellus](https://go.microsoft.com/fwlink/?linkid=2127841)<br>[Lomapyyntöjen hallinta Teamsissa](hr-teams-leave-app.md) |
| Työnkulun parannetut pyynnöt ja hyväksynnät | [Organisaation ja henkilöstöhallinnon työnkulkukokemuksen parannukset](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) | [Toimen Itselle määritetyt työnimikkeet -luettelon määritysasetus](https://docs.microsoft.com/dynamics365/human-resources/hr-whats-new-2020-09-03#configuration-option-to-position-work-items-assigned-to-me-list-477004) |

## <a name="coming-soon"></a>Tulossa pian

Seuraava uusi ominaisuus on aikataulutettu tulevaan julkaisuun:

- [Mukautetut linkit esimiehen itsepalvelussa](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/custom-links-manager-self-service)

Täydellinen luettelo suunnitelluista ominaisuuksista ja niiden aikataulutetuista julkaisuista on kohdassa [Dynamics 365 Human Resourcesin vuoden 2019 2. julkaisuaallon yleiskatsaus](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/).

## <a name="additional-resources"></a>Lisäresurssit

[Human Resourcesin uudet ja muuttuneet ominaisuudet](hr-admin-whats-new.md)
[Dynamics 365 Human Resourcesin vuoden 2020 2. julkaisuaallon yleiskatsaus](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/)
[Päivitysprosessi](hr-admin-setup-update-process.md)
[Ominaisuuksien hallinta](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]