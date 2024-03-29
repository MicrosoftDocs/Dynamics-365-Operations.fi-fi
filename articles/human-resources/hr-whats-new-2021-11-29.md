---
title: Dynamics 365 Human Resourcesin uudet tai muuttuneet ominaisuudet 19. marraskuuta 2021
description: Tässä artikkelissa käsitellään erillisen Microsoft Dynamics 365 Human Resourcesin 19. marraskuuta 2021 julkaistuja uusia tai muuttuneita ominaisuuksia.
author: marcelbf
ms.date: 12/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-12-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d3e08432a4ce4d73cd67ad839191abe9f6e691a6
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8886070"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-november-19-2021"></a>Dynamics 365 Human Resourcesin uudet tai muuttuneet ominaisuudet 19. marraskuuta 2021

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Tässä artikkelissa käsitellään Microsoft Dynamics 365 Human Resourcesin uusia, muuttuneita tai tulevia toimintoja.

Lisätietoja päivitysprosessista ja aikataulusta on kohdassa [Päivitysprosessi](hr-admin-setup-update-process.md).

Lisätietoja uusista ominaisuuksista ja niiden odotetuista yleisen saatavuuden päivämääristä on kohdassa [Dynamics 365 Human Resourcesin vuoden 2021 2. julkaisuaalto](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>Tässä julkaisussa

Tämä julkaisu sisältää seuraavat ohjelmakorjaukset. Muutokset koskevat koontiversion numeroa 8.1.4591.

### <a name="bug-fixes"></a>Ohjelmavirhekorjaukset

Tämä julkaisu sisältää seuraavat ohjelmakorjaukset.

> [!NOTE]
> Tavoitteena on, että nämä tiedot ovat käytettävissä mahdollisimman pian. Tämän artikkelin päivitys saattaa sisältää ohjelmakorjauksia, jotka on otettu käyttöön koontiversiossa tämän artikkelin alkuperäisen julkaisun jälkeen.

| Ongelman numero | Ongelma | Kuvaus |
|---|---|---|
| 626178 | Siirtyminen puuttuu **esimiehen itsepalvelun** työntekijän ruuduista | Tämä ongelma on nyt korjattu. Siirtyminen on käytettävissä, jos haluat nähdä raportin tiedot **Esimiehen itsepalvelussa**. |
| 632573 | **Kurssia** tallennettaessa ei ole oikeellisuustarkistusvirhettä. | Tämä ongelma on nyt korjattu. Kun luot kurssin, jonka **osallistujien vähimmäismäärä** on suurempi kuin 0, voiton voi tallentaa silloinkin, kun **osallistujien enimmäismäärä on** 0. |
| 615955 | Virhe "Kentän **tarkoitus** on täytettävä" luotaessa uutta työhönottopyynnön sijaintia. | Kun luot osoitteen uudelle työhönottopyynnön sijainnille, saat virheilmoituksen: "Tarkoitus-kenttä on täytettävä." **Tarkoitus**-kenttä ei kuitenkaan ole käytettävissä sivulla. |
| 620797 | Tyhjä **Sukupuoli**-kenttävirhe on harhaanjohtava | Kun sukupuolta ei ole syötetty henkilökohtaiselle yhteyshenkilölle, raportissa näkyy teksti "Napsauta tai napauta tätä tekstiä." Se tarkoittaa, ettei kenttään voi kirjoittaa mitään. |
| 620800 | Etulausekelinkki on piilotettu | Etulauseketta ei voi oletusarvon mukaan tarkastella **Työntekijän itsepalvelussa**.  Linkki on lisätty **Työntekijän itsepalvelun** oikealle puolelle **Linkit**-osassa |
| 629778 | CDS-integraatioon liittyvät suorituskykyongelmat. | Varmennukseen liittyvä pyyntö on aiheuttanut suorituskykyongelman. |

## <a name="in-preview"></a>Esiversiossa

Seuraavat uudet ominaisuudet ovat esiversioita. Lisätietoja ominaisuuksien ottamisesta käyttöön tai poistamisesta käytöstä on kohdassa [Ominaisuuksien hallinta](hr-admin-manage-features.md).

| Ominaisuus | Julkaisusuunnitelma | Dokumentaatio |
|---|---|---|
| Etujen hallinnan työtila | [Etujen hallinnan työtila (esikatselu)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Etujen hallinnan työtila](hr-benefits-management-workspace.md) |


## <a name="coming-soon"></a>Tulossa pian
Täydellinen luettelo suunnitelluista ominaisuuksista ja niiden aikataulutetuista julkaisuista on kohdassa [Dynamics 365 ja toimialan pilvet: vuoden 2021 2. julkaisuaalto](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/).

[!INCLUDE[footer-include](../includes/footer-banner.md)]
