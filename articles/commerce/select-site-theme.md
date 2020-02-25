---
title: Sivuston teeman valitseminen
description: Tässä ohjeaiheessa kuvataan, miten sivuston teema määritetään tai miten sitä muutetaan Microsoft Dynamics 365 Commerce -sovelluksessa.
author: bicyclingfool
manager: annbe
ms.date: 12/12/2019
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
ms.openlocfilehash: 45184c7b0e29d1258b26368fbc7221df91013cc3
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002748"
---
# <a name="select-a-site-theme"></a><span data-ttu-id="6f3b2-103">Sivuston teeman valitseminen</span><span class="sxs-lookup"><span data-stu-id="6f3b2-103">Select a site theme</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="6f3b2-104">Tässä ohjeaiheessa kuvataan, miten sivuston teema määritetään tai miten sitä muutetaan Microsoft Dynamics 365 Commerce -sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="6f3b2-104">This topic describes how to set or change your site's theme in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="6f3b2-105">Yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="6f3b2-105">Overview</span></span>

<span data-ttu-id="6f3b2-106">Sivuston asettelu ja tyyli (esimerkiksi fontit, koot ja värit) määritetään valitsemasi teeman mukaan ja otetaan käyttöön sivustossa.</span><span class="sxs-lookup"><span data-stu-id="6f3b2-106">A site's layout and style (for example, fonts, sizes, and colors) are defined by the theme that you select and apply to the site.</span></span> <span data-ttu-id="6f3b2-107">Yrityksen kehittäjä luo ja ottaa käyttöön teeman.</span><span class="sxs-lookup"><span data-stu-id="6f3b2-107">A theme is created and deployed by a developer at your company.</span></span> <span data-ttu-id="6f3b2-108">Yleiskatsaus teemoista on kohdassa [Teemojen yleiskatsaus](http://).</span><span class="sxs-lookup"><span data-stu-id="6f3b2-108">For an overview of themes, see [Theming overview](http://).</span></span> <span data-ttu-id="6f3b2-109">Lisätietoja teemojen luomisesta ja käyttöönotosta on kohdassa [Uuden teeman luominen](http://).</span><span class="sxs-lookup"><span data-stu-id="6f3b2-109">For more information about how to create and deploy themes, see [Create a new theme](http://).</span></span>

<span data-ttu-id="6f3b2-110">Kun luot sivuston ensimmäisen kerran, se käyttää teemaa, jonka nimi on **Fabrikam**.</span><span class="sxs-lookup"><span data-stu-id="6f3b2-110">By default, when you first create a site, it uses a theme that is named **Fabrikam**.</span></span> <span data-ttu-id="6f3b2-111">Tämä oletusteema on osa aloituspakkausta.</span><span class="sxs-lookup"><span data-stu-id="6f3b2-111">This default theme is provided as part of the starter kit.</span></span> <span data-ttu-id="6f3b2-112">Kun olet ottanut käyttöön muita teemoja sivustossa, voit määrittää sivuston siten, että se käyttää yhtä niistä.</span><span class="sxs-lookup"><span data-stu-id="6f3b2-112">After you've deployed additional themes for your site, you can configure the site so that it uses one of them instead.</span></span>

## <a name="select-the-site-theme"></a><span data-ttu-id="6f3b2-113">Sivuston teeman valitseminen</span><span class="sxs-lookup"><span data-stu-id="6f3b2-113">Select the site theme</span></span>

<span data-ttu-id="6f3b2-114">Voit valita sivustossa käytettävän teeman noudattamalla seuraavia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="6f3b2-114">To select the theme that is applied to your site, follow these steps.</span></span>

1. <span data-ttu-id="6f3b2-115">Siirry sivuston muokkausympäristössä sivustoon.</span><span class="sxs-lookup"><span data-stu-id="6f3b2-115">In the site authoring environment, go to your site.</span></span>
1. <span data-ttu-id="6f3b2-116">Siirry kohtaan **Sivuston hallinta** \> **Laajennettavuus**.</span><span class="sxs-lookup"><span data-stu-id="6f3b2-116">Go to **Site Management** \> **Extensibility**.</span></span>
1. <span data-ttu-id="6f3b2-117">Valitse **Teema**-kohdassa teema avattavasta valikosta.</span><span class="sxs-lookup"><span data-stu-id="6f3b2-117">Under **Theme**, select a theme on the drop-down menu.</span></span>
1. <span data-ttu-id="6f3b2-118">Jos haluat käyttää valittua teemaa sivustossa, valitse **Tallenna ja julkaise**.</span><span class="sxs-lookup"><span data-stu-id="6f3b2-118">To apply the selected theme to your site, select **Save and publish**.</span></span>

> [!NOTE]
> <span data-ttu-id="6f3b2-119">Valitsemasi teema julkaistaan sivustoon heti, kun valitset **Tallenna ja julkaise** -kohdan **Laajennettavuus**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="6f3b2-119">The theme that you select is published to your site as soon as you select **Save and publish** on the **Extensibility** page.</span></span> <span data-ttu-id="6f3b2-120">Voit esikatsella teemaa sivustossa ennen sen käyttöönottoa käyttämällä kehitys- tai eristysympäristöä.</span><span class="sxs-lookup"><span data-stu-id="6f3b2-120">To preview a theme on your site before you apply it, you can use your development or sandbox environment.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6f3b2-121">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="6f3b2-121">Additional resources</span></span>

[<span data-ttu-id="6f3b2-122">Logon lisääminen</span><span class="sxs-lookup"><span data-stu-id="6f3b2-122">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="6f3b2-123">CSS-ohitustiedostojen parissa työskentely</span><span class="sxs-lookup"><span data-stu-id="6f3b2-123">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="6f3b2-124">Favicon-kuvakkeen lisääminen</span><span class="sxs-lookup"><span data-stu-id="6f3b2-124">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="6f3b2-125">Tervetuloviestin lisääminen</span><span class="sxs-lookup"><span data-stu-id="6f3b2-125">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="6f3b2-126">Copyright-ilmoituksen lisääminen</span><span class="sxs-lookup"><span data-stu-id="6f3b2-126">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="6f3b2-127">Kielten lisääminen sivustoon</span><span class="sxs-lookup"><span data-stu-id="6f3b2-127">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="6f3b2-128">Komentosarjakoodin lisääminen sivuston sivuihin telemetrian tukemiseksi</span><span class="sxs-lookup"><span data-stu-id="6f3b2-128">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)
