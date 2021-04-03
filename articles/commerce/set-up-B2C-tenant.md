---
title: B2C-vuokraajan määrittäminen Commercessa
description: Tässä ohjeaiheessa kerrotaan, miten Azure Active Directoryn (Azure AD) kuluttajakaupan (B2C) vuokraajat määritetään Dynamics 365 Commercen käyttäjän sivuston todennusta varten.
author: BrianShook
manager: annbe
ms.date: 06/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: brshoo
ms.search.validFrom: 2020-02-13
ms.dyn365.ops.version: ''
ms.openlocfilehash: 4ee667bb49e70e0c881a2db1248b3f0c7fc017ce
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/19/2021
ms.locfileid: "5478137"
---
# <a name="set-up-a-b2c-tenant-in-commerce"></a><span data-ttu-id="fcb79-103">B2C-vuokraajan määrittäminen Commercessa</span><span class="sxs-lookup"><span data-stu-id="fcb79-103">Set up a B2C tenant in Commerce</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="fcb79-104">Tässä ohjeaiheessa kerrotaan, miten Azure Active Directoryn (Azure AD) kuluttajakaupan (B2C) vuokraajat määritetään Dynamics 365 Commercen käyttäjän sivuston todennusta varten.</span><span class="sxs-lookup"><span data-stu-id="fcb79-104">This topic describes how to set up your Azure Active Directory (Azure AD) business-to-consumer (B2C) tenants for user site authentication in Dynamics 365 Commerce.</span></span>

<span data-ttu-id="fcb79-105">Dynamics 365 Commerce käyttää Azure AD B2C -ratkaisua käyttäjän tunnistetietojen ja todennuksen työnkulkujen tukemisessa.</span><span class="sxs-lookup"><span data-stu-id="fcb79-105">Dynamics 365 Commerce uses Azure AD B2C to support user credential and authentication flows.</span></span> <span data-ttu-id="fcb79-106">Käyttäjä voi rekisteröityä, kirjautua sisään ja nollata salasanan näiden työnkulkujen avulla.</span><span class="sxs-lookup"><span data-stu-id="fcb79-106">A user can sign up, sign in, and reset their password through these flows.</span></span> <span data-ttu-id="fcb79-107">Azure AD B2C tallentaa luottamukselliset käyttäjän todennustiedot, kuten käyttäjätunnuksen ja salasanan.</span><span class="sxs-lookup"><span data-stu-id="fcb79-107">Azure AD B2C stores sensitive user authentication information, such as username and password.</span></span> <span data-ttu-id="fcb79-108">B2C-vuokraajan käyttäjätietueeseen tallennetaan B2C:n paikallisen tilin tietue tai B2C:n yhteisöpalvelun tunnuksen tarjoajan tietue.</span><span class="sxs-lookup"><span data-stu-id="fcb79-108">The user record in the B2C tenant will store either a B2C local account record or a B2C social identity provider record.</span></span> <span data-ttu-id="fcb79-109">Nämä B2C-tietueet linkitetään takaisin asiakastietueeseen Commerce-ympäristössä.</span><span class="sxs-lookup"><span data-stu-id="fcb79-109">These B2C records will link back to the customer record in the Commerce environment.</span></span>

## <a name="create-or-link-to-an-existing-aad-b2c-tenant-in-the-azure-portal"></a><span data-ttu-id="fcb79-110">Olemassa olevan AAD B2C -vuokraajan luominen tai linkittäminen Azure-portaalissa</span><span class="sxs-lookup"><span data-stu-id="fcb79-110">Create or link to an existing AAD B2C tenant in the Azure portal</span></span>

