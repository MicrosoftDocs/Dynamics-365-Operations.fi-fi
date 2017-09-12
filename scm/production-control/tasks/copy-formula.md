--- 
title: Kopioi kaava
description: "Tässä menettelyssä keskitytään luomaan resepti, joka sisältää samat ainesosat kuin aiemmin luotu resepti, mutta jossa on vähemmän eroja."
author: YuyuScheller
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 036bd9f592ca584afad9d4b9b7a49a9787076056
ms.contentlocale: fi-fi
ms.lasthandoff: 08/29/2017

---
# <a name="copy-a-formula"></a><span data-ttu-id="4acb0-103">Kopioi kaava</span><span class="sxs-lookup"><span data-stu-id="4acb0-103">Copy a formula</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4acb0-104">Tässä menettelyssä keskitytään luomaan resepti, joka sisältää samat ainesosat kuin aiemmin luotu resepti, mutta jossa on vähemmän eroja.</span><span class="sxs-lookup"><span data-stu-id="4acb0-104">This procedure focuses on creating a formula that includes the same ingredients as an existing formula, but with minor differences.</span></span> <span data-ttu-id="4acb0-105">Voit luoda reseptirivit kopioimalla kopiointitoiminnolla sellainen aiemmin luotu resepti, joka sisältää eniten tarvitsemiasi ainesosia.</span><span class="sxs-lookup"><span data-stu-id="4acb0-105">To create the formula lines, you can use the Copy function to copy an existing formula that has most of the ingredients that you need.</span></span> <span data-ttu-id="4acb0-106">Sitten voit tehdä uuden version yksittäisille riveille tarvittavat muutokset.</span><span class="sxs-lookup"><span data-stu-id="4acb0-106">You can then make any necessary changes to the individual lines in the new version.</span></span> <span data-ttu-id="4acb0-107">Kopiointitoiminnon ansiosta ei tarvitse tehdä useita lähes samanlaisia reseptejä.</span><span class="sxs-lookup"><span data-stu-id="4acb0-107">By using the Copy function, you do not have to create multiple formulas that are almost identical.</span></span> <span data-ttu-id="4acb0-108">Tämän tehtävän luomisessa käytetty demotietojen yritys on USP2.</span><span class="sxs-lookup"><span data-stu-id="4acb0-108">The demo data company used to create this task is USP2.</span></span>


## <a name="create-a-formula"></a><span data-ttu-id="4acb0-109">Reseptin luominen</span><span class="sxs-lookup"><span data-stu-id="4acb0-109">Create a formula</span></span>
1. <span data-ttu-id="4acb0-110">Valitse Tuotetietojen hallinta > Tuoterakenteet ja kaavat > Reseptit.</span><span class="sxs-lookup"><span data-stu-id="4acb0-110">Go to Product information management > Bills of materials and formulas > Formulas.</span></span>
2. <span data-ttu-id="4acb0-111">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="4acb0-111">Click New.</span></span>
3. <span data-ttu-id="4acb0-112">Kirjoita arvo Resepti-kenttään.</span><span class="sxs-lookup"><span data-stu-id="4acb0-112">In the Formula field, type a value.</span></span>
4. <span data-ttu-id="4acb0-113">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="4acb0-113">In the Name field, type a value.</span></span>
    * <span data-ttu-id="4acb0-114">Syötä reseptille uusi merkityksellinen nimi.</span><span class="sxs-lookup"><span data-stu-id="4acb0-114">Type a meaningful name for the formula.</span></span>  
5. <span data-ttu-id="4acb0-115">Avaa haku napsauttamalla Toimipaikka-kentässä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="4acb0-115">In the Site field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="4acb0-116">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="4acb0-116">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="4acb0-117">Avaa haku valitsemalla Nimikeryhmä-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="4acb0-117">In the Item group field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="4acb0-118">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="4acb0-118">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="4acb0-119">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="4acb0-119">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="4acb0-120">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="4acb0-120">Click Save.</span></span>

## <a name="copy-formula-lines"></a><span data-ttu-id="4acb0-121">Reseptirivien kopioiminen</span><span class="sxs-lookup"><span data-stu-id="4acb0-121">Copy formula lines</span></span>
1. <span data-ttu-id="4acb0-122">Valitse toimintoruudussa Resepti.</span><span class="sxs-lookup"><span data-stu-id="4acb0-122">On the Action Pane, click Formula.</span></span>
2. <span data-ttu-id="4acb0-123">Valitse Kopioi.</span><span class="sxs-lookup"><span data-stu-id="4acb0-123">Click Copy.</span></span>
3. <span data-ttu-id="4acb0-124">Avaa haku valitsemalla Nimiketunnus-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="4acb0-124">In the Item number field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="4acb0-125">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="4acb0-125">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="4acb0-126">Avaa haku valitsemalla Reseptiversio-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="4acb0-126">In the Formula version field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="4acb0-127">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="4acb0-127">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="4acb0-128">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="4acb0-128">Click OK.</span></span>

## <a name="adjust-copied-formula-lines"></a><span data-ttu-id="4acb0-129">Kopioitujen reseptirivien oikaisu</span><span class="sxs-lookup"><span data-stu-id="4acb0-129">Adjust copied formula lines</span></span>
1. <span data-ttu-id="4acb0-130">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="4acb0-130">In the list, mark the selected row.</span></span>
2. <span data-ttu-id="4acb0-131">Valitse Poista.</span><span class="sxs-lookup"><span data-stu-id="4acb0-131">Click Delete.</span></span>
3. <span data-ttu-id="4acb0-132">Valitse Kyllä.</span><span class="sxs-lookup"><span data-stu-id="4acb0-132">Click Yes.</span></span>

## <a name="approve-formula"></a><span data-ttu-id="4acb0-133">Hyväksy resepti</span><span class="sxs-lookup"><span data-stu-id="4acb0-133">Approve formula</span></span>
1. <span data-ttu-id="4acb0-134">Valitse toimintoruudussa Resepti.</span><span class="sxs-lookup"><span data-stu-id="4acb0-134">On the Action Pane, click Formula.</span></span>
2. <span data-ttu-id="4acb0-135">Valitse Hyväksy resepti.</span><span class="sxs-lookup"><span data-stu-id="4acb0-135">Click Approve formula.</span></span>
3. <span data-ttu-id="4acb0-136">Avaa haku valitsemalla Hyväksynyt-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="4acb0-136">In the Approved by field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="4acb0-137">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="4acb0-137">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="4acb0-138">Klikkaa Valitse.</span><span class="sxs-lookup"><span data-stu-id="4acb0-138">Click Select.</span></span>
6. <span data-ttu-id="4acb0-139">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="4acb0-139">Click OK.</span></span>


