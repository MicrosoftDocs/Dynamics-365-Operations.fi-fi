---
title: Mukautettujen sivujen määrittäminen käyttäjän sisäänkirjautumisia varten
description: Tässä ohjeaiheessa kerrotaan, miten Microsoft Dynamics 365 Commercessa luodaan mukautettuja sivuja, jotka käsittelevät Azure Active Directoryn (Azure AD) kuluttajakaupan (B2C) vuokraajien mukautettuja sisäänkirjauksia.
author: brianshook
manager: annbe
ms.date: 06/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 71c0f0b6969985b04262b522dd2165eb1475878d
ms.sourcegitcommit: 9a2e9f7dfec47c42178bb67a3e099e610515baf3
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/16/2020
ms.locfileid: "3456969"
---
# <a name="set-up-custom-pages-for-user-sign-ins"></a><span data-ttu-id="b5b57-103">Mukautettujen sivujen määrittäminen käyttäjän sisäänkirjautumisia varten</span><span class="sxs-lookup"><span data-stu-id="b5b57-103">Set up custom pages for user sign-ins</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="b5b57-104">Tässä ohjeaiheessa kerrotaan, miten Microsoft Dynamics 365 Commercessa luodaan mukautettuja sivuja, jotka käsittelevät Azure Active Directoryn (Azure AD) kuluttajakaupan (B2C) vuokraajien mukautettuja sisäänkirjauksia.</span><span class="sxs-lookup"><span data-stu-id="b5b57-104">This topic describes how to build custom pages in Microsoft Dynamics 365 Commerce that handle customized sign-ins for users of Azure Active Directory (Azure AD) business-to-consumer (B2C) tenants.</span></span>

## <a name="overview"></a><span data-ttu-id="b5b57-105">Yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="b5b57-105">Overview</span></span>

<span data-ttu-id="b5b57-106">Jotta Dynamics 365 Commercessa tehdyt mukautetut sivut voivat käyttää käyttäjän sisäänkirjausten työnkulkuja, Commerce-ympäristössä viitattavat Azure AD -käytännöt on määritettävä.</span><span class="sxs-lookup"><span data-stu-id="b5b57-106">To use custom pages that are authored in Dynamics 365 Commerce to handle user sign-in flows, you must set up the Azure AD policies that will be referenced in the Commerce environment.</span></span> <span data-ttu-id="b5b57-107">Voit määrittää Azure AD:n kuluttajakaupan Rekisteröinti ja sisäänkirjaus-, Profiilin muokkaus- ja Sanasanan nollaus -käytännöt käyttämällä Azure AD:n kuluttajakaupan sovellusta.</span><span class="sxs-lookup"><span data-stu-id="b5b57-107">You can configure the "Sign up and sign in," "Profile editing," and "Password reset" Azure AD B2C policies by using the Azure AD B2C application.</span></span> <span data-ttu-id="b5b57-108">Azure AD:n kuluttajakaupan vuokraajan ja käytännön nimiin ei voi viitata valmisteluprosessin aikana, kun se tehdään Commerce-ympäristössä Microsoft Dynamics Lifecycle Services (LCS) -palvelun avulla.</span><span class="sxs-lookup"><span data-stu-id="b5b57-108">The Azure AD B2C tenant and policy names can then be referenced during the provisioning process that is done for the Commerce environment by using Microsoft Dynamics Lifecycle Services (LCS).</span></span>

<span data-ttu-id="b5b57-109">Mukautetut Commerce-sivut voidaan luoda käyttämällä sisäänkirjauksen, rekisteröinnin, tiliprofiilin muokkauksen tai salasanan nollauksen moduulia.</span><span class="sxs-lookup"><span data-stu-id="b5b57-109">The custom Commerce pages can be built by using the sign in, sign up, account profile edit, or password reset module.</span></span> <span data-ttu-id="b5b57-110">Näille mukautetuille sivuille julkaistaviin sivun URL-osoitteisiin on tämän jälkeen viitattava Azure AD:n kuluttajakaupan käytännön määrityksissä Azure-portaalissa.</span><span class="sxs-lookup"><span data-stu-id="b5b57-110">The page URLs that are published for these custom pages should then be referenced in Azure AD B2C policy configurations in the Azure portal.</span></span>

## <a name="set-up-b2c-policies"></a><span data-ttu-id="b5b57-111">Kuluttajakaupan käytäntöjen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="b5b57-111">Set up B2C policies</span></span>

<span data-ttu-id="b5b57-112">Kun olet määrittänyt Azure AD:n kuluttajakaupan vuokraajan ja liittänyt sen Commerce-ympäristöön, siirry **Azure AD:n kuluttajakauppa** -sivulla Azure-portaalissa ja valitse sitten **Käytännöt**-kohdassa **Käyttäjän työnkulut (käytännöt)**.</span><span class="sxs-lookup"><span data-stu-id="b5b57-112">After you set up your Azure AD B2C tenant and associate it with your Commerce environment, go to the **Azure AD B2C** page in the Azure portal, and then, on the menu, under **Policies**, select **User flows (policies)**.</span></span>

![Käyttäjän työnkulut (käytännöt) -komento valikossa](./media/B2C_CustomPage_PoliciesMenu.png)

