---
title: Copyright-ilmoituksen lisääminen
description: Tässä ohjeaiheessa kerrotaan, miten voit lisätä sähköisen kaupankäynnin sivustoon copyright-ilmoituksen.
author: psimolin
manager: AnnBe
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
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 58c2949057ef777f706d12cee2dd3341d1a3b7e6
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/20/2019
ms.locfileid: "2914565"
---
# <a name="add-a-copyright-notice"></a><span data-ttu-id="b5668-103">Copyright-ilmoituksen lisääminen</span><span class="sxs-lookup"><span data-stu-id="b5668-103">Add a copyright notice</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="b5668-104">Tässä ohjeaiheessa kerrotaan, miten voit lisätä sähköisen kaupankäynnin sivustoon copyright-ilmoituksen.</span><span class="sxs-lookup"><span data-stu-id="b5668-104">This topic describes how to add a copyright notice to your e-Commerce website.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="b5668-105">Edellytykset</span><span class="sxs-lookup"><span data-stu-id="b5668-105">Prerequisites</span></span>

<span data-ttu-id="b5668-106">Ennen kuin voit lisätä copyright-ilmoituksen sivustoon, siinä on oltava seuraavat nimikkeet:</span><span class="sxs-lookup"><span data-stu-id="b5668-106">Before you can add a copyright notice to your site, you must have the following items:</span></span>

- <span data-ttu-id="b5668-107">Malli, joka sisältää jaetun alatunnisteen osan.</span><span class="sxs-lookup"><span data-stu-id="b5668-107">A template that includes a shared footer fragment.</span></span>
- <span data-ttu-id="b5668-108">Sivu, joka käyttää kyseistä mallia.</span><span class="sxs-lookup"><span data-stu-id="b5668-108">A page that uses that template.</span></span>

## <a name="add-a-copyright-notice"></a><span data-ttu-id="b5668-109">Copyright-ilmoituksen lisääminen</span><span class="sxs-lookup"><span data-stu-id="b5668-109">Add a copyright notice</span></span>

<span data-ttu-id="b5668-110">Voit lisätä copyright-ilmoituksen jokaisen tiettyä mallia käyttävän sivun alaosaan seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="b5668-110">To add a copyright notice to the bottom of every page that uses a specific template, follow these steps.</span></span>

