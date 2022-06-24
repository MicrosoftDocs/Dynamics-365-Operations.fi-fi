---
title: Dynamics 365 Human Resourcesin uudet tai muuttuneet ominaisuudet 3. toukokuuta 2021
description: Tässä artikkelissa käsitellään Microsoft Dynamics 365 Human Resourcesin 3. toukokuuta 2021 julkaistuja uusia tai muuttuneita ominaisuuksia.
author: marcelbf
ms.date: 05/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-05-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 01ebd15e09e181a7ea0ec5bf70c8df731d2169c0
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8902857"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-may-3-2021"></a>Dynamics 365 Human Resourcesin uudet tai muuttuneet ominaisuudet 3. toukokuuta 2021

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Tässä artikkelissa käsitellään Dynamics 365 Human Resourcesin uusia, muuttuneita tai tulevia toimintoja.

Lisätietoja päivitysprosessista ja aikataulusta on kohdassa [Päivitysprosessi](hr-admin-setup-update-process.md).

Lisätietoja uusista ominaisuuksista ja niiden odotetuista yleisen saatavuuden päivämääristä on kohdassa [Dynamics 365 Human Resourcesin vuoden 2021 1. julkaisuaallon yleiskatsaus](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>Tässä julkaisussa

Tämä julkaisu sisältää seuraavat uudet ominaisuudet ja ohjelmakorjaukset. Muutokset koskevat koontiversion numeroa 8.1.4140.

### <a name="new-features"></a>Uudet ominaisuudet

Seuraavat ominaisuudet ovat yleisesti saatavana tässä julkaisussa.

| Ominaisuus | Julkaisusuunnitelma | Dokumentaatio |
| --- | --- | --- |
| Lisää tietopalkki, kun elinkaaritapahtumat luodaan. | - | Kun luot elinkaaritapahtuman, tietorivillä näkyy sanoma, joka ilmaisee luodun elinkaaritapahtuman tyypin.

### <a name="bug-fixes"></a>Ohjelmavirhekorjaukset

Tämä julkaisu sisältää seuraavat ohjelmakorjaukset.

> [!NOTE]
> Tavoitteena on, että nämä tiedot ovat käytettävissä mahdollisimman pian. Tämän artikkelin päivitys saattaa sisältää ohjelmakorjauksia, jotka on otettu käyttöön koontiversiossa tämän artikkelin alkuperäisen julkaisun jälkeen.

| Ongelman numero | Ongelma |  Kuvaus |
| --- | --- | --- |
| 559312 |  Taso ei näy, kun työntekijälle luodaan kiinteä kompensaatiosuunnitelma. |  Kun käyttäjän aikavyöhykkeen ja yrityksen aikavyöhykkeen välillä on ristiriita, työn kompensaatiotasoa ei lueta. Kysely on päivitetty haettavaksi UTC-ajan perusteella. |
| 573676  | Uutta jaksoa ei voi lisätä **Etusuunnitelma**-lomakkeeseen. | Päivitetty lomake niin, että **Uusi**-painike on käytössä **Kausi**-pikavälilehdessä **Etusuunnitelmat**-kohdassa. |

## <a name="in-preview"></a>Esiversiossa

Seuraavat uudet ominaisuudet ovat esiversioita. Lisätietoja ominaisuuksien ottamisesta käyttöön tai poistamisesta käytöstä on kohdassa [Ominaisuuksien hallinta](hr-admin-manage-features.md).

| Ominaisuus | Julkaisusuunnitelma | Dokumentaatio |
| --- | --- | --- |
| Etujen hallinnan työtila | [Etujen hallinnan työtila (esikatselu)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Etujen hallinnan työtila](hr-benefits-management-workspace.md) |
| Loma- ja poissaolotyönkulun parannukset | [Loma- ja poissaolotyönkulun parannukset](https://go.microsoft.com/fwlink/?linkid=2147528) | [Pyydä vapaata](hr-employee-self-service-request-time-off.md)|
| Ota käyttöön palkanlaskennan yksinkertaistettu integrointi (Palkanlaskennan integroinnin ohjelmointirajapinnat) | [Yksinkertaisen integroinnin käyttöönotto palkanlaskennan palveluntarjoajien kanssa](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-simplified-integration-payroll-providers) | [Palkanlaskennan integroinnin ohjelmointirajapinta](hr-admin-integration-payroll-api-introduction.md)|
| Loman jaksotustapahtuman tarkistus | - | [Loman jaksotustapahtuman tarkistus](hr-leave-and-absence-accrue.md)|

## <a name="coming-soon"></a>Tulossa pian

| Ominaisuus | Lisätietoja |
| --- | --- |
| Platform Update 10.0.18 (42) | Ympäristön päivitys 10.0.18 on ajoitettu alkamaan julkaisun kanssa 17.5.2021. Lisätietoja on [Rahoitus ja toiminnot -sovellusten version 10.0.18 alustan päivityksissä (toukokuu 2021)](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-18). |
| Etujen hallinnan kelpoisuussääntöjen mukautettujen kenttien tuki  | [Mukautetun kentän tuki kelpoisuuskäsittelylle](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/custom-field-support-eligibility-processing) |

Täydellinen luettelo suunnitelluista ominaisuuksista ja niiden aikataulutetuista julkaisuista on kohdassa [Dynamics 365 Human Resourcesin vuoden 2021 1. julkaisuaallon yleiskatsaus](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="see-also"></a>Lisätietoja

[Human Resourcesin uudet ja muuttuneet ominaisuudet](hr-admin-whats-new.md)</br>
[Yhteenveto Dynamics 365 Human Resourcesin vuoden 2021 julkaisuaallosta 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)</br>
[Päivitysprosessi](hr-admin-setup-update-process.md)</br>
[Ominaisuuksien hallinta](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
