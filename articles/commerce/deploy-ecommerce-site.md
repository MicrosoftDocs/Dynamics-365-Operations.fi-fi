---
title: Uuden sähköisen kaupankäynnin vuokraajan käyttöönotto
description: Tässä ohjeaiheessa kerrotaan, miten uusi sähköisen kaupankäynnin vuokraaja otetaan käyttöön Microsoft Dynamics Lifecycle Services (LCS) -palvelun avulla.
author: psimolin
manager: annbe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: c2632632b9b21dd3a88e9a4df0e65cfd28e579d2
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697448"
---
# <a name="deploy-a-new-e-commerce-tenant"></a>Uuden sähköisen kaupankäynnin vuokraajan käyttöönotto

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa kerrotaan, miten uusi sähköisen kaupankäynnin sivusto otetaan käyttöön Microsoft Dynamics Lifecycle Services (LCS) -palvelun avulla.

## <a name="overview"></a>Yleiskatsaus
    
Microsoft Dynamics Lifecycle Services (LCS) on pilvipohjainen yhteinen työtila, jossa kumppanit ja asiakkaat voivat hallita projekteja ja ympäristöjä, katsella uusimpia tietoja Microsoft Dynamics -tuotteista ja -toiminnoista sekä luoda, seurata ja selata tukitapauksia. Sähköisen kaupankäynnin hallintatoiminnot integroidaan LCS:n kanssa.

Lisätietoja LCS:stä on kohdassa [Lifecycle Services -käyttöopas](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide).
    
## <a name="get-started"></a>Aloittaminen

Ennen kuin voit alustaa sähköisen kaupankäynnin, sinun on alustettava projekti, ympäristö ja Retail Cloud Scale Unit (RCSU). Jos haluat tehdä alustuksen LCS:ssä, tarvitset joko projektin omistajan tai ympäristön valvojan roolin oikeudet. Tuotanto- ja eristysympäristön topologioita tuetaan.

Lisätietoja ympäristöistä on kohdassa [Ympäristön suunnittelu](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/imp-lifecycle/environment-planning). Lisätietoja RCSU:sta on kohdassa [Retail Cloud Scale Unitin alustaminen](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/deployment/initialize-retail-channels).

## <a name="initialize-e-commerce"></a>Sähköisen kaupankäynnin alustaminen

Tämän menetelmän avulla voit alustaa sähköisen kaupankäynnin ominaisuuden aiemmin luodussa ympäristössä.

Varmista ennen aloittamista, että sinulla on seuraavat pakolliset tiedot:

- Käytettävä RCSU.
- Microsoft Azure Active Directory -käyttöoikeusryhmä, jota sähköisen kaupankäynnin järjestelmänvalvojat käyttävät group that will be used for e-Commerce system admins.
- Microsoft Azure Active Directory -käyttöoikeusryhmä, jota luokitusten ja arvostelujen valvojat käyttävät.
- Toimialueet, jotka liitetään ympäristöön.

Lisäksi voit kerätä seuraavat valinnaiset tiedot:

- Azure AD:n kuluttajakaupan tiedot:

    - Vuokraajan nimi.
    - Asiakastunnus.
    - Sisäänkirjauksen mukautettu toimialue.
    - Vastauksen URL-osoite.
    - SignUp SignIn -käytännön tunnus.
    - Salasanan nollauskäytännön tunnus.
    - Profiilin muokkauskäytännön tunnus.

[!NOTE]
Nämä tiedot voidaan lisätä myöhemmin palvelupyynnön avulla.

Kun olet kerännyt tarvittavat tiedot, alusta sähköinen kaupankäynti seuraavasti.

1. Kirjaudu sisään [LCS:ään](https://lcs.dynamics.com).
1. Avaa projekti, joka sisältää sen ympäristön, jossa haluat alustaa sähköisen kaupankäynnin.
1. Valitse **Ympäristöt**-osassa ympäristö.
1. Valitse **Ympäristön ominaisuudet** -kohdassa **Retailin hallinta** -linkki.
1. Valitse **Sähköinen kaupankäynti** -välilehdessä **Asetukset**. Näyttöön tulee valintaikkuna, johon on kirjoitettava valmistelun edellyttämät tiedot.
1. Täytä tarvittavat tiedot ja siirry seuraavalle sivulle.
1. Täytä tarvittavat tiedot seuraavalla sivulla ja lähetä lomake. Palaat **Sähköinen kaupankäynti** -välilehteen, jossa näet, että alustus on alkanut.
1. Jos haluat tarkastella alustuksen tilaa, valitse **Päivitä** tai palaa **Sähköinen kaupankäynti** -välilehteen myöhemmin.
    
Kun sähköinen kaupankäynti alustetaan LCS:stä, järjestelmä valmistelee useita osia, jotka ovat pakollisia sähköisessä kaupankäynnissä, ja liittää ne ympäristöön. Kun valmistelu on tehty, **Sähköinen kaupankäynti** -välilehti **Retail-hallinta**-sivulla päivitetään vastaamaan valmistelua. Sivulla näkyvät viimeisimmät mukautuksen käyttöönotot ja muiden käynnissä olevien käyttöönottojen tila. Se sisältää myös linkit sähköisen kaupankäynnin sivustoon ja sähköisen kaupankäynnin sivuston hallintatyökalun (muokkaustyökalu).

## <a name="access-the-authoring-environment"></a>Muokkausympäristön käyttäminen

Jos haluat käyttää muokkausympäristöä, siirry **Sähköinen kaupankäynti** -välilehteen **Retail-hallinta**-sivulla. Sieltä löydät linkit sähköisen kaupankäynnin sivustoon ja sivuston hallintatyökaluun.

## <a name="additional-resources"></a>Lisäresurssit

[Verkkokaupan yleiskatsaus](online-store-overview.md)

[Sähköisen kaupankäynnin sivuston luominen](create-ecommerce-site.md)

[Liitä verkkosivusto kanavaan](associate-site-online-store.md)

[Toimialueen nimen määrittäminen](configure-your-domain-name.md)

[Sisältöverkon (CDN) tuen lisääminen](add-cdn-support.md)

[Sijaintiin perustuvan myymälän tunnistuksen käyttöönotto](enable-store-detection.md)

[Mukautettujen sivujen määrittäminen käyttäjän kirjautumisia varten](custom-pages-user-logins.md)