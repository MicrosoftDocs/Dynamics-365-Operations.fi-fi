---
title: Evästeen hyväksyntämoduuli
description: Tässä ohjeaiheessa on tietoja evästeiden hyväksyntämoduuleista ja niiden lisäämisestä sivuston sivuille Microsoft Dynamics 365 Commercessa.
author: anupamar-ms
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 2f0118b197f465113bb894e3e57b3e682e04ef36
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5796000"
---
# <a name="cookie-consent-module"></a><span data-ttu-id="4b61a-103">Evästeiden hyväksynnän moduuli</span><span class="sxs-lookup"><span data-stu-id="4b61a-103">Cookie consent module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="4b61a-104">Tässä ohjeaiheessa on tietoja evästeiden hyväksyntämoduuleista ja niiden lisäämisestä sivuston sivuille Microsoft Dynamics 365 Commercessa.</span><span class="sxs-lookup"><span data-stu-id="4b61a-104">This topic covers cookie consent modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="4b61a-105">Evästeiden hyväksyntämoduuli kehottaa sivuston käyttäjiä eksplisiittisesti antamaan suostumuksen evästeiden sallimiseksi mille tahansa selaimen evästeitä jäljittävälle ominaisuudelle tai moduulille.</span><span class="sxs-lookup"><span data-stu-id="4b61a-105">The cookie consent module prompts site users to explicitly provide consent to allow cookies for any feature or module that tracks browser cookies.</span></span> <span data-ttu-id="4b61a-106">Suostumus on pakollinen, kun sivuston käyttäjä selaa sivustoa ensimmäistä kertaa uudessa selainistunnossa.</span><span class="sxs-lookup"><span data-stu-id="4b61a-106">The consent is required the first time a site user browses a site in a new browser session.</span></span> <span data-ttu-id="4b61a-107">Kun suostumus vastaanotetaan, sitä seurataan eikä sivuston käyttäjältä kysytä hyväksyntää uudelleen.</span><span class="sxs-lookup"><span data-stu-id="4b61a-107">When consent is received, it is tracked and the site user will not be prompted for consent again.</span></span> <span data-ttu-id="4b61a-108">Lisätietoja on kohdassa [Evästeiden vaatimustenmukaisuus](cookie-compliance.md).</span><span class="sxs-lookup"><span data-stu-id="4b61a-108">For more information, see [Cookie compliance](cookie-compliance.md).</span></span>

<span data-ttu-id="4b61a-109">Jos sivuston käyttäjän evästeiden suostumusta ei saada, mitään evästeiden hyväksyntää edellyttäviä toimintoja tai moduuleja ei muodosteta sivulla.</span><span class="sxs-lookup"><span data-stu-id="4b61a-109">If site user cookie consent is not received, any features or modules that require cookie consent will not be rendered on the page.</span></span> <span data-ttu-id="4b61a-110">Esimerkiksi kassamoduuli, yhteisöpalvelun jakamisen moduuli ja ensisijainen myymälän ominaisuus vaativat evästeiden suostumuksen. Niitä ei muodosteta, jos sivuston käyttäjän suostumusta ei saada.</span><span class="sxs-lookup"><span data-stu-id="4b61a-110">For example, the checkout module, social share module, and preferred store feature all require cookie consent and will not be rendered if site user consent is not received.</span></span> 

<span data-ttu-id="4b61a-111">Evästeiden hyväksyntämoduuli voidaan konfiguroida sivun otsikko-osaan, jotta se voidaan pakottaa sivun latautuessa.</span><span class="sxs-lookup"><span data-stu-id="4b61a-111">A cookie consent module can be configured on a page's header fragment so that it can be enforced when the page loads.</span></span> <span data-ttu-id="4b61a-112">Evästeiden hyväksyntämoduulissa tulisi olla selkeä sanoma, jossa ilmoitetaan sivuston käyttäjälle evästeiden käytöstä. Sen tulisi sisältää linkki sivuston tietosuojasivulle.</span><span class="sxs-lookup"><span data-stu-id="4b61a-112">The cookie consent module should have a clear message informing the site user about cookie usage on the site and should provide a link to the site's privacy page.</span></span>

<span data-ttu-id="4b61a-113">Seuraavassa kuvassa on esimerkki evästeiden hyväksymisviestistä sekä linkki sivuston tietosuojakäytännön sivulle. Se näkyy sivuston sivun otsikossa.</span><span class="sxs-lookup"><span data-stu-id="4b61a-113">The following illustration highlights an example of a cookie consent message with a link to the site's privacy policy page displayed on the header of a site page.</span></span>
<span data-ttu-id="4b61a-114">![Esimerkki evästeiden hyväksyntämoduulista](./media/ecommerce-cookieconsent.png)</span><span class="sxs-lookup"><span data-stu-id="4b61a-114">![Example of a cookie consent module](./media/ecommerce-cookieconsent.png)</span></span>

