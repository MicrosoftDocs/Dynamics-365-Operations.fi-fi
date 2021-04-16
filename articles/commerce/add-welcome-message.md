---
title: Tervetuloviestin lisääminen
description: Tässä ohjeaiheessa kuvataan, miten tervetulosanoma lisätään Microsoft Dynamics 365 Commerce -sivustoon.
author: psimolin
ms.date: 04/13/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 3e61f43eca7d1343d020e1c01b5b1140f07b63c6
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797380"
---
# <a name="add-a-welcome-message"></a><span data-ttu-id="2710d-103">Tervetuloviestin lisääminen</span><span class="sxs-lookup"><span data-stu-id="2710d-103">Add a welcome message</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="2710d-104">Tässä ohjeaiheessa kuvataan, miten tervetulosanoma lisätään Microsoft Dynamics 365 Commerce -sivustoon.</span><span class="sxs-lookup"><span data-stu-id="2710d-104">This topic describes how to add a welcome message to your Microsoft Dynamics 365 Commerce website.</span></span>

<span data-ttu-id="2710d-105">Sähköisen kaupankäynnin sivuston tervetulosanoma voi kertoa kävijöille meneillään olevista alennusmyynneistä, sivuston päivityksistä ja kausittaisista kokoelmista.</span><span class="sxs-lookup"><span data-stu-id="2710d-105">A welcome message on your e-Commerce website can inform visitors about ongoing sales, site updates, or availability of seasonal collections.</span></span> <span data-ttu-id="2710d-106">Tervetulosanoma määritetään hälytysmoduulin avulla.</span><span class="sxs-lookup"><span data-stu-id="2710d-106">The welcome message is set by using the alert module.</span></span>

<span data-ttu-id="2710d-107">Hälytysmoduuli on lisättävä ylätunnisteosan **Virhe/tietosanomat**-paikkaan.</span><span class="sxs-lookup"><span data-stu-id="2710d-107">The alert module should be added to the **Error/Information messages** slot of the header fragment.</span></span> <span data-ttu-id="2710d-108">Hälytysmoduulin avulla voit määrittää näkyvän tekstin, tekstin värin ja tasauksen.</span><span class="sxs-lookup"><span data-stu-id="2710d-108">The alert module lets you specify the text that is shown, the text color, and the alignment.</span></span> <span data-ttu-id="2710d-109">Sen avulla voit myös määrittää, voivatko sivuston vierailijat hylätä viestin.</span><span class="sxs-lookup"><span data-stu-id="2710d-109">It also lets you specify whether visitors to the site can dismiss the message.</span></span>

<span data-ttu-id="2710d-110">Kun jaettuun ylätunnisteosaan lisätään tervetulosanoma, se näkyy jokaisella sivulla, jolla käytetään jaettua ylätunnisteen osaa.</span><span class="sxs-lookup"><span data-stu-id="2710d-110">When a welcome message is added to a shared header fragment, it will be shown on every page that uses the template where that shared header fragment is used.</span></span>

<span data-ttu-id="2710d-111">Voit lisätä sivustoon tervetulosanoman seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="2710d-111">To add a welcome message to your site, follow these steps.</span></span>

1. <span data-ttu-id="2710d-112">Siirry sivustollesi Commerce-sivuston luontiohjelmassa.</span><span class="sxs-lookup"><span data-stu-id="2710d-112">In Commerce site builder, go to your site.</span></span>
1. <span data-ttu-id="2710d-113">Valitse **Osat**.</span><span class="sxs-lookup"><span data-stu-id="2710d-113">Select **Fragments**.</span></span>
1. <span data-ttu-id="2710d-114">Valitse ylätunnisteosa, johon sanoma lisätään.</span><span class="sxs-lookup"><span data-stu-id="2710d-114">Select the header fragment to add the message to.</span></span>
1. <span data-ttu-id="2710d-115">Laajenna jäsennyspuussa **Virhe-/tietosanomat**-kohta.</span><span class="sxs-lookup"><span data-stu-id="2710d-115">In the outline tree, expand **Error/Information messages**.</span></span>
1. <span data-ttu-id="2710d-116">Valitse hälytysmoduuli ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="2710d-116">Select the alert module, and then select **OK**.</span></span> <span data-ttu-id="2710d-117">Jos hälytysmoduulia ei vielä ole, valitse ensin kolmen pisteen painike (**...**) **Virhe-/tietosanomat**-kohdan vieressä ja valitse sitten **Lisää moduuli**.</span><span class="sxs-lookup"><span data-stu-id="2710d-117">If an alert module doesn't yet exist, first select the ellipsis button (**...**) next to **Error/Information messages**, and then select **Add module**.</span></span>
1. <span data-ttu-id="2710d-118">Valitse oikealla olevassa ominaisuusruudussa **Tiedot**-välilehden **Lisää tietolähde** -kohta ja valitse sitten **Sisältö**.</span><span class="sxs-lookup"><span data-stu-id="2710d-118">In the property pane on the right, on the **Data** tab, select **Add Data Source**, and then select **Content**.</span></span>
1. <span data-ttu-id="2710d-119">Kirjoita **Syöttöteksti**-kenttään tervetulosanoman teksti.</span><span class="sxs-lookup"><span data-stu-id="2710d-119">In the **Input Text** field, enter the text of the welcome message.</span></span>
1. <span data-ttu-id="2710d-120">Valitse **Tallenna**, valitse **Viimeistele muokkaus** tarkistaaksesi ylätunnisteen osan, ja julkaise se valitsemalla **Julkaise**.</span><span class="sxs-lookup"><span data-stu-id="2710d-120">Select **Save**, select **Finish editing** to check in the header fragment, and then select **Publish** to publish it.</span></span> 

<span data-ttu-id="2710d-121">Tervetulosanoma tulee nyt näkyviin jokaisen valittua ylätunnisteosaa käyttävän sivuston sivun yläosaan.</span><span class="sxs-lookup"><span data-stu-id="2710d-121">The welcome message will now appear at the top of every site page that uses the selected header fragment.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2710d-122">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="2710d-122">Additional resources</span></span>

[<span data-ttu-id="2710d-123">Logon lisääminen</span><span class="sxs-lookup"><span data-stu-id="2710d-123">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="2710d-124">Sivuston teeman valitseminen</span><span class="sxs-lookup"><span data-stu-id="2710d-124">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="2710d-125">CSS-ohitustiedostojen parissa työskentely</span><span class="sxs-lookup"><span data-stu-id="2710d-125">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="2710d-126">Favicon-kuvakkeen lisääminen</span><span class="sxs-lookup"><span data-stu-id="2710d-126">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="2710d-127">Copyright-ilmoituksen lisääminen</span><span class="sxs-lookup"><span data-stu-id="2710d-127">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="2710d-128">Kielten lisääminen sivustoon</span><span class="sxs-lookup"><span data-stu-id="2710d-128">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="2710d-129">Komentosarjakoodin lisääminen sivuston sivuihin telemetrian tukemiseksi</span><span class="sxs-lookup"><span data-stu-id="2710d-129">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
