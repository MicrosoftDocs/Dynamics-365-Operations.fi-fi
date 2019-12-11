---
title: Osallistu käyttääksesi luokituksia ja arvosteluja
description: Tässä ohjeaiheessa kerrotaan, miten voit käyttää luokituksia ja arvosteluja Microsoft Dynamics 365 Commerce -sivustossa.
author: gvrmohanreddy
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 10e3c33af232fa46df09a103b2e73eae09a909eb
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697977"
---
# <a name="opt-in-to-use-ratings-and-reviews"></a>Osallistu käyttääksesi luokituksia ja arvosteluja

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa kerrotaan, miten voit käyttää luokituksia ja arvosteluja Microsoft Dynamics 365 Commerce -sivustossa.

## <a name="overview"></a>Yleiskatsaus

Luokitukset ja arvostelut -ratkaisu on monikanavaratkaisu, jonka voit ottaa käyttöön Dynamics 365 Commerce -sovelluksessa käyttämällä Microsoft Dynamics Lifecycle Services (LCS) -palvelua. LCS on hallintaportaali, jonka avulla jälleenmyyjät voivat hallita ympäristöjä aina valmistelusta käytöstäpoistoon asti.

Jos haluat käyttää luokitukset ja arvostelut -ratkaisua Commerce-sivustossa, sinun on ensin suostuttava sen käyttöön.

## <a name="opt-in-to-use-ratings-and-reviews"></a>Osallistu käyttääksesi luokituksia ja arvosteluja

Voit ottaa luokitukset ja arvostelut käyttöön sivustossa seuraavasti.

1. Noudata kohdan [Uuden sähköisen kaupankäynnin sivuston käyttöönotto](deploy-ecommerce-site.md) ohjeita.
1. Kun olet edelleen LCS-sovelluksessa, siirry kohtaan **Retail-käyttöönoton asetukset \> Muut asetukset**.
1. Määritä **Ota luokitukset ja arvostelut -palvelu käyttöön** -asetuksen arvoksi **Kyllä**.
1. Syötä **Luokitusten ja arvostelujen valvojan AAD-käyttöoikeusryhmä (käyttöoikeusryhmän objektin tunnus)** -kenttään sen Microsoft Azure Active Directory (Azure AD) -käyttöoikeusryhmän tunnus, joka sisältää luokitusten ja arvosteluiden valvojat.

    ![Osallistu käyttääksesi luokituksia ja arvosteluja](media/LCS_RnR_Preference.png)

1. Suorita sähköisen kaupankäynnin alustusprosessi loppuun.

## <a name="additional-resources"></a>Lisäresurssit

[Luokitukset ja arvostelut – yleiskatsaus](ratings-reviews-overview.md)

[Hallitse luokituksia ja arvosteluja](manage-reviews.md)

[Määritä luokitukset ja arvostelut](configure-ratings-reviews.md)

[Tuoteluokitusten synkronoiminen Dynamics 365 Retailissa](sync-product-ratings.md)
