---
title: Luokitusten ja arvostelujen tuominen ja vieminen
description: Tässä artikkelissa kuvataan, kuinka tuoteluokituksia ja -arvioita tuodaan ja viedään Microsoft Dynamics 365 Commercessa.
author: gvrmohanreddy
ms.date: 01/12/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: f369e3cd208cdfba816f817ead75374ee6982912
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9271932"
---
# <a name="import-and-export-ratings-and-reviews"></a>Luokitusten ja arvostelujen tuominen ja vieminen

[!include [banner](includes/banner.md)]

Tässä artikkelissa kuvataan, kuinka tuoteluokituksia ja -arvioita tuodaan ja viedään Microsoft Dynamics 365 Commercessa.

Dynamics 365 Commerce tarjoaa [luokitukset ja arvostelut](ratings-reviews-overview.md) monikanavaratkaisuna. Kun siirryt Dynamics 365 Commercen luokituksiin ja arviointiratkaisuun, haluat ehkä siirtää aiemmin luodut luokitukset ja arviot tiedot Commerce-alustalle. Voit myös viedä Commercen luokituksia ja arvioita liiketoimintavaatimusten mukaan. Power Automaten liittimen avulla voit tuoda luokituksia ja arvioita Commerceen ja viedä ne Commercesta.

> [!NOTE]
> Tietoja logiikan työnkulujen käytön aloittamisesta Power Automatessa on kohdassa [Pilvityönkulun luominen Power Automatessa](/power-automate/get-started-logic-flow).

## <a name="prerequisites"></a>Edellytykset

Ennen kuin voit tuoda ja viedä luokituksia ja arvioita, sinun on täytettävä seuraavat edellytykset:

- Luokitukset ja tarkistusratkaisut on otettava käyttöön e-commerce-sivustossa Commerce-ympäristössä. Lisätietoja on kohdassa [Ota käyttöön luokitusten ja arvostelujen käyttö](opt-in-ratings-reviews.md).
- The Dynamics 365 Ratings and Reviews Power App Connector on määritettävä niin, että sovelluksessa voi ottaa käyttöön joko "lähetä arvioita" tai "vie arvioita" Power Automatessa. Lisätietoja on kohdassa [Dynamics 365 Commerce - luokitusten ja arvostelujen käyttö (esiversio)](/connectors/dynamics365ratingsre/).
- Service to Service (S2S) -todennus on konfiguroitu niin, että luokitukset ja ohjelmointirajapintaliittymän (API) arviot voidaan kutsua suojatusti Commercen ulkopuolelta. Lisätietoja on kohdassa [Palveluiden välisen todennuksen määrittäminen](service-to-service-auth.md).

## <a name="import-ratings-and-reviews"></a>Tuo luokituksia ja arvosteluja

Voit tuoda luokituksia ja tarkastella tietoja aiemmin luodusta järjestelmästä Commerce-järjestelmään lisäämällä Dynamics 365 -luokitukset ja Power Automate -liittimen aiemmin luotuun Power Automate -työnkulkuun tai uuteen. Lisätietoja on kohdassa [Dynamics 365 Commerce - luokitusten ja arvostelujen käyttö (esiversio)](/connectors/dynamics365ratingsre/).

> [!IMPORTANT]
> Ennen kuin tämän menettelyn voi suorittaa, [S2S-tunnusten todennus on määritettävä](service-to-service-auth.md).

Jos haluat tuoda luokituksia ja arvioita Commerceen Dynamics 365 -luokitusten ja arviointien Power Automate -liittimen avulla, noudata seuraavia ohjeita.

1. Valitse **Lähetä käyttäjäarvio** -toiminto.
1. Muodosta yhteys käyttämällä Azure Active Directory (Azure AD) -sovelluksen tietoja, jotka on luotu S2S-todennuksen konfiguroinnissa. Lisätietoja on kohdassa [Palveluiden välisen todennuksen määrittäminen](service-to-service-auth.md).
1. **Lähetä käyttäjän tarkistus** -toiminto tarkistaa yhden toimenpiteen kerrallaan. Toista näin toimenpide. Käytä lähdearvioita luettelona bulkkiarvion lähettämiseen.
    
## <a name="export-ratings-and-reviews"></a>Vie luokituksia ja arvosteluja

Voit viedä luokituksia ja tarkastella tietoja Commerce-järjestelmään lisäämällä Dynamics 365 -luokitukset ja Power Automate -liittimen aiemmin luotuun Power Automate -työnkulkuun tai uuteen. Lisätietoja on kohdassa [Dynamics 365 Commerce - luokitusten ja arvostelujen käyttö (esiversio)](/connectors/dynamics365ratingsre/).

Jos haluat viedä luokituksia ja arvioita Commercesta Dynamics 365 -luokitusten ja arviointien Power Automate -liittimen avulla, noudata seuraavia ohjeita.

1. Valitse **Vie kaikki arviot** -toiminto.
1. Suorita toiminto. 

## <a name="additional-resources"></a>Lisäresurssit

[Luokitukset ja arvostelut – yleiskatsaus](ratings-reviews-overview.md)

[Luokitusten ja arvostelujen käytön hyväksyminen](opt-in-ratings-reviews.md)

[Hallitse luokituksia ja arvosteluja](manage-reviews.md)

[Määritä luokitukset ja arvostelut](configure-ratings-reviews.md)

[Synkronoi tuoteluokitukset](sync-product-ratings.md)

[Salli valvojan julkaista luokituksia ja arvosteluja manuaalisesti](manual-publish-rating-reviews.md)

[Palvelujen välisen todennuksen määrittäminen](service-to-service-auth.md)

[Luokitusten ja arvostelujen usein kysytyt kysymykset](ratings-reviews-faq.md)
