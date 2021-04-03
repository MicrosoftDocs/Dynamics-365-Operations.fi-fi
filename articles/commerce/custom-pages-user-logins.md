---
title: Mukautettujen sivujen määrittäminen käyttäjän sisäänkirjautumisia varten
description: Tässä ohjeaiheessa kerrotaan, miten Microsoft Dynamics 365 Commercessa luodaan mukautettuja sivuja, jotka käsittelevät Azure Active Directoryn (Azure AD) kuluttajakaupan (B2C) vuokraajien mukautettuja sisäänkirjauksia.
author: brianshook
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 3328fad5328ae1954a6749f9a5eebcb71c723698
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/19/2021
ms.locfileid: "5477945"
---
# <a name="set-up-custom-pages-for-user-sign-ins"></a><span data-ttu-id="a4b5d-103">Mukautettujen sivujen määrittäminen käyttäjän sisäänkirjautumisia varten</span><span class="sxs-lookup"><span data-stu-id="a4b5d-103">Set up custom pages for user sign-ins</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="a4b5d-104">Tässä ohjeaiheessa kerrotaan, miten Microsoft Dynamics 365 Commercessa luodaan mukautettuja sivuja, jotka käsittelevät Azure Active Directoryn (Azure AD) kuluttajakaupan (B2C) vuokraajien mukautettuja sisäänkirjauksia.</span><span class="sxs-lookup"><span data-stu-id="a4b5d-104">This topic describes how to build custom pages in Microsoft Dynamics 365 Commerce that handle customized sign-ins for users of Azure Active Directory (Azure AD) business-to-consumer (B2C) tenants.</span></span>

<span data-ttu-id="a4b5d-105">Jotta Dynamics 365 Commercessa tehdyt mukautetut sivut voivat käyttää käyttäjän sisäänkirjausten työnkulkuja, Commerce-ympäristössä viitattavat Azure AD -käytännöt on määritettävä.</span><span class="sxs-lookup"><span data-stu-id="a4b5d-105">To use custom pages that are authored in Dynamics 365 Commerce to handle user sign-in flows, you must set up the Azure AD policies that will be referenced in the Commerce environment.</span></span> <span data-ttu-id="a4b5d-106">Voit määrittää Azure AD:n kuluttajakaupan Rekisteröinti ja sisäänkirjaus-, Profiilin muokkaus- ja Sanasanan nollaus -käytännöt käyttämällä Azure AD:n kuluttajakaupan sovellusta.</span><span class="sxs-lookup"><span data-stu-id="a4b5d-106">You can configure the "Sign up and sign in," "Profile editing," and "Password reset" Azure AD B2C policies by using the Azure AD B2C application.</span></span> <span data-ttu-id="a4b5d-107">Azure AD:n kuluttajakaupan vuokraajan ja käytännön nimiin ei voi viitata valmisteluprosessin aikana, kun se tehdään Commerce-ympäristössä Microsoft Dynamics Lifecycle Services (LCS) -palvelun avulla.</span><span class="sxs-lookup"><span data-stu-id="a4b5d-107">The Azure AD B2C tenant and policy names can then be referenced during the provisioning process that is done for the Commerce environment by using Microsoft Dynamics Lifecycle Services (LCS).</span></span>

<span data-ttu-id="a4b5d-108">Mukautetut Commerce-sivut voidaan luoda käyttämällä sisäänkirjauksen, rekisteröinnin, tiliprofiilin muokkauksen tai salasanan nollauksen moduulia.</span><span class="sxs-lookup"><span data-stu-id="a4b5d-108">The custom Commerce pages can be built by using the sign in, sign up, account profile edit, or password reset module.</span></span> <span data-ttu-id="a4b5d-109">Näille mukautetuille sivuille julkaistaviin sivun URL-osoitteisiin on tämän jälkeen viitattava Azure AD:n kuluttajakaupan käytännön määrityksissä Azure-portaalissa.</span><span class="sxs-lookup"><span data-stu-id="a4b5d-109">The page URLs that are published for these custom pages should then be referenced in Azure AD B2C policy configurations in the Azure portal.</span></span>

## <a name="set-up-b2c-policies"></a><span data-ttu-id="a4b5d-110">Kuluttajakaupan käytäntöjen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="a4b5d-110">Set up B2C policies</span></span>

<span data-ttu-id="a4b5d-111">Kun olet määrittänyt Azure AD:n kuluttajakaupan vuokraajan ja liittänyt sen Commerce-ympäristöön, siirry **Azure AD:n kuluttajakauppa** -sivulla Azure-portaalissa ja valitse sitten **Käytännöt**-kohdassa **Käyttäjän työnkulut (käytännöt)**.</span><span class="sxs-lookup"><span data-stu-id="a4b5d-111">After you set up your Azure AD B2C tenant and associate it with your Commerce environment, go to the **Azure AD B2C** page in the Azure portal, and then, on the menu, under **Policies**, select **User flows (policies)**.</span></span>

![Käyttäjän työnkulut (käytännöt) -komento valikossa](./media/B2C_CustomPage_PoliciesMenu.png)

<span data-ttu-id="a4b5d-113">Nyt voit määrittää käyttäjän Rekisteröinti ja sisäänkirjaus-, Profiilin muokkaus ja Salasanan nollaus -työnkulut.</span><span class="sxs-lookup"><span data-stu-id="a4b5d-113">You can now configure the "Sign up and sign in," "Profile editing," and "Password reset" user sign-in flows.</span></span>