<span data-ttu-id="b5b57-114">Nyt voit määrittää käyttäjän Rekisteröinti ja sisäänkirjaus-, Profiilin muokkaus ja Salasanan nollaus -työnkulut.</span><span class="sxs-lookup"><span data-stu-id="b5b57-114">You can now configure the "Sign up and sign in," "Profile editing," and "Password reset" user sign-in flows.</span></span>

### <a name="configure-the-sign-up-and-sign-in-policy"></a><span data-ttu-id="b5b57-115">Rekisteröinti ja sisäänkirjaus -käytännön määrittäminen</span><span class="sxs-lookup"><span data-stu-id="b5b57-115">Configure the "Sign up and sign in" policy</span></span>

<span data-ttu-id="b5b57-116">Voit määrittää Rekisteröinti ja sisäänkirjaus -käytännön seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="b5b57-116">To configure the "Sign up and sign in" policy, follow these steps.</span></span>

1. <span data-ttu-id="b5b57-117">Valitse **Uusi käyttäjän työnkulku** ja valitse sitten **Suositellut**-välilehdessä **Rekisteröinti ja sisäänkirjaus** -käytäntö.</span><span class="sxs-lookup"><span data-stu-id="b5b57-117">Select **New user flow**, and then, on the **Recommended** tab, select the **Sign up and sign in** policy.</span></span>
1. <span data-ttu-id="b5b57-118">Syötä käytännön nimi (esimerkiksi **B2C\_1\_SignInSignUp**).</span><span class="sxs-lookup"><span data-stu-id="b5b57-118">Enter a name for the policy (for example, **B2C\_1\_SignInSignUp**).</span></span>
1. <span data-ttu-id="b5b57-119">Valitse **Tunnistetietojen toimittajat** -osassa käytännön kanssa käytettävät tunnistetietojen toimittajat.</span><span class="sxs-lookup"><span data-stu-id="b5b57-119">In the **Identity Providers** section, select the identity providers to use for the policy.</span></span> <span data-ttu-id="b5b57-120">Vähintään **Sähköpostirekisteröityminen** on valittava.</span><span class="sxs-lookup"><span data-stu-id="b5b57-120">At a minimum, **Email signup** must be selected.</span></span>
1. <span data-ttu-id="b5b57-121">Valitse **Kerää määrite** -sarakkeessa **Sähköpostiosoite**-, **Etunimi**- ja **Sukunimi**-valintaruudut.</span><span class="sxs-lookup"><span data-stu-id="b5b57-121">In the **Collect attribute** column, select the check boxes for **Email Address**, **Given Name**, and **Surname**.</span></span>
1. <span data-ttu-id="b5b57-122">Valitse **Palauta vaatimus** -sarakkeessa **Sähköpostiosoitteet**-, **Etunimi**-, **Tunnistetietojen tarjoaja**-, **Sukunimi**- ja **Käyttäjän objektin tunnus** -valintaruudut.</span><span class="sxs-lookup"><span data-stu-id="b5b57-122">In the **Return claim** column, select the check boxes for **Email Addresses**, **Given Name**, **Identity Provider**, **Surname**, and **User's Object ID**.</span></span>

    ![Valitut määritteet ja vaatimukset](./media/B2C_SignInSignUp_Attributes.png)

1. <span data-ttu-id="b5b57-124">Valitse **OK**, kun haluat luoda käytännön.</span><span class="sxs-lookup"><span data-stu-id="b5b57-124">Select **OK** to create the policy.</span></span>
1. <span data-ttu-id="b5b57-125">Kaksoisnapsauta uuden käytännön nimeä ja valitse siirtymisruudussa **Ominaisuudet**.</span><span class="sxs-lookup"><span data-stu-id="b5b57-125">Double-click the new policy name, and then, in the navigation pane, select **Properties**.</span></span>
1. <span data-ttu-id="b5b57-126">Määritä **Ota JavaScriptia käyttävä sivun asettelu käyttöön (esikatselu)** -asetuksen arvoksi **Käytössä**.</span><span class="sxs-lookup"><span data-stu-id="b5b57-126">Set the **Enable JavaScript enforcing page layout (preview)** option to **On**.</span></span>

    ![Uuden käytännön Ominaisuudet-sivu](./media/B2C_SignInSignUp_EnableJavascript.png)

> [!NOTE]
> <span data-ttu-id="b5b57-128">Käytännön nimeen viitataan täysin Commerce-ympäristössä.</span><span class="sxs-lookup"><span data-stu-id="b5b57-128">The policy name will be fully referenced in the Commerce environment.</span></span> <span data-ttu-id="b5b57-129">(**B2C\_1\_**-etuliite sisällytetään viitteeseen.) Käytäntöjä ei voi nimetä uudelleen luomisen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="b5b57-129">(The **B2C\_1\_** prefix will be included in the reference.) Policies can't be renamed after they are created.</span></span> <span data-ttu-id="b5b57-130">Jos korvaat Commerce-ympäristön olemassa olevan käytännön, voit poistaa alkuperäisen käytännön ja luoda uuden käytännön, jolla on sama nimi.</span><span class="sxs-lookup"><span data-stu-id="b5b57-130">If you're replacing an existing policy for your Commerce environment, you can delete the original policy and build a new policy that has the same name.</span></span> <span data-ttu-id="b5b57-131">Vaihtoehtoisesti, jos ympäristö on jo valmisteltu, voit lähettää uuden käytännön nimen palvelupyynnön kautta.</span><span class="sxs-lookup"><span data-stu-id="b5b57-131">Alternatively, if the environment has already been provisioned, you can submit the new policy name through a service request.</span></span>

