---
title: Dynamics 365 Talent - Core HR:n uudet tai muuttuneet ominaisuudet (16. lokakuuta 2018)
description: Tässä ohjeaiheessa käsitellään Microsoft Dynamics 365 Talent - Core HR:n uusia tai muuttuneita ominaisuuksia.
author: Darinkramer
manager: AnnBe
ms.date: 10/22/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-10-22
ms.dyn365.ops.version: Talent
ms.openlocfilehash: d5f2aea5fcc81d0b4c1d8a392a3e56c888440a94
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4461016"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent---core-hr-october-16-2018"></a>Dynamics 365 Talent - Core HR:n uudet tai muuttuneet ominaisuudet (16. lokakuuta 2018)

**Koontiversio 8.1.1067**

Tässä ohjeaiheessa käsitellään Core HR -ohjelman uusia tai muuttuneita ominaisuuksia.

## <a name="allow-managers-to-update-time-off-requests"></a>Esimiehet saavat päivittää poissaolopyynnöt

Työntekijän poissaolopyyntöjä on ehkä päivitettävä sen jälkeen, kun ne hyväksytty työnkulun kautta. Monissa tapauksissa esimies tekee nämä päivityksen työntekijän puolesta. Tämän uuden ominaisuuden ansiosta esimiehet voivat päivittää tai peruuttaa poissaolopyynnöt työntekijöiden puolesta. Toimintoa hallitaan **Tee jonkun puolesta** -parametrilla, joka voidaan määrittää **Henkilöstöparametrit**-sivulla. 
 
## <a name="allow-hr-to-update-time-off-requests"></a>Henkilöstöhallinto saa päivittää poissaolopyynnöt

Edellä kuvatun toiminnon tavoin henkilöstöhallinnon on ehkä päivitettävä työntekijän poissaolopyyntöjä sen jälkeen, kun ne on jo hyväksytty työnkulun kautta. Henkilöstöhallinnon käyttäjät voivat päivittää poissaolopyynnöt tällä ominaisuudella. Toiminto otetaan käyttöön **Henkilöt**-työtilassa ja **Työntekijä**-sivulla uudella **Näytä poissaoloaika** -asetuksella. Henkilöstöhallinnon käyttäjät voivat tarkastella näillä sivuilla pyyntöjä ja päivittää poissaolotapahtumia samalla tavoin kuin esimiehet suorittavat näitä tehtäviä.

Tämän toiminnon käyttöä hallitaan seuraavalla suojausvelvollisuudella:
- Velvollisuus: Ylläpidä työntekijäkohtaisia loma- ja poissaoloprosesseja.
- Käyttöoikeus: Ylläpidä kaikkien työntekijöiden loma- ja poissaolopyyntöjä.

## <a name="other-changes"></a>Muut muutokset
Tässä versiossa on tehty seuraavat päivitykset:
- Työntekijän työhönottotoimintoja on muutettu siten, että eivät enää juutu **Työnkulku valmis** -tilaan.
- Työntekijätietue voidaan nyt luoda ilman työsuhteen alkamispäivämäärää.
- Työntekijän itsepalvelu -kohdassa näkyvän kurssin Dynamics 365 Talent -rekisteröitymispäivässä käytetään nyt aikavyöhykepoikkeamaa.
- Excel-tiedostot voidaan tuoda useita kertoja ilman virheilmoituksia, kun käytössä on **työntekijäyksikkö**.

## <a name="known-issue"></a>Tunnettu ongelma

- **Ongelma**: kun työntekijään lisätään uusi liite, **Uusi**- ja **Muokkaa**-painikkeet näkyvät harmaina. 
- **Ongelman kiertäminen:** Varmista ennen liitesivun avaamista, että **Työntekijä**-sivun tietoruudut on suljettu. Jos tietoruudut ovat suljettuja **Työntekijä**-sivua ladattaessa, liitepainikkeet otetaan käyttöön. (Tämä ongelma korjataan seuraavassa ympäristöpäivityksessä.)


[!INCLUDE[footer-include](../includes/footer-banner.md)]