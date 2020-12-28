---
title: Evästeen yhteensopivuus
description: Tässä ohjeaiheessa käsitellään evästeiden yhteensopivuuden ja Microsoft Dynamics 365 Commercen oletuskäytäntöjen huomioitavia seikkoja.
author: BrianShook
manager: annbe
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 4f54b9b8130a167dbecdb13fccd7039f827f6ed0
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4411871"
---
# <a name="cookie-compliance"></a><span data-ttu-id="1aab2-103">Evästeen yhteensopivuus</span><span class="sxs-lookup"><span data-stu-id="1aab2-103">Cookie compliance</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="1aab2-104">Tässä ohjeaiheessa käsitellään evästeiden yhteensopivuuden ja Microsoft Dynamics 365 Commercen oletuskäytäntöjen huomioitavia seikkoja.</span><span class="sxs-lookup"><span data-stu-id="1aab2-104">This topic describes considerations for cookie compliance and the default policies that are included in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="1aab2-105">Yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="1aab2-105">Overview</span></span>

<span data-ttu-id="1aab2-106">Yksityisyys on tärkeä tekijä aina, kun käytetään verkkokaupan asiakkaisiin vaikuttavia seurantatekniikoita.</span><span class="sxs-lookup"><span data-stu-id="1aab2-106">Privacy is an important factor when tracking technologies that affect e-Commerce customers.</span></span> <span data-ttu-id="1aab2-107">Tietosuojan yhteensopivuusstandardien noudattaminen, kuten yleinen tietosuoja-asetus (GDPR) Euroopan unionin (EU) alueella, on otettava huomioon sähköisessä tietosuojaohjeessa, jokaisella sivustolla, joka on käytössä tällä hetkellä.</span><span class="sxs-lookup"><span data-stu-id="1aab2-107">Because of privacy compliance standards such as the General Data Protection Regulation (GDPR) in the European Union (EU), electronic privacy guidelines must be considered for any site that is active today.</span></span> <span data-ttu-id="1aab2-108">Koska monet sähköisen kaupankäynnin sivustot ovat oletusarvoisesti yleisesti saatavilla, on tärkeää, että tarkistat verkkokauppasivustosi yhteensopivuusstandardit.</span><span class="sxs-lookup"><span data-stu-id="1aab2-108">Because many e-Commerce sites are globally accessible by default, it's important that you review the compliance standards for your e-Commerce site.</span></span>

