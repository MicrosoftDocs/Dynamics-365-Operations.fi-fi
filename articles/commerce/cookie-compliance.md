---
title: Evästeen yhteensopivuus
description: Tässä ohjeaiheessa käsitellään evästeiden yhteensopivuuden ja Microsoft Dynamics 365 Commercen oletuskäytäntöjen huomioitavia seikkoja.
author: BrianShook
manager: annbe
ms.date: 06/12/2020
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
ms.openlocfilehash: e1fa016dc9f46b048220f0f83e4b0783087de91e
ms.sourcegitcommit: c66c4c67a21e7d7d3a94a3fd766c3184b6e65c4e
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/12/2020
ms.locfileid: "3446910"
---
# <a name="cookie-compliance"></a><span data-ttu-id="b5d04-103">Evästeen yhteensopivuus</span><span class="sxs-lookup"><span data-stu-id="b5d04-103">Cookie compliance</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b5d04-104">Tässä ohjeaiheessa käsitellään evästeiden yhteensopivuuden ja Microsoft Dynamics 365 Commercen oletuskäytäntöjen huomioitavia seikkoja.</span><span class="sxs-lookup"><span data-stu-id="b5d04-104">This topic describes considerations for cookie compliance and the default policies that are included in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="b5d04-105">Yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="b5d04-105">Overview</span></span>

<span data-ttu-id="b5d04-106">Yksityisyys on tärkeä tekijä aina, kun käytetään verkkokaupan asiakkaisiin vaikuttavia seurantatekniikoita.</span><span class="sxs-lookup"><span data-stu-id="b5d04-106">Privacy is an important factor when tracking technologies that affect e-Commerce customers.</span></span> <span data-ttu-id="b5d04-107">Tietosuojan yhteensopivuusstandardien noudattaminen, kuten yleinen tietosuoja-asetus (GDPR) Euroopan unionin (EU) alueella, on otettava huomioon sähköisessä tietosuojaohjeessa, jokaisella sivustolla, joka on käytössä tällä hetkellä.</span><span class="sxs-lookup"><span data-stu-id="b5d04-107">Because of privacy compliance standards such as the General Data Protection Regulation (GDPR) in the European Union (EU), electronic privacy guidelines must be considered for any site that is active today.</span></span> <span data-ttu-id="b5d04-108">Koska monet sähköisen kaupankäynnin sivustot ovat oletusarvoisesti yleisesti saatavilla, on tärkeää, että tarkistat verkkokauppasivustosi yhteensopivuusstandardit.</span><span class="sxs-lookup"><span data-stu-id="b5d04-108">Because many e-Commerce sites are globally accessible by default, it's important that you review the compliance standards for your e-Commerce site.</span></span>