<span data-ttu-id="b5b57-132">Palaa tähän käytäntöön ja tee määritykset loppuun, kun mukautetut sivut on luotu.</span><span class="sxs-lookup"><span data-stu-id="b5b57-132">You will return to this policy to finish the setup after you've built the custom pages.</span></span> <span data-ttu-id="b5b57-133">Nyt voit sulkea käytännön ja palata **Käyttäjän työnkulut (käytännöt)** -sivulle Azure-portaalissa.</span><span class="sxs-lookup"><span data-stu-id="b5b57-133">For now, close the policy to return to the **User flows (policies)** page in the Azure portal.</span></span>

### <a name="configure-the-profile-editing-policy"></a><span data-ttu-id="b5b57-134">Profiilin muokkaus -käytännön määrittäminen</span><span class="sxs-lookup"><span data-stu-id="b5b57-134">Configure the "Profile editing" policy</span></span>

<span data-ttu-id="b5b57-135">Voit määrittää Profiilin muokkaus -käytännön seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="b5b57-135">To configure the "Profile editing" policy, follow these steps.</span></span>

1. <span data-ttu-id="b5b57-136">Valitse **Uusi käyttäjän työnkulku** ja valitse sitten **Suositellut**-välilehdessä **Profiilin muokkaus** -käytäntö.</span><span class="sxs-lookup"><span data-stu-id="b5b57-136">Select **New user flow**, and then, on the **Recommended** tab, select the **Profile editing** policy.</span></span>
1. <span data-ttu-id="b5b57-137">Syötä käytännön nimi (esimerkiksi **B2C\_1\_EditProfile**).</span><span class="sxs-lookup"><span data-stu-id="b5b57-137">Enter a name for the policy (for example, **B2C\_1\_EditProfile**).</span></span>
1. <span data-ttu-id="b5b57-138">Valitse **Tunnistetietojen toimittajat** -osassa käytännön kanssa käytettävät tunnistetietojen toimittajat.</span><span class="sxs-lookup"><span data-stu-id="b5b57-138">In the **Identity Providers** section, select the identity providers to use for the policy.</span></span> <span data-ttu-id="b5b57-139">Vähintään **Paikallisen tilin sisäänkirjaus** on valittava.</span><span class="sxs-lookup"><span data-stu-id="b5b57-139">At a minimum, **Local Account SignIn** must be selected.</span></span>
1. <span data-ttu-id="b5b57-140">Valitse **Kerää määrite** -sarakkeessa **Sähköpostiosoitteet**- ja **Sukunimi**-valintaruudut.</span><span class="sxs-lookup"><span data-stu-id="b5b57-140">In the **Collect attribute** column, select the check boxes for **Email Addresses** and **Surname**.</span></span>
1. <span data-ttu-id="b5b57-141">Valitse **Palauta vaatimus** -sarakkeessa **Sähköpostiosoitteet**-, **Etunimi**-, **Tunnistetietojen tarjoaja**-, **Sukunimi**- ja **Käyttäjän objektin tunnus** -valintaruudut.</span><span class="sxs-lookup"><span data-stu-id="b5b57-141">In the **Return claim** column, select the check boxes for **Email Addresses**, **Given Name**, **Identity Provider**, **Surname**, and **User's Object ID**.</span></span>
1. <span data-ttu-id="b5b57-142">Valitse **OK**, kun haluat luoda käytännön.</span><span class="sxs-lookup"><span data-stu-id="b5b57-142">Select **OK** to create the policy.</span></span>
1. <span data-ttu-id="b5b57-143">Kaksoisnapsauta uuden käytännön nimeä ja valitse siirtymisruudussa **Ominaisuudet**.</span><span class="sxs-lookup"><span data-stu-id="b5b57-143">Double-click the new policy name, and then, in the navigation pane, select **Properties**.</span></span>
1. <span data-ttu-id="b5b57-144">Määritä **Ota JavaScriptia käyttävä sivun asettelu käyttöön (esikatselu)** -asetuksen arvoksi **Käytössä**.</span><span class="sxs-lookup"><span data-stu-id="b5b57-144">Set the **Enable JavaScript enforcing page layout (preview)** option to **On**.</span></span>

<span data-ttu-id="b5b57-145">Palaa tähän käytäntöön ja tee määritykset loppuun, kun mukautetut sivut on luotu.</span><span class="sxs-lookup"><span data-stu-id="b5b57-145">You will return to this policy to finish the setup after you've built the custom pages.</span></span> <span data-ttu-id="b5b57-146">Nyt voit sulkea käytännön ja palata **Käyttäjän työnkulut (käytännöt)** -sivulle Azure-portaalissa.</span><span class="sxs-lookup"><span data-stu-id="b5b57-146">For now, close the policy to return to the **User flows (policies)** page in the Azure portal.</span></span>

### <a name="configure-the-password-reset-policy"></a><span data-ttu-id="b5b57-147">Salasanan nollaus -käytännön määrittäminen</span><span class="sxs-lookup"><span data-stu-id="b5b57-147">Configure the "Password reset" policy</span></span>

