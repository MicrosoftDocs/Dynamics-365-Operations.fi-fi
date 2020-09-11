---
title: Dynamics 365 Human Resourcesin uudet tai muuttuneet ominaisuudet (7. helmikuuta 2020)
description: Tässä artikkelissa käsitellään Microsoft Dynamics 365 Human Resourcesin 7. helmikuuta 2020 julkaistuja uusia tai muuttuneita ominaisuuksia.
author: Darinkramer
manager: AnnBe
ms.date: 02/07/2020
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
ms.search.validFrom: 2020-02-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 8ca740c9b839a08bdb8b426ff191bea64febcd15
ms.sourcegitcommit: 2bcacef1e010c312f019dbf9740ce87d627848a7
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/20/2020
ms.locfileid: "3712083"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-february-7-2020"></a>Dynamics 365 Human Resourcesin uudet tai muuttuneet ominaisuudet (7. helmikuuta 2020)

Tässä artikkelissa käsitellään Dynamics 365 Human Resourcesin uusia tai muuttuneita toimintoja. Muutokset koskevat koontiversion numeroa 8.1.2835. Joissakin otsikoissa suluissa olevat luvut viittaavat tukinumeroihin Microsoft Dynamics Lifecycle Services (LCS) -palveluissa.

## <a name="learning-analytics-doesnt-show-the-course-if-the-classroom-is-blank-388289"></a>Automaattianalyysi ei näytä kurssia, jos luokkahuone on tyhjä (388289)

Automaattianalyysisivulla näkyy nyt kurssi, jos luokkahuone on tyhjä.

## <a name="position-lookup-doesnt-take-the-time-zone-into-account-405344"></a>Paikkahaku ei ota aikavyöhykettä huomioon (405344)

Avointen toimien haku ottaa nyt huomioon aikavyöhykkeen vahvistettaessa, onko toimi avoin.

## <a name="current-balance-analysis-view-doesnt-update-with-the-correct-current-leave-balance-after-submitting-time-off-requests-409756"></a>Nykyisen saldon analyysinäkymä ei päivity, kun oikea tämänhetkinen saldo on määritetty, kun lomapyynnöt on tehty (409756)

Tämänhetkinen saldo sisältää nyt lähetetyt lomapyynnöt.

## <a name="in-preview"></a>Esiversiossa

Seuraavat esikatseluominaisuudet ovat käytettävissä 3. helmikuuta 2020:

- Lisätietoja **Lomien ja poissaolojen esikatseluominaisuuksista** on kohdassa [Lomien ja poissaolojen esikatseluominaisuudet](hr-leave-and-absence-overview.md?leave-and-absence-preview-features).

- **Etujen hallinnan esikatselu** – Lisätietoja esimerkiksi tunnetuista ongelmista on kohdassa [Etujen hallinnan yleiskuvaus](hr-benefits-management-overview.md).

## <a name="coming-soon"></a>Tulossa pian

### <a name="platform-update-32"></a>Ympäristön update 32 -päivitys 

Käyttöympäristön päivitys 32 on pian saatavilla. [Lue lisätietoja käyttöympäristön päivityksestä 32 tästä](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-update-32).

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