<span data-ttu-id="b5d04-109">Saat lisätietoja perusperiaatteista, joita Microsoft käyttää evästeiden noudattamiseen, käymällä [Microsoft Trust Centerissä](https://www.microsoft.com/trust-center).</span><span class="sxs-lookup"><span data-stu-id="b5d04-109">To learn more about the basic principles that Microsoft uses for cookie compliance, visit the [Microsoft Trust Center](https://www.microsoft.com/trust-center).</span></span> <span data-ttu-id="b5d04-110">Tällä sivustolla voit myös saada lisätietoja yhteensopivuus- ja yksityisyysasioista.</span><span class="sxs-lookup"><span data-stu-id="b5d04-110">On that site, you can also get more information about areas of compliance and privacy.</span></span>

<span data-ttu-id="b5d04-111">Seuraavassa taulukossa on viiteluettelo evästeitä, joita Dynamics 365 Commerce -sivustot tällä hetkellä sijoittavat.</span><span class="sxs-lookup"><span data-stu-id="b5d04-111">The following table shows the current reference list of cookies placed by Dynamics 365 Commerce sites.</span></span>

| <span data-ttu-id="b5d04-112">Evästeen nimi</span><span class="sxs-lookup"><span data-stu-id="b5d04-112">Cookie name</span></span>                               | <span data-ttu-id="b5d04-113">Käyttö</span><span class="sxs-lookup"><span data-stu-id="b5d04-113">Usage</span></span>                                                        |
| ------------------------------------------- | ------------------------------------------------------------ |
| <span data-ttu-id="b5d04-114">.AspNet.Cookies</span><span class="sxs-lookup"><span data-stu-id="b5d04-114">.AspNet.Cookies</span></span>                             | <span data-ttu-id="b5d04-115">Tallentaa Microsoft Azure Active Directoryn (Azure AD) kertakirjautumisen todentamisevästeet.</span><span class="sxs-lookup"><span data-stu-id="b5d04-115">Store Microsoft Azure Active Directory (Azure AD) authentication cookies for single sign-on (SSO).</span></span> <span data-ttu-id="b5d04-116">Tallentaa salatut käyttäjän objektitiedot (nimen, sukunimen ja sähköpostiosoitteen).</span><span class="sxs-lookup"><span data-stu-id="b5d04-116">Stores encrypted user principal information (name, surname, email).</span></span> |
| <span data-ttu-id="b5d04-117">&#95;msdyn365___cart&#95;</span><span class="sxs-lookup"><span data-stu-id="b5d04-117">&#95;msdyn365___cart&#95;</span></span>                           | <span data-ttu-id="b5d04-118">Tallentaa ostoskorin tunnukset, jolla saadaan luettelo ostoskoriesiintymään lisätyistä tuotteista.</span><span class="sxs-lookup"><span data-stu-id="b5d04-118">Store cart ID used to obtain list of products added to cart instance.</span></span> |
| <span data-ttu-id="b5d04-119">&#95;msdyn365___ucc&#95;</span><span class="sxs-lookup"><span data-stu-id="b5d04-119">&#95;msdyn365___ucc&#95;</span></span>                            | <span data-ttu-id="b5d04-120">Evästeiden vaatimustenmukainen hyväksynnän seuranta.</span><span class="sxs-lookup"><span data-stu-id="b5d04-120">Cookie compliance consent tracking.</span></span>                          |
| <span data-ttu-id="b5d04-121">ai_session</span><span class="sxs-lookup"><span data-stu-id="b5d04-121">ai_session</span></span>                                  | <span data-ttu-id="b5d04-122">Määrittää, kuinka moni käyttäjän tehtäväistunto on sisältänyt tiettyjä sivuja ja sovelluksen toimintoja.</span><span class="sxs-lookup"><span data-stu-id="b5d04-122">Detects how many sessions of user activity have included certain pages and features of the app.</span></span> |
| <span data-ttu-id="b5d04-123">ai_user</span><span class="sxs-lookup"><span data-stu-id="b5d04-123">ai_user</span></span>                                     | <span data-ttu-id="b5d04-124">Määrittää, kuinka moni henkilö on käyttänyt sovellusta ja sen toimintoja.</span><span class="sxs-lookup"><span data-stu-id="b5d04-124">Detects how many people used the app and its features.</span></span> <span data-ttu-id="b5d04-125">Käyttäjien laskennassa käytetään anonyymeja tunnuksia.</span><span class="sxs-lookup"><span data-stu-id="b5d04-125">Users are counted using anonymous IDs.</span></span> |
| <span data-ttu-id="b5d04-126">b2cru</span><span class="sxs-lookup"><span data-stu-id="b5d04-126">b2cru</span></span>                                       | <span data-ttu-id="b5d04-127">Tallentaa uudelleenohjauksen URL-osoitteen dynaamisesti.</span><span class="sxs-lookup"><span data-stu-id="b5d04-127">Stores redirect URL dynamically.</span></span>                              |
| <span data-ttu-id="b5d04-128">JSESSESSIID</span><span class="sxs-lookup"><span data-stu-id="b5d04-128">JSESSIONID</span></span>                                  | <span data-ttu-id="b5d04-129">Adyen-maksuyhdistin käyttää käyttäjäistunnon tallentamiseen.</span><span class="sxs-lookup"><span data-stu-id="b5d04-129">Used by payment connector Adyen to store user session.</span></span>       |
| <span data-ttu-id="b5d04-130">OpenIdConnect.nonce.&#42;</span><span class="sxs-lookup"><span data-stu-id="b5d04-130">OpenIdConnect.nonce.&#42;</span></span>                       | <span data-ttu-id="b5d04-131">Todennus</span><span class="sxs-lookup"><span data-stu-id="b5d04-131">Authentication</span></span>                                               |
| <span data-ttu-id="b5d04-132">x-ms-cpim-cache:.&#42;</span><span class="sxs-lookup"><span data-stu-id="b5d04-132">x-ms-cpim-cache:.&#42;</span></span>                          | <span data-ttu-id="b5d04-133">Käytetään pyynnön tilan ylläpitämiseen.</span><span class="sxs-lookup"><span data-stu-id="b5d04-133">Used for maintaining the request state.</span></span>                      |
| <span data-ttu-id="b5d04-134">x-ms-cpim-csrf</span><span class="sxs-lookup"><span data-stu-id="b5d04-134">x-ms-cpim-csrf</span></span>                              | <span data-ttu-id="b5d04-135">Jaetun julkaisuoikeuspyynnön väärentämisen (CRSF) tunnus, jota käytetään CRSF-väärennökseltä suojautumiseen.</span><span class="sxs-lookup"><span data-stu-id="b5d04-135">Cross-site request forgery (CRSF) token used for protection from CRSF.</span></span>     |
| <span data-ttu-id="b5d04-136">x-ms-cpim-dc</span><span class="sxs-lookup"><span data-stu-id="b5d04-136">x-ms-cpim-dc</span></span>                                | <span data-ttu-id="b5d04-137">Käytetään reitittämään pyyntöjä sopivaan tuotannon todennuspalvelinesiintymään.</span><span class="sxs-lookup"><span data-stu-id="b5d04-137">Used to route requests to the appropriate production authentication server instance.</span></span> |
| <span data-ttu-id="b5d04-138">x-ms-cpim-rc.&#42;</span><span class="sxs-lookup"><span data-stu-id="b5d04-138">x-ms-cpim-rc.&#42;</span></span>                              | <span data-ttu-id="b5d04-139">Käytetään reitittämään pyyntöjä sopivaan tuotannon todennuspalvelinesiintymään.</span><span class="sxs-lookup"><span data-stu-id="b5d04-139">Used to route requests to the appropriate production authentication server instance.</span></span> |
| <span data-ttu-id="b5d04-140">x-ms-cpim-slice</span><span class="sxs-lookup"><span data-stu-id="b5d04-140">x-ms-cpim-slice</span></span>                             | <span data-ttu-id="b5d04-141">Käytetään reitittämään pyyntöjä sopivaan tuotannon todennuspalvelinesiintymään.</span><span class="sxs-lookup"><span data-stu-id="b5d04-141">Used to route requests to the appropriate production authentication server instance.</span></span> |
| <span data-ttu-id="b5d04-142">x-ms-cpim-sso:rushmoreb2c.onmicrosoft.com_0</span><span class="sxs-lookup"><span data-stu-id="b5d04-142">x-ms-cpim-sso:rushmoreb2c.onmicrosoft.com_0</span></span> | <span data-ttu-id="b5d04-143">Käytetään kertakirjautumisistunnon ylläpitämiseen.</span><span class="sxs-lookup"><span data-stu-id="b5d04-143">Used for maintaining the SSO session.</span></span>                        |
| <span data-ttu-id="b5d04-144">x-ms-cpim-trans</span><span class="sxs-lookup"><span data-stu-id="b5d04-144">x-ms-cpim-trans</span></span>                             | <span data-ttu-id="b5d04-145">Käytetään tapahtumien seurantaan (kuluttajakauppasivustossa todennettavien avoimien välilehtien määrä), mikä sisältää myös nykyisen tapahtuman.</span><span class="sxs-lookup"><span data-stu-id="b5d04-145">Used for tracking transactions (the number of open tabs authenticating against a business-to-consumer (B2C) site), including the current transaction.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="b5d04-146">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="b5d04-146">Additional resources</span></span>

[<span data-ttu-id="b5d04-147">Helppokäyttöisyyden toiminnot ja ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="b5d04-147">Accessibility features and capabilities</span></span>](accessibility.md)

[<span data-ttu-id="b5d04-148">Yhteensopivuuden yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="b5d04-148">Compliance overview</span></span>](compliance-overview.md)

[<span data-ttu-id="b5d04-149">Lisää tietosuojakäytäntösivu</span><span class="sxs-lookup"><span data-stu-id="b5d04-149">Add a privacy policy page</span></span>](add-privacy-page.md)

[<span data-ttu-id="b5d04-150">Seurattuihin sisällönmuutoksiin liittyvien käyttäjätunnusten korvaaminen</span><span class="sxs-lookup"><span data-stu-id="b5d04-150">Replace user IDs associated with tracked content changes</span></span>](replace-IDs-tracked-changes.md)
