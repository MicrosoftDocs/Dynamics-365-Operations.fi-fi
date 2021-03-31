---
title: Varianttiryhmän luonti
description: Tässä aiheessa kuvataan, miten tuotteelle luodaan koko-, tyyli- tai värivarianttiryhmiä Microsoft Dynamics 365 Commercessa.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: RetailSizeGroupTable, ConfigGroupIdLookup, RetailStyleGroupTable
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 4c34aca043f10fef38f186800c429cac36c41ce7
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5207844"
---
# <a name="create-a-variant-group"></a><span data-ttu-id="f8b98-103">Varianttiryhmän luominen</span><span class="sxs-lookup"><span data-stu-id="f8b98-103">Create a variant group</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="f8b98-104">Tässä aiheessa kuvataan, miten tuotteelle luodaan koko-, tyyli- tai värivarianttiryhmiä Microsoft Dynamics 365 Commercessa.</span><span class="sxs-lookup"><span data-stu-id="f8b98-104">This topic describes how to create a size, style, or color variant group for a product in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="f8b98-105">Yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="f8b98-105">Overview</span></span>

<span data-ttu-id="f8b98-106">Dynamics 365 Commerce tukee tuotteelle useita variantteja.</span><span class="sxs-lookup"><span data-stu-id="f8b98-106">Dynamics 365 Commerce supports multiple variants for products.</span></span> <span data-ttu-id="f8b98-107">Varianttiryhmien määrittäminen eri tuoteluokille on paras ratkaisu.</span><span class="sxs-lookup"><span data-stu-id="f8b98-107">It is ideal to set up variant groups for different product categories.</span></span> <span data-ttu-id="f8b98-108">Esimerkiksi t-paidoille voidaan luoda kokoryhmä, joka sisältää koot XS, S, M, L ja XL, tai väriryhmä, joka sisältää kaikki tuotteen saatavilla olevat värivaihtoehdot.</span><span class="sxs-lookup"><span data-stu-id="f8b98-108">For example, a size group can be created for t-shirts with sizes extra small, small, medium, large, and extra large, or a color group could be created to include all available colors of a product.</span></span> <span data-ttu-id="f8b98-109">Varianttiryhmät kannattaa lisätä ennen tuotteiden lisäämistä.</span><span class="sxs-lookup"><span data-stu-id="f8b98-109">Variant groups should be added before products are added.</span></span>

<span data-ttu-id="f8b98-110">Tässä ohjeaiheessa luodaan ja määritetään kokoryhmä.</span><span class="sxs-lookup"><span data-stu-id="f8b98-110">In this topic, a size group will be created and configured.</span></span> <span data-ttu-id="f8b98-111">Vastaavia menettelyjä voidaan käyttää tyyli- ja väriryhmien lisäämiseen ja määrittämiseen.</span><span class="sxs-lookup"><span data-stu-id="f8b98-111">Similar procedures can be used for adding and configuring style groups and color groups.</span></span>

## <a name="create-a-size-group"></a><span data-ttu-id="f8b98-112">Kokoryhmän luominen</span><span class="sxs-lookup"><span data-stu-id="f8b98-112">Create a size group</span></span>

<span data-ttu-id="f8b98-113">Luo kokoryhmä noudattamalla seuraavia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="f8b98-113">To create a size group, follow these steps.</span></span>
 
1. <span data-ttu-id="f8b98-114">Siirry siirtymisruudussa kohtaan **Moduulit \> Vähittäiskauppa ja kauppa \> Tuotteet ja luokat \> Varianttiryhmät \> Kokoryhmät**.</span><span class="sxs-lookup"><span data-stu-id="f8b98-114">In the navigation pane, go to **Modules \> Retail and commerce \> Products and categories \> Variant groups \> Size groups**.</span></span>
1. <span data-ttu-id="f8b98-115">Valitse toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="f8b98-115">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="f8b98-116">Anna **Kokoryhmä**-ruudussa kokoryhmän yksilöivä nimi.</span><span class="sxs-lookup"><span data-stu-id="f8b98-116">In the **Size group** box, enter a name for the size group.</span></span>
1. <span data-ttu-id="f8b98-117">Kirjoita soveltuva kuvaus **Kuvaus**-ruutuun.</span><span class="sxs-lookup"><span data-stu-id="f8b98-117">In the **Description** box, enter an appropriate description.</span></span>
1. <span data-ttu-id="f8b98-118">Valitse toimintoruudussa **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="f8b98-118">On the action pane, select **Save**.</span></span>

