---
title: Uuden sähköisen kaupankäynnin vuokraajan käyttöönotto
description: Tässä ohjeaiheessa kerrotaan, miten uusi sähköisen kaupankäynnin Dynamics 365 Commerce -sivusto otetaan käyttöön Microsoft Dynamics Lifecycle Services (LCS) -palvelun avulla.
author: psimolin
manager: annbe
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 3b750ee89a85688dcebe673f9c3ff13693e9fcad
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4976735"
---
# <a name="deploy-a-new-e-commerce-tenant"></a>Uuden sähköisen kaupankäynnin vuokraajan käyttöönotto


[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa kerrotaan, miten uusi sähköisen kaupankäynnin Dynamics 365 Commerce -sivusto otetaan käyttöön Microsoft Dynamics Lifecycle Services (LCS) -palvelun avulla.

## <a name="overview"></a>Yleiskuvaus

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

> [!NOTE]
> Nämä tiedot voidaan lisätä myöhemmin palvelupyynnön avulla.

Kun olet kerännyt tarvittavat tiedot, alusta sähköinen kaupankäynti seuraavasti.

1. Kirjaudu sisään [LCS:ään](https://lcs.dynamics.com).
1. Avaa projekti, joka sisältää sen ympäristön, jossa haluat alustaa sähköisen kaupankäynnin.
1. Valitse **Ympäristöt**-osassa ympäristö.
1. Valitse **Ympäristön ominaisuudet** -kohdassa **Retailin hallinta** -linkki.
1. Valitse **Sähköinen kaupankäynti** -välilehdessä **Asetukset**. Näyttöön tulee valintaikkuna, johon on kirjoitettava valmistelun edellyttämät tiedot.
1. Täytä tarvittavat tiedot ja siirry seuraavalle sivulle.
1. Täytä tarvittavat tiedot seuraavalla sivulla ja lähetä lomake. Palaat **Sähköinen kaupankäynti** -välilehteen, jossa näet, että alustus on alkanut.
1. Jos haluat tarkastella alustuksen tilaa, valitse **Päivitä** tai palaa **Sähköinen kaupankäynti** -välilehteen myöhemmin.
    
Kun sähköinen kaupankäynti alustetaan LCS:stä, järjestelmä valmistelee useita osia, jotka ovat pakollisia sähköisessä kaupankäynnissä, ja liittää ne ympäristöön. Kun valmistelu on tehty, **Sähköinen kaupankäynti** -välilehti **Retail-hallinta**-sivulla päivitetään vastaamaan valmistelua. Sivulla näkyvät viimeisimmät mukautuksen käyttöönotot ja muiden käynnissä olevien käyttöönottojen tila. Se sisältää myös linkit sähköisen kaupankäynnin sivustoon ja sähköisen kaupankäynnin sivustomuodostinsivulle, jolla sivut luodaan.

## <a name="access-commerce-site-builder"></a>Commerce-sivuston muodostimen käyttö

Kun haluat käyttää Commerce-sivuston muodostinta, siirry **Sähköinen kaupankäynti**-välilehteen LCS:n **Vähittäismyynnin hallinta** -sivu ja valitse **Sähköisen kaupankäynnin hallintatyökalu** -linkki. Sivustonmuodostimen aloitussivulla näkyy vuokraajatason näkymä. Tällä sivulla voit:

- Muokata vuokraajatason asetuksia.
- Siirry mille tahansa luomallesi sivustolle katseluoikeuksilla. 
- Käytä tarkistustoimintoja, kuten arviointia ja raportointia.
- Luo uusi sivusto. Lisätietoja uuden sivuston luomisesta ja käyttöönotosta on kohdassa [Luo sähköisen kaupankäynnin sivusto](create-ecommerce-site.md). 

## <a name="additional-resources"></a>Lisäresurssit

[Toimialueen nimen määrittäminen](configure-your-domain-name.md)

[Sähköisen kaupankäynnin sivuston luominen](create-ecommerce-site.md)

[Dynamics 365 Commerce -sivuston liittäminen online-kanavaan](associate-site-online-store.md)

[Robots.txt-tiedostojen hallinta](manage-robots-txt-files.md)

[URL-uudelleenohjausten joukkolataus palveluun](upload-bulk-redirects.md)

[B2C-vuokraajan määrittäminen Commercessa](set-up-B2C-tenant.md)

[Mukautettujen sivujen määrittäminen käyttäjän kirjautumisia varten](custom-pages-user-logins.md)

[Useiden B2C-vuokraajien määrittäminen Commerce-ympäristössä](configure-multi-B2C-tenants.md)

[Sisältöverkon (CDN) tuen lisääminen](add-cdn-support.md)

[Sijaintiin perustuvan myymälän tunnistuksen käyttöönotto](enable-store-detection.md)