### <a name="configure-the-sign-up-and-sign-in-policy"></a><span data-ttu-id="a4b5d-114">Rekisteröinti ja sisäänkirjaus -käytännön määrittäminen</span><span class="sxs-lookup"><span data-stu-id="a4b5d-114">Configure the "Sign up and sign in" policy</span></span>

<span data-ttu-id="a4b5d-115">Voit määrittää Rekisteröinti ja sisäänkirjaus -käytännön seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="a4b5d-115">To configure the "Sign up and sign in" policy, follow these steps.</span></span>

1. <span data-ttu-id="a4b5d-116">Valitse **Uusi käyttäjän työnkulku** ja valitse sitten **Suositellut**-välilehdessä **Rekisteröinti ja sisäänkirjaus** -käytäntö.</span><span class="sxs-lookup"><span data-stu-id="a4b5d-116">Select **New user flow**, and then, on the **Recommended** tab, select the **Sign up and sign in** policy.</span></span>
1. <span data-ttu-id="a4b5d-117">Syötä käytännön nimi (esimerkiksi **B2C\_1\_SignInSignUp**).</span><span class="sxs-lookup"><span data-stu-id="a4b5d-117">Enter a name for the policy (for example, **B2C\_1\_SignInSignUp**).</span></span>
1. <span data-ttu-id="a4b5d-118">Valitse **Tunnistetietojen toimittajat** -osassa käytännön kanssa käytettävät tunnistetietojen toimittajat.</span><span class="sxs-lookup"><span data-stu-id="a4b5d-118">In the **Identity Providers** section, select the identity providers to use for the policy.</span></span> <span data-ttu-id="a4b5d-119">Vähintään **Sähköpostirekisteröityminen** on valittava.</span><span class="sxs-lookup"><span data-stu-id="a4b5d-119">At a minimum, **Email signup** must be selected.</span></span>
1. <span data-ttu-id="a4b5d-120">Valitse **Kerää määrite** -sarakkeessa **Sähköpostiosoite**-, **Etunimi**- ja **Sukunimi**-valintaruudut.</span><span class="sxs-lookup"><span data-stu-id="a4b5d-120">In the **Collect attribute** column, select the check boxes for **Email Address**, **Given Name**, and **Surname**.</span></span>
1. <span data-ttu-id="a4b5d-121">Valitse **Palauta vaatimus** -sarakkeessa **Sähköpostiosoitteet**-, **Etunimi**-, **Tunnistetietojen tarjoaja**-, **Sukunimi**- ja **Käyttäjän objektin tunnus** -valintaruudut.</span><span class="sxs-lookup"><span data-stu-id="a4b5d-121">In the **Return claim** column, select the check boxes for **Email Addresses**, **Given Name**, **Identity Provider**, **Surname**, and **User's Object ID**.</span></span>

    ![Valitut määritteet ja vaatimukset](./media/B2C_SignInSignUp_Attributes.png)

1. <span data-ttu-id="a4b5d-123">Valitse **OK**, kun haluat luoda käytännön.</span><span class="sxs-lookup"><span data-stu-id="a4b5d-123">Select **OK** to create the policy.</span></span>
1. <span data-ttu-id="a4b5d-124">Kaksoisnapsauta uuden käytännön nimeä ja valitse siirtymisruudussa **Ominaisuudet**.</span><span class="sxs-lookup"><span data-stu-id="a4b5d-124">Double-click the new policy name, and then, in the navigation pane, select **Properties**.</span></span>
1. <span data-ttu-id="a4b5d-125">Määritä **Ota JavaScriptia käyttävä sivun asettelu käyttöön (esikatselu)** -asetuksen arvoksi **Käytössä**.</span><span class="sxs-lookup"><span data-stu-id="a4b5d-125">Set the **Enable JavaScript enforcing page layout (preview)** option to **On**.</span></span>

    ![Uuden käytännön Ominaisuudet-sivu](./media/B2C_SignInSignUp_EnableJavascript.png)

> [!NOTE]
> <span data-ttu-id="a4b5d-127">Käytännön nimeen viitataan täysin Commerce-ympäristössä.</span><span class="sxs-lookup"><span data-stu-id="a4b5d-127">The policy name will be fully referenced in the Commerce environment.</span></span> <span data-ttu-id="a4b5d-128">(**B2C\_1\_**-etuliite sisällytetään viitteeseen.) Käytäntöjä ei voi nimetä uudelleen luomisen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="a4b5d-128">(The **B2C\_1\_** prefix will be included in the reference.) Policies can't be renamed after they are created.</span></span> <span data-ttu-id="a4b5d-129">Jos korvaat Commerce-ympäristön olemassa olevan käytännön, voit poistaa alkuperäisen käytännön ja luoda uuden käytännön, jolla on sama nimi.</span><span class="sxs-lookup"><span data-stu-id="a4b5d-129">If you're replacing an existing policy for your Commerce environment, you can delete the original policy and build a new policy that has the same name.</span></span> <span data-ttu-id="a4b5d-130">Vaihtoehtoisesti, jos ympäristö on jo valmisteltu, voit lähettää uuden käytännön nimen palvelupyynnön kautta.</span><span class="sxs-lookup"><span data-stu-id="a4b5d-130">Alternatively, if the environment has already been provisioned, you can submit the new policy name through a service request.</span></span>

