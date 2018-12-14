---
title: Dynamics 365 for Talent Core HR:n uudet tai muuttuneet ominaisuudet (15.11.2018)
description: "Tässä aiheessa käsitellään Microsoft Dynamics 365 for Talent Core HR -ohjelman uusia tai muuttuneita ominaisuuksia."
author: Darinkramer
manager: AnnBe
ms.date: 11/15/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: Talent
ms.translationtype: HT
ms.sourcegitcommit: 3cc19a8e5f726495e698a3a2f4ccce7460a61657
ms.openlocfilehash: 0e9de5e36e67941ab09c773a63b0e7045105a07e
ms.contentlocale: fi-fi
ms.lasthandoff: 12/04/2018

---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-november-15-2018"></a>Dynamics 365 for Talent Core HR:n uudet tai muuttuneet ominaisuudet (15.11.2018)

[!include [banner](includes/banner.md)]

**Koontiversio 8.1.2045**

Tässä ohjeaiheessa käsitellään Core HR -ohjelman uusia tai muuttuneita ominaisuuksia.

## <a name="other-changesfixes"></a>Muut muutokset ja korjaukset

### <a name="unable-to-change-employees-current-position-to-a-future-open-position"></a>Työntekijän nykyistä toimea ei voi muuttaa tulevaksi avoimeksi toimeksi

Tehdyn muutoksen avulla toimen siirrot voidaan käyttöön, kun toimi on vapaana vain tulevaisuudessa. 

### <a name="position-does-not-display-when-creating-a-new-employee"></a>Toimi ei näy uutta työntekijää luotaessa

Tehdyn muutoksen avulla näytetään kaikki avoimet toimet, jotka on käytettävissä, kun uusi työntekijöitä palkataan Talentissa. Tämä sisältää myös historialliset toimet tai toimet, joiden päivämäärä on tulevaisuudessa. Toimet näkyvät nyt oikein työsuhteen aloituspäivän perusteella. 

### <a name="termination-date-is-displaying-based-on-user-settings"></a>Työsuhteen päättymispäivän näyttäminen käyttäjäasetusten perusteella

Entisten työntekijöiden luetteloon tehdyn muutoksen avulla työsuhteen päättymispäivää tarkasteltaessa otetaan huomioon työntekijän ensisijaisen aikavyöhykkeen aiheuttamat aikavyöhykepoikkeamat.

### <a name="work-items-assigned-to-me-links-not-displaying-the-correct-information"></a>Oikeat tiedot eivät näyt Minulle määritetyt työnimikkeet -linkeissä

Tämän muutoksen ansiosta siirtyminen luettelon yksittäisten työnimikkeiden tietoihin näyttää oikeat tiedot valitusta nimikkeestä. Tämä ongelma esiintyi vain suojauksen lisäasetuksia käytettäessä.


## <a name="known-issue"></a>Tunnettu ongelma

- **Ongelma**: kun työntekijään lisätään uusi liite, **Uusi**- ja **Muokkaa**-painikkeet näkyvät harmaina. 
- **Ongelman kiertäminen:** Varmista ennen liitesivun avaamista, että **Työntekijä**-sivun tietoruudut on suljettu. Jos tietoruudut ovat suljettuja **Työntekijä**-sivua ladattaessa, liitepainikkeet otetaan käyttöön. (Tämä ongelma korjataan seuraavassa ympäristöpäivityksessä.)

