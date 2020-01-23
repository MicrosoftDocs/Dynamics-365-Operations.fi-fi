---
title: Logon lisääminen
description: Tässä ohjeaiheessa kerrotaan, miten logo lisätään sivustollesi Microsoft Dynamics 365 Commerce -sovelluksessa.
author: bicyclingfool
manager: AnnBe
ms.date: 12/12/2019
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
ms.openlocfilehash: 23bac9aae6beb59912bbc9e1f2c6958c007550b0
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/20/2019
ms.locfileid: "2914616"
---
# <a name="add-a-logo"></a><span data-ttu-id="8e8ca-103">Logon lisääminen</span><span class="sxs-lookup"><span data-stu-id="8e8ca-103">Add a logo</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="8e8ca-104">Tässä ohjeaiheessa kerrotaan, miten logo lisätään sivustollesi Microsoft Dynamics 365 Commerce -sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="8e8ca-104">This topic describes how to add a logo to your site in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="8e8ca-105">Yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="8e8ca-105">Overview</span></span>

<span data-ttu-id="8e8ca-106">Kun rakennat sivustoasi, yksi ensimmäisistä asioista, jonka luultavasti teet, on lisätä yrityksesi tai brändin logo sivuston otsikkoon.</span><span class="sxs-lookup"><span data-stu-id="8e8ca-106">When you build your site, one of the first things that you will probably do is add your company or brand logo to the site's header.</span></span> <span data-ttu-id="8e8ca-107">Dynamics 365 Commerce -online-aloituspakkaus tarjoaa moduulin, joka tekee tästä tehtävästä helppoa.</span><span class="sxs-lookup"><span data-stu-id="8e8ca-107">The Dynamics 365 Commerce online starter kit provides a module that makes this task easy.</span></span>

<span data-ttu-id="8e8ca-108">Voit lisätä logon suoraan malliin, asetteluun tai sivulle.</span><span class="sxs-lookup"><span data-stu-id="8e8ca-108">You can add a logo directly to a template, layout, or page.</span></span> <span data-ttu-id="8e8ca-109">Tällä tavoin voit helposti muuttaa tietyillä sivuilla tai sivuryhmillä näkyvää logoa.</span><span class="sxs-lookup"><span data-stu-id="8e8ca-109">In this way, you can easily change the logo that appears on specific pages or groups of pages.</span></span> <span data-ttu-id="8e8ca-110">Tämä ohjeaihe kattaa kuitenkin yleisimmät skenaariot, joissa lisäät logon otsikon osioihin, joita voidaan käyttää uudelleen kaikilla sivustosi sivuilla.</span><span class="sxs-lookup"><span data-stu-id="8e8ca-110">However, this topic covers the most frequent scenario, where you add your logo to a header fragment that can be reused across all the pages of your site.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="8e8ca-111">Edellytykset</span><span class="sxs-lookup"><span data-stu-id="8e8ca-111">Prerequisites</span></span>

<span data-ttu-id="8e8ca-112">Ennen kuin voit lisätä logon sivustosi kaikille sivuille, sinun on suoritettava nämä tehtävät.</span><span class="sxs-lookup"><span data-stu-id="8e8ca-112">Before you can add a logo to all the pages of your site, you must complete these tasks.</span></span>

1. <span data-ttu-id="8e8ca-113">Lataa logosi digitaaliseen resurssinhallintaan, jota voit käyttää **Resurssit**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="8e8ca-113">Upload your logo to the digital assets manager, which you can access from the **Assets** page.</span></span>
1. <span data-ttu-id="8e8ca-114">Luo otsikko-osa.</span><span class="sxs-lookup"><span data-stu-id="8e8ca-114">Create a header fragment.</span></span> <span data-ttu-id="8e8ca-115">Lisätietoja osien luomisesta ja käyttämisestä on kohdassa [osien käyttäminen](work-with-fragments.md).</span><span class="sxs-lookup"><span data-stu-id="8e8ca-115">For more information about how to create and use fragments, see [Work with fragments](work-with-fragments.md).</span></span>
1. <span data-ttu-id="8e8ca-116">Sisällytä otsikon osa malliin, jota sivustosi sivut käyttävät asettelu- ja moduulivaihtoehtoihin.</span><span class="sxs-lookup"><span data-stu-id="8e8ca-116">Include the header fragment in the template that the pages of your site use for their layout and module options.</span></span> <span data-ttu-id="8e8ca-117">Lisätietoja malleista on osiossa [Mallien avulla työskentely](work-with-templates.md).</span><span class="sxs-lookup"><span data-stu-id="8e8ca-117">For more information about templates, see [Work with templates](work-with-templates.md).</span></span>

