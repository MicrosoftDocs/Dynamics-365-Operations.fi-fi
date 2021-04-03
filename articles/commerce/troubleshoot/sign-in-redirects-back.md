---
title: Kirjautumislinkki ohjaa takaisin sähköisen kaupankäynnin sivustoon
description: Tämä ohjeaihe antaa vianmääritysohjeet, jotka voivat auttaa, kun kirjautumislinkki uudelleenohjaa takaisin sähköisen kaupankäynnin sivustoon kirjautumissivun asemesta.
author: Reza-Assadi
manager: AnnBe
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
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
ms.openlocfilehash: 36f10c9f68570a6c67da6b4b6e4155f4634f633a
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585295"
---
# <a name="sign-in-link-redirects-back-to-an-e-commerce-site"></a><span data-ttu-id="f2ee5-103">Kirjautumislinkki ohjaa takaisin sähköisen kaupankäynnin sivustoon</span><span class="sxs-lookup"><span data-stu-id="f2ee5-103">Sign-in link redirects back to an e-commerce site</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f2ee5-104">Tämä ohjeaihe antaa vianmääritysohjeet, jotka voivat auttaa, kun kirjautumislinkki uudelleenohjaa takaisin sähköisen kaupankäynnin sivustoon kirjautumissivun asemesta.</span><span class="sxs-lookup"><span data-stu-id="f2ee5-104">This topic provides troubleshooting guidance that can help when a sign-in link redirects back to the e-commerce site instead of going to the sign-in page.</span></span>

## <a name="description"></a><span data-ttu-id="f2ee5-105">kuvaus</span><span class="sxs-lookup"><span data-stu-id="f2ee5-105">Description</span></span>

<span data-ttu-id="f2ee5-106">Kun olet konfiguroinut Commercen sivuston muodostimessa uuden Microsoft Azure Active Directory B2C (Azure AD B2C) -vuokraajan, **Kirjaudu**-linkin valitsevat käyttäjät ohjataan takaisin sähköisen kaupankäynnin saapumissivulle kirjautumissivulle menemättä.</span><span class="sxs-lookup"><span data-stu-id="f2ee5-106">After you configure a new Microsoft Azure Active Directory B2C (Azure AD B2C) tenant in Commerce site builder, users who select the **Sign in** link are redirected back to the main e-commerce landing page without going to the sign-in page.</span></span>

## <a name="resolution"></a><span data-ttu-id="f2ee5-107">Ratkaisu</span><span class="sxs-lookup"><span data-stu-id="f2ee5-107">Resolution</span></span>

### <a name="confirm-that-the-reply-url-is-correctly-configured-in-the-azure-ad-b2c-application"></a><span data-ttu-id="f2ee5-108">Vahvista, että vastauksen URL-osoite on määritetty oikein Azure AD B2C -sovelluksessa</span><span class="sxs-lookup"><span data-stu-id="f2ee5-108">Confirm that the reply URL is correctly configured in the Azure AD B2C application</span></span>

<span data-ttu-id="f2ee5-109">Voit vahvistaa, että vastauksen URL-osoite on määritetty oikein Azure AD B2C -sovelluksessa, toimimalla seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="f2ee5-109">To confirm that the reply URL is correctly configured in the Azure AD B2C application, follow these steps.</span></span>

1. <span data-ttu-id="f2ee5-110">Siirry [Azure-portaaliin](https://portal.azure.com/).</span><span class="sxs-lookup"><span data-stu-id="f2ee5-110">Go to the [Azure portal](https://portal.azure.com/).</span></span>
1. <span data-ttu-id="f2ee5-111">Valitse Azure AD B2C -sovellus, jonka loit sivuston käyttöön.</span><span class="sxs-lookup"><span data-stu-id="f2ee5-111">Select the Azure AD B2C application that you created for your site access.</span></span>
1. <span data-ttu-id="f2ee5-112">Valitse sovellus, jonka olet luonut Azure AD B2C -asetusten yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="f2ee5-112">Select the application that you created during the Azure AD B2C setup.</span></span>
1. <span data-ttu-id="f2ee5-113">Varmista **Vastauksen URL-osoite** -kohdassa, että luettelossa on sekä sivuston toimialueen URL-osoite että sähköisen kaupankäynnin luoman URL-osoitteen merkinnät seuraavan kuvan mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="f2ee5-113">Under **Reply URL**, make sure that the list includes entries for both the site domain URL and the e-commerce-generated URL, as shown in the example in the following illustration.</span></span>

    ![Azure AD B2C:n Vastauksen URL-osoite -merkinnät](media/aad-b2c-reply-url.jpg)

> [!NOTE]
> <span data-ttu-id="f2ee5-115">Sekä sivuston toimialueen URL-osoitteen että sähköisen kaupankäynnin luoman URL-osoitteen on oltava kelvollisessa URL-muodossa, jossa ei ole vinoviivoja lopussa eikä alussa.</span><span class="sxs-lookup"><span data-stu-id="f2ee5-115">Both the site domain URL and the e-commerce-generated URL must be in a valid URL format that doesn't include leading or trailing slashes.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f2ee5-116">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="f2ee5-116">Additional resources</span></span>

[<span data-ttu-id="f2ee5-117">Verkkosovelluksen rekisteröiminen Azure Active Directory B2C:ssä</span><span class="sxs-lookup"><span data-stu-id="f2ee5-117">Register a web application in Azure Active Directory B2C</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/tutorial-register-applications?tabs=app-reg-ga#register-a-web-application)

[<span data-ttu-id="f2ee5-118">Kuluttajakaupan vuokraajan määrittäminen Commercessa</span><span class="sxs-lookup"><span data-stu-id="f2ee5-118">Set up a B2C tenant in Commerce</span></span>](../set-up-b2c-tenant.md)
