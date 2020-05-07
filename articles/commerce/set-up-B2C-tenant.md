---
title: B2C-vuokraajan määrittäminen Commercessa
description: Tässä ohjeaiheessa kerrotaan, miten Azure Active Directoryn (Azure AD) kuluttajakaupan (B2C) vuokraajat määritetään Dynamics 365 Commercen käyttäjän sivuston todennusta varten.
author: BrianShook
manager: annbe
ms.date: 04/17 /2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: ''
ms.search.region: Global
ms.search.industry: retail
ms.author: BriShoo
ms.search.validFrom: 2020-02-13
ms.dyn365.ops.version: ''
ms.openlocfilehash: f4768eede43003aac892b861b4a86ababe98a189
ms.sourcegitcommit: 063c4d7155be6c2cadcafa1630d16ee235285479
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/17/2020
ms.locfileid: "3270207"
---
# <a name="set-up-a-b2c-tenant-in-commerce"></a><span data-ttu-id="f74ed-103">B2C-vuokraajan määrittäminen Commercessa</span><span class="sxs-lookup"><span data-stu-id="f74ed-103">Set up a B2C tenant in Commerce</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="f74ed-104">Tässä ohjeaiheessa kerrotaan, miten Azure Active Directoryn (Azure AD) kuluttajakaupan (B2C) vuokraajat määritetään Dynamics 365 Commercen käyttäjän sivuston todennusta varten.</span><span class="sxs-lookup"><span data-stu-id="f74ed-104">This topic describes how to set up your Azure Active Directory (Azure AD) business-to-consumer (B2C) tenants for user site authentication in Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="f74ed-105">Yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="f74ed-105">Overview</span></span>

<span data-ttu-id="f74ed-106">Dynamics 365 Commerce käyttää Azure AD B2C -ratkaisua käyttäjän tunnistetietojen ja todennuksen työnkulkujen tukemisessa.</span><span class="sxs-lookup"><span data-stu-id="f74ed-106">Dynamics 365 Commerce uses Azure AD B2C to support user credential and authentication flows.</span></span> <span data-ttu-id="f74ed-107">Käyttäjä voi rekisteröityä, kirjautua sisään ja nollata salasanan näiden työnkulkujen avulla.</span><span class="sxs-lookup"><span data-stu-id="f74ed-107">A user can sign up, sign in, and reset their password through these flows.</span></span> <span data-ttu-id="f74ed-108">Azure AD B2C tallentaa luottamukselliset käyttäjän todennustiedot, kuten käyttäjätunnuksen ja salasanan.</span><span class="sxs-lookup"><span data-stu-id="f74ed-108">Azure AD B2C stores sensitive user authentication information, such as username and password.</span></span> <span data-ttu-id="f74ed-109">B2C-vuokraajan käyttäjätietueeseen tallennetaan B2C:n paikallisen tilin tietue tai B2C:n yhteisöpalvelun tunnuksen tarjoajan tietue.</span><span class="sxs-lookup"><span data-stu-id="f74ed-109">The user record in the B2C tenant will store either a B2C local account record or a B2C social identity provider record.</span></span> <span data-ttu-id="f74ed-110">Nämä B2C-tietueet linkitetään takaisin asiakastietueeseen Commerce-ympäristössä.</span><span class="sxs-lookup"><span data-stu-id="f74ed-110">These B2C records will link back to the customer record in the Commerce environment.</span></span>

## <a name="create-or-link-to-an-existing-aad-b2c-tenant-in-the-azure-portal"></a><span data-ttu-id="f74ed-111">Olemassa olevan AAD B2C -vuokraajan luominen tai linkittäminen Azure-portaalissa</span><span class="sxs-lookup"><span data-stu-id="f74ed-111">Create or link to an existing AAD B2C tenant in the Azure portal</span></span>