## <a name="add-a-logo-to-a-header-fragment"></a><span data-ttu-id="8e8ca-118">Logon lisääminen otsikko-osaan</span><span class="sxs-lookup"><span data-stu-id="8e8ca-118">Add a logo to a header fragment</span></span>

<span data-ttu-id="8e8ca-119">Jos haluat lisätä logon sivustosi otsikko-osaan, toimi seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="8e8ca-119">To add a logo to the header fragment for your site, follow these steps.</span></span>

1. <span data-ttu-id="8e8ca-120">Valitse vasemmalla olevasta siirtymisruudusta **osat** ja valitse sitten luomasi ylätunnisteen osa.</span><span class="sxs-lookup"><span data-stu-id="8e8ca-120">In the navigation pane on the left, select **Fragments**, and then select the header fragment that you created.</span></span>
2. <span data-ttu-id="8e8ca-121">Valitse **Kirjaa ulos**.</span><span class="sxs-lookup"><span data-stu-id="8e8ca-121">Select **Check out**.</span></span>
3. <span data-ttu-id="8e8ca-122">Laajenna **Otsikkopaikka** ja **Logopaikka**.</span><span class="sxs-lookup"><span data-stu-id="8e8ca-122">Expand the **Header** slot and the **Logo** slot.</span></span>
4. <span data-ttu-id="8e8ca-123">Valitse kolmen pisteen painike (**...**) **Logopaikalle** ja valitse sitten **Lisää moduuli**.</span><span class="sxs-lookup"><span data-stu-id="8e8ca-123">Select the ellipsis button (**...**) for the **Logo** slot, and then select **Add module**.</span></span>
5. <span data-ttu-id="8e8ca-124">Valitse logomoduuli.</span><span class="sxs-lookup"><span data-stu-id="8e8ca-124">Select the logo module.</span></span>
6. <span data-ttu-id="8e8ca-125">Määritä oikeanpuoleisessa ominaisuusruudussa logomoduuli, niin, että logosi näkyy siinä.</span><span class="sxs-lookup"><span data-stu-id="8e8ca-125">In the properties pane on the right, configure the logo module so that it shows your logo.</span></span>
7. <span data-ttu-id="8e8ca-126">Tallenna ylätunnisteosa, kirjaa se sisään ja julkaise se.</span><span class="sxs-lookup"><span data-stu-id="8e8ca-126">Save the header fragment, check it in, and publish it.</span></span>

<span data-ttu-id="8e8ca-127">Kun olet julkaissut päivitetyn otsikon osan, kaikki ylätunnisteosan sisältävää mallia käyttävät sivuston sivut näyttävät logon.</span><span class="sxs-lookup"><span data-stu-id="8e8ca-127">After you publish the updated header fragment, all site pages that use the template that contains the header fragment will show your logo.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8e8ca-128">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="8e8ca-128">Additional resources</span></span>

[<span data-ttu-id="8e8ca-129">Sivuston teeman valitseminen</span><span class="sxs-lookup"><span data-stu-id="8e8ca-129">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="8e8ca-130">CSS-ohitustiedostojen parissa työskentely</span><span class="sxs-lookup"><span data-stu-id="8e8ca-130">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="8e8ca-131">Favicon-kuvakkeen lisääminen</span><span class="sxs-lookup"><span data-stu-id="8e8ca-131">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="8e8ca-132">Tervetuloviestin lisääminen</span><span class="sxs-lookup"><span data-stu-id="8e8ca-132">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="8e8ca-133">Copyright-ilmoituksen lisääminen</span><span class="sxs-lookup"><span data-stu-id="8e8ca-133">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="8e8ca-134">Kielten lisääminen sivustoon</span><span class="sxs-lookup"><span data-stu-id="8e8ca-134">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="8e8ca-135">Komentosarjakoodin lisääminen sivuston sivuihin telemetrian tukemiseksi</span><span class="sxs-lookup"><span data-stu-id="8e8ca-135">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