<span data-ttu-id="b5b57-148">Voit määrittää Salasanan nollaus -käytännön seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="b5b57-148">To configure the "Password reset" policy, follow these steps.</span></span>

1. <span data-ttu-id="b5b57-149">Valitse **Uusi käyttäjän työnkulku** ja valitse sitten **Esikatselu**-välilehdessä **Salasanan nollaus versio 1.1** -käytäntö.</span><span class="sxs-lookup"><span data-stu-id="b5b57-149">Select **New user flow**, and then, on the **Preview** tab, select the **Password reset v1.1** policy.</span></span>

    ![Salasanan nollaus versio 1.1 -käytäntö valittuna Esikatselu-välilehdessä](./media/B2C_ForgetPassword_Menu.png)

1. <span data-ttu-id="b5b57-151">Syötä käytännön nimi (esimerkiksi **B2C\_1\_ForgetPassword**).</span><span class="sxs-lookup"><span data-stu-id="b5b57-151">Enter a name for the policy (for example, **B2C\_1\_ForgetPassword**).</span></span>
1. <span data-ttu-id="b5b57-152">Valitse **Tunnistetietojen tarjoajat** -osassa **Nollaa salasana sähköpostiosoitteen avulla**.</span><span class="sxs-lookup"><span data-stu-id="b5b57-152">In the **Identity Providers** section, select **Reset password using email address**.</span></span>
1. <span data-ttu-id="b5b57-153">Valitse **Palauta vaatimus** -sarakkeessa **Sähköpostiosoitteet**-, **Etunimi**, **Sukunimi**- ja **Käyttäjän objektin tunnus** valintaruudut.</span><span class="sxs-lookup"><span data-stu-id="b5b57-153">In the **Return claim** column, select the check boxes for **Email Addresses**, **Given Name**, **Surname**, and **User's Object ID**.</span></span>

    ![Valitut vaatimukset](./media/B2C_ForgetPassword_Attributes.png)

1. <span data-ttu-id="b5b57-155">Valitse **OK**, kun haluat luoda käytännön.</span><span class="sxs-lookup"><span data-stu-id="b5b57-155">Select **OK** to create the policy.</span></span>
1. <span data-ttu-id="b5b57-156">Kaksoisnapsauta uuden käytännön nimeä ja valitse siirtymisruudussa **Ominaisuudet**.</span><span class="sxs-lookup"><span data-stu-id="b5b57-156">Double-click the new policy name, and then, in the navigation pane, select **Properties**.</span></span>
1. <span data-ttu-id="b5b57-157">Määritä **Ota JavaScriptia käyttävä sivun asettelu käyttöön (esikatselu)** -asetuksen arvoksi **Käytössä**.</span><span class="sxs-lookup"><span data-stu-id="b5b57-157">Set the **Enable JavaScript enforcing page layout (preview)** option to **On**.</span></span>

<span data-ttu-id="b5b57-158">Palaa tähän käytäntöön ja tee määritykset loppuun, kun mukautetut sivut on luotu.</span><span class="sxs-lookup"><span data-stu-id="b5b57-158">You will return to this policy to finish the setup after you've built the custom pages.</span></span> <span data-ttu-id="b5b57-159">Nyt voit sulkea käytännön ja palata **Käyttäjän työnkulut (käytännöt)** -sivulle Azure-portaalissa.</span><span class="sxs-lookup"><span data-stu-id="b5b57-159">For now, close the policy to return to the **User flows (policies)** page in the Azure portal.</span></span>

## <a name="build-the-custom-pages"></a><span data-ttu-id="b5b57-160">Mukautettujen sivujen luominen</span><span class="sxs-lookup"><span data-stu-id="b5b57-160">Build the custom pages</span></span>

<span data-ttu-id="b5b57-161">Voit luoda mukautettuja sivuja käyttäjän sisäänkirjausten käsittelemistä varten seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="b5b57-161">To build the custom pages to handle user sign-ins, follow these steps.</span></span>

1. <span data-ttu-id="b5b57-162">Siirry Commerce-muokkaustyökalut-kohdassa sivustoon.</span><span class="sxs-lookup"><span data-stu-id="b5b57-162">In the Commerce authoring tools, go to your site.</span></span>
1. <span data-ttu-id="b5b57-163">Muodosta seuraavat viisi mallia ja sivua:</span><span class="sxs-lookup"><span data-stu-id="b5b57-163">Build the following five templates and five pages:</span></span>

    - <span data-ttu-id="b5b57-164">**Sisäänkirjaus**-malli ja -sivu, jotka käyttävät sisäänkirjauksen moduulia.</span><span class="sxs-lookup"><span data-stu-id="b5b57-164">A **Sign In** template and page that use the sign in module.</span></span>
    - <span data-ttu-id="b5b57-165">**Rekisteröinti**-malli ja -sivu, jotka käyttävät rekisteröinnin moduulia.</span><span class="sxs-lookup"><span data-stu-id="b5b57-165">A **Sign Up** template and page that use the sign up module.</span></span>
    - <span data-ttu-id="b5b57-166">**Salasanan nollaus** -malli ja -sivu, jotka käyttävät salasanan nollauksen moduulia.</span><span class="sxs-lookup"><span data-stu-id="b5b57-166">A **Password Reset** template and page that use the password reset module.</span></span>
    - <span data-ttu-id="b5b57-167">**Salasanan nollauksen vahvistus** -malli ja -sivu, jotka käyttävät salasanan nollauksen vahvistuksen moduulia.</span><span class="sxs-lookup"><span data-stu-id="b5b57-167">A **Password Reset verification** template and page that use the password reset verification module.</span></span>
    - <span data-ttu-id="b5b57-168">**Profiilin muokkaus** -malli ja -sivu, jotka käyttävät tiliprofiilin muokkauksen moduulia</span><span class="sxs-lookup"><span data-stu-id="b5b57-168">A **Profile Edit** template and page that use the account profile edit module</span></span>

