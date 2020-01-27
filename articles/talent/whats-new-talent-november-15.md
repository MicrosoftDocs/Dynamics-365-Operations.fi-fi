---
title: Dynamics 365 Talent - Core HR:n uudet tai muuttuneet ominaisuudet (15. marraskuuta 2018)
description: Tässä ohjeaiheessa käsitellään Microsoft Dynamics 365 Talent - Core HR:n uusia tai muuttuneita ominaisuuksia.
author: Darinkramer
manager: AnnBe
ms.date: 11/15/2018
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
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 1a7598db1dc4c11864cf5f5a73d00672ceb66e8c
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/06/2019
ms.locfileid: "2897463"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent---core-hr-november-15-2018"></a>Dynamics 365 Talent - Core HR:n uudet tai muuttuneet ominaisuudet (15. marraskuuta 2018)

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