<span data-ttu-id="a4b5d-131">Palaa tähän käytäntöön ja tee määritykset loppuun, kun mukautetut sivut on luotu.</span><span class="sxs-lookup"><span data-stu-id="a4b5d-131">You will return to this policy to finish the setup after you've built the custom pages.</span></span> <span data-ttu-id="a4b5d-132">Nyt voit sulkea käytännön ja palata **Käyttäjän työnkulut (käytännöt)** -sivulle Azure-portaalissa.</span><span class="sxs-lookup"><span data-stu-id="a4b5d-132">For now, close the policy to return to the **User flows (policies)** page in the Azure portal.</span></span>

### <a name="configure-the-profile-editing-policy"></a><span data-ttu-id="a4b5d-133">Profiilin muokkaus -käytännön määrittäminen</span><span class="sxs-lookup"><span data-stu-id="a4b5d-133">Configure the "Profile editing" policy</span></span>

<span data-ttu-id="a4b5d-134">Voit määrittää Profiilin muokkaus -käytännön seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="a4b5d-134">To configure the "Profile editing" policy, follow these steps.</span></span>

1. <span data-ttu-id="a4b5d-135">Valitse **Uusi käyttäjän työnkulku** ja valitse sitten **Suositellut**-välilehdessä **Profiilin muokkaus** -käytäntö.</span><span class="sxs-lookup"><span data-stu-id="a4b5d-135">Select **New user flow**, and then, on the **Recommended** tab, select the **Profile editing** policy.</span></span>
1. <span data-ttu-id="a4b5d-136">Syötä käytännön nimi (esimerkiksi **B2C\_1\_EditProfile**).</span><span class="sxs-lookup"><span data-stu-id="a4b5d-136">Enter a name for the policy (for example, **B2C\_1\_EditProfile**).</span></span>
1. <span data-ttu-id="a4b5d-137">Valitse **Tunnistetietojen toimittajat** -osassa käytännön kanssa käytettävät tunnistetietojen toimittajat.</span><span class="sxs-lookup"><span data-stu-id="a4b5d-137">In the **Identity Providers** section, select the identity providers to use for the policy.</span></span> <span data-ttu-id="a4b5d-138">Vähintään **Paikallisen tilin sisäänkirjaus** on valittava.</span><span class="sxs-lookup"><span data-stu-id="a4b5d-138">At a minimum, **Local Account SignIn** must be selected.</span></span>
1. <span data-ttu-id="a4b5d-139">Valitse **Kerää määrite** -sarakkeessa **Sähköpostiosoitteet**- ja **Sukunimi**-valintaruudut.</span><span class="sxs-lookup"><span data-stu-id="a4b5d-139">In the **Collect attribute** column, select the check boxes for **Email Addresses** and **Surname**.</span></span>
1. <span data-ttu-id="a4b5d-140">Valitse **Palauta vaatimus** -sarakkeessa **Sähköpostiosoitteet**-, **Etunimi**-, **Tunnistetietojen tarjoaja**-, **Sukunimi**- ja **Käyttäjän objektin tunnus** -valintaruudut.</span><span class="sxs-lookup"><span data-stu-id="a4b5d-140">In the **Return claim** column, select the check boxes for **Email Addresses**, **Given Name**, **Identity Provider**, **Surname**, and **User's Object ID**.</span></span>
1. <span data-ttu-id="a4b5d-141">Valitse **OK**, kun haluat luoda käytännön.</span><span class="sxs-lookup"><span data-stu-id="a4b5d-141">Select **OK** to create the policy.</span></span>
1. <span data-ttu-id="a4b5d-142">Kaksoisnapsauta uuden käytännön nimeä ja valitse siirtymisruudussa **Ominaisuudet**.</span><span class="sxs-lookup"><span data-stu-id="a4b5d-142">Double-click the new policy name, and then, in the navigation pane, select **Properties**.</span></span>
1. <span data-ttu-id="a4b5d-143">Määritä **Ota JavaScriptia käyttävä sivun asettelu käyttöön (esikatselu)** -asetuksen arvoksi **Käytössä**.</span><span class="sxs-lookup"><span data-stu-id="a4b5d-143">Set the **Enable JavaScript enforcing page layout (preview)** option to **On**.</span></span>

<span data-ttu-id="a4b5d-144">Palaa tähän käytäntöön ja tee määritykset loppuun, kun mukautetut sivut on luotu.</span><span class="sxs-lookup"><span data-stu-id="a4b5d-144">You will return to this policy to finish the setup after you've built the custom pages.</span></span> <span data-ttu-id="a4b5d-145">Nyt voit sulkea käytännön ja palata **Käyttäjän työnkulut (käytännöt)** -sivulle Azure-portaalissa.</span><span class="sxs-lookup"><span data-stu-id="a4b5d-145">For now, close the policy to return to the **User flows (policies)** page in the Azure portal.</span></span>

### <a name="configure-the-password-reset-policy"></a><span data-ttu-id="a4b5d-146">Salasanan nollaus -käytännön määrittäminen</span><span class="sxs-lookup"><span data-stu-id="a4b5d-146">Configure the "Password reset" policy</span></span>

