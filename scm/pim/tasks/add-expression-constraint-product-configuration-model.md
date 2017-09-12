--- 
title: "Lisää rajoituslauseke tuotemääritysmalliin"
description: "Tässä menettelyssä käsitellään, miten uusi rajoituslauseke lisätään tuotemääritysmalliin."
author: YuyuScheller
manager: AnnBe
ms.date: 10/27/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 8db46c5b8361c96745b440c0d0684e18c06a6c6f
ms.contentlocale: fi-fi
ms.lasthandoff: 08/29/2017

---
# <a name="add-an-expression-constraint-to-a-product-configuration-model"></a><span data-ttu-id="34dbd-103">Lisää rajoituslauseke tuotemääritysmalliin</span><span class="sxs-lookup"><span data-stu-id="34dbd-103">Add an expression constraint to a product configuration model</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="34dbd-104">Tässä menettelyssä käsitellään, miten uusi rajoituslauseke lisätään tuotemääritysmalliin.</span><span class="sxs-lookup"><span data-stu-id="34dbd-104">This procedure shows how you can add a new constraint expression to a product configuration model.</span></span> <span data-ttu-id="34dbd-105">Se näyttää, miten voit määrätä, että kulmasuojausta on käytettävä kaiuttimessa, jos käyttäjä on valinnut metallin etusäleikköön.</span><span class="sxs-lookup"><span data-stu-id="34dbd-105">It shows how you can mandate that corner protection must be applied to a speaker if the user has selected a front grill in metal.</span></span> <span data-ttu-id="34dbd-106">Menettely käyttää USMF-demoyrityksen Korkealaatuinen kaiutin -komponenttia.</span><span class="sxs-lookup"><span data-stu-id="34dbd-106">The procedure uses the High end speaker component in the demo company USMF.</span></span>


## <a name="create-an-expression-constraint"></a><span data-ttu-id="34dbd-107">Luo lausekerajoitus</span><span class="sxs-lookup"><span data-stu-id="34dbd-107">Create an expression constraint</span></span>
1. <span data-ttu-id="34dbd-108">Valitse Tuotevarianttimallin määritys.</span><span class="sxs-lookup"><span data-stu-id="34dbd-108">Click Product variant model definition.</span></span>
2. <span data-ttu-id="34dbd-109">Valitse Tuotekonfiguraation mallit.</span><span class="sxs-lookup"><span data-stu-id="34dbd-109">Click Product configuration models.</span></span>
3. <span data-ttu-id="34dbd-110">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="34dbd-110">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="34dbd-111">Tässä esimerkissä käytetään Korkealaatuinen kaiutin -mallia.</span><span class="sxs-lookup"><span data-stu-id="34dbd-111">This example uses the high end speaker model.</span></span>  
4. <span data-ttu-id="34dbd-112">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="34dbd-112">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="34dbd-113">Laajenna Rajoitukset-osa.</span><span class="sxs-lookup"><span data-stu-id="34dbd-113">Expand the Constraints section.</span></span>
6. <span data-ttu-id="34dbd-114">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="34dbd-114">Click Add.</span></span>
7. <span data-ttu-id="34dbd-115">Valitse Luo.</span><span class="sxs-lookup"><span data-stu-id="34dbd-115">Click Create.</span></span>
8. <span data-ttu-id="34dbd-116">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="34dbd-116">In the Name field, type a value.</span></span>

## <a name="enter-expression"></a><span data-ttu-id="34dbd-117">Anna lauseke</span><span class="sxs-lookup"><span data-stu-id="34dbd-117">Enter expression</span></span>
1. <span data-ttu-id="34dbd-118">Valitse Muokkaa lauseketta.</span><span class="sxs-lookup"><span data-stu-id="34dbd-118">Click Edit expression.</span></span>
    * <span data-ttu-id="34dbd-119">Jos vapautat käyttöliittymän tehtävätallenteen tässä vaiheessa, voit muodostaa rajoituslausekkeen IntelliSensen ja symboliluettelon avulla.</span><span class="sxs-lookup"><span data-stu-id="34dbd-119">If you unlock the user interface in the task recording at this stage, you can use IntelliSense and the list of symbols to build the constraint expression .</span></span>  
2. <span data-ttu-id="34dbd-120">Lisää ConstraintBody-kenttään Implies[FrontGrill=="Metal", CornerProtection].</span><span class="sxs-lookup"><span data-stu-id="34dbd-120">In the ConstraintBody field, enter 'Implies[FrontGrill=="Metal", CornerProtection] '.</span></span>
    * <span data-ttu-id="34dbd-121">Tämän lausekkeen logiikka ilmaisee, että jos etusäleikkö on metallia, sitten kulmasuojausvaihtoehto on valittava.</span><span class="sxs-lookup"><span data-stu-id="34dbd-121">This expression logic states: If the Front grill is  metal, then the corner protection option must be selected.</span></span>  
3. <span data-ttu-id="34dbd-122">Valitse Vahvista.</span><span class="sxs-lookup"><span data-stu-id="34dbd-122">Click Validate.</span></span>
    * <span data-ttu-id="34dbd-123">Vahvistustoiminto suoritetaan rajoitelausekkeessa, jossa se tarkistaa syntaksivirheet.</span><span class="sxs-lookup"><span data-stu-id="34dbd-123">The validate function runs through the constraint expression and checks for syntax errors.</span></span>  
4. <span data-ttu-id="34dbd-124">Valitse Sulje.</span><span class="sxs-lookup"><span data-stu-id="34dbd-124">Click Close.</span></span>
5. <span data-ttu-id="34dbd-125">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="34dbd-125">Click OK.</span></span>


