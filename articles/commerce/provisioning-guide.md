---
title: Commercen esikatseluympäristön valmisteleminen
description: Tässä ohjeaiheessa kerrotaan, kuinka voit valmistella Microsoft Dynamics 365 Commercen esikatseluympäristön.
author: psimolin
manager: annbe
ms.date: 01/06/2020
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
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: b77d2cbbc100aeae5dcd53ddbe69ff2e4435da13
ms.sourcegitcommit: 4d77d06a07ec9e7a3fcbd508afdffaa406fd3dd8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/06/2020
ms.locfileid: "2934745"
---
# <a name="provision-a-commerce-preview-environment"></a><span data-ttu-id="d42d8-103">Commercen esikatseluympäristön valmisteleminen</span><span class="sxs-lookup"><span data-stu-id="d42d8-103">Provision a Commerce preview environment</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="d42d8-104">Tässä ohjeaiheessa kerrotaan, kuinka voit valmistella Microsoft Dynamics 365 Commercen esikatseluympäristön.</span><span class="sxs-lookup"><span data-stu-id="d42d8-104">This topic explains how to provision a Microsoft Dynamics 365 Commerce preview environment.</span></span>

<span data-ttu-id="d42d8-105">Ennen kuin aloitat, kannattaa lukaista tämän koko ohjeaiheen läpi. Näin saat käsityksen siitä, millainen prosessi on ja mitä tämä ohjeaihe sisältää.</span><span class="sxs-lookup"><span data-stu-id="d42d8-105">Before you begin, we recommend that you at least skim through this whole topic to get an idea of what the process entails and what this topic contains.</span></span>

