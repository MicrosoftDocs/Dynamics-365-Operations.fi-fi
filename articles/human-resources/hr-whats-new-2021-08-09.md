---
title: Dynamics 365 Human Resourcesin uudet ja muuttuneet ominaisuudet, 9. huhtikuuta 2021
description: Tässä ohjeaiheessa käsitellään Microsoft Dynamics 365 Human Resourcesin 9. elokuuta 2021 julkaistuja uusia tai muuttuneita ominaisuuksia.
author: marcelbf
ms.date: 08/09/2021
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
ms.search.validFrom: 2021-08-09
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0f515b614aedce3d58994bf21104ada25702a71e
ms.sourcegitcommit: fc19ee0aba2a6174fef305d151f1eb23ca6c0346
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/13/2021
ms.locfileid: "7385697"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-august-9-2021"></a>Dynamics 365 Human Resourcesin uudet ja muuttuneet ominaisuudet, 9. huhtikuuta 2021

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Tässä aiheessa käsitellään Microsoft Dynamics 365 Human Resourcesin uusia, muuttuneita tai pian tulossa olevia ominaisuuksia.

Lisätietoja päivitysprosessista ja aikataulusta on kohdassa [Päivitysprosessi](hr-admin-setup-update-process.md).

Lisätietoja uusista ominaisuuksista ja niiden odotetuista yleisen saatavuuden päivämääristä on kohdassa [Dynamics 365 Human Resourcesin vuoden 2021 2. julkaisuaallon yleiskatsaus](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>Tässä julkaisussa

Tämä julkaisu sisältää seuraavat uudet ominaisuudet ja ohjelmakorjaukset. Muutokset koskevat koontiversion numeroa 8.1.4393.

### <a name="bug-fixes"></a>Ohjelmavirhekorjaukset

Tämä julkaisu sisältää seuraavat ohjelmakorjaukset.

> [!NOTE]
> Tavoitteena on, että nämä tiedot ovat käytettävissä mahdollisimman pian. Tämän aiheen päivitys saattaa sisältää ohjelmakorjauksia, jotka on otettu käyttöön koontiversiossa tämän ohjeaiheen alkuperäisen julkaisin jälkeen.

| Ongelman numero | Ongelma | kuvaus |
| --- | --- | --- |
| 558385 | Oletusedustajaa ei valita, kun **Edustajien automaattinen valinta** -vaihtoehto on otettu käyttöön oletusedustajilla. | Tämä ongelma on nyt korjattu. Useita oletusedustajia valitaan automaattisesti hyväksytyissä suunnitelmissa, kun **Edustajien automaattinen valinta** -vaihtoehto on otettu käyttöön **Human Resourcesin jaetut parametrit** -sivulla. |
| 589617 | **Poissaolo**-sivun **Ostettavissa**- ja **Myytävissä**-saldot ovat tyhjiä, kun käyttö on rajoitettu tiettyyn yritykseen. | Tämä ongelma on nyt korjattu. **Poissaolo**-sivulla näkyy oikeat **Ostettavissa**- ja **Myytävissä**-saldot ovat tyhjät, kun käyttäjä on rajoitettu tiettyyn yritykseen. |

## <a name="in-preview"></a>Esiversiossa

Seuraavat uudet ominaisuudet ovat esiversioita. Lisätietoja ominaisuuksien ottamisesta käyttöön tai poistamisesta käytöstä on kohdassa [Ominaisuuksien hallinta](hr-admin-manage-features.md).

| Ominaisuus | Julkaisusuunnitelma | Dokumentaatio |
| --- | --- | --- |
| Etujen hallinnan työtila | [Etujen hallinnan työtila (esikatselu)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Etujen hallinnan työtila](hr-benefits-management-workspace.md) |
| Ota käyttöön palkanlaskennan yksinkertaistettu integrointi (Palkanlaskennan integroinnin ohjelmointirajapinnat) | [Yksinkertaisen integroinnin käyttöönotto palkanlaskennan palveluntarjoajien kanssa](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-simplified-integration-payroll-providers) | [Palkanlaskennan integroinnin ohjelmointirajapinta](hr-admin-integration-payroll-api-introduction.md)|
| Poissaolojen hallinnan esimiehen käyttöön ottaminen | [Poissaolojen hallinnan esimiehen käyttöön ottaminen](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-absence-manager-manage-leave) | Tässä versiossa päivitetään poissaolojen hallintatyötilan näkymä. Lisätietoja on kohdassa [Poissaolojen hallintaroolin määrittäminen](https://go.microsoft.com/fwlink/?linkid=2168107). |
| Määritä liitteen tarve lomatyyppiä kohden | [Määritä liitteen tarve lomatyyppiä kohden](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/mandate-attachments-specific-leave-types) |[Loma- ja poissaolotyyppien määrittäminen](https://go.microsoft.com/fwlink/?linkid=2168108)|
| Määritä lomayksiköt lomatyypin mukaan | [Määritä lomayksiköt lomatyypin mukaan](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/configure-leave-units-per-leave-type) |[Loma- ja poissaolotyyppien määrittäminen](https://go.microsoft.com/fwlink/?linkid=2168215)|
| Merkitse työntekijät valmiiksi maksettavaksi | [Merkitse työntekijät valmiiksi maksettavaksi](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-employees-be-marked-as-ready-pay) | [Valmis maksettavaksi](/dynamics365/human-resources/hr-compensation-payroll) |

## <a name="coming-soon"></a>Tulossa pian

Täydellinen luettelo suunnitelluista ominaisuuksista ja niiden aikataulutetuista julkaisuista on kohdassa [Dynamics 365 Human Resourcesin vuoden 2021 2. julkaisuaallon yleiskatsaus](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/).

| Ominaisuus | Lisätietoja |
| --- | --- |
| Platform Update 10.0.21 (45) | Platform update -päivitys 10.0.21 on ajoitettu alkamaan palvelujulkaisun kanssa 4. lokakuuta 2021. Lisätietoja on kohdassa [Finance and Operations -sovellusten version 10.0.21 Platform Update -päivitykset (lokakuu 2021)](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-21). |

## <a name="see-also"></a>Lisätietoja

[Human Resourcesin uudet ja muuttuneet ominaisuudet](hr-admin-whats-new.md)</br>
[Yhteenveto Dynamics 365 Human Resourcesin vuoden 2021 julkaisuaallosta 2](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/)</br>
[Päivitysprosessi](hr-admin-setup-update-process.md)</br>
[Ominaisuuksien hallinta](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
