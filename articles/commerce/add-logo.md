---
title: Logon lisääminen
description: Tässä ohjeaiheessa kerrotaan, miten logo lisätään sivustollesi Microsoft Dynamics 365 Commerce -sovelluksessa.
author: bicyclingfool
manager: AnnBe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: f15680deb0eab763ba68f2897139c915d1f8a6a3
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4411919"
---
# <a name="add-a-logo"></a><span data-ttu-id="03446-103">Logon lisääminen</span><span class="sxs-lookup"><span data-stu-id="03446-103">Add a logo</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="03446-104">Tässä ohjeaiheessa kerrotaan, miten logo lisätään sivustollesi Microsoft Dynamics 365 Commerce -sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="03446-104">This topic describes how to add a logo to your site in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="03446-105">Yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="03446-105">Overview</span></span>

<span data-ttu-id="03446-106">Kun rakennat sivustoasi, yksi ensimmäisistä asioista, jonka luultavasti teet, on lisätä yrityksesi tai brändin logo sivuston otsikkoon.</span><span class="sxs-lookup"><span data-stu-id="03446-106">When you build your site, one of the first things that you will probably do is add your company or brand logo to the site's header.</span></span> <span data-ttu-id="03446-107">Dynamics 365 Commerce -online-moduulikirjasto tarjoaa moduulin, joka tekee tästä tehtävästä helppoa.</span><span class="sxs-lookup"><span data-stu-id="03446-107">The Dynamics 365 Commerce online module library provides a module that makes this task easy.</span></span>

<span data-ttu-id="03446-108">Voit lisätä logon suoraan malliin, asetteluun tai sivulle.</span><span class="sxs-lookup"><span data-stu-id="03446-108">You can add a logo directly to a template, layout, or page.</span></span> <span data-ttu-id="03446-109">Tällä tavoin voit helposti muuttaa tietyillä sivuilla tai sivuryhmillä näkyvää logoa.</span><span class="sxs-lookup"><span data-stu-id="03446-109">In this way, you can easily change the logo that appears on specific pages or groups of pages.</span></span> <span data-ttu-id="03446-110">Tämä ohjeaihe kattaa kuitenkin yleisimmät skenaariot, joissa lisäät logon otsikon osioihin, joita voidaan käyttää uudelleen kaikilla sivustosi sivuilla.</span><span class="sxs-lookup"><span data-stu-id="03446-110">However, this topic covers the most frequent scenario, where you add your logo to a header fragment that can be reused across all the pages of your site.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="03446-111">Edellytykset</span><span class="sxs-lookup"><span data-stu-id="03446-111">Prerequisites</span></span>

<span data-ttu-id="03446-112">Ennen kuin voit lisätä logon sivustosi kaikille sivuille, sinun on suoritettava nämä tehtävät.</span><span class="sxs-lookup"><span data-stu-id="03446-112">Before you can add a logo to all the pages of your site, you must complete these tasks.</span></span>

1. <span data-ttu-id="03446-113">Lataa logo mediakirjastoon.</span><span class="sxs-lookup"><span data-stu-id="03446-113">Upload your logo to the Media Library.</span></span>
1. <span data-ttu-id="03446-114">Luo otsikko-osa.</span><span class="sxs-lookup"><span data-stu-id="03446-114">Create a header fragment.</span></span> <span data-ttu-id="03446-115">Lisätietoja osien luomisesta ja käyttämisestä on kohdassa [osien käyttäminen](work-with-fragments.md).</span><span class="sxs-lookup"><span data-stu-id="03446-115">For more information about how to create and use fragments, see [Work with fragments](work-with-fragments.md).</span></span>
1. <span data-ttu-id="03446-116">Sisällytä otsikon osa malliin, jota sivustosi sivut käyttävät asettelu- ja moduulivaihtoehtoihin.</span><span class="sxs-lookup"><span data-stu-id="03446-116">Include the header fragment in the template that the pages of your site use for their layout and module options.</span></span> <span data-ttu-id="03446-117">Lisätietoja malleista on osiossa [Mallien avulla työskentely](work-with-templates.md).</span><span class="sxs-lookup"><span data-stu-id="03446-117">For more information about templates, see [Work with templates](work-with-templates.md).</span></span>

## <a name="add-a-logo-to-a-header-fragment"></a><span data-ttu-id="03446-118">Logon lisääminen otsikko-osaan</span><span class="sxs-lookup"><span data-stu-id="03446-118">Add a logo to a header fragment</span></span>

<span data-ttu-id="03446-119">Jos haluat lisätä logon sivustosi otsikko-osaan, toimi seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="03446-119">To add a logo to the header fragment for your site, follow these steps.</span></span>

1. <span data-ttu-id="03446-120">Valitse vasemmanpuoleisessa siirtymisruudussa **Osat**.</span><span class="sxs-lookup"><span data-stu-id="03446-120">In the navigation pane on the left, select **Fragments**.</span></span>
1. <span data-ttu-id="03446-121">Valitse aiemmin luomasi otsikon osa ja valitse sitten **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="03446-121">Select the header fragment that you created, and then select **Edit**.</span></span>
1. <span data-ttu-id="03446-122">Laajenna otsikkomoduuli.</span><span class="sxs-lookup"><span data-stu-id="03446-122">Expand the header module.</span></span>
1. <span data-ttu-id="03446-123">Anna logon kuva ja linkki otsikkomoduulin ominaisuusruudussa.</span><span class="sxs-lookup"><span data-stu-id="03446-123">In the property pane for the header module, provide an image and link for the logo.</span></span> 
1. <span data-ttu-id="03446-124">Tallenna otsikko-osa, lopeta sen muokkaus ja julkaise se.</span><span class="sxs-lookup"><span data-stu-id="03446-124">Save the header fragment, finish editing it, and publish it.</span></span>

<span data-ttu-id="03446-125">Kun olet julkaissut päivitetyn otsikon osan, kaikki ylätunnisteosan sisältävää mallia käyttävät sivuston sivut näyttävät logon.</span><span class="sxs-lookup"><span data-stu-id="03446-125">After you publish the updated header fragment, all site pages that use the template that contains the header fragment will show your logo.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="03446-126">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="03446-126">Additional resources</span></span>

[<span data-ttu-id="03446-127">Sivuston teeman valitseminen</span><span class="sxs-lookup"><span data-stu-id="03446-127">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="03446-128">CSS-ohitustiedostojen parissa työskentely</span><span class="sxs-lookup"><span data-stu-id="03446-128">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="03446-129">Favicon-kuvakkeen lisääminen</span><span class="sxs-lookup"><span data-stu-id="03446-129">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="03446-130">Tervetuloviestin lisääminen</span><span class="sxs-lookup"><span data-stu-id="03446-130">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="03446-131">Copyright-ilmoituksen lisääminen</span><span class="sxs-lookup"><span data-stu-id="03446-131">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="03446-132">Kielten lisääminen sivustoon</span><span class="sxs-lookup"><span data-stu-id="03446-132">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="03446-133">Komentosarjakoodin lisääminen sivuston sivuihin telemetrian tukemiseksi</span><span class="sxs-lookup"><span data-stu-id="03446-133">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

