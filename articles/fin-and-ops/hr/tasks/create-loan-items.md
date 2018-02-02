--- 
title: Luo lainauskohteet
description: "Lainan kohteet ovat tietueita, joiden avulla voit seurata fyysisiä yrityksen työntekijöille lainaamia kohteita, kuten puhelimia ja tietokoneita."
author: kherr75
manager: AnnBe
ms.date: 11/01/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations, Talent
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a9d0d9a3f278a09e89311ee75b6f95fb4f3b04cb
ms.openlocfilehash: 2cce715ea17689ec128e31e9d6cff0b052c9ca9a
ms.contentlocale: fi-fi
ms.lasthandoff: 02/02/2018

---
# <a name="create-loan-items"></a><span data-ttu-id="5eff4-103">Luo lainauskohteet</span><span class="sxs-lookup"><span data-stu-id="5eff4-103">Create loan items</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5eff4-104">Lainan kohteet ovat tietueita, joiden avulla voit seurata fyysisiä yrityksen työntekijöille lainaamia kohteita, kuten puhelimia ja tietokoneita.</span><span class="sxs-lookup"><span data-stu-id="5eff4-104">Loan items are records that help you track physical items, such as phones or computers, that your company lends to workers.</span></span> <span data-ttu-id="5eff4-105">Jokaisella fyysisellä kohteella on oltava vastaava lainan kohde.</span><span class="sxs-lookup"><span data-stu-id="5eff4-105">Each physical item must have a corresponding loan item.</span></span> <span data-ttu-id="5eff4-106">Jokaisessa lainan kohteen tietueessa tulisi kuvailla, mitä lainataan, kuka vastaa lainasta sekä aika (päivinä), jonka kohde voi olla lainassa.</span><span class="sxs-lookup"><span data-stu-id="5eff4-106">Each loan item record should describe what is being loaned, who is responsible for the loan, and the number of days the item can be on loan.</span></span> <span data-ttu-id="5eff4-107">Voit luoda samalla useita lainan kohteita, kuten avaimia, kulkukortteja tai työpukuja.</span><span class="sxs-lookup"><span data-stu-id="5eff4-107">You can create multiple loan items, such as keys, access cards, or uniforms, at the same time.</span></span> <span data-ttu-id="5eff4-108">Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="5eff4-108">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-loan-types"></a><span data-ttu-id="5eff4-109">Lainatyyppien luominen</span><span class="sxs-lookup"><span data-stu-id="5eff4-109">Create Loan types</span></span>
1. <span data-ttu-id="5eff4-110">Valitse Henkilöstöhallinto > Työntekijät > Lainan kohteet > Lainatyypit.</span><span class="sxs-lookup"><span data-stu-id="5eff4-110">Go to Human resources > Workers > Loan items > Loan types.</span></span>
2. <span data-ttu-id="5eff4-111">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="5eff4-111">Click New.</span></span>
3. <span data-ttu-id="5eff4-112">Syötä arvo Lainatyyppi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="5eff4-112">In the Loan type field, type a value.</span></span>
4. <span data-ttu-id="5eff4-113">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="5eff4-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="5eff4-114">Määritä, kuinka monta päivää tätä lainatyyppiä olevat nimikkeet voivat olla myöhässä.</span><span class="sxs-lookup"><span data-stu-id="5eff4-114">Enter the number of days that items assigned to this loan type can be overdue.</span></span> 
6. <span data-ttu-id="5eff4-115">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="5eff4-115">Click Save.</span></span>
7. <span data-ttu-id="5eff4-116">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="5eff4-116">Close the page.</span></span>
8. <span data-ttu-id="5eff4-117">Päivitä sivu.</span><span class="sxs-lookup"><span data-stu-id="5eff4-117">Refresh the page.</span></span>

## <a name="create-loan-items"></a><span data-ttu-id="5eff4-118">Luo lainauskohteet</span><span class="sxs-lookup"><span data-stu-id="5eff4-118">Create Loan items</span></span>
1. <span data-ttu-id="5eff4-119">Valitse Henkilöstöhallinto > Työntekijät > Lainan kohteet > Lainan kohteet.</span><span class="sxs-lookup"><span data-stu-id="5eff4-119">Go to Human resources > Workers > Loan items > Loan items.</span></span>
2. <span data-ttu-id="5eff4-120">Valitse Luo lainan kohteita.</span><span class="sxs-lookup"><span data-stu-id="5eff4-120">Click Create loan items.</span></span>
3. <span data-ttu-id="5eff4-121">Syötä Määrä-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="5eff4-121">In the Qty. field, enter a number.</span></span>
4. <span data-ttu-id="5eff4-122">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="5eff4-122">In the Description field, type a value.</span></span>
5. <span data-ttu-id="5eff4-123">Avaa haku valitsemalla Lainatyyppi-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="5eff4-123">In the Loan type field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="5eff4-124">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="5eff4-124">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="5eff4-125">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="5eff4-125">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="5eff4-126">Määritä, miten monta päivää kohde voi olla lainassa.</span><span class="sxs-lookup"><span data-stu-id="5eff4-126">Enter the number of days the item can be on loan.</span></span>
    * <span data-ttu-id="5eff4-127">Lainatut välineet -sivun Suunniteltu palautus -kentän oletusarvo lasketaan lisäämällä kuluvaan päivämäärään tämä numero.</span><span class="sxs-lookup"><span data-stu-id="5eff4-127">The default value for the Planned return field on the Loaned equipment page is calculated as the current date plus this number.</span></span>  
9. <span data-ttu-id="5eff4-128">Avaa haku valitsemalla Vastuuhenkilö-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="5eff4-128">In the Person in charge field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="5eff4-129">Klikkaa Valitse.</span><span class="sxs-lookup"><span data-stu-id="5eff4-129">Click Select.</span></span>
11. <span data-ttu-id="5eff4-130">Syötä numero Aloitusarvo-kenttään.</span><span class="sxs-lookup"><span data-stu-id="5eff4-130">In the Starting value field, enter a number.</span></span>
12. <span data-ttu-id="5eff4-131">Syötä numero Väli-kenttään.</span><span class="sxs-lookup"><span data-stu-id="5eff4-131">In the Interval field, enter a number.</span></span>
13. <span data-ttu-id="5eff4-132">Syötä arvo Muoto-kenttään.</span><span class="sxs-lookup"><span data-stu-id="5eff4-132">In the Format field, type a value.</span></span>
    * <span data-ttu-id="5eff4-133">Jos lainan kohteen aloitusnumero on esimerkiksi 10, syötä Muoto-kenttään kaksi numeroa.</span><span class="sxs-lookup"><span data-stu-id="5eff4-133">For example, if the starting number for a loan item is 10, enter two number symbols in the Format field.</span></span>  
14. <span data-ttu-id="5eff4-134">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="5eff4-134">Click OK.</span></span>
15. <span data-ttu-id="5eff4-135">Päivitä sivu.</span><span class="sxs-lookup"><span data-stu-id="5eff4-135">Refresh the page.</span></span>


