---
title: Sivuston teeman valitseminen
description: Tässä ohjeaiheessa kuvataan, miten sivuston teema määritetään tai miten sitä muutetaan Microsoft Dynamics 365 Commerce -sovelluksessa.
author: bicyclingfool
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 66fcff9fa18d3c98e022ef91d15903fbba8b6b61
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4982397"
---
# <a name="select-a-site-theme"></a><span data-ttu-id="f37da-103">Sivuston teeman valitseminen</span><span class="sxs-lookup"><span data-stu-id="f37da-103">Select a site theme</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="f37da-104">Tässä ohjeaiheessa kuvataan, miten sivuston teema määritetään tai miten sitä muutetaan Microsoft Dynamics 365 Commerce -sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="f37da-104">This topic describes how to set or change your site's theme in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="f37da-105">Yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="f37da-105">Overview</span></span>

<span data-ttu-id="f37da-106">Sivuston asettelu ja tyyli (esimerkiksi fontit, koot ja värit) määritetään valitsemasi teeman mukaan ja otetaan käyttöön sivustossa.</span><span class="sxs-lookup"><span data-stu-id="f37da-106">A site's layout and style (for example, fonts, sizes, and colors) are defined by the theme that you select and apply to the site.</span></span> <span data-ttu-id="f37da-107">Yrityksen kehittäjä luo ja ottaa käyttöön teeman.</span><span class="sxs-lookup"><span data-stu-id="f37da-107">A theme is created and deployed by a developer at your company.</span></span> <span data-ttu-id="f37da-108">Yleiskatsaus teemoista on kohdassa [Teemojen yleiskatsaus](e-commerce-extensibility/theming.md).</span><span class="sxs-lookup"><span data-stu-id="f37da-108">For an overview of themes, see [Theming overview](e-commerce-extensibility/theming.md).</span></span> <span data-ttu-id="f37da-109">Lisätietoja teemojen luomisesta ja käyttöönotosta on kohdassa [Uuden teeman luominen](e-commerce-extensibility/create-theme.md).</span><span class="sxs-lookup"><span data-stu-id="f37da-109">For more information about how to create and deploy themes, see [Create a new theme](e-commerce-extensibility/create-theme.md).</span></span>

<span data-ttu-id="f37da-110">Kun luot sivuston ensimmäisen kerran, se käyttää teemaa, jonka nimi on **Fabrikam**.</span><span class="sxs-lookup"><span data-stu-id="f37da-110">By default, when you first create a site, it uses a theme that is named **Fabrikam**.</span></span> <span data-ttu-id="f37da-111">Tämä oletusteema on osa Commercen moduulikirjastoa.</span><span class="sxs-lookup"><span data-stu-id="f37da-111">This default theme is provided as part of the Commerce module library.</span></span> <span data-ttu-id="f37da-112">Kun olet ottanut käyttöön muita teemoja sivustossa, voit määrittää sivuston siten, että se käyttää yhtä niistä.</span><span class="sxs-lookup"><span data-stu-id="f37da-112">After you've deployed additional themes for your site, you can configure the site so that it uses one of them instead.</span></span>

## <a name="select-the-site-theme"></a><span data-ttu-id="f37da-113">Sivuston teeman valitseminen</span><span class="sxs-lookup"><span data-stu-id="f37da-113">Select the site theme</span></span>

<span data-ttu-id="f37da-114">Voit valita sivustossa käytettävän teeman noudattamalla seuraavia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="f37da-114">To select the theme that is applied to your site, follow these steps.</span></span>

1. <span data-ttu-id="f37da-115">Siirry sivuston muokkausympäristössä sivustoon.</span><span class="sxs-lookup"><span data-stu-id="f37da-115">In the site authoring environment, go to your site.</span></span>
1. <span data-ttu-id="f37da-116">Siirry kohtaan **Sivuston hallinta** \> **Laajennettavuus**.</span><span class="sxs-lookup"><span data-stu-id="f37da-116">Go to **Site Management** \> **Extensibility**.</span></span>
1. <span data-ttu-id="f37da-117">Valitse **Teema**-kohdassa teema avattavasta valikosta.</span><span class="sxs-lookup"><span data-stu-id="f37da-117">Under **Theme**, select a theme on the drop-down menu.</span></span>
1. <span data-ttu-id="f37da-118">Jos haluat käyttää valittua teemaa sivustossa, valitse **Tallenna ja julkaise**.</span><span class="sxs-lookup"><span data-stu-id="f37da-118">To apply the selected theme to your site, select **Save and publish**.</span></span>

> [!NOTE]
> <span data-ttu-id="f37da-119">Valitsemasi teema julkaistaan sivustoon heti, kun valitset **Tallenna ja julkaise** -kohdan **Laajennettavuus**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="f37da-119">The theme that you select is published to your site as soon as you select **Save and publish** on the **Extensibility** page.</span></span> <span data-ttu-id="f37da-120">Voit esikatsella teemaa sivustossa ennen sen käyttöönottoa käyttämällä kehitys- tai eristysympäristöä.</span><span class="sxs-lookup"><span data-stu-id="f37da-120">To preview a theme on your site before you apply it, you can use your development or sandbox environment.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f37da-121">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="f37da-121">Additional resources</span></span>

[<span data-ttu-id="f37da-122">Logon lisääminen</span><span class="sxs-lookup"><span data-stu-id="f37da-122">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="f37da-123">CSS-ohitustiedostojen parissa työskentely</span><span class="sxs-lookup"><span data-stu-id="f37da-123">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="f37da-124">Favicon-kuvakkeen lisääminen</span><span class="sxs-lookup"><span data-stu-id="f37da-124">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="f37da-125">Tervetuloviestin lisääminen</span><span class="sxs-lookup"><span data-stu-id="f37da-125">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="f37da-126">Copyright-ilmoituksen lisääminen</span><span class="sxs-lookup"><span data-stu-id="f37da-126">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="f37da-127">Kielten lisääminen sivustoon</span><span class="sxs-lookup"><span data-stu-id="f37da-127">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="f37da-128">Komentosarjakoodin lisääminen sivuston sivuihin telemetrian tukemiseksi</span><span class="sxs-lookup"><span data-stu-id="f37da-128">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

[<span data-ttu-id="f37da-129">Teemojen yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="f37da-129">Theming overview</span></span>](e-commerce-extensibility/theming.md)

[<span data-ttu-id="f37da-130">Uuden teeman luominen</span><span class="sxs-lookup"><span data-stu-id="f37da-130">Create a new theme</span></span>](e-commerce-extensibility/create-theme.md)

