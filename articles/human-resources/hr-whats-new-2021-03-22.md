---
title: Dynamics 365 Human Resourcesin uudet tai muuttuneet ominaisuudet (22. maaliskuuta 2021)
description: Tässä ohjeaiheessa käsitellään Microsoft Dynamics 365 Human Resourcesin 22. maaliskuuta 2021 julkaistuja uusia tai muuttuneita ominaisuuksia.
author: marcelbf
ms.date: 03/22/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-03-22
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: b973be365b3afa8461f7709c1ecee835c5dcf2f1
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/13/2021
ms.locfileid: "5890648"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-march-22-2021"></a>Dynamics 365 Human Resourcesin uudet tai muuttuneet ominaisuudet (22. maaliskuuta 2021)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Tässä ohjeaiheessa käsitellään Dynamics 365 Human Resourcesin uusia, muuttuneita tai pian tulossa olevia ominaisuuksia.

Lisätietoja päivitysprosessista ja aikataulusta on kohdassa [Päivitysprosessi](hr-admin-setup-update-process.md).

Lisätietoja uusista ominaisuuksista ja niiden odotetuista yleisen saatavuuden päivämääristä on kohdassa [Dynamics 365 Human Resourcesin vuoden 2021 1. julkaisuaallon yleiskatsaus](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>Tässä julkaisussa

Tämä julkaisu sisältää seuraavat uudet ominaisuudet ja ohjelmakorjaukset. Muutokset koskevat koontiversion numeroa 8.1.4049.

### <a name="new-features"></a>Uudet ominaisuudet

Seuraavat ominaisuudet ovat yleisesti saatavana tässä julkaisussa.

| Ominaisuus | Julkaisusuunnitelma | Dokumentaatio |
| --- | --- | --- |
| Asetus, joka pakottaa jumiutuneiden erätöiden peruutuksen ja nollaamisen (560976) | Ei sovellu | [Jumittuneiden erätöiden nollaaminen](./hr-admin-troubleshooting-batch-execution.md) |
| Pienet käyttökokemuksen päivitykset uuden etusuunnitelman luomista varten (419941) | Ei sovellu | [Luo etusuunnitelma](hr-benefits-plans-setup.md) |

### <a name="bug-fixes"></a>Ohjelmavirhekorjaukset

Tämä julkaisu sisältää seuraavat ohjelmakorjaukset.

> [!NOTE]
> Tavoitteena on, että nämä tiedot ovat käytettävissä mahdollisimman pian. Tämän ohjeaiheen päivitys saattaa sisältää ohjelmakorjauksia, jotka on otettu käyttöön koontiversiossa tämän ohjeaiheen alkuperäisen julkaisin jälkeen.

| Ongelman numero | Varasto-otto |  kuvaus |
| --- | --- | --- |
| 554239 | **BusinessProcessTaskAssignment**-tauluun liittyvien yksiköiden suorituskyvyn parannukset | Parantaa **BusinessProcessTaskAssignment**-tauluun liittyvien yksiköiden suorituskykyä lisäämällä ehdotettuja indeksejä tauluun. |
| 566061 | Poista V2-yksikön varakoodi yön aikana suoritettavasta synkronoinnista | Poista Dataversen yösynkronoinnin V2-varakoodi. Varakoodi ei ole enää tarpeen, ja se estää suodatetun synkronoinnin toimimasta odotetulla tavalla. Muutos parantaa Dataverse-tietojen synkronoinnin yhdenmukaisuutta. |
| 538024 | Työntekijän etusuunnitelmat > Uloskuittauksen poistamisen virhe | Korjattu virhe, joja syntyy poistettaessa Työntekijän edut -lomakkeen Etusuunnitelma-vaihtoehdon uloskuittaus. |
| 557965 | **Edut**-työtila: **Aktiiviset elinkaaritapahtumat** -linkin on aina oltava näkyvissä **Linkit**-osassa | Korjattu ongelma, jossa **Aktiiviset elinkaaritapahtumat** -linkki on ollut näkyvissä **Linkit**-osassa, mutta se luo virheen siirryttäessä, jos **(Esiversio) Etujen hallinnan työtila** -ominaisuutta ei ole otettu käyttöön. Lisätietoja työtilan ottamisesta käyttöön on kohdassa [Etujen hallinnan työtila](hr-benefits-management-workspace.md). |
| 556672 | Työntekijälle, jonka työsuhde on päättynyt, ei voi käsitellä jaksotuksia, kun **Yksinkertaistettu työntekijöiden lisääminen** on otettu käyttöön ominaisuuksien hallinnassa | Loma- ja poissaolosuunnitelmien jaksottamisvaihtoehto on lisätty työntekijöiden **Työhistoria**-kohdan **Lisäasetukset**-kohtaan, kun **Yksinkertaistettu työntekijöiden lisääminen** on otettu käyttöön toiminnonhallinnassa. |
| 562656 | **SysRecordChangeLogValidTimeState**-valikkokohteen tulisi sisältyä **SystemExternalBasicMaintain**-suojausvelvollisuuden suojausoikeuksiin ja laajennukseen | Järjestelmän ulkopuolisista järjestelmänvalvojien rooleista puuttuu **Näytä muutokset** -painike päivämääränhallintalomakkeissa. |
| 505989 | Elinkaaritapahtumien käsittely: Oikeutuksen muutosta ei käsitellä oikein käytetyn päivämäärän vuoksi | Korjattu ongelma, jossa oikeutuskäsittelyn muutos riippui toimen alkamispäivämäärästä, ei vain nykyisestä toimesta. |
| 562286 | Työntekijän työsuhteen päättäminen lähettää useita päivityksiä Dataverseen | Kun työntekijän työsuhde päätetään, lähetetään useita päivitystoimintoja Dataverseen, jolloin samasta muutoksesta tulee kaksi päivitysilmoitusta. Tämä voi aiheuttaa useita laukaisuja, jos Power Automate -työnkulku on määritetty käynnistymään toiminnosta. |
| 527340 | Ei esitettävä DateTime -virheilmoitus tulee näyttöön, kun loma- ja poissaolorekisteröinnit avataan | Kun valitaan loma- ja poissaolorekisteröinti, virhe ei enää näy. |
| 561663 | Klusterin valmistelun kasvanut odotusaika | Parantaa klusterin valmistelun päivitysten yhdenmukaista infrastruktuuria ja valmistelun yhdenmukaisuutta. |
| 486129 | Mukautettuja kenttiä ei voi muokata kohteessa **Toimet > Muutosten hallinta** | Korjattu ongelma, jossa mukautettuja kenttiä ei voi muokata **Muutosten hallinta** -välilehdessä kohdassa **Toimet**. |

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