1. <span data-ttu-id="fcb79-111">Kirjaudu [Azure-portaalin osoitteessa](https://portal.azure.com/).</span><span class="sxs-lookup"><span data-stu-id="fcb79-111">Sign in to the [Azure portal](https://portal.azure.com/).</span></span>
1. <span data-ttu-id="fcb79-112">Valitse Azure-portaalin valikossa **Luo resurssi**.</span><span class="sxs-lookup"><span data-stu-id="fcb79-112">From the Azure portal menu, select **Create a resource**.</span></span> <span data-ttu-id="fcb79-113">Varmista,. että käytät tilausta ja hakemistoa, joka yhdistetään Commerce-ympäristöön.</span><span class="sxs-lookup"><span data-stu-id="fcb79-113">Be sure to use the subscription and directory that will be connected with your Commerce environment.</span></span>

    ![Resurssin luominen Azure-portaaliin](./media/B2CImage_1.png)

1. <span data-ttu-id="fcb79-115">Siirry kohtaan **Tunnistetiedot \> Azure Active Directory B2C**.</span><span class="sxs-lookup"><span data-stu-id="fcb79-115">Go to **Identity \> Azure Active Directory B2C**.</span></span>
1. <span data-ttu-id="fcb79-116">Käytä **Uuden B2C-vuokraajan luominen tai linkittäminen olemassa olevaan vuokraajaan** -sivulla seuraavista vaihtoehdoista sitä, joka sopii yrityksen tarpeisiin parhaiten:</span><span class="sxs-lookup"><span data-stu-id="fcb79-116">Once on the **Create New B2C Tenant or Link to existing Tenant** page, use one of the options below that best suits your company's needs:</span></span>

    - <span data-ttu-id="fcb79-117">**Luo uusi Azure AD B2C -vuokraaja**: Käytä tätä vaihtoehtoa, jos haluat luoda uuden AAD B2C -vuokraajan.</span><span class="sxs-lookup"><span data-stu-id="fcb79-117">**Create a new Azure AD B2C Tenant**: Use this option to create a new AAD B2C tenant.</span></span>
        1. <span data-ttu-id="fcb79-118">Valitse **Luo uusi Azure AD B2C -vuokraaja**.</span><span class="sxs-lookup"><span data-stu-id="fcb79-118">Select **Create a new Azure AD B2C Tenant**.</span></span>
        1. <span data-ttu-id="fcb79-119">Määritä **Organisaation nimi** -kohdassa organisaation nimi.</span><span class="sxs-lookup"><span data-stu-id="fcb79-119">Under **Organization name**, enter the organization name.</span></span>
        1. <span data-ttu-id="fcb79-120">Anna **Alkuperäinen toimialueen nimi** -kohdassa alkuperäinen toimialueen nimi.</span><span class="sxs-lookup"><span data-stu-id="fcb79-120">Under **Initial domain name**, enter the initial domain name.</span></span>
        1. <span data-ttu-id="fcb79-121">Valitse **Maa tai alue** -kohdassa maa tai alue.</span><span class="sxs-lookup"><span data-stu-id="fcb79-121">For **Country or region**, select the country or region.</span></span>
        1. <span data-ttu-id="fcb79-122">Valitse **Luo**, jos haluat luoda vuokraajan.</span><span class="sxs-lookup"><span data-stu-id="fcb79-122">Select **Create** to create the tenant.</span></span>

     ![Uuden Azure AD -vuokraajan luominen](./media/B2CImage_2.png)

     - <span data-ttu-id="fcb79-124">**Linkitä olemassa oleva Azure AD B2C -vuokraaja omaan Azure-tilaukseen**: Käytä tätä vaihtoehtoa, jos sinulla on jo Azure AD B2C -vuokraaja, johon haluat linkittää.</span><span class="sxs-lookup"><span data-stu-id="fcb79-124">**Link an existing Azure AD B2C Tenant to my Azure subscription**: Use this option if you already have an Azure AD B2C tenant you want to link to.</span></span>
        1. <span data-ttu-id="fcb79-125">Valitse **Linkitä olemassa oleva Azure AD B2C -vuokraaja Azure-tilaukseen**.</span><span class="sxs-lookup"><span data-stu-id="fcb79-125">Select **Link an existing Azure AD B2C Tenant to my Azure subscription**.</span></span>
        1. <span data-ttu-id="fcb79-126">Valitse **Azure AD B2C -vuokraaja** -kohdassa soveltuva B2C-vuokraaja.</span><span class="sxs-lookup"><span data-stu-id="fcb79-126">For **Azure AD B2C Tenant**, select the appropriate B2C tenant.</span></span> <span data-ttu-id="fcb79-127">Jos valintaikkunaan tulee Kelvollisia B2C-vuokraajia ei löytynyt -sanoma, sinulla ei ole olemassa olevaa B2C-vuokraajaa, vaan se on luotava.</span><span class="sxs-lookup"><span data-stu-id="fcb79-127">If the message "No eligible B2C Tenants found" appears in the selection box, you do not have an existing eligible B2C tenant and will need to create a new one.</span></span>
        1. <span data-ttu-id="fcb79-128">Valitse **Resurssiryhmä**-kohdassa **Luo uusi**.</span><span class="sxs-lookup"><span data-stu-id="fcb79-128">For **Resource group**, select **Create new**.</span></span> <span data-ttu-id="fcb79-129">Anna **nimi** resurssiryhmälle, joka sisältää vuokraajan ja valitse **Resurssiryhmän sijainti**. Valitse lopuksi **Luo**.</span><span class="sxs-lookup"><span data-stu-id="fcb79-129">Enter a **Name** for the resource group that will contain the tenant, select the **Resource group location**, and then select **Create**.</span></span>

    ![Linkitä olemassa oleva Azure AD B2C -vuokraaja Azure-tilaukseen](./media/B2CImage_3.png)

1. <span data-ttu-id="fcb79-131">Kun uusi Azure AD B2C -hakemisto on luotu (tämä voi kestää jonkin aikaa), koontinäyttöön tulee näkyviin uuden hakemiston linkki.</span><span class="sxs-lookup"><span data-stu-id="fcb79-131">Once the new Azure AD B2C directory is created (this may take a few moments), a link to the new directory will appear on the dashboard.</span></span> <span data-ttu-id="fcb79-132">Tämä linkki ohjaa sinut Tervetuloa Azure Active Directory B2C -ratkaisun käyttäjäksi -sivulle.</span><span class="sxs-lookup"><span data-stu-id="fcb79-132">This link will direct you to the "Welcome to Azure Active Directory B2C" page.</span></span>

    ![Linkki uuteen AAD-hakemistoon](./media/B2CImage_4.png)

> [!NOTE]
> <span data-ttu-id="fcb79-134">Jos sinulla on useita Azure-tilin tilauksia tai jos olet määrittänyt B2C-vuokraajan ilman aktiivisen tilauksen linkkiä, **Vianmääritys**-banneri ohjaa sinut kohtaan, jossa voit linkittää vuokraajan ja tilauksen.</span><span class="sxs-lookup"><span data-stu-id="fcb79-134">If you have multiple subscriptions within your Azure account or have set up the B2C tenant without linking to an active subscription, a **Troubleshoot** banner will direct you to link the tenant to a subscription.</span></span> <span data-ttu-id="fcb79-135">Valitse vianmäärityksen sanoma ja ratkaise tilaukseen liittyvä ongelma ohjeiden avulla.</span><span class="sxs-lookup"><span data-stu-id="fcb79-135">Select the troubleshooting message and follow the instructions to resolve the subscription issue.</span></span>

<span data-ttu-id="fcb79-136">Seuraavassa kuvassa on esimerkki Azure AD B2C:n **Vianmääritys**-bannerista.</span><span class="sxs-lookup"><span data-stu-id="fcb79-136">The following image shows an example of an Azure AD B2C **Troubleshoot** banner.</span></span>

![Varoitus siitä, että hakemistolla ei ole aktiivista tilausta](./media/B2CImage_5.png)

## <a name="create-the-b2c-application"></a><span data-ttu-id="fcb79-138">B2C-sovelluksen luominen</span><span class="sxs-lookup"><span data-stu-id="fcb79-138">Create the B2C application</span></span>

<span data-ttu-id="fcb79-139">Kun B2C-vuokraaja on luotu, voit luoda B2C-sovelluksen vuokraajassa ja käyttää Commerce-toimintoja.</span><span class="sxs-lookup"><span data-stu-id="fcb79-139">Once the B2C tenant has been created, you will create a B2C application within the tenant to interact with the Commerce actions.</span></span>

<span data-ttu-id="fcb79-140">Luo B2C-sovellus seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="fcb79-140">To create the B2C application, follow these steps.</span></span>

1. <span data-ttu-id="fcb79-141">Valitse Azure-portaalissa **Sovellukset(Vanha)** ja valitse sitten **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="fcb79-141">In the Azure portal, select **Applications(Legacy)** and then select **Add**.</span></span>
1. <span data-ttu-id="fcb79-142">Anna **Nimi**-kohtaan halutun AAD B2C -sovelluksen nimi.</span><span class="sxs-lookup"><span data-stu-id="fcb79-142">Under **Name**, enter the name of the desired AAD B2C application.</span></span>
1. <span data-ttu-id="fcb79-143">Valitse **Verkkosovellus / verkon ohjelmointirajapinta** -kohdassa **Sisällytä verkkosovellus / verkon ohjelmointirajapinta** -kohdan arvoksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="fcb79-143">Under **Web App/Web API**, for **Include web app / web API**, select **Yes**.</span></span>
1. <span data-ttu-id="fcb79-144">Valitse **Salli implisiittinen työnkulku** -kohdan arvoksi **Kyllä** (oletusarvo).</span><span class="sxs-lookup"><span data-stu-id="fcb79-144">For **Allow implicit flow**, select **Yes** (the default value).</span></span>
1. <span data-ttu-id="fcb79-145">Anna **Vastauksen URL-osoite** -kohtaan määritetyt vastauksen URL-osoitteet.</span><span class="sxs-lookup"><span data-stu-id="fcb79-145">Under **Reply URL**, enter your dedicated reply URLs.</span></span> <span data-ttu-id="fcb79-146">Katso lisätietoja vastauksen URL-osoitteista ja niiden muotoilusta [Vastauksen URL-osoitteet](#reply-urls) -kohdasta.</span><span class="sxs-lookup"><span data-stu-id="fcb79-146">See [Reply URLs](#reply-urls) below for information on reply URLs and how to format them here.</span></span>
1. <span data-ttu-id="fcb79-147">Valitse **Sisällytä alkuperäinen asiakasohjelma** -kohdassa **Ei** (oletusarvo).</span><span class="sxs-lookup"><span data-stu-id="fcb79-147">For **Include native client**, select **No** (the default value).</span></span>
1. <span data-ttu-id="fcb79-148">Valitse **Luo**.</span><span class="sxs-lookup"><span data-stu-id="fcb79-148">Select **Create**.</span></span>

### <a name="reply-urls"></a><span data-ttu-id="fcb79-149">Vastauksen URL-osoitteet</span><span class="sxs-lookup"><span data-stu-id="fcb79-149">Reply URLs</span></span>

<span data-ttu-id="fcb79-150">Vastauksen URL-osoitteet ovat tärkeitä, koska ne tarjoavat sallitut palautustoimialueet, kun sivusto kutsuu Azure AD B2C -ratkaisua käyttäjän todentamista varten.</span><span class="sxs-lookup"><span data-stu-id="fcb79-150">Reply URLs are important as they provide an allow list of the return domains when your site calls Azure AD B2C to authenticate a user.</span></span> <span data-ttu-id="fcb79-151">Toiminto sallii todennetun käyttäjän paluun takaisin toimialueelle, jolta nämä kirjautuvat (oman sivuston toimialue).</span><span class="sxs-lookup"><span data-stu-id="fcb79-151">This permits the return of the authenticated user back to the domain from which they are signing into (your site domain).</span></span> 

<span data-ttu-id="fcb79-152">Lisää **Vastauksen URL-osoite** -ruudun **Azure AD B2C - sovellukset \> Uusi sovellus** -näytössä erilliset rivit sivuston toimialueelle ja (ympäristön valmistelun jälkeen) Commercen luomalle URL-osoitteelle.</span><span class="sxs-lookup"><span data-stu-id="fcb79-152">In the **Reply URL** box on the **Azure AD B2c - Applications \> New application** screen, you need to add separate lines for both your site domain and (once your environment is provisioned) the Commerce-generated URL.</span></span> <span data-ttu-id="fcb79-153">Näissä URL-osoitteissa on aina käytettävä sallittua URL-osoitteen muotoa. Niiden on aina oltava perus-URL-osoitteita (ei lopussa olevia vinoviivoja tai polkuja).</span><span class="sxs-lookup"><span data-stu-id="fcb79-153">These URLs must always use a valid URL format and must be base URLs only (no trailing forward slashes or paths).</span></span> <span data-ttu-id="fcb79-154">Merkkijono ``/_msdyn365/authresp`` on siis liitettävä perus-URL-osoitteisiin seuraavien esimerkkien mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="fcb79-154">The string ``/_msdyn365/authresp`` then needs to be appended to the base URLs, as in the following examples.</span></span>

- <span data-ttu-id="fcb79-155">``https://www.fabrikam.com/_msdyn365/authresp`` (Toimialueen tulisi täsmätä sähköisen kaupankäynnin toimialueeseen kokonaan.</span><span class="sxs-lookup"><span data-stu-id="fcb79-155">``https://www.fabrikam.com/_msdyn365/authresp`` (The domain should match the e-commerce domain completely.</span></span> <span data-ttu-id="fcb79-156">Jos sinulla on useita toimialueita, sinun on lisättävä tämä URL-osoite kullekin toimialueelle.)</span><span class="sxs-lookup"><span data-stu-id="fcb79-156">If you have multiple domains, you need to add this URL for each domain.)</span></span>
- ``https://fabrikam-prod.commerce.dynamics.com/_msdyn365/authresp``

## <a name="create-user-flow-policies"></a><span data-ttu-id="fcb79-157">Käyttäjän työnkulkukäytäntöjen luominen</span><span class="sxs-lookup"><span data-stu-id="fcb79-157">Create user flow policies</span></span>

<span data-ttu-id="fcb79-158">Käyttäjän työnkulut ovat käytäntöjä, joita Azure AD B2C käyttää suojatun sisäänkirjauksen, rekisteröitymisen, profiilin muokkaamisen ja unohdetun salasanan käyttökokemusten määrittämisessä.</span><span class="sxs-lookup"><span data-stu-id="fcb79-158">User flows are the policies Azure AD B2C uses to provide secure sign in, sign up, edit profile, and forget password user experiences.</span></span> <span data-ttu-id="fcb79-159">Dynamics 365 Commerce suorittaa näiden työnkulkujen avulla käytäntöjen toiminnot, joiden avulla se toimii Azure AD B2C -vuokraajan kanssa.</span><span class="sxs-lookup"><span data-stu-id="fcb79-159">Dynamics 365 Commerce uses these flows to perform the policy actions to interact with the Azure AD B2C tenant.</span></span> <span data-ttu-id="fcb79-160">Kun käyttäjä käyttää näitä käytäntöjä, ne ohjataan uudelleen Azure AD B2C -vuokraajalle toimintojen suorittamista varten.</span><span class="sxs-lookup"><span data-stu-id="fcb79-160">When a user interacts with these policies, they are redirected to the Azure AD B2C tenant to perform the actions.</span></span>

<span data-ttu-id="fcb79-161">Azure AD B2C sisältää seuraavat kolme käyttäjän perustyönkulkutyyppiä:</span><span class="sxs-lookup"><span data-stu-id="fcb79-161">Azure AD B2C provides three basic user flow types:</span></span>
- <span data-ttu-id="fcb79-162">Rekisteröityminen ja sisäänkirjaus</span><span class="sxs-lookup"><span data-stu-id="fcb79-162">Sign up and sign in</span></span>
- <span data-ttu-id="fcb79-163">Profiilin muokkaaminen</span><span class="sxs-lookup"><span data-stu-id="fcb79-163">Profile editing</span></span>
- <span data-ttu-id="fcb79-164">Salasanan palauttaminen</span><span class="sxs-lookup"><span data-stu-id="fcb79-164">Password reset</span></span>

<span data-ttu-id="fcb79-165">Voit halutessasi käyttää Azure AD:n käyttäjän oletustyönkulkua. Se näyttää AAD B2C:n isännöimän sivun.</span><span class="sxs-lookup"><span data-stu-id="fcb79-165">You can choose to use the default user flows provided by Azure AD, which will display a page hosted by AAD B2C.</span></span> <span data-ttu-id="fcb79-166">Vaihtoehtoisesti voit luoda HTML-sivun, jonka avulla hallitaan näiden käyttäjän työnkulkukokemusten ulkoasua.</span><span class="sxs-lookup"><span data-stu-id="fcb79-166">Alternately, you can create an HTML page to control the look and feel of these user flow experiences.</span></span> 

<span data-ttu-id="fcb79-167">Jos haluat mukauttaa Dynamics 365 Commercen käyttäjän käytäntöjen sivuja, katso [Käyttäjän sisäänkirjausten mukautettujen sivujen määrittäminen](custom-pages-user-logins.md).</span><span class="sxs-lookup"><span data-stu-id="fcb79-167">To customize the user policy pages for Dynamics 365 Commerce, see [Set up custom pages for user logins](custom-pages-user-logins.md).</span></span> <span data-ttu-id="fcb79-168">Lisätietoja on kohdassa [Azure Active Directory B2C:n käyttäjäkokemusten käyttöliittymän mukauttaminen](https://docs.microsoft.com/azure/active-directory-b2c/tutorial-customize-ui).</span><span class="sxs-lookup"><span data-stu-id="fcb79-168">For additional information, see [Customize the interface of user experiences in Azure Active Directory B2C](https://docs.microsoft.com/azure/active-directory-b2c/tutorial-customize-ui).</span></span>

### <a name="create-a-sign-up-and-sign-in-user-flow-policy"></a><span data-ttu-id="fcb79-169">Rekisteröitymisen ja sisäänkirjauksen käyttäjän työnkulkukäytännön luominen</span><span class="sxs-lookup"><span data-stu-id="fcb79-169">Create a sign up and sign in user flow policy</span></span>

<span data-ttu-id="fcb79-170">Voit luoda rekisteröitymisen ja sisäänkirjauksen käyttäjän työnkulkukäytännön seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="fcb79-170">To create a sign up and sign in user flow policy, follow these steps.</span></span>

1. <span data-ttu-id="fcb79-171">Valitse Azure-portaalin vasemmanpuoleisessa siirtymisruudussa **Käyttäjän työnkulut (käytännöt)**.</span><span class="sxs-lookup"><span data-stu-id="fcb79-171">In the Azure portal, select **User flows (policies)** in the left navigation pane.</span></span>
1. <span data-ttu-id="fcb79-172">Valitse **Azure AD B2C – käyttäjän työnkulut (käytännöt)** -sivulla **Uusi käyttäjän työnkulku**.</span><span class="sxs-lookup"><span data-stu-id="fcb79-172">On the **Azure AD B2C – User flows (policies)** page, select **New User Flow**.</span></span>
1. <span data-ttu-id="fcb79-173">Valitse **Suositellut**-välilehdessä **Rekisteröidy ja kirjaudu sisään**.</span><span class="sxs-lookup"><span data-stu-id="fcb79-173">On the **Recommended** tab, select **Sign up and sign in**.</span></span>
1. <span data-ttu-id="fcb79-174">Anna käytännön nimi **Nimi**-kohdassa.</span><span class="sxs-lookup"><span data-stu-id="fcb79-174">Under **Name**, enter a policy name.</span></span> <span data-ttu-id="fcb79-175">Tämä nimi näkyy myöhemmin portaalin määrittämän etuliitteen kanssa (esimerkiksi B2C_1_).</span><span class="sxs-lookup"><span data-stu-id="fcb79-175">This name will display afterwards with a prefix the portal assigns (for example, "B2C_1_").</span></span>
1. <span data-ttu-id="fcb79-176">Valitse **Tunnistetietojen tarjoajat** -kohdassa soveltuva valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="fcb79-176">Under **Identity providers**, select the appropriate check box.</span></span>
1. <span data-ttu-id="fcb79-177">Valitse **Usean tekijän todennus** yritykselle soveltuva vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="fcb79-177">Under **Multifactor Authentication**, select the appropriate choice for your company.</span></span> 
1. <span data-ttu-id="fcb79-178">Valitse **Käyttäjän määritteet ja vaatimukset** -kohdassa vaihtoehdot määritteiden tai palautusvaatimusten keräämistä varten.</span><span class="sxs-lookup"><span data-stu-id="fcb79-178">Under **User attributes and claims**, select options to collect attributes or return claims as appropriate.</span></span> <span data-ttu-id="fcb79-179">Commerce edellyttää seuraavien oletusasetusten käyttämistä:</span><span class="sxs-lookup"><span data-stu-id="fcb79-179">Commerce requires the following default options:</span></span>

    | <span data-ttu-id="fcb79-180">**Keräilymäärite**</span><span class="sxs-lookup"><span data-stu-id="fcb79-180">**Collect  attribute**</span></span> | <span data-ttu-id="fcb79-181">**Palautusvaatimus**</span><span class="sxs-lookup"><span data-stu-id="fcb79-181">**Return  claim**</span></span> |
    | ---------------------- | ----------------- |
    | <span data-ttu-id="fcb79-182">Sähköpostiosoite</span><span class="sxs-lookup"><span data-stu-id="fcb79-182">Email Address</span></span>          | <span data-ttu-id="fcb79-183">Sähköpostiosoitteet</span><span class="sxs-lookup"><span data-stu-id="fcb79-183">Email Addresses</span></span>   |
    | <span data-ttu-id="fcb79-184">Etunimi</span><span class="sxs-lookup"><span data-stu-id="fcb79-184">Given Name</span></span>             | <span data-ttu-id="fcb79-185">Etunimi</span><span class="sxs-lookup"><span data-stu-id="fcb79-185">Given Name</span></span>        |
    |                        | <span data-ttu-id="fcb79-186">Tunnistetietojen toimittaja</span><span class="sxs-lookup"><span data-stu-id="fcb79-186">Identity Provider</span></span> |
    | <span data-ttu-id="fcb79-187">Sukunimi</span><span class="sxs-lookup"><span data-stu-id="fcb79-187">Surname</span></span>                | <span data-ttu-id="fcb79-188">Sukunimi</span><span class="sxs-lookup"><span data-stu-id="fcb79-188">Surname</span></span>           |
    |                        | <span data-ttu-id="fcb79-189">Käyttäjän objektin tunnus</span><span class="sxs-lookup"><span data-stu-id="fcb79-189">User’s Object ID</span></span>  |

1. <span data-ttu-id="fcb79-190">Valitse **Luo**.</span><span class="sxs-lookup"><span data-stu-id="fcb79-190">Select **Create**.</span></span>

<span data-ttu-id="fcb79-191">Seuraavassa kuvassa on esimerkki Azure AD B2C:n rekisteröitymisen ja sisäänkirjauksen käyttäjän työnkulusta.</span><span class="sxs-lookup"><span data-stu-id="fcb79-191">The following image is an example of the Azure AD B2C sign up and sign in user flow.</span></span>

![Rekisteröinti ja sisäänkirjaus -käytännön asetukset](./media/B2CImage_11.png)

<span data-ttu-id="fcb79-193">Seuraavassa kuvassa on **Suorita käyttäjän työnkulku** -vaihtoehto Azure AD B2C:n rekisteröitymisen ja sisäänkirjauksen käyttäjän työnkulussa.</span><span class="sxs-lookup"><span data-stu-id="fcb79-193">The following image shows the **Run user flow** option in the Azure AD B2C sign up and sign in user flow.</span></span>

![Käyttäjän työnkulku -vaihtoehdon suorittaminen käytännön työnkulussa](./media/B2CImage_23.png)
   
### <a name="create-a-profile-editing-user-flow-policy"></a><span data-ttu-id="fcb79-195">Profiilin muokkaamisen käyttäjän työnkulkukäytännön luominen</span><span class="sxs-lookup"><span data-stu-id="fcb79-195">Create a profile editing user flow policy</span></span>

<span data-ttu-id="fcb79-196">Voit luoda profiilin muokkaamisen käyttäjän työnkulkukäytännön seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="fcb79-196">To create a profile editing user flow policy, follow these steps.</span></span>

1. <span data-ttu-id="fcb79-197">Valitse Azure-portaalin vasemmanpuoleisessa siirtymisruudussa **Käyttäjän työnkulut (käytännöt)**.</span><span class="sxs-lookup"><span data-stu-id="fcb79-197">In the Azure portal, select **User flows (policies)** in the left navigation pane.</span></span>
1. <span data-ttu-id="fcb79-198">Valitse **Azure AD B2C – käyttäjän työnkulut (käytännöt)** -sivulla **Uusi käyttäjän työnkulku**.</span><span class="sxs-lookup"><span data-stu-id="fcb79-198">On the **Azure AD B2C – User flows (policies)** page, select **New User Flow**.</span></span>
1. <span data-ttu-id="fcb79-199">Valitse **Suositellut**-välilehdessä **Profiilin muokkaaminen**.</span><span class="sxs-lookup"><span data-stu-id="fcb79-199">On the **Recommended** tab, select **Profile editing**.</span></span>
1. <span data-ttu-id="fcb79-200">Anna **Nimi**-kohtaan profiilin muokkaamisen käyttäjän työnkulku.</span><span class="sxs-lookup"><span data-stu-id="fcb79-200">Under **Name**, enter the profile editing user flow.</span></span> <span data-ttu-id="fcb79-201">Tämä nimi näkyy myöhemmin portaalin määrittämän etuliitteen kanssa (esimerkiksi B2C_1_).</span><span class="sxs-lookup"><span data-stu-id="fcb79-201">This name will display afterwards with a prefix the portal assigns (for example, "B2C_1_").</span></span>
1. <span data-ttu-id="fcb79-202">Valitse **Tunnistetietojen tarjoajat** -kohdassa **Paikallisen tilin sisäänkirjaus**.</span><span class="sxs-lookup"><span data-stu-id="fcb79-202">Under **Identity providers**, select **Local Account SignIn**.</span></span>
1. <span data-ttu-id="fcb79-203">Valitse **Käyttäjän määritteet** -kohdassa seuraavat valintaruudut:</span><span class="sxs-lookup"><span data-stu-id="fcb79-203">Under **User attributes**, select the following check boxes:</span></span>
    - <span data-ttu-id="fcb79-204">**Sähköpostiosoitteet** (vain **Palautusvaatimus**)</span><span class="sxs-lookup"><span data-stu-id="fcb79-204">**Email Addresses** (**Return claim** only)</span></span>
    - <span data-ttu-id="fcb79-205">**Etunimi** (**Keräilymäärite** ja **Palautusvaatimus**)</span><span class="sxs-lookup"><span data-stu-id="fcb79-205">**Given Name** (**Collect attribute** and **Return claim**)</span></span>
    - <span data-ttu-id="fcb79-206">**Tunnistetietojen tarjoaja** (vain **Palautusvaatimus**)</span><span class="sxs-lookup"><span data-stu-id="fcb79-206">**Identity Provider** (**Return claim** only)</span></span>
    - <span data-ttu-id="fcb79-207">**Sukunimi** (**Keräilymäärite** ja **Palautusvaatimus**)</span><span class="sxs-lookup"><span data-stu-id="fcb79-207">**Surname** (**Collect attribute** and **Return claim**)</span></span>
    - <span data-ttu-id="fcb79-208">**Käyttäjän objektin tunnus** (vain **Palautusvaatimus**)</span><span class="sxs-lookup"><span data-stu-id="fcb79-208">**User's Object ID** (**Return claim** only)</span></span>
1. <span data-ttu-id="fcb79-209">Valitse **Luo**.</span><span class="sxs-lookup"><span data-stu-id="fcb79-209">Select **Create**.</span></span>

<span data-ttu-id="fcb79-210">Seuraavassa kuvassa on esimerkki Azure AD B2C:n profiilin muokkauksen käyttäjän työnkulusta.</span><span class="sxs-lookup"><span data-stu-id="fcb79-210">The following image shows an example of the Azure AD B2C profile editing user flow.</span></span>

![Profiilin muokkaamisen käyttäjän työnkulun luominen](./media/B2CImage_12.png)

### <a name="create-a-password-reset-user-flow-policy"></a><span data-ttu-id="fcb79-212">Salasanan palauttamisen käyttäjän työnkulkukäytännön luominen</span><span class="sxs-lookup"><span data-stu-id="fcb79-212">Create a password reset user flow policy</span></span>

<span data-ttu-id="fcb79-213">Voit luoda salasanan palauttamisen käyttäjän työnkulkukäytännön seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="fcb79-213">To create a password reset user flow policy, follow these steps.</span></span>

1. <span data-ttu-id="fcb79-214">Valitse Azure-portaalin vasemmanpuoleisessa siirtymisruudussa **Käyttäjän työnkulut (käytännöt)**.</span><span class="sxs-lookup"><span data-stu-id="fcb79-214">In the Azure portal, select **User flows (policies)** in the left navigation pane.</span></span>
1. <span data-ttu-id="fcb79-215">Valitse **Azure AD B2C – käyttäjän työnkulut (käytännöt)** -sivulla **Uusi käyttäjän työnkulku**.</span><span class="sxs-lookup"><span data-stu-id="fcb79-215">On the **Azure AD B2C – User flows (policies)** page, select **New User Flow**.</span></span>
1. <span data-ttu-id="fcb79-216">Valitse **Suositellut**-välilehdessä **Salasanan palauttaminen**.</span><span class="sxs-lookup"><span data-stu-id="fcb79-216">On the **Recommended** tab, select **Password Reset**.</span></span>
1. <span data-ttu-id="fcb79-217">Anna **Nimi**-kohtaan salasanan palauttamisen käyttäjän työnkulun nimi.</span><span class="sxs-lookup"><span data-stu-id="fcb79-217">Under **Name**, enter a name for the password reset user flow.</span></span>
1. <span data-ttu-id="fcb79-218">Valitse **Tunnistetietojen tarjoajat** -kohdassa **Nollaa salasana sähköpostiosoitteen avulla**.</span><span class="sxs-lookup"><span data-stu-id="fcb79-218">Under **Identity providers**, select **Reset password using email address**.</span></span>
1. <span data-ttu-id="fcb79-219">Valitse **Luo**.</span><span class="sxs-lookup"><span data-stu-id="fcb79-219">Select **Create**.</span></span>
1. <span data-ttu-id="fcb79-220">Valitse **Sovelluksen vaatimukset** -kohdassa seuraavat valintaruudut:</span><span class="sxs-lookup"><span data-stu-id="fcb79-220">Under **Application claims**, select the following check boxes:</span></span>
    - <span data-ttu-id="fcb79-221">**Sähköpostiosoitteet**</span><span class="sxs-lookup"><span data-stu-id="fcb79-221">**Email addresses**</span></span>
    - <span data-ttu-id="fcb79-222">**Etunimi**</span><span class="sxs-lookup"><span data-stu-id="fcb79-222">**Given Name**</span></span>
    - <span data-ttu-id="fcb79-223">**Sukunimi**</span><span class="sxs-lookup"><span data-stu-id="fcb79-223">**Surname**</span></span>
    - <span data-ttu-id="fcb79-224">**Käyttäjän objektin tunnus**</span><span class="sxs-lookup"><span data-stu-id="fcb79-224">**User's Object ID**</span></span>
1. <span data-ttu-id="fcb79-225">Valitse **Luo**.</span><span class="sxs-lookup"><span data-stu-id="fcb79-225">Select **Create**.</span></span>

<span data-ttu-id="fcb79-226">Seuraavassa kuvassa näytetään, miten **Palauta salasana sähköpostiosoitteen avulla** määritetään Azure AD B2C:n salasanan palauttamisen käyttäjän työnkulussa.</span><span class="sxs-lookup"><span data-stu-id="fcb79-226">The following image shows where to set **Reset Password using mail address** in the Azure AD B2C password reset user flow.</span></span>

![Salasanan palauttamisen käytännön Palauta salasana sähköpostiosoitteen avulla -kohdan määrittäminen](./media/B2CImage_13.png)

## <a name="add-social-identity-providers-optional"></a><span data-ttu-id="fcb79-228">Yhteisöpalvelun tunnistetietojen tarjoajien lisääminen (valinnainen)</span><span class="sxs-lookup"><span data-stu-id="fcb79-228">Add social identity providers (Optional)</span></span>

<span data-ttu-id="fcb79-229">Yhteisöpalvelun tunnistetietojen tarjoajat sallivat käyttäjien käyttää yhteisöpalvelun tilejä todennuksessa.</span><span class="sxs-lookup"><span data-stu-id="fcb79-229">Social identity providers allow users to use their social accounts for authentication.</span></span> <span data-ttu-id="fcb79-230">Yhteisöpalvelun tunnistepalvelun tarjoajan todentamisen lisääminen on valinnaista Dynamics 365 Commercessa.</span><span class="sxs-lookup"><span data-stu-id="fcb79-230">Adding social identity provider authentication is optional in Dynamics 365 Commerce.</span></span> 

<span data-ttu-id="fcb79-231">Jos yhteisöpalvelun tunnistetietojen tarjoajan todentamista ei lisätä, Azure AD B2C:n oletusprofiilit ovat käyttäjäkunnan pääprofiilit.</span><span class="sxs-lookup"><span data-stu-id="fcb79-231">If social identity provider authentication is not added, the default Azure AD B2C profiles will be the main profiles for your user base.</span></span> <span data-ttu-id="fcb79-232">Käyttäjät valitsevat oman käyttäjätunnuksen (haluamansa sähköpostiosoite) ja määrittävät salasanan.</span><span class="sxs-lookup"><span data-stu-id="fcb79-232">Users will select their own username (their preferred email address) and set a password.</span></span> <span data-ttu-id="fcb79-233">Azure AD B2C todentaa käyttäjät suoraan.</span><span class="sxs-lookup"><span data-stu-id="fcb79-233">Azure AD B2C will authenticate users directly.</span></span> 

<span data-ttu-id="fcb79-234">Jos yhteisöpalveluiden tunnustietojen tarjoajan todentaminen lisätään ja käyttäjä valitsee jonkin tarjotuista yhteisöpalveluiden tunnistetietojen tarjoajista, Azure AD B2C -vuokraajaan luodaan yhä yksikkö.</span><span class="sxs-lookup"><span data-stu-id="fcb79-234">If social identity provider authentication is added and a user chooses one of the social identity providers offered, an entity is still created in the Azure AD B2C tenant.</span></span> <span data-ttu-id="fcb79-235">Azure AD B2C todentaa tämän jälkeen käyttäjän valtuustiedot yhteisöpalvelujen tunnistetietojen tarjoajan avulla.</span><span class="sxs-lookup"><span data-stu-id="fcb79-235">Azure AD B2C will then authenticate the user's credentials with the social identity provider.</span></span>

> [!NOTE]
> <span data-ttu-id="fcb79-236">Tunnistetietojen tarjoajan sisäänkirjaus luo tietueen B2C-vuokraajaan. Se tehdään kuitenkin eri muodossa kuin paikalliset tilit, koska se kutsuu ulkoisen yhteisöpalvelujen tunnistetietojen tarjoajan viitteen todennusta varten.</span><span class="sxs-lookup"><span data-stu-id="fcb79-236">The identity provider sign in creates a record in the B2C tenant, but in a different format than local accounts since it will call the external social identity provider reference for authentication.</span></span> <span data-ttu-id="fcb79-237">Käyttäjä voi käyttää samaa sähköpostiosoitetta eri yhteisöpalvelujen tunnistetietojen tarjoajien kanssa. Tämä tarkoittaa sitä, että vuokraajan tunnistuksen käyttäjätunnuksena käyttämä sähköpostiosoite ei ehkä ole yksilöllinen.</span><span class="sxs-lookup"><span data-stu-id="fcb79-237">The user can use the same email address across social identity providers, meaning that the email username used for authentication may not be unique to the tenant.</span></span> <span data-ttu-id="fcb79-238">Azure AD B2C edellyttää vain, että käyttäjillä on yksilöllinen sähköpostiosoite paikallisilla B2C-tileillä.</span><span class="sxs-lookup"><span data-stu-id="fcb79-238">Azure AD B2C will only enforce that users have a unique email address on local B2C accounts.</span></span>

<span data-ttu-id="fcb79-239">Ennen kuin lisäät yhteisöpalvelujen tunnistetietojen tarjoajan todennusta varten, siirry tunnistetietojen tarjoajan portaaliin ja määritä tunnistetietojen tarjoajan sovellus Azure AD B2C -dokumentaatiossa määritetyllä tavalla.</span><span class="sxs-lookup"><span data-stu-id="fcb79-239">Before you can add a social identity provider for authentication, you must go to the identity provider's portal and set up an identity provider application as instructed in the Azure AD B2C documentation.</span></span> <span data-ttu-id="fcb79-240">Alla on luettelo dokumentaation linkeistä.</span><span class="sxs-lookup"><span data-stu-id="fcb79-240">A list of links to the documentation is provided below.</span></span>

- [<span data-ttu-id="fcb79-241">Amazon</span><span class="sxs-lookup"><span data-stu-id="fcb79-241">Amazon</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-amzn-app)
- [<span data-ttu-id="fcb79-242">Azure AD (yksi vuokraaja)</span><span class="sxs-lookup"><span data-stu-id="fcb79-242">Azure AD (Single Tenant)</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-oidc-azure-active-directory)
- [<span data-ttu-id="fcb79-243">Microsoft-tili</span><span class="sxs-lookup"><span data-stu-id="fcb79-243">Microsoft Account</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-msa-app)
- [<span data-ttu-id="fcb79-244">Facebook</span><span class="sxs-lookup"><span data-stu-id="fcb79-244">Facebook</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-fb-app)
- [<span data-ttu-id="fcb79-245">GitHub</span><span class="sxs-lookup"><span data-stu-id="fcb79-245">GitHub</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-github-app)
- [<span data-ttu-id="fcb79-246">Google</span><span class="sxs-lookup"><span data-stu-id="fcb79-246">Google</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-goog-app)
- [<span data-ttu-id="fcb79-247">LinkedIn</span><span class="sxs-lookup"><span data-stu-id="fcb79-247">LinkedIn</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-li-app)
- [<span data-ttu-id="fcb79-248">OpenID Connect</span><span class="sxs-lookup"><span data-stu-id="fcb79-248">OpenID Connect</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-oidc-idp)
- [<span data-ttu-id="fcb79-249">Twitter</span><span class="sxs-lookup"><span data-stu-id="fcb79-249">Twitter</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-twitter-app)

### <a name="add-and-set-up-a-social-identity-provider"></a><span data-ttu-id="fcb79-250">Yhteisöpalvelujen tunnistetietojen tarjoajan lisääminen ja määrittäminen</span><span class="sxs-lookup"><span data-stu-id="fcb79-250">Add and set up a social identity provider</span></span>

<span data-ttu-id="fcb79-251">Voit lisätä ja määrittää yhteisöpalveluiden tunnistetietojen tarjoajan seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="fcb79-251">To add and set up a social identity provider, follow these steps.</span></span>  

1. <span data-ttu-id="fcb79-252">Siirry Azure-portaalissa kohtaan **Tunnistetietojen tarjoajat**.</span><span class="sxs-lookup"><span data-stu-id="fcb79-252">In the Azure portal, navigate to **Identity Providers**.</span></span>
1. <span data-ttu-id="fcb79-253">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="fcb79-253">Select **Add**.</span></span> <span data-ttu-id="fcb79-254">Näkyviin tulee **Lisää tunnistetietojen tarjoaja** -näyttö.</span><span class="sxs-lookup"><span data-stu-id="fcb79-254">The **Add identity provider** screen appears.</span></span>
1. <span data-ttu-id="fcb79-255">Anna **Nimi**-kohtaan käyttäjille sisäänkirjausnäytössä näytettävä nimi.</span><span class="sxs-lookup"><span data-stu-id="fcb79-255">Under **Name**, enter the name to be displayed to users on your sign in screen.</span></span>
1. <span data-ttu-id="fcb79-256">Valitse **Tunnistetietojen tarjoajan tyyppi** -kohtaan luettelosta tunnistetietojen tarjoaja.</span><span class="sxs-lookup"><span data-stu-id="fcb79-256">Under **Identity provider type**, select an identity provider from the list.</span></span>
1. <span data-ttu-id="fcb79-257">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="fcb79-257">Select **OK**.</span></span>
1. <span data-ttu-id="fcb79-258">Valitse **Määritä tämä tunnistetietojen tarjoaja**, jos haluat ottaa käyttöön **Määritä yhteisöpalvelujen tunnistetietojen tarjoaja** -näytön.</span><span class="sxs-lookup"><span data-stu-id="fcb79-258">Select **Set up this identity provider** to access the **Set up the social identity provider** screen.</span></span>
1. <span data-ttu-id="fcb79-259">Anna **Asiakasohjelman tunnus** -kohdassa tunnistetietojen tarjoajan sovelluksen asetuksista saatu asiakasohjelman tunnus.</span><span class="sxs-lookup"><span data-stu-id="fcb79-259">Under **Client ID**, enter the client ID as obtained from the identity provider application setup.</span></span>
1. <span data-ttu-id="fcb79-260">Anna **Asiakasohjelman salasana** -kohdassa tunnistetietojen tarjoajan sovelluksen asetuksista saatu asiakasohjelman salasana.</span><span class="sxs-lookup"><span data-stu-id="fcb79-260">Under **Client secret**, enter the client secret as obtained from the identity provider application setup.</span></span>
1. <span data-ttu-id="fcb79-261">Liitä käyttäjän työnkulku rekisteröitymis ja sisäänkirjauskäytäntöihin seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="fcb79-261">Attach user flow for sign in sign up policies:</span></span>
1. <span data-ttu-id="fcb79-262">Siirry kohtaan **Azure AD B2C – käyttäjän työnkulut (käytännöt) \> {oma sisäänkirjaus- ja rekisteröitymiskäytäntö} \> Tunnistetietojen tarjoajat**.</span><span class="sxs-lookup"><span data-stu-id="fcb79-262">Go to **Azure AD B2C – User flows (policies) \> {your sign-in sign-up policy} \> Identity providers**.</span></span>
1. <span data-ttu-id="fcb79-263">Voit liittää sisäänkirjauksen/rekisteröitymisen käyttäjän työnkulun käytännön valitsemalla kunkin tunnistetietojen tarjoajan, jonka olet määrittänyt tiliä varten.</span><span class="sxs-lookup"><span data-stu-id="fcb79-263">To attach the sign in/sign up user flow policy, select each identity provider you have set up for your account.</span></span> <span data-ttu-id="fcb79-264">Jos haluat testata nämä, valitse **Suorita käyttäjän työnkulku** jokaisen tunnistetietojen tarjoajan kohdalla.</span><span class="sxs-lookup"><span data-stu-id="fcb79-264">To test these, select **Run user flow** for each identity provider.</span></span> <span data-ttu-id="fcb79-265">Uudessa välilehdessä näkyy kirjautumissivu, joka sisältää uuden tunnistetietojen tarjoajan valintaruudun.</span><span class="sxs-lookup"><span data-stu-id="fcb79-265">A new tab will display the sign-in page displaying the new identity provider selection box.</span></span>

<span data-ttu-id="fcb79-266">Seuraavassa kuvassa on esimerkki **Lisää tunnistetietojen tarjoaja**- ja **Määritä yhteisöpalvelujen tunnistetietojen tarjoaja** -näytöistä Azure AD B2C:ssä.</span><span class="sxs-lookup"><span data-stu-id="fcb79-266">The following image shows examples of the **Add identity provider** and **Set up the social identity provider** screens in Azure AD B2C.</span></span>

![Yhteisöpalvelujen tunnistetietojen tarjoajan lisääminen sovellukseen](./media/B2CImage_14.png)

<span data-ttu-id="fcb79-268">Seuraavassa kuvassa on esimerkki siitä, miten tunnistetietojen tarjoajat valitaan Azure AD B2C:n **Tunnistetietojen tarjoaja** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="fcb79-268">The following image shows an example of how to select identity providers on the Azure AD B2C **Identity Providers** page.</span></span>

![Valitse käytäntöä varten kaikki yhteisöpalvelujen tunnistetietojen tarjoajat, jotka otetaan käyttöön](./media/B2CImage_16.png)

<span data-ttu-id="fcb79-270">Seuraavassa kuvassa on esimerkki oletussisäänkirjausnäytöstä, jossa näkyy yhteisöpalveluiden tunnistetietojen tarjoajan sisäänkirjauspainike.</span><span class="sxs-lookup"><span data-stu-id="fcb79-270">The following image shows an example of a default sign-in screen with a social identity provider sign-in button displayed.</span></span>

![Esimerkki oletussisäänkirjausnäytöstä, jossa näkyy yhteisöpalveluiden tunnistetietojen tarjoajan sisäänkirjauspainike](./media/B2CImage_17.png)

## <a name="update-commerce-headquarters-with-the-new-azure-ad-b2c-information"></a><span data-ttu-id="fcb79-272">Commerce-pääkonttorin päivittäminen uusilla Azure AD B2C -tiedoilla</span><span class="sxs-lookup"><span data-stu-id="fcb79-272">Update Commerce headquarters with the new Azure AD B2C information</span></span>

<span data-ttu-id="fcb79-273">Kun Azure AD B2C:n yllä mainitut valmisteluvaiheet on tehty, Azure AD B2C -sovellus on rekisteröitävä Dynamics 365 Commerce -ympäristöön.</span><span class="sxs-lookup"><span data-stu-id="fcb79-273">Once the Azure AD B2C provisioning steps above are completed, the Azure AD B2C application must be registered in your Dynamics 365 Commerce environment.</span></span>

<span data-ttu-id="fcb79-274">Voit päivittää pääkonttorin uusilla Azure AD B2C -tiedoilla seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="fcb79-274">To update headquarters with the new Azure AD B2C information, follow these steps.</span></span>

1. <span data-ttu-id="fcb79-275">Valitse Commercessa **Kaupan yhteiset parametrit** ja valitse **Tunnistetietojen tarjoajat** vasemmanpuoleisessa valikossa.</span><span class="sxs-lookup"><span data-stu-id="fcb79-275">In Commerce, go to **Commerce Shared Parameters** and select **Identity Providers** in the left menu.</span></span>
1. <span data-ttu-id="fcb79-276">Tee **Tunnistetietojen tarjoajat** -kohdassa seuraavat toiminnot:</span><span class="sxs-lookup"><span data-stu-id="fcb79-276">Under **Identity Providers**, do the following:</span></span>
    1. <span data-ttu-id="fcb79-277">Anna **Myöntäjä**-ruutuun tunnistetietojen tarjoajan myöntäjän URL-osoite.</span><span class="sxs-lookup"><span data-stu-id="fcb79-277">In the **Issuer** box, enter the identity provider issuer URL.</span></span> <span data-ttu-id="fcb79-278">Voit etsiä myöntäjän URL-osoitteen alla olevan [Myöntäjän URL-osoitteen hankkiminen](#obtain-issuer-url) -kohdan avulla.</span><span class="sxs-lookup"><span data-stu-id="fcb79-278">To find your issuer URL, see [Obtain issuer URL](#obtain-issuer-url) below.</span></span>
    1. <span data-ttu-id="fcb79-279">Anna **Nimi**-ruutuun myöntäjän tietueen nimi.</span><span class="sxs-lookup"><span data-stu-id="fcb79-279">In the **Name** box, enter a name for your issuer record.</span></span>
    1. <span data-ttu-id="fcb79-280">Anna **Tyyppi**-ruutuun **Azure AD B2C (id_token)**.</span><span class="sxs-lookup"><span data-stu-id="fcb79-280">In the **Type** box, enter **Azure AD B2C (id_token)**.</span></span>
1. <span data-ttu-id="fcb79-281">Valitse yllä mainittu B2C:n tunnistetietojen tarjoajan nimike ja tee **Luovuttavat osapuolet** -kohdassa seuraavat toiminnot:</span><span class="sxs-lookup"><span data-stu-id="fcb79-281">Under **Relying Parties**, with the above B2C identity provider item selected, do the following:</span></span>
    1. <span data-ttu-id="fcb79-282">Anna **ClientID**-ruutuun B2C-sovelluksen tunnus.</span><span class="sxs-lookup"><span data-stu-id="fcb79-282">In the **ClientID** box, enter your B2C application ID.</span></span> <span data-ttu-id="fcb79-283">Se löytyy **Sovelluksen tunnus** -ruudusta B2C-sovelluksen ominaisuuksien sivulta.</span><span class="sxs-lookup"><span data-stu-id="fcb79-283">You can find this in the **Application ID** box of your B2C application's properties page.</span></span>
    1. <span data-ttu-id="fcb79-284">Kirjoita **Tyyppi**-ruutuun **Julkinen**.</span><span class="sxs-lookup"><span data-stu-id="fcb79-284">In the **Type** box, enter **Public**.</span></span>
    1. <span data-ttu-id="fcb79-285">Kirjoita **Käyttäjätyyppi**-ruutuun **Asiakas**.</span><span class="sxs-lookup"><span data-stu-id="fcb79-285">In the **User Type** box, enter **Customer**.</span></span>
1. <span data-ttu-id="fcb79-286">Valitse toimintoruudussa **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="fcb79-286">On the action pane, select **Save**.</span></span>
1. <span data-ttu-id="fcb79-287">Hae Commerce-hakuruudussa **Jakeluaikataulu**</span><span class="sxs-lookup"><span data-stu-id="fcb79-287">In the Commerce search box, search for **Distribution schedule**</span></span>
1. <span data-ttu-id="fcb79-288">Valitse **Jakeluaikataulut**-sivun vasemmanpuoleisessa valikossa **1110 Yleinen määritys** -työ.</span><span class="sxs-lookup"><span data-stu-id="fcb79-288">In the left navigation menu of the **Distribution schedules** page, select job **1110 Global configuration**.</span></span>
1. <span data-ttu-id="fcb79-289">Valitse toimintoruudussa **Suorita nyt**.</span><span class="sxs-lookup"><span data-stu-id="fcb79-289">On the action pane, select **Run Now**.</span></span>

### <a name="obtain-issuer-url"></a><span data-ttu-id="fcb79-290">Myöntäjän URL-osoitteen hankkiminen</span><span class="sxs-lookup"><span data-stu-id="fcb79-290">Obtain issuer URL</span></span>

<span data-ttu-id="fcb79-291">Voit hankkia tunnistetietojen tarjoajan URL-osoitteen seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="fcb79-291">To obtain your identity provider issuer URL, follow these steps.</span></span>

1. <span data-ttu-id="fcb79-292">Luo metatietojen URL-osoite seuraavassa muodossa käyttämällä B2C-vuokraajaa ja käytäntöä seuraavasti: ``https://<B2CTENANTNAME>.b2clogin.com/<B2CTENANTNAME>.onmicrosoft.com/v2.0/.well-known/openid-configuration?p=<B2CSIGN-INPOLICY>``</span><span class="sxs-lookup"><span data-stu-id="fcb79-292">Create a metadata address URL in the following format using your B2C tenant and policy: ``https://<B2CTENANTNAME>.b2clogin.com/<B2CTENANTNAME>.onmicrosoft.com/v2.0/.well-known/openid-configuration?p=<B2CSIGN-INPOLICY>``</span></span>
    - <span data-ttu-id="fcb79-293">Esimerkki: ``https://d365plc.b2clogin.com/d365plc.onmicrosoft.com/v2.0/.well-known/openid-configuration?p=B2C_1_signinup``.</span><span class="sxs-lookup"><span data-stu-id="fcb79-293">Example: ``https://d365plc.b2clogin.com/d365plc.onmicrosoft.com/v2.0/.well-known/openid-configuration?p=B2C_1_signinup``.</span></span>
1. <span data-ttu-id="fcb79-294">Kirjoita metatietojen osoitteen URL-osoite selaimen osoitepalkkiin.</span><span class="sxs-lookup"><span data-stu-id="fcb79-294">Enter the metadata address URL into a browser address bar.</span></span>
1. <span data-ttu-id="fcb79-295">Kopioi metatiedoissa tunnistetietojen tarjoajan myöntäjän URL-osoite (**myöntäjän** arvo).</span><span class="sxs-lookup"><span data-stu-id="fcb79-295">In the metadata, copy the identity provider issuer URL (the value for **"issuer"**).</span></span>
    - <span data-ttu-id="fcb79-296">Esimerkki: ``https://login.fabrikam.com/073405c3-0113-4f43-b5e2-df01266e24ae/v2.0/``.</span><span class="sxs-lookup"><span data-stu-id="fcb79-296">Example: ``https://login.fabrikam.com/073405c3-0113-4f43-b5e2-df01266e24ae/v2.0/``.</span></span>

## <a name="configure-your-b2c-tenant-in-commerce-site-builder"></a><span data-ttu-id="fcb79-297">B2C-vuokraajan määrittäminen Commerce-sivuston luontiohjelmassa</span><span class="sxs-lookup"><span data-stu-id="fcb79-297">Configure your B2C tenant in Commerce site builder</span></span>

<span data-ttu-id="fcb79-298">Kun Azure AD B2C -vuokraajan määrittäminen on tehty, B2C-vuokraaja on määritettävä Commerce-sivuston luontiohjelmassa.</span><span class="sxs-lookup"><span data-stu-id="fcb79-298">Once setup of your Azure AD B2C tenant is completed, you must configure the B2C tenant in Commerce site builder.</span></span> <span data-ttu-id="fcb79-299">Määritysvaiheita ovat esimerkiksi B2C-sovelluksen tietojen kerääminen Azure-portaalista, B2C-sovelluksen tietojen syöttäminen sivuston luontiohjelmaan ja B2C-sovelluksen liittäminen sivustoon ja kanavaan.</span><span class="sxs-lookup"><span data-stu-id="fcb79-299">Configuration steps include collecting B2C application information from the Azure portal, entering that B2C application information into site builder, and then associating the B2C application with your site and channel.</span></span>

### <a name="collect-the-required-application-information"></a><span data-ttu-id="fcb79-300">Tarvittavien sovellustietojen kerääminen</span><span class="sxs-lookup"><span data-stu-id="fcb79-300">Collect the required application information</span></span>

<span data-ttu-id="fcb79-301">Voit kerätä tarvittavat sovellustiedot seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="fcb79-301">To collect the required application information, follow these steps.</span></span>

1. <span data-ttu-id="fcb79-302">Siirry Azure-portaalissa kohtaan **Aloitus \> Azure AD B2C - sovellukset**.</span><span class="sxs-lookup"><span data-stu-id="fcb79-302">In the Azure portal, go to **Home \> Azure AD B2C - Applications**.</span></span>
1. <span data-ttu-id="fcb79-303">Valitse sovellus ja valitse sitten vasemmanpuoleisesta navigointiruudusta **Ominaisuudet**, jos haluat hakea sovelluksen tiedot.</span><span class="sxs-lookup"><span data-stu-id="fcb79-303">Select your application, and then in the left navigation pane select **Properties** to obtain the application details.</span></span>
1. <span data-ttu-id="fcb79-304">Kerää **Sovelluksen tunnus** -ruudusta B2C-sovelluksen tunnus, jonka B2C-vuokraaja loi.</span><span class="sxs-lookup"><span data-stu-id="fcb79-304">From the **Application ID** box, collect the application ID of the B2C application created in your B2C tenant.</span></span> <span data-ttu-id="fcb79-305">Tämä syötetään myöhemmin **Asiakasohjelman GUID** -arvona sivuston luontiohjelmaan.</span><span class="sxs-lookup"><span data-stu-id="fcb79-305">This will later be entered as the **Client GUID** in site builder.</span></span>
1. <span data-ttu-id="fcb79-306">Kerää **Vastauksen URL-osoite** -kohdasta vastauksen URL-osoite.</span><span class="sxs-lookup"><span data-stu-id="fcb79-306">Under **Reply URL**, collect the reply URL.</span></span>
1. <span data-ttu-id="fcb79-307">Siirry kohtaan **Aloitus \> Azure AD B2C – käyttäjän työnkulut (käytännöt)** ja kerää sitten kunkin käyttäjän työnkulkukäytännön nimet.</span><span class="sxs-lookup"><span data-stu-id="fcb79-307">Go to **Home \> Azure AD B2C – User flows (policies)**, and then collect the names of each user flow policy.</span></span>

<span data-ttu-id="fcb79-308">Seuraavassa kuvassa on esimerkki **Azure AD B2C - sovellukset** -sivusta.</span><span class="sxs-lookup"><span data-stu-id="fcb79-308">The following image shows an example of the **Azure AD B2C - Applications** page.</span></span>

![Siirtyminen vuokraajan B2C-sovellukseen](./media/B2CImage_19.png)

<span data-ttu-id="fcb79-310">Seuraavassa kuvassa on esimerkki sovelluksen **Ominaisuudet** -sivusta Azure AD B2C -ratkaisussa.</span><span class="sxs-lookup"><span data-stu-id="fcb79-310">The following image shows an example of an application **Properties** page in Azure AD B2C.</span></span> 

![Sovelluksen tunnuksen kopioiminen B2C-sovelluksen ominaisuuksista](./media/B2CImage_21.png)

<span data-ttu-id="fcb79-312">Seuraavassa kuvassa on esimerkki käyttäjän työnkulkukäytännöistä **Azure AD B2C – käyttäjän työnkulut (käytännöt)** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="fcb79-312">The following image shows an example of user flow policies on the **Azure AD B2C – User flows (policies)** page.</span></span>

![Kaikkien B2C-käytännön työnkulun nimien kerääminen](./media/B2CImage_22.png)

### <a name="enter-your-aad-b2c-tenant-application-information-into-commerce"></a><span data-ttu-id="fcb79-314">AAD B2C -vuokraajan sovelluksen tietojen syöttäminen Commerceen</span><span class="sxs-lookup"><span data-stu-id="fcb79-314">Enter your AAD B2C tenant application information into Commerce</span></span>

<span data-ttu-id="fcb79-315">Anna Azure AD B2C -vuokraajan tiedot Commercen sivuston luontiohjelmaan ennen B2C-vuokraajan liittämistä sivustoihin.</span><span class="sxs-lookup"><span data-stu-id="fcb79-315">You must enter details of the Azure AD B2C tenant into Commerce site builder before associating the B2C tenant with your site(s).</span></span>

<span data-ttu-id="fcb79-316">Voit lisätä AAD B2C -vuokraajan sovelluksen tiedot Commerceen seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="fcb79-316">To add your AAD B2C tenant application information to Commerce, follow these steps.</span></span>

1. <span data-ttu-id="fcb79-317">Kirjaudu sisään järjestelmänvalvojana Commerce-sivuston luontiohjelmaan ympäristössä.</span><span class="sxs-lookup"><span data-stu-id="fcb79-317">Sign in as an administrator to Commerce site builder for your environment.</span></span>
1. <span data-ttu-id="fcb79-318">Laajenna se valitsemalla vasemmasta siirtymisruudusta **Vuokraajan asetukset**.</span><span class="sxs-lookup"><span data-stu-id="fcb79-318">In the left navigation pane, select **Tenant Settings**  to expand it.</span></span>
1. <span data-ttu-id="fcb79-319">Valitse **Vuokraajan asetukset** -kohdasta **B2C-asetukset**.</span><span class="sxs-lookup"><span data-stu-id="fcb79-319">Under **Tenant Settings**, select **B2C Settings**.</span></span> 
1. <span data-ttu-id="fcb79-320">Valitse pääikkunassa **B2C-sovellukset**-kohdan vieressä oleva **Hallitse**.</span><span class="sxs-lookup"><span data-stu-id="fcb79-320">In the main window next **B2C Applications**, select **Manage**.</span></span> <span data-ttu-id="fcb79-321">(Jos vuokraaja näkyy B2C-sovellukset-luettelossa, järjestelmänvalvoja on jo lisännyt sen.</span><span class="sxs-lookup"><span data-stu-id="fcb79-321">(If your tenant appears in the B2C Applications list, then it was already added by an administrator.</span></span> <span data-ttu-id="fcb79-322">Tarkista, että vaiheen 6 nimikkeet vastaavat B2C-sovellusta.)</span><span class="sxs-lookup"><span data-stu-id="fcb79-322">Verify that the items in step 6 below match your B2C Application.)</span></span>
1. <span data-ttu-id="fcb79-323">Valitse **Lisää B2C-sovellus**.</span><span class="sxs-lookup"><span data-stu-id="fcb79-323">Select **Add B2C Application**.</span></span>
1. <span data-ttu-id="fcb79-324">Anna seuraavat pakolliset nimikkeet näkyvissä olevassa muodossa käyttämällä B2C-vuokraajan ja sovelluksen arvoja.</span><span class="sxs-lookup"><span data-stu-id="fcb79-324">Enter the following required items in the form displayed, using values from your B2C tenant and application.</span></span> <span data-ttu-id="fcb79-325">Kentät, jotka eivät ole pakollisia (joissa ei ole tähteä), voidaan jättää tyhjäksi.</span><span class="sxs-lookup"><span data-stu-id="fcb79-325">Fields that are not required (those without an asterisk) may be left blank.</span></span>

    - <span data-ttu-id="fcb79-326">**Sovelluksen nimi**: B2C-sovelluksen nimi, esimerkiksi FABRIKAM B2C.</span><span class="sxs-lookup"><span data-stu-id="fcb79-326">**Application Name**: The name for your B2C Application, for example "Fabrikam B2C".</span></span>
    - <span data-ttu-id="fcb79-327">**Vuokralaisen nimi**: B2C-vuokralaisen nimi (Käytä esimerkiksi fabrikam-nimeä, jos toimialue näkyy muodossa "fabrikam.onmicrosoft.com" B2C-vuokralaiselle).</span><span class="sxs-lookup"><span data-stu-id="fcb79-327">**Tenant Name**: The name of your B2C tenant (for example, use "fabrikam" if the domain appears as "fabrikam.onmicrosoft.com" for the B2C tenant).</span></span> 
    - <span data-ttu-id="fcb79-328">**Unohdetun salasanan käytännön tunnus**: Unohdetun salasanan käyttäjän työnkulkukäytännön tunnus, esimerkiksi B2C_1_PasswordReset.</span><span class="sxs-lookup"><span data-stu-id="fcb79-328">**Forget Password Policy ID**: The forget password user flow policy ID, for example "B2C_1_PasswordReset".</span></span>
    - <span data-ttu-id="fcb79-329">**SignUp SignIn -käytännön tunnus**: Rekisteröitymisen ja sisäänkirjauksen käyttäjän työnkulkukäytännön tunnus, esimerkiksi B2C_1_signup_signin.</span><span class="sxs-lookup"><span data-stu-id="fcb79-329">**Signup Signin Policy ID**: The sign up and sign in user flow policy ID, for example "B2C_1_signup_signin".</span></span>
    - <span data-ttu-id="fcb79-330">**Asiakasohjelman GUID**: B2C-sovelluksen tunnus, esimerkiksi 22290eb2-c52e-42e9-8b35-a2b0a3bcb9e6.</span><span class="sxs-lookup"><span data-stu-id="fcb79-330">**Client GUID**: The B2C application ID, for example "22290eb2-c52e-42e9-8b35-a2b0a3bcb9e6".</span></span>
    - <span data-ttu-id="fcb79-331">**Profiilin muokkauskäytännön tunnus**: Profiilin muokkaamisen käyttäjän työnkulkukäytännön tunnus, esimerkiksi B2C_1A_ProfileEdit.</span><span class="sxs-lookup"><span data-stu-id="fcb79-331">**Edit Profile Policy ID**: The profile editing user flow policy ID, for example "B2C_1A_ProfileEdit".</span></span>

1. <span data-ttu-id="fcb79-332">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="fcb79-332">Select **OK**.</span></span> <span data-ttu-id="fcb79-333">B2C-sovelluksen nimi tulee nyt näkyviin luetteloon.</span><span class="sxs-lookup"><span data-stu-id="fcb79-333">You should now see the name of your B2C application appear in the list.</span></span>
1. <span data-ttu-id="fcb79-334">Tallenna muutokset valitsemalla **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="fcb79-334">Select **Save** to save your changes.</span></span>

### <a name="associate-the-b2c-application-to-your-site-and-channel"></a><span data-ttu-id="fcb79-335">B2C-sovelluksen liittäminen sivustoon ja kanavaan</span><span class="sxs-lookup"><span data-stu-id="fcb79-335">Associate the B2C application to your site and channel</span></span>

> [!WARNING]
> <span data-ttu-id="fcb79-336">Jos sivusto on jo liitetty B2C-sovellukseen, toiseen B2C-sovellukseen vaihtaminen poistaa tähän ympäristöön jo rekisteröityneiden käyttäjien nykyiset viitteet.</span><span class="sxs-lookup"><span data-stu-id="fcb79-336">If your site is already associated with a B2C application, changing to a different B2C application will remove the current references established for users already signed up in this environment.</span></span> <span data-ttu-id="fcb79-337">Jos tätä muutetaan, mitkään tällä hetkellä liitetyn B2C-sovelluksen tunnistetiedot eivät ole käyttäjien käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="fcb79-337">If changed, any credentials associated with the currently-assigned B2C application will not be available to users.</span></span> 
> 
> <span data-ttu-id="fcb79-338">Päivitä vain B2C-sovellus, jos olet määrittämässä kanavan B2C-sovellusta ensimmäistä kertaa tai jos yrität saada käyttäjät rekisteröitymään uudelleen tähän kanavaan uuden B2C-sovelluksen avulla uusilla tunnistetiedoilla.</span><span class="sxs-lookup"><span data-stu-id="fcb79-338">Only update the B2C application if you are setting up the channel's B2C application for the first time or if you intend to have users re-sign up with new credentials to this channel with the new B2C application.</span></span> <span data-ttu-id="fcb79-339">Ole varovainen, kun liität kanavia B2C-sovelluksiin. Anna sovelluksille selkeät nimet.</span><span class="sxs-lookup"><span data-stu-id="fcb79-339">Take caution when associating channels to B2C applications, and name applications clearly.</span></span> <span data-ttu-id="fcb79-340">Jos kanavaa ei ole liitetty B2C-sovellukseen alla kuvattujen vaiheiden avulla, kanavaan kirjautuvat käyttäjät siirretään B2C-sovellukseen, joka on **oletussovellus** B2C-sovellusten **Vuokraajan asetukset \> B2C-asetukset** -luettelossa.</span><span class="sxs-lookup"><span data-stu-id="fcb79-340">If a channel is not associated to a B2C application in the steps below, users signing into that channel for your site will be entered into the B2C application showing as **default** in the **Tenant Settings \> B2C Settings** list of B2C applications.</span></span>

<span data-ttu-id="fcb79-341">Voit liittää B2C-sovelluksen sivustoon ja kanavaan seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="fcb79-341">To associate the B2C application to your site and channel, follow these steps.</span></span>

1. <span data-ttu-id="fcb79-342">Siirry sivustoon Commerce-sivuston luontiohjelmassa.</span><span class="sxs-lookup"><span data-stu-id="fcb79-342">Navigate to your site in Commerce site builder.</span></span>
1. <span data-ttu-id="fcb79-343">Laajenna se valitsemalla vasemmasta siirtymisruudusta **Sivuston asetukset**.</span><span class="sxs-lookup"><span data-stu-id="fcb79-343">In the left navigation pane, select **Site Settings** to expand it.</span></span>
1. <span data-ttu-id="fcb79-344">Valitse **Sivuston asetukset** -kohdassa **Kanavat**.</span><span class="sxs-lookup"><span data-stu-id="fcb79-344">Below **Site Settings**, select **Channels**.</span></span>
1. <span data-ttu-id="fcb79-345">Valitse pääikkunassa **Kanavat**-kohdassa kanava.</span><span class="sxs-lookup"><span data-stu-id="fcb79-345">In the main window under **Channels**, select your channel.</span></span>
1. <span data-ttu-id="fcb79-346">Valitse oikeanpuoleisessa kanavan ominaisuuksien ruudussa B2C-sovelluksen nimi avattavasta **Valitse B2C-sovellus** -luettelosta.</span><span class="sxs-lookup"><span data-stu-id="fcb79-346">In the channel properties pane on the right, select your B2C application name from the **Select B2C Application** drop down menu.</span></span>
1. <span data-ttu-id="fcb79-347">Valitse **Sulje** ja valitse sitten **Tallenna ja julkaise**.</span><span class="sxs-lookup"><span data-stu-id="fcb79-347">Select **Close**, and then select **Save and Publish**.</span></span>

## <a name="additional-b2c-information"></a><span data-ttu-id="fcb79-348">B2C-lisätiedot</span><span class="sxs-lookup"><span data-stu-id="fcb79-348">Additional B2C information</span></span>

### <a name="customer-migration"></a><span data-ttu-id="fcb79-349">Asiakkaan siirtäminen</span><span class="sxs-lookup"><span data-stu-id="fcb79-349">Customer migration</span></span>

<span data-ttu-id="fcb79-350">Jos harkitset asiakastietojen siirtämistä aiemmasta tunnistetietojen tarjoajan ympäristöstä, tarkista asiakkaan siirron tarpeet Dynamics 365 Commerce -ryhmän kanssa.</span><span class="sxs-lookup"><span data-stu-id="fcb79-350">If you are considering migrating customer records from a previous identity provider platform, please work with the Dynamics 365 Commerce team to review your customer migration needs.</span></span>

<span data-ttu-id="fcb79-351">Lisätietoja asiakkaan siirron Azure AD B2C -dokumentaatiosta on kohdassa [Käyttäjien siirtäminen Azure Active Directory B2C -sovellukseen](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-user-migration).</span><span class="sxs-lookup"><span data-stu-id="fcb79-351">For additional Azure AD B2C documentation on customer migration, see [Migrate users to Azure Active Directory B2C](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-user-migration).</span></span>

### <a name="custom-policies"></a><span data-ttu-id="fcb79-352">Mukautetut käytännöt</span><span class="sxs-lookup"><span data-stu-id="fcb79-352">Custom policies</span></span>

<span data-ttu-id="fcb79-353">Lisätietoja Azure AD B2C -sovelluksen yhteydenottojen ja käytännön työnkulkujen mukauttamisesta erilaisiksi kuin B2C-standardikäytännöt on kohdassa [Azure Active Directory B2C -sovelluksen mukautetut käytännöt](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-overview-custom).</span><span class="sxs-lookup"><span data-stu-id="fcb79-353">For additional information regarding customizing Azure AD B2C interactions and policy flows beyond what is offered by B2C standard policies, see [Custom policies in Azure Active Directory B2C](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-overview-custom).</span></span> 

### <a name="secondary-admin"></a><span data-ttu-id="fcb79-354">Toissijainen järjestelmänvalvoja</span><span class="sxs-lookup"><span data-stu-id="fcb79-354">Secondary admin</span></span>

<span data-ttu-id="fcb79-355">Valinnainen toissijainen järjestelmänvalvojatili voidaan lisätä B2C-vuokraajan **Käyttäjä**-osaan.</span><span class="sxs-lookup"><span data-stu-id="fcb79-355">An optional, secondary administrator account can be added in the **Users** section of your B2C tenant.</span></span> <span data-ttu-id="fcb79-356">Tämä voi olla suora tili tai yleinen tili.</span><span class="sxs-lookup"><span data-stu-id="fcb79-356">This can be a direct account or a general account.</span></span> <span data-ttu-id="fcb79-357">Jos sinun on jaettava tili ryhmän resursseille, myös yhteinen tili voidaan luoda.</span><span class="sxs-lookup"><span data-stu-id="fcb79-357">If you need to share an account across team resources, a common account can also be created.</span></span> <span data-ttu-id="fcb79-358">Azure AD B2C -sovellukseen tallennettujen tietojen luottamuksellisuuden vuoksi yrityksen turvakäytäntöjen tulee valvoa yleistä tiliä tarkasti.</span><span class="sxs-lookup"><span data-stu-id="fcb79-358">Due to the sensitivity of the data stored in Azure AD B2C, a common account should be monitored closely per your company's security practices.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="fcb79-359">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="fcb79-359">Additional resources</span></span>

[<span data-ttu-id="fcb79-360">Toimialueen nimen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="fcb79-360">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="fcb79-361">Uuden sähköisen kaupankäynnin vuokraajan käyttöönotto</span><span class="sxs-lookup"><span data-stu-id="fcb79-361">Deploy a new e-commerce tenant</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="fcb79-362">Sähköisen kaupankäynnin sivuston luominen</span><span class="sxs-lookup"><span data-stu-id="fcb79-362">Create an e-commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="fcb79-363">Dynamics 365 Commerce -sivuston liittäminen online-kanavaan</span><span class="sxs-lookup"><span data-stu-id="fcb79-363">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="fcb79-364">Robots.txt-tiedostojen hallinta</span><span class="sxs-lookup"><span data-stu-id="fcb79-364">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

<span data-ttu-id="fcb79-365">[Lataa URL-uudelleenohjaukset joukkotoimintona](upload-bulk-redirects.md)Liitä Dynamics 365 Commerce -sivusto online-kanavaan</span><span class="sxs-lookup"><span data-stu-id="fcb79-365">[Upload URL redirects in bulk](upload-bulk-redirects.md)Associate a Dynamics 365 Commerce site with an online channel</span></span>

[<span data-ttu-id="fcb79-366">Mukautettujen sivujen määrittäminen käyttäjän kirjautumisia varten</span><span class="sxs-lookup"><span data-stu-id="fcb79-366">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="fcb79-367">Useiden kuluttajakaupan vuokraajien määrittäminen Commerce-ympäristössä</span><span class="sxs-lookup"><span data-stu-id="fcb79-367">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="fcb79-368">Sisältöverkon (CDN) tuen lisääminen</span><span class="sxs-lookup"><span data-stu-id="fcb79-368">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="fcb79-369">Sijaintiin perustuvan myymälän tunnistuksen käyttöönotto</span><span class="sxs-lookup"><span data-stu-id="fcb79-369">Enable location-based store detection</span></span>](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