## <a name="add-attributes-to-the-size-group"></a><span data-ttu-id="f8b98-119">Määritteiden lisääminen kokoryhmään</span><span class="sxs-lookup"><span data-stu-id="f8b98-119">Add attributes to the size group</span></span>

<span data-ttu-id="f8b98-120">Voit lisätä määritteitä kokoryhmään seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="f8b98-120">To add attributes to a size group, follow these steps.</span></span>

1. <span data-ttu-id="f8b98-121">Siirry siirtymisruudussa kohtaan **Moduulit \> Vähittäiskauppa ja kauppa \> Tuotteet ja luokat \> Varianttiryhmät \> Kokoryhmät**</span><span class="sxs-lookup"><span data-stu-id="f8b98-121">In the navigation pane, go to **Modules \> Retail and commerce \> Products and categories \> Variant groups \> Size groups**</span></span>
1. <span data-ttu-id="f8b98-122">Valitse kokoryhmä siirtymisruudussa.</span><span class="sxs-lookup"><span data-stu-id="f8b98-122">In the navigation pane, select a size group.</span></span>
1. <span data-ttu-id="f8b98-123">Valitse **Kokoryhmärivit**-kohdassa **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="f8b98-123">Under **Size group lines**, select **Add**.</span></span>
1. <span data-ttu-id="f8b98-124">Kirjoita **Koko**-ruutuun merkkijono, joka edustaa kokoa (esim. XL).</span><span class="sxs-lookup"><span data-stu-id="f8b98-124">In the **Size** box, enter a string representing the size (for example, "XL").</span></span>
1. <span data-ttu-id="f8b98-125">Kirjoita **Koon nimi** -ruutuun koon nimi (esimerkiksi Extra Large).</span><span class="sxs-lookup"><span data-stu-id="f8b98-125">In the **Size name** box, enter a name for the size (for example, "Extra Large").</span></span>
1. <span data-ttu-id="f8b98-126">Syötä **Täydennyspaino**-ruutuun numero, joka edustaa täydennyspainoa.</span><span class="sxs-lookup"><span data-stu-id="f8b98-126">In the **Replenishment weight** box, enter a number representing the replenishment weight.</span></span>
1. <span data-ttu-id="f8b98-127">Syötä **Viivakoodin numero**-ruutuun viivakoodia edustava numero.</span><span class="sxs-lookup"><span data-stu-id="f8b98-127">In the **Number in bar code** box, enter a number representing the bar code.</span></span>
1. <span data-ttu-id="f8b98-128">Syötä **Näyttöjärjestys**-ruutuun numero, joka edustaa näyttöjärjestystä.</span><span class="sxs-lookup"><span data-stu-id="f8b98-128">In the **Display order** box, enter a number representing the display order.</span></span>
1. <span data-ttu-id="f8b98-129">Kun olet lisännyt tarvittavat koot, valitse toimintoruudussa **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="f8b98-129">When finished adding sizes, select **Save** on the action pane.</span></span>

<span data-ttu-id="f8b98-130">Seuraavassa kuvassa on esimerkki rentojen paitakokojen kokoryhmästä.</span><span class="sxs-lookup"><span data-stu-id="f8b98-130">The following image shows an example of a size group for "casual shirt sizes".</span></span>

![Kokoryhmän luominen](media/create-variant-group.png)

## <a name="additional-resources"></a><span data-ttu-id="f8b98-132">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="f8b98-132">Additional resources</span></span>

[<span data-ttu-id="f8b98-133">Tuotetietojen yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="f8b98-133">Product information overview</span></span>](../supply-chain/pim/product-information.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="f8b98-134">Vähittäismyyntituotteiden määrittäminen</span><span class="sxs-lookup"><span data-stu-id="f8b98-134">Set up retail products</span></span>](set-up-retail-products.md)

[<span data-ttu-id="f8b98-135">Tuotedimensiot</span><span class="sxs-lookup"><span data-stu-id="f8b98-135">Product dimensions</span></span>](../supply-chain/pim/product-dimensions.md?toc=/dynamics365/commerce/toc.json)


[!INCLUDE[footer-include](../includes/footer-banner.md)]