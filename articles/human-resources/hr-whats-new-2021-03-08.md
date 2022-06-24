---
title: Dynamics 365 Human Resourcesin uudet tai muuttuneet ominaisuudet (8. maaliskuuta 2021)
description: Tässä artikkelissa käsitellään Microsoft Dynamics 365 Human Resourcesin 8. maaliskuuta 2021 julkaistuja uusia tai muuttuneita ominaisuuksia.
author: marcelbf
ms.date: 03/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-03-08
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 9280e85f9701573717c4115b4d752ed11be4862e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8868051"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-march-08-2021"></a>Dynamics 365 Human Resourcesin uudet tai muuttuneet ominaisuudet (8. maaliskuuta 2021)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Tässä artikkelissa käsitellään Dynamics 365 Human Resourcesin uusia, muuttuneita tai tulevia toimintoja.

Lisätietoja päivitysprosessista ja aikataulusta on kohdassa [Päivitysprosessi](hr-admin-setup-update-process.md).

Lisätietoja uusista ominaisuuksista ja niiden odotetuista yleisen saatavuuden päivämääristä on kohdassa [Dynamics 365 Human Resourcesin vuoden 2021 1. julkaisuaallon yleiskatsaus](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>Tässä julkaisussa

Tämä julkaisu sisältää seuraavat uudet ominaisuudet ja ohjelmakorjaukset. Muutokset koskevat koontiversion numeroa 8.1.4017.

### <a name="new-features"></a>Uudet ominaisuudet

Seuraavat ominaisuudet ovat yleisesti saatavana tässä julkaisussa.

| Ominaisuus | Julkaisusuunnitelma | Dokumentaatio |
| --- | --- | --- |
| Yritystenvälinen näkymä esimiesten lomia varten | [Yritystenvälinen näkymä työntekijöiden lomia varten](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/cross-company-view-employee-leave-managers) | [Loma- ja poissaoloparametrien määrittäminen](./hr-leave-and-absence-parameters.md) |

### <a name="bug-fixes"></a>Ohjelmavirhekorjaukset

Tämä julkaisu sisältää seuraavat ohjelmakorjaukset.

> [!NOTE]
> Tavoitteena on, että nämä tiedot ovat käytettävissä mahdollisimman pian. Tämän artikkelin päivitys saattaa sisältää ohjelmakorjauksia, jotka on otettu käyttöön koontiversiossa tämän artikkelin alkuperäisen julkaisun jälkeen.

| Ongelman numero | Ongelma |  Kuvaus |
| --- | --- | --- |
| 486611 | Virkavapaata ei näytetä lomakalenterissa, kun **Poista lomat käytöstä kaikista kalentereista** -vaihtoehto on käytössä | Jos **Poista lomat käytöstä kaikista kalentereista** -vaihtoehto on käytössä, lomatietoja ei enää näytetä, kun Loma- ja poissaolokalenterin parannukset -ominaisuus otetaan käyttöön.|
| 508972 | Loma- ja poissaolopankin tapahtuma -yksiköltä puuttuu rekisteröinnin vahvistus | Loma- ja poissaolon pankin tapahtuma -yksikköä käytettäessä työntekijöitä, jotka eivät ole vielä rekisteröityneet suunnitelmaan, ei voi enää tuoda. |
| 554854 | Kalenterin päivittäminen Työsuhde-yksikössä aiheuttaa virheen, jos käyttäjäasetuksissa on eri oletusyritys | Työsuhde-yksikön käyttäminen työntekijän kalenterin päivittämiseen ei enää aiheuta virhettä, jos käyttäjäasetuksissa on eri oletusyritys. |
| 558347 | Aloitussivua ladattaessa ilmestyy virhe ”Tietuetta ei voi luoda lomakekonfiguroinneissa (FormRunConfiguration)”. | Mukautukset aiheuttavat virheen ”Tietuetta ei voi luoda lomakekonfiguroinneissa (FormRunConfiguration)” aloitussivua ladattaessa. |
| 557327 | Etujen hallinnan työtila: Ruudukon yläpuolella näkyy rako. | Korjattiin käyttökokemukseen liittyvä ongelma, jossa Edut-työtilan taulukkoruudukon reunoissa näkyi aukko. |
| 557334 | Etujen hallinnan työtila: **Kausi**-pudotusvalikon tulisi näkyä vain **Yhteenveto**-välilehdessä | Etujen **Kausi**-pudotusvalikko näytetään nyt vain, kun **Yhteenveto**-välilehti on aktiivisena Edut-työtilassa, eikä **Prosessin tulokset**- tai **Linkit**-osiossa. |
| 557336 | Etujen hallinnan työtila: Teksti **Avoin rekisteröinti vahvistetuilla suunnitelmilla** on nyt lyhennetty ruutunäkymässä | Ruutunäkymässä oleva teksti muutettiin muotoon **Vahvistetut suunnitelmat... avoin rekisteröinti**, jotta tärkeitä asiayhteystietoja ei rajautuisi pois. |

## <a name="in-preview"></a>Esiversiossa

Seuraavat uudet ominaisuudet ovat esiversioita. Lisätietoja ominaisuuksien ottamisesta käyttöön tai poistamisesta käytöstä on kohdassa [Ominaisuuksien hallinta](hr-admin-manage-features.md).

| Ominaisuus | Julkaisusuunnitelma | Dokumentaatio |
| --- | --- | --- |
| Etujen hallinnan työtila | [Etujen hallinnan työtila (esikatselu)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Etujen hallinnan työtila](hr-benefits-management-workspace.md) |
| Estä työntekijöitä muokkaamasta yrityksen yhteystietoja | [Estä työntekijöitä muokkaamasta yrityksen yhteystietoja](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/restrict-employees-editing-business-contact-details) | [Henkilökohtaisten tietojen muokkaamisen rajoittaminen](hr-employee-self-service-restrict-editing.md)|

## <a name="coming-soon"></a>Tulossa pian

| Ominaisuus | Tietoja |
| --- | --- |
| Työnkulku voi hyväksyä työntekijöidensä esimiehen syöttämät osaamisalueet automaattisesti. | Tulossa pian. |

Täydellinen luettelo suunnitelluista ominaisuuksista ja niiden aikataulutetuista julkaisuista on kohdassa [Dynamics 365 Human Resourcesin vuoden 2021 1. julkaisuaallon yleiskatsaus](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="see-also"></a>Lisätietoja

[Human Resourcesin uudet ja muuttuneet ominaisuudet](hr-admin-whats-new.md)</br>
[Yhteenveto Dynamics 365 Human Resourcesin vuoden 2021 julkaisuaallosta 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)</br>
[Päivitysprosessi](hr-admin-setup-update-process.md)</br>
[Ominaisuuksien hallinta](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]