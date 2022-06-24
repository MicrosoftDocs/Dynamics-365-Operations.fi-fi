---
title: Dynamics 365 Human Resourcesin uudet ja muuttuneet ominaisuudet 12. heinäkuuta 2021
description: Tässä artikkelissa käsitellään Microsoft Dynamics 365 Human Resourcesin 12. heinäkuuta 2021 julkaistuja uusia tai muuttuneita ominaisuuksia.
author: marcelbf
ms.date: 07/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-07-12
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 259004773c4e5a7d8865d563da9bcfea3a116632
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8870955"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-july-12-2021"></a>Dynamics 365 Human Resourcesin uudet ja muuttuneet ominaisuudet 12. heinäkuuta 2021

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Tässä artikkelissa käsitellään Dynamics 365 Human Resourcesin uusia, muuttuneita tai tulevia toimintoja.

Lisätietoja päivitysprosessista ja aikataulusta on kohdassa [Päivitysprosessi](hr-admin-setup-update-process.md).

Lisätietoja uusista ominaisuuksista ja niiden odotetuista yleisen saatavuuden päivämääristä on kohdassa [Dynamics 365 Human Resourcesin vuoden 2021 1. julkaisuaallon yleiskatsaus](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>Tässä julkaisussa

Tämä julkaisu sisältää seuraavat uudet ominaisuudet ja ohjelmakorjaukset. Muutokset koskevat koontiversion numeroa 8.1.4353.

### <a name="new-features"></a>Uudet ominaisuudet

Seuraavat ominaisuudet ovat yleisesti saatavana tässä julkaisussa.

| Ominaisuus | Julkaisusuunnitelma | Dokumentaatio |
| --- | --- | --- |
|  Palveluvuosien näytön vaihto | |Tämän ominaisuuden avulla voit käyttää eri päivämääriä työvuosien laskentaan, joka näkyy **Virtaviivaistettu työntekijän syöttäminen** -sivulla ja **Henkilöt**-sivulla.  Tämä on käytettävissä [henkilöstöhallinnon parametreissa](/dynamics365/human-resources/hr-setup-parameters). |


### <a name="bug-fixes"></a>Ohjelmavirhekorjaukset

Tämä julkaisu sisältää seuraavat ohjelmakorjaukset.

> [!NOTE]
> Tavoitteena on, että nämä tiedot ovat käytettävissä mahdollisimman pian. Tämän artikkelin päivitys saattaa sisältää ohjelmakorjauksia, jotka on otettu käyttöön koontiversiossa tämän artikkelin alkuperäisen julkaisun jälkeen.

| Ongelman numero | Ongelma |  Kuvaus |
| --- | --- | --- |
| 595871 | Human Resourcesin Tietoja-ruudussa on virheellistä Dataverse-terminologiaa | Common Data Servicen tuotemerkkiä uudistettaessa Dataverseksi terminologia on päivitetty Microsoft Dynamics 365 Human Resources -tietoruudussa (**Ohje ja tuki > Tietoja**). |
| 598676 | Virtaviivaistetun työntekijän syöttölomakkeen ohitustehtävä voi luoda virheen, kun sitä käytetään tallennetussa näkymässä| Jos **Työntekijä**-sivulla Virtaviivaistettu työntekijän syöttäminen -ominaisuus on käytössä, sovellus saattaa epäonnistua, jos **Aina avoinna muokattavaksi** on määritetty tallennetussa näkymässä. |
| 592344 |Tehtävän työntekijöiden kokoonpano -osan tulisi olla vain luku -muotoa, kun etujen hallinta on käytössä | Työntekijöiden kokoonpanotiedot luodaan käyttämällä vanhoja etuustoimintoja.  Kun etujen hallinta on käytössä, kentät ovat vain luku -kenttiä. Kun etujen hallinta on käytössä ja **Piilota vanhat etuuslomakkeet** -asetus on **Kyllä** jaetuissa HR-parametreissa, **Työntekijöiden kompensaatio** -välilehti piilotetaan. |
| 598617 | **HcmDiscussion**-lomakkeen aktivointivälilehti aiheuttaa päättymättömän silmukan, kun mukautuksia käytetään | Kun sekä ruudukko- että tietonäkymässä on käytössä **Aina avoinna muokkausta varten**, ohitetun tehtävämetodin välilehden aktivoiva koodi on ristiriidassa mukautuksen kanssa siitä, millä ohjausobjektilla olisi oltava tarkennus, mikä luo päättymättömän silmukan. |
| 593553 | Kirjauskansion päivämäärä -kenttä Suorituskykykirjauskansiossa näkyy UTC-muodossa | **Kirjauskansion päivämäärä** -kenttä suorituskykykirjauskansioissa näyttää UTC-aikavyöhykkeen järjestelmän päivämääräasetuksissa määritetyn aikavyöhykkeen sijaan, minkä vuoksi päivämäärä on joillakin aikavyöhykkeillä väärä. |
| 586930 | Suoritustavoitteiden toimintojen avaaminen avaa aivan toisen tietueen | Kun Suorituskykykirjauskansioiden laajennettujen raporttien katseluominaisuus on otettu käyttöön Ominaisuuksien hallinnassa, suorituskykytavoitteiden valitseminen laajennetuille raporteille **Oma ryhmä** -välilehdellä **Työntekijän itsepalvelussa** avaa työntekijän tavoitteet valitun työntekijän tavoitteiden asemesta. |
| 569959 |  HcmPositionWorkerAssignmentV2-entiteetti ei määritä työntekijää tehtävään | Käyttäjät saivat virheen lisättäessä tehtävänmääritystietuetta entiteetin kautta ja julkaiseminen epäonnistui. |
| 582259 | VETS 4212 -raportti käyttää vuoden 2017 lomaketta vuoden 2020 lomakkeen sijaan | Päivitetty vuoden 2020 muotoon.  Jos haluat ladata uuden muodon, siirry **Raporttimäärityksiin** ja poista VETS-4212-raportti vasemmasta sarakkeesta. Siirry kohtaan **Sähköinen raportointi - Arkistot- HR-resurssit** ja valitse **Avaa**.  Valitse **VETS-4212 PDF-tuloste** ja valitse sitten **Tuo**.|


## <a name="in-preview"></a>Esiversiossa

Seuraavat uudet ominaisuudet ovat esiversioita. Lisätietoja ominaisuuksien ottamisesta käyttöön tai poistamisesta käytöstä on kohdassa [Ominaisuuksien hallinta](hr-admin-manage-features.md).

| Ominaisuus | Julkaisusuunnitelma | Dokumentaatio |
| --- | --- | --- |
| Etujen hallinnan työtila | [Etujen hallinnan työtila (esikatselu)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Etujen hallinnan työtila](hr-benefits-management-workspace.md) |
| Ota käyttöön palkanlaskennan yksinkertaistettu integrointi (Palkanlaskennan integroinnin ohjelmointirajapinnat) | [Yksinkertaisen integroinnin käyttöönotto palkanlaskennan palveluntarjoajien kanssa](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-simplified-integration-payroll-providers) | [Palkanlaskennan integroinnin ohjelmointirajapinta](hr-admin-integration-payroll-api-introduction.md)|
|  Poissaolojen hallinnan esimiehen käyttöön ottaminen | [Poissaolojen hallinnan esimiehen käyttöön ottaminen](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-absence-manager-manage-leave) | [Poissaolopäällikön roolin määrittäminen](https://go.microsoft.com/fwlink/?linkid=2168107)|
|  Määritä liitteen tarve lomatyyppiä kohden | [Määritä liitteen tarve lomatyyppiä kohden](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/mandate-attachments-specific-leave-types) |[Loma- ja poissaolotyyppien määrittäminen](https://go.microsoft.com/fwlink/?linkid=2168108)|
|  Määritä lomayksiköt lomatyypin mukaan | [Määritä lomayksiköt lomatyypin mukaan](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/configure-leave-units-per-leave-type) |[Loma- ja poissaolotyyppien määrittäminen](https://go.microsoft.com/fwlink/?linkid=2168215)|
| Merkitse työntekijät valmiiksi maksettavaksi | [Merkitse työntekijät valmiiksi maksettavaksi](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-employees-be-marked-as-ready-pay) | [Valmis maksettavaksi](/dynamics365/human-resources/hr-compensation-payroll) |

## <a name="coming-soon"></a>Tulossa pian

| Ominaisuus | Lisätietoja |
| --- | --- |
| Platform Update 10.0.20 (44) | Platform update -päivitys 10.0.20 on ajoitettu alkamaan julkaisun kanssa 26. heinäkuuta 2021. Lisätietoja on [Rahoitus ja toiminnot -sovellusten version 10.0.20 alustan päivityksissä (elokuu 2021)](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-20). |

Täydellinen luettelo suunnitelluista ominaisuuksista ja niiden aikataulutetuista julkaisuista on kohdassa [Dynamics 365 Human Resourcesin vuoden 2021 1. julkaisuaallon yleiskatsaus](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="see-also"></a>Lisätietoja

[Human Resourcesin uudet ja muuttuneet ominaisuudet](hr-admin-whats-new.md)</br>
[Yhteenveto Dynamics 365 Human Resourcesin vuoden 2021 julkaisuaallosta 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)</br>
[Päivitysprosessi](hr-admin-setup-update-process.md)</br>
[Ominaisuuksien hallinta](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
