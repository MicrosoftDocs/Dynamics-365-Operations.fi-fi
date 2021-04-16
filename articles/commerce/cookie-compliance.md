---
title: Evästeen yhteensopivuus
description: Tässä ohjeaiheessa käsitellään evästeiden yhteensopivuuden ja Microsoft Dynamics 365 Commercen oletuskäytäntöjen huomioitavia seikkoja.
author: BrianShook
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 2cc2089bc3052c0c59cb0414f8301123a9a30df2
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5796024"
---
# <a name="cookie-compliance"></a><span data-ttu-id="e5678-103">Evästeen yhteensopivuus</span><span class="sxs-lookup"><span data-stu-id="e5678-103">Cookie compliance</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e5678-104">Tässä ohjeaiheessa käsitellään evästeiden yhteensopivuuden ja Microsoft Dynamics 365 Commercen oletuskäytäntöjen huomioitavia seikkoja.</span><span class="sxs-lookup"><span data-stu-id="e5678-104">This topic describes considerations for cookie compliance and the default policies that are included in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="e5678-105">Yksityisyys on tärkeä tekijä aina, kun käytetään verkkokaupan asiakkaisiin vaikuttavia seurantatekniikoita.</span><span class="sxs-lookup"><span data-stu-id="e5678-105">Privacy is an important factor when tracking technologies that affect e-Commerce customers.</span></span> <span data-ttu-id="e5678-106">Tietosuojan yhteensopivuusstandardien noudattaminen, kuten yleinen tietosuoja-asetus (GDPR) Euroopan unionin (EU) alueella, on otettava huomioon sähköisessä tietosuojaohjeessa, jokaisella sivustolla, joka on käytössä tällä hetkellä.</span><span class="sxs-lookup"><span data-stu-id="e5678-106">Because of privacy compliance standards such as the General Data Protection Regulation (GDPR) in the European Union (EU), electronic privacy guidelines must be considered for any site that is active today.</span></span> <span data-ttu-id="e5678-107">Koska monet sähköisen kaupankäynnin sivustot ovat oletusarvoisesti yleisesti saatavilla, on tärkeää, että tarkistat verkkokauppasivustosi yhteensopivuusstandardit.</span><span class="sxs-lookup"><span data-stu-id="e5678-107">Because many e-Commerce sites are globally accessible by default, it's important that you review the compliance standards for your e-Commerce site.</span></span>

