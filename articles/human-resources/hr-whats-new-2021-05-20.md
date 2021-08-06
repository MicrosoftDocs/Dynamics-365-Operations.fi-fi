---
title: Dynamics 365 Human Resourcesin uudet tai muuttuneet ominaisuudet 20. toukokuuta 2021
description: Tässä ohjeaiheessa käsitellään Microsoft Dynamics 365 Human Resourcesin 20. toukokuuta 2021 julkaistuja uusia tai muuttuneita ominaisuuksia.
author: marcelbf
ms.date: 05/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-05-20
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c7b7f71cf084a05bb0278f5df4ddb022ef3d640f
ms.sourcegitcommit: baad2723291774f610324a8054fc14abf3287fe1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/14/2021
ms.locfileid: "6560047"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-may-20-2021"></a>Dynamics 365 Human Resourcesin uudet tai muuttuneet ominaisuudet 20. toukokuuta 2021

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Tässä ohjeaiheessa käsitellään Dynamics 365 Human Resourcesin uusia, muuttuneita tai pian tulossa olevia ominaisuuksia.

Lisätietoja päivitysprosessista ja aikataulusta on kohdassa [Päivitysprosessi](hr-admin-setup-update-process.md).

Lisätietoja uusista ominaisuuksista ja niiden odotetuista yleisen saatavuuden päivämääristä on kohdassa [Dynamics 365 Human Resourcesin vuoden 2021 1. julkaisuaallon yleiskatsaus](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>Tässä julkaisussa

Tämä julkaisu sisältää seuraavat uudet ominaisuudet ja ohjelmakorjaukset. Muutokset koskevat koontiversion numeroa 8.1.4189.

### <a name="new-features"></a>Uudet ominaisuudet

Seuraavat ominaisuudet ovat yleisesti saatavana tässä julkaisussa.

| Ominaisuus | Julkaisusuunnitelma | Dokumentaatio |
| --- | --- | --- |
| Platform Update 10.0.18 (42) | -- | [Finance and Operations -sovellusten version 10.0.18 Platform update -päivitykset (toukokuu 2021)](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-18) |
| Henkilöstöhallinto-sovellus Microsoft Teamsille tukee nyt puolipäivämääritysten ja päivän jakamistoimintoa | -- | [Lomapyyntöjen hallinta Teamsissa](/dynamics365/human-resources/hr-teams-leave-app#create-a-new-request) |

### <a name="bug-fixes"></a>Ohjelmavirhekorjaukset

Tämä julkaisu sisältää seuraavat ohjelmakorjaukset.

> [!NOTE]
> Tavoitteena on, että nämä tiedot ovat käytettävissä mahdollisimman pian. Tämän ohjeaiheen päivitys saattaa sisältää ohjelmakorjauksia, jotka on otettu käyttöön koontiversiossa tämän ohjeaiheen alkuperäisen julkaisin jälkeen.

| Ongelman numero | Ongelma |  kuvaus |
| --- | --- | --- |
| 583776 | Työntekijöiden joukkorekisteröinnit poissaolosuunnitelmiin aiheuttavat tietueiden kaksoiskappaleen virheen | Tämä virhe on korjattu viimeisimmässä julkaisussa, ja joukkopoissaolosuunnitelman rekisteröiminen voidaan käsitellä onnistuneesti. |
| 582263 | Elämäntapahtumien käsittelyä ei voida suorittaa kaikille työntekijöille kerralla | Kun **Työntekijä**-kenttä jätetään tyhjäksi tapahtumakäsittelyä varten, kaikki työntekijät käsitellään. |
| 558383 | Ensisijaista edunsaajaa ei ole merkitty 100%:ksi, jos oletushakijaa ei ole valittu | Virhe on korjattu, joten käyttäjän on valittava vain ensisijainen käyttäjätilin käyttökokemus.|
| 509404 | Osaston henkilöstölaskenta, jossa ei huomioida työntekijöiden liikkumista osaston välillä |Analyysi on päivitetty niin, että se sisältää työntekijöiden siirrot osastojen välillä|
| 579420 | Sarakkeiden jäädyttäminen ruudukkotoiminnossa ei ole vielä käytettävissä | **Sarakkeiden jäädyttäminen ruudukossa** -ominaisuus, joka ei ole käytettävissä henkilöstöresursseissa, on luetteloitu saatavana olevaksi ominaisuuden hallinnassa. Ominaisuus on poistettu käyttöön otettavasta toimintoluettelosta. |

## <a name="in-preview"></a>Esiversiossa

Seuraavat uudet ominaisuudet ovat esiversioita. Lisätietoja ominaisuuksien ottamisesta käyttöön tai poistamisesta käytöstä on kohdassa [Ominaisuuksien hallinta](hr-admin-manage-features.md).

| Ominaisuus | Julkaisusuunnitelma | Dokumentaatio |
| --- | --- | --- |
| Etujen hallinnan kelpoisuussääntöjen mukautettujen kenttien tuki | [Mukautetun kentän tuki kelpoisuuskäsittelylle](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/custom-field-support-eligibility-processing) |[Oikeutussääntöjen määrittäminen](/dynamics365/human-resources/hr-benefits-setup-eligibility-rules) |
| Etujen hallinnan työtila | [Etujen hallinnan työtila (esikatselu)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Etujen hallinnan työtila](hr-benefits-management-workspace.md) |
| Loma- ja poissaolotyönkulun parannukset | [Loma- ja poissaolotyönkulun parannukset](https://go.microsoft.com/fwlink/?linkid=2147528) | [Pyydä vapaata](hr-employee-self-service-request-time-off.md)|
| Ota käyttöön palkanlaskennan yksinkertaistettu integrointi (Palkanlaskennan integroinnin ohjelmointirajapinnat) | [Yksinkertaisen integroinnin käyttöönotto palkanlaskennan palveluntarjoajien kanssa](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-simplified-integration-payroll-providers) | [Palkanlaskennan integroinnin ohjelmointirajapinta](hr-admin-integration-payroll-api-introduction.md)|
| Loman jaksotustapahtuman tarkistus | - | [Loman jaksotustapahtuman tarkistus](hr-leave-and-absence-accrue.md)|

## <a name="coming-soon"></a>Tulossa pian

| Ominaisuus | Lisätietoja |
| --- | --- |
|  Poissaolojen hallinnan esimiehen käyttöön ottaminen | [Poissaolojen hallinnan esimiehen käyttöön ottaminen](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-absence-manager-manage-leave) |

Täydellinen luettelo suunnitelluista ominaisuuksista ja niiden aikataulutetuista julkaisuista on kohdassa [Dynamics 365 Human Resourcesin vuoden 2021 1. julkaisuaallon yleiskatsaus](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="see-also"></a>Lisätietoja

[Human Resourcesin uudet ja muuttuneet ominaisuudet](hr-admin-whats-new.md)</br>
[Yhteenveto Dynamics 365 Human Resourcesin vuoden 2021 julkaisuaallosta 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)</br>
[Päivitysprosessi](hr-admin-setup-update-process.md)</br>
[Ominaisuuksien hallinta](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
