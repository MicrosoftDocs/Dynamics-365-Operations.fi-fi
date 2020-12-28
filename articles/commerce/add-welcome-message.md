---
title: Tervetuloviestin lisääminen
description: Tässä ohjeaiheessa kuvataan, miten tervetulosanoma lisätään Microsoft Dynamics 365 Commerce -sivustoon.
author: psimolin
manager: annbe
ms.date: 04/13/2020
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
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: d2a125b4e71016ad620f128af2e3c9f29aa04f4c
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4411923"
---
# <a name="add-a-welcome-message"></a><span data-ttu-id="beae4-103">Tervetuloviestin lisääminen</span><span class="sxs-lookup"><span data-stu-id="beae4-103">Add a welcome message</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="beae4-104">Tässä ohjeaiheessa kuvataan, miten tervetulosanoma lisätään Microsoft Dynamics 365 Commerce -sivustoon.</span><span class="sxs-lookup"><span data-stu-id="beae4-104">This topic describes how to add a welcome message to your Microsoft Dynamics 365 Commerce website.</span></span>

## <a name="overview"></a><span data-ttu-id="beae4-105">Yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="beae4-105">Overview</span></span>

<span data-ttu-id="beae4-106">Sähköisen kaupankäynnin sivuston tervetulosanoma voi kertoa kävijöille meneillään olevista alennusmyynneistä, sivuston päivityksistä ja kausittaisista kokoelmista.</span><span class="sxs-lookup"><span data-stu-id="beae4-106">A welcome message on your e-Commerce website can inform visitors about ongoing sales, site updates, or availability of seasonal collections.</span></span> <span data-ttu-id="beae4-107">Tervetulosanoma määritetään hälytysmoduulin avulla.</span><span class="sxs-lookup"><span data-stu-id="beae4-107">The welcome message is set by using the alert module.</span></span>

<span data-ttu-id="beae4-108">Hälytysmoduuli on lisättävä ylätunnisteosan **Virhe/tietosanomat**-paikkaan.</span><span class="sxs-lookup"><span data-stu-id="beae4-108">The alert module should be added to the **Error/Information messages** slot of the header fragment.</span></span> <span data-ttu-id="beae4-109">Hälytysmoduulin avulla voit määrittää näkyvän tekstin, tekstin värin ja tasauksen.</span><span class="sxs-lookup"><span data-stu-id="beae4-109">The alert module lets you specify the text that is shown, the text color, and the alignment.</span></span> <span data-ttu-id="beae4-110">Sen avulla voit myös määrittää, voivatko sivuston vierailijat hylätä viestin.</span><span class="sxs-lookup"><span data-stu-id="beae4-110">It also lets you specify whether visitors to the site can dismiss the message.</span></span>

<span data-ttu-id="beae4-111">Kun jaettuun ylätunnisteosaan lisätään tervetulosanoma, se näkyy jokaisella sivulla, jolla käytetään jaettua ylätunnisteen osaa.</span><span class="sxs-lookup"><span data-stu-id="beae4-111">When a welcome message is added to a shared header fragment, it will be shown on every page that uses the template where that shared header fragment is used.</span></span>

<span data-ttu-id="beae4-112">Voit lisätä sivustoon tervetulosanoman seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="beae4-112">To add a welcome message to your site, follow these steps.</span></span>

1. <span data-ttu-id="beae4-113">Siirry sivustollesi Commerce-sivuston luontiohjelmassa.</span><span class="sxs-lookup"><span data-stu-id="beae4-113">In Commerce site builder, go to your site.</span></span>
1. <span data-ttu-id="beae4-114">Valitse **Osat**.</span><span class="sxs-lookup"><span data-stu-id="beae4-114">Select **Fragments**.</span></span>
1. <span data-ttu-id="beae4-115">Valitse ylätunnisteosa, johon sanoma lisätään.</span><span class="sxs-lookup"><span data-stu-id="beae4-115">Select the header fragment to add the message to.</span></span>
1. <span data-ttu-id="beae4-116">Laajenna jäsennyspuussa **Virhe-/tietosanomat**-kohta.</span><span class="sxs-lookup"><span data-stu-id="beae4-116">In the outline tree, expand **Error/Information messages**.</span></span>
1. <span data-ttu-id="beae4-117">Valitse hälytysmoduuli ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="beae4-117">Select the alert module, and then select **OK**.</span></span> <span data-ttu-id="beae4-118">Jos hälytysmoduulia ei vielä ole, valitse ensin kolmen pisteen painike (**...**) **Virhe-/tietosanomat**-kohdan vieressä ja valitse sitten **Lisää moduuli**.</span><span class="sxs-lookup"><span data-stu-id="beae4-118">If an alert module doesn't yet exist, first select the ellipsis button (**...**) next to **Error/Information messages**, and then select **Add module**.</span></span>
1. <span data-ttu-id="beae4-119">Valitse oikealla olevassa ominaisuusruudussa **Tiedot**-välilehden **Lisää tietolähde** -kohta ja valitse sitten **Sisältö**.</span><span class="sxs-lookup"><span data-stu-id="beae4-119">In the property pane on the right, on the **Data** tab, select **Add Data Source**, and then select **Content**.</span></span>
1. <span data-ttu-id="beae4-120">Kirjoita **Syöttöteksti**-kenttään tervetulosanoman teksti.</span><span class="sxs-lookup"><span data-stu-id="beae4-120">In the **Input Text** field, enter the text of the welcome message.</span></span>
1. <span data-ttu-id="beae4-121">Valitse **Tallenna**, valitse **Viimeistele muokkaus** tarkistaaksesi ylätunnisteen osan, ja julkaise se valitsemalla **Julkaise**.</span><span class="sxs-lookup"><span data-stu-id="beae4-121">Select **Save**, select **Finish editing** to check in the header fragment, and then select **Publish** to publish it.</span></span> 

<span data-ttu-id="beae4-122">Tervetulosanoma tulee nyt näkyviin jokaisen valittua ylätunnisteosaa käyttävän sivuston sivun yläosaan.</span><span class="sxs-lookup"><span data-stu-id="beae4-122">The welcome message will now appear at the top of every site page that uses the selected header fragment.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="beae4-123">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="beae4-123">Additional resources</span></span>

[<span data-ttu-id="beae4-124">Logon lisääminen</span><span class="sxs-lookup"><span data-stu-id="beae4-124">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="beae4-125">Sivuston teeman valitseminen</span><span class="sxs-lookup"><span data-stu-id="beae4-125">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="beae4-126">CSS-ohitustiedostojen parissa työskentely</span><span class="sxs-lookup"><span data-stu-id="beae4-126">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="beae4-127">Favicon-kuvakkeen lisääminen</span><span class="sxs-lookup"><span data-stu-id="beae4-127">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="beae4-128">Copyright-ilmoituksen lisääminen</span><span class="sxs-lookup"><span data-stu-id="beae4-128">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="beae4-129">Kielten lisääminen sivustoon</span><span class="sxs-lookup"><span data-stu-id="beae4-129">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="beae4-130">Komentosarjakoodin lisääminen sivuston sivuihin telemetrian tukemiseksi</span><span class="sxs-lookup"><span data-stu-id="beae4-130">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