1. <span data-ttu-id="b5668-111">Siirry kohtaan **Osat** ja **Uusi sivun osa**.</span><span class="sxs-lookup"><span data-stu-id="b5668-111">Go to **Fragments**, and then select **New Page Fragment**.</span></span>
1. <span data-ttu-id="b5668-112">Valitse valintaikkunassa **Alatunniste**-moduuli ja anna osalle nimi.</span><span class="sxs-lookup"><span data-stu-id="b5668-112">In the dialog box, select the **Footer** module, and name the fragment.</span></span> <span data-ttu-id="b5668-113">Kirjoita esimerkiksi **Alatunniste - copyright**.</span><span class="sxs-lookup"><span data-stu-id="b5668-113">For example, enter **Footer-Copyright**.</span></span>
1. <span data-ttu-id="b5668-114">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="b5668-114">Select **OK**.</span></span>
1. <span data-ttu-id="b5668-115">Valitse siirtymisruudussa kolmen pisteen painike (**...**) **Alatunniste**-kohdan vieressä ja valitse sitten **Lisää moduuli**.</span><span class="sxs-lookup"><span data-stu-id="b5668-115">In the navigation pane, select the ellipsis button (**...**) next to **Footer**, and then select **Add Module**.</span></span>
1. <span data-ttu-id="b5668-116">Valitse valintaikkunassa **Alatunnisteluokka** ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="b5668-116">In the dialog box, select **Footer category**, and then select **OK**.</span></span>
1. <span data-ttu-id="b5668-117">Valitse siirtymisruudussa kolmen pisteen painike **Alatunnisteluokka**-kohdan vieressä ja valitse sitten **Lisää moduuli**.</span><span class="sxs-lookup"><span data-stu-id="b5668-117">In the navigation pane, select the ellipsis button next to **Footer category**, and then select **Add Module**.</span></span>
1. <span data-ttu-id="b5668-118">Valitse valintaikkunassa **Sisällöntäyteinen lohkonimike** ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="b5668-118">In the dialog box, select **Content rich block item**, and then select **OK**.</span></span>
1. <span data-ttu-id="b5668-119">Valitse siirtymisruudussa **Sisällöntäyteinen lohkonimike**.</span><span class="sxs-lookup"><span data-stu-id="b5668-119">In the navigation pane, select **Content rich block item**.</span></span>
1. <span data-ttu-id="b5668-120">Lisää oikealla olevassa ominaisuusruudussa **Kappale**-kenttään copyright-sanoma.</span><span class="sxs-lookup"><span data-stu-id="b5668-120">In the properties pane on the right, in the **Paragraph** field, add your copyright message.</span></span> <span data-ttu-id="b5668-121">Syötä esimerkiksi teksti **(C) Fabrikam 2019**.</span><span class="sxs-lookup"><span data-stu-id="b5668-121">For example, enter **(C) Fabrikam 2019**.</span></span>
1. <span data-ttu-id="b5668-122">Valitse **Tallenna**. Valitse **Kirjaa sisään** ja valitse sitten **Julkaise**.</span><span class="sxs-lookup"><span data-stu-id="b5668-122">Select **Save**, select **Check In**, and then select **Publish**.</span></span>
1. <span data-ttu-id="b5668-123">Siirry **Mallit**-kohtaan, valitse malli ja valitse sitten **Kirjaa ulos**.</span><span class="sxs-lookup"><span data-stu-id="b5668-123">Go to **Templates**, select the template, and then select **Check Out**.</span></span>
1. <span data-ttu-id="b5668-124">Laajenna **Sivun jäsennys** -kohdassa **Tekstiosa** ja laajenna sitten **Oletussivu**-kohta.</span><span class="sxs-lookup"><span data-stu-id="b5668-124">Under **Page Outline**, expand **Body**, and then expand **Default Page**.</span></span>
1. <span data-ttu-id="b5668-125">Valitse **Ylätunnistepaikka**-kohdan vieressä oleva kolmen pisteen painike ja valitse sitten **Lisää osa**.</span><span class="sxs-lookup"><span data-stu-id="b5668-125">Select the ellipsis button next to **Footer Slot**, and then select **Add Fragment**.</span></span>
1. <span data-ttu-id="b5668-126">Valitse aiemmin luomasi osa ja valitse sitten **Valitse**.</span><span class="sxs-lookup"><span data-stu-id="b5668-126">Select the fragment that you created earlier, and then select **Select**.</span></span>
1. <span data-ttu-id="b5668-127">Kirjaa malli sisään ja julkaise se.</span><span class="sxs-lookup"><span data-stu-id="b5668-127">Check in the template, and publish it.</span></span>

<span data-ttu-id="b5668-128">Copyright-ilmoituksen sisältävä alatunniste näkyy automaattisesti kaikkien valittua mallia käyttävien sivujen alaosassa.</span><span class="sxs-lookup"><span data-stu-id="b5668-128">The footer that contains the copyright notice automatically appears at the bottom of all pages that use the selected template.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b5668-129">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="b5668-129">Additional resources</span></span>

[<span data-ttu-id="b5668-130">Logon lisääminen</span><span class="sxs-lookup"><span data-stu-id="b5668-130">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="b5668-131">Sivuston teeman valitseminen</span><span class="sxs-lookup"><span data-stu-id="b5668-131">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="b5668-132">CSS-ohitustiedostojen parissa työskentely</span><span class="sxs-lookup"><span data-stu-id="b5668-132">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="b5668-133">Favicon-kuvakkeen lisääminen</span><span class="sxs-lookup"><span data-stu-id="b5668-133">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="b5668-134">Tervetuloviestin lisääminen</span><span class="sxs-lookup"><span data-stu-id="b5668-134">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="b5668-135">Kielten lisääminen sivustoon</span><span class="sxs-lookup"><span data-stu-id="b5668-135">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="b5668-136">Komentosarjakoodin lisääminen sivuston sivuihin telemetrian tukemiseksi</span><span class="sxs-lookup"><span data-stu-id="b5668-136">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

