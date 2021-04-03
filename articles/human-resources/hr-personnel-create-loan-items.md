---
title: Luo lainauskohteet
description: Lainan kohteet ovat tietueita, joiden avulla voit seurata fyysisiä yrityksen työntekijöille lainaamia kohteita, kuten puhelimia ja tietokoneita.
author: andreabichsel
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmLoanType, DefaultDashboard, HcmLoanItem, HcmWorkerLookUp, HcmPersonnelManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5b93f68790a72af28130d80ed189538f9c5c87ab
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/17/2021
ms.locfileid: "5467096"
---
# <a name="create-loan-items"></a><span data-ttu-id="c4933-103">Luo lainauskohteet</span><span class="sxs-lookup"><span data-stu-id="c4933-103">Create loan items</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



<span data-ttu-id="c4933-104">Lainan kohteet ovat tietueita, joiden avulla voit seurata fyysisiä yrityksen työntekijöille lainaamia kohteita, kuten puhelimia ja tietokoneita.</span><span class="sxs-lookup"><span data-stu-id="c4933-104">Loan items are records that help you track physical items, such as phones or computers, that your company lends to workers.</span></span> <span data-ttu-id="c4933-105">Jokaisella fyysisellä kohteella on oltava vastaava lainan kohde.</span><span class="sxs-lookup"><span data-stu-id="c4933-105">Each physical item must have a corresponding loan item.</span></span> <span data-ttu-id="c4933-106">Jokaisessa lainan kohteen tietueessa tulisi kuvailla, mitä lainataan, kuka vastaa lainasta sekä aika (päivinä), jonka kohde voi olla lainassa.</span><span class="sxs-lookup"><span data-stu-id="c4933-106">Each loan item record should describe what is being loaned, who is responsible for the loan, and the number of days the item can be on loan.</span></span> <span data-ttu-id="c4933-107">Voit luoda samalla useita lainan kohteita, kuten avaimia, kulkukortteja tai työpukuja.</span><span class="sxs-lookup"><span data-stu-id="c4933-107">You can create multiple loan items, such as keys, access cards, or uniforms, at the same time.</span></span> <span data-ttu-id="c4933-108">Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="c4933-108">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-loan-types"></a><span data-ttu-id="c4933-109">Lainatyyppien luominen</span><span class="sxs-lookup"><span data-stu-id="c4933-109">Create Loan types</span></span>
1. <span data-ttu-id="c4933-110">Valitse Henkilöstöhallinto > Työntekijät > Lainan kohteet > Lainatyypit.</span><span class="sxs-lookup"><span data-stu-id="c4933-110">Go to Human resources > Workers > Loan items > Loan types.</span></span>
2. <span data-ttu-id="c4933-111">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="c4933-111">Click New.</span></span>
3. <span data-ttu-id="c4933-112">Syötä arvo Lainatyyppi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="c4933-112">In the Loan type field, type a value.</span></span>
4. <span data-ttu-id="c4933-113">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="c4933-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="c4933-114">Määritä, kuinka monta päivää tätä lainatyyppiä olevat nimikkeet voivat olla myöhässä.</span><span class="sxs-lookup"><span data-stu-id="c4933-114">Enter the number of days that items assigned to this loan type can be overdue.</span></span> 
6. <span data-ttu-id="c4933-115">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="c4933-115">Click Save.</span></span>
7. <span data-ttu-id="c4933-116">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="c4933-116">Close the page.</span></span>
8. <span data-ttu-id="c4933-117">Päivitä sivu.</span><span class="sxs-lookup"><span data-stu-id="c4933-117">Refresh the page.</span></span>

## <a name="create-loan-items"></a><span data-ttu-id="c4933-118">Luo lainauskohteet</span><span class="sxs-lookup"><span data-stu-id="c4933-118">Create Loan items</span></span>
1. <span data-ttu-id="c4933-119">Valitse Henkilöstöhallinto > Työntekijät > Lainan kohteet > Lainan kohteet.</span><span class="sxs-lookup"><span data-stu-id="c4933-119">Go to Human resources > Workers > Loan items > Loan items.</span></span>
2. <span data-ttu-id="c4933-120">Valitse Luo lainan kohteita.</span><span class="sxs-lookup"><span data-stu-id="c4933-120">Click Create loan items.</span></span>
3. <span data-ttu-id="c4933-121">Syötä Määrä-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="c4933-121">In the Qty. field, enter a number.</span></span>
4. <span data-ttu-id="c4933-122">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="c4933-122">In the Description field, type a value.</span></span>
5. <span data-ttu-id="c4933-123">Avaa haku valitsemalla Lainatyyppi-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="c4933-123">In the Loan type field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="c4933-124">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="c4933-124">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="c4933-125">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="c4933-125">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="c4933-126">Määritä, miten monta päivää kohde voi olla lainassa.</span><span class="sxs-lookup"><span data-stu-id="c4933-126">Enter the number of days the item can be on loan.</span></span>
    * <span data-ttu-id="c4933-127">Lainatut välineet -sivun Suunniteltu palautus -kentän oletusarvo lasketaan lisäämällä kuluvaan päivämäärään tämä numero.</span><span class="sxs-lookup"><span data-stu-id="c4933-127">The default value for the Planned return field on the Loaned equipment page is calculated as the current date plus this number.</span></span>  
9. <span data-ttu-id="c4933-128">Avaa haku valitsemalla Vastuuhenkilö-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="c4933-128">In the Person in charge field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="c4933-129">Klikkaa Valitse.</span><span class="sxs-lookup"><span data-stu-id="c4933-129">Click Select.</span></span>
11. <span data-ttu-id="c4933-130">Syötä numero Aloitusarvo-kenttään.</span><span class="sxs-lookup"><span data-stu-id="c4933-130">In the Starting value field, enter a number.</span></span>
12. <span data-ttu-id="c4933-131">Syötä numero Väli-kenttään.</span><span class="sxs-lookup"><span data-stu-id="c4933-131">In the Interval field, enter a number.</span></span>
13. <span data-ttu-id="c4933-132">Syötä arvo Muoto-kenttään.</span><span class="sxs-lookup"><span data-stu-id="c4933-132">In the Format field, type a value.</span></span>
    * <span data-ttu-id="c4933-133">Jos lainan kohteen aloitusnumero on esimerkiksi 10, syötä numero Muoto-kenttään kaksi numeromerkkiä.</span><span class="sxs-lookup"><span data-stu-id="c4933-133">For example, if the starting number for a loan item is 10, enter two number symbols symbols in the Format field.</span></span>  
14. <span data-ttu-id="c4933-134">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="c4933-134">Click OK.</span></span>
15. <span data-ttu-id="c4933-135">Päivitä sivu.</span><span class="sxs-lookup"><span data-stu-id="c4933-135">Refresh the page.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]