<span data-ttu-id="b5b57-169">Kun luot sivuja, noudata seuraavia ohjeita:</span><span class="sxs-lookup"><span data-stu-id="b5b57-169">When you build the pages, follow these guidelines:</span></span>

- <span data-ttu-id="b5b57-170">Käytä kunkin sivun tai moduulin kohdalla asettelua ja tyyliä, joka sopii parhaiten liiketoiminnan vaatimuksiin.</span><span class="sxs-lookup"><span data-stu-id="b5b57-170">For each page or module, use the layout and style that best suit your business requirements.</span></span>
- <span data-ttu-id="b5b57-171">Julkaise kaikki sivut ja URL-osoitteet, joita on käytettävä Azure AD:n kuluttajakaupan määrityksessä.</span><span class="sxs-lookup"><span data-stu-id="b5b57-171">Publish all pages and URLs that must be used in the Azure AD B2C setup.</span></span>
- <span data-ttu-id="b5b57-172">Kun sivut ja URL-osoitteet on julkaistu, kerää Azure AD:n kuluttajakaupan käytännön määrityksessä käytettävät URL-osoitteet.</span><span class="sxs-lookup"><span data-stu-id="b5b57-172">After the pages and URLs are published, collect the URLs that must be used for the Azure AD B2C policy configurations.</span></span> <span data-ttu-id="b5b57-173">Jälkiliite **?preloadscripts=true** lisätään jokaiseen URL-osoitteeseen käytön yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="b5b57-173">A **?preloadscripts=true** suffix will be added to every URL when it's used.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b5b57-174">Älä käytä universaaleja ylä- ja alatunnisteita, joissa on suhteellisia linkkejä.</span><span class="sxs-lookup"><span data-stu-id="b5b57-174">Don't reuse universal headers and footers that have relative links.</span></span> <span data-ttu-id="b5b57-175">Koska Azure AD:n kuluttajakaupan toimialue isännöi näitä sivuja käytön yhteydessä, kaikissa linkeissä tulisi käyttää vain absoluuttisia URL-osoitteita.</span><span class="sxs-lookup"><span data-stu-id="b5b57-175">Because these pages will be hosted in the Azure AD B2C domain when they are used, only absolute URLs should be used for all links.</span></span>

## <a name="configure-azure-ad-b2c-policies-with-custom-page-information"></a><span data-ttu-id="b5b57-176">Azure AD:n kuluttajakaupan käytäntöjen ja mukautetun sivun tietojen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="b5b57-176">Configure Azure AD B2C policies with custom page information</span></span> 

<span data-ttu-id="b5b57-177">Palaa Azure-portaalissa **Azure AD:n kuluttajakauppa** -sivulla ja valitse **Käytännöt**-kohdassa valikosta **Käyttäjän työnkulut (käytännöt)**.</span><span class="sxs-lookup"><span data-stu-id="b5b57-177">In the Azure portal, return to the **Azure AD B2C** page, and then, on the menu, under **Policies**, select **User flows (policies)**.</span></span>

### <a name="update-the-sign-up-and-sign-in-policy-with-custom-page-information"></a><span data-ttu-id="b5b57-178">Rekisteröidy ja kirjaudu -käytännön päivittäminen mukautetun sivun tiedoilla</span><span class="sxs-lookup"><span data-stu-id="b5b57-178">Update the "Sign up and sign in" policy with custom page information</span></span>

<span data-ttu-id="b5b57-179">Voit päivittää Rekisteröinti ja sisäänkirjaus -käytännön mukautetun sivun tiedoilla seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="b5b57-179">To update the "Sign up and sign in" policy with custom page information, follow these steps.</span></span>

