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
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 1f92b31e870cbb4d3cc04870273693bed1378c5e
ms.sourcegitcommit: 8028fbc5b9585e87d3331ea02577ff82ede090af
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/16/2020
ms.locfileid: "3817703"
---
# <a name="select-a-site-theme"></a><span data-ttu-id="f3dc4-103">Sivuston teeman valitseminen</span><span class="sxs-lookup"><span data-stu-id="f3dc4-103">Select a site theme</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="f3dc4-104">Tässä ohjeaiheessa kuvataan, miten sivuston teema määritetään tai miten sitä muutetaan Microsoft Dynamics 365 Commerce -sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="f3dc4-104">This topic describes how to set or change your site's theme in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="f3dc4-105">Yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="f3dc4-105">Overview</span></span>

<span data-ttu-id="f3dc4-106">Sivuston asettelu ja tyyli (esimerkiksi fontit, koot ja värit) määritetään valitsemasi teeman mukaan ja otetaan käyttöön sivustossa.</span><span class="sxs-lookup"><span data-stu-id="f3dc4-106">A site's layout and style (for example, fonts, sizes, and colors) are defined by the theme that you select and apply to the site.</span></span> <span data-ttu-id="f3dc4-107">Yrityksen kehittäjä luo ja ottaa käyttöön teeman.</span><span class="sxs-lookup"><span data-stu-id="f3dc4-107">A theme is created and deployed by a developer at your company.</span></span> <span data-ttu-id="f3dc4-108">Yleiskatsaus teemoista on kohdassa [Teemojen yleiskatsaus](http://).</span><span class="sxs-lookup"><span data-stu-id="f3dc4-108">For an overview of themes, see [Theming overview](http://).</span></span> <span data-ttu-id="f3dc4-109">Lisätietoja teemojen luomisesta ja käyttöönotosta on kohdassa [Uuden teeman luominen](http://).</span><span class="sxs-lookup"><span data-stu-id="f3dc4-109">For more information about how to create and deploy themes, see [Create a new theme](http://).</span></span>

<span data-ttu-id="f3dc4-110">Kun luot sivuston ensimmäisen kerran, se käyttää teemaa, jonka nimi on **Fabrikam**.</span><span class="sxs-lookup"><span data-stu-id="f3dc4-110">By default, when you first create a site, it uses a theme that is named **Fabrikam**.</span></span> <span data-ttu-id="f3dc4-111">Tämä oletusteema on osa Commercen moduulikirjastoa.</span><span class="sxs-lookup"><span data-stu-id="f3dc4-111">This default theme is provided as part of the Commerce module library.</span></span> <span data-ttu-id="f3dc4-112">Kun olet ottanut käyttöön muita teemoja sivustossa, voit määrittää sivuston siten, että se käyttää yhtä niistä.</span><span class="sxs-lookup"><span data-stu-id="f3dc4-112">After you've deployed additional themes for your site, you can configure the site so that it uses one of them instead.</span></span>

## <a name="select-the-site-theme"></a><span data-ttu-id="f3dc4-113">Sivuston teeman valitseminen</span><span class="sxs-lookup"><span data-stu-id="f3dc4-113">Select the site theme</span></span>

<span data-ttu-id="f3dc4-114">Voit valita sivustossa käytettävän teeman noudattamalla seuraavia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="f3dc4-114">To select the theme that is applied to your site, follow these steps.</span></span>

1. <span data-ttu-id="f3dc4-115">Siirry sivuston muokkausympäristössä sivustoon.</span><span class="sxs-lookup"><span data-stu-id="f3dc4-115">In the site authoring environment, go to your site.</span></span>
1. <span data-ttu-id="f3dc4-116">Siirry kohtaan **Sivuston hallinta** \> **Laajennettavuus**.</span><span class="sxs-lookup"><span data-stu-id="f3dc4-116">Go to **Site Management** \> **Extensibility**.</span></span>
1. <span data-ttu-id="f3dc4-117">Valitse **Teema**-kohdassa teema avattavasta valikosta.</span><span class="sxs-lookup"><span data-stu-id="f3dc4-117">Under **Theme**, select a theme on the drop-down menu.</span></span>
1. <span data-ttu-id="f3dc4-118">Jos haluat käyttää valittua teemaa sivustossa, valitse **Tallenna ja julkaise**.</span><span class="sxs-lookup"><span data-stu-id="f3dc4-118">To apply the selected theme to your site, select **Save and publish**.</span></span>

> [!NOTE]
> <span data-ttu-id="f3dc4-119">Valitsemasi teema julkaistaan sivustoon heti, kun valitset **Tallenna ja julkaise** -kohdan **Laajennettavuus**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="f3dc4-119">The theme that you select is published to your site as soon as you select **Save and publish** on the **Extensibility** page.</span></span> <span data-ttu-id="f3dc4-120">Voit esikatsella teemaa sivustossa ennen sen käyttöönottoa käyttämällä kehitys- tai eristysympäristöä.</span><span class="sxs-lookup"><span data-stu-id="f3dc4-120">To preview a theme on your site before you apply it, you can use your development or sandbox environment.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f3dc4-121">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="f3dc4-121">Additional resources</span></span>

[<span data-ttu-id="f3dc4-122">Logon lisääminen</span><span class="sxs-lookup"><span data-stu-id="f3dc4-122">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="f3dc4-123">CSS-ohitustiedostojen parissa työskentely</span><span class="sxs-lookup"><span data-stu-id="f3dc4-123">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="f3dc4-124">Favicon-kuvakkeen lisääminen</span><span class="sxs-lookup"><span data-stu-id="f3dc4-124">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="f3dc4-125">Tervetuloviestin lisääminen</span><span class="sxs-lookup"><span data-stu-id="f3dc4-125">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="f3dc4-126">Copyright-ilmoituksen lisääminen</span><span class="sxs-lookup"><span data-stu-id="f3dc4-126">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="f3dc4-127">Kielten lisääminen sivustoon</span><span class="sxs-lookup"><span data-stu-id="f3dc4-127">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="f3dc4-128">Komentosarjakoodin lisääminen sivuston sivuihin telemetrian tukemiseksi</span><span class="sxs-lookup"><span data-stu-id="f3dc4-128">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)
