---
title: Komentosarjakoodin lisääminen sivuston sivuihin telemetrian tukemiseksi
description: Tässä ohjeaiheessa kerrotaan, miten asiakaspuolen komentosarjakoodi lisätään sivustosivuille tukemaan asiakaspuolen telemetriatietojen keräämistä.
author: bicyclingfool
manager: annbe
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 674d00faf1b30f87a0b0062129e1b9fbff955dd4
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/01/2020
ms.locfileid: "3001274"
---
# <a name="add-script-code-to-site-pages-to-support-telemetry"></a><span data-ttu-id="da77b-103">Komentosarjakoodin lisääminen sivuston sivuihin telemetrian tukemiseksi</span><span class="sxs-lookup"><span data-stu-id="da77b-103">Add script code to site pages to support telemetry</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="da77b-104">Tässä ohjeaiheessa kerrotaan, miten asiakaspuolen komentosarjakoodi lisätään sivustosivuille tukemaan asiakaspuolen telemetriatietojen keräämistä.</span><span class="sxs-lookup"><span data-stu-id="da77b-104">This topic describes how to add client-side script code to your site pages to support the collection of client-side telemetry.</span></span>

## <a name="overview"></a><span data-ttu-id="da77b-105">Yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="da77b-105">Overview</span></span>

<span data-ttu-id="da77b-106">Web Analytics on tärkeä työkalu, kun halutaan ymmärtää, miten asiakkaat käyttävät sivustoa ja miten he tekevät päätöksiä. Tämä mahdollistaa muuntokokemuksen optimoinnin ja muunnon maksimoinnin.</span><span class="sxs-lookup"><span data-stu-id="da77b-106">Web analytics are an essential tool when you want to understand how your customers interact with your site and make decisions that will help optimize the experience for maximum conversion.</span></span> <span data-ttu-id="da77b-107">Käytettävissä on useita Web Analytics -paketteja, joiden avulla tavoitteet voidaan saavuttaa. Paketteja ovat esimerkiksi Google Analytics, Clicky, Moz Analytics ja KISSMetrics.</span><span class="sxs-lookup"><span data-stu-id="da77b-107">Many web analytics packages are available to help you achieve these goals, such as Google Analytics, Clicky, Moz Analytics, and KISSMetrics.</span></span> <span data-ttu-id="da77b-108">Useimmat Web Analytics -paketit edellyttävät, että lisäät asiakaspuolen komentosarjakoodin HTML:n **\<head\>**-elementtiin kaikille sivuston sivuille.</span><span class="sxs-lookup"><span data-stu-id="da77b-108">Most web analytics packages require that you add client-side script code in the **\<head\>** element of the HTML for all pages of your site.</span></span>

> [!NOTE]
> <span data-ttu-id="da77b-109">Tämän ohjeaiheen ohjeet koskevat myös muita mukautettuja asiakaspuolen toimintoja, joita Microsoft Dynamics 365 Commerce ei tarjoa suoraan.</span><span class="sxs-lookup"><span data-stu-id="da77b-109">The instructions in this topic also apply to other custom client-side functionality that Microsoft Dynamics 365 Commerce doesn't natively offer.</span></span>

## <a name="create-a-reusable-fragment-for-your-script-code"></a><span data-ttu-id="da77b-110">Uudelleenkäytettävän osan luominen komentosarjakoodia varten</span><span class="sxs-lookup"><span data-stu-id="da77b-110">Create a reusable fragment for your script code</span></span>

<span data-ttu-id="da77b-111">Kun olet luonut osan komentosarjakoodille, sitä voidaan käyttää uudelleen kaikilla sivuston sivuilla.</span><span class="sxs-lookup"><span data-stu-id="da77b-111">After you create a fragment for your script code, it can be reused across all pages on your site.</span></span>

