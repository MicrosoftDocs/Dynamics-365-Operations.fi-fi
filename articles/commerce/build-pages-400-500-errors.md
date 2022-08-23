---
title: Mukautettujen vastaussivujen luominen 4xx-/5xx-tilakoodien virheille
description: Tässä artikkelissa kerrotaan, miten mukautetut vastaussivut luodaan 4xx- ja 5xx-tilakoodivirheille käyttämällä Microsoft Dynamics 365 Commercen muokkaustyökaluja.
author: v-chgri
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 4a3b1762cebc74c1b77f9ca60925608bc966e306
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9276397"
---
# <a name="build-custom-response-pages-for-4xx5xx-status-code-errors"></a>Mukautettujen vastaussivujen luominen 4xx-/5xx-tilakoodien virheille

[!include [banner](includes/banner.md)]

Tässä artikkelissa kerrotaan, miten mukautetut vastaussivut luodaan 4xx- ja 5xx-tilakoodivirheille käyttämällä Microsoft Dynamics 365 Commercen muokkaustyökaluja.

Jos pyyntö ei onnistu, palvelin antaa HTTP-tilakoodivirhevastaukset. 404-tilakoodi tallennetaan ja palautetaan, jos sivua ei löydy. 500-tilakoodi tallennetaan ja palautetaan, jos tapahtuu palvelinvirhe. Dynamics 365 Commercessa sovelluksen käyttäjät voivat luoda mukautettuja tilakoodivirheiden vastausten sivuja, jotka näytetään käyttäjille näiden tilavirhekoodivirheiden vastauksina.

## <a name="build-a-status-code-error-response-page"></a>Tilakoodivirheen vastaussivun luominen

Voit luoda tilakoodivirheen vastaussivun seuraavasti.

1. Kirjaudu haluamallasi selaimella sisään Dynamics 365 Commerce -sovellukseen. 
1. Valitse sivusto, jolle haluat luoda 4xx-/5xx-tilakoodivirheen vastaussivun.

### <a name="build-the-template"></a>Mallin luominen

Voit luoda tilakoodivirheen vastaussivun mallin seuraavasti.

1. Valitse **Mallit**.
1. Luo sivumalli valitsemalla **Uusi**.
1. Kirjoita **Uusi malli** -valintaikkunan **Mallin nimi** -kohtaan uuden mallin nimi ja valitse sitten **OK**.
1. Luo malli sen rakenteen perusteella, jonka haluat määrittää tilakoodivirheen vastaussivulle.
1. Valitse **Tallenna**, valitse **Viimeistele muokkaus** tarkistaaksesi mallin, ja julkaise se valitsemalla **Julkaise**. 

### <a name="build-the-status-code-error-response-page"></a>Tilakoodivirheen vastaussivun luominen

Voit luoda tilakoodivirheen vastaussivun seuraavasti.

1. Siirry kohtaan **Sivut**.
1. Luo sivu valitsemalla **Uusi**.
1. Valitse malli **Valitse malli** -valinta ikkunassa ja kirjoita sitten **Sivun nimi** -kohtaan tilakoodin virhevastaussivun nimi. Jätä **Sivun URL-osoite** -kenttä tyhjäksi.
1. Luo sivu.
1. Valitse **Tallenna**, valitse **Viimeistele muokkaus** tarkistaaksesi sivun, ja julkaise se valitsemalla **Julkaise**.

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


[!INCLUDE[footer-include](../includes/footer-banner.md)]
