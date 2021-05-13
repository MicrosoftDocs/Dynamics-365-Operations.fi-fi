---
title: Luo tuotenumeroiden nimikkeistö esimääritetyille tuotevarianteille
description: Tässä ohjeessa kuvataan, miten tuotenumeroiden nimikkeistö määritetään esimääritetyille tuotevarianteille ja miten se voidaan liittää asianmukaiseen tuotedimensioryhmään.
author: ShylaThompson
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, EcoResNomenclature, EcoResProductDimensionGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4bb73854f52525c0722683086d1b4f1dd7173306
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920654"
---
# <a name="create-a-product-number-nomenclature-for-predefined-product-variants"></a><span data-ttu-id="bbbbc-103">Luo tuotenumeroiden nimikkeistö esimääritetyille tuotevarianteille</span><span class="sxs-lookup"><span data-stu-id="bbbbc-103">Create a product number nomenclature for predefined product variants</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="bbbbc-104">Tässä ohjeessa kuvataan, miten tuotenumeroiden nimikkeistö määritetään esimääritetyille tuotevarianteille ja miten se voidaan liittää asianmukaiseen tuotedimensioryhmään.</span><span class="sxs-lookup"><span data-stu-id="bbbbc-104">This topic explains how to set up a product number nomenclature for predefined product variants, and how you assign it to the appropriate product dimension group.</span></span> <span data-ttu-id="bbbbc-105">Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="bbbbc-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="bbbbc-106">Uuden tuotenumeroiden nimikkeistö on määritetty värin ja koon tuotedimensioryhmään.</span><span class="sxs-lookup"><span data-stu-id="bbbbc-106">The new product number nomenclature is assigned to the Color and Size product dimension group.</span></span> <span data-ttu-id="bbbbc-107">Tuotesuunnittelija tekee yleensä tämän tehtävän.</span><span class="sxs-lookup"><span data-stu-id="bbbbc-107">This task would typically be done by a product designer.</span></span>


## <a name="create-a-product-number-nomenclature"></a><span data-ttu-id="bbbbc-108">Tuotenumeroiden nimikkeistön luominen</span><span class="sxs-lookup"><span data-stu-id="bbbbc-108">Create a product number nomenclature</span></span>

1. <span data-ttu-id="bbbbc-109">Valitse **Tuotetietojen hallinta \> Asetukset \> Tuotenimikkeistö**.</span><span class="sxs-lookup"><span data-stu-id="bbbbc-109">Go to **Product information management \> Setup \> Product nomenclature**.</span></span>
1. <span data-ttu-id="bbbbc-110">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="bbbbc-110">Select **New**.</span></span>
1. <span data-ttu-id="bbbbc-111">Kirjoita **Nimi**-kenttään nimikkeistön nimi, jolla kohteena olevan tuotedimensioryhmän tunnistaa, esimerkiksi `ColorSize`.</span><span class="sxs-lookup"><span data-stu-id="bbbbc-111">In the **Name** field, enter a nomenclature name that helps to identify the target product dimension group, for example, `ColorSize`.</span></span>
1. <span data-ttu-id="bbbbc-112">Kirjoita **Kuvaus**-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="bbbbc-112">In the **Description** field, type a value.</span></span>
1. <span data-ttu-id="bbbbc-113">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="bbbbc-113">Select **Add**.</span></span>
1. <span data-ttu-id="bbbbc-114">Valitse **Päätuotteen numero**.</span><span class="sxs-lookup"><span data-stu-id="bbbbc-114">Select **Product master** number.</span></span>
1. <span data-ttu-id="bbbbc-115">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="bbbbc-115">Select **Add**.</span></span>
1. <span data-ttu-id="bbbbc-116">Valitse **Tekstivakio**.</span><span class="sxs-lookup"><span data-stu-id="bbbbc-116">Select **Text constant**.</span></span>
1. <span data-ttu-id="bbbbc-117">Kirjoita arvo **Teksti**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="bbbbc-117">In the **Text** field, type a value.</span></span>
1. <span data-ttu-id="bbbbc-118">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="bbbbc-118">Select **Add**.</span></span>
1. <span data-ttu-id="bbbbc-119">Valitse **Väri**.</span><span class="sxs-lookup"><span data-stu-id="bbbbc-119">Select **Color**.</span></span>
1. <span data-ttu-id="bbbbc-120">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="bbbbc-120">Select **Add**.</span></span>
1. <span data-ttu-id="bbbbc-121">Valitse **Tekstivakio**.</span><span class="sxs-lookup"><span data-stu-id="bbbbc-121">Select **Text constant**.</span></span>
1. <span data-ttu-id="bbbbc-122">Kirjoita arvo **Teksti**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="bbbbc-122">In the **Text** field, type a value.</span></span>
1. <span data-ttu-id="bbbbc-123">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="bbbbc-123">Select **Add**.</span></span>
1. <span data-ttu-id="bbbbc-124">Valitse **Koko**.</span><span class="sxs-lookup"><span data-stu-id="bbbbc-124">Select **Size**.</span></span>
1. <span data-ttu-id="bbbbc-125">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="bbbbc-125">Close the page.</span></span>

## <a name="assign-the-nomenclature-to-a-product-master"></a><span data-ttu-id="bbbbc-126">Nimikkeistön määrittäminen päätuotteelle</span><span class="sxs-lookup"><span data-stu-id="bbbbc-126">Assign the nomenclature to a product master</span></span>

1. <span data-ttu-id="bbbbc-127">Valitse **Tuotedimensioryhmät**.</span><span class="sxs-lookup"><span data-stu-id="bbbbc-127">Select **Product dimension groups**.</span></span>
2. <span data-ttu-id="bbbbc-128">Valitse **SizeCol-tuotedimensioryhmä**.</span><span class="sxs-lookup"><span data-stu-id="bbbbc-128">Select the **SizeCol product dimension** group.</span></span>
3. <span data-ttu-id="bbbbc-129">Valitse **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="bbbbc-129">Select **Edit**.</span></span>
4. <span data-ttu-id="bbbbc-130">Valitse **Käytä nimikkeistöä** -kentässä **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="bbbbc-130">Select **Yes** in the **Use nomenclature** field.</span></span>
5. <span data-ttu-id="bbbbc-131">Syötä tai valitse arvo **Tuotevariantin numeron nimikkeistö** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="bbbbc-131">In the **Product variant number nomenclature** field, enter or select a value.</span></span>
6. <span data-ttu-id="bbbbc-132">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="bbbbc-132">Close the page.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]