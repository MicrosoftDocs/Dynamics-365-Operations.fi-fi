---
title: Luo tuotenumeroiden nimikkeistö esimääritetyille tuotevarianteille
description: Tässä ohjeessa kuvataan, miten tuotenumeroiden nimikkeistö määritetään esimääritetyille tuotevarianteille ja miten se voidaan liittää asianmukaiseen tuotedimensioryhmään.
author: ShylaThompson
manager: tfehr
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, EcoResNomenclature, EcoResProductDimensionGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6a4ad70a87cd8c6cab2e9853f4f6c52f574d318a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5257411"
---
# <a name="create-a-product-number-nomenclature-for-predefined-product-variants"></a><span data-ttu-id="360cc-103">Luo tuotenumeroiden nimikkeistö esimääritetyille tuotevarianteille</span><span class="sxs-lookup"><span data-stu-id="360cc-103">Create a product number nomenclature for predefined product variants</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="360cc-104">Tässä ohjeessa kuvataan, miten tuotenumeroiden nimikkeistö määritetään esimääritetyille tuotevarianteille ja miten se voidaan liittää asianmukaiseen tuotedimensioryhmään.</span><span class="sxs-lookup"><span data-stu-id="360cc-104">This topic explains how to set up a product number nomenclature for predefined product variants, and how you assign it to the appropriate product dimension group.</span></span> <span data-ttu-id="360cc-105">Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="360cc-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="360cc-106">Uuden tuotenumeroiden nimikkeistö on määritetty värin ja koon tuotedimensioryhmään.</span><span class="sxs-lookup"><span data-stu-id="360cc-106">The new product number nomenclature is assigned to the Color and Size product dimension group.</span></span> <span data-ttu-id="360cc-107">Tuotesuunnittelija tekee yleensä tämän tehtävän.</span><span class="sxs-lookup"><span data-stu-id="360cc-107">This task would typically be done by a product designer.</span></span>


## <a name="create-a-product-number-nomenclature"></a><span data-ttu-id="360cc-108">Tuotenumeroiden nimikkeistön luominen</span><span class="sxs-lookup"><span data-stu-id="360cc-108">Create a product number nomenclature</span></span>
1. <span data-ttu-id="360cc-109">Valitse **Tuotevarianttimallin määritys**.</span><span class="sxs-lookup"><span data-stu-id="360cc-109">Select **Product variant model definition**.</span></span>
2. <span data-ttu-id="360cc-110">Valitse **Tuotenumeron nimikkeistö**.</span><span class="sxs-lookup"><span data-stu-id="360cc-110">Select **Product nomenclature**.</span></span>
3. <span data-ttu-id="360cc-111">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="360cc-111">Select **New**.</span></span>
4. <span data-ttu-id="360cc-112">Kirjoita **Nimi**-kenttään nimikkeistön nimi, jolla kohteena olevan tuotedimensioryhmän tunnistaa, esimerkiksi `ColorSize`.</span><span class="sxs-lookup"><span data-stu-id="360cc-112">In the **Name** field, enter a nomenclature name that helps to identify the target product dimension group, for example, `ColorSize`.</span></span>
5. <span data-ttu-id="360cc-113">Kirjoita **Kuvaus**-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="360cc-113">In the **Description** field, type a value.</span></span>
6. <span data-ttu-id="360cc-114">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="360cc-114">Select **Add**.</span></span>
7. <span data-ttu-id="360cc-115">Valitse **Päätuotteen numero**.</span><span class="sxs-lookup"><span data-stu-id="360cc-115">Select **Product master** number.</span></span>
8. <span data-ttu-id="360cc-116">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="360cc-116">Select **Add**.</span></span>
9. <span data-ttu-id="360cc-117">Valitse **Tekstivakio**.</span><span class="sxs-lookup"><span data-stu-id="360cc-117">Select **Text constant**.</span></span>
10. <span data-ttu-id="360cc-118">Kirjoita arvo **Teksti**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="360cc-118">In the **Text** field, type a value.</span></span>
11. <span data-ttu-id="360cc-119">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="360cc-119">Select **Add**.</span></span>
12. <span data-ttu-id="360cc-120">Valitse **Väri**.</span><span class="sxs-lookup"><span data-stu-id="360cc-120">Select **Color**.</span></span>
13. <span data-ttu-id="360cc-121">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="360cc-121">Select **Add**.</span></span>
14. <span data-ttu-id="360cc-122">Valitse **Tekstivakio**.</span><span class="sxs-lookup"><span data-stu-id="360cc-122">Select **Text constant**.</span></span>
15. <span data-ttu-id="360cc-123">Kirjoita arvo **Teksti**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="360cc-123">In the **Text** field, type a value.</span></span>
16. <span data-ttu-id="360cc-124">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="360cc-124">Select **Add**.</span></span>
17. <span data-ttu-id="360cc-125">Valitse **Koko**.</span><span class="sxs-lookup"><span data-stu-id="360cc-125">Select **Size**.</span></span>
18. <span data-ttu-id="360cc-126">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="360cc-126">Close the page.</span></span>

## <a name="assign-the-nomenclature-to-a-product-master"></a><span data-ttu-id="360cc-127">Nimikkeistön määrittäminen päätuotteelle</span><span class="sxs-lookup"><span data-stu-id="360cc-127">Assign the nomenclature to a product master</span></span>
1. <span data-ttu-id="360cc-128">Valitse **Tuotedimensioryhmät**.</span><span class="sxs-lookup"><span data-stu-id="360cc-128">Select **Product dimension groups**.</span></span>
2. <span data-ttu-id="360cc-129">Valitse **SizeCol-tuotedimensioryhmä**.</span><span class="sxs-lookup"><span data-stu-id="360cc-129">Select the **SizeCol product dimension** group.</span></span>
3. <span data-ttu-id="360cc-130">Valitse **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="360cc-130">Select **Edit**.</span></span>
4. <span data-ttu-id="360cc-131">Valitse **Käytä nimikkeistöä** -kentässä **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="360cc-131">Select **Yes** in the **Use nomenclature** field.</span></span>
5. <span data-ttu-id="360cc-132">Syötä tai valitse arvo **Tuotevariantin numeron nimikkeistö** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="360cc-132">In the **Product variant number nomenclature** field, enter or select a value.</span></span>
6. <span data-ttu-id="360cc-133">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="360cc-133">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]