1. <span data-ttu-id="f74ed-112">Kirjaudu [Azure-portaalin osoitteessa](https://portal.azure.com/).</span><span class="sxs-lookup"><span data-stu-id="f74ed-112">Sign in to the [Azure portal](https://portal.azure.com/).</span></span>
1. <span data-ttu-id="f74ed-113">Valitse Azure-portaalin valikossa **Luo resurssi**.</span><span class="sxs-lookup"><span data-stu-id="f74ed-113">From the Azure portal menu, select **Create a resource**.</span></span> <span data-ttu-id="f74ed-114">Varmista,. että käytät tilausta ja hakemistoa, joka yhdistetään Commerce-ympäristöön.</span><span class="sxs-lookup"><span data-stu-id="f74ed-114">Be sure to use the subscription and directory that will be connected with your Commerce environment.</span></span>

    ![Resurssin luominen Azure-portaaliin](./media/B2CImage_1.png)

1. <span data-ttu-id="f74ed-116">Siirry kohtaan **Tunnistetiedot \> Azure Active Directory B2C**.</span><span class="sxs-lookup"><span data-stu-id="f74ed-116">Go to **Identity \> Azure Active Directory B2C**.</span></span>
1. <span data-ttu-id="f74ed-117">Käytä **Uuden B2C-vuokraajan luominen tai linkittäminen olemassa olevaan vuokraajaan** -sivulla seuraavista vaihtoehdoista sitä, joka sopii yrityksen tarpeisiin parhaiten:</span><span class="sxs-lookup"><span data-stu-id="f74ed-117">Once on the **Create New B2C Tenant or Link to existing Tenant** page, use one of the options below that best suits your company's needs:</span></span>

    - <span data-ttu-id="f74ed-118">**Luo uusi Azure AD B2C -vuokraaja**: Käytä tätä vaihtoehtoa, jos haluat luoda uuden AAD B2C -vuokraajan.</span><span class="sxs-lookup"><span data-stu-id="f74ed-118">**Create a new Azure AD B2C Tenant**: Use this option to create a new AAD B2C tenant.</span></span>
        1. <span data-ttu-id="f74ed-119">Valitse **Luo uusi Azure AD B2C -vuokraaja**.</span><span class="sxs-lookup"><span data-stu-id="f74ed-119">Select **Create a new Azure AD B2C Tenant**.</span></span>
        1. <span data-ttu-id="f74ed-120">Määritä **Organisaation nimi** -kohdassa organisaation nimi.</span><span class="sxs-lookup"><span data-stu-id="f74ed-120">Under **Organization name**, enter the organization name.</span></span>
        1. <span data-ttu-id="f74ed-121">Anna **Alkuperäinen toimialueen nimi** -kohdassa alkuperäinen toimialueen nimi.</span><span class="sxs-lookup"><span data-stu-id="f74ed-121">Under **Initial domain name**, enter the initial domain name.</span></span>
        1. <span data-ttu-id="f74ed-122">Valitse **Maa tai alue** -kohdassa maa tai alue.</span><span class="sxs-lookup"><span data-stu-id="f74ed-122">For **Country or region**, select the country or region.</span></span>
        1. <span data-ttu-id="f74ed-123">Valitse **Luo**, jos haluat luoda vuokraajan.</span><span class="sxs-lookup"><span data-stu-id="f74ed-123">Select **Create** to create the tenant.</span></span>

     ![Uuden Azure AD -vuokraajan luominen](./media/B2CImage_2.png)

     - <span data-ttu-id="f74ed-125">**Linkitä olemassa oleva Azure AD B2C -vuokraaja omaan Azure-tilaukseen**: Käytä tätä vaihtoehtoa, jos sinulla on jo Azure AD B2C -vuokraaja, johon haluat linkittää.</span><span class="sxs-lookup"><span data-stu-id="f74ed-125">**Link an existing Azure AD B2C Tenant to my Azure subscription**: Use this option if you already have an Azure AD B2C tenant you want to link to.</span></span>
        1. <span data-ttu-id="f74ed-126">Valitse **Linkitä olemassa oleva Azure AD B2C -vuokraaja Azure-tilaukseen**.</span><span class="sxs-lookup"><span data-stu-id="f74ed-126">Select **Link an existing Azure AD B2C Tenant to my Azure subscription**.</span></span>
        1. <span data-ttu-id="f74ed-127">Valitse **Azure AD B2C -vuokraaja** -kohdassa soveltuva B2C-vuokraaja.</span><span class="sxs-lookup"><span data-stu-id="f74ed-127">For **Azure AD B2C Tenant**, select the appropriate B2C tenant.</span></span> <span data-ttu-id="f74ed-128">Jos valintaikkunaan tulee Kelvollisia B2C-vuokraajia ei löytynyt -sanoma, sinulla ei ole olemassa olevaa B2C-vuokraajaa, vaan se on luotava.</span><span class="sxs-lookup"><span data-stu-id="f74ed-128">If the message "No eligible B2C Tenants found" appears in the selection box, you do not have an existing eligible B2C tenant and will need to create a new one.</span></span>
        1. <span data-ttu-id="f74ed-129">Valitse **Resurssiryhmä**-kohdassa **Luo uusi**.</span><span class="sxs-lookup"><span data-stu-id="f74ed-129">For **Resource group**, select **Create new**.</span></span> <span data-ttu-id="f74ed-130">Anna **nimi** resurssiryhmälle, joka sisältää vuokraajan ja valitse **Resurssiryhmän sijainti**. Valitse lopuksi **Luo**.</span><span class="sxs-lookup"><span data-stu-id="f74ed-130">Enter a **Name** for the resource group that will contain the tenant, select the **Resource group location**, and then select **Create**.</span></span>

    ![Linkitä olemassa oleva Azure AD B2C -vuokraaja Azure-tilaukseen](./media/B2CImage_3.png)

1. <span data-ttu-id="f74ed-132">Kun uusi Azure AD B2C -hakemisto on luotu (tämä voi kestää jonkin aikaa), koontinäyttöön tulee näkyviin uuden hakemiston linkki.</span><span class="sxs-lookup"><span data-stu-id="f74ed-132">Once the new Azure AD B2C directory is created (this may take a few moments), a link to the new directory will appear on the dashboard.</span></span> <span data-ttu-id="f74ed-133">Tämä linkki ohjaa sinut Tervetuloa Azure Active Directory B2C -ratkaisun käyttäjäksi -sivulle.</span><span class="sxs-lookup"><span data-stu-id="f74ed-133">This link will direct you to the "Welcome to Azure Active Directory B2C" page.</span></span>

    ![Linkki uuteen AAD-hakemistoon](./media/B2CImage_4.png)

> [!NOTE]
> <span data-ttu-id="f74ed-135">Jos sinulla on useita Azure-tilin tilauksia tai jos olet määrittänyt B2C-vuokraajan ilman aktiivisen tilauksen linkkiä, **Vianmääritys**-banneri ohjaa sinut kohtaan, jossa voit linkittää vuokraajan ja tilauksen.</span><span class="sxs-lookup"><span data-stu-id="f74ed-135">If you have multiple subscriptions within your Azure account or have set up the B2C tenant without linking to an active subscription, a **Troubleshoot** banner will direct you to link the tenant to a subscription.</span></span> <span data-ttu-id="f74ed-136">Valitse vianmäärityksen sanoma ja ratkaise tilaukseen liittyvä ongelma ohjeiden avulla.</span><span class="sxs-lookup"><span data-stu-id="f74ed-136">Select the troubleshooting message and follow the instructions to resolve the subscription issue.</span></span>

<span data-ttu-id="f74ed-137">Seuraavassa kuvassa on esimerkki Azure AD B2C:n **Vianmääritys**-bannerista.</span><span class="sxs-lookup"><span data-stu-id="f74ed-137">The following image shows an example of an Azure AD B2C **Troubleshoot** banner.</span></span>

![Varoitus siitä, että hakemistolla ei ole aktiivista tilausta](./media/B2CImage_5.png)

## <a name="create-the-b2c-application"></a><span data-ttu-id="f74ed-139">B2C-sovelluksen luominen</span><span class="sxs-lookup"><span data-stu-id="f74ed-139">Create the B2C application</span></span>

<span data-ttu-id="f74ed-140">Kun B2C-vuokraaja on luotu, voit luoda B2C-sovelluksen vuokraajassa ja käyttää Commerce-toimintoja.</span><span class="sxs-lookup"><span data-stu-id="f74ed-140">Once the B2C tenant has been created, you will create a B2C application within the tenant to interact with the Commerce actions.</span></span>

<span data-ttu-id="f74ed-141">Luo B2C-sovellus seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="f74ed-141">To create the B2C application, follow these steps.</span></span>

1. <span data-ttu-id="f74ed-142">Valitse Azure-portaalissa **Sovellukset** ja valitse sitten **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="f74ed-142">In the Azure portal, select **Applications** and then select **Add**.</span></span>
1. <span data-ttu-id="f74ed-143">Anna **Nimi**-kohtaan halutun AAD B2C -sovelluksen nimi.</span><span class="sxs-lookup"><span data-stu-id="f74ed-143">Under **Name**, enter the name of the desired AAD B2C application.</span></span>
1. <span data-ttu-id="f74ed-144">Valitse **Verkkosovellus / verkon ohjelmointirajapinta** -kohdassa **Sisällytä verkkosovellus / verkon ohjelmointirajapinta** -kohdan arvoksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="f74ed-144">Under **Web App/Web API**, for **Include web app / web API**, select **Yes**.</span></span>
1. <span data-ttu-id="f74ed-145">Valitse **Salli implisiittinen työnkulku** -kohdan arvoksi **Kyllä** (oletusarvo).</span><span class="sxs-lookup"><span data-stu-id="f74ed-145">For **Allow implicit flow**, select **Yes** (the default value).</span></span>
1. <span data-ttu-id="f74ed-146">Anna **Vastauksen URL-osoite** -kohtaan määritetyt vastauksen URL-osoitteet.</span><span class="sxs-lookup"><span data-stu-id="f74ed-146">Under **Reply URL**, enter your dedicated reply URLs.</span></span> <span data-ttu-id="f74ed-147">Katso lisätietoja vastauksen URL-osoitteista ja niiden muotoilusta [Vastauksen URL-osoitteet](#reply-urls) -kohdasta.</span><span class="sxs-lookup"><span data-stu-id="f74ed-147">See [Reply URLs](#reply-urls) below for information on reply URLs and how to format them here.</span></span>
1. <span data-ttu-id="f74ed-148">Valitse **Sisällytä alkuperäinen asiakasohjelma** -kohdassa **Ei** (oletusarvo).</span><span class="sxs-lookup"><span data-stu-id="f74ed-148">For **Include native client**, select **No** (the default value).</span></span>
1. <span data-ttu-id="f74ed-149">Valitse **Luo**.</span><span class="sxs-lookup"><span data-stu-id="f74ed-149">Select **Create**.</span></span>

### <a name="reply-urls"></a><span data-ttu-id="f74ed-150">Vastauksen URL-osoitteet</span><span class="sxs-lookup"><span data-stu-id="f74ed-150">Reply URLs</span></span>

<span data-ttu-id="f74ed-151">Vastauksen URL-osoitteet ovat tärkeitä, koska ne mahdollistavat sallitut palautustoimialueet, kun sivusto kutsuu Azure AD B2C -ratkaisua käyttäjän todentamista varten.</span><span class="sxs-lookup"><span data-stu-id="f74ed-151">Reply URLs are important as they allow a whitelist of the return domains when your site calls Azure AD B2C to authenticate a user.</span></span> <span data-ttu-id="f74ed-152">Näin voit palauttaa todennetun käyttäjän takaisin toimialueelle, jolta nämä kirjautuvat (oman sivuston toimialue).</span><span class="sxs-lookup"><span data-stu-id="f74ed-152">This allows the return of the authenticated user back to the domain from which they are signing into (your site domain).</span></span> 

<span data-ttu-id="f74ed-153">Lisää **Vastauksen URL-osoite** -ruudun **Azure AD B2C - sovellukset \> Uusi sovellus** -näytössä erilliset rivit sivuston toimialueelle ja (ympäristön valmistelun jälkeen) Commercen luomalle URL-osoitteelle.</span><span class="sxs-lookup"><span data-stu-id="f74ed-153">In the **Reply URL** box on the **Azure AD B2c - Applications \> New application** screen, you need to add separate lines for both your site domain and (once your environment is provisioned) the Commerce-generated URL.</span></span> <span data-ttu-id="f74ed-154">Näissä URL-osoitteissa on aina käytettävä sallittua URL-osoitteen muotoa. Niiden on aina oltava perus-URL-osoitteita (ei lopussa olevia vinoviivoja tai polkuja).</span><span class="sxs-lookup"><span data-stu-id="f74ed-154">These URLs must always use a valid URL format and must be base URLs only (no trailing forward slashes or paths).</span></span> <span data-ttu-id="f74ed-155">Merkkijono ``/_msdyn365/authresp`` on siis liitettävä perus-URL-osoitteisiin seuraavien esimerkkien mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="f74ed-155">The string ``/_msdyn365/authresp`` then needs to be appended to the base URLs, as in the following examples.</span></span>

- ``https://fabrikam.com/_msdyn365/authresp``
- ``https://fabrikam-prod.commerce.dynamics.com/_msdyn365/authresp``

## <a name="create-user-flow-policies"></a><span data-ttu-id="f74ed-156">Käyttäjän työnkulkukäytäntöjen luominen</span><span class="sxs-lookup"><span data-stu-id="f74ed-156">Create user flow policies</span></span>

<span data-ttu-id="f74ed-157">Käyttäjän työnkulut ovat käytäntöjä, joita Azure AD B2C käyttää suojatun sisäänkirjauksen, rekisteröitymisen, profiilin muokkaamisen ja unohdetun salasanan käyttökokemusten määrittämisessä.</span><span class="sxs-lookup"><span data-stu-id="f74ed-157">User flows are the policies Azure AD B2C uses to provide secure sign in, sign up, edit profile, and forget password user experiences.</span></span> <span data-ttu-id="f74ed-158">Dynamics 365 Commerce suorittaa näiden työnkulkujen avulla käytäntöjen toiminnot, joiden avulla se toimii Azure AD B2C -vuokraajan kanssa.</span><span class="sxs-lookup"><span data-stu-id="f74ed-158">Dynamics 365 Commerce uses these flows to perform the policy actions to interact with the Azure AD B2C tenant.</span></span> <span data-ttu-id="f74ed-159">Kun käyttäjä käyttää näitä käytäntöjä, ne ohjataan uudelleen Azure AD B2C -vuokraajalle toimintojen suorittamista varten.</span><span class="sxs-lookup"><span data-stu-id="f74ed-159">When a user interacts with these policies, they are redirected to the Azure AD B2C tenant to perform the actions.</span></span>

<span data-ttu-id="f74ed-160">Azure AD B2C sisältää seuraavat kolme käyttäjän perustyönkulkutyyppiä:</span><span class="sxs-lookup"><span data-stu-id="f74ed-160">Azure AD B2C provides three basic user flow types:</span></span>
- <span data-ttu-id="f74ed-161">Rekisteröityminen ja sisäänkirjaus</span><span class="sxs-lookup"><span data-stu-id="f74ed-161">Sign up and sign in</span></span>
- <span data-ttu-id="f74ed-162">Profiilin muokkaaminen</span><span class="sxs-lookup"><span data-stu-id="f74ed-162">Profile editing</span></span>
- <span data-ttu-id="f74ed-163">Salasanan palauttaminen</span><span class="sxs-lookup"><span data-stu-id="f74ed-163">Password reset</span></span>

<span data-ttu-id="f74ed-164">Voit halutessasi käyttää Azure AD:n käyttäjän oletustyönkulkua. Se näyttää AAD B2C:n isännöimän sivun.</span><span class="sxs-lookup"><span data-stu-id="f74ed-164">You can choose to use the default user flows provided by Azure AD, which will display a page hosted by AAD B2C.</span></span> <span data-ttu-id="f74ed-165">Vaihtoehtoisesti voit luoda HTML-sivun, jonka avulla hallitaan näiden käyttäjän työnkulkukokemusten ulkoasua.</span><span class="sxs-lookup"><span data-stu-id="f74ed-165">Alternately, you can create an HTML page to control the look and feel of these user flow experiences.</span></span> 

<span data-ttu-id="f74ed-166">Jos haluat mukauttaa Dynamics 365 Commercen käyttäjän käytäntöjen sivuja, katso [Käyttäjän sisäänkirjausten mukautettujen sivujen määrittäminen](custom-pages-user-logins.md).</span><span class="sxs-lookup"><span data-stu-id="f74ed-166">To customize the user policy pages for Dynamics 365 Commerce, see [Set up custom pages for user logins](custom-pages-user-logins.md).</span></span> <span data-ttu-id="f74ed-167">Lisätietoja on kohdassa [Azure Active Directory B2C:n käyttäjäkokemusten käyttöliittymän mukauttaminen](https://docs.microsoft.com/azure/active-directory-b2c/tutorial-customize-ui).</span><span class="sxs-lookup"><span data-stu-id="f74ed-167">For additional information, see [Customize the interface of user experiences in Azure Active Directory B2C](https://docs.microsoft.com/azure/active-directory-b2c/tutorial-customize-ui).</span></span>

### <a name="create-a-sign-up-and-sign-in-user-flow-policy"></a><span data-ttu-id="f74ed-168">Rekisteröitymisen ja sisäänkirjauksen käyttäjän työnkulkukäytännön luominen</span><span class="sxs-lookup"><span data-stu-id="f74ed-168">Create a sign up and sign in user flow policy</span></span>

<span data-ttu-id="f74ed-169">Voit luoda rekisteröitymisen ja sisäänkirjauksen käyttäjän työnkulkukäytännön seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="f74ed-169">To create a sign up and sign in user flow policy, follow these steps.</span></span>

1. <span data-ttu-id="f74ed-170">Valitse Azure-portaalin vasemmanpuoleisessa siirtymisruudussa **Käyttäjän työnkulut (käytännöt)**.</span><span class="sxs-lookup"><span data-stu-id="f74ed-170">In the Azure portal, select **User flows (policies)** in the left navigation pane.</span></span>
1. <span data-ttu-id="f74ed-171">Valitse **Azure AD B2C – käyttäjän työnkulut (käytännöt)** -sivulla **Uusi käyttäjän työnkulku**.</span><span class="sxs-lookup"><span data-stu-id="f74ed-171">On the **Azure AD B2C – User flows (policies)** page, select **New User Flow**.</span></span>
1. <span data-ttu-id="f74ed-172">Valitse **Suositellut**-välilehdessä **Rekisteröidy ja kirjaudu sisään**.</span><span class="sxs-lookup"><span data-stu-id="f74ed-172">On the **Recommended** tab, select **Sign up and sign in**.</span></span>
1. <span data-ttu-id="f74ed-173">Anna käytännön nimi **Nimi**-kohdassa.</span><span class="sxs-lookup"><span data-stu-id="f74ed-173">Under **Name**, enter a policy name.</span></span> <span data-ttu-id="f74ed-174">Tämä nimi näkyy myöhemmin portaalin määrittämän etuliitteen kanssa (esimerkiksi B2C_1_).</span><span class="sxs-lookup"><span data-stu-id="f74ed-174">This name will display afterwards with a prefix the portal assigns (for example, "B2C_1_").</span></span>
1. <span data-ttu-id="f74ed-175">Valitse **Tunnistetietojen tarjoajat** -kohdassa soveltuva valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="f74ed-175">Under **Identity providers**, select the appropriate check box.</span></span>
1. <span data-ttu-id="f74ed-176">Valitse **Usean tekijän todennus** yritykselle soveltuva vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="f74ed-176">Under **Multifactor Authentication**, select the appropriate choice for your company.</span></span> 
1. <span data-ttu-id="f74ed-177">Valitse **Käyttäjän määritteet ja vaatimukset** -kohdassa vaihtoehdot määritteiden tai palautusvaatimusten keräämistä varten.</span><span class="sxs-lookup"><span data-stu-id="f74ed-177">Under **User attributes and claims**, select options to collect attributes or return claims as appropriate.</span></span> <span data-ttu-id="f74ed-178">Commerce edellyttää seuraavien oletusasetusten käyttämistä:</span><span class="sxs-lookup"><span data-stu-id="f74ed-178">Commerce requires the following default options:</span></span>

    | <span data-ttu-id="f74ed-179">**Keräilymäärite**</span><span class="sxs-lookup"><span data-stu-id="f74ed-179">**Collect  attribute**</span></span> | <span data-ttu-id="f74ed-180">**Palautusvaatimus**</span><span class="sxs-lookup"><span data-stu-id="f74ed-180">**Return  claim**</span></span> |
    | ---------------------- | ----------------- |
    |                        | <span data-ttu-id="f74ed-181">Sähköpostiosoitteet</span><span class="sxs-lookup"><span data-stu-id="f74ed-181">Email Addresses</span></span>   |
    | <span data-ttu-id="f74ed-182">Etunimi</span><span class="sxs-lookup"><span data-stu-id="f74ed-182">Given Name</span></span>             | <span data-ttu-id="f74ed-183">Etunimi</span><span class="sxs-lookup"><span data-stu-id="f74ed-183">Given Name</span></span>        |
    |                        | <span data-ttu-id="f74ed-184">Tunnistetietojen tarjoaja</span><span class="sxs-lookup"><span data-stu-id="f74ed-184">Identity Provider</span></span> |
    | <span data-ttu-id="f74ed-185">Sukunimi</span><span class="sxs-lookup"><span data-stu-id="f74ed-185">Surname</span></span>                | <span data-ttu-id="f74ed-186">Sukunimi</span><span class="sxs-lookup"><span data-stu-id="f74ed-186">Surname</span></span>           |
    |                        | <span data-ttu-id="f74ed-187">Käyttäjän objektin tunnus</span><span class="sxs-lookup"><span data-stu-id="f74ed-187">User’s Object ID</span></span>  |

1. <span data-ttu-id="f74ed-188">Valitse **Luo**.</span><span class="sxs-lookup"><span data-stu-id="f74ed-188">Select **Create**.</span></span>

<span data-ttu-id="f74ed-189">Seuraavassa kuvassa on esimerkki Azure AD B2C:n rekisteröitymisen ja sisäänkirjauksen käyttäjän työnkulusta.</span><span class="sxs-lookup"><span data-stu-id="f74ed-189">The following image is an example of the Azure AD B2C sign up and sign in user flow.</span></span>

![Rekisteröinti ja sisäänkirjaus -käytännön asetukset](./media/B2CImage_11.png)

<span data-ttu-id="f74ed-191">Seuraavassa kuvassa on **Suorita käyttäjän työnkulku** -vaihtoehto Azure AD B2C:n rekisteröitymisen ja sisäänkirjauksen käyttäjän työnkulussa.</span><span class="sxs-lookup"><span data-stu-id="f74ed-191">The following image shows the **Run user flow** option in the Azure AD B2C sign up and sign in user flow.</span></span>

![Käyttäjän työnkulku -vaihtoehdon suorittaminen käytännön työnkulussa](./media/B2CImage_23.png)
   
### <a name="create-a-profile-editing-user-flow-policy"></a><span data-ttu-id="f74ed-193">Profiilin muokkaamisen käyttäjän työnkulkukäytännön luominen</span><span class="sxs-lookup"><span data-stu-id="f74ed-193">Create a profile editing user flow policy</span></span>

<span data-ttu-id="f74ed-194">Voit luoda profiilin muokkaamisen käyttäjän työnkulkukäytännön seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="f74ed-194">To create a profile editing user flow policy, follow these steps.</span></span>

1. <span data-ttu-id="f74ed-195">Valitse Azure-portaalin vasemmanpuoleisessa siirtymisruudussa **Käyttäjän työnkulut (käytännöt)**.</span><span class="sxs-lookup"><span data-stu-id="f74ed-195">In the Azure portal, select **User flows (policies)** in the left navigation pane.</span></span>
1. <span data-ttu-id="f74ed-196">Valitse **Azure AD B2C – käyttäjän työnkulut (käytännöt)** -sivulla **Uusi käyttäjän työnkulku**.</span><span class="sxs-lookup"><span data-stu-id="f74ed-196">On the **Azure AD B2C – User flows (policies)** page, select **New User Flow**.</span></span>
1. <span data-ttu-id="f74ed-197">Valitse **Suositellut**-välilehdessä **Profiilin muokkaaminen**.</span><span class="sxs-lookup"><span data-stu-id="f74ed-197">On the **Recommended** tab, select **Profile editing**.</span></span>
1. <span data-ttu-id="f74ed-198">Anna **Nimi**-kohtaan profiilin muokkaamisen käyttäjän työnkulku.</span><span class="sxs-lookup"><span data-stu-id="f74ed-198">Under **Name**, enter the profile editing user flow.</span></span> <span data-ttu-id="f74ed-199">Tämä nimi näkyy myöhemmin portaalin määrittämän etuliitteen kanssa (esimerkiksi B2C_1_).</span><span class="sxs-lookup"><span data-stu-id="f74ed-199">This name will display afterwards with a prefix the portal assigns (for example, "B2C_1_").</span></span>
1. <span data-ttu-id="f74ed-200">Valitse **Tunnistetietojen tarjoajat** -kohdassa **Paikallisen tilin sisäänkirjaus**.</span><span class="sxs-lookup"><span data-stu-id="f74ed-200">Under **Identity providers**, select **Local Account SignIn**.</span></span>
1. <span data-ttu-id="f74ed-201">Valitse **Käyttäjän määritteet** -kohdassa seuraavat valintaruudut:</span><span class="sxs-lookup"><span data-stu-id="f74ed-201">Under **User attributes**, select the following check boxes:</span></span>
    - <span data-ttu-id="f74ed-202">**Sähköpostiosoitteet** (vain **Palautusvaatimus**)</span><span class="sxs-lookup"><span data-stu-id="f74ed-202">**Email Addresses** (**Return claim** only)</span></span>
    - <span data-ttu-id="f74ed-203">**Etunimi** (**Keräilymäärite** ja **Palautusvaatimus**)</span><span class="sxs-lookup"><span data-stu-id="f74ed-203">**Given Name** (**Collect attribute** and **Return claim**)</span></span>
    - <span data-ttu-id="f74ed-204">**Tunnistetietojen tarjoaja** (vain **Palautusvaatimus**)</span><span class="sxs-lookup"><span data-stu-id="f74ed-204">**Identity Provider** (**Return claim** only)</span></span>
    - <span data-ttu-id="f74ed-205">**Sukunimi** (**Keräilymäärite** ja **Palautusvaatimus**)</span><span class="sxs-lookup"><span data-stu-id="f74ed-205">**Surname** (**Collect attribute** and **Return claim**)</span></span>
    - <span data-ttu-id="f74ed-206">**Käyttäjän objektin tunnus** (vain **Palautusvaatimus**)</span><span class="sxs-lookup"><span data-stu-id="f74ed-206">**User's Object ID** (**Return claim** only)</span></span>
1. <span data-ttu-id="f74ed-207">Valitse **Luo**.</span><span class="sxs-lookup"><span data-stu-id="f74ed-207">Select **Create**.</span></span>

<span data-ttu-id="f74ed-208">Seuraavassa kuvassa on esimerkki Azure AD B2C:n profiilin muokkauksen käyttäjän työnkulusta.</span><span class="sxs-lookup"><span data-stu-id="f74ed-208">The following image shows an example of the Azure AD B2C profile editing user flow.</span></span>

![Profiilin muokkaamisen käyttäjän työnkulun luominen](./media/B2CImage_12.png)

### <a name="create-a-password-reset-user-flow-policy"></a><span data-ttu-id="f74ed-210">Salasanan palauttamisen käyttäjän työnkulkukäytännön luominen</span><span class="sxs-lookup"><span data-stu-id="f74ed-210">Create a password reset user flow policy</span></span>

<span data-ttu-id="f74ed-211">Voit luoda salasanan palauttamisen käyttäjän työnkulkukäytännön seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="f74ed-211">To create a password reset user flow policy, follow these steps.</span></span>

1. <span data-ttu-id="f74ed-212">Valitse Azure-portaalin vasemmanpuoleisessa siirtymisruudussa **Käyttäjän työnkulut (käytännöt)**.</span><span class="sxs-lookup"><span data-stu-id="f74ed-212">In the Azure portal, select **User flows (policies)** in the left navigation pane.</span></span>
1. <span data-ttu-id="f74ed-213">Valitse **Azure AD B2C – käyttäjän työnkulut (käytännöt)** -sivulla **Uusi käyttäjän työnkulku**.</span><span class="sxs-lookup"><span data-stu-id="f74ed-213">On the **Azure AD B2C – User flows (policies)** page, select **New User Flow**.</span></span>
1. <span data-ttu-id="f74ed-214">Valitse **Suositellut**-välilehdessä **Salasanan palauttaminen**.</span><span class="sxs-lookup"><span data-stu-id="f74ed-214">On the **Recommended** tab, select **Password Reset**.</span></span>
1. <span data-ttu-id="f74ed-215">Anna **Nimi**-kohtaan salasanan palauttamisen käyttäjän työnkulun nimi.</span><span class="sxs-lookup"><span data-stu-id="f74ed-215">Under **Name**, enter a name for the password reset user flow.</span></span>
1. <span data-ttu-id="f74ed-216">Valitse **Tunnistetietojen tarjoajat** -kohdassa **Nollaa salasana sähköpostiosoitteen avulla**.</span><span class="sxs-lookup"><span data-stu-id="f74ed-216">Under **Identity providers**, select **Reset password using email address**.</span></span>
1. <span data-ttu-id="f74ed-217">Valitse **Luo**.</span><span class="sxs-lookup"><span data-stu-id="f74ed-217">Select **Create**.</span></span>
1. <span data-ttu-id="f74ed-218">Valitse **Sovelluksen vaatimukset** -kohdassa seuraavat valintaruudut:</span><span class="sxs-lookup"><span data-stu-id="f74ed-218">Under **Application claims**, select the following check boxes:</span></span>
    - <span data-ttu-id="f74ed-219">**Sähköpostiosoitteet**</span><span class="sxs-lookup"><span data-stu-id="f74ed-219">**Email addresses**</span></span>
    - <span data-ttu-id="f74ed-220">**Etunimi**</span><span class="sxs-lookup"><span data-stu-id="f74ed-220">**Given Name**</span></span>
    - <span data-ttu-id="f74ed-221">**Sukunimi**</span><span class="sxs-lookup"><span data-stu-id="f74ed-221">**Surname**</span></span>
    - <span data-ttu-id="f74ed-222">**Käyttäjän objektin tunnus**</span><span class="sxs-lookup"><span data-stu-id="f74ed-222">**User's Object ID**</span></span>
1. <span data-ttu-id="f74ed-223">Valitse **Luo**.</span><span class="sxs-lookup"><span data-stu-id="f74ed-223">Select **Create**.</span></span>

<span data-ttu-id="f74ed-224">Seuraavassa kuvassa näytetään, miten **Palauta salasana sähköpostiosoitteen avulla** määritetään Azure AD B2C:n salasanan palauttamisen käyttäjän työnkulussa.</span><span class="sxs-lookup"><span data-stu-id="f74ed-224">The following image shows where to set **Reset Password using mail address** in the Azure AD B2C password reset user flow.</span></span>

![Salasanan palauttamisen käytännön Palauta salasana sähköpostiosoitteen avulla -kohdan määrittäminen](./media/B2CImage_13.png)

## <a name="add-social-identity-providers-optional"></a><span data-ttu-id="f74ed-226">Yhteisöpalvelun tunnistetietojen tarjoajien lisääminen (valinnainen)</span><span class="sxs-lookup"><span data-stu-id="f74ed-226">Add social identity providers (Optional)</span></span>

<span data-ttu-id="f74ed-227">Yhteisöpalvelun tunnistetietojen tarjoajat sallivat käyttäjien käyttää yhteisöpalvelun tilejä todennuksessa.</span><span class="sxs-lookup"><span data-stu-id="f74ed-227">Social identity providers allow users to use their social accounts for authentication.</span></span> <span data-ttu-id="f74ed-228">Yhteisöpalvelun tunnistepalvelun tarjoajan todentamisen lisääminen on valinnaista Dynamics 365 Commercessa.</span><span class="sxs-lookup"><span data-stu-id="f74ed-228">Adding social identity provider authentication is optional in Dynamics 365 Commerce.</span></span> 

<span data-ttu-id="f74ed-229">Jos yhteisöpalvelun tunnistetietojen tarjoajan todentamista ei lisätä, Azure AD B2C:n oletusprofiilit ovat käyttäjäkunnan pääprofiilit.</span><span class="sxs-lookup"><span data-stu-id="f74ed-229">If social identity provider authentication is not added, the default Azure AD B2C profiles will be the main profiles for your user base.</span></span> <span data-ttu-id="f74ed-230">Käyttäjät valitsevat oman käyttäjätunnuksen (haluamansa sähköpostiosoite) ja määrittävät salasanan.</span><span class="sxs-lookup"><span data-stu-id="f74ed-230">Users will select their own username (their preferred email address) and set a password.</span></span> <span data-ttu-id="f74ed-231">Azure AD B2C todentaa käyttäjät suoraan.</span><span class="sxs-lookup"><span data-stu-id="f74ed-231">Azure AD B2C will authenticate users directly.</span></span> 

<span data-ttu-id="f74ed-232">Jos yhteisöpalveluiden tunnustietojen tarjoajan todentaminen lisätään ja käyttäjä valitsee jonkin tarjotuista yhteisöpalveluiden tunnistetietojen tarjoajista, Azure AD B2C -vuokraajaan luodaan yhä yksikkö.</span><span class="sxs-lookup"><span data-stu-id="f74ed-232">If social identity provider authentication is added and a user chooses one of the social identity providers offered, an entity is still created in the Azure AD B2C tenant.</span></span> <span data-ttu-id="f74ed-233">Azure AD B2C todentaa tämän jälkeen käyttäjän valtuustiedot yhteisöpalvelujen tunnistetietojen tarjoajan avulla.</span><span class="sxs-lookup"><span data-stu-id="f74ed-233">Azure AD B2C will then authenticate the user's credentials with the social identity provider.</span></span>

> [!NOTE]
> <span data-ttu-id="f74ed-234">Tunnistetietojen tarjoajan sisäänkirjaus luo tietueen B2C-vuokraajaan. Se tehdään kuitenkin eri muodossa kuin paikalliset tilit, koska se kutsuu ulkoisen yhteisöpalvelujen tunnistetietojen tarjoajan viitteen todennusta varten.</span><span class="sxs-lookup"><span data-stu-id="f74ed-234">The identity provider sign in creates a record in the B2C tenant, but in a different format than local accounts since it will call the external social identity provider reference for authentication.</span></span> <span data-ttu-id="f74ed-235">Käyttäjä voi käyttää samaa sähköpostiosoitetta eri yhteisöpalvelujen tunnistetietojen tarjoajien kanssa. Tämä tarkoittaa sitä, että vuokraajan tunnistuksen käyttäjätunnuksena käyttämä sähköpostiosoite ei ehkä ole yksilöllinen.</span><span class="sxs-lookup"><span data-stu-id="f74ed-235">The user can use the same email address across social identity providers, meaning that the email username used for authentication may not be unique to the tenant.</span></span> <span data-ttu-id="f74ed-236">Azure AD B2C edellyttää vain, että käyttäjillä on yksilöllinen sähköpostiosoite paikallisilla B2C-tileillä.</span><span class="sxs-lookup"><span data-stu-id="f74ed-236">Azure AD B2C will only enforce that users have a unique email address on local B2C accounts.</span></span>

<span data-ttu-id="f74ed-237">Ennen kuin lisäät yhteisöpalvelujen tunnistetietojen tarjoajan todennusta varten, siirry tunnistetietojen tarjoajan portaaliin ja määritä tunnistetietojen tarjoajan sovellus Azure AD B2C -dokumentaatiossa määritetyllä tavalla.</span><span class="sxs-lookup"><span data-stu-id="f74ed-237">Before you can add a social identity provider for authentication, you must go to the identity provider's portal and set up an identity provider application as instructed in the Azure AD B2C documentation.</span></span> <span data-ttu-id="f74ed-238">Alla on luettelo dokumentaation linkeistä.</span><span class="sxs-lookup"><span data-stu-id="f74ed-238">A list of links to the documentation is provided below.</span></span>

- [<span data-ttu-id="f74ed-239">Amazon</span><span class="sxs-lookup"><span data-stu-id="f74ed-239">Amazon</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-amzn-app)
- [<span data-ttu-id="f74ed-240">Azure AD (yksi vuokraaja)</span><span class="sxs-lookup"><span data-stu-id="f74ed-240">Azure AD (Single Tenant)</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-oidc-azure-active-directory)
- [<span data-ttu-id="f74ed-241">Microsoft-tili</span><span class="sxs-lookup"><span data-stu-id="f74ed-241">Microsoft Account</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-msa-app)
- [<span data-ttu-id="f74ed-242">Facebook</span><span class="sxs-lookup"><span data-stu-id="f74ed-242">Facebook</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-fb-app)
- [<span data-ttu-id="f74ed-243">GitHub</span><span class="sxs-lookup"><span data-stu-id="f74ed-243">GitHub</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-github-app)
- [<span data-ttu-id="f74ed-244">Google</span><span class="sxs-lookup"><span data-stu-id="f74ed-244">Google</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-goog-app)
- [<span data-ttu-id="f74ed-245">LinkedIn</span><span class="sxs-lookup"><span data-stu-id="f74ed-245">LinkedIn</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-li-app)
- [<span data-ttu-id="f74ed-246">OpenID Connect</span><span class="sxs-lookup"><span data-stu-id="f74ed-246">OpenID Connect</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-oidc-idp)
- [<span data-ttu-id="f74ed-247">Twitter</span><span class="sxs-lookup"><span data-stu-id="f74ed-247">Twitter</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-twitter-app)

### <a name="add-and-set-up-a-social-identity-provider"></a><span data-ttu-id="f74ed-248">Yhteisöpalvelujen tunnistetietojen tarjoajan lisääminen ja määrittäminen</span><span class="sxs-lookup"><span data-stu-id="f74ed-248">Add and set up a social identity provider</span></span>

<span data-ttu-id="f74ed-249">Voit lisätä ja määrittää yhteisöpalveluiden tunnistetietojen tarjoajan seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="f74ed-249">To add and set up a social identity provider, follow these steps.</span></span>  

1. <span data-ttu-id="f74ed-250">Siirry Azure-portaalissa kohtaan **Tunnistetietojen tarjoajat**.</span><span class="sxs-lookup"><span data-stu-id="f74ed-250">In the Azure portal, navigate to **Identity Providers**.</span></span>
1. <span data-ttu-id="f74ed-251">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="f74ed-251">Select **Add**.</span></span> <span data-ttu-id="f74ed-252">Näkyviin tulee **Lisää tunnistetietojen tarjoaja** -näyttö.</span><span class="sxs-lookup"><span data-stu-id="f74ed-252">The **Add identity provider** screen appears.</span></span>
1. <span data-ttu-id="f74ed-253">Anna **Nimi**-kohtaan käyttäjille sisäänkirjausnäytössä näytettävä nimi.</span><span class="sxs-lookup"><span data-stu-id="f74ed-253">Under **Name**, enter the name to be displayed to users on your sign in screen.</span></span>
1. <span data-ttu-id="f74ed-254">Valitse **Tunnistetietojen tarjoajan tyyppi** -kohtaan luettelosta tunnistetietojen tarjoaja.</span><span class="sxs-lookup"><span data-stu-id="f74ed-254">Under **Identity provider type**, select an identity provider from the list.</span></span>
1. <span data-ttu-id="f74ed-255">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="f74ed-255">Select **OK**.</span></span>
1. <span data-ttu-id="f74ed-256">Valitse **Määritä tämä tunnistetietojen tarjoaja**, jos haluat ottaa käyttöön **Määritä yhteisöpalvelujen tunnistetietojen tarjoaja** -näytön.</span><span class="sxs-lookup"><span data-stu-id="f74ed-256">Select **Set up this identity provider** to access the **Set up the social identity provider** screen.</span></span>
1. <span data-ttu-id="f74ed-257">Anna **Asiakasohjelman tunnus** -kohdassa tunnistetietojen tarjoajan sovelluksen asetuksista saatu asiakasohjelman tunnus.</span><span class="sxs-lookup"><span data-stu-id="f74ed-257">Under **Client ID**, enter the client ID as obtained from the identity provider application setup.</span></span>
1. <span data-ttu-id="f74ed-258">Anna **Asiakasohjelman salasana** -kohdassa tunnistetietojen tarjoajan sovelluksen asetuksista saatu asiakasohjelman salasana.</span><span class="sxs-lookup"><span data-stu-id="f74ed-258">Under **Client secret**, enter the client secret as obtained from the identity provider application setup.</span></span>
1. <span data-ttu-id="f74ed-259">Liitä käyttäjän työnkulku rekisteröitymis ja sisäänkirjauskäytäntöihin seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="f74ed-259">Attach user flow for sign in sign up policies:</span></span>
1. <span data-ttu-id="f74ed-260">Siirry kohtaan **Azure AD B2C – käyttäjän työnkulut (käytännöt) \> {oma sisäänkirjaus- ja rekisteröitymiskäytäntö} \> Tunnistetietojen tarjoajat**.</span><span class="sxs-lookup"><span data-stu-id="f74ed-260">Go to **Azure AD B2C – User flows (policies) \> {your sign-in sign-up policy} \> Identity providers**.</span></span>
1. <span data-ttu-id="f74ed-261">Voit liittää sisäänkirjauksen/rekisteröitymisen käyttäjän työnkulun käytännön valitsemalla kunkin tunnistetietojen tarjoajan, jonka olet määrittänyt tiliä varten.</span><span class="sxs-lookup"><span data-stu-id="f74ed-261">To attach the sign in/sign up user flow policy, select each identity provider you have set up for your account.</span></span> <span data-ttu-id="f74ed-262">Jos haluat testata nämä, valitse **Suorita käyttäjän työnkulku** jokaisen tunnistetietojen tarjoajan kohdalla.</span><span class="sxs-lookup"><span data-stu-id="f74ed-262">To test these, select **Run user flow** for each identity provider.</span></span> <span data-ttu-id="f74ed-263">Uudessa välilehdessä näkyy kirjautumissivu, joka sisältää uuden tunnistetietojen tarjoajan valintaruudun.</span><span class="sxs-lookup"><span data-stu-id="f74ed-263">A new tab will display the sign-in page displaying the new identity provider selection box.</span></span>

<span data-ttu-id="f74ed-264">Seuraavassa kuvassa on esimerkki **Lisää tunnistetietojen tarjoaja**- ja **Määritä yhteisöpalvelujen tunnistetietojen tarjoaja** -näytöistä Azure AD B2C:ssä.</span><span class="sxs-lookup"><span data-stu-id="f74ed-264">The following image shows examples of the **Add identity provider** and **Set up the social identity provider** screens in Azure AD B2C.</span></span>

![Yhteisöpalvelujen tunnistetietojen tarjoajan lisääminen sovellukseen](./media/B2CImage_14.png)

<span data-ttu-id="f74ed-266">Seuraavassa kuvassa on esimerkki siitä, miten tunnistetietojen tarjoajat valitaan Azure AD B2C:n **Tunnistetietojen tarjoaja** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="f74ed-266">The following image shows an example of how to select identity providers on the Azure AD B2C **Identity Providers** page.</span></span>

![Valitse käytäntöä varten kaikki yhteisöpalvelujen tunnistetietojen tarjoajat, jotka otetaan käyttöön](./media/B2CImage_16.png)

<span data-ttu-id="f74ed-268">Seuraavassa kuvassa on esimerkki oletussisäänkirjausnäytöstä, jossa näkyy yhteisöpalveluiden tunnistetietojen tarjoajan sisäänkirjauspainike.</span><span class="sxs-lookup"><span data-stu-id="f74ed-268">The following image shows an example of a default sign-in screen with a social identity provider sign-in button displayed.</span></span>

![Esimerkki oletussisäänkirjausnäytöstä, jossa näkyy yhteisöpalveluiden tunnistetietojen tarjoajan sisäänkirjauspainike](./media/B2CImage_17.png)

## <a name="update-commerce-headquarters-with-the-new-azure-ad-b2c-information"></a><span data-ttu-id="f74ed-270">Commerce-pääkonttorin päivittäminen uusilla Azure AD B2C -tiedoilla</span><span class="sxs-lookup"><span data-stu-id="f74ed-270">Update Commerce headquarters with the new Azure AD B2C information</span></span>

<span data-ttu-id="f74ed-271">Kun Azure AD B2C:n yllä mainitut valmisteluvaiheet on tehty, Azure AD B2C -sovellus on rekisteröitävä Dynamics 365 Commerce -ympäristöön.</span><span class="sxs-lookup"><span data-stu-id="f74ed-271">Once the Azure AD B2C provisioning steps above are completed, the Azure AD B2C application must be registered in your Dynamics 365 Commerce environment.</span></span>

<span data-ttu-id="f74ed-272">Voit päivittää pääkonttorin uusilla Azure AD B2C -tiedoilla seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="f74ed-272">To update headquarters with the new Azure AD B2C information, follow these steps.</span></span>

1. <span data-ttu-id="f74ed-273">Valitse Commercessa **Kaupan yhteiset parametrit** ja valitse **Tunnistetietojen tarjoajat** vasemmanpuoleisessa valikossa.</span><span class="sxs-lookup"><span data-stu-id="f74ed-273">In Commerce, go to **Commerce Shared Parameters** and select **Identity Providers** in the left menu.</span></span>
1. <span data-ttu-id="f74ed-274">Tee **Tunnistetietojen tarjoajat** -kohdassa seuraavat toiminnot:</span><span class="sxs-lookup"><span data-stu-id="f74ed-274">Under **Identity Providers**, do the following:</span></span>
    1. <span data-ttu-id="f74ed-275">Anna **Myöntäjä**-ruutuun tunnistetietojen tarjoajan myöntäjän URL-osoite.</span><span class="sxs-lookup"><span data-stu-id="f74ed-275">In the **Issuer** box, enter the identity provider issuer URL.</span></span> <span data-ttu-id="f74ed-276">Voit etsiä myöntäjän URL-osoitteen alla olevan [Myöntäjän URL-osoitteen hankkiminen](#obtain-issuer-url) -kohdan avulla.</span><span class="sxs-lookup"><span data-stu-id="f74ed-276">To find your issuer URL, see [Obtain issuer URL](#obtain-issuer-url) below.</span></span>
    1. <span data-ttu-id="f74ed-277">Anna **Nimi**-ruutuun myöntäjän tietueen nimi.</span><span class="sxs-lookup"><span data-stu-id="f74ed-277">In the **Name** box, enter a name for your issuer record.</span></span>
    1. <span data-ttu-id="f74ed-278">Anna **Tyyppi**-ruutuun **Azure AD B2C (id_token)**.</span><span class="sxs-lookup"><span data-stu-id="f74ed-278">In the **Type** box, enter **Azure AD B2C (id_token)**.</span></span>
1. <span data-ttu-id="f74ed-279">Valitse yllä mainittu B2C:n tunnistetietojen tarjoajan nimike ja tee **Luovuttavat osapuolet** -kohdassa seuraavat toiminnot:</span><span class="sxs-lookup"><span data-stu-id="f74ed-279">Under **Relying Parties**, with the above B2C identity provider item selected, do the following:</span></span>
    1. <span data-ttu-id="f74ed-280">Anna **ClientID**-ruutuun B2C-sovelluksen tunnus.</span><span class="sxs-lookup"><span data-stu-id="f74ed-280">In the **ClientID** box, enter your B2C application ID.</span></span> <span data-ttu-id="f74ed-281">Se löytyy **Sovelluksen tunnus** -ruudusta B2C-sovelluksen ominaisuuksien sivulta.</span><span class="sxs-lookup"><span data-stu-id="f74ed-281">You can find this in the **Application ID** box of your B2C application's properties page.</span></span>
    1. <span data-ttu-id="f74ed-282">Kirjoita **Tyyppi**-ruutuun **Julkinen**.</span><span class="sxs-lookup"><span data-stu-id="f74ed-282">In the **Type** box, enter **Public**.</span></span>
    1. <span data-ttu-id="f74ed-283">Kirjoita **Käyttäjätyyppi**-ruutuun **Asiakas**.</span><span class="sxs-lookup"><span data-stu-id="f74ed-283">In the **User Type** box, enter **Customer**.</span></span>
1. <span data-ttu-id="f74ed-284">Valitse toimintoruudussa **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="f74ed-284">On the action pane, select **Save**.</span></span>
1. <span data-ttu-id="f74ed-285">Etsi Commerce-hakuruudussa **numerosarjat** (Organisaation hallinta > Numerosarjat).</span><span class="sxs-lookup"><span data-stu-id="f74ed-285">In the Commerce search box, search for **Number sequences** (Organization administration > Number sequences).</span></span>
1. <span data-ttu-id="f74ed-286">Valitse toimintoruudun alla **Muokkaa**. Se on **Ylläpidä**-kohdassa.</span><span class="sxs-lookup"><span data-stu-id="f74ed-286">Under the action pane, select **Edit** under **Maintain**.</span></span>
1. <span data-ttu-id="f74ed-287">Valitse **Yleinen**-pikavälilehdessä **Ei** **Manuaalinen**-kohdan arvoksi.</span><span class="sxs-lookup"><span data-stu-id="f74ed-287">On the **General** fast tab, select **No** for **Manual**.</span></span>
1. <span data-ttu-id="f74ed-288">Valitse toimintoruudussa **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="f74ed-288">On the action pane, select **Save**.</span></span> 
1. <span data-ttu-id="f74ed-289">Hae Commerce-hakuruudussa **Jakeluaikataulu**</span><span class="sxs-lookup"><span data-stu-id="f74ed-289">In the Commerce search box, search for **Distribution schedule**</span></span>
1. <span data-ttu-id="f74ed-290">Valitse **Jakeluaikataulut**-sivun vasemmanpuoleisessa valikossa **1110 Yleinen määritys** -työ.</span><span class="sxs-lookup"><span data-stu-id="f74ed-290">In the left navigation menu of the **Distribution schedules** page, select job **1110 Global configuration**.</span></span>
1. <span data-ttu-id="f74ed-291">Valitse toimintoruudussa **Suorita nyt**.</span><span class="sxs-lookup"><span data-stu-id="f74ed-291">On the action pane, select **Run Now**.</span></span>

### <a name="obtain-issuer-url"></a><span data-ttu-id="f74ed-292">Myöntäjän URL-osoitteen hankkiminen</span><span class="sxs-lookup"><span data-stu-id="f74ed-292">Obtain issuer URL</span></span>

<span data-ttu-id="f74ed-293">Voit hankkia tunnistetietojen tarjoajan URL-osoitteen seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="f74ed-293">To obtain your identity provider issuer URL, follow these steps.</span></span>

1. <span data-ttu-id="f74ed-294">Luo metatietojen URL-osoite seuraavassa muodossa käyttämällä B2C-vuokraajaa ja käytäntöä seuraavasti: ``https://<B2CTENANTNAME>.b2clogin.com/<B2CTENANTNAME>.onmicrosoft.com/v2.0/.well-known/openid-configuration?p=<B2CSIGN-INPOLICY>``</span><span class="sxs-lookup"><span data-stu-id="f74ed-294">Create a metadata address URL in the following format using your B2C tenant and policy: ``https://<B2CTENANTNAME>.b2clogin.com/<B2CTENANTNAME>.onmicrosoft.com/v2.0/.well-known/openid-configuration?p=<B2CSIGN-INPOLICY>``</span></span>
    - <span data-ttu-id="f74ed-295">Esimerkki: ``https://d365plc.b2clogin.com/d365plc.onmicrosoft.com/v2.0/.well-known/openid-configuration?p=B2C_1_signinup``.</span><span class="sxs-lookup"><span data-stu-id="f74ed-295">Example: ``https://d365plc.b2clogin.com/d365plc.onmicrosoft.com/v2.0/.well-known/openid-configuration?p=B2C_1_signinup``.</span></span>
1. <span data-ttu-id="f74ed-296">Kirjoita metatietojen osoitteen URL-osoite selaimen osoitepalkkiin.</span><span class="sxs-lookup"><span data-stu-id="f74ed-296">Enter the metadata address URL into a browser address bar.</span></span>
1. <span data-ttu-id="f74ed-297">Kopioi metatiedoissa tunnistetietojen tarjoajan myöntäjän URL-osoite (**myöntäjän** arvo).</span><span class="sxs-lookup"><span data-stu-id="f74ed-297">In the metadata, copy the identity provider issuer URL (the value for **"issuer"**).</span></span>
    - <span data-ttu-id="f74ed-298">Esimerkki: ``https://login.fabrikam.com/073405c3-0113-4f43-b5e2-df01266e24ae/v2.0/``.</span><span class="sxs-lookup"><span data-stu-id="f74ed-298">Example: ``https://login.fabrikam.com/073405c3-0113-4f43-b5e2-df01266e24ae/v2.0/``.</span></span>

## <a name="configure-your-b2c-tenant-in-commerce-site-builder"></a><span data-ttu-id="f74ed-299">B2C-vuokraajan määrittäminen Commerce-sivuston luontiohjelmassa</span><span class="sxs-lookup"><span data-stu-id="f74ed-299">Configure your B2C tenant in Commerce site builder</span></span>

<span data-ttu-id="f74ed-300">Kun Azure AD B2C -vuokraajan määrittäminen on tehty, B2C-vuokraaja on määritettävä Commerce-sivuston luontiohjelmassa.</span><span class="sxs-lookup"><span data-stu-id="f74ed-300">Once setup of your Azure AD B2C tenant is completed, you must configure the B2C tenant in Commerce site builder.</span></span> <span data-ttu-id="f74ed-301">Määritysvaiheita ovat esimerkiksi B2C-sovelluksen tietojen kerääminen Azure-portaalista, B2C-sovelluksen tietojen syöttäminen sivuston luontiohjelmaan ja B2C-sovelluksen liittäminen sivustoon ja kanavaan.</span><span class="sxs-lookup"><span data-stu-id="f74ed-301">Configuration steps include collecting B2C application information from the Azure portal, entering that B2C application information into site builder, and then associating the B2C application with your site and channel.</span></span>

### <a name="collect-the-required-application-information"></a><span data-ttu-id="f74ed-302">Tarvittavien sovellustietojen kerääminen</span><span class="sxs-lookup"><span data-stu-id="f74ed-302">Collect the required application information</span></span>

<span data-ttu-id="f74ed-303">Voit kerätä tarvittavat sovellustiedot seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="f74ed-303">To collect the required application information, follow these steps.</span></span>

1. <span data-ttu-id="f74ed-304">Siirry Azure-portaalissa kohtaan **Aloitus \> Azure AD B2C - sovellukset**.</span><span class="sxs-lookup"><span data-stu-id="f74ed-304">In the Azure portal, go to **Home \> Azure AD B2C - Applications**.</span></span>
1. <span data-ttu-id="f74ed-305">Valitse sovellus ja valitse sitten vasemmanpuoleisesta navigointiruudusta **Ominaisuudet**, jos haluat hakea sovelluksen tiedot.</span><span class="sxs-lookup"><span data-stu-id="f74ed-305">Select your application, and then in the left navigation pane select **Properties** to obtain the application details.</span></span>
1. <span data-ttu-id="f74ed-306">Kerää **Sovelluksen tunnus** -ruudusta B2C-sovelluksen tunnus, jonka B2C-vuokraaja loi.</span><span class="sxs-lookup"><span data-stu-id="f74ed-306">From the **Application ID** box, collect the application ID of the B2C application created in your B2C tenant.</span></span> <span data-ttu-id="f74ed-307">Tämä syötetään myöhemmin **Asiakasohjelman GUID** -arvona sivuston luontiohjelmaan.</span><span class="sxs-lookup"><span data-stu-id="f74ed-307">This will later be entered as the **Client GUID** in site builder.</span></span>
1. <span data-ttu-id="f74ed-308">Kerää **Vastauksen URL-osoite** -kohdasta vastauksen URL-osoite.</span><span class="sxs-lookup"><span data-stu-id="f74ed-308">Under **Reply URL**, collect the reply URL.</span></span>
1. <span data-ttu-id="f74ed-309">Siirry kohtaan **Aloitus \> Azure AD B2C – käyttäjän työnkulut (käytännöt)** ja kerää sitten kunkin käyttäjän työnkulkukäytännön nimet.</span><span class="sxs-lookup"><span data-stu-id="f74ed-309">Go to **Home \> Azure AD B2C – User flows (policies)**, and then collect the names of each user flow policy.</span></span>

<span data-ttu-id="f74ed-310">Seuraavassa kuvassa on esimerkki **Azure AD B2C - sovellukset** -sivusta.</span><span class="sxs-lookup"><span data-stu-id="f74ed-310">The following image shows an example of the **Azure AD B2C - Applications** page.</span></span>

![Siirtyminen vuokraajan B2C-sovellukseen](./media/B2CImage_19.png)

<span data-ttu-id="f74ed-312">Seuraavassa kuvassa on esimerkki sovelluksen **Ominaisuudet** -sivusta Azure AD B2C -ratkaisussa.</span><span class="sxs-lookup"><span data-stu-id="f74ed-312">The following image shows an example of an application **Properties** page in Azure AD B2C.</span></span> 

![Sovelluksen tunnuksen kopioiminen B2C-sovelluksen ominaisuuksista](./media/B2CImage_21.png)

<span data-ttu-id="f74ed-314">Seuraavassa kuvassa on esimerkki käyttäjän työnkulkukäytännöistä **Azure AD B2C – käyttäjän työnkulut (käytännöt)** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="f74ed-314">The following image shows an example of user flow policies on the **Azure AD B2C – User flows (policies)** page.</span></span>

![Kaikkien B2C-käytännön työnkulun nimien kerääminen](./media/B2CImage_22.png)

### <a name="enter-your-aad-b2c-tenant-application-information-into-commerce"></a><span data-ttu-id="f74ed-316">AAD B2C -vuokraajan sovelluksen tietojen syöttäminen Commerceen</span><span class="sxs-lookup"><span data-stu-id="f74ed-316">Enter your AAD B2C tenant application information into Commerce</span></span>

<span data-ttu-id="f74ed-317">Anna Azure AD B2C -vuokraajan tiedot Commercen sivuston luontiohjelmaan ennen B2C-vuokraajan liittämistä sivustoihin.</span><span class="sxs-lookup"><span data-stu-id="f74ed-317">You must enter details of the Azure AD B2C tenant into Commerce site builder before associating the B2C tenant with your site(s).</span></span>

<span data-ttu-id="f74ed-318">Voit lisätä AAD B2C -vuokraajan sovelluksen tiedot Commerceen seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="f74ed-318">To add your AAD B2C tenant application information to Commerce, follow these steps.</span></span>

1. <span data-ttu-id="f74ed-319">Kirjaudu sisään järjestelmänvalvojana Commerce-sivuston luontiohjelmaan ympäristössä.</span><span class="sxs-lookup"><span data-stu-id="f74ed-319">Sign in as an administrator to Commerce site builder for your environment.</span></span>
1. <span data-ttu-id="f74ed-320">Laajenna se valitsemalla vasemmasta siirtymisruudusta **Vuokraajan asetukset**.</span><span class="sxs-lookup"><span data-stu-id="f74ed-320">In the left navigation pane, select **Tenant Settings**  to expand it.</span></span>
1. <span data-ttu-id="f74ed-321">Valitse **Vuokraajan asetukset** -kohdasta **B2C-asetukset**.</span><span class="sxs-lookup"><span data-stu-id="f74ed-321">Under **Tenant Settings**, select **B2C Settings**.</span></span> 
1. <span data-ttu-id="f74ed-322">Valitse pääikkunassa **B2C-sovellukset**-kohdan vieressä oleva **Hallitse**.</span><span class="sxs-lookup"><span data-stu-id="f74ed-322">In the main window next **B2C Applications**, select **Manage**.</span></span> <span data-ttu-id="f74ed-323">(Jos vuokraaja näkyy B2C-sovellukset-luettelossa, järjestelmänvalvoja on jo lisännyt sen.</span><span class="sxs-lookup"><span data-stu-id="f74ed-323">(If your tenant appears in the B2C Applications list, then it was already added by an administrator.</span></span> <span data-ttu-id="f74ed-324">Tarkista, että vaiheen 6 nimikkeet vastaavat B2C-sovellusta.)</span><span class="sxs-lookup"><span data-stu-id="f74ed-324">Verify that the items in step 6 below match your B2C Application.)</span></span>
1. <span data-ttu-id="f74ed-325">Valitse **Lisää B2C-sovellus**.</span><span class="sxs-lookup"><span data-stu-id="f74ed-325">Select **Add B2C Application**.</span></span>
1. <span data-ttu-id="f74ed-326">Anna seuraavat pakolliset nimikkeet näkyvissä olevassa muodossa käyttämällä B2C-vuokraajan ja sovelluksen arvoja.</span><span class="sxs-lookup"><span data-stu-id="f74ed-326">Enter the following required items in the form displayed, using values from your B2C tenant and application.</span></span> <span data-ttu-id="f74ed-327">Kentät, jotka eivät ole pakollisia (joissa ei ole tähteä), voidaan jättää tyhjäksi.</span><span class="sxs-lookup"><span data-stu-id="f74ed-327">Fields that are not required (those without an asterisk) may be left blank.</span></span>

    - <span data-ttu-id="f74ed-328">**Sovelluksen nimi**: B2C-sovelluksen nimi, esimerkiksi FABRIKAM B2C.</span><span class="sxs-lookup"><span data-stu-id="f74ed-328">**Application Name**: The name for your B2C Application, for example "Fabrikam B2C".</span></span>
    - <span data-ttu-id="f74ed-329">**Vuokraajan nimi** B2C-vuokraajan nimi, esimerkiksi Fabrikam.</span><span class="sxs-lookup"><span data-stu-id="f74ed-329">**Tenant Name**: The name of your B2C Tenant, for example "Fabrikam".</span></span>
    - <span data-ttu-id="f74ed-330">**Unohdetun salasanan käytännön tunnus**: Unohdetun salasanan käyttäjän työnkulkukäytännön tunnus, esimerkiksi B2C_1_PasswordReset.</span><span class="sxs-lookup"><span data-stu-id="f74ed-330">**Forget Password Policy ID**: The forget password user flow policy ID, for example "B2C_1_PasswordReset".</span></span>
    - <span data-ttu-id="f74ed-331">**SignUp SignIn -käytännön tunnus**: Rekisteröitymisen ja sisäänkirjauksen käyttäjän työnkulkukäytännön tunnus, esimerkiksi B2C_1_signup_signin.</span><span class="sxs-lookup"><span data-stu-id="f74ed-331">**Signup Signin Policy ID**: The sign up and sign in user flow policy ID, for example "B2C_1_signup_signin".</span></span>
    - <span data-ttu-id="f74ed-332">**Asiakasohjelman GUID**: B2C-sovelluksen tunnus, esimerkiksi 22290eb2-c52e-42e9-8b35-a2b0a3bcb9e6.</span><span class="sxs-lookup"><span data-stu-id="f74ed-332">**Client GUID**: The B2C application ID, for example "22290eb2-c52e-42e9-8b35-a2b0a3bcb9e6".</span></span>
    - <span data-ttu-id="f74ed-333">**Profiilin muokkauskäytännön tunnus**: Profiilin muokkaamisen käyttäjän työnkulkukäytännön tunnus, esimerkiksi B2C_1A_ProfileEdit.</span><span class="sxs-lookup"><span data-stu-id="f74ed-333">**Edit Profile Policy ID**: The profile editing user flow policy ID, for example "B2C_1A_ProfileEdit".</span></span>

1. <span data-ttu-id="f74ed-334">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="f74ed-334">Select **OK**.</span></span> <span data-ttu-id="f74ed-335">B2C-sovelluksen nimi tulee nyt näkyviin luetteloon.</span><span class="sxs-lookup"><span data-stu-id="f74ed-335">You should now see the name of your B2C application appear in the list.</span></span>

### <a name="associate-the-b2c-application-to-your-site-and-channel"></a><span data-ttu-id="f74ed-336">B2C-sovelluksen liittäminen sivustoon ja kanavaan</span><span class="sxs-lookup"><span data-stu-id="f74ed-336">Associate the B2C application to your site and channel</span></span>

> [!WARNING]
> <span data-ttu-id="f74ed-337">Jos sivusto on jo liitetty B2C-sovellukseen, toiseen B2C-sovellukseen vaihtaminen poistaa tähän ympäristöön jo rekisteröityneiden käyttäjien nykyiset viitteet.</span><span class="sxs-lookup"><span data-stu-id="f74ed-337">If your site is already associated with a B2C application, changing to a different B2C application will remove the current references established for users already signed up in this environment.</span></span> <span data-ttu-id="f74ed-338">Jos tätä muutetaan, mitkään tällä hetkellä liitetyn B2C-sovelluksen tunnistetiedot eivät ole käyttäjien käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="f74ed-338">If changed, any credentials associated with the currently-assigned B2C application will not be available to users.</span></span> 
> 
> <span data-ttu-id="f74ed-339">Päivitä vain B2C-sovellus, jos olet määrittämässä kanavan B2C-sovellusta ensimmäistä kertaa tai jos yrität saada käyttäjät rekisteröitymään uudelleen tähän kanavaan uuden B2C-sovelluksen avulla uusilla tunnistetiedoilla.</span><span class="sxs-lookup"><span data-stu-id="f74ed-339">Only update the B2C application if you are setting up the channel's B2C application for the first time or if you intend to have users re-sign up with new credentials to this channel with the new B2C application.</span></span> <span data-ttu-id="f74ed-340">Ole varovainen, kun liität kanavia B2C-sovelluksiin. Anna sovelluksille selkeät nimet.</span><span class="sxs-lookup"><span data-stu-id="f74ed-340">Take caution when associating channels to B2C applications, and name applications clearly.</span></span> <span data-ttu-id="f74ed-341">Jos kanavaa ei ole liitetty B2C-sovellukseen alla kuvattujen vaiheiden avulla, kanavaan kirjautuvat käyttäjät siirretään B2C-sovellukseen, joka on **oletussovellus** B2C-sovellusten **Vuokraajan asetukset \> B2C-asetukset** -luettelossa.</span><span class="sxs-lookup"><span data-stu-id="f74ed-341">If a channel is not associated to a B2C application in the steps below, users signing into that channel for your site will be entered into the B2C application showing as **default** in the **Tenant Settings \> B2C Settings** list of B2C applications.</span></span>

<span data-ttu-id="f74ed-342">Voit liittää B2C-sovelluksen sivustoon ja kanavaan seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="f74ed-342">To associate the B2C application to your site and channel, follow these steps.</span></span>

1. <span data-ttu-id="f74ed-343">Siirry sivustoon Commerce-sivuston luontiohjelmassa.</span><span class="sxs-lookup"><span data-stu-id="f74ed-343">Navigate to your site in Commerce site builder.</span></span>
1. <span data-ttu-id="f74ed-344">Laajenna se valitsemalla vasemmasta siirtymisruudusta **Sivuston asetukset**.</span><span class="sxs-lookup"><span data-stu-id="f74ed-344">In the left navigation pane, select **Site Settings** to expand it.</span></span>
1. <span data-ttu-id="f74ed-345">Valitse **Sivuston asetukset** -kohdassa **Kanavat**.</span><span class="sxs-lookup"><span data-stu-id="f74ed-345">Below **Site Settings**, select **Channels**.</span></span>
1. <span data-ttu-id="f74ed-346">Valitse pääikkunassa **Kanavat**-kohdassa kanava.</span><span class="sxs-lookup"><span data-stu-id="f74ed-346">In the main window under **Channels**, select your channel.</span></span>
1. <span data-ttu-id="f74ed-347">Valitse oikeanpuoleisessa kanavan ominaisuuksien ruudussa B2C-sovelluksen nimi avattavasta **Valitse B2C-sovellus** -luettelosta.</span><span class="sxs-lookup"><span data-stu-id="f74ed-347">In the channel properties pane on the right, select your B2C application name from the **Select B2C Application** drop down menu.</span></span>
1. <span data-ttu-id="f74ed-348">Valitse **Sulje** ja valitse sitten **Tallenna ja julkaise**.</span><span class="sxs-lookup"><span data-stu-id="f74ed-348">Select **Close**, and then select **Save and Publish**.</span></span>

## <a name="additional-b2c-information"></a><span data-ttu-id="f74ed-349">B2C-lisätiedot</span><span class="sxs-lookup"><span data-stu-id="f74ed-349">Additional B2C information</span></span>

### <a name="customer-migration"></a><span data-ttu-id="f74ed-350">Asiakkaan siirtäminen</span><span class="sxs-lookup"><span data-stu-id="f74ed-350">Customer migration</span></span>

<span data-ttu-id="f74ed-351">Jos harkitset asiakastietojen siirtämistä aiemmasta tunnistetietojen tarjoajan ympäristöstä, tarkista asiakkaan siirron tarpeet Dynamics 365 Commerce -ryhmän kanssa.</span><span class="sxs-lookup"><span data-stu-id="f74ed-351">If you are considering migrating customer records from a previous identity provider platform, please work with the Dynamics 365 Commerce team to review your customer migration needs.</span></span>

<span data-ttu-id="f74ed-352">Lisätietoja asiakkaan siirron Azure AD B2C -dokumentaatiosta on kohdassa [Käyttäjien siirtäminen Azure Active Directory B2C -sovellukseen](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-user-migration).</span><span class="sxs-lookup"><span data-stu-id="f74ed-352">For additional Azure AD B2C documentation on customer migration, see [Migrate users to Azure Active Directory B2C](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-user-migration).</span></span>

### <a name="custom-policies"></a><span data-ttu-id="f74ed-353">Mukautetut käytännöt</span><span class="sxs-lookup"><span data-stu-id="f74ed-353">Custom policies</span></span>

<span data-ttu-id="f74ed-354">Lisätietoja Azure AD B2C -sovelluksen yhteydenottojen ja käytännön työnkulkujen mukauttamisesta erilaisiksi kuin B2C-standardikäytännöt on kohdassa [Azure Active Directory B2C -sovelluksen mukautetut käytännöt](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-overview-custom).</span><span class="sxs-lookup"><span data-stu-id="f74ed-354">For additional information regarding customizing Azure AD B2C interactions and policy flows beyond what is offered by B2C standard policies, see [Custom policies in Azure Active Directory B2C](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-overview-custom).</span></span> 

### <a name="secondary-admin"></a><span data-ttu-id="f74ed-355">Toissijainen järjestelmänvalvoja</span><span class="sxs-lookup"><span data-stu-id="f74ed-355">Secondary admin</span></span>

<span data-ttu-id="f74ed-356">Valinnainen toissijainen järjestelmänvalvojatili voidaan lisätä B2C-vuokraajan **Käyttäjä**-osaan.</span><span class="sxs-lookup"><span data-stu-id="f74ed-356">An optional, secondary administrator account can be added in the **Users** section of your B2C tenant.</span></span> <span data-ttu-id="f74ed-357">Tämä voi olla suora tili tai yleinen tili.</span><span class="sxs-lookup"><span data-stu-id="f74ed-357">This can be a direct account or a general account.</span></span> <span data-ttu-id="f74ed-358">Jos sinun on jaettava tili ryhmän resursseille, myös yhteinen tili voidaan luoda.</span><span class="sxs-lookup"><span data-stu-id="f74ed-358">If you need to share an account across team resources, a common account can also be created.</span></span> <span data-ttu-id="f74ed-359">Azure AD B2C -sovellukseen tallennettujen tietojen luottamuksellisuuden vuoksi yrityksen turvakäytäntöjen tulee valvoa yleistä tiliä tarkasti.</span><span class="sxs-lookup"><span data-stu-id="f74ed-359">Due to the sensitivity of the data stored in Azure AD B2C, a common account should be monitored closely per your company's security practices.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f74ed-360">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="f74ed-360">Additional resources</span></span>

[<span data-ttu-id="f74ed-361">Toimialueen nimen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="f74ed-361">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="f74ed-362">Uuden sähköisen kaupankäynnin sivuston käyttöönotto</span><span class="sxs-lookup"><span data-stu-id="f74ed-362">Deploy a new e-Commerce site</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="f74ed-363">Sähköisen kaupankäynnin sivuston luominen</span><span class="sxs-lookup"><span data-stu-id="f74ed-363">Create an e-Commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="f74ed-364">Liitä verkkosivusto kanavaan</span><span class="sxs-lookup"><span data-stu-id="f74ed-364">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="f74ed-365">Robots.txt-tiedostojen hallinta</span><span class="sxs-lookup"><span data-stu-id="f74ed-365">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="f74ed-366">URL-osoitteen uudelleenohjausten lataaminen joukkona</span><span class="sxs-lookup"><span data-stu-id="f74ed-366">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="f74ed-367">Mukautettujen sivujen määrittäminen käyttäjän kirjautumisia varten</span><span class="sxs-lookup"><span data-stu-id="f74ed-367">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="f74ed-368">Useiden B2C-vuokraajien määrittäminen Commerce-ympäristössä</span><span class="sxs-lookup"><span data-stu-id="f74ed-368">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="f74ed-369">Sisältöverkon (CDN) tuen lisääminen</span><span class="sxs-lookup"><span data-stu-id="f74ed-369">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="f74ed-370">Sijaintiin perustuvan myymälän tunnistuksen käyttöönotto</span><span class="sxs-lookup"><span data-stu-id="f74ed-370">Enable location-based store detection</span></span>](enable-store-detection.md)