<span data-ttu-id="a4b5d-147">Voit määrittää Salasanan nollaus -käytännön seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="a4b5d-147">To configure the "Password reset" policy, follow these steps.</span></span>

1. <span data-ttu-id="a4b5d-148">Valitse **Uusi käyttäjän työnkulku** ja valitse sitten **Esikatselu**-välilehdessä **Salasanan nollaus versio 1.1** -käytäntö.</span><span class="sxs-lookup"><span data-stu-id="a4b5d-148">Select **New user flow**, and then, on the **Preview** tab, select the **Password reset v1.1** policy.</span></span>

    ![Salasanan nollaus versio 1.1 -käytäntö valittuna Esikatselu-välilehdessä](./media/B2C_ForgetPassword_Menu.png)

1. <span data-ttu-id="a4b5d-150">Syötä käytännön nimi (esimerkiksi **B2C\_1\_ForgetPassword**).</span><span class="sxs-lookup"><span data-stu-id="a4b5d-150">Enter a name for the policy (for example, **B2C\_1\_ForgetPassword**).</span></span>
1. <span data-ttu-id="a4b5d-151">Valitse **Tunnistetietojen tarjoajat** -osassa **Nollaa salasana sähköpostiosoitteen avulla**.</span><span class="sxs-lookup"><span data-stu-id="a4b5d-151">In the **Identity Providers** section, select **Reset password using email address**.</span></span>
1. <span data-ttu-id="a4b5d-152">Valitse **Palauta vaatimus** -sarakkeessa **Sähköpostiosoitteet**-, **Etunimi**, **Sukunimi**- ja **Käyttäjän objektin tunnus** valintaruudut.</span><span class="sxs-lookup"><span data-stu-id="a4b5d-152">In the **Return claim** column, select the check boxes for **Email Addresses**, **Given Name**, **Surname**, and **User's Object ID**.</span></span>

    ![Valitut vaatimukset](./media/B2C_ForgetPassword_Attributes.png)

1. <span data-ttu-id="a4b5d-154">Valitse **OK**, kun haluat luoda käytännön.</span><span class="sxs-lookup"><span data-stu-id="a4b5d-154">Select **OK** to create the policy.</span></span>
1. <span data-ttu-id="a4b5d-155">Kaksoisnapsauta uuden käytännön nimeä ja valitse siirtymisruudussa **Ominaisuudet**.</span><span class="sxs-lookup"><span data-stu-id="a4b5d-155">Double-click the new policy name, and then, in the navigation pane, select **Properties**.</span></span>
1. <span data-ttu-id="a4b5d-156">Määritä **Ota JavaScriptia käyttävä sivun asettelu käyttöön (esikatselu)** -asetuksen arvoksi **Käytössä**.</span><span class="sxs-lookup"><span data-stu-id="a4b5d-156">Set the **Enable JavaScript enforcing page layout (preview)** option to **On**.</span></span>

<span data-ttu-id="a4b5d-157">Palaa tähän käytäntöön ja tee määritykset loppuun, kun mukautetut sivut on luotu.</span><span class="sxs-lookup"><span data-stu-id="a4b5d-157">You will return to this policy to finish the setup after you've built the custom pages.</span></span> <span data-ttu-id="a4b5d-158">Nyt voit sulkea käytännön ja palata **Käyttäjän työnkulut (käytännöt)** -sivulle Azure-portaalissa.</span><span class="sxs-lookup"><span data-stu-id="a4b5d-158">For now, close the policy to return to the **User flows (policies)** page in the Azure portal.</span></span>

## <a name="build-the-custom-pages"></a><span data-ttu-id="a4b5d-159">Mukautettujen sivujen luominen</span><span class="sxs-lookup"><span data-stu-id="a4b5d-159">Build the custom pages</span></span>

<span data-ttu-id="a4b5d-160">Voit luoda mukautettuja sivuja käyttäjän sisäänkirjausten käsittelemistä varten seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="a4b5d-160">To build the custom pages to handle user sign-ins, follow these steps.</span></span>

1. <span data-ttu-id="a4b5d-161">Siirry Commerce-muokkaustyökalut-kohdassa sivustoon.</span><span class="sxs-lookup"><span data-stu-id="a4b5d-161">In the Commerce authoring tools, go to your site.</span></span>
1. <span data-ttu-id="a4b5d-162">Muodosta seuraavat viisi mallia ja sivua:</span><span class="sxs-lookup"><span data-stu-id="a4b5d-162">Build the following five templates and five pages:</span></span>

    - <span data-ttu-id="a4b5d-163">**Sisäänkirjaus**-malli ja -sivu, jotka käyttävät sisäänkirjauksen moduulia.</span><span class="sxs-lookup"><span data-stu-id="a4b5d-163">A **Sign In** template and page that use the sign in module.</span></span>
    - <span data-ttu-id="a4b5d-164">**Rekisteröinti**-malli ja -sivu, jotka käyttävät rekisteröinnin moduulia.</span><span class="sxs-lookup"><span data-stu-id="a4b5d-164">A **Sign Up** template and page that use the sign up module.</span></span>
    - <span data-ttu-id="a4b5d-165">**Salasanan nollaus** -malli ja -sivu, jotka käyttävät salasanan nollauksen moduulia.</span><span class="sxs-lookup"><span data-stu-id="a4b5d-165">A **Password Reset** template and page that use the password reset module.</span></span>
    - <span data-ttu-id="a4b5d-166">**Salasanan nollauksen vahvistus** -malli ja -sivu, jotka käyttävät salasanan nollauksen vahvistuksen moduulia.</span><span class="sxs-lookup"><span data-stu-id="a4b5d-166">A **Password Reset verification** template and page that use the password reset verification module.</span></span>
    - <span data-ttu-id="a4b5d-167">**Profiilin muokkaus** -malli ja -sivu, jotka käyttävät tiliprofiilin muokkauksen moduulia</span><span class="sxs-lookup"><span data-stu-id="a4b5d-167">A **Profile Edit** template and page that use the account profile edit module</span></span>

