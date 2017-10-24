---
title: "Määritä viivakoodit"
description: "Tässä artikkelissa kuvataan viivakoodien käyttö Microsoft Dynamics 365 for Retailissa."
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 15971
ms.assetid: 6b4b2ac2-0344-41aa-8818-62c30017d5ac
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: fdc56bf468babd4b0b0652d9791114af676c8470
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---

# <a name="set-up-bar-codes"></a><span data-ttu-id="3ce93-103">Viivakoodien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="3ce93-103">Set up bar codes</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="3ce93-104">Tässä artikkelissa kuvataan viivakoodien käyttö Microsoft Dynamics 365 for Retailissa.</span><span class="sxs-lookup"><span data-stu-id="3ce93-104">This article describes how to use bar codes in Microsoft Dynamics 365 for Retail.</span></span>

<span data-ttu-id="3ce93-105">Voit käyttää viivakoodeja tuotteiden ostamisessa ja myynnissä, tuotevarianttien seurannassa sekä asiakkaiden ja työntekijöiden määrittämisessä.</span><span class="sxs-lookup"><span data-stu-id="3ce93-105">You can use bar codes to purchase and sell products, track product variants, and set up customers and employees.</span></span> <span data-ttu-id="3ce93-106">Voit lisäksi käyttää viivakoodeja kuponkien, lahjakorttien ja hyvityslaskujen antamiseen ja käyttöön.</span><span class="sxs-lookup"><span data-stu-id="3ce93-106">You can also use bar codes to issue and endorse coupons, gift cards, and credit memos.</span></span> <span data-ttu-id="3ce93-107">Vähittäismyynnin tuotteet voi määrittää niin, että niillä on joko vakioviivakoodit tai itse kehitetyt viivakoodit.</span><span class="sxs-lookup"><span data-stu-id="3ce93-107">You can set up retail products so that they have standard bar codes or custom, in-house bar codes.</span></span> <span data-ttu-id="3ce93-108">Tuotteilla voi olla useampi viivakoodi.</span><span class="sxs-lookup"><span data-stu-id="3ce93-108">Products can have more than one bar code.</span></span> <span data-ttu-id="3ce93-109">Tuotteella voi esimerkiksi olla useita viivakoodeja, jos se on peräisin usealta valmistajalta tai jos sillä on kokoon, tyyliin tai väriin perustuvia variantteja.</span><span class="sxs-lookup"><span data-stu-id="3ce93-109">For example, a product might have multiple bar codes if it comes from various manufacturers, or if it has variants that are based on size, style, or color.</span></span> <span data-ttu-id="3ce93-110">Viivakoodit voivat sisältää tuotteen painon tai hinnan.</span><span class="sxs-lookup"><span data-stu-id="3ce93-110">Bar codes can include the weight or price of the product.</span></span> <span data-ttu-id="3ce93-111">Viivakoodin muodot ovat malleja, joita käytetään viivakoodien luomiseen.</span><span class="sxs-lookup"><span data-stu-id="3ce93-111">Bar code masks are templates that are used to create bar codes.</span></span> <span data-ttu-id="3ce93-112">**Huomautus:** Jos määrität kullekin varianttiyhdistelmälle yksilöllisen viivakoodin, voit lukea nimikkeen viivakoodin kassalla ja antaa ohjelman etsiä myytävän tuotevariantin.</span><span class="sxs-lookup"><span data-stu-id="3ce93-112">**Note:** If you assign a unique bar code to each variant combination, you can scan the bar code at the register and let the program determine which variant of the product is being sold.</span></span> <span data-ttu-id="3ce93-113">Voit myös kerätä ja tarkastella varianttiperusteisia myyntitilastoja.</span><span class="sxs-lookup"><span data-stu-id="3ce93-113">You can also collect and view statistics about sales by variant.</span></span> <span data-ttu-id="3ce93-114">Kullekin koko-, väri- ja tyyliryhmälle voidaan määrittää yksilöllinen luku, joka yksilöi ryhmän viivakoodissa.</span><span class="sxs-lookup"><span data-stu-id="3ce93-114">Each size, color, and style group can be assigned a unique number that identifies that group in the bar code.</span></span> <span data-ttu-id="3ce93-115">Dynamics 365 for Retail muodostaa viivakoodit automaattisesti kullekin muuttujayhdistelmälle viivakoodin muodon perusteella.</span><span class="sxs-lookup"><span data-stu-id="3ce93-115">Dynamics 365 for Retail uses the bar code mask to automatically generate bar codes for each variant combination.</span></span> <span data-ttu-id="3ce93-116">Tämä toiminto voi olla hyödyllinen, jos kokoja, värejä ja tyylejä on paljon, koska jokainen lisätty varianttikoodi suurentaa yhdistelmää merkittävästi.</span><span class="sxs-lookup"><span data-stu-id="3ce93-116">This functionality can be useful if there are many sizes, colors, and styles, because the number of combinations increases significantly as each variant code is added.</span></span> <span data-ttu-id="3ce93-117">Jos toimintoa ei käytetä, viivakoodit täytyy määrittää manuaalisesti kuhunkin tuotevarianttia tarkoittavaan yhdistelmään.</span><span class="sxs-lookup"><span data-stu-id="3ce93-117">If this functionality isn't used, bar codes must be manually assigned to each combination that represents a product variant.</span></span> <span data-ttu-id="3ce93-118">Viivakoodeja voi luoda manuaalisesti tai automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="3ce93-118">You can create bar codes manually or automatically.</span></span> <span data-ttu-id="3ce93-119">Viivakoodien luonti tapahtuu noudattamalla seuraavia tehtäviä järjestyksessä.</span><span class="sxs-lookup"><span data-stu-id="3ce93-119">To create bar codes, complete the following tasks in the order in which they are listed.</span></span>

1.  <span data-ttu-id="3ce93-120">[Viivakoodin muodon merkkien määrittäminen](set-up-bar-code-masks.md).</span><span class="sxs-lookup"><span data-stu-id="3ce93-120">[Set up bar code mask characters](set-up-bar-code-masks.md).</span></span>
2.  <span data-ttu-id="3ce93-121">[Viivakoodin muotojen määrittäminen](set-up-bar-code-masks.md).</span><span class="sxs-lookup"><span data-stu-id="3ce93-121">[Set up bar code masks](set-up-bar-code-masks.md).</span></span>
3.  <span data-ttu-id="3ce93-122">Määritä viivakoodiasetukset.</span><span class="sxs-lookup"><span data-stu-id="3ce93-122">Configure bar code setups.</span></span>
4.  <span data-ttu-id="3ce93-123">Luo viivakoodit tuotteille.</span><span class="sxs-lookup"><span data-stu-id="3ce93-123">Create bar codes for products.</span></span>


<a name="see-also"></a><span data-ttu-id="3ce93-124">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="3ce93-124">See also</span></span>
--------

[<span data-ttu-id="3ce93-125">Viivakoodin muotojen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="3ce93-125">Set up bar code masks</span></span>](set-up-bar-code-masks.md)




