---
title: Dynamics 365 Talent - Core HR:n uudet tai muuttuneet ominaisuudet (27. marraskuuta 2018)
description: Tässä ohjeaiheessa käsitellään Microsoft Dynamics 365 Talent - Core HR:n uusia tai muuttuneita ominaisuuksia.
author: Darinkramer
manager: AnnBe
ms.date: 11/27/2018
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
ms.search.validFrom: 2018-11-27
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 1d6b5f5f7b62c400679df5eb014dee05f02e11d0
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4461022"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent---core-hr-november-27-2018"></a>Dynamics 365 Talent - Core HR:n uudet tai muuttuneet ominaisuudet (27. marraskuuta 2018)

**Koontiversio 8.1.2064**

Tässä ohjeaiheessa käsitellään Core HR -ohjelman uusia tai muuttuneita ominaisuuksia.


## <a name="changes"></a>Muutokset

### <a name="unable-to-create-a-note-in-case-management"></a>Huomautusta voi luoda palvelupyyntöjen hallinnassa

Palvelupyyntöjen hallinnan tapauslokiin liittyvän huomautuksen luontiin tai muokkaukseen liittyvään ongelmaan on tehty muutos.

### <a name="misspelled-word-on-the-analytics-tab-in-the-compensation-workspace"></a>Kirjoitusvirhe kompensaatiotyötilan analytiikkavälilehden sanassa 

Kompensaatiotyötilan kompensaation analyysikaavion etnisen alkuperän kirjoitusvirhe on korjattu.

### <a name="employee-self-service-workspace-not-displaying-when-a-user-isnt-assigned-to-a-worker"></a>Työntekijän itsepalvelutyötilan ei näy, kun käyttäjää ei ole määritetty työntekijälle 

Muutos tilanteessa, jossa **Työntekijän itsepalvelu** -työtila on valittu sellaisen käyttäjän käynnistyksen ensimmäiseksi sivuksi, jota ei ole määritetty työntekijäksi. Tässä tilanteessa näytetään oletuskoontinäyttö.

### <a name="leave-and-absence-error-object-reference-not-set-to-an-instance-of-an-object"></a>Loma- ja poissaolovirhe: objektiviitettä ei ole määritetty objektin esiintymälle

Virhe on korjattu tekemällä muutos lomaan ja poissaoloon sen jälkeen, kun loma- ja poissaolotietueet on hyväksytty **Minulle määritetyt työnimikkeet** -luettelossa.

### <a name="unable-to-recall-an-image-workflow"></a>Kuvatyönkulkua ei voi peruuttaa

Kun kuvatyönkulku on peruutettu, työnkulun tilaksi määritetään peruutettu ja aiemmin luotu pyyntö voidaan poistaa työntekijän itsepalvelutyötilassa.

### <a name="rehired-employees-or-contractors-show-up-multiple-times-after-termination"></a>Uudelleenpalkatut työntekijät ja urakoitsijat näkyvät useita kertoja työsuhteen päättymisen jälkeen 

Tämän päivityksen jälkeen uudelleenpalkatut työntekijät, joiden työsuhde on päättynyt, näkyvät vain kerran poistuneiden luettelossa. 

## <a name="known-issue"></a>Tunnettu ongelma

- **Ongelma**: kun työntekijään lisätään uusi liite, **Uusi**- ja **Muokkaa**-painikkeet näkyvät harmaina. 
- **Ongelman kiertäminen:** Varmista ennen liitesivun avaamista, että **Työntekijä**-sivun tietoruudut on suljettu. Jos tietoruudut ovat suljettuja **Työntekijä**-sivua ladattaessa, liitepainikkeet otetaan käyttöön. (Tämä ongelma korjataan seuraavassa ympäristöpäivityksessä.)


[!INCLUDE[footer-include](../includes/footer-banner.md)]