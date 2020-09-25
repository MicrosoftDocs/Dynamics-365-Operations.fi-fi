---
title: Evästeen hyväksyntämoduuli
description: Tässä ohjeaiheessa on tietoja evästeiden hyväksyntämoduuleista ja niiden lisäämisestä sivuston sivuille Microsoft Dynamics 365 Commercessa.
author: anupamar-ms
manager: annbe
ms.date: 08/31/2020
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
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 842096c6e3045e434aced9642c86690e2ff7483a
ms.sourcegitcommit: 420b9e538f706178f8e1f2786e02f4f400bf2336
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/02/2020
ms.locfileid: "3761387"
---
# <a name="cookie-consent-module"></a><span data-ttu-id="e256c-103">Evästeen hyväksyntämoduuli</span><span class="sxs-lookup"><span data-stu-id="e256c-103">Cookie consent module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e256c-104">Tässä ohjeaiheessa on tietoja evästeiden hyväksyntämoduuleista ja niiden lisäämisestä sivuston sivuille Microsoft Dynamics 365 Commercessa.</span><span class="sxs-lookup"><span data-stu-id="e256c-104">This topic covers cookie consent modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="e256c-105">Yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="e256c-105">Overview</span></span>

<span data-ttu-id="e256c-106">Evästeiden hyväksyntämoduuli kehottaa sivuston käyttäjiä eksplisiittisesti antamaan suostumuksen evästeiden sallimiseksi mille tahansa selaimen evästeitä jäljittävälle ominaisuudelle tai moduulille.</span><span class="sxs-lookup"><span data-stu-id="e256c-106">The cookie consent module prompts site users to explicitly provide consent to allow cookies for any feature or module that tracks browser cookies.</span></span> <span data-ttu-id="e256c-107">Suostumus on pakollinen, kun sivuston käyttäjä selaa sivustoa ensimmäistä kertaa uudessa selainistunnossa.</span><span class="sxs-lookup"><span data-stu-id="e256c-107">The consent is required the first time a site user browses a site in a new browser session.</span></span> <span data-ttu-id="e256c-108">Kun suostumus vastaanotetaan, sitä seurataan eikä sivuston käyttäjältä kysytä hyväksyntää uudelleen.</span><span class="sxs-lookup"><span data-stu-id="e256c-108">When consent is received, it is tracked and the site user will not be prompted for consent again.</span></span> <span data-ttu-id="e256c-109">Lisätietoja on kohdassa [Evästeiden vaatimustenmukaisuus](cookie-compliance.md).</span><span class="sxs-lookup"><span data-stu-id="e256c-109">For more information, see [Cookie compliance](cookie-compliance.md).</span></span>

<span data-ttu-id="e256c-110">Jos sivuston käyttäjän evästeiden suostumusta ei saada, mitään evästeiden hyväksyntää edellyttäviä toimintoja tai moduuleja ei muodosteta sivulla.</span><span class="sxs-lookup"><span data-stu-id="e256c-110">If site user cookie consent is not received, any features or modules that require cookie consent will not be rendered on the page.</span></span> <span data-ttu-id="e256c-111">Esimerkiksi kassamoduuli, yhteisöpalvelun jakamisen moduuli ja ensisijainen myymälän ominaisuus vaativat evästeiden suostumuksen. Niitä ei muodosteta, jos sivuston käyttäjän suostumusta ei saada.</span><span class="sxs-lookup"><span data-stu-id="e256c-111">For example, the checkout module, social share module, and preferred store feature all require cookie consent and will not be rendered if site user consent is not received.</span></span> 

<span data-ttu-id="e256c-112">Evästeiden hyväksyntämoduuli voidaan konfiguroida sivun otsikko-osaan, jotta se voidaan pakottaa sivun latautuessa.</span><span class="sxs-lookup"><span data-stu-id="e256c-112">A cookie consent module can be configured on a page's header fragment so that it can be enforced when the page loads.</span></span> <span data-ttu-id="e256c-113">Evästeiden hyväksyntämoduulissa tulisi olla selkeä sanoma, jossa ilmoitetaan sivuston käyttäjälle evästeiden käytöstä. Sen tulisi sisältää linkki sivuston tietosuojasivulle.</span><span class="sxs-lookup"><span data-stu-id="e256c-113">The cookie consent module should have a clear message informing the site user about cookie usage on the site and should provide a link to the site's privacy page.</span></span>