1. <span data-ttu-id="da77b-112">Siirry kohtaan **Osat \> Uusi sivun osa**.</span><span class="sxs-lookup"><span data-stu-id="da77b-112">Go to **Fragments \> New page fragment**.</span></span>
2. <span data-ttu-id="da77b-113">Valitse **Ulkoinen komentosarja**, kirjoita osan nimi ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="da77b-113">Select **External Script**, enter a name for the fragment, and then select **OK**.</span></span>
3. <span data-ttu-id="da77b-114">Valitse osahierarkiassa **komentosarjan lisäystoiminto** -moduulin osan alitaso, jonka loit juuri.</span><span class="sxs-lookup"><span data-stu-id="da77b-114">In the fragment hierarchy, select the **script injector** module child of the fragment that you just created.</span></span>
4. <span data-ttu-id="da77b-115">Lisää asiakaspuolen komentosarja oikealla olevaan ominaisuusruutuun ja määritä muut tarvittavat määritysvaihtoehdot.</span><span class="sxs-lookup"><span data-stu-id="da77b-115">In the property pane on the right, add your client-side script, and set other configuration options as you require.</span></span>

## <a name="add-the-fragment-to-templates"></a><span data-ttu-id="da77b-116">Osan lisääminen malleihin</span><span class="sxs-lookup"><span data-stu-id="da77b-116">Add the fragment to templates</span></span>

1. <span data-ttu-id="da77b-117">Siirry **Mallit**-kohtaan ja avaa niiden sivujen malli, joihin haluat lisätä komentosarjakoodin.</span><span class="sxs-lookup"><span data-stu-id="da77b-117">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
2. <span data-ttu-id="da77b-118">Laajenna vasemmanpuoleisessa ruudussa mallihierarkia, jolloin **HTML Head** -paikka.</span><span class="sxs-lookup"><span data-stu-id="da77b-118">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
3. <span data-ttu-id="da77b-119">Valitse kolmen pisteen painike (**...**) **HTML Head** -paikkaa varten ja valitse sitten **Lisää osa**.</span><span class="sxs-lookup"><span data-stu-id="da77b-119">Select the ellipsis button (**...**) for the **HTML Head** slot, and then select **Add fragment**.</span></span>
4. <span data-ttu-id="da77b-120">Valitse komentosarjakoodille luomasi osa.</span><span class="sxs-lookup"><span data-stu-id="da77b-120">Select the fragment that you created for your script code.</span></span>
5. <span data-ttu-id="da77b-121">Tallenna malli ja julkaise se.</span><span class="sxs-lookup"><span data-stu-id="da77b-121">Save the template, and check it in.</span></span>

> [!NOTE]
> <span data-ttu-id="da77b-122">Kun olet valmis, sinun on julkaistava osa ja päämalli.</span><span class="sxs-lookup"><span data-stu-id="da77b-122">After you've finished, you must publish the fragment and the master template.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="da77b-123">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="da77b-123">Additional resources</span></span>

[<span data-ttu-id="da77b-124">Logon lisääminen</span><span class="sxs-lookup"><span data-stu-id="da77b-124">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="da77b-125">Sivuston teeman valitseminen</span><span class="sxs-lookup"><span data-stu-id="da77b-125">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="da77b-126">CSS-ohitustiedostojen parissa työskentely</span><span class="sxs-lookup"><span data-stu-id="da77b-126">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="da77b-127">Favicon-kuvakkeen lisääminen</span><span class="sxs-lookup"><span data-stu-id="da77b-127">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="da77b-128">Tervetuloviestin lisääminen</span><span class="sxs-lookup"><span data-stu-id="da77b-128">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="da77b-129">Copyright-ilmoituksen lisääminen</span><span class="sxs-lookup"><span data-stu-id="da77b-129">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="da77b-130">Kielten lisääminen sivustoon</span><span class="sxs-lookup"><span data-stu-id="da77b-130">Add languages to your site</span></span>](add-languages-to-site.md)

