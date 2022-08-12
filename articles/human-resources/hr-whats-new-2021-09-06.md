---
title: Dynamics 365 Human Resources:n uudet tai muuttuneet ominaisuudet 6. syyskuuta 2021
description: Tässä artikkelissa käsitellään Microsoft Dynamics 365 Human Resourcesin 6. syyskuuta 2021 julkaistuja uusia tai muuttuneita ominaisuuksia.
author: marcelbf
ms.date: 09/06/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-09-06
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 03f832a6a3a099c472b781f7e2258ac575127101
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/29/2022
ms.locfileid: "9069997"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-september-6-2021"></a>Dynamics 365 Human Resources:n uudet tai muuttuneet ominaisuudet 6. syyskuuta 2021

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Tässä artikkelissa käsitellään Microsoft Dynamics 365 Human Resourcesin uusia, muuttuneita tai tulevia toimintoja.

Lisätietoja päivitysprosessista ja aikataulusta on kohdassa [Päivitysprosessi](hr-admin-setup-update-process.md).

Lisätietoja uusista ominaisuuksista ja niiden odotetuista yleisen saatavuuden päivämääristä on kohdassa [Dynamics 365 Human Resourcesin vuoden 2021 2. julkaisuaallon yleiskatsaus](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>Tässä julkaisussa

Tämä julkaisu sisältää seuraavat uudet ominaisuudet ja ohjelmakorjaukset. Muutokset koskevat koontiversion numeroa 8.1.4443.

### <a name="new-features"></a>Uudet ominaisuudet

Seuraavat ominaisuudet ovat yleisesti saatavana tässä julkaisussa.

| Ominaisuus | Julkaisusuunnitelma | Dokumentaatio |
|---|---|---|
| Poissaolojen hallinnan esimiehen käyttöön ottaminen | [Poissaolojen hallinnan esimiehen käyttöön ottaminen](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-absence-manager-manage-leave) | Tässä versiossa päivitetään poissaolojen hallintatyötilan näkymä. Lisätietoja on kohdassa [Poissaolojen hallintaroolin määrittäminen](https://go.microsoft.com/fwlink/?linkid=2168107). |
| Määritä liitteen tarve lomatyyppiä kohden | [Määritä liitteen tarve lomatyyppiä kohden](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/mandate-attachments-specific-leave-types) | [Loma- ja poissaolotyyppien määrittäminen](https://go.microsoft.com/fwlink/?linkid=2168108) |
| Määritä lomayksiköt lomatyypin mukaan | [Määritä lomayksiköt lomatyypin mukaan](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/configure-leave-units-per-leave-type) | [Loma- ja poissaolotyyppien määrittäminen](https://go.microsoft.com/fwlink/?linkid=2168215) |

### <a name="bug-fixes"></a>Ohjelmavirhekorjaukset

Tämä julkaisu sisältää seuraavat ohjelmakorjaukset.

> [!NOTE]
> Tavoitteena on, että nämä tiedot ovat käytettävissä mahdollisimman pian. Tämän artikkelin päivitys saattaa sisältää ohjelmakorjauksia, jotka on otettu käyttöön koontiversiossa tämän artikkelin alkuperäisen julkaisun jälkeen.

| Ongelman numero | Ongelma | Kuvaus |
|---|---|---|
| 610128 | Virhe tietojen julkaisussa käytettäessä kohdetta HcmDiscussionOverallCommentEntity | Kun tietoja julkaistaan Excel-työkirjasta HcmDiscussionOverralCommentEntity-entiteettiin, tapahtuu seuraava virhe: "Tietolähdetietuetta tyyppiä HcmTopicOverrall ei löydy." |
| 589073 | EEO-1-raportti laskee "Määrittämätön"-arvoja ja tyhjiä arvoja **Sukupuoli**-kentälle "Nainen"-arvona. | Jos arvoa **Mies** ei määritetä **Sukupuoli**-kentälle, EEO-1-raportti muodostaa oletusarvon **Nainen**. |
| 589617 | Kohteet Poissaolokortin saldo sekä Ostettava ja Myytävä saldo eivät tule näkyviin, jos käyttäjäroolit on rajoitettu tiettyyn juridiseen henkilöön. | Jos käyttäjä (työntekijärooli) on rajoitettu tiettyyn juridiseen henkilöön, saldot eivät näy oikein **Poissaolosaldot**-kortissa ja **Ostettava** ja **Myytävä**-kentissä. |
| 604310 | Poissaolon hallinta -välilehti tulee piilottaa, jos käyttäjälle ei ole delegoitu poissaolohierarkiaa. | Kaikilta juridisilta henkilöiltä **Poissaolon hallinta** -välilehti tulee piilottaa itsepalveluportaalissa, ellei yrityksenlaajuinen parametri ole otettu käyttöön ja ellei käyttäjään ole liitetty vähintään yksi poissaolohierarkia. |

## <a name="in-preview"></a>Esiversiossa

Seuraavat uudet ominaisuudet ovat esiversioita. Lisätietoja ominaisuuksien ottamisesta käyttöön tai poistamisesta käytöstä on kohdassa [Ominaisuuksien hallinta](hr-admin-manage-features.md).

| Ominaisuus | Julkaisusuunnitelma | Dokumentaatio |
|---|---|---|
| Ota käyttöön palkanlaskennan yksinkertaistettu integrointi (Palkanlaskennan integroinnin ohjelmointirajapinnat) | [Yksinkertaisen integroinnin käyttöönotto palkanlaskennan palveluntarjoajien kanssa](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-simplified-integration-payroll-providers) | [Palkanlaskennan integroinnin ohjelmointirajapinta](hr-admin-integration-payroll-api-introduction.md) |
| Etujen hallinnan työtila | [Etujen hallinnan työtila (esikatselu)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Etujen hallinnan työtila](hr-benefits-management-workspace.md) |
| Merkitse työntekijät valmiiksi maksettavaksi | [Merkitse työntekijät valmiiksi maksettavaksi](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-employees-be-marked-as-ready-pay) | [Valmis maksettavaksi](/dynamics365/human-resources/hr-compensation-payroll) |
| Kelpoisuuden mukautetut kentät |[Mukautettujen kenttien tuki kelpoisuuskäsittelyssä](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/custom-field-support-benefits-management) | [Mukautettujen kenttien käyttäminen kelpoisuuskäsittelyssä](/dynamics365/human-resources/hr-benefits-setup-eligibility-rules#using-custom-fields-in-eligibility-rules) |

## <a name="coming-soon"></a>Tulossa pian

Täydellinen luettelo suunnitelluista ominaisuuksista ja niiden aikataulutetuista julkaisuista on kohdassa [Dynamics 365 Human Resourcesin vuoden 2021 2. julkaisuaallon yleiskatsaus](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/).

| Ominaisuus | Lisätietoja |
|---|---|
| Platform Update 10.0.21 (45) | Platform update -päivitys 10.0.21 on ajoitettu alkamaan palvelujulkaisun kanssa 4. lokakuuta 2021. Lisätietoja on [Talous- ja toimintosovellusten version 10.0.21 käyttöympäristön päivityksissä (lokakuu 2021)](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-21). |
| Etulauseke | Etulauseke työntekijän nykyisten etujen tarkastelemista varten. Lisätietoja on julkaisuaallon asiakirjan kohdassa [Etulauseke](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/benefits-summary-statement). |

## <a name="see-also"></a>Lisätietoja

[Human Resourcesin uudet ja muuttuneet ominaisuudet](hr-admin-whats-new.md)</br>
[Yhteenveto Dynamics 365 Human Resourcesin vuoden 2021 julkaisuaallosta 2](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/)</br>
[Päivitysprosessi](hr-admin-setup-update-process.md)</br>
[Ominaisuuksien hallinta](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]