> [!NOTE]
> <span data-ttu-id="d42d8-106">Jos sinulle ei ole vielä myönnetty Dynamics 365 Commerce Preview -sovelluksen käyttöoikeutta, voit pyytää esiversion käyttöoikeuden [Commerce-sivuston](https://aka.ms/Dynamics365CommerceWebsite) avulla.</span><span class="sxs-lookup"><span data-stu-id="d42d8-106">If you haven't yet been granted access to the Dynamics 365 Commerce preview, you can request preview access from the [Commerce website](https://aka.ms/Dynamics365CommerceWebsite).</span></span>

## <a name="overview"></a><span data-ttu-id="d42d8-107">Yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="d42d8-107">Overview</span></span>

<span data-ttu-id="d42d8-108">Jotta voit laatia Commerce Preview -ympäristön onnistuneesti, sinun on luotava projekti, jolla on tietty tuotteen nimi ja tyyppi.</span><span class="sxs-lookup"><span data-stu-id="d42d8-108">To successfully provision your Commerce preview environment, you must create a project that has a specific product name and type.</span></span> <span data-ttu-id="d42d8-109">Ympäristöllä ja Retail Cloud Scale Unit (RCSU) -ratkaisulla on myös joitakin tiettyjä parametreja, joita on käytettävä, kun myöhemmin valmistelet sähköistä kaupankäyntiä.</span><span class="sxs-lookup"><span data-stu-id="d42d8-109">The environment and Retail Cloud Scale Unit (RCSU) also have some specific parameters that you must use when you provision e-Commerce later.</span></span> <span data-ttu-id="d42d8-110">Tämän ohjeaiheen ohjeissa kuvataan kaikki vaaditut vaiheet, jotka sinun on suoritettava, ja parametrit, joita sinun on käytettävä.</span><span class="sxs-lookup"><span data-stu-id="d42d8-110">The instructions in this topic describe all the required steps that you must complete and the parameters that you must use.</span></span>

<span data-ttu-id="d42d8-111">Kun olet onnistuneesti valmistellut Commercen esikatseluympäristön, sinun on suoritettava muutama valmistelun jälkeinen vaihe sen valmistelemiseksi.</span><span class="sxs-lookup"><span data-stu-id="d42d8-111">After you successfully provision your Commerce preview environment, you must complete a few post-provisioning steps to prepare it.</span></span> <span data-ttu-id="d42d8-112">Jotkin vaiheet ovat valinnaisia. Tämä riippuu siitä, mitä järjestelmän alueita haluat arvioida.</span><span class="sxs-lookup"><span data-stu-id="d42d8-112">Some steps are optional, depending on the aspects of the system that you want to evaluate.</span></span> <span data-ttu-id="d42d8-113">Voit aina suorittaa valinnaiset vaiheet myöhemmin.</span><span class="sxs-lookup"><span data-stu-id="d42d8-113">You can always complete the optional steps later.</span></span>

<span data-ttu-id="d42d8-114">Katso lisätietoja Commercen esikatseluympäristön määrittelystä kohdasta sen jälkeen, kun olet valmistellut sen [Commercen esikatseluympäristön määrittäminen](cpe-post-provisioning.md).</span><span class="sxs-lookup"><span data-stu-id="d42d8-114">For information about how to configure your Commerce preview environment after you provision it, see [Configure a Commerce preview environment](cpe-post-provisioning.md).</span></span> <span data-ttu-id="d42d8-115">Jos haluat lisätietoja valinnaisten ominaisuuksien määrittämisestä Commercen esikatseluympäristöön, katso [Lisäominaisuuksien määrittäminen Commercen esikatseluympäristöä varten](cpe-optional-features.md).</span><span class="sxs-lookup"><span data-stu-id="d42d8-115">For information about how to configure optional features for your Commerce preview environment, see [Configure optional features for a Commerce preview environment](cpe-optional-features.md).</span></span>

<span data-ttu-id="d42d8-116">Jos haluat lisätietoja valmistelun vaiheista tai jos kohtaat ongelmia, kerro se Microsoftille [Microsoft Dynamics 365 Commerce Preview Yammer -ryhmän](https://aka.ms/Dynamics365CommercePreviewYammer) kautta.</span><span class="sxs-lookup"><span data-stu-id="d42d8-116">If you have any questions about the provisioning steps, or if you encounter any issues, let Microsoft know in the [Microsoft Dynamics 365 Commerce Preview Yammer group](https://aka.ms/Dynamics365CommercePreviewYammer).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="d42d8-117">Edellytykset</span><span class="sxs-lookup"><span data-stu-id="d42d8-117">Prerequisites</span></span>

<span data-ttu-id="d42d8-118">Seuraavien edellytysten on oltava käytössä, ennen kuin voit määrittää Commerce Preview -ympäristön:</span><span class="sxs-lookup"><span data-stu-id="d42d8-118">The following prerequisites must be in place before you can provision your Commerce preview environment:</span></span>

- <span data-ttu-id="d42d8-119">Sinulla on Microsoft Dynamics Lifecycle Services -portaalin (LCS) käyttöoikeus</span><span class="sxs-lookup"><span data-stu-id="d42d8-119">You have access to the Microsoft Dynamics Lifecycle Services (LCS) portal.</span></span>
- <span data-ttu-id="d42d8-120">Sinut on hyväksytty Dynamics 365 Commerce Preview -ohjelmaan.</span><span class="sxs-lookup"><span data-stu-id="d42d8-120">You've been accepted into the Dynamics 365 Commerce Preview program.</span></span>
- <span data-ttu-id="d42d8-121">Sinulla on projektin luomisessa vaaditut **Mahdolliset myyntiä edeltävät toimet**- tai **Siirrä, luo ratkaisuja ja opi** -kohtien oikeudet.</span><span class="sxs-lookup"><span data-stu-id="d42d8-121">You have the required permissions to create a project for **Prospective presales** or **Migrate, create solutions, and learn**.</span></span>
- <span data-ttu-id="d42d8-122">Olet **Ympäristövastaava**- tai **Projektin omistaja** -roolin jäsen projektissa, jolle valmistelet ympäristöä.</span><span class="sxs-lookup"><span data-stu-id="d42d8-122">You're a member of the **Environment manager** or **Project owner** role in the project where you will provision the environment.</span></span>
- <span data-ttu-id="d42d8-123">Sinulla on järjestelmänvalvojan oikeudet Microsoft Azure -tilausta varten, tai ota yhteyttä tilauksen järjestelmänvalvojaan, joka voi suorittaa puolestasi järjestelmänvalvojan oikeudet vaativat kaksi vaihetta.</span><span class="sxs-lookup"><span data-stu-id="d42d8-123">You have admin access to your Microsoft Azure subscription, or you're in contact with a subscription admin who can complete the two steps that require admin permissions on your behalf.</span></span>
- <span data-ttu-id="d42d8-124">Sinulla on käytettävissä Azure Active Directory (Azure AD) -vuokralaisen tunnus.</span><span class="sxs-lookup"><span data-stu-id="d42d8-124">You have your Azure Active Directory (Azure AD) tenant ID available.</span></span>
- <span data-ttu-id="d42d8-125">Olet luonut Azure AD -käyttöoikeusryhmän, jota voidaan käyttää sähköisen kaupankäynnin järjestelmänvalvojien ryhmänä, ja sinulla on ryhmän tunnus.</span><span class="sxs-lookup"><span data-stu-id="d42d8-125">You've created an Azure AD security group that can be used as an e-Commerce system admin group, and you have its ID available.</span></span>
- <span data-ttu-id="d42d8-126">Olet luonut Azure AD -käyttöoikeusryhmän, jota voidaan käyttää arviot ja arvostelut -moderaattorien ryhmänä, ja sinulla on ryhmän tunnus.</span><span class="sxs-lookup"><span data-stu-id="d42d8-126">You've created an Azure AD security group that can be used as a Ratings and Reviews moderator group, and you have its ID available.</span></span> <span data-ttu-id="d42d8-127">(Tämä suojausryhmä voi olla sama kuin verkkokauppajärjestelmän järjestelmänvalvojaryhmä.)</span><span class="sxs-lookup"><span data-stu-id="d42d8-127">(This security group can be the same as the e-Commerce system admin group.)</span></span>

### <a name="find-your-azure-ad-tenant-id"></a><span data-ttu-id="d42d8-128">Etsi Azure AD-vuokraajan tunnus</span><span class="sxs-lookup"><span data-stu-id="d42d8-128">Find your Azure AD tenant ID</span></span>

<span data-ttu-id="d42d8-129">Azure AD -vuokraajasi tunnus on yleisesti yksilöllinen GUID-tunnus, joka muistuttaa tätä esimerkkiä: **72f988bf-86f1-41af-91ab-2d7cd011db47**.</span><span class="sxs-lookup"><span data-stu-id="d42d8-129">Your Azure AD tenant ID is a globally unique identifier (GUID) that resembles this example: **72f988bf-86f1-41af-91ab-2d7cd011db47**.</span></span>

#### <a name="find-your-azure-ad-tenant-id-by-using-the-azure-portal"></a><span data-ttu-id="d42d8-130">Azure AD -vuokraajan tunnuksen etsiminen Azure-portaalin avulla</span><span class="sxs-lookup"><span data-stu-id="d42d8-130">Find your Azure AD tenant ID by using the Azure portal</span></span>

1. <span data-ttu-id="d42d8-131">Kirjaudu [Azure-portaalin osoitteessa](https://portal.azure.com/).</span><span class="sxs-lookup"><span data-stu-id="d42d8-131">Sign in to the [Azure portal](https://portal.azure.com/).</span></span>
1. <span data-ttu-id="d42d8-132">Varmista, että oikea hakemisto on valittu.</span><span class="sxs-lookup"><span data-stu-id="d42d8-132">Make sure that the correct directory is selected.</span></span>
1. <span data-ttu-id="d42d8-133">Valitse vasemmalla olevasta valikosta **Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="d42d8-133">On the menu on the left, select **Azure Active Directory**.</span></span>
1. <span data-ttu-id="d42d8-134">Valitse **Hallinta**-kohdasta **Ominaisuudet**.</span><span class="sxs-lookup"><span data-stu-id="d42d8-134">Under **Manage**, select **Properties**.</span></span> <span data-ttu-id="d42d8-135">Azure AD -vuokraajan tunnus näkyy **hakemistotunnus**-kohdassa.</span><span class="sxs-lookup"><span data-stu-id="d42d8-135">Your Azure AD tenant ID appears under **Directory ID**.</span></span>

#### <a name="find-your-azure-ad-tenant-id-by-using-openid-connect-metadata"></a><span data-ttu-id="d42d8-136">Azure AD -vuokraajan tunnuksen etsiminen OpenID Connectin metatietojen avulla</span><span class="sxs-lookup"><span data-stu-id="d42d8-136">Find your Azure AD tenant ID by using OpenID Connect metadata</span></span>

<span data-ttu-id="d42d8-137">Luo OpenID-URL-osoite korvaamalla **\{OMA\_TOIMIALUEESI\}**, kuten `microsoft.com`.</span><span class="sxs-lookup"><span data-stu-id="d42d8-137">Create an OpenID URL by replacing **\{YOUR\_DOMAIN\}** with your domain, such as `microsoft.com`.</span></span> <span data-ttu-id="d42d8-138">Esimerkiksi toimialueesta `https://login.microsoftonline.com/{YOUR_DOMAIN}/.well-known/openid-configuration` tulee `https://login.microsoftonline.com/microsoft.com/.well-known/openid-configuration`.</span><span class="sxs-lookup"><span data-stu-id="d42d8-138">For example, `https://login.microsoftonline.com/{YOUR_DOMAIN}/.well-known/openid-configuration` will become `https://login.microsoftonline.com/microsoft.com/.well-known/openid-configuration`.</span></span>

1. <span data-ttu-id="d42d8-139">Siirry siihen OpenID-URL-osoitteeseen, joka sisältää toimialueesi.</span><span class="sxs-lookup"><span data-stu-id="d42d8-139">Go to the OpenID URL that contains your domain.</span></span>

    <span data-ttu-id="d42d8-140">Azure AD-vuokraajan tunnus näkyy usean ominaisuuden arvoissa.</span><span class="sxs-lookup"><span data-stu-id="d42d8-140">You can find you Azure AD tenant ID in multiple property values.</span></span>

1. <span data-ttu-id="d42d8-141">Etsi **valtuutustieto\_päätepiste** ja pura GUID-tunnus, joka näkyy heti `login.microsoftonline.com/`in jälkeen.</span><span class="sxs-lookup"><span data-stu-id="d42d8-141">Find **authorization\_endpoint**, and extract the GUID that appears immediately after `login.microsoftonline.com/`.</span></span>

### <a name="find-your-azure-ad-security-group-id"></a><span data-ttu-id="d42d8-142">Azure AD -suojausryhmän tunnuksen etsiminen</span><span class="sxs-lookup"><span data-stu-id="d42d8-142">Find your Azure AD security group ID</span></span>

<span data-ttu-id="d42d8-143">Azure AD -suojausryhmän tunnus on tämän esimerkin kaltainen GUID: **436ea7f5-ee6c-40c1-9f08-825c5811066a**.</span><span class="sxs-lookup"><span data-stu-id="d42d8-143">The ID of your Azure AD security group is a GUID that resembles this example: **436ea7f5-ee6c-40c1-9f08-825c5811066a**.</span></span>

<span data-ttu-id="d42d8-144">Tässä menettelyssä oletetaan, että olet sen ryhmän jäsen, jolle yrität löytää tunnuksen.</span><span class="sxs-lookup"><span data-stu-id="d42d8-144">This procedure assumes that you're a member of the group that you're trying to find the ID for.</span></span>

1. <span data-ttu-id="d42d8-145">Avaa [Graph-työkalu](https://developer.microsoft.com/graph/graph-explorer#).</span><span class="sxs-lookup"><span data-stu-id="d42d8-145">Open the [Graph Explorer](https://developer.microsoft.com/graph/graph-explorer#).</span></span>
1. <span data-ttu-id="d42d8-146">Valitse **Kirjaudu sisään Microsoftin avulla** ja kirjaudu sisään tunnistetietojen avulla.</span><span class="sxs-lookup"><span data-stu-id="d42d8-146">Select **Sign In with Microsoft**, and sign in by using your credentials.</span></span>
1. <span data-ttu-id="d42d8-147">Valitse vasemmalta **Näytä lisää näytteitä**.</span><span class="sxs-lookup"><span data-stu-id="d42d8-147">On the left, select **show more samples**.</span></span>
1. <span data-ttu-id="d42d8-148">Ota oikeanpuoleisesta ruudusta käyttöön **ryhmät**.</span><span class="sxs-lookup"><span data-stu-id="d42d8-148">In the right pane, enable **Groups**.</span></span>
1. <span data-ttu-id="d42d8-149">Sulje oikeanpuoleinen ruutu.</span><span class="sxs-lookup"><span data-stu-id="d42d8-149">Close the right pane.</span></span>
1. <span data-ttu-id="d42d8-150">Valitse **kaikki ryhmät, joihin kuulun**.</span><span class="sxs-lookup"><span data-stu-id="d42d8-150">Select **all groups I belong to**.</span></span>
1. <span data-ttu-id="d42d8-151">Etsi **Vastauksen esikatselu** -kentästä ryhmäsi.</span><span class="sxs-lookup"><span data-stu-id="d42d8-151">In the **Response Preview** field, find your group.</span></span> <span data-ttu-id="d42d8-152">Suojausryhmän tunnus näkyy **Tunnus**-ominaisuuden alla.</span><span class="sxs-lookup"><span data-stu-id="d42d8-152">The security group ID appears under the **id** property.</span></span>

## <a name="provision-your-commerce-preview-environment"></a><span data-ttu-id="d42d8-153">Commercen esikatseluympäristön valmisteleminen</span><span class="sxs-lookup"><span data-stu-id="d42d8-153">Provision your Commerce preview environment</span></span>

<span data-ttu-id="d42d8-154">Näissä ohjeissa kerrotaan, miten Commerce Preview -ympäristö tarjotaan.</span><span class="sxs-lookup"><span data-stu-id="d42d8-154">These procedures explain how to provision a Commerce preview environment.</span></span> <span data-ttu-id="d42d8-155">Kun olet suorittanut ne onnistuneesti, Commerce Preview -ympäristö on valmiina konfigurointia varten.</span><span class="sxs-lookup"><span data-stu-id="d42d8-155">After you successfully complete them, the Commerce preview environment will be ready for configuration.</span></span> <span data-ttu-id="d42d8-156">Kaikki tässä kuvatut toiminnot tapahtuvat LCS-portaalissa.</span><span class="sxs-lookup"><span data-stu-id="d42d8-156">All the activities that are described here occur in the LCS portal.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d42d8-157">Esikatselun käyttö on sidottu esikatselusovelluksessa määrittämääsi LCS-tiliin ja organisaatioon.</span><span class="sxs-lookup"><span data-stu-id="d42d8-157">Preview access is tied to the LCS account and organization that you specified in your preview application.</span></span> <span data-ttu-id="d42d8-158">Sinun on käytettävä samaa tiliä Commerce Preview -ympäristön tarjoamiseen.</span><span class="sxs-lookup"><span data-stu-id="d42d8-158">You must use the same account to provision the Commerce preview environment.</span></span> <span data-ttu-id="d42d8-159">Jos sinun on käytettävä Commerce Preview -ympäristössä eri LCS-tiliä tai -vuokraajaa, sinun on annettava kyseiset tiedot Microsoftille.</span><span class="sxs-lookup"><span data-stu-id="d42d8-159">If you must use a different LCS account or tenant for the Commerce preview environment, you must provide those details to Microsoft.</span></span> <span data-ttu-id="d42d8-160">Yhteystiedot ovat jäljempänä tämän ohjeaiheen [ Commerce Preview -ympäristön tuki](#commerce-preview-environment-support) -osiossa.</span><span class="sxs-lookup"><span data-stu-id="d42d8-160">For contact information, see the [Commerce preview environment support](#commerce-preview-environment-support) section later in this topic.</span></span>

### <a name="grant-access-to-e-commerce-applications"></a><span data-ttu-id="d42d8-161">Sähköisen kaupankäynnin sovellusten käyttöoikeuden myöntäminen</span><span class="sxs-lookup"><span data-stu-id="d42d8-161">Grant access to e-Commerce applications</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d42d8-162">Henkilön, joka kirjautuu sisään, on oltava Azure AD -vuokraaja-järjestelmänvalvoja , jolla on Azure AD -vuokraajan tunnus.</span><span class="sxs-lookup"><span data-stu-id="d42d8-162">The person who signs in must be an Azure AD tenant admin who has the Azure AD tenant ID.</span></span> <span data-ttu-id="d42d8-163">Jos tätä vaihetta ei suoritettu loppuun, jäljellä olevat valmisteluvaiheet epäonnistuvat.</span><span class="sxs-lookup"><span data-stu-id="d42d8-163">If this step isn't successfully completed, the remaining provisioning steps will fail.</span></span>

<span data-ttu-id="d42d8-164">Jos haluat valtuuttaa sähköisen kaupankäynnin sovellukset käyttämään Azure-tilausta, toimi seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="d42d8-164">To authorize e-Commerce applications to access your Azure subscription, follow these steps.</span></span>

1. <span data-ttu-id="d42d8-165">Kokoa URL-osoite seuraavassa muodossa:</span><span class="sxs-lookup"><span data-stu-id="d42d8-165">Assemble a URL in the following format:</span></span>

    `https://login.windows.net/{AAD_TENANT_ID}/oauth2/authorize?client_id=fbcbf727-cd18-4422-a723-f8274075331a&response_type=code&redirect_uri=https://sb.manage.commerce.dynamics.com/_commerce/Consent&response_mode=query&prompt=admin_consent&state=12345`

1. <span data-ttu-id="d42d8-166">Kopioi ja liitä URL-osoite selaimeesi tai tekstieditoriin ja korvaa **\{AAD\_-\_VUOKRAAJAN\}** tunnus Azure AD -vuokraajasi tunnuksella.</span><span class="sxs-lookup"><span data-stu-id="d42d8-166">Copy and paste the URL into your browser or text editor, and replace **\{AAD\_TENANT\_ID\}** with your Azure AD tenant ID.</span></span> <span data-ttu-id="d42d8-167">Avaa sitten URL-osoite.</span><span class="sxs-lookup"><span data-stu-id="d42d8-167">Then open the URL.</span></span>
1. <span data-ttu-id="d42d8-168">Kirjaudu sisään Azure AD -valintaikkunassa ja vahvista, että haluat myöntää **Dynamics 365 Commerce (esikatselu)** -sovellukselle tilauksesi käyttöoikeuden.</span><span class="sxs-lookup"><span data-stu-id="d42d8-168">In the Azure AD sign-in dialog box, sign in, and confirm that you want to grant **Dynamics 365 Commerce (Preview)** access to your subscription.</span></span> <span data-ttu-id="d42d8-169">Sinut ohjataan sivulle, joka osoittaa, onko toimenpide onnistunut.</span><span class="sxs-lookup"><span data-stu-id="d42d8-169">You're redirected to a page that indicates whether the operation was successful.</span></span>

### <a name="confirm-that-preview-features-are-available-and-turned-on-in-lcs"></a><span data-ttu-id="d42d8-170">Tarkista, että esiversio-ominaisuudet ovat käytettävissä ja että ne on otettu käyttöön LCS:ssä</span><span class="sxs-lookup"><span data-stu-id="d42d8-170">Confirm that preview features are available and turned on in LCS</span></span>

<span data-ttu-id="d42d8-171">Toimi seuraavasti tarkistaaksesi, että esiversio-ominaisuudet ovat käytettävissä ja että ne on otettu käyttöön LCS:ssä.</span><span class="sxs-lookup"><span data-stu-id="d42d8-171">To confirm that preview features are available and turned on in LCS, follow these steps.</span></span>

1. <span data-ttu-id="d42d8-172">Kirjaudu sisään [LCS-portaaliin](https://lcs.dynamics.com) käyttämällä samaa LCS-tiliä, jota käytit pyytämällä esikatselun käyttöoikeutta.</span><span class="sxs-lookup"><span data-stu-id="d42d8-172">Sign in to the [LCS portal](https://lcs.dynamics.com) by using the same LCS account that you used to request access to the preview.</span></span>
1. <span data-ttu-id="d42d8-173">Vieritä LCS:n kotisivua oikeaan reunaan ja valitse **Esiversio-ominaisuuksien hallinta** -ruutu.</span><span class="sxs-lookup"><span data-stu-id="d42d8-173">On the LCS home page, scroll all the way to the right, and select the **Preview feature management** tile.</span></span>

    ![Esiversion hallinta -ruutu](./media/preview1.png)

1. <span data-ttu-id="d42d8-175">Vieritä **Yksityisen esiversion ominaisuudet** -kohtaan ja vahvista, että seuraavat ominaisuudet ovat käytettävissä ja että ne on otettu käyttöön:</span><span class="sxs-lookup"><span data-stu-id="d42d8-175">Scroll down to **Private preview features**, and confirm that the following features are available and turned on:</span></span>

    - <span data-ttu-id="d42d8-176">Sähköisen kaupankäynnin arviointi</span><span class="sxs-lookup"><span data-stu-id="d42d8-176">e-Commerce Evaluation</span></span>
    - <span data-ttu-id="d42d8-177">Commerce Preview -ohjelman ympäristöt</span><span class="sxs-lookup"><span data-stu-id="d42d8-177">Commerce Preview Program Environments</span></span>

    ![Yksityisen esiversion ominaisuudet](./media/preview2.png)

1. <span data-ttu-id="d42d8-179">Jos nämä ominaisuudet eivät näy luettelossa, ota yhteyttä Microsoftiin ja anna työsähköpostiosoitteesi, LCS-tilisi ja vuokralaisen tiedot.</span><span class="sxs-lookup"><span data-stu-id="d42d8-179">If those features don't appear in the list, contact Microsoft, and provide your work email address, LCS account, and tenant details.</span></span> <span data-ttu-id="d42d8-180">Yhteystiedot löydät [ Commerce Preview -ympäristön tuki](#commerce-preview-environment-support) -osiosta.</span><span class="sxs-lookup"><span data-stu-id="d42d8-180">For contact information, see the [Commerce preview environment support](#commerce-preview-environment-support) section.</span></span>

### <a name="create-a-new-project"></a><span data-ttu-id="d42d8-181">Luo uusi projekti</span><span class="sxs-lookup"><span data-stu-id="d42d8-181">Create a new project</span></span>

<span data-ttu-id="d42d8-182">Noudata seuraavia vaiheita luodaksesi uuden projektin LCS:ssä.</span><span class="sxs-lookup"><span data-stu-id="d42d8-182">To create a new project in LCS, follow these steps.</span></span>

1. <span data-ttu-id="d42d8-183">Luo projekti valitsemalla LCS-aloitussivulla plusmerkki (**+**).</span><span class="sxs-lookup"><span data-stu-id="d42d8-183">On the LCS home page, select the plus sign (**+**) to create a project.</span></span>
1. <span data-ttu-id="d42d8-184">Noudata oikeanpuoleisessa ruudussa jotakin näistä vaiheista:</span><span class="sxs-lookup"><span data-stu-id="d42d8-184">In the right pane, follow one of these steps:</span></span>

    - <span data-ttu-id="d42d8-185">Jos olet kumppani, valitse **Siirrä, luo ratkaisuja ja opi**.</span><span class="sxs-lookup"><span data-stu-id="d42d8-185">If you're a partner, select **Migrate, create solutions, and learn**.</span></span>
    - <span data-ttu-id="d42d8-186">Jos olet asiakas, valitse **Mahdolliset myyntiä edeltävät toimet**.</span><span class="sxs-lookup"><span data-stu-id="d42d8-186">If you're a customer, select **Prospective presales**.</span></span>

1. <span data-ttu-id="d42d8-187">Syötä mallin nimi, kuvaus ja toimiala.</span><span class="sxs-lookup"><span data-stu-id="d42d8-187">Enter a name, description, and industry.</span></span>
1. <span data-ttu-id="d42d8-188">Valitse **Tuotenimi** -kentässä **Dynamics 365 Retail**.</span><span class="sxs-lookup"><span data-stu-id="d42d8-188">In the **Product name** field, select **Dynamics 365 Retail**.</span></span>
1. <span data-ttu-id="d42d8-189">Valitse **Tuoteversio**-kentässä **Dynamics 365 Retail**.</span><span class="sxs-lookup"><span data-stu-id="d42d8-189">In the **Product version** field, select **Dynamics 365 Retail**.</span></span>
1. <span data-ttu-id="d42d8-190">Valitse **Metodologia**-kentässä **Dynamics Retail -implementointimetodologia**.</span><span class="sxs-lookup"><span data-stu-id="d42d8-190">In the **Methodology** field, select **Dynamics Retail implementation methodology**.</span></span>
1. <span data-ttu-id="d42d8-191">Valinnainen: Voit tuoda rooleja ja käyttäjiä aiemmin luodusta projektista.</span><span class="sxs-lookup"><span data-stu-id="d42d8-191">Optional: You can import roles and users from an existing project.</span></span>
1. <span data-ttu-id="d42d8-192">Valitse **Luo**.</span><span class="sxs-lookup"><span data-stu-id="d42d8-192">Select **Create**.</span></span> <span data-ttu-id="d42d8-193">Projektinäkymä avautuu.</span><span class="sxs-lookup"><span data-stu-id="d42d8-193">The project view appears.</span></span>

### <a name="add-the-azure-connector"></a><span data-ttu-id="d42d8-194">Azure-yhdistimen lisääminen</span><span class="sxs-lookup"><span data-stu-id="d42d8-194">Add the Azure Connector</span></span>

<span data-ttu-id="d42d8-195">Voit lisätä Azure-yhdistin LCS-projektiin noudattamalla seuraavia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="d42d8-195">To add the Azure Connector to your LCS project, follow these steps.</span></span>

1. <span data-ttu-id="d42d8-196">Noudata seuraavia ohjeita:</span><span class="sxs-lookup"><span data-stu-id="d42d8-196">Follow one of these steps:</span></span>

    - <span data-ttu-id="d42d8-197">Jos olet kumppani, valitse **Projektin asetukset** -ruutu oikeassa reunassa.</span><span class="sxs-lookup"><span data-stu-id="d42d8-197">If you're a partner, select the **Project settings** tile on the far right.</span></span>
    - <span data-ttu-id="d42d8-198">Jos olet asiakas, valitse ylävalikosta **Projektin asetukset**.</span><span class="sxs-lookup"><span data-stu-id="d42d8-198">If you're a customer, select **Project settings** on the top menu.</span></span>

1. <span data-ttu-id="d42d8-199">Valitse **Azure-yhdistimet**.</span><span class="sxs-lookup"><span data-stu-id="d42d8-199">Select **Azure connectors**.</span></span>
1. <span data-ttu-id="d42d8-200">Lisää Azure-yhdistin valitsemalla**Lisää**.</span><span class="sxs-lookup"><span data-stu-id="d42d8-200">Select **Add** to add the Azure Connector.</span></span>
1. <span data-ttu-id="d42d8-201">Kirjoita nimi.</span><span class="sxs-lookup"><span data-stu-id="d42d8-201">Enter a name.</span></span>
1. <span data-ttu-id="d42d8-202">Anna Azure-tilauksen tunnus.</span><span class="sxs-lookup"><span data-stu-id="d42d8-202">Enter your Azure subscription ID.</span></span>
1. <span data-ttu-id="d42d8-203">Ota **Määritä Azuren resurssienhallinta (ARM)** -valinta käyttöön.</span><span class="sxs-lookup"><span data-stu-id="d42d8-203">Turn on the **Configure to use Azure Resource Manager (ARM)** option.</span></span>
1. <span data-ttu-id="d42d8-204">Varmista, että **Azure-tilauksen AAD-vuokraajan toimialue (tai tunnus)** -arvo on määritetty oikein.</span><span class="sxs-lookup"><span data-stu-id="d42d8-204">Verify that the **Azure subscription AAD Tenant Domain (or ID)** value is correct.</span></span> <span data-ttu-id="d42d8-205">Ota tarvittaessa yhteys Azure-tilauksen järjestelmänvalvojaan.</span><span class="sxs-lookup"><span data-stu-id="d42d8-205">Consult your Azure subscription admin as required.</span></span>
1. <span data-ttu-id="d42d8-206">Valitse **Seuraava**.</span><span class="sxs-lookup"><span data-stu-id="d42d8-206">Select **Next**.</span></span>
1. <span data-ttu-id="d42d8-207">Noudata sivulle tulevia ohjeita ja myönnä tilaukselle tarvittavien sovellusten käyttöoikeudet.</span><span class="sxs-lookup"><span data-stu-id="d42d8-207">Follow the instructions on the page to grant the required applications access to your subscription.</span></span> <span data-ttu-id="d42d8-208">Ota tarvittaessa yhteys Azure-tilauksen järjestelmänvalvojaan.</span><span class="sxs-lookup"><span data-stu-id="d42d8-208">Consult your Azure subscription admin as required.</span></span>

    1. <span data-ttu-id="d42d8-209">Kirjaudu [Azure-portaalin osoitteessa](https://portal.azure.com/).</span><span class="sxs-lookup"><span data-stu-id="d42d8-209">Sign in to the [Azure portal](https://portal.azure.com/).</span></span>
    1. <span data-ttu-id="d42d8-210">Varmista, että oikea hakemisto on valittuna, ja valitse sitten vasemmalla olevasta valikosta **Tilaukset**.</span><span class="sxs-lookup"><span data-stu-id="d42d8-210">Make sure that the correct directory is selected, and then, on the menu on the left, select **Subscriptions**.</span></span>
    1. <span data-ttu-id="d42d8-211">Etsi oikea tilaus luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="d42d8-211">Find the correct subscription in the list, and select it.</span></span> <span data-ttu-id="d42d8-212">Käytä hakutoimintoa tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="d42d8-212">Use the search functionality as required.</span></span>
    1. <span data-ttu-id="d42d8-213">Valitse valikosta **Käytön valvonta (IAM)**.</span><span class="sxs-lookup"><span data-stu-id="d42d8-213">On the menu, select **Access control (IAM)**.</span></span>
    1. <span data-ttu-id="d42d8-214">Valitse **Lisää** oikealla olevassa **Lisää roolin määritys** -kohdassa.</span><span class="sxs-lookup"><span data-stu-id="d42d8-214">On the right, under **Add a role assignment**, select **Add**.</span></span> <span data-ttu-id="d42d8-215">**Lisää roolin määritys** -ruutu avautuu.</span><span class="sxs-lookup"><span data-stu-id="d42d8-215">The **Add role assignment** pane appears.</span></span>
    1. <span data-ttu-id="d42d8-216">Valitse **Rooli**-kentästä **Osallistuja**.</span><span class="sxs-lookup"><span data-stu-id="d42d8-216">In the **Role** field, select **Contributor**.</span></span>
    1. <span data-ttu-id="d42d8-217">Jätä **Määritä käyttöoikeus** -kenttään oletusarvo, **Azure AD -käyttäjä, ryhmä tai palvelun päätieto**.</span><span class="sxs-lookup"><span data-stu-id="d42d8-217">In the **Assign access to** field, leave the default value, **Azure AD user, group, or service principal**.</span></span>
    1. <span data-ttu-id="d42d8-218">Syötä **Valitse**-kohtaan **b96b7e94-b82e-4e71-99a0-cf7fb188acea**.</span><span class="sxs-lookup"><span data-stu-id="d42d8-218">Under **Select**, enter **b96b7e94-b82e-4e71-99a0-cf7fb188acea**.</span></span>
    1. <span data-ttu-id="d42d8-219">Valitse luettelosta **Dynamics-käyttöönoton palvelut Services \[käytössä wsfed\]**.</span><span class="sxs-lookup"><span data-stu-id="d42d8-219">Select **Dynamics Deployment Services \[wsfed-enabled\]** in the list.</span></span>
    1. <span data-ttu-id="d42d8-220">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="d42d8-220">Select **Save**.</span></span>

1. <span data-ttu-id="d42d8-221">Valitse **Seuraava**.</span><span class="sxs-lookup"><span data-stu-id="d42d8-221">Select **Next**.</span></span>
1. <span data-ttu-id="d42d8-222">Noudata sivulle tulevia ohjeita ja myönnä tilaukselle tarvittavien sovellusten käyttöoikeudet.</span><span class="sxs-lookup"><span data-stu-id="d42d8-222">Follow the instructions on the page to grant the required applications access to your subscription.</span></span> <span data-ttu-id="d42d8-223">Ota tarvittaessa yhteys Azure-tilauksen järjestelmänvalvojaan.</span><span class="sxs-lookup"><span data-stu-id="d42d8-223">Consult your Azure subscription admin as required.</span></span>
1. <span data-ttu-id="d42d8-224">Valitse **Seuraava**.</span><span class="sxs-lookup"><span data-stu-id="d42d8-224">Select **Next**.</span></span>
1. <span data-ttu-id="d42d8-225">Valitse **Azure-alue**-kohdassa **Itä-Yhdysvallat**, **Itä-Yhdysvallat 2**, **Länsi-Yhdysvallat** tai **Länsi-Yhdysvallat 2**.</span><span class="sxs-lookup"><span data-stu-id="d42d8-225">In the **Azure region** field, select **East US**, **East US 2**, **West US**, or **West US 2**.</span></span>
1. <span data-ttu-id="d42d8-226">Valitse **Yhdistä**.</span><span class="sxs-lookup"><span data-stu-id="d42d8-226">Select **Connect**.</span></span> <span data-ttu-id="d42d8-227">Azure-yhdistin näkyy luettelossa.</span><span class="sxs-lookup"><span data-stu-id="d42d8-227">Your Azure Connector should appear in the list.</span></span>

### <a name="import-the-commerce-preview-demo-base-extension"></a><span data-ttu-id="d42d8-228">Tuo Commerce Preview -esittelyalustan laajennus</span><span class="sxs-lookup"><span data-stu-id="d42d8-228">Import the Commerce Preview Demo Base Extension</span></span>

<span data-ttu-id="d42d8-229">Voit tuoda Commerce Preview-demokannan laajennuksen projektiin noudattamalla seuraavia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="d42d8-229">To import the Commerce Preview Demo Base Extension into your project, follow these steps.</span></span>

1. <span data-ttu-id="d42d8-230">Avaa projektin kotisivu valitsemalla projektin nimi yläreunassa.</span><span class="sxs-lookup"><span data-stu-id="d42d8-230">Open the home page for your project by selecting the project name at the top.</span></span>
1. <span data-ttu-id="d42d8-231">Noudata seuraavia ohjeita:</span><span class="sxs-lookup"><span data-stu-id="d42d8-231">Follow one of these steps:</span></span>

    - <span data-ttu-id="d42d8-232">Jos olet kumppani, valitse **Omaisuuskirjasto** -ruutu oikeassa reunassa.</span><span class="sxs-lookup"><span data-stu-id="d42d8-232">If you're a partner, select the **Asset library** tile on the far right.</span></span>
    - <span data-ttu-id="d42d8-233">Jos olet asiakas, valitse ylävalikosta **Omaisuuskirjasto**.</span><span class="sxs-lookup"><span data-stu-id="d42d8-233">If you're a customer, select **Asset library** on the top menu.</span></span>

1. <span data-ttu-id="d42d8-234">Valitse vasemmalla olevasta luettelosta **Käyttöönotettava ohjelmistopaketti**.</span><span class="sxs-lookup"><span data-stu-id="d42d8-234">In the list on the left, select **Software deployable package**.</span></span>
1. <span data-ttu-id="d42d8-235">Valitse **Tuo**.</span><span class="sxs-lookup"><span data-stu-id="d42d8-235">Select **Import**.</span></span>
1. <span data-ttu-id="d42d8-236">Valitse **Commerce Preview -esittelyn peruslaajennus** **Jaettu resurssikirjasto** -kohdan resurssiluettelosta.</span><span class="sxs-lookup"><span data-stu-id="d42d8-236">Under **Shared asset library**, select **Commerce Preview Demo Base Extension** in the list of assets.</span></span>
1. <span data-ttu-id="d42d8-237">Valitse **Kerää**.</span><span class="sxs-lookup"><span data-stu-id="d42d8-237">Select **Pick**.</span></span> <span data-ttu-id="d42d8-238">Sinut siirretään resurssikirjastoon ja laajennuksen tulisi näkyä luettelossa.</span><span class="sxs-lookup"><span data-stu-id="d42d8-238">You're returned to the Asset library, and you should see the extension in the list.</span></span>

<span data-ttu-id="d42d8-239">Seuraavassa kuvassa näkyvät toiminnot, jotka on tehtävä LCS-**resurssikirjasto**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="d42d8-239">The following illustration shows the actions that must be taken on the LCS **Asset library** page.</span></span>

![Commerce Preview -esittelyalustan laajennuksen tuominen](./media/import.png)

### <a name="deploy-the-environment"></a><span data-ttu-id="d42d8-241">Käyttöönottoympäristö</span><span class="sxs-lookup"><span data-stu-id="d42d8-241">Deploy the environment</span></span>

<span data-ttu-id="d42d8-242">Määritä ympäristö näiden ohjeiden avulla.</span><span class="sxs-lookup"><span data-stu-id="d42d8-242">To deploy the environment, follow these steps.</span></span>

> [!NOTE]
> <span data-ttu-id="d42d8-243">Vaiheita 6, 7 ja/tai 8 ei ehkä tarvitse suorittaa, koska sivut, joilla on yksi vaihtoehto, ohitetaan.</span><span class="sxs-lookup"><span data-stu-id="d42d8-243">You might not have to complete steps 6, 7, and/or 8, because pages that have a single option are skipped.</span></span> <span data-ttu-id="d42d8-244">Kun olet **Ympäristön parametrit** -näkymässä, varmista, että teksti **Dynamics 365 Commerce (esikatselu) - esittely (10.0.6 ja Platform-päivitys 30)** näkyy suoraan **Ympäristön nimi** -kentän yläpuolella.</span><span class="sxs-lookup"><span data-stu-id="d42d8-244">When you're in the **Environment parameters** view, confirm that the text **Dynamics 365 Commerce (Preview) - Demo (10.0.6 with Platform update 30)** appears directly above the **Environment name** field.</span></span> <span data-ttu-id="d42d8-245">Katso vaiheen 8 jälkeen näkyvää kuvaa.</span><span class="sxs-lookup"><span data-stu-id="d42d8-245">See the illustration that appears after step 8.</span></span>

1. <span data-ttu-id="d42d8-246">Valitse päävalikosta **Pilvipalveluympäristöt**.</span><span class="sxs-lookup"><span data-stu-id="d42d8-246">On the top menu, select **Cloud-hosted environments**.</span></span>
1. <span data-ttu-id="d42d8-247">Valitse **+ Lisää** lisätäksesi ympäristön.</span><span class="sxs-lookup"><span data-stu-id="d42d8-247">Select **Add** to add an environment.</span></span>
1. <span data-ttu-id="d42d8-248">Valitse **Tuoteversio**-kentässä **10.0.6**.</span><span class="sxs-lookup"><span data-stu-id="d42d8-248">In the **Application version** field, select **10.0.6**.</span></span>
1. <span data-ttu-id="d42d8-249">Valitse **Ympäristön versio** -kentässä **Platform Update 30**.</span><span class="sxs-lookup"><span data-stu-id="d42d8-249">In the **Platform version** field, select **Platform Update 30**.</span></span>

    ![Sovelluksen ja ympäristön versioiden valitseminen](./media/project1.png)

1. <span data-ttu-id="d42d8-251">Valitse **Seuraava**.</span><span class="sxs-lookup"><span data-stu-id="d42d8-251">Select **Next**.</span></span>
1. <span data-ttu-id="d42d8-252">Valitse **Esittely** ympäristötopologiaksi.</span><span class="sxs-lookup"><span data-stu-id="d42d8-252">Select **Demo** as the environment topology.</span></span>

    ![Ympäristötopologia 1 valitseminen](./media/project2.png)

1. <span data-ttu-id="d42d8-254">Valitse **Dynamics 365 Commerce (Esikatselu) - Esittely** ympäristötopologiaksi.</span><span class="sxs-lookup"><span data-stu-id="d42d8-254">Select **Dynamics 365 Commerce (Preview) - Demo** as the environment topology.</span></span> <span data-ttu-id="d42d8-255">Jos olet määrittänyt aiemmin yhden Azure-yhdistimen, sitä käytetään tässä ympäristössä.</span><span class="sxs-lookup"><span data-stu-id="d42d8-255">If you configured a single Azure Connector earlier, it will be used for this environment.</span></span> <span data-ttu-id="d42d8-256">Jos olet määrittänyt useita Azure-yhdistimiä, voit valita käytettävän yhdistimen: **Itä-Yhdysvallat**, **Itä-Yhdysvallat 2**, **Länsi-Yhdysvallat**tai **Länsi-Yhdysvallat 2**.</span><span class="sxs-lookup"><span data-stu-id="d42d8-256">If you configured multiple Azure Connectors, you can select which connector to use: **East US**, **East US 2**, **West US**, or **West US 2**.</span></span> <span data-ttu-id="d42d8-257">(Parhaan päästä päähän-suorituskyvyn saavuttamiseksi suosittelemme valitsemaan **Länsi-Yhdysvallat 2**.)</span><span class="sxs-lookup"><span data-stu-id="d42d8-257">(For the best end-to-end performance, we recommend that you select **West US 2**.)</span></span>

    ![Ympäristötopologia 2 valitseminen](./media/project3.png)

1. <span data-ttu-id="d42d8-259">Anna ympäristön nimi **Ympäristön käyttöönotto** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="d42d8-259">On the **Deploy environment** page, enter an environment name.</span></span> <span data-ttu-id="d42d8-260">Älä muuta Lisäasetukset-kohtaa.</span><span class="sxs-lookup"><span data-stu-id="d42d8-260">Leave the advanced settings as they are.</span></span>

    ![Ympäristön käyttöönotto -sivu](./media/project4.png)

1. <span data-ttu-id="d42d8-262">Säädä VM:n kokoa tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="d42d8-262">Adjust the VM size as required.</span></span> <span data-ttu-id="d42d8-263">(Suosittelemme VM:n varastointiyksikköä \[SKU\] **D13 v2**.)</span><span class="sxs-lookup"><span data-stu-id="d42d8-263">(We recommend VM stock keeping unit \[SKU\] **D13 v2**.)</span></span>
1. <span data-ttu-id="d42d8-264">Tarkista hinnoittelu- ja lisensointiehdot ja valitse sitten valintaruutu, jos hyväksyt ne.</span><span class="sxs-lookup"><span data-stu-id="d42d8-264">Review the pricing and licensing terms, and then select the check box to indicate that you agree to them.</span></span>
1. <span data-ttu-id="d42d8-265">Valitse **Seuraava**.</span><span class="sxs-lookup"><span data-stu-id="d42d8-265">Select **Next**.</span></span>
1. <span data-ttu-id="d42d8-266">Kun tietojen oikeellisuus on vahvistettu käyttöönoton vahvistussivulla, valitse **Ota käyttöön**.</span><span class="sxs-lookup"><span data-stu-id="d42d8-266">On the deployment confirmation page, verify that the details are correct, and then select **Deploy**.</span></span> <span data-ttu-id="d42d8-267">Sinut siirretään **Pilvipalveluympäristöt**-näkymään ja ympäristösi pitäisi näkyä luettelossa.</span><span class="sxs-lookup"><span data-stu-id="d42d8-267">You're returned to the **Cloud-hosted environments** view, and your environment should appear in the list.</span></span>

    <span data-ttu-id="d42d8-268">Pyydetty ympäristö näkyy jonossa. Tämän jälkeen se otetaan käyttöön.</span><span class="sxs-lookup"><span data-stu-id="d42d8-268">Your requested environment will appear as queued and then deploying.</span></span> <span data-ttu-id="d42d8-269">Ympäristön työnkulut kestävät jonkin aikaa.</span><span class="sxs-lookup"><span data-stu-id="d42d8-269">The environment workflows will take some time to be completed.</span></span> <span data-ttu-id="d42d8-270">Tarkista tilanne, kun aikaa on kulunut noin kuudesta yhdeksään tuntiin.</span><span class="sxs-lookup"><span data-stu-id="d42d8-270">Therefore, check back after approximately six to nine hours.</span></span>

1. <span data-ttu-id="d42d8-271">Varmista ennen jatkamista, että ympäristösi tila on **Otettu käyttöön**.</span><span class="sxs-lookup"><span data-stu-id="d42d8-271">Before you continue, make sure that the status of your environment is **Deployed**.</span></span>

### <a name="initialize-rcsu"></a><span data-ttu-id="d42d8-272">RCSU:n alustaminen</span><span class="sxs-lookup"><span data-stu-id="d42d8-272">Initialize RCSU</span></span>

<span data-ttu-id="d42d8-273">Alusta RCSU-osoite seuraavien ohjeiden avulla.</span><span class="sxs-lookup"><span data-stu-id="d42d8-273">To initialize RCSU, follow these steps.</span></span>

1. <span data-ttu-id="d42d8-274">Valitse **Pilvipalveluympäristöt**-näkymässä luettelosta ympäristösi.</span><span class="sxs-lookup"><span data-stu-id="d42d8-274">In the **Cloud-hosted environments** view, select your environment in the list.</span></span>
1. <span data-ttu-id="d42d8-275">Valitse oikealla olevasta ympäristön näkymästä **Täydet tiedot**.</span><span class="sxs-lookup"><span data-stu-id="d42d8-275">In the environment view on the right, select **Full details**.</span></span> <span data-ttu-id="d42d8-276">Näkyviin tulee ympäristön tietojen näkymä.</span><span class="sxs-lookup"><span data-stu-id="d42d8-276">The environment details view appears.</span></span>
1. <span data-ttu-id="d42d8-277">Valitse **Ympäristön ominaisuudet** -kohdassa **Hallitse**.</span><span class="sxs-lookup"><span data-stu-id="d42d8-277">Under **Environment features**, select **Manage**.</span></span>
1. <span data-ttu-id="d42d8-278">Valitse **Vähittäismyynti**-välilehdestä **Alusta**.</span><span class="sxs-lookup"><span data-stu-id="d42d8-278">On the **Retail** tab, select **Initialize**.</span></span> <span data-ttu-id="d42d8-279">Näkyviin tulee RCSU-alustusparametrien näkymä.</span><span class="sxs-lookup"><span data-stu-id="d42d8-279">The RCSU initialization parameters view appears.</span></span>
1. <span data-ttu-id="d42d8-280">Valitse **Alue**-kohdassa **Itä-Yhdysvallat**, **Itä-Yhdysvallat 2**, **Länsi-Yhdysvallat** tai **Länsi-Yhdysvallat 2**.</span><span class="sxs-lookup"><span data-stu-id="d42d8-280">In the **Region** field, select **East US**, **East US 2**, **West US**, or **West US 2**.</span></span>
1. <span data-ttu-id="d42d8-281">Valitse **Versio**-kentässä **Määritä versio** -luettelosta ja määritä sitten **9.16.19262.5** näyttöön tulevassa kentässä.</span><span class="sxs-lookup"><span data-stu-id="d42d8-281">In the **Version** field, select **Specify a version** in the list, and then specify **9.16.19262.5** in the field that appears.</span></span> <span data-ttu-id="d42d8-282">Muista määrittää tarkka versio, joka on ilmoitettu tässä.</span><span class="sxs-lookup"><span data-stu-id="d42d8-282">Be sure to specify the exact version that is indicated here.</span></span> <span data-ttu-id="d42d8-283">Muussa tapauksessa sinun on päivitettävä RCSU oikeaan versioon myöhemmin.</span><span class="sxs-lookup"><span data-stu-id="d42d8-283">Otherwise, you will have to update RCSU to the correct version later.</span></span>
1. <span data-ttu-id="d42d8-284">Ota käyttöön **Laajennuksen käyttäminen** -vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="d42d8-284">Turn on the **Apply extension** option.</span></span>
1. <span data-ttu-id="d42d8-285">Valitse laajennusluettelosta **Commerce Preview -esittelyn peruslaajennus**.</span><span class="sxs-lookup"><span data-stu-id="d42d8-285">In the list of extensions, select **Commerce Preview Demo Base Extension**.</span></span>
1. <span data-ttu-id="d42d8-286">Valitse **Alusta**.</span><span class="sxs-lookup"><span data-stu-id="d42d8-286">Select **Initialize**.</span></span>
1. <span data-ttu-id="d42d8-287">Kun tietojen oikeellisuus on vahvistettu käyttöönoton vahvistussivulla, valitse **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="d42d8-287">On the deployment confirmation page, verify that the details are correct, and then select **Yes**.</span></span> <span data-ttu-id="d42d8-288">Palaat **Vähittäismyynnin hallinta** -näkymään, jossa on valittuna **Vähittäismyynti**-välilehti.</span><span class="sxs-lookup"><span data-stu-id="d42d8-288">You're returned to the **Retail management** view, where the **Retail** tab is selected.</span></span> <span data-ttu-id="d42d8-289">RCSU on asetettu jonoon valmistelua varten.</span><span class="sxs-lookup"><span data-stu-id="d42d8-289">Your RCSU has been queued for provisioning.</span></span>
1. <span data-ttu-id="d42d8-290">Varmista ennen jatkamista, että RCSU:si tila on **Onnistunut**.</span><span class="sxs-lookup"><span data-stu-id="d42d8-290">Before you continue, make sure that the status of your RCSU is **Success**.</span></span> <span data-ttu-id="d42d8-291">Alustus kestää noin kahdesta viiteen tuntia.</span><span class="sxs-lookup"><span data-stu-id="d42d8-291">Initialization takes approximately two to five hours.</span></span>

### <a name="initialize-e-commerce"></a><span data-ttu-id="d42d8-292">Sähköisen kaupankäynnin alustaminen</span><span class="sxs-lookup"><span data-stu-id="d42d8-292">Initialize e-Commerce</span></span>

<span data-ttu-id="d42d8-293">Alusta sähköinen kaupankäynti seuraavien ohjeiden avulla.</span><span class="sxs-lookup"><span data-stu-id="d42d8-293">To initialize e-Commerce, follow these steps.</span></span>

1. <span data-ttu-id="d42d8-294">Tarkista esikatselun suostumus **sähköisen kaupankäynnin (esikatselu)**-välilehdestä ja valitse sitten **Asetukset**.</span><span class="sxs-lookup"><span data-stu-id="d42d8-294">On the **e-Commerce (Preview)** tab, review the preview consent, and then select **Setup**.</span></span>
1. <span data-ttu-id="d42d8-295">Kirjoita **Sähköisen kaupankäynnin vuokraajan nimi** -kenttään nimi.</span><span class="sxs-lookup"><span data-stu-id="d42d8-295">In the **e-Commerce tenant name** field, enter a name.</span></span> <span data-ttu-id="d42d8-296">Ota huomioon, että tämä nimi näkyy joissakin sähköisen kaupankäynnin esiintymään vievissä URL-osoitteissa.</span><span class="sxs-lookup"><span data-stu-id="d42d8-296">However, be aware that this name will appear in some of the URLs that point to your e-Commerce instance.</span></span>
1. <span data-ttu-id="d42d8-297">Valitse **Retail Cloud Scale -yksikön nimi** -kentässä RCSU-luettelosta.</span><span class="sxs-lookup"><span data-stu-id="d42d8-297">In the **Retail cloud scale unit name** field, select your RCSU in the list.</span></span> <span data-ttu-id="d42d8-298">(Luettelossa pitäisi olla vain yksi vaihtoehto.)</span><span class="sxs-lookup"><span data-stu-id="d42d8-298">(The list should have only one option.)</span></span>

    <span data-ttu-id="d42d8-299">**Sähköisen kaupankäynnin paikkatieto** -kenttä määritetään automaattisesti, eikä arvoa voi muuttaa.</span><span class="sxs-lookup"><span data-stu-id="d42d8-299">The **e-Commerce geography** field is set automatically, and the value can't be changed.</span></span>

1. <span data-ttu-id="d42d8-300">Jatka valitsemalla **Seuraava**.</span><span class="sxs-lookup"><span data-stu-id="d42d8-300">Select **Next** to continue.</span></span>
1. <span data-ttu-id="d42d8-301">Kirjoita **Tuetut isäntänimet** -kenttään mikä tahansa kelvollinen toimialue, kuten `www.fabrikam.com`.</span><span class="sxs-lookup"><span data-stu-id="d42d8-301">In the **Supported host names** field, enter any valid domain, such as `www.fabrikam.com`.</span></span>
1.  <span data-ttu-id="d42d8-302">**AAD-suojausryhmän järjestelmänhallinta** -kenttään, kirjoita haluamasi käyttöoikeusryhmän nimen muutama ensimmäinen kirjain.</span><span class="sxs-lookup"><span data-stu-id="d42d8-302">In the **AAD security group for system admin** field, enter the first few letters of the name of the security group that you want to use.</span></span> <span data-ttu-id="d42d8-303">Tuo hakutulokset näkyviin valitsemalla suurennuslasikuvake.</span><span class="sxs-lookup"><span data-stu-id="d42d8-303">Select the magnifying class icon to display the search results.</span></span> <span data-ttu-id="d42d8-304">Valitse luettelosta suojausryhmä.</span><span class="sxs-lookup"><span data-stu-id="d42d8-304">Select a security group from the list.</span></span>
2.  <span data-ttu-id="d42d8-305">**AAD-turvallisuusryhmä luokituksille ja arvosteluvalvoja** -kenttään, kirjoita haluamasi käyttöoikeusryhmän nimen muutama ensimmäinen kirjain.</span><span class="sxs-lookup"><span data-stu-id="d42d8-305">In the **AAD security group for ratings and review moderator** field, enter the first few letters of the name of the security group that you want to use.</span></span> <span data-ttu-id="d42d8-306">Tuo hakutulokset näkyviin valitsemalla suurennuslasikuvake.</span><span class="sxs-lookup"><span data-stu-id="d42d8-306">Select the magnifying class icon to display the search results.</span></span> <span data-ttu-id="d42d8-307">Valitse luettelosta suojausryhmä.</span><span class="sxs-lookup"><span data-stu-id="d42d8-307">Select a security group from the list.</span></span>
1. <span data-ttu-id="d42d8-308">Jätä **Ota luokitukset ja arvostelut -palvelu käyttöön** -asetus päälle.</span><span class="sxs-lookup"><span data-stu-id="d42d8-308">Leave the **Enable ratings and review service** option turned on.</span></span>
1. <span data-ttu-id="d42d8-309">Jos olet jo suorittanut Microsoft Azure Active Directoryn (Azure AD) suostumusvaiheen, joka on kuvattu kohdassa Myönnä käyttöoikeudet verkkokaupan sovelluksiin, valitse valintaruutu vahvistaaksesi suostumuksesi.</span><span class="sxs-lookup"><span data-stu-id="d42d8-309">If you have already completed the Microsoft Azure Active Directory (Azure AD) consent step as described in the "Grant access to e-Commerce applications" section, select the check box to confirm your consent.</span></span> <span data-ttu-id="d42d8-310">Jos et ole vielä suorittanut tätä vaihetta, sinun on tehtävä se ennen alustuksen jatkamista.</span><span class="sxs-lookup"><span data-stu-id="d42d8-310">If you have not yet completed this step, you need to do that before proceeding with the initialization.</span></span> <span data-ttu-id="d42d8-311">Avaa suostumus-valintaikkuna ja suorita vaihe valitsemalla valintaruudun vieressä olevassa tekstissä oleva linkki.</span><span class="sxs-lookup"><span data-stu-id="d42d8-311">Select the link within the text next to the check box to open the consent dialog box and complete the step.</span></span>
1. <span data-ttu-id="d42d8-312">Valitse **Alusta**.</span><span class="sxs-lookup"><span data-stu-id="d42d8-312">Select **Initialize**.</span></span> <span data-ttu-id="d42d8-313">Palaat **Vähittäismyynnin hallinta** -näkymään, jossa on valittuna **Sähköinen kaupankäynti (esiversio)**-välilehti.</span><span class="sxs-lookup"><span data-stu-id="d42d8-313">You're returned to the **Retail management** view, where the **e-Commerce (Preview)** tab is selected.</span></span> <span data-ttu-id="d42d8-314">Sähköisen kaupankäynnin alustaminen on aloitettu.</span><span class="sxs-lookup"><span data-stu-id="d42d8-314">E-Commerce initialization has started.</span></span>
1. <span data-ttu-id="d42d8-315">Ennen kuin jatkat, odota, kunnes sähköisen kaupankäynnin alustamisen tila on **Alustaminen onnistui**.</span><span class="sxs-lookup"><span data-stu-id="d42d8-315">Before you continue, wait until the status of e-Commerce initialization is **Initialization successful**.</span></span>
1. <span data-ttu-id="d42d8-316">Merkitse oikeassa alakulmassa olevassa **Linkit**-kohdassa seuraavien linkkien URL-osoitteet:</span><span class="sxs-lookup"><span data-stu-id="d42d8-316">Under **Links** in the lower right, make a note of the URLs for the following links:</span></span>

    * <span data-ttu-id="d42d8-317">**Sähköisen kaupankäynnin sivusto** – linkki verkkokaupan sivustosi juureen.</span><span class="sxs-lookup"><span data-stu-id="d42d8-317">**e-Commerce site** – The link to the root of your e-Commerce site.</span></span>
    * <span data-ttu-id="d42d8-318">**Sähköisen kaupankäynnin hallintatyökalu** – linkki sivuston hallintatyökaluun.</span><span class="sxs-lookup"><span data-stu-id="d42d8-318">**e-Commerce site management tool** – The link to the site management tool.</span></span>

## <a name="commerce-preview-environment-support"></a><span data-ttu-id="d42d8-319">Commercen esikatseluympäristön tuki</span><span class="sxs-lookup"><span data-stu-id="d42d8-319">Commerce preview environment support</span></span>

<span data-ttu-id="d42d8-320">Jos valmisteluvaiheiden suorittamisen aikana on ongelmia, saat apua [Microsoft Dynamics 365 Commerce Preview Yammer -ryhmästä](https://aka.ms/Dynamics365CommercePreviewYammer).</span><span class="sxs-lookup"><span data-stu-id="d42d8-320">If you experience issues while you're completing the provisioning steps, visit the [Microsoft Dynamics 365 Commerce Preview Yammer group](https://aka.ms/Dynamics365CommercePreviewYammer) for help.</span></span>

<span data-ttu-id="d42d8-321">Jos kohtaat ongelmia yrittäessäsi käyttää Yammer-ryhmää, voit ottaa yhteyttä Microsoftiin sähköpostitse osoitteella <Dynamics365Commerce@microsoft.com>.</span><span class="sxs-lookup"><span data-stu-id="d42d8-321">If you experience issues when you try to access the Yammer group, you can contact Microsoft by email at <Dynamics365Commerce@microsoft.com>.</span></span> <span data-ttu-id="d42d8-322">Tätä sähköpostiosoitetta ei seurata aktiivisesti.</span><span class="sxs-lookup"><span data-stu-id="d42d8-322">This email address isn't actively monitored.</span></span> <span data-ttu-id="d42d8-323">Varaudu viiveeseen vastausta odottaessasi.</span><span class="sxs-lookup"><span data-stu-id="d42d8-323">Therefore, expect a delay in the response.</span></span>

## <a name="next-steps"></a><span data-ttu-id="d42d8-324">Seuraavat vaiheet</span><span class="sxs-lookup"><span data-stu-id="d42d8-324">Next steps</span></span>

<span data-ttu-id="d42d8-325">Jatkaaksesi käyttöönotto- ja määritysprosessia Commercen esikatseluympäristön määrittelystä, katso [Commercen esikatseluympäristön määrittäminen](cpe-post-provisioning.md).</span><span class="sxs-lookup"><span data-stu-id="d42d8-325">To continue the process of provisioning and configuring your Commerce preview environment, see [Configure a Commerce preview environment](cpe-post-provisioning.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d42d8-326">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="d42d8-326">Additional resources</span></span>

[<span data-ttu-id="d42d8-327">Commercen esikatseluympäristön yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="d42d8-327">Commerce preview environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="d42d8-328">Commercen esikatseluympäristön määrittäminen</span><span class="sxs-lookup"><span data-stu-id="d42d8-328">Configure a Commerce preview environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="d42d8-329">Valinnaisten ominaisuuksien määrittäminen Commercen esikatseluympäristöä varten</span><span class="sxs-lookup"><span data-stu-id="d42d8-329">Configure optional features for a Commerce preview environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="d42d8-330">Commercen esikatseluympäristön usein kysytyt kysymykset</span><span class="sxs-lookup"><span data-stu-id="d42d8-330">Commerce preview environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="d42d8-331">Microsoft Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="d42d8-331">Microsoft Lifecycle Services (LCS)</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="d42d8-332">Retail Cloud Scale Unit (RCSU)</span><span class="sxs-lookup"><span data-stu-id="d42d8-332">Retail Cloud Scale Unit (RCSU)</span></span>](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="d42d8-333">Microsoft Azure -portaali</span><span class="sxs-lookup"><span data-stu-id="d42d8-333">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="d42d8-334">Dynamics 365 Commerce -sivusto</span><span class="sxs-lookup"><span data-stu-id="d42d8-334">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)

[<span data-ttu-id="d42d8-335">Dynamics 365 Retailin ohjeresurssit</span><span class="sxs-lookup"><span data-stu-id="d42d8-335">Help resources for Dynamics 365 Retail</span></span>](../retail/index.md)
