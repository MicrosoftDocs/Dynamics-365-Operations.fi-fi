---
title: Osallistu käyttääksesi luokituksia ja arvosteluja
description: Tässä ohjeaiheessa kerrotaan, miten voit käyttää luokituksia ja arvosteluja Microsoft Dynamics 365 Commerce -sivustossa.
author: gvrmohanreddy
manager: annbe
ms.date: 01/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 6c54a8fa01badb6a383c41dc979e71d82a25ef97
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5251232"
---
# <a name="opt-in-to-use-ratings-and-reviews"></a>Luokitusten ja arvostelujen käytön hyväksyminen

[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa kerrotaan, miten voit käyttää luokituksia ja arvosteluja Microsoft Dynamics 365 Commerce -sivustossa.

## <a name="overview"></a>Yleiskuvaus

Luokitukset ja arvostelut -ratkaisu on monikanavaratkaisu, jonka voit ottaa käyttöön Dynamics 365 Commerce -sovelluksessa käyttämällä Microsoft Dynamics Lifecycle Services (LCS) -palvelua. LCS on hallintaportaali, jonka avulla jälleenmyyjät voivat hallita ympäristöjä aina valmistelusta käytöstäpoistoon asti.

Jos haluat käyttää luokitukset ja arvostelut -ratkaisua Commerce-sivustossa, sinun on valittava luokitukset ja arvostelut verkkokauppasivuston käyttöönoton aikana Dynamics 365 Commercessa.

## <a name="opt-in-to-use-ratings-and-reviews"></a>Osallistu käyttääksesi luokituksia ja arvosteluja

Voit ottaa luokitukset ja arvostelut käyttöön sivustossa seuraavasti.

1. Noudata kohdan [Uuden sähköisen kaupankäynnin sivuston käyttöönotto](deploy-ecommerce-site.md) ohjeita.
1. Kun olet edelleen LCS-sovelluksessa, siirry kohtaan **Retail-käyttöönoton asetukset \> Muut asetukset**.
1. Määritä **Ota luokitukset ja arvostelut -palvelu käyttöön** -asetuksen arvoksi **Kyllä**.
1. Syötä **Luokitusten ja arvostelujen valvojan AAD-käyttöoikeusryhmä (käyttöoikeusryhmän objektin tunnus)** -kenttään sen Microsoft Azure Active Directory (Azure AD) -käyttöoikeusryhmän tunnus, joka sisältää luokitusten ja arvosteluiden valvojat.

    ![Osallistu käyttääksesi luokituksia ja arvosteluja](media/LCS_RnR_Preference.png)

1. Suorita sähköisen kaupankäynnin alustusprosessi loppuun.

> [!NOTE] 
> Jos olet olemassa oleva Dynamics 365 Commerce -asiakas, joka on jo ottanut käyttöön e-Commerce-sivuston ilman luokitusten ja arvostelujen käyttöä ja haluat nyt käyttää Dynamics 365 Commerce -pakkauksen luokituksia ja arvosteluja, lähetä palvelupyyntö. Lisätietoja huoltopyynnön lähettämisessä on ohjeaiheessa [Palvelupyyntöjen lähettämisprosessi](../fin-ops-core/dev-itpro/lifecycle-services/submit-request-dynamics-service-engineering-team.md?toc=/dynamics365/commerce/toc.json). 

## <a name="additional-resources"></a>Lisäresurssit

[Luokitukset ja arvostelut – yleiskatsaus](ratings-reviews-overview.md)

[Hallitse luokituksia ja arvosteluja](manage-reviews.md)

[Määritä luokitukset ja arvostelut](configure-ratings-reviews.md)

[Tuoteluokitusten synkronoiminen Dynamics 365 Commercessa](sync-product-ratings.md)




[!INCLUDE[footer-include](../includes/footer-banner.md)]