---
title: Dynamics 365 Human Resources -sovelluksen uudet tai muuttuneet ominaisuudet 19. huhtikuuta 2021
description: Tässä ohjeaiheessa käsitellään Microsoft Dynamics 365 Human Resourcesin 19. huhtikuuta 2021 julkaistuja uusia tai muuttuneita ominaisuuksia.
author: marcelbf
ms.date: 04/19/2021
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
ms.search.validFrom: 2021-04-19
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d0a908a6c1c8d8e08be61b684d29e9b37468ef80
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/11/2021
ms.locfileid: "6019247"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-april-19-2021"></a>Dynamics 365 Human Resources -sovelluksen uudet tai muuttuneet ominaisuudet 19. huhtikuuta 2021

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Tässä ohjeaiheessa käsitellään Dynamics 365 Human Resourcesin uusia, muuttuneita tai pian tulossa olevia ominaisuuksia.

Lisätietoja päivitysprosessista ja aikataulusta on kohdassa [Päivitysprosessi](hr-admin-setup-update-process.md).

Lisätietoja uusista ominaisuuksista ja niiden odotetuista yleisen saatavuuden päivämääristä on kohdassa [Dynamics 365 Human Resourcesin vuoden 2021 1. julkaisuaallon yleiskatsaus](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>Tässä julkaisussa

Tämä julkaisu sisältää seuraavat uudet ominaisuudet ja ohjelmakorjaukset. Muutokset koskevat koontiversion numeroa 8.1.4113.

### <a name="new-features"></a>Uudet ominaisuudet

Seuraavat ominaisuudet ovat yleisesti saatavana tässä julkaisussa.

| Ominaisuus | Julkaisusuunnitelma | Dokumentaatio |
| --- | --- | --- |
| Platform Update 10.0.17 (41) | -- | [Finance and Operations -sovellusten version 10.0.17 Platform update -päivitykset (huhtikuu 2021)](../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-17.md) |
| Etujen hallinnan lomakkeiden mukautettujen kenttien tuki | [Etujen hallinnan mukautettujen kenttien tuki](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/custom-field-support-benefits-management)| [Etujen hallinnan yleiskatsaus](hr-benefits-management-overview.md)|

### <a name="bug-fixes"></a>Ohjelmavirhekorjaukset

Tämä julkaisu sisältää seuraavat ohjelmakorjaukset.

> [!NOTE]
> Tavoitteena on, että nämä tiedot ovat käytettävissä mahdollisimman pian. Tämän ohjeaiheen päivitys saattaa sisältää ohjelmakorjauksia, jotka on otettu käyttöön koontiversiossa tämän ohjeaiheen alkuperäisen julkaisin jälkeen.

| Ongelman numero | Varasto-otto |  kuvaus |
| --- | --- | --- |
| 552164 | **Tallennettu näkymä** kohdassa **Työntekijän itsepalvelu > Avoimet kurssit** ei toimi kursseille, jotka sisältävät työjärjestyksen | Jos tallennettua näkymää käytetään avointen kurssien (ESS) yhteydessä ja toiseen kurssiin on liitetty työjärjestys, näkymässä ei enää näy useita rivejä kurssille. |
| 560614 | **Edut > Elinkaaritapahtumat** näyttävät ristiriitaisuuksia työkaluvihjeen dokumentaatiossa ja koodissa. | Päivitetyt työkaluvihjeet **Elinkaaritapahtumat**-kohdassa oikean toiminnan näyttämistä varten. |
| 560616 | **Edut > Elinkaaritapahtumat** ovat muokattavissa työntekijän etusuunnitelmassa, mutta se ei vaikuta muutoksiin. | Elinkaaritapahtuman päivitetty käyttäytyminen ottaa sen käyttöön tai poistaa käytöstä työkaluvihjeiden dokumentaation mukaan määräytyvien riippuvaisten asetusten perusteella. |
| 565054 | **Työntekijät, joilla ei ole työsuhdetta** -luettelon sisältöä ei voi tarkastella, kun **Lisäkäyttöoikeudet** ovat käytössä. | Tässä versiossa korjataan ongelma, jonka vuoksi **lisäkäyttöoikeuksien** ollessa käytössä vain järjestelmänvalvojat voivat tarkastella **Työntekijät, joilla ei ole työsuhdetta** -luettelon sisältöä. Koska tämä korjaus on tietoturvamuutos, siihen on annettava suostumus ominaisuuksien hallinnassa. Kun toiminto on käytössä, nämä roolit, joilla on lomakkeen käyttöoikeus, näkevät sisällön, vaikka lisäkäyttöoikeudet olisivatkin käytössä. Lisätietoja on kohdassa [Työntekijät, joilla ei ole työsuhdetta](hr-personnel-workers-without-employment.md). |
| 570586 | Lomapyynnön vahvistus epäonnistuu, kun työsuhde päättyy ennen työntekijän uusinta tapahtumaa kaikissa lomasuunnitelmissa. | Kun työsuhde päättyy, lomapyynnön vahvistus ei epäonnistu työntekijän lomatapahtumien perusteella.|
| 570783 | Yritystenvälisen loman ottaminen käyttöön ja käytöstä poistaminen Human Resourcesin jaetuissa parametreissa muuttaa, mitä yhdessä yrityksessä työskentelevät työntekijät näkevät lomapyynnöissä. | Yhdessä yrityksessä työskentelevät työntekijät eivät näe muutoksia loma pyytämisessä, jos parametri on käytössä tai poistettu käytöstä. |
| 572343 | Vaadittua syykoodia ei näytetä, kun yritystenvälinen lomanäkymäominaisuus on käytössä. | Syykoodi näkyy nyt odotetulla tavalla, kun yritystenvälinen lomanäkymäominaisuus on käytössä. |
| 573676 | **Kauden** lisääminen kohtaan **Etujen hallinta > Linkit > Etusuunnitelmat** ei onnistu. | Virheenkorjaus kun **kautta** ei voitu lisätä tai päivittää aiemmin luodussa **Etusuunnitelma**-lomakkeessa. |

## <a name="in-preview"></a>Esiversiossa

Seuraavat uudet ominaisuudet ovat esiversioita. Lisätietoja ominaisuuksien ottamisesta käyttöön tai poistamisesta käytöstä on kohdassa [Ominaisuuksien hallinta](hr-admin-manage-features.md).

| Ominaisuus | Julkaisusuunnitelma | Dokumentaatio |
| --- | --- | --- |
| Etujen hallinnan työtila | [Etujen hallinnan työtila (esikatselu)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Etujen hallinnan työtila](hr-benefits-management-workspace.md) |
| Loma- ja poissaolotyönkulun parannukset | [Loma- ja poissaolotyönkulun parannukset](https://go.microsoft.com/fwlink/?linkid=2147528) | [Pyydä vapaata](hr-employee-self-service-request-time-off.md)|
| Ota käyttöön palkanlaskennan yksinkertaistettu integrointi (Palkanlaskennan integroinnin ohjelmointirajapinnat) | [Yksinkertaisen integroinnin käyttöönotto palkanlaskennan palveluntarjoajien kanssa](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-simplified-integration-payroll-providers) | [Palkanlaskennan integroinnin ohjelmointirajapinta](hr-admin-integration-payroll-api-introduction.md)|

## <a name="coming-soon"></a>Tulossa pian

| Ominaisuus | Lisätietoja |
| --- | --- |
| Työnkulku voi hyväksyä työntekijöidensä esimiehen syöttämät osaamisalueet automaattisesti. | Tulossa pian. |
| Platform Update 10.0.18 (42) | Ympäristön päivitys 10.0.18 on ajoitettu alkamaan julkaisun kanssa 17.5.2021. Lisätietoja on kohdassa [Finance and Operations -sovellusten version 10.0.18 ympäristöpäivitykset (toukokuu 2021)](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-18). |
| Etujen hallinnan kelpoisuussääntöjen mukautettujen kenttien tuki  | [Mukautetun kentän tuki kelpoisuuskäsittelylle](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/custom-field-support-eligibility-processing) |

Täydellinen luettelo suunnitelluista ominaisuuksista ja niiden aikataulutetuista julkaisuista on kohdassa [Dynamics 365 Human Resourcesin vuoden 2021 1. julkaisuaallon yleiskatsaus](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="see-also"></a>Lisätietoja

[Human Resourcesin uudet ja muuttuneet ominaisuudet](hr-admin-whats-new.md)</br>
[Yhteenveto Dynamics 365 Human Resourcesin vuoden 2021 julkaisuaallosta 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)</br>
[Päivitysprosessi](hr-admin-setup-update-process.md)</br>
[Ominaisuuksien hallinta](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
