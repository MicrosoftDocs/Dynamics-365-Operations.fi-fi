---
title: Dynamics 365 Finance, Supply Chain Management ja Commerce Yhdysvaltain Government Community Cloudissa (GCC)
description: Tässä ohjeaiheessa on tietoja Microsoft Dynamics 365 US Government -tuotteista, jotka ovat hyväksytyn julkishallinnon tai yksityisen organisaation käytettävissä.
author: hasaid
ms.date: 11/12/2021
ms.topic: article
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: hasaid
ms.search.validFrom: 2021-11-09
ms.openlocfilehash: 204bf1886ff7f7393fba5713a54f305274f540d0
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/04/2022
ms.locfileid: "8693305"
---
# <a name="dynamics-365-finance-supply-chain-management-and-commerce-in-us-government-community-cloud-gcc"></a>Dynamics 365 Finance, Supply Chain Management ja Commerce Yhdysvaltain Government Community Cloudissa (GCC)

[!include [banner](../includes/banner.md)]



Tietyt Microsoft Dynamics 365 United States (US) Government -tuotteet ovat saatavilla hyväksytyille julkishallinnon tai yksityisille organisaatioille. Nämä organisaatiot on rajoitettu seuraaviin tyyppeihin:

- Yhdysvaltojen liittovaltion, osavaltion, paikallisen, heimon ja alueellisen julkishallinon yksiköt
- Yksityiset yksiköt, jotka käyttävät Dynamics 365 US Government -ympäristöä ratkaisujen tarjoamiseen viranomaisille tai Cloud Communityn hyväksytyille jäsenille
- Yksityisiä yksiköitä, joiden asiakastiedot ovat julkishallinnon säännösten mukaisia, ja Dynamics 365 US Government on sopiva palvelu säännösten noudattamiseksi

Lisätietoja: [Dynamics 365 US Government](/power-platform/admin/microsoft-dynamics-365-government).

## <a name="onboarding"></a>Onboarding

Voit suorittaa käyttöönottoprojektin alustavan perehdytyksen valmiiksi Microsoft Dynamics Lifecycle Servicesissä (LCS) noudattamalla [käyttöönottoprojektin perehdytyksen](../../../fin-ops-core/fin-ops/imp-lifecycle/onboard.md) ohjeita. Älä kuitenkaan käytä näissä ohjeissa annettua linkkiä julkiseen LCS:ään. Käytä sen sijaan seuraavaa linkkiä avataksesi LCS:n US Government Community Cloud (GCC) -ympäristölle: <https://gov.lcs.microsoftdynamics.us>.