<span data-ttu-id="1aab2-109">Saat lisätietoja perusperiaatteista, joita Microsoft käyttää evästeiden noudattamiseen, käymällä [Microsoft Trust Centerissä](https://www.microsoft.com/trust-center).</span><span class="sxs-lookup"><span data-stu-id="1aab2-109">To learn more about the basic principles that Microsoft uses for cookie compliance, visit the [Microsoft Trust Center](https://www.microsoft.com/trust-center).</span></span> <span data-ttu-id="1aab2-110">Tällä sivustolla voit myös saada lisätietoja yhteensopivuus- ja yksityisyysasioista.</span><span class="sxs-lookup"><span data-stu-id="1aab2-110">On that site, you can also get more information about areas of compliance and privacy.</span></span>

<span data-ttu-id="1aab2-111">Seuraavassa taulukossa on viiteluettelo evästeitä, joita Dynamics 365 Commerce -sivustot tällä hetkellä sijoittavat.</span><span class="sxs-lookup"><span data-stu-id="1aab2-111">The following table shows the current reference list of cookies placed by Dynamics 365 Commerce sites.</span></span>

| <span data-ttu-id="1aab2-112">Evästeen nimi</span><span class="sxs-lookup"><span data-stu-id="1aab2-112">Cookie name</span></span>                               | <span data-ttu-id="1aab2-113">Käyttö</span><span class="sxs-lookup"><span data-stu-id="1aab2-113">Usage</span></span>                                                        |
| ------------------------------------------- | ------------------------------------------------------------ |
| <span data-ttu-id="1aab2-114">.AspNet.Cookies</span><span class="sxs-lookup"><span data-stu-id="1aab2-114">.AspNet.Cookies</span></span>                             | <span data-ttu-id="1aab2-115">Tallentaa Microsoft Azure Active Directoryn (Azure AD) kertakirjautumisen todentamisevästeet.</span><span class="sxs-lookup"><span data-stu-id="1aab2-115">Store Microsoft Azure Active Directory (Azure AD) authentication cookies for single sign-on (SSO).</span></span> <span data-ttu-id="1aab2-116">Tallentaa salatut käyttäjän objektitiedot (nimen, sukunimen ja sähköpostiosoitteen).</span><span class="sxs-lookup"><span data-stu-id="1aab2-116">Stores encrypted user principal information (name, surname, email).</span></span> |
| <span data-ttu-id="1aab2-117">&#95;msdyn365___cart&#95;</span><span class="sxs-lookup"><span data-stu-id="1aab2-117">&#95;msdyn365___cart&#95;</span></span>                           | <span data-ttu-id="1aab2-118">Tallentaa ostoskorin tunnukset, jolla saadaan luettelo ostoskoriesiintymään lisätyistä tuotteista.</span><span class="sxs-lookup"><span data-stu-id="1aab2-118">Store cart ID used to obtain list of products added to cart instance.</span></span> |
| <span data-ttu-id="1aab2-119">&#95;msdyn365___ucc&#95;</span><span class="sxs-lookup"><span data-stu-id="1aab2-119">&#95;msdyn365___ucc&#95;</span></span>                            | <span data-ttu-id="1aab2-120">Evästeiden vaatimustenmukainen hyväksynnän seuranta.</span><span class="sxs-lookup"><span data-stu-id="1aab2-120">Cookie compliance consent tracking.</span></span>                          |
| <span data-ttu-id="1aab2-121">ai_session</span><span class="sxs-lookup"><span data-stu-id="1aab2-121">ai_session</span></span>                                  | <span data-ttu-id="1aab2-122">Määrittää, kuinka moni käyttäjän tehtäväistunto on sisältänyt tiettyjä sivuja ja sovelluksen toimintoja.</span><span class="sxs-lookup"><span data-stu-id="1aab2-122">Detects how many sessions of user activity have included certain pages and features of the app.</span></span> |
| <span data-ttu-id="1aab2-123">ai_user</span><span class="sxs-lookup"><span data-stu-id="1aab2-123">ai_user</span></span>                                     | <span data-ttu-id="1aab2-124">Määrittää, kuinka moni henkilö on käyttänyt sovellusta ja sen toimintoja.</span><span class="sxs-lookup"><span data-stu-id="1aab2-124">Detects how many people used the app and its features.</span></span> <span data-ttu-id="1aab2-125">Käyttäjien laskennassa käytetään anonyymeja tunnuksia.</span><span class="sxs-lookup"><span data-stu-id="1aab2-125">Users are counted using anonymous IDs.</span></span> |
| <span data-ttu-id="1aab2-126">b2cru</span><span class="sxs-lookup"><span data-stu-id="1aab2-126">b2cru</span></span>                                       | <span data-ttu-id="1aab2-127">Tallentaa uudelleenohjauksen URL-osoitteen dynaamisesti.</span><span class="sxs-lookup"><span data-stu-id="1aab2-127">Stores redirect URL dynamically.</span></span>                              |
| <span data-ttu-id="1aab2-128">JSESSESSIID</span><span class="sxs-lookup"><span data-stu-id="1aab2-128">JSESSIONID</span></span>                                  | <span data-ttu-id="1aab2-129">Adyen-maksuyhdistin käyttää käyttäjäistunnon tallentamiseen.</span><span class="sxs-lookup"><span data-stu-id="1aab2-129">Used by payment connector Adyen to store user session.</span></span>       |
| <span data-ttu-id="1aab2-130">OpenIdConnect.nonce.&#42;</span><span class="sxs-lookup"><span data-stu-id="1aab2-130">OpenIdConnect.nonce.&#42;</span></span>                       | <span data-ttu-id="1aab2-131">Todennus</span><span class="sxs-lookup"><span data-stu-id="1aab2-131">Authentication</span></span>                                               |
| <span data-ttu-id="1aab2-132">x-ms-cpim-cache:.&#42;</span><span class="sxs-lookup"><span data-stu-id="1aab2-132">x-ms-cpim-cache:.&#42;</span></span>                          | <span data-ttu-id="1aab2-133">Käytetään pyynnön tilan ylläpitämiseen.</span><span class="sxs-lookup"><span data-stu-id="1aab2-133">Used for maintaining the request state.</span></span>                      |
| <span data-ttu-id="1aab2-134">x-ms-cpim-csrf</span><span class="sxs-lookup"><span data-stu-id="1aab2-134">x-ms-cpim-csrf</span></span>                              | <span data-ttu-id="1aab2-135">Jaetun julkaisuoikeuspyynnön väärentämisen (CRSF) tunnus, jota käytetään CRSF-väärennökseltä suojautumiseen.</span><span class="sxs-lookup"><span data-stu-id="1aab2-135">Cross-site request forgery (CRSF) token used for protection from CRSF.</span></span>     |
| <span data-ttu-id="1aab2-136">x-ms-cpim-dc</span><span class="sxs-lookup"><span data-stu-id="1aab2-136">x-ms-cpim-dc</span></span>                                | <span data-ttu-id="1aab2-137">Käytetään reitittämään pyyntöjä sopivaan tuotannon todennuspalvelinesiintymään.</span><span class="sxs-lookup"><span data-stu-id="1aab2-137">Used to route requests to the appropriate production authentication server instance.</span></span> |
| <span data-ttu-id="1aab2-138">x-ms-cpim-rc.&#42;</span><span class="sxs-lookup"><span data-stu-id="1aab2-138">x-ms-cpim-rc.&#42;</span></span>                              | <span data-ttu-id="1aab2-139">Käytetään reitittämään pyyntöjä sopivaan tuotannon todennuspalvelinesiintymään.</span><span class="sxs-lookup"><span data-stu-id="1aab2-139">Used to route requests to the appropriate production authentication server instance.</span></span> |
| <span data-ttu-id="1aab2-140">x-ms-cpim-slice</span><span class="sxs-lookup"><span data-stu-id="1aab2-140">x-ms-cpim-slice</span></span>                             | <span data-ttu-id="1aab2-141">Käytetään reitittämään pyyntöjä sopivaan tuotannon todennuspalvelinesiintymään.</span><span class="sxs-lookup"><span data-stu-id="1aab2-141">Used to route requests to the appropriate production authentication server instance.</span></span> |
| <span data-ttu-id="1aab2-142">x-ms-cpim-sso:rushmoreb2c.onmicrosoft.com_0</span><span class="sxs-lookup"><span data-stu-id="1aab2-142">x-ms-cpim-sso:rushmoreb2c.onmicrosoft.com_0</span></span> | <span data-ttu-id="1aab2-143">Käytetään kertakirjautumisistunnon ylläpitämiseen.</span><span class="sxs-lookup"><span data-stu-id="1aab2-143">Used for maintaining the SSO session.</span></span>                        |
| <span data-ttu-id="1aab2-144">x-ms-cpim-trans</span><span class="sxs-lookup"><span data-stu-id="1aab2-144">x-ms-cpim-trans</span></span>                             | <span data-ttu-id="1aab2-145">Käytetään tapahtumien seurantaan (kuluttajakauppasivustossa todennettavien avoimien välilehtien määrä), mikä sisältää myös nykyisen tapahtuman.</span><span class="sxs-lookup"><span data-stu-id="1aab2-145">Used for tracking transactions (the number of open tabs authenticating against a business-to-consumer (B2C) site), including the current transaction.</span></span> |

## <a name="site-user-cookie-consent-on-an-e-commerce-site"></a><span data-ttu-id="1aab2-146">Sivuston käyttäjän evästeiden hyväksyntä sähköisen kaupankäynnin sivustossa</span><span class="sxs-lookup"><span data-stu-id="1aab2-146">Site user cookie consent on an e-Commerce site</span></span> 

<span data-ttu-id="1aab2-147">Jos sähköisen kaupankäynnin sivuston ominaisuus tai moduuli käyttää ei-olennaista evästettä, sivuston käyttäjän hyväksyntä on saatava ennen evästeen seuraamista.</span><span class="sxs-lookup"><span data-stu-id="1aab2-147">If an e-Commerce site feature or module uses a non-essential cookie, a site user's consent must be obtained before the cookie is tracked.</span></span> <span data-ttu-id="1aab2-148">Jotta sivuston käyttäjät voivat antaa evästeiden hyväksynnän sähköisen kaupankäynnin sivustossa, sivuston tekijän on lisättävä ja konfiguroitava evästeiden hyväksyntämoduuli sivun otsikkomoduulissa. Näin varmistetaan, että hyväksyntä pyydetään ja vastaanotetaan.</span><span class="sxs-lookup"><span data-stu-id="1aab2-148">To allow site users to provide cookie consent on the e-Commerce site, a site author must add and configure a cookie consent module in the page's header module to ensure that the consent is prompted for and received.</span></span> <span data-ttu-id="1aab2-149">Sivuston käyttäjän hyväksyntä on saatava, ennen kuin ei-olennaista evästettä käyttävä toiminto tai moduuli voidaan hahmontaa sivuston sivulla.</span><span class="sxs-lookup"><span data-stu-id="1aab2-149">Site user consent must be given before a feature or module using a non-essential cookie can be rendered on a site page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1aab2-150">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="1aab2-150">Additional resources</span></span>

[<span data-ttu-id="1aab2-151">Helppokäyttöisyyden toiminnot ja ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="1aab2-151">Accessibility features and capabilities</span></span>](accessibility.md)

[<span data-ttu-id="1aab2-152">Yhteensopivuuden yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="1aab2-152">Compliance overview</span></span>](compliance-overview.md)

[<span data-ttu-id="1aab2-153">Lisää tietosuojakäytäntösivu</span><span class="sxs-lookup"><span data-stu-id="1aab2-153">Add a privacy policy page</span></span>](add-privacy-page.md)

[<span data-ttu-id="1aab2-154">Seurattuihin sisällönmuutoksiin liittyvien käyttäjätunnusten korvaaminen</span><span class="sxs-lookup"><span data-stu-id="1aab2-154">Replace user IDs associated with tracked content changes</span></span>](replace-IDs-tracked-changes.md)

[<span data-ttu-id="1aab2-155">Evästeen hyväksyntämoduuli</span><span class="sxs-lookup"><span data-stu-id="1aab2-155">Cookie consent module</span></span>](cookie-consent-module.md) 
 
[<span data-ttu-id="1aab2-156">Ylätunnistemoduuli</span><span class="sxs-lookup"><span data-stu-id="1aab2-156">Header module</span></span>](author-header-module.md)