1. <span data-ttu-id="b5b57-180">Valitse aiemmin määritetyn **Rekisteröinti ja sisäänkirjaus** -käytännön siirtymisruudussa **Sivun asettelut**.</span><span class="sxs-lookup"><span data-stu-id="b5b57-180">In the **Sign in and sign up** policy that you configured earlier, in the navigation pane, select **Page layouts**.</span></span>
1. <span data-ttu-id="b5b57-181">Valitse **Yhtenäinen rekisteröinti tai sisäänkirjaus -sivu** -asettelu</span><span class="sxs-lookup"><span data-stu-id="b5b57-181">Select the **Unified sign up or sign in page** layout.</span></span>
1. <span data-ttu-id="b5b57-182">Määritä **Käytä mukautettua sivun sisältöä** -asetukseksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="b5b57-182">Set the **Use custom page content** option to **Yes**.</span></span>
1. <span data-ttu-id="b5b57-183">Syötä **Mukautetun sivun URI** -kenttään sisäänkirjauksen täydellinen URL-osoite.</span><span class="sxs-lookup"><span data-stu-id="b5b57-183">In the **Custom page URI** field, enter the full sign-in URL.</span></span> <span data-ttu-id="b5b57-184">Sisällytä jälkiliite **?preloadscripts=true**.</span><span class="sxs-lookup"><span data-stu-id="b5b57-184">Include the **?preloadscripts=true** suffix.</span></span> <span data-ttu-id="b5b57-185">Syötä arvoksi esimerkiksi ``www.<my domain>.com/sign-in?preloadscripts=true``.</span><span class="sxs-lookup"><span data-stu-id="b5b57-185">For example, enter ``www.<my domain>.com/sign-in?preloadscripts=true``.</span></span>
1. <span data-ttu-id="b5b57-186">Valitse **Sivun asettelun versio (esikatselu)** -kentässä **1.2.0**.</span><span class="sxs-lookup"><span data-stu-id="b5b57-186">In the **Page Layout Version (Preview)** field, select **1.2.0**.</span></span>
1. <span data-ttu-id="b5b57-187">Valitse **Paikallisen tilin rekisteröinti -sivu** -asettelu.</span><span class="sxs-lookup"><span data-stu-id="b5b57-187">Select the **Local account sign up page** layout.</span></span>
1. <span data-ttu-id="b5b57-188">Määritä **Käytä mukautettua sivun sisältöä** -asetukseksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="b5b57-188">Set the **Use custom page content** option to **Yes**.</span></span>
1. <span data-ttu-id="b5b57-189">Syötä **Mukautetun sivun URI** -kenttään rekisteröitymisen täydellinen URL-osoite.</span><span class="sxs-lookup"><span data-stu-id="b5b57-189">In the **Custom page URI** field, enter the full sign-up URL.</span></span> <span data-ttu-id="b5b57-190">Sisällytä jälkiliite **?preloadscripts=true**.</span><span class="sxs-lookup"><span data-stu-id="b5b57-190">Include the **?preloadscripts=true** suffix.</span></span> <span data-ttu-id="b5b57-191">Syötä arvoksi esimerkiksi ``www.<my domain>.com/sign-up?preloadscripts=true``.</span><span class="sxs-lookup"><span data-stu-id="b5b57-191">For example, enter ``www.<my domain>.com/sign-up?preloadscripts=true``.</span></span>
1. <span data-ttu-id="b5b57-192">Valitse **Sivun asettelun versio (esikatselu)** -kentässä **1.2.0**.</span><span class="sxs-lookup"><span data-stu-id="b5b57-192">In the **Page Layout Version (Preview)** field, select **1.2.0**.</span></span>
1. <span data-ttu-id="b5b57-193">Tee seuraavat toiminnot **Käyttäjän määritteet** -osassa:</span><span class="sxs-lookup"><span data-stu-id="b5b57-193">In the **User attributes** section, follow these steps:</span></span>

    1. <span data-ttu-id="b5b57-194">Valitse **Sähköpostiosoite**-, **Etunimi**- ja **Sukunimi**-määritteille **Ei**-arvo **Vaatii tarkistuksen** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="b5b57-194">For the **Email Address**, **Given Name**, and **Surname** attributes, select **No** in the **Requires Verification** field.</span></span>
    1. <span data-ttu-id="b5b57-195">Valitse **Etunimi**- ja **Sukunimi**-määritteille **Ei**-arvo **Valinnainen**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="b5b57-195">For the **Given Name** and **Surname** attributes, select **No** in the **Optional** field.</span></span>

    ![Paikallisen tilin rekisteröinti -sivun käytännön määrittäminen](./media/B2C_SignUp_PageURLConfig.png)

### <a name="update-the-profile-editing-policy-with-custom-page-information"></a><span data-ttu-id="b5b57-197">Profiilin muokkaus -käytännön päivittäminen mukautetun sivun tiedoilla</span><span class="sxs-lookup"><span data-stu-id="b5b57-197">Update the "Profile editing" policy with custom page information</span></span>

<span data-ttu-id="b5b57-198">Voit päivittää Profiilin muokkaus -käytännön mukautetun sivun tiedoilla seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="b5b57-198">To update the "Profile editing" policy with custom page information, follow these steps.</span></span>

