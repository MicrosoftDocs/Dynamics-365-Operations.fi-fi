---
title: Kirjautumislinkki ohjaa takaisin sähköisen kaupankäynnin sivustoon
description: Tämä artikkeli antaa vianmääritysohjeet, jotka voivat auttaa, kun kirjautumislinkki uudelleenohjaa takaisin sähköisen kaupankäynnin sivustoon kirjautumissivun asemesta.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 5274599ee5ea23c18648d95431b2e79ebca12dea
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8860215"
---
# <a name="sign-in-link-redirects-back-to-an-e-commerce-site"></a>Kirjautumislinkki ohjaa takaisin sähköisen kaupankäynnin sivustoon

[!include [banner](../../includes/banner.md)]

Tämä artikkeli antaa vianmääritysohjeet, jotka voivat auttaa, kun kirjautumislinkki uudelleenohjaa takaisin sähköisen kaupankäynnin sivustoon kirjautumissivun asemesta.

## <a name="description"></a>kuvaus

Kun olet konfiguroinut Commercen sivuston muodostimessa uuden Microsoft Azure Active Directory B2C (Azure AD B2C) -vuokraajan, **Kirjaudu**-linkin valitsevat käyttäjät ohjataan takaisin sähköisen kaupankäynnin saapumissivulle kirjautumissivulle menemättä.

## <a name="resolution"></a>Ratkaisu

### <a name="confirm-that-the-reply-url-is-correctly-configured-in-the-azure-ad-b2c-application"></a>Vahvista, että vastauksen URL-osoite on määritetty oikein Azure AD B2C -sovelluksessa

Voit vahvistaa, että vastauksen URL-osoite on määritetty oikein Azure AD B2C -sovelluksessa, toimimalla seuraavasti.

1. Siirry [Azure-portaaliin](https://portal.azure.com/).
1. Valitse Azure AD B2C -sovellus, jonka loit sivuston käyttöön.
1. Valitse sovellus, jonka olet luonut Azure AD B2C -asetusten yhteydessä.
1. Varmista **Vastauksen URL-osoite** -kohdassa, että luettelossa on sekä sivuston toimialueen URL-osoite että sähköisen kaupankäynnin luoman URL-osoitteen merkinnät seuraavan kuvan mukaisesti.

    ![Azure AD B2C:n Vastauksen URL-osoite -merkinnät.](media/aad-b2c-reply-url.jpg)

> [!NOTE]
> Sekä sivuston toimialueen URL-osoitteen että sähköisen kaupankäynnin luoman URL-osoitteen on oltava kelvollisessa URL-muodossa, jossa ei ole vinoviivoja lopussa eikä alussa.

## <a name="additional-resources"></a>Lisäresurssit

[Verkkosovelluksen rekisteröiminen Azure Active Directory B2C:ssä](/azure/active-directory-b2c/tutorial-register-applications?tabs=app-reg-ga#register-a-web-application)

[Kuluttajakaupan vuokraajan määrittäminen Commercessa](../set-up-b2c-tenant.md)