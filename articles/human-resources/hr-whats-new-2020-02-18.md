---
title: Dynamics 365 Human Resourcesin uudet tai muuttuneet ominaisuudet (18. helmikuuta 2020)
description: Tässä artikkelissa käsitellään Microsoft Dynamics 365 Human Resourcesin uusia tai muuttuneita toimintoja.
author: Darinkramer
manager: AnnBe
ms.date: 02/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2020-02-18
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 60b46f5bd8f5eeae8aedc9bf81f1e7892caa0c93
ms.sourcegitcommit: bd9ff0d28718d535356ffbe1cffaaf60310dd430
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/13/2020
ms.locfileid: "3555336"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-february-18-2020"></a>Dynamics 365 Human Resourcesin uudet tai muuttuneet ominaisuudet (18. helmikuuta 2020)

Tässä artikkelissa käsitellään Dynamics 365 Human Resourcesin uusia tai muuttuneita toimintoja. Muutokset koskevat koontiversion numeroa 8.1.2903. Joissakin otsikoissa suluissa olevat luvut viittaavat tukinumeroihin LCS-palveluissa.

## <a name="platform-update-32"></a>Ympäristön update 32 -päivitys 

Platform Update 32 on nyt saatavana. Lisätietoja on kohdassa [Finance and Operations -sovellusten Platform update 32:n uudet ja muuttuneet ominaisuudet (helmikuu 2020)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-update-32).

## <a name="search-values-are-remembered-when-changing-view-options-in-streamlined-employee-form-383833"></a>Hakuarvot muistetaan, kun muutat näkymäasetuksia tehostetussa työntekijälomakkeessa (383833)

Uusi **työntekijälomake** muistaa nyt hakuarvot, kun muutat näkymän asetuksia ja otat muutokset käyttöön.

## <a name="compensation-management-summary-tiles-in-preview-feature-redirect-to-wrong-form-401861"></a>Kompensaation hallinnan yhteenvetoruudut esikatselutoiminnon uudelleenohjauksesta väärään muotoon (401861)

Pysyvät ja muuttuvat kompensaation hallinnan ruudut näyttävät nyt oikeat tiedot uudessa **työntekijälomakkeessa**. Koskee vain tehostettua työntekijälomakkeen esikatselutoimintoa. Voit ottaa tämän esikatselutoiminnon käyttöön **ominaisuuksien hallinnassa**. Lisätietoja on ohjeaiheessa [Toimintojen hallinta](hr-admin-manage-features.md).

## <a name="empty-status-field-for-some-leave-request-records-in-common-data-service-414915"></a>Joidenkin lomapyyntötietueiden tyhjä Tila-kenttä Common Data Servicessä (414915)

Tämä muutos korjaa ongelman Common Data Servicessä, kun lomapyynnön **Tila**-kentän arvoksi on määritetty **Tarkistus**. Common Data Service ilmaisee nyt tilan.

## <a name="skill-gap-analysis-only-possible-for-assigned-job-411390"></a>Osaamisalueaukkoanalyysi on mahdollinen vain määritetylle työlle (411390)

Voit tehdä osaamisalueaukkoanalyysin mille tahansa Human Resources -sovelluksen määritetylle työlle.

## <a name="system-currency-doesnt-sync-from-common-data-service-to-human-resources-in-new-environments-418011"></a>Järjestelmän valuuttaa ei synkronoida Common Data Servicestä Human Resources -sovellukseen uusissa ympäristöissä (418011)

Common Data Servicen järjestelmän valuutan voi nyt synkronoida Human Resources -sovellukseen.

## <a name="in-preview"></a>Esiversiossa

- [Lomien ja poissaolojen esikatseluominaisuudet](hr-leave-and-absence-overview.md?leave-and-absence-preview-features)

- [Etujen hallinnan esikatseluominaisuudet](hr-benefits-management-overview.md)

## <a name="coming-soon"></a>Tulossa pian

### <a name="updated-common-data-service-solution"></a>Päivitetty Common Data Service -ratkaisu

Uusi Common Data Service -ratkaisu tulee pian saataville seuraavin muutoksin:

| Kuvaus | Muutos |
| ----------------------------------------- | --- |
| **Työn/toimen** yksikön muutokset | **Kompensaatioalue** lisätty</br>**Taloushallinnon dimensiot** lisätty |
| **Työntekijä**-yksikön muutokset | **Nimien järjestys** lisätty</br>**Työskentelee kotoa** lisätty</br>**Kieliä** lisätty</br>**Ikälisäpäivä** lisätty</br>**Vuosipäivän päivämäärä** lisätty</br>**Alkuperäinen työsuhteen alkamispäivämäärä** lisätty |
| **Työsuhde**-yksikön muutokset | **Taloushallinnon dimensiot** lisätty</br>**Irtisanomisen syy** lisätty</br>**Päättymispäivämäärä** nimettiin uudelleen **Siirtymäpäivästä**</br>**Koeajan päivämäärä** lisätty |
| **Työntekijän osoite**-yksikön muutokset | **Katuosoite** lisätty</br>**Osoiterivi 1**, **Osoiterivi 2**ja **Osoiterivi 3**, jotka on merkitty poistettaviksi |
| Uudet muuttuvat kompensaatioasetusten entiteetit | **Muuttuvan kompensaatiosuunnitelman tyyppi**</br>**Muuttuva kompensaatiosuunnitelma**</br>**Hyvityssäännöt**</br>**Muuttuvan kompensaatiosuunnitelman taso** |
| Uusi **Työntekijäkalenterin työ**-yksikkö | **Työkalenteriyksikkö** lisätty |
| Uusi **Palkanlaskennan toimen tiedot** -yksikkö | **Palkanlaskennan toimen tiedot** lisätty |
| Uusi **Otsikko**-yksikkö | **Otsikko** lisätty. Uusi **Otsikko**-yksikkö sisältyy synkronointiprosessiin Human Resources- ja Common Data Service -sovellusten välillä. Siihen ei aluksi viitata **Työn sijainti**- tai **Työ**-yksiköissä. |

## <a name="see-also"></a>Lisätietoja

[Human Resourcesin uudet ja muuttuneet ominaisuudet](hr-admin-whats-new.md)</br>
[Yhteenveto Dynamics 365 Human Resourcesin vuoden 2019 julkaisuaallosta 2](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Päivitysprosessi](hr-admin-setup-update-process.md)</br>
[Hallitse ominaisuuksia](hr-admin-manage-features.md)