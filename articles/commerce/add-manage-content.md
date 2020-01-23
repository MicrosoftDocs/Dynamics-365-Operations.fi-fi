---
title: Tapoja lisästä sisältöä
description: Tässä ohjeaiheessa on tietoja Microsoft Dynamics 365 Commerce -sivuston sisällön lisäämisestä ja hallinnasta.
author: phinneyridge
manager: annbe
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 2232dc7cdd24416b0df0919b96cd5d1f8113299f
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/20/2019
ms.locfileid: "2914651"
---
# <a name="ways-to-add-content"></a><span data-ttu-id="fd9cb-103">Tapoja lisästä sisältöä</span><span class="sxs-lookup"><span data-stu-id="fd9cb-103">Ways to add content</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="fd9cb-104">Tässä ohjeaiheessa on tietoja Microsoft Dynamics 365 Commerce -sivuston sisällön lisäämisestä ja hallinnasta.</span><span class="sxs-lookup"><span data-stu-id="fd9cb-104">This topic provides information about how to add and manage content on your Microsoft Dynamics 365 Commerce site.</span></span>

## <a name="overview"></a><span data-ttu-id="fd9cb-105">Yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="fd9cb-105">Overview</span></span>

<span data-ttu-id="fd9cb-106">Sivuston ulkoasua, ulkoasua ja sisältöä voi muuttaa monella tavalla.</span><span class="sxs-lookup"><span data-stu-id="fd9cb-106">There are many ways to change the look, feel, and content of your site.</span></span> <span data-ttu-id="fd9cb-107">Monet näistä muutoksista voidaan toteuttaa muiden kuin kehittäjien toimesta riippuen vaaditusta mukautustasosta.</span><span class="sxs-lookup"><span data-stu-id="fd9cb-107">Depending on the required level of customization, many of these changes can be implemented by non-developers.</span></span> <span data-ttu-id="fd9cb-108">Esimerkiksi koodia ei tarvitse kirjoittaa mallien luomisessa, teemojen valitsemisessa ja moduulien valitsemisessa ja määrittämisessä.</span><span class="sxs-lookup"><span data-stu-id="fd9cb-108">For example, no code has to be written to build templates, select themes, and select and configure modules.</span></span> <span data-ttu-id="fd9cb-109">Sen sijaan kehitystaitoja vaaditaan uuden teeman tai moduulin luomisessa, koska sähköisen kaupankäynnin SDK:n ja Microsoft Dynamics Lifecycle Services (LCS) -palvelun kehitystyönkulkua on käytettävä.</span><span class="sxs-lookup"><span data-stu-id="fd9cb-109">By contrast, development skills are required to create a new theme or module, because the e-Commerce software development kit (SDK) and the Microsoft Dynamics Lifecycle Services (LCS) deployment workflow must be used.</span></span>

<span data-ttu-id="fd9cb-110">Seuraavissa ohjeaiheissa on eriteltyjä tietoja sivuston sisällön lisäämisestä ja hallinnasta.</span><span class="sxs-lookup"><span data-stu-id="fd9cb-110">The following topics provide detailed information about how to add and manage site content.</span></span> <span data-ttu-id="fd9cb-111">Ne keskittyvät sivuston alueille, jotka eivät vaadi kehittäjää.</span><span class="sxs-lookup"><span data-stu-id="fd9cb-111">They focus on areas of your site that don't require a developer.</span></span> <span data-ttu-id="fd9cb-112">Niissä kerrotaan tehtävistä, joissa tarvitaan SDK.</span><span class="sxs-lookup"><span data-stu-id="fd9cb-112">As required, they point out tasks that require SDK work.</span></span>

- <span data-ttu-id="fd9cb-113">Lisätietoja aiemmin luodun sivustosivun tekstin, kuvien tai videoiden muuttamisesta on kohdassa [Moduulien käsitteleminen](work-with-modules.md).</span><span class="sxs-lookup"><span data-stu-id="fd9cb-113">To change the text, images, or video on an existing site page, see [Work with modules](work-with-modules.md).</span></span>
- <span data-ttu-id="fd9cb-114">Jos haluat varmistaa, että verkon sisällöntuottajat voivat käyttää tuotemerkkejä, katso lisätietoja kohdasta [Mallien käsitteleminen](work-with-templates.md).</span><span class="sxs-lookup"><span data-stu-id="fd9cb-114">To help guarantee a foolproof, on-brand authoring experience for web content authors, see [Work with templates](work-with-templates.md).</span></span>
- <span data-ttu-id="fd9cb-115">Lisätietoja sivustosivun osien uudelleenjärjestämisestä on kohdassa [Asettelujen käsitteleminen](work-with-layouts.md).</span><span class="sxs-lookup"><span data-stu-id="fd9cb-115">To rearrange sections on a site page, see [Work with layouts](work-with-layouts.md).</span></span>
- <span data-ttu-id="fd9cb-116">Lisätietoja sivustosivujen fonttien, värien ja yleisen ulkoasun muuttamisesta on kohdassa [sivuston teeman valitseminen](select-site-theme.md).</span><span class="sxs-lookup"><span data-stu-id="fd9cb-116">To change the fonts, colors, and general look of site pages, see [Select a site theme](select-site-theme.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="fd9cb-117">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="fd9cb-117">Additional resources</span></span>

[<span data-ttu-id="fd9cb-118">Sivumallisanasto</span><span class="sxs-lookup"><span data-stu-id="fd9cb-118">Page model glossary</span></span>](page-elements-overview.md)

[<span data-ttu-id="fd9cb-119">Asiakirjan tilat ja elinkaari</span><span class="sxs-lookup"><span data-stu-id="fd9cb-119">Document states and lifecycle</span></span>](document-states-overview.md)

[<span data-ttu-id="fd9cb-120">Julkaisuryhmien kanssa työskenteleminen</span><span class="sxs-lookup"><span data-stu-id="fd9cb-120">Work with publish groups</span></span>](publish-groups.md)

[<span data-ttu-id="fd9cb-121">Moduulien käyttäminen</span><span class="sxs-lookup"><span data-stu-id="fd9cb-121">Work with modules</span></span>](work-with-modules.md)

[<span data-ttu-id="fd9cb-122">Katkelmien käyttäminen</span><span class="sxs-lookup"><span data-stu-id="fd9cb-122">Work with fragments</span></span>](work-with-fragments.md)

[<span data-ttu-id="fd9cb-123">Mallit ja asettelut – yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="fd9cb-123">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="fd9cb-124">Sivuston selauksen mukauttaminen</span><span class="sxs-lookup"><span data-stu-id="fd9cb-124">Customize site navigation</span></span>](customize-site-navigation.md)