1. <span data-ttu-id="b5b57-199">Valitse aiemmin määritetyn **Profiilin muokkaus** -käytännön siirtymisruudussa **Sivun asettelut**.</span><span class="sxs-lookup"><span data-stu-id="b5b57-199">In the **Profile Editing** policy that you configured earlier, in the navigation pane, select **Page layouts**.</span></span>
1. <span data-ttu-id="b5b57-200">Valitse **Profiilin muokkaus -sivu** -asettelu.</span><span class="sxs-lookup"><span data-stu-id="b5b57-200">Select the **Profile edit page** layout.</span></span>
1. <span data-ttu-id="b5b57-201">Määritä **Käytä mukautettua sivun sisältöä** -asetukseksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="b5b57-201">Set the **Use custom page content** option to **Yes**.</span></span>
1. <span data-ttu-id="b5b57-202">Syötä **Mukautetun sivun URI** -kenttään profiilin muokkaussivun täydellinen URL-osoite.</span><span class="sxs-lookup"><span data-stu-id="b5b57-202">In the **Custom page URI** field, enter the full profile edit URL.</span></span> <span data-ttu-id="b5b57-203">Sisällytä jälkiliite **?preloadscripts=true**.</span><span class="sxs-lookup"><span data-stu-id="b5b57-203">Include the **?preloadscripts=true** suffix.</span></span> <span data-ttu-id="b5b57-204">Syötä arvoksi esimerkiksi ``www.<my domain>.com/profile-edit?preloadscripts=true``.</span><span class="sxs-lookup"><span data-stu-id="b5b57-204">For example, enter ``www.<my domain>.com/profile-edit?preloadscripts=true``.</span></span>
1. <span data-ttu-id="b5b57-205">Valitse **Sivun asettelun versio (esikatselu)** -kentässä **1.2.0**.</span><span class="sxs-lookup"><span data-stu-id="b5b57-205">In the **Page Layout Version (Preview)** field, select **1.2.0**.</span></span>
1. <span data-ttu-id="b5b57-206">Tee seuraavat toiminnot **Käyttäjän määritteet** -osassa:</span><span class="sxs-lookup"><span data-stu-id="b5b57-206">In the **User attributes** section, follow these steps:</span></span>

    1. <span data-ttu-id="b5b57-207">Valitse **Sähköpostiosoite**- ja **Etunimi**-määritteille **Ei**-arvo **Vaatii tarkistuksen** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="b5b57-207">For the **Email Address**, **Given Name** attributes, select **No** in the **Requires Verification** field.</span></span>
    1. <span data-ttu-id="b5b57-208">Valitse **Etunimi**- ja **Sukunimi**-määritteille **Ei**-arvo **Valinnainen**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="b5b57-208">For the **Given Name** and **Surname** attributes, select **No** in the **Optional** field.</span></span>

### <a name="update-the-password-reset-policy-with-custom-page-information"></a><span data-ttu-id="b5b57-209">Salasanan nollaus -käytännön päivittäminen mukautetun sivun tiedoilla</span><span class="sxs-lookup"><span data-stu-id="b5b57-209">Update the "Password reset" policy with custom page information</span></span>

<span data-ttu-id="b5b57-210">Voit päivittää Salasanan nollaus -käytännön mukautetun sivun tiedoilla seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="b5b57-210">To update the "Password reset" policy with custom page information, follow these steps.</span></span>

1. <span data-ttu-id="b5b57-211">Valitse aiemmin määritetyn **Salasanan nollaus** -käytännön siirtymisruudussa **Sivun asettelut**.</span><span class="sxs-lookup"><span data-stu-id="b5b57-211">In the **Password Reset** policy that you configured earlier, in the navigation pane, select **Page layouts**.</span></span>
1. <span data-ttu-id="b5b57-212">Valitse **Uusi salasana -sivu** -asettelu.</span><span class="sxs-lookup"><span data-stu-id="b5b57-212">Select the **New password page** layout.</span></span>
1. <span data-ttu-id="b5b57-213">Määritä **Käytä mukautettua sivun sisältöä** -asetukseksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="b5b57-213">Set the **Use custom page content** option to **Yes**.</span></span>
1. <span data-ttu-id="b5b57-214">Syötä **Mukautetun sivun URI** -kenttään salasanan palauttamisen täydellinen URL-osoite.</span><span class="sxs-lookup"><span data-stu-id="b5b57-214">In the **Custom page URI** field, enter the full password reset URL.</span></span> <span data-ttu-id="b5b57-215">Sisällytä jälkiliite **?preloadscripts=true**.</span><span class="sxs-lookup"><span data-stu-id="b5b57-215">Include the **?preloadscripts=true** suffix.</span></span> <span data-ttu-id="b5b57-216">Syötä arvoksi esimerkiksi ``www.<my domain>.com/passwordreset?preloadscripts=true``.</span><span class="sxs-lookup"><span data-stu-id="b5b57-216">For example, enter ``www.<my domain>.com/passwordreset?preloadscripts=true``.</span></span>
1. <span data-ttu-id="b5b57-217">Valitse **Sivun asettelun versio (esikatselu)** -kentässä **1.2.0**.</span><span class="sxs-lookup"><span data-stu-id="b5b57-217">In the **Page Layout Version (Preview)** field, select **1.2.0**.</span></span>
1. <span data-ttu-id="b5b57-218">Valitse **Tilin tarkistus -sivu** -asettelu.</span><span class="sxs-lookup"><span data-stu-id="b5b57-218">Select the **Account verification page** layout.</span></span>
1. <span data-ttu-id="b5b57-219">Määritä **Käytä mukautettua sivun sisältöä** -asetukseksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="b5b57-219">Set the **Use custom page content** option to **Yes**.</span></span>
1. <span data-ttu-id="b5b57-220">Syötä **Mukautetun sivun URI** -kenttään salasanan palauttamisen todentamisen URL-osoite.</span><span class="sxs-lookup"><span data-stu-id="b5b57-220">In the **Custom page URI** field, enter the full password reset verification URL.</span></span> <span data-ttu-id="b5b57-221">Sisällytä jälkiliite **?preloadscripts=true**.</span><span class="sxs-lookup"><span data-stu-id="b5b57-221">Include the **?preloadscripts=true** suffix.</span></span> <span data-ttu-id="b5b57-222">Syötä arvoksi esimerkiksi ``www.<my domain>.com/passwordreset-verification?preloadscripts=true``.</span><span class="sxs-lookup"><span data-stu-id="b5b57-222">For example, enter ``www.<my domain>.com/passwordreset-verification?preloadscripts=true``.</span></span>
1. <span data-ttu-id="b5b57-223">Valitse **Sivun asettelun versio (esikatselu)** -kentässä **1.2.0**.</span><span class="sxs-lookup"><span data-stu-id="b5b57-223">In the **Page Layout Version (Preview)** field, select **1.2.0**.</span></span>



