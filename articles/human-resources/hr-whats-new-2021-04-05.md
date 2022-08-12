---
title: Dynamics 365 Human Resources -sovelluksen uudet tai muuttuneet ominaisuudet 5. huhtikuuta 2021
description: Tässä artikkelissa käsitellään Microsoft Dynamics 365 Human Resourcesin 5. huhtikuuta 2021 julkaistuja uusia tai muuttuneita ominaisuuksia.
author: marcelbf
ms.date: 04/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-04-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 9388b2f43762bedf07c89a7a565935d2043ee90c
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/29/2022
ms.locfileid: "9067998"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-april-5-2021"></a>Dynamics 365 Human Resources -sovelluksen uudet tai muuttuneet ominaisuudet 5. huhtikuuta 2021

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Tässä artikkelissa käsitellään Dynamics 365 Human Resourcesin uusia, muuttuneita tai tulevia toimintoja.

Lisätietoja päivitysprosessista ja aikataulusta on kohdassa [Päivitysprosessi](hr-admin-setup-update-process.md).

Lisätietoja uusista ominaisuuksista ja niiden odotetuista yleisen saatavuuden päivämääristä on kohdassa [Dynamics 365 Human Resourcesin vuoden 2021 1. julkaisuaallon yleiskatsaus](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>Tässä julkaisussa

Tämä julkaisu sisältää seuraavat uudet ominaisuudet ja ohjelmakorjaukset. Muutokset koskevat koontiversion numeroa 8.1.4074.

### <a name="new-features"></a>Uudet ominaisuudet

Seuraavat ominaisuudet ovat yleisesti saatavana tässä julkaisussa.

| Ominaisuus | Julkaisusuunnitelma | Dokumentaatio |
| --- | --- | --- |
| Estä työntekijöitä muokkaamasta yrityksen yhteystietoja | [Estä työntekijöitä muokkaamasta yrityksen yhteystietoja](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/restrict-employees-editing-business-contact-details) | [Henkilökohtaisten tietojen muokkaamisen rajoittaminen](./hr-employee-self-service-restrict-editing.md)|

### <a name="bug-fixes"></a>Ohjelmavirhekorjaukset

Tämä julkaisu sisältää seuraavat ohjelmakorjaukset.

> [!NOTE]
> Tavoitteena on, että nämä tiedot ovat käytettävissä mahdollisimman pian. Tämän artikkelin päivitys saattaa sisältää ohjelmakorjauksia, jotka on otettu käyttöön koontiversiossa tämän artikkelin alkuperäisen julkaisun jälkeen.

| Ongelman numero | Ongelma |  Kuvaus |
| --- | --- | --- |
| 550852 | **Hyväksyntä**-painike ei vahvista pakollisten kenttien hyväksymistä **Tarkistus**-lomakkeessa. | Kun määrität **Tarkistus**-lomakkeen kentän pakolliseksi ja julkaiset hallintaroolin muutokset, lomaketta ei vahvistaa odotetulla tavalla. |
| 559564 | Kiinteän kompensaation muutoksen historialliset työntekijätoiminnot antavat virheilmoituksen työsuhteen päättäneille käyttäjille. | Poistuneen työntekijän kompensaation työntekijätoiminto antaa virheilmoituksen. Kun työntekijä on poistunut, ylennys ennen työsuhteen päättämistä aiheuttaa virheen. |
| 560074 | Avattava työsuhdeluokka ei suodata **työntekijätyypin** mukaan, ja siinä näkyvät työntekijöiden ja alihankkijoiden luokat. | **Työntekijä**-lomakkeessa avattavan **Työsuhde**-luokan pitäisi näyttää joko työntekijä- tai alihankkijaluokat työntekijän työntekijätyypin perusteella. |
| 567388 | Osa juuri luotujen työntekijöiden tiedoista ei synkronoidu välittömästi **cdm_worker**-tauluun Dataversessä. | Kun uusi työntekijätietue luodaan, uusi tietue synkronoituu tietueen **cdm_worker**-kohteen tauluun, mutta kaikki ominaisuudet Dataversessä eivät sisältyisi Dataverse-tietueeseen. |
| 563837 | Ominaisuudet, jotka eivät ole käytettävissä henkilöstöhallinnon näytössä. | Useita toimintoja, jotka eivät koske henkilöstöhallinnon näyttöä ominaisuuksien hallinnassa. Nämä toiminnot poistetaan nyt henkilöstöhallinnon käyttöön käytettävissä olevien ominaisuuksien luettelosta. |

## <a name="in-preview"></a>Esiversiossa

Seuraavat uudet ominaisuudet ovat esiversioita. Lisätietoja ominaisuuksien ottamisesta käyttöön tai poistamisesta käytöstä on kohdassa [Ominaisuuksien hallinta](hr-admin-manage-features.md).

| Ominaisuus | Julkaisusuunnitelma | Dokumentaatio |
| --- | --- | --- |
| Etujen hallinnan työtila | [Etujen hallinnan työtila (esikatselu)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Etujen hallinnan työtila](hr-benefits-management-workspace.md) |

## <a name="coming-soon"></a>Tulossa pian

| Ominaisuus | Lisätietoja |
| --- | --- |
| Työnkulku voi hyväksyä työntekijöidensä esimiehen syöttämät osaamisalueet automaattisesti. | Tulossa pian. |
| Platform Update 10.0.17 (41) | Ympäristön päivitys 10.0.17 on ajoitettu alkamaan seuraavan julkaisun kanssa 19.4.2021. Lisätietoja on [Talous- ja toimintosovellusten version 10.0.17 käyttöympäristön päivityksissä (huhtikuu 2021)](../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-17.md). |

Täydellinen luettelo suunnitelluista ominaisuuksista ja niiden aikataulutetuista julkaisuista on kohdassa [Dynamics 365 Human Resourcesin vuoden 2021 1. julkaisuaallon yleiskatsaus](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="see-also"></a>Lisätietoja

[Human Resourcesin uudet ja muuttuneet ominaisuudet](hr-admin-whats-new.md)</br>
[Yhteenveto Dynamics 365 Human Resourcesin vuoden 2021 julkaisuaallosta 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)</br>
[Päivitysprosessi](hr-admin-setup-update-process.md)</br>
[Ominaisuuksien hallinta](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
