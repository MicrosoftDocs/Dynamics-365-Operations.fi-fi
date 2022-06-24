---
title: Commerce-luetteloiden laajennettavuusvaikutus yritysten välisiä mukautuksia varten
description: Tässä artikkelissa kuvataan B2B-ominaisuuden Commerce-luetteloiden laajennettavuusvaikutuksia Microsoft Dynamics 365 Commercessa.
author: ashishmsft
ms.date: 04/28/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2022-02-28
ms.openlocfilehash: f21d3375db69dd412325d00261bfc18e26d0c257
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8849012"
---
# <a name="extensibility-impact-of-commerce-catalogs-for-b2b-customizations"></a>Commerce-luetteloiden laajennettavuusvaikutus yritysten välisiä mukautuksia varten

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Tässä artikkelissa kuvataan **B2B-ominaisuuden Commerce-luetteloiden** laajennettavuusvaikutuksia Microsoft Dynamics 365 Commercessa.

Jos haluat laajentaa luettelokontekstin mukautetuille skenaarioille, mukautuksesi on ehkä päivitettävä. Tämä päivitys noudattaa vakioprosessia, jota asiakkaiden on noudatettava, koska mukautukset eivät ehkä tue automaattisesti uusimpia ominaisuuksia päivitysten jälkeen. Jos mukautuksissa on uusia ominaisuuksia tai virheenkorjauksia, suosittelemme, että päivität mukautuskoodin vastaavasti. Päivitys muistuttaa muutoksia, jotka Microsoft on voinut tehdä ydinkoodiin.

Tarkista seuraavien mukautustapausten perusteella, täytyykö mukautukset päivittää.

> [!NOTE]
> - Kaikkien markkinoinnin sovellusten ohjelmointiliittymän (API:n) tulee olla luettelosta tietoinen. Siksi on tärkeää välittää **CatalogID**-parametri.
> - Oletusluettelo (**CatalogID**=**0**) oletusluettelo ei ole sallittu luettelo kirjautuneille B2B-käyttäjille. Sen vuoksi kaikki arvoa "0" tai oletusarvoa käyttävät API-kutsut epäonnistuvat, koska sivuston käyttäjillä ei ole luettelo 0 käyttölupaa. Jotta kokemus olisi oikein, asiakkaan API-kutsut on päivitettävä niin, että ne välittävät luettelon tunnuksen, joka on valittu luettelon valitsimessa. Jos käytät oletusarvoa ja käyttäjä vaihtaa luetteloita, verkkosivuston tulee tarjota valitun luettelon tiedot. Jotta mukautetut API-liittymät olisivat yhdenmukaisia Commerce-ydinkoodista suoritettavien API-liittymien kanssa, mukautettujen API-liittymien on välitettävä valittu luettelo.

Seuraavat mukautustapaukset edellyttävät kehityspäivityksiä:

- **Tapaus 1:** Asiakas esittelee oman [tietotoiminnon](e-commerce-extensibility/data-actions.md), joka kutsuu tuotteeseen liittyvää API- tai tietotoimintoa. Seuraavat päivitysvaiheet ovat pakollisia:

    1. Jos tietotoiminnossa käytetään suoraa API-kutsua, päivitä tietotoiminto niin, että se välittää luettelon tunnuksen seuraavan esimerkin mukaisesti.

        ![Päivitetty tietotoiminto, joka välittää luettelon tunnuksen.](./media/customization1_a.png)

    1. Jos tietotoiminto kutsuu eri tuotteeseen liittyvää tietotoimintoa mukautuksen sisällä, koodi on päivitettävä niin, että se välittää joitakin uusia parametreja, kuten **requestContext**. **requestContext**-parametrin avulla haetaan nykyisen luettelon tunnus seuraavan esimerkin mukaisesti.

        ![Päivitetty tietotoiminto, joka välittää uuden parametrin.](./media/customization1_b.png)

- **Tapaus 2:** Asiakkaalla on [ohitettu tietotoiminto](e-commerce-extensibility/data-action-overrides.md). Seuraavat päivitysvaihe on pakollinen:

    - Päivitä tietotoiminto samoin kuin tapauksessa 1.

- **Tapaus 3:** Asiakkaalla on näkymälaajennus, komentosarjan lisäysmoduuli tai [kloonattu moduuli](e-commerce-extensibility/modules-overview.md#clone-a-module-library-module), joka sisältää API- tai tietotoimintokutsut. Seuraavat päivitysvaihe on pakollinen:

    - Päivitä koodi tapauksen 1 tapaan seuraavan esimerkin kuvan mukaisesti.

       ![Päivitetty koodi, joka välittää uuden parametrin.](./media/customization3.png)

- **Tapaus 4:** Asiakas käyttää API-kutsua **getById**. Seuraavat päivitysvaihe on pakollinen:

    - Siirry API-kutsuun **getByIds** sen sijaan, sillä API-kutsulla **getById** on joitakin rajoituksia eikä se tue luettelon tiedostamista.

- **Tapaus 5:** Asiakkaalla on tietotoiminto, joka hakee tietoja useista eri luetteloista peräisin ja useista tuotteista. Seuraavat päivitysvaihe on pakollinen:

    - Jaa API-kutsut luettelon tunnuksen mukaan. Esimerkiksi ostoskorin API:lle ostoskori voi sisältää eri luetteloiden tuotteita. Tuoterivit pitää ryhmitellä luettelon tunnuksen mukaan, ja niiden tulisi kutsua API:a kutakin luetteloa varten erikseen, kuten seuraavassa esimerkissä on esitetty.

        ![Päivitetty tietotoiminto, joka ryhmittelee tuoterivit luettelon tunnuksen mukaan.](./media/customization5.png)

## <a name="additional-resources"></a>Lisäresurssit

[Commerce-luetteloiden luominen B2B-sivustoja varten](catalogs-b2b-sites.md)

[Usein kysytyt kysymykset B2B-sivustojen Commerce-luetteloista](catalogs-b2b-sites-FAQ.md)