<span data-ttu-id="a4b5d-168">Kun luot sivuja, noudata seuraavia ohjeita:</span><span class="sxs-lookup"><span data-stu-id="a4b5d-168">When you build the pages, follow these guidelines:</span></span>

- <span data-ttu-id="a4b5d-169">Käytä kunkin sivun tai moduulin kohdalla asettelua ja tyyliä, joka sopii parhaiten liiketoiminnan vaatimuksiin.</span><span class="sxs-lookup"><span data-stu-id="a4b5d-169">For each page or module, use the layout and style that best suit your business requirements.</span></span>
- <span data-ttu-id="a4b5d-170">Julkaise kaikki sivut ja URL-osoitteet, joita on käytettävä Azure AD:n kuluttajakaupan määrityksessä.</span><span class="sxs-lookup"><span data-stu-id="a4b5d-170">Publish all pages and URLs that must be used in the Azure AD B2C setup.</span></span>
- <span data-ttu-id="a4b5d-171">Kun sivut ja URL-osoitteet on julkaistu, kerää Azure AD:n kuluttajakaupan käytännön määrityksessä käytettävät URL-osoitteet.</span><span class="sxs-lookup"><span data-stu-id="a4b5d-171">After the pages and URLs are published, collect the URLs that must be used for the Azure AD B2C policy configurations.</span></span> <span data-ttu-id="a4b5d-172">Jälkiliite **?preloadscripts=true** lisätään jokaiseen URL-osoitteeseen käytön yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="a4b5d-172">A **?preloadscripts=true** suffix will be added to every URL when it's used.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a4b5d-173">Älä käytä universaaleja ylä- ja alatunnisteita, joissa on suhteellisia linkkejä.</span><span class="sxs-lookup"><span data-stu-id="a4b5d-173">Don't reuse universal headers and footers that have relative links.</span></span> <span data-ttu-id="a4b5d-174">Koska Azure AD:n kuluttajakaupan toimialue isännöi näitä sivuja käytön yhteydessä, kaikissa linkeissä tulisi käyttää vain absoluuttisia URL-osoitteita.</span><span class="sxs-lookup"><span data-stu-id="a4b5d-174">Because these pages will be hosted in the Azure AD B2C domain when they are used, only absolute URLs should be used for all links.</span></span>

## <a name="configure-azure-ad-b2c-policies-with-custom-page-information"></a><span data-ttu-id="a4b5d-175">Azure AD:n kuluttajakaupan käytäntöjen ja mukautetun sivun tietojen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="a4b5d-175">Configure Azure AD B2C policies with custom page information</span></span> 

<span data-ttu-id="a4b5d-176">Palaa Azure-portaalissa **Azure AD:n kuluttajakauppa** -sivulla ja valitse **Käytännöt**-kohdassa valikosta **Käyttäjän työnkulut (käytännöt)**.</span><span class="sxs-lookup"><span data-stu-id="a4b5d-176">In the Azure portal, return to the **Azure AD B2C** page, and then, on the menu, under **Policies**, select **User flows (policies)**.</span></span>

### <a name="update-the-sign-up-and-sign-in-policy-with-custom-page-information"></a><span data-ttu-id="a4b5d-177">Rekisteröidy ja kirjaudu -käytännön päivittäminen mukautetun sivun tiedoilla</span><span class="sxs-lookup"><span data-stu-id="a4b5d-177">Update the "Sign up and sign in" policy with custom page information</span></span>

<span data-ttu-id="a4b5d-178">Voit päivittää Rekisteröinti ja sisäänkirjaus -käytännön mukautetun sivun tiedoilla seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="a4b5d-178">To update the "Sign up and sign in" policy with custom page information, follow these steps.</span></span>

