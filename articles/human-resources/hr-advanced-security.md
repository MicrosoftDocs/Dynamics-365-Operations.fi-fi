---
title: Työntekijätietojen käyttöoikeuden rajoittaminen yrityksen mukaan
description: Tässä artikkelissa kerrotaan, miten työntekijän käyttöoikeudet määritetään yrityksen mukaan.
author: twheeloc
ms.date: 11/28/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmSharedParameters, HcmPersonnelManagementWorkspace
audience: Application User
ms.custom: 51891
ms.assetid: c7d8f58c-d78a-4035-abbf-2b0ce16109fe
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: fadd2c34d31bbd259255596c06a8e7517f7a774b
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/16/2022
ms.locfileid: "9780389"
---
# <a name="restrict-access-to-workers-by-legal-entity"></a>Työntekijätietojen käyttöoikeuden rajoittaminen yrityksen mukaan

Tässä artikkelissa kerrotaan, miten työntekijän käyttöoikeudet määritetään yrityksen mukaan.

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Työntekijät on työskentelevät yrityksissä. Seuraavassa on muutamia esimerkkejä:

- Aaron Con on töissä yrityksessä USSI.
- Ahmed Barnett on töissä yrityksessä USMF.
- Alicia Thornber työskentelee yrityksissä GLSI ja USMF.

Riippuen käyttäjän roolista yrityksessä he saattavat tarvita yrityksen kaikkien työntekijöiden tarkasteluoikeuden. Vaihtoehtoisesti käyttäjän oikeuksia ehkä rajattava, jotta hän voi tarkastella vain sen yrityksen työntekijöitä, joka käyttöoikeudet tällä on. Jos haluat määrittää, kenen työntekijän tietoja käyttäjä voi tarkastella, valitse **Rajoita työntekijätietojen käyttöoikeus** -parametri **Henkilöstöhallinnon jaetut parametrit** -sivulla.

Käyttäjällä voi olla esimerkiksi oikeus käyttää **Työntekijä**-sivua ja vain yritystä USMF. Tässä tapauksessa käyttäjä voi tarkastella edellisen luettelon seuraavien työntekijöiden tietoja:

- Jos työntekijätietojen rajoittamistoimintoa ei ole otettu käyttöön, käyttäjä voi tarkastella Aaronin, Ahmedin ja Alician tietoja.
- Jos toiminto on otettu käyttöön, käyttäjä voi tarkastella vain Alician ja Ahmedin tietoja, koska he ovat myös töissä yrityksessä USMF.

Näkyvissä olevat tiedot vaihtelevat käytettävän sovelluksen mukaan.

## <a name="dynamics-365-human-resources-stand-alone"></a>Erillinen Dynamics 365 Human Resources

Jos työntekijätietojen käyttöoikeuksien rajoittamistoiminto on käytössä, rajoitettu käyttäjä näkee tyhjän arvon joissakin työntekijän nimen sisältävissä luetteloissa.

Esimerkiksi käyttäjä, jolla on vain yrityksen USMF käyttöoikeus, voi tehdä seuraavaa:

- **Aktiiviset toimet** -luettelossa Aaronin **Työntekijä**-sarake on tyhjä, koska käyttäjällä ei ole yrityksen USSI työntekijöiden tietojen käyttöoikeutta.
- Jos käyttäjä valitsee työntekijän nimen, näkyviin tulee tyhjä **Työntekijä**-sivu.

## <a name="dynamics-365-human-resources-on-finance-infrastructure"></a>Dynamics 365 Human Resources Financen infrastruktuurissa

Jos työntekijätietojen käyttöoikeuksien rajoittamistoiminto on käytössä, rajoitettu käyttäjä näkee työntekijän nimen joissakin luetteloissa.

Esimerkiksi käyttäjä, jolla on vain yrityksen USMF käyttöoikeus, voi tehdä seuraavaa:

- **Aktiiviset toimet** -luettelossa **Työntekijä**-sarakkeessa on Aaronin nimi. Jos käyttäjä valitsee työntekijän nimen osoittamalla, näytetään vain nimi ja otsikko.
- Jos käyttäjä valitsee työntekijän nimen, näkyviin tulee tyhjä **Työntekijä**-sivu.

> [!TIP]
> Jos käytössä on Dynamics 365 Human resources Financen infrastruktuurissa ja haluat rajoittaa käyttäjien työntekijätietojen tarkasteluoikeuksia näyttämällä tyhjän sivun, voit lisätä käyttäjärooleille **Rajoita työntekijätietojen käyttöoikeuksia** -suojausoikeuden **Suojauksen määritys** -sivulla.

Kun tämä toiminto otetaan käyttöön, käyttöoikeudet määritetään kullekin rajoitettavalle käyttäjille muutaman lisävaiheen avulla.

1. Valitse käyttäjä **Käyttäjät**-sivulta.
2. Valitse käyttäjälle rooli. **Määritä organisaatiot** -vaihtoehto tulee näkyviin.
3. Valitse **Määritä organisaatiot**.
4. Valitse uudelta sivulta **Myönnä pääsy tiettyihin organisaatioihin yksittäin** ja valitse sitten organisaatiot, joihin käyttäjällä tulisi olla pääsy.
5. Toista vaiheet 2–4 käyttäjän kaikille muille rooleille, mukaan lukien järjestelmäkäyttäjän roolin.

> [!NOTE]
> Yritysten, joihin käyttäjällä on pääsy, on oltava samoja käyttäjän kaikissa rooleissa.
