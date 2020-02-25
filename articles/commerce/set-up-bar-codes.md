---
title: Viivakoodien määrittäminen
description: Tässä artikkelissa käsitellään viivakoodien käyttöä Dynamics 365 Commerceissa.
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailBarcodeMaskCharacter, RetailBarcodeMaskSetup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 15971
ms.assetid: 6b4b2ac2-0344-41aa-8818-62c30017d5ac
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 74a08fc168dd3c41fa501ca8110af899a181e333
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/01/2020
ms.locfileid: "3022409"
---
# <a name="set-up-bar-codes"></a><span data-ttu-id="f3ce0-103">Viivakoodien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="f3ce0-103">Set up bar codes</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="f3ce0-104">Tässä artikkelissa käsitellään viivakoodien käyttöä Dynamics 365 Commerceissa.</span><span class="sxs-lookup"><span data-stu-id="f3ce0-104">This article describes how to use bar codes in Dynamics 365 Commerce.</span></span>

<span data-ttu-id="f3ce0-105">Voit käyttää viivakoodeja tuotteiden ostamisessa ja myynnissä, tuotevarianttien seurannassa sekä asiakkaiden ja työntekijöiden määrittämisessä.</span><span class="sxs-lookup"><span data-stu-id="f3ce0-105">You can use bar codes to purchase and sell products, track product variants, and set up customers and employees.</span></span> <span data-ttu-id="f3ce0-106">Voit lisäksi käyttää viivakoodeja kuponkien, lahjakorttien ja hyvityslaskujen antamiseen ja käyttöön.</span><span class="sxs-lookup"><span data-stu-id="f3ce0-106">You can also use bar codes to issue and endorse coupons, gift cards, and credit memos.</span></span> <span data-ttu-id="f3ce0-107">Vähittäismyynnin tuotteet voi määrittää niin, että niillä on joko vakioviivakoodit tai itse kehitetyt viivakoodit.</span><span class="sxs-lookup"><span data-stu-id="f3ce0-107">You can set up retail products so that they have standard bar codes or custom, in-house bar codes.</span></span> <span data-ttu-id="f3ce0-108">Tuotteilla voi olla useampi viivakoodi.</span><span class="sxs-lookup"><span data-stu-id="f3ce0-108">Products can have more than one bar code.</span></span> <span data-ttu-id="f3ce0-109">Tuotteella voi esimerkiksi olla useita viivakoodeja, jos se on peräisin usealta valmistajalta tai jos sillä on kokoon, tyyliin tai väriin perustuvia variantteja.</span><span class="sxs-lookup"><span data-stu-id="f3ce0-109">For example, a product might have multiple bar codes if it comes from various manufacturers, or if it has variants that are based on size, style, or color.</span></span> <span data-ttu-id="f3ce0-110">Viivakoodit voivat sisältää tuotteen painon tai hinnan.</span><span class="sxs-lookup"><span data-stu-id="f3ce0-110">Bar codes can include the weight or price of the product.</span></span> <span data-ttu-id="f3ce0-111">Viivakoodin muodot ovat malleja, joita käytetään viivakoodien luomiseen.</span><span class="sxs-lookup"><span data-stu-id="f3ce0-111">Bar code masks are templates that are used to create bar codes.</span></span>

> [!NOTE]
> <span data-ttu-id="f3ce0-112">Jos määrität kullekin varianttiyhdistelmälle yksilöllisen viivakoodin, voit lukea nimikkeen viivakoodin kassalla ja antaa ohjelman etsiä myytävän tuotevariantin.</span><span class="sxs-lookup"><span data-stu-id="f3ce0-112">If you assign a unique bar code to each variant combination, you can scan the bar code at the register and let the program determine which variant of the product is being sold.</span></span> <span data-ttu-id="f3ce0-113">Voit myös kerätä ja tarkastella varianttiperusteisia myyntitilastoja.</span><span class="sxs-lookup"><span data-stu-id="f3ce0-113">You can also collect and view statistics about sales by variant.</span></span> <span data-ttu-id="f3ce0-114">Kullekin koko-, väri- ja tyyliryhmälle voidaan määrittää yksilöllinen luku, joka yksilöi ryhmän viivakoodissa.</span><span class="sxs-lookup"><span data-stu-id="f3ce0-114">Each size, color, and style group can be assigned a unique number that identifies that group in the bar code.</span></span> <span data-ttu-id="f3ce0-115">Retail muodostaa viivakoodit automaattisesti kullekin muuttujayhdistelmälle viivakoodin muodon perusteella.</span><span class="sxs-lookup"><span data-stu-id="f3ce0-115">Retail uses the bar code mask to automatically generate bar codes for each variant combination.</span></span> <span data-ttu-id="f3ce0-116">Tämä toiminto voi olla hyödyllinen, jos kokoja, värejä ja tyylejä on paljon, koska jokainen lisätty varianttikoodi suurentaa yhdistelmää merkittävästi.</span><span class="sxs-lookup"><span data-stu-id="f3ce0-116">This functionality can be useful if there are many sizes, colors, and styles, because the number of combinations increases significantly as each variant code is added.</span></span> <span data-ttu-id="f3ce0-117">Jos toimintoa ei käytetä, viivakoodit täytyy määrittää manuaalisesti kuhunkin tuotevarianttia tarkoittavaan yhdistelmään.</span><span class="sxs-lookup"><span data-stu-id="f3ce0-117">If this functionality isn't used, bar codes must be manually assigned to each combination that represents a product variant.</span></span>

<span data-ttu-id="f3ce0-118">Viivakoodeja voi luoda manuaalisesti tai automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="f3ce0-118">You can create bar codes manually or automatically.</span></span> <span data-ttu-id="f3ce0-119">Viivakoodien luonti tapahtuu noudattamalla seuraavia tehtäviä järjestyksessä.</span><span class="sxs-lookup"><span data-stu-id="f3ce0-119">To create bar codes, complete the following tasks in the order in which they are listed.</span></span>

1. <span data-ttu-id="f3ce0-120">[Viivakoodin muodon merkkien määrittäminen](set-up-bar-code-masks.md).</span><span class="sxs-lookup"><span data-stu-id="f3ce0-120">[Set up bar code mask characters](set-up-bar-code-masks.md).</span></span>
2. <span data-ttu-id="f3ce0-121">[Viivakoodin muotojen määrittäminen](set-up-bar-code-masks.md).</span><span class="sxs-lookup"><span data-stu-id="f3ce0-121">[Set up bar code masks](set-up-bar-code-masks.md).</span></span>
3. <span data-ttu-id="f3ce0-122">Määritä viivakoodiasetukset.</span><span class="sxs-lookup"><span data-stu-id="f3ce0-122">Configure bar code setups.</span></span>
4. <span data-ttu-id="f3ce0-123">Luo viivakoodit tuotteille.</span><span class="sxs-lookup"><span data-stu-id="f3ce0-123">Create bar codes for products.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f3ce0-124">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="f3ce0-124">Additional resources</span></span>

[<span data-ttu-id="f3ce0-125">Viivakoodin muotojen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="f3ce0-125">Set up bar code masks</span></span>](set-up-bar-code-masks.md)
