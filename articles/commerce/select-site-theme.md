---
title: Sivuston teeman valitseminen
description: Tässä ohjeaiheessa kuvataan, miten sivuston teema määritetään tai miten sitä muutetaan Microsoft Dynamics 365 Commerce -sovelluksessa.
author: bicyclingfool
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 1e11e2ffafa29dfe4ad7a4a8e4d14e9d7c74c31f
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5794064"
---
# <a name="select-a-site-theme"></a><span data-ttu-id="e5662-103">Sivuston teeman valitseminen</span><span class="sxs-lookup"><span data-stu-id="e5662-103">Select a site theme</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e5662-104">Tässä ohjeaiheessa kuvataan, miten sivuston teema määritetään tai miten sitä muutetaan Microsoft Dynamics 365 Commerce -sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="e5662-104">This topic describes how to set or change your site's theme in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="e5662-105">Sivuston asettelu ja tyyli (esimerkiksi fontit, koot ja värit) määritetään valitsemasi teeman mukaan ja otetaan käyttöön sivustossa.</span><span class="sxs-lookup"><span data-stu-id="e5662-105">A site's layout and style (for example, fonts, sizes, and colors) are defined by the theme that you select and apply to the site.</span></span> <span data-ttu-id="e5662-106">Yrityksen kehittäjä luo ja ottaa käyttöön teeman.</span><span class="sxs-lookup"><span data-stu-id="e5662-106">A theme is created and deployed by a developer at your company.</span></span> <span data-ttu-id="e5662-107">Yleiskatsaus teemoista on kohdassa [Teemojen yleiskatsaus](e-commerce-extensibility/theming.md).</span><span class="sxs-lookup"><span data-stu-id="e5662-107">For an overview of themes, see [Theming overview](e-commerce-extensibility/theming.md).</span></span> <span data-ttu-id="e5662-108">Lisätietoja teemojen luomisesta ja käyttöönotosta on kohdassa [Uuden teeman luominen](e-commerce-extensibility/create-theme.md).</span><span class="sxs-lookup"><span data-stu-id="e5662-108">For more information about how to create and deploy themes, see [Create a new theme](e-commerce-extensibility/create-theme.md).</span></span>

<span data-ttu-id="e5662-109">Kun luot sivuston ensimmäisen kerran, se käyttää teemaa, jonka nimi on **Fabrikam**.</span><span class="sxs-lookup"><span data-stu-id="e5662-109">By default, when you first create a site, it uses a theme that is named **Fabrikam**.</span></span> <span data-ttu-id="e5662-110">Tämä oletusteema on osa Commercen moduulikirjastoa.</span><span class="sxs-lookup"><span data-stu-id="e5662-110">This default theme is provided as part of the Commerce module library.</span></span> <span data-ttu-id="e5662-111">Kun olet ottanut käyttöön muita teemoja sivustossa, voit määrittää sivuston siten, että se käyttää yhtä niistä.</span><span class="sxs-lookup"><span data-stu-id="e5662-111">After you've deployed additional themes for your site, you can configure the site so that it uses one of them instead.</span></span>

## <a name="select-the-site-theme"></a><span data-ttu-id="e5662-112">Sivuston teeman valitseminen</span><span class="sxs-lookup"><span data-stu-id="e5662-112">Select the site theme</span></span>

<span data-ttu-id="e5662-113">Voit valita sivustossa käytettävän teeman noudattamalla seuraavia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="e5662-113">To select the theme that is applied to your site, follow these steps.</span></span>

1. <span data-ttu-id="e5662-114">Siirry sivuston muokkausympäristössä sivustoon.</span><span class="sxs-lookup"><span data-stu-id="e5662-114">In the site authoring environment, go to your site.</span></span>
1. <span data-ttu-id="e5662-115">Siirry kohtaan **Sivuston hallinta** \> **Laajennettavuus**.</span><span class="sxs-lookup"><span data-stu-id="e5662-115">Go to **Site Management** \> **Extensibility**.</span></span>
1. <span data-ttu-id="e5662-116">Valitse **Teema**-kohdassa teema avattavasta valikosta.</span><span class="sxs-lookup"><span data-stu-id="e5662-116">Under **Theme**, select a theme on the drop-down menu.</span></span>
1. <span data-ttu-id="e5662-117">Jos haluat käyttää valittua teemaa sivustossa, valitse **Tallenna ja julkaise**.</span><span class="sxs-lookup"><span data-stu-id="e5662-117">To apply the selected theme to your site, select **Save and publish**.</span></span>

> [!NOTE]
> <span data-ttu-id="e5662-118">Valitsemasi teema julkaistaan sivustoon heti, kun valitset **Tallenna ja julkaise** -kohdan **Laajennettavuus**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="e5662-118">The theme that you select is published to your site as soon as you select **Save and publish** on the **Extensibility** page.</span></span> <span data-ttu-id="e5662-119">Voit esikatsella teemaa sivustossa ennen sen käyttöönottoa käyttämällä kehitys- tai eristysympäristöä.</span><span class="sxs-lookup"><span data-stu-id="e5662-119">To preview a theme on your site before you apply it, you can use your development or sandbox environment.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e5662-120">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="e5662-120">Additional resources</span></span>

[<span data-ttu-id="e5662-121">Logon lisääminen</span><span class="sxs-lookup"><span data-stu-id="e5662-121">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="e5662-122">CSS-ohitustiedostojen parissa työskentely</span><span class="sxs-lookup"><span data-stu-id="e5662-122">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="e5662-123">Favicon-kuvakkeen lisääminen</span><span class="sxs-lookup"><span data-stu-id="e5662-123">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="e5662-124">Tervetuloviestin lisääminen</span><span class="sxs-lookup"><span data-stu-id="e5662-124">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="e5662-125">Copyright-ilmoituksen lisääminen</span><span class="sxs-lookup"><span data-stu-id="e5662-125">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="e5662-126">Kielten lisääminen sivustoon</span><span class="sxs-lookup"><span data-stu-id="e5662-126">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="e5662-127">Komentosarjakoodin lisääminen sivuston sivuihin telemetrian tukemiseksi</span><span class="sxs-lookup"><span data-stu-id="e5662-127">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

[<span data-ttu-id="e5662-128">Teemojen yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="e5662-128">Theming overview</span></span>](e-commerce-extensibility/theming.md)

[<span data-ttu-id="e5662-129">Uuden teeman luominen</span><span class="sxs-lookup"><span data-stu-id="e5662-129">Create a new theme</span></span>](e-commerce-extensibility/create-theme.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
