---
title: Mukautettujen vastaussivujen luominen 4xx-/5xx-tilakoodien virheille
description: Tässä ohjeaiheessa kerrotaan, miten mukautetut vastaussivut luodaan 4xx- ja 5xx-tilakoodivirheille käyttämällä Microsoft Dynamics 365 Commercen muokkaustyökaluja.
author: v-chgri
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: bcceeb1bc68c6432442c863ca06b7ba81d0abed8
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697103"
---
# <a name="build-custom-response-pages-for-4xx5xx-status-code-errors"></a>Mukautettujen vastaussivujen luominen 4xx-/5xx-tilakoodien virheille

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa kerrotaan, miten mukautetut vastaussivut luodaan 4xx- ja 5xx-tilakoodivirheille käyttämällä Microsoft Dynamics 365 Commercen muokkaustyökaluja.

## <a name="overview"></a>Yleiskatsaus

Jos pyyntö ei onnistu, palvelin antaa HTTP-tilakoodivirhevastaukset. 404-tilakoodi tallennetaan ja palautetaan, jos sivua ei löydy. 500-tilakoodi tallennetaan ja palautetaan, jos tapahtuu palvelinvirhe. Dynamics 365 Commercessa sovelluksen käyttäjät voivat luoda mukautettuja tilakoodivirheiden vastausten sivuja, jotka näytetään käyttäjille näiden tilavirhekoodivirheiden vastauksina.

## <a name="build-a-status-code-error-response-page"></a>Tilakoodivirheen vastaussivun luominen

Voit luoda tilakoodivirheen vastaussivun seuraavasti.

1. Kirjaudu haluamallasi selaimella sisään Dynamics 365 Commerce -sovellukseen. 
1. Valitse sivusto, jolle haluat luoda 4xx-/5xx-tilakoodivirheen vastaussivun.

### <a name="build-the-template"></a>Mallin luominen

Voit luoda tilakoodivirheen vastaussivun mallin seuraavasti.

1. Siirry kohtaan **Mallit \> Uusi malli**.
1. Anna uudelle mallille nimi.
1. Luo malli sen rakenteen perusteella, jonka haluat määrittää tilakoodivirheen vastaussivulle.
1. Kirjaa malli sisään ja julkaise se.

### <a name="build-the-status-code-error-response-page"></a>Tilakoodivirheen vastaussivun luominen

Voit luoda tilakoodivirheen vastaussivun seuraavasti.

1. Siirry kohtaan **Sivut \> Uusi sivu**.
1. Anna tilakoodivirheen vastaussivulle nimi, mutta **älä** määritä **URL-osoite**-kentän arvoa.
1. Luo sivu.
1. Kirjaa sivu sisään ja julkaise se.

> [!NOTE]
> Voit luoda erilliset tilakoodivirheen vastaussivut 4xx- ja 5xx-tilakoodivirheille. Halutessasi voit käyttää samaa yleistä tilakoodivirheen vastaussivua molemmissa virheluokissa.

### <a name="set-up-a-redirect-for-the-status-code-error-response-page"></a>Tilakoodivirheen vastaussivun uudelleenohjauksen määrittäminen

Voit määrittää tilakoodivirheen vastaussivun uudelleenohjauksen seuraavasti.

1. Siirry kohtaan **URL-osoitteet \> Uusi \> Uusi alias** ja valitse aiemmin luotu tilakoodivirheen vastaussivu.
1. Syötä **Alias**-kenttään **oletusarvo - 4xx** tai **oletusarvo - 5xx** sen mukaan, mille tilakoodivirheen vastaussivulle olet määrittämässä uudelleenohjausta. Nämä aliakset on julkaistava. Muussa tapauksessa uudelleenohjaus ei toimi.
1. Valitse **OK** vahvistaaksesi linkityksen.

> [!NOTE]
> Jos käytät molemmissa virheluokissa yhtä tilakoodivirheen vastaussivua, toista tämä proseduuri ja linkitä alias myös toiseen saman sivun virheluokkaan.

## <a name="additional-resources"></a>Lisäresurssit

[Mallien käyttö](work-with-templates.md)

[Uuden sivuston sivun lisääminen](add-new-page.md)

[Sivun URL-osoitteen luominen](create-page-url.md)
