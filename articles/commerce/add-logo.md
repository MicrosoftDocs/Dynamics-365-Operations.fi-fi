---
title: Logon lisääminen
description: Tässä ohjeaiheessa kerrotaan, miten logo lisätään sivustollesi Microsoft Dynamics 365 Commerce -sovelluksessa.
author: bicyclingfool
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: d9e1cba6bd07e0c3d9ed7d741d87e10837d8021c
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797596"
---
# <a name="add-a-logo"></a><span data-ttu-id="67976-103">Logon lisääminen</span><span class="sxs-lookup"><span data-stu-id="67976-103">Add a logo</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="67976-104">Tässä ohjeaiheessa kerrotaan, miten logo lisätään sivustollesi Microsoft Dynamics 365 Commerce -sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="67976-104">This topic describes how to add a logo to your site in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="67976-105">Kun rakennat sivustoasi, yksi ensimmäisistä asioista, jonka luultavasti teet, on lisätä yrityksesi tai brändin logo sivuston otsikkoon.</span><span class="sxs-lookup"><span data-stu-id="67976-105">When you build your site, one of the first things that you will probably do is add your company or brand logo to the site's header.</span></span> <span data-ttu-id="67976-106">Dynamics 365 Commerce -online-moduulikirjasto tarjoaa moduulin, joka tekee tästä tehtävästä helppoa.</span><span class="sxs-lookup"><span data-stu-id="67976-106">The Dynamics 365 Commerce online module library provides a module that makes this task easy.</span></span>

<span data-ttu-id="67976-107">Voit lisätä logon suoraan malliin, asetteluun tai sivulle.</span><span class="sxs-lookup"><span data-stu-id="67976-107">You can add a logo directly to a template, layout, or page.</span></span> <span data-ttu-id="67976-108">Tällä tavoin voit helposti muuttaa tietyillä sivuilla tai sivuryhmillä näkyvää logoa.</span><span class="sxs-lookup"><span data-stu-id="67976-108">In this way, you can easily change the logo that appears on specific pages or groups of pages.</span></span> <span data-ttu-id="67976-109">Tämä ohjeaihe kattaa kuitenkin yleisimmät skenaariot, joissa lisäät logon otsikon osioihin, joita voidaan käyttää uudelleen kaikilla sivustosi sivuilla.</span><span class="sxs-lookup"><span data-stu-id="67976-109">However, this topic covers the most frequent scenario, where you add your logo to a header fragment that can be reused across all the pages of your site.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="67976-110">Edellytykset</span><span class="sxs-lookup"><span data-stu-id="67976-110">Prerequisites</span></span>

<span data-ttu-id="67976-111">Ennen kuin voit lisätä logon sivustosi kaikille sivuille, sinun on suoritettava nämä tehtävät.</span><span class="sxs-lookup"><span data-stu-id="67976-111">Before you can add a logo to all the pages of your site, you must complete these tasks.</span></span>

1. <span data-ttu-id="67976-112">Lataa logo mediakirjastoon.</span><span class="sxs-lookup"><span data-stu-id="67976-112">Upload your logo to the Media Library.</span></span>
1. <span data-ttu-id="67976-113">Luo otsikko-osa.</span><span class="sxs-lookup"><span data-stu-id="67976-113">Create a header fragment.</span></span> <span data-ttu-id="67976-114">Lisätietoja osien luomisesta ja käyttämisestä on kohdassa [osien käyttäminen](work-with-fragments.md).</span><span class="sxs-lookup"><span data-stu-id="67976-114">For more information about how to create and use fragments, see [Work with fragments](work-with-fragments.md).</span></span>
1. <span data-ttu-id="67976-115">Sisällytä otsikon osa malliin, jota sivustosi sivut käyttävät asettelu- ja moduulivaihtoehtoihin.</span><span class="sxs-lookup"><span data-stu-id="67976-115">Include the header fragment in the template that the pages of your site use for their layout and module options.</span></span> <span data-ttu-id="67976-116">Lisätietoja malleista on osiossa [Mallien avulla työskentely](work-with-templates.md).</span><span class="sxs-lookup"><span data-stu-id="67976-116">For more information about templates, see [Work with templates](work-with-templates.md).</span></span>

## <a name="add-a-logo-to-a-header-fragment"></a><span data-ttu-id="67976-117">Logon lisääminen otsikko-osaan</span><span class="sxs-lookup"><span data-stu-id="67976-117">Add a logo to a header fragment</span></span>

<span data-ttu-id="67976-118">Jos haluat lisätä logon sivustosi otsikko-osaan, toimi seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="67976-118">To add a logo to the header fragment for your site, follow these steps.</span></span>

1. <span data-ttu-id="67976-119">Valitse vasemmanpuoleisessa siirtymisruudussa **Osat**.</span><span class="sxs-lookup"><span data-stu-id="67976-119">In the navigation pane on the left, select **Fragments**.</span></span>
1. <span data-ttu-id="67976-120">Valitse aiemmin luomasi otsikon osa ja valitse sitten **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="67976-120">Select the header fragment that you created, and then select **Edit**.</span></span>
1. <span data-ttu-id="67976-121">Laajenna otsikkomoduuli.</span><span class="sxs-lookup"><span data-stu-id="67976-121">Expand the header module.</span></span>
1. <span data-ttu-id="67976-122">Anna logon kuva ja linkki otsikkomoduulin ominaisuusruudussa.</span><span class="sxs-lookup"><span data-stu-id="67976-122">In the property pane for the header module, provide an image and link for the logo.</span></span> 
1. <span data-ttu-id="67976-123">Tallenna otsikko-osa, lopeta sen muokkaus ja julkaise se.</span><span class="sxs-lookup"><span data-stu-id="67976-123">Save the header fragment, finish editing it, and publish it.</span></span>

<span data-ttu-id="67976-124">Kun olet julkaissut päivitetyn otsikon osan, kaikki ylätunnisteosan sisältävää mallia käyttävät sivuston sivut näyttävät logon.</span><span class="sxs-lookup"><span data-stu-id="67976-124">After you publish the updated header fragment, all site pages that use the template that contains the header fragment will show your logo.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="67976-125">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="67976-125">Additional resources</span></span>

[<span data-ttu-id="67976-126">Sivuston teeman valitseminen</span><span class="sxs-lookup"><span data-stu-id="67976-126">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="67976-127">CSS-ohitustiedostojen parissa työskentely</span><span class="sxs-lookup"><span data-stu-id="67976-127">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="67976-128">Favicon-kuvakkeen lisääminen</span><span class="sxs-lookup"><span data-stu-id="67976-128">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="67976-129">Tervetuloviestin lisääminen</span><span class="sxs-lookup"><span data-stu-id="67976-129">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="67976-130">Copyright-ilmoituksen lisääminen</span><span class="sxs-lookup"><span data-stu-id="67976-130">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="67976-131">Kielten lisääminen sivustoon</span><span class="sxs-lookup"><span data-stu-id="67976-131">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="67976-132">Komentosarjakoodin lisääminen sivuston sivuihin telemetrian tukemiseksi</span><span class="sxs-lookup"><span data-stu-id="67976-132">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