1. <span data-ttu-id="a4b5d-179">Valitse aiemmin määritetyn **Rekisteröinti ja sisäänkirjaus** -käytännön siirtymisruudussa **Sivun asettelut**.</span><span class="sxs-lookup"><span data-stu-id="a4b5d-179">In the **Sign in and sign up** policy that you configured earlier, in the navigation pane, select **Page layouts**.</span></span>
1. <span data-ttu-id="a4b5d-180">Valitse **Yhtenäinen rekisteröinti tai sisäänkirjaus -sivu** -asettelu</span><span class="sxs-lookup"><span data-stu-id="a4b5d-180">Select the **Unified sign up or sign in page** layout.</span></span>
1. <span data-ttu-id="a4b5d-181">Määritä **Käytä mukautettua sivun sisältöä** -asetukseksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="a4b5d-181">Set the **Use custom page content** option to **Yes**.</span></span>
1. <span data-ttu-id="a4b5d-182">Syötä **Mukautetun sivun URI** -kenttään sisäänkirjauksen täydellinen URL-osoite.</span><span class="sxs-lookup"><span data-stu-id="a4b5d-182">In the **Custom page URI** field, enter the full sign-in URL.</span></span> <span data-ttu-id="a4b5d-183">Sisällytä jälkiliite **?preloadscripts=true**.</span><span class="sxs-lookup"><span data-stu-id="a4b5d-183">Include the **?preloadscripts=true** suffix.</span></span> <span data-ttu-id="a4b5d-184">Syötä arvoksi esimerkiksi ``www.<my domain>.com/sign-in?preloadscripts=true``.</span><span class="sxs-lookup"><span data-stu-id="a4b5d-184">For example, enter ``www.<my domain>.com/sign-in?preloadscripts=true``.</span></span>
1. <span data-ttu-id="a4b5d-185">Valitse **Sivun asettelun versio (esikatselu)** -kentässä **1.2.0**.</span><span class="sxs-lookup"><span data-stu-id="a4b5d-185">In the **Page Layout Version (Preview)** field, select **1.2.0**.</span></span>
1. <span data-ttu-id="a4b5d-186">Valitse **Paikallisen tilin rekisteröinti -sivu** -asettelu.</span><span class="sxs-lookup"><span data-stu-id="a4b5d-186">Select the **Local account sign up page** layout.</span></span>
1. <span data-ttu-id="a4b5d-187">Määritä **Käytä mukautettua sivun sisältöä** -asetukseksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="a4b5d-187">Set the **Use custom page content** option to **Yes**.</span></span>
1. <span data-ttu-id="a4b5d-188">Syötä **Mukautetun sivun URI** -kenttään rekisteröitymisen täydellinen URL-osoite.</span><span class="sxs-lookup"><span data-stu-id="a4b5d-188">In the **Custom page URI** field, enter the full sign-up URL.</span></span> <span data-ttu-id="a4b5d-189">Sisällytä jälkiliite **?preloadscripts=true**.</span><span class="sxs-lookup"><span data-stu-id="a4b5d-189">Include the **?preloadscripts=true** suffix.</span></span> <span data-ttu-id="a4b5d-190">Syötä arvoksi esimerkiksi ``www.<my domain>.com/sign-up?preloadscripts=true``.</span><span class="sxs-lookup"><span data-stu-id="a4b5d-190">For example, enter ``www.<my domain>.com/sign-up?preloadscripts=true``.</span></span>
1. <span data-ttu-id="a4b5d-191">Valitse **Sivun asettelun versio (esikatselu)** -kentässä **1.2.0**.</span><span class="sxs-lookup"><span data-stu-id="a4b5d-191">In the **Page Layout Version (Preview)** field, select **1.2.0**.</span></span>
1. <span data-ttu-id="a4b5d-192">Tee seuraavat toiminnot **Käyttäjän määritteet** -osassa:</span><span class="sxs-lookup"><span data-stu-id="a4b5d-192">In the **User attributes** section, follow these steps:</span></span>

    1. <span data-ttu-id="a4b5d-193">Valitse **Sähköpostiosoite**-, **Etunimi**- ja **Sukunimi**-määritteille **Ei**-arvo **Vaatii tarkistuksen** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="a4b5d-193">For the **Email Address**, **Given Name**, and **Surname** attributes, select **No** in the **Requires Verification** field.</span></span>
    1. <span data-ttu-id="a4b5d-194">Valitse **Etunimi**- ja **Sukunimi**-määritteille **Ei**-arvo **Valinnainen**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="a4b5d-194">For the **Given Name** and **Surname** attributes, select **No** in the **Optional** field.</span></span>

    ![Paikallisen tilin rekisteröinti -sivun käytännön määrittäminen](./media/B2C_SignUp_PageURLConfig.png)

### <a name="update-the-profile-editing-policy-with-custom-page-information"></a><span data-ttu-id="a4b5d-196">Profiilin muokkaus -käytännön päivittäminen mukautetun sivun tiedoilla</span><span class="sxs-lookup"><span data-stu-id="a4b5d-196">Update the "Profile editing" policy with custom page information</span></span>

<span data-ttu-id="a4b5d-197">Voit päivittää Profiilin muokkaus -käytännön mukautetun sivun tiedoilla seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="a4b5d-197">To update the "Profile editing" policy with custom page information, follow these steps.</span></span>

