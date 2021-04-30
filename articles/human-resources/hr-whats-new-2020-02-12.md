---
title: Dynamics 365 Human Resourcesin uudet tai muuttuneet ominaisuudet (12. helmikuuta 2020)
description: Tässä artikkelissa käsitellään Microsoft Dynamics 365 Human Resourcesin 12. helmikuuta 2020 julkaistuja uusia tai muuttuneita ominaisuuksia.
author: andreabichsel
ms.date: 02/07/2020
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
ms.author: jaredha
ms.search.validFrom: 2020-02-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0d5991f23723056d7ee766c00ed0f4ee16ff0f85
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/13/2021
ms.locfileid: "5890931"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-february-12-2020"></a>Dynamics 365 Human Resourcesin uudet tai muuttuneet ominaisuudet (12. helmikuuta 2020)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Tässä artikkelissa käsitellään Dynamics 365 Human Resourcesin uusia tai muuttuneita toimintoja. Muutokset koskevat koontiversion numeroa 8.1.2867. Joissakin otsikoissa suluissa olevat luvut viittaavat tukinumeroihin Microsoft Dynamics Lifecycle Services (LCS) -palveluissa.

## <a name="existing-entities-compfixedempls-and-hcmpersonimage-should-be-accessible-from-odata-414178"></a>Aiemmin luotuja yksiköitä CompFixedEmpls ja HcmPersonImage tulee voida käyttää ODatan avulla (414178)

Tämän viikon julkaisussa **CompFixedEmpls**- ja **HcmPersonImage**-yksiköt ovat nyt julkisia ja käytettävissä ODAta:n kautta.

## <a name="delete-employment-from-dataverse-doesnt-work-when-employment-details-arent-active-403193"></a>Työsuhteen poistaminen Dataversestä ei toimi, jos työsuhteen tiedot eivät ole aktiivisia (403193)

Tämä muutos mahdollistaa nyt työsuhteen poistamisen Dataversen kautta, kun aktiivisia työsuhteen tietoja ei ole.

## <a name="course-registration-workflow-changes-status-to-complete-and-errors-after-second-approval-409749"></a>Kurssin rekisteröinnin työnkulku muuttaa tilaksi Valmis ja päättyy virheeseen sekunnin kuluttua hyväksynnästä (409749)

Kurssin rekisteröitymisen työnkua on päivitetty niin, että se sallii useat hyväksyjät.

## <a name="in-preview"></a>Esiversiossa

Seuraavat esikatseluominaisuudet ovat käytettävissä 3. helmikuuta 2020:

- Lisätietoja **Lomien ja poissaolojen esikatseluominaisuuksista** on kohdassa [Lomien ja poissaolojen esikatseluominaisuudet](hr-leave-and-absence-overview.md?leave-and-absence-preview-features).

- **Etujen hallinnan esikatselu** – Lisätietoja, kuten tunnettuja ongelmia, on kohdassa [Etujen hallinnan yleiskuvaus](hr-benefits-management-overview.md).

## <a name="coming-soon"></a>Tulossa pian

### <a name="platform-update-32"></a>Ympäristön update 32 -päivitys 

Käyttöympäristön päivitys 32 on pian saatavilla. [Lue lisätietoja käyttöympäristön päivityksestä 32 tästä](../fin-ops-core/dev-itpro/get-started/whats-new-platform-update-32.md).

### <a name="updated-dataverse-solution"></a>Päivitetty Dataverse -ratkaisu

Uusi Dataverse -ratkaisu tulee pian saataville seuraavin muutoksin:

| Kuvaus | Muutos |
| ----------------------------------------- | --- |
| **Työn/toimen** yksikön muutokset | **Kompensaatioalue** lisätty</br>**Taloushallinnon dimensiot** lisätty |
| **Työntekijä**-yksikön muutokset | **Nimien järjestys** lisätty</br>**Työskentelee kotoa** lisätty</br>**Kieliä** lisätty</br>**Ikälisäpäivä** lisätty</br>**Vuosipäivän päivämäärä** lisätty</br>**Alkuperäinen työsuhteen alkamispäivämäärä** lisätty |
| **Työsuhde**-yksikön muutokset | **Taloushallinnon dimensiot** lisätty</br>**Irtisanomisen syy** lisätty</br>**Päättymispäivämäärä** nimettiin uudelleen **Siirtymäpäivästä**</br>**Koeajan päivämäärä** lisätty |
| **Työntekijän osoite**-yksikön muutokset | **Katuosoite** lisätty</br>**Osoiterivi 1**, **Osoiterivi 2** ja **Osoiterivi 3**, jotka on merkitty poistettaviksi |
| Uudet muuttuvat kompensaatioasetusten entiteetit | **Muuttuvan kompensaatiosuunnitelman tyyppi**</br>**Muuttuva kompensaatiosuunnitelma**</br>**Hyvityssäännöt**</br>**Muuttuvan kompensaatiosuunnitelman taso** |
| Uusi **Työntekijäkalenterin työ**-yksikkö | **Työkalenteriyksikkö** lisätty |
| Uusi **Palkanlaskennan toimen tiedot** -yksikkö | **Palkanlaskennan toimen tiedot** lisätty |
| Uusi **Otsikko**-yksikkö | **Otsikko** lisätty. Uusi **Otsikko**-yksikkö sisältyy synkronointiprosessiin Human Resources- ja Dataverse -sovellusten välillä. Siihen ei aluksi viitata **Työn sijainti**- tai **Työ**-yksiköissä. |

## <a name="see-also"></a>Lisätietoja

[Human Resourcesin uudet ja muuttuneet ominaisuudet](hr-admin-whats-new.md)</br>
[Yhteenveto Dynamics 365 Human Resourcesin vuoden 2019 julkaisuaallosta 2](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Päivitysprosessi](hr-admin-setup-update-process.md)</br>
[Hallitse ominaisuuksia](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]