Kun alustava perehdytys on valmis, noudata [projektin perehdytyksen](../lifecycle-services/project-onboarding.md) ohjeita. Käytä edelleen [GCC:n LCS:ää](https://gov.lcs.microsoftdynamics.us) julkisen LCS:n sijaan.

## <a name="environment-deployment"></a>Ympäristön käyttöönotto

Kun projektin perehdytys on valmis, voit tarkistaa LCS:n lisäominaisuudet, jotka on kuvattu kohdassa [Lifecycle Services (LCS) taloushallinnon ja toimintojen sovellusasiakkaille](../../../fin-ops-core/dev-itpro/lifecycle-services/lcs-works-lcs.md). Siirry sitten ympäristön käyttöönottoon.

- Voit ottaa Microsoftin hallitsemia ympäristöjä käyttöön LCS:n kautta noudattamalla kohdan [Lifecycle Services (LCS) taloushallinnon ja toimintojen sovellusasiakkaille](../../../fin-ops-core/dev-itpro/lifecycle-services/lcs-works-lcs.md#new-deployment-experience) ohjeita.
- Lisätietoja pilvipalvelussa ylläpidetyistä ympäristöistä on kohdassa [Kehitysympäristöjen käyttöönotto ja käyttö](../../../fin-ops-core/dev-itpro/dev-tools/access-instances.md). Sinun on myös suoritettava liittimien Resource Manager -perehdytysprosessi, kuten on kuvattu kohdassa [Azure Resource Manager -perehdytysprosessin suorittaminen Yhdysvaltain julkishallinnon Lifecycle Services -projekteille](arm-onbarding-us-goverment.md).

> [!NOTE]
> US Government LCS -projekteissa tuettuja ovat vain Azure Government -kohtaiset Azure-tilaukset.

## <a name="features-that-arent-available"></a>Ominaisuudet, jotka eivät ole käytettävissä

Jotkin ominaisuudet eivät ole käytössä GCC-käyttöönotossa, tai niitä ei voi käyttää GCC-ympäristössä Dynamics 365:n kanssa. Azure DevOps -palvelut eivät ole esimerkiksi käytettävissä GCC:ssä. Voit kuitenkin käyttää paikallista Azure DevOps- tai julkista Azure DevOps -palveluita. Lisätietoja toimintojen saatavuudesta on kohdassa [Liiketoimintasovellusten saatavuus US Government -ympäristössä](https://aka.ms/BAPFunctionalParity).

## <a name="frequently-asked-questions"></a>Usein kysytyt kysymykset

### <a name="are-dynamics-365-finance-and-dynamics-365-supply-chain-management-supported-in-gcc-high"></a>Tuetaanko Dynamics 365 Financea ja Dynamics 365 Supply Chain Managementia GCC-High-ympäristössä?

Ei Dynamics 365 Financea ja Dynamics 365 Supply Chain Managementia tuetaan vain GCC-ympäristössä?

### <a name="can-i-use-public-azure-devops-with-finance-and-supply-chain-management-in-gcc"></a>Voinko käyttää julkista Azure DevOpsia Financen ja Supply Chain Managementin kanssa GCC:ssä?

Kyllä, voit käyttää julkisia Azure DevOps -palveluja, jos ratkaisulle ei ole vaatimuksia, jotka Federal Risk and Authorization Management Program (FEDRAMP) on sertifioinut. Vaihtoehtoisesti voit käyttää Azure DevOps Serveriä.

### <a name="can-i-deploy-a-cloud-hosted-environment-tier-1-development-environment-on-an-azure-commercial-subscription"></a>Voinko ottaa käyttöön pilvipalvelussa ylläpidetyn Tier-1-kehitysympäristön, kun käytössä on Azure Commercial -tilaus?

Ei [GCC:n LCS:ssä](https://gov.lcs.microsoftdynamics.us) on käytettävä Azure Government -tilausta, jotta voit ottaa käyttöön pilvipalvelussa ylläpidettävän ympäristön.

### <a name="what-can-i-do-if-i-need-a-package-from-the-shared-asset-library-but-it-isnt-available-in-lcs-for-gcc"></a>Mitä voin tehdä, jos jaetun käyttöomaisuuskirjaston pakettia tarvitaan, mutta se ei ole käytettävissä GCC:n LCS:ssä?

Voit ladata saman paketin jaetusta käyttöomaisuuskirjastosta[ julkisessa LCS:stä](https://lcs.dynamics.com). Vaihtoehtoisesti yhteistyökumppanisi voi auttaa lataamaan paketin.

### <a name="is-the-code-upgrade-tool-available-in-gcc"></a>Onko koodin päivitystyökalu käytettävissä GCC:ssä?

Ei, koodin päivitystyökalu ei ole tällä hetkellä käytettävissä GCC:ssä. Prospektiprojektin voi kuitenkin luoda [julkisessa LCS:ssä](https://lcs.dynamics.com) ja käyttää koodin päivitystyökalua. Huomaa, että et voi ottaa käyttöön ympäristöjä prospektiprojekteissa.

### <a name="can-my-partner-open-a-support-ticket-on-my-behalf"></a>Voiko yhteistyökumppani avata tukilipun puolestani?

Kyllä. Jos yhteistyökumppanisi käyttää ei-GCC-tunnistetietoja, tukilippu ohjataan julkiseen tukijonoon. Suosittelemme asiakkaan GCC-oikeutta LCS:ssä tukilippujen avaamiseen.

## <a name="see-also"></a>Lisätietoja

- [Dynamics 365 US Government](/power-platform/admin/microsoft-dynamics-365-government)
- [Liiketoimintasovellusten saatavuus US Government -ympäristössä](https://aka.ms/BAPFunctionalParity).
- [Lifecycle Services (LCS) -käyttöopas](../../../fin-ops-core/dev-itpro/lifecycle-services/lcs-user-guide.md)
- [Pilvikäyttöönoton yleiskatsaus](../../../fin-ops-core/dev-itpro/deployment/cloud-deployment-overview.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
