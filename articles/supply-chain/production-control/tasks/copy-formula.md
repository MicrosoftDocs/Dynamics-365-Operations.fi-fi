---
title: Kopioi kaava
description: Tässä menettelyssä keskitytään luomaan resepti, joka sisältää samat ainesosat kuin aiemmin luotu resepti, mutta jossa on vähemmän eroja.
author: ShylaThompson
manager: tfehr
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0643209f7ef5090684db693bea2483fadcf3760b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4998775"
---
# <a name="copy-a-formula"></a><span data-ttu-id="a74a2-103">Kopioi kaava</span><span class="sxs-lookup"><span data-stu-id="a74a2-103">Copy a formula</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a74a2-104">Tässä menettelyssä keskitytään luomaan resepti, joka sisältää samat ainesosat kuin aiemmin luotu resepti, mutta jossa on vähemmän eroja.</span><span class="sxs-lookup"><span data-stu-id="a74a2-104">This procedure focuses on creating a formula that includes the same ingredients as an existing formula, but with minor differences.</span></span> <span data-ttu-id="a74a2-105">Voit luoda reseptirivit kopioimalla kopiointitoiminnolla sellainen aiemmin luotu resepti, joka sisältää eniten tarvitsemiasi ainesosia.</span><span class="sxs-lookup"><span data-stu-id="a74a2-105">To create the formula lines, you can use the Copy function to copy an existing formula that has most of the ingredients that you need.</span></span> <span data-ttu-id="a74a2-106">Sitten voit tehdä uuden version yksittäisille riveille tarvittavat muutokset.</span><span class="sxs-lookup"><span data-stu-id="a74a2-106">You can then make any necessary changes to the individual lines in the new version.</span></span> <span data-ttu-id="a74a2-107">Kopiointitoiminnon ansiosta ei tarvitse tehdä useita lähes samanlaisia reseptejä.</span><span class="sxs-lookup"><span data-stu-id="a74a2-107">By using the Copy function, you do not have to create multiple formulas that are almost identical.</span></span> <span data-ttu-id="a74a2-108">Tämän tehtävän luomisessa käytetty demotietojen yritys on USP2.</span><span class="sxs-lookup"><span data-stu-id="a74a2-108">The demo data company used to create this task is USP2.</span></span>


## <a name="create-a-formula"></a><span data-ttu-id="a74a2-109">Reseptin luominen</span><span class="sxs-lookup"><span data-stu-id="a74a2-109">Create a formula</span></span>
1. <span data-ttu-id="a74a2-110">Valitse Tuotetietojen hallinta > Tuoterakenteet ja kaavat > Reseptit.</span><span class="sxs-lookup"><span data-stu-id="a74a2-110">Go to Product information management > Bills of materials and formulas > Formulas.</span></span>
2. <span data-ttu-id="a74a2-111">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="a74a2-111">Click New.</span></span>
3. <span data-ttu-id="a74a2-112">Kirjoita arvo Resepti-kenttään.</span><span class="sxs-lookup"><span data-stu-id="a74a2-112">In the Formula field, type a value.</span></span>
4. <span data-ttu-id="a74a2-113">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="a74a2-113">In the Name field, type a value.</span></span>
    * <span data-ttu-id="a74a2-114">Syötä reseptille uusi merkityksellinen nimi.</span><span class="sxs-lookup"><span data-stu-id="a74a2-114">Type a meaningful name for the formula.</span></span>  
5. <span data-ttu-id="a74a2-115">Avaa haku napsauttamalla Toimipaikka-kentässä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="a74a2-115">In the Site field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="a74a2-116">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="a74a2-116">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="a74a2-117">Avaa haku valitsemalla Nimikeryhmä-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="a74a2-117">In the Item group field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="a74a2-118">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="a74a2-118">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="a74a2-119">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="a74a2-119">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="a74a2-120">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="a74a2-120">Click Save.</span></span>

## <a name="copy-formula-lines"></a><span data-ttu-id="a74a2-121">Reseptirivien kopioiminen</span><span class="sxs-lookup"><span data-stu-id="a74a2-121">Copy formula lines</span></span>
1. <span data-ttu-id="a74a2-122">Valitse toimintoruudussa Resepti.</span><span class="sxs-lookup"><span data-stu-id="a74a2-122">On the Action Pane, click Formula.</span></span>
2. <span data-ttu-id="a74a2-123">Valitse Kopioi.</span><span class="sxs-lookup"><span data-stu-id="a74a2-123">Click Copy.</span></span>
3. <span data-ttu-id="a74a2-124">Avaa haku valitsemalla Nimiketunnus-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="a74a2-124">In the Item number field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="a74a2-125">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="a74a2-125">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="a74a2-126">Avaa haku valitsemalla Reseptiversio-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="a74a2-126">In the Formula version field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="a74a2-127">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="a74a2-127">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="a74a2-128">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="a74a2-128">Click OK.</span></span>

## <a name="adjust-copied-formula-lines"></a><span data-ttu-id="a74a2-129">Kopioitujen reseptirivien oikaisu</span><span class="sxs-lookup"><span data-stu-id="a74a2-129">Adjust copied formula lines</span></span>
1. <span data-ttu-id="a74a2-130">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="a74a2-130">In the list, mark the selected row.</span></span>
2. <span data-ttu-id="a74a2-131">Valitse Poista.</span><span class="sxs-lookup"><span data-stu-id="a74a2-131">Click Delete.</span></span>
3. <span data-ttu-id="a74a2-132">Valitse Kyllä.</span><span class="sxs-lookup"><span data-stu-id="a74a2-132">Click Yes.</span></span>

## <a name="approve-formula"></a><span data-ttu-id="a74a2-133">Hyväksy resepti</span><span class="sxs-lookup"><span data-stu-id="a74a2-133">Approve formula</span></span>
1. <span data-ttu-id="a74a2-134">Valitse toimintoruudussa Resepti.</span><span class="sxs-lookup"><span data-stu-id="a74a2-134">On the Action Pane, click Formula.</span></span>
2. <span data-ttu-id="a74a2-135">Valitse Hyväksy resepti.</span><span class="sxs-lookup"><span data-stu-id="a74a2-135">Click Approve formula.</span></span>
3. <span data-ttu-id="a74a2-136">Avaa haku valitsemalla Hyväksynyt-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="a74a2-136">In the Approved by field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="a74a2-137">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="a74a2-137">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="a74a2-138">Klikkaa Valitse.</span><span class="sxs-lookup"><span data-stu-id="a74a2-138">Click Select.</span></span>
6. <span data-ttu-id="a74a2-139">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="a74a2-139">Click OK.</span></span>