1. <span data-ttu-id="a4b5d-198">Valitse aiemmin määritetyn **Profiilin muokkaus** -käytännön siirtymisruudussa **Sivun asettelut**.</span><span class="sxs-lookup"><span data-stu-id="a4b5d-198">In the **Profile Editing** policy that you configured earlier, in the navigation pane, select **Page layouts**.</span></span>
1. <span data-ttu-id="a4b5d-199">Valitse **Profiilin muokkaus -sivu** -asettelu.</span><span class="sxs-lookup"><span data-stu-id="a4b5d-199">Select the **Profile edit page** layout.</span></span>
1. <span data-ttu-id="a4b5d-200">Määritä **Käytä mukautettua sivun sisältöä** -asetukseksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="a4b5d-200">Set the **Use custom page content** option to **Yes**.</span></span>
1. <span data-ttu-id="a4b5d-201">Syötä **Mukautetun sivun URI** -kenttään profiilin muokkaussivun täydellinen URL-osoite.</span><span class="sxs-lookup"><span data-stu-id="a4b5d-201">In the **Custom page URI** field, enter the full profile edit URL.</span></span> <span data-ttu-id="a4b5d-202">Sisällytä jälkiliite **?preloadscripts=true**.</span><span class="sxs-lookup"><span data-stu-id="a4b5d-202">Include the **?preloadscripts=true** suffix.</span></span> <span data-ttu-id="a4b5d-203">Syötä arvoksi esimerkiksi ``www.<my domain>.com/profile-edit?preloadscripts=true``.</span><span class="sxs-lookup"><span data-stu-id="a4b5d-203">For example, enter ``www.<my domain>.com/profile-edit?preloadscripts=true``.</span></span>
1. <span data-ttu-id="a4b5d-204">Valitse **Sivun asettelun versio (esikatselu)** -kentässä **1.2.0**.</span><span class="sxs-lookup"><span data-stu-id="a4b5d-204">In the **Page Layout Version (Preview)** field, select **1.2.0**.</span></span>
1. <span data-ttu-id="a4b5d-205">Tee seuraavat toiminnot **Käyttäjän määritteet** -osassa:</span><span class="sxs-lookup"><span data-stu-id="a4b5d-205">In the **User attributes** section, follow these steps:</span></span>

    1. <span data-ttu-id="a4b5d-206">Valitse **Sähköpostiosoite**- ja **Etunimi**-määritteille **Ei**-arvo **Vaatii tarkistuksen** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="a4b5d-206">For the **Email Address**, **Given Name** attributes, select **No** in the **Requires Verification** field.</span></span>
    1. <span data-ttu-id="a4b5d-207">Valitse **Etunimi**- ja **Sukunimi**-määritteille **Ei**-arvo **Valinnainen**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="a4b5d-207">For the **Given Name** and **Surname** attributes, select **No** in the **Optional** field.</span></span>

### <a name="update-the-password-reset-policy-with-custom-page-information"></a><span data-ttu-id="a4b5d-208">Salasanan nollaus -käytännön päivittäminen mukautetun sivun tiedoilla</span><span class="sxs-lookup"><span data-stu-id="a4b5d-208">Update the "Password reset" policy with custom page information</span></span>

<span data-ttu-id="a4b5d-209">Voit päivittää Salasanan nollaus -käytännön mukautetun sivun tiedoilla seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="a4b5d-209">To update the "Password reset" policy with custom page information, follow these steps.</span></span>

1. <span data-ttu-id="a4b5d-210">Valitse aiemmin määritetyn **Salasanan nollaus** -käytännön siirtymisruudussa **Sivun asettelut**.</span><span class="sxs-lookup"><span data-stu-id="a4b5d-210">In the **Password Reset** policy that you configured earlier, in the navigation pane, select **Page layouts**.</span></span>
1. <span data-ttu-id="a4b5d-211">Valitse **Uusi salasana -sivu** -asettelu.</span><span class="sxs-lookup"><span data-stu-id="a4b5d-211">Select the **New password page** layout.</span></span>
1. <span data-ttu-id="a4b5d-212">Määritä **Käytä mukautettua sivun sisältöä** -asetukseksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="a4b5d-212">Set the **Use custom page content** option to **Yes**.</span></span>
1. <span data-ttu-id="a4b5d-213">Syötä **Mukautetun sivun URI** -kenttään salasanan palauttamisen täydellinen URL-osoite.</span><span class="sxs-lookup"><span data-stu-id="a4b5d-213">In the **Custom page URI** field, enter the full password reset URL.</span></span> <span data-ttu-id="a4b5d-214">Sisällytä jälkiliite **?preloadscripts=true**.</span><span class="sxs-lookup"><span data-stu-id="a4b5d-214">Include the **?preloadscripts=true** suffix.</span></span> <span data-ttu-id="a4b5d-215">Syötä arvoksi esimerkiksi ``www.<my domain>.com/passwordreset?preloadscripts=true``.</span><span class="sxs-lookup"><span data-stu-id="a4b5d-215">For example, enter ``www.<my domain>.com/passwordreset?preloadscripts=true``.</span></span>
1. <span data-ttu-id="a4b5d-216">Valitse **Sivun asettelun versio (esikatselu)** -kentässä **1.2.0**.</span><span class="sxs-lookup"><span data-stu-id="a4b5d-216">In the **Page Layout Version (Preview)** field, select **1.2.0**.</span></span>
1. <span data-ttu-id="a4b5d-217">Valitse **Tilin tarkistus -sivu** -asettelu.</span><span class="sxs-lookup"><span data-stu-id="a4b5d-217">Select the **Account verification page** layout.</span></span>
1. <span data-ttu-id="a4b5d-218">Määritä **Käytä mukautettua sivun sisältöä** -asetukseksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="a4b5d-218">Set the **Use custom page content** option to **Yes**.</span></span>
1. <span data-ttu-id="a4b5d-219">Syötä **Mukautetun sivun URI** -kenttään salasanan palauttamisen todentamisen URL-osoite.</span><span class="sxs-lookup"><span data-stu-id="a4b5d-219">In the **Custom page URI** field, enter the full password reset verification URL.</span></span> <span data-ttu-id="a4b5d-220">Sisällytä jälkiliite **?preloadscripts=true**.</span><span class="sxs-lookup"><span data-stu-id="a4b5d-220">Include the **?preloadscripts=true** suffix.</span></span> <span data-ttu-id="a4b5d-221">Syötä arvoksi esimerkiksi ``www.<my domain>.com/passwordreset-verification?preloadscripts=true``.</span><span class="sxs-lookup"><span data-stu-id="a4b5d-221">For example, enter ``www.<my domain>.com/passwordreset-verification?preloadscripts=true``.</span></span>
1. <span data-ttu-id="a4b5d-222">Valitse **Sivun asettelun versio (esikatselu)** -kentässä **1.2.0**.</span><span class="sxs-lookup"><span data-stu-id="a4b5d-222">In the **Page Layout Version (Preview)** field, select **1.2.0**.</span></span>



