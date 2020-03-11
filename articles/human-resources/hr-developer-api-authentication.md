---
title: Todennus
description: ''
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 025feca31eed8649bc319a1e1a1b6d1af3ddb128
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008932"
---
# <a name="authentication"></a><span data-ttu-id="af1d9-102">Todennus</span><span class="sxs-lookup"><span data-stu-id="af1d9-102">Authentication</span></span>

<span data-ttu-id="af1d9-103">Tässä artikkelissa on yleistietoja käyttöoikeuksien todennuksesta Microsoft Dynamics 365 Human Resourcesin datasovelluksen ohjelmointirajapinnasta.</span><span class="sxs-lookup"><span data-stu-id="af1d9-103">This article provides overview information about how to authenticate with the Microsoft Dynamics 365 Human Resources data application programming interface (API).</span></span>

## <a name="overview"></a><span data-ttu-id="af1d9-104">Yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="af1d9-104">Overview</span></span>

<span data-ttu-id="af1d9-105">Henkilöresurssien dataohjelmointirajapinta on OData-toteutus.</span><span class="sxs-lookup"><span data-stu-id="af1d9-105">The data API for Human Resources is an OData implementation.</span></span> <span data-ttu-id="af1d9-106">Lisätietoja on kohdassa [Open Data Protocol (OData)](../fin-ops-core/dev-itpro/data-entities/odata.md).</span><span class="sxs-lookup"><span data-stu-id="af1d9-106">For more information, see [Open Data Protocol (OData)](../fin-ops-core/dev-itpro/data-entities/odata.md).</span></span>

<span data-ttu-id="af1d9-107">Sovellus on todennettava valtuutettuna soittajana, ennen kuin ohjelmointirajapintapalvelu hakee sovelluspyyntöjä.</span><span class="sxs-lookup"><span data-stu-id="af1d9-107">Your application must authenticate as an authorized caller before the API will service requests from your application.</span></span>

## <a name="fundamentals"></a><span data-ttu-id="af1d9-108">Perusteet</span><span class="sxs-lookup"><span data-stu-id="af1d9-108">Fundamentals</span></span>

<span data-ttu-id="af1d9-109">Jotta voisit soittaa dataohjelmointirajapintaliittymään, sovelluksen on hankittava käyttötunnus Microsoftin käyttäjätietoympäristöstä.</span><span class="sxs-lookup"><span data-stu-id="af1d9-109">To call the data API, your application must acquire an access token from the Microsoft identity platform.</span></span> <span data-ttu-id="af1d9-110">Käyttötunnussanoma sisältää sovelluksen tiedot sekä käyttöoikeudet, jotka sen on kutsuttava henkilöstöhallintaan.</span><span class="sxs-lookup"><span data-stu-id="af1d9-110">The access token contains information about your application and the permission that it has to call resources in Human Resources.</span></span>

### <a name="access-token"></a><span data-ttu-id="af1d9-111">Käyttöoikeustietue</span><span class="sxs-lookup"><span data-stu-id="af1d9-111">Access token</span></span>

