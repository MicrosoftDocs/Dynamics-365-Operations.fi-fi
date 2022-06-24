---
title: Dynamics 365 Human Resourcesin uudet ja muuttuneet ominaisuudet 26. heinäkuuta 2021
description: Tässä artikkelissa käsitellään Microsoft Dynamics 365 Human Resourcesin 26. heinäkuuta 2021 julkaistuja uusia tai muuttuneita ominaisuuksia.
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
ms.search.validFrom: 2021-07-26
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6c7211135733f45a9841ae5a80607b01999d7c69
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8870926"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-july-26-2021"></a>Dynamics 365 Human Resourcesin uudet ja muuttuneet ominaisuudet 26. heinäkuuta 2021

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Tässä artikkelissa käsitellään Dynamics 365 Human Resourcesin uusia, muuttuneita tai tulevia toimintoja.

Lisätietoja päivitysprosessista ja aikataulusta on kohdassa [Päivitysprosessi](hr-admin-setup-update-process.md).

Lisätietoja uusista ominaisuuksista ja niiden odotetuista yleisen saatavuuden päivämääristä on kohdassa [Dynamics 365 Human Resourcesin vuoden 2021 2. julkaisuaallon yleiskatsaus](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>Tässä julkaisussa

Tämä julkaisu sisältää seuraavat uudet ominaisuudet ja ohjelmakorjaukset. Muutokset koskevat koontiversion numeroa 8.1.4384.

### <a name="new-features"></a>Uudet ominaisuudet

Seuraavat ominaisuudet ovat yleisesti saatavana tässä julkaisussa.

| Ominaisuus | Julkaisusuunnitelma | Dokumentaatio |
| --- | --- | --- |
| Ympäristön update 10.0.20 -päivitys | -- | [Taloushallinnon ja toimintojen sovellusten (elokuu 2021) käyttöympäristön päivitysversio 10.0.20](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-20) |

### <a name="bug-fixes"></a>Ohjelmavirhekorjaukset

Tämä julkaisu sisältää seuraavat ohjelmakorjaukset.

> [!NOTE]
> Tavoitteena on, että nämä tiedot ovat käytettävissä mahdollisimman pian. Tämän artikkelin päivitys saattaa sisältää ohjelmakorjauksia, jotka on otettu käyttöön koontiversiossa tämän artikkelin alkuperäisen julkaisun jälkeen.

| Ongelman numero | Ongelma |  Kuvaus |
| --- | --- | --- |
| 600422 | Palkanlaskennan osoitteen vahvistus epäonnistuu maksuvalmiuden osalta. | Vahvistus on päivitetty edellyttämään vain yksi Palkanlaskennan kotipaikan sijainti -osoite ja yksi Palkanlaskennan työpaikan sijainti -osoite. |
| 601226 | Tietojen integrointiongelma: Palkanlaskennan integroinnin vientiprojektissa ei ole vaihtoehto täydelliselle siirrolle | Palkanlaskennan Ceridian DayForce -integrointi teki lisäävän siirron täydellisen siirron sijaan. Ceridian edellyttää, että siirto on aina täydellinen. Tämä ongelma on nyt korjattu, eivätkä tietojen vientiprojektin yksiköt enää vaihdu lisäävään siirtoon. |
| 602272 | Työntekijän itsepalvelu -työtilaan lisätyt ruudut puuttuvat nyt eikä siihen voi enää lisätä ruutuja | Työntekijän itsepalvelun mukauttamisongelma on korjattu. Näkymään voidaan nyt lisätä uusia ruutuja, ja mahdolliset aiemmin luodut mukautukset näkyvät käyttäjille |
| 600711 | Puolen päivän määrityksen valintakenttä on otettu käyttöön koko päivän lomapyynnöille | Tämä ongelma on nyt korjattu, puolen päivän määrityskenttä otetaan käyttöön vain, kun työntekijät valitsevat lomatyypin, jossa puolen päivän määritys on käytössä ja puoli päivää on valittu arvo |
| 602208 | Jaksotuksen arvoyksiköt näyttävät tunnit päivien sijaan | Tämä ongelma on nyt korjattu. **Poissaoloaika**-lomakkeen **Jaksotusarvo**-sarakkeessa näkyy nyt oikea lomayksikkö (tunnit tai päivät). |

## <a name="in-preview"></a>Esiversiossa

Seuraavat uudet ominaisuudet ovat esiversioita. Lisätietoja ominaisuuksien ottamisesta käyttöön tai poistamisesta käytöstä on kohdassa [Ominaisuuksien hallinta](hr-admin-manage-features.md).

| Ominaisuus | Julkaisusuunnitelma | Dokumentaatio |
| --- | --- | --- |
| Etujen hallinnan työtila | [Etujen hallinnan työtila (esikatselu)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Etujen hallinnan työtila](hr-benefits-management-workspace.md) |
| Ota käyttöön palkanlaskennan yksinkertaistettu integrointi (Palkanlaskennan integroinnin ohjelmointirajapinnat) | [Yksinkertaisen integroinnin käyttöönotto palkanlaskennan palveluntarjoajien kanssa](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-simplified-integration-payroll-providers) | [Palkanlaskennan integroinnin ohjelmointirajapinta](hr-admin-integration-payroll-api-introduction.md)|
|  Poissaolojen hallinnan esimiehen käyttöön ottaminen | [Poissaolojen hallinnan esimiehen käyttöön ottaminen](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-absence-manager-manage-leave) | Tässä versiossa päivitetään poissaolojen hallintatyötilan näkymä. Lisätietoja on kohdassa [Poissaolojen hallintaroolin määrittäminen](https://go.microsoft.com/fwlink/?linkid=2168107).|
|  Määritä liitteen tarve lomatyyppiä kohden | [Määritä liitteen tarve lomatyyppiä kohden](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/mandate-attachments-specific-leave-types) |[Loma- ja poissaolotyyppien määrittäminen](https://go.microsoft.com/fwlink/?linkid=2168108)|
|  Määritä lomayksiköt lomatyypin mukaan | [Määritä lomayksiköt lomatyypin mukaan](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/configure-leave-units-per-leave-type) |[Loma- ja poissaolotyyppien määrittäminen](https://go.microsoft.com/fwlink/?linkid=2168215)|
| Merkitse työntekijät valmiiksi maksettavaksi | [Merkitse työntekijät valmiiksi maksettavaksi](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-employees-be-marked-as-ready-pay) | [Valmis maksettavaksi](/dynamics365/human-resources/hr-compensation-payroll) |

## <a name="coming-soon"></a>Tulossa pian

Täydellinen luettelo suunnitelluista ominaisuuksista ja niiden aikataulutetuista julkaisuista on kohdassa [Dynamics 365 Human Resourcesin vuoden 2021 2. julkaisuaallon yleiskatsaus](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/).

## <a name="see-also"></a>Lisätietoja

[Human Resourcesin uudet ja muuttuneet ominaisuudet](hr-admin-whats-new.md)</br>
[Yhteenveto Dynamics 365 Human Resourcesin vuoden 2021 julkaisuaallosta 2](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/)</br>
[Päivitysprosessi](hr-admin-setup-update-process.md)</br>
[Ominaisuuksien hallinta](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
