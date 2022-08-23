---
title: Luokitusten ja arvostelujen käytön hyväksyminen
description: Tässä artikkelissa kerrotaan, miten voit käyttää luokituksia ja arvosteluja Microsoft Dynamics 365 Commerce -sivustossa.
author: gvrmohanreddy
ms.date: 02/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.custom: ''
ms.assetid: ''
ms.search.industry: ''
ms.openlocfilehash: 00fd30ded916cc6b587ceff67728e7d964714716
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9269159"
---
# <a name="opt-in-to-use-ratings-and-reviews"></a>Luokitusten ja arvostelujen käytön hyväksyminen

[!include [banner](includes/banner.md)]

Tässä artikkelissa kerrotaan, miten voit käyttää luokituksia ja arvosteluja Microsoft Dynamics 365 Commerce -sivustossa.

Luokitukset ja arvostelut -ratkaisu on monikanavaratkaisu, jonka voit ottaa käyttöön Dynamics 365 Commerce -sovelluksessa käyttämällä Microsoft Dynamics Lifecycle Services (LCS) -palvelua. LCS on hallintaportaali, jonka avulla jälleenmyyjät voivat hallita ympäristöjä aina valmistelusta käytöstäpoistoon asti.

Jos haluat käyttää luokitukset ja arvostelut -ratkaisua Commerce-sivustossa, sinun on valittava luokitukset ja arvostelut verkkokauppasivuston käyttöönoton aikana Dynamics 365 Commercessa.

## <a name="opt-in-to-use-ratings-and-reviews"></a>Osallistu käyttääksesi luokituksia ja arvosteluja

Voit ottaa luokitukset ja arvostelut käyttöön sivustossa seuraavasti.

1. Noudata kohdan [Uuden sähköisen kaupankäynnin sivuston käyttöönotto](deploy-ecommerce-site.md) ohjeita.
1. Kun olet edelleen LCS-sovelluksessa, siirry kohtaan **Retail-käyttöönoton asetukset \> Muut asetukset**.
1. Määritä **Ota luokitukset ja arvostelut -palvelu käyttöön** -asetuksen arvoksi **Kyllä**.
1. Syötä **Luokitusten ja arvostelujen valvojan AAD-käyttöoikeusryhmä** -kenttään sen Microsoft Azure Active Directory (Azure AD) -käyttöoikeusryhmän tunnus, joka sisältää luokitusten ja arvosteluiden valvojat.

    ![Luokitusten ja arvostelujen käytön hyväksyminen.](media/LCS_RnR_Preference_2.png)

1. Suorita sähköisen kaupankäynnin alustusprosessi loppuun.

> [!NOTE] 
> Jos olet olemassa oleva Dynamics 365 Commerce -asiakas, joka on jo ottanut käyttöön e-Commerce-sivuston ilman luokitusten ja arvostelujen käyttöä ja haluat nyt käyttää Dynamics 365 Commerce -pakkauksen luokituksia ja arvosteluja, lähetä palvelupyyntö. Lisätietoja huoltopyynnön lähettämisessä on ohjeaiheessa [Palvelupyyntöjen lähettämisprosessi](../fin-ops-core/dev-itpro/lifecycle-services/submit-request-dynamics-service-engineering-team.md?toc=/dynamics365/commerce/toc.json). 

## <a name="additional-resources"></a>Lisäresurssit

[Luokitukset ja arvostelut – yleiskatsaus](ratings-reviews-overview.md)

[Hallitse luokituksia ja arvosteluja](manage-reviews.md)

[Määritä luokitukset ja arvostelut](configure-ratings-reviews.md)

[Tuoteluokitusten synkronoiminen Dynamics 365 Commercessa](sync-product-ratings.md)

[Salli valvojan julkaista luokituksia ja arvosteluja manuaalisesti](manual-publish-rating-reviews.md)

[Luokitusten ja arvostelujen tuominen ja vieminen](import-export-reviews.md)

[Palvelujen välisen todennuksen määrittäminen](service-to-service-auth.md)

[Luokitusten ja arvostelujen usein kysytyt kysymykset](ratings-reviews-faq.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
