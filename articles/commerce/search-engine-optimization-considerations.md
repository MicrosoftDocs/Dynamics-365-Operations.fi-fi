---
title: Sivuston hakukoneoptimointia (SEO) koskevia tietoja
description: Tämä ohjeaihe kattaa hakukoneoptimoinnin sivustossa kehityksestä tuotantoon.
author: psimolin
manager: annbe
ms.date: 10/01/2019
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
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: b35d0cb606e1b17a0258ea3fcb6287988d83091c
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/01/2019
ms.locfileid: "2698208"
---
# <a name="search-engine-optimization-seo-considerations-for-your-site"></a><span data-ttu-id="4890e-103">Sivuston hakukoneoptimointia (SEO) koskevia tietoja</span><span class="sxs-lookup"><span data-stu-id="4890e-103">Search engine optimization (SEO) considerations for your site</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="4890e-104">Tämä ohjeaihe kattaa hakukoneoptimoinnin sivustossa kehityksestä tuotantoon.</span><span class="sxs-lookup"><span data-stu-id="4890e-104">This topic covers earch engine optimization (SEO) considerations for your site from development to production.</span></span>

## <a name="a-site-that-is-under-development"></a><span data-ttu-id="4890e-105">Sivustoa kehitetään</span><span class="sxs-lookup"><span data-stu-id="4890e-105">A site that is under development</span></span>

<span data-ttu-id="4890e-106">Sivuston ollessa kehitettävänä sivuston kaikilla sivuilla tulisi olla **NOINDEX**- ja **NOFOLLOW**-metatunnukset. Näin hakukoneet eivät indeksoi sivuja ja tallenna sivuston kehitysversioita välimuistiin.</span><span class="sxs-lookup"><span data-stu-id="4890e-106">While a site is under development, all site pages should have the **NOINDEX** and **NOFOLLOW** meta tags, so that search engines don't index the pages and store development versions of your site in their cache.</span></span> <span data-ttu-id="4890e-107">Voit tehdä tämän määrityksen, jos sivuston sivumalliin on lisätty oletusmetatunnusten moduuli.</span><span class="sxs-lookup"><span data-stu-id="4890e-107">To do this configuration, you must add the default meta tags module to the site page template.</span></span> <span data-ttu-id="4890e-108">Oletusarvoiset metatunnusten ominaisuudet ovat tämän jälkeen hakukoneoptimoinnin ominaisuuksien osan käytettävissä sivueditorissa.</span><span class="sxs-lookup"><span data-stu-id="4890e-108">The default meta tags properties will then be available in the SEO properties section in the page editor.</span></span> <span data-ttu-id="4890e-109">Näiden ominaisuuksien avulla voit hallita metatunnuksia.</span><span class="sxs-lookup"><span data-stu-id="4890e-109">You can use these properties to manage the meta tags.</span></span>

## <a name="soft-launch-of-a-site"></a><span data-ttu-id="4890e-110">Sivuston pehmeä käynnistäminen</span><span class="sxs-lookup"><span data-stu-id="4890e-110">Soft launch of a site</span></span>

<span data-ttu-id="4890e-111">Pehmeän käynnistämisen aikana sivusto on vain rajoitetun yleisön tai markkina-alueen käyttettävissä ennen täydellisen käyttöönoton tapahtumista.</span><span class="sxs-lookup"><span data-stu-id="4890e-111">During a "soft launch," a website is made available to a limited audience or market before the full launch occurs.</span></span> <span data-ttu-id="4890e-112">Jos sivustossa tehdään pehmeä käynnistäminen, **NOINDEX**-metatunnukset kannattaa jättää paikoilleen.</span><span class="sxs-lookup"><span data-stu-id="4890e-112">If you do a soft launch of your website, you should consider leaving the **NOINDEX** meta tags in place.</span></span> <span data-ttu-id="4890e-113">Näin varmistetaan, että pehmeä käynnistys jää rajoitetun yleisön käyttöön.</span><span class="sxs-lookup"><span data-stu-id="4890e-113">In this way, you help guarantee that the soft launch remains restricted to the limited audience that you want to reach.</span></span>

## <a name="a-site-that-is-in-production"></a><span data-ttu-id="4890e-114">Sivusto, joka on tuotannossa</span><span class="sxs-lookup"><span data-stu-id="4890e-114">A site that is in production</span></span>