<span data-ttu-id="e5678-108">Saat lisätietoja perusperiaatteista, joita Microsoft käyttää evästeiden noudattamiseen, käymällä [Microsoft Trust Centerissä](https://www.microsoft.com/trust-center).</span><span class="sxs-lookup"><span data-stu-id="e5678-108">To learn more about the basic principles that Microsoft uses for cookie compliance, visit the [Microsoft Trust Center](https://www.microsoft.com/trust-center).</span></span> <span data-ttu-id="e5678-109">Tällä sivustolla voit myös saada lisätietoja yhteensopivuus- ja yksityisyysasioista.</span><span class="sxs-lookup"><span data-stu-id="e5678-109">On that site, you can also get more information about areas of compliance and privacy.</span></span>

<span data-ttu-id="e5678-110">Seuraavassa taulukossa on viiteluettelo evästeitä, joita Dynamics 365 Commerce -sivustot tällä hetkellä sijoittavat.</span><span class="sxs-lookup"><span data-stu-id="e5678-110">The following table shows the current reference list of cookies placed by Dynamics 365 Commerce sites.</span></span>

| <span data-ttu-id="e5678-111">Evästeen nimi</span><span class="sxs-lookup"><span data-stu-id="e5678-111">Cookie name</span></span>                               | <span data-ttu-id="e5678-112">Käyttö</span><span class="sxs-lookup"><span data-stu-id="e5678-112">Usage</span></span>                                                        |
| ------------------------------------------- | ------------------------------------------------------------ |
| <span data-ttu-id="e5678-113">.AspNet.Cookies</span><span class="sxs-lookup"><span data-stu-id="e5678-113">.AspNet.Cookies</span></span>                             | <span data-ttu-id="e5678-114">Tallentaa Microsoft Azure Active Directoryn (Azure AD) kertakirjautumisen todentamisevästeet.</span><span class="sxs-lookup"><span data-stu-id="e5678-114">Store Microsoft Azure Active Directory (Azure AD) authentication cookies for single sign-on (SSO).</span></span> <span data-ttu-id="e5678-115">Tallentaa salatut käyttäjän objektitiedot (nimen, sukunimen ja sähköpostiosoitteen).</span><span class="sxs-lookup"><span data-stu-id="e5678-115">Stores encrypted user principal information (name, surname, email).</span></span> |
| <span data-ttu-id="e5678-116">&#95;msdyn365___cart&#95;</span><span class="sxs-lookup"><span data-stu-id="e5678-116">&#95;msdyn365___cart&#95;</span></span>                           | <span data-ttu-id="e5678-117">Tallentaa ostoskorin tunnukset, jolla saadaan luettelo ostoskoriesiintymään lisätyistä tuotteista.</span><span class="sxs-lookup"><span data-stu-id="e5678-117">Store cart ID used to obtain list of products added to cart instance.</span></span> |
| <span data-ttu-id="e5678-118">&#95;msdyn365___ucc&#95;</span><span class="sxs-lookup"><span data-stu-id="e5678-118">&#95;msdyn365___ucc&#95;</span></span>                            | <span data-ttu-id="e5678-119">Evästeiden vaatimustenmukainen hyväksynnän seuranta.</span><span class="sxs-lookup"><span data-stu-id="e5678-119">Cookie compliance consent tracking.</span></span>                          |
| <span data-ttu-id="e5678-120">ai_session</span><span class="sxs-lookup"><span data-stu-id="e5678-120">ai_session</span></span>                                  | <span data-ttu-id="e5678-121">Määrittää, kuinka moni käyttäjän tehtäväistunto on sisältänyt tiettyjä sivuja ja sovelluksen toimintoja.</span><span class="sxs-lookup"><span data-stu-id="e5678-121">Detects how many sessions of user activity have included certain pages and features of the app.</span></span> |
| <span data-ttu-id="e5678-122">ai_user</span><span class="sxs-lookup"><span data-stu-id="e5678-122">ai_user</span></span>                                     | <span data-ttu-id="e5678-123">Määrittää, kuinka moni henkilö on käyttänyt sovellusta ja sen toimintoja.</span><span class="sxs-lookup"><span data-stu-id="e5678-123">Detects how many people used the app and its features.</span></span> <span data-ttu-id="e5678-124">Käyttäjien laskennassa käytetään anonyymeja tunnuksia.</span><span class="sxs-lookup"><span data-stu-id="e5678-124">Users are counted using anonymous IDs.</span></span> |
| <span data-ttu-id="e5678-125">b2cru</span><span class="sxs-lookup"><span data-stu-id="e5678-125">b2cru</span></span>                                       | <span data-ttu-id="e5678-126">Tallentaa uudelleenohjauksen URL-osoitteen dynaamisesti.</span><span class="sxs-lookup"><span data-stu-id="e5678-126">Stores redirect URL dynamically.</span></span>                              |
| <span data-ttu-id="e5678-127">JSESSESSIID</span><span class="sxs-lookup"><span data-stu-id="e5678-127">JSESSIONID</span></span>                                  | <span data-ttu-id="e5678-128">Adyen-maksuyhdistin käyttää käyttäjäistunnon tallentamiseen.</span><span class="sxs-lookup"><span data-stu-id="e5678-128">Used by payment connector Adyen to store user session.</span></span>       |
| <span data-ttu-id="e5678-129">OpenIdConnect.nonce.&#42;</span><span class="sxs-lookup"><span data-stu-id="e5678-129">OpenIdConnect.nonce.&#42;</span></span>                       | <span data-ttu-id="e5678-130">Todennus</span><span class="sxs-lookup"><span data-stu-id="e5678-130">Authentication</span></span>                                               |
| <span data-ttu-id="e5678-131">x-ms-cpim-cache:.&#42;</span><span class="sxs-lookup"><span data-stu-id="e5678-131">x-ms-cpim-cache:.&#42;</span></span>                          | <span data-ttu-id="e5678-132">Käytetään pyynnön tilan ylläpitämiseen.</span><span class="sxs-lookup"><span data-stu-id="e5678-132">Used for maintaining the request state.</span></span>                      |
| <span data-ttu-id="e5678-133">x-ms-cpim-csrf</span><span class="sxs-lookup"><span data-stu-id="e5678-133">x-ms-cpim-csrf</span></span>                              | <span data-ttu-id="e5678-134">Jaetun julkaisuoikeuspyynnön väärentämisen (CRSF) tunnus, jota käytetään CRSF-väärennökseltä suojautumiseen.</span><span class="sxs-lookup"><span data-stu-id="e5678-134">Cross-site request forgery (CRSF) token used for protection from CRSF.</span></span>     |
| <span data-ttu-id="e5678-135">x-ms-cpim-dc</span><span class="sxs-lookup"><span data-stu-id="e5678-135">x-ms-cpim-dc</span></span>                                | <span data-ttu-id="e5678-136">Käytetään reitittämään pyyntöjä sopivaan tuotannon todennuspalvelinesiintymään.</span><span class="sxs-lookup"><span data-stu-id="e5678-136">Used to route requests to the appropriate production authentication server instance.</span></span> |
| <span data-ttu-id="e5678-137">x-ms-cpim-rc.&#42;</span><span class="sxs-lookup"><span data-stu-id="e5678-137">x-ms-cpim-rc.&#42;</span></span>                              | <span data-ttu-id="e5678-138">Käytetään reitittämään pyyntöjä sopivaan tuotannon todennuspalvelinesiintymään.</span><span class="sxs-lookup"><span data-stu-id="e5678-138">Used to route requests to the appropriate production authentication server instance.</span></span> |
| <span data-ttu-id="e5678-139">x-ms-cpim-slice</span><span class="sxs-lookup"><span data-stu-id="e5678-139">x-ms-cpim-slice</span></span>                             | <span data-ttu-id="e5678-140">Käytetään reitittämään pyyntöjä sopivaan tuotannon todennuspalvelinesiintymään.</span><span class="sxs-lookup"><span data-stu-id="e5678-140">Used to route requests to the appropriate production authentication server instance.</span></span> |
| <span data-ttu-id="e5678-141">x-ms-cpim-sso:rushmoreb2c.onmicrosoft.com_0</span><span class="sxs-lookup"><span data-stu-id="e5678-141">x-ms-cpim-sso:rushmoreb2c.onmicrosoft.com_0</span></span> | <span data-ttu-id="e5678-142">Käytetään kertakirjautumisistunnon ylläpitämiseen.</span><span class="sxs-lookup"><span data-stu-id="e5678-142">Used for maintaining the SSO session.</span></span>                        |
| <span data-ttu-id="e5678-143">x-ms-cpim-trans</span><span class="sxs-lookup"><span data-stu-id="e5678-143">x-ms-cpim-trans</span></span>                             | <span data-ttu-id="e5678-144">Käytetään tapahtumien seurantaan (kuluttajakauppasivustossa todennettavien avoimien välilehtien määrä), mikä sisältää myös nykyisen tapahtuman.</span><span class="sxs-lookup"><span data-stu-id="e5678-144">Used for tracking transactions (the number of open tabs authenticating against a business-to-consumer (B2C) site), including the current transaction.</span></span> |

## <a name="site-user-cookie-consent-on-an-e-commerce-site"></a><span data-ttu-id="e5678-145">Sivuston käyttäjän evästeiden hyväksyntä sähköisen kaupankäynnin sivustossa</span><span class="sxs-lookup"><span data-stu-id="e5678-145">Site user cookie consent on an e-Commerce site</span></span> 

<span data-ttu-id="e5678-146">Jos sähköisen kaupankäynnin sivuston ominaisuus tai moduuli käyttää ei-olennaista evästettä, sivuston käyttäjän hyväksyntä on saatava ennen evästeen seuraamista.</span><span class="sxs-lookup"><span data-stu-id="e5678-146">If an e-Commerce site feature or module uses a non-essential cookie, a site user's consent must be obtained before the cookie is tracked.</span></span> <span data-ttu-id="e5678-147">Jotta sivuston käyttäjät voivat antaa evästeiden hyväksynnän sähköisen kaupankäynnin sivustossa, sivuston tekijän on lisättävä ja konfiguroitava evästeiden hyväksyntämoduuli sivun otsikkomoduulissa. Näin varmistetaan, että hyväksyntä pyydetään ja vastaanotetaan.</span><span class="sxs-lookup"><span data-stu-id="e5678-147">To allow site users to provide cookie consent on the e-Commerce site, a site author must add and configure a cookie consent module in the page's header module to ensure that the consent is prompted for and received.</span></span> <span data-ttu-id="e5678-148">Sivuston käyttäjän hyväksyntä on saatava, ennen kuin ei-olennaista evästettä käyttävä toiminto tai moduuli voidaan hahmontaa sivuston sivulla.</span><span class="sxs-lookup"><span data-stu-id="e5678-148">Site user consent must be given before a feature or module using a non-essential cookie can be rendered on a site page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e5678-149">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="e5678-149">Additional resources</span></span>

[<span data-ttu-id="e5678-150">Helppokäyttöisyyden toiminnot ja ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="e5678-150">Accessibility features and capabilities</span></span>](accessibility.md)

[<span data-ttu-id="e5678-151">Yhteensopivuuden yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="e5678-151">Compliance overview</span></span>](compliance-overview.md)

[<span data-ttu-id="e5678-152">Lisää tietosuojakäytäntösivu</span><span class="sxs-lookup"><span data-stu-id="e5678-152">Add a privacy policy page</span></span>](add-privacy-page.md)

[<span data-ttu-id="e5678-153">Seurattuihin sisällönmuutoksiin liittyvien käyttäjätunnusten korvaaminen</span><span class="sxs-lookup"><span data-stu-id="e5678-153">Replace user IDs associated with tracked content changes</span></span>](replace-IDs-tracked-changes.md)

[<span data-ttu-id="e5678-154">Evästeen hyväksyntämoduuli</span><span class="sxs-lookup"><span data-stu-id="e5678-154">Cookie consent module</span></span>](cookie-consent-module.md) 
 
[<span data-ttu-id="e5678-155">Ylätunnistemoduuli</span><span class="sxs-lookup"><span data-stu-id="e5678-155">Header module</span></span>](author-header-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