<span data-ttu-id="af1d9-112">Microsoftin käyttäjätietoympäristön myöntämiä käyttöoikeustunnuksia ovat base64 -koodatut JavaScript Object Notation (JSON) -webtunnukset (JWT).</span><span class="sxs-lookup"><span data-stu-id="af1d9-112">Access tokens issued by the Microsoft identity platform are base64–encoded JavaScript Object Notation (JSON) Web Tokens (JWTs).</span></span> <span data-ttu-id="af1d9-113">Ne sisältävät tietoja (väitteitä), joiden mukaan dataohjelmointirajapinta (ja muut Internet-ohjelmointirajapintaliittymät, jotka on suojattu Microsoftin käyttäjätietoympäristöalustalla) käyttää vahvistukseen soittajaa ja varmistaa, että kutsujalla on oikeat käyttöoikeudet pyytämiensä toimintojen suorittamiseen.</span><span class="sxs-lookup"><span data-stu-id="af1d9-113">They contain information (claims) that the data API (and other web APIs that are secured by the Microsoft identity platform) use to validate the caller and make sure that the caller has the correct permissions to perform the operation they're requesting.</span></span> <span data-ttu-id="af1d9-114">Puheluissa voit käsitellä käyttötunnuksia läpinäkymättöminä.</span><span class="sxs-lookup"><span data-stu-id="af1d9-114">During calls, you can treat access tokens as opaque.</span></span> <span data-ttu-id="af1d9-115">Siirtotunnukset on aina lähetettävä suojatun kanavan kautta, esimerkiksi Transport Layer Security (TLS) - ja Hypertext Transfer Protocol Secure (HTTPS) -protokollan avulla.</span><span class="sxs-lookup"><span data-stu-id="af1d9-115">You should always transmit access tokens over a secure channel, such as Transport Layer Security (TLS) and Hypertext Transfer Protocol Secure (HTTPS).</span></span>

<span data-ttu-id="af1d9-116">Tässä on esimerkki Microsoftin käyttäjätietoympäristön myöntämästä käyttöoikeustunnuksesta.</span><span class="sxs-lookup"><span data-stu-id="af1d9-116">Here is an example of an access token that is issued by the Microsoft identity platform.</span></span>

```jwt
EwAoA8l6BAAU7p9QDpi/D7xJLwsTgCg3TskyTaQAAXu71AU9f4aS4rOK5xoO/SU5HZKSXtCsDe0Pj7uSc5Ug008qTI+a9M1tBeKoTs7tHzhJNSKgk7pm5e8d3oGWXX5shyOG3cKSqgfwuNDnmmPDNDivwmi9kmKqWIC9OQRf8InpYXH7NdUYNwN+jljffvNTewdZz42VPrvqoMH7hSxiG7A1h8leOv4F3Ek/oeJX6U8nnL9nJ5pHLVuPWD0aNnTPTJD8Y4oQTp5zLhDIIfaJCaGcQperULVF7K6yX8MhHxIBwek418rKIp11om0SWBXOYSGOM0rNNN59qNiKwLNK+MPUf7ObcRBN5I5vg8jB7IMoz66jrNmT2uiWCyI8MmYDZgAACPoaZ9REyqke+AE1/x1ZX0w7OamUexKF8YGZiw+cDpT/BP1GsONnwI4a8M7HsBtDgZPRd6/Hfqlq3HE2xLuhYX8bAc1MUr0gP9KuH6HDQNlIV4KaRZWxyRo1wmKHOF5G5wTHrtxg8tnXylMc1PKOtaXIU4JJZ1l4x/7FwhPmg9M86PBPWr5zwUj2CVXC7wWlL/6M89Mlh8yXESMO3AIuAmEMKjqauPrgi9hAdI2oqnLZWCRL9gcHBida1y0DTXQhcwMv1ORrk65VFHtVgYAegrxu3NDoJiDyVaPZxDwTYRGjPII3va8GALAMVy5xou2ikzRvJjW7Gm3XoaqJCTCExN4m5i/Dqc81Gr4uT7OaeypYTUjnwCh7aMhsOTDJehefzjXhlkn//2eik+NivKx/BTJBEdT6MR97Wh/ns/VcK7QTmbjwbU2cwLngT7Ylq+uzhx54R9JMaSLhnw+/nIrcVkG77Hi3neShKeZmnl5DC9PuwIbtNvVge3Q+V0ws2zsL3z7ndz4tTMYFdvR/XbrnbEErTDLWrV6Lc3JHQMs0bYUyTBg5dThwCiuZ1evaT6BlMMLuSCVxdBGzXTBcvGwihFzZbyNoX+52DS5x+RbIEvd6KWOpQ6Ni+1GAawHDdNUiQTQFXRxLSHfc9fh7hE4qcD7PqHGsykYj7A0XqHCjbKKgWSkcAg==
```