## <a name="customize-default-text-strings-for-labels-and-descriptions"></a><span data-ttu-id="b5b57-224">Otsikoiden ja kuvausten oletustekstimerkkijonojen mukauttaminen</span><span class="sxs-lookup"><span data-stu-id="b5b57-224">Customize default text strings for labels and descriptions</span></span>

<span data-ttu-id="b5b57-225">Aloituspakkauksen sisäänkirjausmoduulit täytetään etukäteen otsikoiden ja kuvausten oletustekstimerkkijonoilla.</span><span class="sxs-lookup"><span data-stu-id="b5b57-225">In the starter kit, sign in modules are prefilled with default text strings for the labels and descriptions.</span></span> <span data-ttu-id="b5b57-226">Voit mukauttaa nämä SDK:n merkkijonot päivittämällä sisäänkirjausmoduulin global.json-tiedoston arvot.</span><span class="sxs-lookup"><span data-stu-id="b5b57-226">You can customize these strings in the software development kit (SDK) by updating the values in the global.json file for the sign in module.</span></span>

<span data-ttu-id="b5b57-227">Esimerkiksi unohtuneen salasanan oletusteksti on **Unohtuiko salasana?**</span><span class="sxs-lookup"><span data-stu-id="b5b57-227">For example, the default text for the forgotten password link is **Forgotten password?**.</span></span> <span data-ttu-id="b5b57-228">Alla näkyy sisäänkirjaussivun oletusteksti.</span><span class="sxs-lookup"><span data-stu-id="b5b57-228">The following shows this default text on the sign-in page.</span></span>

![Sisäänkirjaussivun oletusteksti unohtunutta salasanaan varten](./media/B2C_SignUp_ModuleFace.png)

<span data-ttu-id="b5b57-230">Voit muokata moduulin aloituspakkauksen global.json-tiedostossa **Unohtuiko salasana?** -kohdan tekstiä seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="b5b57-230">However, in the global.json file for the starter kit sign in module, you can edit the text to **Forgot Password?**, as shown in the following illustration.</span></span>

![Sisäänkirjauksen päivitetty linkkiteksti moduulin global.json-tiedostossa](./media/B2C_CustomizingStringsForModule.png)

<span data-ttu-id="b5b57-232">Kun olet päivittänyt global.json-tiedoston ja julkaissut muutokset, uusi linkkiteksti näkyy sisäänkirjausmoduulissa sekä Commercessa että julkaistulla sisäänkirjaussivulla.</span><span class="sxs-lookup"><span data-stu-id="b5b57-232">After you update the global.json file and publish your changes, the new link text appears in the sign in module in both Commerce and on the live sign-in page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b5b57-233">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="b5b57-233">Additional resources</span></span>

[<span data-ttu-id="b5b57-234">Toimialueen nimen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="b5b57-234">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="b5b57-235">Uuden sähköisen kaupankäynnin sivuston käyttöönotto</span><span class="sxs-lookup"><span data-stu-id="b5b57-235">Deploy a new e-Commerce site</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="b5b57-236">Määritä verkkokauppakanava</span><span class="sxs-lookup"><span data-stu-id="b5b57-236">Set up an online store channel</span></span>](online-stores.md)

[<span data-ttu-id="b5b57-237">Sähköisen kaupankäynnin sivuston luominen</span><span class="sxs-lookup"><span data-stu-id="b5b57-237">Create an e-Commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="b5b57-238">Liitä verkkosivusto kanavaan</span><span class="sxs-lookup"><span data-stu-id="b5b57-238">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="b5b57-239">Robots.txt-tiedostojen hallinta</span><span class="sxs-lookup"><span data-stu-id="b5b57-239">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="b5b57-240">URL-osoitteen uudelleenohjausten lataaminen joukkona</span><span class="sxs-lookup"><span data-stu-id="b5b57-240">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="b5b57-241">B2C-vuokraajan määrittäminen Commercessa</span><span class="sxs-lookup"><span data-stu-id="b5b57-241">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="b5b57-242">Useiden B2C-vuokraajien määrittäminen Commerce-ympäristössä</span><span class="sxs-lookup"><span data-stu-id="b5b57-242">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="b5b57-243">Sisältöverkon (CDN) tuen lisääminen</span><span class="sxs-lookup"><span data-stu-id="b5b57-243">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="b5b57-244">Sijaintiin perustuvan myymälän tunnistuksen käyttöönotto</span><span class="sxs-lookup"><span data-stu-id="b5b57-244">Enable location-based store detection</span></span>](enable-store-detection.md)
