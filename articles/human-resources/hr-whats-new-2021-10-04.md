---
title: Dynamics 365 Human Resources:n uudet tai muuttuneet ominaisuudet 5. lokakuuta 2021
description: Tässä artikkelissa käsitellään Microsoft Dynamics 365 Human Resourcesin 5. lokakuuta 2021 julkaistuja uusia tai muuttuneita ominaisuuksia.
author: marcelbf
ms.date: 10/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-10-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: cc8cd8616f1b82258fccbb2b41d5e72a90aaed63
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8845109"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-october-5-2021"></a>Dynamics 365 Human Resources:n uudet tai muuttuneet ominaisuudet 5. lokakuuta 2021

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Tässä artikkelissa käsitellään Microsoft Dynamics 365 Human Resourcesin uusia, muuttuneita tai tulevia toimintoja.

Lisätietoja päivitysprosessista ja aikataulusta on kohdassa [Päivitysprosessi](hr-admin-setup-update-process.md).

Lisätietoja uusista ominaisuuksista ja niiden odotetuista yleisen saatavuuden päivämääristä on kohdassa [Dynamics 365 Human Resourcesin vuoden 2021 2. julkaisuaallon yleiskatsaus](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>Tässä julkaisussa

Tämä julkaisu sisältää seuraavat uudet ominaisuudet ja ohjelmakorjaukset. Muutokset koskevat koontiversion numeroa 8.1.4485.

### <a name="new-features"></a>Uudet ominaisuudet

Seuraavat ominaisuudet ovat yleisesti saatavana tässä julkaisussa.

| Ominaisuus | Julkaisusuunnitelma | Dokumentaatio |
|---|---|---|
| Platform Update 10.0.21 (45) | -- | [Taloushallinnon ja toimintojen sovellusten (lokakuu 2021) käyttöympäristön päivitysversio 10.0.21](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-21) |


### <a name="bug-fixes"></a>Ohjelmavirhekorjaukset

Tämä julkaisu sisältää seuraavat ohjelmakorjaukset.

> [!NOTE]
> Tavoitteena on, että nämä tiedot ovat käytettävissä mahdollisimman pian. Tämän artikkelin päivitys saattaa sisältää ohjelmakorjauksia, jotka on otettu käyttöön koontiversiossa tämän artikkelin alkuperäisen julkaisun jälkeen.

| Ongelman numero | Ongelma | Kuvaus |
|---|---|---|
| 598896 | Työntekijän summa ei näy, ennen kuin työntekijä on suorittanut rekisteröinnin. | **Työntekijän itsepalvelu** -sivulla edun työntekijän summaa ei näytetä. Työntekijän summa näkyy nyt **Etujen itsepalvelu** -sivulla.  |
| 613440 | **Tietojen hallinnasta** ei voi viedä tietoja | Kun projektin tietoja viedään **tietojenhallinnassa**, vienti epäonnistuu odottamattomalla tavalla. |
| 618327 | Suljetut ja tulevat kaudet näkyvät etuusilmoituksen **Raporttiparametrit**-sivulla | Jos **etuusilmoitukseen** siirrytään **työntekijän itsepalveluun**, **Raporttiparametrit**-sivulla näkyy **Sisällytettävät tietueet**- ja **Suorita taustalla** -pikavälilehdet. Nämä osat on poistettu.|
| 618326 | Virheellinen **Raporttiparametrit**-sivu näkyy **Työntekijän itsepalvelun** etuusilmoitukselle.| Kun käyttäjä siirtyy **Etuusilmoitusraportti**-kohdesivulle, käyttäjä pystyi valitsemaan suljetun tai tulevaisuuteen päivitetyn etusuunnitelman, jolloin tuloksena on tyhjä sivu. Luettelossa pitäisi näkyvä vain nykyinen etuussuunnitelmakausi. |

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
|Virhe lähetettäessä raportti sähköpostitse käyttämällä **raportin kohdetta GER**. | Etuusilmoitus voidaan määrittää käyttämään sähköpostiparametreja **Raportoinnin kohteet GER** -sivua. Kun raportin määritystä ja tulostusta viimeistellään, käyttäjä saa muotoiluvirheen eikä etuusilmoitusta lähetetä.|

## <a name="feature-management-changes"></a>Ominaisuuksien hallinnan muutokset

| Ominaisuus | Kuvaus |
|---|---|
|Suorituskyvyn kirjauskansioiden laajennettu raporttinäkymä | Tämä ominaisuus otetaan käyttöön oletusarvoisesti tässä julkaisussa. |

## <a name="coming-soon"></a>Tulossa pian

Täydellinen luettelo suunnitelluista ominaisuuksista ja niiden aikataulutetuista julkaisuista on kohdassa [Dynamics 365 Human Resourcesin vuoden 2021 2. julkaisuaallon yleiskatsaus](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/).

| Ominaisuus | Yksityiskohdat |
|---|---|
| Platform Update 10.0.22 (46) | Platform update -päivitys 10.0.22 on ajoitettu alkamaan palvelujulkaisun kanssa 1. marraskuuta 2021. Lisätietoja on [Rahoitus ja toiminnot -sovellusten version 10.0.22 alustan päivityksissä (marraskuu 2021)](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-22). |



## <a name="see-also"></a>Lisätietoja

[Human Resourcesin uudet ja muuttuneet ominaisuudet](hr-admin-whats-new.md)</br>
[Yhteenveto Dynamics 365 Human Resourcesin vuoden 2021 julkaisuaallosta 2](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/)</br>
[Päivitysprosessi](hr-admin-setup-update-process.md)</br>
[Ominaisuuksien hallinta](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