<span data-ttu-id="e256c-114">Seuraavassa kuvassa on esimerkki evästeiden hyväksymisviestistä sekä linkki sivuston tietosuojakäytännön sivulle. Se näkyy sivuston sivun otsikossa.</span><span class="sxs-lookup"><span data-stu-id="e256c-114">The following illustration highlights an example of a cookie consent message with a link to the site's privacy policy page displayed on the header of a site page.</span></span>
<span data-ttu-id="e256c-115">![Esimerkki evästeiden hyväksyntämoduulista](./media/ecommerce-cookieconsent.png)</span><span class="sxs-lookup"><span data-stu-id="e256c-115">![Example of a cookie consent module](./media/ecommerce-cookieconsent.png)</span></span>

## <a name="cookie-consent-module-properties"></a><span data-ttu-id="e256c-116">Evästeen hyväksyntämoduulin ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="e256c-116">Cookie consent module properties</span></span>

| <span data-ttu-id="e256c-117">Ominaisuuden nimi</span><span class="sxs-lookup"><span data-stu-id="e256c-117">Property name</span></span>             | <span data-ttu-id="e256c-118">Arvo</span><span class="sxs-lookup"><span data-stu-id="e256c-118">Value</span></span>                 | <span data-ttu-id="e256c-119">kuvaus</span><span class="sxs-lookup"><span data-stu-id="e256c-119">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="e256c-120">Muotoiltu teksti</span><span class="sxs-lookup"><span data-stu-id="e256c-120">Rich Text</span></span>                  | <span data-ttu-id="e256c-121">Muotoiltu teksti</span><span class="sxs-lookup"><span data-stu-id="e256c-121">Rich Text</span></span> | <span data-ttu-id="e256c-122">Määrittää sivuston käyttäjille RTF-ilmoituksen, jonka mukaan sivusto käyttää selaimen evästeitä ja käyttäjien on hyväksyttävä evästeiden käyttö, jotta sivusto on täysin toimintakykyinen.</span><span class="sxs-lookup"><span data-stu-id="e256c-122">Specifies a Rich Text notification to site users that the site uses browser cookies and that users should accept the use of cookies for the site to be fully functional.</span></span> |
| <span data-ttu-id="e256c-123">Linkit</span><span class="sxs-lookup"><span data-stu-id="e256c-123">Links</span></span> | <span data-ttu-id="e256c-124">URL</span><span class="sxs-lookup"><span data-stu-id="e256c-124">URL</span></span> | <span data-ttu-id="e256c-125">Sivuston tietosuojasivulle voidaan lisätä linkkejä, jotka kuvaavat sivustossa seurattavien evästeiden tyyppejä.</span><span class="sxs-lookup"><span data-stu-id="e256c-125">One or more links can be added to a site's privacy page that describes the types of cookies that are tracked on the site.</span></span> |

## <a name="add-a-cookie-consent-module-to-site-pages"></a><span data-ttu-id="e256c-126">Evästeiden hyväksyntämoduulin lisääminen sivuston sivuille</span><span class="sxs-lookup"><span data-stu-id="e256c-126">Add a cookie consent module to site pages</span></span>

<span data-ttu-id="e256c-127">Jotta evästeiden hyväksyntämoduuli voidaan lisätä tehokkaasti useille sivuston sivuille, sen voi lisätä jaettuun sivun otsikon osaan.</span><span class="sxs-lookup"><span data-stu-id="e256c-127">To efficiently add a cookie consent module to multiple site pages, it can be added to a shared page header fragment.</span></span> <span data-ttu-id="e256c-128">Kun otsikon osa on lisätty kaikkiin sivuston sivuihin, evästeiden hyväksyntäilmoitus muodostetaan automaattisesti, kun sivuston käyttäjä siirtyy sivuston sivulle ensimmäisen kerran.</span><span class="sxs-lookup"><span data-stu-id="e256c-128">After the header fragment is added to all site pages, a cookie consent notification will automatically be rendered the first time a site user navigates to any site page.</span></span>

<span data-ttu-id="e256c-129">Lisätietoja otsikon otsikon ja moduuleista on kohdassa [Otsikkomoduuli](author-header-module.md).</span><span class="sxs-lookup"><span data-stu-id="e256c-129">For more information about header fragments and modules, see [Header module](author-header-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e256c-130">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="e256c-130">Additional resources</span></span>

[<span data-ttu-id="e256c-131">Aloituspakkauksen yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="e256c-131">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="e256c-132">Ylätunnistemoduuli</span><span class="sxs-lookup"><span data-stu-id="e256c-132">Header module</span></span>](author-header-module.md) 

[<span data-ttu-id="e256c-133">Evästeen yhteensopivuus</span><span class="sxs-lookup"><span data-stu-id="e256c-133">Cookie compliance</span></span>](cookie-compliance.md)