## <a name="customize-default-text-strings-for-labels-and-descriptions"></a><span data-ttu-id="a4b5d-223">Otsikoiden ja kuvausten oletustekstimerkkijonojen mukauttaminen</span><span class="sxs-lookup"><span data-stu-id="a4b5d-223">Customize default text strings for labels and descriptions</span></span>

<span data-ttu-id="a4b5d-224">Moduulikirjastossa sisäänkirjausmoduulit täytetään etukäteen otsikoiden ja kuvausten oletustekstimerkkijonoilla.</span><span class="sxs-lookup"><span data-stu-id="a4b5d-224">In the module library, sign-in modules are prefilled with default text strings for the labels and descriptions.</span></span> <span data-ttu-id="a4b5d-225">Voit mukauttaa nämä SDK:n merkkijonot päivittämällä sisäänkirjausmoduulin global.json-tiedoston arvot.</span><span class="sxs-lookup"><span data-stu-id="a4b5d-225">You can customize these strings in the software development kit (SDK) by updating the values in the global.json file for the sign in module.</span></span>

<span data-ttu-id="a4b5d-226">Esimerkiksi unohtuneen salasanan oletusteksti on **Unohtuiko salasana?**</span><span class="sxs-lookup"><span data-stu-id="a4b5d-226">For example, the default text for the forgotten password link is **Forgotten password?**.</span></span> <span data-ttu-id="a4b5d-227">Alla näkyy sisäänkirjaussivun oletusteksti.</span><span class="sxs-lookup"><span data-stu-id="a4b5d-227">The following shows this default text on the sign-in page.</span></span>

![Sisäänkirjaussivun oletusteksti unohtunutta salasanaan varten](./media/B2C_SignUp_ModuleFace.png)

<span data-ttu-id="a4b5d-229">Voit kuitenkin muokata moduulikirjaston kirjautumismoduulin global.json-tiedoston tekstin muotoon **Unohtuiko salasanasi?**, kuten seuraavassa kuvassa näkyy.</span><span class="sxs-lookup"><span data-stu-id="a4b5d-229">However, in the global.json file for the module library sign-in module, you can edit the text to **Forgot Password?**, as shown in the following illustration.</span></span>

![Sisäänkirjauksen päivitetty linkkiteksti moduulin global.json-tiedostossa](./media/B2C_CustomizingStringsForModule.png)

<span data-ttu-id="a4b5d-231">Kun olet päivittänyt global.json-tiedoston ja julkaissut muutokset, uusi linkkiteksti näkyy sisäänkirjausmoduulissa sekä Commercessa että julkaistulla sisäänkirjaussivulla.</span><span class="sxs-lookup"><span data-stu-id="a4b5d-231">After you update the global.json file and publish your changes, the new link text appears in the sign-in module in both Commerce and on the live sign-in page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a4b5d-232">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="a4b5d-232">Additional resources</span></span>

[<span data-ttu-id="a4b5d-233">Toimialueen nimen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="a4b5d-233">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="a4b5d-234">Uuden sähköisen kaupankäynnin vuokraajan käyttöönotto</span><span class="sxs-lookup"><span data-stu-id="a4b5d-234">Deploy a new e-commerce tenant</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="a4b5d-235">Sähköisen kaupankäynnin sivuston luominen</span><span class="sxs-lookup"><span data-stu-id="a4b5d-235">Create an e-commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="a4b5d-236">Dynamics 365 Commerce -sivuston liittäminen online-kanavaan</span><span class="sxs-lookup"><span data-stu-id="a4b5d-236">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="a4b5d-237">Robots.txt-tiedostojen hallinta</span><span class="sxs-lookup"><span data-stu-id="a4b5d-237">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="a4b5d-238">URL-uudelleenohjausten joukkolataus palveluun</span><span class="sxs-lookup"><span data-stu-id="a4b5d-238">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="a4b5d-239">B2C-vuokraajan määrittäminen Commercessa</span><span class="sxs-lookup"><span data-stu-id="a4b5d-239">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="a4b5d-240">Useiden B2C-vuokraajien määrittäminen Commerce-ympäristössä</span><span class="sxs-lookup"><span data-stu-id="a4b5d-240">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="a4b5d-241">Sisältöverkon (CDN) tuen lisääminen</span><span class="sxs-lookup"><span data-stu-id="a4b5d-241">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="a4b5d-242">Sijaintiin perustuvan myymälän tunnistuksen käyttöönotto</span><span class="sxs-lookup"><span data-stu-id="a4b5d-242">Enable location-based store detection</span></span>](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
