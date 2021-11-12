---
title: Moderaattorien suorittaman arvostelujen ja arviointien manuaalisen julkaisun käyttöönotto
description: Tässä aiheessa kuvataan, miten moderaattorien suorittama arvostelujen ja arviointien manuaalinen julkaisu otetaan käyttöön Microsoft Dynamics 365 Commercessa ja miten arvostelut ja arvioinnit julkaistaan manuaalisesti.
author: gvrmohanreddy
manager: annbe
ms.date: 09/03/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-09-03
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 25ae7074fcf39bf4408ea1fa0acfc334281bb254
ms.sourcegitcommit: 1707cf45217db6801df260ff60f4648bd9a4bb68
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/23/2021
ms.locfileid: "7675046"
---
# <a name="enable-manual-publishing-of-ratings-and-reviews-by-a-moderator"></a>Moderaattorien suorittaman arvostelujen ja arviointien manuaalisen julkaisun käyttöönotto

[!include [banner](includes/banner.md)]

Tässä aiheessa kuvataan, miten moderaattorien suorittama arvostelujen ja arviointien manuaalinen julkaisu otetaan käyttöön Microsoft Dynamics 365 Commercessa ja miten arvostelut ja arvioinnit julkaistaan manuaalisesti.

Dynamics 365 Commercen arvostelu- ja arviointiratkaisussa käytetään Azure Cognitive Servicesiä kirosanojen valvontaan arvostelujen otsikoissa ja sisällöissä sekä arvostelujen ja arviointien julkaisuun. Siksi manuaalisia toimia ei tarvita sähköisen kaupankäynnin sivustosi arvostelujen ja arviointien tarkastamiseen ja julkaisemiseen.

Jotkut yritykset saattavat kuitenkin haluta mieluummin, että moderaattorit tarkistavat ja hyväksyvät arvostelut manuaalisesti, ennen kuin ne julkaistaan. Moderaattorin suorittaman arvostelujen ja arviointien manuaalisen julkaisun käyttöönottoa varten sinun on otettava **Edellytä moderaattoria arvosteluille ja arvioinneille** -ominaisuus käyttöön Commercen sivustonluontiohjelmassa.

## <a name="enable-the-require-moderator-for-ratings-and-reviews-feature-in-commerce-site-builder"></a>Edellytä moderaattoria arvosteluille ja arvioinneille -ominaisuuden käyttöönotto Commercen sivustonluontiohjelmassa

Noudata seuraavia ohjeita ottaaksesi **Edellytä moderaattoria arvosteluille ja arvioinneille** -ominaisuuden käyttöön Commercen sivustonluontiohjelmassa.

1. Siirry kohtaan **Aloitus \> Arvostelut \> Asetukset**.
1. Määritä **Edellytä moderaattoria arvosteluille ja arvioinneille**-asetuksen arvoksi **Päällä**.

> [!NOTE]
> Ottamalla **Edellytä moderaattoria arvosteluille ja arvioinneille** -ominaisuuden käyttöön lopetat arvostelujen ja arviointien automaattisen julkaisun, joten ne on julkaistava manuaalisesti. Azure Cognitive Services kuitenkin jatkaa kirosanojen valvontaa arvostelujen otsikoissa ja sisällöissä.

<!--![Require moderator for ratings and reviews setting in Commerce site builder.](media/Ratings-reviews-settings-human-moderation.png)-->

## <a name="publish-ratings-and-reviews"></a>Arvostelujen ja arviointien julkaisu

Kun otat **Edellytä moderaattoria arvosteluille ja arvioinneille** -ominaisuuden käyttöön moderaattorin on manuaalisesti tarkistettava ja julkaistava arvostelut ja arvioinnit, jotta ne tulevat näkyviin sähköisen kaupankäynnin sivustollasi.

Voit tarkistaa ja julkaista arvosteluja ja arviointeja Commercen sivustonluontiohjelmassa noudattamalla seuraavia ohjeita.

1. Siirry kohtaan **Arvostelut \> Moderointi**.
1. Jos ruudukon rivin **Tila**-kentän arvoksi on määritetty **Julkaisematon**, kyseisen rivin arvostelua ja arviointia ei ole vielä julkaistu. Voit tarkastella vain julkaisemattomia arvosteluja ja arviointeja valitsemalla ruudukon yläpuolen tilasuodattimessa **Tila: Vaatii tarkistuksen**.
1. Valitse vähintään yksi arvostelu ja arviointi, joiden tilana on **Julkaisematon**, ja valitse sitten komentopalkista **Julkaise**. Valitut arvostelut ja arviot lisätään julkaisujonoon, ja ne tulevat näkyviin sähköisen kaupankäynnin sivustolla, kun ne on julkaistu.

> [!NOTE]
> - Arvostelun ja arvioinnin julkaisun jälkeen tila-arvo muuttuu arvosta **Julkaisematon** nolla-arvoksi (tyhjä kenttä).
> - Jos valitset useita arvosteluja ja arviointeja, joilla on erilaisia tiloja, ja valitset sitten **Julkaise**, vielä julkaisemattomat arvostelut ja arvioinnit julkaistaan. Jo julkaisuja arvosteluja ja arvioita ei kuitenkaan julkaista uudelleen.

Seuraavassa kuvassa näkyy esimerkki, jossa Commercen sivustonluontiohjelman **Moderointi**-sivulla on valittu kolme julkaisematonta arvostelua ja arviointia.

![Kolme julkaisematonta arvostelua ja arviointia valittuna Commercen sivustonluontiohjelman Moderointi-sivulla.](media/Ratings-reviews-publishing-reviews.png)

<!--![Dynamics 365 Commerce - Ratings and Review configuration 2](media/Ratings-reviews-published-reviews.png)-->
<!--![Status filter](media/Ratings-reviews-published-reviews-status-filter.png)-->

## <a name="additional-resources"></a>Lisäresurssit

[Luokitukset ja arvostelut – yleiskatsaus](ratings-reviews-overview.md)