## <a name="cookie-consent-module-properties"></a><span data-ttu-id="4b61a-115">Evästeen hyväksyntämoduulin ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="4b61a-115">Cookie consent module properties</span></span>

| <span data-ttu-id="4b61a-116">Ominaisuuden nimi</span><span class="sxs-lookup"><span data-stu-id="4b61a-116">Property name</span></span>             | <span data-ttu-id="4b61a-117">Arvo</span><span class="sxs-lookup"><span data-stu-id="4b61a-117">Value</span></span>                 | <span data-ttu-id="4b61a-118">kuvaus</span><span class="sxs-lookup"><span data-stu-id="4b61a-118">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="4b61a-119">Muotoiltu teksti</span><span class="sxs-lookup"><span data-stu-id="4b61a-119">Rich Text</span></span>                  | <span data-ttu-id="4b61a-120">Muotoiltu teksti</span><span class="sxs-lookup"><span data-stu-id="4b61a-120">Rich Text</span></span> | <span data-ttu-id="4b61a-121">Määrittää sivuston käyttäjille RTF-ilmoituksen, jonka mukaan sivusto käyttää selaimen evästeitä ja käyttäjien on hyväksyttävä evästeiden käyttö, jotta sivusto on täysin toimintakykyinen.</span><span class="sxs-lookup"><span data-stu-id="4b61a-121">Specifies a Rich Text notification to site users that the site uses browser cookies and that users should accept the use of cookies for the site to be fully functional.</span></span> |
| <span data-ttu-id="4b61a-122">Linkit</span><span class="sxs-lookup"><span data-stu-id="4b61a-122">Links</span></span> | <span data-ttu-id="4b61a-123">URL</span><span class="sxs-lookup"><span data-stu-id="4b61a-123">URL</span></span> | <span data-ttu-id="4b61a-124">Sivuston tietosuojasivulle voidaan lisätä linkkejä, jotka kuvaavat sivustossa seurattavien evästeiden tyyppejä.</span><span class="sxs-lookup"><span data-stu-id="4b61a-124">One or more links can be added to a site's privacy page that describes the types of cookies that are tracked on the site.</span></span> |

## <a name="add-a-cookie-consent-module-to-site-pages"></a><span data-ttu-id="4b61a-125">Evästeiden hyväksyntämoduulin lisääminen sivuston sivuille</span><span class="sxs-lookup"><span data-stu-id="4b61a-125">Add a cookie consent module to site pages</span></span>

<span data-ttu-id="4b61a-126">Jotta evästeiden hyväksyntämoduuli voidaan lisätä tehokkaasti useille sivuston sivuille, sen voi lisätä jaettuun sivun otsikon osaan.</span><span class="sxs-lookup"><span data-stu-id="4b61a-126">To efficiently add a cookie consent module to multiple site pages, it can be added to a shared page header fragment.</span></span> <span data-ttu-id="4b61a-127">Kun otsikon osa on lisätty kaikkiin sivuston sivuihin, evästeiden hyväksyntäilmoitus muodostetaan automaattisesti, kun sivuston käyttäjä siirtyy sivuston sivulle ensimmäisen kerran.</span><span class="sxs-lookup"><span data-stu-id="4b61a-127">After the header fragment is added to all site pages, a cookie consent notification will automatically be rendered the first time a site user navigates to any site page.</span></span>

<span data-ttu-id="4b61a-128">Lisätietoja otsikon otsikon ja moduuleista on kohdassa [Otsikkomoduuli](author-header-module.md).</span><span class="sxs-lookup"><span data-stu-id="4b61a-128">For more information about header fragments and modules, see [Header module](author-header-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4b61a-129">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="4b61a-129">Additional resources</span></span>

[<span data-ttu-id="4b61a-130">Moduulikirjaston yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="4b61a-130">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="4b61a-131">Ylätunnistemoduuli</span><span class="sxs-lookup"><span data-stu-id="4b61a-131">Header module</span></span>](author-header-module.md) 

[<span data-ttu-id="4b61a-132">Evästeen yhteensopivuus</span><span class="sxs-lookup"><span data-stu-id="4b61a-132">Cookie compliance</span></span>](cookie-compliance.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]