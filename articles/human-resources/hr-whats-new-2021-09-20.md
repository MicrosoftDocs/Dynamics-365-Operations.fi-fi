---
title: Dynamics 365 Human Resources:n uudet tai muuttuneet ominaisuudet 20. syyskuuta 2021
description: Tässä ohjeaiheessa käsitellään Microsoft Dynamics 365 Human Resourcesin 20. syyskuuta 2021 julkaistuja uusia tai muuttuneita ominaisuuksia.
author: marcelbf
ms.date: 09/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-09-20
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: a3fd8705c7735cb3c0945f71651fafa767a7addf
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/04/2022
ms.locfileid: "8691579"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-september-20-2021"></a>Dynamics 365 Human Resources:n uudet tai muuttuneet ominaisuudet 20. syyskuuta 2021

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Tässä aiheessa käsitellään Microsoft Dynamics 365 Human Resourcesin uusia, muuttuneita tai pian tulossa olevia ominaisuuksia.

Lisätietoja päivitysprosessista ja aikataulusta on kohdassa [Päivitysprosessi](hr-admin-setup-update-process.md).

Lisätietoja uusista ominaisuuksista ja niiden odotetuista yleisen saatavuuden päivämääristä on kohdassa [Dynamics 365 Human Resourcesin vuoden 2021 2. julkaisuaallon yleiskatsaus](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>Tässä julkaisussa

Tämä julkaisu sisältää seuraavat uudet ominaisuudet ja ohjelmakorjaukset. Muutokset koskevat koontiversion numeroa 8.1.4464.

### <a name="new-features"></a>Uudet ominaisuudet

Seuraavat ominaisuudet ovat yleisesti saatavana tässä julkaisussa.

| Ominaisuus | Julkaisusuunnitelma | Dokumentaatio |
|---|---|---|
| Ota käyttöön palkanlaskennan yksinkertaistettu integrointi (Palkanlaskennan integroinnin ohjelmointirajapinnat) | [Yksinkertaisen integroinnin käyttöönotto palkanlaskennan palveluntarjoajien kanssa](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-simplified-integration-payroll-providers) | [Palkanlaskennan integroinnin ohjelmointirajapinta](hr-admin-integration-payroll-api-introduction.md) |
| Merkitse työntekijät valmiiksi maksettavaksi | [Merkitse työntekijät valmiiksi maksettavaksi](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-employees-be-marked-as-ready-pay) | [Valmis maksettavaksi](/dynamics365/human-resources/hr-compensation-payroll) |

### <a name="bug-fixes"></a>Ohjelmavirhekorjaukset

Tämä julkaisu sisältää seuraavat ohjelmakorjaukset.

> [!NOTE]
> Tavoitteena on, että nämä tiedot ovat käytettävissä mahdollisimman pian. Tämän aiheen päivitys saattaa sisältää ohjelmakorjauksia, jotka on otettu käyttöön koontiversiossa tämän ohjeaiheen alkuperäisen julkaisin jälkeen.

| Ongelman numero | Ongelma | Kuvaus |
|---|---|---|
| 619774 | Osoitekuvauksen muokkaaminen ei synkronoidu Dataverseen reaaliaikaisesti. | Kun työntekijän osoitteen kuvausta muokataan, päivitettyä kuvausta ei synkronoida reaaliaikaisesti Dataverseen. Kuvaus **Logistiikkatoimipaikka**-taulukossa päivitettiin päivityksen lähettämistä varten. |
| 614603| Virhe **Työntekijä**-sivulla, kun **Työntekijän henkilöstötoiminnot** -parametria ei ole valittu. | Kun uutta työntekijää rekrytoidaan tai kun siirrytään **Työntekijä**-sivulle, Kenttä **Henkilöstötoiminnon tyyppi** on täytettävä -virhe näytetään, vaikka **Henkilöstötoiminnot** on poistettu käytöstä. |
| 615367 | **Hyväksytty poissaolo** -välilehdessä näkyy varoitus, ja se näkyy virheellisesti. | Jos lomayksiköksi on määritetty **Päivää** ennen **Määritä lomayksiköt lomatyypin mukaan** -ominaisuuden ottamista käyttöön, **Hyväksytty loma** -välilehdessä näkyy virheellinen varoitus ja virheelliset sarakkeet. |


## <a name="in-preview"></a>Esiversiossa

Seuraavat uudet ominaisuudet ovat esiversioita. Lisätietoja ominaisuuksien ottamisesta käyttöön tai poistamisesta käytöstä on kohdassa [Ominaisuuksien hallinta](hr-admin-manage-features.md).

| Ominaisuus | Julkaisusuunnitelma | Dokumentaatio |
|---|---|---|
| Etujen hallinnan työtila | [Etujen hallinnan työtila (esikatselu)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Etujen hallinnan työtila](hr-benefits-management-workspace.md) |
| Kelpoisuuden mukautetut kentät |[Mukautettujen kenttien tuki kelpoisuuskäsittelyssä](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/custom-field-support-benefits-management) | [Mukautettujen kenttien käyttäminen kelpoisuuskäsittelyssä](/dynamics365/human-resources/hr-benefits-setup-eligibility-rules#using-custom-fields-in-eligibility-rules) |
| Etulauseke |[Etuusilmoitus](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/benefits-summary-statement) | [Etulauseke](hr-benefits-statement.md) |

### <a name="benefits-statement-known-issues"></a>Etuusilmoituksen tunnetut ongelmat

| Ongelma | Kuvaus |
|---|---|
| **Työntekijän itsepalvelun** **Raporttiparametrit**-sivulla oleva etuusilmoitus on virheellinen. | Jos **etuusilmoitukseen** siirrytään **työntekijän itsepalveluun**, **Raporttiparametrit**-sivulla näkyy **Sisällytettävät tietueet**- ja **Suorita taustalla** -pikavälilehdet.  Nämä on poistettava. |
| Suljetut ja tulevat kaudet näkyvät etuusilmoituksen **Raporttiparametri**-sivulla. | Kun käyttäjä siirtyy **Etuusilmoitusraportti**-kohdesivulle, käyttäjä voi valita suljetun tai tulevaisuuteen päivitetyn etusuunnitelman, jolloin tuloksena on tyhjä sivu. Luettelossa pitäisi näkyvä vain nykyinen etuussuunnitelmakausi. |
|Virhe lähetettäessä raportti sähköpostitse käyttämällä raportin kohdetta GER. | Etuusilmoitus voidaan määrittää käyttämään sähköpostiparametreja **Raportoinnin kohteet GER** -sivua. Kun raportin määritystä ja tulostusta viimeistellään, käyttäjä saa muotoiluvirheen eikä etuusilmoitusta lähetetä.|


## <a name="coming-soon"></a>Tulossa pian

Täydellinen luettelo suunnitelluista ominaisuuksista ja niiden aikataulutetuista julkaisuista on kohdassa [Dynamics 365 Human Resourcesin vuoden 2021 2. julkaisuaallon yleiskatsaus](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/).

| Ominaisuus | Lisätietoja |
|---|---|
| Platform Update 10.0.21 (45) | Platform update -päivitys 10.0.21 on ajoitettu alkamaan palvelujulkaisun kanssa 4. lokakuuta 2021. Lisätietoja on [Rahoitus ja toiminnot -sovellusten version 10.0.21 alustan päivityksissä (lokakuu 2021)](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-21). |
|Suorituskyvyn kirjauskansioiden laajennettu raporttinäkymä | Tämä ominaisuus otetaan käyttöön oletusarvoisesti seuraavassa käyttöönotossa. |


## <a name="see-also"></a>Lisätietoja

[Human Resourcesin uudet ja muuttuneet ominaisuudet](hr-admin-whats-new.md)</br>
[Yhteenveto Dynamics 365 Human Resourcesin vuoden 2021 julkaisuaallosta 2](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/)</br>
[Päivitysprosessi](hr-admin-setup-update-process.md)</br>
[Ominaisuuksien hallinta](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