<span data-ttu-id="4890e-115">Kun sivusto on tuotannossa, varmista, että kaikki sivuston sivut on merkitty oikein tunnuksilla.</span><span class="sxs-lookup"><span data-stu-id="4890e-115">When a site is in production, you should make sure that all site pages are correctly tagged.</span></span> <span data-ttu-id="4890e-116">Microsoft Dynamics 365 Commerce käyttää sivulle syötettyjä tietoja sivun hakukoneoptimoinnin tietojen hahmontamisessa.</span><span class="sxs-lookup"><span data-stu-id="4890e-116">Microsoft Dynamics 365 Commerce uses the information that is entered for a page to render all the SEO information on that page.</span></span> <span data-ttu-id="4890e-117">Seuraavat moduulit tarjoavat tämän toiminnon: luokkasivun yhteenveto, luettelosivun yhteenveto ja tuotesivun yhteenveto.</span><span class="sxs-lookup"><span data-stu-id="4890e-117">The following modules provide this functionality: category page summary, list page summary, and product page summary.</span></span>

<span data-ttu-id="4890e-118">Voit optimoida hakukoneindeksoinnin, kun hahmontamisen kehys käyttää sekä Dynamics 365 Commercen määritettyjä hakukoneoptimoinnin ominaisuuksien tietoja että moduulikohtaisia tietoja.</span><span class="sxs-lookup"><span data-stu-id="4890e-118">To optimize search engine indexing, the rendering framework uses both information from the SEO properties that are configured in Dynamics 365 Commerce and module-specific information.</span></span> <span data-ttu-id="4890e-119">Jos kyseessä on sivusto, joka on tuotannossa, varmista, että robots.txt-tiedosto mahdollistaa indeksoinnin koko sivustossa ja että se sisältää linkit julkaistuun sivustokartta-asiakirjaan.</span><span class="sxs-lookup"><span data-stu-id="4890e-119">For a site that is in production, you should make sure that the robots.txt file allows for indexing of your whole site, and that it contains links to your published site map document.</span></span> <span data-ttu-id="4890e-120">Ota käyttöön sivustokartan luontitoiminto kohdassa **Sivuston asetukset \> Sivustokartta käytössä**.</span><span class="sxs-lookup"><span data-stu-id="4890e-120">You should turn on the site map generation functionality at **Site Settings \> Site maps enabled**.</span></span>

### <a name="page-seo-settings-for-internal-preview-limited-audiences-and-all-audiences"></a><span data-ttu-id="4890e-121">Sivun hakukoneoptimoinnin asetukset sisäistä esikatselua, rajoitettuja yleisöjä ja kaikkia yleisöjä varten</span><span class="sxs-lookup"><span data-stu-id="4890e-121">Page SEO settings for internal preview, limited audiences, and all audiences</span></span>

<span data-ttu-id="4890e-122">Koska Dynamics 365 Commerce tukee WYSIWYG-todennettuja esikatseluita, tekijät voivat valmistella sivun sisällön niin, ettei heidän tarvitse huolehtia siitä, että tiedot näkyvät sivustolla kävijöille.</span><span class="sxs-lookup"><span data-stu-id="4890e-122">Because Dynamics 365 Commerce supports "what you see is what you get" (WYSIWYG) authenticated previews, authors can prepare their page content without having to worry that the information will become visible to site visitors.</span></span> <span data-ttu-id="4890e-123">Jos sivu on julkaistava, mutta sen käyttöä on rajoitettava, sillä on oltava **NOINDEX**-metatunnus. Tällöin hakukoneet eivät indeksoi sitä.</span><span class="sxs-lookup"><span data-stu-id="4890e-123">If a page must be published, but its exposure must be limited, it should have the **NOINDEX** meta tag, so that it won't be indexed by search engines.</span></span> <span data-ttu-id="4890e-124">Kun sivu on valmis kaikkia varten, kaikki hakukoneoptimoinnin perusmetatiedot ovat olemassa. Näin maksimoidaan hakukoneindeksoinnin tehokkuus.</span><span class="sxs-lookup"><span data-stu-id="4890e-124">Then, when the page is ready for all audiences, all the basic SEO metadata should be present, to maximize the efficiency of search engine indexing.</span></span> <span data-ttu-id="4890e-125">Lisäksi **NOLIMIT**-metatunnus on poistettava.</span><span class="sxs-lookup"><span data-stu-id="4890e-125">Additionally, the **NOLIMIT** meta tag should be removed.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4890e-126">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="4890e-126">Additional resources</span></span>

[<span data-ttu-id="4890e-127">Sähköisen kaupankäynnin käyttäjien ja roolien hallinta</span><span class="sxs-lookup"><span data-stu-id="4890e-127">Manage e-Commerce users and roles</span></span>](manage-ecommerce-users-roles.md)

[<span data-ttu-id="4890e-128">Komentosarjakoodin lisääminen sivuston sivuihin telemetrian tukemiseksi</span><span class="sxs-lookup"><span data-stu-id="4890e-128">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

[<span data-ttu-id="4890e-129">Sisällön suojauskäytännön (CSP) hallinta</span><span class="sxs-lookup"><span data-stu-id="4890e-129">Manage Content Security Policy (CSP)</span></span>](manage-csp.md)