<span data-ttu-id="af1d9-117">Jos haluat soittaa dataohjelmointirajapintaliittymään, liitä käyttöoikeustietue merkiksi HTTP-pyynnön valtuutustietoihin.</span><span class="sxs-lookup"><span data-stu-id="af1d9-117">To call the data API, you attach the access token as a bearer token to the authorization header in your HTTP request.</span></span> <span data-ttu-id="af1d9-118">Esimerkki:</span><span class="sxs-lookup"><span data-stu-id="af1d9-118">Here is an example.</span></span>

```HTTP
HTTP/1.1
Authorization: Bearer EwAoA8l6BAAU ... 7PqHGsykYj7A0XqHCjbKKgWSkcAg==
Host: https://{cluster}.hr.talent.dynamics.com
GET https://{cluster}.hr.talent.dynamics.com/namespaces/{namespace_guid}/data/JobTypes
```

## <a name="register-a-new-application-by-using-the-azure-portal"></a><span data-ttu-id="af1d9-119">Rekisteröi uusi sovellus Azure-portaalissa</span><span class="sxs-lookup"><span data-stu-id="af1d9-119">Register a new application by using the Azure portal</span></span>

1. <span data-ttu-id="af1d9-120">Kirjaudu [Microsoft Azure -portaaliin](https://portal.azure.com) työ- tai koulutilillä tai henkilökohtaisella Microsoft-tilillä.</span><span class="sxs-lookup"><span data-stu-id="af1d9-120">Sign in to the [Microsoft Azure portal](https://portal.azure.com) with a work or school account, or a personal Microsoft account.</span></span>

2. <span data-ttu-id="af1d9-121">Jos tilin avulla voit käyttää useita vuokralaisia, valitse tilisi oikeasta yläkulmasta ja aseta portaali-istunto Azure Active Directory (Azure AD) haluamallesi vuokralaiselle.</span><span class="sxs-lookup"><span data-stu-id="af1d9-121">If your account gives you access to more than one tenant, select your account in the upper-right corner, and set your portal session to the Azure Active Directory (Azure AD) tenant that you want.</span></span>

3. <span data-ttu-id="af1d9-122">Valitse **Azure Active Directory** -palvelu vasemmanpuoleisesta ruudusta ja valitse sitten **Sovellusrekisteröinnit \> Uusi rekisteröinti**.</span><span class="sxs-lookup"><span data-stu-id="af1d9-122">In the left pane, select the **Azure Active Directory** service, and then select **App registrations \> New registration**.</span></span>

4. <span data-ttu-id="af1d9-123">Kun **Rekisteröi sovellus** -sivu tulee näkyviin, kirjoita sovelluksen rekisteröintitiedot:</span><span class="sxs-lookup"><span data-stu-id="af1d9-123">When the **Register an application** page appears, enter your application's registration information:</span></span>

    - <span data-ttu-id="af1d9-124">**Nimi**: Anna mielekäs sovelluksen nimi, joka näytetään sovelluksen käyttäjille.</span><span class="sxs-lookup"><span data-stu-id="af1d9-124">**Name**: Enter a meaningful application name that will be shown to users of the app.</span></span>
    - <span data-ttu-id="af1d9-125">**Tuetut tilityypit**: Valitse tilityypit, joita sovelluksesi tukee.</span><span class="sxs-lookup"><span data-stu-id="af1d9-125">**Supported account types**: Select the types of accounts that your app should support.</span></span>

        | <span data-ttu-id="af1d9-126">Tuetut tilityypit</span><span class="sxs-lookup"><span data-stu-id="af1d9-126">Supported account types</span></span> | <span data-ttu-id="af1d9-127">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="af1d9-127">Description</span></span> |
        |-------------------------|-------------|
        | <span data-ttu-id="af1d9-128">Vain tämän organisaation hakemiston tilit</span><span class="sxs-lookup"><span data-stu-id="af1d9-128">Accounts in this organizational directory only</span></span> | <span data-ttu-id="af1d9-129">Valitse tämä vaihtoehto, jos olet rakentamassa yrityssovellusta.</span><span class="sxs-lookup"><span data-stu-id="af1d9-129">Select this option if you're building a line-of-business app.</span></span> <span data-ttu-id="af1d9-130">Tämä vaihtoehto ei ole käytettävissä, ellet ole rekisteröimässä sovellusta hakemistossa.</span><span class="sxs-lookup"><span data-stu-id="af1d9-130">This option isn't available unless you're registering the app in a directory.</span></span><p><span data-ttu-id="af1d9-131">Tämä vaihtoehto on liitetty vain yhteen **Azure AD:n vuokralaiseen**.</span><span class="sxs-lookup"><span data-stu-id="af1d9-131">This option is mapped to **Azure AD only single-tenant**.</span></span></p><p><span data-ttu-id="af1d9-132">Tämä vaihtoehto on oletusasetus, ellet ole rekisteröimässä sovellusta hakemiston ulkopuolelle.</span><span class="sxs-lookup"><span data-stu-id="af1d9-132">This option is the default option unless you're registering the app outside a directory.</span></span> <span data-ttu-id="af1d9-133">Tässä tapauksessa oletusvaihtoehto on useat **Azure AD:n vuokralaiset ja henkilökohtaisen Microsoft-tilit**.</span><span class="sxs-lookup"><span data-stu-id="af1d9-133">In that case, the default option is **Azure AD multi-tenant and personal Microsoft accounts**.</span></span></p> |
        | <span data-ttu-id="af1d9-134">Minkä tahansa organisaation hakemiston tilit</span><span class="sxs-lookup"><span data-stu-id="af1d9-134">Accounts in any organizational directory</span></span> | <span data-ttu-id="af1d9-135">Valitse tämä vaihtoehto, jos haluat kohdistaa kaikki liike- ja koulutusasiakkaat.</span><span class="sxs-lookup"><span data-stu-id="af1d9-135">Select this option to target all business and educational customers.</span></span><p><span data-ttu-id="af1d9-136">Tämä vaihtoehto on liitetty useisiin **Azure AD:n vuokralaisiin**.</span><span class="sxs-lookup"><span data-stu-id="af1d9-136">This option is mapped to **Azure AD only multi-tenant**.</span></span></p><p><span data-ttu-id="af1d9-137">Jos olet rekisteröinyt sovelluksen **Azure AD:na vain yhden vuokralaisen käyttöön**, voit päivittää sen **Azure AD:ksi vain usean vuokralaisen käyttöön** ja sitten takaisin **Azure AD:ksi vain yhden vuokralaisen käyttöön** **Todennus**-lavan avulla.</span><span class="sxs-lookup"><span data-stu-id="af1d9-137">If you registered the app as **Azure AD only single-tenant**, you can use the **Authentication** blade to update it to **Azure AD only multi-tenant** and then back to **Azure AD only single-tenant**.</span></span></p> |
        | <span data-ttu-id="af1d9-138">Tilit missä tahansa organisaatiohakemistossa ja omissa Microsoft-tileissä</span><span class="sxs-lookup"><span data-stu-id="af1d9-138">Accounts in any organizational directory and personal Microsoft accounts</span></span> | <span data-ttu-id="af1d9-139">Valitse tämä vaihtoehto, kun haluat kohdistaa laajimman asiakasjoukon.</span><span class="sxs-lookup"><span data-stu-id="af1d9-139">Select this option to target the widest set of customers.</span></span><p><span data-ttu-id="af1d9-140">Tämä vaihtoehto on yhdistetty useisiin **Azure AD:n vuokralaisiin ja henkilökohtaisiin Microsoft-tileihin**.</span><span class="sxs-lookup"><span data-stu-id="af1d9-140">This option is mapped to **Azure AD multi-tenant and personal Microsoft accounts**.</span></span></p><p><span data-ttu-id="af1d9-141">Jos olet rekisteröinyt sovelluksen **Azure AD:n usean vuokralaisen ja henkilökohtaisen Microsoft-tilisi** käyttäjäksi, et voi muuttaa tätä asetusta käyttöliittymässä.</span><span class="sxs-lookup"><span data-stu-id="af1d9-141">If you registered the app as **Azure AD multi-tenant and personal Microsoft accounts**, you can't change this setting in the user interface (UI).</span></span> <span data-ttu-id="af1d9-142">Sen sijaan on käytettävä sovelluksen luetteloeditoria tuettujen tilityyppien muuttamiseen.</span><span class="sxs-lookup"><span data-stu-id="af1d9-142">Instead, you must use the application manifest editor to change the supported account types.</span></span></p> |

    - <span data-ttu-id="af1d9-143">**Uudelleenohjauksen URI (valinnainen)** – Valitse sen sovelluksen tyyppi, jota olet rakentamassa: **Verkko**- tai **Julkinen asiakasohjelma (mobiili & työpöytä**).</span><span class="sxs-lookup"><span data-stu-id="af1d9-143">**Redirect URI (optional)** – Select the type of app that you're building: **Web** or **Public client (mobile & desktop)**.</span></span> <span data-ttu-id="af1d9-144">Kirjoita sitten sovelluksen uudelleenohjauksen URI (tai vastaus-URL).</span><span class="sxs-lookup"><span data-stu-id="af1d9-144">Then enter the redirect URI (or reply URL) for the app.</span></span>

        - <span data-ttu-id="af1d9-145">Jos kyseessä on Internet-sovellus, anna sovelluksen perusosoite.</span><span class="sxs-lookup"><span data-stu-id="af1d9-145">For web apps, provide the base URL of the app.</span></span> <span data-ttu-id="af1d9-146">Tämä `http://localhost:31544` voi olla esimerkiksi paikallisessa tietokoneessa käytettävän Internet-sovelluksen URL-osoite.</span><span class="sxs-lookup"><span data-stu-id="af1d9-146">For example, `http://localhost:31544` might be the URL for a web app that runs on your local machine.</span></span> <span data-ttu-id="af1d9-147">Tämän jälkeen käyttäjät kirjautuvat WWW-asiakasohjelmaan tämän URL-osoitteen avulla.</span><span class="sxs-lookup"><span data-stu-id="af1d9-147">Users then use this URL to sign in to a web client app.</span></span>
        - <span data-ttu-id="af1d9-148">Jos kyseessä on yleinen asiakassovellus, anna URI-tunnus, jota Azure AD käyttää palauttamaan tunnuksen vastauksia.</span><span class="sxs-lookup"><span data-stu-id="af1d9-148">For public client apps, provide the URI that Azure AD uses to return token responses.</span></span> <span data-ttu-id="af1d9-149">Kirjoita sovellukseen liittyviä arvoja, kuten `myapp://auth`.</span><span class="sxs-lookup"><span data-stu-id="af1d9-149">Enter a value that is specific to your app, such as `myapp://auth`.</span></span>

        <span data-ttu-id="af1d9-150">Lisätietoja Internet-sovelluksista ja alkuperäisistä sovelluksista on [Microsoftin käyttäjätietoympäristössä (aiemmin Azure Active Directory sovelluskehittäjille)](https://docs.microsoft.com/azure/active-directory/develop/#quickstarts).</span><span class="sxs-lookup"><span data-stu-id="af1d9-150">To see specific examples for web apps or native apps, see the quickstarts in [Microsoft identity platform (formerly Azure Active Directory for developers)](https://docs.microsoft.com/azure/active-directory/develop/#quickstarts).</span></span>

5. <span data-ttu-id="af1d9-151">Valitse **API-käyttöoikeudet**-kohdasta**Lisää käyttöoikeus**.</span><span class="sxs-lookup"><span data-stu-id="af1d9-151">Under **API permissions**, select **Add a permission**.</span></span> <span data-ttu-id="af1d9-152">Valitse sitten **API-liittymät, joita oma organisaationi käyttää** -välilehti, etsi **Dynamics 365 Human Resources** ja lisää **käyttäjä\_tekeytyminen**-oikeus sovellukseen.</span><span class="sxs-lookup"><span data-stu-id="af1d9-152">Then, on the **APIs my organization uses** tab, search for **Dynamics 365 Human Resources**, and add the **user\_impersonation** permission to your app.</span></span> <span data-ttu-id="af1d9-153">Henkilöstöhallinnon sovellustunnus on f9be0c49-aa22-4ec6-911a-c5da515226ff.</span><span class="sxs-lookup"><span data-stu-id="af1d9-153">The Application ID for Human Resources is f9be0c49-aa22-4ec6-911a-c5da515226ff.</span></span> <span data-ttu-id="af1d9-154">Tämän tunnuksen avulla voit varmistaa, että olet valinnut oikean sovelluksen.</span><span class="sxs-lookup"><span data-stu-id="af1d9-154">Use this ID to ensure you have chosen the correct application.</span></span>

6. <span data-ttu-id="af1d9-155">Valitse **Rekisteröi**.</span><span class="sxs-lookup"><span data-stu-id="af1d9-155">Select **Register**.</span></span>

   <span data-ttu-id="af1d9-156">[![Uuden sovelluksen rekisteröiminen Azure-portaaliin](media/api-new-app-registration-expanded.png)](media/api-new-app-registration-expanded.png#lightbox)</span><span class="sxs-lookup"><span data-stu-id="af1d9-156">[![Registering a new app in the Azure portal](media/api-new-app-registration-expanded.png)](media/api-new-app-registration-expanded.png#lightbox)</span></span>

<span data-ttu-id="af1d9-157">Azure AD määrittää sovellukseesi yksilöllisen sovellustunnuksen (asiakastunnus) ja vie sinut sovelluksesi **yhteenveto**-sivulle.</span><span class="sxs-lookup"><span data-stu-id="af1d9-157">Azure AD assigns a unique application ID (client ID) to your app, and takes you to the **Overview** page for your app.</span></span> <span data-ttu-id="af1d9-158">Jos haluat lisätä sovellukseesi muita ominaisuuksia, voit valita muita asetuksia, kuten brändäyksen sekä sertifikaattien ja salaisuuksien asetukset.</span><span class="sxs-lookup"><span data-stu-id="af1d9-158">To add more capabilities to your app, you can select other configuration options, such as options for branding and for certificates and secrets.</span></span>

## <a name="retrieving-an-access-token"></a><span data-ttu-id="af1d9-159">Käyttötunnussanoman noutaminen</span><span class="sxs-lookup"><span data-stu-id="af1d9-159">Retrieving an access token</span></span>

<span data-ttu-id="af1d9-160">Henkilöstöhallinnon dataohjelmointirajapintaliittymän kutsumiseen käytettävän käyttötunnussanoman tiedot määräytyvät sen mukaan, mitä tekniikoita asiakassovelluksen kehittämisessä käytetään.</span><span class="sxs-lookup"><span data-stu-id="af1d9-160">The specifics of how you retrieve an access token for calling the Human Resources data API will depend on what technologies you're using to develop your client application.</span></span> <span data-ttu-id="af1d9-161">Voit esimerkiksi [kokeilla kolmannen osapuolen apuohjelmaa](../fin-ops-core/dev-itpro/data-entities/third-party-service-test.md) (kuten Postman), kehittää C#-konsolisovellusta tai Internet-palvelua tai rakentaa javascript/TypeScript-asiakasta.</span><span class="sxs-lookup"><span data-stu-id="af1d9-161">For example, you might be [testing with a third party utility](../fin-ops-core/dev-itpro/data-entities/third-party-service-test.md) (such as Postman), developing a C# console application or web service, or building a javascript/TypeScript client.</span></span>

<span data-ttu-id="af1d9-162">Esimerkki C#-asiakassovelluksesta:</span><span class="sxs-lookup"><span data-stu-id="af1d9-162">Example C# client application:</span></span>
```C#
using System;
using System.Net.Http;
using System.Threading.Tasks;

// requires appropriate NuGet package references in the project
using Microsoft.IdentityModel.Clients.ActiveDirectory;

namespace TalentODataPoC
{
    class Program
    {
        // prereq: This client app must be registered in Azure Active Directory. The app must be
        // registered as requiring permission to the Dynamics 365 for Talent API (with the Dynamics
        // HCM Workload delegated permission).
        static string clientId = "4fc703ef-672c-4e2c-813f-2f9d29d726db"; // This value should be obtained from AAD and must match your registered app
        static string talentNamespaceUri = "";

        public static async Task CallTalentODataService()
        {
            // authority URI
            UriBuilder uri = new UriBuilder("https://login.microsoftonline.com/common");
            AuthenticationContext authenticationContext = new AuthenticationContext(uri.ToString());

            // request token for the resource we want to access (Human Resources). This will authenticate
            // the user and return an access token containing claims for the authenticated user.
            var authResult = await authenticationContext.AcquireTokenAsync(
                "http://hr.talent.dynamics.com", /*Talent app id or resource URI*/
                clientId, /*registered client app id*/
                new Uri("https://localhost"), /*redirect URI, as registered in your AAD app*/
                new PlatformParameters(PromptBehavior.SelectAccount));

            // create the authorization header, which needs to be passed in the Header of the HTTP Requests to Talent
            string authHeader = authResult.CreateAuthorizationHeader();

            // HINT: paste the JWT into https://jwt.ms to decode and view it
            Console.Write("authHeader: ");
            Console.WriteLine(authHeader);
            Console.WriteLine();

            HttpClient client = new HttpClient();
            client.DefaultRequestHeaders.Add("Authorization", authHeader);

            string s;

            Console.Write("Talent Namespace URI: ");
            Console.WriteLine(talentNamespaceUri);
            Console.WriteLine();

            // call the OData service to get JobType data from Talent
            var resultOdata = await client.GetAsync(talentNamespaceUri + "data/JobTypes");
            s = await resultOdata.Content.ReadAsStringAsync();
            Console.WriteLine(s);
            Console.WriteLine();
        }

        static void Main(string[] args)
        {
            Console.WriteLine();

            // if the user passes in a single parameter, assume it is the namespaceUri for Talent
            if (args.Length == 1)
            {
                talentNamespaceUri = args[0];
            } else if (args.Length == 0)
            {
                Console.WriteLine("Enter Talent URL including namespace.");
                Console.WriteLine("Example: https://aos-rts-sf-21454f9d830-prod-westus2.hr.talent.dynamics.com/namespaces/2328af1a-2d45-4c6a-99e3-12a4c3867dcf/");
                Console.Write("> ");
                talentNamespaceUri = Console.ReadLine();
                if (!talentNamespaceUri.EndsWith("/"))
                {
                    talentNamespaceUri = talentNamespaceUri + "/";
                }
            } else
            {
                Console.WriteLine("Unexpected Arguments");
                System.Environment.Exit(1);
            }

            Task t = Program.CallTalentODataService();
            t.Wait();
        }
    }
}
```

<span data-ttu-id="af1d9-163">Kun olet hakenut käyttötunnussanoman, ohitat valtuutustietojen otsikossa olevan tunnuksen ja jokaisen pyynnön, jonka lähetät tietojen ohjelmointirajapintaliittymään edellä kuvatulla tavalla.</span><span class="sxs-lookup"><span data-stu-id="af1d9-163">Once you've retrieved an access token, you'll pass the token in the Authorization header as a bearer token with each request you send to the data API, as described above.</span></span>