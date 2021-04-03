---
title: Sivuston valitsinmoduuli
description: Tässä ohjeaiheessa käsitellään sivuston valitsinmoduulia ja sen lisäämistä sivuston sivuille Microsoft Dynamics 365 Commercessa.
author: anupamar-ms
manager: annbe
ms.date: 10/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: e24590d4a8f172809704aab0d761f6db0fb0e11b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5234338"
---
# <a name="site-selector-module"></a><span data-ttu-id="d3df8-103">Toimipaikan valitsinmoduuli</span><span class="sxs-lookup"><span data-stu-id="d3df8-103">Site selector module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="d3df8-104">Tässä ohjeaiheessa käsitellään sivuston valitsinmoduulia ja sen lisäämistä sivuston sivuille Microsoft Dynamics 365 Commercessa.</span><span class="sxs-lookup"><span data-stu-id="d3df8-104">This topic covers the site selector module and describes how to add it to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="d3df8-105">Jos yrityksellä on useita sivustoja eri markkinoilla, alueilla ja kielialueilla, sivuston käyttäjät tarvitsevat kätevän tavan vaihdella sivustoja ja valitse ensisijaisen ostossivuston.</span><span class="sxs-lookup"><span data-stu-id="d3df8-105">When a business has different sites across markets, regions, and locales, site users need an easy way to switch between sites and select their preferred shopping site.</span></span> <span data-ttu-id="d3df8-106">Tätä skenaariota varten käyttäjät voivat selata useita sivustoja sivuston valitsinmoduulin ansiosta.</span><span class="sxs-lookup"><span data-stu-id="d3df8-106">To accommodate this scenario, the site selector module lets users browse across multiple sites.</span></span>

<span data-ttu-id="d3df8-107">Sivuston valitsinmoduuli on määritettävä käyttämällä sivustoluetteloa (markkinat, alueet tai kielialueet), jota sivuston käyttäjät voivat selata.</span><span class="sxs-lookup"><span data-stu-id="d3df8-107">The site selector module must be configured with the list of sites (markets, regions, or locales) that site users can browse.</span></span>

> [!NOTE]
> <span data-ttu-id="d3df8-108">Sivuston valitsinmoduuli on käytettävissä Dynamics 365 Commercen versiossa 10.0.14.</span><span class="sxs-lookup"><span data-stu-id="d3df8-108">The site selector module is available in the Dynamics 365 Commerce 10.0.14 release.</span></span>

<span data-ttu-id="d3df8-109">Seuraavassa kuvassa on esimerkki sivuston sivun otsikossa olevasta sivuston valitsinmoduulista.</span><span class="sxs-lookup"><span data-stu-id="d3df8-109">The following illustration shows an example of a site selector module that is featured in the header of a site page.</span></span>

![Esimerkki sivuston valitsinmoduulista sivustonsivun otsikossa](./media/ecommerce-sitepicker.PNG)

## <a name="site-selector-module-properties"></a><span data-ttu-id="d3df8-111">Sivuston valitsinmoduulin ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="d3df8-111">Site selector module properties</span></span>

| <span data-ttu-id="d3df8-112">Ominaisuuden nimi</span><span class="sxs-lookup"><span data-stu-id="d3df8-112">Property name</span></span> | <span data-ttu-id="d3df8-113">Arvo</span><span class="sxs-lookup"><span data-stu-id="d3df8-113">Value</span></span>                 | <span data-ttu-id="d3df8-114">kuvaus</span><span class="sxs-lookup"><span data-stu-id="d3df8-114">Description</span></span> |
|---------------|-----------------------|-------------|
| <span data-ttu-id="d3df8-115">Otsikko</span><span class="sxs-lookup"><span data-stu-id="d3df8-115">Heading</span></span>       | <span data-ttu-id="d3df8-116">Teksti</span><span class="sxs-lookup"><span data-stu-id="d3df8-116">Text</span></span>                  | <span data-ttu-id="d3df8-117">Moduulin otsikko.</span><span class="sxs-lookup"><span data-stu-id="d3df8-117">The heading for the module.</span></span> |
| <span data-ttu-id="d3df8-118">Sivustoasetukset</span><span class="sxs-lookup"><span data-stu-id="d3df8-118">Site options</span></span>  | <span data-ttu-id="d3df8-119">Nimi, kuva, URL</span><span class="sxs-lookup"><span data-stu-id="d3df8-119">Name, Image, URL</span></span>      | <span data-ttu-id="d3df8-120">Tämä ominaisuus määrittää nimen, linkin sivuston aloitussivulle ja valinnaisen kuvan, jonka jokainen moduuliin kuuluva sivusto näkee.</span><span class="sxs-lookup"><span data-stu-id="d3df8-120">This property specifies a name, a link to the site's home page, and an optional image to show for each site that is included in the module.</span></span> <span data-ttu-id="d3df8-121">Kuva voi olla lippu tai jotakin muuta, joka ilmaisee markkinan, alueen tai kielialueen.</span><span class="sxs-lookup"><span data-stu-id="d3df8-121">The image can be a flag, or some representation of a market, region, or locale.</span></span> |

## <a name="add-a-site-selector-module-to-a-page"></a><span data-ttu-id="d3df8-122">Sivuston valitsinmoduulin lisääminen sivulle</span><span class="sxs-lookup"><span data-stu-id="d3df8-122">Add a site selector module to a page</span></span>

<span data-ttu-id="d3df8-123">Sivuston valitsinmoduuli voidaan lisätä [otsikkomoduuliin](author-header-module.md) sivuston valitsinpaikan alapuolelle.</span><span class="sxs-lookup"><span data-stu-id="d3df8-123">The site selector module can be added to the [Header module](author-header-module.md) under the site selector slot.</span></span> <span data-ttu-id="d3df8-124">Kun moduuli on lisätty, voit määrittää sen otsikon ja sivustovaihtoehdot.</span><span class="sxs-lookup"><span data-stu-id="d3df8-124">After it's added, you can define the module heading and site options.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d3df8-125">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="d3df8-125">Additional resources</span></span>

[<span data-ttu-id="d3df8-126">Moduulikirjaston yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="d3df8-126">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="d3df8-127">Ylätunnistemoduuli</span><span class="sxs-lookup"><span data-stu-id="d3df8-127">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="d3df8-128">Navigointipolkumoduuli</span><span class="sxs-lookup"><span data-stu-id="d3df8-128">Breadcrumb module</span></span>](add-breadcrumb.md)

[<span data-ttu-id="d3df8-129">Siirtymisvalikkomoduulit</span><span class="sxs-lookup"><span data-stu-id="d3df8-129">Navigation menu module</span></span>](nav-menu-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]